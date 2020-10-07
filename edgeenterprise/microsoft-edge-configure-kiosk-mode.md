---
title: Configurar o modo de quiosque do Microsoft Edge
ms.author: aguta
author: aguta
manager: srugh
ms.date: 10/05/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Configurar o modo de quiosque do Microsoft Edge
ms.openlocfilehash: 799b3dd4b7fc96f0b8e5cb718bca98fd4f38ec15
ms.sourcegitcommit: 78905f66f4a6590a57c8f2bf808af92106b62996
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/05/2020
ms.locfileid: "11094858"
---
# <span data-ttu-id="4a665-103">Configurar o modo de quiosque do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="4a665-103">Configure Microsoft Edge kiosk mode</span></span>

<span data-ttu-id="4a665-104">Este artigo descreve como configurar as opções do modo de quiosque do Microsoft Edge que você pode realizar no piloto.</span><span class="sxs-lookup"><span data-stu-id="4a665-104">This article describes how to configure Microsoft Edge kiosk mode options that you can pilot.</span></span> <span data-ttu-id="4a665-105">Há também um roteiro de recursos que temos como alvo.</span><span class="sxs-lookup"><span data-stu-id="4a665-105">There's also a roadmap of features we are targeting.</span></span>

> [!NOTE]
> <span data-ttu-id="4a665-106">Este artigo se aplica ao Microsoft Edge versão 87 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="4a665-106">This article applies to Microsoft Edge version 87 or later.</span></span>

## <span data-ttu-id="4a665-107">Visão geral</span><span class="sxs-lookup"><span data-stu-id="4a665-107">Overview</span></span>

<span data-ttu-id="4a665-108">O modo de quiosque do Microsoft Edge oferece duas experiências de bloqueio do navegador, para que as organizações possam criar, gerenciar e oferecer a melhor experiência para seus clientes.</span><span class="sxs-lookup"><span data-stu-id="4a665-108">Microsoft Edge kiosk mode offers two lockdown experiences of the browser so organizations can create, manage, and provide the best experience for their customers.</span></span> <span data-ttu-id="4a665-109">As seguintes experiências de bloqueio estão disponíveis:</span><span class="sxs-lookup"><span data-stu-id="4a665-109">The following lockdown experiences are available:</span></span>  

- <span data-ttu-id="4a665-110">A experiência de sinalização digital/interativa exibe um site específico no modo de tela inteira.</span><span class="sxs-lookup"><span data-stu-id="4a665-110">The Digital/Interactive signage experience displays a specific site in full-screen mode.</span></span>
- <span data-ttu-id="4a665-111">A experiência de navegação pública executa uma versão de várias guias no Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="4a665-111">The public-browsing experience runs a limited multi-tab version of Microsoft Edge.</span></span>

<span data-ttu-id="4a665-112">As duas experiências estão executando uma sessão Microsoft Edge InPrivate, que protege os dados do usuário.</span><span class="sxs-lookup"><span data-stu-id="4a665-112">Both experiences are running a Microsoft Edge InPrivate session, which protects user data.</span></span>

## <span data-ttu-id="4a665-113">Configurar o modo de quiosque do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="4a665-113">Set up Microsoft Edge kiosk mode</span></span>

