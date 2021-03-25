---
title: Configurações de proxy do Microsoft Edge
ms.author: brianalt
author: dan-wesley
manager: srugh
ms.date: 05/01/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 'Usar opções de linha de comando para definir as configurações de proxy '
ms.openlocfilehash: d0924f723aab6832e5b4eb70c60e1d329d3c7a9d
ms.sourcegitcommit: f363ceb6c42054fabc95ce8d7bca3c52d80e6a9f
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/24/2021
ms.locfileid: "11447635"
---
# <a name="how-to-use-microsoft-edge-command-line-options-to-configure-proxy-settings"></a><span data-ttu-id="c61e1-103">Como usar as opções de linha de comando do Microsoft Edge para definir as configurações de proxy</span><span class="sxs-lookup"><span data-stu-id="c61e1-103">How to use Microsoft Edge command-line options to configure proxy settings</span></span>

<span data-ttu-id="c61e1-104">Este artigo descreve como você pode usar as opções de linha de comando para substituir as configurações de rede do sistema padrão.</span><span class="sxs-lookup"><span data-stu-id="c61e1-104">This article describes how you can use command-line options to override the default system network settings.</span></span>

>[!NOTE]
><span data-ttu-id="c61e1-105">Este artigo aplica-se ao Microsoft Edge versão 77 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="c61e1-105">This article applies to Microsoft Edge version 77 or later.</span></span>

## <a name="system-network-settings"></a><span data-ttu-id="c61e1-106">Configurações de rede do sistema</span><span class="sxs-lookup"><span data-stu-id="c61e1-106">System network settings</span></span>

<span data-ttu-id="c61e1-107">Por padrão, a pilha de rede do Microsoft Edge usa as configurações de rede do sistema.</span><span class="sxs-lookup"><span data-stu-id="c61e1-107">The Microsoft Edge network stack uses the system network settings by default.</span></span> <span data-ttu-id="c61e1-108">Essas configurações incluem as *configurações de proxy* e os *repositórios de certificados e chaves privadas*.</span><span class="sxs-lookup"><span data-stu-id="c61e1-108">These settings include *proxy settings*, and *certificate and private key stores*.</span></span>

<span data-ttu-id="c61e1-109">Há cenários em que os usuários solicitam uma alternativa ao uso das configurações padrão de proxy do sistema.</span><span class="sxs-lookup"><span data-stu-id="c61e1-109">There are scenarios where users request an alternative to using the system's default proxy settings.</span></span> <span data-ttu-id="c61e1-110">Para dar suporte a esses cenários, o Microsoft Edge é compatível com opções de linha de comando que você pode usar para definir configurações de proxy personalizadas.</span><span class="sxs-lookup"><span data-stu-id="c61e1-110">To support these scenarios, Microsoft Edge supports command-line options that you can use to configure custom proxy settings.</span></span>

<span data-ttu-id="c61e1-111">Essas opções de linha de comando correspondem às seguintes políticas no grupo **Servidor de proxy**:</span><span class="sxs-lookup"><span data-stu-id="c61e1-111">These command-line options correspond to the following policies in the **Proxy server** group:</span></span>

