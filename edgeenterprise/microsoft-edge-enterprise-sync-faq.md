---
title: Perguntas frequentes sobre a sincronização empresarial do Microsoft Edge
ms.author: scottbo
author: dan-wesley
manager: silvanam
ms.date: 03/08/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Perguntas frequentes sobre a sincronização empresarial do Microsoft Edge.
ms.openlocfilehash: e25ee985f65ee61dda5cacece73d43be7f1e6d7d
ms.sourcegitcommit: f363ceb6c42054fabc95ce8d7bca3c52d80e6a9f
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/24/2021
ms.locfileid: "11447865"
---
# <a name="microsoft-edge-enterprise-sync-faq"></a><span data-ttu-id="cd320-103">Perguntas frequentes sobre a sincronização empresarial do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="cd320-103">Microsoft Edge enterprise sync FAQ</span></span>

<span data-ttu-id="cd320-104">Este artigo responde a perguntas frequentes sobre a sincronização empresarial do Microsoft Edge versão 77 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="cd320-104">This article answers frequently asked questions about enterprise sync for Microsoft Edge version 77 or later.</span></span>

## <a name="security-and-serverdata-compliance"></a><span data-ttu-id="cd320-105">Segurança e Conformidade com o Servidor/Dados</span><span class="sxs-lookup"><span data-stu-id="cd320-105">Security and Server/Data Compliance</span></span>

### <a name="is-the-synced-data-encrypted"></a><span data-ttu-id="cd320-106">Os dados sincronizados estão criptografados?</span><span class="sxs-lookup"><span data-stu-id="cd320-106">Is the synced data encrypted?</span></span>

<span data-ttu-id="cd320-107">Os dados são criptografados no transporte usando TLS 1.2 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="cd320-107">The data is encrypted in transport using TLS 1.2 or greater.</span></span> <span data-ttu-id="cd320-108">Todos os tipos de dados também são criptografados como descansar no serviço da Microsoft usando o AES128.</span><span class="sxs-lookup"><span data-stu-id="cd320-108">All data types are additionally encrypted at rest in Microsoft's service using AES128.</span></span> <span data-ttu-id="cd320-109">Todos os tipos de dados, exceto os usados na guia aberta e na sincronização do histórico, são adicionalmente criptografados antes de deixar o dispositivo do usuário com chaves gerenciadas através da política da [Proteção de Informações do Microsoft Azure](./microsoft-edge-policies.md#restrictsignintopattern).</span><span class="sxs-lookup"><span data-stu-id="cd320-109">All data types except those used for open tab and history sync are additionally encrypted before leaving the user’s device with keys managed via the [Azure Information Protection](./microsoft-edge-policies.md#restrictsignintopattern) policy.</span></span>

### <a name="why-dont-open-tab-and-history-data-have-more-client-side-encryption"></a><span data-ttu-id="cd320-110">Por que a guia aberta e os dados do histórico não têm mais criptografia do lado do cliente?</span><span class="sxs-lookup"><span data-stu-id="cd320-110">Why don’t open tab and history data have more client-side encryption?</span></span>

