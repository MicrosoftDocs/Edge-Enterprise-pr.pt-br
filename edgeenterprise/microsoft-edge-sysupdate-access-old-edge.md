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
ms.openlocfilehash: e4733d020f3a681ded50e5a087fe086d39362201
ms.sourcegitcommit: f7f7eb69d2298b0f9779a9fd28e3c4e297ef2e05
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125513"
---
# <span data-ttu-id="4773e-103">Acessar a Versão Herdada do Microsoft Edge depois de instalar a nova versão do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="4773e-103">Access Microsoft Edge Legacy after installing the new version of Microsoft Edge</span></span>

<span data-ttu-id="4773e-104">Saiba como acessar a Versão Herdada do Microsoft Edge depois de instalar a nova versão do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="4773e-104">Learn how to access Microsoft Edge Legacy after installing the new version of Microsoft Edge.</span></span>

> [!NOTE]
> <span data-ttu-id="4773e-105">Este artigo aplica-se ao [canal Estável](microsoft-edge-channels.md) do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="4773e-105">This article applies to the Microsoft Edge [Stable channel](microsoft-edge-channels.md).</span></span>

<span data-ttu-id="4773e-106">Embora a maioria das organizações queira substituir o Microsoft Edge Legacy pela nova versão, há algumas situações em que os usuários precisarão acessar as duas versões.</span><span class="sxs-lookup"><span data-stu-id="4773e-106">While most organizations will want to replace Microsoft Edge Legacy with the new version, there are some situations where users will need access to both versions.</span></span> <span data-ttu-id="4773e-107">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="4773e-107">For example:</span></span>

- <span data-ttu-id="4773e-108">Assistência técnica e equipe de suporte que interagem com os usuários que estão usando uma ou ambas as versões do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="4773e-108">Helpdesk and support staff who interact with users who are using either or both versions of Microsoft Edge.</span></span>
- <span data-ttu-id="4773e-109">Desenvolvedores que oferecem suporte aos clientes que usam uma ou ambas as versões do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="4773e-109">Developers who support customers who are using either or both versions of Microsoft Edge.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4773e-110">Executar a Versão Prévia do Microsoft Edge lado a lado com a nova versão do Microsoft Edge não é recomendável para uso em produção.</span><span class="sxs-lookup"><span data-stu-id="4773e-110">Running Microsoft Edge Legacy side-by-side with the new version of Microsoft Edge is not recommended for use in production.</span></span> <span data-ttu-id="4773e-111">Essa configuração deve ser usada apenas em casos específicos em que é necessário testar as versões do navegador.</span><span class="sxs-lookup"><span data-stu-id="4773e-111">This configuration should only be used in specific cases where testing with both browser versions is required.</span></span>
>
> <span data-ttu-id="4773e-112">O aplicativo de área de trabalho da Versão Prévia do Microsoft Edge chegará ao fim do suporte em 9 de março de 2021 em favor do novo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="4773e-112">The Microsoft Edge Legacy desktop app will reach end of support on March 9, 2021 in favor of the new Microsoft Edge.</span></span> <span data-ttu-id="4773e-113">Isso significa que a Versão Prévia do Microsoft Edge não receberá atualizações de segurança após essa data.</span><span class="sxs-lookup"><span data-stu-id="4773e-113">This means that Microsoft Edge Legacy will not receive security updates after that date.</span></span> <span data-ttu-id="4773e-114">Essa alteração é aplicável a todas as experiências executadas no aplicativo da área de trabalho da Versão Prévia do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="4773e-114">This change is applicable to all experiences that run in the Microsoft Edge Legacy desktop app.</span></span> <span data-ttu-id="4773e-115">[Saiba mais](https://techcommunity.microsoft.com/t5/microsoft-365-blog/microsoft-365-apps-say-farewell-to-internet-explorer-11-and/ba-p/1591666).</span><span class="sxs-lookup"><span data-stu-id="4773e-115">[Learn more](https://techcommunity.microsoft.com/t5/microsoft-365-blog/microsoft-365-apps-say-farewell-to-internet-explorer-11-and/ba-p/1591666).</span></span>

## <span data-ttu-id="4773e-116">Antes de começar</span><span class="sxs-lookup"><span data-stu-id="4773e-116">Before you begin</span></span>
> [!NOTE]
> <span data-ttu-id="4773e-117">A partir do Windows 10 versão 20H2 a Versão Prévia do Microsoft Edge não está mais incluída.</span><span class="sxs-lookup"><span data-stu-id="4773e-117">Starting with Windows 10 version 20H2 Microsoft Edge Legacy is no longer included.</span></span> <span data-ttu-id="4773e-118">A experiência lado a lado não é compatível com esta versão do Windows 10.</span><span class="sxs-lookup"><span data-stu-id="4773e-118">Starting with this version of Windows 10 the side-by-side experience is not supported.</span></span>

<span data-ttu-id="4773e-119">Os procedimentos neste artigo se aplicam aos sistemas que foram atualizados com as últimas atualizações de segurança.</span><span class="sxs-lookup"><span data-stu-id="4773e-119">The procedures in this article apply to systems that have been updated with the latest security updates.</span></span> <span data-ttu-id="4773e-120">Quando a nova versão do Microsoft Edge estiver instalada, a versão antiga (Versão Herdada do Microsoft Edge) será ocultada.</span><span class="sxs-lookup"><span data-stu-id="4773e-120">When the new version of Microsoft Edge is installed, the old version (Microsoft Edge Legacy) will be hidden.</span></span> <span data-ttu-id="4773e-121">Por padrão, todas as tentativas de iniciar a versão antiga irão redirecionar o usuário para a versão recém-instalada do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="4773e-121">By default, all attempts to launch the old version will redirect the user to the newly installed version of Microsoft Edge.</span></span> <span data-ttu-id="4773e-122">Este artigo descreve como você pode continuar usando o Microsoft Edge herdado após instalar o Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="4773e-122">This article describes how you can keep using Microsoft Edge Legacy after you install Microsoft Edge.</span></span>

## <span data-ttu-id="4773e-123">QuickStart: experiência lado a lado com o Microsoft Edge Beta e a Versão Prévia do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="4773e-123">Quickstart: Side-by-side experience with Microsoft Edge Beta Channel and Microsoft Edge Legacy</span></span>

<span data-ttu-id="4773e-124">Antes de usar as instruções detalhadas deste artigo, considere as duas etapas a seguir para permitir que os usuários executem a Versão Prévia do Microsoft Edge e o Microsoft Edge ([canal Beta](microsoft-edge-channels.md)) lado a lado.</span><span class="sxs-lookup"><span data-stu-id="4773e-124">Before using the detailed instructions in this article, consider the following two steps to let your users run Microsoft Edge Legacy and the Microsoft Edge [Beta channel](microsoft-edge-channels.md) side-by-side.</span></span>

1. <span data-ttu-id="4773e-125">Impeça a instalação automática do Canal Estável de Microsoft Edge pelo [Windows Update.](https://support.microsoft.com/help/12373/windows-update-faq).</span><span class="sxs-lookup"><span data-stu-id="4773e-125">Prevent the automatic install of the Stable Channel of Microsoft Edge by [Windows Update](https://support.microsoft.com/help/12373/windows-update-faq).</span></span>

   > [!TIP]
   > <span data-ttu-id="4773e-126">Use o [Blocker Toolkit](microsoft-edge-blocker-toolkit.md) para desabilitar a entrega automática do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="4773e-126">Use the [Blocker Toolkit](microsoft-edge-blocker-toolkit.md) to disable automatic delivery of Microsoft Edge.</span></span>

2. <span data-ttu-id="4773e-127">Instale o [canal Beta](https://www.microsoft.com/edge/business/download) da nova versão do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="4773e-127">Install the [Beta channel](https://www.microsoft.com/edge/business/download) of the new version of Microsoft Edge.</span></span>

   > [!NOTE]
   > <span data-ttu-id="4773e-128">Leia [Informações adicionais](#additional-information) para saber mais sobre as configurações de chave do registro.</span><span class="sxs-lookup"><span data-stu-id="4773e-128">Read [Additional information](#additional-information) for information about Registry Key settings.</span></span>

<span data-ttu-id="4773e-129">Essa solução lado a lado é menos complexa e requer menos gerenciamento do que a solução detalhada descrita neste artigo.</span><span class="sxs-lookup"><span data-stu-id="4773e-129">This side-by-side solution is less complex and requires less management than the detailed solution described in this article.</span></span> <span data-ttu-id="4773e-130">No entanto, isso significa que você estará executando o canal Beta em vez do canal Estável.</span><span class="sxs-lookup"><span data-stu-id="4773e-130">However, this solution does mean that you'll be running the Beta Channel rather than the Stable Channel.</span></span>

## <span data-ttu-id="4773e-131">Experiência lado a lado com o canal estável do Microsoft Edge e a Versão Prévia do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="4773e-131">Side-by-side experience with Microsoft Edge Stable Channel and Microsoft Edge Legacy</span></span>

<span data-ttu-id="4773e-132">Instalar o canal Estável da próxima versão do Microsoft Edge no nível do sistema fará com que a versão atual (Versão Herdada do Microsoft Edge) seja ocultada.</span><span class="sxs-lookup"><span data-stu-id="4773e-132">Installing the Stable Channel of the next version of Microsoft Edge at the system-level will cause the current version (Microsoft Edge Legacy) to be hidden.</span></span> <span data-ttu-id="4773e-133">Para permitir que os usuários vejam as duas versões do Microsoft Edge lado a lado no Windows, você poderá habilitar essa experiência ao definir a política de grupo **Permitir experiência de navegador Lado a Lado do Microsoft Edge** como **Habilitada**.</span><span class="sxs-lookup"><span data-stu-id="4773e-133">If you want to let your users see both versions of Microsoft Edge side by side in Windows, you can enable this experience by setting the **Allow Microsoft Edge Side by Side browser experience** group policy to **Enabled**.</span></span>

<span data-ttu-id="4773e-134">Essa política de grupo é documentada [aqui](https://docs.microsoft.com/deployedge/microsoft-edge-update-policies#allowsxs)</span><span class="sxs-lookup"><span data-stu-id="4773e-134">This group policy is documented [here](https://docs.microsoft.com/deployedge/microsoft-edge-update-policies#allowsxs)</span></span>

### <span data-ttu-id="4773e-135">Para configurar a política de experiência do navegador lado a lado:</span><span class="sxs-lookup"><span data-stu-id="4773e-135">To set up the side-by-side browser experience policy:</span></span>

1. <span data-ttu-id="4773e-136">Instalar as definições de política do [Microsoft Edge for Business](https://www.microsoft.com/edge/business/download).</span><span class="sxs-lookup"><span data-stu-id="4773e-136">Install the Policy Definitions from [Microsoft Edge for Business](https://www.microsoft.com/edge/business/download).</span></span>

   - <span data-ttu-id="4773e-137">Escolha o CANAL/BUILD e a plataforma que você deseja usar e, em seguida, clique em OBTER ARQUIVOS DE POLÍTICA.</span><span class="sxs-lookup"><span data-stu-id="4773e-137">Pick the CHANNEL/BUILD and PLATFORM you want to use, and then click GET POLICY FILES.</span></span>
   - <span data-ttu-id="4773e-138">Extraia o arquivo compactados.</span><span class="sxs-lookup"><span data-stu-id="4773e-138">Extract the zipped files.</span></span>
   - <span data-ttu-id="4773e-139">Copie msedge.admx e msedgeupdate.admx para o diretório `C:\Windows\PolicyDefinitions`.</span><span class="sxs-lookup"><span data-stu-id="4773e-139">Copy msedge.admx and msedgeupdate.admx to the `C:\Windows\PolicyDefinitions` directory.</span></span>
   - <span data-ttu-id="4773e-140">Copie msedge.adml e msedgeupdate.adml (do diretório de idioma/local apropriado) para o diretório `C:\Windows\PolicyDefinitions\[APPROPRIATE LANGUAGE/LOCALE]`.</span><span class="sxs-lookup"><span data-stu-id="4773e-140">Copy msedge.adml and msedgeupdate.adml (from the appropriate language/locale directory) to the `C:\Windows\PolicyDefinitions\[APPROPRIATE LANGUAGE/LOCALE]` directory.</span></span>

2. <span data-ttu-id="4773e-141">Abra o Editor de Política de Grupo (gpedit.msc).</span><span class="sxs-lookup"><span data-stu-id="4773e-141">Open the Group Policy Editor (gpedit.msc).</span></span>
3. <span data-ttu-id="4773e-142">Em **Configuração do Computador**, vá para *Modelos Administrativos>Microsoft Edge Update>Aplicativos*.</span><span class="sxs-lookup"><span data-stu-id="4773e-142">Under **Computer Configuration**, go to *Administrative Templates>Microsoft Edge Update>Applications*.</span></span>

    > [!NOTE]
    > <span data-ttu-id="4773e-143">Se você não vir \* Microsoft Edge Update\*, verifique se a etapa 1 foi concluída corretamente.</span><span class="sxs-lookup"><span data-stu-id="4773e-143">If you don't see the *Microsoft Edge Update* folder, verify that step 1 was completed correctly.</span></span>

4. <span data-ttu-id="4773e-144">Em **Aplicativos**, clique duas vezes em "Permitir a experiência de navegador Lado a Lado do Microsoft Edge".</span><span class="sxs-lookup"><span data-stu-id="4773e-144">Under **Applications**, double-click "Allow Microsoft Edge Side by Side browser experience".</span></span> <span data-ttu-id="4773e-145">Veja nossas [práticas recomendadas](#best-practice-guidance) antes de passar para a próxima etapa.</span><span class="sxs-lookup"><span data-stu-id="4773e-145">See our [best practice guidance](#best-practice-guidance) before continuing to the next step.</span></span>

    > [!NOTE]
    > <span data-ttu-id="4773e-146">Por padrão, essa política de grupo é definida como "Não configurada", o que resultará na Versão Herdada do Microsoft Edge sendo ocultada quando a nova versão do Microsoft Edge for instalada.</span><span class="sxs-lookup"><span data-stu-id="4773e-146">By default, this group policy is set to "Not configured", which results in Microsoft Edge Legacy being hidden when the new version of Microsoft Edge is installed.</span></span>

5. <span data-ttu-id="4773e-147">Selecione **Habilitado** e, em seguida, clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="4773e-147">Select **Enabled** and then click **OK**.</span></span>  

<span data-ttu-id="4773e-148">Definir essa política definirá a seguinte chave do Registro como '00000001':</span><span class="sxs-lookup"><span data-stu-id="4773e-148">Setting this policy will set the following Registry Key  to '00000001':</span></span>

- <span data-ttu-id="4773e-149">Chave:</span><span class="sxs-lookup"><span data-stu-id="4773e-149">Key:</span></span> `Computer\HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate`
- <span data-ttu-id="4773e-150">Nome do valor:</span><span class="sxs-lookup"><span data-stu-id="4773e-150">Value Name:</span></span> `Allowsxs`
- <span data-ttu-id="4773e-151">Tipo de valor:</span><span class="sxs-lookup"><span data-stu-id="4773e-151">Value Type:</span></span> `'REG_DWORD'`

#### <span data-ttu-id="4773e-152">Diretrizes de prática recomendada</span><span class="sxs-lookup"><span data-stu-id="4773e-152">Best practice guidance</span></span>

<span data-ttu-id="4773e-153">Para a melhor experiência, **Permitir experiência de navegador Lado a Lado do Microsoft Edge** deve ser habilitado antes que a nova versão do Microsoft Edge seja implantada nos dispositivos dos usuários.</span><span class="sxs-lookup"><span data-stu-id="4773e-153">For the best experience, the **Allow Microsoft Edge Side by Side browser experience** should be enabled before the new version of Microsoft Edge is deployed to your users' devices.</span></span>

<span data-ttu-id="4773e-154">Se a política de grupo for habilitada depois que o Microsoft Edge tiver sido implantado, haverá os seguintes efeitos colaterais e as ações necessárias:</span><span class="sxs-lookup"><span data-stu-id="4773e-154">If the group policy is enabled after Microsoft Edge is deployed, there are the following side effects and required actions:</span></span>

1. <span data-ttu-id="4773e-155">**Permitir experiência de navegador Lado a Lado do Microsoft Edge** não entrará em vigor até o instalador da nova versão do Microsoft Edge ser executado novamente.</span><span class="sxs-lookup"><span data-stu-id="4773e-155">**Allow Microsoft Edge Side by Side browser experience** won't take effect until after the installer for the new version of Microsoft Edge is run again.</span></span>

   > [!NOTE]
   > <span data-ttu-id="4773e-156">O instalador pode ser executado direta ou automaticamente quando a nova versão do Microsoft Edge for atualizada.</span><span class="sxs-lookup"><span data-stu-id="4773e-156">The installer can be run directly or automatically when the new version of Microsoft Edge updates.</span></span>

2. <span data-ttu-id="4773e-157">A Versão Herdada do Microsoft Edge precisará ser fixada novamente em Iniciar ou na Barra de Tarefas porque o marcador será migrado quando a nova versão do Microsoft Edge for implantada.</span><span class="sxs-lookup"><span data-stu-id="4773e-157">Microsoft Edge Legacy will need to be re-pinned to Start or the Taskbar because the pin is migrated when the new version of Microsoft Edge is deployed.</span></span>
3. <span data-ttu-id="4773e-158">Os sites fixados em Iniciar ou na Barra de Tarefas para a Versão Herdada do Microsoft Edge serão migrados para a nova versão do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="4773e-158">Sites that were pinned to Start or the Taskbar for Microsoft Edge Legacy will be migrated to the new version of Microsoft Edge.</span></span>

## <span data-ttu-id="4773e-159">Informações adicionais</span><span class="sxs-lookup"><span data-stu-id="4773e-159">Additional information</span></span>

<span data-ttu-id="4773e-160">Depois que os sistemas forem totalmente atualizados e o canal Estável da próxima versão do Microsoft Edge for instalado, a seguinte chave do Registro e o valor serão definidos:</span><span class="sxs-lookup"><span data-stu-id="4773e-160">After the systems are fully updated and the Stable channel of the next version of Microsoft Edge is installed, the following registry key and value is set:</span></span>

- <span data-ttu-id="4773e-161">Chave:</span><span class="sxs-lookup"><span data-stu-id="4773e-161">Key:</span></span> `Computer\HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\EdgeUpdate\ClientState\{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}`
- <span data-ttu-id="4773e-162">Valor da chave:</span><span class="sxs-lookup"><span data-stu-id="4773e-162">Key value:</span></span> `BrowserReplacement`

  > [!IMPORTANT]
  > <span data-ttu-id="4773e-163">Essa chave é substituída sempre que o canal Estável do Microsoft Edge é atualizado.</span><span class="sxs-lookup"><span data-stu-id="4773e-163">This key is over-written every time the Microsoft Edge Stable channel is updated.</span></span> <span data-ttu-id="4773e-164">Como uma prática recomendada, recomendamos que você NÃO exclua essa chave para permitir que os usuários acessem as duas versões do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="4773e-164">As a best practice, we recommend that you DO NOT delete this key to allow users to access both versions of Microsoft Edge.</span></span>

## <span data-ttu-id="4773e-165">Consulte também</span><span class="sxs-lookup"><span data-stu-id="4773e-165">See also</span></span>

- [<span data-ttu-id="4773e-166">Página de aterrissagem do Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="4773e-166">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="4773e-167">Atualizações do Windows para dar suporte ao Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="4773e-167">Windows updates to support Microsoft Edge</span></span>](microsoft-edge-sysupdate-windows-updates.md)
