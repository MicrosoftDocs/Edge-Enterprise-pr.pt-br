---
title: Estratégia de configuração de site de empresa
ms.author: shisub
author: shisub
manager: srugh
ms.date: 03/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Um guia passo a passo para configurar a lista de Sites do Modo Empresa para o modo Internet Explorer.
ms.openlocfilehash: 1d0b80950439fce77513413c3f5d1143538487d1
ms.sourcegitcommit: 93851b83dc11422924646a04a9e0f60ff2554af7
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/01/2021
ms.locfileid: "11470149"
---
# <a name="enterprise-site-configuration-strategy"></a><span data-ttu-id="4fa1f-103">Estratégia de configuração de site de empresa</span><span class="sxs-lookup"><span data-stu-id="4fa1f-103">Enterprise site configuration strategy</span></span>

<span data-ttu-id="4fa1f-104">Este artigo descreve as alterações na Lista de Sites do Modo Empresa para dar suporte ao modo Internet Explorer para o Microsoft Edge versão 77 e posterior.</span><span class="sxs-lookup"><span data-stu-id="4fa1f-104">This article describes changes to the Enterprise Mode Site List to support Internet Explorer mode for Microsoft Edge version 77 and later.</span></span>

<span data-ttu-id="4fa1f-105">Para obter mais informações sobre o esquema do arquivo XML da Lista de Sites do Modo Empresa, confira as [orientações do esquema do Modo Empresarial v.2](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance).</span><span class="sxs-lookup"><span data-stu-id="4fa1f-105">For more information on the schema for the Enterprise Mode Site List XML file, see [Enterprise Mode schema v.2 guidance](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance).</span></span>

> [!NOTE]
> <span data-ttu-id="4fa1f-106">Este artigo se aplica ao Microsoft Edge versão 77 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="4fa1f-106">This article applies to Microsoft Edge version 77 or later.</span></span>
<!--
## Updated schema elements

The following table describes the \<open-in app\> element added to the v.2 of the Enterprise Mode schema:

| **Element** | **Description** |
| --- | --- |
| \<open-in app="**true**"\> | A child element that controls what browser is used for sites. This element is required for sites that need to **open in IE11**.|

**Example:**

``` xml
<site url="contoso.com">

  <open-in app="true">IE11</open-in>

</site>
```

The following table shows the possible values of the \<open-in\> element:

| **Value** | **Description** |
| --- | --- |
| **\<open-in\>IE11\</open-in\>** | Opens the site in IE mode or a full IE11 window. To enable IE mode, see [Configure IE mode policies](./edge-ie-mode-policies.md)|
| **\<open-in app="**true**"\>IE11\</open-in\>** | Opens the site in a full IE11 window |
| **\<open-in\>MSEdge\</open-in\>** | Opens the site in Microsoft Edge |
| **\<open-in\>None or not specified\</open-in\>** | Opens the site in the default browser or in the browser where the user navigated to the site. |
|**\<open-in\>Configurable\</open-in\>** | Allows the site to participate in IE mode engine determination. To learn more, see [Learn about Configurable sites in IE mode](edge-learnmore-configurable-sites-ie-mode.md).  |

>[!NOTE]
> The attribute app=**"true"** is only recognized when associated to _'open-in' IE11_. Adding it to the other 'open-in' elements won't change browser behavior.   -->

## <a name="configuration-strategy"></a><span data-ttu-id="4fa1f-107">Estratégia de configuração</span><span class="sxs-lookup"><span data-stu-id="4fa1f-107">Configuration strategy</span></span>

<span data-ttu-id="4fa1f-108">As etapas a seguir fazem parte de uma estratégia de configuração de site para o modo IE:</span><span class="sxs-lookup"><span data-stu-id="4fa1f-108">The following steps are part of a site configuration strategy for IE mode:</span></span>
1. <span data-ttu-id="4fa1f-109">Preparar sua lista de sites</span><span class="sxs-lookup"><span data-stu-id="4fa1f-109">Prepare your site list</span></span>
2. <span data-ttu-id="4fa1f-110">Configurar sites neutros</span><span class="sxs-lookup"><span data-stu-id="4fa1f-110">Configure neutral sites</span></span>
3. <span data-ttu-id="4fa1f-111">(Opcional) Usar o compartilhamento de cookies, se necessário</span><span class="sxs-lookup"><span data-stu-id="4fa1f-111">(Optional) Use cookie sharing if necessary</span></span>

<!--
Step 1.  – if you don’t have one use Site Discovery Step-by-Step
Step 2 – Neutral sites + sticky mode
        Use more examples and explain sticky mode better
