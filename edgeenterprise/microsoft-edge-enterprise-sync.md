---
title: Sincronização do Microsoft Edge Enterprise
ms.author: scottbo
author: dan-wesley
manager: silvanam
ms.date: 08/03/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Sincronização do Microsoft Edge Enterprise
ms.openlocfilehash: a6d01356db478871a7c6b386bbb731b32dc4739a
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979127"
---
# Sincronização do Microsoft Edge Enterprise

Este artigo explica como usar o Microsoft Edge para sincronizar seus favoritos, senhas e outros dados do navegador com todos os seus dispositivos conectados.

> [!NOTE]
> Este artigo se aplica ao Microsoft Edge versão 77 ou posterior.

## Visão geral

A sincronização do Microsoft Edge permite que os usuários acessem seus dados de navegação em todos os dispositivos conectados. Os dados com suporte na sincronização incluem:

- Favoritos
- Senhas
- Endereços e etc. (preenchimento de formulário)
- Coleções
- Configurações

A funcionalidade de sincronização é habilitada por meio do consentimento do usuário, e os usuários podem ativar ou desativar a sincronização para cada um dos tipos de dados listados acima.

> [!NOTE]
> Outros dados de configuração e conectividade do dispositivo (como nome, marca e modelo do dispositivo) são carregados para dar suporte à funcionalidade de sincronização.

## Pré-requisitos

Atualmente, a sincronização do Microsoft Edge para as contas do Azure Active Directory (Azure AD) está disponível somente para as seguintes assinaturas:

- Azure AD Premium( P1 e P2)
- M365 Business Premium
- Office 365 E3 e superior
- Proteção de Informações do Azure (AIP) (P1 e P2)
- Todas as assinaturas EDU (O365 A1 ou superior, M365 A1 ou superior, Proteção de Informações do Azure P1 ou P2 para estudantes ou professores)

