---
title: Implantar o Microsoft Edge com atualizações do Windows 10
ms.author: ryhecht
author: RyanHechtMSFT
manager: tinad
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Implantar o Microsoft Edge com atualizações do Windows 10
ms.openlocfilehash: 9102ef37c6a5329a5cba79ed976237d7fd7e2063
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/09/2021
ms.locfileid: "11641887"
---
# <a name="deploy-microsoft-edge-with-windows-10-updates"></a><span data-ttu-id="c3c2c-103">Implantar o Microsoft Edge com atualizações do Windows 10</span><span class="sxs-lookup"><span data-stu-id="c3c2c-103">Deploy Microsoft Edge with Windows 10 updates</span></span>

<span data-ttu-id="c3c2c-104">O artigo fornece informações para usuários que estão implantando o Microsoft Edge usando as atualizações do Windows 10.</span><span class="sxs-lookup"><span data-stu-id="c3c2c-104">The article provides information for users who are deploying Microsoft Edge by using Windows 10 updates.</span></span>

## <a name="for-windows-10-release-20h2"></a><span data-ttu-id="c3c2c-105">Para Windows 10 versão 20H2</span><span class="sxs-lookup"><span data-stu-id="c3c2c-105">For Windows 10 release 20H2</span></span>

<span data-ttu-id="c3c2c-106">O Windows 10 versão 20H2 já tem o Microsoft Edge instalado como navegador padrão.</span><span class="sxs-lookup"><span data-stu-id="c3c2c-106">Windows 10 version 20H2 already has Microsoft Edge installed as its default browser.</span></span>

## <a name="for-windows-10-releases-rs4-through-20h1"></a><span data-ttu-id="c3c2c-107">Para Windows 10, versões RS4 a 20H1</span><span class="sxs-lookup"><span data-stu-id="c3c2c-107">For Windows 10 releases RS4 through 20H1</span></span>

<span data-ttu-id="c3c2c-108">O Windows Server Update Services (WSUS) tem atualizações para cada versão do Windows 10 de RS4 a 20H1 que removerão o aplicativo de desktop Versão Prévia do Microsoft Edge e o substituirão pelo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="c3c2c-108">Windows Server Update Services (WSUS) has updates for each version of Windows 10 from RS4 through 20H1 that will remove the Microsoft Edge Legacy desktop app and replace it with Microsoft Edge.</span></span> <span data-ttu-id="c3c2c-109">Para obter mais informações, consulte [este artigo de suporte](https://support.microsoft.com/topic/update-in-wsus-for-the-new-microsoft-edge-for-windows-10-version-1809-1903-1909-and-2004-october-29-2020-b4980418-4ec4-dee7-3b17-1c6499bd127c) para descobrir qual atualização do WSUS é a certa para a sua versão do Windows.</span><span class="sxs-lookup"><span data-stu-id="c3c2c-109">For more information, see [this support article](https://support.microsoft.com/topic/update-in-wsus-for-the-new-microsoft-edge-for-windows-10-version-1809-1903-1909-and-2004-october-29-2020-b4980418-4ec4-dee7-3b17-1c6499bd127c) to find out which WSUS update is right for your Windows version.</span></span>

## <a name="for-windows-10-releases-prior-to-rs4-and-windows-7-81-and-earlier"></a><span data-ttu-id="c3c2c-110">Para versões do Windows 10 anteriores ao RS4 (e Windows 7, 8.1 e anteriores)</span><span class="sxs-lookup"><span data-stu-id="c3c2c-110">For Windows 10 releases prior to RS4 (and Windows 7, 8.1, and earlier)</span></span>

<span data-ttu-id="c3c2c-111">As atualizações do Windows para instalar o Microsoft Edge não estão disponíveis para essas versões.</span><span class="sxs-lookup"><span data-stu-id="c3c2c-111">Windows updates to install Microsoft Edge aren't available for these versions.</span></span> <span data-ttu-id="c3c2c-112">Considere outras opções para implantar o Microsoft Edge nesses dispositivos, como [Configuration Manager](/configmgr/apps/deploy-use/deploy-edge?bc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2fbreadcrumb%2ftoc.json&toc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2ftoc.json) ou [Intune ](/intune/apps/apps-windows-edge/?bc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2fbreadcrumb%2ftoc.json&toc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2ftoc.json).</span><span class="sxs-lookup"><span data-stu-id="c3c2c-112">Consider other options for deploying Microsoft Edge to these devices such as [Configuration Manager](/configmgr/apps/deploy-use/deploy-edge?bc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2fbreadcrumb%2ftoc.json&toc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2ftoc.json) or [Intune](/intune/apps/apps-windows-edge/?bc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2fbreadcrumb%2ftoc.json&toc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2ftoc.json).</span></span>

## <a name="see-also"></a><span data-ttu-id="c3c2c-113">Veja também</span><span class="sxs-lookup"><span data-stu-id="c3c2c-113">See also</span></span>

- [<span data-ttu-id="c3c2c-114">Página de destino do Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="c3c2c-114">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="c3c2c-115">Planejar sua implantação do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="c3c2c-115">Plan your deployment of Microsoft Edge</span></span>](deploy-edge-plan-deployment.md)