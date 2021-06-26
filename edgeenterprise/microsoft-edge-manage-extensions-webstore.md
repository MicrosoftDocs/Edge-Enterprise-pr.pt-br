---
title: Extensões de auto-hospedagem do Microsoft Edge
ms.author: aspoddar
author: AndreaLBarr
manager: balajek
ms.date: 04/08/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Saiba como empacotar e hospedar extensões do Microsoft Edge na empresa.
ms.openlocfilehash: 403b6879b15c146f40fa2564da76eae59b2abe88
ms.sourcegitcommit: 4192328ee585bc32a9be528766b8a5a98e046c8e
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/25/2021
ms.locfileid: "11618013"
---
# <a name="self-host-microsoft-edge-extensions"></a><span data-ttu-id="73f57-103">Extensões de auto-hospedagem do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="73f57-103">Self-host Microsoft Edge extensions</span></span>

<span data-ttu-id="73f57-104">Este artigo fornece orientações básicas para empacotar uma extensão para hospedar em sua própria loja na web.</span><span class="sxs-lookup"><span data-stu-id="73f57-104">This article provides basic guidance for packaging an extension to host on your own webstore.</span></span> <span data-ttu-id="73f57-105">Ele também inclui instruções sobre como implantar extensões em dispositivos e usuários em sua organização.</span><span class="sxs-lookup"><span data-stu-id="73f57-105">It also includes instructions on how to deploy extensions to devices and users in your organization.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="73f57-106">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="73f57-106">Prerequisites</span></span>

<span data-ttu-id="73f57-107">Para auto-hospedar suas próprias extensões, você precisará fornecer seus próprios serviços de hospedagem da Web para as extensões e seus arquivos de manifesto.</span><span class="sxs-lookup"><span data-stu-id="73f57-107">To self-host your own extensions, you will need to provide your own web hosting services for the extensions and their manifest files.</span></span>

 <span data-ttu-id="73f57-108">As etapas a seguir pressupõem que você já criou sua extensão, tem alguma experiência com arquivos XML, um conhecimento prático sobre a configuração da política de grupo e saiba como usar o registro do Windows.</span><span class="sxs-lookup"><span data-stu-id="73f57-108">The following steps assume that you’ve already created your extension, have some experience with XML files, have a working knowledge of configuring group policy, and know how to use the Windows registry.</span></span>

## <a name="publish-an-extension"></a><span data-ttu-id="73f57-109">Publicar uma extensão</span><span class="sxs-lookup"><span data-stu-id="73f57-109">Publish an extension</span></span>

<span data-ttu-id="73f57-110">Antes de publicar uma extensão, ela precisa ser empacotada em um arquivo CRX (extensão do Chrome).</span><span class="sxs-lookup"><span data-stu-id="73f57-110">Before you publish an extension it needs to be packed into a CRX (Chrome extension) file.</span></span> <span data-ttu-id="73f57-111">Use as etapas a seguir como um guia para empacotar uma extensão como um arquivo CRX.</span><span class="sxs-lookup"><span data-stu-id="73f57-111">Use the following steps as a guide to packing an extension as a CRX file.</span></span>

