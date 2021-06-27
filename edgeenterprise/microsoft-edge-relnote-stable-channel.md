---
title: Notas de versão do Microsoft Edge para Stable Channel
ms.author: aguta
author: AndreaLBarr
manager: srugh
ms.date: 06/24/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Notas de versão do Microsoft Edge para Stable Channel
ms.openlocfilehash: ef059624339f4b50b92fb187023991ae0526afa7
ms.sourcegitcommit: 4192328ee585bc32a9be528766b8a5a98e046c8e
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/25/2021
ms.locfileid: "11617941"
---
# <a name="release-notes-for-microsoft-edge-stable-channel"></a>Notas de versão do Microsoft Edge Stable Channel

Essas notas de versão fornecem informações dos novos recursos e atualizações não relacionados à segurança que estão inclusos Microsoft Edge Stable Channel.

- Todas as atualizações de segurança estão listadas [aqui](microsoft-edge-relnotes-security.md).
- As notas de versão arquivadas do Canal Estável do Microsoft Edge estão localizadas [aqui](microsoft-edge-relnote-archive-stable-channel.md).

 Para entender os canais do Microsoft Edge, confira a [Visão geral dos canais do Microsoft Edge](microsoft-edge-channels.md).

> [!NOTE]
> Para o Canal Estável, as atualizações serão implantadas progressivamente por um ou mais dias. Para saber mais, consulte [Distribuições progressivas para atualizações do Microsoft Edge](microsoft-edge-update-progressive-rollout.md).
>
> A Plataforma da Web do Microsoft Edge evolui constantemente para melhorar a experiência, segurança e privacidade do usuário. Para saber mais, confira [Alterações que afetam a compatibilidade do site chegando ao Microsoft Edge](/microsoft-edge/web-platform/site-impacting-changes).

## <a name="version-91086459-june-24"></a>Versão 91.0.864.59: 24 de junho

