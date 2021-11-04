---
title: Gerenciamento de Lista de Sites para modo Internet Explorer (IE) (Visualização Pública)"
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 11/03/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Saiba como configurar e usar o Gerenciamento de Lista de Sites na Nuvem para o modo IE usando o Centro de administração do Microsoft 365.
ms.openlocfilehash: 29984aa559c0afda5be0457fcbe618dc264a3e68
ms.sourcegitcommit: 4ec03873a85f065d9bfa6203cfe6c3e938f79bc5
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2021
ms.locfileid: "12155038"
---
# <a name="cloud-site-list-management-for-ie-mode-public-preview"></a>Gerenciamento de Lista de Sites na Nuvem para o modo IE (Visualização Pública)

Este artigo explica como configurar e usar o Gerenciamento de Lista de Sites na Nuvem para Internet Explorer (IE) por meio do Centro de administração do Microsoft 365.

## <a name="overview"></a>Visão Geral

À medida que você faz a transição de fluxos de trabalho e aplicativos do IE11 para o modo IE, o **Gerenciamento de Lista de Sites na Nuvem** permite que você gerencie suas listas de sites para o modo IE na nuvem. Você pode trabalhar com listas de sites usando a experiência **Listas de Sites do Microsoft Edge** no **Centro de administração do Microsoft 365**.

