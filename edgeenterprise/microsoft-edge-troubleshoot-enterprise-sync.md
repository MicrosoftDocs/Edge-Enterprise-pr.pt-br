---
title: Diagnosticar e corrigir problemas de sincronização do Microsoft Edge
ms.author: collw
author: dan-wesley
manager: silvanam
ms.date: 07/07/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Diretrizes e ferramentas que um administrador do Microsoft Edge pode usar para solucionar e corrigir problemas comuns de sincronização empresarial
ms.openlocfilehash: 540eaff5016a76fbdb308c5f207de45d1c1e3d11
ms.sourcegitcommit: 42a3ee7e4b91efb49ee99b3c4cbb1be185347b1b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/07/2022
ms.locfileid: "12635806"
---
# <a name="diagnose-and-fix-microsoft-edge-sync-issues"></a>Diagnosticar e corrigir problemas de sincronização do Microsoft Edge

Este artigo fornece diretrizes de solução de problemas para os problemas de sincronização mais comuns em um ambiente do Azure Active Directory (Azure AD). Ele também inclui etapas de solução de problemas e as ferramentas recomendadas para coletar os logs necessários para solucionar um problema de sincronização.

 Se um usuário estiver enfrentando um problema ao sincronizar dados do navegador em seus dispositivos, ele poderá redefinir a sincronização na sincronização de Redefinição de Sincronização de **Perfis** > **** > **** > **de Configurações**. Se a redefinição de sincronização não funcionar, um administrador ou membro da equipe de suporte poderá usar as diretrizes neste artigo para corrigir um problema de sincronização.

> [!NOTE]
> Aplica-se ao Microsoft Edge no Chromium, versão 77 ou posterior, a menos que indicado de outra forma.

## <a name="before-you-begin-identity-issues-versus-sync-issues"></a>Antes de começar: problemas de identidade versus problemas de sincronização

É importante entender a diferença entre problemas de identidade e problemas de sincronização. Um caso de uso popular para manter a identidade do usuário no navegador é dar suporte à sincronização. Por esta razão, os problemas com identidade são frequentemente confundidos com problemas de sincronização. Entenda a diferença entre problemas de identidade e de sincronização antes de começar a solucionar os problemas de sincronização.

Antes de tratar um problema como sendo de sincronização, verifique se o usuário está conectado ao navegador com uma conta válida.

A próxima captura de tela mostra um exemplo de um erro de identidade. O erro é **Last Token Error, EDGE_AUTH_ERROR: 3, 54, 3ea**, que é encontrado *edge://sync-internals em* **Credenciais**.

:::image type="content" source="media/microsoft-edge-enterprise-sync-configure-and-troubleshoot/sync-identity-issue3.png" alt-text="Last Token Error EDGE_AUTH_ERROR: 3,54, 3ea":::

## <a name="basic-troubleshooting-steps"></a>Etapas básicas de solução de problemas

