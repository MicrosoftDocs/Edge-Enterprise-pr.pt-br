---
title: Notas da versão do Microsoft Edge para canal beta
ms.author: aguta
author: dan-wesley
manager: srugh
ms.date: 01/07/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Notas da versão do Microsoft Edge para canal beta
ms.openlocfilehash: ddb745c206dc392dc1dbb46a0522db9648ba624e
ms.sourcegitcommit: e7f3098d8b7d91cae20b5778a71a87daababc312
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/15/2022
ms.locfileid: "12297709"
---
# <a name="release-notes-for-microsoft-edge-beta-channel"></a>Notas de versão do canal do Microsoft Edge beta

Estas notas de versão fornecem informações sobre os novos recursos e atualizações não relacionadas à segurança que estão inclusos no canal Beta do Microsoft Edge. As versões arquivadas dessas notas de versão estão disponíveis em Notas de versão arquivadas [para Microsoft Edge Beta Channel](./microsoft-edge-relnote-archive-beta-channel.md).

> [!NOTE]
> A Plataforma da Web do Microsoft Edge evolui constantemente para melhorar a experiência, segurança e privacidade do usuário. Para saber mais, confira [Compatibilidade de sites: alterações que afetam o Microsoft Edge](/microsoft-edge/web-platform/site-impacting-changes).

## <a name="version-970107254-january-5"></a>Versão 97.0.1072.54: 5 de janeiro

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-970107252-january-3"></a>Versão 97.0.1072.52: 3 de janeiro

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-970107241-december-20"></a>Versão 97.0.1072.41: 20 de dezembro

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-970107234-december-13"></a>Versão 97.0.1072.34: 13 de dezembro

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-970107228-december-8"></a>Versão 97.0.1072.28: 8 de dezembro

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-970107221-december-1"></a>Versão 97.0.1072.21: 1 de dezembro

### <a name="feature-updates"></a>Atualizações de recursos

- **Use o perfil atual para entrar em sites quando várias contas de trabalho ou de estudante estão conectados em um dispositivo.** Quando várias contas de trabalho ou de estudante são assinadas em um dispositivo, os usuários serão solicitados a escolher uma conta no selador de conta para continuar suas visitas aos sites. Nesta versão, os usuários serão solicitados a permitir Microsoft Edge entrar nos sites automaticamente com a conta de trabalho e de estudante que está assinada no perfil atual. Os usuários podem ativar e desativar esse recurso **em preferências Configurações/Perfil.**

- **Adicione suporte para a Prevenção contra Perda de Dados do Microsoft Endpoint (DLP) no macOS.** A aplicação da política de DLP do Ponto de Extremidade da Microsoft está disponível de forma nativa no macOS.

- **Abra arquivos PDF assinados digitalmente.**  Assinaturas digitais são usadas extensivamente para validar a autenticidade de e alterações em um documento. Os usuários podem validar as assinaturas para arquivos PDF diretamente do navegador, sem a necessidade de nenhum complemento.

