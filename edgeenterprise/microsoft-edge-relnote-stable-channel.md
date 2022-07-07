---
title: Notas de versão do Microsoft Edge para Stable Channel
ms.author: leahtu
author: dan-wesley
manager: srugh
ms.date: 07/06/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Notas de versão do Microsoft Edge para Stable Channel
ms.openlocfilehash: b17c25f89c71eba1bdd69d959556dcb34775823c
ms.sourcegitcommit: 42a3ee7e4b91efb49ee99b3c4cbb1be185347b1b
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/07/2022
ms.locfileid: "12635816"
---
# <a name="release-notes-for-microsoft-edge-stable-channel"></a>Notas de versão do Microsoft Edge Stable Channel

Essas notas de versão fornecem informações dos novos recursos e atualizações não relacionados à segurança que estão inclusos Microsoft Edge Stable Channel.

- Todas as atualizações de segurança estão listadas nas [Notas de versão das Atualizações de Segurança do Microsoft Edge](./microsoft-edge-relnotes-security.md).
- As notas de versão arquivadas do Canal Estável do Microsoft Edge estão localizadas nas [Notas de versão arquivadas do Canal Estável do Microsoft Edge](./microsoft-edge-relnote-archive-stable-channel.md).

 Para entender os canais do Microsoft Edge, confira a [Visão geral dos canais do Microsoft Edge](./microsoft-edge-channels.md).

> [!NOTE]
> Para o Canal Estável, as atualizações serão implantadas progressivamente por um ou mais dias. Para saber mais, consulte [Distribuições progressivas para atualizações do Microsoft Edge](./microsoft-edge-update-progressive-rollout.md).
>
> A Plataforma da Web do Microsoft Edge evolui constantemente para melhorar a experiência, segurança e privacidade do usuário. Para saber mais, confira [Compatibilidade de sites: alterações que afetam o Microsoft Edge](/microsoft-edge/web-platform/site-impacting-changes).

## <a name="version-1030126449-july-6"></a>Versão 103.0.1264.49: 6 de julho

