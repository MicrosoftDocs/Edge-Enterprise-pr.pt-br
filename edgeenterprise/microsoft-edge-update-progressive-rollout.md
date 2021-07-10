---
title: Distribuições progressivas para atualizações do canal estável do Microsoft Edge
ms.author: aguta
author: dan-wesley
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Distribuições progressivas para atualizações do canal estável do Microsoft Edge
ms.openlocfilehash: bdcefdc118125d67057fa77513bd732cff6882e3
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/09/2021
ms.locfileid: "11642287"
---
# <a name="progressive-rollouts-for-microsoft-edge-stable-channel-updates"></a><span data-ttu-id="357a8-103">Distribuições progressivas para atualizações do canal estável do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="357a8-103">Progressive rollouts for Microsoft Edge Stable channel updates</span></span>

<span data-ttu-id="357a8-104">A partir do lançamento do Microsoft Edge 83, realizaremos distribuições progressivas de atualizações principais para o canal estável do Microsoft Edge durante alguns dias.</span><span class="sxs-lookup"><span data-stu-id="357a8-104">Starting with Microsoft Edge 83 release, we will perform gradual rollouts of major updates to Microsoft Edge Stable channel over the span of a few days.</span></span> <span data-ttu-id="357a8-105">Essa distribuição progressiva permite monitorar as atualizações e atualizar o navegador com segurança em toda a organização.</span><span class="sxs-lookup"><span data-stu-id="357a8-105">This progressive rollout allows us to monitor upgrades and safely update the browser across the organization.</span></span>

> [!NOTE]
> <span data-ttu-id="357a8-106">Isso se aplica ao canal estável do Microsoft Edge versão 83 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="357a8-106">This applies to Microsoft Edge Stable channel version 83 or later.</span></span>

## <a name="why-do-we-need-progressive-rollout"></a><span data-ttu-id="357a8-107">Por que precisamos de uma distribuição progressiva?</span><span class="sxs-lookup"><span data-stu-id="357a8-107">Why do we need progressive rollout?</span></span>

<span data-ttu-id="357a8-108">Ao monitorar a integridade das atualizações e implementar as atualizações durante esse período, podemos limitar o impacto dos problemas que podem ocorrer com a nova atualização.</span><span class="sxs-lookup"><span data-stu-id="357a8-108">By monitoring the health of our updates closely and rolling out the updates over the course of several days, we can limit the impact of issues that might occur with the new update.</span></span> <span data-ttu-id="357a8-109">Com o Microsoft Edge versão 83, as distribuições progressivas serão habilitadas para todas as versões do Windows 7, Windows 8 e 8.1 e Windows 10 no Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="357a8-109">With Microsoft Edge release 83, Progressive Rollouts will be enabled for all Windows 7, Windows 8 & 8.1, and Windows 10 versions of Microsoft Edge.</span></span> <span data-ttu-id="357a8-110">Vamos dar suporte ao Microsoft Edge no Mac assim que estiver pronto.</span><span class="sxs-lookup"><span data-stu-id="357a8-110">We will support Microsoft Edge on Mac as soon as it is ready.</span></span>

## <a name="how-will-the-updates-work"></a><span data-ttu-id="357a8-111">Como as atualizações funcionarão?</span><span class="sxs-lookup"><span data-stu-id="357a8-111">How will the updates work?</span></span>

