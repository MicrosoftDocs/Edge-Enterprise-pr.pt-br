---
title: Distribuições progressivas para atualizações do canal estável do Microsoft Edge
ms.author: aguta
author: dan-wesley
manager: srugh
ms.date: 05/21/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Distribuições progressivas para atualizações do canal estável do Microsoft Edge
ms.openlocfilehash: 5b0d2f58318b10538d0470b644d346b5b9b9489b
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979090"
---
# Distribuições progressivas para atualizações do canal estável do Microsoft Edge

A partir do lançamento do Microsoft Edge 83, realizaremos distribuições progressivas de atualizações principais para o canal estável do Microsoft Edge durante alguns dias. Essa distribuição progressiva permite monitorar as atualizações e atualizar o navegador com segurança em toda a organização.

> [!NOTE]
> Isso se aplica ao canal estável do Microsoft Edge versão 83 ou posterior.

## Por que precisamos de uma distribuição progressiva?

Ao monitorar a integridade das atualizações e implementar as atualizações durante esse período, podemos limitar o impacto dos problemas que podem ocorrer com a nova atualização. Com o Microsoft Edge versão 83, as distribuições progressivas serão habilitadas para todas as versões do Windows 7, Windows 8 e 8.1 e Windows 10 no Microsoft Edge. Vamos dar suporte ao Microsoft Edge no Mac assim que estiver pronto.

## Como as atualizações funcionarão?

Todas as instalações do Microsoft Edge recebem um valor de atualização. Quando começarmos a distribuição progressiva, você verá a atualização quando o valor no seu dispositivo estiver dentro do intervalo de valores de atualização. À medida que a distribuição progride (dentro de alguns dias), todos os usuários eventualmente receberão a atualização. As atualizações de navegador com correções de segurança críticas terão uma distribuição mais rápida do que as atualizações que não possuem correções de segurança críticas. Isso é feito para garantir a proteção contra vulnerabilidades.

## Como isso afeta as empresas?

Os artefatos do Microsoft Edge são distribuídos para empresas usando vários mecanismos, como o Microsoft Intune, o WSUS (serviço de atualização do Windows Server) e o Gerenciador de Configurações. Essas ferramentas de implantação se comportam de forma diferente com relação à distribuição progressiva:

- As empresas que gerenciam a distribuição por meio do Microsoft Intune estão registradas para as atualizações automáticas. A distribuição progressiva é usada, e todos os usuários verão uma atualização em alguns dias.
- As empresas que gerenciam a distribuição por meio do WSUS (Windows Server Update Services) ou do Gerenciador de Configurações não estão registradas para as atualizações automáticas. Os administradores gerenciam e aplicam as atualizações que estarão disponíveis desde o início. A distribuição progressiva não afeta esse processo.

Compartilhe seus comentários por meio da voz do usuário, do botão de comentários no aplicativo ou abaixo nos comentários, caso tenha dúvidas ou questões.

## Consulte também

- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
