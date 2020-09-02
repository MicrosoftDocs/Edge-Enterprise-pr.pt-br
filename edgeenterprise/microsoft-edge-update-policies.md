---
title: Documentação da política do Microsoft Edge Update
ms.author: stmoody
author: brianalt-msft
manager: tahills
ms.date: 06/10/2020
audience: ITPro
ms.topic: reference
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
ms.custom: ''
description: Documentação para todas as políticas compatíveis com o Microsoft Edge Update
ms.openlocfilehash: d772d8dd6f60b89e9bd12a77b740e5fad699756a
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979092"
---
# <span data-ttu-id="2e632-103">Microsoft Edge - Políticas de atualização</span><span class="sxs-lookup"><span data-stu-id="2e632-103">Microsoft Edge - Update policies</span></span>
<span data-ttu-id="2e632-104">A versão mais recente do Microsoft Edge inclui as seguintes políticas que você pode usar para controlar como e quando o Microsoft Edge é atualizado.</span><span class="sxs-lookup"><span data-stu-id="2e632-104">The latest version of Microsoft Edge includes the following policies that you can use to control how and when Microsoft Edge is updated.</span></span>

           
<span data-ttu-id="2e632-105">Para obter informações sobre outras políticas disponíveis no Microsoft Edge, confira [Referência de política do navegador Microsoft Edge](microsoft-edge-policies.md)</span><span class="sxs-lookup"><span data-stu-id="2e632-105">For information about other policies available in Microsoft Edge, check out [Microsoft Edge browser policy reference](microsoft-edge-policies.md)</span></span>
> [!NOTE]
> <span data-ttu-id="2e632-106">Este artigo se aplica ao Microsoft Edge versão 77 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="2e632-106">This article applies to Microsoft Edge version 77 or later.</span></span>

## <span data-ttu-id="2e632-107">Políticas disponíveis</span><span class="sxs-lookup"><span data-stu-id="2e632-107">Available policies</span></span>
<span data-ttu-id="2e632-108">Estas tabelas listam todas as políticas de grupo relacionadas a atualizações disponíveis nesta versão do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2e632-108">These tables lists all of the update-related group policies available in this release of Microsoft Edge.</span></span> <span data-ttu-id="2e632-109">Use os links na tabela a seguir para obter mais detalhes sobre políticas específicas.</span><span class="sxs-lookup"><span data-stu-id="2e632-109">Use the links in the table to get more details about specific policies.</span></span>

|||
|-|-|
|[<span data-ttu-id="2e632-110">Aplicativos</span><span class="sxs-lookup"><span data-stu-id="2e632-110">Applications</span></span>](#applications)|[<span data-ttu-id="2e632-111">Preferências</span><span class="sxs-lookup"><span data-stu-id="2e632-111">Preferences</span></span>](#preferences)|
|[<span data-ttu-id="2e632-112">Servidor proxy</span><span class="sxs-lookup"><span data-stu-id="2e632-112">Proxy Server</span></span>](#proxy-server)||

### [<span data-ttu-id="2e632-113">Aplicativos</span><span class="sxs-lookup"><span data-stu-id="2e632-113">Applications</span></span>](#applications-policies)
|<span data-ttu-id="2e632-114">Nome da política</span><span class="sxs-lookup"><span data-stu-id="2e632-114">Policy Name</span></span>|<span data-ttu-id="2e632-115">Legenda</span><span class="sxs-lookup"><span data-stu-id="2e632-115">Caption</span></span>|
|-|-|
|[<span data-ttu-id="2e632-116">InstallDefault</span><span class="sxs-lookup"><span data-stu-id="2e632-116">InstallDefault</span></span>](#installdefault)|<span data-ttu-id="2e632-117">Permitir a instalação padrão</span><span class="sxs-lookup"><span data-stu-id="2e632-117">Allow installation default</span></span>|
|[<span data-ttu-id="2e632-118">UpdateDefault</span><span class="sxs-lookup"><span data-stu-id="2e632-118">UpdateDefault</span></span>](#updatedefault)|<span data-ttu-id="2e632-119">Atualizar o padrão de substituição de política</span><span class="sxs-lookup"><span data-stu-id="2e632-119">Update policy override default</span></span>|
|[<span data-ttu-id="2e632-120">Instalar</span><span class="sxs-lookup"><span data-stu-id="2e632-120">Install</span></span>](#install)|<span data-ttu-id="2e632-121">Permitir a instalação (por canal)</span><span class="sxs-lookup"><span data-stu-id="2e632-121">Allow installation (per channel)</span></span>|
|[<span data-ttu-id="2e632-122">Update</span><span class="sxs-lookup"><span data-stu-id="2e632-122">Update</span></span>](#update)|<span data-ttu-id="2e632-123">Atualizar a substituição de política (por canal)</span><span class="sxs-lookup"><span data-stu-id="2e632-123">Update policy override (per channel)</span></span>|
|[<span data-ttu-id="2e632-124">Allowsxs</span><span class="sxs-lookup"><span data-stu-id="2e632-124">Allowsxs</span></span>](#allowsxs)|<span data-ttu-id="2e632-125">Permitir a experiência de navegador Lado a Lado do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="2e632-125">Allow Microsoft Edge Side by Side browser experience</span></span>|
|[<span data-ttu-id="2e632-126">CreateDesktopShortcutDefault</span><span class="sxs-lookup"><span data-stu-id="2e632-126">CreateDesktopShortcutDefault</span></span>](#createdesktopshortcutdefault)|<span data-ttu-id="2e632-127">Impedir a criação de Atalho da Área de Trabalho com a instalação padrão</span><span class="sxs-lookup"><span data-stu-id="2e632-127">Prevent Desktop Shortcut creation upon install default</span></span>|
|[<span data-ttu-id="2e632-128">CreateDesktopShortcut</span><span class="sxs-lookup"><span data-stu-id="2e632-128">CreateDesktopShortcut</span></span>](#createdesktopshortcut)|<span data-ttu-id="2e632-129">Impedir a criação de Atalho da Área de Trabalho com a instalação (por canal)</span><span class="sxs-lookup"><span data-stu-id="2e632-129">Prevent Desktop Shortcut creation upon install (per channel)</span></span>|
|[<span data-ttu-id="2e632-130">TargetVersionPrefix</span><span class="sxs-lookup"><span data-stu-id="2e632-130">TargetVersionPrefix</span></span>](#targetversionprefix)|<span data-ttu-id="2e632-131">Substituir versão de destino (por canal)</span><span class="sxs-lookup"><span data-stu-id="2e632-131">Target version override (per channel)</span></span>|

### [<span data-ttu-id="2e632-132">Preferências</span><span class="sxs-lookup"><span data-stu-id="2e632-132">Preferences</span></span>](#preferences-policies)
|<span data-ttu-id="2e632-133">Nome da política</span><span class="sxs-lookup"><span data-stu-id="2e632-133">Policy Name</span></span>|<span data-ttu-id="2e632-134">Legenda</span><span class="sxs-lookup"><span data-stu-id="2e632-134">Caption</span></span>|
|-|-|
|[<span data-ttu-id="2e632-135">AutoUpdateCheckPeriodMinutes</span><span class="sxs-lookup"><span data-stu-id="2e632-135">AutoUpdateCheckPeriodMinutes</span></span>](#autoupdatecheckperiodminutes)|<span data-ttu-id="2e632-136">Atualizar automaticamente a substituição do período de verificação</span><span class="sxs-lookup"><span data-stu-id="2e632-136">Auto-update check period override</span></span>|
|[<span data-ttu-id="2e632-137">UpdatesSuppressed</span><span class="sxs-lookup"><span data-stu-id="2e632-137">UpdatesSuppressed</span></span>](#updatessuppressed)|<span data-ttu-id="2e632-138">O período em cada dia para suprimir a verificação de atualização automática</span><span class="sxs-lookup"><span data-stu-id="2e632-138">Time period in each day to suppress auto-update check</span></span>|

### [<span data-ttu-id="2e632-139">Servidor proxy</span><span class="sxs-lookup"><span data-stu-id="2e632-139">Proxy Server</span></span>](#proxy-server-policies)
|<span data-ttu-id="2e632-140">Nome da política</span><span class="sxs-lookup"><span data-stu-id="2e632-140">Policy Name</span></span>|<span data-ttu-id="2e632-141">Legenda</span><span class="sxs-lookup"><span data-stu-id="2e632-141">Caption</span></span>|
|-|-|
|[<span data-ttu-id="2e632-142">ProxyMode</span><span class="sxs-lookup"><span data-stu-id="2e632-142">ProxyMode</span></span>](#proxymode)|<span data-ttu-id="2e632-143">Escolher como especificar as configurações do servidor proxy</span><span class="sxs-lookup"><span data-stu-id="2e632-143">Choose how to specify proxy server settings</span></span>|
|[<span data-ttu-id="2e632-144">ProxyPacUrl</span><span class="sxs-lookup"><span data-stu-id="2e632-144">ProxyPacUrl</span></span>](#proxypacurl)|<span data-ttu-id="2e632-145">A URL para um arquivo .pac de proxy</span><span class="sxs-lookup"><span data-stu-id="2e632-145">URL to a proxy .pac file</span></span>|
|[<span data-ttu-id="2e632-146">ProxyServer</span><span class="sxs-lookup"><span data-stu-id="2e632-146">ProxyServer</span></span>](#proxyserver)|<span data-ttu-id="2e632-147">O endereço ou a URL do servidor proxy</span><span class="sxs-lookup"><span data-stu-id="2e632-147">Address or URL of proxy server</span></span>|

                 
      
  
             
            
                  

## <span data-ttu-id="2e632-148">Políticas de aplicativos</span><span class="sxs-lookup"><span data-stu-id="2e632-148">Applications policies</span></span>

[<span data-ttu-id="2e632-149">Voltar ao início</span><span class="sxs-lookup"><span data-stu-id="2e632-149">Back to top</span></span>](#microsoft-edge---update-policies)
### <span data-ttu-id="2e632-150">InstallDefault</span><span class="sxs-lookup"><span data-stu-id="2e632-150">InstallDefault</span></span>
#### <span data-ttu-id="2e632-151">Permitir a instalação padrão</span><span class="sxs-lookup"><span data-stu-id="2e632-151">Allow installation default</span></span>
><span data-ttu-id="2e632-152">Microsoft Edge Update 1.2.145.5 e posterior</span><span class="sxs-lookup"><span data-stu-id="2e632-152">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <span data-ttu-id="2e632-153">Descrição</span><span class="sxs-lookup"><span data-stu-id="2e632-153">Description</span></span>
<span data-ttu-id="2e632-154">Você pode especificar o comportamento padrão de todos os canais para permitir ou bloquear as atualizações do Microsoft Edge quando o Microsoft Edge Update for usado.</span><span class="sxs-lookup"><span data-stu-id="2e632-154">You can specify the default behavior of all channels to allow or block Microsoft Edge updates when Microsoft Edge Update is used.</span></span>

<span data-ttu-id="2e632-155">Você pode substituir esta política para canais individuais habilitando a política '[Permitir instalação](#install)' para canais específicos.</span><span class="sxs-lookup"><span data-stu-id="2e632-155">You can override this policy for individual channels by enabling the '[Allow installation](#install)' policy for specific channels.</span></span>

<span data-ttu-id="2e632-156">Se você desabilitar esta política, a instalação do Microsoft Edge por meio do Microsoft Edge Update será bloqueada.</span><span class="sxs-lookup"><span data-stu-id="2e632-156">If you disable this policy, the installation of Microsoft Edge through Microsoft Edge Update is blocked.</span></span> <span data-ttu-id="2e632-157">Isso afeta a instalação do software do Microsoft Edge somente quando os usuários estiverem executando o Microsoft Edge Update sem ter configurado a política '[Permitir instalação](#install)'.</span><span class="sxs-lookup"><span data-stu-id="2e632-157">This only affects the installation of Microsoft Edge software only when users are running Microsoft Edge Update and when they haven't configured the '[Allow installation](#install)' policy.</span></span>

<span data-ttu-id="2e632-158">Esta política não impede a execução do Microsoft Edge Update, nem impede que os usuários instalem o software do Microsoft Edge por outros métodos.</span><span class="sxs-lookup"><span data-stu-id="2e632-158">This policy doesn't prevent Microsoft Edge Update from running or prevent users from installing Microsoft Edge software using other methods.</span></span>
#### <span data-ttu-id="2e632-159">Informações e configurações do Windows</span><span class="sxs-lookup"><span data-stu-id="2e632-159">Windows information and settings</span></span>
##### <span data-ttu-id="2e632-160">Informações da Política de Grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="2e632-160">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="2e632-161">Nome exclusivo da Política de Grupo: InstallDefault</span><span class="sxs-lookup"><span data-stu-id="2e632-161">GP unique name: InstallDefault</span></span>
- <span data-ttu-id="2e632-162">Nome da Política de Grupo: Permitir a instalação padrão</span><span class="sxs-lookup"><span data-stu-id="2e632-162">GP name: Allow installation default</span></span>
- <span data-ttu-id="2e632-163">Caminho da Política Padrão: Modelos Administrativos/Microsoft Edge Update/Aplicativos</span><span class="sxs-lookup"><span data-stu-id="2e632-163">GP path: Administrative Templates/Microsoft Edge Update/Applications</span></span>
- <span data-ttu-id="2e632-164">Nome do arquivo de ADMX da Política de Grupo: edgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="2e632-164">GP ADMX file name: edgeupdate.admx</span></span>
##### <span data-ttu-id="2e632-165">Configurações de registro do Windows</span><span class="sxs-lookup"><span data-stu-id="2e632-165">Windows Registry Settings</span></span>
- <span data-ttu-id="2e632-166">Caminho: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="2e632-166">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="2e632-167">Nome do valor: InstallDefault</span><span class="sxs-lookup"><span data-stu-id="2e632-167">Value Name: InstallDefault</span></span>
- <span data-ttu-id="2e632-168">Tipo de valor: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="2e632-168">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="2e632-169">Valor de exemplo:</span><span class="sxs-lookup"><span data-stu-id="2e632-169">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="2e632-170">Voltar ao início</span><span class="sxs-lookup"><span data-stu-id="2e632-170">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="2e632-171">UpdateDefault</span><span class="sxs-lookup"><span data-stu-id="2e632-171">UpdateDefault</span></span>
#### <span data-ttu-id="2e632-172">Atualizar o padrão de substituição de política</span><span class="sxs-lookup"><span data-stu-id="2e632-172">Update policy override default</span></span>
><span data-ttu-id="2e632-173">Microsoft Edge Update 1.2.145.5 e posterior</span><span class="sxs-lookup"><span data-stu-id="2e632-173">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <span data-ttu-id="2e632-174">Descrição</span><span class="sxs-lookup"><span data-stu-id="2e632-174">Description</span></span>
<span data-ttu-id="2e632-175">Permite especificar o comportamento padrão para todos os canais referentes à maneira como o Microsoft Edge Update trata as atualizações disponíveis para o Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2e632-175">Lets you specify the default behavior for all channels concerning the way Microsoft Edge Update handles available updates for Microsoft Edge.</span></span> <span data-ttu-id="2e632-176">Pode ser substituído para canais individuais ao especificar a política '[Atualizar a substituição de política](#update)' para esses canais específicos.</span><span class="sxs-lookup"><span data-stu-id="2e632-176">Can be overridden for individual channels by specifying the '[Update policy override](#update)' policy for those specific channels.</span></span>

  <span data-ttu-id="2e632-177">Se você habilitar essa política, o Microsoft Edge Update tratará as atualizações do Microsoft Edge de acordo com as seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="2e632-177">If you enable this policy, Microsoft Edge Update handles Microsoft Edge updates according to how you configure the following options:</span></span>
   - <span data-ttu-id="2e632-178">Sempre permitir atualizações: as atualizações sempre serão aplicadas quando forem encontradas por uma verificação de atualização periódica ou por uma verificação de atualização manual.</span><span class="sxs-lookup"><span data-stu-id="2e632-178">Always allow updates: Updates are always applied when found, either by periodic update check or by a manual update check.</span></span>
   - <span data-ttu-id="2e632-179">Somente atualizações silenciosas automáticas: as atualizações serão aplicadas somente quando forem encontradas pela verificação de atualização periódica.</span><span class="sxs-lookup"><span data-stu-id="2e632-179">Automatic silent updates only: Updates are applied only when they're found by the periodic update check.</span></span>
   - <span data-ttu-id="2e632-180">Somente atualizações manuais: as atualizações serão aplicadas somente quando o usuário executar uma verificação de atualização manual.</span><span class="sxs-lookup"><span data-stu-id="2e632-180">Manual updates only: Updates are applied only when the user runs a manual update check.</span></span>
   - <span data-ttu-id="2e632-181">Atualizações desabilitadas: as atualizações nunca serão aplicadas.</span><span class="sxs-lookup"><span data-stu-id="2e632-181">Updates disabled: Updates are never applied.</span></span>

  <span data-ttu-id="2e632-182">Se você selecionar atualizações manuais, verifique periodicamente se há atualizações usando o mecanismo de atualizações manuais do aplicativo, se disponível.</span><span class="sxs-lookup"><span data-stu-id="2e632-182">If you select manual updates, make sure you periodically check for updates by using the app's manual update mechanism, if available.</span></span> <span data-ttu-id="2e632-183">Se você desabilitar as atualizações, verifique periodicamente se há atualizações e as distribua aos usuários.</span><span class="sxs-lookup"><span data-stu-id="2e632-183">If you disable updates, periodically check for updates, and distribute them to users.</span></span>

  <span data-ttu-id="2e632-184">Se você não habilitar e configurar essa política, o Microsoft Edge Update trata as atualizações disponíveis conforme especificado pela política '[Atualizar a substituição de política"](#update)'.</span><span class="sxs-lookup"><span data-stu-id="2e632-184">If you don't enable and configure this policy, Microsoft Edge Update handles available updates as specified by the '[Update policy override](#update)' policy.</span></span>
#### <span data-ttu-id="2e632-185">Informações e configurações do Windows</span><span class="sxs-lookup"><span data-stu-id="2e632-185">Windows information and settings</span></span>
##### <span data-ttu-id="2e632-186">Informações da Política de Grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="2e632-186">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="2e632-187">Nome exclusivo da Política de Grupo: UpdateDefault</span><span class="sxs-lookup"><span data-stu-id="2e632-187">GP unique name: UpdateDefault</span></span>
- <span data-ttu-id="2e632-188">Nome da Política de Grupo: Atualizar o padrão de substituição de política</span><span class="sxs-lookup"><span data-stu-id="2e632-188">GP name: Update policy override default</span></span>
- <span data-ttu-id="2e632-189">Caminho da Política de Grupo: Modelos Administrativos/Microsoft Edge Update/Aplicativos</span><span class="sxs-lookup"><span data-stu-id="2e632-189">GP path: Administrative Templates/Microsoft Edge Update/Applications</span></span>
- <span data-ttu-id="2e632-190">Nome do arquivo de ADMX da Política de Grupo: edgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="2e632-190">GP ADMX file name: edgeupdate.admx</span></span>
##### <span data-ttu-id="2e632-191">Configurações de registro do Windows</span><span class="sxs-lookup"><span data-stu-id="2e632-191">Windows Registry Settings</span></span>
- <span data-ttu-id="2e632-192">Caminho: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="2e632-192">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="2e632-193">Nome do valor: UpdateDefault</span><span class="sxs-lookup"><span data-stu-id="2e632-193">Value Name: UpdateDefault</span></span>
- <span data-ttu-id="2e632-194">Tipo de valor: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="2e632-194">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="2e632-195">Valor de exemplo:</span><span class="sxs-lookup"><span data-stu-id="2e632-195">Example value:</span></span>
```
0x00000003
```
[<span data-ttu-id="2e632-196">Voltar ao início</span><span class="sxs-lookup"><span data-stu-id="2e632-196">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="2e632-197">Install</span><span class="sxs-lookup"><span data-stu-id="2e632-197">Install</span></span>
#### <span data-ttu-id="2e632-198">Permitir instalação</span><span class="sxs-lookup"><span data-stu-id="2e632-198">Allow installation</span></span>
><span data-ttu-id="2e632-199">Microsoft Edge Update 1.2.145.5 e posterior</span><span class="sxs-lookup"><span data-stu-id="2e632-199">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <span data-ttu-id="2e632-200">Description</span><span class="sxs-lookup"><span data-stu-id="2e632-200">Description</span></span>
<span data-ttu-id="2e632-201">Especifica se um canal do Microsoft Edge pode ser instalado usando o Microsoft Edge Update.</span><span class="sxs-lookup"><span data-stu-id="2e632-201">Specifies whether a Microsoft Edge channel can be installed using Microsoft Edge Update.</span></span>

  <span data-ttu-id="2e632-202">Se você habilitar essa política para um canal, os usuários poderão instalar esse canal do Microsoft Edge por meio do Microsoft Edge Update.</span><span class="sxs-lookup"><span data-stu-id="2e632-202">If you enable this policy for a channel, users can install that channel of Microsoft Edge through Microsoft Edge Update.</span></span>

  <span data-ttu-id="2e632-203">Se você desabilitar essa política para um canal, os usuários não poderão instalar esse canal do Microsoft Edge por meio do Microsoft Edge Update.</span><span class="sxs-lookup"><span data-stu-id="2e632-203">If you disable this policy for a channel, users cannot install that channel of Microsoft Edge through Microsoft Edge Update.</span></span>

  <span data-ttu-id="2e632-204">Se você não configurar essa política para um canal, a configuração da política '[Permitir padrão de instalação](#installdefault)' determinará se os usuários podem instalar esse canal do Microsoft Edge por meio do Microsoft Edge Update.</span><span class="sxs-lookup"><span data-stu-id="2e632-204">If you don't configure this policy for a channel, the '[Allow installation default](#installdefault)' policy configuration determines whether users can install that channel of Microsoft Edge through Microsoft Edge Update.</span></span>
#### <span data-ttu-id="2e632-205">Informações e configurações do Windows</span><span class="sxs-lookup"><span data-stu-id="2e632-205">Windows information and settings</span></span>
##### <span data-ttu-id="2e632-206">Informações da Política de Grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="2e632-206">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="2e632-207">Nome exclusivo da Política de Grupo: Install</span><span class="sxs-lookup"><span data-stu-id="2e632-207">GP unique name: Install</span></span>
- <span data-ttu-id="2e632-208">Nome da Política de Grupo: Permitir instalação</span><span class="sxs-lookup"><span data-stu-id="2e632-208">GP name: Allow installation</span></span>
- <span data-ttu-id="2e632-209">Caminho da Política de Grupo:</span><span class="sxs-lookup"><span data-stu-id="2e632-209">GP path:</span></span> 
  - <span data-ttu-id="2e632-210">Modelos Administrativos/Microsoft Edge Update/Aplicativos/Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="2e632-210">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span></span>
  - <span data-ttu-id="2e632-211">Modelos Administrativos/Microsoft Edge Update/Aplicativos/Microsoft Edge Beta</span><span class="sxs-lookup"><span data-stu-id="2e632-211">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span></span>
  - <span data-ttu-id="2e632-212">Modelos Administrativos/Microsoft Edge Update/Aplicativos/Microsoft Edge Canary</span><span class="sxs-lookup"><span data-stu-id="2e632-212">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span></span>
  - <span data-ttu-id="2e632-213">Modelos Administrativos/Microsoft Edge Update/Aplicativos/Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="2e632-213">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span></span>
- <span data-ttu-id="2e632-214">Nome do arquivo de ADMX da Política de Grupo: edgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="2e632-214">GP ADMX file name: edgeupdate.admx</span></span>
##### <span data-ttu-id="2e632-215">Configurações de registro do Windows</span><span class="sxs-lookup"><span data-stu-id="2e632-215">Windows Registry Settings</span></span>
- <span data-ttu-id="2e632-216">Caminho: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="2e632-216">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="2e632-217">Nome do valor:</span><span class="sxs-lookup"><span data-stu-id="2e632-217">Value Name:</span></span> 
  - <span data-ttu-id="2e632-218">(Estável): Install{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span><span class="sxs-lookup"><span data-stu-id="2e632-218">(Stable): Install{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span></span>
  - <span data-ttu-id="2e632-219">(Beta): Install{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span><span class="sxs-lookup"><span data-stu-id="2e632-219">(Beta): Install{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span></span>
  - <span data-ttu-id="2e632-220">(Canary): Install{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span><span class="sxs-lookup"><span data-stu-id="2e632-220">(Canary): Install{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span></span>
  - <span data-ttu-id="2e632-221">(Dev): Install{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span><span class="sxs-lookup"><span data-stu-id="2e632-221">(Dev): Install{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span></span>
- <span data-ttu-id="2e632-222">Tipo de valor: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="2e632-222">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="2e632-223">Valor de exemplo:</span><span class="sxs-lookup"><span data-stu-id="2e632-223">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="2e632-224">Voltar ao início</span><span class="sxs-lookup"><span data-stu-id="2e632-224">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="2e632-225">Update</span><span class="sxs-lookup"><span data-stu-id="2e632-225">Update</span></span>
#### <span data-ttu-id="2e632-226">Atualizar a substituição de política</span><span class="sxs-lookup"><span data-stu-id="2e632-226">Update policy override</span></span>
><span data-ttu-id="2e632-227">Microsoft Edge Update 1.2.145.5 e posterior</span><span class="sxs-lookup"><span data-stu-id="2e632-227">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <span data-ttu-id="2e632-228">Descrição</span><span class="sxs-lookup"><span data-stu-id="2e632-228">Description</span></span>
<span data-ttu-id="2e632-229">Especifica como o Microsoft Edge Update trata as atualizações disponíveis do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2e632-229">Specifies how Microsoft Edge Update handles available updates from Microsoft Edge.</span></span>

  <span data-ttu-id="2e632-230">Se você habilitar essa política, o Microsoft Edge Update tratará as atualizações do Microsoft Edge de acordo com as seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="2e632-230">If you enable this policy, Microsoft Edge Update handles Microsoft Edge updates according to how you configure the following options:</span></span>
   - <span data-ttu-id="2e632-231">Sempre permitir atualizações: as atualizações sempre serão aplicadas quando forem encontradas por uma verificação de atualização periódica ou por uma verificação de atualização manual.</span><span class="sxs-lookup"><span data-stu-id="2e632-231">Always allow updates: Updates are always applied when found, either by periodic update check or by a manual update check.</span></span>
   - <span data-ttu-id="2e632-232">Somente atualizações silenciosas automáticas: as atualizações serão aplicadas somente quando forem encontradas pela verificação de atualização periódica.</span><span class="sxs-lookup"><span data-stu-id="2e632-232">Automatic silent updates only: Updates are applied only when they're found by the periodic update check.</span></span>
   - <span data-ttu-id="2e632-233">Somente atualizações manuais: as atualizações serão aplicadas somente quando o usuário executar uma verificação de atualização manual.</span><span class="sxs-lookup"><span data-stu-id="2e632-233">Manual updates only: Updates are applied only when the user runs a manual update check.</span></span> <span data-ttu-id="2e632-234">(Nem todos os aplicativos fornecem uma interface para essa opção.)</span><span class="sxs-lookup"><span data-stu-id="2e632-234">(Not all apps provide an interface for this option.)</span></span>
   - <span data-ttu-id="2e632-235">Atualizações desabilitadas: as atualizações nunca serão aplicadas.</span><span class="sxs-lookup"><span data-stu-id="2e632-235">Updates disabled: Updates are never applied.</span></span>

  <span data-ttu-id="2e632-236">Se você selecionar atualizações manuais, verifique periodicamente se há atualizações usando o mecanismo de atualizações manuais do aplicativo, se disponível.</span><span class="sxs-lookup"><span data-stu-id="2e632-236">If you select manual updates, make sure you periodically check for updates by using the app's manual update mechanism, if available.</span></span> <span data-ttu-id="2e632-237">Se você desabilitar as atualizações, verifique periodicamente se há atualizações e as distribua aos usuários.</span><span class="sxs-lookup"><span data-stu-id="2e632-237">If you disable updates, periodically check for updates, and distribute them to users.</span></span>

  <span data-ttu-id="2e632-238">Se você não habilitar e configurar essa política, o Microsoft Edge Update tratará as atualizações disponíveis conforme especificado pela política '[Atualizar a substituição de política padrão](#updatedefault)'.</span><span class="sxs-lookup"><span data-stu-id="2e632-238">If you don't enable and configure this policy, Microsoft Edge Update handles available updates as specified by the '[Update policy override default](#updatedefault)' policy.</span></span>
#### <span data-ttu-id="2e632-239">Informações e configurações do Windows</span><span class="sxs-lookup"><span data-stu-id="2e632-239">Windows information and settings</span></span>
##### <span data-ttu-id="2e632-240">Informações da Política de Grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="2e632-240">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="2e632-241">Nome exclusivo da Política de Grupo: Update</span><span class="sxs-lookup"><span data-stu-id="2e632-241">GP unique name: Update</span></span>
- <span data-ttu-id="2e632-242">Nome da Política de Grupo: Atualizar a substituição de política</span><span class="sxs-lookup"><span data-stu-id="2e632-242">GP name: Update policy override</span></span>
- <span data-ttu-id="2e632-243">Caminho da Política de Grupo:</span><span class="sxs-lookup"><span data-stu-id="2e632-243">GP path:</span></span> 
  - <span data-ttu-id="2e632-244">Modelos Administrativos/Microsoft Edge Update/Aplicativos/Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="2e632-244">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span></span>
  - <span data-ttu-id="2e632-245">Modelos Administrativos/Microsoft Edge Update/Aplicativos/Microsoft Edge Beta</span><span class="sxs-lookup"><span data-stu-id="2e632-245">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span></span>
  - <span data-ttu-id="2e632-246">Modelos Administrativos/Microsoft Edge Update/Aplicativos/Microsoft Edge Canary</span><span class="sxs-lookup"><span data-stu-id="2e632-246">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span></span>
  - <span data-ttu-id="2e632-247">Modelos Administrativos/Microsoft Edge Update/Aplicativos/Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="2e632-247">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span></span>
- <span data-ttu-id="2e632-248">Nome do arquivo de ADMX da Política de Grupo: edgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="2e632-248">GP ADMX file name: edgeupdate.admx</span></span>
##### <span data-ttu-id="2e632-249">Configurações de registro do Windows</span><span class="sxs-lookup"><span data-stu-id="2e632-249">Windows Registry Settings</span></span>
- <span data-ttu-id="2e632-250">Caminho: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="2e632-250">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="2e632-251">Nome do valor:</span><span class="sxs-lookup"><span data-stu-id="2e632-251">Value Name:</span></span> 
  - <span data-ttu-id="2e632-252">(Estável): Update{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span><span class="sxs-lookup"><span data-stu-id="2e632-252">(Stable): Update{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span></span>
  - <span data-ttu-id="2e632-253">(Beta): Update{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span><span class="sxs-lookup"><span data-stu-id="2e632-253">(Beta): Update{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span></span>
  - <span data-ttu-id="2e632-254">(Canary): Update{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span><span class="sxs-lookup"><span data-stu-id="2e632-254">(Canary): Update{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span></span>
  - <span data-ttu-id="2e632-255">(Dev): Update{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span><span class="sxs-lookup"><span data-stu-id="2e632-255">(Dev): Update{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span></span>
- <span data-ttu-id="2e632-256">Tipo de valor: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="2e632-256">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="2e632-257">Valor de exemplo:</span><span class="sxs-lookup"><span data-stu-id="2e632-257">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="2e632-258">Voltar ao início</span><span class="sxs-lookup"><span data-stu-id="2e632-258">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="2e632-259">Allowsxs</span><span class="sxs-lookup"><span data-stu-id="2e632-259">Allowsxs</span></span>
#### <span data-ttu-id="2e632-260">Permitir a experiência de navegador Lado a Lado do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="2e632-260">Allow Microsoft Edge Side by Side browser experience</span></span>
><span data-ttu-id="2e632-261">Microsoft Edge Update 1.2.145.5 e posterior</span><span class="sxs-lookup"><span data-stu-id="2e632-261">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <span data-ttu-id="2e632-262">Description</span><span class="sxs-lookup"><span data-stu-id="2e632-262">Description</span></span>
<span data-ttu-id="2e632-263">Essa política permite que um usuário execute o Microsoft Edge (Edge HTML) e o Microsoft Edge (baseado no Chromium) lado a lado.</span><span class="sxs-lookup"><span data-stu-id="2e632-263">This policy lets a user run Microsoft Edge (Edge HTML) and Microsoft Edge (Chromium-based) side-by-side.</span></span>

<span data-ttu-id="2e632-264">Se essa política for definida como "Não configurada", o Microsoft Edge (baseado no Chromium) substituirá o Microsoft Edge (HTML do Edge) depois que o canal Estável do Microsoft Edge (baseado no Chromium) e as atualizações de segurança de novembro de 2019 forem instalados.</span><span class="sxs-lookup"><span data-stu-id="2e632-264">If this policy is set to “Not configured”, Microsoft Edge (Chromium-based) will replace Microsoft Edge (Edge HTML) after the Microsoft Edge (Chromium-based) stable channel and the November 2019 security updates are installed.</span></span>  <span data-ttu-id="2e632-265">Esse comportamento é igual à configuração "Desabilitada".</span><span class="sxs-lookup"><span data-stu-id="2e632-265">This is the same behavior as the “Disabled” setting.</span></span>

<span data-ttu-id="2e632-266">A configuração "Desabilitada" bloqueia uma experiência lado a lado, e o Microsoft Edge (baseado no Chromium) substituirá o Microsoft Edge (HTML do Edge) depois que o canal Estável do Microsoft Edge (baseado no Chromium) e as atualizações de segurança de novembro de 2019 forem instalados.</span><span class="sxs-lookup"><span data-stu-id="2e632-266">The “Disabled” setting blocks a side-by-side experience and Microsoft Edge (Chromium-based) will replace Microsoft Edge (Edge HTML) after the Microsoft Edge (Chromium-based) stable channel and the November 2019 security updates are installed.</span></span>  <span data-ttu-id="2e632-267">Esse comportamento é igual à configuração "Não configurada".</span><span class="sxs-lookup"><span data-stu-id="2e632-267">This is the same behavior as the “Not Configured” setting.</span></span>

<span data-ttu-id="2e632-268">Quando essa política for "Habilitada", o Microsoft Edge (baseado no Chromium) e o Microsoft Edge (Edge HTML) poderão ser executados lado a lado depois que o Microsoft Edge (baseado no Chromium) for instalado.</span><span class="sxs-lookup"><span data-stu-id="2e632-268">When this policy is “Enabled”, Microsoft Edge (Chromium-based) and Microsoft Edge (Edge HTML) can run side-by-side after Microsoft Edge (Chromium-based) is installed.</span></span>

<span data-ttu-id="2e632-269">Para que essa política de grupo entre em vigor, ela deve ser configurada antes da instalação automática do Microsoft Edge (baseado no Chromium) pelo Windows Update.</span><span class="sxs-lookup"><span data-stu-id="2e632-269">For this group policy to take affect, it must be configured before the automatic install of Microsoft Edge (Chromium-based) by Windows Update.</span></span> <span data-ttu-id="2e632-270">Observação: um usuário pode bloquear a atualização automática do Microsoft Edge (baseado no Chromium) usando o kit de ferramentas do bloqueador do Microsoft Edge (baseado no Chromium).</span><span class="sxs-lookup"><span data-stu-id="2e632-270">Note: A user can block the automatic update of Microsoft Edge (Chromium-based) by using the Microsoft Edge (Chromium-based) Blocker Toolkit.</span></span>
#### <span data-ttu-id="2e632-271">Informações e configurações do Windows</span><span class="sxs-lookup"><span data-stu-id="2e632-271">Windows information and settings</span></span>
##### <span data-ttu-id="2e632-272">Informações da Política de Grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="2e632-272">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="2e632-273">Nome exclusivo da Política de Grupo: Allowsxs</span><span class="sxs-lookup"><span data-stu-id="2e632-273">GP unique name: Allowsxs</span></span>
- <span data-ttu-id="2e632-274">Nome da Política de Grupo: Permitir a experiência de navegador Lado a Lado do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="2e632-274">GP name: Allow Microsoft Edge Side by Side browser experience</span></span>
- <span data-ttu-id="2e632-275">Caminho da Política de Grupo: Modelos Administrativos/Microsoft Edge Update/Aplicativos</span><span class="sxs-lookup"><span data-stu-id="2e632-275">GP path: Administrative Templates/Microsoft Edge Update/Applications</span></span>
- <span data-ttu-id="2e632-276">Nome do arquivo de ADMX da Política de Grupo: edgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="2e632-276">GP ADMX file name: edgeupdate.admx</span></span>
##### <span data-ttu-id="2e632-277">Configurações de registro do Windows</span><span class="sxs-lookup"><span data-stu-id="2e632-277">Windows Registry Settings</span></span>
- <span data-ttu-id="2e632-278">Caminho: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="2e632-278">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="2e632-279">Nome do valor:Allowsxs</span><span class="sxs-lookup"><span data-stu-id="2e632-279">Value Name: Allowsxs</span></span>
- <span data-ttu-id="2e632-280">Tipo de valor: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="2e632-280">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="2e632-281">Valor de exemplo:</span><span class="sxs-lookup"><span data-stu-id="2e632-281">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="2e632-282">Voltar ao início</span><span class="sxs-lookup"><span data-stu-id="2e632-282">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="2e632-283">CreateDesktopShortcutDefault</span><span class="sxs-lookup"><span data-stu-id="2e632-283">CreateDesktopShortcutDefault</span></span>
#### <span data-ttu-id="2e632-284">Impedir a criação de Atalho da Área de Trabalho com a instalação padrão</span><span class="sxs-lookup"><span data-stu-id="2e632-284">Prevent Desktop Shortcut creation upon install default</span></span>
><span data-ttu-id="2e632-285">Microsoft Edge Update 1.3.128.0 e posterior</span><span class="sxs-lookup"><span data-stu-id="2e632-285">Microsoft Edge Update 1.3.128.0 and later</span></span>

#### <span data-ttu-id="2e632-286">Descrição</span><span class="sxs-lookup"><span data-stu-id="2e632-286">Description</span></span>
<span data-ttu-id="2e632-287">Permite especificar o comportamento padrão de todos os canais para criar um atalho da área de trabalho quando o Microsoft Edge for instalado.</span><span class="sxs-lookup"><span data-stu-id="2e632-287">Lets you specify the default behavior for all channels for creating a desktop shortcut when Microsoft Edge is installed.</span></span>

  <span data-ttu-id="2e632-288">Se você habilitar esta política, um atalho da área de trabalho será criado quando o Microsoft Edge for instalado.</span><span class="sxs-lookup"><span data-stu-id="2e632-288">If you enable this policy a desktop shortcut is created when Microsoft Edge is installed.</span></span>
<span data-ttu-id="2e632-289">Se você desabilitar esta política, nenhum atalho da área de trabalho será criado quando o Microsoft Edge for instalado.</span><span class="sxs-lookup"><span data-stu-id="2e632-289">If you disable this policy, no desktop shortcut will be created when Microsoft Edge is installed.</span></span>
<span data-ttu-id="2e632-290">Se você não configurar esta política, um atalho da área de trabalho para o Microsoft Edge será criado durante a instalação.</span><span class="sxs-lookup"><span data-stu-id="2e632-290">If you don’t configure this policy a desktop shortcut to Microsoft Edge will be created during installation.</span></span>
<span data-ttu-id="2e632-291">Se o Microsoft Edge já estiver instalado, esta política não terá efeito.</span><span class="sxs-lookup"><span data-stu-id="2e632-291">If Microsoft Edge is already installed, this policy will have no effect.</span></span>
#### <span data-ttu-id="2e632-292">Informações e configurações do Windows</span><span class="sxs-lookup"><span data-stu-id="2e632-292">Windows information and settings</span></span>
##### <span data-ttu-id="2e632-293">Informações da Política de Grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="2e632-293">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="2e632-294">Nome exclusivo da Política de Grupo: CreateDesktopShortcutDefault</span><span class="sxs-lookup"><span data-stu-id="2e632-294">GP unique name: CreateDesktopShortcutDefault</span></span>
- <span data-ttu-id="2e632-295">Nome da Política de Grupo: Impedir a criação de Atalho da Área de Trabalho com a instalação padrão</span><span class="sxs-lookup"><span data-stu-id="2e632-295">GP name: Prevent Desktop Shortcut creation upon install default</span></span>
- <span data-ttu-id="2e632-296">Caminho da Política Padrão: Modelos Administrativos/Microsoft Edge Update/Aplicativos</span><span class="sxs-lookup"><span data-stu-id="2e632-296">GP path: Administrative Templates/Microsoft Edge Update/Applications</span></span>
- <span data-ttu-id="2e632-297">Nome do arquivo de ADMX da Política de Grupo: edgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="2e632-297">GP ADMX file name: edgeupdate.admx</span></span>
##### <span data-ttu-id="2e632-298">Configurações de registro do Windows</span><span class="sxs-lookup"><span data-stu-id="2e632-298">Windows Registry Settings</span></span>
- <span data-ttu-id="2e632-299">Caminho: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="2e632-299">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="2e632-300">Nome do Valor: CreateDesktopShortcutDefault</span><span class="sxs-lookup"><span data-stu-id="2e632-300">Value Name: CreateDesktopShortcutDefault</span></span>
- <span data-ttu-id="2e632-301">Tipo de valor: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="2e632-301">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="2e632-302">Valor de exemplo:</span><span class="sxs-lookup"><span data-stu-id="2e632-302">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="2e632-303">Voltar ao início</span><span class="sxs-lookup"><span data-stu-id="2e632-303">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="2e632-304">CreateDesktopShortcut</span><span class="sxs-lookup"><span data-stu-id="2e632-304">CreateDesktopShortcut</span></span>
#### <span data-ttu-id="2e632-305">Impedir a criação de Atalho da Área de Trabalho com a instalação</span><span class="sxs-lookup"><span data-stu-id="2e632-305">Prevent Desktop Shortcut creation upon install</span></span>
><span data-ttu-id="2e632-306">Microsoft Edge Update 1.3.128.0 e posterior</span><span class="sxs-lookup"><span data-stu-id="2e632-306">Microsoft Edge Update 1.3.128.0 and later</span></span>

#### <span data-ttu-id="2e632-307">Descrição</span><span class="sxs-lookup"><span data-stu-id="2e632-307">Description</span></span>
<span data-ttu-id="2e632-308">Se você habilitar esta política, um atalho da área de trabalho será criado quando o Microsoft Edge for instalado.</span><span class="sxs-lookup"><span data-stu-id="2e632-308">If you enable this policy a desktop shortcut is created when Microsoft Edge is installed.</span></span>
<span data-ttu-id="2e632-309">Se você desabilitar esta política, nenhum atalho da área de trabalho será criado quando o Microsoft Edge for instalado.</span><span class="sxs-lookup"><span data-stu-id="2e632-309">If you disable this policy, no desktop shortcut will be created when Microsoft Edge is installed.</span></span>
<span data-ttu-id="2e632-310">Se você não configurar esta política, um atalho da área de trabalho para o Microsoft Edge será criado durante a instalação.</span><span class="sxs-lookup"><span data-stu-id="2e632-310">If you don’t configure this policy a desktop shortcut to Microsoft Edge will be created during installation.</span></span>
<span data-ttu-id="2e632-311">Se o Microsoft Edge já estiver instalado, esta política não terá efeito.</span><span class="sxs-lookup"><span data-stu-id="2e632-311">If Microsoft Edge is already installed, this policy will have no effect.</span></span>

  <span data-ttu-id="2e632-312">Se você não configurar esta política para um canal, a configuração de política padrão '[Evitar a criação de um Atalho no Desktop ao instalar](#createdesktopshortcutdefault)' determinará a criação de um atalho quando o Microsoft Edge for instalado.</span><span class="sxs-lookup"><span data-stu-id="2e632-312">If you don't configure this policy for a channel, the '[Prevent Desktop Shortcut creation upon install default](#createdesktopshortcutdefault)' policy configuration determines shortcut creation when Microsoft Edge is installed.</span></span>
#### <span data-ttu-id="2e632-313">Informações e configurações do Windows</span><span class="sxs-lookup"><span data-stu-id="2e632-313">Windows information and settings</span></span>
##### <span data-ttu-id="2e632-314">Informações da Política de Grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="2e632-314">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="2e632-315">Nome exclusivo da Política de Grupo: CreateDesktopShortcut</span><span class="sxs-lookup"><span data-stu-id="2e632-315">GP unique name: CreateDesktopShortcut</span></span>
- <span data-ttu-id="2e632-316">Nome da GP: Impedir a criação de Atalho da Área de Trabalho com a instalação</span><span class="sxs-lookup"><span data-stu-id="2e632-316">GP name: Prevent Desktop Shortcut creation upon install</span></span>
- <span data-ttu-id="2e632-317">Caminho da Política de Grupo:</span><span class="sxs-lookup"><span data-stu-id="2e632-317">GP path:</span></span> 
  - <span data-ttu-id="2e632-318">Modelos Administrativos/Microsoft Edge Update/Aplicativos/Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="2e632-318">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span></span>
  - <span data-ttu-id="2e632-319">Modelos Administrativos/Microsoft Edge Update/Aplicativos/Microsoft Edge Beta</span><span class="sxs-lookup"><span data-stu-id="2e632-319">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span></span>
  - <span data-ttu-id="2e632-320">Modelos Administrativos/Microsoft Edge Update/Aplicativos/Microsoft Edge Canary</span><span class="sxs-lookup"><span data-stu-id="2e632-320">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span></span>
  - <span data-ttu-id="2e632-321">Modelos Administrativos/Microsoft Edge Update/Aplicativos/Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="2e632-321">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span></span>
- <span data-ttu-id="2e632-322">Nome do arquivo de ADMX da Política de Grupo: edgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="2e632-322">GP ADMX file name: edgeupdate.admx</span></span>
##### <span data-ttu-id="2e632-323">Configurações de registro do Windows</span><span class="sxs-lookup"><span data-stu-id="2e632-323">Windows Registry Settings</span></span>
- <span data-ttu-id="2e632-324">Caminho: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="2e632-324">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="2e632-325">Nome do valor:</span><span class="sxs-lookup"><span data-stu-id="2e632-325">Value Name:</span></span> 
  - <span data-ttu-id="2e632-326">(Estável): CreateDesktopShortcut{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span><span class="sxs-lookup"><span data-stu-id="2e632-326">(Stable): CreateDesktopShortcut{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span></span>
  - <span data-ttu-id="2e632-327">(Beta): CreateDesktopShortcut{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span><span class="sxs-lookup"><span data-stu-id="2e632-327">(Beta): CreateDesktopShortcut{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span></span>
  - <span data-ttu-id="2e632-328">(Canary): CreateDesktopShortcut{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span><span class="sxs-lookup"><span data-stu-id="2e632-328">(Canary): CreateDesktopShortcut{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span></span>
  - <span data-ttu-id="2e632-329">(Dev): CreateDesktopShortcut{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span><span class="sxs-lookup"><span data-stu-id="2e632-329">(Dev): CreateDesktopShortcut{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span></span>
- <span data-ttu-id="2e632-330">Tipo de valor: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="2e632-330">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="2e632-331">Valor de exemplo:</span><span class="sxs-lookup"><span data-stu-id="2e632-331">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="2e632-332">Voltar ao início</span><span class="sxs-lookup"><span data-stu-id="2e632-332">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="2e632-333">TargetVersionPrefix</span><span class="sxs-lookup"><span data-stu-id="2e632-333">TargetVersionPrefix</span></span>
#### <span data-ttu-id="2e632-334">Substituir versão de destino</span><span class="sxs-lookup"><span data-stu-id="2e632-334">Target version override</span></span>
><span data-ttu-id="2e632-335">Microsoft Edge Update 1.3.119.43 e posterior</span><span class="sxs-lookup"><span data-stu-id="2e632-335">Microsoft Edge Update 1.3.119.43 and later</span></span>

#### <span data-ttu-id="2e632-336">Descrição</span><span class="sxs-lookup"><span data-stu-id="2e632-336">Description</span></span>
<span data-ttu-id="2e632-337">Quando esta política estiver habilitada e a atualização automática estiver habilitada, o Microsoft Edge será atualizado para a versão especificada por esse valor de política.</span><span class="sxs-lookup"><span data-stu-id="2e632-337">When this policy is enabled, and auto-update is enabled, Microsoft Edge will be updated to the version specified by this policy value.</span></span>

<span data-ttu-id="2e632-338">O valor da política deve ser uma versão do Microsoft Edge específica, por exemplo, 83.0.499.12.</span><span class="sxs-lookup"><span data-stu-id="2e632-338">The policy value must be a specific Microsoft Edge version, e.g. 83.0.499.12.</span></span>

<span data-ttu-id="2e632-339">Se um dispositivo tiver uma versão mais recente do Microsoft Edge do que o valor especificado, a versão mais recente do Microsoft Edge será mantida e ele não será revertido para a versão especificada.</span><span class="sxs-lookup"><span data-stu-id="2e632-339">If a device has newer version of Microsoft Edge than the value specified, Microsoft Edge will remain on the newer version and not downgrade to the specified version.</span></span>

<span data-ttu-id="2e632-340">Se a versão especificada não existir ou estiver formatada inadequadamente, o Microsoft Edge permanecerá na versão atual e não será atualizado para versões futuras automaticamente.</span><span class="sxs-lookup"><span data-stu-id="2e632-340">If the specified version does not exist, or is improperly formatted, then Microsoft Edge will remain on its current version and not update to future versions automatically.</span></span>
#### <span data-ttu-id="2e632-341">Informações e configurações do Windows</span><span class="sxs-lookup"><span data-stu-id="2e632-341">Windows information and settings</span></span>
##### <span data-ttu-id="2e632-342">Informações da Política de Grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="2e632-342">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="2e632-343">Nome exclusivo da Política de Grupo: TargetVersionPrefix</span><span class="sxs-lookup"><span data-stu-id="2e632-343">GP unique name: TargetVersionPrefix</span></span>
- <span data-ttu-id="2e632-344">Nome da Política de Grupo: Substituir versão de destino</span><span class="sxs-lookup"><span data-stu-id="2e632-344">GP name: Target version override</span></span>
- <span data-ttu-id="2e632-345">Caminho da Política de Grupo:</span><span class="sxs-lookup"><span data-stu-id="2e632-345">GP path:</span></span> 
  - <span data-ttu-id="2e632-346">Modelos Administrativos/Microsoft Edge Update/Aplicativos/Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="2e632-346">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span></span>
  - <span data-ttu-id="2e632-347">Modelos Administrativos/Microsoft Edge Update/Aplicativos/Microsoft Edge Beta</span><span class="sxs-lookup"><span data-stu-id="2e632-347">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span></span>
  - <span data-ttu-id="2e632-348">Modelos Administrativos/Microsoft Edge Update/Aplicativos/Microsoft Edge Canary</span><span class="sxs-lookup"><span data-stu-id="2e632-348">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span></span>
  - <span data-ttu-id="2e632-349">Modelos Administrativos/Microsoft Edge Update/Aplicativos/Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="2e632-349">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span></span>
- <span data-ttu-id="2e632-350">Nome do arquivo de ADMX da Política de Grupo: edgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="2e632-350">GP ADMX file name: edgeupdate.admx</span></span>
##### <span data-ttu-id="2e632-351">Configurações de registro do Windows</span><span class="sxs-lookup"><span data-stu-id="2e632-351">Windows Registry Settings</span></span>
- <span data-ttu-id="2e632-352">Caminho: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="2e632-352">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="2e632-353">Nome do valor:</span><span class="sxs-lookup"><span data-stu-id="2e632-353">Value Name:</span></span> 
  - <span data-ttu-id="2e632-354">(Estável): TargetVersionPrefix {56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span><span class="sxs-lookup"><span data-stu-id="2e632-354">(Stable): TargetVersionPrefix{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span></span>
  - <span data-ttu-id="2e632-355">(Beta): TargetVersionPrefix {2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span><span class="sxs-lookup"><span data-stu-id="2e632-355">(Beta): TargetVersionPrefix{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span></span>
  - <span data-ttu-id="2e632-356">(Canary): TargetVersionPrefix {65C35B14-6C1D-4122-AC46-7148CC9D6497}</span><span class="sxs-lookup"><span data-stu-id="2e632-356">(Canary): TargetVersionPrefix{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span></span>
  - <span data-ttu-id="2e632-357">(Dev): TargetVersionPrefix {0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span><span class="sxs-lookup"><span data-stu-id="2e632-357">(Dev): TargetVersionPrefix{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span></span>
- <span data-ttu-id="2e632-358">Tipo do valor: REG_SZ</span><span class="sxs-lookup"><span data-stu-id="2e632-358">Value Type: REG_SZ</span></span>
##### <span data-ttu-id="2e632-359">Valor de exemplo:</span><span class="sxs-lookup"><span data-stu-id="2e632-359">Example value:</span></span>
```
83.0.499.12
```
[<span data-ttu-id="2e632-360">Voltar ao início</span><span class="sxs-lookup"><span data-stu-id="2e632-360">Back to top</span></span>](#microsoft-edge---update-policies)


## <span data-ttu-id="2e632-361">Políticas de preferências</span><span class="sxs-lookup"><span data-stu-id="2e632-361">Preferences policies</span></span>

[<span data-ttu-id="2e632-362">Voltar ao início</span><span class="sxs-lookup"><span data-stu-id="2e632-362">Back to top</span></span>](#microsoft-edge---update-policies)
### <span data-ttu-id="2e632-363">AutoUpdateCheckPeriodMinutes</span><span class="sxs-lookup"><span data-stu-id="2e632-363">AutoUpdateCheckPeriodMinutes</span></span>
#### <span data-ttu-id="2e632-364">Atualizar automaticamente a substituição do período de verificação</span><span class="sxs-lookup"><span data-stu-id="2e632-364">Auto-update check period override</span></span>
><span data-ttu-id="2e632-365">Microsoft Edge Update 1.2.145.5 e posterior</span><span class="sxs-lookup"><span data-stu-id="2e632-365">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <span data-ttu-id="2e632-366">Descrição</span><span class="sxs-lookup"><span data-stu-id="2e632-366">Description</span></span>
<span data-ttu-id="2e632-367">Se habilitada, essa política permite definir um valor para o número mínimo de minutos entre as verificações de atualização automática.</span><span class="sxs-lookup"><span data-stu-id="2e632-367">If enabled, this policy lets you set a value for the minimum number of minutes between automatic update checks.</span></span> <span data-ttu-id="2e632-368">Caso contrário, por padrão, a verificação de atualização automática verifica se há as atualizações a cada 10 horas.</span><span class="sxs-lookup"><span data-stu-id="2e632-368">Otherwise, by default, auto-update checks for updates every 10 hours.</span></span>

  <span data-ttu-id="2e632-369">Se você quiser desabilitar todas as verificações de atualização automática, defina o valor como 0 (não recomendado).</span><span class="sxs-lookup"><span data-stu-id="2e632-369">If you want to disable all auto-update checks, set the value to 0 (not recommended).</span></span>
#### <span data-ttu-id="2e632-370">Informações e configurações do Windows</span><span class="sxs-lookup"><span data-stu-id="2e632-370">Windows information and settings</span></span>
##### <span data-ttu-id="2e632-371">Informações da Política de Grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="2e632-371">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="2e632-372">Nome exclusivo da Política de Grupo: AutoUpdateCheckPeriodMinutes</span><span class="sxs-lookup"><span data-stu-id="2e632-372">GP unique name: AutoUpdateCheckPeriodMinutes</span></span>
- <span data-ttu-id="2e632-373">Nome da Política de Grupo: Atualizar automaticamente a substituição do período de verificação</span><span class="sxs-lookup"><span data-stu-id="2e632-373">GP name: Auto-update check period override</span></span>
- <span data-ttu-id="2e632-374">Caminho da Política de Grupo: Modelos Administrativos/Microsoft Edge Update/Preferências</span><span class="sxs-lookup"><span data-stu-id="2e632-374">GP path: Administrative Templates/Microsoft Edge Update/Preferences</span></span>
- <span data-ttu-id="2e632-375">Nome do arquivo de ADMX da Política de Grupo: edgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="2e632-375">GP ADMX file name: edgeupdate.admx</span></span>
##### <span data-ttu-id="2e632-376">Configurações de registro do Windows</span><span class="sxs-lookup"><span data-stu-id="2e632-376">Windows Registry Settings</span></span>
- <span data-ttu-id="2e632-377">Caminho: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="2e632-377">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="2e632-378">Nome do valor: AutoUpdateCheckPeriodMinutes</span><span class="sxs-lookup"><span data-stu-id="2e632-378">Value Name: AutoUpdateCheckPeriodMinutes</span></span>
- <span data-ttu-id="2e632-379">Tipo de valor: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="2e632-379">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="2e632-380">Valor de exemplo:</span><span class="sxs-lookup"><span data-stu-id="2e632-380">Example value:</span></span>
```
0x00000578
```
[<span data-ttu-id="2e632-381">Voltar ao início</span><span class="sxs-lookup"><span data-stu-id="2e632-381">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="2e632-382">UpdatesSuppressed</span><span class="sxs-lookup"><span data-stu-id="2e632-382">UpdatesSuppressed</span></span>
#### <span data-ttu-id="2e632-383">Período em cada dia para suprimir a verificação de atualização automática</span><span class="sxs-lookup"><span data-stu-id="2e632-383">Time period in each day to suppress auto-update check</span></span>
><span data-ttu-id="2e632-384">Microsoft Edge Update 1.3.33.5 e posterior</span><span class="sxs-lookup"><span data-stu-id="2e632-384">Microsoft Edge Update 1.3.33.5 and later</span></span>

#### <span data-ttu-id="2e632-385">Descrição</span><span class="sxs-lookup"><span data-stu-id="2e632-385">Description</span></span>
<span data-ttu-id="2e632-386">Se você habilitar essa política, as verificações de atualização serão suprimidas por dia a partir de Hora:Minuto por um período de duração (em minutos).</span><span class="sxs-lookup"><span data-stu-id="2e632-386">If you enable this policy, update checks are suppressed each day starting at Hour:Minute for a period of Duration (in minutes).</span></span> <span data-ttu-id="2e632-387">A duração não é afetada pelo horário de verão.</span><span class="sxs-lookup"><span data-stu-id="2e632-387">Duration isn't affected by daylight saving time.</span></span> <span data-ttu-id="2e632-388">Por exemplo, se o horário de início for 22:00 e a duração for de 480 minutos, as atualizações serão suprimidas por exatamente oito horas, independentemente do horário de verão começar ou terminar durante esse período.</span><span class="sxs-lookup"><span data-stu-id="2e632-388">For example, if the start time is 22:00 and the duration is 480 minutes, updates will be suppressed for exactly 8 hours, regardless of whether daylight saving time starts or ends during this period.</span></span>

  <span data-ttu-id="2e632-389">Se você desabilitar ou não configurar essa política, as verificações de atualização não serão suprimidas durante nenhum período específico.</span><span class="sxs-lookup"><span data-stu-id="2e632-389">If you disable or don't configure this policy, update checks aren't suppressed during any specific period.</span></span>
#### <span data-ttu-id="2e632-390">Informações e configurações do Windows</span><span class="sxs-lookup"><span data-stu-id="2e632-390">Windows information and settings</span></span>
##### <span data-ttu-id="2e632-391">Informações da Política de Grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="2e632-391">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="2e632-392">Nome exclusivo da Política de Grupo: UpdatesSuppressed</span><span class="sxs-lookup"><span data-stu-id="2e632-392">GP unique name: UpdatesSuppressed</span></span>
- <span data-ttu-id="2e632-393">Nome da Política de Grupo: Período em cada dia para suprimir a verificação de atualização automática</span><span class="sxs-lookup"><span data-stu-id="2e632-393">GP name: Time period in each day to suppress auto-update check</span></span>
  - <span data-ttu-id="2e632-394">Opções { Hour, Minute, Duration }</span><span class="sxs-lookup"><span data-stu-id="2e632-394">Options { Hour, Minute, Duration }</span></span>
- <span data-ttu-id="2e632-395">Caminho da Política de Grupo: Modelos Administrativos/Microsoft Edge Update/Preferências</span><span class="sxs-lookup"><span data-stu-id="2e632-395">GP path: Administrative Templates/Microsoft Edge Update/Preferences</span></span>
- <span data-ttu-id="2e632-396">Nome do arquivo de ADMX da Política de Grupo: edgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="2e632-396">GP ADMX file name: edgeupdate.admx</span></span>
##### <span data-ttu-id="2e632-397">Configurações de registro do Windows</span><span class="sxs-lookup"><span data-stu-id="2e632-397">Windows Registry Settings</span></span>
- <span data-ttu-id="2e632-398">Caminho: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="2e632-398">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="2e632-399">Nome do valor:</span><span class="sxs-lookup"><span data-stu-id="2e632-399">Value Name:</span></span> 
  - <span data-ttu-id="2e632-400">UpdatesSuppressedDurationMin</span><span class="sxs-lookup"><span data-stu-id="2e632-400">UpdatesSuppressedDurationMin</span></span>
  - <span data-ttu-id="2e632-401">UpdatesSuppressedStartHour</span><span class="sxs-lookup"><span data-stu-id="2e632-401">UpdatesSuppressedStartHour</span></span>
  - <span data-ttu-id="2e632-402">UpdatesSuppressedStartMin</span><span class="sxs-lookup"><span data-stu-id="2e632-402">UpdatesSuppressedStartMin</span></span>
- <span data-ttu-id="2e632-403">Tipo de valor: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="2e632-403">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="2e632-404">Valor de exemplo:</span><span class="sxs-lookup"><span data-stu-id="2e632-404">Example value:</span></span>
```
duration   : 0x0000003c
start hour : 0x00000001
start min  : 0x00000002
```
[<span data-ttu-id="2e632-405">Voltar ao início</span><span class="sxs-lookup"><span data-stu-id="2e632-405">Back to top</span></span>](#microsoft-edge---update-policies)


## <span data-ttu-id="2e632-406">Políticas do servidor proxy</span><span class="sxs-lookup"><span data-stu-id="2e632-406">Proxy Server policies</span></span>
  
  

[<span data-ttu-id="2e632-407">Voltar ao início</span><span class="sxs-lookup"><span data-stu-id="2e632-407">Back to top</span></span>](#microsoft-edge---update-policies)
### <span data-ttu-id="2e632-408">ProxyMode</span><span class="sxs-lookup"><span data-stu-id="2e632-408">ProxyMode</span></span>
#### <span data-ttu-id="2e632-409">Escolher como especificar as configurações do servidor proxy</span><span class="sxs-lookup"><span data-stu-id="2e632-409">Choose how to specify proxy server settings</span></span>
><span data-ttu-id="2e632-410">Microsoft Edge Update 1.3.21.81 e posterior</span><span class="sxs-lookup"><span data-stu-id="2e632-410">Microsoft Edge Update 1.3.21.81 and later</span></span>

#### <span data-ttu-id="2e632-411">Descrição</span><span class="sxs-lookup"><span data-stu-id="2e632-411">Description</span></span>
<span data-ttu-id="2e632-412">Permite especificar as configurações do servidor proxy que serão usadas pelo Microsoft Edge Update.</span><span class="sxs-lookup"><span data-stu-id="2e632-412">Allows you to specify the proxy server settings that are used by Microsoft Edge Update.</span></span>

  <span data-ttu-id="2e632-413">Se você habilitar essa configuração da política, poderá escolher entre as seguintes opções do servidor proxy:</span><span class="sxs-lookup"><span data-stu-id="2e632-413">If you enable this policy, you can choose between the following proxy server options:</span></span>
   - <span data-ttu-id="2e632-414">Se você optar por nunca usar um servidor proxy e sempre se conectar diretamente, todas as outras opções serão ignoradas.</span><span class="sxs-lookup"><span data-stu-id="2e632-414">If you choose to never use a proxy server and always connect directly, all other options are ignored.</span></span>
   - <span data-ttu-id="2e632-415">Se você optar por usar as configurações de proxy do sistema ou detectar automaticamente o servidor proxy, todas as outras opções serão ignoradas.</span><span class="sxs-lookup"><span data-stu-id="2e632-415">If you choose to use system proxy settings or auto-detect the proxy server, all other options are ignored.</span></span>
   - <span data-ttu-id="2e632-416">Se escolher o modo fixo do servidor proxy, você poderá especificar mais opções em '[Endereço ou URL do servidor proxy](#proxyserver)'.</span><span class="sxs-lookup"><span data-stu-id="2e632-416">If you choose fixed server proxy mode, you can specify further options in '[Address or URL of proxy server](#proxyserver)' policy.</span></span>
   - <span data-ttu-id="2e632-417">Se você optar por usar um script de proxy .pac, deve especificar a URL do script em '[De URL para um arquivo .pac de proxy](#proxypacurl)'.</span><span class="sxs-lookup"><span data-stu-id="2e632-417">If you choose to use a .pac proxy script, you must specify the URL for the script in '[URL to a proxy .pac file](#proxypacurl)' policy.</span></span>

  <span data-ttu-id="2e632-418">Se você habilitar essa política, os usuários de sua organização não poderão alterar as configurações de proxy no Microsoft Edge Update.</span><span class="sxs-lookup"><span data-stu-id="2e632-418">If you enable this policy, users in your organization can't change the proxy settings in Microsoft Edge Update.</span></span>

  <span data-ttu-id="2e632-419">Se você desabilitar ou não configurar essa política, nenhuma configuração do servidor proxy será definida, mas os usuários de sua organização poderão escolher suas próprias configurações de proxy para o Microsoft Edge Update.</span><span class="sxs-lookup"><span data-stu-id="2e632-419">If you disable or don't configure this policy, no proxy server settings are configured, but users in your organization can choose their own proxy settings for Microsoft Edge Update.</span></span>
#### <span data-ttu-id="2e632-420">Informações e configurações do Windows</span><span class="sxs-lookup"><span data-stu-id="2e632-420">Windows information and settings</span></span>
##### <span data-ttu-id="2e632-421">Informações da Política de Grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="2e632-421">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="2e632-422">Nome exclusivo da Política de Grupo: ProxyMode</span><span class="sxs-lookup"><span data-stu-id="2e632-422">GP unique name: ProxyMode</span></span>
- <span data-ttu-id="2e632-423">Nome da Política de Grupo: Escolher como especificar as configurações do servidor proxy</span><span class="sxs-lookup"><span data-stu-id="2e632-423">GP name: Choose how to specify proxy server settings</span></span>
- <span data-ttu-id="2e632-424">Caminho da Política de Grupo: Modelos Administrativos/Microsoft Edge Update/Servidor Proxy</span><span class="sxs-lookup"><span data-stu-id="2e632-424">GP path: Administrative Templates/Microsoft Edge Update/Proxy Server</span></span>
- <span data-ttu-id="2e632-425">Nome do arquivo de ADMX da Política de Grupo: edgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="2e632-425">GP ADMX file name: edgeupdate.admx</span></span>
##### <span data-ttu-id="2e632-426">Configurações de registro do Windows</span><span class="sxs-lookup"><span data-stu-id="2e632-426">Windows Registry Settings</span></span>
- <span data-ttu-id="2e632-427">Caminho: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="2e632-427">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="2e632-428">Nome do valor: ProxyMode</span><span class="sxs-lookup"><span data-stu-id="2e632-428">Value Name: ProxyMode</span></span>
- <span data-ttu-id="2e632-429">Tipo do valor: REG_SZ</span><span class="sxs-lookup"><span data-stu-id="2e632-429">Value Type: REG_SZ</span></span>
##### <span data-ttu-id="2e632-430">Valor de exemplo:</span><span class="sxs-lookup"><span data-stu-id="2e632-430">Example value:</span></span>
```
fixed_servers
```
[<span data-ttu-id="2e632-431">Voltar ao início</span><span class="sxs-lookup"><span data-stu-id="2e632-431">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="2e632-432">ProxyPacUrl</span><span class="sxs-lookup"><span data-stu-id="2e632-432">ProxyPacUrl</span></span>
#### <span data-ttu-id="2e632-433">A URL para um arquivo .pac de proxy</span><span class="sxs-lookup"><span data-stu-id="2e632-433">URL to a proxy .pac file</span></span>
><span data-ttu-id="2e632-434">Microsoft Edge Update 1.3.21.81 e posterior</span><span class="sxs-lookup"><span data-stu-id="2e632-434">Microsoft Edge Update 1.3.21.81 and later</span></span>

#### <span data-ttu-id="2e632-435">Descrição</span><span class="sxs-lookup"><span data-stu-id="2e632-435">Description</span></span>
<span data-ttu-id="2e632-436">Permite especificar uma URL para um arquivo (PAC) de configuração automática de proxy.</span><span class="sxs-lookup"><span data-stu-id="2e632-436">Allows you to specify a URL for a proxy auto-config (PAC) file.</span></span>

  <span data-ttu-id="2e632-437">Se habilitar essa política, você poderá especificar uma URL de um arquivo PAC para automatizar a maneira como o Microsoft Edge Update seleciona para a busca de um site específico.</span><span class="sxs-lookup"><span data-stu-id="2e632-437">If you enable this policy, you can specify a URL for a PAC file to automate how Microsoft Edge Update selects the appropriate proxy server for fetching a particular website.</span></span>

  <span data-ttu-id="2e632-438">Essa política será aplicada somente se você especificou as configurações de proxy manuais na política '[Escolher como especificar configurações do servidor proxy](#proxymode)'.</span><span class="sxs-lookup"><span data-stu-id="2e632-438">This policy is applied only if you have specified manual proxy settings in the '[Choose how to specify proxy server settings](#proxymode)' policy.</span></span>

  <span data-ttu-id="2e632-439">Não configure essa política se você selecionou uma configuração de proxy que não seja manual na política '[Escolher como especificar as configurações do servidor proxy](#proxymode)'.</span><span class="sxs-lookup"><span data-stu-id="2e632-439">Don't configure this policy if you have selected a proxy setting other than manual in the '[Choose how to specify proxy server settings](#proxymode)' policy.</span></span>
#### <span data-ttu-id="2e632-440">Informações e configurações do Windows</span><span class="sxs-lookup"><span data-stu-id="2e632-440">Windows information and settings</span></span>
##### <span data-ttu-id="2e632-441">Informações da Política de Grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="2e632-441">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="2e632-442">Nome exclusivo da Política de Grupo: ProxyPacUrl</span><span class="sxs-lookup"><span data-stu-id="2e632-442">GP unique name: ProxyPacUrl</span></span>
- <span data-ttu-id="2e632-443">Nome da Política de Grupo: A URL para um arquivo .pac de proxy</span><span class="sxs-lookup"><span data-stu-id="2e632-443">GP name: URL to a proxy .pac file</span></span>
- <span data-ttu-id="2e632-444">Caminho da Política de Grupo: Modelos Administrativos/Microsoft Edge Update/Servidor Proxy</span><span class="sxs-lookup"><span data-stu-id="2e632-444">GP path: Administrative Templates/Microsoft Edge Update/Proxy Server</span></span>
- <span data-ttu-id="2e632-445">Nome do arquivo de ADMX da Política de Grupo: edgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="2e632-445">GP ADMX file name: edgeupdate.admx</span></span>
##### <span data-ttu-id="2e632-446">Configurações de registro do Windows</span><span class="sxs-lookup"><span data-stu-id="2e632-446">Windows Registry Settings</span></span>
- <span data-ttu-id="2e632-447">Caminho: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="2e632-447">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="2e632-448">Nome do valor: ProxyPacUrl</span><span class="sxs-lookup"><span data-stu-id="2e632-448">Value Name: ProxyPacUrl</span></span>
- <span data-ttu-id="2e632-449">Tipo do valor: REG_SZ</span><span class="sxs-lookup"><span data-stu-id="2e632-449">Value Type: REG_SZ</span></span>
##### <span data-ttu-id="2e632-450">Valor de exemplo:</span><span class="sxs-lookup"><span data-stu-id="2e632-450">Example value:</span></span>
```
https://www.microsoft.com
```
[<span data-ttu-id="2e632-451">Voltar ao início</span><span class="sxs-lookup"><span data-stu-id="2e632-451">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="2e632-452">ProxyServer</span><span class="sxs-lookup"><span data-stu-id="2e632-452">ProxyServer</span></span>
#### <span data-ttu-id="2e632-453">Endereço ou URL do servidor proxy</span><span class="sxs-lookup"><span data-stu-id="2e632-453">Address or URL of proxy server</span></span>
><span data-ttu-id="2e632-454">Microsoft Edge Update 1.3.21.81 e posterior</span><span class="sxs-lookup"><span data-stu-id="2e632-454">Microsoft Edge Update 1.3.21.81 and later</span></span>

#### <span data-ttu-id="2e632-455">Description</span><span class="sxs-lookup"><span data-stu-id="2e632-455">Description</span></span>
<span data-ttu-id="2e632-456">Permite especificar a URL do servidor proxy para o Microsoft Edge Update usar.</span><span class="sxs-lookup"><span data-stu-id="2e632-456">Allows you to specify the URL of the proxy server for Microsoft Edge Update to use.</span></span>

  <span data-ttu-id="2e632-457">Se você habilitar essa política, poderá configurar a URL do servidor proxy usada pelo Microsoft Edge Update em sua organização.</span><span class="sxs-lookup"><span data-stu-id="2e632-457">If you enable this policy, you can set the proxy server URL used by Microsoft Edge Update in your organization.</span></span>

  <span data-ttu-id="2e632-458">Essa política será aplicada somente se você selecionou as configurações de proxy manuais na política '[Escolher como especificar as configurações do servidor proxy](#proxymode)'.</span><span class="sxs-lookup"><span data-stu-id="2e632-458">This policy is applied only if you have selected manual proxy settings in the '[Choose how to specify proxy server settings](#proxymode)' policy.</span></span>

  <span data-ttu-id="2e632-459">Não configure essa política se você selecionou uma configuração de proxy que não seja manual na política '[Escolher como especificar as configurações do servidor proxy](#proxymode)'.</span><span class="sxs-lookup"><span data-stu-id="2e632-459">Don't configure this policy if you have selected a proxy setting other than manual in the '[Choose how to specify proxy server settings](#proxymode)' policy.</span></span>
#### <span data-ttu-id="2e632-460">Informações e configurações do Windows</span><span class="sxs-lookup"><span data-stu-id="2e632-460">Windows information and settings</span></span>
##### <span data-ttu-id="2e632-461">Informações da Política de Grupo (ADMX)</span><span class="sxs-lookup"><span data-stu-id="2e632-461">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="2e632-462">Nome exclusivo da Política de Grupo: ProxyServer</span><span class="sxs-lookup"><span data-stu-id="2e632-462">GP unique name: ProxyServer</span></span>
- <span data-ttu-id="2e632-463">Nome da Política de Grupo: O endereço ou a URL do servidor proxy</span><span class="sxs-lookup"><span data-stu-id="2e632-463">GP name: Address or URL of proxy server</span></span>
- <span data-ttu-id="2e632-464">Caminho da Política de Grupo: Modelos Administrativos/Microsoft Edge Update/Servidor Proxy</span><span class="sxs-lookup"><span data-stu-id="2e632-464">GP path: Administrative Templates/Microsoft Edge Update/Proxy Server</span></span>
- <span data-ttu-id="2e632-465">Nome do arquivo de ADMX da Política de Grupo: edgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="2e632-465">GP ADMX file name: edgeupdate.admx</span></span>
##### <span data-ttu-id="2e632-466">Configurações de registro do Windows</span><span class="sxs-lookup"><span data-stu-id="2e632-466">Windows Registry Settings</span></span>
- <span data-ttu-id="2e632-467">Caminho: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="2e632-467">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="2e632-468">Nome do valor: ProxyServer</span><span class="sxs-lookup"><span data-stu-id="2e632-468">Value Name: ProxyServer</span></span>
- <span data-ttu-id="2e632-469">Tipo do valor: REG_SZ</span><span class="sxs-lookup"><span data-stu-id="2e632-469">Value Type: REG_SZ</span></span>
##### <span data-ttu-id="2e632-470">Valor de exemplo:</span><span class="sxs-lookup"><span data-stu-id="2e632-470">Example value:</span></span>
```
https://www.microsoft.com
```
[<span data-ttu-id="2e632-471">Voltar ao início</span><span class="sxs-lookup"><span data-stu-id="2e632-471">Back to top</span></span>](#microsoft-edge---update-policies)


## <span data-ttu-id="2e632-472">Consulte também</span><span class="sxs-lookup"><span data-stu-id="2e632-472">See also</span></span>
  - [<span data-ttu-id="2e632-473">Configurar o Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="2e632-473">Configuring Microsoft Edge</span></span>](configure-microsoft-edge.md)
  - [<span data-ttu-id="2e632-474">Página de aterrissagem do Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="2e632-474">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
