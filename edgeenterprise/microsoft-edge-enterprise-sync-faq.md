---
title: Perguntas frequentes sobre a sincronização empresarial do Microsoft Edge
ms.author: collw
author: dan-wesley
manager: silvanam
ms.date: 05/16/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Perguntas frequentes sobre a Microsoft Edge enterprise.
ms.openlocfilehash: ac32e0c375651aac9c8ed3ae8d1de9e7b675df95
ms.sourcegitcommit: d384115fb2197261ee8fa3b0bdbcb7455527616f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/17/2022
ms.locfileid: "12517566"
---
# <a name="microsoft-edge-enterprise-sync-faq"></a>Perguntas frequentes sobre a sincronização empresarial do Microsoft Edge

Este artigo responde a perguntas frequentes sobre a sincronização empresarial do Microsoft Edge versão 77 ou posterior.

## <a name="security-and-serverdata-compliance"></a>Segurança e conformidade de servidor/dados

### <a name="is-the-synced-data-encrypted"></a>Os dados sincronizados estão criptografados?

Sim, os dados são criptografados em transporte usando o TLS 1.2 ou superior. Todos os tipos de dados também são criptografados como descansar no serviço da Microsoft usando o AES128. Todos os tipos de dados, exceto os dados usados para sincronização de histórico e guia aberta, são criptografados antes de deixar o dispositivo do usuário com chaves gerenciadas por meio da política de Proteção de Informações do [Azure](./microsoft-edge-policies.md#restrictsignintopattern).

### <a name="why-isnt-there-more-client-side-encryption-on-open-tab-and-history-data"></a>Por que não há mais criptografia do lado do cliente nos dados da guia aberta e do histórico?

Para reduzir o uso de recursos nos dispositivos do usuário final, os dados do histórico são gerados no lado do servidor com base nos dados de roaming da guia aberta. Esse processo não seria possível com a criptografia do lado do cliente desses dados. Para desabilitar a guia aberta e a sincronização do histórico, aplique as políticas [SavingBrowserHistoryDisabled](./microsoft-edge-policies.md#savingbrowserhistorydisabled) ou [SyncTypesListDisabled](./microsoft-edge-policies.md#synctypeslistdisabled) .

### <a name="can-tenant-admins-bring-their-own-key"></a>Os administradores de locatários podem ter suas próprias chaves?

Sim, pela [Proteção de informações do Azure](https://azure.microsoft.com/services/information-protection/).

### <a name="where-is-microsoft-edge-sync-data-stored"></a>Onde os dados sincronizados são armazenados no Microsoft Edge?

Os dados sincronizados para Azure AD contas são armazenados em servidores seguros de acordo com a ID do locatário. Por exemplo, os dados de um locatário registrado nos Estados Unidos são armazenados em servidores localizados geograficamente nessa região e aproveitam a mesma solução de armazenamento usada pelos aplicativos do Office.

### <a name="does-the-data-ever-leave-microsofts-cloud-aside-from-syncing-to-microsoft-edge"></a>Os dados deixam a nuvem da Microsoft, além de sincronizar com o Microsoft Edge?

Não.

### <a name="what-terms-of-service-does-enterprise-sync-fall-under"></a>Em que termos de serviço a sincronização empresarial se encaixa?

Os termos de serviço para Microsoft Edge sincronização se enquadram na licença de software da Microsoft que pode ser Microsoft Edge em  *edge://terms*. A sua assinatura e os termos de serviço do Azure AD estão, em última análise, em [Termos de serviço on-line](https://www.microsoft.com/licensing/product-licensing/products)da Microsoft.

### <a name="does-microsoft-edge-support-government-community-cloud-gcc-high-compliance"></a>O Microsoft Edge dá suporte á conformidade do Government Community Cloud (GCC) High?

Não atualmente. A sincronização do Microsoft Edge está desabilitada para os clientes na nuvem do GCC High.

## <a name="applying-sync"></a>Aplicar Sincronização

### <a name="why-isnt-microsoft-edge-sync-supported-in-all-microsoft-365-subscriptions"></a>Por que não há suporte Microsoft Edge sincronização em todas as Microsoft 365 assinaturas?

Enterprise sincronização depende da Proteção de Informações do [Azure](https://azure.microsoft.com/services/information-protection/), que não está disponível para todas as Microsoft 365 assinaturas.

### <a name="is-microsoft-edge-sync-based-on-enterprise-state-roaming"></a>A sincronização do Microsoft Edge é baseada no Enterprise State Roaming?

Não. O ESR pode ser usado para habilitar a sincronização, mas Microsoft Edge sincronização não faz parte do ESR. Para obter mais informações, consulte [Sincronização do Microsoft Edge](/DeployEdge/microsoft-edge-enterprise-sync) e [Microsoft Edge e Enterprise State Roaming](/DeployEdge/microsoft-edge-enterprise-state-roaming).

### <a name="will-microsoft-edge-ever-support-syncing-between-microsoft-edge-and-ie"></a>O Microsoft Edge oferecerá suporte para sincronização entre o Microsoft Edge e o IE?

Não há planos para dar suporte a essa sincronização. Se você ainda precisar do IE no seu ambiente para oferecer suporte aos aplicativos herdados, considere o nosso [novo modo do IE](./edge-ie-mode.md).

### <a name="will-microsoft-edge-sync-with-microsoft-edge-legacy"></a>O Microsoft Edge será sincronizado com o Microsoft Edge herdado?

Não. Acreditamos que a conexão destes dois ecossistemas comprometerá a confiabilidade da sincronia no Microsoft Edge. Garantiremos que os dados existentes são migrados para o Microsoft Edge. Os usuários também poderão importar dados do navegador de sua escolha, o que também significa que o Microsoft Edge não terá uma maneira de sincronizar com o IE.

## <a name="managing-sync"></a>Gerenciar Sincronização

### <a name="is-it-possible-to-stop-my-users-from-syncing-with-a-personal-tenant"></a>É possível impedir que os meus usuários sincronizem com um locatário pessoal?

Não diretamente, mas você pode determinar quais perfis podem entrar no Microsoft Edge usando a política [RestrictSigninToPattern](./microsoft-edge-policies.md#restrictsignintopattern).

## <a name="see-also"></a>Ver também

- [Sincronização do Microsoft Edge Enterprise](microsoft-edge-enterprise-sync.md)
- [Microsoft Edge e Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md)
- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)