---
title: Usar políticas de grupo para gerenciar extensões do Microsoft Edge
ms.author: aspoddar
author: AndreaLBarr
manager: balajek
ms.date: 06/09/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Usar políticas de grupo para gerenciar extensões do Microsoft Edge na empresa
ms.openlocfilehash: a633b036c1733716dfb257b4711bca57bd6721f0
ms.sourcegitcommit: 4192328ee585bc32a9be528766b8a5a98e046c8e
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/25/2021
ms.locfileid: "11618015"
---
# <a name="use-group-policies-to-manage-microsoft-edge-extensions"></a><span data-ttu-id="09dbd-103">Usar políticas de grupo para gerenciar extensões do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="09dbd-103">Use group policies to manage Microsoft Edge extensions</span></span>

<span data-ttu-id="09dbd-104">Este artigo descreve as opções e as etapas para gerenciar extensões usando políticas de grupo.</span><span class="sxs-lookup"><span data-stu-id="09dbd-104">This article describes the options and steps for managing extensions by using group policies.</span></span> <span data-ttu-id="09dbd-105">As opções de extensão pressupõem que você já tem o Microsoft Edge gerenciado para os usuários.</span><span class="sxs-lookup"><span data-stu-id="09dbd-105">These options  assume that you already have Microsoft Edge managed for your users.</span></span> <span data-ttu-id="09dbd-106">Se você ainda não configurou Microsoft Edge para ser gerenciado para seus usuários, siga o link abaixo para fazer isso agora.</span><span class="sxs-lookup"><span data-stu-id="09dbd-106">If you have not already set up Microsoft Edge to be managed for your users please follow the below link to do so now.</span></span>

- [<span data-ttu-id="09dbd-107">Gerenciar extensões do Microsoft Edge na empresa</span><span class="sxs-lookup"><span data-stu-id="09dbd-107">Manage Microsoft Edge extensions in the enterprise</span></span>](/deployedge/microsoft-edge-manage-extensions)

> [!NOTE]
> <span data-ttu-id="09dbd-108">Este artigo se aplica ao Microsoft Edge versão 77 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="09dbd-108">This article applies to Microsoft Edge version 77 or later.</span></span>

## <a name="block-extensions-based-on-their-permissions"></a><span data-ttu-id="09dbd-109">Bloquear extensões com base em suas permissões</span><span class="sxs-lookup"><span data-stu-id="09dbd-109">Block extensions based on their permissions</span></span>

<span data-ttu-id="09dbd-110">Você pode controlar quais extensões os usuários podem instalar com base nas permissões usando a política [ExtensionSettings](/deployedge/microsoft-edge-policies#extensionsettings).</span><span class="sxs-lookup"><span data-stu-id="09dbd-110">You can control what extensions your users can install based on permissions using the [ExtensionSettings](/deployedge/microsoft-edge-policies#extensionsettings) policy.</span></span> <span data-ttu-id="09dbd-111">Se uma extensão instalada precisar de uma permissão bloqueada, ela simplesmente não será executada.</span><span class="sxs-lookup"><span data-stu-id="09dbd-111">If an installed extension needs a permission that’s blocked, it just won't run.</span></span> <span data-ttu-id="09dbd-112">A extensão não é removida, apenas desabilitada.</span><span class="sxs-lookup"><span data-stu-id="09dbd-112">The extension isn't removed, just disabled.</span></span>

> [!NOTE]
> <span data-ttu-id="09dbd-113">A configuração de permissões bloqueadas só pode ser definida dentro da política de configurações de extensão.</span><span class="sxs-lookup"><span data-stu-id="09dbd-113">The blocked permissions setting can only be set within the extension settings policy.</span></span>  

<span data-ttu-id="09dbd-114">Use as etapas a seguir como um guia para bloquear uma extensão.</span><span class="sxs-lookup"><span data-stu-id="09dbd-114">Use the following steps as a guide for blocking an extension.</span></span>

1. <span data-ttu-id="09dbd-115">Abra o editor de gerenciamento de política de grupo, vá para **Modelos Administrativos > Microsoft Edge > Extensões**  e selecione **Definir configurações de gerenciamento de extensão**.</span><span class="sxs-lookup"><span data-stu-id="09dbd-115">Open the group policy management editor and go to **Administrative Templates > Microsoft Edge > Extensions**  and then select **Configure extension management settings**.</span></span>
2. <span data-ttu-id="09dbd-116">Habilite a política e insira as permissões que você deseja que sejam permitidas ou bloqueadas usando uma cadeia de caracteres JSON que é compactada.</span><span class="sxs-lookup"><span data-stu-id="09dbd-116">Enable the policy, then enter the permissions that you want allowed or blocked, by using a JSON string that gets compressed.</span></span> <span data-ttu-id="09dbd-117">A próxima captura de tela mostra como bloquear uma extensão que usa a permissão "usb".</span><span class="sxs-lookup"><span data-stu-id="09dbd-117">The next screenshot shows how to block an extension that uses the permission "usb".</span></span>

    :::image type="content" source="media/microsoft-edge-manage-extensions-policies/manage-extensions-gp-block-1.png" alt-text="Configurar a política de grupo para bloquear uma extensão.":::

<span data-ttu-id="09dbd-119">O exemplo a seguir mostra o JSON para bloquear qualquer extensão que precise do uso da permissão "usb" e sua cadeia de caracteres compactada.</span><span class="sxs-lookup"><span data-stu-id="09dbd-119">The following example shows the JSON to block any extension that needs the use of permission "usb" and its compressed string.</span></span>

### <a name="json-example"></a><span data-ttu-id="09dbd-120">Exemplo de JSON:</span><span class="sxs-lookup"><span data-stu-id="09dbd-120">JSON example</span></span>

   ```json
   { 
        "*": { 
             "blocked_permissions": ["usb"] 
        } 
   } 
   ```

   ```json
   {"*":{"blocked_permissions":["usb"]}} 
   ```

   > [!NOTE]
   > <span data-ttu-id="09dbd-121">Para bloquear todas as extensões que usam a permissão, use um asterisco para a ID de extensão, conforme mostrado no exemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="09dbd-121">To block all extensions that use the permission, use an asterisk for the extension ID, as shown in the previous example.</span></span> <span data-ttu-id="09dbd-122">Se você especificar uma ID de extensão, a política se aplicará somente a essa extensão.</span><span class="sxs-lookup"><span data-stu-id="09dbd-122">If you specify one extension ID, the policy will only apply to that extension.</span></span> <span data-ttu-id="09dbd-123">Você pode bloquear mais de uma, mas elas precisam ser entradas separadas.</span><span class="sxs-lookup"><span data-stu-id="09dbd-123">You can block more than one, but they need to be separate entries.</span></span>

## <a name="prevent-extensions-from-altering-web-pages"></a><span data-ttu-id="09dbd-124">Impedir que extensões alterem páginas da Web</span><span class="sxs-lookup"><span data-stu-id="09dbd-124">Prevent extensions from altering web pages</span></span>

<span data-ttu-id="09dbd-125">Essa configuração impede que as extensões leiam e alterem dados de sites e domínios confidenciais.</span><span class="sxs-lookup"><span data-stu-id="09dbd-125">This setting prevents extensions from reading and changing  data from sensitive websites and domains.</span></span> <span data-ttu-id="09dbd-126">O bloqueio de ações indesejadas é feito bloqueando ações como injeção de script em seus sites, leitura dos cookies ou modificações de solicitação da Web.</span><span class="sxs-lookup"><span data-stu-id="09dbd-126">Blocking unwanted actions is done by blocking actions such as script injection into your websites, reading the cookies, or making web-request modifications.</span></span> <span data-ttu-id="09dbd-127">Essa configuração não impede que os usuários instalem ou removam extensões, ela só impede que as extensões alterem os sites especificados.</span><span class="sxs-lookup"><span data-stu-id="09dbd-127">This setting doesn’t prevent your users from installing or removing extensions, it only prevents extensions from altering the specified websites.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="09dbd-128">A configuração de hosts permitido ou /bloqueados de Runtime só pode ser definida dentro da política de configurações de extensão.</span><span class="sxs-lookup"><span data-stu-id="09dbd-128">The Runtime allowed/blocked hosts setting can only be set within the extension settings policy.</span></span>  

<span data-ttu-id="09dbd-129">Você pode definir as seguintes configurações na política ExtensionSettings para evitar (ou permitir) alterações de sites ou domínios:</span><span class="sxs-lookup"><span data-stu-id="09dbd-129">You can configure the following settings in the ExtensionSettings policy to prevent (or allow) alterations of websites or domains:</span></span>

- <span data-ttu-id="09dbd-130">**Runtime_blocked_hosts**.</span><span class="sxs-lookup"><span data-stu-id="09dbd-130">**Runtime_blocked_hosts**.</span></span> <span data-ttu-id="09dbd-131">Essa configuração impede que as extensões façam alterações ou leia dados dos sites que você especificar.</span><span class="sxs-lookup"><span data-stu-id="09dbd-131">This setting blocks extensions from making changes or reading data from the websites you specify.</span></span>
- <span data-ttu-id="09dbd-132">**Runtime_allowed_hosts**.</span><span class="sxs-lookup"><span data-stu-id="09dbd-132">**Runtime_allowed_hosts**.</span></span> <span data-ttu-id="09dbd-133">Essa configuração permite que as extensões façam alterações ou leiam dados dos sites que você especificar.</span><span class="sxs-lookup"><span data-stu-id="09dbd-133">This setting allows extensions to make changes or read data from the websites you specify.</span></span> <span data-ttu-id="09dbd-134">O seguinte formato é usado para especificar seus sites na cadeia de caracteres JSON na política:</span><span class="sxs-lookup"><span data-stu-id="09dbd-134">The following format is used for specifying your site(s) in the JSON string in the policy:</span></span>

  ```json
  [http|https|ftp|*]://[subdomain|*].[hostname|*].[eTLD|*] [http|https|ftp|*],
  ```

  > [!NOTE]
  > `[hostname|*], and [eTLD|*]` <span data-ttu-id="09dbd-135">as seções são necessárias, mas a seção `[subdomain|*]` é opcional.</span><span class="sxs-lookup"><span data-stu-id="09dbd-135">sections are required, but `[subdomain|*]` section is optional.</span></span>

<span data-ttu-id="09dbd-136">A tabela a seguir mostra exemplos de padrões de host válidos e padrões correspondentes.</span><span class="sxs-lookup"><span data-stu-id="09dbd-136">The following table shows examples of valid host patterns and matching patterns.</span></span>

|<span data-ttu-id="09dbd-137">Padrões de host válidos</span><span class="sxs-lookup"><span data-stu-id="09dbd-137">Valid host patterns</span></span>|<span data-ttu-id="09dbd-138">Correspondências</span><span class="sxs-lookup"><span data-stu-id="09dbd-138">Matches</span></span>|<span data-ttu-id="09dbd-139">Não corresponde</span><span class="sxs-lookup"><span data-stu-id="09dbd-139">Doesn't match</span></span>|
|--|--|--|
|  `*://*.example.*` | `http://example.com`<br>`https://test.example.co.uk`   | `https://example.microsoft.com`<br>`http://example.microsoft.co.uk`  |
| `http://example.*` | `http://example.com`<br>`http://example.ly` | `https://example.com`<br>`http://test.example.com`   |
| `http://example.com`   | `http://example.com` | `https://example.com`<br>`http://test.example.co.uk` |
| `*://*`   | <span data-ttu-id="09dbd-140">Todas as URLs</span><span class="sxs-lookup"><span data-stu-id="09dbd-140">All URLs</span></span>  |   |

<span data-ttu-id="09dbd-141">Use as etapas a seguir como um guia para bloquear ou permitir que extensões acessem um site ou domínio.</span><span class="sxs-lookup"><span data-stu-id="09dbd-141">Use the following steps as a guide to block or allow extensions to access a website or domain.</span></span>

1. <span data-ttu-id="09dbd-142">Abra o editor de gerenciamento de política de grupo, vá para **Modelos Administrativos > Microsoft Edge > Extensões**e selecione **Definir configurações de gerenciamento de extensão**.</span><span class="sxs-lookup"><span data-stu-id="09dbd-142">Open the group policy management editor and go to **Administrative Templates > Microsoft Edge > Extensions**, and then select **Configure extension management settings**.</span></span>  
2. <span data-ttu-id="09dbd-143">Habilite a política e insira as permissões que você deseja permitir ou bloquear, compactando as permissões para uma única cadeia de caracteres JSON.</span><span class="sxs-lookup"><span data-stu-id="09dbd-143">Enable the policy, then enter the permissions that you want allowed or blocked, compressing the permissions to a single JSON string.</span></span>

<span data-ttu-id="09dbd-144">Os exemplos a seguir mostram como bloquear extensões em um nome de host e como bloquear extensões no mesmo domínio.</span><span class="sxs-lookup"><span data-stu-id="09dbd-144">The following examples show how to block extensions on a hostname and how to block extensions on the same domain.</span></span>

### <a name="json-example-to-block-hostname"></a><span data-ttu-id="09dbd-145">Exemplo de JSON para bloquear o nome do host</span><span class="sxs-lookup"><span data-stu-id="09dbd-145">JSON example to block hostname</span></span>

<span data-ttu-id="09dbd-146">Este exemplo mostra o JSON e a cadeia de caracteres JSON compactada para impedir que qualquer extensão acesse o nome de host `www.microsoft.com`.</span><span class="sxs-lookup"><span data-stu-id="09dbd-146">This example shows the JSON and compressed JSON string to block any extension from accessing the `www.microsoft.com` hostname.</span></span>

```json
{ 
    "*":{ 
            "runtime_blocked_hosts":["www.microsoft.com"] 
    } 
} 
```

```json
{"*":{"runtime_blocked_hosts":["www.microsoft.com"]}} 
```

> [!NOTE]
> <span data-ttu-id="09dbd-147">Para impedir que todas as extensões acessem uma página da Web, use um asterisco para a ID de extensão, conforme mostrado no exemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="09dbd-147">To block all extensions from accessing a webpage, use an asterisk for the extension ID, as shown in the previous example.</span></span>  <span data-ttu-id="09dbd-148">Se você especificar uma ID de extensão em vez de um asterisco, a política só se aplicará a essa extensão.</span><span class="sxs-lookup"><span data-stu-id="09dbd-148">If you specify one extension ID instead of an asterisk, the policy will only apply to that extension.</span></span> <span data-ttu-id="09dbd-149">Você pode bloquear mais de uma extensão, mas elas precisam ser entradas separadas.</span><span class="sxs-lookup"><span data-stu-id="09dbd-149">You can block more than one extension, but they need to be separate entries.</span></span>

### <a name="json-example-to-block-extensions-on-same-domain"></a><span data-ttu-id="09dbd-150">Exemplo de JSON para bloquear extensões no mesmo domínio</span><span class="sxs-lookup"><span data-stu-id="09dbd-150">JSON example to block extensions on same domain</span></span>

<span data-ttu-id="09dbd-151">Este exemplo mostra o JSON e a cadeia de caracteres JSON compactada para bloquear a execução de extensões específicas no mesmo domínio, "importantwebsite".</span><span class="sxs-lookup"><span data-stu-id="09dbd-151">This example shows the JSON and compressed JSON string to block specific extensions from running on the same domain, "importantwebsite".</span></span>

```json
{ 
    "aapbdbdomjkkjkaonfhkkikfgjllcleb": { 
        "runtime_blocked_hosts": ["*://*.importantwebsite"] 
    }, 
    "bfbmjmiodbnnpllbbbfblcplfjjepjdn": { 
        "runtime_blocked_hosts": ["*://*.importantwebsite"] 
    } 
} 
```

```json
{"aapbdbdomjkkjkaonfhkkikfgjllcleb": {"runtime_blocked_hosts": ["*://,*.importantwebsite"]},"bfbmjmiodbnnpllbbbfblcplfjjepjdn": {"runtime_blocked_hosts": ["*://*.importantwebsite"]}} 
```

## <a name="allow-or-block-extensions-in-group-policy"></a><span data-ttu-id="09dbd-152">Permitir ou bloquear extensões na política de grupo</span><span class="sxs-lookup"><span data-stu-id="09dbd-152">Allow or block extensions in group policy</span></span>

<span data-ttu-id="09dbd-153">Você pode usar as políticas [ExtensionInstallBlocklist](/DeployEdge/microsoft-edge-policies#extensioninstallblocklist) e [ExtensionInstallAllowlist](/DeployEdge/microsoft-edge-policies#extensioninstallallowlist) para controlar quais extensões são bloqueadas ou permitidas.</span><span class="sxs-lookup"><span data-stu-id="09dbd-153">You can use the [ExtensionInstallBlocklist](/DeployEdge/microsoft-edge-policies#extensioninstallblocklist) and [ExtensionInstallAllowlist](/DeployEdge/microsoft-edge-policies#extensioninstallallowlist) policies to control which extensions are blocked or allowed.</span></span> <span data-ttu-id="09dbd-154">Use as etapas a seguir como um guia para permitir todas as extensões, exceto aquelas que você deseja bloquear.</span><span class="sxs-lookup"><span data-stu-id="09dbd-154">Use the following steps as a guide to allow all extensions except those you want to block.</span></span>

1. <span data-ttu-id="09dbd-155">Abra o editor de gerenciamento de política de grupo, vá para **Modelos Administrativos > Microsoft Edge > Extensões >** e selecione **Controlar quais extensões não podem ser instaladas**.</span><span class="sxs-lookup"><span data-stu-id="09dbd-155">Open the group policy management editor and go to **Administrative Templates > Microsoft Edge > Extensions >** and then select **Control which extensions cannot be installed**.</span></span>
2. <span data-ttu-id="09dbd-156">Selecione **Habilitado**.</span><span class="sxs-lookup"><span data-stu-id="09dbd-156">Select **Enabled**.</span></span>
3. <span data-ttu-id="09dbd-157">Clique em **Mostrar**.</span><span class="sxs-lookup"><span data-stu-id="09dbd-157">Click **Show**.</span></span>
4. <span data-ttu-id="09dbd-158">Insira a ID do aplicativo das extensões que você deseja bloquear.</span><span class="sxs-lookup"><span data-stu-id="09dbd-158">Enter the app ID of the extensions that you want to block.</span></span> <span data-ttu-id="09dbd-159">Ao adicionar várias IDs de aplicativo, use uma linha separada para cada ID.</span><span class="sxs-lookup"><span data-stu-id="09dbd-159">When adding multiple app ID’s use a separate row for each ID.</span></span>
5. <span data-ttu-id="09dbd-160">Para bloquear todas as extensões, digite **\*** na política para impedir que as extensões sejam instaladas.</span><span class="sxs-lookup"><span data-stu-id="09dbd-160">To block all extensions, type **\*** into the policy to prevent any extensions from being installed.</span></span> <span data-ttu-id="09dbd-161">Você pode usar isso em conjunto com a política "Permitir que extensões específicas sejam instaladas" para permitir que apenas determinadas extensões sejam instaladas.</span><span class="sxs-lookup"><span data-stu-id="09dbd-161">You can use this in conjunction with the "Allow specific extensions to be installed" policy to only allow certain extensions to be installed.</span></span> <span data-ttu-id="09dbd-162">A próxima captura de tela mostra uma extensão que será bloqueada com base na ID do aplicativo fornecida.</span><span class="sxs-lookup"><span data-stu-id="09dbd-162">The next screenshot shows an extension that will be blocked based on the app ID that's provided.</span></span>

   :::image type="content" source="media/microsoft-edge-manage-extensions-policies/manage-extensions-gp-block-2.png" alt-text="Use a ID do aplicativo para bloquear uma extensão.":::

   > [!TIP]
   > <span data-ttu-id="09dbd-164">Se você não encontrar a ID do aplicativo de uma extensão, examine a extensão Site de complementos do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="09dbd-164">If you can’t find the app ID of an extension, look at the extension in the Microsoft Edge Add-ons website.</span></span> <span data-ttu-id="09dbd-165">Localize a extensão específica e você verá a ID do aplicativo no final da URL na omnibox.</span><span class="sxs-lookup"><span data-stu-id="09dbd-165">Find the specific extension and you will see the app ID at the end of the URL in the omnibox.</span></span>

> [!NOTE]
> <span data-ttu-id="09dbd-166">Você pode adicionar uma extensão à lista de bloqueios que já está instalada no computador de um usuário.</span><span class="sxs-lookup"><span data-stu-id="09dbd-166">You can add an extension to the blocklist that’s already installed on a user’s computer.</span></span> <span data-ttu-id="09dbd-167">Isso desabilitará a extensão e impedirá que o usuário a habilite novamente.</span><span class="sxs-lookup"><span data-stu-id="09dbd-167">This will disable the extension and prevent the user from re-enabling it.</span></span> <span data-ttu-id="09dbd-168">Ele não será desinstalado, apenas desabilitado.</span><span class="sxs-lookup"><span data-stu-id="09dbd-168">It won't be uninstalled, just disabled.</span></span>

## <a name="force-install-an-extension"></a><span data-ttu-id="09dbd-169">Forçar a instalação de uma extensão</span><span class="sxs-lookup"><span data-stu-id="09dbd-169">Force-install an extension</span></span>

<span data-ttu-id="09dbd-170">Use a política [ExtensionInstallForcelist](/DeployEdge/microsoft-edge-policies#extensioninstallforcelist) para controlar quais extensões são bloqueadas ou permitidas.</span><span class="sxs-lookup"><span data-stu-id="09dbd-170">Use the [ExtensionInstallForcelist](/DeployEdge/microsoft-edge-policies#extensioninstallforcelist) policy to control which extensions are blocked or allowed.</span></span> <span data-ttu-id="09dbd-171">Use as etapas a seguir como um guia para forçar a instalação de uma extensão.</span><span class="sxs-lookup"><span data-stu-id="09dbd-171">Use the following steps as a guide to force-install an extension.</span></span>

1. <span data-ttu-id="09dbd-172">No Editor Política de Grupo, acesse **Modelos Administrativos> Microsoft Edge > Extensões >** e selecione **Controlar quais extensões são instaladas silenciosamente**.</span><span class="sxs-lookup"><span data-stu-id="09dbd-172">In the Group Policy Editor, go to **Administrative Templates> Microsoft Edge >  Extensions >** and then select **Control which extensions are installed silently**.</span></span>
2. <span data-ttu-id="09dbd-173">Selecione **Habilitado**.</span><span class="sxs-lookup"><span data-stu-id="09dbd-173">Select **Enabled**.</span></span>  
3. <span data-ttu-id="09dbd-174">Clique em **Mostrar**.</span><span class="sxs-lookup"><span data-stu-id="09dbd-174">Click **Show**.</span></span>
4. <span data-ttu-id="09dbd-175">Insira a ID do aplicativo ou as IDs da extensão ou das extensões que você deseja forçar a instalação.</span><span class="sxs-lookup"><span data-stu-id="09dbd-175">Enter the app ID or IDs of the extension or extensions you want to force-install.</span></span>  

<span data-ttu-id="09dbd-176">A extensão será instalada silenciosamente sem a necessidade de interação do usuário.</span><span class="sxs-lookup"><span data-stu-id="09dbd-176">The extension will be installed silently with no need for user interaction.</span></span> <span data-ttu-id="09dbd-177">O usuário também não poderá desinstalar ou desabilitar a extensão.</span><span class="sxs-lookup"><span data-stu-id="09dbd-177">The user also won’t be able to uninstall or disable the extension.</span></span> <span data-ttu-id="09dbd-178">Essa configuração substituirá qualquer política de lista de bloqueio habilitada.</span><span class="sxs-lookup"><span data-stu-id="09dbd-178">This setting will overwrite over any blocklist policy that’s enabled.</span></span>

> [!NOTE]
> <span data-ttu-id="09dbd-179">Para extensões hospedadas na Loja Da Web do Chrome, use uma cadeia de caracteres como: `pckdojakecnhhplcgfflhndiffaohfah;https://clients2.google.com/service/update2/crx`.</span><span class="sxs-lookup"><span data-stu-id="09dbd-179">For extensions hosted in the Chrome web store use a string such as: `pckdojakecnhhplcgfflhndiffaohfah;https://clients2.google.com/service/update2/crx`.</span></span>

## <a name="block-extensions-from-a-specific-store-or-update-url"></a><span data-ttu-id="09dbd-180">Bloquear extensões de um repositório ou URL de atualização específico</span><span class="sxs-lookup"><span data-stu-id="09dbd-180">Block extensions from a specific store or update URL</span></span>

<span data-ttu-id="09dbd-181">Para bloquear extensões de um repositório ou URL específico, você só precisa bloquear o *update_url* para esse repositório usando a política [ExtensionSettings](/deployedge/microsoft-edge-policies#extensionsettings).</span><span class="sxs-lookup"><span data-stu-id="09dbd-181">To block extensions from a particular store or URL, you only need to block the *update_url* for that store using the [ExtensionSettings](/deployedge/microsoft-edge-policies#extensionsettings) policy.</span></span>

<span data-ttu-id="09dbd-182">Use as etapas a seguir como um guia para bloquear extensões de um repositório ou URL específico.</span><span class="sxs-lookup"><span data-stu-id="09dbd-182">Use the following steps as a guide to block extensions from an particular store or URL.</span></span>

1. <span data-ttu-id="09dbd-183">Abra o editor de gerenciamento de política de grupo, vá para **Modelos Administrativos > Microsoft Edge > Extensões >** e selecione **Definir configurações de gerenciamento de extensão**.</span><span class="sxs-lookup"><span data-stu-id="09dbd-183">Open the group policy management editor and go to **Administrative Templates > Microsoft Edge > Extensions >** and then select **Configure extension management settings**.</span></span>  
2. <span data-ttu-id="09dbd-184">Habilite a política e insira as permissões que você deseja permitir ou bloquear, compactando-a em uma única cadeia de caracteres JSON.</span><span class="sxs-lookup"><span data-stu-id="09dbd-184">Enable the policy, then enter the permissions that you want allowed or blocked, compressing it to a single JSON string.</span></span>

<span data-ttu-id="09dbd-185">O exemplo a seguir mostra o JSON e a cadeia de caracteres JSON compactada a serem bloqueados do Chrome Web Store usando sua URL de atualização (`https://clients2.google.com/service/update2/crx`).</span><span class="sxs-lookup"><span data-stu-id="09dbd-185">The next example shows the JSON and compressed JSON string to block from the Chrome Web Store using its update URL (`https://clients2.google.com/service/update2/crx`).</span></span>

### <a name="json-example-for-blocking-on-update-url"></a><span data-ttu-id="09dbd-186">Exemplo de JSON para bloqueio na URL de atualização</span><span class="sxs-lookup"><span data-stu-id="09dbd-186">JSON example for blocking on update URL</span></span>

```json
{ 
"update_url:https://clients2.google.com/service/update2/crx":{ 
                                                             " installation_mode":"blocked" 
                                                             } 
} 
```

```json
{"update_url:https://clients2.google.com/service/update2/crx":{"installation_mode":"blocked"}} 
```

> [!NOTE]
> <span data-ttu-id="09dbd-187">Observe que você ainda pode usar **ExtensionInstallForcelist** e **ExtensionInstallAllowlist** para permitir ou forçar a instalação de extensões específicas, mesmo se o armazenamento estiver bloqueado usando o JSON no exemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="09dbd-187">You can still use **ExtensionInstallForceList** and **ExtensionInstallAllowList** to allow/force install specific extensions even if the store is blocked using the JSON in the previous example.</span></span>

## <a name="see-also"></a><span data-ttu-id="09dbd-188">Veja também</span><span class="sxs-lookup"><span data-stu-id="09dbd-188">See also</span></span>

- [<span data-ttu-id="09dbd-189">Gerenciar extensões do Microsoft Edge na empresa</span><span class="sxs-lookup"><span data-stu-id="09dbd-189">Manage Microsoft Edge extensions in the enterprise</span></span>](microsoft-edge-manage-extensions.md)
- [<span data-ttu-id="09dbd-190">Criar um repositório para hospedar extensões do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="09dbd-190">Create a web store to host Microsoft Edge extensions</span></span>](microsoft-edge-manage-extensions-webstore.md)
- [<span data-ttu-id="09dbd-191">Guia de referência para a política ExtensionSettings</span><span class="sxs-lookup"><span data-stu-id="09dbd-191">Reference guide for the ExtensionSettings policy</span></span>](microsoft-edge-manage-extensions-ref-guide.md)
- [<span data-ttu-id="09dbd-192">Perguntas frequentes sobre extensões do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="09dbd-192">FAQ for Microsoft Edge Extensions</span></span>](microsoft-edge-manage-extensions-faq.md)
- [<span data-ttu-id="09dbd-193">Página de aterrissagem do Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="09dbd-193">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
