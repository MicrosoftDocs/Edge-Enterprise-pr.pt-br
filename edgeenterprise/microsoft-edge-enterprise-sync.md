---
title: Sincronização do Microsoft Edge Enterprise
ms.author: scottbo
author: dan-wesley
manager: silvanam
ms.date: 08/03/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Sincronização do Microsoft Edge Enterprise
ms.openlocfilehash: a6d01356db478871a7c6b386bbb731b32dc4739a
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979127"
---
# <span data-ttu-id="4d063-103">Sincronização do Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="4d063-103">Microsoft Edge Enterprise Sync</span></span>

<span data-ttu-id="4d063-104">Este artigo explica como usar o Microsoft Edge para sincronizar seus favoritos, senhas e outros dados do navegador com todos os seus dispositivos conectados.</span><span class="sxs-lookup"><span data-stu-id="4d063-104">This article explains how to use Microsoft Edge to sync your favorites, passwords, and other browser data across all your signed-in devices.</span></span>

> [!NOTE]
> <span data-ttu-id="4d063-105">Este artigo se aplica ao Microsoft Edge versão 77 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="4d063-105">This article applies to Microsoft Edge version 77 or later.</span></span>

## <span data-ttu-id="4d063-106">Visão geral</span><span class="sxs-lookup"><span data-stu-id="4d063-106">Overview</span></span>

<span data-ttu-id="4d063-107">A sincronização do Microsoft Edge permite que os usuários acessem seus dados de navegação em todos os dispositivos conectados.</span><span class="sxs-lookup"><span data-stu-id="4d063-107">Microsoft Edge sync enables users to access their browsing data across all their signed-in devices.</span></span> <span data-ttu-id="4d063-108">Os dados com suporte na sincronização incluem:</span><span class="sxs-lookup"><span data-stu-id="4d063-108">The data supported by sync includes:</span></span>

- <span data-ttu-id="4d063-109">Favoritos</span><span class="sxs-lookup"><span data-stu-id="4d063-109">Favorites</span></span>
- <span data-ttu-id="4d063-110">Senhas</span><span class="sxs-lookup"><span data-stu-id="4d063-110">Passwords</span></span>
- <span data-ttu-id="4d063-111">Endereços e etc. (preenchimento de formulário)</span><span class="sxs-lookup"><span data-stu-id="4d063-111">Addresses and more (form-fill)</span></span>
- <span data-ttu-id="4d063-112">Coleções</span><span class="sxs-lookup"><span data-stu-id="4d063-112">Collections</span></span>
- <span data-ttu-id="4d063-113">Configurações</span><span class="sxs-lookup"><span data-stu-id="4d063-113">Settings</span></span>

<span data-ttu-id="4d063-114">A funcionalidade de sincronização é habilitada por meio do consentimento do usuário, e os usuários podem ativar ou desativar a sincronização para cada um dos tipos de dados listados acima.</span><span class="sxs-lookup"><span data-stu-id="4d063-114">Sync functionality is enabled via user consent and users can turn sync on or off for each of the data types listed above.</span></span>

> [!NOTE]
> <span data-ttu-id="4d063-115">Outros dados de configuração e conectividade do dispositivo (como nome, marca e modelo do dispositivo) são carregados para dar suporte à funcionalidade de sincronização.</span><span class="sxs-lookup"><span data-stu-id="4d063-115">Additional device connectivity and configuration data (such as device name, make and model) is uploaded to support sync functionality.</span></span>

## <span data-ttu-id="4d063-116">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="4d063-116">Prerequisites</span></span>

<span data-ttu-id="4d063-117">Atualmente, a sincronização do Microsoft Edge para as contas do Azure Active Directory (Azure AD) está disponível somente para as seguintes assinaturas:</span><span class="sxs-lookup"><span data-stu-id="4d063-117">Currently Microsoft Edge sync for Azure Active Directory (Azure AD) accounts is available for the following subscriptions:</span></span>

