---
title: Configuração por site por política
ms.author: collw
author: dan-wesley
manager: laurawi
ms.date: 01/04/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Configuração por site por política
ms.openlocfilehash: 147f14fdd09f56161bf03ca88b5e6107ba9c88c5
ms.sourcegitcommit: e7f3098d8b7d91cae20b5778a71a87daababc312
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/15/2022
ms.locfileid: "12297859"
---
# <a name="per-site-configuration-by-policy"></a>Configuração por site por política

Este artigo descreve as configurações por site por política e como o navegador lida com as cargas de página de um site.

## <a name="the-browser-as-a-decision-maker"></a>O navegador como um tomadores de decisão

Como parte de cada carga de página, os navegadores tomarão muitas decisões. Algumas, mas não todas, dessas decisões incluem: se uma API específica está disponível, se uma carga de recursos deve ser permitida e se um script pode ser executado.

Na maioria dos casos, as decisões do navegador são governadas pelas seguintes entradas:

- Uma configuração de usuário
- A URL da página para a qual a decisão é tomada

Na plataforma Web do Internet Explorer, cada uma dessas decisões foi chamada de URLAction. Para obter mais informações, consulte [URL Action Flags](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537178%28v%3dvs.85%29). A URLAction, Enterprise Política de Grupo e as configurações do usuário no Painel de Controle da Internet controlavam como o navegador lidaria com cada decisão.  

No Microsoft Edge, a maioria das permissões por site é controlada por configurações e políticas expressas usando uma sintaxe simples com suporte limitado a curinga. Segurança do Windows zonas ainda são usadas para algumas decisões de configuração.

## <a name="windows-security-zones"></a>Segurança do Windows Zonas

Para simplificar a configuração para o usuário ou administrador, a plataforma herdado classificou os sites em uma das cinco zonas de segurança diferentes. Essas Zonas de Segurança são: Máquina Local, Intranet Local, Confiável, Internet e Sites Restritos.

Ao tomar uma decisão de carregamento de página, o navegador mapeia o site para uma Zona e consulta a configuração para a URLAction para que Zona decida o que fazer. Padrões razoáveis como "Atender automaticamente aos desafios de autenticação da minha Intranet" significa que a maioria dos usuários nunca precisa alterar as configurações padrão.

Os usuários podem usar o Painel Controle de internet para atribuir sites específicos a Zonas e configurar os resultados de permissão para cada zona. Em ambientes gerenciados, os administradores podem usar Política de Grupo para atribuir sites específicos a Zonas (por meio da política "Lista de Atribuições de Site a Zona") e especificar as configurações para URLActions por zona. Além da atribuição manual administrativa ou de usuário de sites a Zonas, outras heurísticas podem atribuir [sites à Zona de Intranet Local.](/archive/blogs/ieinternals/the-intranet-zone) Em particular, nomes de host sem ponto (por exemplo, `http://payroll` ) foram atribuídos à Zona da Intranet. Se um script de Configuração de Proxy tivesse sido usado, todos os sites configurados para ignorar o proxy seriam mapeados para a Zona da Intranet.

A Versão Prévia do Microsoft Edge herdou a arquitetura de Zonas de seu predecessor, o Internet Explorer, com algumas alterações simplificadas:

- As cinco Zonas internas do Windows foram reduzidas para três: Internet (Internet), Confiável (Intranet+Confiável) e Computador Local. A Zona de Sites Restritos foi removida.
- Os mapeamentos de Zona para URLAction foram codificados no navegador, ignorando as Políticas de Grupo e as configurações no Painel Controle de Internet.

## <a name="per-site-permissions-in-microsoft-edge"></a>Por permissões de site em Microsoft Edge

Microsoft Edge faz uso limitado de Segurança do Windows Zonas. Em vez disso, a maioria das permissões e recursos que oferecem aos administradores configuração por site por meio de  [política](/deployedge/microsoft-edge-policies) depende de listas de regras no  [Formato de Filtro de URL](/DeployEdge/edge-learnmmore-url-list-filter%20format).

Quando os usuários finais abrirem uma página de configurações como , eles encontrarão uma longa lista de opções de configuração e `edge://settings/content/siteDetails?site=https://example.com` listas para várias permissões. Os usuários raramente usam Configurações página diretamente, em vez disso, eles fazem escolhas durante a navegação e o uso de vários widgets e alternâncias no menu suspenso **informações da**   página. Essa lista aparece quando você seleciona o ícone de bloqueio na barra de endereços. Você também pode usar os vários prompts ou botões na borda direita da barra de endereços. A próxima captura de tela mostra um exemplo de informações da página.

:::image type="content" source="media/per-site-configuration-by-policy/edge-page-info.png" alt-text="Informações de página e configurações para a página atual no navegador.":::

