---
title: Configurar a sincronização do Microsoft Edge Enterprise
ms.author: collw
author: dan-wesley
manager: silvanam
ms.date: 03/08/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Opções de administrador e de usuário para configurar o Microsoft Edge para sincronizar os favoritos, senhas e outros dados do navegador.
ms.openlocfilehash: 99edc97bd5f4bab7bf421e0d15e512c5f6f76cc0
ms.sourcegitcommit: 4192328ee585bc32a9be528766b8a5a98e046c8e
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/25/2021
ms.locfileid: "11617751"
---
# <a name="configure-microsoft-edge-enterprise-sync"></a><span data-ttu-id="5a0d9-103">Configurar a sincronização de empresa do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="5a0d9-103">Configure Microsoft Edge enterprise sync</span></span>

<span data-ttu-id="5a0d9-104">Este artigo explica como os administradores podem configurar o Microsoft Edge para sincronizar os favoritos, senhas e outros dados do navegador do usuário em todos os dispositivos conectados.Se você não é um administrador, visite este artigo para saber como se conectar e sincronizar o Microsoft Edge entre dispositivos.</span><span class="sxs-lookup"><span data-stu-id="5a0d9-104">This article explains how admins can configure Microsoft Edge to sync user favorites, passwords, and other browser data across all signed-in devices.If you are not an admin, please visit this article for how to sign-in and sync Microsoft Edge across devices.</span></span> <span data-ttu-id="5a0d9-105">[Entrar para sincronizar Microsoft Edge entre dispositivos](https://support.microsoft.com/microsoft-edge/sign-in-to-sync-microsoft-edge-across-devices-e6ffa79b-ed52-aa32-47e2-5d5597fe4674).</span><span class="sxs-lookup"><span data-stu-id="5a0d9-105">[Sign in to sync Microsoft Edge across devices](https://support.microsoft.com/microsoft-edge/sign-in-to-sync-microsoft-edge-across-devices-e6ffa79b-ed52-aa32-47e2-5d5597fe4674).</span></span>

> [!NOTE]
> <span data-ttu-id="5a0d9-106">Aplica-se ao Microsoft Edge versão 77 ou posterior, a menos que indicado de outra forma.</span><span class="sxs-lookup"><span data-stu-id="5a0d9-106">Applies to Microsoft Edge version 77 or later unless otherwise noted.</span></span>

## <a name="overview"></a><span data-ttu-id="5a0d9-107">Visão geral</span><span class="sxs-lookup"><span data-stu-id="5a0d9-107">Overview</span></span>

<span data-ttu-id="5a0d9-108">A sincronização do Microsoft Edge permite que os usuários acessem seus dados de navegação em todos os dispositivos conectados.</span><span class="sxs-lookup"><span data-stu-id="5a0d9-108">Microsoft Edge sync enables users to access their browsing data across all their signed-in devices.</span></span> <span data-ttu-id="5a0d9-109">Os dados com suporte na sincronização incluem:</span><span class="sxs-lookup"><span data-stu-id="5a0d9-109">The data supported by sync includes:</span></span>

- <span data-ttu-id="5a0d9-110">Favoritos</span><span class="sxs-lookup"><span data-stu-id="5a0d9-110">Favorites</span></span>
- <span data-ttu-id="5a0d9-111">Senhas</span><span class="sxs-lookup"><span data-stu-id="5a0d9-111">Passwords</span></span>
- <span data-ttu-id="5a0d9-112">Endereços e etc. (preenchimento de formulário)</span><span class="sxs-lookup"><span data-stu-id="5a0d9-112">Addresses and more (form-fill)</span></span>
- <span data-ttu-id="5a0d9-113">Coleções</span><span class="sxs-lookup"><span data-stu-id="5a0d9-113">Collections</span></span>
- <span data-ttu-id="5a0d9-114">Configurações</span><span class="sxs-lookup"><span data-stu-id="5a0d9-114">Settings</span></span>
- <span data-ttu-id="5a0d9-115">Extensão</span><span class="sxs-lookup"><span data-stu-id="5a0d9-115">Extension</span></span>
- <span data-ttu-id="5a0d9-116">Abrir guias (disponível no Microsoft Edge versão 88)</span><span class="sxs-lookup"><span data-stu-id="5a0d9-116">Open tabs (available in Microsoft Edge version 88)</span></span>
- <span data-ttu-id="5a0d9-117">Histórico (disponível no Microsoft Edge versão 88)</span><span class="sxs-lookup"><span data-stu-id="5a0d9-117">History (available in Microsoft Edge version 88)</span></span>

<span data-ttu-id="5a0d9-118">A funcionalidade de sincronização é habilitada através do consentimento do usuário, e os usuários podem ativar ou desativar a sincronização de cada um dos tipos de dados listados acima.</span><span class="sxs-lookup"><span data-stu-id="5a0d9-118">Sync functionality is enabled via user consent and users can turn sync on or off for each of the data types listed above.</span></span> <span data-ttu-id="5a0d9-119">Se um usuário estiver com problemas de sincronização, talvez seja necessário redefinir a sincronização em **Configurações** > **Perfis** > **Redefinir sincronização**.</span><span class="sxs-lookup"><span data-stu-id="5a0d9-119">If a user is experiencing a sync issue they might need to reset sync in **Settings** > **Profiles** > **Reset sync**.</span></span>

> [!NOTE]
> <span data-ttu-id="5a0d9-120">Outros dados de configuração e conectividade do dispositivo (como nome, marca e modelo do dispositivo) são carregados para dar suporte à funcionalidade de sincronização.</span><span class="sxs-lookup"><span data-stu-id="5a0d9-120">Additional device connectivity and configuration data (such as device name, make and model) is uploaded to support sync functionality.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="5a0d9-121">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="5a0d9-121">Prerequisites</span></span>

<span data-ttu-id="5a0d9-122">A sincronização do Microsoft Edge das contas do Azure Active Directory (Azure AD) está disponível para qualquer uma das seguintes assinaturas:</span><span class="sxs-lookup"><span data-stu-id="5a0d9-122">Microsoft Edge sync for Azure Active Directory (Azure AD) accounts is available for any of the following subscriptions:</span></span>

- <span data-ttu-id="5a0d9-123">Azure AD Premium (P1 ou P2)</span><span class="sxs-lookup"><span data-stu-id="5a0d9-123">Azure AD Premium (P1 or P2)</span></span>
- <span data-ttu-id="5a0d9-124">M365 Business Premium</span><span class="sxs-lookup"><span data-stu-id="5a0d9-124">M365 Business Premium</span></span>
- <span data-ttu-id="5a0d9-125">Office 365 E1 e superior</span><span class="sxs-lookup"><span data-stu-id="5a0d9-125">Office 365 E1 and above</span></span>
- <span data-ttu-id="5a0d9-126">Proteção de informações do Azure (AIP) (P1 ou P2)</span><span class="sxs-lookup"><span data-stu-id="5a0d9-126">Azure Information Protection (AIP) (P1 or P2)</span></span>
- <span data-ttu-id="5a0d9-127">Todas as assinaturas EDU (Aplicativos da Microsoft para Estudantes ou Docentes, Exchange Online para Estudantes ou Docentes, O365 A1 ou superior, M365 A1 ou superior, Proteção de Informações do Azure P1 ou P2 para Estudantes ou Docentes)</span><span class="sxs-lookup"><span data-stu-id="5a0d9-127">All EDU subscriptions (Microsoft Apps for Students or Faculty, Exchange Online for Students or Faculty, O365 A1 or above, M365 A1 or above, or Azure Information Protection P1 or P2 for Students or Faculty)</span></span>

## <a name="sync-group-policies"></a><span data-ttu-id="5a0d9-128">Políticas de grupo de sincronização</span><span class="sxs-lookup"><span data-stu-id="5a0d9-128">Sync group policies</span></span>

<span data-ttu-id="5a0d9-129">Os administradores podem usar as seguintes políticas de grupo para configurar e gerenciar a sincronização do Microsoft Edge:</span><span class="sxs-lookup"><span data-stu-id="5a0d9-129">Admins can use the following group policies to configure and manage Microsoft Edge sync:</span></span>

- <span data-ttu-id="5a0d9-130">[SyncDisabled](./microsoft-edge-policies.md#syncdisabled): desabilita completamente a sincronização.</span><span class="sxs-lookup"><span data-stu-id="5a0d9-130">[SyncDisabled](./microsoft-edge-policies.md#syncdisabled): Disables sync completely.</span></span>
- <span data-ttu-id="5a0d9-131">[SavingBrowserHistoryDisabled](./microsoft-edge-policies.md#savingbrowserhistorydisabled): desabilita o salvamento do histórico de navegação e a sincronização. Também desabilita a sincronização das guias abertas.</span><span class="sxs-lookup"><span data-stu-id="5a0d9-131">[SavingBrowserHistoryDisabled](./microsoft-edge-policies.md#savingbrowserhistorydisabled): Disables saving browsing history and sync. This policy also disables open-tabs sync.</span></span>
- <span data-ttu-id="5a0d9-132">[AllowDeletingBrowserHistory](./microsoft-edge-policies.md#allowdeletingbrowserhistory): quando essa política é definida como Desabilitada, a sincronização do histórico também será desabilitada.</span><span class="sxs-lookup"><span data-stu-id="5a0d9-132">[AllowDeletingBrowserHistory](./microsoft-edge-policies.md#allowdeletingbrowserhistory): When this policy is set to disabled, history sync will also be disabled.</span></span>
- <span data-ttu-id="5a0d9-133">[SyncTypesListDisabled](./microsoft-edge-policies.md#synctypeslistdisabled): configura a lista dos tipos excluídos da sincronização.</span><span class="sxs-lookup"><span data-stu-id="5a0d9-133">[SyncTypesListDisabled](./microsoft-edge-policies.md#synctypeslistdisabled): Configure the list of types that are excluded from synchronization.</span></span>
- <span data-ttu-id="5a0d9-134">[RoamingProfileSupportEnabled](./microsoft-edge-policies.md#roamingprofilesupportenabled): permite que os perfis Active Directory (AD) usem o armazenamento local.</span><span class="sxs-lookup"><span data-stu-id="5a0d9-134">[RoamingProfileSupportEnabled](./microsoft-edge-policies.md#roamingprofilesupportenabled): Allow Active Directory (AD) profiles to use on-premises storage.</span></span> <span data-ttu-id="5a0d9-135">Para obter mais informações, confira [Sincronização local para usuários do Active Directory (AD)](./microsoft-edge-on-premises-sync.md).</span><span class="sxs-lookup"><span data-stu-id="5a0d9-135">For more information, see [On-premises sync for Active Directory (AD) users](./microsoft-edge-on-premises-sync.md).</span></span>
- <span data-ttu-id="5a0d9-136">[ForceSync](/deployedge/microsoft-edge-policies#forcesync): ativar a sincronização por padrão e não exigir consentimento do usuário para sincronizar.</span><span class="sxs-lookup"><span data-stu-id="5a0d9-136">[ForceSync](/deployedge/microsoft-edge-policies#forcesync): Turn on sync by default and do not require user consent to sync.</span></span>  

## <a name="configure-microsoft-edge-sync"></a><span data-ttu-id="5a0d9-137">Configurar a sincronização do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="5a0d9-137">Configure Microsoft Edge sync</span></span>

<span data-ttu-id="5a0d9-138">As opções de configuração para a sincronização do Microsoft Edge estão disponíveis por meio do serviço de Proteção de Informações do Azure (AIP).</span><span class="sxs-lookup"><span data-stu-id="5a0d9-138">Configuration options for Microsoft Edge sync are available through the Azure Information Protection (AIP) service.</span></span> <span data-ttu-id="5a0d9-139">Quando o (AIP) estiver habilitado para um locatário, todos os usuários poderão sincronizar os dados do Microsoft Edge, independentemente do licenciamento.</span><span class="sxs-lookup"><span data-stu-id="5a0d9-139">When AIP is enabled for a tenant, all users can sync Microsoft Edge data, regardless of licensing.</span></span> <span data-ttu-id="5a0d9-140">Instruções sobre como habilitar o AIP estão disponíveis [aqui](/azure/information-protection/activate-office365).</span><span class="sxs-lookup"><span data-stu-id="5a0d9-140">Instructions on how to enable AIP can be found [here](/azure/information-protection/activate-office365).</span></span>

<span data-ttu-id="5a0d9-141">Para restringir a sincronização a certos conjuntos de usuários, você pode habilitar a [Política de controle de integração do AIP](/powershell/module/aipservice/set-aipserviceonboardingcontrolpolicy?preserve-view=true&view=azureipps)  para esses usuários.</span><span class="sxs-lookup"><span data-stu-id="5a0d9-141">To restrict sync to certain set of users, you can enable the [AIP onboarding control policy](/powershell/module/aipservice/set-aipserviceonboardingcontrolpolicy?preserve-view=true&view=azureipps) for those users.</span></span> <span data-ttu-id="5a0d9-142">Se a sincronização ainda não estiver disponível depois de garantir que todos os usuários necessários estejam integrados, certifique-se de que o IPCv3Service está habilitado usando o cmdlet [Get-AIPServiceIPCv3](/powershell/module/aipservice/get-aipserviceipcv3?preserve-view=true&view=azureipps)  PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5a0d9-142">If sync is still not available after ensuring that all necessary users are onboarded, ensure that the IPCv3Service is enabled using the [Get-AIPServiceIPCv3](/powershell/module/aipservice/get-aipserviceipcv3?preserve-view=true&view=azureipps)  PowerShell cmdlet.</span></span>

> [!CAUTION]
> <span data-ttu-id="5a0d9-143">Ativar a Proteção de Informações do Azure também permitirá que outros aplicativos, como o Microsoft Word ou o Microsoft Outlook, protejam o conteúdo com o AIP.</span><span class="sxs-lookup"><span data-stu-id="5a0d9-143">Activating Azure Information Protection will also allow other applications, such as Microsoft Word or Microsoft Outlook, to protect content with AIP.</span></span> <span data-ttu-id="5a0d9-144">Além disso, qualquer política de controle de integração usada para restringir a sincronização do Microsoft Edge também restringirá outros aplicativos de proteger conteúdo usando o AIP.</span><span class="sxs-lookup"><span data-stu-id="5a0d9-144">In addition, any onboarding control policy used to restrict Edge sync will also restrict other applications from protecting content using AIP.</span></span>

## <a name="microsoft-edge-and-enterprise-state-roaming-esr"></a><span data-ttu-id="5a0d9-145">Microsoft Edge e ESR (Enterprise State Roaming)</span><span class="sxs-lookup"><span data-stu-id="5a0d9-145">Microsoft Edge and Enterprise State Roaming (ESR)</span></span>

<span data-ttu-id="5a0d9-146">O Microsoft Edge é um aplicativo de plataforma cruzada com um escopo expandido para sincronizar dados de usuários em todos os seus dispositivos, e não faz mais parte do Enterprise State Roaming do Azure AD.</span><span class="sxs-lookup"><span data-stu-id="5a0d9-146">Microsoft Edge is a cross-platform application with an expanded scope for syncing user data across all their devices and is no longer a part of Azure AD Enterprise State Roaming.</span></span> <span data-ttu-id="5a0d9-147">No entanto, o Microsoft Edge cumprirá as promessas de proteção de dados do ESR, como a capacidade de trazer sua própria chave.</span><span class="sxs-lookup"><span data-stu-id="5a0d9-147">However, the Microsoft Edge will fulfill the data protection promises of ESR, such as the ability to bring your own key.</span></span> <span data-ttu-id="5a0d9-148">Para obter mais informações, confira [Microsoft Edge e Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).</span><span class="sxs-lookup"><span data-stu-id="5a0d9-148">For more information, see [Microsoft Edge and Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="5a0d9-149">Veja também</span><span class="sxs-lookup"><span data-stu-id="5a0d9-149">See also</span></span>

- [<span data-ttu-id="5a0d9-150">Sincronização do Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="5a0d9-150">Microsoft Edge Enterprise Sync</span></span>](microsoft-edge-enterprise-sync.md)
- [<span data-ttu-id="5a0d9-151">Diagnosticar e corrigir problemas de sincronização do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="5a0d9-151">Diagnose and fix Microsoft Edge sync issues</span></span>](microsoft-edge-troubleshoot-enterprise-sync.md)
- [<span data-ttu-id="5a0d9-152">Microsoft Edge e Enterprise State Roaming</span><span class="sxs-lookup"><span data-stu-id="5a0d9-152">Microsoft Edge and Enterprise State Roaming</span></span>](microsoft-edge-enterprise-state-roaming.md)
- [<span data-ttu-id="5a0d9-153">Página de aterrissagem do Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="5a0d9-153">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)