<span data-ttu-id="4a665-114">Um conjunto inicial de recursos de modo de quiosque já está disponível para teste com o Microsoft Edge Canary Channel, versão 87.</span><span class="sxs-lookup"><span data-stu-id="4a665-114">An initial set of kiosk mode features are now available to test with Microsoft Edge Canary Channel, version 87.</span></span> <span data-ttu-id="4a665-115">Você pode baixar o Microsoft Edge Canary na página do [Microsoft Edge Insider Channels](https://www.microsoftedgeinsider.com/download).</span><span class="sxs-lookup"><span data-stu-id="4a665-115">You can download Microsoft Edge Canary from the [Microsoft Edge Insider Channels](https://www.microsoftedgeinsider.com/download) page.</span></span>

### <span data-ttu-id="4a665-116">Recursos do modo de quiosque</span><span class="sxs-lookup"><span data-stu-id="4a665-116">Kiosk mode features</span></span>

<span data-ttu-id="4a665-117">Os seguintes recursos estão disponíveis:</span><span class="sxs-lookup"><span data-stu-id="4a665-117">The following features are available:</span></span>

- <span data-ttu-id="4a665-118">A navegação InPrivate protege os dados do usuário excluindo os dados e os downloads do navegador quando a sessão termina.</span><span class="sxs-lookup"><span data-stu-id="4a665-118">InPrivate navigation protects user data by deleting browser data and downloads when the session ends.</span></span>
- <span data-ttu-id="4a665-119">Política para configurar Excluir downloads ao sair.</span><span class="sxs-lookup"><span data-stu-id="4a665-119">A policy to configure Delete downloads on exit.</span></span>
- <span data-ttu-id="4a665-120">A opção de redefinir a sessão de usuário após determinado período de inatividade.</span><span class="sxs-lookup"><span data-stu-id="4a665-120">The option to reset a user session after a certain period of inactivity.</span></span>
- <span data-ttu-id="4a665-121">Conjunto inicial de funcionalidade de bloqueio.</span><span class="sxs-lookup"><span data-stu-id="4a665-121">An initial set of lockdown functionality.</span></span> <span data-ttu-id="4a665-122">As funções a seguir estão disponíveis:</span><span class="sxs-lookup"><span data-stu-id="4a665-122">The following functions are available:</span></span>

  - <span data-ttu-id="4a665-123">Menu de contexto do mouse</span><span class="sxs-lookup"><span data-stu-id="4a665-123">Mouse context menu</span></span>
  - <span data-ttu-id="4a665-124">F12 Ferramentas de desenvolvedor</span><span class="sxs-lookup"><span data-stu-id="4a665-124">F12 Developer Tools</span></span>
  - <span data-ttu-id="4a665-125">F11 Sair da tela inteira (enquanto estiver no modo de tela inteira)</span><span class="sxs-lookup"><span data-stu-id="4a665-125">F11 Exit full screen (while in full screen mode)</span></span>
  - <span data-ttu-id="4a665-126">Bloqueio do conjunto inicial de páginas *Edge://*</span><span class="sxs-lookup"><span data-stu-id="4a665-126">Blocking of the initial set of *Edge://* pages</span></span>

> [!NOTE]
> <span data-ttu-id="4a665-127">À medida que o modo de quiosque evolui, mais recursos estarão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="4a665-127">As kiosk mode evolves, more features will be available.</span></span>

## <span data-ttu-id="4a665-128">Usar recursos do modo de quiosque</span><span class="sxs-lookup"><span data-stu-id="4a665-128">Use kiosk mode features</span></span>

<span data-ttu-id="4a665-129">Você pode invocar os recursos do modo de quiosque do Microsoft Edge com as seguintes opções de linha de comando do Windows 10:</span><span class="sxs-lookup"><span data-stu-id="4a665-129">You can invoke Microsoft Edge kiosk mode features can be invoked with the following Windows 10 command line options:</span></span>

- <span data-ttu-id="4a665-130">Sinalização interativa/digital do modo de quiosque:</span><span class="sxs-lookup"><span data-stu-id="4a665-130">Kiosk mode Digital/Interactive signage:</span></span> `msedge.exe --kiosk www.contoso.com --edge-kiosk-type=fullscreen`
- <span data-ttu-id="4a665-131">Navegação pública modo de quiosque:</span><span class="sxs-lookup"><span data-stu-id="4a665-131">Kiosk mode public browsing:</span></span> `msedge.exe --kiosk www.contoso.com --edge-kiosk-type=public-browsing`

### <span data-ttu-id="4a665-132">Opções de linha de comando adicionais</span><span class="sxs-lookup"><span data-stu-id="4a665-132">Additional command line options</span></span>

- `--no-first-run` <span data-ttu-id="4a665-133">: Desabilite a primeira experiência de execução do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="4a665-133">: Disable the first Microsoft Edge run experience.</span></span>
- `--kiosk-idle-timeout-minutes` <span data-ttu-id="4a665-134">: Altere o tempo (em minutos) da última atividade de usuário antes que o modo de quiosque do Microsoft Edge redefina a sessão do usuário.</span><span class="sxs-lookup"><span data-stu-id="4a665-134">: Change the time (in minutes) from the last user activity before Microsoft Edge kiosk mode resets the user's session.</span></span> <span data-ttu-id="4a665-135">Os seguintes valores são válidos:</span><span class="sxs-lookup"><span data-stu-id="4a665-135">The following values are supported:</span></span>

  - <span data-ttu-id="4a665-136">Valores padrão</span><span class="sxs-lookup"><span data-stu-id="4a665-136">Default values</span></span>
    - <span data-ttu-id="4a665-137">Tela cheia - desativado</span><span class="sxs-lookup"><span data-stu-id="4a665-137">Full screen - turned off</span></span>
    - <span data-ttu-id="4a665-138">Navegação pública - 5 minutos</span><span class="sxs-lookup"><span data-stu-id="4a665-138">Public browsing - 5 minutes</span></span>
  - <span data-ttu-id="4a665-139">Valores permitidos</span><span class="sxs-lookup"><span data-stu-id="4a665-139">Allowed values</span></span>
    - <span data-ttu-id="4a665-140">0 - desativa o cronômetro</span><span class="sxs-lookup"><span data-stu-id="4a665-140">0 - turns off the timer</span></span>
    - <span data-ttu-id="4a665-141">1-1440 minutos para redefinição no timer de ociosidade</span><span class="sxs-lookup"><span data-stu-id="4a665-141">1-1440 minutes for reset on idle timer</span></span>

## <span data-ttu-id="4a665-142">Microsoft Edge com acesso atribuído</span><span class="sxs-lookup"><span data-stu-id="4a665-142">Microsoft Edge with assigned access</span></span>

### <span data-ttu-id="4a665-143">Quiosque de aplicativos único</span><span class="sxs-lookup"><span data-stu-id="4a665-143">Single app kiosk</span></span>

<span data-ttu-id="4a665-144">No momento, o Microsoft Edge tem suporte para um subconjunto de tipos de modo quiosque da Versão Prévia do Microsoft Edge para acesso atribuído a um aplicativo único com as seguintes experiências de bloqueio: com a Navegação Digital/Interativa e pública.</span><span class="sxs-lookup"><span data-stu-id="4a665-144">Microsoft Edge currently supports a subset of the same Microsoft Edge Legacy kiosk mode types for single-app assigned access with the following lockdown experiences, Digital/Interactive signage and Public-browsing.</span></span>  

<span data-ttu-id="4a665-145">O modo de quiosque do Microsoft Edge com acesso atribuído está disponível atualmente para teste com a versão mais recente do  [Windows 10 Insider Preview](https://insider.windows.com/), versão 20215 ou superior e com o  [Canal Microsoft Edge Dev](https://www.microsoftedgeinsider.com/download), versão 87.0.644.4 ou superior.</span><span class="sxs-lookup"><span data-stu-id="4a665-145">Kiosk mode with assigned access is currently available for testing with the latest [Windows 10 Insider Preview Build](https://insider.windows.com/), version 20215 or higher, and with the [Microsoft Edge Dev Channel](https://www.microsoftedgeinsider.com/download), version 87.0.644.4 or higher.</span></span>

**<span data-ttu-id="4a665-146">Como faço para obter a visualização do Windows Insiders?</span><span class="sxs-lookup"><span data-stu-id="4a665-146">How do I get the Windows Insiders preview?</span></span>**

<span data-ttu-id="4a665-147">Para instalar uma versão do Windows 10 Insider Preview Build em um computador, siga as instruções em  [Introdução às Compilações do Windows 10 Insider Preview](https://docs.microsoft.com/windows-insider/get-started).</span><span class="sxs-lookup"><span data-stu-id="4a665-147">To install a Windows 10 Insider Preview Build on a PC, follow the instructions in [Getting started with Windows 10 Insider Preview Builds](https://docs.microsoft.com/windows-insider/get-started).</span></span>

### <span data-ttu-id="4a665-148">Quiosque de vários aplicativos</span><span class="sxs-lookup"><span data-stu-id="4a665-148">Multi-app kiosk</span></span>

<span data-ttu-id="4a665-149">O Microsoft Edge pode ser executado com [acesso atribuído a vários aplicativos](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps) no Windows 10, que é o equivalente ao tipo de modo de quiosque "Navegação Normal" da Versão Herdada do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="4a665-149">Microsoft Edge can be run with [multi-app assigned access](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps) on Windows 10, which is the equivalent of Microsoft Edge Legacy "Normal browsing" kiosk mode type.</span></span> <span data-ttu-id="4a665-150">Para configurar o Microsoft Edge com acesso atribuído a vários aplicativos, siga as instruções sobre como [Configurar um quiosque para vários aplicativos](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps).</span><span class="sxs-lookup"><span data-stu-id="4a665-150">To configure Microsoft Edge with multi-app assigned access follow the instructions on how to [Set up a multi-app kiosk](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps).</span></span> <span data-ttu-id="4a665-151">(O AUMID para o canal Estável do Microsoft Edge é **MSEdge**).</span><span class="sxs-lookup"><span data-stu-id="4a665-151">(The AUMID for the Microsoft Edge Stable channel is **MSEdge**).</span></span>

<span data-ttu-id="4a665-152">Ao usar o Microsoft Edge com acesso atribuído a vários aplicativos, você poderá usar as [políticas de navegador do Microsoft Edge](https://review.docs.microsoft.com/en-us/DeployEdge/microsoft-edge-policies) para configurar a experiência de navegação para atender aos seus requisitos exclusivos.</span><span class="sxs-lookup"><span data-stu-id="4a665-152">Configure Microsoft Edge kiosk mode When using Microsoft Edge with multi-app assigned access you can use the [Microsoft Edge browser policies](https://review.docs.microsoft.com/en-us/DeployEdge/microsoft-edge-policies) to configure the browsing experience to meet your unique requirements.</span></span>

### <span data-ttu-id="4a665-153">Configurar usando as configurações do Windows</span><span class="sxs-lookup"><span data-stu-id="4a665-153">Configure using Windows Settings</span></span>

<span data-ttu-id="4a665-154">As Configurações do Windows é a maneira mais simples de configurar um ou mais dispositivos em modo de quiosque de aplicativo único.</span><span class="sxs-lookup"><span data-stu-id="4a665-154">Windows Settings is the simplest way to set up one or two single-app kiosk devices.</span></span> <span data-ttu-id="4a665-155">Use as etapas a seguir para configurar um computador em modo de quiosque de aplicativo único.</span><span class="sxs-lookup"><span data-stu-id="4a665-155">Use the following steps to set up a single-app kiosk computer.</span></span>

1. <span data-ttu-id="4a665-156">Instale a versão do Windows 10 Insider Preview mais recente, versão 20215 ou superior.</span><span class="sxs-lookup"><span data-stu-id="4a665-156">Install the latest Windows 10 Insider Preview, version 20215 or higher.</span></span> <span data-ttu-id="4a665-157">Siga as instruções em [Introdução ao Windows 10 Insider Preview Builds](https://docs.microsoft.com/windows-insider/get-started).</span><span class="sxs-lookup"><span data-stu-id="4a665-157">Follow the instructions in [Getting started with Windows 10 Insider Preview Builds](https://docs.microsoft.com/windows-insider/get-started).</span></span>
2. <span data-ttu-id="4a665-158">Instale a versão mais recente do [Canal Microsoft Edge Dev](https://www.microsoftedgeinsider.com/download), 87.0.644.4 ou superior.</span><span class="sxs-lookup"><span data-stu-id="4a665-158">Install the latest version of [Microsoft Edge Dev channel](https://www.microsoftedgeinsider.com/download), 87.0.644.4 or higher.</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="4a665-159">Como é necessária uma instalação no nível do dispositivo, só há suporte para um canal que não seja Canary.</span><span class="sxs-lookup"><span data-stu-id="4a665-159">Because a device level installation is required, only a non-Canary channel is supported.</span></span>

3. <span data-ttu-id="4a665-160">No computador modo de quiosque, abra as configurações do Windows e digite "modo de quiosque" no campo de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="4a665-160">On the kiosk computer, open Windows Settings, and type "kiosk" in the search field.</span></span> <span data-ttu-id="4a665-161">Selecione  **Configurar um modo de quiosque (acesso atribuído)**, mostrada na próxima captura de tela para abrir a caixa de diálogo para criar o modo de quiosque.</span><span class="sxs-lookup"><span data-stu-id="4a665-161">Select  **Set up a kiosk (assigned access)**, shown in the next screenshot to open the dialog for creating the kiosk.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-1-assigned-access.png" alt-text="Configurar o modo de quiosque com acesso atribuído":::

4. <span data-ttu-id="4a665-163">Na página **Configurar um modo de quiosque** , clique em  **Introdução**.</span><span class="sxs-lookup"><span data-stu-id="4a665-163">On the **Set up a kiosk** page, click **Get started**.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-2-get-started.png" alt-text="Configurar o modo de quiosque com acesso atribuído":::

5. <span data-ttu-id="4a665-165">Digite um nome para criar uma nova conta modo de quiosque ou escolha uma conta existente na lista suspensa preenchida e clique em  **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="4a665-165">Type a name to create a new kiosk account or choose an existing account from the populated dropdown list and then click **Next**.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-3-create-account.png" alt-text="Configurar o modo de quiosque com acesso atribuído":::

6. <span data-ttu-id="4a665-167">Na página **Escolher um aplicativo de modo de quiosque** , selecione **Microsoft Edge** e clique em  **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="4a665-167">On the **Choose a kiosk app** page, select **Microsoft Edge** and then click **Next**.</span></span>

   > [!NOTE]
   > <span data-ttu-id="4a665-168">Isso se aplica apenas ao Microsoft Edge Dev, Beta e a canais estáveis.</span><span class="sxs-lookup"><span data-stu-id="4a665-168">This only applies to Microsoft Edge Dev, Beta, and Stable channels.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-4-pick-app.png" alt-text="Configurar o modo de quiosque com acesso atribuído":::

7. <span data-ttu-id="4a665-170">Escolha uma das opções a seguir para exibir o Microsoft Edge na execução no modo de quiosque:</span><span class="sxs-lookup"><span data-stu-id="4a665-170">Pick one of the following options for how Microsoft Edge displays when running in kiosk mode:</span></span>

   - <span data-ttu-id="4a665-171">Sinalização digital/interativa - Exibe um site específico no modo de tela inteira executando o Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="4a665-171">Digital/Interactive signage - Displays a specific site in full-screen mode, running Microsoft Edge.</span></span>
   - <span data-ttu-id="4a665-172">Navegador público - Executa uma versão limitada com várias guias do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="4a665-172">Public browser - Runs a limited multi-tab version of Microsoft Edge.</span></span>

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-5a-digital-sign.png" alt-text="Configurar o modo de quiosque com acesso atribuído":::

8. <span data-ttu-id="4a665-174">Selecione **Próximo**.</span><span class="sxs-lookup"><span data-stu-id="4a665-174">Select **Next**.</span></span>
9. <span data-ttu-id="4a665-175">Digite a URL a ser carregada quando o quiosque for iniciado.</span><span class="sxs-lookup"><span data-stu-id="4a665-175">Type the URL to load when the kiosk launches.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-6-enter-url.png" alt-text="Configurar o modo de quiosque com acesso atribuído":::

10. <span data-ttu-id="4a665-177">Aceite o valor padrão de 5 minutos para o tempo ocioso ou escolha um outro valor.</span><span class="sxs-lookup"><span data-stu-id="4a665-177">Accept the default value of 5 minutes for the idle time or provide a value of your own.</span></span>

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-7-enter-idle-time.png" alt-text="Configurar o modo de quiosque com acesso atribuído":::

11. <span data-ttu-id="4a665-179">Clique **Próximo**.</span><span class="sxs-lookup"><span data-stu-id="4a665-179">Click **Next**.</span></span>
12. <span data-ttu-id="4a665-180">Feche a janela de  **Configurações**  para salvar e aplicar suas opções.</span><span class="sxs-lookup"><span data-stu-id="4a665-180">Close the **Settings** window to save and apply your choices.</span></span>

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode--8-done.png" alt-text="Configurar o modo de quiosque com acesso atribuído":::

13. <span data-ttu-id="4a665-182">Reinicie o dispositivo de modo de quiosque e entre com a conta de modo de quiosque local para validar a configuração.</span><span class="sxs-lookup"><span data-stu-id="4a665-182">Sign off from the kiosk device and sign in with the local kiosk account to validate the configuration.</span></span>

## <span data-ttu-id="4a665-183">Limitações funcionais</span><span class="sxs-lookup"><span data-stu-id="4a665-183">Functional limitations</span></span>

<span data-ttu-id="4a665-184">Com o lançamento desta versão de visualização do modo de quiosque, continuamos a melhorar o produto e adicionar novos recursos.</span><span class="sxs-lookup"><span data-stu-id="4a665-184">With the release of this preview version of kiosk mode we're continuing work on improving the product and adding new features.</span></span>

<span data-ttu-id="4a665-185">Embora o modo de quiosque não ofereça suporte à funcionalidade a seguir, o trabalho está em andamento nos seguintes recursos:</span><span class="sxs-lookup"><span data-stu-id="4a665-185">Although kiosk mode doesn't currently support the following functionality, work is underway on the following features:</span></span>

- <span data-ttu-id="4a665-186">Coleções</span><span class="sxs-lookup"><span data-stu-id="4a665-186">Collections</span></span>
- <span data-ttu-id="4a665-187">Extensões</span><span class="sxs-lookup"><span data-stu-id="4a665-187">Extensions</span></span>
- <span data-ttu-id="4a665-188">Modo Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="4a665-188">Internet Explorer mode</span></span>
- <span data-ttu-id="4a665-189">Windows Defender Application Guard (WDAG)</span><span class="sxs-lookup"><span data-stu-id="4a665-189">Windows Defender Application Guard (WDAG)</span></span>

## <span data-ttu-id="4a665-190">Mapa</span><span class="sxs-lookup"><span data-stu-id="4a665-190">Roadmap</span></span>

### <span data-ttu-id="4a665-191">Ainda este ano (2020)</span><span class="sxs-lookup"><span data-stu-id="4a665-191">Later this year (2020)</span></span>

<span data-ttu-id="4a665-192">Incluiremos os seguintes recursos:</span><span class="sxs-lookup"><span data-stu-id="4a665-192">We'll add the following features:</span></span>

- <span data-ttu-id="4a665-193">Botão encerrar sessão</span><span class="sxs-lookup"><span data-stu-id="4a665-193">End session button</span></span>
- <span data-ttu-id="4a665-194">Barra de endereços somente leitura</span><span class="sxs-lookup"><span data-stu-id="4a665-194">Read only address bar</span></span>  
  - <span data-ttu-id="4a665-195">Configurável com a Política de Grupo</span><span class="sxs-lookup"><span data-stu-id="4a665-195">Configurable with group policy</span></span>
  - <span data-ttu-id="4a665-196">Quando habilitados, os usuários serão impedidos de editar a barra de endereços e navegar para outra página.</span><span class="sxs-lookup"><span data-stu-id="4a665-196">When enabled, users will be prevented from editing the address bar and navigating to another page.</span></span>

- <span data-ttu-id="4a665-197">Mais funções de bloqueio:</span><span class="sxs-lookup"><span data-stu-id="4a665-197">More lockdown functions:</span></span>

  - <span data-ttu-id="4a665-198">Aceleradores adicionais serão bloqueados (por exemplo, CTRL+N)</span><span class="sxs-lookup"><span data-stu-id="4a665-198">Additional accelerators will be blocked (for example, CTRL+N)</span></span>
  - <span data-ttu-id="4a665-199">O "..." menu configurações habilitará somente as opções necessárias (por exemplo, Imprimir, Ajuda, Comentários e Ler em voz alta)</span><span class="sxs-lookup"><span data-stu-id="4a665-199">The "…" settings menu will enable only required options (for example, Print, Help,  Feedback, and Read aloud)</span></span>
  - <span data-ttu-id="4a665-200">Bloqueio *edge://* adicional de páginas (por exemplo, *edge://settings*)</span><span class="sxs-lookup"><span data-stu-id="4a665-200">Additional *edge://* pages lockdown (for example, *edge://settings*)</span></span>
  - <span data-ttu-id="4a665-201">Configurar opções de impressão, IU</span><span class="sxs-lookup"><span data-stu-id="4a665-201">Configure print options UI</span></span>
  - <span data-ttu-id="4a665-202">Limitando o explorador de arquivos apenas à pasta de download.</span><span class="sxs-lookup"><span data-stu-id="4a665-202">Limiting file explorer to the download folder only.</span></span>

### <span data-ttu-id="4a665-203">No início de 2021</span><span class="sxs-lookup"><span data-stu-id="4a665-203">In early 2021</span></span>

<span data-ttu-id="4a665-204">Incluiremos os seguintes recursos e suporte:</span><span class="sxs-lookup"><span data-stu-id="4a665-204">We'll add the following support and features:</span></span>

- <span data-ttu-id="4a665-205">Disponibilidade geral do modo de quiosque do Microsoft Edge com acesso atribuído a um único aplicativo no Windows.</span><span class="sxs-lookup"><span data-stu-id="4a665-205">General availability of Microsoft Edge kiosk mode with assigned access single app on Windows.</span></span>
- <span data-ttu-id="4a665-206">Recursos adicionais para a paridade com a Versão Prévia do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="4a665-206">Additional features for parity with Microsoft Edge Legacy.</span></span>
- <span data-ttu-id="4a665-207">Integração com o Intune para configurar os dispositivos usando o Profile UX do modo de quiosque.</span><span class="sxs-lookup"><span data-stu-id="4a665-207">Integration with Intune to configure devices using kiosk mode profile UX.</span></span>

## <span data-ttu-id="4a665-208">Consulte também</span><span class="sxs-lookup"><span data-stu-id="4a665-208">See also</span></span>

- [<span data-ttu-id="4a665-209">Configurar quiosques e sinalizações digitais em edições do Windows desktop</span><span class="sxs-lookup"><span data-stu-id="4a665-209">Configure kiosks and digital signs on Windows desktop editions</span></span>](https://docs.microsoft.com/windows/configuration/kiosk-methods)
- [<span data-ttu-id="4a665-210">Implantar o modo de quiosque da Versão Herdada do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="4a665-210">Deploy Microsoft Edge Legacy kiosk mode</span></span>](https://aka.ms/edgekioskmode)
- [<span data-ttu-id="4a665-211">Planejar sua implantação do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="4a665-211">Plan your deployment of Microsoft Edge</span></span>](deploy-edge-plan-deployment.md)
- [<span data-ttu-id="4a665-212">Página de aterrissagem do Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="4a665-212">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
