---
title: Distribuições progressivas para atualizações do canal estável do Microsoft Edge
ms.author: aguta
author: dan-wesley
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Distribuições progressivas para atualizações do canal estável do Microsoft Edge
ms.openlocfilehash: bdcefdc118125d67057fa77513bd732cff6882e3
ms.sourcegitcommit: 8968f3107291935ed9adc84bba348d5f187eadae
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/12/2021
ms.locfileid: "11978737"
---
# <a name="progressive-rollouts-for-microsoft-edge-stable-channel-updates"></a>Distribuições progressivas para atualizações do canal estável do Microsoft Edge

A partir do lançamento do Microsoft Edge 83, realizaremos distribuições progressivas de atualizações principais para o canal estável do Microsoft Edge durante alguns dias. Essa distribuição progressiva permite monitorar as atualizações e atualizar o navegador com segurança em toda a organização.

> [!NOTE]
> Isso se aplica ao canal estável do Microsoft Edge versão 83 ou posterior.

## <a name="why-do-we-need-progressive-rollout"></a>Por que precisamos de uma distribuição progressiva?

Ao monitorar a integridade das atualizações e implementar as atualizações durante esse período, podemos limitar o impacto dos problemas que podem ocorrer com a nova atualização. Com o Microsoft Edge versão 83, as distribuições progressivas serão habilitadas para todas as versões do Windows 7, Windows 8 e 8.1 e Windows 10 no Microsoft Edge. Vamos dar suporte ao Microsoft Edge no Mac assim que estiver pronto.

## <a name="how-will-the-updates-work"></a>Como as atualizações funcionarão?

Todas as instalações do Microsoft Edge recebem um valor de atualização. Quando começarmos a distribuição progressiva, você verá a atualização quando o valor no seu dispositivo estiver dentro do intervalo de valores de atualização. À medida que a distribuição progride (dentro de alguns dias), todos os usuários eventualmente receberão a atualização. As atualizações de navegador com correções de segurança críticas terão uma distribuição mais rápida do que as atualizações que não possuem correções de segurança críticas. Isso é feito para garantir a proteção contra vulnerabilidades.

## <a name="how-does-this-affect-enterprises"></a>Como isso afeta as empresas?

Os artefatos do Microsoft Edge são distribuídos para empresas usando vários mecanismos, como o Microsoft Intune, o WSUS (serviço de atualização do Windows Server) e o Gerenciador de Configurações. Essas ferramentas de implantação se comportam de forma diferente com relação à distribuição progressiva:

- As empresas que gerenciam a distribuição por meio do Microsoft Intune estão registradas para as atualizações automáticas. A distribuição progressiva é usada, e todos os usuários verão uma atualização em alguns dias.
- As empresas que gerenciam a distribuição por meio do WSUS (Windows Server Update Services) ou do Gerenciador de Configurações não estão registradas para as atualizações automáticas. Os administradores gerenciam e aplicam as atualizações que estarão disponíveis desde o início. A distribuição progressiva não afeta esse processo.

Compartilhe seus comentários por meio da voz do usuário, do botão de comentários no aplicativo ou abaixo nos comentários, caso tenha dúvidas ou questões.

## <a name="see-also"></a>Consulte também

- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
