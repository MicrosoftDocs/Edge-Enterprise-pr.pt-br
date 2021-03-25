---
title: Configurar a sincronização do Microsoft Edge Enterprise
ms.author: scottbo
author: dan-wesley
manager: silvanam
ms.date: 03/08/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Opções de administrador e de usuário para configurar o Microsoft Edge para sincronizar os favoritos, senhas e outros dados do navegador.
ms.openlocfilehash: 93af96bd864f08bb17bb1d6f0669f602a56fd8ca
ms.sourcegitcommit: f363ceb6c42054fabc95ce8d7bca3c52d80e6a9f
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/24/2021
ms.locfileid: "11448115"
---
# <a name="configure-microsoft-edge-enterprise-sync"></a>Configurar a sincronização do Microsoft Edge Enterprise

Este artigo explica como os administradores podem configurar o Microsoft Edge para sincronizar os favoritos, senhas e outros dados do navegador do usuário em todos os dispositivos conectados.

> [!NOTE]
> Aplica-se ao Microsoft Edge versão 77 ou posterior, a menos que indicado de outra forma.

## <a name="overview"></a>Visão geral

A sincronização do Microsoft Edge permite que os usuários acessem seus dados de navegação em todos os dispositivos conectados. Os dados com suporte na sincronização incluem:

- Favoritos
- Senhas
- Endereços e etc. (preenchimento de formulário)
- Coleções
- Configurações
- Extensão
- Abrir guias (disponível no Microsoft Edge versão 88)
- Histórico (disponível no Microsoft Edge versão 88)

A funcionalidade de sincronização é habilitada através do consentimento do usuário, e os usuários podem ativar ou desativar a sincronização de cada um dos tipos de dados listados acima. Se um usuário estiver com problemas de sincronização, talvez seja necessário redefinir a sincronização em **Configurações** > **Perfis** > **Redefinir sincronização**.

> [!NOTE]
> Outros dados de configuração e conectividade do dispositivo (como nome, marca e modelo do dispositivo) são carregados para dar suporte à funcionalidade de sincronização.

## <a name="prerequisites"></a>Pré-requisitos

A sincronização do Microsoft Edge das contas do Azure Active Directory (Azure AD) está disponível para qualquer uma das seguintes assinaturas:

- Azure AD Premium (P1 ou P2)
- M365 Business Premium
- Office 365 E1 e superior
- Proteção de informações do Azure (AIP) (P1 ou P2)
- Todas as assinaturas EDU (Aplicativos da Microsoft para Estudantes ou Docentes, Exchange Online para Estudantes ou Docentes, O365 A1 ou superior, M365 A1 ou superior, Proteção de Informações do Azure P1 ou P2 para Estudantes ou Docentes)

## <a name="sync-group-policies"></a>Políticas de grupo de sincronização

Os administradores podem usar as seguintes políticas de grupo para configurar e gerenciar a sincronização do Microsoft Edge:

- [SyncDisabled](./microsoft-edge-policies.md#syncdisabled): desabilita completamente a sincronização.
- [SavingBrowserHistoryDisabled](./microsoft-edge-policies.md#savingbrowserhistorydisabled): desabilita o salvamento do histórico de navegação e a sincronização. Também desabilita a sincronização das guias abertas.
- [AllowDeletingBrowserHistory](./microsoft-edge-policies.md#allowdeletingbrowserhistory): quando essa política é definida como Desabilitada, a sincronização do histórico também será desabilitada.
- [SyncTypesListDisabled](./microsoft-edge-policies.md#synctypeslistdisabled): configura a lista dos tipos excluídos da sincronização.
- [RoamingProfileSupportEnabled](./microsoft-edge-policies.md#roamingprofilesupportenabled): permite que os perfis Active Directory (AD) usem o armazenamento local. Para obter mais informações, confira [Sincronização local para usuários do Active Directory (AD)](./microsoft-edge-on-premises-sync.md).
- [ForceSync]( https://docs.microsoft.com/deployedge/microsoft-edge-policies#forcesync): ativar a sincronização por padrão e não exigir consentimento do usuário para sincronizar.  

## <a name="configure-microsoft-edge-sync"></a>Configurar a sincronização do Microsoft Edge

As opções de configuração para a sincronização do Microsoft Edge estão disponíveis por meio do serviço de Proteção de Informações do Azure (AIP). Quando o (AIP) estiver habilitado para um locatário, todos os usuários poderão sincronizar os dados do Microsoft Edge, independentemente do licenciamento. Instruções sobre como habilitar o AIP estão disponíveis [aqui](/azure/information-protection/activate-office365).

Para restringir a sincronização a certos conjuntos de usuários, você pode habilitar a [Política de controle de integração do AIP](/powershell/module/aipservice/set-aipserviceonboardingcontrolpolicy?preserve-view=true&view=azureipps)  para esses usuários. Se a sincronização ainda não estiver disponível depois de garantir que todos os usuários necessários estejam integrados, certifique-se de que o IPCv3Service está habilitado usando o cmdlet [Get-AIPServiceIPCv3](/powershell/module/aipservice/get-aipserviceipcv3?preserve-view=true&view=azureipps)  PowerShell.

> [!CAUTION]
> Ativar a Proteção de Informações do Azure também permitirá que outros aplicativos, como o Microsoft Word ou o Microsoft Outlook, protejam o conteúdo com o AIP. Além disso, qualquer política de controle de integração usada para restringir a sincronização do Microsoft Edge também restringirá outros aplicativos de proteger conteúdo usando o AIP.

## <a name="microsoft-edge-and-enterprise-state-roaming-esr"></a>Microsoft Edge e ESR (Enterprise State Roaming)

O Microsoft Edge é um aplicativo de plataforma cruzada com um escopo expandido para sincronizar dados de usuários em todos os seus dispositivos, e não faz mais parte do Enterprise State Roaming do Azure AD. No entanto, o Microsoft Edge cumprirá as promessas de proteção de dados do ESR, como a capacidade de trazer sua própria chave. Para obter mais informações, confira [Microsoft Edge e Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).

## <a name="see-also"></a>Veja também

- [Sincronização do Microsoft Edge Enterprise](microsoft-edge-enterprise-sync.md)
- [Diagnosticar e corrigir problemas de sincronização do Microsoft Edge](microsoft-edge-troubleshoot-enterprise-sync.md)
- [Microsoft Edge e Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md)
- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)