---
title: Sincronização do Microsoft Edge Enterprise
ms.author: scottbo
author: dan-wesley
manager: silvanam
ms.date: 12/09/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Sincronização do Microsoft Edge Enterprise
ms.openlocfilehash: 791188b5d28c867d6409a4d5373ea6c1ec7e49c7
ms.sourcegitcommit: 482b2e440a62cbf974dc45ac817f9d9d187ba1b9
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "11205460"
---
# Sincronização do Microsoft Edge Enterprise

Este artigo explica como usar o Microsoft Edge para sincronizar seus favoritos, senhas e outros dados do navegador com todos os seus dispositivos conectados.

> [!NOTE]
> Este artigo se aplica ao Microsoft Edge versão 77 ou posterior, a menos que indicado de outra forma.

## Visão geral

A sincronização do Microsoft Edge permite que os usuários acessem seus dados de navegação em todos os dispositivos conectados. Os dados com suporte na sincronização incluem:

- Favoritos
- Senhas
- Endereços e etc. (preenchimento de formulário)
- Coleções
- Configurações
- Extensão
- Abrir guias (disponível no Microsoft Edge versão 88)
- Histórico (disponível no Microsoft Edge versão 88)

A funcionalidade de sincronização é habilitada através do consentimento do usuário, e os usuários podem ativar ou desativar a sincronização de cada um dos tipos de dados listados acima.

> [!NOTE]
> Outros dados de configuração e conectividade do dispositivo (como nome, marca e modelo do dispositivo) são carregados para dar suporte à funcionalidade de sincronização.

## Pré-requisitos

A sincronização do Microsoft Edge das contas do Azure Active Directory (Azure AD) está disponível para qualquer uma das seguintes assinaturas:

- Azure AD Premium (P1 ou P2)
- M365 Business Premium
- Office 365 E1 e superior
- Proteção de informações do Azure (AIP) (P1 ou P2)
- Todas as assinaturas EDU (Aplicativos da Microsoft para Estudantes ou Docentes, Exchange Online para Estudantes ou Docentes, O365 A1 ou superior, M365 A1 ou superior, Proteção de Informações do Azure P1 ou P2 para Estudantes ou Docentes)

## Configurar a sincronização do Microsoft Edge

