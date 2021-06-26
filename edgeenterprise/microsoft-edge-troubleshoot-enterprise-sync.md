---
title: Diagnosticar e corrigir problemas de sincronização do Microsoft Edge
ms.author: collw
author: dan-wesley
manager: silvanam
ms.date: 03/08/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Diretrizes e ferramentas que um administrador do Microsoft Edge pode usar para solucionar e corrigir problemas comuns de sincronização empresarial
ms.openlocfilehash: d934e1ad73500fcb7f15bcd7dd29cb0f905577c5
ms.sourcegitcommit: 4192328ee585bc32a9be528766b8a5a98e046c8e
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/25/2021
ms.locfileid: "11617901"
---
# <a name="diagnose-and-fix-microsoft-edge-sync-issues"></a>Diagnosticar e corrigir problemas de sincronização do Microsoft Edge

Este artigo fornece as diretrizes para a solução dos problemas mais comuns de sincronização encontrados em um ambiente do Azure Active Directory (Azure AD). Ele também inclui as ferramentas recomendadas para coletar os logs necessários para a solução de problemas de sincronização.

Se um usuário estiver com problemas na sincronização de dados do navegador em seus dispositivos, ele poderá tentar [redefinir a sincronização.](edge-learnmore-reset-data-in-cloud.md) Se isso não funcionar, os administradores ou a equipe de suporte podem usar as seguintes diretrizes para corrigir um problema de sincronização.

> [!NOTE]
> Aplica-se ao Microsoft Edge versão 77 ou posterior, a menos que indicado de outra forma.

## <a name="identity-issues-versus-sync-issues"></a>Problemas de identidade versus problemas de sincronização

Antes de começar, é importante entender a diferença entre problemas de identidade e problemas de sincronização. Um caso de uso popular para manter a identidade do usuário no navegador é dar suporte à sincronização. Por esta razão, os problemas com identidade são frequentemente confundidos com problemas de sincronização. Entenda a diferença entre problemas de identidade e de sincronização antes de começar a solucionar os problemas de sincronização.

Antes de tratar um problema como sendo de sincronização, verifique se o usuário está conectado ao navegador com uma conta válida.

A próxima captura de tela mostra um exemplo de um erro de identidade. O erro é "**Last Token Error, EDGE_AUTH_ERROR: 3, 54, 3ea**", que é encontrado no *edge://sync-internals* em **Credenciais**:

:::image type="content" source="media/microsoft-edge-enterprise-sync-configure-and-troubleshoot/sync-identity-issue.png" alt-text="Last Token Error EDGE_AUTH_ERROR: 3,54, 3ea":::

## <a name="common-sync-issues"></a>Problemas comuns de sincronização

### <a name="issue-cant-access-m365-or-azure-information-protection-subscription"></a>Problema: Não é possível acessar a assinatura do M365 ou a da Proteção de Informações do Azure

Você tem uma assinatura anterior do M365 ou da AIP (Proteção de Informações do Azure) que expirou e foi substituída por uma nova assinatura? Nesse caso, a ID do locatário foi alterada e os dados de serviço precisam ser reajustados. Confira as instruções para redefinir os dados no problema **Erro de criptógrafo encontrado**.

### <a name="issue-sync-is-not-available-for-this-account"></a>Problema: "A sincronização não está disponível para esta conta".

Se este erro for encontrado para uma conta do Azure Active Directory, ou se DISABLED_BY_ADMIN aparecer em *edge://sync-internals*, siga as etapas no próximo procedimento sequencialmente até que o problema seja corrigido.

> [!NOTE]
> Como a origem deste erro geralmente requer uma alteração de configuração em um locatário do Azure Active Directory, estas etapas de solução de problemas só podem ser executadas por um administrador do locatário e não por usuários finais.

1. Verifique se o locatário corporativo tem uma assinatura do M365 com suporte. A lista atual dos tipos de assinatura disponíveis está [fornecida aqui](/azure/information-protection/activate-office365). Se o locatário não tiver uma assinatura com suporte, é possível comprar a Proteção de Informações do Azure separadamente, ou atualizar para uma das assinaturas com suporte.
2. Se uma assinatura com suporte estiver disponível, verifique se o locatário tem a AIP (Proteção de Informações do Microsoft Azure) disponível. As instruções para verificar o status da AIP e, se necessário, ativar a AIP estão [aqui](/azure/information-protection/activate-office365).
3. Se a etapa 2 mostrar que a AIP está ativa, mas a sincronização ainda não funciona, ative o ESR (Enterprise State Roaming). As instruções para habilitar o ESR estão [aqui](/azure/active-directory/devices/enterprise-state-roaming-enable). Observe que o ESR não precisa permanecer ativado. Você pode desativar o ESR se esta etapa corrigir o problema.
4. Confirme se a Proteção de Informações do Azure não tem escopo por meio de uma política de integração. Use o miniaplicativo [Get-AadrmOnboardingControlPolicy](/powershell/module/aadrm/get-aadrmonboardingcontrolpolicy?view=azureipps) do PowerShell para ver se o escopo está habilitado. Os dois exemplos a seguir mostram uma configuração com escopo e outra sem escopo para um grupo de segurança específico.

   ```powershell
    PS C:\Work\scripts\PowerShell> Get-AadrmOnboardingControlPolicy
 
    UseRmsUserLicense SecurityGroupObjectId                Scope
    ----------------- ---------------------                -----
                False 
   ```

   ```powershell

    PS C:\Work\scripts\PowerShell> Get-AadrmOnboardingControlPolicy
 
    UseRmsUserLicense SecurityGroupObjectId                Scope
    ----------------- ---------------------                -----
                False f1488a05-8196-40a6-9483-524948b90282   All
   ```

   Se o escopo estiver habilitado, o usuário afetado deverá ser adicionado ao grupo de segurança para o escopo, ou o escopo deverá ser removido. No exemplo abaixo, a integração definiu a AIP para o grupo de segurança indicado e o escopo deve ser removido com o miniplicativo [Set-AadrmOnboardingControlPolicy](/powershell/module/aadrm/set-aadrmonboardingcontrolpolicy?view=azureipps) do PowerShell.