> [!NOTE]
> A sincronização depende do serviço de proteção oferecido pela Proteção de Informações do Azure (AIP) para proteger os dados de sincronização. Esse serviço está atualmente disponível para as assinaturas anteriores. Para ver a lista completa de SKUs com AIP, consulte [Preços da Proteção de Informações](https://azure.microsoft.com/pricing/details/information-protection/).

## Opções de configuração para a sincronização do Microsoft Edge

As seguintes opções de configuração estão disponíveis para habilitar a sincronização de Microsoft Edge:

- Proteção de Informações do Azure (AIP)
- Enterprise State Roaming (ESR) ou Roaming de Nível Empresarial do AAD

Se o AIP e o ESR estiverem desabilitados, os usuários verão uma mensagem de erro indicando que a sincronização não está disponível para a conta.

### Proteção de Informações do Azure (AIP)

Se o serviço Proteção de Informações do Azure (AIP) estiver habilitado para um locatário, todos os usuários poderão sincronizar os dados do Microsoft Edge, independentemente do licenciamento. Instruções sobre como habilitar o AIP estão disponíveis [aqui](https://docs.microsoft.com/azure/information-protection/activate-office365).

Para restringir a sincronização a certos conjuntos de usuários, você pode habilitar a [Política de controle de integração AADRM](https://docs.microsoft.com/powershell/module/aadrm/set-aadrmonboardingcontrolpolicy?view=azureipps) desses usuários. Se a sincronização ainda não estiver disponível depois de garantir que todos os usuários necessários estejam integrados, certifique-se de que o IPCv3Service está habilitado através do [Get-AIPServiceIPCv3](https://docs.microsoft.com/powershell/module/aipservice/Get-AipServiceIPCv3?view=azureipps) PowerShell cmdlet.

> [!CAUTION]
> A ativação da Proteção de informações do Azure também restringirá o acesso de outros aplicativos que usam AIP, como o Microsoft Word ou o Microsoft Outlook.

### Enterprise State Roaming (ESR) ou Roaming de Nível Empresarial do AAD

Se o recurso [Enterprise State Roaming](https://docs.microsoft.com/azure/active-directory/devices/enterprise-state-roaming-overview) (ESR) do Azure Active Directory estiver habilitado para qualquer usuário ou locatário, eles poderão usar o recurso de sincronização do Microsoft Edge, independentemente da configuração de política de controle de integração.

## Microsoft Edge e Enterprise State Roaming

O novo Microsoft Edge é um aplicativo compatível com diferentes plataformas e possui um escopo expandido para sincronizar os dados do usuário em todos os dispositivos deles e não faz mais parte do Enterprise State Roaming do AAD. No entanto, o novo Microsoft Edge cumprirá as promessas de proteção de dados do ESR, como a capacidade de trazer sua própria chave. Para obter mais informações, consulte [Microsoft Edge e Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).

## Políticas de grupo de sincronização

As seguintes políticas de grupo afetam a sincronização do Microsoft Edge:

- [SyncDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#syncdisabled): desabilita completamente a sincronização.
- [SavingBrowserHistoryDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#savingbrowserhistorydisabled): Desabilita o salvamento do histórico de navegação e a sincronização. Também desabilita a sincronização de guias abertas.
- [SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled): configura a lista de tipos excluídos da sincronização.

## Perguntas frequentes

### SEGURANÇA e CONFORMIDADE COM O SERVIDOR/DADOS

#### Os dados sincronizados estão encriptados? 

Os dados são criptografados no transporte através do TLS 1.2 ou superior e, adicionalmente, em repouso no serviço da Microsoft através do AES256.

#### Onde os dados sincronizados são armazenados para o Microsoft Edge?

Os dados sincronizados para contas do Azure AD são armazenados em servidores seguros de acordo com a ID do locatário. Por exemplo, os dados de um locatário registrado nos Estados Unidos são armazenados em servidores localizados geograficamente nessa região e aproveitam a mesma solução de armazenamento usada pelos aplicativos do Office.

#### Os dados deixam a nuvem da Microsoft, além de sincronizar com o Microsoft Edge?

Não.

#### Os administradores de locatários podem ter suas próprias chaves?

Sim, por meio da [Proteção de Informações do Azure](https://azure.microsoft.com/services/information-protection/).

#### Em que termos de serviço a sincronização empresarial se encaixa?

Os termos de serviço são os mesmos termos da sua assinatura do Azure AD. Todos os termos de serviço do Azure AD estão, em última análise, no [Termos do serviço online](https://www.microsoft.com/licensing/product-licensing/products) da Microsoft.

#### O Microsoft Edge tem suporte para conformidade do Government Community Cloud (GCC) High?

Não hoje. GCC High é nível D, enquanto que o Microsoft Edge tem suporte para o nível C.

### APLICAÇÃO DE SINCRONIZAÇÃO

#### O que acontece com os clientes corporativos e educacionais que decidirem ficar com o Microsoft Edge Legacy?

A versão atual do navegador Microsoft Edge continuará participando da oferta de ESR.

#### Por que eu preciso de uma assinatura premium do Azure AD para sincronizar?

A sincronização empresarial depende da Proteção de Informações do Azure, que não está disponível em todos os níveis do Azure AD.

#### A sincronização do Microsoft Edge é baseada no Enterprise State Roaming?

Não. O ESR pode ser usado para habilitar a sincronização, mas a sincronização do Microsoft Edge não faz parte do ESR. Para obter mais informações, consulte [Sincronização do Microsoft Edge](microsoft-edge-enterprise-sync.md) e [Microsoft Edge e Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).

#### O Microsoft Edge oferecerá suporte para sincronização entre o Microsoft Edge e o IE?

Não há planos para dar suporte a essa sincronização. Se você ainda precisar do IE em seu ambiente para oferecer suporte a aplicativos herdados, considere o nosso [novo modo do IE](https://docs.microsoft.com/deployedge/edge-ie-mode).

#### O novo navegador Microsoft Edge será sincronizado com o Microsoft Edge Legacy?

Não. Acreditamos que conectar esses dois ecossistemas comprometerá a confiabilidade da sincronização no novo Microsoft Edge. Vamos garantir que os dados existentes sejam migrados para o novo Microsoft Edge. Os usuários também poderão importar dados do navegador de sua preferência. Isso também significa que o novo navegador Microsoft Edge não poderá ser sincronizado com o IE.

### GERENCIANDO A SINCRONIZAÇÃO

#### É possível impedir que os meus usuários sincronizem com um locatário pessoal?

Não diretamente, mas você pode determinar quais perfis podem entrar no Microsoft Edge usando a política [RestrictSigninToPattern](https://docs.microsoft.com/deployedge/microsoft-edge-policies#restrictsignintopattern).

## Consulte também

- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Microsoft Edge e Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md)
