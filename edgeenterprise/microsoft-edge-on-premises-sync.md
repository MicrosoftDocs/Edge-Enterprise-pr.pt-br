---
title: Sincronização local para usuários do Active Directory (AD)
ms.author: scottbo
author: dan-wesley
manager: silvanam
ms.date: 02/12/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Sincronização local para usuários do Active Directory (AD)
ms.openlocfilehash: adf0adc8370aa1e18d07d0d2e91727d1ac607bf1
ms.sourcegitcommit: 90b8eab62edbed0e0a84780abd7d3854bf95c130
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "11328043"
---
# <span data-ttu-id="1bb54-103">Sincronização local para usuários do Active Directory (AD)</span><span class="sxs-lookup"><span data-stu-id="1bb54-103">On-premises sync for Active Directory (AD) users</span></span>

<span data-ttu-id="1bb54-104">Este artigo explica como os usuários do Active Directory (AD) podem transferir os favoritos e as configurações do Microsoft Edge entre computadores sem se conectar aos serviços de nuvem da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="1bb54-104">This article explains how Active Directory (AD) users can roam Microsoft Edge favorites and settings between computers without connecting to Microsoft cloud services.</span></span>

> [!NOTE]
> <span data-ttu-id="1bb54-105">Este artigo se aplica ao Microsoft Edge versão 85 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="1bb54-105">This article applies to Microsoft Edge version 85 or later.</span></span>

## <span data-ttu-id="1bb54-106">Introdução</span><span class="sxs-lookup"><span data-stu-id="1bb54-106">Introduction</span></span>

<span data-ttu-id="1bb54-107">Sincronizar os dados do usuário no Microsoft Edge normalmente requer uma conta da Microsoft ou uma conta do Azure Active Directory (Azure AD) e uma conexão com os serviços de nuvem da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="1bb54-107">Syncing user data in Microsoft Edge normally requires either a Microsoft Account or an Azure Active Directory (Azure AD) account, and a connection to Microsoft cloud services.</span></span> <span data-ttu-id="1bb54-108">Com a sincronização local, o Microsoft Edge salva os favoritos e as configurações de um usuário do Active Directory em um arquivo que pode ser movido entre diferentes computadores.</span><span class="sxs-lookup"><span data-stu-id="1bb54-108">With on-premises sync, Microsoft Edge saves an Active Directory user's favorites and settings to a file that can be moved between different computers.</span></span> <span data-ttu-id="1bb54-109">A sincronização local não afeta a sincronização de nuvem para esses perfis que os permitem.</span><span class="sxs-lookup"><span data-stu-id="1bb54-109">On-premises sync doesn't interfere with cloud syncing for those profiles that allow it.</span></span>

## <span data-ttu-id="1bb54-110">Como funciona</span><span class="sxs-lookup"><span data-stu-id="1bb54-110">How it works</span></span>

<span data-ttu-id="1bb54-111">O Microsoft Edge permite que perfis sejam associados a contas do Active Directory (AD), que não podem ser usados com sincronização em nuvem. Quando a sincronização local está habilitada, os dados do perfil AD são salvos em um arquivo chamado profile.pb.</span><span class="sxs-lookup"><span data-stu-id="1bb54-111">Microsoft Edge allows profiles to be associated with Active Directory (AD) accounts, which can't be used with cloud sync. When on-premises sync is enabled, the data from the AD profile is saved to a file named profile.pb.</span></span> <span data-ttu-id="1bb54-112">Por padrão, esse arquivo está armazenado em *%APP_DATA%/Microsoft/Edge*.</span><span class="sxs-lookup"><span data-stu-id="1bb54-112">By default, this file is stored in *%APPDATA%/Microsoft/Edge*.</span></span> <span data-ttu-id="1bb54-113">Após a gravação desse arquivo, ele poderá ser movido entre computadores diferentes, e os dados do usuário serão lidos e escritos em cada computador.</span><span class="sxs-lookup"><span data-stu-id="1bb54-113">After this file is written, it can be moved between different computers, and user data will be read and written on each computer.</span></span> <span data-ttu-id="1bb54-114">O Microsoft Edge apenas lê e grava a partir deste arquivo; é responsabilidade do administrador garantir que o arquivo seja movido conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="1bb54-114">Microsoft Edge only reads and writes from this file; it is the admin's responsibility to ensure that the file is moved as needed.</span></span>

## <span data-ttu-id="1bb54-115">Usar sincronização local</span><span class="sxs-lookup"><span data-stu-id="1bb54-115">Use on-premises sync</span></span>

