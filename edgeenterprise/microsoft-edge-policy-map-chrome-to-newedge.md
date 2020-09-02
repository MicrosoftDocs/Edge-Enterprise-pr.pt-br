---
title: Mapeamento de política do Google Chrome para o Microsoft Edge
ms.author: brianalt
author: brianalt
manager: srugh
ms.date: 02/10/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Mapeamento de política do Google Chrome para o Microsoft Edge
ms.openlocfilehash: 73e3cd542e873ff5546ba4d31515ddd39757d0c0
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979184"
---
# Mapeamento de política do Google Chrome para o Microsoft Edge

Este artigo mapeia as políticas do Google Chrome para as políticas relevantes do Microsoft Edge com suporte na versão 80. Para as políticas herdadas do Microsoft Edge, confira o artigo [Microsoft Edge Legacy para mapeamento de política do Microsoft Edge](microsoft-edge-policy-map-legacy-to-newedge.md).

> [!NOTE]
> O mapeamento fornecido abaixo destina-se a ajudar com a implantação inicial do Microsoft Edge versão 80. Para obter uma lista definitiva das políticas mais recentes, consulte:
> - [Referência de política do navegador](microsoft-edge-policies.md)
> - [Referência da política de atualização](microsoft-edge-update-policies.md)

## Mapa de política do Google Chrome para o Microsoft Edge

