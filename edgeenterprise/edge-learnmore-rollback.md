---
title: Reversão do Microsoft Edge para empresas
ms.author: v-danwes
author: dan-wesley
manager: srugh
ms.date: 07/21/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Como reverter o Microsoft Edge para uma versão anterior
ms.openlocfilehash: 9af0881a079dd3059e567eaadb912b3d929924c4
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979057"
---
# <span data-ttu-id="c75b5-103">Como reverter o Microsoft Edge para uma versão anterior</span><span class="sxs-lookup"><span data-stu-id="c75b5-103">How to roll back Microsoft Edge to a previous version</span></span>

<span data-ttu-id="c75b5-104">Este artigo descreve como reverter para uma versão anterior do Microsoft Edge usando o recurso de reversão.</span><span class="sxs-lookup"><span data-stu-id="c75b5-104">This article describes how to roll back to a previous version of Microsoft Edge using the rollback feature.</span></span>

>[!NOTE]
><span data-ttu-id="c75b5-105">Este artigo se aplica ao Microsoft Edge versão 86 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="c75b5-105">This article applies to Microsoft Edge version 86 or later.</span></span>

## <span data-ttu-id="c75b5-106">Introdução à reversão</span><span class="sxs-lookup"><span data-stu-id="c75b5-106">Introduction to rollback</span></span>

<span data-ttu-id="c75b5-107">A reversão permite que você substitua a versão do navegador Microsoft Edge por uma versão anterior.</span><span class="sxs-lookup"><span data-stu-id="c75b5-107">Rollback lets you replace your Microsoft Edge browser version with an earlier version.</span></span> <span data-ttu-id="c75b5-108">Esse recurso foi projetado para ser uma rede de segurança para empresas que implantam o Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="c75b5-108">This feature is designed to be a safety net for enterprises deploying Microsoft Edge.</span></span> <span data-ttu-id="c75b5-109">Ele oferece uma maneira de solucionar problemas com o Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="c75b5-109">It provides a way to troubleshoot issues with Microsoft Edge.</span></span> <span data-ttu-id="c75b5-110">Os benefícios da reversão são a possibilidade de reverter para a versão anterior do navegador de forma fácil e rápida.</span><span class="sxs-lookup"><span data-stu-id="c75b5-110">The benefits of rollback are the ability to revert to previous browser version easily and quickly.</span></span> <span data-ttu-id="c75b5-111">A reversão reduz o impacto potencial causado por um problema com o Microsoft Edge nas operações de negócios.</span><span class="sxs-lookup"><span data-stu-id="c75b5-111">Rollback reduces the potential impact that a Microsoft Edge issue has on business operations.</span></span>

## <span data-ttu-id="c75b5-112">Antes de começar</span><span class="sxs-lookup"><span data-stu-id="c75b5-112">Before you begin</span></span>

<span data-ttu-id="c75b5-113">É importante compreender como o recurso de reversão está instalado em um ambiente do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="c75b5-113">It's important to understand how the rollback feature is installed in a Microsoft Edge environment.</span></span> <span data-ttu-id="c75b5-114">Você pode implantar a reversão ao usar dois métodos diferentes: manualmente com, um MSI ou ao usar a atualização do Microsoft Edge e a Política de grupo.</span><span class="sxs-lookup"><span data-stu-id="c75b5-114">You can deploy rollback using two different methods: manually with an MSI or by using Microsoft Edge update and Group Policy.</span></span> <span data-ttu-id="c75b5-115">Também incentivamos o uso de uma seleção das Políticas de grupo para se ter uma implantação mais suave.</span><span class="sxs-lookup"><span data-stu-id="c75b5-115">We also  encourage using a selection of Group Policies for a smoother deployment.</span></span>

### <span data-ttu-id="c75b5-116">Recomendações</span><span class="sxs-lookup"><span data-stu-id="c75b5-116">Recommendations</span></span>