- <span data-ttu-id="4d063-118">Azure AD Premium( P1 e P2)</span><span class="sxs-lookup"><span data-stu-id="4d063-118">Azure AD Premium (P1 and P2)</span></span>
- <span data-ttu-id="4d063-119">M365 Business Premium</span><span class="sxs-lookup"><span data-stu-id="4d063-119">M365 Business Premium</span></span>
- <span data-ttu-id="4d063-120">Office 365 E3 e superior</span><span class="sxs-lookup"><span data-stu-id="4d063-120">Office 365 E3 and above</span></span>
- <span data-ttu-id="4d063-121">Proteção de Informações do Azure (AIP) (P1 e P2)</span><span class="sxs-lookup"><span data-stu-id="4d063-121">Azure Information Protection (AIP) (P1& P2)</span></span>
- <span data-ttu-id="4d063-122">Todas as assinaturas EDU (O365 A1 ou superior, M365 A1 ou superior, Proteção de Informações do Azure P1 ou P2 para estudantes ou professores)</span><span class="sxs-lookup"><span data-stu-id="4d063-122">All EDU subscriptions (O365 A1 or above, M365 A1 or above, or Azure Information Protection P1 or P2 for Students or Faculty)</span></span>

> [!NOTE]
> <span data-ttu-id="4d063-123">A sincronização depende do serviço de proteção oferecido pela Proteção de Informações do Azure (AIP) para proteger os dados de sincronização.</span><span class="sxs-lookup"><span data-stu-id="4d063-123">Sync has a dependency on the protection service offered by Azure Information Protection (AIP) to protect sync data.</span></span> <span data-ttu-id="4d063-124">Esse serviço está atualmente disponível para as assinaturas anteriores.</span><span class="sxs-lookup"><span data-stu-id="4d063-124">This service is currently available to the preceding subscriptions.</span></span> <span data-ttu-id="4d063-125">Para ver a lista completa de SKUs com AIP, consulte [Preços da Proteção de Informações](https://azure.microsoft.com/pricing/details/information-protection/).</span><span class="sxs-lookup"><span data-stu-id="4d063-125">To see the full list of SKUs with AIP, see [Information Protection Pricing](https://azure.microsoft.com/pricing/details/information-protection/).</span></span>

## <span data-ttu-id="4d063-126">Opções de configuração para a sincronização do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="4d063-126">Configuration options for Microsoft Edge sync</span></span>

<span data-ttu-id="4d063-127">As seguintes opções de configuração estão disponíveis para habilitar a sincronização de Microsoft Edge:</span><span class="sxs-lookup"><span data-stu-id="4d063-127">The following configuration options are available for enabling Microsoft Edge sync:</span></span>

- <span data-ttu-id="4d063-128">Proteção de Informações do Azure (AIP)</span><span class="sxs-lookup"><span data-stu-id="4d063-128">Azure Information Protection (AIP)</span></span>
- <span data-ttu-id="4d063-129">Enterprise State Roaming (ESR) ou Roaming de Nível Empresarial do AAD</span><span class="sxs-lookup"><span data-stu-id="4d063-129">Azure AD Enterprise State Roaming (ESR)</span></span>

<span data-ttu-id="4d063-130">Se o AIP e o ESR estiverem desabilitados, os usuários verão uma mensagem de erro indicando que a sincronização não está disponível para a conta.</span><span class="sxs-lookup"><span data-stu-id="4d063-130">If both AIP and ESR are disabled, users will see an error message indicating that sync is not available for their account.</span></span>

### <span data-ttu-id="4d063-131">Proteção de Informações do Azure (AIP)</span><span class="sxs-lookup"><span data-stu-id="4d063-131">Azure Information Protection (AIP)</span></span>

<span data-ttu-id="4d063-132">Se o serviço Proteção de Informações do Azure (AIP) estiver habilitado para um locatário, todos os usuários poderão sincronizar os dados do Microsoft Edge, independentemente do licenciamento.</span><span class="sxs-lookup"><span data-stu-id="4d063-132">If the Azure Information Protection (AIP) service is enabled for a tenant, all users can sync Microsoft Edge data, regardless of licensing.</span></span> <span data-ttu-id="4d063-133">Instruções sobre como habilitar o AIP estão disponíveis [aqui](https://docs.microsoft.com/azure/information-protection/activate-office365).</span><span class="sxs-lookup"><span data-stu-id="4d063-133">Instructions on how to enable AIP can be found [here](https://docs.microsoft.com/azure/information-protection/activate-office365).</span></span>

<span data-ttu-id="4d063-134">Para restringir a sincronização a certos conjuntos de usuários, você pode habilitar a [Política de controle de integração AADRM](https://docs.microsoft.com/powershell/module/aadrm/set-aadrmonboardingcontrolpolicy?view=azureipps) desses usuários.</span><span class="sxs-lookup"><span data-stu-id="4d063-134">To restrict sync to certain set of users, you can enable the [AADRM onboarding control policy](https://docs.microsoft.com/powershell/module/aadrm/set-aadrmonboardingcontrolpolicy?view=azureipps) for those users.</span></span> <span data-ttu-id="4d063-135">Se a sincronização ainda não estiver disponível depois de garantir que todos os usuários necessários estejam integrados, certifique-se de que o IPCv3Service está habilitado através do [Get-AIPServiceIPCv3](https://docs.microsoft.com/powershell/module/aipservice/Get-AipServiceIPCv3?view=azureipps) PowerShell cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d063-135">If sync is still not available after ensuring that all necessary users are onboarded, ensure that the IPCv3Service is enabled using the [Get-AIPServiceIPCv3](https://docs.microsoft.com/powershell/module/aipservice/Get-AipServiceIPCv3?view=azureipps) PowerShell cmdlet.</span></span>

> [!CAUTION]
> <span data-ttu-id="4d063-136">A ativação da Proteção de informações do Azure também restringirá o acesso de outros aplicativos que usam AIP, como o Microsoft Word ou o Microsoft Outlook.</span><span class="sxs-lookup"><span data-stu-id="4d063-136">Activating Azure Information Protection will also restrict access for other applications using AIP, such as Microsoft Word or Microsoft Outlook.</span></span>

### <span data-ttu-id="4d063-137">Enterprise State Roaming (ESR) ou Roaming de Nível Empresarial do AAD</span><span class="sxs-lookup"><span data-stu-id="4d063-137">Azure AD Enterprise State Roaming (ESR)</span></span>

<span data-ttu-id="4d063-138">Se o recurso [Enterprise State Roaming](https://docs.microsoft.com/azure/active-directory/devices/enterprise-state-roaming-overview) (ESR) do Azure Active Directory estiver habilitado para qualquer usuário ou locatário, eles poderão usar o recurso de sincronização do Microsoft Edge, independentemente da configuração de política de controle de integração.</span><span class="sxs-lookup"><span data-stu-id="4d063-138">If the Azure Active Directory [Enterprise State Roaming](https://docs.microsoft.com/azure/active-directory/devices/enterprise-state-roaming-overview) (ESR) feature is enabled for any user or tenant, they can use the Microsoft Edge sync feature regardless of the onboarding control policy setting.</span></span>

## <span data-ttu-id="4d063-139">Microsoft Edge e Enterprise State Roaming</span><span class="sxs-lookup"><span data-stu-id="4d063-139">Microsoft Edge and Enterprise State Roaming</span></span>

<span data-ttu-id="4d063-140">O novo Microsoft Edge é um aplicativo compatível com diferentes plataformas e possui um escopo expandido para sincronizar os dados do usuário em todos os dispositivos deles e não faz mais parte do Enterprise State Roaming do AAD.</span><span class="sxs-lookup"><span data-stu-id="4d063-140">The new Microsoft Edge is a cross-platform application with an expanded scope for syncing user data across all their devices and is no longer a part of Azure AD Enterprise State Roaming.</span></span> <span data-ttu-id="4d063-141">No entanto, o novo Microsoft Edge cumprirá as promessas de proteção de dados do ESR, como a capacidade de trazer sua própria chave.</span><span class="sxs-lookup"><span data-stu-id="4d063-141">However, the new Microsoft Edge will fulfill the data protection promises of ESR, such as the ability to bring your own key.</span></span> <span data-ttu-id="4d063-142">Para obter mais informações, consulte [Microsoft Edge e Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).</span><span class="sxs-lookup"><span data-stu-id="4d063-142">For more information, see [Microsoft Edge and Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).</span></span>

## <span data-ttu-id="4d063-143">Políticas de grupo de sincronização</span><span class="sxs-lookup"><span data-stu-id="4d063-143">Sync group policies</span></span>

<span data-ttu-id="4d063-144">As seguintes políticas de grupo afetam a sincronização do Microsoft Edge:</span><span class="sxs-lookup"><span data-stu-id="4d063-144">The following group policies impact Microsoft Edge sync:</span></span>

- <span data-ttu-id="4d063-145">[SyncDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#syncdisabled): desabilita completamente a sincronização.</span><span class="sxs-lookup"><span data-stu-id="4d063-145">[SyncDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#syncdisabled): Disables sync completely.</span></span>
- <span data-ttu-id="4d063-146">[SavingBrowserHistoryDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#savingbrowserhistorydisabled): Desabilita o salvamento do histórico de navegação e a sincronização. Também desabilita a sincronização de guias abertas.</span><span class="sxs-lookup"><span data-stu-id="4d063-146">[SavingBrowserHistoryDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#savingbrowserhistorydisabled): Disables saving browsing history and sync. This policy also disables open-tabs sync.</span></span>
- <span data-ttu-id="4d063-147">[SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled): configura a lista de tipos excluídos da sincronização.</span><span class="sxs-lookup"><span data-stu-id="4d063-147">[SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled): Configure the list of types that are excluded from synchronization.</span></span>

## <span data-ttu-id="4d063-148">Perguntas frequentes</span><span class="sxs-lookup"><span data-stu-id="4d063-148">Frequently Asked Questions</span></span>

### <span data-ttu-id="4d063-149">SEGURANÇA e CONFORMIDADE COM O SERVIDOR/DADOS</span><span class="sxs-lookup"><span data-stu-id="4d063-149">SECURITY and SERVER/DATA COMPLIANCE</span></span>

#### <span data-ttu-id="4d063-150">Os dados sincronizados estão encriptados?</span><span class="sxs-lookup"><span data-stu-id="4d063-150">Is the synced data encrypted?</span></span> 

<span data-ttu-id="4d063-151">Os dados são criptografados no transporte através do TLS 1.2 ou superior e, adicionalmente, em repouso no serviço da Microsoft através do AES256.</span><span class="sxs-lookup"><span data-stu-id="4d063-151">The data is encrypted in transport using TLS 1.2 or greater, and additionally at rest in Microsoft's service using AES256.</span></span>

#### <span data-ttu-id="4d063-152">Onde os dados sincronizados são armazenados para o Microsoft Edge?</span><span class="sxs-lookup"><span data-stu-id="4d063-152">Where is Microsoft Edge sync data stored?</span></span>

<span data-ttu-id="4d063-153">Os dados sincronizados para contas do Azure AD são armazenados em servidores seguros de acordo com a ID do locatário.</span><span class="sxs-lookup"><span data-stu-id="4d063-153">Synced data for Azure AD accounts is stored in secure servers according to the tenant ID.</span></span> <span data-ttu-id="4d063-154">Por exemplo, os dados de um locatário registrado nos Estados Unidos são armazenados em servidores localizados geograficamente nessa região e aproveitam a mesma solução de armazenamento usada pelos aplicativos do Office.</span><span class="sxs-lookup"><span data-stu-id="4d063-154">For example, the data for a tenant that is registered in the United States is stored in servers geo-located for that region and uses the same storage solution as Office applications.</span></span>

#### <span data-ttu-id="4d063-155">Os dados deixam a nuvem da Microsoft, além de sincronizar com o Microsoft Edge?</span><span class="sxs-lookup"><span data-stu-id="4d063-155">Does the data ever leave Microsoft's cloud, aside from syncing to Microsoft Edge?</span></span>

<span data-ttu-id="4d063-156">Não.</span><span class="sxs-lookup"><span data-stu-id="4d063-156">No.</span></span>

#### <span data-ttu-id="4d063-157">Os administradores de locatários podem ter suas próprias chaves?</span><span class="sxs-lookup"><span data-stu-id="4d063-157">Can tenant admins bring their own key?</span></span>

<span data-ttu-id="4d063-158">Sim, por meio da [Proteção de Informações do Azure](https://azure.microsoft.com/services/information-protection/).</span><span class="sxs-lookup"><span data-stu-id="4d063-158">Yes, through [Azure Information Protection](https://azure.microsoft.com/services/information-protection/).</span></span>

#### <span data-ttu-id="4d063-159">Em que termos de serviço a sincronização empresarial se encaixa?</span><span class="sxs-lookup"><span data-stu-id="4d063-159">What terms of service does enterprise sync fall under?</span></span>

<span data-ttu-id="4d063-160">Os termos de serviço são os mesmos termos da sua assinatura do Azure AD.</span><span class="sxs-lookup"><span data-stu-id="4d063-160">The terms of service are the same terms as your Azure AD subscription.</span></span> <span data-ttu-id="4d063-161">Todos os termos de serviço do Azure AD estão, em última análise, no [Termos do serviço online](https://www.microsoft.com/licensing/product-licensing/products) da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="4d063-161">All the Azure AD terms of service ultimately fall under Microsoft's [Online Service Terms](https://www.microsoft.com/licensing/product-licensing/products).</span></span>

#### <span data-ttu-id="4d063-162">O Microsoft Edge tem suporte para conformidade do Government Community Cloud (GCC) High?</span><span class="sxs-lookup"><span data-stu-id="4d063-162">Does Microsoft Edge support Government Community Cloud (GCC) High compliance?</span></span>

<span data-ttu-id="4d063-163">Não hoje.</span><span class="sxs-lookup"><span data-stu-id="4d063-163">Not today.</span></span> <span data-ttu-id="4d063-164">GCC High é nível D, enquanto que o Microsoft Edge tem suporte para o nível C.</span><span class="sxs-lookup"><span data-stu-id="4d063-164">GCC High is Tier D, while Microsoft Edge supports up to Tier C.</span></span>

### <span data-ttu-id="4d063-165">APLICAÇÃO DE SINCRONIZAÇÃO</span><span class="sxs-lookup"><span data-stu-id="4d063-165">APPLYING SYNC</span></span>

#### <span data-ttu-id="4d063-166">O que acontece com os clientes corporativos e educacionais que decidirem ficar com o Microsoft Edge Legacy?</span><span class="sxs-lookup"><span data-stu-id="4d063-166">What happens with enterprise and educational customers who decide to stay with Microsoft Edge Legacy?</span></span>

<span data-ttu-id="4d063-167">A versão atual do navegador Microsoft Edge continuará participando da oferta de ESR.</span><span class="sxs-lookup"><span data-stu-id="4d063-167">The current version of Microsoft Edge browser will continue to participate in the ESR offering.</span></span>

#### <span data-ttu-id="4d063-168">Por que eu preciso de uma assinatura premium do Azure AD para sincronizar?</span><span class="sxs-lookup"><span data-stu-id="4d063-168">Why do I need a premium Azure AD subscription to sync?</span></span>

<span data-ttu-id="4d063-169">A sincronização empresarial depende da Proteção de Informações do Azure, que não está disponível em todos os níveis do Azure AD.</span><span class="sxs-lookup"><span data-stu-id="4d063-169">Enterprise sync depends on Azure Information Protection, which is not available in all Azure AD tiers.</span></span>

#### <span data-ttu-id="4d063-170">A sincronização do Microsoft Edge é baseada no Enterprise State Roaming?</span><span class="sxs-lookup"><span data-stu-id="4d063-170">Is Microsoft Edge sync based on Enterprise State Roaming?</span></span>

<span data-ttu-id="4d063-171">Não.</span><span class="sxs-lookup"><span data-stu-id="4d063-171">No.</span></span> <span data-ttu-id="4d063-172">O ESR pode ser usado para habilitar a sincronização, mas a sincronização do Microsoft Edge não faz parte do ESR.</span><span class="sxs-lookup"><span data-stu-id="4d063-172">ESR can be used to enable sync, but Microsoft Edge sync is not a part of ESR.</span></span> <span data-ttu-id="4d063-173">Para obter mais informações, consulte [Sincronização do Microsoft Edge](microsoft-edge-enterprise-sync.md) e [Microsoft Edge e Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).</span><span class="sxs-lookup"><span data-stu-id="4d063-173">For more information, see [Microsoft Edge Sync](microsoft-edge-enterprise-sync.md) and [Microsoft Edge and Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).</span></span>

#### <span data-ttu-id="4d063-174">O Microsoft Edge oferecerá suporte para sincronização entre o Microsoft Edge e o IE?</span><span class="sxs-lookup"><span data-stu-id="4d063-174">Will Microsoft Edge ever support syncing between Microsoft Edge and IE?</span></span>

<span data-ttu-id="4d063-175">Não há planos para dar suporte a essa sincronização.</span><span class="sxs-lookup"><span data-stu-id="4d063-175">There are no plans to support this syncing.</span></span> <span data-ttu-id="4d063-176">Se você ainda precisar do IE em seu ambiente para oferecer suporte a aplicativos herdados, considere o nosso [novo modo do IE](https://docs.microsoft.com/deployedge/edge-ie-mode).</span><span class="sxs-lookup"><span data-stu-id="4d063-176">If you still need IE in your environment to support legacy apps, consider our [new IE mode](https://docs.microsoft.com/deployedge/edge-ie-mode).</span></span>

#### <span data-ttu-id="4d063-177">O novo navegador Microsoft Edge será sincronizado com o Microsoft Edge Legacy?</span><span class="sxs-lookup"><span data-stu-id="4d063-177">Will the new Microsoft Edge browser sync with Microsoft Edge Legacy?</span></span>

<span data-ttu-id="4d063-178">Não.</span><span class="sxs-lookup"><span data-stu-id="4d063-178">No, it won't.</span></span> <span data-ttu-id="4d063-179">Acreditamos que conectar esses dois ecossistemas comprometerá a confiabilidade da sincronização no novo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="4d063-179">We believe connecting these two ecosystems will lead to compromises in the reliability of sync in the new Microsoft Edge.</span></span> <span data-ttu-id="4d063-180">Vamos garantir que os dados existentes sejam migrados para o novo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="4d063-180">We will ensure that existing data is migrated to the new Microsoft Edge.</span></span> <span data-ttu-id="4d063-181">Os usuários também poderão importar dados do navegador de sua preferência.</span><span class="sxs-lookup"><span data-stu-id="4d063-181">Users will also be able to import data from browser of their choice.</span></span> <span data-ttu-id="4d063-182">Isso também significa que o novo navegador Microsoft Edge não poderá ser sincronizado com o IE.</span><span class="sxs-lookup"><span data-stu-id="4d063-182">This also means that new Microsoft Edge browser won't have a way to sync with IE.</span></span>

### <span data-ttu-id="4d063-183">GERENCIANDO A SINCRONIZAÇÃO</span><span class="sxs-lookup"><span data-stu-id="4d063-183">MANAGING SYNC</span></span>

#### <span data-ttu-id="4d063-184">É possível impedir que os meus usuários sincronizem com um locatário pessoal?</span><span class="sxs-lookup"><span data-stu-id="4d063-184">Is it possible to stop my users from syncing with a personal tenant?</span></span>

<span data-ttu-id="4d063-185">Não diretamente, mas você pode determinar quais perfis podem entrar no Microsoft Edge usando a política [RestrictSigninToPattern](https://docs.microsoft.com/deployedge/microsoft-edge-policies#restrictsignintopattern).</span><span class="sxs-lookup"><span data-stu-id="4d063-185">Not directly, but you can determine which profiles can sign on to Microsoft Edge using the [RestrictSigninToPattern](https://docs.microsoft.com/deployedge/microsoft-edge-policies#restrictsignintopattern) policy.</span></span>

## <span data-ttu-id="4d063-186">Consulte também</span><span class="sxs-lookup"><span data-stu-id="4d063-186">See also</span></span>

- [<span data-ttu-id="4d063-187">Página de aterrissagem do Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="4d063-187">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="4d063-188">Microsoft Edge e Enterprise State Roaming</span><span class="sxs-lookup"><span data-stu-id="4d063-188">Microsoft Edge and Enterprise State Roaming</span></span>](microsoft-edge-enterprise-state-roaming.md)
