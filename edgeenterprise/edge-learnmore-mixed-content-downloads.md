---
title: Microsoft Edge e downloads de conteúdo misto
ms.author: collw
author: dan-wesley
manager: srugh
ms.date: 04/30/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Microsoft Edge e downloads de conteúdo misto
ms.openlocfilehash: a81c44754865b2303320bfe87346c7f7533e6133
ms.sourcegitcommit: 4192328ee585bc32a9be528766b8a5a98e046c8e
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/25/2021
ms.locfileid: "11617301"
---
# <a name="learn-about-microsoft-edge-and-mixed-content-downloads"></a><span data-ttu-id="d0ae6-103">Saiba mais sobre o Microsoft Edge e downloads de conteúdo misto</span><span class="sxs-lookup"><span data-stu-id="d0ae6-103">Learn about Microsoft Edge and mixed content downloads</span></span>

<span data-ttu-id="d0ae6-104">Este artigo explica os downloads de conteúdo misto e como o Microsoft Edge lida com eles.</span><span class="sxs-lookup"><span data-stu-id="d0ae6-104">This article explains mixed content downloads and how Microsoft Edge handles them.</span></span>

>[!NOTE]
><span data-ttu-id="d0ae6-105">Este artigo se aplica ao Microsoft Edge versão 85 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="d0ae6-105">This article applies to Microsoft Edge version 85 or later.</span></span>

## <a name="what-are-mixed-content-downloads"></a><span data-ttu-id="d0ae6-106">O que são downloads de conteúdo misto?</span><span class="sxs-lookup"><span data-stu-id="d0ae6-106">What are mixed content downloads?</span></span>

<span data-ttu-id="d0ae6-107">Um download de conteúdo misto ocorre quando você inicia um download de uma página HTML carregada em uma conexão HTTPS segura, mas existe uma das seguintes condições:</span><span class="sxs-lookup"><span data-stu-id="d0ae6-107">A mixed content download happens when you start a download from an HTML page that was loaded over a secure HTTPS connection, but one of the following conditions exists:</span></span>

- <span data-ttu-id="d0ae6-108">Um ou mais redirecionamentos do local de download foram carregados em uma conexão HTTP insegura.</span><span class="sxs-lookup"><span data-stu-id="d0ae6-108">One or more of the download location's redirects was loaded over an insecure HTTP connection.</span></span>
- <span data-ttu-id="d0ae6-109">O local final do download foi carregado em uma conexão HTTP insegura.</span><span class="sxs-lookup"><span data-stu-id="d0ae6-109">The final download location was loaded over an insecure HTTP connection.</span></span>

<span data-ttu-id="d0ae6-110">Qualquer cenário é um conteúdo misto, porque a solicitação foi feita usando HTTPS seguro e tanto o conteúdo HTTP como o HTTPS estão envolvidos na obtenção do destino final do download.</span><span class="sxs-lookup"><span data-stu-id="d0ae6-110">Either scenario is a mixed content because the request was made using secure HTTPS and both HTTP and HTTPS content are involved in reaching the final download destination.</span></span> <span data-ttu-id="d0ae6-111">Navegadores modernos exibem avisos sobre esse tipo de conteúdo para indicar ao usuário que esse download pode ser transferido sem segurança, mesmo que a página original acessada seja segura.</span><span class="sxs-lookup"><span data-stu-id="d0ae6-111">Modern browsers display warnings about this type of content to indicate to the user that this download may be transferred insecurely even though the original page accessed was secure.</span></span>

## <a name="download-warnings-and-user-options"></a><span data-ttu-id="d0ae6-112">Baixar avisos e opções de usuário</span><span class="sxs-lookup"><span data-stu-id="d0ae6-112">Download warnings and user options</span></span>

<span data-ttu-id="d0ae6-113">O aviso de download garante que os usuários saibam que o arquivo que estão baixando pode ser lido por invasores mal-intencionados em sua rede.</span><span class="sxs-lookup"><span data-stu-id="d0ae6-113">The download warning ensures that users know that the file they're downloading could be read by malicious attackers on their network.</span></span> <span data-ttu-id="d0ae6-114">Esse aviso permite que um usuário tome uma decisão informada sobre se deseja baixar o arquivo.</span><span class="sxs-lookup"><span data-stu-id="d0ae6-114">This warning lets a user make an informed decision on whether to download the file.</span></span>

<span data-ttu-id="d0ae6-115">No Microsoft Edge, os downloads de conteúdo misto serão bloqueados, mas os usuários poderão ignorar e baixar o arquivo se desejarem.</span><span class="sxs-lookup"><span data-stu-id="d0ae6-115">In Microsoft Edge, mixed content downloads will be blocked but users can override and download the file if they want to.</span></span> <span data-ttu-id="d0ae6-116">O Microsoft Edge planeja começar a bloquear downloads de arquivos de conteúdo misto executáveis, começando com o Microsoft Edge versão 85, e bloqueará diferentes tipos de arquivos em versões futuras.</span><span class="sxs-lookup"><span data-stu-id="d0ae6-116">Microsoft Edge plans on starting to block mixed content executable file downloads starting with Microsoft Edge version 85 and will block different filetypes in future releases.</span></span>

