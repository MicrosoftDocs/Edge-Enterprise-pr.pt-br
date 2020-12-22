---
title: Redefinir dados do Microsoft Edge
ms.author: scottbo
author: dan-wesley
manager: silvanam
ms.date: 12/21/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Como redefinir dados do Microsoft Edge na nuvem
ms.openlocfilehash: 638abe5dc80aafa64d05bccd4a0f5542fa13860c
ms.sourcegitcommit: 51f43d220503547f24b56ff3dda5373c5aca6b57
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/21/2020
ms.locfileid: "11238016"
---
# Redefinir dados do Microsoft Edge na nuvem

Este artigo descreve as etapas para redefinir os dados do Microsoft Edge na nuvem.

> [!NOTE]
> Este artigo se aplica ao Microsoft Edge versão 88 ou posterior, a menos que indicado de outra forma.

## Visão geral

Há situações em que você vai precisar redefinir seus dados do Microsoft Edge na nuvem. Por exemplo, você deseja sincronizar seus dados, mas o Microsoft Edge informa que não é possível sincronizá-los. Ou talvez você queira certificar-se de que seus dados foram removidos da nuvem da Microsoft. Em ambos os casos, o Microsoft Edge permite que você execute uma redefinição de dados na nuvem.

## Fazer backup de seus favoritos

Antes de executar uma redefinição, recomendamos que você faça backup de seus favoritos. Use as etapas a seguir para fazer backup de seus favoritos.

1. No Microsoft Edge, selecione **Configurações e mais > Favoritos > Mais opções > Exportar favoritos**.
2. Escolha o arquivo no qual você deseja salvar seus favoritos. Você pode digitar seu próprio nome de arquivo ou usar o nome que o Microsoft Edge fornece por padrão, "favorites_month_day_year.html" como um nome de arquivo. Por exemplo, "favorites_12_17_20.html". Se precisar restaurar seus favoritos mais tarde, você poderá fazê-lo a partir desse arquivo.
3. Clique em **Salvar**.

## Executar redefinição para corrigir um problema de sincronização

Se o Microsoft Edge relatar que não pode sincronizar seus dados, e sugerir que eles sejam redefinidos, execute uma redefinição para corrigir o problema.

Use as etapas a seguir para executar uma redefinição.

1. Primeiro, certifique-se de que você está desconectado do Microsoft Edge em todos os seus dispositivos, incluindo seus dispositivos móveis, exceto o dispositivo em que você está executando a redefinição. Para sair do Microsoft Edge, selecione **Configurações e mais > Configurações > Sair**. Ao sair, não selecione a opção para limpar favoritos, configurações e etc. do seu dispositivo local.
2. Depois de sair de todos os outros dispositivos, abra o Microsoft Edge no desktop. **Selecione Configurações e mais > Sincronizar > Redefinir sincronização**. Na caixa de diálogo resultante, escolha retomar a sincronização após redefinir os dados e, em seguida, selecione **Redefinir**.

## Executar uma redefinição para remover seus dados da nuvem da Microsoft

Se você quiser remover seus dados da nuvem da Microsoft, use as etapas a seguir para fazer uma redefinição.

1. Interrompa a sincronização nos dispositivos, exceto no dispositivo no qual está executando a redefinição.  No Microsoft Edge, selecione **Configurações e mais > Configurações > Sincronizar > Desativar sincronização**.  
2. Depois de interromper a sincronização, selecione **Configurações e mais > Sincronizar > Redefinir sincronização**. Na caixa de diálogo resultante, **não** escolha retomar a sincronização após redefinir os dados. Selecione **Redefinir**.

## O que esperar durante e após uma redefinição de dados

Uma redefinição de dados pode levar de alguns segundos a alguns minutos, dependendo da quantidade de dados armazenados na nuvem da Microsoft. Em alguns casos, você poderá ver uma mensagem informando que não foi possível concluir uma redefinição e uma sugestão para redefinir novamente. Nesse caso, aguarde algumas horas e tente redefinir os dados novamente. Se ainda não conseguir redefinir seus dados, entre em contato com o Suporte do Microsoft Edge.

Depois que uma reinicialização de dados for concluída com êxito, os dados serão sincronizados novamente a partir do seu dispositivo se você optar por retomar a sincronização após a redefinição. Você precisará se conectar novamente nos outros dispositivos se quiser sincronizar nesses dispositivos. No entanto, se você não escolheu retomar a sincronização, seus dados do Microsoft Edge serão removidos da nuvem e não serão mais sincronizados.

## Confira também

- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Sincronização do Microsoft Edge Enterprise](microsoft-edge-enterprise-sync.md)