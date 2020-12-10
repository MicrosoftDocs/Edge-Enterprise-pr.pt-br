---
title: Notas de versão do Microsoft Edge para Stable Channel
ms.author: aguta
author: dan-wesley
manager: srugh
ms.date: 12/08/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Notas de versão do Microsoft Edge para Stable Channel
ms.openlocfilehash: e998437308a9fc95ba6cb683561c109797a3e9c9
ms.sourcegitcommit: 1be5f3584b2a9400ca18c3d5483c3c8929ac9dce
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/09/2020
ms.locfileid: "11203593"
---
# Notas de versão do Microsoft Edge Stable Channel

Essas notas de versão fornecem informações dos novos recursos e atualizações não relacionados à segurança que estão inclusos Microsoft Edge Stable Channel. Para entender os canais do Microsoft Edge, confira a [Visão geral dos canais do Microsoft Edge](microsoft-edge-channels.md). Todas as atualizações de segurança estão listadas [aqui](microsoft-edge-relnotes-security.md).

> [!NOTE]
> Para o Canal Estável, as atualizações serão implantadas progressivamente por um ou mais dias. Para saber mais, confira [Distribuições progressivas para as atualizações do Microsoft Edge](microsoft-edge-update-progressive-rollout.md).

## Versão 87.0.664.57: 7 de dezembro

Correção de vários bugs e problemas de desempenho. As atualizações de segurança estão listadas [aqui](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#december-7-2020).

## Versão 87.0.664.55: 3 de dezembro

Correção de vários bugs e problemas de desempenho. O seguinte recurso foi atualizado para este lançamento.

- **O Shopping está habilitado por padrão**. A partir da versão 87 do Microsoft Edge, os usuários corporativos podem se beneficiar das compras no Microsoft Edge. Com os recursos de compra, o Microsoft Edge ajuda os usuários a encontrar cupons e melhores preços ao fazer compras online. (A experiência de cupom foi lançada com a versão estável 87.0.664.41). A experiência de comparação de preços agora está disponível nesta atualização. Este recurso pode ser configurado usando a política [EdgeShoppingAssistantEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#edgeshoppingassistantenabled). Veja nosso [Blog](https://blogs.windows.com/windowsexperience/2020/11/19/finish-up-that-holiday-shopping-with-new-features-from-microsoft-edge-and-bing/) e [Saiba mais](https://docs.microsoft.com/microsoft-edge/privacy-whitepaper#shopping) sobre o Microsoft Shopping.

## Versão 87.0.664.52: 30 de novembro

Correção de vários bugs e problemas de desempenho.

## Versão 87.0.664.47: 23 de novembro

Correção de vários bugs e problemas de desempenho.

<!-- begin major 87 --->
## Versão 87.0.664.41: 19 de novembro

As atualizações de segurança estão listadas [aqui](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#november-19-2020).

### Atualizações de recursos

- **Redirecionamento automático de sites incompatíveis do Internet Explorer para o Microsoft Edge**. A partir da atualização estável do Microsoft Edge 87, os sites públicos que mostram uma mensagem de incompatibilidade no Internet Explorer serão automaticamente redirecionados para o Microsoft Edge. Para saber mais e configurar essa experiência, confira [Redirecionamento de sites incompatíveis](https://docs.microsoft.com/deployedge/edge-learnmore-neededge).

- **Recursos de privacidade do modo de quiosque habilitados**. Começando com o Microsoft Edge versão 87, os recursos do modo de quiosque que ajudarão empresas em relação à privacidade dos dados do usuário serão habilitados. Esses recursos habilitarão experiências, como limpar os dados do usuário ao sair, excluir arquivos baixados e redefinir a experiência de iniciação configurada após uma quantidade específica de tempo ocioso. Saiba mais sobre como [Configurar as opções do modo de quiosque do Microsoft Edge](https://docs.microsoft.com/deployedge/microsoft-edge-configure-kiosk-mode)

- **Recursos de compra habilitados por padrão**. A partir da versão 87 do Microsoft Edge, os usuários corporativos do Microsoft Edge também podem tirar proveito da compra no Edge. Com os recursos de compra, o Microsoft Edge ajuda os usuários a encontrar cupons e melhores preços ao fazer compras online. A experiência de cupom está disponível com esta atualização e a comparação de preços será lançada em futuras atualizações do Microsoft Edge 87. Esse recurso pode ser configurado por meio da política [EdgeShoppingAssistantEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#edgeshoppingassistantenabled) . Veja o nosso [blog](https://blogs.windows.com/windowsexperience/2020/11/19/finish-up-that-holiday-shopping-with-new-features-from-microsoft-edge-and-bing/) e [saiba mais](https://docs.microsoft.com/microsoft-edge/privacy-whitepaper#shopping) sobre o Microsoft shopping.

- **Implantação de ClickOnce habilitada por padrão**. O ClickOnce está habilitado por padrão no Microsoft Edge 87, o que reduz as barreiras para a implantação de software e alinha-se melhor com o comportamento do navegador da Versão Prévia do Microsoft Edge. A partir do Microsoft Edge 87, o estado "Não Configurado" da política de ClickOnceEnabled refletirá o novo estado de ClickOnce padrão Habilitado (em comparação com o estado padrão anterior Desabilitado).

- **A página nova guia da empresa (NTP) integra a produtividade com o conteúdo do feed personalizado e relevante para o trabalho**. O NTP empresarial combina a página de produtividade do Office 365 oferecemos a todos os usuários que entraram com uma conta corporativa ou de estudante com feeds personalizados da empresa e da indústria relevantes para o trabalho que são organizados em uma única página. Os usuários poderão reconhecer o conteúdo familiar do Office 365 e da Pesquisa da Microsoft para Empresas, da plataforma Bing. Além disso, eles podem personalizar facilmente "Meu feed" escolhendo o conteúdo mais relevante para eles do conteúdo e módulos disponíveis para sua organização. Os administradores de TI podem controlar as configurações de feed de notícias para sua organização, incluindo o setor selecionado para a nova página de guia do Edge, acessando o Centro de Administração do Microsoft 365. [Saiba mais](https://blogs.windows.com/msedgedev/2020/10/29/enterprise-new-tab-page-my-feed/)

- **Segurança e privacidade:**

  - Suporte a Associação de Token TLS para sites de política configurada. A associação de Token TLS ajuda a evitar ataques de roubo de token para garantir que os cookies não possam ser reutilizados a partir de um dispositivo que não tenha sido definido inicialmente. O uso da ligação de token TLS exige a configuração da política [AllowTokenBindingForUrls](https://docs.microsoft.com/deployedge/microsoft-edge-policies#allowtokenbindingforurls) e exige que os sites listados ofereçam suporte a esse recurso.

- **Suporte a teclado para marca-texto em arquivos PDF**. Os usuários podem usar as teclas do teclado para realçar qualquer texto em um PDF.

- **Impressão:**

  - Escolha o lado a ser invertido ao imprimir nos dois lados. Os usuários podem optar por virar o lado maior ou o lado menor de uma planilha ao imprimir em ambos os lados.
  - Escolha o modo de rasterização de impressão para a empresa. Controlar como o Microsoft Edge é impresso em uma impressora não PostScript no Windows. Às vezes, os trabalhos de impressão em impressoras não PostScript precisam ser rasterizados para serem impressos corretamente. As opções de impressão são "Total" e "Rápida".

### Atualizações de política

#### Novas políticas

Dez novas políticas foram adicionadas. Baixe os modelos administrativos atualizados da [página inicial do Microsoft Edge Enterprise](https://www.microsoft.com/edge/business/download). As novas políticas a seguir foram adicionadas.

- [ConfigureFriendlyURLFormat](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#configurefriendlyurlformat) - configure o formato de colagem padrão das URLs copiadas do Microsoft Edge e determine se formatos adicionais estarão disponíveis para os usuários.
- [EdgeShoppingAssistantEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#edgeshoppingassistantenabled) - compras no Microsoft Edge habilitadas.
- [HideInternetExplorerRedirectUXForIncompatibleSitesEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#hideinternetexplorerredirectuxforincompatiblesitesenabled) – oculte o diálogo de redirecionamento único e a faixa no Microsoft Edge.
- [KioskAddressBarEditingEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#kioskaddressbareditingenabled) -configure a edição da barra de endereços para a experiência de navegação pública do modo de quiosque.
- [KioskDeleteDownloadsOnExit](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#kioskdeletedownloadsonexit) - exclua arquivos baixados como parte de uma sessão modo de quiosque quando o Microsoft Edge for fechado.
- [PasswordRevealEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#passwordrevealenabled) - habilitar botão de revelação de senha.
- [RedirectSitesFromInternetExplorerPreventBHOInstall](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#redirectsitesfrominternetexplorerpreventbhoinstall) – impedir a instalação do objeto auxiliar de navegador (BHO) para redirecionar sites incompatíveis do Internet Explorer para o Microsoft Edge.
- [RedirectSitesFromInternetExplorerRedirectMode](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#redirectsitesfrominternetexplorerredirectmode) – redirecione sites incompatíveis do Internet Explorer para o Microsoft Edge.
- [SpeechRecognitionEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#speechrecognitionenabled) - configurar Reconhecimento de Fala.
- [WebCaptureEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webcaptureenabled) - habilitar o recurso de captura da Web no Microsoft Edge.

#### Política Preterida

[NewTabPageSetFeedType](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#newtabpagesetfeedtype) - configurar a nova experiência de página da guia Microsoft Edge.

#### Política obsoleta

[EnableDeprecatedWebPlatformFeatures](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#enabledeprecatedwebplatformfeatures) - reative os recursos da plataforma Web preteridos por um tempo limitado.

<!-- end major 87 -->

## Versão 86.0.622.69: 13 de novembro

As atualizações de segurança estão listadas [aqui](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#november-13-2020). Esta atualização contém [CVE-2020-16013](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-16013) e [CVE-2020-16017](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-16017), que foram relatados pela equipe do Chromium por estarem sendo explorados no momento.

## Versão 86.0.622.68: 11 de novembro

As atualizações de segurança estão listadas [aqui](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#november-11-2020)

## Versão 86.0.622.63: 4 de novembro

As atualizações de segurança estão listadas [aqui](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#november-4-2020). Esta atualização contém a [CVE-2020-16009](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-16009), que foi reportada pela equipe Chromium por estar sendo explorado no momento.

## Versão 86.0.622.61: 2 de novembro

Correção de vários bugs e problemas de desempenho.

## Versão 86.0.622.58: 29 de outubro

Correção de vários bugs e problemas de desempenho.

## Versão 86.0.622.56: 27 de outubro

Correção de vários bugs e problemas de desempenho.

## Versão 86.0.622.51 : 22 de outubro

As atualizações de segurança estão listadas [aqui](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#october-22-2020)

## Versão 86.0.622.48: 20 de outubro

Correção de vários bugs e problemas de desempenho.

## Versão 86.0.622.43: 15 de outubro

Correção de vários bugs e problemas de desempenho.

<!-- begin major 86 -->
## Versão 86.0.622.38: 9 de outubro

As atualizações de segurança estão listadas [aqui](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#october-9-2020)

### Atualizações de recursos

* **Reverter para a versão anterior do Microsoft Edge.** O recurso reversão permite que os administradores voltem para uma versão boa conhecida do Microsoft Edge, caso haja algum problema na versão mais recente do Microsoft Edge. **Observação:** A versão estável 86.0.622.38 é a primeira versão para a qual você pode reverter, o que significa que a versão estável 87 é a primeira versão pronta para ser revertida. [Saiba mais](edge-learnmore-rollback.md).

* **Forçar a habilitação da Sincronização por padrão em toda a empresa.**  Os administradores podem habilitar a sincronização das contas do Azure Active Directory (Azure AD) por padrão com a política de [ForceSync](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#forcesync).

* **Mudança de perfil automática no Windows 7 e 8.1.** A mudança de perfil automática disponível atualmente no Microsoft Edge no Windows 10 foi estendida para versões inferiores do Windows (Windows 7 e 8.1). Para saber mais, confira a postagem de blog [mudança de perfil automática](https://blogs.windows.com/msedgedev/2020/04/30/automatic-profile-switching/).

* **SameSite=Lax Cookies por padrão**. Para melhorar a segurança e a privacidade da web, os cookies agora serão padronizados para manipulação como [SameSite=Lax](https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie/SameSite). Isso significa que os cookies só serão enviados em um contexto de first-party e serão omitidos para as solicitações enviadas a terceiros. Essa alteração pode causar impacto de compatibilidade em sites que exigem cookies para recursos de terceiros funcionarem corretamente. Para permitir tais cookies, os desenvolvedores da Web podem marcar cookies que devem ser configurados e enviados a contextos de terceiros, adicionando `SameSite=none` explícitos e atributos `Secure` quando o cookie é definido. As empresas que desejam isentar determinados sites da alteração podem fazer isso usando a política [LegacySameSiteCookieBehaviorEnabledForDomainList](https://docs.microsoft.com/deployedge/microsoft-edge-policies#legacysamesitecookiebehaviorenabledfordomainlist) ou podem recusar a alteração em todos os sites que usam a política [LegacySameSiteCookieBehaviorEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#legacysamesitecookiebehaviorenabled).

* **Remover a API de cache de aplicativo HTML5.**  A partir da versão 86 do Microsoft Edge, a API de cache de aplicativo herdado que permite o uso offline de páginas da Web será removida do Microsoft Edge. Os desenvolvedores da Web devem examinar a [documentação WebDev](https://web.dev/appcache-removal/) para saber mais sobre como substituir a API de cache de aplicativo com Profissionais de Serviço.  Importante: você pode solicitar um [Token OriginTrial do AppCache](https://developers.chrome.com/origintrials/#/view_trial/1776670052997660673) que permite que os sites continuem usando a versão preterida da API de cache de aplicativo até a versão 90 do Microsoft Edge.

* **Segurança e privacidade:**

  * **Substituir as políticas [MetricsReportingEnabled]( https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#metricsreportingenabled) e [SendSiteInformationToImproveServices]( https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sendsiteinfotoimproveservices) para versões inferiores do Windows e macOS.** Essas políticas foram preteridas na versão 86 do Microsoft Edge e se tornarão preteridas na versão 89 do Microsoft Edge.<br>
Essas políticas são substituídas por [Permitir Telemetria](https://go.microsoft.com/fwlink/?linkid=2099569) no Windows 10 e a nova política [DiagnosticData](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#diagnosticdata) para todas as outras políticas. Isso permitirá que os usuários gerenciem os dados de diagnóstico enviados para a Microsoft do Windows 7, 8, 8.1 e macOS.
  * Suporte ao DNS seguro (DNS em HTTPS).  A partir da versão 86 do Microsoft Edge, as configurações para controlar o DNS seguro em dispositivos não gerenciados estarão disponíveis. Essas configurações não podem ser acessadas por usuários em dispositivos gerenciados, mas os administradores de TI podem habilitar ou desabilitar o DNS seguro usando a política de grupo [dnsoverhttpsmode](https://docs.microsoft.com/deployedge/microsoft-edge-policies#dnsoverhttpsmode).

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

### Atualizações de política

#### Novas políticas

Vinte e três novas políticas foram adicionadas. Baixe os modelos administrativos atualizados da [página inicial do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise). As novas políticas a seguir foram adicionadas.

- [CollectionsServicesAndExportsBlockList](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#collectionsservicesandexportsblocklist) - Bloquear o acesso a uma lista especificada de serviços e exportar destinos em Coleções.
- [DefaultFileSystemReadGuardSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultfilesystemreadguardsetting) - Controlar o uso da API do sistema de arquivos para leitura.
- [DefaultFileSystemWriteGuardSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultfilesystemwriteguardsetting) - Controlar o uso da API do sistema de arquivos para gravação.
- [DefaultSensorsSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultsensorssetting) - configuração de sensores padrão.
- [DefaultSerialGuardSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultserialguardsetting) - Controlar o uso da API serial.
- [DiagnosticData](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#diagnosticdata) - Enviar dados de diagnóstico obrigatórios e opcionais referentes ao uso do navegador.
- [EnterpriseModeSiteListManagerAllowed](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#enterprisemodesitelistmanagerallowed) - Permitir o acesso à ferramenta Enterprise Mode Site List Manager.
- [FileSystemReadAskForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#filesystemreadaskforurls) - Permitir o acesso de leitura pela API do Sistema de arquivos nesses sites.
- [FileSystemReadBlockedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#filesystemreadblockedforurls) - Permitir o acesso de leitura pela API do Sistema de arquivos nesses sites.
- [FileSystemWriteAskForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#filesystemwriteaskforurls) - Permitir o acesso de gravação a arquivos e diretórios nestes sites.
- [FileSystemWriteBlockedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#filesystemwriteblockedforurls) - Bloquear o acesso de gravação a arquivos e diretórios nestes sites.
- [ForceSync](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#forcesync) - Forçar a sincronização dos dados do navegador e não mostrar o aviso de consentimento da sincronização.
- [InsecureFormsWarningsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#insecureformswarningsenabled) - Habilitar avisos para formulários inseguros.
- [InternetExplorerIntegrationTestingAllowed](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#internetexplorerintegrationtestingallowed) - Permitir teste no modo Internet Explorer.
- [SpotlightExperiencesAndRecommendationsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#spotlightexperiencesandrecommendationsenabled) - Escolher se os usuários podem receber imagens de plano de fundo personalizadas e texto, sugestões, notificações e dicas para os serviços Microsoft.
- [NewTabPageAllowedBackgroundTypes](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#newtabpageallowedbackgroundtypes) - Configurar os tipos de plano de fundo permitidos para o layout da página da nova guia.
- [SaveCookiesOnExit](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#savecookiesonexit) - Salvar os cookies ao fechar o Microsoft Edge.
- [SensorsAllowedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sensorsallowedforurls) - Permitir o acesso a sensores em sites específicos.
- [SensorsBlockedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sensorsblockedforurls) - Bloquear o acesso a sensores em sites específicos.
- [SerialAskForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#serialaskforurls) - Permitir a API serial em sites específicos.
- [SerialBlockedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#serialblockedforurls) - Bloquear a API serial em sites específicos.
- [UserAgentClientHintsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#useragentclienthintsenabled) - Habilitar o recurso de Dicas do Cliente Usuário-Agente.
- [UserDataSnapshotRetentionLimit](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#userdatasnapshotretentionlimit) - Limita o número de instantâneos de dados do usuário mantidos para uso no caso de uma reversão de emergência.

#### Políticas preteridas

- [MetricsReportingEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#metricsreportingenabled) - habilita o uso e os relatórios de dados relacionados a falhas.
- [SendSiteInfoToImproveServices](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sendsiteinfotoimproveservices) - envia informações do site para melhorar os serviços da Microsoft.

#### Política obsoleta

[TLS13HardeningForLocalAnchorsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#tls13hardeningforlocalanchorsenabled)- Habilita um recurso de segurança TLS 1,3 para âncoras de confiança locais.

<!-- end 86 -->
## Versão 85.0.564.70 : 6 de outubro

Correção de vários bugs e problemas de desempenho.

## Versão 85.0.564.68: 1 de outubro

Correção de vários bugs e problemas de desempenho.

## Versão 85.0.564.63: 23 de setembro

As atualizações de segurança estão listadas [aqui](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#september-23-2020)

## Versão 85.0.564.51: 9 de setembro

As atualizações de segurança estão listadas [aqui](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#september-9-2020)

## Versão 85.0.564.44: 31 de agosto

Correção de vários bugs e problemas de desempenho.
<!-- begin 85 -->
## Versão 85.0.564.41: 27 de agosto

As atualizações de segurança estão listadas [aqui](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#august-27-2020)

### Atualizações de recursos

- **Sincronização local de Favoritos e Configurações**. Agora, você pode sincronizar os favoritos do navegador e as configurações entre os perfis do Active Directory dentro de seu próprio ambiente sem a necessidade de sincronização na nuvem.

- **O suporte à Política de Grupo do Microsoft Edge para combinações de sites e aplicativos confiáveis para iniciar sem aviso de confirmação.**. Foi acrescentado o suporte à Política de Grupo que permite aos administradores adicionar combinações de sites e aplicativos confiáveis ​​para inicialização sem o aviso de confirmação. Isto adiciona capacidade aos administradores para configurar combinações de protocolo/origem confiáveis (como os aplicativos do Microsoft 365) para seus usuários finais suprimirem a solicitação de confirmação ao navegar para uma URL que contenha um protocolo de aplicativo.

- **Ferramenta Marca-texto para PDF**. Esta ferramenta pode ser facilmente adicionada à barra de ferramentas para realçar facilmente o texto importante no PDF.

- **A API de Acesso ao Armazenamento está disponível**. A API de Acesso ao Armazenamento permite acesso ao armazenamento primário em um contexto de terceiros quando um usuário tem providenciado uma intenção direta de permitir o armazenamento que de outra forma seria bloqueado pela configuração atual do navegador. Para saber mais, veja [API de Acesso de Armazenamento](https://www.chromestatus.com/feature/5612590694662144).

- **Enviar para o OneNote está disponível nas Coleções do Microsoft Edge**. Todos estão entusiasmados em poder enviar as informações que eles reunirão nas Coleções para o OneNote, onde podem acrescentá-las a um projeto maior e colaborar com outras pessoas! E ainda mais importante, no Microsoft Edge 85, você poderá enviar conteúdo para produtos do *Office para Mac* (Word, Excel e OneNote) tanto para a conta Microsoft como para o Azure Active Directory.

- **Atualizações do DevTools**. Para obter detalhes sobre as atualizações a seguir, confira [Novidades no DevTools (Microsoft Edge 85)](https://docs.microsoft.com/microsoft-edge/devtools-guide-chromium/whats-new/2020/06/devtools).

   - O DevTools do Microsoft Edge é compatível com a emulação Surface Duo. O DevTools do Microsoft Edge pode emular o Surface Duo para que você possa testar como o seu conteúdo da Web será visualizado em dispositivos com duas telas. Para ativar esse experimento no DevTools, entre no modo do dispositivo pressionando Ctrl + Shift + M no Windows ou Command + Shift + M no macOS e selecione Surface Duo na lista de seleção do dispositivo.
   - O DevTools do Microsoft Edge permite combinar atalhos de teclado com o Código VS. O DevTools do Microsoft Edge é compatível com a personalização de atalhos de teclado no DevTools para corresponder ao editor/IDE. No Microsoft Edge 85, estamos adicionando a capacidade para combinar os atalhos de teclado do DevTools para o VS Code. Essa alteração ajudará a aumentar a produtividade no Código VS e no DevTools.

### Atualizações de política

#### Novas políticas

Treze novas políticas foram adicionadas. Baixe os modelos administrativos atualizados da [página inicial do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise). As novas políticas a seguir foram adicionadas.

- [AutoLaunchProtocolsFromOrigins](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#autolaunchprotocolsfromorigins) - Definir uma lista de protocolos que podem lançar um aplicativo externo de origens listadas sem alertar o usuário.
- [ AutoOpenAllowedForURLsURLs](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#autoopenallowedforurls) - URLs nas quais o AutoOpenFileTypes pode aplicar.
- [AutoOpenFileTypes](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#autoopenfiletypes) - Lista de tipos de arquivo que devem ser abertos automaticamente no download.
- [DefaultSearchProviderContextMenuAccessAllowed](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultsearchprovidercontextmenuaccessallowed) - Permitir acesso à busca do menu de contexto do provedor de pesquisa padrão.
- [EnableSha1ForLocalAnchors](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#enablesha1forlocalanchors) - Permitir certificados assinados usando SHA-1 quando emitido por âncoras de confiança local.
- [ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#exemptdomainfiletypepairsfromfiletypedownloadwarnings) - Desabilitar o download de avisos baseados em extensão do tipo de arquivo para tipos de arquivo especificados em domínios.
- [IntensiveWakeUpThrottlingEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#intensivewakeupthrottlingenabled) - Controlar o recurso IntensiveWakeUpThrottling.
- [NewTabPagePrerenderEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#newtabpageprerenderenabled) - Habilitar o pré-carregamento da nova página da guia para renderização mais rápida.
- [NewTabPageSearchBox](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#newtabpagesearchbox) - Configurar a nova experiência da caixa de pesquisa da página da guia.
- [PasswordMonitorAllowed](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#passwordmonitorallowed) - Permitir que os usuários sejam alertados caso suas senhas não sejam seguras.
- [RoamingProfileSupportEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#roamingprofilesupportenabled) - Habilitar o uso de cópias de roaming para dados de perfil do Microsoft Edge.
- [RoamingProfileLocation](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#roamingprofilelocation) - Configurar o roaming do diretório de perfil.
- [TLSCipherSuiteDenyList](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#tlsciphersuitedenylist) - Especificar os pacotes de codificação TLS para desabilitar.

#### Políticas obsoletas

- [EnableDomainActionsDownload](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#enabledomainactionsdownload) Habilitar o Download de Ações de Domínio da Microsoft.
- [WebComponentsV0Enabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webcomponentsv0enabled) -reabilita a API de componentes Web V0 até M84.
- [WebDriverOverridesIncompatiblePolicies](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webdriveroverridesincompatiblepolicies) - Permitir ao WebDriver Substituir Políticas Incompatíveis.

<!--- END 85 ---->

## Versão 84.0.522.63: 20 de agosto

As atualizações de segurança estão listadas [aqui](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#august-20-2020).

## Versão 84.0.522.61: 17 de agosto

Correção de vários bugs e problemas de desempenho.

## Versão 84.0.522.59: 11 de agosto

As atualizações de segurança estão listadas [aqui](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#august-11-2020)

## Versão 84.0.522.58: 10 de agosto

Correção de vários bugs e problemas de desempenho.

## Versão 84.0.522.52: 1º de agosto

Correção de vários bugs e problemas de desempenho.

## Version 84.0.522.50: 31 de julho

Correção de vários bugs e problemas de desempenho.

## Versão 84.0.522.49: 29 de julho

As atualizações de segurança estão listadas [aqui](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#july-29-2020)

## Version 84.0.522.48: 28 de julho

Correção de vários bugs e problemas de desempenho.

## Version 84.0.522.44: 23 de julho

Correção de vários bugs e problemas de desempenho.

<!-- begin 84 -->
## Version 84.0.522.40: 16 de julho

As atualizações de segurança estão listadas [aqui](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#july-16-2020)

### Atualizações de recursos

- Esta versão do Microsoft Edge fornece uma melhoria na velocidade de download de lista de sites para o modo Internet Explorer. Reduzimos o atraso de download para a lista de sites no modo Internet Explorer para 0 segundo (de uma espera de 60 segundos) na ausência de uma lista de sites armazenados em cache. Também adicionamos suporte à política de grupo para casos em que as navegações de página inicial no modo Internet Explorer precisem ser adiadas até que a lista de sites seja baixada. Para obter mais informações, confira a política [DelayNavigationsForInitialSiteListDownload](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#delaynavigationsforinitialsitelistdownload).

- O Microsoft Edge agora permite que os usuários entrem no navegador quando ele é "executado como administrador" no Windows 10. Isso ajudará os clientes que usam o Microsoft Edge no Windows Server ou nos cenários de área de trabalho remota ou área restrita.

- O Microsoft Edge agora oferece suporte total ao mouse quando estiver no modo de tela inteira. Agora, você pode usar o mouse para acessar as guias, a barra de endereços e outros itens sem ter que sair do modo de tela inteira.

- Melhoria na compra online. Adicione apelidos personalizados para cartões de crédito ou débitos salvos. Agora, você pode distinguir e diferenciar os cartões de crédito ao fazer compras online. Dar apelidos aos cartões de crédito ou débito permite que você escolha o cartão correto ao usar o preenchimento automático para selecionar um método de pagamento.

- O TLS/1.0 e o TLS/1.1 estão desabilitados por padrão.  A política [SSLVersionMin](https://docs.microsoft.com/deployedge/microsoft-edge-policies#sslversionmin) permite reabilitar o TLS/1.0 e o TLS/1.1. Essa política permanecerá disponível pelo menos até a versão 88 do Microsoft Edge. Para saber mais, confira [Compatibilidade de sites - alterações que afetam o Microsoft Edge](https://docs.microsoft.com/microsoft-edge/web-platform/site-impacting-changes).

- Aperfeiçoamentos do recurso Coleções:

  - Uma funcionalidade de anotação foi adicionada, o que permite que você adicione uma anotação ou comentário a um item em uma coleção. As anotações são agrupadas e permanecem anexadas a um item, mesmo que você organize os itens em uma coleção. Para experimentar esse novo recurso, clique com o botão direito do mouse em um item e escolha "Adicionar anotação".
  - Você pode alterar a cor da tela de fundo das anotações em coleções. Você pode usar a codificação de cores para ajudá-lo a organizar informações e aumentar a produtividade.
  - Os aperfeiçoamentos de desempenho são notáveis, permitindo que você exporte suas coleções para o Excel em menos tempo do que em versões anteriores do Microsoft Edge.

- Suporte adicional à API do Microsoft Edge:

  - A API de acesso ao armazenamento está habilitada para fins de teste. Esse recurso está habilitado para usuários domésticos e usuários da empresa com a política [ExperimentationAndConfigurationServiceControl](https://docs.microsoft.com/deployedge/microsoft-edge-policies#experimentationandconfigurationservicecontrol) definida como "Total". Esse recurso será habilitado por padrão para todos os usuários no Microsoft Edge Stable versão 85.
  
    À medida que a privacidade está ficando cada vez mais importante para os usuários, as solicitações para padrões mais restritivos de navegador e configurações de aceitação de usuário, como bloqueio de todo o acesso de armazenamento de terceiros, são cada vez mais comuns. Embora essas configurações ajudem a melhorar a privacidade e bloquear o acesso indesejado de terceiros desconhecidos ou não confiáveis, eles podem ter efeitos colaterais indesejados, como bloquear o acesso a conteúdo que o usuário pode querer ver (por exemplo, mídia social e conteúdo de mídia inserida.)

    A API de Acesso ao Armazenamento permite acesso ao armazenamento primário em um contexto de terceiros quando um usuário tem providenciado uma intenção direta de permitir o armazenamento que de outra forma seria bloqueado pela configuração atual do navegador. Para saber mais, veja [API de Acesso de Armazenamento](https://www.chromestatus.com/feature/5612590694662144).

  - A API do Sistema de Arquivos Nativo, o que significa que você pode conceder permissões aos sites para editar arquivos ou pastas por meio da API do Sistema de Arquivos Nativo.

- Aperfeiçoamentos em PDF:

  - O recurso Ler em Voz Alta para PDF permite que os usuários ouçam o conteúdo em PDF enquanto realizam outras tarefas que podem ser importantes para eles. Ele também ajuda os alunos com estilo de aprendizagem auditivo-visual a se concentrarem em ler o conteúdo, facilitando o aprendizado.
  - Edição de arquivo PDF aperfeiçoada. Agora, você pode salvar uma edição feita em um PDF em vez de salvar uma cópia sempre que editar o PDF.

- O Microsoft Edge agora oferece a opção Tradução na Leitura Avançada. Quando um usuário abre o modo de exibição de Leitura Avançada, há agora a opção de traduzir a página para o idioma desejado.

- Várias atualizações do DevTools, incluindo o suporte à personalização de atalhos de teclado para corresponder ao VC Code e à visualização do DevTools em alto contraste.  Para obter mais detalhes, consulte [Novidades no DevTools (Microsoft Edge 84)](https://docs.microsoft.com/microsoft-edge/devtools-guide-chromium/whats-new/2020/05/devtools).

### Atualizações de política

#### Novas políticas

Sete novas políticas foram adicionadas. Baixe os modelos administrativos atualizados da [página inicial do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise). As novas políticas a seguir foram adicionadas.

- [AppCacheForceEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#appcacheforceenabled) - Permite reabilitar o recurso AppCache, mesmo que ele esteja desativado por padrão.
- [ApplicationGuardContainerProxy](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#applicationguardcontainerproxy)- Definir as configurações para o Proxy do Contêiner do Application Guard.
- [DelayNavigationsForInitialSiteListDownload](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#delaynavigationsforinitialsitelistdownload) - Exigir que a lista de sites no Modo Empresarial esteja disponível antes da navegação na guia.
- [WinHttpProxyResolverEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#winhttpproxyresolverenabled): Usar o solucionador de proxy do Windows.
- [InternetExplorerIntegrationEnhancedHangDetection](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#internetexplorerintegrationenhancedhangdetection)- Configurar detecção de suspensão avançada no modo Internet Explorer.
- [NativeWindowOcclusionEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#nativewindowocclusionenabled) - para reduzir o consumo de CPU e de energia, o Microsoft Edge detectará quando uma janela é coberta por outras janelas e suspenderá os pixels da pintura do trabalho.
- [NavigationDelayForInitialSiteListDownloadTimeout](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#navigationdelayforinitialsitelistdownloadtimeout) -Definir um tempo limite para o atraso da navegação da guia para a Lista de Sites no Modo Empresarial.

#### Políticas preteridas

- [AllowSyncXHRInPageDismissal](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#allowsyncxhrinpagedismissal) - Autorizar páginas a enviar solicitações de XHR síncronas durante a descarte da página.
- [BuiltinCertificateVerifierEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#builtincertificateverifierenabled) - Determina se o verificador de certificado interno será usado para verificar certificados do servidor.
- [StricterMixedContentTreatmentEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#strictermixedcontenttreatmentenabled)- Habilita um tratamento mais estrito para conteúdo misto.

#### Política obsoleta

[ForceNetworkInProcess](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#forcenetworkinprocess) - Forçar a execução do código de rede no processo do navegador.

<!-- End 84 -->
## Version 83.0.478.64: 13 de julho

Correção de vários bugs e problemas de desempenho.

## Version 83.0.478.61: 7 de julho

Correção de vários bugs e problemas de desempenho.

## Versão 83.0.478.58: 30 de junho

Correção de vários bugs e problemas de desempenho.

## Versão 83.0.478.56: 24 de junho

Correção de vários bugs e problemas de desempenho.

As atualizações de segurança estão listadas [aqui](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#june-24-2020)

## Versão 83.0.478.54: 17 de junho

As atualizações de segurança estão listadas [aqui](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#june-17-2020)

## Versão 83.0.478.50: 15 de junho

Correção de vários bugs e problemas de desempenho.

## Versão 83.0.478.45: 4 de junho

As atualizações de segurança estão listadas [aqui](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#june-4-2020)

## Versão 83.0.478.44: 1 de junho

Correção de vários bugs e problemas de desempenho.

## Versão 83.0.478.37: 21 de maio

As atualizações de segurança estão listadas [aqui](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#may-21-2020)

### Atualizações de recursos

- As atualizações do Microsoft Edge agora serão implantadas gradualmente. No futuro, as atualizações para o Microsoft Edge serão implantadas para os usuários em período de alguns dias. Isso nos permite proteger melhor as atualizações de bugs acidentais, o que melhora a experiência de atualização. Como usuário, você continuará a receber atualizações automáticas. Se a sua organização não estiver inscrita para as atualizações automáticas, você não serão afetados por essa alteração. Para saber mais, confira o artigo [Distribuições progressivas](microsoft-edge-update-progressive-rollout.md).
- Melhorias no Microsoft Defender SmartScreen: foram feitas várias melhorias no serviço Microsoft Defender SmartScreen, como proteção melhorada contra sites mal-intencionados que são redirecionados durante o carregamento e bloqueio de quadros de nível superior que substitui completamente sites mal-intencionados pela página de segurança do Microsoft Defender SmartScreen. O bloqueio de quadros de nível superior impede a reprodução de áudio e outras mídias do site mal-intencionado, o que proporciona uma experiência mais fácil e menos confusa.

- Em resposta a comentários dos usuários, os usuários agora podem impedir a limpeza de determinados cookies automaticamente quando o navegador é fechado. Essa opção será útil se houver um site do qual os usuários não queiram ser desconectados, mas ainda querem que todos os outros cookies sejam removidos quando o navegador fechar. Para usar esse recurso, acesse *edge://settings/clearBrowsingDataOnClose* e ative a opção "Cookies e outros dados do site".

- A Troca Automática de Perfis agora está disponível para ajudar você a acessar seu conteúdo de trabalho com mais facilidade em diferentes perfis. Se você usar vários perfis no trabalho, poderá verificar esse recurso navegando para um site que exija autenticação da sua conta corporativa ou de estudante enquanto estiver no seu perfil pessoal. Quando detectarmos isso, você receberá uma solicitação para mudar para o seu perfil de trabalho para acessar o site sem precisar se autenticar. Quando você escolhe o perfil de trabalho para o qual deseja mudar, o site simplesmente abre no seu perfil de trabalho. Esse recurso de mudança de perfil ajuda você a manter seus dados pessoais e de trabalho separados e a acessar seu conteúdo de trabalho com mais facilidade. Se você não quiser que o recurso solicite a troca de perfis, você pode escolher a opção não me pergunte novamente isso ficará fora do seu caminho.

- Aperfeiçoamentos de recursos de coleções:
  - Você pode usar o recurso de arrastar e soltar para adicionar um item a uma coleção sem abrir a coleção. Ao arrastar e soltar, você também pode escolher um local na lista de coleções onde deseja colocar o item.
  - Você pode adicionar vários itens a uma coleção em vez de adicionar um item por vez. Para adicionar vários itens, selecione-os e, em seguida, arraste-os para uma coleção. Ou você pode selecionar os itens, clicar com o botão direito do mouse e escolher a coleção onde deseja colocar os itens.

- Você pode adicionar todas as guias em uma janela do Microsoft Edge a uma nova coleção sem adicioná-las individualmente. Para fazer isso, clique com o botão direito do mouse em qualquer guia e escolha "Adicionar todas as guias a uma nova coleção".

- A sincronização de extensão já está disponível. Agora você pode sincronizar suas extensões entre todos os seus dispositivos! As extensões da Microsoft Store e da Chrome Web Store serão sincronizadas com o Microsoft Edge. Para usar esse recurso: Clique nas reticências (**…**) na barra de menus, selecione **Configurações**. Em Seu perfil, clique em **Sincronização** para ver as opções de sincronização. Em **Perfis/Sincronização**, use a alternância para ativar as Extensões. Você pode usar a política de grupo [SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled) para desativar a sincronização de extensões.

- Foi melhorada a mensagem na página de gerenciamento de downloads para downloads não seguros que foram bloqueados.

- Melhorias da Leitura Avançada:
  - Adicionado suporte para Advérbios na experiência Classe Gramatical que temos na Leitura Avançada. Ao ler um artigo na Leitura Avançada, abra as Ferramentas de Gramática e ative Advérbios em Classe Gramatical para destacar todos os advérbios na página.
  - Foi adicionada a capacidade de selecionar qualquer conteúdo em uma página da Web e abri-lo na Leitura Avançada. Essa capacidade permite que os usuários usem a Leitura Avançada e todas as Ferramentas de Aprendizagem, como Foco de Linha e Leitura em Voz Alta, em todos os sites.

- O link Doctor fornece a correção de host e uma consulta de pesquisa aos usuários quando eles digitam incorretamente uma URL. Por exemplo: <br>
Um usuário digita incorretamente "powerbi como" powerbbi". com. O link Doctor vai sugerir "powerbi". com como uma correção e criar um link para pesquisar por "powerbbi" caso o usuário esteja procurando algo diferente.

- Permita que os usuários salvem a decisão para iniciar um protocolo externo para um site específico. Os usuários podem configurar a política [ExternalProtocolDialogShowAlwaysOpenCheckbox]( https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#externalprotocoldialogshowalwaysopencheckbox) para habilitar ou desabilitar esse recurso.

- Os usuários podem definir o Microsoft Edge como navegador padrão diretamente no Microsoft Edge **Configurações**. Isso permite aos usuários alterarem seu navegador padrão, dentro do contexto do próprio navegador, em vez de precisar pesquisar as configurações do sistema operacional. Para usar esse recurso, vá para *edge://settings/defaultBrowser* e clique em **tornar padrão**.

- Várias atualizações do DevTools, incluindo o suporte à depuração remota, aperfeiçoamentos na IU e muito mais. Para obter mais detalhes, consulte [Novidades no DevTools (Microsoft Edge 83)](https://docs.microsoft.com/microsoft-edge/devtools-guide-chromium/whats-new/2020/03/devtools).

- O cenário de aviso MCAS (Segurança de Acesso à Microsoft Cloud) agora está disponível. Isso permite que administradores configurem o Warn, uma nova categoria de bloqueio MCAS, onde o usuário pode substituir uma página de bloqueio do MCAS. Os bloqueios do MDATP E5 são nativamente integrados aos bloqueios SmartScreen no Microsoft Edge para obter uma experiência perfeita. Essa experiência permite um bloco vermelho de página inteira com a mensagem "este site é bloqueado pela sua organização", em vez de apenas uma notificação do sistema.

- Não permitir um XMLHttpRequest síncrono no descarte de página. O envio de XMLHttpRequests síncronos durante o carregamento de uma página da Web será removido. Essa alteração melhorará o desempenho e a confiabilidade do navegador, mas poderá afetar os aplicativos da Web que ainda não foram atualizados para usar APIs da Web mais modernas, incluindo sendBeacon e FETCH. A Política de Grupo para desabilitar essa alteração e permitir XHR síncronos durante a transmissão de página estará disponível até o Microsoft Edge 88. Para saber mais, confira [Compatibilidade de sites - alterações que afetam o Microsoft Edge](https://docs.microsoft.com/microsoft-edge/web-platform/site-impacting-changes).

### Atualizações de política

#### Novas políticas

15 novas políticas foram adicionadas. Baixe os modelos administrativos atualizados da [página inicial do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise). As novas políticas a seguir foram adicionadas.

- [AllowSurfGame](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#allowsurfgame) - Permitir jogo de surf.
- [AllowTokenBindingForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#allowtokenbindingforurls) - Configurar a lista de sites com os quais o Microsoft Edge tentará estabelecer uma Associação de Token.
- [BingAdsSuppression](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#bingadssuppression) - Bloquear todos os anúncios nos resultados de pesquisa do Bing.
- [BuiltinCertificateVerifierEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#builtincertificateverifierenabled) - Determina se o verificador de certificado interno será usado para verificar certificados do servidor.
- [ClearCachedImagesAndFilesOnExit](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#clearcachedimagesandfilesonexit) - Limpar imagens e arquivos em cache quando o Microsoft Edge é fechado.
- [ConfigureShare](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#configureshare) - Configurar a experiência de Compartilhamento.
- [DeleteDataOnMigration](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#deletedataonmigration) - Excluir dados antigos do navegador na migração.
- [DnsOverHttpsMode](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#dnsoverhttpsmode) - Controlar o modo de DNS sobre HTTPS.
- [DnsOverHttpsTemplates](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#dnsoverhttpstemplates) - Especificar o modelo de URI do resolvedor de DNS sobre HTTPS desejado.
- [FamilySafetySettingsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#familysafetysettingsenabled) - Permitir que os usuários configurem a Proteção para a família.
- [LocalProvidersEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#localprovidersenabled) - Permitir sugestões de provedores locais.
- [ScrollToTextFragmentEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#scrolltotextfragmentenabled) - Ativar a rolagem para o texto especificado nos fragmentos de URL.
- [ScreenCaptureAllowed](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#screencaptureallowed) - Permitir ou negar a captura de tela.
- [SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled) - Configurar a lista de tipos excluídos da sincronização.
- [NativeWindowOcclusionEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#nativewindowocclusionenabled) - Ative a ocultação do Windows Nativo.

#### Política preterida

A política a seguir continuará funcionando nesta versão. Ela se tornará "obsoleta" em uma versão futura.

[EnableDomainActionsDownload](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#enabledomainactionsdownload) Habilitar o Download de Ações de Domínio da Microsoft

<!-- end 83 -->

## Versão 81.0.416.77: 18 de maio

Correção de vários bugs e problemas de desempenho.

## Versão 81.0.416.72: 7 de maio

As atualizações de segurança estão listadas [aqui](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#may-7-2020)

## Versão 81.0.416.68: 29 de abril

As atualizações de segurança estão listadas [aqui](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#april-29-2020)

## Versão 81.0.416.64: 23 de abril

As atualizações de segurança estão listadas [aqui](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#april-23-2020)

## Versão 81.0.416.58: 17 de abril

As atualizações de segurança estão listadas [aqui](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#april-17-2020)

## Versão 81.0.416.53: 13 de abril

As atualizações de segurança estão listadas [aqui](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#april-13-2020)

### Atualizações de recursos

- Adicionado suporte à Proteção de Informações do Windows (WIP), que ajuda as empresas a proteger dados confidenciais contra divulgação não autorizada. [Saiba mais](https://docs.microsoft.com/deployedge/microsoft-edge-security-windows-information-protection).

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

### Atualizações de política

#### Novas políticas

Foram adicionadas 11 novas políticas. Baixe os modelos administrativos atualizados da [página inicial do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise). As novas políticas a seguir foram adicionadas.

- [AmbientAuthenticationInPrivateModesEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#ambientauthenticationinprivatemodesenabled)- Habilite a autenticação ambiente para perfis InPrivate e Guest. 
- [AudioSandboxEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#audiosandboxenabled)- Permite que a caixa de proteção de áudio seja executada.
- [ForceLegacyDefaultReferrerPolicy](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#forcelegacydefaultreferrerpolicy): Usa uma política referencial padrão de no-referrer-when-downgrade.
- [GloballyScopeHTTPAuthCacheEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#globallyscopehttpauthcacheenabled)- Habilita o cache de autenticação HTTP globalmente.
- [ImportExtensions](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#importextensions)- Permite a importação de extensões.
- [ImportCookies](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#importcookies)- Permite a importação de cookies.
- [ImportShortcuts](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#importshortcuts)- Permite a importação de atalhos.
- [InternetExplorerIntegrationSiteRedirect](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#internetexplorerintegrationsiteredirect)Especifica como as navegações "na página" para sites não configurados se comportam quando iniciadas nas páginas do modo Internet Explorer.
- [StricterMixedContentTreatmentEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#strictermixedcontenttreatmentenabled)- Habilita um tratamento mais estrito para conteúdo misto.
- [TLS13HardeningForLocalAnchorsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#tls13hardeningforlocalanchorsenabled)- Habilita um recurso de segurança TLS 1,3 para âncoras de confiança locais.
- [ConfigureOnPremisesAccountAutoSignIn](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#configureonpremisesaccountautosignin)- Configura o login automático com uma conta de domínio do Active Directory quando não houver nenhuma conta de domínio do Azure AD.

#### Alterações de nome e legenda da política

A política `OmniboxMSBProviderEnabled` é alterada para [AddressBarMicrosoftSearchInBingProviderEnabled](https://docs.microsoft.com//DeployEdge/microsoft-edge-policies#addressbarmicrosoftsearchinbingproviderenabled) - A legenda da política é "Habilitar a pesquisa da Microsoft nas sugestões do Bing na barra de endereço".

#### Políticas preteridas

As seguintes políticas continuam a funcionar nesta versão. Elas se tornarão "obsoletas" em uma versão futura.

- [WebComponentsV0Enabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webcomponentsv0enabled) - Reabilita a API de componentes Web V0 até M84.
- [WebDriverOverridesIncompatiblePolicies](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webdriveroverridesincompatiblepolicies)- Permite que o WebDriver substitua incompatível.

#### Problemas resolvidos

- Foi corrigido um problema em que o modo IE no Microsoft Edge fazia com que uma caixa de diálogo de download em andamento fosse exibida mesmo após o download do arquivo.
- Foi corrigido um problema em que o Microsoft Edge estava descartando cookies de sessão quando uma página que já estava no modo IE era acionada para abrir uma nova guia do modo IE.

## Versão 80.0.361.111: 7 de abril

Correção de vários bugs e problemas de desempenho.

## Versão 80.0.361.109: 1º de abril

As atualizações de segurança estão listadas [aqui](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#april-1-2020)

## Versão 80.0.361.69: 19 de março

As atualizações de segurança estão listadas [aqui](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#march-19-2020)

## Versão 80.0.361.66: 4 de março

As atualizações de segurança estão listadas [aqui](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#march-4-2020)

## Versão 80.0.361.62: 25 de fevereiro

As atualizações de segurança estão listadas [aqui](https://docs.microsoft.com/deployedge/microsoft-edge-relnotes-security#february-25-2020)

## Versão 80.0.361.57: 20 de fevereiro

As atualizações de segurança estão listadas [aqui](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#february-20-2020)

## Versão 80.0.361.56: 19 de fevereiro

Correção de vários bugs e problemas de desempenho.

## Versão 80.0.361.54: 14 de fevereiro

### Problemas resolvidos

- Foi corrigido um problema em que senha, pagamento e cookies não são importados no Microsoft Edge.

## Versão 80.0.361.50: 11 de fevereiro

Correção de vários bugs e problemas de desempenho.

## Versão 80.0.361.48: 07 de fevereiro

As atualizações de segurança estão listadas [aqui](https://docs.microsoft.com/deployedge/microsoft-edge-relnotes-security#february-7-2020)

### Atualizações de recursos

- Proteção do SmartScreen adicionada para baixar aplicativos potencialmente indesejados. [Saiba mais](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-antivirus/detect-block-potentially-unwanted-apps-windows-defender-antivirus)
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

### Atualizações de política

#### Novas políticas

16 novas políticas foram adicionadas. Baixe os modelos administrativos atualizados da [página inicial do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise). As novas políticas a seguir foram adicionadas.

- [AlternateErrorPagesEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#alternateerrorpagesenabled) -sugere páginas semelhantes quando uma página da Web não puder ser encontrada.
- [DefaultInsecureContentSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultinsecurecontentsetting) -controla o uso de exceções de conteúdo inseguro.
- [DNSInterceptionChecksEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#dnsinterceptionchecksenabled) -verificações de interceptação de DNS habilitadas.
- [HideFirstRunExperience](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#hidefirstrunexperience) -oculta a experiência de primeira execução e a tela inicial.
- [InsecureContentAllowedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#insecurecontentallowedforurls) -permitir conteúdo não seguro em sites especificados.
- [InsecureContentBlockedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#insecurecontentblockedforurls) -bloqueia conteúdo não seguro em sites especificados.
- [LegacySameSiteCookieBehaviorEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#legacysamesitecookiebehaviorenabled) -habilita a configuração padrão de cookie herdado SameSite padrão.
- [LegacySameSiteCookieBehaviorEnabledForDomainList](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#legacysamesitecookiebehaviorenabledfordomainlist) -reverte para comportamento SameSite herdado de cookies em sites especificados.
- [PaymentMethodQueryEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#paymentmethodqueryenabled) -permite que os sites consultem os métodos de pagamento disponíveis.
- [PersonalizationReportingEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#personalizationreportingenabled) – permite a personalização de anúncios, pesquisas e notícias enviando o histórico de navegação à Microsoft.
- [PinningWizardAllowed](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#pinningwizardallowed) -permite que o assistente seja fixado na barra de tarefas.
- [SmartScreenPuaEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#smartscreenpuaenabled) -configura o Microsoft Defender SmartScreen para bloquear aplicativos potencialmente indesejados.
- [TotalMemoryLimitMb](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#totalmemorylimitmb) -define o limite em megabytes de memória que uma única instância do Microsoft Edge pode usar.
- [WebAppInstallForceList](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webappinstallforcelist) -configura a lista de aplicativos Web instalados pela força.
- [WebComponentsV0Enabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webcomponentsv0enabled) -reabilita a API de componentes Web V0 até M84.
- [WebRtcLocalIpsAllowedUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webrtclocalipsallowedurls) -gerencia a exposição de endereços IP locais por WebRTC.

#### Políticas preteridas

A política a seguir foi substituída.

- [NewTabPageCompanyLogo](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#newtabpagecompanylogo) -define o logotipo da empresa da nova guia.

### Problemas resolvidos

- Corrigido um problema em que o áudio não estava funcionando no ambiente Citrix.
- Foi corrigido um problema em que o Microsoft Edge e a experiência lado a lado do Microsoft Edge resulta em links e erros herdados.

## Consulte também

- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
