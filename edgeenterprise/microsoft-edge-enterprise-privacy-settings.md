---
title: Configurações de privacidade do Microsoft Edge Enterprise
ms.author: likravit
author: dan-wesley
manager: srugh
ms.date: 09/09/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Definir as configurações de privacidade do Microsoft Edge Enterprise
ms.openlocfilehash: 25b475206734634df9995f568a6d4e8c52e9f9de
ms.sourcegitcommit: 16984537c8f5c9c60e92f41f0f869231fb79ccd0
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/09/2020
ms.locfileid: "11005489"
---
# Configurar as políticas do Microsoft Edge para oferecer suporte à privacidade da empresa

A Microsoft está comprometida em fornecer às empresas as informações e os controles necessários para fazer escolhas sobre a coleta de dados no Microsoft Edge.

## Visão geral

Por padrão, quando o Microsoft Edge é implantado no Windows 10, os dados de diagnóstico são enviados com base na [Configuração de dados de diagnóstico do Windows](https://go.microsoft.com/fwlink/?linkid=2099569) dos usuários.

Quando o Microsoft Edge é implantado em plataformas não Windows, os dados de diagnóstico são coletados de acordo com as configurações das seguintes políticas de grupo:

- (PRETERIDA) [MetricsReportingEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#metricsreportingenabled) - Habilita a geração de relatórios de dados relacionados a falhas e de uso. Essa política se tornará obsoleta na versão 89 do Microsoft Edge.
- (PRETERIDA) [SendSiteInfoToImproveServices](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sendsiteinfotoimproveservices) - Envia informações do site para melhorar os serviços Microsoft. Essa política se tornará obsoleta na versão 89 do Microsoft Edge.

As políticas preteridas mencionadas são substituídas por [Permitir Telemetria](https://go.microsoft.com/fwlink/?linkid=2099569) no Windows 10 e a política [DiagnosticData](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#diagnosticdata) para todas as outras políticas.  

## Definir configurações de política

Antes começar, baixe e use o modelo de política do Microsoft Edge mais recente (para obter mais informações, consulte [Configurar o Microsoft Edge](configure-microsoft-edge.md)).

### Enviar dados de diagnóstico obrigatórios e opcionais referentes ao uso do navegador

Se a política [DiagnosticData](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#diagnosticdata) estiver configurada, ela tem precedência sobre [MetricsReportingEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#metricsreportingenabled)  e [SendSiteInfoToImproveServices](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sendsiteinfotoimproveservices).

#### Dados de diagnóstico obrigatórios e opcionais

Os dados de diagnóstico obrigatórios são coletados para manter o Microsoft Edge seguro, atualizado e funcionando corretamente.

Os dados de diagnóstico opcionais incluem dados sobre como você usa o navegador, os sites visitados e os relatórios de falha para ajudar a manter o Microsoft Edge seguro, atualizado e funcionando corretamente, e são usados para melhorar o Microsoft Edge e outros produtos e serviços Microsoft para todos os usuários.

> [!NOTE]
> Essa política não é compatível com dispositivos com Windows 10. Para controlar a coleta de dados no Windows 10, os administradores de TI devem usar a política de grupo de dados de diagnóstico do Windows. Essa política irá **Permitir Telemetria** ou **Permitir Dados de Diagnóstico**, dependendo da versão do Windows. Saiba mais sobre a [coleta de dados de diagnóstico do Windows 10](https://docs.microsoft.com/windows/privacy/configure-windows-diagnostic-data-in-your-organization).

Use uma das seguintes configurações para configurar **DiagnosticData**:

- Desativado (não recomendado) (0) desativa a coleta de dados de diagnóstico obrigatórios ou opcionais. 
- Dados obrigatórios (1) envia os dados de diagnóstico obrigatórios mas desativa a coleta de dados de diagnóstico opcionais. O Microsoft Edge irá enviar os dados de diagnóstico obrigatórios para manter o Microsoft Edge seguro, atualizado e funcionando corretamente. 
- Dados opcionais (2) envia os dados de diagnóstico opcionais, inclui dados sobre o uso do navegador, sites visitados, relatórios de falha enviados à Microsoft para ajudar a manter o Microsoft Edge seguro, atualizado e funcionando corretamente e é usado para melhorar o Microsoft Edge e outros produtos e serviços Microsoft para todos os usuários.

No Windows 7, Windows 8/8.1 e macOS, essa política controla o envio dos dados de diagnóstico obrigatórios e opcionais à Microsoft.

Se você não configurar ou desativar essa política, o padrão do Microsoft Edge será a preferência do usuário.

### (PRETERIDA) Habilitar a geração de relatórios de dados relacionados a falhas e de uso

A política **MetricsReportingEnabled** habilita a geração de relatórios de dados relacionados a falhas e de uso do Microsoft Edge para a Microsoft.

O Microsoft Edge coleta um conjunto de dados necessários para manter o produto atualizado, seguro e funcionando corretamente. Isso inclui informações básicas de conectividade e configuração do dispositivo do Microsoft Edge sobre o consentimento de coleta de dados atual, a versão do aplicativo e o estado da sua instalação do Microsoft Edge. Esse conjunto de dados pode ser desativado desabilitando a política.

Habilite essa política para enviar relatórios de dados relacionados a falhas e uso para a Microsoft. Desabilite essa política para não enviar esses dados para a Microsoft. Em ambos os casos, os usuários não poderão alterar nem substituir a configuração.

Quando o Microsoft Edge estiver sendo executado no Windows 10:

- Se essa política não estiver configurada, o padrão do Microsoft Edge será a configuração de dados de diagnóstico do Windows.
- Se essa política estiver habilitada, o Microsoft Edge enviará dados de uso somente se a configuração de dados de diagnóstico do Windows estiver definida como **Avançada** ou **Completa**.
  - Se essa política estiver habilitada, o Microsoft Edge só enviará dados de uso se [SendSiteInfoToImproveServices](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sendsiteinfotoimproveservices) também estiver habilitada.
- Se essa política estiver desabilitada, o Microsoft Edge não enviará dados de uso. Os dados relacionados a falha são enviados com base na configuração de dados de diagnóstico do Windows. [Saiba mais sobre as configurações de Dados de diagnóstico do Windows:](https://go.microsoft.com/fwlink/?linkid=2099569).

Quando o Microsoft Edge estiver sendo executado no Windows 7, 8 e macOS:

- Se essa política não estiver configurada, o padrão do Microsoft Edge será a preferência do usuário.
-  Se essa política estiver habilitada, o Microsoft Edge só enviará dados de uso se [SendSiteInfoToImproveServices](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sendsiteinfotoimproveservices) também estiver habilitada.

### (PRETERIDA) Enviar informações de sites para aprimorar os serviços Microsoft

A política **SendSiteInformationToImproveServices** permite o envio de informações sobre sites visitados no Microsoft Edge para a Microsoft visando melhorar os produtos e serviços Microsoft, tais como a pesquisa.

Habilite essa política para enviar informações sobre os sites visitados no Microsoft Edge para a Microsoft. Desabilite essa política para não enviar informações sobre os sites visitados com o Microsoft Edge para a Microsoft. Em ambos os casos, os usuários não poderão alterar nem substituir a configuração.

Quando o Microsoft Edge estiver sendo executado no Windows 10:

- Se essa política não estiver configurada, o padrão do Microsoft Edge será a configuração de dados de diagnóstico do Windows.
- Se essa política estiver habilitada, o Microsoft Edge enviará informações dos sites visitados apenas se a configuração de dados de diagnóstico do Windows estiver definida como **Completa**.
  - Se essa política estiver habilitada, o Microsoft Edge só enviará dados de uso se [MetricsReportingEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#metricsreportingenabled) também estiver habilitada. 
- Se essa política estiver desabilitada, o Microsoft Edge não enviará informações dos sites visitados. Para [saber mais sobre as configurações de dados de diagnóstico do Windows](https://go.microsoft.com/fwlink/?linkid=2099569).

Quando o Microsoft Edge estiver sendo executado no Windows 7, 8 e macOS:

- Se essa política estiver habilitada, o Microsoft Edge só enviará dados de uso se [MetricsReportingEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#metricsreportingenabled) também estiver habilitada.
- Se essa política não estiver configurada, o padrão do Microsoft Edge será a preferência do usuário.

## Detalhes da implementação

Para dispositivos não Windows 10: 
- Se a política [DiagnosticData](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#diagnosticdata) estiver configurada, ela terá precedência sobre [MetricsReportingEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#metricsreportingenabled)  e [SendSiteInfoToImproveServices](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sendsiteinfotoimproveservices). 
- Se a política [DiagnosticData](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#diagnosticdata) não estiver configurada, o Microsoft Edge escutará [MetricsReportingEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#metricsreportingenabled)  e [SendSiteInfoToImproveServices](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sendsiteinfotoimproveservices).  

Para que os canais do Windows 10 entendam nossa implementação com a dependência da configuração de dados de diagnóstico do Windows, a tabela a seguir identifica se os dados de diagnóstico  **Obrigatórios** e **Opcionais** foram enviados à Microsoft.

| Configuração de dados de diagnóstico do Windows | Dados de diagnóstico necessários  | Dados de diagnóstico opcionais |
|---------------------------------|-----------------------------------------------|-----------------------------------------------------|
| Segurança                        | Não enviado                                      | Não enviado                                            |
| Básico                           | Enviado                                      | Não enviado                                            |
| Avançado                        | Enviado                                          | Não enviado                                            |
| Completo                            | Enviado                                          | Enviado                                                |

> [!IMPORTANT]
> O Microsoft Edge será compatível com **MetricsReportingEnabled**  e **SendSiteInfoToImproveServices** nas versões 86 – 88 do Microsoft Edge. Na versão 89 do Microsoft Edge, **MetricsReportingEnabled**  e **SendSiteInfoToImproveServices** não serão mais compatíveis e a versão usará **DiagnosticData** como padrão em plataformas não Windows 10 ou a política **Permitir Telemetria** para Windows 10.

## Opções adicionais da política de privacidade

Convém considerar as seguintes políticas de grupo relacionadas à privacidade de dados:

- Bloquear cookies em sites específicos
- Bloquear cookies de terceiros
- Configurar Não Rastrear
- Desabilitar o modo InPrivate

## Ver também

- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Políticas do Microsoft Edge](microsoft-edge-policies.md)
- [White paper de Privacidade do Microsoft Edge](https://docs.microsoft.com/microsoft-edge/privacy-whitepaper)
