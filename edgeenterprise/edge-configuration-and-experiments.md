---
title: Configurações e experimentação do Microsoft Edge
ms.author: kvice
author: dan-wesley
manager: srugh
ms.date: 02/20/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Configurações e experimentação do Microsoft Edge
ms.openlocfilehash: f66da4075c33c1f375dfb593c1a1bd2b4a139833
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979030"
---
# Configurações e experimentação do Microsoft Edge

Este artigo descreve a interação entre o Microsoft Edge e o ECS (Experimentation and Configuration Service). O Microsoft Edge se comunica com esse serviço para solicitar e receber tipos diferentes de carga. Essas cargas incluem configurações, distribuições de recursos e experimentos.

> [!IMPORTANT]
> Certifique-se de que os clientes possam acessar o `https://config.edge.skype.com` para que as cargas possam ser recebidas.

> [!NOTE]
> Isso aplica-se ao Microsoft Edge versão 77 ou posterior.

## Configurações

As configurações são a carga que se destina a garantir a integridade, a segurança e a conformidade de privacidade do produto, e devem ter o mesmo valor para todos os usuários (com base em plataformas e canais). Isso pode ser a habilitação de um sinalizador de recurso para uma ação de domínio e também pode ser usado para desabilitar um sinalizador de recurso no caso de um bug.

## Distribuição Controlada de Recursos

A Distribuição Controlada de Recursos (CFR) é um procedimento para aumentar lentamente o tamanho do grupo de usuários que recebe um recurso. Ao distribuir um novo recurso para um subconjunto da população de usuários selecionado aleatoriamente, será possível comparar os comentários do usuário com um grupo de controles do mesmo tamanho, sem o recurso de medir o impacto do recurso.

## Experimentos

Os builds do Microsoft Edge têm recursos e funcionalidades que ainda estão em desenvolvimento ou são experimentais. Os Experimentos são como a CFR, mas o tamanho do grupo de usuários é muito menor para testar o novo conceito. Esses recursos ficam ocultos por padrão até que o recurso seja distribuído ou o experimento seja concluído. Os sinalizadores de experimento são usados para habilitar e desabilitar esses recursos.

## Sobre o ECS

Em todos os cenários anteriores, o serviço fornece os valores de sinalizador de recurso para o cliente do navegador para que eles possam ser aplicados. Dependendo da atualização, as configurações são aplicadas imediatamente ou quando o usuário reinicia o navegador.

A interação do Microsoft Edge com esse serviço é controlada por configurações na política [ExperimentationAndConfigurationServiceControl](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#experimentationandconfigurationservicecontrol). Você pode definir as configurações de política para:

- Recuperar somente configurações
- Recuperar configurações e experimentos
- Desabilitar a comunicação com o serviço

  > [!CAUTION]
  > Se você desabilitar as comunicações com o serviço, isso afetará a capacidade da Microsoft de responder a um bug grave de maneira oportuna.

## Consulte também

- [Página de aterrissagem do Microsoft Edge Enterprise](https://www.microsoftedgeinsider.com/enterprise)
- [Página de aterrissagem da documentação do Microsoft Edge](https://docs.microsoft.com/DeployEdge/)
