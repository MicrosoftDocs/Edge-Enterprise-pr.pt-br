---
title: Blocker Toolkit para desabilitar a entrega automática do Microsoft Edge
ms.author: kvice
author: dan-wesley
manager: srugh
ms.date: 06/30/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Blocker Toolkit para desabilitar a entrega automática do Microsoft Edge
ms.openlocfilehash: 7563d2c94cf91a8434328699e46c75dbcfb77561
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979135"
---
# <span data-ttu-id="290d4-103">Blocker Toolkit para desabilitar a entrega automática do Microsoft Edge (baseado no Chromium)</span><span class="sxs-lookup"><span data-stu-id="290d4-103">Blocker Toolkit to disable automatic delivery of Microsoft Edge (Chromium-based)</span></span>

<span data-ttu-id="290d4-104">Este artigo descreve o Blocker Toolkit para desabilitar a entrega automática e a instalação do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="290d4-104">This article describes the Blocker Toolkit for disabling automatic delivery and installation of Microsoft Edge.</span></span> <span data-ttu-id="290d4-105">Este artigo foi atualizado em **09/01/2020** com mais informações sobre dispositivos que podem exigir que você use o Blocker Toolkit, em **28/02/2020** para remover "gerenciado por MDM" dos critérios de exclusão de dispositivos da atualização automática e, em **30/06/2020** para indicar que todos os dispositivos conectados ao Windows Update estão no escopo para receber essa atualização (com efeito não antes de 30/07/2020).</span><span class="sxs-lookup"><span data-stu-id="290d4-105">This article was updated on **01/09/2020** with more information about devices that might require you to use the Blocker Toolkit, on **2/28/2020** to remove "MDM managed" from the criteria of devices to be excluded from this automatic update, and on **6/30/2020** to reflect that all Windows Update connected devices are in scope to receive this update (effective no sooner than 7/30/2020).</span></span>

> [!NOTE]
> <span data-ttu-id="290d4-106">Isso se aplica ao canal estável do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="290d4-106">This applies to Microsoft Edge Stable channel.</span></span>

## <span data-ttu-id="290d4-107">Visão geral</span><span class="sxs-lookup"><span data-stu-id="290d4-107">Overview</span></span>

<span data-ttu-id="290d4-108">Para ajudar nossos clientes a se tornarem mais seguros e atualizados, a Microsoft distribuirá o Microsoft Edge (Chromium) para dispositivos conectados ao Windows Update executando Windows 10 versão 1803 e posterior.</span><span class="sxs-lookup"><span data-stu-id="290d4-108">To help our customers become more secure and up-to-date, Microsoft will distribute Microsoft Edge (Chromium-based) to all Windows Update-connected devices running Windows 10 version 1803 and newer.</span></span> <span data-ttu-id="290d4-109">Esse processo será iniciado após 15 de janeiro de 2020, e mais informações estarão disponíveis nessa data.</span><span class="sxs-lookup"><span data-stu-id="290d4-109">This process will start after January 15, 2020 and more information will be available on that date.</span></span>

<span data-ttu-id="290d4-110">O Blocker Toolkit destina-se a organizações que desejam bloquear a entrega automática do Microsoft Edge (baseado no Chromium) em dispositivos conectados ao Windows Update que executam o Windows 10 versão 1803 e posterior.</span><span class="sxs-lookup"><span data-stu-id="290d4-110">The Blocker Toolkit is intended for organizations that would like to block automatic delivery of Microsoft Edge (Chromium-based) to Windows Updated-connected devices running Windows 10 version 1803 and newer.</span></span>
<span data-ttu-id="290d4-111">Os dispositivos que são gerenciados pelo Windows Server Update Services (WSUS) ou Windows Update para Empresas (WUfB) serão excluídos desta atualização automática.</span><span class="sxs-lookup"><span data-stu-id="290d4-111">Devices that are Windows Server Update Services (WSUS) or Windows Update for Business (WUfB) managed will be excluded from this automatic update.</span></span>

**<span data-ttu-id="290d4-112">É importante observar que:</span><span class="sxs-lookup"><span data-stu-id="290d4-112">It's important to note that:</span></span>**

- <span data-ttu-id="290d4-113">O Blocker Toolkit não impede que os usuários instalem manualmente o Microsoft Edge (baseado no Chromium) do download pela Internet ou de mídias externas.</span><span class="sxs-lookup"><span data-stu-id="290d4-113">The Blocker Toolkit will not prevent users from manually installing Microsoft Edge (Chromium-based) from Internet download, or from external media.</span></span>
- <span data-ttu-id="290d4-114">As organizações com atualizações gerenciadas por meio do Windows Update para Empresas (WUfB) não receberão automaticamente essa atualização e não precisarão implantar o Blocker Toolkit.</span><span class="sxs-lookup"><span data-stu-id="290d4-114">Organizations with updates managed through Windows Update for Business (WUfB) will not automatically receive this update and do not need to deploy the blocker toolkit.</span></span>
- <span data-ttu-id="290d4-115">As organizações com ambientes gerenciados com uma solução de gerenciamento de atualizações, como o Windows Server Update Services (WSUS) ou o System Center Configuration Manager (SCCM, não precisam implantar o Blocker Toolkit.</span><span class="sxs-lookup"><span data-stu-id="290d4-115">Organizations with environments managed with an update management solution such as Windows Server Update Services (WSUS) or System Center Configuration Manager (SCCM) do not have to deploy the Blocker Toolkit.</span></span> <span data-ttu-id="290d4-116">Elas podem usar esses produtos para gerenciar totalmente a implantação de atualizações lançadas por meio do Windows Update e do Microsoft Update, incluindo o Microsoft Edge (baseado no Chromium), nos ambientes.</span><span class="sxs-lookup"><span data-stu-id="290d4-116">They can use those products to fully manage deployment of updates released through Windows Update and Microsoft Update, including Microsoft Edge (Chromium-based), within their environment.</span></span>
- <span data-ttu-id="290d4-117">Esta atualização é uma atualização autônoma (não faz parte da atualização cumulativa mensal) para proporcionar flexibilidade aos clientes corporativos e controle máximo sobre a implantação dessa atualização.</span><span class="sxs-lookup"><span data-stu-id="290d4-117">This update is a stand-alone update (not part of the monthly cumulative update) to give Enterprise customers flexibility and maximum control over deploying this update.</span></span>
- <span data-ttu-id="290d4-118">O novo Microsoft Edge (Chromium) será incluído como parte da atualização de recursos do Windows 10, versão 20H2 no segundo semestre de 2020.</span><span class="sxs-lookup"><span data-stu-id="290d4-118">The new Microsoft Edge (Chromium-based) will be included as part of the Windows 10, version 20H2 feature update in the second half of 2020.</span></span> <span data-ttu-id="290d4-119">O Blocker Toolkit não afeta o comportamento ou a implantação da versão 20H2.</span><span class="sxs-lookup"><span data-stu-id="290d4-119">The Blocker toolkit does not impact 20H2 behaviors or deployment.</span></span> <span data-ttu-id="290d4-120">Confira mais informações sobre o Windows 10, versão 20H2 [aqui](https://blogs.windows.com/windowsexperience/2020/06/16/whats-next-for-windows-10-updates/).</span><span class="sxs-lookup"><span data-stu-id="290d4-120">See more information about Windows 10, version 20H2 [here](https://blogs.windows.com/windowsexperience/2020/06/16/whats-next-for-windows-10-updates/).</span></span>

<span data-ttu-id="290d4-121">Você pode baixar o arquivo executável do Blocker Toolkit em [https://msedgeblockertoolkit.blob.core.windows.net/blockertoolkit/MicrosoftEdgeChromiumBlockerToolkit.exe](https://msedgeblockertoolkit.blob.core.windows.net/blockertoolkit/MicrosoftEdgeChromiumBlockerToolkit.exe).</span><span class="sxs-lookup"><span data-stu-id="290d4-121">You can download the Blocker Toolkit executable file from [https://msedgeblockertoolkit.blob.core.windows.net/blockertoolkit/MicrosoftEdgeChromiumBlockerToolkit.exe](https://msedgeblockertoolkit.blob.core.windows.net/blockertoolkit/MicrosoftEdgeChromiumBlockerToolkit.exe).</span></span>

### <span data-ttu-id="290d4-122">Componentes do kit de ferramentas</span><span class="sxs-lookup"><span data-stu-id="290d4-122">Toolkit components</span></span>

<span data-ttu-id="290d4-123">Este kit de ferramentas contém os seguintes componentes:</span><span class="sxs-lookup"><span data-stu-id="290d4-123">This toolkit contains the following components:</span></span>

- <span data-ttu-id="290d4-124">Script do bloqueador de executáveis (.CMD)</span><span class="sxs-lookup"><span data-stu-id="290d4-124">Executable blocker script (.CMD)</span></span>
- <span data-ttu-id="290d4-125">Modelo Administrativo da Política de Grupo (.ADMX e .ADML)</span><span class="sxs-lookup"><span data-stu-id="290d4-125">Group Policy Administrative Template (.ADMX and .ADML)</span></span>

### <span data-ttu-id="290d4-126">Sistemas operacionais com suporte</span><span class="sxs-lookup"><span data-stu-id="290d4-126">Supported Operating Systems</span></span>

<span data-ttu-id="290d4-127">Windows 10 versão 1803 e mais recente.</span><span class="sxs-lookup"><span data-stu-id="290d4-127">Windows 10 version 1803 and newer.</span></span>

## <span data-ttu-id="290d4-128">Script do bloqueador</span><span class="sxs-lookup"><span data-stu-id="290d4-128">Blocker script</span></span>

<span data-ttu-id="290d4-129">O script cria uma chave do Registro e define o valor associado para bloquear ou desbloquear (dependendo da opção de linha de comando usada) a entrega automática do Microsoft Edge (baseado no Chromium) no computador local ou em um computador de destino remoto.</span><span class="sxs-lookup"><span data-stu-id="290d4-129">The script creates a registry key and sets the associated value to block or unblock (depending on the command-line option used) automatic delivery of Microsoft Edge (Chromium-based) on either the local machine or a remote target machine.</span></span>

**<span data-ttu-id="290d4-130">Chave do Registro:</span><span class="sxs-lookup"><span data-stu-id="290d4-130">Registry key:</span></span>** `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\EdgeUpdate`<br>
**<span data-ttu-id="290d4-131">Nome do valor da chave:</span><span class="sxs-lookup"><span data-stu-id="290d4-131">Key value name:</span></span>** `DoNotUpdateToEdgeWithChromium`

| <span data-ttu-id="290d4-132">Valor</span><span class="sxs-lookup"><span data-stu-id="290d4-132">Value</span></span>                | <span data-ttu-id="290d4-133">Resultado</span><span class="sxs-lookup"><span data-stu-id="290d4-133">Result</span></span>                         |
|----------------------|--------------------------------|
| *<span data-ttu-id="290d4-134">A chave não está definida</span><span class="sxs-lookup"><span data-stu-id="290d4-134">Key is not defined</span></span>* | <span data-ttu-id="290d4-135">A distribuição *não* está bloqueada.</span><span class="sxs-lookup"><span data-stu-id="290d4-135">Distribution is *not* blocked.</span></span> |
| <span data-ttu-id="290d4-136">0</span><span class="sxs-lookup"><span data-stu-id="290d4-136">0</span></span>                    | <span data-ttu-id="290d4-137">A distribuição *não* está bloqueada.</span><span class="sxs-lookup"><span data-stu-id="290d4-137">Distribution is *not* blocked.</span></span> |
| <span data-ttu-id="290d4-138">1</span><span class="sxs-lookup"><span data-stu-id="290d4-138">1</span></span>                    | <span data-ttu-id="290d4-139">A distribuição está bloqueada.</span><span class="sxs-lookup"><span data-stu-id="290d4-139">Distribution is blocked.</span></span>       |

<span data-ttu-id="290d4-140">O script tem a seguinte sintaxe de linha de comando:</span><span class="sxs-lookup"><span data-stu-id="290d4-140">The script has the following command-line syntax:</span></span><br>
`EdgeChromium_Blocker.cmd [<machine name>] [/B] [/U] [/H]`

### <span data-ttu-id="290d4-141">Nome do computador</span><span class="sxs-lookup"><span data-stu-id="290d4-141">Machine name</span></span>

<span data-ttu-id="290d4-142">O parâmetro `<machine name>` é opcional.</span><span class="sxs-lookup"><span data-stu-id="290d4-142">The `<machine name>` parameter is optional.</span></span> <span data-ttu-id="290d4-143">Se não for especificado, a ação será executada no computador local.</span><span class="sxs-lookup"><span data-stu-id="290d4-143">If not specified, the action is performed on the local machine.</span></span> <span data-ttu-id="290d4-144">Caso contrário, o computador remoto é acessado por meio das funcionalidades de registro remoto do comando `REG`.</span><span class="sxs-lookup"><span data-stu-id="290d4-144">Otherwise, the remote machine is accessed through the remote registry capabilities of the `REG` command.</span></span> <span data-ttu-id="290d4-145">Se o registro remoto não puder ser acessado devido a permissões de segurança ou o computador local não for encontrado, uma mensagem de erro será retornada do comando `REG`.</span><span class="sxs-lookup"><span data-stu-id="290d4-145">If the remote registry can't be accessed due to security permissions or the remote machine can't be found, an error message is returned from the `REG` command.</span></span>

### <span data-ttu-id="290d4-146">Opções</span><span class="sxs-lookup"><span data-stu-id="290d4-146">Switches</span></span>

<span data-ttu-id="290d4-147">As opções usadas pelo script são mutuamente exclusivas e somente a primeira opção válida de um determinado comando é acionada.</span><span class="sxs-lookup"><span data-stu-id="290d4-147">Switches used by the script are mutually exclusive and only the first valid switch from a given command is acted on.</span></span> <span data-ttu-id="290d4-148">O script pode ser executado várias vezes no mesmo computador.</span><span class="sxs-lookup"><span data-stu-id="290d4-148">The script can be run multiple times on the same machine.</span></span>

| <span data-ttu-id="290d4-149">Opção</span><span class="sxs-lookup"><span data-stu-id="290d4-149">Switch</span></span>       | <span data-ttu-id="290d4-150">Descrição</span><span class="sxs-lookup"><span data-stu-id="290d4-150">Description</span></span>                              |
|--------------|------------------------------------------|
| `/B`         | <span data-ttu-id="290d4-151">Bloqueia a distribuição</span><span class="sxs-lookup"><span data-stu-id="290d4-151">Blocks distribution</span></span>                      |
| `/U`         | <span data-ttu-id="290d4-152">Desbloqueia a distribuição</span><span class="sxs-lookup"><span data-stu-id="290d4-152">Unblocks distribution</span></span>                    |
| `/H` <span data-ttu-id="290d4-153">ou</span><span class="sxs-lookup"><span data-stu-id="290d4-153">or</span></span> `/?` | <span data-ttu-id="290d4-154">Exibe a seguinte ajuda resumida:</span><span class="sxs-lookup"><span data-stu-id="290d4-154">Displays the following summary help:</span></span><br>`This tool can be used to remotely block or unblock the delivery of Microsoft Edge (Chromium-based) through Automatic Updates.`<br> `Usage:`<br>`EdgeChromium_Blocker.cmd [<machine name>] [/B][/U][/H]`<br>`B = Block Microsoft Edge (Chromium-based) deployment`<br>`U = Allow Microsoft Edge (Chromium-based) deployment`<br>`H = Help`<br>`Examples:`<br>`EdgeChromium_Blocker.cmd mymachine /B (blocks delivery on machine "mymachine")`<br>`EdgeChromium_Blocker.cmd /U (unblocks delivery on the local machine)`<br> |

## <span data-ttu-id="290d4-155">Modelo Administrativo da Política de Grupo (arquivos .ADMX e .ADML)</span><span class="sxs-lookup"><span data-stu-id="290d4-155">Group Policy Administrative Template (.ADMX and .ADML files)</span></span>

<span data-ttu-id="290d4-156">O Modelo Administrativo da Política de Grupo (arquivos .ADMX e .ADML) permite que os administradores importem as novas configurações de Política de Grupo para bloquear ou desbloquear a entrega automática do Microsoft Edge (baseado no Chromium) em seu ambiente de Política de Grupo e usar a Política de Grupo para executar a ação centralmente entre os sistemas em seu ambiente.</span><span class="sxs-lookup"><span data-stu-id="290d4-156">The Group Policy Administrative Template (.ADMX  and .ADML files) allows administrators to import the new Group Policy settings to block or unblock automatic delivery of Microsoft Edge (Chromium-based) into their Group Policy environment, and use Group Policy to centrally execute the action across systems in their environment.</span></span>

<span data-ttu-id="290d4-157">Os usuários que executam o Windows 10 RS3 Enterprise/EDU e RS4 e versões mais recentes verão a política no seguinte caminho:</span><span class="sxs-lookup"><span data-stu-id="290d4-157">Users running Windows 10 RS3 Enterprise/EDU and RS4 and newer, will see the policy under the following path:</span></span>

```
/Computer Configuration  
  /Administrative Templates
    /Classic Administrative Templates
      /Windows Components
        /Windows Update  
          /Microsoft Edge (Chromium-based) Blockers  
```

<span data-ttu-id="290d4-158">Essa configuração está disponível somente como uma configuração de computador. Não há configuração do usuário.</span><span class="sxs-lookup"><span data-stu-id="290d4-158">This setting is available only as a Computer setting; there is no Per-User setting.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="290d4-159">Essa configuração do Registro não é armazenada em uma chave de políticas e é considerada uma *preferência*.</span><span class="sxs-lookup"><span data-stu-id="290d4-159">This registry setting isn't stored in a policies key and is considered a *preference*.</span></span> <span data-ttu-id="290d4-160">Portanto, se o Objeto de Política de Grupo que implementa a configuração for removido ou a política for definida como **Não Configurada**, a configuração permanecerá.</span><span class="sxs-lookup"><span data-stu-id="290d4-160">Therefore, if the Group Policy Object that implements the setting is ever removed or the policy is set to **Not Configured**, the setting will remain.</span></span> <span data-ttu-id="290d4-161">Para desbloquear a distribuição do Microsoft Edge (baseado no Chromium) usando a Política de Grupo, defina a política como **Desabilitada**.</span><span class="sxs-lookup"><span data-stu-id="290d4-161">To unblock distribution of Microsoft Edge (Chromium-based) by using Group Policy, set the policy to **Disabled**.</span></span>

## <span data-ttu-id="290d4-162">Consulte também</span><span class="sxs-lookup"><span data-stu-id="290d4-162">See also</span></span>

- [<span data-ttu-id="290d4-163">Página de aterrissagem do Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="290d4-163">Microsoft Edge Enterprise landing page</span></span>](https://www.microsoftedgeinsider.com/enterprise)
- [<span data-ttu-id="290d4-164">Atualizações do Windows para dar suporte ao Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="290d4-164">Windows updates to support Microsoft Edge</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-sysupdate-windows-updates)
- [<span data-ttu-id="290d4-165">Como acessar a versão antiga do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="290d4-165">How to access the old version of Microsoft Edge</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-sysupdate-access-old-edge)