- **Citações em Microsoft Edge.** As fontes de referência para pesquisa são um requisito comum para os alunos. Eles precisam gerenciar muitas referências e fontes de pesquisa, que não são tarefas fáceis. Eles também precisam traduzir essas citações para formatos de citação apropriados, como APA, MLA e Chicago. Esse novo recurso "Citações" no Microsoft Edge (agora em Visualização) oferece aos alunos uma melhor maneira de gerenciar e gerar citações à medida que pesquisam online. Com citações ativas em Coleções ou Configurações e mais **(Alt-F),** o Microsoft Edge gera automaticamente citações que os alunos podem usar posteriormente para que possam se concentrar em suas pesquisas. Quando terminarem, eles podem compilar facilmente essas citações em um produto final. Para obter mais informações, consulte [Previewing Citations in Microsoft Edge](https://blogs.windows.com/msedgedev/2021/11/04/preview-citations-feature-edge/).

### <a name="policy-updates"></a>Atualizações de política

#### <a name="new-policies"></a>Novas Políticas

- [AccessibilityImageLabelsEnabled](/DeployEdge/microsoft-edge-policies#accessibilityimagelabelsenabled) - Obter Descrições de Imagem da Microsoft Habilitada
- [CORSNonWildcardRequestHeadersSupport](/DeployEdge/microsoft-edge-policies#corsnonwildcardrequestheaderssupport) - Suporte ao header de solicitação não curinga do CORS habilitado
- [EdgeDiscoverEnabled](/DeployEdge/microsoft-edge-policies#edgediscoverenabled) - Recurso Descobrir no Microsoft Edge
- [EdgeEnhanceImagesEnabled](/DeployEdge/microsoft-edge-policies#edgeenhanceimagesenabled) - Aprimorar imagens habilitadas
- [InternetExplorerModeTabInEdgeModeAllowed](/DeployEdge/microsoft-edge-policies#internetexplorermodetabinedgemodeallowed) - Permitir que os sites configurados para o modo Internet Explorer abram no Microsoft Edge
- [SameOriginTabCaptureAllowedByOrigins](/DeployEdge/microsoft-edge-policies#sameorigintabcaptureallowedbyorigins) - Permitir a captura da guia Mesma Origem por essas origens
- [ScreenCaptureAllowedByOrigins](/DeployEdge/microsoft-edge-policies#screencaptureallowedbyorigins) - Permitir captura de desktop, janela e tabulação por essas origens
- [SerialAllowAllPortsForUrls](/DeployEdge/microsoft-edge-policies#serialallowallportsforurls) - Conceder automaticamente permissão aos sites para conectar todas as portas seriais
- [SerialAllowUsbDevicesForUrls](/DeployEdge/microsoft-edge-policies#serialallowusbdevicesforurls) - Conceder automaticamente permissão aos sites para se conectar a dispositivos seriais USB
- [SmartScreenDnsRequestsEnabled](/DeployEdge/microsoft-edge-policies#smartscreendnsrequestsenabled) - Habilitar Microsoft Defender SmartScreen de DNS
- [TabCaptureAllowedByOrigins](/DeployEdge/microsoft-edge-policies#tabcaptureallowedbyorigins) - Permitir captura de tabulação por essas origens
- [WebSQLInThirdPartyContextEnabled](/DeployEdge/microsoft-edge-policies#websqlinthirdpartycontextenabled) - Force WebSQL em contextos de terceiros a serem reabilitar
- [WindowCaptureAllowedByOrigins](/DeployEdge/microsoft-edge-policies#windowcaptureallowedbyorigins) - Permitir captura de janela e tabulação por essas origens

## <a name="version-960105434-november-23"></a>Versão 96.0.1054.34: 23 de novembro

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-960105426-november-17"></a>Versão 96.0.1054.26: 17 de novembro

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-960105424-november-16"></a>Versão 96.0.1054.24: 16 de novembro

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-960105413-november-5"></a>Versão 96.0.1054.13: 5 de novembro

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-96010548-november-1"></a>Versão 96.0.1054.8: 1 de novembro

### <a name="feature-updates"></a>Atualizações de recursos

- **Iniciar o Progressive Web App (PWA) diretamente por meio de links de protocolo.** Permitir que os PWAs instalados manipularem links que usam um protocolo específico para uma experiência mais integrada.

- **Saiba como resolver problemas de matemática com o Solver de Matemática.** Estamos animados em anunciar que você pode usar o Resolvedor de Matemática Microsoft Edge obter ajuda com uma ampla variedade de conceitos matemáticos. Esses conceitos variam de equações aritméticas e quadráticas primárias a trigonometria e cálculo. O Solver de Matemática permite que você tire uma foto de um problema de matemática manuscrita ou impressa e, em seguida, fornece uma solução instantânea com instruções passo a passo para ajudá-lo a aprender a alcançar a solução sem ajuda. O Math Solver também vem com um teclado matemático que você pode usar para digitar facilmente problemas matemáticos. Esse teclado elimina a necessidade de pesquisar em torno de um teclado tradicional para encontrar os caracteres matemáticos necessários. Depois de resolver seu problema, o Math Solver fornece opções para continuar a aprender com quizzes, planilhas e tutoriais de vídeo.

- **Realçamento de forma livre em PDFs.** A experiência de exibição e marcação em PDF é aprimorada com a adição de realçadores de forma livre. Você pode realçar seções em PDFs que não têm acesso e documentos verificados.

- **Proteção de Pilha imposta por hardware.**  Microsoft Edge começar a oferecer suporte a um modo de navegação ainda mais seguro que usa o fluxo de controle dependente de hardware para processos do navegador em hardware suportado (Intel 11th Gen. ou AMD Zen 3). Observação: como se trata de uma Rollout de Recursos Controlados, talvez você não perceba que esse recurso está habilitado em todos os dispositivos. Você pode habilitar ou desabilitar a Proteção de Pilha imposta por hardware manipulando o IFEO (Image File Execution Options) usando a política de grupo.

- **Nova caixa de diálogo de aviso para sites typosquatting.** O navegador agora mostrará um aviso em alguns sites com URLs semelhantes a outros sites. Essa interface do usuário usa heurísticas do lado do cliente para avisar os usuários sobre sites que podem estar spoofando sites populares. Para obter mais informações, consulte [O que é typosquatting?](https://support.microsoft.com/topic/what-is-typosquatting-54a18872-8459-4d47-b3e3-d84d9a362eb0).

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

Correção de vários bugs e problemas de desempenho.

<!-- archive from version 95.0.1020.9: September 28 to version 94.0.992.14: September 7 ---->
<!-- archive from Version 94.0.992.9: September 2 to Version 92.0.902.40: July 6 -->
<!--Archive on Oct 27 From Version 92.0.902.22: June 21 to Version 89.0.774.23: February 8  -->
<!--- Archived from Version 87.0.664.18: October 26 to to version 89.0.774.18: February 3 ---->
<!--- Archived from Version 87.0.664.12: October 20 to to version 86.0.622.15: September 14 ---->
<!--- Archived to version 86.0.622.11: September 9 ---->
<!--- Archived to version 85.0.564.18: July 28 ---->

## <a name="see-also"></a>Ver também

- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
