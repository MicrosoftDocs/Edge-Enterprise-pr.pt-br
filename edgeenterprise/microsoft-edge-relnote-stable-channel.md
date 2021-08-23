---
title: Notas de versão do Microsoft Edge para Stable Channel
ms.author: aguta
author: AndreaLBarr
manager: srugh
ms.date: 08/19/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Notas de versão do Microsoft Edge para Stable Channel
ms.openlocfilehash: 66d70216da337b5052a7e5b86446db50c30a6f66
ms.sourcegitcommit: 81ecf79c5fd604cae91aaec3786859172c83ec79
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2021
ms.locfileid: "11909896"
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

## <a name="version-92090278-august-19"></a>Versão 92.0.902.78: 19 de agosto

As atualizações de segurança do canal estável estão listadas [aqui](/deployedge/microsoft-edge-relnotes-security#august-19-2021).

## <a name="version-92090267-august-5"></a>Versão 92.0.902.67: 5 de agosto

As atualizações de segurança do canal Estável estão listadas [aqui](/deployedge/microsoft-edge-relnotes-security#august-05-2021).

## <a name="version-92090262-july-29"></a>Versão 92.0.902.62: 29 de julho

Vários bugs e problemas de desempenho corrigidos.

### <a name="modified-policy"></a>Política modificada

- AutoplayAllowed: definir como “Desabilitado” agora define a reprodução automática de mídia como “Limite”

## <a name="version-92090255-july-22"></a>Versão 92.0.902.55: 22 de julho

As atualizações de segurança do canal Estável estão listadas [aqui](/deployedge/microsoft-edge-relnotes-security#july-22-2021).

### <a name="feature-updates"></a>Atualizações de recursos

**Os usuários podem acessar facilmente o modo Internet Explorer no Microsoft Edge**. A partir da versão 92 do Microsoft Edge, os usuários podem recarregar um site no modo Internet Explorer no Microsoft Edge em vez de depender do aplicativo autônomo do IE 11 enquanto aguardam a configuração de um site na Lista de Sites do Modo Empresarial. Os usuários serão solicitados a adicionar o site à sua lista de sites locais de forma que a navegação para a mesma página no Microsoft Edge seja renderizada automaticamente no modo IE pelos próximos 30 dias. Você pode usar a política [InternetExplorerIntegrationReloadInIEModeAllowed](/deployedge/microsoft-edge-policies#internetexplorerintegrationreloadiniemodeallowed) para configurar essa experiência e permitir o acesso aos pontos de entrada do modo IE, bem como a capacidade de adicionar sites à lista de sites locais. Você pode usar a política [InternetExplorerIntegrationLocalSiteListExpirationDays](/deployedge/microsoft-edge-policies#internetexplorerintegrationlocalsitelistexpirationdays) para ajustar o número de dias para manter os sites na lista de sites locais. Observe que KB5003698 ou posterior é necessário para Windows 10, versão 1909; ou KB5003690 ou posterior é necessário para Windows 10, versão 2004, Windows 10, versão 20H2 ou Windows 10, versão 21H1 para a experiência de ponta a ponta. Para obter mais informações, [consulte Lista de sites local no modo IE](/deployedge/edge-ie-mode-local-site-list).

**Os arquivos MHTML serão abertos por padrão no modo Internet Explorer**. A partir do Microsoft Edge versão 92 Estável, os tipos de arquivo MHTML serão abertos automaticamente no modo Internet Explorer no Microsoft Edge em vez do aplicativo Internet Explorer (IE11). Isso é mais comumente observado ao tentar visualizar emails do Outlook em um navegador. Essa alteração ocorrerá apenas se o IE11 for o manipulador padrão para este tipo de arquivo. Se você preferir alterar isso, você pode fazê-lo antes de instalar a atualização da versão Estável 92 usando [ esta diretrizes](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration).

**O aviso de "Desabilitar extensões do modo desenvolvedor" pode ser ignorado por 2 semanas**. A partir da versão 92 da Microsoft Edge, você pode adiar o aviso "Desabilitar extensões do modo desenvolvedor" por 2 semanas, selecionando a opção na caixa de diálogo de aviso.

**Gerenciar suas extensões diretamente da barra de ferramentas**. O novo menu de extensões na barra de ferramentas permitirá que você oculte/fixe extensões facilmente. Os links rápidos para gerenciar extensões e encontrar novas extensões facilitarão a localização de novas extensões e o gerenciamento das existentes.

**O padrão para reprodução automática será definido como Limite**.  Para ajudá-lo a manter seu foco online, mudamos o padrão para reprodução automática de mídia para Limite de Permitir, começando com a versão 92 do Microsoft Edge.

**Os instrumentos de pagamento agora são sincronizados entre dispositivos**. A partir do Microsoft Edge versão 92, você tem a opção de sincronizar suas informações de pagamento em seus dispositivos conectados. Observação: esta é uma Distribuição de Recursos Controlados. Se você não localizar esse recurso, volte em breve enquanto continuamos nossa distribuição.
Atualmente, esse recurso está disponível apenas nos EUA e somente para usuários MSA (não AAD)

**Melhorias na renderização de fontes**. Foram feitas melhorias na renderização do texto para melhorar a clareza e reduzir o borrão. Observação: esta é uma Distribuição de Recursos Controlados. Se você não localizar esse recurso, volte em breve enquanto continuamos nossa distribuição.

**Recursos de botão da barra de ferramentas, como Favoritos e Coleções, lembrarão a escolha do usuário de fixá-los ao lado da janela**. Agora habilitado por padrão, se o usuário optar por fixar um botão da barra de ferramentas, ele sempre abrirá no estado fixado até que ele decida desafixar.

**Os usuários agora podem gerenciar a opção "Permitir o login único para sites de trabalho ou de escola usando esse perfil" por meio da política de grupo**.  A opção “Permitir logon único para sites de trabalho ou de escola usando este perfil” permite que perfis não AAD possam usar o logon único para sites corporativos ou de escola usando as credenciais corporativas ou de escola presentes no computador. Essa opção aparece para os usuários finais como uma alternância em Configurações -> Perfis -> Preferências de Perfil somente para perfis não AAD.  Você pode usar a política [AADWebSiteSSOUsingThisProfileEnabled](/deployedge/microsoft-edge-policies#aadwebsitessousingthisprofileenabled) para configurar o comportamento.  

**Integridade da senha** É importante usar senhas fortes e exclusivas em diferentes contas para manter a segurança online. No entanto, isso é mais fácil de dizer do que fazer e a maioria dos usuários exibe hábitos de senha ruins, como usar senhas fracas que são fáceis de adivinhar ou reutilizar as mesmas senhas fortes entre contas.

Com esta versão mais recente do Microsoft Edge, sua tarefa de usar senhas fortes e exclusivas fica um pouco mais fácil! O Microsoft Edge agora dirá se as senhas salvas são fortes o suficiente e também indicará se elas foram usadas em vários sites, ajudando você a se manter mais seguro online. Você pode encontrar suas informações de integridade de senha na lista de senhas salvas na página edge://settings/passwords.
  
**Privacidade adicionada para suas senhas salvas** Se você estiver usando um dispositivo que compartilha com outras pessoas ou tiver deixado seu computador desbloqueado por qualquer motivo, agora você pode optar por uma segunda verificação usando sua senha de dispositivo para evitar que outras pessoas tenham acesso às senhas do seu site. Simples!

**Extensão do Outlook**.  Fique por dentro da caixa de entrada do Microsoft Outlook, calendário, tarefas e muito mais sem precisar abrir uma nova janela do navegador.  Você pode obter a nova extensão do Outlook aqui: [Microsoft Outlook - Complementos do Microsoft Edge](https://microsoftedge.microsoft.com/addons/detail/microsoft-outlook/kkpalkknhlklpbflpcpkepmmbnmfailf?hl=en-US)

**Em alinhamento com o Chromium de código aberto, Microsoft Edge atualiza a maneira como renderiza tabelas em páginas da Web.** Essa alteração corrige problemas conhecidos e Microsoft Edge mais perto da maneira especificada como as tabelas devem ser renderizações na Web/outros navegadores. Recomendamos que você teste fluxos de trabalho importantes em seu ambiente para problemas inesperados. Um explicador completo está disponível [aqui](https://docs.google.com/document/d/16PFD1GtMI9Zgwu0jtPaKZJ75Q2wyZ9EZnVbBacOfiNA/edit).

### <a name="new-policies"></a>Novas políticas

- [AADWebSiteSSOUsingThisProfileEnabled](/DeployEdge/microsoft-edge-policies#aadwebsitessousingthisprofileenabled)Logon único para sites de trabalho ou escola usando este perfil habilitado.
- [AutomaticHttpsDefault](/DeployEdge/microsoft-edge-policies#automatichttpsdefault) Configurar HTTPS Automático
- [HeadlessModeEnabled](/DeployEdge/microsoft-edge-policies#headlessmodeenabled) Controle o uso do Modo Sem Periféricos
- [InsecurePrivateNetworkRequestsAllowed](/DeployEdge/microsoft-edge-policies#insecureprivatenetworkrequestsallowed) Especifica se deve permitir que sites inseguros façam solicitações para pontos de extremidade de rede mais privada.
- [InsecurePrivateNetworkRequestsAllowedForUrls](/DeployEdge/microsoft-edge-policies#insecureprivatenetworkrequestsallowedforurls) Permite que os sites listados façam solicitações para pontos de extremidade de rede mais privada a partir de contextos inseguros
- [InternetExplorerIntegrationLocalSiteListExpirationDays](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationlocalsitelistexpirationdays) Especifique o número de dias que um site permanece na lista de sites do modo IE local
- [InternetExplorerIntegrationReloadInIEModeAllowed](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationreloadiniemodeallowed) Permite que sites não configurados sejam recarregados no modo Internet Explorer
- [SharedArrayBufferUnrestrictedAccessAllowed](/DeployEdge/microsoft-edge-policies#sharedarraybufferunrestrictedaccessallowed) Especifica se SharedArrayBuffers pode ser usado em um contexto não isolado de origem cruzada

### <a name="deprecated-policy"></a>Política Preterida

- [InternetExplorerIntegrationTestingAllowed](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationtestingallowed) - Permitir teste no modo Internet Explorer.

### <a name="obsoleted-policy"></a>Política Obsoleta

- [EnableSha1ForLocalAnchors](/DeployEdge/microsoft-edge-policies#enablesha1forlocalanchors) Permitir certificados assinados usando SHA-1 quando emitidos por âncoras de confiança locais.

## <a name="version-91086471-july-19"></a>Versão 91.0.864.71: 19 de julho

> [!Important]
>Esta atualização contém [CVE-2021-30563](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-30563), que foi relatado pela equipe Chromium como tendo uma exploração em execução. Para obter mais informações, consulte [Guia de Atualização de Segurança](https://msrc.microsoft.com/update-guide/vulnerability/ADV200002).

As atualizações de segurança do canal Estável estão listadas [aqui](/deployedge/microsoft-edge-relnotes-security#july-19-2021).

## <a name="version-91086467-july-8"></a>Versão 91.0.864.67: 8 de julho

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-91086464-july-2"></a>Versão 91.0.864.64: 2 de julho

Vários bugs e problemas de desempenho corrigidos.

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
