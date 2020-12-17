---
title: Blocker Toolkit para desabilitar a entrega automática do Microsoft Edge
ms.author: kvice
author: dan-wesley
manager: srugh
ms.date: 12/16/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Blocker Toolkit para desabilitar a entrega automática do Microsoft Edge
ms.openlocfilehash: 9fb97d2dfec4822f8ce76dc3e37b85118c6572ad
ms.sourcegitcommit: 606282995b466a968bab40c16005a6653323c763
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/16/2020
ms.locfileid: "11229612"
---
# <span data-ttu-id="4e489-103">Blocker Toolkit para desabilitar a entrega automática do Microsoft Edge (baseado no Chromium)</span><span class="sxs-lookup"><span data-stu-id="4e489-103">Blocker Toolkit to disable automatic delivery of Microsoft Edge (Chromium-based)</span></span>

<span data-ttu-id="4e489-104">Este artigo descreve o Blocker Toolkit para desabilitar a entrega automática e a instalação do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="4e489-104">This article describes the Blocker Toolkit for disabling automatic delivery and installation of Microsoft Edge.</span></span>

<span data-ttu-id="4e489-105">As seguintes atualizações foram feitas neste artigo:</span><span class="sxs-lookup"><span data-stu-id="4e489-105">The following updates have been made to this article:</span></span>

- <span data-ttu-id="4e489-106">**01/09/2020** com mais informações sobre dispositivos que podem exigir o uso do kit de ferramentas do Bloqueador</span><span class="sxs-lookup"><span data-stu-id="4e489-106">**01/09/2020** with more information about devices that might require you to use the Blocker Toolkit</span></span>
- <span data-ttu-id="4e489-107">**28/02/2020** para remover "MDM gerenciado" dos critérios de dispositivos a serem excluídos desta atualização automática</span><span class="sxs-lookup"><span data-stu-id="4e489-107">**2/28/2020** to remove "MDM managed" from the criteria of devices to be excluded from this automatic update</span></span>
- <span data-ttu-id="4e489-108">**30/06/2020**para refletir que todos os dispositivos conectados do Windows Update estão no escopo para receber esta atualização (em vigor não antes de 30/07/2020)</span><span class="sxs-lookup"><span data-stu-id="4e489-108">**6/30/2020** to reflect that all Windows Update connected devices are in scope to receive this update (effective no sooner than 7/30/2020)</span></span>
- <span data-ttu-id="4e489-109">**10/12/2020** para explicar as situações pré-20H2 nas quais as configurações do Kit de ferramentas do Bloqueador serão ignoradas</span><span class="sxs-lookup"><span data-stu-id="4e489-109">**12/10/2020** to explain pre 20H2 situations in which the Blocker Toolkit settings will be ignored</span></span>

> [!NOTE]
> <span data-ttu-id="4e489-110">Isso se aplica ao canal estável do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="4e489-110">This applies to Microsoft Edge Stable channel.</span></span>

## <span data-ttu-id="4e489-111">Visão geral</span><span class="sxs-lookup"><span data-stu-id="4e489-111">Overview</span></span>

<span data-ttu-id="4e489-112">Para ajudar nossos clientes a se tornarem mais seguros e atualizados, a Microsoft distribuirá o Microsoft Edge (Chromium) para dispositivos conectados ao Windows Update executando Windows 10 versão 1803 e posterior.</span><span class="sxs-lookup"><span data-stu-id="4e489-112">To help our customers become more secure and up-to-date, Microsoft will distribute Microsoft Edge (Chromium-based) to all Windows Update-connected devices running Windows 10 version 1803 and newer.</span></span> <span data-ttu-id="4e489-113">Esse processo será iniciado após 15 de janeiro de 2020, e mais informações estarão disponíveis nessa data.</span><span class="sxs-lookup"><span data-stu-id="4e489-113">This process will start after January 15, 2020 and more information will be available on that date.</span></span>

<span data-ttu-id="4e489-114">O Blocker Toolkit destina-se a organizações que desejam bloquear a entrega automática do Microsoft Edge (baseado no Chromium) em dispositivos conectados ao Windows Update que executam o Windows 10 versão 1803 e posterior.</span><span class="sxs-lookup"><span data-stu-id="4e489-114">The Blocker Toolkit is intended for organizations that would like to block automatic delivery of Microsoft Edge (Chromium-based) to Windows Updated-connected devices running Windows 10 version 1803 and newer.</span></span> <span data-ttu-id="4e489-115">Os dispositivos gerenciados pelo Windows Server Update Services (WSUS) ou Windows Update para Empresas (WUfB) serão excluídos deste Windows Update automático, mas podem receber o novo Microsoft Edge (baseado no Chromium) por meio de sua organização.</span><span class="sxs-lookup"><span data-stu-id="4e489-115">Devices that are Windows Server Update Services (WSUS) or Windows Update for Business (WUfB) managed will be excluded from this automatic Windows Update, but may receive the new Microsoft Edge (Chromium-based) through their organization.</span></span>

**<span data-ttu-id="4e489-116">É importante observar que:</span><span class="sxs-lookup"><span data-stu-id="4e489-116">It's important to note that:</span></span>**

- <span data-ttu-id="4e489-117">O Blocker Toolkit não impede que os usuários instalem manualmente o Microsoft Edge (baseado no Chromium) do download pela Internet ou de mídias externas.</span><span class="sxs-lookup"><span data-stu-id="4e489-117">The Blocker Toolkit will not prevent users from manually installing Microsoft Edge (Chromium-based) from Internet download, or from external media.</span></span>
- <span data-ttu-id="4e489-118">As organizações com atualizações gerenciadas por meio do Windows Update para Empresas (WUfB) não receberão automaticamente essa atualização e não precisarão implantar o Blocker Toolkit.</span><span class="sxs-lookup"><span data-stu-id="4e489-118">Organizations with updates managed through Windows Update for Business (WUfB) will not automatically receive this update and do not need to deploy the blocker toolkit.</span></span>
- <span data-ttu-id="4e489-119">As organizações com ambientes gerenciados com uma solução de gerenciamento de atualizações, como o Windows Server Update Services (WSUS) ou o System Center Configuration Manager (SCCM, não precisam implantar o Blocker Toolkit.</span><span class="sxs-lookup"><span data-stu-id="4e489-119">Organizations with environments managed with an update management solution such as Windows Server Update Services (WSUS) or System Center Configuration Manager (SCCM) do not have to deploy the Blocker Toolkit.</span></span> <span data-ttu-id="4e489-120">Eles podem usar esses produtos para gerenciar totalmente a implantação de atualizações lançadas por meio do Windows Update e do Microsoft Update, incluindo a [Atualização no WSUS para o novo Microsoft Edge](https://support.microsoft.com/help/4584642/update-in-wsus-for-the-new-microsoft-edge), em seu ambiente.</span><span class="sxs-lookup"><span data-stu-id="4e489-120">They can use those products to fully manage deployment of updates released through Windows Update and Microsoft Update, including the [Update in WSUS for the new Microsoft Edge](https://support.microsoft.com/help/4584642/update-in-wsus-for-the-new-microsoft-edge), within their environment.</span></span>
- <span data-ttu-id="4e489-121">Esta atualização é uma atualização autônoma (não faz parte da atualização cumulativa mensal) para proporcionar flexibilidade aos clientes corporativos e controle máximo sobre a implantação dessa atualização.</span><span class="sxs-lookup"><span data-stu-id="4e489-121">This update is a stand-alone update (not part of the monthly cumulative update) to give Enterprise customers flexibility and maximum control over deploying this update.</span></span>
- <span data-ttu-id="4e489-122">O novo Microsoft Edge (baseado em Chromium) está incluído como parte da atualização de recursos do Windows 10, versão 20H2 no segundo semestre de 2020.</span><span class="sxs-lookup"><span data-stu-id="4e489-122">The new Microsoft Edge (Chromium-based) is included as part of the Windows 10, version 20H2 feature update in the second half of 2020.</span></span> <span data-ttu-id="4e489-123">O kit de ferramentas Bloqueador não afeta o comportamento ou a implantação da versão 20H2.</span><span class="sxs-lookup"><span data-stu-id="4e489-123">The Blocker toolkit does not impact 20H2 behaviors or deployment.</span></span> <span data-ttu-id="4e489-124">Confira mais informações sobre o Windows 10, versão 20H2 [aqui](https://blogs.windows.com/windowsexperience/2020/06/16/whats-next-for-windows-10-updates/).</span><span class="sxs-lookup"><span data-stu-id="4e489-124">See more information about Windows 10, version 20H2 [here](https://blogs.windows.com/windowsexperience/2020/06/16/whats-next-for-windows-10-updates/).</span></span>

<span data-ttu-id="4e489-125">Você pode baixar o arquivo executável do Blocker Toolkit em [https://msedgeblockertoolkit.blob.core.windows.net/blockertoolkit/MicrosoftEdgeChromiumBlockerToolkit.exe](https://msedgeblockertoolkit.blob.core.windows.net/blockertoolkit/MicrosoftEdgeChromiumBlockerToolkit.exe).</span><span class="sxs-lookup"><span data-stu-id="4e489-125">You can download the Blocker Toolkit executable file from [https://msedgeblockertoolkit.blob.core.windows.net/blockertoolkit/MicrosoftEdgeChromiumBlockerToolkit.exe](https://msedgeblockertoolkit.blob.core.windows.net/blockertoolkit/MicrosoftEdgeChromiumBlockerToolkit.exe).</span></span>

### <span data-ttu-id="4e489-126">Componentes do kit de ferramentas</span><span class="sxs-lookup"><span data-stu-id="4e489-126">Toolkit components</span></span>

<span data-ttu-id="4e489-127">Este kit de ferramentas contém os seguintes componentes:</span><span class="sxs-lookup"><span data-stu-id="4e489-127">This toolkit contains the following components:</span></span>

- <span data-ttu-id="4e489-128">Script do bloqueador de executáveis (.CMD)</span><span class="sxs-lookup"><span data-stu-id="4e489-128">Executable blocker script (.CMD)</span></span>
- <span data-ttu-id="4e489-129">Modelo Administrativo da Política de Grupo (.ADMX e .ADML)</span><span class="sxs-lookup"><span data-stu-id="4e489-129">Group Policy Administrative Template (.ADMX and .ADML)</span></span>

### <span data-ttu-id="4e489-130">Sistemas operacionais com suporte</span><span class="sxs-lookup"><span data-stu-id="4e489-130">Supported Operating Systems</span></span>

<span data-ttu-id="4e489-131">Windows 10 versão 1803 e mais recente.</span><span class="sxs-lookup"><span data-stu-id="4e489-131">Windows 10 version 1803 and newer.</span></span>

## <span data-ttu-id="4e489-132">Script do bloqueador</span><span class="sxs-lookup"><span data-stu-id="4e489-132">Blocker script</span></span>

<span data-ttu-id="4e489-133">O script cria uma chave do Registro e define o valor associado para bloquear ou desbloquear (dependendo da opção de linha de comando usada) a entrega automática do Microsoft Edge (baseado no Chromium) no computador local ou em um computador de destino remoto.</span><span class="sxs-lookup"><span data-stu-id="4e489-133">The script creates a registry key and sets the associated value to block or unblock (depending on the command-line option used) automatic delivery of Microsoft Edge (Chromium-based) on either the local machine or a remote target machine.</span></span>

**<span data-ttu-id="4e489-134">Chave do Registro:</span><span class="sxs-lookup"><span data-stu-id="4e489-134">Registry key:</span></span>** `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\EdgeUpdate`<br>
**<span data-ttu-id="4e489-135">Nome do valor da chave:</span><span class="sxs-lookup"><span data-stu-id="4e489-135">Key value name:</span></span>** `DoNotUpdateToEdgeWithChromium`

| <span data-ttu-id="4e489-136">Valor</span><span class="sxs-lookup"><span data-stu-id="4e489-136">Value</span></span>                | <span data-ttu-id="4e489-137">Resultado</span><span class="sxs-lookup"><span data-stu-id="4e489-137">Result</span></span>                         |
|----------------------|--------------------------------|
| *<span data-ttu-id="4e489-138">A chave não está definida</span><span class="sxs-lookup"><span data-stu-id="4e489-138">Key is not defined</span></span>* | <span data-ttu-id="4e489-139">A distribuição *não* está bloqueada.</span><span class="sxs-lookup"><span data-stu-id="4e489-139">Distribution is *not* blocked.</span></span> |
| <span data-ttu-id="4e489-140">0</span><span class="sxs-lookup"><span data-stu-id="4e489-140">0</span></span>                    | <span data-ttu-id="4e489-141">A distribuição *não* está bloqueada.</span><span class="sxs-lookup"><span data-stu-id="4e489-141">Distribution is *not* blocked.</span></span> |
| <span data-ttu-id="4e489-142">1</span><span class="sxs-lookup"><span data-stu-id="4e489-142">1</span></span>                    | <span data-ttu-id="4e489-143">A distribuição está bloqueada.</span><span class="sxs-lookup"><span data-stu-id="4e489-143">Distribution is blocked.</span></span>       |

<span data-ttu-id="4e489-144">O script tem a seguinte sintaxe de linha de comando:</span><span class="sxs-lookup"><span data-stu-id="4e489-144">The script has the following command-line syntax:</span></span><br>
`EdgeChromium_Blocker.cmd [<machine name>] [/B] [/U] [/H]`

### <span data-ttu-id="4e489-145">Nome do computador</span><span class="sxs-lookup"><span data-stu-id="4e489-145">Machine name</span></span>

<span data-ttu-id="4e489-146">O parâmetro `<machine name>` é opcional.</span><span class="sxs-lookup"><span data-stu-id="4e489-146">The `<machine name>` parameter is optional.</span></span> <span data-ttu-id="4e489-147">Se não for especificado, a ação será executada no computador local.</span><span class="sxs-lookup"><span data-stu-id="4e489-147">If not specified, the action is performed on the local machine.</span></span> <span data-ttu-id="4e489-148">Caso contrário, o computador remoto é acessado por meio das funcionalidades de registro remoto do comando `REG`.</span><span class="sxs-lookup"><span data-stu-id="4e489-148">Otherwise, the remote machine is accessed through the remote registry capabilities of the `REG` command.</span></span> <span data-ttu-id="4e489-149">Se o registro remoto não puder ser acessado devido a permissões de segurança ou o computador local não for encontrado, uma mensagem de erro será retornada do comando `REG`.</span><span class="sxs-lookup"><span data-stu-id="4e489-149">If the remote registry can't be accessed due to security permissions or the remote machine can't be found, an error message is returned from the `REG` command.</span></span>

### <span data-ttu-id="4e489-150">Opções</span><span class="sxs-lookup"><span data-stu-id="4e489-150">Switches</span></span>

<span data-ttu-id="4e489-151">As opções usadas pelo script são mutuamente exclusivas e somente a primeira opção válida de um determinado comando é acionada.</span><span class="sxs-lookup"><span data-stu-id="4e489-151">Switches used by the script are mutually exclusive and only the first valid switch from a given command is acted on.</span></span> <span data-ttu-id="4e489-152">O script pode ser executado várias vezes no mesmo computador.</span><span class="sxs-lookup"><span data-stu-id="4e489-152">The script can be run multiple times on the same machine.</span></span>

| <span data-ttu-id="4e489-153">Opção</span><span class="sxs-lookup"><span data-stu-id="4e489-153">Switch</span></span>       | <span data-ttu-id="4e489-154">Descrição</span><span class="sxs-lookup"><span data-stu-id="4e489-154">Description</span></span>                              |
|--------------|------------------------------------------|
| `/B`         | <span data-ttu-id="4e489-155">Bloqueia a distribuição</span><span class="sxs-lookup"><span data-stu-id="4e489-155">Blocks distribution</span></span>                      |
| `/U`         | <span data-ttu-id="4e489-156">Desbloqueia a distribuição</span><span class="sxs-lookup"><span data-stu-id="4e489-156">Unblocks distribution</span></span>                    |
| `/H` <span data-ttu-id="4e489-157">ou</span><span class="sxs-lookup"><span data-stu-id="4e489-157">or</span></span> `/?` | <span data-ttu-id="4e489-158">Exibe a seguinte ajuda resumida:</span><span class="sxs-lookup"><span data-stu-id="4e489-158">Displays the following summary help:</span></span><br>`This tool can be used to remotely block or unblock the delivery of Microsoft Edge (Chromium-based) through Automatic Updates.`<br> `Usage:`<br>`EdgeChromium_Blocker.cmd [<machine name>] [/B][/U][/H]`<br>`B = Block Microsoft Edge (Chromium-based) deployment`<br>`U = Allow Microsoft Edge (Chromium-based) deployment`<br>`H = Help`<br>`Examples:`<br>`EdgeChromium_Blocker.cmd mymachine /B (blocks delivery on machine "mymachine")`<br>`EdgeChromium_Blocker.cmd /U (unblocks delivery on the local machine)`<br> |

## <span data-ttu-id="4e489-159">Modelo Administrativo da Política de Grupo (arquivos .ADMX e .ADML)</span><span class="sxs-lookup"><span data-stu-id="4e489-159">Group Policy Administrative Template (.ADMX and .ADML files)</span></span>

<span data-ttu-id="4e489-160">O Modelo Administrativo da Política de Grupo (arquivos .ADMX e .ADML) permite que os administradores importem as novas configurações de Política de Grupo para bloquear ou desbloquear a entrega automática do Microsoft Edge (baseado no Chromium) em seu ambiente de Política de Grupo e usar a Política de Grupo para executar a ação centralmente entre os sistemas em seu ambiente.</span><span class="sxs-lookup"><span data-stu-id="4e489-160">The Group Policy Administrative Template (.ADMX  and .ADML files) allows administrators to import the new Group Policy settings to block or unblock automatic delivery of Microsoft Edge (Chromium-based) into their Group Policy environment, and use Group Policy to centrally execute the action across systems in their environment.</span></span>

<span data-ttu-id="4e489-161">Os usuários que executam o Windows 10 RS3 Enterprise/EDU e RS4 e versões mais recentes verão a política no seguinte caminho:</span><span class="sxs-lookup"><span data-stu-id="4e489-161">Users running Windows 10 RS3 Enterprise/EDU and RS4 and newer, will see the policy under the following path:</span></span>

```
/Computer Configuration  
  /Administrative Templates
    /Classic Administrative Templates
      /Windows Components
        /Windows Update  
          /Microsoft Edge (Chromium-based) Blockers  
```

<span data-ttu-id="4e489-162">Essa configuração está disponível somente como uma configuração de computador. Não há configuração do usuário.</span><span class="sxs-lookup"><span data-stu-id="4e489-162">This setting is available only as a Computer setting; there is no Per-User setting.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4e489-163">Essa configuração do Registro não é armazenada em uma chave de políticas e é considerada uma *preferência*.</span><span class="sxs-lookup"><span data-stu-id="4e489-163">This registry setting isn't stored in a policies key and is considered a *preference*.</span></span> <span data-ttu-id="4e489-164">Portanto, se o Objeto de Política de Grupo que implementa a configuração for removido ou a política for definida como **Não Configurada**, a configuração permanecerá.</span><span class="sxs-lookup"><span data-stu-id="4e489-164">Therefore, if the Group Policy Object that implements the setting is ever removed or the policy is set to **Not Configured**, the setting will remain.</span></span> <span data-ttu-id="4e489-165">Para desbloquear a distribuição do Microsoft Edge (baseado no Chromium) usando a Política de Grupo, defina a política como **Desabilitada**.</span><span class="sxs-lookup"><span data-stu-id="4e489-165">To unblock distribution of Microsoft Edge (Chromium-based) by using Group Policy, set the policy to **Disabled**.</span></span>

## <span data-ttu-id="4e489-166">Consulte também</span><span class="sxs-lookup"><span data-stu-id="4e489-166">See also</span></span>

- [<span data-ttu-id="4e489-167">Página de aterrissagem do Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="4e489-167">Microsoft Edge Enterprise landing page</span></span>](https://www.microsoftedgeinsider.com/enterprise)
- [<span data-ttu-id="4e489-168">Atualizações do Windows para dar suporte ao Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="4e489-168">Windows updates to support Microsoft Edge</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-sysupdate-windows-updates)
- [<span data-ttu-id="4e489-169">Como acessar a versão antiga do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="4e489-169">How to access the old version of Microsoft Edge</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-sysupdate-access-old-edge)
