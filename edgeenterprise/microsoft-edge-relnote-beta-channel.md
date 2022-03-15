---
title: Notas da versão do Microsoft Edge para canal beta
ms.author: leahtu
author: dan-wesley
manager: srugh
ms.date: 03/14/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Notas da versão do Microsoft Edge para canal beta
ms.openlocfilehash: 8633a5f15fe737a64a0160de714c1c4e53541482
ms.sourcegitcommit: 556aca8dde42dd66364427f095e8e473b86651a0
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2022
ms.locfileid: "12445705"
---
# <a name="release-notes-for-microsoft-edge-beta-channel"></a>Notas de versão do canal do Microsoft Edge beta

Estas notas de versão fornecem informações sobre os novos recursos e atualizações não relacionadas à segurança que estão inclusos no canal Beta do Microsoft Edge. As versões arquivadas dessas notas de versão estão disponíveis em Notas de versão arquivadas [para Microsoft Edge Beta Channel](./microsoft-edge-relnote-archive-beta-channel.md).

> [!NOTE]
> A Plataforma da Web do Microsoft Edge evolui constantemente para melhorar a experiência, segurança e privacidade do usuário. Para saber mais, confira [Compatibilidade de sites: alterações que afetam o Microsoft Edge](/microsoft-edge/web-platform/site-impacting-changes).

## <a name="version-990115039-march-10"></a>Versão 99.0.1150.39: 10 de março

### <a name="feature-updates"></a>Atualizações de recursos

