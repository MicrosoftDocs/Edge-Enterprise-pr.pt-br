---
title: Microsoft Edge e sites configuráveis no modo IE
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Microsoft Edge e sites configuráveis no modo IE
ms.openlocfilehash: 0248ecd394acee5773751c0685969e3d40940431
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/09/2021
ms.locfileid: "11641797"
---
# <a name="learn-about-configurable-sites-in-ie-mode"></a><span data-ttu-id="f7f32-103">Saiba mais sobre sites configuráveis no modo IE</span><span class="sxs-lookup"><span data-stu-id="f7f32-103">Learn about Configurable sites in IE mode</span></span>

<span data-ttu-id="f7f32-104">Este artigo explica o recurso de sites configuráveis na lista de sites do modo empresarial ao usar o modo IE no Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="f7f32-104">This article explains the Configurable sites feature of the Enterprise Mode Site List when using IE mode in Microsoft Edge.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="f7f32-105">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="f7f32-105">Prerequisites</span></span>

- <span data-ttu-id="f7f32-106">Atualizações do Windows</span><span class="sxs-lookup"><span data-stu-id="f7f32-106">Windows updates</span></span>

  - <span data-ttu-id="f7f32-107">Windows 10 versão 1909; Windows Server versão 1909 – KB4550945 ou posterior</span><span class="sxs-lookup"><span data-stu-id="f7f32-107">Windows 10 version 1909, Windows server version 1909 – KB4550945  or higher</span></span>
  - <span data-ttu-id="f7f32-108">Windows 10 versão 1903; Windows Server versão 1903 – KB4550945 ou posterior</span><span class="sxs-lookup"><span data-stu-id="f7f32-108">Windows 10 version 1903, Windows server version 1903 – KB4550945  or higher</span></span>
  - <span data-ttu-id="f7f32-109">Windows 10 versão 1809; Windows Server versão 1809; e Windows Server 2019 – KB4550969 ou posterior</span><span class="sxs-lookup"><span data-stu-id="f7f32-109">Windows 10 version 1809, Windows Server version 1809, and Windows Server 2019 - KB4550969 or higher</span></span>
  - <span data-ttu-id="f7f32-110">Windows 10 versão 1803 – KB4550944 ou superior</span><span class="sxs-lookup"><span data-stu-id="f7f32-110">Windows 10 version 1803 – KB4550944 or higher</span></span>
  - <span data-ttu-id="f7f32-111">Windows 10 versão 1607; Windows Server 2016 – KB4556826 ou superior</span><span class="sxs-lookup"><span data-stu-id="f7f32-111">Windows 10 version 1607, Windows Server 2016 - KB4556826 or higher</span></span>
  - <span data-ttu-id="f7f32-112">Versão inicial do Windows 10, julho de 2015 – KB4550947 ou superior</span><span class="sxs-lookup"><span data-stu-id="f7f32-112">Windows 10 initial version, July 2015 - KB4550947 or higher</span></span>
  - <span data-ttu-id="f7f32-113">Windows 8.1 – KB4556798 ou superior</span><span class="sxs-lookup"><span data-stu-id="f7f32-113">Windows 8.1 – KB4556798 or higher</span></span>

- <span data-ttu-id="f7f32-114">Microsoft Edge versão 83 ou posterior</span><span class="sxs-lookup"><span data-stu-id="f7f32-114">Microsoft Edge version 83 or later</span></span>
- <span data-ttu-id="f7f32-115">[Modo IE](./edge-ie-mode.md) configurado com a lista de sites do modo empresarial</span><span class="sxs-lookup"><span data-stu-id="f7f32-115">[IE mode](./edge-ie-mode.md) configured with Enterprise Mode Site List</span></span>

## <a name="overview"></a><span data-ttu-id="f7f32-116">Visão geral</span><span class="sxs-lookup"><span data-stu-id="f7f32-116">Overview</span></span>

<span data-ttu-id="f7f32-117">Configurar sites que precisam do modo IE na lista de sites do modo empresarial funcionará bem na maioria dos ambientes com aplicativos herdados.</span><span class="sxs-lookup"><span data-stu-id="f7f32-117">Configuring sites needing IE mode in the Enterprise Mode Site List will work well for most environments with legacy applications.</span></span> <span data-ttu-id="f7f32-118">No entanto, em alguns casos essa abordagem não é a melhor para configurar um subconjunto de sites para abrir no modo do IE sem processar um domínio inteiro no modo do IE.</span><span class="sxs-lookup"><span data-stu-id="f7f32-118">However, in some cases this approach isn't the best to configure a subset of sites to open in IE mode without rendering an entire domain in IE mode.</span></span> <span data-ttu-id="f7f32-119">Por exemplo, quando seu ambiente do contém aplicativos modernos e herdados sendo executados em um único servidor, e você gostaria de ter a flexibilidade para renderizar apenas os aplicativos herdados no modo IE e os aplicativos restantes para renderizar no modo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="f7f32-119">For example, when your environment contains both modern and legacy applications running on a single server and you would like the flexibility to render only the legacy applications in IE mode and the remaining applications to render in Microsoft Edge mode.</span></span>

