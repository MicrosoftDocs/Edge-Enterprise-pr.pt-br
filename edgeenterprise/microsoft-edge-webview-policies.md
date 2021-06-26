---
title: Documentação de Política do Microsoft Edge WebView2
ms.author: stmoody
author: dan-wesley
manager: tahills
ms.date: 06/17/2021
audience: ITPro
ms.topic: reference
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
ms.custom: ''
description: Documentação do Windows e do Mac para todas as políticas compatíveis com o Microsoft Edge Browser
ms.openlocfilehash: 78d4a610fd4d5ba5549ea1e2e4833acc9e686016
ms.sourcegitcommit: 4192328ee585bc32a9be528766b8a5a98e046c8e
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/25/2021
ms.locfileid: "11617963"
---
# <a name="microsoft-edge-webview2---policies"></a><span data-ttu-id="5c2e9-103">Políticas do Microsoft Edge WebView2</span><span class="sxs-lookup"><span data-stu-id="5c2e9-103">Microsoft Edge WebView2 - Policies</span></span>

<span data-ttu-id="5c2e9-104">A versão mais recente do Microsoft Edge WebView2 inclui as políticas a seguir.</span><span class="sxs-lookup"><span data-stu-id="5c2e9-104">The latest version of Microsoft Edge WebView2 includes the following policies.</span></span> <span data-ttu-id="5c2e9-105">Você pode usar essas políticas para configurar como o Microsoft Edge WebView2 será executado em sua organização.</span><span class="sxs-lookup"><span data-stu-id="5c2e9-105">You can use these policies to configure how Microsoft Edge WebView2 runs in your organization.</span></span>

<span data-ttu-id="5c2e9-106">Para saber mais sobre o conjunto adicional de políticas, usado para controlar como e quando o Microsoft Edge WebView2 é atualizado, confira [Referência de política de atualização do Microsoft Edge](microsoft-edge-update-policies.md).</span><span class="sxs-lookup"><span data-stu-id="5c2e9-106">For information about an additional set of policies used to control how and when Microsoft Edge WebView2 is updated, check out [Microsoft Edge update policy reference](microsoft-edge-update-policies.md).</span></span>


> [!NOTE]
> <span data-ttu-id="5c2e9-107">Este artigo se aplica ao Microsoft Edge versão 87 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="5c2e9-107">This article applies to Microsoft Edge version 87 or later.</span></span>

## <a name="available-policies"></a><span data-ttu-id="5c2e9-108">Políticas disponíveis</span><span class="sxs-lookup"><span data-stu-id="5c2e9-108">Available policies</span></span>

<span data-ttu-id="5c2e9-109">Estas tabelas listam todas as políticas de grupo disponíveis nesta versão do Microsoft Edge WebView2.</span><span class="sxs-lookup"><span data-stu-id="5c2e9-109">These tables list all of the group policies available in this release of Microsoft Edge WebView2.</span></span> <span data-ttu-id="5c2e9-110">Use os links na tabela a seguir para obter mais detalhes sobre políticas específicas.</span><span class="sxs-lookup"><span data-stu-id="5c2e9-110">Use the links in the table to get more details about specific policies.</span></span>