- [<span data-ttu-id="c61e1-112">ProxyBypassList</span><span class="sxs-lookup"><span data-stu-id="c61e1-112">ProxyBypassList</span></span>](./microsoft-edge-policies.md#proxybypasslist)
- [<span data-ttu-id="c61e1-113">ProxyMode</span><span class="sxs-lookup"><span data-stu-id="c61e1-113">ProxyMode</span></span>](./microsoft-edge-policies.md#proxymode)
- [<span data-ttu-id="c61e1-114">ProxyPacUrl</span><span class="sxs-lookup"><span data-stu-id="c61e1-114">ProxyPacUrl</span></span>](./microsoft-edge-policies.md#proxypacurl)
- [<span data-ttu-id="c61e1-115">ProxyServer</span><span class="sxs-lookup"><span data-stu-id="c61e1-115">ProxyServer</span></span>](./microsoft-edge-policies.md#proxyserver)
- [<span data-ttu-id="c61e1-116">ProxySettings</span><span class="sxs-lookup"><span data-stu-id="c61e1-116">ProxySettings</span></span>](./microsoft-edge-policies.md#proxysettings)

## <a name="command-line-options-for-proxy-settings"></a><span data-ttu-id="c61e1-117">Opções de linha de comando para configurações de proxy</span><span class="sxs-lookup"><span data-stu-id="c61e1-117">Command-line options for proxy settings</span></span>

<span data-ttu-id="c61e1-118">O Microsoft Edge dá suporte às seguintes opções de linha de comando relacionadas ao proxy.</span><span class="sxs-lookup"><span data-stu-id="c61e1-118">Microsoft Edge supports the following proxy-related command-line options.</span></span>

 **`--no-proxy-server`**
 
<span data-ttu-id="c61e1-119">Informa ao Microsoft Edge para não usar um Proxy, mesmo que o sistema esteja de alguma forma configurado para usar um.</span><span class="sxs-lookup"><span data-stu-id="c61e1-119">Tells Microsoft Edge not to use a Proxy, even if the system is otherwise configured to use one.</span></span> <span data-ttu-id="c61e1-120">Ela substitui todas as outras configurações de proxy fornecidas.</span><span class="sxs-lookup"><span data-stu-id="c61e1-120">It overrides any other proxy settings that are provided.</span></span>

**`--proxy-auto-detect`**

<span data-ttu-id="c61e1-121">Informa ao Microsoft Edge para tentar detectar automaticamente sua configuração de proxy.</span><span class="sxs-lookup"><span data-stu-id="c61e1-121">Tells Microsoft Edge to try and automatically detect your proxy configuration.</span></span> <span data-ttu-id="c61e1-122">Esse argumento será ignorado se `--proxy-server` estiver configurado.</span><span class="sxs-lookup"><span data-stu-id="c61e1-122">This argument is ignored if `--proxy-server` is configured.</span></span>

**`--proxy-server=<scheme>=<uri>[:<port>][;...] | <uri>[:<port>] | "direct://"`**

<span data-ttu-id="c61e1-123">Informa ao Microsoft Edge para usar uma configuração de proxy personalizada.</span><span class="sxs-lookup"><span data-stu-id="c61e1-123">Tells Microsoft Edge to use a custom proxy configuration.</span></span> <span data-ttu-id="c61e1-124">Você pode especificar uma configuração de proxy personalizada de três maneiras.</span><span class="sxs-lookup"><span data-stu-id="c61e1-124">You can specify a custom proxy configuration in three ways.</span></span>

1. <span data-ttu-id="c61e1-125">Forneça um mapeamento separado por ponto-e-vírgula de esquemas de lista para pares de url/porta.</span><span class="sxs-lookup"><span data-stu-id="c61e1-125">Provide a semicolon-separated mapping of list scheme to url/port pairs.</span></span> <span data-ttu-id="c61e1-126">Por exemplo, `--proxy-server="http=proxy1:8080;ftp=ftpproxy"` diz ao Microsoft Edge para usar o proxy HTTP "proxy1:8080" para URLs de http e o proxy HTTP "ftpproxy:80" para URLs de ftp.</span><span class="sxs-lookup"><span data-stu-id="c61e1-126">For example, `--proxy-server="http=proxy1:8080;ftp=ftpproxy"` tells Microsoft Edge to use HTTP proxy "proxy1:8080" for http URLs and HTTP proxy "ftpproxy:80" for ftp URLs.</span></span>
2. <span data-ttu-id="c61e1-127">Fornecendo um único uri com porta opcional a ser usada para todas as URLs.</span><span class="sxs-lookup"><span data-stu-id="c61e1-127">By providing a single uri with optional port to use for all URLs.</span></span> <span data-ttu-id="c61e1-128">Por exemplo, `--proxy-server="proxy2:8080"` usará o proxy em "proxy2:8080" para todo o tráfego.</span><span class="sxs-lookup"><span data-stu-id="c61e1-128">For example, `--proxy-server="proxy2:8080"` will use the proxy at "proxy2:8080" for all traffic.</span></span>
3. <span data-ttu-id="c61e1-129">Usando o valor especial "direct://".</span><span class="sxs-lookup"><span data-stu-id="c61e1-129">By using the special "direct://" value.</span></span> <span data-ttu-id="c61e1-130">Por exemplo, `--proxy-server="direct://"` fará com que nenhuma conexão use um proxy.</span><span class="sxs-lookup"><span data-stu-id="c61e1-130">For example, `--proxy-server="direct://"` will make all connections not use a proxy.</span></span> 

>[!NOTE]
><span data-ttu-id="c61e1-131">Você pode configurar o Microsoft Edge para tentar usar um proxy e fazer fallback para entrar diretamente se o proxy não estiver disponível.</span><span class="sxs-lookup"><span data-stu-id="c61e1-131">You can configure Microsoft Edge to try using a proxy and fallback to going direct if the proxy isn't available.</span></span> <span data-ttu-id="c61e1-132">Por exemplo, `--proxy-server="http://proxy2:8080,direct://`.</span><span class="sxs-lookup"><span data-stu-id="c61e1-132">For example, `--proxy-server="http://proxy2:8080,direct://`.</span></span>

**`--proxy-bypass-list=(<trailing_domain>|<ip-address>)[:<port>][;...]`**

<span data-ttu-id="c61e1-133">Informa ao Microsoft Edge para ignorar qualquer proxy especificado para a lista de hosts separados por ponto-e-vírgula especificada.</span><span class="sxs-lookup"><span data-stu-id="c61e1-133">Tells Microsoft Edge to bypass any specified proxy for the specified semicolon-separated list of hosts.</span></span> <span data-ttu-id="c61e1-134">Esse sinalizador deve ser usado com `--proxy-server`.</span><span class="sxs-lookup"><span data-stu-id="c61e1-134">This flag must be used with `--proxy-server`.</span></span>

>[!NOTE]
><span data-ttu-id="c61e1-135">A correspondência de domínio à direita não requer separadores ".", "\*microsoft.com" corresponderá a "imicrosoft.com".</span><span class="sxs-lookup"><span data-stu-id="c61e1-135">Trailing-domain matching doesn't require "." separators, "\*microsoft.com" will match "imicrosoft.com".</span></span> <span data-ttu-id="c61e1-136">Por exemplo, `--proxy-server="proxy2:8080" --proxy-bypass-list="*.microsoft.com;*example.com;127.0.0.1:8080"` usará o servidor proxy "proxy2" na porta 8080 para todos os hosts, exceto as solicitações para \*.microsoft.com, example.com e 127.0.0.1 na porta 8080.</span><span class="sxs-lookup"><span data-stu-id="c61e1-136">For example, `--proxy-server="proxy2:8080" --proxy-bypass-list="*.microsoft.com;*example.com;127.0.0.1:8080"` will use the proxy server "proxy2" on port 8080 for all hosts except requests for \*.microsoft.com, example.com, and 127.0.0.1 on port 8080.</span></span> <span data-ttu-id="c61e1-137">No exemplo anterior, as solicitações de imicrosoft.com ainda serão mediadas por proxy.</span><span class="sxs-lookup"><span data-stu-id="c61e1-137">In the previous example, imicrosoft.com requests will still be proxied.</span></span> <span data-ttu-id="c61e1-138">No entanto, as solicitações de iexample.com ignoram o proxy porque \* example.com foi especificado em vez de \*. example.com.</span><span class="sxs-lookup"><span data-stu-id="c61e1-138">However, iexample.com requests will bypass the proxy because \*example.com was specified instead of \*.example.com.</span></span>

**`--proxy-pac-url=<pac-file-url>`**

<span data-ttu-id="c61e1-139">Informa ao Microsoft Edge para usar o arquivo PAC na URL especificada.</span><span class="sxs-lookup"><span data-stu-id="c61e1-139">Tells Microsoft Edge to use the PAC file at the specified URL.</span></span> <span data-ttu-id="c61e1-140">Por exemplo, `--proxy-pac-url="https://wpad/proxy.pac"` informa o Microsoft Edge para resolver informações de proxy de solicitações de URL usando o arquivo **proxy.pac**.</span><span class="sxs-lookup"><span data-stu-id="c61e1-140">For example, `--proxy-pac-url="https://wpad/proxy.pac"` tells Microsoft Edge to resolve proxy information for URL requests using the **proxy.pac** file.</span></span>

## <a name="content-license"></a><span data-ttu-id="c61e1-141">Licença de conteúdo</span><span class="sxs-lookup"><span data-stu-id="c61e1-141">Content license</span></span>

> [!NOTE]
> <span data-ttu-id="c61e1-142">Partes desta página são modificações baseadas no trabalho criado e compartilhado pela Chromium.org e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional](http://creativecommons.org/licenses/by/4.0/).</span><span class="sxs-lookup"><span data-stu-id="c61e1-142">Portions of this page are modifications based on work created and shared by Chromium.org and used according to terms described in the [Creative Commons Attribution 4.0 International License](http://creativecommons.org/licenses/by/4.0/).</span></span> <span data-ttu-id="c61e1-143">A página original pode ser encontrada [aqui](https://www.chromium.org/developers/design-documents/network-settings#TOC-Command-line-options-for-proxy-sett).</span><span class="sxs-lookup"><span data-stu-id="c61e1-143">The original page can be found [here](https://www.chromium.org/developers/design-documents/network-settings#TOC-Command-line-options-for-proxy-sett).</span></span>
  
<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br /><span data-ttu-id="c61e1-144">Esse trabalho é licenciado sob uma <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons</a>.</span><span class="sxs-lookup"><span data-stu-id="c61e1-144">This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.</span></span>

## <a name="see-also"></a><span data-ttu-id="c61e1-145">Consulte também</span><span class="sxs-lookup"><span data-stu-id="c61e1-145">See also</span></span>

- <span data-ttu-id="c61e1-146">Para ver as configurações avançadas e as opções adicionais, consulte a [documentação do proxy](https://chromium.googlesource.com/chromium/src/+/HEAD/net/docs/proxy.md) no projeto Chromium Open Source.</span><span class="sxs-lookup"><span data-stu-id="c61e1-146">To see advanced configuration settings and additional options, consult the [proxy documentation](https://chromium.googlesource.com/chromium/src/+/HEAD/net/docs/proxy.md) in the Chromium Open Source project.</span></span>
- [<span data-ttu-id="c61e1-147">Página de aterrissagem do Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="c61e1-147">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)