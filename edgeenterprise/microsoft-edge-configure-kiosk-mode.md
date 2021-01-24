---
title: Configurar o modo de quiosque do Microsoft Edge
ms.author: aguta
author: aguta
manager: srugh
ms.date: 01/21/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Configurar o modo de quiosque do Microsoft Edge
ms.openlocfilehash: be353a0e13e9234de40296a2e8dcc31b1b800f52
ms.sourcegitcommit: 8a88fd38bdb5e132e89bf17dd2b5fb72f5d1b4b9
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/22/2021
ms.locfileid: "11297467"
---
# <span data-ttu-id="3d4ef-103">Configurar o modo de quiosque do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="3d4ef-103">Configure Microsoft Edge kiosk mode</span></span>

<span data-ttu-id="3d4ef-104">Este artigo descreve como configurar as opções do modo de quiosque do Microsoft Edge que você pode realizar no piloto.</span><span class="sxs-lookup"><span data-stu-id="3d4ef-104">This article describes how to configure Microsoft Edge kiosk mode options that you can pilot.</span></span> <span data-ttu-id="3d4ef-105">Há também um roteiro de recursos que estamos planejando.</span><span class="sxs-lookup"><span data-stu-id="3d4ef-105">There's also a roadmap of features we're targeting.</span></span>

> [!NOTE]
> <span data-ttu-id="3d4ef-106">Este artigo se aplica ao Microsoft Edge versão 87 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="3d4ef-106">This article applies to Microsoft Edge version 87 or later.</span></span>

## <span data-ttu-id="3d4ef-107">Visão geral</span><span class="sxs-lookup"><span data-stu-id="3d4ef-107">Overview</span></span>

<span data-ttu-id="3d4ef-108">O modo de quiosque do Microsoft Edge oferece duas experiências de bloqueio do navegador, para que as organizações possam criar, gerenciar e oferecer a melhor experiência para seus clientes.</span><span class="sxs-lookup"><span data-stu-id="3d4ef-108">Microsoft Edge kiosk mode offers two lockdown experiences of the browser so organizations can create, manage, and provide the best experience for their customers.</span></span> <span data-ttu-id="3d4ef-109">As seguintes experiências de bloqueio estão disponíveis:</span><span class="sxs-lookup"><span data-stu-id="3d4ef-109">The following lockdown experiences are available:</span></span>  

- <span data-ttu-id="3d4ef-110">Experiência de **Sinalização Digital/Interativa**: exibe um site específico no modo de tela inteira.</span><span class="sxs-lookup"><span data-stu-id="3d4ef-110">**Digital/Interactive Signage** experience - Displays a specific site in full-screen mode.</span></span>
- <span data-ttu-id="3d4ef-111">Experiência de **Navegação Pública**: executa uma versão de várias guias no Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="3d4ef-111">**Public-Browsing** experience - Runs a limited multi-tab version of Microsoft Edge.</span></span>

<span data-ttu-id="3d4ef-112">As duas experiências estão executando uma sessão InPrivate do Microsoft Edge, que protege os dados do usuário.</span><span class="sxs-lookup"><span data-stu-id="3d4ef-112">Both experiences are running a Microsoft Edge InPrivate session, which protects user data.</span></span>

## <span data-ttu-id="3d4ef-113">Configurar o modo de quiosque do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="3d4ef-113">Set up Microsoft Edge kiosk mode</span></span>