- [<span data-ttu-id="5c2e9-111">Configurações de substituição do carregador</span><span class="sxs-lookup"><span data-stu-id="5c2e9-111">Loader Override Settings</span></span>](#loader-override-settings)


### [*<a name="loader-override-settings"></a><span data-ttu-id="5c2e9-112">Configurações de substituição do carregador</span><span class="sxs-lookup"><span data-stu-id="5c2e9-112">Loader Override Settings</span></span>*](#loader-override-settings-policies)

|<span data-ttu-id="5c2e9-113">Nome da política</span><span class="sxs-lookup"><span data-stu-id="5c2e9-113">Policy Name</span></span>|<span data-ttu-id="5c2e9-114">Legenda</span><span class="sxs-lookup"><span data-stu-id="5c2e9-114">Caption</span></span>|
|-|-|
|[<span data-ttu-id="5c2e9-115">BrowserExecutableFolder</span><span class="sxs-lookup"><span data-stu-id="5c2e9-115">BrowserExecutableFolder</span></span>](#browserexecutablefolder)|<span data-ttu-id="5c2e9-116">Configurar o local da pasta executável do navegador</span><span class="sxs-lookup"><span data-stu-id="5c2e9-116">Configure the location of the browser executable folder</span></span>|
|[<span data-ttu-id="5c2e9-117">ReleaseChannelPreference</span><span class="sxs-lookup"><span data-stu-id="5c2e9-117">ReleaseChannelPreference</span></span>](#releasechannelpreference)|<span data-ttu-id="5c2e9-118">Definir a preferência de ordem de pesquisa do canal de lançamento</span><span class="sxs-lookup"><span data-stu-id="5c2e9-118">Set the release channel search order preference</span></span>|




  ## <a name="loader-override-settings-policies"></a><span data-ttu-id="5c2e9-119">Políticas de configurações de substituição do carregador</span><span class="sxs-lookup"><span data-stu-id="5c2e9-119">Loader Override Settings policies</span></span>

  [<span data-ttu-id="5c2e9-120">Voltar ao início</span><span class="sxs-lookup"><span data-stu-id="5c2e9-120">Back to top</span></span>](#microsoft-edge-webview2---policies)

  ### <a name="browserexecutablefolder"></a><span data-ttu-id="5c2e9-121">BrowserExecutableFolder</span><span class="sxs-lookup"><span data-stu-id="5c2e9-121">BrowserExecutableFolder</span></span>

  #### <a name="configure-the-location-of-the-browser-executable-folder"></a><span data-ttu-id="5c2e9-122">Configurar o local da pasta executável do navegador</span><span class="sxs-lookup"><span data-stu-id="5c2e9-122">Configure the location of the browser executable folder</span></span>

  
  
  #### <a name="supported-versions"></a><span data-ttu-id="5c2e9-123">Versões com suporte:</span><span class="sxs-lookup"><span data-stu-id="5c2e9-123">Supported versions:</span></span>

  - <span data-ttu-id="5c2e9-124">No Windows desde 87 ou posterior</span><span class="sxs-lookup"><span data-stu-id="5c2e9-124">On Windows since 87 or later</span></span>

  #### <a name="description"></a><span data-ttu-id="5c2e9-125">Descrição</span><span class="sxs-lookup"><span data-stu-id="5c2e9-125">Description</span></span>

  <span data-ttu-id="5c2e9-126">Essa política configura aplicativos de WebView2 para usar o WebView2 Runtime no caminho especificado.</span><span class="sxs-lookup"><span data-stu-id="5c2e9-126">This policy configures WebView2 applications to use the WebView2 Runtime in the specified path.</span></span> <span data-ttu-id="5c2e9-127">A pasta deve conter os seguintes arquivos: msedgewebview2.exe, msedge.dll e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="5c2e9-127">The folder should contain the following files: msedgewebview2.exe, msedge.dll, and so on.</span></span>

<span data-ttu-id="5c2e9-128">Para definir o valor do caminho da pasta, forneça um Nome do valor e um Par do valor.</span><span class="sxs-lookup"><span data-stu-id="5c2e9-128">To set the value for the folder path, provide a Value name and Value pair.</span></span> <span data-ttu-id="5c2e9-129">Defina o nome do valor para a ID do Modelo de Usuário do Aplicativo ou o nome do arquivo executável.</span><span class="sxs-lookup"><span data-stu-id="5c2e9-129">Set value name to the Application User Model ID or the executable file name.</span></span> <span data-ttu-id="5c2e9-130">Você pode usar o caractere curinga "\*" como nome do valor a ser aplicado a todos os aplicativos.</span><span class="sxs-lookup"><span data-stu-id="5c2e9-130">You can use the "\*" wildcard as value name to apply to all applications.</span></span>

  #### <a name="supported-features"></a><span data-ttu-id="5c2e9-131">Recursos compatíveis:</span><span class="sxs-lookup"><span data-stu-id="5c2e9-131">Supported features:</span></span>

  - <span data-ttu-id="5c2e9-132">Pode ser obrigatório: Sim</span><span class="sxs-lookup"><span data-stu-id="5c2e9-132">Can be mandatory: Yes</span></span>
  - <span data-ttu-id="5c2e9-133">Pode ser recomendável: não</span><span class="sxs-lookup"><span data-stu-id="5c2e9-133">Can be recommended: No</span></span>
  - <span data-ttu-id="5c2e9-134">Atualização dinâmica das políticas: Sim</span><span class="sxs-lookup"><span data-stu-id="5c2e9-134">Dynamic Policy Refresh: Yes</span></span>

  #### <a name="data-type"></a><span data-ttu-id="5c2e9-135">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="5c2e9-135">Data Type:</span></span>

  - <span data-ttu-id="5c2e9-136">Lista de cadeias de caracteres</span><span class="sxs-lookup"><span data-stu-id="5c2e9-136">List of strings</span></span>

  #### <a name="windows-information-and-settings"></a><span data-ttu-id="5c2e9-137">Informações e configurações do Windows</span><span class="sxs-lookup"><span data-stu-id="5c2e9-137">Windows information and settings</span></span>

  ##### <a name="group-policy-admx-info"></a><span data-ttu-id="5c2e9-138">Informações da Política de Grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="5c2e9-138">Group Policy (ADMX) info</span></span>

  - <span data-ttu-id="5c2e9-139">Nome exclusivo da PG: BrowserExecutableFolder</span><span class="sxs-lookup"><span data-stu-id="5c2e9-139">GP unique name: BrowserExecutableFolder</span></span>
  - <span data-ttu-id="5c2e9-140">Nome da PG: Configurar o local da pasta executável do navegador</span><span class="sxs-lookup"><span data-stu-id="5c2e9-140">GP name: Configure the location of the browser executable folder</span></span>
  - <span data-ttu-id="5c2e9-141">Caminho da PG (obrigatório): Modelos administrativos/Microsoft Edge WebView2/Configurações de substituição do carregador</span><span class="sxs-lookup"><span data-stu-id="5c2e9-141">GP path (Mandatory): Administrative Templates/Microsoft Edge WebView2/Loader Override Settings</span></span>
  - <span data-ttu-id="5c2e9-142">Caminho da Política de Grupo (recomendado): N/A</span><span class="sxs-lookup"><span data-stu-id="5c2e9-142">GP path (Recommended): N/A</span></span>
  - <span data-ttu-id="5c2e9-143">Nome do arquivo ADMX da PG: MSEdgeWebView2.admx</span><span class="sxs-lookup"><span data-stu-id="5c2e9-143">GP ADMX file name: MSEdgeWebView2.admx</span></span>

  ##### <a name="windows-registry-settings"></a><span data-ttu-id="5c2e9-144">Configurações de registro do Windows</span><span class="sxs-lookup"><span data-stu-id="5c2e9-144">Windows Registry Settings</span></span>

  - <span data-ttu-id="5c2e9-145">Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge\WebView2\BrowserExecutableFolder</span><span class="sxs-lookup"><span data-stu-id="5c2e9-145">Path (Mandatory): SOFTWARE\Policies\Microsoft\Edge\WebView2\BrowserExecutableFolder</span></span>
  - <span data-ttu-id="5c2e9-146">Caminho (recomendado): N/A</span><span class="sxs-lookup"><span data-stu-id="5c2e9-146">Path (Recommended): N/A</span></span>
  - <span data-ttu-id="5c2e9-147">Nome de valor: lista de REG_SZ</span><span class="sxs-lookup"><span data-stu-id="5c2e9-147">Value Name: list of REG_SZ</span></span>
  - <span data-ttu-id="5c2e9-148">Tipo de valor: lista de REG_SZ</span><span class="sxs-lookup"><span data-stu-id="5c2e9-148">Value Type: list of REG_SZ</span></span>

  ##### <a name="example-value"></a><span data-ttu-id="5c2e9-149">Valor de exemplo:</span><span class="sxs-lookup"><span data-stu-id="5c2e9-149">Example value:</span></span>

```
SOFTWARE\Policies\Microsoft\Edge\WebView2\BrowserExecutableFolder = "Name: *, Value: C:\\Program Files\\Microsoft Edge WebView2 Runtime Redistributable 85.0.541.0 x64"

```

  

  [<span data-ttu-id="5c2e9-150">Voltar ao início</span><span class="sxs-lookup"><span data-stu-id="5c2e9-150">Back to top</span></span>](#microsoft-edge-webview2---policies)

  ### <a name="releasechannelpreference"></a><span data-ttu-id="5c2e9-151">ReleaseChannelPreference</span><span class="sxs-lookup"><span data-stu-id="5c2e9-151">ReleaseChannelPreference</span></span>

  #### <a name="set-the-release-channel-search-order-preference"></a><span data-ttu-id="5c2e9-152">Definir a preferência de ordem de pesquisa do canal de lançamento</span><span class="sxs-lookup"><span data-stu-id="5c2e9-152">Set the release channel search order preference</span></span>

  
  
  #### <a name="supported-versions"></a><span data-ttu-id="5c2e9-153">Versões com suporte:</span><span class="sxs-lookup"><span data-stu-id="5c2e9-153">Supported versions:</span></span>

  - <span data-ttu-id="5c2e9-154">No Windows desde 87 ou posterior</span><span class="sxs-lookup"><span data-stu-id="5c2e9-154">On Windows since 87 or later</span></span>

  #### <a name="description"></a><span data-ttu-id="5c2e9-155">Descrição</span><span class="sxs-lookup"><span data-stu-id="5c2e9-155">Description</span></span>

  <span data-ttu-id="5c2e9-156">O pedido padrão de pesquisa de canal é WebView2 Runtime, Beta, Dev e Canary.</span><span class="sxs-lookup"><span data-stu-id="5c2e9-156">The default channel search order is WebView2 Runtime, Beta, Dev, and Canary.</span></span>

<span data-ttu-id="5c2e9-157">Para inverter a ordem de pesquisa padrão, defina essa política como 1.</span><span class="sxs-lookup"><span data-stu-id="5c2e9-157">To reverse the default search order, set this policy to 1.</span></span>

<span data-ttu-id="5c2e9-158">Para definir o valor da preferência de canal de lançamento, forneça um Nome do valor e um Par do valor.</span><span class="sxs-lookup"><span data-stu-id="5c2e9-158">To set the value for the release channel preference, provide a Value name and Value pair.</span></span> <span data-ttu-id="5c2e9-159">Defina o nome do valor para a ID do Modelo de Usuário do Aplicativo ou o nome do arquivo executável.</span><span class="sxs-lookup"><span data-stu-id="5c2e9-159">Set value name to the Application User Model ID or the executable file name.</span></span> <span data-ttu-id="5c2e9-160">Você pode usar o caractere curinga "\*" como nome do valor a ser aplicado a todos os aplicativos.</span><span class="sxs-lookup"><span data-stu-id="5c2e9-160">You can use the "\*" wildcard as value name to apply to all applications.</span></span>

  #### <a name="supported-features"></a><span data-ttu-id="5c2e9-161">Recursos compatíveis:</span><span class="sxs-lookup"><span data-stu-id="5c2e9-161">Supported features:</span></span>

  - <span data-ttu-id="5c2e9-162">Pode ser obrigatório: Sim</span><span class="sxs-lookup"><span data-stu-id="5c2e9-162">Can be mandatory: Yes</span></span>
  - <span data-ttu-id="5c2e9-163">Pode ser recomendável: não</span><span class="sxs-lookup"><span data-stu-id="5c2e9-163">Can be recommended: No</span></span>
  - <span data-ttu-id="5c2e9-164">Atualização dinâmica das políticas: Sim</span><span class="sxs-lookup"><span data-stu-id="5c2e9-164">Dynamic Policy Refresh: Yes</span></span>

  #### <a name="data-type"></a><span data-ttu-id="5c2e9-165">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="5c2e9-165">Data Type:</span></span>

  - <span data-ttu-id="5c2e9-166">Lista de cadeias de caracteres</span><span class="sxs-lookup"><span data-stu-id="5c2e9-166">List of strings</span></span>

  #### <a name="windows-information-and-settings"></a><span data-ttu-id="5c2e9-167">Informações e configurações do Windows</span><span class="sxs-lookup"><span data-stu-id="5c2e9-167">Windows information and settings</span></span>

  ##### <a name="group-policy-admx-info"></a><span data-ttu-id="5c2e9-168">Informações da Política de Grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="5c2e9-168">Group Policy (ADMX) info</span></span>

  - <span data-ttu-id="5c2e9-169">Nome exclusivo da PG: ReleaseChannelPreference</span><span class="sxs-lookup"><span data-stu-id="5c2e9-169">GP unique name: ReleaseChannelPreference</span></span>
  - <span data-ttu-id="5c2e9-170">Nome da PG: Definir a preferência de ordem de pesquisa do canal de lançamento</span><span class="sxs-lookup"><span data-stu-id="5c2e9-170">GP name: Set the release channel search order preference</span></span>
  - <span data-ttu-id="5c2e9-171">Caminho da PG (obrigatório): Modelos administrativos/Microsoft Edge WebView2/Configurações de substituição do carregador</span><span class="sxs-lookup"><span data-stu-id="5c2e9-171">GP path (Mandatory): Administrative Templates/Microsoft Edge WebView2/Loader Override Settings</span></span>
  - <span data-ttu-id="5c2e9-172">Caminho da Política de Grupo (recomendado): N/A</span><span class="sxs-lookup"><span data-stu-id="5c2e9-172">GP path (Recommended): N/A</span></span>
  - <span data-ttu-id="5c2e9-173">Nome do arquivo ADMX da PG: MSEdgeWebView2.admx</span><span class="sxs-lookup"><span data-stu-id="5c2e9-173">GP ADMX file name: MSEdgeWebView2.admx</span></span>

  ##### <a name="windows-registry-settings"></a><span data-ttu-id="5c2e9-174">Configurações de registro do Windows</span><span class="sxs-lookup"><span data-stu-id="5c2e9-174">Windows Registry Settings</span></span>

  - <span data-ttu-id="5c2e9-175">Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge\WebView2\ReleaseChannelPreference</span><span class="sxs-lookup"><span data-stu-id="5c2e9-175">Path (Mandatory): SOFTWARE\Policies\Microsoft\Edge\WebView2\ReleaseChannelPreference</span></span>
  - <span data-ttu-id="5c2e9-176">Caminho (recomendado): N/A</span><span class="sxs-lookup"><span data-stu-id="5c2e9-176">Path (Recommended): N/A</span></span>
  - <span data-ttu-id="5c2e9-177">Nome de valor: lista de REG_SZ</span><span class="sxs-lookup"><span data-stu-id="5c2e9-177">Value Name: list of REG_SZ</span></span>
  - <span data-ttu-id="5c2e9-178">Tipo de valor: lista de REG_SZ</span><span class="sxs-lookup"><span data-stu-id="5c2e9-178">Value Type: list of REG_SZ</span></span>

  ##### <a name="example-value"></a><span data-ttu-id="5c2e9-179">Valor de exemplo:</span><span class="sxs-lookup"><span data-stu-id="5c2e9-179">Example value:</span></span>

```
SOFTWARE\Policies\Microsoft\Edge\WebView2\ReleaseChannelPreference = "Name: *, Value: 1"

```

  

  [<span data-ttu-id="5c2e9-180">Voltar ao início</span><span class="sxs-lookup"><span data-stu-id="5c2e9-180">Back to top</span></span>](#microsoft-edge-webview2---policies)


## <a name="see-also"></a><span data-ttu-id="5c2e9-181">Consulte também</span><span class="sxs-lookup"><span data-stu-id="5c2e9-181">See also</span></span>

- [<span data-ttu-id="5c2e9-182">Configurar o Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="5c2e9-182">Configuring Microsoft Edge</span></span>](configure-microsoft-edge.md)
- [<span data-ttu-id="5c2e9-183">Página de aterrissagem do Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="5c2e9-183">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="5c2e9-184">Blog de linhas de base de segurança da Microsoft</span><span class="sxs-lookup"><span data-stu-id="5c2e9-184">Microsoft Security Baselines Blog</span></span>](https://techcommunity.microsoft.com/t5/microsoft-security-baselines/bg-p/Microsoft-Security-Baselines)