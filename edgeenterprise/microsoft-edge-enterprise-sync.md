---
title: Sincronização do Microsoft Edge Enterprise
ms.author: scottbo
author: dan-wesley
manager: silvanam
ms.date: 09/30/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Sincronização do Microsoft Edge Enterprise
ms.openlocfilehash: d5868fb496c036d750925bb5ae6dfa3de0293fd2
ms.sourcegitcommit: 8a4479a1b034c3c13ea03ee3a2374a1af332cb38
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/30/2020
ms.locfileid: "11091943"
---
# <span data-ttu-id="3ad02-103">Sincronização do Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="3ad02-103">Microsoft Edge Enterprise Sync</span></span>

<span data-ttu-id="3ad02-104">Este artigo explica como usar o Microsoft Edge para sincronizar seus favoritos, senhas e outros dados do navegador com todos os seus dispositivos conectados.</span><span class="sxs-lookup"><span data-stu-id="3ad02-104">This article explains how to use Microsoft Edge to sync your favorites, passwords, and other browser data across all your signed-in devices.</span></span>

> [!NOTE]
> <span data-ttu-id="3ad02-105">Este artigo se aplica ao Microsoft Edge versão 77 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="3ad02-105">This article applies to Microsoft Edge version 77 or later.</span></span>

## <span data-ttu-id="3ad02-106">Visão geral</span><span class="sxs-lookup"><span data-stu-id="3ad02-106">Overview</span></span>

<span data-ttu-id="3ad02-107">A sincronização do Microsoft Edge permite que os usuários acessem seus dados de navegação em todos os dispositivos conectados.</span><span class="sxs-lookup"><span data-stu-id="3ad02-107">Microsoft Edge sync enables users to access their browsing data across all their signed-in devices.</span></span> <span data-ttu-id="3ad02-108">Os dados com suporte na sincronização incluem:</span><span class="sxs-lookup"><span data-stu-id="3ad02-108">The data supported by sync includes:</span></span>

- <span data-ttu-id="3ad02-109">Favoritos</span><span class="sxs-lookup"><span data-stu-id="3ad02-109">Favorites</span></span>
- <span data-ttu-id="3ad02-110">Senhas</span><span class="sxs-lookup"><span data-stu-id="3ad02-110">Passwords</span></span>
- <span data-ttu-id="3ad02-111">Endereços e etc. (preenchimento de formulário)</span><span class="sxs-lookup"><span data-stu-id="3ad02-111">Addresses and more (form-fill)</span></span>
- <span data-ttu-id="3ad02-112">Coleções</span><span class="sxs-lookup"><span data-stu-id="3ad02-112">Collections</span></span>
- <span data-ttu-id="3ad02-113">Configurações</span><span class="sxs-lookup"><span data-stu-id="3ad02-113">Settings</span></span>

<span data-ttu-id="3ad02-114">A funcionalidade de sincronização é habilitada por meio do consentimento do usuário, e os usuários podem ativar ou desativar a sincronização para cada um dos tipos de dados listados acima.</span><span class="sxs-lookup"><span data-stu-id="3ad02-114">Sync functionality is enabled via user consent and users can turn sync on or off for each of the data types listed above.</span></span>

> [!NOTE]
> <span data-ttu-id="3ad02-115">Outros dados de configuração e conectividade do dispositivo (como nome, marca e modelo do dispositivo) são carregados para dar suporte à funcionalidade de sincronização.</span><span class="sxs-lookup"><span data-stu-id="3ad02-115">Additional device connectivity and configuration data (such as device name, make and model) is uploaded to support sync functionality.</span></span>

## <span data-ttu-id="3ad02-116">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="3ad02-116">Prerequisites</span></span>

<span data-ttu-id="3ad02-117">A sincronização do Microsoft Edge para as contas do Azure Active Directory (Azure AD) está disponível qualquer uma das seguintes assinaturas:</span><span class="sxs-lookup"><span data-stu-id="3ad02-117">Microsoft Edge sync for Azure Active Directory (Azure AD) accounts is available for any of the following subscriptions:</span></span>

- <span data-ttu-id="3ad02-118">Azure AD Premium( P1 e P2)</span><span class="sxs-lookup"><span data-stu-id="3ad02-118">Azure AD Premium (P1 and P2)</span></span>
- <span data-ttu-id="3ad02-119">M365 Business Premium</span><span class="sxs-lookup"><span data-stu-id="3ad02-119">M365 Business Premium</span></span>
- <span data-ttu-id="3ad02-120">Office 365 E3 e superior</span><span class="sxs-lookup"><span data-stu-id="3ad02-120">Office 365 E3 and above</span></span>
- <span data-ttu-id="3ad02-121">Proteção de Informações do Azure (AIP) (P1 e P2)</span><span class="sxs-lookup"><span data-stu-id="3ad02-121">Azure Information Protection (AIP) (P1& P2)</span></span>
- <span data-ttu-id="3ad02-122">Todas as assinaturas EDU (Aplicativos da Microsoft para Estudantes ou Docentes, Exchange Online para Estudantes ou Docentes, O365 A1 ou superior, M365 A1 ou superior, Proteção de Informações do Azure P1 ou P2 para Estudantes ou Docentes)</span><span class="sxs-lookup"><span data-stu-id="3ad02-122">All EDU subscriptions (Microsoft Apps for Students or Faculty, Exchange Online for Students or Faculty, O365 A1 or above, M365 A1 or above, or Azure Information Protection P1 or P2 for Students or Faculty)</span></span>

## <span data-ttu-id="3ad02-123">Configurar a sincronização do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="3ad02-123">Configuring Microsoft Edge sync</span></span>

