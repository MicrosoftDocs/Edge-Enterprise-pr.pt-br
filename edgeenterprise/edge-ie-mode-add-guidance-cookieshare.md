---
title: Compartilhamento de cookies do Microsoft Edge para o Internet Explorer
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 12/21/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 'Como compartilhar os cookies do Microsoft Edge para o Internet Explorer '
ms.openlocfilehash: ddd9d34b5e2b0ee49093734da82e4a4fa7aa6a69
ms.sourcegitcommit: 306582403d4272831bcac390154c7cc7041a9b7e
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/21/2020
ms.locfileid: "11238178"
---
# <span data-ttu-id="c5dc2-103">Compartilhamento de cookies do Microsoft Edge para o Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="c5dc2-103">Cookie sharing from Microsoft Edge to Internet Explorer</span></span>

<span data-ttu-id="c5dc2-104">Este artigo explica como configurar o compartilhamento de cookie de sessão de um processo do Microsoft Edge para o processo do Internet Explorer, ao usar o modo Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="c5dc2-104">This article explains explains how to configure session cookie sharing from a Microsoft Edge process to Internet Explorer process, while using Internet Explorer mode.</span></span>

> [!NOTE]
> <span data-ttu-id="c5dc2-105">Este artigo se aplica ao Microsoft Edge versão 87 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="c5dc2-105">This article applies to Microsoft Edge version 87 or later.</span></span>

## <span data-ttu-id="c5dc2-106">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="c5dc2-106">Prerequisites</span></span>

- <span data-ttu-id="c5dc2-107">Atualizações do Windows</span><span class="sxs-lookup"><span data-stu-id="c5dc2-107">Windows updates</span></span>

  - <span data-ttu-id="c5dc2-108">Windows 10, versão 2004, Windows Server, versão 2004-KB4571744 ou superior</span><span class="sxs-lookup"><span data-stu-id="c5dc2-108">Windows 10 version 2004, Windows Server version 2004 - KB4571744 or higher</span></span>
  - <span data-ttu-id="c5dc2-109">Windows 10, versão 1909, Windows Server, versão 1909 – KB4566116 ou superior</span><span class="sxs-lookup"><span data-stu-id="c5dc2-109">Windows 10 version 1909, Windows Server version 1909 – KB4566116 or higher</span></span>
  - <span data-ttu-id="c5dc2-110">Windows 10, versão 1903, Windows Server, versão 1903 – KB4566116 ou superior</span><span class="sxs-lookup"><span data-stu-id="c5dc2-110">Windows 10 version 1903, Windows Server version 1903 – KB4566116 or higher</span></span>
  - <span data-ttu-id="c5dc2-111">Windows 10, versão 1809, Windows Server, versão 1809 e Windows Server 2019 - KB4571748 ou superior</span><span class="sxs-lookup"><span data-stu-id="c5dc2-111">Windows 10 version 1809, Windows Server version 1809, and Windows Server 2019 - KB4571748 or higher</span></span>
  - <span data-ttu-id="c5dc2-112">Windows 10 versão 1803 - KB4577032 ou superior</span><span class="sxs-lookup"><span data-stu-id="c5dc2-112">Windows 10 version 1803 – KB4577032 or higher</span></span>

