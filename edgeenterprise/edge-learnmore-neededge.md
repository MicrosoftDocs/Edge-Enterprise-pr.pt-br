---
title: Redirecionamento do Internet Explorer para o Microsoft Edge para compatibilidade com os sites modernos
ms.author: laannade
author: dan-wesley
manager: ratetali
ms.date: 11/16/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Redirecionamento do Internet Explorer para o Microsoft Edge para compatibilidade com os sites modernos
ms.openlocfilehash: 7cd74eda6d8ada7647862ea69f77a982713f0c14
ms.sourcegitcommit: 4192328ee585bc32a9be528766b8a5a98e046c8e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/25/2021
ms.locfileid: "11617291"
---
# <a name="redirection-from-internet-explorer-to-microsoft-edge-for-compatibility-with-modern-web-sites"></a><span data-ttu-id="66492-103">Redirecionamento do Internet Explorer para o Microsoft Edge para compatibilidade com os sites modernos</span><span class="sxs-lookup"><span data-stu-id="66492-103">Redirection from Internet Explorer to Microsoft Edge for compatibility with modern web sites</span></span>

> [!NOTE]
> <span data-ttu-id="66492-104">Este artigo se aplica ao Microsoft Edge Estável versão 87 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="66492-104">This article applies to Microsoft Edge Stable version 87 or later.</span></span>

## <a name="overview"></a><span data-ttu-id="66492-105">Visão Geral</span><span class="sxs-lookup"><span data-stu-id="66492-105">Overview</span></span>

>[!Note]
> <span data-ttu-id="66492-106">O aplicativo de área de trabalho Internet Explorer 11 será desativado e ficará sem suporte em 15 de junho de 2022 (para obter uma lista do que está no escopo, [consulte as Perguntas frequentes](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/internet-explorer-11-desktop-app-retirement-faq/ba-p/2366549)).</span><span class="sxs-lookup"><span data-stu-id="66492-106">The Internet Explorer 11 desktop application will be retired and go out of support on June 15, 2022 (for a list of what’s in scope, [see the FAQ](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/internet-explorer-11-desktop-app-retirement-faq/ba-p/2366549)).</span></span> <span data-ttu-id="66492-107">Os mesmos aplicativos e sites do IE11 que você usa hoje podem abrir no Microsoft Edge com o modo Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="66492-107">The same IE11 apps and sites you use today can open in Microsoft Edge with Internet Explorer mode.</span></span> <span data-ttu-id="66492-108">[Saiba mais aqui](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/).</span><span class="sxs-lookup"><span data-stu-id="66492-108">[Learn more here](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/).</span></span>

<span data-ttu-id="66492-109">Muitos sites modernos têm designs incompatíveis com o Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="66492-109">Many modern websites have designs that are incompatible with Internet Explorer.</span></span> <span data-ttu-id="66492-110">Sempre que um usuário do Internet Explorer visita um site público incompatível, ele recebe uma mensagem informando que o site não é compatível com seu navegador e que precisa mudar manualmente para um navegador diferente.</span><span class="sxs-lookup"><span data-stu-id="66492-110">Whenever an Internet Explorer user visits an incompatible public site, they get a message that tells them the site is incompatible with their browser, and they need to manually switch to a different browser.</span></span>

<span data-ttu-id="66492-111">A necessidade de mudar manualmente para um navegador diferente muda a partir da versão 87 do Microsoft Edge Estável.</span><span class="sxs-lookup"><span data-stu-id="66492-111">The need to  manually switch to a different browser changes starting with Microsoft Edge Stable version 87.</span></span>

<span data-ttu-id="66492-112">Quando o usuário visita um site incompatível com o Internet Explorer, ele será automaticamente redirecionado para o Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="66492-112">When a user goes to a site that is incompatible with Internet Explorer, they will be automatically redirected to Microsoft Edge.</span></span> <span data-ttu-id="66492-113">Este artigo descreve a experiência do usuário para o redirecionamento e as políticas de grupo que são utilizadas para configurar ou desativar o redirecionamento automático.</span><span class="sxs-lookup"><span data-stu-id="66492-113">This article describes the user experience for redirection and the group policies that are used to configure or disable automatic redirection.</span></span>

