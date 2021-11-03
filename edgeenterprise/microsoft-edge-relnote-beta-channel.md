---
title: Notas da versão do Microsoft Edge para canal beta
ms.author: aguta
author: dan-wesley
manager: srugh
ms.date: 11/01/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Notas da versão do Microsoft Edge para canal beta
ms.openlocfilehash: 57ea92fde42d4ad4c63f238c3b30fa218ee5b360
ms.sourcegitcommit: 42f01cad0bf15224222b2aeadb48f03d46c35723
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2021
ms.locfileid: "12154512"
---
# <a name="release-notes-for-microsoft-edge-beta-channel"></a>Notas de versão do canal do Microsoft Edge beta

Estas notas de versão fornecem informações sobre os novos recursos e atualizações não relacionadas à segurança que estão inclusos no canal Beta do Microsoft Edge. Versões arquivadas dessas notas de versão estão disponíveis [aqui](microsoft-edge-relnote-archive-beta-channel.md).

> [!NOTE]
> A Plataforma da Web Microsoft Edge evolui constantemente para melhorar a experiência, segurança e privacidade do usuário. Para saber mais, confira [Compatibilidade de sites: alterações que afetam o Microsoft Edge](/microsoft-edge/web-platform/site-impacting-changes).

## <a name="version-96010548-november-1"></a>Versão 96.0.1054.8: 1 de novembro

### <a name="feature-updates"></a>Atualizações de recursos

- **Iniciar o Progressive Web App (PWA) diretamente por meio de links de protocolo.** Permitir que os PWAs instalados manipularem links que usam um protocolo específico para uma experiência mais integrada.

- **Saiba como resolver problemas de matemática com o Solver de Matemática.** Estamos animados em anunciar que você pode usar o Resolvedor de Matemática Microsoft Edge obter ajuda com uma ampla variedade de conceitos matemáticos. Esses conceitos variam de equações aritméticas e quadráticas primárias a trigonometria e cálculo. O Solver de Matemática permite que você tire uma foto de um problema de matemática manuscrita ou impressa e, em seguida, fornece uma solução instantânea com instruções passo a passo para ajudá-lo a aprender a alcançar a solução sem ajuda. O Math Solver também vem com um teclado matemático que você pode usar para digitar facilmente problemas matemáticos. Esse teclado elimina a necessidade de pesquisar em torno de um teclado tradicional para encontrar os caracteres matemáticos necessários. Depois de resolver seu problema, o Math Solver fornece opções para continuar a aprender com quizzes, planilhas e tutoriais de vídeo.

- **Aprimoramentos de rolagem para documentos PDF.** Estamos melhorando o desempenho de rolagem para fornecer uma experiência de rolagem mais suave em documentos PDF. Você não verá barras brancas aparecendo durante a rolagem.

- **Realçamento de forma livre em PDFs.** A experiência de exibição e marcação em PDF é aprimorada com a adição de realçadores de forma livre. Você pode realçar seções em PDFs que não têm acesso e documentos verificados.

- **Tecnologia de aplicação de fluxo de controle (CET).**  Microsoft Edge começar a oferecer suporte a um modo de navegação ainda mais seguro que usa o fluxo de controle dependente de hardware para processos do navegador. O fluxo de controle é fornecido neste hardware com suporte: Intel 11th Gen. ou AMD Zen 3. Você pode desabilitar o CET configurando Opções de Execução de Arquivo de Imagem (IFEO) usando a política de grupo.

