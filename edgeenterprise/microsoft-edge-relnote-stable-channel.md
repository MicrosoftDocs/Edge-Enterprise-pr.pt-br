---
title: Notas de versão do Microsoft Edge para Stable Channel
ms.author: aguta
author: dan-wesley
manager: srugh
ms.date: 03/15/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Notas de versão do Microsoft Edge para Stable Channel
ms.openlocfilehash: 7d08aa1d9cf1f3e04861561169d2f6a01772e5f2
ms.sourcegitcommit: b1060a5c71174ba1d2eea91efb51232beeb97bf8
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "11409245"
---
# <a name="release-notes-for-microsoft-edge-stable-channel"></a>Notas de versão do Microsoft Edge Stable Channel

Essas notas de versão fornecem informações dos novos recursos e atualizações não relacionados à segurança que estão inclusos Microsoft Edge Stable Channel.

- Todas as atualizações de segurança estão listadas [aqui](microsoft-edge-relnotes-security.md).
- As notas de versão arquivadas do Canal Estável do Microsoft Edge estão localizadas [aqui](microsoft-edge-relnote-archive-stable-channel.md).

 Para entender os canais do Microsoft Edge, confira a [Visão geral dos canais do Microsoft Edge](microsoft-edge-channels.md).

> [!NOTE]
> Para o Canal Estável, as atualizações serão implantadas progressivamente por um ou mais dias. Para saber mais, confira [Lançamentos progressivos para atualizações do Microsoft Edge](microsoft-edge-update-progressive-rollout.md).

## <a name="version-89077454-march-13"></a>Versão 89.0.774.54: 13 de março