<span data-ttu-id="3d4ef-114">Um conjunto inicial de recursos de modo de quiosque já está disponível para teste com o Canal Estável do Microsoft Edge, versão 87.</span><span class="sxs-lookup"><span data-stu-id="3d4ef-114">An initial set of kiosk mode features is available to test with Microsoft Edge Stable Channel, version 87.</span></span> <span data-ttu-id="3d4ef-115">Você pode baixar a versão mais recente do [Microsoft Edge (Canal Estável Oficial)](https://www.microsoft.com/edge).</span><span class="sxs-lookup"><span data-stu-id="3d4ef-115">You can download the latest version from [Microsoft Edge (Official Stable Channel)](https://www.microsoft.com/edge).</span></span>

### <span data-ttu-id="3d4ef-116">Recursos com suporte no modo quiosque</span><span class="sxs-lookup"><span data-stu-id="3d4ef-116">Kiosk mode supported features</span></span>

<span data-ttu-id="3d4ef-117">A tabela a seguir lista os recursos com suporte no modo quiosque.</span><span class="sxs-lookup"><span data-stu-id="3d4ef-117">The following table lists the features supported by kiosk mode.</span></span>

|<span data-ttu-id="3d4ef-118">Recurso</span><span class="sxs-lookup"><span data-stu-id="3d4ef-118">Feature</span></span>|<span data-ttu-id="3d4ef-119">Sinalização Interativa/Digital</span><span class="sxs-lookup"><span data-stu-id="3d4ef-119">Digital\Interactive Signage</span></span>|<span data-ttu-id="3d4ef-120">Navegação pública</span><span class="sxs-lookup"><span data-stu-id="3d4ef-120">Public browsing</span></span>|<span data-ttu-id="3d4ef-121">Disponível com a versão do Microsoft Edge (e superior)</span><span class="sxs-lookup"><span data-stu-id="3d4ef-121">Available with Microsoft Edge version (and higher)</span></span>|
|-|-|-|-|
|<span data-ttu-id="3d4ef-122">Navegação InPrivate.</span><span class="sxs-lookup"><span data-stu-id="3d4ef-122">InPrivate Navigation</span></span>|<span data-ttu-id="3d4ef-123">S</span><span class="sxs-lookup"><span data-stu-id="3d4ef-123">Y</span></span>|<span data-ttu-id="3d4ef-124">S</span><span class="sxs-lookup"><span data-stu-id="3d4ef-124">Y</span></span>|<span data-ttu-id="3d4ef-125">87</span><span class="sxs-lookup"><span data-stu-id="3d4ef-125">87</span></span>|
|<span data-ttu-id="3d4ef-126">Redefinir em inatividade</span><span class="sxs-lookup"><span data-stu-id="3d4ef-126">Reset on inactivity</span></span>|<span data-ttu-id="3d4ef-127">S</span><span class="sxs-lookup"><span data-stu-id="3d4ef-127">Y</span></span>|<span data-ttu-id="3d4ef-128">S</span><span class="sxs-lookup"><span data-stu-id="3d4ef-128">Y</span></span>|<span data-ttu-id="3d4ef-129">87</span><span class="sxs-lookup"><span data-stu-id="3d4ef-129">87</span></span>|
|<span data-ttu-id="3d4ef-130">[Barra de endereços somente leitura](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#kioskaddressbareditingenabled) (política)</span><span class="sxs-lookup"><span data-stu-id="3d4ef-130">[Read only address bar](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#kioskaddressbareditingenabled) (policy)</span></span> |<span data-ttu-id="3d4ef-131">N</span><span class="sxs-lookup"><span data-stu-id="3d4ef-131">N</span></span>|<span data-ttu-id="3d4ef-132">S</span><span class="sxs-lookup"><span data-stu-id="3d4ef-132">Y</span></span> |<span data-ttu-id="3d4ef-133">87</span><span class="sxs-lookup"><span data-stu-id="3d4ef-133">87</span></span>|
|<span data-ttu-id="3d4ef-134">[Excluir downloads na saída](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#kioskdeletedownloadsonexit) (política)</span><span class="sxs-lookup"><span data-stu-id="3d4ef-134">[Delete downloads on exit](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#kioskdeletedownloadsonexit) (policy)</span></span>  | <span data-ttu-id="3d4ef-135">S</span><span class="sxs-lookup"><span data-stu-id="3d4ef-135">Y</span></span>|<span data-ttu-id="3d4ef-136">S</span><span class="sxs-lookup"><span data-stu-id="3d4ef-136">Y</span></span> |<span data-ttu-id="3d4ef-137">87</span><span class="sxs-lookup"><span data-stu-id="3d4ef-137">87</span></span>|
|<span data-ttu-id="3d4ef-138">F11 bloqueado (entrar/sair de tela inteira)</span><span class="sxs-lookup"><span data-stu-id="3d4ef-138">F11 blocked (enter/exit full-screen)</span></span> | <span data-ttu-id="3d4ef-139">S</span><span class="sxs-lookup"><span data-stu-id="3d4ef-139">Y</span></span> | <span data-ttu-id="3d4ef-140">S</span><span class="sxs-lookup"><span data-stu-id="3d4ef-140">Y</span></span> | <span data-ttu-id="3d4ef-141">87</span><span class="sxs-lookup"><span data-stu-id="3d4ef-141">87</span></span> |
|<span data-ttu-id="3d4ef-142">F12 bloqueado (iniciar Ferramentas do Desenvolvedor)</span><span class="sxs-lookup"><span data-stu-id="3d4ef-142">F12 blocked (launch Developer Tools)</span></span> | <span data-ttu-id="3d4ef-143">S</span><span class="sxs-lookup"><span data-stu-id="3d4ef-143">Y</span></span> | <span data-ttu-id="3d4ef-144">S</span><span class="sxs-lookup"><span data-stu-id="3d4ef-144">Y</span></span> | <span data-ttu-id="3d4ef-145">87</span><span class="sxs-lookup"><span data-stu-id="3d4ef-145">87</span></span> |
| <span data-ttu-id="3d4ef-146">Suporte a várias guias</span><span class="sxs-lookup"><span data-stu-id="3d4ef-146">Multi tab support</span></span> | <span data-ttu-id="3d4ef-147">N</span><span class="sxs-lookup"><span data-stu-id="3d4ef-147">N</span></span>| <span data-ttu-id="3d4ef-148">S</span><span class="sxs-lookup"><span data-stu-id="3d4ef-148">Y</span></span>| <span data-ttu-id="3d4ef-149">87</span><span class="sxs-lookup"><span data-stu-id="3d4ef-149">87</span></span>|
|<span data-ttu-id="3d4ef-150">Botão encerrar sessão</span><span class="sxs-lookup"><span data-stu-id="3d4ef-150">End session button</span></span> | <span data-ttu-id="3d4ef-151">N</span><span class="sxs-lookup"><span data-stu-id="3d4ef-151">N</span></span>| <span data-ttu-id="3d4ef-152">S</span><span class="sxs-lookup"><span data-stu-id="3d4ef-152">Y</span></span>| <span data-ttu-id="3d4ef-153">88</span><span class="sxs-lookup"><span data-stu-id="3d4ef-153">88</span></span>|
|<span data-ttu-id="3d4ef-154">Todas as URLs internas do Microsoft Edge estão bloqueadas, exceto *edge://downloads* e *edge://print*</span><span class="sxs-lookup"><span data-stu-id="3d4ef-154">All internal Microsoft Edge URLs are blocked, except for *edge://downloads* and *edge://print*</span></span> |<span data-ttu-id="3d4ef-155">N</span><span class="sxs-lookup"><span data-stu-id="3d4ef-155">N</span></span>|<span data-ttu-id="3d4ef-156">S</span><span class="sxs-lookup"><span data-stu-id="3d4ef-156">Y</span></span>|<span data-ttu-id="3d4ef-157">88</span><span class="sxs-lookup"><span data-stu-id="3d4ef-157">88</span></span>|
| <span data-ttu-id="3d4ef-158">Ctrl+N bloqueado (abrir uma nova janela)</span><span class="sxs-lookup"><span data-stu-id="3d4ef-158">CTRL+N blocked (open a new window)</span></span> | <span data-ttu-id="3d4ef-159">S</span><span class="sxs-lookup"><span data-stu-id="3d4ef-159">Y</span></span> | <span data-ttu-id="3d4ef-160">S</span><span class="sxs-lookup"><span data-stu-id="3d4ef-160">Y</span></span> | <span data-ttu-id="3d4ef-161">89</span><span class="sxs-lookup"><span data-stu-id="3d4ef-161">89</span></span> |
| <span data-ttu-id="3d4ef-162">Ctrl+T bloqueado (abrir nova guia)</span><span class="sxs-lookup"><span data-stu-id="3d4ef-162">CTRL+T blocked (open new tab)</span></span> | <span data-ttu-id="3d4ef-163">N</span><span class="sxs-lookup"><span data-stu-id="3d4ef-163">N</span></span> | <span data-ttu-id="3d4ef-164">S</span><span class="sxs-lookup"><span data-stu-id="3d4ef-164">Y</span></span> | <span data-ttu-id="3d4ef-165">89</span><span class="sxs-lookup"><span data-stu-id="3d4ef-165">89</span></span> |
|<span data-ttu-id="3d4ef-166">Configurações e mais (...) exibirá somente as opções necessárias</span><span class="sxs-lookup"><span data-stu-id="3d4ef-166">Settings and more (...) will display only the required options</span></span>  |<span data-ttu-id="3d4ef-167">N</span><span class="sxs-lookup"><span data-stu-id="3d4ef-167">N</span></span> |<span data-ttu-id="3d4ef-168">S</span><span class="sxs-lookup"><span data-stu-id="3d4ef-168">Y</span></span> |<span data-ttu-id="3d4ef-169">89</span><span class="sxs-lookup"><span data-stu-id="3d4ef-169">89</span></span> |

> [!NOTE]
> <span data-ttu-id="3d4ef-170">À medida que o modo de quiosque evolui, mais recursos estarão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="3d4ef-170">As kiosk mode evolves, more features will be available.</span></span>

## <span data-ttu-id="3d4ef-171">Usar recursos do modo de quiosque</span><span class="sxs-lookup"><span data-stu-id="3d4ef-171">Use kiosk mode features</span></span>

<span data-ttu-id="3d4ef-172">Você pode invocar os recursos do modo de quiosque do Microsoft Edge com as seguintes opções de linha de comando do Windows 10:</span><span class="sxs-lookup"><span data-stu-id="3d4ef-172">Microsoft Edge kiosk mode features can be invoked with the following Windows 10 command line options:</span></span>

- <span data-ttu-id="3d4ef-173">Sinalização Interativa/Digital do modo de quiosque:</span><span class="sxs-lookup"><span data-stu-id="3d4ef-173">Kiosk mode Digital/Interactive signage:</span></span> `msedge.exe --kiosk www.contoso.com --edge-kiosk-type=fullscreen`
- <span data-ttu-id="3d4ef-174">Navegação pública modo de quiosque:</span><span class="sxs-lookup"><span data-stu-id="3d4ef-174">Kiosk mode public browsing:</span></span> `msedge.exe --kiosk www.contoso.com --edge-kiosk-type=public-browsing`

### <span data-ttu-id="3d4ef-175">Opções de linha de comando adicionais</span><span class="sxs-lookup"><span data-stu-id="3d4ef-175">Additional command line options</span></span>

- `--no-first-run` <span data-ttu-id="3d4ef-176">: Desabilite a primeira experiência de execução do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="3d4ef-176">: Disable the first Microsoft Edge run experience.</span></span>
- `--kiosk-idle-timeout-minutes` <span data-ttu-id="3d4ef-177">: Altere o tempo (em minutos) da última atividade de usuário antes que o modo de quiosque do Microsoft Edge redefina a sessão do usuário.</span><span class="sxs-lookup"><span data-stu-id="3d4ef-177">: Change the time (in minutes) from the last user activity before Microsoft Edge kiosk mode resets the user's session.</span></span> <span data-ttu-id="3d4ef-178">Os seguintes valores são válidos:</span><span class="sxs-lookup"><span data-stu-id="3d4ef-178">The following values are supported:</span></span>

  - <span data-ttu-id="3d4ef-179">Valores padrão</span><span class="sxs-lookup"><span data-stu-id="3d4ef-179">Default values</span></span>
    - <span data-ttu-id="3d4ef-180">Tela cheia - desativado</span><span class="sxs-lookup"><span data-stu-id="3d4ef-180">Full screen - turned off</span></span>
    - <span data-ttu-id="3d4ef-181">Navegação pública - 5 minutos</span><span class="sxs-lookup"><span data-stu-id="3d4ef-181">Public browsing - 5 minutes</span></span>
  - <span data-ttu-id="3d4ef-182">Valores permitidos</span><span class="sxs-lookup"><span data-stu-id="3d4ef-182">Allowed values</span></span>
    - <span data-ttu-id="3d4ef-183">0 - desativa o cronômetro</span><span class="sxs-lookup"><span data-stu-id="3d4ef-183">0 - turns off the timer</span></span>
    - <span data-ttu-id="3d4ef-184">1-1440 minutos para redefinição no timer de ociosidade</span><span class="sxs-lookup"><span data-stu-id="3d4ef-184">1-1440 minutes for reset on idle timer</span></span>

## <span data-ttu-id="3d4ef-185">Políticas suportadas no modo de quiosque</span><span class="sxs-lookup"><span data-stu-id="3d4ef-185">Support policies for kiosk mode</span></span>

<span data-ttu-id="3d4ef-186">Use qualquer uma das políticas do Microsoft Edge listadas na tabela a seguir para aprimorar a experiência de quiosque para o tipo de quiosque do Microsoft Edge que você configurar.</span><span class="sxs-lookup"><span data-stu-id="3d4ef-186">Use any of the Microsoft Edge policies listed in the following table to enhance the kiosk experience for the Microsoft Edge kiosk mode type you configure.</span></span> <span data-ttu-id="3d4ef-187">Para saber mais sobre essas políticas, consulte [Microsoft Edge – Referência de política do browser](https://docs.microsoft.com/deployedge/microsoft-edge-policies).</span><span class="sxs-lookup"><span data-stu-id="3d4ef-187">To learn more about these policies, see [Microsoft Edge – Browser policy reference](https://docs.microsoft.com/deployedge/microsoft-edge-policies).</span></span>

> [!NOTE]
> <span data-ttu-id="3d4ef-188">A configuração da política não está limitada às políticas listadas na tabela a seguir. No entanto, políticas adicionais devem ser testadas para garantir que a funcionalidade do modo quiosque não seja afetada negativamente.</span><span class="sxs-lookup"><span data-stu-id="3d4ef-188">Policy configuration isn't limited to the policies listed in the following table, however additional policies should be tested to ensure that kiosk mode functionality isn't negatively affected.</span></span>

|<span data-ttu-id="3d4ef-189">Política de grupo</span><span class="sxs-lookup"><span data-stu-id="3d4ef-189">Group policy</span></span>|<span data-ttu-id="3d4ef-190">Sinalização Interativa/Digital</span><span class="sxs-lookup"><span data-stu-id="3d4ef-190">Digital\Interactive signage</span></span>|<span data-ttu-id="3d4ef-191">Navegação pública em um aplicativo</span><span class="sxs-lookup"><span data-stu-id="3d4ef-191">Public browsing single-app</span></span>|
|--|--|--|
|[<span data-ttu-id="3d4ef-192">Impressão</span><span class="sxs-lookup"><span data-stu-id="3d4ef-192">Printing</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#printing-policies) | <span data-ttu-id="3d4ef-193">S</span><span class="sxs-lookup"><span data-stu-id="3d4ef-193">Y</span></span>|<span data-ttu-id="3d4ef-194">S</span><span class="sxs-lookup"><span data-stu-id="3d4ef-194">Y</span></span> |
|[<span data-ttu-id="3d4ef-195">HomePageLocation</span><span class="sxs-lookup"><span data-stu-id="3d4ef-195">HomePageLocation</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#homepagelocation) |<span data-ttu-id="3d4ef-196">N</span><span class="sxs-lookup"><span data-stu-id="3d4ef-196">N</span></span> | <span data-ttu-id="3d4ef-197">S</span><span class="sxs-lookup"><span data-stu-id="3d4ef-197">Y</span></span>|
|[<span data-ttu-id="3d4ef-198">ShowHomeButton</span><span class="sxs-lookup"><span data-stu-id="3d4ef-198">ShowHomeButton</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#showhomebutton) |<span data-ttu-id="3d4ef-199">N</span><span class="sxs-lookup"><span data-stu-id="3d4ef-199">N</span></span> | <span data-ttu-id="3d4ef-200">S</span><span class="sxs-lookup"><span data-stu-id="3d4ef-200">Y</span></span>|
|[<span data-ttu-id="3d4ef-201">NewTabPageLocation</span><span class="sxs-lookup"><span data-stu-id="3d4ef-201">NewTabPageLocation</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#newtabpagelocation) |<span data-ttu-id="3d4ef-202">N</span><span class="sxs-lookup"><span data-stu-id="3d4ef-202">N</span></span> |<span data-ttu-id="3d4ef-203">S</span><span class="sxs-lookup"><span data-stu-id="3d4ef-203">Y</span></span> |
|[<span data-ttu-id="3d4ef-204">FavoritesBarEnabled</span><span class="sxs-lookup"><span data-stu-id="3d4ef-204">FavoritesBarEnabled</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#favoritesbarenabled) |<span data-ttu-id="3d4ef-205">N</span><span class="sxs-lookup"><span data-stu-id="3d4ef-205">N</span></span> |<span data-ttu-id="3d4ef-206">S</span><span class="sxs-lookup"><span data-stu-id="3d4ef-206">Y</span></span> |
|[<span data-ttu-id="3d4ef-207">URLAllowlist</span><span class="sxs-lookup"><span data-stu-id="3d4ef-207">URLAllowlist</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#urlallowlist) |<span data-ttu-id="3d4ef-208">S</span><span class="sxs-lookup"><span data-stu-id="3d4ef-208">Y</span></span> |<span data-ttu-id="3d4ef-209">S</span><span class="sxs-lookup"><span data-stu-id="3d4ef-209">Y</span></span> |
|[<span data-ttu-id="3d4ef-210">URLBlocklist</span><span class="sxs-lookup"><span data-stu-id="3d4ef-210">URLBlocklist</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#urlblocklist) |<span data-ttu-id="3d4ef-211">S</span><span class="sxs-lookup"><span data-stu-id="3d4ef-211">Y</span></span> | <span data-ttu-id="3d4ef-212">S</span><span class="sxs-lookup"><span data-stu-id="3d4ef-212">Y</span></span>|
|[<span data-ttu-id="3d4ef-213">ManagedSearchEngines</span><span class="sxs-lookup"><span data-stu-id="3d4ef-213">ManagedSearchEngines</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#managedsearchengines) |<span data-ttu-id="3d4ef-214">N</span><span class="sxs-lookup"><span data-stu-id="3d4ef-214">N</span></span> | <span data-ttu-id="3d4ef-215">S</span><span class="sxs-lookup"><span data-stu-id="3d4ef-215">Y</span></span>|
|[<span data-ttu-id="3d4ef-216">UserFeedbackAllowed</span><span class="sxs-lookup"><span data-stu-id="3d4ef-216">UserFeedbackAllowed</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#userfeedbackallowed) |<span data-ttu-id="3d4ef-217">N</span><span class="sxs-lookup"><span data-stu-id="3d4ef-217">N</span></span> | <span data-ttu-id="3d4ef-218">S</span><span class="sxs-lookup"><span data-stu-id="3d4ef-218">Y</span></span>|
|[<span data-ttu-id="3d4ef-219">VerticalTabsAllowed</span><span class="sxs-lookup"><span data-stu-id="3d4ef-219">VerticalTabsAllowed</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#verticaltabsallowed) | <span data-ttu-id="3d4ef-220">N</span><span class="sxs-lookup"><span data-stu-id="3d4ef-220">N</span></span>|<span data-ttu-id="3d4ef-221">S</span><span class="sxs-lookup"><span data-stu-id="3d4ef-221">Y</span></span> |
|[<span data-ttu-id="3d4ef-222">Configurações do SmartScreen</span><span class="sxs-lookup"><span data-stu-id="3d4ef-222">SmartScreen settings</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#smartscreen-settings-policies) |<span data-ttu-id="3d4ef-223">S</span><span class="sxs-lookup"><span data-stu-id="3d4ef-223">Y</span></span> |<span data-ttu-id="3d4ef-224">S</span><span class="sxs-lookup"><span data-stu-id="3d4ef-224">Y</span></span> |

## <span data-ttu-id="3d4ef-225">Microsoft Edge com acesso atribuído</span><span class="sxs-lookup"><span data-stu-id="3d4ef-225">Microsoft Edge with assigned access</span></span>

### <span data-ttu-id="3d4ef-226">Quiosque de aplicativo único</span><span class="sxs-lookup"><span data-stu-id="3d4ef-226">Single app kiosk</span></span>

<span data-ttu-id="3d4ef-227">No momento, o Microsoft Edge tem suporte para um subconjunto de tipos de modo quiosque da Versão Prévia do Microsoft Edge para acesso atribuído a um aplicativo único com as seguintes experiências de bloqueio: com a Navegação Digital/Interativa e Pública.</span><span class="sxs-lookup"><span data-stu-id="3d4ef-227">Microsoft Edge currently supports a subset of the same Microsoft Edge Legacy kiosk mode types for single-app assigned access with the following lockdown experiences: Digital/Interactive signage, and Public-browsing.</span></span>  

<span data-ttu-id="3d4ef-228">O modo de quiosque do Microsoft Edge com acesso atribuído está disponível atualmente para teste com a versão mais recente do  [Windows 10 Insider Preview](https://insider.windows.com/), versão 20215 ou superior e com o  [Canal Microsoft Edge Dev](https://www.microsoftedgeinsider.com/download), versão 87.0.644.4 ou superior.</span><span class="sxs-lookup"><span data-stu-id="3d4ef-228">Kiosk mode with assigned access is currently available for testing with the latest [Windows 10 Insider Preview Build](https://insider.windows.com/), version 20215 or higher, and with the [Microsoft Edge Dev Channel](https://www.microsoftedgeinsider.com/download), version 87.0.644.4 or higher.</span></span>

**<span data-ttu-id="3d4ef-229">Como faço para obter a visualização do Windows Insiders?</span><span class="sxs-lookup"><span data-stu-id="3d4ef-229">How do I get the Windows Insiders preview?</span></span>**

<span data-ttu-id="3d4ef-230">Para instalar uma versão do Windows 10 Insider Preview Build em um computador, siga as instruções em  [Introdução às Compilações do Windows 10 Insider Preview](https://docs.microsoft.com/windows-insider/get-started).</span><span class="sxs-lookup"><span data-stu-id="3d4ef-230">To install a Windows 10 Insider Preview Build on a PC, follow the instructions in [Getting started with Windows 10 Insider Preview Builds](https://docs.microsoft.com/windows-insider/get-started).</span></span>

### <span data-ttu-id="3d4ef-231">Quiosque de vários aplicativos</span><span class="sxs-lookup"><span data-stu-id="3d4ef-231">Multi-app kiosk</span></span>

<span data-ttu-id="3d4ef-232">O Microsoft Edge pode ser executado com [acesso atribuído a vários aplicativos](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps) no Windows 10, que é o equivalente ao tipo de modo de quiosque "Navegação Normal" da Versão Herdada do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="3d4ef-232">Microsoft Edge can be run with [multi-app assigned access](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps) on Windows 10, which is the equivalent of Microsoft Edge Legacy "Normal browsing" kiosk mode type.</span></span> <span data-ttu-id="3d4ef-233">Para configurar o Microsoft Edge com acesso atribuído a vários aplicativos, siga as instruções sobre como [Configurar um quiosque para vários aplicativos](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps).</span><span class="sxs-lookup"><span data-stu-id="3d4ef-233">To configure Microsoft Edge with multi-app assigned access, follow the instructions on how to [Set up a multi-app kiosk](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps).</span></span> <span data-ttu-id="3d4ef-234">(O AUMID para o canal Estável do Microsoft Edge é **MSEdge**).</span><span class="sxs-lookup"><span data-stu-id="3d4ef-234">(The AUMID for the Microsoft Edge Stable channel is **MSEdge**).</span></span>

<span data-ttu-id="3d4ef-235">Ao usar o Microsoft Edge com acesso atribuído a vários aplicativos, você poderá usar as [políticas de navegador do Microsoft Edge](https://review.docs.microsoft.com/DeployEdge/microsoft-edge-policies) para configurar a experiência de navegação para atender aos seus requisitos exclusivos.</span><span class="sxs-lookup"><span data-stu-id="3d4ef-235">When using Microsoft Edge with multi-app assigned access, you can configure Microsoft Edge kiosk to use the[Microsoft Edge browser policies](https://review.docs.microsoft.com/DeployEdge/microsoft-edge-policies) to configure the browsing experience to meet your unique requirements.</span></span>

### <span data-ttu-id="3d4ef-236">Configurar usando as configurações do Windows</span><span class="sxs-lookup"><span data-stu-id="3d4ef-236">Configure using Windows Settings</span></span>

<span data-ttu-id="3d4ef-237">As Configurações do Windows é a maneira mais simples de configurar um ou mais dispositivos em modo de quiosque de aplicativo único.</span><span class="sxs-lookup"><span data-stu-id="3d4ef-237">Windows Settings is the simplest way to set up one or two single-app kiosk devices.</span></span> <span data-ttu-id="3d4ef-238">Use as etapas a seguir para configurar um computador em modo de quiosque de aplicativo único.</span><span class="sxs-lookup"><span data-stu-id="3d4ef-238">Use the following steps to set up a single-app kiosk computer.</span></span>

1. <span data-ttu-id="3d4ef-239">Instale a versão do Windows 10 Insider Preview mais recente, versão 20215 ou superior.</span><span class="sxs-lookup"><span data-stu-id="3d4ef-239">Install the latest Windows 10 Insider Preview, version 20215 or higher.</span></span> <span data-ttu-id="3d4ef-240">Siga as instruções em [Introdução às Compilações de Visualização do Windows 10 Insider](https://docs.microsoft.com/windows-insider/get-started).</span><span class="sxs-lookup"><span data-stu-id="3d4ef-240">Follow the instructions in [Getting started with Windows 10 Insider Preview Builds](https://docs.microsoft.com/windows-insider/get-started).</span></span>
2. <span data-ttu-id="3d4ef-241">Instale a versão mais recente do [Canal Estável do Microsoft Edge](https://www.microsoft.com/edge)versão 87 ou superior.</span><span class="sxs-lookup"><span data-stu-id="3d4ef-241">Install the latest version of [Microsoft Edge Stable channel](https://www.microsoft.com/edge), version 87 or higher.</span></span>  <span data-ttu-id="3d4ef-242">Para testar os recursos mais recentes, você pode baixar o [Canal Microsoft Edge Dev](https://www.microsoftedgeinsider.com/download)mais recente, versão 89 ou superior.</span><span class="sxs-lookup"><span data-stu-id="3d4ef-242">To test the latest features, you can download the latest [Microsoft Edge Dev channel](https://www.microsoftedgeinsider.com/download), version 89 or higher.</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="3d4ef-243">Como é necessária uma instalação no nível do dispositivo, só há suporte para um canal que não seja Canary.</span><span class="sxs-lookup"><span data-stu-id="3d4ef-243">Because a device level installation is required, only a non-Canary channel is supported.</span></span>

3. <span data-ttu-id="3d4ef-244">No computador modo de quiosque, abra as configurações do Windows e digite "modo de quiosque" no campo de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="3d4ef-244">On the kiosk computer, open Windows Settings, and type "kiosk" in the search field.</span></span> <span data-ttu-id="3d4ef-245">Selecione  **Configurar um modo de quiosque (acesso atribuído)**, mostrada na próxima captura de tela para abrir a caixa de diálogo para criar o modo de quiosque.</span><span class="sxs-lookup"><span data-stu-id="3d4ef-245">Select  **Set up a kiosk (assigned access)**, shown in the next screenshot to open the dialog for creating the kiosk.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-1-assigned-access.png" alt-text="Configurar o modo de quiosque com acesso atribuído":::

4. <span data-ttu-id="3d4ef-247">Na página **Configurar um modo de quiosque** , clique em  **Introdução**.</span><span class="sxs-lookup"><span data-stu-id="3d4ef-247">On the **Set up a kiosk** page, click **Get started**.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-2-get-started.png" alt-text="Página modo de quiosque – introdução":::

5. <span data-ttu-id="3d4ef-249">Digite um nome para criar uma nova conta modo de quiosque ou escolha uma conta existente na lista suspensa preenchida e clique em  **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="3d4ef-249">Type a name to create a new kiosk account or choose an existing account from the populated dropdown list and then click **Next**.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-3-create-account.png" alt-text="Modo de quiosque - criar conta":::

6. <span data-ttu-id="3d4ef-251">Na página **Escolher um aplicativo de modo de quiosque** , selecione **Microsoft Edge** e clique em  **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="3d4ef-251">On the **Choose a kiosk app** page, select **Microsoft Edge** and then click **Next**.</span></span>

   > [!NOTE]
   > <span data-ttu-id="3d4ef-252">Isso se aplica apenas ao Microsoft Edge Dev, Beta e a canais estáveis.</span><span class="sxs-lookup"><span data-stu-id="3d4ef-252">This only applies to Microsoft Edge Dev, Beta, and Stable channels.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-4-pick-app.png" alt-text="Modo de quiosque - escolha um aplicativo":::

7. <span data-ttu-id="3d4ef-254">Escolha uma das opções a seguir para exibir o Microsoft Edge na execução no modo de quiosque:</span><span class="sxs-lookup"><span data-stu-id="3d4ef-254">Pick one of the following options for how Microsoft Edge displays when running in kiosk mode:</span></span>

   - <span data-ttu-id="3d4ef-255">Sinalização digital/interativa - Exibe um site específico no modo de tela inteira executando o Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="3d4ef-255">Digital/Interactive signage - Displays a specific site in full-screen mode, running Microsoft Edge.</span></span>
   - <span data-ttu-id="3d4ef-256">Navegador público - Executa uma versão limitada com várias guias do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="3d4ef-256">Public browser - Runs a limited multi-tab version of Microsoft Edge.</span></span>

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-5a-digital-sign.png" alt-text="Exibição do modo quiosque – sinal digital de tela inteira":::

8. <span data-ttu-id="3d4ef-258">Selecione **Próximo**.</span><span class="sxs-lookup"><span data-stu-id="3d4ef-258">Select **Next**.</span></span>
9. <span data-ttu-id="3d4ef-259">Digite a URL a ser carregada quando o quiosque for iniciado.</span><span class="sxs-lookup"><span data-stu-id="3d4ef-259">Type the URL to load when the kiosk launches.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-6-enter-url.png" alt-text="Modo de quiosque - Inserir URL":::

10. <span data-ttu-id="3d4ef-261">Aceite o valor padrão de 5 minutos para o tempo ocioso ou escolha um outro valor.</span><span class="sxs-lookup"><span data-stu-id="3d4ef-261">Accept the default value of 5 minutes for the idle time or provide a value of your own.</span></span>

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-7-enter-idle-time.png" alt-text="Modo de quiosque - Inserir tempo ocioso":::

11. <span data-ttu-id="3d4ef-263">Clique **Próximo**.</span><span class="sxs-lookup"><span data-stu-id="3d4ef-263">Click **Next**.</span></span>
12. <span data-ttu-id="3d4ef-264">Feche a janela de  **Configurações**  para salvar e aplicar suas opções.</span><span class="sxs-lookup"><span data-stu-id="3d4ef-264">Close the **Settings** window to save and apply your choices.</span></span>

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode--8-done.png" alt-text="Modo de quiosque – concluir configuração":::

13. <span data-ttu-id="3d4ef-266">Saia do dispositivo de modo de quiosque e entre com a conta de modo de quiosque local para validar a configuração.</span><span class="sxs-lookup"><span data-stu-id="3d4ef-266">Sign out from the kiosk device and sign in with the local kiosk account to validate the configuration.</span></span>

## <span data-ttu-id="3d4ef-267">Limitações funcionais</span><span class="sxs-lookup"><span data-stu-id="3d4ef-267">Functional limitations</span></span>

<span data-ttu-id="3d4ef-268">Com o lançamento desta versão de visualização do modo de quiosque, continuamos a melhorar o produto e adicionar novos recursos.</span><span class="sxs-lookup"><span data-stu-id="3d4ef-268">With the release of this preview version of kiosk mode we're continuing work on improving the product and adding new features.</span></span>

<span data-ttu-id="3d4ef-269">Recomendamos que você desligue:</span><span class="sxs-lookup"><span data-stu-id="3d4ef-269">We recommend that you turn off:</span></span>

- [<span data-ttu-id="3d4ef-270">StartupBoostEnabled</span><span class="sxs-lookup"><span data-stu-id="3d4ef-270">StartupBoostEnabled</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#startupboostenabled)
- [<span data-ttu-id="3d4ef-271">InternetExplorerIntegrationLevel</span><span class="sxs-lookup"><span data-stu-id="3d4ef-271">InternetExplorerIntegrationLevel</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#internetexplorerintegrationlevel)
- [<span data-ttu-id="3d4ef-272">Extensões</span><span class="sxs-lookup"><span data-stu-id="3d4ef-272">Extensions</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#extensions-policies)
- [<span data-ttu-id="3d4ef-273">BackgroundModeEnabled</span><span class="sxs-lookup"><span data-stu-id="3d4ef-273">BackgroundModeEnabled</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#backgroundmodeenabled)

## <span data-ttu-id="3d4ef-274">Roteiro</span><span class="sxs-lookup"><span data-stu-id="3d4ef-274">Roadmap</span></span>

### <span data-ttu-id="3d4ef-275">No início de 2021</span><span class="sxs-lookup"><span data-stu-id="3d4ef-275">In early 2021</span></span>

<span data-ttu-id="3d4ef-276">Incluiremos os seguintes recursos e suporte:</span><span class="sxs-lookup"><span data-stu-id="3d4ef-276">We'll add the following support and features:</span></span>

- <span data-ttu-id="3d4ef-277">Disponibilidade geral do modo de quiosque do Microsoft Edge com acesso atribuído a um único aplicativo no Windows 10 1909 ou superior.</span><span class="sxs-lookup"><span data-stu-id="3d4ef-277">General availability of Microsoft Edge kiosk mode with assigned access single app on Windows 10 1909 and higher.</span></span>
- <span data-ttu-id="3d4ef-278">Recursos adicionais para a paridade com a Versão Prévia do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="3d4ef-278">Additional features for parity with Microsoft Edge Legacy.</span></span>
- <span data-ttu-id="3d4ef-279">Integração com o Intune para configurar os dispositivos usando o Profile UX do modo de quiosque.</span><span class="sxs-lookup"><span data-stu-id="3d4ef-279">Integration with Intune to configure devices using kiosk mode profile UX.</span></span>
- <span data-ttu-id="3d4ef-280">Atalhos de teclado adicionais serão bloqueados.</span><span class="sxs-lookup"><span data-stu-id="3d4ef-280">Additional keyboard shortcuts will be blocked.</span></span>
- <span data-ttu-id="3d4ef-281">Restrinja o lançamento de outros aplicativos do navegador.</span><span class="sxs-lookup"><span data-stu-id="3d4ef-281">Restrict the launch of other applications from the browser.</span></span>

## <span data-ttu-id="3d4ef-282">Veja também</span><span class="sxs-lookup"><span data-stu-id="3d4ef-282">See also</span></span>

- [<span data-ttu-id="3d4ef-283">Configurar quiosques e sinalizações digitais em edições do Windows desktop</span><span class="sxs-lookup"><span data-stu-id="3d4ef-283">Configure kiosks and digital signs on Windows desktop editions</span></span>](https://docs.microsoft.com/windows/configuration/kiosk-methods)
- [<span data-ttu-id="3d4ef-284">Implantar o modo de quiosque da Versão Herdada do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="3d4ef-284">Deploy Microsoft Edge Legacy kiosk mode</span></span>](https://aka.ms/edgekioskmode)
- [<span data-ttu-id="3d4ef-285">Planejar sua implantação do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="3d4ef-285">Plan your deployment of Microsoft Edge</span></span>](deploy-edge-plan-deployment.md)
- [<span data-ttu-id="3d4ef-286">Página de aterrissagem do Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="3d4ef-286">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