Antes de começar a solucionar problemas, verifique os problemas [comuns de](#common-sync-issues) sincronização para ver se algum desses problemas se aplica ao seu problema de sincronização.

Use as etapas a seguir como um guia para solucionar um problema de sincronização.

1. Entre em seu Office 365 ou no portal de administração do Microsoft 365 e verifique se sua licença é válida.
2. Entre em seu portal do Azure e verifique se sua licença do Azure é válida.
3. Saia da sua conta em todos os navegadores do Microsoft Edge em todos os computadores e/ou dispositivos móveis, não apenas aquele que você está usando.
4. Verifique se você está na versão mais recente do Microsoft Edge que dá suporte a todos os recursos de sincronização (pelo menos 98.0.1108.43 (build oficial) (64 bits)).
5. Entre novamente em seu perfil no Microsoft Edge. Recomendamos que você faça uma redefinição de sincronização. Para obter mais informações, [consulte Executar uma redefinição para corrigir um problema de sincronização](/deployedge/edge-learnmore-reset-data-in-cloud#perform-a-reset-to-fix-a-synchronization-problem).
6. Verifique se sua conta está habilitada para sincronização. Em uma nova guia, vá para: *edge://sync-internals/*. A seção Resumo, mostrada na próxima captura de tela, mostra que a sincronização está habilitada.

   :::image type="content" source="media/microsoft-edge-enterprise-sync-configure-and-troubleshoot/summary-confirm-sync-working.png" alt-text="Resumo de sync-internals":::

7. Verifique se o dispositivo em que você está sendo sincronizado está sendo sincronizado. Vá para *edge://sync-internals/* e selecione a guia Navegador **do Nó de Sincronização** . Abra a **pasta Informações do** dispositivo para ver quais dispositivos estão na lista de sincronização.
8. Verifique o status de entrada. Vá para *edge://signin-internals/*. A próxima captura de tela mostra o status de entrada de um usuário.

   :::image type="content" source="media/microsoft-edge-enterprise-sync-configure-and-troubleshoot/sync-get-signin-status-for-sync.png" alt-text="Obter o status de entrada de sign-internals":::

9. Verifique se há alguma política que possa impedir a sincronização. Vá para *edge://policy/* para ver a página Políticas. A próxima captura de tela mostra um exemplo de políticas ativas para um usuário conectado. Esta página também mostra a Precedência de Política e Microsoft Edge Update Políticas.

   :::image type="content" source="media/microsoft-edge-enterprise-sync-configure-and-troubleshoot/sync-ts-get-active-policies2.png" alt-text="Página Políticas para o usuário conectado":::

## <a name="common-sync-issues"></a>Problemas comuns de sincronização

### <a name="issue-cant-access-microsoft-365-or-azure-information-protection-subscription"></a>Problema: não é possível acessar a assinatura do Microsoft 365 ou Proteção de Informações Azure

Você tem uma assinatura anterior do Microsoft 365 ou do AIP (Azure Proteção de Informações) que expirou e foi substituída por uma nova assinatura? Nesse caso, a ID do locatário foi alterada e os dados de serviço precisam ser reajustados. Consulte as instruções para redefinir dados em [Problema: erro do Cryptographer encontrado](#issue-cryptographer-error-encountered).

### <a name="issue-sync-is-not-available-for-this-account"></a>Problema: "A sincronização não está disponível para esta conta".

Se este erro for encontrado para uma conta do Azure Active Directory, ou se DISABLED_BY_ADMIN aparecer em *edge://sync-internals*, siga as etapas no próximo procedimento sequencialmente até que o problema seja corrigido.

> [!NOTE]
> Como a origem desse erro geralmente precisa de uma alteração de configuração em um locatário do Azure Active Directory, essas etapas de solução de problemas só podem ser executadas por um administrador de locatários.

1. Verifique se o locatário corporativo tem uma das assinaturas com suporte em [Configurar a sincronização corporativa do Microsoft Edge](/deployedge/microsoft-edge-enterprise-sync). Para descobrir qual assinatura você tem, consulte [Qual assinatura eu tenho?](/microsoft-365/admin/admin-overview/what-subscription-do-i-have). Se o locatário não tiver uma assinatura com suporte, é possível comprar a Proteção de Informações do Azure separadamente, ou atualizar para uma das assinaturas com suporte.
2. Se uma assinatura com suporte estiver disponível, verifique se o locatário tem o AIP (Azure Proteção de Informações). Se você precisar verificar o status da AIP e, se necessário, ativar a AIP, confira estas instruções: Ativando o serviço de proteção do [Azure Proteção de Informações](/azure/information-protection/activate-service).
3. Se a etapa 2 mostrar que a AIP está ativa, mas a sincronização ainda não funciona, ative o ESR (Enterprise State Roaming). Se você precisar habilitar o ESR, confira estas instruções: Habilitar [o Enterprise State Roaming no Azure Active Directory](/azure/active-directory/devices/enterprise-state-roaming-enable).

   > [!NOTE]
   > ESR não precisa ficar. Você pode desativar o ESR se esta etapa corrigir o problema.

4. Confirme se o Proteção de Informações do Azure não está no escopo por meio de uma política de integração. Você pode usar o cmdlet [Get-AIPServiceOnboardingControlPolicy](/powershell/module/aipservice/get-aipserviceonboardingcontrolpolicy) do PowerShell para ver se o escopo está habilitado. Verifique se o monitor aIPService do PowerShell está instalado. Você pode obtê-lo aqui: [instale o módulo AIPService do PowerShell para o Azure Proteção de Informações](/azure/information-protection/install-powershell). Os dois exemplos a seguir mostram uma configuração com escopo e outra sem escopo para um grupo de segurança específico.

   ```powershell
    PS C:\Work\scripts\PowerShell> Get-AIPServiceOnboardingControlPolicy
 
    UseRmsUserLicense SecurityGroupObjectId                Scope
    ----------------- ---------------------                -----
                False 
   ```

   ```powershell

    PS C:\Work\scripts\PowerShell> Get-AIPServiceOnboardingControlPolicy
 
    UseRmsUserLicense SecurityGroupObjectId                Scope
    ----------------- ---------------------                -----
                False f1488a05-8196-40a6-9483-524948b90282   All
   ```

   Se o escopo estiver habilitado, o usuário afetado deverá ser adicionado ao grupo de segurança para o escopo, ou o escopo deverá ser removido. O escopo pode ser removido com o applet [Set-AIPServiceOnboardingControlPolicy](/powershell/module/aipservice/set-aipserviceonboardingcontrolpolicy) do PowerShell.

5. Confirme se o IPCv3Service está ativado no locatário. O cmdlet [Get-AIPServiceConfiguration](/powershell/module/aipservice/get-aipserviceconfiguration) do PowerShell mostra o status do serviço.

   :::image type="content" source="media/microsoft-edge-enterprise-sync-configure-and-troubleshoot/sync-scoped-cfg-example.png" alt-text="Verifique se IPCv3Service está habilitado.":::

6. Se o problema não for corrigido, contate o [suporte do Microsoft Edge](https://www.microsoftedgeinsider.com/support).

### <a name="issue-stuck-at-setting-up-sync-or-couldnt-connect-to-the-sync-server-retrying"></a>Problema: preso em "Configurando sincronização..." ou "Não foi possível se conectar ao servidor de sincronização. Tentando novamente..."

1. Tente sair e entrar novamente.
2. Vá para *edge://sync-internals*. Se o erro a seguir aparecer na seção **Informações de** tipo, vá para o [erro cryptographer encontrado.](#issue-cryptographer-error-encountered)

   `"Error:GenerateCryptoErrorsForTypes@../../components/sync/driver/data_type_manager_impl.cc:42, cryptographer error was encountered"`

3. Tente executar ping no ponto de extremidade do servidor. O ponto de extremidade do servidor para um cliente está disponível em *edge://sync-internals*. A próxima captura de tela mostra informações do ponto de extremidade em **Informações do Ambiente**.

   :::image type="content" source="media/microsoft-edge-enterprise-sync-configure-and-troubleshoot/sync-endpoint-info2.png" alt-text="Informações sobre o ponto de extremidade":::

4. Se o ponto de extremidade do servidor estiver vazio ou se o servidor não puder executar ping porque há um firewall no ambiente, confirme se os pontos de extremidade de serviço necessários estão disponíveis para o dispositivo cliente.

   - Pontos de extremidade do serviço de sincronização do Microsoft Edge:
     - `https://edge-enterprise.activity.windows.com`
     - `https://edge.activity.windows.com`
    - Pontos de extremidade da Proteção de Informações do Azure:
      - `https://api.aadrm.com` (para a maioria dos locatários)
      - `https://api.aadrm.de` (para locatários na Alemanha)
      - `https://api.aadrm.cn` (para locatários na China)
   - [Configurações de Firewall corporativo para dar suporte ao tráfego do WNS](/windows/uwp/design/shell/tiles-and-notifications/firewall-allowlist-config).

5. Se o problema ainda não estiver corrigido, entre em contato com o [suporte do Microsoft Edge.](https://www.microsoftedgeinsider.com/support)

### <a name="issue-cryptographer-error-encountered"></a>Problema: erro de criptógrafo encontrado

Esse erro é visível em **Informações** de tipo *no edge://sync-internals* e pode significar que os dados do lado do serviço do usuário precisam ser redefinidos. O próximo exemplo mostra uma mensagem de erro de criptografia:

`"Error:GenerateCryptoErrorsForTypes@../../components/sync/driver/data_type_manager_impl.cc:42, cryptographer error was encountered".`

Use as seguintes etapas para corrigir esse problema:

1. Reinicie o Microsoft Edge e *vá para edge://sync-internals*. Examine a seção **Status da Chave de Conta do AAD** para ver se alguma das seguintes mensagens está presente:
   - Último Resultado da MIP = "Êxito": esse erro significa que os dados do servidor podem ser criptografados com uma chave perdida. Uma redefinição de dados é necessária para retomar a sincronização.
   - Último Resultado da MIP = "Sem permissões": é possivelmente causado por uma alteração Azure AD ou alterações de assinatura de locatário. Uma redefinição de dados é necessária para retomar a sincronização.
   - Outros erros podem significar que há um problema de configuração do servidor.
2. Se uma redefinição de dados for necessária, consulte [Redefinir dados do Microsoft Edge na nuvem](edge-learnmore-reset-data-in-cloud.md).

### <a name="issue-sync-has-been-turned-off-by-your-administrator"></a>Problema: "A sincronização foi desativada pelo administrador".

Verifique se a [política SyncDisabled](./microsoft-edge-policies.md#syncdisabled) não está definida.

## <a name="see-also"></a>Ver também

- [Sincronização do Microsoft Edge Enterprise](microsoft-edge-enterprise-sync.md)
- [Perguntas frequentes sobre sincronização de empresa do Microsoft Edge](microsoft-edge-enterprise-sync-faq.md)
- [Microsoft Edge e Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md)
- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)