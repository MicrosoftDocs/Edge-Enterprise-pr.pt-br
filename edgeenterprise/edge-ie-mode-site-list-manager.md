---
title: 'Gerenciador de Lista de Site Empresarial no Microsoft Edge '
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 04/20/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Saiba como habilitar e usar Enterprise Site List Manager no Microsoft Edge
ms.openlocfilehash: a17225f3243e57e8f45b04991b858c592f9f75d6
ms.sourcegitcommit: 592f6e40b13e28af588473b2a75c3ae697e5db2d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/05/2022
ms.locfileid: "12505642"
---
# <a name="enterprise-site-list-manager-in-microsoft-edge"></a>Gerenciador de Lista de Sites de Empresa no Microsoft Edge

>[!Note]
> O aplicativo da área de trabalho do Internet Explorer 11 será desativado e ficará sem suporte em 15 de junho de 2022 (para obter uma lista do que está no escopo, consulte as Perguntas frequentes sobre desativação do aplicativo da área de trabalho do [Internet Explorer 11](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/internet-explorer-11-desktop-app-retirement-faq/ba-p/2366549)). Os mesmos aplicativos e sites do IE11 que você usa hoje podem abrir no Microsoft Edge com o modo Internet Explorer. [Saiba mais aqui](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/).

Este artigo explica como habilitar o acesso e usar o Gerenciador de Lista de Sites do Enterprise no Microsoft Edge para criar, editar e exportar sua Lista de Sites do Modo Enterprise para o modo Internet Explorer (IE).

> [!NOTE]
> Este artigo se aplica ao Microsoft Edge versão 89 ou posterior. A funcionalidade de cookies compartilhados está disponível Microsoft Edge versão 101 ou posterior.

## <a name="overview"></a>Visão geral

O Gerenciador de Lista de Site Empresarial é uma versão no navegador da ferramenta independente do Gerenciador de Lista de Sites Corporativos que permite criar, editar e exportar a lista de sites da sua organização. Você pode acessar o gerenciador de lista Enterprise site no *edge://compat/SiteListManager*.

