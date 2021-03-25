---
title: Configurar sites na lista de sites do modo empresarial
ms.author: cjacks
author: cjacks
manager: saudm
ms.date: 05/28/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Configurar Lista de Sites Empresariais
ms.openlocfilehash: 9b1943e4d50dcc770b4a634b99ecbd001d1ffbcc
ms.sourcegitcommit: f363ceb6c42054fabc95ce8d7bca3c52d80e6a9f
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/24/2021
ms.locfileid: "11447645"
---
# <a name="configure-sites-on-the-enterprise-mode-site-list"></a><span data-ttu-id="30904-103">Configurar sites na lista de sites do modo empresarial</span><span class="sxs-lookup"><span data-stu-id="30904-103">Configure Sites on the Enterprise Mode Site List</span></span>

<span data-ttu-id="30904-104">Este artigo descreve alterações na Lista de Sites do Modo Empresarial que oferecem suporte à configuração do modo IE para Microsoft Edge versão 77 e posterior.</span><span class="sxs-lookup"><span data-stu-id="30904-104">This article describes changes to the Enterprise Mode Site List that support configuring IE mode for Microsoft Edge version 77 and later.</span></span>

<span data-ttu-id="30904-105">Para obter mais informações sobre o esquema do arquivo XML da Lista de Sites do Modo Empresarial, consulte as [orientações do esquema do Modo Empresarial v.2](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance).</span><span class="sxs-lookup"><span data-stu-id="30904-105">For more information on the schema for the Enterprise Mode Site List XML file, see [Enterprise Mode schema v.2 guidance](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance).</span></span>

> [!NOTE]
> <span data-ttu-id="30904-106">Este artigo se aplica aos Canais **Estável**, **Beta** e **Dev** do Microsoft Edge Beta, versão 77 ou posteriores.</span><span class="sxs-lookup"><span data-stu-id="30904-106">This article applies to Microsoft Edge **Stable**, **Beta** and **Dev** Channels, version 77 or later.</span></span>

## <a name="updated-schema-elements"></a><span data-ttu-id="30904-107">Elementos do esquema atualizados</span><span class="sxs-lookup"><span data-stu-id="30904-107">Updated schema elements</span></span>

<span data-ttu-id="30904-108">A tabela a seguir descreve o elemento \<open-in app\> adicionado ao esquema v.2 do esquema Modo Empresarial:</span><span class="sxs-lookup"><span data-stu-id="30904-108">The following table describes the \<open-in app\> element added to the v.2 of the Enterprise Mode schema:</span></span>

| **<span data-ttu-id="30904-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="30904-109">Element</span></span>** | **<span data-ttu-id="30904-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="30904-110">Description</span></span>** |
| --- | --- |
| \<open-in app="**true**"\> | <span data-ttu-id="30904-111">Um elemento filho que controla qual navegador é usado para sites.</span><span class="sxs-lookup"><span data-stu-id="30904-111">A child element that controls what browser is used for sites.</span></span> <span data-ttu-id="30904-112">Esse elemento é obrigatório para sites que precisam ser **abertos no IE11**.</span><span class="sxs-lookup"><span data-stu-id="30904-112">This element is required for sites that need to **open in IE11**.</span></span>|

**<span data-ttu-id="30904-113">Exemplo:</span><span class="sxs-lookup"><span data-stu-id="30904-113">Example:</span></span>**

``` xml
<site url="contoso.com">

  <open-in app="true">IE11</open-in>

</site>
```

<span data-ttu-id="30904-114">A tabela a seguir mostra os valores possíveis do elemento\<open-in\>:</span><span class="sxs-lookup"><span data-stu-id="30904-114">The following table shows the possible values of the \<open-in\> element:</span></span>