<span data-ttu-id="c75b5-117">O recurso de reversão é destinado a ser uma correção temporária dos problemas que você possa encontrar em uma atualização do navegador Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="c75b5-117">The rollback feature is meant to be a temporary fix for issues you might find in a Microsoft Edge browser update.</span></span> <span data-ttu-id="c75b5-118">Recomendamos que os usuários instalem a versão mais recente do navegador Microsoft Edge para usar a proteção oferecida pelas atualizações de segurança mais recentes.</span><span class="sxs-lookup"><span data-stu-id="c75b5-118">We recommend that users install the latest version of the Microsoft Edge browser to use the protection provided by the latest security updates.</span></span> <span data-ttu-id="c75b5-119">Reverter para uma versão anterior corre o perigo de se expor aos problemas de segurança conhecidos.</span><span class="sxs-lookup"><span data-stu-id="c75b5-119">Rollback to an earlier version risks exposure to known security issues.</span></span>

<span data-ttu-id="c75b5-120">Antes de reverter temporariamente a versão do seu navegador, também recomendamos que você habilite a Sincronização para todos os usuários da sua organização.</span><span class="sxs-lookup"><span data-stu-id="c75b5-120">Before temporarily rolling back your browser version, we also highly recommend that you enable Sync for all the users in your organization.</span></span> <span data-ttu-id="c75b5-121">Se você não ativar a Sincronização, há um risco de perda permanente dos dados de navegação.</span><span class="sxs-lookup"><span data-stu-id="c75b5-121">If you don't turn on Sync, there's a risk of permanent browsing data loss.</span></span> <span data-ttu-id="c75b5-122">Para obter mais informações sobre a Sincronização, consulte [Sincronização do Microsoft Edge](microsoft-edge-enterprise-sync.md).</span><span class="sxs-lookup"><span data-stu-id="c75b5-122">For more information about Sync, see [Microsoft Edge Sync](microsoft-edge-enterprise-sync.md).</span></span>

> [!CAUTION]
> <span data-ttu-id="c75b5-123">Use apenas a reversão quando for necessário, pois sempre há o risco de perda de dados.</span><span class="sxs-lookup"><span data-stu-id="c75b5-123">Only use rollback when necessary, there's always the risk of data loss.</span></span>

## <span data-ttu-id="c75b5-124">Habilitar a reversão manualmente com um MSI</span><span class="sxs-lookup"><span data-stu-id="c75b5-124">Enable rollback manually with an MSI</span></span>

<span data-ttu-id="c75b5-125">Usar as etapas a seguir para fazer a reversão manualmente usando um MSI.</span><span class="sxs-lookup"><span data-stu-id="c75b5-125">Use the following steps to roll back manually with an MSI.</span></span>

