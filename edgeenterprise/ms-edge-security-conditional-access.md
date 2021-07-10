---
title: Microsoft Edge e acesso condicional
ms.author: srugh
author: srugh
manager: seanlyn
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Microsoft Edge e acesso condicional
ms.openlocfilehash: 27d93627f8a86ad821a00d6d78b7db352e9e557a
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/09/2021
ms.locfileid: "11642847"
---
# <a name="microsoft-edge-and-conditional-access"></a><span data-ttu-id="6d236-103">Microsoft Edge e acesso condicional</span><span class="sxs-lookup"><span data-stu-id="6d236-103">Microsoft Edge and Conditional Access</span></span>
  
<span data-ttu-id="6d236-104">Esse artigo descreve como o Microsoft Edge é compatível com o acesso condicional e como acessar os recursos protegidos pelo acesso condicional.</span><span class="sxs-lookup"><span data-stu-id="6d236-104">This article describes how Microsoft Edge supports Conditional Access, and how to access resources protected by Conditional Access.</span></span>

> [!NOTE]
> <span data-ttu-id="6d236-105">Este artigo se aplica ao Microsoft Edge versão 77 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="6d236-105">This article applies to Microsoft Edge version 77 or later.</span></span>

<span data-ttu-id="6d236-106">Um aspecto fundamental da segurança na nuvem é a identidade e o acesso ao gerenciamento de seus recursos na nuvem.</span><span class="sxs-lookup"><span data-stu-id="6d236-106">A key aspect of cloud security is identity and access when it comes to managing your cloud resources.</span></span> <span data-ttu-id="6d236-107">Em um mundo que prioriza a mobilidade e a nuvem, os usuários podem acessar os recursos da sua organização usando vários dispositivos e aplicativos em qualquer lugar.</span><span class="sxs-lookup"><span data-stu-id="6d236-107">In a mobile-first, cloud-first world, users can access your organization's resources using a variety of devices and apps from anywhere.</span></span> <span data-ttu-id="6d236-108">Como resultado, o foco apenas em quem pode acessar um recurso não é suficiente.</span><span class="sxs-lookup"><span data-stu-id="6d236-108">As a result of this, just focusing on who can access a resource is not sufficient.</span></span> <span data-ttu-id="6d236-109">Também é necessário considerar como um recurso é acessado.</span><span class="sxs-lookup"><span data-stu-id="6d236-109">You also need to factor in how a resource is accessed.</span></span> <span data-ttu-id="6d236-110">O acesso condicional do Azure Active Directory (Azure AD) ajuda você a dominar o equilíbrio entre segurança e produtividade.</span><span class="sxs-lookup"><span data-stu-id="6d236-110">Azure Active Directory (Azure AD) Conditional Access helps you master the balance between security and productivity.</span></span>

## <a name="accessing-conditional-access-protected-resources-in-microsoft-edge"></a><span data-ttu-id="6d236-111">Acesso a recursos protegidos com acesso condicional no Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="6d236-111">Accessing Conditional Access protected resources in Microsoft Edge</span></span>

<span data-ttu-id="6d236-112">O Microsoft Edge oferece suporte ao acesso condicional do Azure AD nativamente.</span><span class="sxs-lookup"><span data-stu-id="6d236-112">Microsoft Edge natively supports Azure AD Conditional Access.</span></span> <span data-ttu-id="6d236-113">Não é necessário instalar uma extensão separada.</span><span class="sxs-lookup"><span data-stu-id="6d236-113">There's no need to install a separate extension.</span></span> <span data-ttu-id="6d236-114">Quando você estiver conectado a um perfil do Microsoft Edge com as credenciais empresariais de AD do Azure, o Microsoft Edge permite um acesso impecável aos recursos de nuvem empresarial protegidos usando o Acesso condicional.</span><span class="sxs-lookup"><span data-stu-id="6d236-114">When you're signed into a Microsoft Edge profile with enterprise Azure AD credentials, Microsoft Edge allows seamless access to enterprise cloud resources protected using Conditional Access.</span></span>