<span data-ttu-id="357a8-112">Todas as instalações do Microsoft Edge recebem um valor de atualização.</span><span class="sxs-lookup"><span data-stu-id="357a8-112">Each installation of Microsoft Edge is assigned an upgrade value.</span></span> <span data-ttu-id="357a8-113">Quando começarmos a distribuição progressiva, você verá a atualização quando o valor no seu dispositivo estiver dentro do intervalo de valores de atualização.</span><span class="sxs-lookup"><span data-stu-id="357a8-113">When we start rolling out incrementally, you'll see the update when the value on your device falls within the upgrade value range.</span></span> <span data-ttu-id="357a8-114">À medida que a distribuição progride (dentro de alguns dias), todos os usuários eventualmente receberão a atualização.</span><span class="sxs-lookup"><span data-stu-id="357a8-114">As the rollout progresses (within a few days), all users will eventually get the update.</span></span> <span data-ttu-id="357a8-115">As atualizações de navegador com correções de segurança críticas terão uma distribuição mais rápida do que as atualizações que não possuem correções de segurança críticas.</span><span class="sxs-lookup"><span data-stu-id="357a8-115">Browser updates with critical security fixes will have a faster rollout cadence than updates that don't have critical security fixes.</span></span> <span data-ttu-id="357a8-116">Isso é feito para garantir a proteção contra vulnerabilidades.</span><span class="sxs-lookup"><span data-stu-id="357a8-116">This is done to ensure prompt protection from vulnerabilities.</span></span>

## <a name="how-does-this-affect-enterprises"></a><span data-ttu-id="357a8-117">Como isso afeta as empresas?</span><span class="sxs-lookup"><span data-stu-id="357a8-117">How does this affect enterprises?</span></span>

<span data-ttu-id="357a8-118">Os artefatos do Microsoft Edge são distribuídos para empresas usando vários mecanismos, como o Microsoft Intune, o WSUS (serviço de atualização do Windows Server) e o Gerenciador de Configurações.</span><span class="sxs-lookup"><span data-stu-id="357a8-118">Microsoft Edge artifacts are distributed to enterprises using multiple mechanisms such as Microsoft Intune, Windows Server Update Service (WSUS), and Configuration Manager.</span></span> <span data-ttu-id="357a8-119">Essas ferramentas de implantação se comportam de forma diferente com relação à distribuição progressiva:</span><span class="sxs-lookup"><span data-stu-id="357a8-119">These deployment tools behave differently with respect to Progressive Rollout:</span></span>

- <span data-ttu-id="357a8-120">As empresas que gerenciam a distribuição por meio do Microsoft Intune estão registradas para as atualizações automáticas.</span><span class="sxs-lookup"><span data-stu-id="357a8-120">Enterprises that manage distribution via Microsoft Intune are registered for auto-updates.</span></span> <span data-ttu-id="357a8-121">A distribuição progressiva é usada, e todos os usuários verão uma atualização em alguns dias.</span><span class="sxs-lookup"><span data-stu-id="357a8-121">Progressive Rollout is used, and all the users will see an update in a few days.</span></span>
- <span data-ttu-id="357a8-122">As empresas que gerenciam a distribuição por meio do WSUS (Windows Server Update Services) ou do Gerenciador de Configurações não estão registradas para as atualizações automáticas.</span><span class="sxs-lookup"><span data-stu-id="357a8-122">Enterprises that manage distribution through WSUS (Windows Server Update Services) or Configuration Manager are not registered for auto-updates.</span></span> <span data-ttu-id="357a8-123">Os administradores gerenciam e aplicam as atualizações que estarão disponíveis desde o início.</span><span class="sxs-lookup"><span data-stu-id="357a8-123">Administrators manage and apply the updates that will be available from the start.</span></span> <span data-ttu-id="357a8-124">A distribuição progressiva não afeta esse processo.</span><span class="sxs-lookup"><span data-stu-id="357a8-124">Progressive Rollout does not affect this process.</span></span>

<span data-ttu-id="357a8-125">Compartilhe seus comentários por meio da voz do usuário, do botão de comentários no aplicativo ou abaixo nos comentários, caso tenha dúvidas ou questões.</span><span class="sxs-lookup"><span data-stu-id="357a8-125">Please share your valuable feedback through user voice, the in-application feedback button, or below in the comments if you have any concerns or questions.</span></span>

## <a name="see-also"></a><span data-ttu-id="357a8-126">Consulte também</span><span class="sxs-lookup"><span data-stu-id="357a8-126">See also</span></span>

- [<span data-ttu-id="357a8-127">Página de aterrissagem do Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="357a8-127">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
