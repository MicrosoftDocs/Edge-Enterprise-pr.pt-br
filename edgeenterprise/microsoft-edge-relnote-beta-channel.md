---
title: Notas da versão do Microsoft Edge para canal beta
ms.author: aguta
author: AndreaLBarr
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Notas da versão do Microsoft Edge para canal beta
ms.openlocfilehash: 1115c8d7822fef7e3784a465d5d4ddfd7b6bd6b1
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/09/2021
ms.locfileid: "11643157"
---
# <a name="release-notes-for-microsoft-edge-beta-channel"></a>Notas de versão do canal do Microsoft Edge beta

Estas notas de versão fornecem informações sobre os novos recursos e atualizações não relacionadas à segurança que estão inclusos no canal Beta do Microsoft Edge. Versões arquivadas dessas notas de versão estão disponíveis [aqui](microsoft-edge-relnote-archive-beta-channel.md).

> [!NOTE]
> A Plataforma da Web Microsoft Edge evolui constantemente para melhorar a experiência, segurança e privacidade do usuário. Para saber mais, confira [Alterações que afetam a compatibilidade do site chegando ao Microsoft Edge](/microsoft-edge/web-platform/site-impacting-changes).

## <a name="version-92090222-june-21"></a>Versão 92.0.902.22: 21 de junho

### <a name="feature-updates"></a>Atualizações de recursos

- **Os usuários podem acessar facilmente o modo Internet Explorer no Microsoft Edge**. A partir da versão 92 do Microsoft Edge, os usuários podem recarregar um site no modo Internet Explorer no Microsoft Edge em vez de depender do aplicativo autônomo do IE 11 enquanto aguardam a configuração de um site na Lista de Sites do Modo Empresarial. Os usuários serão solicitados a adicionar o site à sua lista de sites locais de forma que a navegação para a mesma página no Microsoft Edge seja renderizada automaticamente no modo IE pelos próximos 30 dias. Você pode usar a política *[InternetExplorerIntegrationReloadInIEModeAllowed](/deployedge/microsoft-edge-policies#internetexplorerintegrationreloadiniemodeallowed)* para configurar essa experiência e permitir o acesso aos pontos de entrada do modo IE, bem como a capacidade de adicionar sites à lista de sites locais. Você pode usar a política *[InternetExplorerIntegrationLocalSiteListExpirationDays](/deployedge/microsoft-edge-policies#internetexplorerintegrationlocalsitelistexpirationdays)* para ajustar o número de dias para manter os sites na lista de sites locais.
Observe que KB5003698 ou posterior é necessário para Windows 10, versão 1909; ou KB5003690 ou posterior é necessário para Windows 10, versão 2004, Windows 10, versão 20H2 ou Windows 10, versão 21H1 para a experiência de ponta a ponta.

- **Os arquivos MHTML serão abertos por padrão no modo Internet Explorer**. A partir do Microsoft Edge versão 92 Estável, os tipos de arquivo MHTML serão abertos automaticamente no modo Internet Explorer no Microsoft Edge em vez do aplicativo Internet Explorer (IE11). Isso é mais comumente observado ao tentar visualizar emails do Outlook em um navegador. Essa alteração ocorrerá apenas se o IE11 for o manipulador padrão para este tipo de arquivo. Se preferir alterar isso, você pode fazer isso antes de instalar a atualização da versão 92 Estável usando [este guia](/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration).

- **Os instrumentos de pagamento agora são sincronizados entre dispositivos**. A partir do Microsoft Edge versão 92, você tem a opção de sincronizar suas informações de pagamento em seus dispositivos conectados.
Observação: esta é uma Distribuição de Recurso Controlado e atualmente estamos em 50%. Se você não localizar esse recurso, volte em breve enquanto continuamos nossa distribuição.

- **O aviso "Desabilitar extensões do modo de desenvolvedor" pode ser descartado permanentemente**. A partir da versão 92 do Microsoft Edge, você pode desabilitar o aviso "Desabilitar extensões do modo de desenvolvedor" clicando na opção 'Não mostrar novamente'.
Observação: este é uma Distribuição de Recurso Controlado e atualmente estamos em 25%. Se você não localizar esse recurso, volte em breve enquanto continuamos nossa distribuição.

- **Gerencie suas extensões diretamente na barra de ferramentas**. O novo menu de extensões na barra de ferramentas permitirá que você oculte/fixe extensões facilmente. Os links rápidos para gerenciar extensões e encontrar novas extensões facilitarão a localização de novas extensões e o gerenciamento das existentes.
Observação: este é uma Distribuição de Recurso Controlado e atualmente estamos em 25%. Se você não localizar esse recurso, volte em breve enquanto continuamos nossa distribuição.

- **HTTPS automático**. Os usuários terão a opção de atualizar a navegação de HTTP para HTTPS em domínios que provavelmente suportam este protocolo mais seguro. Esse suporte também pode ser configurado para tentar entrega HTTPS para todos os domínios.
Observação: estamos testando esse recurso e esse comportamento não será detectado se você tiver desativado os experimentos.

- **Melhorias na renderização de fontes**. Foram feitas melhorias na renderização do texto para melhorar a clareza e reduzir o borrão.
Observação: este é uma Distribuição de Recurso Controlado e atualmente estamos em 25%. Se você não localizar esse recurso, volte em breve enquanto continuamos nossa distribuição.

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
