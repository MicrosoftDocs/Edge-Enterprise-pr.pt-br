---
title: 'Configuração por Site por Política '
ms.author: collw
author: AndreaLBarr
manager: laurawi
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: 'Configuração por Site por Política '
ms.openlocfilehash: d7cc68264c9fca9e667908ff4988f512c152bfc4857fd14166519fb3eb337a5a
ms.sourcegitcommit: d44c0997ffe40d67421312ed96e7766da947eaa0
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/05/2021
ms.locfileid: "11725584"
---
# <a name="persite-configuration-by-policy"></a>Configuração por Site por Política

## <a name="introduction-browsers-as-decision-makers"></a>Introdução: Navegadores como Tomadores de Decisão

Como parte de cada carregamento de página, os navegadores toma muitas decisões. Uma API específica deve estar disponível? Uma carga de recursos deve ser permitida? O script deve ter permissão para ser executado? A lista é longa.

Na maioria dos casos, as decisões são regidas por duas entradas: uma configuração de usuário e a URL da página para a qual a decisão está sendo tomada.

Na plataforma Web Internet Explorer herdada, cada uma dessas decisões foi chamada de [urlAction](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537178%28v%3dvs.85%29)e configurações de usuário e Política de Grupo Enterprise dentro do Painel Controle de Internet controlava como o navegador lidava com cada decisão.  

No Microsoft Edge, a maioria das permissões por site é controlada por configurações e políticas expressas usando uma sintaxe simples com suporte limitado a curinga. As Zonas de Segurança do Windows ainda são usadas apenas para um pequeno número de decisões de configuração.

## <a name="background-windows-security-zones"></a>Histórico: Zonas de Segurança do Windows

Para simplificar a configuração para o usuário ou seu administrador, a plataforma herdada classificava os sites em cinco ** Zonas de Segurança diferentes:** Máquina Local, Intranet Local, Confiável, Internet e Sites Restritos.

Ao tomar uma decisão, o navegador primeiro mapeava o site para uma Zona e, em seguida, consultava a configuração dessa URLAction para essa Zona para decidir o que fazer. Padrões razoáveis, como "Atender automaticamente aos desafios de autenticação da minha Intranet", significavam que a maioria dos usuários nunca precisavam alterar as configurações para fora de seus padrões.

Os usuários podem usar o Painel Controle de internet para atribuir sites específicos a Zonas e configurar os resultados de permissão para cada zona. Em ambientes gerenciados, os administradores podem usar Política de Grupo para atribuir sites específicos a Zonas (por meio da política "Lista de Atribuições de Site a Zona") e especificar as configurações para URLActions por zona. Além da atribuição manual administrativa ou de usuário de sites a Zonas, a heurística adicional poderia [atribuir sites à Zona da Intranet Local](/archive/blogs/ieinternals/the-intranet-zone). Em particular, nomes de host sem ponto (por exemplo, `http://payroll`) eram atribuídos à Zona da Intranet. Se um script de Configuração de Proxy tivesse sido usado, todos os sites configurados para ignorar o proxy seriam mapeados para a Zona da Intranet.

A Versão Prévia do Microsoft Edge herdou a arquitetura de Zonas de seu predecessor, o Internet Explorer, com algumas alterações simplificadas:

- As cinco Zonas internas do Windows foram reduzidas para três: Internet (Internet), Confiável (Intranet+Confiável) e Computador Local. A Zona de Sites Restritos foi removida.

- Os mapeamentos de Zona para URLAction foram codificados no navegador, ignorando as Políticas de Grupo e as configurações no Painel Controle de Internet.

## <a name="per-site-permissions-in-the-microsoft-edge"></a>Permissões por site no Microsoft Edge

Ao contrário de seus predecessores, o novo Microsoft Edge faz uso muito limitado das Xonas de Segurança do Windows. Em vez disso, a maioria das permissões e recursos que oferecem aos administradores configuração por site por meio de  [política](/deployedge/microsoft-edge-policies) depende de listas de regras no  [Formato de Filtro de URL](/DeployEdge/edge-learnmmore-url-list-filter%20format).

Quando os usuários finais abrirem <code>edge://settings/content/siteDetails?site=https://example.com</code>, eles encontrarão uma longa lista de opções de configuração e listas para várias permissões. Os usuários raramente usam a Página de Configurações diretamente, fazendo escolhas durante a navegação usando vários widgets e alternâncias na lista suspensa de  **Informações da Página**  (que aparece quando você clica no ícone de bloqueio na barra de endereços) ou por meio de vários prompts ou botões na borda direita da barra de endereços.

