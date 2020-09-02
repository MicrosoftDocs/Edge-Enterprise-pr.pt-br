---
title: Configurações e experimentação do Microsoft Edge
ms.author: kvice
author: dan-wesley
manager: srugh
ms.date: 02/20/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Configurações e experimentação do Microsoft Edge
ms.openlocfilehash: f66da4075c33c1f375dfb593c1a1bd2b4a139833
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979030"
---
# <span data-ttu-id="ec9ba-103">Configurações e experimentação do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="ec9ba-103">Microsoft Edge configurations and experimentation</span></span>

<span data-ttu-id="ec9ba-104">Este artigo descreve a interação entre o Microsoft Edge e o ECS (Experimentation and Configuration Service).</span><span class="sxs-lookup"><span data-stu-id="ec9ba-104">This article describes the interaction between Microsoft Edge and the Experimentation and Configuration Service (ECS).</span></span> <span data-ttu-id="ec9ba-105">O Microsoft Edge se comunica com esse serviço para solicitar e receber tipos diferentes de carga.</span><span class="sxs-lookup"><span data-stu-id="ec9ba-105">Microsoft Edge communicates with this service to request and receive different kinds of payloads.</span></span> <span data-ttu-id="ec9ba-106">Essas cargas incluem configurações, distribuições de recursos e experimentos.</span><span class="sxs-lookup"><span data-stu-id="ec9ba-106">These payloads include configurations, feature rollouts, and experiments.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ec9ba-107">Certifique-se de que os clientes possam acessar o `https://config.edge.skype.com` para que as cargas possam ser recebidas.</span><span class="sxs-lookup"><span data-stu-id="ec9ba-107">Make sure clients are able to access `https://config.edge.skype.com` so payloads can be received.</span></span>

> [!NOTE]
> <span data-ttu-id="ec9ba-108">Isso aplica-se ao Microsoft Edge versão 77 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="ec9ba-108">This applies to Microsoft Edge version 77 or later.</span></span>

## <span data-ttu-id="ec9ba-109">Configurações</span><span class="sxs-lookup"><span data-stu-id="ec9ba-109">Configurations</span></span>

<span data-ttu-id="ec9ba-110">As configurações são a carga que se destina a garantir a integridade, a segurança e a conformidade de privacidade do produto, e devem ter o mesmo valor para todos os usuários (com base em plataformas e canais). Isso pode ser a habilitação de um sinalizador de recurso para uma ação de domínio e também pode ser usado para desabilitar um sinalizador de recurso no caso de um bug.</span><span class="sxs-lookup"><span data-stu-id="ec9ba-110">Configurations are the payload meant to ensure product health, security, and privacy compliance, and are intended to have the same value for all the users (based on platforms and channels.) This could be to enable a feature flag for a domain action, and can also be used to disable a feature flag in the event of a bug.</span></span>

## <span data-ttu-id="ec9ba-111">Distribuição Controlada de Recursos</span><span class="sxs-lookup"><span data-stu-id="ec9ba-111">Controlled Feature Rollout</span></span>

<span data-ttu-id="ec9ba-112">A Distribuição Controlada de Recursos (CFR) é um procedimento para aumentar lentamente o tamanho do grupo de usuários que recebe um recurso.</span><span class="sxs-lookup"><span data-stu-id="ec9ba-112">Controlled Feature Rollout (CFR) is a procedure for slowly increasing the size of the user group that receives a feature.</span></span> <span data-ttu-id="ec9ba-113">Ao distribuir um novo recurso para um subconjunto da população de usuários selecionado aleatoriamente, será possível comparar os comentários do usuário com um grupo de controles do mesmo tamanho, sem o recurso de medir o impacto do recurso.</span><span class="sxs-lookup"><span data-stu-id="ec9ba-113">By distributing a new feature to a randomly selected subset of the user population, it’s possible to compare user feedback to an equally sized control group without the feature to measure the impact of the feature.</span></span>

## <span data-ttu-id="ec9ba-114">Experimentos</span><span class="sxs-lookup"><span data-stu-id="ec9ba-114">Experiments</span></span>