> [!IMPORTANT]
> Esta atualização contém [CVE-2021-21193](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-21193) que foi relatada pela equipe do Chromium como tendo uma exploração na natureza. Para obter mais informações, consulte o [Guia de atualização de segurança](https://msrc.microsoft.com/update-guide).

As atualizações de segurança do canal estável estão listadas [aqui](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#march-13-2021).

## <a name="version-89077450-march-10"></a>Versão 89.0.774.50: 10 de março

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-89077448-march-8"></a>Versão 89.0.774.48: 8 de março

Correção de vários bugs e problemas de desempenho.

<!-- begin major 89 -->
## <a name="version-89077445-march-4"></a>Versão 89.0.774.45: 4 de março

> [!IMPORTANT]
> Esta atualização contém o [CVE-2021-21166](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-21166) que foi reportado pela equipe da Chromium por ter uma vulnerabilidade em aberto. Para obter mais informações, confira o [Guia de Atualização de Segurança](https://msrc.microsoft.com/update-guide).

As atualizações de segurança do canal estável estão listadas [aqui](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#march-4-2021).

### <a name="resolved-issues"></a>Problemas resolvidos

- **Atualizações e correções de atalhos da barra de tarefas e do menu Iniciar:**
  - Clicar com o botão direito do mouse no atalho do Microsoft Edge no menu Iniciar agora mostrará corretamente a opção para desafixar o Microsoft Edge da barra de tarefas quando ele estiver fixado.
  - Layouts iniciais que incluem uma [configuração da barra de tarefas](https://docs.microsoft.com/windows/configuration/configure-windows-10-taskbar) para fixar o Microsoft Edge na barra de tarefas não resultará mais em um segundo atalho do Microsoft Edge sendo fixado na barra de tarefas.
  - As organizações que utilizam Perfis de Roaming do Windows não verão mais um ícone branco vazio no lugar do ícone do Microsoft Edge na barra de tarefas quando seus usuários fizerem logon no Windows.

### <a name="feature-updates"></a>Atualizações de recursos

- **O modo quiosque permite recursos adicionais de bloqueio**. A partir da versão 89 do Microsoft Edge, adicionamos funcionalidades adicionais de bloqueio no modo de quiosque para permitir que os clientes executem as tarefas em uma experiência mais produtiva e segura. [Saiba mais](microsoft-edge-configure-kiosk-mode.md#kiosk-mode-supported-features).

- **A ferramenta Enterprise Mode Site List Manager estará disponível no navegador através da página do *edge://compat* **. Você pode usar esta ferramenta para criar, editar e exportar o XML da lista de sites para o modo Internet Explorer no Microsoft Edge. Você pode habilitar o acesso a esta ferramenta conforme necessário por meio da política de grupo. [Saiba Mais](https://docs.microsoft.com/deployedge/edge-ie-mode-site-list-manager).

- **Melhore o desempenho do navegador com guias de suspensão**. As guias em suspensão aprimoram o desempenho do navegador colocando as guias inativas em suspensão para liberar recursos do sistema, como memória e CPU, para que as guias ativas ou outros aplicativos possam usá-las. Os usuários podem impedir que os sites entrem em suspensão e configurem o período de tempo antes de uma Tabulação inativa entrar em suspensão. Para manter os usuários em seu fluxo, há também a [heurística](https://techcommunity.microsoft.com/t5/articles/sleeping-tabs-faq/m-p/1705434) para evitar que certos sites entre em modo de suspensão, como sites intranet. Esse recurso pode ser gerenciado com políticas de grupo.

- **Redefinir manualmente seus dados de sincronização do Microsoft Edge na nuvem**. Introduziremos uma maneira de redefinir os seus dados de sincronização do Microsoft Edge dentro do produto. Isso garante que os seus dados sejam removidos dos serviços Microsoft, além de resolver certos problemas do produto que exigiam um tíquete de suporte.

- **Habilitação inteligente de SSO (Logon único) para todas as contas do Windows Azure Active Directory (Azure AD) para usuários com um único perfil do Microsoft Edge que não é do Azure AD**.  Ative automaticamente essa configuração para os usuários que podem se beneficiar ao máximo desse recurso. Se um usuário tiver apenas um perfil do Microsoft Edge (e não for o Azure AD ou o Modo Infantil), a configuração será automaticamente acionada quando o Microsoft Edge for inicializado. Essa alternância automática também será desativada automaticamente se um usuário mais tarde optar por entrar em um perfil diferente do Microsoft Edge com uma conta do Azure AD. Os usuários podem atualizar manualmente suas preferências para esse recurso em **Configurações > Perfis > Preferências de perfil > Permitir um logon único para sites de trabalho ou de escola usando esse perfil**.

- **Melhorias na experiência de seleção de texto em documentos PDF**. Os usuários começarão a ter uma experiência de seleção de texto mais uniforme e consistente em documentos PDF abertos no Microsoft Edge a partir da versão 89.

- **O campo de data de nascimento agora é compatível com o preenchimento automático**. Hoje, o Microsoft Edge ajuda você a economizar tempo e esforço ao preencher formulários e criar contas online, preenchendo automaticamente seus dados como endereços, nomes, números de telefone, etc. A partir da versão 89 do Microsoft Edge, estamos adicionando suporte para outro campo que você pode ter salvar e preencher automaticamente: a data de nascimento. Você pode exibir, editar e excluir essas informações a qualquer momento nas configurações do seu perfil.

### <a name="policy-updates"></a>Atualizações de política

#### <a name="new-policies"></a>Novas políticas

Sete novas políticas foram adicionadas. Baixe os modelos administrativos atualizados da [página inicial do Microsoft Edge Enterprise](https://www.microsoft.com/edge/business/download). As novas políticas a seguir foram adicionadas.

- [BrowsingDataLifetime](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#browsingdatalifetime) - Configurações do Tempo de Vida de Dados de Navegação
- [MAMEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#mamenabled) - Gerenciamento de Aplicativos Móveis Habilitado
- [DefinePreferredLanguages](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#definepreferredlanguages) - Define uma lista ordenada de idiomas preferidos em que os sites devem ser exibidos se o site oferecer suporte
- [ShowRecommendationsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#showrecommendationsenabled) - Permitir recomendações e notificações promocionais do Microsoft Edge
- [PrintingAllowedBackgroundGraphicsModes](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#printingallowedbackgroundgraphicsmodes) - Restringe o modo de impressão de elementos gráficos de plano de fundo
- [PrintingBackgroundGraphicsDefault](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#printingbackgroundgraphicsdefault) - Modo padrão de impressão de gráficos em segundo plano
- [SmartActionsBlockList](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#smartactionsblocklist) - Bloqueie ações inteligentes  para uma lista de serviços

#### <a name="obsoleted-policies"></a>Políticas obsoletas

As políticas a seguir estão obsoletas.

- [ForceLegacyDefaultReferrerPolicy](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#forcelegacydefaultreferrerpolicy) - Usa uma política referencial padrão de no-referrer-when-downgrade
- [MetricsReportingEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#metricsreportingenabled) - Habilita o uso e os relatórios de dados relacionados a falhas
- [SendSiteInfoToImproveServices](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sendsiteinfotoimproveservices) - Envie as informações do site para melhorar os serviços da Microsoft
<!-- end major 89 -->
## <a name="version-88070581-february-25"></a>Versão 88.0.705.81: 25 de fevereiro

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-88070574-february-17"></a>Versão 88.0.705.74: 17 de fevereiro

As atualizações de segurança do canal estável estão listadas [aqui](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#February-17-2021).

## <a name="version-88070568-february-11"></a>Versão 88.0.705.68: 11 de fevereiro

Correção de vários bugs e problemas de desempenho.

## <a name="version-88070563-february-5"></a>Versão 88.0.705.63: 5 de Fevereiro

> [!IMPORTANT]
> Esta atualização contém o [CVE-2021-21148](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-21148) que foi reportado pela equipe da Chromium por ter uma vulnerabilidade em aberto.

As atualizações de segurança do canal estável estão listadas [aqui](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#February-5-2021).

## <a name="version-88070562-february-4"></a>Versão 88.0.705.62: 4 de Fevereiro

As atualizações de segurança do canal estável estão listadas [aqui](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#February-4-2021).

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-88070556-january-28"></a>Versão 88.0.705.56: 28 de Janeiro

Correção de vários bugs e problemas de desempenho.

## <a name="version-88070553-january-26"></a>Versão 88.0.705.53: 26 de janeiro

Correção de vários bugs e problemas de desempenho.

## <a name="version-88070550-january-21"></a>Versão 88.0.705.50: 21 de janeiro

As atualizações de segurança do canal estável estão listadas [aqui](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#january-21-2021).

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

- **Melhore a velocidade de inicialização do Microsoft Edge com o aumento da inicialização**. Para melhorar a velocidade de inicialização do Microsoft Edge, desenvolvemos um recurso chamado aumento de inicialização. O aumento da inicialização abre o Microsoft Edge mais rapidamente, permitindo que o Microsoft Edge seja executado em segundo plano. Observação: esse recurso está limitado a um grupo de usuários selecionado aleatoriamente que habilitou o experimento. Esses usuários estão fazendo comentários para a equipe de recursos.

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

#### <a name="deprecated-policies"></a>Políticas preteridas

- [ProactiveAuthEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proactiveauthenabled) - habilita a autenticação pró-ativa.
- [ProxyBypassList](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxybypasslist) - configura regras de bypass de proxy.
- [Proxymode](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxymode) - define configurações de servidor proxy.
- [ProxyPacUrl](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxypacurl) - define a URL do arquivo proxy.pac.
- [ProxyServer](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxyserver) - configura o endereço ou URL do servidor proxy.
- [WebDriverOverridesIncompatiblePolicies](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webdriveroverridesincompatiblepolicies) - permite que o WebDriver substitua políticas incompatíveis.

### <a name="obsoleted-policies"></a>Políticas Obsoletas

- [AllowPopupsDuringPageUnload](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#allowpopupsduringpageunload) - permite que uma página mostre pop-ups durante seu descarregamento.
- [DefaultPluginsSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultpluginssetting) - configuração padrão do Adobe Flash.
- [PluginsAllowedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#pluginsallowedforurls) - permite o plug-in do Adobe Flash em sites específicos.
- [PluginsBlockedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#pluginsblockedforurls) - bloqueia o plug-in do Adobe Flash em sites específicos.
- [RunAllFlashInAllowMode](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#runallflashinallowmode) - estende a configuração do Adobe Flash Content para todo o conteúdo.
<!--- end major 88  --->
## <a name="version-87066475-january-7"></a>Versão 87.0.664.75: 7 de janeiro

As atualizações de segurança do canal estável estão listadas [aqui](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#january-7-2021).

## <a name="version-87066466-december-17"></a>Versão 87.0.664.66: 17 de dezembro

Correção de vários bugs e problemas de desempenho.

## <a name="version-87066460-december-10"></a>Versão 87.0.664.60: 10 de dezembro

Correção de vários bugs e problemas de desempenho.

## <a name="version-87066457-december-7"></a>Versão 87.0.664.57: 7 de dezembro

Vários bugs e problemas de desempenho corrigidos. As atualizações de segurança do canal estável estão listadas [aqui](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#december-7-2020).

## <a name="version-87066455-december-3"></a>Versão 87.0.664.55: 3 de dezembro

Correção de vários bugs e problemas de desempenho. O seguinte recurso foi atualizado para este lançamento.

- **O Shopping está habilitado por padrão**. A partir da versão 87 do Microsoft Edge, os usuários corporativos podem se beneficiar das compras no Microsoft Edge. Com os recursos de compra, o Microsoft Edge ajuda os usuários a encontrar cupons e melhores preços ao fazer compras online. (A experiência de cupom foi lançada com a versão estável 87.0.664.41). A experiência de comparação de preços agora está disponível nesta atualização. Este recurso pode ser configurado usando a política [EdgeShoppingAssistantEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#edgeshoppingassistantenabled). Veja nosso [Blog](https://blogs.windows.com/windowsexperience/2020/11/19/finish-up-that-holiday-shopping-with-new-features-from-microsoft-edge-and-bing/) e [Saiba mais](https://docs.microsoft.com/microsoft-edge/privacy-whitepaper#shopping) sobre o Microsoft Shopping.

## <a name="version-87066452-november-30"></a>Versão 87.0.664.52: 30 de novembro

Correção de vários bugs e problemas de desempenho.

## <a name="version-87066447-november-23"></a>Versão 87.0.664.47: 23 de novembro

Correção de vários bugs e problemas de desempenho.

<!-- begin major 87 --->
## <a name="version-87066441-november-19"></a>Versão 87.0.664.41: 19 de novembro

As atualizações de segurança do canal estável estão listadas [aqui](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#november-19-2020).

### <a name="feature-updates"></a>Atualizações de recursos

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

### <a name="policy-updates"></a>Atualizações de política

#### <a name="new-policies"></a>Novas políticas

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

#### <a name="deprecated-policy"></a>Política Preterida

[NewTabPageSetFeedType](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#newtabpagesetfeedtype) - configurar a nova experiência de página da guia Microsoft Edge.

#### <a name="obsoleted-policy"></a>Política obsoleta

[EnableDeprecatedWebPlatformFeatures](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#enabledeprecatedwebplatformfeatures) - reative os recursos da plataforma Web preteridos por um tempo limitado.

<!-- end major 87 -->

## <a name="version-86062269-november-13"></a>Versão 86.0.622.69: 13 de novembro

> [!IMPORTANT]
> Esta atualização contém o [CVE-2020-16013](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-16013) e o [CVE-2020-16017](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-16017), que foi reportado pela equipe da Chromium por ter uma vulnerabilidade em aberto.

As atualizações de segurança do canal estável estão listadas [aqui](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#november-13-2020).

## <a name="version-86062268-november-11"></a>Versão 86.0.622.68: 11 de novembro

As atualizações de segurança do canal estável estão listadas [aqui](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#november-11-2020)

## <a name="version-86062263-november-4"></a>Versão 86.0.622.63: 4 de novembro

> [!IMPORTANT]
> Esta atualização contém o [CVE-2020-16009](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-16009), que foi reportado pela equipe da Chromium por ter uma vulnerabilidade em aberto.

As atualizações de segurança do canal estável estão listadas [aqui](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#november-4-2020).

## <a name="version-86062261-november-2"></a>Versão 86.0.622.61: 2 de novembro

Correção de vários bugs e problemas de desempenho.

## <a name="version-86062258-october-29"></a>Versão 86.0.622.58: 29 de outubro

Correção de vários bugs e problemas de desempenho.

## <a name="version-86062256-october-27"></a>Versão 86.0.622.56: 27 de outubro

Correção de vários bugs e problemas de desempenho.

## <a name="version-86062251-october-22"></a>Versão 86.0.622.51 : 22 de outubro

As atualizações de segurança do canal estável estão listadas [aqui](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#october-22-2020)

## <a name="version-86062248-october-20"></a>Versão 86.0.622.48: 20 de outubro

Correção de vários bugs e problemas de desempenho.

## <a name="version-86062243-october-15"></a>Versão 86.0.622.43: 15 de outubro

Correção de vários bugs e problemas de desempenho.

<!-- Archive from 86.0.622.38-october-9 to beta 86.0.62.215-september-14  ->
<!-- Archived to version 84.0.522.40: July 16 -->

## <a name="see-also"></a>Ver também

- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
