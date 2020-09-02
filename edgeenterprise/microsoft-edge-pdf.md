---
title: Leitor de PDF no Microsoft Edge
ms.author: adigan
author: dan-wesley
manager: balajek
ms.date: 08/05/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Saiba mais sobre o leitor de PDF no Microsoft Edge.
ms.openlocfilehash: c189bc08d4af0c9d5c4d9c573e0b5b7ef32a7fb3
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979143"
---
# <span data-ttu-id="3204d-103">Leitor de PDF no Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="3204d-103">PDF reader in Microsoft Edge</span></span>

<span data-ttu-id="3204d-104">Os arquivos em PDF representam uma parte significativa do nosso cotidiano.</span><span class="sxs-lookup"><span data-stu-id="3204d-104">PDF files make up a substantial part of our day-to-day lives.</span></span> <span data-ttu-id="3204d-105">Eles estão disponíveis sob a forma de contratos e acordos, boletins informativos, formulários, artigos de pesquisa, currículos, etc.</span><span class="sxs-lookup"><span data-stu-id="3204d-105">They come in the form of contracts and agreements, newsletters, forms, research articles, resumes, and so on.</span></span> <span data-ttu-id="3204d-106">Esses arquivos destacam a necessidade de um leitor de PDF confiável, seguro e eficiente que possa ser adotado pelas empresas.</span><span class="sxs-lookup"><span data-stu-id="3204d-106">These files highlight the need for a reliable, secure, and powerful PDF reader that can be adopted by Enterprises.</span></span>

<span data-ttu-id="3204d-107">O Microsoft Edge acompanha um leitor de PDF interno que permite que você abra os arquivos PDF locais, arquivos PDF on-line ou arquivos PDF inseridos nas páginas da Web.</span><span class="sxs-lookup"><span data-stu-id="3204d-107">Microsoft Edge comes with a built-in PDF reader that lets you open your local pdf files, online pdf files, or pdf files embedded in web pages.</span></span> <span data-ttu-id="3204d-108">Você pode fazer anotações nesses arquivos com tinta e destaque.</span><span class="sxs-lookup"><span data-stu-id="3204d-108">You can annotate these files with ink and highlighting.</span></span> <span data-ttu-id="3204d-109">Esse leitor de PDF oferece aos usuários uma única aplicação para atender às necessidades da página Web e do documento PDF.</span><span class="sxs-lookup"><span data-stu-id="3204d-109">This PDF reader gives users a single application to meet web page and PDF document needs.</span></span> <span data-ttu-id="3204d-110">O leitor de PDF do Microsoft Edge é uma aplicação segura e confiável que funciona em todas as plataformas de área de trabalho do Windows e do MacOS.</span><span class="sxs-lookup"><span data-stu-id="3204d-110">The Microsoft Edge PDF reader is a secure and reliable application that works across the Windows and macOS desktop platforms.</span></span>

> [!NOTE]
> <span data-ttu-id="3204d-111">Este artigo se aplica ao Microsoft Edge versão 77 ou posteriores.</span><span class="sxs-lookup"><span data-stu-id="3204d-111">This article applies to Microsoft Edge version 77 or later.</span></span>

## <span data-ttu-id="3204d-112">Pré-requisitos, suporte e restrições</span><span class="sxs-lookup"><span data-stu-id="3204d-112">Prerequisites, support, and constraints</span></span>

<span data-ttu-id="3204d-113">A tabela a seguir mostra quais canais e versões do Microsoft Edge oferecem suporte a cada recurso do leitor de PDF.</span><span class="sxs-lookup"><span data-stu-id="3204d-113">The following table shows which channels and versions of Microsoft Edge support each PDF reader feature.</span></span>

