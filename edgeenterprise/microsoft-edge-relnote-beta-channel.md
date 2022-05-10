---
title: Notas da versão do Microsoft Edge para canal beta
ms.author: leahtu
author: dan-wesley
manager: srugh
ms.date: 05/05/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Notas da versão do Microsoft Edge para canal beta
ms.openlocfilehash: ad834db28ce7cda0a03068cda6618ef21a1a1747
ms.sourcegitcommit: 303788d3d5aa516f6f9b5ecbde5ceb1418e3590d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2022
ms.locfileid: "12508351"
---
# <a name="release-notes-for-microsoft-edge-beta-channel"></a>Notas de versão do canal do Microsoft Edge beta

Estas notas de versão fornecem informações sobre os novos recursos e atualizações não relacionadas à segurança que estão inclusos no canal Beta do Microsoft Edge. As versões arquivadas dessas notas de versão estão disponíveis nas notas [de versão arquivadas para Microsoft Edge Beta Channel](./microsoft-edge-relnote-archive-beta-channel.md).

> [!NOTE]
> A Plataforma da Web do Microsoft Edge evolui constantemente para melhorar a experiência, segurança e privacidade do usuário. Para saber mais, confira [Compatibilidade de sites: alterações que afetam o Microsoft Edge](/microsoft-edge/web-platform/site-impacting-changes).

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

## <a name="version-1010121010-april-8"></a>Versão 101.0.1210.10: 8 de abril

### <a name="feature-updates"></a>Atualizações de recursos

