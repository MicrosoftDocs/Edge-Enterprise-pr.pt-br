---
title: Configurar a sincronização do Microsoft Edge Enterprise
ms.author: collw
author: dan-wesley
manager: silvanam
ms.date: 05/31/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Opções de administrador e de usuário para configurar o Microsoft Edge para sincronizar os favoritos, senhas e outros dados do navegador.
ms.openlocfilehash: a16815291ac78ffb1e1d85cb24d6a43025ea2503
ms.sourcegitcommit: b8ce42bb539f74a93f1e66497e3b6f6f076e0c2a
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/01/2022
ms.locfileid: "12555384"
---
# <a name="configure-microsoft-edge-enterprise-sync"></a>Configurar a sincronização do Microsoft Edge Enterprise

Este artigo explica como os administradores podem configurar o Microsoft Edge para sincronizar os favoritos, senhas e outros dados do navegador do usuário em todos os dispositivos conectados.

> [!NOTE]
> Aplica-se ao Microsoft Edge no Chromium, versão 77 ou posterior, a menos que indicado de outra forma.

## <a name="introduction"></a>Introdução

A sincronização do Microsoft Edge permite que os usuários acessem seus dados de navegação em todos os dispositivos conectados. Os usuários podem sincronizar os seguintes dados:

- Favoritos
- Senhas
- Endereços e etc. (preenchimento de formulário)
- Coleções
- Configurações
- Extensões
- Abrir guias (disponível no Microsoft Edge versão 88 ou posterior)
- Histórico (disponível na versão Microsoft Edge 88 ou posterior)

> [!NOTE]
> Dados adicionais de conectividade e configuração do dispositivo (como nome do dispositivo, fabricante do dispositivo e modelo de dispositivo) são carregados para dar suporte à funcionalidade de sincronização.

### <a name="sync-functionality-and-user-sync-configuration"></a>Funcionalidade de sincronização e configuração de sincronização do usuário

