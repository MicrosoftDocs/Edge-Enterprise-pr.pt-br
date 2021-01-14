---
title: Notas de versão arquivadas para o Canal Beta do Microsoft Edge
ms.author: aguta
author: dan-wesley
manager: srugh
ms.date: 01/13/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Notas de versão arquivadas para o Canal Beta do Microsoft Edge
ms.openlocfilehash: 107a45a340e43e2be9c55751966c543a6579bd70
ms.sourcegitcommit: 498a62144b099a1198c06f98ad010cf95aa33727
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/13/2021
ms.locfileid: "11268252"
---
# Notas de versão arquivadas para o Canal Beta do Microsoft Edge

Estas notas de versão fornecem informações sobre os novos recursos e atualizações não relacionadas à segurança que estão inclusos no canal Beta do Microsoft Edge. Para entender os canais do Microsoft Edge, confira a [Visão geral dos canais do Microsoft Edge](microsoft-edge-channels.md). Todas as atualizações de segurança estão listadas [aqui](microsoft-edge-relnotes-security.md).

## Versão 85.0.564.18, 28 de Julho

### Atualizações de recursos

- **Sincronização local de Favoritos e Configurações**. Agora, você pode sincronizar os favoritos do navegador e as configurações entre os perfis do Active Directory dentro de seu próprio ambiente sem a necessidade de sincronização na nuvem.

- **O suporte à Política de Grupo do Microsoft Edge para combinações de sites e aplicativos confiáveis para iniciar sem aviso de confirmação.** Foi acrescentado o suporte à Política de Grupo que permite aos administradores adicionar combinações de sites e aplicativos confiáveis ​​para inicialização sem o aviso de confirmação. Isto adiciona capacidade aos administradores para configurar combinações de protocolo/origem confiáveis (como os aplicativos do Microsoft 365) para seus usuários finais suprimirem a solicitação de confirmação ao navegar para uma URL que contenha um protocolo de aplicativo.

- **Ferramenta Marca-texto para PDF**. Esta ferramenta pode ser facilmente adicionada à barra de ferramentas para realçar facilmente o texto importante no PDF.

