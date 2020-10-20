---
title: Redirecionamento do Internet Explorer para o Microsoft Edge para compatibilidade com os sites modernos
ms.author: laannade
author: dan-wesley
manager: ratetali
ms.date: 10/19/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Redirecionamento do Internet Explorer para o Microsoft Edge para compatibilidade com os sites modernos
ms.openlocfilehash: ce9e8dabdff25cc3ba375746ec82ddd78b6d7694
ms.sourcegitcommit: cf991cc4bd2e70169902cbda9ddc870d70e31ca2
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/19/2020
ms.locfileid: "11120516"
---
# <span data-ttu-id="abfbf-103">Redirecionamento do Internet Explorer para o Microsoft Edge para compatibilidade com os sites modernos</span><span class="sxs-lookup"><span data-stu-id="abfbf-103">Redirection from Internet Explorer to Microsoft Edge for compatibility with modern web sites</span></span>

> [!NOTE]
> <span data-ttu-id="abfbf-104">Este artigo se aplica ao Microsoft Edge Estável versão 87 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="abfbf-104">This article applies to Microsoft Edge Stable version 87 or later.</span></span>

## <span data-ttu-id="abfbf-105">Visão geral</span><span class="sxs-lookup"><span data-stu-id="abfbf-105">Overview</span></span>

<span data-ttu-id="abfbf-106">Muitos sites modernos têm designs incompatíveis com o Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="abfbf-106">Many modern websites have designs that are incompatible with Internet Explorer.</span></span> <span data-ttu-id="abfbf-107">Sempre que um usuário do Internet Explorer visita um site público incompatível, ele recebe uma mensagem informando que o site não é compatível com seu navegador e que precisa mudar manualmente para um navegador diferente.</span><span class="sxs-lookup"><span data-stu-id="abfbf-107">Whenever an Internet Explorer user visits an incompatible public site, they get a message that tells them the site is incompatible with their browser, and they need to manually switch to a different browser.</span></span>

<span data-ttu-id="abfbf-108">A necessidade de mudar manualmente para um navegador diferente muda a partir da versão 87 do Microsoft Edge Estável.</span><span class="sxs-lookup"><span data-stu-id="abfbf-108">The need to  manually switch to a different browser changes starting with Microsoft Edge Stable version 87.</span></span>

<span data-ttu-id="abfbf-109">Quando o usuário visita um site incompatível com o Internet Explorer, ele será automaticamente redirecionado para o Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="abfbf-109">When a user goes to a site that is incompatible with Internet Explorer, they will be automatically redirected to Microsoft Edge.</span></span> <span data-ttu-id="abfbf-110">Este artigo descreve a experiência do usuário para o redirecionamento e as políticas de grupo que são utilizadas para configurar ou desativar o redirecionamento automático.</span><span class="sxs-lookup"><span data-stu-id="abfbf-110">This article describes the user experience for redirection and the group policies that are used to configure or disable automatic redirection.</span></span>

> [!NOTE]
> <span data-ttu-id="abfbf-111">A Microsoft mantém uma lista de todos os sites que são conhecidos por não serem compatíveis com o Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="abfbf-111">Microsoft maintains a list of all sites that are known to be incompatible with Internet Explorer.</span></span>

## <span data-ttu-id="abfbf-112">Experiência de redirecionamento</span><span class="sxs-lookup"><span data-stu-id="abfbf-112">Redirection experience</span></span>

<span data-ttu-id="abfbf-113">No redirecionamento para o Microsoft Edge, os usuários veem uma única vez a caixa de diálogo na próxima captura de tela.</span><span class="sxs-lookup"><span data-stu-id="abfbf-113">On redirection to Microsoft Edge, users are shown the one-time dialog in the next screenshot.</span></span> <span data-ttu-id="abfbf-114">Este diálogo explica porque eles estão sendo redirecionados e solicita o consentimento para copiar seus dados de navegação e preferências do Internet Explorer para o Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="abfbf-114">This dialog explains why they're getting redirected and prompts for consent to copy their browsing data and preferences from Internet Explorer to Microsoft Edge.</span></span> <span data-ttu-id="abfbf-115">Os seguintes dados de navegação serão importados: Favoritos, senhas, mecanismos de busca, guias abertas, histórico, configurações, cookies e a Página Inicial.</span><span class="sxs-lookup"><span data-stu-id="abfbf-115">The following browsing data will be imported: Favorites, Passwords, Search engines, open tabs, History, settings, cookies, and the Home Page.</span></span>

