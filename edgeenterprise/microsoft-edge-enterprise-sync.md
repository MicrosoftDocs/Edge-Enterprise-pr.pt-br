---
title: Sincronização do Microsoft Edge Enterprise
ms.author: scottbo
author: dan-wesley
manager: silvanam
ms.date: 12/09/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Sincronização do Microsoft Edge Enterprise
ms.openlocfilehash: 791188b5d28c867d6409a4d5373ea6c1ec7e49c7
ms.sourcegitcommit: 482b2e440a62cbf974dc45ac817f9d9d187ba1b9
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "11205460"
---
# <span data-ttu-id="32897-103">Sincronização do Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="32897-103">Microsoft Edge Enterprise Sync</span></span>

<span data-ttu-id="32897-104">Este artigo explica como usar o Microsoft Edge para sincronizar seus favoritos, senhas e outros dados do navegador com todos os seus dispositivos conectados.</span><span class="sxs-lookup"><span data-stu-id="32897-104">This article explains how to use Microsoft Edge to sync your favorites, passwords, and other browser data across all your signed-in devices.</span></span>

> [!NOTE]
> <span data-ttu-id="32897-105">Este artigo se aplica ao Microsoft Edge versão 77 ou posterior, a menos que indicado de outra forma.</span><span class="sxs-lookup"><span data-stu-id="32897-105">This article applies to Microsoft Edge version 77 or later unless otherwise noted.</span></span>

## <span data-ttu-id="32897-106">Visão geral</span><span class="sxs-lookup"><span data-stu-id="32897-106">Overview</span></span>

<span data-ttu-id="32897-107">A sincronização do Microsoft Edge permite que os usuários acessem seus dados de navegação em todos os dispositivos conectados.</span><span class="sxs-lookup"><span data-stu-id="32897-107">Microsoft Edge sync enables users to access their browsing data across all their signed-in devices.</span></span> <span data-ttu-id="32897-108">Os dados com suporte na sincronização incluem:</span><span class="sxs-lookup"><span data-stu-id="32897-108">The data supported by sync includes:</span></span>

- <span data-ttu-id="32897-109">Favoritos</span><span class="sxs-lookup"><span data-stu-id="32897-109">Favorites</span></span>
- <span data-ttu-id="32897-110">Senhas</span><span class="sxs-lookup"><span data-stu-id="32897-110">Passwords</span></span>
- <span data-ttu-id="32897-111">Endereços e etc. (preenchimento de formulário)</span><span class="sxs-lookup"><span data-stu-id="32897-111">Addresses and more (form-fill)</span></span>
- <span data-ttu-id="32897-112">Coleções</span><span class="sxs-lookup"><span data-stu-id="32897-112">Collections</span></span>
- <span data-ttu-id="32897-113">Configurações</span><span class="sxs-lookup"><span data-stu-id="32897-113">Settings</span></span>
- <span data-ttu-id="32897-114">Extensão</span><span class="sxs-lookup"><span data-stu-id="32897-114">Extension</span></span>
- <span data-ttu-id="32897-115">Abrir guias (disponível no Microsoft Edge versão 88)</span><span class="sxs-lookup"><span data-stu-id="32897-115">Open tabs (available in Microsoft Edge version 88)</span></span>
- <span data-ttu-id="32897-116">Histórico (disponível no Microsoft Edge versão 88)</span><span class="sxs-lookup"><span data-stu-id="32897-116">History (available in Microsoft Edge version 88)</span></span>

<span data-ttu-id="32897-117">A funcionalidade de sincronização é habilitada através do consentimento do usuário, e os usuários podem ativar ou desativar a sincronização de cada um dos tipos de dados listados acima.</span><span class="sxs-lookup"><span data-stu-id="32897-117">Sync functionality is enabled via user consent and users can turn sync on or off for each of the data types listed above.</span></span>

> [!NOTE]
> <span data-ttu-id="32897-118">Outros dados de configuração e conectividade do dispositivo (como nome, marca e modelo do dispositivo) são carregados para dar suporte à funcionalidade de sincronização.</span><span class="sxs-lookup"><span data-stu-id="32897-118">Additional device connectivity and configuration data (such as device name, make and model) is uploaded to support sync functionality.</span></span>

## <span data-ttu-id="32897-119">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="32897-119">Prerequisites</span></span>