| **<span data-ttu-id="30904-115">Valor</span><span class="sxs-lookup"><span data-stu-id="30904-115">Value</span></span>** | **<span data-ttu-id="30904-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="30904-116">Description</span></span>** |
| --- | --- |
| **\<open-in\><span data-ttu-id="30904-117">IE11</span><span class="sxs-lookup"><span data-stu-id="30904-117">IE11</span></span>\</open-in\>** | <span data-ttu-id="30904-118">Abre o site no modo IE ou em uma janela completa do IE11.</span><span class="sxs-lookup"><span data-stu-id="30904-118">Opens the site in IE mode or a full IE11 window.</span></span> <span data-ttu-id="30904-119">Para ativar o modo IE, confira [Configurar políticas do modo IE](./edge-ie-mode-policies.md)</span><span class="sxs-lookup"><span data-stu-id="30904-119">To enable IE mode, see [Configure IE mode policies](./edge-ie-mode-policies.md)</span></span>|
| **\<open-in app="**true**"\><span data-ttu-id="30904-120">IE11</span><span class="sxs-lookup"><span data-stu-id="30904-120">IE11</span></span>\</open-in\>** | <span data-ttu-id="30904-121">Abre o site em uma janela completa do IE11</span><span class="sxs-lookup"><span data-stu-id="30904-121">Opens the site in a full IE11 window</span></span> |
| **\<open-in\><span data-ttu-id="30904-122">MSEdge</span><span class="sxs-lookup"><span data-stu-id="30904-122">MSEdge</span></span>\</open-in\>** | <span data-ttu-id="30904-123">Abre o site no Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="30904-123">Opens the site in Microsoft Edge</span></span> |
| **\<open-in\><span data-ttu-id="30904-124">Nenhum ou não especificado.</span><span class="sxs-lookup"><span data-stu-id="30904-124">None or not specified</span></span>\</open-in\>** | <span data-ttu-id="30904-125">Abre o site no navegador padrão ou no navegador em que o usuário navegou até o site.</span><span class="sxs-lookup"><span data-stu-id="30904-125">Opens the site in the default browser or in the browser where the user navigated to the site.</span></span> |
|**\<open-in\><span data-ttu-id="30904-126">Configurável</span><span class="sxs-lookup"><span data-stu-id="30904-126">Configurable</span></span>\</open-in\>** | <span data-ttu-id="30904-127">Permite ao site participar da determinação do mecanismo do IE.</span><span class="sxs-lookup"><span data-stu-id="30904-127">Allows the site to participate in IE mode engine determination.</span></span> <span data-ttu-id="30904-128">Para saber mais, confira [Saber mais sobre sites Configuráveis no modo IE](edge-learnmore-configurable-sites-ie-mode.md).</span><span class="sxs-lookup"><span data-stu-id="30904-128">To learn more, see [Learn about Configurable sites in IE mode](edge-learnmore-configurable-sites-ie-mode.md).</span></span>  |

>[!NOTE]
> <span data-ttu-id="30904-129">O atributo app =**"true"** é reconhecido somente quando associado a _'open-in' IE11_.</span><span class="sxs-lookup"><span data-stu-id="30904-129">The attribute app=**"true"** is only recognized when associated to _'open-in' IE11_.</span></span> <span data-ttu-id="30904-130">Adicioná-lo aos outros elementos 'open-in' não mudará o comportamento do navegador.</span><span class="sxs-lookup"><span data-stu-id="30904-130">Adding it to the other 'open-in' elements won't change browser behavior.</span></span>   

## <a name="configure-neutral-sites"></a><span data-ttu-id="30904-131">Configurar sites neutros</span><span class="sxs-lookup"><span data-stu-id="30904-131">Configure neutral sites</span></span>

<span data-ttu-id="30904-132">Para que o modo IE funcione corretamente, os servidores de autenticação/Logon Único precisarão ser explicitamente configurados como sites neutros.</span><span class="sxs-lookup"><span data-stu-id="30904-132">In order for IE mode to work properly, authentication / Single Sign-On servers will need to be explicitly configured as neutral sites.</span></span> <span data-ttu-id="30904-133">Caso contrário, as páginas do modo IE tentarão redirecionar para o Microsoft Edge e a autenticação falhará.</span><span class="sxs-lookup"><span data-stu-id="30904-133">Otherwise, IE mode pages will try to redirect to Microsoft Edge, and authentication will fail.</span></span>