![Notificação de navegação e solicitação de importação de dados e preferências.](media/edge-learnmore-neededge/neededge-dialog1.png)

<span data-ttu-id="abfbf-117">Mesmo não dando seu consentimento ao marcar "Sempre traga meus dados de navegação e preferências do Internet Explorer", eles podem clicar em **Continuar navegação** para continuar sua sessão.</span><span class="sxs-lookup"><span data-stu-id="abfbf-117">Even if they don't give their consent by checking "Always bring over my browsing data and preferences from Internet Explorer", they can click **Continue browsing** to continue their session.</span></span>

<span data-ttu-id="abfbf-118">Finalmente, um banner de incompatibilidade do site, exibido na próxima captura de tela, aparece abaixo da barra de endereços para cada redirecionamento.</span><span class="sxs-lookup"><span data-stu-id="abfbf-118">Finally, a website incompatibility banner, shown in the next screenshot, appears below the address bar for every redirection.</span></span>

![Notificações sobre sites modernos e solicitações para definir o Microsoft Edge como navegador padrão ou para explorar o Microsoft Edge.](media/edge-learnmore-neededge/neededge-banner.png)

<span data-ttu-id="abfbf-120">O banner de incompatibilidade do site:</span><span class="sxs-lookup"><span data-stu-id="abfbf-120">The website incompatibility banner:</span></span>

- <span data-ttu-id="abfbf-121">incentiva o usuário a mudar para o Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="abfbf-121">encourages the user to switch to Microsoft Edge</span></span>
- <span data-ttu-id="abfbf-122">oferece para definir o Microsoft Edge como navegador padrão</span><span class="sxs-lookup"><span data-stu-id="abfbf-122">offers to make Microsoft Edge as the default browser</span></span>
- <span data-ttu-id="abfbf-123">dá ao usuário a opção de explorar o Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="abfbf-123">gives the user the option to explore Microsoft Edge</span></span>