As opções de configuração para a sincronização do Microsoft Edge estão disponíveis por meio do serviço de Proteção de Informações do Azure (AIP). Quando o (AIP) estiver habilitado para um locatário, todos os usuários poderão sincronizar os dados do Microsoft Edge, independentemente do licenciamento. Instruções sobre como habilitar o AIP estão disponíveis [aqui](https://docs.microsoft.com/azure/information-protection/activate-office365).

Para restringir a sincronização a certos conjuntos de usuários, você pode habilitar a [Política de controle de integração do AIP](https://docs.microsoft.com/powershell/module/aipservice/set-aipserviceonboardingcontrolpolicy?view=azureipps&preserve-view=true)  para esses usuários. Se a sincronização ainda não estiver disponível depois de garantir que todos os usuários necessários estejam integrados, certifique-se de que o IPCv3Service está habilitado usando o cmdlet [Get-AIPServiceIPCv3](https://docs.microsoft.com/powershell/module/aipservice/get-aipserviceipcv3?view=azureipps&preserve-view=true)  PowerShell.

> [!CAUTION]
> Ativar a Proteção de Informações do Azure também permitirá que outros aplicativos, como o Microsoft Word ou o Microsoft Outlook, protejam o conteúdo com o AIP. Além disso, qualquer política de controle de integração usada para restringir a sincronização do Microsoft Edge também restringirá outros aplicativos de proteger conteúdo usando o AIP.

## Microsoft Edge e Enterprise State Roaming

O novo Microsoft Edge é um aplicativo compatível com diferentes plataformas e possui um escopo expandido para sincronizar os dados do usuário em todos os dispositivos deles e não faz mais parte do Enterprise State Roaming do AAD. No entanto, o novo Microsoft Edge cumprirá as promessas de proteção de dados do ESR, como a capacidade de trazer sua própria chave. Para obter mais informações, consulte [Microsoft Edge e Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).

## Políticas de grupo de sincronização

As seguintes políticas de grupo afetam a sincronização do Microsoft Edge:

- [SyncDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#syncdisabled): desabilita completamente a sincronização.
- [SavingBrowserHistoryDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#savingbrowserhistorydisabled): desabilita o salvamento do histórico de navegação e a sincronização. Também desabilita a sincronização das guias abertas.
- [AllowDeletingBrowserHistory](https://docs.microsoft.com/deployedge/microsoft-edge-policies#allowdeletingbrowserhistory): quando essa política é definida como Desabilitada, a sincronização do histórico também será desabilitada.
- [SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled): configura a lista dos tipos excluídos da sincronização.
- [RoamingProfileSupportEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#roamingprofilesupportenabled): permite que os perfis Active Directory (AD) usem o armazenamento local. Para obter mais informações, consulte [Sincronização local para usuários do Active Directory (AD)](https://docs.microsoft.com/DeployEdge/microsoft-edge-on-premises-sync).
- [ForceSync]( https://docs.microsoft.com/deployedge/microsoft-edge-policies#forcesync): ativar a sincronização por padrão e não exigir consentimento do usuário para sincronizar.  

## Perguntas frequentes

### SEGURANÇA e CONFORMIDADE COM O SERVIDOR/DADOS

#### Os dados sincronizados estão encriptados?

Os dados são criptografados no transporte usando TLS 1.2 ou posterior. Todos os tipos de dados também são criptografados como descansar no serviço da Microsoft usando o AES128. Todos os tipos de dados, exceto os usados na guia aberta e na sincronização do histórico, também são criptografados antes de sair do dispositivo do usuário com chaves gerenciadas pela [Proteção de informações do Azure](https://docs.microsoft.com/azure/information-protection/).

#### Por que não abrir a guia e os dados do histórico têm criptografia abrir ao lado do cliente adicional?  

Para reduzir o uso de recursos nos dispositivos de usuário final, os dados do histórico são gerados no lado do servidor com base nos dados de roaming da guia aberta. Esse processo não seria possível com a criptografia ao lado do cliente desses dados. Para desabilitar a guia aberta e a sincronização do histórico, aplique as políticas [SavingBrowserHistoryDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#savingbrowserhistorydisabled) ou [SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled) .

#### Os administradores de locatários podem ter suas próprias chaves?

Sim, pela [Proteção de informações do Azure](https://azure.microsoft.com/services/information-protection/).

#### Onde os dados sincronizados são armazenados no Microsoft Edge?

Os dados sincronizados para contas do Azure AD são armazenados em servidores seguros de acordo com a ID do locatário. Por exemplo, os dados de um locatário registrado nos Estados Unidos são armazenados em servidores localizados geograficamente nessa região e aproveitam a mesma solução de armazenamento usada pelos aplicativos do Office.

#### Os dados deixam a nuvem da Microsoft, além de sincronizar com o Microsoft Edge?

Não.

#### Em que termos de serviço a sincronização empresarial se encaixa?

Os termos de serviço da sincronização do Microsoft Edge se enquadram na licença de software da Microsoft exibida no Microsoft Edge em *Edge://terms*. A sua assinatura e os termos de serviço do Azure AD estão, em última análise, em [Termos de serviço on-line](https://www.microsoft.com/licensing/product-licensing/products)da Microsoft.

#### O Microsoft Edge dá suporte á conformidade do Government Community Cloud (GCC) High?

Não atualmente. Para os clientes na nuvem GCC High, o Microsoft Edge sync está desabilitado.

### APLICAÇÃO DE SINCRONIZAÇÃO

#### Por que a sincronização do Microsoft Edge não é compatível com todas as assinaturas do M365?

A sincronização da empresa depende da Proteção de informações do Azure, que não está disponível em todas as assinaturas do M365.

#### A sincronização do Microsoft Edge é baseada no Enterprise State Roaming?

Não. O ESR pode ser usado para habilitar a sincronização, mas a sincronização do Microsoft Edge não faz parte do ESR. Para obter mais informações, consulte [Sincronização do Microsoft Edge](microsoft-edge-enterprise-sync.md) e [Microsoft Edge e Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).

#### O Microsoft Edge oferecerá suporte para sincronização entre o Microsoft Edge e o IE?

Não há planos para dar suporte a essa sincronização. Se você ainda precisar do IE no seu ambiente para oferecer suporte aos aplicativos herdados, considere o nosso [novo modo do IE](https://docs.microsoft.com/deployedge/edge-ie-mode).

#### O Microsoft Edge será sincronizado com o Microsoft Edge herdado?

Não. Acreditamos que a conexão destes dois ecossistemas comprometerá a confiabilidade da sincronia no Microsoft Edge. Garantiremos que os dados existentes serão migrados para o Microsoft Edge. Os usuários também poderão importar dados do navegador de sua preferência. Isso também significa que o novo navegador Microsoft Edge não poderá ser sincronizado com o IE.

### GERENCIANDO A SINCRONIZAÇÃO

#### É possível impedir que os meus usuários sincronizem com um locatário pessoal?

Não diretamente, mas você pode determinar quais perfis podem entrar no Microsoft Edge usando a política [RestrictSigninToPattern](https://docs.microsoft.com/deployedge/microsoft-edge-policies#restrictsignintopattern).

## Consulte também

- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Microsoft Edge e Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md)
