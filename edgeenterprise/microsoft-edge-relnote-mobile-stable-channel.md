---
title: Notas de versão do Microsoft Edge para Canal Estável Móvel
ms.author: leahtu
author: dan-wesley
manager: srugh
ms.date: 08/17/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Notas de versão do Microsoft Edge para Canal Estável Móvel
ms.openlocfilehash: 709259c60594c5d4d2aed265ff43c0cd6c8a4001
ms.sourcegitcommit: 3e3362b0c5c663df160e8e8f68a4c82564183b2d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/31/2022
ms.locfileid: "12740691"
---
# <a name="release-notes-for-microsoft-edge-mobile-stable-channel"></a>Notas de versão para o Canal Estável Móvel do Microsoft Edge

Essas notas de versão fornecem informações sobre os novos recursos disponíveis para contas corporativas ou de estudante, e atualizações não relacionadas à segurança incluídas no Microsoft Edge para Canal Estável Móvel.

Para entender os canais do Microsoft Edge, confira a [Visão geral dos canais do Microsoft Edge](./microsoft-edge-channels.md).

Todas as atualizações de segurança do Canal Estável estão listadas em [Notas de versão para Atualizações de Segurança do Microsoft Edge](./microsoft-edge-relnotes-security.md).

> [!NOTE]
> Para o Canal Estável, as atualizações são implantadas progressivamente por um ou mais dias. Para saber mais, consulte [Distribuições progressivas para atualizações do Microsoft Edge](./microsoft-edge-update-progressive-rollout.md). Pode haver um atraso antes que a nova versão seja preenchida para o App Store (iOS) e o Google Play (Android).

## <a name="version-1040129360-august-17"></a>Versão 104.0.1293.60: 17 de agosto

> [!IMPORTANT]
> Essa atualização contém uma correção para [CVE-2022-2856](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2022-2856), que foi relatada pela equipe Chromium como tendo uma exploração em execução. Para obter mais informações, consulte o [Guia de atualização de segurança](https://msrc.microsoft.com/update-guide).

As atualizações de segurança do canal Estável estão listadas [aqui](/deployedge/microsoft-edge-relnotes-security#august-17-2022).

## <a name="version-1040129358-august-16"></a>Versão 104.0.1293.58: 16 de agosto

Correção de vários bugs.

### <a name="feature-updates"></a>Atualizações de recursos

- **Suporte para desabilitação do recurso navegação inPrivate e Senha (iOS e Android).**  Antes do Microsoft Edge 104, o Edge para iOS e Android desabilitou a navegação InPrivate e a Senha (solicita que você salve senhas para o usuário) por padrão quando permitir apenas contas corporativas ou de estudante estiver configurada.<br><br>
A partir do Microsoft Edge 104, você tem mais flexibilidade porque o InPrivate e a Senha não serão desabilitados por padrão quando somente permitir contas corporativas ou de estudante estiver configurada. Em vez disso, você pode decidir se deseja desabilitar a navegação InPrivate ou a senha configurando a chave **com.microsoft.intune.mam.managedbrowser.disabledFeatures** . Para obter mais informações, consulte [Desabilitar recursos específicos](/mem/intune/apps/manage-microsoft-edge#disable-specific-features).

## <a name="version-103126453-july-1"></a>Versão 103.1264.53: 1º de julho

Correção de vários bugs.

## <a name="version-1030126438-june-30"></a>Versão 103.0.1264.38: 30 de junho

Correção de vários bugs.

## <a name="version-1020124530-may-31"></a>Versão 102.0.1245.30: 31 de maio

Correção de vários bugs.

### <a name="feature-updates"></a>Atualizações de recursos

- **Suporte para alternar a pilha de rede entre o Chromium e o iOS (somente iOS).** A política [NetworkStackPref](/mem/intune/apps/manage-microsoft-edge#switch-network-stack-between-chromium-and-ios) permite que você escolha a preferência de rede para o Microsoft Edge para iOS.

### <a name="policy-updates"></a>Atualizações de política

#### <a name="new-policies"></a>Novas políticas

- [NetworkStackPref](/mem/intune/apps/manage-microsoft-edge#switch-network-stack-between-chromium-and-ios) - Escolha a preferência de rede para o Microsoft Edge para iOS

## <a name="version-1010121043-may-9"></a>Versão 101.0.1210.43: 9 de maio

Correção de vários bugs.

## <a name="version-1010121032-april-29"></a>Versão 101.0.1210.32: 29 de abril

Correção de vários bugs.

### <a name="feature-updates"></a>Atualizações de recursos

- **Ler em Voz Alta: reprodução em segundo plano e reprodução no modo silencioso (iOS e Android)**
  - Ao reproduzir em segundo plano, os usuários podem controlar Ler em Voz Alta (pausar, retomar, avançar ou retornar) por meio do painel de notificação e da tela de bloqueio.
  - Quando um usuário alterna as guias do Microsoft Edge ao usar Ler em Voz Alta, ele pode usar uma barra de controle flutuante para pausar, retomar ou fechar a opção Ler em Voz Alta.
  - Quando a alternância silenciosa de um dispositivo está ativada, ela não afeta a reprodução de Ler em Voz Alta, desde que o volume de mídia esteja ativado.
  
## <a name="see-also"></a>Consulte também

- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
