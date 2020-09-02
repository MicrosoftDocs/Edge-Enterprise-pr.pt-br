---
title: Formato de filtro para políticas de URL do Microsoft Edge
ms.author: brianalt
author: dan-wesley
manager: srugh
ms.date: 05/01/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Saiba mais sobre o formato de filtro usado para as políticas URLBlocklist e URLAllowlist do Microsoft Edge.
ms.openlocfilehash: 5a0eff1ca7be17fccd1087716d426b13ea302847
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979065"
---
# <span data-ttu-id="d8f84-103">Formato de filtro para políticas baseadas em lista de URL</span><span class="sxs-lookup"><span data-stu-id="d8f84-103">Filter format for URL list-based policies</span></span>

<span data-ttu-id="d8f84-104">Este artigo descreve o formato de filtro usado para as políticas baseadas em lista de URLs do Microsoft Edge (por exemplo, as políticas [URLBlocklist](microsoft-edge-policies.md#urlblocklist), [URLAllowList](microsoft-edge-policies.md#urlallowlist) e [CertificateTransparencyEnforcementDisabledForUrls](microsoft-edge-policies.md#certificatetransparencyenforcementdisabledforurls).</span><span class="sxs-lookup"><span data-stu-id="d8f84-104">This article describes the filter format used for the Microsoft Edge URL list-based policies (For example, [URLBlocklist](microsoft-edge-policies.md#urlblocklist), [URLAllowList](microsoft-edge-policies.md#urlallowlist), and [CertificateTransparencyEnforcementDisabledForUrls](microsoft-edge-policies.md#certificatetransparencyenforcementdisabledforurls) policies.</span></span>

> [!NOTE]
> <span data-ttu-id="d8f84-105">Este artigo aplica-se ao Microsoft Edge versão 77 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="d8f84-105">This article applies to Microsoft Edge version 77 or later.</span></span>

## <span data-ttu-id="d8f84-106">O formato de filtro</span><span class="sxs-lookup"><span data-stu-id="d8f84-106">The filter format</span></span>

<span data-ttu-id="d8f84-107">O formato de filtro é:</span><span class="sxs-lookup"><span data-stu-id="d8f84-107">The filter format is:</span></span>

```
    [scheme://][.]host[:port][/path][@query]
```

<span data-ttu-id="d8f84-108">Os campos no formato de filtro são:</span><span class="sxs-lookup"><span data-stu-id="d8f84-108">The fields in the filter format are:</span></span>

| <span data-ttu-id="d8f84-109">Campo</span><span class="sxs-lookup"><span data-stu-id="d8f84-109">Field</span></span> | <span data-ttu-id="d8f84-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="d8f84-110">Description</span></span> |
| --- | --- |
| <span data-ttu-id="d8f84-111">**esquema** (*opcional*)</span><span class="sxs-lookup"><span data-stu-id="d8f84-111">**scheme** (*optional*)</span></span> | <span data-ttu-id="d8f84-112">Ele pode ser http://, https://, ftp://, edge:// etc.</span><span class="sxs-lookup"><span data-stu-id="d8f84-112">It can be http://, https://, ftp://, edge://, etc.</span></span> |
| <span data-ttu-id="d8f84-113">**host** (*necessário*)</span><span class="sxs-lookup"><span data-stu-id="d8f84-113">**host** (*required*)</span></span> | <span data-ttu-id="d8f84-114">Ele deve ser um nome de host ou endereço IP válido e você pode usar um caractere curinga ("\*").</span><span class="sxs-lookup"><span data-stu-id="d8f84-114">It must be a valid host name or IP address and you can use a wildcard ("\*").</span></span> <span data-ttu-id="d8f84-115">Para desabilitar a correspondência de subdomínio, inclua um ponto opcional (".") antes do **host**.</span><span class="sxs-lookup"><span data-stu-id="d8f84-115">To disable subdomain matching, include an optional dot (".") before **host**.</span></span> |
| <span data-ttu-id="d8f84-116">**porta** (*opcional*)</span><span class="sxs-lookup"><span data-stu-id="d8f84-116">**port** (*optional*)</span></span> | <span data-ttu-id="d8f84-117">Os valores válidos variam de 1 a 65535.</span><span class="sxs-lookup"><span data-stu-id="d8f84-117">Valid values range from 1 to 65535.</span></span> |
| <span data-ttu-id="d8f84-118">**caminho** (*opcional*)</span><span class="sxs-lookup"><span data-stu-id="d8f84-118">**path** (*optional*)</span></span> | <span data-ttu-id="d8f84-119">Você pode usar qualquer cadeia de caracteres no caminho.</span><span class="sxs-lookup"><span data-stu-id="d8f84-119">You can use any string in the path.</span></span> |
| <span data-ttu-id="d8f84-120">**consulta** (*opcional*)</span><span class="sxs-lookup"><span data-stu-id="d8f84-120">**query** (*optional*)</span></span> | <span data-ttu-id="d8f84-121">A **consulta** é de tokens chave-valor ou somente chave-valor separados por um "E" comercial ("&").</span><span class="sxs-lookup"><span data-stu-id="d8f84-121">The **query** is either key-value or key-only tokens separated by an ampersand ("&").</span></span> <span data-ttu-id="d8f84-122">Separe os tokens de chave-valor com um sinal de igual ("=").</span><span class="sxs-lookup"><span data-stu-id="d8f84-122">Separate key-value tokens with an equal sign ("=").</span></span> <span data-ttu-id="d8f84-123">Para indicar uma correspondência de prefixo, você pode usar um asterisco ("\*") no final da **consulta**.</span><span class="sxs-lookup"><span data-stu-id="d8f84-123">To indicate a prefix match, you can use an asterisk ("\*") at the end of the **query**.</span></span> |

## <span data-ttu-id="d8f84-124">Como comprar o formato de filtro ao formato de URL</span><span class="sxs-lookup"><span data-stu-id="d8f84-124">Comparing the filter format to the URL format</span></span>

<span data-ttu-id="d8f84-125">O formato do filtro é parecido com o formato da URL, exceto pelo seguinte:</span><span class="sxs-lookup"><span data-stu-id="d8f84-125">The filter format resembles the URL format, except for the following differences:</span></span>

- <span data-ttu-id="d8f84-126">Se você incluir "user:pass", ele será ignorado.</span><span class="sxs-lookup"><span data-stu-id="d8f84-126">If you include "user:pass", it will be ignored.</span></span> <span data-ttu-id="d8f84-127">Por exemplo, http://user:pass@ftp.contoso.com/pub/example.iso.</span><span class="sxs-lookup"><span data-stu-id="d8f84-127">For example, http://user:pass@ftp.contoso.com/pub/example.iso.</span></span>
- <span data-ttu-id="d8f84-128">Se você incluir um identificador de fragmento ("#"), ele e tudo que vier depois dele serão ignorados.</span><span class="sxs-lookup"><span data-stu-id="d8f84-128">If you include a fragment identifier ("#"), it and everything that follows the identifier is ignored.</span></span>
- <span data-ttu-id="d8f84-129">Você pode usar um caractere curinga ("\*") como o **host** e pode prefixá-lo com um ponto (".").</span><span class="sxs-lookup"><span data-stu-id="d8f84-129">You can use a wildcard ("\*") as the **host** and you can prefix it with a dot (".").</span></span>
- <span data-ttu-id="d8f84-130">Você pode usar uma barra ("/") ou um ponto (".") como sufixo para o **host**.</span><span class="sxs-lookup"><span data-stu-id="d8f84-130">You can use a forward slash ("/") or a dot (".") as a suffix for the **host**.</span></span> <span data-ttu-id="d8f84-131">Nesse caso, o sufixo é ignorado.</span><span class="sxs-lookup"><span data-stu-id="d8f84-131">In this case, the suffix is ignored.</span></span>

## <span data-ttu-id="d8f84-132">Critérios de seleção de filtro</span><span class="sxs-lookup"><span data-stu-id="d8f84-132">Filter selection criteria</span></span>

<span data-ttu-id="d8f84-133">O filtro selecionado para uma URL é a correspondência mais específica encontrada após o processamento das seguintes regras de seleção de filtro:</span><span class="sxs-lookup"><span data-stu-id="d8f84-133">The filter selected for a URL is the most specific match found after processing the following filter selection rules:</span></span>

1. <span data-ttu-id="d8f84-134">Os filtros com a correspondência de **host** mais longa são selecionados primeiro.</span><span class="sxs-lookup"><span data-stu-id="d8f84-134">Filters with the longest **host** match are selected first.</span></span>
2. <span data-ttu-id="d8f84-135">Dos filtros selecionados, todos os filtros com um esquema ou porta sem correspondência são descartados.</span><span class="sxs-lookup"><span data-stu-id="d8f84-135">From the selected filters, any filter with a non-matching scheme or port is discarded.</span></span>
3. <span data-ttu-id="d8f84-136">Nos filtros restantes, o filtro com o **caminho** de correspondência mais longo é selecionado.</span><span class="sxs-lookup"><span data-stu-id="d8f84-136">From the remaining filters, the filter with the longest matching **path** is selected.</span></span>
4. <span data-ttu-id="d8f84-137">Nos filtros restantes, o filtro com o conjunto de tokens de consulta mais longo é selecionado.</span><span class="sxs-lookup"><span data-stu-id="d8f84-137">From the remaining filters, the filter with the longest set of query tokens is selected.</span></span> <span data-ttu-id="d8f84-138">Nesta etapa, o filtro de lista de permissões terá precedência sobre o filtro de lista de bloqueios se os dois filtros tiverem o mesmo tamanho de **caminho** e número de tokens de **consulta**.</span><span class="sxs-lookup"><span data-stu-id="d8f84-138">At this step, the allow list filter takes precedence over the block list filter if both filters have the same **path** length and number of **query** tokens.</span></span>
5. <span data-ttu-id="d8f84-139">Se não houver um filtro válido restante, o subdomínio mais à esquerda será removido do **host** e o processo de seleção será reiniciado na etapa 1.</span><span class="sxs-lookup"><span data-stu-id="d8f84-139">If there's no valid filter remaining, then the left-most subdomain is removed from **host** and the selection process starts over at step 1.</span></span> <span data-ttu-id="d8f84-140">O **host** de asterisco especial ("\*") é o último pesquisado e corresponde a todos os hosts.</span><span class="sxs-lookup"><span data-stu-id="d8f84-140">The special asterisk ("\*") **host** is the last searched and it matches all hosts.</span></span>
6. <span data-ttu-id="d8f84-141">Se um filtro estiver disponível, ele bloqueará ou permitirá a solicitação de URL.</span><span class="sxs-lookup"><span data-stu-id="d8f84-141">If a filter's available, it blocks or allows the URL request.</span></span>

   >[!NOTE]
   ><span data-ttu-id="d8f84-142">O comportamento padrão é permitir a solicitação de URL se nenhum filtro corresponder.</span><span class="sxs-lookup"><span data-stu-id="d8f84-142">The default behavior is to allow the URL request if no filter is matched.</span></span>

## <span data-ttu-id="d8f84-143">Critérios de seleção de filtro de exemplo</span><span class="sxs-lookup"><span data-stu-id="d8f84-143">Example filter selection criteria</span></span>

<span data-ttu-id="d8f84-144">Neste exemplo, ao procurar uma correspondência para "https://sub.contoso.com/docs" a seleção de filtro:</span><span class="sxs-lookup"><span data-stu-id="d8f84-144">In this example, when searching for a match to "https://sub.contoso.com/docs" the filter selection will:</span></span>

1. <span data-ttu-id="d8f84-145">Procurará um filtro para "sub.contoso.com".</span><span class="sxs-lookup"><span data-stu-id="d8f84-145">Search for a filter for "sub.contoso.com".</span></span> <span data-ttu-id="d8f84-146">Se encontrar um filtro, a pesquisa prosseguirá para a etapa 2.</span><span class="sxs-lookup"><span data-stu-id="d8f84-146">If it finds a filter, the search moves to step 2.</span></span> <span data-ttu-id="d8f84-147">Se um filtro não for encontrado, ela tentará novamente com "contoso.com", "com" e, por fim, "".</span><span class="sxs-lookup"><span data-stu-id="d8f84-147">If a filter isn't found, then it tries again with "contoso.com", "com", and finally "".</span></span>
2. <span data-ttu-id="d8f84-148">Nos filtros selecionados, qualquer um que não tenha "http" no **esquema** será removido.</span><span class="sxs-lookup"><span data-stu-id="d8f84-148">From the selected filters, any that don't have "http" in the **scheme** are removed.</span></span>
3. <span data-ttu-id="d8f84-149">Dos filtros restantes, qualquer um que tenha um número de porta exato que não seja "80" será removido.</span><span class="sxs-lookup"><span data-stu-id="d8f84-149">From the remaining filters, any that have an exact port number that isn't "80" are removed.</span></span>
4. <span data-ttu-id="d8f84-150">Dos filtros restantes, qualquer um que não tenha "/docs" como prefixo do **caminho** será removido.</span><span class="sxs-lookup"><span data-stu-id="d8f84-150">From the remaining filters, any that don't have "/docs" as a prefix of the **path** are removed.</span></span>
5. <span data-ttu-id="d8f84-151">Dos filtros restantes, o filtro com o maior prefixo de caminho será selecionado e aplicado.</span><span class="sxs-lookup"><span data-stu-id="d8f84-151">From the remaining filters, the filter with the longest path prefix is selected and applied.</span></span> <span data-ttu-id="d8f84-152">Se um filtro não for encontrado, o processo de seleção será reiniciado novamente na etapa 1.</span><span class="sxs-lookup"><span data-stu-id="d8f84-152">If a filter isn't found, the selection process starts over again at step 1.</span></span> <span data-ttu-id="d8f84-153">O processo é repetido com o próximo subdomínio.</span><span class="sxs-lookup"><span data-stu-id="d8f84-153">The process is repeated with the next subdomain.</span></span>

### <span data-ttu-id="d8f84-154">Informações adicionais de filtro</span><span class="sxs-lookup"><span data-stu-id="d8f84-154">Additional filter information</span></span>

<span data-ttu-id="d8f84-155">Se um filtro tiver um ponto (".") prefixando o **host**, então somente as correspondências de **host** exatas serão filtradas.</span><span class="sxs-lookup"><span data-stu-id="d8f84-155">If a filter has a dot (".") prefixing the **host** then only exact **host** matches are filtered.</span></span> <span data-ttu-id="d8f84-156">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="d8f84-156">For example:</span></span>

- <span data-ttu-id="d8f84-157">“contoso.com” (sem ponto) corresponderá a “contoso.com”, “www.contoso.com” e “sub.www.contoso.com”</span><span class="sxs-lookup"><span data-stu-id="d8f84-157">"contoso.com" (no dot) will match "contoso.com", "www.contoso.com", and "sub.www.contoso.com"</span></span>
- <span data-ttu-id="d8f84-158">“.www.contoso.com” (com um prefixo de ponto) só corresponderá a “www.contoso.com”</span><span class="sxs-lookup"><span data-stu-id="d8f84-158">".www.contoso.com" (with a dot prefix) will only match "www.contoso.com"</span></span>

<span data-ttu-id="d8f84-159">Você pode usar um **esquema** padrão ou de cliente.</span><span class="sxs-lookup"><span data-stu-id="d8f84-159">You can use either a standard or customer **schema**.</span></span> <span data-ttu-id="d8f84-160">Os esquemas padrão com suporte incluem:</span><span class="sxs-lookup"><span data-stu-id="d8f84-160">Supported standard schemas include:</span></span>

- <span data-ttu-id="d8f84-161">_about_, _blob_, _content_, _edge_, _cid_, _data_, _file_, _filesystem_, _ftp_, _gopher_, _http_, _https_, _javascript_, _mailto_, _ws_ e _wss_.</span><span class="sxs-lookup"><span data-stu-id="d8f84-161">_about_, _blob_, _content_, _edge_, _cid_, _data_, _file_, _filesystem_, _ftp_, _gopher_, _http_, _https_, _javascript_, _mailto_, _ws_, and _wss_.</span></span>

<span data-ttu-id="d8f84-162">Qualquer outro **esquema** será tratado como um **esquema** personalizado, mas somente os padrões _schema:\*_ e _schema://\*_ são permitidos.</span><span class="sxs-lookup"><span data-stu-id="d8f84-162">Any other **schema** is treated as a custom **schema**, but only the _schema:\*_ and _schema://\*_ patterns are allowed.</span></span> <span data-ttu-id="d8f84-163">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="d8f84-163">For example:</span></span>

- <span data-ttu-id="d8f84-164">“custom:*” ou “custom://*” corresponderá a “custom:app”</span><span class="sxs-lookup"><span data-stu-id="d8f84-164">"custom:*" or "custom://*" will match "custom:app"</span></span>
- <span data-ttu-id="d8f84-165">“custom:app” ou “custom://app” são inválidos</span><span class="sxs-lookup"><span data-stu-id="d8f84-165">"custom:app" or "custom://app" are invalid</span></span>

<span data-ttu-id="d8f84-166">**schema** e **host** não diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="d8f84-166">**schema** and **host** aren't case-sensitive.</span></span> <span data-ttu-id="d8f84-167">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="d8f84-167">For example:</span></span>

- <span data-ttu-id="d8f84-168">O filtro “http://contoso.com” corresponde a “HTTP://contoso.com”, “http://contoso.COM” e “http://contoso.com”</span><span class="sxs-lookup"><span data-stu-id="d8f84-168">"http://contoso.com" filter matches "HTTP://contoso.com", "http://contoso.COM", and "http://contoso.com"</span></span>

<span data-ttu-id="d8f84-169">**path** e **query** diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="d8f84-169">**path** and **query** are case-sensitive.</span></span> <span data-ttu-id="d8f84-170">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="d8f84-170">For example:</span></span>

- <span data-ttu-id="d8f84-171">O filtro “http://contoso.com/path?query=A” não corresponde a “http://contoso.com/Path?query=A” ou “http://contoso.com/path?Query=A”.</span><span class="sxs-lookup"><span data-stu-id="d8f84-171">"http://contoso.com/path?query=A" filter doesn't match "http://contoso.com/Path?query=A" or "http://contoso.com/path?Query=A".</span></span> <span data-ttu-id="d8f84-172">Ele corresponde a “http://contoso.COM/path?query=A”.</span><span class="sxs-lookup"><span data-stu-id="d8f84-172">It does match "http://contoso.COM/path?query=A".</span></span>

## <span data-ttu-id="d8f84-173">Licença de conteúdo</span><span class="sxs-lookup"><span data-stu-id="d8f84-173">Content license</span></span>

> [!NOTE]
> <span data-ttu-id="d8f84-174">Partes desta página são modificações baseadas no trabalho criado e compartilhado pela Chromium.org e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional](http://creativecommons.org/licenses/by/4.0/).</span><span class="sxs-lookup"><span data-stu-id="d8f84-174">Portions of this page are modifications based on work created and shared by Chromium.org and used according to terms described in the [Creative Commons Attribution 4.0 International License](http://creativecommons.org/licenses/by/4.0/).</span></span> <span data-ttu-id="d8f84-175">A página original do [Chromium pode ser encontrada aqui](https://www.chromium.org/administrators/url-blacklist-filter-format).</span><span class="sxs-lookup"><span data-stu-id="d8f84-175">The original [Chromium page can be found here](https://www.chromium.org/administrators/url-blacklist-filter-format).</span></span>
  
<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br /><span data-ttu-id="d8f84-176">Esse trabalho é licenciado sob uma <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons</a>.</span><span class="sxs-lookup"><span data-stu-id="d8f84-176">This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.</span></span>

## <span data-ttu-id="d8f84-177">Consulte também</span><span class="sxs-lookup"><span data-stu-id="d8f84-177">See also</span></span>

- [<span data-ttu-id="d8f84-178">Página de aterrissagem do Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="d8f84-178">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
