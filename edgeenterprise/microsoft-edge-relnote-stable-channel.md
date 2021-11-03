---
title: Notas de versão do Microsoft Edge para Stable Channel
ms.author: leahtu
author: dan-wesley
manager: srugh
ms.date: 11/01/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Notas de versão do Microsoft Edge para Stable Channel
ms.openlocfilehash: 5c8a893254d9c9be0ccf22c76a3f873f31a58756
ms.sourcegitcommit: 42f01cad0bf15224222b2aeadb48f03d46c35723
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2021
ms.locfileid: "12154491"
---
# <a name="release-notes-for-microsoft-edge-stable-channel"></a>Notas de versão do Microsoft Edge Stable Channel

Essas notas de versão fornecem informações dos novos recursos e atualizações não relacionados à segurança que estão inclusos Microsoft Edge Stable Channel.

- Todas as atualizações de segurança estão listadas [aqui](microsoft-edge-relnotes-security.md).
- As notas de versão arquivadas do Canal Estável do Microsoft Edge estão localizadas [aqui](microsoft-edge-relnote-archive-stable-channel.md).

 Para entender os canais do Microsoft Edge, confira a [Visão geral dos canais do Microsoft Edge](microsoft-edge-channels.md).

> [!NOTE]
> Para o Canal Estável, as atualizações serão implantadas progressivamente por um ou mais dias. Para saber mais, consulte [Distribuições progressivas para atualizações do Microsoft Edge](microsoft-edge-update-progressive-rollout.md).
>
> A Plataforma da Web do Microsoft Edge evolui constantemente para melhorar a experiência, segurança e privacidade do usuário. Para saber mais, confira [Compatibilidade de sites: alterações que afetam o Microsoft Edge](/microsoft-edge/web-platform/site-impacting-changes).

## <a name="version-94099258-october-30"></a>Versão 94.0.992.58: 30 de outubro

Correção de vários bugs e problemas de desempenho para a versão Estável Estendida.

## <a name="version-950102040-october-29"></a>Versão 95.0.1020.40: 29 de outubro

