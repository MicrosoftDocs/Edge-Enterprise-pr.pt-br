---
title: Documentação de política do navegador Microsoft Edge
ms.author: stmoody
author: brianalt-msft
manager: tahills
ms.date: 10/08/2020
audience: ITPro
ms.topic: reference
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
ms.custom: ''
description: Documentação do Windows e do Mac para todas as políticas compatíveis com o Microsoft Edge Browser
ms.openlocfilehash: 56abadf907dfffec733af2456cc20db36510880b
ms.sourcegitcommit: 4e6188ade942ca6fd599a4ce1c8e0d90d3d03399
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2020
ms.locfileid: "11105737"
---
# <span data-ttu-id="6fff8-103">Políticas do Microsoft Edge WebView2</span><span class="sxs-lookup"><span data-stu-id="6fff8-103">Microsoft Edge WebView2 - Policies</span></span>

<span data-ttu-id="6fff8-104">A versão mais recente do Microsoft Edge WebView2 inclui as políticas a seguir.</span><span class="sxs-lookup"><span data-stu-id="6fff8-104">The latest version of Microsoft Edge WebView2 includes the following policies.</span></span> <span data-ttu-id="6fff8-105">Você pode usar essas políticas para configurar como o Microsoft Edge WebView2 será executado em sua organização.</span><span class="sxs-lookup"><span data-stu-id="6fff8-105">You can use these policies to configure how Microsoft Edge WebView2 runs in your organization.</span></span>

<span data-ttu-id="6fff8-106">Para saber mais sobre o conjunto adicional de políticas, usado para controlar como e quando o Microsoft Edge WebView2 é atualizado, confira [Referência de política de atualização do Microsoft Edge](microsoft-edge-update-policies.md).</span><span class="sxs-lookup"><span data-stu-id="6fff8-106">For information about an additional set of policies used to control how and when Microsoft Edge WebView2 is updated, check out [Microsoft Edge update policy reference](microsoft-edge-update-policies.md).</span></span>

> [!NOTE]
> <span data-ttu-id="6fff8-107">Este artigo se aplica ao Microsoft Edge versão 87 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="6fff8-107">This article applies to Microsoft Edge version 87 or later.</span></span>

## <span data-ttu-id="6fff8-108">Políticas disponíveis</span><span class="sxs-lookup"><span data-stu-id="6fff8-108">Available policies</span></span>
<span data-ttu-id="6fff8-109">Estas tabelas listam todas as políticas de grupo disponíveis nesta versão do Microsoft Edge WebView2.</span><span class="sxs-lookup"><span data-stu-id="6fff8-109">These tables list all of the group policies available in this release of Microsoft Edge WebView2.</span></span> <span data-ttu-id="6fff8-110">Use os links na tabela a seguir para obter mais detalhes sobre políticas específicas.</span><span class="sxs-lookup"><span data-stu-id="6fff8-110">Use the links in the table to get more details about specific policies.</span></span>

