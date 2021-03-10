---
title: Configurar a sincronização do Microsoft Edge Enterprise
ms.author: scottbo
author: dan-wesley
manager: silvanam
ms.date: 03/08/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Opções de administrador e de usuário para configurar o Microsoft Edge para sincronizar os favoritos, senhas e outros dados do navegador.
ms.openlocfilehash: bfaa1db297093d0b0655a8d217aefcd59d11ac5e
ms.sourcegitcommit: 86e0de9b27ad4297a6d5a57c866d7ef4fc7bb0cd
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "11400135"
---
# <a name="configure-microsoft-edge-enterprise-sync"></a><span data-ttu-id="479a5-103">Configurar a sincronização do Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="479a5-103">Configure Microsoft Edge enterprise sync</span></span>

<span data-ttu-id="479a5-104">Este artigo explica como os administradores podem configurar o Microsoft Edge para sincronizar os favoritos, senhas e outros dados do navegador do usuário em todos os dispositivos conectados.</span><span class="sxs-lookup"><span data-stu-id="479a5-104">This article explains how admins can configure Microsoft Edge to sync user favorites, passwords, and other browser data across all signed-in devices.</span></span>

> [!NOTE]
> <span data-ttu-id="479a5-105">Aplica-se ao Microsoft Edge versão 77 ou posterior, a menos que indicado de outra forma.</span><span class="sxs-lookup"><span data-stu-id="479a5-105">Applies to Microsoft Edge version 77 or later unless otherwise noted.</span></span>

## <a name="overview"></a><span data-ttu-id="479a5-106">Visão geral</span><span class="sxs-lookup"><span data-stu-id="479a5-106">Overview</span></span>

<span data-ttu-id="479a5-107">A sincronização do Microsoft Edge permite que os usuários acessem seus dados de navegação em todos os dispositivos conectados.</span><span class="sxs-lookup"><span data-stu-id="479a5-107">Microsoft Edge sync enables users to access their browsing data across all their signed-in devices.</span></span> <span data-ttu-id="479a5-108">Os dados com suporte na sincronização incluem:</span><span class="sxs-lookup"><span data-stu-id="479a5-108">The data supported by sync includes:</span></span>

- <span data-ttu-id="479a5-109">Favoritos</span><span class="sxs-lookup"><span data-stu-id="479a5-109">Favorites</span></span>
- <span data-ttu-id="479a5-110">Senhas</span><span class="sxs-lookup"><span data-stu-id="479a5-110">Passwords</span></span>
- <span data-ttu-id="479a5-111">Endereços e etc. (preenchimento de formulário)</span><span class="sxs-lookup"><span data-stu-id="479a5-111">Addresses and more (form-fill)</span></span>
- <span data-ttu-id="479a5-112">Coleções</span><span class="sxs-lookup"><span data-stu-id="479a5-112">Collections</span></span>
- <span data-ttu-id="479a5-113">Configurações</span><span class="sxs-lookup"><span data-stu-id="479a5-113">Settings</span></span>
- <span data-ttu-id="479a5-114">Extensão</span><span class="sxs-lookup"><span data-stu-id="479a5-114">Extension</span></span>
- <span data-ttu-id="479a5-115">Abrir guias (disponível no Microsoft Edge versão 88)</span><span class="sxs-lookup"><span data-stu-id="479a5-115">Open tabs (available in Microsoft Edge version 88)</span></span>
- <span data-ttu-id="479a5-116">Histórico (disponível no Microsoft Edge versão 88)</span><span class="sxs-lookup"><span data-stu-id="479a5-116">History (available in Microsoft Edge version 88)</span></span>

<span data-ttu-id="479a5-117">A funcionalidade de sincronização é habilitada através do consentimento do usuário, e os usuários podem ativar ou desativar a sincronização de cada um dos tipos de dados listados acima.</span><span class="sxs-lookup"><span data-stu-id="479a5-117">Sync functionality is enabled via user consent and users can turn sync on or off for each of the data types listed above.</span></span> <span data-ttu-id="479a5-118">Se um usuário estiver com problemas de sincronização, talvez seja necessário redefinir a sincronização em **Configurações** > **Perfis** > **Redefinir sincronização**.</span><span class="sxs-lookup"><span data-stu-id="479a5-118">If a user is experiencing a sync issue they might need to reset sync in **Settings** > **Profiles** > **Reset sync**.</span></span>

> [!NOTE]
> <span data-ttu-id="479a5-119">Outros dados de configuração e conectividade do dispositivo (como nome, marca e modelo do dispositivo) são carregados para dar suporte à funcionalidade de sincronização.</span><span class="sxs-lookup"><span data-stu-id="479a5-119">Additional device connectivity and configuration data (such as device name, make and model) is uploaded to support sync functionality.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="479a5-120">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="479a5-120">Prerequisites</span></span>

<span data-ttu-id="479a5-121">A sincronização do Microsoft Edge das contas do Azure Active Directory (Azure AD) está disponível para qualquer uma das seguintes assinaturas:</span><span class="sxs-lookup"><span data-stu-id="479a5-121">Microsoft Edge sync for Azure Active Directory (Azure AD) accounts is available for any of the following subscriptions:</span></span>

- <span data-ttu-id="479a5-122">Azure AD Premium (P1 ou P2)</span><span class="sxs-lookup"><span data-stu-id="479a5-122">Azure AD Premium (P1 or P2)</span></span>
- <span data-ttu-id="479a5-123">M365 Business Premium</span><span class="sxs-lookup"><span data-stu-id="479a5-123">M365 Business Premium</span></span>
- <span data-ttu-id="479a5-124">Office 365 E1 e superior</span><span class="sxs-lookup"><span data-stu-id="479a5-124">Office 365 E1 and above</span></span>
- <span data-ttu-id="479a5-125">Proteção de informações do Azure (AIP) (P1 ou P2)</span><span class="sxs-lookup"><span data-stu-id="479a5-125">Azure Information Protection (AIP) (P1 or P2)</span></span>
- <span data-ttu-id="479a5-126">Todas as assinaturas EDU (Aplicativos da Microsoft para Estudantes ou Docentes, Exchange Online para Estudantes ou Docentes, O365 A1 ou superior, M365 A1 ou superior, Proteção de Informações do Azure P1 ou P2 para Estudantes ou Docentes)</span><span class="sxs-lookup"><span data-stu-id="479a5-126">All EDU subscriptions (Microsoft Apps for Students or Faculty, Exchange Online for Students or Faculty, O365 A1 or above, M365 A1 or above, or Azure Information Protection P1 or P2 for Students or Faculty)</span></span>

## <a name="sync-group-policies"></a><span data-ttu-id="479a5-127">Políticas de grupo de sincronização</span><span class="sxs-lookup"><span data-stu-id="479a5-127">Sync group policies</span></span>

<span data-ttu-id="479a5-128">Os administradores podem usar as seguintes políticas de grupo para configurar e gerenciar a sincronização do Microsoft Edge:</span><span class="sxs-lookup"><span data-stu-id="479a5-128">Admins can use the following group policies to configure and manage Microsoft Edge sync:</span></span>

