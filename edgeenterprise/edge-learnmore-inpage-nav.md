---
title: Manter a navegação na página no modo do Internet Explorer
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Manter a navegação na página no modo do Internet Explorer
ms.openlocfilehash: 20b18d121c3babfaacffd4a08316b25be714d95e
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/09/2021
ms.locfileid: "11641357"
---
# <a name="keep-in-page-navigation-in-internet-explorer-mode"></a><span data-ttu-id="bd7f0-103">Manter a navegação na página no modo do Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="bd7f0-103">Keep in-page navigation in Internet Explorer mode</span></span>

<span data-ttu-id="bd7f0-104">Você pode usar essa política como uma solução temporária para forçar toda a navegação na página de sites do modo do Internet Explorer (modo IE) para permanecer no modo do IE.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-104">You can use this policy as a temporary solution to force all in-page navigation from Internet Explorer mode (IE mode) sites to stay in IE mode.</span></span>

<span data-ttu-id="bd7f0-105">Uma navegação na página é iniciada a partir de um link, um script ou um formulário na página atual.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-105">An in-page navigation is started from a link, a script, or a form on the current page.</span></span> <span data-ttu-id="bd7f0-106">Também pode ser um redirecionamento do servidor de uma tentativa anterior de navegação na página.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-106">It can also be a server-side redirect of a previous in-page navigation attempt.</span></span> <span data-ttu-id="bd7f0-107">Por outro lado, um usuário pode iniciar uma navegação que não é “na página” e independente da página atual de várias maneiras, usando os controles do navegador.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-107">Conversely, a user can start a navigation that isn't in-page that's independent of the current page in several ways by using the browser controls.</span></span> <span data-ttu-id="bd7f0-108">Por exemplo, usando a barra de endereço, o botão voltar ou um link favorito.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-108">For example, using the address bar, the back button, or a favorite link.</span></span>

>[!NOTE]
><span data-ttu-id="bd7f0-109">Este artigo se aplica ao Microsoft Edge versão 81 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-109">This article applies to Microsoft Edge version 81 or later.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="bd7f0-110">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="bd7f0-110">Prerequisites</span></span>

<span data-ttu-id="bd7f0-111">As seguintes atualizações do Windows são necessárias para esta política:</span><span class="sxs-lookup"><span data-stu-id="bd7f0-111">The following Windows updates are required for this policy:</span></span>

- <span data-ttu-id="bd7f0-112">Windows 10 versão 1909 e 1903, Windows Server versão 1909 e 1903 ([KB4532695](https://support.microsoft.com/help/4532695))</span><span class="sxs-lookup"><span data-stu-id="bd7f0-112">Windows 10 version 1909 & 1903, Windows Server version 1909 & 1903  ([KB4532695](https://support.microsoft.com/help/4532695))</span></span>
- <span data-ttu-id="bd7f0-113">Windows 10 versão 1809, Windows Server versão 1809, Windows Server 2019 ([KB4534321](https://support.microsoft.com/help/4534321))</span><span class="sxs-lookup"><span data-stu-id="bd7f0-113">Windows 10 version 1809, Windows Server version 1809, Windows Server 2019 ([KB4534321](https://support.microsoft.com/help/4534321))</span></span>
- <span data-ttu-id="bd7f0-114">Windows 10 versão 1803 ([KB4534308](https://support.microsoft.com/help/4534308))</span><span class="sxs-lookup"><span data-stu-id="bd7f0-114">Windows 10 version 1803 ([KB4534308](https://support.microsoft.com/help/4534308))</span></span>
- <span data-ttu-id="bd7f0-115">Windows 10 versão 1709 ([KB4534318](https://support.microsoft.com/help/4534318))</span><span class="sxs-lookup"><span data-stu-id="bd7f0-115">Windows 10 version 1709 ([KB4534318](https://support.microsoft.com/help/4534318))</span></span>


## <a name="about-this-policy"></a><span data-ttu-id="bd7f0-116">Sobre essa política</span><span class="sxs-lookup"><span data-stu-id="bd7f0-116">About this policy</span></span>

<span data-ttu-id="bd7f0-117">Essa política oferece tempo para identificar e configurar todos os servidores de autenticação usados ​​pelos seus sites no modo IE.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-117">This policy gives you time to identify and configure all of the authentication servers used by your IE mode sites.</span></span> <span data-ttu-id="bd7f0-118">No entanto, essa política pode resultar em uma experiência de navegação inconsistente, na qual alguns sites são renderizados no modo IE e outras vezes renderizados no modo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-118">However, this policy can result in an inconsistent browsing experience, where some sites are rendered in IE mode and at other times rendered in Microsoft Edge mode.</span></span> <span data-ttu-id="bd7f0-119">Essa experiência depende se a navegação do site começou em uma página de modo do IE.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-119">This experience depends on whether the navigation to the site began from an IE mode page.</span></span> <span data-ttu-id="bd7f0-120">Qualquer site que não esteja explicitamente configurado para abrir em um mecanismo de renderização específico estará sujeito a essa inconsistência.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-120">Any site that isn't explicitly configured to open in a specific rendering engine will be subject to this inconsistency.</span></span>

<span data-ttu-id="bd7f0-121">Se você habilitar essa política, recomendamos que a desabilite depois de identificar todos os servidores de autenticação e adicioná-los à lista de sites como neutros.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-121">If you enable this policy, we recommend that you disable it after you've identified all the authentication servers and added them to the site list as neutral.</span></span> <span data-ttu-id="bd7f0-122">Isso garante que seus sites modernos nunca sejam renderizados inadvertidamente no modo do IE.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-122">This action ensures that your modern sites never inadvertently render in IE mode.</span></span>

## <a name="keep-in-page-navigation-in-ie-mode"></a><span data-ttu-id="bd7f0-123">Manter navegações na página no modo do IE</span><span class="sxs-lookup"><span data-stu-id="bd7f0-123">Keep in-page navigation in IE mode</span></span>

<span data-ttu-id="bd7f0-124">Para manter as navegações automáticas ou toda a navegação na página no modo Internet Explorer, siga estas etapas:</span><span class="sxs-lookup"><span data-stu-id="bd7f0-124">To keep automatic or all in-page navigation in Internet Explorer mode, follow these steps:</span></span>

1. <span data-ttu-id="bd7f0-125">Abra o Editor de política de grupo local.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-125">Open Local Group Policy Editor.</span></span>
2. <span data-ttu-id="bd7f0-126">Clique em **Configuração do Computador** > **Modelos Administrativos** > **Microsoft Edge**.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-126">Click **Computer Configuration** > **Administrative Templates** > **Microsoft Edge**.</span></span>
3. <span data-ttu-id="bd7f0-127">Em **Configuração**, clique duas vezes em **Especificar como as navegações "na página" para sites não configurados se comportam quando iniciadas nas páginas do modo Internet Explorer**.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-127">Under **Setting**, double-click **Specify how "in-page" navigations to unconfigured sites behave when started from Internet Explorer mode pages**.</span></span>

   ![Configuração de política na página](media/edge-learnmore-inpage-nav/learnmore-in-page-nav-settings.png)

4. <span data-ttu-id="bd7f0-129">Selecione **Habilitado**</span><span class="sxs-lookup"><span data-stu-id="bd7f0-129">Select **Enabled**</span></span> 

   ![Habilitar política na página](media/edge-learnmore-inpage-nav/learnmore-in-page-nav-enable.png)

5. <span data-ttu-id="bd7f0-131">Escolha uma das opções a seguir na lista suspensa:</span><span class="sxs-lookup"><span data-stu-id="bd7f0-131">Choose one of the following options from the dropdown list:</span></span>

   - <span data-ttu-id="bd7f0-132">**Padrão** - Apenas sites configurados para abrir no modo Internet Explorer serão abertos nesse modo.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-132">**Default** - Only sites configured to open in Internet Explorer mode will open in that mode.</span></span> <span data-ttu-id="bd7f0-133">Qualquer site não configurado para abrir no modo Internet Explorer será redirecionado de volta ao Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-133">Any site not configured to open in Internet Explorer mode will be redirected back to Microsoft Edge.</span></span>
   - <span data-ttu-id="bd7f0-134">**Manter apenas navegações automáticas no modo Internet Explorer** - Use essa opção se desejar a experiência padrão, exceto que todas as navegações automáticas (como redirecionamentos 302) para sites não configurados serão mantidas no modo Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-134">**Keep only automatic navigations in Internet Explorer mode** - Use this option if you want the default experience except that all automatic navigations (such as 302 redirects) to unconfigured sites will be kept in Internet Explorer mode.</span></span>
   - <span data-ttu-id="bd7f0-135">**Manter toda a navegação na página no modo Internet Explorer**  \* *_(Menos Recomendado)_*_ - Todas as navegação de páginas carregadas no modo IE para sites não configurados são mantidas no modo Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-135">**Keep all in-page navigation in Internet Explorer mode** \**_(Least Recommended)_*_ - All navigations from pages loaded in IE mode to unconfigured sites are kept in Internet Explorer mode.</span></span>

6. <span data-ttu-id="bd7f0-136">Clique em _*OK*\* **ou Aplicar** para salvar as configurações de política.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-136">Click _*OK*\* or **Apply** to save the policy settings.</span></span>

## <a name="see-also"></a><span data-ttu-id="bd7f0-137">Consulte também</span><span class="sxs-lookup"><span data-stu-id="bd7f0-137">See also</span></span>

- [<span data-ttu-id="bd7f0-138">Página de aterrissagem do Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="bd7f0-138">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
