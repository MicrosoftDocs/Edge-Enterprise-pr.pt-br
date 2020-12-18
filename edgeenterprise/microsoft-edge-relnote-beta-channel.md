---
title: Notas da versão do Microsoft Edge para canal beta
ms.author: aguta
author: dan-wesley
manager: srugh
ms.date: 12/16/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Notas da versão do Microsoft Edge para canal beta
ms.openlocfilehash: ee992fad6effe1f10b72c34f3073915a22e13ccd
ms.sourcegitcommit: 124e8bc890c80ffd68e25b4acc3815ef2dda699e
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11229685"
---
# Notas de versão do canal do Microsoft Edge beta

Estas notas de versão fornecem informações sobre os novos recursos e atualizações não relacionadas à segurança que estão inclusos no canal Beta do Microsoft Edge.

<!-- begin major 88 -->
## Versão 88.0.705.18: 9 de dezembro

### Atualizações de recursos

- **Preteridos:**

  - Preterir o suporte para o protocolo FTP. O suporte para o protocolo de FTP herdado foi removido do Microsoft Edge. Tentar navegar para um link de FTP fará com que o navegador direcione o sistema operacional para abrir um aplicativo externo para manipular o link de FTP. Como alternativa, os administradores de TI podem configurar o Microsoft Edge para usar o modo IE para sites que dependem do protocolo FTP.
  - O suporte ao Adobe Flash será removido. A partir do Microsoft Edge beta versão 88, a funcionalidade e o suporte do Adobe Flash serão removidos. Saiba mais: [Atualização no fim do suporte do Adobe Flash Player - blog do Microsoft Edge (Windows.com)](https://blogs.windows.com/msedgedev/2020/09/04/update-adobe-flash-end-support/)

- **Autenticação:**

  - O logon único (SSO) agora está disponível para contas do Azure Active Directory (Azure AD) e para a conta Microsoft (MSA) em Windows MacOS e de nível inferior. Um usuário conectado no Microsoft Edge no Windows Microsoft MacOS ou no nível inferior do Microsoft Windows (7, 8.1) agora será automaticamente conectado aos sites que estiverem configurados para permitir logon único com contas Work e Microsoft (por exemplo, bing.com, office.com, msn.com, outlook.com).<br>Observação: um usuário pode ter que sair e entrar novamente se ele se conectar ao Microsoft Edge em uma versão anterior ao Microsoft Edge 88 para aproveitar esse recurso.
  - Alternar automaticamente os usuários do MacOS para o perfil de trabalho dos sites que se autenticam com a conta corporativa. A partir da versão 88 do Microsoft Edge, oferecemos a capacidade de alternar os sites que se autenticam com o perfil de trabalho do usuário no MacOS.<br>Observação: um usuário pode ter que sair e entrar novamente se ele se conectar ao Microsoft Edge em uma versão anterior ao Microsoft Edge 88 para aproveitar esse recurso.

- Opção do modo de quiosque para encerrar a sessão. O botão "Encerrar sessão" agora está disponível em uma experiência de navegação pública do modo de quiosque. Esse recurso garante que os dados e as configurações do navegador sejam excluídos quando o Microsoft Edge estiver fechado. Saiba mais sobre os recursos do modo de quiosque e o roteiro, [Configurar o modo de quiosque do Microsoft Edge](https://docs.microsoft.com/deployedge/microsoft-edge-configure-kiosk-mode).

- **Segurança e privacidade:**

  - Alertas são gerados se a senha de um usuário for encontrada em um vazamento online. As senhas do usuário são verificadas em um repositório de credenciais violadas e envia ao usuário um alerta se uma correspondência for encontrada. Para garantir a segurança e a privacidade, as senhas dos usuários são criptografadas e criptografadas quando são verificadas no banco de dados de credenciais vazadas.
  - Atualizar conteúdo misto automaticamente. As páginas seguras fornecidas por HTTPS podem conter imagens de referência que são servidas por HTTP não seguro. Para melhorar a privacidade e a segurança no Microsoft Edge 88, essas imagens serão recuperadas por HTTPS. Se a imagem não estiver disponível em HTTPS, ela não será carregada.
  - Exiba as permissões do site por site e por atividades recentes. Começando com o Microsoft Edge 88, os usuários poderão gerenciar permissões do site com mais facilidade. Elas poderão exibir permissões por site da Web, em vez do tipo de permissão apenas. Além disso, adicionamos uma seção de atividade recente que mostrará a um usuário todas as alterações recentes nas permissões do site.
  - Controles avançados para os cookies do navegador. A partir do Microsoft Edge 88, os usuários podem excluir cookies de terceiros sem afetar os cookies dos primeiros participantes. Os usuários também poderão filtrar os cookies por nome ou terceiro e classificar por nome, número de cookies e a quantidade de dados armazenados e modificados pela última vez.

- **Desempenho:**

  - Melhorar o desempenho do navegador com guias em suspensão. As guias em suspensão aprimoram o desempenho do navegador colocando as guias inativas em suspensão para liberar recursos do sistema, como memória e CPU, para que as guias ativas ou outros aplicativos possam usá-las. Os usuários podem impedir que os sites entrem em suspensão e configurem o período de tempo antes de uma Tabulação inativa entrar em suspensão. Para manter os usuários em fluxo, há também heurística para impedir que determinados sites entrem em suspensão, como sites de intranet. Este recurso é limitado a um grupo selecionado aleatoriamente de usuários que ativaram a experimentação. Estamos planejando ter o recurso de guias de suspensão habilitado por padrão no Microsoft Edge versão 89. Esse recurso pode ser gerenciado com políticas de grupo.
  - Melhorar a velocidade de inicialização do Microsoft Edge com o aumento de inicialização. Para melhorar a velocidade de inicialização do Microsoft Edge, desenvolvemos um recurso chamado aumento de inicialização. O aumento da inicialização abre o Microsoft Edge mais rapidamente, permitindo que o Microsoft Edge seja executado em segundo plano. Observação: esse recurso está limitado a um grupo de usuários selecionado aleatoriamente que habilitou o experimento. Esses usuários estão fazendo comentários para a equipe de recursos.

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

### Atualizações de política

#### Novas políticas

Dezesseis novas políticas foram adicionadas. Baixe os modelos administrativos atualizados da [página inicial do Microsoft Edge Enterprise](https://www.microsoft.com/edge/business/download). As novas políticas a seguir foram adicionadas.

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
- [UpdatePolicyOverride](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#updatepolicyoverride) - especifica como o Microsoft Edge Update manipula as atualizações disponíveis do Microsoft Edge.
- [VerticalTabsAllowed](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#verticaltabsallowed) - configura a disponibilidade de um layout vertical para guias na lateral do navegador.
- [WebRtcAllowLegacyTLSProtocols](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webrtcallowlegacytlsprotocols) - Permite fazer downgrade TLS/DTLS legado em WebRTC.

#### Políticas preteridas

As políticas a seguir estão preteridas.

- [ProactiveAuthEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proactiveauthenabled) – habilita a autenticação pró-ativa.
- [ProxyBypassList](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxybypasslist) - configura regras de bypass de proxy.
- [Proxymode](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxymode) - define configurações de servidor proxy.
- [ProxyPacUrl](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxypacurl) - define a URL do arquivo proxy.pac.
- [ProxyServer](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxyserver) - configura o endereço ou URL do servidor proxy.
- [WebDriverOverridesIncompatiblePolicies](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webdriveroverridesincompatiblepolicies) - permite que o WebDriver substitua políticas incompatíveis.

#### Políticas obsoletas

As políticas a seguir estão obsoletas.

- [DefaultPluginsSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultpluginssetting) - configuração padrão do Adobe Flash.
- [PluginsAllowedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#pluginsallowedforurls) - permite o plug-in do Adobe Flash em sites específicos.
- [PluginsBlockedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#pluginsblockedforurls) - bloqueia o plug-in do Adobe Flash em sites específicos.
- [RunAllFlashInAllowMode](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#runallflashinallowmode) - estende a configuração do Adobe Flash Content para todo o conteúdo.

<!-- end major 88 -->

## Versão 87.0.664.55: 3 de dezembro

Correção de vários bugs e problemas de desempenho. O novo recurso a seguir é compatível com esta versão.

- Alertas **são gerados se a senha de um usuário for encontrada em um vazamento online**. As senhas do usuário são verificadas em um repositório de credenciais violadas e envia ao usuário um alerta se uma correspondência for encontrada. Para garantir a segurança e a privacidade, as senhas dos usuários são criptografadas e criptografadas quando são verificadas no banco de dados de credenciais vazadas.

## Versão 87.0.664.52: 30 de novembro

Correção de vários bugs e problemas de desempenho.

## Versão 87.0.664.40: 18 de novembro

Correção de vários bugs e problemas de desempenho.

## Versão 87.0.664.36: 16 de novembro

Correção de vários bugs e problemas de desempenho.

## Versão 87.0.664.30: 9 de novembro

Correção de vários bugs e problemas de desempenho.

## Versão 87.0.664.24: 2 de novembro

Correção de vários bugs e problemas de desempenho.

## Versão 87.0.664.18: 26 de outubro

Correção de vários bugs e problemas de desempenho.

<!-- begin major 87 -->
## Versão 87.0.664.12: 20 de outubro

### Atualizações de recursos

- **Recursos de privacidade do modo de quiosque habilitados**. A partir do Microsoft Edge versão 87, os recursos do modo de quiosque que ajudarão as empresas em torno da privacidade dos dados do usuário serão habilitados. Esses recursos habilitarão experiências, como limpar os dados do usuário ao sair, excluir arquivos baixados e redefinir a experiência de iniciação configurada após uma quantidade específica de tempo ocioso. Saiba mais sobre como [Configurar as opções do modo de quiosque do Microsoft Edge](https://docs.microsoft.com/deployedge/microsoft-edge-configure-kiosk-mode)
- **Implantação de ClickOnce habilitada por padrão**. O ClickOnce está habilitado por padrão no Microsoft Edge 87, o que reduz as barreiras para a implantação de software e alinha-se melhor com o comportamento do navegador da Versão Prévia do Microsoft Edge. A partir do Microsoft Edge 87, o estado "Não Configurado" da política de ClickOnceEnabled refletirá o novo estado de ClickOnce padrão Habilitado (em comparação com o estado padrão anterior Desabilitado).
- **A página nova guia da empresa (NTP) integra a produtividade com o conteúdo do feed personalizado e relevante para o trabalho**. O NTP empresarial combina a página de produtividade do Office 365 oferecemos a todos os usuários que entraram com uma conta corporativa ou de estudante com feeds personalizados da empresa e da indústria relevantes para o trabalho que são organizados em uma única página. Os usuários poderão reconhecer o conteúdo familiar do Office 365 e da Pesquisa da Microsoft para Empresas, da plataforma Bing. Além disso, eles podem facilmente inverter para um "Meu Feed" personalizável com conteúdo e módulos relevantes para o usuário, para a empresa ou para a sua indústria, além de uma seleção de outros feeds disponibilizados pela organização. [Saiba mais](https://docs.microsoft.com/microsoft-365/admin/manage/manage-industry-news?view=o365-worldwide&preserve-view=true).

- **Segurança e privacidade:**

  - Suporte a Associação de Token TLS para sites de política configurada. A associação de Token TLS ajuda a evitar ataques de roubo de token para garantir que os cookies não possam ser reutilizados a partir de um dispositivo que não tenha sido definido inicialmente. O uso da ligação de token TLS exige a configuração da política [AllowTokenBindingForUrls](https://docs.microsoft.com/deployedge/microsoft-edge-policies#allowtokenbindingforurls) e exige que os sites listados ofereçam suporte a esse recurso.

- **Suporte a teclado para marca-texto em arquivos PDF**. Os usuários podem usar as teclas do teclado para realçar qualquer texto em um PDF.

- **Impressão:**

  - Escolha o lado a ser invertido ao imprimir nos dois lados. Os usuários podem optar por virar o lado maior ou o lado menor de uma planilha ao imprimir em ambos os lados.
  - Escolha o modo de rasterização de impressão para a empresa. Controlar como o Microsoft Edge é impresso em uma impressora não PostScript no Windows. Às vezes, os trabalhos de impressão em impressoras não PostScript precisam ser rasterizados para serem impressos corretamente. As opções de impressão são "Total" e "Rápida".

### Atualizações de política

#### Novas políticas

Dez novas políticas foram adicionadas. Baixe os modelos administrativos atualizados da [página inicial do Microsoft Edge Enterprise](https://www.microsoft.com/edge/business/download). As novas políticas a seguir foram adicionadas.

- [ConfigureFriendlyURLFormat](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#configurefriendlyurlformat) -configure o formato de colagem padrão das URLs copiadas do Microsoft Edge e determine se outros formatos estarão disponíveis para os usuários.
- [EdgeShoppingAssistantEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#edgeshoppingassistantenabled) -Compras Habilitadas no Microsoft Edge.
- [HideInternetExplorerRedirectUXForIncompatibleSitesEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#hideinternetexplorerredirectuxforincompatiblesitesenabled) – oculte o diálogo de redirecionamento único e a faixa no Microsoft Edge.
- [KioskAddressBarEditingEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#kioskaddressbareditingenabled) -configure a edição da barra de endereços para a experiência de navegação pública do modo de quiosque.
- [KioskDeleteDownloadsOnExit](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#kioskdeletedownloadsonexit) - exclua arquivos baixados como parte de uma sessão quiosque quando o Microsoft Edge é fechado.
- [PasswordRevealEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#passwordrevealenabled) -habilite o botão revelar Senha.
- [RedirectSitesFromInternetExplorerPreventBHOInstall](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#redirectsitesfrominternetexplorerpreventbhoinstall) – impede a instalação do BHO para redirecionar sites incompatíveis do Internet Explorer para o Microsoft Edge.
- [RedirectSitesFromInternetExplorerRedirectMode](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#redirectsitesfrominternetexplorerredirectmode) – redirecione sites incompatíveis do Internet Explorer para o Microsoft Edge.
- [SpeechRecognitionEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#speechrecognitionenabled) - Configurar Reconhecimento de Fala.
- [WebCaptureEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webcaptureenabled) -habilite o recurso de captura da Web no Microsoft Edge.

#### Política Preterida

[NewTabPageSetFeedType](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#newtabpagesetfeedtype) - configurar a nova experiência de página da guia Microsoft Edge.

#### Política obsoleta

[EnableDeprecatedWebPlatformFeatures](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#enabledeprecatedwebplatformfeatures) - reative os recursos da plataforma Web preteridos por um tempo limitado.

<!-- end major 87 -->

## Versão 86.0.622.43: 16 de outubro

Correção de vários bugs e problemas de desempenho.

## Versão 86.0.622.36: 7 de outubro

Correção de vários bugs e problemas de desempenho.

## Versão 86.0.622.31: 1 de outubro

Correção de vários bugs e problemas de desempenho.

## Versão 86.0.622.28: 28 de setembro

Correção de vários bugs e problemas de desempenho.

## Versão 86.0.622.15: 14 de setembro

Correção de vários bugs e problemas de desempenho.

## Versão 86.0.622.11: 9 de setembro

### Atualizações de recursos

* **Modo Internet Explorer:**

   * Permita que os usuários usem a interface do usuário (UI) do Microsoft Edge para testar sites no modo Internet Explorer. A partir da versão 86 do Microsoft Edge, os administradores poderão habilitar uma opção da interface do usuário para seus usuários para carregar uma guia no modo Internet Explorer para fins de teste ou como um stopgap até que os sites sejam adicionados ao XML da lista de sites.

* **Excluir downloads do disco usando o gerenciador de downloads.** Agora, os usuários podem excluir os arquivos baixados de seu disco, sem sair do navegador. A nova funcionalidade Excluir downloads existe no menu de contexto da prateleira de downloads ou da página de downloads.

* **Reverter para a versão anterior do Microsoft Edge.** O recurso reversão permite que os administradores voltem para uma versão boa conhecida do Microsoft Edge, caso haja algum problema na versão mais recente do Microsoft Edge.
[Saiba mais](edge-learnmore-rollback.md).

* **Forçar a habilitação da Sincronização por padrão em toda a empresa.**  Os administradores podem habilitar a sincronização das contas do Azure Active Directory (Azure AD) por padrão com a política de [ForceSync](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#forcesync).

* **Atualizações de PDF:**

  * Sumário para documentos em PDF. A partir da versão 86, o Microsoft Edge terá suporte ao sumário, o que permitirá que os usuários naveguem com facilidade por um documento em PDF.
  * Acesse todas as funcionalidades de PDF em telas pequenas de fator forma. Acesse todos os recursos do leitor de PDF do Microsoft Edge em dispositivos com telas pequenas.
  * Suporte à caneta digital para marca-texto em arquivos PDF. Com essa atualização, os usuários podem usar a caneta digital para realçar o texto diretamente em arquivos PDF, da mesma forma que uma marca-texto física realçaria o papel.
  * Rolagem aperfeiçoada de PDF. Agora, você poderá experimentar a rolagem livre de travamentos ao navegar por documentos em PDF grandes.

* **Mudança de perfil automática no Windows 7, 8 e 8.1.** A mudança de perfil automática disponível atualmente no Microsoft Edge no Windows 10 foi estendida para versões inferiores do Windows (Windows 7, 8 e 8.1). Para saber mais, confira a postagem de blog [mudança de perfil automática](https://blogs.windows.com/msedgedev/2020/04/30/automatic-profile-switching/).

* **Os usuários verão sugestões de preenchimento automático quando começarem a digitar uma consulta de pesquisa no site de Complementos do Microsoft Edge.** O preenchimento automático ajuda os usuários a concluir a consulta de pesquisa sem ter que digitar a cadeia de caracteres inteira. Isso será útil porque os usuários não precisarão se lembrar das ortografias corretas e poderão escolher uma das opções disponíveis.

* **Remover a API de cache de aplicativo HTML5.**  A partir da versão 86 do Microsoft Edge, a API de cache de aplicativo herdado que permite o uso offline de páginas da Web será removida do Microsoft Edge. Os desenvolvedores da Web devem examinar a [documentação WebDev](https://web.dev/appcache-removal/) para saber mais sobre como substituir a API de cache de aplicativo com Profissionais de Serviço.  Importante: você pode solicitar um [Token OriginTrial do AppCache](https://developers.chrome.com/origintrials/#/view_trial/1776670052997660673) que permite que os sites continuem usando a versão preterida da API de cache de aplicativo até a versão 90 do Microsoft Edge.

* **Segurança:**

  * Suporte ao DNS seguro (DNS em HTTPS).  A partir da versão 86 do Microsoft Edge, as configurações para controlar o DNS seguro em dispositivos não gerenciados estarão disponíveis. Essas configurações não podem ser acessadas por usuários em dispositivos gerenciados, mas os administradores de TI podem habilitar ou desabilitar o DNS seguro usando a política de grupo [dnsoverhttpsmode](https://docs.microsoft.com/deployedge/microsoft-edge-policies#dnsoverhttpsmode).


* **Adicione uma imagem personalizada à página Nova guia (NTP) usando uma política de grupo.** A partir da versão 86 do Microsoft Edge, a NTP tem a opção de substituir a imagem padrão por uma imagem personalizada fornecida pelo usuário. A habilidade de gerenciar as propriedades desta imagem também é compatível com a política de grupo.

* **Combinar os atalhos de teclado personalizados com o VS Code.** O DevTools do Microsoft Edge agora é compatível com a personalização de atalhos de teclado no DevTools para corresponder ao editor/IDE. (No Microsoft Edge 84, adicionamos a capacidade de combinar os atalhos de teclado do DevTools com o VS Code).

* **Substituir as políticas [MetricsReportingEnabled]( https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#metricsreportingenabled) e [SendSiteInformationToImproveServices]( https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sendsiteinfotoimproveservices) para versões inferiores do Windows e macOS.** Essas políticas foram preteridas na versão 86 do Microsoft Edge e se tornarão preteridas na versão 89 do Microsoft Edge.<br>
Essas políticas são substituídas por [Permitir Telemetria](https://go.microsoft.com/fwlink/?linkid=2099569) no Windows 10 e a nova política [DiagnosticData](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#diagnosticdata) para todas as outras políticas. Isso permitirá que os usuários gerenciem os dados de diagnóstico enviados para a Microsoft do Windows 7, 8, 8.1 e macOS.

* **SameSite=Lax Cookies por padrão**. Para melhorar a segurança e a privacidade da web, os cookies agora serão padronizados para manipulação como [SameSite=Lax](https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie/SameSite). Isso significa que os cookies só serão enviados em um contexto de first-party e serão omitidos para as solicitações enviadas a terceiros. Essa alteração pode causar impacto de compatibilidade em sites que exigem cookies para recursos de terceiros funcionarem corretamente. Para permitir tais cookies, os desenvolvedores da Web podem marcar cookies que devem ser configurados e enviados a contextos de terceiros, adicionando `SameSite=none` explícitos e atributos `Secure` quando o cookie é definido. As empresas que desejam isentar determinados sites da alteração podem fazer isso usando a política [LegacySameSiteCookieBehaviorEnabledForDomainList](https://docs.microsoft.com/deployedge/microsoft-edge-policies#legacysamesitecookiebehaviorenabledfordomainlist) ou podem recusar a alteração em todos os sites que usam a política [LegacySameSiteCookieBehaviorEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#legacysamesitecookiebehaviorenabled).

### Atualizações de política

#### Novas políticas

Dezenove novas políticas foram adicionadas. Baixe os modelos administrativos atualizados da [página inicial do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise). As novas políticas a seguir foram adicionadas.

- [CollectionsServicesAndExportsBlockList](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#collectionsservicesandexportsblocklist) - Bloquear o acesso a uma lista especificada de serviços e exportar destinos em Coleções.
- [DefaultSensorsSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultsensorssetting) - configuração de sensores padrão.
- [DefaultSerialGuardSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultserialguardsetting) - Controlar o uso da API serial.
- [DiagnosticData](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#diagnosticdata) -  Enviar dados de diagnóstico obrigatórios e opcionais referentes ao uso do navegador.
- [EnterpriseModeSiteListManagerAllowed](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#enterprisemodesitelistmanagerallowed) - Permitir o acesso à ferramenta Enterprise Mode Site List Manager.
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
- [URLBlocklist](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#urlblocklist) - Bloquear o acesso a uma lista de URLs.
- [URLAllowlist](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#urlallowlist) - Definir uma lista de URLs permitidas.
- [UserAgentClientHintsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#useragentclienthintsenabled) - Habilitar o recurso de Dicas do Cliente Usuário-Agente.
- [UserDataSnapshotRetentionLimit](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#userdatasnapshotretentionlimit) - Limita o número de instantâneos de dados do usuário mantidos para uso no caso de uma reversão de emergência.

#### Políticas preteridas

- [MetricsReportingEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#metricsreportingenabled) - habilita o uso e os relatórios de dados relacionados a falhas.
- [SendSiteInfoToImproveServices](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sendsiteinfotoimproveservices) - envia informações do site para melhorar os serviços da Microsoft.

#### Política obsoleta

[TLS13HardeningForLocalAnchorsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#tls13hardeningforlocalanchorsenabled)- Habilita um recurso de segurança TLS 1,3 para âncoras de confiança locais.

#### Legenda de política alterada

[NativeWindowOcclusionEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#nativewindowocclusionenabled) - Habilitar a oclusão da janela nativa.

#### A descrição da política foi alterada

- [AdsSettingForIntrusiveAdsSites](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#adssettingforintrusiveadssites)
- [AllowTokenBindingForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#allowtokenbindingforurls)
- [AmbientAuthenticationInPrivateModesEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#ambientauthenticationinprivatemodesenabled)
- [ApplicationGuardContainerProxy](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#applicationguardcontainerproxy)
- [AutoImportAtFirstRun](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#autoimportatfirstrun)
- [AutoOpenFileTypes](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#autoopenfiletypes)
- [BrowserSignin](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#browsersignin)
- [ClearBrowsingDataOnExit](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#clearbrowsingdataonexit) 
- [ClickOnceEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#clickonceenabled)
- [CommandLineFlagSecurityWarningsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#commandlineflagsecuritywarningsenabled)
- [ConfigureOnPremisesAccountAutoSignIn](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#configureonpremisesaccountautosignin)
- [ConfigureShare](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#configureshare)
- [CookiesAllowedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#cookiesallowedforurls)
- [CustomHelpLink](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#customhelplink)
- [DefaultCookiesSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultcookiessetting)
- [DefaultGeolocationSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultgeolocationsetting)
- [DefaultImagesSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultimagessetting)
- [DefaultInsecureContentSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultinsecurecontentsetting)
- [DefaultJavaScriptSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultjavascriptsetting)
- [DefaultNotificationsSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultnotificationssetting)
- [DefaultPluginsSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultpluginssetting)
- [DefaultPopupsSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultpopupssetting)
- [DefaultSearchProviderEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultsearchproviderenabled)
- [DefaultWebBluetoothGuardSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultwebbluetoothguardsetting)
- [DefaultWebUsbGuardSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultwebusbguardsetting)
- [DelayNavigationsForInitialSiteListDownload](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#delaynavigationsforinitialsitelistdownload)
- [DeveloperToolsAvailability](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#developertoolsavailability)
- [EnableSha1ForLocalAnchors](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#enablesha1forlocalanchors)
- [DownloadRestrictions](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#downloadrestrictions)
- [EnableDeprecatedWebPlatformFeatures](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#enabledeprecatedwebplatformfeatures)
- [WinHttpProxyResolverEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#winhttpproxyresolverenabled)
- [ExperimentationAndConfigurationServiceControl](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#experimentationandconfigurationservicecontrol)
- [ExternalProtocolDialogShowAlwaysOpenCheckbox](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#externalprotocoldialogshowalwaysopencheckbox)
- [ExtensionInstallForcelist](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#extensioninstallforcelist)
- [ForceBingSafeSearch](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#forcebingsafesearch)
- [ForceYouTubeRestrict](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#forceyoutuberestrict)
- [HomepageIsNewTabPage](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#homepageisnewtabpage)
- [HomepageLocation](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#homepagelocation)
- [InPrivateModeAvailability](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#inprivatemodeavailability)
- [InternetExplorerIntegrationEnhancedHangDetection](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#internetexplorerintegrationenhancedhangdetection)
- [InternetExplorerIntegrationLevel](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#internetexplorerintegrationlevel)
- [InternetExplorerIntegrationSiteRedirect](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#internetexplorerintegrationsiteredirect)
- [LegacySameSiteCookieBehaviorEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#legacysamesitecookiebehaviorenabled)
- [NativeWindowOcclusionEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#nativewindowocclusionenabled)
- [NavigationDelayForInitialSiteListDownloadTimeout](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#navigationdelayforinitialsitelistdownloadtimeout)
- [NetworkPredictionOptions](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#networkpredictionoptions)
- [NewTabPageLocation](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#newtabpagelocation)
- [NewTabPageSearchBox](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#newtabpagesearchbox)
- [NewTabPageSetFeedType](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#newtabpagesetfeedtype)
- [NonRemovableProfileEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#nonremovableprofileenabled)
- [PasswordProtectionWarningTrigger](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#passwordprotectionwarningtrigger)
- [PasswordProtectionLoginURLs](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#passwordprotectionloginurls)
- [PasswordProtectionChangePasswordURL](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#passwordprotectionchangepasswordurl)
- [PluginsAllowedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#pluginsallowedforurls)
- [PluginsBlockedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#pluginsblockedforurls)
- [PreventSmartScreenPromptOverride](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#preventsmartscreenpromptoverride)
- [PreventSmartScreenPromptOverrideForFiles](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#preventsmartscreenpromptoverrideforfiles)
- [ProxyMode](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxymode)
- [RegisteredProtocolHandlers](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#registeredprotocolhandlers)
- [RelaunchNotification](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#relaunchnotification)
- [RestoreOnStartup](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#restoreonstartup)
- [RestoreOnStartupURLs](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#restoreonstartupurls)
- [RestrictSigninToPattern](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#restrictsignintopattern)
- [SSLVersionMin](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sslversionmin)
- [SmartScreenAllowListDomains](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#smartscreenallowlistdomains)
- [SmartScreenEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#smartscreenenabled)
- [SmartScreenForTrustedDownloadsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#smartscreenfortrusteddownloadsenabled)
- [SmartScreenPuaEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#smartscreenpuaenabled)
- [SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled)
- [TrackingPrevention](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#trackingprevention)
- [WebRtcLocalhostIpHandling](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webrtclocalhostiphandling)

<!-- end 86 -->

## Versão 85.0.564.41: 25 de agosto

Correção de vários bugs e problemas de desempenho.

## Versão 85.0.564.40: 21 de agosto

Correção de vários bugs e problemas de desempenho.

## Versão 85.0.564.36: 17 de agosto

Correção de vários bugs e problemas de desempenho.

## Versão 85.0.564.30: 10 de agosto

Correção de vários bugs e problemas de desempenho.

## Versão 85.0.564.23: 03 de agosto

Correção de vários bugs e problemas de desempenho.

<!--- BEGIN 85 ---->
## Versão 85.0.564.18, 28 de Julho

### Atualizações de recursos

- **Sincronização local de Favoritos e Configurações**. Agora, você pode sincronizar os favoritos do navegador e as configurações entre os perfis do Active Directory dentro de seu próprio ambiente sem a necessidade de sincronização na nuvem.

- **O suporte à Política de Grupo do Microsoft Edge para combinações de sites e aplicativos confiáveis para iniciar sem aviso de confirmação.** Foi acrescentado o suporte à Política de Grupo que permite aos administradores adicionar combinações de sites e aplicativos confiáveis ​​para inicialização sem o aviso de confirmação. Isto adiciona capacidade aos administradores para configurar combinações de protocolo/origem confiáveis (como os aplicativos do Microsoft 365) para seus usuários finais suprimirem a solicitação de confirmação ao navegar para uma URL que contenha um protocolo de aplicativo.

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

<!--- END ---->

## Versão 84.0.522.35: 9 de julho

Correção de vários bugs e problemas de desempenho.

## Versão 84.0.522.28: 26 de junho

Correção de vários bugs e problemas de desempenho.

## Versão 84.0.522.26: 24 de junho

Correção de vários bugs e problemas de desempenho.

## Versão 84.0.522.20: 15 de junho

Correção de vários bugs e problemas de desempenho.

## Versão 84.0.522.15: 8 de junho

Correção de vários bugs e problemas de desempenho.

## Versão 84.0.522.11: 2 de junho

### Atualizações de recursos

- Esta versão do Microsoft Edge fornece uma melhoria na velocidade de download de lista de sites para o modo Internet Explorer.  Reduzimos o atraso de download para a lista de sites no modo Internet Explorer para 0 segundo (de uma espera de 60 segundos) na ausência de uma lista de sites armazenados em cache. Também adicionamos suporte à política de grupo para casos em que as navegações de página inicial no modo Internet Explorer precisem ser adiadas até que a lista de sites seja baixada. Para obter mais informações, confira a política [DelayNavigationsForInitialSiteListDownload](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#delaynavigationsforinitialsitelistdownload).

- O Microsoft Edge agora permite que os usuários entrem no navegador quando ele é "executado como administrador" no Windows 10. Isso ajudará os clientes que usam o Microsoft Edge no Windows Server ou nos cenários de área de trabalho remota ou área restrita.

- O Microsoft Edge agora oferece suporte total ao mouse quando estiver no modo de tela inteira. Agora, você pode usar o mouse para acessar as guias, a barra de endereços e outros itens sem ter que sair do modo de tela inteira.

- Melhoria na compra online. Adicione apelidos personalizados para cartões de crédito ou débitos salvos. Agora, você pode distinguir e diferenciar os cartões de crédito ao fazer compras online. Dar apelidos aos cartões de crédito ou débito permite que você escolha o cartão correto ao usar o preenchimento automático para selecionar um método de pagamento.

- O TLS/1.0 e o TLS/1.1 estão desabilitados por padrão. Para ajudar a descobrir sites afetados, você pode definir o sinalizador *edge://flags/#display-legacy-tls-warnings* para fazer o Microsoft Edge exibir um aviso não bloqueado de "Não Seguro" ao carregar páginas que exijam protocolos TLS herdados. A política [SSLVersionMin](https://docs.microsoft.com/deployedge/microsoft-edge-policies#sslversionmin) permite reabilitar o TLS/1.0 e o TLS/1.1. Essa política permanecerá disponível pelo menos até a versão 88 do Microsoft Edge. Para saber mais, confira [Compatibilidade de sites - alterações que afetam o Microsoft Edge](https://docs.microsoft.com/microsoft-edge/web-platform/site-impacting-changes).

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

### Atualizações de política

#### Novas políticas

Cinco novas políticas foram adicionadas. Baixe os modelos administrativos atualizados da [página inicial do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise). As novas políticas a seguir foram adicionadas.

- [AppCacheForceEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#appcacheforceenabled) - Permite reabilitar o recurso AppCache, mesmo que ele esteja desativado por padrão.
- [ApplicationGuardContainerProxy](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#applicationguardcontainerproxy)- Proxy de Contêiner do Application Guard.
- [DelayNavigationsForInitialSiteListDownload](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#delaynavigationsforinitialsitelistdownload) - Exigir que a lista de sites no Modo Empresarial esteja disponível antes da navegação na guia.
- [NativeWindowOcclusionEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#nativewindowocclusionenabled) - Ative a ocultação do Windows Nativo.
- [NavigationDelayForInitialSiteListDownloadTimeout](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#navigationdelayforinitialsitelistdownloadtimeout) -Definir um tempo limite para o atraso da navegação da guia para a Lista de Sites no Modo Empresarial.

#### Políticas preteridas

- [AllowSyncXHRInPageDismissal](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#allowsyncxhrinpagedismissal) - Autorizar páginas a enviar solicitações de XHR síncronas durante a descarte da página.
- [BuiltinCertificateVerifierEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#builtincertificateverifierenabled) - Determina se o verificador de certificado interno será usado para verificar certificados do servidor.
- [StricterMixedContentTreatmentEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#strictermixedcontenttreatmentenabled)- Habilita um tratamento mais estrito para conteúdo misto.

#### Política obsoleta

[ForceNetworkInProcess](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#forcenetworkinprocess) - Forçar a execução do código de rede no processo do navegador.

<!-- end 84 -->

## Versão 83.0.478.44: 1 de junho

Correção de vários bugs e problemas de desempenho.

## Versão 83.0.478.37: 20 de maio

Correção de vários bugs e problemas de desempenho.

## Versão 83.0.478.33: 15 de maio

Correção de vários bugs e problemas de desempenho.

## Versão 83.0.478.28: 7 de maio

Correção de vários bugs e problemas de desempenho.

## Versão 83.0.478.25: 4 de maio

Correção de vários bugs e problemas de desempenho.

## Versão 83.0.478.18: 27 de abril

Correção de vários bugs e problemas de desempenho.

## Versão 83.0.478.13: 22 de abril

### Atualizações de recursos

- Melhorias no Microsoft Defender SmartScreen: foram feitas várias melhorias no serviço Microsoft Defender SmartScreen, como proteção melhorada contra sites mal-intencionados que são redirecionados durante o carregamento e bloqueio de quadros de nível superior que substitui completamente sites mal-intencionados pela página de segurança do Microsoft Defender SmartScreen. O bloqueio de quadros de nível superior impede a reprodução de áudio e outras mídias do site mal-intencionado, o que proporciona uma experiência mais fácil e menos confusa.

- Em resposta a comentários dos usuários, os usuários agora podem impedir a limpeza de determinados cookies automaticamente quando o navegador é fechado. Essa opção será útil se houver um site do qual os usuários não queiram ser desconectados, mas ainda querem que todos os outros cookies sejam removidos quando o navegador fechar. Para usar esse recurso, acesse *edge://settings/clearBrowsingDataOnClose* e ative a opção "Cookies e outros dados do site".

- A Troca Automática de Perfis agora está disponível para ajudar você a acessar seu conteúdo de trabalho com mais facilidade em diferentes perfis. Se você usar vários perfis no trabalho, poderá verificar esse recurso navegando para um site que exija autenticação da sua conta corporativa ou de estudante enquanto estiver no seu perfil pessoal. Quando detectarmos uma alteração, você receberá uma solicitação para mudar para o seu perfil de trabalho para acessar o site sem precisar se autenticar. Quando você escolhe o perfil de trabalho para o qual deseja mudar, o site simplesmente abre no seu perfil de trabalho. Esse recurso de mudança de perfil ajuda você a manter seus dados pessoais e de trabalho separados e a acessar seu conteúdo de trabalho com mais facilidade. Se você não quiser que o recurso solicite a troca de perfis, você pode escolher a opção não me pergunte novamente isso ficará fora do seu caminho.

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

- Os usuários podem definir o Microsoft Edge como navegador padrão diretamente no Microsoft Edge **Configurações**. Esse recurso facilita a alteração do navegador padrão pelos usuários, dentro do contexto do próprio navegador, em vez de precisar pesquisar as configurações do sistema operacional. Para usar esse recurso, vá para *edge://settings/defaultBrowser* e clique em **tornar padrão**.

- Várias atualizações do DevTools, incluindo o suporte à depuração remota, aperfeiçoamentos na IU e muito mais. Para saber mais, consulte [Novidades no DevTools (Microsoft Edge 83)](https://docs.microsoft.com/microsoft-edge/devtools-guide-chromium/whats-new/2020/03/devtools).

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

<!--  end 83 -->

## Versão 81.0.416.60: 20 de abril

Correção de vários bugs e problemas de desempenho.

## Versão 81.0.416.58: 17 de abril

Atualizações de segurança.

## Versão 81.0.416.50: 10 de abril

Correção de vários bugs e problemas de desempenho.

## Versão 81.0.416.45: 3 de abril

Correção de vários bugs e problemas de desempenho.

## Versão 81.0.416.41: 30 de março

Correção de vários bugs e problemas de desempenho.

## Versão 81.0.416.34: 17 de março

Correção de vários bugs e problemas de desempenho.

## Versão 81.0.416.31: 12 de março

Correção de vários bugs e problemas de desempenho.

## Versão 81.0.416.28: 9 de março

Correção de vários bugs e problemas de desempenho.

## Versão 81.0.416.20: 28 de fevereiro

Correção de vários bugs e problemas de desempenho.

## Versão 81.0.416.12: 20 de fevereiro

### Atualizações de recursos

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

### Atualizações de política

#### Novas políticas

12 novas políticas foram adicionadas. Baixe os modelos administrativos atualizados da [página inicial do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise). As novas políticas a seguir foram adicionadas.

- [AmbientAuthenticationInPrivateModesEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#ambientauthenticationinprivatemodesenabled)- Habilite a autenticação ambiente para perfis InPrivate e Guest. 
- [AudioSandboxEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#audiosandboxenabled)- Permite que a caixa de proteção de áudio seja executada.
- [ForceLegacyDefaultReferrerPolicy](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#forcelegacydefaultreferrerpolicy): Usa uma política referencial padrão de no-referrer-when-downgrade.
- [GloballyScopeHTTPAuthCacheEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#globallyscopehttpauthcacheenabled)- Habilita o cache de autenticação HTTP globalmente.
- [ImportExtensions](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#importextensions)- Permite a importação de extensões.
- [ImportCookies](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#importcookies)- Permite a importação de cookies.
- [ImportShortcuts](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#importshortcuts)- Permite a importação de atalhos.
- [InternetExplorerIntegrationSiteRedirect](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#internetexplorerintegrationsiteredirect)Especifica como as navegações "na página" para sites não configurados se comportam quando iniciadas nas páginas do modo Internet Explorer.
- [OmniboxMSBProviderEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#omniboxmsbproviderenabled)- Habilita o provedor Microsoft Search for Business no omnibox. 
- [StricterMixedContentTreatmentEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#strictermixedcontenttreatmentenabled)- Habilita um tratamento mais estrito para conteúdo misto.
- [TLS13HardeningForLocalAnchorsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#tls13hardeningforlocalanchorsenabled)- Habilita um recurso de segurança TLS 1,3 para âncoras de confiança locais.
- [ConfigureOnPremisesAccountAutoSignIn](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#configureonpremisesaccountautosignin)- Configura o login automático com uma conta de domínio do Active Directory quando não houver nenhuma conta de domínio do Azure AD.

#### Políticas preteridas

As seguintes políticas continuam a funcionar nesta versão. Elas se tornarão "obsoletas" em uma versão futura.

- [WebComponentsV0Enabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webcomponentsv0enabled) - Reabilita a API de componentes Web V0 até M84.
- [WebDriverOverridesIncompatiblePolicies](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webdriveroverridesincompatiblepolicies)- Permite que o WebDriver substitua incompatível.

## Consulte também

- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
