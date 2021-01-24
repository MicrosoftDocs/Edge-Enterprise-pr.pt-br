---
title: Notas de versão do Microsoft Edge para Stable Channel
ms.author: aguta
author: dan-wesley
manager: srugh
ms.date: 01/22/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Notas de versão do Microsoft Edge para Stable Channel
ms.openlocfilehash: b7a875c7a3688d1839be9c3fdc835f77e14f3bae
ms.sourcegitcommit: f0f250190fc09964175778338a177f1240946b98
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/22/2021
ms.locfileid: "11297185"
---
# Notas de versão do Microsoft Edge Stable Channel

Essas notas de versão fornecem informações dos novos recursos e atualizações não relacionados à segurança que estão inclusos Microsoft Edge Stable Channel.

- Todas as atualizações de segurança estão listadas [aqui](microsoft-edge-relnotes-security.md).
- As notas de versão arquivadas do Canal Estável do Microsoft Edge estão localizadas [aqui](microsoft-edge-relnote-archive-stable-channel.md).

 Para entender os canais do Microsoft Edge, confira a [Visão geral dos canais do Microsoft Edge](microsoft-edge-channels.md).

> [!NOTE]
> Para o Canal Estável, as atualizações serão implantadas progressivamente por um ou mais dias. Para saber mais, confira [Distribuições progressivas para as atualizações do Microsoft Edge](microsoft-edge-update-progressive-rollout.md).

## Versão 88.0.705.50: 21 de janeiro