Step 3 – If that doesn’t cover your needs, then use Cookie sharing -->

## <a name="prepare-your-site-list"></a><span data-ttu-id="4fa1f-112">Preparar sua lista de sites</span><span class="sxs-lookup"><span data-stu-id="4fa1f-112">Prepare your site list</span></span>

<span data-ttu-id="4fa1f-113">Se você já tiver uma lista de sites do Modo Empresa para o IE11 ou a Versão Prévia do Microsoft Edge, poderá reutilizar para configurar o modo IE.</span><span class="sxs-lookup"><span data-stu-id="4fa1f-113">If you already have an Enterprise Mode site list for IE11 or Microsoft Edge Legacy, you can reuse it to configure IE mode.</span></span>

<span data-ttu-id="4fa1f-114">No entanto, se você não tiver uma lista de sites, poderá usar a [ferramenta de descoberta de sites de empresa](https://docs.microsoft.com/deployedge/edge-ie-mode-site-discovery) para preencher sua lista de sites.</span><span class="sxs-lookup"><span data-stu-id="4fa1f-114">However, if you don't have a site list, you can use the [Enterprise Site Discovery tool](https://docs.microsoft.com/deployedge/edge-ie-mode-site-discovery) to populate your site list.</span></span>

## <a name="configure-neutral-sites"></a><span data-ttu-id="4fa1f-115">Configurar sites neutros</span><span class="sxs-lookup"><span data-stu-id="4fa1f-115">Configure neutral sites</span></span>

<span data-ttu-id="4fa1f-116">Para que o modo IE funcione corretamente, os servidores de autenticação/logon único (SSO) precisam ser configurados explicitamente como sites neutros.</span><span class="sxs-lookup"><span data-stu-id="4fa1f-116">In order for IE mode to work properly, authentication / Single Sign-On (SSO) servers will need to be explicitly configured as neutral sites.</span></span> <span data-ttu-id="4fa1f-117">Caso contrário, as páginas do modo IE tentarão redirecionar para o Microsoft Edge e a autenticação falhará.</span><span class="sxs-lookup"><span data-stu-id="4fa1f-117">Otherwise, IE mode pages will try to redirect to Microsoft Edge, and authentication will fail.</span></span>

<span data-ttu-id="4fa1f-118">Um site neutro usará o navegador onde a navegação começou - no modo Microsoft Edge ou IE.</span><span class="sxs-lookup"><span data-stu-id="4fa1f-118">A neutral site will use the browser where the navigation started - either Microsoft Edge or IE mode.</span></span> <span data-ttu-id="4fa1f-119">A configuração de sites neutros garante que todos os aplicativos que usam esses servidores de autenticação, modernos e herdados, continuem funcionando.</span><span class="sxs-lookup"><span data-stu-id="4fa1f-119">Configuring neutral sites ensures that all applications using these authentication servers, both modern and legacy, continue to work.</span></span>

<span data-ttu-id="4fa1f-120">Para configurar sites neutros, configure o menu suspenso *Open In* como “Nenhum” na ferramenta Enterprise Mode Site List Manager ou atualizando diretamente o XML da lista de sites:</span><span class="sxs-lookup"><span data-stu-id="4fa1f-120">You can configure neutral sites by setting the *Open In* dropdown to 'None' in the Enterprise Mode Site List Manager tool or by directly updating the site list XML:</span></span>

``` xml
<site url="login.contoso.com">
   
    <open-in>None</open-in>

</site>
```

<span data-ttu-id="4fa1f-121">Para identificar servidores de autenticação, inspecione o tráfego de rede de um aplicativo usando as Ferramentas de Desenvolvedor do IE11.</span><span class="sxs-lookup"><span data-stu-id="4fa1f-121">To identify authentication servers, inspect the network traffic from an application using the IE11 Developer Tools.</span></span> <span data-ttu-id="4fa1f-122">Se precisar de mais tempo para identificar seus servidores de autenticação, você pode configurar uma política para manter todas as navegações in-page no modo IE para permitir que seus usuários continuem seus fluxos de trabalho sem interrupções.</span><span class="sxs-lookup"><span data-stu-id="4fa1f-122">If you need more time to identify your authentication servers, you can configure a policy to keep all in-page navigations in IE mode to allow your users to continue their workflows uninterrupted.</span></span> <span data-ttu-id="4fa1f-123">Para minimizar o uso do modo IE quando desnecessário, desabilite essa configuração depois de identificar e adicionar seus servidores de autenticação à lista de sites.</span><span class="sxs-lookup"><span data-stu-id="4fa1f-123">To minimize the use of IE mode when unnecessary, disable this setting once you've identified and added your authentication servers to the site list.</span></span> <span data-ttu-id="4fa1f-124">Para obter mais informações, confira [Manter a navegação na página no modo IE](https://docs.microsoft.com/deployedge/edge-learnmore-inpage-nav).</span><span class="sxs-lookup"><span data-stu-id="4fa1f-124">For more information, see [Keep in-page navigation in IE mode](https://docs.microsoft.com/deployedge/edge-learnmore-inpage-nav).</span></span>

>[!NOTE]
   ><span data-ttu-id="4fa1f-125">O esquema v.1 do modo empresa não é compatível com a integração do modo IE.</span><span class="sxs-lookup"><span data-stu-id="4fa1f-125">Enterprise Mode schema v.1 isn't supported for IE mode integration.</span></span> <span data-ttu-id="4fa1f-126">Se você estiver usando o esquema v.1 atualmente com o Internet Explorer 11, deverá atualizar para o esquema v.2.</span><span class="sxs-lookup"><span data-stu-id="4fa1f-126">If you are currently using schema v.1 with Internet Explorer 11, you must upgrade to schema v.2.</span></span> <span data-ttu-id="4fa1f-127">Para obter mais informações, confira [Diretrizes sobre o esquema v.2 do Modo Empresa](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance).</span><span class="sxs-lookup"><span data-stu-id="4fa1f-127">For more information, see [Enterprise Mode schema v.2 guidance](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance).</span></span>

## <a name="optional-use-cookie-sharing-if-necessary"></a><span data-ttu-id="4fa1f-128">(Opcional) Usar o compartilhamento de cookies, se necessário</span><span class="sxs-lookup"><span data-stu-id="4fa1f-128">(Optional) Use cookie sharing if necessary</span></span>

<span data-ttu-id="4fa1f-129">Por padrão, os processos do Microsoft Edge e do Internet Explorer não compartilham cookies de sessão e essa falta de compartilhamento pode ser inconveniente em alguns casos ao usar o modo IE.</span><span class="sxs-lookup"><span data-stu-id="4fa1f-129">By default, the Microsoft Edge and Internet Explorer processes don't share session cookies, and this lack of sharing can be inconvenient in some cases while using IE mode.</span></span> <span data-ttu-id="4fa1f-130">Por exemplo, quando um usuário precisa se autenticar novamente no modo IE quando anteriormente estava acostumado a fazê-lo ou ao sair de uma sessão do Microsoft Edge, não saia da sessão do modo Internet Explorer para transações críticas.</span><span class="sxs-lookup"><span data-stu-id="4fa1f-130">For example, when a user has to reauthenticate in IE mode when previously they are accustomed to doing so or when signing out of a Microsoft Edge session doesn’t sign out of the Internet Explorer mode session for critical transactions.</span></span> <span data-ttu-id="4fa1f-131">Nesses cenários, você pode configurar cookies específicos definidos pelo SSO para serem enviados do Microsoft Edge para o Internet Explorer para que a experiência de autenticação se torne mais contínua, eliminando a necessidade de reautenticação.</span><span class="sxs-lookup"><span data-stu-id="4fa1f-131">In these scenarios, you can configure specific cookies set by SSO to be sent from Microsoft Edge to Internet Explorer so the authentication experience becomes more seamless by eliminating the need to reauthenticate.</span></span> <span data-ttu-id="4fa1f-132">Para obter mais informações, confira[Compartilhamento de cookies do Microsoft Edge para o Internet Explorer](https://docs.microsoft.com/deployedge/edge-ie-mode-add-guidance-cookieshare).</span><span class="sxs-lookup"><span data-stu-id="4fa1f-132">For more information, see [Cookie sharing from Microsoft Edge to Internet Explorer](https://docs.microsoft.com/deployedge/edge-ie-mode-add-guidance-cookieshare).</span></span>

## <a name="see-also"></a><span data-ttu-id="4fa1f-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="4fa1f-133">See also</span></span>

- [<span data-ttu-id="4fa1f-134">Página de aterrissagem do Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="4fa1f-134">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="4fa1f-135">Sobre o modo IE</span><span class="sxs-lookup"><span data-stu-id="4fa1f-135">About IE mode</span></span>](./edge-ie-mode.md)
- [<span data-ttu-id="4fa1f-136">Informações adicionais sobre o Modo Empresarial</span><span class="sxs-lookup"><span data-stu-id="4fa1f-136">Additional Enterprise Mode information</span></span>](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