- **Melhorias na experiência de Gerenciamento de Lista de Sites na Nuvem para Modo IE.** Identifique lacunas em sua lista de sites corporativos configurando relatórios de comentários de site com as políticas [InternetExplorerIntegrationCloudUserSitesReporting](/deployedge/microsoft-edge-policies#internetexplorerintegrationcloudusersitesreporting) e [InternetExplorerIntegrationCloudNeutralSitesReporting](/deployedge/microsoft-edge-policies#internetexplorerintegrationcloudneutralsitesreporting) . Você pode exibir URLs de lista de sites locais de usuários e URLs de sites neutros potencialmente configuradas incorretamente na experiência de listas de sites Microsoft Edge no Centro de Administração Microsoft 365. Para saber mais, confira [Exibir comentários do site no Administração Microsoft 365 Center](/deployedge/edge-ie-mode-cloud-site-list-mgmt#view-site-feedback-on-the-microsoft-365-admin-center-1).  **Observação:** Esta é uma adoção de recursos controlados. Se você não vir esse recurso, verifique novamente à medida que continuarmos nossa adoção.

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

- **Próximo número de versão de três dígitos na cadeia de caracteres de agente do usuário.** A partir da versão 100, Microsoft Edge enviará um número de versão de três dígitos no User-Agent, por exemplo "Edg/100". A partir do Microsoft Edge 97, os proprietários de sites podem testar essa cadeia de caracteres de agente futura habilitando o sinalizador de experimento **do #force-major-version-to-100** em *edge://flags para* garantir que User-Agent lógica de análise do User-Agent seja robusta e funcione conforme esperado.

- **Personalize experiências de vários perfis com preferências de perfil para sites.** Os usuários podem personalizar sua experiência de vários perfis com a capacidade de criar uma lista personalizada de sites para alternar perfis automáticos em Microsoft Edge.

- **Compartilhamento bidirecional de cookie para modo IE.** Esse recurso expande o recurso de compartilhamento de cookies já disponível e permite que os usuários sincronizem cookies de sessão específicos do modo Internet Explorer/IE para Microsoft Edge. Para obter mais informações, consulte [Compartilhamento de cookies entre o Microsoft Edge e o Internet Explorer](/deployedge/edge-ie-mode-add-guidance-cookieshare).

- **Navegue por documentos PDF usando miniaturas de página.** Agora você poderá navegar pelo documento PDF usando miniaturas que representam as páginas. Essas miniaturas aparecerão no painel no lado esquerdo do leitor de PDF.

- **Configure a lista de domínios para os quais a interface do usuário (interface do usuário) do gerenciador de senhas para Salvar e Preencher será desabilitada.** Use a [política PasswordManagerBlocklist](/deployedge/microsoft-edge-policies#passwordmanagerblocklist) para configurar a lista de domínios (esquemas HTTP/HTTPS e nomes de host) onde Microsoft Edge deve desabilitar o gerenciador de senhas. Isso significa que os fluxos de trabalho Salvar e Preencher serão desabilitados, o que garante que as senhas desses sites não possam ser salvas ou preenchidas automaticamente em formulários da Web.

- **Atualizar extensões para o Microsoft Edge de complementos usando API (em visualização pública).** Você pode integrar essas API diretamente ao pipeline de com build e publicar atualizações de pacote no site Microsoft Edge de complementos. Para saber mais, consulte [Using the Microsoft Edge add-ons API (in private preview)](/microsoft-edge/extensions-chromium/publish/api/using-addons-api)

### <a name="policy-updates"></a>Atualizações de política

#### <a name="new-policies"></a>Novas Políticas

- [AllowGamesMenu](/DeployEdge/microsoft-edge-policies#allowgamesmenu) - Permitir que os usuários acessem o menu de jogos
- [DoNotSilentlyBlockProtocolsFromOrigins](/DeployEdge/microsoft-edge-policies#donotsilentlyblockprotocolsfromorigins) - Definir uma lista de protocolos que não podem ser bloqueados silenciosamente pela proteção anti-inundação
- [HubsSidebarEnabled](/DeployEdge/microsoft-edge-policies#hubssidebarenabled) - Barra lateral Mostrar Hubs
- [InternetExplorerIntegrationCloudNeutralSitesReporting](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationcloudneutralsitesreporting) - Configure reporting of potentially misconfigured neutral site URLs to the M365 Admin Center Site Lists app
- [InternetExplorerIntegrationCloudUserSitesReporting](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationcloudusersitesreporting) - Configurar relatórios de entradas de lista de usuários do modo IE para o aplicativo Listas de Sites do Centro de Administração do M365
- [PasswordManagerBlocklist](/DeployEdge/microsoft-edge-policies#passwordmanagerblocklist) - Configurar a lista de domínios para os quais a interface do usuário do gerenciador de senhas (Salvar e Preencher) será desabilitada
- [RelatedMatchesCloudServiceEnabled](/DeployEdge/microsoft-edge-policies#relatedmatchescloudserviceenabled) - Configure Related Matches in Find on Page
- [SignInCtaOnNtpEnabled](/DeployEdge/microsoft-edge-policies#signinctaonntpenabled) - Habilitar a caixa de diálogo Habilitar entrar clique em ação
- [UserAgentReduction](/DeployEdge/microsoft-edge-policies#useragentreduction) - Habilitar ou desabilitar a User-Agent Redução

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

- **Aprimora sua segurança na Web.** Um modo de navegação no Microsoft Edge em que a segurança do navegador tem prioridade, dando a você uma camada extra de proteção ao navegar na Web. Os administradores podem aplicar as seguintes Políticas de Grupo às áreas de trabalho do usuário final (Windows, macOS e Linux) para ajudar a proteger contra zero dias. Essas políticas também fazem com que sites importantes e aplicativos de linha de negócios continuem a funcionar conforme o esperado. Esse recurso é um grande passo à frente porque permite reduzir os dias ativos imprevistos (com base nas tendências históricas). Quando ligado, esse recurso traz a Proteção de Pilha imposta por hardware, o AcG (Proteção de Código Arbitrário) e o CfG (Content Flow Guard) como suporte a mitigações de segurança para aumentar a segurança dos usuários na Web.
Políticas de grupo:
  - [EnhanceSecurityMode](/DeployEdge/microsoft-edge-policies#enhancesecuritymode)
  - [EnhanceSecurityModeBypassListDomains](/DeployEdge/microsoft-edge-policies#enhancesecuritymodebypasslistdomains)
  - [EnhanceSecurityModeEnforceListDomains](/DeployEdge/microsoft-edge-policies#enhancesecuritymodeenforcelistdomains)

- **Senha primária personalizada.** O navegador já tem a funcionalidade em que os usuários podem adicionar uma etapa de autenticação antes que as senhas salvas sejam preenchidas automaticamente em formulários da Web. Isso adiciona outra camada de privacidade e ajuda a impedir que usuários não autorizados usem senhas salvas para fazer logon em sites. A senha primária personalizada é uma evolução desse mesmo recurso, onde os usuários agora poderão usar uma cadeia de caracteres personalizada de sua escolha como senha principal. Depois de habilitado, os usuários inserirão essa senha para autenticar a si mesmos e terão suas senhas salvas preenchidas automaticamente em formulários da Web.

- **Barras de rolagem de sobreposição adicionadas Microsoft Edge.** Atualizamos nossas barras de rolagem com um design baseado em sobreposição. Os usuários podem ativar esse recurso *em edge://flags*.

### <a name="policy-updates"></a>Atualizações de política

#### <a name="new-policies"></a>Novas Políticas

- [AddressBarEditingEnabled](/DeployEdge/microsoft-edge-policies#addressbareditingenabled) - Configurar a edição da barra de endereços.
- [EdgeFollowEnabled](/DeployEdge/microsoft-edge-policies#edgefollowenabled) - Habilitar o serviço Follow Microsoft Edge.
- [EnhanceSecurityMode](/DeployEdge/microsoft-edge-policies#enhancesecuritymode) - aprimora o estado de segurança Microsoft Edge.
- [EnhanceSecurityModeBypassListDomains](/DeployEdge/microsoft-edge-policies#enhancesecuritymodebypasslistdomains) - Configure the list of domains for which enhance security mode will not be enforced.
- [EnhanceSecurityModeEnforceListDomains](/DeployEdge/microsoft-edge-policies#enhancesecuritymodeenforcelistdomains) - Configure the list of domains for which enhance security mode will always be enforced.
- [InAppSupportEnabled](/DeployEdge/microsoft-edge-policies#inappsupportenabled) - Suporte no aplicativo Habilitado.
- [MicrosoftEdgeInsiderPromotionEnabled](/DeployEdge/microsoft-edge-policies#microsoftedgeinsiderpromotionenabled) - Microsoft Edge Promoção do Insider Habilitada.
- [PrintStickySettings](/DeployEdge/microsoft-edge-policies#printstickysettings) - Configurações pegativas de visualização de impressão.
- [SandboxExternalProtocolBlocked](/DeployEdge/microsoft-edge-policies#sandboxexternalprotocolblocked) - Permitir Microsoft Edge bloquear as navegação para protocolos externos em um iframe em áreas de segurança.
- [U2fSecurityKeyApiEnabled](/DeployEdge/microsoft-edge-policies#u2fsecuritykeyapienabled) - Permitir o uso da API de chave de segurança U2F preterida.

## <a name="version-970107254-january-5"></a>Versão 97.0.1072.54: 5 de janeiro

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-970107252-january-3"></a>Versão 97.0.1072.52: 3 de janeiro

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-970107241-december-20"></a>Versão 97.0.1072.41: 20 de dezembro

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-970107234-december-13"></a>Versão 97.0.1072.34: 13 de dezembro

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-970107228-december-8"></a>Versão 97.0.1072.28: 8 de dezembro

Correção de vários bugs e problemas de desempenho.

<!--- Version 97.0.1072.21: December 1 to Version 96.0.1054.13: November 5  --->
<!--- archive from Version 96.0.1054.8: November 1 to Version 95.0.1020.14: October 5  --->
<!-- archive from version 95.0.1020.9: September 28 to version 94.0.992.14: September 7 ---->
<!-- archive from Version 94.0.992.9: September 2 to Version 92.0.902.40: July 6 -->
<!--Archive on Oct 27 From Version 92.0.902.22: June 21 to Version 89.0.774.23: February 8  -->
<!--- Archived from Version 87.0.664.18: October 26 to to version 89.0.774.18: February 3 ---->
<!--- Archived from Version 87.0.664.12: October 20 to to version 86.0.622.15: September 14 ---->
<!--- Archived to version 86.0.622.11: September 9 ---->
<!--- Archived to version 85.0.564.18: July 28 ---->

## <a name="see-also"></a>Ver também

- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)

