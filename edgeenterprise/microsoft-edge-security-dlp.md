---
title: Prevenção contra Perda de Dados no Microsoft Edge
ms.author: archandr
author: dan-wesley
manager: seanlynd
ms.date: 03/01/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Prevenção contra Perda de Dados (DLP) no Microsoft Edge
ms.openlocfilehash: ac34386ed1b691d7b45f30c2b2ec295955d11104
ms.sourcegitcommit: f363ceb6c42054fabc95ce8d7bca3c52d80e6a9f
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/24/2021
ms.locfileid: "11447925"
---
# <a name="data-loss-prevention-dlp-in-microsoft-edge"></a><span data-ttu-id="a3119-103">Prevenção contra Perda de Dados (DLP) no Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="a3119-103">Data Loss Prevention (DLP) in Microsoft Edge</span></span>

<span data-ttu-id="a3119-104">Prevenção contra perda de dados (DLP) é um sistema de tecnologias que identifica e protege dados confidenciais da empresa contra divulgação não autorizada.</span><span class="sxs-lookup"><span data-stu-id="a3119-104">Data loss prevention (DLP) is a system of technologies that identify and safeguard sensitive enterprise data from unauthorized disclosure.</span></span> <span data-ttu-id="a3119-105">Para seguir os padrões de negócios e regulamentações do setor, as organizações devem proteger as informações confidenciais e evitar sua divulgação não autorizada.</span><span class="sxs-lookup"><span data-stu-id="a3119-105">To comply with business standards and industry regulations, organizations must protect sensitive information and prevent its unauthorized disclosure.</span></span> <span data-ttu-id="a3119-106">As informações confidenciais incluem dados financeiros ou informações de identificação pessoal (PII), como números de cartão de crédito, números de seguridade social ou registros de saúde, entre muitas outras coisas.</span><span class="sxs-lookup"><span data-stu-id="a3119-106">Sensitive information includes financial data or personally identifiable information (PII) such as credit card numbers, social security numbers, or health records, among many other things.</span></span>

<span data-ttu-id="a3119-107">O trabalho remoto aumentou a ênfase no uso de DLP.</span><span class="sxs-lookup"><span data-stu-id="a3119-107">Remote work has increased the emphasis on using DLP.</span></span> <span data-ttu-id="a3119-108">Com o uso crescente de atividades pessoais e de trabalho em dispositivos, as empresas estão percebendo um risco maior no compartilhamento não autorizado de dados corporativos fora do local de trabalho.</span><span class="sxs-lookup"><span data-stu-id="a3119-108">With the growing use of personal and work activities on devices, enterprises are seeing an increased risk of unauthorized sharing of corporate data outside the workplace.</span></span>

<span data-ttu-id="a3119-109">Essa combinação de atividades do usuário também se espalhou para os dispositivos onde os dados são compartilhados entre dispositivos pessoais e corporativos em uma variedade de redes públicas e privadas.</span><span class="sxs-lookup"><span data-stu-id="a3119-109">This blending of user activities has spread to devices as well, where data is moved between personal and corporate devices over a variety of public and private networks.</span></span> <span data-ttu-id="a3119-110">O resultado líquido é um aumento considerável no risco de exposição de dados confidenciais.</span><span class="sxs-lookup"><span data-stu-id="a3119-110">The net result is a dramatically increased risk of exposing sensitive data.</span></span>

<span data-ttu-id="a3119-111">O Microsoft Edge oferece suporte nativo a duas soluções de DLP diferentes, Microsoft Endpoint DLP e Proteção de Informações do Windows (WIP).</span><span class="sxs-lookup"><span data-stu-id="a3119-111">Microsoft Edge natively supports two different DLP solutions, Microsoft Endpoint DLP and Windows Information Protection (WIP).</span></span>

## <a name="microsoft-endpoint-data-loss-prevention-endpoint-dlp"></a><span data-ttu-id="a3119-112">A prevenção contra perda de dados do ponto de extremidade da Microsoft (Endpoint DLP)</span><span class="sxs-lookup"><span data-stu-id="a3119-112">Microsoft Endpoint data loss prevention (Endpoint DLP)</span></span>

