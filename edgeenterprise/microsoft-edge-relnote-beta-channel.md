---
title: Notas da versão do Microsoft Edge para canal beta
ms.author: aguta
author: dan-wesley
manager: srugh
ms.date: 03/10/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Notas da versão do Microsoft Edge para canal beta
ms.openlocfilehash: 24fbf10b0b32ef4e64c74fdeaa4831bf01df7a87
ms.sourcegitcommit: 6d37cd6dc8618742f4729fc901fc66829dab462e
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/10/2021
ms.locfileid: "11406242"
---
# <a name="release-notes-for-microsoft-edge-beta-channel"></a>Notas de versão do canal do Microsoft Edge beta

Estas notas de versão fornecem informações sobre os novos recursos e atualizações não relacionadas à segurança que estão inclusos no canal Beta do Microsoft Edge. Versões arquivadas dessas notas de versão estão disponíveis [ aqui](microsoft-edge-relnote-archive-beta-channel.md).

> [!NOTE]
> Atualizamos a nota de versão do Microsoft Edge Beta [Versão 89.0.774.18: 3 de fevereiro](#version-89077418-february-3) para refletir os recursos que foram lançados.

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

- **A ferramenta Enterprise Mode Site List Manager estará disponível no navegador através da página do *edge://compat* **. Você pode usar esta ferramenta para criar, editar e exportar o XML da lista de sites para o modo Internet Explorer no Microsoft Edge. Você pode habilitar o acesso a esta ferramenta conforme necessário por meio da política de grupo. [Saiba Mais](https://docs.microsoft.com/deployedge/edge-ie-mode-site-list-manager).

- **Melhore o desempenho do navegador com guias de suspensão**. As guias em suspensão aprimoram o desempenho do navegador colocando as guias inativas em suspensão para liberar recursos do sistema, como memória e CPU, para que as guias ativas ou outros aplicativos possam usá-las. Os usuários podem impedir que os sites entrem em suspensão e configurem o período de tempo antes de uma Tabulação inativa entrar em suspensão. Para manter os usuários em seu fluxo, há também a [heurística](https://techcommunity.microsoft.com/t5/articles/sleeping-tabs-faq/m-p/1705434) para evitar que certos sites entre em modo de suspensão, como sites intranet. Esse recurso pode ser gerenciado com políticas de grupo.

  > [!NOTE]
  > "Melhorar o desempenho do navegador com guias de suspensão" é uma atualização para as notas de lançamento de 3 de fevereiro para a versão principal 89.0.774.18.

- **Redefinir manualmente seus dados de sincronização do Microsoft Edge na nuvem**. Introduziremos uma maneira de redefinir os seus dados de sincronização do Microsoft Edge dentro do produto. Isso garante que os seus dados sejam removidos dos serviços Microsoft, além de resolver certos problemas de produto que exigiam um tíquete de suporte.

- **Melhorias na experiência de seleção de texto em documentos PDF**. Os usuários começarão a ter uma experiência de seleção de texto mais uniforme e consistente em documentos PDF abertos no Microsoft Edge a partir da versão 89.

- **O campo de data de nascimento agora é compatível com o preenchimento automático**. Hoje, o Microsoft Edge ajuda você a economizar tempo e esforço ao preencher formulários e criar contas online, preenchendo automaticamente seus dados como endereços, nomes, números de telefone, etc. A partir da versão 89 do Microsoft Edge, estamos adicionando suporte para outro campo que você pode ter salvar e preencher automaticamente: a data de nascimento. Você pode exibir, editar e excluir essas informações a qualquer momento nas configurações do seu perfil.

- **Suporte para pesquisa com linguagem natural na barra de endereços, página de pesquisa do histórico e no hub de histórico**. A partir da versão 89 do Microsoft Edge, encontrar um artigo/site será mais fácil com a pesquisa em idioma natural na barra de endereços, na página do histórico e no hub de histórico. Os usuários podem pesquisar pelo conteúdo/descrição/tempo de uma página exibidos anteriormente (tal como "receita de bolo da semana passada"), além de correspondências de títulos/palavras-chave de URL. Este recurso é limitado a um grupo selecionado aleatoriamente de usuários que ativaram a experimentação. Esses usuários estão fazendo comentários para a equipe de recursos.

### <a name="policy-updates"></a>Atualizações de política

#### <a name="new-policies"></a>Novas políticas

- [BrowsingDataLifetime](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#browsingdatalifetime) - Configurações de Tempo de Vida de Dados de Navegação
- [MAMEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#mamenabled) - Gerenciamento de Aplicativos Móveis Habilitado
- [DefinePreferredLanguages](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#definepreferredlanguages) - Define uma lista ordenada de idiomas preferidos em que os sites devem ser exibidos se o site oferecer suporte
- [ShowRecommendationsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#showrecommendationsenabled) - Permite recomendações e notificações promocionais do Microsoft Edge
- [PrintingAllowedBackgroundGraphicsModes](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#printingallowedbackgroundgraphicsmodes) - Restringe o modo de impressão de elementos gráficos de plano de fundo
- [PrintingBackgroundGraphicsDefault](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#printingbackgroundgraphicsdefault)- Modo padrão de impressão de elementos gráficos de plano de fundo
- [SmartActionsBlockList](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#smartactionsblocklist)- Bloqueia ações inteligentes para uma lista de serviços

#### <a name="obsoleted-policies"></a>Políticas obsoletas

- [ForceLegacyDefaultReferrerPolicy](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#forcelegacydefaultreferrerpolicy) - Usa uma política referencial padrão de no-referrer-when-downgrade
- [MetricsReportingEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#metricsreportingenabled) - Habilita o uso e os relatórios de dados relacionados a falhas
- [SendSiteInfoToImproveServices](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sendsiteinfotoimproveservices) - Envia informações do site para melhorar os serviços da Microsoft
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

- **Opção de modo de quiosque para encerrar a sessão**. O botão "Encerrar sessão" agora está disponível em uma experiência de navegação pública do modo de quiosque. Esse recurso garante que os dados e as configurações do navegador sejam excluídos quando o Microsoft Edge estiver fechado. Saiba mais sobre os recursos do modo de quiosque e o roteiro, [Configurar o modo de quiosque do Microsoft Edge](https://docs.microsoft.com/deployedge/microsoft-edge-configure-kiosk-mode).

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

#### <a name="deprecated-policies"></a>Políticas preteridas

As políticas a seguir estão preteridas.

- [ProactiveAuthEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proactiveauthenabled) – habilita a autenticação pró-ativa.
- [ProxyBypassList](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxybypasslist) - configura regras de bypass de proxy.
- [Proxymode](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxymode) - define configurações de servidor proxy.
- [ProxyPacUrl](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxypacurl) - define a URL do arquivo proxy.pac.
- [ProxyServer](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxyserver) - configura o endereço ou URL do servidor proxy.
- [WebDriverOverridesIncompatiblePolicies](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webdriveroverridesincompatiblepolicies) - permite que o WebDriver substitua políticas incompatíveis.

#### <a name="obsoleted-policies"></a>Políticas obsoletas

As políticas a seguir estão obsoletas.

- [DefaultPluginsSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultpluginssetting) - configuração padrão do Adobe Flash.
- [PluginsAllowedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#pluginsallowedforurls) - permite o plug-in do Adobe Flash em sites específicos.
- [PluginsBlockedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#pluginsblockedforurls) - bloqueia o plug-in do Adobe Flash em sites específicos.
- [RunAllFlashInAllowMode](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#runallflashinallowmode) - estende a configuração do Adobe Flash Content para todo o conteúdo.

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

<!-- begin major 87 -->
## <a name="version-87066412-october-20"></a>Versão 87.0.664.12: 20 de outubro

### <a name="feature-updates"></a>Atualizações de recursos

- **Recursos de privacidade do modo de quiosque habilitados**. A partir do Microsoft Edge versão 87, os recursos do modo de quiosque que ajudarão as empresas em torno da privacidade dos dados do usuário serão habilitados. Esses recursos habilitarão experiências, como limpar os dados do usuário ao sair, excluir arquivos baixados e redefinir a experiência de iniciação configurada após uma quantidade específica de tempo ocioso. Saiba mais sobre como [Configurar as opções do modo de quiosque do Microsoft Edge](https://docs.microsoft.com/deployedge/microsoft-edge-configure-kiosk-mode)
- **Implantação de ClickOnce habilitada por padrão**. O ClickOnce está habilitado por padrão no Microsoft Edge 87, o que reduz as barreiras para a implantação de software e alinha-se melhor com o comportamento do navegador da Versão Prévia do Microsoft Edge. A partir do Microsoft Edge 87, o estado "Não Configurado" da política de ClickOnceEnabled refletirá o novo estado de ClickOnce padrão Habilitado (em comparação com o estado padrão anterior Desabilitado).
- **A página nova guia da empresa (NTP) integra a produtividade com o conteúdo do feed personalizado e relevante para o trabalho**. O NTP empresarial combina a página de produtividade do Office 365 oferecemos a todos os usuários que entraram com uma conta corporativa ou de estudante com feeds personalizados da empresa e da indústria relevantes para o trabalho que são organizados em uma única página. Os usuários poderão reconhecer o conteúdo familiar do Office 365 e da Pesquisa da Microsoft para Empresas, da plataforma Bing. Além disso, eles podem facilmente inverter para um "Meu Feed" personalizável com conteúdo e módulos relevantes para o usuário, para a empresa ou para a sua indústria, além de uma seleção de outros feeds disponibilizados pela organização. [Saiba mais](https://docs.microsoft.com/microsoft-365/admin/manage/manage-industry-news?view=o365-worldwide&preserve-view=true).

- **Segurança e privacidade:**

  - Suporte a Associação de Token TLS para sites de política configurada. A associação de Token TLS ajuda a evitar ataques de roubo de token para garantir que os cookies não possam ser reutilizados a partir de um dispositivo que não tenha sido definido inicialmente. O uso da ligação de token TLS exige a configuração da política [AllowTokenBindingForUrls](https://docs.microsoft.com/deployedge/microsoft-edge-policies#allowtokenbindingforurls) e exige que os sites listados ofereçam suporte a esse recurso.

- **Suporte a teclado para marca-texto em arquivos PDF**. Os usuários podem usar as teclas do teclado para realçar qualquer texto em um PDF.

- **Impressão:**

  - Escolha o lado a ser invertido ao imprimir nos dois lados. Os usuários podem optar por virar o lado maior ou o lado menor de uma planilha ao imprimir em ambos os lados.
  - Escolha o modo de rasterização de impressão para a empresa. Controlar como o Microsoft Edge é impresso em uma impressora não PostScript no Windows. Às vezes, os trabalhos de impressão em impressoras não PostScript precisam ser rasterizados para serem impressos corretamente. As opções de impressão são "Total" e "Rápida".

### <a name="policy-updates"></a>Atualizações de política

#### <a name="new-policies"></a>Novas políticas

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

#### <a name="deprecated-policy"></a>Política Preterida

[NewTabPageSetFeedType](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#newtabpagesetfeedtype) - configurar a nova experiência de página da guia Microsoft Edge.

#### <a name="obsoleted-policy"></a>Política obsoleta

[EnableDeprecatedWebPlatformFeatures](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#enabledeprecatedwebplatformfeatures) - reative os recursos da plataforma Web preteridos por um tempo limitado.

<!-- end major 87 -->

## <a name="version-86062243-october-16"></a>Versão 86.0.622.43: 16 de outubro

Correção de vários bugs e problemas de desempenho.

## <a name="version-86062236-october-7"></a>Versão 86.0.622.36: 7 de outubro

Correção de vários bugs e problemas de desempenho.

## <a name="version-86062231-october-1"></a>Versão 86.0.622.31: 1 de outubro

Correção de vários bugs e problemas de desempenho.

## <a name="version-86062228-september-28"></a>Versão 86.0.622.28: 28 de setembro

Correção de vários bugs e problemas de desempenho.

## <a name="version-86062215-september-14"></a>Versão 86.0.622.15: 14 de setembro

Correção de vários bugs e problemas de desempenho.

<!--- Archived to version 86.0.622.11: September 9 ---->
<!--- Archived to version 85.0.564.18: July 28 ---->

## <a name="see-also"></a>Ver também

- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
