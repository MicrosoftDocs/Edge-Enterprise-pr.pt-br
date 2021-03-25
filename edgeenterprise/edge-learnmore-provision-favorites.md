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
# <a name="provision-favorites-for-microsoft-edge"></a><span data-ttu-id="f17ae-103">Provisionar favoritos para o Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="f17ae-103">Provision favorites for Microsoft Edge</span></span>

<span data-ttu-id="f17ae-104">Com base nos comentários dos clientes, fizemos aperfeiçoamentos no provisionamento dos favoritos.</span><span class="sxs-lookup"><span data-stu-id="f17ae-104">Based on customer feedback, we've made improvements to provisioning favorites.</span></span> <span data-ttu-id="f17ae-105">A partir do Microsoft Edge versão 85, os administradores não precisam mais criar manualmente um arquivo para provisionar os favoritos.</span><span class="sxs-lookup"><span data-stu-id="f17ae-105">Starting with Microsoft Edge version 85, Admins no longer have to manually craft a file to provision favorites.</span></span> <span data-ttu-id="f17ae-106">Os administradores podem adicionar favoritos e pastas usando a interface do usuário do Microsoft Edge para gerar um arquivo que possa ser exportado para uma política de grupo.</span><span class="sxs-lookup"><span data-stu-id="f17ae-106">Admins can add favorites and folders using the Microsoft Edge UI to generate a file that can be exported to a group policy.</span></span>

<span data-ttu-id="f17ae-107">Este artigo descreve como configurar um conjunto de favoritos e pastas para sua organização.</span><span class="sxs-lookup"><span data-stu-id="f17ae-107">This article describes how to provision a set of favorites and folders for your organization.</span></span> <span data-ttu-id="f17ae-108">Você pode usar a política [Configurar favoritos](//DeployEdge/microsoft-edge-policies#configure-favorites) para provisionar favoritos e pastas.</span><span class="sxs-lookup"><span data-stu-id="f17ae-108">You can use the [Configure favorites](//DeployEdge/microsoft-edge-policies#configure-favorites) policy to provision favorites and folders.</span></span>

> [!NOTE]
> <span data-ttu-id="f17ae-109">Este artigo se aplica ao Microsoft Edge versão 85 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="f17ae-109">This article applies to Microsoft Edge version 85 or later.</span></span>

## <a name="prerequisites-and-recommendations"></a><span data-ttu-id="f17ae-110">Pré-requisitos e recomendações</span><span class="sxs-lookup"><span data-stu-id="f17ae-110">Prerequisites and recommendations</span></span>

- <span data-ttu-id="f17ae-111">Microsoft Edge versão 85 com o modelo administrativo apropriado instalado para políticas de grupo.</span><span class="sxs-lookup"><span data-stu-id="f17ae-111">Microsoft Edge version 85 with the appropriate administrative template installed for group policies.</span></span>
- <span data-ttu-id="f17ae-112">Recomendamos que você use um novo perfil no Microsoft Edge para provisionar esses favoritos.</span><span class="sxs-lookup"><span data-stu-id="f17ae-112">We recommend that you use a new profile in Microsoft Edge to provision these favorites.</span></span> <span data-ttu-id="f17ae-113">Todos os favoritos salvos com o perfil serão incluídos na exportação.</span><span class="sxs-lookup"><span data-stu-id="f17ae-113">All favorites that are saved with the profile will be included in the export.</span></span>  

## <a name="provision-favorites-and-folders"></a><span data-ttu-id="f17ae-114">Provisionar favoritos e pastas</span><span class="sxs-lookup"><span data-stu-id="f17ae-114">Provision favorites and folders</span></span>

<span data-ttu-id="f17ae-115">Use as etapas a seguir para provisionar favoritos e pastas para seus usuários.</span><span class="sxs-lookup"><span data-stu-id="f17ae-115">Use the following steps to provision favorites and folders for your users.</span></span>

1. <span data-ttu-id="f17ae-116">Vá para a barra de endereços do Microsoft Edge e digite esta URL: *edge://flags/#edge-Favorites-admin-Export*.</span><span class="sxs-lookup"><span data-stu-id="f17ae-116">Go to the Microsoft Edge address bar and type this URL: *edge://flags/#edge-favorites-admin-export*.</span></span>
2. <span data-ttu-id="f17ae-117">Em **Exportar configuração de favoritos para administradores**, selecione **Habilitado** na lista suspensa e, em seguida, clique em **Reiniciar**.</span><span class="sxs-lookup"><span data-stu-id="f17ae-117">Under **Favorites configuration export for administrators**, pick **Enabled** from the dropdown list and then click **Restart**.</span></span>

3. <span data-ttu-id="f17ae-118">Vá para a página **Favoritos** em *edge://favorites*, para que você possa adicionar os favoritos e as pastas que deseja provisionar.</span><span class="sxs-lookup"><span data-stu-id="f17ae-118">Go to the **Favorites** page at *edge://favorites* so you can add the favorites and folders that you want to provision.</span></span>

<!--
4. On the **Favorites bar**, click **Add folder**. The folder structure of favorites that are set in the profile you're using will be reflected in the folder you provision for your users. The next screenshot shows "Managed favorites", the folder we'll use to provision favorites.

   ![Add a folder](media/edge-learnmore-provision-favorites/provision-favorites-add-folder.png)

   > [!TIP]
   > Add existing folders that contain favorites you want to provision for your users.

5. Select "Managed favorites" and then click **Add favorite**. The next screenshot shows the favorite we've added.

   ![Add a favorite](media/edge-learnmore-provision-favorites/provision-favorites-add-favorite.png)-->

4. <span data-ttu-id="f17ae-119">Quando terminar de adicionar os favoritos e as pastas, você os exportará para que eles possam ser usados pelo política **Configurar favoritos**.</span><span class="sxs-lookup"><span data-stu-id="f17ae-119">When you finish adding favorites and folders you'll export them so they can be used by the **Configure favorites** policy.</span></span> <span data-ttu-id="f17ae-120">Vá para a barra de endereços e navegue até *edge://favorites*, clique nas reticências "**...**" e escolha **Exportar configuração de favoritos**.</span><span class="sxs-lookup"><span data-stu-id="f17ae-120">Go to the address bar and navigate to *edge://favorites*, click the ellipsis "**…**" and choose **Export favorites configuration**.</span></span> <span data-ttu-id="f17ae-121">A próxima captura de tela mostra as opções que você tem durante o provisionamento de favoritos.</span><span class="sxs-lookup"><span data-stu-id="f17ae-121">The next screenshot shows the options you have when provisioning favorites.</span></span>

   ![Opções de menu para trabalhar com favoritos.](media/edge-learnmore-provision-favorites/provision-favorites-menu-options.png)

5. <span data-ttu-id="f17ae-123">Em **Exportar sua configuração favoritos** forneça um nome para a pasta que os usuários verão.</span><span class="sxs-lookup"><span data-stu-id="f17ae-123">Under **Export your favorites configuration** you provide a name for the folder that your users will see.</span></span> <span data-ttu-id="f17ae-124">Digite o nome da pasta e escolha o formato de Plataforma que você deseja usar.</span><span class="sxs-lookup"><span data-stu-id="f17ae-124">Type the Folder name and pick the Platform format you want to use.</span></span> <span data-ttu-id="f17ae-125">Clique em **Copiar para área de transferência**.</span><span class="sxs-lookup"><span data-stu-id="f17ae-125">Click **Copy to clipboard**.</span></span> <span data-ttu-id="f17ae-126">A próxima captura de tela mostra "Favoritos gerenciados" para o nome da pasta e a plataforma é o Windows.</span><span class="sxs-lookup"><span data-stu-id="f17ae-126">The next screenshot shows "Managed favorites" for the folder name and the platform is Windows.</span></span>

   ![Caixa de diálogo para exportar os favoritos para uma pasta do Windows.](media/edge-learnmore-provision-favorites/provision-favorites-export.png)

6. <span data-ttu-id="f17ae-128">Na janela Editor de Política de Grupo, navegue para *Configuração do Computador/Modelos Administrativos*, e selecione **Configurar Favoritos**.</span><span class="sxs-lookup"><span data-stu-id="f17ae-128">Open the Group Policy Editor, navigate to *Computer Configuration/Administrative Templates/* and pick **Configure Favorites**.</span></span> <span data-ttu-id="f17ae-129">Habilitar a política "Configurar Favoritos".</span><span class="sxs-lookup"><span data-stu-id="f17ae-129">Enable the "Configure Favorites" policy.</span></span> <span data-ttu-id="f17ae-130">Em **Opções:**, cole o conteúdo exportado na área de texto Configurar favoritos, em seguida, clique em **Aplicar**.</span><span class="sxs-lookup"><span data-stu-id="f17ae-130">Under **Options:**, paste the exported contents in the Configure favorites text area then click **Apply**.</span></span> <span data-ttu-id="f17ae-131">A próxima captura de tela mostra um exemplo da pasta "Favoritos gerenciados" na etapa 5.</span><span class="sxs-lookup"><span data-stu-id="f17ae-131">The next screenshot shows an example of the "Managed favorites" folder from step 5.</span></span>

   ![Use gpedit para habilitar e configurar a política "Configurar favoritos".](media/edge-learnmore-provision-favorites/provision-favorites-gpedit.png)

7. <span data-ttu-id="f17ae-133">Clique em **OK** ou **Aplicar** para salvar as configurações de política.</span><span class="sxs-lookup"><span data-stu-id="f17ae-133">Click **OK** or **Apply** to safe the policy settings.</span></span>

## <a name="see-also"></a><span data-ttu-id="f17ae-134">Consulte também</span><span class="sxs-lookup"><span data-stu-id="f17ae-134">See also</span></span>

- [<span data-ttu-id="f17ae-135">Página de aterrissagem do Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="f17ae-135">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)