As atualizações de segurança do canal estável estão listadas [aqui](/deployedge/microsoft-edge-relnotes-security#june-24-2021).

## <a name="version-91086454-june-18"></a>Versão 91.0.864.54: 18 de junho

> [!Important]
> Esta atualização contém [CVE-2021-30554](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-30554) que foi relatada pela equipe do Chromium como tendo uma exploração na natureza. Para obter mais informações, confira o [Guia de Atualização de Segurança](https://msrc.microsoft.com/update-guide/vulnerability/ADV200002).

As atualizações de segurança do canal estável estão listadas [aqui](/deployedge/microsoft-edge-relnotes-security#june-18-2021).

## <a name="version-91086448-june-11"></a>Versão 91.0.864.48: 11 de junho

> [!Important]
>Esta atualização contém [CVE-2021-30551](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-30551) que foi relatada pela equipe do Chromium como tendo uma exploração na natureza. Para obter mais informações, confira o [Guia de Atualização de Segurança](https://msrc.microsoft.com/update-guide/vulnerability/ADV200002).

As atualizações de segurança do canal estável estão listadas [aqui](/deployedge/microsoft-edge-relnotes-security#june-11-2021).

## <a name="version-91086441-june-3"></a>Versão 91.0.864.41: 3 de junho

As atualizações de segurança do canal estável estão listadas [aqui](/deployedge/microsoft-edge-relnotes-security#june-3-2021).

## <a name="version-91086437-may-27"></a>Versão 91.0.864.37: 27 de maio

As atualizações de segurança do canal estável estão listadas [aqui](/deployedge/microsoft-edge-relnotes-security#may-27-2021).

### <a name="feature-updates"></a>Atualizações de recursos

- **Identifique o tráfego de rede originado dos contêineres do Microsoft Defender Application Guard no nível do proxy**. A partir da versão 91 do Microsoft Edge, há suporte integrado para marcar o tráfego de rede originado de contêineres do Application Guard, permitindo que as empresas os identifiquem e apliquem políticas específicas.

- **Opção de suporte para permitir a sincronização de favoritos do host para o contêiner do Edge Application Guard**. A partir do Microsoft Edge versão 91, os usuários têm a opção de configurar o Application Guard para sincronizar seus favoritos do host para o contêiner. Isso garante que novos favoritos também apareçam no contêiner.

- **A partir do Microsoft Edge versão 91, o navegador interromperá automaticamente os downloads de tipos que podem danificar seu computador se esses downloads forem iniciados sem a interação do usuário e não forem suportados pela verificação de Reputação de Aplicativo SmartScreen**. Os usuários podem substituir e continuar o download clicando com o botão direito e escolhendo “Manter” no item de download. Os administradores corporativos podem recusar esse comportamento configurando a seguinte política:
  - [ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](/deployedge/microsoft-edge-policies#exemptdomainfiletypepairsfromfiletypedownloadwarnings.md): Desabilita o download de avisos baseados em extensão do tipo de arquivo para tipos de arquivo especificados em domínios.

    Para obter mais informações, consulte [Interrupções de downloads na Segurança do Microsoft Edge](microsoft-edge-security-downloads-interruptions.md).

- **Suporte para APIs de Reconhecimento de Fala**. A partir da versão 91 do Microsoft Edge, o suporte API para comandos de reconhecimento de voz no Google.com e sites semelhantes será adicionado. Este recurso é limitado a um grupo selecionado aleatoriamente de usuários que habilitaram a experimentação. Esses usuários estão fazendo comentários para a equipe de recursos.

- **Personalize seu navegador com novas cores de tema**. Personalize o Microsoft Edge com uma das quatorze novas cores de tema na página Configurações -> Aparência. Você também pode instalar temas personalizados do site do Complemento do Microsoft Edge. [Saiba mais](https://techcommunity.microsoft.com/t5/articles/make-microsoft-edge-your-own-with-themes/m-p/2083165)

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

- [ProactiveAuthEnabled](./microsoft-edge-policies.md#proactiveauthenabled): habilita a Autenticação Proativa
<!-- end major 91 -->

## <a name="version-90081866-may-20"></a>Versão 90.0.818.66: 20 de maio

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-90081862-may-13"></a>Versão 90.0.818.62: 13 de maio

As atualizações de segurança do canal estável estão listadas [aqui](/deployedge/microsoft-edge-relnotes-security#may-13-2021).

## <a name="version-90081856-may-6"></a>Versão 90.0.818.56: 6 de maio

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-90081851-april-29"></a>Versão 90.0.818.51: 29 de abril

As atualizações de segurança do canal estável estão listadas [aqui](/deployedge/microsoft-edge-relnotes-security#april-29-2021).

## <a name="version-90081849-april-26"></a>Versão 90.0.818.49: 26 de abril

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-90081846-april-22"></a>Versão 90.0.818.46: 22 de abril ##

As atualizações de segurança do canal estável estão listadas [aqui](/deployedge/microsoft-edge-relnotes-security#april-22-2021).

## <a name="version-90081842-april-19"></a>Versão 90.0.818.42: 19 de abril

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-90081841-april-16"></a>Versão 90.0.818.41: 16 de abril ##

> [!Important]
>Esta atualização contém [CVE-2021-21224](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-21224) que foi relatada pela equipe do Chromium como tendo uma exploração na natureza. Para obter mais informações, confira o [Guia de Atualização de Segurança](https://msrc.microsoft.com/update-guide).

As atualizações de segurança do canal estável estão listadas [aqui](/deployedge/microsoft-edge-relnotes-security#april-16-2021).

## <a name="version-90081839-april-15"></a>Versão 90.0.818.39: 15 de abril ##

As atualizações de segurança do canal estável estão listadas [aqui](/deployedge/microsoft-edge-relnotes-security#april-15-2021).

## <a name="feature-updates"></a>Atualizações de recursos ##

-    **O Logon Único (SSO) agora está disponível para contas do Azure Active Directory (Azure AD) e conta Microsoft (MSA) no macOS.** Um usuário conectado no Microsoft Edge em macOS agora terá automaticamente acesso aos sites que estão configurados para permitir logon único com as contas Microsoft e Corporativas (por exemplo, bing.com, office.com, msn.com e outlook.com).

- **Modo de quiosque.** A partir do Microsoft Edge versão 90, bloqueamos as configurações de impressão da interface do usuário para permitir apenas as impressoras configuradas e as opções “Imprimir em PDF”. Também fizemos melhorias no modo quiosque de aplicativo único de acesso atribuído para restringir a inicialização de outros aplicativos a partir do navegador. Para obter mais informações sobre os recursos do modo quiosque, clique [aqui](/deployedge/microsoft-edge-configure-kiosk-mode#kiosk-mode-supported-features).

- **Interromper Downloads**: a partir do Microsoft Edge versão 91, o navegador interromperá automaticamente os downloads de tipos que podem danificar seu computador se esses downloads forem iniciados sem a interação do usuário e não forem suportados pela verificação de Reputação do Aplicativo SmartScreen. Os usuários podem substituir e continuar o download clicando com o botão direito e escolhendo “Manter” no item de download.
Os administradores de empresas podem optar por não adotar esse comportamento por uma destas duas políticas:
- [ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](/deployedge/microsoft-edge-policies#exemptdomainfiletypepairsfromfiletypedownloadwarnings): desabilita avisos baseados em extensão de tipo de arquivo de download para tipos de arquivo especificados em domínios. Para obter mais informações, confira [Interrupções de downloads da Segurança do Microsoft Edge](/deployedge/microsoft-edge-security-downloads-interruptions)

- **Impressão**:

    - **Novo modo de rasterização de impressão para impressoras não PostScript.** A partir da versão 90 do Microsoft Edge, os administradores poderão usar uma nova política para definir o modo de rasterização de impressão para seus usuários. Esta política  controla como o Microsoft Edge imprime para impressoras não PostScript no Windows. Às vezes, os trabalhos de impressão em impressoras não PostScript precisam ser rasterizados para serem impressos corretamente. As opções de impressão são Completa e Rápida.
    
  - **Opções adicionais de dimensionamento de página para impressão.** Os usuários agora podem personalizar o dimensionamento enquanto imprimem páginas da Web e documentos PDF usando as opções adicionais. A opção "Ajustar à página" garante que a página da Web ou o documento se ajuste ao espaço disponível no "Tamanho do papel" selecionado para impressão. A opção "Tamanho real" garante que não ocorram mudanças no tamanho do conteúdo que está sendo impresso, independentemente do "Tamanho do papel" selecionado.

-   **Produtividade:**

    -   **As sugestões de preenchimento automático são estendidas para incluir o conteúdo dos campos de endereço da área de transferência.** O conteúdo da área de transferência é analisado quando você clica em um campo de perfil/endereço (por exemplo, telefone, email, CEP, cidade, estado, etc.) para mostrar como sugestões de preenchimento automático.

    -   **Os usuários podem pesquisar sugestões de preenchimento automático mesmo se um formulário ou campo não for detectado.** Hoje, se você tiver suas informações salvas no Microsoft Edge, as sugestões de preenchimento automático aparecem automaticamente e ajudam você a economizar tempo enquanto preenche formulários. Nos casos em que o preenchimento automático falhar em um formulário ou se você quiser buscar dados em formulários que normalmente não têm preenchimento automático (como formulários temporários), você pode procurar suas informações usando o preenchimento automático.

-   **Acesse downloads a partir de um submenu na barra de menu.** Os downloads aparecerão no canto superior direito com todos os downloads ativos em um só lugar. Este menu é facilmente descartável para que os usuários possam continuar navegando ininterruptamente e possam monitorar o progresso geral do download diretamente da barra de ferramentas. [Saiba mais](https://techcommunity.microsoft.com/t5/articles/introducing-the-new-downloads-experience/m-p/2111551).

-   **Melhorias na renderização de fontes.** A partir da versão 90 do Microsoft Edge, fizemos melhorias na renderização do texto para melhorar a clareza e reduzir o desfocado. Parte das melhorias de renderização da fonte aparecerão na versão Beta 90, mas serão desativadas por padrão.

- **Modo Crianças.** Atualizamos a política para que, quando a política estiver habilitada, ela desabilite o recurso Modo Criança, além da proteção para a família. Saiba mais sobre o Modo Crianças aqui:[aqui](https://go.microsoft.com/fwlink/?linkid=2146910)

## <a name="policy-updates"></a>Atualizações de política

## <a name="new-policies"></a>Novas políticas

Oito novas políticas foram adicionadas. Baixe os Modelos Administrativos atualizados da [página de aterrissagem do Microsoft Edge Empresa](https://www.microsoft.com/edge/business/download). Foram adicionadas as novas políticas a seguir:
-   [ApplicationGuardFavoritesSyncEnabled](/DeployEdge/microsoft-edge-policies#applicationguardfavoritessyncenabled): habilitada a Sincronização de Favoritos do Application Guard
- [ApplicationGuardTrafficIdentificationEnabled](/DeployEdge/microsoft-edge-policies#applicationguardtrafficidentificationenabled): identificação de Tráfego do Application Guard
- [ExplicitlyAllowedNetworkPorts](/DeployEdge/microsoft-edge-policies#explicitlyallowednetworkports): portas de rede explicitamente permitidas
- [ImportStartupPageSettings](/DeployEdge/microsoft-edge-policies#importstartuppagesettings): permite a importação das configurações da página de inicialização
- [MathSolverEnabled](/DeployEdge/microsoft-edge-policies#mathsolverenabled): permite que os usuários capturem um problema de matemática e obtenham a solução com uma explicação passo a passo no Microsoft Edge
- [NewTabPageContentEnabled](/DeployEdge/microsoft-edge-policies#newtabpagecontentenabled): permite conteúdo do Microsoft News na página nova guia
- [NewTabPageQuickLinksEnabled](/DeployEdge/microsoft-edge-policies#newtabpagequicklinksenabled): permite links rápidos na página nova guia
-   [fetch UrlpaliveDurationSecondsOnShutdown](/DeployEdge/microsoft-edge-policies#fetchkeepalivedurationsecondsonshutdown): busca duração keepalive no desligamento
-   [ManagedConfigurationPerOrigin](/DeployEdge/microsoft-edge-policies#managedconfigurationperorigin): define valores de configuração gerenciada para sites de origens específicas
-   [PrintRasterizationMode](/DeployEdge/microsoft-edge-policies#printrasterizationmode) - Modo de Rasterização de Impressão
-   [QuickViewOfficeFilesEnabled](/DeployEdge/microsoft-edge-policies#quickviewofficefilesenabled) - Gerenciar a capacidade de Visualização Rápida de arquivos do Office no Microsoft Edge
-   [SSLErrorOverrideAllowedForOrigins](/DeployEdge/microsoft-edge-policies#sslerroroverrideallowedfororigins) - Permitir que os usuários prossigam a partir da página de aviso HTTPS para origens específicas
-   [WindowOcclusionEnabled](/DeployEdge/microsoft-edge-policies#windowocclusionenabled) - Habilitar Oclusão de Janela
-   [WindowsHelloForHTTPAuthEnabled](/DeployEdge/microsoft-edge-policies#windowshelloforhttpauthenabled) - Windows Hello habilitado para autenticação HTTP

## <a name="deprecated-policies"></a>Políticas preteridas

- [ProactiveAuthEnabled](/DeployEdge/microsoft-edge-policies#proactiveauthenabled): habilita a Autenticação Proativa
-   [NativeWindowOcclusionEnabled](/DeployEdge/microsoft-edge-policies#nativewindowocclusionenabled): habilita a Oclusão de Janela Nativa
-   [SSLVersionMin](/DeployEdge/microsoft-edge-policies#sslversionmin): versão mínima do TLS habilitada

## <a name="version-89077477-april-14"></a>Versão 89.0.774.77: 14 de abril

> [!Important]
>Esta atualização contém [CVE-2021-21206](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-21206) e [CVE-2021-21220](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-21220) que foram relatados pela equipe do Chromium como tendo uma exploração na natureza.  Para obter mais informações, confira o [Guia de Atualização de Segurança](https://msrc.microsoft.com/update-guide).

As atualizações de segurança do canal estável estão listadas [aqui](/deployedge/microsoft-edge-relnotes-security#april-14-2021).

## <a name="version-89077476-april-12"></a>Versão 89.0.774.76: 12 de abril

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-89077475-april-8"></a>Versão 89.0.774.75: 8 de abril

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-89077468-april-1"></a>Versão 89.0.774.68: 1º de abril

As atualizações de segurança do canal estável estão listadas [aqui](./microsoft-edge-relnotes-security.md#april-1-2021).

## <a name="version-89077463-march-25"></a>Versão 89.0.774.63: 25 de março

Vários bugs corrigidos e problemas de desempenho.

## <a name="version-89077457-march-18"></a>Versão 89.0.774.57: 18 de março

Correção de vários bugs e problemas de desempenho.

## <a name="version-89077454-march-13"></a>Versão 89.0.774.54: 13 de março

> [!IMPORTANT]
> Esta atualização contém [CVE-2021-21193](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-21193) que foi relatada pela equipe do Chromium como tendo uma exploração na natureza. Para obter mais informações, consulte o [Guia de atualização de segurança](https://msrc.microsoft.com/update-guide).

As atualizações de segurança do canal estável estão listadas [aqui](./microsoft-edge-relnotes-security.md#march-13-2021).

## <a name="version-89077450-march-10"></a>Versão 89.0.774.50: 10 de março

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-89077448-march-8"></a>Versão 89.0.774.48: 8 de março

Correção de vários bugs e problemas de desempenho.

<!-- begin major 89 -->
## <a name="version-89077445-march-4"></a>Versão 89.0.774.45: 4 de março

> [!IMPORTANT]
> Esta atualização contém o [CVE-2021-21166](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-21166) que foi reportado pela equipe da Chromium por ter uma vulnerabilidade em aberto. Para obter mais informações, confira o [Guia de Atualização de Segurança](https://msrc.microsoft.com/update-guide).

As atualizações de segurança do canal estável estão listadas [aqui](./microsoft-edge-relnotes-security.md#march-4-2021).

### <a name="resolved-issues"></a>Problemas resolvidos

- **Atualizações e correções de atalhos da barra de tarefas e do menu Iniciar:**
  - Clicar com o botão direito do mouse no atalho do Microsoft Edge no menu Iniciar agora mostrará corretamente a opção para desafixar o Microsoft Edge da barra de tarefas quando ele estiver fixado.
  - Layouts iniciais que incluem uma [configuração da barra de tarefas](/windows/configuration/configure-windows-10-taskbar) para fixar o Microsoft Edge na barra de tarefas não resultará mais em um segundo atalho do Microsoft Edge sendo fixado na barra de tarefas.
  - As organizações que utilizam Perfis de Roaming do Windows não verão mais um ícone branco vazio no lugar do ícone do Microsoft Edge na barra de tarefas quando seus usuários fizerem logon no Windows.

### <a name="feature-updates"></a>Atualizações de recursos

- **O modo quiosque permite recursos adicionais de bloqueio**. A partir da versão 89 do Microsoft Edge, adicionamos funcionalidades adicionais de bloqueio no modo de quiosque para permitir que os clientes executem as tarefas em uma experiência mais produtiva e segura. [Saiba mais](microsoft-edge-configure-kiosk-mode.md#kiosk-mode-supported-features).

- **A ferramenta Enterprise Mode Site List Manager estará disponível no navegador através da página do *edge://compat* **. Você pode usar esta ferramenta para criar, editar e exportar o XML da lista de sites para o modo Internet Explorer no Microsoft Edge. Você pode habilitar o acesso a esta ferramenta conforme necessário por meio da política de grupo. [Saiba Mais](./edge-ie-mode-site-list-manager.md).

- **Melhore o desempenho do navegador com guias de suspensão**. As guias em suspensão aprimoram o desempenho do navegador colocando as guias inativas em suspensão para liberar recursos do sistema, como memória e CPU, para que as guias ativas ou outros aplicativos possam usá-las. Os usuários podem impedir que os sites entrem em suspensão e configurem o período de tempo antes de uma Tabulação inativa entrar em suspensão. Para manter os usuários em seu fluxo, há também a [heurística](https://techcommunity.microsoft.com/t5/articles/sleeping-tabs-faq/m-p/1705434) para evitar que certos sites entre em modo de suspensão, como sites intranet. Esse recurso pode ser gerenciado com políticas de grupo.

- **Redefinir manualmente seus dados de sincronização do Microsoft Edge na nuvem**. Introduziremos uma maneira de redefinir os seus dados de sincronização do Microsoft Edge dentro do produto. Isso garante que os seus dados sejam removidos dos serviços Microsoft, além de resolver certos problemas do produto que exigiam um tíquete de suporte.

- **Habilitação inteligente de SSO (Logon único) para todas as contas do Windows Azure Active Directory (Azure AD) para usuários com um único perfil do Microsoft Edge que não é do Azure AD**.  Ative automaticamente essa configuração para os usuários que podem se beneficiar ao máximo desse recurso. Se um usuário tiver apenas um perfil do Microsoft Edge (e não for o Azure AD ou o Modo Infantil), a configuração será automaticamente acionada quando o Microsoft Edge for inicializado. Essa alternância automática também será desativada automaticamente se um usuário mais tarde optar por entrar em um perfil diferente do Microsoft Edge com uma conta do Azure AD. Os usuários podem atualizar manualmente suas preferências para esse recurso em **Configurações > Perfis > Preferências de perfil > Permitir um logon único para sites de trabalho ou de escola usando esse perfil**.

- **Melhorias na experiência de seleção de texto em documentos PDF**. Os usuários começarão a ter uma experiência de seleção de texto mais uniforme e consistente em documentos PDF abertos no Microsoft Edge a partir da versão 89.

- **O campo de data de nascimento agora é compatível com o preenchimento automático**. Hoje, o Microsoft Edge ajuda você a economizar tempo e esforço ao preencher formulários e criar contas online, preenchendo automaticamente seus dados como endereços, nomes, números de telefone, etc. A partir da versão 89 do Microsoft Edge, estamos adicionando suporte para outro campo que você pode ter salvar e preencher automaticamente: a data de nascimento. Você pode exibir, editar e excluir essas informações a qualquer momento nas configurações do seu perfil.

### <a name="policy-updates"></a>Atualizações de política

#### <a name="new-policies"></a>Novas políticas

Sete novas políticas foram adicionadas. Baixe os modelos administrativos atualizados da [página inicial do Microsoft Edge Enterprise](https://www.microsoft.com/edge/business/download). As novas políticas a seguir foram adicionadas.

- [BrowsingDataLifetime](./microsoft-edge-policies.md#browsingdatalifetime) - Configurações do Tempo de Vida de Dados de Navegação
- [MAMEnabled](./microsoft-edge-policies.md#mamenabled) - Gerenciamento de Aplicativos Móveis Habilitado
- [DefinePreferredLanguages](./microsoft-edge-policies.md#definepreferredlanguages) - Define uma lista ordenada de idiomas preferidos em que os sites devem ser exibidos se o site oferecer suporte
- [ShowRecommendationsEnabled](./microsoft-edge-policies.md#showrecommendationsenabled) - Permitir recomendações e notificações promocionais do Microsoft Edge
- [PrintingAllowedBackgroundGraphicsModes](./microsoft-edge-policies.md#printingallowedbackgroundgraphicsmodes) - Restringe o modo de impressão de elementos gráficos de plano de fundo
- [PrintingBackgroundGraphicsDefault](./microsoft-edge-policies.md#printingbackgroundgraphicsdefault) - Modo padrão de impressão de gráficos em segundo plano
- [SmartActionsBlockList](./microsoft-edge-policies.md#smartactionsblocklist) - Bloqueie ações inteligentes  para uma lista de serviços

#### <a name="obsoleted-policies"></a>Políticas obsoletas

As políticas a seguir estão obsoletas.

- [ForceLegacyDefaultReferrerPolicy](./microsoft-edge-policies.md#forcelegacydefaultreferrerpolicy) - Usa uma política referencial padrão de no-referrer-when-downgrade
- [MetricsReportingEnabled](./microsoft-edge-policies.md#metricsreportingenabled) - Habilita o uso e os relatórios de dados relacionados a falhas
- [SendSiteInfoToImproveServices](./microsoft-edge-policies.md#sendsiteinfotoimproveservices): envia as informações do site para melhorar os serviços da Microsoft
<!-- end major 89 -->

<!-- Archive from 86.0.622.43: October 15 to beta 88.0.705.81: February 25  ->
<!-- Archive from 86.0.622.38-october-9 to beta 86.0.62.215-september-14  ->
<!-- Archived to version 84.0.522.40: July 16 -->

## <a name="see-also"></a>Veja também

- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)