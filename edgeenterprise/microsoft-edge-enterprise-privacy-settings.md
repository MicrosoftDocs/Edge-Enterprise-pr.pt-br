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
# Configurar as políticas do Microsoft Edge para oferecer suporte à privacidade da empresa

A Microsoft está comprometida em fornecer às empresas as informações e os controles necessários para fazer escolhas sobre a coleta de dados no Microsoft Edge.

## Visão geral

Por padrão, o Microsoft Edge implantado nas plataformas não Windows não envia dados de diagnóstico ou informações do site para a Microsoft. Por padrão, quando o Microsoft Edge é implantado no Windows 10, os dados de diagnóstico são enviados com base na [Configuração de dados de diagnóstico do Windows](https://go.microsoft.com/fwlink/?linkid=2099569) dos usuários.

Você pode configurar como o Microsoft Edge realiza a coleta de dados da sua organização com as seguintes políticas de grupo:

- [MetricsReportingEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#metricsreportingenabled) - habilita o uso e os relatórios de dados relacionados a falhas.
- [SendSiteInfoToImproveServices](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sendsiteinfotoimproveservices) - envia informações do site para melhorar os serviços da Microsoft.

## Definir configurações de política

Antes começar, baixe e use o modelo de política do Microsoft Edge mais recente (para obter mais informações, consulte [Configurar o Microsoft Edge](configure-microsoft-edge.md)).

### Habilite a geração de relatórios de dados relacionados a falhas e uso

Esta política habilita a geração de relatórios de dados relacionados a falhas e uso do Microsoft Edge para a Microsoft.

O Microsoft Edge coleta um conjunto de dados que são necessários para manter o produto seguro, atualizado e funcionando corretamente. Isso inclui informações básicas de conectividade e configuração do dispositivo do Microsoft Edge sobre o consentimento de coleta de dados atual, a versão do aplicativo e o estado da sua instalação do Microsoft Edge. Esse conjunto de dados pode ser desativado desabilitando a política.

Habilite essa política para enviar relatórios de dados relacionados a falhas e uso para a Microsoft. Desabilite essa política para não enviar esses dados para a Microsoft. Em ambos os casos, os usuários não poderão alterar nem substituir a configuração.

Quando o Microsoft Edge estiver sendo executado no Windows 10:

- Se essa política não estiver configurada, o padrão do Microsoft Edge será a configuração de dados de diagnóstico do Windows.
- Se essa política estiver habilitada, o Microsoft Edge enviará dados de uso somente se a configuração de dados de diagnóstico do Windows estiver definida como **Avançada** ou **Completa**.
- Se essa política estiver desabilitada, o Microsoft Edge não enviará dados de uso. Os dados relacionados a falha são enviados com base na configuração de dados de diagnóstico do Windows. [Saiba mais sobre as configurações de Dados de diagnóstico do Windows:](https://go.microsoft.com/fwlink/?linkid=2099569).

Quando o Microsoft Edge estiver sendo executado no Windows 7, 8 e macOS:

- Se essa política não estiver configurada, o padrão do Microsoft Edge será a preferência do usuário.

### Envie as informações de sites para melhorar os serviços Microsoft

Essa política permite o envio de informações sobre sites visitados no Microsoft Edge para a Microsoft visando melhorar os produtos e serviços Microsoft, tais como a pesquisa.

Habilite essa política para enviar informações sobre os sites visitados no Microsoft Edge para a Microsoft. Desabilite essa política para não enviar informações sobre os sites visitados com o Microsoft Edge para a Microsoft. Em ambos os casos, os usuários não poderão alterar nem substituir a configuração.

Quando o Microsoft Edge estiver sendo executado no Windows 10:

- Se essa política não estiver configurada, o padrão do Microsoft Edge será a configuração de dados de diagnóstico do Windows.
- Se essa política estiver habilitada, o Microsoft Edge enviará informações dos sites visitados apenas se a configuração de dados de diagnóstico do Windows estiver definida como **Completa**.
- Se essa política estiver desabilitada, o Microsoft Edge não enviará informações dos sites visitados. Para [saber mais sobre as configurações de dados de diagnóstico do Windows](https://go.microsoft.com/fwlink/?linkid=2099569).

Quando o Microsoft Edge estiver sendo executado no Windows 7, 8 e macOS:

- Se essa política não estiver configurada, o padrão do Microsoft Edge será a preferência do usuário.

## Detalhes da implementação

Para que os canais do Windows 10 entendam nossa implementação com a dependência da configuração de dados de diagnóstico do Windows, a tabela a seguir descreve nossa configuração se **Habilitar relatórios de uso e dados relacionados a falhas** e **Enviar informações do site para melhorar os serviços Microsoft** não estiverem configurados.

| Configuração de dados de diagnóstico do Windows | Habilite a geração de relatórios de dados relacionados a falhas e uso | Envie as informações de sites para melhorar os serviços Microsoft |
|---------------------------------|-----------------------------------------------|-----------------------------------------------------|
| Segurança                        | Não enviado                                      | Não enviado                                            |
| Básico                           | Não enviado                                      | Não enviado                                            |
| Avançado                        | Enviado                                          | Não enviado                                            |
| Completo                            | Enviado                                          | Enviado                                                |

Se as configurações dos canais Windows 10 não forem configuradas de acordo com esta tabela, retornaremos à menor configuração de coleta de dados.

Por exemplo:

- Você define a política "Habilitar relatórios de dados de uso e de falha" como **Habilitada**, mas a configuração de dados de Diagnóstico do Windows está definida como **Básica**. Não enviaremos dados de uso e relacionados a falhas.
- Você define a diretiva "Enviar informações do site para melhorar os serviços da Microsoft" como **Desabilitada**, mas a configuração de dados de Diagnóstico do Windows está definida como **Completa**. Não enviaremos informações dos sites visitados.

A implementação correta das configurações anteriores é definir a política "Habilitar relatórios de uso e dados relacionados a falhas" como **Habilitada** e definir a configuração de dados de diagnóstico do Windows como **Melhorada** ou**Completa**. 

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