<span data-ttu-id="f7f32-120">A solução é usar o recurso sites configuráveis da lista de sites do modo empresarial.</span><span class="sxs-lookup"><span data-stu-id="f7f32-120">The solution is to use the Configurable sites feature of the Enterprise Mode Site List.</span></span> <span data-ttu-id="f7f32-121">Quando o recurso está habilitado, o Microsoft Edge permite que os sites com a marca "configurada" participem da determinação do mecanismo do IE.</span><span class="sxs-lookup"><span data-stu-id="f7f32-121">When the feature is enabled, Microsoft Edge will allow sites with the "configurable" tag to participate in IE mode engine determination.</span></span>

## <a name="how-configurable-sites-works"></a><span data-ttu-id="f7f32-122">Como funcionam os sites configuráveis</span><span class="sxs-lookup"><span data-stu-id="f7f32-122">How Configurable sites works</span></span>

### <a name="automatic-switching-from-the-microsoft-edge-engine-to-the-ie-mode-engine"></a><span data-ttu-id="f7f32-123">Mudança automática do mecanismo no Microsoft Edge para o mecanismo no modo IE</span><span class="sxs-lookup"><span data-stu-id="f7f32-123">Automatic switching from the Microsoft Edge engine to the IE mode engine</span></span>

<span data-ttu-id="f7f32-124">Para usar o recurso sites configuráveis, você precisará de um ou mais sites na lista de sites do modo empresarial para ter a opção `<open-in>Configurable</open-in>`.</span><span class="sxs-lookup"><span data-stu-id="f7f32-124">To use the Configurable sites feature, you'll need one or more sites in the Enterprise Mode Site List to have the `<open-in>Configurable</open-in>` option.</span></span>

<span data-ttu-id="f7f32-125">Exemplo:</span><span class="sxs-lookup"><span data-stu-id="f7f32-125">Example:</span></span>

```
<site-list version="1">
  <site url="app.com">
    <open-in>Configurable</open-in>
  </site>
</site-list>
```

<span data-ttu-id="f7f32-126">Quando o recurso sites configuráveis estiver habilitado, ocorrerá o seguinte comportamento:</span><span class="sxs-lookup"><span data-stu-id="f7f32-126">When the Configurable sites feature is enabled, the following behavior occurs:</span></span>

1. <span data-ttu-id="f7f32-127">Ao fazer uma solicitação para um site configurável, o Microsoft Edge enviará o cabeçalho da solicitação HTTP "`X-InternetExplorerModeConfigurable: 1`".</span><span class="sxs-lookup"><span data-stu-id="f7f32-127">When making a request to a Configurable site, Microsoft Edge will send the HTTP request header "`X-InternetExplorerModeConfigurable: 1`".</span></span>
2. <span data-ttu-id="f7f32-128">Um site configurável pode enviar uma resposta de redirecionamento (por exemplo, HTTP 302) com o cabeçalho de resposta HTTP "`X-InternetExplorerMode: 1`" para solicitar que o Microsoft Edge carregue o site no modo IE.</span><span class="sxs-lookup"><span data-stu-id="f7f32-128">A Configurable site may send a redirect response (for example, HTTP 302) with the HTTP response header "`X-InternetExplorerMode: 1`" to request that Microsoft Edge loads the site in IE mode.</span></span>
3. <span data-ttu-id="f7f32-129">O destino do redirecionamento (ou seja, o valor do cabeçalho de resposta do Local) também deve ser um siteConfigurável ou **Neutro**, caso contrário, o cabeçalho de resposta do modo IE será ignorado.</span><span class="sxs-lookup"><span data-stu-id="f7f32-129">The target of the redirect (that is, the value of the **Location** response header) must also be a **Configurable** or **Neutral** site, otherwise the IE mode response header will be ignored.</span></span> <span data-ttu-id="f7f32-130">Espera-se que o destino do redirecionamento geralmente seja igual à URL original.</span><span class="sxs-lookup"><span data-stu-id="f7f32-130">It's expected that the target of the redirect will usually be the same as the original URL.</span></span> <span data-ttu-id="f7f32-131">No entanto, não precisa ser.</span><span class="sxs-lookup"><span data-stu-id="f7f32-131">However, it doesn't have to be.</span></span>

   > [!NOTE]
   > <span data-ttu-id="f7f32-132">A resposta de redirecionamento está sujeita ao cache de acordo com o comportamento de cache HTTP normal do Microsoft Edge para redirecionamentos.</span><span class="sxs-lookup"><span data-stu-id="f7f32-132">The redirect response is subject to caching according to Microsoft Edge's normal HTTP caching behavior for redirects.</span></span>

### <a name="switching-back-from-ie-mode-engine-to-microsoft-edge-engine"></a><span data-ttu-id="f7f32-133">Mudança de um mecanismo do modo IE para o mecanismo do modo Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="f7f32-133">Switching back from IE mode engine to Microsoft Edge engine</span></span>

<span data-ttu-id="f7f32-134">Habilitar os sites configuráveis no Microsoft Edge habilita automaticamente os seguintes comportamentos nas guias do modo IE:</span><span class="sxs-lookup"><span data-stu-id="f7f32-134">Enabling Configurable sites in Microsoft Edge automatically enables the following behaviors in IE mode tabs:</span></span>

1. <span data-ttu-id="f7f32-135">Ao fazer uma solicitação para um site configurável, as guias do modo IE enviarão o cabeçalho da solicitação HTTP "`X-InternetExplorerModeConfigurable: 1`", da mesma forma que as guias do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="f7f32-135">When making a request to a Configurable site, IE mode tabs will send the HTTP request header "`X-InternetExplorerModeConfigurable: 1`", the same as Microsoft Edge tabs.</span></span>
2. <span data-ttu-id="f7f32-136">Um site configurável poderá enviar uma resposta de redirecionamento (por exemplo, HTTP 302) com o cabeçalho de resposta HTTP "`X-InternetExplorerMode: 0`" para solicitar que o a navegação retorne ao modo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="f7f32-136">A Configurable site might send a redirect response (for example, HTTP 302) with the HTTP response header "`X-InternetExplorerMode: 0`" to request that the navigation switch back to Microsoft Edge mode.</span></span>
3. <span data-ttu-id="f7f32-137">O destino do redirecionamento (ou seja, o valor do cabeçalho de resposta do **Local**) também deve ser um site**Configurável** ou **Neutro**, caso contrário, o cabeçalho de resposta do modo IE será ignorado.</span><span class="sxs-lookup"><span data-stu-id="f7f32-137">The target of the redirect (that is, the value of the **Location** response header) must also be a **Configurable** or **Neutral** site, otherwise the IE mode response header will be ignored.</span></span> <span data-ttu-id="f7f32-138">Espera-se que o destino do redirecionamento geralmente seja igual à URL original.</span><span class="sxs-lookup"><span data-stu-id="f7f32-138">It's expected that the target of the redirect will usually be the same as the original URL.</span></span> <span data-ttu-id="f7f32-139">No entanto, não precisa ser.</span><span class="sxs-lookup"><span data-stu-id="f7f32-139">However, it doesn't have to be.</span></span>

   > [!NOTE]
   > <span data-ttu-id="f7f32-140">A resposta de redirecionamento está sujeita ao cache de acordo com o comportamento de cache HTTP normal do Microsoft Edge para redirecionamentos.</span><span class="sxs-lookup"><span data-stu-id="f7f32-140">The redirect response is subject to caching according to Microsoft Edge's normal HTTP caching behavior for redirects.</span></span>

> [!TIP]
> <span data-ttu-id="f7f32-141">Os dois mecanismos de navegador enviam o mesmo cabeçalho de solicitação "`X-InternetExplorerModeConfigurable: 1`" aos sites configuráveis.</span><span class="sxs-lookup"><span data-stu-id="f7f32-141">Both browser engines send the same "`X-InternetExplorerModeConfigurable: 1`" request header to Configurable sites.</span></span> <span data-ttu-id="f7f32-142">Você deve usar o cabeçalho da solicitação do agente do usuário para diferenciar as solicitações no modo Microsoft Edge versus no modo IE para evitar o redirecionamento quando o site estiver carregando no mecanismo correto.</span><span class="sxs-lookup"><span data-stu-id="f7f32-142">You should use the User-Agent request header to distinguish between requests from Microsoft Edge mode vs. IE mode to avoid redirecting when the site is already loading in the correct engine.</span></span>

## <a name="see-also"></a><span data-ttu-id="f7f32-143">Consulte também</span><span class="sxs-lookup"><span data-stu-id="f7f32-143">See also</span></span>

- [<span data-ttu-id="f7f32-144">Sobre o modo IE</span><span class="sxs-lookup"><span data-stu-id="f7f32-144">About IE mode</span></span>](./edge-ie-mode.md)
- [<span data-ttu-id="f7f32-145">Informações adicionais sobre o Modo Empresarial</span><span class="sxs-lookup"><span data-stu-id="f7f32-145">Additional Enterprise Mode information</span></span>](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
- [<span data-ttu-id="f7f32-146">Página de aterrissagem do Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="f7f32-146">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)