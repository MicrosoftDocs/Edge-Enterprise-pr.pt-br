---
title: Prevenção contra Perda de Dados no Microsoft Edge
ms.author: archandr
author: dan-wesley
manager: seanlynd
ms.date: 02/05/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Prevenção contra Perda de Dados (DLP) no Microsoft Edge
ms.openlocfilehash: 8c7906f69f8d1161b47aa381bc04bcdaa70fe6cd
ms.sourcegitcommit: c290b0b0fa6b7d7f94dcdfdda91302da733326ec
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/06/2021
ms.locfileid: "11314554"
---
# <span data-ttu-id="87818-103">Prevenção contra Perda de Dados (DLP) no Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="87818-103">Data Loss Prevention (DLP) in Microsoft Edge</span></span>

<span data-ttu-id="87818-104">Prevenção contra perda de dados (DLP) é um sistema de tecnologias que identifica e protege dados confidenciais da empresa contra divulgação não autorizada.</span><span class="sxs-lookup"><span data-stu-id="87818-104">Data loss prevention (DLP) is a system of technologies that identify and safeguard sensitive enterprise data from unauthorized disclosure.</span></span> <span data-ttu-id="87818-105">Para seguir os padrões de negócios e regulamentações do setor, as organizações devem proteger as informações confidenciais e evitar sua divulgação não autorizada.</span><span class="sxs-lookup"><span data-stu-id="87818-105">To comply with business standards and industry regulations, organizations must protect sensitive information and prevent its unauthorized disclosure.</span></span> <span data-ttu-id="87818-106">As informações confidenciais incluem dados financeiros ou informações de identificação pessoal (PII), como números de cartão de crédito, números de seguridade social ou registros de saúde, entre muitas outras coisas.</span><span class="sxs-lookup"><span data-stu-id="87818-106">Sensitive information includes financial data or personally identifiable information (PII) such as credit card numbers, social security numbers, or health records, among many other things.</span></span>

<span data-ttu-id="87818-107">O trabalho remoto aumentou a ênfase no uso de DLP.</span><span class="sxs-lookup"><span data-stu-id="87818-107">Remote work has increased the emphasis on using DLP.</span></span> <span data-ttu-id="87818-108">Com o uso crescente de atividades pessoais e de trabalho em dispositivos, as empresas estão percebendo um risco maior no compartilhamento não autorizado de dados corporativos fora do local de trabalho.</span><span class="sxs-lookup"><span data-stu-id="87818-108">With the growing use of personal and work activities on devices, enterprises are seeing an increased risk of unauthorized sharing of corporate data outside the workplace.</span></span>

<span data-ttu-id="87818-109">Essa combinação de atividades do usuário também se espalhou para os dispositivos onde os dados são compartilhados entre dispositivos pessoais e corporativos em uma variedade de redes públicas e privadas.</span><span class="sxs-lookup"><span data-stu-id="87818-109">This blending of user activities has spread to devices as well, where data is moved between personal and corporate devices over a variety of public and private networks.</span></span> <span data-ttu-id="87818-110">O resultado líquido é um aumento considerável no risco de exposição de dados confidenciais.</span><span class="sxs-lookup"><span data-stu-id="87818-110">The net result is a dramatically increased risk of exposing sensitive data.</span></span>

<span data-ttu-id="87818-111">O Microsoft Edge oferece suporte nativo a duas soluções de DLP diferentes, Microsoft Endpoint DLP e Proteção de Informações do Windows (WIP).</span><span class="sxs-lookup"><span data-stu-id="87818-111">Microsoft Edge natively supports two different DLP solutions, Microsoft Endpoint DLP and Windows Information Protection (WIP).</span></span>

## <span data-ttu-id="87818-112">A prevenção contra perda de dados do ponto de extremidade da Microsoft (Endpoint DLP)</span><span class="sxs-lookup"><span data-stu-id="87818-112">Microsoft Endpoint data loss prevention (Endpoint DLP)</span></span>

