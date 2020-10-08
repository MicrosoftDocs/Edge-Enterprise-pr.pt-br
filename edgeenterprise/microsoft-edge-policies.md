---
title: Documentação de política do navegador Microsoft Edge
ms.author: stmoody
author: brianalt-msft
manager: tahills
ms.date: 10/02/2020
audience: ITPro
ms.topic: reference
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
ms.custom: ''
description: Documentação do Windows e do Mac para todas as políticas compatíveis com o Microsoft Edge Browser
ms.openlocfilehash: 906a8cdd73e07efc5662e9b3ea51d8b7a2f03079
ms.sourcegitcommit: 3478cfcf2b03944213a7c7c61f05490bc37aa7c4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/03/2020
ms.locfileid: "11094745"
---
# Microsoft Edge - Políticas
A versão mais recente do Microsoft Edge inclui as políticas a seguir. Você pode usar essas políticas para configurar como o Microsoft Edge será executado em sua organização.

Para saber mais sobre o conjunto de políticas, usado para controlar como e quando o Microsoft Edge é atualizado, confira [Referência de política de atualização do Microsoft Edge](microsoft-edge-update-policies.md).

Você pode baixar o [Kit de ferramentas de conformidade de segurança da Microsoft](https://www.microsoft.com/download/details.aspx?id=55319) para obter as configurações de linha de base de configuração de segurança do Microsoft Edge. Para saber mais, confira o blog [Linhas de base de segurança da Microsoft,](https://techcommunity.microsoft.com/t5/microsoft-security-baselines/bg-p/Microsoft-Security-Baselines).

> [!NOTE]
> Este artigo se aplica ao Microsoft Edge versão 77 ou posterior.

## Políticas disponíveis
Estas tabelas listam todas as políticas de grupo relacionadas ao navegador disponíveis nesta versão do Microsoft Edge. Use os links na tabela a seguir para obter mais detalhes sobre políticas específicas.

|||
|-|-|
|[Configurações do Application Guard](#application-guard-settings)|[Cast](#cast)|
|[Configurações de conteúdo](#content-settings)|[Provedor de pesquisa padrão](#default-search-provider)|
|[Extensões](#extensions)|[Autenticação HTTP](#http-authentication)|
|[Configurações do modo de quiosque](#kiosk-mode-settings)|[Sistema de mensagens nativo](#native-messaging)|
|[Gerenciador de senhas e proteção](#password-manager-and-protection)|[Impressão](#printing)|
|[Servidor proxy](#proxy-server)|[Configurações do SmartScreen](#smartscreen-settings)|
|[Página de inicialização, página inicial e nova guia](#startup-home-page-and-new-tab-page)|[Adicional](#additional)|


### [*Configurações do Application Guard*](#application-guard-settings-policies)
|Nome da política|Legenda|
|-|-|
|[ApplicationGuardContainerProxy](#applicationguardcontainerproxy)|Proxy de contêiner do Application Guard|
### [*Cast*](#cast-policies)
|Nome da política|Legenda|
|-|-|
|[EnableMediaRouter](#enablemediarouter)|Habilitar o Google Cast|
|[ShowCastIconInToolbar](#showcasticonintoolbar)|Mostrar o ícone de conversão na barra de ferramentas|
### [*Configurações de conteúdo*](#content-settings-policies)
|Nome da política|Legenda|
|-|-|
|[AutoSelectCertificateForUrls](#autoselectcertificateforurls)|Selecionar automaticamente os certificados de cliente para esses sites|
|[CookiesAllowedForUrls](#cookiesallowedforurls)|Permitir cookies em sites específicos|
|[CookiesBlockedForUrls](#cookiesblockedforurls)|Bloquear cookies em sites específicos|
|[CookiesSessionOnlyForUrls](#cookiessessiononlyforurls)|Limitar cookies de sites específicos para a sessão atual|
|[DefaultCookiesSetting](#defaultcookiessetting)|Configurar cookies|
|[DefaultFileSystemReadGuardSetting](#defaultfilesystemreadguardsetting)|Controlar o uso da API do Sistema de arquivos para leitura|
|[DefaultFileSystemWriteGuardSetting](#defaultfilesystemwriteguardsetting)|Controlar o uso da API do Sistema de arquivos para gravação|
|[DefaultGeolocationSetting](#defaultgeolocationsetting)|Configuração de geolocalização padrão|
|[DefaultImagesSetting](#defaultimagessetting)|Configuração de imagens padrão|
|[DefaultInsecureContentSetting](#defaultinsecurecontentsetting)|Controlar o uso de exceções de conteúdo não seguro|
|[DefaultJavaScriptSetting](#defaultjavascriptsetting)|Configuração padrão de JavaScript|
|[DefaultNotificationsSetting](#defaultnotificationssetting)|Configuração de notificação padrão|
|[DefaultPluginsSetting](#defaultpluginssetting)|Configuração padrão do Adobe Flash|
|[DefaultPopupsSetting](#defaultpopupssetting)|Configuração da janela pop-up padrão|
|[DefaultWebBluetoothGuardSetting](#defaultwebbluetoothguardsetting)|Controlar o uso da API do Bluetooth na Web|
|[DefaultWebUsbGuardSetting](#defaultwebusbguardsetting)|Controlar o uso da API WebUSB|
|[FileSystemReadAskForUrls](#filesystemreadaskforurls)|Permitir o acesso de leitura pela API do Sistema de arquivos nesses sites|
|[FileSystemReadBlockedForUrls](#filesystemreadblockedforurls)|Bloquear o acesso de leitura por meio da API do Sistema de arquivos nesses sites|
|[FileSystemWriteAskForUrls](#filesystemwriteaskforurls)|Permitir o acesso de gravação a arquivos e pastas nestes sites|
|[FileSystemWriteBlockedForUrls](#filesystemwriteblockedforurls)|Bloquear o acesso de gravação a arquivos e pastas nestes sites|
|[ImagesAllowedForUrls](#imagesallowedforurls)|Permitir imagens nestes sites|
|[ImagesBlockedForUrls](#imagesblockedforurls)|Bloquear imagens em sites específicos|
|[InsecureContentAllowedForUrls](#insecurecontentallowedforurls)|Permitir conteúdo não seguro em sites especificados|
|[InsecureContentBlockedForUrls](#insecurecontentblockedforurls)|Bloquear conteúdo inseguro em sites especificados|
|[JavaScriptAllowedForUrls](#javascriptallowedforurls)|Permitir JavaScript em sites específicos|
|[JavaScriptBlockedForUrls](#javascriptblockedforurls)|Bloquear o JavaScript em sites específicos|
|[LegacySameSiteCookieBehaviorEnabled](#legacysamesitecookiebehaviorenabled)|Habilita a configuração padrão de cookie herdado SameSite padrão.|
|[LegacySameSiteCookieBehaviorEnabledForDomainList](#legacysamesitecookiebehaviorenabledfordomainlist)|Reverter para o comportamento herdado SameSite para cookies em sites especificados|
|[NotificationsAllowedForUrls](#notificationsallowedforurls)|Permitir notificações em sites específicos|
|[NotificationsBlockedForUrls](#notificationsblockedforurls)|Bloquear notificações em sites específicos|
|[PluginsAllowedForUrls](#pluginsallowedforurls)|Permitir o plug-in Adobe Flash em sites específicos|
|[PluginsBlockedForUrls](#pluginsblockedforurls)|Bloquear o plug-in Adobe Flash em sites específicos|
|[PopupsAllowedForUrls](#popupsallowedforurls)|Permitir janelas pop-up em sites específicos|
|[PopupsBlockedForUrls](#popupsblockedforurls)|Bloquear janelas pop-up em sites específicos|
|[RegisteredProtocolHandlers](#registeredprotocolhandlers)|Registrar manipuladores de protocolo|
|[SpotlightExperiencesAndRecommendationsEnabled](#spotlightexperiencesandrecommendationsenabled)|Escolha se os usuários podem receber imagens de plano de fundo personalizadas e texto, sugestões, notificações,
e dicas para os serviços Microsoft|
|[WebUsbAllowDevicesForUrls](#webusballowdevicesforurls)|Conceder acesso a sites específicos para conectar-se a dispositivos USB específicos|
|[WebUsbAskForUrls](#webusbaskforurls)|Permitir WebUSB em sites específicos|
|[WebUsbBlockedForUrls](#webusbblockedforurls)|Bloquear WebUSB em sites específicos|
### [*Provedor de pesquisa padrão*](#default-search-provider-policies)
|Nome da política|Legenda|
|-|-|
|[DefaultSearchProviderEnabled](#defaultsearchproviderenabled)|Habilitar o provedor de pesquisa padrão|
|[DefaultSearchProviderEncodings](#defaultsearchproviderencodings)|Codificações de provedores de pesquisa padrão|
|[DefaultSearchProviderImageURL](#defaultsearchproviderimageurl)|Especifica o recurso Pesquisar por imagem para o provedor de pesquisa padrão|
|[DefaultSearchProviderImageURLPostParams](#defaultsearchproviderimageurlpostparams)|Parâmetros para uma URL de imagem que usa POST|
|[DefaultSearchProviderKeyword](#defaultsearchproviderkeyword)|Palavra-chave do provedor de pesquisa padrão|
|[DefaultSearchProviderName](#defaultsearchprovidername)|Nome do provedor de pesquisa padrão|
|[DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl)|URL de pesquisa do provedor de pesquisa padrão|
|[DefaultSearchProviderSuggestURL](#defaultsearchprovidersuggesturl)|URL do provedor de pesquisa padrão para sugestões|
|[NewTabPageSearchBox](#newtabpagesearchbox)|Configurar a nova experiência da caixa de pesquisa da página da guia|
### [*Extensões*](#extensions-policies)
|Nome da política|Legenda|
|-|-|
|[ExtensionAllowedTypes](#extensionallowedtypes)|Configurar tipos de extensão permitidas|
|[ExtensionInstallAllowlist](#extensioninstallallowlist)|Permitir que extensões específicas sejam instaladas|
|[ExtensionInstallBlocklist](#extensioninstallblocklist)|Controlar quais extensões não podem ser instaladas|
|[ExtensionInstallForcelist](#extensioninstallforcelist)|Controlar quais extensões são instaladas silenciosamente|
|[ExtensionInstallSources](#extensioninstallsources)|Configurar fontes de instalação de extensão e script de usuário|
|[ExtensionSettings](#extensionsettings)|Definir configurações de gerenciamento de extensão.|
### [*Autenticação HTTP*](#http-authentication-policies)
|Nome da política|Legenda|
|-|-|
|[AllowCrossOriginAuthPrompt](#allowcrossoriginauthprompt)|Permitir solicitações de autenticação HTTP Cross-Origin|
|[AuthNegotiateDelegateAllowlist](#authnegotiatedelegateallowlist)|Especifica uma lista de servidores para os quais o Microsoft Edge pode delegar credenciais de usuário|
|[AuthSchemes](#authschemes)|Esquemas de autenticação com suporte|
|[AuthServerAllowlist](#authserverallowlist)|Configurar a lista de servidores de autenticação permitidos|
|[DisableAuthNegotiateCnameLookup](#disableauthnegotiatecnamelookup)|Desabilitar a pesquisa CNAME durante a negociação da autenticação Kerberos|
|[EnableAuthNegotiatePort](#enableauthnegotiateport)|Incluir porta não padrão no SPN Kerberos|
|[NtlmV2Enabled](#ntlmv2enabled)|Controlar se a autenticação NTLMv2 está habilitada|
### [*Configurações do modo de quiosque*](#kiosk-mode-settings-policies)
|Nome da política|Legenda|
|-|-|
|[KioskDeleteDownloadsOnExit](#kioskdeletedownloadsonexit)|Excluir arquivos baixados como parte de uma sessão Kiosk quando o Microsoft Edge for fechado|
### [*Sistema de mensagens nativo*](#native-messaging-policies)
|Nome da política|Legenda|
|-|-|
|[NativeMessagingAllowlist](#nativemessagingallowlist)|Controlar quais hosts nativos de mensagens os usuários podem usar|
|[NativeMessagingBlocklist](#nativemessagingblocklist)|Configurar lista de bloqueio de mensagens nativas|
|[NativeMessagingUserLevelHosts](#nativemessaginguserlevelhosts)|Permitir hosts de mensagens nativas em nível de usuário (instalado sem permissões de administrador)|
### [*Gerenciador de senhas e proteção*](#password-manager-and-protection-policies)
|Nome da política|Legenda|
|-|-|
|[PasswordManagerEnabled](#passwordmanagerenabled)|Habilitar o salvamento de senhas no gerenciador de senhas|
|[PasswordMonitorAllowed](#passwordmonitorallowed)|Permitir que os usuários sejam alertados caso suas senhas não sejam seguras|
|[PasswordProtectionChangePasswordURL](#passwordprotectionchangepasswordurl)|Configurar a URL de alteração de senha|
|[PasswordProtectionLoginURLs](#passwordprotectionloginurls)|Configurar a lista de URLs de logon corporativos onde o serviço de proteção por senha deve capturar os hashes com sal de uma senha|
|[PasswordProtectionWarningTrigger](#passwordprotectionwarningtrigger)|Configurar o gatilho de aviso de proteção por senha|
### [*Impressão*](#printing-policies)
|Nome da política|Legenda|
|-|-|
|[DefaultPrinterSelection](#defaultprinterselection)|Regras de seleção de impressora padrão|
|[PrintHeaderFooter](#printheaderfooter)|Imprimir cabeçalhos e rodapés|
|[PrintPreviewUseSystemDefaultPrinter](#printpreviewusesystemdefaultprinter)|Definir a impressora padrão do sistema como impressora padrão|
|[PrintingEnabled](#printingenabled)|Habilitar impressão|
|[PrintingPaperSizeDefault](#printingpapersizedefault)|Tamanho da página de impressão padrão|
|[UseSystemPrintDialog](#usesystemprintdialog)|Imprimir usando a caixa de diálogo de impressão do sistema|
### [*Servidor proxy*](#proxy-server-policies)
|Nome da política|Legenda|
|-|-|
|[ProxyBypassList](#proxybypasslist)|Configurar regras de bypass de proxy|
|[ProxyMode](#proxymode)|Definir configurações do servidor proxy.|
|[ProxyPacUrl](#proxypacurl)|Defina o URL do arquivo .pac do proxy|
|[ProxyServer](#proxyserver)|Configurar o endereço ou a URL do servidor proxy|
|[ProxySettings](#proxysettings)|Configurações de proxy|
### [*Configurações do SmartScreen*](#smartscreen-settings-policies)
|Nome da política|Legenda|
|-|-|
|[PreventSmartScreenPromptOverride](#preventsmartscreenpromptoverride)|Evitar ignorar os avisos do Microsoft Defender SmartScreen para sites|
|[PreventSmartScreenPromptOverrideForFiles](#preventsmartscreenpromptoverrideforfiles)|Impedir que os avisos do Microsoft Defender SmartScreen sobre download sejam ignorados|
|[SmartScreenAllowListDomains](#smartscreenallowlistdomains)|Configurar a lista de domínios para os quais o Microsoft Defender SmartScreen não desencadeará avisos|
|[SmartScreenEnabled](#smartscreenenabled)|Configurar o Microsoft Defender SmartScreen|
|[SmartScreenForTrustedDownloadsEnabled](#smartscreenfortrusteddownloadsenabled)|Forçar o Microsoft Defender SmartScreen verifica downloads de fontes confiáveis|
|[SmartScreenPuaEnabled](#smartscreenpuaenabled)|Configura o Microsoft Defender SmartScreen para bloquear aplicativos potencialmente indesejados.|
### [*Página de inicialização&comma; página inicial e nova guia*](#startup-home-page-and-new-tab-page-policies)
|Nome da política|Legenda|
|-|-|
|[HomepageIsNewTabPage](#homepageisnewtabpage)|Definir a nova página da guia como página inicial|
|[HomepageLocation](#homepagelocation)|Configurar a URL da página inicial|
|[NewTabPageAllowedBackgroundTypes](#newtabpageallowedbackgroundtypes)|Configurar os tipos de plano de fundo permitidos para o layout da página nova guia|
|[NewTabPageCompanyLogo](#newtabpagecompanylogo)|Definir logotipo da empresa da página de nova guia (descontinuado)|
|[NewTabPageHideDefaultTopSites](#newtabpagehidedefaulttopsites)|Ocultar os principais sites padrão da página nova guia|
|[NewTabPageLocation](#newtabpagelocation)|Configurar a URL da página nova guia|
|[NewTabPageManagedQuickLinks](#newtabpagemanagedquicklinks)|Definir link rápido de Página Nova Guia|
|[NewTabPagePrerenderEnabled](#newtabpageprerenderenabled)|Habilitar o pré-carregamento da nova página da guia para renderização mais rápida|
|[NewTabPageSetFeedType](#newtabpagesetfeedtype)|Configurar a nova experiência de página da guia Microsoft Edge|
|[RestoreOnStartup](#restoreonstartup)|Ação a ser realizada na inicialização|
|[RestoreOnStartupURLs](#restoreonstartupurls)|Sites a abrir quando o navegador for iniciado|
|[ShowHomeButton](#showhomebutton)|Botão Mostrar página inicial na barra de ferramentas|
### [*Adicional*](#additional-policies)
|Nome da política|Legenda|
|-|-|
|[AddressBarMicrosoftSearchInBingProviderEnabled](#addressbarmicrosoftsearchinbingproviderenabled)|Habilitar a Pesquisa da Microsoft em sugestões do Bing na barra de endereços|
|[AdsSettingForIntrusiveAdsSites](#adssettingforintrusiveadssites)|Configuração Ads para sites com publicidade invasiva|
|[AllowDeletingBrowserHistory](#allowdeletingbrowserhistory)|Habilitar a exclusão do navegador e baixar o histórico|
|[AllowFileSelectionDialogs](#allowfileselectiondialogs)|Permitir diálogos de seleção de arquivo|
|[AllowPopupsDuringPageUnload](#allowpopupsduringpageunload)|Permite que uma página mostre pop-ups durante seu descarregamento|
|[AllowSurfGame](#allowsurfgame)|Permitir a navegação|
|[AllowSyncXHRInPageDismissal](#allowsyncxhrinpagedismissal)|Permitir que as páginas enviem solicitações XHR síncronas durante o descarte da página (preterida)|
|[AllowTokenBindingForUrls](#allowtokenbindingforurls)|Configurar a lista de sites com os quais o Microsoft Edge tentará estabelecer uma Associação de Token.|
|[AllowTrackingForUrls](#allowtrackingforurls)|Configurar exceções de prevenção de rastreamento para sites específicos|
|[AlternateErrorPagesEnabled](#alternateerrorpagesenabled)|Sugerir páginas similares quando uma página da Web não consegue ser encontrada|
|[AlwaysOpenPdfExternally](#alwaysopenpdfexternally)|Sempre abrir arquivos PDF externamente|
|[AmbientAuthenticationInPrivateModesEnabled](#ambientauthenticationinprivatemodesenabled)|Habilitar a autenticação ambiente para perfis InPrivate e Convidado|
|[AppCacheForceEnabled](#appcacheforceenabled)|Permite reabilitar o recurso AppCache, mesmo que ele esteja desativado por padrão|
|[ApplicationLocaleValue](#applicationlocalevalue)|Definir a localidade do aplicativo|
|[AudioCaptureAllowed](#audiocaptureallowed)|Permitir ou bloquear captura de áudio|
|[AudioCaptureAllowedUrls](#audiocaptureallowedurls)|Sites que podem acessar dispositivos de captura de áudio sem solicitar permissão|
|[AudioSandboxEnabled](#audiosandboxenabled)|Permitir a execução da área restrita de áudio|
|[AutoImportAtFirstRun](#autoimportatfirstrun)|Importar automaticamente os dados e as configurações de outro navegador na primeira execução|
|[AutoLaunchProtocolsFromOrigins](#autolaunchprotocolsfromorigins)|Definir uma lista de protocolos que podem iniciar um aplicativo externo de origens listadas sem perguntar ao usuário|
|[AutoOpenAllowedForURLs](#autoopenallowedforurls)|URLs nas quais AutoOpenFileTypes pode aplicar|
|[AutoOpenFileTypes](#autoopenfiletypes)|Lista de tipos de arquivo que devem ser abertos automaticamente no download|
|[AutofillAddressEnabled](#autofilladdressenabled)|Habilitar o preenchimento automático para endereços|
|[AutofillCreditCardEnabled](#autofillcreditcardenabled)|Habilitar o preenchimento automático para cartões de crédito|
|[AutoplayAllowed](#autoplayallowed)|Permitir a reprodução automática de mídia para sites|
|[BackgroundModeEnabled](#backgroundmodeenabled)|Continuar executando aplicativos de segundo plano após o Microsoft Edge ser fechado|
|[BackgroundTemplateListUpdatesEnabled](#backgroundtemplatelistupdatesenabled)|Permite atualizações em segundo plano para a lista de modelos disponíveis para Coleções e outros recursos que usam modelos|
|[BingAdsSuppression](#bingadssuppression)|Bloquear todos os anúncios nos resultados de pesquisa do Bing|
|[BlockThirdPartyCookies](#blockthirdpartycookies)|Bloquear cookies de terceiros|
|[BrowserAddProfileEnabled](#browseraddprofileenabled)|Habilitar a criação de perfil no menu de atalho de identidade ou na página de configurações|
|[BrowserGuestModeEnabled](#browserguestmodeenabled)|Habilitar o modo convidado|
|[BrowserNetworkTimeQueriesEnabled](#browsernetworktimequeriesenabled)|Permitir consultas a um serviço de Hoário da Rede do Navegador|
|[BrowserSignin](#browsersignin)|Configurações de entrada do navegador|
|[BuiltInDnsClientEnabled](#builtindnsclientenabled)|Usar o cliente DNS interno|
|[BuiltinCertificateVerifierEnabled](#builtincertificateverifierenabled)|Determina se o verificador interno de certificado será usado para verificar certificados do servidor (preterido)|
|[CertificateTransparencyEnforcementDisabledForCas](#certificatetransparencyenforcementdisabledforcas)|Desabilitar a imposição da transparência do certificado para obter uma lista de hashes subjectPublicKeyInfo|
|[CertificateTransparencyEnforcementDisabledForLegacyCas](#certificatetransparencyenforcementdisabledforlegacycas)|Desabilitar a imposição da transparência do certificado para uma lista de autoridades de certificação herdadas|
|[CertificateTransparencyEnforcementDisabledForUrls](#certificatetransparencyenforcementdisabledforurls)|Desabilitar a imposição da transparência do certificado para URLs específicas|
|[ClearBrowsingDataOnExit](#clearbrowsingdataonexit)|Limpar os dados da navegação quando o Microsoft Edge é fechado|
|[ClearCachedImagesAndFilesOnExit](#clearcachedimagesandfilesonexit)|Limpar arquivos e imagens armazenadas em cache ao fechar o Microsoft Edge|
|[ClickOnceEnabled](#clickonceenabled)|Permitir que os usuários abram arquivos usando o protocolo ClickOnce|
|[CollectionsServicesAndExportsBlockList](#collectionsservicesandexportsblocklist)|Bloquear o acesso a uma lista especificada de serviços e exportar destinos em Coleções|
|[CommandLineFlagSecurityWarningsEnabled](#commandlineflagsecuritywarningsenabled)|Habilitar avisos de segurança para sinalizadores de linha de comando|
|[ComponentUpdatesEnabled](#componentupdatesenabled)|Habilitar atualizações de componentes no Microsoft Edge|
|[ConfigureDoNotTrack](#configuredonottrack)|Configurar Não Rastrear|
|[ConfigureOnPremisesAccountAutoSignIn](#configureonpremisesaccountautosignin)|Configura o login automático com uma conta de domínio do Active Directory quando não houver nenhuma conta de domínio do Azure AD.|
|[ConfigureOnlineTextToSpeech](#configureonlinetexttospeech)|Configurar Conversão de Texto em Fala online|
|[ConfigureShare](#configureshare)|Configurar a experiência de compartilhamento|
|[CustomHelpLink](#customhelplink)|Especificar um link de ajuda personalizado|
|[DNSInterceptionChecksEnabled](#dnsinterceptionchecksenabled)|Verificações de interceptações DNS habilitadas|
|[DefaultBrowserSettingEnabled](#defaultbrowsersettingenabled)|Definir o Microsoft Edge como o navegador padrão|
|[DefaultSearchProviderContextMenuAccessAllowed](#defaultsearchprovidercontextmenuaccessallowed)|Permitir que o menu de contexto do provedor de pesquisa padrão pesquise no acesso|
|[DefaultSensorsSetting](#defaultsensorssetting)|Configuração de sensores padrão|
|[DefaultSerialGuardSetting](#defaultserialguardsetting)|Controlar o uso da API serial|
|[DelayNavigationsForInitialSiteListDownload](#delaynavigationsforinitialsitelistdownload)|Exigir que a lista de sites no Modo Empresarial esteja disponível antes da navegação na guia|
|[DeleteDataOnMigration](#deletedataonmigration)|Excluir dados antigos do navegador na migração|
|[DeveloperToolsAvailability](#developertoolsavailability)|Controlar onde as ferramentas de desenvolvedor podem ser usadas|
|[DiagnosticData](#diagnosticdata)|Enviar dados de diagnóstico obrigatórios e opcionais referentes ao uso do navegador|
|[DirectInvokeEnabled](#directinvokeenabled)|Permitir que os usuários abram arquivos usando o protocolo DirectInvoke|
|[Disable3DAPIs](#disable3dapis)|Desabilitar o suporte para APIs de gráficos 3D|
|[DisableScreenshots](#disablescreenshots)|Desabilitar a captura de tela|
|[DiskCacheDir](#diskcachedir)|Definir diretório de cache de disco|
|[DiskCacheSize](#diskcachesize)|Definir o tamanho do cache de disco, em bytes|
|[DnsOverHttpsMode](#dnsoverhttpsmode)|Controlar o modo de DNS em HTTPS|
|[DnsOverHttpsTemplates](#dnsoverhttpstemplates)|Especificar o modelo de URI do resolvedor de DNS sobre HTTPS desejado.|
|[DownloadDirectory](#downloaddirectory)|Configurar o diretório de download|
|[DownloadRestrictions](#downloadrestrictions)|Permitir restrições de download|
|[EdgeCollectionsEnabled](#edgecollectionsenabled)|Habilitar o recurso Coleções|
|[EditFavoritesEnabled](#editfavoritesenabled)|Permite que os usuários editem favoritos|
|[EnableDeprecatedWebPlatformFeatures](#enabledeprecatedwebplatformfeatures)|Reabilitar os recursos de plataforma da Web reaprovados por um tempo limitado|
|[EnableDomainActionsDownload](#enabledomainactionsdownload)|Habilitar ações de domínio para download da Microsoft (obsoleta)|
|[EnableOnlineRevocationChecks](#enableonlinerevocationchecks)|Habilitar verificações OCSP/CRL online|
|[EnableSha1ForLocalAnchors](#enablesha1forlocalanchors)|Permitir certificados assinados usando SHA-1 quando emitido por âncoras de confiança local (substituídos)|
|[EnterpriseHardwarePlatformAPIEnabled](#enterprisehardwareplatformapienabled)|Permitir que as extensões gerenciadas usem a API de plataforma de hardware empresarial|
|[EnterpriseModeSiteListManagerAllowed](#enterprisemodesitelistmanagerallowed)|Permitir o acesso à ferramenta Enterprise Mode Site List Manager|
|[ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](#exemptdomainfiletypepairsfromfiletypedownloadwarnings)|Desabilitar o download de avisos com base na extensão de tipo de arquivo para tipos de arquivo especificados em domínios|
|[ExperimentationAndConfigurationServiceControl](#experimentationandconfigurationservicecontrol)|Controlar a comunicação com o serviço de experimentação e configuração|
|[ExternalProtocolDialogShowAlwaysOpenCheckbox](#externalprotocoldialogshowalwaysopencheckbox)|Mostrar a caixa de seleção "sempre aberta" no diálogo de protocolo externo|
|[FamilySafetySettingsEnabled](#familysafetysettingsenabled)|Permitir que os usuários configurem a proteção para a família|
|[FavoritesBarEnabled](#favoritesbarenabled)|Habilitar barra de favoritos|
|[ForceBingSafeSearch](#forcebingsafesearch)|Aplicar a Pesquisa Segura do Bing|
|[ForceCertificatePromptsOnMultipleMatches](#forcecertificatepromptsonmultiplematches)|Configurar se o Microsoft Edge deve selecionar automaticamente um certificado quando houver várias correspondências de certificado para um site configurado com "AutoSelectCertificateForUrls"|
|[ForceEphemeralProfiles](#forceephemeralprofiles)|Habilitar o uso de perfis efêmeros|
|[ForceGoogleSafeSearch](#forcegooglesafesearch)|Aplicar a Pesquisa Segura do Google|
|[ForceLegacyDefaultReferrerPolicy](#forcelegacydefaultreferrerpolicy)|Usa uma política referencial padrão de no-referrer-when-downgrade (preterida)|
|[ForceNetworkInProcess](#forcenetworkinprocess)|Forçar o código de rede a executar no processo do navegador (obsoleta)|
|[ForceSync](#forcesync)|Forçar a sincronização dos dados do navegador e não mostrar o aviso de consentimento da sincronização|
|[ForceYouTubeRestrict](#forceyoutuberestrict)|Forçar o modo restrito mínimo do YouTube|
|[FullscreenAllowed](#fullscreenallowed)|Permitir o modo de tela inteira|
|[GloballyScopeHTTPAuthCacheEnabled](#globallyscopehttpauthcacheenabled)|Habilitar o cache de autenticação HTTP globalmente em escopo|
|[GoToIntranetSiteForSingleWordEntryInAddressBar](#gotointranetsiteforsinglewordentryinaddressbar)|Forçar a navegação direta no site da intranet, em vez de pesquisar em entradas de palavras únicas na barra de endereços|
|[HSTSPolicyBypassList](#hstspolicybypasslist)|Configurar a lista de nomes que ignorarão a verificação de política HSTS|
|[HardwareAccelerationModeEnabled](#hardwareaccelerationmodeenabled)|Usar a aceleração de hardware quando disponível|
|[HideFirstRunExperience](#hidefirstrunexperience)|Oculta a experiência de Primeira execução e a tela inicial.|
|[ImportAutofillFormData](#importautofillformdata)|Permitir a importação de dados do formulário de Preenchimento automático|
|[ImportBrowserSettings](#importbrowsersettings)|Permitir a importação de configurações do navegador|
|[ImportCookies](#importcookies)|Permitir a importação de cookies|
|[ImportExtensions](#importextensions)|Permitir a importação de extensões|
|[ImportFavorites](#importfavorites)|Permitir a importação de favoritos|
|[ImportHistory](#importhistory)|Permitir a importação do histórico de navegação|
|[ImportHomepage](#importhomepage)|Permitir a importação de configurações da página inicial|
|[ImportOpenTabs](#importopentabs)|Permitir a importação de guias abertas|
|[ImportPaymentInfo](#importpaymentinfo)|Permitir a importação de informações de pagamento|
|[ImportSavedPasswords](#importsavedpasswords)|Permitir a importação de senhas salvas|
|[ImportSearchEngine](#importsearchengine)|Permitir a importação das configurações do mecanismo de pesquisa|
|[ImportShortcuts](#importshortcuts)|Permitir a importação de atalhos|
|[InPrivateModeAvailability](#inprivatemodeavailability)|Configurar a disponibilidade do modo InPrivate|
|[InsecureFormsWarningsEnabled](#insecureformswarningsenabled)|Habilitar avisos para formulários inseguros|
|[IntensiveWakeUpThrottlingEnabled](#intensivewakeupthrottlingenabled)|Controlar o recurso IntensiveWakeUpThrottling|
|[InternetExplorerIntegrationEnhancedHangDetection](#internetexplorerintegrationenhancedhangdetection)|Configurar a detecção de trava avançada para o modo do Internet Explorer|
|[InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel)|Configurar a integração do Internet Explorer|
|[InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist)|Configurar a lista de sites do modo Empresarial|
|[InternetExplorerIntegrationSiteRedirect](#internetexplorerintegrationsiteredirect)|Especificar como as navegações "na página" para sites não configurados se comportam quando iniciadas nas páginas do modo Internet Explorer.|
|[InternetExplorerIntegrationTestingAllowed](#internetexplorerintegrationtestingallowed)|Permitir teste no modo Internet Explorer|
|[IsolateOrigins](#isolateorigins)|Habilitar o isolamento de sites para determinadas origens|
|[LocalProvidersEnabled](#localprovidersenabled)|Permitir sugestões de provedores locais|
|[ManagedFavorites](#managedfavorites)|Configurar Favoritos|
|[ManagedSearchEngines](#managedsearchengines)|Gerenciar mecanismos de pesquisa|
|[MaxConnectionsPerProxy](#maxconnectionsperproxy)|Número máximo de conexões simultâneas com o servidor proxy|
|[MediaRouterCastAllowAllIPs](#mediaroutercastallowallips)|Permitir que o Google Cast se conecte a dispositivos de conversão em todos os endereços IP|
|[MetricsReportingEnabled](#metricsreportingenabled)|Habilitar a geração de relatórios de dados de uso e relacionados a falhas (descontinuada)|
|[NativeWindowOcclusionEnabled](#nativewindowocclusionenabled)|Habilitar Native Window Occlusion|
|[NavigationDelayForInitialSiteListDownloadTimeout](#navigationdelayforinitialsitelistdownloadtimeout)|Definir um tempo limite para o atraso da navegação da guia para a lista de sites do Modo Empresarial|
|[NetworkPredictionOptions](#networkpredictionoptions)|Habilitar a previsão de rede|
|[NonRemovableProfileEnabled](#nonremovableprofileenabled)|Configurar se um usuário sempre tem um perfil padrão conectado automaticamente à sua conta corporativa ou de estudante|
|[OverrideSecurityRestrictionsOnInsecureOrigin](#overridesecurityrestrictionsoninsecureorigin)|Controle onde as restrições de segurança em origens inseguras se aplicam|
|[PaymentMethodQueryEnabled](#paymentmethodqueryenabled)|Permitir que os sites pesquisem os métodos de pagamento disponíveis|
|[PersonalizationReportingEnabled](#personalizationreportingenabled)|Permite a personalização de anúncios, pesquisas e notícias enviando o histórico de navegação à Microsoft.|
|[PinningWizardAllowed](#pinningwizardallowed)|Permitir fixar o assistente na barra de tarefas|
|[ProactiveAuthEnabled](#proactiveauthenabled)|Habilitar a autenticação Proativa|
|[PromotionalTabsEnabled](#promotionaltabsenabled)|Habilitar o conteúdo promocional em uma guia|
|[PromptForDownloadLocation](#promptfordownloadlocation)|Perguntar onde salvar os arquivos baixados|
|[QuicAllowed](#quicallowed)|Permitir protocolo QUIC|
|[RelaunchNotification](#relaunchnotification)|Notificar um usuário que uma reinicialização do navegador é recomendada ou necessária para atualizações pendentes|
|[RelaunchNotificationPeriod](#relaunchnotificationperiod)|Definir o período de tempo das notificações de atualização|
|[RendererCodeIntegrityEnabled](#renderercodeintegrityenabled)|Habilitar integridade de código de renderizador|
|[RequireOnlineRevocationChecksForLocalAnchors](#requireonlinerevocationchecksforlocalanchors)|Especificar se serão necessárias verificações OCSP/CRL online para âncoras de confiança locais|
|[ResolveNavigationErrorsUseWebService](#resolvenavigationerrorsusewebservice)|Habilitar a resolução de erros de navegação usando um serviço Web|
|[RestrictSigninToPattern](#restrictsignintopattern)|Restringir quais contas podem ser usadas como contas principais do Microsoft Edge|
|[RoamingProfileLocation](#roamingprofilelocation)|Configurar o diretório de perfil móvel|
|[RoamingProfileSupportEnabled](#roamingprofilesupportenabled)|Habilitar o uso de cópias de roaming para dados de perfil do Microsoft Edge|
|[RunAllFlashInAllowMode](#runallflashinallowmode)|Estender a configuração de conteúdo do Adobe Flash a todo o conteúdo|
|[SSLErrorOverrideAllowed](#sslerroroverrideallowed)|Permitir que os usuários continuem a partir da página de aviso de HTTPS|
|[SSLVersionMin](#sslversionmin)|Versão mínima do TLS habilitada|
|[SaveCookiesOnExit](#savecookiesonexit)|Salvar os cookies ao fechar o Microsoft Edge|
|[SavingBrowserHistoryDisabled](#savingbrowserhistorydisabled)|Desabilitar o salvamento do histórico do navegador|
|[ScreenCaptureAllowed](#screencaptureallowed)|Permitir ou negar captura de tela|
|[ScrollToTextFragmentEnabled](#scrolltotextfragmentenabled)|Ativar a rolagem para o texto especificado nos fragmentos de URL.|
|[SearchSuggestEnabled](#searchsuggestenabled)|Permitir sugestões de pesquisa|
|[SecurityKeyPermitAttestation](#securitykeypermitattestation)|Sites ou domínios que não precisam de permissão para usar o atestado de chave de segurança direta|
|[SendIntranetToInternetExplorer](#sendintranettointernetexplorer)|Enviar todos os sites da intranet para o Internet Explorer|
|[SendSiteInfoToImproveServices](#sendsiteinfotoimproveservices)|Enviar informações de sites para aprimorar os serviços da Microsoft (descontinuado)|
|[SensorsAllowedForUrls](#sensorsallowedforurls)|Permitir o acesso a sensores em sites específicos|
|[SensorsBlockedForUrls](#sensorsblockedforurls)|Bloquear o acesso a sensores em sites específicos|
|[SerialAskForUrls](#serialaskforurls)|Permitir a API serial em sites específicos|
|[SerialBlockedForUrls](#serialblockedforurls)|Bloquear a API serial em sites específicos|
|[ShowOfficeShortcutInFavoritesBar](#showofficeshortcutinfavoritesbar)|Exibir o atalho do Microsoft Office na barra de favoritos (obsoleto)|
|[SignedHTTPExchangeEnabled](#signedhttpexchangeenabled)|Habilitar o suporte para o Exchange HTTP (SXG) assinado|
|[SitePerProcess](#siteperprocess)|Habilitar o isolamento de sites para todos os sites|
|[SpellcheckEnabled](#spellcheckenabled)|Habilitar verificação ortográfica|
|[SpellcheckLanguage](#spellchecklanguage)|Habilitar idiomas de verificação ortográfica específicos|
|[SpellcheckLanguageBlocklist](#spellchecklanguageblocklist)|Forçar a desabilitação de idiomas de verificação ortográfica|
|[StricterMixedContentTreatmentEnabled](#strictermixedcontenttreatmentenabled)|Habilitar tratamento mais estrito para conteúdo misto (preterido)|
|[SuppressUnsupportedOSWarning](#suppressunsupportedoswarning)|Suprimir o aviso do sistema operacional sem suporte|
|[SyncDisabled](#syncdisabled)|Desabilitar a sincronização de dados usando o Microsoft Sync Services|
|[SyncTypesListDisabled](#synctypeslistdisabled)|Configurar a lista de tipos excluídos da sincronização.|
|[TLS13HardeningForLocalAnchorsEnabled](#tls13hardeningforlocalanchorsenabled)|Habilitar um recurso de segurança TLS 1.3 para âncoras de confiança locais (obsoleto)|
|[TLSCipherSuiteDenyList](#tlsciphersuitedenylist)|Especificar os pacotes de codificação TLS para desabilitar|
|[TabFreezingEnabled](#tabfreezingenabled)|Permitir congelamento das guias de plano de fundo|
|[TaskManagerEndProcessEnabled](#taskmanagerendprocessenabled)|Habilitar processos finais no Gerenciador de tarefas do navegador|
|[TotalMemoryLimitMb](#totalmemorylimitmb)|Definir o limite em megabytes de memória que uma única instância do Microsoft Edge pode usar.|
|[TrackingPrevention](#trackingprevention)|Bloquear o acompanhamento de atividades de navegação na Web do usuário|
|[TranslateEnabled](#translateenabled)|Habilitar traduzir|
|[URLAllowlist](#urlallowlist)|Definir uma lista de URLs permitidas|
|[URLBlocklist](#urlblocklist)|Bloquear o acesso a uma lista de URLs|
|[UserAgentClientHintsEnabled](#useragentclienthintsenabled)|Habilitar o recurso de Dicas do Cliente Usuário-Agente (descontinuado)|
|[UserDataDir](#userdatadir)|Definir o diretório de dados de usuário|
|[UserDataSnapshotRetentionLimit](#userdatasnapshotretentionlimit)|Limita o número de instantâneos de dados do usuário mantidos para uso no caso de uma reversão de emergência|
|[UserFeedbackAllowed](#userfeedbackallowed)|Permitir comentários do usuário|
|[VideoCaptureAllowed](#videocaptureallowed)|Permitir ou bloquear captura de vídeo|
|[VideoCaptureAllowedUrls](#videocaptureallowedurls)|Sites que podem acessar dispositivos de captura de vídeo sem solicitar permissão|
|[WPADQuickCheckEnabled](#wpadquickcheckenabled)|Definir otimização de WPAD|
|[WebAppInstallForceList](#webappinstallforcelist)|Configura a lista de aplicativos Web instalados pela força.|
|[WebComponentsV0Enabled](#webcomponentsv0enabled)|Reabilitar a API de componentes Web V0 até M84 (obsoleta)|
|[WebDriverOverridesIncompatiblePolicies](#webdriveroverridesincompatiblepolicies)|Permitir que o WebDriver substitua políticas incompatíveis (obsoleta)|
|[WebRtcLocalIpsAllowedUrls](#webrtclocalipsallowedurls)|Gerenciar a exposição de endereço IP local por WebRTC|
|[WebRtcLocalhostIpHandling](#webrtclocalhostiphandling)|Restringir a exposição de endereço IP local por WebRTC|
|[WebRtcUdpPortRange](#webrtcudpportrange)|Restringir o intervalo de portas UDP locais usado por WebRTC|
|[WinHttpProxyResolverEnabled](#winhttpproxyresolverenabled)|Usar o solucionador de proxy do Windows (preterida)|




  ## Políticas de configurações do Application Guard

  [Voltar ao início](#microsoft-edge---policies)

  ### ApplicationGuardContainerProxy
  #### Proxy de contêiner do Application Guard
  
  
  #### Versões com suporte:
  - No Windows desde 84 ou posterior

  #### Descrição
  Define as configurações de proxy para o Microsoft Edge Application Guard.
Se você habilitar essa política, o Microsoft Edge Application Guard ignorará outras fontes de configurações de proxy.

Se você não configurar essa política, o Microsoft Edge Application Guard usará a configuração de proxy do host.

Essa política não afeta a configuração de proxy do Microsoft Edge fora do Application Guard (no host).

O campo Proxymode permite especificar o servidor proxy usado pelo Microsoft Edge Application Guard.

O campo ProxyPacUrl é uma URL para um arquivo .pac de proxy.

O campo ProxyServer é uma URL para o servidor proxy.

Se você escolher o valor 'direto' como "Proxymode", todos os outros campos serão ignorados.

Se você escolher o valor ' auto_detect ' como "Proxymode", todos os outros campos são ignorados.

Se você escolher o valor 'fixed_server ' como "Proxymode", o campo "ProxyServer" será usado.

Se você escolher o valor 'pac_script ' como "Proxymode", o campo "ProxyPacUrl" será usado.

Para saber mais sobre como identificar o tráfego do Application Guard por proxy duplo, acesse [https://go.microsoft.com/fwlink/?linkid=2134653](https://go.microsoft.com/fwlink/?linkid=2134653).

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: não requer a reinicialização do navegador

  #### Tipo de dados:
  - Dictionary

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: ApplicationGuardContainerProxy
  - Nome da Política de Grupo: Proxy de Contêiner do Application Guard
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/Application Guard settings
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: ApplicationGuardContainerProxy
  - Tipo do valor: REG_SZ
  ##### Valor de exemplo:
```
SOFTWARE\Policies\Microsoft\Edge\ApplicationGuardContainerProxy = {
  "ProxyMode": "direct", 
  "ProxyPacUrl": "https://internal.site/example.pac", 
  "ProxyServer": "123.123.123.123:8080"
}
```


  

  [Voltar ao início](#microsoft-edge---policies)

  ## Políticas de conversão

  [Voltar ao início](#microsoft-edge---policies)

  ### EnableMediaRouter
  #### Habilitar o Google Cast
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Habilite essa política para habilitar o Google Cast. Os usuários podem iniciá-lo no menu aplicativo, nos menus de contexto de página, nos controles de mídia em sites habilitados para conversão e (se mostrado) no ícone de barra de ferramentas Cast.

Desabilitar esta política para desabilitar o Google Cast.

Por padrão, o Google Cast está habilitado.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: não requer a reinicialização do navegador

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: EnableMediaRouter
  - Nome da Política de Grupo: habilitar o Google Cast
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/Cast
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: EnableMediaRouter
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: EnableMediaRouter
  - Valor de exemplo:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### ShowCastIconInToolbar
  #### Mostrar o ícone de conversão na barra de ferramentas
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Defina essa política como verdadeira para mostrar o ícone da barra de ferramentas Cast na barra de ferramentas ou no menu estouro. Os usuários não conseguirão removê-la.

Se você não configurar essa política ou se desabilitá-la, os usuários poderão fixar ou remover o ícone usando seu menu contextual.

Se você também tiver definido a política [EnableMediaRouter](#enablemediarouter) como falsa, essa política será ignorada, e o ícone da barra de ferramentas não será exibido.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: não requer a reinicialização do navegador

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: ShowCastIconInToolbar
  - Nome da Política de Grupo: Mostrar o ícone de conversão na barra de ferramentas
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/Cast
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: ShowCastIconInToolbar
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000000
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ShowCastIconInToolbar
  - Valor de exemplo:
``` xml
<false/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ## Políticas de configurações de conteúdo

  [Voltar ao início](#microsoft-edge---policies)

  ### AutoSelectCertificateForUrls
  #### Selecionar automaticamente os certificados de cliente para esses sites
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  A configuração da política permite que você faça uma lista de padrões de URL que especificam sites para os quais o Microsoft Edge pode selecionar automaticamente um certificado de cliente. O valor é uma matriz de dicionários estringidos JSON, cada uma com o formato {"Pattern": "$URL _PATTERN", "Filter": $FILTER}, onde $URL _PATTERN é um padrão de configuração de conteúdo. $FILTER restringe os certificados de cliente para os quais o navegador seleciona automaticamente. Independente do filtro, somente os certificados que correspondem à solicitação de certificado do servidor serão selecionados.

Exemplos de uso da $FILTER seção:

* Quando a $FILTER está definida como {"EMISSOR": {"CN": "$ISSUER _CN"}}, somente os certificados do cliente emitidos por um certificado com a $ISSUER _CN devem ser selecionados.

* Quando $FILTER contém as seções "EMISSOR" e "ASSUNTO", somente os certificados de cliente que atendem a ambas as condições são selecionados.

* Quando $FILTER contém uma seção "ASSUNTO" com o valor "O", um certificado precisa que pelo menos uma organização corresponda ao valor especificado a ser selecionado.

* Quando $FILTER contém uma seção "assunto" com um valor de "OU", um certificado precisa ter pelo menos uma unidade organizacional que corresponda ao valor especificado a ser selecionado.

* Quando $FILTER está definida como {}, a seleção de certificados de cliente não é restringida também. Observe que os filtros fornecidos pelo servidor Web ainda se aplicam.

Se você deixar a política não definida, não há nenhuma autoseleção para qualquer site.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: AutoSelectCertificateForUrls
  - Nome da Política de Grupo: Selecionar automaticamente os certificados de cliente para esses sites
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/Content settings
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge\AutoSelectCertificateForUrls
  - Caminho (recomendado): N/A
  - Nome do valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de exemplo:
```
SOFTWARE\Policies\Microsoft\Edge\AutoSelectCertificateForUrls\1 = "{\"pattern\":\"https://www.contoso.com\",\"filter\":{\"ISSUER\":{\"CN\":\"certificate issuer name\", \"L\": \"certificate issuer location\", \"O\": \"certificate issuer org\", \"OU\": \"certificate issuer org unit\"}, \"SUBJECT\":{\"CN\":\"certificate subject name\", \"L\": \"certificate subject location\", \"O\": \"certificate subject org\", \"OU\": \"certificate subject org unit\"}}}"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: AutoSelectCertificateForUrls
  - Valor de exemplo:
``` xml
<array>
  <string>{"pattern":"https://www.contoso.com","filter":{"ISSUER":{"CN":"certificate issuer name", "L": "certificate issuer location", "O": "certificate issuer org", "OU": "certificate issuer org unit"}, "SUBJECT":{"CN":"certificate subject name", "L": "certificate subject location", "O": "certificate subject org", "OU": "certificate subject org unit"}}}</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### CookiesAllowedForUrls
  #### Permitir cookies em sites específicos
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Defina uma lista de sites, com base em padrões de URL, que podem definir cookies.

Se você não configurar essa política, o valor padrão global da diretiva [DefaultCookiesSetting](#defaultcookiessetting) (se definida) ou a configuração pessoal do usuário será usada para todos os sites.

Confira as políticas [CookiesBlockedForUrls](#cookiesblockedforurls) e [CookiesSessionOnlyForUrls](#cookiessessiononlyforurls) para obter mais informações.

Observe que não é possível definir padrões de URL conflitantes entre essas três políticas:

- [CookiesBlockedForUrls](#cookiesblockedforurls)

- CookiesAllowedForUrls

- [CookiesSessionOnlyForUrls](#cookiessessiononlyforurls)

Para impedir que os cookies sejam excluídos na saída, configure a política [SaveCookiesOnExit](#savecookiesonexit).

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: CookiesAllowedForUrls
  - Nome da Política de Grupo: permitir cookies em sites específicos
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/Content settings
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge\CookiesAllowedForUrls
  - Caminho (recomendado): N/A
  - Nome do valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de exemplo:
```
SOFTWARE\Policies\Microsoft\Edge\CookiesAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\CookiesAllowedForUrls\2 = "[*.]contoso.edu"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: CookiesAllowedForUrls
  - Valor de exemplo:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### CookiesBlockedForUrls
  #### Bloquear cookies em sites específicos
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Defina uma lista de sites, com base em padrões de URL, que não podem definir cookies.

Se você não configurar essa política, o valor padrão global da diretiva [DefaultCookiesSetting](#defaultcookiessetting) (se definida) ou a configuração pessoal do usuário será usada para todos os sites.

Confira as políticas [CookiesAllowedForUrls](#cookiesallowedforurls) e [CookiesSessionOnlyForUrls](#cookiessessiononlyforurls) para obter mais informações.

Observe que não é possível definir padrões de URL conflitantes entre essas três políticas:

- CookiesBlockedForUrls

- [CookiesAllowedForUrls](#cookiesallowedforurls)

- [CookiesSessionOnlyForUrls](#cookiessessiononlyforurls)

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: CookiesBlockedForUrls
  - Nome da Política de Grupo: Bloquear cookies em sites específicos
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/Content settings
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge\CookiesBlockedForUrls
  - Caminho (recomendado): N/A
  - Nome do valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de exemplo:
```
SOFTWARE\Policies\Microsoft\Edge\CookiesBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\CookiesBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: CookiesBlockedForUrls
  - Valor de exemplo:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### CookiesSessionOnlyForUrls
  #### Limitar cookies de sites específicos para a sessão atual
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Os cookies criados por sites que correspondem a um padrão de URL que você definir serão excluídos quando a sessão terminar (quando a janela for fechada).

Os cookies criados por sites que não correspondem ao padrão são controlados pela política [DefaultCookiesSetting](#defaultcookiessetting) (se definida) ou pela configuração pessoal do usuário. Esse também é o comportamento padrão se você não configurar essa política.

Se o Microsoft Edge estiver sendo executado em modo de tela de fundo, a sessão pode não fechar quando a última janela é fechada, o que significa que os cookies não serão limpos quando a janela for fechada. Confira a política [BackgroundModeEnabled](#backgroundmodeenabled) para saber mais sobre como configurar o que acontece quando o Microsoft Edge é executado em segundo plano.

Você também pode usar as políticas [CookiesAllowedForUrls](#cookiesallowedforurls) e [CookiesBlockedForUrls](#cookiesblockedforurls) para controlar quais sites podem criar cookies.

Observe que não é possível definir padrões de URL conflitantes entre essas três políticas:

- [CookiesBlockedForUrls](#cookiesblockedforurls)

- [CookiesAllowedForUrls](#cookiesallowedforurls)

- CookiesSessionOnlyForUrls

Se você definir a política [RestoreOnStartup](#restoreonstartup) para restaurar URLs de sessões anteriores, essa política será ignorada e os cookies serão armazenados permanentemente para esses sites.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: CookiesSessionOnlyForUrls
  - Nome da Política de Grupo: limitar cookies de sites específicos para a sessão atual
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/Content settings
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge\CookiesSessionOnlyForUrls
  - Caminho (recomendado): N/A
  - Nome do valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de exemplo:
```
SOFTWARE\Policies\Microsoft\Edge\CookiesSessionOnlyForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\CookiesSessionOnlyForUrls\2 = "[*.]contoso.edu"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: CookiesSessionOnlyForUrls
  - Valor de exemplo:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### DefaultCookiesSetting
  #### Configurar cookies
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Controlar se os sites podem criar cookies no dispositivo do usuário. Essa política é tudo ou nada: você pode permitir que todos os sites criem cookies ou que nenhum site crie cookies. Não é possível usar essa política para habilitar cookies de sites específicos.

Defina a política como ' SessionOnly ' para limpar os cookies quando a sessão for fechada. Se o Microsoft Edge estiver sendo executado em modo de tela de fundo, a sessão pode não fechar quando a última janela é fechada, o que significa que os cookies não serão limpos quando a janela for fechada. Confira a política [BackgroundModeEnabled](#backgroundmodeenabled) para saber mais sobre como configurar o que acontece quando o Microsoft Edge é executado em segundo plano.

Se você não configurar essa política, o padrão "AllowCookies" será usado, e os usuários poderão alterar essa configuração em Configurações do Microsoft Edge. (Se você não quiser que os usuários possam alterar essa configuração, defina a política.)

Mapeamento das opções de política:

* AllowCookies (1) = Permitir que todos os sites criem cookies

* BlockCookies (2) = Não permitir que nenhum site crie cookies

* SessionOnly (4) = Manter os cookies apenas durante a sessão, com exceção dos listados em [SaveCookiesOnExit](#savecookiesonexit) 

Use as informações anteriores ao configurar essa política.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Inteiro

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: DefaultCookiesSetting
  - Nome da Política de Grupo: Configurar cookies
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/Content settings
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: DefaultCookiesSetting
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: DefaultCookiesSetting
  - Valor de exemplo:
``` xml
<integer>1</integer>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### DefaultFileSystemReadGuardSetting
  #### Controlar o uso da API do Sistema de arquivos para leitura
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 86 ou mais recente

  #### Descrição
  Se você definir esta política como 3, os sites poderão solicitar acesso de leitura ao sistema de arquivos do sistema operacional do host usando a API do Sistema de arquivos. Se você definir esta política como 2, o acesso será negado.

Se você não definir esta política, os sites poderão solicitar acesso. Você pode alterar esta configuração.

Mapeamento das opções de política:

* BlockFileSystemRead (2) = Não permitir que os sites solicitem acesso de leitura a arquivos e diretórios por meio da API do Sistema de arquivos

* AskFileSystemRead (3) = Permitir que os sites peçam ao usuário para conceder acesso de leitura a arquivos e diretórios por meio da API do Sistema de arquivos

Use as informações anteriores ao configurar essa política.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Inteiro

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: DefaultFileSystemReadGuardSetting
  - Nome da Política de Grupo: Controlar o uso da API do Sistema de arquivos para leitura
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/Content settings
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do Valor: DefaultFileSystemReadGuardSetting
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000002
```


  #### Informações e configurações do Mac
  - Nome da Chave de Preferência: DefaultFileSystemReadGuardSetting
  - Valor de exemplo:
``` xml
<integer>2</integer>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### DefaultFileSystemWriteGuardSetting
  #### Controlar o uso da API do Sistema de arquivos para gravação
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 86 ou mais recente

  #### Descrição
  Se você definir esta política como 3, os sites poderão solicitar acesso de gravação ao sistema de arquivos do sistema operacional do host usando a API do Sistema de arquivos. Se você definir esta política como 2, o acesso será negado.

Se você não definir esta política, os sites poderão solicitar acesso. Você pode alterar esta configuração.

Mapeamento das opções de política:

* BlockFileSystemWrite (2) = Não permitir que os sites solicitem acesso de leitura a arquivos e diretórios

* AskFileSystemWrite (3) = Permitir que os sites peçam ao usuário para conceder acesso de leitura a arquivos e diretórios

Use as informações anteriores ao configurar essa política.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Inteiro

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: DefaultFileSystemWriteGuardSetting
  - Nome da Política de Grupo: Controlar o uso da API do Sistema de arquivos para gravação
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/Content settings
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: DefaultFileSystemWriteGuardSetting
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000002
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: DefaultFileSystemWriteGuardSetting
  - Valor de exemplo:
``` xml
<integer>2</integer>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### DefaultGeolocationSetting
  #### Configuração de geolocalização padrão
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Defina se os sites podem controlar os locais físicos dos usuários. Você pode permitir o controle por padrão ('AllowGeolocation'), negar por padrão ('BlockGeolocation') ou perguntar ao usuário sempre que um site solicitar seu local ('AskGeolocation').

Se você não configurar essa política, a política "AskGeolocation" será usada e o usuário poderá alterá-la.

Mapeamento das opções de política:

* AllowGeolocation (1) = Permitir que os sites rastreiem a localização dos usuários

* BlockGeolocation (2) = Não permitir que nenhum site rastreie a localização dos usuários

* AskGeolocation (3) = Perguntar sempre que um site desejar rastrear a localização dos usuários

Use as informações anteriores ao configurar essa política.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Inteiro

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: DefaultGeolocationSetting
  - Nome da Política de Grupo: Configuração de geolocalização padrão
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/Content settings
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: DefaultGeolocationSetting
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: DefaultGeolocationSetting
  - Valor de exemplo:
``` xml
<integer>1</integer>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### DefaultImagesSetting
  #### Configuração de imagens padrão
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Defina se os sites podem exibir imagens. Você pode permitir imagens em todos os sites ('AllowImages') ou bloqueá-las em todos os sites ('BlockImages').

Se você não configurar essa política, as imagens serão permitidas por padrão, e o usuário poderá alterar essa configuração.

Mapeamento das opções de política:

* AllowImages (1) = Permitir que todos os sites mostrem todas as imagens

* BlockImages (2) = Não permitir que sites exibam imagens

Use as informações anteriores ao configurar essa política.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Inteiro

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: DefaultImagesSetting
  - Nome da Política de Grupo: Configuração de imagens padrão
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/Content settings
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: DefaultImagesSetting
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: DefaultImagesSetting
  - Valor de exemplo:
``` xml
<integer>1</integer>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### DefaultInsecureContentSetting
  #### Controlar o uso de exceções de conteúdo não seguro
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 80 ou mais recente

  #### Descrição
  Permite definir se os usuários podem adicionar exceções para permitir conteúdo misto de sites específicos.

Essa política pode ser substituída por padrões de URL específicos usando as políticas [InsecureContentAllowedForUrls](#insecurecontentallowedforurls) e [InsecureContentBlockedForUrls](#insecurecontentblockedforurls).

Se essa política não estiver definida, os usuários poderão adicionar exceções para permitir conteúdos em formato misto e desabilitar as auto-atualizações para conteúdos mistos bloqueados opcionalmente.

Mapeamento das opções de política:

* BlockInsecureContent (2) = Não permitir que os sites carreguem conteúdo misto bloqueado

* AllowExceptionsInsecureContent (3) = Permitir que os usuários adicionem exceções para permitir conteúdo misto

Use as informações anteriores ao configurar essa política.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Inteiro

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo:DefaultInsecureContentSetting
  - Nome da Política de Grupo: Controlar o uso de exceções de conteúdo não seguro
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/Content settings
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: DefaultInsecureContentSetting
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000002
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: DefaultInsecureContentSetting
  - Valor de exemplo:
``` xml
<integer>2</integer>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### DefaultJavaScriptSetting
  #### Configuração padrão de JavaScript
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Definir se os sites podem executar o JavaScript. Você pode permitir para todos os sites ('AllowJavaScript') ou bloquear para todos os sites ('BlockJavaScript').

Se você não configurar essa política, todos os sites podem executar o JavaScript por padrão, e o usuário pode alterar essa configuração.

Mapeamento das opções de política:

* AllowJavaScript (1) = Permitir que todos os sites executem JavaScript

* BlockJavaScript (2) = Não permitir que nenhum site execute JavaScript

Use as informações anteriores ao configurar essa política.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Inteiro

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: DefaultJavaScriptSetting
  - Nome da Política de Grupo: configuração padrão de JavaScript
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/Content settings
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: DefaultJavaScriptSetting
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: DefaultJavaScriptSetting
  - Valor de exemplo:
``` xml
<integer>1</integer>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### DefaultNotificationsSetting
  #### Configuração de notificação padrão
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Defina se os sites podem exibir as notificações da área de trabalho. Você pode permiti-los por padrão ('AllowNotifications'), os negá-los por padrão ('BlockNotifications') ou a cada vez que o site deseja mostrar uma notificação ('AskNotifications').

Se você não configurar essa política, as notificações serão permitidas por padrão, e o usuário poderá alterar essa configuração.

Mapeamento das opções de política:

* AllowNotifications (1) = Permitir que os sites mostrem notificações da área de trabalho

* BlockNotifications (2) = Não permitir que nenhum site mostre notificações da área de trabalho

* AskNotifications (3) = Perguntar sempre que um site deseja mostrar as notificações da área de trabalho

Use as informações anteriores ao configurar essa política.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Inteiro

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: DefaultNotificationsSetting
  - Nome da Política de Grupo: Configuração de notificação padrão
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/Content settings
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: DefaultNotificationsSetting
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000002
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: DefaultNotificationsSetting
  - Valor de exemplo:
``` xml
<integer>2</integer>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### DefaultPluginsSetting
  #### Configuração padrão do Adobe Flash
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  [PluginsAllowedForUrls](#pluginsallowedforurls) e [PluginsBlockedForUrls](#pluginsblockedforurls) são verificados primeiro e, em seguida, esta política. As opções são 'ClickToPlay' e 'BlockPlugins'. Se você definir essa política como 'BlockPlugins', esse plug-in será negado para todos os sites. 'ClickToPlay' permite a execução do plug-in do Flash, mas os usuários clicam no espaço reservado para iniciá-lo.

Se você não configurar essa política, o usuário poderá alterar essa configuração manualmente.

Observação: a reprodução automática só é permitida para domínios explicitamente listados na política [PluginsAllowedForUrls](#pluginsallowedforurls). Para ativar a reprodução automática para todos os sites, adicione http://* e https://* à lista de URLs permitidas.

Mapeamento das opções de política:

* BlockPlugins (2) = Bloquear o plug-in Adobe Flash

* ClickToPlay (3) = Clique para executar

Use as informações anteriores ao configurar essa política.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Inteiro

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: DefaultPluginsSetting
  - Nome da Política de Grupo: Configuração padrão do Adobe Flash
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/Content settings
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: DefaultPluginsSetting
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000002
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: DefaultPluginsSetting
  - Valor de exemplo:
``` xml
<integer>2</integer>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### DefaultPopupsSetting
  #### Configuração da janela pop-up padrão
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Defina se os sites podem mostrar janelas pop-up. Você pode permiti-los em todos os sites ('AllowPopups') ou bloqueá-los em todos os sites ('BlockPopups').

Se você não configurar essa política, janelas pop-up serão bloqueadas por padrão, e os usuários poderão alterar essa configuração.

Mapeamento das opções de política:

* AllowPopups (1) = Permitir que todos os sites exibam pop-ups

* BlockPopups (2) = Não permitir que nenhum site mostre pop-ups

Use as informações anteriores ao configurar essa política.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Inteiro

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: DefaultPopupsSetting
  - Nome da Política de Grupo: Configuração da janela pop-up padrão
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/Content settings
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: DefaultPopupsSetting
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: DefaultPopupsSetting
  - Valor de exemplo:
``` xml
<integer>1</integer>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### DefaultWebBluetoothGuardSetting
  #### Controlar o uso da API do Bluetooth na Web
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Controlar se os sites podem acessar dispositivos Bluetooth próximos. Você pode bloquear completamente o acesso ou exigir que o site pergunte ao usuário toda vez que quiser acessar um dispositivo Bluetooth.

Se você não configurar essa política, o valor padrão ('AskWebBluetooth', o que significa que os usuários são sempre solicitados) será usado e os usuários podem alterá-la.

Mapeamento das opções de política:

* BlockWebBluetooth (2) = Não permitir que todos os sites solicitem acesso a dispositivos Bluetooth por meio da API Web Bluetooth

* AskWebBluetooth (3) = Permitir que os sites peçam ao usuário para conceder acesso a um dispositivo Bluetooth próximo

Use as informações anteriores ao configurar essa política.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Inteiro

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: DefaultWebBluetoothGuardSetting
  - Nome da Política de Grupo: Controlar o uso da API Bluetooth da Web
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/Content settings
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do Valor: DefaultWebBluetoothGuardSetting
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000002
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: DefaultWebBluetoothGuardSetting
  - Valor de exemplo:
``` xml
<integer>2</integer>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### DefaultWebUsbGuardSetting
  #### Controlar o uso da API WebUSB
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Defina se os sites podem acessar dispositivos USB conectados. Você pode bloquear completamente o acesso ou perguntar ao usuário toda vez que o site deseja obter acesso a dispositivos USB conectados.

Você pode substituir essa política por padrões de URL específicos usando as políticas [WebUsbAskForUrls](#webusbaskforurls) e [WebUsbBlockedForUrls](#webusbblockedforurls).

Se você não configurar essa política, os sites poderão perguntar aos usuários se eles podem acessar os dispositivos USB conectados ('AskWebUsb') por padrão, e os usuários podem alterar essa configuração.

Mapeamento das opções de política:

* BlockWebUsb (2) = Não permitir que os sites solicitem acesso a dispositivos USB pela API WebUSB

* AskWebUsb (3) = Permitir que os sites peçam ao usuário para conceder acesso a um dispositivo USB conectado

Use as informações anteriores ao configurar essa política.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Inteiro

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: DefaultWebUsbGuardSetting
  - Nome da Política de Grupo: Controlar o uso da API WebUSB
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/Content settings
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: DefaultWebUsbGuardSetting
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000002
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: DefaultWebUsbGuardSetting
  - Valor de exemplo:
``` xml
<integer>2</integer>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### FileSystemReadAskForUrls
  #### Permitir o acesso de leitura pela API do Sistema de arquivos nesses sites
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 86 ou mais recente

  #### Descrição
  A configuração da política permite listar os padrões de URL que especificam quais sites podem pedir aos usuários que lhes concedam acesso de leitura a arquivos ou diretórios no sistema de arquivos do sistema operacional do host por meio da API do Sistema de arquivos.

Não definir a política significa que [DefaultFileSystemReadGuardSetting](#defaultfilesystemreadguardsetting) se aplica a todos os sites, se estiver definida. Caso contrário, as configurações pessoais dos usuários serão aplicadas.

Os padrões de URL não podem entrar em conflito com [FileSystemReadBlockedForUrls](#filesystemreadblockedforurls). Nenhuma das políticas tem precedência se uma URL corresponder a ambas.

Para obter informações detalhadas sobre os padrões de URL válidos, confira https://cloud.google.com/docs/chrome-enterprise/policies/url-patterns.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: FileSystemReadAskForUrls
  - Nome da Política de Grupo: Permitir o acesso de leitura pela API do Sistema de arquivos nesses sites
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/Content settings
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge\FileSystemReadAskForUrls
  - Caminho (recomendado): N/A
  - Nome do valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de exemplo:
```
SOFTWARE\Policies\Microsoft\Edge\FileSystemReadAskForUrls\1 = "https://www.example.com"
SOFTWARE\Policies\Microsoft\Edge\FileSystemReadAskForUrls\2 = "[*.]example.edu"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: FileSystemReadAskForUrls
  - Valor de exemplo:
``` xml
<array>
  <string>https://www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### FileSystemReadBlockedForUrls
  #### Bloquear o acesso de leitura por meio da API do Sistema de arquivos nesses sites
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 86 ou mais recente

  #### Descrição
  Se você definir esta política, poderá listar os padrões de URL que especificam quais sites não podem pedir aos usuários que lhes concedam acesso de leitura a arquivos ou diretórios no sistema de arquivos do sistema operacional do host por meio da API do Sistema de arquivos.

Se você não definir esta política, [DefaultFileSystemReadGuardSetting](#defaultfilesystemreadguardsetting) será aplicada a todos os sites, se estiver definida. Caso contrário, as configurações pessoais dos usuários serão aplicadas.

Os padrões de URL não podem entrar em conflito com [FileSystemReadAskForUrls](#filesystemreadaskforurls). Nenhuma das políticas tem precedência se uma URL corresponder a ambas.

Para obter informações detalhadas sobre os padrões de URL válidos, confira https://cloud.google.com/docs/chrome-enterprise/policies/url-patterns.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: FileSystemReadBlockedForUrls
  - Nome da Política de Grupo: Bloquear o acesso de leitura por meio da API do Sistema de arquivos nesses sites
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/Content settings
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge\FileSystemReadBlockedForUrls
  - Caminho (recomendado): N/A
  - Nome do valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de exemplo:
```
SOFTWARE\Policies\Microsoft\Edge\FileSystemReadBlockedForUrls\1 = "https://www.example.com"
SOFTWARE\Policies\Microsoft\Edge\FileSystemReadBlockedForUrls\2 = "[*.]example.edu"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: FileSystemReadBlockedForUrls
  - Valor de exemplo:
``` xml
<array>
  <string>https://www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### FileSystemWriteAskForUrls
  #### Permitir o acesso de gravação a arquivos e pastas nestes sites
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 86 ou mais recente

  #### Descrição
  Se você definir esta política, poderá listar os padrões de URL que especificam quais sites podem solicitar aos usuários que concedam acesso de gravação a arquivos ou diretórios no sistema de arquivos do sistema operacional do host.

Se você não definir esta política, [DefaultFileSystemWriteGuardSetting](#defaultfilesystemwriteguardsetting) se aplica a todos os sites, se estiver definida. Caso contrário, as configurações pessoais dos usuários serão aplicadas.

Os padrões de URL não podem entrar em conflito com [FileSystemWriteBlockedForUrls](#filesystemwriteblockedforurls). Nenhuma das políticas tem precedência se uma URL corresponder a ambas.

Para obter informações detalhadas sobre os padrões de URL válidos, confira https://cloud.google.com/docs/chrome-enterprise/policies/url-patterns.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: FileSystemWriteAskForUrls
  - Nome da Política de Grupo: Permitir o acesso de gravação a arquivos e pastas nestes sites
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/Content settings
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge\FileSystemWriteAskForUrls
  - Caminho (recomendado): N/A
  - Nome do valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de exemplo:
```
SOFTWARE\Policies\Microsoft\Edge\FileSystemWriteAskForUrls\1 = "https://www.example.com"
SOFTWARE\Policies\Microsoft\Edge\FileSystemWriteAskForUrls\2 = "[*.]example.edu"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: FileSystemWriteAskForUrls
  - Valor de exemplo:
``` xml
<array>
  <string>https://www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### FileSystemWriteBlockedForUrls
  #### Bloquear o acesso de gravação a arquivos e pastas nestes sites
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 86 ou mais recente

  #### Descrição
  Se você definir esta política, poderá listar os padrões de URL que especificam quais sites não podem solicitar aos usuários que concedam acesso de gravação a arquivos ou diretórios no sistema de arquivos do sistema operacional do host.

Se você não definir esta política, [DefaultFileSystemWriteGuardSetting](#defaultfilesystemwriteguardsetting) se aplica a todos os sites, se estiver definida. Caso contrário, as configurações pessoais dos usuários serão aplicadas.

Os padrões de URL não podem entrar em conflito com [FileSystemWriteAskForUrls](#filesystemwriteaskforurls). Nenhuma das políticas tem precedência se uma URL corresponder a ambas.

Para obter informações detalhadas sobre os padrões de URL válidos, confira https://cloud.google.com/docs/chrome-enterprise/policies/url-patterns.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: FileSystemWriteBlockedForUrls
  - Nome da Política de Grupo: Bloquear o acesso de gravação a arquivos e diretórios nestes sites
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/Content settings
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): OFTWARE\Policies\Microsoft\Edge\FileSystemWriteBlockedForUrls
  - Caminho (recomendado): N/A
  - Nome do valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de exemplo:
```
SOFTWARE\Policies\Microsoft\Edge\FileSystemWriteBlockedForUrls\1 = "https://www.example.com"
SOFTWARE\Policies\Microsoft\Edge\FileSystemWriteBlockedForUrls\2 = "[*.]example.edu"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: FileSystemWriteBlockedForUrls
  - Valor de exemplo:
``` xml
<array>
  <string>https://www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### ImagesAllowedForUrls
  #### Permitir imagens nestes sites
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Defina uma lista de sites, com base em padrões de URL, que não podem exibir imagens.

Se você não configurar essa política, o valor padrão global será usado para todos os sites da diretiva [DefaultImagesSetting](#defaultimagessetting) (se definida) ou à configuração pessoal do usuário.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: ImagesAllowedForUrls
  - Nome da Política de Grupo: permitir imagens nestes sites
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/Content settings
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge\ImagesAllowedForUrls
  - Caminho (recomendado): N/A
  - Nome do valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de exemplo:
```
SOFTWARE\Policies\Microsoft\Edge\ImagesAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\ImagesAllowedForUrls\2 = "[*.]contoso.edu"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ImagesAllowedForUrls
  - Valor de exemplo:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### ImagesBlockedForUrls
  #### Bloquear imagens em sites específicos
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Defina uma lista de sites, com base em padrões de URL, que não têm permissão para exibir imagens.

Se você não configurar essa política, o valor padrão global da diretiva [DefaultImagesSetting](#defaultimagessetting) (se definida) ou a configuração pessoal do usuário será usada para todos os sites.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: ImagesBlockedForUrls
  - Nome da Política de Grupo: Bloquear imagens em sites específicos
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/Content settings
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge\ImagesBlockedForUrls
  - Caminho (recomendado): N/A
  - Nome do valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de exemplo:
```
SOFTWARE\Policies\Microsoft\Edge\ImagesBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\ImagesBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ImagesBlockedForUrls
  - Valor de exemplo:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### InsecureContentAllowedForUrls
  #### Permitir conteúdo não seguro em sites especificados
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 80 ou mais recente

  #### Descrição
  Crie uma lista de padrões de URL para especificar sites que podem exibir conteúdo misto inseguro (ou seja, conteúdo HTTP em sites HTTPS).

Se você não configurar essa política, o conteúdo misto bloqueável será bloqueado, e o conteúdo misto opcionalmente bloqueável será atualizado. No entanto, os usuários poderão definir exceções para permitir conteúdo misto não seguro para sites específicos.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: InsecureContentAllowedForUrls
  - Nome da Política de Grupo: Permitir conteúdo não seguro em sites especificados
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/Content settings
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge\InsecureContentAllowedForUrls
  - Caminho (recomendado): N/A
  - Nome do valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de exemplo:
```
SOFTWARE\Policies\Microsoft\Edge\InsecureContentAllowedForUrls\1 = "https://www.example.com"
SOFTWARE\Policies\Microsoft\Edge\InsecureContentAllowedForUrls\2 = "[*.]example.edu"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: InsecureContentAllowedForUrls
  - Valor de exemplo:
``` xml
<array>
  <string>https://www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### InsecureContentBlockedForUrls
  #### Bloquear conteúdo inseguro em sites especificados
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 80 ou mais recente

  #### Descrição
  Crie uma lista de padrões de URL para especificar sites que não têm permissão para exibir conteúdo bloqueável (por exemplo, ativo) misto (isto é, conteúdo HTTP em sites HTTPS) e para os quais as atualizações de conteúdo misturadas opcionalmente bloqueáveis serão desabilitadas.

Se você não configurar essa política, o conteúdo misto bloqueável será bloqueado, e o conteúdo misto opcionalmente bloqueável será atualizado. No entanto, os usuários poderão definir exceções para permitir conteúdo misto não seguro para sites específicos.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: InsecureContentBlockedForUrls
  - Nome da Política de Grupo: Bloquear conteúdo não seguro em sites especificados
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/Content settings
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge\InsecureContentBlockedForUrls
  - Caminho (recomendado): N/A
  - Nome do valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de exemplo:
```
SOFTWARE\Policies\Microsoft\Edge\InsecureContentBlockedForUrls\1 = "https://www.example.com"
SOFTWARE\Policies\Microsoft\Edge\InsecureContentBlockedForUrls\2 = "[*.]example.edu"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: InsecureContentBlockedForUrls
  - Valor de exemplo:
``` xml
<array>
  <string>https://www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### JavaScriptAllowedForUrls
  #### Permitir JavaScript em sites específicos
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Defina uma lista de sites, com base em padrões de URL, que podem executar o JavaScript.

Se você não configurar essa política, o valor padrão global da diretiva [DefaultJavaScriptSetting](#defaultjavascriptsetting) (se definida) ou a configuração pessoal do usuário será usada para todos os sites.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: JavaScriptAllowedForUrls
  - Nome da Política de Grupo: Permitir JavaScript em sites específicos
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/Content settings
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge\JavaScriptAllowedForUrls
  - Caminho (recomendado): N/A
  - Nome do valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de exemplo:
```
SOFTWARE\Policies\Microsoft\Edge\JavaScriptAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\JavaScriptAllowedForUrls\2 = "[*.]contoso.edu"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: JavaScriptAllowedForUrls
  - Valor de exemplo:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### JavaScriptBlockedForUrls
  #### Bloquear o JavaScript em sites específicos
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Defina uma lista de sites, com base em padrões de URL, que não têm permissão para executar JavaScript.

Se você não configurar essa política, o valor padrão global da diretiva [DefaultJavaScriptSetting](#defaultjavascriptsetting) (se definida) ou a configuração pessoal do usuário será usada para todos os sites.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: JavaScriptBlockedForUrls
  - Nome da Política de Grupo: bloquear o JavaScript em sites específicos
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/Content settings
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge\JavaScriptBlockedForUrls
  - Caminho (recomendado): N/A
  - Nome do valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de exemplo:
```
SOFTWARE\Policies\Microsoft\Edge\JavaScriptBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\JavaScriptBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: JavaScriptBlockedForUrls
  - Valor de exemplo:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### LegacySameSiteCookieBehaviorEnabled
  #### Habilita a configuração padrão de cookie herdado SameSite padrão.
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 80 ou mais recente

  #### Descrição
  Permite que você reverta todos os cookies para o comportamento herdado SameSite. A reversão para o comportamento herdado causa cookies que não especificam um atributo SameSite a ser tratado como se fossem "SameSite = None", remove o requisito para os cookies "SameSite = None" para transportar o atributo "Secure" e pula a comparação de esquema ao avaliar se dois sites são de mesmo site.

Se você não definir essa política, o comportamento de SameSite padrão para cookies dependerá de outras fontes de configuração do recurso SameSite-by-default, Cookies-without-SameSite-must-be-secure e Schemeful Same-Site. Esses recursos também podem ser configurados por uma avaliação de campo ou pelo sinalizador de mesmo site-por padrão-cookies, o sinalizador de cookies-sem o mesmo site-de segurança, ou o sinalizador do mesmo site no edge://flags.

Mapeamento das opções de política:

* DefaultToLegacySameSiteCookieBehavior (1) = Reverter para comportamento herdado SameSite para cookies em todos os sites

* DefaultToSameSiteByDefaultCookieBehavior (2) = Usar o comportamento SameSite por padrão para cookies em todos os sites

Use as informações anteriores ao configurar essa política.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Inteiro

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: LegacySameSiteCookieBehaviorEnabled
  - Nome da Política de Grupo: Habilitar o comportamento padrão de cookie herdado SameSite
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/Content settings
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: LegacySameSiteCookieBehaviorEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: LegacySameSiteCookieBehaviorEnabled
  - Valor de exemplo:
``` xml
<integer>1</integer>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### LegacySameSiteCookieBehaviorEnabledForDomainList
  #### Reverter para o comportamento herdado SameSite para cookies em sites especificados
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 80 ou mais recente

  #### Descrição
  Os cookies definidos para domínios que correspondem a padrões especificados voltarão para o comportamento herdado SameSite.

A reversão para o comportamento herdado causa cookies que não especificam um atributo SameSite a ser tratado como se fossem "SameSite = None", remove o requisito para os cookies "SameSite = None" para transportar o atributo "Secure" e pula a comparação de esquema ao avaliar se dois sites são de mesmo site.

Se você não definir essa política, o valor padrão global será utilizado. O padrão global também será usado para cookies em domínios não cobertos pelos padrões que você especificar.

O valor padrão global pode ser configurado usando a política [LegacySameSiteCookieBehaviorEnabled](#legacysamesitecookiebehaviorenabled). Se [LegacySameSiteCookieBehaviorEnabled](#legacysamesitecookiebehaviorenabled) não estiver definido, o valor padrão global retorna a outras fontes de configuração.

Observe que os padrões listados nesta política são tratados como domínios, não URLs, para que você não possa especificar um esquema ou uma porta.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: LegacySameSiteCookieBehaviorEnabledForDomainList
  - Nome da Política de Grupo: Reverter para o comportamento herdado SameSite para cookies em sites especificados
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/Content settings
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge\LegacySameSiteCookieBehaviorEnabledForDomainList
  - Caminho (recomendado): N/A
  - Nome do valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de exemplo:
```
SOFTWARE\Policies\Microsoft\Edge\LegacySameSiteCookieBehaviorEnabledForDomainList\1 = "www.example.com"
SOFTWARE\Policies\Microsoft\Edge\LegacySameSiteCookieBehaviorEnabledForDomainList\2 = "[*.]example.edu"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: LegacySameSiteCookieBehaviorEnabledForDomainList
  - Valor de exemplo:
``` xml
<array>
  <string>www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### NotificationsAllowedForUrls
  #### Permitir notificações em sites específicos
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Permite que você crie uma lista de padrões de URL para especificar sites que têm permissão para exibir notificações.

Se você não definir essa política, o valor padrão global será utilizado para todos os sites. Esse valor padrão será da política [DefaultNotificationsSetting](#defaultnotificationssetting), se ela estiver definida, ou da configuração pessoal do usuário. Para obter informações detalhadas sobre os padrões de URL válidos, consulte [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: NotificationsAllowedForUrls
  - Nome da Política de Grupo: permitir notificações em sites específicos
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/Content settings
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge\NotificationsAllowedForUrls
  - Caminho (recomendado): N/A
  - Nome do valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de exemplo:
```
SOFTWARE\Policies\Microsoft\Edge\NotificationsAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\NotificationsAllowedForUrls\2 = "[*.]contoso.edu"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: NotificationsAllowedForUrls
  - Valor de exemplo:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### NotificationsBlockedForUrls
  #### Bloquear notificações em sites específicos
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Permite que você crie uma lista de padrões de URL para especificar sites que não têm permissão para exibir notificações.

Se você não definir essa política, o valor padrão global será utilizado para todos os sites. Esse valor padrão será da política [DefaultNotificationsSetting](#defaultnotificationssetting), se ela estiver definida, ou da configuração pessoal do usuário. Para obter informações detalhadas sobre os padrões de URL válidos, consulte [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: NotificationsBlockedForUrls
  - Nome da Política de Grupo: Bloquear notificações em sites específicos
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/Content settings
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge\NotificationsBlockedForUrls
  - Caminho (recomendado): N/A
  - Nome do valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de exemplo:
```
SOFTWARE\Policies\Microsoft\Edge\NotificationsBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\NotificationsBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: NotificationsBlockedForUrls
  - Valor de exemplo:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### PluginsAllowedForUrls
  #### Permitir o plug-in Adobe Flash em sites específicos
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Defina uma lista de sites, com base em padrões de URL, que podem executar o plug-in Adobe Flash.

Se você não configurar essa política, o valor padrão global da diretiva [DefaultPluginsSetting](#defaultpluginssetting) (se definida) ou a configuração pessoal do usuário será usada para todos os sites.

Para obter informações detalhadas sobre os padrões de URL válidos, consulte [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322). No entanto, iniciando no M85, padrões com os caracteres curinga '*' e '[*.]' no host não têm mais suporte para esta política.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: PluginsAllowedForUrls
  - Nome da Política de Grupo: Permitir o plug-in Adobe Flash em sites específicos
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/Content settings
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge\PluginsAllowedForUrls
  - Caminho (recomendado): N/A
  - Nome do valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de exemplo:
```
SOFTWARE\Policies\Microsoft\Edge\PluginsAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\PluginsAllowedForUrls\2 = "http://contoso.edu:8080"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: PluginsAllowedForUrls
  - Valor de exemplo:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>http://contoso.edu:8080</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### PluginsBlockedForUrls
  #### Bloquear o plug-in Adobe Flash em sites específicos
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Defina uma lista de sites, com base em padrões de URL, que são impedidos de executar o Adobe Flash.

Se você não configurar essa política, o valor padrão global da diretiva [DefaultPluginsSetting](#defaultpluginssetting) (se definida) ou a configuração pessoal do usuário será usada para todos os sites.

Para obter informações detalhadas sobre os padrões de URL válidos, consulte [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322). No entanto, iniciando no M85, padrões com os caracteres curinga '*' e '[*.]' no host não têm mais suporte para esta política.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: PluginsBlockedForUrls
  - Nome da Política de Grupo: Bloquear o plug-in Adobe Flash em sites específicos
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/Content settings
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge\PluginsBlockedForUrls
  - Caminho (recomendado): N/A
  - Nome do valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de exemplo:
```
SOFTWARE\Policies\Microsoft\Edge\PluginsBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\PluginsBlockedForUrls\2 = "http://contoso.edu:8080"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: PluginsBlockedForUrls
  - Valor de exemplo:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>http://contoso.edu:8080</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### PopupsAllowedForUrls
  #### Permitir janelas pop-up em sites específicos
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Defina uma lista de sites, com base em padrões de URL, que podem abrir janelas pop-up.

Se você não configurar essa política, o valor padrão global da diretiva [DefaultPopupsSetting](#defaultpopupssetting) (se definida) ou a configuração pessoal do usuário será usada para todos os sites.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: PopupsAllowedForUrls
  - Nome da Política de Grupo: Permitir janelas pop-up em sites específicos
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/Content settings
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge\PopupsAllowedForUrls
  - Caminho (recomendado): N/A
  - Nome do valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de exemplo:
```
SOFTWARE\Policies\Microsoft\Edge\PopupsAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\PopupsAllowedForUrls\2 = "[*.]contoso.edu"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: PopupsAllowedForUrls
  - Valor de exemplo:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### PopupsBlockedForUrls
  #### Bloquear janelas pop-up em sites específicos
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Defina uma lista de sites, com base em padrões de URL, que estão impedidos de abrir janelas pop-up.

Se você não configurar essa política, o valor padrão global da diretiva [DefaultPopupsSetting](#defaultpopupssetting) (se definida) ou a configuração pessoal do usuário será usada para todos os sites.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: PopupsBlockedForUrls
  - Nome da Política de Grupo: Bloquear janelas pop-up em sites específicos
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/Content settings
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge\PopupsBlockedForUrls
  - Caminho (recomendado): N/A
  - Nome do valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de exemplo:
```
SOFTWARE\Policies\Microsoft\Edge\PopupsBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\PopupsBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: PopupsBlockedForUrls
  - Valor de exemplo:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### RegisteredProtocolHandlers
  #### Registrar manipuladores de protocolo
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Defina essa política (recomendável apenas) para registrar uma lista de manipuladores de protocolo. Essa lista é mesclada com aquelas registradas pelo usuário e ambas estão disponíveis para uso.

Para registrar um manipulador de protocolo:

- Definir a propriedade do protocolo para o esquema (por exemplo, "mailto")
- Definir a propriedade URL para a propriedade URL do aplicativo que trata o esquema especificado no campo "protocolo". O padrão pode incluir um marcador de posição "%s", que será substituído pela URL manipulada.

Os usuários não podem remover um manipulador de protocolo registrado por esta política. No entanto, eles podem instalar um novo manipulador de protocolo padrão para substituir os manipuladores de protocolo existentes.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Não
  - Pode ser recomendável: Sim
  - Atualização dinâmica das políticas: não requer a reinicialização do navegador

  #### Tipo de dados:
  - Dictionary

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: RegisteredProtocolHandlers
  - Nome da Política de Grupo: Registrar manipuladores de protocolo
  - Caminho da Política de Grupo (obrigatório): N/A
  - Caminho da Política de Grupo (recomendado): Administrative Templates/Microsoft Edge - Default Settings (usuários podem substituir)/Content settings
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): N/A
  - Caminho (recomendado): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nome do Valor: RegisteredProtocolHandlers
  - Tipo do valor: REG_SZ
  ##### Valor de exemplo:
```
SOFTWARE\Policies\Microsoft\Edge\RegisteredProtocolHandlers = [
  {
    "default": true, 
    "protocol": "mailto", 
    "url": "https://mail.contoso.com/mail/?extsrc=mailto&url=%s"
  }
]
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: RegisteredProtocolHandlers
  - Valor de exemplo:
``` xml
<key>RegisteredProtocolHandlers</key>
<array>
  <dict>
    <key>default</key>
    <true/>
    <key>protocol</key>
    <string>mailto</string>
    <key>url</key>
    <string>https://mail.contoso.com/mail/?extsrc=mailto&url=%s</string>
  </dict>
</array>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### SpotlightExperiencesAndRecommendationsEnabled
  #### Escolha se os usuários podem receber imagens de plano de fundo personalizadas e texto, sugestões, notificações,
e dicas para os serviços Microsoft
  
  
  #### Versões com suporte:
  - No Windows desde 86 ou posterior

  #### Descrição
  Escolha se os usuários podem receber imagens de plano de fundo personalizadas e texto, sugestões, notificações e dicas para os serviços Microsoft.

Se você habilitar ou não definir essa configuração, as experiências e as recomendações em destaque serão ativadas.

Se você desabilitar essa configuração, as experiências e as recomendações em destaque serão desativadas.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: não requer a reinicialização do navegador

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Politica de Grupo: SpotlightExperiencesAndRecommendationsEnabled
  - Nome da política de grupo: escolha se os usuários podem receber imagens de plano de fundo personalizadas e texto, sugestões, notificações e dicas para os serviços Microsoft.
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/Content settings
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do Valor: SpotlightExperiencesAndRecommendationsEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  

  [Voltar ao início](#microsoft-edge---policies)

  ### WebUsbAllowDevicesForUrls
  #### Conceder acesso a sites específicos para conectar-se a dispositivos USB específicos
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Permite que você defina uma lista de URLs que especificam quais sites recebem permissão automaticamente para acessar um dispositivo USB com determinado fornecedor e IDs de produto. Cada item na lista deve conter os dispositivos e URLs para que a política seja válida. Cada item em dispositivos pode conter um ID de fornecedor e um campo de ID do produto. Todos os IDs omitidos são tratados como curinga com uma exceção, e essa exceção é que um ID de produto não pode ser especificado sem o ID do fornecedor. Caso contrário, a política não será válida e será ignorada.

O modelo de permissão USB usa a URL do site de solicitação ("solicitando URL") e a URL do site de quadro de nível superior ("URL da incorporação") para conceder permissão à URL de solicitação para acessar o dispositivo USB. A URL de solicitação pode ser diferente da URL inserida quando o site de solicitação é carregado em um iframe. Portanto, o campo "URLs" pode conter até duas cadeias de caracteres de URL delimitadas por uma vírgula para especificar a solicitação e a inserção da URL, respectivamente. Se apenas uma URL for especificada, o acesso aos dispositivos USB correspondentes será concedido quando a URL do site solicitante corresponder a essa URL, independentemente do status da incorporação. As URLs em "URLs" devem ser URLs válidas, caso contrário, a política será ignorada.

Se essa política não estiver definida, o valor padrão global será usado para todos os sites da política [DefaultWebUsbGuardSetting](#defaultwebusbguardsetting), caso tenha sido definido, ou a configuração pessoal do usuário.

Os padrões de URL nesta política não devem conflitar com os que foram configurados via [WebUsbBlockedForUrls](#webusbblockedforurls). Se houver um conflito, essa política terá precedência sobre [WebUsbBlockedForUrls](#webusbblockedforurls) e [WebUsbAskForUrls](#webusbaskforurls).

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Dictionary

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: WebUsbAllowDevicesForUrls
  - Nome da Política de Grupo: Conceder acesso a sites específicos para conectar-se a dispositivos USB específicos
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/Content settings
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: WebUsbAllowDevicesForUrls
  - Tipo do valor: REG_SZ
  ##### Valor de exemplo:
```
SOFTWARE\Policies\Microsoft\Edge\WebUsbAllowDevicesForUrls = [
  {
    "devices": [
      {
        "product_id": 5678, 
        "vendor_id": 1234
      }
    ], 
    "urls": [
      "https://contoso.com", 
      "https://fabrikam.com"
    ]
  }
]
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: WebUsbAllowDevicesForUrls
  - Valor de exemplo:
``` xml
<key>WebUsbAllowDevicesForUrls</key>
<array>
  <dict>
    <key>devices</key>
    <array>
      <dict>
        <key>product_id</key>
        <integer>5678</integer>
        <key>vendor_id</key>
        <integer>1234</integer>
      </dict>
    </array>
    <key>urls</key>
    <array>
      <string>https://contoso.com</string>
      <string>https://fabrikam.com</string>
    </array>
  </dict>
</array>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### WebUsbAskForUrls
  #### Permitir WebUSB em sites específicos
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Defina uma lista de sites, com base em padrões de URL, que podem solicitar acesso ao usuário para um dispositivo USB.

Se você não configurar essa política, o valor padrão global da diretiva [DefaultWebUsbGuardSetting](#defaultwebusbguardsetting) (se definida) ou a configuração pessoal do usuário será usada para todos os sites.

Os padrões de URL definidos nesta política não podem entrar em conflito com aqueles configurados na política [WebUsbBlockedForUrls](#webusbblockedforurls)- você não pode permitir e bloquear uma URL. Para obter informações detalhadas sobre os padrões de URL válidos, consulte [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: WebUsbAskForUrls
  - Nome da Política de Grupo: Permitir WebUSB em sites específicos
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/Content settings
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge\WebUsbAskForUrls
  - Caminho (recomendado): N/A
  - Nome do valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de exemplo:
```
SOFTWARE\Policies\Microsoft\Edge\WebUsbAskForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\WebUsbAskForUrls\2 = "[*.]contoso.edu"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: WebUsbAskForUrls
  - Valor de exemplo:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### WebUsbBlockedForUrls
  #### Bloquear WebUSB em sites específicos
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Defina uma lista de sites, com base em padrões de URL, que não podem solicitar ao usuário que conceda acesso a um dispositivo USB.

Se você não configurar essa política, o valor padrão global da diretiva [DefaultWebUsbGuardSetting](#defaultwebusbguardsetting) (se definida) ou a configuração pessoal do usuário será usada para todos os sites.

Os padrões de URL nesta política não podem entrar em conflito com aqueles configurados na política [WebUsbAskForUrls](#webusbaskforurls). Você não pode permitir nem bloquear uma URL.  Para obter informações detalhadas sobre os padrões de URL válidos, consulte [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: WebUsbBlockedForUrls
  - Nome da Política de Grupo: bloquear WebUSB em sites específicos
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/Content settings
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge\WebUsbBlockedForUrls
  - Caminho (recomendado): N/A
  - Nome do valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de exemplo:
```
SOFTWARE\Policies\Microsoft\Edge\WebUsbBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\WebUsbBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: WebUsbBlockedForUrls
  - Valor de exemplo:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ## Políticas de provedor de pesquisa padrão

  [Voltar ao início](#microsoft-edge---policies)

  ### DefaultSearchProviderEnabled
  #### Habilitar o provedor de pesquisa padrão
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Permite o uso de um provedor de pesquisa padrão.

Se você habilitar essa política, um usuário poderá procurar um termo digitando na barra de endereços (desde que não seja uma URL).

Você pode especificar o provedor de pesquisa padrão a ser utilizado, habilitando o restante das políticas de pesquisa padrão. Se elas estiverem vazias (não configuradas) ou configuradas incorretamente, o usuário poderá escolher o provedor padrão.

Se você desabilitar essa política, o usuário não poderá pesquisar na barra de endereços.

Se você habilitar ou desabilitar essa política, os usuários não poderão alterá-la ou substituí-la.

Se você não configurar essa política, o provedor de pesquisa padrão será habilitado e o usuário poderá escolher o provedor de pesquisa padrão e definir a lista de provedores de pesquisa.

Essa política está disponível apenas nas instâncias do Windows que fazem parte de um domínio do Microsoft Active Directory, em instâncias do Windows 10 Pro ou Enterprise que estejam inscritas no gerenciamento de dispositivos ou em instâncias do macOS que são gerenciadas por meio do MDM ou passaram a fazer parte de um domínio por meio de MCX.

A partir do Microsoft Edge 84, você pode definir essa política como uma política recomendada.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: Sim
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: DefaultSearchProviderEnabled
  - Nome da Política de Grupo: Habilitar o provedor de pesquisa padrão
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/Default search provider
  - Caminho do GP (Recomendado): Modelos administrativos/Microsoft Edge - Configurações padrão (os usuários podem substituir)/Provedor de pesquisa padrão
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nome do Valor: DefaultSearchProviderEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: DefaultSearchProviderEnabled
  - Valor de exemplo:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### DefaultSearchProviderEncodings
  #### Codificações de provedores de pesquisa padrão
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Especifique as codificações de caractere compatíveis com o provedor de pesquisa. Codificações são nomes de página de código como UTF-8, GB2312 e ISO-8859-1. Elas são testadas na ordem fornecida.

Essa política é opcional. Se ela não estiver configurada, o padrão UTF-8 será usado.

Essa política será aplicada somente se você habilitar as políticas [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) e [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl).

A partir do Microsoft Edge 84, você pode definir essa política como uma política recomendada. Se o usuário já tiver definido um provedor de pesquisa padrão, o provedor de pesquisa padrão configurado por essa política recomendada não será adicionado à lista de provedores de pesquisa que o usuário pode escolher. Se esse for o comportamento desejado, use a política de [ManagedSearchEngines](#managedsearchengines).

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: Sim
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo:: DefaultSearchProviderEncodings
  - Nome da Política de Grupo: Codificações de provedores de pesquisa padrão
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/Default search provider
  - Caminho do GP (Recomendado): Modelos administrativos/Microsoft Edge - Configurações padrão (os usuários podem substituir)/Provedor de pesquisa padrão
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge\DefaultSearchProviderEncodings
  - Caminho (Recomendado): SOFTWARE\Policies\Microsoft\Edge\Recommended\DefaultSearchProviderEncodings
  - Nome do valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de exemplo:
```
SOFTWARE\Policies\Microsoft\Edge\DefaultSearchProviderEncodings\1 = "UTF-8"
SOFTWARE\Policies\Microsoft\Edge\DefaultSearchProviderEncodings\2 = "UTF-16"
SOFTWARE\Policies\Microsoft\Edge\DefaultSearchProviderEncodings\3 = "GB2312"
SOFTWARE\Policies\Microsoft\Edge\DefaultSearchProviderEncodings\4 = "ISO-8859-1"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: DefaultSearchProviderEncodings
  - Valor de exemplo:
``` xml
<array>
  <string>UTF-8</string>
  <string>UTF-16</string>
  <string>GB2312</string>
  <string>ISO-8859-1</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### DefaultSearchProviderImageURL
  #### Especifica o recurso Pesquisar por imagem para o provedor de pesquisa padrão
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Especifica a URL do mecanismo de pesquisa usado para pesquisa de imagens. As solicitações de pesquisa são enviadas usando o método GET.

Essa política é opcional. Se você não a configurar, a pesquisa de imagens não estará disponível.

Especificar a URL de pesquisa de imagens do Bing como: '{bing:baseURL}images/detail/search?iss=sbiupload&FORM=ANCMS1#enterInsights'.

Especifique a URL de pesquisa de imagens do Google como: '{google:baseURL}searchbyimage/upload'.

Consulte a política [DefaultSearchProviderImageURLPostParams](#defaultsearchproviderimageurlpostparams) para concluir a configuração da pesquisa de imagens.

Essa política será aplicada somente se você habilitar as políticas [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) e [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl).

A partir do Microsoft Edge 84, você pode definir essa política como uma política recomendada. Se o usuário já tiver definido um provedor de pesquisa padrão, o provedor de pesquisa padrão configurado por essa política recomendada não será adicionado à lista de provedores de pesquisa que o usuário pode escolher. Se esse for o comportamento desejado, use a política de [ManagedSearchEngines](#managedsearchengines).

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: Sim
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - String

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: DefaultSearchProviderImageURL
  - Nome da Política de Grupo: Especifica o recurso pesquisar-por-imagem para o provedor de pesquisa padrão
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/Default search provider
  - Caminho do GP (Recomendado): Modelos administrativos/Microsoft Edge - Configurações padrão (os usuários podem substituir)/Provedor de pesquisa padrão
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nome do Valor: DefaultSearchProviderImageURL
  - Tipo do valor: REG_SZ
  ##### Valor de exemplo:
```
"https://search.contoso.com/searchbyimage/upload"
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: DefaultSearchProviderImageURL
  - Valor de exemplo:
``` xml
<string>https://search.contoso.com/searchbyimage/upload</string>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### DefaultSearchProviderImageURLPostParams
  #### Parâmetros para uma URL de imagem que usa POST
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Se você habilitar essa política, ela especificará os parâmetros usados quando uma pesquisa de imagem que usa POST é realizada. A política é composta por pares de nome/valor separados por vírgulas. Se um valor for um parâmetro de modelo, como {imageThumbnail} no exemplo anterior, ele será substituído por dados em miniatura da imagem real. Essa política será aplicada somente se você habilitar as políticas [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) e [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl).

Especificar o endereço de URL de pesquisa de imagens do Bing como: ' imageBin = {Google: imageThumbnailBase64} '.

Especificar o URL da pesquisa de imagens do Google, como: 'encoded_image={google:imageThumbnail},image_url={google:imageURL},sbisrc={google:imageSearchSource},original_width={google:imageOriginalWidth},original_height={google:imageOriginalHeight}'.

Se você não definir essa política, as solicitações de pesquisa de imagens serão enviadas usando o método GET.

A partir do Microsoft Edge 84, você pode definir essa política como uma política recomendada. Se o usuário já tiver definido um provedor de pesquisa padrão, o provedor de pesquisa padrão configurado por essa política recomendada não será adicionado à lista de provedores de pesquisa que o usuário pode escolher. Se esse for o comportamento desejado, use a política de [ManagedSearchEngines](#managedsearchengines).

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: Sim
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - String

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: DefaultSearchProviderImageURLPostParams
  - Nome da Política de Grupo: Parâmetros de uma URL de imagem que usa POST
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/Default search provider
  - Caminho do GP (Recomendado): Modelos administrativos/Microsoft Edge - Configurações padrão (os usuários podem substituir)/Provedor de pesquisa padrão
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nome do Valor: DefaultSearchProviderImageURLPostParams
  - Tipo do valor: REG_SZ
  ##### Valor de exemplo:
```
"content={imageThumbnail},url={imageURL},sbisrc={SearchSource}"
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: DefaultSearchProviderImageURLPostParams
  - Valor de exemplo:
``` xml
<string>content={imageThumbnail},url={imageURL},sbisrc={SearchSource}</string>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### DefaultSearchProviderKeyword
  #### Palavra-chave do provedor de pesquisa padrão
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Especifica a palavra-chave, que é o atalho usado na barra de endereços para disparar a pesquisa desse provedor.

Essa política é opcional. Se você não a configurar, nenhuma palavra-chave ativará o provedor de pesquisa.

Essa política será aplicada somente se você habilitar as políticas [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) e [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl).

A partir do Microsoft Edge 84, você pode definir essa política como uma política recomendada. Se o usuário já tiver definido um provedor de pesquisa padrão, o provedor de pesquisa padrão configurado por essa política recomendada não será adicionado à lista de provedores de pesquisa que o usuário pode escolher. Se esse for o comportamento desejado, use a política de [ManagedSearchEngines](#managedsearchengines).

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: Sim
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - String

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: DefaultSearchProviderKeyword
  - Nome da Política de Grupo: Palavra-chave do provedor de pesquisa padrão
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/Default search provider
  - Caminho do GP (Recomendado): Modelos administrativos/Microsoft Edge - Configurações padrão (os usuários podem substituir)/Provedor de pesquisa padrão
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nome do Valor: DefaultSearchProviderKeyword
  - Tipo do valor: REG_SZ
  ##### Valor de exemplo:
```
"mis"
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: DefaultSearchProviderKeyword
  - Valor de exemplo:
``` xml
<string>mis</string>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### DefaultSearchProviderName
  #### Nome do provedor de pesquisa padrão
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Especifica o nome do provedor de pesquisa padrão.

Se você habilitar essa política, definirá o nome do provedor de pesquisa padrão.

Se você não habilitar essa política ou deixá-la vazia, o nome do host especificado pela URL de pesquisa será usado.

"DefaultSearchProviderName" deve ser definido como um provedor de pesquisa criptografado aprovado pela organização que corresponde ao provedor de pesquisa criptografado definido em DTBC-0008. Essa política será aplicada somente se você habilitar as políticas [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) e [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl).

A partir do Microsoft Edge 84, você pode definir essa política como uma política recomendada. Se o usuário já tiver definido um provedor de pesquisa padrão, o provedor de pesquisa padrão configurado por essa política recomendada não será adicionado à lista de provedores de pesquisa que o usuário pode escolher. Se esse for o comportamento desejado, use a política de [ManagedSearchEngines](#managedsearchengines).

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: Sim
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - String

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: DefaultSearchProviderName
  - Nome da Política de Grupo: Nome do provedor de pesquisa padrão
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/Default search provider
  - Caminho do GP (Recomendado): Modelos administrativos/Microsoft Edge - Configurações padrão (os usuários podem substituir)/Provedor de pesquisa padrão
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nome do valor: DefaultSearchProviderName
  - Tipo do valor: REG_SZ
  ##### Valor de exemplo:
```
"My Intranet Search"
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: DefaultSearchProviderName
  - Valor de exemplo:
``` xml
<string>My Intranet Search</string>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### DefaultSearchProviderSearchURL
  #### URL de pesquisa do provedor de pesquisa padrão
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Especifica a URL do mecanismo de pesquisa usado para uma pesquisa padrão. A URL contém a cadeia de caracteres '{searchTerms}', que é substituída durante a consulta pelos termos que o usuário está procurando.

Especificar a URL de pesquisa do Bing como:

'{bing:baseURL}search?q={searchTerms}'.

Especificar a URL de pesquisa do Google como: '{google:baseURL}search?q={searchTerms}&{google:RLZ}{google:originalQueryForSuggestion}{google:assistedQueryStats}{google:searchFieldtrialParameter}{google:searchClient}{google:sourceId}ie={inputEncoding}'.

Essa política é necessária quando você habilita a política [DefaultSearchProviderEnabled](#defaultsearchproviderenabled). Se você não habilitar a última política, essa política será ignorada.

A partir do Microsoft Edge 84, você pode definir essa política como uma política recomendada. Se o usuário já tiver definido um provedor de pesquisa padrão, o provedor de pesquisa padrão configurado por essa política recomendada não será adicionado à lista de provedores de pesquisa que o usuário pode escolher. Se esse for o comportamento desejado, use a política de [ManagedSearchEngines](#managedsearchengines).

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: Sim
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - String

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: DefaultSearchProviderSearchURL
  - Nome da Política de Grupo: URL de pesquisa do provedor de pesquisa padrão
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/Default search provider
  - Caminho do GP (Recomendado): Modelos administrativos/Microsoft Edge - Configurações padrão (os usuários podem substituir)/Provedor de pesquisa padrão
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nomeo do Valor: DefaultSearchProviderSearchURL
  - Tipo do valor: REG_SZ
  ##### Valor de exemplo:
```
"https://search.contoso.com/search?q={searchTerms}"
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: DefaultSearchProviderSearchURL
  - Valor de exemplo:
``` xml
<string>https://search.contoso.com/search?q={searchTerms}</string>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### DefaultSearchProviderSuggestURL
  #### URL do provedor de pesquisa padrão para sugestões
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Especifica a URL do mecanismo de pesquisa usado para fornecer sugestões de pesquisa. A URL contém a cadeia de caracteres '{searchTerms}', que é substituída no momento da consulta pela digitação do usuário até o momento.

Essa política é opcional. Se você não a configurar, os usuários não verão sugestões de pesquisa. Eles poderão ver sugestões de seu histórico de navegação e favoritos.

A URL sugerida do Bing pode ser especificada da seguinte forma:

'{bing:baseURL}qbox?query={searchTerms}'.

A URL sugerida do Google pode ser especificada como: '{google:baseURL}complete/search?output=chrome&q={searchTerms}'.

Essa política será aplicada somente se você habilitar as políticas [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) e [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl).

A partir do Microsoft Edge 84, você pode definir essa política como uma política recomendada. Se o usuário já tiver definido um provedor de pesquisa padrão, o provedor de pesquisa padrão configurado por essa política recomendada não será adicionado à lista de provedores de pesquisa que o usuário pode escolher. Se esse for o comportamento desejado, use a política de [ManagedSearchEngines](#managedsearchengines).

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: Sim
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - String

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: DefaultSearchProviderSuggestURL
  - Nome da Política de Grupo: URL do provedor de pesquisa padrão para sugestões
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/Default search provider
  - Caminho do GP (Recomendado): Modelos administrativos/Microsoft Edge - Configurações padrão (os usuários podem substituir)/Provedor de pesquisa padrão
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nome do Valor: DefaultSearchProviderSuggestURL
  - Tipo do valor: REG_SZ
  ##### Valor de exemplo:
```
"https://search.contoso.com/suggest?q={searchTerms}"
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: DefaultSearchProviderSuggestURL
  - Valor de exemplo:
``` xml
<string>https://search.contoso.com/suggest?q={searchTerms}</string>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### NewTabPageSearchBox
  #### Configurar a nova experiência da caixa de pesquisa da página da guia
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 85 ou mais recente

  #### Descrição
  Você pode configurar a caixa de pesquisa da nova guia para usar a "caixa de pesquisa (recomendado)" ou "barra de endereços" para pesquisar novas guias. Essa política só funcionará se você definir o mecanismo de pesquisa para um valor diferente de Bing, configurando as duas políticas a seguir: [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) e [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl).

 Se você desabilitar ou não configurar essa política e:

- Se a barra de endereços padrão do mecanismo de pesquisa for Bing, a página nova guia usará a caixa de pesquisa para pesquisar em novas guias.
- Se a barra de endereços padrão do mecanismo de pesquisa não for Bing, os usuários terão uma opção adicional (use "barra de endereços") ao pesquisar em novas guias.


Se você habilitar essa política e defini-la como:

- "Caixa de pesquisa (recomendada)" ('Bing'), a página da nova guia usa a caixa de pesquisa para pesquisar novas guias.
- "Barra de endereços" ('redirecionar'), a caixa de pesquisa da nova guia usa a barra de endereços para pesquisar novas guias.

Mapeamento das opções de política:

* bing (bing) = Caixa de pesquisa (Recomendado)

* redirecionar (redirecionar) = Barra de endereços

Use as informações anteriores ao configurar essa política.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: Sim
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - String

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: NewTabPageSetFeedType
  - Nome da Política de Grupo: Configurar a nova experiência da caixa de pesquisa da página da guia
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/Default search provider
  - Caminho do GP (Recomendado): Modelos administrativos/Microsoft Edge - Configurações padrão (os usuários podem substituir)/Provedor de pesquisa padrão
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Value Name: NewTabPageSearchBox
  - Tipo do valor: REG_SZ
  ##### Valor de exemplo:
```
"bing"
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: NewTabPageSearchBox
  - Valor de exemplo:
``` xml
<string>bing</string>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ## Políticas de extensões

  [Voltar ao início](#microsoft-edge---policies)

  ### ExtensionAllowedTypes
  #### Configurar tipos de extensão permitidas
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Controla quais tipos de extensão podem ser instalados e limita o acesso de tempo de execução.

Essa configuração define os tipos de extensões permitidas e com quais hosts elas podem interagir. O valor é uma lista de cadeias de caracteres, cada uma delas deve ser uma das seguintes: "extension", "theme", "user_script", and "hosted_app". Confira a documentação do Microsoft Edge Extensions para saber mais sobre esses tipos.

Observe que essa política também afeta as extensões a serem instaladas à força ao usar a política [ExtensionInstallForcelist](#extensioninstallforcelist).

Se você habilitar essa política, somente as extensões que correspondem a um tipo na lista serão instaladas.

Se você não configurar essa política, não há restrições para os tipos de extensão aceitáveis.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: ExtensionAllowedTypes
  - Nome da Política de Grupo: Configurar tipos de extensão permitidos
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/Extensions
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge\ExtensionAllowedTypes
  - Caminho (recomendado): N/A
  - Nome do valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de exemplo:
```
SOFTWARE\Policies\Microsoft\Edge\ExtensionAllowedTypes\1 = "hosted_app"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ExtensionAllowedTypes
  - Valor de exemplo:
``` xml
<array>
  <string>hosted_app</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### ExtensionInstallAllowlist
  #### Permitir que extensões específicas sejam instaladas
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Por padrão, todas as extensões são permitidas. No entanto, se você bloquear todas as extensões, configurando a política "ExtensionInstallBlockList" para "*", os usuários só poderão instalar extensões definidas nesta política.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: ExtensionInstallAllowlist
  - Nome da Política de Grupo: Permitir que extensões específicas sejam instaladas
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/Extensions
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallAllowlist
  - Caminho (recomendado): N/A
  - Nome do valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de exemplo:
```
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallAllowlist\1 = "extension_id1"
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallAllowlist\2 = "extension_id2"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ExtensionInstallAllowlist
  - Valor de exemplo:
``` xml
<array>
  <string>extension_id1</string>
  <string>extension_id2</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### ExtensionInstallBlocklist
  #### Controlar quais extensões não podem ser instaladas
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Liste extensões específicas que os usuários não podem instalar no Microsoft Edge. Ao implantar essa política, todas as extensões nesta lista que foram instaladas anteriormente serão desabilitadas e o usuário não poderá habilitá-las. Se você remover um item da lista de extensões bloqueadas, essa extensão será reabilitada automaticamente em todos os lugares em que já havia sido instalada.

Use "*" para bloquear todas as extensões que não estão explicitamente listadas na lista de permissões.

Se você não configurar essa política, os usuários poderão instalar as extensões no Microsoft Edge.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: ExtensionInstallBlocklist
  - Nome da Política de Grupo: Controlar quais extensões não podem ser instaladas
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/Extensions
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallBlocklist
  - Caminho (recomendado): N/A
  - Nome do valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de exemplo:
```
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallBlocklist\1 = "extension_id1"
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallBlocklist\2 = "extension_id2"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ExtensionInstallBlocklist
  - Valor de exemplo:
``` xml
<array>
  <string>extension_id1</string>
  <string>extension_id2</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### ExtensionInstallForcelist
  #### Controlar quais extensões são instaladas silenciosamente
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Especifica as extensões instaladas silenciosamente, sem a interação do usuário e que os usuários não podem desinstalar ou desabilitar ("instalação forçada"). Todas as permissões solicitadas pelas extensões são concedidas implicitamente, sem interação do usuário, incluindo quaisquer permissões adicionais solicitadas por versões futuras da extensão. Além disso, as permissões são concedidas para as APIs de extensão enterprise.deviceAttributes e enterprise.platformKeys. (Essas duas APIs estão disponíveis apenas para extensões que são instaladas à força.)

Essa política tem precedência sobre uma política [ExtensionInstallBlocklist](#extensioninstallblocklist) potencialmente conflitante. Quando você tira uma extensão da lista de instalação forçada, ela é desinstalada automaticamente no Microsoft Edge.

A instalação forçada se limitada aos aplicativos e extensões listados no site Complementos do Microsoft Edge para instâncias que não são uma das seguintes opções: as instâncias do Windows que fazem parte de um domínio do Microsoft Active Directory, ou instâncias do Windows 10 Pro ou Enterprise que se inscreveram para o gerenciamento de dispositivos e as instâncias do macOS gerenciadas via MDM ou associadas a um domínio por meio do MCX.

Observe que os usuários podem modificar o código-fonte de qualquer extensão usando as ferramentas de desenvolvedor, potencialmente processando a extensão Dysfunctional. Se isso for uma preocupação, defina a política [DeveloperToolsAvailability](#developertoolsavailability).

Use o formato a seguir para adicionar uma extensão à lista:

[ExtensionId]; [updateURL]

- ExtensionId: A cadeia de 32 caracteres, encontrada em edge://extensions, no modo de desenvolvedor.

- updateURL (opcional) é o endereço do documento XML de atualização para o aplicativo ou extensão, conforme descrito em [https://go.microsoft.com/fwlink/?linkid=2095043](https://go.microsoft.com/fwlink/?linkid=2095043). Se você deseja instalar uma extensão na Web Store, forneça a URL de atualização do Chrome Web Store, https://clients2.google.com/service/update2/crx. Observe que a URL de atualização definida nesta política só é usada para a instalação inicial. As atualizações subsequentes da extensão usam a URL de atualização indicada no manifesto da extensão. Se você não definir o updateURL, a extensão será considerada hospedada na Microsoft Store e a seguinte URL de atualização será usada (https://edge.microsoft.com/extensionwebstorebase/v1/crx).

Por exemplo, gggmmkjegpiggikcnhidnjjhmicpibll; https://edge.microsoft.com/extensionwebstorebase/v1/crx instala o aplicativo Microsoft Online na URL "atualizar" da Microsoft Store. Para obter mais informações sobre as extensões de hospedagem, confira: [https://go.microsoft.com/fwlink/?linkid=2095044](https://go.microsoft.com/fwlink/?linkid=2095044).

Se você não configurar essa política, nenhuma extensão será instalada automaticamente, e os usuários poderão desinstalar qualquer extensão no Microsoft Edge.

Observe que essa política não se aplica ao modo InPrivate.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: ExtensionInstallForcelist
  - Nome da Política de Grupo: Controlar quais extensões são instaladas silenciosamente
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/Extensions
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallForcelist
  - Caminho (recomendado): N/A
  - Nome do valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de exemplo:
```
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallForcelist\1 = "gbchcmhmhahfdphkhkmpfmihenigjmpp;https://edge.microsoft.com/extensionwebstorebase/v1/crx"
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallForcelist\2 = "abcdefghijklmnopabcdefghijklmnop"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ExtensionInstallForcelist
  - Valor de exemplo:
``` xml
<array>
  <string>gbchcmhmhahfdphkhkmpfmihenigjmpp;https://edge.microsoft.com/extensionwebstorebase/v1/crx</string>
  <string>abcdefghijklmnopabcdefghijklmnop</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### ExtensionInstallSources
  #### Configurar fontes de instalação de extensão e script de usuário
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Defina URLs que possam instalar extensões e temas.

Por padrão, os usuários têm que baixar um arquivo *.crx para cada extensão ou script que deseja instalar e, em seguida, arrastá-lo para a página de configurações do Microsoft Edge. Essa política permite que URLs específicas usem a extensão ou o script para o usuário.

Cada item nesta lista é um padrão de correspondência de estilo de extensão (consulte [https://go.microsoft.com/fwlink/?linkid=2095039](https://go.microsoft.com/fwlink/?linkid=2095039)). Os usuários podem instalar facilmente os itens de qualquer URL que corresponda a um item nesta lista. O local do arquivo *.crx e a página onde o download é iniciado (em outras palavras, a referencial) devem ser permitidos por esses padrões.

A política [ExtensionInstallBlocklist](#extensioninstallblocklist) tem precedência sobre esta política. As extensões que estiverem na lista de bloqueios não serão instaladas, mesmo se vierem de um site nesta lista.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: ExtensionInstallSources
  - Nome da Política de Grupo: Configurar fontes de instalação de extensão e script de usuário
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/Extensions
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallSources
  - Caminho (recomendado): N/A
  - Nome do valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de exemplo:
```
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallSources\1 = "https://corp.contoso.com/*"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ExtensionInstallSources
  - Valor de exemplo:
``` xml
<array>
  <string>https://corp.contoso.com/*</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### ExtensionSettings
  #### Definir configurações de gerenciamento de extensão.
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Define as configurações de gerenciamento de extensão para o Microsoft Edge.

Essa política controla várias configurações, incluindo as configurações controladas por qualquer política de extensão existente. Essa política substitui as políticas herdadas se ambas estiverem definidas.

Esta política mapeia um ID de extensão ou uma URL de atualização para a sua configuração. Com uma ID de extensão, a configuração é aplicada somente à extensão especificada. Defina uma configuração padrão para o ID especial "*" para aplicar a todas as extensões que não estão listadas especificamente nesta política. Com uma URL de atualização, a configuração é aplicada a todas as extensões com a URL de atualização exata mencionada no manifesto desta extensão, conforme descrito em [https://go.microsoft.com/fwlink/?linkid=2095043](https://go.microsoft.com/fwlink/?linkid=2095043).

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Dictionary

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: ExtensionSettings
  - Nome da Política de Grupo: Configurar definições de gerenciamento de extensão
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/Extensions
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do Valor: ExtensionsEnabled
  - Tipo do valor: REG_SZ
  ##### Valor de exemplo:
```
SOFTWARE\Policies\Microsoft\Edge\ExtensionSettings = {
  "*": {
    "allowed_types": [
      "hosted_app"
    ], 
    "blocked_install_message": "Custom error message.", 
    "blocked_permissions": [
      "downloads", 
      "bookmarks"
    ], 
    "install_sources": [
      "https://company-intranet/apps"
    ], 
    "installation_mode": "blocked", 
    "runtime_allowed_hosts": [
      "*://good.contoso.com"
    ], 
    "runtime_blocked_hosts": [
      "*://*.contoso.com"
    ]
  }, 
  "abcdefghijklmnopabcdefghijklmnop": {
    "blocked_permissions": [
      "history"
    ], 
    "installation_mode": "allowed", 
    "minimum_version_required": "1.0.1"
  }, 
  "bcdefghijklmnopabcdefghijklmnopa": {
    "allowed_permissions": [
      "downloads"
    ], 
    "installation_mode": "force_installed", 
    "runtime_allowed_hosts": [
      "*://good.contoso.com"
    ], 
    "runtime_blocked_hosts": [
      "*://*.contoso.com"
    ], 
    "update_url": "https://contoso.com/update_url"
  }, 
  "cdefghijklmnopabcdefghijklmnopab": {
    "blocked_install_message": "Custom error message.", 
    "installation_mode": "blocked"
  }, 
  "defghijklmnopabcdefghijklmnopabc,efghijklmnopabcdefghijklmnopabcd": {
    "blocked_install_message": "Custom error message.", 
    "installation_mode": "blocked"
  }, 
  "fghijklmnopabcdefghijklmnopabcde": {
    "blocked_install_message": "Custom removal message.", 
    "installation_mode": "removed"
  }, 
  "update_url:https://www.contoso.com/update.xml": {
    "allowed_permissions": [
      "downloads"
    ], 
    "blocked_permissions": [
      "wallpaper"
    ], 
    "installation_mode": "allowed"
  }
}
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ExtensionSettings
  - Valor de exemplo:
``` xml
<key>ExtensionSettings</key>
<dict>
  <key>*</key>
  <dict>
    <key>allowed_types</key>
    <array>
      <string>hosted_app</string>
    </array>
    <key>blocked_install_message</key>
    <string>Custom error message.</string>
    <key>blocked_permissions</key>
    <array>
      <string>downloads</string>
      <string>bookmarks</string>
    </array>
    <key>install_sources</key>
    <array>
      <string>https://company-intranet/apps</string>
    </array>
    <key>installation_mode</key>
    <string>blocked</string>
    <key>runtime_allowed_hosts</key>
    <array>
      <string>*://good.contoso.com</string>
    </array>
    <key>runtime_blocked_hosts</key>
    <array>
      <string>*://*.contoso.com</string>
    </array>
  </dict>
  <key>abcdefghijklmnopabcdefghijklmnop</key>
  <dict>
    <key>blocked_permissions</key>
    <array>
      <string>history</string>
    </array>
    <key>installation_mode</key>
    <string>allowed</string>
    <key>minimum_version_required</key>
    <string>1.0.1</string>
  </dict>
  <key>bcdefghijklmnopabcdefghijklmnopa</key>
  <dict>
    <key>allowed_permissions</key>
    <array>
      <string>downloads</string>
    </array>
    <key>installation_mode</key>
    <string>force_installed</string>
    <key>runtime_allowed_hosts</key>
    <array>
      <string>*://good.contoso.com</string>
    </array>
    <key>runtime_blocked_hosts</key>
    <array>
      <string>*://*.contoso.com</string>
    </array>
    <key>update_url</key>
    <string>https://contoso.com/update_url</string>
  </dict>
  <key>cdefghijklmnopabcdefghijklmnopab</key>
  <dict>
    <key>blocked_install_message</key>
    <string>Custom error message.</string>
    <key>installation_mode</key>
    <string>blocked</string>
  </dict>
  <key>defghijklmnopabcdefghijklmnopabc,efghijklmnopabcdefghijklmnopabcd</key>
  <dict>
    <key>blocked_install_message</key>
    <string>Custom error message.</string>
    <key>installation_mode</key>
    <string>blocked</string>
  </dict>
  <key>fghijklmnopabcdefghijklmnopabcde</key>
  <dict>
    <key>blocked_install_message</key>
    <string>Custom removal message.</string>
    <key>installation_mode</key>
    <string>removed</string>
  </dict>
  <key>update_url:https://www.contoso.com/update.xml</key>
  <dict>
    <key>allowed_permissions</key>
    <array>
      <string>downloads</string>
    </array>
    <key>blocked_permissions</key>
    <array>
      <string>wallpaper</string>
    </array>
    <key>installation_mode</key>
    <string>allowed</string>
  </dict>
</dict>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ## Políticas de autenticação HTTP

  [Voltar ao início](#microsoft-edge---policies)

  ### AllowCrossOriginAuthPrompt
  #### Permitir solicitações de autenticação HTTP Cross-Origin
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Controla se imagens de terceiros em uma página podem mostrar um aviso de autenticação.

Geralmente, isso é desabilitado como uma defesa contra phishing. Se você não configurar essa política, ela será desabilitada e imagens de terceiros não poderão exibir um aviso de autenticação.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: AllowCrossOriginAuthPrompt
  - Nome da GP: permitir avisos de autenticação HTTP Cross-Origin
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/HTTP authentication
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do Valor: AllowCrossOriginAuthPrompt
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000000
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: AllowCrossOriginAuthPrompt
  - Valor de exemplo:
``` xml
<false/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### AuthNegotiateDelegateAllowlist
  #### Especifica uma lista de servidores para os quais o Microsoft Edge pode delegar credenciais de usuário
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Configure a lista de servidores que o Microsoft Edge pode delegar.

Separe vários nomes de servidor com vírgulas. Caracteres curinga (*) são permitidos.

Se você não configurar essa política, o Microsoft Edge não delegará credenciais de usuário, mesmo que um servidor seja detectado como intranet.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: não requer a reinicialização do navegador

  #### Tipo de dados:
  - String

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: AuthNegotiateDelegateAllowlist
  - Nome da Política de Grupo: Especifica uma lista de servidores para os quais o Microsoft Edge pode delegar credenciais de usuário
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/HTTP authentication
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do Valor: AuthNegotiateDelegateAllowlist
  - Tipo do valor: REG_SZ
  ##### Valor de exemplo:
```
"contoso.com"
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: AuthNegotiateDelegateAllowlist
  - Valor de exemplo:
``` xml
<string>contoso.com</string>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### AuthSchemes
  #### Esquemas de autenticação com suporte
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Especifica quais esquemas de autenticação HTTP são compatíveis.

Você pode configurar a política usando estes valores: 'basic', 'digest', 'ntlm', and 'negotiate'. Separe vários valores com vírgulas.

Se você não configurar essa política, todos os quatro esquemas serão usados.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: não requer a reinicialização do navegador

  #### Tipo de dados:
  - String

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: AuthSchemes
  - Nome da Política de Grupo: Esquemas de autenticação com suporte
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/HTTP authentication
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: AuthSchemes
  - Tipo do valor: REG_SZ
  ##### Valor de exemplo:
```
"basic,digest,ntlm,negotiate"
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: AuthSchemes
  - Valor de exemplo:
``` xml
<string>basic,digest,ntlm,negotiate</string>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### AuthServerAllowlist
  #### Configurar a lista de servidores de autenticação permitidos
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Especifica quais servidores devem ser habilitados para autenticação integrada. A autenticação integrada só é habilitada quando o Microsoft Edge recebe um desafio de autenticação de um proxy ou de um servidor nesta lista.

Separe vários nomes de servidor com vírgulas. Caracteres curinga (*) são permitidos.

Se você não configurar essa política, o Microsoft Edge tentará detectar se um servidor está somente na intranet e responderá à solicitações IWA. Se o servidor estiver na Internet, as solicitações IWA dele serão ignoradas pelo Microsoft Edge.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: não requer a reinicialização do navegador

  #### Tipo de dados:
  - String

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: AuthServerAllowlist
  - Nome da Política de Grupo: Configurar lista de servidores de autenticação permitidos
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/HTTP authentication
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: AuthServerAllowlist
  - Tipo do valor: REG_SZ
  ##### Valor de exemplo:
```
"*contoso.com,contoso.com"
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: AuthServerAllowlist
  - Valor de exemplo:
``` xml
<string>*contoso.com,contoso.com</string>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### DisableAuthNegotiateCnameLookup
  #### Desabilitar a pesquisa CNAME durante a negociação da autenticação Kerberos
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Determina se o SPN Kerberos gerado se baseia no nome DNS canônico (CNAME) ou no nome original inserido.

Se você habilitar essa política, a pesquisa CNAME será ignorada, e o nome do servidor (conforme inserido) será usado.

Se você desabilitar essa política ou não a configurar, será usado o nome canônico do servidor.  Isso é determinado através da pesquisa CNAME.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: não requer a reinicialização do navegador

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: DisableAuthNegotiateCnameLookup
  - Nome da Política de Grupo: Desabilitar a pesquisa CNAME durante a negociação da autenticação Kerberos
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/HTTP authentication
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do Valor: DisableAuthNegotiateCnameLookup
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000000
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: DisableAuthNegotiateCnameLookup
  - Valor de exemplo:
``` xml
<false/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### EnableAuthNegotiatePort
  #### Incluir porta não padrão no SPN Kerberos
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Especifica se o SPN Kerberos gerado deve incluir uma porta não padrão.

Se você habilitar essa política, e o usuário incluir uma porta não padrão (uma porta diferente de 80 ou 443) em uma URL, essa porta será incluída no SPN Kerberos gerado.

Se você não configurar ou desabilitar essa política, o SPN Kerberos gerado não incluirá uma porta em nenhum caso.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: não requer a reinicialização do navegador

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: EnableAuthNegotiatePort
  - Nome da Política de Grupo: Incluir porta não padrão no SPN Kerberos
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/HTTP authentication
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: EnableAuthNegotiatePort
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000000
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: EnableAuthNegotiatePort
  - Valor de exemplo:
``` xml
<false/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### NtlmV2Enabled
  #### Controlar se a autenticação NTLMv2 está habilitada
  
  
  #### Versões com suporte:
  - No macOS desde 77 ou posterior

  #### Descrição
  Controla se o NTLMv2 está habilitado.

Todas as versões recentes dos servidores do Samba e do Windows oferecem suporte a NTLMv2. Você só deve desabilitar o NTLMv2 para resolver problemas de compatibilidade com versões anteriores, pois isso reduz a segurança de autenticação.

Se você não configurar essa política, o NTLMv2 estará habilitado por padrão.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  

  #### Informações e configurações do Mac
  - Nome da chave de preferência: NtlmV2Enabled
  - Valor de exemplo:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ## Configurações de política do modo de quiosque

  [Voltar ao início](#microsoft-edge---policies)

  ### KioskDeleteDownloadsOnExit
  #### Excluir arquivos baixados como parte de uma sessão Kiosk quando o Microsoft Edge for fechado
  
  
  #### Versões com suporte:
  - No Windows desde 87 ou posterior

  #### Descrição
  Observação: essa política só tem suporte quando o Edge é inicializado com o parâmetro de linha de comando "--Edge-Kiosk-tipo".

Se você habilitar essa política, os arquivos baixados como parte da sessão Kiosk serão excluídos sempre que o Microsoft Edge for fechado.

Se você desabilitar essa política ou não a configurar, os arquivos baixados como parte da sessão Kiosk não serão excluídos quando o Microsoft Edge for fechado.

Para obter informações detalhadas sobre como configurar o modo de quiosque, confira [https://go.microsoft.com/fwlink/?linkid=2137578](https://go.microsoft.com/fwlink/?linkid=2137578).

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: não requer a reinicialização do navegador

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: KioskDeleteDownloadsOnExit
  - Nome da GP: excluir arquivos baixados como parte de uma sessão Kiosk quando o Microsoft Edge é fechado
  - Caminho da GP (obrigatório): modelos administrativos/Microsoft Edge/configurações do modo de quiosque
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: KioskDeleteDownloadsOnExit
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  

  [Voltar ao início](#microsoft-edge---policies)

  ## Políticas de mensagens nativas

  [Voltar ao início](#microsoft-edge---policies)

  ### NativeMessagingAllowlist
  #### Controlar quais hosts nativos de mensagens os usuários podem usar
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Liste hosts de mensagens nativos específicos que os usuários podem usar no Microsoft Edge.

Por padrão, todos os hosts de mensagens nativos são permitidos. Se você definir a política [NativeMessagingBlocklist](#nativemessagingblocklist) como *, todos os hosts de mensagens nativos serão bloqueados e somente hosts de mensagens nativos listados neste artigo serão carregados.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: NativeMessagingAllowlist
  - Nome da Política de Grupo: Controlar quais hosts de mensagem nativos os usuários podem usar
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/Native Messaging
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge\NativeMessagingAllowlist
  - Caminho (recomendado): N/A
  - Nome do valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de exemplo:
```
SOFTWARE\Policies\Microsoft\Edge\NativeMessagingAllowlist\1 = "com.native.messaging.host.name1"
SOFTWARE\Policies\Microsoft\Edge\NativeMessagingAllowlist\2 = "com.native.messaging.host.name2"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: NativeMessagingAllowlist
  - Valor de exemplo:
``` xml
<array>
  <string>com.native.messaging.host.name1</string>
  <string>com.native.messaging.host.name2</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### NativeMessagingBlocklist
  #### Configurar lista de bloqueio de mensagens nativas
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Especifica quais hosts de mensagens nativos não devem ser usados.

Use "*" para bloquear todos os hosts de mensagens nativos, a menos que estejam explicitamente listados na lista de permissões.

Se você não configurar essa política, o Microsoft Edge carregará todos os hosts de mensagens nativos instalados.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: NativeMessagingBlocklist
  - Nome da Política de Grupo: Configurar a lista de bloqueio de mensagens nativa
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/Native Messaging
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge\NativeMessagingBlocklist
  - Caminho (recomendado): N/A
  - Nome do valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de exemplo:
```
SOFTWARE\Policies\Microsoft\Edge\NativeMessagingBlocklist\1 = "com.native.messaging.host.name1"
SOFTWARE\Policies\Microsoft\Edge\NativeMessagingBlocklist\2 = "com.native.messaging.host.name2"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: NativeMessagingBlocklist
  - Valor de exemplo:
``` xml
<array>
  <string>com.native.messaging.host.name1</string>
  <string>com.native.messaging.host.name2</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### NativeMessagingUserLevelHosts
  #### Permitir hosts de mensagens nativas em nível de usuário (instalado sem permissões de administrador)
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Permite a instalação em nível de usuário de hosts nativos de mensagens.

Se você desabilitar essa política, o Microsoft Edge usará somente hosts nativos de mensagens instaladas no nível do sistema.

Por padrão, quando você não configura essa política, o Microsoft Edge permite o uso de hosts de mensagens nativos no nível do usuário.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: NativeMessagingUserLevelHosts
  - Nome da Política de Grupo: Permitir hosts de mensagens nativos em nível de usuário (instalado sem permissões de administrador)
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/Native Messaging
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do Valor: NativeMessagingUserLevelHosts
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000000
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: NativeMessagingUserLevelHosts
  - Valor de exemplo:
``` xml
<false/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ## Gerenciador de senhas e políticas de proteção

  [Voltar ao início](#microsoft-edge---policies)

  ### PasswordManagerEnabled
  #### Habilitar o salvamento de senhas no gerenciador de senhas
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Habilitar o Microsoft Edge para salvar senhas do usuário.

Se você habilitar essa política, os usuários poderão salvar suas senhas no Microsoft Edge. Na próxima vez que visitar o site, o Microsoft Edge inserirá a senha automaticamente.

Se você desabilitar essa política, os usuários não poderão salvar novas senhas, mas ainda poderão usar senhas salvas anteriormente.

Se você habilitar ou desabilitar essa política, os usuários não podem alterá-la ou substituí-la no Microsoft Edge. Se você não configurá-lo, os usuários poderão salvar senhas, além de desativar esse recurso.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: Sim
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: PasswordManagerEnabled
  - Nome da Política de Grupo: Habilitar o salvamento de senhas no gerenciador de senhas
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/Password manager and protection
  - Caminho da Política de Grupo (recomendado): Administrative Templates/Microsoft Edge - Default Settings (usuários podem substituir)/Password manager and protection
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nome do valor: PasswordManagerEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: PasswordManagerEnabled
  - Valor de exemplo:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### PasswordMonitorAllowed
  #### Permitir que os usuários sejam alertados caso suas senhas não sejam seguras
  
  
  #### Versões com suporte:
  - No Windows desde 85 ou posterior

  #### Descrição
  Permitir o Microsoft Edge de monitorar senhas do usuário.

Se você habilitar essa política e um usuário consentir a habilitação da política, ele será alertado se qualquer uma das suas senhas armazenadas no Microsoft Edge for considerada insegura. O Microsoft Edge mostrará um alerta e essas informações também estarão disponíveis em Configurações > Senhas > Monitor de senhas.

Se você desabilitar essa política, os usuários não precisarão de permissão para habilitar esse recurso. As senhas não serão verificadas e não serão alertadas.

Se você habilitar ou não configurar a política, os usuários poderão ativar ou desativar esse recurso.

Para saber mais sobre como o Microsoft Edge localiza senhas perigosas consulte [https://go.microsoft.com/fwlink/?linkid=2133833](https://go.microsoft.com/fwlink/?linkid=2133833)

Orientações adicionais:

Essa política pode ser definida como recomendável e obrigatória, mas com um texto explicativo importante.

Obrigatório habilitado: devido a um consentimento de usuário individual ser uma pré-condição para habilitar esse recurso para um determinado usuário, essa política não tem uma configuração habilitada obrigatória. Se a política estiver definida como Obrigatèoria, a interface do usuário em configurações não será alterada e a seguinte mensagem de erro será exibida no edge://policy

Exemplo de mensagem de estado de erro: "Esse valor de política é ignorado porque o Monitor de Senhas exige que o usuário individual seja ativado. Você pode solicitar que os usuários da organização acedam às Configurações > Perfil > Senha e ativar o recurso".

Recomendado habilitado: se a política estiver definida como Recomendada, a interface do usuário nas configurações permanecerá no estado 'desativado', mas um ícone de maleta ficará visível ao lado dessa descrição exibida em foco: "Sua organização recomenda um valor específico para essa configuração e você escolheu um valor diferente".

Obrigatório e Recomendado desabilitado: esses estados funcionam de maneira normal, com as legendas usuais exibidas para os usuários.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: Sim
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: PasswordManagerEnabled
  - Política de Grupo: Permitir que os usuários sejam alertados caso suas senhas não sejam seguras
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/Password manager and protection
  - Caminho da Política de Grupo (recomendado): Administrative Templates/Microsoft Edge - Default Settings (usuários podem substituir)/Password manager and protection
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nome do valor: PasswordManagerEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  

  [Voltar ao início](#microsoft-edge---policies)

  ### PasswordProtectionChangePasswordURL
  #### Configurar a URL de alteração de senha
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Configura a URL de alteração de senha (somente esquemas HTTP e HTTPS).

O serviço de proteção por senha enviará usuários para esta URL para alterar a senha depois de ver um aviso no navegador.

Se você habilitar essa política, o serviço de proteção por senha enviará os usuários para esta URL para alterar a senha deles.

Se você desabilitar essa política ou não a configurar, o serviço de proteção por senha não redirecionará os usuários para uma URL de alteração de senha.

Essa política está disponível apenas nas instâncias do Windows que fazem parte de um domínio do Microsoft Active Directory, em instâncias do Windows 10 Pro ou Enterprise que estejam inscritas no gerenciamento de dispositivos ou em instâncias do macOS que são gerenciadas por meio do MDM ou passaram a fazer parte de um domínio por meio de MCX.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - String

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: PasswordProtectionChangePasswordURL
  - Nome da Política de Grupo: Configurar a URL de alteração de senha
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/Password manager and protection
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do Valor: PasswordProtectionChangePasswordURL
  - Tipo do valor: REG_SZ
  ##### Valor de exemplo:
```
"https://contoso.com/change_password.html"
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: PasswordProtectionChangePasswordURL
  - Valor de exemplo:
``` xml
<string>https://contoso.com/change_password.html</string>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### PasswordProtectionLoginURLs
  #### Configurar a lista de URLs de logon corporativos onde o serviço de proteção por senha deve capturar os hashes com sal de uma senha
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Configure a lista de URLs de logon corporativo (somente esquemas HTTP e HTTPS) em que o Microsoft Edge deve capturar os hashes de sal de senhas e usá-la para detectar a reutilização de senhas.

Se você habilitar essa política, o serviço de proteção por senha captura as impressões digitais das senhas nas URLs definidas.

Se você desabilitar essa política ou não a configurar, nenhuma impressão digital de senha será capturada.

Essa política está disponível apenas nas instâncias do Windows que fazem parte de um domínio do Microsoft Active Directory, em instâncias do Windows 10 Pro ou Enterprise que estejam inscritas no gerenciamento de dispositivos ou em instâncias do macOS que são gerenciadas por meio do MDM ou passaram a fazer parte de um domínio por meio de MCX.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: PasswordProtectionLoginURLs
  - Configurar a lista de URLs de logon corporativos onde o serviço de proteção por senha deve capturar os salted hashes de uma senha
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/Password manager and protection
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge\PasswordProtectionLoginURLs
  - Caminho (recomendado): N/A
  - Nome do valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de exemplo:
```
SOFTWARE\Policies\Microsoft\Edge\PasswordProtectionLoginURLs\1 = "https://contoso.com/login.html"
SOFTWARE\Policies\Microsoft\Edge\PasswordProtectionLoginURLs\2 = "https://login.contoso.com"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: PasswordProtectionLoginURLs
  - Valor de exemplo:
``` xml
<array>
  <string>https://contoso.com/login.html</string>
  <string>https://login.contoso.com</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### PasswordProtectionWarningTrigger
  #### Configurar o gatilho de aviso de proteção por senha
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Permite que você controle quando o alerta de proteção por senha deve ser acionado. A proteção por senha alerta os usuários quando eles reutilizam suas senhas protegidas em sites potencialmente suspeitos.

Você pode usar as políticas [PasswordProtectionLoginURLs](#passwordprotectionloginurls) e [PasswordProtectionChangePasswordURL](#passwordprotectionchangepasswordurl) para configurar quais senhas proteger.

Isenções: senhas para os sites listados em [PasswordProtectionLoginURLs](#passwordprotectionloginurls) e [PasswordProtectionChangePasswordURL](#passwordprotectionchangepasswordurl), bem como para sites listados em [SmartScreenAllowListDomains](#smartscreenallowlistdomains), não acionarão um aviso de proteção de senha.

Definir como "PasswordProtectionWarningOff" para não mostrar o alerta de proteção por senha.

Definir como "PasswordProtectionWarningOnPasswordReuse" para mostrar avisos de proteção por senha quando o usuário reutilizar sua senha protegida em um site que não esteja na lista de permissão.

Se você desabilitar ou não configurar essa política, o gatilho de aviso não será exibido.

Mapeamento das opções de política:

* PasswordProtectionWarningOff (0) = O aviso de proteção por senha está desativado

* PasswordProtectionWarningOnPasswordReuse (1) = O aviso de proteção por senha é acionado por reutilização de senha

Use as informações anteriores ao configurar essa política.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Inteiro

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: PasswordProtectionWarningTrigger
  - Nome da Política de Grupo: Configurar o gatilho de aviso de proteção por senha
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/Password manager and protection
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: PasswordProtectionWarningTrigger
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: PasswordProtectionWarningTrigger
  - Valor de exemplo:
``` xml
<integer>1</integer>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ## Políticas de impressão

  [Voltar ao início](#microsoft-edge---policies)

  ### DefaultPrinterSelection
  #### Regras de seleção de impressora padrão
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Substitui as regras de seleção da impressora padrão do Microsoft Edge. Essa política determina as regras para selecionar a impressora padrão no Microsoft Edge, o que acontece na primeira vez que um usuário tenta imprimir uma página.

Quando essa política estiver definida, o Microsoft Edge tentará encontrar uma impressora que corresponda a todos os atributos especificados e a usará como impressora padrão. Se houver várias impressoras que atendem aos critérios, a primeira impressora será usada.

Se você não configurar essa política ou se nenhuma impressora correspondente for encontrada durante o tempo limite, o padrão da impressora será a impressora de PDF embutida ou nenhuma impressora, se a impressora de PDF não estiver disponível.

O valor é analisado como um objeto JSON, de acordo com o esquema a seguir: { "type": "object", "properties": { "idPattern": { "description": "Regular expression to match printer id.", "type": "string" }, "namePattern": { "description": "Regular expression to match printer display name.", "type": "string" } } }

Omitir um campo significa que todos os valores são correspondentes. Por exemplo, se você não especificar a conectividade da impressora, a visualização de impressão começará a descobrir todos os tipos de impressoras locais. Padrões de expressão regular devem seguir a sintaxe RegExp do JavaScript e as correspondências diferenciam maiúsculas de minúsculas.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - String

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: DefaultPrinterSelection
  - Nome da Política de Grupo: Regras de seleção de impressora padrão
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/Printing
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: DefaultPrinterSelection
  - Tipo do valor: REG_SZ
  ##### Valor de exemplo:
```
"{ \"idPattern\": \".*public\", \"namePattern\": \".*Color\" }"
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: DefaultPrinterSelection
  - Valor de exemplo:
``` xml
<string>{ "idPattern": ".*public", "namePattern": ".*Color" }</string>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### PrintHeaderFooter
  #### Imprimir cabeçalhos e rodapés
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Forçar 'cabeçalhos e rodapés' a serem ativados ou desativados na caixa de diálogo de impressão.

Se você não configurar essa política, os usuários poderão decidir se desejam imprimir cabeçalhos e rodapés.

Se você desabilitar essa política, os usuários não poderão imprimir cabeçalhos e rodapés.

Se você habilitar essa política, os usuários sempre poderão imprimir cabeçalhos e rodapés.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: Sim
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: PrintHeaderFooter
  - Nome da Política de Grupo: Imprimir cabeçalhos e rodapés
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/Printing
  - Caminho da Política de Grupo (recomendado): Administrative Templates/Microsoft Edge - Default Settings (usuários podem substituir)/Printing
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nome do valor: PrintHeaderFooter
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000000
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: PrintHeaderFooter
  - Valor de exemplo:
``` xml
<false/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### PrintPreviewUseSystemDefaultPrinter
  #### Definir a impressora padrão do sistema como impressora padrão
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Diz ao Microsoft Edge para usar a impressora padrão do sistema como a opção padrão na visualização de impressão, em vez de na impressora usada mais recentemente.

Se você desabilitar essa política ou não a configurar, a visualização de impressão usará a impressora usada recentemente como a opção de destino padrão.

Se você habilitar essa política, a visualização de impressão usará a impressora padrão do sistema operacional como a opção de destino padrão.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: Sim
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: PrintPreviewUseSystemDefaultPrinter
  - Nome da Política de Grupo: definir a impressora padrão do sistema como a impressora padrão
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/Printing
  - Caminho da Política de Grupo (recomendado): Administrative Templates/Microsoft Edge - Default Settings (usuários podem substituir)/Printing
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nome do Valor: PrintPreviewUseSystemDefaultPrinter
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000000
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: PrintPreviewUseSystemDefaultPrinter
  - Valor de exemplo:
``` xml
<false/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### PrintingEnabled
  #### Habilitar impressão
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Permite a impressão no Microsoft Edge e impede que os usuários alterem essa configuração.

Se você habilitar essa política ou não a configurar, os usuários poderão imprimir.

Se você desabilitar essa política, os usuários não poderão imprimir no Microsoft Edge. A impressão está desabilitada no menu chave, extensões, aplicativos JavaScript e assim por diante. Os usuários ainda podem imprimir de plug-ins que ignoram o Microsoft Edge durante a impressão. Por exemplo, determinados aplicativos do Adobe Flash têm a opção imprimir no menu de contexto, que não é coberto por esta política.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: PrintingEnabled
  - Nome da Política de Grupo: Habilitar a impressão
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/Printing
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: PrintingEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: PrintingEnabled
  - Valor de exemplo:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### PrintingPaperSizeDefault
  #### Tamanho da página de impressão padrão
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 86 ou mais recente

  #### Descrição
  Substitui o tamanho da página de impressão padrão.

O nome deve conter um dos formatos listados ou “personalizado” se o tamanho do papel necessário não estiver na lista. Se o valor “custom” for fornecido, a propriedade custom_size deve ser especificada. Ele descreve a altura e a largura desejadas em micrômetros. Caso contrário, a propriedade custom_size não deve ser especificada. A política que viola estas regras será ignorada.

Se o tamanho da página não estiver disponível na impressora escolhida pelo usuário, esta política será ignorada.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Dictionary

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: PrintingPaperSizeDefault
  - Nome da Política de Grupo: Tamanho da página de impressão padrão
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/Printing
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: PrintingPaperSizeDefault
  - Tipo do valor: REG_SZ
  ##### Valor de exemplo:
```
SOFTWARE\Policies\Microsoft\Edge\PrintingPaperSizeDefault = {
  "custom_size": {
    "height": 297000, 
    "width": 210000
  }, 
  "name": "custom"
}
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: PrintingPaperSizeDefault
  - Valor de exemplo:
``` xml
<key>PrintingPaperSizeDefault</key>
<dict>
  <key>custom_size</key>
  <dict>
    <key>height</key>
    <integer>297000</integer>
    <key>width</key>
    <integer>210000</integer>
  </dict>
  <key>name</key>
  <string>custom</string>
</dict>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### UseSystemPrintDialog
  #### Imprimir usando a caixa de diálogo de impressão do sistema
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Mostra a caixa de diálogo impressão do sistema, em vez de visualização de impressão.

Se você habilitar essa política, o Microsoft Edge abrirá a caixa de diálogo Impressão do sistema, em vez de visualização de impressão interna, quando um usuário imprimir uma página.

Se você não configurar ou desabilitar essa política, os comandos de impressão acionarão a tela de visualização de impressão do Microsoft Edge.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: não requer a reinicialização do navegador

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: UseSystemPrintDialog
  - Nome da Política de Grupo: Imprimir usando a caixa de diálogo de impressão do sistema
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/Printing
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: UseSystemPrintDialog
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000000
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: UseSystemPrintDialog
  - Valor de exemplo:
``` xml
<false/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ## Políticas do servidor proxy

  [Voltar ao início](#microsoft-edge---policies)

  ### ProxyBypassList
  #### Configurar regras de bypass de proxy
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Define uma lista de hosts para os quais o Microsoft Edge ignorará o proxy.

Essa política será aplicada somente se você tiver selecionado a opção ' usar servidores de proxy fixo ' na política [Proxymode](#proxymode). Se você tiver selecionado qualquer outro modo para configurar as políticas de proxy, não habilite ou configure esta política.

Se você habilitar essa política, poderá criar uma lista de hosts para os quais o Microsoft Edge não usa um proxy.

Se você não configurar essa política, nenhuma lista de hosts será criada para que o Microsoft Edge ignore um proxy. Deixe essa política desconfigurada se você tiver especificado qualquer outro método para a configuração das políticas de proxy.

Para obter exemplos mais detalhados, acesse [https://go.microsoft.com/fwlink/?linkid=2094936](https://go.microsoft.com/fwlink/?linkid=2094936).

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - String

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: ProxyBypassList
  - Nome da Política de Grupo: Configurar regras de bypass de proxy
  - Caminho da Política de Grupo: Administrative Templates/Microsoft Edge/Proxy server
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: ProxyBypassList
  - Tipo do valor: REG_SZ
  ##### Valor de exemplo:
```
"https://www.contoso.com, https://www.fabrikam.com"
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ProxyBypassList
  - Valor de exemplo:
``` xml
<string>https://www.contoso.com, https://www.fabrikam.com</string>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### ProxyMode
  #### Definir configurações do servidor proxy.
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Especificar as configurações de servidor proxy usadas pelo Microsoft Edge. Se você habilitar essa política, os usuários não poderão alterar as configurações de proxy.

Se você optar por nunca usar um servidor proxy e sempre se conectar diretamente, todas as outras opções serão ignoradas.

Se você optar por usar as configurações de proxy do sistema, todas as outras opções serão ignoradas.

Se você optar por detectar automaticamente o servidor proxy, todas as outras opções serão ignoradas.

Se você escolher o modo de proxy de servidor fixo, poderá especificar mais opções em [ProxyServer](#proxyserver) e em uma lista de regras de bypass de proxy separadas por vírgulas.

Se você optar por usar um script de proxy .pac, especifique a URL do script em "A URL para um arquivo .pac de proxy".

Para obter exemplos detalhados, vá para [https://go.microsoft.com/fwlink/?linkid=2094936](https://go.microsoft.com/fwlink/?linkid=2094936).

Se você habilitar essa política, o Microsoft Edge ignorará todas as opções relacionadas ao proxy especificadas da linha de comando.

Se você não configurar essa política, os usuários poderão escolher suas próprias configurações de proxy.

Mapeamento das opções de política:

* ProxyDisabled (direto) = Nunca usar um proxy

* ProxyAutoDetect (auto_detect) = Detecção automática de configurações de proxy

* ProxyPacScript (pac_script) = Usar um script de proxy .pac

* ProxyFixedServers (fixed_servers) = Usar servidores proxy fixos

* ProxyUseSystem (sistema) = Usar as configurações de proxy do sistema

Use as informações anteriores ao configurar essa política.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - String

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: ProxyMode
  - Nome da Política de Grupo: Definir configurações do servidor proxy.
  - Caminho da Política de Grupo: Administrative Templates/Microsoft Edge/Proxy server
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: ProxyMode
  - Tipo do valor: REG_SZ
  ##### Valor de exemplo:
```
"direct"
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: Proxymode
  - Valor de exemplo:
``` xml
<string>direct</string>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### ProxyPacUrl
  #### Defina o URL do arquivo .pac do proxy
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Especifica a URL de um arquivo PAC (proxy automático).

Essa política será aplicada somente se você tiver selecionado a opção "usar um. script proxy da PAC" na política [Proxymode](#proxymode). Se você tiver selecionado qualquer outro modo para configurar as políticas de proxy, não habilite ou configure esta política.

Se você habilitar essa política, poderá especificar a URL de um arquivo PAC, que define como o navegador escolherá automaticamente o servidor proxy apropriado para procurar um site específico.

Se você desabilitar ou não configurar essa política, nenhum arquivo PAC será especificado. Deixe essa política desconfigurada se você tiver especificado qualquer outro método para a configuração das políticas de proxy.

Para obter exemplos detalhados, confira [https://go.microsoft.com/fwlink/?linkid=2094936](https://go.microsoft.com/fwlink/?linkid=2094936).

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - String

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: ProxyPacUrl
  - Nome da Política de Grupo: Defina o URL do arquivo .pac do proxy
  - Caminho da Política de Grupo: Administrative Templates/Microsoft Edge/Proxy server
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: ProxyPacUrl
  - Tipo do valor: REG_SZ
  ##### Valor de exemplo:
```
"https://internal.contoso.com/example.pac"
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ProxyPacUrl
  - Valor de exemplo:
``` xml
<string>https://internal.contoso.com/example.pac</string>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### ProxyServer
  #### Configurar o endereço ou a URL do servidor proxy
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Especifica a URL do servidor proxy.

Essa política será aplicada somente se você tiver selecionado a opção ' usar servidores de proxy fixo ' na política [Proxymode](#proxymode). Se você tiver selecionado qualquer outro modo para configurar as políticas de proxy, não habilite ou configure esta política.

Se você habilitar essa política, o servidor proxy configurado por essa política será usado para todas as URLs.

Se você desabilitar ou não configurar essa política, os usuários poderão escolher suas próprias configurações de proxy durante esse modo de proxy. Deixe essa política desconfigurada se você tiver especificado qualquer outro método para a configuração das políticas de proxy.

Para obter mais opções e exemplos detalhados, confira [https://go.microsoft.com/fwlink/?linkid=2094936](https://go.microsoft.com/fwlink/?linkid=2094936).

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - String

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: ProxyServer
  - Nome da Política de Grupo: Configurar o endereço ou a URL do servidor proxy
  - Caminho da Política de Grupo: Administrative Templates/Microsoft Edge/Proxy server
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: ProxyServer
  - Tipo do valor: REG_SZ
  ##### Valor de exemplo:
```
"123.123.123.123:8080"
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ProxyServer
  - Valor de exemplo:
``` xml
<string>123.123.123.123:8080</string>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### ProxySettings
  #### Configurações de proxy
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Define as configurações de proxy para o Microsoft Edge.

Se você habilitar essa política, o Microsoft Edge ignorará todas as opções relacionadas ao proxy especificadas da linha de comando.

Se você não configurar essa política, os usuários poderão escolher suas próprias configurações de proxy.

Essa política substitui as seguintes políticas individuais:

[ProxyMode](#proxymode)
[ProxyPacUrl](#proxypacurl)
[ProxyServer](#proxyserver)
[ProxyBypassList](#proxybypasslist)

O campo Proxymode permite especificar o servidor proxy usado pelo Microsoft Edge e impede que os usuários alterem as configurações de proxy.

O campo ProxyPacUrl é uma URL para um arquivo .pac de proxy.

O campo ProxyServer é uma URL para o servidor proxy.

O campo ProxyBypassList é uma lista de hosts de proxy que o Microsoft Edge ignora.

Se você escolher o valor "direto" como "Proxymode", um proxy nunca será usado e todos os outros campos serão ignorados.

Se você escolher o valor "sistema" como "Proxymode", o proxy do sistema será usado e todos os outros campos serão ignorados.

Se você escolher o valor ' auto_detect ' como "Proxymode", todos os outros campos são ignorados.

Se você escolher o valor ' fixed_server ' como "Proxymode", os campos 'ProxyServer' e 'ProxyBypassList ' serão usados.

Se você escolher o valor ' pac_script ' como "Proxymode", os campos 'ProxyPacUrl' e 'ProxyBypassList ' serão usados.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Dictionary

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: ProxyServer
  - Nome da Política de Grupo: Configurações de proxy
  - Caminho da Política de Grupo: Administrative Templates/Microsoft Edge/Proxy server
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: ProxySettings
  - Tipo do valor: REG_SZ
  ##### Valor de exemplo:
```
SOFTWARE\Policies\Microsoft\Edge\ProxySettings = {
  "ProxyBypassList": "https://www.example1.com,https://www.example2.com,https://internalsite/", 
  "ProxyMode": "direct", 
  "ProxyPacUrl": "https://internal.site/example.pac", 
  "ProxyServer": "123.123.123.123:8080"
}
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ProxySettings
  - Valor de exemplo:
``` xml
<key>ProxySettings</key>
<dict>
  <key>ProxyBypassList</key>
  <string>https://www.example1.com,https://www.example2.com,https://internalsite/</string>
  <key>ProxyMode</key>
  <string>direct</string>
  <key>ProxyPacUrl</key>
  <string>https://internal.site/example.pac</string>
  <key>ProxyServer</key>
  <string>123.123.123.123:8080</string>
</dict>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ## Políticas de configurações do SmartScreen

  [Voltar ao início](#microsoft-edge---policies)

  ### PreventSmartScreenPromptOverride
  #### Evitar ignorar os avisos do Microsoft Defender SmartScreen para sites
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Esta configuração de política permite que você decida se os usuários podem ignorar os avisos do Microsoft Defender SmartScreen sobre sites potencialmente mal-intencionados.

Se você habilitar essa configuração, os usuários não poderão ignorar os avisos do Microsoft Defender SmartScreen nem continuar para acessar o site.

Se você desabilitar ou não definir essa configuração, os usuários poderão ignorar os avisos do Microsoft Defender SmartScreen e continuar para acessar o site.

Essa política está disponível apenas nas instâncias do Windows que fazem parte de um domínio do Microsoft Active Directory, em instâncias do Windows 10 Pro ou Enterprise que estejam inscritas no gerenciamento de dispositivos ou em instâncias do macOS que são gerenciadas por meio do MDM ou passaram a fazer parte de um domínio por meio de MCX.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: PreventSmartScreenPromptOverride
  - Nome da Política de Grupo: Evitar ignorar os avisos do Microsoft Defender SmartScreen para sites
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/SmartScreen settings
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome da Política de Grupo: PreventSmartScreenPromptOverride
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da Chave de Preferência: PreventSmartScreenPromptOverride
  - Valor de exemplo:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### PreventSmartScreenPromptOverrideForFiles
  #### Impedir que os avisos do Microsoft Defender SmartScreen sobre download sejam ignorados
  
  
  #### Versões com suporte:
  - No Windows desde 77 ou posterior
  - No macOS desde 79 ou posterior

  #### Descrição
  Essa política permite determinar se os usuários podem substituir os avisos do Microsoft Defender SmartScreen sobre downloads não verificados.

Se você habilitar essa política, os usuários em sua organização não poderão ignorar os avisos do Microsoft Defender SmartScreen e serão impedidos de concluir os downloads não verificados.

Se você desabilitar ou não configurar essa política, os usuários poderão ignorar os avisos do Microsoft Defender SmartScreen e concluir downloads não verificados.

Essa política está disponível apenas nas instâncias do Windows que fazem parte de um domínio do Microsoft Active Directory, em instâncias do Windows 10 Pro ou Enterprise que estejam inscritas no gerenciamento de dispositivos ou em instâncias do macOS que são gerenciadas por meio do MDM ou passaram a fazer parte de um domínio por meio de MCX.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: PreventSmartScreenPromptOverrideForFiles
  - Nome da Política de Grupo: Impedir que os avisos do Microsoft Defender SmartScreen sobre download sejam ignorados
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/SmartScreen settings
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome da Política de Grupo: PreventSmartScreenPromptOverrideForFiles
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da Chave de Preferência: PreventSmartScreenPromptOverrideForFiles
  - Valor de exemplo:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### SmartScreenAllowListDomains
  #### Configurar a lista de domínios para os quais o Microsoft Defender SmartScreen não desencadeará avisos
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Configurar a lista de domínios confiáveis do Microsoft Defender SmartScreen. Isso significa que o Microsoft Defender SmartScreen não verificará se há recursos potencialmente mal intencionados, como software de phishing e outros malwares, caso as URLs de origem sejam correspondentes a esses domínios.
O serviço de proteção de download do Microsoft Defender SmartScreen não verificará os downloads hospedados nesses domínios.

Se você habilitar essa política, o Microsoft Defender SmartScreen confiará nesses domínios.
Se você desabilitar ou não definir essa política, a proteção do Microsoft Defender SmartScreen padrão será aplicada a todos os recursos.

Essa política está disponível apenas nas instâncias do Windows que fazem parte de um domínio do Microsoft Active Directory, em instâncias do Windows 10 Pro ou Enterprise que estejam inscritas no gerenciamento de dispositivos ou em instâncias do macOS que são gerenciadas por meio do MDM ou passaram a fazer parte de um domínio por meio de MCX.
Observe também que essa política não se aplica se a sua organização tiver habilitado a Proteção Avançada contra Ameaças do Microsoft Defender. Em vez disso, você deve configurar suas listas de permissão e bloqueio na Central de Segurança do Microsoft Defender.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: SmartScreenAllowListDomains
  - Nome da Política de Grupo: Configurar a lista de domínios para os quais o Microsoft Defender SmartScreen não desencadeará avisos
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/SmartScreen settings
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge\SmartScreenAllowListDomains
  - Caminho (recomendado): N/A
  - Nome do valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de exemplo:
```
SOFTWARE\Policies\Microsoft\Edge\SmartScreenAllowListDomains\1 = "mydomain.com"
SOFTWARE\Policies\Microsoft\Edge\SmartScreenAllowListDomains\2 = "myuniversity.edu"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: SmartScreenAllowListDomains
  - Valor de exemplo:
``` xml
<array>
  <string>mydomain.com</string>
  <string>myuniversity.edu</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### SmartScreenEnabled
  #### Configurar o Microsoft Defender SmartScreen
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Esta configuração de política permite configurar se o Microsoft Defender SmartScreen deve ser ativado. O Microsoft Defender SmartScreen fornece mensagens de alerta para ajudar a proteger seus usuários contra possíveis tentativas de phishing e softwares mal-intencionados. Por padrão, o Microsoft Defender SmartScreen está ativado.

Se você habilitar essa configuração, o Microsoft Defender SmartScreen será ativado.

Se você desabilitar essa configuração, o Microsoft Defender SmartScreen será desabilitado.

Se você não definir essa configuração, os usuários poderão optar por usar ou não o Microsoft Defender SmartScreen.

Essa política está disponível apenas nas instâncias do Windows que fazem parte de um domínio do Microsoft Active Directory, em instâncias do Windows 10 Pro ou Enterprise que estejam inscritas no gerenciamento de dispositivos ou em instâncias do macOS que são gerenciadas por meio do MDM ou passaram a fazer parte de um domínio por meio de MCX.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: Sim
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: SmartScreenEnabled
  - Nome da Política de Grupo: Configurar o Microsoft Defender SmartScreen
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/SmartScreen settings
  - Caminho da Política de Grupo (recomendado): Administrative Templates/Microsoft Edge - Default Settings (usuários podem substituir)/SmartScreen settings
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nome do valor: SmartScreenEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: SmartScreenEnabled
  - Valor de exemplo:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### SmartScreenForTrustedDownloadsEnabled
  #### Forçar o Microsoft Defender SmartScreen verifica downloads de fontes confiáveis
  
  
  #### Versões com suporte:
  - No Windows desde 78 ou posterior

  #### Descrição
  Essa configuração de política permite que você configure se o Microsoft Defender SmartScreen verificará a reputação de downloads de uma fonte confiável.

Se você habilitar ou não definir essa configuração, o Microsoft Defender SmartScreen verificará a reputação do download independentemente da origem.

Se você desabilitar essa configuração, o Microsoft Defender SmartScreen não verificará a reputação do download ao baixar de uma fonte confiável.

Essa política só está disponível em instâncias do Windows que fazem parte de um domínio do Microsoft Active Directory, instâncias do Windows 10 Pro ou Enterprise que foram inscritas no gerenciamento de dispositivos.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: Sim
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: SmartScreenForTrustedDownloadsEnabled
  - Nome da Política de Grupo: Forçar o Microsoft Defender SmartScreen verifica downloads de fontes confiáveis
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/SmartScreen settings
  - Caminho da Política de Grupo (recomendado): Administrative Templates/Microsoft Edge - Default Settings (usuários podem substituir)/SmartScreen settings
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nome do valor: SmartScreenForTrustedDownloadsEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000000
```


  

  [Voltar ao início](#microsoft-edge---policies)

  ### SmartScreenPuaEnabled
  #### Configura o Microsoft Defender SmartScreen para bloquear aplicativos potencialmente indesejados.
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 80 ou mais recente

  #### Descrição
  Essa configuração de política permite que você configure o bloqueio de aplicativos potencialmente indesejados com o Microsoft Defender SmartScreen. O bloqueio de aplicativos potencialmente indesejados com o Microsoft Defender SmartScreen fornece mensagens de aviso para ajudar a proteger os usuários de adware, mineiros de moeda, pacotes e outros aplicativos de baixa reputação hospedados em sites. O bloqueio de aplicativos potencialmente indesejados com o Microsoft Defender SmartScreen está desativado por padrão.

Se você habilitar essa configuração, o bloqueio de aplicativos potencialmente indesejados com o Microsoft Defender SmartScreen será ativado.

Se você desabilitar essa configuração, o bloqueio de aplicativos potencialmente indesejados no Microsoft Defender SmartScreen será desabilitado.

Se você não definir essa configuração, os usuários poderão optar por usar o bloqueio de aplicativos potencialmente indesejados no Microsoft Defender SmartScreen.

Essa política está disponível apenas nas instâncias do Windows que fazem parte de um domínio do Microsoft Active Directory, em instâncias do Windows 10 Pro ou Enterprise que estejam inscritas no gerenciamento de dispositivos ou em instâncias do macOS que são gerenciadas por meio do MDM ou passaram a fazer parte de um domínio por meio de MCX.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: Sim
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: SmartScreenPuaEnabled
  - Nome da Política de Grupo: Configura o Microsoft Defender SmartScreen para bloquear aplicativos potencialmente indesejados.
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/SmartScreen settings
  - Caminho da Política de Grupo (recomendado): Administrative Templates/Microsoft Edge - Default Settings (usuários podem substituir)/SmartScreen settings
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nome do valor: SmartScreenPuaEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: SmartScreenPuaEnabled
  - Valor de exemplo:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ## Página inicial&comma; de inicialização e políticas de nova guia

  [Voltar ao início](#microsoft-edge---policies)

  ### HomepageIsNewTabPage
  #### Definir a nova página da guia como página inicial
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Configura a página inicial padrão no Microsoft Edge. Você pode definir a página inicial para uma URL que você especificar ou para a página nova guia.

Se você habilitar essa política, a página nova guia sempre será usada para a página inicial e o local da URL da página inicial será ignorado.

Se você desabilitar essa política, a página inicial do usuário não poderá ser a página nova guia, a menos que a URL esteja definida como "edge://newtab".

Se não for configurada, os usuários poderão escolher se a página nova guia é a página inicial.

Essa política está disponível apenas nas instâncias do Windows que fazem parte de um domínio do Microsoft Active Directory, em instâncias do Windows 10 Pro ou Enterprise que estejam inscritas no gerenciamento de dispositivos ou em instâncias do macOS que são gerenciadas por meio do MDM ou passaram a fazer parte de um domínio por meio de MCX.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: Sim
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: HomepageIsNewTabPage
  - Nome da Política de Grupo: Definir a nova página da guia como página inicial
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/Startup, home page and new tab page
  - Caminho da Política de Grupo (recomendado): Administrative Templates/Microsoft Edge - Default Settings (usuários podem substituir)/Startup, home page and new tab page
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nome do valor: HomepageIsNewTabPage
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: HomepageIsNewTabPage
  - Valor de exemplo:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### HomepageLocation
  #### Configurar a URL da página inicial
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Configura a URL da página inicial padrão no Microsoft Edge.

A página inicial é a página aberta pelo botão página inicial. As páginas que abrem na inicialização são controladas pelas políticas [RestoreOnStartup](#restoreonstartup).

Você pode definir uma URL aqui ou definir a página inicial para abrir a página da nova guia. Se você optar por abrir a página nova guia, essa política não entrará em vigor.

Se você habilitar essa política, os usuários não poderão alterar a URL da Home Page, mas poderão usar a página nova guia como página inicial.

Se você desabilitar ou não configurar essa política, os usuários poderão escolher a própria página inicial, desde que a política [HomepageIsNewTabPage](#homepageisnewtabpage) não esteja habilitada.

Essa política está disponível apenas nas instâncias do Windows que fazem parte de um domínio do Microsoft Active Directory, em instâncias do Windows 10 Pro ou Enterprise que estejam inscritas no gerenciamento de dispositivos ou em instâncias do macOS que são gerenciadas por meio do MDM ou passaram a fazer parte de um domínio por meio de MCX.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: Sim
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - String

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: HomepageLocation
  - Nome da Política de Grupo: Configurar a URL da página inicial
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/Startup, home page and new tab page
  - Caminho da Política de Grupo (recomendado): Administrative Templates/Microsoft Edge - Default Settings (usuários podem substituir)/Startup, home page and new tab page
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nome do valor: HomepageLocation
  - Tipo do valor: REG_SZ
  ##### Valor de exemplo:
```
"https://www.contoso.com"
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: HomepageLocation
  - Valor de exemplo:
``` xml
<string>https://www.contoso.com</string>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### NewTabPageAllowedBackgroundTypes
  #### Configurar os tipos de plano de fundo permitidos para o layout da página nova guia
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 86 ou mais recente

  #### Descrição
  Você pode configurar quais tipos de imagem de tela de fundo são permitidas no layout da página nova guia no Microsoft Edge.

Se você não configurar essa política, todos os tipos de imagem de tela de fundo na página nova guia serão habilitados.

Mapeamento das opções de política:

* DisableImageOfTheDay (1) = Desabilitar o tipo de imagem do plano de fundo diário

* DisableCustomImage (2) = Desabilitar o tipo de imagem de tela de fundo personalizada

* DisableAll (3) = Desabilitar todos os tipos de imagem de tela de fundo

Use as informações anteriores ao configurar essa política.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Inteiro

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: NewTabPageAllowedBackgroundTypes
  - Nome da GP: Configurar os tipos de plano de fundo permitidos para o layout da página da nova guia
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/Startup, home page and new tab page
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do Valor: NewTabPageAllowedBackgroundTypes
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000002
```


  #### Informações e configurações do Mac
  - Nome da Chave de Preferência: NewTabPageAllowedBackgroundTypes
  - Valor de exemplo:
``` xml
<integer>2</integer>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### NewTabPageCompanyLogo
  #### Definir logotipo da empresa da página de nova guia (descontinuado)
  
  >OBSOLETA: Essa política está obsoleta e não funciona a partir da versão 85 do Microsoft Edge.
  #### Versões com suporte:
  - No Windows e no macOS, desde 79 até 85

  #### Descrição
  Esta política não funcionou conforme o esperado devido a alterações nos requisitos operacionais. Portanto, ela está obsoleta e não deve ser usada.

Especifica o logotipo da empresa a ser usado na página nova guia no Microsoft Edge.

A política deve ser configurada como uma cadeia de caracteres que expressa o logotipo (s) no formato JSON. Por exemplo: { "default_logo": { "url": "https://www.contoso.com/logo.png", "hash": "cd0aa9856147b6c5b4ff2b7dfee5da20aa38253099ef1b4a64aced233c9afe29" }, "light_logo": { "url": "https://www.contoso.com/light_logo.png", "hash": "517d286edb416bb2625ccfcba9de78296e90da8e32330d4c9c8275c4c1c33737" } }

Configure essa política especificando a URL a partir da qual o Microsoft Edge poderá baixar o logotipo e seu hash criptográfico (SHA-256), usado para verificar a integridade do download. O logotipo deve estar no formato PNG ou SVG, e o tamanho do arquivo não deve exceder 16 MB. O logotipo é baixado e armazenado em cache e será baixado sempre que a URL ou o hash for alterado. A URL deve estar acessível sem qualquer autenticação.

O 'default_logo' é obrigatório e será usado quando não houver nenhuma imagem de tela de fundo. Se o 'light_logo ' for fornecido, ele será usado quando a nova guia do usuário tiver uma imagem de tela de fundo. Recomendamos um logotipo horizontal com um plano de fundo transparente, alinhado à esquerda e centralizado verticalmente. O logotipo deve ter uma altura mínima de 32 pixels e uma taxa de proporção de 1:1 a 4:1. O 'default_logo' deve ter o contraste apropriado contra um plano de fundo branco ou preto, enquanto o 'light_logo' deve ter o contraste correto contra uma imagem de fundo.

Se você habilitar essa política, o Microsoft Edge será baixado e mostrará os logotipos especificados na página nova guia. Os usuários não podem substituir nem ocultar os logotipos.

Se você desabilitar ou não configurar essa política, o Microsoft Edge não mostrará o logotipo da empresa ou um logotipo da Microsoft na página nova guia.

Para obter ajuda na determinação do hash SHA-256, consulte https://docs.microsoft.com/powershell/module/microsoft.powershell.utility/get-filehash.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: não requer a reinicialização do navegador

  #### Tipo de dados:
  - Dictionary

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: NewTabPageCompanyLogo
  - Nome da Política de Grupo: Definir logotipo da empresa da página de nova guia (descontinuado)
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/Startup, home page and new tab page
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: NewTabPageCompanyLogo
  - Tipo do valor: REG_SZ
  ##### Valor de exemplo:
```
SOFTWARE\Policies\Microsoft\Edge\NewTabPageCompanyLogo = {
  "default_logo": {
    "hash": "cd0aa9856147b6c5b4ff2b7dfee5da20aa38253099ef1b4a64aced233c9afe29", 
    "url": "https://www.contoso.com/logo.png"
  }, 
  "light_logo": {
    "hash": "517d286edb416bb2625ccfcba9de78296e90da8e32330d4c9c8275c4c1c33737", 
    "url": "https://www.contoso.com/light_logo.png"
  }
}
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: NewTabPageCompanyLogo
  - Valor de exemplo:
``` xml
<key>NewTabPageCompanyLogo</key>
<dict>
  <key>default_logo</key>
  <dict>
    <key>hash</key>
    <string>cd0aa9856147b6c5b4ff2b7dfee5da20aa38253099ef1b4a64aced233c9afe29</string>
    <key>url</key>
    <string>https://www.contoso.com/logo.png</string>
  </dict>
  <key>light_logo</key>
  <dict>
    <key>hash</key>
    <string>517d286edb416bb2625ccfcba9de78296e90da8e32330d4c9c8275c4c1c33737</string>
    <key>url</key>
    <string>https://www.contoso.com/light_logo.png</string>
  </dict>
</dict>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### NewTabPageHideDefaultTopSites
  #### Ocultar os principais sites padrão da página nova guia
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Oculta os principais sites padrão da página nova guia no Microsoft Edge.

Se você definir essa política como verdadeira, os blocos de principais sites padrão serão ocultos.

Se você definir essa política como falsa ou não a configurar, os blocos de principais sites padrão permanecerão visíveis.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: NewTabPageHideDefaultTopSites
  - Nome da Política de Grupo: Ocultar os principais sites padrão da página nova guia
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/Startup, home page and new tab page
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: NewTabPageHideDefaultTopSites
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: NewTabPageHideDefaultTopSites
  - Valor de exemplo:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### NewTabPageLocation
  #### Configurar a URL da página nova guia
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Configura a URL padrão para a página nova guia.

Essa política determina a página que é aberta quando novas guias são criadas (inclusive quando novas janelas são abertas). Isso também afetará a página de inicialização se ela estiver definida para ser aberta para a página nova guia.

Essa política não determina qual página será aberta na inicialização. Isso é controlado pela política [RestoreOnStartup](#restoreonstartup). Ela também não afeta a página inicial, caso tenha sido definida para abrir a página da nova guia.

Se você não configurar essa política, a página de nova guia padrão será usada.

Se você configurar essa política *e* a política [NewTabPageSetFeedType](#newtabpagesetfeedtype), esta política terá precedência.

Se uma URL inválida for fornecida, novas guias serão abertas about://blank.

Essa política está disponível apenas nas instâncias do Windows que fazem parte de um domínio do Microsoft Active Directory, em instâncias do Windows 10 Pro ou Enterprise que estejam inscritas no gerenciamento de dispositivos ou em instâncias do macOS que são gerenciadas por meio do MDM ou passaram a fazer parte de um domínio por meio de MCX.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: Sim
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - String

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: NewTabPageLocation
  - Nome da Política de Grupo: Configurar a URL da página nova guia
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/Startup, home page and new tab page
  - Caminho da Política de Grupo (recomendado): Administrative Templates/Microsoft Edge - Default Settings (usuários podem substituir)/Startup, home page and new tab page
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nome do valor: NewTabPageLocation
  - Tipo do valor: REG_SZ
  ##### Valor de exemplo:
```
"https://www.fabrikam.com"
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: NewTabPageLocation
  - Valor de exemplo:
``` xml
<string>https://www.fabrikam.com</string>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### NewTabPageManagedQuickLinks
  #### Definir link rápido de Página Nova Guia
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 79 ou mais recente

  #### Descrição
  Por padrão, o Microsoft Edge exibe links rápidos na página nova guia, usando os atalhos adicionados pelo usuário e os principais sites baseados no histórico de navegação. Com essa política, você pode configurar até três blocos de link rápido na página nova guia, expressa como um objeto JSON:

[ { "url": "https://www.contoso.com", "title": "Contoso Portal", "pinned": true/false }, ... ]

O campo 'URL' é obrigatório. 'titled' e 'pinned' são opcionais. Se 'titled' não for fornecido, a URL será usada como o título padrão. Se 'pinned' não for fornecido, o valor padrão será falso.

O Microsoft Edge exibe essas imagens na ordem listada, da esquerda para a direita, com todos os blocos fixos exibidos antes dos blocos não fixados.

Se a política estiver definida como obrigatória, o campo 'pinned' será ignorado e todos os blocos serão fixados. Os blocos não podem ser excluídos pelo usuário e serão exibidos sempre na frente da lista links rápidos.

Se a política estiver definida como recomendado, os blocos fixados permanecerão na lista, mas o usuário poderá editá-los e excluí-los. Os blocos de link rápido que não estão afixados se comportam como principais sites padrão e ficam na lista, caso outros sites sejam visitados com mais frequência. Ao aplicar links não fixados por essa política a um perfil de navegador existente, os links podem não aparecer, dependendo de como eles são classificados em comparação com o histórico de navegação do usuário.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: Sim
  - Atualização dinâmica das políticas: não requer a reinicialização do navegador

  #### Tipo de dados:
  - Dictionary

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: NewTabPageManagedQuickLinks
  - Nome da Política de Grupo: Definir link rápido de Página Nova Guia
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/Startup, home page and new tab page
  - Caminho da Política de Grupo (recomendado): Administrative Templates/Microsoft Edge - Default Settings (usuários podem substituir)/Startup, home page and new tab page
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nome do valor: NewTabPageManagedQuickLinks
  - Tipo do valor: REG_SZ
  ##### Valor de exemplo:
```
SOFTWARE\Policies\Microsoft\Edge\NewTabPageManagedQuickLinks = [
  {
    "pinned": true, 
    "title": "Contoso Portal", 
    "url": "https://contoso.com"
  }, 
  {
    "title": "Fabrikam", 
    "url": "https://fabrikam.com"
  }
]
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: NewTabPageManagedQuickLinks
  - Valor de exemplo:
``` xml
<key>NewTabPageManagedQuickLinks</key>
<array>
  <dict>
    <key>pinned</key>
    <true/>
    <key>title</key>
    <string>Contoso Portal</string>
    <key>url</key>
    <string>https://contoso.com</string>
  </dict>
  <dict>
    <key>title</key>
    <string>Fabrikam</string>
    <key>url</key>
    <string>https://fabrikam.com</string>
  </dict>
</array>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### NewTabPagePrerenderEnabled
  #### Habilitar o pré-carregamento da nova página da guia para renderização mais rápida
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 85 ou mais recente

  #### Descrição
  Se você configurar essa política, o pré-carregamento da página da nova guia será habilitado e os usuários não poderão alterar essa configuração. Se você não configurar essa política, o pré-carregamento é habilitado e o usuário poderá alterar essa configuração.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: Sim
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: NewTabPagePrerenderEnabled
  - Nome da Política de Grupo: Habilitar o pré-carregamento da nova página da guia para renderização mais rápida
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/Startup, home page and new tab page
  - Caminho da Política de Grupo (recomendado): Administrative Templates/Microsoft Edge - Default Settings (usuários podem substituir)/Startup, home page and new tab page
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nome do valor: NewTabPagePrerenderEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: NewTabPagePrerenderEnabled
  - Valor de exemplo:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### NewTabPageSetFeedType
  #### Configurar a nova experiência de página da guia Microsoft Edge
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 79 ou mais recente

  #### Descrição
  Permite que você escolha a experiência do Microsoft Notícias ou o feed do Office 365 para a página nova guia.

Quando você define essa política como 'Notícias', os usuários podem ver a experiência no feed do Microsoft Notícias na página nova guia.

Quando você define essa política para o "Office", os usuários com um navegador do Azure Active Directory poderão ver a experiência de feed do Office 365 na página nova guia.

Se você desabilitar ou não configurar essa política:

- Os usuários com um logon do Azure Active Directory no navegador recebem a nova experiência de feed da página de guia do Office 365, bem como a nova experiência padrão de feed de página de guia.

- Os usuários que não tiverem uma entrada no navegador do Azure Active Directory poderão ver a nova experiência padrão da página da guia.

Se você configurar essa política *e* a política [NewTabPageLocation](#newtabpagelocation), [NewTabPageLocation](#newtabpagelocation) terá precedência.

Configuração padrão: Desabilitada ou não configurada.

Mapeamento das opções de política:

* Notícias (0) = experiência de feed Microsoft Notícias

* Office (1) = Experiência de feed do Office 365

Use as informações anteriores ao configurar essa política.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: Sim
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Inteiro

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: NewTabPageSetFeedType
  - Nome da Política de Grupo: Configurar a nova experiência de página da guia Microsoft Edge
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/Startup, home page and new tab page
  - Caminho da Política de Grupo (recomendado): Administrative Templates/Microsoft Edge - Default Settings (usuários podem substituir)/Startup, home page and new tab page
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nome do valor: NewTabPageSetFeedType
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000000
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: NewTabPageSetFeedType
  - Valor de exemplo:
``` xml
<integer>0</integer>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### RestoreOnStartup
  #### Ação a ser realizada na inicialização
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Especifique como o Microsoft Edge se comportará quando for iniciado.

Se você quiser que uma nova guia seja sempre aberta na inicialização, escolha 'RestoreOnStartupIsNewTabPage'.

Se você quiser reabrir URLs abertas da última vez que o Microsoft Edge foi encerrado, escolha 'RestoreOnStartupIsLastSession'. A sessão de navegação será restaurada como estava. Observe que essa opção desabilita algumas configurações que se baseiam em sessões ou que executam ações na saída (por exemplo, limpar dados de navegação em cookies de saída ou somente de sessão).

Se você quiser abrir um conjunto específico de URLs, escolha 'RestoreOnStartupIsURLs'.

Desabilitar essa configuração é equivalente a deixá-la não configurada. Os usuários podem alterá-la no Microsoft Edge.

Essa política está disponível apenas nas instâncias do Windows que fazem parte de um domínio do Microsoft Active Directory, em instâncias do Windows 10 Pro ou Enterprise que estejam inscritas no gerenciamento de dispositivos ou em instâncias do macOS que são gerenciadas por meio do MDM ou passaram a fazer parte de um domínio por meio de MCX.

Mapeamento das opções de política:

* RestoreOnStartupIsNewTabPage (5) = Abrir uma nova guia

* RestoreOnStartupIsLastSession (1) = Restaurar a última sessão

* RestoreOnStartupIsURLs (4) = Abrir uma lista de URLs

Use as informações anteriores ao configurar essa política.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: Sim
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Inteiro

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: RestoreOnStartup
  - Nome da Política de Grupo: Ação a ser realizada na inicialização
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/Startup, home page and new tab page
  - Caminho da Política de Grupo (recomendado): Administrative Templates/Microsoft Edge - Default Settings (usuários podem substituir)/Startup, home page and new tab page
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nome do valor: RestoreOnStartup
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000004
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: RestoreOnStartup
  - Valor de exemplo:
``` xml
<integer>4</integer>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### RestoreOnStartupURLs
  #### Sites a abrir quando o navegador for iniciado
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Especificar uma lista de sites para abrir automaticamente quando o navegador for iniciado. Se você não configurar essa política, nenhum site será aberto na inicialização.

Essa política só funcionará se você também definir a política [RestoreOnStartup](#restoreonstartup) para "abrir uma lista de URLs" (4).

Essa política está disponível apenas nas instâncias do Windows que fazem parte de um domínio do Microsoft Active Directory, em instâncias do Windows 10 Pro ou Enterprise que estejam inscritas no gerenciamento de dispositivos ou em instâncias do macOS que são gerenciadas por meio do MDM ou passaram a fazer parte de um domínio por meio de MCX.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: Sim
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: RestoreOnStartupURLs
  - Nome da Política de Grupo: Sites a abrir quando o navegador for iniciado
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/Startup, home page and new tab page
  - Caminho da Política de Grupo (recomendado): Administrative Templates/Microsoft Edge - Default Settings (usuários podem substituir)/Startup, home page and new tab page
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge\RestoreOnStartupURLs
  - Caminho (recomendado): SOFTWARE\Policies\Microsoft\Edge\Recommended\RestoreOnStartupURLs
  - Nome do valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de exemplo:
```
SOFTWARE\Policies\Microsoft\Edge\RestoreOnStartupURLs\1 = "https://contoso.com"
SOFTWARE\Policies\Microsoft\Edge\RestoreOnStartupURLs\2 = "https://www.fabrikam.com"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: RestoreOnStartupURLs
  - Valor de exemplo:
``` xml
<array>
  <string>https://contoso.com</string>
  <string>https://www.fabrikam.com</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### ShowHomeButton
  #### Botão Mostrar página inicial na barra de ferramentas
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Mostra o botão Página Inicial na barra de ferramentas do Microsoft Edge.

Habilite essa política para sempre mostrar o botão Página Inicial. Desabilite-o para nunca mostrar o botão.

Se você não configurar a política, os usuários poderão optar por mostrar o botão Página Inicial.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: Sim
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: ShowHomeButton
  - Nome da Política de Grupo: Botão Mostrar página inicial na barra de ferramentas
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/Startup, home page and new tab page
  - Caminho da Política de Grupo (recomendado): Administrative Templates/Microsoft Edge - Default Settings (usuários podem substituir)/Startup, home page and new tab page
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nome do valor: ShowHomeButton
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ShowHomeButton
  - Valor de exemplo:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ## Políticas adicionais

  [Voltar ao início](#microsoft-edge---policies)

  ### AddressBarMicrosoftSearchInBingProviderEnabled
  #### Habilitar a Pesquisa da Microsoft em sugestões do Bing na barra de endereços
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 81 ou mais recente

  #### Descrição
  Permite a exibição da pesquisa relevante da Microsoft em sugestões do Bing na lista de sugestões da barra de endereços quando o usuário digita uma cadeia de pesquisa na barra de endereços. Se você habilitar ou não configurar essa política, os usuários poderão ver os resultados internos da plataforma Pesquisa da Microsoft no Bing, na lista de sugestões de barra de endereços do Microsoft Edge. Para ver a pesquisa da Microsoft nos resultados do Bing, o usuário deve estar conectado ao Microsoft Edge com a conta do Azure AD para essa organização.
Se você desabilitar essa política, os usuários não poderão ver resultados internos na lista de sugestões de barra de endereços do Microsoft Edge.
Se você tiver habilitado o conjunto de políticas que força um provedor de pesquisa padrão ([DefaultSearchProviderEnabled](#defaultsearchproviderenabled), [DefaultSearchProviderName](#defaultsearchprovidername) e [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl)) e o provedor de pesquisa especificado não for Bing, essa política não será aplicável e não haverá uma pesquisa da Microsoft em sugestões de Bing na lista de sugestões da barra de endereços.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: AddressBarMicrosoftSearchInBingProviderEnabled
  - Nome da Política de Grupo: Habilitar a Pesquisa da Microsoft em sugestões do Bing na barra de endereços
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: AddressBarMicrosoftSearchInBingProviderEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: AddressBarMicrosoftSearchInBingProviderEnabled
  - Valor de exemplo:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### AdsSettingForIntrusiveAdsSites
  #### Configuração Ads para sites com publicidade invasiva
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 78 ou mais recente

  #### Descrição
  Controla se os anúncios são bloqueados em sites com anúncios invasivos.

Mapeamento das opções de política:

* AllowAds (1) = Permitir anúncios em todos os sites

* BlockAds (2) = Bloquear anúncios em sites com propagandas invasivas. (Valor padrão)

Use as informações anteriores ao configurar essa política.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Inteiro

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: AdsSettingForIntrusiveAdsSites
  - Nome da Política de Grupo: Configuração Ads para sites com publicidade invasiva
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: AdsSettingForIntrusiveAdsSites
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: AdsSettingForIntrusiveAdsSites
  - Valor de exemplo:
``` xml
<integer>1</integer>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### AllowDeletingBrowserHistory
  #### Habilitar a exclusão do navegador e baixar o histórico
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Permite excluir o histórico do navegador e baixar o histórico e impede que os usuários alterem essa configuração.

Observe que, mesmo se essa política estiver desabilitada, não é garantido que o histórico de navegação e de download seja mantido: os usuários podem editar ou excluir os arquivos de banco de dados do histórico diretamente, e o próprio navegador poderá remover (com base no período de expiração) ou arquivar qualquer item do histórico ou todos os itens a qualquer momento.

Se você habilitar essa política ou não a configurar, os usuários poderão excluir o histórico de navegação e downloads.

Se você desabilitar essa política, os usuários não poderão excluir o histórico de navegação e downloads.

Se você habilitar essa política, não habilite a política [ClearBrowsingDataOnExit](#clearbrowsingdataonexit), porque ambas lidam com a exclusão de dados. Se você habilitar ambos, a política [ClearBrowsingDataOnExit](#clearbrowsingdataonexit) terá precedência e excluirá todos os dados quando o Microsoft Edge fechar, independentemente de como essa política está configurada.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: AllowDeletingBrowserHistory
  - Nome da Política de Grupo: Habilitar a exclusão do navegador e baixar histórico
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: AllowDeletingBrowserHistory
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: AllowDeletingBrowserHistory
  - Valor de exemplo:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### AllowFileSelectionDialogs
  #### Permitir diálogos de seleção de arquivo
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Permitir o acesso a arquivos locais, permitindo que o Microsoft Edge exiba os diálogos de seleção de arquivo.

Se você habilitar ou não configurar essa política, os usuários poderão abrir as caixas de diálogo de seleção de arquivo como normal.

Se você desabilitar essa política, sempre que o usuário executar uma ação que acione uma caixa de diálogo de seleção de arquivo (como importar favoritos, carregar arquivos ou salvar links), uma mensagem será exibida, e o usuário deverá clicar em Cancelar na caixa de diálogo de seleção de arquivo.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: AllowFileSelectionDialogs
  - Nome da Política de Grupo: Permitir diálogos de seleção de arquivo
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: AllowFileSelectionDialogs
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: AllowFileSelectionDialogs
  - Valor de exemplo:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### AllowPopupsDuringPageUnload
  #### Permite que uma página mostre pop-ups durante seu descarregamento
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 78 ou mais recente

  #### Descrição
  Essa política permite que um administrador especifique que uma página pode mostrar pop-ups durante seu descarregamento.

Quando a política estiver definida como habilitada, as páginas poderão mostrar pop-ups enquanto estiverem sendo descarregadas.

Quando a política estiver definida como desabilitada ou desativada, as páginas não terão permissão para mostrar os pop-ups enquanto estão sendo descarregadas. Esse é o mesmo da seguinte especificação: (https://html.spec.whatwg.org/#apis-for-creating-and-navigating-browsing-contexts-by-name).

Essa política será removida no futuro.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: não requer a reinicialização do navegador

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: AllowPopupsDuringPageUnload
  - Nome da Política de Grupo: Permite que uma página mostre pop-ups durante seu descarregamento
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: AllowPopupsDuringPageUnload
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000000
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: AllowPopupsDuringPageUnload
  - Valor de exemplo:
``` xml
<false/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### AllowSurfGame
  #### Permitir a navegação
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 83 ou mais recente

  #### Descrição
  Se você desabilitar essa política, os usuários não poderão reproduzir o jogo de navegação quando o dispositivo estiver offline ou se o usuário navegar até edge://surf.

Se você habilitar ou não configurar essa política, os usuários poderão executar o jogo de navegação.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: não requer a reinicialização do navegador

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: AllowSurfGame
  - Nome da Política de Grupo: Permitir jogos de navegação
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: AllowSurfGame
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000000
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: AllowSurfGame
  - Valor de exemplo:
``` xml
<false/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### AllowSyncXHRInPageDismissal
  #### Permitir que as páginas enviem solicitações XHR síncronas durante o descarte da página (preterida)
  >SUBSTITUÍDO: Essa política está preterida. Ela tem suporte no momento, mas se tornará obsoleta em uma versão futura.
  
  #### Versões com suporte:
  - No Windows e no macOS desde 79 ou mais recente

  #### Descrição
  Essa política foi preterida porque destina-se a ser um mecanismo de curto prazo para dar mais tempo para que as empresas atualizem o conteúdo da Web se e quando ela for incompatível com a alteração para não permitir solicitações XHR síncronas durante a descarte da página. Ela não funcionará no Microsoft Edge versão 88.

Essa política permite especificar que uma página pode enviar solicitações XHR síncronas durante o descarte da página.

Se você habilitar essa política, as páginas poderão enviar solicitações XHR síncronas durante o descarte da página.

Se você desabilitar essa política ou não configurar essa política, não será possível enviar solicitações de XHR síncronos durante o descarte da página.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: não requer a reinicialização do navegador

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: AllowSyncXHRInPageDismissal
  - Nome da GP: Autorizar páginas a enviar solicitações de XHR síncronas durante a descarte da página (substituído)
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: AllowSyncXHRInPageDismissal
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000000
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: AllowSyncXHRInPageDismissal
  - Valor de exemplo:
``` xml
<false/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### AllowTokenBindingForUrls
  #### Configurar a lista de sites com os quais o Microsoft Edge tentará estabelecer uma Associação de Token.
  
  
  #### Versões com suporte:
  - No Windows desde 83 ou posterior

  #### Descrição
  Configure a lista de padrões de URL para sites para os quais o navegador tentará executar o protocolo de vinculação de token.
Para os domínios nesta lista, o navegador enviará a Associação de Token ClientHello no handshake TLS (consulte https://tools.ietf.org/html/rfc8472).
Se o servidor responder com uma resposta ServerHello válida, o navegador criará e enviará mensagens de Associação de Token nas solicitações de HTTPS subsequentes. Confira https://tools.ietf.org/html/rfc8471 para saber mais.

Se esta lista estiver vazia, a Associação de Token será desabilitada.

Essa política só estará disponível em dispositivos Windows 10 com o recurso Modo de Segurança Virtual.

A partir do Microsoft Edge 86, essa política deixou de ser compatível com a atualização dinâmica.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: não requer a reinicialização do navegador

  #### Tipo de dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: AllowTokenBindingForUrls
  - Nome da Política de Grupo: Configurar a lista de sites com os quais o Microsoft Edge tentará estabelecer uma Associação de Token.
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge\AllowTokenBindingForUrls
  - Caminho (recomendado): N/A
  - Nome do valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de exemplo:
```
SOFTWARE\Policies\Microsoft\Edge\AllowTokenBindingForUrls\1 = "mydomain.com"
SOFTWARE\Policies\Microsoft\Edge\AllowTokenBindingForUrls\2 = "[*.]mydomain2.com"
SOFTWARE\Policies\Microsoft\Edge\AllowTokenBindingForUrls\3 = "[*.].mydomain2.com"

```


  

  [Voltar ao início](#microsoft-edge---policies)

  ### AllowTrackingForUrls
  #### Configurar exceções de prevenção de rastreamento para sites específicos
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 78 ou mais recente

  #### Descrição
  Configure a lista de padrões de URL excluídos da prevenção contra rastreamento.

Se você configurar essa política, a lista de padrões de URL configurada será excluída da prevenção de rastreamento.

Se você não configurar essa política, o valor padrão global da política "Bloquear o acompanhamento de atividades de navegação na Web" (se definido) ou a configuração pessoal do usuário será usado para todos os sites.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: AllowTrackingForUrls
  - Nome da Política de Grupo: Configurar exceções de prevenção de rastreamento para sites específicos
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge\AllowTrackingForUrls
  - Caminho (recomendado): N/A
  - Nome do valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de exemplo:
```
SOFTWARE\Policies\Microsoft\Edge\AllowTrackingForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\AllowTrackingForUrls\2 = "[*.]contoso.edu"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: AllowTrackingForUrls
  - Valor de exemplo:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### AlternateErrorPagesEnabled
  #### Sugerir páginas similares quando uma página da Web não consegue ser encontrada
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 80 ou mais recente

  #### Descrição
  Permita que o Microsoft Edge emita uma conexão com um serviço Web para gerar URLs e sugestões de pesquisa para problemas de conectividade, como erros de DNS.

Se você habilitar essa política, um serviço web será usado para gerar sugestões de URL e pesquisa para erros de rede.

Se você desabilitar essa política, nenhuma chamada para o serviço web será feita e uma página de erro padrão será exibida.

Se você não configurar essa política, o Microsoft Edge respeitará a preferência do usuário definida em serviços em edge://settings/privacy.
Especificamente, há um botão de alternância **Sugerir páginas similares quando uma página da Web não consegue ser encontrada**, que o usuário pode ativar ou desativar. Observe que, se você tiver habilitado essa política (AlternateErrorPagesEnabled), a configuração Sugerir páginas similares quando uma página da Web não for encontrada estará ativada, mas o usuário não poderá alterar a configuração usando o botão de alternância. Se você desabilitar essa política, a configuração Sugerir páginas similares quando não for possível localizar uma página da Web será desativada, e o usuário não poderá alterar a configuração usando o botão de alternância.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: Sim
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: AlternateErrorPagesEnabled
  - Nome da Política de Grupo: Sugerir páginas similares quando uma página da Web não consegue ser encontrada
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): Administrative Templates/Microsoft Edge - Default Settings (usuários podem substituir)/
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nome do valor: AlternateErrorPagesEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: AlternateErrorPagesEnabled
  - Valor de exemplo:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### AlwaysOpenPdfExternally
  #### Sempre abrir arquivos PDF externamente
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Desabilita o Visualizador de PDF interno no Microsoft Edge.

Se você habilitar essa política, o Microsoft Edge tratará arquivos PDF como downloads e permitirá que os usuários os abram usando o aplicativo padrão.

Se você não configurar essa política ou desabilitá-la, o Microsoft Edge abrirá arquivos PDF (a menos que o usuário a desative).

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: AlwaysOpenPdfExternally
  - Nome da Política de Grupo: Sempre abrir arquivos PDF externamente
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: AlwaysOpenPdfExternally
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: AlwaysOpenPdfExternally
  - Valor de exemplo:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### AmbientAuthenticationInPrivateModesEnabled
  #### Habilitar a autenticação ambiente para perfis InPrivate e Convidado
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 81 ou mais recente

  #### Descrição
  Configure essa política para permitir ou não permitir a autenticação do ambiente para perfis InPrivate e Guest no Microsoft Edge.

A autenticação de ambiente é uma autenticação http com as credenciais padrão quando as credenciais explícitas não são fornecidas por meio de esquemas Challenge/Response NTLM/Kerberos/Negotiate.

Se você definir a política para 'RegularOnly', ela permitirá a autenticação ambiental apenas para sessões Normais. As sessões InPrivate e Guest não terão permissão para a autenticação em ambiente.

Se você definir a política como 'InPrivateAndRegular', ela permitirá a autenticação do ambiente InPrivate e Sessões Normais. As sessões de convidado não terão permissão para a autenticação em ambiente.

Se você definir a política como 'GuestAndRegular', ela permitirá a autenticação ambiental para as sessões Convidado e Regular. As sessões InPrivate não serão permitidas para a autenticação ambiental

Se você definir a política para 'All', ela permitirá a autenticação ambiental em todas as sessões.

Observe que a autenticação do ambiente sempre é permitida em perfis regulares.

No Microsoft Edge versão 81 e posterior, se a política não estiver definida, a autenticação do ambiente será habilitada somente em sessões normais.

Mapeamento das opções de política:

* RegularOnly (0) = Habilitar a autenticação ambiental somente em sessões normais

* InPrivateAndRegular (1) = Habilitar autenticação ambiental em sessões InPrivate e normais

* GuestAndRegular (2) = Habilitar a autenticação ambiental nas sessões convidado e normais

* 3 = habilitar a autenticação ambiental nas sessões comuns, InPrivate e convidado

Use as informações anteriores ao configurar essa política.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Inteiro

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: AmbientAuthenticationInPrivateModesEnabled
  - Nome da Política de Grupo: Habilitar a autenticação ambiente para perfis InPrivate e Convidado
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: AmbientAuthenticationInPrivateModesEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000000
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: AmbientAuthenticationInPrivateModesEnabled
  - Valor de exemplo:
``` xml
<integer>0</integer>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### AppCacheForceEnabled
  #### Permite reabilitar o recurso AppCache, mesmo que ele esteja desativado por padrão
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 84 ou mais recente

  #### Descrição
  Se você definir essa política como verdadeira, o AppCache estará habilitado, mesmo quando o AppCache no Microsoft Edge não estiver disponível por padrão.

Se você definir essa política como falsa ou não a definir, o AppCache seguirá os padrões do Microsoft Edge.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: não requer a reinicialização do navegador

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: AppCacheForceEnabled
  - Nome da Política de Grupo: Permite reabilitar o recurso AppCache, mesmo que ele esteja desativado por padrão
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: AppCacheForceEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000000
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: AppCacheForceEnabled
  - Valor de exemplo:
``` xml
<false/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### ApplicationLocaleValue
  #### Definir a localidade do aplicativo
  
  
  #### Versões com suporte:
  - No Windows desde 77 ou posterior

  #### Descrição
  Configura a localidade do aplicativo no Microsoft Edge e impede que os usuários alterem a localidade.

Se você habilitar essa política, o Microsoft Edge usará o local especificado. Se a localidade configurada não tiver suporte, será usado "en-US".

Se você desabilitar ou não definir essa configuração, o Microsoft Edge usará a localidade preferencial especificada pelo usuário (se configurada) ou a localidade de fallback "en-US".

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: Sim
  - Atualização dinâmica das políticas: não requer a reinicialização do navegador

  #### Tipo de dados:
  - String

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: ApplicationLocaleValue
  - Nome da Política de Grupo: Definir a localidade do aplicativo
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): Administrative Templates/Microsoft Edge - Default Settings (usuários podem substituir)/
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nome do valor: ApplicationLocaleValue
  - Tipo do valor: REG_SZ
  ##### Valor de exemplo:
```
"en"
```


  

  [Voltar ao início](#microsoft-edge---policies)

  ### AudioCaptureAllowed
  #### Permitir ou bloquear captura de áudio
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Permite que você defina se um usuário será instruído a conceder acesso a um site para o dispositivo de captura de áudio. Esta política se aplica a todas as URLs, exceto aquelas configuradas na lista [AudioCaptureAllowedUrls](#audiocaptureallowedurls).

Se você habilitar essa política ou não a configurar ( configuração padrão), o usuário será instruído a fornecer acesso de captura de áudio, exceto nas URLs na lista [AudioCaptureAllowedUrls](#audiocaptureallowedurls). Essas URLs listadas recebem acesso sem solicitação.

Se você desabilitar essa política, o usuário não será questionado e a captura de áudio só poderá ser acessada para as URLs configuradas em [AudioCaptureAllowedUrls](#audiocaptureallowedurls).

Essa política afeta todos os tipos de entradas de áudio, não apenas o microfone interno.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: AudioCaptureAllowed
  - Nome da Política de Grupo: Permitir ou bloquear captura de áudio
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: AudioCaptureAllowed
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000000
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: AudioCaptureAllowed
  - Valor de exemplo:
``` xml
<false/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### AudioCaptureAllowedUrls
  #### Sites que podem acessar dispositivos de captura de áudio sem solicitar permissão
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Especificar sites, com base em padrões de URL, que podem usar dispositivos de captura de áudio sem pedir permissão ao usuário. Os padrões nesta lista são comparados com a origem de segurança da URL da solicitação. Se elas corresponderem, o site recebe acesso automaticamente aos dispositivos de captura de áudio.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: AudioCaptureAllowedUrls
  - Nome da Política de Grupo: Sites que podem acessar dispositivos de captura de áudio sem solicitar permissão
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge\AudioCaptureAllowedUrls
  - Caminho (recomendado): N/A
  - Nome do valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de exemplo:
```
SOFTWARE\Policies\Microsoft\Edge\AudioCaptureAllowedUrls\1 = "https://www.contoso.com/"
SOFTWARE\Policies\Microsoft\Edge\AudioCaptureAllowedUrls\2 = "https://[*.]contoso.edu/"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: AudioCaptureAllowedUrls
  - Valor de exemplo:
``` xml
<array>
  <string>https://www.contoso.com/</string>
  <string>https://[*.]contoso.edu/</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### AudioSandboxEnabled
  #### Permitir a execução da área restrita de áudio
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 81 ou mais recente

  #### Descrição
  Esta política controla a área restrita do processo de áudio.

Se você habilitar essa política, o processo de áudio será executado na área restrita.

Se você desabilitar essa política, o processo de áudio será executado em modo não seguro e o módulo de processamento de áudio do WebRTC será executado no processo de renderização.
Isso deixa os usuários sujeitos a riscos de segurança relacionados à execução do subsistema de áudio unsandboxed.

Se você não configurar esta política, a configuração padrão da caixa de proteção de áudio será usada, o que pode diferir com base na plataforma.

Essa política destina-se a proporcionar flexibilidade às empresas para desabilitar a área restrita de áudio se elas usarem configurações de software de segurança que interfiram na área restrita.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: não requer a reinicialização do navegador

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: AudioSandboxEnabled
  - Nome da Política de Grupo: Permitir a execução da área restrita de áudio
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: AudioSandboxEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: AudioSandboxEnabled
  - Valor de exemplo:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### AutoImportAtFirstRun
  #### Importar automaticamente os dados e as configurações de outro navegador na primeira execução
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Se você habilitar essa política, todos os tipos de texto e configurações compatíveis do navegador especificado serão importados silenciosamente e automaticamente na primeira execução. Durante a primeira experiência de execução, a seção de importação também será ignorada.

Os dados do navegador Versão Prévia do Microsoft Edge serão sempre migrados silenciosamente na primeira vez, independentemente do valor desta política.

Se essa política estiver definida como 'FromDefaultBrowser', os tipos de dados correspondentes ao navegador padrão no dispositivo gerenciado serão importados.

Se o navegador especificado como o valor desta política não estiver presente no dispositivo gerenciado, o Microsoft Edge simplesmente pulará a importação sem nenhuma notificação para o usuário.

Se você definir essa política como 'DisabledAutoImport', a seção de importação da experiência de primeira execução será ignorada inteiramente, e o Microsoft Edge não importará os dados e as configurações do navegador automaticamente.

Se essa política estiver definida como 'FromInternetExplorer', os seguintes tipos de dados serão importados do Internet Explorer:
1. Favoritos ou indicadores
2. Senhas salvas
3. Mecanismos de pesquisa
4. Histórico de navegação
5. Home page

Se essa política estiver definida como 'FromGoogleChrome', os seguintes tipos de texto serão importados do Google Chrome:
1. Favoritos
2. Senhas salvas
3. Endereços e muito mais
4. Informações de pagamento
5. Histórico de navegação
6. Configurações
7. Guias fixado e fixo
8. Extensões
9. Cookies

Observação: para obter mais detalhes sobre o que é importado do Google Chrome, confira [https://go.microsoft.com/fwlink/?linkid=2120835](https://go.microsoft.com/fwlink/?linkid=2120835)

Se essa política estiver definida como 'FromSafari', os dados do usuário não serão mais importados para o Microsoft Edge. Isso ocorre devido à maneira como o acesso ao disco completo funciona no Mac.
No macOS Mojave ou superior, não é mais possível ter uma importação automatizada e autônoma de dados do Safari para o Microsoft Edge.

A partir do Microsoft Edge versão 83, se essa política estiver definida para o valor de 'FromMozillaFirefox', os seguintes tipos de texto serão importados do Mozilla Firefox:
1. Favoritos ou indicadores
2. Senhas salvas
3. Endereços e muito mais
4. Histórico de navegação

Se você deseja impedir que tipos de dados específicos sejam importados nos dispositivos gerenciados, você pode usar esta política com outras políticas, como [ImportAutofillFormData](#importautofillformdata), [ImportBrowserSettings](#importbrowsersettings), [ImportFavorites](#importfavorites)e etc.

Mapeamento das opções de política:

* FromDefaultBrowser (0) = Importa automaticamente todos os tipos de texto e configurações compatíveis do navegador padrão

* FromInternetExplorer (1) = Importa automaticamente todos os tipos de texto e configurações compatíveis do Internet Explorer

* FromGoogleChrome (2) = Importa automaticamente todos os tipos de texto e configurações compatíveis do Google Chrome

* FromSafari (3) = Importa automaticamente todos os tipos de texto e configurações compatíveis do Safari

* DisabledAutoImport (4) = Desabilita a importação automática, e a seção de importação da experiência da primeira execução é ignorada

* FromMozillaFirefox (5) = Importa automaticamente todos os tipos de texto e configurações compatíveis do Mozilla Firefox

Use as informações anteriores ao configurar essa política.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: não requer a reinicialização do navegador

  #### Tipo de dados:
  - Inteiro

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: AutoImportAtFirstRun
  - Nome da Política de Grupo: Importar automaticamente os dados e as configurações de outro navegador na primeira execução
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: AutoImportAtFirstRun
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000002
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: AutoImportAtFirstRun
  - Valor de exemplo:
``` xml
<integer>2</integer>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### AutoLaunchProtocolsFromOrigins
  #### Definir uma lista de protocolos que podem iniciar um aplicativo externo de origens listadas sem perguntar ao usuário
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 85 ou mais recente

  #### Descrição
  Permite que você defina uma lista de protocolos e, para cada protocolo, uma lista associada de padrões de origem permitidos, que podem iniciar um aplicativo externo sem solicitar o usuário. O separador à direita não deve ser incluído ao listar o protocolo. Por exemplo, liste "Skype" em vez de "Skype:" ou "skype://".

Se você configurar essa política, um protocolo só poderá iniciar um aplicativo externo sem perguntar se:

- o protocolo está listado

- a origem do site que tentou iniciar o protocolo corresponde a um dos padrões de origem na lista de allowed_origins do protocolo.

Se a condição for falsa, o prompt de inicialização do protocolo externo não será omitido pela política.

Se você não configurar essa política, nenhum protocolo poderá ser iniciado sem um aviso. Os usuários podem optar por recusar solicitações por protocolo/por site, a menos que a política [ExternalProtocolDialogShowAlwaysOpenCheckbox](#externalprotocoldialogshowalwaysopencheckbox) esteja definida como desabilitada. Essa política não afeta as isenções por solicitação por protocolo/por site definidas pelos usuários.

Os padrões de correspondência de origem usam um formato semelhante para os da [URLBlocklist](#urlblocklist) política, que estão documentadas em [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

No entanto, padrões de correspondência de origem para esta política não podem conter elementos "/path" ou "@query". Todos os padrões que contenham um elemento "/path" ou "@query" serão ignorados.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Dictionary

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: AutoLaunchProtocolsFromOrigins
  - Nome da Política de Grupo: Definir uma lista de protocolos que podem iniciar um aplicativo externo de origens listadas sem perguntar ao usuário
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: AutoLaunchProtocolsFromOrigins
  - Tipo do valor: REG_SZ
  ##### Valor de exemplo:
```
SOFTWARE\Policies\Microsoft\Edge\AutoLaunchProtocolsFromOrigins = [
  {
    "allowed_origins": [
      "example.com", 
      "http://www.example.com:8080"
    ], 
    "protocol": "spotify"
  }, 
  {
    "allowed_origins": [
      "https://example.com", 
      "https://.mail.example.com"
    ], 
    "protocol": "teams"
  }, 
  {
    "allowed_origins": [
      "*"
    ], 
    "protocol": "outlook"
  }
]
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: AutoLaunchProtocolsFromOrigins
  - Valor de exemplo:
``` xml
<key>AutoLaunchProtocolsFromOrigins</key>
<array>
  <dict>
    <key>allowed_origins</key>
    <array>
      <string>example.com</string>
      <string>http://www.example.com:8080</string>
    </array>
    <key>protocol</key>
    <string>spotify</string>
  </dict>
  <dict>
    <key>allowed_origins</key>
    <array>
      <string>https://example.com</string>
      <string>https://.mail.example.com</string>
    </array>
    <key>protocol</key>
    <string>teams</string>
  </dict>
  <dict>
    <key>allowed_origins</key>
    <array>
      <string>*</string>
    </array>
    <key>protocol</key>
    <string>outlook</string>
  </dict>
</array>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### AutoOpenAllowedForURLs
  #### URLs nas quais AutoOpenFileTypes pode aplicar
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 85 ou mais recente

  #### Descrição
  Uma lista de URLs às quais [AutoOpenFileTypes](#autoopenfiletypes) será aplicada. Essa política não afeta os valores abertos automaticamente pelos usuários por meio da prateleira de download... > Entrada de menu "sempre abrir arquivos deste tipo".

Se você definir URLs nesta política, os arquivos só serão abertos automaticamente por política se a URL fizer parte desse conjunto e o tipo de arquivo estiver listado em [AutoOpenFileTypes](#autoopenfiletypes). Se a condição for falsa, o download não será aberto automaticamente pela política.

Se você não definir essa política, todos os downloads do tipo de arquivo no local [AutoOpenFileTypes](#autoopenfiletypes) serão abertos automaticamente.

Um padrão de URL deve ser formatado de acordo com [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: AutoOpenAllowedForURLs
  - Nome da Política de Grupo: URLs nas quais AutoOpenFileTypes pode aplicar
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs
  - Caminho (recomendado): N/A
  - Nome do valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de exemplo:
```
SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs\1 = "example.com"
SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs\2 = "https://ssl.server.com"
SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs\3 = "hosting.com/good_path"
SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs\4 = "https://server:8080/path"
SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs\5 = ".exact.hostname.com"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: AutoOpenAllowedForURLs
  - Valor de exemplo:
``` xml
<array>
  <string>example.com</string>
  <string>https://ssl.server.com</string>
  <string>hosting.com/good_path</string>
  <string>https://server:8080/path</string>
  <string>.exact.hostname.com</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### AutoOpenFileTypes
  #### Lista de tipos de arquivo que devem ser abertos automaticamente no download
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 85 ou mais recente

  #### Descrição
  Essa política define uma lista de tipos de arquivo que devem ser abertos automaticamente no download. Observação: o separador à esquerda não deve ser incluído ao listar o tipo de arquivo, então liste "txt", em vez de ".txt".

Por padrão, esses tipos de arquivo serão abertos automaticamente em todas as URLs. Você pode usar a política [AutoOpenAllowedForURLs](#autoopenallowedforurls) para restringir as URLs para as quais esses tipos de arquivos serão abertos automaticamente.

Os arquivos com tipos que devem ser abertos automaticamente ainda estarão sujeitos a verificações ativadas do Microsoft Defender SmartScreen e não serão abertos se eles falharem.

Os tipos de arquivo que um usuário já especificou para serem abertos automaticamente, continuarão a fazê-lo quando forem baixados. O usuário continuará a ser capaz de especificar outros tipos de arquivos para serem abertos automaticamente.

Se você não definir essa política, somente os tipos de arquivo que um usuário já especificou para serem abertos automaticamente o farão quando forem baixados.

Essa política está disponível apenas nas instâncias do Windows que fazem parte de um domínio do Microsoft Active Directory, em instâncias do Windows 10 Pro ou Enterprise que estejam inscritas no gerenciamento de dispositivos ou em instâncias do macOS que são gerenciadas por meio do MDM ou passaram a fazer parte de um domínio por meio de MCX.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: AutoOpenFileTypes
  - Nome da Política de Grupo: Lista de tipos de arquivo que devem ser abertos automaticamente no download
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge\AutoOpenFileTypes
  - Caminho (recomendado): N/A
  - Nome do valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de exemplo:
```
SOFTWARE\Policies\Microsoft\Edge\AutoOpenFileTypes\1 = "exe"
SOFTWARE\Policies\Microsoft\Edge\AutoOpenFileTypes\2 = "txt"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: AutoOpenFileTypes
  - Valor de exemplo:
``` xml
<array>
  <string>exe</string>
  <string>txt</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### AutofillAddressEnabled
  #### Habilitar o preenchimento automático para endereços
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Habilita o recurso de Autopreenchimento e permite que os usuários realizem automaticamente as informações de endereço em formulários da Web usando informações armazenadas anteriormente.

Se você desabilitar essa política, o preenchimento automático nunca sugerirá ou preencherá as informações de endereço, nem salvará as informações de endereço adicionais que o usuário pode enviar durante a navegação na web.

Se você habilitar essa política ou não a configurar, os usuários poderão controlar o preenchimento automático de endereços na interface do usuário.

Observe que, se você desabilitar essa política, também interromperá todas as atividades de todos os formulários da web, exceto os formulários de pagamento e de senha. Nenhuma outra entrada será salva, e o Microsoft Edge não sugerirá ou preencherá automaticamente nenhuma entrada anterior.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: Sim
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: AutofillAddressEnabled
  - Nome da Política de Grupo: Habilitar o preenchimento automático para endereços
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): Administrative Templates/Microsoft Edge - Default Settings (usuários podem substituir)/
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nome do valor: AutofillAddressEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000000
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: AutofillAddressEnabled
  - Valor de exemplo:
``` xml
<false/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### AutofillCreditCardEnabled
  #### Habilitar o preenchimento automático para cartões de crédito
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Habilita o recurso AutoPreenchimento do Microsoft Edge e permite que os usuários preencham automaticamente informações de cartão de crédito em formulários da web usando as informações armazenadas anteriormente.

Se você desabilitar essa política, o preenchimento automático nunca sugerirá ou preencherá as informações de cartão de crédito, nem salvará outras informações de cartão de crédito que os usuários podem enviar durante a navegação na web.

Se você habilitar essa política ou não a configurar, os usuários poderão controlar o preenchimento automático para cartões de crédito.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: Sim
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: AutofillCreditCardEnabled
  - Nome da Política de Grupo: Habilitar o preenchimento automático para cartões de crédito
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): Administrative Templates/Microsoft Edge - Default Settings (usuários podem substituir)/
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nome do valor: AutofillCreditCardEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000000
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: AutofillCreditCardEnabled
  - Valor de exemplo:
``` xml
<false/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### AutoplayAllowed
  #### Permitir a reprodução automática de mídia para sites
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 78 ou mais recente

  #### Descrição
  Essa política define a política de reprodução automática de mídia para sites.

A configuração padrão, "Não configurada", respeita as configurações de reprodução automática atuais e permite que os usuários configurem suas configurações de reprodução automática.

A configuração "Habilitada" define a reprodução automática de mídia como "Permitir".  Todos os sites podem ser reproduzidos em mídia. Os usuários não podem substituir esta política.

A configuração de "Desabilitado" define a reprodução automática de mídia como "Bloquear".  Nenhum site tem permissão para executar a reprodução automática. Os usuários não podem substituir esta política.

Será necessário fechar uma guia e abri-la novamente para que essa política tenha efeito.


  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: AutoplayAllowed
  - Nome da Política de Grupo: Permitir a reprodução automática de mídia para sites
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: AutoplayAllowed
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: AutoplayAllowed
  - Valor de exemplo:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### BackgroundModeEnabled
  #### Continuar executando aplicativos de segundo plano após o Microsoft Edge ser fechado
  
  
  #### Versões com suporte:
  - No Windows desde 77 ou posterior

  #### Descrição
  Permite que os processos do Microsoft Edge comecem a entrar no sistema operacional e continuem a executar após a última janela do navegador ser fechada. Neste cenário, os aplicativos de plano de fundo e a sessão de navegação atual permanecem ativos, incluindo qualquer cookie de sessão. Um processo aberto em segundo plano exibe um ícone na bandeja do sistema e sempre é possível fechá-lo.

Se você habilitar essa política, o modo de tela de fundo será ativado.

Se você desabilitar essa política, o modo de tela de fundo será desabilitado.

Se você não configurar essa política, o modo de tela de fundo será desabilitado inicialmente, e o usuário poderá configurar seu comportamento em edge://settings/system.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: Sim
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: BackgroundModeEnabled
  - Nome da Política de Grupo: Continuar executando aplicativos de segundo plano após o Microsoft Edge ser fechado
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): Administrative Templates/Microsoft Edge - Default Settings (usuários podem substituir)/
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nome do valor: BackgroundModeEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  

  [Voltar ao início](#microsoft-edge---policies)

  ### BackgroundTemplateListUpdatesEnabled
  #### Permite atualizações em segundo plano para a lista de modelos disponíveis para Coleções e outros recursos que usam modelos
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 79 ou mais recente

  #### Descrição
  Permite atualizações em segundo plano para a lista de modelos disponíveis para Coleções e outros recursos que usam modelos.  Os modelos são usados para extrair metadados ricos de uma página da Web quando a página é salva em um conjunto.

Se você habilitar essa configuração ou se a configuração estiver desconfigurada, a lista de modelos disponíveis será baixada no segundo plano de um serviço da Microsoft a cada 24 horas.

Se você desabilitar essa configuração, a lista de modelos disponíveis será baixada sob demanda. Esse tipo de download pode resultar em pequenas penalidades de desempenho para coletas e outros recursos.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: BackgroundTemplateListUpdatesEnabled
  - Nome da Política de Grupo: Permite atualizações em segundo plano para a lista de modelos disponíveis para Coleções e outros recursos que usam modelos
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: BackgroundTemplateListUpdatesEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: BackgroundTemplateListUpdatesEnabled
  - Valor de exemplo:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### BingAdsSuppression
  #### Bloquear todos os anúncios nos resultados de pesquisa do Bing
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 83 ou mais recente

  #### Descrição
  Habilita uma experiência de pesquisa sem anúncios no Bing.com

Se você habilitar essa política, um usuário poderá pesquisar no bing.com e ter uma experiência de pesquisa sem anúncios. Ao mesmo tempo, a configuração da Pesquisa Segura será definida como “Estrita” e não poderá ser alterada pelo usuário.

Se você não configurar essa política, a experiência padrão terá anúncios nos resultados da pesquisa em bing.com. O filtro da Pesquisa Segura será definido como “Moderado” por padrão e poderá ser alterado pelo usuário.

Essa política só estará disponível para SKUs K-12 identificados como locatários EDU pela Microsoft.

Confira [https://go.microsoft.com/fwlink/?linkid=2119711](https://go.microsoft.com/fwlink/?linkid=2119711) para saber mais sobre essa política ou se os seguintes cenários se aplicam a você:

* Você tem um locatário EDU, mas a política não funciona.

* Foi permitido que seu IP tenha uma experiência de pesquisa gratuita do AD.

* Você estava enfrentando uma experiência de pesquisa sem anúncios na Versão Prévia do Microsoft Edge e deseja atualizar para a nova versão do Microsoft Edge.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: não requer a reinicialização do navegador

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: BingAdsSuppression
  - Nome da Política de Grupo: Bloquear todos os anúncios nos resultados de pesquisa do Bing
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: BingAdsSuppression
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: BingAdsSuppression
  - Valor de exemplo:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### BlockThirdPartyCookies
  #### Bloquear cookies de terceiros
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Impedir que os elementos da página da web que não pertencem ao domínio que está na barra de endereços definam cookies.

Se você habilitar essa política, os elementos de página da Web que não pertencem ao domínio que está na barra de endereços não poderão definir cookies

Se você desabilitar essa política, os elementos da página da Web de domínios diferentes da barra de endereços poderão definir os cookies.

Se você não configurar essa política, os cookies de terceiros serão habilitados, mas os usuários poderão alterar essa configuração.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: Sim
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: BlockThirdPartyCookies
  - Nome da Política de Grupo: Bloquear cookies de terceiros
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): Administrative Templates/Microsoft Edge - Default Settings (usuários podem substituir)/
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nome do valor: BlockThirdPartyCookies
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000000
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: BlockThirdPartyCookies
  - Valor de exemplo:
``` xml
<false/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### BrowserAddProfileEnabled
  #### Habilitar a criação de perfil no menu de atalho de identidade ou na página de configurações
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Permite que os usuários criem novos perfis usando a opção **Adicionar perfil**.
Se você habilitar essa política ou não a configurar, o Microsoft Edge permitirá que os usuários usem **Adicionar perfil** no submenu Identidade ou na página de Configurações para criar novos perfis.

Se você desabilitar essa política, os usuários não poderão adicionar novos perfis no submenu Identidade ou na página de Configurações.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: BrowserAddProfileEnabled
  - Nome da Política de Grupo: Habilitar a criação de perfil no menu de atalho de identidade ou na página de configurações
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: BrowserAddProfileEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: BrowserAddProfileEnabled
  - Valor de exemplo:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### BrowserGuestModeEnabled
  #### Habilitar o modo convidado
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Habilitar a opção para permitir o uso de perfis convidados no Microsoft Edge. Em um perfil de convidado, o navegador não importa dados de navegação de perfis existentes e exclui a navegação de dados quando todos os perfis de convidado forem fechados.

Se você habilitar essa política ou não a configurar, o Microsoft Edge permitirá que os usuários naveguem em perfis convidados.

Se você desabilitar essa política, o Microsoft Edge não permitirá que os usuários naveguem em perfis convidados.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: BrowserGuestModeEnabled
  - Nome da Política de Grupo: Habilitar o modo convidado
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: BrowserGuestModeEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: BrowserGuestModeEnabled
  - Valor de exemplo:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### BrowserNetworkTimeQueriesEnabled
  #### Permitir consultas a um serviço de Hoário da Rede do Navegador
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Impede que o Microsoft Edge envie consultas para um serviço de tempo de rede do navegador para recuperar um carimbo de data/hora exato.

Se você desabilitar essa política, o Microsoft Edge deixará de enviar consultas para o serviço de tempo de rede do navegador.

Se você habilitar essa política ou não a configurar, o Microsoft Edge enviará algumas consultas para um serviço de tempo de rede do navegador.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: BrowserNetworkTimeQueriesEnabled
  - Nome da Política de Grupo: Permitir consultas a um serviço de Hoário da Rede do Navegador
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: BrowserNetworkTimeQueriesEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: BrowserNetworkTimeQueriesEnabled
  - Valor de exemplo:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### BrowserSignin
  #### Configurações de entrada do navegador
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Especificar se um usuário pode entrar no Microsoft Edge com a conta dele e usar serviços relacionados à conta, como sincronizar e logon único. Para controlar a disponibilidade da sincronização, use a política [SyncDisabled](#syncdisabled), em vez disso.

Se você definir essa política como 'Desabilitar', certifique-se de também definir a política [NonRemovableProfileEnabled](#nonremovableprofileenabled) para desabilitada porque [NonRemovableProfileEnabled](#nonremovableprofileenabled) desabilita a criação de um perfil de navegador conectado automaticamente. Se ambas as políticas estiverem definidas, o Microsoft Edge usará a política "desabilitar a entrada no navegador" e se comportará como se [NonRemovableProfileEnabled](#nonremovableprofileenabled) estivesse definida como desabilitada.

Se você definir essa política como 'Habilitar', os usuários poderão entrar no navegador. Entrar no navegador não significa que a sincronização esteja ativada por padrão. O usuário deve aceitar separadamente para usar esse recurso.

Se você definir essa política como 'Forçar', os usuários deverão entrar em um perfil para usar o navegador. Por padrão, isso permitirá que o usuário escolha se deseja sincronizar com sua conta, a menos que a sincronização seja desabilitada pelo administrador do domínio ou com a política [SyncDisabled](#syncdisabled). O valor padrão da política [BrowserGuestModeEnabled](#browserguestmodeenabled) é definido como falso.

Se você não configurar essa política, os usuários poderão decidir se desejam habilitar a opção de entrada no navegador e usá-la como alternativa.

Mapeamento das opções de política:

* Desabilitar (0) = Desabilitar a entrada no navegador

* Habilitar (1) = Habilitar a entrada no navegador

* Forçar (2) = Forçar os usuários a entrar para usar o navegador

Use as informações anteriores ao configurar essa política.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: não requer a reinicialização do navegador

  #### Tipo de dados:
  - Inteiro

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: BrowserSignin
  - Nome da Política de Grupo: Configurações de entrada do navegador
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: BrowserSignin
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000002
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: BrowserSignin
  - Valor de exemplo:
``` xml
<integer>2</integer>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### BuiltInDnsClientEnabled
  #### Usar o cliente DNS interno
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Controla se o cliente DNS interno deve ser usado.

Isso não afeta quais servidores DNS serão usados, apenas a pilha de software que será usada para se comunicar com eles. Por exemplo, se o sistema operacional estiver configurado para usar um servidor DNS corporativo, esse mesmo servidor seria usado pelo cliente DNS interno. No entanto, é possível que o cliente DNS interno enderece servidores de maneiras diferentes usando protocolos mais modernos relacionados a DNS, como o DNS em TLS.

Se você habilitar essa política, o cliente DNS interno será usado, se ele estiver disponível.

Se você desabilitar essa política, o cliente nunca será utilizado.

Se você não configurar essa política, o cliente DNS interno ficará habilitado por padrão no MacOS, e os usuários poderão alterar se desejam usar o cliente DNS interno editando edge://flags ou especificando um sinalizador de linha de comando.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: BuiltInDnsClientEnabled
  - Nome da Política de Grupo: Usar o cliente DNS interno
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: BuiltInDnsClientEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: BuiltInDnsClientEnabled
  - Valor de exemplo:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### BuiltinCertificateVerifierEnabled
  #### Determina se o verificador interno de certificado será usado para verificar certificados do servidor (preterido)
  >SUBSTITUÍDO: Essa política está preterida. Ela tem suporte no momento, mas se tornará obsoleta em uma versão futura.
  
  #### Versões com suporte:
  - No macOS desde 83 ou posterior

  #### Descrição
  Essa política foi preterida porque seu objetivo é apenas servir como um mecanismo de curto prazo, para dar mais tempo para que as empresas atualizem seus ambientes e relatem problemas se forem considerados incompatíveis com o verificador de certificados interno.

Esta política não funcionará no Microsoft Edge versão 87, quando o suporte para o verificador de certificado herdado no Mac OS X está planejado para ser removido.


  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: não requer a reinicialização do navegador

  #### Tipo de dados:
  - Booliano

  

  #### Informações e configurações do Mac
  - Nome da chave de preferência: BuiltinCertificateVerifierEnabled
  - Valor de exemplo:
``` xml
<false/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### CertificateTransparencyEnforcementDisabledForCas
  #### Desabilitar a imposição da transparência do certificado para obter uma lista de hashes subjectPublicKeyInfo
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Desabilita a imposição da transparência do certificado para obter uma lista de hashes subjectPublicKeyInfo.

Essa política permite que você desabilite os requisitos de divulgação de transparência do certificado para cadeias de certificados que contêm certificados com um dos hashes subjectPublicKeyInfo especificados. Isso permite certificados que, de outra forma, seriam não confiáveis por não serem divulgados publicamente adequadamente para ainda serem usados em hosts corporativos.

Para desabilitar a imposição da transparência do certificado quando essa política estiver definida, um dos seguintes conjuntos de condições deve ser atendido:
1. O código hash é o subjectPublicKeyInfo do certificado do servidor.
2. O código hash é de um subjectPublicKeyInfo exibido em um certificado da autoridade de certificação na cadeia de certificados, esse certificado da autoridade de certificação está restrito pela extensão X. 509v3 nameConstraints, um ou mais directoryName nameConstraints estão presentes no permittedSubtrees, e o directoryName contém um atributo organizationName.
3. O código hash é de um subjectPublicKeyInfo que aparece em um certificado da autoridade de certificação na cadeia de certificados, o certificado da autoridade de certificação tem um ou mais atributos OrganizationName no assunto do certificado, e o certificado do servidor contém o mesmo número de atributos OrganizationName, na mesma ordem, e com valores idênticos byte para byte.

Um código hash subjectPublicKeyInfo é especificado por meio da concatenação do nome do algoritmo de hash, do caractere "/" e da codificação Base64 desse algoritmo hash aplicado ao subjectPublicKeyInfo codificado por DER do certificado especificado. A codificação Base64 tem o mesmo formato de uma impressão digital SPKI, conforme definido na RFC 7469, seção 2.4. Algoritmos de hash não reconhecidos são ignorados. O único algoritmo de hash compatível no momento é "sha256".

Se você desabilitar essa política ou não a configurar, todo o certificado necessário para ser divulgado por meio da transparência do certificado será tratado como não confiável, caso não seja divulgado de acordo com a política de transparência do certificado.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: CertificateTransparencyEnforcementDisabledForCas
  - Nome da Política de Grupo: Desabilitar a imposição da transparência do certificado para obter uma lista de hashes subjectPublicKeyInfo
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForCas
  - Caminho (recomendado): N/A
  - Nome do valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de exemplo:
```
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForCas\1 = "sha256/AAAAAAAAAAAAAAAAAAAAAA=="
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForCas\2 = "sha256//////////////////////w=="

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: CertificateTransparencyEnforcementDisabledForCas
  - Valor de exemplo:
``` xml
<array>
  <string>sha256/AAAAAAAAAAAAAAAAAAAAAA==</string>
  <string>sha256//////////////////////w==</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### CertificateTransparencyEnforcementDisabledForLegacyCas
  #### Desabilitar a imposição da transparência do certificado para uma lista de autoridades de certificação herdadas
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Desabilita a imposição de requisitos de transparência de certificado para uma lista de CAS (autoridades de certificação) herdadas.

Essa política permite que você desabilite os requisitos de divulgação de transparência do certificado para cadeias de certificados que contêm certificados com um dos hashes subjectPublicKeyInfo especificados. Isso permite certificados que, de outra forma, seriam não confiáveis por não serem divulgados publicamente adequadamente continuem sendo usados em hosts corporativos.

Para que a imposição de transparência de certificados seja desabilitada, você deve definir o hash para um subjectPublicKeyInfo que aparece em um certificado de autoridade de certificação, reconhecido como uma autoridade de certificação herdada. Uma autoridade de certificação herdada é uma autoridade de certificação publicamente confiável por padrão por um ou mais sistemas operacionais com suporte no Microsoft Edge.

Você especifica um código hash subjectPublicKeyInfo concatenando o nome do algoritmo de hash, o caractere "/" e a codificação Base64 desse algoritmo de hash aplicado ao subjectPublicKeyInfo codificado por DER do certificado especificado. A codificação Base64 tem o mesmo formato de uma impressão digital SPKI, conforme definido na RFC 7469, seção 2.4. Algoritmos de hash não reconhecidos são ignorados. O único algoritmo de hash compatível no momento é "sha256".

Se não a configurar essa política, todo o certificado necessário para ser divulgado por meio da transparência do certificado será tratado como não confiável, caso não seja divulgado de acordo com a política de transparência do certificado.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: CertificateTransparencyEnforcementDisabledForLegacyCas
  - Nome da Política de Grupo: Desabilitar a imposição da transparência do certificado para uma lista de autoridades de certificação herdadas
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForLegacyCas
  - Caminho (recomendado): N/A
  - Nome do valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de exemplo:
```
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForLegacyCas\1 = "sha256/AAAAAAAAAAAAAAAAAAAAAA=="
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForLegacyCas\2 = "sha256//////////////////////w=="

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: CertificateTransparencyEnforcementDisabledForLegacyCas
  - Valor de exemplo:
``` xml
<array>
  <string>sha256/AAAAAAAAAAAAAAAAAAAAAA==</string>
  <string>sha256//////////////////////w==</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### CertificateTransparencyEnforcementDisabledForUrls
  #### Desabilitar a imposição da transparência do certificado para URLs específicas
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Desabilita a imposição de requisitos de transparência de certificado para as URLs listadas.

Essa política permite que você não divulgue certificados para os nomes de host nas URLs especificadas por meio da Transparência de Certificados. Isso permite que você use certificados que, de outra forma, seriam não confiáveis, pois eles não foram divulgados publicamente, mas dificulta a detecção de certificados emitidos incorretamente para esses hosts.

Formate seu padrão de URL de acordo com [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322). Como os certificados são válidos para um determinado nome de host, independente do esquema, da porta ou do caminho, apenas a parte do nome do host da URL é considerada. Não há suporte para hosts curinga.

Se você não configurar essa política, todo o certificado que deve ser divulgado por meio da transparência do certificado será tratado como não confiável, se não for divulgado.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: CertificateTransparencyEnforcementDisabledForUrls
  - Nome da Política de Grupo: Desabilitar a imposição da transparência do certificado para URLs específicas
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForUrls
  - Caminho (recomendado): N/A
  - Nome do valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de exemplo:
```
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForUrls\1 = "contoso.com"
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForUrls\2 = ".contoso.com"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: CertificateTransparencyEnforcementDisabledForUrls
  - Valor de exemplo:
``` xml
<array>
  <string>contoso.com</string>
  <string>.contoso.com</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### ClearBrowsingDataOnExit
  #### Limpar os dados da navegação quando o Microsoft Edge é fechado
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 78 ou mais recente

  #### Descrição
  O Microsoft Edge não limpa os dados de navegação por padrão quando é fechado. Pesquisar dados inclui informações inseridas em formulários, senhas e até mesmo os sites visitados.

Se você habilitar essa política, todos os dados de navegação serão excluídos sempre que o Microsoft Edge for fechado. Observe que, se você habilitar essa política, ela terá precedência sobre a configuração [DefaultCookiesSetting](#defaultcookiessetting)

Se você desabilitar ou não configurar essa política, os usuários poderão configurar a opção limpar dados de navegação nas Configurações.

Se você habilitar essa política, não configure a política [AllowDeletingBrowserHistory](#allowdeletingbrowserhistory) ou [ClearCachedImagesAndFilesOnExit](#clearcachedimagesandfilesonexit), porque todos elas lidam com a exclusão de dados de navegação. Se você configurar as políticas anteriores e essa política, todos os dados de navegação serão excluídos quando o Microsoft Edge for fechado, independentemente de como você configurou [AllowDeletingBrowserHistory](#allowdeletingbrowserhistory) ou [ClearCachedImagesAndFilesOnExit](#clearcachedimagesandfilesonexit).

Para impedir que os cookies sejam excluídos na saída, configure a política [SaveCookiesOnExit](#savecookiesonexit).

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: Sim
  - Atualização dinâmica das políticas: não requer a reinicialização do navegador

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: ClearBrowsingDataOnExit
  - Nome da Política de Grupo: Limpar os dados da navegação quando o Microsoft Edge é fechado
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): Administrative Templates/Microsoft Edge - Default Settings (usuários podem substituir)/
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nome do valor: ClearBrowsingDataOnExit
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ClearBrowsingDataOnExit
  - Valor de exemplo:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### ClearCachedImagesAndFilesOnExit
  #### Limpar arquivos e imagens armazenadas em cache ao fechar o Microsoft Edge
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 83 ou mais recente

  #### Descrição
  O Microsoft Edge não limpa arquivos e imagens armazenados em cache por padrão quando é fechado.

Se você habilitar essa política, os arquivos e imagens armazenados em cache serão excluídos sempre que o Microsoft Edge for fechado.

Se você desabilitar essa política, os usuários não poderão configurar as imagens e arquivos armazenados em cache em edge://settings/clearBrowsingDataOnClose.

Se você não configurar essa política, os usuários poderão escolher se imagens e arquivos armazenados em cache serão limpos na saída.

Se você desabilitar essa política, não habilite a política [ClearBrowsingDataOnExit](#clearbrowsingdataonexit), porque ambas lidam com a exclusão de dados. Se você configurar ambos, a política [ClearBrowsingDataOnExit](#clearbrowsingdataonexit) terá precedência e excluirá todos os dados quando o Microsoft Edge fechar, independentemente de como você configurou [ClearCachedImagesAndFilesOnExit](#clearcachedimagesandfilesonexit).

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: Sim
  - Atualização dinâmica das políticas: não requer a reinicialização do navegador

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: ClearCachedImagesAndFilesOnExit
  - Nome da Política de Grupo: Limpar arquivos e imagens armazenadas em cache ao fechar o Microsoft Edge
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): Administrative Templates/Microsoft Edge - Default Settings (usuários podem substituir)/
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nome do valor: ClearCachedImagesAndFilesOnExit
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ClearCachedImagesAndFilesOnExit
  - Valor de exemplo:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### ClickOnceEnabled
  #### Permitir que os usuários abram arquivos usando o protocolo ClickOnce
  
  
  #### Versões com suporte:
  - No Windows desde 78 ou posterior

  #### Descrição
  Permita que os usuários abram arquivos usando o protocolo ClickOnce. O protocolo ClickOnce permite que os sites solicitem que o navegador abra arquivos de uma URL específica usando o manipulador de arquivo ClickOnce no computador ou dispositivo do usuário.

Se você habilitar essa política, os usuários poderão abrir arquivos usando o protocolo ClickOnce. Essa política substitui a configuração ClickOnce do usuário na página edge://flags/.

Se você desabilitar essa política, os usuários não poderão abrir arquivos usando o protocolo ClickOnce. Em vez disso, o arquivo será salvo no sistema de arquivos usando o navegador. Essa política substitui a configuração ClickOnce do usuário na página edge://flags/.

Se você não configurar essa política, os usuários com versões do Microsoft Edge anteriores ao Microsoft Edge 87 não conseguirão abrir arquivos usando o protocolo ClickOnce por padrão. Os usuários têm a opção de habilitar o uso do protocolo ClickOnce com a página edge://flags/. Os usuários com o Microsoft Edge versões 87 e posterior podem abrir arquivos usando o protocolo ClickOnce por padrão, mas têm a opção de desabilitar o protocolo ClickOnce com a página edge://flags/.

A desabilitação do ClickOnce poderá impedir que aplicativos ClickOnce (arquivos .application) sejam iniciados corretamente.

Para obter mais informações sobre o ClickOnce, confira [https://go.microsoft.com/fwlink/?linkid=2103872](https://go.microsoft.com/fwlink/?linkid=2103872) e [https://go.microsoft.com/fwlink/?linkid=2099880](https://go.microsoft.com/fwlink/?linkid=2099880).

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: ClickOnceEnabled
  - Nome da Política de Grupo: Permitir que os usuários abram arquivos usando o protocolo ClickOnce
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: ClickOnceEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000000
```


  

  [Voltar ao início](#microsoft-edge---policies)

  ### CollectionsServicesAndExportsBlockList
  #### Bloquear o acesso a uma lista especificada de serviços e exportar destinos em Coleções
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 86 ou mais recente

  #### Descrição
  Listar os serviços específicos e exportar destinos que os usuários não podem acessar no recurso Coleções no Microsoft Edge. Isso inclui exibir dados adicionais do Bing e exportar coleções para produtos da Microsoft ou parceiros externos.

Se você habilitar essa política, os serviços e os destinos de exportação correspondentes à lista específica serão bloqueados.

Se você não configurar essa política, não há restrições para os tipos de extensão aceitáveis.

Mapeamento das opções de política:

* pinterest_suggestions (pinterest_suggestions) = Sugestões do Pinterest

Use as informações anteriores ao configurar essa política.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: não requer a reinicialização do navegador

  #### Tipo de dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: CollectionsServicesAndExportsBlockList
  - Nome da GP: Bloquear o acesso a uma lista especificada de serviços e exportar destinos em Coleções
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge\URLBlocklist
  - Caminho (recomendado): N/A
  - Nome do valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de exemplo:
```
SOFTWARE\Policies\Microsoft\Edge\CollectionsServicesAndExportsBlockList\1 = "pinterest_suggestions"

```


  #### Informações e configurações do Mac
  - Nome da Chave de Preferência: CollectionsServicesAndExportsBlockList
  - Valor de exemplo:
``` xml
<array>
  <string>pinterest_suggestions</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### CommandLineFlagSecurityWarningsEnabled
  #### Habilitar avisos de segurança para sinalizadores de linha de comando
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 78 ou mais recente

  #### Descrição
  Se desabilitada, essa política impede que os avisos de segurança apareçam quando o Microsoft Edge é iniciado com sinalizadores de linha de comando potencialmente perigosos.

Se estiver habilitada ou desativada, os avisos de segurança serão exibidos quando esses sinalizadores de linha de comando forem usados para iniciar o Microsoft Edge.

Por exemplo, o sinalizador--disable-gpu-sandbox gera este aviso: você está usando um sinalizador de linha de comando sem suporte:--disable-gpu-sandbox. Isso representa riscos de segurança e estabilidade.

Essa política está disponível apenas nas instâncias do Windows que fazem parte de um domínio do Microsoft Active Directory, em instâncias do Windows 10 Pro ou Enterprise que estejam inscritas no gerenciamento de dispositivos ou em instâncias do macOS que são gerenciadas por meio do MDM ou passaram a fazer parte de um domínio por meio de MCX.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: não requer a reinicialização do navegador

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: CommandLineFlagSecurityWarningsEnabled
  - Nome da Política de Grupo: Habilitar avisos de segurança para sinalizadores de linha de comando
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: CommandLineFlagSecurityWarningsEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: CommandLineFlagSecurityWarningsEnabled
  - Valor de exemplo:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### ComponentUpdatesEnabled
  #### Habilitar atualizações de componentes no Microsoft Edge
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Se você habilitar ou não configurar essa política, as atualizações de componentes serão habilitadas no Microsoft Edge.

Se você desabilitar essa política ou defini-la como falsa, as atualizações de componentes serão desabilitadas para todos os componentes no Microsoft Edge.

No entanto, alguns componentes estão isentos desta política. Isso inclui qualquer componente que não contenha um código executável, que não altere significativamente o comportamento do navegador, ou que seja essencial para a segurança. Ou seja, as atualizações consideradas "essenciais para segurança" ainda serão aplicadas, mesmo que você desabilite essa política.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: não requer a reinicialização do navegador

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: ComponentUpdatesEnabled
  - Nome da Política de Grupo: Habilitar atualizações de componentes no Microsoft Edge
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: ComponentUpdatesEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ComponentUpdatesEnabled
  - Valor de exemplo:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### ConfigureDoNotTrack
  #### Configurar Não Rastrear
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Especificar se deseja enviar solicitações Não Rastrear aos sites que solicitam informações de rastreamento. As solicitações Não Rastrear permitem que os sites visitados saibam que você não deseja que suas atividades de navegação sejam controladas. Por padrão, o Microsoft Edge não envia solicitações Não Rastrear, mas os usuários podem ativar esse recurso para enviá-las.

Se você habilitar essa política, as solicitações Não Rastrear sempre serão enviadas a sites que solicitam informações de rastreamento.

Se você desabilitar essa política, as solicitações nunca serão enviadas.

Se você não configurar essa política, os usuários poderão optar por enviar essas solicitações.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: ConfigureDoNotTrack
  - Nome da Política de Grupo: Configurar Não Rastrear
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: ConfigureDoNotTrack
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000000
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ConfigureDoNotTrack
  - Valor de exemplo:
``` xml
<false/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### ConfigureOnPremisesAccountAutoSignIn
  #### Configura o login automático com uma conta de domínio do Active Directory quando não houver nenhuma conta de domínio do Azure AD.
  
  
  #### Versões com suporte:
  - No Windows desde 81 ou posterior

  #### Descrição
  Habilite o uso de contas do Active Directory para entrada automática se os computadores dos usuários forem Ingressados no Domínio e seu ambiente não for híbrido. Se você deseja que os usuários se conectem automaticamente com as contas do Azure Active Directory, faça o ingresso do Azure AD (Confira [https://go.microsoft.com/fwlink/?linkid=2118197](https://go.microsoft.com/fwlink/?linkid=2118197) para obter mais informações) ou o ingresso híbrido (consulte [https://go.microsoft.com/fwlink/?linkid=2118365](https://go.microsoft.com/fwlink/?linkid=2118365) para saber mais) em seu ambiente.

Se você configurou a política [BrowserSignin](#browsersignin) como desabilitada, essa política não terá efeito.

Se você habilitar essa política e configurá-la para "SignInAndMakeDomainAccountNonRemovable", o Microsoft Edge entrará automaticamente em usuários que estejam em máquinas ingressados pelo domínio usando suas contas do Active Directory.

Se você definir essa política como "Desabilitada" ou não a definir, o Microsoft Edge não entrará automaticamente em usuários que estejam em computadores ingressados no domínio com contas do Active Directory.

Mapeamento das opções de política:

* Desabilitado (0) = Desabilitado

* SignInAndMakeDomainAccountNonRemovable (1) = Entrar e tornar a conta de domínio não removível

Use as informações anteriores ao configurar essa política.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: não requer a reinicialização do navegador

  #### Tipo de dados:
  - Inteiro

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: ConfigureOnPremisesAccountAutoSignIn
  - Nome da Política de Grupo: Configurar o login automático com uma conta de domínio do Active Directory quando não houver nenhuma conta de domínio do Azure AD.
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: ConfigureOnPremisesAccountAutoSignIn
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000000
```


  

  [Voltar ao início](#microsoft-edge---policies)

  ### ConfigureOnlineTextToSpeech
  #### Configurar Conversão de Texto em Fala online
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Defina se o navegador pode aproveitar a Conversão de Texto em Fala Online, parte dos Serviços Cognitivos do Azure. Essas fontes de voz têm qualidade melhor do que as fontes de voz pré-instaladas do sistema.

Se você habilitar ou não configurar essa política, os aplicativos baseados na Web que usam a API SpeechSynthesis poderão usar fontes de voz da Conversão de Texto em Fala Online.

Se você desabilitar essa política, as fontes de voz não estarão disponíveis.

Leia mais sobre este recurso aqui: API do SpeechSynthesis: [https://go.microsoft.com/fwlink/?linkid=2110038](https://go.microsoft.com/fwlink/?linkid=2110038) Serviços Cognitivos: [https://go.microsoft.com/fwlink/?linkid=2110141](https://go.microsoft.com/fwlink/?linkid=2110141)

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: ConfigureOnlineTextToSpeech
  - Nome da Política de Grupo: Configurar Conversão de Texto em Fala online
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: ConfigureOnlineTextToSpeech
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ConfigureOnlineTextToSpeech
  - Valor de exemplo:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### ConfigureShare
  #### Configurar a experiência de compartilhamento
  
  
  #### Versões com suporte:
  - No Windows desde 83 ou posterior

  #### Descrição
  Se você definir essa política como “ShareAllowed” (o padrão), os usuários poderão acessar a experiência de compartilhamento do Windows 10 no menu Configurações e Mais no Microsoft Edge para compartilhar com outros aplicativos no sistema.

Se você definir essa política como "ShareDisallowed", os usuários não conseguirão acessar a experiência Compartilhamento do Windows 10. Se o botão compartilhar estiver na barra de ferramentas, ele também será ocultado.

Mapeamento das opções de política:

* ShareAllowed (0) = Permitir o uso da experiência Compartilhamento

* ShareDisallowed (1) = Não permitir o uso da experiência Compartilhamento

Use as informações anteriores ao configurar essa política.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: não requer a reinicialização do navegador

  #### Tipo de dados:
  - Inteiro

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: ConfigureShare
  - Nome da Política de Grupo: Configurar a experiência de Compartilhamento.
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: ConfigureShare
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  

  [Voltar ao início](#microsoft-edge---policies)

  ### CustomHelpLink
  #### Especificar um link de ajuda personalizado
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 79 ou mais recente

  #### Descrição
  Especificar um link para o menu Ajuda ou a tecla F1.

Se você habilitar essa política, um administrador poderá especificar um link para o menu Ajuda ou para a tecla F1.

Se você desabilitar ou não configurar essa política, será usado o link padrão para o menu Ajuda ou a tecla F1.

Essa política está disponível apenas nas instâncias do Windows que fazem parte de um domínio do Microsoft Active Directory, em instâncias do Windows 10 Pro ou Enterprise que estejam inscritas no gerenciamento de dispositivos ou em instâncias do macOS que são gerenciadas por meio do MDM ou passaram a fazer parte de um domínio por meio de MCX.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - String

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: CustomHelpLink
  - Nome da Política de Grupo: Especificar um link de ajuda personalizado
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: CustomHelpLink
  - Tipo do valor: REG_SZ
  ##### Valor de exemplo:
```
"https://go.microsoft.com/fwlink/?linkid=2080734"
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: CustomHelpLink
  - Valor de exemplo:
``` xml
<string>https://go.microsoft.com/fwlink/?linkid=2080734</string>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### DNSInterceptionChecksEnabled
  #### Verificações de interceptações DNS habilitadas
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 80 ou mais recente

  #### Descrição
  Essa política configura uma opção local que pode ser usada para desabilitar as verificações de interceptações de DNS. Essas verificações tentam descobrir se o navegador está atrás de um proxy que redireciona nomes de host desconhecidos.

Essa detecção pode não ser necessária em um ambiente corporativo onde a configuração de rede é conhecida. Ela pode ser desabilitada para evitar o tráfego DNS e HTTP adicional no início e cada alteração de configuração de DNS.

Se você habilitar ou não definir essa política, as verificações de interceptações DNS serão executadas.

Se você desabilitar essa política, não será realizada a verificação de interceptações de DNS.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: DNSInterceptionChecksEnabled
  - Nome da Política de Grupo: Verificações de interceptações DNS habilitadas
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: DNSInterceptionChecksEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: DNSInterceptionChecksEnabled
  - Valor de exemplo:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### DefaultBrowserSettingEnabled
  #### Definir o Microsoft Edge como o navegador padrão
  
  
  #### Versões com suporte:
  - No Windows 7 e no macOS desde 77 ou posterior

  #### Descrição
  Se você definir essa política como verdadeira, o Microsoft Edge sempre verificará na inicialização se é o navegador padrão e se registrará automaticamente, se possível.

Se você definir essa política como falsa, o Microsoft Edge será interrompido de verificar se é o padrão e desativa os controles de usuário para essa opção.

Se você não definir essa política, o Microsoft Edge permite aos usuários controlar se esse é o padrão e, caso contrário, se as notificações do usuário devem ser exibidas.

Observação para os administradores do Windows: essa política só funciona em computadores que executam o Windows 7. Para as versões mais recentes do Windows, você precisará implantar um arquivo de "associações de aplicativos padrão" que torna o Microsoft Edge o manipulador para os protocolos https e http (e, opcionalmente, os formatos de arquivo e protocolo FTP, como. html,. htm,. pdf,. svg,. webp). Consulte [https://go.microsoft.com/fwlink/?linkid=2094932](https://go.microsoft.com/fwlink/?linkid=2094932) para mais informações.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: DefaultBrowserSettingEnabled
  - Nome da Política de Grupo: Definir o Microsoft Edge como o navegador padrão
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: DefaultBrowserSettingEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: DefaultBrowserSettingEnabled
  - Valor de exemplo:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### DefaultSearchProviderContextMenuAccessAllowed
  #### Permitir que o menu de contexto do provedor de pesquisa padrão pesquise no acesso
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 85 ou mais recente

  #### Descrição
  Permite o uso de um provedor de pesquisa padrão no menu de contexto.

Se você definir essa política para desabilitada, o item de menu de contexto da pesquisa que depende do provedor de pesquisa padrão e da pesquisa da barra lateral não estará disponível.

Se essa política estiver definida como habilitada ou não definida, o item de menu de contexto para o seu provedor de pesquisa padrão e a pesquisa da barra lateral estarão disponíveis.

O valor da política será aplicado apenas quando a política [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) estiver ativada, e não será aplicado em caso contrário.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: DefaultSearchProviderContextMenuAccessAllowed
  - Nome da GP: Permitir que o menu de contexto do provedor de pesquisa padrão pesquise no acesso
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: DefaultSearchProviderContextMenuAccessAllowed
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da Chave de Preferência: DefaultSearchProviderContextMenuAccessAllowed
  - Valor de exemplo:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### DefaultSensorsSetting
  #### Configuração de sensores padrão
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 86 ou mais recente

  #### Descrição
  Defina se os sites podem acessar e usar sensores como sensores de movimento e de luz. Você pode bloquear ou permitir completamente que os sites tenham acesso aos sensores.

A configuração da política como 1 permite que os sites acessem e usem os sensores. Definir a política para 2 nega o acesso aos sensores.

Você pode substituir essa política por padrões de URL específicos usando as políticas [SensorsAllowedForUrls](#sensorsallowedforurls) e [SensorsBlockedForUrls](#sensorsblockedforurls).

Se você não configurar essa política, os sites podem acessar e usar os sensores, e os usuários poderão alterar essa configuração. Esse é o padrão global para [SensorsAllowedForUrls](#sensorsallowedforurls) e [SensorsBlockedForUrls](#sensorsblockedforurls).

Mapeamento das opções de política:

* AllowSensors (1) = permitir que os sites acessem os sensores

* BlockSensors (2) = não permitir que os sites acessem os sensores

Use as informações anteriores ao configurar essa política.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Inteiro

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: DefaultSensorsSetting
  - Nome da Política de Grupo: Configuração de sensores padrão
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome exclusivo da Política de Grupo: DefaultSensorsSetting
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000002
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: DefaultSensorsSetting
  - Valor de exemplo:
``` xml
<integer>2</integer>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### DefaultSerialGuardSetting
  #### Controlar o uso da API serial
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 86 ou mais recente

  #### Descrição
  Defina se os sites podem acessar portas seriais. Você pode bloquear completamente o acesso ou perguntar ao usuário toda vez que o site deseja obter acesso a portas seriais.

Definir a política como 3 permite que os sites solicitem acesso à portas seriais. Definir a política para 2 nega o acesso às portas seriais.

Você pode substituir essa política por padrões de URL específicos usando as políticas [SerialAskForUrls](#serialaskforurls) e [SerialBlockedForUrls](#serialblockedforurls).

Se você não configurar essa política, por padrão, os sites poderão perguntar aos usuários se eles podem acessar uma porta serial, e os usuários podem alterar essa configuração.

Mapeamento das opções de política:

* BlockSerial (2) = não permitir que todos os sites solicitem acesso às portas seriais pela API serial

* AskSerial (3) = permitir que os sites solicitem permissão para que o usuário acesse uma porta serial

Use as informações anteriores ao configurar essa política.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Inteiro

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: DefaultSerialGuardSetting
  - Nome exclusivo da Política de Grupo: Controlar o uso da API serial
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do Valor: DefaultSerialGuardSetting
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000002
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: DefaultSerialGuardSetting
  - Valor de exemplo:
``` xml
<integer>2</integer>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### DelayNavigationsForInitialSiteListDownload
  #### Exigir que a lista de sites no Modo Empresarial esteja disponível antes da navegação na guia
  
  
  #### Versões com suporte:
  - No Windows desde 84 ou posterior

  #### Descrição
  Permite que você especifique se o Microsoft Edge vai aguardar até que o navegador baixe a lista de sites inicial no Modo Empresarial. Essa configuração destina-se ao cenário em que a home page do navegador deve ser carregada no modo do Internet Explorer e é importante fazer isso no navegador pela primeira vez, após o modo do IE estar habilitado. Se esse cenário não existir, recomendamos não habilitar essa configuração porque isso pode afetar negativamente o desempenho do carregamento da home page. A configuração se aplica somente quando o Microsoft Edge não tiver uma lista de sites do Modo Empresarial em cache, como no primeiro navegador executado após o modo IE estar habilitado.

Essa configuração funciona em conjunto com a: [InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel) está definida como "IEMode" e a política [InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist) onde a lista tem pelo menos uma entrada.

O comportamento de tempo limite dessa política pode ser configurado com a política de [NavigationDelayForInitialSiteListDownloadTimeout](#navigationdelayforinitialsitelistdownloadtimeout).

Se você definir essa política como 'All', quando o Microsoft Edge não tiver uma versão em cache do Enterprise Mode Site List, as tabulações adiarão a navegação até que o navegador baixe a lista de sites. Os sites configurados para abrir no modo Internet Explorer pela lista de sites serão carregados no modo Internet Explorer, mesmo durante a navegação inicial do navegador. Os sites que provavelmente não conseguem ser configurados para abrir no Internet Explorer, como em qualquer site com um esquema diferente de http:, https:, arquivo: ou FTP: não atrasam a navegação e a carregam imediatamente no modo Edge.

Se você definir essa política como "Nenhum" ou não a configurar, quando o Microsoft Edge não tiver uma versão em cache do Enterprise Mode Site List, as guias navegarão imediatamente e não aguardarão o navegador baixar o Enterprise Mode Site List. Os sites configurados para abrir no modo Internet Explorer pela lista de sites serão abertos no modo Microsoft Edge até que o navegador termine de baixar a lista de sites do Modo Empresarial.

Mapeamento das opções de política:

* Nenhum (0) = Nenhum

* Todos (1) = Todas as navegações elegíveis

Use as informações anteriores ao configurar essa política.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: não requer a reinicialização do navegador

  #### Tipo de dados:
  - Inteiro

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: DelayNavigationsForInitialSiteListDownload
  - Nome da Política de Grupo: Exigir que a lista de sites no Modo Empresarial esteja disponível antes da navegação na guia
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: DelayNavigationsForInitialSiteListDownload
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  

  [Voltar ao início](#microsoft-edge---policies)

  ### DeleteDataOnMigration
  #### Excluir dados antigos do navegador na migração
  
  
  #### Versões com suporte:
  - No Windows desde 83 ou posterior

  #### Descrição
  Essa política determina se os dados de navegação do usuário na Versão Prévia do Microsoft Edge serão excluídos após a migração para a versão 81 ou posterior do Microsoft Edge.

Se você definir essa política como "habilitada", todos os dados de navegação da Versão Prévia do Microsoft Edge serão excluídos após a migração para o Microsoft Edge versão 81 ou posterior. Essa política deve ser definida antes de migrar para a versão 81 ou posterior do Microsoft Edge, a fim de ter algum efeito sobre os dados de navegação existentes.

Se você definir essa política como "desabilitada" ou se a política não estiver configurada, os dados de navegação do usuário não serão excluídos após a migração para a versão 83 ou posterior do Microsoft Edge.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: não requer a reinicialização do navegador

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: DeleteDataOnMigration
  - Nome da Política de Grupo: Excluir dados antigos do navegador na migração
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: DeleteDataOnMigration
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000000
```


  

  [Voltar ao início](#microsoft-edge---policies)

  ### DeveloperToolsAvailability
  #### Controlar onde as ferramentas de desenvolvedor podem ser usadas
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Controlar onde as ferramentas de desenvolvedor podem ser usadas.

Se você definir essa política como 'DeveloperToolsDisallowedForForceInstalledExtensions' (o padrão), os usuários poderão acessar as ferramentas de desenvolvedor e o console de JavaScript em geral, mas não no contexto de extensões instaladas pela política da sua empresa.

Se você definir essa política como 'DeveloperToolsAllowed', os usuários poderão acessar as ferramentas de desenvolvedor e o console do JavaScript em todos os contextos, incluindo as extensões instaladas pela política da sua empresa.

Se você definir essa política como 'DeveloperToolsDisallowed', os usuários não poderão acessar as ferramentas de desenvolvedor nem verificar elementos do website. Os atalhos de teclado e as entradas de menus ou menus de contexto que abrem as ferramentas de desenvolvedor ou o console do JavaScript estão desabilitados.

Mapeamento das opções de política:

* DeveloperToolsDisallowedForForceInstalledExtensions (0) = Bloquear as ferramentas de desenvolvedor nas extensões instaladas pela política da empresa, permitir em outros contextos

* DeveloperToolsAllowed (1) = Permitir usar as ferramentas de desenvolvedor

* DeveloperToolsDisallowed (2) = Não permitir usar as ferramentas de desenvolvedor

Use as informações anteriores ao configurar essa política.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Inteiro

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: DeveloperToolsAvailability
  - Nome da Política de Grupo: Controlar onde as ferramentas de desenvolvedor podem ser usadas
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: DeveloperToolsAvailability
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000002
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: DeveloperToolsAvailability
  - Valor de exemplo:
``` xml
<integer>2</integer>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### DiagnosticData
  #### Enviar dados de diagnóstico obrigatórios e opcionais referentes ao uso do navegador
  
  
  #### Versões com suporte:
  - No Windows 7 e no macOS, a partir da 86 ou posterior

  #### Descrição
  Essa política controla o envio para a Microsoft de dados de diagnóstico obrigatórios e opcionais referentes ao uso do navegador.

Os dados de diagnóstico obrigatórios são coletados para manter o Microsoft Edge seguro, atualizado e funcionando conforme o esperado.

Os dados de diagnóstico opcionais incluem dados sobre como o navegador é usado, os sites que você visita e relatórios de falha enviados para a Microsoft para aprimorar o produto e os serviços.

Essa política não é suportada nos dispositivos com Windows 10. Para controlar essa coleta de dados no Windows 10, os administradores de TI precisam usar a política de grupo de dados de diagnóstico do Windows. Essa política irá “Permitir a telemetria” ou “Permitir dados de diagnóstico”, dependendo da versão do Windows. Saiba mais sobre a coleta de dados de diagnóstico do Windows 10: [https://go.microsoft.com/fwlink/?linkid=2099569](https://go.microsoft.com/fwlink/?linkid=2099569)

Use uma das seguintes configurações para configurar essa política:

“Off” desativa a coleta de dados de diagnóstico obrigatórios ou opcionais. Essa opção não é recomendada.

“RequiredData” envia os dados de diagnóstico obrigatórios mas desativa a coleta dos dados de diagnóstico opcionais. O Microsoft Edge irá enviar os dados de diagnóstico obrigatórios para manter o Microsoft Edge seguro, atualizado e funcionando conforme o esperado.

“OptionalData” envia os dados de diagnóstico opcionais, que incluem dados sobre como o navegador é usado, os sites que você visita e relatórios de falha enviados para a Microsoft para aprimorar o produto e os serviços.

No Windows 7/macOS, essa política controla o envio para a Microsoft dos dados de diagnóstico obrigatórios e opcionais.

Se você não configurar ou desativar essa política, o Microsoft Edge estabelecerá como padrão a preferência do usuário.

Mapeamento das opções de política:

* Off (0) = Desativada (não recomendado)

* RequiredData (1) = Dados obrigatórios

* OptionalData (2) = Dados opcionais

Use as informações anteriores ao configurar essa política.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: não requer a reinicialização do navegador

  #### Tipo de dados:
  - Inteiro

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome único da Política de Grupo: DiagnosticData
  - Nome da Política de Grupo: Enviar dados de diagnóstico obrigatórios e opcionais referentes ao uso do navegador
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: DiagnosticData
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000002
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: DiagnosticData
  - Valor de exemplo:
``` xml
<integer>2</integer>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### DirectInvokeEnabled
  #### Permitir que os usuários abram arquivos usando o protocolo DirectInvoke
  
  
  #### Versões com suporte:
  - No Windows desde 78 ou posterior

  #### Descrição
  Permitir que os usuários abram arquivos usando o protocolo DirectInvoke. O protocolo DirectInvoke permite que os sites solicitem que o navegador abra arquivos de uma URL específica usando um identificador de arquivo específico no computador ou dispositivo do usuário.

Se você habilitar ou não configurar essa política, os usuários poderão abrir arquivos usando o protocolo DirectInvoke.

Se você desabilitar essa política, os usuários não poderão abrir arquivos usando o protocolo DirectInvoke. Em vez disso, o arquivo será salvo no sistema de arquivos.

Observação: a desabilitação do DirectInvoke pode impedir que determinados recursos do Microsoft Office SharePoint Online funcionem conforme o esperado.

Para obter mais informações sobre DirectInvoke, confira [https://go.microsoft.com/fwlink/?linkid=2103872](https://go.microsoft.com/fwlink/?linkid=2103872) e [https://go.microsoft.com/fwlink/?linkid=2099871](https://go.microsoft.com/fwlink/?linkid=2099871).

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: DirectInvokeEnabled
  - Nome da Política de Grupo: Permitir que os usuários abram arquivos usando o protocolo DirectInvoke
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: DirectInvokeEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000000
```


  

  [Voltar ao início](#microsoft-edge---policies)

  ### Disable3DAPIs
  #### Desabilitar o suporte para APIs de gráficos 3D
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Impedir que páginas da Web acessem a GPU (unidade de processamento gráfico). Especificamente, as páginas da Web não conseguem acessar a API do WebGL e plug-ins não podem usar a API Pepper 3D.

Se você não configurar ou desabilitar essa política, isso potencialmente permite que páginas da web usem a API do WebGL e plug-ins para usar a API Pepper 3D. O Microsoft Edge pode, por padrão, ainda exigir que os argumentos de linha de comando sejam passados para usar essas APIs.

Se a política[HardwareAccelerationModeEnabled](#hardwareaccelerationmodeenabled) estiver definida como falsa, a configuração da política de "Disable3DAPIs" será ignorada. Isso é o equivalente à definição da política de "Disable3DAPIs" como verdadeira.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: Disable3DAPIs
  - Nome da Política de Grupo: Desabilitar o suporte para APIs de gráficos 3D
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: Disable3DAPIs
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000000
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: Disable3DAPIs
  - Valor de exemplo:
``` xml
<false/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### DisableScreenshots
  #### Desabilitar a captura de tela
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Controla se os usuários podem fazer capturas de tela da página do navegador.

Se habilitada, o usuário não poderá fazer capturas de tela usando atalhos de teclado ou APIs de extensão.

Se essa política estiver desabilitada ou não estiver configurada, os usuários poderão fazer capturas de tela.

Observe que essa política controla as capturas de tela obtidas no próprio navegador. Mesmo que você habilite essa política, os usuários ainda poderão fazer capturas de tela usando algum método fora do navegador (como usar um recurso do sistema operacional ou outro aplicativo).

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: DisableScreenshots
  - Nome da Política de Grupo: Desabilitar a captura de tela
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: DisableScreenshots
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: DisableScreenshots
  - Valor de exemplo:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### DiskCacheDir
  #### Definir diretório de cache de disco
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Configurar o diretório a ser usado para armazenar arquivos armazenados em cache.

Se você habilitar essa política, o Microsoft Edge usará o diretório fornecido, independentemente de o usuário ter especificado o sinalizador '--disk-cache-dir' flag. Para evitar a perda de dados ou outros erros inesperados, não configure essa política para uma pasta raiz do volume ou para uma pasta que é usada para outros fins, porque o Microsoft Edge gerencia seu conteúdo.

Confira [https://go.microsoft.com/fwlink/?linkid=2095041](https://go.microsoft.com/fwlink/?linkid=2095041) para obter uma lista de variáveis que você pode usar ao especificar diretórios e caminhos.

Se você não configurar essa política, o diretório de cache padrão será usado, e os usuários poderão substituir esse padrão pelo sinalizador de linha de comando '--disk-cache-dir' 

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: não requer a reinicialização do navegador

  #### Tipo de dados:
  - String

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: DiskCacheDir
  - Nome da Política de Grupo: Definir diretório de cache de disco
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: DiskCacheDir
  - Tipo do valor: REG_SZ
  ##### Valor de exemplo:
```
"${user_home}/Edge_cache"
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: DiskCacheDir
  - Valor de exemplo:
``` xml
<string>${user_home}/Edge_cache</string>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### DiskCacheSize
  #### Definir o tamanho do cache de disco, em bytes
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Configura o tamanho do cache, em bytes, usado para armazenar arquivos no disco.

Se você habilitar essa política, o Microsoft Edge usará o tamanho de cache fornecido, independentemente de o usuário ter especificado o sinalizador '--disk-cache-size'. O valor especificado nesta política não é um limite rígido, mas uma sugestão para o sistema de cache; qualquer valor abaixo de alguns megabytes é muito pequeno e será arredondado para um mínimo razoável.

Se você definir o valor desta política como 0, o tamanho do cache padrão será usado e os usuários não poderão alterá-lo.

Se você não configurar essa política, o tamanho padrão será usado, mas os usuários poderão substituí-los pelo sinalizador  '--disk-cache-size'.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: não requer a reinicialização do navegador

  #### Tipo de dados:
  - Inteiro

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: DiskCacheSize
  - Nome da Política de Grupo: Definir o tamanho do cache de disco, em bytes
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: DiskCacheSize
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x06400000
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: DiskCacheSize
  - Valor de exemplo:
``` xml
<integer>104857600</integer>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### DnsOverHttpsMode
  #### Controlar o modo de DNS em HTTPS
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 83 ou mais recente

  #### Descrição
  Controlar o modo de resolução DNS sobre HTTPS. Observe que essa política só definirá o modo padrão para cada consulta. O modo pode ser substituído para tipos especiais de consultas, como solicitações para resolver um nome de host DNS.

O modo "desativado" desabilitará o DNS em HTTPS.

O modo "automático" enviará primeiro as consultas DNS sobre HTTPS se houver um servidor DNS sobre HTTPS disponível e poderá recorrer ao envio de consultas inseguras por erro.

O modo "seguro" só enviará consultas DNS ao HTTPS e falhará na resolução de erros.

Se você não configurar esta política, o navegador poderá enviar solicitações de DNS sobre HTTPS para um resolvedor associado ao resolvedor de sistema configurado do usuário.

Mapeamento das opções de política:

* desativado (desativado) = Desabilitar o DNS em HTTPS

* automático (automático) = Habilitar o DNS em HTTPS com o fallback não seguro

* automático (automático) = Habilitar o DNS em HTTPS sem o fallback não seguro

Use as informações anteriores ao configurar essa política.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - String

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: DnsOverHttpsMode
  - Nome da Política de Grupo: Controlar o modo de DNS sobre HTTPS.
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: DnsOverHttpsMode
  - Tipo do valor: REG_SZ
  ##### Valor de exemplo:
```
"off"
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: DnsOverHttpsMode
  - Valor de exemplo:
``` xml
<string>off</string>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### DnsOverHttpsTemplates
  #### Especificar o modelo de URI do resolvedor de DNS sobre HTTPS desejado.
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 83 ou mais recente

  #### Descrição
  O modelo de URI do resolvedor de DNS sobre HTTPS desejado. Para especificar vários resolvedores DNS de HTTPS, separe os modelos de URI correspondentes por espaços.

Se você definir [DnsOverHttpsMode](#dnsoverhttpsmode) como "seguro", essa política deverá estar definida e não poderá estar vazia.

Se você definir [DnsOverHttpsMode](#dnsoverhttpsmode) como "automático" e essa política for definida, os modelos de URI especificados serão usados. Se você não definir essa política, os mapeamentos embutidos serão usados para tentar atualizar o resolvedor de DNS atual do usuário para um resolvedor de DoH operado pelo mesmo provedor.

Se o modelo URI contiver uma variável DNS, as solicitações ao resolvedor usarão GET; caso contrário, as solicitações usarão POST.

Os modelos formatados incorretamente serão ignorados.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - String

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: DnsOverHttpsTemplates
  - Nome da Política de Grupo: Especificar o modelo de URI do resolvedor de DNS sobre HTTPS desejado.
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: DnsOverHttpsTemplates
  - Tipo do valor: REG_SZ
  ##### Valor de exemplo:
```
"https://dns.example.net/dns-query{?dns}"
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: DnsOverHttpsTemplates
  - Valor de exemplo:
``` xml
<string>https://dns.example.net/dns-query{?dns}</string>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### DownloadDirectory
  #### Configurar o diretório de download
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Configura o diretório a ser usado para baixar arquivos.

Se você habilitar essa política, o Microsoft Edge usará o diretório fornecido, independentemente de o usuário ter especificado um ou escolhido a solicitação do local de download todas as vezes. Confira [https://go.microsoft.com/fwlink/?linkid=2095041](https://go.microsoft.com/fwlink/?linkid=2095041) para obter uma lista de variáveis que podem ser usadas.

Se você desabilitar ou não configurar essa política, o diretório de download padrão será usado, e o usuário poderá alterá-lo.

Se você definir um caminho inválido, o Microsoft Edge usará o diretório de download padrão do usuário.

Se a pasta especificada pelo caminho não existir, o download disparará um aviso que pergunta ao usuário onde eles querem salvar o download.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: Sim
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - String

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: DownloadDirectory
  - Nome da Política de Grupo: Configurar o diretório de download
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): Administrative Templates/Microsoft Edge - Default Settings (usuários podem substituir)/
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nome do valor: DownloadDirectory
  - Tipo do valor: REG_SZ
  ##### Valor de exemplo:
```
"\n      Linux-based OSes (including Mac): /home/${user_name}/Downloads\n      Windows: C:\\Users\\${user_name}\\Downloads"
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: DownloadDirectory
  - Valor de exemplo:
``` xml
<string>
      Linux-based OSes (including Mac): /home/${user_name}/Downloads
      Windows: C:\Users\${user_name}\Downloads</string>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### DownloadRestrictions
  #### Permitir restrições de download
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Configura o tipo de download que o Microsoft Edge bloqueia completamente, sem permitir que os usuários substituam a decisão de segurança.

Configurar 'BlockDangerousDownloads' para permitir todos os downloads, exceto aqueles que contêm avisos do Microsoft Defender SmartScreen.

Configurar 'BlockPotentiallyDangerousDownloads' para permitir todos os downloads, exceto aqueles com os avisos do Microsoft Defender SmartScreen sobre downloads potencialmente perigosos ou indesejados.

Configurar 'BlockAllDownloads' para bloquear todos os downloads.

Se você não configurar essa política ou definir a opção 'DefaultDownloadSecurity', os downloads passarão pelas restrições de segurança usuais com base nos resultados da análise do Microsoft Defender SmartScreen.

Lembre-se de que essas restrições se aplicam aos downloads de conteúdo de página da Web, bem como nas opções do menu de contexto “baixar link”. Essas restrições não se aplicam ao salvar ou baixar a página atualmente exibida, nem se aplicam à opção Salvar como PDF nas opções de impressão.

Confira [https://go.microsoft.com/fwlink/?linkid=2094934](https://go.microsoft.com/fwlink/?linkid=2094934) para saber mais sobre o Microsoft Defender SmartScreen.

Mapeamento das opções de política:

* DefaultDownloadSecurity (0) = Nenhuma restrição especial

* BlockDangerousDownloads (1) = Bloquear downloads perigosos

* BlockPotentiallyDangerousDownloads (2) = Bloquear downloads potencialmente perigosos ou indesejados

* BlockAllDownloads (3) = Bloquear todos os downloads

Use as informações anteriores ao configurar essa política.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: Sim
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Inteiro

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: DownloadRestrictions
  - Nome da Política de Grupo: Permitir restrições de download
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): Administrative Templates/Microsoft Edge - Default Settings (usuários podem substituir)/
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nome do valor: DownloadRestrictions
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000002
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: DownloadRestrictions
  - Valor de exemplo:
``` xml
<integer>2</integer>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### EdgeCollectionsEnabled
  #### Habilitar o recurso Coleções
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 78 ou mais recente

  #### Descrição
  Permite que os usuários acessem o recurso Coleções, onde eles podem coletar, organizar, compartilhar e exportar conteúdo com mais eficiência e com a integração com o Office.

Se você habilitar ou não configurar essa política, os usuários poderão acessar e usar o recurso coleções no Microsoft Edge.

Se você desabilitar essa política, os usuários não poderão acessar e usar conjuntos no Microsoft Edge.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: não requer a reinicialização do navegador

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: EdgeCollectionsEnabled
  - Nome da Política de Grupo: Habilitar o recurso Coleções
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: EdgeCollectionsEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: EdgeCollectionsEnabled
  - Valor de exemplo:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### EditFavoritesEnabled
  #### Permite que os usuários editem favoritos
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Habilite essa política para permitir que os usuários adicionem, removam e modifiquem favoritos. Esse será o comportamento padrão se você não configurar a política.

Desabilite essa política para impedir que os usuários adicionem, removam ou modifiquem os favoritos. Eles ainda podem usar favoritos existentes.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: EditFavoritesEnabled
  - Nome da Política de Grupo: Permite que os usuários editem favoritos
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: EditFavoritesEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000000
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: EditFavoritesEnabled
  - Valor de exemplo:
``` xml
<false/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### EnableDeprecatedWebPlatformFeatures
  #### Reabilitar os recursos de plataforma da Web reaprovados por um tempo limitado
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Especifique uma lista de recursos de Web Platform substituídos para reabilitar temporariamente.

Essa política permite reabilitar os recursos de plataforma da Web reaprovados por um tempo limitado. Os recursos são identificados por uma marca de cadeia de caracteres.

Se você não configurar essa política, se a lista estiver vazia ou se um recurso não corresponder a uma das marcas de cadeia de caracteres com suporte, todos os recursos de plataforma da web substituídos permanecerão desabilitados.

Enquanto a própria política tem suporte nas plataformas acima, o recurso habilitado pode não estar disponível em todas essas plataformas. Nem todos os recursos substituídos da plataforma da Web podem ser reativados. Somente os usuários explicitamente listados abaixo podem ser habilitados novamente e apenas por um período de tempo limitado, que é diferente por recurso. Você pode revisar o intuito por trás do recurso de plataforma da Web em https://bit.ly/blinkintents.

O formato geral da marca de cadeia de caracteres é [DeprecatedFeatureName] _EffectiveUntil [AAAAMMDD].

Mapeamento das opções de política:

* ExampleDeprecatedFeature (ExampleDeprecatedFeature_EffectiveUntil20080902) = Habilitar a API ExampleDeprecatedFeature durante 2008/09/02

Use as informações anteriores ao configurar essa política.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: EnableDeprecatedWebPlatformFeatures
  - Nome da Política de Grupo: Reabilitar os recursos de plataforma da Web reaprovados por um tempo limitado
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge\EnableDeprecatedWebPlatformFeatures
  - Caminho (recomendado): N/A
  - Nome do valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de exemplo:
```
SOFTWARE\Policies\Microsoft\Edge\EnableDeprecatedWebPlatformFeatures\1 = "ExampleDeprecatedFeature_EffectiveUntil20080902"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: EnableDeprecatedWebPlatformFeatures
  - Valor de exemplo:
``` xml
<array>
  <string>ExampleDeprecatedFeature_EffectiveUntil20080902</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### EnableDomainActionsDownload
  #### Habilitar ações de domínio para download da Microsoft (obsoleta)
  
  >OBSOLETA: Esta política é obsoleta e não funciona após a versão 84 do Microsoft Edge.
  #### Versões com suporte:
  - No Windows e no macOS desde 77 até 84

  #### Descrição
  Essa política não funciona porque o estado conflitante deve ser evitado. Essa política era usada para ativar/desativar o download da lista ações de domínio, mas nem sempre ela atingia o estado desejado. O serviço de experimentação e configuração, que manipula o download, tem sua própria política de grupo para configurar o que será baixado do serviço. Use a política [ExperimentationAndConfigurationServiceControl](#experimentationandconfigurationservicecontrol), em vez dela.

No Microsoft Edge, as ações de domínio representam uma série de recursos de compatibilidade que ajudam o navegador a funcionar corretamente na Web.

A Microsoft mantém uma lista de ações a serem executadas em determinados domínios por motivos de compatibilidade. Por exemplo, o navegador pode substituir a Sequência de agente do usuário em um site se ele estiver quebrado devido à nova Sequência de agente do usuário no Microsoft Edge. Cada uma dessas ações deve ser temporária enquanto a Microsoft tenta resolver o problema com o proprietário do site.

Quando o navegador começar e, em seguida, periodicamente, o navegador entrará em contato com o Serviço de Experimentação e Configuração que contém a lista de ações de compatibilidade mais atualizadas para realizá-las. Essa lista é salva localmente após ser recuperada pela primeira vez, para que as solicitações subsequentes só atualizem a lista se a cópia do servidor for alterada.

Se você habilitar essa política, a lista de ações de domínio continuará a ser baixada do Serviço de Experimentação e Configuração.

Se você desabilitar essa política, a lista de ações de domínio deixará de ser baixada do Serviço de Experimentação e Configuração.

Se você não configurar essa política, a lista de ações de domínio continuará a ser baixada do Serviço de Experimentação e Configuração.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: EnableDomainActionsDownload
  - Nome da GP: Habilitar a Transferência de Ações de Domínio da Microsoft (obsoleta)
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: EnableDomainActionsDownload
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: EnableDomainActionsDownload
  - Valor de exemplo:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### EnableOnlineRevocationChecks
  #### Habilitar verificações OCSP/CRL online
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  As verificações de revogação online não fornecem benefícios consideráveis à segurança e são desabilitadas por padrão.

Se você habilitar essa política, o Microsoft Edge executará verificações online de OCSP/CRL com falha suave. "Falha de software" significa que se não for possível acessar o servidor de revogação, o certificado será considerado válido.

Se você desabilitar a política ou não a configurar, o Microsoft Edge não executará verificações de revogação online.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: EnableOnlineRevocationChecks
  - Nome da Política de Grupo: Habilitar verificações OCSP/CRL online
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: EnableOnlineRevocationChecks
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000000
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: EnableOnlineRevocationChecks
  - Valor de exemplo:
``` xml
<false/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### EnableSha1ForLocalAnchors
  #### Permitir certificados assinados usando SHA-1 quando emitido por âncoras de confiança local (substituídos)
  >SUBSTITUÍDO: Essa política está preterida. Ela tem suporte no momento, mas se tornará obsoleta em uma versão futura.
  
  #### Versões com suporte:
  - No Windows e no macOS desde 85 ou mais recente

  #### Descrição
  Quando essa configuração estiver habilitada, o Microsoft Edge permitirá conexões protegidas por certificados com a SHA-1, desde que as cadeias de certificados sejam vinculadas localmente e válidas.

Observe que essa política depende da pilha de verificação de certificado do sistema operacional (SO), permitindo assinaturas SHA-1. Se a atualização do sistema operacional alterar o gerenciamento do sistema operacional de certificados SHA-1, talvez essa política não tenha mais efeito.  Além disso, esta política destina-se a uma solução alternativa e temporária para dar mais tempo para que as empresas deixem de usar o SHA-1. Essa política será removida no Microsoft Edge 92 a ser lançado no meio de 2021.

Se você não definir essa política ou defini-la como falsa, ou se o certificado SHA-1 se vincula a uma raiz de certificado confiável publicamente, o Microsoft Edge não permitirá certificados assinados por SHA-1.

Essa política está disponível apenas nas instâncias do Windows que fazem parte de um domínio do Microsoft Active Directory, em instâncias do Windows 10 Pro ou Enterprise que estejam inscritas no gerenciamento de dispositivos ou em instâncias do macOS que são gerenciadas por meio do MDM ou passaram a fazer parte de um domínio por meio de MCX.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: EnableSha1ForLocalAnchors
  - Nome da GP: Permitir certificados assinados usando SHA-1 quando emitido por âncoras de confiança local (substituídos)
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do Valor: EnableSha1ForLocalAnchors
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000000
```


  #### Informações e configurações do Mac
  - Nome da Chave de Preferência: EnableSha1ForLocalAnchors
  - Valor de exemplo:
``` xml
<false/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### EnterpriseHardwarePlatformAPIEnabled
  #### Permitir que as extensões gerenciadas usem a API de plataforma de hardware empresarial
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 78 ou mais recente

  #### Descrição
  Quando essa política está definida como habilitada, as extensões instaladas pela política empresarial têm permissão para usar a API de plataforma de hardware empresarial.
Quando essa política estiver definida como desabilitada ou não for definida, não será permitida nenhuma extensão para usar a API de plataforma de hardware empresarial.
Essa política também se aplica a extensões de componente.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: EnterpriseHardwarePlatformAPIEnabled
  - Nome da Política de Grupo: Permitir que as extensões gerenciadas usem a API de plataforma de hardware empresarial
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: EnterpriseHardwarePlatformAPIEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: EnterpriseHardwarePlatformAPIEnabled
  - Valor de exemplo:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### EnterpriseModeSiteListManagerAllowed
  #### Permitir o acesso à ferramenta Enterprise Mode Site List Manager
  
  
  #### Versões com suporte:
  - No Windows desde 86 ou posterior

  #### Descrição
  Permite definir se o Enterprise Mode Site List Manager está disponível para os usuários.

Se você habilitar essa política, os usuários poderão ver o botão de navegação Enterprise Mode Site List Manager na página edge://compat, navegar até a ferramenta e usá-la.

Se você desabilitar ou não configurar essa política, os usuários não verão o botão de navegação Enterprise Mode Site List Manager e não poderão usá-los.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: EnterpriseModeSiteListManagerAllowed
  - Nome da GP: Permitir o acesso à ferramenta Enterprise Mode Site List Manager
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do Valor: EnterpriseModeSiteListManagerAllowed
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000000
```


  

  [Voltar ao início](#microsoft-edge---policies)

  ### ExemptDomainFileTypePairsFromFileTypeDownloadWarnings
  #### Desabilitar o download de avisos com base na extensão de tipo de arquivo para tipos de arquivo especificados em domínios
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 85 ou mais recente

  #### Descrição
  Você pode habilitar essa política para criar um dicionário de extensões de tipo de arquivo com uma lista de domínios correspondente que será isenta de avisos de download baseados na extensão de tipo de arquivo. Isso permite aos administradores corporativos bloquear os avisos de download baseados na extensão do tipo de arquivo de arquivos associados à um domínio listado. Por exemplo, se a extensão "jnlp" estiver associada a "website1.com", os usuários não verão um aviso ao baixar arquivos "jnlp" do "website1.com", mas verão um aviso de download durante o download dos arquivos "jnlp" de "website2.com".

Os arquivos com extensões de tipo de arquivo especificadas para domínios identificados por essa política ainda estarão sujeitos aos avisos de segurança com base na extensão de tipo não-arquivo, como avisos de download de conteúdo misto e avisos do Microsoft Defender SmartScreen.

Se você desabilitar essa política ou não a configurar, os tipos de arquivo que acionam os avisos de download baseados na extensão mostrarão avisos para o usuário.

Se você habilitar essa política:

* O padrão de URL deve ser formatado de acordo com [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).
* A extensão do tipo de arquivo inserida deve estar em ASCII de letras minúsculas. O separador à esquerda não deve ser incluído ao listar o tipo de extensão do arquivo, então liste "txt", em vez de ".txt".

Exemplo:

O valor do exemplo a seguir impediria os avisos de download baseados na extensão do tipo de arquivo em extensões SWF, exe e jnlp para domínios *.contoso.com. Ele mostrará ao usuário um aviso de download baseado na extensão de tipo de arquivo em qualquer outro domínio para arquivos exe e jnlp, mas não para arquivos SWF.

[ { "file_extension": "jnlp", "domains": ["contoso.com"] }, { "file_extension": "exe", "domains": ["contoso.com"] }, { "file_extension": "swf", "domains": ["*"] } ]

Observe que, enquanto o exemplo anterior mostra a supressão de avisos de download com base na extensão do tipo de arquivo para todos os domínios, não é recomendável aplicar a supressão de tais avisos para todos os domínios para qualquer extensão perigosa do tipo de arquivo devido a problemas de segurança. Ele é mostrado no exemplo apenas para demonstrar a capacidade de fazê-lo.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: ExemptDomainFileTypePairsFromFileTypeDownloadWarnings
  - Nome da Política de Grupo: Desabilitar o download de avisos com base na extensão do tipo de arquivo para tipos de arquivo especificados em domínios
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge\ExemptDomainFileTypePairsFromFileTypeDownloadWarnings
  - Caminho (recomendado): N/A
  - Nome do valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de exemplo:
```
SOFTWARE\Policies\Microsoft\Edge\ExemptDomainFileTypePairsFromFileTypeDownloadWarnings\1 = {"domains": ["https://contoso.com", "contoso2.com"], "file_extension": "jnlp"}
SOFTWARE\Policies\Microsoft\Edge\ExemptDomainFileTypePairsFromFileTypeDownloadWarnings\2 = {"domains": ["*"], "file_extension": "swf"}

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ExemptDomainFileTypePairsFromFileTypeDownloadWarnings
  - Valor de exemplo:
``` xml
<array>
  <string>{'domains': ['https://contoso.com', 'contoso2.com'], 'file_extension': 'jnlp'}</string>
  <string>{'domains': ['*'], 'file_extension': 'swf'}</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### ExperimentationAndConfigurationServiceControl
  #### Controlar a comunicação com o serviço de experimentação e configuração
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  No Microsoft Edge, o Serviço Experimentação e Configuração é usado para implantar o conteúdo de experimentação e configuração.

O conteúdo de experimentação consiste em uma lista dos recursos em desenvolvimento inicial que a Microsoft está disponibilizando para testes e comentários.

O conteúdo de configuração consiste em uma lista de configurações que a Microsoft deseja implantar no Microsoft Edge para otimizar a experiência do usuário. Por exemplo, o conteúdo de configuração pode especificar a frequência com que o Microsoft Edge envia solicitações para o serviço de experimentação e configuração para recuperar o conteúdo mais recente.

Além disso, o conteúdo de configuração também pode conter uma lista de ações a serem executadas em determinados domínios por motivos de compatibilidade. Por exemplo, o navegador pode substituir a Sequência de agente do usuário em um site se ele estiver quebrado devido à nova Sequência de agente do usuário no Microsoft Edge. Cada uma dessas ações deve ser temporária enquanto a Microsoft tenta resolver o problema com o proprietário do site.

Se você definir essa política como o modo 'FullMode', o conteúdo total será baixado do Serviço de Experimentação e Configuração. Isso inclui os conteúdos de experimentação e configuração.

Se você definir essa política como 'ConfigurationsOnlyMode', somente o conteúdo de configuração será entregue.

Se você definir essa política como 'RestrictedMode', a comunicação com o Serviço de Experimentação e Configuração será interrompida completamente.

Se você não configurar essa política, em um dispositivo gerenciado em canais estáveis e beta, o comportamento será o mesmo do 'ConfigurationsOnlyMode'.

Se você não configurar essa política, em um dispositivo não gerenciado o comportamento será o mesmo que o 'FullMode'.

Mapeamento das opções de política:

* FullMode (2) = Recuperar configurações e experiências

* ConfigurationsOnlyMode (1) = Recuperar apenas configurações

* RestrictedMode (0) = Desabilitar a comunicação com o Serviço de Experimentação e Configuração

Use as informações anteriores ao configurar essa política.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Inteiro

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: ExperimentationAndConfigurationServiceControl
  - Nome da Política de Grupo: Controlar a comunicação com o serviço de experimentação e configuração
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: ExperimentationAndConfigurationServiceControl
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000002
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ExperimentationAndConfigurationServiceControl
  - Valor de exemplo:
``` xml
<integer>2</integer>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### ExternalProtocolDialogShowAlwaysOpenCheckbox
  #### Mostrar a caixa de seleção "sempre aberta" no diálogo de protocolo externo
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 79 ou mais recente

  #### Descrição
  Essa política controla se a caixa de seleção "Sempre permitir que este site abra links deste tipo" será mostrada em solicitações de inicialização do protocolo externo. Esta política só se aplica a links https://.

Se você definir essa política, quando uma solicitação de confirmação de protocolo externo for exibida, o usuário poderá selecionar "sempre permitir" para ignorar todos os avisos de confirmação futuros do protocolo neste site.

Se você definir essa política, a caixa de seleção "Sempre permitir" não será exibida. O usuário será solicitado a fornecer uma confirmação sempre que um protocolo externo for chamado.

Antes do Microsoft Edge 83, se você não configurar esta política, a caixa de seleção "Sempre permitir" não será exibida. O usuário será solicitado a fornecer uma confirmação sempre que um protocolo externo for chamado.

Se você não configurar essa política no Microsoft Edge 83, a visibilidade da caixa de seleção será controlada pelo sinalizador "Ativar lembrando preferências de solicitação de inicialização do protocolo" em edge://flags

No Microsoft Edge 84, se você não configurar essa política quando um prompt de confirmação de protocolo externo for exibido, o usuário poderá selecionar "Permitir sempre" para pular todas as futuras solicitações de confirmação do protocolo neste site.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: não requer a reinicialização do navegador

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: ExternalProtocolDialogShowAlwaysOpenCheckbox
  - Nome da Política de Grupo: Mostrar a caixa de seleção "sempre aberta" no diálogo de protocolo externo
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: ExternalProtocolDialogShowAlwaysOpenCheckbox
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ExternalProtocolDialogShowAlwaysOpenCheckbox
  - Valor de exemplo:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### FamilySafetySettingsEnabled
  #### Permitir que os usuários configurem a proteção para a família
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 83 ou mais recente

  #### Descrição
  Essa política desabilita e oculta completamente a página de Proteção para a família nas Configurações. A navegação para edge://settings/familysafety também será bloqueada. A página de proteção para a família descreve quais recursos estão disponíveis para grupos da família e como ingressar em um grupo da família. Saiba mais sobre a proteção para a família aqui: ([https://go.microsoft.com/fwlink/?linkid=2098432](https://go.microsoft.com/fwlink/?linkid=2098432)).

Se você habilitar essa política ou não a configurar, a página de segurança da família será exibida.

Se você desabilitar essa política, a página de segurança da família não será exibida.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: FamilySafetySettingsEnabled
  - Nome da Política de Grupo: Permitir que os usuários configurem a proteção para a família
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: FamilySafetySettingsEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: FamilySafetySettingsEnabled
  - Valor de exemplo:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### FavoritesBarEnabled
  #### Habilitar barra de favoritos
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Ativa ou desativa a barra Favoritos.

Se você habilitar essa política, os usuários verão a barra Favoritos.

Se você desabilitar essa política, os usuários não verão a barra Favoritos.

Se essa política não estiver configurada, o usuário poderá decidir se quer ou não usar a barra Favoritos.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: Sim
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: FavoritesBarEnabled
  - Nome da Política de Grupo: Habilitar barra de favoritos
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): Administrative Templates/Microsoft Edge - Default Settings (usuários podem substituir)/
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nome do valor: FavoritesBarEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: FavoritesBarEnabled
  - Valor de exemplo:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### ForceBingSafeSearch
  #### Aplicar a Pesquisa Segura do Bing
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Verifique se as consultas na pesquisa na web do Bing são feitas com a Pesquisa Segura definida com o valor especificado. Os usuários não poderão alterar essa configuração.

Se você configurar essa política como 'BingSafeSearchNoRestrictionsMode', a Pesquisa Segura na pesquisa do Bing voltará para o valor bing.com.

Se você configurar essa política para 'BingSafeSearchModerateMode', a configuração moderada será usada na Pesquisa Segura. A configuração moderada filtra vídeos e imagens para adultos, mas não texto dos resultados da pesquisa.

Se você configurar essa política para 'BingSafeSearchStrictMode', será usada a configuração estrita na Pesquisa Segura. A configuração estrita filtra textos, imagens e vídeos para adultos.

Se você desabilitar essa política ou não a configurar, a pesquisa no Bing não será imposta, e os usuários poderão definir o valor desejado na bing.com.

Mapeamento das opções de política:

* BingSafeSearchNoRestrictionsMode (0) = Não configura restrições de pesquisa no Bing

* BingSafeSearchModerateMode (1) = Configure restrições de pesquisa moderada no Bing

* BingSafeSearchStrictMode (2) = Configure restrições de pesquisa estritas no Bing

Use as informações anteriores ao configurar essa política.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Inteiro

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: ForceBingSafeSearch
  - Nome da Política de Grupo: Aplicar a Pesquisa Segura do Bing
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: ForceBingSafeSearch
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000000
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ForceBingSafeSearch
  - Valor de exemplo:
``` xml
<integer>0</integer>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### ForceCertificatePromptsOnMultipleMatches
  #### Configurar se o Microsoft Edge deve selecionar automaticamente um certificado quando houver várias correspondências de certificado para um site configurado com "AutoSelectCertificateForUrls"
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 81 ou mais recente

  #### Descrição
  Alterna se os usuários são solicitados a selecionar um certificado se houver vários certificados disponíveis e se um site estiver configurado com [AutoSelectCertificateForUrls](#autoselectcertificateforurls). Se você não configurar [AutoSelectCertificateForUrls](#autoselectcertificateforurls) para um site, o usuário será sempre instruído a selecionar um certificado.

Se você definir essa política como verdadeira, o Microsoft Edge solicitará que um usuário selecione um certificado para sites na lista definido em [AutoSelectCertificateForUrls](#autoselectcertificateforurls) apenas se houver mais de um certificado.

Se você definir essa política como falsa ou não a configurar, o Microsoft Edge selecionará automaticamente um certificado mesmo se houver várias correspondências para um certificado. O usuário não será instruído a selecionar um certificado para sites na lista definida em [AutoSelectCertificateForUrls](#autoselectcertificateforurls).

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: não requer a reinicialização do navegador

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: ForceCertificatePromptsOnMultipleMatches
  - Nome da Política de Grupo: Configurar se o Microsoft Edge deve selecionar automaticamente um certificado quando houver várias correspondências de certificado para um site configurado com "AutoSelectCertificateForUrls"
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: ForceCertificatePromptsOnMultipleMatches
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ForceCertificatePromptsOnMultipleMatches
  - Valor de exemplo:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### ForceEphemeralProfiles
  #### Habilitar o uso de perfis efêmeros
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Controla se os perfis de usuário são alternados para o modo efêmero. Um perfil efêmero é criado quando uma sessão começa, é excluído quando a sessão termina e é associado ao perfil original do usuário.

Se você habilitar essa política, os perfis serão executados no modo efêmero. Isso permite que os usuários trabalhem em seus próprios dispositivos sem salvar os dados da navegação nesses dispositivos. Se você habilitar essa política como uma política do sistema operacional (por exemplo, usando o GPO no Windows), ela será aplicada a todos os perfis do sistema.

Se você desabilitar essa política ou não a configurar, os usuários terão seus perfis regulares quando entrarem no navegador.

No modo efêmero, os dados de perfil são salvos em disco apenas quanto ao comprimento da sessão do usuário. Os recursos, como histórico do navegador, extensões e seus dados, dados da web como cookies e bancos de dados da web, não são salvos após o navegador ser fechado. Isso não impede que o usuário baixe manualmente os dados para o disco, ou salve ou imprima páginas. Se o usuário tiver habilitado a sincronização, todos os dados serão preservados em suas contas de sincronização, exatamente como os perfis comuns. Os usuários também podem usar a navegação InPrivate no modo efêmero, a menos que você desabilite explicitamente isso.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: não requer a reinicialização do navegador

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: ForceEphemeralProfiles
  - Nome da Política de Grupo: Habilitar o uso de perfis efêmeros
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: ForceEphemeralProfiles
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ForceEphemeralProfiles
  - Valor de exemplo:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### ForceGoogleSafeSearch
  #### Aplicar a Pesquisa Segura do Google
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Força as consultas na pesquisa Web do Google a serem realizadas com a Pesquisa Segura e impede que os usuários alterem essa configuração.

Se você habilitar essa política, a Pesquisa Segura na Pesquisa do Google estará sempre ativa.

Se você desabilitar essa política ou não a configurar, a Pesquisa Segura na Pesquisa do Google não será forçada.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: ForceGoogleSafeSearch
  - Nome da Política de Grupo: Aplicar a Pesquisa Segura do Google
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: ForceGoogleSafeSearch
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000000
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ForceGoogleSafeSearch
  - Valor de exemplo:
``` xml
<false/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### ForceLegacyDefaultReferrerPolicy
  #### Usa uma política referencial padrão de no-referrer-when-downgrade (preterida)
  >SUBSTITUÍDO: Essa política está preterida. Ela tem suporte no momento, mas se tornará obsoleta em uma versão futura.
  
  #### Versões com suporte:
  - No Windows e no macOS desde 81 ou mais recente

  #### Descrição
  Essa política foi preterida porque destina-se a ser um mecanismo de curto prazo para dar mais tempo para que as empresas atualizem o conteúdo da Web se e quando ela for incompatível com a política referencial padrão atual. Ela não funcionará no Microsoft Edge versão 88.

A política referencial padrão do Microsoft Edge está sendo reforçada de seu valor atual de não-referencial-quando-faz o downgrade para origem-estrita-quando-origem-cruzada que é mais segura, através de uma implantação gradual.

Antes da implantação, essa política empresarial não terá efeito. Após a distribuição, quando essa política empresarial estiver habilitada, a política referencial padrão do Microsoft Edge será definida como seu valor antigo de não-referencial-quando-downgrade.

Esta política corporativa está desabilitada por padrão.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: ForceLegacyDefaultReferrerPolicy
  - Nome da Política de Grupo: Usa uma política referencial padrão de no-referrer-when-downgrade (preterida)
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: ForceLegacyDefaultReferrerPolicy
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000000
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ForceLegacyDefaultReferrerPolicy
  - Valor de exemplo:
``` xml
<false/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### ForceNetworkInProcess
  #### Forçar o código de rede a executar no processo do navegador (obsoleta)
  
  >OBSOLETA: Esta política é obsoleta e não funciona após a versão 83 do Microsoft Edge.
  #### Versões com suporte:
  - No Windows desde 78 até 83

  #### Descrição
  Essa política não funciona porque destinava-se a ser um mecanismo de curto prazo para dar mais tempo para migrar para o software de terceiros que não dependa das APIs de rede. Os servidores proxy são recomendados em relação aos LSPs e ao patch da API Win32.

Essa política força o código de rede a ser executado no processo do navegador.

Essa política está desabilitada por padrão. Se habilitada, os usuários poderão ter problemas de segurança quando o processo de rede estiver na área restrita.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: não requer a reinicialização do navegador

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: ForceNetworkInProcess
  - Nome da Política de Grupo: Forçar o código de rede a executar no processo do navegador (obsoleta)
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: ForceNetworkInProcess
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000000
```


  

  [Voltar ao início](#microsoft-edge---policies)

  ### ForceSync
  #### Forçar a sincronização dos dados do navegador e não mostrar o aviso de consentimento da sincronização
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 86 ou mais recente

  #### Descrição
  Força a sincronização de dados no Microsoft Edge. Essa política também impede que o usuário desative a sincronização.

Se você não configurar essa política, os usuários poderão ativar ou desativar a sincronização. Se você habilitar essa política, os usuários não poderão desativar a sincronização.

Para que essa política funcione conforme o esperado, a política [BrowserSignin](#browsersignin) não deve ser configurada, ou deve ser definida como habilitada. Se [BrowserSignin](#browsersignin) estiver definida como desabilitada, [ForceSync](#forcesync) não terá efeito.

[SyncDisabled](#syncdisabled) não deve ser configurada ou deve ser definida como false. Se ela estiver definida como true, [ForceSync](#forcesync) não terá efeito.

0 = não inicia automaticamente a sincronização e mostra o consentimento da sincronização (padrão) 
1 = forçar a sincronização para o Azure AD/Azure AD- no perfil degradado de usuário e não mostrar a solicitação de consentimento da sincronização

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: ForceSync
  - Nome da Política de Grupo: forçar a sincronização dos dados do navegador e não mostrar o aviso de consentimento da sincronização
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome de Valor: ForceSync
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ForceSync
  - Valor de exemplo:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### ForceYouTubeRestrict
  #### Forçar o modo restrito mínimo do YouTube
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Impõe um modo restrito mínimo no YouTube e impede que os usuários escolham um modo menos restrito.

Definir como 'Strict' para reforçar o modo Restrito Estrito no YouTube.

Definir como 'Moderado' para forçar o usuário a usar o modo de Restrição Moderada e o Modo Restrito Estrito no YouTube. Eles não podem desabilitar o modo restrito.

Definir como "Desativado" ou não configurar essa política para não impor o Modo Restrito no YouTube. As políticas externas, como políticas do YouTube, ainda poderão impor o modo restrito.

Mapeamento das opções de política:

* Desativado (0) = Não impor o Modo Restrito no YouTube

* Moderado (1) = Forçar pelo menos o Modo Restrito Moderado no YouTube

* Estrito (2) = Impor o Modo Restrito Estrito ao YouTube

Use as informações anteriores ao configurar essa política.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Inteiro

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: ForceYouTubeRestrict
  - Nome da Política de Grupo: Forçar o modo restrito mínimo do YouTube
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: ForceYouTubeRestrict
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000000
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ForceYouTubeRestrict
  - Valor de exemplo:
``` xml
<integer>0</integer>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### FullscreenAllowed
  #### Permitir o modo de tela inteira
  
  
  #### Versões com suporte:
  - No Windows desde 77 ou posterior

  #### Descrição
  Definir a disponibilidade do modo de tela inteira- todas as interfaces de usuário do Microsoft Edge estão ocultas e somente o conteúdo da Web fica visível.

Se você habilitar essa política ou não a configurar, o usuário, os aplicativos e as extensões com permissões apropriadas poderão entrar no modo de tela inteira.

Se você desabilitar essa política, os usuários, os aplicativos e as extensões não poderão entrar no modo de tela inteira.

Abrir o Microsoft Edge no modo de quiosque usando a linha de comando ficará indisponível quando o modo de tela inteira estiver desabilitado.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: FullscreenAllowed
  - Nome da Política de Grupo: Permitir o modo de tela inteira
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: FullscreenAllowed
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  

  [Voltar ao início](#microsoft-edge---policies)

  ### GloballyScopeHTTPAuthCacheEnabled
  #### Habilitar o cache de autenticação HTTP globalmente em escopo
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 81 ou mais recente

  #### Descrição
  Essa política configura um único cache global por perfil com credenciais de autenticação de servidor HTTP.

Se você desabilitar ou não definir essa política, o navegador usará o comportamento padrão de autenticação entre sites, que na versão 80, será o escopo das credenciais de autenticação do servidor HTTP por site de nível superior. Portanto, se dois sites usam recursos do mesmo domínio de autenticação, será necessário fornecer credenciais de maneira independente no contexto de ambos os sites. As credenciais de proxy armazenadas em cache serão reutilizadas nos sites.

Se você habilitar essa política, as credenciais de autenticação HTTP inseridas no contexto de um site serão usadas automaticamente no contexto de outro site.

Habilitar essa política deixa os sites abertos para alguns tipos de ataques entre sites e permite que os usuários sejam rastreados entre sites, mesmo sem cookies, adicionando entradas ao cache de autenticação HTTP usando credenciais inseridas em URLs.

Esta política destina-se a fornecer às empresas, dependendo do comportamento herdado, a possibilidade de atualizar seus procedimentos de logon e será removida no futuro.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: GloballyScopeHTTPAuthCacheEnabled
  - Nome da Política de Grupo: Habilitar o cache de autenticação HTTP globalmente em escopo
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: GloballyScopeHTTPAuthCacheEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000000
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: GloballyScopeHTTPAuthCacheEnabled
  - Valor de exemplo:
``` xml
<false/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### GoToIntranetSiteForSingleWordEntryInAddressBar
  #### Forçar a navegação direta no site da intranet, em vez de pesquisar em entradas de palavras únicas na barra de endereços
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 78 ou mais recente

  #### Descrição
  Se você habilitar essa política, o resultado da melhor sugestão automática na lista de sugestões da barra de endereços navegará até os sites da intranet se o texto inserido na barra de endereços for uma única palavra sem pontuação.

A navegação padrão durante a digitação de uma única palavra sem pontuação fará a navegação em um site de intranet que corresponda ao texto digitado.

Se você habilitar essa política, o segundo resultado de sugestão automática na lista de sugestões da barra de endereço realizará uma pesquisa na web exatamente como foi inserida, desde que esse texto seja uma única palavra sem pontuação. O provedor de pesquisa padrão será usado, a menos que uma política para evitar a pesquisa na Web também esteja habilitada.

Os dois efeitos para habilitar essa política são:

A navegação para sites em resposta a consultas únicas do Word que normalmente seria resolvidas para um item do histórico não ocorrerá mais. Em vez disso, o navegador tentará navegar até os sites internos que podem não existir na intranet de uma organização. Isso resultará em um erro 404.

Termos de pesquisa populares de uma única palavra exigirão a seleção manual de sugestões de pesquisa para realizar uma pesquisa adequadamente.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: GoToIntranetSiteForSingleWordEntryInAddressBar
  - Nome da Política de Grupo: Forçar a navegação direta no site da intranet, em vez de pesquisar em entradas de palavras únicas na barra de endereços
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: GoToIntranetSiteForSingleWordEntryInAddressBar
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000000
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: GoToIntranetSiteForSingleWordEntryInAddressBar
  - Valor de exemplo:
``` xml
<false/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### HSTSPolicyBypassList
  #### Configurar a lista de nomes que ignorarão a verificação de política HSTS
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 79 ou mais recente

  #### Descrição
  Os nomes de host especificados nesta lista serão isentos da verificação de política HSTS que podem, potencialmente, atualizar solicitações de "http://" para "https://". Somente os nomes de host de rótulo único são permitidos nesta política. Os nomes de host devem ser canônicos. Todos os IDNs devem ser convertidos no formato de uma etiqueta A, e todas as letras ASCII devem estar em letras minúsculas. Essa política se aplica somente aos nomes de host específicos especificados. Isso não se aplica a subdomínios dos nomes da lista.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: não requer a reinicialização do navegador

  #### Tipo de dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: HSTSPolicyBypassList
  - Nome da Política de Grupo: Configurar a lista de nomes que ignorarão a verificação de política HSTS
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge\HSTSPolicyBypassList
  - Caminho (recomendado): N/A
  - Nome do valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de exemplo:
```
SOFTWARE\Policies\Microsoft\Edge\HSTSPolicyBypassList\1 = "meet"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: HSTSPolicyBypassList
  - Valor de exemplo:
``` xml
<array>
  <string>meet</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### HardwareAccelerationModeEnabled
  #### Usar a aceleração de hardware quando disponível
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Especifique para usar a aceleração de hardware, caso ela esteja disponível. Se você habilitar essa política ou não a configurar, a aceleração de hardware será habilitada, a menos que um recurso GPU seja explicitamente bloqueado.

Se você desabilitar essa política, a aceleração de hardware será desabilitada.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: não requer a reinicialização do navegador

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: HardwareAccelerationModeEnabled
  - Nome da Política de Grupo: Usar a aceleração de hardware quando disponível
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: HardwareAccelerationModeEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: HardwareAccelerationModeEnabled
  - Valor de exemplo:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### HideFirstRunExperience
  #### Oculta a experiência de Primeira execução e a tela inicial.
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 80 ou mais recente

  #### Descrição
  Se você habilitar essa política, a experiência de primeira execução e a tela inicial não serão mostradas aos usuários quando eles executarem o Microsoft Edge pela primeira vez.

Para as opções de configuração exibidas na primeira experiência de execução, o navegador usará como padrão o seguinte:

- Na página nova guia, o tipo de feed será definido como novidades do MSN e o layout como Inspirado.

- O usuário ainda será automaticamente conectado ao Microsoft Edge se a conta do Windows for do tipo Azure AD ou MSA.

-A sincronização não será habilitada por padrão, e os usuários serão instruídos a escolher se deseja sincronizar na inicialização do navegador. Você pode usar as[](#forcesync)ForceSync[ ou a política [SyncDisabled](#syncdisabled) para configurar a sincronização e o aviso de consentimento de sincronização.](#forcesync)

Se você desabilitar ou não configurar essa política, a primeira experiência de execução e a tela inicial Splash serão exibidas.

Observação: as opções de configuração específicas exibidas para o usuário na primeira experiência de execução também podem ser gerenciadas usando outras políticas específicas. Você pode usar a política HideFirstRunExperience em conjunto com essas políticas para configurar uma experiência específica de navegador em seus dispositivos gerenciados. Algumas dessas outras políticas são:

-[AutoImportAtFirstRun](#autoimportatfirstrun)

-[NewTabPageLocation](#newtabpagelocation)

-[NewTabPageSetFeedType](#newtabpagesetfeedtype)

-[ForceSync](#forcesync)

-[SyncDisabled](#syncdisabled)

-[BrowserSignin](#browsersignin)

-[NonRemovableProfileEnabled](#nonremovableprofileenabled)

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: não requer a reinicialização do navegador

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: HideFirstRunExperience
  - Nome da Política de Grupo: Oculta a experiência de Primeira execução e a tela inicial.
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: HideFirstRunExperience
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: HideFirstRunExperience
  - Valor de exemplo:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### ImportAutofillFormData
  #### Permitir a importação de dados do formulário de Preenchimento automático
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Permite que os usuários importem formulários de autoPreenchimento de outro navegador para o Microsoft Edge.

Se você habilitar essa política, a opção importar dados de Autopreenchimento manualmente será selecionada automaticamente.

Se você desabilitar essa política, os dados de formulário de Autopreenchimento não serão importados na primeira execução e os usuários não poderão importá-los manualmente.

Se você não configurar essa política, os dados de Autopreenchimento serão importados na primeira execução e os usuários poderão optar por importar esses dados manualmente durante as sessões de navegação posteriores.

Você pode definir essa política como uma recomendação. Isso significa que o Microsoft Edge importará os dados de Autopreenchimento na primeira execução, mas os usuários poderão marcar ou desmarcar os **dados de Autopreenchimento** na opção de importação manual.

**Observação**: essa política atualmente gerencia a importação do Google Chrome (no Windows 7, 8 e 10 e no macOS) e nos navegadores Mozilla Firefox (no Windows 7, 8 e 10 e no macOS).

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: Sim
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: ImportAutofillFormData
  - Nome da Política de Grupo: Permitir a importação de dados do formulário de Preenchimento automático
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): Administrative Templates/Microsoft Edge - Default Settings (usuários podem substituir)/
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nome do valor: ImportAutofillFormData
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ImportAutofillFormData
  - Valor de exemplo:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### ImportBrowserSettings
  #### Permitir a importação de configurações do navegador
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 78 ou mais recente

  #### Descrição
  Permite que os usuários importem configurações do navegador de outro navegador para o Microsoft Edge.

Se você habilitar essa política, a caixa de seleção **Configurações do navegador** será marcada automaticamente na caixa de diálogo **Importar dados do navegador**.

Se você desabilitar essa política, as configurações do navegador não serão importadas na primeira execução e os usuários não poderão importá-las manualmente.

Se você não configurar essa política, as configurações do navegador serão importadas na primeira execução e os usuários poderão optar por importá-las manualmente durante as sessões de navegação posteriores.

Você também pode definir essa política como uma recomendação. Isso significa que o Microsoft Edge importa as configurações na primeira execução, mas os usuários podem marcar ou desmarcar as **configurações de navegador** na importação manual.

**Observação**: essa política atualmente gerencia a importação do Google Chrome (no Windows 7, 8 e 10 e no macOS).

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: Sim
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: ImportBrowserSettings
  - Nome da Política de Grupo: Permitir a importação de configurações do navegador
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): Administrative Templates/Microsoft Edge - Default Settings (usuários podem substituir)/
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nome do valor: ImportBrowserSettings
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ImportBrowserSettings
  - Valor de exemplo:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### ImportCookies
  #### Permitir a importação de cookies
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 81 ou mais recente

  #### Descrição
  Permite que os usuários importem cookies de outro navegador para o Microsoft Edge.

Se você desabilitar essa política, os cookies não serão importados na primeira execução.

Se você não configurar essa política, os cookies serão importados na primeira execução.

Você também pode definir essa política como uma recomendação. Isso significa que o Microsoft Edge importa cookies na primeira execução.

**Observação**: essa política atualmente gerencia a importação do Google Chrome (no Windows 7, 8 e 10 e no macOS).

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: Sim
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: ImportCookies
  - Nome da Política de Grupo: permitir a importação de cookies
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): Administrative Templates/Microsoft Edge - Default Settings (usuários podem substituir)/
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nome do valor: ImportCookies
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ImportCookies
  - Valor de exemplo:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### ImportExtensions
  #### Permitir a importação de extensões
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 81 ou mais recente

  #### Descrição
  Permite que os usuários importem extensões de outro navegador para o Microsoft Edge.

Se você habilitar essa política, a caixa de seleção **Extensões** será marcada automaticamente na caixa de diálogo **Importar dados do navegador**.

Se você desabilitar essa política, as extensões não serão importadas na primeira execução e os usuários não poderão importá-las manualmente.

Se você não configurar essa política, as extensões serão importadas na primeira execução e os usuários poderão optar por importá-las manualmente durante as sessões de navegação posteriores.

Você também pode definir essa política como uma recomendação. Isso significa que o Microsoft Edge importa extensões na primeira execução, mas os usuários podem marcar ou desmarcar a opção **favoritos** durante a importação manual.

**Observação**: essa política atualmente oferece suporte à importação do Google Chrome (no Windows 7, 8 e 10 e no macOS).

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: Sim
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: ImportExtensions
  - Nome da Política de Grupo: Permitir a importação de extensões
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): Administrative Templates/Microsoft Edge - Default Settings (usuários podem substituir)/
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nome do valor: ImportExtensions
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ImportExtensions
  - Valor de exemplo:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### ImportFavorites
  #### Permitir a importação de favoritos
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Permite que os usuários importem favoritos de outro navegador para o Microsoft Edge.

Se você habilitar essa política, a caixa de seleção **Favoritos** será marcada automaticamente na caixa de diálogo **Importar dados de navegador**.

Se você desabilitar essa política, os favoritos não serão importados na primeira execução e os usuários não poderão importá-los manualmente.

Se você não configurar essa política, os favoritos serão importados na primeira execução e os usuários poderão optar por importá-los manualmente durante as sessões de navegação posteriores.

Você também pode definir essa política como uma recomendação. Isso significa que o Microsoft Edge importa os favoritos na primeira execução, mas os usuários podem marcar ou desmarcar a opção **Favoritos** durante uma importação manual.

**Observação**: essa política atualmente gerencia a importação dos navegadores Internet Explorer (no Windows 7, 8 e 10), Google Chrome (no Windows 7, 8 e 10 e no macOS) e o Mozilla Firefox (no Windows 7, 8 e 10 e no macOS) e no Apple Safari (macOs).

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: Sim
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: ImportFavorites
  - Nome da Política de Grupo: Permitir a importação de favoritos
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): Administrative Templates/Microsoft Edge - Default Settings (usuários podem substituir)/
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nome do valor: ImportFavorites
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ImportFavorites
  - Valor de exemplo:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### ImportHistory
  #### Permitir a importação do histórico de navegação
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Permite que os usuários importem o histórico de navegação de outro navegador para o Microsoft Edge.

Se você habilitar essa política, a caixa de seleção **Histórico de navegação** será marcada automaticamente na caixa de diálogo **Importar dados de navegador**.

Se você desabilitar essa política, os dados do histórico de navegação não serão importados na primeira execução e os usuários não poderão importar esses dados manualmente.

Se você não configurar essa política, os dados do histórico de navegação serão importados na primeira execução e os usuários poderão optar por importá-los manualmente durante as sessões de navegação posteriores.

Você também pode definir essa política como uma recomendação. Isso significa que o Microsoft Edge importa o histórico de navegação na primeira execução, mas os usuários podem marcar ou desmarcar a opção **histórico** durante a importação manual.

**Observação**: essa política atualmente gerencia a importação dos navegadores Internet Explorer (no Windows 7, 8 e 10), Google Chrome (no Windows 7, 8 e 10 e no macOS) e o Mozilla Firefox (no Windows 7, 8 e 10 e no macOS) e no Apple Safari (macOs).

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: Sim
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: ImportHistory
  - Nome da Política de Grupo: Permitir a importação do histórico de navegação
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): Administrative Templates/Microsoft Edge - Default Settings (usuários podem substituir)/
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nome do valor: ImportHistory
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ImportHistory
  - Valor de exemplo:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### ImportHomepage
  #### Permitir a importação de configurações da página inicial
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Permite que os usuários importem as configurações da página inicial de outro navegador para o Microsoft Edge.

Se você habilitar essa política, a opção para importar manualmente a configuração da página inicial será selecionada automaticamente.

Se você desabilitar essa política, a configuração da página inicial não será importada na primeira execução e os usuários não poderão importá-las manualmente.

Se você não configurar essa política, a configuração da página inicial será importada na primeira execução, e os usuários poderão optar por importar esses dados manualmente durante as sessões de navegação posteriores.

Você pode definir essa política como uma recomendação. Isso significa que o Microsoft Edge importa a configuração da página inicial na primeira execução, mas os usuários podem marcar ou desmarcar a **página inicial** durante a importação manual.

**Observação**: essa política atualmente gerencia a importação do Internet Explorer (no Windows 7, 8 e 10).

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: ImportHomepage
  - Nome da Política de Grupo: Permitir a importação de configurações da página inicial
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: ImportHomepage
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ImportHomepage
  - Valor de exemplo:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### ImportOpenTabs
  #### Permitir a importação de guias abertas
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 79 ou mais recente

  #### Descrição
  Permite que os usuários importem guias abertas e fixadas de outro navegador para o Microsoft Edge.

Se você habilitar essa política, a caixa de seleção **Abrir guias** será marcada automaticamente na caixa de diálogo **Importar dados do navegador**.

Se você desabilitar essa política, as guias abertas não serão importadas na primeira execução e os usuários não poderão importá-las manualmente.

Se você não configurar essa política, as guias abertas serão importadas na primeira execução e os usuários poderão optar por importá-las manualmente durante as sessões de navegação posteriores.

Você também pode definir essa política como uma recomendação. Isso significa que o Microsoft Edge importa as guias abertas na primeira execução, mas os usuários podem marcar ou desmarcar as **Guias abertas** durante a importação manual.

**Observação**: essa política atualmente oferece suporte à importação do Google Chrome (no Windows 7, 8 e 10 e no macOS).

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: Sim
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: ImportOpenTabs
  - Nome da Política de Grupo: Permitir a importação de guias abertas
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): Administrative Templates/Microsoft Edge - Default Settings (usuários podem substituir)/
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nome do valor: ImportOpenTabs
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ImportOpenTabs
  - Valor de exemplo:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### ImportPaymentInfo
  #### Permitir a importação de informações de pagamento
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Permite que os usuários importem informações de pagamento de outro navegador para o Microsoft Edge.

Se você habilitar essa política, a caixa de seleção **informação de pagamento** será marcada automaticamente na caixa de diálogo **importar dados de navegador**.

Se você desabilitar essa política, as informações de pagamento não serão importadas na primeira execução e os usuários não poderão importá-las manualmente.

Se você não configurar essa política, as informações de pagamento serão importadas na primeira execução e os usuários poderão optar por importá-las manualmente durante as sessões de navegação posteriores.

Você também pode definir essa política como uma recomendação. Isso significa que o Microsoft Edge importa informações de pagamento na primeira execução, mas os usuários podem marcar ou desmarcar a opção **informações de pagamento** durante uma importação manual.

**Observação:** essa política atualmente gerencia a importação do Google Chrome (no Windows 7, 8 e 10 e no macOS).

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: Sim
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: ImportPaymentInfo
  - Nome da Política de Grupo: Permitir a importação de informações de pagamento
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): Administrative Templates/Microsoft Edge - Default Settings (usuários podem substituir)/
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nome do valor: ImportPaymentInfo
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ImportPaymentInfo
  - Valor de exemplo:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### ImportSavedPasswords
  #### Permitir a importação de senhas salvas
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Permite que os usuários importem senhas salvas de outro navegador para o Microsoft Edge.

Se você habilitar essa política, a opção para importar automaticamente senhas salvas será selecionada automaticamente.

Se você desabilitar essa política, as senhas salvas não serão importadas na primeira execução e os usuários não poderão importá-las manualmente.

Se você não configurar essa política, as senhas serão importadas na primeira execução e os usuários poderão optar por importá-las manualmente durante as sessões de navegação posteriores.

Você pode definir essa política como uma recomendação. Isso significa que o Microsoft Edge importa senhas na primeira execução, mas os usuários podem marcar ou desmarcar as **senhas** na importação manual.

**Observação**: essa política atualmente gerencia a importação dos navegadores Internet Explorer (no Windows 7, 8 e 10), Google Chrome (no Windows 7, 8 e 10 e no macOS) e o Mozilla Firefox (no Windows 7, 8 e 10 e no macOS).

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: Sim
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: ImportSavedPasswords
  - Nome da Política de Grupo: Permitir a importação de senhas salvas
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): Administrative Templates/Microsoft Edge - Default Settings (usuários podem substituir)/
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nome do valor: ImportSavedPasswords
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ImportSavedPasswords
  - Valor de exemplo:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### ImportSearchEngine
  #### Permitir a importação das configurações do mecanismo de pesquisa
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Permite aos usuários importar configurações do mecanismo de pesquisa de outro navegador para o Microsoft Edge.

Se você habilitar essa política, a opção Importar configurações do mecanismo de pesquisa será selecionada automaticamente.

Se você desabilitar essa política, as configurações do mecanismo de pesquisa não serão importadas na primeira execução e os usuários não poderão importá-las manualmente.

Se você não definir essa política, as configurações do mecanismo de pesquisa serão importadas na primeira execução e os usuários poderão optar por importar esses dados manualmente durante as sessões de navegação posteriores.

Você pode definir essa política como uma recomendação. Isso significa que o Microsoft Edge importa configurações de mecanismo de pesquisa na primeira execução, mas os usuários podem marcar ou desmarcar a opção **mecanismo de pesquisa** durante uma importação manual.

**Observação**: essa política atualmente gerencia a importação do Internet Explorer (no Windows 7, 8 e 10).

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: Sim
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: ImportSearchEngine
  - Nome da Política de Grupo: Permitir a importação das configurações do mecanismo de pesquisa
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): Administrative Templates/Microsoft Edge - Default Settings (usuários podem substituir)/
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nome do valor: ImportSearchEngine
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ImportSearchEngine
  - Valor de exemplo:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### ImportShortcuts
  #### Permitir a importação de atalhos
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 81 ou mais recente

  #### Descrição
  Permite que os usuários importem atalhos de outro navegador para o Microsoft Edge.

Se você desabilitar essa política, os atalhos não serão importados na primeira execução.

Se você não configurar essa política, os atalhos serão importados na primeira execução.

Você também pode definir essa política como uma recomendação. Isso significa que o Microsoft Edge importa os atalhos na primeira execução.

**Observação**: essa política atualmente gerencia a importação do Google Chrome (no Windows 7, 8 e 10 e no macOS).

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: Sim
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: ImportShortcuts
  - Nome da Política de Grupo: Permitir a importação de atalhos
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): Administrative Templates/Microsoft Edge - Default Settings (usuários podem substituir)/
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nome do valor: ImportShortcuts
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ImportShortcuts
  - Valor de exemplo:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### InPrivateModeAvailability
  #### Configurar a disponibilidade do modo InPrivate
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Especifica se o usuário pode abrir páginas no modo InPrivate no Microsoft Edge.

Se você não configurar essa política ou defini-la como “Habilitada”, os usuários poderão abrir páginas no modo InPrivate.

Definir essa política como "Desabilitada" para impedir que os usuários usem o modo InPrivate.

Configure esta política como 'Forçado' para usar sempre no modo InPrivate.

Mapeamento das opções de política:

* Habilitado (0) = Modo InPrivate disponível

* Desabilitado (1) = Modo InPrivate desabilitado

* Forçado (2) = Modo InPrivate forçado

Use as informações anteriores ao configurar essa política.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Inteiro

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: InPrivateModeAvailability
  - Nome da Política de Grupo: Configurar a disponibilidade do modo InPrivate
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: InPrivateModeAvailability
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: InPrivateModeAvailability
  - Valor de exemplo:
``` xml
<integer>1</integer>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### InsecureFormsWarningsEnabled
  #### Habilitar avisos para formulários inseguros
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 86 ou mais recente

  #### Descrição
  Essa política controla o tratamento de formulários inseguros (formulários enviados em HTTP) inseridos em sites seguros (HTTPS) no navegador.
Se você habilitar essa política ou não a definir, um aviso de página inteira será mostrado quando um formulário não seguro for enviado. Além disso, uma bolha de aviso será exibida ao lado dos campos de formulário quando eles forem prioritários, e o preenchimento automático será desabilitado para esses formulários.
Se você desabilitar essa política, os avisos não serão exibidos para os formulários inseguros, e o preenchimento automático funcionará normalmente.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: InsecureFormsWarningsEnabled
  - Nome da Política de Grupo: habilitar avisos para formulários inseguros
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do Valor: InsecureFormsWarningsEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: InsecureFormsWarningsEnabled
  - Valor de exemplo:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### IntensiveWakeUpThrottlingEnabled
  #### Controlar o recurso IntensiveWakeUpThrottling
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 85 ou mais recente

  #### Descrição
  Quando habilitado, o recurso de IntensiveWakeUpThrottling faz com que os cronômetros de JavaScript nas guias de segundo plano sejam regulados e coalescidos agressivamente, executando não mais que uma vez por minuto depois que uma página tenha estado em segundo plano por cinco minutos ou mais.

Esse é um recurso compatível com os padrões da Web, mas pode danificar a funcionalidade de alguns sites, fazendo com que determinadas ações sejam adiadas até um minuto. No entanto, isso resulta em economias significativas de CPU e bateria quando habilitado. Consulte https://bit.ly/30b1XR4 para obter mais detalhes.

Se você habilitar essa política, o recurso será forçado habilitado e os usuários não poderão substituir essa configuração.
Se você desabilitar essa política, o recurso será forçado desabilitado e os usuários não poderão substituir essa configuração.
Se você não configurar essa política, o recurso será controlado pela sua própria lógica interna. Os usuários podem definir manualmente essa configuração.

Observe que a política é aplicada por processo de processamento, com o valor mais recente da configuração de política em vigor quando um processo de processamento é iniciado. É necessário reiniciar para garantir que todas as guias carregadas recebam uma configuração de política consistente. É inofensivo para os processos serem executados com valores diferentes nesta política.


  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: IntensiveWakeUpThrottlingEnabled
  - Nome da Política de Grupo: Controlar o recurso IntensiveWakeUpThrottling
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: IntensiveWakeUpThrottlingEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: IntensiveWakeUpThrottlingEnabled
  - Valor de exemplo:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### InternetExplorerIntegrationEnhancedHangDetection
  #### Configurar a detecção de trava avançada para o modo do Internet Explorer
  
  
  #### Versões com suporte:
  - No Windows desde 84 ou posterior

  #### Descrição
  A detecção de trava avançada é uma abordagem mais granular para detectar páginas da Web travadas no modo Internet Explorer da que usa o Internet Explorer autônomo. Quando uma página da Web travada é detectada, o navegador aplica uma mitigação para impedir que o restante do navegador seja travado.

Essa configuração permite que você defina a detecção de trava avançada caso tenha problemas incompatíveis com qualquer um dos seus sites. Recomendamos desabilitar essa política somente se você vir notificações como "(site) não está respondendo" no modo Internet Explorer, mas não no Internet Explorer autônomo.

Essa configuração funciona em conjunto com a: [InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel) está definida como "IEMode" e a política [InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist) onde a lista tem pelo menos uma entrada.

Se você definir essa política como 'Habilitada' ou não a configurar, os sites que estiverem executando no modo Internet Explorer usarão a detecção de trava avançada.

Se você definir essa política como 'Desabilitada', a detecção de trava avançada será desabilitada, e os usuários receberão o comportamento de detecção básica do Internet Explorer.

Para saber mais sobre o modo do Internet Explorer, confira [https://go.microsoft.com/fwlink/?linkid=2094210](https://go.microsoft.com/fwlink/?linkid=2094210)

Mapeamento das opções de política:

* Desabilitada (0) = Detecção de trava avançada desabilitada

* Habilitada (1) = Detecção de trava avançada habilitada

Use as informações anteriores ao configurar essa política.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: não requer a reinicialização do navegador

  #### Tipo de dados:
  - Inteiro

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: InternetExplorerIntegrationEnhancedHangDetection
  - Nome da Política de Grupo: Configurar a detecção de trava avançada para o modo do Internet Explorer
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: InternetExplorerIntegrationEnhancedHangDetection
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  

  [Voltar ao início](#microsoft-edge---policies)

  ### InternetExplorerIntegrationLevel
  #### Configurar a integração do Internet Explorer
  
  
  #### Versões com suporte:
  - No Windows desde 77 ou posterior

  #### Descrição
  Para obter instruções sobre como configurar a melhor experiência para o modo do Internet Explorer, confira [https://go.microsoft.com/fwlink/?linkid=2094210](https://go.microsoft.com/fwlink/?linkid=2094210)

Mapeamento das opções de política:

* Nenhum (0) = Nenhum

* IEMode (1) = Modo do Internet Explorer

* NeedIE (2) = Internet Explorer 11

Use as informações anteriores ao configurar essa política.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: não requer a reinicialização do navegador

  #### Tipo de dados:
  - Inteiro

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: InternetExplorerIntegrationLevel
  - Nome da Política de Grupo: Configurar a integração do Internet Explorer
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: InternetExplorerIntegrationLevel
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  

  [Voltar ao início](#microsoft-edge---policies)

  ### InternetExplorerIntegrationSiteList
  #### Configurar a lista de sites do modo Empresarial
  
  
  #### Versões com suporte:
  - No Windows desde 78 ou posterior

  #### Descrição
  Para obter instruções sobre como configurar a melhor experiência para o modo do Internet Explorer, confira [https://go.microsoft.com/fwlink/?linkid=2094210](https://go.microsoft.com/fwlink/?linkid=2094210)

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: não requer a reinicialização do navegador

  #### Tipo de dados:
  - String

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: InternetExplorerIntegrationSiteList
  - Nome da Política de Grupo: Configurar a lista de sites do modo Empresarial
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: InternetExplorerIntegrationSiteList
  - Tipo do valor: REG_SZ
  ##### Valor de exemplo:
```
"https://internal.contoso.com/sitelist.xml"
```


  

  [Voltar ao início](#microsoft-edge---policies)

  ### InternetExplorerIntegrationSiteRedirect
  #### Especificar como as navegações "na página" para sites não configurados se comportam quando iniciadas nas páginas do modo Internet Explorer.
  
  
  #### Versões com suporte:
  - No Windows desde 81 ou posterior

  #### Descrição
  Uma navegação “na página” é iniciada a partir de um link, um script ou um formulário na página atual. Também pode ser um redirecionamento do servidor de uma tentativa anterior de navegação “na página”. Por outro lado, um usuário pode iniciar uma navegação que não é “na página” e independente da página atual de várias maneiras, usando os controles do navegador. Por exemplo, usando a barra de endereço, o botão voltar ou um link favorito.

Essa configuração permite especificar se as navegações de páginas carregadas no modo do Internet Explorer para sites não configurados (que não estão configurados na lista de sites do modo empresarial) voltam para o Microsoft Edge ou permanecem no modo do Internet Explorer.

Essa configuração funciona em conjunto com a: [InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel) está definida como "IEMode" e a política [InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist) onde a lista tem pelo menos uma entrada.

Se você desabilitar ou não configurar essa política, somente os sites configurados para abrir no modo Internet Explorer serão abertos nesse modo. Qualquer site não configurado para abrir no modo Internet Explorer será redirecionado de volta ao Microsoft Edge.

Se você definir essa política como 'Padrão', somente os sites configurados para abrir no modo do Internet Explorer serão abertos nesse modo. Qualquer site não configurado para abrir no modo Internet Explorer será redirecionado de volta ao Microsoft Edge.

Se você definir essa política como 'AutomaticNavigationsOnly', obterá a experiência padrão, exceto que todas as navegações automáticas (por exemplo, redirecionamentos 302) para sites não configurados que serão mantidas no modo do Internet Explorer.

Se você definir essa política como 'AllInPageNavigations', todas as navegações de páginas carregadas no modo IE para sites não configurados serão mantidas no modo Internet Explorer (Menos Recomendado).

Para saber mais sobre o modo do Internet Explorer, confira [https://go.microsoft.com/fwlink/?linkid=2105106](https://go.microsoft.com/fwlink/?linkid=2105106)

Mapeamento das opções de política:

* Padrão (0) = Padrão

* AutomaticNavigationsOnly (1) = Manter somente as navegações automáticas no modo do Internet Explorer

* AllInPageNavigations (2) = Manter todas as navegações na página no modo Internet Explorer

Use as informações anteriores ao configurar essa política.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: não requer a reinicialização do navegador

  #### Tipo de dados:
  - Inteiro

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: InternetExplorerIntegrationSiteRedirect
  - Nome da Política de Grupo: Especificar como as navegações "na página" para sites não configurados se comportam quando iniciadas nas páginas do modo Internet Explorer.
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: InternetExplorerIntegrationSiteRedirect
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000000
```


  

  [Voltar ao início](#microsoft-edge---policies)

  ### InternetExplorerIntegrationTestingAllowed
  #### Permitir teste no modo Internet Explorer
  
  
  #### Versões com suporte:
  - No Windows desde 86 ou posterior

  #### Descrição
  Essa política é um substituto para a política de sinalizador do modo IE. Permite que os usuários abram uma guia do modo IE na opção do menu UI.

Essa configuração funciona em conjunto com a: [InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel) está definida como "IEMode" e a política [InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist) onde a lista tem pelo menos uma entrada.

Se você habilitar essa política, os usuários poderão abrir a guia no modo IE da opção IU e navegar o site atual para um site modo IE.

Se você desabilitar essa política, os usuários não poderão ver a opção IU no menu diretamente.

Se você não configurar essa política, poderá configurar o sinalizador de teste do modo IE manualmente.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: não requer a reinicialização do navegador

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: InternetExplorerIntegrationTestingAllowed
  - Nome da Política de Grupo: Permitir teste no modo Internet Explorer
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do Valor: InternetExplorerIntegrationTestingAllowed
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000000
```


  

  [Voltar ao início](#microsoft-edge---policies)

  ### IsolateOrigins
  #### Habilitar o isolamento de sites para determinadas origens
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Especifique as origens para serem executadas isoladamente, em seus próprios processos.

Essa política também isola as origens chamadas por subdomínios, por exemplo, especificar https://contoso.com/ fará https://foo.contoso.com/ ser isolada como parte do sitehttps://contoso.com/.

Se a política estiver habilitada, cada uma das origens indicadas em uma lista de valores separados por vírgulas será executada em seu próprio processo.

Se você desabilitar essa política, os recursos "IsolateOrigins" e "SitePerProcess" serão desabilitados. Os usuários ainda podem habilitá-las manualmente, por meio de sinalizadores de linha de comando.

Se você não configurar a política, o usuário poderá alterar essa configuração.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: não requer a reinicialização do navegador

  #### Tipo de dados:
  - String

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: IsolateOrigins
  - Nome da Política de Grupo: Habilitar o isolamento de sites para determinadas origens
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: IsolateOrigins
  - Tipo do valor: REG_SZ
  ##### Valor de exemplo:
```
"https://contoso.com/,https://fabrikam.com/"
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: IsolateOrigins
  - Valor de exemplo:
``` xml
<string>https://contoso.com/,https://fabrikam.com/</string>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### LocalProvidersEnabled
  #### Permitir sugestões de provedores locais
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 83 ou mais recente

  #### Descrição
  Permitir sugestões de provedores de sugestões no dispositivo (provedores locais), por exemplo, Favoritos e Histórico de navegação, na Barra de endereços e na lista Sugestão Automática do Microsoft Edge.

Se você habilitar essa política, serão usadas sugestões de provedores locais.

Se você desabilitar essa política, as sugestões de provedores locais nunca serão usadas. As sugestões de histórico local e favoritos locais não serão exibidas.

Se você não configurar essa política, as sugestões de provedores locais serão permitidas, mas o usuário poderá mudar de acordo com as configurações.

Alguns recursos podem não estar disponíveis se uma política para desabilitar esse recurso tiver sido aplicada. Por exemplo, sugestões de histórico de navegação não estarão disponíveis se você habilitar a política [SavingBrowserHistoryDisabled](#savingbrowserhistorydisabled).

Essa política exige uma reinicialização do navegador para concluir a aplicação.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: Sim
  - Atualização dinâmica das políticas: não requer a reinicialização do navegador

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: LocalProvidersEnabled
  - Nome da Política de Grupo: Permitir sugestões de provedores locais
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): Administrative Templates/Microsoft Edge - Default Settings (usuários podem substituir)/
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nome do valor: LocalProvidersEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000000
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: LocalProvidersEnabled
  - Valor de exemplo:
``` xml
<false/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### ManagedFavorites
  #### Configurar Favoritos
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Configura uma lista de favoritos gerenciados.

A política cria uma lista de favoritos. Cada favorito contém as teclas "nome" e "URL", que contêm o nome do favorito e seu destino. Você pode configurar uma subpasta definindo os favoritos sem uma chave "URL", mas com uma chave "infantil" adicional que contenha uma lista de favoritos, conforme definido acima (algumas delas podem ser pastas novamente). O Microsoft Edge resolve URLs incompletas como se elas fossem enviadas por meio da Barra de Endereços, por exemplo, "microsoft.com" torna-se "https://microsoft.com/".

Esses favoritos são colocados em uma pasta que não pode ser modificada pelo usuário (mas o usuário pode optar por ocultá-los na barra Favoritos). Por padrão, o nome da pasta é "Favoritos gerenciados", mas você pode alterá-lo, adicionando à lista de favoritos um dicionário contendo a chave "toplevel_name" com o nome da pasta desejado como o valor.

Os favoritos gerenciados não são sincronizados com a conta de usuário e não podem ser modificados por extensões.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Dictionary

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: ManagedFavorites
  - Nome da Política de Grupo: Configurar Favoritos
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: ManagedFavorites
  - Tipo do valor: REG_SZ
  ##### Valor de exemplo:
```
SOFTWARE\Policies\Microsoft\Edge\ManagedFavorites = [
  {
    "toplevel_name": "My managed favorites folder"
  }, 
  {
    "name": "Microsoft", 
    "url": "microsoft.com"
  }, 
  {
    "name": "Bing", 
    "url": "bing.com"
  }, 
  {
    "children": [
      {
        "name": "Microsoft Edge Insiders", 
        "url": "www.microsoftedgeinsider.com"
      }, 
      {
        "name": "Microsoft Edge", 
        "url": "www.microsoft.com/windows/microsoft-edge"
      }
    ], 
    "name": "Microsoft Edge links"
  }
]
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ManagedFavorites
  - Valor de exemplo:
``` xml
<key>ManagedFavorites</key>
<array>
  <dict>
    <key>toplevel_name</key>
    <string>My managed favorites folder</string>
  </dict>
  <dict>
    <key>name</key>
    <string>Microsoft</string>
    <key>url</key>
    <string>microsoft.com</string>
  </dict>
  <dict>
    <key>name</key>
    <string>Bing</string>
    <key>url</key>
    <string>bing.com</string>
  </dict>
  <dict>
    <key>children</key>
    <array>
      <dict>
        <key>name</key>
        <string>Microsoft Edge Insiders</string>
        <key>url</key>
        <string>www.microsoftedgeinsider.com</string>
      </dict>
      <dict>
        <key>name</key>
        <string>Microsoft Edge</string>
        <key>url</key>
        <string>www.microsoft.com/windows/microsoft-edge</string>
      </dict>
    </array>
    <key>name</key>
    <string>Microsoft Edge links</string>
  </dict>
</array>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### ManagedSearchEngines
  #### Gerenciar mecanismos de pesquisa
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Permite que você configure uma lista de até dez mecanismos de pesquisa, que deve ser marcada como mecanismo de pesquisa padrão.
Você não precisa especificar a codificação. A partir do Microsoft Edge 80, os parâmetros suggest_url e image_search_url são opcionais. O parâmetro opcional, image_search_post_params (consiste em pares de nome/valor separados por vírgula), que está disponível a partir do Microsoft Edge 80.

A partir do Microsoft Edge 83, você pode habilitar a descoberta de mecanismos de pesquisa com o parâmetro opcional allow_search_engine_discovery. Esse parâmetro deve ser o primeiro item na lista. Se allow_search_engine_discovery não for especificado, a descoberta de mecanismos de pesquisa será desabilitada por padrão. A partir do Microsoft Edge 84, você pode definir essa política como uma política recomendada para permitir a descoberta de provedores de pesquisa. Não é necessário adicionar o parâmetro opcional allow_search_engine_discovery.

Se você habilitar essa política, os usuários não poderão adicionar, remover ou alterar nenhum mecanismo de pesquisa na lista. Os usuários podem definir seu mecanismo de pesquisa padrão para qualquer mecanismo de pesquisa na lista.

Se você desabilitar ou não configurar essa política, os usuários poderão modificar a lista de mecanismos de pesquisa conforme desejado.

Se a política [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl) estiver definida, essa política (ManagedSearchEngines) será ignorada. O usuário deve reiniciar o navegador para concluir a aplicação da política.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: Sim
  - Atualização dinâmica das políticas: não requer a reinicialização do navegador

  #### Tipo de dados:
  - Dictionary

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: ManagedSearchEngines
  - Nome da Política de Grupo: Gerenciar mecanismos de pesquisa
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): Administrative Templates/Microsoft Edge - Default Settings (usuários podem substituir)/
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nome do valor: ManagedSearchEngines
  - Tipo do valor: REG_SZ
  ##### Valor de exemplo:
```
SOFTWARE\Policies\Microsoft\Edge\ManagedSearchEngines = [
  {
    "allow_search_engine_discovery": true
  }, 
  {
    "is_default": true, 
    "keyword": "example1.com", 
    "name": "Example1", 
    "search_url": "https://www.example1.com/search?q={searchTerms}", 
    "suggest_url": "https://www.example1.com/qbox?query={searchTerms}"
  }, 
  {
    "image_search_post_params": "content={imageThumbnail},url={imageURL},sbisrc={SearchSource}", 
    "image_search_url": "https://www.example2.com/images/detail/search?iss=sbiupload", 
    "keyword": "example2.com", 
    "name": "Example2", 
    "search_url": "https://www.example2.com/search?q={searchTerms}", 
    "suggest_url": "https://www.example2.com/qbox?query={searchTerms}"
  }, 
  {
    "encoding": "UTF-8", 
    "image_search_url": "https://www.example3.com/images/detail/search?iss=sbiupload", 
    "keyword": "example3.com", 
    "name": "Example3", 
    "search_url": "https://www.example3.com/search?q={searchTerms}", 
    "suggest_url": "https://www.example3.com/qbox?query={searchTerms}"
  }, 
  {
    "keyword": "example4.com", 
    "name": "Example4", 
    "search_url": "https://www.example4.com/search?q={searchTerms}"
  }
]
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ManagedSearchEngines
  - Valor de exemplo:
``` xml
<key>ManagedSearchEngines</key>
<array>
  <dict>
    <key>allow_search_engine_discovery</key>
    <true/>
  </dict>
  <dict>
    <key>is_default</key>
    <true/>
    <key>keyword</key>
    <string>example1.com</string>
    <key>name</key>
    <string>Example1</string>
    <key>search_url</key>
    <string>https://www.example1.com/search?q={searchTerms}</string>
    <key>suggest_url</key>
    <string>https://www.example1.com/qbox?query={searchTerms}</string>
  </dict>
  <dict>
    <key>image_search_post_params</key>
    <string>content={imageThumbnail},url={imageURL},sbisrc={SearchSource}</string>
    <key>image_search_url</key>
    <string>https://www.example2.com/images/detail/search?iss=sbiupload</string>
    <key>keyword</key>
    <string>example2.com</string>
    <key>name</key>
    <string>Example2</string>
    <key>search_url</key>
    <string>https://www.example2.com/search?q={searchTerms}</string>
    <key>suggest_url</key>
    <string>https://www.example2.com/qbox?query={searchTerms}</string>
  </dict>
  <dict>
    <key>encoding</key>
    <string>UTF-8</string>
    <key>image_search_url</key>
    <string>https://www.example3.com/images/detail/search?iss=sbiupload</string>
    <key>keyword</key>
    <string>example3.com</string>
    <key>name</key>
    <string>Example3</string>
    <key>search_url</key>
    <string>https://www.example3.com/search?q={searchTerms}</string>
    <key>suggest_url</key>
    <string>https://www.example3.com/qbox?query={searchTerms}</string>
  </dict>
  <dict>
    <key>keyword</key>
    <string>example4.com</string>
    <key>name</key>
    <string>Example4</string>
    <key>search_url</key>
    <string>https://www.example4.com/search?q={searchTerms}</string>
  </dict>
</array>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### MaxConnectionsPerProxy
  #### Número máximo de conexões simultâneas com o servidor proxy
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Especifica o número máximo de conexões simultâneas com o servidor proxy.

Alguns servidores proxy não podem lidar com um grande número de conexões simultâneas por cliente. Você pode resolver isso configurando essa política para um valor mais baixo.

O valor desta política deve ser menor do que 100 e maior do que 6. O valor padrão é 32.

Alguns aplicativos web são conhecidos por consumir várias conexões com GETs suspensos. Diminuir o máximo de conexões para abaixo de 32 pode levar à interrupção da rede do navegador se muitos desses aplicativos estiverem abertos. 

Se você não configurar essa política, o valor padrão (32) será usado.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: não requer a reinicialização do navegador

  #### Tipo de dados:
  - Inteiro

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: MaxConnectionsPerProxy
  - Nome da Política de Grupo: Número máximo de conexões simultâneas com o servidor proxy
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: MaxConnectionsPerProxy
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000020
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: MaxConnectionsPerProxy
  - Valor de exemplo:
``` xml
<integer>32</integer>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### MediaRouterCastAllowAllIPs
  #### Permitir que o Google Cast se conecte a dispositivos de conversão em todos os endereços IP
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Habilitar essa política para permitir que o Google Cast se conecte a dispositivos Cast em todos os endereços IP, não apenas em endereços privados RFC1918/RFC4193.

Desative esta política para restringir o Google Cast a dispositivos Cast nos endereços privados RFC1918 / RFC4193.

Se você não configurar essa política, o Google Cast se conectará aos dispositivos Cast somente em endereços privados RFC1918/RFC4193, a menos que você habilite o recurso CastAllowAllIPs.

Se a política [EnableMediaRouter](#enablemediarouter) estiver desabilitada, essa política não terá efeito.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: MediaRouterCastAllowAllIPs
  - Nome da Política de Grupo: Permitir que o Google Cast se conecte a dispositivos de conversão em todos os endereços IP
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: MediaRouterCastAllowAllIPs
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000000
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: MediaRouterCastAllowAllIPs
  - Valor de exemplo:
``` xml
<false/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### MetricsReportingEnabled
  #### Habilitar a geração de relatórios de dados de uso e relacionados a falhas (descontinuada)
  >SUBSTITUÍDO: Essa política está preterida. Ela tem suporte no momento, mas se tornará obsoleta em uma versão futura.
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Essa política foi preterida. Está sendo suportada no momento, mas se tornará obsoleta no Microsoft Edge 89. Essa política foi substituída pela nova política: [DiagnosticData](#diagnosticdata) para o Windows 7, Windows 8 e macOS. Essa política foi substituída por “Permitir telemetria” no Win 10 ([https://go.microsoft.com/fwlink/?linkid=2099569](https://go.microsoft.com/fwlink/?linkid=2099569)).

Esta política habilita a geração de relatórios de dados relacionados a falhas e uso do Microsoft Edge para a Microsoft.

Habilite essa política para enviar relatórios de dados relacionados a falhas e uso para a Microsoft. Desabilite essa política para não enviar esses dados para a Microsoft. Em ambos os casos, os usuários não poderão alterar nem substituir a configuração.

Nos Windows 10, se você não configurar essa política, o Microsoft Edge usará como padrão a configuração de dados de diagnóstico do Windows. Se essa política estiver habilitada, o Microsoft Edge enviará dados de uso somente se a configuração de dados de diagnóstico do Windows estiver definida como Avançada ou Completa. Se essa política estiver desabilitada, o Microsoft Edge não enviará dados de uso. Os dados relacionados a falha são enviados com base na configuração de dados de diagnóstico do Windows. Saiba mais sobre as configurações de dados de diagnóstico do Windows em[https://go.microsoft.com/fwlink/?linkid=2099569](https://go.microsoft.com/fwlink/?linkid=2099569).

No Windows 7, Windows 8 e macOS essa política controla o envio de dados de uso e relacionados a falhas. Se você não configurar essa política, o padrão do Microsoft Edge será a preferência do usuário.

Para habilitar essa política, [SendSiteInfoToImproveServices](#sendsiteinfotoimproveservices) deve ser configurado como Habilitado. Se [MetricsReportingEnabled](#metricsreportingenabled) ou [SendSiteInfoToImproveServices](#sendsiteinfotoimproveservices) estiverem com status Não Configurado ou Desabilitado os dados não serão enviados para a Microsoft.

Essa política está disponível apenas nas instâncias do Windows que fazem parte de um domínio do Microsoft Active Directory, em instâncias do Windows 10 Pro ou Enterprise que estejam inscritas no gerenciamento de dispositivos ou em instâncias do macOS que são gerenciadas por meio do MDM ou passaram a fazer parte de um domínio por meio de MCX.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: não requer a reinicialização do navegador

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: MetricsReportingEnabled
  - Nome da Política de Grupo: Habilitar a geração de relatórios de dados de uso e relacionados a falhas (descontinuada)
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: MetricsReportingEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: MetricsReportingEnabled
  - Valor de exemplo:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### NativeWindowOcclusionEnabled
  #### Habilitar Native Window Occlusion
  
  
  #### Versões com suporte:
  - No Windows desde 84 ou posterior

  #### Descrição
  Ativa a oclusão da janela nativa no Microsoft Edge.

Se você habilitar essa configuração para reduzir o consumo de CPU e de energia, o Microsoft Edge detectará quando uma janela é coberta por outras janelas e suspenderá os pixels da pintura do trabalho.

Se você desabilitar essa configuração, o Microsoft Edge não detectará quando uma janela é coberta por outras janelas.

Se essa política não estiver definida, a detecção de ocultação da janela será habilitada.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: NativeWindowOcclusionEnabled
  - Nome da GP: habilitar a oclusão da janela nativa
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: NativeWindowOcclusionEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  

  [Voltar ao início](#microsoft-edge---policies)

  ### NavigationDelayForInitialSiteListDownloadTimeout
  #### Definir um tempo limite para o atraso da navegação da guia para a lista de sites do Modo Empresarial
  
  
  #### Versões com suporte:
  - No Windows desde 84 ou posterior

  #### Descrição
  Permite que você especifique se o Microsoft Edge vai aguardar até que o navegador baixe a lista de sites inicial no Modo Empresarial.

Essa configuração funciona em conjunto com o: [InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel) está definido como "IEMode" e a política [InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist), onde a lista tem pelo menos uma entrada e [DelayNavigationsForInitialSiteListDownload](#delaynavigationsforinitialsitelistdownload) está definida como "Todas as navegações elegíveis" (1).

As guias não aguardam mais do que esse tempo limite para o download da lista de sites do Modo Empresarial. Se o navegador não tiver terminado de baixar a lista de sites no Modo Empresarial quando o tempo limite expirar, as guias do Microsoft Edge continuarão a ser navegadas. O valor do tempo limite não deve ultrapassar 20 segundos e não ser inferior a 1 segundo.

Se você definir o tempo limite nesta política como um valor maior do que o padrão de 2 segundos, uma barra de informações será exibida para o usuário após 2 segundos. A barra de informações contém um botão que permite ao usuário abandonar a espera para a conclusão do download da lista de sites do Modo Empresarial.

Se você não configurar essa política, o tempo limite padrão de 2 segundos será utilizado. Esse padrão está sujeito à alterações futuras.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: não requer a reinicialização do navegador

  #### Tipo de dados:
  - Inteiro

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: NavigationDelayForInitialSiteListDownloadTimeout
  - Nome da Política de Grupo: Definir um tempo limite para o atraso da navegação da guia para a lista de sites do Modo Empresarial
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do Valor: NavigationDelayForInitialSiteListDownloadTimeout
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x0000000a
```


  

  [Voltar ao início](#microsoft-edge---policies)

  ### NetworkPredictionOptions
  #### Habilitar a previsão de rede
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Ativa a previsão de rede e impede que os usuários alterem essa configuração.

Isso controla a pré-busca de DNS, a pré-conexão TCP e SSL e a pré-renderização de páginas da web.

Se você não configurar essa política, a previsão de rede será habilitada, mas o usuário poderá alterá-la.

Mapeamento das opções de política:

* NetworkPredictionAlways (0) = Prever ações de rede em qualquer conexão de rede

* NetworkPredictionWifiOnly (1) = Sem suporte, se esse valor for usado, ele será tratado como se a configuração "Prever ações de rede em qualquer conexão de rede" (0) tiver sido definida

* NetworkPredictionNever (2) = Não prever ações de rede em nenhuma conexão de rede

Use as informações anteriores ao configurar essa política.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: Sim
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Inteiro

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: NetworkPredictionOptions
  - Nome da Política de Grupo: Habilitar a previsão de rede
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): Administrative Templates/Microsoft Edge - Default Settings (usuários podem substituir)/
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nome do valor: NetworkPredictionOptions
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000002
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: NetworkPredictionOptions
  - Valor de exemplo:
``` xml
<integer>2</integer>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### NonRemovableProfileEnabled
  #### Configurar se um usuário sempre tem um perfil padrão conectado automaticamente à sua conta corporativa ou de estudante
  
  
  #### Versões com suporte:
  - No Windows desde 78 ou posterior

  #### Descrição
  Essa política determina se um usuário pode remover o perfil Microsoft Edge automaticamente conectado com uma conta corporativa ou de estudante.

Se você habilitar essa política, um perfil não removível será criado com a conta corporativa ou de estudante do usuário no Windows. Esse perfil não poderá ser desconectado nem removido.

Se você desabilitar ou não configurar essa política, o perfil automaticamente conectado com uma conta corporativa ou de estudante do usuário no Windows poderá ser desconectado ou removido pelo usuário.

Se você quiser configurar o navegador, use a política [BrowserSignin](#browsersignin).

Essa política só está disponível em instâncias do Windows que fazem parte de um domínio do Microsoft Active Directory, instâncias do Windows 10 Pro ou Enterprise que foram inscritas no gerenciamento de dispositivos.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: NonRemovableProfileEnabled
  - Nome da Política de Grupo: Configurar se um usuário sempre tem um perfil padrão conectado automaticamente à sua conta corporativa ou de estudante
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: NonRemovableProfileEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  

  [Voltar ao início](#microsoft-edge---policies)

  ### OverrideSecurityRestrictionsOnInsecureOrigin
  #### Controle onde as restrições de segurança em origens inseguras se aplicam
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Especifica uma lista de origens (URLs) ou padrões de nome de host (por exemplo, "*. contoso.com") para os quais as restrições de segurança não devem ser aplicadas.

Essa política permite especificar origens permitidas para aplicativos herdados que não podem implantar o TLS ou configurar um servidor de migração para o desenvolvimento da web interna para que os desenvolvedores possam testar recursos que exigem contextos seguros sem ter de implantar o TLS no servidor de teste. Essa política também impede que a origem seja rotulada como "não seguro" em omnibox.

Configurar uma lista de URLs nesta política tem o mesmo efeito que configurar o sinalizador de linha de comando '--unsafely-treat-insecure-origin-as-secure' para uma lista separada por vírgula das mesmas URLs. Se você habilitar essa política, ela substituirá o sinalizador de linha de comando.

Para obter mais informações sobre contextos protegidos, consulte https://www.w3.org/TR/secure-contexts/.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: não requer a reinicialização do navegador

  #### Tipo de dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: OverrideSecurityRestrictionsOnInsecureOrigin
  - Nome da Política de Grupo: Controle onde as restrições de segurança em origens inseguras se aplicam
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge\OverrideSecurityRestrictionsOnInsecureOrigin
  - Caminho (recomendado): N/A
  - Nome do valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de exemplo:
```
SOFTWARE\Policies\Microsoft\Edge\OverrideSecurityRestrictionsOnInsecureOrigin\1 = "http://testserver.contoso.com/"
SOFTWARE\Policies\Microsoft\Edge\OverrideSecurityRestrictionsOnInsecureOrigin\2 = "*.contoso.com"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: OverrideSecurityRestrictionsOnInsecureOrigin
  - Valor de exemplo:
``` xml
<array>
  <string>http://testserver.contoso.com/</string>
  <string>*.contoso.com</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### PaymentMethodQueryEnabled
  #### Permitir que os sites pesquisem os métodos de pagamento disponíveis
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 80 ou mais recente

  #### Descrição
  Permite definir se os sites podem verificar se o usuário tem métodos de pagamento salvos.

Se você desabilitar essa política, os sites que usam as APIs PaymentRequest.canMakePayment ou PaymentRequest.hasEnrolledInstrument serão informados de que nenhum método de pagamento está disponível.

Se você habilitar essa política ou não definir essa política, os sites poderão verificar se o usuário tem métodos de pagamento salvos.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: PaymentMethodQueryEnabled
  - Nome da Política de Grupo: Permitir que os sites pesquisem os métodos de pagamento disponíveis
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: PaymentMethodQueryEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: PaymentMethodQueryEnabled
  - Valor de exemplo:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### PersonalizationReportingEnabled
  #### Permite a personalização de anúncios, pesquisas e notícias enviando o histórico de navegação à Microsoft.
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 80 ou mais recente

  #### Descrição
  Essa política impede que a Microsoft colete o histórico de navegação do Microsoft Edge de um usuário para ser usado para personalizar anúncios, pesquisa, notícias e outros serviços Microsoft.

Essa configuração só está disponível para usuários com uma conta Microsoft. Essa configuração não está disponível para contas infantis ou contas corporativas.

Se você desabilitar essa política, os usuários não poderão alterar nem substituir a configuração. Se essa política não estiver configurada ou habilitada, o padrão do Microsoft Edge será a preferência do usuário.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: PersonalizationReportingEnabled
  - Nome da Política de Grupo: Permitir a personalização de anúncios, pesquisas e notícias enviando o histórico de navegação à Microsoft.
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: PersonalizationReportingEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: PersonalizationReportingEnabled
  - Valor de exemplo:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### PinningWizardAllowed
  #### Permitir fixar o assistente na barra de tarefas
  
  
  #### Versões com suporte:
  - No Windows desde 80 ou posterior

  #### Descrição
  O Microsoft Edge usa o assistente Fixar na barra de tarefas para ajudar os usuários a fixar sites sugeridos na barra de tarefas. O recurso Fixar na barra de tarefas é habilitado por padrão e pode ser acessado pelo usuário por meio do menu Configurações e mais.

Se você habilitar essa política ou não a configurar, os usuários poderão chamar o assistente de Fixação à barra de tarefas no menu Configurações e Mais. O assistente também pode ser chamado por meio de um lançamento de protocolo.

Se você desabilitar essa política, o assistente Fixar na barra de tarefas será desabilitado no menu e não poderá ser chamado por meio de um lançamento de protocolo.

As configurações do usuário para habilitar ou desabilitar o assistente Fixar na barra de tarefas não estarão disponíveis.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: não requer a reinicialização do navegador

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: PinningWizardAllowed
  - Nome da Política de Grupo: Permitir fixar o assistente na barra de tarefas
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: PinningWizardAllowed
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000000
```


  

  [Voltar ao início](#microsoft-edge---policies)

  ### ProactiveAuthEnabled
  #### Habilitar a autenticação Proativa
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Permite que você configure a ativação da Autenticação Pró-ativa.

Se você habilitar essa política, o Microsoft Edge tentará autenticar proativamente o usuário conectado com os serviços Microsoft. Em intervalos regulares, o Microsoft Edge verifica com um serviço online para obter um manifesto atualizado que contém a configuração que governa como fazer isso.

Se você desabilitar essa política, o Microsoft Edge não tentará autenticar proativamente o usuário conectado com os serviços Microsoft. O Microsoft Edge não verifica mais um serviço online em busca de um manifesto atualizado que contém a configuração para fazer isso.

Se você não configurar essa política, a Autenticação Pró-ativa será ativada.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: não requer a reinicialização do navegador

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: ProactiveAuthEnabled
  - Nome da Política de Grupo: Habilitar a autenticação Proativa
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: ProactiveAuthEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ProactiveAuthEnabled
  - Valor de exemplo:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### PromotionalTabsEnabled
  #### Habilitar o conteúdo promocional em uma guia
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Controlar a apresentação do conteúdo promocional ou educacional da guia completa. Essa configuração controla a apresentação das páginas de boas-vindas que ajudam os usuários a entrar no Microsoft Edge, escolher seu navegador padrão ou saber mais sobre os recursos do produto.

Se você habilitar essa política (definir como verdadeira) ou não a configurar, o Microsoft Edge poderá mostrar o conteúdo de guia integral aos usuários para fornecer informações sobre o produto.

Se você desabilitar (definir como falsa) essa política, o Microsoft Edge não poderá mostrar o conteúdo de guia integral aos usuários.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: PromotionalTabsEnabled
  - Nome da Política de Grupo: Habilitar o conteúdo promocional em uma guia
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: PromotionalTabsEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000000
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: PromotionalTabsEnabled
  - Valor de exemplo:
``` xml
<false/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### PromptForDownloadLocation
  #### Perguntar onde salvar os arquivos baixados
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Definir se deseja perguntar onde deseja salvar um arquivo antes de baixá-lo.

Se você habilitar essa política, o usuário será solicitado a salvar o arquivo antes de baixá-lo. Se você não a configurar, os arquivos serão salvos automaticamente no local padrão, sem perguntar ao usuário.

Se você não configurar essa política, o usuário poderá alterar essa configuração.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: PromptForDownloadLocation
  - Nome da Política de Grupo: Perguntar onde salvar os arquivos baixados
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: PromptForDownloadLocation
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000000
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: PromptForDownloadLocation
  - Valor de exemplo:
``` xml
<false/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### QuicAllowed
  #### Permitir protocolo QUIC
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Permitir o uso do protocolo QUIC no Microsoft Edge.

Se você habilitar essa política ou não a configurar, o protocolo QUIC será permitido.

Se você desabilitar essa política, o protocolo QUIC será bloqueado.

O QUIC é um protocolo de rede de camada de transporte que pode melhorar o desempenho de aplicativos web que usam o TCP no momento.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: não requer a reinicialização do navegador

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: QuicAllowed
  - Nome da Política de Grupo: Permitir protocolo QUIC
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: QuicAllowed
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: QuicAllowed
  - Valor de exemplo:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### RelaunchNotification
  #### Notificar um usuário que uma reinicialização do navegador é recomendada ou necessária para atualizações pendentes
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Notifique os usuários de que precisam reiniciar o Microsoft Edge para aplicar uma atualização pendente.

Se você não configurar essa política, o Microsoft Edge adicionará um ícone de reciclagem na extremidade direita da barra do menu superior para solicitar que os usuários reiniciem o navegador para aplicar a atualização.

Se você habilitar essa política e configurá-la como "Recomendável", um aviso recorrente alertará os usuários de que uma reinicialização é recomendada. Os usuários podem descartar esse aviso e adiar a reinicialização.

Se você definir a política como “Obrigatória”, um aviso recorrente avisará os usuários que o navegador será reiniciado automaticamente assim que o período de notificação passar. O período padrão é sete dias. Você pode configurar esse período com a política de [RelaunchNotificationPeriod](#relaunchnotificationperiod).

A sessão do usuário será restaurada quando o navegador reiniciar.

Mapeamento das opções de política:

* Recomendado (1) = Recomendável - Mostra um aviso recorrente para o usuário indicando que é recomendável reiniciar

* Obrigatório (2) = Obrigatório - Mostra um aviso recorrente para o usuário indicando que a reinicialização é obrigatória

Use as informações anteriores ao configurar essa política.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Inteiro

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: RelaunchNotification
  - Nome da Política de Grupo: Notificar um usuário que uma reinicialização do navegador é recomendada ou necessária para atualizações pendentes
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: RelaunchNotification
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: RelaunchNotification
  - Valor de exemplo:
``` xml
<integer>1</integer>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### RelaunchNotificationPeriod
  #### Definir o período de tempo das notificações de atualização
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Permite que você defina o período de tempo, em milissegundos, em que os usuários serão notificados de que o Microsoft Edge deve ser reiniciado para aplicar uma atualização pendente.

Durante esse período de tempo, o usuário será informado repetidamente da necessidade de uma atualização. No Microsoft Edge, o menu do aplicativo é alterado para indicar que um reinício é necessário quando um terço (1/3) das notificações passar o período. Essa notificação mudará depois de passar dois terços do período de notificação e novamente quando o período de notificação tiver passado por completo. As notificações adicionais habilitadas pela política [RelaunchNotification](#relaunchnotification) seguem o mesmo cronograma.

Caso contrário, o período padrão de 604,8 milhões milissegundos (uma semana) será usado.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Inteiro

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: RelaunchNotificationPeriod
  - Nome da Política de Grupo: Definir o período de tempo das notificações de atualização
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: RelaunchNotificationPeriod
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x240c8400
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: RelaunchNotificationPeriod
  - Valor de exemplo:
``` xml
<integer>604800000</integer>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### RendererCodeIntegrityEnabled
  #### Habilitar integridade de código de renderizador
  
  
  #### Versões com suporte:
  - No Windows desde 78 ou posterior

  #### Descrição
  Se essa política estiver ativada ou não definida, a Integridade do código do renderizador será ativada. Essa política só deve ser desabilitada se houver problemas de compatibilidade com software de terceiros que devem ser executados dentro dos processos de renderização do Microsoft Edge.

Desabilitar essa política tem um efeito prejudicial à segurança e à estabilidade do Microsoft Edge porque um código desconhecido e potencialmente hostil poderá ser carregado dentro dos processos de renderização do Microsoft Edge.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: não requer a reinicialização do navegador

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: RendererCodeIntegrityEnabled
  - Nome da Política de Grupo: Habilitar integridade de código de renderizador
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: RendererCodeIntegrityEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000000
```


  

  [Voltar ao início](#microsoft-edge---policies)

  ### RequireOnlineRevocationChecksForLocalAnchors
  #### Especificar se serão necessárias verificações OCSP/CRL online para âncoras de confiança locais
  
  
  #### Versões com suporte:
  - No Windows desde 77 ou posterior

  #### Descrição
  Controlar se a verificação de revogação online (verificações OCSP/CRL) é necessária. Se o Microsoft Edge não conseguir obter as informações de status de revogação, esses certificados serão tratados como revogados ("falha em discos rígidos").

Se você habilitar essa política, o Microsoft Edge sempre executará a verificação de revogação de certificados de servidor que validam com êxito e são assinados por certificados de autoridade de certificação instalados localmente.

Se você não configurar ou desabilitar essa política, o Microsoft Edge usará as configurações de verificação de revogação online existentes.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: RequireOnlineRevocationChecksForLocalAnchors
  - Nome da Política de Grupo: Especificar se serão necessárias verificações OCSP/CRL online para âncoras de confiança locais
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: RequireOnlineRevocationChecksForLocalAnchors
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000000
```


  

  [Voltar ao início](#microsoft-edge---policies)

  ### ResolveNavigationErrorsUseWebService
  #### Habilitar a resolução de erros de navegação usando um serviço Web
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Permitir que o Microsoft Edge emita uma conexão sem dados com um serviço da web para sondar as redes em casos como Wi-Fi de hotéis e aeroportos.

Se você habilitar essa política, um serviço web será usado para testes de conectividade de rede.

Se você desabilitar essa política, o Microsoft Edge usará APIs nativas para tentar resolver problemas de navegação e conectividade de rede.

**Observação**: exceto no Windows 8 e nas versões posteriores do Windows, o Microsoft Edge *sempre* usa APIs nativas para resolver problemas de conectividade.

Se você não configurar essa política, o Microsoft Edge respeitará a preferência do usuário definida em serviços em edge://settings/privacy.
Especificamente, há um botão de alternância**Usar um serviço web para ajudar a resolver erros de navegação**, que o usuário pode ativar ou desativar. Lembre-se de que, se você tiver habilitado essa política (ResolveNavigationErrorsUseWebService), a configuração **Usar um serviço Web para resolver erros de navegação** estará ativada, mas o usuário não poderá alterar a configuração usando o botão de alternância. Se você tiver desabilitado essa política, a configuração **Usar um serviço Web para resolver erros de navegação** a configuração estará desativada, e o usuário não poderá alterar a configuração usando o botão de alternância.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: Sim
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: ResolveNavigationErrorsUseWebService
  - Nome da Política de Grupo: Habilitar a resolução de erros de navegação usando um serviço Web
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): Administrative Templates/Microsoft Edge - Default Settings (usuários podem substituir)/
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nome do valor: ResolveNavigationErrorsUseWebService
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ResolveNavigationErrorsUseWebService
  - Valor de exemplo:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### RestrictSigninToPattern
  #### Restringir quais contas podem ser usadas como contas principais do Microsoft Edge
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Determina quais contas podem ser definidas como contas principais do navegador no Microsoft Edge (a conta escolhida durante o fluxo de aceitação da sincronização).

Se um usuário tentar configurar uma conta primária do navegador com um nome de usuário que não corresponda a esse padrão, eles serão bloqueados e verão uma mensagem de erro apropriada. Você pode configurar essa política para corresponder a várias contas usando uma expressão regular no estilo Perl para o padrão. Observe que as correspondências padrão diferenciam maiúsculas de minúsculas. Para obter mais informações sobre as regras de expressão regular usadas, consulte https://go.microsoft.com/fwlink/p/?linkid=2133903.

Se você não configurar essa política ou deixá-la em branco, os usuários poderão definir qualquer conta como uma conta primária do navegador no Microsoft Edge.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - String

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: RestrictSigninToPattern
  - Nome da Política de Grupo: Restringir quais contas podem ser usadas como contas principais do Microsoft Edge
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: RestrictSigninToPattern
  - Tipo do valor: REG_SZ
  ##### Valor de exemplo:
```
".*@contoso.com"
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: RestrictSigninToPattern
  - Valor de exemplo:
``` xml
<string>.*@contoso.com</string>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### RoamingProfileLocation
  #### Configurar o diretório de perfil móvel
  
  
  #### Versões com suporte:
  - No Windows desde 85 ou posterior

  #### Descrição
  Configura o diretório a ser usado para armazenar a cópia de perfis de roaming.

Se você habilitar essa política, o Microsoft Edge usará o diretório fornecido para armazenar uma cópia de roaming dos perfis, desde que você também tenha habilitado a política [RoamingProfileSupportEnabled](#roamingprofilesupportenabled). Se você desabilitar a política [RoamingProfileSupportEnabled](#roamingprofilesupportenabled) ou não configurá-la, o valor armazenado nessa política não será utilizado.

Confira [https://go.microsoft.com/fwlink/?linkid=2095041](https://go.microsoft.com/fwlink/?linkid=2095041) para obter uma lista de variáveis que você pode usar.

Se você não configurar essa política, o caminho de perfil móvel será utilizado.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: não requer a reinicialização do navegador

  #### Tipo de dados:
  - String

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: RoamingProfileLocation
  - Nome da Política de Grupo: Configurar o diretório de perfil móvel
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: RoamingProfileLocation
  - Tipo do valor: REG_SZ
  ##### Valor de exemplo:
```
"${roaming_app_data}\\edge-profile"
```


  

  [Voltar ao início](#microsoft-edge---policies)

  ### RoamingProfileSupportEnabled
  #### Habilitar o uso de cópias de roaming para dados de perfil do Microsoft Edge
  
  
  #### Versões com suporte:
  - No Windows desde 85 ou posterior

  #### Descrição
  Habilite essa política para usar perfis móveis no Windows. As configurações armazenadas nos perfis do Microsoft Edge (favoritos e preferências) também são salvas em um arquivo armazenado na pasta de perfil de usuário móvel (ou em um local especificado pelo administrador na política [RoamingProfileLocation](#roamingprofilelocation)).

Se você desabilitar essa política ou não a configurar, somente os perfis locais normais serão usados.

A política [SyncDisabled](#syncdisabled) desabilita toda a sincronização de dados, substituindo a política.

Confira https://docs.microsoft.com/windows-server/storage/folder-redirection/deploy-roaming-user-profiles para saber mais sobre como usar perfis de usuários móveis.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: não requer a reinicialização do navegador

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: RoamingProfileSupportEnabled
  - Nome da Política de Grupo: Habilitar o uso de cópias de roaming para dados de perfil do Microsoft Edge
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: RoamingProfileSupportEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  

  [Voltar ao início](#microsoft-edge---policies)

  ### RunAllFlashInAllowMode
  #### Estender a configuração de conteúdo do Adobe Flash a todo o conteúdo
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Se você habilitar essa política, todo o conteúdo do Adobe Flash inserido em sites configurados para permitir o Adobe Flash nas configurações de conteúdo, pelo usuário ou pela política empresarial, será executado. Isso inclui conteúdo de outras origens e/ou conteúdo pequeno.

Para controlar quais sites podem executar o Adobe Flash, Confira as especificações nas políticas [DefaultPluginsSetting](#defaultpluginssetting), [PluginsAllowedForUrls](#pluginsallowedforurls)e [PluginsBlockedForUrls](#pluginsblockedforurls).

Se você desabilitar essa política ou não a configurar, o conteúdo do Adobe Flash de outras origens (de sites que não estão especificados nas três políticas mencionadas imediatamente acima) ou o conteúdo pequeno poderá ser bloqueado.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: RunAllFlashInAllowMode
  - Nome da Política de Grupo: Estender a configuração de conteúdo do Adobe Flash a todo o conteúdo
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: RunAllFlashInAllowMode
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: RunAllFlashInAllowMode
  - Valor de exemplo:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### SSLErrorOverrideAllowed
  #### Permitir que os usuários continuem a partir da página de aviso de HTTPS
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  O Microsoft Edge mostra uma página de aviso quando os usuários acessam sites que têm erros SSL.

Se você habilitar ou não configurar (padrão) essa política, os usuários podem clicar nessas páginas de aviso.

Se você desabilitar essa política, os usuários serão impedidos de clicar em qualquer página de aviso.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: SSLErrorOverrideAllowed
  - Nome da Política de Grupo: Permitir que os usuários continuem a partir da página de aviso de HTTPS
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: SSLErrorOverrideAllowed
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: SSLErrorOverrideAllowed
  - Valor de exemplo:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### SSLVersionMin
  #### Versão mínima do TLS habilitada
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Define a versão mínima suportada do TLS. Se você não configurar essa política, o Microsoft Edge usará uma versão mínima padrão, TLS 1,0.

Se você habilitar essa política, o Microsoft Edge não usará qualquer versão de SSL/TLS inferior à versão especificada. Todos os valores não reconhecidos são ignorados.

Mapeamento das opções de política:

* TLSv1 (tls1) = TLS 1.0

* TLSv1.1 (tls1.1) = TLS 1.1

* TLSv1.2 (tls1.2) = TLS 1.2

Use as informações anteriores ao configurar essa política.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - String

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: SSLVersionMin
  - Nome da Política de Grupo: Versão mínima do TLS habilitada
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: SSLVersionMin
  - Tipo do valor: REG_SZ
  ##### Valor de exemplo:
```
"tls1"
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: SSLVersionMin
  - Valor de exemplo:
``` xml
<string>tls1</string>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### SaveCookiesOnExit
  #### Salvar os cookies ao fechar o Microsoft Edge
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 86 ou mais recente

  #### Descrição
  Quando essa política estiver habilitada, o conjunto de cookies especificado estará isento da exclusão quando o navegador for fechado. Essa política só estará em vigor quando:
- O botão de alternância "Cookies e outros dados do site" estiver configurado em Configurações/Privacidade e serviços/Limpar dados de navegação ao fechar; ou
- A política [ClearBrowsingDataOnExit](#clearbrowsingdataonexit) estiver habilitada; ou
- A política [DefaultCookiesSetting](#defaultcookiessetting) estiver configurada para “Manter os cookies apenas durante a sessão”.

Você pode definir uma lista de sites, com base em padrões de URL, que terão seus cookies preservados em todas as sessões.

Observação: os usuários continuam podendo editar a lista de sites relativa aos cookies para adicionar ou remover URLs. No entanto, não podem remover URLs que foram adicionados por um administrador.

Se você habilitar essa política, a lista de cookies não será apagada quando o navegador for fechado.

Se você desabilitar ou não configurar essa política, será usada a configuração pessoal do usuário.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: não requer a reinicialização do navegador

  #### Tipo de dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome único da Política de Grupo: SaveCookiesOnExit
  - Nome da Política de Grupo: Salvar os cookies ao fechar o Microsoft Edge
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge\SaveCookiesOnExit
  - Caminho (recomendado): N/A
  - Nome do valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de exemplo:
```
SOFTWARE\Policies\Microsoft\Edge\SaveCookiesOnExit\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\SaveCookiesOnExit\2 = "[*.]contoso.edu"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: SaveCookiesOnExit
  - Valor de exemplo:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### SavingBrowserHistoryDisabled
  #### Desabilitar o salvamento do histórico do navegador
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Desabilita o salvamento do histórico do navegador e impede que os usuários alterem essa configuração.

Se você habilitar essa política, o histórico de navegação não será salvo. Isso também desabilita a sincronização de tabulação.

Se você desabilitar essa política ou não a configurar, o histórico de navegação será salvo.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: SavingBrowserHistoryDisabled
  - Nome da Política de Grupo: Desabilitar o salvamento do histórico do navegador
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do Valor: SavingBrowserHistoryDisabled
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: SavingBrowserHistoryDisabled
  - Valor de exemplo:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### ScreenCaptureAllowed
  #### Permitir ou negar captura de tela
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 83 ou mais recente

  #### Descrição
  Se você habilitar essa política ou não configurar essa política, uma página da Web poderá usar APIs de compartilhamento de tela (por exemplo, getDisplayMedia () ou a API da extensão de captura da área de trabalho) para uma captura de tela.
Se você desabilitar essa política, as chamadas a APIs de compartilhamento de tela falharão. Por exemplo, se você estiver usando uma reunião online baseada na Web, o vídeo ou o compartilhamento de tela não funcionarão.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: ScreenCaptureAllowed
  - Nome da Política de Grupo: Permitir ou negar captura de tela
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: ScreenCaptureAllowed
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000000
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ScreenCaptureAllowed
  - Valor de exemplo:
``` xml
<false/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### ScrollToTextFragmentEnabled
  #### Ativar a rolagem para o texto especificado nos fragmentos de URL.
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 83 ou mais recente

  #### Descrição
  Esse recurso permite que as navegações por URL de hiperlink e barra de endereço direcionem texto específico em uma página da Web, que será rolada para depois que a página da Web terminar de carregar.

Se você habilitar ou não configurar essa política, a rolagem de página da Web para fragmentos de texto específicos por meio de uma URL será habilitada.

Se você desabilitar essa política, a rolagem de página da Web para fragmentos de texto específicos por meio de uma URL será desabilitada.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: não requer a reinicialização do navegador

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: ScrollToTextFragmentEnabled
  - Nome da Política de Grupo: Habilitar a rolagem para o texto especificado em fragmentos de URL
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: ScrollToTextFragmentEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000000
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ScrollToTextFragmentEnabled
  - Valor de exemplo:
``` xml
<false/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### SearchSuggestEnabled
  #### Permitir sugestões de pesquisa
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Permite sugestões de pesquisa na Web na barra de endereços e sugere automaticamente a lista de endereços do Microsoft Edge e impede que os usuários alterem essa política.

Se você habilitar essa política, serão usadas sugestões de pesquisa na Web.

Se você desabilitar essa política, as sugestões de pesquisa na Web nunca serão usadas, mas as sugestões de favoritos locais e do histórico local ainda serão exibidas. Se você desabilitar essa política, nem os caracteres digitados nem as URLs visitadas serão incluídas na telemetria para a Microsoft.

Se essa política não estiver definida, as sugestões de pesquisa serão habilitadas, mas o usuário poderá alterá-la.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: Sim
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: SearchSuggestEnabled
  - Nome da Política de Grupo: Permitir sugestões de pesquisa
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): Administrative Templates/Microsoft Edge - Default Settings (usuários podem substituir)/
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nome do valor: SearchSuggestEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: SearchSuggestEnabled
  - Valor de exemplo:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### SecurityKeyPermitAttestation
  #### Sites ou domínios que não precisam de permissão para usar o atestado de chave de segurança direta
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Especifica sites e domínios que não precisam de permissão explícita quando os certificados de atestado das chaves de segurança são solicitados. Além disso, um sinal é enviado para a chave de segurança, indicando que pode usar atestado individual. Sem isso, os usuários são solicitados sempre que um site solicita o atestado das chaves de segurança.

Sites (por exemplo https://contoso.com/some/path), só correspondem a appID U2Fs. Domínios (por exemplo, contoso.com) correspondem apenas como IDs webauthn RP. Para abranger as APIs U2F e webauthn para um determinado site, você precisa listar a URL do appID e o domínio.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: SecurityKeyPermitAttestation
  - Nome da Política de Grupo: Sites ou domínios que não precisam de permissão para usar o atestado de chave de segurança direta
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge\SecurityKeyPermitAttestation
  - Caminho (recomendado): N/A
  - Nome do valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de exemplo:
```
SOFTWARE\Policies\Microsoft\Edge\SecurityKeyPermitAttestation\1 = "https://contoso.com"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: SecurityKeyPermitAttestation
  - Valor de exemplo:
``` xml
<array>
  <string>https://contoso.com</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### SendIntranetToInternetExplorer
  #### Enviar todos os sites da intranet para o Internet Explorer
  
  
  #### Versões com suporte:
  - No Windows desde 77 ou posterior

  #### Descrição
  Para obter instruções sobre como configurar a melhor experiência para o modo do Internet Explorer, confira [https://go.microsoft.com/fwlink/?linkid=2094210](https://go.microsoft.com/fwlink/?linkid=2094210)

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: não requer a reinicialização do navegador

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: SendIntranetToInternetExplorer
  - Nome da Política de Grupo: Enviar todos os sites da intranet para o Internet Explorer
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do Valor: SendIntranetToInternetExplorer
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  

  [Voltar ao início](#microsoft-edge---policies)

  ### SendSiteInfoToImproveServices
  #### Enviar informações de sites para aprimorar os serviços da Microsoft (descontinuado)
  >SUBSTITUÍDO: Essa política está preterida. Ela tem suporte no momento, mas se tornará obsoleta em uma versão futura.
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Essa política foi preterida. Está sendo suportada no momento, mas se tornará obsoleta no Microsoft Edge 89. Essa política foi substituída pela nova política: [DiagnosticData](#diagnosticdata) para o Windows 7, Windows 8 e macOS. Essa política foi substituída por “Permitir telemetria” no Win 10 ([https://go.microsoft.com/fwlink/?linkid=2099569](https://go.microsoft.com/fwlink/?linkid=2099569)).

Essa política permite o envio de informações sobre sites visitados no Microsoft Edge para a Microsoft visando melhorar serviços, tais como a pesquisa.

Habilite essa política para enviar informações sobre os sites visitados no Microsoft Edge para a Microsoft. Desabilite essa política para não enviar informações sobre os sites visitados no Microsoft Edge para a Microsoft. Em ambos os casos, os usuários não poderão alterar nem substituir a configuração.

Nos Windows 10, se você não configurar essa política, o Microsoft Edge usará como padrão a configuração de dados de diagnóstico do Windows. Se essa política estiver habilitada, o Microsoft Edge enviará informações sobre os sites visitados no Microsoft Edge se a configuração de dados de diagnóstico do Windows estiver definida como Completa. Se essa política estiver desabilitada, o Microsoft Edge não enviará informações sobre os sites visitados. Saiba mais sobre as configurações de Dados de diagnóstico do Windows:[https://go.microsoft.com/fwlink/?linkid=2099569](https://go.microsoft.com/fwlink/?linkid=2099569)

No Windows 7, Windows 8 e macOS, essa política controla o envio de informações sobre sites visitados. Se você não configurar essa política, o padrão do Microsoft Edge será a preferência do usuário.

Para habilitar essa política, [MetricsReportingEnabled](#metricsreportingenabled) deve ser configurado como habilitado. Se [SendSiteInfoToImproveServices](#sendsiteinfotoimproveservices) ou [MetricsReportingEnabled](#metricsreportingenabled) estiverem com status Não Configurado ou Desabilitado os dados não serão enviados para a Microsoft.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: não requer a reinicialização do navegador

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: SendSiteInfoToImproveServices
  - Nome da Política de Grupo: Envie as informações de sites para aprimorar os serviços da Microsoft (descontinuada)
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: SendSiteInfoToImproveServices
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000000
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: SendSiteInfoToImproveServices
  - Valor de exemplo:
``` xml
<false/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### SensorsAllowedForUrls
  #### Permitir o acesso a sensores em sites específicos
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 86 ou mais recente

  #### Descrição
  Defina uma lista de sites, com base em padrões de URL, que podem acessar e usar sensores, como sensores de movimento e de luz.

Se você não configurar essa política, o valor padrão global da diretiva [DefaultSensorsSetting](#defaultsensorssetting) (se definida) ou a configuração pessoal do usuário será usada para todos os sites.

Para padrões de URL que não correspondam a essa política, a ordem de precedência a seguir será usada: a política [SensorsBlockedForUrls](#sensorsblockedforurls) (se definida), a política [DefaultSensorsSetting](#defaultsensorssetting) (se definida) ou as configurações pessoais do usuário.

Os padrões de URL definidos nessa política não podem entrar em conflito com aqueles configurados na política [SensorsBlockedForUrls](#sensorsblockedforurls). Você não pode permitir e bloquear uma URL.

Para obter informações detalhadas sobre os padrões de URL válidos, consulte [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: SensorsAllowedForUrls
  - Nome da Política de Grupo: Permitir o acesso a sensores em sites específicos
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge\SensorsAllowedForUrls
  - Caminho (recomendado): N/A
  - Nome do valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de exemplo:
```
SOFTWARE\Policies\Microsoft\Edge\SensorsAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\SensorsAllowedForUrls\2 = "[*.]contoso.edu"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: SensorsAllowedForUrls
  - Valor de exemplo:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### SensorsBlockedForUrls
  #### Bloquear o acesso a sensores em sites específicos
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 86 ou mais recente

  #### Descrição
  Defina uma lista de sites, com base em padrões de URL, que não podem acessar sensores, como sensores de movimento e de luz.

Se você não configurar essa política, o valor padrão global da diretiva [DefaultSensorsSetting](#defaultsensorssetting) (se definida) ou a configuração pessoal do usuário será usada para todos os sites.

Para padrões de URL que não correspondam a essa política, a ordem de precedência a seguir será usada: a política [SensorsAllowedForUrls](#sensorsallowedforurls) (se definida), a política [DefaultSensorsSetting](#defaultsensorssetting) (se definida) ou as configurações pessoais do usuário.

Os padrões de URL definidos nessa política não podem entrar em conflito com aqueles configurados na política [SensorsAllowedForUrls](#sensorsallowedforurls). Você não pode permitir e bloquear uma URL.

Para obter informações detalhadas sobre os padrões de URL válidos, consulte [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: SensorsBlockedForUrls
  - Nome da Política de Grupo: Bloquear o acesso a sensores em sites específicos
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge\SensorsBlockedForUrls
  - Caminho (recomendado): N/A
  - Nome do valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de exemplo:
```
SOFTWARE\Policies\Microsoft\Edge\SensorsBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\SensorsBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: SensorsBlockedForUrls
  - Valor de exemplo:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### SerialAskForUrls
  #### Permitir a API serial em sites específicos
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 86 ou mais recente

  #### Descrição
  Defina uma lista de sites, com base em padrões de URL, que podem solicitar acesso ao usuário para uma porta serial.

Se você não configurar essa política, o valor padrão global da diretiva [DefaultSerialGuardSetting](#defaultserialguardsetting) (se definida) ou a configuração pessoal do usuário será usada para todos os sites.

Para padrões de URL que não correspondam a essa política, a ordem de precedência a seguir será usada: a política [SerialBlockedForUrls](#serialblockedforurls) (se definida), a política [DefaultSensorsSetting](#defaultserialguardsetting) (se definida) ou as configurações pessoais do usuário.

Os padrões de URL definidos nessa política não podem entrar em conflito com aqueles configurados na política [SerialBlockedForUrls](#serialblockedforurls). Você não pode permitir e bloquear uma URL.

Para obter informações detalhadas sobre os padrões de URL válidos, consulte [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: SerialAskForUrls
  - Nome da Política de Grupo: Permitir a API serial em sites específicos
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge\SerialAskForUrls
  - Caminho (recomendado): N/A
  - Nome do valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de exemplo:
```
SOFTWARE\Policies\Microsoft\Edge\SerialAskForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\SerialAskForUrls\2 = "[*.]contoso.edu"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: SerialAskForUrls
  - Valor de exemplo:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### SerialBlockedForUrls
  #### Bloquear a API serial em sites específicos
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 86 ou mais recente

  #### Descrição
  Defina uma lista de sites, com base em padrões de URL, que não podem solicitar ao usuário que conceda acesso a uma porta serial.

Se você não configurar essa política, o valor padrão global da diretiva [DefaultSerialGuardSetting](#defaultserialguardsetting) (se definida) ou a configuração pessoal do usuário será usada para todos os sites.

Para padrões de URL que não correspondam a essa política, a ordem de precedência a seguir será usada: a política [SerialAskForUrls](#serialaskforurls) (se definida), a política [DefaultSerialGuardSetting](#defaultserialguardsetting) (se definida) ou as configurações pessoais do usuário.

Os padrões de URL nesta política não podem entrar em conflito com aqueles configurados na política [SerialAskForUrls](#serialaskforurls). Você não pode permitir e bloquear uma URL.

Para obter informações detalhadas sobre os padrões de URL válidos, consulte [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: SerialBlockedForUrls
  - Nome da Política de Grupo: Bloquear a API serial em sites específicos
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge\SerialBlockedForUrls
  - Caminho (recomendado): N/A
  - Nome do valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de exemplo:
```
SOFTWARE\Policies\Microsoft\Edge\SerialBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\SerialBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: SerialBlockedForUrls
  - Valor de exemplo:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### ShowOfficeShortcutInFavoritesBar
  #### Exibir o atalho do Microsoft Office na barra de favoritos (obsoleto)
  >SUBSTITUÍDO: Essa política está preterida. Ela tem suporte no momento, mas se tornará obsoleta em uma versão futura.
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Esta política não funcionou conforme o esperado devido a alterações nos requisitos operacionais. Therefore it's deprecated and should not be used.

Especifica se um atalho deve ser incluído no Office.com na barra de favoritos. For users signed into Microsoft Edge the shortcut takes users to their Microsoft Office apps and docs. If you enable or don't configure this policy, users can choose whether to see the shortcut by changing the toggle in the favorites bar context menu.
Se você desativar esta política, o atalho não será mostrado.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: ShowOfficeShortcutInFavoritesBar
  - Nome da GP: Exibir o atalho do Microsoft Office na barra de favoritos (obsoleto)
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do Valor: ShowOfficeShortcutInFavoritesBar
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000000
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ShowOfficeShortcutInFavoritesBar
  - Valor de exemplo:
``` xml
<false/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### SignedHTTPExchangeEnabled
  #### Habilitar o suporte para o Exchange HTTP (SXG) assinado
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 78 ou mais recente

  #### Descrição
  Habilitar o suporte para o Exchange HTTP (SXG) assinado

Se essa política não estiver definida ou habilitada, o Microsoft Edge aceitará o conteúdo da Web servido como Trocas HTTP Assinadas.

Se essa política estiver definida como desabilitada, as trocas HTTP assinadas não poderão ser carregadas.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: SignedHTTPExchangeEnabled
  - Nome da Política de Grupo: Habilitar o suporte para o Exchange HTTP (SXG) assinado
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: SignedHTTPExchangeEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: SignedHTTPExchangeEnabled
  - Valor de exemplo:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### SitePerProcess
  #### Habilitar o isolamento de sites para todos os sites
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  A política "SitePerProcess" pode ser usada para impedir que os usuários façam o comportamento padrão de isolar todos os sites. Lembre-se de que você também pode usar a política [IsolateOrigins](#isolateorigins)para isolar origens adicionais e mais refinadas.

Se você habilitar essa política, os usuários não poderão recusar o comportamento padrão em que cada site é executado em seu próprio processo.

Se você desabilitar ou não configurar essa política, um usuário poderá optar por não isolar o site.  (Por exemplo, usando a entrada "Desabilitar isolamento de site" em edge://flags.)  Desabilitar a política ou não configurar a política não desativa o isolamento do site.


  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: não requer a reinicialização do navegador

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: SitePerProcess
  - Nome da Política de Grupo: Habilitar o isolamento de sites para todos os sites
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: SitePerProcess
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: SitePerProcess
  - Valor de exemplo:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### SpellcheckEnabled
  #### Habilitar verificação ortográfica
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Se você habilitar ou não configurar essa política, o usuário poderá usar o verificador ortográfico.

Se você desabilitar essa política, o usuário não poderá usar o verificador ortográfico e as políticas[SpellcheckLanguage](#spellchecklanguage) e [SpellcheckLanguageBlocklist](#spellchecklanguageblocklist) também serão desabilitadas.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: SpellcheckEnabled
  - Nome da Política de Grupo: Habilitar a verificação ortográfica
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: SpellcheckEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000000
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: SpellcheckEnabled
  - Valor de exemplo:
``` xml
<false/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### SpellcheckLanguage
  #### Habilitar idiomas de verificação ortográfica específicos
  
  
  #### Versões com suporte:
  - No Windows desde 77 ou posterior

  #### Descrição
  Permite a verificação ortográfica em diferentes idiomas. Todos os idiomas que você especificar que não são reconhecidos são ignorados.

Se você habilitar essa política, a verificação ortográfica será habilitada para os idiomas especificados, bem como os idiomas que o usuário habilitou.

Se você não configurar ou desabilitar essa política, não haverá alteração nas preferências de verificação ortográfica do usuário.

Se a política [SpellcheckEnabled](#spellcheckenabled) estiver desabilitada, essa política não terá efeito.

Se um idioma estiver incluído nas políticas "SpellcheckLanguage" e [SpellcheckLanguageBlocklist](#spellchecklanguageblocklist), o idioma de verificação ortográfica estará habilitado.

Os idiomas oferecidos são: af, bg, ca, cs, cy, da, de, el, en-AU, en-CA, en-GB, en-US, es, es-419, es-AR, es-ES, es-MX, es-US, et, fa, fo, fr, he, hi, hr, hu, id, it, ko, lt, lv, nb, nl, pl, pt-BR, pt-PT, ro, ru, sh, sk, sl, sq, sr, sv, ta, tg, tr, uk, vi.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: SpellcheckLanguage
  - Nome da Política de Grupo: Habilitar idiomas de verificação ortográfica específicos
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguage
  - Caminho (recomendado): N/A
  - Nome do valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de exemplo:
```
SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguage\1 = "fr"
SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguage\2 = "es"

```


  

  [Voltar ao início](#microsoft-edge---policies)

  ### SpellcheckLanguageBlocklist
  #### Forçar a desabilitação de idiomas de verificação ortográfica
  
  
  #### Versões com suporte:
  - No Windows desde 78 ou posterior

  #### Descrição
  Forçar a desabilitação de idiomas de verificação ortográfica. Os idiomas não reconhecidos nessa lista serão ignorados.

Se você habilitar essa política, a verificação ortográfica será desabilitada para os idiomas especificados. O usuário ainda pode habilitar ou desabilitar a verificação ortográfica para idiomas que não estão na lista.

Se você não definir essa política ou desabilitá-la, não haverá alteração nas preferências de verificação ortográfica do usuário.

Se a política [SpellcheckEnabled](#spellcheckenabled) estiver definida como desabilitada, essa política não terá efeito.

Se um idioma estiver incluído nas políticas [SpellcheckLanguage](#spellchecklanguage) e “SpellcheckLanguageBlocklist”, o idioma de verificação ortográfica estará habilitado.

Os idiomas com suporte no momento são: af, bg, ca, cs, da, de, el, en-AU, en-CA, en-GB, en-US, es, es-419, es-AR, es-ES, es-MX, es- US, et, fa, fo, fr, he, oi, hr, hu, id, it, ko, lt, lv, nb, nl, pl, pt-BR, pt-PT, ro, ru, sh, sk, sl, sq, sr, sv, ta, tg, tr, uk, vi.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: SpellcheckLanguageBlocklist
  - Nome da Política de Grupo: Forçar a desabilitação de idiomas de verificação ortográfica
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguageBlocklist
  - Caminho (recomendado): N/A
  - Nome do valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de exemplo:
```
SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguageBlocklist\1 = "fr"
SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguageBlocklist\2 = "es"

```


  

  [Voltar ao início](#microsoft-edge---policies)

  ### StricterMixedContentTreatmentEnabled
  #### Habilitar tratamento mais estrito para conteúdo misto (preterido)
  >SUBSTITUÍDO: Essa política está preterida. Ela tem suporte no momento, mas se tornará obsoleta em uma versão futura.
  
  #### Versões com suporte:
  - No Windows e no macOS desde 81 ou mais recente

  #### Descrição
  Essa política foi preterida porque destina-se a ser um mecanismo de curto prazo para dar mais tempo para que as empresas atualizem o conteúdo da Web se e quando ele for incompatível com um tratamento de conteúdo misto mais estrito. Ela não funcionará no Microsoft Edge versão 85.

Esta política controla o tratamento de conteúdo misto (conteúdo HTTP em sites HTTPS) no navegador.

Se você definir essa política como verdadeira ou não definida, o áudio e o vídeo misto serão automaticamente atualizados para HTTPS (ou seja, a URL será regravada como HTTPS, sem um retorno se o recurso não estiver disponível em HTTPS) e um aviso "não seguro" será mostrado na barra de URLs para conteúdo misto de imagens.

Se você definir a política como falsa, as atualizações automáticas serão desabilitadas para áudio e vídeo, e nenhum aviso será mostrado para imagens.

Essa política não afeta outros tipos de conteúdo misto diferentes de áudio, vídeo e imagens.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: StricterMixedContentTreatmentEnabled
  - Nome da GP: Habilitar tratamento mais estrito para conteúdo misto (preterido)
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: StricterMixedContentTreatmentEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: StricterMixedContentTreatmentEnabled
  - Valor de exemplo:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### SuppressUnsupportedOSWarning
  #### Suprimir o aviso do sistema operacional sem suporte
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Omite o aviso que é exibido quando o Microsoft Edge está sendo executado em um computador ou sistema operacional sem suporte.

Se essa política for falsa ou não estiver configurada, os avisos serão exibidos em computadores sem suporte ou sistemas operacionais.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: não requer a reinicialização do navegador

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: SuppressUnsupportedOSWarning
  - Nome da Política de Grupo: Suprimir o aviso do sistema operacional sem suporte
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do Valor: SuppressUnsupportedOSWarning
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: SuppressUnsupportedOSWarning
  - Valor de exemplo:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### SyncDisabled
  #### Desabilitar a sincronização de dados usando o Microsoft Sync Services
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Desabilita a sincronização de dados no Microsoft Edge. Essa política também impede que a solicitação de consentimento de sincronização apareça.

Se você não definir essa política ou aplicá-la conforme recomendado, os usuários poderão ativar ou desativar a sincronização. Se você aplicar essa política como obrigatória, os usuários não poderão ativar a sincronização.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: Sim
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: SyncDisabled
  - Nome da Política de Grupo: Desabilitar a sincronização de dados usando o Microsoft Sync Services
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): Administrative Templates/Microsoft Edge - Default Settings (usuários podem substituir)/
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nome do valor: SyncDisabled
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: SyncDisabled
  - Valor de exemplo:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### SyncTypesListDisabled
  #### Configurar a lista de tipos excluídos da sincronização.
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 83 ou mais recente

  #### Descrição
  Se você habilitar essa política, todos os tipos de dados especificados serão excluídos da sincronização. Essa política pode ser usada para limitar o tipo de dados carregados para o serviço de sincronização do Microsoft Edge.

Você pode fornecer um dos seguintes tipos de dados para essa política: "favorites", "settings", "passwords", "addressesAndMore", "extensions", "history", "openTabs" e "collections". Observe que esses nomes de tipo de dados diferenciam maiúsculas de minúsculas.

Os usuários não poderão substituir os tipos de dados desabilitados.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: não requer a reinicialização do navegador

  #### Tipo de dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: SyncTypesListDisabled
  - Nome da Política de Grupo: Configurar a lista de tipos excluídos da sincronização.
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge\SyncTypesListDisabled
  - Caminho (recomendado): N/A
  - Nome do valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de exemplo:
```
SOFTWARE\Policies\Microsoft\Edge\SyncTypesListDisabled\1 = "favorites"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: SyncTypesListDisabled
  - Valor de exemplo:
``` xml
<array>
  <string>favorites</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### TLS13HardeningForLocalAnchorsEnabled
  #### Habilitar um recurso de segurança TLS 1.3 para âncoras de confiança locais (obsoleto)
  
  >OBSOLETA: Essa política está obsoleta e não funciona a partir da versão 85 do Microsoft Edge.
  #### Versões com suporte:
  - No Windows e no macOS, desde a 81 até a 85

  #### Descrição
  Essa política não funciona porque se destinava a ser um mecanismo de curto prazo para dar às empresas mais tempo para atualizar os proxies afetados.

Esta política controla um recurso de segurança no TLS 1.3 que protege as conexões contra ataques de downgrade. É compatível com versões anteriores e não afeta as conexões com servidores ou proxies TLS 1.2 compatíveis. No entanto, as versões mais antigas de alguns proxies de interceptação TLS têm uma falha de implementação, o que os torna incompatíveis.

Se você habilitar essa política ou não a definir, o Microsoft Edge habilitará estas proteções de segurança para todas as conexões.

Se você desabilitar essa política, o Microsoft Edge desabilitará estas proteções de segurança para conexões autenticadas com Certificados de Autoridade de Certificação instalados localmente. Essas proteções estão sempre ativadas para conexões autenticadas com Certificados de Autoridade de Certificação de confiança pública.

Essa política pode ser usada para testar todos os proxies afetados e atualizá-los. Espera-se que os proxies afetados falhem nas conexões com um código de erro de ERR_TLS13_DOWNGRADE_DETECTED.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: TLS13HardeningForLocalAnchorsEnabled
  - Nome da Política de Grupo: Habilite um recurso de segurança TLS 1.3 para âncoras de confiança local (obsoleta)
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do Valor: TLS13HardeningForLocalAnchorsEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: TLS13HardeningForLocalAnchorsEnabled
  - Valor de exemplo:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### TLSCipherSuiteDenyList
  #### Especificar os pacotes de codificação TLS para desabilitar
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 85 ou mais recente

  #### Descrição
  Configure a lista de pacotes de codificação que são desativados para conexões TLS.

Se você configurar essa política, a lista de pacotes de codificação configurada não será usada ao estabelecer conexões TLS.

Se você não configurar essa política, o navegador escolherá quais pacotes de codificação TLS usar.

Os valores do pacote de codificação a ser desabilitado são especificados como valores hexadecimais de 16 bits. Os valores são atribuídos pelo registro IANA (Autoridade de Números Atribuídos da Internet).

O pacote de codificação TLS 1.3 TLS_AES_128_GCM_SHA256 (0x1301) é necessário para TLS 1.3 e não pode ser desabilitado por esta política.

Essa política não afeta as conexões baseadas em QUIC. O QUIC pode ser desativado pela política [QuicAllowed](#quicallowed).

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: TLSCipherSuiteDenyList
  - Nome da Política de Grupo: Especificar os pacotes de codificação TLS para desabilitar
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (Mandatório): SOFTWARE\Policies\Microsoft\Edge\TLSCipherSuiteDenyList
  - Caminho (recomendado): N/A
  - Nome do valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de exemplo:
```
SOFTWARE\Policies\Microsoft\Edge\TLSCipherSuiteDenyList\1 = "0x1303"
SOFTWARE\Policies\Microsoft\Edge\TLSCipherSuiteDenyList\2 = "0xcca8"
SOFTWARE\Policies\Microsoft\Edge\TLSCipherSuiteDenyList\3 = "0xcca9"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: TLSCipherSuiteDenyList
  - Valor de exemplo:
``` xml
<array>
  <string>0x1303</string>
  <string>0xcca8</string>
  <string>0xcca9</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### TabFreezingEnabled
  #### Permitir congelamento das guias de plano de fundo
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 79 ou mais recente

  #### Descrição
  Controla se o Microsoft Edge pode congelar as guias que estão em segundo plano por pelo menos 5 minutos.

A tecla congelamento reduz o uso da CPU, da bateria e da memória. O Microsoft Edge usa a heurística para evitar o congelamento de guias que fazem um trabalho útil em segundo plano, como exibir notificações, reproduzir som e transmitir vídeo.

Se você habilitar ou não configurar essa política, as guias que estiverem em segundo plano por, pelo menos, 5 minutos, poderão ser congeladas.

Se você desabilitar essa política, nenhuma guia será congelada.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: TabFreezingEnabled
  - Nome da Política de Grupo: Permitir o congelamento das guias de plano de fundo
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: TabFreezingEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000000
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: TabFreezingEnabled
  - Valor de exemplo:
``` xml
<false/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### TaskManagerEndProcessEnabled
  #### Habilitar processos finais no Gerenciador de tarefas do navegador
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Se você habilitar ou não configurar essa política, os usuários poderão finalizar processos no Gerenciador de tarefas do navegador. Se você desabilitá-la, os usuários não poderão finalizar processos e o botão Finalizar processo será desabilitado no Gerenciador de tarefas do navegador.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: TaskManagerEndProcessEnabled
  - Nome da Política de Grupo: Habilitar os processos finais no Gerenciador de tarefas do navegador
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do Valor: TaskManagerEndProcessEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: TaskManagerEndProcessEnabled
  - Valor de exemplo:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### TotalMemoryLimitMb
  #### Definir o limite em megabytes de memória que uma única instância do Microsoft Edge pode usar.
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 80 ou mais recente

  #### Descrição
  Configura a quantidade de memória que uma única instância do Microsoft Edge pode usar antes que as guias comecem a ser descartadas para economizar memória. A memória usada pela guia será liberada, e a guia terá que ser recarregada quando for alternada.

Se você habilitar essa política, o navegador começará a descartar as guias para economizar memória assim que a limitação for excedida. No entanto, não há garantias de que o navegador esteja sempre sendo executado sob o limite. Qualquer valor abaixo de 1024 será arredondado para 1024.

Se você não definir essa política, o navegador só tentará economizar memória quando tiver detectado que a quantidade de memória física no computador é baixa.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Inteiro

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: TotalMemoryLimitMb
  - Nome da Política de Grupo: Define o limite em megabytes de memória que uma única instância do Microsoft Edge pode usar.
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: TotalMemoryLimitMb
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000800
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: TotalMemoryLimitMb
  - Valor de exemplo:
``` xml
<integer>2048</integer>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### TrackingPrevention
  #### Bloquear o acompanhamento de atividades de navegação na Web do usuário
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 78 ou mais recente

  #### Descrição
  Permite que você decida se deseja bloquear os sites da atividade de navegação na web do usuário.

Se você desabilitar essa política ou não a configurar, os usuários poderão definir seu próprio nível de prevenção de rastreamento.

Mapeamento das opções de política:

* TrackingPreventionOff (0) = Desativado (sem prevenção contra rastreamento)

* TrackingPreventionBasic (1) = Básico (bloqueia rastreadores nocivos, conteúdo e anúncios serão personalizados)

* TrackingPreventionBalanced (2) = Balanceado (bloqueia rastreadores e rastreadores nocivos de sites que o usuário não visitou; o conteúdo e os anúncios serão menos personalizados)

* TrackingPreventionStrict (3) = Estrito (bloqueia rastreadores nocivos e a maioria dos rastreadores de todos os sites; o conteúdo e os anúncios terão personalização mínima. Algumas partes de sites podem não funcionar.

Use as informações anteriores ao configurar essa política.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Inteiro

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo:TrackingPrevention
  - Nome da Política de Grupo: Bloquear o acompanhamento de atividades de navegação na Web do usuário
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: TrackingPrevention
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000002
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: TrackingPrevention
  - Valor de exemplo:
``` xml
<integer>2</integer>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### TranslateEnabled
  #### Habilitar traduzir
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Habilita o serviço de tradução integrado da Microsoft no Microsoft Edge.

Se você habilitar essa política, o Microsoft Edge oferecerá a funcionalidade de tradução para o usuário, mostrando um submenu de tradução integrado quando apropriado e uma opção de tradução no menu de contexto do botão direito do mouse.

Desabilite essa política para desabilitar todos os recursos internos de tradução.

Se você não configurar a política, os usuários poderão escolher se desejam ou não usar a funcionalidade de tradução.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: Sim
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: TranslateEnabled
  - Nome da Política de Grupo: Habilitar Tradução
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): Administrative Templates/Microsoft Edge - Default Settings (usuários podem substituir)/
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nome do valor: TranslateEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: TranslateEnabled
  - Valor de exemplo:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### URLAllowlist
  #### Definir uma lista de URLs permitidas
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Permite o acesso às URLs listadas, como exceções para a lista de blocos de URL.

Formata o padrão de URL de acordo com [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

Você pode usar essa política para abrir exceções para listas de bloqueio restritivas. Por exemplo, você pode incluir "*" na lista de bloqueios para bloquear todas as solicitações e, em seguida, usar essa política para permitir o acesso a uma lista limitada de URLs. Você pode usar essa política para abrir exceções a determinados esquemas, subdomínios de outros domínios, portas ou caminhos específicos.

O filtro mais específico determina se uma URL está bloqueada ou permitida. A lista permitida tem precedência sobre a lista de bloqueios.

Essa política é limitada a 1000 entradas. as entradas subsequentes serão ignoradas.

Essa política também permite que o navegador invoque automaticamente aplicativos externos registrados como manipuladores de protocolo para protocolos como "tel:" or "ssh:".

Se você não configurar essa política, não haverá nenhuma exceção para a lista de bloqueios na política [URLBlocklist](#urlblocklist).

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: URLAllowlist
  - Nome da Política de Grupo: Definir uma lista de URLs permitidas
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge\URLAllowlist
  - Caminho (recomendado): N/A
  - Nome do valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de exemplo:
```
SOFTWARE\Policies\Microsoft\Edge\URLAllowlist\1 = "contoso.com"
SOFTWARE\Policies\Microsoft\Edge\URLAllowlist\2 = "https://ssl.server.com"
SOFTWARE\Policies\Microsoft\Edge\URLAllowlist\3 = "hosting.com/good_path"
SOFTWARE\Policies\Microsoft\Edge\URLAllowlist\4 = "https://server:8080/path"
SOFTWARE\Policies\Microsoft\Edge\URLAllowlist\5 = ".exact.hostname.com"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: URLAllowlist
  - Valor de exemplo:
``` xml
<array>
  <string>contoso.com</string>
  <string>https://ssl.server.com</string>
  <string>hosting.com/good_path</string>
  <string>https://server:8080/path</string>
  <string>.exact.hostname.com</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### URLBlocklist
  #### Bloquear o acesso a uma lista de URLs
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Define uma lista de sites, com base nos padrões de URL, que estão bloqueados (os usuários não podem carregá-los).

Formata o padrão de URL de acordo com [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

Você pode definir exceções na política [URLAllowlist](#urlallowlist). Essas políticas estão limitadas a 1000 entradas. As entradas subsequentes serão ignoradas.

Observe que não é recomendável bloquear URLs "edge://* ' internas, isso que pode levar a erros inesperados.

Essa política não impede a atualização dinâmica da página por meio de JavaScript. Por exemplo, se você bloquear "contoso.com/abc", os usuários ainda poderão visitar "contoso.com" e clicar em um link para acessar "contoso.com/abc", desde que a página não atualize.

Se você não configurar essa política, nenhuma URL será bloqueada.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: URLBlocklist
  - Nome da Política de Grupo: Bloquear o acesso a uma lista de URLs
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge\URLBlocklist
  - Caminho (recomendado): N/A
  - Nome do valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de exemplo:
```
SOFTWARE\Policies\Microsoft\Edge\URLBlocklist\1 = "contoso.com"
SOFTWARE\Policies\Microsoft\Edge\URLBlocklist\2 = "https://ssl.server.com"
SOFTWARE\Policies\Microsoft\Edge\URLBlocklist\3 = "hosting.com/bad_path"
SOFTWARE\Policies\Microsoft\Edge\URLBlocklist\4 = "https://server:8080/path"
SOFTWARE\Policies\Microsoft\Edge\URLBlocklist\5 = ".exact.hostname.com"
SOFTWARE\Policies\Microsoft\Edge\URLBlocklist\6 = "file://*"
SOFTWARE\Policies\Microsoft\Edge\URLBlocklist\7 = "custom_scheme:*"
SOFTWARE\Policies\Microsoft\Edge\URLBlocklist\8 = "*"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: URLBlocklist
  - Valor de exemplo:
``` xml
<array>
  <string>contoso.com</string>
  <string>https://ssl.server.com</string>
  <string>hosting.com/bad_path</string>
  <string>https://server:8080/path</string>
  <string>.exact.hostname.com</string>
  <string>file://*</string>
  <string>custom_scheme:*</string>
  <string>*</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### UserAgentClientHintsEnabled
  #### Habilitar o recurso de Dicas do Cliente Usuário-Agente (descontinuado)
  >SUBSTITUÍDO: Essa política está preterida. Ela tem suporte no momento, mas se tornará obsoleta em uma versão futura.
  
  #### Versões com suporte:
  - No Windows e no macOS desde 86 ou mais recente

  #### Descrição
  Essa política foi descontinuada porque se destinava a ser um mecanismo de curto prazo para dar às empresas mais tempo para atualizar seu conteúdo na web se e quando fosse constatado que era incompatível com o recurso Dicas do Cliente Usuário-Agente. Não irá funcionar no Microsoft Edge versão 89.

Quando habilitada, o recurso Dicas de Cliente Agente-Usuário envia cabeçalhos granulares que fornecem informações sobre o navegador do usuário (por exemplo, a versão do navegador) e ambiente (por exemplo, a arquitetura do sistema).

Esse é um recurso aditivo, mas os novos cabeçalhos podem quebrar alguns sites que restringem os caracteres que as solicitações podem conter.

Se você habilitar ou não configurar essa política, o recurso Dicas de Cliente Agente-Usuário será habilitado. Se você desabilitar essa política, esse recurso não estará disponível.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: UserAgentClientHintsEnabled
  - Nome da Política de Grupo: Habilitar o recurso de Dicas do Cliente Usuário-Agente (descontinuada)
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do Valor: UserAgentClientHintsEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da Chave de Preferência: UserAgentClientHintsEnabled
  - Valor de exemplo:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### UserDataDir
  #### Definir o diretório de dados de usuário
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Define o diretório a ser usado para armazenar dados do usuário.

Se você habilitar essa política, o Microsoft Edge usará o diretório especificado, independentemente de o usuário ter definido o sinalizador da linha de comando “--user-data-dir”.

Se você não habilitar essa política, o caminho de perfil padrão será usado, mas o usuário pode substituí-lo usando o sinalizador “--user-data-dir”. Os usuários podem encontrar o diretório para o perfil em edge://version/under profile path.

Para evitar a perda de dados ou outros erros, não configure essa política para uma pasta raiz do volume ou para uma pasta que é usada para outros fins, porque o Microsoft Edge gerencia seu conteúdo.

Confira [https://go.microsoft.com/fwlink/?linkid=2095041](https://go.microsoft.com/fwlink/?linkid=2095041) para obter uma lista de variáveis que podem ser usadas.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: não requer a reinicialização do navegador

  #### Tipo de dados:
  - String

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: UserDataDir
  - Nome da Política de Grupo: Configurar o diretório de dados do usuário
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: UserDataDir
  - Tipo do valor: REG_SZ
  ##### Valor de exemplo:
```
"${users}/${user_name}/Edge"
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: UserDataDir
  - Valor de exemplo:
``` xml
<string>${users}/${user_name}/Edge</string>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### UserDataSnapshotRetentionLimit
  #### Limita o número de instantâneos de dados do usuário mantidos para uso no caso de uma reversão de emergência
  
  
  #### Versões com suporte:
  - No Windows desde 86 ou posterior

  #### Descrição
  Em todas as atualizações de versão principais, o Microsoft Edge criará um instantâneo das partes dos dados de navegação do usuário para usar no caso de uma emergência posterior que exija uma reversão temporária de versão. Se uma reversão temporária for executada para uma versão para a qual o usuário tenha um instantâneo correspondente, os dados no instantâneo serão restaurados. Isso permite aos usuários manter configurações como marcadores e dados de preenchimento automático.

Se você não definir essa política, o valor padrão dos três instantâneos será utilizado.

Se você definir essa política, os instantâneos antigos serão excluídos conforme necessário para respeitar o limite definido. Se você definir essa política como 0, nenhum instantâneo será retirado.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: não requer a reinicialização do navegador

  #### Tipo de dados:
  - Inteiro

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo:UserDataSnapshotRetentionLimit
  - Nome da Política de Grupo: Limita o número de instantâneos de dados do usuário mantidos para uso no caso de uma reversão de emergência
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do Valor: UserDataSnapshotRetentionLimit
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000003
```


  

  [Voltar ao início](#microsoft-edge---policies)

  ### UserFeedbackAllowed
  #### Permitir comentários do usuário
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  O Microsoft Edge usa o recurso de Comentários do Edge (habilitado por padrão) para permitir que os usuários enviem comentários, sugestões ou pesquisas de clientes, além de relatar problemas com o navegador. Além disso, por padrão, os usuários não podem desabilitar (desativar) o recurso de Comentários do Edge.

Se você habilitar essa política ou não a configurar, os usuários poderão invocar os Comentários do Edge.

Se você desabilitar essa política, os usuários não poderão invocar os Comentários do Edge.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: não requer a reinicialização do navegador

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: UserFeedbackAllowed
  - Nome da Política de Grupo: Permitir comentários do usuário
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: UserFeedbackAllowed
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: UserFeedbackAllowed
  - Valor de exemplo:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### VideoCaptureAllowed
  #### Permitir ou bloquear captura de vídeo
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Controlar se os sites podem capturar o vídeo.

Se habilitada ou não configurada (padrão), o usuário será solicitado a informar o acesso de captura de vídeo para todos os sites, exceto aqueles com URLs configuradas na lista de políticas [VideoCaptureAllowedUrls](#videocaptureallowedurls), à qual será concedido acesso sem solicitação.

Se você desabilitar essa política, o usuário não será questionado e a captura de vídeo só estará disponível para URLs configuradas na política [VideoCaptureAllowedUrls](#videocaptureallowedurls).

Essa política afeta todos os tipos de entradas de vídeo, não apenas a câmera interna.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: VideoCaptureAllowed
  - Nome da Política de Grupo: Permitir ou bloquear captura de vídeo
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: VideoCaptureAllowed
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000000
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: VideoCaptureAllowed
  - Valor de exemplo:
``` xml
<false/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### VideoCaptureAllowedUrls
  #### Sites que podem acessar dispositivos de captura de vídeo sem solicitar permissão
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Especificar sites, com base em padrões de URL, que podem usar dispositivos de captura de vídeo sem pedir permissão ao usuário. Os padrões nesta lista são comparados com a origem de segurança da URL da solicitação. Se elas corresponderem, o site recebe acesso automaticamente aos dispositivos de captura de vídeo.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: VideoCaptureAllowedUrls
  - Nome da Política de Grupo: Sites que podem acessar dispositivos de captura de vídeo sem solicitar permissão
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge\VideoCaptureAllowedUrls
  - Caminho (recomendado): N/A
  - Nome do valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de exemplo:
```
SOFTWARE\Policies\Microsoft\Edge\VideoCaptureAllowedUrls\1 = "https://www.contoso.com/"
SOFTWARE\Policies\Microsoft\Edge\VideoCaptureAllowedUrls\2 = "https://[*.]contoso.edu/"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: VideoCaptureAllowedUrls
  - Valor de exemplo:
``` xml
<array>
  <string>https://www.contoso.com/</string>
  <string>https://[*.]contoso.edu/</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### WPADQuickCheckEnabled
  #### Definir otimização de WPAD
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Permite desativar a otimização de WPAD (descoberta automática de proxy da Web) no Microsoft Edge.

Se você desabilitar essa política, a otimização WPAD será desabilitada, o que faz o navegador esperar mais por um servidor WPAD baseado em DNS.

Se você habilitar ou não configurar a política, a otimização de WPAD estará ativada.

Independente da política ser habilitada, a configuração de otimização WPAD não pode ser alterada pelos usuários.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: não requer a reinicialização do navegador

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: WPADQuickCheckEnabled
  - Nome da Política de Grupo: Definir otimização de WPAD
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: WPADQuickCheckEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: WPADQuickCheckEnabled
  - Valor de exemplo:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### WebAppInstallForceList
  #### Configura a lista de aplicativos Web instalados pela força.
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 80 ou mais recente

  #### Descrição
  Configure essa política para especificar uma lista de aplicativos Web que são instalados silenciosamente, sem interação do usuário e quais usuários não podem desinstalar ou desativar.

Cada item de lista da política é um objeto com membro obrigatório: URL (a URL do aplicativo Web a ser instalada) e 2 Membros opcionais: default_launch_container (especifica o modo de janela que o aplicativo Web abre com uma nova guia é o padrão) e o create_desktop_shortcut (verdadeiro se quiser criar atalhos para a área de trabalho do Linux e Windows).

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:
  - Dictionary

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: WebAppInstallForceList
  - Nome da Política de Grupo: Configurar a lista de aplicativos Web instalados pela força
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: WebAppInstallForceList
  - Tipo do valor: REG_SZ
  ##### Valor de exemplo:
```
SOFTWARE\Policies\Microsoft\Edge\WebAppInstallForceList = [
  {
    "create_desktop_shortcut": true, 
    "default_launch_container": "window", 
    "url": "https://www.contoso.com/maps"
  }, 
  {
    "default_launch_container": "tab", 
    "url": "https://app.contoso.edu"
  }
]
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: WebAppInstallForceList
  - Valor de exemplo:
``` xml
<key>WebAppInstallForceList</key>
<array>
  <dict>
    <key>create_desktop_shortcut</key>
    <true/>
    <key>default_launch_container</key>
    <string>window</string>
    <key>url</key>
    <string>https://www.contoso.com/maps</string>
  </dict>
  <dict>
    <key>default_launch_container</key>
    <string>tab</string>
    <key>url</key>
    <string>https://app.contoso.edu</string>
  </dict>
</array>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### WebComponentsV0Enabled
  #### Reabilitar a API de componentes Web V0 até M84 (obsoleta)
  
  >OBSOLETA: Esta política é obsoleta e não funciona após a versão 84 do Microsoft Edge.
  #### Versões com suporte:
  - No Windows e no macOS desde 80 até 84

  #### Descrição
  Essa política não funciona porque ela permitiu que esses recursos fossem reativados seletivamente até o Microsoft Edge versão 85. As APIs V0 dos componentes da web (Shadow DOM V0, elementos personalizados V0 e importações HTML) ficaram obsoletas em 2018 e foram desabilitadas por padrão a partir do Microsoft Edge versão 80.

Se você definir essa política como true, os recursos do V0 de componentes da Web serão habilitados para todos os sites.

Se você definir essa política como falsa ou não definir essa política, os recursos do V0 de componentes da Web serão desabilitados por padrão, a partir do Microsoft Edge versão 80.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: não requer a reinicialização do navegador

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: WebComponentsV0Enabled
  - Nome da Política de Grupo: Reabilitar a API de componentes Web V0 até M84 (obsoleta)
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: WebComponentsV0Enabled
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: WebComponentsV0Enabled
  - Valor de exemplo:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### WebDriverOverridesIncompatiblePolicies
  #### Permitir que o WebDriver substitua políticas incompatíveis (obsoleta)
  
  >OBSOLETA: Esta política é obsoleta e não funciona após a versão 84 do Microsoft Edge.
  #### Versões com suporte:
  - No Windows e no macOS desde 77 até 84

  #### Descrição
  Essa política não funciona porque o WebDriver agora é compatível com todas as políticas existentes.

Essa política permite que os usuários do recurso WebDriver substituam políticas que possam interferir na operação.

Atualmente essa política desabilita as políticas [SitePerProcess](#siteperprocess) e [IsolateOrigins](#isolateorigins).

Se a política estiver habilitada, o WebDriver poderá substituir políticas incompatíveis.
Se a política estiver desabilitada ou não configurada, o WebDriver não terá permissão para substituir as políticas incompatíveis.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: não requer a reinicialização do navegador

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: WebDriverOverridesIncompatiblePolicies
  - Nome da Política de Grupo: Permitir que o WebDriver substitua políticas incompatíveis (obsoleta)
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: WebDriverOverridesIncompatiblePolicies
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: WebDriverOverridesIncompatiblePolicies
  - Valor de exemplo:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### WebRtcLocalIpsAllowedUrls
  #### Gerenciar a exposição de endereço IP local por WebRTC
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 80 ou mais recente

  #### Descrição
  Especifica uma lista de origens (URLs) ou padrões de nome de host (como "*contoso.com*") para os quais o endereço IP local deve ser exposto por WebRTC.

Se você habilitar essa política e definir uma lista de origens (URLs) ou padrões de nome de host, quando edge://flags/#enable-webrtc-hide-local-ips-with-mdns estiver habilitado, o WebRTC exibirá o endereço IP local para casos que correspondam a padrões na lista.

Se você desabilitar ou não configurar essa política e edge://flags/#enable-webrtc-hide-local-ips-with-mdns estiver habilitado, o WebRTC não exporá os endereços IP locais. O endereço IP local é escondido com um nome de host do mDNS.

Se você habilitar, desabilitar ou não configurar essa política, e edge://flags/#enable-webrtc-hide-local-ips-with-mdns estiver desabilitado, o WebRTC exibirá endereços IP locais.

Observe que essa política enfraquece a proteção de endereços IP locais que podem ser necessários para os administradores.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: não requer a reinicialização do navegador

  #### Tipo de dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: WebRtcLocalIpsAllowedUrls
  - Nome da Política de Grupo: Gerenciar a exposição de endereço IP local não WebRTC
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge\WebRtcLocalIpsAllowedUrls
  - Caminho (recomendado): N/A
  - Nome do valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de exemplo:
```
SOFTWARE\Policies\Microsoft\Edge\WebRtcLocalIpsAllowedUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\WebRtcLocalIpsAllowedUrls\2 = "*contoso.com*"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: WebRtcLocalIpsAllowedUrls
  - Valor de exemplo:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>*contoso.com*</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### WebRtcLocalhostIpHandling
  #### Restringir a exposição de endereço IP local por WebRTC
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Permite definir se o WebRTC expõe ou não o endereço IP local do usuário.

Se você definir essa política como "AllowAllInterfaces" ou "AllowPublicAndPrivateInterfaces", o WebRTC vai expor o endereço IP local.

Se você definir essa política como "AllowPublicInterfaceOnly" ou "DisableNonProxiedUdp", o WebRTC não vai expor o endereço IP local.

Se você não definir essa política, ou se a desabilitada, WebRTC exporá o endereço IP local.

Mapeamento das opções de política:

* AllowAllInterfaces (padrão) = Permitir todas as interfaces. Isso expõe o endereço IP local.

* AllowPublicAndPrivateInterfaces (default_public_and_private_interfaces) = Permitir a interface pública e privada por meio da rota http padrão. Isso expõe o endereço IP local.

* AllowPublicInterfaceOnly (default_public_interface_only) = Permitir interface pública por rota http padrão. Isso não expõe o endereço IP local.

* DisableNonProxiedUdp (disable_non_proxied_udp) = Usar o TCP, a menos que o servidor proxy dê suporte a UDP. Isso não expõe o endereço IP local.

Use as informações anteriores ao configurar essa política.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: não requer a reinicialização do navegador

  #### Tipo de dados:
  - String

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: WebRtcLocalhostIpHandling
  - Nome da Política de Grupo: Restringir a exposição de endereço IP local por WebRTC
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: WebRtcLocalhostIpHandling
  - Tipo do valor: REG_SZ
  ##### Valor de exemplo:
```
"default"
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: WebRtcLocalhostIpHandling
  - Valor de exemplo:
``` xml
<string>default</string>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### WebRtcUdpPortRange
  #### Restringir o intervalo de portas UDP locais usado por WebRTC
  
  
  #### Versões com suporte:
  - No Windows e no macOS desde 77 ou mais recente

  #### Descrição
  Restringe o intervalo de portas UDP usado por WebRTC para um intervalo de portas especificado (pontos de extremidade inclusos).

Ao configurar essa política, você especifica o intervalo de portas UDP locais que WebRTC pode usar.

Se você não configurar essa política, ou se a definir como uma cadeia de caracteres vazia ou intervalo de portas inválida, WebRTC poderá usar qualquer porta UDP local disponível.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: não requer a reinicialização do navegador

  #### Tipo de dados:
  - String

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome Exclusivo da Política de Grupo: WebRtcUdpPortRange
  - Nome da Política de Grupo: Restringir o intervalo de portas UDP locais usado por WebRTC
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: WebRtcUdpPortRange
  - Tipo do valor: REG_SZ
  ##### Valor de exemplo:
```
"10000-11999"
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: WebRtcUdpPortRange
  - Valor de exemplo:
``` xml
<string>10000-11999</string>
```
  

  [Voltar ao início](#microsoft-edge---policies)

  ### WinHttpProxyResolverEnabled
  #### Usar o solucionador de proxy do Windows (preterida)
  >SUBSTITUÍDO: Essa política está preterida. Ela tem suporte no momento, mas se tornará obsoleta em uma versão futura.
  
  #### Versões com suporte:
  - No Windows desde 84 ou posterior

  #### Descrição
  Essa política foi preterida porque será substituída por um recurso semelhante em uma versão futura, confira https://crbug.com/1032820.

Use o Windows para resolver proxies de todas as redes de navegador, em vez do resolvedor de proxy integrado no Microsoft Edge. O resolvedor de proxy do Windows habilita recursos de proxy do Windows, como DirectAccess/NRPT.

Essa política acompanha os problemas descritos por https://crbug.com/644030. Isso faz com que os arquivos PAC sejam obtidos e executados pelo código do Windows, incluindo os arquivos PAC definidos pela política [ProxyPacUrl](#proxypacurl). Como as buscas de rede para o arquivo PAC ocorrem por meio do Windows em vez de código do Microsoft Edge, políticas de rede como [DnsOverHttpsMode](#dnsoverhttpsmode) não se aplicarão às buscas de rede para um arquivo PAC.

Se você habilitar essa política, o solucionador de proxy do Windows será utilizado.

Se você desabilitar ou não configurar essa política, o solucionador de proxy do Microsoft Edge será utilizado.

  #### Recursos compatíveis:
  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: não requer a reinicialização do navegador

  #### Tipo de dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da Política de Grupo: WinHttpProxyResolverEnabled
  - Nome da Política de Grupo: usar o solucionador de proxy do Windows (preterida)
  - Caminho da Política de Grupo (obrigatório): Administrative Templates/Microsoft Edge/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da Política de Grupo: MSEdge.admx
  ##### Configurações de registro do Windows
  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (recomendado): N/A
  - Nome do valor: WinHttpProxyResolverEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de exemplo:
```
0x00000001
```


  

  [Voltar ao início](#microsoft-edge---policies)


## Consulte também
- [Configurar o Microsoft Edge](configure-microsoft-edge.md)
- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Blog de linhas de base de segurança da Microsoft](https://techcommunity.microsoft.com/t5/microsoft-security-baselines/bg-p/Microsoft-Security-Baselines)