Depois que a sincronização é configurada, a funcionalidade de sincronização é habilitada pelo consentimento do usuário. Os usuários podem ativar ou desativar a sincronização dos dados com suporte. Para obter mais informações, consulte [Entrar para sincronizar o Microsoft Edge nos dispositivos](https://support.microsoft.com/microsoft-edge/sign-in-to-sync-microsoft-edge-across-devices-e6ffa79b-ed52-aa32-47e2-5d5597fe4674).

> [!NOTE]
> Se um usuário estiver com problemas de sincronização, talvez seja necessário redefinir a sincronização em **Configurações** > **Perfis** > **Sincronização** > **Redefinir Sincronização**.

## <a name="prerequisites"></a>Pré-requisitos

Os seguintes pré-requisitos se aplicam à sincronização do Microsoft Edge Enterprise:

- Microsoft Edge versão que oferece suporte às funções de sincronização desejadas
- Assinatura de um serviço na nuvem em um ambiente com suporte
- Proteção de informações do Azure (AIP) (P1 ou P2)

## <a name="supported-environments"></a>Ambientes com suporte

A sincronização do Microsoft Edge das contas do Azure Active Directory (Azure AD) está disponível para qualquer uma das seguintes assinaturas:

- Azure AD Premium (P1 ou P2)
  
  > [!NOTE]
  > Os clientes que têm apenas o Azure AD P1 ou P2 devem habilitar o Azure AD Enterprise State Roaming (ESR). A sincronização do ESR não faz parte do ESR, mas o ESR é necessário para fornecer a funcionalidade de AIP necessária para as configurações P1 e P2. Para saber mais, consulte o artigo [Habilitar o Enterprise State Roaming no Azure Active Directory](/azure/active-directory/devices/enterprise-state-roaming-enable).

- Microsoft 365 Business Premium, Business Standard ou Business Basic

  > [!NOTE]
  > Há suporte para o Business Basic, mas alguns locatários existentes precisam ser preenchidos com o plano de serviço RMS_S_BASIC necessário para a AIP. Os clientes poderão arquivar uma solicitação de suporte se precisarem fazer backup de um locatário.

- Office 365 E1 e superior
- Todas as assinaturas EDU, incluindo:
  - Microsoft Apps para estudantes ou docentes
  - Exchange Online para estudantes ou docentes
  - O365 A1 ou superior
  - Microsoft 365 A1 ou superior
  - Proteção de Informações do Azure P1 ou P2 para alunos ou docentes

## <a name="sync-group-policies"></a>Políticas de grupo de sincronização

Os administradores podem usar as seguintes políticas de grupo para configurar e gerenciar a sincronização do Microsoft Edge:

- [SyncDisabled](./microsoft-edge-policies.md#syncdisabled): desabilita a sincronização de dados.  Essa política desabilita apenas a sincronização na nuvem e não afeta a política RoamingProfileSupportEnabled.
- [SavingBrowserHistoryDisabled](./microsoft-edge-policies.md#savingbrowserhistorydisabled): desabilita salvar o histórico de navegação e sincronizar e abrir a sincronização de guias.
- [AllowDeletingBrowserHistory](./microsoft-edge-policies.md#allowdeletingbrowserhistory): quando essa política é definida como Desabilitada, a sincronização do histórico também será desabilitada.
- [SyncTypesListDisabled](./microsoft-edge-policies.md#synctypeslistdisabled): configura a lista dos tipos de dados excluídos da sincronização. Use essa política para limitar o tipo de dados carregados no sincronização de sincronização do Microsoft Edge.
- [RoamingProfileSupportEnabled](./microsoft-edge-policies.md#roamingprofilesupportenabled): permite que os perfis Active Directory (AD) usem o armazenamento local. As configurações armazenadas nos perfis do Microsoft Edge (favoritos e preferências) também são salvas em um arquivo armazenado na pasta de perfil de usuário móvel (ou em um local especificado pelo administrador). Para obter mais informações, consulte [Sincronização local dos usuários do Active Directory (AD)](./microsoft-edge-on-premises-sync.md).
- [ForceSync](/deployedge/microsoft-edge-policies#forcesync): forçar a sincronização dos dados do navegador e não mostrar o aviso de consentimento da sincronização. Os usuários não podem desabilitar essa política.

## <a name="use-azure-information-protection-to-configure-microsoft-edge-sync"></a>Usar a Proteção de Informações do Azure para configurar a sincronização do Microsoft Edge

As opções de configuração para a sincronização do Microsoft Edge estão disponíveis por meio do serviço de Proteção de Informações do Azure (AIP). Quando o (AIP) estiver habilitado para um locatário, todos os usuários poderão sincronizar os dados do Microsoft Edge, independentemente do licenciamento. O serviço de proteção pode ser ativado automaticamente, usando o PowerShell ou usando o portal do Azure. Para obter mais informações e instruções sobre como habilitar a AIP, consulte [Ativar o serviço de proteção da Proteção de Informações do Azure (AIP)](/azure/information-protection/activate-office365).

> [!CAUTION]
> Ativar a Proteção de Informações do Azure também permitirá que outros aplicativos, como o Microsoft Word ou o Microsoft Outlook, protejam o conteúdo com o AIP. As políticas de controle de integração usadas para restringir a sincronização do Microsoft Edge também impedirão que outros aplicativos protejam o conteúdo usando a AIP.

### <a name="control-user-onboarding-for-a-phased-deployment"></a>Controlar a integração do usuário para uma implantação em fases

Você pode usar o cmdlet [Set-AipServiceOnboardingControlPolicy](/powershell/module/aipservice/set-aipserviceonboardingcontrolpolicy?preserve-view=true&view=azureipps) para definir a política que controla a integração do usuário na Proteção de Informações do Azure. Se a sincronização ainda não estiver disponível depois que todos os usuários especificados forem integrados, verifique se IPCv3Service está habilitado usando o cmdlet do PowerShell [Get-AIPServiceIPCv3](/powershell/module/aipservice/get-aipserviceipcv3?preserve-view=true&view=azureipps). Para obter mais informações, consulte [Configurar controles de integração para uma implantação em fases](/azure/information-protection/activate-service#configuring-onboarding-controls-for-a-phased-deployment).

## <a name="microsoft-edge-and-enterprise-state-roaming-esr"></a>Microsoft Edge e ESR (Enterprise State Roaming)

O Microsoft Edge é um aplicativo de plataforma cruzada com um escopo expandido para sincronizar dados de usuários em todos os seus dispositivos, e não faz mais parte do Enterprise State Roaming do Azure AD. Entretanto, o Microsoft Edge cumprirá as promessas de proteção de dados do ESR, como a capacidade de trazer sua própria chave. Para obter mais informações, confira [Microsoft Edge e Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).

## <a name="see-also"></a>Veja também

- [Diagnosticar e corrigir problemas de sincronização do Microsoft Edge](microsoft-edge-troubleshoot-enterprise-sync.md)
- [Perguntas frequentes sobre sincronização de empresa do Microsoft Edge](microsoft-edge-enterprise-sync-faq.md)
- [Microsoft Edge e Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md)
- [O que é a Proteção de Informações do Azure?](/azure/information-protection/what-is-information-protection)
- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)