> [!IMPORTANT]
> Esta atualização contém uma correção para [CVE-2021-38000](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-38000) e [CVE-2021-38003](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-38003) que foram relatadas pela equipe Chromium como tendo uma exploração na natureza. Para obter mais informações, consulte o [Guia de Atualização de Segurança](https://msrc.microsoft.com/update-guide)

As atualizações de segurança do canal Estável estão listadas [aqui](/deployedge/microsoft-edge-relnotes-security#october-29-2021).

## <a name="version-950102038-october-28"></a>Versão 95.0.1020.38: 28 de outubro

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-94099257-october-27"></a>Versão 94.0.992.57: 27 de outubro

Correção de vários bugs e problemas de desempenho para a versão Estável Estendida.

## <a name="version-950102030-october-21"></a>Versão 95.0.1020.30: 21 de outubro

As atualizações de segurança do canal estável estão listadas [aqui](/deployedge/microsoft-edge-relnotes-security#october-21-2021).

### <a name="feature-updates"></a>Atualizações de recursos

- **Veja no Explorador de Arquivos o suporte para bibliotecas do Microsoft Office SharePoint Online no Microsoft Edge.**  Agora você pode habilitar o recurso Exibir no explorador de arquivos nas Bibliotecas de Documentos Modernos do Microsoft Office SharePoint Online. Para que esta experiência seja visível e funcione para seus usuários, você precisa ativar a política do Microsoft Edge [Configurar a funcionalidade Exibir no explorador de arquivos para páginas do SharePoint no Microsoft Edge](/deployedge/microsoft-edge-policies#configureviewinfileexplorer) e atualizar sua configuração de locatário do Microsoft Office SharePoint Online. Saiba mais: [Veja arquivos Microsoft Office SharePoint Online com o Explorador de arquivo no Microsoft Edge](/SharePoint/sharepoint-view-in-edge).

- **Os links de URL do arquivo de zona da intranet serão abertos no Windows Explorador de Arquivos.**  Você pode permitir links de URL de arquivos para arquivos da zona intranet originários de sites HTTPS da zona intranet para abrir o Windows Explorador de Arquivos para esse arquivo ou diretório. Você pode habilitar esta experiência usando a política [IntranetFileLinksEnabled](/deployedge/microsoft-edge-policies#intranetfilelinksenabled).

- **Melhorias na experiência de downloads.** O suporte para o download da experiência do usuário é estendido para aplicativos progressivos de web PWAs e WebView. Também começaremos a suportar o arrastar e soltar para o Explorador de Arquivos e Desktop.

- **Continue de onde parou em documentos PDF.**  Agora você poderá retomar a leitura de onde você fechou seu documento PDF pela última vez.

- **O modo de eficiência estende a vida útil da bateria quando seu laptop entra em modo de economia de bateria.**  O modo de eficiência ficará ativo quando seu laptop entrar no modo de economia de bateria para permitir que o navegador gerencia o uso de recursos para aumentar a vida útil da bateria de sua máquina. Você terá quatro opções quando o modo de eficiência se tornar ativo: Desligado e bateria fraca, Desligado, Sempre, e Nunca. Nota: Esta recurso é uma distribuição de Recurso Controlado. Se você não vê este recurso, verifique em breve enquanto continuamos nossa distribuição.

- **Caixas de texto de formulário livre adicionadas aos documentos PDF.** Agora damos suporte à adição de caixas de texto de formulário livre a documentos PDF. Você pode usar estas caixas para preencher formulários e adicionar notas visíveis.

- **Suporte de citação adicionado às Coleções.**  Melhoramos a experiência das Coleções, especialmente para alunos e pesquisadores. As coleções começarão a apoiar citações e listas de leitura.

- **Atualizar suas senhas mais rapidamente e com menos cliques.** O navegador agora o levará diretamente para a página Alterar Senha de um determinado site. Esta ação economiza tempo e cliques ao remover a necessidade de navegar para a página manualmente. Depois que você estiver nesta página, o navegador também irá preencher automaticamente sua senha existente e sugerirá uma nova senha forte e única.  Nota: Atualmente esta recurso está disponível apenas em um número limitado de sites.

- **Criação automática de conta.** Agora oferecemos suporte adicional nas páginas de Inscrição, permitindo que você crie uma conta online com um clique. Você pode fazer isso selecionando o lista pendente de sugestões ao clicar em qualquer campo do formulário no formulário de Inscrição. Fazendo isso, não só mostrará informações relevantes para o formulário de Inscrição, mas também uma forte sugestão de nova senha. Após a seleção, todas as informações relevantes são preenchidas nos respectivos campos e a senha sugerida será automaticamente armazenada ao ser enviada para o site. Nota: Atualmente esta recurso está disponível apenas em um número limitado de sites.

### <a name="policy-updates"></a>Atualizações de política

#### <a name="new-policies"></a>Novas Políticas

- [BrowserLegacyExtensionPointsBlockingEnabled](/DeployEdge/microsoft-edge-policies#browserlegacyextensionpointsblockingenabled) Habilitar o bloqueio do ponto de extensão do navegador
- [CrossOriginWebAssemblyModuleSharingEnabled](/DeployEdge/microsoft-edge-policies#crossoriginwebassemblymodulesharingenabled) Especifica se os módulos WebAssembly podem ser enviados entre origens
- [DisplayCapturePermissionsPolicyEnabled](/DeployEdge/microsoft-edge-policies#displaycapturepermissionspolicyenabled) Especifica se as permissões de captura de exibição política é verificada ou ignorada
- [InternetExplorerIntegrationWindowOpenHeightAdjustment](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationwindowopenheightadjustment) Configurar o ajuste de pixels entre as alturas do modo window.open, com origem nas páginas do modo IE vs. páginas do modo Edge
- [InternetExplorerIntegrationWindowOpenWidthAdjustment](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationwindowopenwidthadjustment) Configurar o ajuste de pixels entre as larguras do modo window.open com origem nas páginas do modo IE vs. páginas do modo Edge
- [IntranetFileLinksEnabled](/DeployEdge/microsoft-edge-policies#intranetfilelinksenabled) Permitir que links de URL de arquivos de zona da intranet da Microsoft Edge sejam abertos no Explorador de Arquivos do Windows
- [NewSmartScreenLibraryEnabled](/DeployEdge/microsoft-edge-policies#newsmartscreenlibraryenabled) Habilitar a nova biblioteca SmartScreen
- [ShadowStackCrashRollbackBehavior](/DeployEdge/microsoft-edge-policies#shadowstackcrashrollbackbehavior) Configurar o comportamento do ShadowStack rollback
- [VisualSearchEnabled](/DeployEdge/microsoft-edge-policies#visualsearchenabled) Pesquisa visual habilitada

#### <a name="obsoleted-policies"></a>Políticas Obsoletas

- [InternetExplorerIntegrationTestingAllowed](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationtestingallowed) - Permitir teste no modo Internet Explorer.
- [LegacySameSiteCookieBehaviorEnabled](/DeployEdge/microsoft-edge-policies#legacysamesitecookiebehaviorenabled) Habilitar configuração padrão de comportamento de cookie SameSite herdado

## <a name="version-94099250-october-14"></a>Versão 94.0.992.50: 14 de outubro

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-94099247-october-11"></a>Versão 94.0.992.47:11 de outubro

As atualizações de segurança do canal Estável estão listadas [aqui](/deployedge/microsoft-edge-relnotes-security#october-11-2021).

## <a name="version-94099238-october-1"></a>Versão 94.0.992.38: 01 de outubro

> [!Important]
> Esta atualização contém uma correção para [CVE-2021-37975](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-37975) e [CVE-2021-37976](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-37976), que foram relatadas pela equipe do Chromium como tendo uma exploração em execução. Para obter mais informações, consulte o [Guia de Atualização de Segurança](https://msrc.microsoft.com/update-guide)

As atualizações de segurança do canal Estável estão listadas [aqui](/deployedge/microsoft-edge-relnotes-security#october-01-2021).

## <a name="version-94099237-september-30"></a>Versão 94.0.992.37: 30 de setembro

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-94099231-september-24"></a>Versão 94.0.992.31: 24 de setembro

> [!Important]
> Essa atualização contém uma correção para [o CVE-2021-37973,](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-37973) que foi relatada pela equipe Chromium como tendo uma exploração na natureza. Para obter mais informações, confira o [Guia de Atualização de Segurança](https://msrc.microsoft.com/update-guide).

As atualizações de segurança do canal Estável estão listadas [aqui](/deployedge/microsoft-edge-relnotes-security#september-24-2021).

### <a name="feature-updates"></a>Atualizações de recursos

- **O Microsoft Edge concluiu a mudança para uma cadência de 4 semanas para atualizações.**  Adotamos um novo ciclo de lançamento de 4 semanas para as versões principais. Leia mais aqui: https://blogs.windows.com/msedgedev/2021/03/12/new-release-cycles-microsoft-edge-extended-stable/

- **Nova opção estável estendida sendo oferecida.**  Estamos oferecendo uma nova opção Estável Estendida para nossos clientes Empresariais gerenciados. A opção Estável Estendida permanecerá em revisões pares e será atualizada a cada 8 semanas. Haverá uma atualização de segurança quinzenal.  Informações adicionais aqui: https://blogs.windows.com/msedgedev/2021/07/15/opt-in-extended-stable-release-cycle/

- **Melhorias no comportamento padrão de abertura de arquivos MHTML.**  Os arquivos MHTML continuarão a abrir no modo IE se o modo IE estiver habilitado, a menos que o arquivo MHTML tenha sido salvo do Microsoft Edge (usando as opções Salvar como ou Salvar página como no Microsoft Edge). Se o arquivo foi salvo do Microsoft Edge, ele agora será aberto no Microsoft Edge.  Essa alteração corrigirá um problema de renderização observado ao abrir um arquivo MHTML no modo IE quando salvo no Microsoft Edge.

- **Restrinja as solicitações de rede privada para proteger contextos.** O acesso a recursos em redes locais (intranet) a partir de páginas na Internet requer que essas páginas sejam entregues por HTTPS. Essa alteração está ocorrendo no projeto Chromium, no qual o Microsoft Edge se baseia. Para obter mais informações, navegue até a [entrada de Status da Plataforma Chrome.](https://chromestatus.com/feature/5436853517811712) Duas políticas de compatibilidade estão disponíveis para oferecer suporte a cenários que precisam preservar a compatibilidade com páginas não seguras: [InsecurePrivateNetworkRequestAllowed](/deployedge/microsoft-edge-policies#insecureprivatenetworkrequestsallowed) e [InsecurePrivateNetworkRequestAllowedForUrls](/deployedge/microsoft-edge-policies#insecureprivatenetworkrequestsallowedforurls).

- **Bloqueie downloads de conteúdo misto.** As páginas seguras só baixarão arquivos hospedados em outras páginas seguras, e os downloads hospedados em páginas não seguras (não HTTPS) serão bloqueados se iniciados em uma página segura. Essa alteração está ocorrendo no projeto Chromium, no qual o Microsoft Edge se baseia. Para obter mais informações, navegue até a [entrada do blog de segurança do Google](https://security.googleblog.com/2020/02/protecting-users-from-insecure_6.html).

- **Habilite o login implícito para contas locais.** Ao habilitar a política [OnlyOnPremisesImplicitSigninEnabled](/deployedge/microsoft-edge-policies#onlyonpremisesimplicitsigninenabled), apenas contas locais serão habilitadas para login implícito.  O Microsoft Edge não tentará entrar implicitamente em contas MSA ou AAD. A atualização de contas locais para contas do AAD também será interrompida.

- **Nova página de configurações de acessibilidade.**  Reunimos as configurações relacionadas à acessibilidade em uma única página. Você pode localizar a nova página edge: //settings/accessibility na lista de configurações principal. Aqui você pode localizar configurações para aumentar a página da web, mostrar um contorno de alta visibilidade ao redor da área de foco e outras configurações que podem ajudar a melhorar sua experiência de navegação na web. Continuaremos adicionando novas configurações aqui em versões futuras do Microsoft Edge.

***Novas Políticas***

- [ApplicationGuardPassiveModeEnabled](/DeployEdge/microsoft-edge-policies#applicationguardpassivemodeenabled) Ignorar a configuração da lista de sites do Application Guard e navegar no Edge normalmente
- [OnlyOnPremisesImplicitSigninEnabled](/DeployEdge/microsoft-edge-policies#onlyonpremisesimplicitsigninenabled) Apenas conta local habilitada para entrada implícita
- [WebRtcRespectOsRoutingTableEnabled](/DeployEdge/microsoft-edge-policies#webrtcrespectosroutingtableenabled) Habilite o suporte para regras de tabela de roteamento do sistema operacional Windows ao fazer conexões ponto a ponto via WebRTC

***Política Obsoleta***

- [UserAgentClientHintsEnabled](/DeployEdge/microsoft-edge-policies#useragentclienthintsenabled) Habilite o recurso de Dicas de Cliente do Agente do Usuário

## <a name="version-93096152-september-16"></a>Versão 93.0.961.52: 16 de setembro

>[!Important]
>Esta atualização contém uma correção para [CVE-2021-30633](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-30632) que foi relatada pela equipe Chromium como tendo uma exploração em execução. Para obter mais informações, confira o [Guia de Atualização de Segurança](https://msrc.microsoft.com/update-guide).

As atualizações de segurança do canal estável estão listadas [aqui](/deployedge/microsoft-edge-relnotes-security#september-16-2021).

## <a name="version-93096147-september-11"></a>Versão 93.0.961.47: 11 de setembro

> [!Important]
> Esta atualização contém uma correção para [CVE-2021-30632](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-30632) que foi relatado pela equipe do Chromium como tendo um exploit. Para obter mais informações, confira o [Guia de Atualização de Segurança](https://msrc.microsoft.com/update-guide).

As atualizações de segurança do canal estável estão listadas [aqui](/deployedge/microsoft-edge-relnotes-security#september-11-2021).

## <a name="version-93096144-september-9"></a>Versão 93.0.961.44: 9 de setembro

As atualizações de segurança do canal estável estão listadas [aqui](/deployedge/microsoft-edge-relnotes-security#september-09-2021).

## <a name="version-93096138-september-2"></a>Versão 93.0.961.38: 2 de setembro

As atualizações de segurança do canal estável estão listadas [aqui](/deployedge/microsoft-edge-relnotes-security#september-02-2021).

### <a name="feature-updates"></a>Atualizações de recursos

- **Preferências Iniciais no Microsoft Edge.**  O Microsoft Edge agora oferece suporte a um número limitado de Preferências Iniciais (anteriormente Preferências Mestre). Os administradores de IT podem implantar essas configurações como padrão antes que o navegador seja executado pela primeira vez por seus usuários. Informações adicionais aqui: [Configurar o Microsoft Edge usando as configurações de Preferências Iniciais para a primeira execução](/deployedge/initial-preferences-support-on-microsoft-edge-browser).

- **O modo IE no Microsoft Edge dará suporte ao comportamento "sem mesclagem".**  Para um usuário final, quando uma nova janela do navegador é lançada de um aplicativo de modo IE, ela estará em uma sessão separada, semelhante ao comportamento sem mesclagem no IE11. Você precisará ajustar sua lista de sites para configurar sites que precisam impedir o compartilhamento de sessão como "sem mesclagem". Nos bastidores, para cada janela do Microsoft Edge, a primeira vez que uma guia de modo IE é visitada dentro dessa janela, se for um dos sites designados "sem mesclagem", essa janela será bloqueada em uma sessão do IE "sem mesclagem" diferente de todas as outras janelas do Microsoft Edge pelo menos até que a última guia de modo IE seja fechada nessa janela. Isso segue o comportamento anterior em que os usuários podem iniciar o IE sem mesclagem e também podem iniciar o Microsoft Edge sem mesclagem por meio de outros mecanismos.  Informações adicionais aqui: [solução de problemas de modo IE e perguntas frequentes | Microsoft Docs](/deployedge/edge-ie-mode-faq#does-ie-mode-on-microsoft-edge-support-the--nomerge--option-that-was-supported-in-internet-explorer-11-)

- **Nova política para interromper a entrada implícita.**  A política [ImplicitSignInEnabled](/deployedge/microsoft-edge-policies#implicitsigninenabled) permite que os administradores do sistema desabilitem a entrada implícita em navegadores Microsoft Edge.

- **Políticas para ignorar prompts do ClickOnce e DirectInvoke.** Atualizamos nossas políticas para permitir ignorar prompts do ClickOnce e o aplicativo do DirectInvoke para tipos de arquivo especificados, de domínios especificados. Para fazer isso, você precisará:

  - Habilitar [ClickOnceEnabled](/deployedge/microsoft-edge-policies#clickonceenabled) ou [DirectInvokeEnabled](/deployedge/microsoft-edge-policies#directinvokeenabled)
  - Habilitar a política [AutoOpenFileTypes](/deployedge/microsoft-edge-policies#autoopenfiletypes) e definir a lista de tipos de arquivo específicos para os quais ClickOnce e DirectInvoke devem ser desabilitados
  - Habilitar a política [AutoOpenAllowedForURLs](/deployedge/microsoft-edge-policies#autoopenallowedforurls) e definir a lista de domínios específicos para os quais ClickOnce e DirectInvoke serão desabilitados.

  Observação: AutoOpenAllowedForURLs é uma política de suporte para AutoOpenFileTypes. Se AutoOpenAllowedForURLs não estiver definido e AutoOpenFileTypes estiver definido, os tipos de arquivo listados abrirão automaticamente de todas as URLs.

- **Grupos de Guias.**  Estamos ativando o grupo de guias que oferece a capacidade de categorizar guias em grupos definidos pelo usuário e ajuda você a encontrar, alternar e gerenciar guias com mais eficiência em vários fluxos de trabalho.  

- **Ocultar a barra de título ao usar Guias Verticais.**  Obtenha os pixels extras de volta ocultando a barra de título do navegador, enquanto estiver em Guias Verticais. Agora você pode ir para edge://settings/appearance e, na seção Personalizar Barra de Ferramentas, selecione a opção para ocultar a barra de título enquanto estiver no modo Guia Vertical.

- **Video em Picture-in-Picture (PiP) da barra de ferramentas de foco.**  Quando você passar o mouse sobre um vídeo com suporte, aparecerá uma barra de ferramentas que permite que você veja esse vídeo em uma janela PiP.  Observe que, no momento, isso está disponível para usuários do Microsoft Edge no macOS.  

- **Remoção do 3DES no TLS. O suporte para o pacote de codificação TLS_RSA_WITH_3DES_EDE_CBC_SHA será removido.** Essa alteração está ocorrendo no projeto Chromium, no qual o Microsoft Edge se baseia. Para obter mais informações, navegue até a [entrada de Status da Plataforma Chrome.](https://chromestatus.com/feature/6678134168485888) Além disso, no Microsoft Edge versão 93, a política [TripleDESEnabled](/deployedge/microsoft-edge-policies#tripledesenabled) estará disponível para dar suporte a cenários que precisam preservar a compatibilidade com servidores desatualizados. Essa política de compatibilidade se tornará obsoleta e não funcionará no Microsoft Edge versão 95. Certifique-se de atualizar os servidores afetados antes disso.

***Novas políticas***

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
- [WAMAuthBelowWin10RS3Enabled](/DeployEdge/microsoft-edge-policies#wamauthbelowwin10rs3enabled) para autenticação abaixo do Windows 10 RS3 habilitado

***Política Preterida***

- [LegacySameSiteCookieBehaviorEnabled](/DeployEdge/microsoft-edge-policies#legacysamesitecookiebehaviorenabled) Habilitar configuração padrão de comportamento de cookie SameSite herdado

***Política Obsoleta***

- [NewTabPageSetFeedType](/DeployEdge/microsoft-edge-policies#newtabpagesetfeedtype) Configure Microsoft Edge nova experiência de página da guia

***Alteração Adicional***

- [ConfigureShare](/DeployEdge/microsoft-edge-policies#configureshare) adicionar suporte à plataforma mac
- [PasswordMonitorAllowed](/DeployEdge/microsoft-edge-policies#passwordmonitorallowed) Adicionar suporte à plataforma mac

## <a name="version-92090284-august-26"></a>Versão 92.0.902.84: 26 de agosto

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-92090278-august-19"></a>Versão 92.0.902.78: 19 de agosto

As atualizações de segurança do canal estável estão listadas [aqui](/deployedge/microsoft-edge-relnotes-security#august-19-2021).

## <a name="version-92090273-august-12"></a>Versão 92.0.902.73: 12 de agosto

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-92090267-august-5"></a>Versão 92.0.902.67: 5 de agosto

As atualizações de segurança do canal Estável estão listadas [aqui](/deployedge/microsoft-edge-relnotes-security#august-05-2021).

## <a name="version-92090262-july-29"></a>Versão 92.0.902.62: 29 de julho

Vários bugs e problemas de desempenho corrigidos.

### <a name="modified-policy"></a>Política modificada

- AutoplayAllowed: definir como “Desabilitado” agora define a reprodução automática de mídia como “Limite”
<!-- end major 92 -->
<!-- Archive from Version 92.0.902.55: July 22 to Version 91.0.864.37: May 27 -->
<!-- Archive from 89.0.774.45: March 4 to 90.0.818.66: May 20 ->
<!-- Archive from 86.0.622.43: October 15 to beta 88.0.705.81: February 25  ->
<!-- Archive from 86.0.622.38-october-9 to beta 86.0.62.215-september-14  ->
<!-- Archived to version 84.0.522.40: July 16 -->

## <a name="see-also"></a>Veja também

- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