|||
|-|-|
|[<span data-ttu-id="6fff8-111">Configurações de substituição do carregador</span><span class="sxs-lookup"><span data-stu-id="6fff8-111">Loader Override Settings</span></span>](#loader-override-settings)|

### [*<span data-ttu-id="6fff8-112">Configurações de substituição do carregador</span><span class="sxs-lookup"><span data-stu-id="6fff8-112">Loader Override Settings</span></span>*](#loader-override-settings-policies)
|<span data-ttu-id="6fff8-113">Nome da política</span><span class="sxs-lookup"><span data-stu-id="6fff8-113">Policy Name</span></span>|<span data-ttu-id="6fff8-114">Legenda</span><span class="sxs-lookup"><span data-stu-id="6fff8-114">Caption</span></span>|
|-|-|
|[<span data-ttu-id="6fff8-115">browserExecutableFolder</span><span class="sxs-lookup"><span data-stu-id="6fff8-115">browserExecutableFolder</span></span>](#browserexecutablefolder)|<span data-ttu-id="6fff8-116">Configurar o local da pasta executável do navegador</span><span class="sxs-lookup"><span data-stu-id="6fff8-116">Configure the location of the browser executable folder</span></span>|
|[<span data-ttu-id="6fff8-117">releaseChannelPreference</span><span class="sxs-lookup"><span data-stu-id="6fff8-117">releaseChannelPreference</span></span>](#releasechannelpreference)|<span data-ttu-id="6fff8-118">Definir a preferência de ordem de pesquisa do canal de lançamento</span><span class="sxs-lookup"><span data-stu-id="6fff8-118">Set the release channel search order preference</span></span>|




  ## <span data-ttu-id="6fff8-119">Políticas de configurações de substituição do carregador</span><span class="sxs-lookup"><span data-stu-id="6fff8-119">Loader Override Settings policies</span></span>

  [<span data-ttu-id="6fff8-120">Voltar ao início</span><span class="sxs-lookup"><span data-stu-id="6fff8-120">Back to top</span></span>](#microsoft-edge-webview2---policies)

  ### <span data-ttu-id="6fff8-121">browserExecutableFolder</span><span class="sxs-lookup"><span data-stu-id="6fff8-121">browserExecutableFolder</span></span>
  #### <span data-ttu-id="6fff8-122">Configurar o local da pasta executável do navegador</span><span class="sxs-lookup"><span data-stu-id="6fff8-122">Configure the location of the browser executable folder</span></span>
  
  
  #### <span data-ttu-id="6fff8-123">Versões com suporte:</span><span class="sxs-lookup"><span data-stu-id="6fff8-123">Supported versions:</span></span>
  - <span data-ttu-id="6fff8-124">No Windows desde 87 ou posterior</span><span class="sxs-lookup"><span data-stu-id="6fff8-124">On Windows since 87 or later</span></span>

  #### <span data-ttu-id="6fff8-125">Descrição</span><span class="sxs-lookup"><span data-stu-id="6fff8-125">Description</span></span>
  <span data-ttu-id="6fff8-126">Essa política configura aplicativos de WebView2 para usar o WebView2 Runtime no caminho especificado.</span><span class="sxs-lookup"><span data-stu-id="6fff8-126">This policy configures WebView2 applications to use the WebView2 Runtime in the specified path.</span></span> <span data-ttu-id="6fff8-127">A pasta deve conter os seguintes arquivos: msedgewebview2.exe, msedge.dll e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="6fff8-127">The folder should contain the following files: msedgewebview2.exe, msedge.dll, and so on.</span></span>

<span data-ttu-id="6fff8-128">Para definir o valor do caminho da pasta, forneça um Nome do valor e um Par do valor.</span><span class="sxs-lookup"><span data-stu-id="6fff8-128">To set the value for the folder path, provide a Value name and Value pair.</span></span> <span data-ttu-id="6fff8-129">Defina o nome do valor para a ID do Modelo de Usuário do Aplicativo ou o nome do arquivo executável.</span><span class="sxs-lookup"><span data-stu-id="6fff8-129">Set value name to the Application User Model ID or the executable file name.</span></span> <span data-ttu-id="6fff8-130">Você pode usar o caractere curinga "\*" como nome do valor a ser aplicado a todos os aplicativos.</span><span class="sxs-lookup"><span data-stu-id="6fff8-130">You can use the "\*" wildcard as value name to apply to all applications.</span></span>

  #### <span data-ttu-id="6fff8-131">Recursos compatíveis:</span><span class="sxs-lookup"><span data-stu-id="6fff8-131">Supported features:</span></span>
  - <span data-ttu-id="6fff8-132">Pode ser obrigatório: Sim</span><span class="sxs-lookup"><span data-stu-id="6fff8-132">Can be mandatory: Yes</span></span>
  - <span data-ttu-id="6fff8-133">Pode ser recomendável: não</span><span class="sxs-lookup"><span data-stu-id="6fff8-133">Can be recommended: No</span></span>
  - <span data-ttu-id="6fff8-134">Atualização dinâmica das políticas: Sim</span><span class="sxs-lookup"><span data-stu-id="6fff8-134">Dynamic Policy Refresh: Yes</span></span>

  #### <span data-ttu-id="6fff8-135">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="6fff8-135">Data Type:</span></span>
  - <span data-ttu-id="6fff8-136">Lista de cadeias de caracteres</span><span class="sxs-lookup"><span data-stu-id="6fff8-136">List of strings</span></span>

  #### <span data-ttu-id="6fff8-137">Informações e configurações do Windows</span><span class="sxs-lookup"><span data-stu-id="6fff8-137">Windows information and settings</span></span>
  ##### <span data-ttu-id="6fff8-138">Informações da Política de Grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="6fff8-138">Group Policy (ADMX) info</span></span>
  - <span data-ttu-id="6fff8-139">Nome exclusivo da PG: browserExecutableFolder</span><span class="sxs-lookup"><span data-stu-id="6fff8-139">GP unique name: browserExecutableFolder</span></span>
  - <span data-ttu-id="6fff8-140">Nome da PG: Configurar o local da pasta executável do navegador</span><span class="sxs-lookup"><span data-stu-id="6fff8-140">GP name: Configure the location of the browser executable folder</span></span>
  - <span data-ttu-id="6fff8-141">Caminho da PG (obrigatório): Modelos administrativos/Microsoft Edge WebView2/Configurações de substituição do carregador</span><span class="sxs-lookup"><span data-stu-id="6fff8-141">GP path (Mandatory): Administrative Templates/Microsoft Edge WebView2/Loader Override Settings</span></span>
  - <span data-ttu-id="6fff8-142">Caminho da Política de Grupo (recomendado): N/A</span><span class="sxs-lookup"><span data-stu-id="6fff8-142">GP path (Recommended): N/A</span></span>
  - <span data-ttu-id="6fff8-143">Nome do arquivo ADMX da PG: MSEdgeWebView2.admx</span><span class="sxs-lookup"><span data-stu-id="6fff8-143">GP ADMX file name: MSEdgeWebView2.admx</span></span>
  ##### <span data-ttu-id="6fff8-144">Configurações de registro do Windows</span><span class="sxs-lookup"><span data-stu-id="6fff8-144">Windows Registry Settings</span></span>
  - <span data-ttu-id="6fff8-145">Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge\WebView2\browserExecutableFolder</span><span class="sxs-lookup"><span data-stu-id="6fff8-145">Path (Mandatory): SOFTWARE\Policies\Microsoft\Edge\WebView2\browserExecutableFolder</span></span>
  - <span data-ttu-id="6fff8-146">Caminho (recomendado): N/A</span><span class="sxs-lookup"><span data-stu-id="6fff8-146">Path (Recommended): N/A</span></span>
  - <span data-ttu-id="6fff8-147">Nome de valor: lista de REG_SZ</span><span class="sxs-lookup"><span data-stu-id="6fff8-147">Value Name: list of REG_SZ</span></span>
  - <span data-ttu-id="6fff8-148">Tipo de valor: lista de REG_SZ</span><span class="sxs-lookup"><span data-stu-id="6fff8-148">Value Type: list of REG_SZ</span></span>
  ##### <span data-ttu-id="6fff8-149">Valor de exemplo:</span><span class="sxs-lookup"><span data-stu-id="6fff8-149">Example value:</span></span>
```
SOFTWARE\Policies\Microsoft\Edge\WebView2\browserExecutableFolder = "Name: *, Value: C:\\Program Files\\Microsoft Edge WebView2 Runtime Redistributable 85.0.541.0 x64"

```


  

  [<span data-ttu-id="6fff8-150">Voltar ao início</span><span class="sxs-lookup"><span data-stu-id="6fff8-150">Back to top</span></span>](#microsoft-edge-webview2---policies)

  ### <span data-ttu-id="6fff8-151">releaseChannelPreference</span><span class="sxs-lookup"><span data-stu-id="6fff8-151">releaseChannelPreference</span></span>
  #### <span data-ttu-id="6fff8-152">Definir a preferência de ordem de pesquisa do canal de lançamento</span><span class="sxs-lookup"><span data-stu-id="6fff8-152">Set the release channel search order preference</span></span>
  
  
  #### <span data-ttu-id="6fff8-153">Versões com suporte:</span><span class="sxs-lookup"><span data-stu-id="6fff8-153">Supported versions:</span></span>
  - <span data-ttu-id="6fff8-154">No Windows desde 87 ou posterior</span><span class="sxs-lookup"><span data-stu-id="6fff8-154">On Windows since 87 or later</span></span>

  #### <span data-ttu-id="6fff8-155">Descrição</span><span class="sxs-lookup"><span data-stu-id="6fff8-155">Description</span></span>
  <span data-ttu-id="6fff8-156">O pedido padrão de pesquisa de canal é WebView2 Runtime, Beta, Dev e Canary.</span><span class="sxs-lookup"><span data-stu-id="6fff8-156">The default channel search order is WebView2 Runtime, Beta, Dev, and Canary.</span></span>

<span data-ttu-id="6fff8-157">Para inverter a ordem de pesquisa padrão, defina essa política como 1.</span><span class="sxs-lookup"><span data-stu-id="6fff8-157">To reverse the default search order, set this policy to 1.</span></span>

<span data-ttu-id="6fff8-158">Para definir o valor da preferência de canal de lançamento, forneça um Nome do valor e um Par do valor.</span><span class="sxs-lookup"><span data-stu-id="6fff8-158">To set the value for the release channel preference, provide a Value name and Value pair.</span></span> <span data-ttu-id="6fff8-159">Defina o nome do valor para a ID do Modelo de Usuário do Aplicativo ou o nome do arquivo executável.</span><span class="sxs-lookup"><span data-stu-id="6fff8-159">Set value name to the Application User Model ID or the executable file name.</span></span> <span data-ttu-id="6fff8-160">Você pode usar o caractere curinga "\*" como nome do valor a ser aplicado a todos os aplicativos.</span><span class="sxs-lookup"><span data-stu-id="6fff8-160">You can use the "\*" wildcard as value name to apply to all applications.</span></span>

  #### <span data-ttu-id="6fff8-161">Recursos compatíveis:</span><span class="sxs-lookup"><span data-stu-id="6fff8-161">Supported features:</span></span>
  - <span data-ttu-id="6fff8-162">Pode ser obrigatório: Sim</span><span class="sxs-lookup"><span data-stu-id="6fff8-162">Can be mandatory: Yes</span></span>
  - <span data-ttu-id="6fff8-163">Pode ser recomendável: não</span><span class="sxs-lookup"><span data-stu-id="6fff8-163">Can be recommended: No</span></span>
  - <span data-ttu-id="6fff8-164">Atualização dinâmica das políticas: Sim</span><span class="sxs-lookup"><span data-stu-id="6fff8-164">Dynamic Policy Refresh: Yes</span></span>

  #### <span data-ttu-id="6fff8-165">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="6fff8-165">Data Type:</span></span>
  - <span data-ttu-id="6fff8-166">Lista de cadeias de caracteres</span><span class="sxs-lookup"><span data-stu-id="6fff8-166">List of strings</span></span>

  #### <span data-ttu-id="6fff8-167">Informações e configurações do Windows</span><span class="sxs-lookup"><span data-stu-id="6fff8-167">Windows information and settings</span></span>
  ##### <span data-ttu-id="6fff8-168">Informações da Política de Grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="6fff8-168">Group Policy (ADMX) info</span></span>
  - <span data-ttu-id="6fff8-169">Nome exclusivo da PG: releaseChannelPreference</span><span class="sxs-lookup"><span data-stu-id="6fff8-169">GP unique name: releaseChannelPreference</span></span>
  - <span data-ttu-id="6fff8-170">Nome da PG: Definir a preferência de ordem de pesquisa do canal de lançamento</span><span class="sxs-lookup"><span data-stu-id="6fff8-170">GP name: Set the release channel search order preference</span></span>
  - <span data-ttu-id="6fff8-171">Caminho da PG (obrigatório): Modelos administrativos/Microsoft Edge WebView2/Configurações de substituição do carregador</span><span class="sxs-lookup"><span data-stu-id="6fff8-171">GP path (Mandatory): Administrative Templates/Microsoft Edge WebView2/Loader Override Settings</span></span>
  - <span data-ttu-id="6fff8-172">Caminho da Política de Grupo (recomendado): N/A</span><span class="sxs-lookup"><span data-stu-id="6fff8-172">GP path (Recommended): N/A</span></span>
  - <span data-ttu-id="6fff8-173">Nome do arquivo ADMX da PG: MSEdgeWebView2.admx</span><span class="sxs-lookup"><span data-stu-id="6fff8-173">GP ADMX file name: MSEdgeWebView2.admx</span></span>
  ##### <span data-ttu-id="6fff8-174">Configurações de registro do Windows</span><span class="sxs-lookup"><span data-stu-id="6fff8-174">Windows Registry Settings</span></span>
  - <span data-ttu-id="6fff8-175">Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge\WebView2\releaseChannelPreference</span><span class="sxs-lookup"><span data-stu-id="6fff8-175">Path (Mandatory): SOFTWARE\Policies\Microsoft\Edge\WebView2\releaseChannelPreference</span></span>
  - <span data-ttu-id="6fff8-176">Caminho (recomendado): N/A</span><span class="sxs-lookup"><span data-stu-id="6fff8-176">Path (Recommended): N/A</span></span>
  - <span data-ttu-id="6fff8-177">Nome de valor: lista de REG_SZ</span><span class="sxs-lookup"><span data-stu-id="6fff8-177">Value Name: list of REG_SZ</span></span>
  - <span data-ttu-id="6fff8-178">Tipo de valor: lista de REG_SZ</span><span class="sxs-lookup"><span data-stu-id="6fff8-178">Value Type: list of REG_SZ</span></span>
  ##### <span data-ttu-id="6fff8-179">Valor de exemplo:</span><span class="sxs-lookup"><span data-stu-id="6fff8-179">Example value:</span></span>
```
SOFTWARE\Policies\Microsoft\Edge\WebView2\releaseChannelPreference = "Name: *, Value: 1"

```


  

  [<span data-ttu-id="6fff8-180">Voltar ao início</span><span class="sxs-lookup"><span data-stu-id="6fff8-180">Back to top</span></span>](#microsoft-edge-webview2---policies)


## <span data-ttu-id="6fff8-181">Consulte também</span><span class="sxs-lookup"><span data-stu-id="6fff8-181">See also</span></span>
- [<span data-ttu-id="6fff8-182">Configurar o Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="6fff8-182">Configuring Microsoft Edge</span></span>](configure-microsoft-edge.md)
- [<span data-ttu-id="6fff8-183">Página de aterrissagem do Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="6fff8-183">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="6fff8-184">Blog de linhas de base de segurança da Microsoft</span><span class="sxs-lookup"><span data-stu-id="6fff8-184">Microsoft Security Baselines Blog</span></span>](https://techcommunity.microsoft.com/t5/microsoft-security-baselines/bg-p/Microsoft-Security-Baselines)