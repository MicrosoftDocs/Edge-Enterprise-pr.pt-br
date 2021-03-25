---
title: Provisionar favoritos para o Microsoft Edge
ms.author: capoon
author: dan-wesley
manager: abutcher
ms.date: 09/29/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Provisionar favoritos para o Microsoft Edge
ms.openlocfilehash: 67627fa10806435d76cecae00f79867bc5af03df
ms.sourcegitcommit: f363ceb6c42054fabc95ce8d7bca3c52d80e6a9f
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/24/2021
ms.locfileid: "11447595"
---
# <a name="provision-favorites-for-microsoft-edge"></a>Provisionar favoritos para o Microsoft Edge

Com base nos comentários dos clientes, fizemos aperfeiçoamentos no provisionamento dos favoritos. A partir do Microsoft Edge versão 85, os administradores não precisam mais criar manualmente um arquivo para provisionar os favoritos. Os administradores podem adicionar favoritos e pastas usando a interface do usuário do Microsoft Edge para gerar um arquivo que possa ser exportado para uma política de grupo.

Este artigo descreve como configurar um conjunto de favoritos e pastas para sua organização. Você pode usar a política [Configurar favoritos](//DeployEdge/microsoft-edge-policies#configure-favorites) para provisionar favoritos e pastas.

> [!NOTE]
> Este artigo se aplica ao Microsoft Edge versão 85 ou posterior.

## <a name="prerequisites-and-recommendations"></a>Pré-requisitos e recomendações

- Microsoft Edge versão 85 com o modelo administrativo apropriado instalado para políticas de grupo.
- Recomendamos que você use um novo perfil no Microsoft Edge para provisionar esses favoritos. Todos os favoritos salvos com o perfil serão incluídos na exportação.  

## <a name="provision-favorites-and-folders"></a>Provisionar favoritos e pastas

Use as etapas a seguir para provisionar favoritos e pastas para seus usuários.

1. Vá para a barra de endereços do Microsoft Edge e digite esta URL: *edge://flags/#edge-Favorites-admin-Export*.
2. Em **Exportar configuração de favoritos para administradores**, selecione **Habilitado** na lista suspensa e, em seguida, clique em **Reiniciar**.

3. Vá para a página **Favoritos** em *edge://favorites*, para que você possa adicionar os favoritos e as pastas que deseja provisionar.

<!--
4. On the **Favorites bar**, click **Add folder**. The folder structure of favorites that are set in the profile you're using will be reflected in the folder you provision for your users. The next screenshot shows "Managed favorites", the folder we'll use to provision favorites.

   ![Add a folder](media/edge-learnmore-provision-favorites/provision-favorites-add-folder.png)

   > [!TIP]
   > Add existing folders that contain favorites you want to provision for your users.

5. Select "Managed favorites" and then click **Add favorite**. The next screenshot shows the favorite we've added.

   ![Add a favorite](media/edge-learnmore-provision-favorites/provision-favorites-add-favorite.png)-->

4. Quando terminar de adicionar os favoritos e as pastas, você os exportará para que eles possam ser usados pelo política **Configurar favoritos**. Vá para a barra de endereços e navegue até *edge://favorites*, clique nas reticências "**...**" e escolha **Exportar configuração de favoritos**. A próxima captura de tela mostra as opções que você tem durante o provisionamento de favoritos.

   ![Opções de menu para trabalhar com favoritos.](media/edge-learnmore-provision-favorites/provision-favorites-menu-options.png)

5. Em **Exportar sua configuração favoritos** forneça um nome para a pasta que os usuários verão. Digite o nome da pasta e escolha o formato de Plataforma que você deseja usar. Clique em **Copiar para área de transferência**. A próxima captura de tela mostra "Favoritos gerenciados" para o nome da pasta e a plataforma é o Windows.

   ![Caixa de diálogo para exportar os favoritos para uma pasta do Windows.](media/edge-learnmore-provision-favorites/provision-favorites-export.png)

6. Na janela Editor de Política de Grupo, navegue para *Configuração do Computador/Modelos Administrativos*, e selecione **Configurar Favoritos**. Habilitar a política "Configurar Favoritos". Em **Opções:**, cole o conteúdo exportado na área de texto Configurar favoritos, em seguida, clique em **Aplicar**. A próxima captura de tela mostra um exemplo da pasta "Favoritos gerenciados" na etapa 5.

   ![Use gpedit para habilitar e configurar a política "Configurar favoritos".](media/edge-learnmore-provision-favorites/provision-favorites-gpedit.png)

7. Clique em **OK** ou **Aplicar** para salvar as configurações de política.

## <a name="see-also"></a>Consulte também

- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)