<span data-ttu-id="3ad02-124">As opções de configuração para a sincronização do Microsoft Edge estão disponíveis por meio do serviço de Proteção de Informações do Azure (AIP).</span><span class="sxs-lookup"><span data-stu-id="3ad02-124">Configuration options for Microsoft Edge sync are available through the Azure Information Protection (AIP) service.</span></span> <span data-ttu-id="3ad02-125">Quando o (AIP) estiver habilitado para um locatário, todos os usuários poderão sincronizar os dados do Microsoft Edge, independentemente do licenciamento.</span><span class="sxs-lookup"><span data-stu-id="3ad02-125">When AIP is enabled for a tenant, all users can sync Microsoft Edge data, regardless of licensing.</span></span> <span data-ttu-id="3ad02-126">Instruções sobre como habilitar o AIP estão disponíveis [aqui](https://docs.microsoft.com/azure/information-protection/activate-office365).</span><span class="sxs-lookup"><span data-stu-id="3ad02-126">Instructions on how to enable AIP can be found [here](https://docs.microsoft.com/azure/information-protection/activate-office365).</span></span>

<span data-ttu-id="3ad02-127">Para restringir a sincronização a certos conjuntos de usuários, você pode habilitar a [Política de controle de integração do AIP](https://docs.microsoft.com/powershell/module/aipservice/set-aipserviceonboardingcontrolpolicy?view=azureipps)  para esses usuários.</span><span class="sxs-lookup"><span data-stu-id="3ad02-127">To restrict sync to certain set of users, you can enable the [AIP onboarding control policy](https://docs.microsoft.com/powershell/module/aipservice/set-aipserviceonboardingcontrolpolicy?view=azureipps) for those users.</span></span> <span data-ttu-id="3ad02-128">Se a sincronização ainda não estiver disponível depois de garantir que todos os usuários necessários estejam integrados, certifique-se de que o IPCv3Service está habilitado usando o cmdlet [Get-AIPServiceIPCv3](https://docs.microsoft.com/powershell/module/aipservice/get-aipserviceipcv3?view=azureipps)  PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3ad02-128">If sync is still not available after ensuring that all necessary users are onboarded, ensure that the IPCv3Service is enabled using the [Get-AIPServiceIPCv3](https://docs.microsoft.com/powershell/module/aipservice/get-aipserviceipcv3?view=azureipps)  PowerShell cmdlet.</span></span>

> [!CAUTION]
> <span data-ttu-id="3ad02-129">Ativar a Proteção de Informações do Azure também permitirá que outros aplicativos, como o Microsoft Word ou o Microsoft Outlook, protejam o conteúdo com o AIP.</span><span class="sxs-lookup"><span data-stu-id="3ad02-129">Activating Azure Information Protection will also allow other applications, such as Microsoft Word or Microsoft Outlook, to protect content with AIP.</span></span> <span data-ttu-id="3ad02-130">Além disso, qualquer política de controle de integração usada para restringir a sincronização do Microsoft Edge também restringirá outros aplicativos de proteger conteúdo usando o AIP.</span><span class="sxs-lookup"><span data-stu-id="3ad02-130">In addition, any onboarding control policy used to restrict Edge sync will also restrict other applications from protecting content using AIP.</span></span>

## <span data-ttu-id="3ad02-131">Microsoft Edge e Enterprise State Roaming</span><span class="sxs-lookup"><span data-stu-id="3ad02-131">Microsoft Edge and Enterprise State Roaming</span></span>

<span data-ttu-id="3ad02-132">O novo Microsoft Edge é um aplicativo compatível com diferentes plataformas e possui um escopo expandido para sincronizar os dados do usuário em todos os dispositivos deles e não faz mais parte do Enterprise State Roaming do AAD.</span><span class="sxs-lookup"><span data-stu-id="3ad02-132">The new Microsoft Edge is a cross-platform application with an expanded scope for syncing user data across all their devices and is no longer a part of Azure AD Enterprise State Roaming.</span></span> <span data-ttu-id="3ad02-133">No entanto, o novo Microsoft Edge cumprirá as promessas de proteção de dados do ESR, como a capacidade de trazer sua própria chave.</span><span class="sxs-lookup"><span data-stu-id="3ad02-133">However, the new Microsoft Edge will fulfill the data protection promises of ESR, such as the ability to bring your own key.</span></span> <span data-ttu-id="3ad02-134">Para obter mais informações, consulte [Microsoft Edge e Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).</span><span class="sxs-lookup"><span data-stu-id="3ad02-134">For more information, see [Microsoft Edge and Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).</span></span>

## <span data-ttu-id="3ad02-135">Políticas de grupo de sincronização</span><span class="sxs-lookup"><span data-stu-id="3ad02-135">Sync group policies</span></span>

<span data-ttu-id="3ad02-136">As seguintes políticas de grupo afetam a sincronização do Microsoft Edge:</span><span class="sxs-lookup"><span data-stu-id="3ad02-136">The following group policies impact Microsoft Edge sync:</span></span>

- <span data-ttu-id="3ad02-137">[SyncDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#syncdisabled): desabilita completamente a sincronização.</span><span class="sxs-lookup"><span data-stu-id="3ad02-137">[SyncDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#syncdisabled): Disables sync completely.</span></span>
- <span data-ttu-id="3ad02-138">[SavingBrowserHistoryDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#savingbrowserhistorydisabled): Desabilita o salvamento do histórico de navegação e a sincronização. Também desabilita a sincronização de guias abertas.</span><span class="sxs-lookup"><span data-stu-id="3ad02-138">[SavingBrowserHistoryDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#savingbrowserhistorydisabled): Disables saving browsing history and sync. This policy also disables open-tabs sync.</span></span>
- <span data-ttu-id="3ad02-139">[SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled): configura a lista de tipos excluídos da sincronização.</span><span class="sxs-lookup"><span data-stu-id="3ad02-139">[SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled): Configure the list of types that are excluded from synchronization.</span></span>
- <span data-ttu-id="3ad02-140">[RoamingProfileSupportEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#roamingprofilesupportenabled): permite que os perfis Active Directory (AD) usem o armazenamento local.</span><span class="sxs-lookup"><span data-stu-id="3ad02-140">[RoamingProfileSupportEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#roamingprofilesupportenabled): Allow Active Directory (AD) profiles to use on-premises storage.</span></span> <span data-ttu-id="3ad02-141">Para obter mais informações, consulte [Sincronização local para usuários do Active Directory (AD)](https://docs.microsoft.com/DeployEdge/microsoft-edge-on-premises-sync).</span><span class="sxs-lookup"><span data-stu-id="3ad02-141">For more information, see [On-premises sync for Active Directory (AD) users](https://docs.microsoft.com/DeployEdge/microsoft-edge-on-premises-sync).</span></span>
- <span data-ttu-id="3ad02-142">[ForceSync]( https://docs.microsoft.com/deployedge/microsoft-edge-policies#forcesync): ativar a sincronização por padrão e não exigir consentimento do usuário para sincronizar.</span><span class="sxs-lookup"><span data-stu-id="3ad02-142">[ForceSync]( https://docs.microsoft.com/deployedge/microsoft-edge-policies#forcesync): Turn sync on by default and do not require user consent to sync.</span></span>  

## <span data-ttu-id="3ad02-143">Perguntas frequentes</span><span class="sxs-lookup"><span data-stu-id="3ad02-143">Frequently Asked Questions</span></span>

### <span data-ttu-id="3ad02-144">SEGURANÇA e CONFORMIDADE COM O SERVIDOR/DADOS</span><span class="sxs-lookup"><span data-stu-id="3ad02-144">SECURITY and SERVER/DATA COMPLIANCE</span></span>

#### <span data-ttu-id="3ad02-145">Os dados sincronizados estão encriptados?</span><span class="sxs-lookup"><span data-stu-id="3ad02-145">Is the synced data encrypted?</span></span> 

<span data-ttu-id="3ad02-146">Os dados são criptografados no transporte usando TLS 1.2 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="3ad02-146">The data is encrypted in transport using TLS 1.2 or greater.</span></span> <span data-ttu-id="3ad02-147">A maioria dos tipos de dados também é criptografada em REST no serviço da Microsoft usando AES256.</span><span class="sxs-lookup"><span data-stu-id="3ad02-147">Most data types are additionally encrypted at rest in Microsoft's service using AES256.</span></span> 

#### <span data-ttu-id="3ad02-148">Onde os dados sincronizados são armazenados para o Microsoft Edge?</span><span class="sxs-lookup"><span data-stu-id="3ad02-148">Where is Microsoft Edge sync data stored?</span></span>

<span data-ttu-id="3ad02-149">Os dados sincronizados para contas do Azure AD são armazenados em servidores seguros de acordo com a ID do locatário.</span><span class="sxs-lookup"><span data-stu-id="3ad02-149">Synced data for Azure AD accounts is stored in secure servers according to the tenant ID.</span></span> <span data-ttu-id="3ad02-150">Por exemplo, os dados de um locatário registrado nos Estados Unidos são armazenados em servidores localizados geograficamente nessa região e aproveitam a mesma solução de armazenamento usada pelos aplicativos do Office.</span><span class="sxs-lookup"><span data-stu-id="3ad02-150">For example, the data for a tenant that is registered in the United States is stored in servers geo-located for that region and uses the same storage solution as Office applications.</span></span>

#### <span data-ttu-id="3ad02-151">Os dados deixam a nuvem da Microsoft, além de sincronizar com o Microsoft Edge?</span><span class="sxs-lookup"><span data-stu-id="3ad02-151">Does the data ever leave Microsoft's cloud, aside from syncing to Microsoft Edge?</span></span>

<span data-ttu-id="3ad02-152">Não.</span><span class="sxs-lookup"><span data-stu-id="3ad02-152">No.</span></span>

#### <span data-ttu-id="3ad02-153">Os administradores de locatários podem ter suas próprias chaves?</span><span class="sxs-lookup"><span data-stu-id="3ad02-153">Can tenant admins bring their own key?</span></span>

<span data-ttu-id="3ad02-154">Sim, por meio da [Proteção de Informações do Azure](https://azure.microsoft.com/services/information-protection/).</span><span class="sxs-lookup"><span data-stu-id="3ad02-154">Yes, through [Azure Information Protection](https://azure.microsoft.com/services/information-protection/).</span></span>

#### <span data-ttu-id="3ad02-155">Em que termos de serviço a sincronização empresarial se encaixa?</span><span class="sxs-lookup"><span data-stu-id="3ad02-155">What terms of service does enterprise sync fall under?</span></span>

<span data-ttu-id="3ad02-156">Os termos de serviço são os mesmos termos da sua assinatura do Azure AD.</span><span class="sxs-lookup"><span data-stu-id="3ad02-156">The terms of service are the same terms as your Azure AD subscription.</span></span> <span data-ttu-id="3ad02-157">Todos os termos de serviço do Azure AD estão, em última análise, no [Termos do serviço online](https://www.microsoft.com/licensing/product-licensing/products) da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="3ad02-157">All the Azure AD terms of service ultimately fall under Microsoft's [Online Service Terms](https://www.microsoft.com/licensing/product-licensing/products).</span></span>

#### <span data-ttu-id="3ad02-158">O Microsoft Edge tem suporte para conformidade do Government Community Cloud (GCC) High?</span><span class="sxs-lookup"><span data-stu-id="3ad02-158">Does Microsoft Edge support Government Community Cloud (GCC) High compliance?</span></span>

<span data-ttu-id="3ad02-159">Não hoje.</span><span class="sxs-lookup"><span data-stu-id="3ad02-159">Not today.</span></span> <span data-ttu-id="3ad02-160">GCC High é nível D, enquanto que o Microsoft Edge tem suporte para o nível C.</span><span class="sxs-lookup"><span data-stu-id="3ad02-160">GCC High is Tier D, while Microsoft Edge supports up to Tier C.</span></span>

### <span data-ttu-id="3ad02-161">APLICAÇÃO DE SINCRONIZAÇÃO</span><span class="sxs-lookup"><span data-stu-id="3ad02-161">APPLYING SYNC</span></span>

#### <span data-ttu-id="3ad02-162">O que acontece com os clientes corporativos e educacionais que decidirem ficar com o Microsoft Edge Legacy?</span><span class="sxs-lookup"><span data-stu-id="3ad02-162">What happens with enterprise and educational customers who decide to stay with Microsoft Edge Legacy?</span></span>

<span data-ttu-id="3ad02-163">A versão atual do navegador Microsoft Edge continuará participando da oferta de ESR.</span><span class="sxs-lookup"><span data-stu-id="3ad02-163">The current version of Microsoft Edge browser will continue to participate in the ESR offering.</span></span>

#### <span data-ttu-id="3ad02-164">Por que eu preciso de uma assinatura premium do Azure AD para sincronizar?</span><span class="sxs-lookup"><span data-stu-id="3ad02-164">Why do I need a premium Azure AD subscription to sync?</span></span>

<span data-ttu-id="3ad02-165">A sincronização empresarial depende da Proteção de Informações do Azure, que não está disponível em todos os níveis do Azure AD.</span><span class="sxs-lookup"><span data-stu-id="3ad02-165">Enterprise sync depends on Azure Information Protection, which is not available in all Azure AD tiers.</span></span>

#### <span data-ttu-id="3ad02-166">A sincronização do Microsoft Edge é baseada no Enterprise State Roaming?</span><span class="sxs-lookup"><span data-stu-id="3ad02-166">Is Microsoft Edge sync based on Enterprise State Roaming?</span></span>

<span data-ttu-id="3ad02-167">Não.</span><span class="sxs-lookup"><span data-stu-id="3ad02-167">No.</span></span> <span data-ttu-id="3ad02-168">O ESR pode ser usado para habilitar a sincronização, mas a sincronização do Microsoft Edge não faz parte do ESR.</span><span class="sxs-lookup"><span data-stu-id="3ad02-168">ESR can be used to enable sync, but Microsoft Edge sync is not a part of ESR.</span></span> <span data-ttu-id="3ad02-169">Para obter mais informações, consulte [Sincronização do Microsoft Edge](microsoft-edge-enterprise-sync.md) e [Microsoft Edge e Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).</span><span class="sxs-lookup"><span data-stu-id="3ad02-169">For more information, see [Microsoft Edge Sync](microsoft-edge-enterprise-sync.md) and [Microsoft Edge and Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).</span></span>

#### <span data-ttu-id="3ad02-170">O Microsoft Edge oferecerá suporte para sincronização entre o Microsoft Edge e o IE?</span><span class="sxs-lookup"><span data-stu-id="3ad02-170">Will Microsoft Edge ever support syncing between Microsoft Edge and IE?</span></span>

<span data-ttu-id="3ad02-171">Não há planos para dar suporte a essa sincronização.</span><span class="sxs-lookup"><span data-stu-id="3ad02-171">There are no plans to support this syncing.</span></span> <span data-ttu-id="3ad02-172">Se você ainda precisar do IE em seu ambiente para oferecer suporte a aplicativos herdados, considere o nosso [novo modo do IE](https://docs.microsoft.com/deployedge/edge-ie-mode).</span><span class="sxs-lookup"><span data-stu-id="3ad02-172">If you still need IE in your environment to support legacy apps, consider our [new IE mode](https://docs.microsoft.com/deployedge/edge-ie-mode).</span></span>

#### <span data-ttu-id="3ad02-173">O novo navegador Microsoft Edge será sincronizado com o Microsoft Edge Legacy?</span><span class="sxs-lookup"><span data-stu-id="3ad02-173">Will the new Microsoft Edge browser sync with Microsoft Edge Legacy?</span></span>

<span data-ttu-id="3ad02-174">Não.</span><span class="sxs-lookup"><span data-stu-id="3ad02-174">No, it won't.</span></span> <span data-ttu-id="3ad02-175">Acreditamos que conectar esses dois ecossistemas comprometerá a confiabilidade da sincronização no novo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="3ad02-175">We believe connecting these two ecosystems will lead to compromises in the reliability of sync in the new Microsoft Edge.</span></span> <span data-ttu-id="3ad02-176">Vamos garantir que os dados existentes sejam migrados para o novo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="3ad02-176">We will ensure that existing data is migrated to the new Microsoft Edge.</span></span> <span data-ttu-id="3ad02-177">Os usuários também poderão importar dados do navegador de sua preferência.</span><span class="sxs-lookup"><span data-stu-id="3ad02-177">Users will also be able to import data from browser of their choice.</span></span> <span data-ttu-id="3ad02-178">Isso também significa que o novo navegador Microsoft Edge não poderá ser sincronizado com o IE.</span><span class="sxs-lookup"><span data-stu-id="3ad02-178">This also means that new Microsoft Edge browser won't have a way to sync with IE.</span></span>

### <span data-ttu-id="3ad02-179">GERENCIANDO A SINCRONIZAÇÃO</span><span class="sxs-lookup"><span data-stu-id="3ad02-179">MANAGING SYNC</span></span>

#### <span data-ttu-id="3ad02-180">É possível impedir que os meus usuários sincronizem com um locatário pessoal?</span><span class="sxs-lookup"><span data-stu-id="3ad02-180">Is it possible to stop my users from syncing with a personal tenant?</span></span>

<span data-ttu-id="3ad02-181">Não diretamente, mas você pode determinar quais perfis podem entrar no Microsoft Edge usando a política [RestrictSigninToPattern](https://docs.microsoft.com/deployedge/microsoft-edge-policies#restrictsignintopattern).</span><span class="sxs-lookup"><span data-stu-id="3ad02-181">Not directly, but you can determine which profiles can sign on to Microsoft Edge using the [RestrictSigninToPattern](https://docs.microsoft.com/deployedge/microsoft-edge-policies#restrictsignintopattern) policy.</span></span>

## <span data-ttu-id="3ad02-182">Consulte também</span><span class="sxs-lookup"><span data-stu-id="3ad02-182">See also</span></span>

- [<span data-ttu-id="3ad02-183">Página de aterrissagem do Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="3ad02-183">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="3ad02-184">Microsoft Edge e Enterprise State Roaming</span><span class="sxs-lookup"><span data-stu-id="3ad02-184">Microsoft Edge and Enterprise State Roaming</span></span>](microsoft-edge-enterprise-state-roaming.md)
