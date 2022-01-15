---
title: Entenda a prevenção contra perda de dados no Microsoft Edge
ms.author: archandr
author: dan-wesley
manager: seanlynd
ms.date: 11/22/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Entenda a prevenção contra perda de dados (DLP) no Microsoft Edge
ms.openlocfilehash: b20a9eb965256adcebd47a5eb1805fb4f0a5992b
ms.sourcegitcommit: e7f3098d8b7d91cae20b5778a71a87daababc312
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/15/2022
ms.locfileid: "12297899"
---
# <a name="understand-data-loss-prevention-dlp-in-microsoft-edge"></a>Entenda a prevenção contra perda de dados (DLP) no Microsoft Edge

Este artigo descreve como o Microsoft Edge dá suporte à prevenção contra perda de dados (DLP) com DLP do ponto de extremidade e Windows Proteção de Informações (WIP).

## <a name="dlp-defined"></a>DLP definido

Prevenção contra perda de dados (DLP) é um sistema de tecnologias que identifica e protege dados confidenciais da empresa contra divulgação não autorizada. Para seguir os padrões de negócios e regulamentações do setor, as organizações devem proteger as informações confidenciais e evitar sua divulgação não autorizada. Informações confidenciais incluem dados financeiros ou informações pessoais. Alguns exemplos de informações pessoais incluem números de cartão de crédito, números de previdência social e registros de saúde.

O trabalho remoto aumentou a ênfase no uso de DLP. Com o uso crescente de atividades pessoais e de trabalho em dispositivos, as empresas estão percebendo um risco maior no compartilhamento não autorizado de dados corporativos fora do local de trabalho.

Essa mesclagem de atividades do usuário também se estendeu para dispositivos, onde os dados são movidos entre dispositivos pessoais e corporativos em várias redes públicas e privadas. O resultado líquido é um aumento considerável no risco de exposição de dados confidenciais.

O Microsoft Edge oferece suporte nativo a duas soluções de DLP diferentes, Microsoft Endpoint DLP e Proteção de Informações do Windows (WIP).

## <a name="microsoft-endpoint-data-loss-prevention-endpoint-dlp"></a>A prevenção contra perda de dados do ponto de extremidade da Microsoft (Endpoint DLP)

A prevenção contra perda de dados do ponto de extremidade da Microsoft é a próxima geração de prevenção contra perda de dados usando conceitos modernos, como proteção centrada em dados. Ele é integrado para Windows 10 e Microsoft Edge para que ele não precise de mais agentes ou plug-ins no dispositivo.

> [!NOTE]
> Isso se aplica ao Microsoft Edge na versão 85 ou posterior.

Para saber mais sobre Endpoint DLP, use os seguintes recursos:

- [Video: Microsoft Edge e Prevenção contra perda de dados (DLP)](microsoft-edge-video-security-dlp.md)
- [Saiba mais sobre a prevenção contra perda de dados do ponto de extremidade do Microsoft 365 ](/microsoft-365/compliance/endpoint-dlp-learn-about?preserve-view=true&view=o365-worldwide)
- [Introdução à prevenção contra perda de dados do Ponto de extremidade](/microsoft-365/compliance/endpoint-dlp-getting-started?preserve-view=true&view=o365-worldwide)

Microsoft Edge impõe políticas configuradas pelo administrador para arquivos confidenciais e registra eventos de auditoria para atividades não compatíveis.

Algumas das atividades do usuário que você pode auditar e gerenciar em dispositivos que executam o Windows 10 incluem as seguintes atividades:

- Upload de Arquivos: Proteja o upload de arquivos confidenciais para locais não autorizados na nuvem. <!-- The next 3 screenshots show a sequence where a user tries to drop a sensitive data file on to their local storage.-->
- Proteção da Área de Transferência: Protege os dados confidenciais contra cópias do arquivo.
- Proteção de Impressão: Protege arquivos confidenciais contra impressão.
- Salvar no USB/REDE: Protege arquivos confidenciais de serem salvos em armazenamento USB removível ou em locais de rede não autorizados.

Para obter informações mais detalhadas sobre as atividades do usuário que você pode auditar e gerenciar, confira [Atividades do Ponto de Extremidade que você pode monitorar e executar](/microsoft-365/compliance/endpoint-dlp-learn-about?preserve-view=true&view=o365-worldwide#endpoint-activities-you-can-monitor-and-take-action-on).

## <a name="windows-information-protection"></a>Proteção de Informações do Windows

Verifique o [Suporte para Proteção de Informações do Windows](./microsoft-edge-security-windows-information-protection.md), que descreve como o Microsoft Edge oferece suporte para Proteção de Informações do Windows (WIP). Você pode aprender mais sobre os requisitos do sistema, benefícios e recursos com suporte nas seguintes seções:

- [Requisitos do sistema](./microsoft-edge-security-windows-information-protection.md#system-requirements)
- [Benefícios da Proteção de Informações do Windows](./microsoft-edge-security-windows-information-protection.md#windows-information-protection-benefits)
- [Recursos da WIP com suporte no Microsoft Edge](./microsoft-edge-security-windows-information-protection.md#wip-features-supported-in-microsoft-edge)

## <a name="see-also"></a>Consulte também

- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Vídeo: Prevenção contra perda de dados - Microsoft Edge](https://www.youtube.com/watch?v=dLD04U9eTqg)
- [Visão geral da prevenção contra perda de dados](/microsoft-365/compliance/data-loss-prevention-policies?preserve-view=true&view=o365-worldwide)
- [Proteger os dados da sua empresa usando a Proteção de Informações do Windows](/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip)