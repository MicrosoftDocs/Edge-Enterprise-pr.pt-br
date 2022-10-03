---
title: Notas de versão do Microsoft Edge para Stable Channel
ms.author: leahtu
author: dan-wesley
manager: srugh
ms.date: 10/03/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Notas de versão do Microsoft Edge para Stable Channel
ms.openlocfilehash: 56abe43ff1a4b7a7365f3492e8be7d1d038e4ced
ms.sourcegitcommit: 51b4070bcff302e1b8809e41b810c3e027e9c146
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/03/2022
ms.locfileid: "12763189"
---
# Notas de versão do Microsoft Edge Stable Channel

Essas notas de versão fornecem informações dos novos recursos e atualizações não relacionados à segurança que estão inclusos Microsoft Edge Stable Channel.

- Todas as atualizações de segurança estão listadas nas [Notas de versão das Atualizações de Segurança do Microsoft Edge](./microsoft-edge-relnotes-security.md).
- As notas de versão arquivadas do Canal Estável do Microsoft Edge estão localizadas nas [Notas de versão arquivadas do Canal Estável do Microsoft Edge](./microsoft-edge-relnote-archive-stable-channel.md).

 Para entender os canais do Microsoft Edge, confira a [Visão geral dos canais do Microsoft Edge](./microsoft-edge-channels.md).

> [!NOTE]
> Para o Canal Estável, as atualizações serão implantadas progressivamente por um ou mais dias. Para saber mais, consulte [Distribuições progressivas para atualizações do Microsoft Edge](./microsoft-edge-update-progressive-rollout.md).
>
> A Plataforma da Web do Microsoft Edge evolui constantemente para melhorar a experiência, segurança e privacidade do usuário. Para saber mais, confira [Compatibilidade de sites: alterações que afetam o Microsoft Edge](/microsoft-edge/web-platform/site-impacting-changes).

## Versão 106.0.1370.34: 3 de outubro de 2022

As atualizações de segurança do canal Estável estão listadas [aqui](/deployedge/microsoft-edge-relnotes-security#october-3-2022).

### Atualizações de recursos

- **Defesa da Web mais confiável.** Navegue pela Web com proteção mais confiável graças à biblioteca [Microsoft Defender SmartScreen](/deployedge/microsoft-edge-security-smartscreen) para Microsoft Edge no Windows, que foi introduzida no Microsoft Edge versão 103. A [política NewSmartScreenLibraryEnabled](/deployedge/microsoft-edge-policies#newsmartscreenlibraryenabled) foi preterida no Microsoft Edge versão 106 e ficará obsoleta no Microsoft Edge versão 107.

- **Aumento dos resultados de trabalho na barra de endereços do Microsoft Edge.** Aumentamos o número máximo de resultados de trabalho exibidos na barra de endereços de 2 para 4, o que oferece maior visibilidade do conteúdo de trabalho disponível à medida que você pesquisa. Esse recurso requer [a política AddressBarMicrosoftSearchInBingProviderEnabled](/deployedge/microsoft-edge-policies#addressbarmicrosoftsearchinbingproviderenabled) habilitada para funcionar.

### Atualizações de política

#### Novas políticas

- [EfficiencyModeEnabled](/DeployEdge/microsoft-edge-policies#efficiencymodeenabled) – modo de eficiência habilitado
- [EfficiencyModeOnPowerEnabled](/DeployEdge/microsoft-edge-policies#efficiencymodeonpowerenabled) – Habilitar o modo de eficiência quando o dispositivo estiver conectado a uma fonte de energia
- [InternetExplorerIntegrationAlwaysUseOSCapture](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationalwaysuseoscapture) – sempre use o mecanismo de captura do sistema operacional para evitar problemas com a captura de guias do modo Internet Explorer

#### Políticas preteridas

- [NewSmartScreenLibraryEnabled](/DeployEdge/microsoft-edge-policies#newsmartscreenlibraryenabled) – Habilitar nova biblioteca SmartScreen
- [ShadowStackCrashRollbackBehavior](/DeployEdge/microsoft-edge-policies#shadowstackcrashrollbackbehavior) – Configurar o comportamento de reversão de falha do ShadowStack

#### Políticas obsoletas

- [OutlookHubMenuEnabled](/DeployEdge/microsoft-edge-policies#outlookhubmenuenabled): permite que os usuários acessem o menu do Outlook
- [EdgeDiscoverEnabled](/DeployEdge/microsoft-edge-policies#edgediscoverenabled) - Recurso de descoberta no Microsoft Edge

## Versão 105.0.1343.53: 26 de setembro de 2022

Vários bugs e problemas de desempenho corrigidos.

## Versão 105.0.1343.50: 22 de setembro de 2022

Vários bugs e problemas de desempenho corrigidos.

## Versão 105.0.1343.42: 15 de setembro de 2022

As atualizações de segurança do canal Estável estão listadas [aqui](/deployedge/microsoft-edge-relnotes-security#september-15-2022).

## Versão 104.0.1293.91: 15 de setembro de 2022

Correção de vários bugs e problemas de desempenho para a versão Estável Estendida.

## Versão 105.0.1343.33: 8 de setembro de 2022

Vários bugs e problemas de desempenho corrigidos.

## Versão 104.0.1293.81: 2 de setembro de 2022

> [!IMPORTANT]
> Esta atualização para o Estável Estendido contém uma correção para [CVE-2022-3075](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2022-3075), que foi relatada pela equipe do Chromium como tendo uma exploração em execução. Para obter mais informações, consulte o [Guia de atualização de segurança](https://msrc.microsoft.com/update-guide).

As atualizações de segurança do canal estável estão listadas [aqui](/deployedge/microsoft-edge-relnotes-security#september-2-2022)

## Versão 105.0.1343.27: 2 de setembro de 2022

> [!IMPORTANT]
> Essa atualização contém uma correção para [o CVE-2022-3075](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2022-3075), que foi relatada pela equipe Chromium como tendo uma exploração em execução. Para obter mais informações, confira o [Guia de Atualização de Segurança](https://msrc.microsoft.com/update-guide).

As atualizações de segurança do canal estável estão listadas [aqui](/deployedge/microsoft-edge-relnotes-security#september-2-2022).

## Versão 105.0.1343.25: 1º de setembro de 2022

As atualizações de segurança do canal estável estão listadas [aqui](/deployedge/microsoft-edge-relnotes-security#september-1-2022).

### Atualizações de recursos

- **Aprimoramentos de modo de segurança aprimorados.** O modo de segurança aprimorado agora dá suporte ao WebAssembly para Windows x64. O suporte adicional entre plataformas é esperado no futuro. Para obter mais informações, confira [Navegar com mais segurança com o Microsoft Edge](/deployedge/microsoft-edge-security-browse-safer).

- **Melhoria na experiência de Gerenciamento de Lista de Sites na Nuvem para o modo IE.**

  - Você pode restaurar para uma das três últimas versões publicadas da sua lista de sites no Administração Microsoft 365 Center. Para obter mais informações, [consulte Restaurar uma versão anterior de uma lista de sites](/deployedge/edge-ie-mode-cloud-site-list-mgmt#restore-a-previous-version-of-a-site-list).
  - Você pode identificar lacunas em sua lista de sites corporativos configurando relatórios de comentários do site com as políticas [InternetExplorerIntegrationCloudUserSitesReporting](/deployedge/microsoft-edge-policies#internetexplorerintegrationcloudusersitesreporting) e [InternetExplorerIntegrationCloudNeutralSitesReporting](/deployedge/microsoft-edge-policies#internetexplorerintegrationcloudneutralsitesreporting). Você pode exibir URLs de lista de sites locais de usuários e URLs de site neutro potencialmente configuradas incorretamente na experiência de listas de sites do Microsoft Edge na Administração Microsoft 365 Center. Para saber mais, confira [Exibir comentários do site no Administração Microsoft 365 Center](/deployedge/edge-ie-mode-cloud-site-list-mgmt#view-site-feedback-on-the-microsoft-365-admin-center-1).
  - Você pode configurar o compartilhamento de cookie de sessão entre o Microsoft Edge e o Internet Explorer para o modo IE em sua lista de sites na Administração Microsoft 365 Central. Para saber mais, confira o [compartilhamento de cookies entre o Microsoft Edge e o Internet Explorer](/deployedge/edge-ie-mode-add-guidance-cookieshare).

- **Melhorias na experiência de Gerenciamento de Lista de Sites na Nuvem para o modo IE agora estão disponíveis no GCC.** Os clientes da GCC agora podem utilizar a experiência completa de lista de sites do Microsoft Edge no Administração Microsoft 365 Center.

### Atualizações de política

#### Novas políticas

- [ExemptFileTypeDownloadWarnings](/DeployEdge/microsoft-edge-policies#exemptfiletypedownloadwarnings) – desabilitar o download de avisos baseados em extensão de tipo de arquivo para tipos de arquivo especificados em domínios
- [InternetExplorerIntegrationAlwaysWaitForUnload](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationalwayswaitforunload) – Aguarde até que as guias do modo Internet Explorer descarreguem completamente antes de encerrar a sessão do navegador
- [MicrosoftEditorProofingEnabled](/DeployEdge/microsoft-edge-policies#microsofteditorproofingenabled) - Verificação ortográfica fornecida pelo Editor Microsoft
- [MicrosoftEditorSynonymsEnabled](/DeployEdge/microsoft-edge-policies#microsofteditorsynonymsenabled) - Sinônimos são fornecidos ao usar Editor Microsoft verificador ortográfico
- [PrintPdfAsImageDefault](/DeployEdge/microsoft-edge-policies#printpdfasimagedefault) – Imprimir PDF como Padrão de Imagem
- [UnthrottledNestedTimeoutEnabled](/DeployEdge/microsoft-edge-policies#unthrottlednestedtimeoutenabled) - JavaScript setTimeout não será fixado até que um limite de aninhamento mais alto seja definido

#### Políticas preteridas

- [ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](/DeployEdge/microsoft-edge-policies#exemptdomainfiletypepairsfromfiletypedownloadwarnings): Desabilita o download de avisos baseados em extensão do tipo de arquivo para tipos de arquivo especificados em domínios.

#### Alterações de política adicionais

- [GuidedSwitchEnabled](/DeployEdge/microsoft-edge-policies#guidedswitchenabled) – Adicionar suporte à plataforma Linux

## Versão 104.0.1293.78: 1º de setembro de 2022

Correção de vários bugs e problemas de desempenho para a versão Estável Estendida.

## Versão 104.0.1293.70: 25 de agosto de 2022

Vários bugs e problemas de desempenho corrigidos.

## Versão 104.0.1293.63 : 19 de agosto

> [!IMPORTANT]
> Essa atualização contém uma correção para [CVE-2022-2856](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2022-2856), que foi relatada pela equipe Chromium como tendo uma exploração em execução. Para obter mais informações, confira o [Guia de Atualização de Segurança](https://msrc.microsoft.com/update-guide).

As atualizações de segurança do canal Estável estão listadas [aqui](/deployedge/microsoft-edge-relnotes-security#august-19-2022).

### Atualizações de recursos

- **Pesquise na barra lateral do Microsoft Edge.** Acesse facilmente uma pesquisa de barra lateral atualizada por meio da barra lateral do Microsoft Edge, incluindo acesso fácil à Pesquisa da Microsoft no Bing para organizações. Observação: essa é uma distribuição de recursos controlada. Se você não vir esse recurso, verifique novamente à medida que continuarmos nossa distribuição.

- **Jogos para a barra lateral do Microsoft Edge.** Jogue jogos casuais populares gratuitamente. Os administradores podem controlar a disponibilidade do menu Jogos na barra lateral do Microsoft Edge. Observação: essa é uma distribuição de recursos controlada. Se você não vir esse recurso, verifique novamente à medida que continuarmos nossa distribuição.

- **Descubra na barra lateral do Microsoft Edge.** Descubra o conteúdo relevante para a página que você está navegando, incluindo resumos, informações de origem e muito mais. Observação: essa é uma distribuição de recursos controlada. Se você não vir esse recurso, verifique novamente à medida que continuarmos nossa distribuição.

- **Obtenha suas ferramentas favoritas na barra lateral do Microsoft Edge.** Acesse facilmente as ferramentas usadas com facilidade durante a navegação na Web, incluindo Calculadora, Teste de velocidade da Internet e Conversor de Unidade. Observação: essa é uma distribuição de recursos controlada. Se você não vir esse recurso, verifique novamente à medida que continuarmos nossa distribuição.

- **Outlook na barra lateral do Microsoft Edge.** Acesse rapidamente e facilmente o Email e o Calendário do Outlook. Observação: essa é uma distribuição de recursos controlada. Se você não vir esse recurso, verifique novamente à medida que continuarmos nossa distribuição.

- **Office na barra lateral do Microsoft Edge.** Acesse documentos e aplicativos do Microsoft Office de maneira rápida e fácil. Os administradores podem controlar o menu do Microsoft Office na barra lateral do Microsoft Edge. Observação: essa é uma distribuição de recursos controlada. Se você não vir esse recurso, verifique novamente à medida que continuarmos nossa distribuição.

## Versão 104.0.1293.54: 11 de agosto

Corrigidos vários bugs e problemas de desempenho para a versão Estável e Estável Estendida.

## Versão 104.0.1293.47: 5 de agosto

As atualizações de segurança do canal estável estão listadas [aqui](/deployedge/microsoft-edge-relnotes-security#august-5-2022).

### Atualizações de recursos

- **Aprimorar sua segurança na Web**. As melhorias para **Aprimorar sua segurança na web** em *edge://settings/privacy* agora incluem **Básico** como nova opção padrão. Com essa opção, o Microsoft Edge aplicará uma proteção de segurança adicional aos sites menos visitados. Este recurso preserva a experiência do usuário nos sites mais populares na Web. Para obter mais informações, confira [Navegar com mais segurança com o Microsoft Edge](/deployedge/microsoft-edge-security-browse-safer).

- **Importar os dados do Chrome sem o Chrome durante a Primeira Experiência de Execução.** Esse recurso permite que um usuário traga seus dados do Chrome fazendo logon na sua conta do Google durante a Experiência de Primeira Execução do Microsoft Edge. Esse recurso pode ser desativado desabilitando a Experiência de Primeira Execução com a política [HideFirstRunExperience](/deployedge/microsoft-edge-policies#hidefirstrunexperience) ou definindo [AutoImportAtFirstRun](/deployedge/microsoft-edge-policies#autoimportatfirstrun) como 'DisabledAutoImport'.

### Atualizações de política

#### Novas políticas

- [AllowedDomainsForApps](/DeployEdge/microsoft-edge-policies#alloweddomainsforapps) - Define os domínios com permissão para acessar o Google Workspace
- [AskBeforeCloseEnabled](/DeployEdge/microsoft-edge-policies#askbeforecloseenabled) - Obtém a confirmação do usuário antes de fechar uma janela do navegador com várias guias
- [BrowserCodeIntegritySetting](/DeployEdge/microsoft-edge-policies#browsercodeintegritysetting) - Define a configuração de proteção da integridade do código do processo do navegador
- [DoubleClickCloseTabEnabled](/DeployEdge/microsoft-edge-policies#doubleclickclosetabenabled) - Recurso de Clique Duplo no Microsoft Edge habilitado (disponível apenas na China)
- [ImportOnEachLaunch](/DeployEdge/microsoft-edge-policies#importoneachlaunch) - Permite a importação de dados de outros navegadores em cada inicialização do Microsoft Edge
- [QuickSearchShowMiniMenu](/DeployEdge/microsoft-edge-policies#quicksearchshowminimenu) - Habilita o mini menu do Microsoft Edge
- [PasswordManagerRestrictLengthEnabled](/DeployEdge/microsoft-edge-policies#passwordmanagerrestrictlengthenabled) - Restringe o comprimento das senhas que podem ser salvas no Gerenciador de senhas
- [PDFXFAEnabled](/DeployEdge/microsoft-edge-policies#pdfxfaenabled) - Suporte a XFA em leitor de PDF nativo habilitado
- [TextPredictionEnabled](/DeployEdge/microsoft-edge-policies#textpredictionenabled) - Previsão de texto habilitada por padrão

#### Política obsoleta

- [U2fSecurityKeyApiEnabled](/DeployEdge/microsoft-edge-policies#u2fsecuritykeyapienabled) - Permitir o uso da API de chave de segurança U2F preterida

## Versão 103.0.1264.77: 28 de julho

Vários bugs e problemas de desempenho corrigidos.

## Versão 102.0.1245.62: 27 de julho

Correção de vários bugs e problemas de desempenho para a versão Estável Estendida.

## Versão 103.0.1264.71: 22 de julho

As atualizações de segurança do canal estável estão listadas [aqui](/deployedge/microsoft-edge-relnotes-security#july-22-2022).

## Versão 103.0.1264.62: 14 de julho

Vários bugs e problemas de desempenho corrigidos. Recomendamos que os usuários instalem essa atualização para resolver o problema a seguir.

### Problema conhecido

Microsoft Edge no Windows 10 versão 1809 de 32 bits (x86) pode ter problemas de inicialização com as próximas Atualizações do Windows que não são de segurança de julho (KB5015880 - 17763.3224). Isso foi corrigido com a versão mais recente do canal estável do Microsoft Edge, versão 103.0.1264.62. Os usuários corporativos que encontram esse problema na versão 102 do canal Estável Estendido Microsoft Edge precisam desabilitar a política [NewSmartScreenLibraryEnabled](/deployedge/microsoft-edge-policies#newsmartscreenlibraryenabled).

## Versão 103.0.1264.49: 6 de julho

> [!Important]
> Esta atualização contém uma correção para [CVE-2022-2294](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2022-2294), que foi relatada pela equipe do Chromium como tendo um exploit em execução. Para obter mais informações, consulte o [Guia de atualização de segurança](https://msrc.microsoft.com/update-guide).

As atualizações de segurança do canal Estável estão listadas [aqui](/deployedge/microsoft-edge-relnotes-security#july-6-2022).

## Versão 102.0.1245.56: 6 de julho

Correção de vários bugs e problemas de desempenho para a versão Estável Estendida.

## Versão 103.0.1264.44: 30 de junho

As atualizações de segurança do canal Estável estão listadas [aqui](/deployedge/microsoft-edge-relnotes-security#june-30-2022).

## Versão 102.0.1245.50: 23 de junho

Correção de vários bugs e problemas de desempenho para a versão Estável Estendida.

<!--- from Version 103.0.1264.37: June 23 to Version 102.0.1245.33: June 3 ---->
<!--- from Version 103.0.1264.37: June 23 to Version 102.0.1245.33: June 3 ---->
<!--- from Version 102.0.1245.30: May 31 to Version 100.0.1185.57: May 2 ---->
<!-- from Version 101.0.1210.32: April 28 to Version 100.0.1185.36: April 7 -->
<!---from Version 100.0.1185.29: April 1  to  Version 99.0.1150.36: March 7 --->
<!--- from Version 99.0.1150.30: March 3 to Version 98.0.1108.50: February 10 --->
<!--- from Version 98.0.1108.43: February 3 to Version 96.0.1054.72: January 6  -->
<!---- From Version 97.0.1072.55: January 6 to Version 96.0.1054.34: November 23 ---->
<!---archive from Version 96.0.1054.29: November 19 to Version 94.0.992.57: October 27 --->
<!-- archive from Version 95.0.1020.30: October 21 to Version 94.0.992.37: September 30 -->
<!-- archive from Version 94.0.992.31: September 24 to Version 93.0.961.44: September 9  -->
<!--- Archive from Version 93.0.961.38: September 2 to Version 92.0.902.62: July 29 --->
<!-- Archive from Version 92.0.902.55: July 22 to Version 91.0.864.37: May 27 -->
<!-- Archive from 89.0.774.45: March 4 to 90.0.818.66: May 20 ->
<!-- Archive from 86.0.622.43: October 15 to beta 88.0.705.81: February 25  ->
<!-- Archive from 86.0.622.38-october-9 to beta 86.0.62.215-september-14  ->
<!-- Archived to version 84.0.522.40: July 16 -->

## Consulte também

- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
