---
title: Documentação da política do Microsoft Edge Update
ms.author: stmoody
author: brianalt-msft
manager: tahills
ms.date: 10/07/2020
audience: ITPro
ms.topic: reference
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
ms.custom: ''
description: Documentação para todas as políticas compatíveis com o Microsoft Edge Update
ms.openlocfilehash: feb7859f062ae39e2bbfe08d8e478386defb85cf
ms.sourcegitcommit: 4e6188ade942ca6fd599a4ce1c8e0d90d3d03399
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2020
ms.locfileid: "11105565"
---
# <span data-ttu-id="c75ac-103">Microsoft Edge - Políticas de atualização</span><span class="sxs-lookup"><span data-stu-id="c75ac-103">Microsoft Edge - Update policies</span></span>
<span data-ttu-id="c75ac-104">A versão mais recente do Microsoft Edge inclui as seguintes políticas que você pode usar para controlar como e quando o Microsoft Edge é atualizado.</span><span class="sxs-lookup"><span data-stu-id="c75ac-104">The latest version of Microsoft Edge includes the following policies that you can use to control how and when Microsoft Edge is updated.</span></span>

<span data-ttu-id="c75ac-105">Para obter informações sobre outras políticas disponíveis no Microsoft Edge, confira [Referência de política do navegador Microsoft Edge](microsoft-edge-policies.md)</span><span class="sxs-lookup"><span data-stu-id="c75ac-105">For information about other policies available in Microsoft Edge, check out [Microsoft Edge browser policy reference](microsoft-edge-policies.md)</span></span>
> [!NOTE]
> <span data-ttu-id="c75ac-106">Este artigo se aplica ao Microsoft Edge versão 77 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="c75ac-106">This article applies to Microsoft Edge version 77 or later.</span></span>
## <span data-ttu-id="c75ac-107">Políticas disponíveis</span><span class="sxs-lookup"><span data-stu-id="c75ac-107">Available policies</span></span>
<span data-ttu-id="c75ac-108">Estas tabelas listam todas as políticas de grupo relacionadas a atualizações disponíveis nesta versão do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="c75ac-108">These tables lists all of the update-related group policies available in this release of Microsoft Edge.</span></span> <span data-ttu-id="c75ac-109">Use os links na tabela a seguir para obter mais detalhes sobre políticas específicas.</span><span class="sxs-lookup"><span data-stu-id="c75ac-109">Use the links in the table to get more details about specific policies.</span></span>

