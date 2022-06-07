---
title: Notas da versão do Microsoft Edge para canal beta
ms.author: leahtu
author: dan-wesley
manager: srugh
ms.date: 06/06/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Notas da versão do Microsoft Edge para canal beta
ms.openlocfilehash: 601edcda764e8d14e8d9c2cf973e4ee3fdb20354
ms.sourcegitcommit: ba3b92abf91d52388ba6c2a4feebc4464c7c286e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/07/2022
ms.locfileid: "12577371"
---
# <a name="release-notes-for-microsoft-edge-beta-channel"></a>Notas de versão do canal do Microsoft Edge beta

Estas notas de versão fornecem informações sobre os novos recursos e atualizações não relacionadas à segurança que estão inclusos no canal Beta do Microsoft Edge. As versões arquivadas dessas notas de versão estão disponíveis nas notas [de versão arquivadas do Canal Beta do Microsoft Edge](./microsoft-edge-relnote-archive-beta-channel.md).

> [!NOTE]
> A Plataforma da Web do Microsoft Edge evolui constantemente para melhorar a experiência, segurança e privacidade do usuário. Para saber mais, confira [Compatibilidade de sites: alterações que afetam o Microsoft Edge](/microsoft-edge/web-platform/site-impacting-changes).

## <a name="version-1030126417-june-6"></a>Versão 103.0.1264.17: 6 de junho

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-1030126413-june-2"></a>Versão 103.0.1264.13: 2 de junho

## <a name="feature-updates"></a>Atualizações de recursos

- **Capacidade de controlar a alternância automática de perfil.** A [política GuidedSwitchEnabled](/DeployEdge/microsoft-edge-policies#guidedswitchenabled) permite que o Microsoft Edge solicite que o usuário alterne para o perfil apropriado quando o Microsoft Edge detectar que um link é um link pessoal ou de trabalho.

- **Alternador de Certificado do Cliente.** Esse recurso oferecerá uma maneira para os usuários limparem o certificado lembrado e ressurgir o seletor de certificado ao visitar um site que exige autenticação de certificado http. A alternância pode ser feita sem sair manualmente do Microsoft Edge.

- **Segurança aprimorada para navegação na Web.** Os usuários podem navegar na Web com segurança com confiabilidade e estabilidade aprimoradas graças ao cliente de defesa da Web reescrito (anteriormente conhecido como Microsoft Defender SmartScreen) no Microsoft Edge para Windows.

### <a name="policy-updates"></a>Atualizações de política

#### <a name="new-policies"></a>Novas políticas

- [GuidedSwitchEnabled](/DeployEdge/microsoft-edge-policies#guidedswitchenabled) – Comutador Guiado Habilitado
- [InternetExplorerZoomDisplay](/DeployEdge/microsoft-edge-policies#internetexplorerzoomdisplay) – Exibir zoom nas guias do Modo IE com Escala de DPI incluída como está no Internet Explorer
- [LiveCaptionsAllowed](/DeployEdge/microsoft-edge-policies#livecaptionsallowed) – Legendas ao vivo permitidas
- [OriginAgentClusterDefaultEnabled](/DeployEdge/microsoft-edge-policies#originagentclusterdefaultenabled) – Clustering de agente com chave de origem habilitado por padrão

## <a name="version-1020124525-may-26"></a>Versão 102.0.1245.25: 26 de maio

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-1020124522-may-24"></a>Versão 102.0.1245.22: 24 de maio

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-1020124518-may-20"></a>Versão 102.0.1245.18: 20 de maio

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-1020124514-may-16"></a>Versão 102.0.1245.14: 16 de maio

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-1020124512-may-13"></a>Versão 102.0.1245.12: 13 de maio

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-102012457-may-10"></a>Versão 102.0.1245.7: 10 de maio

### <a name="policy-updates"></a>Atualizações de política

#### <a name="new-policies"></a>Novas políticas

- [AllHttpAuthSchemesAllowedForOrigins](/DeployEdge/microsoft-edge-policies#allhttpauthschemesallowedfororigins): lista de origens que permitem toda a autenticação HTTP
- [OutlookHubMenuEnabled](/DeployEdge/microsoft-edge-policies#outlookhubmenuenabled): permite que os usuários acessem o menu do Outlook
- [NetworkServiceSandboxEnabled](/DeployEdge/microsoft-edge-policies#networkservicesandboxenabled): habilitar a área restrita do serviço de rede
- [UserAgentClientHintsGREASEUpdateEnabled](/DeployEdge/microsoft-edge-policies#useragentclienthintsgreaseupdateenabled): controla o recurso Atualização GREASE das Dicas do Cliente do Agente do Usuário

## <a name="version-1010121039-may-5"></a>Versão 101.0.1210.39: 5 de maio

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-1010121031-april-27"></a>Versão 101.0.1210.31: 27 de abril

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-1010121026-april-22"></a>Versão 101.0.1210.26: 22 de abril

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-1010121019-april-18"></a>Versão 101.0.1210.19: 18 de abril

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-1010121014-april-12"></a>Versão 101.0.1210.14: 12 de abril

Vários bugs e problemas de desempenho corrigidos.

### <a name="feature-updates"></a>Atualizações de recursos

- **Melhorias no Gerenciador de Lista de Sites Corporativos.** Agora você pode configurar cookies compartilhados entre o Microsoft Edge e o Internet Explorer em sua lista de sites corporativos. Você pode acessar o [Gerenciador de Lista de Sites Corporativos](/deployedge/edge-ie-mode-site-list-manager) em *edge://compat/SiteListManager*.

<!--- from Version 101.0.1210.10: April 8 to Version 100.0.1185.12: March 18 --->
<!--- from Version 100.0.1185.10: March 17 to Version 99.0.1150.16: February 14 --->
<!--- From Version 99.0.1150.11: February 9 to Version 98.0.1108.27: January 19 --->
<!-- archive from Version 98.0.1108.23: January 14 to Version 97.0.1072.28: December 8 -->
<!--- Version 97.0.1072.21: December 1 to Version 96.0.1054.13: November 5  --->
<!--- archive from Version 96.0.1054.8: November 1 to Version 95.0.1020.14: October 5  --->
<!-- archive from version 95.0.1020.9: September 28 to version 94.0.992.14: September 7 -->
<!-- archive from Version 94.0.992.9: September 2 to Version 92.0.902.40: July 6 -->
<!--Archive from Version 92.0.902.22: June 21 to Version 89.0.774.23: February 8  -->
<!-- Archive from Version 87.0.664.18: October 26 to to version 89.0.774.18: February 3 --->
<!-- Archive from Version 87.0.664.12: October 20 to version 86.0.622.15: September 14 -->
<!--- Archived to version 86.0.622.11: September 9 ---->
<!--- Archived to version 85.0.564.18: July 28 ---->

## <a name="see-also"></a>Ver também

- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)

