---
title: Bloquear o acesso a contas de consumidor
ms.author: v-danwesley
author: dan-wesley
manager: collw
ms.date: 06/16/2022
audience: ITPro
ms.topic: conceptual
ms.custom: generated
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Bloquear o acesso a contas de consumidor
ms.openlocfilehash: 8a3856fbd87f5a4686a10ae8b0547453088d0b18
ms.sourcegitcommit: 3b050349583c29490bbf4505744d271a2478606f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/16/2022
ms.locfileid: "12595958"
---
# <a name="block-access-to-consumer-accounts"></a>Bloquear o acesso a contas de consumidor

Você pode impedir que os usuários se conectarem aos serviços do Google usando contas diferentes das contas que você forneceu a eles. Os motivos para bloquear o acesso são impedir que os usuários em sua rede corporativa usem suas contas pessoais do Gmail ou acessem uma conta gerenciada do Google de outro domínio.

Os usuários podem ver a seguinte mensagem quando você bloqueia o acesso a contas de consumidor: "Esta conta não tem permissão para entrar nessa rede".

> [!NOTE]
> Este artigo se aplica Microsoft Edge versão estável 104 ou posterior.

## <a name="what-does-this-policy-do"></a>O que essa política faz?

Essa política faz com que o cabeçalho **X-GoogApps-Allowed-Domains:** seja acrescentado a todas as solicitações HTTP e HTTPS para todos os google.com domínios. Esse cabeçalho é seguido por uma lista separada por vírgulas com os nomes de domínio permitidos.

Exemplo: `X-GoogApps-Allowed-Domains: mydomain1.com, mydomain2.com`

> [!NOTE]
> Microsoft Edge, que é criado Chromium, está herdando essa política upstream do projeto Chromium código aberto.

## <a name="configure-policy-settings"></a>Definir configurações de política

Para saber como definir as Microsoft Edge de política no Intune, consulte Definir configurações Microsoft Edge política com [Microsoft Intune.](configure-edge-with-intune.md)

## <a name="content-license"></a>Licença de conteúdo

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e compartilhado pela Chromium.org e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional](http://creativecommons.org/licenses/by/4.0/). A página original pode ser encontrada [aqui](https://support.google.com/a/answer/1668854).

<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br />Esse trabalho é licenciado sob uma <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons</a>.