<span data-ttu-id="1bb54-116">Para usar a sincronização local, você precisa habilitá-la, associar um perfil a uma conta do AD e, opcionalmente, alterar a localização dos dados do usuário.</span><span class="sxs-lookup"><span data-stu-id="1bb54-116">To use on-premises sync, you have to enable it, associate a profile with an AD account, and optionally, change the location of the user data.</span></span>

### <span data-ttu-id="1bb54-117">Habilitar sincronização local</span><span class="sxs-lookup"><span data-stu-id="1bb54-117">Enable on-premises sync</span></span>

<span data-ttu-id="1bb54-118">Para habilitar a sincronização local no Microsoft Edge, configure a política [RoamingProfileSupportEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#roamingprofilesupportenabled).</span><span class="sxs-lookup"><span data-stu-id="1bb54-118">To enable on-premises sync in Microsoft Edge, configure the [RoamingProfileSupportEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#roamingprofilesupportenabled) policy.</span></span>

### <span data-ttu-id="1bb54-119">Garantir que o perfil esteja associado a uma conta do Active Directory</span><span class="sxs-lookup"><span data-stu-id="1bb54-119">Ensure that a profile is associated with an Active Directory account</span></span>

<span data-ttu-id="1bb54-120">A sincronização local só funciona com o perfil associado a uma conta do Active Directory (AD).</span><span class="sxs-lookup"><span data-stu-id="1bb54-120">On-premises sync only works with the profile associated with an Active Directory (AD) account.</span></span> <span data-ttu-id="1bb54-121">Se esse perfil não existir, a sincronização local não funcionará.</span><span class="sxs-lookup"><span data-stu-id="1bb54-121">If no such profile exists, on-premises sync will not function.</span></span> <span data-ttu-id="1bb54-122">Para garantir que os usuários entrem com uma conta do AD, configure a política [ConfigureOnPremisesAccountAutoSignIn](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#configureonpremisesaccountautosignin).</span><span class="sxs-lookup"><span data-stu-id="1bb54-122">To ensure that users sign on with an AD account, configure the [ConfigureOnPremisesAccountAutoSignIn](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#configureonpremisesaccountautosignin) policy.</span></span> <span data-ttu-id="1bb54-123">Para a sincronização local, o Microsoft Edge depende apenas do AD para estabelecer uma identidade para os dados do usuário, e não há relação direta entre como o Microsoft Edge lê e escreve os dados locais e como o administrador configurou o roaming para um usuário do AD.</span><span class="sxs-lookup"><span data-stu-id="1bb54-123">For on-premises sync, Microsoft Edge only relies on AD to establish an identity for the user data, and there's no direct relationship between how Microsoft Edge reads and writes on-premises data to how the admin has configured roaming for an AD user.</span></span>

### <span data-ttu-id="1bb54-124">Alterar a localização dos dados do usuário (opcional)</span><span class="sxs-lookup"><span data-stu-id="1bb54-124">Change the location of the user data (optional)</span></span>

<span data-ttu-id="1bb54-125">Por padrão, os dados do usuário são armazenados em um arquivamento chamado **profile.pb** em *%APPDATA%/Microsoft/Edge*.</span><span class="sxs-lookup"><span data-stu-id="1bb54-125">By default, the user data is stored in a filed named **profile.pb** in *%APPDATA%/Microsoft/Edge*.</span></span> <span data-ttu-id="1bb54-126">Para alterar o local desse arquivo, configure a política [RoamingProfileLocation](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#roamingprofilelocation).</span><span class="sxs-lookup"><span data-stu-id="1bb54-126">To change the location of this file, configure the [RoamingProfileLocation](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#roamingprofilelocation) policy.</span></span>

## <span data-ttu-id="1bb54-127">Alterações na experiência do usuário quando a sincronização no local está habilitada</span><span class="sxs-lookup"><span data-stu-id="1bb54-127">Changes in the user experience when on-premises sync is enabled</span></span>

<span data-ttu-id="1bb54-128">Quando a sincronização local estiver habilitada, os usuários não serão solicitados a habilitar a sincronização. Além disso, os usuários não podem desativar a sincronização nas configurações de sincronização e não podem ativar os tipos de sincronização que não têm suporte da sincronização local.</span><span class="sxs-lookup"><span data-stu-id="1bb54-128">When on-premises sync is enabled, users won't be asked to enable sync. In addition, users can't turn off sync in Sync settings, and they can't turn on sync types that aren't supported by on-premises sync.</span></span>

## <span data-ttu-id="1bb54-129">Anotações de uso de sincronização no local</span><span class="sxs-lookup"><span data-stu-id="1bb54-129">On-premises sync usage notes</span></span>

### <span data-ttu-id="1bb54-130">Executando a sincronização de nuvem e a sincronização local no mesmo computador</span><span class="sxs-lookup"><span data-stu-id="1bb54-130">Running cloud sync and on-premises sync on the same computer</span></span>

<span data-ttu-id="1bb54-131">A sincronização local não afeta a sincronização na nuvem. Se o Microsoft Edge tiver várias contas da Microsoft ou perfis do Azure Active Directory que sincronizam com a nuvem, estes perfis continuarão a sincronizar enquanto a sincronização local estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="1bb54-131">On-premises sync doesn't interfere with cloud sync. If Microsoft Edge has multiple Microsoft Account or Azure Active Directory profiles that sync to the cloud, these profiles will continue to sync while on-premises sync is enabled.</span></span>

### <span data-ttu-id="1bb54-132">Não é recomendável executar o Microsoft Edge em mais de um computador por vez</span><span class="sxs-lookup"><span data-stu-id="1bb54-132">Running Microsoft Edge on more than one computer at a time isn't recommended</span></span>

<span data-ttu-id="1bb54-133">Como a sincronização local funciona movendo um arquivo de dados do usuário entre computadores, a sincronização local não sincroniza as alterações entre as sessões simultâneas.</span><span class="sxs-lookup"><span data-stu-id="1bb54-133">Because on-premises sync works by moving a user data file between computers, on-premises sync doesn't sync changes between simultaneous sessions.</span></span> <span data-ttu-id="1bb54-134">Por esse motivo, a sincronização local funciona melhor quando usada em um computador por vez.</span><span class="sxs-lookup"><span data-stu-id="1bb54-134">For this reason, on-premises sync works best when used on one computer at a time.</span></span> <span data-ttu-id="1bb54-135">Se houver sessões locais simultâneas em execução, os dados em qualquer um dos computadores poderão ser substituídos inesperadamente por dados de outro computador na próxima vez que você iniciar uma sessão do navegador.</span><span class="sxs-lookup"><span data-stu-id="1bb54-135">If there are simultaneous on-premises sessions running, data on any of the computers may be unexpectedly overwritten by data from another computer the next time you start a browser session.</span></span>

> [!NOTE]
> <span data-ttu-id="1bb54-136">O Microsoft Edge bloqueia o arquivo **perfil.pb** quando a sincronização local está habilitada.</span><span class="sxs-lookup"><span data-stu-id="1bb54-136">Microsoft Edge locks the **profile.pb** file when on-premises sync is enabled.</span></span> <span data-ttu-id="1bb54-137">Se o redirecionamento de pastas for usado para compartilhar um arquivo **perfil.pb** único entre computadores diferentes, só será possível iniciar uma instância do Microsoft Edge usando esse arquivo.</span><span class="sxs-lookup"><span data-stu-id="1bb54-137">If folder redirection is used to share a single **profile.pb** file between different computers, then only one instance of Microsoft Edge using that file can be started.</span></span>

### <span data-ttu-id="1bb54-138">Usando outras políticas de sincronização com a sincronização local</span><span class="sxs-lookup"><span data-stu-id="1bb54-138">Using other sync policies with on-premises sync</span></span>

<span data-ttu-id="1bb54-139">A política [SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled) pode ser usada para desabilitar seletivamente a sincronização de favoritos ou configurações, se necessário.</span><span class="sxs-lookup"><span data-stu-id="1bb54-139">The [SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled) policy can be used to selectively disable either favorites or settings sync if desired.</span></span> <span data-ttu-id="1bb54-140">A política [SyncDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#syncdisabled) não tem impacto na sincronização local.</span><span class="sxs-lookup"><span data-stu-id="1bb54-140">The [SyncDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#syncdisabled) policy has no impact on on-premises sync.</span></span>

## <span data-ttu-id="1bb54-141">Consulte também</span><span class="sxs-lookup"><span data-stu-id="1bb54-141">See also</span></span>

- [<span data-ttu-id="1bb54-142">Página de aterrissagem do Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="1bb54-142">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="1bb54-143">Microsoft Edge e Enterprise State Roaming</span><span class="sxs-lookup"><span data-stu-id="1bb54-143">Microsoft Edge and Enterprise State Roaming</span></span>](microsoft-edge-enterprise-state-roaming.md)
- [<span data-ttu-id="1bb54-144">Sincronização do Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="1bb54-144">Microsoft Edge Enterprise Sync</span></span>](microsoft-edge-enterprise-sync.md)