<span data-ttu-id="abfbf-124">Quando um site é redirecionado do Internet Explorer para o Microsoft Edge, a guia do Internet Explorer que começou a carregar o site é fechada se não tiver nenhum conteúdo anterior.</span><span class="sxs-lookup"><span data-stu-id="abfbf-124">When a site is redirected from Internet Explorer to Microsoft Edge, the Internet Explorer tab that started loading the site is closed if it had no prior content.</span></span> <span data-ttu-id="abfbf-125">Caso contrário, a visualização da guia ativa vai para uma  página de  [suporte](https://support.microsoft.com/office/the-website-you-were-trying-to-reach-doesn-t-work-with-internet-explorer-8f5fc675-cd47-414c-9535-12821ddfc554?ui=en-US&rs=en-US&ad=US) da Microsoft que explica por que o site foi redirecionado para o Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="abfbf-125">Otherwise, the active tab view goes to a  Microsoft [support](https://support.microsoft.com/office/the-website-you-were-trying-to-reach-doesn-t-work-with-internet-explorer-8f5fc675-cd47-414c-9535-12821ddfc554?ui=en-US&rs=en-US&ad=US) page that explains why the site was redirected to Microsoft Edge.</span></span>

> [!NOTE]
> <span data-ttu-id="abfbf-126">Após o redirecionamento, os usuários podem voltar a usar o Internet Explorer para sites que não estão na lista de incompatibilidades do Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="abfbf-126">After a redirection users can go back to using Internet Explorer for sites that are not on the Internet Explorer incompatibility list.</span></span>  

## <span data-ttu-id="abfbf-127">Políticas de configuração do redirecionamento para o Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="abfbf-127">Policies to configure redirection to Microsoft Edge</span></span>

> [!NOTE]
> <span data-ttu-id="abfbf-128">Essas políticas estarão disponíveis como atualizações de arquivo ADMX em 26 de outubro de 2020 e no Intune em 9 de novembro de 2020.</span><span class="sxs-lookup"><span data-stu-id="abfbf-128">These policies will be available as ADMX file updates by October 26, 2020 and will be available in Intune by November 9, 2020.</span></span>

<span data-ttu-id="abfbf-129">Três políticas de grupo devem ser configuradas para permitir o redirecionamento automático para a Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="abfbf-129">Three group policies must be configured to enable automatic redirection to Microsoft Edge.</span></span> <span data-ttu-id="abfbf-130">Estas políticas são:</span><span class="sxs-lookup"><span data-stu-id="abfbf-130">These policies are:</span></span>

- <span data-ttu-id="abfbf-131">RedirectSitesFromInternetExplorerPreventBHOInstall</span><span class="sxs-lookup"><span data-stu-id="abfbf-131">RedirectSitesFromInternetExplorerPreventBHOInstall</span></span>
- <span data-ttu-id="abfbf-132">RedirectSitesFromInternetExplorerRedirectMode</span><span class="sxs-lookup"><span data-stu-id="abfbf-132">RedirectSitesFromInternetExplorerRedirectMode</span></span>
- <span data-ttu-id="abfbf-133">HideInternetExplorerRedirectUXForIncompatibleSitesEnabled</span><span class="sxs-lookup"><span data-stu-id="abfbf-133">HideInternetExplorerRedirectUXForIncompatibleSitesEnabled</span></span>

### <span data-ttu-id="abfbf-134">Política: RedirectSitesFromInternetExplorerPreventBHOInstall</span><span class="sxs-lookup"><span data-stu-id="abfbf-134">Policy: RedirectSitesFromInternetExplorerPreventBHOInstall</span></span>

<span data-ttu-id="abfbf-135">O redirecionamento do Internet Explorer para o Microsoft Edge requer um Objeto Auxiliar de Navegador do Internet Explorer (BHO) chamado "IEtoEdge BHO".</span><span class="sxs-lookup"><span data-stu-id="abfbf-135">Redirection from Internet Explorer to Microsoft Edge requires an Internet Explorer Browser Helper Object (BHO) named "IEtoEdge BHO".</span></span> <span data-ttu-id="abfbf-136">A política **RedirectSitesFromInternetExplorerPreventBHOInstall** controla se o BHO está ou não instalado.</span><span class="sxs-lookup"><span data-stu-id="abfbf-136">The **RedirectSitesFromInternetExplorerPreventBHOInstall** policy controls whether or not this BHO is installed.</span></span>  

- <span data-ttu-id="abfbf-137">Se você ativar esta política, o BHO necessário para o redirecionamento não será instalado e seus usuários continuarão a ver mensagens de incompatibilidade para certos sites no Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="abfbf-137">If you enable this policy, the BHO required for redirection will not be installed and your users will continue to see incompatibility messages for certain websites on Internet Explorer.</span></span> <span data-ttu-id="abfbf-138">Se o BHO já estiver instalado, ele será desinstalado na próxima vez em que o canal do Microsoft Edge Estável for atualizado.</span><span class="sxs-lookup"><span data-stu-id="abfbf-138">If the BHO is already installed, it will be uninstalled the next time the Microsoft Edge Stable channel is updated.</span></span>
- <span data-ttu-id="abfbf-139">Se você desativar ou não configurar esta política, o BHO será instalado.</span><span class="sxs-lookup"><span data-stu-id="abfbf-139">If you disable or don't configure this policy, the BHO will be installed.</span></span> <span data-ttu-id="abfbf-140">Este é o comportamento padrão.</span><span class="sxs-lookup"><span data-stu-id="abfbf-140">This is the default behavior.</span></span>

<span data-ttu-id="abfbf-141">Além de precisar do BHO, há uma dependência do **RedirectSitesFromInternetExplorerRedirectMode**, que precisa ser definida como "Sitelist" ou "Não Configurado".</span><span class="sxs-lookup"><span data-stu-id="abfbf-141">In addition to needing the BHO, there is a dependency on the **RedirectSitesFromInternetExplorerRedirectMode**, which needs to be set to "Sitelist" or "Not Configured".</span></span>

### <span data-ttu-id="abfbf-142">Política: RedirectSitesFromInternetExplorerRedirectMode</span><span class="sxs-lookup"><span data-stu-id="abfbf-142">Policy: RedirectSitesFromInternetExplorerRedirectMode</span></span>

 <span data-ttu-id="abfbf-143">Esta política corresponde à configuração do Microsoft Edge **Navegador padrão** "Permitir que o Internet Explorer abra sites no Microsoft Edge".</span><span class="sxs-lookup"><span data-stu-id="abfbf-143">This policy corresponds to the Microsoft Edge **Default browser** setting "Let Internet Explorer open sites in Microsoft Edge".</span></span> <span data-ttu-id="abfbf-144">Você pode acessar essa configuração indo para o URL *edge://settings/defaultbrowser*.</span><span class="sxs-lookup"><span data-stu-id="abfbf-144">You can access this setting by going to the *edge://settings/defaultbrowser* URL.</span></span>  

- <span data-ttu-id="abfbf-145">Se você não configurar esta política ou defini-la como "Sitelist", o Internet Explorer redirecionará os sites incompatíveis para o Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="abfbf-145">If you don't configure this policy or set it to "Sitelist", Internet Explorer will redirect incompatible sites to Microsoft Edge.</span></span> <span data-ttu-id="abfbf-146">Este é o comportamento padrão.</span><span class="sxs-lookup"><span data-stu-id="abfbf-146">This is the default behavior.</span></span>
- <span data-ttu-id="abfbf-147">Se você desativar esta política, os sites incompatíveis não serão redirecionados para a Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="abfbf-147">If you disable this policy, incompatible sites aren't redirected to Microsoft Edge.</span></span>

> [!NOTE]
> <span data-ttu-id="abfbf-148">Se estiver em um dispositivo pessoal que não é gerenciado pela sua organização, você verá outra configuração chamada "Permitir que sites sejam carregados no modo Internet Explorer" em **Compatibilidade com o Internet Explorer**.</span><span class="sxs-lookup"><span data-stu-id="abfbf-148">If you're on a personal device that isn't  managed by your organization, you'll see another setting named "Allow sites to be loaded in Internet Explorer mode" under **Internet Explorer compatibility**.</span></span>
>
><span data-ttu-id="abfbf-149">Se você estiver em um dispositivo associado ao domínio ou registrado no Mobile Device Management (MDM), não verá esta opção.</span><span class="sxs-lookup"><span data-stu-id="abfbf-149">If you're on a domain joined or Mobile Device Management (MDM) enrolled device, you won't see this option.</span></span>
>
> <span data-ttu-id="abfbf-150">Em vez disso, se você quiser permitir que seus usuários carreguem sites no modo Internet Explorer, você pode fazê-lo configurando a política [Permitir o Internet Explorer no modo teste](https://docs.microsoft.com/deployedge/microsoft-edge-policies#allow-internet-explorer-mode-testing).</span><span class="sxs-lookup"><span data-stu-id="abfbf-150">Instead, if you want to let your users load sites in Internet Explorer mode, you can do so by configuring the policy [Allow Internet Explorer mode testing](https://docs.microsoft.com/deployedge/microsoft-edge-policies#allow-internet-explorer-mode-testing).</span></span>

### <span data-ttu-id="abfbf-151">Política: HideInternetExplorerRedirectUXForIncompatibleSitesEnabled</span><span class="sxs-lookup"><span data-stu-id="abfbf-151">Policy: HideInternetExplorerRedirectUXForIncompatibleSitesEnabled</span></span>

<span data-ttu-id="abfbf-152">Esta política configura a experiência do usuário com o redirecionamento de sites incompatíveis para o Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="abfbf-152">This policy configures the user experience for incompatible site redirection to Microsoft Edge.</span></span>  

- <span data-ttu-id="abfbf-153">Se você ativar esta política, os usuários nunca verão a caixa de diálogo de redirecionamento e nem o banner de redirecionamento.</span><span class="sxs-lookup"><span data-stu-id="abfbf-153">If you enable this policy, users never see the one-time redirection dialog and the redirection banner.</span></span> <span data-ttu-id="abfbf-154">Nenhum dado do navegador ou preferências do usuário serão importados.</span><span class="sxs-lookup"><span data-stu-id="abfbf-154">No browser data or user preferences are imported.</span></span>
- <span data-ttu-id="abfbf-155">Se você desabilitar ou não configurar esta política, a caixa de diálogo de redirecionamento será exibida no primeiro redirecionamento e o banner de redirecionamento persistente será exibido nas sessões que começam com um redirecionamento.</span><span class="sxs-lookup"><span data-stu-id="abfbf-155">If you disable or don't configure this policy, the redirection dialog will be shown on the first redirection and the persistent redirection banner will be shown for sessions that start with a redirection.</span></span>

  > [!NOTE]
  > <span data-ttu-id="abfbf-156">Os dados de navegação do usuário serão importados sempre que o usuário encontrar um novo redirecionamento.</span><span class="sxs-lookup"><span data-stu-id="abfbf-156">User browsing data will be imported every time a user encounters a new redirection.</span></span> <span data-ttu-id="abfbf-157">Entretanto, isso só acontecerá se o usuário consentir a importação na caixa de diálogo de redirecionamento.</span><span class="sxs-lookup"><span data-stu-id="abfbf-157">However, this only happens if the user consented to the import on the one-time redirection dialog.</span></span>

## <span data-ttu-id="abfbf-158">Desative o redirecionamento para o Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="abfbf-158">Disable redirection to Microsoft Edge</span></span>

<span data-ttu-id="abfbf-159">Se você quiser desativar o redirecionamento ANTES da atualização para o Microsoft Edge Estável versão 87, siga o seguinte passo:</span><span class="sxs-lookup"><span data-stu-id="abfbf-159">If you want to disable redirection BEFORE updating to Microsoft Edge Stable version 87, use the following step:</span></span>

1. <span data-ttu-id="abfbf-160">Defina a política **RedirectSitesFromInternetExplorerRedirectMode** para **Habilitada**.</span><span class="sxs-lookup"><span data-stu-id="abfbf-160">Set the **RedirectSitesFromInternetExplorerRedirectMode** policy to **Enabled**.</span></span> <span data-ttu-id="abfbf-161">Esta configuração deixará de redirecionar assim que a política entrar em vigor.</span><span class="sxs-lookup"><span data-stu-id="abfbf-161">This setting will stop redirecting as soon as the policy takes effect.</span></span>

<span data-ttu-id="abfbf-162">Se você quiser desativar o redirecionamento DEPOIS da atualização para o Microsoft Edge Estável versão 87, siga os seguintes passos:</span><span class="sxs-lookup"><span data-stu-id="abfbf-162">If you want to disable redirection AFTER updating to Microsoft Edge Stable version 87, use the following steps:</span></span>

1. <span data-ttu-id="abfbf-163">Defina a política **RedirectSitesFromInternetExplorerRedirectMode** para **Desabilitada**.</span><span class="sxs-lookup"><span data-stu-id="abfbf-163">Set the **RedirectSitesFromInternetExplorerRedirectMode** policy to **Disabled**.</span></span> <span data-ttu-id="abfbf-164">Esta configuração deixará de redirecionar assim que a política entrar em vigor.</span><span class="sxs-lookup"><span data-stu-id="abfbf-164">This setting will stop redirecting as soon as the policy takes effect.</span></span>
2. <span data-ttu-id="abfbf-165">Defina a política **RedirectSitesFromInternetExplorerPreventBHOInstall** para **Habilitada**.</span><span class="sxs-lookup"><span data-stu-id="abfbf-165">Set the **RedirectSitesFromInternetExplorerPreventBHOInstall** policy to **Enabled**.</span></span> <span data-ttu-id="abfbf-166">Isto vai desinstalar o BHO depois da próxima atualização do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="abfbf-166">This will uninstall the BHO after the next Microsoft Edge update.</span></span>

## <span data-ttu-id="abfbf-167">Veja também</span><span class="sxs-lookup"><span data-stu-id="abfbf-167">See also</span></span>

- [<span data-ttu-id="abfbf-168">Página de destino do Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="abfbf-168">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="abfbf-169">Políticas do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="abfbf-169">Microsoft Edge Policies</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies)