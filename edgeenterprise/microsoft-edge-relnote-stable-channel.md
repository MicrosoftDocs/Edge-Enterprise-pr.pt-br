---
title: Notas de versão do Microsoft Edge para Stable Channel
ms.author: leahtu
author: dan-wesley
manager: srugh
ms.date: 04/07/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Notas de versão do Microsoft Edge para Stable Channel
ms.openlocfilehash: 0cf9c2d0ac7a60c03ad6c80d4186629d296a73c6
ms.sourcegitcommit: dd8cdbd35726c795ddce917e549ddf17ee7f5290
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/11/2022
ms.locfileid: "12473662"
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

## <a name="see-also"></a>Consulte também

- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