> [!Important]
> Esta atualização contém uma correção para [CVE-2022-2294](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2022-2294), que foi relatada pela equipe do Chromium como tendo um exploit em execução. Para obter mais informações, consulte o [Guia de atualização de segurança](https://msrc.microsoft.com/update-guide).

As atualizações de segurança do canal Estável estão listadas [aqui](/deployedge/microsoft-edge-relnotes-security#july-6-2022).

## <a name="version-1020124556-july-6"></a>Versão 102.0.1245.56: 6 de julho

Correção de vários bugs e problemas de desempenho para a versão Estável Estendida.

## <a name="version-1030126444-june-30"></a>Versão 103.0.1264.44: 30 de junho

As atualizações de segurança do canal Estável estão listadas [aqui](/deployedge/microsoft-edge-relnotes-security#june-30-2022).

## <a name="version-1020124550-june-23"></a>Versão 102.0.1245.50: 23 de junho

Correção de vários bugs e problemas de desempenho para a versão Estável Estendida.

## <a name="version-1030126437-june-23"></a>Versão 103.0.1264.37: 23 de junho

As atualizações de segurança do canal Estável estão listadas [aqui](/deployedge/microsoft-edge-relnotes-security#june-23-2022).

### <a name="feature-updates"></a>Atualizações de recursos

- **Capacidade de controlar a alternância automática de perfil.** A política [GuidedSwitchEnabled](/DeployEdge/microsoft-edge-policies#guidedswitchenabled) permite que a Microsoft Edge solicite ao usuário que mude para o perfil apropriado quando o Microsoft Edge detectar que um link é um link pessoal ou de trabalho.

- **Alternador de Certificado do Cliente.** Esse recurso oferecerá uma maneira para os usuários limparem o certificado lembrado e ressurgir o seletor de certificado ao visitar um site que exige autenticação de certificado http. A alternância pode ser feita sem sair manualmente do Microsoft Edge.

- **Defesa da Web mais confiável.** Navegue pela Web com proteção mais confiável graças à biblioteca reescrita do[Microsoft Defender SmartScreen](/deployedge/microsoft-edge-security-smartscreen) para Microsoft Edge no Windows. A política [NewSmartScreenLibraryEnabled](microsoft-edge-policies.md#newsmartscreenlibraryenabled) permitirá que os clientes empresariais continuem usando a versão herdada da biblioteca até que ela seja preterida no Microsoft Edge versão 105.

- **Faixa de Pesquisa de Trabalho na barra de endereços do Microsoft Edge.** Essa faixa ajuda você a permanecer no fluxo do seu trabalho ao restringir o foco da pesquisa aos resultados somente de trabalho. Para ver os resultados focados no trabalho da sua organização, selecione a faixa no início da pesquisa. Para ser direcionado para a página de resultados da pesquisa no local de trabalho da sua organização, selecione a faixa em qualquer ponto da pesquisa. Use a política [AddressBarMicrosoftSearchInBingProviderEnabled](/deployedge/microsoft-edge-policies#addressbarmicrosoftsearchinbingproviderenabled) para ativar ou desativar esse recurso.

### <a name="policy-updates"></a>Atualizações de política

#### <a name="new-policies"></a>Novas políticas

- [GuidedSwitchEnabled](/DeployEdge/microsoft-edge-policies#guidedswitchenabled) – Comutador Guiado Habilitado
- [InternetExplorerZoomDisplay](/DeployEdge/microsoft-edge-policies#internetexplorerzoomdisplay) - Exibir zoom nas guias do Modo IE com Escala de DPI incluída como está no Internet Explorer
- [LiveCaptionsAllowed](/DeployEdge/microsoft-edge-policies#livecaptionsallowed) – Legendas ao vivo permitidas
- [OriginAgentClusterDefaultEnabled](/DeployEdge/microsoft-edge-policies#originagentclusterdefaultenabled) - Agrupamento de agentes com chave de origem habilitada por padrão

#### <a name="additional-policy-changes"></a>Alterações de política adicionais

- [SleepingTabsTimeout](/DeployEdge/microsoft-edge-policies#sleepingtabstimeout) - Define o tempo limite de inatividade da guia plano de fundo para guias inativas. **Nota:** Um tempo limite de 30 segundos de inatividade foi adicionado a essa política.

## <a name="version-1020124544-june-16"></a>Versão 102.0.1245.44: 16 de junho

Corrigidos vários bugs e problemas de desempenho para a versão Estável e Estável Estendida.

## <a name="version-1020124541-june-13"></a>Versão 102.0.1245.41: 13 de junho

As atualizações de segurança do canal Estável estão listadas [aqui](/deployedge/microsoft-edge-relnotes-security#june-13-2022).

## <a name="version-1020124539-june-9"></a>Versão 102.0.1245.39: 9 de junho

As atualizações de segurança do canal Estável estão listadas [aqui](/deployedge/microsoft-edge-relnotes-security#june-9-2022).

## <a name="version-1020124533-june-3"></a>Versão 102.0.1245.33: 3 de junho

Corrigidos vários bugs e problemas de desempenho para a versão Estável e Estável Estendida.

## <a name="version-1020124530-may-31"></a>Versão 102.0.1245.30: 31 de maio

As atualizações de segurança do canal Estável estão listadas [aqui](/deployedge/microsoft-edge-relnotes-security#may-31-2022).

### <a name="policy-updates"></a>Atualizações de política

#### <a name="new-policies"></a>Novas políticas

- [AllHttpAuthSchemesAllowedForOrigins](/DeployEdge/microsoft-edge-policies#allhttpauthschemesallowedfororigins): lista de origens que permitem toda a autenticação HTTP
- [OutlookHubMenuEnabled](/DeployEdge/microsoft-edge-policies#outlookhubmenuenabled): permite que os usuários acessem o menu do Outlook
- [NetworkServiceSandboxEnabled](/DeployEdge/microsoft-edge-policies#networkservicesandboxenabled): habilitar a área restrita do serviço de rede
- [UserAgentClientHintsGREASEUpdateEnabled](/DeployEdge/microsoft-edge-policies#useragentclienthintsgreaseupdateenabled): controla o recurso Atualização GREASE das Dicas do Cliente do Agente do Usuário

## <a name="version-1010121053-may-19"></a>Versão 101.0.1210.53: 19 de maio

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-1000118560-may-13"></a>Versão 100.0.1185.60: 13 de maio

Correção de vários bugs e problemas de desempenho para a versão Estável Estendida.

## <a name="version-1010121047-may-13"></a>Versão 101.0.1210.47: 13 de maio

As atualizações de segurança do canal estável estão listadas [aqui](/deployedge/microsoft-edge-relnotes-security#may-13-2022).

## <a name="version-1010121039-may-5"></a>Versão 101.0.1210.39: 5 de maio

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-1000118557-may-2"></a>Versão 100.0.1185.57: 2 de maio

Correção de vários bugs e problemas de desempenho para a versão Estável Estendida.

## <a name="version-1010121032-april-28"></a>Versão 101.0.1210.32: 28 de abril

As atualizações de segurança do canal Estável estão listadas [aqui](/deployedge/microsoft-edge-relnotes-security#april-28-2022).

### <a name="feature-updates"></a>Atualizações de recursos

- **Capacidade de definir o perfil padrão.** A política [EdgeDefaultProfileEnabled](/DeployEdge/microsoft-edge-policies#edgedefaultprofileenabled) permitirá que você defina um perfil padrão para usar ao abrir o navegador em vez do último perfil usado. Essa política não será aplicável se o parâmetro `--profile-directory` tiver sido especificado.

- **Inicie os PWAs (Aplicativos Web Progressivos) na barra de favoritos.** As melhorias na experiência de inicialização do PWA começarão a aparecer com um ícone de Aplicativos que pode ser adicionado à barra de ferramentas.

- **Gerencie a configuração "Permitir extensões de outras lojas".** Agora você pode usar a política [ControlDefaultStateOfAllowExtensionFromOtherStoresSettingEnabled](/DeployEdge/microsoft-edge-policies#controldefaultstateofallowextensionfromotherstoressettingenabled) para definir o estado padrão da configuração "Permitir extensões de outras lojas".

- **Melhorias no Gerenciador de Lista de Sites Corporativos.** Agora você pode configurar cookies compartilhados entre o Microsoft Edge e o Internet Explorer em sua lista de sites corporativos. Você pode acessar o [Gerenciador de Lista de Sites Corporativos](/deployedge/edge-ie-mode-site-list-manager) em *edge://compat/SiteListManager*.

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

#### <a name="deprecated-policies"></a>Políticas preteridas

- [ForceCertificatePromptsOnMultipleMatches](/DeployEdge/microsoft-edge-policies#forcecertificatepromptsonmultiplematches) - Configure se o Microsoft Edge deve selecionar automaticamente um certificado quando houver várias correspondências de certificado para um site configurado com "AutoSelectCertificateForUrls"

#### <a name="obsoleted-policies"></a>Políticas obsoletas

- [WebSQLInThirdPartyContextEnabled](/DeployEdge/microsoft-edge-policies#websqlinthirdpartycontextenabled) - Forçar o WebSQL em contextos de terceiros para ser habilitado novamente

## <a name="version-1000118550-april-21"></a>Versão 100.0.1185.50: 21 de abril

Corrigidos vários bugs e problemas de desempenho para a versão Estável e Estável Estendida.

## <a name="version-1000118544-april-15"></a>Versão 100.0.1185.44: 15 de abril

> [!Important]
> Esta atualização contém uma correção para [CVE-2022-1364](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2022-1364), que foi relatada pela equipe do Chromium como tendo uma exploração em estado selvagem. Para obter mais informações, confira o [Guia de Atualização de Segurança](https://msrc.microsoft.com/update-guide).

As atualizações de segurança do canal Estável estão listadas [aqui](/deployedge/microsoft-edge-relnotes-security#april-15-2022).

## <a name="version-1000118539-april-11"></a>Versão 100.0.1185.39: 11 de abril

Corrigidos vários bugs e problemas de desempenho para a versão Estável e Estável Estendida.

## <a name="version-1000118536-april-7"></a>Versão 100.0.1185.36: 7 de abril

As atualizações de segurança do canal estável estão listadas [aqui](/deployedge/microsoft-edge-relnotes-security#april-7-2022).

## <a name="version-1000118529-april-1"></a>Versão 100.0.1185.29: 1º de abril

As atualizações de segurança do canal estável estão listadas [aqui](/deployedge/microsoft-edge-relnotes-security#april-1-2022).

### <a name="feature-updates"></a>Atualizações de recursos

- **Número de versão de três dígitos da cadeia de caracteres de agente de usuário.** O Microsoft Edge agora enviará um número de versão de três dígitos, como Edg/100 no cabeçalho do agente de usuário. Isso pode confundir scripts ou análises do lado do servidor que usam um analisador com erros para determinar o número de versão da cadeia de caracteres de agente de usuário. Você pode usar a política [ForceMajorVersionToMinorPositionInUserAgent](/deployedge/microsoft-edge-policies#forcemajorversiontominorpositioninuseragent) para controlar se a versão principal da cadeia de caracteres de agente de usuário deve ser congelada em 99. Além disso, o sinalizador **#force-major-version-to-minor** está disponível no *edge://flags* para congelar a versão principal da cadeia de caracteres de agente de usuário para 99.

- **Simplificando as Ativações do protocolo de aplicativo do Microsoft 365.** As Ativações do protocolo de aplicativo do Microsoft 365 nos serviços confiáveis de armazenamento em nuvem da Microsoft agora iniciarão determinados aplicativos diretamente do Microsoft 365, incluindo subdomínios do SharePoint e URLs do Microsoft OneDrive. Você pode usar as políticas [AutoLaunchProtocolsComponentEnabled](/deployedge/microsoft-edge-policies#autolaunchprotocolscomponentenabled) e [AutoLaunchProtocolsFromOrigins](/deployedge/microsoft-edge-policies#autolaunchprotocolsfromorigins) para habilitar os prompts de ativação do protocolo de aplicativo, se desejado, e para definir outros aplicativos e serviços em que os avisos são habilitados ou desabilitados.

- **Proteção de pilha imposta por hardware.** O Microsoft Edge continuará dando suporte a uma proteção mais refinada, combatendo vulnerabilidades de corrupção de memória e protegendo chamadas indiretas. A proteção de pilha imposta por hardware é compatível apenas pelo Windows 8 e posterior. Para obter mais informações, confira [Proteção de pilha imposta por hardware](https://techcommunity.microsoft.com/t5/windows-kernel-internals-blog/developer-guidance-for-hardware-enforced-stack-protection/ba-p/2163340). Esse comportamento de recurso pode ser controlado usando a política [ShadowStackCrashRollbackBehavior](/deployedge/microsoft-edge-policies#shadowstackcrashrollbackbehavior).

- **Visualize arquivos PDF no Microsoft Outlook e no Explorador de Arquivos.** Os usuários podem visualizar um arquivo PDF em uma visualização somente leitura leve e avançada. Esse recurso está disponível para anexos em PDF da área de trabalho do Outlook ou para arquivos PDF locais usando o Explorador de Arquivos.

- **Abra arquivos PDF assinados digitalmente.** As assinaturas digitais são usadas extensivamente para validar a autenticidade de um documento e as alterações feitas em um documento. Você pode usar a política [PDFSecureMode](/deployedge/microsoft-edge-policies#pdfsecuremode) para habilitar a validação de assinatura digital de arquivos PDF, diretamente do navegador, sem a necessidade de suplementos.

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

## <a name="version-980110892-march-26"></a>Versão 98.0.1108.92: 26 de março

Correção de vários bugs e problemas de desempenho para a versão Estável Estendida.

## <a name="version-990115055-march-26"></a>Versão 99.0.1150.55: 26 de março

> [!Important]
> Esta atualização contém uma correção para [CVE-2022-1096](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2022-1096), que foi relatada pela equipe do Chromium como tendo uma exploração em estado selvagem. Para obter mais informações, confira o [Guia de Atualização de Segurança](https://msrc.microsoft.com/update-guide).

As atualizações de segurança do canal Estável estão listadas [aqui](/deployedge/microsoft-edge-relnotes-security#march-26-2022).

## <a name="version-990115052-march-24"></a>Versão 99.0.1150.52: 24 de março

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-980110884-march-17"></a>Versão 98.0.1108.84: 17 de março

Correção de vários bugs e problemas de desempenho para a versão Estável Estendida.

## <a name="version-990115046-march-17"></a>Versão 99.0.1150.46: 17 de março

As atualizações de segurança do canal Estável estão listadas [aqui](/deployedge/microsoft-edge-relnotes-security#march-17-2022).

## <a name="version-990115039-march-10"></a>Versão 99.0.1150.39: 10 de março

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-980110876-march-9"></a>Versão 98.0.1108.76: 9 de março

Correção de vários bugs e problemas de desempenho para a versão Estável Estendida.

## <a name="version-990115036-march-7"></a>Versão 99.0.1150.36: 7 de março

Vários bugs e problemas de desempenho corrigidos.

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

## <a name="see-also"></a>Ver também

- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
