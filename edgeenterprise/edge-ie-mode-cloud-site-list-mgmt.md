---
title: Gerenciamento de Lista de Sites na Nuvem para modo Internet Explorer (IE)
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 06/08/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Saiba como configurar e usar o Gerenciamento de Lista de Sites na Nuvem para o modo IE usando o Centro de administração do Microsoft 365.
ms.openlocfilehash: e3e1368fd09ba7fa548c223b95d05c52ebf8c324
ms.sourcegitcommit: 4133b81fde3ee1a63a2e8d342d4138c5bba427df
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/09/2022
ms.locfileid: "12581372"
---
# <a name="cloud-site-list-management-for-internet-explorer-ie-mode"></a>Gerenciamento de Lista de Sites na Nuvem para modo Internet Explorer (IE)

Este artigo explica como configurar e usar o Gerenciamento de Lista de Sites na Nuvem para Internet Explorer (IE) por meio do Centro de administração do Microsoft 365.

> [!NOTE]
> No momento, essa experiência do usuário está disponível apenas para instâncias de nuvem GCC e em todo o mundo.

## <a name="overview"></a>Visão Geral

À medida que você faz a transição de fluxos de trabalho e aplicativos do IE11 para o modo IE, o **Gerenciamento de Lista de Sites na Nuvem** permite que você gerencie suas listas de sites para o modo IE na nuvem. Você pode trabalhar com listas de sites usando a experiência **Listas de Sites do Microsoft Edge** no **Centro de administração do Microsoft 365**.

Para saber mais, assista ao próximo vídeo.

[![Novo Gerenciamento de Lista de Sites na Nuvem para o modo IE](media/edge-ie-mode-cloud-site-list-mgmt/0.png)](https://www.youtube.com/watch?v=p3FyGvsNKC8 "|::ref1::|").

Essa experiência permite armazenar a lista de sites da sua organização em um local de nuvem compatível, em vez de precisar de uma infraestrutura local para hospedar sua ’ lista de sites. Você pode criar, importar, exportar listas de sites e auditar alterações nas entradas da lista de sites por meio do Centro de administração do Microsoft 365. Você pode publicar várias listas de sites na nuvem e usar a política de grupo para atribuir diferentes grupos de dispositivos para usar listas diferentes.

## <a name="prerequisites"></a>Pré-requisitos

Os pré-requisitos a seguir se aplicam a esse recurso.

1. Os clientes devem ter um locatário do Azure Active Directory.
2. Os administradores devem ter Microsoft Edge versão 93 ou superior instalado e a versão mais recente dos [arquivos de política](https://aka.ms/edgeenterprise).
3. Os administradores precisam ser um [Administrador do Microsoft Edge](/azure/active-directory/roles/permissions-reference#edge-administrator) ou um [Administrador Global](/azure/active-directory/roles/permissions-reference#global-administrator) no locatário para acessar a experiência de listas de sites do Microsoft Edge.

## <a name="cloud-site-list-management-experience"></a>Experiência de Gerenciamento de Lista de Sites na Nuvem

Há quatro aspectos da experiência de Gerenciamento de Lista de Sites na Nuvem:

- Publicar a lista de sites corporativos na nuvem.
- Associar a lista de sites na nuvem ao Microsoft Edge.
- Gerenciando o conteúdo da lista de sites no Centro de administração do Microsoft 365.
- Exibindo os comentários do site no Centro de administração do Microsoft 365.

### <a name="publish-enterprise-site-list-to-the-cloud"></a>Publicar a lista de sites corporativos na nuvem

Os administradores podem publicar uma ou mais listas de sites em um ponto de extremidade autenticado que Microsoft Edge clientes em seu locatário podem baixar para a experiência de modo IE. Os administradores podem importar o XML das listas de sites corporativos existentes para a experiência de Listas de Sites do Microsoft Edge no Centro de Administração do Microsoft 365 e publicá-lo no local da nuvem.

### <a name="associate-the-cloud-hosted-site-list-with-microsoft-edge"></a>Associar a lista de sites hospedados na nuvem ao Microsoft Edge

Com Microsoft Edge versão 93, os administradores podem usar a configuração [InternetExplorerIntegrationCloudSiteList](/deployedge/microsoft-edge-policies#internetexplorerintegrationcloudsitelist) para definir uma das listas de sites hospedados na nuvem que o Microsoft Edge pode consumir para o modo IE. Os usuários devem estar conectados no Microsoft Edge para que o cliente consuma a lista de sites da nuvem.

> [!IMPORTANT]
> Quando essa política é configurada, ela substitui a política original [InternetExplorerIntegrationSiteList](/deployedge/microsoft-edge-policies#internetexplorerintegrationsitelist).

### <a name="manage-site-list-contents-on-the-microsoft-365-admin-center"></a>Gerenciar o conteúdo da lista de sites no Centro de administração do Microsoft 365

Os administradores podem criar uma nova lista ou importar uma lista de sites existente para a Microsoft Edge de listas de sites. Eles podem adicionar, editar, excluir o conteúdo da lista de sites e exibir o histórico de comentários para controlar alterações em entradas individuais. A próxima seção explica como optar pela visualização pública e acessar Microsoft Edge experiência de listas de sites no Centro de administração do Microsoft 365.

### <a name="view-site-feedback-on-the-microsoft-365-admin-center"></a>Exibir comentários do site no Centro de administração do Microsoft 365

Com a versão 99 do Microsoft Edge, os administradores podem usar as políticas [InternetExplorerIntegrationCloudUserSitesReporting](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationcloudusersitesreporting) e [InternetExplorerIntegrationCloudNeutralSitesReporting](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationcloudneutralsitesreporting) para identificar lacunas em sua lista de sites com comentários do site. Eles podem exibir sites que os usuários adicionaram às [listas de sites locais](/deployedge/edge-ie-mode-local-site-list) e sites neutros potencialmente configurados incorretamente.

## <a name="publish-enterprise-site-list-to-the-cloud"></a>Publicar a lista de sites corporativos na nuvem

Use as etapas a seguir como um guia para criar uma lista de sites, importar uma lista de sites e publicar uma lista de sites. Antes de concluir essas etapas, entre no Centro de administração do Microsoft 365.

1. Entre no [Centro de administração do Microsoft 365](https://admin.microsoft.com) com suas credenciais de administrador.
2. No painel de navegação esquerdo, selecione **Configurações > Configurações da Organização**.
3. Você verá a opção de **listas de sites do Microsoft Edge**.

   > [!NOTE]
   > Se você não vir essa opção na página De configurações da Organização enquanto estamos implantando em todas as instâncias de produção, você precisará optar pela **Versão direcionada**. Se você não vir a opção **listas de sites do Microsoft Edge**, confira as perguntas frequentes: [não vejo a opção "listas de sites do Microsoft Edge" na página "Configurações da organização" no Centro de administração do Microsoft 365. Por que isso?](#i-dont-see-the-microsoft-edge-site-lists-option-in-the-org-settings-page-on-microsoft-365-admin-center-why-is-that).

### <a name="steps-to-create-a-site-list"></a>Etapas para criar uma lista de sites

1. Na página Configurações da Organização, selecione **listas de sites do Microsoft Edge**
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

1. Para configurar dispositivos para usar uma lista de sites publicados, selecione a lista de sites que você deseja atribuir aos dispositivos.
2. Na página resultante, copie a **ID da lista de sites**.
3. Para o grupo de dispositivos escolhido, selecione **Habilitado** e insira **ID de lista de site** na política [Configurar a Lista de Site de Nuvem modo Empresarial](/deployedge/microsoft-edge-policies#internetexplorerintegrationcloudsitelist).
4. Você pode executar **gpupdate/force** no Prompt de Comando para atualizar o dispositivo com a política ou aguardar até que a política de grupo entre em vigor. Depois que a política for atualizada, você poderá verificar se o Microsoft Edge está lendo a lista de sites na nuvem acessando [edge://compat/enterprise](edge://compat/enterprise). Você precisa estar conectado ao Microsoft Edge.

> [!NOTE]
> Depois de publicar uma lista de sites pela primeira vez e atualizar a política de grupo, você precisa reiniciar o Microsoft Edge. Aguarde 60 segundos ou selecione a opção **Forçar Atualização** em [edge://compat/enterprise](edge://compat/enterprise). Ao publicar atualizações em uma lista de sites já associada, pode haver uma versão mais antiga da lista de sites no cache. Essa entrada será atualizada após 60 segundos. Para obter mais informações, consulte [O que acontece se usuários saírem do Microsoft Edge?](#what-happens-if-users-log-out-of-microsoft-edge).

## <a name="manage-site-list-contents-on-the-microsoft-365-admin-center"></a>Gerenciar o conteúdo da lista de sites no Centro de administração do Microsoft 365

Você pode adicionar, editar, excluir o conteúdo da lista de sites e exibir o histórico de comentários para acompanhar as alterações em entradas individuais para sites e cookies compartilhados.

Se você tiver cenários híbridos que exigem que sua lista de sites seja hospedada localmente, poderá exportar sua lista de sites do Centro de administração do Microsoft 365. Use as etapas a seguir como um guia para gerenciar o conteúdo da lista de sites.

### <a name="add-a-site-to-the-site-list"></a>Adicionar um site à lista de sites

Você pode adicionar sites individuais a qualquer lista de sites. Depois de adicionar sites à lista, você pode usar os filtros predefinidos usando o botão **Filtrar** (ao lado da caixa Pesquisar) para exibir as atualizações da lista.

1. Vá para a lista de sites em que você deseja adicionar um site.
2. Selecione **Adicionar um site**.
3. Insira o endereço do site e escolha o mecanismo que deve ser usado para abrir o site. Adicione comentários conforme necessário e selecione **Salvar**.

   > [!NOTE]
   > A coluna **Status** para quaisquer entradas adicionadas a uma lista de sites publicados mostrará **Adição pendente**. Se você navegar até a lista de listas de sites selecionando **listas de sites do Microsoft Edge** na parte superior da tela, verá que a coluna **Status de publicação** mostra **Alterações de publicação pendentes** para indicar que as atualizações mais recentes da lista de sites precisam ser publicadas para que os usuários as recebam. Você pode usar o botão **Filtrar** (ao lado da caixa Pesquisar) para selecionar **Adição pendente** para ver todas as entradas adicionadas que estão pendentes de publicação.

### <a name="delete-a-site-from-the-site-list"></a>Excluir um site da lista de sites

Use as etapas a seguir para excluir uma entrada de site.

1. Escolha a entrada do site que você gostaria de excluir da lista de sites. Selecione **Excluir site**.
2. Selecione **Excluir** no pop-up da caixa de diálogo.
3. Depois de ver a confirmação de que uma entrada de site foi excluída, ela permanecerá na lista até que a lista de sites seja publicada no local da nuvem. Você pode exibir a lista de sites excluídos antes de publicar selecionando o botão **Filtrar** e filtrando os sites no estado **Exclusão pendente**.

   > [!NOTE]
   > A coluna **Status** para quaisquer entradas excluídas de uma lista de sites publicados mostrará **Exclusão pendente**. Se você navegar até a lista de listas de sites selecionando **listas de sites do Microsoft Edge** na parte superior da tela, verá que a coluna **Status de publicação** mostra **Alterações de publicação pendentes** para indicar que as atualizações mais recentes da lista de sites precisam ser publicadas para que os usuários as recebam. Você pode usar o botão **Filtrar** (ao lado da caixa Pesquisar) para selecionar **Exclusão pendente** para ver todas as entradas excluídas que estão pendentes de publicação.

### <a name="view-the-change-history-for-site-entries"></a>Exibir o histórico de alterações para entradas do site

Para exibir o histórico de alterações das entradas do site:

- Selecione a entrada do site para a qual você deseja ver o histórico de alterações, e depois selecione **Exibir histórico**.

### <a name="copy-a-site-to-other-site-lists"></a>Copiar um site para outras listas de sites

Use as etapas a seguir para copiar uma entrada de site de uma lista de sites para uma ou mais listas de sites.

1. Escolha uma entrada de site que você gostaria de copiar para outra lista. Selecione **Copiar para mais listas**.
2. Selecione uma ou mais listas de sites para as quais você deseja copiar na lista suspensa.
3. Selecione **Copiar site** na parte inferior do painel.
4. Depois de ver a confirmação de que uma entrada de site foi copiada, ela permanecerá na lista de sites da qual você a copiou. Ele também aparecerá nas listas de sites para os quais você copiou.

   > [!NOTE]
   > A coluna **Status** para quaisquer entradas copiadas para uma lista de sites publicados mostrará **Adição pendente**. Se você navegar até a lista de listas de sites selecionando **listas de sites do Microsoft Edge** na parte superior da tela, verá que a coluna **Status de publicação** mostra **Alterações de publicação pendentes** para indicar que as atualizações mais recentes da lista de sites precisam ser publicadas para que os usuários as recebam. Você pode usar o botão **Filtrar** (ao lado da caixa Pesquisar) para selecionar **Adição pendente** para ver todas as entradas adicionadas que estão pendentes de publicação.

### <a name="add-a-shared-cookie-to-the-site-list"></a>Adicionar um cookie compartilhado à lista sites

Você pode adicionar cookies compartilhados individuais a qualquer lista de sites. Depois de adicionar cookies compartilhados à lista, você pode usar os filtros predefinidos usando o botão **Filtrar** (ao lado da caixa Pesquisar) para visualizar as atualizações da lista.

1. Vá para a lista de sites onde deseja adicionar um cookie compartilhado.
2. Selecione **Adicionar um cookie compartilhado**.
3. Insira o domínio e o nome do cookie. Adicione comentários conforme necessário e selecione **Salvar**.

> [!NOTE]
> A coluna **Status** para quaisquer entradas adicionadas a uma lista de sites publicados mostrará **Adição pendente**. Se você navegar até a lista de listas de sites selecionando **Listas de sites do Microsoft Edge** na parte superior da tela, verá que a coluna **Status da publicação** mostra as **Alterações pendentes de publicação** para indicar que as atualizações mais recentes da lista de sites precisam ser publicadas para que os usuários as recebam. Você pode usar o botão **Filtrar** (ao lado da caixa Pesquisar) para selecionar **Adição pendente** para ver todas as entradas adicionadas que estão pendentes de publicação.

### <a name="delete-a-shared-cookie-from-the-site-list"></a>Excluir um cookie compartilhado da lista sites

Use as etapas a seguir para excluir uma entrada de cookie compartilhada.

1. Escolha a entrada que você deseja excluir da lista de sites. Selecione **Excluir cookie compartilhado**.
2. Selecione **Excluir** no pop-up da caixa de diálogo.
3. Depois de ver a confirmação de que uma entrada foi excluída, ela permanecerá na lista até que a lista de sites seja publicada no local da nuvem. Você pode exibir a lista de cookies compartilhados excluídos antes de publicar selecionando o botão **Filtrar** e filtrando por cookies no estado **Exclusão pendente**.

> [!NOTE]
> A coluna **Status** para quaisquer entradas excluídas de uma lista de sites publicados mostrará **Exclusão pendente**. Se você navegar até a lista de listas de sites selecionando **Listas de sites do Microsoft Edge** na parte superior da tela, verá que a coluna **Status da publicação** mostra as **Alterações pendentes de publicação** para indicar que as atualizações mais recentes da lista de sites precisam ser publicadas para que os usuários as recebam. Você pode usar o botão **Filtrar** (ao lado da caixa Pesquisar) para selecionar **Exclusão pendente** para ver todas as entradas excluídas que estão pendentes de publicação.

### <a name="view-the-change-history-for-shared-cookies"></a>Visualizar o histórico de alterações dos cookies compartilhados

Para exibir o histórico de alterações dos cookies compartilhados:

- Selecione a entrada para a qual você deseja ver o histórico de alterações, e depois selecione **Exibir histórico**.

### <a name="copy-a-shared-cookie-to-other-site-lists"></a>Copiar um cookie compartilhado para outras listas de sites

Siga as etapas a seguir para copiar uma entrada de cookie compartilhada de uma lista de sites para uma ou mais listas de sites.

1. Escolha uma entrada que você gostaria de copiar para outra lista. Selecione **Copiar para mais listas**.
2. Selecione uma ou mais listas de sites para as quais você deseja copiar na lista suspensa.
3. Selecione **Copiar cookie** na parte inferior do painel.
4. Depois de ver a confirmação de que uma entrada de site foi copiada, ela permanecerá na lista de sites da qual você a copiou. Ele também aparecerá nas listas de sites para os quais você copiou.

> [!NOTE]
> A coluna **Status** para quaisquer entradas copiadas para uma lista de sites publicados mostrará **Adição pendente**. Se você navegar até a lista de listas de sites selecionando **listas de sites do Microsoft Edge** na parte superior da tela, verá que a coluna **Status de publicação** mostra **Alterações de publicação pendentes** para indicar que as atualizações mais recentes da lista de sites precisam ser publicadas para que os usuários as recebam. Você pode usar o botão **Filtrar** (ao lado da caixa Pesquisar) para selecionar **Adição pendente** para ver todas as entradas adicionadas que estão pendentes de publicação.

### <a name="export-a-site-list"></a>Exportar uma lista de sites

Há cenários em que você deseja exportar uma lista de sites. Por exemplo, se você não conseguir mover sua lista de sites para a nuvem imediatamente ou se precisar manter um ambiente híbrido com listas de sites na nuvem e no local. Você pode usar a experiência de Gerenciamento de Lista de Sites na Nuvem para gerenciar atualizações para uma lista de sites em um local central e exportar a lista de sites para o host local.

Para exportar uma lista de sites:

1. Na página listas de sites do Microsoft Edge, selecione a lista de sites que você deseja exportar.
2. Selecione **Exportar lista** para baixar o arquivo XML da lista de sites

## <a name="view-site-feedback-on-the-microsoft-365-admin-center"></a>Exibir comentários do site no Centro de administração do Microsoft 365

A guia Comentários do site mostra os sites que os usuários estão adicionando à lista de sites do modo IE local, bem como sites neutros potencialmente configurados incorretamente relatados pelo Microsoft Edge. Você verá o endereço do site, o número de usuários que estão adicionando esse site e de qual lista de sites publicada e hospedada na nuvem os comentários vieram. Você pode agir em uma entrada individual adicionando-a a uma lista de sites existente, pausando ou excluindo os comentários. Você também pode exibir o histórico de alterações e os comentários.

> [!NOTE]
> No momento, esse recurso está disponível apenas para instâncias de nuvem em todo o mundo.

### <a name="add-a-site-to-site-lists"></a>Adicionar um site a listas de sites

Use as etapas a seguir para adicionar um site a uma ou mais listas de sites de comentários do site.

1. Escolha a entrada que você deseja adicionar. Selecione **Adicionar a listas de sites**.  
2. Selecione uma ou mais listas de sites a serem adicionadas na lista suspensa. Escolha o mecanismo que deve ser usado para abrir o site e adicionar comentários conforme necessário.
3. Selecione **Adicionar site** na parte inferior do painel.

   > [!NOTE]
   > O status dessa entrada será atualizado para **Resolvido** porque foi **Adicionado**. Este site agora aparecerá nas listas de sites selecionadas.

### <a name="pause-incoming-feedback-on-a-site"></a>Pausar comentários de entrada em um site

Você pode adiar a ação em uma entrada pendente pausando comentários. Você pode pausar comentários por 30 dias ou indefinidamente. Use as etapas a seguir para pausar os comentários de entrada.  

1. Escolha uma entrada em que você deseja pausar comentários. Selecione **Pausar Comentários**.  
2. Adicione comentários conforme necessário e selecione por quanto tempo você gostaria de pausar comentários.  
3. Selecione **Pausar** na parte inferior do painel.

    > [!NOTE]
    > O status dessa entrada será atualizado para **Resolvido** porque foi **Pausado**. Se você pausar por 30 dias, depois de 30 dias, se houver algum comentário de entrada, o status da entrada será atualizado novamente para **Pendente** para que você aja.

### <a name="delete-feedback-on-a-site"></a>Excluir comentários em um site

Use as etapas a seguir para excluir uma entrada de comentários.

1. Escolha a entrada que você deseja excluir. Selecione **Excluir comentários**.
2. Selecione **Excluir** na caixa de diálogo pop-up.

    > [!NOTE]
    > Se você excluir uma entrada, ela poderá reaparecer no futuro como comentários de entrada se os usuários continuarem a adicionar o site às listas de sites locais ou se o Microsoft Edge detectá-lo como um site neutro potencialmente configurado incorretamente.

### <a name="view-the-change-history-for-site-feedback-entries"></a>Exibir o histórico de alterações para entradas do site

Para exibir o histórico de alterações:

- Selecione a entrada do site para a qual você deseja ver o histórico de alterações e selecione **Histórico de comentários** no painel lateral.

## <a name="faq"></a>Perguntas frequentes

### <a name="i-dont-see-the-microsoft-edge-site-lists-option-in-the-org-settings-page-on-microsoft-365-admin-center-why-is-that"></a>Não vejo a opção "listas de sites do Microsoft Edge" na página "Configurações da organização" no Centro de administração do Microsoft 365. Por quê?

A experiência estará disponível quando a distribuição for concluída em meados de dezembro. Enquanto a experiência está sendo distribuída, você precisará optar por exibir essa experiência no Centro de Administração Microsoft 365. Você deve ser um administrador global no Microsoft 365 para aceitar.

Você pode usar as seguintes etapas para optar por:

1. Entre no [Centro de Administração Microsoft 365](https://admin.microsoft.com) e vá para  **Configurações>Configurações da organização**. Na guia  **Perfil da organização** , escolha **Preferências de versão**.
2. Para desabilitar a versão direcionada, selecione **Versão Padrão**e, em seguida, selecione **Salvar alterações**.
3. Para habilitar a versão direcionada para todos os usuários em sua organização, selecione **Lançamento direcionado para todos** e selecione  **Salvar alterações**.
4. Para habilitar a versão direcionada para algumas pessoas em sua organização, selecione  **Lançamento direcionado para usuários selecionados** e selecione  **Salvar alterações**.
5. Escolha **Selecionar usuários** para adicionar usuários um de cada vez, ou **Carregar usuários** para adicioná-los em massa.
6. Quando terminar de adicionar usuários, selecione  **Salvar alterações**.

Para obter mais informações, consulte [Configurar as opções de versão Padrão ou Direcionada – Administrador do Microsoft 365](/microsoft-365/admin/manage/release-options-in-office-365)

### <a name="when-i-select-microsoft-edge-site-lists-and-try-to-create-a-new-list-i-get-this-error---request-failed-with-status-code-500-why-is-that"></a>Quando seleciono “Listas de sites do Microsoft Edge” e tento criar uma nova lista, recebo esse erro - “Falha na solicitação com o código de status 500”. Por quê?

As Listas de Sites do Microsoft Edge armazena seus dados e configurações em uma infraestrutura de serviço compartilhada com serviços de nuvem corporativos, tais como Exchange Online, SharePoint Online, Teams e Microsoft Azure AD. Em casos raros, quando as listas de sites do Microsoft Edge são o primeiro recurso a usar essa infraestrutura, o provisionamento pode levar algum tempo. Nesses casos, a solicitação inicial do Centro de Administração do Microsoft 365 falhará. Quando a solicitação falhar, um alerta será enviado ao sistema de provisionamento para resolver o problema. Normalmente, o provisionamento é concluído em três dias. Portanto, se você receber esse erro, tente novamente em alguns dias e crie uma nova lista. Se você ainda não conseguiu criar uma nova lista ou se precisar de assistência urgente, contate o Suporte da Microsoft.

### <a name="can-users-who-havent-signed-in-to-microsoft-edge-download-the-site-list"></a>Os usuários que ainda não entraram no Microsoft Edge podem baixar a lista de sites?

Não, os usuários devem entrar no navegador para baixar a lista de sites hospedados na nuvem. Você pode configurar uma política para permitir a Entrada Implícita para impedir a interrupção da experiência do usuário. Para obter mais informações, consulte [ImplicitSignInEnabled](/DeployEdge/microsoft-edge-policies#implicitsigninenabled).

### <a name="what-is-the-default-refresh-interval-after-updates-are-made-to-site-list-contents"></a>Qual é o intervalo de atualização padrão depois que as atualizações são feitas no conteúdo da lista de sites?

A lista de sites é atualizada no Microsoft Edge a cada duas horas. Você pode alterar esse intervalo na política [InternetExplorerIntegrationSiteListRefreshInterval.](/deployedge/microsoft-edge-policies#internetexplorerintegrationsitelistrefreshinterval) O intervalo mínimo de atualização é de 30 minutos.

### <a name="what-happens-if-users-log-out-of-microsoft-edge"></a>O que acontece se os usuários saírem do Microsoft Edge?

O acesso à lista de sites requer entrada explícita no navegador para o primeiro download. Em um cenário em que o usuário faz logoff depois de fazer logon, a lista de sites é armazenada em cache no Microsoft Edge. A lista permanecerá armazenada em cache mesmo se o usuário fizer logoff do Microsoft Edge de sua conta do Azure Active Directory (Azure AD). Microsoft Edge não tentará fazer fallback para o local de download não na nuvem enquanto a política de lista de sites de nuvem estiver configurada. Microsoft Edge tenta atualizar a lista de sites armazenados em cache nos seguintes horários (observe que todas as tentativas falharão se o usuário não estiver conectado ao Microsoft Edge):

- 60 segundos depois de reiniciar o navegador.
- A cada duas horas quando o Microsoft Edge está em execução. O intervalo de atualização de 120 minutos pode ser alterado usando a política [InternetExplorerIntegrationSiteListRefreshInterval](/deployedge/microsoft-edge-policies#internetexplorerintegrationsitelistrefreshinterval). O intervalo mínimo de atualização é de 30 minutos.

## <a name="support-and-feedback"></a>Suporte e Comentários

O suporte para a experiência de Gerenciamento de Lista de Sites na Nuvem é coberto pelo contrato de [Suporte Premier da Microsoft](https://www.microsoft.com/unifiedsupport/premier) existente. Você pode entrar em contato com Suporte da Microsoft para relatar problemas ou comentários. Você também pode deixar comentários em nosso [Fórum TechCommunity](https://techcommunity.microsoft.com/t5/enterprise/bd-p/EdgeInsiderEnterprise).

## <a name="see-also"></a>Consulte também

- [Sobre o modo IE](./edge-ie-mode.md)
- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
