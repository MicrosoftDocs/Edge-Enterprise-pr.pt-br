---
title: Notas de versão arquivadas para o Canal Beta do Microsoft Edge
ms.author: leahtu
author: dan-wesley
manager: srugh
ms.date: 08/16/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Notas de versão arquivadas para o Canal Beta do Microsoft Edge
ms.openlocfilehash: a0a5ccc012097f8978bd05366451b8becef5ebf6
ms.sourcegitcommit: f4876eadb712279d577c43950de70fd5e7854c72
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2022
ms.locfileid: "12713305"
---
# <a name="archived-release-notes-for-microsoft-edge-beta-channel"></a>Notas de versão arquivadas para o Canal Beta do Microsoft Edge

Estas notas de versão fornecem informações sobre os novos recursos e atualizações não relacionadas à segurança que estão inclusos no canal Beta do Microsoft Edge. Para entender os canais do Microsoft Edge, confira a [Visão geral dos canais do Microsoft Edge](microsoft-edge-channels.md). Todas as atualizações de segurança estão listadas [aqui](microsoft-edge-relnotes-security.md).

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

## <a name="version-1010121010-april-8"></a>Versão 101.0.1210.10: 8 de abril

### <a name="feature-updates"></a>Atualizações de recursos

- **Capacidade de definir o perfil padrão.** A [política EdgeDefaultProfileEnabled](/DeployEdge/microsoft-edge-policies#edgedefaultprofileenabled) permitirá que você defina um perfil padrão a ser usado ao abrir o navegador em vez do último perfil usado. Essa política não será aplicável se o parâmetro `--profile-directory` tiver sido especificado.

- **Inicie o Aplicativos Web Progressivo (PWAs) na Barra de Favoritos.** Melhorias na experiência de inicialização do PWA começarão a aparecer começando com um ícone de Aplicativos que pode ser adicionado à barra de ferramentas.

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

- **Melhorias na experiência de Gerenciamento de Lista de Sites na Nuvem para o Modo IE.** Você pode configurar o compartilhamento de cookie de sessão entre o Microsoft Edge e o Internet Explorer para o Modo IE na lista de sites na Administração Microsoft 365 Central. **Nota:** Essa é uma distribuição de recursos controlada. Se você não vir esse recurso, verifique novamente à medida que continuarmos nossa distribuição

- **Visualize arquivos PDF no Microsoft Outlook e no Explorador de Arquivos.** Os usuários podem visualizar um arquivo PDF em uma visualização somente leitura leve e avançada.  Disponível para anexos pdf da área de trabalho do Outlook ou para arquivos PDF locais usando Explorador de Arquivos.  

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

- **Melhorias na experiência de Gerenciamento de Lista de Sites na Nuvem para o Modo IE.** Identifique lacunas em sua lista de sites corporativos configurando relatórios de comentários do site com as políticas [InternetExplorerIntegrationCloudUserSitesReporting](/deployedge/microsoft-edge-policies#internetexplorerintegrationcloudusersitesreporting) e [InternetExplorerIntegrationCloudNeutralSitesReporting](/deployedge/microsoft-edge-policies#internetexplorerintegrationcloudneutralsitesreporting) . Você pode exibir URLs de lista de sites locais de usuários e URLs de site neutro potencialmente configuradas incorretamente na experiência de listas de sites do Microsoft Edge na Administração Microsoft 365 Center. Para saber mais, confira [Exibir comentários do site no Administração Microsoft 365 Center](/deployedge/edge-ie-mode-cloud-site-list-mgmt#view-site-feedback-on-the-microsoft-365-admin-center-1).  **Nota:** Essa é uma distribuição de recursos controlada. Se você não vir esse recurso, verifique novamente à medida que continuarmos nossa distribuição.

## <a name="version-990115030-march-2"></a>Versão 99.0.1150.30: 2 de março

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-990115025-february-25"></a>Versão 99.0.1150.25: 25 de fevereiro

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-990115021-february-22"></a>Versão 99.0.1150.21: 22 de fevereiro

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-990115016-february-14"></a>Versão 99.0.1150.16: 14 de fevereiro

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-990115011-february-9"></a>Versão 99.0.1150.11: 9 de fevereiro

### <a name="feature-updates"></a>Atualizações de recursos

- **Em breve, número de versão de três dígitos na cadeia de caracteres de agente do usuário.** A partir da versão 100, o Microsoft Edge enviará um número de versão de três dígitos no cabeçalho do agente de usuário, por exemplo, "Edg/100". A partir do Microsoft Edge 97, os proprietários de sites podem testar essa próxima cadeia de caracteres de agente habilitando o sinalizador de experimento **#force-major-version-to-100** em *edge://flags* para garantir que sua lógica de análise do agente de usuário seja robusta e funcione conforme o esperado.

- **Personalize experiências de vários perfis com preferências de perfil de sites.** Os usuários podem personalizar sua experiência de vários perfis com a capacidade de criar uma lista personalizada de sites de alternância automática de perfis no Microsoft Edge.

- **Compartilhamento bidirecional de cookie para o modo IE.** Esse recurso expande a funcionalidade de compartilhamento de cookies já disponível e permite que os usuários sincronizem cookies de sessão específicos do modo Internet Explorer/IE para o Microsoft Edge. Para obter mais informações, consulte [Compartilhamento de cookies entre o Microsoft Edge e o Internet Explorer](/deployedge/edge-ie-mode-add-guidance-cookieshare).

- **Navegue por documentos PDF usando miniaturas da página.** Agora você poderá navegar pelo documento PDF usando miniaturas que representam as páginas. Essas miniaturas aparecerão no painel no lado esquerdo do leitor de PDF.

- **Configure a lista de domínios nos quais a Interface de usuário (UI) do gerenciador de senhas de Salvar e Preencher será desabilitada.** Use a política [PasswordManagerBlocklist](/deployedge/microsoft-edge-policies#passwordmanagerblocklist) para configurar a lista de domínios (somente esquemas e nomes do host HTTP/HTTPS) onde o Microsoft Edge deve desabilitar o gerenciador de senhas. Isso significa que os fluxos de trabalho Salvar e Preencher serão desabilitados, o que garante que as senhas desses sites não possam ser salvas ou preenchidas automaticamente em formulários da Web.

- **Atualize as extensões para o repositório de Complementos do Microsoft Edge usando as APIs (em versão prévia pública).** Você pode integrar essas APIs diretamente ao pipeline de build e publicar atualizações de pacote no site do Complemento do Microsoft Edge. Para saber mais, confira [Usando a API de Complementos do Microsoft Edge (em versão prévia privada)](/microsoft-edge/extensions-chromium/publish/api/using-addons-api)

### <a name="policy-updates"></a>Atualizações de política

#### <a name="new-policies"></a>Novas políticas

- [AllowGamesMenu](/DeployEdge/microsoft-edge-policies#allowgamesmenu) - Permitir que os usuários acessem o menu de jogos
- [DoNotSilentlyBlockProtocolsFromOrigins](/DeployEdge/microsoft-edge-policies#donotsilentlyblockprotocolsfromorigins) - Definir uma lista de protocolos que não podem ser bloqueados silenciosamente pela proteção anti-inundação
- [HubsSidebarEnabled](/DeployEdge/microsoft-edge-policies#hubssidebarenabled) – Mostrar barra lateral dos hubs
- [InternetExplorerIntegrationCloudNeutralSitesReporting](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationcloudneutralsitesreporting) - Configurar relatórios de URLs de sites neutros potencialmente mal configurados para o aplicativo Listas de sites do Centro de administração do M365
- [InternetExplorerIntegrationCloudUserSitesReporting](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationcloudusersitesreporting) - Configurar o relatório de entradas da lista de usuários do modo IE para o aplicativo Listas de sites do Centro de administração do M365
- [PasswordManagerBlocklist](/DeployEdge/microsoft-edge-policies#passwordmanagerblocklist) - Configurar a lista de domínios dos quais a interface do usuário do gerenciador de senhas (Salvar e Preencher) será desabilitada
- [RelatedMatchesCloudServiceEnabled](/DeployEdge/microsoft-edge-policies#relatedmatchescloudserviceenabled) - Configurar correspondências relacionadas em Localizar na página
- [SignInCtaOnNtpEnabled](/DeployEdge/microsoft-edge-policies#signinctaonntpenabled) - Habilitar caixa de diálogo de clique para ação de entrada
- [UserAgentReduction](/DeployEdge/microsoft-edge-policies#useragentreduction) - Habilitar ou desabilitar a Redução do agente de usuário

## <a name="version-980110848-february-8"></a>Versão 98.0.1108.48: 8 de fevereiro

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-980110843-february-3"></a>Versão 98.0.1108.43: 3 de fevereiro

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-980110842-february-2"></a>Versão 98.0.1108.42: 2 de fevereiro

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-980110839-january-31"></a>Versão 98.0.1108.39: 31 de janeiro

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-980110833-january-24"></a>Versão 98.0.1108.33: 24 de janeiro

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-980110827-january-19"></a>Versão 98.0.1108.27: 19 de janeiro

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-980110823-january-14"></a>Versão 98.0.1108.23: 14 de janeiro

### <a name="feature-updates"></a>Atualizações de recursos

- **Melhore sua segurança na Web.** Um modo de navegação no Microsoft Edge em que a segurança do navegador tem prioridade, fornecendo uma camada extra de proteção ao navegar pela Web. Os administradores podem aplicar as seguintes Políticas de Grupo às áreas de trabalho do usuário final (Windows, macOS e Linux) para ajudar a proteger contra zero dias. Essas políticas também fazem com que sites importantes e aplicativos de linha de negócios continuem funcionando conforme o esperado. Esse recurso é um grande passo à frente porque nos permite atenuar zero dias ativos imprevistos (com base nas tendências históricas). Quando ativado, esse recurso traz proteção de pilha imposta por hardware, ACG (Proteção de Código Arbitrário) e CFG (Proteção de Fluxo de Conteúdo) como suporte a mitigações de segurança para aumentar a segurança dos usuários na Web.
Políticas de Grupo:
  - [EnhanceSecurityMode](/DeployEdge/microsoft-edge-policies#enhancesecuritymode)
  - [EnhanceSecurityModeBypassListDomains](/DeployEdge/microsoft-edge-policies#enhancesecuritymodebypasslistdomains)
  - [EnhanceSecurityModeEnforceListDomains](/DeployEdge/microsoft-edge-policies#enhancesecuritymodeenforcelistdomains)

- **Senha primária personalizada.** O navegador já tem a funcionalidade em que os usuários podem adicionar uma etapa de autenticação antes que as senhas salvas sejam preenchidas automaticamente em formulários da Web. Isso adiciona outra camada de privacidade e ajuda a impedir que usuários não autorizados usem senhas salvas para fazer logon em sites. A senha primária personalizada é uma evolução desse mesmo recurso, onde os usuários agora poderão usar uma cadeia de caracteres personalizada de sua escolha como senha principal. Depois de habilitado, os usuários inserirão essa senha para autenticar a si mesmos e terão suas senhas salvas preenchidas automaticamente em formulários da Web.

- **Barras de rolagem de sobreposição adicionadas ao Microsoft Edge.** Atualizamos nossas barras de rolagem com um design baseado em sobreposição. Os usuários podem ativar esse recurso em *edge://flags*.

### <a name="policy-updates"></a>Atualizações de política

#### <a name="new-policies"></a>Novas Políticas

- [AddressBarEditingEnabled](/DeployEdge/microsoft-edge-policies#addressbareditingenabled) – Configurar a edição da barra de endereços.
- [EdgeFollowEnabled](/DeployEdge/microsoft-edge-policies#edgefollowenabled) – Habilitar o serviço Seguir no Microsoft Edge.
- [EnhanceSecurityMode](/DeployEdge/microsoft-edge-policies#enhancesecuritymode) – aprimora o estado de segurança no Microsoft Edge.
- [EnhanceSecurityModeBypassListDomains](/DeployEdge/microsoft-edge-policies#enhancesecuritymodebypasslistdomains) – configure a lista de domínios para os quais o modo de segurança avançada não será imposto.
- [EnhanceSecurityModeEnforceListDomains](/DeployEdge/microsoft-edge-policies#enhancesecuritymodeenforcelistdomains) – Configure a lista de domínios para os quais o modo de segurança avançada sempre será imposto.
- [InAppSupportEnabled](/DeployEdge/microsoft-edge-policies#inappsupportenabled) – Suporte no aplicativo habilitado.
- [MicrosoftEdgeInsiderPromotionEnabled](/DeployEdge/microsoft-edge-policies#microsoftedgeinsiderpromotionenabled) – Promoção do Microsoft Edge Insider Habilitada.
- [PrintStickySettings](/DeployEdge/microsoft-edge-policies#printstickysettings) – Imprimir configurações autoadesas de visualização.
- [SandboxExternalProtocolBlocked](/DeployEdge/microsoft-edge-policies#sandboxexternalprotocolblocked) – permitir que o Microsoft Edge bloqueie as navegação para protocolos externos em um iframe em área restrita.
- [U2fSecurityKeyApiEnabled](/DeployEdge/microsoft-edge-policies#u2fsecuritykeyapienabled) – Permitir o uso da API de Chave de Segurança U2F preterida.

## <a name="version-970107254-january-5"></a>Versão 97.0.1072.54: 5 de janeiro

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-970107252-january-3"></a>Versão 97.0.1072.52: 3 de janeiro

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-970107241-december-20"></a>Versão 97.0.1072.41: 20 de dezembro

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-970107234-december-13"></a>Versão 97.0.1072.34: 13 de dezembro

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-970107228-december-8"></a>Versão 97.0.1072.28: 8 de dezembro

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-970107221-december-1"></a>Versão 97.0.1072.21: 1 de dezembro

### <a name="feature-updates"></a>Atualizações de recursos

- **Use o perfil atual para entrar em sites quando várias contas corporativas ou de estudante forem conectadas em um dispositivo.** Quando várias contas corporativas ou de estudante estiverem conectadas em um dispositivo, os usuários deverão escolher uma conta no seletor de contas para continuar suas visitas a sites. Nesta versão, os usuários serão solicitados a permitir que o Microsoft Edge entre nos sites automaticamente com a conta corporativa e de estudante que está conectada ao perfil atual. Os usuários podem ativar e desativar esse recurso em **Configurações/Preferências de Perfil**.

- **Adicione suporte para a Prevenção contra Perda de Dados de Ponto de Extremidade (DLP) da Microsoft no macOS.** A imposição de política DLP do Ponto de Extremidade da Microsoft está disponível nativamente no macOS.

- **Abra arquivos PDF assinados digitalmente.**  As assinaturas digitais são amplamente usadas para validar a autenticidade de um documento e as alterações feitas em um documento. Os usuários podem validar as assinaturas para arquivos PDF diretamente do navegador, sem a necessidade de suplementos.

- **Citações no Microsoft Edge.** Citar fontes para pesquisa é um requisito comum para estudantes. Eles têm que gerenciar muitas referências e fontes de pesquisa, o que não é uma tarefa fácil. Eles também precisam traduzir essas citações para formatos de citação adequados, como APA, MLA e Chicago. Esse novo recurso "Citações" no Microsoft Edge (agora em versão prévia) oferece aos alunos uma maneira melhor de gerenciar e gerar citações à medida que pesquisam online. Com as citações ativadas em Coleções ou em **Configurações e muito mais (Alt-F)**, o Microsoft Edge gera automaticamente citações que os alunos podem usar mais tarde para que possam se concentrar em suas pesquisas. Quando terminarem, eles podem facilmente compilar essas citações em uma entrega final. Para obter mais informações, confira [Visualizando Citações no Microsoft Edge](https://blogs.windows.com/msedgedev/2021/11/04/preview-citations-feature-edge/).

### <a name="policy-updates"></a>Atualizações de política

#### <a name="new-policies"></a>Novas Políticas

- [AccessibilityImageLabelsEnabled](/DeployEdge/microsoft-edge-policies#accessibilityimagelabelsenabled) - Obter descrições de imagens do Microsoft habilitado
- [CORSNonWildcardRequestHeadersSupport](/DeployEdge/microsoft-edge-policies#corsnonwildcardrequestheaderssupport) - Suporte de cabeçalho de solicitação CORS não curinga habilitado
- [EdgeDiscoverEnabled](/DeployEdge/microsoft-edge-policies#edgediscoverenabled) - Recurso de descoberta no Microsoft Edge
- [EdgeEnhanceImagesEnabled](/DeployEdge/microsoft-edge-policies#edgeenhanceimagesenabled) - Aprimorar imagens habilitadas
- [InternetExplorerModeTabInEdgeModeAllowed](/DeployEdge/microsoft-edge-policies#internetexplorermodetabinedgemodeallowed) - Permitir que sites configurados para o modo Internet Explorer sejam abertos no Microsoft Edge
- [SameOriginTabCaptureAllowedByOrigins](/DeployEdge/microsoft-edge-policies#sameorigintabcaptureallowedbyorigins) - Permitir captura da mesma Guia de origem por essas origens
- [ScreenCaptureAllowedByOrigins](/DeployEdge/microsoft-edge-policies#screencaptureallowedbyorigins) - Permitir captura de área de trabalho, janela e guia por essas origens
- [SerialAllowAllPortsForUrls](/DeployEdge/microsoft-edge-policies#serialallowallportsforurls) - Conceder automaticamente permissão aos sites para conectar todas as portas seriais
- [SerialAllowUsbDevicesForUrls](/DeployEdge/microsoft-edge-policies#serialallowusbdevicesforurls) - Conceder automaticamente permissão aos sites para se conectar a dispositivos seriais USB
- [SmartScreenDnsRequestsEnabled](/DeployEdge/microsoft-edge-policies#smartscreendnsrequestsenabled) - Habilitar solicitações de DNS do Microsoft Defender SmartScreen
- [TabCaptureAllowedByOrigins](/DeployEdge/microsoft-edge-policies#tabcaptureallowedbyorigins) - Permitir captura de guias por essas origens
- [WebSQLInThirdPartyContextEnabled](/DeployEdge/microsoft-edge-policies#websqlinthirdpartycontextenabled) - Forçar o WebSQL em contextos de terceiros para ser habilitado novamente
- [WindowCaptureAllowedByOrigins](/DeployEdge/microsoft-edge-policies#windowcaptureallowedbyorigins) - Permitir captura de janela e guia por essas origens

#### <a name="obsoleted-policies"></a>Políticas Obsoletas

- [AppCacheForceEnabled](/deployedge/microsoft-edge-policies#appcacheforceenabled) - Permite reabilitar o recurso AppCache, mesmo que ele esteja desativado por padrão.

## <a name="version-960105434-november-23"></a>Versão 96.0.1054.34: 23 de novembro

Correção de vários bugs e problemas de desempenho.

## <a name="version-960105426-november-17"></a>Versão 96.0.1054.26: 17 de novembro

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-960105424-november-16"></a>Versão 96.0.1054.24: 16 de novembro

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-960105413-november-5"></a>Versão 96.0.1054.13: 5 de novembro

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-96010548-november-1"></a>Versão 96.0.1054.8: 1º de novembro

### <a name="feature-updates"></a>Atualizações de recursos

- **Inicie o PWA (Aplicativo Web Progressivo) diretamente por meio de links de protocolo.** Permita que os PWAs instalados manipulem links que usam um protocolo específico para uma experiência mais integrada.

- **Saiba como resolver problemas matemáticos com o Math Solver.** Estamos felizes em anunciar que você pode usar o Math Solver no Microsoft Edge para obter ajuda com uma ampla variedade de conceitos matemáticos. Esses conceitos variam de equações aritméticas e quadráticas elementares a trigonometria e cálculo. O Math Solver permite que você tire uma foto de um problema de matemática manuscrito ou impresso e, em seguida, fornece uma solução instantânea com instruções passo a passo para ajudá-lo a aprender a alcançar a solução sem ajuda. O Math Solver também vem com um teclado matemático que você pode usar para digitar facilmente problemas matemáticos. Esse teclado elimina a necessidade de pesquisar em torno de um teclado tradicional para encontrar os caracteres matemáticos necessários. Depois de resolver o problema, o Math Solver fornece opções para continuar aprendendo com testes, planilhas e tutoriais em vídeo.

- **Realce de forma livre em PDFs.** A experiência de exibição e marcação em PDF é aprimorada com a adição de marcadores de forma livre. Você pode realçar seções em PDFs às qual não tem acesso e documentos digitalizados.

- **Proteção de pilha imposta por hardware.**  O Microsoft Edge começará a dar suporte a um modo de navegação ainda mais seguro que usa o fluxo de controle dependente de hardware para processos de navegador em hardware com suporte (Intel 11ª Geração. ou AMD Zen 3). Observação: como esta é uma Distribuição de Recursos Controlada, talvez você não observe esse recurso habilitado em todos os dispositivos. Você pode habilitar ou desabilitar a Proteção contra Pilha imposta por hardware manipulando IFEO (Opções de Execução de Arquivo de Imagem) usando a política de grupo.

- **Nova caixa de diálogo de aviso para sites de typosquatting.** O navegador agora mostrará um aviso em alguns sites com URLs semelhantes a outros sites. Essa interface do usuário usa heurística do lado do cliente para avisar os usuários sobre sites que podem estar falsificando sites populares. Para obter mais informações, consulte [O que é typosquatting?](https://support.microsoft.com/topic/what-is-typosquatting-54a18872-8459-4d47-b3e3-d84d9a362eb0).

- **Entrega aprimorada entre o modo IE e o navegador moderno.**  A partir desta versão do Microsoft Edge, as navegação entre o Microsoft Edge e o modo Internet Explorer incluirão dados de formulário e cabeçalhos HTTP adicionais. Os cabeçalhos de referenciador, os dados de postagem, os dados de formulários e os métodos de solicitação serão encaminhados corretamente entre as duas experiências. Você pode especificar quais tipos de dados devem ser incluídos usando a política [InternetExplorerIntegrationComplexNavDataTypes](/deployedge/microsoft-edge-policies#internetexplorerintegrationcomplexnavdatatypes) . Para obter mais informações, consulte as perguntas frequentes: [Meu aplicativo requer a transferência de dados POST entre o modo IE e o Microsoft Edge](./edge-ie-mode-faq.md#my-application-requires-transferring-post-data-between-ie-mode-and-microsoft-edge-is-this-supported).

- **Gerenciamento de Lista de Sites na Nuvem para o modo IE na Visualização Pública.**  O Gerenciamento de Lista de Sites na Nuvem permite que você gerencie suas listas de sites para o modo IE na nuvem sem precisar de uma infraestrutura local para hospedar a lista de sites da sua organização. Você pode acessar o recurso Gerenciamento de Lista de Sites na Nuvem usando a experiência de Listas de Sites do Microsoft Edge no Administração Microsoft 365 Center. Para saber mais, confira o artigo [Gerenciamento de Lista de Sites na Nuvem para modo IE (Versão Prévia](./edge-ie-mode-cloud-site-list-mgmt.md) Pública).

- **Atualize o Microsoft Edge WebWiew2 usando o WSUS.** Os administradores de TI que usam o WSUS para atualizar o Microsoft Edge também poderão atualizar o Microsoft Edge WebView2 usando o WSUS. Essa funcionalidade oferece aos administradores um processo de manutenção mais fácil para dispositivos offline.

- **Atualizações do WSUS para o Servidor.** As atualizações do WSUS e do Catálogo para canais do Microsoft Edge (Estável, Beta, Desenvolvimento) agora serão aplicadas a SKUs do Windows Server que têm o Microsoft Edge instalado, incluindo o Windows Server 2022. Para obter mais informações sobre como configurar atualizações do WSUS para o Microsoft Edge, consulte [Atualizar o Microsoft Edge](/mem/configmgr/apps/deploy-use/deploy-edge?bc=%2FDeployEdge%2Fbreadcrumb%2Ftoc.json&toc=%2FDeployEdge%2Ftoc.json#update-microsoft-edge).

### <a name="policy-updates"></a>Atualizações de política

#### <a name="new-policies"></a>Novas Políticas

- [ApplicationGuardUploadBlockingEnabled](/DeployEdge/microsoft-edge-policies#applicationguarduploadblockingenabled) – impede que os arquivos sejam carregados no Application Guard.
- [AudioProcessHighPriorityEnabled](/DeployEdge/microsoft-edge-policies#audioprocesshighpriorityenabled)  - Permitir que o processo de áudio seja executado com prioridade acima do normal no Windows.
- [AutoLaunchProtocolsComponentEnabled](/DeployEdge/microsoft-edge-policies#autolaunchprotocolscomponentenabled) – Componente de protocolos autoLaunch habilitado.
- [EfficiencyMode](/DeployEdge/microsoft-edge-policies#efficiencymode) – configure quando o modo de eficiência deve ficar ativo.
- [ForceSyncTypes](/DeployEdge/microsoft-edge-policies#forcesynctypes) – Configure a lista de tipos incluídos para sincronização.
- [InternetExplorerIntegrationComplexNavDataTypes](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationcomplexnavdatatypes) – Configure se os dados de formulário e os cabeçalhos HTTP serão enviados ao entrar ou sair do modo Internet Explorer.
- [InternetExplorerModeToolbarButtonEnabled](/DeployEdge/microsoft-edge-policies#internetexplorermodetoolbarbuttonenabled) – mostrar o botão Recarregar no modo Internet Explorer na barra de ferramentas.
- [PrintPostScriptMode](/DeployEdge/microsoft-edge-policies#printpostscriptmode) – Imprimir no modo PostScript.
- [PrintRasterizePdfDpi](/DeployEdge/microsoft-edge-policies#printrasterizepdfdpi) – Imprimir em Rasterizar DPI do PDF.
- [RendererAppContainerEnabled](/DeployEdge/microsoft-edge-policies#rendererappcontainerenabled) – habilite o renderizador no contêiner de aplicativo.
- [SharedLinksEnabled](/DeployEdge/microsoft-edge-policies#sharedlinksenabled) – Mostrar links compartilhados de aplicativos do Microsoft 365 no Histórico.
- [TyposquattingCheckerEnabled](/DeployEdge/microsoft-edge-policies#typosquattingcheckerenabled) – Configure Edge TyposquattingChecker.

<!-- end major 96 --->

## <a name="version-950102038-october-28"></a>Versão 95.0.1020.38: 28 de outubro

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-950102020-october-11"></a>Versão 95.0.1020.20: 11 de outubro

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-950102014-october-5"></a>Versão 95.0.1020.14: 5 de outubro

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-95010209-september-28"></a>Versão 95.0.1020.9: 28 de setembro

### <a name="feature-updates"></a>Atualizações de recursos

- **Veja no Explorador de Arquivos o suporte para bibliotecas do Microsoft Office SharePoint Online no Microsoft Edge.**  Agora você pode habilitar a exibição em Explorador de Arquivos para bibliotecas de documentos modernas do SharePoint Online. Para que essa experiência fique visível e funcione para seus usuários, você precisará habilitar a política do Microsoft Edge "Configurar a exibição no recurso Explorador de Arquivos para páginas do [SharePoint no Microsoft Edge"](/deployedge/microsoft-edge-policies#configureviewinfileexplorer) e atualizar sua configuração de locatário do SharePoint Online. Saiba mais: [Exibir arquivos do SharePoint com Explorador de Arquivos no Microsoft Edge – SharePoint no Microsoft 365 | Microsoft Docs](/SharePoint/sharepoint-view-in-edge).

- **Os links de URL do arquivo de zona da intranet serão abertos no Windows Explorador de Arquivos.**  Você pode permitir links de URL de arquivos para arquivos da zona intranet originários de sites HTTPS da zona intranet para abrir o Windows Explorador de Arquivos para esse arquivo ou diretório. Você pode habilitar esta experiência usando a política [IntranetFileLinksEnabled](/deployedge/microsoft-edge-policies#intranetfilelinksenabled).

- **Melhorias na experiência de downloads.**  O suporte para a experiência do usuário de download está sendo estendido para PWAs e WebView de aplicativos Web progressivos. Também começaremos a suportar o arrastar e soltar para o Explorador de Arquivos e Desktop.

- **Continue de onde parou em documentos PDF.**  Você pode retomar a leitura no local em que fechou o documento PDF pela última vez.

- **O modo de eficiência estende a vida útil da bateria quando seu laptop entra em modo de economia de bateria.**  O modo de eficiência ficará ativo quando seu laptop entrar no modo de economia de bateria para permitir que o navegador gerencia o uso de recursos para aumentar a vida útil da bateria de sua máquina. Você terá quatro opções para quando o modo de eficiência ficar ativo, Desconectado e bateria fraca, Desconectado, Sempre e Nunca. Observação: esta é uma distribuição de recursos controlada. Os dispositivos com bateria devem ter o recurso ativado.

***Novas Políticas***

- [BrowserLegacyExtensionPointsBlockingEnabled](/DeployEdge/microsoft-edge-policies#browserlegacyextensionpointsblockingenabled) – habilite o bloqueio de ponto de extensão herdado do navegador.
- [CrossOriginWebAssemblyModuleSharingEnabled](/DeployEdge/microsoft-edge-policies#crossoriginwebassemblymodulesharingenabled) - Especifica se os módulos WebAssembly podem ser enviados entre origens.
- [DisplayCapturePermissionsPolicyEnabled](/DeployEdge/microsoft-edge-policies#displaycapturepermissionspolicyenabled) - Especifica se a política de permissões de captura de exibição está marcada ou ignorada.
- [InternetExplorerIntegrationWindowOpenHeightAdjustment](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationwindowopenheightadjustment) – Configure o ajuste de pixel entre window.open heights originado de páginas do modo IE versus páginas do modo Microsoft Edge.
- [InternetExplorerIntegrationWindowOpenWidthAdjustment](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationwindowopenheightadjustment) – Configure o ajuste de pixel entre larguras window.open originados de páginas do modo IE versus páginas do modo Microsoft Edge.
- [IntranetFileLinksEnabled](/DeployEdge/microsoft-edge-policies#intranetfilelinksenabled) – Permitir que links de URL do arquivo de zona da intranet do Microsoft Edge abram no Windows Explorador de Arquivos.
- [ShadowStackCrashRollbackBehavior](/DeployEdge/microsoft-edge-policies#shadowstackcrashrollbackbehavior) – Configure o comportamento de reversão de falha do ShadowStack.
- [VisualSearchEnabled](/DeployEdge/microsoft-edge-policies#visualsearchenabled) – Habilitar pesquisa visual.

***Políticas Obsoletas***

- [InternetExplorerIntegrationTestingAllowed](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationtestingallowed) - Permitir teste no modo Internet Explorer.
- [LegacySameSiteCookieBehaviorEnabled](/DeployEdge/microsoft-edge-policies#legacysamesitecookiebehaviorenabled) -habilita a configuração padrão de cookie herdado SameSite padrão.

## <a name="version-94099223-september-17"></a>Versão 94.0.992.23: 17 de setembro

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-94099219-september-13"></a>Versão 94.0.992.19: 13 de setembro

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-94099214-september-7"></a>Versão 94.0.992.14: 7 de setembro

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-9409929-september-2"></a>Versão 94.0.992.9: 2 de setembro

### <a name="feature-updates"></a>Atualizações de recursos

- **O Microsoft Edge está mudando para uma cadência de 4 semanas para atualizações nos canais Beta e Estável.**  Adotaremos um novo ciclo de lançamento de 4 semanas para versões principais. Você pode ler mais sobre a decisão aqui: https://blogs.windows.com/msedgedev/2021/03/12/new-release-cycles-microsoft-edge-extended-stable/

- **Nova opção estável estendida sendo oferecida.**  Estamos oferecendo uma nova opção Estável Estendida para nossos clientes Empresariais gerenciados. A opção Estável Estendida permanecerá em revisões pares e será atualizada a cada 8 semanas. Haverá uma atualização de segurança quinzenal.  Informações adicionais aqui: https://blogs.windows.com/msedgedev/2021/07/15/opt-in-extended-stable-release-cycle/

- **Melhorias no comportamento padrão de abertura de arquivos MHTML.**  Os arquivos MHTML continuarão a abrir no modo IE se o modo IE estiver habilitado, a menos que o arquivo MHTML tenha sido salvo do Microsoft Edge (usando as opções Salvar como ou Salvar página como no Microsoft Edge). Se o arquivo foi salvo do Microsoft Edge, ele agora será aberto no Microsoft Edge.  Essa alteração corrigirá um problema de renderização observado ao abrir um arquivo MHTML no modo IE quando salvo no Microsoft Edge.

- **Restrinja as solicitações de rede privada para proteger contextos.** O acesso a recursos em redes locais (intranet) a partir de páginas na Internet requer que essas páginas sejam entregues por HTTPS. Essa alteração está ocorrendo no projeto Chromium, no qual o Microsoft Edge se baseia. Para obter mais informações, navegue até a [entrada de Status da Plataforma Chrome.](https://chromestatus.com/feature/5436853517811712) Duas políticas de compatibilidade estão disponíveis para oferecer suporte a cenários que precisam preservar a compatibilidade com páginas não seguras: [InsecurePrivateNetworkRequestAllowed](/deployedge/microsoft-edge-policies#insecureprivatenetworkrequestsallowed) e [InsecurePrivateNetworkRequestAllowedForUrls](/deployedge/microsoft-edge-policies#insecureprivatenetworkrequestsallowedforurls).

- **Bloqueie downloads de conteúdo misto.** As páginas seguras só baixarão arquivos hospedados em outras páginas seguras, e os downloads hospedados em páginas não seguras (não HTTPS) serão bloqueados se iniciados em uma página segura. Essa alteração está ocorrendo no projeto Chromium, no qual o Microsoft Edge se baseia. Para obter mais informações, navegue até a [entrada do blog de segurança do Google](https://security.googleblog.com/2020/02/protecting-users-from-insecure_6.html).

- **Habilite o login implícito para contas locais.**   Ao habilitar a política OnlyOnPremisesImplicitSigninEnabled, apenas contas locais serão habilitadas para login implícito.  O Microsoft Edge não tentará entrar implicitamente em contas MSA ou AAD. A atualização de contas locais para contas do AAD também será interrompida.

- **Caixas de texto de formulário livre adicionadas aos documentos PDF.**  Agora damos suporte à adição de caixas de texto de formulário gratuitas a documentos PDF que você pode usar para preencher formulários e adicionar anotações visíveis.

- **Atualize suas senhas com facilidade.**  O navegador agora levará você diretamente para a página Alterar Senha para um determinado site economizando tempo e clicando evitando a necessidade de navegar até a página manualmente. Quando você estiver nessa página, o navegador também preencherá automaticamente sua senha existente e sugerirá uma nova senha forte e exclusiva.  Observe que, atualmente, esse recurso está disponível em um número limitado de sites.  

- **Nova página de configurações de acessibilidade.** Reunimos as configurações relacionadas à acessibilidade em uma única página. Você pode localizar a nova página edge: //settings/accessibility na lista de configurações principal. Aqui você pode localizar configurações para aumentar a página da web, mostrar um contorno de alta visibilidade ao redor da área de foco e outras configurações que podem ajudar a melhorar sua experiência de navegação na web. Continuaremos adicionando novas configurações aqui em versões futuras do Microsoft Edge.

***Novas Políticas***

- [ApplicationGuardPassiveModeEnabled](/DeployEdge/microsoft-edge-policies#applicationguardpassivemodeenabled) Ignorar a configuração da lista de sites do Application Guard e navegar no Edge normalmente
- [OnlyOnPremisesImplicitSigninEnabled](/DeployEdge/microsoft-edge-policies#onlyonpremisesimplicitsigninenabled) Apenas conta local habilitada para entrada implícita
- [WebRtcRespectOsRoutingTableEnabled](/DeployEdge/microsoft-edge-policies#webrtcrespectosroutingtableenabled) Habilite o suporte para regras de tabela de roteamento do sistema operacional Windows ao fazer conexões ponto a ponto via WebRTC

***Política Obsoleta***

- [UserAgentClientHintsEnabled](/DeployEdge/microsoft-edge-policies#useragentclienthintsenabled) Habilite o recurso de Dicas de Cliente do Agente do Usuário

## <a name="version-93096133-august-27"></a>Versão 93.0.961.33: 27 de agosto

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-93096127-august-20"></a>Versão 93.0.961.27: 20 de agosto

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-93096124-august-18"></a>Versão 93.0.961.24: 18 de agosto

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-93096111-august-3"></a>Versão 93.0.961.11: 3 de agosto

### <a name="feature-updates"></a>Atualizações de recursos

- **Preferências Iniciais no Microsoft Edge.**  A partir da versão 93 do Microsoft Edge, a implantação do Microsoft Edge em sua empresa ficará mais fácil com a adição de [Preferências Iniciais](/deployedge/initial-preferences-support-on-microsoft-edge-browser).

- **O modo IE no Microsoft Edge dará suporte ao comportamento "sem mesclagem".**  A partir da versão 93 do Microsoft Edge, o modo IE no Microsoft Edge será compatível com "sem mesclagem". Para um usuário final, quando uma nova janela do navegador é iniciada de um aplicativo de modo IE, ela estará em uma sessão separada, semelhante ao comportamento no IE11. Você precisará ajustar sua lista de sites para configurar sites que precisam impedir o compartilhamento de sessão. Nos bastidores, para cada janela do Microsoft Edge, a primeira vez que uma guia de modo IE é visitada dentro dessa janela, se for um dos sites designados "sem mesclagem", essa janela será bloqueada em uma sessão do IE "sem mesclagem" diferente de todas as outras janelas do Microsoft Edge pelo menos até que a última guia de modo IE seja fechada nessa janela. Saiba mais [aqui](/deployedge/edge-ie-mode-faq#does-ie-mode-on-microsoft-edge-support-the--no-merge--option-that-was-supported-in-internet-explorer-11-).

- **Grupos de Guias.**  A capacidade de categorizar guias em grupos definidos pelo usuário ajuda você a encontrar, alternar e gerenciar guias com mais eficiência em vários fluxos de trabalho. Para habilitar isso, estamos ativando o agrupamento de guias começando com o Microsoft Edge versão 93.

- **Ocultar a barra de título ao usar Guias Verticais.**  Obtenha os pixels extras de volta ocultando a barra de título do navegador, enquanto estiver em Guias Verticais. A partir do Microsoft Edge versão 93, você pode ir para edge://settings/appearance e, na seção Personalizar Barra de Ferramentas, selecione a opção para ocultar a barra de título enquanto estiver no modo Guia Vertical.

- **Video em Picture-in-Picture (PiP) da barra de ferramentas de foco.**  A partir da versão 93 do Microsoft Edge, ficará ainda mais fácil entrar no modo Imagem em Imagem (PiP). Quando você passar o mouse sobre um vídeo com suporte, aparecerá uma barra de ferramentas que permite que você veja esse vídeo em uma janela PiP.  Observação: isso está disponível atualmente para usuários do Microsoft Edge no macOS.  Verifique novamente em breve à medida que continuarmos nossa distribuição para usuários do Windows.

- **Remoção do 3DES no TLS.**  A partir do Microsoft Edge versão 93, o suporte para o TLS_RSA_WITH_3DES_EDE_CBC_SHA de criptografia será removido. Essa alteração está ocorrendo no projeto Chromium, no qual o Microsoft Edge se baseia. Para obter mais informações, navegue até a [entrada de Status da Plataforma Chrome.](https://chromestatus.com/feature/6678134168485888) Além disso, no Microsoft Edge versão 93, a política [TripleDESEnabled](/deployedge/microsoft-edge-policies#tripledesenabled) estará disponível para dar suporte a cenários que precisam preservar a compatibilidade com servidores desatualizados. Essa política de compatibilidade se tornará obsoleta e não funcionará no Microsoft Edge versão 95. Certifique-se de atualizar os servidores afetados antes disso.

- **Políticas para ignorar prompts do ClickOnce e DirectInvoke.**  Atualizamos nossas políticas para permitir ignorar prompts do ClickOnce e o aplicativo do DirectInvoke para tipos de arquivo especificados, de domínios especificados. Para fazer isso, você precisará:

  - Habilitar [ClickOnceEnabled](/deployedge/microsoft-edge-policies#clickonceenabled) ou [DirectInvokeEnabled](/deployedge/microsoft-edge-policies#directinvokeenabled)
  - Habilitar a política [AutoOpenFileTypes](/deployedge/microsoft-edge-policies#autoopenfiletypes) e definir a lista de tipos de arquivo específicos para os quais ClickOnce e DirectInvoke devem ser desabilitados
  - Habilite [a política AutoOpenAllowedForURLs](/deployedge/microsoft-edge-policies#autoopenallowedforurls) e defina a lista de domínios específicos para os qual o ClickOnce e o DirectInvoke serão desabilitados

  Observação: AutoOpenAllowedForURLs é uma política de suporte para AutoOpenFileTypes. Se AutoOpenAllowedForURLs não estiver definido e AutoOpenFileTypes estiver definido, os tipos de arquivo listados abrirão automaticamente de todas as URLs.

### <a name="new-policies"></a>Novas políticas

- [AutoplayAllowlist](/DeployEdge/microsoft-edge-policies#autoplayallowlist) Permitir reprodução automática de mídia em sites específicos
- [CECPQ2Enabled](/DeployEdge/microsoft-edge-policies#cecpq2enabled) CECPQ2 pós-quantum key-agreement habilitado para TLS
- [ConfigureViewInFileExplorer](/DeployEdge/microsoft-edge-policies#configureviewinfileexplorer) Configure a Exibição no recurso Explorador de Arquivos para páginas do SharePoint no Microsoft Edge
- [DefaultJavaScriptJitSetting](/DeployEdge/microsoft-edge-policies#defaultjavascriptjitsetting) Controlar o uso do JavaScript JIT
- [ShowPDFDefaultRecommendationsEnabled](/DeployEdge/microsoft-edge-policies#showpdfdefaultrecommendationsenabled) Permitir que as notificações definam Microsoft Edge como leitor de PDF padrão
- [FeatureFlagOverridesControl](/DeployEdge/microsoft-edge-policies#featureflagoverridescontrol) Configure a capacidade dos usuários de substituir sinalizadores de recurso
- [ImplicitSignInEnabled](/DeployEdge/microsoft-edge-policies#implicitsigninenabled) Habilitar entrada implícita
- [InternetExplorerIntegrationCloudSiteList](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationcloudsitelist) Configure modo Empresarial Lista de Sites na Nuvem do modo Empresarial
- [InternetExplorerIntegrationSiteListRefreshInterval](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationsitelistrefreshinterval) Configure com que frequência a Lista de Sites do modo Empresarial é atualizada
- [JavaScriptJitAllowedForSites](/DeployEdge/microsoft-edge-policies#javascriptjitallowedforsites) Permitir que o JavaScript use JIT nesses sites
- [JavaScriptJitBlockedForSites](/DeployEdge/microsoft-edge-policies#javascriptjitblockedforsites) Impedir que o JavaScript use JIT nesses sites
- [LocalBrowserDataShareEnabled](/DeployEdge/microsoft-edge-policies#localbrowserdatashareenabled) Permitir que o Windows pesquise dados de navegação Microsoft Edge locais
- [MAUEnabled](/DeployEdge/microsoft-edge-policies#mauenabled) Sempre use o Microsoft AutoUpdate como atualizador para Microsoft Edge
- [MSAWebSiteSSOUsingThisProfileAllowed](/DeployEdge/microsoft-edge-policies#msawebsitessousingthisprofileallowed) Permitir logon único para sites da Microsoft usando este perfil
- [OneAuthAuthenticationEnforced](/DeployEdge/microsoft-edge-policies#oneauthauthenticationenforced) Fluxo de Autenticação do OneAuth Imposto para entrada
- [PasswordGeneratorEnabled](/DeployEdge/microsoft-edge-policies#passwordgeneratorenabled) Permitir que os usuários obtenham uma sugestão de senha forte sempre que estiverem criando uma conta online
- [PrimaryPasswordSetting](/DeployEdge/microsoft-edge-policies#primarypasswordsetting) Define uma configuração que solicita que os usuários insiram a senha do dispositivo ao usar o preenchimento automático de senha
- [PrintingWebpageLayout](/DeployEdge/microsoft-edge-policies#printingwebpagelayout) Define o layout para impressão
- [RemoteDebuggingAllowed](/DeployEdge/microsoft-edge-policies#remotedebuggingallowed) Permitir depuração remota
- [RelaunchWindow](/DeployEdge/microsoft-edge-policies#relaunchwindow) Defina o intervalo de tempo para reinicialização
- [TravelAssistanceEnabled](/DeployEdge/microsoft-edge-policies#travelassistanceenabled) Habilitar assistência de viagem
- [TripleDESEnabled](/DeployEdge/microsoft-edge-policies#tripledesenabled) Habilitar conjuntos de codificação 3DES no TLS

#### <a name="deprecated-policy"></a>Política Preterida

- [LegacySameSiteCookieBehaviorEnabled](/DeployEdge/microsoft-edge-policies#legacysamesitecookiebehaviorenabled) Habilitar configuração padrão de comportamento de cookie SameSite herdado

#### <a name="obsoleted-policy"></a>Política Obsoleta

- [NewTabPageSetFeedType](/DeployEdge/microsoft-edge-policies#newtabpagesetfeedtype) Configure Microsoft Edge nova experiência de página da guia

#### <a name="additional-change"></a>Alteração Adicional

- [ConfigureShare](/DeployEdge/microsoft-edge-policies#configureshare) adicionar suporte à plataforma mac

## <a name="version-93096118-august-10"></a>Versão 93.0.961.18: 10 de agosto

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-92090262-july-29"></a>Versão 92.0.902.62: 29 de julho

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-92090255-july-21"></a>Versão 92.0.902.55: 21 de julho

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-92090245-july-12"></a>Versão 92.0.902.45: 12 de julho

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-92090240-july-6"></a>Versão 92.0.902.40: 6 de julho

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-92090222-june-21"></a>Versão 92.0.902.22: 21 de junho

### <a name="feature-updates"></a>Atualizações de recursos

- **Pesquisa de idioma natural para o histórico do navegador na barra de endereços**. Encontrar o artigo/site que você está procurando agora é mais fácil graças à pesquisa de idioma natural diretamente na barra de endereços. Você pode encontrar os resultados da pesquisa com base no conteúdo/descrição/tempo da página (como "receita de bolo da semana passada") além de títulos/palavras-chave de URL.
Observação: esta é uma Distribuição de Recursos Controlados. Se você não localizar esse recurso, volte em breve enquanto continuamos nossa distribuição.

- **Os usuários podem acessar facilmente o modo Internet Explorer no Microsoft Edge**. A partir da versão 92 do Microsoft Edge, os usuários podem recarregar um site no modo Internet Explorer no Microsoft Edge em vez de depender do aplicativo autônomo do IE 11 enquanto aguardam a configuração de um site na Lista de Sites do Modo Empresarial. Os usuários serão solicitados a adicionar o site à sua lista de sites locais de forma que a navegação para a mesma página no Microsoft Edge seja renderizada automaticamente no modo IE pelos próximos 30 dias. Você pode usar a política *[InternetExplorerIntegrationReloadInIEModeAllowed](/deployedge/microsoft-edge-policies#internetexplorerintegrationreloadiniemodeallowed)* para configurar essa experiência e permitir o acesso aos pontos de entrada do modo IE, bem como a capacidade de adicionar sites à lista de sites locais. Você pode usar a política *[InternetExplorerIntegrationLocalSiteListExpirationDays](/deployedge/microsoft-edge-policies#internetexplorerintegrationlocalsitelistexpirationdays)* para ajustar o número de dias para manter os sites na lista de sites locais.
Observe que KB5003698 ou posterior é necessário para Windows 10, versão 1909; ou KB5003690 ou posterior é necessário para Windows 10, versão 2004, Windows 10, versão 20H2 ou Windows 10, versão 21H1 para a experiência de ponta a ponta.

- **Os arquivos MHTML serão abertos por padrão no modo Internet Explorer**. A partir do Microsoft Edge versão 92 Estável, os tipos de arquivo MHTML serão abertos automaticamente no modo Internet Explorer no Microsoft Edge em vez do aplicativo Internet Explorer (IE11). Isso é mais comumente observado ao tentar visualizar emails do Outlook em um navegador. Essa alteração ocorrerá apenas se o IE11 for o manipulador padrão para este tipo de arquivo. Se preferir alterar isso, você pode fazer isso antes de instalar a atualização da versão 92 Estável usando [este guia](/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration).

- **Os instrumentos de pagamento agora são sincronizados entre dispositivos**. A partir do Microsoft Edge versão 92, você tem a opção de sincronizar suas informações de pagamento em seus dispositivos conectados.
Observação: esta é uma Distribuição de Recursos Controlados. Se você não vê este recurso, verifique em breve enquanto continuamos nossa distribuição.

- **O aviso "Desabilitar extensões do modo de desenvolvedor" pode ser descartado permanentemente**. A partir da versão 92 do Microsoft Edge, você pode desabilitar o aviso "Desabilitar extensões do modo de desenvolvedor" clicando na opção 'Não mostrar novamente'.
Observação: esta é uma Distribuição de Recursos Controlados. Se você não vê este recurso, verifique em breve enquanto continuamos nossa distribuição.

- **Gerenciar suas extensões diretamente da barra de ferramentas**. O novo menu de extensões na barra de ferramentas permitirá que você oculte/fixe extensões facilmente. Os links rápidos para gerenciar extensões e encontrar novas extensões facilitarão a localização de novas extensões e o gerenciamento das existentes.
Observação: esta é uma Distribuição de Recursos Controlados. Se você não vê este recurso, verifique em breve enquanto continuamos nossa distribuição.

- **HTTPS automático**. Os usuários terão a opção de atualizar a navegação de HTTP para HTTPS em domínios que provavelmente suportam este protocolo mais seguro. Esse suporte também pode ser configurado para tentar entrega HTTPS para todos os domínios.
Observação: estamos testando esse recurso e esse comportamento não será detectado se você tiver desativado os experimentos.

- **Melhorias na renderização de fontes**. Foram feitas melhorias na renderização do texto para melhorar a clareza e reduzir o borrão.
Observação: esta é uma Distribuição de Recursos Controlados. Se você não vê este recurso, verifique em breve enquanto continuamos nossa distribuição.

### <a name="policy-updates"></a>Atualizações de política

#### <a name="new-policies"></a>Novas políticas

Oito novas políticas foram adicionadas. Baixe os Modelos Administrativos atualizados da [página de aterrissagem do Microsoft Edge Empresa](https://www.microsoft.com/edge/business/download). Foram adicionadas as novas políticas a seguir:

- [AADWebSiteSSOUsingThisProfileEnabled](/DeployEdge/microsoft-edge-policies#aadwebsitessousingthisprofileenabled)Logon único para sites de trabalho ou escola usando este perfil habilitado.
- [AutomaticHttpsDefault](/DeployEdge/microsoft-edge-policies#automatichttpsdefault) Configurar HTTPS Automático
- [HeadlessModeEnabled](/DeployEdge/microsoft-edge-policies#headlessmodeenabled) Controle o uso do Modo Sem Periféricos
- [InsecurePrivateNetworkRequestsAllowed](/DeployEdge/microsoft-edge-policies#insecureprivatenetworkrequestsallowed) Especifica se é possível permitir que sites inseguros façam solicitações para pontos de extremidade de rede mais privados
- [InsecurePrivateNetworkRequestsAllowedForUrls](/DeployEdge/microsoft-edge-policies#insecureprivatenetworkrequestsallowedforurls) Permite que os sites listados façam solicitações para pontos de extremidade de rede mais privada a partir de contextos inseguros
- [InternetExplorerIntegrationLocalSiteListExpirationDays](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationlocalsitelistexpirationdays) Especifique o número de dias que um site permanece na lista de sites do modo IE local
- [InternetExplorerIntegrationReloadInIEModeAllowed](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationreloadiniemodeallowed) Permite que sites não configurados sejam recarregados no modo Internet Explorer
- [SharedArrayBufferUnrestrictedAccessAllowed](/DeployEdge/microsoft-edge-policies#sharedarraybufferunrestrictedaccessallowed) Especifica se SharedArrayBuffers pode ser usado em um contexto não isolado de origem cruzada

#### <a name="obsoleted-policy"></a>Política Obsoleta

- [EnableSha1ForLocalAnchors](/DeployEdge/microsoft-edge-policies#enablesha1forlocalanchors) Permitir certificados assinados usando SHA-1 quando emitidos por âncoras de confiança locais.

## <a name="version-9209029-june-8"></a>Versão 92.0.902.9: 8 de junho

Vários bugs corrigidos e problemas de desempenho.

## <a name="version-91086441-june-3"></a>Versão 91.0.864.41: 3 de junho

Vários bugs corrigidos e problemas de desempenho.

## <a name="version-91086437-may-27"></a>Versão 91.0.864.37: 27 de maio

Vários bugs corrigidos e problemas de desempenho.

## <a name="version-91086436-may-26"></a>Versão 91.0.864.36: 26 de maio

Vários bugs corrigidos e problemas de desempenho.

## <a name="version-91086433-may-21"></a>Versão 91.0.864.33: 21 de maio

Vários bugs corrigidos e problemas de desempenho.

## <a name="version-91086427-may-14"></a>Versão 91.0.864.27: 14 de maio

Vários bugs corrigidos e problemas de desempenho.

## <a name="version-91086419-may-7"></a>Versão 91.0.864.19: 7 de maio

Vários bugs corrigidos e problemas de desempenho.

## <a name="version-91086415-may-3"></a>Versão 91.0.864.15: 3 de maio

Vários bugs corrigidos e problemas de desempenho.

## <a name="version-91086411-april-30"></a>Versão 91.0.864.11: 30 de abril

### <a name="feature-updates"></a>Atualizações de recursos

- **Identifique o tráfego de rede originado dos contêineres do Microsoft Defender Application Guard no nível do proxy**. A partir da versão 91 do Microsoft Edge, há suporte integrado para marcar o tráfego de rede originado de contêineres do Application Guard, permitindo que as empresas os identifiquem e apliquem políticas específicas.

- **Opção de suporte para permitir a sincronização de favoritos do host para o contêiner do Edge Application Guard**. A partir do Microsoft Edge versão 91, os usuários têm a opção de configurar o Application Guard para sincronizar seus favoritos do host para o contêiner. Isso garante que novos favoritos também apareçam no contêiner.

- **Suporte para APIs de Reconhecimento de Fala**. A partir da versão 91 do Microsoft Edge, o suporte API para comandos de reconhecimento de voz no Google.com e sites semelhantes será adicionado. Este recurso é limitado a um grupo selecionado aleatoriamente de usuários que habilitaram a experimentação. Esses usuários estão fazendo comentários para a equipe de recursos.

- **Personalize seu navegador com novas cores de tema**. Personalize o Microsoft Edge com uma das quatorze novas cores de tema na página Configurações -> Aparência. Você também pode instalar temas personalizados do site do Complemento do Microsoft Edge. [Saber mais](https://techcommunity.microsoft.com/t5/articles/make-microsoft-edge-your-own-with-themes/m-p/2083165)

- **Interromper Downloads** A partir do Microsoft Edge versão 91, o navegador interromperá automaticamente os downloads de tipos que podem danificar seu computador se esses downloads forem iniciados sem a interação do usuário e não forem suportados pela verificação de Reputação do Aplicativo SmartScreen. Os usuários podem substituir e continuar o download clicando com o botão direito e escolhendo “Manter” no item de download. 
<!---
Enterprise administrators may opt out of this behavior one of these two policies: 

    - [ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](./deployedge/microsoft-edge-policies.md#exemptdomainfiletypepairsfromfiletypedownloadwarnings) - Disable download file type extension-based warnings for specified file types on domains --->
Para obter mais informações, consulte [Interrupções de downloads do Microsoft Edge Security](/deployedge/microsoft-edge-security-downloads-interruptions)

### <a name="policy-updates"></a>Atualizações de política

#### <a name="new-policies"></a>Novas políticas

Seis novas políticas foram adicionadas. Baixe os Modelos Administrativos atualizados da [página de aterrissagem do Microsoft Edge Empresa](https://www.microsoft.com/edge/business/download). Foram adicionadas as novas políticas a seguir:

- [ApplicationGuardTrafficIdentificationEnabled](/DeployEdge/microsoft-edge-policies#applicationguardtrafficidentificationenabled) - Identificação de Tráfego do Application Guard
- [ExplicitlyAllowedNetworkPorts](/DeployEdge/microsoft-edge-policies#explicitlyallowednetworkports) - Portas de rede explicitamente permitidas
- [ImportStartupPageSettings](/DeployEdge/microsoft-edge-policies#importstartuppagesettings) - Permitir a importação das configurações da página de inicialização
- [MathSolverEnabled](/DeployEdge/microsoft-edge-policies#mathsolverenabled) - Permite que os usuários capturem um problema de matemática e obtenham a solução com uma explicação passo a passo no Microsoft Edge
- [NewTabPageContentEnabled](/DeployEdge/microsoft-edge-policies#newtabpagecontentenabled) - Permitir conteúdo do Microsoft News na página nova guia
- [NewTabPageQuickLinksEnabled](/DeployEdge/microsoft-edge-policies#newtabpagequicklinksenabled) - Permitir links rápidos na página nova guia

#### <a name="obsoleted-policy"></a>Política Obsoleta

- [ProactiveAuthEnabled](./microsoft-edge-policies.md#proactiveauthenabled) - Habilitar Autenticação Proativa
<!-- end major 91 -->

## <a name="version-90081846-april-22"></a>Versão 90.0.818.46: 22 de abril

Vários bugs corrigidos e problemas de desempenho.

## <a name="version-90081842-april-20"></a>Versão 90.0.818.42: 20 de abril

Vários bugs corrigidos e problemas de desempenho.

## <a name="version-90081841-april-16"></a>Versão 90.0.818.41: 16 de abril

Vários bugs corrigidos e problemas de desempenho.

## <a name="version-90081838-april-14"></a>Versão 90.0.818.38: 14 de abril

Vários bugs corrigidos e problemas de desempenho.

## <a name="version-90081836-april-12"></a>Versão 90.0.818.36: 12 de abril

Vários bugs corrigidos e problemas de desempenho.

## <a name="version-90081827-april-2"></a>Versão 90.0.818.27: 2 de abril

Vários bugs corrigidos e problemas de desempenho.

## <a name="version-90081822-march-29"></a>Versão 90.0.818.22: 29 de março

Vários bugs corrigidos e problemas de desempenho.

## <a name="version-90081814-march-22"></a>Versão 90.0.818.14: 22 de março

Correção de vários bugs e problemas de desempenho.
<!-- begin major 90 -->
## <a name="version-9008188-march-16"></a>Versão 90.0.818.8: 16 de março

### <a name="feature-updates"></a>Atualizações de recursos

- **O Logon Único (SSO) agora está disponível para contas do Azure Active Directory (Azure AD) e conta Microsoft (MSA) no macOS**. Um usuário conectado no Microsoft Edge em macOS agora terá automaticamente acesso aos sites que estão configurados para permitir logon único com as contas Microsoft e Corporativas (por exemplo, bing.com, office.com, msn.com e outlook.com).

- **Modo de quiosque.** A partir do Microsoft Edge versão 90, bloqueamos as configurações de impressão da interface do usuário para permitir apenas as impressoras configuradas e as opções “Imprimir em PDF”. Também fizemos melhorias no modo quiosque de aplicativo único de acesso atribuído para restringir a inicialização de outros aplicativos a partir do navegador. Para obter mais informações sobre os recursos do modo quiosque, clique [aqui](/deployedge/microsoft-edge-configure-kiosk-mode#kiosk-mode-supported-features).

- **Impressão:**

  - **Novo modo de rasterização de impressão para impressoras não PostScript**. A partir da versão 90 do Microsoft Edge, os administradores poderão usar uma nova política para definir o modo de rasterização de impressão para seus usuários. Esta política  controla como o Microsoft Edge imprime para impressoras não PostScript no Windows.  Às vezes, os trabalhos de impressão em impressoras não PostScript precisam ser rasterizados para serem impressos corretamente. As opções de impressão são Completa e Rápida.

  - **Opções adicionais de dimensionamento de página para impressão**. Os usuários agora podem personalizar o dimensionamento enquanto imprimem páginas da Web e documentos PDF usando as opções adicionais. A opção "Ajustar à página" garante que a página da Web ou o documento se ajuste ao espaço disponível no "Tamanho do papel" selecionado para impressão. A opção "Tamanho real" garante que não ocorram mudanças no tamanho do conteúdo que está sendo impresso, independentemente do "Tamanho do papel" selecionado.

- **Produtividade:**

  - **As sugestões de preenchimento automático são estendidas para incluir o conteúdo dos campos de endereço da área de transferência**. O conteúdo da área de transferência é analisado quando você clica em um campo de perfil/endereço (por exemplo, telefone, email, CEP, cidade, estado, etc.) para mostrar como sugestões de preenchimento automático.

  - **Os usuários podem pesquisar sugestões de preenchimento automático mesmo se um formulário ou campo não for detectado**. Hoje, se você tiver suas informações salvas no Microsoft Edge, as sugestões de preenchimento automático aparecem automaticamente e ajudam você a economizar tempo enquanto preenche formulários. Nos casos em que o preenchimento automático perde um formulário ou se você deseja buscar dados em formulários que normalmente não possuem preenchimento automático (como formulários temporários), você pode pesquisar suas informações usando o preenchimento automático.

- **Acesse downloads a partir de um submenu na barra de menu**. Os downloads aparecerão no canto superior direito com todos os downloads ativos em um só lugar. Este menu é facilmente descartável para que os usuários possam continuar navegando ininterruptamente e possam monitorar o progresso geral do download diretamente da barra de ferramentas. [Saiba mais](https://techcommunity.microsoft.com/t5/articles/introducing-the-new-downloads-experience/m-p/2111551).


### <a name="policy-updates"></a>Atualizações de política

#### <a name="new-policies"></a>Novas políticas

Sete novas políticas foram adicionadas. Baixe os modelos administrativos atualizados da [página de aterrissagem do Microsoft Edge Enterprise](https://www.microsoft.com/edge/business/download). Foram adicionadas as novas políticas a seguir:

- [ApplicationGuardFavoritesSyncEnabled](./microsoft-edge-policies.md#applicationguardfavoritessyncenabled) - Habilitada a Sincronização de Favoritos do Application Guard
- [ManagedConfigurationPerOrigin](./microsoft-edge-policies.md#managedconfigurationperorigin) - Define valores de configuração gerenciada para sites de origens específicas
- [PrintRasterizationMode](./microsoft-edge-policies.md#printrasterizationmode) - Modo de Rasterização de Impressão
- [QuickViewOfficeFilesEnabled](./microsoft-edge-policies.md#quickviewofficefilesenabled) - Gerenciar a capacidade de Visualização Rápida de arquivos do Office no Microsoft Edge
- [SSLErrorOverrideAllowedForOrigins](./microsoft-edge-policies.md#sslerroroverrideallowedfororigins) - Permitir que os usuários prossigam a partir da página de aviso HTTPS para origens específicas
- [WindowOcclusionEnabled](./microsoft-edge-policies.md#windowocclusionenabled) - Habilitar Oclusão de Janela
- [WindowsHelloForHTTPAuthEnabled](./microsoft-edge-policies.md#windowshelloforhttpauthenabled) - Windows Hello habilitado para autenticação HTTP

#### <a name="deprecated-policies"></a>Políticas preteridas

- [NativeWindowOcclusionEnabled](./microsoft-edge-policies.md#nativewindowocclusionenabled) - Habilitar Oclusão de Janela Nativa
- [SSLVersionMin](./microsoft-edge-policies.md#sslversionmin)- Versão mínima do TLS habilitada
<!-- end major 90 -->

## <a name="version-89077454-march-13"></a>Versão 89.0.774.54: 13 de março

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-89077450-march-10"></a>Versão 89.0.774.50: 10 de março

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-89077448-march-8"></a>Versão 89.0.774.48: 8 de março

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-89077445-march-3"></a>Versão 89.0.774.45: 3 de março

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-89077439-february-26"></a>Versão 89.0.774.39: 26 de fevereiro

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-89077434-february-22"></a>Versão 89.0.774.34: 22 de fevereiro

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-89077427-february-12"></a>Versão 89.0.774.27: 12 de fevereiro

Correção de vários bugs e problemas de desempenho.

## <a name="version-89077423-february-8"></a>Versão 89.0.774.23: 8 de fevereiro

Correção de vários bugs e problemas de desempenho.

## <a name="version-89077418-february-3"></a>Versão 89.0.774.18: 3 de fevereiro

### <a name="feature-updates"></a>Atualizações de recursos

- **O modo quiosque permite recursos adicionais de bloqueio**. A partir da versão 89 do Microsoft Edge, adicionamos funcionalidades adicionais de bloqueio no modo de quiosque para permitir que os clientes executem as tarefas em uma experiência mais produtiva e segura. [Saiba mais](microsoft-edge-configure-kiosk-mode.md#kiosk-mode-supported-features).

- **A ferramenta Enterprise Mode Site List Manager estará disponível no navegador através da página do *edge://compat* **. Você pode usar esta ferramenta para criar, editar e exportar o XML da lista de sites para o modo Internet Explorer no Microsoft Edge. Você pode habilitar o acesso a esta ferramenta conforme necessário por meio da política de grupo. [Saiba Mais](./edge-ie-mode-site-list-manager.md).

- **Melhore o desempenho do navegador com guias de suspensão**. As guias em suspensão aprimoram o desempenho do navegador colocando as guias inativas em suspensão para liberar recursos do sistema, como memória e CPU, para que as guias ativas ou outros aplicativos possam usá-las. Os usuários podem impedir que os sites entrem em suspensão e configurem o período de tempo antes de uma Tabulação inativa entrar em suspensão. Para manter os usuários em seu fluxo, há também a [heurística](https://techcommunity.microsoft.com/t5/articles/sleeping-tabs-faq/m-p/1705434) para evitar que certos sites entre em modo de suspensão, como sites intranet. Esse recurso pode ser gerenciado com políticas de grupo.

  > [!NOTE]
  > "Melhorar o desempenho do navegador com guias de suspensão" é uma atualização para as notas de lançamento de 3 de fevereiro para a versão principal 89.0.774.18.

- **Redefinir manualmente seus dados de sincronização do Microsoft Edge na nuvem**. Introduziremos uma maneira de redefinir os seus dados de sincronização do Microsoft Edge dentro do produto. Isso garante que os seus dados sejam removidos dos serviços Microsoft, além de resolver certos problemas de produto que exigiam um tíquete de suporte.

- **Melhorias na experiência de seleção de texto em documentos PDF**. Os usuários começarão a ter uma experiência de seleção de texto mais uniforme e consistente em documentos PDF abertos no Microsoft Edge a partir da versão 89.

- **O campo de data de nascimento agora é compatível com o preenchimento automático**. Hoje, o Microsoft Edge ajuda você a economizar tempo e esforço ao preencher formulários e criar contas online, preenchendo automaticamente seus dados como endereços, nomes, números de telefone, etc. A partir da versão 89 do Microsoft Edge, estamos adicionando suporte para outro campo que você pode ter salvar e preencher automaticamente: a data de nascimento. Você pode exibir, editar e excluir essas informações a qualquer momento nas configurações do seu perfil.

- **Suporte para pesquisa com linguagem natural na barra de endereços, página de pesquisa do histórico e no hub de histórico**. A partir da versão 89 do Microsoft Edge, encontrar um artigo/site será mais fácil com a pesquisa em idioma natural na barra de endereços, na página do histórico e no hub de histórico. Os usuários podem pesquisar pelo conteúdo/descrição/tempo de uma página exibidos anteriormente (tal como "receita de bolo da semana passada"), além de correspondências de títulos/palavras-chave de URL. Este recurso é limitado a um grupo selecionado aleatoriamente de usuários que ativaram a experimentação. Esses usuários estão fazendo comentários para a equipe de recursos.

### <a name="policy-updates"></a>Atualizações de política

#### <a name="new-policies"></a>Novas políticas

- [BrowsingDataLifetime](./microsoft-edge-policies.md#browsingdatalifetime) - Configurações de Tempo de Vida de Dados de Navegação
- [MAMEnabled](./microsoft-edge-policies.md#mamenabled) - Gerenciamento de Aplicativos Móveis Habilitado
- [DefinePreferredLanguages](./microsoft-edge-policies.md#definepreferredlanguages) - Define uma lista ordenada de idiomas preferidos em que os sites devem ser exibidos se o site oferecer suporte
- [ShowRecommendationsEnabled](./microsoft-edge-policies.md#showrecommendationsenabled) - Permite recomendações e notificações promocionais do Microsoft Edge
- [PrintingAllowedBackgroundGraphicsModes](./microsoft-edge-policies.md#printingallowedbackgroundgraphicsmodes) - Restringe o modo de impressão de elementos gráficos de plano de fundo
- [PrintingBackgroundGraphicsDefault](./microsoft-edge-policies.md#printingbackgroundgraphicsdefault)- Modo padrão de impressão de elementos gráficos de plano de fundo
- [SmartActionsBlockList](./microsoft-edge-policies.md#smartactionsblocklist)- Bloqueia ações inteligentes para uma lista de serviços

#### <a name="obsoleted-policies"></a>Políticas obsoletas

- [ForceLegacyDefaultReferrerPolicy](./microsoft-edge-policies.md#forcelegacydefaultreferrerpolicy) - Usa uma política referencial padrão de no-referrer-when-downgrade
- [MetricsReportingEnabled](./microsoft-edge-policies.md#metricsreportingenabled) - Habilita o uso e os relatórios de dados relacionados a falhas
- [SendSiteInfoToImproveServices](./microsoft-edge-policies.md#sendsiteinfotoimproveservices) - Envia informações do site para melhorar os serviços da Microsoft
<!-- end major 89 -->

## <a name="version-88070556-january-29"></a>Versão 88.0.705.56: 29 de janeiro

Correção de vários bugs e problemas de desempenho.

## <a name="version-88070549-january-20"></a>Versão beta 88.0.705.49: 20 de janeiro

Correção de vários bugs e problemas de desempenho.

## <a name="version-88070545-january-15"></a>Versão 88.0.705.45: 15 de janeiro

Correção de vários bugs e problemas de desempenho.

## <a name="version-88070541-january-11"></a>Versão 88.0.705.41: 11 de janeiro

Correção de vários bugs e problemas de desempenho.

## <a name="version-88070529-december-21"></a>Versão 88.0.705.29: 21 de dezembro

Correção de vários bugs e problemas de desempenho.

<!-- begin major 88 -->
## <a name="version-88070518-december-9"></a>Versão 88.0.705.18: 9 de dezembro

### <a name="feature-updates"></a>Atualizações de recursos

- **Preteridos:**

  - Preterir o suporte para o protocolo FTP. O suporte para o protocolo de FTP herdado foi removido do Microsoft Edge. Tentar navegar para um link de FTP fará com que o navegador direcione o sistema operacional para abrir um aplicativo externo para manipular o link de FTP. Como alternativa, os administradores de TI podem configurar o Microsoft Edge para usar o modo IE para sites que dependem do protocolo FTP.
  - O suporte ao Adobe Flash será removido. A partir do Microsoft Edge beta versão 88, a funcionalidade e o suporte do Adobe Flash serão removidos. Saiba mais: [Atualização no fim do suporte do Adobe Flash Player - blog do Microsoft Edge (Windows.com)](https://blogs.windows.com/msedgedev/2020/09/04/update-adobe-flash-end-support/)

- **Autenticação:**

  - O logon único (SSO) agora está disponível para contas do Azure Active Directory (Azure AD) e para a conta Microsoft (MSA) em Windows MacOS e de nível inferior. Um usuário conectado no Microsoft Edge no Windows Microsoft MacOS ou no nível inferior do Microsoft Windows (7, 8.1) agora será automaticamente conectado aos sites que estiverem configurados para permitir logon único com contas Work e Microsoft (por exemplo, bing.com, office.com, msn.com, outlook.com).<br>Observação: um usuário pode ter que sair e entrar novamente se ele se conectar ao Microsoft Edge em uma versão anterior ao Microsoft Edge 88 para aproveitar esse recurso.
  - Alternar automaticamente os usuários do MacOS para o perfil de trabalho dos sites que se autenticam com a conta corporativa. A partir da versão 88 do Microsoft Edge, oferecemos a capacidade de alternar os sites que se autenticam com o perfil de trabalho do usuário no MacOS.<br>Observação: um usuário pode ter que sair e entrar novamente se ele se conectar ao Microsoft Edge em uma versão anterior ao Microsoft Edge 88 para aproveitar esse recurso.

- **Opção de modo de quiosque para encerrar a sessão**. O botão "Encerrar sessão" agora está disponível em uma experiência de navegação pública do modo de quiosque. Esse recurso garante que os dados e as configurações do navegador sejam excluídos quando o Microsoft Edge estiver fechado. Saiba mais sobre os recursos do modo de quiosque e o roteiro, [Configurar o modo de quiosque do Microsoft Edge](./microsoft-edge-configure-kiosk-mode.md).

- **Segurança e privacidade:**

  - Alertas são gerados se a senha de um usuário for encontrada em um vazamento online. As senhas do usuário são verificadas em um repositório de credenciais violadas e envia ao usuário um alerta se uma correspondência for encontrada. Para garantir a segurança e a privacidade, as senhas dos usuários são criptografadas e criptografadas quando são verificadas no banco de dados de credenciais vazadas.
  - Atualizar conteúdo misto automaticamente. As páginas seguras fornecidas por HTTPS podem conter imagens de referência que são servidas por HTTP não seguro. Para melhorar a privacidade e a segurança no Microsoft Edge 88, essas imagens serão recuperadas por HTTPS. Se a imagem não estiver disponível em HTTPS, ela não será carregada.
  - Exiba as permissões do site por site e por atividades recentes. Começando com o Microsoft Edge 88, os usuários poderão gerenciar permissões do site com mais facilidade. Elas poderão exibir permissões por site da Web, em vez do tipo de permissão apenas. Além disso, adicionamos uma seção de atividade recente que mostrará a um usuário todas as alterações recentes nas permissões do site.
  - Controles avançados para os cookies do navegador. A partir do Microsoft Edge 88, os usuários podem excluir cookies de terceiros sem afetar os cookies dos primeiros participantes. Os usuários também poderão filtrar os cookies por nome ou terceiro e classificar por nome, número de cookies e a quantidade de dados armazenados e modificados pela última vez.

- **Desempenho:**

  - Melhorar o desempenho do navegador com guias em suspensão. As guias em suspensão aprimoram o desempenho do navegador colocando as guias inativas em suspensão para liberar recursos do sistema, como memória e CPU, para que as guias ativas ou outros aplicativos possam usá-las. Os usuários podem impedir que os sites entrem em suspensão e configurem o período de tempo antes de uma Tabulação inativa entrar em suspensão. Para manter os usuários em fluxo, há também heurística para impedir que determinados sites entrem em suspensão, como sites de intranet. Este recurso é limitado a um grupo selecionado aleatoriamente de usuários que ativaram a experimentação. Estamos planejando ter o recurso de guias de suspensão habilitado por padrão no Microsoft Edge versão 89. Esse recurso pode ser gerenciado com políticas de grupo.
  - Melhorar a velocidade de inicialização do Microsoft Edge com o início rápido. Para melhorar a velocidade de inicialização do Microsoft Edge, desenvolvemos um recurso chamado início rápido. O início rápido abre o Microsoft Edge mais rapidamente, permitindo que o Microsoft Edge seja executado em segundo plano. Observação: esse recurso está limitado a um grupo de usuários selecionado aleatoriamente que habilitou o experimento. Esses usuários estão fazendo comentários para a equipe de recursos.

- **Produtividade:**

  - Melhorar a produtividade e várias tarefas com guias verticais. À medida que o número de guias horizontais aumenta, os títulos de sites começam a ser cortados e os controles de guia são perdidos quando cada guia é reduzida. Isso interrompe o fluxo de trabalho do usuário à medida que passa mais tempo encontrando, trocando e gerenciando suas guias e menos tempo na tarefa em questão. As guias verticais permitem que os usuários movam suas guias para a lateral, onde ícones alinhados verticalmente e títulos de sites mais longos facilitam verificação, identificação e alternância rápidas para a guia que elas desejam abrir.
  - Preenchimento automático do campo data do nascimento. O Microsoft Edge já ajuda a poupar tempo e esforço ao preencher formulários e criar contas online por meio do preenchimento automático de dados do usuário, como endereços, nomes, números de telefone, etc. O Microsoft Edge agora oferece suporte ao campo data de nascimento que os usuários podem salvar e preencher automaticamente. Um usuário pode exibir, editar e excluir essas informações a qualquer momento em suas configurações de perfil.
  - Melhorias em Fechadas recentemente no Histórico. Fechadas recentemente agora mantém as últimas 25 guias e janelas em qualquer sessão de navegação anterior, em vez de apenas na sessão anterior. Os usuários podem selecionar Fechadas recentemente na nova experiência do Histórico para ver todas as guias que estavam abertas.
  - Recurso “Seu dia resumido” habilitado por padrão. A partir do Microsoft Edge versão 88, os profissionais da informação podem se beneficiar dos recursos de produtividade inteligentes em sua página Nova guia (NTP). Oferecemos aos usuários conectados com sua conta de estudante ou corporativa conteúdo personalizado e relevante desenvolvido por seu gráfico M365. Os usuários podem examinar rapidamente seus módulos “Seu dia num relance” para rastrear facilmente suas reuniões e trabalhos recentes, bem como iniciar rapidamente os aplicativos que desejam usar.

- **PDF:**

  - Exibição de documento em PDF no modo de exibição de livro (duas páginas). A partir da versão 88 do Microsoft Edge, os usuários podem exibir documentos em PDF em uma única página ou no modo de exibição de duas páginas. Para alterar o modo de exibição, clique no botão **Modo de exibição de página** na barra de ferramentas.
  - Suporte a notas de texto ancoradas para arquivos PDF. A partir da versão 87 do Microsoft Edge, os usuários podem adicionar anotações de texto digitadas em qualquer parte do texto em arquivos PDF.
  - Experiência de seleção de texto uniforme em documentos PDF. Os usuários terão uma experiência de seleção de texto uniforme e consistente em documentos PDF abertos no Microsoft Edge.
  - Exibir páginas da Web salvas como arquivos PDF na barra de downloads. Agora os usuários podem exibir os arquivos PDF gerados configurando "Salvar como PDF" como o destino da impressora para páginas da Web na barra de downloads.

- **Fontes:**

  - Os ícones do navegador são atualizados para o sistema de design Fluent. Como parte do nosso trabalho contínuo em relação ao design Fluent no navegador, fizemos alterações para alinhar os ícones ao novo sistema de ícones da Microsoft. Essas mudanças afetarão muitas das nossas interfaces de usuário de alto toque, incluindo guias, barra de endereços, bem como ícones de navegação e ícones de orientação encontrados em nossos vários menus.
  - Renderização de fonte aprimorada. A renderização de texto é melhorada para melhorar a clareza e reduzir o desfoque.

### <a name="policy-updates"></a>Atualizações de política

#### <a name="new-policies"></a>Novas políticas

Dezesseis novas políticas foram adicionadas. Baixe os modelos administrativos atualizados da [página inicial do Microsoft Edge Enterprise](https://www.microsoft.com/edge/business/download). As novas políticas a seguir foram adicionadas.

- [BlockExternalExtensions](./microsoft-edge-policies.md#blockexternalextensions) - bloqueia a instalação de extensões externas.
- [InternetExplorerIntegrationLocalFileAllowed](./microsoft-edge-policies.md#internetexplorerintegrationlocalfileallowed) - permite a inicialização de arquivos locais no modo Internet Explorer.
- [InternetExplorerIntegrationLocalFileExtensionAllowList](./microsoft-edge-policies.md#internetexplorerintegrationlocalfileextensionallowlist) - abre arquivos locais na lista de permissões de extensão de arquivo do modo Internet Explorer.
- [InternetExplorerIntegrationLocalFileShowContextMenu](./microsoft-edge-policies.md#internetexplorerintegrationlocalfileshowcontextmenu) - exibe o menu de contexto para abrir um link no modo do Internet Explorer.
- [IntranetRedirectBehavior](./microsoft-edge-policies.md#intranetredirectbehavior) - comportamento de redirecionamento da intranet.
- [PrinterTypeDenyList](./microsoft-edge-policies.md#printertypedenylist) - desativa tipos de impressora na lista de negações.
- [ShowMicrosoftRewards](./microsoft-edge-policies.md#showmicrosoftrewards) - exibe experiências de recompensas da Microsoft.
- [SleepingTabsEnabled](./microsoft-edge-policies.md#sleepingtabsenabled) - configura Guias em suspensão.
- [SleepingTabsTimeout](./microsoft-edge-policies.md#sleepingtabstimeout) - define o tempo limite de inatividade da guia plano de fundo para Guias em suspensão.
- [SleepingTabsBlockedForUrls](./microsoft-edge-policies.md#sleepingtabsblockedforurls) - bloqueia Guias em suspensão em sites específicos.
- [StartupBoostEnabled](./microsoft-edge-policies.md#startupboostenabled) - habilita o início rápido.
- [UpdatePolicyOverride](./microsoft-edge-policies.md#updatepolicyoverride) - especifica como o Microsoft Edge Update manipula as atualizações disponíveis do Microsoft Edge.
- [VerticalTabsAllowed](./microsoft-edge-policies.md#verticaltabsallowed) - configura a disponibilidade de um layout vertical para guias na lateral do navegador.
- [WebRtcAllowLegacyTLSProtocols](./microsoft-edge-policies.md#webrtcallowlegacytlsprotocols) - Permite fazer downgrade TLS/DTLS legado em WebRTC.

#### <a name="deprecated-policies"></a>Políticas preteridas

As políticas a seguir estão preteridas.

- [ProactiveAuthEnabled](./microsoft-edge-policies.md#proactiveauthenabled) – habilita a autenticação pró-ativa.
- [ProxyBypassList](./microsoft-edge-policies.md#proxybypasslist) - configura regras de bypass de proxy.
- [Proxymode](./microsoft-edge-policies.md#proxymode) - define configurações de servidor proxy.
- [ProxyPacUrl](./microsoft-edge-policies.md#proxypacurl) - define a URL do arquivo proxy.pac.
- [ProxyServer](./microsoft-edge-policies.md#proxyserver) - configura o endereço ou URL do servidor proxy.
- [WebDriverOverridesIncompatiblePolicies](./microsoft-edge-policies.md#webdriveroverridesincompatiblepolicies) - permite que o WebDriver substitua políticas incompatíveis.

#### <a name="obsoleted-policies"></a>Políticas obsoletas

As políticas a seguir estão obsoletas.

- [DefaultPluginsSetting](./microsoft-edge-policies.md#defaultpluginssetting) - configuração padrão do Adobe Flash.
- [PluginsAllowedForUrls](./microsoft-edge-policies.md#pluginsallowedforurls) - permite o plug-in do Adobe Flash em sites específicos.
- [PluginsBlockedForUrls](./microsoft-edge-policies.md#pluginsblockedforurls) - bloqueia o plug-in do Adobe Flash em sites específicos.
- [RunAllFlashInAllowMode](./microsoft-edge-policies.md#runallflashinallowmode) - estende a configuração do Adobe Flash Content para todo o conteúdo.

<!-- end major 88 -->

## <a name="version-87066455-december-3"></a>Versão 87.0.664.55: 3 de dezembro

Correção de vários bugs e problemas de desempenho. O novo recurso a seguir é compatível com esta versão.

- Alertas **são gerados se a senha de um usuário for encontrada em um vazamento online**. As senhas do usuário são verificadas em um repositório de credenciais violadas e envia ao usuário um alerta se uma correspondência for encontrada. Para garantir a segurança e a privacidade, as senhas dos usuários são criptografadas e criptografadas quando são verificadas no banco de dados de credenciais vazadas.

## <a name="version-87066452-november-30"></a>Versão 87.0.664.52: 30 de novembro

Correção de vários bugs e problemas de desempenho.

## <a name="version-87066440-november-18"></a>Versão 87.0.664.40: 18 de novembro

Correção de vários bugs e problemas de desempenho.

## <a name="version-87066436-november-16"></a>Versão 87.0.664.36: 16 de novembro

Correção de vários bugs e problemas de desempenho.

## <a name="version-87066430-november-9"></a>Versão 87.0.664.30: 9 de novembro

Correção de vários bugs e problemas de desempenho.

## <a name="version-87066424-november-2"></a>Versão 87.0.664.24: 2 de novembro

Correção de vários bugs e problemas de desempenho.

## <a name="version-87066418-october-26"></a>Versão 87.0.664.18: 26 de outubro

Correção de vários bugs e problemas de desempenho.

<!-- begin major 87 -->
## <a name="version-87066412-october-20"></a>Versão 87.0.664.12: 20 de outubro

### <a name="feature-updates"></a>Atualizações de recursos

- **Recursos de privacidade do modo de quiosque habilitados**. A partir do Microsoft Edge versão 87, os recursos do modo de quiosque que ajudarão as empresas em torno da privacidade dos dados do usuário serão habilitados. Esses recursos habilitarão experiências, como limpar os dados do usuário ao sair, excluir arquivos baixados e redefinir a experiência de iniciação configurada após uma quantidade específica de tempo ocioso. Saiba mais sobre como [Configurar as opções do modo de quiosque do Microsoft Edge](./microsoft-edge-configure-kiosk-mode.md)
- **Implantação de ClickOnce habilitada por padrão**. O ClickOnce está habilitado por padrão no Microsoft Edge 87, o que reduz as barreiras para a implantação de software e alinha-se melhor com o comportamento do navegador da Versão Prévia do Microsoft Edge. A partir do Microsoft Edge 87, o estado "Não Configurado" da política de ClickOnceEnabled refletirá o novo estado de ClickOnce padrão Habilitado (em comparação com o estado padrão anterior Desabilitado).
- **A página nova guia da empresa (NTP) integra a produtividade com o conteúdo do feed personalizado e relevante para o trabalho**. O NTP empresarial combina a página de produtividade do Office 365 oferecemos a todos os usuários que entraram com uma conta corporativa ou de estudante com feeds personalizados da empresa e da indústria relevantes para o trabalho que são organizados em uma única página. Os usuários poderão reconhecer o conteúdo familiar do Office 365 e da Pesquisa da Microsoft para Empresas, da plataforma Bing. Além disso, eles podem facilmente inverter para um "Meu Feed" personalizável com conteúdo e módulos relevantes para o usuário, para a empresa ou para a sua indústria, além de uma seleção de outros feeds disponibilizados pela organização. [Saiba mais](/microsoft-365/admin/manage/manage-industry-news?preserve-view=true&view=o365-worldwide).

- **Segurança e privacidade:**

  - Suporte a Associação de Token TLS para sites de política configurada. A associação de Token TLS ajuda a evitar ataques de roubo de token para garantir que os cookies não possam ser reutilizados a partir de um dispositivo que não tenha sido definido inicialmente. O uso da ligação de token TLS exige a configuração da política [AllowTokenBindingForUrls](./microsoft-edge-policies.md#allowtokenbindingforurls) e exige que os sites listados ofereçam suporte a esse recurso.

- **Suporte a teclado para marca-texto em arquivos PDF**. Os usuários podem usar as teclas do teclado para realçar qualquer texto em um PDF.

- **Impressão:**

  - Escolha o lado a ser invertido ao imprimir nos dois lados. Os usuários podem optar por virar o lado maior ou o lado menor de uma planilha ao imprimir em ambos os lados.
  - Escolha o modo de rasterização de impressão para a empresa. Controlar como o Microsoft Edge é impresso em uma impressora não PostScript no Windows. Às vezes, os trabalhos de impressão em impressoras não PostScript precisam ser rasterizados para serem impressos corretamente. As opções de impressão são "Total" e "Rápida".

### <a name="policy-updates"></a>Atualizações de política

#### <a name="new-policies"></a>Novas políticas

Dez novas políticas foram adicionadas. Baixe os modelos administrativos atualizados da [página inicial do Microsoft Edge Enterprise](https://www.microsoft.com/edge/business/download). As novas políticas a seguir foram adicionadas.

- [ConfigureFriendlyURLFormat](./microsoft-edge-policies.md#configurefriendlyurlformat) -configure o formato de colagem padrão das URLs copiadas do Microsoft Edge e determine se outros formatos estarão disponíveis para os usuários.
- [EdgeShoppingAssistantEnabled](./microsoft-edge-policies.md#edgeshoppingassistantenabled) -Compras Habilitadas no Microsoft Edge.
- [HideInternetExplorerRedirectUXForIncompatibleSitesEnabled](./microsoft-edge-policies.md#hideinternetexplorerredirectuxforincompatiblesitesenabled) – oculte o diálogo de redirecionamento único e a faixa no Microsoft Edge.
- [KioskAddressBarEditingEnabled](./microsoft-edge-policies.md#kioskaddressbareditingenabled) -configure a edição da barra de endereços para a experiência de navegação pública do modo de quiosque.
- [KioskDeleteDownloadsOnExit](./microsoft-edge-policies.md#kioskdeletedownloadsonexit) - exclua arquivos baixados como parte de uma sessão quiosque quando o Microsoft Edge é fechado.
- [PasswordRevealEnabled](./microsoft-edge-policies.md#passwordrevealenabled) -habilite o botão revelar Senha.
- [RedirectSitesFromInternetExplorerPreventBHOInstall](./microsoft-edge-policies.md#redirectsitesfrominternetexplorerpreventbhoinstall) – impede a instalação do BHO para redirecionar sites incompatíveis do Internet Explorer para o Microsoft Edge.
- [RedirectSitesFromInternetExplorerRedirectMode](./microsoft-edge-policies.md#redirectsitesfrominternetexplorerredirectmode) – redirecione sites incompatíveis do Internet Explorer para o Microsoft Edge.
- [SpeechRecognitionEnabled](./microsoft-edge-policies.md#speechrecognitionenabled) - Configurar Reconhecimento de Fala.
- [WebCaptureEnabled](./microsoft-edge-policies.md#webcaptureenabled) -habilite o recurso de captura da Web no Microsoft Edge.

#### <a name="deprecated-policy"></a>Política Preterida

[NewTabPageSetFeedType](./microsoft-edge-policies.md#newtabpagesetfeedtype) - configurar a nova experiência de página da guia Microsoft Edge.

#### <a name="obsoleted-policy"></a>Política obsoleta

[EnableDeprecatedWebPlatformFeatures](./microsoft-edge-policies.md#enabledeprecatedwebplatformfeatures) - reative os recursos da plataforma Web preteridos por um tempo limitado.

<!-- end major 87 -->

## <a name="version-86062243-october-16"></a>Versão 86.0.622.43: 16 de outubro

Correção de vários bugs e problemas de desempenho.

## <a name="version-86062236-october-7"></a>Versão 86.0.622.36: 7 de outubro

Correção de vários bugs e problemas de desempenho.

## <a name="version-86062231-october-1"></a>Versão 86.0.622.31: 1 de outubro

Correção de vários bugs e problemas de desempenho.

## <a name="version-86062228-september-28"></a>Versão 86.0.622.28: 28 de setembro

Correção de vários bugs e problemas de desempenho.

## <a name="version-86062215-september-14"></a>Versão 86.0.622.15: 14 de setembro

Correção de vários bugs e problemas de desempenho.
<!-- major 86 -->
## <a name="version-86062211-september-9"></a>Versão 86.0.622.11: 9 de setembro

### <a name="feature-updates"></a>Atualizações de recursos

* **Modo Internet Explorer:**

   * Permita que os usuários usem a interface do usuário (UI) do Microsoft Edge para testar sites no modo Internet Explorer. A partir da versão 86 do Microsoft Edge, os administradores poderão habilitar uma opção da interface do usuário para seus usuários para carregar uma guia no modo Internet Explorer para fins de teste ou como um stopgap até que os sites sejam adicionados ao XML da lista de sites.

* **Excluir downloads do disco usando o gerenciador de downloads.** Agora, os usuários podem excluir os arquivos baixados de seu disco, sem sair do navegador. A nova funcionalidade Excluir downloads existe no menu de contexto da prateleira de downloads ou da página de downloads.

* **Reverter para a versão anterior do Microsoft Edge.** O recurso reversão permite que os administradores voltem para uma versão boa conhecida do Microsoft Edge, caso haja algum problema na versão mais recente do Microsoft Edge.
[Saiba mais](edge-learnmore-rollback.md).

* **Forçar a habilitação da Sincronização por padrão em toda a empresa.**  Os administradores podem habilitar a sincronização das contas do Azure Active Directory (Azure AD) por padrão com a política de [ForceSync](./microsoft-edge-policies.md#forcesync).

* **Atualizações de PDF:**

  * Sumário para documentos em PDF. A partir da versão 86, o Microsoft Edge terá suporte ao sumário, o que permitirá que os usuários naveguem com facilidade por um documento em PDF.
  * Acesse todas as funcionalidades de PDF em telas pequenas de fator forma. Acesse todos os recursos do leitor de PDF do Microsoft Edge em dispositivos com telas pequenas.
  * Suporte à caneta digital para marca-texto em arquivos PDF. Com essa atualização, os usuários podem usar a caneta digital para realçar o texto diretamente em arquivos PDF, da mesma forma que uma marca-texto física realçaria o papel.
  * Rolagem aperfeiçoada de PDF. Agora, você poderá experimentar a rolagem livre de travamentos ao navegar por documentos em PDF grandes.

* **Mudança de perfil automática no Windows 7, 8 e 8.1.** A mudança de perfil automática disponível atualmente no Microsoft Edge no Windows 10 foi estendida para versões inferiores do Windows (Windows 7, 8 e 8.1). Para saber mais, confira a postagem de blog [mudança de perfil automática](https://blogs.windows.com/msedgedev/2020/04/30/automatic-profile-switching/).

* **Os usuários verão sugestões de preenchimento automático quando começarem a digitar uma consulta de pesquisa no site de Complementos do Microsoft Edge.** O preenchimento automático ajuda os usuários a concluir a consulta de pesquisa sem ter que digitar a cadeia de caracteres inteira. Isso será útil porque os usuários não precisarão se lembrar das ortografias corretas e poderão escolher uma das opções disponíveis.

* **Remover a API de cache de aplicativo HTML5.**  A partir da versão 86 do Microsoft Edge, a API de cache de aplicativo herdado que permite o uso offline de páginas da Web será removida do Microsoft Edge. Os desenvolvedores da Web devem examinar a [documentação WebDev](https://web.dev/appcache-removal/) para saber mais sobre como substituir a API de cache de aplicativo com Profissionais de Serviço.  Importante: você pode solicitar um [Token OriginTrial do AppCache](https://developers.chrome.com/origintrials/#/view_trial/1776670052997660673) que permite que os sites continuem usando a versão preterida da API de cache de aplicativo até a versão 90 do Microsoft Edge.

* **Segurança:**

  * Suporte ao DNS seguro (DNS em HTTPS).  A partir da versão 86 do Microsoft Edge, as configurações para controlar o DNS seguro em dispositivos não gerenciados estarão disponíveis. Essas configurações não podem ser acessadas por usuários em dispositivos gerenciados, mas os administradores de TI podem habilitar ou desabilitar o DNS seguro usando a política de grupo [dnsoverhttpsmode](./microsoft-edge-policies.md#dnsoverhttpsmode).


* **Adicione uma imagem personalizada à página Nova guia (NTP) usando uma política de grupo.** A partir da versão 86 do Microsoft Edge, a NTP tem a opção de substituir a imagem padrão por uma imagem personalizada fornecida pelo usuário. A habilidade de gerenciar as propriedades desta imagem também é compatível com a política de grupo.

* **Combinar os atalhos de teclado personalizados com o VS Code.** O DevTools do Microsoft Edge agora é compatível com a personalização de atalhos de teclado no DevTools para corresponder ao editor/IDE. (No Microsoft Edge 84, adicionamos a capacidade de combinar os atalhos de teclado do DevTools com o VS Code).

* **Substituir as políticas [MetricsReportingEnabled](/DeployEdge/microsoft-edge-policies#metricsreportingenabled) e [SendSiteInformationToImproveServices](/DeployEdge/microsoft-edge-policies#sendsiteinfotoimproveservices) para versões inferiores do Windows e macOS.** Essas políticas foram preteridas na versão 86 do Microsoft Edge e se tornarão preteridas na versão 89 do Microsoft Edge.<br>
Essas políticas são substituídas por [Permitir Telemetria](/windows/privacy/configure-windows-diagnostic-data-in-your-organization) no Windows 10 e a nova política [DiagnosticData](./microsoft-edge-policies.md#diagnosticdata) para todas as outras políticas. Isso permitirá que os usuários gerenciem os dados de diagnóstico enviados para a Microsoft do Windows 7, 8, 8.1 e macOS.

* **SameSite=Lax Cookies por padrão**. Para melhorar a segurança e a privacidade da web, os cookies agora serão padronizados para manipulação como [SameSite=Lax](https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie/SameSite). Isso significa que os cookies só serão enviados em um contexto de first-party e serão omitidos para as solicitações enviadas a terceiros. Essa alteração pode causar impacto de compatibilidade em sites que exigem cookies para recursos de terceiros funcionarem corretamente. Para permitir tais cookies, os desenvolvedores da Web podem marcar cookies que devem ser configurados e enviados a contextos de terceiros, adicionando `SameSite=none` explícitos e atributos `Secure` quando o cookie é definido. As empresas que desejam isentar determinados sites da alteração podem fazer isso usando a política [LegacySameSiteCookieBehaviorEnabledForDomainList](./microsoft-edge-policies.md#legacysamesitecookiebehaviorenabledfordomainlist) ou podem recusar a alteração em todos os sites que usam a política [LegacySameSiteCookieBehaviorEnabled](./microsoft-edge-policies.md#legacysamesitecookiebehaviorenabled).

### <a name="policy-updates"></a>Atualizações de política

#### <a name="new-policies"></a>Novas políticas

Dezenove novas políticas foram adicionadas. Baixe os modelos administrativos atualizados da [página inicial do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise). As novas políticas a seguir foram adicionadas.

- [CollectionsServicesAndExportsBlockList](./microsoft-edge-policies.md#collectionsservicesandexportsblocklist) - Bloquear o acesso a uma lista especificada de serviços e exportar destinos em Coleções.
- [DefaultSensorsSetting](./microsoft-edge-policies.md#defaultsensorssetting) - configuração de sensores padrão.
- [DefaultSerialGuardSetting](./microsoft-edge-policies.md#defaultserialguardsetting) - Controlar o uso da API serial.
- [DiagnosticData](./microsoft-edge-policies.md#diagnosticdata) -  Enviar dados de diagnóstico obrigatórios e opcionais referentes ao uso do navegador.
- [EnterpriseModeSiteListManagerAllowed](./microsoft-edge-policies.md#enterprisemodesitelistmanagerallowed) - Permitir o acesso à ferramenta Enterprise Mode Site List Manager.
- [ForceSync](./microsoft-edge-policies.md#forcesync) - Forçar a sincronização dos dados do navegador e não mostrar o aviso de consentimento da sincronização.
- [InsecureFormsWarningsEnabled](./microsoft-edge-policies.md#insecureformswarningsenabled) - Habilitar avisos para formulários inseguros.
- [InternetExplorerIntegrationTestingAllowed](./microsoft-edge-policies.md#internetexplorerintegrationtestingallowed) - Permitir teste no modo Internet Explorer.
- [SpotlightExperiencesAndRecommendationsEnabled](./microsoft-edge-policies.md#spotlightexperiencesandrecommendationsenabled) - Escolher se os usuários podem receber imagens de plano de fundo personalizadas e texto, sugestões, notificações e dicas para os serviços Microsoft.
- [NewTabPageAllowedBackgroundTypes](./microsoft-edge-policies.md#newtabpageallowedbackgroundtypes) - Configurar os tipos de plano de fundo permitidos para o layout da página da nova guia.
- [SaveCookiesOnExit](./microsoft-edge-policies.md#savecookiesonexit) - Salvar os cookies ao fechar o Microsoft Edge.
- [SensorsAllowedForUrls](./microsoft-edge-policies.md#sensorsallowedforurls) - Permitir o acesso a sensores em sites específicos.
- [SensorsBlockedForUrls](./microsoft-edge-policies.md#sensorsblockedforurls) - Bloquear o acesso a sensores em sites específicos.
- [SerialAskForUrls](./microsoft-edge-policies.md#serialaskforurls) - Permitir a API serial em sites específicos.
- [SerialBlockedForUrls](./microsoft-edge-policies.md#serialblockedforurls) - Bloquear a API serial em sites específicos.
- [URLBlocklist](./microsoft-edge-policies.md#urlblocklist) - Bloquear o acesso a uma lista de URLs.
- [URLAllowlist](./microsoft-edge-policies.md#urlallowlist) - Definir uma lista de URLs permitidas.
- [UserAgentClientHintsEnabled](./microsoft-edge-policies.md#useragentclienthintsenabled) - Habilitar o recurso de Dicas do Cliente Usuário-Agente.
- [UserDataSnapshotRetentionLimit](./microsoft-edge-policies.md#userdatasnapshotretentionlimit) - Limita o número de instantâneos de dados do usuário mantidos para uso no caso de uma reversão de emergência.

#### <a name="deprecated-policies"></a>Políticas preteridas

- [MetricsReportingEnabled](./microsoft-edge-policies.md#metricsreportingenabled) - habilita o uso e os relatórios de dados relacionados a falhas.
- [SendSiteInfoToImproveServices](./microsoft-edge-policies.md#sendsiteinfotoimproveservices) - envia informações do site para melhorar os serviços da Microsoft.

#### <a name="obsoleted-policy"></a>Política obsoleta

[TLS13HardeningForLocalAnchorsEnabled](./microsoft-edge-policies.md#tls13hardeningforlocalanchorsenabled)- Habilita um recurso de segurança TLS 1,3 para âncoras de confiança locais.

#### <a name="policy-caption-changed"></a>Legenda de política alterada

[NativeWindowOcclusionEnabled](./microsoft-edge-policies.md#nativewindowocclusionenabled) - Habilitar a oclusão da janela nativa.

#### <a name="policy-description-changed"></a>A descrição da política foi alterada

- [AdsSettingForIntrusiveAdsSites](./microsoft-edge-policies.md#adssettingforintrusiveadssites)
- [AllowTokenBindingForUrls](./microsoft-edge-policies.md#allowtokenbindingforurls)
- [AmbientAuthenticationInPrivateModesEnabled](./microsoft-edge-policies.md#ambientauthenticationinprivatemodesenabled)
- [ApplicationGuardContainerProxy](./microsoft-edge-policies.md#applicationguardcontainerproxy)
- [AutoImportAtFirstRun](./microsoft-edge-policies.md#autoimportatfirstrun)
- [AutoOpenFileTypes](./microsoft-edge-policies.md#autoopenfiletypes)
- [BrowserSignin](./microsoft-edge-policies.md#browsersignin)
- [ClearBrowsingDataOnExit](./microsoft-edge-policies.md#clearbrowsingdataonexit) 
- [ClickOnceEnabled](./microsoft-edge-policies.md#clickonceenabled)
- [CommandLineFlagSecurityWarningsEnabled](./microsoft-edge-policies.md#commandlineflagsecuritywarningsenabled)
- [ConfigureOnPremisesAccountAutoSignIn](./microsoft-edge-policies.md#configureonpremisesaccountautosignin)
- [ConfigureShare](./microsoft-edge-policies.md#configureshare)
- [CookiesAllowedForUrls](./microsoft-edge-policies.md#cookiesallowedforurls)
- [CustomHelpLink](./microsoft-edge-policies.md#customhelplink)
- [DefaultCookiesSetting](./microsoft-edge-policies.md#defaultcookiessetting)
- [DefaultGeolocationSetting](./microsoft-edge-policies.md#defaultgeolocationsetting)
- [DefaultImagesSetting](./microsoft-edge-policies.md#defaultimagessetting)
- [DefaultInsecureContentSetting](./microsoft-edge-policies.md#defaultinsecurecontentsetting)
- [DefaultJavaScriptSetting](./microsoft-edge-policies.md#defaultjavascriptsetting)
- [DefaultNotificationsSetting](./microsoft-edge-policies.md#defaultnotificationssetting)
- [DefaultPluginsSetting](./microsoft-edge-policies.md#defaultpluginssetting)
- [DefaultPopupsSetting](./microsoft-edge-policies.md#defaultpopupssetting)
- [DefaultSearchProviderEnabled](./microsoft-edge-policies.md#defaultsearchproviderenabled)
- [DefaultWebBluetoothGuardSetting](./microsoft-edge-policies.md#defaultwebbluetoothguardsetting)
- [DefaultWebUsbGuardSetting](./microsoft-edge-policies.md#defaultwebusbguardsetting)
- [DelayNavigationsForInitialSiteListDownload](./microsoft-edge-policies.md#delaynavigationsforinitialsitelistdownload)
- [DeveloperToolsAvailability](./microsoft-edge-policies.md#developertoolsavailability)
- [EnableSha1ForLocalAnchors](./microsoft-edge-policies.md#enablesha1forlocalanchors)
- [DownloadRestrictions](./microsoft-edge-policies.md#downloadrestrictions)
- [EnableDeprecatedWebPlatformFeatures](./microsoft-edge-policies.md#enabledeprecatedwebplatformfeatures)
- [WinHttpProxyResolverEnabled](./microsoft-edge-policies.md#winhttpproxyresolverenabled)
- [ExperimentationAndConfigurationServiceControl](./microsoft-edge-policies.md#experimentationandconfigurationservicecontrol)
- [ExternalProtocolDialogShowAlwaysOpenCheckbox](./microsoft-edge-policies.md#externalprotocoldialogshowalwaysopencheckbox)
- [ExtensionInstallForcelist](./microsoft-edge-policies.md#extensioninstallforcelist)
- [ForceBingSafeSearch](./microsoft-edge-policies.md#forcebingsafesearch)
- [ForceYouTubeRestrict](./microsoft-edge-policies.md#forceyoutuberestrict)
- [HomepageIsNewTabPage](./microsoft-edge-policies.md#homepageisnewtabpage)
- [HomepageLocation](./microsoft-edge-policies.md#homepagelocation)
- [InPrivateModeAvailability](./microsoft-edge-policies.md#inprivatemodeavailability)
- [InternetExplorerIntegrationEnhancedHangDetection](./microsoft-edge-policies.md#internetexplorerintegrationenhancedhangdetection)
- [InternetExplorerIntegrationLevel](./microsoft-edge-policies.md#internetexplorerintegrationlevel)
- [InternetExplorerIntegrationSiteRedirect](./microsoft-edge-policies.md#internetexplorerintegrationsiteredirect)
- [LegacySameSiteCookieBehaviorEnabled](./microsoft-edge-policies.md#legacysamesitecookiebehaviorenabled)
- [NativeWindowOcclusionEnabled](./microsoft-edge-policies.md#nativewindowocclusionenabled)
- [NavigationDelayForInitialSiteListDownloadTimeout](./microsoft-edge-policies.md#navigationdelayforinitialsitelistdownloadtimeout)
- [NetworkPredictionOptions](./microsoft-edge-policies.md#networkpredictionoptions)
- [NewTabPageLocation](./microsoft-edge-policies.md#newtabpagelocation)
- [NewTabPageSearchBox](./microsoft-edge-policies.md#newtabpagesearchbox)
- [NewTabPageSetFeedType](./microsoft-edge-policies.md#newtabpagesetfeedtype)
- [NonRemovableProfileEnabled](./microsoft-edge-policies.md#nonremovableprofileenabled)
- [PasswordProtectionWarningTrigger](./microsoft-edge-policies.md#passwordprotectionwarningtrigger)
- [PasswordProtectionLoginURLs](./microsoft-edge-policies.md#passwordprotectionloginurls)
- [PasswordProtectionChangePasswordURL](./microsoft-edge-policies.md#passwordprotectionchangepasswordurl)
- [PluginsAllowedForUrls](./microsoft-edge-policies.md#pluginsallowedforurls)
- [PluginsBlockedForUrls](./microsoft-edge-policies.md#pluginsblockedforurls)
- [PreventSmartScreenPromptOverride](./microsoft-edge-policies.md#preventsmartscreenpromptoverride)
- [PreventSmartScreenPromptOverrideForFiles](./microsoft-edge-policies.md#preventsmartscreenpromptoverrideforfiles)
- [ProxyMode](./microsoft-edge-policies.md#proxymode)
- [RegisteredProtocolHandlers](./microsoft-edge-policies.md#registeredprotocolhandlers)
- [RelaunchNotification](./microsoft-edge-policies.md#relaunchnotification)
- [RestoreOnStartup](./microsoft-edge-policies.md#restoreonstartup)
- [RestoreOnStartupURLs](./microsoft-edge-policies.md#restoreonstartupurls)
- [RestrictSigninToPattern](./microsoft-edge-policies.md#restrictsignintopattern)
- [SSLVersionMin](./microsoft-edge-policies.md#sslversionmin)
- [SmartScreenAllowListDomains](./microsoft-edge-policies.md#smartscreenallowlistdomains)
- [SmartScreenEnabled](./microsoft-edge-policies.md#smartscreenenabled)
- [SmartScreenForTrustedDownloadsEnabled](./microsoft-edge-policies.md#smartscreenfortrusteddownloadsenabled)
- [SmartScreenPuaEnabled](./microsoft-edge-policies.md#smartscreenpuaenabled)
- [SyncTypesListDisabled](./microsoft-edge-policies.md#synctypeslistdisabled)
- [TrackingPrevention](./microsoft-edge-policies.md#trackingprevention)
- [WebRtcLocalhostIpHandling](./microsoft-edge-policies.md#webrtclocalhostiphandling)

<!-- end 86 -->

## <a name="version-85056441-august-25"></a>Versão 85.0.564.41: 25 de agosto

Correção de vários bugs e problemas de desempenho.

## <a name="version-85056440-august-21"></a>Versão 85.0.564.40: 21 de agosto

Correção de vários bugs e problemas de desempenho.

## <a name="version-85056436-august-17"></a>Versão 85.0.564.36: 17 de agosto

Correção de vários bugs e problemas de desempenho.

## <a name="version-85056430-august-10"></a>Versão 85.0.564.30: 10 de agosto

Correção de vários bugs e problemas de desempenho.

## <a name="version-85056423-august-3"></a>Versão 85.0.564.23: 03 de agosto

Correção de vários bugs e problemas de desempenho.
<!-- major 85 -->
## <a name="version-85056418-july-28"></a>Versão 85.0.564.18, 28 de Julho

### <a name="feature-updates"></a>Atualizações de recursos

- **Sincronização local de Favoritos e Configurações**. Agora, você pode sincronizar os favoritos do navegador e as configurações entre os perfis do Active Directory dentro de seu próprio ambiente sem a necessidade de sincronização na nuvem.

- **O suporte à Política de Grupo do Microsoft Edge para combinações de sites e aplicativos confiáveis para iniciar sem aviso de confirmação.** Foi acrescentado o suporte à Política de Grupo que permite aos administradores adicionar combinações de sites e aplicativos confiáveis ​​para inicialização sem o aviso de confirmação. Isto adiciona capacidade aos administradores para configurar combinações de protocolo/origem confiáveis (como os aplicativos do Microsoft 365) para seus usuários finais suprimirem a solicitação de confirmação ao navegar para uma URL que contenha um protocolo de aplicativo.

- **Ferramenta Marca-texto para PDF**. Esta ferramenta pode ser facilmente adicionada à barra de ferramentas para realçar facilmente o texto importante no PDF.

- **A API de Acesso ao Armazenamento está disponível**. A API de Acesso ao Armazenamento permite acesso ao armazenamento primário em um contexto de terceiros quando um usuário tem providenciado uma intenção direta de permitir o armazenamento que de outra forma seria bloqueado pela configuração atual do navegador. Para saber mais, veja [API de Acesso de Armazenamento](https://www.chromestatus.com/feature/5612590694662144).

- **Enviar para o OneNote está disponível nas Coleções do Microsoft Edge**. Todos estão entusiasmados em poder enviar as informações que eles reunirão nas Coleções para o OneNote, onde podem acrescentá-las a um projeto maior e colaborar com outras pessoas! E ainda mais importante, no Microsoft Edge 85, você poderá enviar conteúdo para produtos do *Office para Mac* (Word, Excel e OneNote) tanto para a conta Microsoft como para o Azure Active Directory.

- **Atualizações do DevTools**. Para obter detalhes sobre as atualizações a seguir, confira [Novidades no DevTools (Microsoft Edge 85)](/microsoft-edge/devtools-guide-chromium/whats-new/2020/06/devtools).

   - O DevTools do Microsoft Edge é compatível com a emulação Surface Duo. O DevTools do Microsoft Edge pode emular o Surface Duo para que você possa testar como o seu conteúdo da Web será visualizado em dispositivos com duas telas. Para ativar esse experimento no DevTools, entre no modo do dispositivo pressionando Ctrl + Shift + M no Windows ou Command + Shift + M no macOS e selecione Surface Duo na lista de seleção do dispositivo.
   - O DevTools do Microsoft Edge permite combinar atalhos de teclado com o Código VS. O DevTools do Microsoft Edge é compatível com a personalização de atalhos de teclado no DevTools para corresponder ao editor/IDE. No Microsoft Edge 85, estamos adicionando a capacidade para combinar os atalhos de teclado do DevTools para o VS Code. Essa alteração ajudará a aumentar a produtividade no Código VS e no DevTools.

### <a name="policy-updates"></a>Atualizações de política

#### <a name="new-policies"></a>Novas políticas

Treze novas políticas foram adicionadas. Baixe os modelos administrativos atualizados da [página inicial do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise). As novas políticas a seguir foram adicionadas.

- [AutoLaunchProtocolsFromOrigins](./microsoft-edge-policies.md#autolaunchprotocolsfromorigins) - Definir uma lista de protocolos que podem lançar um aplicativo externo de origens listadas sem alertar o usuário.
- [ AutoOpenAllowedForURLsURLs](./microsoft-edge-policies.md#autoopenallowedforurls) - URLs nas quais o AutoOpenFileTypes pode aplicar.
- [AutoOpenFileTypes](./microsoft-edge-policies.md#autoopenfiletypes) - Lista de tipos de arquivo que devem ser abertos automaticamente no download.
- [DefaultSearchProviderContextMenuAccessAllowed](./microsoft-edge-policies.md#defaultsearchprovidercontextmenuaccessallowed) - Permitir acesso à busca do menu de contexto do provedor de pesquisa padrão.
- [EnableSha1ForLocalAnchors](./microsoft-edge-policies.md#enablesha1forlocalanchors) - Permitir certificados assinados usando SHA-1 quando emitido por âncoras de confiança local. <!--- [ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](./microsoft-edge-policies.md#exemptdomainfiletypepairsfromfiletypedownloadwarnings) - Disable download file type extension-based warnings for specified file types on domains. -->
- [IntensiveWakeUpThrottlingEnabled](./microsoft-edge-policies.md#intensivewakeupthrottlingenabled) - Controlar o recurso IntensiveWakeUpThrottling.
- [NewTabPagePrerenderEnabled](./microsoft-edge-policies.md#newtabpageprerenderenabled) - Habilitar o pré-carregamento da nova página da guia para renderização mais rápida.
- [NewTabPageSearchBox](./microsoft-edge-policies.md#newtabpagesearchbox) - Configurar a nova experiência da caixa de pesquisa da página da guia.
- [PasswordMonitorAllowed](./microsoft-edge-policies.md#passwordmonitorallowed) - Permitir que os usuários sejam alertados caso suas senhas não sejam seguras.
- [RoamingProfileSupportEnabled](./microsoft-edge-policies.md#roamingprofilesupportenabled) - Habilitar o uso de cópias de roaming para dados de perfil do Microsoft Edge.
- [RoamingProfileLocation](./microsoft-edge-policies.md#roamingprofilelocation) - Configurar o roaming do diretório de perfil.
- [TLSCipherSuiteDenyList](./microsoft-edge-policies.md#tlsciphersuitedenylist) - Especificar os pacotes de codificação TLS para desabilitar.

#### <a name="obsoleted-policies"></a>Políticas obsoletas

- [EnableDomainActionsDownload](./microsoft-edge-policies.md#enabledomainactionsdownload) Habilitar o Download de Ações de Domínio da Microsoft.
- [WebComponentsV0Enabled](./microsoft-edge-policies.md#webcomponentsv0enabled) -reabilita a API de componentes Web V0 até M84.
- [WebDriverOverridesIncompatiblePolicies](./microsoft-edge-policies.md#webdriveroverridesincompatiblepolicies) - Permitir ao WebDriver Substituir Políticas Incompatíveis.

<!--- END ---->

## <a name="version-84052235-july-9"></a>Versão 84.0.522.35: 9 de julho

Correção de vários bugs e problemas de desempenho.

## <a name="version-84052228-june-26"></a>Versão 84.0.522.28: 26 de junho

Correção de vários bugs e problemas de desempenho.

## <a name="version-84052226-june-24"></a>Versão 84.0.522.26: 24 de junho

Correção de vários bugs e problemas de desempenho.

## <a name="version-84052220-june-15"></a>Versão 84.0.522.20: 15 de junho

Correção de vários bugs e problemas de desempenho.

## <a name="version-84052215-june-8"></a>Versão 84.0.522.15: 8 de junho

Correção de vários bugs e problemas de desempenho.

## <a name="version-84052211-june-2"></a>Versão 84.0.522.11: 2 de junho

### <a name="feature-updates"></a>Atualizações de recursos

- Esta versão do Microsoft Edge fornece uma melhoria na velocidade de download de lista de sites para o modo Internet Explorer.  Reduzimos o atraso de download para a lista de sites no modo Internet Explorer para 0 segundo (de uma espera de 60 segundos) na ausência de uma lista de sites armazenados em cache. Também adicionamos suporte à política de grupo para casos em que as navegações de página inicial no modo Internet Explorer precisem ser adiadas até que a lista de sites seja baixada. Para obter mais informações, confira a política [DelayNavigationsForInitialSiteListDownload](./microsoft-edge-policies.md#delaynavigationsforinitialsitelistdownload).

- O Microsoft Edge agora permite que os usuários entrem no navegador quando ele é "executado como administrador" no Windows 10. Isso ajudará os clientes que usam o Microsoft Edge no Windows Server ou nos cenários de área de trabalho remota ou área restrita.

- O Microsoft Edge agora oferece suporte total ao mouse quando estiver no modo de tela inteira. Agora, você pode usar o mouse para acessar as guias, a barra de endereços e outros itens sem ter que sair do modo de tela inteira.

- Melhoria na compra online. Adicione apelidos personalizados para cartões de crédito ou débitos salvos. Agora, você pode distinguir e diferenciar os cartões de crédito ao fazer compras online. Dar apelidos aos cartões de crédito ou débito permite que você escolha o cartão correto ao usar o preenchimento automático para selecionar um método de pagamento.

- O TLS/1.0 e o TLS/1.1 estão desabilitados por padrão. Para ajudar a descobrir sites afetados, você pode definir o sinalizador *edge://flags/#display-legacy-tls-warnings* para fazer o Microsoft Edge exibir um aviso não bloqueado de "Não Seguro" ao carregar páginas que exijam protocolos TLS herdados. A política [SSLVersionMin](./microsoft-edge-policies.md#sslversionmin) permite reabilitar o TLS/1.0 e o TLS/1.1. Essa política permanecerá disponível pelo menos até a versão 88 do Microsoft Edge. Para saber mais, confira [Compatibilidade de sites - alterações que afetam o Microsoft Edge](/microsoft-edge/web-platform/site-impacting-changes).

- Aperfeiçoamentos do recurso Coleções:

  - Uma funcionalidade de anotação foi adicionada, o que permite que você adicione uma anotação ou comentário a um item em uma coleção. As anotações são agrupadas e permanecem anexadas a um item, mesmo que você organize os itens em uma coleção. Para experimentar esse novo recurso, clique com o botão direito do mouse em um item e escolha "Adicionar anotação".
  - Você pode alterar a cor da tela de fundo das anotações em coleções. Você pode usar a codificação de cores para ajudá-lo a organizar informações e aumentar a produtividade.
  - Os aperfeiçoamentos de desempenho são notáveis, permitindo que você exporte suas coleções para o Excel em menos tempo do que em versões anteriores do Microsoft Edge.

- Suporte adicional à API do Microsoft Edge:

  - A API de Acesso ao Armazenamento. Essa API permite o acesso ao armazenamento primário em um contexto de terceiros quando um usuário expressa uma intenção direta de permitir o armazenamento que seria bloqueado pela configuração atual do navegador.

    À medida que a privacidade está ficando cada vez mais importante para os usuários, as solicitações para padrões mais restritivos de navegador e configurações de aceitação de usuário, como bloqueio de todo o acesso de armazenamento de terceiros, são cada vez mais comuns. Embora essas configurações ajudem a melhorar a privacidade e bloquear o acesso indesejado de terceiros desconhecidos ou não confiáveis, eles podem ter efeitos colaterais indesejados, como bloquear o acesso a conteúdo que o usuário pode querer ver (por exemplo, mídia social e conteúdo de mídia inserida.)

  - A API do Sistema de Arquivos Nativo, o que significa que você pode conceder permissões aos sites para editar arquivos ou pastas por meio da API do Sistema de Arquivos Nativo.

- Aperfeiçoamentos em PDF:

  - O recurso Ler em Voz Alta para PDF permite que os usuários ouçam o conteúdo em PDF enquanto realizam outras tarefas que podem ser importantes para eles. Ele também ajuda os alunos com estilo de aprendizagem auditivo-visual a se concentrarem em ler o conteúdo, facilitando o aprendizado.
  - Edição de arquivo PDF aperfeiçoada. Agora, você pode salvar uma edição feita em um PDF em vez de salvar uma cópia sempre que editar o PDF.

- O Microsoft Edge agora oferece a opção Tradução na Leitura Avançada. Quando um usuário abre o modo de exibição de Leitura Avançada, há agora a opção de traduzir a página para o idioma desejado.

- O DevTools é compatível com a personalização de atalhos de teclado para corresponder ao editor/IDE, que inclui o VS Code.

### <a name="policy-updates"></a>Atualizações de política

#### <a name="new-policies"></a>Novas políticas

Cinco novas políticas foram adicionadas. Baixe os modelos administrativos atualizados da [página inicial do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise). As novas políticas a seguir foram adicionadas.

- [AppCacheForceEnabled](./microsoft-edge-policies.md#appcacheforceenabled) - Permite reabilitar o recurso AppCache, mesmo que ele esteja desativado por padrão.
- [ApplicationGuardContainerProxy](./microsoft-edge-policies.md#applicationguardcontainerproxy)- Proxy de Contêiner do Application Guard.
- [DelayNavigationsForInitialSiteListDownload](./microsoft-edge-policies.md#delaynavigationsforinitialsitelistdownload) - Exigir que a lista de sites no Modo Empresarial esteja disponível antes da navegação na guia.
- [NativeWindowOcclusionEnabled](./microsoft-edge-policies.md#nativewindowocclusionenabled) - Ative a ocultação do Windows Nativo.
- [NavigationDelayForInitialSiteListDownloadTimeout](./microsoft-edge-policies.md#navigationdelayforinitialsitelistdownloadtimeout) -Definir um tempo limite para o atraso da navegação da guia para a Lista de Sites no Modo Empresarial.

#### <a name="deprecated-policies"></a>Políticas preteridas

- [AllowSyncXHRInPageDismissal](./microsoft-edge-policies.md#allowsyncxhrinpagedismissal) - Autorizar páginas a enviar solicitações de XHR síncronas durante a descarte da página.
- [BuiltinCertificateVerifierEnabled](./microsoft-edge-policies.md#builtincertificateverifierenabled) - Determina se o verificador de certificado interno será usado para verificar certificados do servidor.
- [StricterMixedContentTreatmentEnabled](./microsoft-edge-policies.md#strictermixedcontenttreatmentenabled)- Habilita um tratamento mais estrito para conteúdo misto.

#### <a name="obsoleted-policy"></a>Política obsoleta

[ForceNetworkInProcess](./microsoft-edge-policies.md#forcenetworkinprocess) - Forçar a execução do código de rede no processo do navegador.

<!-- end 84 -->

## <a name="version-83047844-june-1"></a>Versão 83.0.478.44: 1 de junho

Correção de vários bugs e problemas de desempenho.

## <a name="version-83047837-may-20"></a>Versão 83.0.478.37: 20 de maio

Correção de vários bugs e problemas de desempenho.

## <a name="version-83047833-may-15"></a>Versão 83.0.478.33: 15 de maio

Correção de vários bugs e problemas de desempenho.

## <a name="version-83047828-may-7"></a>Versão 83.0.478.28: 7 de maio

Correção de vários bugs e problemas de desempenho.

## <a name="version-83047825-may-4"></a>Versão 83.0.478.25: 4 de maio

Correção de vários bugs e problemas de desempenho.

## <a name="version-83047818-april-27"></a>Versão 83.0.478.18: 27 de abril

Correção de vários bugs e problemas de desempenho.

## <a name="version-83047813-april-22"></a>Versão 83.0.478.13: 22 de abril

### <a name="feature-updates"></a>Atualizações de recursos

- Melhorias no Microsoft Defender SmartScreen: foram feitas várias melhorias no serviço Microsoft Defender SmartScreen, como proteção melhorada contra sites mal-intencionados que são redirecionados durante o carregamento e bloqueio de quadros de nível superior que substitui completamente sites mal-intencionados pela página de segurança do Microsoft Defender SmartScreen. O bloqueio de quadros de nível superior impede a reprodução de áudio e outras mídias do site mal-intencionado, o que proporciona uma experiência mais fácil e menos confusa.

- Em resposta a comentários dos usuários, os usuários agora podem impedir a limpeza de determinados cookies automaticamente quando o navegador é fechado. Essa opção será útil se houver um site do qual os usuários não queiram ser desconectados, mas ainda querem que todos os outros cookies sejam removidos quando o navegador fechar. Para usar esse recurso, acesse *edge://settings/clearBrowsingDataOnClose* e ative a opção "Cookies e outros dados do site".

- A Troca Automática de Perfis agora está disponível para ajudar você a acessar seu conteúdo de trabalho com mais facilidade em diferentes perfis. Se você usar vários perfis no trabalho, poderá verificar esse recurso navegando para um site que exija autenticação da sua conta corporativa ou de estudante enquanto estiver no seu perfil pessoal. Quando detectarmos uma alteração, você receberá uma solicitação para mudar para o seu perfil de trabalho para acessar o site sem precisar se autenticar. Quando você escolhe o perfil de trabalho para o qual deseja mudar, o site simplesmente abre no seu perfil de trabalho. Esse recurso de mudança de perfil ajuda você a manter seus dados pessoais e de trabalho separados e a acessar seu conteúdo de trabalho com mais facilidade. Se você não quiser que o recurso solicite a troca de perfis, você pode escolher a opção não me pergunte novamente isso ficará fora do seu caminho.

- Aperfeiçoamentos de recursos de coleções:
  - Você pode usar o recurso de arrastar e soltar para adicionar um item a uma coleção sem abrir a coleção. Ao arrastar e soltar, você também pode escolher um local na lista de coleções onde deseja colocar o item.
  - Você pode adicionar vários itens a uma coleção em vez de adicionar um item por vez. Para adicionar vários itens, selecione-os e, em seguida, arraste-os para uma coleção. Ou você pode selecionar os itens, clicar com o botão direito do mouse e escolher a coleção onde deseja colocar os itens.

- Você pode adicionar todas as guias em uma janela do Microsoft Edge a uma nova coleção sem adicioná-las individualmente. Para fazer isso, clique com o botão direito do mouse em qualquer guia e escolha "Adicionar todas as guias a uma nova coleção".

- A sincronização de extensão já está disponível. Agora você pode sincronizar suas extensões entre todos os seus dispositivos! As extensões da Microsoft Store e da Chrome Web Store serão sincronizadas com o Microsoft Edge. Para usar esse recurso: Clique nas reticências (**…**) na barra de menus, selecione **Configurações**. Em Seu perfil, clique em **Sincronização** para ver as opções de sincronização. Em **Perfis/Sincronização**, use a alternância para ativar as Extensões. Você pode usar a política de grupo [SyncTypesListDisabled](./microsoft-edge-policies.md#synctypeslistdisabled) para desativar a sincronização de extensões.

- Foi melhorada a mensagem na página de gerenciamento de downloads para downloads não seguros que foram bloqueados.

- Melhorias da Leitura Avançada:
  - Adicionado suporte para Advérbios na experiência Classe Gramatical que temos na Leitura Avançada. Ao ler um artigo na Leitura Avançada, abra as Ferramentas de Gramática e ative Advérbios em Classe Gramatical para destacar todos os advérbios na página.
  - Foi adicionada a capacidade de selecionar qualquer conteúdo em uma página da Web e abri-lo na Leitura Avançada. Essa capacidade permite que os usuários usem a Leitura Avançada e todas as Ferramentas de Aprendizagem, como Foco de Linha e Leitura em Voz Alta, em todos os sites.

- O link Doctor fornece a correção de host e uma consulta de pesquisa aos usuários quando eles digitam incorretamente uma URL. Por exemplo: <br>
Um usuário digita incorretamente "powerbi como" powerbbi". com. O link Doctor vai sugerir "powerbi". com como uma correção e criar um link para pesquisar por "powerbbi" caso o usuário esteja procurando algo diferente.

- Permita que os usuários salvem a decisão para iniciar um protocolo externo para um site específico. Os usuários podem configurar a política [ExternalProtocolDialogShowAlwaysOpenCheckbox](/DeployEdge/microsoft-edge-policies#externalprotocoldialogshowalwaysopencheckbox) para habilitar ou desabilitar esse recurso.

- Os usuários podem definir o Microsoft Edge como navegador padrão diretamente no Microsoft Edge **Configurações**. Esse recurso facilita a alteração do navegador padrão pelos usuários, dentro do contexto do próprio navegador, em vez de precisar pesquisar as configurações do sistema operacional. Para usar esse recurso, vá para *edge://settings/defaultBrowser* e clique em **tornar padrão**.

- Várias atualizações do DevTools, incluindo o suporte à depuração remota, aperfeiçoamentos na IU e muito mais. Para saber mais, consulte [Novidades no DevTools (Microsoft Edge 83)](/microsoft-edge/devtools-guide-chromium/whats-new/2020/03/devtools).

### <a name="policy-updates"></a>Atualizações de política

#### <a name="new-policies"></a>Novas políticas

15 novas políticas foram adicionadas. Baixe os modelos administrativos atualizados da [página inicial do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise). As novas políticas a seguir foram adicionadas.

- [AllowSurfGame](./microsoft-edge-policies.md#allowsurfgame) - Permitir jogo de surf.
- [AllowTokenBindingForUrls](./microsoft-edge-policies.md#allowtokenbindingforurls) - Configurar a lista de sites com os quais o Microsoft Edge tentará estabelecer uma Associação de Token.
- [BingAdsSuppression](./microsoft-edge-policies.md#bingadssuppression) - Bloquear todos os anúncios nos resultados de pesquisa do Bing.
- [BuiltinCertificateVerifierEnabled](./microsoft-edge-policies.md#builtincertificateverifierenabled) - Determina se o verificador de certificado interno será usado para verificar certificados do servidor.
- [ClearCachedImagesAndFilesOnExit](./microsoft-edge-policies.md#clearcachedimagesandfilesonexit) - Limpar imagens e arquivos em cache quando o Microsoft Edge é fechado.
- [ConfigureShare](./microsoft-edge-policies.md#configureshare) - Configurar a experiência de Compartilhamento.
- [DeleteDataOnMigration](./microsoft-edge-policies.md#deletedataonmigration) - Excluir dados antigos do navegador na migração.
- [DnsOverHttpsMode](./microsoft-edge-policies.md#dnsoverhttpsmode) - Controlar o modo de DNS sobre HTTPS.
- [DnsOverHttpsTemplates](./microsoft-edge-policies.md#dnsoverhttpstemplates) - Especificar o modelo de URI do resolvedor de DNS sobre HTTPS desejado.
- [FamilySafetySettingsEnabled](./microsoft-edge-policies.md#familysafetysettingsenabled) - Permitir que os usuários configurem a Proteção para a família.
- [LocalProvidersEnabled](./microsoft-edge-policies.md#localprovidersenabled) - Permitir sugestões de provedores locais.
- [ScrollToTextFragmentEnabled](./microsoft-edge-policies.md#scrolltotextfragmentenabled) - Ativar a rolagem para o texto especificado nos fragmentos de URL.
- [ScreenCaptureAllowed](./microsoft-edge-policies.md#screencaptureallowed) - Permitir ou negar a captura de tela.
- [SyncTypesListDisabled](./microsoft-edge-policies.md#synctypeslistdisabled) - Configurar a lista de tipos excluídos da sincronização.
- [NativeWindowOcclusionEnabled](./microsoft-edge-policies.md#nativewindowocclusionenabled) - Ative a ocultação do Windows Nativo.

#### <a name="deprecated-policy"></a>Política preterida

A política a seguir continuará funcionando nesta versão. Ela se tornará "obsoleta" em uma versão futura.

[EnableDomainActionsDownload](./microsoft-edge-policies.md#enabledomainactionsdownload) Habilitar o Download de Ações de Domínio da Microsoft

<!--  end 83 -->

## <a name="version-81041660-april-20"></a>Versão 81.0.416.60: 20 de abril

Correção de vários bugs e problemas de desempenho.

## <a name="version-81041658-april-17"></a>Versão 81.0.416.58: 17 de abril

Atualizações de segurança.

## <a name="version-81041650-april-10"></a>Versão 81.0.416.50: 10 de abril

Correção de vários bugs e problemas de desempenho.

## <a name="version-81041645-april-3"></a>Versão 81.0.416.45: 3 de abril

Correção de vários bugs e problemas de desempenho.

## <a name="version-81041641-march-30"></a>Versão 81.0.416.41: 30 de março

Correção de vários bugs e problemas de desempenho.

## <a name="version-81041634-march-17"></a>Versão 81.0.416.34: 17 de março

Correção de vários bugs e problemas de desempenho.

## <a name="version-81041631-march-12"></a>Versão 81.0.416.31: 12 de março

Correção de vários bugs e problemas de desempenho.

## <a name="version-81041628-march-9"></a>Versão 81.0.416.28: 9 de março

Correção de vários bugs e problemas de desempenho.

## <a name="version-81041620-february-28"></a>Versão 81.0.416.20: 28 de fevereiro

Correção de vários bugs e problemas de desempenho.

## <a name="version-81041612-february-20"></a>Versão 81.0.416.12: 20 de fevereiro

### <a name="feature-updates"></a>Atualizações de recursos

- Agora as coleções estão disponíveis. Você pode começar clicando no ícone Coleções ao lado da barra de endereços. Esta ação abrirá o painel Coleções, no qual você pode criar, editar e exibir Coleções. Projetamos Coleções com base no que você faz na Web. Se você for um comprador, um viajante ou um aluno, as Coleções poderão ajudá-lo. [Saiba mais](https://blogs.windows.com/msedgedev/2019/12/09/improvements-collections-sync-microsoft-edge/#LuDPRDUDCgdgdOVt.97).

- Permitir a remoção (Ocultar da barra de ferramentas) do botão coleções na barra de ferramentas do Microsoft Edge para obter consistência.

- A entrada local de uma conta do Active Directory local só será direcionada a organizações que as ativam. Se os usuários já tiverem entrado com uma conta do AD local, eles poderão sair dela. Agora, os usuários só entrarão automaticamente com a conta primária em seu sistema operacional se for uma conta Microsoft ou uma conta do Azure Active Directory. Os administradores podem habilitar para entrar automaticamente com uma conta do AD local usando a política ConfigureOnPremisesAccountAutoSignIn.

- Application Guard. Suporte para extensões agora disponível no contêiner.

- Foi adicionada uma mensagem para informar aos usuários que o Internet Explorer não está instalado quando eles navegam para uma página que está configurada para abrir no modo do Internet Explorer.

- A ferramenta modo de exibição 3D foi atualizada no Microsoft Edge DevTools com um novo recurso que ajuda a depurar o contexto de empilhamento de índice z. O modo de exibição 3D mostra uma representação da profundidade do DOM (modelo de objeto do documento) usando a cor e o empilhamento, e o modo de exibição de índice z ajuda a isolar os diferentes contextos de empilhamento da sua página. [Saiba mais](https://blogs.windows.com/msedgedev/2020/01/23/debug-z-index-3d-view-edge-devtools/).

- Localizadas as ferramentas de desenvolvimento F12 em dez novos idiomas, para que eles correspondam ao idioma usado no restante do navegador. [Saiba mais](https://blogs.windows.com/msedgedev/2020/02/04/localizing-edge-devtools/).

- Suporte adicional para a reprodução de Dolby Vision. No Windows 10 Build 17134 com Dolby Vision habilitado (Atualização de abril de 2018), os sites podem mostrar o conteúdo de visão Dolby. Veja como habilitar o conteúdo da visão Dolby da [Netflix](https://help.netflix.com/en/node/42384).

- O Microsoft Edge agora pode identificar e remover favoritos duplicados e pastas de mesclagem com o mesmo nome. Para acessar a ferramenta, clique na estrela na barra de ferramentas do navegador e selecione “Remover favoritos duplicados”.  Você poderá confirmar as alterações e todas as atualizações em seus favoritos serão sincronizadas entre dispositivos.

- Nós ouvimos de usuários que pode ser difícil distinguir uma janela de navegação normal no tema escuro de uma janela InPrivate, porque os quadros de janela são escuros. A nova pílula azul sólida InPrivate no canto superior direito ajuda a garantir aos usuários de que eles estão navegando no InPrivate.

- Abra links externos no perfil correto do navegador. Selecione um perfil padrão para que os links abertos para aplicativos externos sejam abertos a partir de *edge://settings/multiProfileSettings*.

- Foi adicionado um aviso para alertar os usuários que fazem login em um perfil de navegador com uma conta depois de fazer login anteriormente em outra conta. Isso ajudará a evitar a mesclagem de dados não intencionais.

- Caso tenha cartões de pagamento salvos em sua conta da Microsoft, você poderá usá-los no Microsoft Edge durante o preenchimento dos formulários de pagamento. Os cartões em sua conta da Microsoft serão sincronizados entre os dispositivos da área de trabalho e os detalhes completos serão compartilhados com o site após a autenticação de dois fatores (código de segurança e identidade da Microsoft). Para maior praticidade, você pode optar por salvar com segurança uma cópia do cartão no dispositivo durante a autenticação.

- O Foco de Linha foi projetado para os usuários que preferem se concentrar em uma parte limitada do conteúdo conforme eles são lidos. Permite aos usuários manter o foco em 1, 3 ou 5 linhas por vez e destacar o restante da página para permitir que os usuários leiam sem distrações. Os usuários podem rolar a tela usando o toque ou as teclas de direção, e o foco é deslocado de acordo.

- O Microsoft Edge agora está integrado ao verificador ortográfico do Windows nas plataformas do Windows 8.1 e posteriores. Esta integração fornece maior suporte a idiomas, com acesso a mais dicionários de idiomas e a capacidade de usar dicionários personalizados do Windows. Não será necessária nenhuma outra ação dos usuários quando um idioma tiver sido adicionado nas configurações de idioma do sistema operacional e uma verificação ortográfica de idioma estiver habilitada nas configurações do Microsoft Edge.

- Agora, quando os documentos em PDF estão abertos usando o Microsoft Edge, os usuários podem criar destaques, alterar a cor e excluir realces. Isso ajuda a referenciar partes importantes do documento posteriormente e a colaborar.

- Ao carregar documentos longos em PDF que foram otimizados para a Web, as páginas visualizadas pelo usuário serão carregadas mais rapidamente, paralelamente, enquanto o restante do documento estiver sendo carregado.

- Agora é mais fácil iniciar a leitura avançada de um site pressionando a tecla F9.

- Agora é mais fácil começar a ler em voz alta usando um atalho de teclado (Ctrl + Shift + U).

### <a name="policy-updates"></a>Atualizações de política

#### <a name="new-policies"></a>Novas políticas

12 novas políticas foram adicionadas. Baixe os modelos administrativos atualizados da [página inicial do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise). As novas políticas a seguir foram adicionadas.

- [AmbientAuthenticationInPrivateModesEnabled](./microsoft-edge-policies.md#ambientauthenticationinprivatemodesenabled)- Habilite a autenticação ambiente para perfis InPrivate e Guest. 
- [AudioSandboxEnabled](./microsoft-edge-policies.md#audiosandboxenabled)- Permite que a caixa de proteção de áudio seja executada.
- [ForceLegacyDefaultReferrerPolicy](./microsoft-edge-policies.md#forcelegacydefaultreferrerpolicy): Usa uma política referencial padrão de no-referrer-when-downgrade.
- [GloballyScopeHTTPAuthCacheEnabled](./microsoft-edge-policies.md#globallyscopehttpauthcacheenabled)- Habilita o cache de autenticação HTTP globalmente.
- [ImportExtensions](./microsoft-edge-policies.md#importextensions)- Permite a importação de extensões.
- [ImportCookies](./microsoft-edge-policies.md#importcookies)- Permite a importação de cookies.
- [ImportShortcuts](./microsoft-edge-policies.md#importshortcuts)- Permite a importação de atalhos.
- [InternetExplorerIntegrationSiteRedirect](./microsoft-edge-policies.md#internetexplorerintegrationsiteredirect)Especifica como as navegações "na página" para sites não configurados se comportam quando iniciadas nas páginas do modo Internet Explorer.
- [OmniboxMSBProviderEnabled](./microsoft-edge-policies.md)- Habilita o provedor Microsoft Search for Business no omnibox.
- [StricterMixedContentTreatmentEnabled](./microsoft-edge-policies.md#strictermixedcontenttreatmentenabled)- Habilita um tratamento mais estrito para conteúdo misto.
- [TLS13HardeningForLocalAnchorsEnabled](./microsoft-edge-policies.md#tls13hardeningforlocalanchorsenabled)- Habilita um recurso de segurança TLS 1,3 para âncoras de confiança locais.
- [ConfigureOnPremisesAccountAutoSignIn](./microsoft-edge-policies.md#configureonpremisesaccountautosignin)- Configura o login automático com uma conta de domínio do Active Directory quando não houver nenhuma conta de domínio do Azure AD.

#### <a name="deprecated-policies"></a>Políticas preteridas

As seguintes políticas continuam a funcionar nesta versão. Elas se tornarão "obsoletas" em uma versão futura.

- [WebComponentsV0Enabled](./microsoft-edge-policies.md#webcomponentsv0enabled) - Reabilita a API de componentes Web V0 até M84.
- [WebDriverOverridesIncompatiblePolicies](./microsoft-edge-policies.md#webdriveroverridesincompatiblepolicies)- Permite que o WebDriver substitua incompatível.

## <a name="see-also"></a>Consulte também

- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
