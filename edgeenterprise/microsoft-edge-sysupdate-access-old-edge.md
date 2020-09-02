---
title: Acessar a versão antiga do Microsoft Edge
ms.author: jtkim
author: dan-wesley
manager: srugh
ms.date: 08/17/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Saiba como acessar a versão herdada do Microsoft Edge.
ms.openlocfilehash: e5a97a487dc6b3a45504a721e460a69103b0174e
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979103"
---
# <span data-ttu-id="2c299-103">Acessar a Versão Herdada do Microsoft Edge depois de instalar a nova versão do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="2c299-103">Access Microsoft Edge Legacy after installing the new version of Microsoft Edge</span></span>

<span data-ttu-id="2c299-104">Saiba como acessar a Versão Herdada do Microsoft Edge depois de instalar a nova versão do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2c299-104">Learn how to access Microsoft Edge Legacy after installing the new version of Microsoft Edge.</span></span>

> [!NOTE]
> <span data-ttu-id="2c299-105">Este artigo aplica-se ao [canal Estável](microsoft-edge-channels.md) do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2c299-105">This article applies to the Microsoft Edge [Stable channel](microsoft-edge-channels.md).</span></span>

<span data-ttu-id="2c299-106">Embora a maioria das organizações queira substituir o Microsoft Edge Legacy pela nova versão, há algumas situações em que os usuários precisarão acessar as duas versões.</span><span class="sxs-lookup"><span data-stu-id="2c299-106">While most organizations will want to replace Microsoft Edge Legacy with the new version, there are some situations where users will need access to both versions.</span></span> <span data-ttu-id="2c299-107">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="2c299-107">For example:</span></span>

- <span data-ttu-id="2c299-108">Assistência técnica e equipe de suporte que interagem com os usuários que estão usando uma ou ambas as versões do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2c299-108">Helpdesk and support staff who interact with users who are using either or both versions of Microsoft Edge.</span></span>
- <span data-ttu-id="2c299-109">Desenvolvedores que oferecem suporte aos clientes que usam uma ou ambas as versões do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2c299-109">Developers who support customers who are using either or both versions of Microsoft Edge.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2c299-110">Executar a Versão Prévia do Microsoft Edge lado a lado com a nova versão do Microsoft Edge não é recomendável para uso em produção.</span><span class="sxs-lookup"><span data-stu-id="2c299-110">Running Microsoft Edge Legacy side-by-side with the new version of Microsoft Edge is not recommended for use in production.</span></span> <span data-ttu-id="2c299-111">Essa configuração deve ser usada apenas em casos específicos em que é necessário testar as versões do navegador.</span><span class="sxs-lookup"><span data-stu-id="2c299-111">This configuration should only be used in specific cases where testing with both browser versions is required.</span></span>
>
> <span data-ttu-id="2c299-112">O aplicativo de área de trabalho da Versão Prévia do Microsoft Edge chegará ao fim do suporte em 9 de março de 2021 em favor do novo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2c299-112">The Microsoft Edge Legacy desktop app will reach end of support on March 9, 2021 in favor of the new Microsoft Edge.</span></span> <span data-ttu-id="2c299-113">Isso significa que a Versão Prévia do Microsoft Edge não receberá atualizações de segurança após essa data.</span><span class="sxs-lookup"><span data-stu-id="2c299-113">This means that Microsoft Edge Legacy will not receive security updates after that date.</span></span> <span data-ttu-id="2c299-114">Essa alteração é aplicável a todas as experiências executadas no aplicativo da área de trabalho da Versão Prévia do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2c299-114">This change is applicable to all experiences that run in the Microsoft Edge Legacy desktop app.</span></span> <span data-ttu-id="2c299-115">[Saiba mais](https://techcommunity.microsoft.com/t5/microsoft-365-blog/microsoft-365-apps-say-farewell-to-internet-explorer-11-and/ba-p/1591666).</span><span class="sxs-lookup"><span data-stu-id="2c299-115">[Learn more](https://techcommunity.microsoft.com/t5/microsoft-365-blog/microsoft-365-apps-say-farewell-to-internet-explorer-11-and/ba-p/1591666).</span></span>

## <span data-ttu-id="2c299-116">Antes de começar</span><span class="sxs-lookup"><span data-stu-id="2c299-116">Before you begin</span></span>

<span data-ttu-id="2c299-117">Os procedimentos neste artigo se aplicam aos sistemas que foram atualizados com as últimas atualizações de segurança.</span><span class="sxs-lookup"><span data-stu-id="2c299-117">The procedures in this article apply to systems that have been updated with the latest security updates.</span></span> <span data-ttu-id="2c299-118">Quando a nova versão do Microsoft Edge estiver instalada, a versão antiga (Versão Herdada do Microsoft Edge) será ocultada.</span><span class="sxs-lookup"><span data-stu-id="2c299-118">When the new version of Microsoft Edge is installed, the old version (Microsoft Edge Legacy) will be hidden.</span></span> <span data-ttu-id="2c299-119">Por padrão, todas as tentativas de iniciar a versão antiga irão redirecionar o usuário para a versão recém-instalada do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2c299-119">By default, all attempts to launch the old version will redirect the user to the newly installed version of Microsoft Edge.</span></span> <span data-ttu-id="2c299-120">Este artigo descreve como você pode continuar usando o Microsoft Edge herdado após instalar o Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2c299-120">This article describes how you can keep using Microsoft Edge Legacy after you install Microsoft Edge.</span></span>

## <span data-ttu-id="2c299-121">QuickStart: experiência lado a lado com o Microsoft Edge Beta e a Versão Prévia do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="2c299-121">Quickstart: Side-by-side experience with Microsoft Edge Beta Channel and Microsoft Edge Legacy</span></span>

<span data-ttu-id="2c299-122">Antes de usar as instruções detalhadas deste artigo, considere as duas etapas a seguir para permitir que os usuários executem a Versão Prévia do Microsoft Edge e o Microsoft Edge ([canal Beta](microsoft-edge-channels.md)) lado a lado.</span><span class="sxs-lookup"><span data-stu-id="2c299-122">Before using the detailed instructions in this article, consider the following two steps to let your users run Microsoft Edge Legacy and the Microsoft Edge [Beta channel](microsoft-edge-channels.md) side-by-side.</span></span>

1. <span data-ttu-id="2c299-123">Impeça a instalação automática do Canal Estável de Microsoft Edge pelo [Windows Update.](https://support.microsoft.com/help/12373/windows-update-faq).</span><span class="sxs-lookup"><span data-stu-id="2c299-123">Prevent the automatic install of the Stable Channel of Microsoft Edge by [Windows Update](https://support.microsoft.com/help/12373/windows-update-faq).</span></span>

   > [!TIP]
   > <span data-ttu-id="2c299-124">Use o [Blocker Toolkit](microsoft-edge-blocker-toolkit.md) para desabilitar a entrega automática do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2c299-124">Use the [Blocker Toolkit](microsoft-edge-blocker-toolkit.md) to disable automatic delivery of Microsoft Edge.</span></span>

2. <span data-ttu-id="2c299-125">Instale o [canal Beta](https://www.microsoft.com/edge/business/download) da nova versão do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2c299-125">Install the [Beta channel](https://www.microsoft.com/edge/business/download) of the new version of Microsoft Edge.</span></span>

   > [!NOTE]
   > <span data-ttu-id="2c299-126">Leia [Informações adicionais](#additional-information) para saber mais sobre as configurações de chave do registro.</span><span class="sxs-lookup"><span data-stu-id="2c299-126">Read [Additional information](#additional-information) for information about Registry Key settings.</span></span>

<span data-ttu-id="2c299-127">Essa solução lado a lado é menos complexa e requer menos gerenciamento do que a solução detalhada descrita neste artigo.</span><span class="sxs-lookup"><span data-stu-id="2c299-127">This side-by-side solution is less complex and requires less management than the detailed solution described in this article.</span></span> <span data-ttu-id="2c299-128">No entanto, isso significa que você estará executando o canal Beta em vez do canal Estável.</span><span class="sxs-lookup"><span data-stu-id="2c299-128">However, this solution does mean that you'll be running the Beta Channel rather than the Stable Channel.</span></span>

## <span data-ttu-id="2c299-129">Experiência lado a lado com o canal estável do Microsoft Edge e a Versão Prévia do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="2c299-129">Side-by-side experience with Microsoft Edge Stable Channel and Microsoft Edge Legacy</span></span>

<span data-ttu-id="2c299-130">Instalar o canal Estável da próxima versão do Microsoft Edge no nível do sistema fará com que a versão atual (Versão Herdada do Microsoft Edge) seja ocultada.</span><span class="sxs-lookup"><span data-stu-id="2c299-130">Installing the Stable Channel of the next version of Microsoft Edge at the system-level will cause the current version (Microsoft Edge Legacy) to be hidden.</span></span> <span data-ttu-id="2c299-131">Para permitir que os usuários vejam as duas versões do Microsoft Edge lado a lado no Windows, você poderá habilitar essa experiência ao definir a política de grupo **Permitir experiência de navegador Lado a Lado do Microsoft Edge** como **Habilitada**.</span><span class="sxs-lookup"><span data-stu-id="2c299-131">If you want to let your users see both versions of Microsoft Edge side by side in Windows, you can enable this experience by setting the **Allow Microsoft Edge Side by Side browser experience** group policy to **Enabled**.</span></span>

<span data-ttu-id="2c299-132">Essa política de grupo é documentada [aqui](https://docs.microsoft.com/deployedge/microsoft-edge-update-policies#allowsxs)</span><span class="sxs-lookup"><span data-stu-id="2c299-132">This group policy is documented [here](https://docs.microsoft.com/deployedge/microsoft-edge-update-policies#allowsxs)</span></span>

### <span data-ttu-id="2c299-133">Para configurar a política de experiência do navegador lado a lado:</span><span class="sxs-lookup"><span data-stu-id="2c299-133">To set up the side-by-side browser experience policy:</span></span>

1. <span data-ttu-id="2c299-134">Instalar as definições de política do [Microsoft Edge for Business](https://www.microsoft.com/edge/business/download).</span><span class="sxs-lookup"><span data-stu-id="2c299-134">Install the Policy Definitions from [Microsoft Edge for Business](https://www.microsoft.com/edge/business/download).</span></span>

   - <span data-ttu-id="2c299-135">Escolha o CANAL/BUILD e a plataforma que você deseja usar e, em seguida, clique em OBTER ARQUIVOS DE POLÍTICA.</span><span class="sxs-lookup"><span data-stu-id="2c299-135">Pick the CHANNEL/BUILD and PLATFORM you want to use, and then click GET POLICY FILES.</span></span>
   - <span data-ttu-id="2c299-136">Extraia o arquivo compactados.</span><span class="sxs-lookup"><span data-stu-id="2c299-136">Extract the zipped files.</span></span>
   - <span data-ttu-id="2c299-137">Copie msedge.admx e msedgeupdate.admx para o diretório `C:\Windows\PolicyDefinitions`.</span><span class="sxs-lookup"><span data-stu-id="2c299-137">Copy msedge.admx and msedgeupdate.admx to the `C:\Windows\PolicyDefinitions` directory.</span></span>
   - <span data-ttu-id="2c299-138">Copie msedge.adml e msedgeupdate.adml (do diretório de idioma/local apropriado) para o diretório `C:\Windows\PolicyDefinitions\[APPROPRIATE LANGUAGE/LOCALE]`.</span><span class="sxs-lookup"><span data-stu-id="2c299-138">Copy msedge.adml and msedgeupdate.adml (from the appropriate language/locale directory) to the `C:\Windows\PolicyDefinitions\[APPROPRIATE LANGUAGE/LOCALE]` directory.</span></span>

2. <span data-ttu-id="2c299-139">Abra o Editor de Política de Grupo (gpedit.msc).</span><span class="sxs-lookup"><span data-stu-id="2c299-139">Open the Group Policy Editor (gpedit.msc).</span></span>
3. <span data-ttu-id="2c299-140">Em **Configuração do Computador**, vá para *Modelos Administrativos>Microsoft Edge Update>Aplicativos*.</span><span class="sxs-lookup"><span data-stu-id="2c299-140">Under **Computer Configuration**, go to *Administrative Templates>Microsoft Edge Update>Applications*.</span></span>

    > [!NOTE]
    > <span data-ttu-id="2c299-141">Se você não vir \* Microsoft Edge Update\*, verifique se a etapa 1 foi concluída corretamente.</span><span class="sxs-lookup"><span data-stu-id="2c299-141">If you don't see the *Microsoft Edge Update* folder, verify that step 1 was completed correctly.</span></span>

4. <span data-ttu-id="2c299-142">Em **Aplicativos**, clique duas vezes em "Permitir a experiência de navegador Lado a Lado do Microsoft Edge".</span><span class="sxs-lookup"><span data-stu-id="2c299-142">Under **Applications**, double-click "Allow Microsoft Edge Side by Side browser experience".</span></span> <span data-ttu-id="2c299-143">Veja nossas [práticas recomendadas](#best-practice-guidance) antes de passar para a próxima etapa.</span><span class="sxs-lookup"><span data-stu-id="2c299-143">See our [best practice guidance](#best-practice-guidance) before continuing to the next step.</span></span>

    > [!NOTE]
    > <span data-ttu-id="2c299-144">Por padrão, essa política de grupo é definida como "Não configurada", o que resultará na Versão Herdada do Microsoft Edge sendo ocultada quando a nova versão do Microsoft Edge for instalada.</span><span class="sxs-lookup"><span data-stu-id="2c299-144">By default, this group policy is set to "Not configured", which results in Microsoft Edge Legacy being hidden when the new version of Microsoft Edge is installed.</span></span>

5. <span data-ttu-id="2c299-145">Selecione **Habilitado** e, em seguida, clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="2c299-145">Select **Enabled** and then click **OK**.</span></span>  

<span data-ttu-id="2c299-146">Definir essa política definirá a seguinte chave do Registro como '00000001':</span><span class="sxs-lookup"><span data-stu-id="2c299-146">Setting this policy will set the following Registry Key  to '00000001':</span></span>

- <span data-ttu-id="2c299-147">Chave:</span><span class="sxs-lookup"><span data-stu-id="2c299-147">Key:</span></span> `Computer\HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate`
- <span data-ttu-id="2c299-148">Nome do valor:</span><span class="sxs-lookup"><span data-stu-id="2c299-148">Value Name:</span></span> `Allowsxs`
- <span data-ttu-id="2c299-149">Tipo de valor:</span><span class="sxs-lookup"><span data-stu-id="2c299-149">Value Type:</span></span> `'REG_DWORD'`

#### <span data-ttu-id="2c299-150">Diretrizes de prática recomendada</span><span class="sxs-lookup"><span data-stu-id="2c299-150">Best practice guidance</span></span>

<span data-ttu-id="2c299-151">Para a melhor experiência, **Permitir experiência de navegador Lado a Lado do Microsoft Edge** deve ser habilitado antes que a nova versão do Microsoft Edge seja implantada nos dispositivos dos usuários.</span><span class="sxs-lookup"><span data-stu-id="2c299-151">For the best experience, the **Allow Microsoft Edge Side by Side browser experience** should be enabled before the new version of Microsoft Edge is deployed to your users' devices.</span></span>

<span data-ttu-id="2c299-152">Se a política de grupo for habilitada depois que o Microsoft Edge tiver sido implantado, haverá os seguintes efeitos colaterais e as ações necessárias:</span><span class="sxs-lookup"><span data-stu-id="2c299-152">If the group policy is enabled after Microsoft Edge is deployed, there are the following side effects and required actions:</span></span>

1. <span data-ttu-id="2c299-153">**Permitir experiência de navegador Lado a Lado do Microsoft Edge** não entrará em vigor até o instalador da nova versão do Microsoft Edge ser executado novamente.</span><span class="sxs-lookup"><span data-stu-id="2c299-153">**Allow Microsoft Edge Side by Side browser experience** won't take effect until after the installer for the new version of Microsoft Edge is run again.</span></span>

   > [!NOTE]
   > <span data-ttu-id="2c299-154">O instalador pode ser executado direta ou automaticamente quando a nova versão do Microsoft Edge for atualizada.</span><span class="sxs-lookup"><span data-stu-id="2c299-154">The installer can be run directly or automatically when the new version of Microsoft Edge updates.</span></span>

2. <span data-ttu-id="2c299-155">A Versão Herdada do Microsoft Edge precisará ser fixada novamente em Iniciar ou na Barra de Tarefas porque o marcador será migrado quando a nova versão do Microsoft Edge for implantada.</span><span class="sxs-lookup"><span data-stu-id="2c299-155">Microsoft Edge Legacy will need to be re-pinned to Start or the Taskbar because the pin is migrated when the new version of Microsoft Edge is deployed.</span></span>
3. <span data-ttu-id="2c299-156">Os sites fixados em Iniciar ou na Barra de Tarefas para a Versão Herdada do Microsoft Edge serão migrados para a nova versão do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2c299-156">Sites that were pinned to Start or the Taskbar for Microsoft Edge Legacy will be migrated to the new version of Microsoft Edge.</span></span>

## <span data-ttu-id="2c299-157">Informações adicionais</span><span class="sxs-lookup"><span data-stu-id="2c299-157">Additional information</span></span>

<span data-ttu-id="2c299-158">Depois que os sistemas forem totalmente atualizados e o canal Estável da próxima versão do Microsoft Edge for instalado, a seguinte chave do Registro e o valor serão definidos:</span><span class="sxs-lookup"><span data-stu-id="2c299-158">After the systems are fully updated and the Stable channel of the next version of Microsoft Edge is installed, the following registry key and value is set:</span></span>

- <span data-ttu-id="2c299-159">Chave:</span><span class="sxs-lookup"><span data-stu-id="2c299-159">Key:</span></span> `Computer\HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\EdgeUpdate\ClientState\{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}`
- <span data-ttu-id="2c299-160">Valor da chave:</span><span class="sxs-lookup"><span data-stu-id="2c299-160">Key value:</span></span> `BrowserReplacement`

  > [!IMPORTANT]
  > <span data-ttu-id="2c299-161">Essa chave é substituída sempre que o canal Estável do Microsoft Edge é atualizado.</span><span class="sxs-lookup"><span data-stu-id="2c299-161">This key is over-written every time the Microsoft Edge Stable channel is updated.</span></span> <span data-ttu-id="2c299-162">Como uma prática recomendada, recomendamos que você NÃO exclua essa chave para permitir que os usuários acessem as duas versões do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2c299-162">As a best practice, we recommend that you DO NOT delete this key to allow users to access both versions of Microsoft Edge.</span></span>

## <span data-ttu-id="2c299-163">Consulte também</span><span class="sxs-lookup"><span data-stu-id="2c299-163">See also</span></span>

- [<span data-ttu-id="2c299-164">Página de aterrissagem do Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="2c299-164">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="2c299-165">Atualizações do Windows para dar suporte ao Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="2c299-165">Windows updates to support Microsoft Edge</span></span>](microsoft-edge-sysupdate-windows-updates.md)
