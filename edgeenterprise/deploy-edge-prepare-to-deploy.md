---
title: Microsoft Edge em seu ambiente
ms.author: v-danwesley
author: dan-wesley
manager: tinad
ms.date: 05/26/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Microsoft Edge em seu ambiente
ms.openlocfilehash: 4c0622276a4ba93691a79d21779196c9603f2ff6
ms.sourcegitcommit: 3771634abdfd7d376778ad6ae10a385d5658b7d3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/27/2022
ms.locfileid: "12551788"
---
# <a name="microsoft-edge-in-your-environment"></a>Microsoft Edge em seu ambiente

Este artigo descreve como se preparar para implantar o Microsoft Edge quando o Versão Prévia do Microsoft Edge chegar ao fim do serviço.

De acordo com a [postagem do blog](https://aka.ms/EdgeLegacyEOS)da Equipe de Produto do Microsoft Edge, o suporte para o aplicativo de desktop Versão Prévia do Microsoft Edge terminará em 9 de Março de 2021. Quando você aplica a versão Update Tuesday (ou "B") em abril, ela remove a Versão Prévia do Microsoft Edge dos dispositivos que executam o Windows 10 RS4 até 20H1 e o substitui pelo Microsoft Edge.

## <a name="how-to-prepare"></a>Como preparar

Para se preparar para a instalação do Microsoft Edge em dispositivos Windows 10 RS4 a 20H1 com o lançamento da terça-feira de atualização em abril, recomendamos a leitura de [Planeje sua implantação do Microsoft Edge](deploy-edge-plan-deployment.md).

Depois de planejar sua implantação, use uma das abordagens a seguir para se preparar para implantar o Microsoft Edge.

- **Instale políticas de grupo para personalizar sua abordagem de atualização do Microsoft Edge**. Para obter mais informações, Consulte [Definir as configurações de política do Microsoft Edge no Windows](configure-microsoft-edge.md)e preste atenção especial ao material de referência[ da Política de Atualização](microsoft-edge-update-policies.md). Se você instalar políticas de grupo para gerenciar suas atualizações antes de instalar o lançamento da terça-feira de atualização de abril, o Microsoft Edge começará a respeitar sua política imediatamente. Se não houver nenhuma política de grupo instalada, o Microsoft Edge se atualizará automaticamente.

- **Remova o aplicativo de desktop Versão Prévia do Microsoft Edge antes da data de término do serviço em 9 de Março de 2021 e implante o Microsoft Edge**. Para Windows 10 RS4 a 20H1, você pode fazer isso usando as atualizações do Windows. Para obter mais informações, consulte [Implantar o Microsoft Edge com atualizações do Windows 10](deploy-edge-with-windows-10-updates.md).

## <a name="see-also"></a>Veja também

- [Página de destino do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Planejar sua implantação do Microsoft Edge](deploy-edge-plan-deployment.md)