---
title: 'Gerenciador de Lista de Site Empresarial no Microsoft Edge '
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 02/02/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 'Habilitar e usar o Gerenciador de Lista de Site Empresarial no Microsoft Edge no Microsoft Edge '
ms.openlocfilehash: 9700c2b78bba514525c4d80d211ef744dd175d2f
ms.sourcegitcommit: ff67ccc93d07588a9128e9b1fe007d5393a9d6af
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/03/2021
ms.locfileid: "11312577"
---
# Gerenciador de Lista de Site Empresarial no Microsoft Edge

Este artigo explica como habilitar o acesso e usar o Gerenciador de Lista de Site Empresarial no Microsoft Edge no Microsoft Edge para criar, editar e exportar sua Lista de Sites Corporativos para o modo Internet Explorer.

> [!NOTE]
> Este artigo se aplica ao Microsoft Edge versão 89 ou posterior. 

## Visão geral

O Gerenciador de Lista de Site Empresarial é uma versão no navegador da [ferramenta independente do Gerenciador de Lista de Sites Corporativos](https://www.microsoft.com/download/details.aspx?id=49974) que permite criar, editar e exportar a lista de sites da sua organização.

Melhorias futuras na ferramenta para o modo Internet Explorer estarão disponíveis por meio do Gerenciador de Lista de Site Empresarial no Microsoft Edge no Microsoft Edge. A ferramenta autônoma continuará disponível no Centro de Download, mas não obterá nenhuma atualização de recursos.

## Habilitando o acesso ao Gerenciador de Lista de Site Empresarial no Microsoft Edge

Você pode configurar o acesso à ferramenta usando a política de grupo [ EnterpriseModeSiteListManagerAllowed ](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#enterprisemodesitelistmanagerallowed).

Se ativado, seus usuários verão uma opção chamada do Gerenciador de Lista de Site Empresarial no painel de navegação esquerdo em *edge://compat*. Se desabilitado, os usuários não verão o ponto de entrada para Gerenciador de Lista de Site Empresarial no painel de navegação esquerdo. Este é o comportamento padrão.

## Usando o Gerenciador de Lista de Site Empresarial

A ferramenta Gerenciador de Lista de Site Empresarial usa a versão v.2 do esquema. Se você importar um esquema de versão v.1 para o Gerenciador de Lista de Site Empresarial (esquema v.2), o XML será salvo na versão v.2 do esquema. Confira a [Orientação do esquema v.2 do modo Empresarial](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance).

### Adicione sites únicos à sua lista de sites  

Use as etapas a seguir para adicionar sites individuais à sua lista de sites.

> [!NOTE]
> Você só pode adicionar URLs específicos, não zonas da Internet ou Intranet.

1. No Gerenciador de Lista de Site Empresarial, clique em  **Adicionar um site**.
2. Digite o URL do site que deseja adicionar, por exemplo: <domain>.com ou <domain>.com/<path>  na caixa URL.
3. Selecione uma das seguintes opções na lista **Abrir em** :

   - **IE11**. Abre o site no aplicativo IE11.
   - **Modo IE**. Abre o site no modo Internet Explorer no Microsoft Edge, se habilitado, e no aplicativo IE11, caso contrário. Confira [modo Internet Explorer no Microsoft Edge](https://docs.microsoft.com/deployedge/edge-ie-mode).
   - **MSEdge**. Abre o site no Microsoft Edge.
   - **Configurável**. Permite que o site participe da determinação do mecanismo do modo IE. Confira [Sites configuráveis no modo IE](https://docs.microsoft.com/deployedge/edge-learnmore-configurable-sites-ie-mode)
   - **Nenhum**. Abre em qualquer navegador que o usuário escolher.  

4. Em  **Modo de compatibilidade**, escolha uma das seguintes opções:

   - ** IE8Enterprise **. Carrega o site no modo Empresarial do IE8.
   - **IE7Enterprise**. Carrega o site no modo Empresarial IE7.
   - **IE[x]**. Onde [x] é o número do modo de documento e o site é carregado no modo de documento especificado.
   - **Modo padrão**. Carrega o site usando o modo de compatibilidade padrão da página.

   O caminho em um domínio pode exigir um modo de compatibilidade diferente do próprio domínio. Por exemplo, o domínio pode estar aparentemente correto no navegador IE11 padrão, mas o caminho pode ter problemas e exigir o uso do modo Empresarial. Se você adicionou o domínio anteriormente, sua escolha de compatibilidade original ainda está selecionada. No entanto, se o domínio for novo,  **IE8 Enterprise Mode**   é selecionado automaticamente.

   O modo Empresarial tem precedência sobre modos de documento, para que sites que já estão incluídos na lista de sites de modo Empresarial não sejam afetados por esta atualização e continuem a ser carregados no modo Empresarial, como de costume. Para obter informações mais específicas sobre o uso de modos de documento, confira [Corrigir problemas de compatibilidade da web usando modos de documento e a lista de sites do modo Empresarial](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/fix-compat-issues-with-doc-modes-and-enterprise-mode-site-list).

5. A caixa de seleção**Permitir redirecionamento** se aplica ao tratamento de redirecionamentos do lado do servidor. Se você marcar esta caixa, os redirecionamentos do lado do servidor serão abertos no navegador especificado pela tag de abertura. Para obter mais informações, confira  [aqui](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance#updated-schema-attributes).
6. Digite qualquer comentário sobre o site na caixa **Comentário**. Os administradores só podem ver os comentários enquanto estão nesta ferramenta e esses comentários são retidos no xml da lista de sites.
7. Clique em **Adicionar ** para adicionar o site à sua lista de sites.

### Exportar lista de sites para XML

Depois de criar sua lista de sites no Gerenciador de Lista de Site Empresarial, você pode exportar o conteúdo para um modo Enterprise (.EMIE) ou arquivo XML. 

> [!NOTE]
> Este arquivo inclui todos os seus URLs, incluindo suas seleções de modo de compatibilidade e deve ser armazenado em um local seguro.

Para exportar a lista de sites, siga estas etapas:

1. No Gerenciador de Lista de Sites Corporativos, clique em**Export to XML**.
2. Insira um **Número da versão** e um **Nome do arquivo**.
3. Clique em**Exportar**.

Você pode salvar o arquivo localmente ou em um compartilhamento de rede. No entanto, você deve certificar-se de implantá-lo no local especificado em sua chave de registro. Para obter mais informações, confira  [Ativar o modo Internet Explorer e usar uma lista de sites](https://docs.microsoft.com/deployedge/edge-ie-mode-policies).

### Importe vários sites para sua lista de sites

Depois de criar seu arquivo .xml, você pode adicionar sites em massa ao editor usando**Importar de XML**.

Se você deseja substituir todo o conteúdo no editor, clique nas reticências (…) e escolha **Limpar lista**. Depois de limpar o editor, use as etapas a seguir para importar o site.

1. No Gerenciador de Lista de Sites Corporativos, clique em **Importar de XML**. 
2. Clique em**Escolher arquivo** para selecionar sua lista de sites e adicionar os sites incluídos à ferramenta. Escolha a lista de sites que deseja adicionar e clique em  **Abrir**. Os formatos suportados para importação são .xml, .emie ou .txt contendo o esquema v.2 para Lista de Sites de Modo Empresarial . Confira a [orientação do esquema v.2 do modo Empresarial](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance).
3. Clique em **Carregar**  para adicionar os sites do arquivo do editor.

Você pode salvar o arquivo localmente ou em um compartilhamento de rede. No entanto, você deve certificar-se de implantá-lo no local especificado em sua chave de registro. Para obter mais informações, confira  [Ativar o modo Internet Explorer e usar uma lista de sites](https://docs.microsoft.com/deployedge/edge-ie-mode-policies).

### Editar sites em sua lista de sites

 Você pode editar atributos de entradas de site existentes no Gerenciador de Lista de Site Empresarial. Você também pode adicionar, remover ou excluir comentários associados.

1. No Gerenciador de Lista de Site Empresarial, clique nas reticências (…) e escolha **Editar site** para o URL que deseja editar.
2. Você pode editar qualquer atributo da entrada do site, exceto o URL. Clique em **Salvar** após terminar a edição.

   > [!NOTE]
   > Se você deseja excluir uma entrada de site, escolha **Excluir site ** na etapa 1.

3. Clique em **Exportar para XML** e salve o arquivo atualizado.

Você pode salvar o arquivo localmente ou em um compartilhamento de rede. No entanto, você deve certificar-se de implantá-lo no local especificado em sua chave de registro. Para obter mais informações, confira  [Ativar o modo Internet Explorer e usar uma lista de sites](https://docs.microsoft.com/deployedge/edge-ie-mode-policies).

### Visualize a sua lista de sites em formato XML

Você pode visualizar os sites no editor em formato XML antes de exportar e salvar no local da lista de sites. Clique em **Visualização XML** para abrir o arquivo em uma nova guia.

### Pesquisar no Gerenciador de Lista de Site Empresarial

Você pode pesquisar para ver se um site específico já aparece em sua lista de sites para que você não tente adicioná-lo novamente.

Para pesquisar, digite parte do URL na caixa de pesquisa  **Filtrar sites por URL** no canto superior direito do editor.

## Veja também

- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Sobre o modo IE](https://docs.microsoft.com/deployedge/edge-ie-mode)
- [Diretrizes de esquema v.2 do modo Empresarial](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance)
- [Informações adicionais sobre o Modo Empresarial](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
