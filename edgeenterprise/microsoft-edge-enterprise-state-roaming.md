---
title: Microsoft Edge e Enterprise State Roaming
ms.author: kvice
author: dan-wesley
manager: laurawi
ms.date: 02/14/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Microsoft Edge e Enterprise State Roaming
ms.openlocfilehash: 6090ecfda2f792d49e452771943bc6348066a3d8
ms.sourcegitcommit: 90b8eab62edbed0e0a84780abd7d3854bf95c130
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "11328053"
---
# <span data-ttu-id="e80cb-103">Microsoft Edge e Enterprise State Roaming</span><span class="sxs-lookup"><span data-stu-id="e80cb-103">Microsoft Edge and Enterprise State Roaming</span></span>

<span data-ttu-id="e80cb-104">Este artigo explica como a participação do Microsoft Edge na oferta do Enterprise State Roaming (ESR) está mudando para oferecer um suporte melhor à sincronização entre plataformas e dispositivos.</span><span class="sxs-lookup"><span data-stu-id="e80cb-104">This article explains how Microsoft Edge participation in the Enterprise State Roaming (ESR) offering is changing to better support sync across platforms and devices.</span></span>

> [!NOTE]
> <span data-ttu-id="e80cb-105">Este artigo se aplica ao Microsoft Edge versão 77 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="e80cb-105">This article applies to Microsoft Edge version 77 or later.</span></span>

## <span data-ttu-id="e80cb-106">Introdução</span><span class="sxs-lookup"><span data-stu-id="e80cb-106">Introduction</span></span>

<span data-ttu-id="e80cb-107">Com o Windows 10, os usuários do [Azure Active Directory (Azure AD)](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-whatis) têm a possibilidade de sincronizar de maneira segura as configurações de usuário e os dados das configurações do aplicativo com a nuvem.</span><span class="sxs-lookup"><span data-stu-id="e80cb-107">With Windows 10, [Azure Active Directory (Azure AD)](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-whatis) users gained the ability to securely synchronize their user settings and application settings data to the cloud.</span></span> <span data-ttu-id="e80cb-108">O [Enterprise State Roaming (ESR)](https://docs.microsoft.com/azure/active-directory/devices/enterprise-state-roaming-overview) oferece aos usuários uma experiência unificada em todos os dispositivos Windows e reduz o tempo necessário para configurar um novo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e80cb-108">[Enterprise State Roaming (ESR)](https://docs.microsoft.com/azure/active-directory/devices/enterprise-state-roaming-overview) provides users with a unified experience across their Windows devices and reduces the time needed for configuring a new device.</span></span>

<span data-ttu-id="e80cb-109">Como parte da adoção da plataforma Chromium pelo Microsoft Edge, sua solução de sincronização agora está desconectada da estrutura de sincronização do Windows.</span><span class="sxs-lookup"><span data-stu-id="e80cb-109">As part of Microsoft Edge adopting the Chromium platform, its sync solution is now disconnected from Windows sync framework.</span></span> <span data-ttu-id="e80cb-110">Isso afeta a relação do Microsoft Edge com a oferta de ESR.</span><span class="sxs-lookup"><span data-stu-id="e80cb-110">This affects the relationship of Microsoft Edge to the ESR offering.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e80cb-111">O novo Microsoft Edge não participa da oferta de ESR.</span><span class="sxs-lookup"><span data-stu-id="e80cb-111">The new Microsoft Edge does not participate in the ESR offering.</span></span>

## <span data-ttu-id="e80cb-112">O que mudará no Microsoft Edge?</span><span class="sxs-lookup"><span data-stu-id="e80cb-112">What’s changing with Microsoft Edge?</span></span>

<span data-ttu-id="e80cb-113">Com o novo Microsoft Edge, a solução de sincronização não está vinculada ao ecossistema de sincronização do Windows.</span><span class="sxs-lookup"><span data-stu-id="e80cb-113">With the new Microsoft Edge, the sync solution isn’t tied to Windows sync ecosystem.</span></span> <span data-ttu-id="e80cb-114">Isso nos permite oferecer o Microsoft Edge em todas as plataformas, como Windows 7, Windows 8.1, iOS, Android e macOS.</span><span class="sxs-lookup"><span data-stu-id="e80cb-114">This enables us to offer Microsoft Edge across all the platforms, such as Windows 7, Windows 8.1, iOS, Android and macOS.</span></span> <span data-ttu-id="e80cb-115">Isso também nos permite oferecer sincronização para contas não primárias no Windows.</span><span class="sxs-lookup"><span data-stu-id="e80cb-115">This also enables us to offer sync for non-primary accounts on Windows.</span></span> <span data-ttu-id="e80cb-116">Além disso, podemos fornecer o Microsoft Edge em uma cadência de lançamento mais frequente e flexível que a do Windows.</span><span class="sxs-lookup"><span data-stu-id="e80cb-116">In addition, we can ship Microsoft Edge at a more frequent and flexible release cadence than Windows.</span></span> <span data-ttu-id="e80cb-117">(Para obter mais informações, consulte [Atualizações do Windows para oferecer suporte à próxima versão do Microsoft Edge](microsoft-edge-sysupdate-windows-updates.md).</span><span class="sxs-lookup"><span data-stu-id="e80cb-117">(For more information, see [Windows updates to support the next version of Microsoft Edge](microsoft-edge-sysupdate-windows-updates.md).</span></span> <span data-ttu-id="e80cb-118">Todos esses fatores destacaram a necessidade de reavaliar a participação do Microsoft Edge na oferta de ESR.</span><span class="sxs-lookup"><span data-stu-id="e80cb-118">All these factors highlighted the need to re-assess Microsoft Edge participation in the ESR offering.</span></span>

<span data-ttu-id="e80cb-119">O ESR é enquadrado como uma oferta de produto do Windows com promessas sobre como os dados de dispositivos Windows são manipulados, mas a sincronização do Microsoft Edge vai além dos dispositivos Windows.</span><span class="sxs-lookup"><span data-stu-id="e80cb-119">ESR is framed as a Windows product offering with promises about how data from Windows devices is handled, but Microsoft Edge sync will extend beyond Windows devices.</span></span> <span data-ttu-id="e80cb-120">E, à medida que os dados transitam por esses dispositivos, é difícil definir a oferta de sincronização do Microsoft Edge no contexto do ESR.</span><span class="sxs-lookup"><span data-stu-id="e80cb-120">And, as the data roams across these devices, it makes it difficult to define the Microsoft Edge sync offering in the context of ESR.</span></span> <span data-ttu-id="e80cb-121">Para simplificar a maneira como a sincronização funciona e é gerenciada, e para acomodar as alterações destacadas, foi tomada a decisão de tirar o Microsoft Edge da oferta de ESR.</span><span class="sxs-lookup"><span data-stu-id="e80cb-121">To simplify how sync works and is managed, and to accommodate the changes that are highlighted, a decision was made to pull Microsoft Edge out of the ESR offering.</span></span>

## <span data-ttu-id="e80cb-122">Isso significa que as empresas perderão as capacidades que tinham como parte do ESR?</span><span class="sxs-lookup"><span data-stu-id="e80cb-122">Does this mean Enterprises will lose the abilities they had as part of ESR?</span></span>

<span data-ttu-id="e80cb-123">Não.</span><span class="sxs-lookup"><span data-stu-id="e80cb-123">No.</span></span> <span data-ttu-id="e80cb-124">O Microsoft Edge continuará dando suporte à maioria das capacidades fornecidas na oferta de ESR.</span><span class="sxs-lookup"><span data-stu-id="e80cb-124">Microsoft Edge will continue to support most of the abilities provided in the ESR offering.</span></span>

### <span data-ttu-id="e80cb-125">Experiência unificada entre dispositivos e novo tempo de configuração de dispositivo</span><span class="sxs-lookup"><span data-stu-id="e80cb-125">Unified experience across devices and new device configuration time</span></span>

<span data-ttu-id="e80cb-126">Quando um usuário se conecta ao seu dispositivo Windows com uma conta do Azure Active Directory (AAD), o Microsoft Edge herda implicitamente essa identidade na primeira inicialização do novo navegador.</span><span class="sxs-lookup"><span data-stu-id="e80cb-126">When a user is signed into their windows device with an Azure Active Directory (Azure AD account), Microsoft Edge will implicitly inherit that Identity on first launch of the new browser.</span></span>

<span data-ttu-id="e80cb-127">Depois que o usuário autorizar explicitamente a ativação da sincronização no novo Microsoft Edge, o navegador sincronizará todos os dados do navegador, como favoritos, senhas e histórico.</span><span class="sxs-lookup"><span data-stu-id="e80cb-127">After a user has explicitly consented to turning on sync in the new Microsoft Edge, the browser will sync all the browser data, such as favorites, passwords, and history.</span></span> <span data-ttu-id="e80cb-128">Isso garante uma experiência unificada em todos os dispositivos e reduz o tempo necessário para personalizar o navegador.</span><span class="sxs-lookup"><span data-stu-id="e80cb-128">This ensures a unified experience across devices and reduces the time needed to personalize the browser.</span></span>

### <span data-ttu-id="e80cb-129">Separação de dados corporativos e do consumidor</span><span class="sxs-lookup"><span data-stu-id="e80cb-129">Separation of corporate and consumer data</span></span>

<span data-ttu-id="e80cb-130">As organizações estão no controle dos dados, e não há mistura de dados corporativos em uma conta de nuvem do consumidor ou de dados do consumidor em uma conta de nuvem corporativa.</span><span class="sxs-lookup"><span data-stu-id="e80cb-130">Organizations are in control of their data, and there is no mixing of corporate data in a consumer cloud account or consumer data in an enterprise cloud account.</span></span>

### <span data-ttu-id="e80cb-131">Segurança reforçada</span><span class="sxs-lookup"><span data-stu-id="e80cb-131">Enhanced security</span></span>

<span data-ttu-id="e80cb-132">Os dados são criptografados automaticamente antes de saírem do dispositivo Windows 10 do usuário usando a Proteção de Informações do Azure, e os dados permanecem criptografados em repouso na nuvem.</span><span class="sxs-lookup"><span data-stu-id="e80cb-132">Data is automatically encrypted before leaving the user’s Windows 10 device by using Azure Information Protection, and data stays encrypted at rest in the cloud.</span></span> <span data-ttu-id="e80cb-133">Todo o conteúdo continua criptografado em repouso na nuvem, exceto os namespaces, como nomes de configurações.</span><span class="sxs-lookup"><span data-stu-id="e80cb-133">All content stays encrypted at rest in the cloud, except for the namespaces, like settings names.</span></span>

### <span data-ttu-id="e80cb-134">Monitoramento</span><span class="sxs-lookup"><span data-stu-id="e80cb-134">Monitoring</span></span>

<span data-ttu-id="e80cb-135">Forneceremos controle e visibilidade sobre quem sincroniza as configurações em sua organização e em quais dispositivos por meio da integração com o portal do Azure AD.</span><span class="sxs-lookup"><span data-stu-id="e80cb-135">We will provide control and visibility over who syncs settings in your organization and on which devices through integration with the Azure AD portal.</span></span> <span data-ttu-id="e80cb-136">Essa funcionalidade será habilitada em uma versão futura.</span><span class="sxs-lookup"><span data-stu-id="e80cb-136">This capability will be enabled in a future release.</span></span>

### <span data-ttu-id="e80cb-137">Gerenciamento</span><span class="sxs-lookup"><span data-stu-id="e80cb-137">Management</span></span>

<span data-ttu-id="e80cb-138">Os administradores poderão controlar quais membros em sua organização podem habilitar a sincronização. Consulte [Configurar a sincronização do Microsoft Edge](microsoft-edge-enterprise-sync.md#configure-microsoft-edge-sync) e [Sincronizar políticas de grupo](microsoft-edge-enterprise-sync.md#sync-group-policies).</span><span class="sxs-lookup"><span data-stu-id="e80cb-138">Admins will be able to control which members in your organization can enable sync. See [Configure Microsoft Edge sync](microsoft-edge-enterprise-sync.md#configure-microsoft-edge-sync) and [Sync group policies](microsoft-edge-enterprise-sync.md#sync-group-policies).</span></span> <span data-ttu-id="e80cb-139">Além disso, os usuários podem ativar/desativar a sincronização para cada um dos seus dispositivos, bem como alternar cada atributo de dados individualmente para sincronização.</span><span class="sxs-lookup"><span data-stu-id="e80cb-139">Additionally, users can turn sync on/off for each of their devices as well as toggle each data attribute individually for sync.</span></span>

### <span data-ttu-id="e80cb-140">Gerenciamento de chaves</span><span class="sxs-lookup"><span data-stu-id="e80cb-140">Key management</span></span>

<span data-ttu-id="e80cb-141">O recurso de sincronização usa a Proteção de Informações do Azure (AIP) para proteger os dados sincronizados somente para o usuário e os administradores corporativos.</span><span class="sxs-lookup"><span data-stu-id="e80cb-141">The synchronization feature leverages Azure Information Protection (AIP) to protect the synchronized data for only the user and the enterprise admins.</span></span> <span data-ttu-id="e80cb-142">O AIP oferece suporte a dispositivos gerenciados pela Microsoft (padrão) e com a própria chave para gerenciamento de chaves na nuvem.</span><span class="sxs-lookup"><span data-stu-id="e80cb-142">AIP supports both Microsoft managed (default) and bring your own key for cloud-key management.</span></span> <span data-ttu-id="e80cb-143">A estratégia de gerenciamento de chaves na nuvem usada por sua organização é transparente para o Microsoft Edge e não tem impacto sobre o recurso de sincronização.</span><span class="sxs-lookup"><span data-stu-id="e80cb-143">The cloud-key management strategy your organization uses is transparent to Microsoft Edge and has no impact on the synchronization feature.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e80cb-144">O método [Mantenha sua própria chave (HYOK)](https://docs.microsoft.com/azure/information-protection/configure-adrms-restrictions) e o Active Directory Rights Management Services não têm suporte.</span><span class="sxs-lookup"><span data-stu-id="e80cb-144">[Hold your own key (HYOK)](https://docs.microsoft.com/azure/information-protection/configure-adrms-restrictions) and the Active Directory Rights Management Service aren't supported.</span></span>

## <span data-ttu-id="e80cb-145">Resumo dos atributos de sincronização</span><span class="sxs-lookup"><span data-stu-id="e80cb-145">Summary of sync attributes</span></span>

<span data-ttu-id="e80cb-146">Os seguintes atributos de dados serão sincronizados na nova versão do Microsoft Edge na primeira inicialização:</span><span class="sxs-lookup"><span data-stu-id="e80cb-146">The following data attributes will sync in the new version of Microsoft Edge at first launch:</span></span>

- <span data-ttu-id="e80cb-147">Favoritos</span><span class="sxs-lookup"><span data-stu-id="e80cb-147">Favorites</span></span>
- <span data-ttu-id="e80cb-148">Senhas</span><span class="sxs-lookup"><span data-stu-id="e80cb-148">Passwords</span></span>
- <span data-ttu-id="e80cb-149">Preenchimento de formulários</span><span class="sxs-lookup"><span data-stu-id="e80cb-149">Form-fill</span></span>
- <span data-ttu-id="e80cb-150">Histórico</span><span class="sxs-lookup"><span data-stu-id="e80cb-150">History</span></span>
- <span data-ttu-id="e80cb-151">Guias abertas (sessões)</span><span class="sxs-lookup"><span data-stu-id="e80cb-151">Open tabs (sessions)</span></span>
- <span data-ttu-id="e80cb-152">Configurações (preferências)</span><span class="sxs-lookup"><span data-stu-id="e80cb-152">Settings (preferences)</span></span>
- <span data-ttu-id="e80cb-153">Extensões</span><span class="sxs-lookup"><span data-stu-id="e80cb-153">Extensions</span></span>

<span data-ttu-id="e80cb-154">A lista anterior de atributos é diferente dos atributos que podem ser sincronizados no Microsoft Edge Legacy.</span><span class="sxs-lookup"><span data-stu-id="e80cb-154">The preceding list of attributes is different than the attributes that could be synced in Microsoft Edge Legacy.</span></span> <span data-ttu-id="e80cb-155">(Para obter detalhes sobre as configurações do Microsoft Edge Legacy, consulte [Configurações de roaming do Windows 10](https://docs.microsoft.com/azure/active-directory/devices/enterprise-state-roaming-windows-settings-reference).) Os usuários podem habilitar/desabilitar esses atributos seletivamente usando as configurações do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="e80cb-155">(For details about Microsoft Edge Legacy settings, see [Windows 10 roaming settings](https://docs.microsoft.com/azure/active-directory/devices/enterprise-state-roaming-windows-settings-reference).) Users can selectively enable/disable these attributes using Microsoft Edge settings.</span></span> <span data-ttu-id="e80cb-156">Devido à diferença de atributos entre as duas versões (por exemplo, histórico), os usuários podem ser solicitados a autorizar a sincronização novamente.</span><span class="sxs-lookup"><span data-stu-id="e80cb-156">Given the difference in attributes between the two versions (for example, history), users might be asked to give sync consent again.</span></span>

> [!NOTE]
> <span data-ttu-id="e80cb-157">Diferentemente do Microsoft Edge Legacy, o novo Microsoft Edge não usa o Gerenciador de credenciais do Windows para senhas e, portanto, não sincroniza senhas com o Internet Explorer ou outros apps que usam o Gerenciador de credenciais do Windows.</span><span class="sxs-lookup"><span data-stu-id="e80cb-157">Unlike Microsoft Edge Legacy, the new Microsoft Edge doesn't use Windows credential Manager for passwords and as a result, won't sync passwords with Internet Explorer or other apps that use Windows Credential manager.</span></span>

## <span data-ttu-id="e80cb-158">Termos de serviço</span><span class="sxs-lookup"><span data-stu-id="e80cb-158">Terms of service</span></span>

<span data-ttu-id="e80cb-159">Os termos de serviço de sincronização do Microsoft Edge estão sujeitos à licença de software da Microsoft visível no Microsoft Edge, em *edge://terms*.</span><span class="sxs-lookup"><span data-stu-id="e80cb-159">Terms of service for Microsoft Edge sync falls under the Microsoft software license viewable in Microsoft Edge at *edge://terms*.</span></span>

## <span data-ttu-id="e80cb-160">Consulte também</span><span class="sxs-lookup"><span data-stu-id="e80cb-160">See also</span></span>

- [<span data-ttu-id="e80cb-161">Página de aterrissagem do Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="e80cb-161">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="e80cb-162">Sincronização do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="e80cb-162">Microsoft Edge Sync</span></span>](microsoft-edge-enterprise-sync.md)