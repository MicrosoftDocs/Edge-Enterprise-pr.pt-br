---
title: Configurações de privacidade do Microsoft Edge Enterprise
ms.author: likravit
author: dan-wesley
manager: srugh
ms.date: 05/26/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Definir as configurações de privacidade do Microsoft Edge Enterprise
ms.openlocfilehash: 2b7a33087ae5110c53d18b3192486d4ae62fa540
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979128"
---
# <span data-ttu-id="6605f-103">Configurar as políticas do Microsoft Edge para oferecer suporte à privacidade da empresa</span><span class="sxs-lookup"><span data-stu-id="6605f-103">Configure Microsoft Edge policies to support enterprise privacy</span></span>

<span data-ttu-id="6605f-104">A Microsoft está comprometida em fornecer às empresas as informações e os controles necessários para fazer escolhas sobre a coleta de dados no Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="6605f-104">Microsoft is committed to providing enterprises with the information and controls needed to make choices about data collection in Microsoft Edge.</span></span>

## <span data-ttu-id="6605f-105">Visão geral</span><span class="sxs-lookup"><span data-stu-id="6605f-105">Overview</span></span>

<span data-ttu-id="6605f-106">Por padrão, o Microsoft Edge implantado nas plataformas não Windows não envia dados de diagnóstico ou informações do site para a Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6605f-106">By default, Microsoft Edge deployed on non-Windows platforms doesn't send diagnostic data or site information to Microsoft.</span></span> <span data-ttu-id="6605f-107">Por padrão, quando o Microsoft Edge é implantado no Windows 10, os dados de diagnóstico são enviados com base na [Configuração de dados de diagnóstico do Windows](https://go.microsoft.com/fwlink/?linkid=2099569) dos usuários.</span><span class="sxs-lookup"><span data-stu-id="6605f-107">When Microsoft Edge is deployed on Windows 10, the default is to send diagnostic data based on the users' [Windows Diagnostic data setting](https://go.microsoft.com/fwlink/?linkid=2099569).</span></span>

<span data-ttu-id="6605f-108">Você pode configurar como o Microsoft Edge realiza a coleta de dados da sua organização com as seguintes políticas de grupo:</span><span class="sxs-lookup"><span data-stu-id="6605f-108">You can also configure how Microsoft Edge handles data collection for your organization with the following group policies:</span></span>