1. <span data-ttu-id="c75b5-126">Desabilitar as atualizações do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="c75b5-126">Disable Microsoft Edge Updates.</span></span>

   > [!NOTE]
   > <span data-ttu-id="c75b5-127">Recomendamos que você instale os Modelos administrativos mais recentes.</span><span class="sxs-lookup"><span data-stu-id="c75b5-127">We recommend that you install the most current Administrative templates.</span></span> <span data-ttu-id="c75b5-128">Para obter mais informações, consulte [Download e instalação do modelo administrativo do Microsoft Edge](https://docs.microsoft.com/DeployEdge/configure-microsoft-edge#1-download-and-install-the-microsoft-edge-administrative-template).</span><span class="sxs-lookup"><span data-stu-id="c75b5-128">For more information, see [Download and install the Microsoft Edge administrative template](https://docs.microsoft.com/DeployEdge/configure-microsoft-edge#1-download-and-install-the-microsoft-edge-administrative-template).</span></span>

   - <span data-ttu-id="c75b5-129">Abra o Editor de política de grupo local e acesse *Configuração do computador>Atualização do Microsoft Edge>Aplicativos>Microsoft Edge>*.</span><span class="sxs-lookup"><span data-stu-id="c75b5-129">Open the local Group Policy Editor and go to *Computer Configuration>Administrative Templates>Microsoft Edge Update>Applications>Microsoft Edge>*.</span></span>
   - <span data-ttu-id="c75b5-130">Selecione **Atualizar a substituição da política** e depois selecione **Ativado**.</span><span class="sxs-lookup"><span data-stu-id="c75b5-130">Select **Update policy override** and then select **Enabled**.</span></span>
   - <span data-ttu-id="c75b5-131">Em **Opções**, clique em **Atualização desabilitada** na Lista suspensa de políticas.</span><span class="sxs-lookup"><span data-stu-id="c75b5-131">Under **Options**, pick **Update disabled** from the Policy dropdown list.</span></span>

2. <span data-ttu-id="c75b5-132">Obtenha o MSI.</span><span class="sxs-lookup"><span data-stu-id="c75b5-132">Get the MSI.</span></span>

   - <span data-ttu-id="c75b5-133">Baixe o MSI da versão que você quer reverter [aqui](https://www.microsoft.com/edge/business/download).</span><span class="sxs-lookup"><span data-stu-id="c75b5-133">Download the MSI for the version you want to roll back to [from here](https://www.microsoft.com/edge/business/download).</span></span>
   - <span data-ttu-id="c75b5-134">Salve o MSI na sua área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="c75b5-134">Save the MSI to your desktop.</span></span>

3. <span data-ttu-id="c75b5-135">Execute o comando de reversão.</span><span class="sxs-lookup"><span data-stu-id="c75b5-135">Run the rollback command.</span></span>

   - <span data-ttu-id="c75b5-136">Abra o aviso de comando do Windows com **Executar como administrador**.</span><span class="sxs-lookup"><span data-stu-id="c75b5-136">Open the Windows command prompt with **Run as administrator**.</span></span>
   - <span data-ttu-id="c75b5-137">Digite o seguinte comando, onde: *C:\Users\username\Desktop\test* é o caminho para o MSI baixado e FileName é o nome do arquivo. msi:</span><span class="sxs-lookup"><span data-stu-id="c75b5-137">Type the following command, where: *C:\Users\username\Desktop\test* is the path to the MSI you downloaded, and FileName is the name of the .msi file:</span></span><br>
 `C:\Users\username\Desktop\test>msiexec /I FileName.msi /qn ALLOWDOWNGRADE=1`<br>
     > [!NOTE]
     > <span data-ttu-id="c75b5-138">Para obter mais informações sobre o msiexec, consulte [msiexec](https://docs.microsoft.com/windows-server/administration/windows-commands/msiexec).</span><span class="sxs-lookup"><span data-stu-id="c75b5-138">For more information about msiexec, see [msiexec](https://docs.microsoft.com/windows-server/administration/windows-commands/msiexec).</span></span>
   - <span data-ttu-id="c75b5-139">Feche o Microsoft Edge e abra-o novamente para verificar se a reversão funcionou.</span><span class="sxs-lookup"><span data-stu-id="c75b5-139">Close and reopen Microsoft Edge to verify that the rollback worked.</span></span> <span data-ttu-id="c75b5-140">Em **Configurações e mais** (ALT + F), acesse **Configurações** e selecione **Sobre o Microsoft Edge**.</span><span class="sxs-lookup"><span data-stu-id="c75b5-140">Under **Settings and more** (ALT + F), go to **Settings** and select **About Microsoft Edge**.</span></span>

## <span data-ttu-id="c75b5-141">Habilitar a reversão com a atualização do Microsoft Edge e a Política de grupo</span><span class="sxs-lookup"><span data-stu-id="c75b5-141">Enable rollback with Microsoft Edge update and Group Policy</span></span>

<span data-ttu-id="c75b5-142">Use as seguintes etapas para ativar a reversão com a atualização do Microsoft Edge e a Política de grupo.</span><span class="sxs-lookup"><span data-stu-id="c75b5-142">Use the following steps to enable rollback with Microsoft Edge update and Group Policy.</span></span>

1. <span data-ttu-id="c75b5-143">Abra o Editor de política de grupo local e acesse *Configuração do computador>Atualização do Microsoft Edge>Aplicativos>Microsoft Edge>*.</span><span class="sxs-lookup"><span data-stu-id="c75b5-143">Open the local Group Policy Editor and go to *Computer Configuration>Administrative Templates>Microsoft Edge Update>Applications>Microsoft Edge>*.</span></span>
2. <span data-ttu-id="c75b5-144">Selecione **Reversão para a versão de destino** e selecione **Habilitado**.</span><span class="sxs-lookup"><span data-stu-id="c75b5-144">Select **Rollback to target version** and then select **Enabled**.</span></span>
3. <span data-ttu-id="c75b5-145">Selecione **Substituição da versão de destino** e clique na versão do navegador que você quer reverter.</span><span class="sxs-lookup"><span data-stu-id="c75b5-145">Select **Target version override** and pick the browser version you want to roll back to.</span></span>
4. <span data-ttu-id="c75b5-146">Selecione **Atualizar a substituição da política** e depois selecione **Ativado**.</span><span class="sxs-lookup"><span data-stu-id="c75b5-146">Select **Update policy override** and then select **Enabled**.</span></span> <span data-ttu-id="c75b5-147">Em **Opções**, escolha uma das opções a seguir na Lista suspensa de políticas (exceto para **Atualização desabilitada**):</span><span class="sxs-lookup"><span data-stu-id="c75b5-147">Under **Options**, pick one of the following options from the Policy dropdown list (except for **Update disabled**):</span></span>

   - <span data-ttu-id="c75b5-148">Sempre permitir as atualizações</span><span class="sxs-lookup"><span data-stu-id="c75b5-148">Always allow updates</span></span>
   - <span data-ttu-id="c75b5-149">Apenas atualizações silenciosas automáticas</span><span class="sxs-lookup"><span data-stu-id="c75b5-149">Automatic silent updates only</span></span>
   - <span data-ttu-id="c75b5-150">Apenas atualizações manuais</span><span class="sxs-lookup"><span data-stu-id="c75b5-150">Manual updates only</span></span>  

5. <span data-ttu-id="c75b5-151">A reversão ocorrerá na próxima vez que a atualização do Microsoft Edge verificar se há atualizações.</span><span class="sxs-lookup"><span data-stu-id="c75b5-151">Rollback will happen the next time Microsoft Edge Update checks for an update.</span></span>

   > [!NOTE]
   > <span data-ttu-id="c75b5-152">Se você quiser que a reversão ocorra imediatamente, você tem que alterar o intervalo de pesquisa de atualização do Microsoft Edge ou ativar a reversão usando um MSI.</span><span class="sxs-lookup"><span data-stu-id="c75b5-152">If you want rollback to happen right away you have to change the Microsoft Edge Update polling interval or enable rollback using an MSI.</span></span>

### <span data-ttu-id="c75b5-153">Erros comuns da reversão</span><span class="sxs-lookup"><span data-stu-id="c75b5-153">Common rollback errors</span></span>

<span data-ttu-id="c75b5-154">Os seguintes erros impedirão a reversão:</span><span class="sxs-lookup"><span data-stu-id="c75b5-154">The following errors will prevent rollback:</span></span>

- <span data-ttu-id="c75b5-155">A entrada é uma versão de destino sem suporte</span><span class="sxs-lookup"><span data-stu-id="c75b5-155">Input is an unsupported target version</span></span>
- <span data-ttu-id="c75b5-156">A entrada é uma versão de destino inexistente</span><span class="sxs-lookup"><span data-stu-id="c75b5-156">Input is a non-existent target version</span></span>
- <span data-ttu-id="c75b5-157">A entrada está formatada incorretamente</span><span class="sxs-lookup"><span data-stu-id="c75b5-157">Input is incorrectly formatted</span></span>

### <span data-ttu-id="c75b5-158">Políticas de grupo recomendadas</span><span class="sxs-lookup"><span data-stu-id="c75b5-158">Recommended Group Policies</span></span>

<span data-ttu-id="c75b5-159">As configurações e políticas de grupo a seguir são altamente recomendáveis para usar a reversão.</span><span class="sxs-lookup"><span data-stu-id="c75b5-159">The following group policies and settings are highly recommended for using rollback.</span></span>

#### <span data-ttu-id="c75b5-160">Políticas de grupo de sincronização</span><span class="sxs-lookup"><span data-stu-id="c75b5-160">Sync Group Policies</span></span>

- <span data-ttu-id="c75b5-161">ForceSync.</span><span class="sxs-lookup"><span data-stu-id="c75b5-161">ForceSync.</span></span> <span data-ttu-id="c75b5-162">Defina ForceSync como habilitado.</span><span class="sxs-lookup"><span data-stu-id="c75b5-162">Set ForceSync to enabled.</span></span> <span data-ttu-id="c75b5-163">Esta política forçará a Sincronização em todos os usuários do Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="c75b5-163">This policy will force enable Sync on all Azure Active Directory (Azure AD) users.</span></span> <span data-ttu-id="c75b5-164">Essa política só é eficaz para as versões 86 e posteriores do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="c75b5-164">This policy is only effective for Microsoft Edge versions 86 and later.</span></span>
- <span data-ttu-id="c75b5-165">O *Configurar a lista dos tipos que são excluídos da política de sincronização* permite que os administradores controlem quais dados podem ser sincronizados pelos usuários.</span><span class="sxs-lookup"><span data-stu-id="c75b5-165">The *Configure the list of the types that are excluded from synchronization policy* allows admins to control what data can be synced by users.</span></span>

#### <span data-ttu-id="c75b5-166">Navegador para reiniciar as Políticas de grupo</span><span class="sxs-lookup"><span data-stu-id="c75b5-166">Browser restart Group Policies</span></span>

<span data-ttu-id="c75b5-167">Recomendamos forçar a reinicialização dos usuários depois da reversão.</span><span class="sxs-lookup"><span data-stu-id="c75b5-167">We recommend forcing a restart on users after rollback is enabled.</span></span>

- <span data-ttu-id="c75b5-168">Habilitar *Ativar Notificar um usuário de que é recomendado ou necessário reiniciar um navegador quando houver atualizações pendentes*.</span><span class="sxs-lookup"><span data-stu-id="c75b5-168">Enable *Notify a user that a browser restart is recommended or required for pending updates*.</span></span> <span data-ttu-id="c75b5-169">Em opções, selecione **Necessário**.</span><span class="sxs-lookup"><span data-stu-id="c75b5-169">Under Options, select **Required**.</span></span>
- <span data-ttu-id="c75b5-170">Habilitar *Definir o período de tempo das notificações de atualização* e defina o tempo desejado em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="c75b5-170">Enable *Set the time period for update notifications* and then set the desired time in milliseconds.</span></span>

## <span data-ttu-id="c75b5-171">Perguntas frequentes</span><span class="sxs-lookup"><span data-stu-id="c75b5-171">Frequently asked questions</span></span>

### <span data-ttu-id="c75b5-172">Reversão manual do MSI</span><span class="sxs-lookup"><span data-stu-id="c75b5-172">Manual MSI rollback</span></span>

#### <span data-ttu-id="c75b5-173">Quais erros genéricos do MSI podem ocorrer?</span><span class="sxs-lookup"><span data-stu-id="c75b5-173">What generic MSI failures that can happen?</span></span>

1. <span data-ttu-id="c75b5-174">Se a política de grupo Instalar atualização estiver desabilitada, a reversão não ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="c75b5-174">If the Install update group policy is disabled, rollback won't occur.</span></span>

   - <span data-ttu-id="c75b5-175">Para usar a reversão, certifique-se de que a opção Instalar está configurada como **Habilitada**.</span><span class="sxs-lookup"><span data-stu-id="c75b5-175">To use rollback, make sure Install is set to **Enabled**.</span></span> <span data-ttu-id="c75b5-176">Quando essa política está desabilitada, ela impede que os canais do Microsoft Edge sejam instalados.</span><span class="sxs-lookup"><span data-stu-id="c75b5-176">When this policy is disabled, it prevents Microsoft Edge channels from being installed.</span></span> <span data-ttu-id="c75b5-177">Para obter mais informações, consulte [Instalar](https://docs.microsoft.com/deployedge/microsoft-edge-update-policies#install).</span><span class="sxs-lookup"><span data-stu-id="c75b5-177">For more information, see [Install](https://docs.microsoft.com/deployedge/microsoft-edge-update-policies#install).</span></span>

2. <span data-ttu-id="c75b5-178">Se as Atualizações de esclarecimento não estiverem presentes, as instalações do Microsoft Edge serão bloqueadas, a menos que *Permitir que a experiência do navegador Microsoft Edge lado a lado* estiver habilitado.</span><span class="sxs-lookup"><span data-stu-id="c75b5-178">If Enlightenment Updates aren't present, Microsoft Edge installations will be blocked unless *Allow Microsoft Edge Side by Side browser experience* is enabled.</span></span>

   - <span data-ttu-id="c75b5-179">Para as versões Windows 1903 e 1909: se a sua última atualização foi antes de outubro de 2019, talvez você tenha essa edição.</span><span class="sxs-lookup"><span data-stu-id="c75b5-179">For Windows versions 1903 and 1909: If your last update was before October 2019, you may have this issue.</span></span>
   - <span data-ttu-id="c75b5-180">Para as versões Windows 1709, 1803 e 1809: se sua última atualização foi antes de novembro de 2019, você pode ter essa edição.</span><span class="sxs-lookup"><span data-stu-id="c75b5-180">For Windows versions 1709, 1803, and 1809: If your last update was before November 2019, you may have this issue.</span></span><br>
<span data-ttu-id="c75b5-181">Para obter mais informações, consulte [Atualizações do Windows para oferecer suporte à próxima versão do Microsoft Edge](https://docs.microsoft.com/deployedge/microsoft-edge-sysupdate-windows-updates).</span><span class="sxs-lookup"><span data-stu-id="c75b5-181">For more information, see [Windows updates to support the next version of Microsoft Edge](https://docs.microsoft.com/deployedge/microsoft-edge-sysupdate-windows-updates)</span></span>

#### <span data-ttu-id="c75b5-182">A seguinte mensagem de erro foi exibida depois de usar o Aviso de comando e a reversão não ocorreu.</span><span class="sxs-lookup"><span data-stu-id="c75b5-182">The following error message was shown after using the Command Prompt and rollback didn't occur.</span></span> <span data-ttu-id="c75b5-183">Qual é o problema?</span><span class="sxs-lookup"><span data-stu-id="c75b5-183">What's wrong?</span></span>

![Mensagem de status da reversão](./media/edge-learnmore-rollback/edge-rollback-cmd-flag-error.png)

<span data-ttu-id="c75b5-185">*ALLOWDOWNGRADE = 1* não foi executado.</span><span class="sxs-lookup"><span data-stu-id="c75b5-185">*ALLOWDOWNGRADE=1* was not executed.</span></span>

### <span data-ttu-id="c75b5-186">Reversão da atualização do Microsoft Edge e da Política de grupo</span><span class="sxs-lookup"><span data-stu-id="c75b5-186">Microsoft Edge Update and Group Policy rollback</span></span>

#### <span data-ttu-id="c75b5-187">Configurei *Reversão para a versão de destino*, habilitei *Substituir a política de atualização*, inseri a versão do navegador desejado para *Substituição da versão de destino*, mas a versão do navegador não era a que eu esperava.</span><span class="sxs-lookup"><span data-stu-id="c75b5-187">I set *Rollback to target version*, enabled *Update policy override*, input my desired browser version for *Target version override*, but the browser version wasn't what I expected.</span></span> <span data-ttu-id="c75b5-188">Qual é o problema?</span><span class="sxs-lookup"><span data-stu-id="c75b5-188">What's wrong?</span></span>

<span data-ttu-id="c75b5-189">Alguns erros comuns que impedem a reversão são:</span><span class="sxs-lookup"><span data-stu-id="c75b5-189">Some common errors that prevent rollback are:</span></span>

- <span data-ttu-id="c75b5-190">Se a Reversão para a versão de destino não for definida, a reversão não será executada.</span><span class="sxs-lookup"><span data-stu-id="c75b5-190">If Rollback to target version isn't set, rollback will not be executed.</span></span>
- <span data-ttu-id="c75b5-191">Há um dos seguintes problemas com a configuração de substituição da versão de destino:</span><span class="sxs-lookup"><span data-stu-id="c75b5-191">There are one of the following issues with the target version override setting:</span></span>

  - <span data-ttu-id="c75b5-192">A substituição da versão de destino está definida como uma versão de destino sem suporte.</span><span class="sxs-lookup"><span data-stu-id="c75b5-192">Target version override is set to an unsupported target version.</span></span>
  - <span data-ttu-id="c75b5-193">A substituição da versão de destino está definida para uma versão de destino inexistente.</span><span class="sxs-lookup"><span data-stu-id="c75b5-193">Target version override is set to a non-existent target version.</span></span>
  - <span data-ttu-id="c75b5-194">A entrada Substituição da versão de destino está formatada incorretamente.</span><span class="sxs-lookup"><span data-stu-id="c75b5-194">Target version override input is incorrectly formatted.</span></span>

- <span data-ttu-id="c75b5-195">Se a Substituição da política de atualizações estiver definida como " Atualizações desabilitadas", as atualizações do Microsoft Edge não aceitarão atualizações.</span><span class="sxs-lookup"><span data-stu-id="c75b5-195">If Update policy override is set to "Updates disabled", Microsoft Edge Update won't accept any updates.</span></span> <span data-ttu-id="c75b5-196">Isso resulta em uma reversão não executada.</span><span class="sxs-lookup"><span data-stu-id="c75b5-196">This results in rollback not getting executed.</span></span>

### <span data-ttu-id="c75b5-197">Configurei todas as políticas de grupo corretamente, mas a reversão não foi executada.</span><span class="sxs-lookup"><span data-stu-id="c75b5-197">I set all the group policies correctly, but rollback didn't execute.</span></span> <span data-ttu-id="c75b5-198">O que aconteceu?</span><span class="sxs-lookup"><span data-stu-id="c75b5-198">What happened?</span></span>

<span data-ttu-id="c75b5-199">A atualização do Microsoft Edge ainda não executa nenhuma verificação de atualizações.</span><span class="sxs-lookup"><span data-stu-id="c75b5-199">Microsoft Edge Update hasn't run a check for updates yet.</span></span> <span data-ttu-id="c75b5-200">Por padrão, a atualização automática verifica se há atualizações a cada 10 horas.</span><span class="sxs-lookup"><span data-stu-id="c75b5-200">By default, auto-update checks for updates every 10 hours.</span></span> <span data-ttu-id="c75b5-201">Você pode corrigir isso alterando o intervalo de pesquisa de atualização do Microsoft Edge com a política de grupo Substituição automática do período de verificação da atualização.</span><span class="sxs-lookup"><span data-stu-id="c75b5-201">You can fix this by changing Microsoft Edge Update's polling interval with the Auto-update check period override group policy.</span></span> <span data-ttu-id="c75b5-202">Para obter mais informações, consulte a política [AutoUpdateCheckPeriodMinutes](https://docs.microsoft.com/deployedge/microsoft-edge-update-policies#autoupdatecheckperiodminutes).</span><span class="sxs-lookup"><span data-stu-id="c75b5-202">For more information, see the [AutoUpdateCheckPeriodMinutes](https://docs.microsoft.com/deployedge/microsoft-edge-update-policies#autoupdatecheckperiodminutes) policy.</span></span>

### <span data-ttu-id="c75b5-203">Como um Administrador de TI, segui todas as etapas para reverter corretamente.</span><span class="sxs-lookup"><span data-stu-id="c75b5-203">As an IT admin, I followed all the steps for rollback correctly.</span></span> <span data-ttu-id="c75b5-204">Apenas uma parte do meu grupo de usuários foi revertida.</span><span class="sxs-lookup"><span data-stu-id="c75b5-204">Only a portion of my user group was rolled back.</span></span> <span data-ttu-id="c75b5-205">Por que os outros usuários ainda não foram revertidos?</span><span class="sxs-lookup"><span data-stu-id="c75b5-205">Why haven't the other users been rolled back yet?</span></span>

<span data-ttu-id="c75b5-206">A configuração da política de grupo ainda não foi sincronizada com todos os clientes.</span><span class="sxs-lookup"><span data-stu-id="c75b5-206">The group policy setting hasn't synced to all the clients yet.</span></span> <span data-ttu-id="c75b5-207">Quando o administrador define uma política de grupo, os clientes não recebem essas configurações instantaneamente.</span><span class="sxs-lookup"><span data-stu-id="c75b5-207">When admins set a group policy, clients don't receive these settings instantaneously.</span></span>

<!--
You can update all users' group policy with the  

When admins set all users don't get this setting instantaneously 

GP Update force group policy – link to this 

-->





## <span data-ttu-id="c75b5-208">Consulte também</span><span class="sxs-lookup"><span data-stu-id="c75b5-208">See also</span></span>

- [<span data-ttu-id="c75b5-209">Página de aterrissagem do Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="c75b5-209">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