- **Nova caixa de diálogo de aviso para sites typosquatting.** O navegador agora mostrará um aviso em alguns sites com URLs muito semelhantes a outros sites. Essa interface do usuário usa heurísticas do lado do cliente para avisar os usuários sobre sites que podem estar spoofando sites populares. Para obter mais informações, consulte [O que é typosquatting?](https://support.microsoft.com/topic/what-is-typosquatting-54a18872-8459-4d47-b3e3-d84d9a362eb0).

- **Handoff aprimorado entre o modo IE e o navegador moderno.**  A partir dessa versão do Microsoft Edge, as navegação entre o Microsoft Edge e o modo Internet Explorer incluirão dados de formulário e cabeçalhos HTTP adicionais. Os headers de referência, os dados postados, os dados de formulários e os métodos de solicitação serão encaminhados corretamente entre as duas experiências. Você pode especificar quais tipos de dados devem ser incluídos usando a [política InternetExplorerIntegrationComplexNavDataTypes.](/deployedge/microsoft-edge-policies#internetexplorerintegrationcomplexnavdatatypes)

- **Gerenciamento de Lista de Sites na Nuvem para modo IE na Visualização Pública.**  O Gerenciamento de Lista de Sites na Nuvem permite que você gerencie suas listas de sites para o modo IE na nuvem sem precisar de uma infraestrutura local para hospedar a lista de sites da sua organização. Você pode acessar o recurso Gerenciamento de Lista de Sites na Nuvem usando Microsoft Edge experiência de Listas de Sites no Administração Microsoft 365 Center. Para saber mais, consulte o artigo Gerenciamento de Lista de Sites na Nuvem [para modo IE (Visualização Pública).](./edge-ie-mode-cloud-site-list-mgmt.md)

- **Atualize Microsoft Edge WebWiew2 usando o WSUS.** Os administradores de IT que usam o WSUS para atualizar Microsoft Edge também poderão atualizar Microsoft Edge WebView2 usando o WSUS. Esse recurso oferece aos administradores um processo de manutenção mais fácil para dispositivos offline.

- **Atualizações do WSUS para Server.** As atualizações do WSUS e do Catálogo para canais Microsoft Edge (Estável, Beta, Dev) agora serão aplicadas Windows SKUs do servidor que tenham Microsoft Edge instalados, incluindo o Windows Server 2022. Para obter mais informações sobre como configurar as atualizações do WSUS para Microsoft Edge, consulte [Update Microsoft Edge](https://docs.microsoft.com/mem/configmgr/apps/deploy-use/deploy-edge?bc=https%3A%2F%2Fdocs.microsoft.com%2FDeployEdge%2Fbreadcrumb%2Ftoc.json&toc=https%3A%2F%2Fdocs.microsoft.com%2FDeployEdge%2Ftoc.json#update-microsoft-edge).

### <a name="policy-updates"></a>Atualizações de política

#### <a name="new-policies"></a>Novas Políticas

- [ApplicationGuardUploadBlockingEnabled](/DeployEdge/microsoft-edge-policies#applicationguarduploadblockingenabled) - Impede que os arquivos são carregados enquanto estão no Application Guard.
- [AudioProcessHighPriorityEnabled](/DeployEdge/microsoft-edge-policies#audioprocesshighpriorityenabled) - Permitir que o processo de áudio seja executado com prioridade acima do normal em Windows.
- [AutoLaunchProtocolsComponentEnabled](/DeployEdge/microsoft-edge-policies#autolaunchprotocolscomponentenabled) - Componente autoLaunch Protocols Enabled.
- [EfficiencyMode](/DeployEdge/microsoft-edge-policies#efficiencymode) - Configure quando o modo de eficiência deve ficar ativo.
- [ForceSyncTypes](/DeployEdge/microsoft-edge-policies#forcesynctypes) - Configure a lista de tipos incluídos para sincronização.
- [InternetExplorerIntegrationComplexNavDataTypes](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationcomplexnavdatatypes) - Configure whether form data and HTTP headers will be sent when entering or exiting Internet Explorer mode.
- [InternetExplorerModeToolbarButtonEnabled](/DeployEdge/microsoft-edge-policies#internetexplorermodetoolbarbuttonenabled) - Mostrar o botão Recarregar no modo Internet Explorer na barra de ferramentas.
- [PrintPostScriptMode](/DeployEdge/microsoft-edge-policies#printpostscriptmode) - Imprimir no PostScript Modo.
- [PrintRasterizePdfDpi](/DeployEdge/microsoft-edge-policies#printrasterizepdfdpi) - Imprimir em Rasterize PDF DPI.
- [RendererAppContainerEnabled](/DeployEdge/microsoft-edge-policies#rendererappcontainerenabled) - Habilitar renderador no contêiner de aplicativos.
- [SharedLinksEnabled](/DeployEdge/microsoft-edge-policies#sharedlinksenabled) - Mostrar links compartilhados de Microsoft 365 aplicativos no Histórico.
- [TyposquattingCheckerEnabled](/DeployEdge/microsoft-edge-policies#typosquattingcheckerenabled) - Configure Edge TyposquattingChecker.

<!-- end major 96 --->

## <a name="version-950102038-october-28"></a>Versão 95.0.1020.38: 28 de outubro

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-950102020-october-11"></a>Versão 95.0.1020.20: 11 de outubro

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-950102014-october-5"></a>Versão 95.0.1020.14: 5 de outubro

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-95010209-september-28"></a>Versão 95.0.1020.9: 28 de setembro

### <a name="feature-updates"></a>Atualizações de recursos

- **Veja no Explorador de Arquivos o suporte para bibliotecas do Microsoft Office SharePoint Online no Microsoft Edge.**  Agora você pode habilitar o recurso Exibir no Explorador de Arquivos para SharePoint bibliotecas de documentos modernas online. Para que essa experiência seja visível e funcione para seus usuários, você precisará habilitar Microsoft Edge política "Configurar o recurso Exibir no Explorador de Arquivos para páginas SharePoint [em Microsoft Edge"](/deployedge/microsoft-edge-policies#configureviewinfileexplorer) e atualizar sua configuração de locatário do SharePoint Online. Saiba mais: Exibir SharePoint arquivos com o Explorador de [Arquivos no Microsoft Edge - SharePoint no Microsoft 365 | Microsoft Docs](/SharePoint/sharepoint-view-in-edge).

- **Os links de URL do arquivo de zona da intranet serão abertos no Windows Explorador de Arquivos.**  Você pode permitir links de URL de arquivos para arquivos da zona intranet originários de sites HTTPS da zona intranet para abrir o Windows Explorador de Arquivos para esse arquivo ou diretório. Você pode habilitar esta experiência usando a política [IntranetFileLinksEnabled](/deployedge/microsoft-edge-policies#intranetfilelinksenabled).

- **Melhorias na experiência de downloads.**  O suporte para a experiência do usuário de download está sendo estendido para aplicativos Web progressivos PWAs e WebView. Também começaremos a suportar o arrastar e soltar para o Explorador de Arquivos e Desktop.

- **Continue de onde parou em documentos PDF.**  Você pode retomar a leitura do local onde fechou o documento PDF pela última vez.

- **O modo de eficiência estende a vida útil da bateria quando seu laptop entra em modo de economia de bateria.**  O modo de eficiência ficará ativo quando seu laptop entrar no modo de economia de bateria para permitir que o navegador gerencia o uso de recursos para aumentar a vida útil da bateria de sua máquina. Você terá quatro opções para quando o modo de eficiência se tornar ativo, Unplugged e bateria baixa, Unplugged, Always e Never. Observação: esta é uma rollout de recursos controlados. Dispositivos com bateria devem ter o recurso ligado.

***Novas políticas***

- [BrowserLegacyExtensionPointsBlockingEnabled](/DeployEdge/microsoft-edge-policies#browserlegacyextensionpointsblockingenabled) - Habilitar o bloqueio do ponto de extensão herdado do navegador.
- [CrossOriginWebAssemblyModuleSharingEnabled](/DeployEdge/microsoft-edge-policies#crossoriginwebassemblymodulesharingenabled) - Especifica se os módulos WebAssembly podem ser enviados de origem cruzada.
- [DisplayCapturePermissionsPolicyEnabled](/DeployEdge/microsoft-edge-policies#displaycapturepermissionspolicyenabled) - Especifica se a política de permissões de captura de exibição está marcada ou ignorada.
- [InternetExplorerIntegrationWindowOpenHeightAdjustment](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationwindowopenheightadjustment) - Configure the pixel adjustment between window.open heights sourced from IE mode pages vs. Microsoft Edge mode pages.
- [InternetExplorerIntegrationWindowOpenWidthAdjustment](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationwindowopenheightadjustment) - Configure the pixel adjustment between window.open widths sourced from IE mode pages vs. Microsoft Edge mode pages.
- [IntranetFileLinksEnabled](/DeployEdge/microsoft-edge-policies#intranetfilelinksenabled) - Permitir que os links de URL do arquivo de zona da intranet Microsoft Edge abrir no Windows File Explorer.
- [ShadowStackCrashRollbackBehavior](/DeployEdge/microsoft-edge-policies#shadowstackcrashrollbackbehavior) - Configurar o comportamento de rebaixamento de falha do ShadowStack.
- [VisualSearchEnabled](/DeployEdge/microsoft-edge-policies#visualsearchenabled) - Habilitar a pesquisa visual.

***Políticas Obsoletas***

- [InternetExplorerIntegrationTestingAllowed](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationtestingallowed) - Permitir teste no modo Internet Explorer.
- [LegacySameSiteCookieBehaviorEnabled](/DeployEdge/microsoft-edge-policies#legacysamesitecookiebehaviorenabled) -habilita a configuração padrão de cookie herdado SameSite padrão.

## <a name="version-94099223-september-17"></a>Versão 94.0.992.23: 17 de setembro

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-94099219-september-13"></a>Versão 94.0.992.19: 13 de setembro

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-94099214-september-7"></a>Versão 94.0.992.14: 7 de setembro

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-9409929-september-2"></a>Versão 94.0.992.9: 2 de setembro

### <a name="feature-updates"></a>Atualizações de recursos

- **Microsoft Edge mudar para uma cadência de 4 semanas para atualizações nos canais Beta e Estável.**  Adotaremos um novo ciclo de lançamento de quatro semanas para versões principais. Você pode ler mais sobre a decisão aqui: https://blogs.windows.com/msedgedev/2021/03/12/new-release-cycles-microsoft-edge-extended-stable/

- **Nova opção estável estendida sendo oferecida.**  Estamos oferecendo uma nova opção Estável Estendida para nossos clientes Empresariais gerenciados. A opção Estável Estendida permanecerá em revisões pares e será atualizada a cada 8 semanas. Haverá uma atualização de segurança quinzenal.  Informações adicionais aqui: https://blogs.windows.com/msedgedev/2021/07/15/opt-in-extended-stable-release-cycle/

- **Melhorias no comportamento padrão de abertura de arquivos MHTML.**  Os arquivos MHTML continuarão a abrir no modo IE se o modo IE estiver habilitado, a menos que o arquivo MHTML tenha sido salvo do Microsoft Edge (usando as opções Salvar como ou Salvar página como no Microsoft Edge). Se o arquivo foi salvo do Microsoft Edge, ele agora será aberto no Microsoft Edge.  Essa alteração corrigirá um problema de renderização observado ao abrir um arquivo MHTML no modo IE quando salvo no Microsoft Edge.

- **Restrinja as solicitações de rede privada para proteger contextos.** O acesso a recursos em redes locais (intranet) a partir de páginas na Internet requer que essas páginas sejam entregues por HTTPS. Essa alteração está ocorrendo no projeto Chromium, no qual o Microsoft Edge se baseia. Para obter mais informações, navegue até a [entrada de Status da Plataforma Chrome.](https://chromestatus.com/feature/5436853517811712) Duas políticas de compatibilidade estão disponíveis para oferecer suporte a cenários que precisam preservar a compatibilidade com páginas não seguras: [InsecurePrivateNetworkRequestAllowed](/deployedge/microsoft-edge-policies#insecureprivatenetworkrequestsallowed) e [InsecurePrivateNetworkRequestAllowedForUrls](/deployedge/microsoft-edge-policies#insecureprivatenetworkrequestsallowedforurls).

- **Bloqueie downloads de conteúdo misto.** As páginas seguras só baixarão arquivos hospedados em outras páginas seguras, e os downloads hospedados em páginas não seguras (não HTTPS) serão bloqueados se iniciados em uma página segura. Essa alteração está ocorrendo no projeto Chromium, no qual o Microsoft Edge se baseia. Para obter mais informações, navegue até a [entrada do blog de segurança do Google](https://security.googleblog.com/2020/02/protecting-users-from-insecure_6.html).

- **Habilite o login implícito para contas locais.**   Ao habilitar a política OnlyOnPremisesImplicitSigninEnabled, apenas contas locais serão habilitadas para login implícito.  O Microsoft Edge não tentará entrar implicitamente em contas MSA ou AAD. A atualização de contas locais para contas do AAD também será interrompida.

- **Caixas de texto de formulário livre adicionadas aos documentos PDF.**  Agora, temos suporte para adicionar caixas de texto de formulário gratuitos a documentos PDF que você pode usar para preencher formulários e adicionar anotações visíveis.

- **Atualize suas senhas com facilidade.**  O navegador agora o levará diretamente para a página Alterar Senha para um determinado site economizando tempo e clicando evitando a necessidade de navegar até a página manualmente. Depois de estar nessa página, o navegador também irá autofiliá-la e sugerir uma nova senha forte e exclusiva.  Observe que, no momento, esse recurso está disponível em um número limitado de sites.  

- **Nova página de configurações de acessibilidade.** Reunimos as configurações relacionadas à acessibilidade em uma única página. Você pode localizar a nova página edge: //settings/accessibility na lista de configurações principal. Aqui você pode localizar configurações para aumentar a página da web, mostrar um contorno de alta visibilidade ao redor da área de foco e outras configurações que podem ajudar a melhorar sua experiência de navegação na web. Continuaremos adicionando novas configurações aqui em versões futuras do Microsoft Edge.

***Novas Políticas***

- [ApplicationGuardPassiveModeEnabled](/DeployEdge/microsoft-edge-policies#applicationguardpassivemodeenabled) Ignorar a configuração da lista de sites do Application Guard e navegar no Edge normalmente
- [OnlyOnPremisesImplicitSigninEnabled](/DeployEdge/microsoft-edge-policies#onlyonpremisesimplicitsigninenabled) Apenas conta local habilitada para entrada implícita
- [WebRtcRespectOsRoutingTableEnabled](/DeployEdge/microsoft-edge-policies#webrtcrespectosroutingtableenabled) Habilite o suporte para regras de tabela de roteamento do sistema operacional Windows ao fazer conexões ponto a ponto via WebRTC

***Política Obsoleta***

- [UserAgentClientHintsEnabled](/DeployEdge/microsoft-edge-policies#useragentclienthintsenabled) Habilite o recurso de Dicas de Cliente do Agente do Usuário

## <a name="version-93096133-august-27"></a>Versão 93.0.961.33: 27 de agosto

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-93096127-august-20"></a>Versão 93.0.961.27: 20 de agosto

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-93096124-august-18"></a>Versão 93.0.961.24: 18 de agosto

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-93096111-august-3"></a>Versão 93.0.961.11: 3 de agosto

### <a name="feature-updates"></a>Atualizações de recursos

- **Preferências Iniciais no Microsoft Edge.**  A partir Microsoft Edge versão 93, a implantação de Microsoft Edge para sua empresa se tornará mais fácil com a adição de [Preferências Iniciais.](/deployedge/initial-preferences-support-on-microsoft-edge-browser)

- **O modo IE no Microsoft Edge dará suporte ao comportamento "sem mesclagem".**  A partir Microsoft Edge versão 93, o modo IE no Microsoft Edge dará suporte a "no-merge". Para um usuário final, quando uma nova janela do navegador é lançada de um aplicativo de modo IE, ela estará em uma sessão separada, semelhante ao comportamento no IE11. Você precisará ajustar sua lista de sites para configurar sites que precisam impedir o compartilhamento de sessão. Nos bastidores, para cada janela do Microsoft Edge, a primeira vez que uma guia de modo IE é visitada dentro dessa janela, se for um dos sites designados "sem mesclagem", essa janela será bloqueada em uma sessão do IE "sem mesclagem" diferente de todas as outras janelas do Microsoft Edge pelo menos até que a última guia de modo IE seja fechada nessa janela. Saiba mais [aqui](/deployedge/edge-ie-mode-faq#does-ie-mode-on-microsoft-edge-support-the--no-merge--option-that-was-supported-in-internet-explorer-11-).

- **Grupos de Guias.**  A capacidade de categorizar guias em grupos definidos pelo usuário ajuda você a encontrar, alternar e gerenciar guias com mais eficiência em vários fluxos de trabalho. Para habilitar isso, estamos ativando o grupo de guias começando com Microsoft Edge versão 93.

- **Ocultar a barra de título ao usar Guias Verticais.**  Obtenha os pixels extras de volta ocultando a barra de título do navegador, enquanto estiver em Guias Verticais. A partir Microsoft Edge versão 93, você pode ir para o edge://settings/appearance e, na seção Personalizar Barra de Ferramentas, selecione a opção para ocultar a barra de título enquanto estiver no modo Guia Vertical.

- **Video em Picture-in-Picture (PiP) da barra de ferramentas de foco.**  A partir Microsoft Edge versão 93, ficará ainda mais fácil inserir Imagem no modo Imagem (PiP). Quando você passar o mouse sobre um vídeo com suporte, aparecerá uma barra de ferramentas que permite que você veja esse vídeo em uma janela PiP.  Observação: isso está disponível atualmente para Microsoft Edge usuários no macOS.  Volte logo à medida que continuarmos nossa adoção para Windows usuários.

- **Remoção do 3DES no TLS.**  A partir Microsoft Edge versão 93, o suporte para o TLS_RSA_WITH_3DES_EDE_CBC_SHA de codificação será removido. Essa alteração está ocorrendo no projeto Chromium, no qual o Microsoft Edge se baseia. Para obter mais informações, navegue até a [entrada de Status da Plataforma Chrome.](https://chromestatus.com/feature/6678134168485888) Além disso, no Microsoft Edge versão 93, a política [TripleDESEnabled](/deployedge/microsoft-edge-policies#tripledesenabled) estará disponível para dar suporte a cenários que precisam preservar a compatibilidade com servidores desatualizados. Essa política de compatibilidade se tornará obsoleta e não funcionará no Microsoft Edge versão 95. Certifique-se de atualizar os servidores afetados antes disso.

- **Políticas para ignorar prompts do ClickOnce e DirectInvoke.**  Atualizamos nossas políticas para permitir ignorar prompts do ClickOnce e o aplicativo do DirectInvoke para tipos de arquivo especificados, de domínios especificados. Para fazer isso, você precisará:

  - Habilitar [ClickOnceEnabled](/deployedge/microsoft-edge-policies#clickonceenabled) ou [DirectInvokeEnabled](/deployedge/microsoft-edge-policies#directinvokeenabled)
  - Habilitar a política [AutoOpenFileTypes](/deployedge/microsoft-edge-policies#autoopenfiletypes) e definir a lista de tipos de arquivo específicos para os quais ClickOnce e DirectInvoke devem ser desabilitados
  - Habilita [a política AutoOpenAllowedForURLs](/deployedge/microsoft-edge-policies#autoopenallowedforurls) e defina a lista de domínios específicos para os ClickOnce e o DirectInvoke serão desabilitados

  Observação: AutoOpenAllowedForURLs é uma política de suporte para AutoOpenFileTypes. Se AutoOpenAllowedForURLs não estiver definido e AutoOpenFileTypes estiver definido, os tipos de arquivo listados abrirão automaticamente de todas as URLs.

### <a name="new-policies"></a>Novas políticas

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

#### <a name="deprecated-policy"></a>Política Preterida

- [LegacySameSiteCookieBehaviorEnabled](/DeployEdge/microsoft-edge-policies#legacysamesitecookiebehaviorenabled) Habilitar configuração padrão de comportamento de cookie SameSite herdado

#### <a name="obsoleted-policy"></a>Política Obsoleta

- [NewTabPageSetFeedType](/DeployEdge/microsoft-edge-policies#newtabpagesetfeedtype) Configure Microsoft Edge nova experiência de página da guia

#### <a name="additional-change"></a>Alteração Adicional

- [ConfigureShare](/DeployEdge/microsoft-edge-policies#configureshare) adicionar suporte à plataforma mac

## <a name="version-93096118-august-10"></a>Versão 93.0.961.18: 10 de agosto

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-92090262-july-29"></a>Versão 92.0.902.62: 29 de julho

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-92090255-july-21"></a>Versão 92.0.902.55: 21 de julho

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-92090245-july-12"></a>Versão 92.0.902.45: 12 de julho

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-92090240-july-6"></a>Versão 92.0.902.40: 6 de julho

Correção de vários bugs e problemas de desempenho.

<!--Archive on Oct 27 From Version 92.0.902.22: June 21 to Version 89.0.774.23: February 8  -->
<!--- Archived from Version 87.0.664.18: October 26 to to version 89.0.774.18: February 3 ---->
<!--- Archived from Version 87.0.664.12: October 20 to to version 86.0.622.15: September 14 ---->
<!--- Archived to version 86.0.622.11: September 9 ---->
<!--- Archived to version 85.0.564.18: July 28 ---->

## <a name="see-also"></a>Ver também

- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