- **A API de Acesso ao Armazenamento está disponível**. A API de Acesso ao Armazenamento permite acesso ao armazenamento primário em um contexto de terceiros quando um usuário tem providenciado uma intenção direta de permitir o armazenamento que de outra forma seria bloqueado pela configuração atual do navegador. Para saber mais, veja [API de Acesso de Armazenamento](https://www.chromestatus.com/feature/5612590694662144).

- **Enviar para o OneNote está disponível nas Coleções do Microsoft Edge**. Todos estão entusiasmados em poder enviar as informações que eles reunirão nas Coleções para o OneNote, onde podem acrescentá-las a um projeto maior e colaborar com outras pessoas! E ainda mais importante, no Microsoft Edge 85, você poderá enviar conteúdo para produtos do *Office para Mac* (Word, Excel e OneNote) tanto para a conta Microsoft como para o Azure Active Directory.

- **Atualizações do DevTools**. Para obter detalhes sobre as atualizações a seguir, confira [Novidades no DevTools (Microsoft Edge 85)](https://docs.microsoft.com/microsoft-edge/devtools-guide-chromium/whats-new/2020/06/devtools).

   - O DevTools do Microsoft Edge é compatível com a emulação Surface Duo. O DevTools do Microsoft Edge pode emular o Surface Duo para que você possa testar como o seu conteúdo da Web será visualizado em dispositivos com duas telas. Para ativar esse experimento no DevTools, entre no modo do dispositivo pressionando Ctrl + Shift + M no Windows ou Command + Shift + M no macOS e selecione Surface Duo na lista de seleção do dispositivo.
   - O DevTools do Microsoft Edge permite combinar atalhos de teclado com o Código VS. O DevTools do Microsoft Edge é compatível com a personalização de atalhos de teclado no DevTools para corresponder ao editor/IDE. No Microsoft Edge 85, estamos adicionando a capacidade para combinar os atalhos de teclado do DevTools para o VS Code. Essa alteração ajudará a aumentar a produtividade no Código VS e no DevTools.

### Atualizações de política

#### Novas políticas

Treze novas políticas foram adicionadas. Baixe os modelos administrativos atualizados da [página inicial do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise). As novas políticas a seguir foram adicionadas.

- [AutoLaunchProtocolsFromOrigins](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#autolaunchprotocolsfromorigins) - Definir uma lista de protocolos que podem lançar um aplicativo externo de origens listadas sem alertar o usuário.
- [ AutoOpenAllowedForURLsURLs](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#autoopenallowedforurls) - URLs nas quais o AutoOpenFileTypes pode aplicar.
- [AutoOpenFileTypes](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#autoopenfiletypes) - Lista de tipos de arquivo que devem ser abertos automaticamente no download.
- [DefaultSearchProviderContextMenuAccessAllowed](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultsearchprovidercontextmenuaccessallowed) - Permitir acesso à busca do menu de contexto do provedor de pesquisa padrão.
- [EnableSha1ForLocalAnchors](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#enablesha1forlocalanchors) - Permitir certificados assinados usando SHA-1 quando emitido por âncoras de confiança local.
- [ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#exemptdomainfiletypepairsfromfiletypedownloadwarnings) - Desabilitar o download de avisos baseados em extensão do tipo de arquivo para tipos de arquivo especificados em domínios.
- [IntensiveWakeUpThrottlingEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#intensivewakeupthrottlingenabled) - Controlar o recurso IntensiveWakeUpThrottling.
- [NewTabPagePrerenderEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#newtabpageprerenderenabled) - Habilitar o pré-carregamento da nova página da guia para renderização mais rápida.
- [NewTabPageSearchBox](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#newtabpagesearchbox) - Configurar a nova experiência da caixa de pesquisa da página da guia.
- [PasswordMonitorAllowed](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#passwordmonitorallowed) - Permitir que os usuários sejam alertados caso suas senhas não sejam seguras.
- [RoamingProfileSupportEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#roamingprofilesupportenabled) - Habilitar o uso de cópias de roaming para dados de perfil do Microsoft Edge.
- [RoamingProfileLocation](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#roamingprofilelocation) - Configurar o roaming do diretório de perfil.
- [TLSCipherSuiteDenyList](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#tlsciphersuitedenylist) - Especificar os pacotes de codificação TLS para desabilitar.

#### Políticas obsoletas

- [EnableDomainActionsDownload](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#enabledomainactionsdownload) Habilitar o Download de Ações de Domínio da Microsoft.
- [WebComponentsV0Enabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webcomponentsv0enabled) -reabilita a API de componentes Web V0 até M84.
- [WebDriverOverridesIncompatiblePolicies](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webdriveroverridesincompatiblepolicies) - Permitir ao WebDriver Substituir Políticas Incompatíveis.

<!--- END ---->

## Versão 84.0.522.35: 9 de julho

Correção de vários bugs e problemas de desempenho.

## Versão 84.0.522.28: 26 de junho

Correção de vários bugs e problemas de desempenho.

## Versão 84.0.522.26: 24 de junho

Correção de vários bugs e problemas de desempenho.

## Versão 84.0.522.20: 15 de junho

Correção de vários bugs e problemas de desempenho.

## Versão 84.0.522.15: 8 de junho

Correção de vários bugs e problemas de desempenho.

## Versão 84.0.522.11: 2 de junho

### Atualizações de recursos

- Esta versão do Microsoft Edge fornece uma melhoria na velocidade de download de lista de sites para o modo Internet Explorer.  Reduzimos o atraso de download para a lista de sites no modo Internet Explorer para 0 segundo (de uma espera de 60 segundos) na ausência de uma lista de sites armazenados em cache. Também adicionamos suporte à política de grupo para casos em que as navegações de página inicial no modo Internet Explorer precisem ser adiadas até que a lista de sites seja baixada. Para obter mais informações, confira a política [DelayNavigationsForInitialSiteListDownload](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#delaynavigationsforinitialsitelistdownload).

- O Microsoft Edge agora permite que os usuários entrem no navegador quando ele é "executado como administrador" no Windows 10. Isso ajudará os clientes que usam o Microsoft Edge no Windows Server ou nos cenários de área de trabalho remota ou área restrita.

- O Microsoft Edge agora oferece suporte total ao mouse quando estiver no modo de tela inteira. Agora, você pode usar o mouse para acessar as guias, a barra de endereços e outros itens sem ter que sair do modo de tela inteira.

- Melhoria na compra online. Adicione apelidos personalizados para cartões de crédito ou débitos salvos. Agora, você pode distinguir e diferenciar os cartões de crédito ao fazer compras online. Dar apelidos aos cartões de crédito ou débito permite que você escolha o cartão correto ao usar o preenchimento automático para selecionar um método de pagamento.

- O TLS/1.0 e o TLS/1.1 estão desabilitados por padrão. Para ajudar a descobrir sites afetados, você pode definir o sinalizador *edge://flags/#display-legacy-tls-warnings* para fazer o Microsoft Edge exibir um aviso não bloqueado de "Não Seguro" ao carregar páginas que exijam protocolos TLS herdados. A política [SSLVersionMin](https://docs.microsoft.com/deployedge/microsoft-edge-policies#sslversionmin) permite reabilitar o TLS/1.0 e o TLS/1.1. Essa política permanecerá disponível pelo menos até a versão 88 do Microsoft Edge. Para saber mais, confira [Compatibilidade de sites - alterações que afetam o Microsoft Edge](https://docs.microsoft.com/microsoft-edge/web-platform/site-impacting-changes).

- Aperfeiçoamentos do recurso Coleções:

  - Uma funcionalidade de anotação foi adicionada, o que permite que você adicione uma anotação ou comentário a um item em uma coleção. As anotações são agrupadas e permanecem anexadas a um item, mesmo que você organize os itens em uma coleção. Para experimentar esse novo recurso, clique com o botão direito do mouse em um item e escolha "Adicionar anotação".
  - Você pode alterar a cor da tela de fundo das anotações em coleções. Você pode usar a codificação de cores para ajudá-lo a organizar informações e aumentar a produtividade.
  - Os aperfeiçoamentos de desempenho são notáveis, permitindo que você exporte suas coleções para o Excel em menos tempo do que em versões anteriores do Microsoft Edge.

- Suporte adicional à API do Microsoft Edge:

  - A API de Acesso ao Armazenamento. Essa API permite o acesso ao armazenamento primário em um contexto de terceiros quando um usuário expressa uma intenção direta de permitir o armazenamento que seria bloqueado pela configuração atual do navegador.

    À medida que a privacidade está ficando cada vez mais importante para os usuários, as solicitações para padrões mais restritivos de navegador e configurações de aceitação de usuário, como bloqueio de todo o acesso de armazenamento de terceiros, são cada vez mais comuns. Embora essas configurações ajudem a melhorar a privacidade e bloquear o acesso indesejado de terceiros desconhecidos ou não confiáveis, eles podem ter efeitos colaterais indesejados, como bloquear o acesso a conteúdo que o usuário pode querer ver (por exemplo, mídia social e conteúdo de mídia inserida.)

  - A API do Sistema de Arquivos Nativo, o que significa que você pode conceder permissões aos sites para editar arquivos ou pastas por meio da API do Sistema de Arquivos Nativo.

- Aperfeiçoamentos em PDF:

  - O recurso Ler em Voz Alta para PDF permite que os usuários ouçam o conteúdo em PDF enquanto realizam outras tarefas que podem ser importantes para eles. Ele também ajuda os alunos com estilo de aprendizagem auditivo-visual a se concentrarem em ler o conteúdo, facilitando o aprendizado.
  - Edição de arquivo PDF aperfeiçoada. Agora, você pode salvar uma edição feita em um PDF em vez de salvar uma cópia sempre que editar o PDF.

- O Microsoft Edge agora oferece a opção Tradução na Leitura Avançada. Quando um usuário abre o modo de exibição de Leitura Avançada, há agora a opção de traduzir a página para o idioma desejado.

- O DevTools é compatível com a personalização de atalhos de teclado para corresponder ao editor/IDE, que inclui o VS Code.

### Atualizações de política

#### Novas políticas

Cinco novas políticas foram adicionadas. Baixe os modelos administrativos atualizados da [página inicial do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise). As novas políticas a seguir foram adicionadas.

- [AppCacheForceEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#appcacheforceenabled) - Permite reabilitar o recurso AppCache, mesmo que ele esteja desativado por padrão.
- [ApplicationGuardContainerProxy](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#applicationguardcontainerproxy)- Proxy de Contêiner do Application Guard.
- [DelayNavigationsForInitialSiteListDownload](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#delaynavigationsforinitialsitelistdownload) - Exigir que a lista de sites no Modo Empresarial esteja disponível antes da navegação na guia.
- [NativeWindowOcclusionEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#nativewindowocclusionenabled) - Ative a ocultação do Windows Nativo.
- [NavigationDelayForInitialSiteListDownloadTimeout](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#navigationdelayforinitialsitelistdownloadtimeout) -Definir um tempo limite para o atraso da navegação da guia para a Lista de Sites no Modo Empresarial.

#### Políticas preteridas

- [AllowSyncXHRInPageDismissal](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#allowsyncxhrinpagedismissal) - Autorizar páginas a enviar solicitações de XHR síncronas durante a descarte da página.
- [BuiltinCertificateVerifierEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#builtincertificateverifierenabled) - Determina se o verificador de certificado interno será usado para verificar certificados do servidor.
- [StricterMixedContentTreatmentEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#strictermixedcontenttreatmentenabled)- Habilita um tratamento mais estrito para conteúdo misto.

#### Política obsoleta

[ForceNetworkInProcess](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#forcenetworkinprocess) - Forçar a execução do código de rede no processo do navegador.

<!-- end 84 -->

## Versão 83.0.478.44: 1 de junho

Correção de vários bugs e problemas de desempenho.

## Versão 83.0.478.37: 20 de maio

Correção de vários bugs e problemas de desempenho.

## Versão 83.0.478.33: 15 de maio

Correção de vários bugs e problemas de desempenho.

## Versão 83.0.478.28: 7 de maio

Correção de vários bugs e problemas de desempenho.

## Versão 83.0.478.25: 4 de maio

Correção de vários bugs e problemas de desempenho.

## Versão 83.0.478.18: 27 de abril

Correção de vários bugs e problemas de desempenho.

## Versão 83.0.478.13: 22 de abril

### Atualizações de recursos

- Melhorias no Microsoft Defender SmartScreen: foram feitas várias melhorias no serviço Microsoft Defender SmartScreen, como proteção melhorada contra sites mal-intencionados que são redirecionados durante o carregamento e bloqueio de quadros de nível superior que substitui completamente sites mal-intencionados pela página de segurança do Microsoft Defender SmartScreen. O bloqueio de quadros de nível superior impede a reprodução de áudio e outras mídias do site mal-intencionado, o que proporciona uma experiência mais fácil e menos confusa.

- Em resposta a comentários dos usuários, os usuários agora podem impedir a limpeza de determinados cookies automaticamente quando o navegador é fechado. Essa opção será útil se houver um site do qual os usuários não queiram ser desconectados, mas ainda querem que todos os outros cookies sejam removidos quando o navegador fechar. Para usar esse recurso, acesse *edge://settings/clearBrowsingDataOnClose* e ative a opção "Cookies e outros dados do site".

- A Troca Automática de Perfis agora está disponível para ajudar você a acessar seu conteúdo de trabalho com mais facilidade em diferentes perfis. Se você usar vários perfis no trabalho, poderá verificar esse recurso navegando para um site que exija autenticação da sua conta corporativa ou de estudante enquanto estiver no seu perfil pessoal. Quando detectarmos uma alteração, você receberá uma solicitação para mudar para o seu perfil de trabalho para acessar o site sem precisar se autenticar. Quando você escolhe o perfil de trabalho para o qual deseja mudar, o site simplesmente abre no seu perfil de trabalho. Esse recurso de mudança de perfil ajuda você a manter seus dados pessoais e de trabalho separados e a acessar seu conteúdo de trabalho com mais facilidade. Se você não quiser que o recurso solicite a troca de perfis, você pode escolher a opção não me pergunte novamente isso ficará fora do seu caminho.

- Aperfeiçoamentos de recursos de coleções:
  - Você pode usar o recurso de arrastar e soltar para adicionar um item a uma coleção sem abrir a coleção. Ao arrastar e soltar, você também pode escolher um local na lista de coleções onde deseja colocar o item.
  - Você pode adicionar vários itens a uma coleção em vez de adicionar um item por vez. Para adicionar vários itens, selecione-os e, em seguida, arraste-os para uma coleção. Ou você pode selecionar os itens, clicar com o botão direito do mouse e escolher a coleção onde deseja colocar os itens.

- Você pode adicionar todas as guias em uma janela do Microsoft Edge a uma nova coleção sem adicioná-las individualmente. Para fazer isso, clique com o botão direito do mouse em qualquer guia e escolha "Adicionar todas as guias a uma nova coleção".

- A sincronização de extensão já está disponível. Agora você pode sincronizar suas extensões entre todos os seus dispositivos! As extensões da Microsoft Store e da Chrome Web Store serão sincronizadas com o Microsoft Edge. Para usar esse recurso: Clique nas reticências (**…**) na barra de menus, selecione **Configurações**. Em Seu perfil, clique em **Sincronização** para ver as opções de sincronização. Em **Perfis/Sincronização**, use a alternância para ativar as Extensões. Você pode usar a política de grupo [SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled) para desativar a sincronização de extensões.

- Foi melhorada a mensagem na página de gerenciamento de downloads para downloads não seguros que foram bloqueados.

- Melhorias da Leitura Avançada:
  - Adicionado suporte para Advérbios na experiência Classe Gramatical que temos na Leitura Avançada. Ao ler um artigo na Leitura Avançada, abra as Ferramentas de Gramática e ative Advérbios em Classe Gramatical para destacar todos os advérbios na página.
  - Foi adicionada a capacidade de selecionar qualquer conteúdo em uma página da Web e abri-lo na Leitura Avançada. Essa capacidade permite que os usuários usem a Leitura Avançada e todas as Ferramentas de Aprendizagem, como Foco de Linha e Leitura em Voz Alta, em todos os sites.

- O link Doctor fornece a correção de host e uma consulta de pesquisa aos usuários quando eles digitam incorretamente uma URL. Por exemplo: <br>
Um usuário digita incorretamente "powerbi como" powerbbi". com. O link Doctor vai sugerir "powerbi". com como uma correção e criar um link para pesquisar por "powerbbi" caso o usuário esteja procurando algo diferente.

- Permita que os usuários salvem a decisão para iniciar um protocolo externo para um site específico. Os usuários podem configurar a política [ExternalProtocolDialogShowAlwaysOpenCheckbox]( https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#externalprotocoldialogshowalwaysopencheckbox) para habilitar ou desabilitar esse recurso.

- Os usuários podem definir o Microsoft Edge como navegador padrão diretamente no Microsoft Edge **Configurações**. Esse recurso facilita a alteração do navegador padrão pelos usuários, dentro do contexto do próprio navegador, em vez de precisar pesquisar as configurações do sistema operacional. Para usar esse recurso, vá para *edge://settings/defaultBrowser* e clique em **tornar padrão**.

- Várias atualizações do DevTools, incluindo o suporte à depuração remota, aperfeiçoamentos na IU e muito mais. Para saber mais, consulte [Novidades no DevTools (Microsoft Edge 83)](https://docs.microsoft.com/microsoft-edge/devtools-guide-chromium/whats-new/2020/03/devtools).

### Atualizações de política

#### Novas políticas

15 novas políticas foram adicionadas. Baixe os modelos administrativos atualizados da [página inicial do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise). As novas políticas a seguir foram adicionadas.

- [AllowSurfGame](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#allowsurfgame) - Permitir jogo de surf.
- [AllowTokenBindingForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#allowtokenbindingforurls) - Configurar a lista de sites com os quais o Microsoft Edge tentará estabelecer uma Associação de Token.
- [BingAdsSuppression](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#bingadssuppression) - Bloquear todos os anúncios nos resultados de pesquisa do Bing.
- [BuiltinCertificateVerifierEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#builtincertificateverifierenabled) - Determina se o verificador de certificado interno será usado para verificar certificados do servidor.
- [ClearCachedImagesAndFilesOnExit](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#clearcachedimagesandfilesonexit) - Limpar imagens e arquivos em cache quando o Microsoft Edge é fechado.
- [ConfigureShare](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#configureshare) - Configurar a experiência de Compartilhamento.
- [DeleteDataOnMigration](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#deletedataonmigration) - Excluir dados antigos do navegador na migração.
- [DnsOverHttpsMode](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#dnsoverhttpsmode) - Controlar o modo de DNS sobre HTTPS.
- [DnsOverHttpsTemplates](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#dnsoverhttpstemplates) - Especificar o modelo de URI do resolvedor de DNS sobre HTTPS desejado.
- [FamilySafetySettingsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#familysafetysettingsenabled) - Permitir que os usuários configurem a Proteção para a família.
- [LocalProvidersEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#localprovidersenabled) - Permitir sugestões de provedores locais.
- [ScrollToTextFragmentEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#scrolltotextfragmentenabled) - Ativar a rolagem para o texto especificado nos fragmentos de URL.
- [ScreenCaptureAllowed](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#screencaptureallowed) - Permitir ou negar a captura de tela.
- [SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled) - Configurar a lista de tipos excluídos da sincronização.
- [NativeWindowOcclusionEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#nativewindowocclusionenabled) - Ative a ocultação do Windows Nativo.

#### Política preterida

A política a seguir continuará funcionando nesta versão. Ela se tornará "obsoleta" em uma versão futura.

[EnableDomainActionsDownload](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#enabledomainactionsdownload) Habilitar o Download de Ações de Domínio da Microsoft

<!--  end 83 -->

## Versão 81.0.416.60: 20 de abril

Correção de vários bugs e problemas de desempenho.

## Versão 81.0.416.58: 17 de abril

Atualizações de segurança.

## Versão 81.0.416.50: 10 de abril

Correção de vários bugs e problemas de desempenho.

## Versão 81.0.416.45: 3 de abril

Correção de vários bugs e problemas de desempenho.

## Versão 81.0.416.41: 30 de março

Correção de vários bugs e problemas de desempenho.

## Versão 81.0.416.34: 17 de março

Correção de vários bugs e problemas de desempenho.

## Versão 81.0.416.31: 12 de março

Correção de vários bugs e problemas de desempenho.

## Versão 81.0.416.28: 9 de março

Correção de vários bugs e problemas de desempenho.

## Versão 81.0.416.20: 28 de fevereiro

Correção de vários bugs e problemas de desempenho.

## Versão 81.0.416.12: 20 de fevereiro

### Atualizações de recursos

- Agora as coleções estão disponíveis. Você pode começar clicando no ícone Coleções ao lado da barra de endereços. Esta ação abrirá o painel Coleções, no qual você pode criar, editar e exibir Coleções. Projetamos Coleções com base no que você faz na Web. Se você for um comprador, um viajante ou um aluno, as Coleções poderão ajudá-lo. [Saiba mais](https://blogs.windows.com/msedgedev/2019/12/09/improvements-collections-sync-microsoft-edge/#LuDPRDUDCgdgdOVt.97).

- Permitir a remoção (Ocultar da barra de ferramentas) do botão coleções na barra de ferramentas do Microsoft Edge para obter consistência.

- A entrada local de uma conta do Active Directory local só será direcionada a organizações que as ativam. Se os usuários já tiverem entrado com uma conta do AD local, eles poderão sair dela. Agora, os usuários só entrarão automaticamente com a conta primária em seu sistema operacional se for uma conta Microsoft ou uma conta do Azure Active Directory. Os administradores podem habilitar para entrar automaticamente com uma conta do AD local usando a política ConfigureOnPremisesAccountAutoSignIn.

- Application Guard. Suporte para extensões agora disponível no contêiner.

- Foi adicionada uma mensagem para informar aos usuários que o Internet Explorer não está instalado quando eles navegam para uma página que está configurada para abrir no modo do Internet Explorer.

- A ferramenta modo de exibição 3D foi atualizada no Microsoft Edge DevTools com um novo recurso que ajuda a depurar o contexto de empilhamento de índice z. O modo de exibição 3D mostra uma representação da profundidade do DOM (modelo de objeto do documento) usando a cor e o empilhamento, e o modo de exibição de índice z ajuda a isolar os diferentes contextos de empilhamento da sua página. [Saiba mais](https://blogs.windows.com/msedgedev/2020/01/23/debug-z-index-3d-view-edge-devtools/).

- Localizadas as ferramentas de desenvolvimento F12 em dez novos idiomas, para que eles correspondam ao idioma usado no restante do navegador. [Saiba mais](https://blogs.windows.com/msedgedev/2020/02/04/localizing-edge-devtools/).

- Suporte adicional para a reprodução de Dolby Vision. No Windows 10 Build 17134 com Dolby Vision habilitado (Atualização de abril de 2018), os sites podem mostrar o conteúdo de visão Dolby. Veja como habilitar o conteúdo da visão Dolby da [Netflix](https://help.netflix.com/en/node/42384).

- O Microsoft Edge agora pode identificar e remover favoritos duplicados e pastas de mesclagem com o mesmo nome. Para acessar a ferramenta, clique na estrela na barra de ferramentas do navegador e selecione “Remover favoritos duplicados”.  Você poderá confirmar as alterações e todas as atualizações em seus favoritos serão sincronizadas entre dispositivos.

- Nós ouvimos de usuários que pode ser difícil distinguir uma janela de navegação normal no tema escuro de uma janela InPrivate, porque os quadros de janela são escuros. A nova pílula azul sólida InPrivate no canto superior direito ajuda a garantir aos usuários de que eles estão navegando no InPrivate.

- Abra links externos no perfil correto do navegador. Selecione um perfil padrão para que os links abertos para aplicativos externos sejam abertos a partir de *edge://settings/multiProfileSettings*.

- Foi adicionado um aviso para alertar os usuários que fazem login em um perfil de navegador com uma conta depois de fazer login anteriormente em outra conta. Isso ajudará a evitar a mesclagem de dados não intencionais.

- Caso tenha cartões de pagamento salvos em sua conta da Microsoft, você poderá usá-los no Microsoft Edge durante o preenchimento dos formulários de pagamento. Os cartões em sua conta da Microsoft serão sincronizados entre os dispositivos da área de trabalho e os detalhes completos serão compartilhados com o site após a autenticação de dois fatores (código de segurança e identidade da Microsoft). Para maior praticidade, você pode optar por salvar com segurança uma cópia do cartão no dispositivo durante a autenticação.

- O Foco de Linha foi projetado para os usuários que preferem se concentrar em uma parte limitada do conteúdo conforme eles são lidos. Permite aos usuários manter o foco em 1, 3 ou 5 linhas por vez e destacar o restante da página para permitir que os usuários leiam sem distrações. Os usuários podem rolar a tela usando o toque ou as teclas de direção, e o foco é deslocado de acordo.

- O Microsoft Edge agora está integrado ao verificador ortográfico do Windows nas plataformas do Windows 8.1 e posteriores. Esta integração fornece maior suporte a idiomas, com acesso a mais dicionários de idiomas e a capacidade de usar dicionários personalizados do Windows. Não será necessária nenhuma outra ação dos usuários quando um idioma tiver sido adicionado nas configurações de idioma do sistema operacional e uma verificação ortográfica de idioma estiver habilitada nas configurações do Microsoft Edge.

- Agora, quando os documentos em PDF estão abertos usando o Microsoft Edge, os usuários podem criar destaques, alterar a cor e excluir realces. Isso ajuda a referenciar partes importantes do documento posteriormente e a colaborar.

- Ao carregar documentos longos em PDF que foram otimizados para a Web, as páginas visualizadas pelo usuário serão carregadas mais rapidamente, paralelamente, enquanto o restante do documento estiver sendo carregado.

- Agora é mais fácil iniciar a leitura avançada de um site pressionando a tecla F9.

- Agora é mais fácil começar a ler em voz alta usando um atalho de teclado (Ctrl + Shift + U).

### Atualizações de política

#### Novas políticas

12 novas políticas foram adicionadas. Baixe os modelos administrativos atualizados da [página inicial do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise). As novas políticas a seguir foram adicionadas.

- [AmbientAuthenticationInPrivateModesEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#ambientauthenticationinprivatemodesenabled)- Habilite a autenticação ambiente para perfis InPrivate e Guest. 
- [AudioSandboxEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#audiosandboxenabled)- Permite que a caixa de proteção de áudio seja executada.
- [ForceLegacyDefaultReferrerPolicy](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#forcelegacydefaultreferrerpolicy): Usa uma política referencial padrão de no-referrer-when-downgrade.
- [GloballyScopeHTTPAuthCacheEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#globallyscopehttpauthcacheenabled)- Habilita o cache de autenticação HTTP globalmente.
- [ImportExtensions](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#importextensions)- Permite a importação de extensões.
- [ImportCookies](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#importcookies)- Permite a importação de cookies.
- [ImportShortcuts](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#importshortcuts)- Permite a importação de atalhos.
- [InternetExplorerIntegrationSiteRedirect](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#internetexplorerintegrationsiteredirect)Especifica como as navegações "na página" para sites não configurados se comportam quando iniciadas nas páginas do modo Internet Explorer.
- [OmniboxMSBProviderEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#omniboxmsbproviderenabled)- Habilita o provedor Microsoft Search for Business no omnibox. 
- [StricterMixedContentTreatmentEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#strictermixedcontenttreatmentenabled)- Habilita um tratamento mais estrito para conteúdo misto.
- [TLS13HardeningForLocalAnchorsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#tls13hardeningforlocalanchorsenabled)- Habilita um recurso de segurança TLS 1,3 para âncoras de confiança locais.
- [ConfigureOnPremisesAccountAutoSignIn](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#configureonpremisesaccountautosignin)- Configura o login automático com uma conta de domínio do Active Directory quando não houver nenhuma conta de domínio do Azure AD.

#### Políticas preteridas

As seguintes políticas continuam a funcionar nesta versão. Elas se tornarão "obsoletas" em uma versão futura.

- [WebComponentsV0Enabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webcomponentsv0enabled) - Reabilita a API de componentes Web V0 até M84.
- [WebDriverOverridesIncompatiblePolicies](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webdriveroverridesincompatiblepolicies)- Permite que o WebDriver substitua incompatível.

## Consulte também

- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)