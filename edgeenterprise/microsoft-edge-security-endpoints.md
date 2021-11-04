---
title: Lista de permissões para pontos de extremidade do Microsoft Edge
ms.author: kvice
author: dan-wesley
manager: srugh
ms.date: 11/02/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Lista de permissões para pontos de extremidade do Microsoft Edge
ms.openlocfilehash: 9e6a87290f2f73ba11bc98eecd3aa693c35b5ace
ms.sourcegitcommit: 3e155a4395ae3a2ae478eb4b52c436b1c1f2e5db
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2021
ms.locfileid: "12155205"
---
# <a name="allow-list-for-microsoft-edge-endpoints"></a>Lista de permissões para pontos de extremidade do Microsoft Edge

O Microsoft Edge requer conectividade com a Internet para dar suporte aos recursos. Este artigo identifica as URLs de domínio que você precisa adicionar à Lista de permissões para garantir a comunicação por meio de firewalls e outros mecanismos de segurança.

> [!NOTE]
> Isso se aplica ao Microsoft Edge versão 77 ou posterior.

## <a name="domain-urls-to-allow"></a>URLs de domínio a serem permitidas

Permita as URLs de domínio a seguir para o Microsoft Edge.

### <a name="update-service"></a>Serviço de Atualização

O serviço que o Microsoft Edge usa para verificar se há novas atualizações.

- `https://msedge.api.cdp.microsoft.com`

### <a name="experimentation-and-configuration-service"></a>Serviço Experimentação e Configuração

- `https://config.edge.skype.com`

### <a name="download-locations-for-microsoft-edge"></a>Locais de download para o Microsoft Edge

Locais de onde o Microsoft Edge pode ser baixado durante uma instalação inicial ou quando uma atualização está disponível. O local de download é determinado pelo Serviço de Atualização.

#### <a name="http"></a>HTTP

- `http://msedge.f.tlu.dl.delivery.mp.microsoft.com`
- `http://msedge.f.dl.delivery.mp.microsoft.com`
- `http://msedge.b.tlu.dl.delivery.mp.microsoft.com`
- `http://msedge.b.dl.delivery.mp.microsoft.com`

#### <a name="https"></a>HTTPS

- `https://msedge.sf.tlu.dl.delivery.mp.microsoft.com`
- `https://msedge.sf.dl.delivery.mp.microsoft.com`
- `https://msedge.sb.tlu.dl.delivery.mp.microsoft.com`
- `https://msedge.sb.dl.delivery.mp.microsoft.com`

  > [!TIP]
  > Para simplificar a lista de permissões para locais de download, é possível usar um curinga: `*.dl.delivery.mp.microsoft.com`

### <a name="download-locations-for-microsoft-edge-extensions"></a>Locais de download para Extensões do Microsoft Edge

Locais de onde as Extensões do Microsoft Edge podem ser baixadas durante uma instalação inicial ou quando uma atualização está disponível. O local de download é determinado pelo Serviço de Atualização.

#### <a name="http"></a>HTTP

- `http://msedgeextensions.f.tlu.dl.delivery.mp.microsoft.com`
- `http://msedgeextensions.f.dl.delivery.mp.microsoft.com`
- `http://msedgeextensions.b.tlu.dl.delivery.mp.microsoft.com`
- `http://msedgeextensions.b.dl.delivery.mp.microsoft.com`

#### <a name="https"></a>HTTPS

- `https://msedgeextensions.sf.tlu.dl.delivery.mp.microsoft.com`
- `https://msedgeextensions.sf.dl.delivery.mp.microsoft.com`
- `https://msedgeextensions.sb.tlu.dl.delivery.mp.microsoft.com`
- `https://msedgeextensions.sb.dl.delivery.mp.microsoft.com`

  > [!TIP]
  > Para simplificar a lista de permissões para locais de download, é possível usar um curinga: `*.dl.delivery.mp.microsoft.com`

### <a name="optionally-for-download-delivery-optimization"></a>Opcionalmente para a Otimização de Entrega de Downloads

Para obter informações sobre a otimização de entrega, consulte [Otimização de Entrega para atualizações do Windows 10](/windows/deployment/update/waas-delivery-optimization).

- Comunicação entre Cliente e Serviço: `*.do.dsp.mp.microsoft.com` (Porta HTTP 80, Porta HTTPS 443)
- Comunicação entre Clientes: a porta TCP 7680 deve estar aberta para o tráfego de entrada

### <a name="sync"></a>Sync

Esses pontos de extremidade gerenciam a leitura e a escrita de dados sincronizados, o gerenciamento de direitos para proteger os dados e a notificação do navegador quando novos dados de sincronização estiverem disponíveis.

- Pontos de extremidade do serviço de sincronização do Microsoft Edge:

  - `https://edge-enterprise.activity.windows.com`
  - `https://edge.activity.windows.com`

- Pontos de extremidade da Proteção de Informações do Azure:

  - `https://api.aadrm.com` (para a maioria dos locatários)
  - `https://api.aadrm.de` (para locatários na Alemanha)
  - `https://api.aadrm.cn` (para locatários na China)

- [Pontos de extremidade do Serviço de Notificação do Windows](/windows/uwp/design/shell/tiles-and-notifications/firewall-allowlist-config)

### <a name="cloud-site-list-management"></a>Gerenciamento de lista de sites na nuvem

O serviço que Microsoft Edge usa para baixar a lista de sites hospedado na nuvem para o modo Internet Explorer (IE). Para obter mais informações, consulte [Gerenciamento de Lista de Sites na Nuvem](https://aka.ms/CloudSiteList)

- `https://edge.microsoft.com/`

## <a name="other-browser-support-services"></a>Outros serviços de suporte do navegador

Fornecem metadados para recursos do navegador, como proteção contra rastreamento, listas de certificados revogados e outras atualizações de componentes do navegador. Fornecem dicionários de verificação ortográfica e listas de bloqueio de anúncios para download. Fornecem serviços para dar suporte a recursos do navegador como coleções, autopreenchimento e repositório de extensões.

- `http://edge.microsoft.com/`
- `https://edge.microsoft.com/`

## <a name="see-also"></a>Consulte também

- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Página de aterrissagem da documentação do Microsoft Edge](./index.yml)
- [Gerenciar pontos de extremidade de conexão do Windows 10 Enterprise, versão 1903](/windows/privacy/manage-windows-1903-endpoints)