- **Capacidade de definir o perfil padrão.** A [política EdgeDefaultProfileEnabled](/DeployEdge/microsoft-edge-policies#edgedefaultprofileenabled) permitirá que você defina um perfil padrão a ser usado ao abrir o navegador em vez do último perfil usado. Essa política não será aplicável se o `--profile-directory` parâmetro tiver sido especificado.

- **Alternador de Certificado do Cliente.** Esse recurso oferecerá uma maneira para os usuários limparem o certificado lembrado e ressurgir o seletor de certificado ao visitar um site que exige autenticação de certificado http. Isso pode ser feito sem sair manualmente Microsoft Edge.

- **Inicie o Aplicativos Web Progressivo (PWAs) na Barra de Favoritos.** Melhorias na PWA de inicialização começarão a aparecer começando com um ícone de Aplicativos que pode ser adicionado à barra de ferramentas.

- **Gerencie a configuração "Permitir extensões de outras lojas".** Use a [política ControlDefaultStateOfAllowExtensionFromOtherStoresSettingEnabled](/DeployEdge/microsoft-edge-policies#controldefaultstateofallowextensionfromotherstoressettingenabled) para controlar o estado padrão da configuração "Permitir extensões de outros repositórios".

### <a name="policy-updates"></a>Atualizações de política

#### <a name="new-policies"></a>Novas políticas

- [ConfigureKeyboardShortcuts](/DeployEdge/microsoft-edge-policies#configurekeyboardshortcuts) - Configure a lista de comandos para os quais desabilitar atalhos de teclado
- [ControlDefaultStateOfAllowExtensionFromOtherStoresSettingEnabled](/DeployEdge/microsoft-edge-policies#controldefaultstateofallowextensionfromotherstoressettingenabled) - Configurar o estado padrão da configuração Permitir extensões de outras lojas
- [EdgeAssetDeliveryServiceEnabled](/DeployEdge/microsoft-edge-policies#edgeassetdeliveryserviceenabled) - Permitir que recursos baixem ativos do Serviço de Entrega de Ativos
- [EdgeDefaultProfileEnabled](/DeployEdge/microsoft-edge-policies#edgedefaultprofileenabled) - Configuração de perfil padrão habilitada
- [InternetExplorerModeEnableSavePageAs](/DeployEdge/microsoft-edge-policies#internetexplorermodeenablesavepageas) - Permitir Salvar página como no modo Internet Explorer
- [KioskSwipeGesturesEnabled](/DeployEdge/microsoft-edge-policies#kioskswipegesturesenabled) - Deslizar gestos no modo de quiosque do Microsoft Edge habilitado
- [MicrosoftOfficeMenuEnabled](/DeployEdge/microsoft-edge-policies#microsoftofficemenuenabled) - Permitir que os usuários acessem o menu do Microsoft Office
- [SiteSafetyServicesEnabled](/DeployEdge/microsoft-edge-policies#sitesafetyservicesenabled) - Permitir que os usuários configurem os serviços de segurança do site

#### <a name="deprecated-policy"></a>Política preterida

- [ForceCertificatePromptsOnMultipleMatches](/DeployEdge/microsoft-edge-policies#forcecertificatepromptsonmultiplematches) - Configure se o Microsoft Edge deve selecionar automaticamente um certificado quando houver várias correspondências de certificado para um site configurado com "AutoSelectCertificateForUrls"

#### <a name="obsoleted-policy"></a>Política obsoleta

- [WebSQLInThirdPartyContextEnabled](/DeployEdge/microsoft-edge-policies#websqlinthirdpartycontextenabled) - Forçar o WebSQL em contextos de terceiros para ser habilitado novamente


## <a name="version-1000118527-march-31"></a>Versão 100.0.1185.27: 31 de março

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-1000118523-march-28"></a>Versão 100.0.1185.23: 28 de março

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-1000118517-march-23"></a>Versão 100.0.1185.17: 23 de março

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-1000118512-march-18"></a>Versão 100.0.1185.12: 18 de março

Vários bugs e problemas de desempenho corrigidos.

### <a name="feature-updates"></a>Atualizações de recursos

- **Simplificando as Ativações do protocolo de aplicativo do Microsoft 365.** As Ativações do protocolo de aplicativo do Microsoft 365 nos serviços confiáveis de armazenamento em nuvem da Microsoft agora iniciarão determinados aplicativos diretamente do Microsoft 365, incluindo subdomínios do SharePoint e URLs do Microsoft OneDrive. Você pode usar as políticas [AutoLaunchProtocolsComponentEnabled](/deployedge/microsoft-edge-policies#autolaunchprotocolscomponentenabled) e [AutoLaunchProtocolsFromOrigins](/deployedge/microsoft-edge-policies#autolaunchprotocolsfromorigins) para habilitar os prompts de ativação do protocolo de aplicativo, se desejado, e para definir outros aplicativos e serviços em que os avisos são habilitados ou desabilitados.

## <a name="version-1000118510-march-17"></a>Versão 100.0.1185.10: 17 de março

### <a name="feature-updates"></a>Atualizações de recursos

- **Melhorias na experiência de Gerenciamento de Lista de Sites na Nuvem para o Modo IE.** Você pode configurar o compartilhamento de cookie de sessão entre Microsoft Edge Internet Explorer para Modo IE em sua lista de sites na Administração Microsoft 365 Central. **Nota:** Essa é uma distribuição de recursos controlada. Se você não vir esse recurso, verifique novamente à medida que continuarmos nossa distribuição

- **Visualize arquivos PDF no Microsoft Outlook e no Explorador de Arquivos.** Os usuários podem visualizar um arquivo PDF em uma visualização somente leitura leve e avançada.  Disponível para Outlook pdf da área de trabalho ou para arquivos PDF locais usando Explorador de Arquivos.  

- **Sincronização de aplicativo Web instalada em todos os dispositivos da área de trabalho.** Sites ou PWAs (Aplicativos Web progressivos) que foram instalados como aplicativos serão sincronizados em todos os dispositivos da área de trabalho em que você entrou e habilitou a sincronização. Eles serão mostrados como "Aplicativos disponíveis" para você instalar. Um aplicativo removido de um dispositivo sincronizará a remoção em todos os dispositivos.

### <a name="policy-updates"></a>Atualizações de política

#### <a name="new-policies"></a>Novas políticas

- [AdsTransparencyEnabled](/DeployEdge/microsoft-edge-policies#adstransparencyenabled) - Configurar se o recurso de transparência de anúncios estiver habilitado
- [DefaultWebHidGuardSetting](/DeployEdge/microsoft-edge-policies#defaultwebhidguardsetting) - Controlar uso da API WebHID
- [HideRestoreDialogEnabled](/DeployEdge/microsoft-edge-policies#hiderestoredialogenabled) - Ocultar a caixa de diálogo das páginas de restauração após a falha do navegador
- [PDFSecureMode](/DeployEdge/microsoft-edge-policies#pdfsecuremode) - Modo de segurança e validação de assinatura digital baseada em certificado no leitor de PDF nativo
- [PromptOnMultipleMatchingCertificates](/DeployEdge/microsoft-edge-policies#promptonmultiplematchingcertificates) - Solicitar que o usuário selecione um certificado quando vários certificados corresponderem
- [WebHidAskForUrls](/DeployEdge/microsoft-edge-policies#webhidaskforurls) - Permitir a API WebHID nesses sites
- [WebHidBlockedForUrls](/DeployEdge/microsoft-edge-policies#webhidblockedforurls) - Bloquear a API WebHID nesses sites

#### <a name="deprecated-policy"></a>Política preterida

- [BackgroundTemplateListUpdatesEnabled](/DeployEdge/microsoft-edge-policies#backgroundtemplatelistupdatesenabled) - Habilitar atualizações em segundo plano para a lista de modelos disponíveis para coleções e outros recursos que usam modelos

#### <a name="obsoleted-policy"></a>Política obsoleta

- [AllowSyncXHRInPageDismissal](/DeployEdge/microsoft-edge-policies#allowsyncxhrinpagedismissal) - Permitir que as páginas enviem solicitações XHR síncronas durante o encerramento da página

## <a name="version-990115039-march-10"></a>Versão 99.0.1150.39: 10 de março

### <a name="feature-updates"></a>Atualizações de recursos

- **Melhorias na experiência de Gerenciamento de Lista de Sites na Nuvem para o Modo IE.** Identifique lacunas em sua lista de sites corporativos configurando relatórios de comentários do site com as políticas [InternetExplorerIntegrationCloudUserSitesReporting](/deployedge/microsoft-edge-policies#internetexplorerintegrationcloudusersitesreporting) e [InternetExplorerIntegrationCloudNeutralSitesReporting](/deployedge/microsoft-edge-policies#internetexplorerintegrationcloudneutralsitesreporting) . Você pode exibir URLs de lista de sites locais de usuários e URLs de site neutro potencialmente configuradas incorretamente na experiência de listas de sites do Microsoft Edge no Administração Microsoft 365 Center. Para saber mais, confira [Exibir comentários do site no Administração Microsoft 365 Center](/deployedge/edge-ie-mode-cloud-site-list-mgmt#view-site-feedback-on-the-microsoft-365-admin-center-1).  **Nota:** Essa é uma distribuição de recursos controlada. Se você não vir esse recurso, verifique novamente à medida que continuarmos nossa distribuição.

## <a name="version-990115030-march-2"></a>Versão 99.0.1150.30: 2 de março

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-990115025-february-25"></a>Versão 99.0.1150.25: 25 de fevereiro

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-990115021-february-22"></a>Versão 99.0.1150.21: 22 de fevereiro

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-990115016-february-14"></a>Versão 99.0.1150.16: 14 de fevereiro

Correção de vários bugs e problemas de desempenho.

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