- <span data-ttu-id="479a5-129">[SyncDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#syncdisabled): desabilita completamente a sincronização.</span><span class="sxs-lookup"><span data-stu-id="479a5-129">[SyncDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#syncdisabled): Disables sync completely.</span></span>
- <span data-ttu-id="479a5-130">[SavingBrowserHistoryDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#savingbrowserhistorydisabled): desabilita o salvamento do histórico de navegação e a sincronização. Também desabilita a sincronização das guias abertas.</span><span class="sxs-lookup"><span data-stu-id="479a5-130">[SavingBrowserHistoryDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#savingbrowserhistorydisabled): Disables saving browsing history and sync. This policy also disables open-tabs sync.</span></span>
- <span data-ttu-id="479a5-131">[AllowDeletingBrowserHistory](https://docs.microsoft.com/deployedge/microsoft-edge-policies#allowdeletingbrowserhistory): quando essa política é definida como Desabilitada, a sincronização do histórico também será desabilitada.</span><span class="sxs-lookup"><span data-stu-id="479a5-131">[AllowDeletingBrowserHistory](https://docs.microsoft.com/deployedge/microsoft-edge-policies#allowdeletingbrowserhistory): When this policy is set to disabled, history sync will also be disabled.</span></span>
- <span data-ttu-id="479a5-132">[SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled): configura a lista dos tipos excluídos da sincronização.</span><span class="sxs-lookup"><span data-stu-id="479a5-132">[SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled): Configure the list of types that are excluded from synchronization.</span></span>
- <span data-ttu-id="479a5-133">[RoamingProfileSupportEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#roamingprofilesupportenabled): permite que os perfis Active Directory (AD) usem o armazenamento local.</span><span class="sxs-lookup"><span data-stu-id="479a5-133">[RoamingProfileSupportEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#roamingprofilesupportenabled): Allow Active Directory (AD) profiles to use on-premises storage.</span></span> <span data-ttu-id="479a5-134">Para obter mais informações, confira [Sincronização local para usuários do Active Directory (AD)](https://docs.microsoft.com/DeployEdge/microsoft-edge-on-premises-sync).</span><span class="sxs-lookup"><span data-stu-id="479a5-134">For more information, see [On-premises sync for Active Directory (AD) users](https://docs.microsoft.com/DeployEdge/microsoft-edge-on-premises-sync).</span></span>
- <span data-ttu-id="479a5-135">[ForceSync]( https://docs.microsoft.com/deployedge/microsoft-edge-policies#forcesync): ativar a sincronização por padrão e não exigir consentimento do usuário para sincronizar.</span><span class="sxs-lookup"><span data-stu-id="479a5-135">[ForceSync]( https://docs.microsoft.com/deployedge/microsoft-edge-policies#forcesync): Turn on sync by default and do not require user consent to sync.</span></span>  

## <a name="configure-microsoft-edge-sync"></a><span data-ttu-id="479a5-136">Configurar a sincronização do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="479a5-136">Configure Microsoft Edge sync</span></span>

<span data-ttu-id="479a5-137">As opções de configuração para a sincronização do Microsoft Edge estão disponíveis por meio do serviço de Proteção de Informações do Azure (AIP).</span><span class="sxs-lookup"><span data-stu-id="479a5-137">Configuration options for Microsoft Edge sync are available through the Azure Information Protection (AIP) service.</span></span> <span data-ttu-id="479a5-138">Quando o (AIP) estiver habilitado para um locatário, todos os usuários poderão sincronizar os dados do Microsoft Edge, independentemente do licenciamento.</span><span class="sxs-lookup"><span data-stu-id="479a5-138">When AIP is enabled for a tenant, all users can sync Microsoft Edge data, regardless of licensing.</span></span> <span data-ttu-id="479a5-139">Instruções sobre como habilitar o AIP estão disponíveis [aqui](https://docs.microsoft.com/azure/information-protection/activate-office365).</span><span class="sxs-lookup"><span data-stu-id="479a5-139">Instructions on how to enable AIP can be found [here](https://docs.microsoft.com/azure/information-protection/activate-office365).</span></span>

<span data-ttu-id="479a5-140">Para restringir a sincronização a certos conjuntos de usuários, você pode habilitar a [Política de controle de integração do AIP](https://docs.microsoft.com/powershell/module/aipservice/set-aipserviceonboardingcontrolpolicy?view=azureipps&preserve-view=true)  para esses usuários.</span><span class="sxs-lookup"><span data-stu-id="479a5-140">To restrict sync to certain set of users, you can enable the [AIP onboarding control policy](https://docs.microsoft.com/powershell/module/aipservice/set-aipserviceonboardingcontrolpolicy?view=azureipps&preserve-view=true) for those users.</span></span> <span data-ttu-id="479a5-141">Se a sincronização ainda não estiver disponível depois de garantir que todos os usuários necessários estejam integrados, certifique-se de que o IPCv3Service está habilitado usando o cmdlet [Get-AIPServiceIPCv3](https://docs.microsoft.com/powershell/module/aipservice/get-aipserviceipcv3?view=azureipps&preserve-view=true)  PowerShell.</span><span class="sxs-lookup"><span data-stu-id="479a5-141">If sync is still not available after ensuring that all necessary users are onboarded, ensure that the IPCv3Service is enabled using the [Get-AIPServiceIPCv3](https://docs.microsoft.com/powershell/module/aipservice/get-aipserviceipcv3?view=azureipps&preserve-view=true)  PowerShell cmdlet.</span></span>

> [!CAUTION]
> <span data-ttu-id="479a5-142">Ativar a Proteção de Informações do Azure também permitirá que outros aplicativos, como o Microsoft Word ou o Microsoft Outlook, protejam o conteúdo com o AIP.</span><span class="sxs-lookup"><span data-stu-id="479a5-142">Activating Azure Information Protection will also allow other applications, such as Microsoft Word or Microsoft Outlook, to protect content with AIP.</span></span> <span data-ttu-id="479a5-143">Além disso, qualquer política de controle de integração usada para restringir a sincronização do Microsoft Edge também restringirá outros aplicativos de proteger conteúdo usando o AIP.</span><span class="sxs-lookup"><span data-stu-id="479a5-143">In addition, any onboarding control policy used to restrict Edge sync will also restrict other applications from protecting content using AIP.</span></span>

## <a name="microsoft-edge-and-enterprise-state-roaming-esr"></a><span data-ttu-id="479a5-144">Microsoft Edge e ESR (Enterprise State Roaming)</span><span class="sxs-lookup"><span data-stu-id="479a5-144">Microsoft Edge and Enterprise State Roaming (ESR)</span></span>

<span data-ttu-id="479a5-145">O Microsoft Edge é um aplicativo de plataforma cruzada com um escopo expandido para sincronizar dados de usuários em todos os seus dispositivos, e não faz mais parte do Enterprise State Roaming do Azure AD.</span><span class="sxs-lookup"><span data-stu-id="479a5-145">Microsoft Edge is a cross-platform application with an expanded scope for syncing user data across all their devices and is no longer a part of Azure AD Enterprise State Roaming.</span></span> <span data-ttu-id="479a5-146">No entanto, o Microsoft Edge cumprirá as promessas de proteção de dados do ESR, como a capacidade de trazer sua própria chave.</span><span class="sxs-lookup"><span data-stu-id="479a5-146">However, the Microsoft Edge will fulfill the data protection promises of ESR, such as the ability to bring your own key.</span></span> <span data-ttu-id="479a5-147">Para obter mais informações, confira [Microsoft Edge e Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).</span><span class="sxs-lookup"><span data-stu-id="479a5-147">For more information, see [Microsoft Edge and Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="479a5-148">Veja também</span><span class="sxs-lookup"><span data-stu-id="479a5-148">See also</span></span>

- [<span data-ttu-id="479a5-149">Sincronização do Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="479a5-149">Microsoft Edge Enterprise Sync</span></span>](microsoft-edge-enterprise-sync.md)
- [<span data-ttu-id="479a5-150">Diagnosticar e corrigir problemas de sincronização do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="479a5-150">Diagnose and fix Microsoft Edge sync issues</span></span>](microsoft-edge-troubleshoot-enterprise-sync.md)
- [<span data-ttu-id="479a5-151">Microsoft Edge e Enterprise State Roaming</span><span class="sxs-lookup"><span data-stu-id="479a5-151">Microsoft Edge and Enterprise State Roaming</span></span>](microsoft-edge-enterprise-state-roaming.md)
- [<span data-ttu-id="479a5-152">Página de aterrissagem do Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="479a5-152">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