As atualizações de segurança estão listadas [aqui](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#january-21-2021).

<!--- begin major 88  --->
### Atualizações de recursos

- **Preteridos:**

  - Preterir o suporte para o protocolo FTP. O suporte para o protocolo de FTP herdado foi removido do Microsoft Edge. Tentar navegar para um link de FTP fará com que o navegador direcione o sistema operacional para abrir um aplicativo externo para manipular o link de FTP. Como alternativa, os administradores de TI podem configurar o Microsoft Edge para usar o modo IE para sites que dependem do protocolo FTP.
  - O suporte ao Adobe Flash será removido. A partir do Microsoft Edge beta versão 88, a funcionalidade e o suporte do Adobe Flash serão removidos. Saiba mais: [Atualização no fim do suporte do Adobe Flash Player - blog do Microsoft Edge (Windows.com)](https://blogs.windows.com/msedgedev/2020/09/04/update-adobe-flash-end-support/)

- **Autenticação:**

  - O SSO (SSO) já está disponível para contas do Azure Active Directory (Azure AD) e conta da Microsoft (MSA) no Windows de nível inferior. Um usuário conectado no Microsoft Edge no nível inferior do Microsoft Windows (7, 8.1) agora será automaticamente conectado aos sites que estiverem configurados para permitir logon único com contas Work e Microsoft (por exemplo, bing.com, office.com, msn.com, outlook.com).<br>Observação: um usuário pode ter que sair e entrar novamente se ele se conectar ao Microsoft Edge em uma versão anterior ao Microsoft Edge 88 para aproveitar esse recurso.

- **Opção de modo de quiosque para encerrar a sessão**. O botão "Encerrar sessão" agora está disponível em uma experiência de navegação pública do modo de quiosque. Esse recurso garante que os dados e as configurações do navegador sejam excluídos quando o Microsoft Edge estiver fechado. Saiba mais sobre os recursos do modo de quiosque e o roteiro, [Configurar o modo de quiosque do Microsoft Edge](https://docs.microsoft.com/deployedge/microsoft-edge-configure-kiosk-mode).

- **Segurança e privacidade:**

  - Alertas são gerados se a senha de um usuário for encontrada em um vazamento online. As senhas do usuário são verificadas em um repositório de credenciais violadas e envia ao usuário um alerta se uma correspondência for encontrada. Para garantir a segurança e a privacidade, as senhas dos usuários são criptografadas e criptografadas quando são verificadas no banco de dados de credenciais vazadas.
  - Atualizar conteúdo misto automaticamente. As páginas seguras fornecidas por HTTPS podem conter imagens de referência que são servidas por HTTP não seguro. Para melhorar a privacidade e a segurança no Microsoft Edge 88, essas imagens serão recuperadas por HTTPS. Se a imagem não estiver disponível em HTTPS, ela não será carregada.
  - Exiba as permissões do site por site e por atividades recentes. Começando com o Microsoft Edge 88, os usuários poderão gerenciar permissões do site com mais facilidade. Elas poderão exibir permissões por site da Web, em vez do tipo de permissão apenas. Além disso, adicionamos uma seção de atividade recente que mostrará a um usuário todas as alterações recentes nas permissões do site.
  - Controles avançados para os cookies do navegador. A partir do Microsoft Edge 88, os usuários podem excluir cookies de terceiros sem afetar os cookies dos primeiros participantes. Os usuários também poderão filtrar os cookies por nome ou terceiro e classificar por nome, número de cookies e a quantidade de dados armazenados e modificados pela última vez.

- **Senhas:**

  - Gerador de senhas. O Microsoft Edge oferece um gerador de senhas fortes integrado que você pode usar ao se inscrever em uma nova conta ou ao alterar uma senha existente. Basta procurar a lista suspensa de senha sugerida pelo navegador no campo de senha e, quando selecionada, ela será salva automaticamente no navegador e será sincronizada entre os dispositivos para facilitar o uso futuro.
  - Monitor de Senhas. Quando qualquer uma das suas senhas salvas no navegador corresponder às que foram vistas na lista de credenciais vazadas, o Microsoft Edge o notificará e solicitará que atualize sua senha. O Monitor de Senhas verifica se há combinações em seu nome e está ativado por padrão.
  - Editar Senha. Agora você pode editar suas senhas salvas diretamente nas Configurações do Microsoft Edge. Sempre que uma senha for atualizada fora do Microsoft Edge, é fácil substituir a senha antiga salva pela nova editando a entrada salva em Configurações. 

- **Desempenho:**

  - Melhorar o desempenho do navegador com guias em suspensão. As guias em suspensão aprimoram o desempenho do navegador colocando as guias inativas em suspensão para liberar recursos do sistema, como memória e CPU, para que as guias ativas ou outros aplicativos possam usá-las. Os usuários podem impedir que os sites entrem em suspensão e configurem o período de tempo antes de uma Tabulação inativa entrar em suspensão. Para manter os usuários em fluxo, há também heurística para impedir que determinados sites entrem em suspensão, como sites de intranet. Este recurso é limitado a um grupo selecionado aleatoriamente de usuários que ativaram a experimentação. Estamos planejando ter o recurso de guias de suspensão habilitado por padrão no Microsoft Edge versão 89. Esse recurso pode ser gerenciado com políticas de grupo.
  - Melhorar a velocidade de inicialização do Microsoft Edge com o aumento de inicialização. Para melhorar a velocidade de inicialização do Microsoft Edge, desenvolvemos um recurso chamado aumento de inicialização. O aumento da inicialização abre o Microsoft Edge mais rapidamente, permitindo que o Microsoft Edge seja executado em segundo plano. Observação: esse recurso está limitado a um grupo de usuários selecionado aleatoriamente que habilitou o experimento. Esses usuários estão fazendo comentários para a equipe de recursos.

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

### Atualizações de política

#### Novas políticas

Foram adicionadas dezoito novas políticas. Baixe os modelos administrativos atualizados da [página inicial do Microsoft Edge Enterprise](https://www.microsoft.com/edge/business/download). As novas políticas a seguir foram adicionadas.

- [BasicAuthOverHttpEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#basicauthoverhttpenabled) - permitir autenticação básica para HTTP.
- [BlockExternalExtensions](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#blockexternalextensions) - bloqueia a instalação de extensões externas.
- [InternetExplorerIntegrationLocalFileAllowed](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#internetexplorerintegrationlocalfileallowed) - permite a inicialização de arquivos locais no modo Internet Explorer.
- [InternetExplorerIntegrationLocalFileExtensionAllowList](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#internetexplorerintegrationlocalfileextensionallowlist) - abre arquivos locais na lista de permissões de extensão de arquivo do modo Internet Explorer.
- [InternetExplorerIntegrationLocalFileShowContextMenu](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#internetexplorerintegrationlocalfileshowcontextmenu) - exibe o menu de contexto para abrir um link no modo do Internet Explorer.
- [IntranetRedirectBehavior](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#intranetredirectbehavior) - comportamento de redirecionamento da intranet.
- [PrinterTypeDenyList](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#printertypedenylist) - desativa tipos de impressora na lista de negações.
- [ShowMicrosoftRewards](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#showmicrosoftrewards) - exibe experiências de recompensas da Microsoft.
- [SleepingTabsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sleepingtabsenabled) - configura Guias em suspensão.
- [SleepingTabsTimeout](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sleepingtabstimeout) - define o tempo limite de inatividade da guia plano de fundo para Guias em suspensão.
- [SleepingTabsBlockedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sleepingtabsblockedforurls) - bloqueia Guias em suspensão em sites específicos.
- [StartupBoostEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#startupboostenabled) - habilita o aumento de inicialização.
- [TargetBlankImpliesNoOpener](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#targetblankimpliesnoopener) - não defina window.opener para links targeting _blank.
- [UpdatePolicyOverride](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#updatepolicyoverride) - especifica como o Microsoft Edge Update manipula as atualizações disponíveis do Microsoft Edge.
- [VerticalTabsAllowed](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#verticaltabsallowed) - configura a disponibilidade de um layout vertical para guias na lateral do navegador.
- [WebRtcAllowLegacyTLSProtocols](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webrtcallowlegacytlsprotocols) - permite downgrade de TLS/DTLS herdado no WebRTC.
- [WebWidgetAllowed](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webwidgetallowed) - habilita o widget Web.
- [WebWidgetIsEnabledOnStartup](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webwidgetisenabledonstartup) - permite o widget da Web na inicialização do Windows.

#### Políticas preteridas

- [ProactiveAuthEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proactiveauthenabled) - habilita a autenticação pró-ativa.
- [ProxyBypassList](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxybypasslist) - configura regras de bypass de proxy.
- [Proxymode](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxymode) - define configurações de servidor proxy.
- [ProxyPacUrl](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxypacurl) - define a URL do arquivo proxy.pac.
- [ProxyServer](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxyserver) - configura o endereço ou URL do servidor proxy.
- [WebDriverOverridesIncompatiblePolicies](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webdriveroverridesincompatiblepolicies) - permite que o WebDriver substitua políticas incompatíveis.

### Políticas Obsoletas

- [AllowPopupsDuringPageUnload](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#allowpopupsduringpageunload) - permite que uma página mostre pop-ups durante seu descarregamento.
- [DefaultPluginsSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultpluginssetting) - configuração padrão do Adobe Flash.
- [PluginsAllowedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#pluginsallowedforurls) - permite o plug-in do Adobe Flash em sites específicos.
- [PluginsBlockedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#pluginsblockedforurls) - bloqueia o plug-in do Adobe Flash em sites específicos.
- [RunAllFlashInAllowMode](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#runallflashinallowmode) - estende a configuração do Adobe Flash Content para todo o conteúdo.
<!--- end major 88  --->
## Versão 87.0.664.75: 7 de janeiro

As atualizações de segurança estão listadas [aqui](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#january-7-2021).

## Versão 87.0.664.66: 17 de dezembro

Correção de vários bugs e problemas de desempenho.

## Versão 87.0.664.60: 10 de dezembro

Correção de vários bugs e problemas de desempenho.

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

<!-- 85.0.564.41: August 27 -->
<!-- Archived to version 84.0.522.40: July 16 -->

## Ver também

- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
