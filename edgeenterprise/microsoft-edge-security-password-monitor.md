---
title: Monitor de Senha habilitado automaticamente para usuários
ms.author: supalsul
author: AndreLBarr
manager: tulasim
ms.date: 07/12/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Monitor de Senha habilitado automaticamente para usuários
ms.openlocfilehash: bd1fe390b972c66cd9b4c20ab3a9fabde76c7e03
ms.sourcegitcommit: 65530c0bad3097a510f507503eae9c5c67db47a0
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/12/2021
ms.locfileid: "11643878"
---
# <a name="password-monitor-auto-enabled-for-users"></a>Monitor de Senha habilitado automaticamente para usuários

Este artigo descreve como o Monitor de Senhas no Microsoft Edge será ativado para usuários selecionados e fornece aos administradores as etapas para controlar como o monitoramento está habilitado.

> [!NOTE]
> Este artigo se aplica ao Microsoft Edge versão 88 ou posterior.

## <a name="introduction-benefits-and-availability"></a>Introdução, benefícios e disponibilidade

O Monitor de Senhas ajuda os usuários do Microsoft Edge a proteger suas contas online informando-os se alguma de suas senhas foi encontrada em um vazamento online. Vazamentos online ou violações de dados ocorrem quando atores ruins roubam dados de sites ou aplicativos de terceiros. Para saber mais, confira o [Monitor de senhas: proteção de senhas no documento do Microsoft Edge](https://www.microsoft.com/research/blog/password-monitor-safeguarding-passwords-in-microsoft-edge/) no Blog da Pesquisa da Microsoft.

### <a name="benefits"></a>Benefícios

Dada a frequência e o escopo desses ataques online, ter esse tipo de proteção se tornou necessário para todos. O Microsoft Edge tem a capacidade interna de verificar com segurança as senhas salvas de um usuário em relação a senhas que se sabem comprometidas e os alerta se uma correspondência for encontrada.  

## <a name="configure-group-policy-for-password-monitor"></a>Configurar a política de grupo para o Monitor de Senhas

Esse recurso é controlado por meio da política de grupo[PasswordMonitorAllowed](./microsoft-edge-policies.md#passwordmonitorallowed).

Depois que a política é habilitada, os usuários ainda precisam dar consentimento para ativar o recurso. O consentimento é necessário porque o recurso contém dados pessoais e confidenciais do usuário (senhas). Se o recurso estiver desabilitado usando a política de grupo, os usuários não poderão substituir essa configuração.  

## <a name="enabling-password-monitor-for-users"></a>Habilitando o Monitor de Senhas para usuários

Depois que a política de monitor de senhas é habilitada, há maneiras diferentes de disponibilizar esse recurso para os usuários.

- Habilitar automaticamente. Os usuários que estão logados usando sua conta de trabalho (Active Directory ou Azure Active Directory), e sincronizando suas senhas, serão habilitados automaticamente para esse recurso. Eles verão a notificação na próxima captura de tela informando que o recurso está ligado.

  :::image type="content" source="media/microsoft-edge-security-password-monitor/monitor-enabled-notice.png" alt-text="Aviso habilitado para o Monitor de Senhas":::

-  Obter consentimento explícito. Os usuários que não têm a Sincronização de Senhas ativado serão perguntados se desejam dar permissão para ativar o Monitor de Senhas. Eles serão solicitados quando as seguintes ações ocorrerem:
   - Quando um usuário estiver salvando uma nova senha.
 
     :::image type="content" source="media/microsoft-edge-security-password-monitor/monitor-save-pw-prompt.png" alt-text="Solicitar para salvar senha":::

   - Quando um usuário fizer login no navegador usando uma senha salva.
  
     :::image type="content" source="media/microsoft-edge-security-password-monitor/monitor-after-signin.png" alt-text="Solicitação de confirmação após entrar":::
   
- Ativação direta. Os usuários podem ir a **Configurações** > **Senhas** a qualquer momento e ativar ou desativar o recurso.

## <a name="user-scenarios-with-password-monitor-auto-enabled"></a>Cenários de usuário com Monitor de Senha habilitado automaticamente

A tabela a seguir mostra cenários em que o Monitor de Senhas é habilitado automaticamente e como ele funcionará em dispositivos do usuário.

| Cenário | Condições básicas | Impacto |
|--|--|--|
| 1 com Sincronização em | Sincronização ATIVADA<br>Recurso habilitado anteriormente: Não<br>Resposta à Interface do Usuário de Consentimento: Nenhum | Recurso habilitado por padrão e um balão de aviso são mostrados 2 mins após o navegador ser iniciado.<br>- Se a sincronização estiver desativada depois disso, o recurso será desabilitado.<br>- Recurso desligado antes de alterar a sincronização, a sincronização não afetará mais o recurso.   |
| 2 com Sincronização ativada | Sincronização ATIVADA<br>Recurso habilitado anteriormente: Sim<br>Resposta à Interface do Usuário de Consentimento: Nenhuma | O recurso permanece o mesmo que a escolha do usuário.  O balão de aviso não é mostrado e não há nenhum efeito da alteração de sincronização no valor do recurso.|
| 3 com Sincronização desligada | Sincronização desligada<br>Recurso habilitado anteriormente: Não<br>Resposta à Interface do Usuário de Consentimento: Nenhuma | A sincronização estará desativada e o recurso ficará desabilitado<br>- A qualquer momento depois disso, se o usuário ativar a sincronização sem alterar o recurso: o recurso é habilitado e a notificação de ativar automaticamente é mostrada 2 minutos após a sincronização ser ativada. <br> - Se a sincronização estiver desativada novamente, o recurso será desabilitado <br>- Se o recurso for alterado antes de a sincronização ser ativada, a sincronização não afetará mais o Monitor de Senhas.  |  
| 4 com Sincronização desligada | Sincronização DESATIVADA<br>Recurso habilitado anteriormente: Sim<br>Resposta à Interface do Usuário de Consentimento: Nenhuma | O recurso permanece o mesmo da escolha do usuário, o balãi de aviso não é mostrado e não há efeito de alteração de sincronização no valor do recurso.  |

Além disso, se um usuário tiver entrado usando uma conta de trabalho restrita por meio de políticas para qualquer um dos seguintes, o recurso NÃO será habilitado automaticamente para eles:

- O Monitor de Senhas está desabilitado  
- A Sincronização de Senhas está desabilitada
- O compartilhamento de dados com servidores da Microsoft está desabilitado

## <a name="frequently-asked-questions"></a>Perguntas Frequentes

### <a name="how-can-password-monitor-be-disabled-for-my-organization"></a>Como o Monitor de Senhas pode ser desabilitado para minha organização?

Você pode desabilitar o Monitor de Senhas para sua organização:
- Usando a política de grupo PasswordMonitorAllowed.
- Impedindo que os dados sejam sincronizados e enviados aos servidores da Microsoft.

  > [!NOTE]
  > O Monitor de Senhas pode funcionar mesmo se a Sincronização de Senha estiver desabilitada, desde que o usuário tenha dado consentimento explícito para ativar o recurso ou o tiver ativado por meio de Configurações.

### <a name="what-happens-if-a-user-for-whom-the-feature-has-been-auto-enabled-turns-password-monitor-off-via-settings"></a>O que acontece se um usuário para o qual o recurso tenha sido habilitado automaticamente ative o Monitor de Senhas por meio das Configurações?

A configuração do usuário é a mesma e o recurso permanecerá desabilitado para esse usuário. No entanto, eles podem ser mostrados uma caixa de diálogo de consentimento novamente caso nunca tenham respondido anteriormente à solicitação de consentimento.

## <a name="see-also"></a>Veja também

- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)