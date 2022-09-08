---
title: Entender a Prevenção contra Perda de Dados no Microsoft Edge
ms.author: archandr
author: dan-wesley
manager: seanlynd
ms.date: 09/06/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Entender a prevenção contra perda de dados (DLP) no Microsoft Edge
ms.openlocfilehash: 401525c5ee6369c32caeb9bf61635ec441d5e3aa
ms.sourcegitcommit: 80d9f61a23a7dc0def80089850a53ea02e571ed6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/08/2022
ms.locfileid: "12746117"
---
# <a name="understand-data-loss-prevention-dlp-in-microsoft-edge"></a>Entender a prevenção contra perda de dados (DLP) no Microsoft Edge

Este artigo descreve como o Microsoft Edge dá suporte à prevenção contra perda de dados (DLP) com dlp de ponto de extremidade e wip (windows Proteção de Informações).

## <a name="dlp-defined"></a>DLP definido

Prevenção contra perda de dados (DLP) é um sistema de tecnologias que identifica e protege dados confidenciais da empresa contra divulgação não autorizada. Para seguir os padrões de negócios e regulamentações do setor, as organizações devem proteger as informações confidenciais e evitar sua divulgação não autorizada. Informações confidenciais incluem dados financeiros ou informações pessoais. Alguns exemplos de informações pessoais incluem números de cartão de crédito, números de seguro social e registros de saúde.

O trabalho remoto aumentou a ênfase no uso de DLP. Com o uso crescente de atividades pessoais e de trabalho em dispositivos, as empresas estão percebendo um risco maior no compartilhamento não autorizado de dados corporativos fora do local de trabalho.

Essa combinação de atividades do usuário também se espalhou para dispositivos, onde os dados são movidos entre dispositivos pessoais e corporativos em várias redes públicas e privadas. O resultado líquido é um aumento considerável no risco de exposição de dados confidenciais.

O Microsoft Edge oferece suporte nativo a duas soluções de DLP diferentes, Microsoft Endpoint DLP e Proteção de Informações do Windows (WIP).

## <a name="microsoft-endpoint-data-loss-prevention-endpoint-dlp"></a>A prevenção contra perda de dados do ponto de extremidade da Microsoft (Endpoint DLP)

A prevenção contra perda de dados do ponto de extremidade da Microsoft é a próxima geração de prevenção contra perda de dados usando conceitos modernos, como proteção centrada em dados. Ele é interno para Windows 10 e o Microsoft Edge para que ele não precise de mais agentes ou plug-ins no dispositivo.

> [!NOTE]
> Isso se aplica ao Microsoft Edge na versão 85 ou posterior.

Para saber mais sobre Endpoint DLP, use os seguintes recursos:

- [Video: Microsoft Edge e Prevenção contra perda de dados (DLP)](microsoft-edge-video-security-dlp.md)
- [Saiba mais sobre a prevenção contra perda de dados do ponto de extremidade do Microsoft 365 ](/microsoft-365/compliance/endpoint-dlp-learn-about?preserve-view=true&view=o365-worldwide)
- [Introdução à prevenção contra perda de dados do Ponto de extremidade](/microsoft-365/compliance/endpoint-dlp-getting-started?preserve-view=true&view=o365-worldwide)

O Microsoft Edge impõe políticas configuradas pelo administrador para arquivos confidenciais e registra eventos de auditoria para atividades sem conformidade.

Algumas das atividades do usuário que você pode auditar e gerenciar em dispositivos que executam o Windows 10 incluem as seguintes atividades:

- Upload de Arquivos: Proteja o upload de arquivos confidenciais para locais não autorizados na nuvem. <!-- The next 3 screenshots show a sequence where a user tries to drop a sensitive data file on to their local storage.-->
- Proteção da Área de Transferência: Protege os dados confidenciais contra cópias do arquivo.
- Proteção de Impressão: Protege arquivos confidenciais contra impressão.
- Salvar no USB/REDE: Protege arquivos confidenciais de serem salvos em armazenamento USB removível ou em locais de rede não autorizados.

Para obter informações mais detalhadas sobre as atividades do usuário que você pode auditar e gerenciar, confira [Atividades do Ponto de Extremidade que você pode monitorar e executar](/microsoft-365/compliance/endpoint-dlp-learn-about?preserve-view=true&view=o365-worldwide#endpoint-activities-you-can-monitor-and-take-action-on).

## <a name="windows-information-protection"></a>Proteção de Informações do Windows

> [!NOTE]
> A proteção de informações do Windows será descontinuada ao longo do tempo. Para obter mais informações, consulte [Anunciando o pôr do sol do Windows Proteção de Informações (WIP)](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/announcing-the-sunset-of-windows-information-protection-wip/ba-p/3579282).

Verifique o [Suporte para Proteção de Informações do Windows](./microsoft-edge-security-windows-information-protection.md), que descreve como o Microsoft Edge oferece suporte para Proteção de Informações do Windows (WIP). Você pode aprender mais sobre os requisitos do sistema, benefícios e recursos com suporte nas seguintes seções:

- [Requisitos do sistema](./microsoft-edge-security-windows-information-protection.md#system-requirements)
- [Benefícios da Proteção de Informações do Windows](./microsoft-edge-security-windows-information-protection.md#windows-information-protection-benefits)
- [Recursos da WIP com suporte no Microsoft Edge](./microsoft-edge-security-windows-information-protection.md#wip-features-supported-in-microsoft-edge)

## <a name="see-also"></a>Consulte também

- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Vídeo: Prevenção contra perda de dados - Microsoft Edge](https://www.youtube.com/watch?v=dLD04U9eTqg)
- [Visão geral da prevenção contra perda de dados](/microsoft-365/compliance/data-loss-prevention-policies?preserve-view=true&view=o365-worldwide)
- [Proteger os dados da sua empresa usando a Proteção de Informações do Windows](/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip)