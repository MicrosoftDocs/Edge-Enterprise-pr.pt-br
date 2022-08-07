---
title: Notas da versão do Microsoft Edge para canal beta
ms.author: leahtu
author: dan-wesley
manager: srugh
ms.date: 08/04/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Notas da versão do Microsoft Edge para canal beta
ms.openlocfilehash: 80c2115fa1317e8f0d55fb6ac702325c9d61df8d
ms.sourcegitcommit: c4b3a38fdb78cf663f82d35148716d88f3e7551d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2022
ms.locfileid: "12691859"
---
# <a name="release-notes-for-microsoft-edge-beta-channel"></a>Notas de versão do canal do Microsoft Edge beta

Estas notas de versão fornecem informações sobre os novos recursos e atualizações não relacionadas à segurança que estão inclusos no canal Beta do Microsoft Edge. As versões arquivadas dessas notas de versão estão disponíveis nas notas [de versão arquivadas para Microsoft Edge Beta Channel](./microsoft-edge-relnote-archive-beta-channel.md).

> [!NOTE]
> A Plataforma da Web do Microsoft Edge evolui constantemente para melhorar a experiência, segurança e privacidade do usuário. Para saber mais, confira [Compatibilidade de sites: alterações que afetam o Microsoft Edge](/microsoft-edge/web-platform/site-impacting-changes).

## <a name="version-1040129344-august-3"></a>Versão 104.0.1293.44: 3 de agosto

Vários bugs e problemas de desempenho corrigidos.

### <a name="feature-updates"></a>Atualizações de recursos

- **Aprimora sua segurança na Web**. Melhorias **para aprimorar a segurança na Web** *edge://settings/privacy* agora incluem **Básico** como a nova opção padrão.  Com essa opção, o Microsoft Edge aplicará proteção de segurança adicional aos sites menos visitados. Isso preserva a experiência do usuário para os sites mais populares na Web. Para obter mais informações, [consulte Procurar com mais segurança com o Microsoft Edge](/deployedge/microsoft-edge-security-browse-safer).

## <a name="version-1040129341-august-1"></a>Versão 104.0.1293.41: 1º de agosto

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-1040129335-july-25"></a>Versão 104.0.1293.35: 25 de julho

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-1040129325-july-18"></a>Versão 104.0.1293.25: 18 de julho

Vários bugs e problemas de desempenho corrigidos.

### <a name="feature-updates"></a>Atualizações de recursos