- <span data-ttu-id="6605f-109">[MetricsReportingEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#metricsreportingenabled) - habilita o uso e os relatórios de dados relacionados a falhas.</span><span class="sxs-lookup"><span data-stu-id="6605f-109">[MetricsReportingEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#metricsreportingenabled) - Enable usage and crash-related data reporting.</span></span>
- <span data-ttu-id="6605f-110">[SendSiteInfoToImproveServices](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sendsiteinfotoimproveservices) - envia informações do site para melhorar os serviços da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6605f-110">[SendSiteInfoToImproveServices](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sendsiteinfotoimproveservices) - Send site information to improve Microsoft services.</span></span>

## <span data-ttu-id="6605f-111">Definir configurações de política</span><span class="sxs-lookup"><span data-stu-id="6605f-111">Configure policy settings</span></span>

<span data-ttu-id="6605f-112">Antes começar, baixe e use o modelo de política do Microsoft Edge mais recente (para obter mais informações, consulte [Configurar o Microsoft Edge](configure-microsoft-edge.md)).</span><span class="sxs-lookup"><span data-stu-id="6605f-112">Before you begin, download and use the latest Microsoft Edge Policy Template (For more information, see [Configure Microsoft Edge](configure-microsoft-edge.md).)</span></span>

### <span data-ttu-id="6605f-113">Habilite a geração de relatórios de dados relacionados a falhas e uso</span><span class="sxs-lookup"><span data-stu-id="6605f-113">Enable usage and crash-related data reporting</span></span>

<span data-ttu-id="6605f-114">Esta política habilita a geração de relatórios de dados relacionados a falhas e uso do Microsoft Edge para a Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6605f-114">This policy enables reporting of usage and crash-related data about Microsoft Edge to Microsoft.</span></span>

<span data-ttu-id="6605f-115">O Microsoft Edge coleta um conjunto de dados que são necessários para manter o produto seguro, atualizado e funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="6605f-115">Microsoft Edge collects a set of required data that's necessary to keep the product up to date, secure, and performing properly.</span></span> <span data-ttu-id="6605f-116">Isso inclui informações básicas de conectividade e configuração do dispositivo do Microsoft Edge sobre o consentimento de coleta de dados atual, a versão do aplicativo e o estado da sua instalação do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="6605f-116">This data includes basic device connectivity and configuration information from Microsoft Edge about the current data collection consent, app version, and installation state about your installation of Microsoft Edge.</span></span><span data-ttu-id="6605f-117"> Esse conjunto de dados pode ser desativado desabilitando a política.</span><span class="sxs-lookup"><span data-stu-id="6605f-117"> This data collection can be turned off by disabling the policy.</span></span>

<span data-ttu-id="6605f-118">Habilite essa política para enviar relatórios de dados relacionados a falhas e uso para a Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6605f-118">Enable this policy to send reporting of usage and crash-related data to Microsoft.</span></span> <span data-ttu-id="6605f-119">Desabilite essa política para não enviar esses dados para a Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6605f-119">Disable this policy to not send the data to Microsoft.</span></span> <span data-ttu-id="6605f-120">Em ambos os casos, os usuários não poderão alterar nem substituir a configuração.</span><span class="sxs-lookup"><span data-stu-id="6605f-120">In both cases, users can't change or override the setting.</span></span>

<span data-ttu-id="6605f-121">Quando o Microsoft Edge estiver sendo executado no Windows 10:</span><span class="sxs-lookup"><span data-stu-id="6605f-121">When Microsoft Edge is running on Windows 10:</span></span>

- <span data-ttu-id="6605f-122">Se essa política não estiver configurada, o padrão do Microsoft Edge será a configuração de dados de diagnóstico do Windows.</span><span class="sxs-lookup"><span data-stu-id="6605f-122">If this policy isn't configured, Microsoft Edge will default to the Windows diagnostic data setting.</span></span>
- <span data-ttu-id="6605f-123">Se essa política estiver habilitada, o Microsoft Edge enviará dados de uso somente se a configuração de dados de diagnóstico do Windows estiver definida como **Avançada** ou **Completa**.</span><span class="sxs-lookup"><span data-stu-id="6605f-123">If this policy is enabled, Microsoft Edge will only send usage data if the Windows Diagnostic data setting is set to **Enhanced** or **Full**.</span></span>
- <span data-ttu-id="6605f-124">Se essa política estiver desabilitada, o Microsoft Edge não enviará dados de uso.</span><span class="sxs-lookup"><span data-stu-id="6605f-124">If this policy is disabled, Microsoft Edge will not send usage data.</span></span> <span data-ttu-id="6605f-125">Os dados relacionados a falha são enviados com base na configuração de dados de diagnóstico do Windows.</span><span class="sxs-lookup"><span data-stu-id="6605f-125">Crash-related data is sent based on the Windows Diagnostic data setting.</span></span> <span data-ttu-id="6605f-126">[Saiba mais sobre as configurações de Dados de diagnóstico do Windows:](https://go.microsoft.com/fwlink/?linkid=2099569).</span><span class="sxs-lookup"><span data-stu-id="6605f-126">[Learn more about Windows Diagnostic data settings](https://go.microsoft.com/fwlink/?linkid=2099569).</span></span>

<span data-ttu-id="6605f-127">Quando o Microsoft Edge estiver sendo executado no Windows 7, 8 e macOS:</span><span class="sxs-lookup"><span data-stu-id="6605f-127">When Microsoft Edge is running on Windows 7, 8, and macOS:</span></span>

- <span data-ttu-id="6605f-128">Se essa política não estiver configurada, o padrão do Microsoft Edge será a preferência do usuário.</span><span class="sxs-lookup"><span data-stu-id="6605f-128">If this policy isn't configured, Microsoft Edge will default to the user's preference.</span></span>

### <span data-ttu-id="6605f-129">Envie as informações de sites para melhorar os serviços Microsoft</span><span class="sxs-lookup"><span data-stu-id="6605f-129">Send site information to improve Microsoft services</span></span>

<span data-ttu-id="6605f-130">Essa política permite o envio de informações sobre sites visitados no Microsoft Edge para a Microsoft visando melhorar os produtos e serviços Microsoft, tais como a pesquisa.</span><span class="sxs-lookup"><span data-stu-id="6605f-130">This policy enables sending information about websites visited in Microsoft Edge to Microsoft to improve Microsoft products and services such as search.</span></span>

<span data-ttu-id="6605f-131">Habilite essa política para enviar informações sobre os sites visitados no Microsoft Edge para a Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6605f-131">Enable this policy to send information about websites visited in Microsoft Edge to Microsoft.</span></span> <span data-ttu-id="6605f-132">Desabilite essa política para não enviar informações sobre os sites visitados com o Microsoft Edge para a Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6605f-132">Disable this policy to not send information about the websites that are visited in Microsoft Edge to Microsoft.</span></span> <span data-ttu-id="6605f-133">Em ambos os casos, os usuários não poderão alterar nem substituir a configuração.</span><span class="sxs-lookup"><span data-stu-id="6605f-133">In both cases, users can't change or override the setting.</span></span>

<span data-ttu-id="6605f-134">Quando o Microsoft Edge estiver sendo executado no Windows 10:</span><span class="sxs-lookup"><span data-stu-id="6605f-134">When Microsoft Edge is running on Windows 10:</span></span>

- <span data-ttu-id="6605f-135">Se essa política não estiver configurada, o padrão do Microsoft Edge será a configuração de dados de diagnóstico do Windows.</span><span class="sxs-lookup"><span data-stu-id="6605f-135">If this policy isn't configured, Microsoft Edge will default to the Windows diagnostic data setting.</span></span>
- <span data-ttu-id="6605f-136">Se essa política estiver habilitada, o Microsoft Edge enviará informações dos sites visitados apenas se a configuração de dados de diagnóstico do Windows estiver definida como **Completa**.</span><span class="sxs-lookup"><span data-stu-id="6605f-136">If this policy is enabled, Microsoft Edge will only send information about the websites that are visited if the Windows Diagnostic data setting is set to **Full**.</span></span>
- <span data-ttu-id="6605f-137">Se essa política estiver desabilitada, o Microsoft Edge não enviará informações dos sites visitados.</span><span class="sxs-lookup"><span data-stu-id="6605f-137">If this policy is disabled, Microsoft Edge will not send info about websites visited.</span></span> <span data-ttu-id="6605f-138">Para [saber mais sobre as configurações de dados de diagnóstico do Windows](https://go.microsoft.com/fwlink/?linkid=2099569).</span><span class="sxs-lookup"><span data-stu-id="6605f-138">To [learn more about Windows Diagnostic data settings](https://go.microsoft.com/fwlink/?linkid=2099569).</span></span>

<span data-ttu-id="6605f-139">Quando o Microsoft Edge estiver sendo executado no Windows 7, 8 e macOS:</span><span class="sxs-lookup"><span data-stu-id="6605f-139">When Microsoft Edge is running on Windows 7, 8, and macOS:</span></span>

- <span data-ttu-id="6605f-140">Se essa política não estiver configurada, o padrão do Microsoft Edge será a preferência do usuário.</span><span class="sxs-lookup"><span data-stu-id="6605f-140">If this policy isn't configured, Microsoft Edge will default to the user's preference.</span></span>

## <span data-ttu-id="6605f-141">Detalhes da implementação</span><span class="sxs-lookup"><span data-stu-id="6605f-141">Implementation details</span></span>

<span data-ttu-id="6605f-142">Para que os canais do Windows 10 entendam nossa implementação com a dependência da configuração de dados de diagnóstico do Windows, a tabela a seguir descreve nossa configuração se **Habilitar relatórios de uso e dados relacionados a falhas** e **Enviar informações do site para melhorar os serviços Microsoft** não estiverem configurados.</span><span class="sxs-lookup"><span data-stu-id="6605f-142">For Windows 10 to understand our implementation with the dependency on the Windows Diagnostic data setting, the following table describes our configuration if **Enable usage and crash-related data reporting** and **Send site information to improve Microsoft services** were not configured.</span></span>

| <span data-ttu-id="6605f-143">Configuração de dados de diagnóstico do Windows</span><span class="sxs-lookup"><span data-stu-id="6605f-143">Windows Diagnostic data setting</span></span> | <span data-ttu-id="6605f-144">Habilite a geração de relatórios de dados relacionados a falhas e uso</span><span class="sxs-lookup"><span data-stu-id="6605f-144">Enable usage and crash-related data reporting</span></span> | <span data-ttu-id="6605f-145">Envie as informações de sites para melhorar os serviços Microsoft</span><span class="sxs-lookup"><span data-stu-id="6605f-145">Send site information to improve Microsoft services</span></span> |
|---------------------------------|-----------------------------------------------|-----------------------------------------------------|
| <span data-ttu-id="6605f-146">Segurança</span><span class="sxs-lookup"><span data-stu-id="6605f-146">Security</span></span>                        | <span data-ttu-id="6605f-147">Não enviado</span><span class="sxs-lookup"><span data-stu-id="6605f-147">Not sent</span></span>                                      | <span data-ttu-id="6605f-148">Não enviado</span><span class="sxs-lookup"><span data-stu-id="6605f-148">Not sent</span></span>                                            |
| <span data-ttu-id="6605f-149">Básico</span><span class="sxs-lookup"><span data-stu-id="6605f-149">Basic</span></span>                           | <span data-ttu-id="6605f-150">Não enviado</span><span class="sxs-lookup"><span data-stu-id="6605f-150">Not sent</span></span>                                      | <span data-ttu-id="6605f-151">Não enviado</span><span class="sxs-lookup"><span data-stu-id="6605f-151">Not sent</span></span>                                            |
| <span data-ttu-id="6605f-152">Avançado</span><span class="sxs-lookup"><span data-stu-id="6605f-152">Enhanced</span></span>                        | <span data-ttu-id="6605f-153">Enviado</span><span class="sxs-lookup"><span data-stu-id="6605f-153">Sent</span></span>                                          | <span data-ttu-id="6605f-154">Não enviado</span><span class="sxs-lookup"><span data-stu-id="6605f-154">Not sent</span></span>                                            |
| <span data-ttu-id="6605f-155">Completo</span><span class="sxs-lookup"><span data-stu-id="6605f-155">Full</span></span>                            | <span data-ttu-id="6605f-156">Enviado</span><span class="sxs-lookup"><span data-stu-id="6605f-156">Sent</span></span>                                          | <span data-ttu-id="6605f-157">Enviado</span><span class="sxs-lookup"><span data-stu-id="6605f-157">Sent</span></span>                                                |

<span data-ttu-id="6605f-158">Se as configurações dos canais Windows 10 não forem configuradas de acordo com esta tabela, retornaremos à menor configuração de coleta de dados.</span><span class="sxs-lookup"><span data-stu-id="6605f-158">If your configurations for Windows 10 are misconfigured in accordance with the preceding table, we will fall back to the lesser data collection setting.</span></span>

<span data-ttu-id="6605f-159">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="6605f-159">For example:</span></span>

- <span data-ttu-id="6605f-160">Você define a política "Habilitar relatórios de dados de uso e de falha" como **Habilitada**, mas a configuração de dados de Diagnóstico do Windows está definida como **Básica**.</span><span class="sxs-lookup"><span data-stu-id="6605f-160">You set the "Enable usage and crash-related data reporting" policy to **Enabled** but the Windows Diagnostic data setting is set to **Basic**.</span></span> <span data-ttu-id="6605f-161">Não enviaremos dados de uso e relacionados a falhas.</span><span class="sxs-lookup"><span data-stu-id="6605f-161">We won't send usage and crash-related data.</span></span>
- <span data-ttu-id="6605f-162">Você define a diretiva "Enviar informações do site para melhorar os serviços da Microsoft" como **Desabilitada**, mas a configuração de dados de Diagnóstico do Windows está definida como **Completa**.</span><span class="sxs-lookup"><span data-stu-id="6605f-162">You set the "Send site information to improve Microsoft services" policy to **Disabled** but the Windows Diagnostic data setting is set to **Full**.</span></span> <span data-ttu-id="6605f-163">Não enviaremos informações dos sites visitados.</span><span class="sxs-lookup"><span data-stu-id="6605f-163">We won't send information about the sites that are visited.</span></span>

<span data-ttu-id="6605f-164">A implementação correta das configurações anteriores é definir a política "Habilitar relatórios de uso e dados relacionados a falhas" como **Habilitada** e definir a configuração de dados de diagnóstico do Windows como **Melhorada** ou**Completa**. </span><span class="sxs-lookup"><span data-stu-id="6605f-164">The correct implementation for the previous settings is to set the "Enable usage and crash-related data reporting" policy to **Enabled** and set the Windows Diagnostic data setting to **Enhanced** or **Full**.</span></span>

## <span data-ttu-id="6605f-165">Opções adicionais da política de privacidade</span><span class="sxs-lookup"><span data-stu-id="6605f-165">Additional privacy policy options</span></span>

<span data-ttu-id="6605f-166">Convém considerar as seguintes políticas de grupo relacionadas à privacidade de dados:</span><span class="sxs-lookup"><span data-stu-id="6605f-166">You may want to consider the following group policies related to data privacy:</span></span>

- <span data-ttu-id="6605f-167">Bloquear cookies em sites específicos</span><span class="sxs-lookup"><span data-stu-id="6605f-167">Block cookies on specific sites</span></span>
- <span data-ttu-id="6605f-168">Bloquear cookies de terceiros</span><span class="sxs-lookup"><span data-stu-id="6605f-168">Block third-party cookies</span></span>
- <span data-ttu-id="6605f-169">Configurar Não Rastrear</span><span class="sxs-lookup"><span data-stu-id="6605f-169">Configure Do Not Track</span></span>
- <span data-ttu-id="6605f-170">Desabilitar o modo InPrivate</span><span class="sxs-lookup"><span data-stu-id="6605f-170">Disable InPrivate mode</span></span>

## <span data-ttu-id="6605f-171">Ver também</span><span class="sxs-lookup"><span data-stu-id="6605f-171">See also</span></span>

- [<span data-ttu-id="6605f-172">Página de aterrissagem do Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="6605f-172">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="6605f-173">Políticas do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="6605f-173">Microsoft Edge policies</span></span>](microsoft-edge-policies.md)
- [<span data-ttu-id="6605f-174">White paper de Privacidade do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="6605f-174">Microsoft Edge Privacy Whitepaper</span></span>](https://docs.microsoft.com/microsoft-edge/privacy-whitepaper)