Melhorias futuras na ferramenta para o modo Internet Explorer estarão disponíveis por meio Enterprise Site List Manager (*edge://compat/SiteListManager*) no Microsoft Edge. A ferramenta autônoma continuará disponível no Centro de Download, mas não obterá nenhuma atualização de recursos.

## <a name="enabling-access-to-enterprise-site-list-manager"></a>Habilitando o acesso ao Gerenciador de Lista de Site Empresarial no Microsoft Edge

Você pode configurar o acesso à ferramenta gerenciador de lista de sites usando a política de grupo [EnterpriseModeSiteListManagerAllowed](./microsoft-edge-policies.md#enterprisemodesitelistmanagerallowed) .

Se essa política estiver habilitada, os usuários verão uma opção chamada Enterprise Site List Manager no painel de navegação à esquerda *no edge://compat*. Se a política estiver desabilitada, os usuários não verão o ponto de entrada para Enterprise Site List Manager no painel de navegação esquerdo, que é o comportamento padrão.

## <a name="using-the-enterprise-site-list-manager"></a>Usando o Gerenciador de Lista de Site Empresarial

A ferramenta Gerenciador de Lista de Site Empresarial usa a versão v.2 do esquema. Se você importar um esquema de versão v.1 para o Gerenciador de Lista de Site Empresarial (esquema v.2), o XML será salvo na versão v.2 do esquema. Confira a [Orientação do esquema v.2 do modo Empresarial](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance).

### <a name="add-single-sites-to-your-site-list"></a>Adicione sites únicos à sua lista de sites  

Use as etapas a seguir para adicionar sites individuais à sua lista de sites.

> [!NOTE]
> Você só pode adicionar URLs específicos, não zonas da Internet ou Intranet.

1. No gerenciador Enterprise lista de sites,  **selecioneAdicionar um site**.
2. Insira a URL do site que você deseja adicionar, por exemplo: \<domain\>.com ou.com \<domain\>/\<path\> na caixa url.
3. Selecione uma das seguintes opções na lista **Abrir em** :

   - **IE11**. Abre o site no aplicativo IE11.
   - **Modo IE**. Abre o site no modo Internet Explorer no Microsoft Edge, se habilitado, e no aplicativo IE11, caso contrário. Confira [modo Internet Explorer no Microsoft Edge](./edge-ie-mode.md).
   - **MSEdge**. Abre o site no Microsoft Edge.
   - **Configurável**. Permite que o site participe da determinação do mecanismo do modo IE. Confira [Sites configuráveis no modo IE](./edge-learnmore-configurable-sites-ie-mode.md)
   - **Nenhum**. Abre em qualquer navegador que o usuário escolher.  

4. Em  **Modo de compatibilidade**, escolha uma das seguintes opções:

   - ** IE8Enterprise **. Carrega o site no modo Empresarial do IE8.
   - **IE7Enterprise**. Carrega o site no modo Empresarial IE7.
   - **IE[x]**. Onde [x] é o número do modo de documento e o site é carregado no modo de documento especificado.
   - **Modo padrão**. Carrega o site usando o modo de compatibilidade padrão da página.

   O caminho em um domínio pode exigir um modo de compatibilidade diferente do próprio domínio. Por exemplo, o domínio pode estar aparentemente correto no navegador IE11 padrão, mas o caminho pode ter problemas e exigir o uso do modo Empresarial. Se você adicionou o domínio anteriormente, sua escolha de compatibilidade original ainda está selecionada. No entanto, se o domínio for novo,  **IE8 Enterprise Mode**   é selecionado automaticamente.

   Enterprise modo tem precedência sobre os modos de documento, portanto, os sites que já estão incluídos na lista de sites do modo Enterprise não serão afetados por essa atualização. Esses sites continuarão a ser carregados Enterprise modo. Para obter informações mais específicas sobre o uso de modos de documento, confira [Corrigir problemas de compatibilidade da web usando modos de documento e a lista de sites do modo Empresarial](/internet-explorer/ie11-deploy-guide/fix-compat-issues-with-doc-modes-and-enterprise-mode-site-list).

5. A caixa de seleção**Permitir redirecionamento** se aplica ao tratamento de redirecionamentos do lado do servidor. Se você marcar esta caixa, os redirecionamentos do lado do servidor serão abertos no navegador especificado pela tag de abertura. Para obter mais informações, consulte `allow-redirect` os [atributos de esquema atualizados](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance#updated-schema-attributes).
6. Digite qualquer comentário sobre o site na caixa **Comentário**. Os administradores só podem ver os comentários enquanto estão nesta ferramenta e esses comentários são retidos no xml da lista de sites.
7.  **SelectAdd** para adicionar o site à sua lista de sites.

### <a name="add-shared-cookies-to-your-site-list"></a>Adicionar cookies compartilhados à sua lista de sites

Use as etapas a seguir para adicionar cookies compartilhados individuais à sua lista de sites. Para saber mais sobre o compartilhamento de cookies, consulte [o compartilhamento de cookies entre o Microsoft Edge e o Internet Explorer](/deployedge/edge-ie-mode-add-guidance-cookieshare).

1. No gerenciador Enterprise lista de sites, selecione **Adicionar um cookie compartilhado**.
2. Insira o domínio que você deseja adicionar na caixa **Domínio** . Insira o nome do cookie na caixa Nome **do** Cookie.
3. Se o cookie for um cookie somente host, verifique **Somente Host**.
4. Se necessário, insira o caminho na **caixa** Caminho.
5. Selecione uma das seguintes opções na lista mecanismo **de origem** :

   - **MSEdge**. Compartilhe cookies de sessão do Microsoft Edge para o Internet Explorer.
   - **IE11**. Compartilhe cookies de sessão do Internet Explorer para Microsoft Edge.
   - **Os dois.** Compartilhe cookies de sessão de e para Microsoft Edge Internet Explorer.

6. Insira comentários sobre o cookie compartilhado na **caixa Comentário** .
7. Selecione **Adicionar** para adicionar o cookie compartilhado.

### <a name="export-site-list-to-xml"></a>Exportar lista de sites para XML

Depois de criar sua lista de sites no Gerenciador de Lista de Site Empresarial, você pode exportar o conteúdo para um modo Enterprise (.EMIE) ou arquivo XML.

> [!NOTE]
> Esse arquivo inclui todas as URLs e cookies compartilhados e deve ser armazenado em algum lugar seguro.

Para exportar a lista de sites, siga estas etapas:

1. No gerenciador Enterprise Lista de Sites, selecione **Exportar para XML**.
2. Insira um **Número da versão** e um **Nome do arquivo**.
3. Selecione **Exportar**.

Você pode salvar o arquivo localmente ou em um compartilhamento de rede. No entanto, você deve certificar-se de implantá-lo no local especificado em sua chave de registro. Para obter mais informações, confira  [Ativar o modo Internet Explorer e usar uma lista de sites](./edge-ie-mode-policies.md).

### <a name="import-multiple-sites-and-shared-cookies-to-your-site-list"></a>Importar vários sites e cookies compartilhados para sua lista de sites

Depois de criar seu arquivo .xml, você pode adicionar sites ou cookies compartilhados em massa ao editor usando **Importar do XML**.

Se você quiser substituir todo o conteúdo no editor, selecione as reticências (**...**) e, em seguida, escolha **Limpar lista**. Depois de limpar o editor, use as etapas a seguir para importar a lista de sites.

1. No gerenciador Enterprise lista de sites, selecione **Importar do XML**.
2. Selecione **Escolher arquivo** para selecionar sua lista de sites para adicionar os sites incluídos ou cookies compartilhados à ferramenta. Escolha a lista de sites que você deseja adicionar e, em seguida, **selecione Abrir**.

   Os formatos com suporte para Importação são .xml, .emie ou .txt que contêm o esquema v.2 para Enterprise Lista de Sites do Modo de Exibição. Confira a [orientação do esquema v.2 do modo Empresarial](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance).

3.  **SelectLoadto**  adicionar os sites ou cookies compartilhados do arquivo ao editor.

Você pode salvar o arquivo localmente ou em um compartilhamento de rede. No entanto, você deve certificar-se de implantá-lo no local especificado em sua chave de registro. Para obter mais informações, confira  [Ativar o modo Internet Explorer e usar uma lista de sites](./edge-ie-mode-policies.md).

### <a name="edit-sites-in-your-site-list"></a>Editar sites em sua lista de sites

 Você pode editar atributos de entradas de site existentes no Gerenciador de Lista de Site Empresarial. Você também pode adicionar, remover ou excluir comentários associados.

1. No Enterprise Site List Manager, selecione as reticências (**...**) e escolha Editar **site** para a URL que você deseja editar.
2. Você pode editar qualquer atributo da entrada do site, exceto o URL. Selecione **Salvar** depois de concluir a edição.

   > [!NOTE]
   > Se você deseja excluir uma entrada de site, escolha **Excluir site ** na etapa 1.

3. Selecione **Exportar para XML** e salve o arquivo atualizado.

Você pode salvar o arquivo localmente ou em um compartilhamento de rede. No entanto, você deve certificar-se de implantá-lo no local especificado em sua chave de registro. Para obter mais informações, confira  [Ativar o modo Internet Explorer e usar uma lista de sites](./edge-ie-mode-policies.md).

### <a name="edit-shared-cookies-in-your-site-list"></a>Editar cookies compartilhados em sua lista de sites

Você pode editar atributos de entradas de cookie compartilhado existentes no Enterprise Site List Manager. Você também pode adicionar, remover ou excluir comentários associados. Use as etapas a seguir para editar cookies compartilhados.

1. No Enterprise Site List Manager, selecione as reticências (**...**) e escolha Editar **cookie** para o domínio que você deseja editar.
2. Você pode editar qualquer atributo da entrada do site, exceto o Domínio. Selecione **Salvar** depois de concluir a edição.

> [!NOTE]
> Se você quiser excluir uma entrada de cookie compartilhado, escolha **Excluir cookie compartilhado** na etapa 1.

### <a name="preview-your-site-list-in-xml-format"></a>Visualize a sua lista de sites em formato XML

Você pode visualizar os sites e cookies compartilhados no editor no formato XML antes de exportar e salvar em seu local de lista de sites. Selecione **a visualização** XML para abrir o arquivo em uma nova guia.

### <a name="search-in-the-enterprise-site-list-manager"></a>Pesquisar no Gerenciador de Lista de Site Empresarial

Você pode pesquisar para ver se um site ou cookie compartilhado específico já aparece em sua lista de sites para que você não tente adicioná-lo novamente.

Para pesquisar, digite parte da URL ou domínio na caixa de pesquisa no canto superior direito do editor.

## <a name="see-also"></a>Consulte também

- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Sobre o modo IE](./edge-ie-mode.md)
- [Diretrizes de esquema v.2 do modo Empresarial](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance)
- [Informações adicionais sobre o Modo Empresarial](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)