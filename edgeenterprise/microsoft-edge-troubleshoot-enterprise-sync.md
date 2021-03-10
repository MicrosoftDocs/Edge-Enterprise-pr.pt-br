---
title: Diagnosticar e corrigir problemas de sincronização do Microsoft Edge
ms.author: scottbo
author: dan-wesley
manager: silvanam
ms.date: 03/08/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Diretrizes e ferramentas que um administrador do Microsoft Edge pode usar para solucionar e corrigir problemas comuns de sincronização empresarial
ms.openlocfilehash: 767b26c74e91213b407e8264a8ed185f38dfc2e9
ms.sourcegitcommit: 86e0de9b27ad4297a6d5a57c866d7ef4fc7bb0cd
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "11400175"
---
# <a name="diagnose-and-fix-microsoft-edge-sync-issues"></a><span data-ttu-id="f0f23-103">Diagnosticar e corrigir problemas de sincronização do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="f0f23-103">Diagnose and fix Microsoft Edge sync issues</span></span>

<span data-ttu-id="f0f23-104">Este artigo fornece as diretrizes para a solução dos problemas mais comuns de sincronização encontrados em um ambiente do Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="f0f23-104">This article provides troubleshooting guidance for the most commonly encountered sync issues in an Azure Active Directory (Azure AD) environment.</span></span> <span data-ttu-id="f0f23-105">Ele também inclui as ferramentas recomendadas para coletar os logs necessários para a solução de problemas de sincronização.</span><span class="sxs-lookup"><span data-stu-id="f0f23-105">It also includes the recommended tools for gathering the logs needed for troubleshooting a sync issue.</span></span>

<span data-ttu-id="f0f23-106">Se um usuário estiver com problemas na sincronização de dados do navegador em seus dispositivos, ele poderá tentar [redefinir a sincronização.](edge-learnmore-reset-data-in-cloud.md) Se isso não funcionar, os administradores ou a equipe de suporte podem usar as seguintes diretrizes para corrigir um problema de sincronização.</span><span class="sxs-lookup"><span data-stu-id="f0f23-106">If a user is experiencing an issue syncing browser data across their devices they can try [resetting sync](edge-learnmore-reset-data-in-cloud.md). If this doesn't work, admins or support staff can use the following guidance to fix a sync issue.</span></span>

> [!NOTE]
> <span data-ttu-id="f0f23-107">Aplica-se ao Microsoft Edge versão 77 ou posterior, a menos que indicado de outra forma.</span><span class="sxs-lookup"><span data-stu-id="f0f23-107">Applies to Microsoft Edge version 77 or later unless otherwise noted.</span></span>

## <a name="identity-issues-versus-sync-issues"></a><span data-ttu-id="f0f23-108">Problemas de identidade versus problemas de sincronização</span><span class="sxs-lookup"><span data-stu-id="f0f23-108">Identity issues versus sync issues</span></span>

<span data-ttu-id="f0f23-109">Antes de começar, é importante entender a diferença entre problemas de identidade e problemas de sincronização.</span><span class="sxs-lookup"><span data-stu-id="f0f23-109">Before you begin it's important to understand the difference between identity issues and sync issues.</span></span> <span data-ttu-id="f0f23-110">Um caso de uso popular para manter a identidade do usuário no navegador é dar suporte à sincronização. Por esta razão, os problemas com identidade são frequentemente confundidos com problemas de sincronização.</span><span class="sxs-lookup"><span data-stu-id="f0f23-110">A popular use case for maintaining user identity in the browser is to support sync. For this reason, identity issues are frequently confused with sync issues.</span></span> <span data-ttu-id="f0f23-111">Entenda a diferença entre problemas de identidade e de sincronização antes de começar a solucionar os problemas de sincronização.</span><span class="sxs-lookup"><span data-stu-id="f0f23-111">Understand the difference between identity and sync issue before you start troubleshooting sync.</span></span>

<span data-ttu-id="f0f23-112">Antes de tratar um problema como sendo de sincronização, verifique se o usuário está conectado ao navegador com uma conta válida.</span><span class="sxs-lookup"><span data-stu-id="f0f23-112">Before you treat an issue as a sync issue, check to see if the user is signed into the browser with a valid account.</span></span>