<span data-ttu-id="ec9ba-115">Os builds do Microsoft Edge têm recursos e funcionalidades que ainda estão em desenvolvimento ou são experimentais.</span><span class="sxs-lookup"><span data-stu-id="ec9ba-115">Microsoft Edge builds have features and functionality that are still in development or are experimental.</span></span> <span data-ttu-id="ec9ba-116">Os Experimentos são como a CFR, mas o tamanho do grupo de usuários é muito menor para testar o novo conceito.</span><span class="sxs-lookup"><span data-stu-id="ec9ba-116">Experiments are like CFR, but the size of the user group is much smaller for testing the new concept.</span></span> <span data-ttu-id="ec9ba-117">Esses recursos ficam ocultos por padrão até que o recurso seja distribuído ou o experimento seja concluído.</span><span class="sxs-lookup"><span data-stu-id="ec9ba-117">These features are hidden by default until the feature's rolled out or the experiment's finished.</span></span> <span data-ttu-id="ec9ba-118">Os sinalizadores de experimento são usados para habilitar e desabilitar esses recursos.</span><span class="sxs-lookup"><span data-stu-id="ec9ba-118">Experiment flags are used to enable and disable these features.</span></span>

## <span data-ttu-id="ec9ba-119">Sobre o ECS</span><span class="sxs-lookup"><span data-stu-id="ec9ba-119">About the ECS</span></span>

<span data-ttu-id="ec9ba-120">Em todos os cenários anteriores, o serviço fornece os valores de sinalizador de recurso para o cliente do navegador para que eles possam ser aplicados.</span><span class="sxs-lookup"><span data-stu-id="ec9ba-120">In all the preceding scenarios, the service delivers the feature flag values to the browser client so they can be applied.</span></span> <span data-ttu-id="ec9ba-121">Dependendo da atualização, as configurações são aplicadas imediatamente ou quando o usuário reinicia o navegador.</span><span class="sxs-lookup"><span data-stu-id="ec9ba-121">Depending on the update, configurations are applied immediately or when the user restarts the browser.</span></span>

<span data-ttu-id="ec9ba-122">A interação do Microsoft Edge com esse serviço é controlada por configurações na política [ExperimentationAndConfigurationServiceControl](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#experimentationandconfigurationservicecontrol).</span><span class="sxs-lookup"><span data-stu-id="ec9ba-122">Microsoft Edge's interaction with this service is controlled by settings in the [ExperimentationAndConfigurationServiceControl](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#experimentationandconfigurationservicecontrol) policy.</span></span> <span data-ttu-id="ec9ba-123">Você pode definir as configurações de política para:</span><span class="sxs-lookup"><span data-stu-id="ec9ba-123">You can configure policy settings to:</span></span>

- <span data-ttu-id="ec9ba-124">Recuperar somente configurações</span><span class="sxs-lookup"><span data-stu-id="ec9ba-124">Retrieve configurations only</span></span>
- <span data-ttu-id="ec9ba-125">Recuperar configurações e experimentos</span><span class="sxs-lookup"><span data-stu-id="ec9ba-125">Retrieve configurations and experiments</span></span>
- <span data-ttu-id="ec9ba-126">Desabilitar a comunicação com o serviço</span><span class="sxs-lookup"><span data-stu-id="ec9ba-126">Disable communication with the service</span></span>

  > [!CAUTION]
  > <span data-ttu-id="ec9ba-127">Se você desabilitar as comunicações com o serviço, isso afetará a capacidade da Microsoft de responder a um bug grave de maneira oportuna.</span><span class="sxs-lookup"><span data-stu-id="ec9ba-127">If you disable communications with the service, this will affect Microsoft’s ability to respond to a severe bug in a timely manner.</span></span>

## <span data-ttu-id="ec9ba-128">Consulte também</span><span class="sxs-lookup"><span data-stu-id="ec9ba-128">See also</span></span>

- [<span data-ttu-id="ec9ba-129">Página de aterrissagem do Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="ec9ba-129">Microsoft Edge Enterprise landing page</span></span>](https://www.microsoftedgeinsider.com/enterprise)
- [<span data-ttu-id="ec9ba-130">Página de aterrissagem da documentação do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="ec9ba-130">Microsoft Edge documentation landing page</span></span>](https://docs.microsoft.com/DeployEdge/)
