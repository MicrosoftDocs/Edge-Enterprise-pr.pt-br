---
title: Lista de permissões para pontos de extremidade do Microsoft Edge
ms.author: kvice
author: dan-wesley
manager: srugh
ms.date: 06/09/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Lista de permissões para pontos de extremidade do Microsoft Edge
ms.openlocfilehash: 76186524a708861432199d5da7eec7573ebecb96
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979163"
---
# <span data-ttu-id="33e58-103">Lista de permissões para pontos de extremidade do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="33e58-103">Allow list for Microsoft Edge endpoints</span></span>

<span data-ttu-id="33e58-104">O Microsoft Edge requer conectividade com a Internet para dar suporte aos recursos.</span><span class="sxs-lookup"><span data-stu-id="33e58-104">Microsoft Edge requires connectivity to the Internet to support its features.</span></span> <span data-ttu-id="33e58-105">Este artigo identifica as URLs de domínio que você precisa adicionar à Lista de permissões para garantir a comunicação por meio de firewalls e outros mecanismos de segurança.</span><span class="sxs-lookup"><span data-stu-id="33e58-105">This article identifies the domain URLs that you need to add to the Allow list to ensure communications through firewalls and other security mechanisms.</span></span>

> [!NOTE]
> <span data-ttu-id="33e58-106">Isso se aplica ao Microsoft Edge versão 77 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="33e58-106">This applies  to Microsoft Edge version 77 or later.</span></span>

## <span data-ttu-id="33e58-107">URLs de domínio a serem permitidas</span><span class="sxs-lookup"><span data-stu-id="33e58-107">Domain URLs to allow</span></span>

<span data-ttu-id="33e58-108">Permita as URLs de domínio a seguir para o Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="33e58-108">Allow the following domain URLs for Microsoft Edge.</span></span>

### <span data-ttu-id="33e58-109">Serviço de Atualização</span><span class="sxs-lookup"><span data-stu-id="33e58-109">Update Service</span></span>

<span data-ttu-id="33e58-110">O serviço que o Microsoft Edge usa para verificar se há novas atualizações.</span><span class="sxs-lookup"><span data-stu-id="33e58-110">The service that Microsoft Edge uses to check for new updates.</span></span>

- `https://msedge.api.cdp.microsoft.com`

### <span data-ttu-id="33e58-111">Serviço Experimentação e Configuração</span><span class="sxs-lookup"><span data-stu-id="33e58-111">Experimentation and Configuration service</span></span>

- `https://config.ecs.skype.com`

### <span data-ttu-id="33e58-112">Locais de download para o Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="33e58-112">Download locations for Microsoft Edge</span></span>

<span data-ttu-id="33e58-113">Locais de onde o Microsoft Edge pode ser baixado durante uma instalação inicial ou quando uma atualização está disponível.</span><span class="sxs-lookup"><span data-stu-id="33e58-113">Locations Microsoft Edge can be downloaded from during an initial install or when an update is available.</span></span> <span data-ttu-id="33e58-114">O local de download é determinado pelo Serviço de Atualização.</span><span class="sxs-lookup"><span data-stu-id="33e58-114">The download location is determined by the Update Service.</span></span>

#### <span data-ttu-id="33e58-115">HTTP</span><span class="sxs-lookup"><span data-stu-id="33e58-115">HTTP</span></span>

- `http://msedge.f.tlu.dl.delivery.mp.microsoft.com`
- `http://msedge.f.dl.delivery.mp.microsoft.com`
- `http://msedge.b.tlu.dl.delivery.mp.microsoft.com`
- `http://msedge.b.dl.delivery.mp.microsoft.com`

#### <span data-ttu-id="33e58-116">HTTPS</span><span class="sxs-lookup"><span data-stu-id="33e58-116">HTTPS</span></span>