|||
|-|-|
|[<span data-ttu-id="c75ac-110">Aplicativos</span><span class="sxs-lookup"><span data-stu-id="c75ac-110">Applications</span></span>](#applications)|[<span data-ttu-id="c75ac-111">Preferências</span><span class="sxs-lookup"><span data-stu-id="c75ac-111">Preferences</span></span>](#preferences)|
|[<span data-ttu-id="c75ac-112">Servidor proxy</span><span class="sxs-lookup"><span data-stu-id="c75ac-112">Proxy Server</span></span>](#proxy-server)|[<span data-ttu-id="c75ac-113">Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="c75ac-113">Microsoft Edge WebView</span></span>](#microsoft-edge-webview)|

### [<span data-ttu-id="c75ac-114">Aplicativos</span><span class="sxs-lookup"><span data-stu-id="c75ac-114">Applications</span></span>](#applications-policies)
|<span data-ttu-id="c75ac-115">Nome da política</span><span class="sxs-lookup"><span data-stu-id="c75ac-115">Policy Name</span></span>|<span data-ttu-id="c75ac-116">Legenda</span><span class="sxs-lookup"><span data-stu-id="c75ac-116">Caption</span></span>|
|-|-|
|[<span data-ttu-id="c75ac-117">InstallDefault</span><span class="sxs-lookup"><span data-stu-id="c75ac-117">InstallDefault</span></span>](#installdefault)|<span data-ttu-id="c75ac-118">Permitir a instalação padrão</span><span class="sxs-lookup"><span data-stu-id="c75ac-118">Allow installation default</span></span>|
|[<span data-ttu-id="c75ac-119">UpdateDefault</span><span class="sxs-lookup"><span data-stu-id="c75ac-119">UpdateDefault</span></span>](#updatedefault)|<span data-ttu-id="c75ac-120">Atualizar o padrão de substituição de política</span><span class="sxs-lookup"><span data-stu-id="c75ac-120">Update policy override default</span></span>|
|[<span data-ttu-id="c75ac-121">Install</span><span class="sxs-lookup"><span data-stu-id="c75ac-121">Install</span></span>](#install)|<span data-ttu-id="c75ac-122">Permitir a instalação (por canal)</span><span class="sxs-lookup"><span data-stu-id="c75ac-122">Allow installation (per channel)</span></span>|
|[<span data-ttu-id="c75ac-123">Update</span><span class="sxs-lookup"><span data-stu-id="c75ac-123">Update</span></span>](#update)|<span data-ttu-id="c75ac-124">Atualizar a substituição de política (por canal)</span><span class="sxs-lookup"><span data-stu-id="c75ac-124">Update policy override (per channel)</span></span>|
|[<span data-ttu-id="c75ac-125">Allowsxs</span><span class="sxs-lookup"><span data-stu-id="c75ac-125">Allowsxs</span></span>](#allowsxs)|<span data-ttu-id="c75ac-126">Permitir a experiência de navegador Lado a Lado do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="c75ac-126">Allow Microsoft Edge Side by Side browser experience</span></span>|
|[<span data-ttu-id="c75ac-127">CreateDesktopShortcutDefault</span><span class="sxs-lookup"><span data-stu-id="c75ac-127">CreateDesktopShortcutDefault</span></span>](#createdesktopshortcutdefault)|<span data-ttu-id="c75ac-128">Impedir a criação de Atalho da Área de Trabalho com a instalação padrão</span><span class="sxs-lookup"><span data-stu-id="c75ac-128">Prevent Desktop Shortcut creation upon install default</span></span>|
|[<span data-ttu-id="c75ac-129">CreateDesktopShortcut</span><span class="sxs-lookup"><span data-stu-id="c75ac-129">CreateDesktopShortcut</span></span>](#createdesktopshortcut)|<span data-ttu-id="c75ac-130">Impedir a criação de Atalho da Área de Trabalho com a instalação (por canal)</span><span class="sxs-lookup"><span data-stu-id="c75ac-130">Prevent Desktop Shortcut creation upon install (per channel)</span></span>|
|[<span data-ttu-id="c75ac-131">RollbackToTargetVersion</span><span class="sxs-lookup"><span data-stu-id="c75ac-131">RollbackToTargetVersion</span></span>](#rollbacktotargetversion)|<span data-ttu-id="c75ac-132">Reverter para a Versão de Destino (por canal)</span><span class="sxs-lookup"><span data-stu-id="c75ac-132">Rollback to Target version (per channel)</span></span>|
|[<span data-ttu-id="c75ac-133">TargetVersionPrefix</span><span class="sxs-lookup"><span data-stu-id="c75ac-133">TargetVersionPrefix</span></span>](#targetversionprefix)|<span data-ttu-id="c75ac-134">Substituir versão de destino (por canal)</span><span class="sxs-lookup"><span data-stu-id="c75ac-134">Target version override (per channel)</span></span>|

### [<span data-ttu-id="c75ac-135">Preferências</span><span class="sxs-lookup"><span data-stu-id="c75ac-135">Preferences</span></span>](#preferences-policies)
|<span data-ttu-id="c75ac-136">Nome da política</span><span class="sxs-lookup"><span data-stu-id="c75ac-136">Policy Name</span></span>|<span data-ttu-id="c75ac-137">Legenda</span><span class="sxs-lookup"><span data-stu-id="c75ac-137">Caption</span></span>|
|-|-|
|[<span data-ttu-id="c75ac-138">AutoUpdateCheckPeriodMinutes</span><span class="sxs-lookup"><span data-stu-id="c75ac-138">AutoUpdateCheckPeriodMinutes</span></span>](#autoupdatecheckperiodminutes)|<span data-ttu-id="c75ac-139">Atualizar automaticamente a substituição do período de verificação</span><span class="sxs-lookup"><span data-stu-id="c75ac-139">Auto-update check period override</span></span>|
|[<span data-ttu-id="c75ac-140">UpdatesSuppressed</span><span class="sxs-lookup"><span data-stu-id="c75ac-140">UpdatesSuppressed</span></span>](#updatessuppressed)|<span data-ttu-id="c75ac-141">O período em cada dia para suprimir a verificação de atualização automática</span><span class="sxs-lookup"><span data-stu-id="c75ac-141">Time period in each day to suppress auto-update check</span></span>|

### [<span data-ttu-id="c75ac-142">Servidor proxy</span><span class="sxs-lookup"><span data-stu-id="c75ac-142">Proxy Server</span></span>](#proxy-server-policies)
|<span data-ttu-id="c75ac-143">Nome da política</span><span class="sxs-lookup"><span data-stu-id="c75ac-143">Policy Name</span></span>|<span data-ttu-id="c75ac-144">Legenda</span><span class="sxs-lookup"><span data-stu-id="c75ac-144">Caption</span></span>|
|-|-|
|[<span data-ttu-id="c75ac-145">ProxyMode</span><span class="sxs-lookup"><span data-stu-id="c75ac-145">ProxyMode</span></span>](#proxymode)|<span data-ttu-id="c75ac-146">Escolher como especificar as configurações do servidor proxy</span><span class="sxs-lookup"><span data-stu-id="c75ac-146">Choose how to specify proxy server settings</span></span>|
|[<span data-ttu-id="c75ac-147">ProxyPacUrl</span><span class="sxs-lookup"><span data-stu-id="c75ac-147">ProxyPacUrl</span></span>](#proxypacurl)|<span data-ttu-id="c75ac-148">A URL para um arquivo .pac de proxy</span><span class="sxs-lookup"><span data-stu-id="c75ac-148">URL to a proxy .pac file</span></span>|
|[<span data-ttu-id="c75ac-149">ProxyServer</span><span class="sxs-lookup"><span data-stu-id="c75ac-149">ProxyServer</span></span>](#proxyserver)|<span data-ttu-id="c75ac-150">Endereço ou URL do servidor proxy</span><span class="sxs-lookup"><span data-stu-id="c75ac-150">Address or URL of proxy server</span></span>|

### [<span data-ttu-id="c75ac-151">Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="c75ac-151">Microsoft Edge WebView</span></span>](#microsoft-edge-webview-policies)
|<span data-ttu-id="c75ac-152">Nome da política</span><span class="sxs-lookup"><span data-stu-id="c75ac-152">Policy Name</span></span>|<span data-ttu-id="c75ac-153">Legenda</span><span class="sxs-lookup"><span data-stu-id="c75ac-153">Caption</span></span>|
|-|-|
|[<span data-ttu-id="c75ac-154">Instalar</span><span class="sxs-lookup"><span data-stu-id="c75ac-154">Install</span></span>](#install-webview)|<span data-ttu-id="c75ac-155">Permitir instalação</span><span class="sxs-lookup"><span data-stu-id="c75ac-155">Allow installation</span></span>|
|[<span data-ttu-id="c75ac-156">Atualização</span><span class="sxs-lookup"><span data-stu-id="c75ac-156">Update</span></span>](#update-webview)|<span data-ttu-id="c75ac-157">Atualizar a substituição de política</span><span class="sxs-lookup"><span data-stu-id="c75ac-157">Update policy override</span></span>|

## <span data-ttu-id="c75ac-158">Políticas de aplicativos</span><span class="sxs-lookup"><span data-stu-id="c75ac-158">Applications policies</span></span>

[<span data-ttu-id="c75ac-159">Voltar ao início</span><span class="sxs-lookup"><span data-stu-id="c75ac-159">Back to top</span></span>](#microsoft-edge---update-policies)
### <span data-ttu-id="c75ac-160">InstallDefault</span><span class="sxs-lookup"><span data-stu-id="c75ac-160">InstallDefault</span></span>
#### <span data-ttu-id="c75ac-161">Permitir a instalação padrão</span><span class="sxs-lookup"><span data-stu-id="c75ac-161">Allow installation default</span></span>
><span data-ttu-id="c75ac-162">Microsoft Edge Update 1.2.145.5 e posterior</span><span class="sxs-lookup"><span data-stu-id="c75ac-162">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <span data-ttu-id="c75ac-163">Descrição</span><span class="sxs-lookup"><span data-stu-id="c75ac-163">Description</span></span>
<span data-ttu-id="c75ac-164">Você pode especificar o comportamento padrão de todos os canais para permitir ou bloquear o Microsoft Edge em dispositivos associados ao domínio.</span><span class="sxs-lookup"><span data-stu-id="c75ac-164">You can specify the default behavior of all channels to allow or block Microsoft Edge on domain-joined devices.</span></span>

<span data-ttu-id="c75ac-165">Você pode substituir esta política para canais individuais habilitando a política '[Permitir instalação](#install)' para canais específicos.</span><span class="sxs-lookup"><span data-stu-id="c75ac-165">You can override this policy for individual channels by enabling the '[Allow installation](#install)' policy for specific channels.</span></span>

<span data-ttu-id="c75ac-166">Se você desabilitar esta política, a instalação do Microsoft Edge será bloqueada.</span><span class="sxs-lookup"><span data-stu-id="c75ac-166">If you disable this policy, the installation of Microsoft Edge is blocked.</span></span> <span data-ttu-id="c75ac-167">Isso só afeta a instalação do software Microsoft Edge quando a '[Permitir instalação](#install)' está definida como Não configurada.</span><span class="sxs-lookup"><span data-stu-id="c75ac-167">This only affects the installation of Microsoft Edge software when the '[Allow installation](#install)' policy is set to Not Configured.</span></span>

<span data-ttu-id="c75ac-168">Esta política não impede a execução do Microsoft Edge Update, nem impede que os usuários instalem o software do Microsoft Edge por outros métodos.</span><span class="sxs-lookup"><span data-stu-id="c75ac-168">This policy doesn't prevent Microsoft Edge Update from running or prevent users from installing Microsoft Edge software using other methods.</span></span>

<span data-ttu-id="c75ac-169">Esta política está disponível apenas em instâncias do Windows que fazem parte de um domínio Microsoft® Active Directory®.</span><span class="sxs-lookup"><span data-stu-id="c75ac-169">This policy is available only on Windows instances that are joined to a Microsoft® Active Directory® domain.</span></span>
#### <span data-ttu-id="c75ac-170">Informações e configurações do Windows</span><span class="sxs-lookup"><span data-stu-id="c75ac-170">Windows information and settings</span></span>
##### <span data-ttu-id="c75ac-171">Informações da Política de Grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="c75ac-171">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="c75ac-172">Nome exclusivo da Política de Grupo: InstallDefault</span><span class="sxs-lookup"><span data-stu-id="c75ac-172">GP unique name: InstallDefault</span></span>
- <span data-ttu-id="c75ac-173">Nome da Política de Grupo: Permitir a instalação padrão</span><span class="sxs-lookup"><span data-stu-id="c75ac-173">GP name: Allow installation default</span></span>
- <span data-ttu-id="c75ac-174">Caminho da Política Padrão: Modelos Administrativos/Microsoft Edge Update/Aplicativos</span><span class="sxs-lookup"><span data-stu-id="c75ac-174">GP path: Administrative Templates/Microsoft Edge Update/Applications</span></span>
- <span data-ttu-id="c75ac-175">Nome do arquivo GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="c75ac-175">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="c75ac-176">Configurações de registro do Windows</span><span class="sxs-lookup"><span data-stu-id="c75ac-176">Windows Registry Settings</span></span>
- <span data-ttu-id="c75ac-177">Caminho: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="c75ac-177">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="c75ac-178">Nome do valor: InstallDefault</span><span class="sxs-lookup"><span data-stu-id="c75ac-178">Value Name: InstallDefault</span></span>
- <span data-ttu-id="c75ac-179">Tipo de valor: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="c75ac-179">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="c75ac-180">Valor de exemplo:</span><span class="sxs-lookup"><span data-stu-id="c75ac-180">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="c75ac-181">Voltar ao início</span><span class="sxs-lookup"><span data-stu-id="c75ac-181">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="c75ac-182">UpdateDefault</span><span class="sxs-lookup"><span data-stu-id="c75ac-182">UpdateDefault</span></span>
#### <span data-ttu-id="c75ac-183">Atualizar o padrão de substituição de política</span><span class="sxs-lookup"><span data-stu-id="c75ac-183">Update policy override default</span></span>
><span data-ttu-id="c75ac-184">Microsoft Edge Update 1.2.145.5 e posterior</span><span class="sxs-lookup"><span data-stu-id="c75ac-184">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <span data-ttu-id="c75ac-185">Descrição</span><span class="sxs-lookup"><span data-stu-id="c75ac-185">Description</span></span>
<span data-ttu-id="c75ac-186">Permite especificar o comportamento padrão para todos os canais referentes à maneira como o Microsoft Edge Update trata as atualizações disponíveis para o Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="c75ac-186">Lets you specify the default behavior for all channels concerning the way Microsoft Edge Update handles available updates for Microsoft Edge.</span></span> <span data-ttu-id="c75ac-187">Pode ser substituído para canais individuais ao especificar a política '[Atualizar a substituição de política](#update)' para esses canais específicos.</span><span class="sxs-lookup"><span data-stu-id="c75ac-187">Can be overridden for individual channels by specifying the '[Update policy override](#update)' policy for those specific channels.</span></span>

  <span data-ttu-id="c75ac-188">Se você habilitar essa política, o Microsoft Edge Update tratará as atualizações do Microsoft Edge de acordo com as seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="c75ac-188">If you enable this policy, Microsoft Edge Update handles Microsoft Edge updates according to how you configure the following options:</span></span>
   - <span data-ttu-id="c75ac-189">Sempre permitir atualizações: as atualizações sempre serão aplicadas quando forem encontradas por uma verificação de atualização periódica ou por uma verificação de atualização manual.</span><span class="sxs-lookup"><span data-stu-id="c75ac-189">Always allow updates: Updates are always applied when found, either by periodic update check or by a manual update check.</span></span>
   - <span data-ttu-id="c75ac-190">Somente atualizações silenciosas automáticas: as atualizações serão aplicadas somente quando forem encontradas pela verificação de atualização periódica.</span><span class="sxs-lookup"><span data-stu-id="c75ac-190">Automatic silent updates only: Updates are applied only when they're found by the periodic update check.</span></span>
   - <span data-ttu-id="c75ac-191">Somente atualizações manuais: as atualizações serão aplicadas somente quando o usuário executar uma verificação de atualização manual.</span><span class="sxs-lookup"><span data-stu-id="c75ac-191">Manual updates only: Updates are applied only when the user runs a manual update check.</span></span>
   - <span data-ttu-id="c75ac-192">Atualizações desabilitadas: as atualizações nunca serão aplicadas.</span><span class="sxs-lookup"><span data-stu-id="c75ac-192">Updates disabled: Updates are never applied.</span></span>

  <span data-ttu-id="c75ac-193">Se você selecionar atualizações manuais, verifique periodicamente se há atualizações usando o mecanismo de atualizações manuais do aplicativo, se disponível.</span><span class="sxs-lookup"><span data-stu-id="c75ac-193">If you select manual updates, make sure you periodically check for updates by using the app's manual update mechanism, if available.</span></span> <span data-ttu-id="c75ac-194">Se você desabilitar as atualizações, verifique periodicamente se há atualizações e as distribua aos usuários.</span><span class="sxs-lookup"><span data-stu-id="c75ac-194">If you disable updates, periodically check for updates, and distribute them to users.</span></span>

  <span data-ttu-id="c75ac-195">Se você não habilitar e configurar essa política, o Microsoft Edge Update trata as atualizações disponíveis conforme especificado pela política '[Atualizar a substituição de política"](#update)'.</span><span class="sxs-lookup"><span data-stu-id="c75ac-195">If you don't enable and configure this policy, Microsoft Edge Update handles available updates as specified by the '[Update policy override](#update)' policy.</span></span>

  <span data-ttu-id="c75ac-196">Esta política está disponível apenas em instâncias do Windows que fazem parte de um domínio Microsoft® Active Directory®.</span><span class="sxs-lookup"><span data-stu-id="c75ac-196">This policy is available only on Windows instances that are joined to a Microsoft® Active Directory® domain.</span></span>
#### <span data-ttu-id="c75ac-197">Informações e configurações do Windows</span><span class="sxs-lookup"><span data-stu-id="c75ac-197">Windows information and settings</span></span>
##### <span data-ttu-id="c75ac-198">Informações da Política de Grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="c75ac-198">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="c75ac-199">Nome exclusivo da Política de Grupo: UpdateDefault</span><span class="sxs-lookup"><span data-stu-id="c75ac-199">GP unique name: UpdateDefault</span></span>
- <span data-ttu-id="c75ac-200">Nome da Política de Grupo: Atualizar o padrão de substituição de política</span><span class="sxs-lookup"><span data-stu-id="c75ac-200">GP name: Update policy override default</span></span>
- <span data-ttu-id="c75ac-201">Caminho da Política Padrão: Modelos Administrativos/Microsoft Edge Update/Aplicativos</span><span class="sxs-lookup"><span data-stu-id="c75ac-201">GP path: Administrative Templates/Microsoft Edge Update/Applications</span></span>
- <span data-ttu-id="c75ac-202">Nome do arquivo GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="c75ac-202">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="c75ac-203">Configurações de registro do Windows</span><span class="sxs-lookup"><span data-stu-id="c75ac-203">Windows Registry Settings</span></span>
- <span data-ttu-id="c75ac-204">Caminho: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="c75ac-204">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="c75ac-205">Nome do valor: UpdateDefault</span><span class="sxs-lookup"><span data-stu-id="c75ac-205">Value Name: UpdateDefault</span></span>
- <span data-ttu-id="c75ac-206">Tipo de valor: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="c75ac-206">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="c75ac-207">Valor de exemplo:</span><span class="sxs-lookup"><span data-stu-id="c75ac-207">Example value:</span></span>
```
0x00000003
```
[<span data-ttu-id="c75ac-208">Voltar ao início</span><span class="sxs-lookup"><span data-stu-id="c75ac-208">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="c75ac-209">Install</span><span class="sxs-lookup"><span data-stu-id="c75ac-209">Install</span></span>
#### <span data-ttu-id="c75ac-210">Permitir instalação</span><span class="sxs-lookup"><span data-stu-id="c75ac-210">Allow installation</span></span>
><span data-ttu-id="c75ac-211">Microsoft Edge Update 1.2.145.5 e posterior</span><span class="sxs-lookup"><span data-stu-id="c75ac-211">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <span data-ttu-id="c75ac-212">Descrição</span><span class="sxs-lookup"><span data-stu-id="c75ac-212">Description</span></span>
<span data-ttu-id="c75ac-213">Especifica se um canal do Microsoft Edge pode ser instalado em dispositivos ingressados ​​no domínio.</span><span class="sxs-lookup"><span data-stu-id="c75ac-213">Specifies whether a Microsoft Edge channel can be installed on domain-joined devices.</span></span>

  <span data-ttu-id="c75ac-214">Se você habilitar esta política para um canal, o Microsoft Edge não terá sua instalação bloqueada.</span><span class="sxs-lookup"><span data-stu-id="c75ac-214">If you enable this policy for a channel, Microsoft Edge will not be blocked from installation.</span></span>

  <span data-ttu-id="c75ac-215">Se você desabilitar esta política para um canal, o Microsoft Edge será bloqueado para instalação.</span><span class="sxs-lookup"><span data-stu-id="c75ac-215">If you disable this policy for a channel, Microsoft Edge will be blocked from installation.</span></span>

  <span data-ttu-id="c75ac-216">Se você não configurar esta política para um canal, a configuração da política '[Permitir instalação padrão](#installdefault)' determina se os usuários podem instalar esse canal do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="c75ac-216">If you don't configure this policy for a channel, the '[Allow installation default](#installdefault)' policy configuration determines whether users can install that channel of Microsoft Edge.</span></span>

  <span data-ttu-id="c75ac-217">Esta política está disponível apenas em instâncias do Windows que fazem parte de um domínio Microsoft® Active Directory®.</span><span class="sxs-lookup"><span data-stu-id="c75ac-217">This policy is available only on Windows instances that are joined to a Microsoft® Active Directory® domain.</span></span>
#### <span data-ttu-id="c75ac-218">Informações e configurações do Windows</span><span class="sxs-lookup"><span data-stu-id="c75ac-218">Windows information and settings</span></span>
##### <span data-ttu-id="c75ac-219">Informações da Política de Grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="c75ac-219">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="c75ac-220">Nome exclusivo da Política de Grupo: Install</span><span class="sxs-lookup"><span data-stu-id="c75ac-220">GP unique name: Install</span></span>
- <span data-ttu-id="c75ac-221">Nome da Política de Grupo: Permitir instalação</span><span class="sxs-lookup"><span data-stu-id="c75ac-221">GP name: Allow installation</span></span>
- <span data-ttu-id="c75ac-222">Caminho da Política de Grupo:</span><span class="sxs-lookup"><span data-stu-id="c75ac-222">GP path:</span></span> 
  - <span data-ttu-id="c75ac-223">Modelos Administrativos/Microsoft Edge Update/Aplicativos/Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="c75ac-223">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span></span>
  - <span data-ttu-id="c75ac-224">Modelos Administrativos/Microsoft Edge Update/Aplicativos/Microsoft Edge Beta</span><span class="sxs-lookup"><span data-stu-id="c75ac-224">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span></span>
  - <span data-ttu-id="c75ac-225">Modelos Administrativos/Microsoft Edge Update/Aplicativos/Microsoft Edge Canary</span><span class="sxs-lookup"><span data-stu-id="c75ac-225">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span></span>
  - <span data-ttu-id="c75ac-226">Modelos Administrativos/Microsoft Edge Update/Aplicativos/Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="c75ac-226">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span></span>
- <span data-ttu-id="c75ac-227">Nome do arquivo GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="c75ac-227">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="c75ac-228">Configurações de registro do Windows</span><span class="sxs-lookup"><span data-stu-id="c75ac-228">Windows Registry Settings</span></span>
- <span data-ttu-id="c75ac-229">Caminho: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="c75ac-229">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="c75ac-230">Nome do valor:</span><span class="sxs-lookup"><span data-stu-id="c75ac-230">Value Name:</span></span> 
  - <span data-ttu-id="c75ac-231">(Estável): Install{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span><span class="sxs-lookup"><span data-stu-id="c75ac-231">(Stable): Install{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span></span>
  - <span data-ttu-id="c75ac-232">(Beta): Install{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span><span class="sxs-lookup"><span data-stu-id="c75ac-232">(Beta): Install{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span></span>
  - <span data-ttu-id="c75ac-233">(Canary): Install{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span><span class="sxs-lookup"><span data-stu-id="c75ac-233">(Canary): Install{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span></span>
  - <span data-ttu-id="c75ac-234">(Dev): Install{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span><span class="sxs-lookup"><span data-stu-id="c75ac-234">(Dev): Install{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span></span>
- <span data-ttu-id="c75ac-235">Tipo de valor: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="c75ac-235">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="c75ac-236">Valor de exemplo:</span><span class="sxs-lookup"><span data-stu-id="c75ac-236">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="c75ac-237">Voltar ao início</span><span class="sxs-lookup"><span data-stu-id="c75ac-237">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="c75ac-238">Update</span><span class="sxs-lookup"><span data-stu-id="c75ac-238">Update</span></span>
#### <span data-ttu-id="c75ac-239">Atualizar a substituição de política</span><span class="sxs-lookup"><span data-stu-id="c75ac-239">Update policy override</span></span>
><span data-ttu-id="c75ac-240">Microsoft Edge Update 1.2.145.5 e posterior</span><span class="sxs-lookup"><span data-stu-id="c75ac-240">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <span data-ttu-id="c75ac-241">Descrição</span><span class="sxs-lookup"><span data-stu-id="c75ac-241">Description</span></span>
<span data-ttu-id="c75ac-242">Especifica como o Microsoft Edge Update trata as atualizações disponíveis do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="c75ac-242">Specifies how Microsoft Edge Update handles available updates from Microsoft Edge.</span></span>

<span data-ttu-id="c75ac-243">Se você habilitar essa política, o Microsoft Edge Update tratará as atualizações do Microsoft Edge de acordo com as seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="c75ac-243">If you enable this policy, Microsoft Edge Update handles Microsoft Edge updates according to how you configure the following options:</span></span>
  - <span data-ttu-id="c75ac-244">Sempre permitir atualizações: as atualizações sempre serão aplicadas quando forem encontradas por uma verificação de atualização periódica ou por uma verificação de atualização manual.</span><span class="sxs-lookup"><span data-stu-id="c75ac-244">Always allow updates: Updates are always applied when found, either by periodic update check or by a manual update check.</span></span>
  - <span data-ttu-id="c75ac-245">Somente atualizações silenciosas automáticas: as atualizações serão aplicadas somente quando forem encontradas pela verificação de atualização periódica.</span><span class="sxs-lookup"><span data-stu-id="c75ac-245">Automatic silent updates only: Updates are applied only when they're found by the periodic update check.</span></span>
  - <span data-ttu-id="c75ac-246">Somente atualizações manuais: as atualizações serão aplicadas somente quando o usuário executar uma verificação de atualização manual.</span><span class="sxs-lookup"><span data-stu-id="c75ac-246">Manual updates only: Updates are applied only when the user runs a manual update check.</span></span> <span data-ttu-id="c75ac-247">(Nem todos os aplicativos fornecem uma interface para essa opção.)</span><span class="sxs-lookup"><span data-stu-id="c75ac-247">(Not all apps provide an interface for this option.)</span></span>
  - <span data-ttu-id="c75ac-248">Atualizações desabilitadas: as atualizações nunca serão aplicadas.</span><span class="sxs-lookup"><span data-stu-id="c75ac-248">Updates disabled: Updates are never applied.</span></span>

<span data-ttu-id="c75ac-249">Se você selecionar atualizações manuais, verifique periodicamente se há atualizações usando o mecanismo de atualizações manuais do aplicativo, se disponível.</span><span class="sxs-lookup"><span data-stu-id="c75ac-249">If you select manual updates, make sure you periodically check for updates by using the app's manual update mechanism, if available.</span></span> <span data-ttu-id="c75ac-250">Se você desabilitar as atualizações, verifique periodicamente se há atualizações e as distribua aos usuários.</span><span class="sxs-lookup"><span data-stu-id="c75ac-250">If you disable updates, periodically check for updates, and distribute them to users.</span></span>

<span data-ttu-id="c75ac-251">Se você não habilitar e configurar essa política, o Microsoft Edge Update tratará as atualizações disponíveis conforme especificado pela política '[Atualizar a substituição de política padrão](#updatedefault)'.</span><span class="sxs-lookup"><span data-stu-id="c75ac-251">If you don't enable and configure this policy, Microsoft Edge Update handles available updates as specified by the '[Update policy override default](#updatedefault)' policy.</span></span>

<span data-ttu-id="c75ac-252">Consulte [https://go.microsoft.com/fwlink/?linkid=2136406](https://go.microsoft.com/fwlink/?linkid=2136406) para mais informações.</span><span class="sxs-lookup"><span data-stu-id="c75ac-252">See [https://go.microsoft.com/fwlink/?linkid=2136406](https://go.microsoft.com/fwlink/?linkid=2136406) for more information.</span></span>

<span data-ttu-id="c75ac-253">Esta política está disponível apenas em instâncias do Windows que fazem parte de um domínio Microsoft® Active Directory®.</span><span class="sxs-lookup"><span data-stu-id="c75ac-253">This policy is available only on Windows instances that are joined to a Microsoft® Active Directory® domain.</span></span>
#### <span data-ttu-id="c75ac-254">Informações e configurações do Windows</span><span class="sxs-lookup"><span data-stu-id="c75ac-254">Windows information and settings</span></span>
##### <span data-ttu-id="c75ac-255">Informações da Política de Grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="c75ac-255">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="c75ac-256">Nome exclusivo da Política de Grupo: Update</span><span class="sxs-lookup"><span data-stu-id="c75ac-256">GP unique name: Update</span></span>
- <span data-ttu-id="c75ac-257">Nome da Política de Grupo: Atualizar a substituição de política</span><span class="sxs-lookup"><span data-stu-id="c75ac-257">GP name: Update policy override</span></span>
- <span data-ttu-id="c75ac-258">Caminho da Política de Grupo:</span><span class="sxs-lookup"><span data-stu-id="c75ac-258">GP path:</span></span> 
  - <span data-ttu-id="c75ac-259">Modelos Administrativos/Microsoft Edge Update/Aplicativos/Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="c75ac-259">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span></span>
  - <span data-ttu-id="c75ac-260">Modelos Administrativos/Microsoft Edge Update/Aplicativos/Microsoft Edge Beta</span><span class="sxs-lookup"><span data-stu-id="c75ac-260">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span></span>
  - <span data-ttu-id="c75ac-261">Modelos Administrativos/Microsoft Edge Update/Aplicativos/Microsoft Edge Canary</span><span class="sxs-lookup"><span data-stu-id="c75ac-261">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span></span>
  - <span data-ttu-id="c75ac-262">Modelos Administrativos/Microsoft Edge Update/Aplicativos/Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="c75ac-262">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span></span>
- <span data-ttu-id="c75ac-263">Nome do arquivo GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="c75ac-263">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="c75ac-264">Configurações de registro do Windows</span><span class="sxs-lookup"><span data-stu-id="c75ac-264">Windows Registry Settings</span></span>
- <span data-ttu-id="c75ac-265">Caminho: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="c75ac-265">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="c75ac-266">Nome do valor:</span><span class="sxs-lookup"><span data-stu-id="c75ac-266">Value Name:</span></span> 
  - <span data-ttu-id="c75ac-267">(Estável): Update{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span><span class="sxs-lookup"><span data-stu-id="c75ac-267">(Stable): Update{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span></span>
  - <span data-ttu-id="c75ac-268">(Beta): Update{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span><span class="sxs-lookup"><span data-stu-id="c75ac-268">(Beta): Update{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span></span>
  - <span data-ttu-id="c75ac-269">(Canary): Update{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span><span class="sxs-lookup"><span data-stu-id="c75ac-269">(Canary): Update{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span></span>
  - <span data-ttu-id="c75ac-270">(Dev): Update{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span><span class="sxs-lookup"><span data-stu-id="c75ac-270">(Dev): Update{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span></span>
- <span data-ttu-id="c75ac-271">Tipo de valor: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="c75ac-271">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="c75ac-272">Valor de exemplo:</span><span class="sxs-lookup"><span data-stu-id="c75ac-272">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="c75ac-273">Voltar ao início</span><span class="sxs-lookup"><span data-stu-id="c75ac-273">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="c75ac-274">Allowsxs</span><span class="sxs-lookup"><span data-stu-id="c75ac-274">Allowsxs</span></span>
#### <span data-ttu-id="c75ac-275">Permitir a experiência de navegador Lado a Lado do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="c75ac-275">Allow Microsoft Edge Side by Side browser experience</span></span>
><span data-ttu-id="c75ac-276">Microsoft Edge Update 1.2.145.5 e posterior</span><span class="sxs-lookup"><span data-stu-id="c75ac-276">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <span data-ttu-id="c75ac-277">Description</span><span class="sxs-lookup"><span data-stu-id="c75ac-277">Description</span></span>
<span data-ttu-id="c75ac-278">Essa política permite que um usuário execute o Microsoft Edge (Edge HTML) e o Microsoft Edge (baseado no Chromium) lado a lado.</span><span class="sxs-lookup"><span data-stu-id="c75ac-278">This policy lets a user run Microsoft Edge (Edge HTML) and Microsoft Edge (Chromium-based) side-by-side.</span></span>

<span data-ttu-id="c75ac-279">Se essa política for definida como "Não configurada", o Microsoft Edge (baseado no Chromium) substituirá o Microsoft Edge (HTML do Edge) depois que o canal Estável do Microsoft Edge (baseado no Chromium) e as atualizações de segurança de novembro de 2019 forem instalados.</span><span class="sxs-lookup"><span data-stu-id="c75ac-279">If this policy is set to “Not configured”, Microsoft Edge (Chromium-based) will replace Microsoft Edge (Edge HTML) after the Microsoft Edge (Chromium-based) stable channel and the November 2019 security updates are installed.</span></span>  <span data-ttu-id="c75ac-280">Esse comportamento é igual à configuração "Desabilitada".</span><span class="sxs-lookup"><span data-stu-id="c75ac-280">This is the same behavior as the “Disabled” setting.</span></span>

<span data-ttu-id="c75ac-281">A configuração "Desabilitada" bloqueia uma experiência lado a lado, e o Microsoft Edge (baseado no Chromium) substituirá o Microsoft Edge (HTML do Edge) depois que o canal Estável do Microsoft Edge (baseado no Chromium) e as atualizações de segurança de novembro de 2019 forem instalados.</span><span class="sxs-lookup"><span data-stu-id="c75ac-281">The “Disabled” setting blocks a side-by-side experience and Microsoft Edge (Chromium-based) will replace Microsoft Edge (Edge HTML) after the Microsoft Edge (Chromium-based) stable channel and the November 2019 security updates are installed.</span></span>  <span data-ttu-id="c75ac-282">Esse comportamento é igual à configuração "Não configurada".</span><span class="sxs-lookup"><span data-stu-id="c75ac-282">This is the same behavior as the “Not Configured” setting.</span></span>

<span data-ttu-id="c75ac-283">Quando essa política for "Habilitada", o Microsoft Edge (baseado no Chromium) e o Microsoft Edge (Edge HTML) poderão ser executados lado a lado depois que o Microsoft Edge (baseado no Chromium) for instalado.</span><span class="sxs-lookup"><span data-stu-id="c75ac-283">When this policy is “Enabled”, Microsoft Edge (Chromium-based) and Microsoft Edge (Edge HTML) can run side-by-side after Microsoft Edge (Chromium-based) is installed.</span></span>

<span data-ttu-id="c75ac-284">Para que essa política de grupo entre em vigor, ela deve ser configurada antes da instalação automática do Microsoft Edge (baseado no Chromium) pelo Windows Update.</span><span class="sxs-lookup"><span data-stu-id="c75ac-284">For this group policy to take affect, it must be configured before the automatic install of Microsoft Edge (Chromium-based) by Windows Update.</span></span> <span data-ttu-id="c75ac-285">Observação: um usuário pode bloquear a atualização automática do Microsoft Edge (baseado no Chromium) usando o kit de ferramentas do bloqueador do Microsoft Edge (baseado no Chromium).</span><span class="sxs-lookup"><span data-stu-id="c75ac-285">Note: A user can block the automatic update of Microsoft Edge (Chromium-based) by using the Microsoft Edge (Chromium-based) Blocker Toolkit.</span></span>
#### <span data-ttu-id="c75ac-286">Informações e configurações do Windows</span><span class="sxs-lookup"><span data-stu-id="c75ac-286">Windows information and settings</span></span>
##### <span data-ttu-id="c75ac-287">Informações da Política de Grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="c75ac-287">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="c75ac-288">Nome exclusivo da Política de Grupo: Allowsxs</span><span class="sxs-lookup"><span data-stu-id="c75ac-288">GP unique name: Allowsxs</span></span>
- <span data-ttu-id="c75ac-289">Nome da Política de Grupo: Permitir a experiência de navegador Lado a Lado do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="c75ac-289">GP name: Allow Microsoft Edge Side by Side browser experience</span></span>
- <span data-ttu-id="c75ac-290">Caminho da Política Padrão: Modelos Administrativos/Microsoft Edge Update/Aplicativos</span><span class="sxs-lookup"><span data-stu-id="c75ac-290">GP path: Administrative Templates/Microsoft Edge Update/Applications</span></span>
- <span data-ttu-id="c75ac-291">Nome do arquivo GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="c75ac-291">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="c75ac-292">Configurações de registro do Windows</span><span class="sxs-lookup"><span data-stu-id="c75ac-292">Windows Registry Settings</span></span>
- <span data-ttu-id="c75ac-293">Caminho: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="c75ac-293">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="c75ac-294">Nome do valor:Allowsxs</span><span class="sxs-lookup"><span data-stu-id="c75ac-294">Value Name: Allowsxs</span></span>
- <span data-ttu-id="c75ac-295">Tipo de valor: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="c75ac-295">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="c75ac-296">Valor de exemplo:</span><span class="sxs-lookup"><span data-stu-id="c75ac-296">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="c75ac-297">Voltar ao início</span><span class="sxs-lookup"><span data-stu-id="c75ac-297">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="c75ac-298">CreateDesktopShortcutDefault</span><span class="sxs-lookup"><span data-stu-id="c75ac-298">CreateDesktopShortcutDefault</span></span>
#### <span data-ttu-id="c75ac-299">Impedir a criação de Atalho da Área de Trabalho com a instalação padrão</span><span class="sxs-lookup"><span data-stu-id="c75ac-299">Prevent Desktop Shortcut creation upon install default</span></span>
><span data-ttu-id="c75ac-300">Microsoft Edge Update 1.3.128.0 e posterior</span><span class="sxs-lookup"><span data-stu-id="c75ac-300">Microsoft Edge Update 1.3.128.0 and later</span></span>

#### <span data-ttu-id="c75ac-301">Descrição</span><span class="sxs-lookup"><span data-stu-id="c75ac-301">Description</span></span>
<span data-ttu-id="c75ac-302">Permite especificar o comportamento padrão de todos os canais para criar um atalho da área de trabalho quando o Microsoft Edge for instalado.</span><span class="sxs-lookup"><span data-stu-id="c75ac-302">Lets you specify the default behavior for all channels for creating a desktop shortcut when Microsoft Edge is installed.</span></span>

  <span data-ttu-id="c75ac-303">Se você habilitar esta política, um atalho da área de trabalho será criado quando o Microsoft Edge for instalado.</span><span class="sxs-lookup"><span data-stu-id="c75ac-303">If you enable this policy a desktop shortcut is created when Microsoft Edge is installed.</span></span>
<span data-ttu-id="c75ac-304">Se você desabilitar esta política, nenhum atalho da área de trabalho será criado quando o Microsoft Edge for instalado.</span><span class="sxs-lookup"><span data-stu-id="c75ac-304">If you disable this policy, no desktop shortcut will be created when Microsoft Edge is installed.</span></span>
<span data-ttu-id="c75ac-305">Se você não configurar esta política, um atalho da área de trabalho para o Microsoft Edge será criado durante a instalação.</span><span class="sxs-lookup"><span data-stu-id="c75ac-305">If you don’t configure this policy a desktop shortcut to Microsoft Edge will be created during installation.</span></span>
<span data-ttu-id="c75ac-306">Se o Microsoft Edge já estiver instalado, esta política não terá efeito.</span><span class="sxs-lookup"><span data-stu-id="c75ac-306">If Microsoft Edge is already installed, this policy will have no effect.</span></span>
#### <span data-ttu-id="c75ac-307">Informações e configurações do Windows</span><span class="sxs-lookup"><span data-stu-id="c75ac-307">Windows information and settings</span></span>
##### <span data-ttu-id="c75ac-308">Informações da Política de Grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="c75ac-308">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="c75ac-309">Nome exclusivo da Política de Grupo: CreateDesktopShortcutDefault</span><span class="sxs-lookup"><span data-stu-id="c75ac-309">GP unique name: CreateDesktopShortcutDefault</span></span>
- <span data-ttu-id="c75ac-310">Nome da Política de Grupo: Impedir a criação de Atalho da Área de Trabalho com a instalação padrão</span><span class="sxs-lookup"><span data-stu-id="c75ac-310">GP name: Prevent Desktop Shortcut creation upon install default</span></span>
- <span data-ttu-id="c75ac-311">Caminho da Política Padrão: Modelos Administrativos/Microsoft Edge Update/Aplicativos</span><span class="sxs-lookup"><span data-stu-id="c75ac-311">GP path: Administrative Templates/Microsoft Edge Update/Applications</span></span>
- <span data-ttu-id="c75ac-312">Nome do arquivo GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="c75ac-312">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="c75ac-313">Configurações de registro do Windows</span><span class="sxs-lookup"><span data-stu-id="c75ac-313">Windows Registry Settings</span></span>
- <span data-ttu-id="c75ac-314">Caminho: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="c75ac-314">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="c75ac-315">Nome do Valor: CreateDesktopShortcutDefault</span><span class="sxs-lookup"><span data-stu-id="c75ac-315">Value Name: CreateDesktopShortcutDefault</span></span>
- <span data-ttu-id="c75ac-316">Tipo de valor: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="c75ac-316">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="c75ac-317">Valor de exemplo:</span><span class="sxs-lookup"><span data-stu-id="c75ac-317">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="c75ac-318">Voltar ao início</span><span class="sxs-lookup"><span data-stu-id="c75ac-318">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="c75ac-319">CreateDesktopShortcut</span><span class="sxs-lookup"><span data-stu-id="c75ac-319">CreateDesktopShortcut</span></span>
#### <span data-ttu-id="c75ac-320">Impedir a criação de Atalho da Área de Trabalho com a instalação</span><span class="sxs-lookup"><span data-stu-id="c75ac-320">Prevent Desktop Shortcut creation upon install</span></span>
><span data-ttu-id="c75ac-321">Microsoft Edge Update 1.3.128.0 e posterior</span><span class="sxs-lookup"><span data-stu-id="c75ac-321">Microsoft Edge Update 1.3.128.0 and later</span></span>

#### <span data-ttu-id="c75ac-322">Descrição</span><span class="sxs-lookup"><span data-stu-id="c75ac-322">Description</span></span>
<span data-ttu-id="c75ac-323">Se você habilitar esta política, um atalho da área de trabalho será criado quando o Microsoft Edge for instalado.</span><span class="sxs-lookup"><span data-stu-id="c75ac-323">If you enable this policy a desktop shortcut is created when Microsoft Edge is installed.</span></span>
<span data-ttu-id="c75ac-324">Se você desabilitar esta política, nenhum atalho da área de trabalho será criado quando o Microsoft Edge for instalado.</span><span class="sxs-lookup"><span data-stu-id="c75ac-324">If you disable this policy, no desktop shortcut will be created when Microsoft Edge is installed.</span></span>
<span data-ttu-id="c75ac-325">Se você não configurar esta política, um atalho da área de trabalho para o Microsoft Edge será criado durante a instalação.</span><span class="sxs-lookup"><span data-stu-id="c75ac-325">If you don’t configure this policy a desktop shortcut to Microsoft Edge will be created during installation.</span></span>
<span data-ttu-id="c75ac-326">Se o Microsoft Edge já estiver instalado, esta política não terá efeito.</span><span class="sxs-lookup"><span data-stu-id="c75ac-326">If Microsoft Edge is already installed, this policy will have no effect.</span></span>

  <span data-ttu-id="c75ac-327">Se você não configurar esta política para um canal, a configuração de política padrão '[Evitar a criação de um Atalho no Desktop ao instalar](#createdesktopshortcutdefault)' determinará a criação de um atalho quando o Microsoft Edge for instalado.</span><span class="sxs-lookup"><span data-stu-id="c75ac-327">If you don't configure this policy for a channel, the '[Prevent Desktop Shortcut creation upon install default](#createdesktopshortcutdefault)' policy configuration determines shortcut creation when Microsoft Edge is installed.</span></span>
#### <span data-ttu-id="c75ac-328">Informações e configurações do Windows</span><span class="sxs-lookup"><span data-stu-id="c75ac-328">Windows information and settings</span></span>
##### <span data-ttu-id="c75ac-329">Informações da Política de Grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="c75ac-329">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="c75ac-330">Nome exclusivo da Política de Grupo: CreateDesktopShortcut</span><span class="sxs-lookup"><span data-stu-id="c75ac-330">GP unique name: CreateDesktopShortcut</span></span>
- <span data-ttu-id="c75ac-331">Nome da GP: Impedir a criação de Atalho da Área de Trabalho com a instalação</span><span class="sxs-lookup"><span data-stu-id="c75ac-331">GP name: Prevent Desktop Shortcut creation upon install</span></span>
- <span data-ttu-id="c75ac-332">Caminho da Política de Grupo:</span><span class="sxs-lookup"><span data-stu-id="c75ac-332">GP path:</span></span> 
  - <span data-ttu-id="c75ac-333">Modelos Administrativos/Microsoft Edge Update/Aplicativos/Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="c75ac-333">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span></span>
  - <span data-ttu-id="c75ac-334">Modelos Administrativos/Microsoft Edge Update/Aplicativos/Microsoft Edge Beta</span><span class="sxs-lookup"><span data-stu-id="c75ac-334">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span></span>
  - <span data-ttu-id="c75ac-335">Modelos Administrativos/Microsoft Edge Update/Aplicativos/Microsoft Edge Canary</span><span class="sxs-lookup"><span data-stu-id="c75ac-335">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span></span>
  - <span data-ttu-id="c75ac-336">Modelos Administrativos/Microsoft Edge Update/Aplicativos/Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="c75ac-336">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span></span>
- <span data-ttu-id="c75ac-337">Nome do arquivo GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="c75ac-337">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="c75ac-338">Configurações de registro do Windows</span><span class="sxs-lookup"><span data-stu-id="c75ac-338">Windows Registry Settings</span></span>
- <span data-ttu-id="c75ac-339">Caminho: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="c75ac-339">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="c75ac-340">Nome do valor:</span><span class="sxs-lookup"><span data-stu-id="c75ac-340">Value Name:</span></span> 
  - <span data-ttu-id="c75ac-341">(Estável): CreateDesktopShortcut{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span><span class="sxs-lookup"><span data-stu-id="c75ac-341">(Stable): CreateDesktopShortcut{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span></span>
  - <span data-ttu-id="c75ac-342">(Beta): CreateDesktopShortcut{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span><span class="sxs-lookup"><span data-stu-id="c75ac-342">(Beta): CreateDesktopShortcut{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span></span>
  - <span data-ttu-id="c75ac-343">(Canary): CreateDesktopShortcut{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span><span class="sxs-lookup"><span data-stu-id="c75ac-343">(Canary): CreateDesktopShortcut{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span></span>
  - <span data-ttu-id="c75ac-344">(Dev): CreateDesktopShortcut{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span><span class="sxs-lookup"><span data-stu-id="c75ac-344">(Dev): CreateDesktopShortcut{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span></span>
- <span data-ttu-id="c75ac-345">Tipo de valor: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="c75ac-345">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="c75ac-346">Valor de exemplo:</span><span class="sxs-lookup"><span data-stu-id="c75ac-346">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="c75ac-347">Voltar ao início</span><span class="sxs-lookup"><span data-stu-id="c75ac-347">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="c75ac-348">RollbackToTargetVersion</span><span class="sxs-lookup"><span data-stu-id="c75ac-348">RollbackToTargetVersion</span></span>
#### <span data-ttu-id="c75ac-349">Reverter para a Versão de Destino</span><span class="sxs-lookup"><span data-stu-id="c75ac-349">Rollback to Target version</span></span>
><span data-ttu-id="c75ac-350">Microsoft Edge Update 1.3.133.3 e posterior</span><span class="sxs-lookup"><span data-stu-id="c75ac-350">Microsoft Edge Update 1.3.133.3 and later</span></span>

#### <span data-ttu-id="c75ac-351">Descrição</span><span class="sxs-lookup"><span data-stu-id="c75ac-351">Description</span></span>
<span data-ttu-id="c75ac-352">Especifica que o Microsoft Edge Update deve reverter as instalações do Microsoft Edge para a versão indicada em '[Substituição da versão de destino](#targetversionprefix)'.</span><span class="sxs-lookup"><span data-stu-id="c75ac-352">Specifies that Microsoft Edge Update should rollback installations of Microsoft Edge to the version indicated in '[Target version override](#targetversionprefix)'.</span></span>

<span data-ttu-id="c75ac-353">Esta política não tem efeito a menos que '[Substituição da versão de destino](#targetversionprefix)' seja definida e '[Substituição da política de atualização](#update)' seja definida como um dos estados ATIVADO (Sempre permitir atualizações, Somente atualizações automáticas silenciosas, Somente atualizações manuais).</span><span class="sxs-lookup"><span data-stu-id="c75ac-353">This policy has no effect unless '[Target version override](#targetversionprefix)' is set and '[Update policy override](#update)' is set to one of the ON states (Always allow updates, Automatic silent updates only, Manual updates only).</span></span>

<span data-ttu-id="c75ac-354">Se você desabilitar esta política ou não configurá-la, as instalações que possuem uma versão superior à especificada pela '[Substituição da versão de destino](#targetversionprefix)' serão deixadas como estão.</span><span class="sxs-lookup"><span data-stu-id="c75ac-354">If you disable this policy or don't configure it, installs that have a version higher than that specified by '[Target version override](#targetversionprefix)' will be left as-is.</span></span>

<span data-ttu-id="c75ac-355">Se você habilitar esta política, as instalações que possuem uma versão atual superior à especificada pela '[Substituição da versão de destino](#targetversionprefix)' serão desatualizadas para a versão de destino.</span><span class="sxs-lookup"><span data-stu-id="c75ac-355">If you enable this policy, installs that have a current version higher than specified by the '[Target version override](#targetversionprefix)' will be downgraded to the target version.</span></span>

<span data-ttu-id="c75ac-356">Recomendamos que os usuários instalem a versão mais recente do navegador Microsoft Edge para garantir a proteção pelas atualizações de segurança mais recentes.</span><span class="sxs-lookup"><span data-stu-id="c75ac-356">We recommend that users install the latest version of the Microsoft Edge browser to ensure protection by the latest security updates.</span></span> <span data-ttu-id="c75ac-357">Reverter para uma versão anterior corre o perigo de se expor aos problemas de segurança conhecidos.</span><span class="sxs-lookup"><span data-stu-id="c75ac-357">Rollback to an earlier version risks exposure to known security issues.</span></span> <span data-ttu-id="c75ac-358">Esta política deve ser usada como uma correção temporária para resolver problemas em uma atualização do navegador Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="c75ac-358">This policy is meant to be used as a temporary fix to address issues in a Microsoft Edge browser update.</span></span>

<span data-ttu-id="c75ac-359">Antes de reverter temporariamente a versão do seu navegador, recomendamos que você ative a Sincronização ([https://go.microsoft.com/fwlink/?linkid=2133032](https://go.microsoft.com/fwlink/?linkid=2133032)) para todos os usuários em sua organização.</span><span class="sxs-lookup"><span data-stu-id="c75ac-359">Before temporarily rolling back your browser version, we recommend that you turn on Sync ([https://go.microsoft.com/fwlink/?linkid=2133032](https://go.microsoft.com/fwlink/?linkid=2133032)) for all users in your organization.</span></span> <span data-ttu-id="c75ac-360">Se você não ativar a Sincronização, existe o risco de perda permanente de dados de navegação.</span><span class="sxs-lookup"><span data-stu-id="c75ac-360">If you don't turn on Sync, there is a risk of permanent browsing data loss.</span></span> <span data-ttu-id="c75ac-361">Use esta política por sua conta e risco.</span><span class="sxs-lookup"><span data-stu-id="c75ac-361">Use this policy at your own risk.</span></span>

<span data-ttu-id="c75ac-362">Nota: Todas as versões disponíveis para reversão podem ser vistas aqui [https://aka.ms/EdgeEnterprise](https://aka.ms/EdgeEnterprise).</span><span class="sxs-lookup"><span data-stu-id="c75ac-362">Note: All versions available for rollback can be viewed here [https://aka.ms/EdgeEnterprise](https://aka.ms/EdgeEnterprise).</span></span>

<span data-ttu-id="c75ac-363">Esta política se aplica ao Microsoft Edge versão 86 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="c75ac-363">This policy applies to Microsoft Edge version 86 or later.</span></span>

<span data-ttu-id="c75ac-364">Consulte [https://go.microsoft.com/fwlink/?linkid=2133918](https://go.microsoft.com/fwlink/?linkid=2133918) para mais informações.</span><span class="sxs-lookup"><span data-stu-id="c75ac-364">See [https://go.microsoft.com/fwlink/?linkid=2133918](https://go.microsoft.com/fwlink/?linkid=2133918) for more information.</span></span>

<span data-ttu-id="c75ac-365">Esta política está disponível apenas em instâncias do Windows que fazem parte de um domínio Microsoft® Active Directory®.</span><span class="sxs-lookup"><span data-stu-id="c75ac-365">This policy is available only on Windows instances that are joined to a Microsoft® Active Directory® domain.</span></span>
#### <span data-ttu-id="c75ac-366">Informações e configurações do Windows</span><span class="sxs-lookup"><span data-stu-id="c75ac-366">Windows information and settings</span></span>
##### <span data-ttu-id="c75ac-367">Informações da Política de Grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="c75ac-367">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="c75ac-368">Nome exclusivo da GP: RollbackToTargetVersion</span><span class="sxs-lookup"><span data-stu-id="c75ac-368">GP unique name: RollbackToTargetVersion</span></span>
- <span data-ttu-id="c75ac-369">Nome da GP: Reverter para a Versão de Destino</span><span class="sxs-lookup"><span data-stu-id="c75ac-369">GP name: Rollback to Target version</span></span>
- <span data-ttu-id="c75ac-370">Caminho da Política de Grupo:</span><span class="sxs-lookup"><span data-stu-id="c75ac-370">GP path:</span></span> 
  - <span data-ttu-id="c75ac-371">Modelos Administrativos/Microsoft Edge Update/Aplicativos/Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="c75ac-371">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span></span>
  - <span data-ttu-id="c75ac-372">Modelos Administrativos/Microsoft Edge Update/Aplicativos/Microsoft Edge Beta</span><span class="sxs-lookup"><span data-stu-id="c75ac-372">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span></span>
  - <span data-ttu-id="c75ac-373">Modelos Administrativos/Microsoft Edge Update/Aplicativos/Microsoft Edge Canary</span><span class="sxs-lookup"><span data-stu-id="c75ac-373">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span></span>
  - <span data-ttu-id="c75ac-374">Modelos Administrativos/Microsoft Edge Update/Aplicativos/Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="c75ac-374">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span></span>
- <span data-ttu-id="c75ac-375">Nome do arquivo GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="c75ac-375">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="c75ac-376">Configurações de registro do Windows</span><span class="sxs-lookup"><span data-stu-id="c75ac-376">Windows Registry Settings</span></span>
- <span data-ttu-id="c75ac-377">Caminho: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="c75ac-377">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="c75ac-378">Nome do valor:</span><span class="sxs-lookup"><span data-stu-id="c75ac-378">Value Name:</span></span> 
  - <span data-ttu-id="c75ac-379">(Estável): RollbackToTargetVersion{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span><span class="sxs-lookup"><span data-stu-id="c75ac-379">(Stable): RollbackToTargetVersion{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span></span>
  - <span data-ttu-id="c75ac-380">(Beta): RollbackToTargetVersion{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span><span class="sxs-lookup"><span data-stu-id="c75ac-380">(Beta): RollbackToTargetVersion{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span></span>
  - <span data-ttu-id="c75ac-381">(Canário): RollbackToTargetVersion{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span><span class="sxs-lookup"><span data-stu-id="c75ac-381">(Canary): RollbackToTargetVersion{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span></span>
  - <span data-ttu-id="c75ac-382">(Dev): RollbackToTargetVersion{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span><span class="sxs-lookup"><span data-stu-id="c75ac-382">(Dev): RollbackToTargetVersion{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span></span>
- <span data-ttu-id="c75ac-383">Tipo de valor: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="c75ac-383">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="c75ac-384">Valor de exemplo:</span><span class="sxs-lookup"><span data-stu-id="c75ac-384">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="c75ac-385">Voltar ao início</span><span class="sxs-lookup"><span data-stu-id="c75ac-385">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="c75ac-386">TargetVersionPrefix</span><span class="sxs-lookup"><span data-stu-id="c75ac-386">TargetVersionPrefix</span></span>
#### <span data-ttu-id="c75ac-387">Substituir versão de destino</span><span class="sxs-lookup"><span data-stu-id="c75ac-387">Target version override</span></span>
><span data-ttu-id="c75ac-388">Microsoft Edge Update 1.3.119.43 e posterior</span><span class="sxs-lookup"><span data-stu-id="c75ac-388">Microsoft Edge Update 1.3.119.43 and later</span></span>

#### <span data-ttu-id="c75ac-389">Descrição</span><span class="sxs-lookup"><span data-stu-id="c75ac-389">Description</span></span>
<span data-ttu-id="c75ac-390">Quando esta política estiver habilitada e a atualização automática estiver habilitada, o Microsoft Edge será atualizado para a versão especificada por esse valor de política.</span><span class="sxs-lookup"><span data-stu-id="c75ac-390">When this policy is enabled, and auto-update is enabled, Microsoft Edge will be updated to the version specified by this policy value.</span></span>

<span data-ttu-id="c75ac-391">O valor da política deve ser uma versão do Microsoft Edge específica, por exemplo, 83.0.499.12.</span><span class="sxs-lookup"><span data-stu-id="c75ac-391">The policy value must be a specific Microsoft Edge version, e.g. 83.0.499.12.</span></span>

<span data-ttu-id="c75ac-392">Se um dispositivo tiver uma versão mais recente do Microsoft Edge do que o valor especificado, a versão mais recente do Microsoft Edge será mantida e ele não será revertido para a versão especificada.</span><span class="sxs-lookup"><span data-stu-id="c75ac-392">If a device has newer version of Microsoft Edge than the value specified, Microsoft Edge will remain on the newer version and not downgrade to the specified version.</span></span>

<span data-ttu-id="c75ac-393">Se a versão especificada não existir ou estiver formatada inadequadamente, o Microsoft Edge permanecerá na versão atual e não será atualizado para versões futuras automaticamente.</span><span class="sxs-lookup"><span data-stu-id="c75ac-393">If the specified version does not exist, or is improperly formatted, then Microsoft Edge will remain on its current version and not update to future versions automatically.</span></span>

<span data-ttu-id="c75ac-394">Consulte [https://go.microsoft.com/fwlink/?linkid=2136707](https://go.microsoft.com/fwlink/?linkid=2136707) para mais informações.</span><span class="sxs-lookup"><span data-stu-id="c75ac-394">See [https://go.microsoft.com/fwlink/?linkid=2136707](https://go.microsoft.com/fwlink/?linkid=2136707) for more information.</span></span>

<span data-ttu-id="c75ac-395">Esta política está disponível apenas em instâncias do Windows que fazem parte de um domínio Microsoft® Active Directory®.</span><span class="sxs-lookup"><span data-stu-id="c75ac-395">This policy is available only on Windows instances that are joined to a Microsoft® Active Directory® domain.</span></span>
#### <span data-ttu-id="c75ac-396">Informações e configurações do Windows</span><span class="sxs-lookup"><span data-stu-id="c75ac-396">Windows information and settings</span></span>
##### <span data-ttu-id="c75ac-397">Informações da Política de Grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="c75ac-397">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="c75ac-398">Nome exclusivo da Política de Grupo: TargetVersionPrefix</span><span class="sxs-lookup"><span data-stu-id="c75ac-398">GP unique name: TargetVersionPrefix</span></span>
- <span data-ttu-id="c75ac-399">Nome da Política de Grupo: Substituir versão de destino</span><span class="sxs-lookup"><span data-stu-id="c75ac-399">GP name: Target version override</span></span>
- <span data-ttu-id="c75ac-400">Caminho da Política de Grupo:</span><span class="sxs-lookup"><span data-stu-id="c75ac-400">GP path:</span></span> 
  - <span data-ttu-id="c75ac-401">Modelos Administrativos/Microsoft Edge Update/Aplicativos/Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="c75ac-401">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span></span>
  - <span data-ttu-id="c75ac-402">Modelos Administrativos/Microsoft Edge Update/Aplicativos/Microsoft Edge Beta</span><span class="sxs-lookup"><span data-stu-id="c75ac-402">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span></span>
  - <span data-ttu-id="c75ac-403">Modelos Administrativos/Microsoft Edge Update/Aplicativos/Microsoft Edge Canary</span><span class="sxs-lookup"><span data-stu-id="c75ac-403">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span></span>
  - <span data-ttu-id="c75ac-404">Modelos Administrativos/Microsoft Edge Update/Aplicativos/Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="c75ac-404">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span></span>
- <span data-ttu-id="c75ac-405">Nome do arquivo GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="c75ac-405">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="c75ac-406">Configurações de registro do Windows</span><span class="sxs-lookup"><span data-stu-id="c75ac-406">Windows Registry Settings</span></span>
- <span data-ttu-id="c75ac-407">Caminho: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="c75ac-407">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="c75ac-408">Nome do valor:</span><span class="sxs-lookup"><span data-stu-id="c75ac-408">Value Name:</span></span> 
  - <span data-ttu-id="c75ac-409">(Estável): TargetVersionPrefix {56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span><span class="sxs-lookup"><span data-stu-id="c75ac-409">(Stable): TargetVersionPrefix{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span></span>
  - <span data-ttu-id="c75ac-410">(Beta): TargetVersionPrefix {2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span><span class="sxs-lookup"><span data-stu-id="c75ac-410">(Beta): TargetVersionPrefix{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span></span>
  - <span data-ttu-id="c75ac-411">(Canary): TargetVersionPrefix {65C35B14-6C1D-4122-AC46-7148CC9D6497}</span><span class="sxs-lookup"><span data-stu-id="c75ac-411">(Canary): TargetVersionPrefix{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span></span>
  - <span data-ttu-id="c75ac-412">(Dev): TargetVersionPrefix {0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span><span class="sxs-lookup"><span data-stu-id="c75ac-412">(Dev): TargetVersionPrefix{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span></span>
- <span data-ttu-id="c75ac-413">Tipo do valor: REG_SZ</span><span class="sxs-lookup"><span data-stu-id="c75ac-413">Value Type: REG_SZ</span></span>
##### <span data-ttu-id="c75ac-414">Valor de exemplo:</span><span class="sxs-lookup"><span data-stu-id="c75ac-414">Example value:</span></span>
```
83.0.499.12
```
[<span data-ttu-id="c75ac-415">Voltar ao início</span><span class="sxs-lookup"><span data-stu-id="c75ac-415">Back to top</span></span>](#microsoft-edge---update-policies)


## <span data-ttu-id="c75ac-416">Políticas de preferências</span><span class="sxs-lookup"><span data-stu-id="c75ac-416">Preferences policies</span></span>

[<span data-ttu-id="c75ac-417">Voltar ao início</span><span class="sxs-lookup"><span data-stu-id="c75ac-417">Back to top</span></span>](#microsoft-edge---update-policies)
### <span data-ttu-id="c75ac-418">AutoUpdateCheckPeriodMinutes</span><span class="sxs-lookup"><span data-stu-id="c75ac-418">AutoUpdateCheckPeriodMinutes</span></span>
#### <span data-ttu-id="c75ac-419">Atualizar automaticamente a substituição do período de verificação</span><span class="sxs-lookup"><span data-stu-id="c75ac-419">Auto-update check period override</span></span>
><span data-ttu-id="c75ac-420">Microsoft Edge Update 1.2.145.5 e posterior</span><span class="sxs-lookup"><span data-stu-id="c75ac-420">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <span data-ttu-id="c75ac-421">Descrição</span><span class="sxs-lookup"><span data-stu-id="c75ac-421">Description</span></span>
<span data-ttu-id="c75ac-422">Se habilitada, essa política permite definir um valor para o número mínimo de minutos entre as verificações de atualização automática.</span><span class="sxs-lookup"><span data-stu-id="c75ac-422">If enabled, this policy lets you set a value for the minimum number of minutes between automatic update checks.</span></span> <span data-ttu-id="c75ac-423">Caso contrário, por padrão, a verificação de atualização automática verifica se há as atualizações a cada 10 horas.</span><span class="sxs-lookup"><span data-stu-id="c75ac-423">Otherwise, by default, auto-update checks for updates every 10 hours.</span></span>

  <span data-ttu-id="c75ac-424">Se você quiser desabilitar todas as verificações de atualização automática, defina o valor como 0 (não recomendado).</span><span class="sxs-lookup"><span data-stu-id="c75ac-424">If you want to disable all auto-update checks, set the value to 0 (not recommended).</span></span>
#### <span data-ttu-id="c75ac-425">Informações e configurações do Windows</span><span class="sxs-lookup"><span data-stu-id="c75ac-425">Windows information and settings</span></span>
##### <span data-ttu-id="c75ac-426">Informações da Política de Grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="c75ac-426">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="c75ac-427">Nome exclusivo da Política de Grupo: AutoUpdateCheckPeriodMinutes</span><span class="sxs-lookup"><span data-stu-id="c75ac-427">GP unique name: AutoUpdateCheckPeriodMinutes</span></span>
- <span data-ttu-id="c75ac-428">Nome da Política de Grupo: Atualizar automaticamente a substituição do período de verificação</span><span class="sxs-lookup"><span data-stu-id="c75ac-428">GP name: Auto-update check period override</span></span>
- <span data-ttu-id="c75ac-429">Caminho da Política de Grupo: Modelos Administrativos/Microsoft Edge Update/Preferências</span><span class="sxs-lookup"><span data-stu-id="c75ac-429">GP path: Administrative Templates/Microsoft Edge Update/Preferences</span></span>
- <span data-ttu-id="c75ac-430">Nome do arquivo GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="c75ac-430">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="c75ac-431">Configurações de registro do Windows</span><span class="sxs-lookup"><span data-stu-id="c75ac-431">Windows Registry Settings</span></span>
- <span data-ttu-id="c75ac-432">Caminho: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="c75ac-432">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="c75ac-433">Nome do valor: AutoUpdateCheckPeriodMinutes</span><span class="sxs-lookup"><span data-stu-id="c75ac-433">Value Name: AutoUpdateCheckPeriodMinutes</span></span>
- <span data-ttu-id="c75ac-434">Tipo de valor: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="c75ac-434">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="c75ac-435">Valor de exemplo:</span><span class="sxs-lookup"><span data-stu-id="c75ac-435">Example value:</span></span>
```
0x00000578
```
[<span data-ttu-id="c75ac-436">Voltar ao início</span><span class="sxs-lookup"><span data-stu-id="c75ac-436">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="c75ac-437">UpdatesSuppressed</span><span class="sxs-lookup"><span data-stu-id="c75ac-437">UpdatesSuppressed</span></span>
#### <span data-ttu-id="c75ac-438">Período em cada dia para suprimir a verificação de atualização automática</span><span class="sxs-lookup"><span data-stu-id="c75ac-438">Time period in each day to suppress auto-update check</span></span>
><span data-ttu-id="c75ac-439">Microsoft Edge Update 1.3.33.5 e posterior</span><span class="sxs-lookup"><span data-stu-id="c75ac-439">Microsoft Edge Update 1.3.33.5 and later</span></span>

#### <span data-ttu-id="c75ac-440">Descrição</span><span class="sxs-lookup"><span data-stu-id="c75ac-440">Description</span></span>
<span data-ttu-id="c75ac-441">Se você habilitar essa política, as verificações de atualização serão suprimidas por dia a partir de Hora:Minuto por um período de duração (em minutos).</span><span class="sxs-lookup"><span data-stu-id="c75ac-441">If you enable this policy, update checks are suppressed each day starting at Hour:Minute for a period of Duration (in minutes).</span></span> <span data-ttu-id="c75ac-442">A duração não é afetada pelo horário de verão.</span><span class="sxs-lookup"><span data-stu-id="c75ac-442">Duration isn't affected by daylight saving time.</span></span> <span data-ttu-id="c75ac-443">Por exemplo, se o horário de início for 22:00 e a duração for de 480 minutos, as atualizações serão suprimidas por exatamente oito horas, independentemente do horário de verão começar ou terminar durante esse período.</span><span class="sxs-lookup"><span data-stu-id="c75ac-443">For example, if the start time is 22:00 and the duration is 480 minutes, updates will be suppressed for exactly 8 hours, regardless of whether daylight saving time starts or ends during this period.</span></span>

  <span data-ttu-id="c75ac-444">Se você desabilitar ou não configurar essa política, as verificações de atualização não serão suprimidas durante nenhum período específico.</span><span class="sxs-lookup"><span data-stu-id="c75ac-444">If you disable or don't configure this policy, update checks aren't suppressed during any specific period.</span></span>
#### <span data-ttu-id="c75ac-445">Informações e configurações do Windows</span><span class="sxs-lookup"><span data-stu-id="c75ac-445">Windows information and settings</span></span>
##### <span data-ttu-id="c75ac-446">Informações da Política de Grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="c75ac-446">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="c75ac-447">Nome exclusivo da Política de Grupo: UpdatesSuppressed</span><span class="sxs-lookup"><span data-stu-id="c75ac-447">GP unique name: UpdatesSuppressed</span></span>
- <span data-ttu-id="c75ac-448">Nome da Política de Grupo: Período em cada dia para suprimir a verificação de atualização automática</span><span class="sxs-lookup"><span data-stu-id="c75ac-448">GP name: Time period in each day to suppress auto-update check</span></span>
  - <span data-ttu-id="c75ac-449">Opções { Hour, Minute, Duration }</span><span class="sxs-lookup"><span data-stu-id="c75ac-449">Options { Hour, Minute, Duration }</span></span>
- <span data-ttu-id="c75ac-450">Caminho da Política de Grupo: Modelos Administrativos/Microsoft Edge Update/Preferências</span><span class="sxs-lookup"><span data-stu-id="c75ac-450">GP path: Administrative Templates/Microsoft Edge Update/Preferences</span></span>
- <span data-ttu-id="c75ac-451">Nome do arquivo GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="c75ac-451">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="c75ac-452">Configurações de registro do Windows</span><span class="sxs-lookup"><span data-stu-id="c75ac-452">Windows Registry Settings</span></span>
- <span data-ttu-id="c75ac-453">Caminho: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="c75ac-453">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="c75ac-454">Nome do valor:</span><span class="sxs-lookup"><span data-stu-id="c75ac-454">Value Name:</span></span> 
  - <span data-ttu-id="c75ac-455">UpdatesSuppressedDurationMin</span><span class="sxs-lookup"><span data-stu-id="c75ac-455">UpdatesSuppressedDurationMin</span></span>
  - <span data-ttu-id="c75ac-456">UpdatesSuppressedStartHour</span><span class="sxs-lookup"><span data-stu-id="c75ac-456">UpdatesSuppressedStartHour</span></span>
  - <span data-ttu-id="c75ac-457">UpdatesSuppressedStartMin</span><span class="sxs-lookup"><span data-stu-id="c75ac-457">UpdatesSuppressedStartMin</span></span>
- <span data-ttu-id="c75ac-458">Tipo de valor: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="c75ac-458">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="c75ac-459">Valor de exemplo:</span><span class="sxs-lookup"><span data-stu-id="c75ac-459">Example value:</span></span>
```
duration   : 0x0000003c
start hour : 0x00000001
start min  : 0x00000002
```
[<span data-ttu-id="c75ac-460">Voltar ao início</span><span class="sxs-lookup"><span data-stu-id="c75ac-460">Back to top</span></span>](#microsoft-edge---update-policies)


## <span data-ttu-id="c75ac-461">Políticas do servidor proxy</span><span class="sxs-lookup"><span data-stu-id="c75ac-461">Proxy Server policies</span></span>

[<span data-ttu-id="c75ac-462">Voltar ao início</span><span class="sxs-lookup"><span data-stu-id="c75ac-462">Back to top</span></span>](#microsoft-edge---update-policies)
### <span data-ttu-id="c75ac-463">ProxyMode</span><span class="sxs-lookup"><span data-stu-id="c75ac-463">ProxyMode</span></span>
#### <span data-ttu-id="c75ac-464">Escolher como especificar as configurações do servidor proxy</span><span class="sxs-lookup"><span data-stu-id="c75ac-464">Choose how to specify proxy server settings</span></span>
><span data-ttu-id="c75ac-465">Microsoft Edge Update 1.3.21.81 e posterior</span><span class="sxs-lookup"><span data-stu-id="c75ac-465">Microsoft Edge Update 1.3.21.81 and later</span></span>

#### <span data-ttu-id="c75ac-466">Descrição</span><span class="sxs-lookup"><span data-stu-id="c75ac-466">Description</span></span>
<span data-ttu-id="c75ac-467">Permite especificar as configurações do servidor proxy que serão usadas pelo Microsoft Edge Update.</span><span class="sxs-lookup"><span data-stu-id="c75ac-467">Allows you to specify the proxy server settings that are used by Microsoft Edge Update.</span></span>

  <span data-ttu-id="c75ac-468">Se você habilitar essa configuração da política, poderá escolher entre as seguintes opções do servidor proxy:</span><span class="sxs-lookup"><span data-stu-id="c75ac-468">If you enable this policy, you can choose between the following proxy server options:</span></span>
   - <span data-ttu-id="c75ac-469">Se você optar por nunca usar um servidor proxy e sempre se conectar diretamente, todas as outras opções serão ignoradas.</span><span class="sxs-lookup"><span data-stu-id="c75ac-469">If you choose to never use a proxy server and always connect directly, all other options are ignored.</span></span>
   - <span data-ttu-id="c75ac-470">Se você optar por usar as configurações de proxy do sistema ou detectar automaticamente o servidor proxy, todas as outras opções serão ignoradas.</span><span class="sxs-lookup"><span data-stu-id="c75ac-470">If you choose to use system proxy settings or auto-detect the proxy server, all other options are ignored.</span></span>
   - <span data-ttu-id="c75ac-471">Se escolher o modo fixo do servidor proxy, você poderá especificar mais opções em '[Endereço ou URL do servidor proxy](#proxyserver)'.</span><span class="sxs-lookup"><span data-stu-id="c75ac-471">If you choose fixed server proxy mode, you can specify further options in '[Address or URL of proxy server](#proxyserver)' policy.</span></span>
   - <span data-ttu-id="c75ac-472">Se você optar por usar um script de proxy .pac, deve especificar a URL do script em '[De URL para um arquivo .pac de proxy](#proxypacurl)'.</span><span class="sxs-lookup"><span data-stu-id="c75ac-472">If you choose to use a .pac proxy script, you must specify the URL for the script in '[URL to a proxy .pac file](#proxypacurl)' policy.</span></span>

  <span data-ttu-id="c75ac-473">Se você habilitar essa política, os usuários de sua organização não poderão alterar as configurações de proxy no Microsoft Edge Update.</span><span class="sxs-lookup"><span data-stu-id="c75ac-473">If you enable this policy, users in your organization can't change the proxy settings in Microsoft Edge Update.</span></span>

  <span data-ttu-id="c75ac-474">Se você desabilitar ou não configurar essa política, nenhuma configuração do servidor proxy será definida, mas os usuários de sua organização poderão escolher suas próprias configurações de proxy para o Microsoft Edge Update.</span><span class="sxs-lookup"><span data-stu-id="c75ac-474">If you disable or don't configure this policy, no proxy server settings are configured, but users in your organization can choose their own proxy settings for Microsoft Edge Update.</span></span>
#### <span data-ttu-id="c75ac-475">Informações e configurações do Windows</span><span class="sxs-lookup"><span data-stu-id="c75ac-475">Windows information and settings</span></span>
##### <span data-ttu-id="c75ac-476">Informações da Política de Grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="c75ac-476">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="c75ac-477">Nome exclusivo da Política de Grupo: ProxyMode</span><span class="sxs-lookup"><span data-stu-id="c75ac-477">GP unique name: ProxyMode</span></span>
- <span data-ttu-id="c75ac-478">Nome da Política de Grupo: Escolher como especificar as configurações do servidor proxy</span><span class="sxs-lookup"><span data-stu-id="c75ac-478">GP name: Choose how to specify proxy server settings</span></span>
- <span data-ttu-id="c75ac-479">Caminho da Política de Grupo: Modelos Administrativos/Microsoft Edge Update/Servidor Proxy</span><span class="sxs-lookup"><span data-stu-id="c75ac-479">GP path: Administrative Templates/Microsoft Edge Update/Proxy Server</span></span>
- <span data-ttu-id="c75ac-480">Nome do arquivo GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="c75ac-480">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="c75ac-481">Configurações de registro do Windows</span><span class="sxs-lookup"><span data-stu-id="c75ac-481">Windows Registry Settings</span></span>
- <span data-ttu-id="c75ac-482">Caminho: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="c75ac-482">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="c75ac-483">Nome do valor: ProxyMode</span><span class="sxs-lookup"><span data-stu-id="c75ac-483">Value Name: ProxyMode</span></span>
- <span data-ttu-id="c75ac-484">Tipo do valor: REG_SZ</span><span class="sxs-lookup"><span data-stu-id="c75ac-484">Value Type: REG_SZ</span></span>
##### <span data-ttu-id="c75ac-485">Valor de exemplo:</span><span class="sxs-lookup"><span data-stu-id="c75ac-485">Example value:</span></span>
```
fixed_servers
```
[<span data-ttu-id="c75ac-486">Voltar ao início</span><span class="sxs-lookup"><span data-stu-id="c75ac-486">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="c75ac-487">ProxyPacUrl</span><span class="sxs-lookup"><span data-stu-id="c75ac-487">ProxyPacUrl</span></span>
#### <span data-ttu-id="c75ac-488">A URL para um arquivo .pac de proxy</span><span class="sxs-lookup"><span data-stu-id="c75ac-488">URL to a proxy .pac file</span></span>
><span data-ttu-id="c75ac-489">Microsoft Edge Update 1.3.21.81 e posterior</span><span class="sxs-lookup"><span data-stu-id="c75ac-489">Microsoft Edge Update 1.3.21.81 and later</span></span>

#### <span data-ttu-id="c75ac-490">Descrição</span><span class="sxs-lookup"><span data-stu-id="c75ac-490">Description</span></span>
<span data-ttu-id="c75ac-491">Permite especificar uma URL para um arquivo (PAC) de configuração automática de proxy.</span><span class="sxs-lookup"><span data-stu-id="c75ac-491">Allows you to specify a URL for a proxy auto-config (PAC) file.</span></span>

  <span data-ttu-id="c75ac-492">Se habilitar essa política, você poderá especificar uma URL de um arquivo PAC para automatizar a maneira como o Microsoft Edge Update seleciona para a busca de um site específico.</span><span class="sxs-lookup"><span data-stu-id="c75ac-492">If you enable this policy, you can specify a URL for a PAC file to automate how Microsoft Edge Update selects the appropriate proxy server for fetching a particular website.</span></span>

  <span data-ttu-id="c75ac-493">Essa política será aplicada somente se você especificou as configurações de proxy manuais na política '[Escolher como especificar configurações do servidor proxy](#proxymode)'.</span><span class="sxs-lookup"><span data-stu-id="c75ac-493">This policy is applied only if you have specified manual proxy settings in the '[Choose how to specify proxy server settings](#proxymode)' policy.</span></span>

  <span data-ttu-id="c75ac-494">Não configure essa política se você selecionou uma configuração de proxy que não seja manual na política '[Escolher como especificar as configurações do servidor proxy](#proxymode)'.</span><span class="sxs-lookup"><span data-stu-id="c75ac-494">Don't configure this policy if you have selected a proxy setting other than manual in the '[Choose how to specify proxy server settings](#proxymode)' policy.</span></span>
#### <span data-ttu-id="c75ac-495">Informações e configurações do Windows</span><span class="sxs-lookup"><span data-stu-id="c75ac-495">Windows information and settings</span></span>
##### <span data-ttu-id="c75ac-496">Informações da Política de Grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="c75ac-496">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="c75ac-497">Nome exclusivo da Política de Grupo: ProxyPacUrl</span><span class="sxs-lookup"><span data-stu-id="c75ac-497">GP unique name: ProxyPacUrl</span></span>
- <span data-ttu-id="c75ac-498">Nome da Política de Grupo: A URL para um arquivo .pac de proxy</span><span class="sxs-lookup"><span data-stu-id="c75ac-498">GP name: URL to a proxy .pac file</span></span>
- <span data-ttu-id="c75ac-499">Caminho da Política de Grupo: Modelos Administrativos/Microsoft Edge Update/Servidor Proxy</span><span class="sxs-lookup"><span data-stu-id="c75ac-499">GP path: Administrative Templates/Microsoft Edge Update/Proxy Server</span></span>
- <span data-ttu-id="c75ac-500">Nome do arquivo GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="c75ac-500">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="c75ac-501">Configurações de registro do Windows</span><span class="sxs-lookup"><span data-stu-id="c75ac-501">Windows Registry Settings</span></span>
- <span data-ttu-id="c75ac-502">Caminho: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="c75ac-502">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="c75ac-503">Nome do valor: ProxyPacUrl</span><span class="sxs-lookup"><span data-stu-id="c75ac-503">Value Name: ProxyPacUrl</span></span>
- <span data-ttu-id="c75ac-504">Tipo do valor: REG_SZ</span><span class="sxs-lookup"><span data-stu-id="c75ac-504">Value Type: REG_SZ</span></span>
##### <span data-ttu-id="c75ac-505">Valor de exemplo:</span><span class="sxs-lookup"><span data-stu-id="c75ac-505">Example value:</span></span>
```
https://www.microsoft.com
```
[<span data-ttu-id="c75ac-506">Voltar ao início</span><span class="sxs-lookup"><span data-stu-id="c75ac-506">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="c75ac-507">ProxyServer</span><span class="sxs-lookup"><span data-stu-id="c75ac-507">ProxyServer</span></span>
#### <span data-ttu-id="c75ac-508">Endereço ou URL do servidor proxy</span><span class="sxs-lookup"><span data-stu-id="c75ac-508">Address or URL of proxy server</span></span>
><span data-ttu-id="c75ac-509">Microsoft Edge Update 1.3.21.81 e posterior</span><span class="sxs-lookup"><span data-stu-id="c75ac-509">Microsoft Edge Update 1.3.21.81 and later</span></span>

#### <span data-ttu-id="c75ac-510">Description</span><span class="sxs-lookup"><span data-stu-id="c75ac-510">Description</span></span>
<span data-ttu-id="c75ac-511">Permite especificar a URL do servidor proxy para o Microsoft Edge Update usar.</span><span class="sxs-lookup"><span data-stu-id="c75ac-511">Allows you to specify the URL of the proxy server for Microsoft Edge Update to use.</span></span>

  <span data-ttu-id="c75ac-512">Se você habilitar essa política, poderá configurar a URL do servidor proxy usada pelo Microsoft Edge Update em sua organização.</span><span class="sxs-lookup"><span data-stu-id="c75ac-512">If you enable this policy, you can set the proxy server URL used by Microsoft Edge Update in your organization.</span></span>

  <span data-ttu-id="c75ac-513">Essa política será aplicada somente se você selecionou as configurações de proxy manuais na política '[Escolher como especificar as configurações do servidor proxy](#proxymode)'.</span><span class="sxs-lookup"><span data-stu-id="c75ac-513">This policy is applied only if you have selected manual proxy settings in the '[Choose how to specify proxy server settings](#proxymode)' policy.</span></span>

  <span data-ttu-id="c75ac-514">Não configure essa política se você selecionou uma configuração de proxy que não seja manual na política '[Escolher como especificar as configurações do servidor proxy](#proxymode)'.</span><span class="sxs-lookup"><span data-stu-id="c75ac-514">Don't configure this policy if you have selected a proxy setting other than manual in the '[Choose how to specify proxy server settings](#proxymode)' policy.</span></span>
#### <span data-ttu-id="c75ac-515">Informações e configurações do Windows</span><span class="sxs-lookup"><span data-stu-id="c75ac-515">Windows information and settings</span></span>
##### <span data-ttu-id="c75ac-516">Informações da Política de Grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="c75ac-516">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="c75ac-517">Nome exclusivo da Política de Grupo: ProxyServer</span><span class="sxs-lookup"><span data-stu-id="c75ac-517">GP unique name: ProxyServer</span></span>
- <span data-ttu-id="c75ac-518">Nome da Política de Grupo: O endereço ou a URL do servidor proxy</span><span class="sxs-lookup"><span data-stu-id="c75ac-518">GP name: Address or URL of proxy server</span></span>
- <span data-ttu-id="c75ac-519">Caminho da Política de Grupo: Modelos Administrativos/Microsoft Edge Update/Servidor Proxy</span><span class="sxs-lookup"><span data-stu-id="c75ac-519">GP path: Administrative Templates/Microsoft Edge Update/Proxy Server</span></span>
- <span data-ttu-id="c75ac-520">Nome do arquivo GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="c75ac-520">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="c75ac-521">Configurações de registro do Windows</span><span class="sxs-lookup"><span data-stu-id="c75ac-521">Windows Registry Settings</span></span>
- <span data-ttu-id="c75ac-522">Caminho: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="c75ac-522">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="c75ac-523">Nome do valor: ProxyServer</span><span class="sxs-lookup"><span data-stu-id="c75ac-523">Value Name: ProxyServer</span></span>
- <span data-ttu-id="c75ac-524">Tipo do valor: REG_SZ</span><span class="sxs-lookup"><span data-stu-id="c75ac-524">Value Type: REG_SZ</span></span>
##### <span data-ttu-id="c75ac-525">Valor de exemplo:</span><span class="sxs-lookup"><span data-stu-id="c75ac-525">Example value:</span></span>
```
https://www.microsoft.com
```
[<span data-ttu-id="c75ac-526">Voltar ao início</span><span class="sxs-lookup"><span data-stu-id="c75ac-526">Back to top</span></span>](#microsoft-edge---update-policies)


## <span data-ttu-id="c75ac-527">Políticas do Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="c75ac-527">Microsoft Edge WebView policies</span></span>

[<span data-ttu-id="c75ac-528">Voltar ao início</span><span class="sxs-lookup"><span data-stu-id="c75ac-528">Back to top</span></span>](#microsoft-edge---update-policies)
### <span data-ttu-id="c75ac-529">Instalar (WebView)</span><span class="sxs-lookup"><span data-stu-id="c75ac-529">Install (WebView)</span></span>
#### <span data-ttu-id="c75ac-530">Permitir instalação</span><span class="sxs-lookup"><span data-stu-id="c75ac-530">Allow installation</span></span>
><span data-ttu-id="c75ac-531">Microsoft Edge Update 1.3.127.1 e posterior</span><span class="sxs-lookup"><span data-stu-id="c75ac-531">Microsoft Edge Update 1.3.127.1 and later</span></span>

#### <span data-ttu-id="c75ac-532">Descrição</span><span class="sxs-lookup"><span data-stu-id="c75ac-532">Description</span></span>
<span data-ttu-id="c75ac-533">Permite especificar se o Microsoft Edge WebView pode ser instalado usando o Microsoft Edge Update.</span><span class="sxs-lookup"><span data-stu-id="c75ac-533">Lets you specify whether Microsoft Edge WebView can be installed using Microsoft Edge Update.</span></span>

  - <span data-ttu-id="c75ac-534">Se você habilitar esta política, os usuários poderão instalar o Microsoft Edge WebView por meio do Microsoft Edge Update.</span><span class="sxs-lookup"><span data-stu-id="c75ac-534">If you enable this policy, users can install Microsoft Edge WebView through Microsoft Edge Update.</span></span>
  - <span data-ttu-id="c75ac-535">Se você desabilitar esta política, os usuários não poderão instalar o Microsoft Edge WebView por meio do Microsoft Edge Update.</span><span class="sxs-lookup"><span data-stu-id="c75ac-535">If you disable this policy, users cannot install Microsoft Edge WebView through Microsoft Edge Update.</span></span>
  - <span data-ttu-id="c75ac-536">Se você não configurar esta política, a configuração da política '[Permitir instalação padrão](#installdefault)' determina se os usuários podem instalar o Microsoft Edge WebView por meio do Microsoft Edge Update.</span><span class="sxs-lookup"><span data-stu-id="c75ac-536">If you don't configure this policy, the '[Allow installation default](#installdefault)' policy configuration determines whether users can install Microsoft Edge WebView through Microsoft Edge Update.</span></span>
#### <span data-ttu-id="c75ac-537">Informações e configurações do Windows</span><span class="sxs-lookup"><span data-stu-id="c75ac-537">Windows information and settings</span></span>
##### <span data-ttu-id="c75ac-538">Informações da Política de Grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="c75ac-538">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="c75ac-539">Nome exclusivo da Política de Grupo: Install</span><span class="sxs-lookup"><span data-stu-id="c75ac-539">GP unique name: Install</span></span>
- <span data-ttu-id="c75ac-540">Nome da Política de Grupo: Permitir instalação</span><span class="sxs-lookup"><span data-stu-id="c75ac-540">GP name: Allow installation</span></span>
- <span data-ttu-id="c75ac-541">Caminho da Política de Grupo: Modelos Administrativos/Microsoft Edge Update/Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="c75ac-541">GP path: Administrative Templates/Microsoft Edge Update/Microsoft Edge WebView</span></span>
- <span data-ttu-id="c75ac-542">Nome do arquivo GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="c75ac-542">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="c75ac-543">Configurações de registro do Windows</span><span class="sxs-lookup"><span data-stu-id="c75ac-543">Windows Registry Settings</span></span>
- <span data-ttu-id="c75ac-544">Caminho: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="c75ac-544">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="c75ac-545">Nome do valor:</span><span class="sxs-lookup"><span data-stu-id="c75ac-545">Value Name:</span></span> 
  - <span data-ttu-id="c75ac-546">Install{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}</span><span class="sxs-lookup"><span data-stu-id="c75ac-546">Install{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}</span></span>
- <span data-ttu-id="c75ac-547">Tipo de valor: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="c75ac-547">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="c75ac-548">Valor de exemplo:</span><span class="sxs-lookup"><span data-stu-id="c75ac-548">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="c75ac-549">Voltar ao início</span><span class="sxs-lookup"><span data-stu-id="c75ac-549">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="c75ac-550">Atualização (WebView)</span><span class="sxs-lookup"><span data-stu-id="c75ac-550">Update (WebView)</span></span>
#### <span data-ttu-id="c75ac-551">Atualizar a substituição de política</span><span class="sxs-lookup"><span data-stu-id="c75ac-551">Update policy override</span></span>
><span data-ttu-id="c75ac-552">Microsoft Edge Update 1.3.127.1 e posterior</span><span class="sxs-lookup"><span data-stu-id="c75ac-552">Microsoft Edge Update 1.3.127.1 and later</span></span>

#### <span data-ttu-id="c75ac-553">Descrição</span><span class="sxs-lookup"><span data-stu-id="c75ac-553">Description</span></span>
<span data-ttu-id="c75ac-554">Permite especificar se as atualizações automáticas estão habilitadas ou não para o Microsoft Edge WebView.</span><span class="sxs-lookup"><span data-stu-id="c75ac-554">Lets you specify whether or not automatic updates are enabled for Microsoft Edge WebView.</span></span> <span data-ttu-id="c75ac-555">O Microsoft Edge WebView é um componente usado pelos aplicativos para exibir conteúdo da Web.</span><span class="sxs-lookup"><span data-stu-id="c75ac-555">Microsoft Edge WebView is a component used by applications to display web content.</span></span>
<span data-ttu-id="c75ac-556">As atualizações automáticas estão habilitadas por padrão.</span><span class="sxs-lookup"><span data-stu-id="c75ac-556">Automatic updates are enabled by default.</span></span> <span data-ttu-id="c75ac-557">Desabilitar as atualizações automáticas do Microsoft Edge WebView pode causar problemas de compatibilidade com aplicativos que dependem desse componente.</span><span class="sxs-lookup"><span data-stu-id="c75ac-557">Disabling automatic updates for Microsoft Edge WebView might cause compatibility issues with applications that depend on this component.</span></span>

  <span data-ttu-id="c75ac-558">Se você habilitar esta política, o Microsoft Edge Update tratará as atualizações do Microsoft Edge WebView de acordo com as seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="c75ac-558">If you enable this policy, Microsoft Edge Update handles Microsoft Edge WebView updates according to how you configure the following options:</span></span>
  - <span data-ttu-id="c75ac-559">Sempre permitir atualizações: as atualizações serão baixadas e aplicadas automaticamente</span><span class="sxs-lookup"><span data-stu-id="c75ac-559">Always allow updates: Updates are automatically downloaded and applied</span></span>
  - <span data-ttu-id="c75ac-560">Atualizações desabilitadas: as atualizações nunca serão baixadas ou aplicadas</span><span class="sxs-lookup"><span data-stu-id="c75ac-560">Updates disabled: Updates are never downloaded or applied</span></span>

  <span data-ttu-id="c75ac-561">Se você não habilitar esta política, as atualizações serão baixadas e aplicadas automaticamente.</span><span class="sxs-lookup"><span data-stu-id="c75ac-561">If you don't enable this policy, updates are automatically downloaded and applied.</span></span>
#### <span data-ttu-id="c75ac-562">Informações e configurações do Windows</span><span class="sxs-lookup"><span data-stu-id="c75ac-562">Windows information and settings</span></span>
##### <span data-ttu-id="c75ac-563">Informações da Política de Grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="c75ac-563">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="c75ac-564">Nome exclusivo da Política de Grupo: Update</span><span class="sxs-lookup"><span data-stu-id="c75ac-564">GP unique name: Update</span></span>
- <span data-ttu-id="c75ac-565">Nome da Política de Grupo: Atualizar a substituição de política</span><span class="sxs-lookup"><span data-stu-id="c75ac-565">GP name: Update policy override</span></span>
- <span data-ttu-id="c75ac-566">Caminho da Política de Grupo: Modelos Administrativos/Microsoft Edge Update/Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="c75ac-566">GP path: Administrative Templates/Microsoft Edge Update/Microsoft Edge WebView</span></span>
- <span data-ttu-id="c75ac-567">Nome do arquivo GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="c75ac-567">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="c75ac-568">Configurações de registro do Windows</span><span class="sxs-lookup"><span data-stu-id="c75ac-568">Windows Registry Settings</span></span>
- <span data-ttu-id="c75ac-569">Caminho: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="c75ac-569">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="c75ac-570">Nome do valor:</span><span class="sxs-lookup"><span data-stu-id="c75ac-570">Value Name:</span></span> 
  - <span data-ttu-id="c75ac-571">Update{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}</span><span class="sxs-lookup"><span data-stu-id="c75ac-571">Update{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}</span></span>
- <span data-ttu-id="c75ac-572">Tipo de valor: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="c75ac-572">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="c75ac-573">Valor de exemplo:</span><span class="sxs-lookup"><span data-stu-id="c75ac-573">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="c75ac-574">Voltar ao início</span><span class="sxs-lookup"><span data-stu-id="c75ac-574">Back to top</span></span>](#microsoft-edge---update-policies)


## <span data-ttu-id="c75ac-575">Consulte também</span><span class="sxs-lookup"><span data-stu-id="c75ac-575">See also</span></span>
  - [<span data-ttu-id="c75ac-576">Configurar o Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="c75ac-576">Configuring Microsoft Edge</span></span>](configure-microsoft-edge.md)
  - [<span data-ttu-id="c75ac-577">Página de aterrissagem do Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="c75ac-577">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)