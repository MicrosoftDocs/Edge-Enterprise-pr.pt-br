---
title: Notas da versão do Microsoft Edge para canal beta
ms.author: leahtu
author: dan-wesley
manager: srugh
ms.date: 08/26/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Notas da versão do Microsoft Edge para canal beta
ms.openlocfilehash: f5ea6224dc1613be6513d125873c92002dd0712f
ms.sourcegitcommit: f8a5f3bbc786f3666a2974a4f7be0e6145efb8da
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2022
ms.locfileid: "12735924"
---
# <a name="release-notes-for-microsoft-edge-beta-channel"></a>Notas de versão do canal do Microsoft Edge beta

Estas notas de versão fornecem informações sobre os novos recursos e atualizações não relacionadas à segurança que estão inclusos no canal Beta do Microsoft Edge. As versões arquivadas dessas notas de versão estão disponíveis nas notas [de versão arquivadas para Microsoft Edge Beta Channel](./microsoft-edge-relnote-archive-beta-channel.md).

> [!NOTE]
> A Plataforma da Web do Microsoft Edge evolui constantemente para melhorar a experiência, segurança e privacidade do usuário. Para saber mais, confira [Compatibilidade de sites: alterações que afetam o Microsoft Edge](/microsoft-edge/web-platform/site-impacting-changes).

## <a name="version-1050134317-august-26-2022"></a>Versão 105.0.1343.17: 26 de agosto de 2022

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-1050134310-august-19"></a>Versão 105.0.1343.10: 19 de agosto

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-105013437-august-16"></a>Versão 105.0.1343.7: 16 de agosto

Vários bugs e problemas de desempenho corrigidos.

### <a name="feature-updates"></a>Atualizações de recursos

- **Melhoria na experiência de Gerenciamento de Lista de Sites na Nuvem para o modo IE.** Você pode restaurar para uma das três últimas versões publicadas da sua lista de sites no Administração Microsoft 365 Center. Para obter mais informações, [consulte Restaurar uma versão anterior de uma lista de sites](/deployedge/edge-ie-mode-cloud-site-list-mgmt#restore-a-previous-version-of-a-site-list).

- **Melhorias na experiência de Gerenciamento de Lista de Sites na Nuvem para o Modo IE agora estão disponíveis no GCC.** Você pode identificar lacunas em sua lista de sites corporativos configurando relatórios de comentários do site com as políticas [InternetExplorerIntegrationCloudUserSitesReporting](/deployedge/microsoft-edge-policies#internetexplorerintegrationcloudusersitesreporting) e [InternetExplorerIntegrationCloudNeutralSitesReporting](/deployedge/microsoft-edge-policies#internetexplorerintegrationcloudneutralsitesreporting) . Você pode exibir URLs de lista de sites locais de usuários e URLs de site neutro potencialmente configuradas incorretamente na experiência de listas de sites do Microsoft Edge na Administração Microsoft 365 Center. Para obter mais informações, [consulte Exibir comentários do site no Administração Microsoft 365 Center](/deployedge/edge-ie-mode-cloud-site-list-mgmt#view-site-feedback-on-the-microsoft-365-admin-center-1). Além disso, você pode configurar o compartilhamento de cookie de sessão entre o Microsoft Edge e o Internet Explorer para o Modo IE na lista de sites na Administração Microsoft 365 Central. Para obter mais informações, consulte [Compartilhamento de cookies entre o Microsoft Edge e o Internet Explorer](/deployedge/edge-ie-mode-add-guidance-cookieshare).

### <a name="policy-updates"></a>Atualizações de política

#### <a name="new-policies"></a>Novas políticas

- [ExemptFileTypeDownloadWarnings](/DeployEdge/microsoft-edge-policies#exemptfiletypedownloadwarnings) – desabilitar o download de avisos baseados em extensão de tipo de arquivo para tipos de arquivo especificados em domínios
- [InternetExplorerIntegrationAlwaysWaitForUnload](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationalwayswaitforunload) – Aguarde até que as guias do modo Internet Explorer descarreguem completamente antes de encerrar a sessão do navegador
- [MicrosoftEditorProofingEnabled](/DeployEdge/microsoft-edge-policies#microsofteditorproofingenabled) - Verificação ortográfica fornecida pelo Editor Microsoft
- [MicrosoftEditorSynonymsEnabled](/DeployEdge/microsoft-edge-policies#microsofteditorsynonymsenabled) - Sinônimos são fornecidos ao usar Editor Microsoft verificador ortográfico
- [PrintPdfAsImageDefault](/DeployEdge/microsoft-edge-policies#printpdfasimagedefault) – Imprimir PDF como Padrão de Imagem
- [UnthrottledNestedTimeoutEnabled](/DeployEdge/microsoft-edge-policies#unthrottlednestedtimeoutenabled) - JavaScript setTimeout não será fixado até que um limite de aninhamento mais alto seja definido

#### <a name="deprecated-policy"></a>Política preterida

- [ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](/DeployEdge/microsoft-edge-policies#exemptdomainfiletypepairsfromfiletypedownloadwarnings): Desabilita o download de avisos baseados em extensão do tipo de arquivo para tipos de arquivo especificados em domínios.

#### <a name="additional-change"></a>Alteração adicional

- [GuidedSwitchEnabled](/DeployEdge/microsoft-edge-policies#guidedswitchenabled) – Adicionar suporte à plataforma Linux

## <a name="version-1040129344-august-3"></a>Versão 104.0.1293.44: 3 de agosto

Vários bugs e problemas de desempenho corrigidos.

### <a name="feature-updates"></a>Atualizações de recursos

- **Aprimorar sua segurança na Web**. As melhorias para **Aprimorar sua segurança na web** em *edge://settings/privacy* agora incluem **Básico** como nova opção padrão.  Com essa opção, o Microsoft Edge aplicará uma proteção de segurança adicional aos sites menos visitados. Isso preserva a experiência do usuário para os sites mais populares na Web. Para obter mais informações, confira [Navegar com mais segurança com o Microsoft Edge](/deployedge/microsoft-edge-security-browse-safer).

## <a name="version-1040129341-august-1"></a>Versão 104.0.1293.41: 1º de agosto

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-1040129335-july-25"></a>Versão 104.0.1293.35: 25 de julho

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-1040129325-july-18"></a>Versão 104.0.1293.25: 18 de julho

Vários bugs e problemas de desempenho corrigidos.

### <a name="feature-updates"></a>Atualizações de recursos

- **Importar os dados do Chrome sem o Chrome durante a Primeira Experiência de Execução.** Esse recurso permite que um usuário traga seus dados do Chrome fazendo logon na sua conta do Google durante a Experiência de Primeira Execução do Microsoft Edge. Esse recurso pode ser desativado desabilitando a Experiência de Primeira Execução com a política [HideFirstRunExperience](/deployedge/microsoft-edge-policies#hidefirstrunexperience) ou definindo [AutoImportAtFirstRun](/deployedge/microsoft-edge-policies#autoimportatfirstrun) como 'DisabledAutoImport'.

## <a name="version-1040129321-july-14"></a>Versão 104.0.1293.21: 14 de julho

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-1040129314-july-7"></a>Versão 104.0.1293.14: 7 de julho

### <a name="policy-updates"></a>Atualizações de política

#### <a name="new-policies"></a>Novas políticas

- [AllowedDomainsForApps](/DeployEdge/microsoft-edge-policies#alloweddomainsforapps) - Define os domínios com permissão para acessar o Google Workspace
- [AskBeforeCloseEnabled](/DeployEdge/microsoft-edge-policies#askbeforecloseenabled) - Obtém a confirmação do usuário antes de fechar uma janela do navegador com várias guias
- [BrowserCodeIntegritySetting](/DeployEdge/microsoft-edge-policies#browsercodeintegritysetting) - Define a configuração de proteção da integridade do código do processo do navegador
- [DoubleClickCloseTabEnabled](/DeployEdge/microsoft-edge-policies#doubleclickclosetabenabled) - Recurso de Clique Duplo no Microsoft Edge habilitado (disponível apenas na China)
- [ImportOnEachLaunch](/DeployEdge/microsoft-edge-policies#importoneachlaunch) - Permite a importação de dados de outros navegadores em cada inicialização do Microsoft Edge
- [QuickSearchShowMiniMenu](/DeployEdge/microsoft-edge-policies#quicksearchshowminimenu) - Habilita o mini menu do Microsoft Edge
- [PasswordManagerRestrictLengthEnabled](/DeployEdge/microsoft-edge-policies#passwordmanagerrestrictlengthenabled) - Restringe o comprimento das senhas que podem ser salvas no Gerenciador de senhas
- [PDFXFAEnabled](/DeployEdge/microsoft-edge-policies#pdfxfaenabled) - Suporte a XFA em leitor de PDF nativo habilitado
- [TextPredictionEnabled](/DeployEdge/microsoft-edge-policies#textpredictionenabled) - Previsão de texto habilitada por padrão

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

<!--- from Version 103.0.1264.13: June 2 to Version 102.0.1245.12: May 13 ---->
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