As empresas podem usar Política de Grupo para provisionar listas de sites para políticas individuais que controlam o comportamento do navegador. Para localizar essas políticas, basta abrir a [documentação de Política de Grupo do Microsoft Edge](/deployedge/microsoft-edge-policies) e pesquisar por **ForUrls** para localizar as políticas que permitem e bloqueiam o comportamento com base na URL do site carregado. A maioria das configurações relevantes é listada na seção [Configurações de Política de Grupo para Conteúdo](/deployedge/microsoft-edge-policies#content-settings).

Também há várias políticas (cujos nomes contêm **Padrão**) que controlam o comportamento padrão de uma determinada configuração.

Muitas das configurações são muito desconhecidas (WebSerial, WebMIDI) e, muitas vezes, não há motivo para alterar uma configuração para fora do padrão (Imagens).

## <a name="common-questions"></a>Perguntas comuns

## <a name="q-can-the-url-filter-format-match-on-a-sites-ip-address"></a>P: O Formato do Filtro de URL pode corresponder ao endereço IP de um site?

Não, o formato não dá suporte à especificação de um intervalo de IP para listas de permissão e bloqueio. Ele dá suporte à especificação de **literais** de IP individuais, mas essas regras só serão respeitadas se o usuário navegar até o site usando esse literal (por exemplo: <http://127.0.0.1/>). Se um nome de host for usado (<http://localhost>), a regra de literal de IP não será respeitada, mesmo que o IP resolvido do host corresponda ao IP listado pelo filtro.

## <a name="q-can-url-filters-matchjustdotless-host-names"></a>P: Os filtros de URL podem corresponder apenas a nomes de host sem ponto?

Não. Você deve listar individualmente cada nome de host desejado, por exemplo: (`https://payroll`, `https://stock`, `https://who`, etc).

Se você estava pensando o suficiente para estruturar sua intranet de modo que seus nomes de host estejam no formato:

- <div style="display: inline">`https://payroll.contoso-intranet.com`</div>

- <div style="display: inline">`https://timecard.contoso-intranet.com`</div>

- <div style="display: inline">`https://sharepoint.contoso-intranet.com`</div>

Parabéns, você implementou uma prática recomendada. Você pode configurar cada política desejada com uma entrada ***.contoso-intranet.com** e toda a Intranet será aceita.

## <a name="use-of-security-zones-inthe-microsoft-edge"></a>Uso de Zonas de Segurança no Microsoft Edge

Embora o Microsoft Edge dependa principalmente de políticas individuais que usam o formato de Filtro de URL, ele continua a usar as Zonas de Segurança do Windows por padrão em um pequeno número de locais para simplificar a implantação em Empresas que, historicamente, se baseiam na configuração de Zonas. Os seguintes comportamentos são controlados pela Política de zona:

1. Ao decidir se deseja liberar automaticamente as credenciais da Autenticação Integrada do Windows (Kerberos/NTLM)

2. Ao decidir como lidar com Downloads de Arquivos

3. Para o Modo Internet Explorer

## <a name="credential-release"></a>Liberação de Credencial

Por padrão, o Microsoft Edge avaliará URLACTION_CREDENTIALS_USE para decidir se a Autenticação Integrada do Windows é usada automaticamente ou se o usuário deverá ver um prompt de autenticação manual. Configurar uma [política de lista de site AuthServerAllowlist](/deployedge/microsoft-edge-policies#authserverallowlist) impedirá que a Política de Zona seja consultada.

## <a name="file-downloads"></a>Downloads de arquivos

Evidências sobre as origens de um download de arquivo (a chamada "[Marca da Web](https://textslashplain.com/2016/04/04/downloads-and-the-mark-of-the-web/) é registrada para arquivos baixados da Zona da Internet. Outros aplicativos (por exemplo, o Shell do Windows, Microsoft Office, etc.) podem levar essa evidência de origem em consideração ao decidir como lidar com um arquivo.

Se a política de Zona de Segurança do Windows estiver configurada para Desabilitar a configuração Iniciando aplicativos e arquivos não seguros, o gerenciador de downloads do Microsoft Edge bloqueará downloads de arquivos de sites nessa Zona com uma observação: "Não foi possível baixar: bloqueado".  

## <a name="ie-mode"></a>Modo IE

O modo IE pode ser configurado para [todos os sites da Intranet no modo IE](/deployedge/edge-ie-mode#configure-all-intranet-sites). Quando nessa configuração, o Edge avalia a Zona de uma URL ao decidir se ela deve ou não ser aberta no modo IE. Além dessa decisão inicial, as guias do modo IE estão, na verdade, executando o Internet Explorer e, como consequência, avaliam as configurações de Zonas para cada decisão de política, assim como o próprio Internet Explorer fazia.

## <a name="summary"></a>Resumo

Na maioria dos casos, as configurações do Microsoft Edge podem ser deixadas em seus padrões. Os administradores que desejam alterar os padrões de todos os sites ou sites específicos podem usar as Políticas de Grupo apropriadas para especificar listas de sites ou comportamentos padrão. Em alguns casos (versão de credencial, download de arquivo e modo IE), os administradores continuarão a controlar o comportamento, definindo as configurações das Zonas de Segurança do Windows.
