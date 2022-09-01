---
title: Notas de versão arquivadas para o Canal Estável do Microsoft Edge
ms.author: leahtu
author: leahmsft
manager: srugh
ms.date: 09/01/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Notas de versão arquivadas para o Canal Estável do Microsoft Edge
ms.openlocfilehash: 2497868637be9d23278a59bd1fa311a2eb281f78
ms.sourcegitcommit: 346c4c3e30ed30b68b59b77ec712d52eb8c62ce1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/01/2022
ms.locfileid: "12741554"
---
# <a name="archived-release-notes-for-microsoft-edge-stable-channel"></a>Notas de versão arquivadas para o Canal Estável do Microsoft Edge

Essas notas de versão fornecem informações dos novos recursos e atualizações não relacionados à segurança que estão inclusos Microsoft Edge Stable Channel. Todas as atualizações de segurança estão listadas [aqui](microsoft-edge-relnotes-security.md).

## <a name="version-1020124530-may-31-2022"></a>Versão 102.0.1245.30: 31 de maio de 2022

As atualizações de segurança do canal Estável estão listadas [aqui](/deployedge/microsoft-edge-relnotes-security#may-31-2022).

### <a name="policy-updates"></a>Atualizações de política

#### <a name="new-policies"></a>Novas políticas

- [AllHttpAuthSchemesAllowedForOrigins](/DeployEdge/microsoft-edge-policies#allhttpauthschemesallowedfororigins): lista de origens que permitem toda a autenticação HTTP
- [OutlookHubMenuEnabled](/DeployEdge/microsoft-edge-policies#outlookhubmenuenabled): permite que os usuários acessem o menu do Outlook
- [NetworkServiceSandboxEnabled](/DeployEdge/microsoft-edge-policies#networkservicesandboxenabled): habilitar a área restrita do serviço de rede
- [UserAgentClientHintsGREASEUpdateEnabled](/DeployEdge/microsoft-edge-policies#useragentclienthintsgreaseupdateenabled): controla o recurso Atualização GREASE das Dicas do Cliente do Agente do Usuário

## <a name="version-1010121053-may-19-2022"></a>Versão 101.0.1210.53: 19 de maio de 2022

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-1000118560-may-13-2022"></a>Versão 100.0.1185.60: 13 de maio de 2022

Correção de vários bugs e problemas de desempenho para a versão Estável Estendida.

## <a name="version-1010121047-may-13-2022"></a>Versão 101.0.1210.47: 13 de maio de 2022

As atualizações de segurança do canal Estável estão listadas [aqui](/deployedge/microsoft-edge-relnotes-security#may-13-2022).

## <a name="version-1010121039-may-5-2022"></a>Versão 101.0.1210.39: 5 de maio de 2022

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-1000118557-may-2-2022"></a>Versão 100.0.1185.57: 2 de maio de 2022

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

## <a name="version-990115030-march-3"></a>Versão 99.0.1150.30: 3 de março

As atualizações de segurança do canal Estável estão listadas [aqui](/deployedge/microsoft-edge-relnotes-security#march-3-2022).

### <a name="feature-updates"></a>Atualizações de recursos

- **Em breve, número de versão de três dígitos na cadeia de caracteres de agente do usuário.** A partir da versão 100, o Microsoft Edge enviará um número de versão de três dígitos no cabeçalho do agente de usuário, por exemplo, "Edg/100". A partir do Microsoft Edge 97, os proprietários de sites podem testar essa próxima cadeia de caracteres de agente habilitando o sinalizador de experimento **#force-major-version-to-100** em *edge://flags* para garantir que sua lógica de análise do agente de usuário seja robusta e funcione conforme o esperado.

- **Personalize experiências de vários perfis com preferências de perfil de sites.** Os usuários podem personalizar sua experiência de vários perfis com a capacidade de criar uma lista personalizada de sites de alternância automática de perfis no Microsoft Edge.

- **Navegue por documentos PDF usando miniaturas da página.** Agora você poderá navegar pelo documento PDF usando miniaturas que representam as páginas. Essas miniaturas aparecerão no painel no lado esquerdo do leitor de PDF.

- **Configure a lista de domínios nos quais a Interface de usuário (UI) do gerenciador de senhas de Salvar e Preencher será desabilitada.** Use a política [PasswordManagerBlocklist](/deployedge/microsoft-edge-policies#passwordmanagerblocklist) para configurar a lista de domínios (somente esquemas e nomes do host HTTP/HTTPS) onde o Microsoft Edge deve desabilitar o gerenciador de senhas. Isso significa que os fluxos de trabalho Salvar e Preencher serão desabilitados, o que garante que as senhas desses sites não possam ser salvas ou preenchidas automaticamente em formulários da Web.

- **Senha primária personalizada.** O navegador já tem a funcionalidade em que os usuários podem adicionar uma etapa de autenticação antes que as senhas salvas sejam preenchidas automaticamente em formulários da Web. Isso adiciona outra camada de privacidade e ajuda a impedir que usuários não autorizados usem senhas salvas para fazer logon em sites. A senha primária personalizada é uma evolução desse mesmo recurso, onde os usuários agora poderão usar uma cadeia de caracteres personalizada de sua escolha como senha principal. Depois de habilitado, os usuários inserirão essa senha para autenticar a si mesmos e terão suas senhas salvas preenchidas automaticamente em formulários da Web.

### <a name="policy-updates"></a>Atualizações de política

#### <a name="new-policies"></a>Novas Políticas

- [DoNotSilentlyBlockProtocolsFromOrigins](/DeployEdge/microsoft-edge-policies#donotsilentlyblockprotocolsfromorigins) - Definir uma lista de protocolos que não podem ser bloqueados silenciosamente pela proteção anti-inundação
- [ForceMajorVersionToMinorPositionInUserAgent](/DeployEdge/microsoft-edge-policies#forcemajorversiontominorpositioninuseragent) - Habilitar ou desabilitar o congelamento da cadeia de caracteres de agente de usuário na versão principal 99
- [HubsSidebarEnabled](/DeployEdge/microsoft-edge-policies#hubssidebarenabled) – Mostrar barra lateral dos hubs
- [InternetExplorerIntegrationCloudNeutralSitesReporting](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationcloudneutralsitesreporting) - Configurar relatórios de URLs de sites neutros potencialmente mal configurados para o aplicativo Listas de sites do Centro de administração do M365
- [InternetExplorerIntegrationCloudUserSitesReporting](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationcloudusersitesreporting) - Configurar o relatório de entradas da lista de usuários do modo IE para o aplicativo Listas de sites do Centro de administração do M365
- [PasswordManagerBlocklist](/DeployEdge/microsoft-edge-policies#passwordmanagerblocklist) - Configurar a lista de domínios dos quais a interface do usuário do gerenciador de senhas (Salvar e Preencher) será desabilitada
- [RelatedMatchesCloudServiceEnabled](/DeployEdge/microsoft-edge-policies#relatedmatchescloudserviceenabled) - Configurar correspondências relacionadas em Localizar na página
- [SignInCtaOnNtpEnabled](/DeployEdge/microsoft-edge-policies#signinctaonntpenabled) - Habilitar caixa de diálogo de clique para ação de entrada
- [UserAgentReduction](/DeployEdge/microsoft-edge-policies#useragentreduction) - Habilitar ou desabilitar a Redução do agente de usuário

## <a name="version-980110862-february-24"></a>Versão 98.0.1108.62: 24 de fevereiro

Corrigidos vários bugs e problemas de desempenho para a versão Estável e Estável Estendida.

## <a name="version-980110856-february-17"></a>Versão 98.0.1108.56: 17 de fevereiro

Corrigidos vários bugs e problemas de desempenho para a versão Estável e Estável Estendida.

## <a name="version-980110855-february-16"></a>Versão 98.0.1108.55: 16 de fevereiro

> [!Important]
> Essa atualização contém uma correção para [CVE-2022-0609](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2022-0609) que foi relatada pela equipe do Chromium como tendo uma exploração em execução. Para obter mais informações, confira o [Guia de Atualização de Segurança](https://msrc.microsoft.com/update-guide).

As atualizações de segurança do canal Estável estão listadas [aqui](/deployedge/microsoft-edge-relnotes-security#february-16-2022).

## <a name="version-980110850-february-10"></a>Versão 98.0.1108.50: 10 de fevereiro

As atualizações de segurança do canal Estável estão listadas [aqui](/deployedge/microsoft-edge-relnotes-security#february-10-2022).

## <a name="version-980110843-february-3"></a>Versão 98.0.1108.43: 3 de fevereiro

As atualizações de segurança do canal estável estão listadas [aqui](/deployedge/microsoft-edge-relnotes-security#february-3-2022).

### <a name="feature-updates"></a>Atualizações de recursos

- **Melhore sua segurança na Web.** Este é um modo de navegação no Microsoft Edge em que a segurança do navegador tem prioridade, oferecendo aos usuários uma camada extra de proteção ao navegar na Web. Os administradores podem aplicar políticas de grupo a áreas de trabalho de usuários finais (Windows, macOS e Linux) para ajudar a proteger contra explorações em execução (também conhecidas como 0-days). As seguintes políticas de grupo suportam este modo de navegação:

  - [EnhanceSecurityMode](/deployedge/microsoft-edge-policies#enhancesecuritymode)
  - [EnhanceSecurityModeBypassListDomains](/deployedge/microsoft-edge-policies#enhancesecuritymodebypasslistdomains)
  - [EnhanceSecurityModeEnforceListDomains](/deployedge/microsoft-edge-policies#enhancesecuritymodeenforcelistdomains)

- **Em breve, número de versão de três dígitos na cadeia de caracteres de agente do usuário.** A partir da versão 100, o Microsoft Edge enviará um número de versão de três dígitos no cabeçalho do agente de usuário, por exemplo "Edg/**100**". A partir do Microsoft Edge 97, os proprietários de sites podem testar essa próxima cadeia de caracteres de agente de usuário habilitando o sinalizador de experimento **#force-major-version-to-100** no *edge://flags* para garantir que sua lógica de análise do agente de usuário seja robusta e funcione conforme o esperado.

- **Substituir a semântica SDP do Plano B do WebRTC.** Essa alteração substitui um dialeto herdado do Protocolo de Descrição de Sessão (SDP) chamado Plano B. Esse formato SDP está sendo substituído pelo Plano Unificado, que é um formato SDP compatível com especificações e entre navegadores. Para obter mais informações, confira a entrada Status da plataforma Chrome [PSA: o Plano B deve incluir o M96 Beta e Estável](https://chromestatus.com/feature/5823036655665152), e [PSA: o Plano B incluindo a data de término da avaliação de depreciação estável e estendida](https://groups.google.com/g/discuss-webrtc/c/gEHrZyYKsfU). Solicitar uma [Avaliação da semântica de SDP do Plano B do RTCPeerConnection](https://developer.chrome.com/origintrials/#/view_trial/3892235977954951169) permite que os sites continuem a usar a API preterida até a versão 101.

- **Barras de rolagem de sobreposição adicionadas ao Microsoft Edge.** Atualizamos nossas barras de rolagem com um design baseado em sobreposição. Os usuários podem ativar esse recurso em *edge://flags*.

### <a name="policy-updates"></a>Atualizações de política

#### <a name="new-policies"></a>Novas Políticas

- [AddressBarEditingEnabled](/DeployEdge/microsoft-edge-policies#addressbareditingenabled) - Configurar a edição da barra de endereços
- [AllowGamesMenu](/DeployEdge/microsoft-edge-policies#allowgamesmenu) - Permitir que os usuários acessem o menu de jogos
- [EdgeFollowEnabled](/DeployEdge/microsoft-edge-policies#edgefollowenabled) - Habilitar o serviço Seguir no Microsoft Edge
- [EnhanceSecurityMode](/DeployEdge/microsoft-edge-policies#enhancesecuritymode) - Aprimorar o estado de segurança no Microsoft Edge
- [EnhanceSecurityModeBypassListDomains](/DeployEdge/microsoft-edge-policies#enhancesecuritymodebypasslistdomains) - Configurar a lista de domínios nos quais o modo de segurança aprimorado não será imposto
- [EnhanceSecurityModeEnforceListDomains](/DeployEdge/microsoft-edge-policies#enhancesecuritymodeenforcelistdomains) - Configurar a lista de domínios nos quais o modo de segurança aprimorado sempre será imposto
- [InAppSupportEnabled](/DeployEdge/microsoft-edge-policies#inappsupportenabled) - Suporte no aplicativo habilitado
- [MicrosoftEdgeInsiderPromotionEnabled](/DeployEdge/microsoft-edge-policies#microsoftedgeinsiderpromotionenabled) - Promoção do Microsoft Edge Insider habilitada
- [PrintStickySettings](/DeployEdge/microsoft-edge-policies#printstickysettings) - Configurações fixas da visualização de impressão
- [SandboxExternalProtocolBlocked](/DeployEdge/microsoft-edge-policies#sandboxexternalprotocolblocked) - Permitir que o Microsoft Edge bloqueie navegações para protocolos externos em um iframe na área restrita
- [U2fSecurityKeyApiEnabled](/DeployEdge/microsoft-edge-policies#u2fsecuritykeyapienabled) - Permitir o uso da API de chave de segurança U2F preterida

## <a name="version-970107276-january-27"></a>Versão 97.0.1072.76: 27 de janeiro

Vários bugs e problemas de desempenho corrigidos.

### <a name="feature-updates"></a>Atualizações de recursos

- **Em breve, número de versão de três dígitos na cadeia de caracteres de agente do usuário.** A partir da versão 100, o Microsoft Edge enviará um número de versão de três dígitos no cabeçalho do agente de usuário, por exemplo "Edg/**100**". A partir do Microsoft Edge 97, os proprietários de sites podem testar essa próxima cadeia de caracteres de agente de usuário habilitando o sinalizador de experimento **#force-major-version-to-100** no *edge://flags* para garantir que sua lógica de análise do agente de usuário seja robusta e funcione conforme o esperado.

## <a name="version-960105475-january-21"></a>Versão 96.0.1054.75: 21 de janeiro

Correção de vários bugs e problemas de desempenho para a versão Estável Estendida.

## <a name="version-970107269-january-20"></a>Versão 97.0.1072.69: 20 de janeiro

As atualizações de segurança do canal estável estão listadas [aqui](/deployedge/microsoft-edge-relnotes-security#january-20-2022).

## <a name="version-970107262-january-13"></a>Versão 97.0.1072.62: 13 de janeiro

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-960105472-january-6"></a>Versão 96.0.1054.72: 6 de janeiro

Correção de vários bugs e problemas de desempenho para a versão Estável Estendida.

## <a name="version-970107255-january-6"></a>Versão 97.0.1072.55: 6 de janeiro

As atualizações de segurança do canal estável estão listadas [aqui](/deployedge/microsoft-edge-relnotes-security#january-6-2022).

### <a name="feature-updates"></a>Atualizações de recursos

- **Use o perfil atual para entrar em sites quando várias contas corporativas ou de estudante estiverem conectadas em um dispositivo.** Quando várias contas corporativas ou de estudante estiverem conectadas em um dispositivo, os usuários deverão escolher uma conta no seletor de contas para continuar suas visitas a sites. Nesta versão, os usuários serão solicitados a permitir que o Microsoft Edge entre nos sites automaticamente com a conta corporativa ou de estudante conectada ao perfil atual. Os usuários podem ativar e desativar esse recurso em **Configurações** > **Preferências de perfil**.

- **Adicione suporte para a Prevenção contra Perda de Dados de Ponto de Extremidade (DLP) da Microsoft no macOS.** A aplicação da política do Microsoft Endpoint DLP estará disponível nativamente no macOS.

- **HTTPS automático.** Os usuários podem atualizar as navegações de HTTP para HTTPS em domínios que provavelmente suportam esse protocolo mais seguro. Esse suporte também pode ser configurado para tentar entrega HTTPS para todos os domínios. Nota: Esta recurso é uma distribuição de Recurso Controlado. Se não encontrar esse recurso, verifique novamente enquanto continuamos nossa distribuição.

- **Bloqueie o WebSQL em contextos de terceiros.** O uso do recurso WebSQL herdado será bloqueado em quadros de terceiros. A política [WebSQLInThirdPartyContextEnabled](/deployedge/microsoft-edge-policies#websqlinthirdpartycontextenabled) está disponível como uma opção de recusa até a versão 101 do Microsoft Edge. Essa alteração está acontecendo no projeto do Chromium no qual o Microsoft Edge se baseia. Para obter mais informações, confira a entrada [Status da plataforma Chrome](https://chromestatus.com/feature/5684870116278272).

- **Citações no Microsoft Edge.** Citar fontes para pesquisa é um requisito comum para estudantes. Eles têm que gerenciar muitas referências e fontes de pesquisa, o que não é uma tarefa fácil. Eles também precisam traduzir essas citações para formatos de citação adequados, como APA, MLA e Chicago. Esse novo recurso "Citações", agora em Versão prévia no Microsoft Edge, oferece aos alunos uma maneira melhor de gerenciar e gerar citações conforme eles pesquisam online. Com as citações ativadas em Coleções ou em **Configurações e muito mais (Alt-F)**, o Microsoft Edge gera automaticamente citações que os alunos podem usar mais tarde para que possam se concentrar em suas pesquisas. Quando terminarem, eles podem facilmente compilar essas citações em uma entrega final. Para obter mais informações, confira [Visualizando Citações no Microsoft Edge](https://blogs.windows.com/msedgedev/2021/11/04/preview-citations-feature-edge/).

- **Proteção de Fluxo de Controle (CFG).** O Microsoft Edge começará a suportar uma proteção mais refinada, combatendo vulnerabilidades de corrupção de memória e protegendo chamadas indiretas. O CFG só é compatível com Windows 8 e posteriores. Para obter mais informações, confira [Proteção de Fluxo de Controle](/windows/win32/secbp/control-flow-guard).
  
  > [!NOTE]
  > Esta é uma tecnologia em evolução, compartilhe seus comentários para nos ajudar a fortalecer seu suporte.

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

## <a name="version-960105462-december-17"></a>Versão 96.0.1054.62: 17 de dezembro

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-960105457-december-14"></a>Versão 96.0.1054.57: 14 de dezembro

> [!Important]
> Esta atualização contém uma correção para [CVE-2021-4102](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-4102), que foi relatada pela equipe do Chromium como tendo uma exploração em execução. Para obter mais informações, consulte o [Guia de atualização de segurança](https://msrc.microsoft.com/update-guide).

As atualizações de segurança do canal Estável estão listadas [aqui](/deployedge/microsoft-edge-relnotes-security#december-14-2021).

## <a name="version-960105453-december-10"></a>Versão 96.0.1054.53: 10 de dezembro

As atualizações de segurança do canal Estável estão listadas [aqui](/deployedge/microsoft-edge-relnotes-security#december-10-2021).

## <a name="version-960105443-december-2"></a>Versão 96.0.1054.43: 2 de dezembro

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-960105441-november-30"></a>Versão 96.0.1054.41: 30 de novembro

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-960105434-november-23"></a>Versão 96.0.1054.34: 23 de novembro

Correção de vários bugs e problemas de desempenho.

## <a name="version-960105429-november-19"></a>Versão 96.0.1054.29: 19 de novembro

As atualizações de segurança do canal Estável estão listadas [aqui](/deployedge/microsoft-edge-relnotes-security#november-19-2021).

### <a name="feature-updates"></a>Atualizações de recursos

- **Gerenciamento de Lista de Sites na Nuvem para o modo IE na Visualização Pública.** O Gerenciamento de Lista de Sites na Nuvem permite que você gerencie suas listas de sites para o modo IE na nuvem sem precisar de uma infraestrutura local para hospedar a lista de sites da sua organização. Você pode acessar o recurso Gerenciamento de Lista de Sites na Nuvem usando a experiência de Listas de Sites do Microsoft Edge no Administração Microsoft 365 Center. Para saber mais, confira o artigo [Gerenciamento de Lista de Sites na Nuvem para modo IE (Versão Prévia](./edge-ie-mode-cloud-site-list-mgmt.md) Pública).
  
- **Entrega aprimorada entre o modo IE e o navegador moderno.** A partir desta versão do Microsoft Edge, as navegação entre o Microsoft Edge e o modo Internet Explorer incluirão dados de formulário e cabeçalhos HTTP adicionais. Os cabeçalhos de referenciador, os dados de postagem, os dados de formulários e os métodos de solicitação serão encaminhados corretamente entre as duas experiências. Você pode especificar quais tipos de dados devem ser incluídos usando a política InternetExplorerIntegrationComplexNavDataTypes. Para obter mais informações, consulte as perguntas frequentes: [Meu aplicativo requer a transferência de dados POST entre o modo IE e o Microsoft Edge. Há suporte para isso?](./edge-ie-mode-faq.md#my-application-requires-transferring-post-data-between-ie-mode-and-microsoft-edge-is-this-supported)

- **Atualize o Microsoft Edge WebView2 usando o WSUS.** Os administradores de TI que Windows Server Update Services (WSUS) para atualizar o Microsoft Edge também poderão atualizar o Microsoft Edge WebView2 usando o WSUS. Essa funcionalidade oferece aos administradores um processo de manutenção mais fácil para dispositivos offline.

- **Atualizações do WSUS para o Servidor.** As atualizações do WSUS e do Catálogo para canais do Microsoft Edge (Estável, Beta e Desenvolvimento) agora serão aplicadas a SKUs do Windows Server que têm o Microsoft Edge instalado, incluindo o Windows Server 2022. Para obter mais informações sobre como configurar atualizações do WSUS para o Microsoft Edge, consulte [Atualizar o Microsoft Edge](/mem/configmgr/apps/deploy-use/deploy-edge).

- **Componente de Protocolos de Inicialização Automática do Microsoft Edge.** O Microsoft Edge 96 apresenta o componente AutoLaunch [Protocols que](https://textslashplain.com/2019/07/16/updating-browsers-quickly-flags-respins-and-components/) contém listas de dicionários de origem de esquema para permitir ou bloquear automaticamente. Isso protege os clientes contra esquemas perigosos (por exemplo, um manipulador de protocolo com um dia) ao eliminar prompts de emparelhamentos seguros conhecidos (por exemplo, o site do Teams pode abrir o aplicativo cliente do Teams). Se, por algum motivo, você não quiser que o Microsoft Edge bloqueie manipuladores de protocolo vulneráveis e permita emparelhamentos seguros conhecidos, use a alternância no edge://settings/content/applicationLinks ou defina *a* política [AutoLaunchProtocolsComponentEnabled](/deployedge/microsoft-edge-policies#autolaunchprotocolscomponentenabled) como False.

- **Inicie o PWA (Aplicativo Web Progressivo) diretamente por meio de links de protocolo.** Permita que os PWAs instalados manipulem links que usam um protocolo específico para uma experiência mais integrada.

- **Exiba rapidamente os arquivos do Office no navegador.** Os usuários agora podem exibir arquivos do Office, incluindo documentos, planilhas e apresentações que eles podem encontrar ao navegar no Microsoft Edge no navegador, sem precisar baixar o arquivo e abri-lo em um aplicativo diferente. Não haverá alterações na experiência de abertura de arquivo para arquivos do Office hospedados no OneDrive ou no SharePoint.
  
- **Realce de forma livre em PDFs.** A experiência de exibição e marcação em PDF é aprimorada com a adição de marcadores de forma livre. Você pode realçar seções em PDFs às qual não tem acesso e documentos digitalizados.

- **Proteção de pilha imposta por hardware.** O Microsoft Edge começará a dar suporte a um modo de navegação ainda mais seguro que usa o fluxo de controle dependente de hardware para processos de navegador em hardware com suporte (Intel 11ª Geração. ou AMD Zen 3). Observação: como esta é uma Distribuição de Recursos Controlada, talvez você não observe esse recurso habilitado em todos os dispositivos. Você pode habilitar ou desabilitar a Proteção contra Pilha imposta por hardware manipulando IFEO (Opções de Execução de Arquivo de Imagem) usando a política de grupo.

- **Nova caixa de diálogo de aviso para sites de typosquatting.** O navegador mostrará um aviso em alguns sites com URLs muito semelhantes a outros sites. Essa interface do usuário usa heurística do lado do cliente para avisar os usuários sobre sites que podem estar falsificando sites populares. Para obter mais informações, consulte [O que é typosquatting?](https://support.microsoft.com/topic/what-is-typosquatting-54a18872-8459-4d47-b3e3-d84d9a362eb0).
  
- **Dicionário adicionado à minibarra de ferramentas Leitura Avançada.**  Estamos adicionando funcionalidade de dicionário à minibarra de ferramentas para ajudar na leitura e na pesquisa. Você poderá pesquisar a ortografia e as definições de palavras com mais rapidez e facilidade na Leitura Avançada experiência.
  
- **Saiba como resolver problemas matemáticos com o Math Solver.** Estamos felizes em anunciar que você pode usar o Math Solver no Microsoft Edge para obter ajuda com uma ampla variedade de conceitos matemáticos. Esses conceitos variam de equações aritméticas e quadráticas elementares a trigonometria e cálculo. O Math Solver permite que você tire uma foto de um problema de matemática manuscrito ou impresso e, em seguida, fornece uma solução instantânea com instruções passo a passo para ajudá-lo a aprender a alcançar a solução sem ajuda. O Math Solver também vem com um teclado matemático que você pode usar para digitar facilmente problemas matemáticos. Esse teclado elimina a necessidade de pesquisar em torno de um teclado tradicional para encontrar os caracteres matemáticos necessários. Depois de resolver o problema, o Math Solver fornece opções para continuar aprendendo com testes, planilhas e tutoriais em vídeo.

- **Suporte à VPN de túnel dividido para WebRTC.** Permite que os clientes corporativos obtenham o benefício do túnel dividido de VPN para tráfego ponto a ponto no Microsoft Edge. Você pode habilitar esse recurso usando a [política WebRtcRespectOsRoutingTableEnabled](/deployedge/microsoft-edge-policies#webrtcrespectosroutingtableenabled) .

### <a name="policy-updates"></a>Atualizações de política

#### <a name="new-policies"></a>Novas Políticas

- [ApplicationGuardUploadBlockingEnabled](/DeployEdge/microsoft-edge-policies#applicationguarduploadblockingenabled) – impede que os arquivos sejam carregados no Application Guard
- [AudioProcessHighPriorityEnabled](/DeployEdge/microsoft-edge-policies#audioprocesshighpriorityenabled) – Permitir que o processo de áudio seja executado com prioridade acima do normal no Windows
- [AutoLaunchProtocolsComponentEnabled](/DeployEdge/microsoft-edge-policies#autolaunchprotocolscomponentenabled) – Componente de protocolos autoLaunch habilitado
- [EfficiencyMode](/DeployEdge/microsoft-edge-policies#efficiencymode) – Configurar quando o modo de eficiência deve ficar ativo
- [ForceSyncTypes](/DeployEdge/microsoft-edge-policies#forcesynctypes) – Configurar a lista de tipos incluídos para sincronização
- [InternetExplorerIntegrationComplexNavDataTypes](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationcomplexnavdatatypes) – Configure se os dados de formulário e os cabeçalhos HTTP serão enviados ao entrar ou sair do modo Internet Explorer
- [InternetExplorerModeToolbarButtonEnabled](/DeployEdge/microsoft-edge-policies#internetexplorermodetoolbarbuttonenabled) – mostrar o botão Recarregar no modo Internet Explorer na barra de ferramentas
- [PrintPostScriptMode](/DeployEdge/microsoft-edge-policies#printpostscriptmode) – Modo PostScript de Impressão
- [PrintRasterizePdfDpi](/DeployEdge/microsoft-edge-policies#printrasterizepdfdpi) – Imprimir Rasterizar PDF DPI
- [RendererAppContainerEnabled](/DeployEdge/microsoft-edge-policies#rendererappcontainerenabled) – Habilitar o renderizador no contêiner do aplicativo
- [SharedLinksEnabled](/DeployEdge/microsoft-edge-policies#sharedlinksenabled) – Mostrar links compartilhados de aplicativos do Microsoft 365 no Histórico
- [TyposquattingCheckerEnabled](/DeployEdge/microsoft-edge-policies#typosquattingcheckerenabled) – Configurar TyposquattingChecker de Borda

## <a name="version-950102053-november-12"></a>Versão 95.0.1020.53: 12 de novembro

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-950102044-november-4"></a>Versão 95.0.1020.44: 4 de novembro

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-94099258-october-30"></a>Versão 94.0.992.58: 30 de outubro

Correção de vários bugs e problemas de desempenho para a versão Estável Estendida.

## <a name="version-950102040-october-29"></a>Versão 95.0.1020.40: 29 de outubro

> [!IMPORTANT]
> Esta atualização contém uma correção para [CVE-2021-38000](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-38000) e [CVE-2021-38003](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-38003) que foram relatadas pela equipe Chromium como tendo uma exploração na natureza. Para obter mais informações, consulte o [Guia de Atualização de Segurança](https://msrc.microsoft.com/update-guide)

As atualizações de segurança do canal Estável estão listadas [aqui](/deployedge/microsoft-edge-relnotes-security#october-29-2021).

## <a name="version-950102038-october-28"></a>Versão 95.0.1020.38: 28 de outubro

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-94099257-october-27"></a>Versão 94.0.992.57: 27 de outubro

Correção de vários bugs e problemas de desempenho para a versão Estável Estendida.

## <a name="version-950102030-october-21"></a>Versão 95.0.1020.30: 21 de outubro

As atualizações de segurança do canal estável estão listadas [aqui](/deployedge/microsoft-edge-relnotes-security#october-21-2021).

### <a name="feature-updates"></a>Atualizações de recursos

- **Veja no Explorador de Arquivos o suporte para bibliotecas do Microsoft Office SharePoint Online no Microsoft Edge.**  Agora você pode habilitar o recurso Exibir no explorador de arquivos nas Bibliotecas de Documentos Modernos do Microsoft Office SharePoint Online. Para que esta experiência seja visível e funcione para seus usuários, você precisa ativar a política do Microsoft Edge [Configurar a funcionalidade Exibir no explorador de arquivos para páginas do SharePoint no Microsoft Edge](/deployedge/microsoft-edge-policies#configureviewinfileexplorer) e atualizar sua configuração de locatário do Microsoft Office SharePoint Online. Saiba mais: [Veja arquivos Microsoft Office SharePoint Online com o Explorador de arquivo no Microsoft Edge](/SharePoint/sharepoint-view-in-edge).

- **Os links de URL do arquivo de zona da intranet serão abertos no Windows Explorador de Arquivos.**  Você pode permitir links de URL de arquivos para arquivos da zona intranet originários de sites HTTPS da zona intranet para abrir o Windows Explorador de Arquivos para esse arquivo ou diretório. Você pode habilitar esta experiência usando a política [IntranetFileLinksEnabled](/deployedge/microsoft-edge-policies#intranetfilelinksenabled).

- **Melhorias na experiência de downloads.** O suporte para o download da experiência do usuário é estendido para aplicativos progressivos de web PWAs e WebView. Também começaremos a suportar o arrastar e soltar para o Explorador de Arquivos e Desktop.

- **Continue de onde parou em documentos PDF.**  Agora você poderá retomar a leitura de onde você fechou seu documento PDF pela última vez.

- **O modo de eficiência estende a vida útil da bateria quando seu laptop entra em modo de economia de bateria.**  O modo de eficiência ficará ativo quando seu laptop entrar no modo de economia de bateria para permitir que o navegador gerencia o uso de recursos para aumentar a vida útil da bateria de sua máquina. Você terá quatro opções quando o modo de eficiência se tornar ativo: Desligado e bateria fraca, Desligado, Sempre, e Nunca. Nota: Esta recurso é uma distribuição de Recurso Controlado. Se você não vê este recurso, verifique em breve enquanto continuamos nossa distribuição.

- **Caixas de texto de formulário livre adicionadas aos documentos PDF.** Agora damos suporte à adição de caixas de texto de formulário livre a documentos PDF. Você pode usar estas caixas para preencher formulários e adicionar notas visíveis.

- **Suporte de citação adicionado às Coleções.**  Melhoramos a experiência das Coleções, especialmente para alunos e pesquisadores. As coleções começarão a apoiar citações e listas de leitura.

- **Atualizar suas senhas mais rapidamente e com menos cliques.** O navegador agora o levará diretamente para a página Alterar Senha de um determinado site. Esta ação economiza tempo e cliques ao remover a necessidade de navegar para a página manualmente. Depois que você estiver nesta página, o navegador também irá preencher automaticamente sua senha existente e sugerirá uma nova senha forte e única.  Nota: Atualmente esta recurso está disponível apenas em um número limitado de sites.

- **Criação automática de conta.** Agora oferecemos suporte adicional nas páginas de Inscrição, permitindo que você crie uma conta online com um clique. Você pode fazer isso selecionando o lista pendente de sugestões ao clicar em qualquer campo do formulário no formulário de Inscrição. Fazendo isso, não só mostrará informações relevantes para o formulário de Inscrição, mas também uma forte sugestão de nova senha. Após a seleção, todas as informações relevantes são preenchidas nos respectivos campos e a senha sugerida será automaticamente armazenada ao ser enviada para o site. Nota: Atualmente esta recurso está disponível apenas em um número limitado de sites.

### <a name="policy-updates"></a>Atualizações de política

#### <a name="new-policies"></a>Novas Políticas

- [BrowserLegacyExtensionPointsBlockingEnabled](/DeployEdge/microsoft-edge-policies#browserlegacyextensionpointsblockingenabled) Habilitar o bloqueio do ponto de extensão do navegador
- [CrossOriginWebAssemblyModuleSharingEnabled](/DeployEdge/microsoft-edge-policies#crossoriginwebassemblymodulesharingenabled) Especifica se os módulos WebAssembly podem ser enviados entre origens
- [DisplayCapturePermissionsPolicyEnabled](/DeployEdge/microsoft-edge-policies#displaycapturepermissionspolicyenabled) Especifica se as permissões de captura de exibição política é verificada ou ignorada
- [InternetExplorerIntegrationWindowOpenHeightAdjustment](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationwindowopenheightadjustment) Configurar o ajuste de pixels entre as alturas do modo window.open, com origem nas páginas do modo IE vs. páginas do modo Edge
- [InternetExplorerIntegrationWindowOpenWidthAdjustment](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationwindowopenwidthadjustment) Configurar o ajuste de pixels entre as larguras do modo window.open com origem nas páginas do modo IE vs. páginas do modo Edge
- [IntranetFileLinksEnabled](/DeployEdge/microsoft-edge-policies#intranetfilelinksenabled) Permitir que links de URL de arquivos de zona da intranet da Microsoft Edge sejam abertos no Explorador de Arquivos do Windows
- [NewSmartScreenLibraryEnabled](/DeployEdge/microsoft-edge-policies#newsmartscreenlibraryenabled) Habilitar a nova biblioteca SmartScreen
- [ShadowStackCrashRollbackBehavior](/DeployEdge/microsoft-edge-policies#shadowstackcrashrollbackbehavior) Configurar o comportamento do ShadowStack rollback
- [VisualSearchEnabled](/DeployEdge/microsoft-edge-policies#visualsearchenabled) Pesquisa visual habilitada

#### <a name="obsoleted-policies"></a>Políticas Obsoletas

- [InternetExplorerIntegrationTestingAllowed](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationtestingallowed) - Permitir teste no modo Internet Explorer.
- [LegacySameSiteCookieBehaviorEnabled](/DeployEdge/microsoft-edge-policies#legacysamesitecookiebehaviorenabled) Habilitar configuração padrão de comportamento de cookie SameSite herdado

## <a name="version-94099250-october-14"></a>Versão 94.0.992.50: 14 de outubro

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-94099247-october-11"></a>Versão 94.0.992.47:11 de outubro

As atualizações de segurança do canal Estável estão listadas [aqui](/deployedge/microsoft-edge-relnotes-security#october-11-2021).

## <a name="version-94099238-october-1"></a>Versão 94.0.992.38: 01 de outubro

> [!Important]
> Esta atualização contém uma correção para [CVE-2021-37975](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-37975) e [CVE-2021-37976](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-37976), que foram relatadas pela equipe do Chromium como tendo uma exploração em execução. Para obter mais informações, consulte o [Guia de Atualização de Segurança](https://msrc.microsoft.com/update-guide)

As atualizações de segurança do canal Estável estão listadas [aqui](/deployedge/microsoft-edge-relnotes-security#october-01-2021).

## <a name="version-94099237-september-30"></a>Versão 94.0.992.37: 30 de setembro

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-94099231-september-24"></a>Versão 94.0.992.31: 24 de setembro

> [!Important]
> Essa atualização contém uma correção para [o CVE-2021-37973,](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-37973) que foi relatada pela equipe Chromium como tendo uma exploração na natureza. Para obter mais informações, confira o [Guia de Atualização de Segurança](https://msrc.microsoft.com/update-guide).

As atualizações de segurança do canal Estável estão listadas [aqui](/deployedge/microsoft-edge-relnotes-security#september-24-2021).

### <a name="feature-updates"></a>Atualizações de recursos

- **O Microsoft Edge concluiu a mudança para uma cadência de 4 semanas para atualizações.**  Adotamos um novo ciclo de lançamento de 4 semanas para as versões principais. Leia mais aqui: https://blogs.windows.com/msedgedev/2021/03/12/new-release-cycles-microsoft-edge-extended-stable/

- **Nova opção estável estendida sendo oferecida.**  Estamos oferecendo uma nova opção Estável Estendida para nossos clientes Empresariais gerenciados. A opção Estável Estendida permanecerá em revisões pares e será atualizada a cada 8 semanas. Haverá uma atualização de segurança quinzenal.  Informações adicionais aqui: https://blogs.windows.com/msedgedev/2021/07/15/opt-in-extended-stable-release-cycle/

- **Melhorias no comportamento padrão de abertura de arquivos MHTML.**  Os arquivos MHTML continuarão a abrir no modo IE se o modo IE estiver habilitado, a menos que o arquivo MHTML tenha sido salvo do Microsoft Edge (usando as opções Salvar como ou Salvar página como no Microsoft Edge). Se o arquivo foi salvo do Microsoft Edge, ele agora será aberto no Microsoft Edge.  Essa alteração corrigirá um problema de renderização observado ao abrir um arquivo MHTML no modo IE quando salvo no Microsoft Edge.

- **Restrinja as solicitações de rede privada para proteger contextos.** O acesso a recursos em redes locais (intranet) a partir de páginas na Internet requer que essas páginas sejam entregues por HTTPS. Essa alteração está ocorrendo no projeto Chromium, no qual o Microsoft Edge se baseia. Para obter mais informações, navegue até a [entrada de Status da Plataforma Chrome.](https://chromestatus.com/feature/5436853517811712) Duas políticas de compatibilidade estão disponíveis para oferecer suporte a cenários que precisam preservar a compatibilidade com páginas não seguras: [InsecurePrivateNetworkRequestAllowed](/deployedge/microsoft-edge-policies#insecureprivatenetworkrequestsallowed) e [InsecurePrivateNetworkRequestAllowedForUrls](/deployedge/microsoft-edge-policies#insecureprivatenetworkrequestsallowedforurls).

- **Bloqueie downloads de conteúdo misto.** As páginas seguras só baixarão arquivos hospedados em outras páginas seguras, e os downloads hospedados em páginas não seguras (não HTTPS) serão bloqueados se iniciados em uma página segura. Essa alteração está ocorrendo no projeto Chromium, no qual o Microsoft Edge se baseia. Para obter mais informações, navegue até a [entrada do blog de segurança do Google](https://security.googleblog.com/2020/02/protecting-users-from-insecure_6.html).

- **Habilite o login implícito para contas locais.** Ao habilitar a política [OnlyOnPremisesImplicitSigninEnabled](/deployedge/microsoft-edge-policies#onlyonpremisesimplicitsigninenabled), apenas contas locais serão habilitadas para login implícito.  O Microsoft Edge não tentará entrar implicitamente em contas MSA ou AAD. A atualização de contas locais para contas do AAD também será interrompida.

- **Nova página de configurações de acessibilidade.**  Reunimos as configurações relacionadas à acessibilidade em uma única página. Você pode localizar a nova página edge: //settings/accessibility na lista de configurações principal. Aqui você pode localizar configurações para aumentar a página da web, mostrar um contorno de alta visibilidade ao redor da área de foco e outras configurações que podem ajudar a melhorar sua experiência de navegação na web. Continuaremos adicionando novas configurações aqui em versões futuras do Microsoft Edge.

***Novas Políticas***

- [ApplicationGuardPassiveModeEnabled](/DeployEdge/microsoft-edge-policies#applicationguardpassivemodeenabled) Ignorar a configuração da lista de sites do Application Guard e navegar no Edge normalmente
- [OnlyOnPremisesImplicitSigninEnabled](/DeployEdge/microsoft-edge-policies#onlyonpremisesimplicitsigninenabled) Apenas conta local habilitada para entrada implícita
- [WebRtcRespectOsRoutingTableEnabled](/DeployEdge/microsoft-edge-policies#webrtcrespectosroutingtableenabled) Habilite o suporte para regras de tabela de roteamento do sistema operacional Windows ao fazer conexões ponto a ponto via WebRTC

***Política Obsoleta***

- [UserAgentClientHintsEnabled](/DeployEdge/microsoft-edge-policies#useragentclienthintsenabled) Habilite o recurso de Dicas de Cliente do Agente do Usuário

## <a name="version-93096152-september-16"></a>Versão 93.0.961.52: 16 de setembro

>[!Important]
>Esta atualização contém uma correção para [CVE-2021-30633](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-30632) que foi relatada pela equipe Chromium como tendo uma exploração em execução. Para obter mais informações, confira o [Guia de Atualização de Segurança](https://msrc.microsoft.com/update-guide).

As atualizações de segurança do canal estável estão listadas [aqui](/deployedge/microsoft-edge-relnotes-security#september-16-2021).

## <a name="version-93096147-september-11"></a>Versão 93.0.961.47: 11 de setembro

> [!Important]
> Esta atualização contém uma correção para [CVE-2021-30632](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-30632) que foi relatado pela equipe do Chromium como tendo um exploit. Para obter mais informações, confira o [Guia de Atualização de Segurança](https://msrc.microsoft.com/update-guide).

As atualizações de segurança do canal estável estão listadas [aqui](/deployedge/microsoft-edge-relnotes-security#september-11-2021).

## <a name="version-93096144-september-9"></a>Versão 93.0.961.44: 9 de setembro

As atualizações de segurança do canal estável estão listadas [aqui](/deployedge/microsoft-edge-relnotes-security#september-09-2021).

## <a name="version-93096138-september-2"></a>Versão 93.0.961.38: 2 de setembro

As atualizações de segurança do canal estável estão listadas [aqui](/deployedge/microsoft-edge-relnotes-security#september-02-2021).

### <a name="feature-updates"></a>Atualizações de recursos

- **Preferências Iniciais no Microsoft Edge.**  O Microsoft Edge agora oferece suporte a um número limitado de Preferências Iniciais (anteriormente Preferências Mestre). Os administradores de IT podem implantar essas configurações como padrão antes que o navegador seja executado pela primeira vez por seus usuários. Informações adicionais aqui: [Configurar o Microsoft Edge usando as configurações de Preferências Iniciais para a primeira execução](/deployedge/initial-preferences-support-on-microsoft-edge-browser).

- **O modo IE no Microsoft Edge dará suporte ao comportamento "sem mesclagem".**  Para um usuário final, quando uma nova janela do navegador é lançada de um aplicativo de modo IE, ela estará em uma sessão separada, semelhante ao comportamento sem mesclagem no IE11. Você precisará ajustar sua lista de sites para configurar sites que precisam impedir o compartilhamento de sessão como "sem mesclagem". Nos bastidores, para cada janela do Microsoft Edge, a primeira vez que uma guia de modo IE é visitada dentro dessa janela, se for um dos sites designados "sem mesclagem", essa janela será bloqueada em uma sessão do IE "sem mesclagem" diferente de todas as outras janelas do Microsoft Edge pelo menos até que a última guia de modo IE seja fechada nessa janela. Isso segue o comportamento anterior em que os usuários podem iniciar o IE sem mesclagem e também podem iniciar o Microsoft Edge sem mesclagem por meio de outros mecanismos.  Informações adicionais aqui: [solução de problemas de modo IE e perguntas frequentes | Microsoft Docs](/deployedge/edge-ie-mode-faq#does-ie-mode-on-microsoft-edge-support-the--nomerge--option-that-was-supported-in-internet-explorer-11-)

- **Nova política para interromper a entrada implícita.**  A política [ImplicitSignInEnabled](/deployedge/microsoft-edge-policies#implicitsigninenabled) permite que os administradores do sistema desabilitem a entrada implícita em navegadores Microsoft Edge.

- **Políticas para ignorar prompts do ClickOnce e DirectInvoke.** Atualizamos nossas políticas para permitir ignorar prompts do ClickOnce e o aplicativo do DirectInvoke para tipos de arquivo especificados, de domínios especificados. Para fazer isso, você precisará:

  - Habilitar [ClickOnceEnabled](/deployedge/microsoft-edge-policies#clickonceenabled) ou [DirectInvokeEnabled](/deployedge/microsoft-edge-policies#directinvokeenabled)
  - Habilitar a política [AutoOpenFileTypes](/deployedge/microsoft-edge-policies#autoopenfiletypes) e definir a lista de tipos de arquivo específicos para os quais ClickOnce e DirectInvoke devem ser desabilitados
  - Habilitar a política [AutoOpenAllowedForURLs](/deployedge/microsoft-edge-policies#autoopenallowedforurls) e definir a lista de domínios específicos para os quais ClickOnce e DirectInvoke serão desabilitados.

  Observação: AutoOpenAllowedForURLs é uma política de suporte para AutoOpenFileTypes. Se AutoOpenAllowedForURLs não estiver definido e AutoOpenFileTypes estiver definido, os tipos de arquivo listados abrirão automaticamente de todas as URLs.

- **Grupos de Guias.**  Estamos ativando o grupo de guias que oferece a capacidade de categorizar guias em grupos definidos pelo usuário e ajuda você a encontrar, alternar e gerenciar guias com mais eficiência em vários fluxos de trabalho.  

- **Ocultar a barra de título ao usar Guias Verticais.**  Obtenha os pixels extras de volta ocultando a barra de título do navegador, enquanto estiver em Guias Verticais. Agora você pode ir para edge://settings/appearance e, na seção Personalizar Barra de Ferramentas, selecione a opção para ocultar a barra de título enquanto estiver no modo Guia Vertical.

- **Video em Picture-in-Picture (PiP) da barra de ferramentas de foco.**  Quando você passar o mouse sobre um vídeo com suporte, aparecerá uma barra de ferramentas que permite que você veja esse vídeo em uma janela PiP.  Observe que, no momento, isso está disponível para usuários do Microsoft Edge no macOS.  

- **Remoção do 3DES no TLS. O suporte para o pacote de codificação TLS_RSA_WITH_3DES_EDE_CBC_SHA será removido.** Essa alteração está ocorrendo no projeto Chromium, no qual o Microsoft Edge se baseia. Para obter mais informações, navegue até a [entrada de Status da Plataforma Chrome.](https://chromestatus.com/feature/6678134168485888) Além disso, no Microsoft Edge versão 93, a política [TripleDESEnabled](/deployedge/microsoft-edge-policies#tripledesenabled) estará disponível para dar suporte a cenários que precisam preservar a compatibilidade com servidores desatualizados. Essa política de compatibilidade se tornará obsoleta e não funcionará no Microsoft Edge versão 95. Certifique-se de atualizar os servidores afetados antes disso.

***Novas políticas***

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
- [WAMAuthBelowWin10RS3Enabled](/DeployEdge/microsoft-edge-policies#wamauthbelowwin10rs3enabled) para autenticação abaixo do Windows 10 RS3 habilitado

***Política Preterida***

- [LegacySameSiteCookieBehaviorEnabled](/DeployEdge/microsoft-edge-policies#legacysamesitecookiebehaviorenabled) Habilitar configuração padrão de comportamento de cookie SameSite herdado

***Política Obsoleta***

- [NewTabPageSetFeedType](/DeployEdge/microsoft-edge-policies#newtabpagesetfeedtype) Configure Microsoft Edge nova experiência de página da guia

***Alteração Adicional***

- [ConfigureShare](/DeployEdge/microsoft-edge-policies#configureshare) adicionar suporte à plataforma mac
- [PasswordMonitorAllowed](/DeployEdge/microsoft-edge-policies#passwordmonitorallowed) Adicionar suporte à plataforma mac

## <a name="version-92090284-august-26"></a>Versão 92.0.902.84: 26 de agosto

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-92090278-august-19"></a>Versão 92.0.902.78: 19 de agosto

As atualizações de segurança do canal estável estão listadas [aqui](/deployedge/microsoft-edge-relnotes-security#august-19-2021).

## <a name="version-92090273-august-12"></a>Versão 92.0.902.73: 12 de agosto

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-92090267-august-5"></a>Versão 92.0.902.67: 5 de agosto

As atualizações de segurança do canal Estável estão listadas [aqui](/deployedge/microsoft-edge-relnotes-security#august-05-2021).

## <a name="version-92090262-july-29"></a>Versão 92.0.902.62: 29 de julho

Vários bugs e problemas de desempenho corrigidos.

### <a name="modified-policy"></a>Política modificada

- AutoplayAllowed: definir como “Desabilitado” agora define a reprodução automática de mídia como “Limite”

## <a name="version-92090255-july-22"></a>Versão 92.0.902.55: 22 de julho

As atualizações de segurança do canal Estável estão listadas [aqui](/deployedge/microsoft-edge-relnotes-security#july-22-2021).

### <a name="feature-updates"></a>Atualizações de recursos

**Os usuários podem acessar facilmente o modo Internet Explorer no Microsoft Edge**. A partir da versão 92 do Microsoft Edge, os usuários podem recarregar um site no modo Internet Explorer no Microsoft Edge em vez de depender do aplicativo autônomo do IE 11 enquanto aguardam a configuração de um site na Lista de Sites do Modo Empresarial. Os usuários serão solicitados a adicionar o site à sua lista de sites locais de forma que a navegação para a mesma página no Microsoft Edge seja renderizada automaticamente no modo IE pelos próximos 30 dias. Você pode usar a política [InternetExplorerIntegrationReloadInIEModeAllowed](/deployedge/microsoft-edge-policies#internetexplorerintegrationreloadiniemodeallowed) para configurar essa experiência e permitir o acesso aos pontos de entrada do modo IE, bem como a capacidade de adicionar sites à lista de sites locais. Você pode usar a política [InternetExplorerIntegrationLocalSiteListExpirationDays](/deployedge/microsoft-edge-policies#internetexplorerintegrationlocalsitelistexpirationdays) para ajustar o número de dias para manter os sites na lista de sites locais. Observe que KB5003698 ou posterior é necessário para Windows 10, versão 1909; ou KB5003690 ou posterior é necessário para Windows 10, versão 2004, Windows 10, versão 20H2 ou Windows 10, versão 21H1 para a experiência de ponta a ponta. Para obter mais informações, [consulte Lista de sites local no modo IE](/deployedge/edge-ie-mode-local-site-list).

**Os arquivos MHTML serão abertos por padrão no modo Internet Explorer**. A partir do Microsoft Edge versão 92 Estável, os tipos de arquivo MHTML serão abertos automaticamente no modo Internet Explorer no Microsoft Edge em vez do aplicativo Internet Explorer (IE11). Isso é mais comumente observado ao tentar visualizar emails do Outlook em um navegador. Essa alteração ocorrerá apenas se o IE11 for o manipulador padrão para este tipo de arquivo. Se você preferir alterar isso, você pode fazê-lo antes de instalar a atualização da versão Estável 92 usando [ esta diretrizes](/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration).

**O aviso de "Desabilitar extensões do modo desenvolvedor" pode ser ignorado por 2 semanas**. A partir da versão 92 da Microsoft Edge, você pode adiar o aviso "Desabilitar extensões do modo desenvolvedor" por 2 semanas, selecionando a opção na caixa de diálogo de aviso.

**Gerenciar suas extensões diretamente da barra de ferramentas**. O novo menu de extensões na barra de ferramentas permitirá que você oculte/fixe extensões facilmente. Os links rápidos para gerenciar extensões e encontrar novas extensões facilitarão a localização de novas extensões e o gerenciamento das existentes.

**O padrão para reprodução automática será definido como Limite**.  Para ajudá-lo a manter seu foco online, mudamos o padrão para reprodução automática de mídia para Limite de Permitir, começando com a versão 92 do Microsoft Edge.

**Os instrumentos de pagamento agora são sincronizados entre dispositivos**. A partir do Microsoft Edge versão 92, você tem a opção de sincronizar suas informações de pagamento em seus dispositivos conectados. Observação: esta é uma Distribuição de Recursos Controlados. Se você não localizar esse recurso, volte em breve enquanto continuamos nossa distribuição.
Atualmente, esse recurso está disponível apenas nos EUA e somente para usuários MSA (não AAD)

**Melhorias na renderização de fontes**. Foram feitas melhorias na renderização do texto para melhorar a clareza e reduzir o borrão. Observação: esta é uma Distribuição de Recursos Controlados. Se você não localizar esse recurso, volte em breve enquanto continuamos nossa distribuição.

**Recursos de botão da barra de ferramentas, como Favoritos e Coleções, lembrarão a escolha do usuário de fixá-los ao lado da janela**. Agora habilitado por padrão, se o usuário optar por fixar um botão da barra de ferramentas, ele sempre abrirá no estado fixado até que ele decida desafixar.

**Os usuários agora podem gerenciar a opção "Permitir o login único para sites de trabalho ou de escola usando esse perfil" por meio da política de grupo**.  A opção “Permitir logon único para sites de trabalho ou de escola usando este perfil” permite que perfis não AAD possam usar o logon único para sites corporativos ou de escola usando as credenciais corporativas ou de escola presentes no computador. Essa opção aparece para os usuários finais como uma alternância em Configurações -> Perfis -> Preferências de Perfil somente para perfis não AAD.  Você pode usar a política [AADWebSiteSSOUsingThisProfileEnabled](/deployedge/microsoft-edge-policies#aadwebsitessousingthisprofileenabled) para configurar o comportamento.  

**Integridade da senha** É importante usar senhas fortes e exclusivas em diferentes contas para manter a segurança online. No entanto, isso é mais fácil de dizer do que fazer e a maioria dos usuários exibe hábitos de senha ruins, como usar senhas fracas que são fáceis de adivinhar ou reutilizar as mesmas senhas fortes entre contas.

Com esta versão mais recente do Microsoft Edge, sua tarefa de usar senhas fortes e exclusivas fica um pouco mais fácil! O Microsoft Edge agora dirá se as senhas salvas são fortes o suficiente e também indicará se elas foram usadas em vários sites, ajudando você a se manter mais seguro online. Você pode encontrar suas informações de integridade de senha na lista de senhas salvas na página edge://settings/passwords.
  
**Privacidade adicionada para suas senhas salvas** Se você estiver usando um dispositivo que compartilha com outras pessoas ou tiver deixado seu computador desbloqueado por qualquer motivo, agora você pode optar por uma segunda verificação usando sua senha de dispositivo para evitar que outras pessoas tenham acesso às senhas do seu site. Simples!

**Extensão do Outlook**.  Fique por dentro da caixa de entrada do Microsoft Outlook, calendário, tarefas e muito mais sem precisar abrir uma nova janela do navegador.  Você pode obter a nova extensão do Outlook aqui: [Microsoft Outlook - Complementos do Microsoft Edge](https://microsoftedge.microsoft.com/addons/detail/microsoft-outlook/kkpalkknhlklpbflpcpkepmmbnmfailf?hl=en-US)

**Em alinhamento com o Chromium de código aberto, Microsoft Edge atualiza a maneira como renderiza tabelas em páginas da Web.** Essa alteração corrige problemas conhecidos e Microsoft Edge mais perto da maneira especificada como as tabelas devem ser renderizações na Web/outros navegadores. Recomendamos que você teste fluxos de trabalho importantes em seu ambiente para problemas inesperados. Um explicador completo está disponível [aqui](https://docs.google.com/document/d/16PFD1GtMI9Zgwu0jtPaKZJ75Q2wyZ9EZnVbBacOfiNA/edit).

### <a name="new-policies"></a>Novas políticas

- [AADWebSiteSSOUsingThisProfileEnabled](/DeployEdge/microsoft-edge-policies#aadwebsitessousingthisprofileenabled)Logon único para sites de trabalho ou escola usando este perfil habilitado.
- [AutomaticHttpsDefault](/DeployEdge/microsoft-edge-policies#automatichttpsdefault) Configurar HTTPS Automático
- [HeadlessModeEnabled](/DeployEdge/microsoft-edge-policies#headlessmodeenabled) Controle o uso do Modo Sem Periféricos
- [InsecurePrivateNetworkRequestsAllowed](/DeployEdge/microsoft-edge-policies#insecureprivatenetworkrequestsallowed) Especifica se deve permitir que sites inseguros façam solicitações para pontos de extremidade de rede mais privada.
- [InsecurePrivateNetworkRequestsAllowedForUrls](/DeployEdge/microsoft-edge-policies#insecureprivatenetworkrequestsallowedforurls) Permite que os sites listados façam solicitações para pontos de extremidade de rede mais privada a partir de contextos inseguros
- [InternetExplorerIntegrationLocalSiteListExpirationDays](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationlocalsitelistexpirationdays) Especifique o número de dias que um site permanece na lista de sites do modo IE local
- [InternetExplorerIntegrationReloadInIEModeAllowed](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationreloadiniemodeallowed) Permite que sites não configurados sejam recarregados no modo Internet Explorer
- [SharedArrayBufferUnrestrictedAccessAllowed](/DeployEdge/microsoft-edge-policies#sharedarraybufferunrestrictedaccessallowed) Especifica se SharedArrayBuffers pode ser usado em um contexto não isolado de origem cruzada

### <a name="deprecated-policy"></a>Política Preterida

- [InternetExplorerIntegrationTestingAllowed](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationtestingallowed) - Permitir teste no modo Internet Explorer.

### <a name="obsoleted-policy"></a>Política Obsoleta

- [EnableSha1ForLocalAnchors](/DeployEdge/microsoft-edge-policies#enablesha1forlocalanchors) Permitir certificados assinados usando SHA-1 quando emitidos por âncoras de confiança locais.

## <a name="version-91086471-july-19"></a>Versão 91.0.864.71: 19 de julho

> [!Important]
>Esta atualização contém uma correção para [CVE-2021-30563](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-30563) que foi relatado pela equipe do Chromium como tendo um exploit. Para obter mais informações, confira o [Guia de Atualização de Segurança](https://msrc.microsoft.com/update-guide/vulnerability/ADV200002).

As atualizações de segurança do canal Estável estão listadas [aqui](/deployedge/microsoft-edge-relnotes-security#july-19-2021).

## <a name="version-91086467-july-8"></a>Versão 91.0.864.67: 8 de julho

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-91086464-july-2"></a>Versão 91.0.864.64: 2 de julho

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-91086459-june-24"></a>Versão 91.0.864.59: 24 de junho

As atualizações de segurança do canal estável estão listadas [aqui](/deployedge/microsoft-edge-relnotes-security#june-24-2021).

## <a name="version-91086454-june-18"></a>Versão 91.0.864.54: 18 de junho

> [!Important]
> Esta atualização contém uma correção para [CVE-2021-30554](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-30554) que foi relatado pela equipe do Chromium como tendo um exploit. Para obter mais informações, confira o [Guia de Atualização de Segurança](https://msrc.microsoft.com/update-guide/vulnerability/ADV200002).

As atualizações de segurança do canal estável estão listadas [aqui](/deployedge/microsoft-edge-relnotes-security#june-18-2021).

## <a name="version-91086448-june-11"></a>Versão 91.0.864.48: 11 de junho

> [!Important]
>Esta atualização contém uma correção para [CVE-2021-30551](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-30551) que foi relatada pela equipe Chromium como tendo uma exploração em execução. Para obter mais informações, confira o [Guia de Atualização de Segurança](https://msrc.microsoft.com/update-guide/vulnerability/ADV200002).

As atualizações de segurança do canal estável estão listadas [aqui](/deployedge/microsoft-edge-relnotes-security#june-11-2021).

## <a name="version-91086441-june-3"></a>Versão 91.0.864.41: 3 de junho

As atualizações de segurança do canal estável estão listadas [aqui](/deployedge/microsoft-edge-relnotes-security#june-3-2021).

## <a name="version-91086437-may-27"></a>Versão 91.0.864.37: 27 de maio

As atualizações de segurança do canal estável estão listadas [aqui](/deployedge/microsoft-edge-relnotes-security#may-27-2021).

### <a name="feature-updates"></a>Atualizações de recursos

- **Identifique o tráfego de rede originado dos contêineres do Microsoft Defender Application Guard no nível do proxy**. A partir da versão 91 do Microsoft Edge, há suporte integrado para marcar o tráfego de rede originado de contêineres do Application Guard, permitindo que as empresas os identifiquem e apliquem políticas específicas.

- **Opção de suporte para permitir a sincronização de favoritos do host para o contêiner do Edge Application Guard**. A partir do Microsoft Edge versão 91, os usuários têm a opção de configurar o Application Guard para sincronizar seus favoritos do host para o contêiner. Isso garante que novos favoritos também apareçam no contêiner.

- **A partir do Microsoft Edge versão 91, o navegador interromperá automaticamente os downloads de tipos que podem danificar seu computador se esses downloads forem iniciados sem a interação do usuário e não forem suportados pela verificação de Reputação de Aplicativo SmartScreen**. Os usuários podem substituir e continuar o download clicando com o botão direito e escolhendo “Manter” no item de download. Os administradores corporativos podem recusar esse comportamento configurando a seguinte política:
  - [ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](/deployedge/microsoft-edge-policies#exemptdomainfiletypepairsfromfiletypedownloadwarnings.md): Desabilita o download de avisos baseados em extensão do tipo de arquivo para tipos de arquivo especificados em domínios.

    Para obter mais informações, consulte [Interrupções de downloads na Segurança do Microsoft Edge](microsoft-edge-security-downloads-interruptions.md).

- **Suporte para APIs de Reconhecimento de Fala**. A partir da versão 91 do Microsoft Edge, o suporte API para comandos de reconhecimento de voz no Google.com e sites semelhantes será adicionado. Este recurso é limitado a um grupo selecionado aleatoriamente de usuários que habilitaram a experimentação. Esses usuários estão fazendo comentários para a equipe de recursos.

- **Personalize seu navegador com novas cores de tema**. Personalize o Microsoft Edge com uma das quatorze novas cores de tema na página Configurações -> Aparência. Você também pode instalar temas personalizados do site do Complemento do Microsoft Edge. [Saiba mais](https://techcommunity.microsoft.com/t5/articles/make-microsoft-edge-your-own-with-themes/m-p/2083165)

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

- [ProactiveAuthEnabled](./microsoft-edge-policies.md#proactiveauthenabled): habilita a Autenticação Proativa

## <a name="version-90081866-may-20"></a>Versão 90.0.818.66: 20 de maio

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-90081862-may-13"></a>Versão 90.0.818.62: 13 de maio

As atualizações de segurança do canal estável estão listadas [aqui](/deployedge/microsoft-edge-relnotes-security#may-13-2021).

## <a name="version-90081856-may-6"></a>Versão 90.0.818.56: 6 de maio

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-90081851-april-29"></a>Versão 90.0.818.51: 29 de abril

As atualizações de segurança do canal estável estão listadas [aqui](/deployedge/microsoft-edge-relnotes-security#april-29-2021).

## <a name="version-90081849-april-26"></a>Versão 90.0.818.49: 26 de abril

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-90081846-april-22"></a>Versão 90.0.818.46: 22 de abril ##

As atualizações de segurança do canal estável estão listadas [aqui](/deployedge/microsoft-edge-relnotes-security#april-22-2021).

## <a name="version-90081842-april-19"></a>Versão 90.0.818.42: 19 de abril

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-90081841-april-16"></a>Versão 90.0.818.41: 16 de abril ##

> [!Important]
>Esta atualização contém uma correção para [CVE-2021-21224](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-21224) que foi relatada pela equipe do Chromium como tendo uma exploração em execução. Para obter mais informações, confira o [Guia de Atualização de Segurança](https://msrc.microsoft.com/update-guide).

As atualizações de segurança do canal estável estão listadas [aqui](/deployedge/microsoft-edge-relnotes-security#april-16-2021).

## <a name="version-90081839-april-15"></a>Versão 90.0.818.39: 15 de abril ##

As atualizações de segurança do canal estável estão listadas [aqui](/deployedge/microsoft-edge-relnotes-security#april-15-2021).

## <a name="feature-updates"></a>Atualizações de recursos ##

-    **O Logon Único (SSO) agora está disponível para contas do Azure Active Directory (Azure AD) e conta Microsoft (MSA) no macOS.** Um usuário conectado no Microsoft Edge em macOS agora terá automaticamente acesso aos sites que estão configurados para permitir logon único com as contas Microsoft e Corporativas (por exemplo, bing.com, office.com, msn.com e outlook.com).

- **Modo de quiosque.** A partir do Microsoft Edge versão 90, bloqueamos as configurações de impressão da interface do usuário para permitir apenas as impressoras configuradas e as opções “Imprimir em PDF”. Também fizemos melhorias no modo quiosque de aplicativo único de acesso atribuído para restringir a inicialização de outros aplicativos a partir do navegador. Para obter mais informações sobre os recursos do modo quiosque, clique [aqui](/deployedge/microsoft-edge-configure-kiosk-mode#kiosk-mode-supported-features).

- **Interromper Downloads**: a partir do Microsoft Edge versão 91, o navegador interromperá automaticamente os downloads de tipos que podem danificar seu computador se esses downloads forem iniciados sem a interação do usuário e não forem suportados pela verificação de Reputação do Aplicativo SmartScreen. Os usuários podem substituir e continuar o download clicando com o botão direito e escolhendo “Manter” no item de download.
Os administradores de empresas podem optar por não adotar esse comportamento por uma destas duas políticas:
- [ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](/deployedge/microsoft-edge-policies#exemptdomainfiletypepairsfromfiletypedownloadwarnings): desabilita avisos baseados em extensão de tipo de arquivo de download para tipos de arquivo especificados em domínios. Para obter mais informações, confira [Interrupções de downloads da Segurança do Microsoft Edge](/deployedge/microsoft-edge-security-downloads-interruptions)

- **Impressão**:

    - **Novo modo de rasterização de impressão para impressoras não PostScript.** A partir da versão 90 do Microsoft Edge, os administradores poderão usar uma nova política para definir o modo de rasterização de impressão para seus usuários. Esta política  controla como o Microsoft Edge imprime para impressoras não PostScript no Windows. Às vezes, os trabalhos de impressão em impressoras não PostScript precisam ser rasterizados para serem impressos corretamente. As opções de impressão são Completa e Rápida.
    
  - **Opções adicionais de dimensionamento de página para impressão.** Os usuários agora podem personalizar o dimensionamento enquanto imprimem páginas da Web e documentos PDF usando as opções adicionais. A opção "Ajustar à página" garante que a página da Web ou o documento se ajuste ao espaço disponível no "Tamanho do papel" selecionado para impressão. A opção "Tamanho real" garante que não ocorram mudanças no tamanho do conteúdo que está sendo impresso, independentemente do "Tamanho do papel" selecionado.

-   **Produtividade:**

    -   **As sugestões de preenchimento automático são estendidas para incluir o conteúdo dos campos de endereço da área de transferência.** O conteúdo da área de transferência é analisado quando você clica em um campo de perfil/endereço (por exemplo, telefone, email, CEP, cidade, estado, etc.) para mostrar como sugestões de preenchimento automático.

    -   **Os usuários podem pesquisar sugestões de preenchimento automático mesmo se um formulário ou campo não for detectado.** Hoje, se você tiver suas informações salvas no Microsoft Edge, as sugestões de preenchimento automático aparecem automaticamente e ajudam você a economizar tempo enquanto preenche formulários. Nos casos em que o preenchimento automático falhar em um formulário ou se você quiser buscar dados em formulários que normalmente não têm preenchimento automático (como formulários temporários), você pode procurar suas informações usando o preenchimento automático.

-   **Acesse downloads a partir de um submenu na barra de menu.** Os downloads aparecerão no canto superior direito com todos os downloads ativos em um só lugar. Este menu é facilmente descartável para que os usuários possam continuar navegando ininterruptamente e possam monitorar o progresso geral do download diretamente da barra de ferramentas. [Saiba mais](https://techcommunity.microsoft.com/t5/articles/introducing-the-new-downloads-experience/m-p/2111551).

-   **Melhorias na renderização de fontes.** A partir da versão 90 do Microsoft Edge, fizemos melhorias na renderização do texto para melhorar a clareza e reduzir o desfocado. Parte das melhorias de renderização da fonte aparecerão na versão Beta 90, mas serão desativadas por padrão.

- **Modo Crianças.** Atualizamos a política para que, quando a política estiver habilitada, ela desabilite o recurso Modo Criança, além da proteção para a família. Saiba mais sobre o Modo Crianças aqui:[aqui](https://go.microsoft.com/fwlink/?linkid=2146910)

## <a name="policy-updates"></a>Atualizações de política

## <a name="new-policies"></a>Novas políticas

Oito novas políticas foram adicionadas. Baixe os Modelos Administrativos atualizados da [página de aterrissagem do Microsoft Edge Empresa](https://www.microsoft.com/edge/business/download). Foram adicionadas as novas políticas a seguir:
-   [ApplicationGuardFavoritesSyncEnabled](/DeployEdge/microsoft-edge-policies#applicationguardfavoritessyncenabled): habilitada a Sincronização de Favoritos do Application Guard
- [ApplicationGuardTrafficIdentificationEnabled](/DeployEdge/microsoft-edge-policies#applicationguardtrafficidentificationenabled): identificação de Tráfego do Application Guard
- [ExplicitlyAllowedNetworkPorts](/DeployEdge/microsoft-edge-policies#explicitlyallowednetworkports): portas de rede explicitamente permitidas
- [ImportStartupPageSettings](/DeployEdge/microsoft-edge-policies#importstartuppagesettings): permite a importação das configurações da página de inicialização
- [MathSolverEnabled](/DeployEdge/microsoft-edge-policies#mathsolverenabled): permite que os usuários capturem um problema de matemática e obtenham a solução com uma explicação passo a passo no Microsoft Edge
- [NewTabPageContentEnabled](/DeployEdge/microsoft-edge-policies#newtabpagecontentenabled): permite conteúdo do Microsoft News na página nova guia
- [NewTabPageQuickLinksEnabled](/DeployEdge/microsoft-edge-policies#newtabpagequicklinksenabled): permite links rápidos na página nova guia
-   [fetch UrlpaliveDurationSecondsOnShutdown](/DeployEdge/microsoft-edge-policies#fetchkeepalivedurationsecondsonshutdown): busca duração keepalive no desligamento
-   [ManagedConfigurationPerOrigin](/DeployEdge/microsoft-edge-policies#managedconfigurationperorigin): define valores de configuração gerenciada para sites de origens específicas
-   [PrintRasterizationMode](/DeployEdge/microsoft-edge-policies#printrasterizationmode) - Modo de Rasterização de Impressão
-   [QuickViewOfficeFilesEnabled](/DeployEdge/microsoft-edge-policies#quickviewofficefilesenabled) - Gerenciar a capacidade de Visualização Rápida de arquivos do Office no Microsoft Edge
-   [SSLErrorOverrideAllowedForOrigins](/DeployEdge/microsoft-edge-policies#sslerroroverrideallowedfororigins) - Permitir que os usuários prossigam a partir da página de aviso HTTPS para origens específicas
-   [WindowOcclusionEnabled](/DeployEdge/microsoft-edge-policies#windowocclusionenabled) - Habilitar Oclusão de Janela
-   [WindowsHelloForHTTPAuthEnabled](/DeployEdge/microsoft-edge-policies#windowshelloforhttpauthenabled) - Windows Hello habilitado para autenticação HTTP

## <a name="deprecated-policies"></a>Políticas preteridas

- [ProactiveAuthEnabled](/DeployEdge/microsoft-edge-policies#proactiveauthenabled): habilita a Autenticação Proativa
-   [NativeWindowOcclusionEnabled](/DeployEdge/microsoft-edge-policies#nativewindowocclusionenabled): habilita a Oclusão de Janela Nativa
-   [SSLVersionMin](/DeployEdge/microsoft-edge-policies#sslversionmin): versão mínima do TLS habilitada

## <a name="version-89077477-april-14"></a>Versão 89.0.774.77: 14 de abril

> [!Important]
>Essa atualização contém uma correção para [CVE-2021-21206](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-21206) e [CVE-2021-21220](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-21220) que foi relatada pela equipe do Chromium como tendo uma exploração em execução.  Para obter mais informações, confira o [Guia de Atualização de Segurança](https://msrc.microsoft.com/update-guide).

As atualizações de segurança do canal estável estão listadas [aqui](/deployedge/microsoft-edge-relnotes-security#april-14-2021).

## <a name="version-89077476-april-12"></a>Versão 89.0.774.76: 12 de abril

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-89077475-april-8"></a>Versão 89.0.774.75: 8 de abril

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-89077468-april-1"></a>Versão 89.0.774.68: 1º de abril

As atualizações de segurança do canal estável estão listadas [aqui](./microsoft-edge-relnotes-security.md#april-1-2021).

## <a name="version-89077463-march-25"></a>Versão 89.0.774.63: 25 de março

Vários bugs corrigidos e problemas de desempenho.

## <a name="version-89077457-march-18"></a>Versão 89.0.774.57: 18 de março

Correção de vários bugs e problemas de desempenho.

## <a name="version-89077454-march-13"></a>Versão 89.0.774.54: 13 de março

> [!IMPORTANT]
> Esta atualização contém [CVE-2021-21193](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-21193) que foi relatada pela equipe do Chromium como tendo uma exploração na natureza. Para obter mais informações, consulte o [Guia de atualização de segurança](https://msrc.microsoft.com/update-guide).

As atualizações de segurança do canal estável estão listadas [aqui](./microsoft-edge-relnotes-security.md#march-13-2021).

## <a name="version-89077450-march-10"></a>Versão 89.0.774.50: 10 de março

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-89077448-march-8"></a>Versão 89.0.774.48: 8 de março

Vários bugs e problemas de desempenho corrigidos.

<!-- begin major 89 -->

## <a name="version"></a>Versão

> [!IMPORTANT]
> Esta atualização contém o [CVE-2021-21166](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-21166) que foi reportado pela equipe da Chromium por ter uma vulnerabilidade em aberto. Para obter mais informações, confira o [Guia de Atualização de Segurança](https://msrc.microsoft.com/update-guide).

As atualizações de segurança do canal estável estão listadas [aqui](./microsoft-edge-relnotes-security.md#march-4-2021).

### <a name="resolved-issues"></a>Problemas resolvidos

- **Atualizações e correções de atalhos da barra de tarefas e do menu Iniciar:**
  - Clicar com o botão direito do mouse no atalho do Microsoft Edge no menu Iniciar agora mostrará corretamente a opção para desafixar o Microsoft Edge da barra de tarefas quando ele estiver fixado.
  - Layouts iniciais que incluem uma [configuração da barra de tarefas](/windows/configuration/configure-windows-10-taskbar) para fixar o Microsoft Edge na barra de tarefas não resultará mais em um segundo atalho do Microsoft Edge sendo fixado na barra de tarefas.
  - As organizações que utilizam Perfis de Roaming do Windows não verão mais um ícone branco vazio no lugar do ícone do Microsoft Edge na barra de tarefas quando seus usuários fizerem logon no Windows.

### <a name="feature-updates"></a>Atualizações de recursos

- **O modo quiosque permite recursos adicionais de bloqueio**. A partir da versão 89 do Microsoft Edge, adicionamos funcionalidades adicionais de bloqueio no modo de quiosque para permitir que os clientes executem as tarefas em uma experiência mais produtiva e segura. [Saiba mais](microsoft-edge-configure-kiosk-mode.md#kiosk-mode-supported-features).

- **A ferramenta Enterprise Mode Site List Manager estará disponível no navegador através da página do *edge://compat* **. Você pode usar esta ferramenta para criar, editar e exportar o XML da lista de sites para o modo Internet Explorer no Microsoft Edge. Você pode habilitar o acesso a esta ferramenta conforme necessário por meio da política de grupo. [Saiba Mais](./edge-ie-mode-site-list-manager.md).

- **Melhore o desempenho do navegador com guias de suspensão**. As guias em suspensão aprimoram o desempenho do navegador colocando as guias inativas em suspensão para liberar recursos do sistema, como memória e CPU, para que as guias ativas ou outros aplicativos possam usá-las. Os usuários podem impedir que os sites entrem em suspensão e configurem o período de tempo antes de uma Tabulação inativa entrar em suspensão. Para manter os usuários em seu fluxo, há também a [heurística](https://techcommunity.microsoft.com/t5/articles/sleeping-tabs-faq/m-p/1705434) para evitar que certos sites entre em modo de suspensão, como sites intranet. Esse recurso pode ser gerenciado com políticas de grupo.

- **Redefinir manualmente seus dados de sincronização do Microsoft Edge na nuvem**. Introduziremos uma maneira de redefinir os seus dados de sincronização do Microsoft Edge dentro do produto. Isso garante que os seus dados sejam removidos dos serviços Microsoft, além de resolver certos problemas do produto que exigiam um tíquete de suporte.

- **Habilitação inteligente de SSO (Logon único) para todas as contas do Windows Azure Active Directory (Azure AD) para usuários com um único perfil do Microsoft Edge que não é do Azure AD**.  Ative automaticamente essa configuração para os usuários que podem se beneficiar ao máximo desse recurso. Se um usuário tiver apenas um perfil do Microsoft Edge (e não for o Azure AD ou o Modo Infantil), a configuração será automaticamente acionada quando o Microsoft Edge for inicializado. Essa alternância automática também será desativada automaticamente se um usuário mais tarde optar por entrar em um perfil diferente do Microsoft Edge com uma conta do Azure AD. Os usuários podem atualizar manualmente suas preferências para esse recurso em **Configurações > Perfis > Preferências de perfil > Permitir um logon único para sites de trabalho ou de escola usando esse perfil**.

- **Melhorias na experiência de seleção de texto em documentos PDF**. Os usuários começarão a ter uma experiência de seleção de texto mais uniforme e consistente em documentos PDF abertos no Microsoft Edge a partir da versão 89.

- **O campo de data de nascimento agora é compatível com o preenchimento automático**. Hoje, o Microsoft Edge ajuda você a economizar tempo e esforço ao preencher formulários e criar contas online, preenchendo automaticamente seus dados como endereços, nomes, números de telefone, etc. A partir da versão 89 do Microsoft Edge, estamos adicionando suporte para outro campo que você pode ter salvar e preencher automaticamente: a data de nascimento. Você pode exibir, editar e excluir essas informações a qualquer momento nas configurações do seu perfil.

### <a name="policy-updates"></a>Atualizações de política

#### <a name="new-policies"></a>Novas políticas

Sete novas políticas foram adicionadas. Baixe os modelos administrativos atualizados da [página inicial do Microsoft Edge Enterprise](https://www.microsoft.com/edge/business/download). As novas políticas a seguir foram adicionadas.

- [BrowsingDataLifetime](./microsoft-edge-policies.md#browsingdatalifetime) - Configurações do Tempo de Vida de Dados de Navegação
- [MAMEnabled](./microsoft-edge-policies.md#mamenabled) - Gerenciamento de Aplicativos Móveis Habilitado
- [DefinePreferredLanguages](./microsoft-edge-policies.md#definepreferredlanguages) - Define uma lista ordenada de idiomas preferidos em que os sites devem ser exibidos se o site oferecer suporte
- [ShowRecommendationsEnabled](./microsoft-edge-policies.md#showrecommendationsenabled) - Permitir recomendações e notificações promocionais do Microsoft Edge
- [PrintingAllowedBackgroundGraphicsModes](./microsoft-edge-policies.md#printingallowedbackgroundgraphicsmodes) - Restringe o modo de impressão de elementos gráficos de plano de fundo
- [PrintingBackgroundGraphicsDefault](./microsoft-edge-policies.md#printingbackgroundgraphicsdefault) - Modo padrão de impressão de gráficos em segundo plano
- [SmartActionsBlockList](./microsoft-edge-policies.md#smartactionsblocklist) - Bloqueie ações inteligentes  para uma lista de serviços

#### <a name="obsoleted-policies"></a>Políticas obsoletas

As políticas a seguir estão obsoletas.

- [ForceLegacyDefaultReferrerPolicy](./microsoft-edge-policies.md#forcelegacydefaultreferrerpolicy) - Usa uma política referencial padrão de no-referrer-when-downgrade
- [MetricsReportingEnabled](./microsoft-edge-policies.md#metricsreportingenabled) - Habilita o uso e os relatórios de dados relacionados a falhas
- [SendSiteInfoToImproveServices](./microsoft-edge-policies.md#sendsiteinfotoimproveservices) - Envie as informações do site para melhorar os serviços da Microsoft

<!-- end major 89 -->

## <a name="version-88070581-february-25"></a>Versão 88.0.705.81: 25 de fevereiro

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-88070574-february-17"></a>Versão 88.0.705.74: 17 de fevereiro

As atualizações de segurança do canal estável estão listadas [aqui](./microsoft-edge-relnotes-security.md#february-17-2021).

## <a name="version-88070568-february-11"></a>Versão 88.0.705.68: 11 de fevereiro

Correção de vários bugs e problemas de desempenho.

## <a name="version-88070563-february-5"></a>Versão 88.0.705.63: 5 de Fevereiro

> [!IMPORTANT]
> Esta atualização contém o [CVE-2021-21148](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-21148) que foi reportado pela equipe da Chromium por ter uma vulnerabilidade em aberto.

As atualizações de segurança do canal estável estão listadas [aqui](./microsoft-edge-relnotes-security.md#february-5-2021).

## <a name="version-88070562-february-4"></a>Versão 88.0.705.62: 4 de Fevereiro

As atualizações de segurança do canal estável estão listadas [aqui](./microsoft-edge-relnotes-security.md#february-4-2021).

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-88070556-january-28"></a>Versão 88.0.705.56: 28 de Janeiro

Correção de vários bugs e problemas de desempenho.

## <a name="version-88070553-january-26"></a>Versão 88.0.705.53: 26 de janeiro

Correção de vários bugs e problemas de desempenho.

## <a name="version-88070550-january-21"></a>Versão 88.0.705.50: 21 de janeiro

As atualizações de segurança do canal estável estão listadas [aqui](./microsoft-edge-relnotes-security.md#january-21-2021).

<!--- begin major 88  --->
### <a name="feature-updates"></a>Atualizações de recursos

- **Preteridos:**

  - Preterir o suporte para o protocolo FTP. O suporte para o protocolo de FTP herdado foi removido do Microsoft Edge. Tentar navegar para um link de FTP fará com que o navegador direcione o sistema operacional para abrir um aplicativo externo para manipular o link de FTP. Como alternativa, os administradores de TI podem configurar o Microsoft Edge para usar o modo IE para sites que dependem do protocolo FTP.
  - O suporte ao Adobe Flash será removido. A partir do Microsoft Edge beta versão 88, a funcionalidade e o suporte do Adobe Flash serão removidos. Saiba mais: [Atualização no fim do suporte do Adobe Flash Player - blog do Microsoft Edge (Windows.com)](https://blogs.windows.com/msedgedev/2020/09/04/update-adobe-flash-end-support/)

- **Autenticação:**

  - O SSO (SSO) já está disponível para contas do Azure Active Directory (Azure AD) e conta da Microsoft (MSA) no Windows de nível inferior. Um usuário conectado no Microsoft Edge no nível inferior do Microsoft Windows (7, 8.1) agora será automaticamente conectado aos sites que estiverem configurados para permitir logon único com contas Work e Microsoft (por exemplo, bing.com, office.com, msn.com, outlook.com).<br>Observação: um usuário pode ter que sair e entrar novamente se ele se conectar ao Microsoft Edge em uma versão anterior ao Microsoft Edge 88 para aproveitar esse recurso.
  
  - Logon Único (SSO) para sites de trabalho usando qualquer conta do Windows Azure Active Directory (Azure AD) no sistema de perfis que não são do Azure AD do Microsoft Edge. Este recurso pode ser habilitado para qualquer perfil que não esteja conectado com uma conta corporativa/de estudante, não seja convidado ou privado e permita o uso de qualquer conta corporativa/de estudante no sistema operacional com esse perfil. Esse recurso pode ser configurado em **Configurações** > **Perfis** > **Preferências de Perfil** > **Permitir logon único para sites de trabalho ou escola usando esse perfil**.
  
    > [!NOTE]
    > "Logon único (SSO) para todas as contas do Windows usando o perfil do Microsoft Edge" é uma atualização das notas de versão de 21 de janeiro.

- **Opção de modo de quiosque para encerrar a sessão**. O botão "Encerrar sessão" agora está disponível em uma experiência de navegação pública do modo de quiosque. Esse recurso garante que os dados e as configurações do navegador sejam excluídos quando o Microsoft Edge estiver fechado. Saiba mais sobre os recursos do modo de quiosque e o roteiro, [Configurar o modo de quiosque do Microsoft Edge](./microsoft-edge-configure-kiosk-mode.md).

- **Segurança e privacidade:**

  - Alertas são gerados se a senha de um usuário for encontrada em um vazamento online. As senhas do usuário são verificadas em um repositório de credenciais violadas e envia ao usuário um alerta se uma correspondência for encontrada. Para garantir a segurança e a privacidade, as senhas dos usuários são criptografadas e criptografadas quando são verificadas no banco de dados de credenciais vazadas.
  - Atualizar conteúdo misto automaticamente. As páginas seguras fornecidas por HTTPS podem conter imagens de referência que são servidas por HTTP não seguro. Para melhorar a privacidade e a segurança no Microsoft Edge 88, essas imagens serão recuperadas por HTTPS. Se a imagem não estiver disponível em HTTPS, ela não será carregada.
  - Exiba as permissões do site por site e por atividades recentes. Começando com o Microsoft Edge 88, os usuários poderão gerenciar permissões do site com mais facilidade. Elas poderão exibir permissões por site da Web, em vez do tipo de permissão apenas. Além disso, adicionamos uma seção de atividade recente que mostrará a um usuário todas as alterações recentes nas permissões do site.
  - Controles avançados para os cookies do navegador. A partir do Microsoft Edge 88, os usuários podem excluir cookies de terceiros sem afetar os cookies dos primeiros participantes. Os usuários também poderão filtrar os cookies por nome ou terceiro e classificar por nome, número de cookies e a quantidade de dados armazenados e modificados pela última vez.

- **Senhas:**

  - Gerador de senhas. O Microsoft Edge oferece um gerador de senhas fortes integrado que você pode usar ao se inscrever em uma nova conta ou ao alterar uma senha existente. Basta procurar a lista suspensa de senha sugerida pelo navegador no campo de senha e, quando selecionada, ela será salva automaticamente no navegador e será sincronizada entre os dispositivos para facilitar o uso futuro.
  - Monitor de Senhas. Quando qualquer uma das suas senhas salvas no navegador corresponder às que foram vistas na lista de credenciais vazadas, o Microsoft Edge o notificará e solicitará que atualize sua senha. O Monitor de Senhas verifica se há combinações em seu nome e está ativado por padrão.
  - Editar Senha. Agora você pode editar suas senhas salvas diretamente nas Configurações do Microsoft Edge. Sempre que uma senha for atualizada fora do Microsoft Edge, é fácil substituir a senha antiga salva pela nova editando a entrada salva em Configurações. 

- **Melhore a velocidade de inicialização do Microsoft Edge com o início rápido**. Para melhorar a velocidade de inicialização do Microsoft Edge, desenvolvemos um recurso chamado início rápido. O início rápido abre o Microsoft Edge mais rapidamente, permitindo que o Microsoft Edge seja executado em segundo plano. Observação: esse recurso está limitado a um grupo de usuários selecionado aleatoriamente que habilitou o experimento. Esses usuários estão fazendo comentários para a equipe de recursos.

- **Produtividade:**

  - Melhorar a produtividade e várias tarefas com guias verticais. À medida que o número de guias horizontais aumenta, os títulos de sites começam a ser cortados e os controles de guia são perdidos quando cada guia é reduzida. Isso interrompe o fluxo de trabalho do usuário à medida que passa mais tempo encontrando, trocando e gerenciando suas guias e menos tempo na tarefa em questão. As guias verticais permitem que os usuários movam suas guias para a lateral, onde ícones alinhados verticalmente e títulos de sites mais longos facilitam verificação, identificação e alternância rápidas para a guia que elas desejam abrir.
  - Preenchimento automático do campo data do nascimento. O Microsoft Edge já ajuda a poupar tempo e esforço ao preencher formulários e criar contas online por meio do preenchimento automático de dados do usuário, como endereços, nomes, números de telefone, etc. O Microsoft Edge agora oferece suporte ao campo data de nascimento que os usuários podem salvar e preencher automaticamente. Um usuário pode exibir, editar e excluir essas informações a qualquer momento em suas configurações de perfil.
  - Melhorias em Fechadas recentemente no Histórico. Fechadas recentemente agora mantém as últimas 25 guias e janelas em qualquer sessão de navegação anterior, em vez de apenas na sessão anterior. Os usuários podem selecionar Fechadas recentemente na nova experiência do Histórico para ver todas as guias que estavam abertas.
  - Recurso “Seu dia resumido” habilitado por padrão. A partir do Microsoft Edge versão 88, os profissionais da informação podem se beneficiar dos recursos de produtividade inteligentes em sua página Nova guia (NTP). Os usuários do Microsoft Edge 87 também experimentarão esses recursos 2 semanas após o lançamento do Microsoft Edge 88. Oferecemos aos usuários conectados com sua conta de estudante ou corporativa conteúdo personalizado e relevante desenvolvido por seu gráfico M365. Os usuários podem examinar rapidamente seus módulos “Seu dia num relance” para rastrear facilmente suas reuniões e trabalhos recentes, bem como iniciar rapidamente os aplicativos que desejam usar.

- **Sincronização de histórico e guias abertas.** A sincronização de histórico e guias abertas agora está disponível para os usuários aproveitarem. A habilitação desses recursos ajudará os usuários a continuar de onde deixaram, tornando seu histórico de navegação e guias abertas disponíveis em todos os seus dispositivos de sincronização. Atualizamos as políticas de histórico do navegador e sincronização, portanto, agora os usuários estão conectados e produtivos em todos os dispositivos usando o Microsoft Edge. [Saiba mais](https://blogs.windows.com/windowsexperience/2021/01/21/this-year-lets-resolve-to-make-the-most-of-our-time-online-and-better-protect-ourselves-from-online-threats/).

- **PDF:**

  - Exibição de documento em PDF no modo de exibição de livro (duas páginas). A partir da versão 88 do Microsoft Edge, os usuários podem exibir documentos em PDF em uma única página ou no modo de exibição de duas páginas. Para alterar o modo de exibição, clique no botão **Modo de exibição de página** na barra de ferramentas.
  - Suporte a notas de texto ancoradas para arquivos PDF. A partir da versão 87 do Microsoft Edge, os usuários podem adicionar anotações de texto digitadas em qualquer parte do texto em arquivos PDF.

- **Fontes:**

  - Os ícones do navegador são atualizados para o sistema de design Fluent. Como parte do nosso trabalho contínuo em relação ao design Fluent no navegador, fizemos alterações para alinhar os ícones ao novo sistema de ícones da Microsoft. Essas mudanças afetarão muitas das nossas interfaces de usuário de alto toque, incluindo guias, barra de endereços, bem como ícones de navegação e ícones de orientação encontrados em nossos vários menus.
  - Renderização de fonte aprimorada. A renderização de texto é melhorada para melhorar a clareza e reduzir o desfoque.

### <a name="policy-updates"></a>Atualizações de política

#### <a name="new-policies"></a>Novas políticas

Foram adicionadas dezoito novas políticas. Baixe os modelos administrativos atualizados da [página inicial do Microsoft Edge Enterprise](https://www.microsoft.com/edge/business/download). As novas políticas a seguir foram adicionadas.

- [BasicAuthOverHttpEnabled](./microsoft-edge-policies.md#basicauthoverhttpenabled) - permitir autenticação básica para HTTP.
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
- [TargetBlankImpliesNoOpener](./microsoft-edge-policies.md#targetblankimpliesnoopener) - não defina window.opener para links targeting _blank.
- [UpdatePolicyOverride](./microsoft-edge-policies.md#updatepolicyoverride) - especifica como o Microsoft Edge Update manipula as atualizações disponíveis do Microsoft Edge.
- [VerticalTabsAllowed](./microsoft-edge-policies.md#verticaltabsallowed) - configura a disponibilidade de um layout vertical para guias na lateral do navegador.
- [WebRtcAllowLegacyTLSProtocols](./microsoft-edge-policies.md#webrtcallowlegacytlsprotocols) - permite downgrade de TLS/DTLS herdado no WebRTC.
- [WebWidgetAllowed](./microsoft-edge-policies.md#webwidgetallowed) - habilita o widget Web.
- [WebWidgetIsEnabledOnStartup](./microsoft-edge-policies.md#webwidgetisenabledonstartup) - permite o widget da Web na inicialização do Windows.

#### <a name="deprecated-policies"></a>Políticas preteridas

- [ProactiveAuthEnabled](./microsoft-edge-policies.md#proactiveauthenabled) - habilita a autenticação pró-ativa.
- [ProxyBypassList](./microsoft-edge-policies.md#proxybypasslist) - configura regras de bypass de proxy.
- [Proxymode](./microsoft-edge-policies.md#proxymode) - define configurações de servidor proxy.
- [ProxyPacUrl](./microsoft-edge-policies.md#proxypacurl) - define a URL do arquivo proxy.pac.
- [ProxyServer](./microsoft-edge-policies.md#proxyserver) - configura o endereço ou URL do servidor proxy.
- [WebDriverOverridesIncompatiblePolicies](./microsoft-edge-policies.md#webdriveroverridesincompatiblepolicies) - permite que o WebDriver substitua políticas incompatíveis.

### <a name="obsoleted-policies"></a>Políticas Obsoletas

- [AllowPopupsDuringPageUnload](./microsoft-edge-policies.md#allowpopupsduringpageunload) - permite que uma página mostre pop-ups durante seu descarregamento.
- [DefaultPluginsSetting](./microsoft-edge-policies.md#defaultpluginssetting) - configuração padrão do Adobe Flash.
- [PluginsAllowedForUrls](./microsoft-edge-policies.md#pluginsallowedforurls) - permite o plug-in do Adobe Flash em sites específicos.
- [PluginsBlockedForUrls](./microsoft-edge-policies.md#pluginsblockedforurls) - bloqueia o plug-in do Adobe Flash em sites específicos.
- [RunAllFlashInAllowMode](./microsoft-edge-policies.md#runallflashinallowmode) - estende a configuração do Adobe Flash Content para todo o conteúdo.
<!--- end major 88  --->
## <a name="version-87066475-january-7"></a>Versão 87.0.664.75: 7 de janeiro

As atualizações de segurança do canal estável estão listadas [aqui](./microsoft-edge-relnotes-security.md#january-7-2021).

## <a name="version-87066466-december-17"></a>Versão 87.0.664.66: 17 de dezembro

Correção de vários bugs e problemas de desempenho.

## <a name="version-87066460-december-10"></a>Versão 87.0.664.60: 10 de dezembro

Correção de vários bugs e problemas de desempenho.

## <a name="version-87066457-december-7"></a>Versão 87.0.664.57: 7 de dezembro

Vários bugs e problemas de desempenho corrigidos. As atualizações de segurança do canal estável estão listadas [aqui](./microsoft-edge-relnotes-security.md#december-7-2020).

## <a name="version-87066455-december-3"></a>Versão 87.0.664.55: 3 de dezembro

Correção de vários bugs e problemas de desempenho. O seguinte recurso foi atualizado para este lançamento.

- **O Shopping está habilitado por padrão**. A partir da versão 87 do Microsoft Edge, os usuários corporativos podem se beneficiar das compras no Microsoft Edge. Com os recursos de compra, o Microsoft Edge ajuda os usuários a encontrar cupons e melhores preços ao fazer compras online. (A experiência de cupom foi lançada com a versão estável 87.0.664.41). A experiência de comparação de preços agora está disponível nesta atualização. Este recurso pode ser configurado usando a política [EdgeShoppingAssistantEnabled](./microsoft-edge-policies.md#edgeshoppingassistantenabled). Veja nosso [Blog](https://blogs.windows.com/windowsexperience/2020/11/19/finish-up-that-holiday-shopping-with-new-features-from-microsoft-edge-and-bing/) e [Saiba mais](/microsoft-edge/privacy-whitepaper#shopping) sobre o Microsoft Shopping.

## <a name="version-87066452-november-30"></a>Versão 87.0.664.52: 30 de novembro

Correção de vários bugs e problemas de desempenho.

## <a name="version-87066447-november-23"></a>Versão 87.0.664.47: 23 de novembro

Correção de vários bugs e problemas de desempenho.

<!-- begin major 87 --->
## <a name="version-87066441-november-19"></a>Versão 87.0.664.41: 19 de novembro

As atualizações de segurança do canal estável estão listadas [aqui](./microsoft-edge-relnotes-security.md#november-19-2020).

### <a name="feature-updates"></a>Atualizações de recursos

- **Redirecionamento automático de sites incompatíveis do Internet Explorer para o Microsoft Edge**. A partir da atualização estável do Microsoft Edge 87, os sites públicos que mostram uma mensagem de incompatibilidade no Internet Explorer serão automaticamente redirecionados para o Microsoft Edge. Para saber mais e configurar essa experiência, confira [Redirecionamento de sites incompatíveis](./edge-learnmore-neededge.md).

- **Recursos de privacidade do modo de quiosque habilitados**. Começando com o Microsoft Edge versão 87, os recursos do modo de quiosque que ajudarão empresas em relação à privacidade dos dados do usuário serão habilitados. Esses recursos habilitarão experiências, como limpar os dados do usuário ao sair, excluir arquivos baixados e redefinir a experiência de iniciação configurada após uma quantidade específica de tempo ocioso. Saiba mais sobre como [Configurar as opções do modo de quiosque do Microsoft Edge](./microsoft-edge-configure-kiosk-mode.md)

- **Recursos de compra habilitados por padrão**. A partir da versão 87 do Microsoft Edge, os usuários corporativos do Microsoft Edge também podem tirar proveito da compra no Edge. Com os recursos de compra, o Microsoft Edge ajuda os usuários a encontrar cupons e melhores preços ao fazer compras online. A experiência de cupom está disponível com esta atualização e a comparação de preços será lançada em futuras atualizações do Microsoft Edge 87. Esse recurso pode ser configurado por meio da política [EdgeShoppingAssistantEnabled](./microsoft-edge-policies.md#edgeshoppingassistantenabled) . Veja o nosso [blog](https://blogs.windows.com/windowsexperience/2020/11/19/finish-up-that-holiday-shopping-with-new-features-from-microsoft-edge-and-bing/) e [saiba mais](/microsoft-edge/privacy-whitepaper#shopping) sobre o Microsoft shopping.

- **Implantação de ClickOnce habilitada por padrão**. O ClickOnce está habilitado por padrão no Microsoft Edge 87, o que reduz as barreiras para a implantação de software e alinha-se melhor com o comportamento do navegador da Versão Prévia do Microsoft Edge. A partir do Microsoft Edge 87, o estado "Não Configurado" da política de ClickOnceEnabled refletirá o novo estado de ClickOnce padrão Habilitado (em comparação com o estado padrão anterior Desabilitado).

- **A página nova guia da empresa (NTP) integra a produtividade com o conteúdo do feed personalizado e relevante para o trabalho**. O NTP empresarial combina a página de produtividade do Office 365 oferecemos a todos os usuários que entraram com uma conta corporativa ou de estudante com feeds personalizados da empresa e da indústria relevantes para o trabalho que são organizados em uma única página. Os usuários poderão reconhecer o conteúdo familiar do Office 365 e da Pesquisa da Microsoft para Empresas, da plataforma Bing. Além disso, eles podem personalizar facilmente "Meu feed" escolhendo o conteúdo mais relevante para eles do conteúdo e módulos disponíveis para sua organização. Os administradores de TI podem controlar as configurações de feed de notícias para sua organização, incluindo o setor selecionado para a nova página de guia do Edge, acessando o Centro de Administração do Microsoft 365. [Saiba mais](https://blogs.windows.com/msedgedev/2020/10/29/enterprise-new-tab-page-my-feed/)

- **Segurança e privacidade:**

  - Suporte a Associação de Token TLS para sites de política configurada. A associação de Token TLS ajuda a evitar ataques de roubo de token para garantir que os cookies não possam ser reutilizados a partir de um dispositivo que não tenha sido definido inicialmente. O uso da ligação de token TLS exige a configuração da política [AllowTokenBindingForUrls](./microsoft-edge-policies.md#allowtokenbindingforurls) e exige que os sites listados ofereçam suporte a esse recurso.

- **Suporte a teclado para marca-texto em arquivos PDF**. Os usuários podem usar as teclas do teclado para realçar qualquer texto em um PDF.

- **Impressão:**

  - Escolha o lado a ser invertido ao imprimir nos dois lados. Os usuários podem optar por virar o lado maior ou o lado menor de uma planilha ao imprimir em ambos os lados.
  - Escolha o modo de rasterização de impressão para a empresa. Controlar como o Microsoft Edge é impresso em uma impressora não PostScript no Windows. Às vezes, os trabalhos de impressão em impressoras não PostScript precisam ser rasterizados para serem impressos corretamente. As opções de impressão são "Total" e "Rápida".

### <a name="policy-updates"></a>Atualizações de política

#### <a name="new-policies"></a>Novas políticas

Dez novas políticas foram adicionadas. Baixe os modelos administrativos atualizados da [página inicial do Microsoft Edge Enterprise](https://www.microsoft.com/edge/business/download). As novas políticas a seguir foram adicionadas.

- [ConfigureFriendlyURLFormat](./microsoft-edge-policies.md#configurefriendlyurlformat) - configure o formato de colagem padrão das URLs copiadas do Microsoft Edge e determine se formatos adicionais estarão disponíveis para os usuários.
- [EdgeShoppingAssistantEnabled](./microsoft-edge-policies.md#edgeshoppingassistantenabled) - compras no Microsoft Edge habilitadas.
- [HideInternetExplorerRedirectUXForIncompatibleSitesEnabled](./microsoft-edge-policies.md#hideinternetexplorerredirectuxforincompatiblesitesenabled) – oculte o diálogo de redirecionamento único e a faixa no Microsoft Edge.
- [KioskAddressBarEditingEnabled](./microsoft-edge-policies.md#kioskaddressbareditingenabled) -configure a edição da barra de endereços para a experiência de navegação pública do modo de quiosque.
- [KioskDeleteDownloadsOnExit](./microsoft-edge-policies.md#kioskdeletedownloadsonexit) - exclua arquivos baixados como parte de uma sessão modo de quiosque quando o Microsoft Edge for fechado.
- [PasswordRevealEnabled](./microsoft-edge-policies.md#passwordrevealenabled) - habilitar botão de revelação de senha.
- [RedirectSitesFromInternetExplorerPreventBHOInstall](./microsoft-edge-policies.md#redirectsitesfrominternetexplorerpreventbhoinstall) – impedir a instalação do objeto auxiliar de navegador (BHO) para redirecionar sites incompatíveis do Internet Explorer para o Microsoft Edge.
- [RedirectSitesFromInternetExplorerRedirectMode](./microsoft-edge-policies.md#redirectsitesfrominternetexplorerredirectmode) – redirecione sites incompatíveis do Internet Explorer para o Microsoft Edge.
- [SpeechRecognitionEnabled](./microsoft-edge-policies.md#speechrecognitionenabled) - configurar Reconhecimento de Fala.
- [WebCaptureEnabled](./microsoft-edge-policies.md#webcaptureenabled) - habilitar o recurso de captura da Web no Microsoft Edge.

#### <a name="deprecated-policy"></a>Política Preterida

[NewTabPageSetFeedType](./microsoft-edge-policies.md#newtabpagesetfeedtype) - configurar a nova experiência de página da guia Microsoft Edge.

#### <a name="obsoleted-policy"></a>Política obsoleta

[EnableDeprecatedWebPlatformFeatures](./microsoft-edge-policies.md#enabledeprecatedwebplatformfeatures) - reative os recursos da plataforma Web preteridos por um tempo limitado.

<!-- end major 87 -->

## <a name="version-86062269-november-13"></a>Versão 86.0.622.69: 13 de novembro

> [!IMPORTANT]
> Esta atualização contém o [CVE-2020-16013](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-16013) e o [CVE-2020-16017](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-16017), que foi reportado pela equipe da Chromium por ter uma vulnerabilidade em aberto.

As atualizações de segurança do canal estável estão listadas [aqui](./microsoft-edge-relnotes-security.md#november-13-2020).

## <a name="version-86062268-november-11"></a>Versão 86.0.622.68: 11 de novembro

As atualizações de segurança do canal estável estão listadas [aqui](./microsoft-edge-relnotes-security.md#november-11-2020)

## <a name="version-86062263-november-4"></a>Versão 86.0.622.63: 4 de novembro

> [!IMPORTANT]
> Esta atualização contém o [CVE-2020-16009](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-16009), que foi reportado pela equipe da Chromium por ter uma vulnerabilidade em aberto.

As atualizações de segurança do canal estável estão listadas [aqui](./microsoft-edge-relnotes-security.md#november-4-2020).

## <a name="version-86062261-november-2"></a>Versão 86.0.622.61: 2 de novembro

Correção de vários bugs e problemas de desempenho.

## <a name="version-86062258-october-29"></a>Versão 86.0.622.58: 29 de outubro

Correção de vários bugs e problemas de desempenho.

## <a name="version-86062256-october-27"></a>Versão 86.0.622.56: 27 de outubro

Correção de vários bugs e problemas de desempenho.

## <a name="version-86062251-october-22"></a>Versão 86.0.622.51 : 22 de outubro

As atualizações de segurança do canal estável estão listadas [aqui](./microsoft-edge-relnotes-security.md#october-22-2020)

## <a name="version-86062248-october-20"></a>Versão 86.0.622.48: 20 de outubro

Correção de vários bugs e problemas de desempenho.

## <a name="version-86062243-october-15"></a>Versão 86.0.622.43: 15 de outubro

Correção de vários bugs e problemas de desempenho.

## <a name="version-86062238-october-9"></a>Versão 86.0.622.38: 9 de outubro

As atualizações de segurança estão listadas [aqui](./microsoft-edge-relnotes-security.md#october-9-2020)

### <a name="feature-updates"></a>Atualizações de recursos

* **Reverter para a versão anterior do Microsoft Edge.** O recurso reversão permite que os administradores voltem para uma versão boa conhecida do Microsoft Edge, caso haja algum problema na versão mais recente do Microsoft Edge. **Observação:** A versão estável 86.0.622.38 é a primeira versão para a qual você pode reverter, o que significa que a versão estável 87 é a primeira versão pronta para ser revertida. [Saiba mais](edge-learnmore-rollback.md).

* **Forçar a habilitação da Sincronização por padrão em toda a empresa.**  Os administradores podem habilitar a sincronização das contas do Azure Active Directory (Azure AD) por padrão com a política de [ForceSync](./microsoft-edge-policies.md#forcesync).

* **Mudança de perfil automática no Windows 7 e 8.1.** A mudança de perfil automática disponível atualmente no Microsoft Edge no Windows 10 foi estendida para versões inferiores do Windows (Windows 7 e 8.1). Para saber mais, confira a postagem de blog [mudança de perfil automática](https://blogs.windows.com/msedgedev/2020/04/30/automatic-profile-switching/).

* **SameSite=Lax Cookies por padrão**. Para melhorar a segurança e a privacidade da web, os cookies agora serão padronizados para manipulação como [SameSite=Lax](https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie/SameSite). Isso significa que os cookies só serão enviados em um contexto de first-party e serão omitidos para as solicitações enviadas a terceiros. Essa alteração pode causar impacto de compatibilidade em sites que exigem cookies para recursos de terceiros funcionarem corretamente. Para permitir tais cookies, os desenvolvedores da Web podem marcar cookies que devem ser configurados e enviados a contextos de terceiros, adicionando `SameSite=none` explícitos e atributos `Secure` quando o cookie é definido. As empresas que desejam isentar determinados sites da alteração podem fazer isso usando a política [LegacySameSiteCookieBehaviorEnabledForDomainList](./microsoft-edge-policies.md#legacysamesitecookiebehaviorenabledfordomainlist) ou podem recusar a alteração em todos os sites que usam a política [LegacySameSiteCookieBehaviorEnabled](./microsoft-edge-policies.md#legacysamesitecookiebehaviorenabled).

* **Remover a API de cache de aplicativo HTML5.**  A partir da versão 86 do Microsoft Edge, a API de cache de aplicativo herdado que permite o uso offline de páginas da Web será removida do Microsoft Edge. Os desenvolvedores da Web devem examinar a [documentação WebDev](https://web.dev/appcache-removal/) para saber mais sobre como substituir a API de cache de aplicativo com Profissionais de Serviço.  Importante: você pode solicitar um [Token OriginTrial do AppCache](https://developers.chrome.com/origintrials/#/view_trial/1776670052997660673) que permite que os sites continuem usando a versão preterida da API de cache de aplicativo até a versão 90 do Microsoft Edge.

* **Segurança e privacidade:**

  * Substituir as políticas [MetricsReportingEnabled](/DeployEdge/microsoft-edge-policies#metricsreportingenabled) e [SendSiteInformationToImproveServices](/DeployEdge/microsoft-edge-policies#sendsiteinfotoimproveservices) para versões inferiores do Windows e macOS. Essas políticas foram preteridas na versão 86 do Microsoft Edge e se tornarão preteridas na versão 89 do Microsoft Edge.<br>
Essas políticas são substituídas por [Permitir Telemetria](/windows/privacy/configure-windows-diagnostic-data-in-your-organization) no Windows 10 e a nova política [DiagnosticData](./microsoft-edge-policies.md#diagnosticdata) para todas as outras políticas. Isso permitirá que os usuários gerenciem os dados de diagnóstico enviados para a Microsoft do Windows 7, 8, 8.1 e macOS.
  * Suporte ao DNS seguro (DNS em HTTPS).  A partir da versão 86 do Microsoft Edge, as configurações para controlar o DNS seguro em dispositivos não gerenciados estarão disponíveis. Essas configurações não podem ser acessadas por usuários em dispositivos gerenciados, mas os administradores de TI podem habilitar ou desabilitar o DNS seguro usando a política de grupo [dnsoverhttpsmode](./microsoft-edge-policies.md#dnsoverhttpsmode).

* **Modo de Internet Explorer:** Permita que os usuários usem a interface do usuário (UI) do Microsoft Edge para testar sites no modo Internet Explorer. A partir da versão 86 do Microsoft Edge, os administradores poderão habilitar uma opção da interface do usuário para seus usuários para carregar uma guia no modo Internet Explorer para fins de teste ou como um stopgap até que os sites sejam adicionados ao XML da lista de sites.

* **Atualizações de PDF:**

  * Sumário para documentos em PDF. A partir da versão 86, o Microsoft Edge terá suporte ao sumário, o que permitirá que os usuários naveguem com facilidade por um documento em PDF.
  * Acesse todas as funcionalidades de PDF em telas pequenas de fator forma. Acesse todos os recursos do leitor de PDF do Microsoft Edge em dispositivos com telas pequenas.
  * Suporte à caneta digital para marca-texto em arquivos PDF. Com essa atualização, os usuários podem usar a caneta digital para realçar o texto diretamente em arquivos PDF, da mesma forma que uma marca-texto física realçaria o papel.
  * Rolagem aperfeiçoada de PDF. Agora, você poderá experimentar a rolagem livre de travamentos ao navegar por documentos em PDF grandes.

* **Os usuários verão sugestões de preenchimento automático quando começarem a digitar uma consulta de pesquisa no site de Complementos do Microsoft Edge.** O preenchimento automático ajuda os usuários a concluir a consulta de pesquisa sem ter que digitar a cadeia de caracteres inteira. Isso será útil porque os usuários não precisarão se lembrar das ortografias corretas e poderão escolher uma das opções disponíveis.

* **Adicione uma imagem personalizada à página Nova guia (NTP) usando uma política de grupo.** A partir da versão 86 do Microsoft Edge, a NTP tem a opção de substituir a imagem padrão por uma imagem personalizada fornecida pelo usuário. A habilidade de gerenciar as propriedades desta imagem também é compatível com a política de grupo.

* **Combinar os atalhos de teclado personalizados com o VS Code.** O DevTools do Microsoft Edge agora é compatível com a personalização de atalhos de teclado no DevTools para corresponder ao editor/IDE. (No Microsoft Edge 84, adicionamos a capacidade de combinar os atalhos de teclado do DevTools com o VS Code).

* **Excluir downloads do disco usando o gerenciador de downloads.** Agora, os usuários podem excluir os arquivos baixados de seu disco, sem sair do navegador. A nova funcionalidade Excluir downloads existe no menu de contexto da prateleira de downloads ou da página de downloads.

### <a name="policy-updates"></a>Atualizações de política

#### <a name="new-policies"></a>Novas políticas

Vinte e três novas políticas foram adicionadas. Baixe os modelos administrativos atualizados da [página inicial do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise). As novas políticas a seguir foram adicionadas.

- [CollectionsServicesAndExportsBlockList](./microsoft-edge-policies.md#collectionsservicesandexportsblocklist) - Bloquear o acesso a uma lista especificada de serviços e exportar destinos em Coleções.
- [DefaultFileSystemReadGuardSetting](./microsoft-edge-policies.md#defaultfilesystemreadguardsetting) - Controlar o uso da API do sistema de arquivos para leitura.
- [DefaultFileSystemWriteGuardSetting](./microsoft-edge-policies.md#defaultfilesystemwriteguardsetting) - Controlar o uso da API do sistema de arquivos para gravação.
- [DefaultSensorsSetting](./microsoft-edge-policies.md#defaultsensorssetting) - configuração de sensores padrão.
- [DefaultSerialGuardSetting](./microsoft-edge-policies.md#defaultserialguardsetting) - Controlar o uso da API serial.
- [DiagnosticData](./microsoft-edge-policies.md#diagnosticdata) - Enviar dados de diagnóstico obrigatórios e opcionais referentes ao uso do navegador.
- [EnterpriseModeSiteListManagerAllowed](./microsoft-edge-policies.md#enterprisemodesitelistmanagerallowed) - Permitir o acesso à ferramenta Enterprise Mode Site List Manager.
- [FileSystemReadAskForUrls](./microsoft-edge-policies.md#filesystemreadaskforurls) - Permitir o acesso de leitura pela API do Sistema de arquivos nesses sites.
- [FileSystemReadBlockedForUrls](./microsoft-edge-policies.md#filesystemreadblockedforurls) - Permitir o acesso de leitura pela API do Sistema de arquivos nesses sites.
- [FileSystemWriteAskForUrls](./microsoft-edge-policies.md#filesystemwriteaskforurls) - Permitir o acesso de gravação a arquivos e diretórios nestes sites.
- [FileSystemWriteBlockedForUrls](./microsoft-edge-policies.md#filesystemwriteblockedforurls) - Bloquear o acesso de gravação a arquivos e diretórios nestes sites.
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
- [UserAgentClientHintsEnabled](./microsoft-edge-policies.md#useragentclienthintsenabled) - Habilitar o recurso de Dicas do Cliente Usuário-Agente.
- [UserDataSnapshotRetentionLimit](./microsoft-edge-policies.md#userdatasnapshotretentionlimit) - Limita o número de instantâneos de dados do usuário mantidos para uso no caso de uma reversão de emergência.

#### <a name="deprecated-policies"></a>Políticas preteridas

- [MetricsReportingEnabled](./microsoft-edge-policies.md#metricsreportingenabled) - habilita o uso e os relatórios de dados relacionados a falhas.
- [SendSiteInfoToImproveServices](./microsoft-edge-policies.md#sendsiteinfotoimproveservices) - envia informações do site para melhorar os serviços da Microsoft.

#### <a name="obsoleted-policy"></a>Política obsoleta

[TLS13HardeningForLocalAnchorsEnabled](./microsoft-edge-policies.md#tls13hardeningforlocalanchorsenabled)- Habilita um recurso de segurança TLS 1,3 para âncoras de confiança locais.

## <a name="version-85056470-october-6"></a>Versão 85.0.564.70 : 6 de outubro

Correção de vários bugs e problemas de desempenho.

## <a name="version-85056468-october-1"></a>Versão 85.0.564.68: 1 de outubro

Correção de vários bugs e problemas de desempenho.

## <a name="version-85056463-september-23"></a>Versão 85.0.564.63: 23 de setembro

As atualizações de segurança estão listadas [aqui](./microsoft-edge-relnotes-security.md#september-23-2020)

## <a name="version-85056451-september-9"></a>Versão 85.0.564.51: 9 de setembro

As atualizações de segurança estão listadas [aqui](./microsoft-edge-relnotes-security.md#september-9-2020)

## <a name="version-85056444-august-31"></a>Versão 85.0.564.44: 31 de agosto

Correção de vários bugs e problemas de desempenho.

<!-- 85.0.564.41: August 27 -->

## <a name="version-85056441-august-27"></a>Versão 85.0.564.41: 27 de agosto

As atualizações de segurança estão listadas [aqui](./microsoft-edge-relnotes-security.md#august-27-2020)

### <a name="feature-updates"></a>Atualizações de recursos

- **Sincronização local de Favoritos e Configurações**. Agora, você pode sincronizar os favoritos do navegador e as configurações entre os perfis do Active Directory dentro de seu próprio ambiente sem a necessidade de sincronização na nuvem.

- **O suporte à Política de Grupo do Microsoft Edge para combinações de sites e aplicativos confiáveis para iniciar sem aviso de confirmação.**. Foi acrescentado o suporte à Política de Grupo que permite aos administradores adicionar combinações de sites e aplicativos confiáveis ​​para inicialização sem o aviso de confirmação. Isto adiciona capacidade aos administradores para configurar combinações de protocolo/origem confiáveis (como os aplicativos do Microsoft 365) para seus usuários finais suprimirem a solicitação de confirmação ao navegar para uma URL que contenha um protocolo de aplicativo.

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

## <a name="version-84052263-august-20"></a>Versão 84.0.522.63: 20 de agosto

As atualizações de segurança estão listadas [aqui](./microsoft-edge-relnotes-security.md#august-20-2020).

## <a name="version-84052261-august-17"></a>Versão 84.0.522.61: 17 de agosto

Correção de vários bugs e problemas de desempenho.

## <a name="version-84052259-august-11"></a>Versão 84.0.522.59: 11 de agosto

As atualizações de segurança estão listadas [aqui](./microsoft-edge-relnotes-security.md#august-11-2020)

## <a name="version-84052258-august-10"></a>Versão 84.0.522.58: 10 de agosto

Correção de vários bugs e problemas de desempenho.

## <a name="version-84052252-august-1"></a>Versão 84.0.522.52: 1º de agosto

Correção de vários bugs e problemas de desempenho.

## <a name="version-84052250-july-31"></a>Version 84.0.522.50: 31 de julho

Correção de vários bugs e problemas de desempenho.

## <a name="version-84052249-july-29"></a>Versão 84.0.522.49: 29 de julho

As atualizações de segurança estão listadas [aqui](./microsoft-edge-relnotes-security.md#july-29-2020)

## <a name="version-84052248-july-28"></a>Version 84.0.522.48: 28 de julho

Correção de vários bugs e problemas de desempenho.

## <a name="version-84052244-july-23"></a>Version 84.0.522.44: 23 de julho

Correção de vários bugs e problemas de desempenho.

## <a name="version-84052240-july-16"></a>Version 84.0.522.40: 16 de julho

As atualizações de segurança estão listadas [aqui](./microsoft-edge-relnotes-security.md#july-16-2020)

### <a name="feature-updates"></a>Atualizações de recursos

- Esta versão do Microsoft Edge fornece uma melhoria na velocidade de download de lista de sites para o modo Internet Explorer. Reduzimos o atraso de download para a lista de sites no modo Internet Explorer para 0 segundo (de uma espera de 60 segundos) na ausência de uma lista de sites armazenados em cache. Também adicionamos suporte à política de grupo para casos em que as navegações de página inicial no modo Internet Explorer precisem ser adiadas até que a lista de sites seja baixada. Para obter mais informações, confira a política [DelayNavigationsForInitialSiteListDownload](./microsoft-edge-policies.md#delaynavigationsforinitialsitelistdownload).

- O Microsoft Edge agora permite que os usuários entrem no navegador quando ele é "executado como administrador" no Windows 10. Isso ajudará os clientes que usam o Microsoft Edge no Windows Server ou nos cenários de área de trabalho remota ou área restrita.

- O Microsoft Edge agora oferece suporte total ao mouse quando estiver no modo de tela inteira. Agora, você pode usar o mouse para acessar as guias, a barra de endereços e outros itens sem ter que sair do modo de tela inteira.

- Melhoria na compra online. Adicione apelidos personalizados para cartões de crédito ou débitos salvos. Agora, você pode distinguir e diferenciar os cartões de crédito ao fazer compras online. Dar apelidos aos cartões de crédito ou débito permite que você escolha o cartão correto ao usar o preenchimento automático para selecionar um método de pagamento.

- O TLS/1.0 e o TLS/1.1 estão desabilitados por padrão.  A política [SSLVersionMin](./microsoft-edge-policies.md#sslversionmin) permite reabilitar o TLS/1.0 e o TLS/1.1. Essa política permanecerá disponível pelo menos até a versão 88 do Microsoft Edge. Para saber mais, confira [Compatibilidade de sites - alterações que afetam o Microsoft Edge](/microsoft-edge/web-platform/site-impacting-changes).

- Aperfeiçoamentos do recurso Coleções:

  - Uma funcionalidade de anotação foi adicionada, o que permite que você adicione uma anotação ou comentário a um item em uma coleção. As anotações são agrupadas e permanecem anexadas a um item, mesmo que você organize os itens em uma coleção. Para experimentar esse novo recurso, clique com o botão direito do mouse em um item e escolha "Adicionar anotação".
  - Você pode alterar a cor da tela de fundo das anotações em coleções. Você pode usar a codificação de cores para ajudá-lo a organizar informações e aumentar a produtividade.
  - Os aperfeiçoamentos de desempenho são notáveis, permitindo que você exporte suas coleções para o Excel em menos tempo do que em versões anteriores do Microsoft Edge.

- Suporte adicional à API do Microsoft Edge:

  - A API de acesso ao armazenamento está habilitada para fins de teste. Esse recurso está habilitado para usuários domésticos e usuários da empresa com a política [ExperimentationAndConfigurationServiceControl](./microsoft-edge-policies.md#experimentationandconfigurationservicecontrol) definida como "Total". Esse recurso será habilitado por padrão para todos os usuários no Microsoft Edge Stable versão 85.
  
    À medida que a privacidade está ficando cada vez mais importante para os usuários, as solicitações para padrões mais restritivos de navegador e configurações de aceitação de usuário, como bloqueio de todo o acesso de armazenamento de terceiros, são cada vez mais comuns. Embora essas configurações ajudem a melhorar a privacidade e bloquear o acesso indesejado de terceiros desconhecidos ou não confiáveis, eles podem ter efeitos colaterais indesejados, como bloquear o acesso a conteúdo que o usuário pode querer ver (por exemplo, mídia social e conteúdo de mídia inserida.)

    A API de Acesso ao Armazenamento permite acesso ao armazenamento primário em um contexto de terceiros quando um usuário tem providenciado uma intenção direta de permitir o armazenamento que de outra forma seria bloqueado pela configuração atual do navegador. Para saber mais, veja [API de Acesso de Armazenamento](https://www.chromestatus.com/feature/5612590694662144).

  - A API do Sistema de Arquivos Nativo, o que significa que você pode conceder permissões aos sites para editar arquivos ou pastas por meio da API do Sistema de Arquivos Nativo.

- Aperfeiçoamentos em PDF:

  - O recurso Ler em Voz Alta para PDF permite que os usuários ouçam o conteúdo em PDF enquanto realizam outras tarefas que podem ser importantes para eles. Ele também ajuda os alunos com estilo de aprendizagem auditivo-visual a se concentrarem em ler o conteúdo, facilitando o aprendizado.
  - Edição de arquivo PDF aperfeiçoada. Agora, você pode salvar uma edição feita em um PDF em vez de salvar uma cópia sempre que editar o PDF.

- O Microsoft Edge agora oferece a opção Tradução na Leitura Avançada. Quando um usuário abre o modo de exibição de Leitura Avançada, há agora a opção de traduzir a página para o idioma desejado.

- Várias atualizações do DevTools, incluindo o suporte à personalização de atalhos de teclado para corresponder ao VC Code e à visualização do DevTools em alto contraste.  Para obter mais detalhes, consulte [Novidades no DevTools (Microsoft Edge 84)](/microsoft-edge/devtools-guide-chromium/whats-new/2020/05/devtools).

### <a name="policy-updates"></a>Atualizações de política

#### <a name="new-policies"></a>Novas políticas

Sete novas políticas foram adicionadas. Baixe os modelos administrativos atualizados da [página inicial do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise). As novas políticas a seguir foram adicionadas.

- [AppCacheForceEnabled](./microsoft-edge-policies.md#appcacheforceenabled) - Permite reabilitar o recurso AppCache, mesmo que ele esteja desativado por padrão.
- [ApplicationGuardContainerProxy](./microsoft-edge-policies.md#applicationguardcontainerproxy)- Definir as configurações para o Proxy do Contêiner do Application Guard.
- [DelayNavigationsForInitialSiteListDownload](./microsoft-edge-policies.md#delaynavigationsforinitialsitelistdownload) - Exigir que a lista de sites no Modo Empresarial esteja disponível antes da navegação na guia.
- [WinHttpProxyResolverEnabled](./microsoft-edge-policies.md#winhttpproxyresolverenabled): Usar o solucionador de proxy do Windows.
- [InternetExplorerIntegrationEnhancedHangDetection](./microsoft-edge-policies.md#internetexplorerintegrationenhancedhangdetection)- Configurar detecção de suspensão avançada no modo Internet Explorer.
- [NativeWindowOcclusionEnabled](./microsoft-edge-policies.md#nativewindowocclusionenabled) - para reduzir o consumo de CPU e de energia, o Microsoft Edge detectará quando uma janela é coberta por outras janelas e suspenderá os pixels da pintura do trabalho.
- [NavigationDelayForInitialSiteListDownloadTimeout](./microsoft-edge-policies.md#navigationdelayforinitialsitelistdownloadtimeout) -Definir um tempo limite para o atraso da navegação da guia para a Lista de Sites no Modo Empresarial.

#### <a name="deprecated-policies"></a>Políticas preteridas

- [AllowSyncXHRInPageDismissal](./microsoft-edge-policies.md#allowsyncxhrinpagedismissal) - Autorizar páginas a enviar solicitações de XHR síncronas durante a descarte da página.
- [BuiltinCertificateVerifierEnabled](./microsoft-edge-policies.md#builtincertificateverifierenabled) - Determina se o verificador de certificado interno será usado para verificar certificados do servidor.
- [StricterMixedContentTreatmentEnabled](./microsoft-edge-policies.md#strictermixedcontenttreatmentenabled)- Habilita um tratamento mais estrito para conteúdo misto.

#### <a name="obsoleted-policy"></a>Política obsoleta

[ForceNetworkInProcess](./microsoft-edge-policies.md#forcenetworkinprocess) - Forçar a execução do código de rede no processo do navegador.

<!-- End 84 -->
## <a name="version-83047864-july-13"></a>Version 83.0.478.64: 13 de julho

Correção de vários bugs e problemas de desempenho.

## <a name="version-83047861-july-7"></a>Version 83.0.478.61: 7 de julho

Correção de vários bugs e problemas de desempenho.

## <a name="version-83047858-june-30"></a>Versão 83.0.478.58: 30 de junho

Correção de vários bugs e problemas de desempenho.

## <a name="version-83047856-june-24"></a>Versão 83.0.478.56: 24 de junho

Correção de vários bugs e problemas de desempenho.

As atualizações de segurança estão listadas [aqui](./microsoft-edge-relnotes-security.md#june-24-2020)

## <a name="version-83047854-june-17"></a>Versão 83.0.478.54: 17 de junho

As atualizações de segurança estão listadas [aqui](./microsoft-edge-relnotes-security.md#june-17-2020)

## <a name="version-83047850-june-15"></a>Versão 83.0.478.50: 15 de junho

Correção de vários bugs e problemas de desempenho.

## <a name="version-83047845-june-4"></a>Versão 83.0.478.45: 4 de junho

As atualizações de segurança estão listadas [aqui](./microsoft-edge-relnotes-security.md#june-4-2020)

## <a name="version-83047844-june-1"></a>Versão 83.0.478.44: 1 de junho

Correção de vários bugs e problemas de desempenho.

## <a name="version-83047837-may-21"></a>Versão 83.0.478.37: 21 de maio

As atualizações de segurança estão listadas [aqui](./microsoft-edge-relnotes-security.md#may-21-2020)

### <a name="feature-updates"></a>Atualizações de recursos

- As atualizações do Microsoft Edge agora serão implantadas gradualmente. No futuro, as atualizações para o Microsoft Edge serão implantadas para os usuários em período de alguns dias. Isso nos permite proteger melhor as atualizações de bugs acidentais, o que melhora a experiência de atualização. Como usuário, você continuará a receber atualizações automáticas. Se a sua organização não estiver inscrita para as atualizações automáticas, você não serão afetados por essa alteração. Para saber mais, confira o artigo [Distribuições progressivas](microsoft-edge-update-progressive-rollout.md).
- Melhorias no Microsoft Defender SmartScreen: foram feitas várias melhorias no serviço Microsoft Defender SmartScreen, como proteção melhorada contra sites mal-intencionados que são redirecionados durante o carregamento e bloqueio de quadros de nível superior que substitui completamente sites mal-intencionados pela página de segurança do Microsoft Defender SmartScreen. O bloqueio de quadros de nível superior impede a reprodução de áudio e outras mídias do site mal-intencionado, o que proporciona uma experiência mais fácil e menos confusa.

- Em resposta a comentários dos usuários, os usuários agora podem impedir a limpeza de determinados cookies automaticamente quando o navegador é fechado. Essa opção será útil se houver um site do qual os usuários não queiram ser desconectados, mas ainda querem que todos os outros cookies sejam removidos quando o navegador fechar. Para usar esse recurso, acesse *edge://settings/clearBrowsingDataOnClose* e ative a opção "Cookies e outros dados do site".

- A Troca Automática de Perfis agora está disponível para ajudar você a acessar seu conteúdo de trabalho com mais facilidade em diferentes perfis. Se você usar vários perfis no trabalho, poderá verificar esse recurso navegando para um site que exija autenticação da sua conta corporativa ou de estudante enquanto estiver no seu perfil pessoal. Quando detectarmos isso, você receberá uma solicitação para mudar para o seu perfil de trabalho para acessar o site sem precisar se autenticar. Quando você escolhe o perfil de trabalho para o qual deseja mudar, o site simplesmente abre no seu perfil de trabalho. Esse recurso de mudança de perfil ajuda você a manter seus dados pessoais e de trabalho separados e a acessar seu conteúdo de trabalho com mais facilidade. Se você não quiser que o recurso solicite a troca de perfis, você pode escolher a opção não me pergunte novamente isso ficará fora do seu caminho.

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

- Os usuários podem definir o Microsoft Edge como navegador padrão diretamente no Microsoft Edge **Configurações**. Isso permite aos usuários alterarem seu navegador padrão, dentro do contexto do próprio navegador, em vez de precisar pesquisar as configurações do sistema operacional. Para usar esse recurso, vá para *edge://settings/defaultBrowser* e clique em **tornar padrão**.

- Várias atualizações do DevTools, incluindo o suporte à depuração remota, aperfeiçoamentos na IU e muito mais. Para obter mais detalhes, consulte [Novidades no DevTools (Microsoft Edge 83)](/microsoft-edge/devtools-guide-chromium/whats-new/2020/03/devtools).

- Microsoft Defender para Aplicativos de Nuvem cenário de aviso agora está disponível. Isso permite que os administradores configurem o aviso, uma nova categoria de blocos do Defender para Aplicativos na Nuvem, em que o usuário pode substituir uma página de bloco do Defender para Aplicativos na Nuvem. Os bloqueios do MDATP E5 são nativamente integrados aos bloqueios SmartScreen no Microsoft Edge para obter uma experiência perfeita. Essa experiência permite um bloco vermelho de página inteira com a mensagem "este site é bloqueado pela sua organização", em vez de apenas uma notificação do sistema.

- Não permitir um XMLHttpRequest síncrono no descarte de página. O envio de XMLHttpRequests síncronos durante o carregamento de uma página da Web será removido. Essa alteração melhorará o desempenho e a confiabilidade do navegador, mas poderá afetar os aplicativos da Web que ainda não foram atualizados para usar APIs da Web mais modernas, incluindo sendBeacon e FETCH. A Política de Grupo para desabilitar essa alteração e permitir XHR síncronos durante a transmissão de página estará disponível até o Microsoft Edge 88. Para saber mais, confira [Compatibilidade de sites - alterações que afetam o Microsoft Edge](/microsoft-edge/web-platform/site-impacting-changes).

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

<!-- end 83 -->

## <a name="version-81041677-may-18"></a>Versão 81.0.416.77: 18 de maio

Correção de vários bugs e problemas de desempenho.

## <a name="version-81041672-may-7"></a>Versão 81.0.416.72: 7 de maio

As atualizações de segurança estão listadas [aqui](./microsoft-edge-relnotes-security.md#may-7-2020)

## <a name="version-81041668-april-29"></a>Versão 81.0.416.68: 29 de abril

As atualizações de segurança estão listadas [aqui](./microsoft-edge-relnotes-security.md#april-29-2020)

## <a name="version-81041664-april-23"></a>Versão 81.0.416.64: 23 de abril

As atualizações de segurança estão listadas [aqui](./microsoft-edge-relnotes-security.md#april-23-2020)

## <a name="version-81041658-april-17"></a>Versão 81.0.416.58: 17 de abril

As atualizações de segurança estão listadas [aqui](./microsoft-edge-relnotes-security.md#april-17-2020)

## <a name="version-81041653-april-13"></a>Versão 81.0.416.53: 13 de abril

As atualizações de segurança estão listadas [aqui](./microsoft-edge-relnotes-security.md#april-13-2020)

### <a name="feature-updates"></a>Atualizações de recursos

- Adicionado suporte à Proteção de Informações do Windows (WIP), que ajuda as empresas a proteger dados confidenciais contra divulgação não autorizada. [Saiba mais](./microsoft-edge-security-windows-information-protection.md).

- Agora as coleções estão disponíveis. Para começar, clique no ícone Coleções ao lado da barra de endereço. Esta ação abrirá o painel Coleções, no qual você pode criar, editar e exibir Coleções. Projetamos Coleções com base no que você faz na Web. Se você for um comprador, um viajante ou um aluno, as Coleções poderão ajudá-lo. [Saiba mais](https://blogs.windows.com/msedgedev/2019/12/09/improvements-collections-sync-microsoft-edge/#LuDPRDUDCgdgdOVt.97).

- Permitir a remoção (Ocultar da barra de ferramentas) do botão coleções na barra de ferramentas do Microsoft Edge para obter consistência.

- A entrada local de uma conta do Active Directory local só será direcionada a organizações que as ativam.  Se os usuários já tiverem feito login com uma conta local do AD, eles poderão sair dela. Os usuários só entrarão automaticamente com a conta primária em seu sistema operacional se for uma conta Microsoft ou uma conta do Azure Active Directory. Os administradores podem habilitar para entrar automaticamente com uma conta do AD local usando a política ConfigureOnPremisesAccountAutoSignIn.

- Application Guard. Suporte para extensões agora disponível no contêiner.

- Foi adicionada uma mensagem para informar aos usuários que o Internet Explorer não está instalado quando eles navegam para uma página configurada para abrir no modo Internet Explorer.

- A ferramenta modo de exibição 3D foi atualizada no Microsoft Edge DevTools com um novo recurso que ajuda a depurar o contexto de empilhamento de índice z. O modo de exibição 3D mostra uma representação da profundidade do DOM (modelo de objeto do documento) usando a cor e o empilhamento, e o modo de exibição de índice z ajuda a isolar os diferentes contextos de empilhamento da sua página. [Saiba mais](https://blogs.windows.com/msedgedev/2020/01/23/debug-z-index-3d-view-edge-devtools/).

- As ferramentas de desenvolvimento F12 estão localizadas em 10 novos idiomas para que correspondam ao idioma usado no restante do navegador. [Saiba mais](https://blogs.windows.com/msedgedev/2020/02/04/localizing-edge-devtools/).

- Suporte adicional para a reprodução de Dolby Vision. No Windows 10 Build 17134 com Dolby Vision habilitado (Atualização de abril de 2018), os sites podem mostrar o conteúdo de visão Dolby. Veja como habilitar o conteúdo da visão Dolby da [Netflix](https://help.netflix.com/en/node/42384).

- O Microsoft Edge agora pode identificar e remover favoritos duplicados e pastas de mesclagem com o mesmo nome. Para acessar a ferramenta, clique na estrela na barra de ferramentas do navegador e selecione “Remover favoritos duplicados”.  Você pode confirmar que as alterações e as atualizações dos seus favoritos serão sincronizadas entre os dispositivos.

- Nós ouvimos de usuários que pode ser difícil distinguir uma janela de navegação normal no tema escuro de uma janela InPrivate, porque os quadros de janela são escuros. A nova pílula azul sólida InPrivate no canto superior direito ajuda a garantir aos usuários de que eles estão navegando no InPrivate.

- Abra links externos no perfil correto do navegador. Selecione um perfil padrão para que os links abertos para aplicativos externos sejam abertos a partir de *edge://settings/multiProfileSettings*.

- Foi adicionado um aviso que alerta os usuários que fazem login em um perfil de navegador com uma conta depois de fazer login anteriormente com outra conta. Esse aviso ajudará a impedir a fusão não intencional de dados.

- Caso tenha cartões de pagamento salvos em sua conta da Microsoft, você poderá usá-los no Microsoft Edge durante o preenchimento dos formulários de pagamento. Os cartões em sua conta da Microsoft serão sincronizados entre os dispositivos da área de trabalho e os detalhes completos serão compartilhados com o site após a autenticação de dois fatores (código de segurança e identidade da Microsoft). Para maior praticidade, você pode optar por salvar com segurança uma cópia do cartão no dispositivo durante a autenticação.

- O Foco de Linha foi projetado para os usuários que preferem se concentrar em uma parte limitada do conteúdo conforme eles são lidos. Ele permite que os usuários mantenham o foco em uma, três ou cinco linhas por vez e escurece o restante da página para permitir que os usuários leiam sem distrações. Os usuários podem rolar a tela usando o toque ou as teclas de direção, e o foco é deslocado de acordo.

- O Microsoft Edge agora está integrado ao verificador ortográfico do Windows nas plataformas do Windows 8.1 e posteriores. Esta integração fornece maior suporte a idiomas, com acesso a mais dicionários de idiomas e a capacidade de usar dicionários personalizados do Windows. Não é necessária nenhuma ação adicional dos usuários quando um idioma foi adicionado nas configurações de idioma do SO. Além disso, uma alternância de verificação ortográfica de idioma é ativada nas configurações do Microsoft Edge.

- Agora, quando os documentos em PDF estão abertos usando o Microsoft Edge, os usuários podem criar destaques, alterar a cor e excluir realces. Esse recurso ajuda a referenciar partes importantes do documento posteriormente e a colaborar.

- Ao carregar documentos longos em PDF que foram otimizados para a Web, as páginas visualizadas pelo usuário serão carregadas mais rapidamente, paralelamente, enquanto o restante do documento estiver sendo carregado.

- Agora é mais fácil iniciar a leitura avançada de um site pressionando a tecla F9.

- Agora é mais fácil começar a ler em voz alta usando um atalho de teclado (Ctrl + Shift + U).

- Adicionado um parâmetro de linha de comando MSI que permite suprimir a criação de ícones da área de trabalho ao instalar o Microsoft Edge. O exemplo a seguir mostra como usar esse novo parâmetro: <br>
`MicrosoftEdgeEnterpriseX64.msi DONOTCREATEDESKTOPSHORTCUT=true`<br>
Haverá uma política de grupo para oferecer suporte a essa funcionalidade em uma próxima versão.

### <a name="policy-updates"></a>Atualizações de política

#### <a name="new-policies"></a>Novas políticas

Foram adicionadas 11 novas políticas. Baixe os modelos administrativos atualizados da [página inicial do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise). As novas políticas a seguir foram adicionadas.

- [AmbientAuthenticationInPrivateModesEnabled](./microsoft-edge-policies.md#ambientauthenticationinprivatemodesenabled)- Habilite a autenticação ambiente para perfis InPrivate e Guest. 
- [AudioSandboxEnabled](./microsoft-edge-policies.md#audiosandboxenabled)- Permite que a caixa de proteção de áudio seja executada.
- [ForceLegacyDefaultReferrerPolicy](./microsoft-edge-policies.md#forcelegacydefaultreferrerpolicy): Usa uma política referencial padrão de no-referrer-when-downgrade.
- [GloballyScopeHTTPAuthCacheEnabled](./microsoft-edge-policies.md#globallyscopehttpauthcacheenabled)- Habilita o cache de autenticação HTTP globalmente.
- [ImportExtensions](./microsoft-edge-policies.md#importextensions)- Permite a importação de extensões.
- [ImportCookies](./microsoft-edge-policies.md#importcookies)- Permite a importação de cookies.
- [ImportShortcuts](./microsoft-edge-policies.md#importshortcuts)- Permite a importação de atalhos.
- [InternetExplorerIntegrationSiteRedirect](./microsoft-edge-policies.md#internetexplorerintegrationsiteredirect)Especifica como as navegações "na página" para sites não configurados se comportam quando iniciadas nas páginas do modo Internet Explorer.
- [StricterMixedContentTreatmentEnabled](./microsoft-edge-policies.md#strictermixedcontenttreatmentenabled)- Habilita um tratamento mais estrito para conteúdo misto.
- [TLS13HardeningForLocalAnchorsEnabled](./microsoft-edge-policies.md#tls13hardeningforlocalanchorsenabled)- Habilita um recurso de segurança TLS 1,3 para âncoras de confiança locais.
- [ConfigureOnPremisesAccountAutoSignIn](./microsoft-edge-policies.md#configureonpremisesaccountautosignin)- Configura o login automático com uma conta de domínio do Active Directory quando não houver nenhuma conta de domínio do Azure AD.

#### <a name="policy-name-and-caption-changes"></a>Alterações de nome e legenda da política

A política `OmniboxMSBProviderEnabled` é alterada para [AddressBarMicrosoftSearchInBingProviderEnabled](/DeployEdge/microsoft-edge-policies#addressbarmicrosoftsearchinbingproviderenabled) - A legenda da política é "Habilitar a pesquisa da Microsoft nas sugestões do Bing na barra de endereço".

#### <a name="deprecated-policies"></a>Políticas preteridas

As seguintes políticas continuam a funcionar nesta versão. Elas se tornarão "obsoletas" em uma versão futura.

- [WebComponentsV0Enabled](./microsoft-edge-policies.md#webcomponentsv0enabled) - Reabilita a API de componentes Web V0 até M84.
- [WebDriverOverridesIncompatiblePolicies](./microsoft-edge-policies.md#webdriveroverridesincompatiblepolicies)- Permite que o WebDriver substitua incompatível.

#### <a name="resolved-issues"></a>Problemas resolvidos

- Foi corrigido um problema em que o modo IE no Microsoft Edge fazia com que uma caixa de diálogo de download em andamento fosse exibida mesmo após o download do arquivo.
- Foi corrigido um problema em que o Microsoft Edge estava descartando cookies de sessão quando uma página que já estava no modo IE era acionada para abrir uma nova guia do modo IE.

## <a name="version-800361111-april-7"></a>Versão 80.0.361.111: 7 de abril

Correção de vários bugs e problemas de desempenho.

## <a name="version-800361109-april-1"></a>Versão 80.0.361.109: 1º de abril

As atualizações de segurança estão listadas [aqui](./microsoft-edge-relnotes-security.md#april-1-2020)

## <a name="version-80036169-march-19"></a>Versão 80.0.361.69: 19 de março

As atualizações de segurança estão listadas [aqui](./microsoft-edge-relnotes-security.md#march-19-2020)

## <a name="version-80036166-march-4"></a>Versão 80.0.361.66: 4 de março

As atualizações de segurança estão listadas [aqui](./microsoft-edge-relnotes-security.md#march-4-2020)

## <a name="version-80036162-february-25"></a>Versão 80.0.361.62: 25 de fevereiro

As atualizações de segurança estão listadas [aqui](./microsoft-edge-relnotes-security.md#february-25-2020)

## <a name="version-80036157-february-20"></a>Versão 80.0.361.57: 20 de fevereiro

As atualizações de segurança estão listadas [aqui](./microsoft-edge-relnotes-security.md#february-20-2020)

## <a name="version-80036156-february-19"></a>Versão 80.0.361.56: 19 de fevereiro

Correção de vários bugs e problemas de desempenho.

## <a name="version-80036154-february-14"></a>Versão 80.0.361.54: 14 de fevereiro

### <a name="resolved-issues"></a>Problemas resolvidos

- Foi corrigido um problema em que senha, pagamento e cookies não são importados no Microsoft Edge.

## <a name="version-80036150-february-11"></a>Versão 80.0.361.50: 11 de fevereiro

Correção de vários bugs e problemas de desempenho.

## <a name="version-80036148-february-7"></a>Versão 80.0.361.48: 07 de fevereiro

As atualizações de segurança estão listadas [aqui](./microsoft-edge-relnotes-security.md#february-7-2020)

### <a name="feature-updates"></a>Atualizações de recursos

- Proteção do SmartScreen adicionada para baixar aplicativos potencialmente indesejados. [Saiba mais](/windows/security/threat-protection/windows-defender-antivirus/detect-block-potentially-unwanted-apps-windows-defender-antivirus)
- Suporte adicional para a reprodução de Dolby Vision.
- Usuários habilitados do Windows Mixed Reality para visualizar vídeos em 360 ° nos fones de ouvido VR.
- Foi adicionada uma opção ao modo de exibição de leitura para aumentar o espaçamento do texto.
- Suporte adicional para a exclusão do link usando a borracha da Caneta Surface.
- Suporte adicionado para usar as teclas de direção e a barra de espaços para desenhar capturas de tela de comentários no modo do editor.
- Melhorou a confiabilidade das capturas de tela para que parem de aparecer totalmente pretas ao enviar feedback.
- Adicionado suporte de tema escuro à nova página da guia local que é mostrada quando o dispositivo não está conectado à Internet.
- Foi adicionada a capacidade de restaurar sites instalados como aplicativos quando uma sessão do navegador é restaurada após atualização, erro, etc.
- Adicionado suporte ao tema escuro à interface do usuário do PDF quando o navegador é gerenciado pela Diretiva de Grupo.
- Atualização do Adobe Flash para a versão 32.0.0.321. [Saiba mais](https://helpx.adobe.com/flash-player/release-note/fp_32_air_32_release_notes.html)

### <a name="policy-updates"></a>Atualizações de política

#### <a name="new-policies"></a>Novas políticas

16 novas políticas foram adicionadas. Baixe os modelos administrativos atualizados da [página inicial do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise). As novas políticas a seguir foram adicionadas.

- [AlternateErrorPagesEnabled](./microsoft-edge-policies.md#alternateerrorpagesenabled) -sugere páginas semelhantes quando uma página da Web não puder ser encontrada.
- [DefaultInsecureContentSetting](./microsoft-edge-policies.md#defaultinsecurecontentsetting) -controla o uso de exceções de conteúdo inseguro.
- [DNSInterceptionChecksEnabled](./microsoft-edge-policies.md#dnsinterceptionchecksenabled) -verificações de interceptação de DNS habilitadas.
- [HideFirstRunExperience](./microsoft-edge-policies.md#hidefirstrunexperience) -oculta a experiência de primeira execução e a tela inicial.
- [InsecureContentAllowedForUrls](./microsoft-edge-policies.md#insecurecontentallowedforurls) -permitir conteúdo não seguro em sites especificados.
- [InsecureContentBlockedForUrls](./microsoft-edge-policies.md#insecurecontentblockedforurls) -bloqueia conteúdo não seguro em sites especificados.
- [LegacySameSiteCookieBehaviorEnabled](./microsoft-edge-policies.md#legacysamesitecookiebehaviorenabled) -habilita a configuração padrão de cookie herdado SameSite padrão.
- [LegacySameSiteCookieBehaviorEnabledForDomainList](./microsoft-edge-policies.md#legacysamesitecookiebehaviorenabledfordomainlist) -reverte para comportamento SameSite herdado de cookies em sites especificados.
- [PaymentMethodQueryEnabled](./microsoft-edge-policies.md#paymentmethodqueryenabled) -permite que os sites consultem os métodos de pagamento disponíveis.
- [PersonalizationReportingEnabled](./microsoft-edge-policies.md#personalizationreportingenabled) – permite a personalização de anúncios, pesquisas e notícias enviando o histórico de navegação à Microsoft.
- [PinningWizardAllowed](./microsoft-edge-policies.md#pinningwizardallowed) -permite que o assistente seja fixado na barra de tarefas.
- [SmartScreenPuaEnabled](./microsoft-edge-policies.md#smartscreenpuaenabled) -configura o Microsoft Defender SmartScreen para bloquear aplicativos potencialmente indesejados.
- [TotalMemoryLimitMb](./microsoft-edge-policies.md#totalmemorylimitmb) -define o limite em megabytes de memória que uma única instância do Microsoft Edge pode usar.
- [WebAppInstallForceList](./microsoft-edge-policies.md#webappinstallforcelist) -configura a lista de aplicativos Web instalados pela força.
- [WebComponentsV0Enabled](./microsoft-edge-policies.md#webcomponentsv0enabled) -reabilita a API de componentes Web V0 até M84.
- [WebRtcLocalIpsAllowedUrls](./microsoft-edge-policies.md#webrtclocalipsallowedurls) -gerencia a exposição de endereços IP locais por WebRTC.

#### <a name="deprecated-policies"></a>Políticas preteridas

A política a seguir foi substituída.

- [NewTabPageCompanyLogo](./microsoft-edge-policies.md#newtabpagecompanylogo) -define o logotipo da empresa da nova guia.

### <a name="resolved-issues"></a>Problemas resolvidos

- Corrigido um problema em que o áudio não estava funcionando no ambiente Citrix.
- Foi corrigido um problema em que o Microsoft Edge e a experiência lado a lado do Microsoft Edge resulta em links e erros herdados.

## <a name="see-also"></a>Consulte também

- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
