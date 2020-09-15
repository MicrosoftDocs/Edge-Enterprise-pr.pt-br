---
title: ClickOnce e DirectInvoke no Microsoft Edge
ms.author: kele
author: dan-wesley
manager: srugh
ms.date: 09/10/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Saiba mais sobre o ClickOnce e o DirectInvoke no Microsoft Edge.
ms.openlocfilehash: 1d4e08c0ce3ee2afec7968cd892f77ef7bdc3fff
ms.sourcegitcommit: 4c0b84b03e686a7a2989ce2187dbadf35418104a
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012791"
---
# <span data-ttu-id="d055a-103">Noções básicas sobre os recursos ClickOnce e DirectInvoke no Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="d055a-103">Understand the ClickOnce and DirectInvoke features in Microsoft Edge</span></span>

<span data-ttu-id="d055a-104">ClickOnce e DirectInvoke são recursos disponíveis no IE e no Microsoft Edge (versão 45 e anterior) que oferecem suporte ao uso de um manipulador de arquivos para baixar arquivos de um site.</span><span class="sxs-lookup"><span data-stu-id="d055a-104">ClickOnce and DirectInvoke are features available in IE and Microsoft Edge (version 45 and earlier) that support the use of a file handler to download files from a website.</span></span> <span data-ttu-id="d055a-105">Embora eles atendam a diferentes finalidades, os dois recursos permitem que sites especifiquem que um arquivo solicitado para download seja passado para um manipulador de arquivos no dispositivo do usuário.</span><span class="sxs-lookup"><span data-stu-id="d055a-105">Although they serve different purposes, both features let websites specify that a file requested for download is passed to a file handler on the user's device.</span></span> <span data-ttu-id="d055a-106">As solicitações do ClickOnce são manipuladas pelo manipulador de arquivos nativo no Windows.</span><span class="sxs-lookup"><span data-stu-id="d055a-106">ClickOnce requests are handled by the native file handler in Windows.</span></span> <span data-ttu-id="d055a-107">As solicitações do DirectInvoke são manipuladas por um manipulador de arquivos registrado pelo site que hospeda o arquivo.</span><span class="sxs-lookup"><span data-stu-id="d055a-107">DirectInvoke requests are handled by a registered file handler specified by the website hosting the file.</span></span>

<span data-ttu-id="d055a-108">Para obter mais informações sobre esses recursos, consulte:</span><span class="sxs-lookup"><span data-stu-id="d055a-108">For more information about these features, see:</span></span>