<span data-ttu-id="f0f23-113">A próxima captura de tela mostra um exemplo de um erro de identidade.</span><span class="sxs-lookup"><span data-stu-id="f0f23-113">The next screenshot shows an example of an identity error.</span></span> <span data-ttu-id="f0f23-114">O erro é "**Last Token Error, EDGE_AUTH_ERROR: 3, 54, 3ea**", que é encontrado no *edge://sync-internals* em **Credenciais**:</span><span class="sxs-lookup"><span data-stu-id="f0f23-114">The error is "**Last Token Error, EDGE_AUTH_ERROR: 3, 54, 3ea**", which is found in *edge://sync-internals* under **Credentials**:</span></span>

:::image type="content" source="media/microsoft-edge-enterprise-sync-configure-and-troubleshoot/sync-identity-issue.png" alt-text="Last Token Error EDGE_AUTH_ERROR: 3,54, 3ea":::

## <a name="common-sync-issues"></a><span data-ttu-id="f0f23-116">Problemas comuns de sincronização</span><span class="sxs-lookup"><span data-stu-id="f0f23-116">Common sync issues</span></span>

### <a name="issue-cant-access-m365-or-azure-information-protection-subscription"></a><span data-ttu-id="f0f23-117">Problema: Não é possível acessar a assinatura do M365 ou a da Proteção de Informações do Azure</span><span class="sxs-lookup"><span data-stu-id="f0f23-117">Issue: Can't access M365 or Azure Information Protection subscription</span></span>

<span data-ttu-id="f0f23-118">Você tem uma assinatura anterior do M365 ou da AIP (Proteção de Informações do Azure) que expirou e foi substituída por uma nova assinatura?</span><span class="sxs-lookup"><span data-stu-id="f0f23-118">Do you have a previous M365 or Azure Information Protection (AIP) subscription that expired and then replaced with a new subscription?</span></span> <span data-ttu-id="f0f23-119">Nesse caso, a ID do locatário foi alterada e os dados de serviço precisam ser reajustados.</span><span class="sxs-lookup"><span data-stu-id="f0f23-119">If so, then the tenant ID has changed and the service data needs to be reset.</span></span> <span data-ttu-id="f0f23-120">Confira as instruções para redefinir os dados no problema **Erro de criptógrafo encontrado**.</span><span class="sxs-lookup"><span data-stu-id="f0f23-120">See the instructions for resetting data in the **Cryptographer error encountered** issue.</span></span>

### <a name="issue-sync-is-not-available-for-this-account"></a><span data-ttu-id="f0f23-121">Problema: "A sincronização não está disponível para esta conta".</span><span class="sxs-lookup"><span data-stu-id="f0f23-121">Issue: “Sync is not available for this account.”</span></span>

<span data-ttu-id="f0f23-122">Se este erro for encontrado para uma conta do Azure Active Directory, ou se DISABLED_BY_ADMIN aparecer em *edge://sync-internals*, siga as etapas no próximo procedimento sequencialmente até que o problema seja corrigido.</span><span class="sxs-lookup"><span data-stu-id="f0f23-122">If this error is encountered for an Azure Active Directory account, or if DISABLED_BY_ADMIN appears in *edge://sync-internals*, follow the steps in the next procedure sequentially until the problem is fixed.</span></span>

> [!NOTE]
> <span data-ttu-id="f0f23-123">Como a origem deste erro geralmente requer uma alteração de configuração em um locatário do Azure Active Directory, estas etapas de solução de problemas só podem ser executadas por um administrador do locatário e não por usuários finais.</span><span class="sxs-lookup"><span data-stu-id="f0f23-123">Because the source of this error is usually requires a configuration change in an Azure Active Directory tenant, these troubleshooting steps can only performed by a tenant admin and not by end users.</span></span>

1. <span data-ttu-id="f0f23-124">Verifique se o locatário corporativo tem uma assinatura do M365 com suporte.</span><span class="sxs-lookup"><span data-stu-id="f0f23-124">Verify that the enterprise tenant has a supported M365 subscription.</span></span> <span data-ttu-id="f0f23-125">A lista atual dos tipos de assinatura disponíveis está [fornecida aqui](https://docs.microsoft.com/azure/information-protection/activate-office365).</span><span class="sxs-lookup"><span data-stu-id="f0f23-125">The current list of available subscription types is [provided here](https://docs.microsoft.com/azure/information-protection/activate-office365).</span></span> <span data-ttu-id="f0f23-126">Se o locatário não tiver uma assinatura com suporte, é possível comprar a Proteção de Informações do Azure separadamente, ou atualizar para uma das assinaturas com suporte.</span><span class="sxs-lookup"><span data-stu-id="f0f23-126">If the tenant doesn't have a supported subscription, they can either purchase Azure Information Protection separately, or upgrade to one of the supported subscriptions.</span></span>
2. <span data-ttu-id="f0f23-127">Se uma assinatura com suporte estiver disponível, verifique se o locatário tem a AIP (Proteção de Informações do Microsoft Azure) disponível.</span><span class="sxs-lookup"><span data-stu-id="f0f23-127">If a supported subscription is available, verify that the tenant has Azure Information Protection (AIP) available.</span></span> <span data-ttu-id="f0f23-128">As instruções para verificar o status da AIP e, se necessário, ativar a AIP estão [aqui](https://docs.microsoft.com/azure/information-protection/activate-office365).</span><span class="sxs-lookup"><span data-stu-id="f0f23-128">The instructions for checking the AIP status and, if necessary, activating AIP are [here](https://docs.microsoft.com/azure/information-protection/activate-office365).</span></span>
3. <span data-ttu-id="f0f23-129">Se a etapa 2 mostrar que a AIP está ativa, mas a sincronização ainda não funciona, ative o ESR (Enterprise State Roaming).</span><span class="sxs-lookup"><span data-stu-id="f0f23-129">If step 2 shows that AIP is active but sync still doesn't work, turn on Enterprise State Roaming (ESR).</span></span> <span data-ttu-id="f0f23-130">As instruções para habilitar o ESR estão [aqui](https://docs.microsoft.com/azure/active-directory/devices/enterprise-state-roaming-enable).</span><span class="sxs-lookup"><span data-stu-id="f0f23-130">The instructions for enabling ESR are [here](https://docs.microsoft.com/azure/active-directory/devices/enterprise-state-roaming-enable).</span></span> <span data-ttu-id="f0f23-131">Observe que o ESR não precisa permanecer ativado.</span><span class="sxs-lookup"><span data-stu-id="f0f23-131">Note that ESR does not need to stay on.</span></span> <span data-ttu-id="f0f23-132">Você pode desativar o ESR se esta etapa corrigir o problema.</span><span class="sxs-lookup"><span data-stu-id="f0f23-132">You can turn off ESR if this step fixes the issue.</span></span>
4. <span data-ttu-id="f0f23-133">Confirme se a Proteção de Informações do Azure não tem escopo por meio de uma política de integração.</span><span class="sxs-lookup"><span data-stu-id="f0f23-133">Confirm that Azure Information Protection is not scoped via an onboarding policy.</span></span> <span data-ttu-id="f0f23-134">Use o miniaplicativo [Get-AadrmOnboardingControlPolicy](https://docs.microsoft.com/powershell/module/aadrm/get-aadrmonboardingcontrolpolicy?view=azureipps) do PowerShell para ver se o escopo está habilitado.</span><span class="sxs-lookup"><span data-stu-id="f0f23-134">You can use the [Get-AadrmOnboardingControlPolicy](https://docs.microsoft.com/powershell/module/aadrm/get-aadrmonboardingcontrolpolicy?view=azureipps) PowerShell applet to see if scoping is enabled.</span></span> <span data-ttu-id="f0f23-135">Os dois exemplos a seguir mostram uma configuração com escopo e outra sem escopo para um grupo de segurança específico.</span><span class="sxs-lookup"><span data-stu-id="f0f23-135">The next two examples show an unscoped configuration and a configuration scoped to a specific security group.</span></span>

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

   <span data-ttu-id="f0f23-136">Se o escopo estiver habilitado, o usuário afetado deverá ser adicionado ao grupo de segurança para o escopo, ou o escopo deverá ser removido.</span><span class="sxs-lookup"><span data-stu-id="f0f23-136">If scoping is enabled, the affected user should either be added to the security group for the scope, or the scope should be removed.</span></span> <span data-ttu-id="f0f23-137">No exemplo abaixo, a integração definiu a AIP para o grupo de segurança indicado e o escopo deve ser removido com o miniplicativo [Set-AadrmOnboardingControlPolicy](https://docs.microsoft.com/powershell/module/aadrm/set-aadrmonboardingcontrolpolicy?view=azureipps) do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f0f23-137">In the example below, onboarding has scoped AIP to the indicated security group and the scoping should be removed with the [Set-AadrmOnboardingControlPolicy](https://docs.microsoft.com/powershell/module/aadrm/set-aadrmonboardingcontrolpolicy?view=azureipps) PowerShell applet.</span></span>

5. <span data-ttu-id="f0f23-138">Confirme se o IPCv3Service está ativado no locatário.</span><span class="sxs-lookup"><span data-stu-id="f0f23-138">Confirm that the IPCv3Service is turned on in the tenant.</span></span> <span data-ttu-id="f0f23-139">O miniaplicativo [Get-AadrmConfiguration](https://docs.microsoft.com/powershell/module/aadrm/get-aadrmconfiguration?view=azureipps) do PowerShell mostra o status do serviço.</span><span class="sxs-lookup"><span data-stu-id="f0f23-139">The [Get-AadrmConfiguration](https://docs.microsoft.com/powershell/module/aadrm/get-aadrmconfiguration?view=azureipps)  PowerShell applet shows the status of the service.</span></span>

   :::image type="content" source="media/microsoft-edge-enterprise-sync-configure-and-troubleshoot/sync-scoped-cfg-example.png" alt-text="Verifique se IPCv3Service está habilitado.":::

6. <span data-ttu-id="f0f23-141">Se o problema não for corrigido, contate o [suporte do Microsoft Edge](https://www.microsoftedgeinsider.com/support).</span><span class="sxs-lookup"><span data-stu-id="f0f23-141">If the issue isn't fixed, contact [Microsoft Edge support](https://www.microsoftedgeinsider.com/support).</span></span>

### <a name="issue-stuck-at-setting-up-sync-or-couldnt-connect-to-the-sync-server-retrying"></a><span data-ttu-id="f0f23-142">Problema: Travado em "Configurando a sincronização..." ou "Não foi possível se conectar ao servidor de sincronização.</span><span class="sxs-lookup"><span data-stu-id="f0f23-142">Issue: Stuck at "Setting up sync..." or “Couldn’t connect to the sync server.</span></span> <span data-ttu-id="f0f23-143">Tentando novamente..."</span><span class="sxs-lookup"><span data-stu-id="f0f23-143">Retrying…”</span></span>

1. <span data-ttu-id="f0f23-144">Tente sair e entrar novamente.</span><span class="sxs-lookup"><span data-stu-id="f0f23-144">Try to sign out and then sign in.</span></span>
2. <span data-ttu-id="f0f23-145">Vá para *edge://sync-internals*.</span><span class="sxs-lookup"><span data-stu-id="f0f23-145">Go to *edge://sync-internals*.</span></span> <span data-ttu-id="f0f23-146">Se na seção "**Informações do tipo**" o seguinte erro estiver presente, pule para o problema a seguir, **Erro de criptógrafo encontrado**.</span><span class="sxs-lookup"><span data-stu-id="f0f23-146">If under the "**Type info**" section the following error is present, then  skip to the following issue, **Cryptographer error encountered**.</span></span>

   `"Error:GenerateCryptoErrorsForTypes@../../components/sync/driver/data_type_manager_impl.cc:42, cryptographer error was encountered"`

3. <span data-ttu-id="f0f23-147">Tente executar ping no ponto de extremidade do servidor.</span><span class="sxs-lookup"><span data-stu-id="f0f23-147">Try pinging the server endpoint.</span></span> <span data-ttu-id="f0f23-148">O ponto de extremidade do servidor para um cliente está disponível em *edge://sync-internals*.</span><span class="sxs-lookup"><span data-stu-id="f0f23-148">The server endpoint for a client is available in *edge://sync-internals*.</span></span> <span data-ttu-id="f0f23-149">A próxima captura de tela mostra informações do ponto de extremidade em **Informações do Ambiente**.</span><span class="sxs-lookup"><span data-stu-id="f0f23-149">The next screenshot shows endpoint information under **Environment Info**.</span></span>

   :::image type="content" source="media/microsoft-edge-enterprise-sync-configure-and-troubleshoot/sync-endpoint-info.png" alt-text="Informações sobre o ponto de extremidade":::

4. <span data-ttu-id="f0f23-151">Se o ponto de extremidade do servidor estiver vazio, ou se o servidor não puder ser pingado e um firewall estiver presente no ambiente, confirme se os pontos de extremidade de serviço necessários estão disponíveis para o computador cliente.</span><span class="sxs-lookup"><span data-stu-id="f0f23-151">If the server endpoint is empty, or if server cannot be pinged and a firewall is present in the environment, confirm that the necessary service endpoints are available to the client computer.</span></span>

   - <span data-ttu-id="f0f23-152">Pontos de extremidade do serviço de sincronização do Microsoft Edge:</span><span class="sxs-lookup"><span data-stu-id="f0f23-152">Microsoft Edge sync service endpoints:</span></span>
     - [https://edge-enterprise.activity.windows.com](https://edge-enterprise.activity.windows.com)
     - [https://edge.activity.windows.com](https://edge.activity.windows.com)
    - <span data-ttu-id="f0f23-153">Pontos de extremidade da Proteção de Informações do Azure:</span><span class="sxs-lookup"><span data-stu-id="f0f23-153">Azure Information Protection endpoints:</span></span>
      - <span data-ttu-id="f0f23-154">[https://api.aadrm.com](https://api.aadrm.com) (para a maioria dos locatários)</span><span class="sxs-lookup"><span data-stu-id="f0f23-154">[https://api.aadrm.com](https://api.aadrm.com) (for most tenants)</span></span>
      - <span data-ttu-id="f0f23-155">[https://api.aadrm.de](https://api.aadrm.de) (para locatários na Alemanha)</span><span class="sxs-lookup"><span data-stu-id="f0f23-155">[https://api.aadrm.de](https://api.aadrm.de) (for tenants in Germany)</span></span>
      - <span data-ttu-id="f0f23-156">[https://api.aadrm.cn](https://api.aadrm.cn) (para locatários na China)</span><span class="sxs-lookup"><span data-stu-id="f0f23-156">[https://api.aadrm.cn](https://api.aadrm.cn) (for tenants in China)</span></span>
   - <span data-ttu-id="f0f23-157">[Pontos de Extremidade do Serviço de Notificação do Windows](https://docs.microsoft.com/windows/uwp/design/shell/tiles-and-notifications/firewall-allowlist-config).</span><span class="sxs-lookup"><span data-stu-id="f0f23-157">[Windows Notification Service endpoints](https://docs.microsoft.com/windows/uwp/design/shell/tiles-and-notifications/firewall-allowlist-config).</span></span>

5. <span data-ttu-id="f0f23-158">Se o problema ainda não estiver corrigido, entre em contato com o [suporte do Microsoft Edge.](https://www.microsoftedgeinsider.com/support)</span><span class="sxs-lookup"><span data-stu-id="f0f23-158">If the issue still isn't fixed, contact [Microsoft Edge support](https://www.microsoftedgeinsider.com/support).</span></span>

### <a name="issue-cryptographer-error-encountered"></a><span data-ttu-id="f0f23-159">Problema: erro de criptógrafo encontrado</span><span class="sxs-lookup"><span data-stu-id="f0f23-159">Issue: Cryptographer error encountered</span></span>

<span data-ttu-id="f0f23-160">Este erro está visível em **Informações do tipo** em *edge://sync-internals*, e isso poderá significar que os dados do lado de serviço do usuário precisam ser redefinidos.</span><span class="sxs-lookup"><span data-stu-id="f0f23-160">This error is visible under **Type info** in *edge://sync-internals* and may mean that the user's service side data needs to be reset.</span></span> <span data-ttu-id="f0f23-161">O exemplo a seguir mostra uma mensagem de erro de criptografia:</span><span class="sxs-lookup"><span data-stu-id="f0f23-161">The following example shows a cryptography error message:</span></span>
<br><span data-ttu-id="f0f23-162">"Error:GenerateCryptoErrorsForTypes@.. /.. /components/sync/driver/data_type_manager_impl.cc:42, erro criptografador encontrado".</span><span class="sxs-lookup"><span data-stu-id="f0f23-162">"Error:GenerateCryptoErrorsForTypes@../../components/sync/driver/data_type_manager_impl.cc:42, cryptographer error was encountered".</span></span>

1. <span data-ttu-id="f0f23-163">Reinicie o Microsoft Edge e navegue até *edge://sync-internals* e verifique a seção “**Status da Chave de Conta do AAD**”</span><span class="sxs-lookup"><span data-stu-id="f0f23-163">Restart Microsoft Edge and navigate to *edge://sync-internals* and check the “**AAD Account Key Status**” section</span></span>
   - <span data-ttu-id="f0f23-164">"Êxito" em "Último Resultado do MIP": o erro de criptógrafo significa que os dados do servidor podem ser criptografados com uma chave perdida.</span><span class="sxs-lookup"><span data-stu-id="f0f23-164">"Success" in "Last MIP Result": the cryptographer error means server data might be encrypted with a lost key.</span></span> <span data-ttu-id="f0f23-165">É necessário a redefinição dos dados para retomar a sincronia.</span><span class="sxs-lookup"><span data-stu-id="f0f23-165">Data reset is needed to resume sync.</span></span>
   - <span data-ttu-id="f0f23-166">"Sem permissões" em "Último Resultado do MIP": possivelmente isso foi causado por uma alteração no Azure AD ou por alterações na assinatura do locatário.</span><span class="sxs-lookup"><span data-stu-id="f0f23-166">"No permissions" in "Last MIP Result": It is possibly caused by an Azure AD change or tenant subscription changes.</span></span> <span data-ttu-id="f0f23-167">É necessário a redefinição dos dados para retomar a sincronia.</span><span class="sxs-lookup"><span data-stu-id="f0f23-167">Data reset is needed to resume sync.</span></span>
   - <span data-ttu-id="f0f23-168">Outros erros podem significar problemas de configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="f0f23-168">Other errors may mean server configuration issues.</span></span>
2. <span data-ttu-id="f0f23-169">Se a redefinição de dados for necessária, confira [Redefinir dados do Microsoft Edge na nuvem](edge-learnmore-reset-data-in-cloud.md).</span><span class="sxs-lookup"><span data-stu-id="f0f23-169">If data reset is needed, see [Reset Microsoft Edge data in the cloud](edge-learnmore-reset-data-in-cloud.md).</span></span>

### <a name="issue-sync-has-been-turned-off-by-your-administrator"></a><span data-ttu-id="f0f23-170">Problema: "A sincronização foi desativada pelo administrador".</span><span class="sxs-lookup"><span data-stu-id="f0f23-170">Issue: “Sync has been turned off by your administrator.”</span></span>

<span data-ttu-id="f0f23-171">Verifique se a [política SyncDisabled ](https://docs.microsoft.com/deployedge/microsoft-edge-policies#syncdisabled) não está definida.</span><span class="sxs-lookup"><span data-stu-id="f0f23-171">Make sure that the [SyncDisabled policy](https://docs.microsoft.com/deployedge/microsoft-edge-policies#syncdisabled)  is not set.</span></span>

## <a name="see-also"></a><span data-ttu-id="f0f23-172">Veja também</span><span class="sxs-lookup"><span data-stu-id="f0f23-172">See also</span></span>

- [<span data-ttu-id="f0f23-173">Sincronização do Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="f0f23-173">Microsoft Edge Enterprise Sync</span></span>](microsoft-edge-enterprise-sync.md)
- [<span data-ttu-id="f0f23-174">Microsoft Edge e Enterprise State Roaming</span><span class="sxs-lookup"><span data-stu-id="f0f23-174">Microsoft Edge and Enterprise State Roaming</span></span>](microsoft-edge-enterprise-state-roaming.md)
- [<span data-ttu-id="f0f23-175">Página de aterrissagem do Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="f0f23-175">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