<span data-ttu-id="32897-120">A sincronização do Microsoft Edge das contas do Azure Active Directory (Azure AD) está disponível para qualquer uma das seguintes assinaturas:</span><span class="sxs-lookup"><span data-stu-id="32897-120">Microsoft Edge sync for Azure Active Directory (Azure AD) accounts is available for any of the following subscriptions:</span></span>

- <span data-ttu-id="32897-121">Azure AD Premium (P1 ou P2)</span><span class="sxs-lookup"><span data-stu-id="32897-121">Azure AD Premium (P1 or P2)</span></span>
- <span data-ttu-id="32897-122">M365 Business Premium</span><span class="sxs-lookup"><span data-stu-id="32897-122">M365 Business Premium</span></span>
- <span data-ttu-id="32897-123">Office 365 E1 e superior</span><span class="sxs-lookup"><span data-stu-id="32897-123">Office 365 E1 and above</span></span>
- <span data-ttu-id="32897-124">Proteção de informações do Azure (AIP) (P1 ou P2)</span><span class="sxs-lookup"><span data-stu-id="32897-124">Azure Information Protection (AIP) (P1 or P2)</span></span>
- <span data-ttu-id="32897-125">Todas as assinaturas EDU (Aplicativos da Microsoft para Estudantes ou Docentes, Exchange Online para Estudantes ou Docentes, O365 A1 ou superior, M365 A1 ou superior, Proteção de Informações do Azure P1 ou P2 para Estudantes ou Docentes)</span><span class="sxs-lookup"><span data-stu-id="32897-125">All EDU subscriptions (Microsoft Apps for Students or Faculty, Exchange Online for Students or Faculty, O365 A1 or above, M365 A1 or above, or Azure Information Protection P1 or P2 for Students or Faculty)</span></span>

## <span data-ttu-id="32897-126">Configurar a sincronização do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="32897-126">Configuring Microsoft Edge sync</span></span>

<span data-ttu-id="32897-127">As opções de configuração para a sincronização do Microsoft Edge estão disponíveis por meio do serviço de Proteção de Informações do Azure (AIP).</span><span class="sxs-lookup"><span data-stu-id="32897-127">Configuration options for Microsoft Edge sync are available through the Azure Information Protection (AIP) service.</span></span> <span data-ttu-id="32897-128">Quando o (AIP) estiver habilitado para um locatário, todos os usuários poderão sincronizar os dados do Microsoft Edge, independentemente do licenciamento.</span><span class="sxs-lookup"><span data-stu-id="32897-128">When AIP is enabled for a tenant, all users can sync Microsoft Edge data, regardless of licensing.</span></span> <span data-ttu-id="32897-129">Instruções sobre como habilitar o AIP estão disponíveis [aqui](https://docs.microsoft.com/azure/information-protection/activate-office365).</span><span class="sxs-lookup"><span data-stu-id="32897-129">Instructions on how to enable AIP can be found [here](https://docs.microsoft.com/azure/information-protection/activate-office365).</span></span>

<span data-ttu-id="32897-130">Para restringir a sincronização a certos conjuntos de usuários, você pode habilitar a [Política de controle de integração do AIP](https://docs.microsoft.com/powershell/module/aipservice/set-aipserviceonboardingcontrolpolicy?view=azureipps&preserve-view=true)  para esses usuários.</span><span class="sxs-lookup"><span data-stu-id="32897-130">To restrict sync to certain set of users, you can enable the [AIP onboarding control policy](https://docs.microsoft.com/powershell/module/aipservice/set-aipserviceonboardingcontrolpolicy?view=azureipps&preserve-view=true) for those users.</span></span> <span data-ttu-id="32897-131">Se a sincronização ainda não estiver disponível depois de garantir que todos os usuários necessários estejam integrados, certifique-se de que o IPCv3Service está habilitado usando o cmdlet [Get-AIPServiceIPCv3](https://docs.microsoft.com/powershell/module/aipservice/get-aipserviceipcv3?view=azureipps&preserve-view=true)  PowerShell.</span><span class="sxs-lookup"><span data-stu-id="32897-131">If sync is still not available after ensuring that all necessary users are onboarded, ensure that the IPCv3Service is enabled using the [Get-AIPServiceIPCv3](https://docs.microsoft.com/powershell/module/aipservice/get-aipserviceipcv3?view=azureipps&preserve-view=true)  PowerShell cmdlet.</span></span>

> [!CAUTION]
> <span data-ttu-id="32897-132">Ativar a Proteção de Informações do Azure também permitirá que outros aplicativos, como o Microsoft Word ou o Microsoft Outlook, protejam o conteúdo com o AIP.</span><span class="sxs-lookup"><span data-stu-id="32897-132">Activating Azure Information Protection will also allow other applications, such as Microsoft Word or Microsoft Outlook, to protect content with AIP.</span></span> <span data-ttu-id="32897-133">Além disso, qualquer política de controle de integração usada para restringir a sincronização do Microsoft Edge também restringirá outros aplicativos de proteger conteúdo usando o AIP.</span><span class="sxs-lookup"><span data-stu-id="32897-133">In addition, any onboarding control policy used to restrict Edge sync will also restrict other applications from protecting content using AIP.</span></span>

## <span data-ttu-id="32897-134">Microsoft Edge e Enterprise State Roaming</span><span class="sxs-lookup"><span data-stu-id="32897-134">Microsoft Edge and Enterprise State Roaming</span></span>

<span data-ttu-id="32897-135">O novo Microsoft Edge é um aplicativo compatível com diferentes plataformas e possui um escopo expandido para sincronizar os dados do usuário em todos os dispositivos deles e não faz mais parte do Enterprise State Roaming do AAD.</span><span class="sxs-lookup"><span data-stu-id="32897-135">The new Microsoft Edge is a cross-platform application with an expanded scope for syncing user data across all their devices and is no longer a part of Azure AD Enterprise State Roaming.</span></span> <span data-ttu-id="32897-136">No entanto, o novo Microsoft Edge cumprirá as promessas de proteção de dados do ESR, como a capacidade de trazer sua própria chave.</span><span class="sxs-lookup"><span data-stu-id="32897-136">However, the new Microsoft Edge will fulfill the data protection promises of ESR, such as the ability to bring your own key.</span></span> <span data-ttu-id="32897-137">Para obter mais informações, consulte [Microsoft Edge e Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).</span><span class="sxs-lookup"><span data-stu-id="32897-137">For more information, see [Microsoft Edge and Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).</span></span>

## <span data-ttu-id="32897-138">Políticas de grupo de sincronização</span><span class="sxs-lookup"><span data-stu-id="32897-138">Sync group policies</span></span>

<span data-ttu-id="32897-139">As seguintes políticas de grupo afetam a sincronização do Microsoft Edge:</span><span class="sxs-lookup"><span data-stu-id="32897-139">The following group policies impact Microsoft Edge sync:</span></span>

- <span data-ttu-id="32897-140">[SyncDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#syncdisabled): desabilita completamente a sincronização.</span><span class="sxs-lookup"><span data-stu-id="32897-140">[SyncDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#syncdisabled): Disables sync completely.</span></span>
- <span data-ttu-id="32897-141">[SavingBrowserHistoryDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#savingbrowserhistorydisabled): desabilita o salvamento do histórico de navegação e a sincronização. Também desabilita a sincronização das guias abertas.</span><span class="sxs-lookup"><span data-stu-id="32897-141">[SavingBrowserHistoryDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#savingbrowserhistorydisabled): Disables saving browsing history and sync. This policy also disables open-tabs sync.</span></span>
- <span data-ttu-id="32897-142">[AllowDeletingBrowserHistory](https://docs.microsoft.com/deployedge/microsoft-edge-policies#allowdeletingbrowserhistory): quando essa política é definida como Desabilitada, a sincronização do histórico também será desabilitada.</span><span class="sxs-lookup"><span data-stu-id="32897-142">[AllowDeletingBrowserHistory](https://docs.microsoft.com/deployedge/microsoft-edge-policies#allowdeletingbrowserhistory): When this policy is set to disabled, history sync will also be disabled.</span></span>
- <span data-ttu-id="32897-143">[SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled): configura a lista dos tipos excluídos da sincronização.</span><span class="sxs-lookup"><span data-stu-id="32897-143">[SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled): Configure the list of types that are excluded from synchronization.</span></span>
- <span data-ttu-id="32897-144">[RoamingProfileSupportEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#roamingprofilesupportenabled): permite que os perfis Active Directory (AD) usem o armazenamento local.</span><span class="sxs-lookup"><span data-stu-id="32897-144">[RoamingProfileSupportEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#roamingprofilesupportenabled): Allow Active Directory (AD) profiles to use on-premises storage.</span></span> <span data-ttu-id="32897-145">Para obter mais informações, consulte [Sincronização local para usuários do Active Directory (AD)](https://docs.microsoft.com/DeployEdge/microsoft-edge-on-premises-sync).</span><span class="sxs-lookup"><span data-stu-id="32897-145">For more information, see [On-premises sync for Active Directory (AD) users](https://docs.microsoft.com/DeployEdge/microsoft-edge-on-premises-sync).</span></span>
- <span data-ttu-id="32897-146">[ForceSync]( https://docs.microsoft.com/deployedge/microsoft-edge-policies#forcesync): ativar a sincronização por padrão e não exigir consentimento do usuário para sincronizar.</span><span class="sxs-lookup"><span data-stu-id="32897-146">[ForceSync]( https://docs.microsoft.com/deployedge/microsoft-edge-policies#forcesync): Turn sync on by default and do not require user consent to sync.</span></span>  

## <span data-ttu-id="32897-147">Perguntas frequentes</span><span class="sxs-lookup"><span data-stu-id="32897-147">Frequently Asked Questions</span></span>

### <span data-ttu-id="32897-148">SEGURANÇA e CONFORMIDADE COM O SERVIDOR/DADOS</span><span class="sxs-lookup"><span data-stu-id="32897-148">SECURITY and SERVER/DATA COMPLIANCE</span></span>

#### <span data-ttu-id="32897-149">Os dados sincronizados estão encriptados?</span><span class="sxs-lookup"><span data-stu-id="32897-149">Is the synced data encrypted?</span></span>

<span data-ttu-id="32897-150">Os dados são criptografados no transporte usando TLS 1.2 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="32897-150">The data is encrypted in transport using TLS 1.2 or greater.</span></span> <span data-ttu-id="32897-151">Todos os tipos de dados também são criptografados como descansar no serviço da Microsoft usando o AES128.</span><span class="sxs-lookup"><span data-stu-id="32897-151">All data types are additionally encrypted at rest in Microsoft's service using AES128.</span></span> <span data-ttu-id="32897-152">Todos os tipos de dados, exceto os usados na guia aberta e na sincronização do histórico, também são criptografados antes de sair do dispositivo do usuário com chaves gerenciadas pela [Proteção de informações do Azure](https://docs.microsoft.com/azure/information-protection/).</span><span class="sxs-lookup"><span data-stu-id="32897-152">All data types except those used for open tab and history sync are additionally encrypted before leaving the user’s device with keys managed via [Azure Information Protection](https://docs.microsoft.com/azure/information-protection/).</span></span>

#### <span data-ttu-id="32897-153">Por que não abrir a guia e os dados do histórico têm criptografia abrir ao lado do cliente adicional?</span><span class="sxs-lookup"><span data-stu-id="32897-153">Why don’t open tab and history data have additional client-side encryption?</span></span>  

<span data-ttu-id="32897-154">Para reduzir o uso de recursos nos dispositivos de usuário final, os dados do histórico são gerados no lado do servidor com base nos dados de roaming da guia aberta.</span><span class="sxs-lookup"><span data-stu-id="32897-154">In order to reduce resource utilization on end user devices, history data is generated server-side based on open tab roaming data.</span></span> <span data-ttu-id="32897-155">Esse processo não seria possível com a criptografia ao lado do cliente desses dados.</span><span class="sxs-lookup"><span data-stu-id="32897-155">This process would not be possible with client-side encryption of this data.</span></span> <span data-ttu-id="32897-156">Para desabilitar a guia aberta e a sincronização do histórico, aplique as políticas [SavingBrowserHistoryDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#savingbrowserhistorydisabled) ou [SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled) .</span><span class="sxs-lookup"><span data-stu-id="32897-156">To disable open tab and history sync, apply the [SavingBrowserHistoryDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#savingbrowserhistorydisabled) or [SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled) policies.</span></span>

#### <span data-ttu-id="32897-157">Os administradores de locatários podem ter suas próprias chaves?</span><span class="sxs-lookup"><span data-stu-id="32897-157">Can tenant admins bring their own key?</span></span>

<span data-ttu-id="32897-158">Sim, pela [Proteção de informações do Azure](https://azure.microsoft.com/services/information-protection/).</span><span class="sxs-lookup"><span data-stu-id="32897-158">Yes, through [Azure Information Protection](https://azure.microsoft.com/services/information-protection/).</span></span>

#### <span data-ttu-id="32897-159">Onde os dados sincronizados são armazenados no Microsoft Edge?</span><span class="sxs-lookup"><span data-stu-id="32897-159">Where is Microsoft Edge sync data stored?</span></span>

<span data-ttu-id="32897-160">Os dados sincronizados para contas do Azure AD são armazenados em servidores seguros de acordo com a ID do locatário.</span><span class="sxs-lookup"><span data-stu-id="32897-160">Synced data for Azure AD accounts is stored in secure servers according to the tenant ID.</span></span> <span data-ttu-id="32897-161">Por exemplo, os dados de um locatário registrado nos Estados Unidos são armazenados em servidores localizados geograficamente nessa região e aproveitam a mesma solução de armazenamento usada pelos aplicativos do Office.</span><span class="sxs-lookup"><span data-stu-id="32897-161">For example, the data for a tenant that is registered in the United States is stored in servers geo-located for that region and uses the same storage solution as Office applications.</span></span>

#### <span data-ttu-id="32897-162">Os dados deixam a nuvem da Microsoft, além de sincronizar com o Microsoft Edge?</span><span class="sxs-lookup"><span data-stu-id="32897-162">Does the data ever leave Microsoft's cloud, aside from syncing to Microsoft Edge?</span></span>

<span data-ttu-id="32897-163">Não.</span><span class="sxs-lookup"><span data-stu-id="32897-163">No.</span></span>

#### <span data-ttu-id="32897-164">Em que termos de serviço a sincronização empresarial se encaixa?</span><span class="sxs-lookup"><span data-stu-id="32897-164">What terms of service does enterprise sync fall under?</span></span>

<span data-ttu-id="32897-165">Os termos de serviço da sincronização do Microsoft Edge se enquadram na licença de software da Microsoft exibida no Microsoft Edge em *Edge://terms*.</span><span class="sxs-lookup"><span data-stu-id="32897-165">Terms of service for Microsoft Edge sync falls under the Microsoft software license viewable in Microsoft Edge at *edge://terms*.</span></span> <span data-ttu-id="32897-166">A sua assinatura e os termos de serviço do Azure AD estão, em última análise, em [Termos de serviço on-line](https://www.microsoft.com/licensing/product-licensing/products)da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="32897-166">Your Azure AD subscription and terms of service ultimately fall under Microsoft's [Online Service Terms](https://www.microsoft.com/licensing/product-licensing/products).</span></span>

#### <span data-ttu-id="32897-167">O Microsoft Edge dá suporte á conformidade do Government Community Cloud (GCC) High?</span><span class="sxs-lookup"><span data-stu-id="32897-167">Does Microsoft Edge support Government Community Cloud (GCC) High compliance?</span></span>

<span data-ttu-id="32897-168">Não atualmente.</span><span class="sxs-lookup"><span data-stu-id="32897-168">Not today.</span></span> <span data-ttu-id="32897-169">Para os clientes na nuvem GCC High, o Microsoft Edge sync está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="32897-169">For customers in the GCC High cloud, Microsoft Edge sync is disabled.</span></span>

### <span data-ttu-id="32897-170">APLICAÇÃO DE SINCRONIZAÇÃO</span><span class="sxs-lookup"><span data-stu-id="32897-170">APPLYING SYNC</span></span>

#### <span data-ttu-id="32897-171">Por que a sincronização do Microsoft Edge não é compatível com todas as assinaturas do M365?</span><span class="sxs-lookup"><span data-stu-id="32897-171">Why isn’t Microsoft Edge sync supported in all M365 subscriptions?</span></span>

<span data-ttu-id="32897-172">A sincronização da empresa depende da Proteção de informações do Azure, que não está disponível em todas as assinaturas do M365.</span><span class="sxs-lookup"><span data-stu-id="32897-172">Enterprise sync depends on Azure Information Protection, which is not available in all M365 subscriptions.</span></span>

#### <span data-ttu-id="32897-173">A sincronização do Microsoft Edge é baseada no Enterprise State Roaming?</span><span class="sxs-lookup"><span data-stu-id="32897-173">Is Microsoft Edge sync based on Enterprise State Roaming?</span></span>

<span data-ttu-id="32897-174">Não.</span><span class="sxs-lookup"><span data-stu-id="32897-174">No.</span></span> <span data-ttu-id="32897-175">O ESR pode ser usado para habilitar a sincronização, mas a sincronização do Microsoft Edge não faz parte do ESR.</span><span class="sxs-lookup"><span data-stu-id="32897-175">ESR can be used to enable sync, but Microsoft Edge sync is not a part of ESR.</span></span> <span data-ttu-id="32897-176">Para obter mais informações, consulte [Sincronização do Microsoft Edge](microsoft-edge-enterprise-sync.md) e [Microsoft Edge e Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).</span><span class="sxs-lookup"><span data-stu-id="32897-176">For more information, see [Microsoft Edge Sync](microsoft-edge-enterprise-sync.md) and [Microsoft Edge and Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).</span></span>

#### <span data-ttu-id="32897-177">O Microsoft Edge oferecerá suporte para sincronização entre o Microsoft Edge e o IE?</span><span class="sxs-lookup"><span data-stu-id="32897-177">Will Microsoft Edge ever support syncing between Microsoft Edge and IE?</span></span>

<span data-ttu-id="32897-178">Não há planos para dar suporte a essa sincronização.</span><span class="sxs-lookup"><span data-stu-id="32897-178">There are no plans to support this syncing.</span></span> <span data-ttu-id="32897-179">Se você ainda precisar do IE no seu ambiente para oferecer suporte aos aplicativos herdados, considere o nosso [novo modo do IE](https://docs.microsoft.com/deployedge/edge-ie-mode).</span><span class="sxs-lookup"><span data-stu-id="32897-179">If you still need IE in your environment to support legacy apps, consider our [new IE mode](https://docs.microsoft.com/deployedge/edge-ie-mode).</span></span>

#### <span data-ttu-id="32897-180">O Microsoft Edge será sincronizado com o Microsoft Edge herdado?</span><span class="sxs-lookup"><span data-stu-id="32897-180">Will Microsoft Edge sync with Microsoft Edge Legacy?</span></span>

<span data-ttu-id="32897-181">Não.</span><span class="sxs-lookup"><span data-stu-id="32897-181">No, it won't.</span></span> <span data-ttu-id="32897-182">Acreditamos que a conexão destes dois ecossistemas comprometerá a confiabilidade da sincronia no Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="32897-182">We believe connecting these two ecosystems will lead to compromises in the reliability of sync in the Microsoft Edge.</span></span> <span data-ttu-id="32897-183">Garantiremos que os dados existentes serão migrados para o Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="32897-183">We will ensure that existing data is migrated to the Microsoft Edge.</span></span> <span data-ttu-id="32897-184">Os usuários também poderão importar dados do navegador de sua preferência.</span><span class="sxs-lookup"><span data-stu-id="32897-184">Users will also be able to import data from browser of their choice.</span></span> <span data-ttu-id="32897-185">Isso também significa que o novo navegador Microsoft Edge não poderá ser sincronizado com o IE.</span><span class="sxs-lookup"><span data-stu-id="32897-185">This also means that new Microsoft Edge browser won't have a way to sync with IE.</span></span>

### <span data-ttu-id="32897-186">GERENCIANDO A SINCRONIZAÇÃO</span><span class="sxs-lookup"><span data-stu-id="32897-186">MANAGING SYNC</span></span>

#### <span data-ttu-id="32897-187">É possível impedir que os meus usuários sincronizem com um locatário pessoal?</span><span class="sxs-lookup"><span data-stu-id="32897-187">Is it possible to stop my users from syncing with a personal tenant?</span></span>

<span data-ttu-id="32897-188">Não diretamente, mas você pode determinar quais perfis podem entrar no Microsoft Edge usando a política [RestrictSigninToPattern](https://docs.microsoft.com/deployedge/microsoft-edge-policies#restrictsignintopattern).</span><span class="sxs-lookup"><span data-stu-id="32897-188">Not directly, but you can determine which profiles can sign on to Microsoft Edge using the [RestrictSigninToPattern](https://docs.microsoft.com/deployedge/microsoft-edge-policies#restrictsignintopattern) policy.</span></span>

## <span data-ttu-id="32897-189">Consulte também</span><span class="sxs-lookup"><span data-stu-id="32897-189">See also</span></span>

- [<span data-ttu-id="32897-190">Página de aterrissagem do Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="32897-190">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="32897-191">Microsoft Edge e Enterprise State Roaming</span><span class="sxs-lookup"><span data-stu-id="32897-191">Microsoft Edge and Enterprise State Roaming</span></span>](microsoft-edge-enterprise-state-roaming.md)
