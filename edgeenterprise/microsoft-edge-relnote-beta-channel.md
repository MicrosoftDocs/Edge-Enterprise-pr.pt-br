---
title: Notas da versão do Microsoft Edge para canal beta
ms.author: aguta
author: dan-wesley
manager: srugh
ms.date: 11/03/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Notas da versão do Microsoft Edge para canal beta
ms.openlocfilehash: bcc2ecf91c6d90443de26b5bff1c744d7582aa18
ms.sourcegitcommit: 4ec03873a85f065d9bfa6203cfe6c3e938f79bc5
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2021
ms.locfileid: "12155098"
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

- **Handoff aprimorado entre o modo IE e o navegador moderno.**  A partir dessa versão do Microsoft Edge, as navegação entre o Microsoft Edge e o modo Internet Explorer incluirão dados de formulário e cabeçalhos HTTP adicionais. Os headers de referência, os dados postados, os dados de formulários e os métodos de solicitação serão encaminhados corretamente entre as duas experiências. Você pode especificar quais tipos de dados devem ser incluídos usando a [política InternetExplorerIntegrationComplexNavDataTypes.](/deployedge/microsoft-edge-policies#internetexplorerintegrationcomplexnavdatatypes) Para obter mais informações, consulte esta perguntas frequentes: Meu aplicativo requer a transferência de dados POST entre o [modo IE e Microsoft Edge](./edge-ie-mode-faq.md#my-application-requires-transferring-post-data-between-ie-mode-and-microsoft-edge-is-this-supported).

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

Correção de vários bugs e problemas de desempenho.

<!-- archive from Version 94.0.992.9: September 2 to Version 92.0.902.40: July 6 -->
<!--Archive on Oct 27 From Version 92.0.902.22: June 21 to Version 89.0.774.23: February 8  -->
<!--- Archived from Version 87.0.664.18: October 26 to to version 89.0.774.18: February 3 ---->
<!--- Archived from Version 87.0.664.12: October 20 to to version 86.0.622.15: September 14 ---->
<!--- Archived to version 86.0.622.11: September 9 ---->
<!--- Archived to version 85.0.564.18: July 28 ---->

## <a name="see-also"></a>Ver também

- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
