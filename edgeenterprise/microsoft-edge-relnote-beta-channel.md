---
title: Notas da versão do Microsoft Edge para canal beta
ms.author: aguta
author: AndreaLBarr
manager: srugh
ms.date: 09/28/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Notas da versão do Microsoft Edge para canal beta
ms.openlocfilehash: c62d540b014a47f1240d542c68ee52822719239f
ms.sourcegitcommit: 4442aa94d4ff2fef8dd6f389ec0c6823b150d04f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/28/2021
ms.locfileid: "12053310"
---
# <a name="release-notes-for-microsoft-edge-beta-channel"></a>Notas de versão do canal do Microsoft Edge beta

Estas notas de versão fornecem informações sobre os novos recursos e atualizações não relacionadas à segurança que estão inclusos no canal Beta do Microsoft Edge. Versões arquivadas dessas notas de versão estão disponíveis [aqui](microsoft-edge-relnote-archive-beta-channel.md).

> [!NOTE]
> A Plataforma da Web Microsoft Edge evolui constantemente para melhorar a experiência, segurança e privacidade do usuário. Para saber mais, confira [Compatibilidade de sites: alterações que afetam o Microsoft Edge](/microsoft-edge/web-platform/site-impacting-changes).

## <a name="version-95010209-september-28"></a>Versão 95.0.1020.9: 28 de setembro

### <a name="feature-updates"></a>Atualizações de recursos

- **Exibir no Suporte ao Explorador de Arquivos para SharePoint online em Microsoft Edge.**  Agora você pode habilitar o recurso Exibir no Explorador de Arquivos SharePoint bibliotecas de documentos modernas online. Para que essa experiência seja visível e funcione para seus usuários, você precisará habilitar Microsoft Edge política de Microsoft Edge "Configurar o recurso Exibir no Explorador de Arquivos para páginas SharePoint no [Microsoft Edge"](/deployedge/microsoft-edge-policies#configureviewinfileexplorer) e atualizar a configuração de locatário do SharePoint Online. Saiba mais: Exibir SharePoint arquivos com o Explorador de [Arquivos no Microsoft Edge - SharePoint no Microsoft 365 | Microsoft Docs](/SharePoint/sharepoint-view-in-edge).

- **Os links da URL do arquivo de zona da intranet serão abertos Windows Explorador de Arquivos.**  Você pode permitir que links de URL de arquivo para arquivos de zona de intranet provenientes de sites HTTPS da zona de intranet abram Windows Explorador de Arquivos para esse arquivo ou diretório. Você pode habilitar essa experiência usando a [política IntranetFileLinksEnabled.](/deployedge/microsoft-edge-policies#intranetfilelinksenabled)

- **Melhorias na experiência de downloads.**  O suporte para a experiência do usuário de download está sendo estendido para aplicativos Web progressivos PWAs e WebView. Também vamos começar a dar suporte a arrastar e soltar para o Explorador de Arquivos e Área de Trabalho.

- **Pick up where you left off on PDF documents.**  Agora você poderá retomar a leitura de onde fechou o documento PDF pela última vez.

- **O modo de eficiência estende a duração da bateria quando o laptop entra no modo de economia de bateria.**  O modo de eficiência se tornará ativo quando o laptop entrar no modo de economia de bateria para permitir que o navegador gerencie o uso de recursos para estender a vida útil da bateria do computador. Você terá quatro opções para quando o modo de eficiência se tornar ativo, Unplugged e bateria baixa, Unplugged, Always e Never. Observação: esta é uma Distribuição de Recursos Controlados. Dispositivos com bateria devem ter o recurso ligado.

***Novas Políticas***

- [BrowserLegacyExtensionPointsBlockingEnabled](/DeployEdge/microsoft-edge-policies#browserlegacyextensionpointsblockingenabled) Habilitar o bloqueio de ponto de extensão herdado do navegador
- [CrossOriginWebAssemblyModuleSharingEnabled](/DeployEdge/microsoft-edge-policies#crossoriginwebassemblymodulesharingenabled) Especifica se os módulos WebAssembly podem ser enviados de origem cruzada
- [DisplayCapturePermissionsPolicyEnabled](/DeployEdge/microsoft-edge-policies#displaycapturepermissionspolicyenabled) Especifica se a política de permissões de captura de exibição está marcada ou ignorada
- [InternetExplorerIntegrationWindowOpenHeightAdjustment](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationwindowopenheightadjustment) Configurar o ajuste de pixel entre window.open heights de páginas do modo IE vs. Páginas de modo de borda
- [InternetExplorerIntegrationWindowOpenWidthAdjustment](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationwindowopenwidthadjustment) Configurar o ajuste de pixel entre as larguras window.open origem das páginas do modo IE versus páginas de modo de borda
- [IntranetFileLinksEnabled](/DeployEdge/microsoft-edge-policies#intranetfilelinksenabled) Permitir que links de URL de arquivo de zona de intranet Microsoft Edge abrir no Windows Explorador de Arquivos
- [ShadowStackCrashRollbackBehavior](/DeployEdge/microsoft-edge-policies#shadowstackcrashrollbackbehavior) Configurar o comportamento de rebaixamento de falha do ShadowStack
- [VisualSearchEnabled](/DeployEdge/microsoft-edge-policies#visualsearchenabled) Pesquisa visual habilitada

***Políticas Obsoletas***

- [InternetExplorerIntegrationTestingAllowed](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationtestingallowed) - Permitir teste no modo Internet Explorer.
- [LegacySameSiteCookieBehaviorEnabled](/DeployEdge/microsoft-edge-policies#legacysamesitecookiebehaviorenabled) Habilitar configuração padrão de comportamento de cookie SameSite herdado

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

- **Caixas de texto de formulário gratuito adicionadas a documentos PDF.**  Agora, temos suporte para adicionar caixas de texto de formulário gratuitos a documentos PDF que você pode usar para preencher formulários e adicionar anotações visíveis.

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

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-92090222-june-21"></a>Versão 92.0.902.22: 21 de junho

### <a name="feature-updates"></a>Atualizações de recursos

- **Pesquisa de idioma natural para o histórico do navegador na barra de endereços**. Localizar o artigo/site que você está procurando agora é mais fácil graças à pesquisa de idioma natural na barra de endereços. Você pode encontrar resultados de pesquisa com base no conteúdo/descrição/tempo da página (como "receita de torta da semana passada") além de títulos/url de palavras-chave.
Observação: esta é uma Distribuição de Recursos Controlados. Se você não localizar esse recurso, volte em breve enquanto continuamos nossa distribuição.

- **Os usuários podem acessar facilmente o modo Internet Explorer no Microsoft Edge**. A partir da versão 92 do Microsoft Edge, os usuários podem recarregar um site no modo Internet Explorer no Microsoft Edge em vez de depender do aplicativo autônomo do IE 11 enquanto aguardam a configuração de um site na Lista de Sites do Modo Empresarial. Os usuários serão solicitados a adicionar o site à sua lista de sites locais de forma que a navegação para a mesma página no Microsoft Edge seja renderizada automaticamente no modo IE pelos próximos 30 dias. Você pode usar a política *[InternetExplorerIntegrationReloadInIEModeAllowed](/deployedge/microsoft-edge-policies#internetexplorerintegrationreloadiniemodeallowed)* para configurar essa experiência e permitir o acesso aos pontos de entrada do modo IE, bem como a capacidade de adicionar sites à lista de sites locais. Você pode usar a política *[InternetExplorerIntegrationLocalSiteListExpirationDays](/deployedge/microsoft-edge-policies#internetexplorerintegrationlocalsitelistexpirationdays)* para ajustar o número de dias para manter os sites na lista de sites locais.
Observe que KB5003698 ou posterior é necessário para Windows 10, versão 1909; ou KB5003690 ou posterior é necessário para Windows 10, versão 2004, Windows 10, versão 20H2 ou Windows 10, versão 21H1 para a experiência de ponta a ponta.

- **Os arquivos MHTML serão abertos por padrão no modo Internet Explorer**. A partir do Microsoft Edge versão 92 Estável, os tipos de arquivo MHTML serão abertos automaticamente no modo Internet Explorer no Microsoft Edge em vez do aplicativo Internet Explorer (IE11). Isso é mais comumente observado ao tentar visualizar emails do Outlook em um navegador. Essa alteração ocorrerá apenas se o IE11 for o manipulador padrão para este tipo de arquivo. Se preferir alterar isso, você pode fazer isso antes de instalar a atualização da versão 92 Estável usando [este guia](/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration).

- **Os instrumentos de pagamento agora são sincronizados entre dispositivos**. A partir do Microsoft Edge versão 92, você tem a opção de sincronizar suas informações de pagamento em seus dispositivos conectados.
Observação: esta é uma Distribuição de Recursos Controlados. Se você não vir esse recurso, volte logo à medida que continuarmos nossa versão.

- **O aviso "Desabilitar extensões do modo de desenvolvedor" pode ser descartado permanentemente**. A partir da versão 92 do Microsoft Edge, você pode desabilitar o aviso "Desabilitar extensões do modo de desenvolvedor" clicando na opção 'Não mostrar novamente'.
Observação: esta é uma Distribuição de Recursos Controlados. Se você não vir esse recurso, volte logo à medida que continuarmos nossa versão.

- **Gerenciar suas extensões diretamente da barra de ferramentas**. O novo menu de extensões na barra de ferramentas permitirá que você oculte/fixe extensões facilmente. Os links rápidos para gerenciar extensões e encontrar novas extensões facilitarão a localização de novas extensões e o gerenciamento das existentes.
Observação: esta é uma Distribuição de Recursos Controlados. Se você não vir esse recurso, volte logo à medida que continuarmos nossa versão.

- **HTTPS automático**. Os usuários terão a opção de atualizar a navegação de HTTP para HTTPS em domínios que provavelmente suportam este protocolo mais seguro. Esse suporte também pode ser configurado para tentar entrega HTTPS para todos os domínios.
Observação: estamos testando esse recurso e esse comportamento não será detectado se você tiver desativado os experimentos.

- **Melhorias na renderização de fontes**. Foram feitas melhorias na renderização do texto para melhorar a clareza e reduzir o borrão.
Observação: esta é uma Distribuição de Recursos Controlados. Se você não vir esse recurso, volte logo à medida que continuarmos nossa versão.

### <a name="policy-updates"></a>Atualizações de política

#### <a name="new-policies"></a>Novas políticas

Oito novas políticas foram adicionadas. Baixe os Modelos Administrativos atualizados da [página de aterrissagem do Microsoft Edge Empresa](https://www.microsoft.com/edge/business/download). Foram adicionadas as novas políticas a seguir:

- [AADWebSiteSSOUsingThisProfileEnabled](/DeployEdge/microsoft-edge-policies#aadwebsitessousingthisprofileenabled)Logon único para sites de trabalho ou escola usando este perfil habilitado.
- [AutomaticHttpsDefault](/DeployEdge/microsoft-edge-policies#automatichttpsdefault) Configurar HTTPS Automático
- [HeadlessModeEnabled](/DeployEdge/microsoft-edge-policies#headlessmodeenabled) Controle o uso do Modo Sem Periféricos
- [InsecurePrivateNetworkRequestsAllowed](/DeployEdge/microsoft-edge-policies#insecureprivatenetworkrequestsallowed) Especifica se é possível permitir que sites inseguros façam solicitações para pontos de extremidade de rede mais privados
- [InsecurePrivateNetworkRequestsAllowedForUrls](/DeployEdge/microsoft-edge-policies#insecureprivatenetworkrequestsallowedforurls) Permite que os sites listados façam solicitações para pontos de extremidade de rede mais privada a partir de contextos inseguros
- [InternetExplorerIntegrationLocalSiteListExpirationDays](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationlocalsitelistexpirationdays) Especifique o número de dias que um site permanece na lista de sites do modo IE local
- [InternetExplorerIntegrationReloadInIEModeAllowed](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationreloadiniemodeallowed) Permite que sites não configurados sejam recarregados no modo Internet Explorer
- [SharedArrayBufferUnrestrictedAccessAllowed](/DeployEdge/microsoft-edge-policies#sharedarraybufferunrestrictedaccessallowed) Especifica se SharedArrayBuffers pode ser usado em um contexto não isolado de origem cruzada

#### <a name="obsoleted-policy"></a>Política Obsoleta

- [EnableSha1ForLocalAnchors](/DeployEdge/microsoft-edge-policies#enablesha1forlocalanchors) Permitir certificados assinados usando SHA-1 quando emitidos por âncoras de confiança locais.

## <a name="version-9209029-june-8"></a>Versão 92.0.902.9: 8 de junho

Vários bugs corrigidos e problemas de desempenho.

## <a name="version-91086441-june-3"></a>Versão 91.0.864.41: 3 de junho

Vários bugs corrigidos e problemas de desempenho.

## <a name="version-91086437-may-27"></a>Versão 91.0.864.37: 27 de maio

Vários bugs corrigidos e problemas de desempenho.

## <a name="version-91086436-may-26"></a>Versão 91.0.864.36: 26 de maio

Vários bugs corrigidos e problemas de desempenho.

## <a name="version-91086433-may-21"></a>Versão 91.0.864.33: 21 de maio

Vários bugs corrigidos e problemas de desempenho.

## <a name="version-91086427-may-14"></a>Versão 91.0.864.27: 14 de maio

Vários bugs corrigidos e problemas de desempenho.

## <a name="version-91086419-may-7"></a>Versão 91.0.864.19: 7 de maio

Vários bugs corrigidos e problemas de desempenho.

## <a name="version-91086415-may-3"></a>Versão 91.0.864.15: 3 de maio

Vários bugs corrigidos e problemas de desempenho.

## <a name="version-91086411-april-30"></a>Versão 91.0.864.11: 30 de abril

### <a name="feature-updates"></a>Atualizações de recursos

- **Identifique o tráfego de rede originado dos contêineres do Microsoft Defender Application Guard no nível do proxy**. A partir da versão 91 do Microsoft Edge, há suporte integrado para marcar o tráfego de rede originado de contêineres do Application Guard, permitindo que as empresas os identifiquem e apliquem políticas específicas.

- **Opção de suporte para permitir a sincronização de favoritos do host para o contêiner do Edge Application Guard**. A partir do Microsoft Edge versão 91, os usuários têm a opção de configurar o Application Guard para sincronizar seus favoritos do host para o contêiner. Isso garante que novos favoritos também apareçam no contêiner.

- **Suporte para APIs de Reconhecimento de Fala**. A partir da versão 91 do Microsoft Edge, o suporte API para comandos de reconhecimento de voz no Google.com e sites semelhantes será adicionado. Este recurso é limitado a um grupo selecionado aleatoriamente de usuários que habilitaram a experimentação. Esses usuários estão fazendo comentários para a equipe de recursos.

- **Personalize seu navegador com novas cores de tema**. Personalize o Microsoft Edge com uma das quatorze novas cores de tema na página Configurações -> Aparência. Você também pode instalar temas personalizados do site do Complemento do Microsoft Edge. [Saber mais](https://techcommunity.microsoft.com/t5/articles/make-microsoft-edge-your-own-with-themes/m-p/2083165)

- **Interromper Downloads** A partir do Microsoft Edge versão 91, o navegador interromperá automaticamente os downloads de tipos que podem danificar seu computador se esses downloads forem iniciados sem a interação do usuário e não forem suportados pela verificação de Reputação do Aplicativo SmartScreen. Os usuários podem substituir e continuar o download clicando com o botão direito e escolhendo “Manter” no item de download.
Os administradores de empresas podem optar por não adotar esse comportamento por uma destas duas políticas:
    - [ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](/deployedge/microsoft-edge-policies#exemptdomainfiletypepairsfromfiletypedownloadwarnings) - Desabilitar avisos baseados em extensão de tipo de arquivo de download para tipos de arquivo especificados em domínios. Para obter mais informações, confira [Interrupções de downloads do Microsoft Edge Security](/deployedge/microsoft-edge-security-downloads-interruptions)

### <a name="policy-updates"></a>Atualizações de política

#### <a name="new-policies"></a>Novas políticas

Seis novas políticas foram adicionadas. Baixe os Modelos Administrativos atualizados da [página de aterrissagem do Microsoft Edge Empresa](https://www.microsoft.com/edge/business/download). Foram adicionadas as novas políticas a seguir:

- [ApplicationGuardTrafficIdentificationEnabled](/DeployEdge/microsoft-edge-policies#applicationguardtrafficidentificationenabled) - Identificação de Tráfego do Application Guard
- [ExplicitlyAllowedNetworkPorts](/DeployEdge/microsoft-edge-policies#explicitlyallowednetworkports) - Portas de rede explicitamente permitidas
- [ImportStartupPageSettings](/DeployEdge/microsoft-edge-policies#importstartuppagesettings) - Permitir a importação das configurações da página de inicialização
- [MathSolverEnabled](/DeployEdge/microsoft-edge-policies#mathsolverenabled) - Permite que os usuários capturem um problema de matemática e obtenham a solução com uma explicação passo a passo no Microsoft Edge
- [NewTabPageContentEnabled](/DeployEdge/microsoft-edge-policies#newtabpagecontentenabled) - Permitir conteúdo do Microsoft News na página nova guia
- [NewTabPageQuickLinksEnabled](/DeployEdge/microsoft-edge-policies#newtabpagequicklinksenabled) - Permitir links rápidos na página nova guia

#### <a name="obsoleted-policy"></a>Política Obsoleta

- [ProactiveAuthEnabled](./microsoft-edge-policies.md#proactiveauthenabled) - Habilitar Autenticação Proativa
<!-- end major 91 -->

## <a name="version-90081846-april-22"></a>Versão 90.0.818.46: 22 de abril

Vários bugs corrigidos e problemas de desempenho.

## <a name="version-90081842-april-20"></a>Versão 90.0.818.42: 20 de abril

Vários bugs corrigidos e problemas de desempenho.

## <a name="version-90081841-april-16"></a>Versão 90.0.818.41: 16 de abril

Vários bugs corrigidos e problemas de desempenho.

## <a name="version-90081838-april-14"></a>Versão 90.0.818.38: 14 de abril

Vários bugs corrigidos e problemas de desempenho.

## <a name="version-90081836-april-12"></a>Versão 90.0.818.36: 12 de abril

Vários bugs corrigidos e problemas de desempenho.

## <a name="version-90081827-april-2"></a>Versão 90.0.818.27: 2 de abril

Vários bugs corrigidos e problemas de desempenho.

## <a name="version-90081822-march-29"></a>Versão 90.0.818.22: 29 de março

Vários bugs corrigidos e problemas de desempenho.

## <a name="version-90081814-march-22"></a>Versão 90.0.818.14: 22 de março

Correção de vários bugs e problemas de desempenho.
<!-- begin major 90 -->
## <a name="version-9008188-march-16"></a>Versão 90.0.818.8: 16 de março

### <a name="feature-updates"></a>Atualizações de recursos

- **O Logon Único (SSO) agora está disponível para contas do Azure Active Directory (Azure AD) e conta Microsoft (MSA) no macOS**. Um usuário conectado no Microsoft Edge em macOS agora terá automaticamente acesso aos sites que estão configurados para permitir logon único com as contas Microsoft e Corporativas (por exemplo, bing.com, office.com, msn.com e outlook.com).

- **Modo de quiosque.** A partir do Microsoft Edge versão 90, bloqueamos as configurações de impressão da interface do usuário para permitir apenas as impressoras configuradas e as opções “Imprimir em PDF”. Também fizemos melhorias no modo quiosque de aplicativo único de acesso atribuído para restringir a inicialização de outros aplicativos a partir do navegador. Para obter mais informações sobre os recursos do modo quiosque, clique [aqui](/deployedge/microsoft-edge-configure-kiosk-mode#kiosk-mode-supported-features).

- **Impressão:**

  - **Novo modo de rasterização de impressão para impressoras não PostScript**. A partir da versão 90 do Microsoft Edge, os administradores poderão usar uma nova política para definir o modo de rasterização de impressão para seus usuários. Esta política  controla como o Microsoft Edge imprime para impressoras não PostScript no Windows.  Às vezes, os trabalhos de impressão em impressoras não PostScript precisam ser rasterizados para serem impressos corretamente. As opções de impressão são Completa e Rápida.

  - **Opções adicionais de dimensionamento de página para impressão**. Os usuários agora podem personalizar o dimensionamento enquanto imprimem páginas da Web e documentos PDF usando as opções adicionais. A opção "Ajustar à página" garante que a página da Web ou o documento se ajuste ao espaço disponível no "Tamanho do papel" selecionado para impressão. A opção "Tamanho real" garante que não ocorram mudanças no tamanho do conteúdo que está sendo impresso, independentemente do "Tamanho do papel" selecionado.

- **Produtividade:**

  - **As sugestões de preenchimento automático são estendidas para incluir o conteúdo dos campos de endereço da área de transferência**. O conteúdo da área de transferência é analisado quando você clica em um campo de perfil/endereço (por exemplo, telefone, email, CEP, cidade, estado, etc.) para mostrar como sugestões de preenchimento automático.

  - **Os usuários podem pesquisar sugestões de preenchimento automático mesmo se um formulário ou campo não for detectado**. Hoje, se você tiver suas informações salvas no Microsoft Edge, as sugestões de preenchimento automático aparecem automaticamente e ajudam você a economizar tempo enquanto preenche formulários. Nos casos em que o preenchimento automático perde um formulário ou se você deseja buscar dados em formulários que normalmente não possuem preenchimento automático (como formulários temporários), você pode pesquisar suas informações usando o preenchimento automático.

- **Acesse downloads a partir de um submenu na barra de menu**. Os downloads aparecerão no canto superior direito com todos os downloads ativos em um só lugar. Este menu é facilmente descartável para que os usuários possam continuar navegando ininterruptamente e possam monitorar o progresso geral do download diretamente da barra de ferramentas. [Saiba mais](https://techcommunity.microsoft.com/t5/articles/introducing-the-new-downloads-experience/m-p/2111551).


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

<!--- Archived from Version 87.0.664.18: October 26 to to version 89.0.774.18: February 3 ---->
<!--- Archived from Version 87.0.664.12: October 20 to to version 86.0.622.15: September 14 ---->
<!--- Archived to version 86.0.622.11: September 9 ---->
<!--- Archived to version 85.0.564.18: July 28 ---->

## <a name="see-also"></a>Ver também

- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