- `https://msedge.sf.tlu.dl.delivery.mp.microsoft.com`
- `https://msedge.sf.dl.delivery.mp.microsoft.com`
- `https://msedge.sb.tlu.dl.delivery.mp.microsoft.com`
- `https://msedge.sb.dl.delivery.mp.microsoft.com`

  > [!TIP]
  > <span data-ttu-id="33e58-117">Para simplificar a lista de permissões para locais de download, é possível usar um curinga:</span><span class="sxs-lookup"><span data-stu-id="33e58-117">To simplify the allow list for download locations a wild card can be used:</span></span> `*.dl.delivery.mp.microsoft.com`

### <span data-ttu-id="33e58-118">Locais de download para Extensões do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="33e58-118">Download locations for Microsoft Edge Extensions</span></span>

<span data-ttu-id="33e58-119">Locais de onde as Extensões do Microsoft Edge podem ser baixadas durante uma instalação inicial ou quando uma atualização está disponível.</span><span class="sxs-lookup"><span data-stu-id="33e58-119">Locations Microsoft Edge Extensions can be downloaded from during an initial install or when an update is available.</span></span> <span data-ttu-id="33e58-120">O local de download é determinado pelo Serviço de Atualização.</span><span class="sxs-lookup"><span data-stu-id="33e58-120">The download location is determined by the Update Service.</span></span>

#### <span data-ttu-id="33e58-121">HTTP</span><span class="sxs-lookup"><span data-stu-id="33e58-121">HTTP</span></span>

- `http://msedgeextensions.f.tlu.dl.delivery.mp.microsoft.com`
- `http://msedgeextensions.f.dl.delivery.mp.microsoft.com`
- `http://msedgeextensions.b.tlu.dl.delivery.mp.microsoft.com`
- `http://msedgeextensions.b.dl.delivery.mp.microsoft.com`

#### <span data-ttu-id="33e58-122">HTTPS</span><span class="sxs-lookup"><span data-stu-id="33e58-122">HTTPS</span></span>

- `https://msedgeextensions.sf.tlu.dl.delivery.mp.microsoft.com`
- `https://msedgeextensions.sf.dl.delivery.mp.microsoft.com`
- `https://msedgeextensions.sb.tlu.dl.delivery.mp.microsoft.com`
- `https://msedgeextensions.sb.dl.delivery.mp.microsoft.com`

  > [!TIP]
  > <span data-ttu-id="33e58-123">Para simplificar a lista de permissões para locais de download, é possível usar um curinga:</span><span class="sxs-lookup"><span data-stu-id="33e58-123">To simplify the allow list for download locations a wild card can be used:</span></span> `*.dl.delivery.mp.microsoft.com`

### <span data-ttu-id="33e58-124">Opcionalmente para a Otimização de Entrega de Downloads</span><span class="sxs-lookup"><span data-stu-id="33e58-124">Optionally for Download Delivery Optimization</span></span>

<span data-ttu-id="33e58-125">Para obter informações sobre a otimização de entrega, consulte [Otimização de Entrega para atualizações do Windows 10](https://aka.ms/waas-do).</span><span class="sxs-lookup"><span data-stu-id="33e58-125">For information about delivery optimization, see [Delivery Optimization for Windows 10 updates](https://aka.ms/waas-do).</span></span>

- <span data-ttu-id="33e58-126">Comunicação entre Cliente e Serviço: `*.do.dsp.mp.microsoft.com` (Porta HTTP 80, Porta HTTPS 443)</span><span class="sxs-lookup"><span data-stu-id="33e58-126">Client to Service communication: `*.do.dsp.mp.microsoft.com` (HTTP Port 80, HTTPS Port 443)</span></span>
- <span data-ttu-id="33e58-127">Comunicação entre Clientes: a porta TCP 7680 deve estar aberta para o tráfego de entrada</span><span class="sxs-lookup"><span data-stu-id="33e58-127">Client to Client communication: TCP port 7680 should be open for inbound traffic</span></span>

### <span data-ttu-id="33e58-128">Sync</span><span class="sxs-lookup"><span data-stu-id="33e58-128">Sync</span></span>

<span data-ttu-id="33e58-129">Esses pontos de extremidade gerenciam a leitura e a escrita de dados sincronizados, o gerenciamento de direitos para proteger os dados e a notificação do navegador quando novos dados de sincronização estiverem disponíveis.</span><span class="sxs-lookup"><span data-stu-id="33e58-129">These endpoints manage the reading and writing of synced data, rights management for secure data, and notifying the browser when new sync data is available.</span></span>

- <span data-ttu-id="33e58-130">Pontos de extremidade do serviço de sincronização do Edge:</span><span class="sxs-lookup"><span data-stu-id="33e58-130">Edge sync service endpoints:</span></span>

  - `https://enterprise.edge.activity.windows.com`
  - `https://edge.activity.windows.com`

- <span data-ttu-id="33e58-131">Pontos de extremidade da Proteção de Informações do Azure:</span><span class="sxs-lookup"><span data-stu-id="33e58-131">Azure Information Protection endpoints:</span></span>

  - `https://api.aadrm.com` <span data-ttu-id="33e58-132">(para a maioria dos locatários)</span><span class="sxs-lookup"><span data-stu-id="33e58-132">(for most tenants)</span></span>
  - `https://api.aadrm.de` <span data-ttu-id="33e58-133">(para locatários na Alemanha)</span><span class="sxs-lookup"><span data-stu-id="33e58-133">(for tenants in Germany)</span></span>
  - `https://api.aadrm.cn` <span data-ttu-id="33e58-134">(para locatários na China)</span><span class="sxs-lookup"><span data-stu-id="33e58-134">(for tenants in China)</span></span>

- [<span data-ttu-id="33e58-135">Pontos de extremidade do Serviço de Notificação do Windows</span><span class="sxs-lookup"><span data-stu-id="33e58-135">Windows Notification Service endpoints</span></span>](https://docs.microsoft.com/windows/uwp/design/shell/tiles-and-notifications/firewall-allowlist-config)

## <span data-ttu-id="33e58-136">Outros serviços de suporte do navegador</span><span class="sxs-lookup"><span data-stu-id="33e58-136">Other browser support services</span></span>

<span data-ttu-id="33e58-137">Fornecem metadados para recursos do navegador, como proteção contra rastreamento, listas de certificados revogados e outras atualizações de componentes do navegador.</span><span class="sxs-lookup"><span data-stu-id="33e58-137">Provide metadata for browser features such as tracking protection, certificate revocation lists, and other browser component updates.</span></span> <span data-ttu-id="33e58-138">Fornecem dicionários de verificação ortográfica e listas de bloqueio de anúncios para download.</span><span class="sxs-lookup"><span data-stu-id="33e58-138">Provide downloadable spellcheck dictionaries and ad-blocking block lists.</span></span> <span data-ttu-id="33e58-139">Fornecem serviços para dar suporte a recursos do navegador como coleções, autopreenchimento e repositório de extensões.</span><span class="sxs-lookup"><span data-stu-id="33e58-139">Provide services to support browser features such as collections, autofill, and extension store.</span></span>

- `http://edge.microsoft.com/`
- `https://edge.microsoft.com/`

## <span data-ttu-id="33e58-140">Consulte também</span><span class="sxs-lookup"><span data-stu-id="33e58-140">See also</span></span>

- [<span data-ttu-id="33e58-141">Página de aterrissagem do Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="33e58-141">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="33e58-142">Página de aterrissagem da documentação do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="33e58-142">Microsoft Edge documentation landing page</span></span>](https://docs.microsoft.com/DeployEdge/)
- [<span data-ttu-id="33e58-143">Gerenciar pontos de extremidade de conexão do Windows 10 Enterprise, versão 1903</span><span class="sxs-lookup"><span data-stu-id="33e58-143">Manage connection endpoints for Windows 10 Enterprise, version 1903</span></span>](https://docs.microsoft.com/windows/privacy/manage-windows-1903-endpoints)