- **Importe dados do Chrome sem o Chrome durante a Experiência de Primeira Execução.** Esse recurso permite que um usuário traga seus dados do Chrome fazendo logon em sua conta do Google durante a Experiência de Primeira Execução do Microsoft Edge. Esse recurso pode ser desativado desabilitando a Experiência de Primeira Execução com a política [HideFirstRunExperience](/deployedge/microsoft-edge-policies#hidefirstrunexperience) ou definindo [AutoImportAtFirstRun](/deployedge/microsoft-edge-policies#autoimportatfirstrun) como 'DisabledAutoImport'.

## <a name="version-1040129321-july-14"></a>Versão 104.0.1293.21: 14 de julho

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-1040129314-july-7"></a>Versão 104.0.1293.14: 7 de julho

### <a name="policy-updates"></a>Atualizações de política

#### <a name="new-policies"></a>Novas políticas

- [AllowedDomainsForApps](/DeployEdge/microsoft-edge-policies#alloweddomainsforapps) – Definir domínios permitidos para acessar o Espaço de Trabalho do Google
- [AskBeforeCloseEnabled](/DeployEdge/microsoft-edge-policies#askbeforecloseenabled) – Obter confirmação do usuário antes de fechar uma janela do navegador com várias guias
- [BrowserCodeIntegritySetting](/DeployEdge/microsoft-edge-policies#browsercodeintegritysetting) – Definir a configuração de proteção de integridade do código do processo do navegador
- [DoubleClickCloseTabEnabled](/DeployEdge/microsoft-edge-policies#doubleclickclosetabenabled) – recurso de clique duplo no Microsoft Edge habilitado (disponível somente na China)
- [ImportOnEachLaunch](/DeployEdge/microsoft-edge-policies#importoneachlaunch) – Permitir a importação de dados de outros navegadores em cada inicialização do Microsoft Edge
- [QuickSearchShowMiniMenu](/DeployEdge/microsoft-edge-policies#quicksearchshowminimenu) – habilita o mini menu do Microsoft Edge
- [PasswordManagerRestrictLengthEnabled](/DeployEdge/microsoft-edge-policies#passwordmanagerrestrictlengthenabled) - Restringir o comprimento das senhas que podem ser salvas no Gerenciador de Senhas
- [PDFXFAEnabled](/DeployEdge/microsoft-edge-policies#pdfxfaenabled) – Suporte a XFA no leitor de PDF nativo habilitado
- [TextPredictionEnabled](/DeployEdge/microsoft-edge-policies#textpredictionenabled) – Previsão de texto habilitada por padrão

#### <a name="obsoleted-policy"></a>Política obsoleta

- [U2fSecurityKeyApiEnabled](/DeployEdge/microsoft-edge-policies#u2fsecuritykeyapienabled) - Permitir o uso da API de chave de segurança U2F preterida

## <a name="version-1030126445-july-1"></a>Versão 103.0.1264.45: 1º de julho

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-1030126437-june-22"></a>Versão 103.0.1264.37: 22 de junho

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-1030126432-june-20"></a>Versão 103.0.1264.32: 20 de junho

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-1030126421-june-10"></a>Versão 103.0.1264.21: 10 de junho

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-1030126417-june-6"></a>Versão 103.0.1264.17: 6 de junho

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-1030126413-june-2"></a>Versão 103.0.1264.13: 2 de junho

### <a name="feature-updates"></a>Atualizações de recursos

- **Capacidade de controlar a alternância automática de perfil.** A política [GuidedSwitchEnabled](/DeployEdge/microsoft-edge-policies#guidedswitchenabled) permite que a Microsoft Edge solicite ao usuário que mude para o perfil apropriado quando o Microsoft Edge detectar que um link é um link pessoal ou de trabalho.

- **Alternador de Certificado do Cliente.** Esse recurso oferecerá uma maneira para os usuários limparem o certificado lembrado e ressurgir o seletor de certificado ao visitar um site que exige autenticação de certificado http. A alternância pode ser feita sem sair manualmente do Microsoft Edge.

- **Defesa da Web mais confiável.** Navegue pela Web com proteção mais confiável graças à biblioteca reescrita do[Microsoft Defender SmartScreen](/deployedge/microsoft-edge-security-smartscreen) para Microsoft Edge no Windows. A política [NewSmartScreenLibraryEnabled](microsoft-edge-policies.md#newsmartscreenlibraryenabled) permitirá que os clientes empresariais continuem usando a versão herdada da biblioteca até que ela seja preterida no Microsoft Edge versão 105.

### <a name="policy-updates"></a>Atualizações de política

#### <a name="new-policies"></a>Novas políticas

- [GuidedSwitchEnabled](/DeployEdge/microsoft-edge-policies#guidedswitchenabled) – Comutador Guiado Habilitado
- [InternetExplorerZoomDisplay](/DeployEdge/microsoft-edge-policies#internetexplorerzoomdisplay) - Exibir zoom nas guias do Modo IE com Escala de DPI incluída como está no Internet Explorer
- [LiveCaptionsAllowed](/DeployEdge/microsoft-edge-policies#livecaptionsallowed) – Legendas ao vivo permitidas
- [OriginAgentClusterDefaultEnabled](/DeployEdge/microsoft-edge-policies#originagentclusterdefaultenabled) - Agrupamento de agentes com chave de origem habilitada por padrão

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

<!--- from Version 102.0.1245.7: May 10 to Version 101.0.1210.14: April 12 ---->
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

