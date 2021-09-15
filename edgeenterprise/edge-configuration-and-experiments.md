---
title: Configurações e experimentação do Microsoft Edge
ms.author: kvice
author: dan-wesley
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Configurações e experimentação do Microsoft Edge
ms.openlocfilehash: 1ebfe5fc1da107aa7e9e20b629f14aff468bdd6d
ms.sourcegitcommit: 8968f3107291935ed9adc84bba348d5f187eadae
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/12/2021
ms.locfileid: "11978562"
---
# <a name="microsoft-edge-configurations-and-experimentation"></a>Configurações e experimentação do Microsoft Edge

Este artigo descreve a interação entre o Microsoft Edge e o ECS (Experimentation and Configuration Service). O Microsoft Edge se comunica com esse serviço para solicitar e receber tipos diferentes de carga. Essas cargas incluem configurações, distribuições de recursos e experimentos.

> [!IMPORTANT]
> Certifique-se de que os clientes possam acessar o `https://config.edge.skype.com` para que as cargas possam ser recebidas.

> [!NOTE]
> Isso aplica-se ao Microsoft Edge versão 77 ou posterior.

## <a name="configurations"></a>Configurações

As configurações são a carga que se destina a garantir a integridade, a segurança e a conformidade de privacidade do produto, e devem ter o mesmo valor para todos os usuários (com base em plataformas e canais). Isso pode ser a habilitação de um sinalizador de recurso para uma ação de domínio e também pode ser usado para desabilitar um sinalizador de recurso no caso de um bug.

## <a name="controlled-feature-rollout"></a>Distribuição Controlada de Recursos

A Distribuição Controlada de Recursos (CFR) é um procedimento para aumentar lentamente o tamanho do grupo de usuários que recebe um recurso. Ao distribuir um novo recurso para um subconjunto da população de usuários selecionado aleatoriamente, será possível comparar os comentários do usuário com um grupo de controles do mesmo tamanho, sem o recurso de medir o impacto do recurso.

## <a name="experiments"></a>Experimentos

Os builds do Microsoft Edge têm recursos e funcionalidades que ainda estão em desenvolvimento ou são experimentais. Os Experimentos são como a CFR, mas o tamanho do grupo de usuários é muito menor para testar o novo conceito. Esses recursos ficam ocultos por padrão até que o recurso seja distribuído ou o experimento seja concluído. Os sinalizadores de experimento são usados para habilitar e desabilitar esses recursos.

## <a name="about-the-ecs"></a>Sobre o ECS

Em todos os cenários anteriores, o serviço fornece os valores de sinalizador de recurso para o cliente do navegador para que eles possam ser aplicados. Dependendo da atualização, as configurações são aplicadas imediatamente ou quando o usuário reinicia o navegador.

A interação do Microsoft Edge com esse serviço é controlada por configurações na política [ExperimentationAndConfigurationServiceControl](./microsoft-edge-policies.md#experimentationandconfigurationservicecontrol). Você pode definir as configurações de política para:

- Recuperar somente configurações
- Recuperar configurações e experimentos
- Desabilitar a comunicação com o serviço

  > [!CAUTION]
  > Se você desabilitar as comunicações com o serviço, isso afetará a capacidade da Microsoft de responder a um bug grave de maneira oportuna.

## <a name="see-also"></a>Consulte também

- [Página de aterrissagem do Microsoft Edge Enterprise](https://www.microsoftedgeinsider.com/enterprise)
- [Página de aterrissagem da documentação do Microsoft Edge](./index.yml)