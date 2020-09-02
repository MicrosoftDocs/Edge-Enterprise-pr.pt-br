---
title: Visão geral da segurança do Microsoft Edge
ms.author: srugh
author: srugh
manager: seanlyn
ms.date: 04/29/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Visão geral da implantação do Microsoft Edge
ms.openlocfilehash: f22f2dcbace00cd535d201950c2af488c708525b
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979156"
---
# <span data-ttu-id="87ca1-103">Visão geral da segurança do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="87ca1-103">Overview of Microsoft Edge security</span></span>
  
<span data-ttu-id="87ca1-104">Os administradores de TI da empresa estão constantemente enfrentando uma infinidade de desafios de segurança existentes e emergentes. Ao mesmo tempo, protegem a rede corporativa e os dispositivos de ataques mal-intencionados, assim como impedem o acesso não autorizado e vazamentos de dados corporativos.</span><span class="sxs-lookup"><span data-stu-id="87ca1-104">IT admins in the enterprise are constantly facing a myriad of existing and emerging security challenges while protecting the corporate network and devices from malicious attacks and preventing unauthorized access and leaks of corporate data.</span></span> <span data-ttu-id="87ca1-105">O Microsoft Edge fornece vários recursos exclusivos internos e nativos que ajudam a resolver esses desafios.</span><span class="sxs-lookup"><span data-stu-id="87ca1-105">Microsoft Edge provides several natively built, unique capabilities that help address these challenges.</span></span>

> [!NOTE]
> <span data-ttu-id="87ca1-106">Este artigo se aplica ao Microsoft Edge versão 77 ou posteriores.</span><span class="sxs-lookup"><span data-stu-id="87ca1-106">This article applies to Microsoft Edge version 77 or later.</span></span>

## <span data-ttu-id="87ca1-107">Acesso condicional</span><span class="sxs-lookup"><span data-stu-id="87ca1-107">Conditional Access</span></span>

<span data-ttu-id="87ca1-108">Um aspecto fundamental da segurança na nuvem é a identidade e o acesso ao gerenciamento de seus recursos na nuvem.</span><span class="sxs-lookup"><span data-stu-id="87ca1-108">A key aspect of cloud security is identity and access when it comes to managing your cloud resources.</span></span> <span data-ttu-id="87ca1-109">Em um mundo que prioriza a mobilidade e a nuvem, os usuários podem acessar os recursos da sua organização usando vários dispositivos e aplicativos em qualquer lugar.</span><span class="sxs-lookup"><span data-stu-id="87ca1-109">In a mobile-first, cloud-first world, users can access your organization's resources using a variety of devices and apps from anywhere.</span></span> <span data-ttu-id="87ca1-110">Como resultado, o foco apenas em quem pode acessar um recurso não é suficiente.</span><span class="sxs-lookup"><span data-stu-id="87ca1-110">As a result of this, just focusing on who can access a resource is not sufficient.</span></span> <span data-ttu-id="87ca1-111">Também é necessário considerar como um recurso é acessado.</span><span class="sxs-lookup"><span data-stu-id="87ca1-111">You also need to factor in how a resource is accessed.</span></span> <span data-ttu-id="87ca1-112">O acesso condicional do Azure Active Directory (Azure AD) ajuda você a dominar o equilíbrio entre segurança e produtividade.</span><span class="sxs-lookup"><span data-stu-id="87ca1-112">Azure Active Directory (Azure AD) Conditional Access helps you master the balance between security and productivity.</span></span>

### <span data-ttu-id="87ca1-113">Acesso a recursos protegidos com acesso condicional no Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="87ca1-113">Accessing Conditional Access protected resources in Microsoft Edge</span></span>

<span data-ttu-id="87ca1-114">O Microsoft Edge oferece suporte ao acesso condicional do Azure AD nativamente.</span><span class="sxs-lookup"><span data-stu-id="87ca1-114">Microsoft Edge natively supports Azure AD Conditional Access.</span></span> <span data-ttu-id="87ca1-115">Não é necessário instalar uma extensão separada.</span><span class="sxs-lookup"><span data-stu-id="87ca1-115">There's no need to install a separate extension.</span></span> <span data-ttu-id="87ca1-116">Quando você estiver conectado a um perfil do Microsoft Edge com as credenciais empresariais de AD do Azure, o Microsoft Edge permite um acesso impecável aos recursos de nuvem empresarial protegidos usando o Acesso condicional.</span><span class="sxs-lookup"><span data-stu-id="87ca1-116">When you're signed into a Microsoft Edge profile with enterprise Azure AD credentials, Microsoft Edge allows seamless access to enterprise cloud resources protected using Conditional Access.</span></span>

