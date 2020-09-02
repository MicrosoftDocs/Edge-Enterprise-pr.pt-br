---
title: Configurar o Microsoft Edge usando o Gerenciamento de Dispositivo Móvel
ms.author: kvice
author: dan-wesley
manager: laurawi
ms.date: 10/25/2019
audience: ITPro
ms.topic: technical
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Configurar o Microsoft Edge usando o Gerenciamento de Dispositivo Móvel.
ms.openlocfilehash: dda35199f653b3dfb8f20b33b068c59621222b36
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10978997"
---
# <span data-ttu-id="d4bfd-103">Configurar o Microsoft Edge usando o Gerenciamento de Dispositivo Móvel</span><span class="sxs-lookup"><span data-stu-id="d4bfd-103">Configure Microsoft Edge using Mobile Device Management</span></span>

<span data-ttu-id="d4bfd-104">Este artigo explica como configurar o Microsoft Edge no Windows 10 usando o [Gerenciamento de Dispositivo Móvel (MDM)](https://docs.microsoft.com/windows/client-management/mdm/) por meio da [Ingestão de ADMX](https://docs.microsoft.com/windows/client-management/mdm/win32-and-centennial-app-policy-configuration).</span><span class="sxs-lookup"><span data-stu-id="d4bfd-104">This article explains how to configure Microsoft Edge on Windows 10 using [Mobile Device Management (MDM)](https://docs.microsoft.com/windows/client-management/mdm/) by means of [ADMX Ingestion](https://docs.microsoft.com/windows/client-management/mdm/win32-and-centennial-app-policy-configuration).</span></span> <span data-ttu-id="d4bfd-105">Este artigo também descreve:</span><span class="sxs-lookup"><span data-stu-id="d4bfd-105">This article also describes:</span></span>

- <span data-ttu-id="d4bfd-106">Como [criar um OMA-URI (Open Mobile Alliance Uniform Resource Identifier) para políticas do Microsoft Edge](#create-an-oma-uri-for-microsoft-edge-policies).</span><span class="sxs-lookup"><span data-stu-id="d4bfd-106">How to [create Open Mobile Alliance Uniform Resource Identifier (OMA-URI) for Microsoft Edge policies](#create-an-oma-uri-for-microsoft-edge-policies).</span></span>
- <span data-ttu-id="d4bfd-107">Como [configurar o Microsoft Edge no Intune usando a ingestão de ADMX e o OMA-URI personalizado](#configure-microsoft-edge-in-intune-using-admx-ingestion).</span><span class="sxs-lookup"><span data-stu-id="d4bfd-107">How to [configure Microsoft Edge in Intune using ADMX ingestion and custom OMA-URI](#configure-microsoft-edge-in-intune-using-admx-ingestion).</span></span>

> [!NOTE]
> <span data-ttu-id="d4bfd-108">Este artigo aplica-se ao Microsoft Edge versão 77 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-108">This article applies to Microsoft Edge version 77 or later.</span></span>

## <span data-ttu-id="d4bfd-109">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="d4bfd-109">Prerequisites</span></span>

<span data-ttu-id="d4bfd-110">Windows 10 com os seguintes requisitos mínimos do sistema:</span><span class="sxs-lookup"><span data-stu-id="d4bfd-110">Windows 10, with the following minimum system requirements:</span></span>

- <span data-ttu-id="d4bfd-111">Windows 10, versão 1903 com [KB4512941](https://support.microsoft.com/help/4512941/) e [KB4517211](https://support.microsoft.com/help/4517211/) instalados</span><span class="sxs-lookup"><span data-stu-id="d4bfd-111">Windows 10, version 1903 with [KB4512941](https://support.microsoft.com/help/4512941/) and [KB4517211](https://support.microsoft.com/help/4517211/) installed</span></span>
- <span data-ttu-id="d4bfd-112">Windows 10, versão 1809 com [KB4512534](https://support.microsoft.com/help/4512534/) e [KB4520062](https://support.microsoft.com/help/4520062/) instalados</span><span class="sxs-lookup"><span data-stu-id="d4bfd-112">Windows 10, version 1809 with [KB4512534](https://support.microsoft.com/help/4512534/) and [KB4520062](https://support.microsoft.com/help/4520062/) installed</span></span>
- <span data-ttu-id="d4bfd-113">Windows 10, versão 1803 com [KB4512509](https://support.microsoft.com/help/4512509/) e [KB4519978](https://support.microsoft.com/help/4519978) instalados</span><span class="sxs-lookup"><span data-stu-id="d4bfd-113">Windows 10, version 1803 with [KB4512509](https://support.microsoft.com/help/4512509/) and [KB4519978](https://support.microsoft.com/help/4519978) installed</span></span>
- <span data-ttu-id="d4bfd-114">Windows 10, versão 1709 com [KB4516071](https://support.microsoft.com/help/4516071/) e [KB4520006](https://support.microsoft.com/help/4520006) instalados</span><span class="sxs-lookup"><span data-stu-id="d4bfd-114">Windows 10, version 1709 with [KB4516071](https://support.microsoft.com/help/4516071/) and [KB4520006](https://support.microsoft.com/help/4520006) installed</span></span>

## <span data-ttu-id="d4bfd-115">Visão geral</span><span class="sxs-lookup"><span data-stu-id="d4bfd-115">Overview</span></span>

<span data-ttu-id="d4bfd-116">Você pode configurar o Microsoft Edge no Windows 10 usando o MDM com seu provedor de EMM (Gerenciamento de Mobilidade Empresarial) ou MDM preferencial que dê suporte à [Ingestão de ADMX](https://docs.microsoft.com/windows/client-management/mdm/win32-and-centennial-app-policy-configuration).</span><span class="sxs-lookup"><span data-stu-id="d4bfd-116">You can configure Microsoft Edge on Windows 10 using MDM with your preferred Enterprise Mobility Management (EMM) or MDM provider that supports [ADMX Ingestion](https://docs.microsoft.com/windows/client-management/mdm/win32-and-centennial-app-policy-configuration).</span></span>

<span data-ttu-id="d4bfd-117">Configurar o Microsoft Edge com MDM é um processo de duas partes:</span><span class="sxs-lookup"><span data-stu-id="d4bfd-117">Configuring Microsoft Edge with MDM is a two part process:</span></span>

1. <span data-ttu-id="d4bfd-118">A ingestão do arquivo ADMX do Microsoft Edge no seu provedor de EMM ou MDM.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-118">Ingesting the Microsoft Edge ADMX file into your EMM or MDM provider.</span></span> <span data-ttu-id="d4bfd-119">Consulte seu provedor para obter instruções sobre como ingerir um arquivo ADMX.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-119">See your provider for instructions on how to ingest an ADMX file.</span></span>

   > [!NOTE]
   > <span data-ttu-id="d4bfd-120">Para o Microsoft Intune, consulte [Configurar o Microsoft Edge no Intune usando a ingestão de ADMX](#configure-microsoft-edge-in-intune-using-admx-ingestion).</span><span class="sxs-lookup"><span data-stu-id="d4bfd-120">For Microsoft Intune, see [Configure Microsoft Edge in Intune using ADMX ingestion](#configure-microsoft-edge-in-intune-using-admx-ingestion).</span></span>

2. <span data-ttu-id="d4bfd-121">[Como criar um OMA-URI para uma política do Microsoft Edge](#create-an-oma-uri-for-microsoft-edge-policies).</span><span class="sxs-lookup"><span data-stu-id="d4bfd-121">[Creating an OMA-URI for a Microsoft Edge policy](#create-an-oma-uri-for-microsoft-edge-policies).</span></span>

## <span data-ttu-id="d4bfd-122">Criar um OMA-URI para políticas do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="d4bfd-122">Create an OMA-URI for Microsoft Edge policies</span></span>

<span data-ttu-id="d4bfd-123">As seções a seguir descrevem como criar o caminho OMA-URI e pesquisar e definir o valor no formato XML para políticas de navegador obrigatórias e recomendadas.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-123">The following sections describe how to create the OMA-URI path and look up and define the value in XML format for mandatory and recommended browser polices.</span></span>

<span data-ttu-id="d4bfd-124">Antes de começar, baixe o arquivo de modelos de política do Microsoft Edge (MicrosoftEdgePolicyTemplates.cab) da [página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise) e extraia o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-124">Before you get started download the Microsoft Edge policy templates file (MicrosoftEdgePolicyTemplates.cab) from the [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise) and extract the contents.</span></span>

<span data-ttu-id="d4bfd-125">Há três etapas para definir o OMA-URI:</span><span class="sxs-lookup"><span data-stu-id="d4bfd-125">There are three steps for defining the OMA-URI:</span></span>

1. [<span data-ttu-id="d4bfd-126">Criar o caminho OMA-URI</span><span class="sxs-lookup"><span data-stu-id="d4bfd-126">Create the OMA-URI path</span></span>](#create-the-oma-uri-path)
2. [<span data-ttu-id="d4bfd-127">Especificar o tipo de dados OMA-URI</span><span class="sxs-lookup"><span data-stu-id="d4bfd-127">Specify the OMA-URI data type</span></span>](#specify-the-data-type)
3. [<span data-ttu-id="d4bfd-128">Definir o valor do OMA-URI</span><span class="sxs-lookup"><span data-stu-id="d4bfd-128">Set the OMA-URI value</span></span>](#set-the-value-for-a-browser-policy)

### <span data-ttu-id="d4bfd-129">Criar o caminho OMA-URI</span><span class="sxs-lookup"><span data-stu-id="d4bfd-129">Create the OMA-URI path</span></span>

<span data-ttu-id="d4bfd-130">Use a fórmula a seguir como um guia para criar os caminhos OMA-URI.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-130">Use the following formula as a guide for creating the OMA-URI paths.</span></span> <br/><br/>
*`./Device/Vendor/MSFT/Policy/Config/<ADMXIngestName>~Policy~<ADMXNamespace>~<ADMXCategory>/<PolicyName>`* <br/><br/>

| <span data-ttu-id="d4bfd-131">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="d4bfd-131">Parameter</span></span>         | <span data-ttu-id="d4bfd-132">Descrição</span><span class="sxs-lookup"><span data-stu-id="d4bfd-132">Description</span></span>                                                                                   |
|-------------------|-----------------------------------------------------------------------------------------------|
| \<ADMXIngestName> | <span data-ttu-id="d4bfd-133">Use "Edge" ou o que você definiu ao ingerir o modelo administrativo.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-133">Use "Edge" or what you defined when ingesting the administrative template.</span></span> <span data-ttu-id="d4bfd-134">Por exemplo, se você tiver usado "./Device/Vendor/MSFT/Policy/ConfigOperations/ADMXInstall/MicrosoftEdge/Policy/EdgeAdmx", então use "MicrosoftEdge".</span><span class="sxs-lookup"><span data-stu-id="d4bfd-134">For example, if you used "./Device/Vendor/MSFT/Policy/ConfigOperations/ADMXInstall/MicrosoftEdge/Policy/EdgeAdmx", then use "MicrosoftEdge".</span></span><br/><br/> <span data-ttu-id="d4bfd-135">O `<ADMXIngestionName>` deve corresponder ao que foi usado quando o arquivo ADMX foi ingerido.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-135">The `<ADMXIngestionName>` must match what was used when you ingested the ADMX file.</span></span> |
| \<ADMXNamespace>  | <span data-ttu-id="d4bfd-136">"microsoft_edge" ou "microsoft_edge_recommended", dependendo de você estar definindo uma política obrigatória ou recomendada.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-136">Either "microsoft_edge" or "microsoft_edge_recommended" depending on whether you're setting a mandatory or recommended policy.</span></span> |
| \<ADMXCategory>   | <span data-ttu-id="d4bfd-137">O "parentCategory" da política é definido no arquivo ADMX.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-137">The "parentCategory" of the policy is defined in the ADMX file.</span></span> <span data-ttu-id="d4bfd-138">Omita `<ADMXCategory>` se a política não estiver agrupada (nenhuma "parentCategory" definida).</span><span class="sxs-lookup"><span data-stu-id="d4bfd-138">Omit the `<ADMXCategory>` if the policy isn't grouped (No "parentCategory" defined).</span></span> |
| \<PolicyName>     | <span data-ttu-id="d4bfd-139">O nome da política pode ser encontrado no artigo [Referência de política do navegador](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies).</span><span class="sxs-lookup"><span data-stu-id="d4bfd-139">The policy name can be found in the [Browser policy reference](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies) article.</span></span> |

#### <span data-ttu-id="d4bfd-140">Exemplo de caminho de URI:</span><span class="sxs-lookup"><span data-stu-id="d4bfd-140">URI path example:</span></span>

<span data-ttu-id="d4bfd-141">Neste exemplo, suponha que o nó `<ADMXIngestName>` tenha sido nomeado como "Edge" e que você está definindo uma política obrigatória.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-141">For this example, assume the `<ADMXIngestName>` node was named “Edge" and you're setting a mandatory policy.</span></span> <span data-ttu-id="d4bfd-142">O caminho do URI seria:</span><span class="sxs-lookup"><span data-stu-id="d4bfd-142">The URI path would be:</span></span><br/><br/>
*`./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~<ADMXCategory>/<PolicyName>`*

<span data-ttu-id="d4bfd-143">Se a política não estiver em um grupo (por exemplo, DiskCacheSize), remova "`~<ADMXCategory>`".</span><span class="sxs-lookup"><span data-stu-id="d4bfd-143">If the policy isn't in a group (for example, DiskCacheSize) remove "`~<ADMXCategory>`".</span></span> <span data-ttu-id="d4bfd-144">Substitua `<PolicyName>` pelo nome da política, DiskCacheSize.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-144">Replace `<PolicyName>` with the name of the policy, DiskCacheSize.</span></span> <span data-ttu-id="d4bfd-145">O caminho do URI seria:</span><span class="sxs-lookup"><span data-stu-id="d4bfd-145">The URI path would be:</span></span><br/><br/>
*`./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge/DiskCacheSize`*

<span data-ttu-id="d4bfd-146">Se a política estiver em um grupo, siga estas etapas:</span><span class="sxs-lookup"><span data-stu-id="d4bfd-146">If the policy is in a group, follow these steps:</span></span>

1. <span data-ttu-id="d4bfd-147">Abra **msedge.admx** com qualquer editor xml.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-147">Open **msedge.admx** with any xml editor.</span></span>
2. <span data-ttu-id="d4bfd-148">Procure o nome da política que você deseja definir.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-148">Search for the policy name you want to set.</span></span> <span data-ttu-id="d4bfd-149">Por exemplo, "ExtensionInstallForceList".</span><span class="sxs-lookup"><span data-stu-id="d4bfd-149">For example, "ExtensionInstallForceList".</span></span>
3. <span data-ttu-id="d4bfd-150">Use o valor do atributo *ref* do elemento *parentCategory*.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-150">Use the value of the *ref* attribute from the *parentCategory* element.</span></span> <span data-ttu-id="d4bfd-151">Por exemplo, "extensões" de \<parentCategory ref=" Extensions"/>.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-151">For example, "Extensions" from \<parentCategory ref=" Extensions"/>.</span></span>
4. <span data-ttu-id="d4bfd-152">Substitua `<ADMXCategory>` pelo valor do atributo *ref* para construir o caminho do URI.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-152">Replace `<ADMXCategory>` with the *ref* attribute value to construct the URI path.</span></span> <span data-ttu-id="d4bfd-153">O caminho URI seria:</span><span class="sxs-lookup"><span data-stu-id="d4bfd-153">The URI path would be:</span></span><br/><br/>
*`/Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~Extensions/ExtensionInstallForcelist`*

### <span data-ttu-id="d4bfd-154">Especificar o tipo de dados</span><span class="sxs-lookup"><span data-stu-id="d4bfd-154">Specify the data type</span></span>

<span data-ttu-id="d4bfd-155">O tipo de dados OMA-URI sempre será "String".</span><span class="sxs-lookup"><span data-stu-id="d4bfd-155">The OMA-URI data type is always “String”.</span></span>

### <span data-ttu-id="d4bfd-156">Definir o valor de uma política do navegador</span><span class="sxs-lookup"><span data-stu-id="d4bfd-156">Set the value for a browser policy</span></span>

<span data-ttu-id="d4bfd-157">Esta seção descreve como definir o valor, em formato XML, para cada tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-157">This section describes how to set the value, in XML format, for each data type.</span></span> <span data-ttu-id="d4bfd-158">Vá para [Referência de política do navegador](https://docs.microsoft.com/deployedge/microsoft-edge-policies) para procurar o tipo de dados da política.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-158">Go to [Browser policy reference](https://docs.microsoft.com/deployedge/microsoft-edge-policies) to look up the data type of the policy.</span></span>

> [!NOTE]
> <span data-ttu-id="d4bfd-159">Para tipos de dados não Boolianos, o valor sempre começa com `<enabled/>`.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-159">For non-Boolean data types, the value always starts with `<enabled/>`.</span></span>

#### <span data-ttu-id="d4bfd-160">Tipo de dados Booliano</span><span class="sxs-lookup"><span data-stu-id="d4bfd-160">Boolean data type</span></span>

<span data-ttu-id="d4bfd-161">Para políticas que sejam tipos Boolianos, use `<enabled/>` ou `<disabled/>`.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-161">For policies that are Boolean types use `<enabled/>` or `<disabled/>`.</span></span>

#### <span data-ttu-id="d4bfd-162">Tipo de dados Integer</span><span class="sxs-lookup"><span data-stu-id="d4bfd-162">Integer data type</span></span>

<span data-ttu-id="d4bfd-163">O valor sempre precisará ser iniciado com o elemento `<enabled/>` seguido por `<data id="[valueName]" value="[decimal value]"/>`.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-163">The value always needs to start with the `<enabled/>` element followed by `<data id="[valueName]" value="[decimal value]"/>`.</span></span>

<span data-ttu-id="d4bfd-164">Para encontrar o nome do valor e o valor decimal para uma nova página de guia, use estas etapas:</span><span class="sxs-lookup"><span data-stu-id="d4bfd-164">To find the value name and decimal value for a new tab page, use the following steps:</span></span>

1. <span data-ttu-id="d4bfd-165">Abra **msedge.admx** com qualquer editor xml.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-165">Open **msedge.admx** with any xml editor.</span></span>
2. <span data-ttu-id="d4bfd-166">Procure o elemento `<policy>` em que o atributo de nome corresponda ao nome da política que você deseja definir.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-166">Search for the `<policy>` element where the name attribute matches the policy name you want to set.</span></span> <span data-ttu-id="d4bfd-167">Para "RestoreOnStartup", procure `name="RestoreOnStartup"`.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-167">For "RestoreOnStartup", search for `name="RestoreOnStartup"`.</span></span>
3. <span data-ttu-id="d4bfd-168">No nó `<elements>`, encontre o valor que você deseja definir.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-168">In the `<elements>` node, find the value you want to set.</span></span>
4. <span data-ttu-id="d4bfd-169">Use o valor no atributo "valueName" no nó `<elements>`.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-169">Use the value in the "valueName" attribute in the `<elements>` node.</span></span> <span data-ttu-id="d4bfd-170">Para "RestoreOnStartup", o "valueName" é "RestoreOnStartup".</span><span class="sxs-lookup"><span data-stu-id="d4bfd-170">For "RestoreOnStartup" the "valueName" is "RestoreOnStartup".</span></span>
5. <span data-ttu-id="d4bfd-171">Use o valor no atributo "value" no nó `<decimal>`.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-171">Use the value in the "value" attribute in the `<decimal>` node.</span></span> <span data-ttu-id="d4bfd-172">Para "RestoreOnStartup" abrir a página da nova guia, o valor é "5".</span><span class="sxs-lookup"><span data-stu-id="d4bfd-172">For "RestoreOnStartup" to open the new tab page the value is "5".</span></span>

<span data-ttu-id="d4bfd-173">Para abrir a nova página de guia na inicialização, use:</span><span class="sxs-lookup"><span data-stu-id="d4bfd-173">To open the new tab page on startup use:</span></span><br>
`<enabled/> <data id="RestoreOnStartup" value="5"/>`

#### <span data-ttu-id="d4bfd-174">Lista de tipos de dados de cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="d4bfd-174">List of strings data type</span></span>

<span data-ttu-id="d4bfd-175">O valor sempre precisará ser iniciado com o elemento `<enabled/>` seguido por `<data id="[listID]" value="[string 1];[string 2];[string 3]"/>`.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-175">The value always needs to start with the `<enabled/>` element followed by `<data id="[listID]" value="[string 1];[string 2];[string 3]"/>`.</span></span>

> [!NOTE]
> <span data-ttu-id="d4bfd-176">O nome do atributo "id=" não é o nome da política, mesmo se na maioria dos casos ele corresponder ao nome da política.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-176">The "id=" attribute name isn't the policy name, even though in most cases it matches the policy name.</span></span> <span data-ttu-id="d4bfd-177">É o valor do atributo de ID do nó \<list>, encontrado no arquivo ADMX.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-177">It's the \<list> node id attribute value, which is found in the ADMX file.</span></span>

<span data-ttu-id="d4bfd-178">Para localizar o listID e definir o valor para bloquear uma URL, siga estas etapas:</span><span class="sxs-lookup"><span data-stu-id="d4bfd-178">To find the listID and define the value to block a URL, follow these steps:</span></span>

1. <span data-ttu-id="d4bfd-179">Abra **msedge.admx** com qualquer editor xml.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-179">Open **msedge.admx** with any xml editor.</span></span>
2. <span data-ttu-id="d4bfd-180">Procure o elemento `<policy>` em que o atributo de nome corresponda ao nome da política que você deseja definir.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-180">Search for the `<policy>` element where the name attribute matches the policy name you want to set.</span></span> <span data-ttu-id="d4bfd-181">Para "URLBlocklist", procure `name="URLBlocklist"`.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-181">For "URLBlocklist", search for `name="URLBlocklist"`.</span></span>
3. <span data-ttu-id="d4bfd-182">Use o valor no atributo "id" do `<list> node for [listID]`.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-182">Use the value in the "id" attribute of the `<list> node for [listID]`.</span></span>
4. <span data-ttu-id="d4bfd-183">O "valor" é uma lista de URLs separadas por um ponto-e-vírgula (;)</span><span class="sxs-lookup"><span data-stu-id="d4bfd-183">The "value" is a list of URLs separated by a semicolon (;)</span></span>

<span data-ttu-id="d4bfd-184">Por exemplo, para bloquear o acesso a `contoso.com` e `https://ssl.server.com`:</span><span class="sxs-lookup"><span data-stu-id="d4bfd-184">For example, to block access to `contoso.com` and `https://ssl.server.com`:</span></span><br>
`<enabled/> <data id=" URLBlocklistDesc" value="contoso.com;https://ssl.server.com"/>`

#### <span data-ttu-id="d4bfd-185">Tipo de dados Dictionary ou String</span><span class="sxs-lookup"><span data-stu-id="d4bfd-185">Dictionary or String data type</span></span>

<span data-ttu-id="d4bfd-186">O valor sempre precisará ser iniciado com `<enabled/>` seguido por `<data id="[textID]" value="[string]"/>`.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-186">The value always needs to start with the `<enabled/>` followed by `<data id="[textID]" value="[string]"/>` .</span></span>

<span data-ttu-id="d4bfd-187">Para localizar a textID e definir o valor que defina a localidade, siga estas etapas:</span><span class="sxs-lookup"><span data-stu-id="d4bfd-187">To find the textID and define the value set the locale, follow these steps:</span></span>

1. <span data-ttu-id="d4bfd-188">Abra **msedge.admx** com qualquer editor xml.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-188">Open **msedge.admx** with any xml editor.</span></span>
2. <span data-ttu-id="d4bfd-189">Procure o elemento `<policy>` em que o atributo de nome corresponda ao nome da política que você deseja definir.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-189">Search for the `<policy>` element where the name attribute matches the policy name you want to set.</span></span> <span data-ttu-id="d4bfd-190">Para "ApplicationLocaleValue", procure `name="ApplicationLocaleValue"`.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-190">For "ApplicationLocaleValue", search for `name="ApplicationLocaleValue"`.</span></span>
3. <span data-ttu-id="d4bfd-191">Use o valor no atributo "id" do nó `<text>` para `[textID]`.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-191">Use the value in the "id" attribute of the `<text>` node for `[textID]`.</span></span>
4. <span data-ttu-id="d4bfd-192">Defina o "valor" com o código de cultura.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-192">Set the "value" to the culture code.</span></span>

<span data-ttu-id="d4bfd-193">Para definir a localidade como "es-US" com a política "ApplicationLocaleValue":</span><span class="sxs-lookup"><span data-stu-id="d4bfd-193">To set the locale to "es-US" with the "ApplicationLocaleValue" policy:</span></span><br>
`<enabled/> <data id="ApplicationLocaleValue" value="es-US"/>`

### <span data-ttu-id="d4bfd-194">Criar o OMA-URI para políticas recomendadas</span><span class="sxs-lookup"><span data-stu-id="d4bfd-194">Create the OMA-URI for a recommended policies</span></span>

<span data-ttu-id="d4bfd-195">Definir o caminho do URI para políticas recomendadas dependerá da política que você deseja configurar.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-195">Defining the URI path for recommended policies depends on the policy you want to configure.</span></span>

#### <span data-ttu-id="d4bfd-196">Para definir o caminho do URI para uma política recomendada</span><span class="sxs-lookup"><span data-stu-id="d4bfd-196">To define the URI path for a recommended policy</span></span>

<span data-ttu-id="d4bfd-197">Use a fórmula do caminho do URI (*`./Device/Vendor/MSFT/Policy/Config/<ADMXIngestName>~Policy~<ADMXNamespace>~<ADMXCategory>/<PolicyName>`*) e as etapas a seguir para definir o caminho do URI:</span><span class="sxs-lookup"><span data-stu-id="d4bfd-197">Use the URI path formula (*`./Device/Vendor/MSFT/Policy/Config/<ADMXIngestName>~Policy~<ADMXNamespace>~<ADMXCategory>/<PolicyName>`*) and the following steps to define the URI path:</span></span>

1. <span data-ttu-id="d4bfd-198">Abra **msedge.admx** com qualquer editor xml.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-198">Open **msedge.admx** with any xml editor.</span></span>
2. <span data-ttu-id="d4bfd-199">Se a política que você deseja configurar não estiver em um grupo, pule para a etapa 4 e remova `~<ADMXCategory>` do caminho.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-199">If the policy you want to configure isn't in a group, skip to step 4 and remove `~<ADMXCategory>` from the path.</span></span>
3. <span data-ttu-id="d4bfd-200">Se a política que você deseja configurar estiver em um grupo:</span><span class="sxs-lookup"><span data-stu-id="d4bfd-200">If the policy you want to configure is in a group:</span></span>

   - <span data-ttu-id="d4bfd-201">Para pesquisar a `<ADMXCategory>`, procure a política que você deseja definir.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-201">To look up the `<ADMXCategory>`, search for the policy you want to set.</span></span> <span data-ttu-id="d4bfd-202">Ao pesquisar, acrescente "_recommended" ao nome da política.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-202">When searching append "_recommended" to the policy name.</span></span> <span data-ttu-id="d4bfd-203">Por exemplo, uma pesquisa para "RegisteredProtocolHandlers_recommended” tem o seguinte resultado:</span><span class="sxs-lookup"><span data-stu-id="d4bfd-203">For example, a search for "RegisteredProtocolHandlers_recommended” has the following result:</span></span>

        ```xml
         <policy class="Both" displayName="$(string.RegisteredProtocolHandlers)" explainText="$(string.RegisteredProtocolHandlers_Explain)" key="Software\Policies\Microsoft\Edge\Recommended" name="RegisteredProtocolHandlers_recommended" presentation="$(presentation.RegisteredProtocolHandlers)">
           <parentCategory ref="ContentSettings_recommended"/>
           <supportedOn ref="SUPPORTED_WIN7_V77"/>
           <elements>
             <text id="RegisteredProtocolHandlers" maxLength="1000000" valueName="RegisteredProtocolHandlers"/>
           </elements>
         </policy>
        ```

   - <span data-ttu-id="d4bfd-204">Copie o valor do atributo *ref* do elemento `<parentCategory>`.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-204">Copy the value of the *ref* attribute from the `<parentCategory>` element.</span></span> <span data-ttu-id="d4bfd-205">Para "ContentSettings", copie "ContentSettings_recommended" de `<parentCategory ref=" ContentSettings_recommended"/>`.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-205">For "ContentSettings", copy "ContentSettings_recommended" from `<parentCategory ref=" ContentSettings_recommended"/>`.</span></span>
   - <span data-ttu-id="d4bfd-206">Substitua `<ADMXCategory>` pelo valor do atributo *ref* para construir o caminho do URI na fórmula de caminho do URI.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-206">Replace `<ADMXCategory>` with the *ref* attribute value to construct the URI path in the URI path formula.</span></span>

4. <span data-ttu-id="d4bfd-207">O `<PolicyName>` é o nome da política com "_recommended" anexado.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-207">The `<PolicyName>` is the name of the policy with "_recommended" appended to it.</span></span>

#### <span data-ttu-id="d4bfd-208">Exemplos de caminho OMA-URI para políticas recomendadas</span><span class="sxs-lookup"><span data-stu-id="d4bfd-208">OMA-URI path examples for recommended policies</span></span>

<span data-ttu-id="d4bfd-209">A tabela a seguir mostra exemplos de caminhos OMA-URI para políticas recomendadas.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-209">The following table shows examples of OMA-URI paths for recommended policies.</span></span>

|              <span data-ttu-id="d4bfd-210">Política</span><span class="sxs-lookup"><span data-stu-id="d4bfd-210">Policy</span></span>               |             <span data-ttu-id="d4bfd-211">OMA-URI</span><span class="sxs-lookup"><span data-stu-id="d4bfd-211">OMA-URI</span></span>                      |
|-----------------------------------|------------------------------------------|
| [<span data-ttu-id="d4bfd-212">RegisteredProtocolHandlers</span><span class="sxs-lookup"><span data-stu-id="d4bfd-212">RegisteredProtocolHandlers</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#registeredprotocolhandlers)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~ContentSettings_recommended/RegisteredProtocolHandlers_recommended`                        |
| [<span data-ttu-id="d4bfd-213">PasswordManagerEnabled</span><span class="sxs-lookup"><span data-stu-id="d4bfd-213">PasswordManagerEnabled</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#passwordmanagerenabled)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~PasswordManager_recommended/PasswordManagerEnabled_recommended`                        |
| [<span data-ttu-id="d4bfd-214">PrintHeaderFooter</span><span class="sxs-lookup"><span data-stu-id="d4bfd-214">PrintHeaderFooter</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#printheaderfooter)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~Printing_recommended/PrintHeaderFooter_recommended`                        |
| [<span data-ttu-id="d4bfd-215">SmartScreenEnabled</span><span class="sxs-lookup"><span data-stu-id="d4bfd-215">SmartScreenEnabled</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#smartscreenenabled)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~SmartScreen_recommended/SmartScreenEnabled_recommended`                        |
| [<span data-ttu-id="d4bfd-216">HomePageLocation</span><span class="sxs-lookup"><span data-stu-id="d4bfd-216">HomePageLocation</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#homepagelocation)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~Startup_recommended/HomepageLocation_recommended`                        |
| [<span data-ttu-id="d4bfd-217">ShowHomeButton</span><span class="sxs-lookup"><span data-stu-id="d4bfd-217">ShowHomeButton</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#showhomebutton)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~Startup_recommended/ShowHomeButton_recommended`                        |
| [<span data-ttu-id="d4bfd-218">FavoritesBarEnabled</span><span class="sxs-lookup"><span data-stu-id="d4bfd-218">FavoritesBarEnabled</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#favoritesbarenabled)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~/FavoritesBarEnabled_recommended`                        |

### <span data-ttu-id="d4bfd-219">Exemplos de OMA-URI</span><span class="sxs-lookup"><span data-stu-id="d4bfd-219">OMA-URI examples</span></span>

<span data-ttu-id="d4bfd-220">Os exemplos de OMA-URI com seu caminho do URI, tipo e um valor de exemplo.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-220">OMA-URI examples with their URI path, type, and an example value.</span></span>

#### <span data-ttu-id="d4bfd-221">Exemplos do tipo de dados Booliano</span><span class="sxs-lookup"><span data-stu-id="d4bfd-221">Boolean data type examples</span></span>

*<span data-ttu-id="d4bfd-222">[ShowHomeButton](https://docs.microsoft.com/deployedge/microsoft-edge-policies#ShowHomeButton):</span><span class="sxs-lookup"><span data-stu-id="d4bfd-222">[ShowHomeButton](https://docs.microsoft.com/deployedge/microsoft-edge-policies#ShowHomeButton):</span></span>*

| <span data-ttu-id="d4bfd-223">Campo</span><span class="sxs-lookup"><span data-stu-id="d4bfd-223">Field</span></span>   | <span data-ttu-id="d4bfd-224">Valor</span><span class="sxs-lookup"><span data-stu-id="d4bfd-224">Value</span></span>                                                                                |
|---------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d4bfd-225">Nome</span><span class="sxs-lookup"><span data-stu-id="d4bfd-225">Name</span></span>    | <span data-ttu-id="d4bfd-226">Microsoft Edge: ShowHomeButton</span><span class="sxs-lookup"><span data-stu-id="d4bfd-226">Microsoft Edge: ShowHomeButton</span></span>                                                       |
| <span data-ttu-id="d4bfd-227">OMA-URI</span><span class="sxs-lookup"><span data-stu-id="d4bfd-227">OMA-URI</span></span> | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~Startup/ShowHomeButton` |
| <span data-ttu-id="d4bfd-228">tipo</span><span class="sxs-lookup"><span data-stu-id="d4bfd-228">type</span></span>    | <span data-ttu-id="d4bfd-229">String</span><span class="sxs-lookup"><span data-stu-id="d4bfd-229">String</span></span>                                                                               |
| <span data-ttu-id="d4bfd-230">Valor</span><span class="sxs-lookup"><span data-stu-id="d4bfd-230">Value</span></span>   | `<enabled/>`                                                                          |

*<span data-ttu-id="d4bfd-231">[DefaultSearchProviderEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#DefaultSearchProviderEnabled):</span><span class="sxs-lookup"><span data-stu-id="d4bfd-231">[DefaultSearchProviderEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#DefaultSearchProviderEnabled):</span></span>*

| <span data-ttu-id="d4bfd-232">Campo</span><span class="sxs-lookup"><span data-stu-id="d4bfd-232">Field</span></span>   | <span data-ttu-id="d4bfd-233">Valor</span><span class="sxs-lookup"><span data-stu-id="d4bfd-233">Value</span></span>                                                                                |
|---------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d4bfd-234">Nome</span><span class="sxs-lookup"><span data-stu-id="d4bfd-234">Name</span></span>    | <span data-ttu-id="d4bfd-235">Microsoft Edge: DefaultSearchProviderEnabled</span><span class="sxs-lookup"><span data-stu-id="d4bfd-235">Microsoft Edge: DefaultSearchProviderEnabled</span></span>                                         |
| <span data-ttu-id="d4bfd-236">OMA-URI</span><span class="sxs-lookup"><span data-stu-id="d4bfd-236">OMA-URI</span></span> | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~DefaultSearchProvider/DefaultSearchProviderEnabled`    |
| <span data-ttu-id="d4bfd-237">tipo</span><span class="sxs-lookup"><span data-stu-id="d4bfd-237">type</span></span>    | <span data-ttu-id="d4bfd-238">String</span><span class="sxs-lookup"><span data-stu-id="d4bfd-238">String</span></span>                                                                               |
| <span data-ttu-id="d4bfd-239">Valor</span><span class="sxs-lookup"><span data-stu-id="d4bfd-239">Value</span></span>   | `<disable/>`                                                                          |

### <span data-ttu-id="d4bfd-240">Exemplos de tipo de dados Integer</span><span class="sxs-lookup"><span data-stu-id="d4bfd-240">Integer data type examples</span></span>

*<span data-ttu-id="d4bfd-241">[AutoImportAtFirstRun](https://docs.microsoft.com/deployedge/microsoft-edge-policies#AutoImportAtFirstRun):</span><span class="sxs-lookup"><span data-stu-id="d4bfd-241">[AutoImportAtFirstRun](https://docs.microsoft.com/deployedge/microsoft-edge-policies#AutoImportAtFirstRun):</span></span>*

| <span data-ttu-id="d4bfd-242">Campo</span><span class="sxs-lookup"><span data-stu-id="d4bfd-242">Field</span></span>   | <span data-ttu-id="d4bfd-243">Valor</span><span class="sxs-lookup"><span data-stu-id="d4bfd-243">Value</span></span>                                                                                |
|---------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d4bfd-244">Nome</span><span class="sxs-lookup"><span data-stu-id="d4bfd-244">Name</span></span>    | <span data-ttu-id="d4bfd-245">Microsoft Edge: AutoImportAtFirstRun</span><span class="sxs-lookup"><span data-stu-id="d4bfd-245">Microsoft Edge: AutoImportAtFirstRun</span></span>                                                 |
| <span data-ttu-id="d4bfd-246">OMA-URI</span><span class="sxs-lookup"><span data-stu-id="d4bfd-246">OMA-URI</span></span> | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge/AutoImportAtFirstRun`   |
| <span data-ttu-id="d4bfd-247">tipo</span><span class="sxs-lookup"><span data-stu-id="d4bfd-247">type</span></span>    | <span data-ttu-id="d4bfd-248">String</span><span class="sxs-lookup"><span data-stu-id="d4bfd-248">String</span></span>                                                                               |
| <span data-ttu-id="d4bfd-249">Valor</span><span class="sxs-lookup"><span data-stu-id="d4bfd-249">Value</span></span>   | `<enabled/><data id="AutoImportAtFirstRun" value="1"/>`                             |

*<span data-ttu-id="d4bfd-250">[DefaultImagesSetting](https://docs.microsoft.com/deployedge/microsoft-edge-policies#DefaultImagesSetting):</span><span class="sxs-lookup"><span data-stu-id="d4bfd-250">[DefaultImagesSetting](https://docs.microsoft.com/deployedge/microsoft-edge-policies#DefaultImagesSetting):</span></span>*

| <span data-ttu-id="d4bfd-251">Campo</span><span class="sxs-lookup"><span data-stu-id="d4bfd-251">Field</span></span>   | <span data-ttu-id="d4bfd-252">Valor</span><span class="sxs-lookup"><span data-stu-id="d4bfd-252">Value</span></span>                                                                                |
|---------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d4bfd-253">Nome</span><span class="sxs-lookup"><span data-stu-id="d4bfd-253">Name</span></span>    | <span data-ttu-id="d4bfd-254">Microsoft Edge: DefaultImagesSetting</span><span class="sxs-lookup"><span data-stu-id="d4bfd-254">Microsoft Edge: DefaultImagesSetting</span></span>                                                 |
| <span data-ttu-id="d4bfd-255">OMA-URI</span><span class="sxs-lookup"><span data-stu-id="d4bfd-255">OMA-URI</span></span> | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~ContentSettings/DefaultImagesSetting`    |
| <span data-ttu-id="d4bfd-256">tipo</span><span class="sxs-lookup"><span data-stu-id="d4bfd-256">type</span></span>    | <span data-ttu-id="d4bfd-257">String</span><span class="sxs-lookup"><span data-stu-id="d4bfd-257">String</span></span>                                                                               |
| <span data-ttu-id="d4bfd-258">Valor</span><span class="sxs-lookup"><span data-stu-id="d4bfd-258">Value</span></span>   | `<enabled/><data id="DefaultImagesSetting" value="2"/>`                             |

*<span data-ttu-id="d4bfd-259">[DiskCacheSize](https://docs.microsoft.com/deployedge/microsoft-edge-policies#DiskCacheSize):</span><span class="sxs-lookup"><span data-stu-id="d4bfd-259">[DiskCacheSize](https://docs.microsoft.com/deployedge/microsoft-edge-policies#DiskCacheSize):</span></span>*

| <span data-ttu-id="d4bfd-260">Campo</span><span class="sxs-lookup"><span data-stu-id="d4bfd-260">Field</span></span>   | <span data-ttu-id="d4bfd-261">Valor</span><span class="sxs-lookup"><span data-stu-id="d4bfd-261">Value</span></span>                                                                                |
|---------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d4bfd-262">Nome</span><span class="sxs-lookup"><span data-stu-id="d4bfd-262">Name</span></span>    | <span data-ttu-id="d4bfd-263">Microsoft Edge: DiskCacheSize</span><span class="sxs-lookup"><span data-stu-id="d4bfd-263">Microsoft Edge: DiskCacheSize</span></span>                                                        |
| <span data-ttu-id="d4bfd-264">OMA-URI</span><span class="sxs-lookup"><span data-stu-id="d4bfd-264">OMA-URI</span></span> | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge/DiskCacheSize`        |
| <span data-ttu-id="d4bfd-265">tipo</span><span class="sxs-lookup"><span data-stu-id="d4bfd-265">type</span></span>    | <span data-ttu-id="d4bfd-266">String</span><span class="sxs-lookup"><span data-stu-id="d4bfd-266">String</span></span>                                                                               |
| <span data-ttu-id="d4bfd-267">Valor</span><span class="sxs-lookup"><span data-stu-id="d4bfd-267">Value</span></span>   | `<enabled/><data id="DiskCacheSize" value="1000000"/>`                               |

#### <span data-ttu-id="d4bfd-268">Lista de exemplos de tipos de dados de cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="d4bfd-268">List of strings data type examples</span></span>
<!--
*[NotificationsAllowedForUrls](https://docs.microsoft.com/deployedge/microsoft-edge-policies#NotificationsAllowedForUrls):*

| Field   | Value                                                                                |
|---------|--------------------------------------------------------------------------------------|
| Name    | Microsoft Edge: NotificationsAllowedForUrls                                          |
| OMA-URI | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~ContentSettings/NotificationsAllowedForUrls`    |
| Type    | String                                                                               |
| Value   | `<enabled/><data id="NotificationsAllowedForUrlsDesc" value="https://www.contoso.com"/>`<br>For multiple list items: `<data id="NotificationsAllowedForUrlsDesc" value="https://www.contoso.com;[*.]contoso.edu"/>`                               |
-->
*<span data-ttu-id="d4bfd-269">[RestoreOnStartupURLS](https://docs.microsoft.com/deployedge/microsoft-edge-policies#RestoreOnStartupURLS):</span><span class="sxs-lookup"><span data-stu-id="d4bfd-269">[RestoreOnStartupURLS](https://docs.microsoft.com/deployedge/microsoft-edge-policies#RestoreOnStartupURLS):</span></span>*

| <span data-ttu-id="d4bfd-270">Campo</span><span class="sxs-lookup"><span data-stu-id="d4bfd-270">Field</span></span>   | <span data-ttu-id="d4bfd-271">Valor</span><span class="sxs-lookup"><span data-stu-id="d4bfd-271">Value</span></span>                                                                                |
|---------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d4bfd-272">Nome</span><span class="sxs-lookup"><span data-stu-id="d4bfd-272">Name</span></span>    | <span data-ttu-id="d4bfd-273">Microsoft Edge: RestoreOnStartupURLS</span><span class="sxs-lookup"><span data-stu-id="d4bfd-273">Microsoft Edge: RestoreOnStartupURLS</span></span>                                                 |
| <span data-ttu-id="d4bfd-274">OMA-URI</span><span class="sxs-lookup"><span data-stu-id="d4bfd-274">OMA-URI</span></span> | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~Startup/RestoreOnStartupURLs`    |
| <span data-ttu-id="d4bfd-275">Tipo</span><span class="sxs-lookup"><span data-stu-id="d4bfd-275">Type</span></span>    | <span data-ttu-id="d4bfd-276">String</span><span class="sxs-lookup"><span data-stu-id="d4bfd-276">String</span></span>                                                                               |
| <span data-ttu-id="d4bfd-277">Valor</span><span class="sxs-lookup"><span data-stu-id="d4bfd-277">Value</span></span>   | `<enabled/><data id="RestoreOnStartupURLsDesc" value="1&#xF000;http://www.bing.com"/>`<br><span data-ttu-id="d4bfd-278">Para vários itens de lista:</span><span class="sxs-lookup"><span data-stu-id="d4bfd-278">For multiple list items:</span></span> `<enabled/><data id="RestoreOnStartupURLsDesc" value="1&#xF000;http://www.bing.com&#xF000;2&#xF000;http://www.microsoft.com"/>`  |

*<span data-ttu-id="d4bfd-279">[ExtensionInstallForcelist](https://docs.microsoft.com/deployedge/microsoft-edge-policies#ExtensionInstallForcelist):</span><span class="sxs-lookup"><span data-stu-id="d4bfd-279">[ExtensionInstallForcelist](https://docs.microsoft.com/deployedge/microsoft-edge-policies#ExtensionInstallForcelist):</span></span>*

| <span data-ttu-id="d4bfd-280">Campo</span><span class="sxs-lookup"><span data-stu-id="d4bfd-280">Field</span></span>   | <span data-ttu-id="d4bfd-281">Valor</span><span class="sxs-lookup"><span data-stu-id="d4bfd-281">Value</span></span>                                                                                |
|---------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d4bfd-282">Nome</span><span class="sxs-lookup"><span data-stu-id="d4bfd-282">Name</span></span>    | <span data-ttu-id="d4bfd-283">Microsoft Edge: ExtensionInstallForcelist</span><span class="sxs-lookup"><span data-stu-id="d4bfd-283">Microsoft Edge: ExtensionInstallForcelist</span></span>                                            |
| <span data-ttu-id="d4bfd-284">OMA-URI</span><span class="sxs-lookup"><span data-stu-id="d4bfd-284">OMA-URI</span></span> | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~Extensions/ExtensionInstallForcelist`    |
| <span data-ttu-id="d4bfd-285">Tipo</span><span class="sxs-lookup"><span data-stu-id="d4bfd-285">Type</span></span>    | <span data-ttu-id="d4bfd-286">String</span><span class="sxs-lookup"><span data-stu-id="d4bfd-286">String</span></span>                                                                               |
| <span data-ttu-id="d4bfd-287">Valor</span><span class="sxs-lookup"><span data-stu-id="d4bfd-287">Value</span></span>   | `<enabled/><data id="ExtensionInstallForcelistDesc" value="1&#xF000;gbchcmhmhahfdphkhkmpfmihenigjmpp;https://extensionwebstorebase.edgesv.net/v1/crx"/>`                               |

#### <span data-ttu-id="d4bfd-288">Exemplo de tipo de dados Dictionary e String</span><span class="sxs-lookup"><span data-stu-id="d4bfd-288">Dictionary and String data type example</span></span>

*<span data-ttu-id="d4bfd-289">[ProxyMode](https://docs.microsoft.com/deployedge/microsoft-edge-policies#ProxyMode):</span><span class="sxs-lookup"><span data-stu-id="d4bfd-289">[ProxyMode](https://docs.microsoft.com/deployedge/microsoft-edge-policies#ProxyMode):</span></span>*

| <span data-ttu-id="d4bfd-290">Campo</span><span class="sxs-lookup"><span data-stu-id="d4bfd-290">Field</span></span>   | <span data-ttu-id="d4bfd-291">Valor</span><span class="sxs-lookup"><span data-stu-id="d4bfd-291">Value</span></span>                                                                                |
|---------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d4bfd-292">Nome</span><span class="sxs-lookup"><span data-stu-id="d4bfd-292">Name</span></span>    | <span data-ttu-id="d4bfd-293">Microsoft Edge: ProxyMode</span><span class="sxs-lookup"><span data-stu-id="d4bfd-293">Microsoft Edge: ProxyMode</span></span>                                                            |
| <span data-ttu-id="d4bfd-294">OMA-URI</span><span class="sxs-lookup"><span data-stu-id="d4bfd-294">OMA-URI</span></span> | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~ProxyMode/ProxyMode`  |
| <span data-ttu-id="d4bfd-295">Tipo</span><span class="sxs-lookup"><span data-stu-id="d4bfd-295">Type</span></span>    | <span data-ttu-id="d4bfd-296">String</span><span class="sxs-lookup"><span data-stu-id="d4bfd-296">String</span></span>                                                                               |
| <span data-ttu-id="d4bfd-297">Valor</span><span class="sxs-lookup"><span data-stu-id="d4bfd-297">Value</span></span>   | `<enabled/><data id="ProxyMode" value="auto_detect"/>`                               |

## <span data-ttu-id="d4bfd-298">Configurar o Microsoft Edge no Intune usando a ingestão de ADMX</span><span class="sxs-lookup"><span data-stu-id="d4bfd-298">Configure Microsoft Edge in Intune using ADMX ingestion</span></span>

<span data-ttu-id="d4bfd-299">A maneira recomendada de configurar o Microsoft Edge com o Microsoft Intune é usar o perfil Modelos Administrativos conforme descrito em [Definir as configurações de política do Microsoft Edge com o Microsoft Intune](https://docs.microsoft.com/deployedge/configure-edge-with-intune).</span><span class="sxs-lookup"><span data-stu-id="d4bfd-299">The recommended way to configure Microsoft Edge with Microsoft Intune is to use the Administrative Templates profile as described in [Configure Microsoft Edge policy settings with Microsoft Intune](https://docs.microsoft.com/deployedge/configure-edge-with-intune).</span></span> <span data-ttu-id="d4bfd-300">Se deseja avaliar uma política que no momento não esteja disponível nos Modelos Administrativos do Microsoft Edge no Intune, você poderá configurar o Microsoft Edge usando [configurações personalizadas para dispositivos Windows 10 no Intune](https://docs.microsoft.com/intune/configuration/custom-settings-windows-10).</span><span class="sxs-lookup"><span data-stu-id="d4bfd-300">If you want to evaluate a policy that is currently not available in the Microsoft Edge Administrative Templates in Intune you can configure Microsoft Edge using  [custom settings for Windows 10 devices in Intune](https://docs.microsoft.com/intune/configuration/custom-settings-windows-10).</span></span>

<span data-ttu-id="d4bfd-301">Esta seção descreve como:</span><span class="sxs-lookup"><span data-stu-id="d4bfd-301">This section describes how to:</span></span>

1. [<span data-ttu-id="d4bfd-302">Ingerir o arquivo ADMX do Microsoft Edge no Intune</span><span class="sxs-lookup"><span data-stu-id="d4bfd-302">Ingest the Microsoft Edge ADMX file into Intune</span></span>](#ingest-the-microsoft-edge-admx-file-into-intune)
2. [<span data-ttu-id="d4bfd-303">Definir uma política usando OMA-URI personalizado no Intune</span><span class="sxs-lookup"><span data-stu-id="d4bfd-303">Set a policy using custom OMA-URI in Intune</span></span>](#set-a-policy-using-custom-oma-uri-in-intune)

> [!IMPORTANT]
> <span data-ttu-id="d4bfd-304">Como prática recomendada, não use um perfil OMA-URI personalizado e um perfil de modelos de Administração para definir a mesma configuração do Microsoft Edge no Intune.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-304">As a best practice, don’t use a custom OMA-URI profile and an Administration templates profile to configure the same Microsoft Edge setting in Intune.</span></span> <span data-ttu-id="d4bfd-305">Se você implantar a mesma política usando um perfil OMA-URI e um perfil de modelo Administrativo personalizados, mas com valores diferentes, os usuários obterão resultados imprevisíveis.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-305">If you deploy the same policy using both a custom OMA-URI  and an Administrative template profile, but with different values, users will get unpredictable results.</span></span> <span data-ttu-id="d4bfd-306">É altamente recomendável remover seu perfil OMA-URI antes de usar um perfil de modelos de Administração.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-306">We strongly recommend removing your OMA-URI profile before using an Administration templates profile.</span></span>

### <span data-ttu-id="d4bfd-307">Ingerir o arquivo ADMX do Microsoft Edge no Intune</span><span class="sxs-lookup"><span data-stu-id="d4bfd-307">Ingest the Microsoft Edge ADMX file into Intune</span></span>

<span data-ttu-id="d4bfd-308">Esta seção descreve como ingerir o modelo administrativo do Microsoft Edge (arquivo **msedge.admx**) no Intune.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-308">This section describes how to ingest the Microsoft Edge administrative template (**msedge.admx** file) into Intune.</span></span>

> [!WARNING]
> <span data-ttu-id="d4bfd-309">Não modifique o arquivo ADMX antes de ingerir o arquivo.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-309">Don't modify the ADMX file before ingesting the file.</span></span>

<span data-ttu-id="d4bfd-310">Para ingerir o arquivo ADMX, siga estas etapas:</span><span class="sxs-lookup"><span data-stu-id="d4bfd-310">To ingest the ADMX file, follow these steps:</span></span>

1. <span data-ttu-id="d4bfd-311">Baixe o arquivo de modelos de política do Microsoft Edge (MicrosoftEdgePolicyTemplates.cab) da [página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise) e extraia o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-311">Download the Microsoft Edge policy templates file (MicrosoftEdgePolicyTemplates.cab) from the [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise) and extract the contents.</span></span> <span data-ttu-id="d4bfd-312">O arquivo que você deseja ingerir é **msedge.admx**.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-312">The file that you want to ingest is **msedge.admx**.</span></span>
2. <span data-ttu-id="d4bfd-313">Entre no [portal do Microsoft Azure](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="d4bfd-313">Sign in to the [Microsoft Azure portal](https://portal.azure.com).</span></span>
3. <span data-ttu-id="d4bfd-314">Selecione **Intune** em _Todos os Serviços_ ou procure Intune na caixa de pesquisa do portal.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-314">Select **Intune** from _All Services_, or search for Intune in the portal search box.</span></span>
4. <span data-ttu-id="d4bfd-315">Em _Microsoft Intune - Visão geral_, selecione **Configuração do dispositivo** | **Perfis**.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-315">From _Microsoft Intune - Overview_, select **Device configuration** | **Profiles**.</span></span>
5. <span data-ttu-id="d4bfd-316">Na barra de comandos superior, selecione **+ Criar perfil**.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-316">On the top command bar, select **+ Create profile**.</span></span>

   ![Criar um perfil de dispositivo](./media/edge-cfg-with-mdm/configure-edge-mdm-intune-create-profile.png)

6. <span data-ttu-id="d4bfd-318">Forneça as seguintes informações de perfil:</span><span class="sxs-lookup"><span data-stu-id="d4bfd-318">Provide the following profile information:</span></span>

   - <span data-ttu-id="d4bfd-319">**Nome**: insira um nome descritivo.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-319">**Name**: Enter a descriptive name.</span></span> <span data-ttu-id="d4bfd-320">Neste exemplo, "Configuração ingerida do ADMX do Microsoft Edge".</span><span class="sxs-lookup"><span data-stu-id="d4bfd-320">For this example, "Microsoft Edge ADMX ingested configuration".</span></span>
   - <span data-ttu-id="d4bfd-321">**Descrição**: insira uma descrição opcional para o perfil.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-321">**Description**: Enter an optional description for the profile.</span></span>
   - <span data-ttu-id="d4bfd-322">**Plataforma**: selecione "Windows 10 e posterior"</span><span class="sxs-lookup"><span data-stu-id="d4bfd-322">**Platform**: Select "Windows 10 and later"</span></span>
   - <span data-ttu-id="d4bfd-323">**Tipo de perfil**: selecione "Personalizado"</span><span class="sxs-lookup"><span data-stu-id="d4bfd-323">**Profile type**: Select "Custom"</span></span>

7. <span data-ttu-id="d4bfd-324">Em **Configurações Personalizadas de OMA-URI**, clique em **Adicionar** para adicionar uma ingestão de ADMX.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-324">On **Custom OMA-URI Settings**, click **Add** to add an ADMX ingestion.</span></span>

   ![Adicionar ingestão para OMA-URI](./media/edge-cfg-with-mdm/configure-edge-mdm-intune-create-profile-add-omauri.png)

8. <span data-ttu-id="d4bfd-326">Em **Adicionar Linha**, forneça as seguintes informações:</span><span class="sxs-lookup"><span data-stu-id="d4bfd-326">On **Add Row**, provide the following information:</span></span>

   - <span data-ttu-id="d4bfd-327">**Nome**: insira um nome descritivo.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-327">**Name**: Enter a descriptive name.</span></span> <span data-ttu-id="d4bfd-328">Neste exemplo, use "Ingestão de ADMX do Microsoft Edge".</span><span class="sxs-lookup"><span data-stu-id="d4bfd-328">For this example, use "Microsoft Edge ADMX ingestion".</span></span>
   - <span data-ttu-id="d4bfd-329">**Descrição**: insira uma descrição opcional para a configuração.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-329">**Description**: Enter an optional description for the setting.</span></span>
   - <span data-ttu-id="d4bfd-330">**OMA-URI**: insira "*./Device/Vendor/MSFT/Policy/ConfigOperations/ADMXInstall/Edge/Policy/EdgeAdmx*"</span><span class="sxs-lookup"><span data-stu-id="d4bfd-330">**OMA-URI**: Enter "*./Device/Vendor/MSFT/Policy/ConfigOperations/ADMXInstall/Edge/Policy/EdgeAdmx*"</span></span>
   - <span data-ttu-id="d4bfd-331">**Tipo de dados**: selecione "String"</span><span class="sxs-lookup"><span data-stu-id="d4bfd-331">**Data type**: Select "String"</span></span>
   - <span data-ttu-id="d4bfd-332">**Valor**: essa área de entrada aparece depois que você seleciona o **Tipo de dados**.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-332">**Value**: This input area appears after you select the **Data type**.</span></span> <span data-ttu-id="d4bfd-333">Abra o arquivo msedge.admx do arquivo de modelos de política do Microsoft Edge que você extraiu na etapa 1.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-333">Open the msedge.admx file from the Microsoft Edge policy templates file you extracted in step 1.</span></span> <span data-ttu-id="d4bfd-334">Copie **TODO o texto** do arquivo msedge.admx e cole-o na área de texto **Valor** mostrada na captura de tela a seguir.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-334">Copy **ALL the text** from the msedge.admx file and paste it in the **Value** text area shown in the following screenshot.</span></span>

        ![Adicionar uma ingestão de ADMX](./media/edge-cfg-with-mdm/configure-edge-intune-mdm-omauri-addrow-ingest.png)

   - <span data-ttu-id="d4bfd-336">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-336">Click **OK**.</span></span>

9. <span data-ttu-id="d4bfd-337">Em **Configurações Personalizadas de OMA-URI**, clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-337">On **Custom OMA-URI Settings**, click **OK**.</span></span>
10. <span data-ttu-id="d4bfd-338">Em **Criar perfil**, clique em **Criar**.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-338">On **Create profile**, click **Create**.</span></span> <span data-ttu-id="d4bfd-339">A próxima captura de tela mostra informações sobre o perfil recém-criado.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-339">The next screenshot shows information about the newly created profile.</span></span>

    ![<span data-ttu-id="d4bfd-340">Novas informações sobre o perfil do dispositivo</span><span class="sxs-lookup"><span data-stu-id="d4bfd-340">New device profile information</span></span> ](./media/edge-cfg-with-mdm/configure-edge-mdm-intune-create-profile-done.png)

<!--
> [!NOTE]
> You can use the preceding steps to ingest the msedgeupate.admx policy template file.
-->
### <span data-ttu-id="d4bfd-341">Definir uma política usando OMA-URI personalizado no Intune</span><span class="sxs-lookup"><span data-stu-id="d4bfd-341">Set a policy using custom OMA-URI in Intune</span></span>

> [!NOTE]
> <span data-ttu-id="d4bfd-342">Antes de usar as etapas nesta seção, você deverá concluir as etapas descritas em [Ingerir o arquivo ADMX do Microsoft Edge no Intune](#ingest-the-microsoft-edge-admx-file-into-intune).</span><span class="sxs-lookup"><span data-stu-id="d4bfd-342">Before using the steps in this section you must complete the steps described in [Ingest the Microsoft Edge ADMX file into Intune](#ingest-the-microsoft-edge-admx-file-into-intune).</span></span>

1. <span data-ttu-id="d4bfd-343">Entre no [portal do Microsoft Azure](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="d4bfd-343">Sign in to the [Microsoft Azure portal](https://portal.azure.com).</span></span>
2. <span data-ttu-id="d4bfd-344">Selecione **Intune** em _Todos os Serviços_ ou procure Intune na caixa de pesquisa do portal.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-344">Select **Intune** from _All Services_, or search for Intune in the portal search box.</span></span>
3. <span data-ttu-id="d4bfd-345">Acesse **Intune**>**Configuração do dispositivo**>**Perfis**.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-345">Go to **Intune**>**Device configuration**>**Profiles**.</span></span>
4. <span data-ttu-id="d4bfd-346">Selecione o perfil "Configuração ingerida do ADMX do Microsoft Edge" ou o nome usado para o perfil.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-346">Select the "Microsoft Edge ADMX ingested configuration" profile or the name you used for the profile.</span></span>
5. <span data-ttu-id="d4bfd-347">Para adicionar configurações de política do Microsoft Edge, você terá de abrir as **Configurações Personalizadas de OMA-URI**.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-347">To add Microsoft Edge policy settings, you have to open **Custom OMA-URI Settings**.</span></span> <span data-ttu-id="d4bfd-348">Em **Gerenciar**, clique em **Propriedades** e clique em **Configurações**.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-348">Under **Manage**, click **Properties**, and then click **Settings**.</span></span>

    ![Definir configurações de perfil](./media/edge-cfg-with-mdm/configure-edge-mdm-intune-add-policy-settings.png)

6. <span data-ttu-id="d4bfd-350">Em **Configurações Personalizadas de OMA-URI**, clique em **Adicionar**.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-350">On **Custom OMA-URI Settings**, click **Add**.</span></span>

    ![Adicionar linha às configurações de OMA-URI](./media/edge-cfg-with-mdm/configure-edge-mdm-intune-add-policy-settings-add-row.png)

7. <span data-ttu-id="d4bfd-352">Em **Adicionar Linha**, forneça as seguintes informações:</span><span class="sxs-lookup"><span data-stu-id="d4bfd-352">On **Add Row**, provide the following information:</span></span>

   - <span data-ttu-id="d4bfd-353">**Nome**: insira um nome descritivo.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-353">**Name**: Enter a descriptive name.</span></span> <span data-ttu-id="d4bfd-354">Sugerimos o uso do nome de política que você deseja configurar.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-354">We suggest using the policy name you want to configure.</span></span> <span data-ttu-id="d4bfd-355">Neste exemplo, use "ShowHomeButton".</span><span class="sxs-lookup"><span data-stu-id="d4bfd-355">For this example, use "ShowHomeButton".</span></span>
   - <span data-ttu-id="d4bfd-356">**Descrição** (opcional): insira uma descrição para a configuração.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-356">**Description** (Optional): Enter a description for the setting.</span></span>
   - <span data-ttu-id="d4bfd-357">**OMA-URI**: insira o OMA-URI para a política.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-357">**OMA-URI**: Enter the OMA-URI for the policy.</span></span> <span data-ttu-id="d4bfd-358">Usando a política "ShowHomeButton" como um exemplo, utilize esta cadeia de caracteres: "*./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~Startup/ShowHomeButton*"</span><span class="sxs-lookup"><span data-stu-id="d4bfd-358">Using the for "ShowHomeButton" policy as an example, use this string: "*./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~Startup/ShowHomeButton*"</span></span>
   - <span data-ttu-id="d4bfd-359">**Tipo de dados**: selecione o tipo de dados de configurações de política.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-359">**Data type**: Select the policy settings data type.</span></span> <span data-ttu-id="d4bfd-360">Para a política "ShowHomeButton", use "String"</span><span class="sxs-lookup"><span data-stu-id="d4bfd-360">For the "ShowHomeButton" policy, use "String"</span></span>
   - <span data-ttu-id="d4bfd-361">**Valor**: insira a configuração que você deseja configurar para a política.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-361">**Value**: Enter the setting that you want to configure for the policy.</span></span> <span data-ttu-id="d4bfd-362">No exemplo de "ShowHomeButton", insira "\<enabled/>".</span><span class="sxs-lookup"><span data-stu-id="d4bfd-362">For "ShowHomeButton" example, enter "\<enabled/>".</span></span> <span data-ttu-id="d4bfd-363">A captura de tela a seguir mostra as definições para a configuração de uma política.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-363">The following screenshot shows the settings for configuring a policy.</span></span>

        ![Adicionar Linha, Configurações Personalizadas de OMA-URI](./media/edge-cfg-with-mdm/configure-edge-mdm-custom-omauri-setting.png)

   - <span data-ttu-id="d4bfd-365">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-365">Click **OK**.</span></span>

8. <span data-ttu-id="d4bfd-366">Em **Configurações Personalizadas de OMA-URI**, clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-366">On **Custom OMA-URI Settings**, click **OK**.</span></span>
9. <span data-ttu-id="d4bfd-367">No perfil "**Configuração ingerida do ADMX do Microsoft Edge - Propriedades**" (ou o nome que você usou), clique em **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-367">On the "**Microsoft Edge ADMX ingested configuration - Properties**" profile (or the name you used), click **Save**.</span></span>

<span data-ttu-id="d4bfd-368">Depois que o perfil for criado e as propriedades definidas, você precisará [atribuir o perfil ao Microsoft Intune](https://docs.microsoft.com/intune/configuration/device-profile-assign).</span><span class="sxs-lookup"><span data-stu-id="d4bfd-368">After the profile is created and the properties set, you have to [assign the profile in Microsoft Intune](https://docs.microsoft.com/intune/configuration/device-profile-assign).</span></span>

#### <span data-ttu-id="d4bfd-369">Confirmar se a política foi definida</span><span class="sxs-lookup"><span data-stu-id="d4bfd-369">Confirm that the policy was set</span></span>

<span data-ttu-id="d4bfd-370">Siga as etapas a seguir para confirmar se a política do Microsoft Edge está usando o perfil que você criou.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-370">Use the following steps to confirm that the Microsoft Edge policy is using the profile you created.</span></span> <span data-ttu-id="d4bfd-371">(Dê ao Microsoft Intune tempo para propagar a política para um dispositivo atribuído no exemplo de perfil "Configuração ingerida do ADMX do Microsoft Edge").</span><span class="sxs-lookup"><span data-stu-id="d4bfd-371">(Give Microsoft Intune time to propagate the policy to a device you assigned in the "Microsoft Edge ADMX ingested configuration" profile example.)</span></span>

1. <span data-ttu-id="d4bfd-372">Abra o Microsoft Edge e acesse *edge://policy*.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-372">Open Microsoft Edge and go to *edge://policy*.</span></span>
2. <span data-ttu-id="d4bfd-373">Na página **Políticas**, veja se a política definida no perfil está listada.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-373">On the **Policies** page, see if the policy you set in the profile is listed.</span></span>
3. <span data-ttu-id="d4bfd-374">Se sua política não for mostrada, consulte [Diagnosticar falhas de MDM no Windows 10](https://docs.microsoft.com/windows/client-management/mdm/diagnose-mdm-failures-in-windows-10) ou [Solucionar problemas de uma configuração de política](#troubleshoot-a-policy-setting).</span><span class="sxs-lookup"><span data-stu-id="d4bfd-374">If your policy isn't shown, see [Diagnose MDM failures in Windows 10](https://docs.microsoft.com/windows/client-management/mdm/diagnose-mdm-failures-in-windows-10) or [Troubleshoot a policy setting](#troubleshoot-a-policy-setting).</span></span>

#### <span data-ttu-id="d4bfd-375">Solucionar problemas de uma configuração de política</span><span class="sxs-lookup"><span data-stu-id="d4bfd-375">Troubleshoot a policy setting</span></span>

<span data-ttu-id="d4bfd-376">Se uma política do Microsoft Edge não estiver entrando em vigor, tente as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="d4bfd-376">If a Microsoft Edge policy isn’t taking effect, try the following steps:</span></span>

<span data-ttu-id="d4bfd-377">Abra a página *edge://policy* no dispositivo de destino (um dispositivo ao qual você atribuiu o perfil no Microsoft Intune) e procure pela política.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-377">Open the *edge://policy* page on the target device (a device you assigned the profile to in Microsoft Intune) and search for the policy.</span></span> <span data-ttu-id="d4bfd-378">Se a política não estiver na página *edge://policy*, tente o seguinte:</span><span class="sxs-lookup"><span data-stu-id="d4bfd-378">If the policy isn’t on the *edge://policy* page, try the following:</span></span>

- <span data-ttu-id="d4bfd-379">Verifique se a política está no Registro e se está correta.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-379">Check that the policy is in the registry and is correct.</span></span> <span data-ttu-id="d4bfd-380">No dispositivo de destino, abra o Editor do Registro do Windows 10 (**tecla Windows + r**, insira “*regedit*” e então pressione **Enter**). Verifique se a política está corretamente definida no caminho *\Software\Policies\ Microsoft\Edge*.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-380">On the target device open the Windows 10 Registry Editor (**Windows key + r**, enter “*regedit*” and then press **Enter**.) Check that the policy is correctly defined in the *\Software\Policies\ Microsoft\Edge* path.</span></span> <span data-ttu-id="d4bfd-381">Se você não encontrar a política no caminho esperado, a política não foi enviada por push corretamente para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-381">If you don’t find the policy in the expected path, then the policy wasn’t pushed to the device correctly.</span></span>
- <span data-ttu-id="d4bfd-382">Verifique se o caminho OMA-URI está correto e se o valor é uma cadeia de caracteres XML válida.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-382">Check that the OMA-URI path is correct, and the value is a valid XML string.</span></span> <span data-ttu-id="d4bfd-383">Se qualquer um deles estiver incorreto, a política não será enviada por push para o dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="d4bfd-383">If either of these are incorrect the policy won’t be pushed to the target device.</span></span>

<span data-ttu-id="d4bfd-384">Para obter mais dicas sobre a solução de problemas, consulte [Configurar o Microsoft Intune](https://docs.microsoft.com/intune/fundamentals/setup-steps) e [Sincronizar dispositivos](https://docs.microsoft.com/intune/remote-actions/device-sync).</span><span class="sxs-lookup"><span data-stu-id="d4bfd-384">For more trouble shooting tips, see [Set up Microsoft Intune](https://docs.microsoft.com/intune/fundamentals/setup-steps) and [Sync devices](https://docs.microsoft.com/intune/remote-actions/device-sync).</span></span>

## <span data-ttu-id="d4bfd-385">Consulte também</span><span class="sxs-lookup"><span data-stu-id="d4bfd-385">See also</span></span>

- [<span data-ttu-id="d4bfd-386">Página de aterrissagem do Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="d4bfd-386">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="d4bfd-387">Definir as configurações de política do Microsoft Edge com o Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="d4bfd-387">Configure Microsoft Edge policy settings with Microsoft Intune</span></span>](configure-edge-with-intune.md)
- [<span data-ttu-id="d4bfd-388">Gerenciamento de dispositivos móveis</span><span class="sxs-lookup"><span data-stu-id="d4bfd-388">Mobile device management</span></span>](https://docs.microsoft.com/windows/client-management/mdm/)
- [<span data-ttu-id="d4bfd-389">Usar configurações personalizadas para dispositivos Windows 10 no Intune</span><span class="sxs-lookup"><span data-stu-id="d4bfd-389">Use custom settings for Windows 10 devices in Intune</span></span>](https://docs.microsoft.com/intune/configuration/custom-settings-windows-10)
- [<span data-ttu-id="d4bfd-390">Configuração de política de aplicativo Win32 e Ponte de Desktop</span><span class="sxs-lookup"><span data-stu-id="d4bfd-390">Win32 and Desktop Bridge app policy configuration</span></span>](https://docs.microsoft.com/windows/client-management/mdm/win32-and-centennial-app-policy-configuration)
- [<span data-ttu-id="d4bfd-391">Noções básicas sobre políticas baseadas em ADMX</span><span class="sxs-lookup"><span data-stu-id="d4bfd-391">Understanding ADMX-backed policies</span></span>](https://docs.microsoft.com/windows/client-management/mdm/understanding-admx-backed-policies)
