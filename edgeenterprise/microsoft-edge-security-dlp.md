---
title: Prevenção contra Perda de Dados no Microsoft Edge
ms.author: archandr
author: dan-wesley
manager: seanlynd
ms.date: 11/18/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Prevenção contra Perda de Dados (DLP) no Microsoft Edge
ms.openlocfilehash: 72f670caf34a09cdfc7f47575f688c2a39d3c221
ms.sourcegitcommit: 5a5be508c3c9c57187aca821b4a16f639abdd7e2
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/18/2020
ms.locfileid: "11176938"
---
# Prevenção contra Perda de Dados (DLP) no Microsoft Edge

Prevenção contra perda de dados (DLP) é um sistema de tecnologias que identifica e protege dados confidenciais da empresa contra divulgação não autorizada. Para seguir os padrões de negócios e regulamentações do setor, as organizações devem proteger as informações confidenciais e evitar sua divulgação não autorizada. As informações confidenciais incluem dados financeiros ou informações de identificação pessoal (PII), como números de cartão de crédito, números de seguridade social ou registros de saúde, entre muitas outras coisas.

O trabalho remoto aumentou a ênfase no uso de DLP. Com o uso crescente de atividades pessoais e de trabalho em dispositivos, as empresas estão percebendo um risco maior no compartilhamento não autorizado de dados corporativos fora do local de trabalho.

Essa combinação de atividades do usuário também se espalhou para os dispositivos onde os dados são compartilhados entre dispositivos pessoais e corporativos em uma variedade de redes públicas e privadas. O resultado líquido é um aumento considerável no risco de exposição de dados confidenciais.

O Microsoft Edge oferece suporte nativo a duas soluções de DLP diferentes, Microsoft Endpoint DLP e Proteção de Informações do Windows (WIP).

## A prevenção contra perda de dados do ponto de extremidade da Microsoft (Endpoint DLP)

A prevenção contra perda de dados do ponto de extremidade da Microsoft é a próxima geração de prevenção contra perda de dados usando conceitos modernos, como proteção centrada em dados. Ela é integrada ao Windows 10 e ao Microsoft Edge, portanto, não é necessário agentes adicionais ou plugins no dispositivo.

> [!NOTE]
> Isso se aplica ao Microsoft Edge na versão 85 ou posterior.

Para saber mais sobre a DLP do Ponto de extremidade:

- [Saiba mais sobre a prevenção contra perda de dados do ponto de extremidade do Microsoft 365 ](https://docs.microsoft.com/microsoft-365/compliance/endpoint-dlp-learn-about?view=o365-worldwide)
- [Introdução à prevenção contra perda de dados do Ponto de extremidade](https://docs.microsoft.com/microsoft-365/compliance/endpoint-dlp-getting-started?view=o365-worldwide)

O Microsoft Edge impõe políticas configuradas pelo administrador para arquivos confidenciais e registros de eventos de auditoria para atividades não compatíveis.

Algumas das atividades do usuário que você pode auditar e gerenciar em dispositivos que executam o Windows 10 incluem as seguintes atividades:

- Upload de Arquivos: Proteja o upload de arquivos confidenciais para locais não autorizados na nuvem. As próximas 3 capturas de tela mostram uma sequência em que um usuário tenta soltar um arquivo de dados confidenciais em seu armazenamento local.
- Proteção da Área de Transferência: Protege os dados confidenciais contra cópias do arquivo.
- Proteção de Impressão: Protege arquivos confidenciais contra impressão.
- Salvar no USB/REDE: Protege arquivos confidenciais de serem salvos em armazenamento USB removível ou em locais de rede não autorizados.

Para obter informações mais detalhadas sobre as atividades do usuário que você pode auditar e gerenciar, confira [Atividades do Ponto de Extremidade que você pode monitorar e executar](https://docs.microsoft.com/microsoft-365/compliance/endpoint-dlp-learn-about?view=o365-worldwide#endpoint-activities-you-can-monitor-and-take-action-on).

## Proteção de Informações do Windows

Verifique o [Suporte para Proteção de Informações do Windows](https://docs.microsoft.com/deployedge/microsoft-edge-security-windows-information-protection), que descreve como o Microsoft Edge oferece suporte para Proteção de Informações do Windows (WIP). Você pode aprender mais sobre os requisitos do sistema, benefícios e recursos com suporte nas seguintes seções:

- [Requisitos do sistema](https://docs.microsoft.com/deployedge/:microsoft-edge-security-windows-information-protection#system-requirements)
- [Benefícios da Proteção de Informações do Windows](https://docs.microsoft.com/deployedge/microsoft-edge-security-windows-information-protection#windows-information-protection-benefits)
- [Recursos da WIP com suporte no Microsoft Edge](https://docs.microsoft.com/DeployEdge/microsoft-edge-security-windows-information-protection#wip-features-supported-in-microsoft-edge)

## Consulte também

- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Vídeo: Prevenção contra perda de dados - Microsoft Edge](https://www.youtube.com/watch?v=dLD04U9eTqg)
- [Visão geral da prevenção contra perda de dados](https://docs.microsoft.com/microsoft-365/compliance/data-loss-prevention-policies?view=o365-worldwide)
- [Proteger os dados da sua empresa usando a Proteção de Informações do Windows](https://docs.microsoft.com/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip)
