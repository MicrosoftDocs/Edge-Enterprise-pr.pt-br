---
title: Reversão do Microsoft Edge para empresas
ms.author: v-danwes
author: dan-wesley
manager: srugh
ms.date: 09/02/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Como reverter o Microsoft Edge para uma versão anterior
ms.openlocfilehash: 9f659b0bcdd82f54a814c8ad4157521061cdfa7c
ms.sourcegitcommit: 827a47d641c7ddc1d89be5d5fc0615373dec18b0
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993701"
---
# <span data-ttu-id="773ed-103">Como reverter o Microsoft Edge para uma versão anterior</span><span class="sxs-lookup"><span data-stu-id="773ed-103">How to roll back Microsoft Edge to a previous version</span></span>

<span data-ttu-id="773ed-104">Este artigo descreve como reverter para uma versão anterior do Microsoft Edge usando o recurso de reversão.</span><span class="sxs-lookup"><span data-stu-id="773ed-104">This article describes how to roll back to a previous version of Microsoft Edge using the rollback feature.</span></span>

>[!NOTE]
><span data-ttu-id="773ed-105">Este artigo se aplica ao Microsoft Edge versão 86 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="773ed-105">This article applies to Microsoft Edge version 86 or later.</span></span>

## <span data-ttu-id="773ed-106">Introdução à reversão</span><span class="sxs-lookup"><span data-stu-id="773ed-106">Introduction to rollback</span></span>

<span data-ttu-id="773ed-107">A reversão permite que você substitua a versão do navegador Microsoft Edge por uma versão anterior.</span><span class="sxs-lookup"><span data-stu-id="773ed-107">Rollback lets you replace your Microsoft Edge browser version with an earlier version.</span></span> <span data-ttu-id="773ed-108">Esse recurso foi projetado para ser uma rede de segurança para empresas que implantam o Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="773ed-108">This feature is designed to be a safety net for enterprises deploying Microsoft Edge.</span></span> <span data-ttu-id="773ed-109">Ele oferece uma maneira de solucionar problemas com o Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="773ed-109">It provides a way to troubleshoot issues with Microsoft Edge.</span></span> <span data-ttu-id="773ed-110">Os benefícios da reversão são a possibilidade de reverter para a versão anterior do navegador de forma fácil e rápida.</span><span class="sxs-lookup"><span data-stu-id="773ed-110">The benefits of rollback are the ability to revert to previous browser version easily and quickly.</span></span> <span data-ttu-id="773ed-111">A reversão reduz o impacto potencial causado por um problema com o Microsoft Edge nas operações de negócios.</span><span class="sxs-lookup"><span data-stu-id="773ed-111">Rollback reduces the potential impact that a Microsoft Edge issue has on business operations.</span></span>

## <span data-ttu-id="773ed-112">Antes de começar</span><span class="sxs-lookup"><span data-stu-id="773ed-112">Before you begin</span></span>

<span data-ttu-id="773ed-113">É importante compreender como o recurso de reversão está instalado em um ambiente do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="773ed-113">It's important to understand how the rollback feature is installed in a Microsoft Edge environment.</span></span> <span data-ttu-id="773ed-114">Você pode implantar a reversão ao usar dois métodos diferentes: manualmente com, um MSI ou ao usar a atualização do Microsoft Edge e a Política de grupo.</span><span class="sxs-lookup"><span data-stu-id="773ed-114">You can deploy rollback using two different methods: manually with an MSI or by using Microsoft Edge update and Group Policy.</span></span> <span data-ttu-id="773ed-115">Também incentivamos o uso de uma seleção das Políticas de grupo para se ter uma implantação mais suave.</span><span class="sxs-lookup"><span data-stu-id="773ed-115">We also  encourage using a selection of Group Policies for a smoother deployment.</span></span>

### <span data-ttu-id="773ed-116">Recomendações</span><span class="sxs-lookup"><span data-stu-id="773ed-116">Recommendations</span></span>

<span data-ttu-id="773ed-117">O recurso de reversão é destinado a ser uma correção temporária dos problemas que você possa encontrar em uma atualização do navegador Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="773ed-117">The rollback feature is meant to be a temporary fix for issues you might find in a Microsoft Edge browser update.</span></span> <span data-ttu-id="773ed-118">Recomendamos que os usuários instalem a versão mais recente do navegador Microsoft Edge para usar a proteção oferecida pelas atualizações de segurança mais recentes.</span><span class="sxs-lookup"><span data-stu-id="773ed-118">We recommend that users install the latest version of the Microsoft Edge browser to use the protection provided by the latest security updates.</span></span> <span data-ttu-id="773ed-119">Reverter para uma versão anterior corre o perigo de se expor aos problemas de segurança conhecidos.</span><span class="sxs-lookup"><span data-stu-id="773ed-119">Rollback to an earlier version risks exposure to known security issues.</span></span>

<span data-ttu-id="773ed-120">Antes de reverter temporariamente a versão do seu navegador, também recomendamos que você habilite a Sincronização para todos os usuários da sua organização.</span><span class="sxs-lookup"><span data-stu-id="773ed-120">Before temporarily rolling back your browser version, we also highly recommend that you enable Sync for all the users in your organization.</span></span> <span data-ttu-id="773ed-121">Se você não ativar a Sincronização, há um risco de perda permanente dos dados de navegação.</span><span class="sxs-lookup"><span data-stu-id="773ed-121">If you don't turn on Sync, there's a risk of permanent browsing data loss.</span></span> <span data-ttu-id="773ed-122">Para obter mais informações sobre a Sincronização, consulte [Sincronização do Microsoft Edge](microsoft-edge-enterprise-sync.md).</span><span class="sxs-lookup"><span data-stu-id="773ed-122">For more information about Sync, see [Microsoft Edge Sync](microsoft-edge-enterprise-sync.md).</span></span>

> [!CAUTION]
> <span data-ttu-id="773ed-123">Use apenas a reversão quando for necessário, pois sempre há o risco de perda de dados.</span><span class="sxs-lookup"><span data-stu-id="773ed-123">Only use rollback when necessary, there's always the risk of data loss.</span></span>

## <span data-ttu-id="773ed-124">Habilitar a reversão manualmente com um MSI</span><span class="sxs-lookup"><span data-stu-id="773ed-124">Enable rollback manually with an MSI</span></span>

<span data-ttu-id="773ed-125">Usar as etapas a seguir para fazer a reversão manualmente usando um MSI.</span><span class="sxs-lookup"><span data-stu-id="773ed-125">Use the following steps to roll back manually with an MSI.</span></span>

1. <span data-ttu-id="773ed-126">Desabilitar as atualizações do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="773ed-126">Disable Microsoft Edge Updates.</span></span>

   > [!NOTE]
   > <span data-ttu-id="773ed-127">Recomendamos que você instale os Modelos administrativos mais recentes.</span><span class="sxs-lookup"><span data-stu-id="773ed-127">We recommend that you install the most current Administrative templates.</span></span> <span data-ttu-id="773ed-128">Para obter mais informações, consulte [Download e instalação do modelo administrativo do Microsoft Edge](https://docs.microsoft.com/DeployEdge/configure-microsoft-edge#1-download-and-install-the-microsoft-edge-administrative-template).</span><span class="sxs-lookup"><span data-stu-id="773ed-128">For more information, see [Download and install the Microsoft Edge administrative template](https://docs.microsoft.com/DeployEdge/configure-microsoft-edge#1-download-and-install-the-microsoft-edge-administrative-template).</span></span>

   - <span data-ttu-id="773ed-129">Abra o Editor de política de grupo local e acesse *Configuração do computador>Atualização do Microsoft Edge>Aplicativos>Microsoft Edge>*.</span><span class="sxs-lookup"><span data-stu-id="773ed-129">Open the local Group Policy Editor and go to *Computer Configuration>Administrative Templates>Microsoft Edge Update>Applications>Microsoft Edge>*.</span></span>
   - <span data-ttu-id="773ed-130">Selecione **Atualizar a substituição da política** e depois selecione **Ativado**.</span><span class="sxs-lookup"><span data-stu-id="773ed-130">Select **Update policy override** and then select **Enabled**.</span></span>
   - <span data-ttu-id="773ed-131">Em **Opções**, clique em **Atualização desabilitada** na Lista suspensa de políticas.</span><span class="sxs-lookup"><span data-stu-id="773ed-131">Under **Options**, pick **Update disabled** from the Policy dropdown list.</span></span>

2. <span data-ttu-id="773ed-132">Obtenha o MSI.</span><span class="sxs-lookup"><span data-stu-id="773ed-132">Get the MSI.</span></span>

   - <span data-ttu-id="773ed-133">Baixe o MSI da versão que você quer reverter [aqui](https://www.microsoft.com/edge/business/download).</span><span class="sxs-lookup"><span data-stu-id="773ed-133">Download the MSI for the version you want to roll back to [from here](https://www.microsoft.com/edge/business/download).</span></span>
   - <span data-ttu-id="773ed-134">Salve o MSI na sua área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="773ed-134">Save the MSI to your desktop.</span></span>

3. <span data-ttu-id="773ed-135">Execute o comando de reversão.</span><span class="sxs-lookup"><span data-stu-id="773ed-135">Run the rollback command.</span></span>

   - <span data-ttu-id="773ed-136">Abra o aviso de comando do Windows com **Executar como administrador**.</span><span class="sxs-lookup"><span data-stu-id="773ed-136">Open the Windows command prompt with **Run as administrator**.</span></span>
   - <span data-ttu-id="773ed-137">Digite o seguinte comando, onde: *C:\Users\username\Desktop\test* é o caminho para o MSI baixado e FileName é o nome do arquivo. msi:</span><span class="sxs-lookup"><span data-stu-id="773ed-137">Type the following command, where: *C:\Users\username\Desktop\test* is the path to the MSI you downloaded, and FileName is the name of the .msi file:</span></span><br>
 `C:\Users\username\Desktop\test>msiexec /I FileName.msi /qn ALLOWDOWNGRADE=1`<br>
     > [!NOTE]
     > <span data-ttu-id="773ed-138">Para obter mais informações sobre o msiexec, consulte [msiexec](https://docs.microsoft.com/windows-server/administration/windows-commands/msiexec).</span><span class="sxs-lookup"><span data-stu-id="773ed-138">For more information about msiexec, see [msiexec](https://docs.microsoft.com/windows-server/administration/windows-commands/msiexec).</span></span>
   - <span data-ttu-id="773ed-139">Feche o Microsoft Edge e abra-o novamente para verificar se a reversão funcionou.</span><span class="sxs-lookup"><span data-stu-id="773ed-139">Close and reopen Microsoft Edge to verify that the rollback worked.</span></span> <span data-ttu-id="773ed-140">Em **Configurações e mais** (ALT + F), acesse **Configurações** e selecione **Sobre o Microsoft Edge**.</span><span class="sxs-lookup"><span data-stu-id="773ed-140">Under **Settings and more** (ALT + F), go to **Settings** and select **About Microsoft Edge**.</span></span>

## <span data-ttu-id="773ed-141">Habilitar a reversão com a atualização do Microsoft Edge e a Política de grupo</span><span class="sxs-lookup"><span data-stu-id="773ed-141">Enable rollback with Microsoft Edge update and Group Policy</span></span>

<span data-ttu-id="773ed-142">Use as seguintes etapas para ativar a reversão com a atualização do Microsoft Edge e a Política de grupo.</span><span class="sxs-lookup"><span data-stu-id="773ed-142">Use the following steps to enable rollback with Microsoft Edge update and Group Policy.</span></span>

1. <span data-ttu-id="773ed-143">Abra o Editor de política de grupo local e acesse *Configuração do computador>Atualização do Microsoft Edge>Aplicativos>Microsoft Edge>*.</span><span class="sxs-lookup"><span data-stu-id="773ed-143">Open the local Group Policy Editor and go to *Computer Configuration>Administrative Templates>Microsoft Edge Update>Applications>Microsoft Edge>*.</span></span>
2. <span data-ttu-id="773ed-144">Selecione **Reversão para a versão de destino** e selecione **Habilitado**.</span><span class="sxs-lookup"><span data-stu-id="773ed-144">Select **Rollback to target version** and then select **Enabled**.</span></span>
3. <span data-ttu-id="773ed-145">Selecione **Substituição da versão de destino** e clique na versão do navegador que você quer reverter.</span><span class="sxs-lookup"><span data-stu-id="773ed-145">Select **Target version override** and pick the browser version you want to roll back to.</span></span>
4. <span data-ttu-id="773ed-146">Selecione **Atualizar a substituição da política** e depois selecione **Ativado**.</span><span class="sxs-lookup"><span data-stu-id="773ed-146">Select **Update policy override** and then select **Enabled**.</span></span> <span data-ttu-id="773ed-147">Em **Opções**, escolha uma das opções a seguir na Lista suspensa de políticas (exceto para **Atualização desabilitada**):</span><span class="sxs-lookup"><span data-stu-id="773ed-147">Under **Options**, pick one of the following options from the Policy dropdown list (except for **Update disabled**):</span></span>

   - <span data-ttu-id="773ed-148">Sempre permitir as atualizações</span><span class="sxs-lookup"><span data-stu-id="773ed-148">Always allow updates</span></span>
   - <span data-ttu-id="773ed-149">Apenas atualizações silenciosas automáticas</span><span class="sxs-lookup"><span data-stu-id="773ed-149">Automatic silent updates only</span></span>

     > [!NOTE]
     > <span data-ttu-id="773ed-150">Para forçar uma atualização de política de grupo, digite `dsregcmd /status`no prompt de comando do administrador do Windows (executar como administrador).</span><span class="sxs-lookup"><span data-stu-id="773ed-150">To force a group policy update, type `dsregcmd /status` at the Windows administrator Command Prompt (Run as administrator).</span></span>

5. <span data-ttu-id="773ed-151">Clique em **OK** para salvar as configurações da política.</span><span class="sxs-lookup"><span data-stu-id="773ed-151">Click **OK** to save the policy settings.</span></span> <span data-ttu-id="773ed-152">A reversão ocorrerá na próxima vez que a atualização do Microsoft Edge verificar se há atualizações.</span><span class="sxs-lookup"><span data-stu-id="773ed-152">Rollback will happen the next time Microsoft Edge Update checks for an update.</span></span> <span data-ttu-id="773ed-153">Se você quiser que a atualização ocorra mais cedo, você pode alterar o intervalo de pesquisa do Microsoft Edge Update ou ativar a reversão usando um MSI.</span><span class="sxs-lookup"><span data-stu-id="773ed-153">If you want the update to happen sooner, you can change the Microsoft Edge Update polling interval or enable rollback using an MSI.</span></span>

### <span data-ttu-id="773ed-154">Erros comuns da reversão</span><span class="sxs-lookup"><span data-stu-id="773ed-154">Common rollback errors</span></span>

<span data-ttu-id="773ed-155">Os seguintes erros impedirão a reversão:</span><span class="sxs-lookup"><span data-stu-id="773ed-155">The following errors will prevent rollback:</span></span>

- <span data-ttu-id="773ed-156">A entrada é uma versão de destino sem suporte</span><span class="sxs-lookup"><span data-stu-id="773ed-156">Input is an unsupported target version</span></span>
- <span data-ttu-id="773ed-157">A entrada é uma versão de destino inexistente</span><span class="sxs-lookup"><span data-stu-id="773ed-157">Input is a non-existent target version</span></span>
- <span data-ttu-id="773ed-158">A entrada está formatada incorretamente</span><span class="sxs-lookup"><span data-stu-id="773ed-158">Input is incorrectly formatted</span></span>

### <span data-ttu-id="773ed-159">Políticas de grupo recomendadas</span><span class="sxs-lookup"><span data-stu-id="773ed-159">Recommended Group Policies</span></span>

<span data-ttu-id="773ed-160">As configurações e políticas de grupo a seguir são altamente recomendáveis para usar a reversão.</span><span class="sxs-lookup"><span data-stu-id="773ed-160">The following group policies and settings are highly recommended for using rollback.</span></span>

#### <span data-ttu-id="773ed-161">Políticas de grupo de sincronização</span><span class="sxs-lookup"><span data-stu-id="773ed-161">Sync Group Policies</span></span>

- <span data-ttu-id="773ed-162">ForceSync.</span><span class="sxs-lookup"><span data-stu-id="773ed-162">ForceSync.</span></span> <span data-ttu-id="773ed-163">Defina ForceSync como habilitado.</span><span class="sxs-lookup"><span data-stu-id="773ed-163">Set ForceSync to enabled.</span></span> <span data-ttu-id="773ed-164">Esta política forçará a Sincronização em todos os usuários do Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="773ed-164">This policy will force enable Sync on all Azure Active Directory (Azure AD) users.</span></span> <span data-ttu-id="773ed-165">Essa política só é eficaz para as versões 86 e posteriores do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="773ed-165">This policy is only effective for Microsoft Edge versions 86 and later.</span></span>
- <span data-ttu-id="773ed-166">O *Configurar a lista dos tipos que são excluídos da política de sincronização* permite que os administradores controlem quais dados podem ser sincronizados pelos usuários.</span><span class="sxs-lookup"><span data-stu-id="773ed-166">The *Configure the list of the types that are excluded from synchronization policy* allows admins to control what data can be synced by users.</span></span>

#### <span data-ttu-id="773ed-167">Navegador para reiniciar as Políticas de grupo</span><span class="sxs-lookup"><span data-stu-id="773ed-167">Browser restart Group Policies</span></span>

<span data-ttu-id="773ed-168">Recomendamos forçar a reinicialização dos usuários depois da reversão.</span><span class="sxs-lookup"><span data-stu-id="773ed-168">We recommend forcing a restart on users after rollback is enabled.</span></span>

- <span data-ttu-id="773ed-169">Habilitar *Ativar Notificar um usuário de que é recomendado ou necessário reiniciar um navegador quando houver atualizações pendentes*.</span><span class="sxs-lookup"><span data-stu-id="773ed-169">Enable *Notify a user that a browser restart is recommended or required for pending updates*.</span></span> <span data-ttu-id="773ed-170">Em opções, selecione **Necessário**.</span><span class="sxs-lookup"><span data-stu-id="773ed-170">Under Options, select **Required**.</span></span>
- <span data-ttu-id="773ed-171">Habilitar *Definir o período de tempo das notificações de atualização* e defina o tempo desejado em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="773ed-171">Enable *Set the time period for update notifications* and then set the desired time in milliseconds.</span></span>

## <span data-ttu-id="773ed-172">Instantâneo</span><span class="sxs-lookup"><span data-stu-id="773ed-172">Snapshot</span></span>

<span data-ttu-id="773ed-173">Um instantâneo é uma versão carimbada da pasta dados do usuário.</span><span class="sxs-lookup"><span data-stu-id="773ed-173">A snapshot is a version stamped copy of the user data folder.</span></span> <span data-ttu-id="773ed-174">Durante uma atualização de versão, um instantâneo da versão anterior é feito e armazenado na pasta do instantâneo.</span><span class="sxs-lookup"><span data-stu-id="773ed-174">During a version upgrade, a snapshot of the previous version is made and stored in the snapshot folder.</span></span> <span data-ttu-id="773ed-175">Após a reversão, um instantâneo com a versão correspondida será copiado para a nova pasta de dados do usuário e excluído da pasta do instantâneo.</span><span class="sxs-lookup"><span data-stu-id="773ed-175">After rollback occurs, a version matched snapshot will be copied into the new user data folder and deleted from the snapshot folder.</span></span> <span data-ttu-id="773ed-176">Se uma versão correspondente ao recurso de downgrade não estiver disponível, a reversão dependerá da sincronização para preencher os dados do usuário na nova versão do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="773ed-176">If no version matched snapshot is available upon downgrade, rollback will rely on Sync to populate user data into the new Microsoft Edge version.</span></span>

<span data-ttu-id="773ed-177">A política de grupo [UserDataSnapshotRetentionLimit] permite definir um limite para o número de instantâneos que podem ser mantidos a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="773ed-177">The [UserDataSnapshotRetentionLimit] group policy allows you to set a limit for the number of snapshots that can be retained at any given time.</span></span> <span data-ttu-id="773ed-178">Por padrão, três instantâneos são mantidos.</span><span class="sxs-lookup"><span data-stu-id="773ed-178">By default, three snapshots are kept.</span></span> <span data-ttu-id="773ed-179">Você pode configurar essa política para manter até cinco instantâneos.</span><span class="sxs-lookup"><span data-stu-id="773ed-179">You can configure this policy to keep from 0-5 snapshots.</span></span>

## <span data-ttu-id="773ed-180">Perguntas frequentes</span><span class="sxs-lookup"><span data-stu-id="773ed-180">Frequently asked questions</span></span>

### <span data-ttu-id="773ed-181">Reversão manual do MSI</span><span class="sxs-lookup"><span data-stu-id="773ed-181">Manual MSI rollback</span></span>

#### <span data-ttu-id="773ed-182">Quais erros genéricos do MSI podem ocorrer?</span><span class="sxs-lookup"><span data-stu-id="773ed-182">What generic MSI failures that can happen?</span></span>

1. <span data-ttu-id="773ed-183">Se a política de grupo Instalar atualização estiver desabilitada, a reversão não ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="773ed-183">If the Install update group policy is disabled, rollback won't occur.</span></span>

   - <span data-ttu-id="773ed-184">Para usar a reversão, certifique-se de que a opção Instalar está configurada como **Habilitada**.</span><span class="sxs-lookup"><span data-stu-id="773ed-184">To use rollback, make sure Install is set to **Enabled**.</span></span> <span data-ttu-id="773ed-185">Quando essa política está desabilitada, ela impede que os canais do Microsoft Edge sejam instalados.</span><span class="sxs-lookup"><span data-stu-id="773ed-185">When this policy is disabled, it prevents Microsoft Edge channels from being installed.</span></span> <span data-ttu-id="773ed-186">Para obter mais informações, consulte [Instalar](https://docs.microsoft.com/deployedge/microsoft-edge-update-policies#install).</span><span class="sxs-lookup"><span data-stu-id="773ed-186">For more information, see [Install](https://docs.microsoft.com/deployedge/microsoft-edge-update-policies#install).</span></span>

2. <span data-ttu-id="773ed-187">Se as Atualizações de esclarecimento não estiverem presentes, as instalações do Microsoft Edge serão bloqueadas, a menos que *Permitir que a experiência do navegador Microsoft Edge lado a lado* estiver habilitado.</span><span class="sxs-lookup"><span data-stu-id="773ed-187">If Enlightenment Updates aren't present, Microsoft Edge installations will be blocked unless *Allow Microsoft Edge Side by Side browser experience* is enabled.</span></span>

   - <span data-ttu-id="773ed-188">Para as versões Windows 1903 e 1909: se a sua última atualização foi antes de outubro de 2019, talvez você tenha essa edição.</span><span class="sxs-lookup"><span data-stu-id="773ed-188">For Windows versions 1903 and 1909: If your last update was before October 2019, you may have this issue.</span></span>
   - <span data-ttu-id="773ed-189">Para as versões Windows 1709, 1803 e 1809: se sua última atualização foi antes de novembro de 2019, você pode ter essa edição.</span><span class="sxs-lookup"><span data-stu-id="773ed-189">For Windows versions 1709, 1803, and 1809: If your last update was before November 2019, you may have this issue.</span></span><br>
<span data-ttu-id="773ed-190">Para obter mais informações, consulte [Atualizações do Windows para oferecer suporte à próxima versão do Microsoft Edge](https://docs.microsoft.com/deployedge/microsoft-edge-sysupdate-windows-updates).</span><span class="sxs-lookup"><span data-stu-id="773ed-190">For more information, see [Windows updates to support the next version of Microsoft Edge](https://docs.microsoft.com/deployedge/microsoft-edge-sysupdate-windows-updates)</span></span>

#### <span data-ttu-id="773ed-191">A seguinte mensagem de erro foi exibida depois de usar o Aviso de comando e a reversão não ocorreu.</span><span class="sxs-lookup"><span data-stu-id="773ed-191">The following error message was shown after using the Command Prompt and rollback didn't occur.</span></span> <span data-ttu-id="773ed-192">Qual é o problema?</span><span class="sxs-lookup"><span data-stu-id="773ed-192">What's wrong?</span></span>

![Mensagem de status da reversão](./media/edge-learnmore-rollback/edge-rollback-cmd-flag-error.png)

<span data-ttu-id="773ed-194">*ALLOWDOWNGRADE = 1* não foi executado.</span><span class="sxs-lookup"><span data-stu-id="773ed-194">*ALLOWDOWNGRADE=1* was not executed.</span></span>

### <span data-ttu-id="773ed-195">Reversão da atualização do Microsoft Edge e da Política de grupo</span><span class="sxs-lookup"><span data-stu-id="773ed-195">Microsoft Edge Update and Group Policy rollback</span></span>

#### <span data-ttu-id="773ed-196">Configurei *Reversão para a versão de destino*, habilitei *Substituir a política de atualização*, inseri a versão do navegador desejado para *Substituição da versão de destino*, mas a versão do navegador não era a que eu esperava.</span><span class="sxs-lookup"><span data-stu-id="773ed-196">I set *Rollback to target version*, enabled *Update policy override*, input my desired browser version for *Target version override*, but the browser version wasn't what I expected.</span></span> <span data-ttu-id="773ed-197">Qual é o problema?</span><span class="sxs-lookup"><span data-stu-id="773ed-197">What's wrong?</span></span>

<span data-ttu-id="773ed-198">Alguns erros comuns que impedem a reversão são:</span><span class="sxs-lookup"><span data-stu-id="773ed-198">Some common errors that prevent rollback are:</span></span>

- <span data-ttu-id="773ed-199">Se a Reversão para a versão de destino não for definida, a reversão não será executada.</span><span class="sxs-lookup"><span data-stu-id="773ed-199">If Rollback to target version isn't set, rollback will not be executed.</span></span>
- <span data-ttu-id="773ed-200">Há um dos seguintes problemas com a configuração de substituição da versão de destino:</span><span class="sxs-lookup"><span data-stu-id="773ed-200">There are one of the following issues with the target version override setting:</span></span>

  - <span data-ttu-id="773ed-201">A substituição da versão de destino está definida como uma versão de destino sem suporte.</span><span class="sxs-lookup"><span data-stu-id="773ed-201">Target version override is set to an unsupported target version.</span></span>
  - <span data-ttu-id="773ed-202">A substituição da versão de destino está definida para uma versão de destino inexistente.</span><span class="sxs-lookup"><span data-stu-id="773ed-202">Target version override is set to a non-existent target version.</span></span>
  - <span data-ttu-id="773ed-203">A entrada Substituição da versão de destino está formatada incorretamente.</span><span class="sxs-lookup"><span data-stu-id="773ed-203">Target version override input is incorrectly formatted.</span></span>

- <span data-ttu-id="773ed-204">Se a substituição da política de atualizações estiver definida como " Atualizações desabilitadas", o Microsoft Edge Update não aceitará atualizações e a reversão não será executada.</span><span class="sxs-lookup"><span data-stu-id="773ed-204">If Update policy override is set to "Updates disabled", Microsoft Edge Update won't accept any updates and rollback isn't executed.</span></span>

### <span data-ttu-id="773ed-205">Configurei todas as políticas de grupo corretamente, mas a reversão não foi executada.</span><span class="sxs-lookup"><span data-stu-id="773ed-205">I set all the group policies correctly, but rollback didn't execute.</span></span> <span data-ttu-id="773ed-206">O que aconteceu?</span><span class="sxs-lookup"><span data-stu-id="773ed-206">What happened?</span></span>

<span data-ttu-id="773ed-207">A atualização do Microsoft Edge ainda não executa nenhuma verificação de atualizações.</span><span class="sxs-lookup"><span data-stu-id="773ed-207">Microsoft Edge Update hasn't run a check for updates yet.</span></span> <span data-ttu-id="773ed-208">Por padrão, a atualização automática verifica se há atualizações a cada 10 horas.</span><span class="sxs-lookup"><span data-stu-id="773ed-208">By default, auto-update checks for updates every 10 hours.</span></span> <span data-ttu-id="773ed-209">Você pode corrigir esse problema alterando o intervalo de pesquisa do Microsoft Edge Update com a política de substituição de grupo do período de verificação da atualização automática.</span><span class="sxs-lookup"><span data-stu-id="773ed-209">You can fix this issue by changing Microsoft Edge Update's polling interval with the Auto-update check period override group policy.</span></span> <span data-ttu-id="773ed-210">Para obter mais informações, consulte a política [AutoUpdateCheckPeriodMinutes](https://docs.microsoft.com/deployedge/microsoft-edge-update-policies#autoupdatecheckperiodminutes).</span><span class="sxs-lookup"><span data-stu-id="773ed-210">For more information, see the [AutoUpdateCheckPeriodMinutes](https://docs.microsoft.com/deployedge/microsoft-edge-update-policies#autoupdatecheckperiodminutes) policy.</span></span>

### <span data-ttu-id="773ed-211">Como um Administrador de TI, segui todas as etapas para reverter corretamente.</span><span class="sxs-lookup"><span data-stu-id="773ed-211">As an IT admin, I followed all the steps for rollback correctly.</span></span> <span data-ttu-id="773ed-212">Apenas uma parte do meu grupo de usuários foi revertida.</span><span class="sxs-lookup"><span data-stu-id="773ed-212">Only a portion of my user group was rolled back.</span></span> <span data-ttu-id="773ed-213">Por que os outros usuários ainda não foram revertidos?</span><span class="sxs-lookup"><span data-stu-id="773ed-213">Why haven't the other users been rolled back yet?</span></span>

<span data-ttu-id="773ed-214">A configuração da política de grupo ainda não foi sincronizada com todos os clientes.</span><span class="sxs-lookup"><span data-stu-id="773ed-214">The group policy setting hasn't synced to all the clients yet.</span></span> <span data-ttu-id="773ed-215">Quando o administrador define uma política de grupo, os clientes não recebem essas configurações instantaneamente.</span><span class="sxs-lookup"><span data-stu-id="773ed-215">When admins set a group policy, clients don't receive these settings instantaneously.</span></span> <span data-ttu-id="773ed-216">Você pode [forçar uma atualização remota da política de grupo](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-server-2012-r2-and-2012/jj134201(v=ws.11)).</span><span class="sxs-lookup"><span data-stu-id="773ed-216">You can [Force a Remote Group Policy Refresh](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-server-2012-r2-and-2012/jj134201(v=ws.11)).</span></span>


## <span data-ttu-id="773ed-217">Consulte também</span><span class="sxs-lookup"><span data-stu-id="773ed-217">See also</span></span>

- [<span data-ttu-id="773ed-218">Página de aterrissagem do Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="773ed-218">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