<span data-ttu-id="6d236-115">Em um dispositivo compatível, a identidade que acessa o recurso deve corresponder à identidade do perfil.</span><span class="sxs-lookup"><span data-stu-id="6d236-115">On a compliant device, the identity accessing the resource should match the identity on the profile.</span></span>  <span data-ttu-id="6d236-116">Se isso não acontecer, você verá uma mensagem como a da próxima captura de tela.</span><span class="sxs-lookup"><span data-stu-id="6d236-116">If it doesn't, you'll see a message like the one in the next screenshot.</span></span> <span data-ttu-id="6d236-117">No exemplo de captura de tela, "testadmin@evostsoneboxtest.com" é a conta necessária para acessar o recurso.</span><span class="sxs-lookup"><span data-stu-id="6d236-117">In the screenshot example, "testadmin@evostsoneboxtest.com" is the sign-in account needed to access the resource.</span></span>

![Mensagem de acesso condicional no navegador](./media/edge-security/microsoft-edge-security-conditional-access.png)

<span data-ttu-id="6d236-119">Para continuar, você precisa alternar para o perfil necessário (se tiver um) ou criar um perfil com a identidade correspondente.</span><span class="sxs-lookup"><span data-stu-id="6d236-119">To continue, you have to switch to the required profile (if you have one) or create a profile with matching identity.</span></span>

<span data-ttu-id="6d236-120">Para entrar e trabalhar com seu perfil, clique na imagem da conta no canto superior direito do navegador.</span><span class="sxs-lookup"><span data-stu-id="6d236-120">To sign in and work with your profile, click the account picture in the top right corner of the browser.</span></span> <span data-ttu-id="6d236-121">É possível usar o menu suspendo para:</span><span class="sxs-lookup"><span data-stu-id="6d236-121">You can use the dropdown menu to:</span></span>

- <span data-ttu-id="6d236-122">Selecionar outro perfil.</span><span class="sxs-lookup"><span data-stu-id="6d236-122">Select another profile.</span></span> <span data-ttu-id="6d236-123">Clicar no nome do perfil.</span><span class="sxs-lookup"><span data-stu-id="6d236-123">Click the profile name.</span></span>
- <span data-ttu-id="6d236-124">Criar um perfil.</span><span class="sxs-lookup"><span data-stu-id="6d236-124">Create a profile.</span></span> <span data-ttu-id="6d236-125">Clique em **Adicionar um recurso**.</span><span class="sxs-lookup"><span data-stu-id="6d236-125">Click **Add a profile**.</span></span>
- <span data-ttu-id="6d236-126">Gerenciar seus perfis.</span><span class="sxs-lookup"><span data-stu-id="6d236-126">Manage your profiles.</span></span> <span data-ttu-id="6d236-127">Clique em **Gerenciar configurações de perfil**.</span><span class="sxs-lookup"><span data-stu-id="6d236-127">Click **Manage profile settings**.</span></span>

<span data-ttu-id="6d236-128">Esse suporte está disponível em todas as plataformas, incluindo todas as versões compatíveis do Windows e do macOS.</span><span class="sxs-lookup"><span data-stu-id="6d236-128">This support is available across all platforms, including all supported versions of Windows and macOS.</span></span>

### <a name="how-to-deploy-conditional-access-in-azure-active-directory"></a><span data-ttu-id="6d236-129">Como implantar o Acesso condicional no Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="6d236-129">How to deploy Conditional Access in Azure Active Directory</span></span>

<span data-ttu-id="6d236-130">[Implantar Acesso condicional](/azure/active-directory/conditional-access/plan-conditional-access) fornece um guia detalhado para ajudar a implantar o Acesso condicional no Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="6d236-130">[Deploy Conditional Access](/azure/active-directory/conditional-access/plan-conditional-access) provides a detailed guide to help deploy Conditional Access in Azure Active Directory.</span></span>

## <a name="see-also"></a><span data-ttu-id="6d236-131">Consulte também</span><span class="sxs-lookup"><span data-stu-id="6d236-131">See also</span></span>

- [<span data-ttu-id="6d236-132">Página de aterrissagem do Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="6d236-132">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="6d236-133">Vídeo: segurança, compatibilidade e gerenciabilidade</span><span class="sxs-lookup"><span data-stu-id="6d236-133">Video: Security, compatibility, and manageability</span></span>](/microsoft-edge-video-security-compatibility-manageability.md)