<span data-ttu-id="87ca1-117">Em um dispositivo compatível, a identidade que acessa o recurso deve corresponder à identidade do perfil.</span><span class="sxs-lookup"><span data-stu-id="87ca1-117">On a compliant device, the identity accessing the resource should match the identity on the profile.</span></span>  <span data-ttu-id="87ca1-118">Se isso não acontecer, você verá uma mensagem como a da próxima captura de tela.</span><span class="sxs-lookup"><span data-stu-id="87ca1-118">If it doesn't, you'll see a message like the one in the next screenshot.</span></span> <span data-ttu-id="87ca1-119">No exemplo de captura de tela, "testadmin@evostsoneboxtest.com" é a conta necessária para acessar o recurso.</span><span class="sxs-lookup"><span data-stu-id="87ca1-119">In the screenshot example, "testadmin@evostsoneboxtest.com" is the sign-in account needed to access the resource.</span></span>

![Mensagem de acesso condicional no navegador](./media/edge-security/microsoft-edge-security-conditional-access.png)

<span data-ttu-id="87ca1-121">Para continuar, você precisa alternar para o perfil necessário (se tiver um) ou criar um perfil com a identidade correspondente.</span><span class="sxs-lookup"><span data-stu-id="87ca1-121">To continue, you have to switch to the required profile (if you have one) or create a profile with matching identity.</span></span>

<span data-ttu-id="87ca1-122">Para entrar e trabalhar com seu perfil, clique na imagem da conta no canto superior direito do navegador.</span><span class="sxs-lookup"><span data-stu-id="87ca1-122">To sign in and work with your profile, click the account picture in the top right corner of the browser.</span></span> <span data-ttu-id="87ca1-123">É possível usar o menu suspendo para:</span><span class="sxs-lookup"><span data-stu-id="87ca1-123">You can use the dropdown menu to:</span></span>

- <span data-ttu-id="87ca1-124">Selecionar outro perfil.</span><span class="sxs-lookup"><span data-stu-id="87ca1-124">Select another profile.</span></span> <span data-ttu-id="87ca1-125">Clicar no nome do perfil.</span><span class="sxs-lookup"><span data-stu-id="87ca1-125">Click the profile name.</span></span>
- <span data-ttu-id="87ca1-126">Criar um perfil.</span><span class="sxs-lookup"><span data-stu-id="87ca1-126">Create a profile.</span></span> <span data-ttu-id="87ca1-127">Clique em **Adicionar um recurso**.</span><span class="sxs-lookup"><span data-stu-id="87ca1-127">Click **Add a profile**.</span></span>
- <span data-ttu-id="87ca1-128">Gerenciar seus perfis.</span><span class="sxs-lookup"><span data-stu-id="87ca1-128">Manage your profiles.</span></span> <span data-ttu-id="87ca1-129">Clique em **Gerenciar configurações de perfil**.</span><span class="sxs-lookup"><span data-stu-id="87ca1-129">Click **Manage profile settings**.</span></span>

<span data-ttu-id="87ca1-130">Esse suporte está disponível em todas as plataformas, incluindo todas as versões compatíveis do Windows e do macOS.</span><span class="sxs-lookup"><span data-stu-id="87ca1-130">This support is available across all platforms, including all supported versions of Windows and macOS.</span></span>

### <span data-ttu-id="87ca1-131">Como implantar o Acesso condicional no Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="87ca1-131">How to deploy Conditional Access in Azure Active Directory</span></span>

<span data-ttu-id="87ca1-132">[Implantar Acesso condicional](https://docs.microsoft.com/azure/active-directory/conditional-access/plan-conditional-access) fornece um guia detalhado para ajudar a implantar o Acesso condicional no Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="87ca1-132">[Deploy Conditional Access](https://docs.microsoft.com/azure/active-directory/conditional-access/plan-conditional-access) provides a detailed guide to help deploy Conditional Access in Azure Active Directory.</span></span>

## <span data-ttu-id="87ca1-133">Consulte também</span><span class="sxs-lookup"><span data-stu-id="87ca1-133">See also</span></span>

- [<span data-ttu-id="87ca1-134">Página de aterrissagem do Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="87ca1-134">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="87ca1-135">Vídeo: segurança, compatibilidade e gerenciabilidade</span><span class="sxs-lookup"><span data-stu-id="87ca1-135">Video: Security, compatibility, and manageability</span></span>](/microsoft-edge-video-security-compatibility-manageability.md)