As empresas podem usar a Política de Grupo para configurar listas de sites para políticas individuais que controlam o comportamento do navegador. Para encontrar essas políticas, abra [a](/deployedge/microsoft-edge-policies)documentação Microsoft Edge Política de Grupo e procure "ForUrls" para encontrar as políticas que permitem e bloqueiam o comportamento com base na URL do   site carregado. A maioria das configurações relevantes está listada na seção Política de Grupo [para Conteúdo Configurações](/deployedge/microsoft-edge-policies#content-settings) conteúdo.

Há também muitas políticas (cujos nomes contêm "Padrão") que controlam o comportamento padrão de uma determinada configuração.

Muitas das configurações são ocultas (WebSerial, WebMIDI) e muitas vezes não há motivo para alterar uma configuração do padrão.

## <a name="security-zones-inmicrosoft-edge"></a>Zonas de segurança em Microsoft Edge

Embora Microsoft Edge se baseia principalmente em políticas individuais usando o formato de Filtro de URL, ele continua a usar zonas de segurança Windows' por padrão em alguns casos. Essa abordagem simplifica a implantação em Empresas que se baseiram historicamente na configuração de Zonas.

Os seguintes comportamentos são controlados pela Política de zona:

- Decidir se deve liberar Windows autenticação integrada (Kerberos ou NTLM) automaticamente.
- Decidir como lidar com downloads de arquivos.
- Para o modo Internet Explorer.

## <a name="credential-release"></a>Versão de credencial

Por padrão, Microsoft Edge avalia para decidir se Windows Autenticação Integrada é usada automaticamente ou se o usuário verá  `URLACTION_CREDENTIALS_USE`  um prompt de autenticação manual. Configurar a política de lista de [sites do AuthServerAllowlist](/deployedge/microsoft-edge-policies#authserverallowlist) impedirá que a Política de Zona seja consultada.

## <a name="file-downloads"></a>Downloads de arquivos

As evidências sobre as origens de um download de arquivo (também conhecido como " Marca da[Web](https://textslashplain.com/2016/04/04/downloads-and-the-mark-of-the-web/)" são gravadas para arquivos baixados da Zona da Internet. Outros aplicativos, como o shell Windows, e Microsoft Office podem levar essa evidência de origem em consideração ao decidir como lidar com um arquivo.

Se a política Segurança do Windows Zona estiver configurada para desabilitar a configuração para iniciar aplicativos e baixar arquivos não seguros, o gerenciador de download do Microsoft Edge bloqueará downloads de arquivos de sites nessa Zona. Um usuário verá esta observação: "Não foi possível baixar – Bloqueado".  

## <a name="ie-mode"></a>Modo IE

O modo IE pode ser configurado para [todos os sites da Intranet no modo IE](/deployedge/edge-ie-mode#configure-all-intranet-sites). Ao usar essa configuração, Microsoft Edge avalia a zona de uma URL ao decidir se ela deve ou não ser aberta no modo IE. Além dessa decisão inicial, as guias do modo IE estão realmente executando o Internet Explorer e, como resultado, avaliam as configurações de zonas para cada decisão de política, assim como o Internet Explorer.

## <a name="summary"></a>Resumo

Na maioria dos casos, as configurações do Microsoft Edge podem ser deixadas em seus padrões. Os administradores que desejam alterar os padrões de todos os sites ou sites específicos podem usar as Políticas de Grupo apropriadas para especificar listas de sites ou comportamentos padrão. Em alguns casos, como liberação de credenciais, download de arquivo e modo IE, os administradores continuarão a controlar o comportamento configurando as configurações Segurança do Windows Zonas.

## <a name="frequently-asked-questions"></a>Perguntas frequentes

### <a name="can-the-url-filter-format-match-on-a-sites-ip-address"></a>O formato de filtro de URL pode corresponder ao endereço IP de um site?

Não, o formato não dá suporte à especificação de um intervalo DE IP para listas de autorizações e listas de bloqueios. Ele dá suporte à especificação de literais IP **individuais,** mas essas regras só serão respeitadas se o usuário navegar até o site usando esse literal (por exemplo, `http://127.0.0.1/` ). Se um nome de host for usado (`http://localhost`), a regra de literal de IP não será respeitada, mesmo que o IP resolvido do host corresponda ao IP listado pelo filtro.

### <a name="can-url-filters-matchdotless-host-names"></a>Os filtros de URL podem corresponder a nomes de host sem pontos?

Não. Você deve listar cada nome de host, por `https://payroll` exemplo , , e assim por `https://stock` `https://who` diante.

Se você estava pensando o suficiente para estruturar sua intranet de forma que seus nomes de host sejam do seguinte formulário, implementou uma prática prática prática.

- `https://payroll.contoso-intranet.com`

- `https://timecard.contoso-intranet.com`

- `https://sharepoint.contoso-intranet.com`

No cenário anterior, você pode configurar cada política com uma entrada ***.contoso-intranet.com**e toda a   intranet será optada.

## <a name="see-also"></a>Consulte também

- [Documentação do Microsoft Edge](./index.yml)
- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