<span data-ttu-id="87818-113">A prevenção contra perda de dados do ponto de extremidade da Microsoft é a próxima geração de prevenção contra perda de dados usando conceitos modernos, como proteção centrada em dados.</span><span class="sxs-lookup"><span data-stu-id="87818-113">Microsoft Endpoint DLP is the next generation of data loss prevention using modern concepts such as data-centric protection.</span></span> <span data-ttu-id="87818-114">Ela é integrada ao Windows 10 e ao Microsoft Edge, portanto, não é necessário agentes adicionais ou plugins no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="87818-114">It's built-in to Windows 10 and Microsoft Edge so it doesn't need additional agents or plugins on the device.</span></span>

> [!NOTE]
> <span data-ttu-id="87818-115">Isso se aplica ao Microsoft Edge na versão 85 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="87818-115">This applies to Microsoft Edge version 85 or later.</span></span>

<span data-ttu-id="87818-116">Para saber mais sobre Endpoint DLP, use os seguintes recursos:</span><span class="sxs-lookup"><span data-stu-id="87818-116">To learn more about Endpoint DLP, use the following resources:</span></span>

- [<span data-ttu-id="87818-117">Video: Microsoft Edge e Prevenção contra perda de dados (DLP)</span><span class="sxs-lookup"><span data-stu-id="87818-117">Video: Microsoft Edge and Data loss prevention (DLP)</span></span>](microsoft-edge-video-security-dlp.md)
- [<span data-ttu-id="87818-118">Saiba mais sobre a prevenção contra perda de dados do ponto de extremidade do Microsoft 365 </span><span class="sxs-lookup"><span data-stu-id="87818-118">Learn about Microsoft 365 Endpoint data loss prevention</span></span>](https://docs.microsoft.com/microsoft-365/compliance/endpoint-dlp-learn-about?view=o365-worldwide&preserve-view=true)
- [<span data-ttu-id="87818-119">Introdução à prevenção contra perda de dados do Ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="87818-119">Get started with Endpoint data loss prevention</span></span>](https://docs.microsoft.com/microsoft-365/compliance/endpoint-dlp-getting-started?view=o365-worldwide&preserve-view=true)

<span data-ttu-id="87818-120">O Microsoft Edge impõe políticas configuradas pelo administrador para arquivos confidenciais e registros de eventos de auditoria para atividades não compatíveis.</span><span class="sxs-lookup"><span data-stu-id="87818-120">Microsoft Edge enforces admin configured policies for sensitive files and records audit events for non-compliant activities.</span></span>

<span data-ttu-id="87818-121">Algumas das atividades do usuário que você pode auditar e gerenciar em dispositivos que executam o Windows 10 incluem as seguintes atividades:</span><span class="sxs-lookup"><span data-stu-id="87818-121">Some of the user activities that you can audit and manage on devices running Windows 10 include the following activities:</span></span>

- <span data-ttu-id="87818-122">Upload de Arquivos: Proteja o upload de arquivos confidenciais para locais não autorizados na nuvem.</span><span class="sxs-lookup"><span data-stu-id="87818-122">File Upload: Protect sensitive file upload to unauthorized cloud locations.</span></span> <!-- The next 3 screenshots show a sequence where a user tries to drop a sensitive data file on to their local storage.-->
- <span data-ttu-id="87818-123">Proteção da Área de Transferência: Protege os dados confidenciais contra cópias do arquivo.</span><span class="sxs-lookup"><span data-stu-id="87818-123">Clipboard Protection: Protect sensitive data from being copied out of the file.</span></span>
- <span data-ttu-id="87818-124">Proteção de Impressão: Protege arquivos confidenciais contra impressão.</span><span class="sxs-lookup"><span data-stu-id="87818-124">Print Protection: Protect sensitive file from being printed.</span></span>
- <span data-ttu-id="87818-125">Salvar no USB/REDE: Protege arquivos confidenciais de serem salvos em armazenamento USB removível ou em locais de rede não autorizados.</span><span class="sxs-lookup"><span data-stu-id="87818-125">Save to USB/Network: Protect sensitive file from being saved to removable USB storage or unauthorized network locations.</span></span>

<span data-ttu-id="87818-126">Para obter informações mais detalhadas sobre as atividades do usuário que você pode auditar e gerenciar, confira [Atividades do Ponto de Extremidade que você pode monitorar e executar](https://docs.microsoft.com/microsoft-365/compliance/endpoint-dlp-learn-about?view=o365-worldwide#endpoint-activities-you-can-monitor-and-take-action-on&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="87818-126">For more detailed information about user activities you can audit and manage, see [Endpoint activities you can monitor and take action on](https://docs.microsoft.com/microsoft-365/compliance/endpoint-dlp-learn-about?view=o365-worldwide#endpoint-activities-you-can-monitor-and-take-action-on&preserve-view=true).</span></span>

## <span data-ttu-id="87818-127">Proteção de Informações do Windows</span><span class="sxs-lookup"><span data-stu-id="87818-127">Windows Information Protection</span></span>

<span data-ttu-id="87818-128">Verifique o [Suporte para Proteção de Informações do Windows](https://docs.microsoft.com/deployedge/microsoft-edge-security-windows-information-protection), que descreve como o Microsoft Edge oferece suporte para Proteção de Informações do Windows (WIP).</span><span class="sxs-lookup"><span data-stu-id="87818-128">Check out [Support for Windows Information Protection](https://docs.microsoft.com/deployedge/microsoft-edge-security-windows-information-protection), which describes how Microsoft Edge supports Windows Information Protection (WIP).</span></span> <span data-ttu-id="87818-129">Você pode aprender mais sobre os requisitos do sistema, benefícios e recursos com suporte nas seguintes seções:</span><span class="sxs-lookup"><span data-stu-id="87818-129">You can learn moe about system requirements, benefits, and supported features in the following sections:</span></span>

- [<span data-ttu-id="87818-130">Requisitos do sistema</span><span class="sxs-lookup"><span data-stu-id="87818-130">System Requirements</span></span>](https://docs.microsoft.com/deployedge/:microsoft-edge-security-windows-information-protection#system-requirements)
- [<span data-ttu-id="87818-131">Benefícios da Proteção de Informações do Windows</span><span class="sxs-lookup"><span data-stu-id="87818-131">Windows Information Protection Benefits</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-security-windows-information-protection#windows-information-protection-benefits)
- [<span data-ttu-id="87818-132">Recursos da WIP com suporte no Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="87818-132">WIP features supported in Microsoft Edge</span></span>](https://docs.microsoft.com/DeployEdge/microsoft-edge-security-windows-information-protection#wip-features-supported-in-microsoft-edge)

## <span data-ttu-id="87818-133">Consulte também</span><span class="sxs-lookup"><span data-stu-id="87818-133">See also</span></span>

- [<span data-ttu-id="87818-134">Página de aterrissagem do Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="87818-134">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="87818-135">Vídeo: Prevenção contra perda de dados - Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="87818-135">Video: Data loss prevention - Microsoft Edge</span></span>](https://www.youtube.com/watch?v=dLD04U9eTqg)
- [<span data-ttu-id="87818-136">Visão geral da prevenção contra perda de dados</span><span class="sxs-lookup"><span data-stu-id="87818-136">Overview of data loss prevention</span></span>](https://docs.microsoft.com/microsoft-365/compliance/data-loss-prevention-policies?view=o365-worldwide&preserve-view=true)
- [<span data-ttu-id="87818-137">Proteger os dados da sua empresa usando a Proteção de Informações do Windows</span><span class="sxs-lookup"><span data-stu-id="87818-137">Protect your enterprise data using Windows Information Protection</span></span>](https://docs.microsoft.com/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip)