<span data-ttu-id="cd320-111">Para reduzir o uso de recursos nos dispositivos do usuário final, os dados do histórico são gerados no lado do servidor com base nos dados de roaming da guia aberta.</span><span class="sxs-lookup"><span data-stu-id="cd320-111">To reduce resource utilization on end-user devices, history data is generated server-side based on open tab roaming data.</span></span> <span data-ttu-id="cd320-112">Este processo não seria possível com a criptografia ao lado do cliente desses dados.</span><span class="sxs-lookup"><span data-stu-id="cd320-112">This process would not be possible with client-side encryption of this data.</span></span> <span data-ttu-id="cd320-113">Para desabilitar a guia aberta e a sincronização do histórico, aplique as políticas [SavingBrowserHistoryDisabled](./microsoft-edge-policies.md#savingbrowserhistorydisabled) ou [SyncTypesListDisabled](./microsoft-edge-policies.md#synctypeslistdisabled) .</span><span class="sxs-lookup"><span data-stu-id="cd320-113">To disable open tab and history sync, apply the [SavingBrowserHistoryDisabled](./microsoft-edge-policies.md#savingbrowserhistorydisabled) or [SyncTypesListDisabled](./microsoft-edge-policies.md#synctypeslistdisabled) policies.</span></span>

### <a name="can-tenant-admins-bring-their-own-key"></a><span data-ttu-id="cd320-114">Os administradores de locatários podem ter suas próprias chaves?</span><span class="sxs-lookup"><span data-stu-id="cd320-114">Can tenant admins bring their own key?</span></span>

<span data-ttu-id="cd320-115">Sim, pela [Proteção de informações do Azure](https://azure.microsoft.com/services/information-protection/).</span><span class="sxs-lookup"><span data-stu-id="cd320-115">Yes, through [Azure Information Protection](https://azure.microsoft.com/services/information-protection/).</span></span>

### <a name="where-is-microsoft-edge-sync-data-stored"></a><span data-ttu-id="cd320-116">Onde os dados sincronizados são armazenados no Microsoft Edge?</span><span class="sxs-lookup"><span data-stu-id="cd320-116">Where is Microsoft Edge sync data stored?</span></span>

<span data-ttu-id="cd320-117">Os dados sincronizados para contas do Azure AD são armazenados em servidores seguros de acordo com a ID do locatário.</span><span class="sxs-lookup"><span data-stu-id="cd320-117">Synced data for Azure AD accounts is stored in secure servers according to the tenant ID.</span></span> <span data-ttu-id="cd320-118">Por exemplo, os dados de um locatário registrado nos Estados Unidos são armazenados em servidores localizados geograficamente nessa região e aproveitam a mesma solução de armazenamento usada pelos aplicativos do Office.</span><span class="sxs-lookup"><span data-stu-id="cd320-118">For example, the data for a tenant that is registered in the United States is stored in servers geo-located for that region and uses the same storage solution as Office applications.</span></span>

### <a name="does-the-data-ever-leave-microsofts-cloud-aside-from-syncing-to-microsoft-edge"></a><span data-ttu-id="cd320-119">Os dados deixam a nuvem da Microsoft, além de sincronizar com o Microsoft Edge?</span><span class="sxs-lookup"><span data-stu-id="cd320-119">Does the data ever leave Microsoft's cloud, aside from syncing to Microsoft Edge?</span></span>

<span data-ttu-id="cd320-120">Não.</span><span class="sxs-lookup"><span data-stu-id="cd320-120">No.</span></span>

### <a name="what-terms-of-service-does-enterprise-sync-fall-under"></a><span data-ttu-id="cd320-121">Em que termos de serviço a sincronização empresarial se encaixa?</span><span class="sxs-lookup"><span data-stu-id="cd320-121">What terms of service does enterprise sync fall under?</span></span>

<span data-ttu-id="cd320-122">Os termos de serviço da sincronização do Microsoft Edge se enquadram na licença de software da Microsoft exibida no Microsoft Edge em *Edge://terms*.</span><span class="sxs-lookup"><span data-stu-id="cd320-122">Terms of service for Microsoft Edge sync falls under the Microsoft software license viewable in Microsoft Edge at *edge://terms*.</span></span> <span data-ttu-id="cd320-123">A sua assinatura e os termos de serviço do Azure AD estão, em última análise, em [Termos de serviço on-line](https://www.microsoft.com/licensing/product-licensing/products)da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="cd320-123">Your Azure AD subscription and terms of service ultimately fall under Microsoft's [Online Service Terms](https://www.microsoft.com/licensing/product-licensing/products).</span></span>

### <a name="does-microsoft-edge-support-government-community-cloud-gcc-high-compliance"></a><span data-ttu-id="cd320-124">O Microsoft Edge dá suporte á conformidade do Government Community Cloud (GCC) High?</span><span class="sxs-lookup"><span data-stu-id="cd320-124">Does Microsoft Edge support Government Community Cloud (GCC) High compliance?</span></span>

<span data-ttu-id="cd320-125">Não atualmente.</span><span class="sxs-lookup"><span data-stu-id="cd320-125">Not today.</span></span> <span data-ttu-id="cd320-126">A sincronização do Microsoft Edge está desabilitada para os clientes na nuvem do GCC High.</span><span class="sxs-lookup"><span data-stu-id="cd320-126">For customers in the GCC High cloud, Microsoft Edge sync is disabled.</span></span>

## <a name="applying-sync"></a><span data-ttu-id="cd320-127">Aplicar Sincronização</span><span class="sxs-lookup"><span data-stu-id="cd320-127">Applying Sync</span></span>

### <a name="why-isnt-microsoft-edge-sync-supported-in-all-m365-subscriptions"></a><span data-ttu-id="cd320-128">Por que a sincronização do Microsoft Edge não é compatível com todas as assinaturas do M365?</span><span class="sxs-lookup"><span data-stu-id="cd320-128">Why isn’t Microsoft Edge sync supported in all M365 subscriptions?</span></span>

<span data-ttu-id="cd320-129">A sincronização empresarial depende da [Proteção de Informações do Azure,](https://azure.microsoft.com/services/information-protection/)que não está disponível em todas as assinaturas do M365.</span><span class="sxs-lookup"><span data-stu-id="cd320-129">Enterprise sync depends on [Azure Information Protection](https://azure.microsoft.com/services/information-protection/), which is not available in all M365 subscriptions.</span></span>

### <a name="is-microsoft-edge-sync-based-on-enterprise-state-roaming"></a><span data-ttu-id="cd320-130">A sincronização do Microsoft Edge é baseada no Enterprise State Roaming?</span><span class="sxs-lookup"><span data-stu-id="cd320-130">Is Microsoft Edge sync based on Enterprise State Roaming?</span></span>

<span data-ttu-id="cd320-131">Não.</span><span class="sxs-lookup"><span data-stu-id="cd320-131">No.</span></span> <span data-ttu-id="cd320-132">O ESR pode ser usado para habilitar a sincronização, mas a sincronização do Microsoft Edge não faz parte do ESR.</span><span class="sxs-lookup"><span data-stu-id="cd320-132">ESR can be used to enable sync, but Microsoft Edge sync is not a part of ESR.</span></span> <span data-ttu-id="cd320-133">Para obter mais informações, consulte [Sincronização do Microsoft Edge](https://review.docs.microsoft.com/DeployEdge/microsoft-edge-enterprise-sync) e [Microsoft Edge e Enterprise State Roaming](https://review.docs.microsoft.com/DeployEdge/microsoft-edge-enterprise-state-roaming).</span><span class="sxs-lookup"><span data-stu-id="cd320-133">For more information, see [Microsoft Edge Sync](https://review.docs.microsoft.com/DeployEdge/microsoft-edge-enterprise-sync) and [Microsoft Edge and Enterprise State Roaming](https://review.docs.microsoft.com/DeployEdge/microsoft-edge-enterprise-state-roaming).</span></span>

### <a name="will-microsoft-edge-ever-support-syncing-between-microsoft-edge-and-ie"></a><span data-ttu-id="cd320-134">O Microsoft Edge oferecerá suporte para sincronização entre o Microsoft Edge e o IE?</span><span class="sxs-lookup"><span data-stu-id="cd320-134">Will Microsoft Edge ever support syncing between Microsoft Edge and IE?</span></span>

<span data-ttu-id="cd320-135">Não há planos para dar suporte a essa sincronização.</span><span class="sxs-lookup"><span data-stu-id="cd320-135">There are no plans to support this syncing.</span></span> <span data-ttu-id="cd320-136">Se você ainda precisar do IE no seu ambiente para oferecer suporte aos aplicativos herdados, considere o nosso [novo modo do IE](./edge-ie-mode.md).</span><span class="sxs-lookup"><span data-stu-id="cd320-136">If you still need IE in your environment to support legacy apps, consider our [new IE mode](./edge-ie-mode.md).</span></span>

### <a name="will-microsoft-edge-sync-with-microsoft-edge-legacy"></a><span data-ttu-id="cd320-137">O Microsoft Edge será sincronizado com o Microsoft Edge herdado?</span><span class="sxs-lookup"><span data-stu-id="cd320-137">Will Microsoft Edge sync with Microsoft Edge Legacy?</span></span>

<span data-ttu-id="cd320-138">Não.</span><span class="sxs-lookup"><span data-stu-id="cd320-138">No, it won't.</span></span> <span data-ttu-id="cd320-139">Acreditamos que a conexão destes dois ecossistemas comprometerá a confiabilidade da sincronia no Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="cd320-139">We believe connecting these two ecosystems will lead to compromises in the reliability of sync in the Microsoft Edge.</span></span> <span data-ttu-id="cd320-140">Garantiremos que os dados existentes serão migrados para o Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="cd320-140">We will ensure that existing data is migrated to the Microsoft Edge.</span></span> <span data-ttu-id="cd320-141">Os usuários também poderão importar dados do navegador de sua escolha, o que também significa que o Microsoft Edge não terá uma maneira de sincronizar com o IE.</span><span class="sxs-lookup"><span data-stu-id="cd320-141">Users will also be able to import data from browser of their choice, which also means that Microsoft Edge won't have a way to sync with IE.</span></span>

## <a name="managing-sync"></a><span data-ttu-id="cd320-142">Gerenciar Sincronização</span><span class="sxs-lookup"><span data-stu-id="cd320-142">Managing Sync</span></span>

### <a name="is-it-possible-to-stop-my-users-from-syncing-with-a-personal-tenant"></a><span data-ttu-id="cd320-143">É possível impedir que os meus usuários sincronizem com um locatário pessoal?</span><span class="sxs-lookup"><span data-stu-id="cd320-143">Is it possible to stop my users from syncing with a personal tenant?</span></span>

<span data-ttu-id="cd320-144">Não diretamente, mas você pode determinar quais perfis podem entrar no Microsoft Edge usando a política [RestrictSigninToPattern](./microsoft-edge-policies.md#restrictsignintopattern).</span><span class="sxs-lookup"><span data-stu-id="cd320-144">Not directly, but you can determine which profiles can sign on to Microsoft Edge using the [RestrictSigninToPattern](./microsoft-edge-policies.md#restrictsignintopattern) policy.</span></span>

## <a name="see-also"></a><span data-ttu-id="cd320-145">Ver também</span><span class="sxs-lookup"><span data-stu-id="cd320-145">See also</span></span>

- [<span data-ttu-id="cd320-146">Sincronização do Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="cd320-146">Microsoft Edge Enterprise Sync</span></span>](microsoft-edge-enterprise-sync.md)
- [<span data-ttu-id="cd320-147">Microsoft Edge e Enterprise State Roaming</span><span class="sxs-lookup"><span data-stu-id="cd320-147">Microsoft Edge and Enterprise State Roaming</span></span>](microsoft-edge-enterprise-state-roaming.md)
- [<span data-ttu-id="cd320-148">Página de aterrissagem do Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="cd320-148">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)