1. <span data-ttu-id="73f57-112">Na barra de endereços do Microsoft Edge, vá para *edge://extensions* e ative o **Modo desenvolvedor** se ele ainda não estiver habilitado.</span><span class="sxs-lookup"><span data-stu-id="73f57-112">In the Microsoft Edge address bar, go to *edge://extensions* and turn on **Developer mode** if it’s not already enabled.</span></span>
2. <span data-ttu-id="73f57-113">Em **Extensões instaladas,** clique em **Extensão de Pacote** para criar o arquivo CRX.</span><span class="sxs-lookup"><span data-stu-id="73f57-113">Under **Installed extensions**, click **Pack Extension** to create the CRX file.</span></span>
3. <span data-ttu-id="73f57-114">Use a **Extensão de pacote** para encontrar o diretório que tem a origem da extensão.</span><span class="sxs-lookup"><span data-stu-id="73f57-114">Use the **Pack extension** dialog to find the directory that has the source for the extension.</span></span> <span data-ttu-id="73f57-115">Selecione o diretório e clique em **Extensão de pacote**.</span><span class="sxs-lookup"><span data-stu-id="73f57-115">Select the directory and then click **Pack extension**.</span></span>  <span data-ttu-id="73f57-116">Isso criará seu arquivo CRX, juntamente com um arquivo PEM.</span><span class="sxs-lookup"><span data-stu-id="73f57-116">This will create your CRX file, along with a PEM file.</span></span> <span data-ttu-id="73f57-117">Salve o arquivo PEM porque ele é necessário para fazer atualizações de versão para a extensão.</span><span class="sxs-lookup"><span data-stu-id="73f57-117">Save the PEM file because it’s needed for making version updates to the extension.</span></span> <span data-ttu-id="73f57-118">A próxima captura de tela mostra a caixa de diálogo da **Extensão do pacote** para localizar o diretório raiz da extensão.</span><span class="sxs-lookup"><span data-stu-id="73f57-118">The next screenshot shows the **Pack extension** dialog for locating the root directory of the extension.</span></span>

   :::image type="content" source="media/microsoft-edge-manage-extensions-webstore/manage-extensions-pack-dialog.png" alt-text="Caixa de diálogo da extensão de pacote para localizar o código-fonte de uma extensão.":::

   > [!IMPORTANT]
   > <span data-ttu-id="73f57-120">Armazene o arquivo PEM em um local seguro porque ele é a chave para a extensão e é necessário para atualizações futuras.</span><span class="sxs-lookup"><span data-stu-id="73f57-120">Store the PEM file in a safe location because it’s the key for the extension and it’s needed for future updates.</span></span>

4. <span data-ttu-id="73f57-121">Arraste o arquivo CRX para a janela de extensões e certifique-se de que ele seja carregado.</span><span class="sxs-lookup"><span data-stu-id="73f57-121">Drag the CRX file into your extensions window and make sure that it loads.</span></span>
5. <span data-ttu-id="73f57-122">Teste a extensão e anote o campo ID (esta é a ID CRX) e o número da versão.</span><span class="sxs-lookup"><span data-stu-id="73f57-122">Test the extension and take note of the ID field (this is the CRX ID) and version number.</span></span> <span data-ttu-id="73f57-123">Você precisará das informações mais tarde.</span><span class="sxs-lookup"><span data-stu-id="73f57-123">You’ll need this information later.</span></span> <span data-ttu-id="73f57-124">A próxima captura de tela mostra uma extensão de teste com sua ID CRX.</span><span class="sxs-lookup"><span data-stu-id="73f57-124">The next screenshot shows a test extension with its CRX ID.</span></span>

   :::image type="content" source="media/microsoft-edge-manage-extensions-webstore/manage-extensions-test-extension.png" alt-text="Exemplo de extensão mostrando a ID CRX":::

