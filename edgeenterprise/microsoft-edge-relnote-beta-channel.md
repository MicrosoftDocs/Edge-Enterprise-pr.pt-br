---
title: Notas da versão do Microsoft Edge para canal beta
ms.author: aguta
author: dan-wesley
manager: srugh
ms.date: 01/13/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Notas da versão do Microsoft Edge para canal beta
ms.openlocfilehash: 4a37171481d57d3255a7b19eca61c2e90aea3c52
ms.sourcegitcommit: 498a62144b099a1198c06f98ad010cf95aa33727
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/13/2021
ms.locfileid: "11268222"
---
# Notas de versão do canal do Microsoft Edge beta

Estas notas de versão fornecem informações sobre os novos recursos e atualizações não relacionadas à segurança que estão inclusos no canal Beta do Microsoft Edge. As versões arquivadas dessas notas de versão estão disponíveis [aqui.](microsoft-edge-relnote-archive-beta-channel.md)

## Versão 88.0.705.41: 11 de janeiro

Correção de vários bugs e problemas de desempenho.

## Versão 88.0.705.29: 21 de dezembro

Correção de vários bugs e problemas de desempenho.

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

<!--- Archived to version 85.0.564.18: July 28 ---->

## Ver também

- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