5. Confirme se o IPCv3Service está ativado no locatário. O miniaplicativo [Get-AadrmConfiguration](/powershell/module/aadrm/get-aadrmconfiguration?view=azureipps) do PowerShell mostra o status do serviço.

   :::image type="content" source="media/microsoft-edge-enterprise-sync-configure-and-troubleshoot/sync-scoped-cfg-example.png" alt-text="Verifique se IPCv3Service está habilitado.":::

6. Se o problema não for corrigido, contate o [suporte do Microsoft Edge](https://www.microsoftedgeinsider.com/support).

### <a name="issue-stuck-at-setting-up-sync-or-couldnt-connect-to-the-sync-server-retrying"></a>Problema: Travado em "Configurando a sincronização..." ou "Não foi possível se conectar ao servidor de sincronização. Tentando novamente..."

1. Tente sair e entrar novamente.
2. Vá para *edge://sync-internals*. Se na seção "**Informações do tipo**" o seguinte erro estiver presente, pule para o problema a seguir, **Erro de criptógrafo encontrado**.

   `"Error:GenerateCryptoErrorsForTypes@../../components/sync/driver/data_type_manager_impl.cc:42, cryptographer error was encountered"`

3. Tente executar ping no ponto de extremidade do servidor. O ponto de extremidade do servidor para um cliente está disponível em *edge://sync-internals*. A próxima captura de tela mostra informações do ponto de extremidade em **Informações do Ambiente**.

   :::image type="content" source="media/microsoft-edge-enterprise-sync-configure-and-troubleshoot/sync-endpoint-info.png" alt-text="Informações sobre o ponto de extremidade":::

4. Se o ponto de extremidade do servidor estiver vazio, ou se o servidor não puder ser pingado e um firewall estiver presente no ambiente, confirme se os pontos de extremidade de serviço necessários estão disponíveis para o computador cliente.

   - Pontos de extremidade do serviço de sincronização do Microsoft Edge:
     - [https://edge-enterprise.activity.windows.com](https://edge-enterprise.activity.windows.com)
     - [https://edge.activity.windows.com](https://edge.activity.windows.com)
    - Pontos de extremidade da Proteção de Informações do Azure:
      - [https://api.aadrm.com](https://api.aadrm.com) (para a maioria dos locatários)
      - [https://api.aadrm.de](https://api.aadrm.de) (para locatários na Alemanha)
      - [https://api.aadrm.cn](https://api.aadrm.cn) (para locatários na China)
   - [Pontos de Extremidade do Serviço de Notificação do Windows](/windows/uwp/design/shell/tiles-and-notifications/firewall-allowlist-config).

5. Se o problema ainda não estiver corrigido, entre em contato com o [suporte do Microsoft Edge.](https://www.microsoftedgeinsider.com/support)

### <a name="issue-cryptographer-error-encountered"></a>Problema: erro de criptógrafo encontrado

Este erro está visível em **Informações do tipo** em *edge://sync-internals*, e isso poderá significar que os dados do lado de serviço do usuário precisam ser redefinidos. O exemplo a seguir mostra uma mensagem de erro de criptografia:
<br>"Error:GenerateCryptoErrorsForTypes@.. /.. /components/sync/driver/data_type_manager_impl.cc:42, erro criptografador encontrado".

1. Reinicie o Microsoft Edge e navegue até *edge://sync-internals* e verifique a seção “**Status da Chave de Conta do AAD**”
   - "Êxito" em "Último Resultado do MIP": o erro de criptógrafo significa que os dados do servidor podem ser criptografados com uma chave perdida. É necessário a redefinição dos dados para retomar a sincronia.
   - "Sem permissões" em "Último Resultado do MIP": possivelmente isso foi causado por uma alteração no Azure AD ou por alterações na assinatura do locatário. É necessário a redefinição dos dados para retomar a sincronia.
   - Outros erros podem significar problemas de configuração do servidor.
2. Se a redefinição de dados for necessária, confira [Redefinir dados do Microsoft Edge na nuvem](edge-learnmore-reset-data-in-cloud.md).

### <a name="issue-sync-has-been-turned-off-by-your-administrator"></a>Problema: "A sincronização foi desativada pelo administrador".

Verifique se a [política SyncDisabled ](./microsoft-edge-policies.md#syncdisabled) não está definida.

## <a name="see-also"></a>Veja também

- [Sincronização do Microsoft Edge Enterprise](microsoft-edge-enterprise-sync.md)
- [Microsoft Edge e Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md)
- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)