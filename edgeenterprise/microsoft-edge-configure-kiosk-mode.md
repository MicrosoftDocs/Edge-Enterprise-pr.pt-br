---
title: Configurar o modo de quiosque do Microsoft Edge
ms.author: aguta
author: aguta
manager: srugh
ms.date: 09/22/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Configurar o modo de quiosque do Microsoft Edge
ms.openlocfilehash: d7c9df82079f8343d43ccfd312623e6e01358fa9
ms.sourcegitcommit: 858227653fc89532d1d274735f53280e27b2a8c0
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/22/2020
ms.locfileid: "11072638"
---
# <span data-ttu-id="ff4a3-103">Configurar o modo de quiosque do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="ff4a3-103">Configure Microsoft Edge kiosk mode</span></span>

<span data-ttu-id="ff4a3-104">Este artigo descreve como configurar as opções do modo de quiosque do Microsoft Edge que você pode realizar no piloto.</span><span class="sxs-lookup"><span data-stu-id="ff4a3-104">This article describes how to configure Microsoft Edge kiosk mode options that you can pilot.</span></span> <span data-ttu-id="ff4a3-105">Há também um roteiro de recursos que temos como alvo.</span><span class="sxs-lookup"><span data-stu-id="ff4a3-105">There's also a roadmap of features we are targeting.</span></span>

> [!NOTE]
> <span data-ttu-id="ff4a3-106">Este artigo se aplica ao Microsoft Edge versão 87 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="ff4a3-106">This article applies to Microsoft Edge version 87 or later.</span></span>

<span data-ttu-id="ff4a3-107">Para obter informações sobre o modo de quiosque da Versão Herdada do Microsoft Edge (versão 45 e anteriores), consulte [Implantar o modo de quiosque do Microsoft Edge](https://aka.ms/edgekioskmode).</span><span class="sxs-lookup"><span data-stu-id="ff4a3-107">For information about Microsoft Edge Legacy kiosk mode (version 45 and earlier) see [Deploy Microsoft Edge kiosk mode](https://aka.ms/edgekioskmode).</span></span>

## <span data-ttu-id="ff4a3-108">Visão geral</span><span class="sxs-lookup"><span data-stu-id="ff4a3-108">Overview</span></span>

<span data-ttu-id="ff4a3-109">O modo de quiosque do Microsoft Edge oferece duas experiências de bloqueio do navegador, para que as organizações possam criar, gerenciar e oferecer a melhor experiência para seus clientes.</span><span class="sxs-lookup"><span data-stu-id="ff4a3-109">Microsoft Edge kiosk mode offers two lockdown experiences of the browser so organizations can create, manage, and provide the best experience for their customers.</span></span> <span data-ttu-id="ff4a3-110">As seguintes experiências de bloqueio estão disponíveis:</span><span class="sxs-lookup"><span data-stu-id="ff4a3-110">The following lockdown experiences are available:</span></span>  

- <span data-ttu-id="ff4a3-111">A experiência de sinalização digital/interativa exibe um site específico no modo de tela inteira.</span><span class="sxs-lookup"><span data-stu-id="ff4a3-111">The Digital/Interactive signage experience displays a specific site in full-screen mode.</span></span>
- <span data-ttu-id="ff4a3-112">A experiência de navegação pública executa uma versão de várias guias no Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ff4a3-112">The public-browsing experience runs a limited multi-tab version of Microsoft Edge.</span></span>

<span data-ttu-id="ff4a3-113">As duas experiências estão executando uma sessão Microsoft Edge InPrivate, que protege os dados do usuário.</span><span class="sxs-lookup"><span data-stu-id="ff4a3-113">Both experiences are running a Microsoft Edge InPrivate session, which protects user data.</span></span>

## <span data-ttu-id="ff4a3-114">Configurar o modo de quiosque do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="ff4a3-114">Set up Microsoft Edge kiosk mode</span></span>  

<span data-ttu-id="ff4a3-115">Um conjunto inicial de recursos de modo de quiosque já está disponível para teste com o Microsoft Edge Canary Channel, versão 87.</span><span class="sxs-lookup"><span data-stu-id="ff4a3-115">An initial set of kiosk mode features are now available to test with Microsoft Edge Canary Channel, version 87.</span></span> <span data-ttu-id="ff4a3-116">Você pode baixar o Microsoft Edge Canary na página do [Microsoft Edge Insider Channels](https://www.microsoftedgeinsider.com/download).</span><span class="sxs-lookup"><span data-stu-id="ff4a3-116">You can download Microsoft Edge Canary from the [Microsoft Edge Insider Channels](https://www.microsoftedgeinsider.com/download) page.</span></span>

### <span data-ttu-id="ff4a3-117">Recursos do modo de quiosque</span><span class="sxs-lookup"><span data-stu-id="ff4a3-117">Kiosk mode features</span></span>

<span data-ttu-id="ff4a3-118">Os seguintes recursos estão disponíveis:</span><span class="sxs-lookup"><span data-stu-id="ff4a3-118">The following features are available:</span></span>

- <span data-ttu-id="ff4a3-119">Navegação InPrivate.</span><span class="sxs-lookup"><span data-stu-id="ff4a3-119">InPrivate navigation.</span></span> <span data-ttu-id="ff4a3-120">Protege os dados do usuário excluindo os dados e os downloads do navegador quando a sessão termina.</span><span class="sxs-lookup"><span data-stu-id="ff4a3-120">Protects user data by deleting browser data and downloads when the session ends.</span></span>
- <span data-ttu-id="ff4a3-121">Política para configurar Excluir downloads ao sair.</span><span class="sxs-lookup"><span data-stu-id="ff4a3-121">Policy to configure Delete downloads on exit.</span></span>
- <span data-ttu-id="ff4a3-122">Redefinir a sessão de usuário após um determinado período de inatividade.</span><span class="sxs-lookup"><span data-stu-id="ff4a3-122">Reset user session after a certain period of inactivity.</span></span>
- <span data-ttu-id="ff4a3-123">Conjunto inicial de funcionalidade de bloqueio.</span><span class="sxs-lookup"><span data-stu-id="ff4a3-123">Initial set of lockdown functionality.</span></span> <span data-ttu-id="ff4a3-124">As funções a seguir estão disponíveis:</span><span class="sxs-lookup"><span data-stu-id="ff4a3-124">The following functions are available:</span></span>

  - <span data-ttu-id="ff4a3-125">Menu de contexto do mouse</span><span class="sxs-lookup"><span data-stu-id="ff4a3-125">Mouse context menu</span></span>
  - <span data-ttu-id="ff4a3-126">F12 Ferramentas de desenvolvedor</span><span class="sxs-lookup"><span data-stu-id="ff4a3-126">F12 Developer Tools</span></span>
  - <span data-ttu-id="ff4a3-127">F11 Sair da tela inteira (enquanto estiver no modo de tela inteira)</span><span class="sxs-lookup"><span data-stu-id="ff4a3-127">F11 Exit full screen (while in full screen mode)</span></span>
  - <span data-ttu-id="ff4a3-128">Bloqueio do conjunto inicial de páginas *Edge://*</span><span class="sxs-lookup"><span data-stu-id="ff4a3-128">Blocking of the initial set of *Edge://* pages</span></span>

> [!NOTE]
> <span data-ttu-id="ff4a3-129">À medida que o modo de quiosque evolui, mais recursos estarão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="ff4a3-129">As kiosk mode evolves, more features will be available.</span></span>

### <span data-ttu-id="ff4a3-130">Usar recursos do modo de quiosque</span><span class="sxs-lookup"><span data-stu-id="ff4a3-130">Use kiosk mode features</span></span>

<span data-ttu-id="ff4a3-131">Você pode invocar os recursos do modo de quiosque do Microsoft Edge com as seguintes opções de linha de comando do Windows 10:</span><span class="sxs-lookup"><span data-stu-id="ff4a3-131">You can invoke Microsoft Edge kiosk mode features can be invoked with the following Windows 10 command line options:</span></span>

- <span data-ttu-id="ff4a3-132">Sinalização interativa/digital do modo de quiosque:</span><span class="sxs-lookup"><span data-stu-id="ff4a3-132">Kiosk mode Digital/Interactive signage:</span></span> `msedge.exe --kiosk www.contoso.com --edge-kiosk-type=fullscreen`
- <span data-ttu-id="ff4a3-133">Navegação pública modo de quiosque:</span><span class="sxs-lookup"><span data-stu-id="ff4a3-133">Kiosk mode public browsing:</span></span> `msedge.exe --kiosk www.contoso.com --edge-kiosk-type=public-browsing`

#### <span data-ttu-id="ff4a3-134">Opções de linha de comando adicionais</span><span class="sxs-lookup"><span data-stu-id="ff4a3-134">Additional command line options</span></span>

- `--no-first-run` <span data-ttu-id="ff4a3-135">: Desabilite a primeira experiência de execução do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ff4a3-135">: Disable the first Microsoft Edge run experience.</span></span>
- `--kiosk-idle-timeout-minutes` <span data-ttu-id="ff4a3-136">: Altere o tempo (em minutos) da última atividade de usuário antes que o modo de quiosque do Microsoft Edge redefina a sessão do usuário.</span><span class="sxs-lookup"><span data-stu-id="ff4a3-136">: Change the time (in minutes) from the last user activity before Microsoft Edge kiosk mode resets the user's session.</span></span> <span data-ttu-id="ff4a3-137">Os seguintes valores são válidos:</span><span class="sxs-lookup"><span data-stu-id="ff4a3-137">The following values are supported:</span></span>

  - <span data-ttu-id="ff4a3-138">Valores padrão</span><span class="sxs-lookup"><span data-stu-id="ff4a3-138">Default values</span></span>
    - <span data-ttu-id="ff4a3-139">Tela cheia - desativado</span><span class="sxs-lookup"><span data-stu-id="ff4a3-139">Full screen - turned off</span></span>
    - <span data-ttu-id="ff4a3-140">Navegação pública - 5 minutos</span><span class="sxs-lookup"><span data-stu-id="ff4a3-140">Public browsing - 5 minutes</span></span>
  - <span data-ttu-id="ff4a3-141">Valores permitidos</span><span class="sxs-lookup"><span data-stu-id="ff4a3-141">Allowed values</span></span>
    - <span data-ttu-id="ff4a3-142">0 - desativa o cronômetro</span><span class="sxs-lookup"><span data-stu-id="ff4a3-142">0 - turns off the timer</span></span>
    - <span data-ttu-id="ff4a3-143">1-1440 minutos para redefinição no timer de ociosidade</span><span class="sxs-lookup"><span data-stu-id="ff4a3-143">1-1440 minutes for reset on idle timer</span></span>

## <span data-ttu-id="ff4a3-144">Configurar o modo de quiosque com acesso atribuído</span><span class="sxs-lookup"><span data-stu-id="ff4a3-144">Set up kiosk mode with assigned access</span></span>

<span data-ttu-id="ff4a3-145">O modo de quiosque do Microsoft Edge com acesso atribuído está disponível atualmente para teste com a versão mais recente do [Windows 10 Insider Preview](https://insider.windows.com/), versão 20215 ou superior e com o [Microsoft Edge Dev](https://www.microsoftedgeinsider.com/download), versão 87.0.644 ou superior.</span><span class="sxs-lookup"><span data-stu-id="ff4a3-145">Microsoft Edge kiosk mode with assigned access is currently available for testing with the latest [Windows 10 Insider Preview Build](https://insider.windows.com/), version 20215 or higher, and with the [Microsoft Edge Dev Channel](https://www.microsoftedgeinsider.com/download), version 87.0.644 or higher.</span></span>

**<span data-ttu-id="ff4a3-146">Como faço para obter a visualização do Windows Insiders?</span><span class="sxs-lookup"><span data-stu-id="ff4a3-146">How do I get the Windows Insiders preview?</span></span>**

<span data-ttu-id="ff4a3-147">Para instalar uma versão do Windows 10 Insider Preview Build em um computador, siga as instruções em [Introdução ao Windows 10 Insider Preview Builds](https://docs.microsoft.com/windows-insider/get-started).</span><span class="sxs-lookup"><span data-stu-id="ff4a3-147">To install a Windows 10 Insider Preview Build on a PC, follow the instructions in [Getting started with Windows 10 Insider Preview Builds](https://docs.microsoft.com/windows-insider/get-started).</span></span>

### <span data-ttu-id="ff4a3-148">Configurar usando as configurações do Windows</span><span class="sxs-lookup"><span data-stu-id="ff4a3-148">Configure using Windows Settings</span></span>

<span data-ttu-id="ff4a3-149">As Configurações do Windows é a maneira mais simples de configurar um ou mais dispositivos em modo de quiosque de aplicativo único.</span><span class="sxs-lookup"><span data-stu-id="ff4a3-149">Windows Settings is the simplest way to set up one or two single-app kiosk devices.</span></span> <span data-ttu-id="ff4a3-150">Use as etapas a seguir para configurar um computador em modo de quiosque de aplicativo único.</span><span class="sxs-lookup"><span data-stu-id="ff4a3-150">Use the following steps to set up a single-app kiosk computer.</span></span>

1. <span data-ttu-id="ff4a3-151">Instale a versão do Windows 10 Insider Preview mais recente, versão 20215 ou superior.</span><span class="sxs-lookup"><span data-stu-id="ff4a3-151">Install the latest Windows 10 Insider Preview, version 20215 or higher.</span></span> <span data-ttu-id="ff4a3-152">Siga as instruções em [Introdução ao Windows 10 Insider Preview Builds](https://docs.microsoft.com/windows-insider/get-started).</span><span class="sxs-lookup"><span data-stu-id="ff4a3-152">Follow the instructions in [Getting started with Windows 10 Insider Preview Builds](https://docs.microsoft.com/windows-insider/get-started).</span></span>
2. <span data-ttu-id="ff4a3-153">Instalar a versão mais recente do [canal Microsoft Edge Dev](https://www.microsoftedgeinsider.com/download), 87.0.644 ou superior.</span><span class="sxs-lookup"><span data-stu-id="ff4a3-153">Install the latest version of [Microsoft Edge Dev channel](https://www.microsoftedgeinsider.com/download), 87.0.644 or higher.</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="ff4a3-154">Como é necessária uma instalação no nível do dispositivo, só há suporte para um canal que não seja Canary.</span><span class="sxs-lookup"><span data-stu-id="ff4a3-154">Because a device level installation is required, only a non-Canary channel is supported.</span></span>

3. <span data-ttu-id="ff4a3-155">No computador modo de quiosque, abra as configurações do Windows e digite "modo de quiosque" no campo de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="ff4a3-155">On the kiosk computer, open Windows Settings, and type "kiosk" in the search field.</span></span> <span data-ttu-id="ff4a3-156">Selecione  **Configurar um modo de quiosque (acesso atribuído)**, mostrada na próxima captura de tela para abrir a caixa de diálogo para criar o modo de quiosque.</span><span class="sxs-lookup"><span data-stu-id="ff4a3-156">Select  **Set up a kiosk (assigned access)**, shown in the next screenshot to open the dialog for creating the kiosk.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-1-assigned-access.png" alt-text="Configurar o modo de quiosque com acesso atribuído":::

4. <span data-ttu-id="ff4a3-158">Na página **Configurar um modo de quiosque** , clique em  **Introdução**.</span><span class="sxs-lookup"><span data-stu-id="ff4a3-158">On the **Set up a kiosk** page, click **Get started**.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-2-get-started.png" alt-text="Página modo de quiosque – introdução":::

5. <span data-ttu-id="ff4a3-160">Digite um nome para criar uma nova conta modo de quiosque ou escolha uma conta existente na lista suspensa preenchida e clique em  **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="ff4a3-160">Type a name to create a new kiosk account or choose an existing account from the populated dropdown list and then click **Next**.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-3-create-account.png" alt-text="Modo de quiosque - criar conta":::

6. <span data-ttu-id="ff4a3-162">Na página **Escolher um aplicativo de modo de quiosque** , selecione **Microsoft Edge** e clique em  **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="ff4a3-162">On the **Choose a kiosk app** page, select **Microsoft Edge** and then click **Next**.</span></span>

   > [!NOTE]
   > <span data-ttu-id="ff4a3-163">Isso se aplica apenas ao Microsoft Edge Dev, Beta e a canais estáveis.</span><span class="sxs-lookup"><span data-stu-id="ff4a3-163">This only applies to Microsoft Edge Dev, Beta, and Stable channels.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-4-pick-app.png" alt-text="Modo de quiosque - escolha um aplicativo":::

7. <span data-ttu-id="ff4a3-165">Escolha uma das opções a seguir para exibir o Microsoft Edge na execução no modo de quiosque:</span><span class="sxs-lookup"><span data-stu-id="ff4a3-165">Pick one of the following options for how Microsoft Edge displays when running in kiosk mode:</span></span>

   - <span data-ttu-id="ff4a3-166">Sinalização digital/interativa - Exibe um site específico no modo de tela inteira executando o Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ff4a3-166">Digital/Interactive signage - Displays a specific site in full-screen mode, running Microsoft Edge.</span></span>
   - <span data-ttu-id="ff4a3-167">Navegador público - Executa uma versão limitada com várias guias do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ff4a3-167">Public browser - Runs a limited multi-tab version of Microsoft Edge.</span></span>

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-5a-digital-sign.png" alt-text="Exibição do modo quiosque – sinal digital de tela inteira":::

8. <span data-ttu-id="ff4a3-169">Selecione **Próximo**.</span><span class="sxs-lookup"><span data-stu-id="ff4a3-169">Select **Next**.</span></span>
9. <span data-ttu-id="ff4a3-170">Digite a URL a ser carregada quando o quiosque for iniciado.</span><span class="sxs-lookup"><span data-stu-id="ff4a3-170">Type the URL to load when the kiosk launches.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-6-enter-url.png" alt-text="Modo de quiosque - Inserir URL":::

10. <span data-ttu-id="ff4a3-172">Aceite o valor padrão de 5 minutos para o tempo ocioso ou escolha um outro valor.</span><span class="sxs-lookup"><span data-stu-id="ff4a3-172">Accept the default value of 5 minutes for the idle time or provide a value of your own.</span></span>

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-7-enter-idle-time.png" alt-text="Modo de quiosque - Inserir tempo ocioso":::

11. <span data-ttu-id="ff4a3-174">Clique **Próximo**.</span><span class="sxs-lookup"><span data-stu-id="ff4a3-174">Click **Next**.</span></span>
12. <span data-ttu-id="ff4a3-175">Feche a janela de  **Configurações**  para salvar e aplicar suas opções.</span><span class="sxs-lookup"><span data-stu-id="ff4a3-175">Close the **Settings** window to save and apply your choices.</span></span>

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode--8-done.png" alt-text="Modo de quiosque – concluir configuração":::

13. <span data-ttu-id="ff4a3-177">Reinicie o dispositivo de modo de quiosque e entre com a conta de modo de quiosque local para validar a configuração.</span><span class="sxs-lookup"><span data-stu-id="ff4a3-177">Sign off from the kiosk device and sign in with the local kiosk account to validate the configuration.</span></span>

## <span data-ttu-id="ff4a3-178">Limitações funcionais</span><span class="sxs-lookup"><span data-stu-id="ff4a3-178">Functional limitations</span></span>

<span data-ttu-id="ff4a3-179">Com o lançamento desta versão de visualização do modo de quiosque, continuamos a melhorar o produto e adicionar novos recursos.</span><span class="sxs-lookup"><span data-stu-id="ff4a3-179">With the release of this preview version of kiosk mode we're continuing work on improving the product and adding new features.</span></span>

<span data-ttu-id="ff4a3-180">Embora o modo de quiosque não ofereça suporte à funcionalidade a seguir, o trabalho está em andamento nos seguintes recursos:</span><span class="sxs-lookup"><span data-stu-id="ff4a3-180">Although kiosk mode doesn't currently support the following functionality, work is underway on the following features:</span></span>

- <span data-ttu-id="ff4a3-181">Coleções</span><span class="sxs-lookup"><span data-stu-id="ff4a3-181">Collections</span></span>
- <span data-ttu-id="ff4a3-182">Extensões</span><span class="sxs-lookup"><span data-stu-id="ff4a3-182">Extensions</span></span>
- <span data-ttu-id="ff4a3-183">Modo Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="ff4a3-183">Internet Explorer mode</span></span>
- <span data-ttu-id="ff4a3-184">Windows Defender Application Guard (WDAG)</span><span class="sxs-lookup"><span data-stu-id="ff4a3-184">Windows Defender Application Guard (WDAG)</span></span>

## <span data-ttu-id="ff4a3-185">Mapa</span><span class="sxs-lookup"><span data-stu-id="ff4a3-185">Roadmap</span></span>

### <span data-ttu-id="ff4a3-186">Ainda este ano (2020)</span><span class="sxs-lookup"><span data-stu-id="ff4a3-186">Later this year (2020)</span></span>

<span data-ttu-id="ff4a3-187">Incluiremos os seguintes recursos:</span><span class="sxs-lookup"><span data-stu-id="ff4a3-187">We'll add the following features:</span></span>

- <span data-ttu-id="ff4a3-188">Botão encerrar sessão</span><span class="sxs-lookup"><span data-stu-id="ff4a3-188">End session button</span></span>
- <span data-ttu-id="ff4a3-189">Barra de endereços da URL somente leitura</span><span class="sxs-lookup"><span data-stu-id="ff4a3-189">Read only URL address bar</span></span>  
  - <span data-ttu-id="ff4a3-190">Configurável com a Política de Grupo</span><span class="sxs-lookup"><span data-stu-id="ff4a3-190">Configurable with group policy</span></span>
  - <span data-ttu-id="ff4a3-191">Quando habilitados, os usuários serão impedidos de editar a URL da barra de endereços para experimentar a navegação para outra página.</span><span class="sxs-lookup"><span data-stu-id="ff4a3-191">When enabled, users will be prevented from editing the address bar URL to try navigating away to another page.</span></span>

- <span data-ttu-id="ff4a3-192">Mais funções de bloqueio:</span><span class="sxs-lookup"><span data-stu-id="ff4a3-192">More lockdown functions:</span></span>

  - <span data-ttu-id="ff4a3-193">Aceleradores adicionais serão bloqueados (por exemplo, CTRL+N)</span><span class="sxs-lookup"><span data-stu-id="ff4a3-193">Additional accelerators will be blocked (for example, CTRL+N)</span></span>
  - <span data-ttu-id="ff4a3-194">O "..." menu configurações habilitará somente as opções necessárias (por exemplo, Imprimir, Ajuda, Comentários e Ler em voz alta)</span><span class="sxs-lookup"><span data-stu-id="ff4a3-194">The "…" settings menu will enable only required options (for example, Print, Help,  Feedback, and Read aloud)</span></span>
  - <span data-ttu-id="ff4a3-195">Bloqueio *edge://* adicional de páginas (por exemplo, *edge://settings*)</span><span class="sxs-lookup"><span data-stu-id="ff4a3-195">Additional *edge://* pages lockdown (for example, *edge://settings*)</span></span>
  - <span data-ttu-id="ff4a3-196">Configurar opções de impressão, IU</span><span class="sxs-lookup"><span data-stu-id="ff4a3-196">Configure print options UI</span></span>
  - <span data-ttu-id="ff4a3-197">Limitando o explorador de arquivos apenas à pasta de download.</span><span class="sxs-lookup"><span data-stu-id="ff4a3-197">Limiting file explorer to the download folder only.</span></span>

### <span data-ttu-id="ff4a3-198">No início de 2021</span><span class="sxs-lookup"><span data-stu-id="ff4a3-198">In early 2021</span></span>

<span data-ttu-id="ff4a3-199">Incluiremos os seguintes recursos e suporte:</span><span class="sxs-lookup"><span data-stu-id="ff4a3-199">We'll add the following support and features:</span></span>

- <span data-ttu-id="ff4a3-200">Disponibilidade geral do modo de quiosque do Microsoft Edge com acesso atribuído a um único aplicativo no Windows.</span><span class="sxs-lookup"><span data-stu-id="ff4a3-200">General availability of Microsoft Edge kiosk mode with assigned access single app on Windows.</span></span>
- <span data-ttu-id="ff4a3-201">Recursos adicionais para a paridade com a Versão Prévia do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ff4a3-201">Additional features for parity with Microsoft Edge Legacy.</span></span>
- <span data-ttu-id="ff4a3-202">Integração com o Intune para configurar os dispositivos usando o Profile UX do modo de quiosque.</span><span class="sxs-lookup"><span data-stu-id="ff4a3-202">Integration with Intune to configure devices using kiosk mode profile UX.</span></span>

## <span data-ttu-id="ff4a3-203">Consulte também</span><span class="sxs-lookup"><span data-stu-id="ff4a3-203">See also</span></span>

- [<span data-ttu-id="ff4a3-204">Configurar quiosques e sinalizações digitais em edições do Windows desktop</span><span class="sxs-lookup"><span data-stu-id="ff4a3-204">Configure kiosks and digital signs on Windows desktop editions</span></span>](https://docs.microsoft.com/windows/configuration/kiosk-methods)
- [<span data-ttu-id="ff4a3-205">Implantar o modo de quiosque da Versão Herdada do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="ff4a3-205">Deploy Microsoft Edge Legacy kiosk mode</span></span>](https://aka.ms/edgekioskmode) 
- [<span data-ttu-id="ff4a3-206">Planejar sua implantação do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="ff4a3-206">Plan your deployment of Microsoft Edge</span></span>](deploy-edge-plan-deployment.md)
- [<span data-ttu-id="ff4a3-207">Página de aterrissagem do Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="ff4a3-207">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)