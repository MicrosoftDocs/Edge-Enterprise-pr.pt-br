---
title: Gerenciar extensões do Microsoft Edge na empresa
ms.author: aspoddar
author: AndreaLBarr
manager: balajek
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Gerenciar extensões do Microsoft Edge na empresa
ms.openlocfilehash: 26134a8c352354c0c447518120f3d79332100c80
ms.sourcegitcommit: 8968f3107291935ed9adc84bba348d5f187eadae
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/12/2021
ms.locfileid: "11978619"
---
# <a name="manage-microsoft-edge-extensions-in-the-enterprise"></a>Gerenciar extensões do Microsoft Edge na empresa

Este artigo fornece diretrizes de práticas recomendadas para os administradores que gerenciam as extensões do Microsoft Edge em suas organizações. Use as informações neste artigo para desenvolver uma estratégia de gerenciamento de extensões na organização.

> [!NOTE]
> Este artigo se aplica ao Microsoft Edge versão 77 ou posterior.

## <a name="introduction"></a>Introdução

As organizações querem proteger os dados corporativos e de usuários, além de avaliar as extensões do navegador para garantir que eles sejam seguros e relevantes para a empresa. Os administradores querem:

- Impedir que aplicativos e extensões inválidos sejam instalados.
- Manter as extensões que os usuários precisam para o trabalho.
- Gerenciar o acesso aos dados do usuário e da empresa.  

Este artigo é o primeiro de uma série que ajuda os administradores a gerenciar extensões para proporcionar uma experiência segura e produtiva para seus usuários. Esta série mostra as diferentes opções e ajuda você a escolher o melhor método para gerenciar extensões. A série consiste nos seguintes artigos:

- [Gerenciar extensões do Microsoft Edge na empresa](microsoft-edge-manage-extensions.md). Criar estratégia para gerenciar extensões e configurar modelos administrativos necessários de gerenciamento do navegador.
- [Usar políticas de grupo para gerenciar extensões do Microsoft Edge](microsoft-edge-manage-extensions-policies.md). Opções de uso das políticas de grupo para gerenciar extensões.
- [Criar um repositório para hospedar extensões do Microsoft Edge](microsoft-edge-manage-extensions-webstore.md). Criar e hospedar extensões.
- [Perguntas frequentes sobre extensões do Microsoft Edge](microsoft-edge-manage-extensions-faq.md). Perguntas frequentes.

## <a name="things-to-consider-when-managing-extensions"></a>Coisas a serem consideradas ao gerenciar extensões

Os usuários precisam de acesso a certos aplicativos, sites e extensões para trabalhar, mas ao mesmo tempo, é necessário proteger os usuários e os dados da empresa. Uma estratégia de segurança eficaz envolve fazer as perguntas certas para a empresa e como as extensões podem atender às necessidades dela. Algumas das principais perguntas a serem feitas são:

- Quais regulamentos e medidas de conformidade preciso seguir?
- Algumas extensões solicitam permissões muito amplas, que podem ir contra as políticas de segurança de dados da minha empresa?
- Quantos dados corporativos ou de usuário são armazenados nos dispositivos dos meus usuários?

Ao responder a essas perguntas, use as políticas granulares que Microsoft Edge fornece para:

- Bloquear ou permitir extensões nos computadores dos usuários com base nas políticas de proteção de dados.
- Forçar a instalação de extensões nos dispositivos dos usuários para que eles tenham as ferramentas necessárias para serem produtivos.
- Listas de permissões ou de bloqueios de extensões para permitir a menor quantidade de direitos necessários para que os usuários possam trabalhar.

O modelo tradicional para gerenciar extensões usa a abordagem de listas de permissões e de bloqueios para extensões específicas. No entanto, o Microsoft Edge também permite gerenciar as permissões solicitadas por extensões. Usando esse modelo, você pode decidir quais direitos e permissões deseja permitir que as extensões usem em seus computadores e dispositivos, e assim, implementar uma política global que permita ou bloqueie extensões com base em seus requisitos.  

## <a name="understand-extension-permissions"></a>Entender as permissões de extensão

As extensões podem requerer direitos para fazer alterações em um dispositivo ou em uma página da Web para funcionar corretamente. Esses direitos são chamados de permissões. Os desenvolvedores devem listar quais direitos e acesso as extensões precisam. Há duas categorias principais para permissões e várias extensões precisam de ambas as seguintes permissões:

- As permissões de host requerem a extensão para listar páginas da Web que ela pode exibir ou modificar.
- As permissões do dispositivo são os direitos necessários para uma extensão no dispositivo em que está em execução.

Alguns exemplos dessas permissões são: acesso a uma porta USB, armazenamento ou tela de exibição, e comunicação com programas nativos.  

## <a name="get-ready-to-manage-extensions"></a>Prepare-se para gerenciar extensões

## <a name="before-you-begin"></a>Antes de começar

As opções de extensão pressupõem que você já tem o Microsoft Edge gerenciado para os usuários. Para obter mais informações sobre como configurar modelos administrativos para as políticas do Microsoft Edge, confira:

-   [Definir configurações de política do Microsoft Edge no Windows](/DeployEdge/configure-microsoft-edge)
-   [Configurar para o Windows com o Intune](/mem/intune/configuration/administrative-templates-configure-edge?bc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2fbreadcrumb%2ftoc.json&toc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2ftoc.json)
-   [Configurar para o Windows com Gerenciamento de Dispositivos Móveis](/deployedge/configure-edge-with-mdm)
-   [Configurar para macOS usando um. plist](/deployedge/configure-microsoft-edge-on-mac)
-   [Configurar para macOS com Jamf](/deployedge/configure-microsoft-edge-on-mac-jamf)

As etapas de configuração neste artigo são para o Windows; para a implementação correspondente no MAC/Linux, veja a referência da política do navegador Microsoft Edge.

## <a name="decide-which-extensions-to-allow"></a>Decidir quais extensões permitir

A maioria das organizações deve gerenciar as permissões das extensões e a que websites elas têm acesso. Esse método é mais seguro, fácil de gerenciar e escalonável para grandes organizações.  

- Permissões bloqueadas/permitidas – permite controlar as extensões de acordo com as permissões necessárias.
- Hosts de bloco de runtime – permite controlar quais sites essas extensões podem acessar.

Usar essa abordagem economiza tempo, pois você só precisará defini-las uma vez. E com a política de hosts de runtime, seus sites mais importantes estarão protegidos. Há outras opções, como por exemplo:

-   Forçar a instalação de extensões – permite instalar extensões silenciosamente.
-   Lista de permissões/de bloqueios (se necessário) – decida quais extensões têm permissão para serem instaladas.

Use as etapas a seguir como um guia para decidir quais extensões permitir em sua organização.

1. Crie uma lista de quais extensões os funcionários precisam em seus computadores. Teste as extensões em um ambiente de teste para diagnosticar problemas de compatibilidade com aplicativos internos.
2. Escolha quais sites precisam de mais segurança.

   - Descubra de quais sites ou domínios internos confidenciais você precisa para impedir que extensões façam alterações ou leiam dados.  
   - Impeça o acesso a esses sites bloqueando as chamadas à API quando a extensão for executada. Isso inclui o bloqueio de solicitações da Web, leitura de cookies, injeção de JavaScript, XHR e assim por diante.

3. Determine quais permissões são necessárias para que essas extensões sejam executadas. Identifique quais permissões representam possíveis riscos aos usuários.

   - Audite as extensões que os usuários instalaram e veja quais permissões elas precisam. Você pode examinar o arquivo JSON de manifesto do aplicativo Web no código da extensão. Execute as seguintes etapas para ver quais direitos a extensão precisa:

     - Instale a extensão do site [Complementos do Microsoft Edge](https://microsoftedge.microsoft.com/addons/) ou da [Chrome Web Store](https://chrome.google.com/webstore).
     - Teste a extensão e entenda como ela funciona em sua organização.
     - Examine as permissões que a extensão requer acessando *edge://extensions*. Por exemplo, a extensão do Microsoft Office mostrada na próxima captura de tela solicita as permissões "Ler seu histórico de navegação" e "Exibir notificações". Avalie a utilidade da extensão em relação ao nível de permissões que ela solicita. Depois de aprovar uma extensão para a organização, gerencie-a usando as seguintes ferramentas.
   :::image type="content" source="media/microsoft-edge-manage-extensions/manage-extesions-office-extension.png" alt-text="Extensão do Microsoft Office com permissões.":::

   - Você também pode validar as extensões solicitadas pelos usuários da organização antes de aprová-las na organização. Algumas das permissões que as extensões usam podem ser indefinidas. Para aplicativos comercialmente críticos, contate diretamente o desenvolvedor ou o fornecedor do aplicativo para obter mais informações sobre a extensão, ou verifique o código-fonte. Eles devem detalhar as alterações que a extensão pode fazer em dispositivos e sites.
   - Examine a lista Declarar Permissões, que lista todas as permissões que uma extensão pode usar. Nessa lista, decida quais permissões deseja permitir em sua organização.

4. Crie uma lista mestra com base nos dados coletados. Essa lista incluirá as seguintes informações:

   - **Extensões necessárias**. Essa lista pode ser organizada por departamento, local do escritório ou outras informações relevantes.
   - **Listas de permissões de extensões**. Extensões necessárias com permissões que podem ser bloqueadas, mas terão permissão para serem executadas. Essas extensões são necessárias para os usuários ou são determinadas para não serem um risco por meio de conversas com o fornecedor.
   - **Lista de bloqueios de extensão**. Extensões bloqueadas para serem instaladas. As extensões nessa lista têm as permissões sem permissão para serem executadas. Inclui também os principais sites e domínios a serem mantidos seguros e sem permissão de acesso à extensão. Posteriormente, você pode comparar essa lista de bloqueio com outras que já tenha em vigor. Talvez você descubra que poderá relaxar suas políticas atuais de listas de blocos.

5. Apresente sua lista aos stakeholders e à equipe de TI para comprar.
6. Teste a nova política no laboratório ou com um pequeno piloto na organização.
7. Distribua em fases esses novos conjuntos de políticas aos funcionários. Para obter mais informações, confira [Usar políticas de grupo para gerenciar extensões do Microsoft Edge](microsoft-edge-manage-extensions-policies.md).
8. Examine os comentários de seus usuários.
9. Repita e ajuste o processo mensalmente, trimestralmente ou anualmente.

Com sua linha de base de permissões permitidas aplicadas e os sites corporativos confidenciais protegidos, você poderá fornecer a sua empresa mais segurança e ao mesmo tempo proporcionar uma melhor experiência aos usuários. Os funcionários poderão instalar extensões que antes não conseguiam, mas não poderão executá-las em locais de negócios confidenciais.  

## <a name="see-also"></a>Confira também

- [Usar políticas de grupo para gerenciar extensões do Microsoft Edge](microsoft-edge-manage-extensions-policies.md)
- [Criar um repositório para hospedar extensões do Microsoft Edge](microsoft-edge-manage-extensions-webstore.md)
- [Guia de referência para a política ExtensionSettings](microsoft-edge-manage-extensions-ref-guide.md)
- [Perguntas frequentes sobre extensões do Microsoft Edge](microsoft-edge-manage-extensions-faq.md)
- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)