- [<span data-ttu-id="d055a-109">ClickOnce</span><span class="sxs-lookup"><span data-stu-id="d055a-109">ClickOnce</span></span>](https://docs.microsoft.com/visualstudio/deployment/clickonce-security-and-deployment?view=vs-2019)
- [<span data-ttu-id="d055a-110">DirectInvoke</span><span class="sxs-lookup"><span data-stu-id="d055a-110">DirectInvoke</span></span>]( https://technet.microsoft.com/learning/jj215788(v=vs.94).aspx)

> [!NOTE]
> <span data-ttu-id="d055a-111">Atualmente, o Chromium não oferece suporte nativo ao ClickOnce nem ao DirectInvoke.</span><span class="sxs-lookup"><span data-stu-id="d055a-111">Currently, Chromium doesn't provide native support for ClickOnce or DirectInvoke.</span></span>

## <span data-ttu-id="d055a-112">Visão geral: pré-requisitos e processo</span><span class="sxs-lookup"><span data-stu-id="d055a-112">Overview: prerequisites and process</span></span>

<span data-ttu-id="d055a-113">Para que o ClickOnce e o DirectInvoke funcionem conforme planejado e o manipulador de arquivos seja solicitado com êxito, o manipulador de arquivos deve ser registrado no sistema operacional como compatível com ClickOnce ou DirectInvoke.</span><span class="sxs-lookup"><span data-stu-id="d055a-113">For ClickOnce and DirectInvoke to work as designed and for the file handler to be successfully requested, the file handler must be registered to the operating system as supporting ClickOnce or DirectInvoke.</span></span> <span data-ttu-id="d055a-114">Geralmente, esse registro acontece quando o sistema operacional original é instalado ou quando um novo programa instalado solicita a capacidade de usar o DirectInvoke para atualizações.</span><span class="sxs-lookup"><span data-stu-id="d055a-114">This registration typically happens when the original operating system is installed or when a new program that's installed requests the ability to use DirectInvoke for updates.</span></span>

<span data-ttu-id="d055a-115">Quando um site recebe uma solicitação de download que requer o ClickOnce ou o DirectInvoke, ocorrem as seguintes ações:</span><span class="sxs-lookup"><span data-stu-id="d055a-115">When a website receives a download request that requires ClickOnce or DirectInvoke, the following actions happen:</span></span>

- <span data-ttu-id="d055a-116">O site solicita que o navegador use um manipulador de arquivos especificado.</span><span class="sxs-lookup"><span data-stu-id="d055a-116">The website requests that the browser use a specified file handler.</span></span>
- <span data-ttu-id="d055a-117">O navegador verifica o Registro do sistema operacional para confirmar se o manipulador de arquivos está registrado para o tipo de arquivo solicitado.</span><span class="sxs-lookup"><span data-stu-id="d055a-117">The browser checks the operating system registry to see if the file handler is registered for the requested file type.</span></span>
- <span data-ttu-id="d055a-118">Se o manipulador de arquivos estiver registrado, o navegador chamará o manipulador de arquivos e passará a URL como um argumento para o manipulador de arquivos.</span><span class="sxs-lookup"><span data-stu-id="d055a-118">If the file handler is registered, the browser calls the file handler and passes the URL as an argument to the file handler.</span></span>
- <span data-ttu-id="d055a-119">O manipulador de arquivos processa a URL e baixa o arquivo.</span><span class="sxs-lookup"><span data-stu-id="d055a-119">The file handler processes the URL and downloads the file.</span></span>

  > [!NOTE]
  > <span data-ttu-id="d055a-120">A URL é usada para determinar a origem do arquivo, bem como todos os parâmetros a serem usados ao acessar o arquivo.</span><span class="sxs-lookup"><span data-stu-id="d055a-120">The URL is used to determine the source of the file, as well as any parameters to use when accessing the file.</span></span>  <span data-ttu-id="d055a-121">Por exemplo: pontos de extremidade, manifesto ou metadados.</span><span class="sxs-lookup"><span data-stu-id="d055a-121">For example: endpoints, a manifest, or metadata.</span></span>

## <span data-ttu-id="d055a-122">Casos de uso</span><span class="sxs-lookup"><span data-stu-id="d055a-122">Use cases</span></span>

<span data-ttu-id="d055a-123">Os seguintes casos de uso são representativos.</span><span class="sxs-lookup"><span data-stu-id="d055a-123">The following use cases are representative.</span></span>

<span data-ttu-id="d055a-124">Você pode usar o ClickOnce para implantar e atualizar facilmente software em dispositivos com mínima interação do usuário.</span><span class="sxs-lookup"><span data-stu-id="d055a-124">You can use ClickOnce to easily deploy and update software on devices with minimal user interaction.</span></span> <span data-ttu-id="d055a-125">Os usuários podem instalar e executar um aplicativo do Windows clicando em um link em uma página da Web.</span><span class="sxs-lookup"><span data-stu-id="d055a-125">Users can install and run a Windows application by clicking a link in a web page.</span></span> <span data-ttu-id="d055a-126">Se configurado corretamente, o aplicativo ClickOnce pode instalar programas sem que os usuários definam configurações para o instalador.</span><span class="sxs-lookup"><span data-stu-id="d055a-126">If configured correctly, the ClickOnce application can install programs without having users set configurations for the installer.</span></span> <span data-ttu-id="d055a-127">Por exemplo, locais dos arquivos, quais opções instalar etc.</span><span class="sxs-lookup"><span data-stu-id="d055a-127">For example, file locations, what options to install, and so on.</span></span>

<span data-ttu-id="d055a-128">Os casos de uso do DirectInvoke dependem da intenção do site que está solicitando o DirectInvoke.</span><span class="sxs-lookup"><span data-stu-id="d055a-128">DirectInvoke use cases depend on the intent of the website requesting DirectInvoke.</span></span> <span data-ttu-id="d055a-129">Por exemplo, o recurso de edição colaborativa de arquivos do Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="d055a-129">For example, the collaborative file-editing feature of Microsoft Word.</span></span> <span data-ttu-id="d055a-130">Em vez de clicar em um link e baixar a cópia inteira de um documento em que você está trabalhando com seus colegas, o DirectInvoke permite baixar as partes do documento que foram alteradas.</span><span class="sxs-lookup"><span data-stu-id="d055a-130">Instead of clicking a link and downloading the entire copy of a document you're working on with your colleagues, DirectInvoke lets you download the parts of the document that have been changed.</span></span> <span data-ttu-id="d055a-131">Isso reduz a quantidade de dados transferidos, podendo reduzir o tempo necessário para abrir o documento.</span><span class="sxs-lookup"><span data-stu-id="d055a-131">This strategy reduces the amount of data transferred and can reduce the time needed to open the document.</span></span>  

## <span data-ttu-id="d055a-132">Suporte atual ao ClickOnce e ao DirectInvoke no Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="d055a-132">Current support for ClickOnce and DirectInvoke in Microsoft Edge</span></span>

<span data-ttu-id="d055a-133">Suporte ao ClickOnce e ao DirectInvoke:</span><span class="sxs-lookup"><span data-stu-id="d055a-133">Support for ClickOnce and DirectInvoke:</span></span>

- <span data-ttu-id="d055a-134">O ClickOnce e o DirectInvoke têm suporte prontos para todos os usuários do Windows.</span><span class="sxs-lookup"><span data-stu-id="d055a-134">ClickOnce and DirectInvoke are supported out of the box for all Windows users.</span></span>

  > [!NOTE]
  > <span data-ttu-id="d055a-135">Os usuários que precisam desabilitar o suporte ao ClickOnce podem acessar *edge://flags/#edge-click-once* e selecionar **Desabilitador** na lista suspensa.</span><span class="sxs-lookup"><span data-stu-id="d055a-135">Users that want to disable ClickOnce support can go to *edge://flags/#edge-click-once* and select **Disabled** from the dropdown list.</span></span> <span data-ttu-id="d055a-136">Você precisará **Reiniciar** o navegador.</span><span class="sxs-lookup"><span data-stu-id="d055a-136">You'll have to **Restart** the browser.</span></span>

- <span data-ttu-id="d055a-137">O ClickOnce e o DirectInvoke não têm suporte em outras plataformas que não seja o Windows.</span><span class="sxs-lookup"><span data-stu-id="d055a-137">ClickOnce and DirectInvoke aren't supported on any platforms other than Windows.</span></span>

## <span data-ttu-id="d055a-138">Segurança de manipulação de arquivos do ClickOnce e do DirectInvoke</span><span class="sxs-lookup"><span data-stu-id="d055a-138">ClickOnce and DirectInvoke file handling security</span></span>

<span data-ttu-id="d055a-139">O ClickOnce e o DirectInvoke são protegidos pelo serviço de verificação de reputação de URL do Microsoft Defender SmartScreen.</span><span class="sxs-lookup"><span data-stu-id="d055a-139">ClickOnce and DirectInvoke are protected by Microsoft Defender SmartScreen's URL reputation scanning service.</span></span>

<span data-ttu-id="d055a-140">Se uma solicitação do ClickOnce ou do DirectInvoke for sinalizada pelo serviço de reputação de URL do Microsoft Defender SmartScreen como não seguro, os usuários com o ClickOnce ou o DirectInvoke habilitado verão dois pop-ups.</span><span class="sxs-lookup"><span data-stu-id="d055a-140">If a ClickOnce or a DirectInvoke request is flagged by the Microsoft Defender SmartScreen URL reputation service as unsafe, users with ClickOnce or DirectInvoke enabled will see two popups.</span></span>

<span data-ttu-id="d055a-141">O primeiro pop-up pergunta ao usuário se ele quer abrir o arquivo.</span><span class="sxs-lookup"><span data-stu-id="d055a-141">The first popup asks the user if they want to open the file.</span></span> <span data-ttu-id="d055a-142">Esse pop-up é exibido independentemente de o arquivo ter sido sinalizado como seguro ou não seguro.</span><span class="sxs-lookup"><span data-stu-id="d055a-142">This popup is displayed regardless of whether the file was flagged as safe or unsafe.</span></span> <span data-ttu-id="d055a-143">O usuário pode **Relatar o arquivo como não seguro**, **Cancelar** a solicitação ou clicar em **Abrir** para continuar.</span><span class="sxs-lookup"><span data-stu-id="d055a-143">The user can **Report the file as unsafe**, **Cancel** the request, or click **Open** to continue.</span></span>

   ![Aviso para abrir um arquivo](./media/edge-learn-more-co-di/edge-clickonce-modal-1.png)

<span data-ttu-id="d055a-145">Se o usuário tentar abrir um arquivo que foi sinalizado como não seguro, um segundo pop-up será exibido.</span><span class="sxs-lookup"><span data-stu-id="d055a-145">If the user tries to open the file, and the file was flagged as unsafe, a second popup is displayed.</span></span>  <span data-ttu-id="d055a-146">Esse pop-up avisa o usuário de que o arquivo foi sinalizado como não seguro e pergunta se ele tem certeza de que quer baixar o arquivo.</span><span class="sxs-lookup"><span data-stu-id="d055a-146">This popup warns the user that the file was flagged as unsafe, and asks them if they're sure they want to download the file.</span></span>

<span data-ttu-id="d055a-147">O segundo pop-up só aparece se:</span><span class="sxs-lookup"><span data-stu-id="d055a-147">The second popup only shows up if:</span></span>

- <span data-ttu-id="d055a-148">o arquivo for um arquivo do ClickOnce ou do DirectInvoke</span><span class="sxs-lookup"><span data-stu-id="d055a-148">the file is a ClickOnce or DirectInvoke file</span></span>
- <span data-ttu-id="d055a-149">o ClickOnce ou o DirectInvoke estiverem habilitados</span><span class="sxs-lookup"><span data-stu-id="d055a-149">ClickOnce or DirectInvoke are enabled</span></span>
- <span data-ttu-id="d055a-150">o arquivo estiver sinalizado como não seguro</span><span class="sxs-lookup"><span data-stu-id="d055a-150">the file is flagged as unsafe</span></span>

 ![Aviso para abrir um arquivo não seguro](./media/edge-learn-more-co-di/edge-clickonce-modal-2.png)

> [!NOTE]
> <span data-ttu-id="d055a-152">Se o ClickOnce ou o DirectInvoke estiverem desabilitados, os arquivos solicitados serão tratados como downloads regulares e, se sinalizados como não seguros, serão marcados como não seguros.</span><span class="sxs-lookup"><span data-stu-id="d055a-152">If ClickOnce or DirectInvoke are disabled, requested files are treated as regular downloads and if flagged as unsafe, will be marked as unsafe.</span></span> <span data-ttu-id="d055a-153">Isso é consistente com o tratamento de outros downloads não seguros.</span><span class="sxs-lookup"><span data-stu-id="d055a-153">This is consistent with the treatment of other unsafe downloads.</span></span>

## <span data-ttu-id="d055a-154">Políticas do ClickOnce e do DirectInvoke</span><span class="sxs-lookup"><span data-stu-id="d055a-154">ClickOnce and DirectInvoke policies</span></span>

<span data-ttu-id="d055a-155">Há duas políticas de grupo que você pode usar para habilitar ou desabilitar o ClickOnce e o DirectInvoke para usuários corporativos.</span><span class="sxs-lookup"><span data-stu-id="d055a-155">There are two group policies that you can use to enable or disable ClickOnce and DirectInvoke for enterprise users.</span></span> <span data-ttu-id="d055a-156">Essas duas políticas são [ClickOnceEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#clickonceenabled) e [DirectInvokeEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#directinvokeenabled).</span><span class="sxs-lookup"><span data-stu-id="d055a-156">These two policies are [ClickOnceEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#clickonceenabled) and [DirectInvokeEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#directinvokeenabled).</span></span> <span data-ttu-id="d055a-157">Essas duas políticas são rotuladas no Editor de Política de Grupo como "Permitir que os usuários abram arquivos usando o protocolo ClickOnce" e "Permitir que os usuários abram arquivos usando o protocolo DirectInvoke", respectivamente.</span><span class="sxs-lookup"><span data-stu-id="d055a-157">These two policies are labeled in the Group Policy Editor as "Allow users to open files using the ClickOnce protocol" and "Allow users to open files using the DirectInvoke protocol" respectively.</span></span>

## <span data-ttu-id="d055a-158">Comportamento do ClickOnce e do DirectInvoke</span><span class="sxs-lookup"><span data-stu-id="d055a-158">ClickOnce and DirectInvoke behavior</span></span>

<span data-ttu-id="d055a-159">Os exemplos a seguir mostram a manipulação de arquivos quando o ClickOnce e o DirectInvoke estão habilitados ou desabilitados.</span><span class="sxs-lookup"><span data-stu-id="d055a-159">The following examples show file handling when ClickOnce and DirectInvoke are enabled or disabled.</span></span>

### <span data-ttu-id="d055a-160">ClickOnce habilitado</span><span class="sxs-lookup"><span data-stu-id="d055a-160">ClickOnce enabled</span></span>

1. <span data-ttu-id="d055a-161">Um usuário abre um link para uma página que solicita suporte ao ClickOnce e recebe o aviso exibido na próxima captura de tela.</span><span class="sxs-lookup"><span data-stu-id="d055a-161">A user opens a link to a page that requests ClickOnce support and gets the prompt in the next screenshot.</span></span>

   ![Aviso para abrir um arquivo não seguro](./media/edge-learn-more-co-di/edge-clickonce-enabled-1.png)

2. <span data-ttu-id="d055a-163">Depois que o usuário clica em **Abrir**, o ClickOnce tenta iniciar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d055a-163">After the user clicks **Open**, ClickOnce attempts to launch the application.</span></span>

   ![O ClickOnce tenta iniciar o aplicativo](./media/edge-learn-more-co-di/edge-clickonce-enabled-launch-app.png)

3. <span data-ttu-id="d055a-165">Depois que o usuário clica em **Abrir**, o navegador mostra um pop-up que pergunta se o usuário tem certeza de que quer instalar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d055a-165">After the user clicks **Open**, the browser shows a popup that asks the user if they're sure they want to install the application.</span></span>

   ![Aviso para abrir o arquivo](./media/edge-learn-more-co-di/edge-clickonce-enabled-2.png)

   > [!NOTE]
   > <span data-ttu-id="d055a-167">A interface, as mensagens e as opções mostradas pelo manipulador de arquivos do ClickOnce variam de acordo com o tipo e a configuração do arquivo acessado.</span><span class="sxs-lookup"><span data-stu-id="d055a-167">The interface, messaging, and options shown by the ClickOnce file handler will vary depending on the type and configuration of the file that's accessed.</span></span>

### <span data-ttu-id="d055a-168">ClickOnce desabilitado</span><span class="sxs-lookup"><span data-stu-id="d055a-168">ClickOnce disabled</span></span>

1. <span data-ttu-id="d055a-169">Quando um usuário abre um link para uma página que solicita suporte ao ClickOnce, ele verá uma mensagem na bandeja de download semelhante à da próxima captura de tela.</span><span class="sxs-lookup"><span data-stu-id="d055a-169">When a user opens a link to a page that requests ClickOnce support, they will see a message in the download tray that is similar to the one in the next screenshot.</span></span>

   ![Aviso de download de arquivo](./media/edge-learn-more-co-di/edge-clickonce-disabled-1.png)

### <span data-ttu-id="d055a-171">DirectInvoke habilitado</span><span class="sxs-lookup"><span data-stu-id="d055a-171">DirectInvoke enabled</span></span>

1. <span data-ttu-id="d055a-172">Um usuário abre um link para uma página que solicita suporte ao DirectInvoke e recebe o aviso exibido na próxima captura de tela.</span><span class="sxs-lookup"><span data-stu-id="d055a-172">A user opens a link to a page that requests DirectInvoke support and gets the prompt in the next screenshot.</span></span>

   ![Aviso para abrir um arquivo](./media/edge-learn-more-co-di/edge-directinvoke-open-link-1.png)

2. <span data-ttu-id="d055a-174">Quando o usuário clica em **Abrir**, o manipulador de arquivos solicitado é aberto.</span><span class="sxs-lookup"><span data-stu-id="d055a-174">When the user clicks **Open**, the requested file handler is opened.</span></span> <span data-ttu-id="d055a-175">Neste exemplo, o Microsoft Word é usado para abrir o documento exibido na captura de tela anterior.</span><span class="sxs-lookup"><span data-stu-id="d055a-175">In this example, Microsoft Word is used to open the document that's shown in the previous screenshot.</span></span>

   > [!NOTE]
   > <span data-ttu-id="d055a-176">A interface, as mensagens e as opções mostradas pelo manipulador de arquivos do DirectInvoke variam de acordo com o tipo e a configuração do arquivo acessado.</span><span class="sxs-lookup"><span data-stu-id="d055a-176">The interface, messaging, and options shown by the DirectInvoke file handler will vary depending on the type and configuration of the file that's accessed.</span></span>

### <span data-ttu-id="d055a-177">DirectInvoke desabilitado</span><span class="sxs-lookup"><span data-stu-id="d055a-177">DirectInvoke disabled</span></span>

1. <span data-ttu-id="d055a-178">Quando um usuário abre um link para uma página que solicita suporte ao DirectInvoke, o DirectInvoke se comporta igual quando o ClickOnce está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="d055a-178">When a user opens a link to a page that requests DirectInvoke support, DirectInvoke behaves the same as when ClickOnce is disabled.</span></span> <span data-ttu-id="d055a-179">Ele verá uma mensagem na bandeja de download semelhante à da próxima captura de tela.</span><span class="sxs-lookup"><span data-stu-id="d055a-179">They will see a message in the download tray that's similar to the one in the next screenshot.</span></span>

   ![Aviso para abrir um arquivo](./media/edge-learn-more-co-di/edge-directinvoke-open-link-2.png)

## <span data-ttu-id="d055a-181">Ver também</span><span class="sxs-lookup"><span data-stu-id="d055a-181">See also</span></span>

- [<span data-ttu-id="d055a-182">Segurança e implantação do ClickOnce</span><span class="sxs-lookup"><span data-stu-id="d055a-182">ClickOnce security and deployment</span></span>](https://go.microsoft.com/fwlink/?linkid=2099880)
- [<span data-ttu-id="d055a-183">DirectInvoke no Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="d055a-183">DirectInvoke in Internet Explorer</span></span>](https://go.microsoft.com/fwlink/?linkid=2099871)
- [<span data-ttu-id="d055a-184">Página de aterrissagem do Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="d055a-184">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
