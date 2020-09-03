---
title: Lista de permissões para pontos de extremidade do Microsoft Edge
ms.author: kvice
author: dan-wesley
manager: srugh
ms.date: 06/09/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Lista de permissões para pontos de extremidade do Microsoft Edge
ms.openlocfilehash: 76186524a708861432199d5da7eec7573ebecb96
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979163"
---
# Lista de permissões para pontos de extremidade do Microsoft Edge

O Microsoft Edge requer conectividade com a Internet para dar suporte aos recursos. Este artigo identifica as URLs de domínio que você precisa adicionar à Lista de permissões para garantir a comunicação por meio de firewalls e outros mecanismos de segurança.

> [!NOTE]
> Isso se aplica ao Microsoft Edge versão 77 ou posterior.

## URLs de domínio a serem permitidas

Permita as URLs de domínio a seguir para o Microsoft Edge.

### Serviço de Atualização

O serviço que o Microsoft Edge usa para verificar se há novas atualizações.

- `https://msedge.api.cdp.microsoft.com`

### Serviço Experimentação e Configuração

- `https://config.ecs.skype.com`

### Locais de download para o Microsoft Edge

Locais de onde o Microsoft Edge pode ser baixado durante uma instalação inicial ou quando uma atualização está disponível. O local de download é determinado pelo Serviço de Atualização.

#### HTTP

- `http://msedge.f.tlu.dl.delivery.mp.microsoft.com`
- `http://msedge.f.dl.delivery.mp.microsoft.com`
- `http://msedge.b.tlu.dl.delivery.mp.microsoft.com`
- `http://msedge.b.dl.delivery.mp.microsoft.com`

#### HTTPS

- `https://msedge.sf.tlu.dl.delivery.mp.microsoft.com`
- `https://msedge.sf.dl.delivery.mp.microsoft.com`
- `https://msedge.sb.tlu.dl.delivery.mp.microsoft.com`
- `https://msedge.sb.dl.delivery.mp.microsoft.com`

  > [!TIP]
  > Para simplificar a lista de permissões para locais de download, é possível usar um curinga: `*.dl.delivery.mp.microsoft.com`

### Locais de download para Extensões do Microsoft Edge

Locais de onde as Extensões do Microsoft Edge podem ser baixadas durante uma instalação inicial ou quando uma atualização está disponível. O local de download é determinado pelo Serviço de Atualização.

#### HTTP

- `http://msedgeextensions.f.tlu.dl.delivery.mp.microsoft.com`
- `http://msedgeextensions.f.dl.delivery.mp.microsoft.com`
- `http://msedgeextensions.b.tlu.dl.delivery.mp.microsoft.com`
- `http://msedgeextensions.b.dl.delivery.mp.microsoft.com`

#### HTTPS

- `https://msedgeextensions.sf.tlu.dl.delivery.mp.microsoft.com`
- `https://msedgeextensions.sf.dl.delivery.mp.microsoft.com`
- `https://msedgeextensions.sb.tlu.dl.delivery.mp.microsoft.com`
- `https://msedgeextensions.sb.dl.delivery.mp.microsoft.com`

  > [!TIP]
  > Para simplificar a lista de permissões para locais de download, é possível usar um curinga: `*.dl.delivery.mp.microsoft.com`

### Opcionalmente para a Otimização de Entrega de Downloads

Para obter informações sobre a otimização de entrega, consulte [Otimização de Entrega para atualizações do Windows 10](https://aka.ms/waas-do).

- Comunicação entre Cliente e Serviço: `*.do.dsp.mp.microsoft.com` (Porta HTTP 80, Porta HTTPS 443)
- Comunicação entre Clientes: a porta TCP 7680 deve estar aberta para o tráfego de entrada

### Sync

Esses pontos de extremidade gerenciam a leitura e a escrita de dados sincronizados, o gerenciamento de direitos para proteger os dados e a notificação do navegador quando novos dados de sincronização estiverem disponíveis.

- Pontos de extremidade do serviço de sincronização do Edge:

  - `https://enterprise.edge.activity.windows.com`
  - `https://edge.activity.windows.com`

- Pontos de extremidade da Proteção de Informações do Azure:

  - `https://api.aadrm.com` (para a maioria dos locatários)
  - `https://api.aadrm.de` (para locatários na Alemanha)
  - `https://api.aadrm.cn` (para locatários na China)

- [Pontos de extremidade do Serviço de Notificação do Windows](https://docs.microsoft.com/windows/uwp/design/shell/tiles-and-notifications/firewall-allowlist-config)

## Outros serviços de suporte do navegador

Fornecem metadados para recursos do navegador, como proteção contra rastreamento, listas de certificados revogados e outras atualizações de componentes do navegador. Fornecem dicionários de verificação ortográfica e listas de bloqueio de anúncios para download. Fornecem serviços para dar suporte a recursos do navegador como coleções, autopreenchimento e repositório de extensões.

- `http://edge.microsoft.com/`
- `https://edge.microsoft.com/`

## Consulte também

- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Página de aterrissagem da documentação do Microsoft Edge](https://docs.microsoft.com/DeployEdge/)
- [Gerenciar pontos de extremidade de conexão do Windows 10 Enterprise, versão 1903](https://docs.microsoft.com/windows/privacy/manage-windows-1903-endpoints)