6. <span data-ttu-id="73f57-126">Upload o arquivo CRX para o host e observe a URL do local de onde ele será baixado.</span><span class="sxs-lookup"><span data-stu-id="73f57-126">Upload the the CRX file to the host and note the URL of the location it will be downloaded from.</span></span> <span data-ttu-id="73f57-127">Essas informações são necessárias para o arquivo de manifesto XML.</span><span class="sxs-lookup"><span data-stu-id="73f57-127">This information is needed for the XML manifest file.</span></span>
7. <span data-ttu-id="73f57-128">Para criar um arquivo XML de manifesto com a ID do aplicativo/extensão, baixe a URL e a versão, defina os seguintes campos:</span><span class="sxs-lookup"><span data-stu-id="73f57-128">To create a manifest XML file with the app/extension ID, download URL, and version, define the following fields:</span></span>  

   - <span data-ttu-id="73f57-129">**appid** - A ID da extensão da etapa 5</span><span class="sxs-lookup"><span data-stu-id="73f57-129">**appid** - The extension ID from step 5</span></span>
   - <span data-ttu-id="73f57-130">**codebase** - O local de download do arquivo CRX da etapa 6</span><span class="sxs-lookup"><span data-stu-id="73f57-130">**codebase** - The download location for the CRX file from step 6</span></span>
   - <span data-ttu-id="73f57-131">**versão** - A versão do aplicativo/extensão, que deve corresponder à versão especificada no manifesto da extensão.</span><span class="sxs-lookup"><span data-stu-id="73f57-131">**version** - The version of the app/extension, which should match the version specified in the manifest of the extension.</span></span>

   <span data-ttu-id="73f57-132">O próximo trecho de código mostra um exemplo de um arquivo de manifesto XML.</span><span class="sxs-lookup"><span data-stu-id="73f57-132">The next code snippet shows an example of an XML manifest file.</span></span>

   ```xml
   <?xml version='1.0' encoding='UTF-8'?> 
   <gupdate xmlns='http://www.google.com/update2/response' protocol='2.0'> 
     <app appid='ekilpdeokbpjmminmhfcgkncmmohmfeb'> 
     <updatecheck codebase='https://app.somecompany.com/extensionfolder/helloworld.crx' version='1.0' /> 
     </app> 
   </gupdate> 
   ```

   <span data-ttu-id="73f57-133">Para obter mais informações, consulte [Extensões de atualização automática no Microsoft Edge - Desenvolvimento do Microsoft Edge](/microsoft-edge/extensions-chromium/enterprise/auto-update).</span><span class="sxs-lookup"><span data-stu-id="73f57-133">For more information, see [Auto-update extensions in Microsoft Edge - Microsoft Edge Development](/microsoft-edge/extensions-chromium/enterprise/auto-update).</span></span>