> [!NOTE]
> <span data-ttu-id="d0ae6-117">A implantação desse recurso está sujeita a alterações com base na programação de lançamentos e nos comentários dos usuários.</span><span class="sxs-lookup"><span data-stu-id="d0ae6-117">Deployment of this feature is subject to change based on release schedule and user feedback.</span></span>

<!-- The schedule of the block for different filetypes is to be determined and may be impacted by usage data and user feedback. -->

<span data-ttu-id="d0ae6-118">Na prateleira de downloads, a mensagem de aviso de bloqueio se parece com o exemplo na próxima captura de tela.</span><span class="sxs-lookup"><span data-stu-id="d0ae6-118">In the download shelf, the block warning message looks like the example in the next screenshot.</span></span>

 ![Aviso de conteúdo misto na bandeja de downloads](./media/edge-learnmore-mixed-content-downloads/edge-mixed-content-download-tray-warning.png)

<span data-ttu-id="d0ae6-120">Na página de download, o aviso de bloqueio é semelhante ao seguinte exemplo de captura de tela:</span><span class="sxs-lookup"><span data-stu-id="d0ae6-120">On the download page, the block warning looks like the following screenshot example:</span></span>

 ![Aviso de substituição de conteúdo misto](./media/edge-learnmore-mixed-content-downloads/edge-mixed-content-download-page-warning.png)

<span data-ttu-id="d0ae6-122">Se um usuário decidir manter o download, ele será solicitado a confirmar sua ação.</span><span class="sxs-lookup"><span data-stu-id="d0ae6-122">If a user decides to keep the download, they are prompted to confirm their action.</span></span> <span data-ttu-id="d0ae6-123">A próxima captura de tela mostra um exemplo desse prompt de confirmação.</span><span class="sxs-lookup"><span data-stu-id="d0ae6-123">The next screenshot shows an example of this confirmation prompt.</span></span>

 ![Escolha o modo Internet Explorer](./media/edge-learnmore-mixed-content-downloads/edge-mixed-content-download-override.png)

## <a name="supporting-policies"></a><span data-ttu-id="d0ae6-125">Políticas de apoio</span><span class="sxs-lookup"><span data-stu-id="d0ae6-125">Supporting policies</span></span>

<span data-ttu-id="d0ae6-126">As empresas que desejem excluir o bloqueio de conteúdo misto de sites específicos podem usar a política [InsecureContentAllowedForUrls](./microsoft-edge-policies.md#insecurecontentallowedforurls) para fazer isso.</span><span class="sxs-lookup"><span data-stu-id="d0ae6-126">Enterprises that want to exclude mixed content blocking from specific websites can use the [InsecureContentAllowedForUrls](./microsoft-edge-policies.md#insecurecontentallowedforurls) policy to do so.</span></span>

## <a name="content-license"></a><span data-ttu-id="d0ae6-127">Licença de conteúdo</span><span class="sxs-lookup"><span data-stu-id="d0ae6-127">Content license</span></span>

> [!NOTE]
> <span data-ttu-id="d0ae6-128">Partes desta página são modificações baseadas no trabalho criado e compartilhado pela Chromium.org e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional](http://creativecommons.org/licenses/by/4.0/).</span><span class="sxs-lookup"><span data-stu-id="d0ae6-128">Portions of this page are modifications based on work created and shared by Chromium.org and used according to terms described in the [Creative Commons Attribution 4.0 International License](http://creativecommons.org/licenses/by/4.0/).</span></span> <span data-ttu-id="d0ae6-129">A página original pode ser encontrada [aqui](https://developers.google.com/web/fundamentals/security/prevent-mixed-content/what-is-mixed-content).</span><span class="sxs-lookup"><span data-stu-id="d0ae6-129">The original page can be found [here](https://developers.google.com/web/fundamentals/security/prevent-mixed-content/what-is-mixed-content).</span></span>
  
<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br /><span data-ttu-id="d0ae6-130">Esse trabalho é licenciado sob uma <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons</a>.</span><span class="sxs-lookup"><span data-stu-id="d0ae6-130">This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.</span></span>

## <a name="see-also"></a><span data-ttu-id="d0ae6-131">Consulte também</span><span class="sxs-lookup"><span data-stu-id="d0ae6-131">See also</span></span>

- [<span data-ttu-id="d0ae6-132">Página de aterrissagem do Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="d0ae6-132">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)