Para saiba mais, assista ao vídeo [Experiência de gerenciamento da lista de sites na nuvem para o modo IE](https://www.youtube.com/watch?v=9-GovDcryXQ).

> [!NOTE]
> Essa experiência agora está em versão prévia pública.

A experiência de visualização permite armazenar a lista de sites da sua organização em um local de nuvem compatível, em vez de precisar de uma infraestrutura local para hospedar sua lista de sites. Você pode criar, importar, exportar listas de sites e auditar alterações nas entradas da lista de sites por meio do Centro de administração do Microsoft 365. Você pode publicar várias listas de sites na nuvem e usar a política de grupo para atribuir diferentes grupos de dispositivos para usar listas diferentes.

## <a name="prerequisites"></a>Pré-requisitos

Os pré-requisitos a seguir se aplicam a esta visualização pública.

1. Os clientes devem ter um locatário do Azure Active Directory.
2. Os administradores devem ter Microsoft Edge versão 93 ou superior instalado e a versão mais recente dos [arquivos de política](https://aka.ms/edgeenterprise).
3. Os administradores precisam ser um [Administrador do Edge](/azure/active-directory/roles/permissions-reference#edge-administrator) ou um [Administrador Global](/azure/active-directory/roles/permissions-reference#global-administrator) no locatário para acessar a experiência de listas de sites do Microsoft Edge.
   - Para optar pela versão prévia pública, um Administrador Global é necessário para optar pelo locatário na versão direcionada. Para obter mais informações, consulte [Aceitar versão prévia pública](#opt-in-to-public-preview).

## <a name="the-preview-experience"></a>A experiência de visualização

Há três aspectos para a experiência de visualização.

### <a name="publish-enterprise-site-list-to-the-cloud"></a>Publicar a lista de sites corporativos na nuvem

Os administradores podem publicar uma ou mais listas de sites em um ponto de extremidade autenticado que Microsoft Edge clientes em seu locatário podem baixar para a experiência de modo IE. Os administradores podem importar o XML das listas de sites corporativos existentes para a experiência de Listas de Sites do Microsoft Edge no Centro de Administração do Microsoft 365 e publicá-lo no local da nuvem. 

### <a name="associate-the-cloud-hosted-site-list-with-microsoft-edge"></a>Associar a lista de sites hospedados na nuvem ao Microsoft Edge

Com Microsoft Edge versão 93, os administradores podem usar a configuração [InternetExplorerIntegrationCloudSiteList](/docs.microsoft.com/deployedge/microsoft-edge-policies#internetexplorerintegrationcloudsitelist) para definir uma das listas de sites hospedados na nuvem que o Microsoft Edge pode consumir para o modo IE. Os usuários devem estar conectados no Microsoft Edge para que o cliente consuma a lista de sites da nuvem.

> [!IMPORTANT]
> Quando essa política é configurada, ela substitui a política original [InternetExplorerIntegrationSiteList](/docs.microsoft.com/deployedge/microsoft-edge-policies#internetexplorerintegrationsitelist).

### <a name="manage-site-list-contents-on-the-microsoft-365-admin-center"></a>Gerenciar o conteúdo da lista de sites no Centro de administração do Microsoft 365

Os administradores podem criar uma nova lista ou importar uma lista de sites existente para a Microsoft Edge de listas de sites. Eles podem adicionar, editar, excluir o conteúdo da lista de sites e exibir o histórico de comentários para controlar alterações em entradas individuais. A próxima seção explica como optar pela visualização pública e acessar Microsoft Edge experiência de listas de sites no Centro de administração do Microsoft 365.

## <a name="opt-in-to-public-preview"></a>Optar pela visualização pública

Durante a versão prévia pública, você precisa optar por exibir as experiências de visualização no Centro de administração do Microsoft 365. Você deve ser um administrador global no Microsoft 365 para aceitar.

Use as etapas a seguir para alterar como sua organização recebe atualizações do Microsoft 365.

> [!NOTE]
> Pode levar até 24 horas para que as seguintes alterações de configuração entrem em vigor no Microsoft 365. Se você recusar uma versão direcionada depois de habilitá-la, os usuários poderão perder o acesso aos recursos que ainda não atingiram o lançamento agendado.

1. Entre no [Centro de Administração do Microsoft 365](https://admin.microsoft.com) e vá para  **Configurações > Configuração da Organização**. Na guia  **Perfil da organização** , escolha **Preferências de versão**.
2. Para desabilitar a versão direcionada, selecione **Versão Padrão**e, em seguida, selecione **Salvar alterações**.
3. Para habilitar a versão direcionada para todos os usuários em sua organização, selecione **Lançamento direcionado para todos** e selecione  **Salvar alterações**.
4. Para habilitar a versão direcionada para algumas pessoas em sua organização, selecione  **Lançamento direcionado para usuários selecionados** e selecione  **Salvar alterações**.
5. Escolha **Selecionar usuários** para adicionar usuários um de cada vez, ou **Carregar usuários** para adicioná-los em massa.
6. Quando terminar de adicionar usuários, selecione  **Salvar alterações**.

Para obter mais informações, consulte [Configurar as opções de versão Padrão ou Direcionada – Administrador do Microsoft 365](/microsoft-365/admin/manage/release-options-in-office-365)

## <a name="publish-enterprise-site-list-to-the-cloud"></a>Publicar a lista de sites corporativos na nuvem

Use as etapas a seguir como um guia para criar uma lista de sites, importar uma lista de sites e publicar a lista de sites. Antes de concluir essas etapas, entre no Centro de administração do Microsoft 365.

1. Entre no [Centro de administração do Microsoft 365](https://admin.microsoft.com) com suas credenciais de administrador.
2. No painel de navegação esquerdo, selecione **Configurações > Configurações da Organização**.
3. Você verá a opção **Listas de Sites do Microsoft Edge (versão prévia)**.

### <a name="steps-to-create-a-site-list"></a>Etapas para criar uma lista de sites

1. Na página Configurações da Organização, selecione **Listas de sites do Microsoft Edge (versão prévia)**
2. Na página resultante, selecione **Criar uma nova lista**.
3. Insira um **nome da lista de Site** e uma **Descrição** e selecione **Criar**.
4. Depois de obter a confirmação, selecione **Fechar painel**. 

### <a name="steps-to-import-a-site-list"></a>Etapas para importar uma lista de sites

1. Selecione a lista de sites que você deseja preencher.
2. Na página resultante, selecione **Importar lista**.
3. No painel direito, selecione **Procurar**.
4. Selecione o arquivo que você deseja importar e selecione **Carregar** na parte inferior do painel.
5. Você pode navegar pelas URLs no arquivo carregado. Se você quiser escolher um arquivo diferente, poderá selecionar **Carregar um arquivo diferente** na parte superior do painel. Se tudo estiver correto, selecione **Adicionar** na parte inferior do painel.
6. Depois que a lista for importada, selecione **Fechar painel**. 

### <a name="steps-to-publish-a-site-list"></a>Etapas para publicar uma lista de sites

1. Para publicar uma lista de sites, volte um nível para a página listas de sites do Microsoft Edge. Selecione a trilha acima do nome da lista de sites para ir um nível acima.
2. Na página de listas de sites do Microsoft Edge, selecione a lista de sites que você deseja publicar na nuvem e selecione **Publicar lista de sites**.
3. No painel direito, atualize o **Número da versão** e selecione **Publicar** na parte inferior do painel.
4. Após a confirmação, selecione **Fechar painel**. 
5. As colunas **Status de publicação**, **Última publicação** e **Última publicação por** são atualizadas.

## <a name="associate-the-cloud-hosted-site-list-with-microsoft-edge"></a>Associar a lista de sites hospedados na nuvem ao Microsoft Edge

Use as etapas a seguir para associar a lista de sites hospedados na nuvem ao Microsoft Edge.

1. Para configurar dispositivos para usar uma lista de sites publicados, clique na lista de sites que você deseja atribuir aos dispositivos.
2. Na página resultante, copie a **ID da lista de sites**.
3. Para o grupo de dispositivos escolhido, selecione **Habilitado** e insira **ID de lista de site** na política [Configurar a Lista de Site de Nuvem modo Empresarial](/deployedge/microsoft-edge-policies#internetexplorerintegrationcloudsitelist).
4. Você pode executar **gpupdate/force** no Prompt de Comando para atualizar o dispositivo com a política ou aguardar até que a política de grupo entre em vigor. Depois que a política for atualizada, você poderá verificar se o Microsoft Edge está lendo a lista de sites na nuvem acessando [edge://compat/enterprise](edge://compat/enterprise). Você precisa estar conectado ao Microsoft Edge.

> [!NOTE]
> Depois de publicar uma lista de sites pela primeira vez e atualizar a política de grupo, você precisa reiniciar o Microsoft Edge. Aguarde 60 segundos ou selecione o botão Forçar Atualização em [edge://compat/enterprise](edge://compat/enterprise). Ao publicar atualizações em uma lista de sites já associada, pode haver uma versão mais antiga da lista de sites no cache. Essa entrada será atualizada após 60 segundos. Para obter mais informações, consulte [O que acontece se usuários saírem do Microsoft Edge?](#what-happens-if-users-log-out-of-microsoft-edge).

## <a name="manage-site-list-contents-on-the-microsoft-365-admin-center"></a>Gerenciar o conteúdo da lista de sites no Centro de administração do Microsoft 365

Você pode adicionar entradas de site individuais, excluir entradas do site e exibir o histórico de alterações para comentários.
Se você tiver cenários híbridos que exigem que sua lista de sites seja hospedada localmente, poderá exportar sua lista de sites do Centro de administração do Microsoft 365. Use as etapas a seguir como um guia para gerenciar o conteúdo da lista de sites.

### <a name="add-individual-sites-to-the-site-list"></a>Adicionar sites individuais à lista de sites

Você pode adicionar sites individuais a qualquer lista de sites. Depois de adicionar sites à lista, você pode usar os filtros predefinidos usando o botão **Filtrar** (ao lado da área de entrada pesquisar) para exibir as atualizações da lista.

1. Vá para a lista de sites em que você deseja adicionar um site.
2. Selecione **Adicionar um site**.
3. Insira o endereço do site e escolha o mecanismo que deve ser usado para abrir o site. Adicione comentários conforme necessário e selecione **Salvar**.

   > [!NOTE]
   > A coluna **Status** para quaisquer entradas adicionadas a uma lista de sites publicados mostrará **Adição pendente**. Se você navegar até a lista de listas de sites selecionando **listas de sites do Microsoft Edge** na parte superior da tela, verá que a coluna **Status de publicação** mostra **Alterações de publicação pendentes** para indicar que as atualizações mais recentes da lista de sites precisam ser publicadas para que os usuários as recebam. Você pode usar o botão **Filtrar** _(ao lado da caixa de pesquisa)_ para selecionar Adição pendente para ver todas as entradas adicionadas que estão pendentes na publicação.

### <a name="view-the-change-history-for-site-entries"></a>Exibir o histórico de alterações para entradas do site

1. Selecione a entrada do site para a qual você deseja ver o histórico de alterações e selecione **Exibir comentários**.

### <a name="delete-a-site-from-the-site-list"></a>Excluir um site da lista de sites

Use as etapas a seguir para excluir uma entrada de site.

1. Escolha a entrada da lista de sites da qual você deseja excluir um site. Selecione **Excluir site**.
2. Selecione **Excluir** na parte inferior do painel.
3. Depois de ver a confirmação de que uma entrada de site foi excluída, ela permanecerá na lista até que a lista de sites seja publicada no local da nuvem. Você pode exibir a lista de sites excluídos antes de publicar selecionando o botão Filtrar e filtrando sites no estado **Exclusão pendente**.

   > [!NOTE]
   > A coluna **Status** para todas as entradas excluídas de uma lista de sites publicados mostrará **Exclusão pendente**. Se você navegar até a lista de listas de sites selecionando **Listas de sites do Microsoft Edge** na parte superior da tela, você verá que a coluna **Status de Publicação** mostra **Alterações de publicação pendentes** para indicar que as atualizações mais recentes da lista de sites precisam ser publicadas para que os usuários as recebam. Você pode usar o botão **Filtrar** _(ao lado da caixa de pesquisa)_ para selecionar Exclusão pendente para ver todas as entradas excluídas que estão em publicação pendente.

### <a name="export-a-site-list"></a>Exportar uma lista de sites

Há cenários em que você deseja exportar uma lista de sites. Por exemplo, se você não conseguir mover sua lista de sites para a nuvem imediatamente ou se precisar manter um ambiente híbrido com listas de sites na nuvem e no local. Você pode usar a experiência de Gerenciamento de Lista de Sites na Nuvem para gerenciar atualizações para uma lista de sites em um local central e exportar a lista de sites para o host local.

1. Na página listas de sites do Microsoft Edge, selecione a lista de sites que você deseja exportar.
2. Na página resultante, você verá as entradas da lista de sites e a opção **Exportar lista**.
3. Selecione **Exportar lista** para baixar o arquivo XML da lista de sites.

## <a name="faq"></a>Perguntas frequentes

### <a name="when-i-select-microsoft-edge-site-lists-and-try-to-create-a-new-list-i-get-this-error---request-failed-with-status-code-500-why-is-that"></a>Quando seleciono “Listas de sites do Microsoft Edge” e tento criar uma nova lista, recebo esse erro - “Falha na solicitação com o código de status 500”. Por quê?

As Listas de Sites do Microsoft Edge armazena seus dados e configurações em uma infraestrutura de serviço compartilhada com serviços de nuvem corporativos, tais como Exchange Online, SharePoint Online, Teams e Microsoft Azure AD. Em casos raros, quando as listas de sites do Microsoft Edge são o primeiro recurso a usar essa infraestrutura, o provisionamento pode levar algum tempo. Nesses casos, a solicitação inicial do Centro de Administração do Microsoft 365 falhará. Quando a solicitação falhar, um alerta será enviado ao sistema de provisionamento para resolver o problema. Normalmente, o provisionamento é concluído em três dias. Portanto, se você receber esse erro, tente novamente em alguns dias e crie uma nova lista. Se você ainda não conseguiu criar uma nova lista ou se precisar de assistência urgente, contate o Suporte da Microsoft.

### <a name="can-users-who-havent-signed-in-to-microsoft-edge-download-the-site-list"></a>Os usuários que ainda não entraram no Microsoft Edge podem baixar a lista de sites?

Não, os usuários devem entrar no navegador para baixar a lista de sites hospedados na nuvem. Você pode configurar uma política para permitir a Entrada Implícita para impedir a interrupção da experiência do usuário. Para obter mais informações, consulte [ImplicitSignInEnabled](/docs.microsoft.com/DeployEdge/microsoft-edge-policies#implicitsigninenabled).

### <a name="what-is-the-default-refresh-interval-after-updates-are-made-to-site-list-contents"></a>Qual é o intervalo de atualização padrão depois que as atualizações são feitas no conteúdo da lista de sites?

A lista de sites é atualizada no Microsoft Edge a cada duas horas. Você pode alterar esse intervalo na política [NavigationDelayForInitialSiteListDownloadTimeout](/docs.microsoft.com/deployedge/microsoft-edge-policies#navigationdelayforinitialsitelistdownloadtimeout). O intervalo mínimo de atualização é de 30 minutos.

### <a name="what-happens-if-users-log-out-of-microsoft-edge"></a>O que acontece se os usuários saírem do Microsoft Edge?

O acesso à lista de sites requer entrada explícita no navegador para o primeiro download. Em um cenário em que o usuário faz logoff depois de fazer logon, a lista de sites é armazenada em cache no Microsoft Edge. A lista permanecerá armazenada em cache mesmo se o usuário fizer logoff do Microsoft Edge de sua conta do Azure Active Directory (Azure AD). Microsoft Edge não tentará fazer fallback para o local de download não na nuvem enquanto a política de lista de sites de nuvem estiver configurada. Microsoft Edge tenta atualizar a lista de sites armazenados em cache nos seguintes horários (observe que todas as tentativas falharão se o usuário não estiver conectado ao Microsoft Edge):

- 60 segundos depois de reiniciar o navegador. Se o atraso de inicialização de 60 segundos precisar ser menor, você poderá usar a política [NavigationDelayForInitialSiteListDownloadTimeout](/deployedge/microsoft-edge-policies#navigationdelayforinitialsitelistdownloadtimeout) para alterar a quantidade de atraso.
- A cada duas horas quando o Microsoft Edge está em execução.

## <a name="support-and-feedback"></a>Suporte e Comentários

Durante a versão prévia pública, a experiência de Gerenciamento de Lista de Sites na Nuvem é coberta pelo seu contrato existente do [Suporte Premier da Microsoft](https://www.microsoft.com/en-us/unifiedsupport/premier). Você pode entrar em contato com Suporte da Microsoft para relatar problemas ou comentários. Você também pode deixar comentários em nosso [Fórum TechCommunity](https://techcommunity.microsoft.com/t5/enterprise/bd-p/EdgeInsiderEnterprise).

## <a name="see-also"></a>Consulte também

- [Sobre o modo IE](./edge-ie-mode.md)
- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
  