<span data-ttu-id="a3119-113">A prevenção contra perda de dados do ponto de extremidade da Microsoft é a próxima geração de prevenção contra perda de dados usando conceitos modernos, como proteção centrada em dados.</span><span class="sxs-lookup"><span data-stu-id="a3119-113">Microsoft Endpoint DLP is the next generation of data loss prevention using modern concepts such as data-centric protection.</span></span> <span data-ttu-id="a3119-114">Ela é integrada ao Windows 10 e ao Microsoft Edge, portanto, não é necessário agentes adicionais ou plugins no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a3119-114">It's built-in to Windows 10 and Microsoft Edge so it doesn't need additional agents or plugins on the device.</span></span>

> [!NOTE]
> <span data-ttu-id="a3119-115">Isso se aplica ao Microsoft Edge na versão 85 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="a3119-115">This applies to Microsoft Edge version 85 or later.</span></span>

<span data-ttu-id="a3119-116">Para saber mais sobre Endpoint DLP, use os seguintes recursos:</span><span class="sxs-lookup"><span data-stu-id="a3119-116">To learn more about Endpoint DLP, use the following resources:</span></span>

- [<span data-ttu-id="a3119-117">Video: Microsoft Edge e Prevenção contra perda de dados (DLP)</span><span class="sxs-lookup"><span data-stu-id="a3119-117">Video: Microsoft Edge and Data loss prevention (DLP)</span></span>](microsoft-edge-video-security-dlp.md)
- [<span data-ttu-id="a3119-118">Saiba mais sobre a prevenção contra perda de dados do ponto de extremidade do Microsoft 365 </span><span class="sxs-lookup"><span data-stu-id="a3119-118">Learn about Microsoft 365 Endpoint data loss prevention</span></span>](/microsoft-365/compliance/endpoint-dlp-learn-about?preserve-view=true&view=o365-worldwide)
- [<span data-ttu-id="a3119-119">Introdução à prevenção contra perda de dados do Ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="a3119-119">Get started with Endpoint data loss prevention</span></span>](/microsoft-365/compliance/endpoint-dlp-getting-started?preserve-view=true&view=o365-worldwide)

<span data-ttu-id="a3119-120">O Microsoft Edge impõe políticas configuradas pelo administrador para arquivos confidenciais e registros de eventos de auditoria para atividades não compatíveis.</span><span class="sxs-lookup"><span data-stu-id="a3119-120">Microsoft Edge enforces admin configured policies for sensitive files and records audit events for non-compliant activities.</span></span>

<span data-ttu-id="a3119-121">Algumas das atividades do usuário que você pode auditar e gerenciar em dispositivos que executam o Windows 10 incluem as seguintes atividades:</span><span class="sxs-lookup"><span data-stu-id="a3119-121">Some of the user activities that you can audit and manage on devices running Windows 10 include the following activities:</span></span>

- <span data-ttu-id="a3119-122">Upload de Arquivos: Proteja o upload de arquivos confidenciais para locais não autorizados na nuvem.</span><span class="sxs-lookup"><span data-stu-id="a3119-122">File Upload: Protect sensitive file upload to unauthorized cloud locations.</span></span> <!-- The next 3 screenshots show a sequence where a user tries to drop a sensitive data file on to their local storage.-->
- <span data-ttu-id="a3119-123">Proteção da Área de Transferência: Protege os dados confidenciais contra cópias do arquivo.</span><span class="sxs-lookup"><span data-stu-id="a3119-123">Clipboard Protection: Protect sensitive data from being copied out of the file.</span></span>
- <span data-ttu-id="a3119-124">Proteção de Impressão: Protege arquivos confidenciais contra impressão.</span><span class="sxs-lookup"><span data-stu-id="a3119-124">Print Protection: Protect sensitive file from being printed.</span></span>
- <span data-ttu-id="a3119-125">Salvar no USB/REDE: Protege arquivos confidenciais de serem salvos em armazenamento USB removível ou em locais de rede não autorizados.</span><span class="sxs-lookup"><span data-stu-id="a3119-125">Save to USB/Network: Protect sensitive file from being saved to removable USB storage or unauthorized network locations.</span></span>

