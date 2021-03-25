---
title: Notas da versão do Microsoft Edge para canal beta
ms.author: aguta
author: dan-wesley
manager: srugh
ms.date: 03/22/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Notas da versão do Microsoft Edge para canal beta
ms.openlocfilehash: 9d9bec56a3629f18f7a9f64553858558a2864100
ms.sourcegitcommit: f363ceb6c42054fabc95ce8d7bca3c52d80e6a9f
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/24/2021
ms.locfileid: "11447565"
---
# <a name="release-notes-for-microsoft-edge-beta-channel"></a>Notas de versão do canal do Microsoft Edge beta

Estas notas de versão fornecem informações sobre os novos recursos e atualizações não relacionadas à segurança que estão inclusos no canal Beta do Microsoft Edge. Versões arquivadas dessas notas de versão estão disponíveis [ aqui](microsoft-edge-relnote-archive-beta-channel.md).

> [!NOTE]
> Atualizamos a nota de versão do Microsoft Edge Beta [Versão 89.0.774.18: 3 de fevereiro](#version-89077418-february-3) para refletir os recursos que foram lançados.

## <a name="version-90081814-march-22"></a>Versão 90.0.818.14: 22 de março

Correção de vários bugs e problemas de desempenho.
<!-- begin major 90 -->
## <a name="version-9008188-march-16"></a>Versão 90.0.818.8: 16 de março

### <a name="feature-updates"></a>Atualizações de recursos

- **O Logon Único (SSO) agora está disponível para contas do Azure Active Directory (Azure AD) e conta Microsoft (MSA) no macOS**. Um usuário conectado no Microsoft Edge em macOS agora terá automaticamente acesso aos sites que estão configurados para permitir logon único com as contas Microsoft e Corporativas (por exemplo, bing.com, office.com, msn.com e outlook.com).

- **Impressão:**

  - **Novo modo de rasterização de impressão para impressoras não PostScript**. A partir da versão 90 do Microsoft Edge, os administradores poderão usar uma nova política para definir o modo de rasterização de impressão para seus usuários. Esta política  controla como o Microsoft Edge imprime para impressoras não PostScript no Windows.  Às vezes, os trabalhos de impressão em impressoras não PostScript precisam ser rasterizados para serem impressos corretamente. As opções de impressão são Completa e Rápida.

  - **Opções adicionais de dimensionamento de página para impressão**. Os usuários agora podem personalizar o dimensionamento enquanto imprimem páginas da Web e documentos PDF usando as opções adicionais. A opção "Ajustar à página" garante que a página da Web ou o documento se ajuste ao espaço disponível no "Tamanho do papel" selecionado para impressão. A opção "Tamanho real" garante que não ocorram mudanças no tamanho do conteúdo que está sendo impresso, independentemente do "Tamanho do papel" selecionado.

- **Produtividade:**

  - **As sugestões de preenchimento automático são estendidas para incluir o conteúdo dos campos de endereço da área de transferência**. O conteúdo da área de transferência é analisado quando você clica em um campo de perfil/endereço (por exemplo, telefone, email, CEP, cidade, estado, etc.) para mostrar como sugestões de preenchimento automático.

  - **Os usuários podem pesquisar sugestões de preenchimento automático mesmo se um formulário ou campo não for detectado**. Hoje, se você tiver suas informações salvas no Microsoft Edge, as sugestões de preenchimento automático aparecem automaticamente e ajudam você a economizar tempo enquanto preenche formulários. Nos casos em que o preenchimento automático falhar em um formulário ou se você quiser buscar dados em formulários que normalmente não têm preenchimento automático (como formulários temporários), você pode procurar suas informações usando o preenchimento automático.

- **Acesse downloads a partir de um submenu na barra de menu**. Os downloads aparecerão no canto superior direito com todos os downloads ativos em um só lugar. Este menu é facilmente descartável para que os usuários possam continuar navegando ininterruptamente e possam monitorar o progresso geral do download diretamente da barra de ferramentas. [Saiba mais](https://techcommunity.microsoft.com/t5/articles/introducing-the-new-downloads-experience/m-p/2111551).

- **Melhorias na renderização de fontes**. A partir da versão 90 do Microsoft Edge, fizemos melhorias na renderização do texto para melhorar a clareza e reduzir o desfocado. Parte das melhorias de renderização da fonte pousará na versão Beta 90, mas serão desativadas por padrão.


### <a name="policy-updates"></a>Atualizações de política

#### <a name="new-policies"></a>Novas políticas

Sete novas políticas foram adicionadas. Baixe os modelos administrativos atualizados da [página de aterrissagem do Microsoft Edge Enterprise](https://www.microsoft.com/edge/business/download). Foram adicionadas as novas políticas a seguir:

- [ApplicationGuardFavoritesSyncEnabled](./microsoft-edge-policies.md#applicationguardfavoritessyncenabled) - Habilitada a Sincronização de Favoritos do Application Guard
- [ManagedConfigurationPerOrigin](./microsoft-edge-policies.md#managedconfigurationperorigin) - Define valores de configuração gerenciada para sites de origens específicas
- [PrintRasterizationMode](./microsoft-edge-policies.md#printrasterizationmode) - Modo de Rasterização de Impressão
- [QuickViewOfficeFilesEnabled](./microsoft-edge-policies.md#quickviewofficefilesenabled) - Gerenciar a capacidade de Visualização Rápida de arquivos do Office no Microsoft Edge
- [SSLErrorOverrideAllowedForOrigins](./microsoft-edge-policies.md#sslerroroverrideallowedfororigins) - Permitir que os usuários prossigam a partir da página de aviso HTTPS para origens específicas
- [WindowOcclusionEnabled](./microsoft-edge-policies.md#windowocclusionenabled) - Habilitar Oclusão de Janela
- [WindowsHelloForHTTPAuthEnabled](./microsoft-edge-policies.md#windowshelloforhttpauthenabled) - Windows Hello habilitado para autenticação HTTP

#### <a name="deprecated-policies"></a>Políticas preteridas

- [NativeWindowOcclusionEnabled](./microsoft-edge-policies.md#nativewindowocclusionenabled) - Habilitar Oclusão de Janela Nativa
- [SSLVersionMin](./microsoft-edge-policies.md#sslversionmin)- Versão mínima do TLS habilitada
<!-- end major 90 -->

## <a name="version-89077454-march-13"></a>Versão 89.0.774.54: 13 de março

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-89077450-march-10"></a>Versão 89.0.774.50: 10 de março

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-89077448-march-8"></a>Versão 89.0.774.48: 8 de março

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-89077445-march-3"></a>Versão 89.0.774.45: 3 de março

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-89077439-february-26"></a>Versão 89.0.774.39: 26 de fevereiro

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-89077434-february-22"></a>Versão 89.0.774.34: 22 de fevereiro

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-89077427-february-12"></a>Versão 89.0.774.27: 12 de fevereiro

Correção de vários bugs e problemas de desempenho.

## <a name="version-89077423-february-8"></a>Versão 89.0.774.23: 8 de fevereiro

Correção de vários bugs e problemas de desempenho.

<!-- begin major 89 -->
## <a name="version-89077418-february-3"></a>Versão 89.0.774.18: 3 de fevereiro

### <a name="feature-updates"></a>Atualizações de recursos

- **O modo quiosque permite recursos adicionais de bloqueio**. A partir da versão 89 do Microsoft Edge, adicionamos funcionalidades adicionais de bloqueio no modo de quiosque para permitir que os clientes executem as tarefas em uma experiência mais produtiva e segura. [Saiba mais](microsoft-edge-configure-kiosk-mode.md#kiosk-mode-supported-features).

- **A ferramenta Enterprise Mode Site List Manager estará disponível no navegador através da página do *edge://compat* **. Você pode usar esta ferramenta para criar, editar e exportar o XML da lista de sites para o modo Internet Explorer no Microsoft Edge. Você pode habilitar o acesso a esta ferramenta conforme necessário por meio da política de grupo. [Saiba Mais](./edge-ie-mode-site-list-manager.md).

- **Melhore o desempenho do navegador com guias de suspensão**. As guias em suspensão aprimoram o desempenho do navegador colocando as guias inativas em suspensão para liberar recursos do sistema, como memória e CPU, para que as guias ativas ou outros aplicativos possam usá-las. Os usuários podem impedir que os sites entrem em suspensão e configurem o período de tempo antes de uma Tabulação inativa entrar em suspensão. Para manter os usuários em seu fluxo, há também a [heurística](https://techcommunity.microsoft.com/t5/articles/sleeping-tabs-faq/m-p/1705434) para evitar que certos sites entre em modo de suspensão, como sites intranet. Esse recurso pode ser gerenciado com políticas de grupo.

  > [!NOTE]
  > "Melhorar o desempenho do navegador com guias de suspensão" é uma atualização para as notas de lançamento de 3 de fevereiro para a versão principal 89.0.774.18.

- **Redefinir manualmente seus dados de sincronização do Microsoft Edge na nuvem**. Introduziremos uma maneira de redefinir os seus dados de sincronização do Microsoft Edge dentro do produto. Isso garante que os seus dados sejam removidos dos serviços Microsoft, além de resolver certos problemas de produto que exigiam um tíquete de suporte.

- **Melhorias na experiência de seleção de texto em documentos PDF**. Os usuários começarão a ter uma experiência de seleção de texto mais uniforme e consistente em documentos PDF abertos no Microsoft Edge a partir da versão 89.

- **O campo de data de nascimento agora é compatível com o preenchimento automático**. Hoje, o Microsoft Edge ajuda você a economizar tempo e esforço ao preencher formulários e criar contas online, preenchendo automaticamente seus dados como endereços, nomes, números de telefone, etc. A partir da versão 89 do Microsoft Edge, estamos adicionando suporte para outro campo que você pode ter salvar e preencher automaticamente: a data de nascimento. Você pode exibir, editar e excluir essas informações a qualquer momento nas configurações do seu perfil.

- **Suporte para pesquisa com linguagem natural na barra de endereços, página de pesquisa do histórico e no hub de histórico**. A partir da versão 89 do Microsoft Edge, encontrar um artigo/site será mais fácil com a pesquisa em idioma natural na barra de endereços, na página do histórico e no hub de histórico. Os usuários podem pesquisar pelo conteúdo/descrição/tempo de uma página exibidos anteriormente (tal como "receita de bolo da semana passada"), além de correspondências de títulos/palavras-chave de URL. Este recurso é limitado a um grupo selecionado aleatoriamente de usuários que ativaram a experimentação. Esses usuários estão fazendo comentários para a equipe de recursos.

### <a name="policy-updates"></a>Atualizações de política

#### <a name="new-policies"></a>Novas políticas

- [BrowsingDataLifetime](./microsoft-edge-policies.md#browsingdatalifetime) - Configurações de Tempo de Vida de Dados de Navegação
- [MAMEnabled](./microsoft-edge-policies.md#mamenabled) - Gerenciamento de Aplicativos Móveis Habilitado
- [DefinePreferredLanguages](./microsoft-edge-policies.md#definepreferredlanguages) - Define uma lista ordenada de idiomas preferidos em que os sites devem ser exibidos se o site oferecer suporte
- [ShowRecommendationsEnabled](./microsoft-edge-policies.md#showrecommendationsenabled) - Permite recomendações e notificações promocionais do Microsoft Edge
- [PrintingAllowedBackgroundGraphicsModes](./microsoft-edge-policies.md#printingallowedbackgroundgraphicsmodes) - Restringe o modo de impressão de elementos gráficos de plano de fundo
- [PrintingBackgroundGraphicsDefault](./microsoft-edge-policies.md#printingbackgroundgraphicsdefault)- Modo padrão de impressão de elementos gráficos de plano de fundo
- [SmartActionsBlockList](./microsoft-edge-policies.md#smartactionsblocklist)- Bloqueia ações inteligentes para uma lista de serviços

#### <a name="obsoleted-policies"></a>Políticas obsoletas

- [ForceLegacyDefaultReferrerPolicy](./microsoft-edge-policies.md#forcelegacydefaultreferrerpolicy) - Usa uma política referencial padrão de no-referrer-when-downgrade
- [MetricsReportingEnabled](./microsoft-edge-policies.md#metricsreportingenabled) - Habilita o uso e os relatórios de dados relacionados a falhas
- [SendSiteInfoToImproveServices](./microsoft-edge-policies.md#sendsiteinfotoimproveservices) - Envia informações do site para melhorar os serviços da Microsoft
<!-- end major 89 -->

## <a name="version-88070556-january-29"></a>Versão 88.0.705.56: 29 de janeiro

Correção de vários bugs e problemas de desempenho.

## <a name="version-88070549-january-20"></a>Versão beta 88.0.705.49: 20 de janeiro

Correção de vários bugs e problemas de desempenho.

## <a name="version-88070545-january-15"></a>Versão 88.0.705.45: 15 de janeiro

Correção de vários bugs e problemas de desempenho.

## <a name="version-88070541-january-11"></a>Versão 88.0.705.41: 11 de janeiro

Correção de vários bugs e problemas de desempenho.

## <a name="version-88070529-december-21"></a>Versão 88.0.705.29: 21 de dezembro

Correção de vários bugs e problemas de desempenho.

<!-- begin major 88 -->
## <a name="version-88070518-december-9"></a>Versão 88.0.705.18: 9 de dezembro

### <a name="feature-updates"></a>Atualizações de recursos

- **Preteridos:**

  - Preterir o suporte para o protocolo FTP. O suporte para o protocolo de FTP herdado foi removido do Microsoft Edge. Tentar navegar para um link de FTP fará com que o navegador direcione o sistema operacional para abrir um aplicativo externo para manipular o link de FTP. Como alternativa, os administradores de TI podem configurar o Microsoft Edge para usar o modo IE para sites que dependem do protocolo FTP.
  - O suporte ao Adobe Flash será removido. A partir do Microsoft Edge beta versão 88, a funcionalidade e o suporte do Adobe Flash serão removidos. Saiba mais: [Atualização no fim do suporte do Adobe Flash Player - blog do Microsoft Edge (Windows.com)](https://blogs.windows.com/msedgedev/2020/09/04/update-adobe-flash-end-support/)

- **Autenticação:**

  - O logon único (SSO) agora está disponível para contas do Azure Active Directory (Azure AD) e para a conta Microsoft (MSA) em Windows MacOS e de nível inferior. Um usuário conectado no Microsoft Edge no Windows Microsoft MacOS ou no nível inferior do Microsoft Windows (7, 8.1) agora será automaticamente conectado aos sites que estiverem configurados para permitir logon único com contas Work e Microsoft (por exemplo, bing.com, office.com, msn.com, outlook.com).<br>Observação: um usuário pode ter que sair e entrar novamente se ele se conectar ao Microsoft Edge em uma versão anterior ao Microsoft Edge 88 para aproveitar esse recurso.
  - Alternar automaticamente os usuários do MacOS para o perfil de trabalho dos sites que se autenticam com a conta corporativa. A partir da versão 88 do Microsoft Edge, oferecemos a capacidade de alternar os sites que se autenticam com o perfil de trabalho do usuário no MacOS.<br>Observação: um usuário pode ter que sair e entrar novamente se ele se conectar ao Microsoft Edge em uma versão anterior ao Microsoft Edge 88 para aproveitar esse recurso.

- **Opção de modo de quiosque para encerrar a sessão**. O botão "Encerrar sessão" agora está disponível em uma experiência de navegação pública do modo de quiosque. Esse recurso garante que os dados e as configurações do navegador sejam excluídos quando o Microsoft Edge estiver fechado. Saiba mais sobre os recursos do modo de quiosque e o roteiro, [Configurar o modo de quiosque do Microsoft Edge](./microsoft-edge-configure-kiosk-mode.md).

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

### <a name="policy-updates"></a>Atualizações de política

#### <a name="new-policies"></a>Novas políticas

Dezesseis novas políticas foram adicionadas. Baixe os modelos administrativos atualizados da [página inicial do Microsoft Edge Enterprise](https://www.microsoft.com/edge/business/download). As novas políticas a seguir foram adicionadas.

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
- [StartupBoostEnabled](./microsoft-edge-policies.md#startupboostenabled) - habilita o aumento de inicialização.
- [UpdatePolicyOverride](./microsoft-edge-policies.md#updatepolicyoverride) - especifica como o Microsoft Edge Update manipula as atualizações disponíveis do Microsoft Edge.
- [VerticalTabsAllowed](./microsoft-edge-policies.md#verticaltabsallowed) - configura a disponibilidade de um layout vertical para guias na lateral do navegador.
- [WebRtcAllowLegacyTLSProtocols](./microsoft-edge-policies.md#webrtcallowlegacytlsprotocols) - Permite fazer downgrade TLS/DTLS legado em WebRTC.

#### <a name="deprecated-policies"></a>Políticas preteridas

As políticas a seguir estão preteridas.

- [ProactiveAuthEnabled](./microsoft-edge-policies.md#proactiveauthenabled) – habilita a autenticação pró-ativa.
- [ProxyBypassList](./microsoft-edge-policies.md#proxybypasslist) - configura regras de bypass de proxy.
- [Proxymode](./microsoft-edge-policies.md#proxymode) - define configurações de servidor proxy.
- [ProxyPacUrl](./microsoft-edge-policies.md#proxypacurl) - define a URL do arquivo proxy.pac.
- [ProxyServer](./microsoft-edge-policies.md#proxyserver) - configura o endereço ou URL do servidor proxy.
- [WebDriverOverridesIncompatiblePolicies](./microsoft-edge-policies.md#webdriveroverridesincompatiblepolicies) - permite que o WebDriver substitua políticas incompatíveis.

#### <a name="obsoleted-policies"></a>Políticas obsoletas

As políticas a seguir estão obsoletas.

- [DefaultPluginsSetting](./microsoft-edge-policies.md#defaultpluginssetting) - configuração padrão do Adobe Flash.
- [PluginsAllowedForUrls](./microsoft-edge-policies.md#pluginsallowedforurls) - permite o plug-in do Adobe Flash em sites específicos.
- [PluginsBlockedForUrls](./microsoft-edge-policies.md#pluginsblockedforurls) - bloqueia o plug-in do Adobe Flash em sites específicos.
- [RunAllFlashInAllowMode](./microsoft-edge-policies.md#runallflashinallowmode) - estende a configuração do Adobe Flash Content para todo o conteúdo.

<!-- end major 88 -->

## <a name="version-87066455-december-3"></a>Versão 87.0.664.55: 3 de dezembro

Correção de vários bugs e problemas de desempenho. O novo recurso a seguir é compatível com esta versão.

- Alertas **são gerados se a senha de um usuário for encontrada em um vazamento online**. As senhas do usuário são verificadas em um repositório de credenciais violadas e envia ao usuário um alerta se uma correspondência for encontrada. Para garantir a segurança e a privacidade, as senhas dos usuários são criptografadas e criptografadas quando são verificadas no banco de dados de credenciais vazadas.

## <a name="version-87066452-november-30"></a>Versão 87.0.664.52: 30 de novembro

Correção de vários bugs e problemas de desempenho.

## <a name="version-87066440-november-18"></a>Versão 87.0.664.40: 18 de novembro

Correção de vários bugs e problemas de desempenho.

## <a name="version-87066436-november-16"></a>Versão 87.0.664.36: 16 de novembro

Correção de vários bugs e problemas de desempenho.

## <a name="version-87066430-november-9"></a>Versão 87.0.664.30: 9 de novembro

Correção de vários bugs e problemas de desempenho.

## <a name="version-87066424-november-2"></a>Versão 87.0.664.24: 2 de novembro

Correção de vários bugs e problemas de desempenho.

## <a name="version-87066418-october-26"></a>Versão 87.0.664.18: 26 de outubro

Correção de vários bugs e problemas de desempenho.

<!--- Archived from Version 87.0.664.12: October 20 to to version 86.0.622.15: September 14 ---->
<!--- Archived to version 86.0.622.11: September 9 ---->
<!--- Archived to version 85.0.564.18: July 28 ---->

## <a name="see-also"></a>Ver também

- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)