8. <span data-ttu-id="73f57-134">Upload o arquivo XML concluído para um local de onde ele possa ser baixado, anotando a URL.</span><span class="sxs-lookup"><span data-stu-id="73f57-134">Upload the completed XML file to a location where it can be downloaded from, noting the URL.</span></span> <span data-ttu-id="73f57-135">Essa URL será necessária ao instalar a extensão usando uma política de grupo.</span><span class="sxs-lookup"><span data-stu-id="73f57-135">This URL will be needed when you install the extension using a group policy.</span></span> <span data-ttu-id="73f57-136">Consulte [Distribuir uma extensão hospedada privadamente.](#distribute-a-privately-hosted-extension)</span><span class="sxs-lookup"><span data-stu-id="73f57-136">See [Distribute a privately hosted extension](#distribute-a-privately-hosted-extension).</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="73f57-137">O local de hospedagem da extensão não precisa de autenticação.</span><span class="sxs-lookup"><span data-stu-id="73f57-137">The hosting location for the extension doesn’t need authentication.</span></span> <span data-ttu-id="73f57-138">Ele precisa estar acessível por dispositivos de usuário onde quer que possam ser usados.</span><span class="sxs-lookup"><span data-stu-id="73f57-138">It needs to be accessible by user devices wherever they might be used.</span></span>

## <a name="publish-updates-to-an-extension"></a><span data-ttu-id="73f57-139">Publicar atualizações em uma extensão</span><span class="sxs-lookup"><span data-stu-id="73f57-139">Publish updates to an extension</span></span>

<span data-ttu-id="73f57-140">Depois de alterar e testar a extensão atualizada, você pode publicá-la.</span><span class="sxs-lookup"><span data-stu-id="73f57-140">After you change and test the updated extension you can publish it.</span></span> <span data-ttu-id="73f57-141">Use as etapas a seguir como um guia para publicar uma atualização.</span><span class="sxs-lookup"><span data-stu-id="73f57-141">Use the following steps as a guide for publishing an update.</span></span>

1. <span data-ttu-id="73f57-142">Altere o número de versão no seu arquivo de extensão manifest.JSON para um número mais alto usando a seguinte sintaxe: `"version":"versionString"`.</span><span class="sxs-lookup"><span data-stu-id="73f57-142">Change the version number in your extension's manifest.JSON file to a higher number using the following syntax: `"version":"versionString"`.</span></span> <span data-ttu-id="73f57-143">Se a "versão":"1.0", você poderá atualizar para "versão":"1.1" ou qualquer número maior que "1.0".</span><span class="sxs-lookup"><span data-stu-id="73f57-143">If the "version":"1.0", then you can update to "version":"1.1" or any number higher than "1.0".</span></span>
2. <span data-ttu-id="73f57-144">Atualize a "versão" de `<updatecheck>` no arquivo XML para corresponder ao número que você colocou no arquivo de manifesto na etapa anterior.</span><span class="sxs-lookup"><span data-stu-id="73f57-144">Update the "version" of `<updatecheck>` in the XML file to match the number that you put in the manifest file in the previous step.</span></span> <span data-ttu-id="73f57-145">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="73f57-145">For example:</span></span><br>`<updatecheck codebase='https://app.somecompany.com/extensionfolder/helloworld.crx' version='1.1' />`
3. <span data-ttu-id="73f57-146">Crie um arquivo CRX que inclua as novas alterações.</span><span class="sxs-lookup"><span data-stu-id="73f57-146">Create a CRX file that includes the new changes.</span></span> <span data-ttu-id="73f57-147">Vá para *edge://extensions* e habilite o **Modo desenvolvedor**.</span><span class="sxs-lookup"><span data-stu-id="73f57-147">Go to *edge://extensions* and enable **Developer mode**.</span></span>
4. <span data-ttu-id="73f57-148">Clique em **Pacote de extensão** e vá para o diretório para a fonte de extensão.</span><span class="sxs-lookup"><span data-stu-id="73f57-148">Click **Pack extension** and go to the directory for the extension source.</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="73f57-149">Use o mesmo arquivo PEM que foi gerado e salvo na primeira vez que o arquivo CRX foi criado.</span><span class="sxs-lookup"><span data-stu-id="73f57-149">Use the same PEM file that was generated and saved the first time the CRX file was created.</span></span> <span data-ttu-id="73f57-150">Se você não usar o mesmo arquivo PEM, a ID do aplicativo da extensão será mudada e a atualização será tratada como uma nova extensão.</span><span class="sxs-lookup"><span data-stu-id="73f57-150">If you don't use the same PEM file the app ID of the extension will change and the update will be treated as a new extension.</span></span>

5. <span data-ttu-id="73f57-151">Arraste e solte o arquivo CRX na janela de extensões e verifique se ele é carregado.</span><span class="sxs-lookup"><span data-stu-id="73f57-151">Drag and drop the CRX file into the extensions window and verify that it loads.</span></span>
6. <span data-ttu-id="73f57-152">Teste a extensão atualizada.</span><span class="sxs-lookup"><span data-stu-id="73f57-152">Test the updated extension.</span></span>
7. <span data-ttu-id="73f57-153">Substitua o arquivo CRX antigo e o arquivo XML pelos novos arquivos para a extensão atualizada.</span><span class="sxs-lookup"><span data-stu-id="73f57-153">Replace the old CRX file and XML file with the new files for the updated extension.</span></span>

<span data-ttu-id="73f57-154">As alterações da extensão serão escolhidas durante o próximo ciclo de sincronização de política.</span><span class="sxs-lookup"><span data-stu-id="73f57-154">The extension's changes will be picked up during the next policy sync cycle.</span></span> <span data-ttu-id="73f57-155">Para obter mais informações sobre a atualização de extensões, consulte: [Atualizar URL](/microsoft-edge/extensions-chromium/enterprise/auto-update#update-url) e [Atualizar manifesto](/microsoft-edge/extensions-chromium/enterprise/auto-update#updated-manifest).</span><span class="sxs-lookup"><span data-stu-id="73f57-155">For more information about updating extensions, see: [Update URL](/microsoft-edge/extensions-chromium/enterprise/auto-update#update-url) and [Update manifest](/microsoft-edge/extensions-chromium/enterprise/auto-update#updated-manifest).</span></span>

## <a name="distribute-a-privately-hosted-extension"></a><span data-ttu-id="73f57-156">Distribuir uma extensão hospedada privadamente</span><span class="sxs-lookup"><span data-stu-id="73f57-156">Distribute a privately hosted extension</span></span>

<span data-ttu-id="73f57-157">Você pode compartilhar o link do local onde o arquivo CRX está hospedado e, assim que os usuários inserirem a URL em seu navegador, a extensão será baixada e instalada.</span><span class="sxs-lookup"><span data-stu-id="73f57-157">You can share the link of the location where the CRX file is hosted, and as soon as users enter the URL in their browser the extension will be downloaded and installed.</span></span> <span data-ttu-id="73f57-158">Os usuários podem habilitar a extensão da página edge://extensions.</span><span class="sxs-lookup"><span data-stu-id="73f57-158">Users can enable the extension from the edge://extensions page.</span></span> <span data-ttu-id="73f57-159">Para permitir que os usuários instalem extensões auto-hospedadas, você precisa adicionar as IDs CRX de extensão à política [ExtensionInstallAllowList.](/deployedge/microsoft-edge-policies#extensioninstallallowlist)</span><span class="sxs-lookup"><span data-stu-id="73f57-159">To allow users to install self-hosted extensions, you need to add the extension CRX IDs to the [ExtensionInstallAllowList](/deployedge/microsoft-edge-policies#extensioninstallallowlist) policy.</span></span>

<span data-ttu-id="73f57-160">Como alternativa, você pode usar a política de grupo [ExtensionInstallForceList](/deployedge/microsoft-edge-manage-extensions-policies#force-install-an-extension) para forçar a instalação de uma extensão nos dispositivos de seus usuários.</span><span class="sxs-lookup"><span data-stu-id="73f57-160">Alternatively, you can use group policy [ExtensionInstallForceList](/deployedge/microsoft-edge-manage-extensions-policies#force-install-an-extension) to Force-install an extension on your users’ devices.</span></span>

<span data-ttu-id="73f57-161">Você pode aplicar essas políticas aos usuários e dispositivos selecionados ou ambos.</span><span class="sxs-lookup"><span data-stu-id="73f57-161">You can apply these policies to your selected users, devices, or both.</span></span> <span data-ttu-id="73f57-162">Lembre-se de que as atualizações de política não são instantâneas e levará tempo para que as configurações de política entrem em vigor.</span><span class="sxs-lookup"><span data-stu-id="73f57-162">Remember though that policy updates are not instantaneous, and it will take time for the policy settings to take effect.</span></span>

## <a name="see-also"></a><span data-ttu-id="73f57-163">Veja também</span><span class="sxs-lookup"><span data-stu-id="73f57-163">See also</span></span>

- [<span data-ttu-id="73f57-164">Gerenciar extensões do Microsoft Edge na empresa</span><span class="sxs-lookup"><span data-stu-id="73f57-164">Manage Microsoft Edge extensions in the enterprise</span></span>](microsoft-edge-manage-extensions.md)
- [<span data-ttu-id="73f57-165">Usar políticas de grupo para gerenciar extensões do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="73f57-165">Use group policies to manage Microsoft Edge extensions</span></span>](microsoft-edge-manage-extensions-policies.md)
- [<span data-ttu-id="73f57-166">Guia detalhado da política ExtensionSettings</span><span class="sxs-lookup"><span data-stu-id="73f57-166">Detailed guide to the ExtensionSettings policy</span></span>](microsoft-edge-manage-extensions-ref-guide.md)
- [<span data-ttu-id="73f57-167">Perguntas frequentes sobre extensões do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="73f57-167">FAQ for Microsoft Edge Extensions</span></span>](microsoft-edge-manage-extensions-faq.md)
- [<span data-ttu-id="73f57-168">Página de aterrissagem do Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="73f57-168">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