| <span data-ttu-id="3204d-114">Recurso</span><span class="sxs-lookup"><span data-stu-id="3204d-114">Feature</span></span> | <span data-ttu-id="3204d-115">Versão de canal estável</span><span class="sxs-lookup"><span data-stu-id="3204d-115">Stable channel version</span></span> |
|---------|------------------------|
| <span data-ttu-id="3204d-116">Exibir e imprimir arquivos PDF locais, on-line e incorporados</span><span class="sxs-lookup"><span data-stu-id="3204d-116">View and print local, online, and embedded PDF files</span></span> | <span data-ttu-id="3204d-117">79.0.309.71</span><span class="sxs-lookup"><span data-stu-id="3204d-117">79.0.309.71</span></span>                |
| <span data-ttu-id="3204d-118">Preenchimento do formulário básico</span><span class="sxs-lookup"><span data-stu-id="3204d-118">Basic form filling</span></span><br><span data-ttu-id="3204d-119">(Os formulários JavaScript não possuem suporte)</span><span class="sxs-lookup"><span data-stu-id="3204d-119">(JavaScript forms aren't supported)</span></span> | <span data-ttu-id="3204d-120">79.0.309.71</span><span class="sxs-lookup"><span data-stu-id="3204d-120">79.0.309.71</span></span>           |
| <span data-ttu-id="3204d-121">Escrita à tinta</span><span class="sxs-lookup"><span data-stu-id="3204d-121">Inking</span></span>  | <span data-ttu-id="3204d-122">80.0.361.48</span><span class="sxs-lookup"><span data-stu-id="3204d-122">80.0.361.48</span></span>            |
| <span data-ttu-id="3204d-123">Personalização de tinta</span><span class="sxs-lookup"><span data-stu-id="3204d-123">Ink customization</span></span> | <span data-ttu-id="3204d-124">83.0.478.54</span><span class="sxs-lookup"><span data-stu-id="3204d-124">83.0.478.54</span></span>  |
| <span data-ttu-id="3204d-125">Highlight</span><span class="sxs-lookup"><span data-stu-id="3204d-125">Highlight</span></span>  | <span data-ttu-id="3204d-126">81.0.416.53.</span><span class="sxs-lookup"><span data-stu-id="3204d-126">81.0.416.53</span></span>         |
| <span data-ttu-id="3204d-127">Ler em voz alta</span><span class="sxs-lookup"><span data-stu-id="3204d-127">Read Aloud</span></span> | <span data-ttu-id="3204d-128">Sendo promovido agora nos canais [Microsoft Edge Insider](https://www.microsoftedgeinsider.com/)</span><span class="sxs-lookup"><span data-stu-id="3204d-128">Currently being promoted in [Microsoft Edge Insider](https://www.microsoftedgeinsider.com/) channels</span></span> |
| <span data-ttu-id="3204d-129">Visualizar arquivos MIP protegidos</span><span class="sxs-lookup"><span data-stu-id="3204d-129">View MIP protected files</span></span> | <span data-ttu-id="3204d-130">Suporte ao Windows na versão 80.0.361.48</span><span class="sxs-lookup"><span data-stu-id="3204d-130">Windows support in 80.0.361.48</span></span><br><span data-ttu-id="3204d-131">Suporte ao Mac na versão 81.0.416.53</span><span class="sxs-lookup"><span data-stu-id="3204d-131">Mac support in 81.0.416.53</span></span> |
|  <span data-ttu-id="3204d-132">Visualizar arquivos IRM protegidos</span><span class="sxs-lookup"><span data-stu-id="3204d-132">View IRM protected files</span></span>  | <span data-ttu-id="3204d-133">83.0.478.37</span><span class="sxs-lookup"><span data-stu-id="3204d-133">83.0.478.37</span></span>            |

### <span data-ttu-id="3204d-134">Restrições</span><span class="sxs-lookup"><span data-stu-id="3204d-134">Constraints</span></span>

<span data-ttu-id="3204d-135">Observe as seguintes restrições para o leitor de PDF atual:</span><span class="sxs-lookup"><span data-stu-id="3204d-135">Note the following constraints for the current PDF reader:</span></span>

-  <span data-ttu-id="3204d-136">A Arquitetura de formulários XML (XFA)é um formato herdado de formulários que não possui suporte no Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="3204d-136">XML Forms Architecture (XFA), is a legacy format of forms that isn't  supported in Microsoft Edge.</span></span>
-  <span data-ttu-id="3204d-137">A documentação relacionada com cenários de Acessibilidade que atualmente não possuem suporte pode ser encontrada no blog [Relatório de conformidade de acessibilidade da Microsoft](https://cloudblogs.microsoft.com/industry-blog/government/2018/09/11/accessibility-conformance-reports/).</span><span class="sxs-lookup"><span data-stu-id="3204d-137">Documentation related to Accessibility scenarios that currently aren't supported can be found on the [Microsoft Accessibility Conformance Reports](https://cloudblogs.microsoft.com/industry-blog/government/2018/09/11/accessibility-conformance-reports/) blog.</span></span>

## <span data-ttu-id="3204d-138">Recursos</span><span class="sxs-lookup"><span data-stu-id="3204d-138">Features</span></span>

### <span data-ttu-id="3204d-139">Escrita à tinta</span><span class="sxs-lookup"><span data-stu-id="3204d-139">Inking</span></span>

<span data-ttu-id="3204d-140">A escrita à tinta nos arquivos em PDF é útil para criar anotações rápidas para facilitar a consulta, o sinal ou o preenchimento de formulários em PDF.</span><span class="sxs-lookup"><span data-stu-id="3204d-140">Inking on PDF files comes in handy to take quick notes for easy reference, sign, or fill out PDF forms.</span></span> <span data-ttu-id="3204d-141">Esse recurso já está disponível no Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="3204d-141">This capability is now available in Microsoft Edge.</span></span> <span data-ttu-id="3204d-142">Além de arquivos em PDF de escrita à tinta, conforme necessário, você pode usar a cor e a largura do traçado para dar atenção às diferentes partes do arquivo em PDF.</span><span class="sxs-lookup"><span data-stu-id="3204d-142">In addition to inking PDF files as needed, you can use color and stroke width to bring attention to different parts of the PDF file.</span></span> <span data-ttu-id="3204d-143">A próxima captura de tela mostra como um usuário pode adicionar escrita à tinta em uma página em PDF.</span><span class="sxs-lookup"><span data-stu-id="3204d-143">The next screenshot shows how a user can add inking to a pdf page.</span></span>

<!-- SCREENSHOT -->
![Página Adicionar escrita à tinta em PDF](media/microsoft-edge-pdf/pdf-reader-inking.png)

### <span data-ttu-id="3204d-145">Highlight</span><span class="sxs-lookup"><span data-stu-id="3204d-145">Highlight</span></span>

<span data-ttu-id="3204d-146">O leitor de PDF no Microsoft Edge é fornecido com o suporte para adicionar e editar destaques.</span><span class="sxs-lookup"><span data-stu-id="3204d-146">PDF reader in Microsoft Edge comes with support for adding and editing highlights.</span></span> <span data-ttu-id="3204d-147">Para criar um destaque, o usuário só precisa selecionar o texto, clicar com o botão direito nele, selecionar destaques no menu e escolher a cor desejada.</span><span class="sxs-lookup"><span data-stu-id="3204d-147">To create a highlight, the user simply needs to select the text, right-click on it, select highlights in the menu and choose the desired color.</span></span> <span data-ttu-id="3204d-148">A próxima captura de tela mostra as opções de destaque disponíveis.</span><span class="sxs-lookup"><span data-stu-id="3204d-148">The next screenshot shows the highlight options that are available.</span></span>

![Usar a opção destacar no leitor de PDF](media/microsoft-edge-pdf/pdf-reader-highlight.png)

### <span data-ttu-id="3204d-150">Ler em voz alta</span><span class="sxs-lookup"><span data-stu-id="3204d-150">Read Aloud</span></span>

<span data-ttu-id="3204d-151">O recurso Ler em Voz alta do PDF permite que os usuários ouçam ao conteúdo em PDF enquanto realizam outras tarefas que podem ser importantes para eles.</span><span class="sxs-lookup"><span data-stu-id="3204d-151">Read Aloud for PDF adds the convenience of listening to PDF content while carrying out other tasks that may be important to users.</span></span> <span data-ttu-id="3204d-152">Ele também ajuda os alunos de auditoria a se concentrarem no conteúdo, o que facilita o aprendizado.</span><span class="sxs-lookup"><span data-stu-id="3204d-152">It also helps auditory learners focus on the content, which makes learning much easier.</span></span> <span data-ttu-id="3204d-153">A próxima captura de tela mostra um exemplo lido em voz alta.</span><span class="sxs-lookup"><span data-stu-id="3204d-153">The next screenshot shows a Read Aloud example.</span></span> <span data-ttu-id="3204d-154">O destaque mostra o texto que está sendo lido no momento.</span><span class="sxs-lookup"><span data-stu-id="3204d-154">The highlighting shows the text that is currently being read.</span></span>

![Usar a opção destacar no leitor de PDF](media/microsoft-edge-pdf/pdf-reader-read-aloud-example.png)

### <span data-ttu-id="3204d-156">PDFs protegidos</span><span class="sxs-lookup"><span data-stu-id="3204d-156">Protected PDFs</span></span>

<span data-ttu-id="3204d-157">A [Proteção de informações da Microsoft (MIP)](https://docs.microsoft.com/microsoft-365/compliance/protect-information?view=o365-worldwide) permite que os usuários colaborem com outras pessoas de maneira segura enquanto aderem às políticas de conformidade da sua organização.</span><span class="sxs-lookup"><span data-stu-id="3204d-157">[Microsoft Information Protection (MIP)](https://docs.microsoft.com/microsoft-365/compliance/protect-information?view=o365-worldwide) enables users to collaborate with others securely, while adhering to your organization's compliance policies.</span></span> <span data-ttu-id="3204d-158">Depois que um arquivo é protegido, as ações que os usuários podem realizar são determinadas pelas permissões que lhes são atribuídas.</span><span class="sxs-lookup"><span data-stu-id="3204d-158">After a file is protected, the actions users can take on it are determined by the permissions assigned to them.</span></span>

<span data-ttu-id="3204d-159">Esses arquivos podem ser abertos diretamente no navegador sem precisar baixar qualquer outro software ou instalar um suplemento.</span><span class="sxs-lookup"><span data-stu-id="3204d-159">These files can be opened directly in the browser, without the need to download any other software, or install any add-in.</span></span> <span data-ttu-id="3204d-160">Isso integra a segurança fornecida pelo MIP diretamente no navegador, proporcionando um fluxo de trabalho contínuo.</span><span class="sxs-lookup"><span data-stu-id="3204d-160">This integrates the security provided by MIP directly into the browser, providing a seamless workflow.</span></span>

<!-- SCREENSHOT -->
![Documento em PDF protegido.](media/microsoft-edge-pdf/pdf-reader-protected-pdf2.png)

<span data-ttu-id="3204d-162">Além dos arquivos protegidos pelo MIP, os arquivos em [PDF em Gerenciamento de direitos de informação (IRM)](https://docs.microsoft.com/microsoft-365/compliance/set-up-irm-in-sp-admin-center?view=o365-worldwide) protegidos por bibliotecas do SharePoint também podem ser abertos originalmente no navegador.</span><span class="sxs-lookup"><span data-stu-id="3204d-162">In addition to MIP protected files, PDF files in [Information Rights Management (IRM)](https://docs.microsoft.com/microsoft-365/compliance/set-up-irm-in-sp-admin-center?view=o365-worldwide) protected SharePoint libraries can also be opened natively in the browser.</span></span>

<span data-ttu-id="3204d-163">Com o Microsoft Edge, os usuários podem visualizar os arquivos MIP protegidos localmente, ou na nuvem.</span><span class="sxs-lookup"><span data-stu-id="3204d-163">With Microsoft Edge, users can view MIP protected files saved locally, or in the cloud.</span></span> <span data-ttu-id="3204d-164">Se for salvo localmente, o arquivo pode ser aberto diretamente no navegador.</span><span class="sxs-lookup"><span data-stu-id="3204d-164">If saved locally, the file can be opened directly in the browser.</span></span> <span data-ttu-id="3204d-165">Se o arquivo for aberto de um serviço de nuvem como o SharePoint, talvez o usuário precise usar a opção "Abrir no navegador".</span><span class="sxs-lookup"><span data-stu-id="3204d-165">If the file is opened from a cloud service as SharePoint, the user may need to use the "Open in browser" option.</span></span>

<span data-ttu-id="3204d-166">Se o perfil com o qual o usuário se conectou no Microsoft Edge tiver pelo menos permissões de visualização do arquivo, o arquivo será aberto no Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="3204d-166">If the profile that the user is logged into Microsoft Edge with has at least view permissions to the file, the file will open in Microsoft Edge.</span></span>

<!-- SCREENSHOT -->
![Aviso para salvar a página de PDF do SharePoint é protegido pelo MIP](media/microsoft-edge-pdf/pdf-reader-sharepoint-irm.png)

## <span data-ttu-id="3204d-168">Acessibilidade</span><span class="sxs-lookup"><span data-stu-id="3204d-168">Accessibility</span></span>

<span data-ttu-id="3204d-169">O leitor de PDF é fornecido com suporte à acessibilidade do teclado, modo de alto contraste e suporte ao leitor de tela através de dispositivos Windows e MacOS.</span><span class="sxs-lookup"><span data-stu-id="3204d-169">The PDF reader comes with support for Keyboard accessibility, High contrast mode, and screen reader support across Windows and macOS devices.</span></span>

### <span data-ttu-id="3204d-170">Acessibilidade do teclado</span><span class="sxs-lookup"><span data-stu-id="3204d-170">Keyboard Accessibility</span></span>

<span data-ttu-id="3204d-171">Os usuários podem usar a navegação para diferentes partes do documento com as quais um usuário pode interagir, como campos de formulário e destaques, usando o teclado.</span><span class="sxs-lookup"><span data-stu-id="3204d-171">Users can use navigate to different parts of the document that a user can interact with, such as form fields and highlights, using the keyboard.</span></span>

<!-- SCREENSHOT -->

### <span data-ttu-id="3204d-172">Modo de alto contraste</span><span class="sxs-lookup"><span data-stu-id="3204d-172">High contrast mode</span></span>

<span data-ttu-id="3204d-173">O leitor de PDF usará as configurações definidas no nível do sistema operacional para renderizar o conteúdo em PDF no modo de alto contraste.</span><span class="sxs-lookup"><span data-stu-id="3204d-173">PDF reader will use the settings defined at the operating system level to render PDF content in high contrast mode.</span></span>

<!-- SCREENSHOT -->
<!--![High contrast mode for pdf file](media/microsoft-edge-pdf/pdf-reader-high-contrast.png)-->

### <span data-ttu-id="3204d-174">Suporte do leitor de tela</span><span class="sxs-lookup"><span data-stu-id="3204d-174">Screen reader support</span></span>

<span data-ttu-id="3204d-175">Os usuários podem navegar e ler arquivos em PDF usando os leitores de tela em computadores com Windows e Mac.</span><span class="sxs-lookup"><span data-stu-id="3204d-175">Users can navigate through and read PDF files using screen readers on Windows and Mac computers.</span></span> <!--The next screenshot shows the toolbar that users can use for audio settings when they're using the Read Aloud option in PDF reader. -->

<!-- SCREENSHOT -->
<!--
![Screen reader toolbar](media/microsoft-edge-pdf/pdf-reader-read-aloud.png) -->

## <span data-ttu-id="3204d-176">Segurança e confiabilidade</span><span class="sxs-lookup"><span data-stu-id="3204d-176">Security and reliability</span></span>

<span data-ttu-id="3204d-177">A segurança está entre os princípios mais importantes de qualquer organização.</span><span class="sxs-lookup"><span data-stu-id="3204d-177">Security is among the most important tenets for any organization.</span></span> <span data-ttu-id="3204d-178">A segurança do leitor de PDF é uma parte integrante do projeto de segurança do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="3204d-178">PDF reader security is an integral part of the Microsoft Edge security design.</span></span> <span data-ttu-id="3204d-179">Dois dos recursos de segurança mais importantes de uma perspectiva do leitor de PDF são o isolamento do processo e o Microsoft Defender Application Guard (Application Guard).</span><span class="sxs-lookup"><span data-stu-id="3204d-179">Two of the most important security features From a PDF reader perspective, two important security features are process isolation and Microsoft Defender Application Guard (Application Guard).</span></span>

- <span data-ttu-id="3204d-180">Isolamento do processo.</span><span class="sxs-lookup"><span data-stu-id="3204d-180">Process isolation.</span></span> <span data-ttu-id="3204d-181">Os PDFs abertos de diferentes sites são totalmente isolados.</span><span class="sxs-lookup"><span data-stu-id="3204d-181">PDFs opened from different web sites are completely process isolated.</span></span> <span data-ttu-id="3204d-182">O navegador não precisa se comunicar com nenhum website, nem com arquivos em PDF abertos de outra fonte.</span><span class="sxs-lookup"><span data-stu-id="3204d-182">The browser doesn't have to communicate with any websites, or PDF files opened from another source.</span></span> <span data-ttu-id="3204d-183">A navegação em PDF é segura contra qualquer ataque que pretenda utilizar PDFs comprometidos como superfície de ataque.</span><span class="sxs-lookup"><span data-stu-id="3204d-183">PDF browsing is secure from any attacks that plan to use compromised PDFs as an attack surface.</span></span>

- <span data-ttu-id="3204d-184">Application Guard.</span><span class="sxs-lookup"><span data-stu-id="3204d-184">Application Guard.</span></span> <span data-ttu-id="3204d-185">Com o Application Guard, os administradores podem configurar uma lista de sites que sua organização confia.</span><span class="sxs-lookup"><span data-stu-id="3204d-185">With Application Guard, admins can set a list of sites that are trusted by their organization.</span></span> <span data-ttu-id="3204d-186">Se os usuários abrirem quaisquer outros sites, eles serão abertos em uma janela separada do Application Guard que funciona no seu próprio contêiner.</span><span class="sxs-lookup"><span data-stu-id="3204d-186">If users open any other sites, they are opened in a separate Application Guard window that runs in its own container.</span></span> <span data-ttu-id="3204d-187">O contêiner ajuda a proteger a rede corporativa e quaisquer dados no computador do usuário de serem comprometidos.</span><span class="sxs-lookup"><span data-stu-id="3204d-187">The container helps protect the corporate network and any data on user's computer from being compromised.</span></span><br><br>
<span data-ttu-id="3204d-188">Essa proteção também se aplica a qualquer arquivo PDF on-line que seja visualizado.</span><span class="sxs-lookup"><span data-stu-id="3204d-188">This protection also applies to any online PDF files that are viewed.</span></span> <span data-ttu-id="3204d-189">Além disso, quaisquer arquivos PDF que forem baixados de uma janela do Application Guard são armazenados e, quando necessário, reabertos no contêiner.</span><span class="sxs-lookup"><span data-stu-id="3204d-189">Further, any PDF files that are downloaded from an Application Guard window are stored, and when needed, re-opened in the container.</span></span> <span data-ttu-id="3204d-190">Isso ajuda a manter seu ambiente seguro não apenas quando o arquivo é baixado, mas durante todo o seu ciclo de vida.</span><span class="sxs-lookup"><span data-stu-id="3204d-190">This helps keeps your environment secure not just when the file is downloaded, but through its whole lifecycle.</span></span> <span data-ttu-id="3204d-191">Para obter mais informações, consulte [Application Guard](https://docs.microsoft.com/DeployEdge/microsoft-edge-security-windows-defender-application-guard).</span><span class="sxs-lookup"><span data-stu-id="3204d-191">For more information, see [Application Guard](https://docs.microsoft.com/DeployEdge/microsoft-edge-security-windows-defender-application-guard).</span></span>

### <span data-ttu-id="3204d-192">Confiabilidade</span><span class="sxs-lookup"><span data-stu-id="3204d-192">Reliability</span></span>

<span data-ttu-id="3204d-193">Uma vez que o Microsoft Edge é baseado no Chromium, os usuários podem esperar pelo mesmo nível de confiabilidade que estão acostumados a ver no Google Chrome.</span><span class="sxs-lookup"><span data-stu-id="3204d-193">Because Microsoft Edge is Chromium-based, users can expect the same level of reliability that they're used to seeing in Google Chrome.</span></span>

## <span data-ttu-id="3204d-194">Implantar e atualizar o leitor de PDF</span><span class="sxs-lookup"><span data-stu-id="3204d-194">Deploy and update PDF reader</span></span>

<span data-ttu-id="3204d-195">O leitor de PDF é instalado e atualizado com o restante do navegador Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="3204d-195">The PDF reader gets deployed and updated with the rest of the Microsoft Edge browser.</span></span> <span data-ttu-id="3204d-196">Para saber mais sobre como implantar o Microsoft Edge, assista ao vídeo [Implantar o Microsoft Edge para centenas ou milhares de dispositivos](microsoft-edge-video-deploy.md).</span><span class="sxs-lookup"><span data-stu-id="3204d-196">To learn more about deploying Microsoft Edge, watch the [Deploy Microsoft Edge to hundreds or thousands of devices](microsoft-edge-video-deploy.md) video.</span></span> <span data-ttu-id="3204d-197">Você também pode encontrar mais informações sobre a implantação na página inicial da [documentação do Microsoft Edge](https://docs.microsoft.com/DeployEdge/).</span><span class="sxs-lookup"><span data-stu-id="3204d-197">You can also find more deployment information on the [Microsoft Edge documentation](https://docs.microsoft.com/DeployEdge/) landing page.</span></span>

> [!TIP]
> <span data-ttu-id="3204d-198">Você pode tornar o Microsoft Edge o leitor de PDF padrão da sua organização.</span><span class="sxs-lookup"><span data-stu-id="3204d-198">You can make Microsoft Edge the default PDF reader for your organization.</span></span> <span data-ttu-id="3204d-199">Para fazer isso, [siga estas etapas](https://docs.microsoft.com/deployedge/edge-default-browser).</span><span class="sxs-lookup"><span data-stu-id="3204d-199">To do this, [follow these steps](https://docs.microsoft.com/deployedge/edge-default-browser).</span></span>

## <span data-ttu-id="3204d-200">Roteiro e comentários</span><span class="sxs-lookup"><span data-stu-id="3204d-200">Roadmap and feedback</span></span>

<span data-ttu-id="3204d-201">O roteiro do leitor de PDF no Microsoft Edge está disponível [aqui](https://techcommunity.microsoft.com/t5/articles/roadmap-for-pdf-reader-in-microsoft-edge/m-p/1467667).</span><span class="sxs-lookup"><span data-stu-id="3204d-201">The roadmap for PDF Reader in Microsoft Edge is available [here](https://techcommunity.microsoft.com/t5/articles/roadmap-for-pdf-reader-in-microsoft-edge/m-p/1467667).</span></span>

<span data-ttu-id="3204d-202">Analisamos ativamente seus comentários sobre os recursos que você considera importantes.</span><span class="sxs-lookup"><span data-stu-id="3204d-202">We're actively looking at feedback from you about the features you find important.</span></span> <span data-ttu-id="3204d-203">Sinta-se à vontade para nos enviar comentários pelo [Microsoft Edge UserVoice](https://microsoftedge.uservoice.com/) e no fórum [Microsoft Edge Insider](https://techcommunity.microsoft.com/t5/microsoft-edge-insider/ct-p/MicrosoftEdgeInsider).</span><span class="sxs-lookup"><span data-stu-id="3204d-203">Feel free to send us feedback through [Microsoft Edge UserVoice](https://microsoftedge.uservoice.com/) and on [Microsoft Edge Insider](https://techcommunity.microsoft.com/t5/microsoft-edge-insider/ct-p/MicrosoftEdgeInsider) forum.</span></span>

## <span data-ttu-id="3204d-204">Consulte também</span><span class="sxs-lookup"><span data-stu-id="3204d-204">See also</span></span>

- [<span data-ttu-id="3204d-205">Página de aterrissagem do Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="3204d-205">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)