<span data-ttu-id="a3119-126">Para obter informações mais detalhadas sobre as atividades do usuário que você pode auditar e gerenciar, confira [Atividades do Ponto de Extremidade que você pode monitorar e executar](/microsoft-365/compliance/endpoint-dlp-learn-about?preserve-view=true&view=o365-worldwide#endpoint-activities-you-can-monitor-and-take-action-on).</span><span class="sxs-lookup"><span data-stu-id="a3119-126">For more detailed information about user activities you can audit and manage, see [Endpoint activities you can monitor and take action on](/microsoft-365/compliance/endpoint-dlp-learn-about?preserve-view=true&view=o365-worldwide#endpoint-activities-you-can-monitor-and-take-action-on).</span></span>

## <a name="windows-information-protection"></a><span data-ttu-id="a3119-127">Proteção de Informações do Windows</span><span class="sxs-lookup"><span data-stu-id="a3119-127">Windows Information Protection</span></span>

<span data-ttu-id="a3119-128">Verifique o [Suporte para Proteção de Informações do Windows](./microsoft-edge-security-windows-information-protection.md), que descreve como o Microsoft Edge oferece suporte para Proteção de Informações do Windows (WIP).</span><span class="sxs-lookup"><span data-stu-id="a3119-128">Check out [Support for Windows Information Protection](./microsoft-edge-security-windows-information-protection.md), which describes how Microsoft Edge supports Windows Information Protection (WIP).</span></span> <span data-ttu-id="a3119-129">Você pode aprender mais sobre os requisitos do sistema, benefícios e recursos com suporte nas seguintes seções:</span><span class="sxs-lookup"><span data-stu-id="a3119-129">You can learn moe about system requirements, benefits, and supported features in the following sections:</span></span>

- [<span data-ttu-id="a3119-130">Requisitos do sistema</span><span class="sxs-lookup"><span data-stu-id="a3119-130">System Requirements</span></span>](./microsoft-edge-security-windows-information-protection.md#system-requirements)
- [<span data-ttu-id="a3119-131">Benefícios da Proteção de Informações do Windows</span><span class="sxs-lookup"><span data-stu-id="a3119-131">Windows Information Protection Benefits</span></span>](./microsoft-edge-security-windows-information-protection.md#windows-information-protection-benefits)
- [<span data-ttu-id="a3119-132">Recursos da WIP com suporte no Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="a3119-132">WIP features supported in Microsoft Edge</span></span>](./microsoft-edge-security-windows-information-protection.md#wip-features-supported-in-microsoft-edge)

## <a name="see-also"></a><span data-ttu-id="a3119-133">Consulte também</span><span class="sxs-lookup"><span data-stu-id="a3119-133">See also</span></span>

- [<span data-ttu-id="a3119-134">Página de aterrissagem do Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="a3119-134">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="a3119-135">Vídeo: Prevenção contra perda de dados - Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="a3119-135">Video: Data loss prevention - Microsoft Edge</span></span>](https://www.youtube.com/watch?v=dLD04U9eTqg)
- [<span data-ttu-id="a3119-136">Visão geral da prevenção contra perda de dados</span><span class="sxs-lookup"><span data-stu-id="a3119-136">Overview of data loss prevention</span></span>](/microsoft-365/compliance/data-loss-prevention-policies?preserve-view=true&view=o365-worldwide)
- [<span data-ttu-id="a3119-137">Proteger os dados da sua empresa usando a Proteção de Informações do Windows</span><span class="sxs-lookup"><span data-stu-id="a3119-137">Protect your enterprise data using Windows Information Protection</span></span>](/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip)