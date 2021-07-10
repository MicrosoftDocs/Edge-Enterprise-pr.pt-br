---
title: Microsoft Edge em seu ambiente
ms.author: ryhecht
author: RyanHechtMSFT
manager: tinad
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Microsoft Edge em seu ambiente
ms.openlocfilehash: 2381380cb399f6a1fbb5efa9378ffeba20fa774f
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/09/2021
ms.locfileid: "11641597"
---
# <a name="microsoft-edge-in-your-environment"></a><span data-ttu-id="530a8-103">Microsoft Edge em seu ambiente</span><span class="sxs-lookup"><span data-stu-id="530a8-103">Microsoft Edge in your environment</span></span>

<span data-ttu-id="530a8-104">Este artigo descreve como se preparar para implantar o Microsoft Edge quando o Versão Prévia do Microsoft Edge chegar ao fim do serviço.</span><span class="sxs-lookup"><span data-stu-id="530a8-104">This article describes how to prepare to deploy Microsoft Edge when Microsoft Edge Legacy reaches its end of service.</span></span>

<span data-ttu-id="530a8-105">De acordo com a [postagem do blog](https://aka.ms/EdgeLegacyEOS)da Equipe de Produto do Microsoft Edge, o suporte para o aplicativo de desktop Versão Prévia do Microsoft Edge terminará em 9 de Março de 2021.</span><span class="sxs-lookup"><span data-stu-id="530a8-105">As per the Microsoft Edge Product Team’s [blog post](https://aka.ms/EdgeLegacyEOS), support for the Microsoft Edge Legacy desktop application will end on March 9, 2021.</span></span> <span data-ttu-id="530a8-106">Quando você aplica a versão Update Tuesday (ou "B") em abril, ela remove a Versão Prévia do Microsoft Edge dos dispositivos que executam o Windows 10 RS4 até 20H1 e o substitui pelo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="530a8-106">When you apply the Update Tuesday (or "B") release in April, it will remove Microsoft Edge Legacy from devices running Windows 10 RS4 through 20H1 and replace it with Microsoft Edge.</span></span>

## <a name="how-to-prepare"></a><span data-ttu-id="530a8-107">Como preparar</span><span class="sxs-lookup"><span data-stu-id="530a8-107">How to Prepare</span></span>

<span data-ttu-id="530a8-108">Para se preparar para a instalação do Microsoft Edge em dispositivos Windows 10 RS4 a 20H1 com o lançamento da terça-feira de atualização em abril, recomendamos a leitura de [Planeje sua implantação do Microsoft Edge](deploy-edge-plan-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="530a8-108">To prepare for Microsoft Edge being installed on Windows 10 RS4 through 20H1 devices with the Update Tuesday release in April, we recommend reading [Plan your deployment of Microsoft Edge](deploy-edge-plan-deployment.md).</span></span>

<span data-ttu-id="530a8-109">Depois de planejar sua implantação, use uma das abordagens a seguir para se preparar para implantar o Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="530a8-109">After you plan your deployment, use one of the following approaches to prepare to deploy Microsoft Edge.</span></span>

- <span data-ttu-id="530a8-110">**Instale políticas de grupo para personalizar sua abordagem de atualização do Microsoft Edge**.</span><span class="sxs-lookup"><span data-stu-id="530a8-110">**Install group policies to customize your Microsoft Edge update approach**.</span></span> <span data-ttu-id="530a8-111">Para obter mais informações, Consulte [Definir as configurações de política do Microsoft Edge no Windows](configure-microsoft-edge.md)e preste atenção especial ao material de referência[ da Política de Atualização](microsoft-edge-update-policies.md).</span><span class="sxs-lookup"><span data-stu-id="530a8-111">For more information, see [Configure Microsoft Edge policy settings on Windows](configure-microsoft-edge.md), and pay special attention to the [Update Policy reference](microsoft-edge-update-policies.md) material.</span></span> <span data-ttu-id="530a8-112">Se você instalar políticas de grupo para gerenciar suas atualizações antes de instalar o lançamento da terça-feira de atualização de abril, o Microsoft Edge começará a respeitar sua política imediatamente.</span><span class="sxs-lookup"><span data-stu-id="530a8-112">If you install group policies to manage your updates before installing April’s Update Tuesday release, Microsoft Edge will immediately start respecting your policy.</span></span> <span data-ttu-id="530a8-113">Se não houver nenhuma política de grupo instalada, o Microsoft Edge se atualizará automaticamente.</span><span class="sxs-lookup"><span data-stu-id="530a8-113">If there isn't any installed group policy, Microsoft Edge will automatically update itself.</span></span>

- <span data-ttu-id="530a8-114">**Remova o aplicativo de desktop Versão Prévia do Microsoft Edge antes da data de término do serviço em 9 de Março de 2021 e implante o Microsoft Edge**.</span><span class="sxs-lookup"><span data-stu-id="530a8-114">**Remove the Microsoft Edge Legacy desktop application before its end of service date of March 9, 2021 and deploy Microsoft Edge**.</span></span> <span data-ttu-id="530a8-115">Para Windows 10 RS4 a 20H1, você pode fazer isso usando as atualizações do Windows.</span><span class="sxs-lookup"><span data-stu-id="530a8-115">For Windows 10 RS4 through 20H1, you can do this by using Windows Updates.</span></span> <span data-ttu-id="530a8-116">Para obter mais informações, consulte [Implantar o Microsoft Edge com atualizações do Windows 10](deploy-edge-with-windows-10-updates.md).</span><span class="sxs-lookup"><span data-stu-id="530a8-116">For more information, see [Deploy Microsoft Edge with Windows 10 updates](deploy-edge-with-windows-10-updates.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="530a8-117">Veja também</span><span class="sxs-lookup"><span data-stu-id="530a8-117">See also</span></span>

- [<span data-ttu-id="530a8-118">Página de destino do Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="530a8-118">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="530a8-119">Planejar sua implantação do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="530a8-119">Plan your deployment of Microsoft Edge</span></span>](deploy-edge-plan-deployment.md)