> [!NOTE]
> <span data-ttu-id="66492-114">A Microsoft mantém uma lista de todos os sites que são conhecidos por não serem compatíveis com o Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="66492-114">Microsoft maintains a list of all sites that are known to be incompatible with Internet Explorer.</span></span> <span data-ttu-id="66492-115">Para obter mais informações, consulte [Solicitar atualizações à lista de sites incompatíveis](/microsoft-edge/web-platform/ie-to-microsoft-edge-redirection#request-an-update-to-the-ie-compatibility-list)</span><span class="sxs-lookup"><span data-stu-id="66492-115">For more information, see [Request updates to the incompatible sites list](/microsoft-edge/web-platform/ie-to-microsoft-edge-redirection#request-an-update-to-the-ie-compatibility-list)</span></span>

## <a name="prerequisites"></a><span data-ttu-id="66492-116">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="66492-116">Prerequisites</span></span>
- <span data-ttu-id="66492-117">Versão 87 estável ou posterior do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="66492-117">Microsoft Edge Stable version 87 or later</span></span>
- <span data-ttu-id="66492-118">Versões do Windows</span><span class="sxs-lookup"><span data-stu-id="66492-118">Windows versions</span></span>
    - <span data-ttu-id="66492-119">Windows 10 versão 1709 ou posterior</span><span class="sxs-lookup"><span data-stu-id="66492-119">Windows 10 version 1709 or later</span></span>
    - <span data-ttu-id="66492-120">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="66492-120">Windows 8.1</span></span>
    - <span data-ttu-id="66492-121">Windows 7</span><span class="sxs-lookup"><span data-stu-id="66492-121">Windows 7</span></span>



## <a name="redirection-experience"></a><span data-ttu-id="66492-122">Experiência de redirecionamento</span><span class="sxs-lookup"><span data-stu-id="66492-122">Redirection experience</span></span>

<span data-ttu-id="66492-123">No redirecionamento para o Microsoft Edge, os usuários veem uma única vez a caixa de diálogo na próxima captura de tela.</span><span class="sxs-lookup"><span data-stu-id="66492-123">On redirection to Microsoft Edge, users are shown the one-time dialog in the next screenshot.</span></span> <span data-ttu-id="66492-124">Este diálogo explica porque eles estão sendo redirecionados e solicita o consentimento para copiar seus dados de navegação e preferências do Internet Explorer para o Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="66492-124">This dialog explains why they're getting redirected and prompts for consent to copy their browsing data and preferences from Internet Explorer to Microsoft Edge.</span></span> <span data-ttu-id="66492-125">Os seguintes dados de navegação serão importados: Favoritos, senhas, mecanismos de busca, guias abertas, histórico, configurações, cookies e a Página Inicial.</span><span class="sxs-lookup"><span data-stu-id="66492-125">The following browsing data will be imported: Favorites, Passwords, Search engines, open tabs, History, settings, cookies, and the Home Page.</span></span>

![Notificação de navegação e solicitação de importação de dados e preferências.](media/edge-learnmore-neededge/neededge-dialog1.png)

<span data-ttu-id="66492-127">Mesmo não dando seu consentimento ao marcar "Sempre traga meus dados de navegação e preferências do Internet Explorer", eles podem clicar em **Continuar navegação** para continuar sua sessão.</span><span class="sxs-lookup"><span data-stu-id="66492-127">Even if they don't give their consent by checking "Always bring over my browsing data and preferences from Internet Explorer", they can click **Continue browsing** to continue their session.</span></span>

<span data-ttu-id="66492-128">Finalmente, um banner de incompatibilidade do site, exibido na próxima captura de tela, aparece abaixo da barra de endereços para cada redirecionamento.</span><span class="sxs-lookup"><span data-stu-id="66492-128">Finally, a website incompatibility banner, shown in the next screenshot, appears below the address bar for every redirection.</span></span>

![Notificações sobre sites modernos e solicitações para definir o Microsoft Edge como navegador padrão ou para explorar o Microsoft Edge.](media/edge-learnmore-neededge/neededge-banner.png)

<span data-ttu-id="66492-130">O banner de incompatibilidade do site:</span><span class="sxs-lookup"><span data-stu-id="66492-130">The website incompatibility banner:</span></span>

- <span data-ttu-id="66492-131">incentiva o usuário a mudar para o Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="66492-131">encourages the user to switch to Microsoft Edge</span></span>
- <span data-ttu-id="66492-132">oferece para definir o Microsoft Edge como navegador padrão</span><span class="sxs-lookup"><span data-stu-id="66492-132">offers to make Microsoft Edge as the default browser</span></span>
- <span data-ttu-id="66492-133">dá ao usuário a opção de explorar o Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="66492-133">gives the user the option to explore Microsoft Edge</span></span>

<span data-ttu-id="66492-134">Quando um site é redirecionado do Internet Explorer para o Microsoft Edge, a guia do Internet Explorer que começou a carregar o site é fechada se não tiver nenhum conteúdo anterior.</span><span class="sxs-lookup"><span data-stu-id="66492-134">When a site is redirected from Internet Explorer to Microsoft Edge, the Internet Explorer tab that started loading the site is closed if it had no prior content.</span></span> <span data-ttu-id="66492-135">Caso contrário, a visualização da guia ativa vai para uma  página de  [suporte](https://support.microsoft.com/office/the-website-you-were-trying-to-reach-doesn-t-work-with-internet-explorer-8f5fc675-cd47-414c-9535-12821ddfc554?ui=en-US&rs=en-US&ad=US) da Microsoft que explica por que o site foi redirecionado para o Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="66492-135">Otherwise, the active tab view goes to a  Microsoft [support](https://support.microsoft.com/office/the-website-you-were-trying-to-reach-doesn-t-work-with-internet-explorer-8f5fc675-cd47-414c-9535-12821ddfc554?ui=en-US&rs=en-US&ad=US) page that explains why the site was redirected to Microsoft Edge.</span></span>

> [!NOTE]
> <span data-ttu-id="66492-136">Após o redirecionamento, os usuários podem voltar a usar o Internet Explorer para sites que não estão na lista de incompatibilidades do Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="66492-136">After a redirection users can go back to using Internet Explorer for sites that are not on the Internet Explorer incompatibility list.</span></span>  

## <a name="policies-to-configure-redirection-to-microsoft-edge"></a><span data-ttu-id="66492-137">Políticas de configuração do redirecionamento para o Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="66492-137">Policies to configure redirection to Microsoft Edge</span></span>

> [!NOTE]
> <span data-ttu-id="66492-138">Essas políticas estarão disponíveis como atualizações de arquivo ADMX em 26 de outubro de 2020 e no Intune em 9 de novembro de 2020.</span><span class="sxs-lookup"><span data-stu-id="66492-138">These policies will be available as ADMX file updates by October 26, 2020 and will be available in Intune by November 9, 2020.</span></span>

<span data-ttu-id="66492-139">Três políticas de grupo devem ser configuradas para permitir o redirecionamento automático para a Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="66492-139">Three group policies must be configured to enable automatic redirection to Microsoft Edge.</span></span> <span data-ttu-id="66492-140">Estas políticas são:</span><span class="sxs-lookup"><span data-stu-id="66492-140">These policies are:</span></span>

- <span data-ttu-id="66492-141">RedirectSitesFromInternetExplorerPreventBHOInstall</span><span class="sxs-lookup"><span data-stu-id="66492-141">RedirectSitesFromInternetExplorerPreventBHOInstall</span></span>
- <span data-ttu-id="66492-142">RedirectSitesFromInternetExplorerRedirectMode</span><span class="sxs-lookup"><span data-stu-id="66492-142">RedirectSitesFromInternetExplorerRedirectMode</span></span>
- <span data-ttu-id="66492-143">HideInternetExplorerRedirectUXForIncompatibleSitesEnabled</span><span class="sxs-lookup"><span data-stu-id="66492-143">HideInternetExplorerRedirectUXForIncompatibleSitesEnabled</span></span>

### <a name="policy-redirectsitesfrominternetexplorerpreventbhoinstall"></a><span data-ttu-id="66492-144">Política: RedirectSitesFromInternetExplorerPreventBHOInstall</span><span class="sxs-lookup"><span data-stu-id="66492-144">Policy: RedirectSitesFromInternetExplorerPreventBHOInstall</span></span>

<span data-ttu-id="66492-145">O redirecionamento do Internet Explorer para o Microsoft Edge requer um Objeto Auxiliar de Navegador do Internet Explorer (BHO) chamado "IEtoEdge BHO".</span><span class="sxs-lookup"><span data-stu-id="66492-145">Redirection from Internet Explorer to Microsoft Edge requires an Internet Explorer Browser Helper Object (BHO) named "IEtoEdge BHO".</span></span> <span data-ttu-id="66492-146">A política **RedirectSitesFromInternetExplorerPreventBHOInstall** controla se o BHO está ou não instalado.</span><span class="sxs-lookup"><span data-stu-id="66492-146">The **RedirectSitesFromInternetExplorerPreventBHOInstall** policy controls whether or not this BHO is installed.</span></span>  

- <span data-ttu-id="66492-147">Se você ativar esta política, o BHO necessário para o redirecionamento não será instalado e seus usuários continuarão a ver mensagens de incompatibilidade para certos sites no Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="66492-147">If you enable this policy, the BHO required for redirection will not be installed and your users will continue to see incompatibility messages for certain websites on Internet Explorer.</span></span> <span data-ttu-id="66492-148">Se o BHO já estiver instalado, ele será desinstalado na próxima vez em que o canal do Microsoft Edge Estável for atualizado.</span><span class="sxs-lookup"><span data-stu-id="66492-148">If the BHO is already installed, it will be uninstalled the next time the Microsoft Edge Stable channel is updated.</span></span>
- <span data-ttu-id="66492-149">Se você desativar ou não configurar esta política, o BHO será instalado.</span><span class="sxs-lookup"><span data-stu-id="66492-149">If you disable or don't configure this policy, the BHO will be installed.</span></span> <span data-ttu-id="66492-150">Este é o comportamento padrão.</span><span class="sxs-lookup"><span data-stu-id="66492-150">This is the default behavior.</span></span>

<span data-ttu-id="66492-151">Além de precisar do BHO, há uma dependência do **RedirectSitesFromInternetExplorerRedirectMode**, que precisa ser definida como "Redirecionar sites com base em sites compatíveis com sites" ou "Não Configurado".</span><span class="sxs-lookup"><span data-stu-id="66492-151">In addition to needing the BHO, there is a dependency on the **RedirectSitesFromInternetExplorerRedirectMode**, which needs to be set to "Redirect sites based on the incompatible sites sitelist" or "Not Configured".</span></span>

### <a name="policy-redirectsitesfrominternetexplorerredirectmode"></a><span data-ttu-id="66492-152">Política: RedirectSitesFromInternetExplorerRedirectMode</span><span class="sxs-lookup"><span data-stu-id="66492-152">Policy: RedirectSitesFromInternetExplorerRedirectMode</span></span>

 <span data-ttu-id="66492-153">Esta política corresponde à configuração do Microsoft Edge **Navegador padrão** "Permitir que o Internet Explorer abra sites no Microsoft Edge".</span><span class="sxs-lookup"><span data-stu-id="66492-153">This policy corresponds to the Microsoft Edge **Default browser** setting "Let Internet Explorer open sites in Microsoft Edge".</span></span> <span data-ttu-id="66492-154">Você pode acessar essa configuração indo para o URL *edge://settings/defaultbrowser*.</span><span class="sxs-lookup"><span data-stu-id="66492-154">You can access this setting by going to the *edge://settings/defaultbrowser* URL.</span></span>  

- <span data-ttu-id="66492-155">Se você não configurar esta política ou defini-la como "Sitelist", o Internet Explorer redirecionará os sites incompatíveis para o Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="66492-155">If you don't configure this policy or set it to "Sitelist", Internet Explorer will redirect incompatible sites to Microsoft Edge.</span></span> <span data-ttu-id="66492-156">Este é o comportamento padrão.</span><span class="sxs-lookup"><span data-stu-id="66492-156">This is the default behavior.</span></span>
- <span data-ttu-id="66492-157">Para desabilitar essa política, marque a **Habilitada** e, em seguida, na lista suspensa em opções: Redirecione sites incompatíveis do Internet Explorer para o Microsoft Edge, selecione **Desabilitar**.</span><span class="sxs-lookup"><span data-stu-id="66492-157">To disable this policy, select **Enabled** AND then in the dropdown under Options: Redirect incompatible sites from Internet Explorer to Microsoft Edge, select **Disable**.</span></span> <span data-ttu-id="66492-158">Nesse estado, os sites incompatíveis não serão redirecionados para o Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="66492-158">In this state, incompatible sites aren't redirected to Microsoft Edge.</span></span>

> [!NOTE]
> <span data-ttu-id="66492-159">Se estiver em um dispositivo pessoal que não é gerenciado pela sua organização, você verá outra configuração chamada "Permitir que sites sejam carregados no modo Internet Explorer" em **Compatibilidade com o Internet Explorer**.</span><span class="sxs-lookup"><span data-stu-id="66492-159">If you're on a personal device that isn't  managed by your organization, you'll see another setting named "Allow sites to be loaded in Internet Explorer mode" under **Internet Explorer compatibility**.</span></span>
>
><span data-ttu-id="66492-160">Se você estiver em um dispositivo associado ao domínio ou registrado no Mobile Device Management (MDM), não verá esta opção.</span><span class="sxs-lookup"><span data-stu-id="66492-160">If you're on a domain joined or Mobile Device Management (MDM) enrolled device, you won't see this option.</span></span>
>
> <span data-ttu-id="66492-161">Em vez disso, se você quiser permitir que seus usuários carreguem sites no modo Internet Explorer, você pode fazê-lo configurando a política [Permitir o Internet Explorer no modo teste](./microsoft-edge-policies.md#intranetredirectbehavior).</span><span class="sxs-lookup"><span data-stu-id="66492-161">Instead, if you want to let your users load sites in Internet Explorer mode, you can do so by configuring the policy [Allow Internet Explorer mode testing](./microsoft-edge-policies.md#intranetredirectbehavior).</span></span>

### <a name="policy-hideinternetexplorerredirectuxforincompatiblesitesenabled"></a><span data-ttu-id="66492-162">Política: HideInternetExplorerRedirectUXForIncompatibleSitesEnabled</span><span class="sxs-lookup"><span data-stu-id="66492-162">Policy: HideInternetExplorerRedirectUXForIncompatibleSitesEnabled</span></span>

<span data-ttu-id="66492-163">Esta política configura a experiência do usuário com o redirecionamento de sites incompatíveis para o Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="66492-163">This policy configures the user experience for incompatible site redirection to Microsoft Edge.</span></span>  

- <span data-ttu-id="66492-164">Se você ativar esta política, os usuários nunca verão a caixa de diálogo de redirecionamento e nem o banner de redirecionamento.</span><span class="sxs-lookup"><span data-stu-id="66492-164">If you enable this policy, users never see the one-time redirection dialog and the redirection banner.</span></span> <span data-ttu-id="66492-165">Nenhum dado do navegador ou preferências do usuário serão importados.</span><span class="sxs-lookup"><span data-stu-id="66492-165">No browser data or user preferences are imported.</span></span>
- <span data-ttu-id="66492-166">Se você desabilitar ou não configurar esta política, a caixa de diálogo de redirecionamento será exibida no primeiro redirecionamento e o banner de redirecionamento persistente será exibido nas sessões que começam com um redirecionamento.</span><span class="sxs-lookup"><span data-stu-id="66492-166">If you disable or don't configure this policy, the redirection dialog will be shown on the first redirection and the persistent redirection banner will be shown for sessions that start with a redirection.</span></span>

  > [!NOTE]
  > <span data-ttu-id="66492-167">Os dados de navegação do usuário serão importados sempre que o usuário encontrar um novo redirecionamento.</span><span class="sxs-lookup"><span data-stu-id="66492-167">User browsing data will be imported every time a user encounters a new redirection.</span></span> <span data-ttu-id="66492-168">Entretanto, isso só acontecerá se o usuário consentir a importação na caixa de diálogo de redirecionamento.</span><span class="sxs-lookup"><span data-stu-id="66492-168">However, this only happens if the user consented to the import on the one-time redirection dialog.</span></span>

## <a name="disable-redirection-to-microsoft-edge"></a><span data-ttu-id="66492-169">Desative o redirecionamento para o Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="66492-169">Disable redirection to Microsoft Edge</span></span>

<span data-ttu-id="66492-170">Se você quiser desativar o redirecionamento ANTES da atualização para o Microsoft Edge Estável versão 87, siga o seguinte passo:</span><span class="sxs-lookup"><span data-stu-id="66492-170">If you want to disable redirection BEFORE updating to Microsoft Edge Stable version 87, use the following step:</span></span>

1. <span data-ttu-id="66492-171">Defina a política **RedirectSitesFromInternetExplorerPreventBHOInstall** para **Habilitada**.</span><span class="sxs-lookup"><span data-stu-id="66492-171">Set the **RedirectSitesFromInternetExplorerPreventBHOInstall** policy to **Enabled**.</span></span>

<span data-ttu-id="66492-172">Se você quiser desativar o redirecionamento DEPOIS da atualização para o Microsoft Edge Estável versão 87, siga os seguintes passos:</span><span class="sxs-lookup"><span data-stu-id="66492-172">If you want to disable redirection AFTER updating to Microsoft Edge Stable version 87, use the following steps:</span></span>

1. <span data-ttu-id="66492-173">Defina a política **RedirectSitesFromInternetExplorerRedirectMode** para **Habilitado** E, em seguida, na lista suspensa em opções: Redirecione sites incompatíveis do Internet Explorer para o Microsoft Edge, selecione **Desabilitar**.</span><span class="sxs-lookup"><span data-stu-id="66492-173">Set the **RedirectSitesFromInternetExplorerRedirectMode** policy to **Enabled** AND then in the dropdown under Options: Redirect incompatible sites from Internet Explorer to Microsoft Edge, select **Disable**.</span></span> <span data-ttu-id="66492-174">Esta configuração deixará de redirecionar assim que a política entrar em vigor.</span><span class="sxs-lookup"><span data-stu-id="66492-174">This setting will stop redirecting as soon as the policy takes effect.</span></span>
2. <span data-ttu-id="66492-175">Defina a política **RedirectSitesFromInternetExplorerPreventBHOInstall** para **Habilitada**.</span><span class="sxs-lookup"><span data-stu-id="66492-175">Set the **RedirectSitesFromInternetExplorerPreventBHOInstall** policy to **Enabled**.</span></span> <span data-ttu-id="66492-176">Isto vai desinstalar o BHO depois da próxima atualização do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="66492-176">This will uninstall the BHO after the next Microsoft Edge update.</span></span>

## <a name="see-also"></a><span data-ttu-id="66492-177">Consulte também</span><span class="sxs-lookup"><span data-stu-id="66492-177">See also</span></span>

- [<span data-ttu-id="66492-178">Solicitar atualizações à lista de sites incompatíveis</span><span class="sxs-lookup"><span data-stu-id="66492-178">Request updates to the incompatible sites list</span></span>](/microsoft-edge/web-platform/ie-to-microsoft-edge-redirection#request-an-update-to-the-ie-compatibility-list)
- [<span data-ttu-id="66492-179">Página de destino do Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="66492-179">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="66492-180">Políticas do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="66492-180">Microsoft Edge Policies</span></span>](./microsoft-edge-policies.md)