<span data-ttu-id="30904-134">Um site neutro usará o navegador onde a navegação começou - no modo Microsoft Edge ou IE.</span><span class="sxs-lookup"><span data-stu-id="30904-134">A neutral site will use the browser where the navigation started - either Microsoft Edge or IE mode.</span></span> <span data-ttu-id="30904-135">A configuração de sites neutros garante que todos os aplicativos que usam esses servidores de autenticação, modernos e herdados, continuem funcionando.</span><span class="sxs-lookup"><span data-stu-id="30904-135">Configuring neutral sites ensures that all applications using these authentication servers, both modern and legacy, continue to work.</span></span>

<span data-ttu-id="30904-136">Para configurar sites neutros, configure o menu suspenso *Open In* como “Nenhum” na ferramenta Enterprise Mode Site List Manager ou atualizando diretamente o XML da lista de sites:</span><span class="sxs-lookup"><span data-stu-id="30904-136">You can configure neutral sites by setting the *Open In* dropdown to 'None' in the Enterprise Mode Site List Manager tool or by directly updating the site list XML:</span></span>

``` xml
<site url="login.contoso.com">
   
    <open-in>None</open-in>

</site>
```

<span data-ttu-id="30904-137">Para identificar servidores de autenticação, inspecione o tráfego de rede de um aplicativo usando as Ferramentas de Desenvolvedor do IE11.</span><span class="sxs-lookup"><span data-stu-id="30904-137">To identify authentication servers, inspect the network traffic from an application using the IE11 Developer Tools.</span></span> <span data-ttu-id="30904-138">Se você precisar de mais tempo para identificar seus servidores de autenticação, poderá configurar uma política para manter toda a navegação na página no modo IE.</span><span class="sxs-lookup"><span data-stu-id="30904-138">If you need more time to identify your authentication servers, you can configure a policy to keep all in-page navigation in IE mode.</span></span> <span data-ttu-id="30904-139">Para minimizar o uso do modo IE, desative essa configuração depois de identificar e adicionar seus servidores de autenticação à lista de sites.</span><span class="sxs-lookup"><span data-stu-id="30904-139">To minimize the use of IE mode, disable this setting once you've identified and added your authentication servers to the site list.</span></span> <span data-ttu-id="30904-140">Para obter mais informações, confira [Configurar a navegação na página para permanecer no modo IE](./microsoft-edge-policies.md#internetexplorerintegrationsiteredirect).</span><span class="sxs-lookup"><span data-stu-id="30904-140">For more information, see [Configure in-page navigation to remain in IE mode](./microsoft-edge-policies.md#internetexplorerintegrationsiteredirect).</span></span>

>[!NOTE]
   ><span data-ttu-id="30904-141">O esquema v.1 do Modo Empresarial não tem suporte na integração do modo IE.</span><span class="sxs-lookup"><span data-stu-id="30904-141">Enterprise Mode schema v.1 isn't supported for IE mode integration.</span></span> <span data-ttu-id="30904-142">Se você estiver usando o esquema v.1 atualmente com o Internet Explorer 11, deverá atualizar para o esquema v.2.</span><span class="sxs-lookup"><span data-stu-id="30904-142">If you are currently using schema v.1 with Internet Explorer 11, you must upgrade to schema v.2.</span></span> <span data-ttu-id="30904-143">Para obter mais informações, consulte [Diretrizes sobre o esquema v.2 do Modo Empresarial](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance).</span><span class="sxs-lookup"><span data-stu-id="30904-143">For more information, see [Enterprise Mode schema v.2 guidance](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance).</span></span>

## <a name="see-also"></a><span data-ttu-id="30904-144">Consulte também</span><span class="sxs-lookup"><span data-stu-id="30904-144">See also</span></span>

- [<span data-ttu-id="30904-145">Página de aterrissagem do Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="30904-145">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="30904-146">Sobre o modo IE</span><span class="sxs-lookup"><span data-stu-id="30904-146">About IE mode</span></span>](./edge-ie-mode.md)
- [<span data-ttu-id="30904-147">Informações adicionais sobre o Modo Empresarial</span><span class="sxs-lookup"><span data-stu-id="30904-147">Additional Enterprise Mode information</span></span>](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)