- <span data-ttu-id="c5dc2-113">Microsoft Edge versão 87 ou posterior</span><span class="sxs-lookup"><span data-stu-id="c5dc2-113">Microsoft Edge version 87 or later</span></span>
- <span data-ttu-id="c5dc2-114">[ Modo IE ](https://aka.ms/iemodeonedge)   configurado com Lista de Sites do modo Empresarial</span><span class="sxs-lookup"><span data-stu-id="c5dc2-114">[IE mode](https://aka.ms/iemodeonedge) configured with Enterprise Mode Site List</span></span>

## <span data-ttu-id="c5dc2-115">Visão geral</span><span class="sxs-lookup"><span data-stu-id="c5dc2-115">Overview</span></span>

<span data-ttu-id="c5dc2-116">Uma configuração comum em grandes organizações é ter um aplicativo que funciona em um link de navegador moderno para outro aplicativo, que pode ser configurado para abrir no modo Internet Explorer com logon Único (SSO) habilitado como parte do fluxo de trabalho.</span><span class="sxs-lookup"><span data-stu-id="c5dc2-116">A common configuration in large organizations is to have an application that works on a modern browser link to another application, which might be configured to open in Internet Explorer mode with Single Sign On (SSO) enabled as part of the workflow.</span></span>

<span data-ttu-id="c5dc2-117">Por padrão, os processos do Microsoft Edge e do Internet Explorer não compartilham os cookies de sessão e isso pode ser inconveniente em alguns casos.</span><span class="sxs-lookup"><span data-stu-id="c5dc2-117">By default, the Microsoft Edge and Internet Explorer processes don't share session cookies, and this can be inconvenient in some cases.</span></span> <span data-ttu-id="c5dc2-118">Por exemplo, quando um usuário precisa se reautenticar no modo do Internet Explorer ou ao sair de uma sessão do Microsoft Edge, ele não sai da sessão do modo Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="c5dc2-118">For example, when a user has to re-authenticate in Internet Explorer mode or when signing out of an Microsoft Edge session doesn’t sign out of the Internet Explorer mode session.</span></span> <span data-ttu-id="c5dc2-119">Nesses cenários, você pode configurar os cookies específicos e definidos pelo SSO para serem enviados do Microsoft Edge para o Internet Explorer para que a experiência de autenticação torne-se mais contínua, eliminando a necessidade de reautenticação.</span><span class="sxs-lookup"><span data-stu-id="c5dc2-119">In these scenarios, you can configure specific cookies set by SSO to be sent from Microsoft Edge to Internet Explorer so the authentication experience becomes more seamless by eliminating the need to re-authenticate.</span></span>

> [!NOTE]
> <span data-ttu-id="c5dc2-120">Os cookies de sessão só podem ser compartilhados do Microsoft Edge para o Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="c5dc2-120">Session cookies can only be shared from Microsoft Edge to Internet Explorer.</span></span> <span data-ttu-id="c5dc2-121">Não é possível compartilhar os cookies de sessão ao contrário (do Internet Explorer para o Microsoft Edge).</span><span class="sxs-lookup"><span data-stu-id="c5dc2-121">Sharing session cookies in reverse (from Internet Explorer to Microsoft Edge) isn't possible.</span></span>

## <span data-ttu-id="c5dc2-122">Como funciona o compartilhamento de cookies</span><span class="sxs-lookup"><span data-stu-id="c5dc2-122">How cookie sharing works</span></span>

<span data-ttu-id="c5dc2-123">O XML da lista de sites do Modo Empresarial foi estendido para permitir que os elementos adicionais especifiquem os cookies que precisam ser compartilhados de uma sessão do Microsoft Edge com o Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="c5dc2-123">The Enterprise Mode site list XML has been extended to allow additional elements to specify cookies that need to be shared from a Microsoft Edge session with Internet Explorer.</span></span>  

<span data-ttu-id="c5dc2-124">Na primeira vez que uma guia do modo do Internet Explorer é criada em uma sessão do Microsoft Edge, todos os cookies correspondentes são compartilhados com a sessão do Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="c5dc2-124">The first time an Internet Explorer mode tab is created in a Microsoft Edge session, all matching cookies are shared to the Internet Explorer session.</span></span> <span data-ttu-id="c5dc2-125">Subsequentemente, sempre que um cookie que corresponde a uma regra é adicionado, excluído ou modificado, ele é enviado como uma atualização para a sessão do Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="c5dc2-125">Subsequently, any time a cookie that matches a rule is added, deleted, or modified it is sent as an update to the Internet Explorer session.</span></span> <span data-ttu-id="c5dc2-126">O conjunto de cookies compartilhados também é reavaliado quando a lista de sites é atualizada.</span><span class="sxs-lookup"><span data-stu-id="c5dc2-126">The set of shared cookies is also re-evaluated when the site list is updated.</span></span>

### <span data-ttu-id="c5dc2-127">Elementos do esquema atualizados</span><span class="sxs-lookup"><span data-stu-id="c5dc2-127">Updated schema elements</span></span>

<span data-ttu-id="c5dc2-128">A tabela a seguir descreve o elemento \<shared-cookie\> adicionado para oferecer suporte ao recurso de compartilhamento de cookies.</span><span class="sxs-lookup"><span data-stu-id="c5dc2-128">The following table describes the \<shared-cookie\> element added to support the cookie sharing feature.</span></span>

| <span data-ttu-id="c5dc2-129">Elemento</span><span class="sxs-lookup"><span data-stu-id="c5dc2-129">Element</span></span>| <span data-ttu-id="c5dc2-130">Descrição</span><span class="sxs-lookup"><span data-stu-id="c5dc2-130">Description</span></span> |
|-|-|
| \<shared-cookie **domain**=".contoso.com" **name**="cookie1"\>\</shared-cookie\><br><br><span data-ttu-id="c5dc2-131">OU</span><span class="sxs-lookup"><span data-stu-id="c5dc2-131">OR</span></span><br><br>\<shared-cookie **host**="subdomain.contoso.com" **name**="cookie2"\>\</shared-cookie\>   |<span data-ttu-id="c5dc2-132">\*\* (Obrigatório) \*\* Um elemento \<shared-cookie\> requer, no mínimo, um atributo de \* domínio \* (para os cookies de domínio) ou um \* host \* (para os cookies somente de host) e um atributo *nome*.</span><span class="sxs-lookup"><span data-stu-id="c5dc2-132">**(Required)** A \<shared-cookie\> element requires, at minimum, a *domain* (for domain cookies) or a *host* (for host-only cookies) attribute and a *name* attribute.</span></span><br><span data-ttu-id="c5dc2-133">Devem corresponder exatamente ao domínio e ao nome do cookie, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="c5dc2-133">These must be exact matches to the cookie's domain and name respectively.</span></span> <span data-ttu-id="c5dc2-134">**Observe** que os subdomínios não correspondem.</span><span class="sxs-lookup"><span data-stu-id="c5dc2-134">**Note** that subdomains do not match.</span></span><br><br><span data-ttu-id="c5dc2-135">O atributo *domínio* é usado para cookies de domínio (e um ponto inicial é permitido, mas opcional).</span><span class="sxs-lookup"><span data-stu-id="c5dc2-135">The *domain* attribute is used for domain cookies (and a leading dot is allowed but optional).</span></span><br><span data-ttu-id="c5dc2-136">O atributo \* host \* é usado para cookies somente de host (e um entrelinhamento é um erro).</span><span class="sxs-lookup"><span data-stu-id="c5dc2-136">The *host* attribute is used for host-only cookies (and a leading dot is an error).</span></span> <span data-ttu-id="c5dc2-137">Especificar que nenhum ou ambos resultará em erro.</span><span class="sxs-lookup"><span data-stu-id="c5dc2-137">Specifying neither or both will result in an error.</span></span><br><span data-ttu-id="c5dc2-138">\* Um cookie é um cookie de domínio se um domínio foi especificado na cadeia de caracteres do cookie (via cabeçalho de resposta HTTP Set-Cookie ou document.cookie JS API).</span><span class="sxs-lookup"><span data-stu-id="c5dc2-138">\* A cookie is a domain cookie if a domain was specified in the cookie string (via HTTP Set-Cookie response header or document.cookie JS API).</span></span> <span data-ttu-id="c5dc2-139">Um cookie de domínio se aplica ao domínio especificado e a todos os subdomínios.</span><span class="sxs-lookup"><span data-stu-id="c5dc2-139">A domain cookie applies to the specified domain and all subdomains.</span></span> <span data-ttu-id="c5dc2-140">Se um domínio não foi especificado na cadeia de caracteres do cookie, o cookie é um cookie somente de host e só se aplica ao host específico para o qual ele foi definido.</span><span class="sxs-lookup"><span data-stu-id="c5dc2-140">If a domain was not specified in the cookie string, the cookie is a host-only cookie and only applies to the specific host that it was set for.</span></span> <span data-ttu-id="c5dc2-141">Observe que algumas classes de URLs, como nomes de host de palavra única (por exemplo, http://intranetsite) e endereços IP (por exemplo, http://10.0.0.1) podem definir apenas os cookies de host.</span><span class="sxs-lookup"><span data-stu-id="c5dc2-141">Note that some classes of URLs such as single-word hostnames (e.g. http://intranetsite) and IP addresses (e.g. http://10.0.0.1) can only set host-only cookies.</span></span>    |
| \<shared-cookie **host**="subdomain.contoso.com" **name**="cookie2" **path**="/a/b/c"\>\</shared-cookie\>  | <span data-ttu-id="c5dc2-142">\*\* (Opcional) \*\* Um atributo \* caminho \* pode ser especificado.</span><span class="sxs-lookup"><span data-stu-id="c5dc2-142">**(Optional)** A *path* attribute may be specified.</span></span> <span data-ttu-id="c5dc2-143">Se nenhum atributo de caminho for especificado (ou se o atributo de caminho estiver vazio), quaisquer cookies que correspondam a domínio/host e nome corresponderão à política, independentemente do caminho (regra de caractere curinga).</span><span class="sxs-lookup"><span data-stu-id="c5dc2-143">If no path attribute is specified (or if the path attribute is empty), any cookies matching domain/host and name match the policy, regardless of path (wildcard rule).</span></span><br><br><span data-ttu-id="c5dc2-144">Se um caminho for especificado, ele deve ser uma correspondência exata.</span><span class="sxs-lookup"><span data-stu-id="c5dc2-144">If a path is specified, it must be an exact match.</span></span><br><span data-ttu-id="c5dc2-145">Se um cookie corresponder a uma regra com um caminho, isso terá precedência sobre uma regra sem caminho.</span><span class="sxs-lookup"><span data-stu-id="c5dc2-145">If a cookie matches a rule with a path, that takes precedence over a rule without a path.</span></span> |

#### <span data-ttu-id="c5dc2-146">Exemplo de compartilhamento</span><span class="sxs-lookup"><span data-stu-id="c5dc2-146">Sharing example</span></span>

```xml
<site-list version="1">
<shared-cookie domain=".contoso.com" name="cookie1"></shared-cookie> 
<shared-cookie host="subdomain.contoso.com" name="cookie2" path="/a/b/c">
</shared-cookie>
</site-list>
```

## <span data-ttu-id="c5dc2-147">Consulte também</span><span class="sxs-lookup"><span data-stu-id="c5dc2-147">See also</span></span>

- [<span data-ttu-id="c5dc2-148">Sobre o modo IE</span><span class="sxs-lookup"><span data-stu-id="c5dc2-148">About IE mode</span></span>](https://docs.microsoft.com/deployedge/edge-ie-mode)
- [<span data-ttu-id="c5dc2-149">Informações de sites configuráveis</span><span class="sxs-lookup"><span data-stu-id="c5dc2-149">Configurable sites information</span></span>](https://docs.microsoft.com/deployedge/edge-learnmore-configurable-sites-ie-mode)
- [<span data-ttu-id="c5dc2-150">Informações adicionais sobre o Modo Empresarial</span><span class="sxs-lookup"><span data-stu-id="c5dc2-150">Additional Enterprise Mode information</span></span>](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
- [<span data-ttu-id="c5dc2-151">Página de aterrissagem do Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="c5dc2-151">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
