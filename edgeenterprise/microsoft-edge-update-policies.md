---
title: Documentação da política do Microsoft Edge Update
ms.author: stmoody
author: dan-wesley
manager: tahills
ms.date: 06/29/2021
audience: ITPro
ms.topic: reference
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
ms.custom: ''
description: Documentação para todas as políticas compatíveis com o Microsoft Edge Update
ms.openlocfilehash: a9808981acad544042c6e0ccb59ff755a670c848
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/09/2021
ms.locfileid: "11642317"
---
# <a name="microsoft-edge---update-policies"></a><span data-ttu-id="e54e3-103">Microsoft Edge - Políticas de atualização</span><span class="sxs-lookup"><span data-stu-id="e54e3-103">Microsoft Edge - Update policies</span></span>

<span data-ttu-id="e54e3-104">A versão mais recente do Microsoft Edge inclui as seguintes políticas que você pode usar para controlar como e quando o Microsoft Edge é atualizado.</span><span class="sxs-lookup"><span data-stu-id="e54e3-104">The latest version of Microsoft Edge includes the following policies that you can use to control how and when Microsoft Edge is updated.</span></span>

<span data-ttu-id="e54e3-105">Para obter informações sobre outras políticas disponíveis no Microsoft Edge, confira [Referência de política do navegador Microsoft Edge](microsoft-edge-policies.md)</span><span class="sxs-lookup"><span data-stu-id="e54e3-105">For information about other policies available in Microsoft Edge, check out [Microsoft Edge browser policy reference](microsoft-edge-policies.md)</span></span>
> [!NOTE]
> <span data-ttu-id="e54e3-106">Este artigo se aplica ao Microsoft Edge versão 77 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="e54e3-106">This article applies to Microsoft Edge version 77 or later.</span></span>
## <a name="available-policies"></a><span data-ttu-id="e54e3-107">Políticas disponíveis</span><span class="sxs-lookup"><span data-stu-id="e54e3-107">Available policies</span></span>
<span data-ttu-id="e54e3-108">Estas tabelas listam todas as políticas de grupo relacionadas a atualizações disponíveis nesta versão do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="e54e3-108">These tables lists all of the update-related group policies available in this release of Microsoft Edge.</span></span> <span data-ttu-id="e54e3-109">Use os links na tabela a seguir para obter mais detalhes sobre políticas específicas.</span><span class="sxs-lookup"><span data-stu-id="e54e3-109">Use the links in the table to get more details about specific policies.</span></span>

<span data-ttu-id="e54e3-110">|&nbsp;|&nbsp;| |**-**|-| |**[Aplicativos](#applications)**|[Preferências](#preferences)| |**[Servidor Proxy](#proxy-server)**|[Microsoft Edge WebView](#microsoft-edge-webview)|</span><span class="sxs-lookup"><span data-stu-id="e54e3-110">|&nbsp;|&nbsp;| |**-**|-| |**[Applications](#applications)**|[Preferences](#preferences)| |**[Proxy Server](#proxy-server)**|[Microsoft Edge WebView](#microsoft-edge-webview)|</span></span>
### [<a name="applications"></a><span data-ttu-id="e54e3-111">Aplicativos</span><span class="sxs-lookup"><span data-stu-id="e54e3-111">Applications</span></span>](#applications-policies)
|<span data-ttu-id="e54e3-112">Nome da política</span><span class="sxs-lookup"><span data-stu-id="e54e3-112">Policy Name</span></span>|<span data-ttu-id="e54e3-113">Legenda</span><span class="sxs-lookup"><span data-stu-id="e54e3-113">Caption</span></span>|
|-|-|
|[<span data-ttu-id="e54e3-114">InstallDefault</span><span class="sxs-lookup"><span data-stu-id="e54e3-114">InstallDefault</span></span>](#installdefault)|<span data-ttu-id="e54e3-115">Permitir a instalação padrão</span><span class="sxs-lookup"><span data-stu-id="e54e3-115">Allow installation default</span></span>|
|[<span data-ttu-id="e54e3-116">UpdateDefault</span><span class="sxs-lookup"><span data-stu-id="e54e3-116">UpdateDefault</span></span>](#updatedefault)|<span data-ttu-id="e54e3-117">Atualizar o padrão de substituição de política</span><span class="sxs-lookup"><span data-stu-id="e54e3-117">Update policy override default</span></span>|
|[<span data-ttu-id="e54e3-118">Install</span><span class="sxs-lookup"><span data-stu-id="e54e3-118">Install</span></span>](#install)|<span data-ttu-id="e54e3-119">Permitir a instalação (por canal)</span><span class="sxs-lookup"><span data-stu-id="e54e3-119">Allow installation (per channel)</span></span>|
|[<span data-ttu-id="e54e3-120">Update</span><span class="sxs-lookup"><span data-stu-id="e54e3-120">Update</span></span>](#update)|<span data-ttu-id="e54e3-121">Atualizar a substituição de política (por canal)</span><span class="sxs-lookup"><span data-stu-id="e54e3-121">Update policy override (per channel)</span></span>|
|[<span data-ttu-id="e54e3-122">Allowsxs</span><span class="sxs-lookup"><span data-stu-id="e54e3-122">Allowsxs</span></span>](#allowsxs)|<span data-ttu-id="e54e3-123">Permitir a experiência de navegador Lado a Lado do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="e54e3-123">Allow Microsoft Edge Side by Side browser experience</span></span>|
|[<span data-ttu-id="e54e3-124">CreateDesktopShortcutDefault</span><span class="sxs-lookup"><span data-stu-id="e54e3-124">CreateDesktopShortcutDefault</span></span>](#createdesktopshortcutdefault)|<span data-ttu-id="e54e3-125">Impedir a criação de Atalho da Área de Trabalho com a instalação padrão</span><span class="sxs-lookup"><span data-stu-id="e54e3-125">Prevent Desktop Shortcut creation upon install default</span></span>|
|[<span data-ttu-id="e54e3-126">CreateDesktopShortcut</span><span class="sxs-lookup"><span data-stu-id="e54e3-126">CreateDesktopShortcut</span></span>](#createdesktopshortcut)|<span data-ttu-id="e54e3-127">Impedir a criação de Atalho da Área de Trabalho com a instalação (por canal)</span><span class="sxs-lookup"><span data-stu-id="e54e3-127">Prevent Desktop Shortcut creation upon install (per channel)</span></span>|
|[<span data-ttu-id="e54e3-128">RollbackToTargetVersion</span><span class="sxs-lookup"><span data-stu-id="e54e3-128">RollbackToTargetVersion</span></span>](#rollbacktotargetversion)|<span data-ttu-id="e54e3-129">Reverter para a Versão de Destino (por canal)</span><span class="sxs-lookup"><span data-stu-id="e54e3-129">Rollback to Target version (per channel)</span></span>|
|[<span data-ttu-id="e54e3-130">TargetVersionPrefix</span><span class="sxs-lookup"><span data-stu-id="e54e3-130">TargetVersionPrefix</span></span>](#targetversionprefix)|<span data-ttu-id="e54e3-131">Substituir versão de destino (por canal)</span><span class="sxs-lookup"><span data-stu-id="e54e3-131">Target version override (per channel)</span></span>|

### [<a name="preferences"></a><span data-ttu-id="e54e3-132">Preferências</span><span class="sxs-lookup"><span data-stu-id="e54e3-132">Preferences</span></span>](#preferences-policies)
|<span data-ttu-id="e54e3-133">Nome da política</span><span class="sxs-lookup"><span data-stu-id="e54e3-133">Policy Name</span></span>|<span data-ttu-id="e54e3-134">Legenda</span><span class="sxs-lookup"><span data-stu-id="e54e3-134">Caption</span></span>|
|-|-|
|[<span data-ttu-id="e54e3-135">AutoUpdateCheckPeriodMinutes</span><span class="sxs-lookup"><span data-stu-id="e54e3-135">AutoUpdateCheckPeriodMinutes</span></span>](#autoupdatecheckperiodminutes)|<span data-ttu-id="e54e3-136">Atualizar automaticamente a substituição do período de verificação</span><span class="sxs-lookup"><span data-stu-id="e54e3-136">Auto-update check period override</span></span>|
|[<span data-ttu-id="e54e3-137">UpdatesSuppressed</span><span class="sxs-lookup"><span data-stu-id="e54e3-137">UpdatesSuppressed</span></span>](#updatessuppressed)|<span data-ttu-id="e54e3-138">O período em cada dia para suprimir a verificação de atualização automática</span><span class="sxs-lookup"><span data-stu-id="e54e3-138">Time period in each day to suppress auto-update check</span></span>|

### [<a name="proxy-server"></a><span data-ttu-id="e54e3-139">Servidor proxy</span><span class="sxs-lookup"><span data-stu-id="e54e3-139">Proxy Server</span></span>](#proxy-server-policies)
|<span data-ttu-id="e54e3-140">Nome da política</span><span class="sxs-lookup"><span data-stu-id="e54e3-140">Policy Name</span></span>|<span data-ttu-id="e54e3-141">Legenda</span><span class="sxs-lookup"><span data-stu-id="e54e3-141">Caption</span></span>|
|-|-|
|[<span data-ttu-id="e54e3-142">ProxyMode</span><span class="sxs-lookup"><span data-stu-id="e54e3-142">ProxyMode</span></span>](#proxymode)|<span data-ttu-id="e54e3-143">Escolher como especificar as configurações do servidor proxy</span><span class="sxs-lookup"><span data-stu-id="e54e3-143">Choose how to specify proxy server settings</span></span>|
|[<span data-ttu-id="e54e3-144">ProxyPacUrl</span><span class="sxs-lookup"><span data-stu-id="e54e3-144">ProxyPacUrl</span></span>](#proxypacurl)|<span data-ttu-id="e54e3-145">A URL para um arquivo .pac de proxy</span><span class="sxs-lookup"><span data-stu-id="e54e3-145">URL to a proxy .pac file</span></span>|
|[<span data-ttu-id="e54e3-146">ProxyServer</span><span class="sxs-lookup"><span data-stu-id="e54e3-146">ProxyServer</span></span>](#proxyserver)|<span data-ttu-id="e54e3-147">Endereço ou URL do servidor proxy</span><span class="sxs-lookup"><span data-stu-id="e54e3-147">Address or URL of proxy server</span></span>|

### [<a name="microsoft-edge-webview"></a><span data-ttu-id="e54e3-148">Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="e54e3-148">Microsoft Edge WebView</span></span>](#microsoft-edge-webview-policies)
|<span data-ttu-id="e54e3-149">Nome da política</span><span class="sxs-lookup"><span data-stu-id="e54e3-149">Policy Name</span></span>|<span data-ttu-id="e54e3-150">Legenda</span><span class="sxs-lookup"><span data-stu-id="e54e3-150">Caption</span></span>|
|-|-|
|[<span data-ttu-id="e54e3-151">Instalar</span><span class="sxs-lookup"><span data-stu-id="e54e3-151">Install</span></span>](#install-webview)|<span data-ttu-id="e54e3-152">Permitir instalação</span><span class="sxs-lookup"><span data-stu-id="e54e3-152">Allow installation</span></span>|
|[<span data-ttu-id="e54e3-153">Atualização</span><span class="sxs-lookup"><span data-stu-id="e54e3-153">Update</span></span>](#update-webview)|<span data-ttu-id="e54e3-154">Atualizar a substituição de política</span><span class="sxs-lookup"><span data-stu-id="e54e3-154">Update policy override</span></span>|

## <a name="applications-policies"></a><span data-ttu-id="e54e3-155">Políticas de aplicativos</span><span class="sxs-lookup"><span data-stu-id="e54e3-155">Applications policies</span></span>

[<span data-ttu-id="e54e3-156">Voltar ao início</span><span class="sxs-lookup"><span data-stu-id="e54e3-156">Back to top</span></span>](#microsoft-edge---update-policies)
### <a name="installdefault"></a><span data-ttu-id="e54e3-157">InstallDefault</span><span class="sxs-lookup"><span data-stu-id="e54e3-157">InstallDefault</span></span>
#### <a name="allow-installation-default"></a><span data-ttu-id="e54e3-158">Permitir a instalação padrão</span><span class="sxs-lookup"><span data-stu-id="e54e3-158">Allow installation default</span></span>
><span data-ttu-id="e54e3-159">Microsoft Edge Update 1.2.145.5 e posterior</span><span class="sxs-lookup"><span data-stu-id="e54e3-159">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <a name="description"></a><span data-ttu-id="e54e3-160">Descrição</span><span class="sxs-lookup"><span data-stu-id="e54e3-160">Description</span></span>
<span data-ttu-id="e54e3-161">Você pode especificar o comportamento padrão de todos os canais para permitir ou bloquear o Microsoft Edge em dispositivos associados ao domínio.</span><span class="sxs-lookup"><span data-stu-id="e54e3-161">You can specify the default behavior of all channels to allow or block Microsoft Edge on domain-joined devices.</span></span>

<span data-ttu-id="e54e3-162">Você pode substituir esta política para canais individuais habilitando a política '[Permitir instalação](#install)' para canais específicos.</span><span class="sxs-lookup"><span data-stu-id="e54e3-162">You can override this policy for individual channels by enabling the '[Allow installation](#install)' policy for specific channels.</span></span>

<span data-ttu-id="e54e3-163">Se você desabilitar esta política, a instalação do Microsoft Edge será bloqueada.</span><span class="sxs-lookup"><span data-stu-id="e54e3-163">If you disable this policy, the installation of Microsoft Edge is blocked.</span></span> <span data-ttu-id="e54e3-164">Isso só afeta a instalação do software Microsoft Edge quando a '[Permitir instalação](#install)' está definida como Não configurada.</span><span class="sxs-lookup"><span data-stu-id="e54e3-164">This only affects the installation of Microsoft Edge software when the '[Allow installation](#install)' policy is set to Not Configured.</span></span>

<span data-ttu-id="e54e3-165">Esta política não impede a execução do Microsoft Edge Update, nem impede que os usuários instalem o software do Microsoft Edge por outros métodos.</span><span class="sxs-lookup"><span data-stu-id="e54e3-165">This policy doesn't prevent Microsoft Edge Update from running or prevent users from installing Microsoft Edge software using other methods.</span></span>

<span data-ttu-id="e54e3-166">Esta política está disponível apenas em instâncias do Windows que fazem parte de um domínio Microsoft® Active Directory®.</span><span class="sxs-lookup"><span data-stu-id="e54e3-166">This policy is available only on Windows instances that are joined to a Microsoft® Active Directory® domain.</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="e54e3-167">Informações e configurações do Windows</span><span class="sxs-lookup"><span data-stu-id="e54e3-167">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="e54e3-168">Informações da Política de Grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="e54e3-168">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="e54e3-169">Nome exclusivo da Política de Grupo: InstallDefault</span><span class="sxs-lookup"><span data-stu-id="e54e3-169">GP unique name: InstallDefault</span></span>
- <span data-ttu-id="e54e3-170">Nome da Política de Grupo: Permitir a instalação padrão</span><span class="sxs-lookup"><span data-stu-id="e54e3-170">GP name: Allow installation default</span></span>
- <span data-ttu-id="e54e3-171">Caminho da Política Padrão: Modelos Administrativos/Microsoft Edge Update/Aplicativos</span><span class="sxs-lookup"><span data-stu-id="e54e3-171">GP path: Administrative Templates/Microsoft Edge Update/Applications</span></span>
- <span data-ttu-id="e54e3-172">Nome do arquivo GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="e54e3-172">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="e54e3-173">Configurações de registro do Windows</span><span class="sxs-lookup"><span data-stu-id="e54e3-173">Windows Registry Settings</span></span>
- <span data-ttu-id="e54e3-174">Caminho: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="e54e3-174">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="e54e3-175">Nome do valor: InstallDefault</span><span class="sxs-lookup"><span data-stu-id="e54e3-175">Value Name: InstallDefault</span></span>
- <span data-ttu-id="e54e3-176">Tipo de valor: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="e54e3-176">Value Type: REG_DWORD</span></span>
##### <a name="example-value"></a><span data-ttu-id="e54e3-177">Valor de exemplo:</span><span class="sxs-lookup"><span data-stu-id="e54e3-177">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="e54e3-178">Voltar ao início</span><span class="sxs-lookup"><span data-stu-id="e54e3-178">Back to top</span></span>](#microsoft-edge---update-policies)


### <a name="updatedefault"></a><span data-ttu-id="e54e3-179">UpdateDefault</span><span class="sxs-lookup"><span data-stu-id="e54e3-179">UpdateDefault</span></span>
#### <a name="update-policy-override-default"></a><span data-ttu-id="e54e3-180">Atualizar o padrão de substituição de política</span><span class="sxs-lookup"><span data-stu-id="e54e3-180">Update policy override default</span></span>
><span data-ttu-id="e54e3-181">Microsoft Edge Update 1.2.145.5 e posterior</span><span class="sxs-lookup"><span data-stu-id="e54e3-181">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <a name="description"></a><span data-ttu-id="e54e3-182">Descrição</span><span class="sxs-lookup"><span data-stu-id="e54e3-182">Description</span></span>
<span data-ttu-id="e54e3-183">Permite especificar o comportamento padrão para todos os canais referentes à maneira como o Microsoft Edge Update trata as atualizações disponíveis para o Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="e54e3-183">Lets you specify the default behavior for all channels concerning the way Microsoft Edge Update handles available updates for Microsoft Edge.</span></span> <span data-ttu-id="e54e3-184">Pode ser substituído para canais individuais ao especificar a política '[Atualizar a substituição de política](#update)' para esses canais específicos.</span><span class="sxs-lookup"><span data-stu-id="e54e3-184">Can be overridden for individual channels by specifying the '[Update policy override](#update)' policy for those specific channels.</span></span>

  <span data-ttu-id="e54e3-185">Se você habilitar essa política, o Microsoft Edge Update tratará as atualizações do Microsoft Edge de acordo com as seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="e54e3-185">If you enable this policy, Microsoft Edge Update handles Microsoft Edge updates according to how you configure the following options:</span></span>
   - <span data-ttu-id="e54e3-186">Sempre permitir atualizações: as atualizações sempre serão aplicadas quando forem encontradas por uma verificação de atualização periódica ou por uma verificação de atualização manual.</span><span class="sxs-lookup"><span data-stu-id="e54e3-186">Always allow updates: Updates are always applied when found, either by periodic update check or by a manual update check.</span></span>
   - <span data-ttu-id="e54e3-187">Somente atualizações silenciosas automáticas: as atualizações serão aplicadas somente quando forem encontradas pela verificação de atualização periódica.</span><span class="sxs-lookup"><span data-stu-id="e54e3-187">Automatic silent updates only: Updates are applied only when they're found by the periodic update check.</span></span>
   - <span data-ttu-id="e54e3-188">Somente atualizações manuais: as atualizações serão aplicadas somente quando o usuário executar uma verificação de atualização manual.</span><span class="sxs-lookup"><span data-stu-id="e54e3-188">Manual updates only: Updates are applied only when the user runs a manual update check.</span></span>
   - <span data-ttu-id="e54e3-189">Atualizações desabilitadas: as atualizações nunca serão aplicadas.</span><span class="sxs-lookup"><span data-stu-id="e54e3-189">Updates disabled: Updates are never applied.</span></span>

  <span data-ttu-id="e54e3-190">Se você selecionar atualizações manuais, verifique periodicamente se há atualizações usando o mecanismo de atualizações manuais do aplicativo, se disponível.</span><span class="sxs-lookup"><span data-stu-id="e54e3-190">If you select manual updates, make sure you periodically check for updates by using the app's manual update mechanism, if available.</span></span> <span data-ttu-id="e54e3-191">Se você desabilitar as atualizações, verifique periodicamente se há atualizações e as distribua aos usuários.</span><span class="sxs-lookup"><span data-stu-id="e54e3-191">If you disable updates, periodically check for updates, and distribute them to users.</span></span>

  <span data-ttu-id="e54e3-192">Se você não habilitar e configurar essa política, o Microsoft Edge Update trata as atualizações disponíveis conforme especificado pela política '[Atualizar a substituição de política"](#update)'.</span><span class="sxs-lookup"><span data-stu-id="e54e3-192">If you don't enable and configure this policy, Microsoft Edge Update handles available updates as specified by the '[Update policy override](#update)' policy.</span></span>

  <span data-ttu-id="e54e3-193">Esta política está disponível apenas em instâncias do Windows que fazem parte de um domínio Microsoft® Active Directory®.</span><span class="sxs-lookup"><span data-stu-id="e54e3-193">This policy is available only on Windows instances that are joined to a Microsoft® Active Directory® domain.</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="e54e3-194">Informações e configurações do Windows</span><span class="sxs-lookup"><span data-stu-id="e54e3-194">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="e54e3-195">Informações da Política de Grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="e54e3-195">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="e54e3-196">Nome exclusivo da Política de Grupo: UpdateDefault</span><span class="sxs-lookup"><span data-stu-id="e54e3-196">GP unique name: UpdateDefault</span></span>
- <span data-ttu-id="e54e3-197">Nome da Política de Grupo: Atualizar o padrão de substituição de política</span><span class="sxs-lookup"><span data-stu-id="e54e3-197">GP name: Update policy override default</span></span>
- <span data-ttu-id="e54e3-198">Caminho da Política Padrão: Modelos Administrativos/Microsoft Edge Update/Aplicativos</span><span class="sxs-lookup"><span data-stu-id="e54e3-198">GP path: Administrative Templates/Microsoft Edge Update/Applications</span></span>
- <span data-ttu-id="e54e3-199">Nome do arquivo GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="e54e3-199">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="e54e3-200">Configurações de registro do Windows</span><span class="sxs-lookup"><span data-stu-id="e54e3-200">Windows Registry Settings</span></span>
- <span data-ttu-id="e54e3-201">Caminho: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="e54e3-201">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="e54e3-202">Nome do valor: UpdateDefault</span><span class="sxs-lookup"><span data-stu-id="e54e3-202">Value Name: UpdateDefault</span></span>
- <span data-ttu-id="e54e3-203">Tipo de valor: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="e54e3-203">Value Type: REG_DWORD</span></span>
##### <a name="example-value"></a><span data-ttu-id="e54e3-204">Valor de exemplo:</span><span class="sxs-lookup"><span data-stu-id="e54e3-204">Example value:</span></span>
```
0x00000003
```
[<span data-ttu-id="e54e3-205">Voltar ao início</span><span class="sxs-lookup"><span data-stu-id="e54e3-205">Back to top</span></span>](#microsoft-edge---update-policies)


### <a name="install"></a><span data-ttu-id="e54e3-206">Install</span><span class="sxs-lookup"><span data-stu-id="e54e3-206">Install</span></span>
#### <a name="allow-installation"></a><span data-ttu-id="e54e3-207">Permitir instalação</span><span class="sxs-lookup"><span data-stu-id="e54e3-207">Allow installation</span></span>
><span data-ttu-id="e54e3-208">Microsoft Edge Update 1.2.145.5 e posterior</span><span class="sxs-lookup"><span data-stu-id="e54e3-208">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <a name="description"></a><span data-ttu-id="e54e3-209">Descrição</span><span class="sxs-lookup"><span data-stu-id="e54e3-209">Description</span></span>
<span data-ttu-id="e54e3-210">Especifica se um canal do Microsoft Edge pode ser instalado em dispositivos ingressados ​​no domínio.</span><span class="sxs-lookup"><span data-stu-id="e54e3-210">Specifies whether a Microsoft Edge channel can be installed on domain-joined devices.</span></span>

  <span data-ttu-id="e54e3-211">Se você habilitar esta política para um canal, o Microsoft Edge não terá sua instalação bloqueada.</span><span class="sxs-lookup"><span data-stu-id="e54e3-211">If you enable this policy for a channel, Microsoft Edge will not be blocked from installation.</span></span>

  <span data-ttu-id="e54e3-212">Se você desabilitar esta política para um canal, o Microsoft Edge será bloqueado para instalação.</span><span class="sxs-lookup"><span data-stu-id="e54e3-212">If you disable this policy for a channel, Microsoft Edge will be blocked from installation.</span></span>

  <span data-ttu-id="e54e3-213">Se você não configurar esta política para um canal, a configuração da política '[Permitir instalação padrão](#installdefault)' determina se os usuários podem instalar esse canal do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="e54e3-213">If you don't configure this policy for a channel, the '[Allow installation default](#installdefault)' policy configuration determines whether users can install that channel of Microsoft Edge.</span></span>

  <span data-ttu-id="e54e3-214">Esta política está disponível apenas em instâncias do Windows que fazem parte de um domínio Microsoft® Active Directory®.</span><span class="sxs-lookup"><span data-stu-id="e54e3-214">This policy is available only on Windows instances that are joined to a Microsoft® Active Directory® domain.</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="e54e3-215">Informações e configurações do Windows</span><span class="sxs-lookup"><span data-stu-id="e54e3-215">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="e54e3-216">Informações da Política de Grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="e54e3-216">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="e54e3-217">Nome exclusivo da Política de Grupo: Install</span><span class="sxs-lookup"><span data-stu-id="e54e3-217">GP unique name: Install</span></span>
- <span data-ttu-id="e54e3-218">Nome da Política de Grupo: Permitir instalação</span><span class="sxs-lookup"><span data-stu-id="e54e3-218">GP name: Allow installation</span></span>
- <span data-ttu-id="e54e3-219">Caminho da Política de Grupo:</span><span class="sxs-lookup"><span data-stu-id="e54e3-219">GP path:</span></span> 
  - <span data-ttu-id="e54e3-220">Modelos Administrativos/Microsoft Edge Update/Aplicativos/Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="e54e3-220">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span></span>
  - <span data-ttu-id="e54e3-221">Modelos Administrativos/Microsoft Edge Update/Aplicativos/Microsoft Edge Beta</span><span class="sxs-lookup"><span data-stu-id="e54e3-221">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span></span>
  - <span data-ttu-id="e54e3-222">Modelos Administrativos/Microsoft Edge Update/Aplicativos/Microsoft Edge Canary</span><span class="sxs-lookup"><span data-stu-id="e54e3-222">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span></span>
  - <span data-ttu-id="e54e3-223">Modelos Administrativos/Microsoft Edge Update/Aplicativos/Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="e54e3-223">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span></span>
- <span data-ttu-id="e54e3-224">Nome do arquivo GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="e54e3-224">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="e54e3-225">Configurações de registro do Windows</span><span class="sxs-lookup"><span data-stu-id="e54e3-225">Windows Registry Settings</span></span>
- <span data-ttu-id="e54e3-226">Caminho: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="e54e3-226">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="e54e3-227">Nome do valor:</span><span class="sxs-lookup"><span data-stu-id="e54e3-227">Value Name:</span></span> 
  - <span data-ttu-id="e54e3-228">(Estável): Install{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span><span class="sxs-lookup"><span data-stu-id="e54e3-228">(Stable): Install{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span></span>
  - <span data-ttu-id="e54e3-229">(Beta): Install{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span><span class="sxs-lookup"><span data-stu-id="e54e3-229">(Beta): Install{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span></span>
  - <span data-ttu-id="e54e3-230">(Canary): Install{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span><span class="sxs-lookup"><span data-stu-id="e54e3-230">(Canary): Install{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span></span>
  - <span data-ttu-id="e54e3-231">(Dev): Install{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span><span class="sxs-lookup"><span data-stu-id="e54e3-231">(Dev): Install{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span></span>
- <span data-ttu-id="e54e3-232">Tipo de valor: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="e54e3-232">Value Type: REG_DWORD</span></span>
##### <a name="example-value"></a><span data-ttu-id="e54e3-233">Valor de exemplo:</span><span class="sxs-lookup"><span data-stu-id="e54e3-233">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="e54e3-234">Voltar ao início</span><span class="sxs-lookup"><span data-stu-id="e54e3-234">Back to top</span></span>](#microsoft-edge---update-policies)


### <a name="update"></a><span data-ttu-id="e54e3-235">Update</span><span class="sxs-lookup"><span data-stu-id="e54e3-235">Update</span></span>
#### <a name="update-policy-override"></a><span data-ttu-id="e54e3-236">Atualizar a substituição de política</span><span class="sxs-lookup"><span data-stu-id="e54e3-236">Update policy override</span></span>
><span data-ttu-id="e54e3-237">Microsoft Edge Update 1.2.145.5 e posterior</span><span class="sxs-lookup"><span data-stu-id="e54e3-237">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <a name="description"></a><span data-ttu-id="e54e3-238">Descrição</span><span class="sxs-lookup"><span data-stu-id="e54e3-238">Description</span></span>
<span data-ttu-id="e54e3-239">Especifica como o Microsoft Edge Update trata as atualizações disponíveis do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="e54e3-239">Specifies how Microsoft Edge Update handles available updates from Microsoft Edge.</span></span>

<span data-ttu-id="e54e3-240">Se você habilitar essa política, o Microsoft Edge Update tratará as atualizações do Microsoft Edge de acordo com as seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="e54e3-240">If you enable this policy, Microsoft Edge Update handles Microsoft Edge updates according to how you configure the following options:</span></span>
  - <span data-ttu-id="e54e3-241">Sempre permitir atualizações: as atualizações sempre serão aplicadas quando forem encontradas por uma verificação de atualização periódica ou por uma verificação de atualização manual.</span><span class="sxs-lookup"><span data-stu-id="e54e3-241">Always allow updates: Updates are always applied when found, either by periodic update check or by a manual update check.</span></span>
  - <span data-ttu-id="e54e3-242">Somente atualizações silenciosas automáticas: as atualizações serão aplicadas somente quando forem encontradas pela verificação de atualização periódica.</span><span class="sxs-lookup"><span data-stu-id="e54e3-242">Automatic silent updates only: Updates are applied only when they're found by the periodic update check.</span></span>
  - <span data-ttu-id="e54e3-243">Somente atualizações manuais: as atualizações serão aplicadas somente quando o usuário executar uma verificação de atualização manual.</span><span class="sxs-lookup"><span data-stu-id="e54e3-243">Manual updates only: Updates are applied only when the user runs a manual update check.</span></span> <span data-ttu-id="e54e3-244">(Nem todos os aplicativos fornecem uma interface para essa opção.)</span><span class="sxs-lookup"><span data-stu-id="e54e3-244">(Not all apps provide an interface for this option.)</span></span>
  - <span data-ttu-id="e54e3-245">Atualizações desabilitadas: as atualizações nunca serão aplicadas.</span><span class="sxs-lookup"><span data-stu-id="e54e3-245">Updates disabled: Updates are never applied.</span></span>

<span data-ttu-id="e54e3-246">Se você selecionar atualizações manuais, verifique periodicamente se há atualizações usando o mecanismo de atualizações manuais do aplicativo, se disponível.</span><span class="sxs-lookup"><span data-stu-id="e54e3-246">If you select manual updates, make sure you periodically check for updates by using the app's manual update mechanism, if available.</span></span> <span data-ttu-id="e54e3-247">Se você desabilitar as atualizações, verifique periodicamente se há atualizações e as distribua aos usuários.</span><span class="sxs-lookup"><span data-stu-id="e54e3-247">If you disable updates, periodically check for updates, and distribute them to users.</span></span>

<span data-ttu-id="e54e3-248">Se você não habilitar e configurar essa política, o Microsoft Edge Update tratará as atualizações disponíveis conforme especificado pela política '[Atualizar a substituição de política padrão](#updatedefault)'.</span><span class="sxs-lookup"><span data-stu-id="e54e3-248">If you don't enable and configure this policy, Microsoft Edge Update handles available updates as specified by the '[Update policy override default](#updatedefault)' policy.</span></span>

<span data-ttu-id="e54e3-249">Consulte [https://go.microsoft.com/fwlink/?linkid=2136406](https://go.microsoft.com/fwlink/?linkid=2136406) para mais informações.</span><span class="sxs-lookup"><span data-stu-id="e54e3-249">See [https://go.microsoft.com/fwlink/?linkid=2136406](https://go.microsoft.com/fwlink/?linkid=2136406) for more information.</span></span>

<span data-ttu-id="e54e3-250">Esta política está disponível apenas em instâncias do Windows que fazem parte de um domínio Microsoft® Active Directory®.</span><span class="sxs-lookup"><span data-stu-id="e54e3-250">This policy is available only on Windows instances that are joined to a Microsoft® Active Directory® domain.</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="e54e3-251">Informações e configurações do Windows</span><span class="sxs-lookup"><span data-stu-id="e54e3-251">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="e54e3-252">Informações da Política de Grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="e54e3-252">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="e54e3-253">Nome exclusivo da Política de Grupo: Update</span><span class="sxs-lookup"><span data-stu-id="e54e3-253">GP unique name: Update</span></span>
- <span data-ttu-id="e54e3-254">Nome da Política de Grupo: Atualizar a substituição de política</span><span class="sxs-lookup"><span data-stu-id="e54e3-254">GP name: Update policy override</span></span>
- <span data-ttu-id="e54e3-255">Caminho da Política de Grupo:</span><span class="sxs-lookup"><span data-stu-id="e54e3-255">GP path:</span></span> 
  - <span data-ttu-id="e54e3-256">Modelos Administrativos/Microsoft Edge Update/Aplicativos/Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="e54e3-256">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span></span>
  - <span data-ttu-id="e54e3-257">Modelos Administrativos/Microsoft Edge Update/Aplicativos/Microsoft Edge Beta</span><span class="sxs-lookup"><span data-stu-id="e54e3-257">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span></span>
  - <span data-ttu-id="e54e3-258">Modelos Administrativos/Microsoft Edge Update/Aplicativos/Microsoft Edge Canary</span><span class="sxs-lookup"><span data-stu-id="e54e3-258">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span></span>
  - <span data-ttu-id="e54e3-259">Modelos Administrativos/Microsoft Edge Update/Aplicativos/Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="e54e3-259">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span></span>
- <span data-ttu-id="e54e3-260">Nome do arquivo GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="e54e3-260">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="e54e3-261">Configurações de registro do Windows</span><span class="sxs-lookup"><span data-stu-id="e54e3-261">Windows Registry Settings</span></span>
- <span data-ttu-id="e54e3-262">Caminho: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="e54e3-262">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="e54e3-263">Nome do valor:</span><span class="sxs-lookup"><span data-stu-id="e54e3-263">Value Name:</span></span> 
  - <span data-ttu-id="e54e3-264">(Estável): Update{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span><span class="sxs-lookup"><span data-stu-id="e54e3-264">(Stable): Update{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span></span>
  - <span data-ttu-id="e54e3-265">(Beta): Update{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span><span class="sxs-lookup"><span data-stu-id="e54e3-265">(Beta): Update{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span></span>
  - <span data-ttu-id="e54e3-266">(Canary): Update{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span><span class="sxs-lookup"><span data-stu-id="e54e3-266">(Canary): Update{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span></span>
  - <span data-ttu-id="e54e3-267">(Dev): Update{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span><span class="sxs-lookup"><span data-stu-id="e54e3-267">(Dev): Update{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span></span>
- <span data-ttu-id="e54e3-268">Tipo de valor: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="e54e3-268">Value Type: REG_DWORD</span></span>
##### <a name="example-value"></a><span data-ttu-id="e54e3-269">Valor de exemplo:</span><span class="sxs-lookup"><span data-stu-id="e54e3-269">Example value:</span></span>
```
always allow updates 0x00000001
Automatic silent updates only 0x00000003
manual updates only 0x00000002
updates disabled 0x00000000
```
[<span data-ttu-id="e54e3-270">Voltar ao início</span><span class="sxs-lookup"><span data-stu-id="e54e3-270">Back to top</span></span>](#microsoft-edge---update-policies)


### <a name="allowsxs"></a><span data-ttu-id="e54e3-271">Allowsxs</span><span class="sxs-lookup"><span data-stu-id="e54e3-271">Allowsxs</span></span>
#### <a name="allow-microsoft-edge-side-by-side-browser-experience"></a><span data-ttu-id="e54e3-272">Permitir a experiência de navegador Lado a Lado do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="e54e3-272">Allow Microsoft Edge Side by Side browser experience</span></span>
><span data-ttu-id="e54e3-273">Microsoft Edge Update 1.2.145.5 e posterior</span><span class="sxs-lookup"><span data-stu-id="e54e3-273">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <a name="description"></a><span data-ttu-id="e54e3-274">Description</span><span class="sxs-lookup"><span data-stu-id="e54e3-274">Description</span></span>
<span data-ttu-id="e54e3-275">Essa política permite que um usuário execute o Microsoft Edge (Edge HTML) e o Microsoft Edge (baseado no Chromium) lado a lado.</span><span class="sxs-lookup"><span data-stu-id="e54e3-275">This policy lets a user run Microsoft Edge (Edge HTML) and Microsoft Edge (Chromium-based) side-by-side.</span></span>

<span data-ttu-id="e54e3-276">Se essa política for definida como "Não configurada", o Microsoft Edge (baseado no Chromium) substituirá o Microsoft Edge (HTML do Edge) depois que o canal Estável do Microsoft Edge (baseado no Chromium) e as atualizações de segurança de novembro de 2019 forem instalados.</span><span class="sxs-lookup"><span data-stu-id="e54e3-276">If this policy is set to “Not configured”, Microsoft Edge (Chromium-based) will replace Microsoft Edge (Edge HTML) after the Microsoft Edge (Chromium-based) stable channel and the November 2019 security updates are installed.</span></span>  <span data-ttu-id="e54e3-277">Esse comportamento é igual à configuração "Desabilitada".</span><span class="sxs-lookup"><span data-stu-id="e54e3-277">This is the same behavior as the “Disabled” setting.</span></span>

<span data-ttu-id="e54e3-278">A configuração "Desabilitada" bloqueia uma experiência lado a lado, e o Microsoft Edge (baseado no Chromium) substituirá o Microsoft Edge (HTML do Edge) depois que o canal Estável do Microsoft Edge (baseado no Chromium) e as atualizações de segurança de novembro de 2019 forem instalados.</span><span class="sxs-lookup"><span data-stu-id="e54e3-278">The “Disabled” setting blocks a side-by-side experience and Microsoft Edge (Chromium-based) will replace Microsoft Edge (Edge HTML) after the Microsoft Edge (Chromium-based) stable channel and the November 2019 security updates are installed.</span></span>  <span data-ttu-id="e54e3-279">Esse comportamento é igual à configuração "Não configurada".</span><span class="sxs-lookup"><span data-stu-id="e54e3-279">This is the same behavior as the “Not Configured” setting.</span></span>

<span data-ttu-id="e54e3-280">Quando essa política for "Habilitada", o Microsoft Edge (baseado no Chromium) e o Microsoft Edge (Edge HTML) poderão ser executados lado a lado depois que o Microsoft Edge (baseado no Chromium) for instalado.</span><span class="sxs-lookup"><span data-stu-id="e54e3-280">When this policy is “Enabled”, Microsoft Edge (Chromium-based) and Microsoft Edge (Edge HTML) can run side-by-side after Microsoft Edge (Chromium-based) is installed.</span></span>

<span data-ttu-id="e54e3-281">Para que essa política de grupo entre em vigor, ela deve ser configurada antes da instalação automática do Microsoft Edge (baseado no Chromium) pelo Windows Update.</span><span class="sxs-lookup"><span data-stu-id="e54e3-281">For this group policy to take affect, it must be configured before the automatic install of Microsoft Edge (Chromium-based) by Windows Update.</span></span> <span data-ttu-id="e54e3-282">Observação: um usuário pode bloquear a atualização automática do Microsoft Edge (baseado no Chromium) usando o kit de ferramentas do bloqueador do Microsoft Edge (baseado no Chromium).</span><span class="sxs-lookup"><span data-stu-id="e54e3-282">Note: A user can block the automatic update of Microsoft Edge (Chromium-based) by using the Microsoft Edge (Chromium-based) Blocker Toolkit.</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="e54e3-283">Informações e configurações do Windows</span><span class="sxs-lookup"><span data-stu-id="e54e3-283">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="e54e3-284">Informações da Política de Grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="e54e3-284">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="e54e3-285">Nome exclusivo da Política de Grupo: Allowsxs</span><span class="sxs-lookup"><span data-stu-id="e54e3-285">GP unique name: Allowsxs</span></span>
- <span data-ttu-id="e54e3-286">Nome da Política de Grupo: Permitir a experiência de navegador Lado a Lado do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="e54e3-286">GP name: Allow Microsoft Edge Side by Side browser experience</span></span>
- <span data-ttu-id="e54e3-287">Caminho da Política Padrão: Modelos Administrativos/Microsoft Edge Update/Aplicativos</span><span class="sxs-lookup"><span data-stu-id="e54e3-287">GP path: Administrative Templates/Microsoft Edge Update/Applications</span></span>
- <span data-ttu-id="e54e3-288">Nome do arquivo GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="e54e3-288">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="e54e3-289">Configurações de registro do Windows</span><span class="sxs-lookup"><span data-stu-id="e54e3-289">Windows Registry Settings</span></span>
- <span data-ttu-id="e54e3-290">Caminho: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="e54e3-290">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="e54e3-291">Nome do valor: Allowsxs</span><span class="sxs-lookup"><span data-stu-id="e54e3-291">Value Name: Allowsxs</span></span>
- <span data-ttu-id="e54e3-292">Tipo de valor: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="e54e3-292">Value Type: REG_DWORD</span></span>
##### <a name="example-value"></a><span data-ttu-id="e54e3-293">Valor de exemplo:</span><span class="sxs-lookup"><span data-stu-id="e54e3-293">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="e54e3-294">Voltar ao início</span><span class="sxs-lookup"><span data-stu-id="e54e3-294">Back to top</span></span>](#microsoft-edge---update-policies)


### <a name="createdesktopshortcutdefault"></a><span data-ttu-id="e54e3-295">CreateDesktopShortcutDefault</span><span class="sxs-lookup"><span data-stu-id="e54e3-295">CreateDesktopShortcutDefault</span></span>
#### <a name="prevent-desktop-shortcut-creation-upon-install-default"></a><span data-ttu-id="e54e3-296">Impedir a criação de Atalho da Área de Trabalho com a instalação padrão</span><span class="sxs-lookup"><span data-stu-id="e54e3-296">Prevent Desktop Shortcut creation upon install default</span></span>
><span data-ttu-id="e54e3-297">Microsoft Edge Update 1.3.128.0 e posterior</span><span class="sxs-lookup"><span data-stu-id="e54e3-297">Microsoft Edge Update 1.3.128.0 and later</span></span>

#### <a name="description"></a><span data-ttu-id="e54e3-298">Descrição</span><span class="sxs-lookup"><span data-stu-id="e54e3-298">Description</span></span>
<span data-ttu-id="e54e3-299">Permite especificar o comportamento padrão de todos os canais para criar um atalho da área de trabalho quando o Microsoft Edge for instalado.</span><span class="sxs-lookup"><span data-stu-id="e54e3-299">Lets you specify the default behavior for all channels for creating a desktop shortcut when Microsoft Edge is installed.</span></span>

  <span data-ttu-id="e54e3-300">Se você habilitar esta política, um atalho da área de trabalho será criado quando o Microsoft Edge for instalado.</span><span class="sxs-lookup"><span data-stu-id="e54e3-300">If you enable this policy a desktop shortcut is created when Microsoft Edge is installed.</span></span>
<span data-ttu-id="e54e3-301">Se você desabilitar esta política, nenhum atalho da área de trabalho será criado quando o Microsoft Edge for instalado.</span><span class="sxs-lookup"><span data-stu-id="e54e3-301">If you disable this policy, no desktop shortcut will be created when Microsoft Edge is installed.</span></span>
<span data-ttu-id="e54e3-302">Se você não configurar esta política, um atalho da área de trabalho para o Microsoft Edge será criado durante a instalação.</span><span class="sxs-lookup"><span data-stu-id="e54e3-302">If you don’t configure this policy a desktop shortcut to Microsoft Edge will be created during installation.</span></span>
<span data-ttu-id="e54e3-303">Se o Microsoft Edge já estiver instalado, esta política não terá efeito.</span><span class="sxs-lookup"><span data-stu-id="e54e3-303">If Microsoft Edge is already installed, this policy will have no effect.</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="e54e3-304">Informações e configurações do Windows</span><span class="sxs-lookup"><span data-stu-id="e54e3-304">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="e54e3-305">Informações da Política de Grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="e54e3-305">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="e54e3-306">Nome exclusivo da Política de Grupo: CreateDesktopShortcutDefault</span><span class="sxs-lookup"><span data-stu-id="e54e3-306">GP unique name: CreateDesktopShortcutDefault</span></span>
- <span data-ttu-id="e54e3-307">Nome da Política de Grupo: Impedir a criação de Atalho da Área de Trabalho com a instalação padrão</span><span class="sxs-lookup"><span data-stu-id="e54e3-307">GP name: Prevent Desktop Shortcut creation upon install default</span></span>
- <span data-ttu-id="e54e3-308">Caminho da Política Padrão: Modelos Administrativos/Microsoft Edge Update/Aplicativos</span><span class="sxs-lookup"><span data-stu-id="e54e3-308">GP path: Administrative Templates/Microsoft Edge Update/Applications</span></span>
- <span data-ttu-id="e54e3-309">Nome do arquivo GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="e54e3-309">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="e54e3-310">Configurações de registro do Windows</span><span class="sxs-lookup"><span data-stu-id="e54e3-310">Windows Registry Settings</span></span>
- <span data-ttu-id="e54e3-311">Caminho: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="e54e3-311">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="e54e3-312">Nome do Valor: CreateDesktopShortcutDefault</span><span class="sxs-lookup"><span data-stu-id="e54e3-312">Value Name: CreateDesktopShortcutDefault</span></span>
- <span data-ttu-id="e54e3-313">Tipo de valor: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="e54e3-313">Value Type: REG_DWORD</span></span>
##### <a name="example-value"></a><span data-ttu-id="e54e3-314">Valor de exemplo:</span><span class="sxs-lookup"><span data-stu-id="e54e3-314">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="e54e3-315">Voltar ao início</span><span class="sxs-lookup"><span data-stu-id="e54e3-315">Back to top</span></span>](#microsoft-edge---update-policies)


### <a name="createdesktopshortcut"></a><span data-ttu-id="e54e3-316">CreateDesktopShortcut</span><span class="sxs-lookup"><span data-stu-id="e54e3-316">CreateDesktopShortcut</span></span>
#### <a name="prevent-desktop-shortcut-creation-upon-install"></a><span data-ttu-id="e54e3-317">Impedir a criação de Atalho da Área de Trabalho com a instalação</span><span class="sxs-lookup"><span data-stu-id="e54e3-317">Prevent Desktop Shortcut creation upon install</span></span>
><span data-ttu-id="e54e3-318">Microsoft Edge Update 1.3.128.0 e posterior</span><span class="sxs-lookup"><span data-stu-id="e54e3-318">Microsoft Edge Update 1.3.128.0 and later</span></span>

#### <a name="description"></a><span data-ttu-id="e54e3-319">Descrição</span><span class="sxs-lookup"><span data-stu-id="e54e3-319">Description</span></span>
<span data-ttu-id="e54e3-320">Se você habilitar esta política, um atalho da área de trabalho será criado quando o Microsoft Edge for instalado.</span><span class="sxs-lookup"><span data-stu-id="e54e3-320">If you enable this policy a desktop shortcut is created when Microsoft Edge is installed.</span></span>
<span data-ttu-id="e54e3-321">Se você desabilitar esta política, nenhum atalho da área de trabalho será criado quando o Microsoft Edge for instalado.</span><span class="sxs-lookup"><span data-stu-id="e54e3-321">If you disable this policy, no desktop shortcut will be created when Microsoft Edge is installed.</span></span>
<span data-ttu-id="e54e3-322">Se você não configurar esta política, um atalho da área de trabalho para o Microsoft Edge será criado durante a instalação.</span><span class="sxs-lookup"><span data-stu-id="e54e3-322">If you don’t configure this policy a desktop shortcut to Microsoft Edge will be created during installation.</span></span>
<span data-ttu-id="e54e3-323">Se o Microsoft Edge já estiver instalado, esta política não terá efeito.</span><span class="sxs-lookup"><span data-stu-id="e54e3-323">If Microsoft Edge is already installed, this policy will have no effect.</span></span>

  <span data-ttu-id="e54e3-324">Se você não configurar esta política para um canal, a configuração de política padrão '[Evitar a criação de um Atalho no Desktop ao instalar](#createdesktopshortcutdefault)' determinará a criação de um atalho quando o Microsoft Edge for instalado.</span><span class="sxs-lookup"><span data-stu-id="e54e3-324">If you don't configure this policy for a channel, the '[Prevent Desktop Shortcut creation upon install default](#createdesktopshortcutdefault)' policy configuration determines shortcut creation when Microsoft Edge is installed.</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="e54e3-325">Informações e configurações do Windows</span><span class="sxs-lookup"><span data-stu-id="e54e3-325">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="e54e3-326">Informações da Política de Grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="e54e3-326">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="e54e3-327">Nome exclusivo da Política de Grupo: CreateDesktopShortcut</span><span class="sxs-lookup"><span data-stu-id="e54e3-327">GP unique name: CreateDesktopShortcut</span></span>
- <span data-ttu-id="e54e3-328">Nome da GP: Impedir a criação de Atalho da Área de Trabalho com a instalação</span><span class="sxs-lookup"><span data-stu-id="e54e3-328">GP name: Prevent Desktop Shortcut creation upon install</span></span>
- <span data-ttu-id="e54e3-329">Caminho da Política de Grupo:</span><span class="sxs-lookup"><span data-stu-id="e54e3-329">GP path:</span></span> 
  - <span data-ttu-id="e54e3-330">Modelos Administrativos/Microsoft Edge Update/Aplicativos/Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="e54e3-330">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span></span>
  - <span data-ttu-id="e54e3-331">Modelos Administrativos/Microsoft Edge Update/Aplicativos/Microsoft Edge Beta</span><span class="sxs-lookup"><span data-stu-id="e54e3-331">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span></span>
  - <span data-ttu-id="e54e3-332">Modelos Administrativos/Microsoft Edge Update/Aplicativos/Microsoft Edge Canary</span><span class="sxs-lookup"><span data-stu-id="e54e3-332">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span></span>
  - <span data-ttu-id="e54e3-333">Modelos Administrativos/Microsoft Edge Update/Aplicativos/Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="e54e3-333">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span></span>
- <span data-ttu-id="e54e3-334">Nome do arquivo GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="e54e3-334">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="e54e3-335">Configurações de registro do Windows</span><span class="sxs-lookup"><span data-stu-id="e54e3-335">Windows Registry Settings</span></span>
- <span data-ttu-id="e54e3-336">Caminho: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="e54e3-336">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="e54e3-337">Nome do valor:</span><span class="sxs-lookup"><span data-stu-id="e54e3-337">Value Name:</span></span> 
  - <span data-ttu-id="e54e3-338">(Estável): CreateDesktopShortcut{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span><span class="sxs-lookup"><span data-stu-id="e54e3-338">(Stable): CreateDesktopShortcut{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span></span>
  - <span data-ttu-id="e54e3-339">(Beta): CreateDesktopShortcut{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span><span class="sxs-lookup"><span data-stu-id="e54e3-339">(Beta): CreateDesktopShortcut{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span></span>
  - <span data-ttu-id="e54e3-340">(Canary): CreateDesktopShortcut{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span><span class="sxs-lookup"><span data-stu-id="e54e3-340">(Canary): CreateDesktopShortcut{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span></span>
  - <span data-ttu-id="e54e3-341">(Dev): CreateDesktopShortcut{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span><span class="sxs-lookup"><span data-stu-id="e54e3-341">(Dev): CreateDesktopShortcut{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span></span>
- <span data-ttu-id="e54e3-342">Tipo de valor: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="e54e3-342">Value Type: REG_DWORD</span></span>
##### <a name="example-value"></a><span data-ttu-id="e54e3-343">Valor de exemplo:</span><span class="sxs-lookup"><span data-stu-id="e54e3-343">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="e54e3-344">Voltar ao início</span><span class="sxs-lookup"><span data-stu-id="e54e3-344">Back to top</span></span>](#microsoft-edge---update-policies)


### <a name="rollbacktotargetversion"></a><span data-ttu-id="e54e3-345">RollbackToTargetVersion</span><span class="sxs-lookup"><span data-stu-id="e54e3-345">RollbackToTargetVersion</span></span>
#### <a name="rollback-to-target-version"></a><span data-ttu-id="e54e3-346">Reverter para a Versão de Destino</span><span class="sxs-lookup"><span data-stu-id="e54e3-346">Rollback to Target version</span></span>
><span data-ttu-id="e54e3-347">Microsoft Edge Update 1.3.133.3 e posterior</span><span class="sxs-lookup"><span data-stu-id="e54e3-347">Microsoft Edge Update 1.3.133.3 and later</span></span>

#### <a name="description"></a><span data-ttu-id="e54e3-348">Descrição</span><span class="sxs-lookup"><span data-stu-id="e54e3-348">Description</span></span>
<span data-ttu-id="e54e3-349">Especifica que o Microsoft Edge Update deve reverter as instalações do Microsoft Edge para a versão indicada em '[Substituição da versão de destino](#targetversionprefix)'.</span><span class="sxs-lookup"><span data-stu-id="e54e3-349">Specifies that Microsoft Edge Update should rollback installations of Microsoft Edge to the version indicated in '[Target version override](#targetversionprefix)'.</span></span>

<span data-ttu-id="e54e3-350">Esta política não tem efeito a menos que '[Substituição da versão de destino](#targetversionprefix)' seja definida e '[Substituição da política de atualização](#update)' seja definida como um dos estados ATIVADO (Sempre permitir atualizações, Somente atualizações automáticas silenciosas, Somente atualizações manuais).</span><span class="sxs-lookup"><span data-stu-id="e54e3-350">This policy has no effect unless '[Target version override](#targetversionprefix)' is set and '[Update policy override](#update)' is set to one of the ON states (Always allow updates, Automatic silent updates only, Manual updates only).</span></span>

<span data-ttu-id="e54e3-351">Se você desabilitar esta política ou não configurá-la, as instalações que possuem uma versão superior à especificada pela '[Substituição da versão de destino](#targetversionprefix)' serão deixadas como estão.</span><span class="sxs-lookup"><span data-stu-id="e54e3-351">If you disable this policy or don't configure it, installs that have a version higher than that specified by '[Target version override](#targetversionprefix)' will be left as-is.</span></span>

<span data-ttu-id="e54e3-352">Se você habilitar esta política, as instalações que possuem uma versão atual superior à especificada pela '[Substituição da versão de destino](#targetversionprefix)' serão desatualizadas para a versão de destino.</span><span class="sxs-lookup"><span data-stu-id="e54e3-352">If you enable this policy, installs that have a current version higher than specified by the '[Target version override](#targetversionprefix)' will be downgraded to the target version.</span></span>

<span data-ttu-id="e54e3-353">Recomendamos que os usuários instalem a versão mais recente do navegador Microsoft Edge para garantir a proteção pelas atualizações de segurança mais recentes.</span><span class="sxs-lookup"><span data-stu-id="e54e3-353">We recommend that users install the latest version of the Microsoft Edge browser to ensure protection by the latest security updates.</span></span> <span data-ttu-id="e54e3-354">Reverter para uma versão anterior corre o perigo de se expor aos problemas de segurança conhecidos.</span><span class="sxs-lookup"><span data-stu-id="e54e3-354">Rollback to an earlier version risks exposure to known security issues.</span></span> <span data-ttu-id="e54e3-355">Esta política deve ser usada como uma correção temporária para resolver problemas em uma atualização do navegador Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="e54e3-355">This policy is meant to be used as a temporary fix to address issues in a Microsoft Edge browser update.</span></span>

<span data-ttu-id="e54e3-356">Antes de reverter temporariamente a versão do seu navegador, recomendamos que você ative a Sincronização ([https://go.microsoft.com/fwlink/?linkid=2133032](https://go.microsoft.com/fwlink/?linkid=2133032)) para todos os usuários em sua organização.</span><span class="sxs-lookup"><span data-stu-id="e54e3-356">Before temporarily rolling back your browser version, we recommend that you turn on Sync ([https://go.microsoft.com/fwlink/?linkid=2133032](https://go.microsoft.com/fwlink/?linkid=2133032)) for all users in your organization.</span></span> <span data-ttu-id="e54e3-357">Se você não ativar a Sincronização, existe o risco de perda permanente de dados de navegação.</span><span class="sxs-lookup"><span data-stu-id="e54e3-357">If you don't turn on Sync, there is a risk of permanent browsing data loss.</span></span> <span data-ttu-id="e54e3-358">Use esta política por sua conta e risco.</span><span class="sxs-lookup"><span data-stu-id="e54e3-358">Use this policy at your own risk.</span></span>

<span data-ttu-id="e54e3-359">Nota: Todas as versões disponíveis para reversão podem ser vistas aqui [https://aka.ms/EdgeEnterprise](https://aka.ms/EdgeEnterprise).</span><span class="sxs-lookup"><span data-stu-id="e54e3-359">Note: All versions available for rollback can be viewed here [https://aka.ms/EdgeEnterprise](https://aka.ms/EdgeEnterprise).</span></span>

<span data-ttu-id="e54e3-360">Esta política se aplica ao Microsoft Edge versão 86 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="e54e3-360">This policy applies to Microsoft Edge version 86 or later.</span></span>

<span data-ttu-id="e54e3-361">Consulte [https://go.microsoft.com/fwlink/?linkid=2133918](https://go.microsoft.com/fwlink/?linkid=2133918) para mais informações.</span><span class="sxs-lookup"><span data-stu-id="e54e3-361">See [https://go.microsoft.com/fwlink/?linkid=2133918](https://go.microsoft.com/fwlink/?linkid=2133918) for more information.</span></span>

<span data-ttu-id="e54e3-362">Esta política está disponível apenas em instâncias do Windows que fazem parte de um domínio Microsoft® Active Directory®.</span><span class="sxs-lookup"><span data-stu-id="e54e3-362">This policy is available only on Windows instances that are joined to a Microsoft® Active Directory® domain.</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="e54e3-363">Informações e configurações do Windows</span><span class="sxs-lookup"><span data-stu-id="e54e3-363">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="e54e3-364">Informações da Política de Grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="e54e3-364">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="e54e3-365">Nome exclusivo da GP: RollbackToTargetVersion</span><span class="sxs-lookup"><span data-stu-id="e54e3-365">GP unique name: RollbackToTargetVersion</span></span>
- <span data-ttu-id="e54e3-366">Nome da GP: Reverter para a Versão de Destino</span><span class="sxs-lookup"><span data-stu-id="e54e3-366">GP name: Rollback to Target version</span></span>
- <span data-ttu-id="e54e3-367">Caminho da Política de Grupo:</span><span class="sxs-lookup"><span data-stu-id="e54e3-367">GP path:</span></span> 
  - <span data-ttu-id="e54e3-368">Modelos Administrativos/Microsoft Edge Update/Aplicativos/Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="e54e3-368">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span></span>
  - <span data-ttu-id="e54e3-369">Modelos Administrativos/Microsoft Edge Update/Aplicativos/Microsoft Edge Beta</span><span class="sxs-lookup"><span data-stu-id="e54e3-369">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span></span>
  - <span data-ttu-id="e54e3-370">Modelos Administrativos/Microsoft Edge Update/Aplicativos/Microsoft Edge Canary</span><span class="sxs-lookup"><span data-stu-id="e54e3-370">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span></span>
  - <span data-ttu-id="e54e3-371">Modelos Administrativos/Microsoft Edge Update/Aplicativos/Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="e54e3-371">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span></span>
- <span data-ttu-id="e54e3-372">Nome do arquivo GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="e54e3-372">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="e54e3-373">Configurações de registro do Windows</span><span class="sxs-lookup"><span data-stu-id="e54e3-373">Windows Registry Settings</span></span>
- <span data-ttu-id="e54e3-374">Caminho: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="e54e3-374">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="e54e3-375">Nome do valor:</span><span class="sxs-lookup"><span data-stu-id="e54e3-375">Value Name:</span></span> 
  - <span data-ttu-id="e54e3-376">(Estável): RollbackToTargetVersion{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span><span class="sxs-lookup"><span data-stu-id="e54e3-376">(Stable): RollbackToTargetVersion{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span></span>
  - <span data-ttu-id="e54e3-377">(Beta): RollbackToTargetVersion{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span><span class="sxs-lookup"><span data-stu-id="e54e3-377">(Beta): RollbackToTargetVersion{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span></span>
  - <span data-ttu-id="e54e3-378">(Canário): RollbackToTargetVersion{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span><span class="sxs-lookup"><span data-stu-id="e54e3-378">(Canary): RollbackToTargetVersion{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span></span>
  - <span data-ttu-id="e54e3-379">(Dev): RollbackToTargetVersion{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span><span class="sxs-lookup"><span data-stu-id="e54e3-379">(Dev): RollbackToTargetVersion{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span></span>
- <span data-ttu-id="e54e3-380">Tipo de valor: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="e54e3-380">Value Type: REG_DWORD</span></span>
##### <a name="example-value"></a><span data-ttu-id="e54e3-381">Valor de exemplo:</span><span class="sxs-lookup"><span data-stu-id="e54e3-381">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="e54e3-382">Voltar ao início</span><span class="sxs-lookup"><span data-stu-id="e54e3-382">Back to top</span></span>](#microsoft-edge---update-policies)


### <a name="targetversionprefix"></a><span data-ttu-id="e54e3-383">TargetVersionPrefix</span><span class="sxs-lookup"><span data-stu-id="e54e3-383">TargetVersionPrefix</span></span>
#### <a name="target-version-override"></a><span data-ttu-id="e54e3-384">Substituir versão de destino</span><span class="sxs-lookup"><span data-stu-id="e54e3-384">Target version override</span></span>
><span data-ttu-id="e54e3-385">Microsoft Edge Update 1.3.119.43 e posterior</span><span class="sxs-lookup"><span data-stu-id="e54e3-385">Microsoft Edge Update 1.3.119.43 and later</span></span>

#### <a name="description"></a><span data-ttu-id="e54e3-386">Descrição</span><span class="sxs-lookup"><span data-stu-id="e54e3-386">Description</span></span>
<span data-ttu-id="e54e3-387">Quando esta política estiver habilitada e a atualização automática estiver habilitada, o Microsoft Edge será atualizado para a versão especificada por esse valor de política.</span><span class="sxs-lookup"><span data-stu-id="e54e3-387">When this policy is enabled, and auto-update is enabled, Microsoft Edge will be updated to the version specified by this policy value.</span></span>

<span data-ttu-id="e54e3-388">O valor da política deve ser uma versão do Microsoft Edge específica, por exemplo, 83.0.499.12.</span><span class="sxs-lookup"><span data-stu-id="e54e3-388">The policy value must be a specific Microsoft Edge version, e.g. 83.0.499.12.</span></span>

<span data-ttu-id="e54e3-389">Se um dispositivo tiver uma versão mais recente do Microsoft Edge do que o valor especificado, a versão mais recente do Microsoft Edge será mantida e ele não será revertido para a versão especificada.</span><span class="sxs-lookup"><span data-stu-id="e54e3-389">If a device has newer version of Microsoft Edge than the value specified, Microsoft Edge will remain on the newer version and not downgrade to the specified version.</span></span>

<span data-ttu-id="e54e3-390">Se a versão especificada não existir ou estiver formatada inadequadamente, o Microsoft Edge permanecerá na versão atual e não será atualizado para versões futuras automaticamente.</span><span class="sxs-lookup"><span data-stu-id="e54e3-390">If the specified version does not exist, or is improperly formatted, then Microsoft Edge will remain on its current version and not update to future versions automatically.</span></span>

<span data-ttu-id="e54e3-391">Consulte [https://go.microsoft.com/fwlink/?linkid=2136707](https://go.microsoft.com/fwlink/?linkid=2136707) para mais informações.</span><span class="sxs-lookup"><span data-stu-id="e54e3-391">See [https://go.microsoft.com/fwlink/?linkid=2136707](https://go.microsoft.com/fwlink/?linkid=2136707) for more information.</span></span>

<span data-ttu-id="e54e3-392">Esta política está disponível apenas em instâncias do Windows que fazem parte de um domínio Microsoft® Active Directory®.</span><span class="sxs-lookup"><span data-stu-id="e54e3-392">This policy is available only on Windows instances that are joined to a Microsoft® Active Directory® domain.</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="e54e3-393">Informações e configurações do Windows</span><span class="sxs-lookup"><span data-stu-id="e54e3-393">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="e54e3-394">Informações da Política de Grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="e54e3-394">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="e54e3-395">Nome exclusivo da Política de Grupo: TargetVersionPrefix</span><span class="sxs-lookup"><span data-stu-id="e54e3-395">GP unique name: TargetVersionPrefix</span></span>
- <span data-ttu-id="e54e3-396">Nome da Política de Grupo: Substituir versão de destino</span><span class="sxs-lookup"><span data-stu-id="e54e3-396">GP name: Target version override</span></span>
- <span data-ttu-id="e54e3-397">Caminho da Política de Grupo:</span><span class="sxs-lookup"><span data-stu-id="e54e3-397">GP path:</span></span> 
  - <span data-ttu-id="e54e3-398">Modelos Administrativos/Microsoft Edge Update/Aplicativos/Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="e54e3-398">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span></span>
  - <span data-ttu-id="e54e3-399">Modelos Administrativos/Microsoft Edge Update/Aplicativos/Microsoft Edge Beta</span><span class="sxs-lookup"><span data-stu-id="e54e3-399">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span></span>
  - <span data-ttu-id="e54e3-400">Modelos Administrativos/Microsoft Edge Update/Aplicativos/Microsoft Edge Canary</span><span class="sxs-lookup"><span data-stu-id="e54e3-400">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span></span>
  - <span data-ttu-id="e54e3-401">Modelos Administrativos/Microsoft Edge Update/Aplicativos/Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="e54e3-401">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span></span>
- <span data-ttu-id="e54e3-402">Nome do arquivo GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="e54e3-402">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="e54e3-403">Configurações de registro do Windows</span><span class="sxs-lookup"><span data-stu-id="e54e3-403">Windows Registry Settings</span></span>
- <span data-ttu-id="e54e3-404">Caminho: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="e54e3-404">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="e54e3-405">Nome do valor:</span><span class="sxs-lookup"><span data-stu-id="e54e3-405">Value Name:</span></span> 
  - <span data-ttu-id="e54e3-406">(Estável): TargetVersionPrefix {56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span><span class="sxs-lookup"><span data-stu-id="e54e3-406">(Stable): TargetVersionPrefix{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span></span>
  - <span data-ttu-id="e54e3-407">(Beta): TargetVersionPrefix {2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span><span class="sxs-lookup"><span data-stu-id="e54e3-407">(Beta): TargetVersionPrefix{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span></span>
  - <span data-ttu-id="e54e3-408">(Canary): TargetVersionPrefix {65C35B14-6C1D-4122-AC46-7148CC9D6497}</span><span class="sxs-lookup"><span data-stu-id="e54e3-408">(Canary): TargetVersionPrefix{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span></span>
  - <span data-ttu-id="e54e3-409">(Dev): TargetVersionPrefix {0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span><span class="sxs-lookup"><span data-stu-id="e54e3-409">(Dev): TargetVersionPrefix{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span></span>
- <span data-ttu-id="e54e3-410">Tipo do valor: REG_SZ</span><span class="sxs-lookup"><span data-stu-id="e54e3-410">Value Type: REG_SZ</span></span>
##### <a name="example-value"></a><span data-ttu-id="e54e3-411">Valor de exemplo:</span><span class="sxs-lookup"><span data-stu-id="e54e3-411">Example value:</span></span>
```
83.0.499.12
```
[<span data-ttu-id="e54e3-412">Voltar ao início</span><span class="sxs-lookup"><span data-stu-id="e54e3-412">Back to top</span></span>](#microsoft-edge---update-policies)


## <a name="preferences-policies"></a><span data-ttu-id="e54e3-413">Políticas de preferências</span><span class="sxs-lookup"><span data-stu-id="e54e3-413">Preferences policies</span></span>

[<span data-ttu-id="e54e3-414">Voltar ao início</span><span class="sxs-lookup"><span data-stu-id="e54e3-414">Back to top</span></span>](#microsoft-edge---update-policies)
### <a name="autoupdatecheckperiodminutes"></a><span data-ttu-id="e54e3-415">AutoUpdateCheckPeriodMinutes</span><span class="sxs-lookup"><span data-stu-id="e54e3-415">AutoUpdateCheckPeriodMinutes</span></span>
#### <a name="auto-update-check-period-override"></a><span data-ttu-id="e54e3-416">Atualizar automaticamente a substituição do período de verificação</span><span class="sxs-lookup"><span data-stu-id="e54e3-416">Auto-update check period override</span></span>
><span data-ttu-id="e54e3-417">Microsoft Edge Update 1.2.145.5 e posterior</span><span class="sxs-lookup"><span data-stu-id="e54e3-417">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <a name="description"></a><span data-ttu-id="e54e3-418">Descrição</span><span class="sxs-lookup"><span data-stu-id="e54e3-418">Description</span></span>
<span data-ttu-id="e54e3-419">Se habilitada, essa política permite definir um valor para o número mínimo de minutos entre as verificações de atualização automática.</span><span class="sxs-lookup"><span data-stu-id="e54e3-419">If enabled, this policy lets you set a value for the minimum number of minutes between automatic update checks.</span></span> <span data-ttu-id="e54e3-420">Caso contrário, por padrão, a verificação de atualização automática verifica se há as atualizações a cada 10 horas.</span><span class="sxs-lookup"><span data-stu-id="e54e3-420">Otherwise, by default, auto-update checks for updates every 10 hours.</span></span>

  <span data-ttu-id="e54e3-421">Se você quiser desabilitar todas as verificações de atualização automática, defina o valor como 0 (não recomendado).</span><span class="sxs-lookup"><span data-stu-id="e54e3-421">If you want to disable all auto-update checks, set the value to 0 (not recommended).</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="e54e3-422">Informações e configurações do Windows</span><span class="sxs-lookup"><span data-stu-id="e54e3-422">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="e54e3-423">Informações da Política de Grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="e54e3-423">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="e54e3-424">Nome exclusivo da Política de Grupo: AutoUpdateCheckPeriodMinutes</span><span class="sxs-lookup"><span data-stu-id="e54e3-424">GP unique name: AutoUpdateCheckPeriodMinutes</span></span>
- <span data-ttu-id="e54e3-425">Nome da Política de Grupo: Atualizar automaticamente a substituição do período de verificação</span><span class="sxs-lookup"><span data-stu-id="e54e3-425">GP name: Auto-update check period override</span></span>
- <span data-ttu-id="e54e3-426">Caminho da Política de Grupo: Modelos Administrativos/Microsoft Edge Update/Preferências</span><span class="sxs-lookup"><span data-stu-id="e54e3-426">GP path: Administrative Templates/Microsoft Edge Update/Preferences</span></span>
- <span data-ttu-id="e54e3-427">Nome do arquivo GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="e54e3-427">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="e54e3-428">Configurações de registro do Windows</span><span class="sxs-lookup"><span data-stu-id="e54e3-428">Windows Registry Settings</span></span>
- <span data-ttu-id="e54e3-429">Caminho: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="e54e3-429">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="e54e3-430">Nome do valor: AutoUpdateCheckPeriodMinutes</span><span class="sxs-lookup"><span data-stu-id="e54e3-430">Value Name: AutoUpdateCheckPeriodMinutes</span></span>
- <span data-ttu-id="e54e3-431">Tipo de valor: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="e54e3-431">Value Type: REG_DWORD</span></span>
##### <a name="example-value"></a><span data-ttu-id="e54e3-432">Valor de exemplo:</span><span class="sxs-lookup"><span data-stu-id="e54e3-432">Example value:</span></span>
```
0x00000578
```
[<span data-ttu-id="e54e3-433">Voltar ao início</span><span class="sxs-lookup"><span data-stu-id="e54e3-433">Back to top</span></span>](#microsoft-edge---update-policies)


### <a name="updatessuppressed"></a><span data-ttu-id="e54e3-434">UpdatesSuppressed</span><span class="sxs-lookup"><span data-stu-id="e54e3-434">UpdatesSuppressed</span></span>
#### <a name="time-period-in-each-day-to-suppress-auto-update-check"></a><span data-ttu-id="e54e3-435">Período em cada dia para suprimir a verificação de atualização automática</span><span class="sxs-lookup"><span data-stu-id="e54e3-435">Time period in each day to suppress auto-update check</span></span>
><span data-ttu-id="e54e3-436">Microsoft Edge Update 1.3.33.5 e posterior</span><span class="sxs-lookup"><span data-stu-id="e54e3-436">Microsoft Edge Update 1.3.33.5 and later</span></span>

#### <a name="description"></a><span data-ttu-id="e54e3-437">Descrição</span><span class="sxs-lookup"><span data-stu-id="e54e3-437">Description</span></span>
<span data-ttu-id="e54e3-438">Se você habilitar essa política, as verificações de atualização serão suprimidas por dia a partir de Hora:Minuto por um período de duração (em minutos).</span><span class="sxs-lookup"><span data-stu-id="e54e3-438">If you enable this policy, update checks are suppressed each day starting at Hour:Minute for a period of Duration (in minutes).</span></span> <span data-ttu-id="e54e3-439">A duração não é afetada pelo horário de verão.</span><span class="sxs-lookup"><span data-stu-id="e54e3-439">Duration isn't affected by daylight saving time.</span></span> <span data-ttu-id="e54e3-440">Por exemplo, se o horário de início for 22:00 e a duração for de 480 minutos, as atualizações serão suprimidas por exatamente oito horas, independentemente do horário de verão começar ou terminar durante esse período.</span><span class="sxs-lookup"><span data-stu-id="e54e3-440">For example, if the start time is 22:00 and the duration is 480 minutes, updates will be suppressed for exactly 8 hours, regardless of whether daylight saving time starts or ends during this period.</span></span>

  <span data-ttu-id="e54e3-441">Se você desabilitar ou não configurar essa política, as verificações de atualização não serão suprimidas durante nenhum período específico.</span><span class="sxs-lookup"><span data-stu-id="e54e3-441">If you disable or don't configure this policy, update checks aren't suppressed during any specific period.</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="e54e3-442">Informações e configurações do Windows</span><span class="sxs-lookup"><span data-stu-id="e54e3-442">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="e54e3-443">Informações da Política de Grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="e54e3-443">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="e54e3-444">Nome exclusivo da Política de Grupo: UpdatesSuppressed</span><span class="sxs-lookup"><span data-stu-id="e54e3-444">GP unique name: UpdatesSuppressed</span></span>
- <span data-ttu-id="e54e3-445">Nome da Política de Grupo: Período em cada dia para suprimir a verificação de atualização automática</span><span class="sxs-lookup"><span data-stu-id="e54e3-445">GP name: Time period in each day to suppress auto-update check</span></span>
  - <span data-ttu-id="e54e3-446">Opções { Hour, Minute, Duration }</span><span class="sxs-lookup"><span data-stu-id="e54e3-446">Options { Hour, Minute, Duration }</span></span>
- <span data-ttu-id="e54e3-447">Caminho da Política de Grupo: Modelos Administrativos/Microsoft Edge Update/Preferências</span><span class="sxs-lookup"><span data-stu-id="e54e3-447">GP path: Administrative Templates/Microsoft Edge Update/Preferences</span></span>
- <span data-ttu-id="e54e3-448">Nome do arquivo GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="e54e3-448">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="e54e3-449">Configurações de registro do Windows</span><span class="sxs-lookup"><span data-stu-id="e54e3-449">Windows Registry Settings</span></span>
- <span data-ttu-id="e54e3-450">Caminho: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="e54e3-450">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="e54e3-451">Nome do valor:</span><span class="sxs-lookup"><span data-stu-id="e54e3-451">Value Name:</span></span> 
  - <span data-ttu-id="e54e3-452">UpdatesSuppressedDurationMin</span><span class="sxs-lookup"><span data-stu-id="e54e3-452">UpdatesSuppressedDurationMin</span></span>
  - <span data-ttu-id="e54e3-453">UpdatesSuppressedStartHour</span><span class="sxs-lookup"><span data-stu-id="e54e3-453">UpdatesSuppressedStartHour</span></span>
  - <span data-ttu-id="e54e3-454">UpdatesSuppressedStartMin</span><span class="sxs-lookup"><span data-stu-id="e54e3-454">UpdatesSuppressedStartMin</span></span>
- <span data-ttu-id="e54e3-455">Tipo de valor: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="e54e3-455">Value Type: REG_DWORD</span></span>
##### <a name="example-value"></a><span data-ttu-id="e54e3-456">Valor de exemplo:</span><span class="sxs-lookup"><span data-stu-id="e54e3-456">Example value:</span></span>
```
duration   : 0x0000003c
start hour : 0x00000001
start min  : 0x00000002
```
[<span data-ttu-id="e54e3-457">Voltar ao início</span><span class="sxs-lookup"><span data-stu-id="e54e3-457">Back to top</span></span>](#microsoft-edge---update-policies)


## <a name="proxy-server-policies"></a><span data-ttu-id="e54e3-458">Políticas do servidor proxy</span><span class="sxs-lookup"><span data-stu-id="e54e3-458">Proxy Server policies</span></span>

[<span data-ttu-id="e54e3-459">Voltar ao início</span><span class="sxs-lookup"><span data-stu-id="e54e3-459">Back to top</span></span>](#microsoft-edge---update-policies)
### <a name="proxymode"></a><span data-ttu-id="e54e3-460">ProxyMode</span><span class="sxs-lookup"><span data-stu-id="e54e3-460">ProxyMode</span></span>
#### <a name="choose-how-to-specify-proxy-server-settings"></a><span data-ttu-id="e54e3-461">Escolher como especificar as configurações do servidor proxy</span><span class="sxs-lookup"><span data-stu-id="e54e3-461">Choose how to specify proxy server settings</span></span>
><span data-ttu-id="e54e3-462">Microsoft Edge Update 1.3.21.81 e posterior</span><span class="sxs-lookup"><span data-stu-id="e54e3-462">Microsoft Edge Update 1.3.21.81 and later</span></span>

#### <a name="description"></a><span data-ttu-id="e54e3-463">Descrição</span><span class="sxs-lookup"><span data-stu-id="e54e3-463">Description</span></span>
<span data-ttu-id="e54e3-464">Permite especificar as configurações do servidor proxy que serão usadas pelo Microsoft Edge Update.</span><span class="sxs-lookup"><span data-stu-id="e54e3-464">Allows you to specify the proxy server settings that are used by Microsoft Edge Update.</span></span>

  <span data-ttu-id="e54e3-465">Se você habilitar essa configuração da política, poderá escolher entre as seguintes opções do servidor proxy:</span><span class="sxs-lookup"><span data-stu-id="e54e3-465">If you enable this policy, you can choose between the following proxy server options:</span></span>
   - <span data-ttu-id="e54e3-466">Se você optar por nunca usar um servidor proxy e sempre se conectar diretamente, todas as outras opções serão ignoradas.</span><span class="sxs-lookup"><span data-stu-id="e54e3-466">If you choose to never use a proxy server and always connect directly, all other options are ignored.</span></span>
   - <span data-ttu-id="e54e3-467">Se você optar por usar as configurações de proxy do sistema ou detectar automaticamente o servidor proxy, todas as outras opções serão ignoradas.</span><span class="sxs-lookup"><span data-stu-id="e54e3-467">If you choose to use system proxy settings or auto-detect the proxy server, all other options are ignored.</span></span>
   - <span data-ttu-id="e54e3-468">Se escolher o modo fixo do servidor proxy, você poderá especificar mais opções em '[Endereço ou URL do servidor proxy](#proxyserver)'.</span><span class="sxs-lookup"><span data-stu-id="e54e3-468">If you choose fixed server proxy mode, you can specify further options in '[Address or URL of proxy server](#proxyserver)' policy.</span></span>
   - <span data-ttu-id="e54e3-469">Se você optar por usar um script de proxy .pac, deve especificar a URL do script em '[De URL para um arquivo .pac de proxy](#proxypacurl)'.</span><span class="sxs-lookup"><span data-stu-id="e54e3-469">If you choose to use a .pac proxy script, you must specify the URL for the script in '[URL to a proxy .pac file](#proxypacurl)' policy.</span></span>

  <span data-ttu-id="e54e3-470">Se você habilitar essa política, os usuários de sua organização não poderão alterar as configurações de proxy no Microsoft Edge Update.</span><span class="sxs-lookup"><span data-stu-id="e54e3-470">If you enable this policy, users in your organization can't change the proxy settings in Microsoft Edge Update.</span></span>

  <span data-ttu-id="e54e3-471">Se você desabilitar ou não configurar essa política, nenhuma configuração do servidor proxy será definida, mas os usuários de sua organização poderão escolher suas próprias configurações de proxy para o Microsoft Edge Update.</span><span class="sxs-lookup"><span data-stu-id="e54e3-471">If you disable or don't configure this policy, no proxy server settings are configured, but users in your organization can choose their own proxy settings for Microsoft Edge Update.</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="e54e3-472">Informações e configurações do Windows</span><span class="sxs-lookup"><span data-stu-id="e54e3-472">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="e54e3-473">Informações da Política de Grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="e54e3-473">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="e54e3-474">Nome exclusivo da Política de Grupo: ProxyMode</span><span class="sxs-lookup"><span data-stu-id="e54e3-474">GP unique name: ProxyMode</span></span>
- <span data-ttu-id="e54e3-475">Nome da Política de Grupo: Escolher como especificar as configurações do servidor proxy</span><span class="sxs-lookup"><span data-stu-id="e54e3-475">GP name: Choose how to specify proxy server settings</span></span>
- <span data-ttu-id="e54e3-476">Caminho da Política de Grupo: Modelos Administrativos/Microsoft Edge Update/Servidor Proxy</span><span class="sxs-lookup"><span data-stu-id="e54e3-476">GP path: Administrative Templates/Microsoft Edge Update/Proxy Server</span></span>
- <span data-ttu-id="e54e3-477">Nome do arquivo GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="e54e3-477">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="e54e3-478">Configurações de registro do Windows</span><span class="sxs-lookup"><span data-stu-id="e54e3-478">Windows Registry Settings</span></span>
- <span data-ttu-id="e54e3-479">Caminho: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="e54e3-479">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="e54e3-480">Nome do valor: ProxyMode</span><span class="sxs-lookup"><span data-stu-id="e54e3-480">Value Name: ProxyMode</span></span>
- <span data-ttu-id="e54e3-481">Tipo do valor: REG_SZ</span><span class="sxs-lookup"><span data-stu-id="e54e3-481">Value Type: REG_SZ</span></span>
##### <a name="example-value"></a><span data-ttu-id="e54e3-482">Valor de exemplo:</span><span class="sxs-lookup"><span data-stu-id="e54e3-482">Example value:</span></span>
```
fixed_servers
```
[<span data-ttu-id="e54e3-483">Voltar ao início</span><span class="sxs-lookup"><span data-stu-id="e54e3-483">Back to top</span></span>](#microsoft-edge---update-policies)


### <a name="proxypacurl"></a><span data-ttu-id="e54e3-484">ProxyPacUrl</span><span class="sxs-lookup"><span data-stu-id="e54e3-484">ProxyPacUrl</span></span>
#### <a name="url-to-a-proxy-pac-file"></a><span data-ttu-id="e54e3-485">A URL para um arquivo .pac de proxy</span><span class="sxs-lookup"><span data-stu-id="e54e3-485">URL to a proxy .pac file</span></span>
><span data-ttu-id="e54e3-486">Microsoft Edge Update 1.3.21.81 e posterior</span><span class="sxs-lookup"><span data-stu-id="e54e3-486">Microsoft Edge Update 1.3.21.81 and later</span></span>

#### <a name="description"></a><span data-ttu-id="e54e3-487">Descrição</span><span class="sxs-lookup"><span data-stu-id="e54e3-487">Description</span></span>
<span data-ttu-id="e54e3-488">Permite especificar uma URL para um arquivo (PAC) de configuração automática de proxy.</span><span class="sxs-lookup"><span data-stu-id="e54e3-488">Allows you to specify a URL for a proxy auto-config (PAC) file.</span></span>

  <span data-ttu-id="e54e3-489">Se habilitar essa política, você poderá especificar uma URL de um arquivo PAC para automatizar a maneira como o Microsoft Edge Update seleciona para a busca de um site específico.</span><span class="sxs-lookup"><span data-stu-id="e54e3-489">If you enable this policy, you can specify a URL for a PAC file to automate how Microsoft Edge Update selects the appropriate proxy server for fetching a particular website.</span></span>

  <span data-ttu-id="e54e3-490">Essa política será aplicada somente se você especificou as configurações de proxy manuais na política '[Escolher como especificar configurações do servidor proxy](#proxymode)'.</span><span class="sxs-lookup"><span data-stu-id="e54e3-490">This policy is applied only if you have specified manual proxy settings in the '[Choose how to specify proxy server settings](#proxymode)' policy.</span></span>

  <span data-ttu-id="e54e3-491">Não configure essa política se você selecionou uma configuração de proxy que não seja manual na política '[Escolher como especificar as configurações do servidor proxy](#proxymode)'.</span><span class="sxs-lookup"><span data-stu-id="e54e3-491">Don't configure this policy if you have selected a proxy setting other than manual in the '[Choose how to specify proxy server settings](#proxymode)' policy.</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="e54e3-492">Informações e configurações do Windows</span><span class="sxs-lookup"><span data-stu-id="e54e3-492">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="e54e3-493">Informações da Política de Grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="e54e3-493">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="e54e3-494">Nome exclusivo da Política de Grupo: ProxyPacUrl</span><span class="sxs-lookup"><span data-stu-id="e54e3-494">GP unique name: ProxyPacUrl</span></span>
- <span data-ttu-id="e54e3-495">Nome da Política de Grupo: A URL para um arquivo .pac de proxy</span><span class="sxs-lookup"><span data-stu-id="e54e3-495">GP name: URL to a proxy .pac file</span></span>
- <span data-ttu-id="e54e3-496">Caminho da Política de Grupo: Modelos Administrativos/Microsoft Edge Update/Servidor Proxy</span><span class="sxs-lookup"><span data-stu-id="e54e3-496">GP path: Administrative Templates/Microsoft Edge Update/Proxy Server</span></span>
- <span data-ttu-id="e54e3-497">Nome do arquivo GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="e54e3-497">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="e54e3-498">Configurações de registro do Windows</span><span class="sxs-lookup"><span data-stu-id="e54e3-498">Windows Registry Settings</span></span>
- <span data-ttu-id="e54e3-499">Caminho: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="e54e3-499">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="e54e3-500">Nome do valor: ProxyPacUrl</span><span class="sxs-lookup"><span data-stu-id="e54e3-500">Value Name: ProxyPacUrl</span></span>
- <span data-ttu-id="e54e3-501">Tipo do valor: REG_SZ</span><span class="sxs-lookup"><span data-stu-id="e54e3-501">Value Type: REG_SZ</span></span>
##### <a name="example-value"></a><span data-ttu-id="e54e3-502">Valor de exemplo:</span><span class="sxs-lookup"><span data-stu-id="e54e3-502">Example value:</span></span>
```
https://www.microsoft.com
```
[<span data-ttu-id="e54e3-503">Voltar ao início</span><span class="sxs-lookup"><span data-stu-id="e54e3-503">Back to top</span></span>](#microsoft-edge---update-policies)


### <a name="proxyserver"></a><span data-ttu-id="e54e3-504">ProxyServer</span><span class="sxs-lookup"><span data-stu-id="e54e3-504">ProxyServer</span></span>
#### <a name="address-or-url-of-proxy-server"></a><span data-ttu-id="e54e3-505">Endereço ou URL do servidor proxy</span><span class="sxs-lookup"><span data-stu-id="e54e3-505">Address or URL of proxy server</span></span>
><span data-ttu-id="e54e3-506">Microsoft Edge Update 1.3.21.81 e posterior</span><span class="sxs-lookup"><span data-stu-id="e54e3-506">Microsoft Edge Update 1.3.21.81 and later</span></span>

#### <a name="description"></a><span data-ttu-id="e54e3-507">Description</span><span class="sxs-lookup"><span data-stu-id="e54e3-507">Description</span></span>
<span data-ttu-id="e54e3-508">Permite especificar a URL do servidor proxy para o Microsoft Edge Update usar.</span><span class="sxs-lookup"><span data-stu-id="e54e3-508">Allows you to specify the URL of the proxy server for Microsoft Edge Update to use.</span></span>

  <span data-ttu-id="e54e3-509">Se você habilitar essa política, poderá configurar a URL do servidor proxy usada pelo Microsoft Edge Update em sua organização.</span><span class="sxs-lookup"><span data-stu-id="e54e3-509">If you enable this policy, you can set the proxy server URL used by Microsoft Edge Update in your organization.</span></span>

  <span data-ttu-id="e54e3-510">Essa política será aplicada somente se você selecionou as configurações de proxy manuais na política '[Escolher como especificar as configurações do servidor proxy](#proxymode)'.</span><span class="sxs-lookup"><span data-stu-id="e54e3-510">This policy is applied only if you have selected manual proxy settings in the '[Choose how to specify proxy server settings](#proxymode)' policy.</span></span>

  <span data-ttu-id="e54e3-511">Não configure essa política se você selecionou uma configuração de proxy que não seja manual na política '[Escolher como especificar as configurações do servidor proxy](#proxymode)'.</span><span class="sxs-lookup"><span data-stu-id="e54e3-511">Don't configure this policy if you have selected a proxy setting other than manual in the '[Choose how to specify proxy server settings](#proxymode)' policy.</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="e54e3-512">Informações e configurações do Windows</span><span class="sxs-lookup"><span data-stu-id="e54e3-512">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="e54e3-513">Informações da Política de Grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="e54e3-513">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="e54e3-514">Nome exclusivo da Política de Grupo: ProxyServer</span><span class="sxs-lookup"><span data-stu-id="e54e3-514">GP unique name: ProxyServer</span></span>
- <span data-ttu-id="e54e3-515">Nome da Política de Grupo: O endereço ou a URL do servidor proxy</span><span class="sxs-lookup"><span data-stu-id="e54e3-515">GP name: Address or URL of proxy server</span></span>
- <span data-ttu-id="e54e3-516">Caminho da Política de Grupo: Modelos Administrativos/Microsoft Edge Update/Servidor Proxy</span><span class="sxs-lookup"><span data-stu-id="e54e3-516">GP path: Administrative Templates/Microsoft Edge Update/Proxy Server</span></span>
- <span data-ttu-id="e54e3-517">Nome do arquivo GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="e54e3-517">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="e54e3-518">Configurações de registro do Windows</span><span class="sxs-lookup"><span data-stu-id="e54e3-518">Windows Registry Settings</span></span>
- <span data-ttu-id="e54e3-519">Caminho: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="e54e3-519">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="e54e3-520">Nome do valor: ProxyServer</span><span class="sxs-lookup"><span data-stu-id="e54e3-520">Value Name: ProxyServer</span></span>
- <span data-ttu-id="e54e3-521">Tipo do valor: REG_SZ</span><span class="sxs-lookup"><span data-stu-id="e54e3-521">Value Type: REG_SZ</span></span>
##### <a name="example-value"></a><span data-ttu-id="e54e3-522">Valor de exemplo:</span><span class="sxs-lookup"><span data-stu-id="e54e3-522">Example value:</span></span>
```
https://www.microsoft.com
```
[<span data-ttu-id="e54e3-523">Voltar ao início</span><span class="sxs-lookup"><span data-stu-id="e54e3-523">Back to top</span></span>](#microsoft-edge---update-policies)


## <a name="microsoft-edge-webview-policies"></a><span data-ttu-id="e54e3-524">Políticas do Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="e54e3-524">Microsoft Edge WebView policies</span></span>

[<span data-ttu-id="e54e3-525">Voltar ao início</span><span class="sxs-lookup"><span data-stu-id="e54e3-525">Back to top</span></span>](#microsoft-edge---update-policies)
### <a name="install-webview"></a><span data-ttu-id="e54e3-526">Instalar (WebView)</span><span class="sxs-lookup"><span data-stu-id="e54e3-526">Install (WebView)</span></span>
#### <a name="allow-installation"></a><span data-ttu-id="e54e3-527">Permitir instalação</span><span class="sxs-lookup"><span data-stu-id="e54e3-527">Allow installation</span></span>
><span data-ttu-id="e54e3-528">Microsoft Edge Update 1.3.127.1 e posterior</span><span class="sxs-lookup"><span data-stu-id="e54e3-528">Microsoft Edge Update 1.3.127.1 and later</span></span>

#### <a name="description"></a><span data-ttu-id="e54e3-529">Descrição</span><span class="sxs-lookup"><span data-stu-id="e54e3-529">Description</span></span>
<span data-ttu-id="e54e3-530">Permite especificar se o Microsoft Edge WebView pode ser instalado usando o Microsoft Edge Update.</span><span class="sxs-lookup"><span data-stu-id="e54e3-530">Lets you specify whether Microsoft Edge WebView can be installed using Microsoft Edge Update.</span></span>

  - <span data-ttu-id="e54e3-531">Se você habilitar esta política, os usuários poderão instalar o Microsoft Edge WebView por meio do Microsoft Edge Update.</span><span class="sxs-lookup"><span data-stu-id="e54e3-531">If you enable this policy, users can install Microsoft Edge WebView through Microsoft Edge Update.</span></span>
  - <span data-ttu-id="e54e3-532">Se você desabilitar esta política, os usuários não poderão instalar o Microsoft Edge WebView por meio do Microsoft Edge Update.</span><span class="sxs-lookup"><span data-stu-id="e54e3-532">If you disable this policy, users cannot install Microsoft Edge WebView through Microsoft Edge Update.</span></span>
  - <span data-ttu-id="e54e3-533">Se você não configurar esta política, a configuração da política '[Permitir instalação padrão](#installdefault)' determina se os usuários podem instalar o Microsoft Edge WebView por meio do Microsoft Edge Update.</span><span class="sxs-lookup"><span data-stu-id="e54e3-533">If you don't configure this policy, the '[Allow installation default](#installdefault)' policy configuration determines whether users can install Microsoft Edge WebView through Microsoft Edge Update.</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="e54e3-534">Informações e configurações do Windows</span><span class="sxs-lookup"><span data-stu-id="e54e3-534">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="e54e3-535">Informações da Política de Grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="e54e3-535">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="e54e3-536">Nome exclusivo da Política de Grupo: Install</span><span class="sxs-lookup"><span data-stu-id="e54e3-536">GP unique name: Install</span></span>
- <span data-ttu-id="e54e3-537">Nome da Política de Grupo: Permitir instalação</span><span class="sxs-lookup"><span data-stu-id="e54e3-537">GP name: Allow installation</span></span>
- <span data-ttu-id="e54e3-538">Caminho da Política de Grupo: Modelos Administrativos/Microsoft Edge Update/Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="e54e3-538">GP path: Administrative Templates/Microsoft Edge Update/Microsoft Edge WebView</span></span>
- <span data-ttu-id="e54e3-539">Nome do arquivo GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="e54e3-539">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="e54e3-540">Configurações de registro do Windows</span><span class="sxs-lookup"><span data-stu-id="e54e3-540">Windows Registry Settings</span></span>
- <span data-ttu-id="e54e3-541">Caminho: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="e54e3-541">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="e54e3-542">Nome do valor:</span><span class="sxs-lookup"><span data-stu-id="e54e3-542">Value Name:</span></span> 
  - <span data-ttu-id="e54e3-543">Install{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}</span><span class="sxs-lookup"><span data-stu-id="e54e3-543">Install{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}</span></span>
- <span data-ttu-id="e54e3-544">Tipo de valor: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="e54e3-544">Value Type: REG_DWORD</span></span>
##### <a name="example-value"></a><span data-ttu-id="e54e3-545">Valor de exemplo:</span><span class="sxs-lookup"><span data-stu-id="e54e3-545">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="e54e3-546">Voltar ao início</span><span class="sxs-lookup"><span data-stu-id="e54e3-546">Back to top</span></span>](#microsoft-edge---update-policies)


### <a name="update-webview"></a><span data-ttu-id="e54e3-547">Atualização (WebView)</span><span class="sxs-lookup"><span data-stu-id="e54e3-547">Update (WebView)</span></span>
#### <a name="update-policy-override"></a><span data-ttu-id="e54e3-548">Atualizar a substituição de política</span><span class="sxs-lookup"><span data-stu-id="e54e3-548">Update policy override</span></span>
><span data-ttu-id="e54e3-549">Microsoft Edge Update 1.3.127.1 e posterior</span><span class="sxs-lookup"><span data-stu-id="e54e3-549">Microsoft Edge Update 1.3.127.1 and later</span></span>

#### <a name="description"></a><span data-ttu-id="e54e3-550">Descrição</span><span class="sxs-lookup"><span data-stu-id="e54e3-550">Description</span></span>
<span data-ttu-id="e54e3-551">Permite especificar se as atualizações automáticas estão habilitadas ou não para o Microsoft Edge WebView.</span><span class="sxs-lookup"><span data-stu-id="e54e3-551">Lets you specify whether or not automatic updates are enabled for Microsoft Edge WebView.</span></span> <span data-ttu-id="e54e3-552">O Microsoft Edge WebView é um componente usado pelos aplicativos para exibir conteúdo da Web.</span><span class="sxs-lookup"><span data-stu-id="e54e3-552">Microsoft Edge WebView is a component used by applications to display web content.</span></span>
<span data-ttu-id="e54e3-553">As atualizações automáticas estão habilitadas por padrão.</span><span class="sxs-lookup"><span data-stu-id="e54e3-553">Automatic updates are enabled by default.</span></span> <span data-ttu-id="e54e3-554">Desabilitar as atualizações automáticas do Microsoft Edge WebView pode causar problemas de compatibilidade com aplicativos que dependem desse componente.</span><span class="sxs-lookup"><span data-stu-id="e54e3-554">Disabling automatic updates for Microsoft Edge WebView might cause compatibility issues with applications that depend on this component.</span></span>

  <span data-ttu-id="e54e3-555">Se você habilitar esta política, o Microsoft Edge Update tratará as atualizações do Microsoft Edge WebView de acordo com as seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="e54e3-555">If you enable this policy, Microsoft Edge Update handles Microsoft Edge WebView updates according to how you configure the following options:</span></span>
  - <span data-ttu-id="e54e3-556">Sempre permitir atualizações: as atualizações serão baixadas e aplicadas automaticamente</span><span class="sxs-lookup"><span data-stu-id="e54e3-556">Always allow updates: Updates are automatically downloaded and applied</span></span>
  - <span data-ttu-id="e54e3-557">Atualizações desabilitadas: as atualizações nunca serão baixadas ou aplicadas</span><span class="sxs-lookup"><span data-stu-id="e54e3-557">Updates disabled: Updates are never downloaded or applied</span></span>

  <span data-ttu-id="e54e3-558">Se você não habilitar esta política, as atualizações serão baixadas e aplicadas automaticamente.</span><span class="sxs-lookup"><span data-stu-id="e54e3-558">If you don't enable this policy, updates are automatically downloaded and applied.</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="e54e3-559">Informações e configurações do Windows</span><span class="sxs-lookup"><span data-stu-id="e54e3-559">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="e54e3-560">Informações da Política de Grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="e54e3-560">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="e54e3-561">Nome exclusivo da Política de Grupo: Update</span><span class="sxs-lookup"><span data-stu-id="e54e3-561">GP unique name: Update</span></span>
- <span data-ttu-id="e54e3-562">Nome da Política de Grupo: Atualizar a substituição de política</span><span class="sxs-lookup"><span data-stu-id="e54e3-562">GP name: Update policy override</span></span>
- <span data-ttu-id="e54e3-563">Caminho da Política de Grupo: Modelos Administrativos/Microsoft Edge Update/Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="e54e3-563">GP path: Administrative Templates/Microsoft Edge Update/Microsoft Edge WebView</span></span>
- <span data-ttu-id="e54e3-564">Nome do arquivo GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="e54e3-564">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="e54e3-565">Configurações de registro do Windows</span><span class="sxs-lookup"><span data-stu-id="e54e3-565">Windows Registry Settings</span></span>
- <span data-ttu-id="e54e3-566">Caminho: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="e54e3-566">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="e54e3-567">Nome do valor:</span><span class="sxs-lookup"><span data-stu-id="e54e3-567">Value Name:</span></span> 
  - <span data-ttu-id="e54e3-568">Update{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}</span><span class="sxs-lookup"><span data-stu-id="e54e3-568">Update{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}</span></span>
- <span data-ttu-id="e54e3-569">Tipo de valor: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="e54e3-569">Value Type: REG_DWORD</span></span>
##### <a name="example-value"></a><span data-ttu-id="e54e3-570">Valor de exemplo:</span><span class="sxs-lookup"><span data-stu-id="e54e3-570">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="e54e3-571">Voltar ao início</span><span class="sxs-lookup"><span data-stu-id="e54e3-571">Back to top</span></span>](#microsoft-edge---update-policies)


## <a name="see-also"></a><span data-ttu-id="e54e3-572">Consulte também</span><span class="sxs-lookup"><span data-stu-id="e54e3-572">See also</span></span>
  - [<span data-ttu-id="e54e3-573">Configurar o Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="e54e3-573">Configuring Microsoft Edge</span></span>](configure-microsoft-edge.md)
  - [<span data-ttu-id="e54e3-574">Página de aterrissagem do Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="e54e3-574">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
