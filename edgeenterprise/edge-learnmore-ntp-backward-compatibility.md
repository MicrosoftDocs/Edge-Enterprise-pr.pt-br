---
title: Compatibilidade com versões anteriores para a página Nova guia da empresa
ms.author: ruchir
author: dan-wesley
manager: vwehren
ms.date: 10/28/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Compatibilidade com versões anteriores para a página Nova guia da empresa
ms.openlocfilehash: 5721db16c634250b3a586f6bd1b6b531a07815a5
ms.sourcegitcommit: f363ceb6c42054fabc95ce8d7bca3c52d80e6a9f
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/24/2021
ms.locfileid: "11447255"
---
# <a name="backwards-compatibility-for-the-enterprise-new-tab-page"></a><span data-ttu-id="5b534-103">Compatibilidade com versões anteriores para a página Nova guia da empresa</span><span class="sxs-lookup"><span data-stu-id="5b534-103">Backwards compatibility for the Enterprise New tab page</span></span>

<span data-ttu-id="5b534-104">Este artigo descreve a mudança para a página da Nova guia e como os usuários podem ser compatíveis com versões anteriores do Microsoft Edge, versão 87 e anterior.</span><span class="sxs-lookup"><span data-stu-id="5b534-104">This article describes the change to the New tab page and how users can be backwards compatible with Microsoft Edge version 87 and earlier.</span></span>

> [!NOTE]
> <span data-ttu-id="5b534-105">Este artigo se aplica ao Microsoft Edge versão 87 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="5b534-105">This article applies to Microsoft Edge version 87 or later.</span></span>

## <a name="information-feeds-from-single-endpoint"></a><span data-ttu-id="5b534-106">Feeds de informações do ponto de extremidade único</span><span class="sxs-lookup"><span data-stu-id="5b534-106">Information feeds from single endpoint</span></span>

<span data-ttu-id="5b534-107">A nova versão da página Nova guia da Empresa combina conteúdo compatível do Microsoft 365 com feeds de informações relevantes e em conformidade com o setor que são servidos pelo ponto de extremidade MSN.com.</span><span class="sxs-lookup"><span data-stu-id="5b534-107">The new version of the Enterprise New tab page combines compliant Microsoft 365 content with industry relevant and compliant information feeds that are served via the MSN.com endpoint.</span></span>