|Política de Chrome do Google|Políticas do Microsoft Edge|
|-|-|
|[AbusiveExperienceInterventionEnforce](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=AbusiveExperienceInterventionEnforce)|Não Aplicável|
|[AdsSettingForIntrusiveAdsSites](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=AdsSettingForIntrusiveAdsSites)|[AdsSettingForIntrusiveAdsSites](https://docs.microsoft.com/deployedge/microsoft-edge-policies#adssettingforintrusiveadssites)|
|[AllowCrossOriginAuthPrompt](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=AllowCrossOriginAuthPrompt)|[AllowCrossOriginAuthPrompt](https://docs.microsoft.com/deployedge/microsoft-edge-policies#allowcrossoriginauthprompt)|
|[AllowDeletingBrowserHistory](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=AllowDeletingBrowserHistory)|[AllowDeletingBrowserHistory](https://docs.microsoft.com/deployedge/microsoft-edge-policies#allowdeletingbrowserhistory)|
|[AllowDinosaurEasterEgg](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=AllowDinosaurEasterEgg)|Não Aplicável|
|[AllowedDomainsForApps](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=AllowedDomainsForApps)|Não Aplicável|
|[AllowFileSelectionDialogs](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=AllowFileSelectionDialogs)|[AllowFileSelectionDialogs](https://docs.microsoft.com/deployedge/microsoft-edge-policies#allowfileselectiondialogs)|
|[AllowOutdatedPlugins](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=AllowOutdatedPlugins)|Não Aplicável|
|[AllowPasswordProtectedFiles](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=AllowPasswordProtectedFiles)|Não Aplicável|
|[AllowPopupsDuringPageUnload](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=AllowPopupsDuringPageUnload)|[AllowPopupsDuringPageUnload](https://docs.microsoft.com/deployedge/microsoft-edge-policies#allowpopupsduringpageunload)|
|[AllowSyncXHRInPageDismissal](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=AllowSyncXHRInPageDismissal)|[AllowSyncXHRInPageDismissal](https://docs.microsoft.com/deployedge/microsoft-edge-policies#allowsyncxhrinpagedismissal)|
|[AlternateErrorPagesEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=AlternateErrorPagesEnabled)|[AlternateErrorPagesEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#alternateerrorpagesenabled)|
|[AlternativeBrowserParameters](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=AlternativeBrowserParameters)|Ver o Microsoft Edge com o modo IE|
|[AlternativeBrowserPath](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=AlternativeBrowserPath)|Ver o Microsoft Edge com o modo IE|
|[AlwaysOpenPdfExternally](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=AlwaysOpenPdfExternally)|[AlwaysOpenPdfExternally](https://docs.microsoft.com/deployedge/microsoft-edge-policies#alwaysopenpdfexternally)|
|[AmbientAuthenticationInPrivateModesEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=AmbientAuthenticationInPrivateModesEnabled)|Não Aplicável|
|[ApplicationLocaleValue](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ApplicationLocaleValue)|[ApplicationLocaleValue](https://docs.microsoft.com/deployedge/microsoft-edge-policies#applicationlocalevalue)|
|[AudioCaptureAllowed](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=AudioCaptureAllowed)|[AudioCaptureAllowed](https://docs.microsoft.com/deployedge/microsoft-edge-policies#audiocaptureallowed)|
|[AudioCaptureAllowedUrls](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=AudioCaptureAllowedUrls)|[AudioCaptureAllowedUrls](https://docs.microsoft.com/deployedge/microsoft-edge-policies#audiocaptureallowedurls)|
|[AudioSandboxEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=AudioSandboxEnabled)|Não Aplicável|
|[AuthNegotiateDelegateByKdcPolicy](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=AuthNegotiateDelegateByKdcPolicy)|Não Aplicável|
|[AuthNegotiateDelegateWhitelist](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=AuthNegotiateDelegateWhitelist)|[AuthNegotiateDelegateAllowlist](https://docs.microsoft.com/deployedge/microsoft-edge-policies#authnegotiatedelegateallowlist)|
|[AuthSchemes](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=AuthSchemes)|[AuthSchemes](https://docs.microsoft.com/deployedge/microsoft-edge-policies#authschemes)|
|[AuthServerWhitelist](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=AuthServerWhitelist)|[AuthServerAllowlist](https://docs.microsoft.com/deployedge/microsoft-edge-policies#authserverallowlist)|
|[AutofillAddressEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=AutofillAddressEnabled)|[AutofillAddressEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#autofilladdressenabled)|
|[AutofillCreditCardEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=AutofillCreditCardEnabled)|[AutofillCreditCardEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#autofillcreditcardenabled)|
|[AutoplayAllowed](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=AutoplayAllowed)|[AutoplayAllowed](https://docs.microsoft.com/deployedge/microsoft-edge-policies#autoplayallowed)|
|[AutoplayWhitelist](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=AutoplayWhitelist)|Não Aplicável|
|[AutoSelectCertificateForUrls](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=AutoSelectCertificateForUrls)|[AutoSelectCertificateForUrls](https://docs.microsoft.com/deployedge/microsoft-edge-policies#autoselectcertificateforurls)|
|[BackgroundModeEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=BackgroundModeEnabled)|[BackgroundModeEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#backgroundmodeenabled)|
|[BlockExternalExtensions](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=BlockExternalExtensions)|Não Aplicável|
|[BlockLargeFileTransfer](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=BlockLargeFileTransfer)|Não Aplicável|
|[BlockThirdPartyCookies](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=BlockThirdPartyCookies)|[BlockThirdPartyCookies](https://docs.microsoft.com/deployedge/microsoft-edge-policies#blockthirdpartycookies)|
|[BookmarkBarEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=BookmarkBarEnabled)|[FavoritesBarEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#favoritesbarenabled)|
|[BrowserAddPersonEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=BrowserAddPersonEnabled)|[BrowserAddProfileEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#browseraddprofileenabled)|
|[BrowserGuestModeEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=BrowserGuestModeEnabled)|[BrowserGuestModeEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#browserguestmodeenabled)|
|[BrowserGuestModeEnforced](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=BrowserGuestModeEnforced)|Não Aplicável|
|[BrowserNetworkTimeQueriesEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=BrowserNetworkTimeQueriesEnabled)|[BrowserNetworkTimeQueriesEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#browsernetworktimequeriesenabled)|
|[BrowserSignin](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=BrowserSignin)|[BrowserSignin](https://docs.microsoft.com/deployedge/microsoft-edge-policies#browsersignin)|
|[BrowserSwitcherChromeParameters](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=BrowserSwitcherChromeParameters)|Ver o Microsoft Edge com o modo IE|
|[BrowserSwitcherChromePath](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=BrowserSwitcherChromePath)|Ver o Microsoft Edge com o modo IE|
|[BrowserSwitcherDelay](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=BrowserSwitcherDelay)|Ver o Microsoft Edge com o modo IE|
|[BrowserSwitcherEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=BrowserSwitcherEnabled)|Ver o Microsoft Edge com o modo IE|
|[BrowserSwitcherExternalGreylistUrl](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=BrowserSwitcherExternalGreylistUrl)|Ver o Microsoft Edge com o modo IE|
|[BrowserSwitcherExternalSitelistUrl](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=BrowserSwitcherExternalSitelistUrl)|Ver o Microsoft Edge com o modo IE|
|[BrowserSwitcherKeepLastChromeTab](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=BrowserSwitcherKeepLastChromeTab)|Ver o Microsoft Edge com o modo IE|
|[BrowserSwitcherUrlGreylist](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=BrowserSwitcherUrlGreylist)|Ver o Microsoft Edge com o modo IE|
|[BrowserSwitcherUrlList](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=BrowserSwitcherUrlList)|Ver o Microsoft Edge com o modo IE|
|[BrowserSwitcherUseIeSitelist](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=BrowserSwitcherUseIeSitelist)|Ver o Microsoft Edge com o modo IE|
|[BuiltInDnsClientEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=BuiltInDnsClientEnabled)|[BuiltInDnsClientEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#builtindnsclientenabled)|
|[CertificateTransparencyEnforcementDisabledForCas](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=CertificateTransparencyEnforcementDisabledForCas)|[CertificateTransparencyEnforcementDisabledForCas](https://docs.microsoft.com/deployedge/microsoft-edge-policies#certificatetransparencyenforcementdisabledforcas)|
|[CertificateTransparencyEnforcementDisabledForLegacyCas](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=CertificateTransparencyEnforcementDisabledForLegacyCas)|[CertificateTransparencyEnforcementDisabledForLegacyCas](https://docs.microsoft.com/deployedge/microsoft-edge-policies#certificatetransparencyenforcementdisabledforlegacycas)|
|[CertificateTransparencyEnforcementDisabledForUrls](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=CertificateTransparencyEnforcementDisabledForUrls)|[CertificateTransparencyEnforcementDisabledForUrls](https://docs.microsoft.com/deployedge/microsoft-edge-policies#certificatetransparencyenforcementdisabledforurls)|
|[CheckContentCompliance](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=CheckContentCompliance)|Não Aplicável|
|[ChromeCleanupEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ChromeCleanupEnabled)|Não Aplicável|
|[ChromeCleanupReportingEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ChromeCleanupReportingEnabled)|Não Aplicável|
|[ClickToCallEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ClickToCallEnabled)|Não Aplicável|
|[CloudExtensionRequestEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=CloudExtensionRequestEnabled)|Não Aplicável|
|[CloudManagementEnrollmentMandatory](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=CloudManagementEnrollmentMandatory)|Não Aplicável|
|[CloudManagementEnrollmentToken](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=CloudManagementEnrollmentToken)|Não Aplicável|
|[CloudPolicyOverridesPlatformPolicy](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=CloudPolicyOverridesPlatformPolicy)|Não Aplicável|
|[CloudPrintProxyEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=CloudPrintProxyEnabled)|Não Aplicável|
|[CloudPrintSubmitEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=CloudPrintSubmitEnabled)|Não Aplicável|
|[CloudReportingEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=CloudReportingEnabled)|Não Aplicável|
|[CoalesceH2ConnectionsWithClientCertificatesForHosts](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=CoalesceH2ConnectionsWithClientCertificatesForHosts)|[CoalesceH2ConnectionsWithClientCertificatesForHosts](https://docs.microsoft.com/deployedge/microsoft-edge-policies#coalesceh2connectionswithclientcertificatesforhosts)|
|[CommandLineFlagSecurityWarningsEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=CommandLineFlagSecurityWarningsEnabled)|[CommandLineFlagSecurityWarningsEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#commandlineflagsecuritywarningsenabled)|
|[ComponentUpdatesEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ComponentUpdatesEnabled)|[ComponentUpdatesEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#componentupdatesenabled)|
|[CookiesAllowedForUrls](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=CookiesAllowedForUrls)|[CookiesAllowedForUrls](https://docs.microsoft.com/deployedge/microsoft-edge-policies#cookiesallowedforurls)|
|[CookiesBlockedForUrls](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=CookiesBlockedForUrls)|[CookiesBlockedForUrls](https://docs.microsoft.com/deployedge/microsoft-edge-policies#cookiesblockedforurls)|
|[CookiesSessionOnlyForUrls](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=CookiesSessionOnlyForUrls)|[CookiesSessionOnlyForUrls](https://docs.microsoft.com/deployedge/microsoft-edge-policies#cookiessessiononlyforurls)|
|[CorsLegacyModeEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=CorsLegacyModeEnabled)|Não Aplicável|
|[CorsMitigationList](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=CorsMitigationList)|Não Aplicável|
|[DefaultBrowserSettingEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DefaultBrowserSettingEnabled)|[DefaultBrowserSettingEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#defaultbrowsersettingenabled)|
|[DefaultCookiesSetting](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DefaultCookiesSetting)|[DefaultCookiesSetting](https://docs.microsoft.com/deployedge/microsoft-edge-policies#defaultcookiessetting)|
|[DefaultDownloadDirectory](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DefaultDownloadDirectory)|Não Aplicável|
|[DefaultGeolocationSetting](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DefaultGeolocationSetting)|[DefaultGeolocationSetting](https://docs.microsoft.com/deployedge/microsoft-edge-policies#defaultgeolocationsetting)|
|[DefaultImagesSetting](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DefaultImagesSetting)|[DefaultImagesSetting](https://docs.microsoft.com/deployedge/microsoft-edge-policies#defaultimagessetting)|
|[DefaultInsecureContentSetting](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DefaultInsecureContentSetting)|[DefaultInsecureContentSetting](https://docs.microsoft.com/deployedge/microsoft-edge-policies#defaultinsecurecontentsetting)|
|[DefaultJavaScriptSetting](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DefaultJavaScriptSetting)|[DefaultJavaScriptSetting](https://docs.microsoft.com/deployedge/microsoft-edge-policies#defaultjavascriptsetting)|
|[DefaultNotificationsSetting](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DefaultNotificationsSetting)|[DefaultNotificationsSetting](https://docs.microsoft.com/deployedge/microsoft-edge-policies#defaultnotificationssetting)|
|[DefaultPluginsSetting](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DefaultPluginsSetting)|[DefaultPluginsSetting](https://docs.microsoft.com/deployedge/microsoft-edge-policies#defaultpluginssetting)|
|[DefaultPopupsSetting](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DefaultPopupsSetting)|[DefaultPopupsSetting](https://docs.microsoft.com/deployedge/microsoft-edge-policies#defaultpopupssetting)|
|[DefaultPrinterSelection](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DefaultPrinterSelection)|[DefaultPrinterSelection](https://docs.microsoft.com/deployedge/microsoft-edge-policies#defaultprinterselection)|
|[DefaultSearchProviderAlternateURLs](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DefaultSearchProviderAlternateURLs)|Não Aplicável|
|[DefaultSearchProviderEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DefaultSearchProviderEnabled)|[DefaultSearchProviderEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#defaultsearchproviderenabled)|
|[DefaultSearchProviderEncodings](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DefaultSearchProviderEncodings)|[DefaultSearchProviderEncodings](https://docs.microsoft.com/deployedge/microsoft-edge-policies#defaultsearchproviderencodings)|
|[DefaultSearchProviderIconURL](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DefaultSearchProviderIconURL)|Não Aplicável|
|[DefaultSearchProviderImageURL](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DefaultSearchProviderImageURL)|[DefaultSearchProviderImageURL](https://docs.microsoft.com/deployedge/microsoft-edge-policies#defaultsearchproviderimageurl)|
|[DefaultSearchProviderImageURLPostParams](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DefaultSearchProviderImageURLPostParams)|[DefaultSearchProviderImageURLPostParams](https://docs.microsoft.com/deployedge/microsoft-edge-policies#defaultsearchproviderimageurlpostparams)|
|[DefaultSearchProviderKeyword](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DefaultSearchProviderKeyword)|[DefaultSearchProviderKeyword](https://docs.microsoft.com/deployedge/microsoft-edge-policies#defaultsearchproviderkeyword)|
|[DefaultSearchProviderName](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DefaultSearchProviderName)|[DefaultSearchProviderName](https://docs.microsoft.com/deployedge/microsoft-edge-policies#defaultsearchprovidername)|
|[DefaultSearchProviderNewTabURL](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DefaultSearchProviderNewTabURL)|Não Aplicável|
|[DefaultSearchProviderSearchURL](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DefaultSearchProviderSearchURL)|[DefaultSearchProviderSearchURL](https://docs.microsoft.com/deployedge/microsoft-edge-policies#defaultsearchprovidersearchurl)|
|[DefaultSearchProviderSearchURLPostParams](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DefaultSearchProviderSearchURLPostParams)|Não Aplicável|
|[DefaultSearchProviderSuggestURL](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DefaultSearchProviderSuggestURL)|[DefaultSearchProviderSuggestURL](https://docs.microsoft.com/deployedge/microsoft-edge-policies#defaultsearchprovidersuggesturl)|
|[DefaultSearchProviderSuggestURLPostParams](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DefaultSearchProviderSuggestURLPostParams)|Não Aplicável|
|[DefaultWebBluetoothGuardSetting](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DefaultWebBluetoothGuardSetting)|[DefaultWebBluetoothGuardSetting](https://docs.microsoft.com/deployedge/microsoft-edge-policies#defaultwebbluetoothguardsetting)|
|[DefaultWebUsbGuardSetting](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DefaultWebUsbGuardSetting)|[DefaultWebUsbGuardSetting](https://docs.microsoft.com/deployedge/microsoft-edge-policies#defaultwebusbguardsetting)|
|[DelayDeliveryUntilVerdict](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DelayDeliveryUntilVerdict)|Não Aplicável|
|[DeveloperToolsAvailability](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DeveloperToolsAvailability)|[DeveloperToolsAvailability](https://docs.microsoft.com/deployedge/microsoft-edge-policies#developertoolsavailability)|
|[Disable3DAPIs](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=Disable3DAPIs)|[Disable3DAPIs](https://docs.microsoft.com/deployedge/microsoft-edge-policies#disable3dapis)|
|[DisableAuthNegotiateCnameLookup](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DisableAuthNegotiateCnameLookup)|[DisableAuthNegotiateCnameLookup](https://docs.microsoft.com/deployedge/microsoft-edge-policies#disableauthnegotiatecnamelookup)|
|[DisablePrintPreview](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DisablePrintPreview)|[UseSystemPrintDialog](https://docs.microsoft.com/deployedge/microsoft-edge-policies#usesystemprintdialog)|
|[DisableSafeBrowsingProceedAnyway](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DisableSafeBrowsingProceedAnyway)|[PreventSmartScreenPromptOverride](https://docs.microsoft.com/deployedge/microsoft-edge-policies#preventsmartscreenpromptoverride)|
|[DisableScreenshots](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DisableScreenshots)|[DisableScreenshots](https://docs.microsoft.com/deployedge/microsoft-edge-policies#disablescreenshots)|
|[DiskCacheDir](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DiskCacheDir)|[DiskCacheDir](https://docs.microsoft.com/deployedge/microsoft-edge-policies#diskcachedir)|
|[DiskCacheSize](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DiskCacheSize)|[DiskCacheSize](https://docs.microsoft.com/deployedge/microsoft-edge-policies#diskcachesize)|
|[DNSInterceptionChecksEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DNSInterceptionChecksEnabled)|[DNSInterceptionChecksEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#dnsinterceptionchecksenabled)|
|[DnsOverHttpsMode](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DnsOverHttpsMode)|Não Aplicável|
|[DnsOverHttpsTemplates](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DnsOverHttpsTemplates)|Não Aplicável|
|[DownloadDirectory](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DownloadDirectory)|[DownloadDirectory](https://docs.microsoft.com/deployedge/microsoft-edge-policies#downloaddirectory)|
|[DownloadRestrictions](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DownloadRestrictions)|[DownloadRestrictions](https://docs.microsoft.com/deployedge/microsoft-edge-policies#downloadrestrictions)|
|[EditBookmarksEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=EditBookmarksEnabled)|[EditFavoritesEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#editfavoritesenabled)|
|[EnableAuthNegotiatePort](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=EnableAuthNegotiatePort)|[EnableAuthNegotiatePort](https://docs.microsoft.com/deployedge/microsoft-edge-policies#enableauthnegotiateport)|
|[EnableDeprecatedWebPlatformFeatures](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=EnableDeprecatedWebPlatformFeatures)|[EnableDeprecatedWebPlatformFeatures](https://docs.microsoft.com/deployedge/microsoft-edge-policies#enabledeprecatedwebplatformfeatures)|
|[EnableMediaRouter](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=EnableMediaRouter)|[EnableMediaRouter](https://docs.microsoft.com/deployedge/microsoft-edge-policies#enablemediarouter)|
|[EnableOnlineRevocationChecks](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=EnableOnlineRevocationChecks)|[EnableOnlineRevocationChecks](https://docs.microsoft.com/deployedge/microsoft-edge-policies#enableonlinerevocationchecks)|
|[EnterpriseHardwarePlatformAPIEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=EnterpriseHardwarePlatformAPIEnabled)|[EnterpriseHardwarePlatformAPIEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#enterprisehardwareplatformapienabled)|
|[ExtensionAllowedTypes](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ExtensionAllowedTypes)|[ExtensionAllowedTypes](https://docs.microsoft.com/deployedge/microsoft-edge-policies#extensionallowedtypes)|
|[ExtensionInstallBlacklist](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ExtensionInstallBlacklist)|[ExtensionInstallBlocklist](https://docs.microsoft.com/deployedge/microsoft-edge-policies#extensioninstallblocklist)|
|[ExtensionInstallForcelist](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ExtensionInstallForcelist)|[ExtensionInstallForcelist](https://docs.microsoft.com/deployedge/microsoft-edge-policies#extensioninstallforcelist)|
|[ExtensionInstallListsMergeEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ExtensionInstallListsMergeEnabled)|Não Aplicável|
|[ExtensionInstallSources](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ExtensionInstallSources)|[ExtensionInstallSources](https://docs.microsoft.com/deployedge/microsoft-edge-policies#extensioninstallsources)|
|[ExtensionInstallWhitelist](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ExtensionInstallWhitelist)|[ExtensionInstallAllowlist](https://docs.microsoft.com/deployedge/microsoft-edge-policies#extensioninstallallowlist)|
|[ExtensionSettings](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ExtensionSettings)|[ExtensionSettings](https://docs.microsoft.com/deployedge/microsoft-edge-policies#extensionsettings)|
|[ExternalProtocolDialogShowAlwaysOpenCheckbox](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ExternalProtocolDialogShowAlwaysOpenCheckbox)|[ExternalProtocolDialogShowAlwaysOpenCheckbox](https://docs.microsoft.com/deployedge/microsoft-edge-policies#externalprotocoldialogshowalwaysopencheckbox)|
|[ForceEphemeralProfiles](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ForceEphemeralProfiles)|[ForceEphemeralProfiles](https://docs.microsoft.com/deployedge/microsoft-edge-policies#forceephemeralprofiles)|
|[ForceGoogleSafeSearch](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ForceGoogleSafeSearch)|[ForceGoogleSafeSearch](https://docs.microsoft.com/deployedge/microsoft-edge-policies#forcegooglesafesearch)|
|[ForceNetworkInProcess](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ForceNetworkInProcess)|[ForceNetworkInProcess](https://docs.microsoft.com/deployedge/microsoft-edge-policies#forcenetworkinprocess)|
|[ForceYouTubeRestrict](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ForceYouTubeRestrict)|[ForceYouTubeRestrict](https://docs.microsoft.com/deployedge/microsoft-edge-policies#forceyoutuberestrict)|
|[FullscreenAllowed](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=FullscreenAllowed)|[FullscreenAllowed](https://docs.microsoft.com/deployedge/microsoft-edge-policies#fullscreenallowed)|
|[GloballyScopeHTTPAuthCacheEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=GloballyScopeHTTPAuthCacheEnabled)|Não Aplicável|
|[HardwareAccelerationModeEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=HardwareAccelerationModeEnabled)|[HardwareAccelerationModeEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#hardwareaccelerationmodeenabled)|
|[HideWebStoreIcon](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=HideWebStoreIcon)|Não Aplicável|
|[HomepageIsNewTabPage](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=HomepageIsNewTabPage)|[HomepageIsNewTabPage](https://docs.microsoft.com/deployedge/microsoft-edge-policies#homepageisnewtabpage)|
|[HomepageLocation](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=HomepageLocation)|[HomepageLocation](https://docs.microsoft.com/deployedge/microsoft-edge-policies#homepagelocation)|
|[HSTSPolicyBypassList](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=HSTSPolicyBypassList)|[HSTSPolicyBypassList](https://docs.microsoft.com/deployedge/microsoft-edge-policies#hstspolicybypasslist)|
|[ImagesAllowedForUrls](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ImagesAllowedForUrls)|[ImagesAllowedForUrls](https://docs.microsoft.com/deployedge/microsoft-edge-policies#imagesallowedforurls)|
|[ImagesBlockedForUrls](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ImagesBlockedForUrls)|[ImagesBlockedForUrls](https://docs.microsoft.com/deployedge/microsoft-edge-policies#imagesblockedforurls)|
|[ImportAutofillFormData](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ImportAutofillFormData)|[ImportAutofillFormData](https://docs.microsoft.com/deployedge/microsoft-edge-policies#importautofillformdata)|
|[ImportBookmarks](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ImportBookmarks)|[ImportFavorites](https://docs.microsoft.com/deployedge/microsoft-edge-policies#importfavorites)|
|[ImportHistory](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ImportHistory)|[ImportHistory](https://docs.microsoft.com/deployedge/microsoft-edge-policies#importhistory)|
|[ImportHomepage](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ImportHomepage)|[ImportHomepage](https://docs.microsoft.com/deployedge/microsoft-edge-policies#importhomepage)|
|[ImportSavedPasswords](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ImportSavedPasswords)|[ImportSavedPasswords](https://docs.microsoft.com/deployedge/microsoft-edge-policies#importsavedpasswords)|
|[ImportSearchEngine](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ImportSearchEngine)|[ImportSearchEngine](https://docs.microsoft.com/deployedge/microsoft-edge-policies#importsearchengine)|
|[IncognitoModeAvailability](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=IncognitoModeAvailability)|[InPrivateModeAvailability](https://docs.microsoft.com/deployedge/microsoft-edge-policies#inprivatemodeavailability)|
|[InsecureContentAllowedForUrls](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=InsecureContentAllowedForUrls)|[InsecureContentAllowedForUrls](https://docs.microsoft.com/deployedge/microsoft-edge-policies#insecurecontentallowedforurls)|
|[InsecureContentBlockedForUrls](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=InsecureContentBlockedForUrls)|[InsecureContentBlockedForUrls](https://docs.microsoft.com/deployedge/microsoft-edge-policies#insecurecontentblockedforurls)|
|[IsolateOrigins](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=IsolateOrigins)|[IsolateOrigins](https://docs.microsoft.com/deployedge/microsoft-edge-policies#isolateorigins)|
|[JavaScriptAllowedForUrls](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=JavaScriptAllowedForUrls)|[JavaScriptAllowedForUrls](https://docs.microsoft.com/deployedge/microsoft-edge-policies#javascriptallowedforurls)|
|[JavaScriptBlockedForUrls](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=JavaScriptBlockedForUrls)|[JavaScriptBlockedForUrls](https://docs.microsoft.com/deployedge/microsoft-edge-policies#javascriptblockedforurls)|
|[LegacySameSiteCookieBehaviorEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=LegacySameSiteCookieBehaviorEnabled)|[LegacySameSiteCookieBehaviorEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#legacysamesitecookiebehaviorenabled)|
|[LegacySameSiteCookieBehaviorEnabledForDomainList](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=LegacySameSiteCookieBehaviorEnabledForDomainList)|[LegacySameSiteCookieBehaviorEnabledForDomainList](https://docs.microsoft.com/deployedge/microsoft-edge-policies#legacysamesitecookiebehaviorenabledfordomainlist)|
|[LocalDiscoveryEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=LocalDiscoveryEnabled)|Não Aplicável|
|[ManagedBookmarks](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ManagedBookmarks)|[ManagedFavorites](https://docs.microsoft.com/deployedge/microsoft-edge-policies#managedfavorites)|
|[MaxConnectionsPerProxy](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=MaxConnectionsPerProxy)|[MaxConnectionsPerProxy](https://docs.microsoft.com/deployedge/microsoft-edge-policies#maxconnectionsperproxy)|
|[MaxInvalidationFetchDelay](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=MaxInvalidationFetchDelay)|Não Aplicável|
|[MediaRouterCastAllowAllIPs](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=MediaRouterCastAllowAllIPs)|[MediaRouterCastAllowAllIPs](https://docs.microsoft.com/deployedge/microsoft-edge-policies#mediaroutercastallowallips)|
|[MetricsReportingEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=MetricsReportingEnabled)|[MetricsReportingEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#metricsreportingenabled)|
|[NativeMessagingBlacklist](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=NativeMessagingBlacklist)|[NativeMessagingBlocklist](https://docs.microsoft.com/deployedge/microsoft-edge-policies#nativemessagingblocklist)|
|[NativeMessagingUserLevelHosts](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=NativeMessagingUserLevelHosts)|[NativeMessagingUserLevelHosts](https://docs.microsoft.com/deployedge/microsoft-edge-policies#nativemessaginguserlevelhosts)|
|[NativeMessagingWhitelist](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=NativeMessagingWhitelist)|[NativeMessagingAllowlist](https://docs.microsoft.com/deployedge/microsoft-edge-policies#nativemessagingallowlist)|
|[NetworkPredictionOptions](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=NetworkPredictionOptions)|[NetworkPredictionOptions](https://docs.microsoft.com/deployedge/microsoft-edge-policies#networkpredictionoptions)|
|[NewTabPageLocation](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=NewTabPageLocation)|[NewTabPageLocation](https://docs.microsoft.com/deployedge/microsoft-edge-policies#newtabpagelocation)|
|[NotificationsAllowedForUrls](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=NotificationsAllowedForUrls)|[NotificationsAllowedForUrls](https://docs.microsoft.com/deployedge/microsoft-edge-policies#notificationsallowedforurls)|
|[NotificationsBlockedForUrls](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=NotificationsBlockedForUrls)|[NotificationsBlockedForUrls](https://docs.microsoft.com/deployedge/microsoft-edge-policies#notificationsblockedforurls)|
|[NtlmV2Enabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=NtlmV2Enabled)|[NtlmV2Enabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#ntlmv2enabled)|
|[NTPCustomBackgroundEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=NTPCustomBackgroundEnabled)|Não Aplicável|
|[OverrideSecurityRestrictionsOnInsecureOrigin](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=OverrideSecurityRestrictionsOnInsecureOrigin)|[OverrideSecurityRestrictionsOnInsecureOrigin](https://docs.microsoft.com/deployedge/microsoft-edge-policies#overridesecurityrestrictionsoninsecureorigin)|
|[PasswordLeakDetectionEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=PasswordLeakDetectionEnabled)|Não Aplicável|
|[PasswordManagerEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=PasswordManagerEnabled)|[PasswordManagerEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#passwordmanagerenabled)|
|[PasswordProtectionChangePasswordURL](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=PasswordProtectionChangePasswordURL)|[PasswordProtectionChangePasswordURL](https://docs.microsoft.com/deployedge/microsoft-edge-policies#passwordprotectionchangepasswordurl)|
|[PasswordProtectionLoginURLs](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=PasswordProtectionLoginURLs)|[PasswordProtectionLoginURLs](https://docs.microsoft.com/deployedge/microsoft-edge-policies#passwordprotectionloginurls)|
|[PasswordProtectionWarningTrigger](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=PasswordProtectionWarningTrigger)|[PasswordProtectionWarningTrigger](https://docs.microsoft.com/deployedge/microsoft-edge-policies#passwordprotectionwarningtrigger)|
|[PaymentMethodQueryEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=PaymentMethodQueryEnabled)|[PaymentMethodQueryEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#paymentmethodqueryenabled)|
|[PluginsAllowedForUrls](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=PluginsAllowedForUrls)|[PluginsAllowedForUrls](https://docs.microsoft.com/deployedge/microsoft-edge-policies#pluginsallowedforurls)|
|[PluginsBlockedForUrls](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=PluginsBlockedForUrls)|[PluginsBlockedForUrls](https://docs.microsoft.com/deployedge/microsoft-edge-policies#pluginsblockedforurls)|
|[PolicyAtomicGroupsEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=PolicyAtomicGroupsEnabled)|Não Aplicável|
|[PolicyDictionaryMultipleSourceMergeList](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=PolicyDictionaryMultipleSourceMergeList)|Não Aplicável|
|[PolicyListMultipleSourceMergeList](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=PolicyListMultipleSourceMergeList)|Não Aplicável|
|[PolicyRefreshRate](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=PolicyRefreshRate)|Não Aplicável|
|[PopupsAllowedForUrls](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=PopupsAllowedForUrls)|[PopupsAllowedForUrls](https://docs.microsoft.com/deployedge/microsoft-edge-policies#popupsallowedforurls)|
|[PopupsBlockedForUrls](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=PopupsBlockedForUrls)|[PopupsBlockedForUrls](https://docs.microsoft.com/deployedge/microsoft-edge-policies#popupsblockedforurls)|
|[PrinterTypeDenyList](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=PrinterTypeDenyList)|Não Aplicável|
|[PrintHeaderFooter](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=PrintHeaderFooter)|[PrintHeaderFooter](https://docs.microsoft.com/deployedge/microsoft-edge-policies#printheaderfooter)|
|[PrintingAllowedBackgroundGraphicsModes](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=PrintingAllowedBackgroundGraphicsModes)|Não Aplicável|
|[PrintingBackgroundGraphicsDefault](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=PrintingBackgroundGraphicsDefault)|Não Aplicável|
|[PrintingEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=PrintingEnabled)|[PrintingEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#printingenabled)|
|[PrintPreviewUseSystemDefaultPrinter](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=PrintPreviewUseSystemDefaultPrinter)|[PrintPreviewUseSystemDefaultPrinter](https://docs.microsoft.com/deployedge/microsoft-edge-policies#printpreviewusesystemdefaultprinter)|
|[PromotionalTabsEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=PromotionalTabsEnabled)|[PromotionalTabsEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#promotionaltabsenabled)|
|[PromptForDownloadLocation](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=PromptForDownloadLocation)|[PromptForDownloadLocation](https://docs.microsoft.com/deployedge/microsoft-edge-policies#promptfordownloadlocation)|
|[ProxyBypassList](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ProxyBypassList)|[ProxyBypassList](https://docs.microsoft.com/deployedge/microsoft-edge-policies#proxybypasslist)|
|[ProxyMode](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ProxyMode)|[ProxyMode](https://docs.microsoft.com/deployedge/microsoft-edge-policies#proxymode)|
|[ProxyPacUrl](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ProxyPacUrl)|[ProxyPacUrl](https://docs.microsoft.com/deployedge/microsoft-edge-policies#proxypacurl)|
|[ProxyServer](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ProxyServer)|[ProxyServer](https://docs.microsoft.com/deployedge/microsoft-edge-policies#proxyserver)|
|[ProxySettings](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ProxySettings)|[ProxySettings](https://docs.microsoft.com/deployedge/microsoft-edge-policies#proxysettings)|
|[QuicAllowed](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=QuicAllowed)|[QuicAllowed](https://docs.microsoft.com/deployedge/microsoft-edge-policies#quicallowed)|
|[RegisteredProtocolHandlers](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=RegisteredProtocolHandlers)|[RegisteredProtocolHandlers](https://docs.microsoft.com/deployedge/microsoft-edge-policies#registeredprotocolhandlers)|
|[RelaunchNotification](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=RelaunchNotification)|[RelaunchNotification](https://docs.microsoft.com/deployedge/microsoft-edge-policies#relaunchnotification)|
|[RelaunchNotificationPeriod](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=RelaunchNotificationPeriod)|[RelaunchNotificationPeriod](https://docs.microsoft.com/deployedge/microsoft-edge-policies#relaunchnotificationperiod)|
|[RemoteAccessHostAllowClientPairing](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=RemoteAccessHostAllowClientPairing)|Não Aplicável|
|[RemoteAccessHostAllowFileTransfer](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=RemoteAccessHostAllowFileTransfer)|Não Aplicável|
|[RemoteAccessHostAllowGnubbyAuth](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=RemoteAccessHostAllowGnubbyAuth)|Não Aplicável|
|[RemoteAccessHostAllowRelayedConnection](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=RemoteAccessHostAllowRelayedConnection)|Não Aplicável|
|[RemoteAccessHostAllowUiAccessForRemoteAssistance](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=RemoteAccessHostAllowUiAccessForRemoteAssistance)|Não Aplicável|
|[RemoteAccessHostClientDomainList](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=RemoteAccessHostClientDomainList)|Não Aplicável|
|[RemoteAccessHostDomainList](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=RemoteAccessHostDomainList)|Não Aplicável|
|[RemoteAccessHostFirewallTraversal](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=RemoteAccessHostFirewallTraversal)|Não Aplicável|
|[RemoteAccessHostMatchUsername](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=RemoteAccessHostMatchUsername)|Não Aplicável|
|[RemoteAccessHostRequireCurtain](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=RemoteAccessHostRequireCurtain)|Não Aplicável|
|[RemoteAccessHostTalkGadgetPrefix](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=RemoteAccessHostTalkGadgetPrefix)|Não Aplicável|
|[RemoteAccessHostTokenUrl](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=RemoteAccessHostTokenUrl)|Não Aplicável|
|[RemoteAccessHostTokenValidationCertificateIssuer](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=RemoteAccessHostTokenValidationCertificateIssuer)|Não Aplicável|
|[RemoteAccessHostTokenValidationUrl](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=RemoteAccessHostTokenValidationUrl)|Não Aplicável|
|[RemoteAccessHostUdpPortRange](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=RemoteAccessHostUdpPortRange)|Não Aplicável|
|[RendererCodeIntegrityEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=RendererCodeIntegrityEnabled)|[RendererCodeIntegrityEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#renderercodeintegrityenabled)|
|[ReportExtensionsAndPluginsData](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ReportExtensionsAndPluginsData)|Não Aplicável|
|[ReportMachineIDData](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ReportMachineIDData)|Não Aplicável|
|[ReportPolicyData](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ReportPolicyData)|Não Aplicável|
|[ReportSafeBrowsingData](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ReportSafeBrowsingData)|Não Aplicável|
|[ReportUserIDData](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ReportUserIDData)|Não Aplicável|
|[ReportVersionData](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ReportVersionData)|Não Aplicável|
|[RequireOnlineRevocationChecksForLocalAnchors](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=RequireOnlineRevocationChecksForLocalAnchors)|[RequireOnlineRevocationChecksForLocalAnchors](https://docs.microsoft.com/deployedge/microsoft-edge-policies#requireonlinerevocationchecksforlocalanchors)|
|[RestoreOnStartup](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=RestoreOnStartup)|[RestoreOnStartup](https://docs.microsoft.com/deployedge/microsoft-edge-policies#restoreonstartup)|
|[RestoreOnStartupURLs](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=RestoreOnStartupURLs)|[RestoreOnStartupURLs](https://docs.microsoft.com/deployedge/microsoft-edge-policies#restoreonstartupurls)|
|[RestrictSigninToPattern](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=RestrictSigninToPattern)|[RestrictSigninToPattern](https://docs.microsoft.com/deployedge/microsoft-edge-policies#restrictsignintopattern)|
|[RoamingProfileLocation](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=RoamingProfileLocation)|Não Aplicável|
|[RoamingProfileSupportEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=RoamingProfileSupportEnabled)|Não Aplicável|
|[RunAllFlashInAllowMode](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=RunAllFlashInAllowMode)|[RunAllFlashInAllowMode](https://docs.microsoft.com/deployedge/microsoft-edge-policies#runallflashinallowmode)|
|[SafeBrowsingEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=SafeBrowsingEnabled)|[SmartScreenEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#smartscreenenabled)|
|[SafeBrowsingExtendedReportingEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=SafeBrowsingExtendedReportingEnabled)|Não Aplicável|
|[SafeBrowsingForTrustedSourcesEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=SafeBrowsingForTrustedSourcesEnabled)|[SmartScreenForTrustedDownloadsEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#smartscreenfortrusteddownloadsenabled)|
|[SafeBrowsingWhitelistDomains](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=SafeBrowsingWhitelistDomains)|[SmartScreenAllowListDomains](https://docs.microsoft.com/deployedge/microsoft-edge-policies#smartscreenallowlistdomains)|
|[SafeSitesFilterBehavior](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=SafeSitesFilterBehavior)|Não Aplicável|
|[SavingBrowserHistoryDisabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=SavingBrowserHistoryDisabled)|[SavingBrowserHistoryDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#savingbrowserhistorydisabled)|
|[SearchSuggestEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=SearchSuggestEnabled)|[SearchSuggestEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#searchsuggestenabled)|
|[SecurityKeyPermitAttestation](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=SecurityKeyPermitAttestation)|[SecurityKeyPermitAttestation](https://docs.microsoft.com/deployedge/microsoft-edge-policies#securitykeypermitattestation)|
|[SendFilesForMalwareCheck](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=SendFilesForMalwareCheck)|Não Aplicável|
|[SharedClipboardEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=SharedClipboardEnabled)|Não Aplicável|
|[ShowAppsShortcutInBookmarkBar](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ShowAppsShortcutInBookmarkBar)|[ShowOfficeShortcutInFavoritesBar](https://docs.microsoft.com/deployedge/microsoft-edge-policies#showofficeshortcutinfavoritesbar)|
|[ShowCastIconInToolbar](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ShowCastIconInToolbar)|[ShowCastIconInToolbar](https://docs.microsoft.com/deployedge/microsoft-edge-policies#showcasticonintoolbar)|
|[ShowHomeButton](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ShowHomeButton)|[ShowHomeButton](https://docs.microsoft.com/deployedge/microsoft-edge-policies#showhomebutton)|
|[SignedHTTPExchangeEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=SignedHTTPExchangeEnabled)|[SignedHTTPExchangeEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#signedhttpexchangeenabled)|
|[SitePerProcess](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=SitePerProcess)|[SitePerProcess](https://docs.microsoft.com/deployedge/microsoft-edge-policies#siteperprocess)|
|[SpellcheckEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=SpellcheckEnabled)|[SpellcheckEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#spellcheckenabled)|
|[SpellcheckLanguage](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=SpellcheckLanguage)|[SpellcheckLanguage](https://docs.microsoft.com/deployedge/microsoft-edge-policies#spellchecklanguage)|
|[SpellcheckLanguageBlacklist](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=SpellcheckLanguageBlacklist)|[SpellcheckLanguageBlocklist](https://docs.microsoft.com/deployedge/microsoft-edge-policies#spellchecklanguageblocklist)|
|[SpellCheckServiceEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=SpellCheckServiceEnabled)|Não Aplicável|
|[SSLErrorOverrideAllowed](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=SSLErrorOverrideAllowed)|[SSLErrorOverrideAllowed](https://docs.microsoft.com/deployedge/microsoft-edge-policies#sslerroroverrideallowed)|
|[SSLVersionMin](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=SSLVersionMin)|[SSLVersionMin](https://docs.microsoft.com/deployedge/microsoft-edge-policies#sslversionmin)|
|[StricterMixedContentTreatmentEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=StricterMixedContentTreatmentEnabled)|Não Aplicável|
|[SuppressUnsupportedOSWarning](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=SuppressUnsupportedOSWarning)|[SuppressUnsupportedOSWarning](https://docs.microsoft.com/deployedge/microsoft-edge-policies#suppressunsupportedoswarning)|
|[SyncDisabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=SyncDisabled)|[SyncDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#syncdisabled)|
|[SyncTypesListDisabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=SyncTypesListDisabled)|Não Aplicável|
|[TabFreezingEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=TabFreezingEnabled)|[TabFreezingEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#tabfreezingenabled)|
|[TaskManagerEndProcessEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=TaskManagerEndProcessEnabled)|[TaskManagerEndProcessEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#taskmanagerendprocessenabled)|
|[ThirdPartyBlockingEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ThirdPartyBlockingEnabled)|Não Aplicável|
|[TLS13HardeningForLocalAnchorsEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=TLS13HardeningForLocalAnchorsEnabled)|Não Aplicável|
|[TotalMemoryLimitMb](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=TotalMemoryLimitMb)|[TotalMemoryLimitMb](https://docs.microsoft.com/deployedge/microsoft-edge-policies#totalmemorylimitmb)|
|[TranslateEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=TranslateEnabled)|[TranslateEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#translateenabled)|
|[UnsafeEventsReportingEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=UnsafeEventsReportingEnabled)|Não Aplicável|
|[URLBlacklist](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=URLBlacklist)|[URLBlocklist](https://docs.microsoft.com/deployedge/microsoft-edge-policies#urlblocklist)|
|[UrlKeyedAnonymizedDataCollectionEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=UrlKeyedAnonymizedDataCollectionEnabled)|Não Aplicável|
|[URLsToCheckComplianceOfDownloadedContent](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=URLsToCheckComplianceOfDownloadedContent)|Não Aplicável|
|[URLsToCheckForMalwareOfUploadedContent](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=URLsToCheckForMalwareOfUploadedContent)|Não Aplicável|
|[URLsToNotCheckComplianceOfUploadedContent](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=URLsToNotCheckComplianceOfUploadedContent)|Não Aplicável|
|[URLWhitelist](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=URLWhitelist)|[URLAllowlist](https://docs.microsoft.com/deployedge/microsoft-edge-policies#urlallowlist)|
|[UserDataDir](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=UserDataDir)|[UserDataDir](https://docs.microsoft.com/deployedge/microsoft-edge-policies#userdatadir)|
|[UserFeedbackAllowed](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=UserFeedbackAllowed)|[UserFeedbackAllowed](https://docs.microsoft.com/deployedge/microsoft-edge-policies#userfeedbackallowed)|
|[VariationsRestrictParameter](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=VariationsRestrictParameter)|Não Aplicável|
|[VideoCaptureAllowed](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=VideoCaptureAllowed)|[VideoCaptureAllowed](https://docs.microsoft.com/deployedge/microsoft-edge-policies#videocaptureallowed)|
|[VideoCaptureAllowedUrls](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=VideoCaptureAllowedUrls)|[VideoCaptureAllowedUrls](https://docs.microsoft.com/deployedge/microsoft-edge-policies#videocaptureallowedurls)|
|[WebAppInstallForceList](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=WebAppInstallForceList)|[WebAppInstallForceList](https://docs.microsoft.com/deployedge/microsoft-edge-policies#webappinstallforcelist)|
|[WebComponentsV0Enabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=WebComponentsV0Enabled)|[WebComponentsV0Enabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#webcomponentsv0enabled)|
|[WebRtcEventLogCollectionAllowed](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=WebRtcEventLogCollectionAllowed)|Não Aplicável|
|[WebRtcLocalIpsAllowedUrls](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=WebRtcLocalIpsAllowedUrls)|[WebRtcLocalIpsAllowedUrls](https://docs.microsoft.com/deployedge/microsoft-edge-policies#webrtclocalipsallowedurls)|
|[WebRtcUdpPortRange](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=WebRtcUdpPortRange)|[WebRtcUdpPortRange](https://docs.microsoft.com/deployedge/microsoft-edge-policies#webrtcudpportrange)|
|[WebUsbAllowDevicesForUrls](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=WebUsbAllowDevicesForUrls)|[WebUsbAllowDevicesForUrls](https://docs.microsoft.com/deployedge/microsoft-edge-policies#webusballowdevicesforurls)|
|[WebUsbAskForUrls](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=WebUsbAskForUrls)|[WebUsbAskForUrls](https://docs.microsoft.com/deployedge/microsoft-edge-policies#webusbaskforurls)|
|[WebUsbBlockedForUrls](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=WebUsbBlockedForUrls)|[WebUsbBlockedForUrls](https://docs.microsoft.com/deployedge/microsoft-edge-policies#webusbblockedforurls)|
|[WPADQuickCheckEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=WPADQuickCheckEnabled)|[WPADQuickCheckEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#wpadquickcheckenabled)|

## Consulte também

- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Configurar o Microsoft Edge](configure-microsoft-edge.md)
- [Referência de política do navegador](microsoft-edge-policies.md)
