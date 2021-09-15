---
title: Perguntas frequentes sobre a sincronização empresarial do Microsoft Edge
ms.author: collw
author: dan-wesley
manager: silvanam
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Perguntas frequentes sobre a sincronização empresarial do Microsoft Edge.
ms.openlocfilehash: a13e1f02f6e871004d45f81159d5cf0a3397b6ad
ms.sourcegitcommit: 8968f3107291935ed9adc84bba348d5f187eadae
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/12/2021
ms.locfileid: "11978745"
---
# <a name="microsoft-edge-enterprise-sync-faq"></a>Perguntas frequentes sobre a sincronização empresarial do Microsoft Edge

Este artigo responde a perguntas frequentes sobre a sincronização empresarial do Microsoft Edge versão 77 ou posterior.

## <a name="security-and-serverdata-compliance"></a>Segurança e Conformidade com o Servidor/Dados

### <a name="is-the-synced-data-encrypted"></a>Os dados sincronizados estão criptografados?

Os dados são criptografados no transporte usando TLS 1.2 ou posterior. Todos os tipos de dados também são criptografados como descansar no serviço da Microsoft usando o AES128. Todos os tipos de dados, exceto os usados na guia aberta e na sincronização do histórico, são adicionalmente criptografados antes de deixar o dispositivo do usuário com chaves gerenciadas através da política da [Proteção de Informações do Microsoft Azure](./microsoft-edge-policies.md#restrictsignintopattern).

### <a name="why-dont-open-tab-and-history-data-have-more-client-side-encryption"></a>Por que a guia aberta e os dados do histórico não têm mais criptografia do lado do cliente?

Para reduzir o uso de recursos nos dispositivos do usuário final, os dados do histórico são gerados no lado do servidor com base nos dados de roaming da guia aberta. Este processo não seria possível com a criptografia ao lado do cliente desses dados. Para desabilitar a guia aberta e a sincronização do histórico, aplique as políticas [SavingBrowserHistoryDisabled](./microsoft-edge-policies.md#savingbrowserhistorydisabled) ou [SyncTypesListDisabled](./microsoft-edge-policies.md#synctypeslistdisabled) .

### <a name="can-tenant-admins-bring-their-own-key"></a>Os administradores de locatários podem ter suas próprias chaves?

Sim, pela [Proteção de informações do Azure](https://azure.microsoft.com/services/information-protection/).

### <a name="where-is-microsoft-edge-sync-data-stored"></a>Onde os dados sincronizados são armazenados no Microsoft Edge?

Os dados sincronizados para contas do Azure AD são armazenados em servidores seguros de acordo com a ID do locatário. Por exemplo, os dados de um locatário registrado nos Estados Unidos são armazenados em servidores localizados geograficamente nessa região e aproveitam a mesma solução de armazenamento usada pelos aplicativos do Office.

### <a name="does-the-data-ever-leave-microsofts-cloud-aside-from-syncing-to-microsoft-edge"></a>Os dados deixam a nuvem da Microsoft, além de sincronizar com o Microsoft Edge?

Não.

### <a name="what-terms-of-service-does-enterprise-sync-fall-under"></a>Em que termos de serviço a sincronização empresarial se encaixa?

Os termos de serviço da sincronização do Microsoft Edge se enquadram na licença de software da Microsoft exibida no Microsoft Edge em *Edge://terms*. A sua assinatura e os termos de serviço do Azure AD estão, em última análise, em [Termos de serviço on-line](https://www.microsoft.com/licensing/product-licensing/products)da Microsoft.

### <a name="does-microsoft-edge-support-government-community-cloud-gcc-high-compliance"></a>O Microsoft Edge dá suporte á conformidade do Government Community Cloud (GCC) High?

Não atualmente. A sincronização do Microsoft Edge está desabilitada para os clientes na nuvem do GCC High.

## <a name="applying-sync"></a>Aplicar Sincronização

### <a name="why-isnt-microsoft-edge-sync-supported-in-all-m365-subscriptions"></a>Por que a sincronização do Microsoft Edge não é compatível com todas as assinaturas do M365?

A sincronização empresarial depende da [Proteção de Informações do Azure,](https://azure.microsoft.com/services/information-protection/)que não está disponível em todas as assinaturas do M365.

### <a name="is-microsoft-edge-sync-based-on-enterprise-state-roaming"></a>A sincronização do Microsoft Edge é baseada no Enterprise State Roaming?

Não. O ESR pode ser usado para habilitar a sincronização, mas a sincronização do Microsoft Edge não faz parte do ESR. Para obter mais informações, consulte [Sincronização do Microsoft Edge](/DeployEdge/microsoft-edge-enterprise-sync) e [Microsoft Edge e Enterprise State Roaming](/DeployEdge/microsoft-edge-enterprise-state-roaming).

### <a name="will-microsoft-edge-ever-support-syncing-between-microsoft-edge-and-ie"></a>O Microsoft Edge oferecerá suporte para sincronização entre o Microsoft Edge e o IE?

Não há planos para dar suporte a essa sincronização. Se você ainda precisar do IE no seu ambiente para oferecer suporte aos aplicativos herdados, considere o nosso [novo modo do IE](./edge-ie-mode.md).

### <a name="will-microsoft-edge-sync-with-microsoft-edge-legacy"></a>O Microsoft Edge será sincronizado com o Microsoft Edge herdado?

Não. Acreditamos que a conexão destes dois ecossistemas comprometerá a confiabilidade da sincronia no Microsoft Edge. Garantiremos que os dados existentes serão migrados para o Microsoft Edge. Os usuários também poderão importar dados do navegador de sua escolha, o que também significa que o Microsoft Edge não terá uma maneira de sincronizar com o IE.

## <a name="managing-sync"></a>Gerenciar Sincronização

### <a name="is-it-possible-to-stop-my-users-from-syncing-with-a-personal-tenant"></a>É possível impedir que os meus usuários sincronizem com um locatário pessoal?

Não diretamente, mas você pode determinar quais perfis podem entrar no Microsoft Edge usando a política [RestrictSigninToPattern](./microsoft-edge-policies.md#restrictsignintopattern).

## <a name="see-also"></a>Ver também

- [Sincronização do Microsoft Edge Enterprise](microsoft-edge-enterprise-sync.md)
- [Microsoft Edge e Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md)
- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)