> [!NOTE]
> <span data-ttu-id="5b534-108">O conteúdo do Office 365 foi originalmente servido usando o domínio [Office.com](https://www.office.com).</span><span class="sxs-lookup"><span data-stu-id="5b534-108">Office 365 content was originally served using the [Office.com](https://www.office.com) domain.</span></span>

<span data-ttu-id="5b534-109">Se o acesso ao domínio MSN.com for restrito à sua organização, é altamente recomendável conceder aos usuários acesso a esse [URL](https://ntp.msn.com).</span><span class="sxs-lookup"><span data-stu-id="5b534-109">If access to the MSN.com domain is restricted for your organization, we strongly recommend giving users access to this [url](https://ntp.msn.com).</span></span>

<span data-ttu-id="5b534-110">Se precisar de mais tempo para habilitar o acesso ao domínio do MSN, recomendamos usar o [NewTabPageSetFeedType](./microsoft-edge-policies.md#newtabpagesetfeedtype), que permite que você escolha a experiência do Microsoft News ou o feed do Office 365 para a página Nova guia.</span><span class="sxs-lookup"><span data-stu-id="5b534-110">If you need more time to enable access to the MSN domain, we recommend using the [NewTabPageSetFeedType](./microsoft-edge-policies.md#newtabpagesetfeedtype), that lets you choose either the Microsoft News or Office 365 feed experience for the new tab page.</span></span>

### <a name="keep-using-officecom"></a><span data-ttu-id="5b534-111">Continuar usando o Office.com</span><span class="sxs-lookup"><span data-stu-id="5b534-111">Keep using Office.com</span></span>

 <span data-ttu-id="5b534-112">Você pode configurar a política **NewTabPageSetFeedType** para continuar usando o domínio substituído do Office.com.</span><span class="sxs-lookup"><span data-stu-id="5b534-112">You can configure the **NewTabPageSetFeedType** policy to keep using the deprecated Office.com domain.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5b534-113">A política **NewTabPageSetFeedType** e o domínio Office.com que atendem ao conteúdo do Office 365 deixarão de funcionar quando a versão 90 do Microsoft Edge for lançada.</span><span class="sxs-lookup"><span data-stu-id="5b534-113">The **NewTabPageSetFeedType** policy and the Office.com domain that serves Office 365 content will quit working when Microsoft Edge version 90 is released.</span></span>

<span data-ttu-id="5b534-114">As configurações de política a seguir forçarão a Nova guia empresarial a converter o conteúdo de documentos do Office a partir do domínio Office.com.</span><span class="sxs-lookup"><span data-stu-id="5b534-114">The following policy settings will force the Enterprise New tab page to render Office document content from the Office.com domain.</span></span>

- <span data-ttu-id="5b534-115">Defina a política como **Obrigatória**.</span><span class="sxs-lookup"><span data-stu-id="5b534-115">Set the policy as **Mandatory**.</span></span>
- <span data-ttu-id="5b534-116">Defina o valor do mapeamento de política para **Office (1) = experiência de feed do Office 365**.</span><span class="sxs-lookup"><span data-stu-id="5b534-116">Set the value of the policy mapping to **Office (1) = Office 365 feed experience**.</span></span>

<span data-ttu-id="5b534-117">Se não for possível migrar para o Office.com, envie-nos seus comentários.</span><span class="sxs-lookup"><span data-stu-id="5b534-117">If the switch to the Office.com isn't possible, reach out and send us feedback.</span></span> <span data-ttu-id="5b534-118">Outra opção é definir o [NewTabPageLocation](./microsoft-edge-policies.md#newtabpagelocation) para que ele aponte para uma URL de ponto de extremidade permitida pela sua organização.</span><span class="sxs-lookup"><span data-stu-id="5b534-118">Another option is to configure the [NewTabPageLocation](./microsoft-edge-policies.md#newtabpagelocation) so it points to an endpoint URL that's allowed by your organization.</span></span>

> [!NOTE]
> <span data-ttu-id="5b534-119">A política **NewTabPageLocation** tem precedência se a política **NewTabPageSetFeedType** também estiver configurada.</span><span class="sxs-lookup"><span data-stu-id="5b534-119">The **NewTabPageLocation** policy has precedence if the **NewTabPageSetFeedType** policy is also configured.</span></span>

## <a name="enterprise-users-will-now-get-microsoft-news-content-via-my-feed"></a><span data-ttu-id="5b534-120">Os usuários corporativos receberão o conteúdo de notícias da Microsoft por meio do Meu Feed</span><span class="sxs-lookup"><span data-stu-id="5b534-120">Enterprise users will now get Microsoft news content via My Feed</span></span>

<span data-ttu-id="5b534-121">A página de Nova guia da empresa oferecerá informações relevantes do setor no **Meus feed** e o conteúdo do Office 365 em um único modo de exibição para os usuários que se conectam a uma conta do Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="5b534-121">The Enterprise New tab page will offer industry relevant information in **My Feed** and Office 365 content in a single view for users signed in with their Azure Active Directory (Azure AD) account.</span></span> <span data-ttu-id="5b534-122">Para os usuários que entrarem com o Azure Active Directory (Azure AD) que selecionarem a opção Microsoft Notícias no submenu configurações, seu novo modo de exibição de página de guia será substituído com conteúdo**Meu feed**.</span><span class="sxs-lookup"><span data-stu-id="5b534-122">For users signed in with their Azure Active Directory (Azure AD) who selected the Microsoft News option in the settings flyout, their new tab page view will be replaced with **My Feed** content.</span></span> <span data-ttu-id="5b534-123">Ao abrir uma nova página da guia no navegador, ele terá a seguinte aparência como o exemplo da captura de tela a seguir.</span><span class="sxs-lookup"><span data-stu-id="5b534-123">When they open a new tab page in the browser it will look like the example in the next screenshot.</span></span>

![Nova guia mostrando o conteúdo do Meu feed.](media/microsoft-edge-ntp-backward-compatibility/microsoft-edge-ntp-myfeed-view.png)

> [!NOTE]
> <span data-ttu-id="5b534-125">Os usuários que não entrarem com o Azure AD ainda poderão ver o feed de notícias do MSN quando abrirem uma Nova guia.</span><span class="sxs-lookup"><span data-stu-id="5b534-125">Users who aren't signed in with Azure AD will continue to see the MSN News feed when they open a new tab.</span></span>

## <a name="page-layout"></a><span data-ttu-id="5b534-126">Layout de página</span><span class="sxs-lookup"><span data-stu-id="5b534-126">Page layout</span></span>

<span data-ttu-id="5b534-127">Com as alterações na página Nova guia, o layout da página não tem mais que controlar dois tipos de conteúdo específicos (Office 365 e Microsoft Notícias), portanto, a opção de conteúdo não está disponível.</span><span class="sxs-lookup"><span data-stu-id="5b534-127">With the changes to the New tab page, the Page layout no longer has to control two specific content types (Office 365 and Microsoft News), so the content toggle isn't available.</span></span> <span data-ttu-id="5b534-128">A próxima captura de tela mostra o submenu do layout da página.</span><span class="sxs-lookup"><span data-stu-id="5b534-128">The next screenshot shows the flyout for the Page layout.</span></span>

![Modo de exibição do layout para a página Nova guia.](media/microsoft-edge-ntp-backward-compatibility/microsoft-edge-ntp-page-layout.png)

<span data-ttu-id="5b534-130">Caso pretenda manter o acesso ao conteúdo do Microsoft Notícias que não esteja associado à sua organização, você deve usar um perfil diferente do navegador.</span><span class="sxs-lookup"><span data-stu-id="5b534-130">If you want to keep accessing Microsoft News content that isn't tied to your organization, you must use a different browser profile.</span></span> <span data-ttu-id="5b534-131">Vá para  *edge://settings/profiles* e saia do seu perfil do Azure AD.</span><span class="sxs-lookup"><span data-stu-id="5b534-131">Go to  *edge://settings/profiles* and sign out of your Azure AD profile.</span></span> <span data-ttu-id="5b534-132">Essa ação exibirá o modo de exibição padrão para a página de Nova guia da empresa.</span><span class="sxs-lookup"><span data-stu-id="5b534-132">This action will bring up the  standard view for the Enterprise new tab page.</span></span> 

## <a name="see-also"></a><span data-ttu-id="5b534-133">Consulte também</span><span class="sxs-lookup"><span data-stu-id="5b534-133">See also</span></span>

- [<span data-ttu-id="5b534-134">Página de aterrissagem do Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="5b534-134">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="5b534-135">Modo Empresarial do Internet Explorer 11</span><span class="sxs-lookup"><span data-stu-id="5b534-135">Enterprise Mode for Internet Explorer 11</span></span>](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)