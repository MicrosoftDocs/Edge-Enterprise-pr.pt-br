---
title: Configurar políticas do modo IE
ms.author: cjacks
author: cjacks
manager: saudm
ms.date: 03/25/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Configurar políticas do modo IE
ms.openlocfilehash: e33aa57b7877d50fe6a5d9e9a888d05c366b0ef0
ms.sourcegitcommit: f363ceb6c42054fabc95ce8d7bca3c52d80e6a9f
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/24/2021
ms.locfileid: "11447355"
---
# <a name="configure-ie-mode-policies"></a><span data-ttu-id="dcea6-103">Configurar políticas do modo IE</span><span class="sxs-lookup"><span data-stu-id="dcea6-103">Configure IE mode policies</span></span>

<span data-ttu-id="dcea6-104">Este artigo explica como configurar as políticas do modo IE.</span><span class="sxs-lookup"><span data-stu-id="dcea6-104">This article explains how to configure IE mode policies.</span></span>

> [!NOTE]
> <span data-ttu-id="dcea6-105">Este artigo se aplica aos Canais **Estável**, **Beta** e **Dev** do Microsoft Edge Beta, versão 77 ou posteriores.</span><span class="sxs-lookup"><span data-stu-id="dcea6-105">This article applies to Microsoft Edge **Stable**, **Beta** and **Dev** Channels, version 77 or later.</span></span>

<span data-ttu-id="dcea6-106">A configuração do modo IE tem três etapas:</span><span class="sxs-lookup"><span data-stu-id="dcea6-106">Configuring IE mode requires three steps:</span></span>

1. [<span data-ttu-id="dcea6-107">Configurar a integração do Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="dcea6-107">Configure Internet Explorer integration</span></span>](#configure-internet-explorer-integration)
2. [<span data-ttu-id="dcea6-108">Redirecionar sites do Microsoft Edge para o modo do IE</span><span class="sxs-lookup"><span data-stu-id="dcea6-108">Redirect sites from Microsoft Edge to IE mode</span></span>](#redirect-sites-from-microsoft-edge-to-ie-mode)
3. <span data-ttu-id="dcea6-109">(Opcional) [Redirecione sites do IE para Microsoft Edge](#redirect-sites-from-ie-to-microsoft-edge)</span><span class="sxs-lookup"><span data-stu-id="dcea6-109">(Optional) [Redirect sites from IE to Microsoft Edge](#redirect-sites-from-ie-to-microsoft-edge)</span></span>

> [!NOTE]
> <span data-ttu-id="dcea6-110">As políticas para habilitar o modo do IE podem ser configuradas por meio do Intune.</span><span class="sxs-lookup"><span data-stu-id="dcea6-110">Policies to enable IE mode can be configured through Intune.</span></span> <span data-ttu-id="dcea6-111">Para obter mais informações, confira [Adicionar o Microsoft Edge ao Microsoft Intune](/intune/apps/apps-windows-edge?bc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2fbreadcrumb%2ftoc.json&toc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2ftoc.json) e [Configurar as políticas do Microsoft Edge com o Microsoft Intune](./configure-edge-with-intune.md).</span><span class="sxs-lookup"><span data-stu-id="dcea6-111">For more information, see [Add Microsoft Edge to Microsoft Intune](/intune/apps/apps-windows-edge?bc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2fbreadcrumb%2ftoc.json&toc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2ftoc.json) and [Configure Microsoft Edge policies with Microsoft Intune](./configure-edge-with-intune.md).</span></span>

## <a name="configure-internet-explorer-integration"></a><span data-ttu-id="dcea6-112">Configurar a integração do Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="dcea6-112">Configure Internet Explorer integration</span></span>

<span data-ttu-id="dcea6-113">Você pode configurar o Internet Explorer para abrir diretamente no Microsoft Edge (modo IE).</span><span class="sxs-lookup"><span data-stu-id="dcea6-113">You can configure Internet Explorer to open directly within Microsoft Edge (IE mode).</span></span> <span data-ttu-id="dcea6-114">Você também pode configurar o Internet Explorer para abrir com uma janela independente do Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="dcea6-114">You can also configure Internet Explorer to open with a standalone Internet Explorer 11 window.</span></span> <span data-ttu-id="dcea6-115">A maioria dos usuários prefere quando os sites são abertos diretamente dentro do Microsoft Edge no modo IE.</span><span class="sxs-lookup"><span data-stu-id="dcea6-115">Most users prefer when sites open directly within Microsoft Edge in IE mode.</span></span>

### <a name="enable-internet-explorer-integration-using-group-policy"></a><span data-ttu-id="dcea6-116">Habilitar a integração do Internet Explorer usando a Política de Grupo</span><span class="sxs-lookup"><span data-stu-id="dcea6-116">Enable Internet Explorer integration using Group Policy</span></span>

1. <span data-ttu-id="dcea6-117">Baixar e usar o [Modelo de Política do Microsoft Edge](https://www.microsoft.com/en-us/edge/business/download) mais recente.</span><span class="sxs-lookup"><span data-stu-id="dcea6-117">Download and use the latest [Microsoft Edge Policy Template](https://www.microsoft.com/en-us/edge/business/download).</span></span>
2. <span data-ttu-id="dcea6-118">Abra o Editor de Políticas de Grupo.</span><span class="sxs-lookup"><span data-stu-id="dcea6-118">Open Group Policy Editor.</span></span>
3. <span data-ttu-id="dcea6-119">Clique em **Configuração do Computador** > **Modelos Administrativos** > **Microsoft Edge**.</span><span class="sxs-lookup"><span data-stu-id="dcea6-119">Click **Computer Configuration** > **Administrative Templates** > **Microsoft Edge**.</span></span>
4. <span data-ttu-id="dcea6-120">Clique duas vezes em **Configurar integração do Internet Explorer**.</span><span class="sxs-lookup"><span data-stu-id="dcea6-120">Double-click **Configure Internet Explorer integration**.</span></span>
5. <span data-ttu-id="dcea6-121">Selecione **Habilitado**.</span><span class="sxs-lookup"><span data-stu-id="dcea6-121">Select **Enabled**.</span></span>
6. <span data-ttu-id="dcea6-122">Em **Opções**, defina o valor da lista suspensa como</span><span class="sxs-lookup"><span data-stu-id="dcea6-122">Under **Options**, set the dropdown value to</span></span> 
   -  <span data-ttu-id="dcea6-123">**Modo Internet Explorer** se você deseja que os sites sejam abertos no modo IE no Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="dcea6-123">**Internet Explorer mode** if you want sites to open in IE mode on Microsoft Edge</span></span>
   -  <span data-ttu-id="dcea6-124">\*\* Internet Explorer 11\*\* se desejar que os sites sejam abertos em uma janela independente do Internet Explorer 11</span><span class="sxs-lookup"><span data-stu-id="dcea6-124">**Internet Explorer 11** if you want sites to open in a standalone Internet Explorer 11 window</span></span>
   -  <span data-ttu-id="dcea6-125">**Nenhum** se você quiser impedir que os usuários configurem o modo Internet Explorer via edge://sinalizadores ou pela linha de comando</span><span class="sxs-lookup"><span data-stu-id="dcea6-125">**None** if you want to stop users from configuring Internet Explorer mode via edge://flags or through the command line</span></span>

   > [!NOTE]
   > <span data-ttu-id="dcea6-126">Definir a política para **Desabilitada** significa que o modo de IE está desabilitado por política, mas pode ser definido por meio de edge://flags ou opções de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="dcea6-126">Setting the policy to **Disabled** implies IE mode is disabled by policy, but can be set through edge://flags or command line options.</span></span>
7. <span data-ttu-id="dcea6-127">Clique em **OK** ou em **Aplicar** para salvar essa configuração de política.</span><span class="sxs-lookup"><span data-stu-id="dcea6-127">Click **OK** or **Apply** to save this policy setting.</span></span>

## <a name="redirect-sites-from-microsoft-edge-to-ie-mode"></a><span data-ttu-id="dcea6-128">Redirecionar sites do Microsoft Edge para o modo do IE</span><span class="sxs-lookup"><span data-stu-id="dcea6-128">Redirect sites from Microsoft Edge to IE mode</span></span>

<span data-ttu-id="dcea6-129">Existem duas opções para identificar quais sites devem abrir no modo IE:</span><span class="sxs-lookup"><span data-stu-id="dcea6-129">There are two options for identifying which sites should open in IE mode:</span></span>

- <span data-ttu-id="dcea6-130">(Recomendado) [Configurar sites na lista de sites da empresa](#configure-sites-on-the-enterprise-site-list)</span><span class="sxs-lookup"><span data-stu-id="dcea6-130">(Recommended) [Configure sites on the Enterprise Site list](#configure-sites-on-the-enterprise-site-list)</span></span>
- [<span data-ttu-id="dcea6-131">Configurar todos os sites de Intranet</span><span class="sxs-lookup"><span data-stu-id="dcea6-131">Configure all Intranet sites</span></span>](#configure-all-intranet-sites)

### <a name="configure-sites-on-the-enterprise-site-list"></a><span data-ttu-id="dcea6-132">Configurar sites na lista de sites da empresa</span><span class="sxs-lookup"><span data-stu-id="dcea6-132">Configure sites on the Enterprise Site list</span></span>

<span data-ttu-id="dcea6-133">Você pode usar as seguintes políticas de grupo para configurar sites específicos para serem abertos no modo IE:</span><span class="sxs-lookup"><span data-stu-id="dcea6-133">You can use the following group policies to configure specific sites to open in IE mode:</span></span>

- <span data-ttu-id="dcea6-134">[Usar a lista de sites do IE no Modo Empresarial](#configure-using-the-use-the-enterprise-mode-ie-website-list-policy) (Internet Explorer)</span><span class="sxs-lookup"><span data-stu-id="dcea6-134">[Use the Enterprise Mode IE website list](#configure-using-the-use-the-enterprise-mode-ie-website-list-policy) (Internet Explorer)</span></span>
- <span data-ttu-id="dcea6-135">[Configurar a lista de sites do Modo Empresarial](#configure-using-the-configure-the-enterprise-mode-site-list-policy) (Microsoft Edge, versão 78 ou posterior)</span><span class="sxs-lookup"><span data-stu-id="dcea6-135">[Configure the Enterprise Mode Site List](#configure-using-the-configure-the-enterprise-mode-site-list-policy) (Microsoft Edge, version 78 or later)</span></span><br/><span data-ttu-id="dcea6-136">Esta política permite criar uma lista de Sites do Modo Empresarial separada para o Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="dcea6-136">This policy lets you create a separate Enterprise Mode Site list for Microsoft Edge.</span></span> <span data-ttu-id="dcea6-137">A habilitação desta política substitui as configurações da política "Usar a lista de sites do Modo Empresarial IE", se "Configurar integração do Internet Explorer" estiver habilitado.</span><span class="sxs-lookup"><span data-stu-id="dcea6-137">Enabling this policy overrides the settings in the "Use the Enterprise Mode IE website list" policy, if "Configure Internet Explorer integration" is enabled.</span></span> <span data-ttu-id="dcea6-138">Desabilitar ou não configurar essa política não afeta o comportamento padrão da política "Configurar integração do Internet Explorer".</span><span class="sxs-lookup"><span data-stu-id="dcea6-138">Disabling or not configuring this policy doesn't affect the default behavior of the "Configure Internet Explorer integration" policy.</span></span>
    > [!NOTE]
    > <span data-ttu-id="dcea6-139">Não é obrigatório configurar a política do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="dcea6-139">It is not mandatory to configure the Microsoft Edge policy.</span></span> <span data-ttu-id="dcea6-140">Muitas organizações usam isso como uma substituição, permitindo-as direcionar a Lista de Sites atual para todos os usuários com a política do IE e direcionar mais facilmente uma versão atualizada para usos piloto com a política do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="dcea6-140">Many organizations use this as an override, allowing them to target the current Site List at all users with the IE policy, and more easily target an updated version to pilot uses with the Microsoft Edge policy.</span></span>

<span data-ttu-id="dcea6-141">Para obter mais informações sobre as listas de sites do Modo Empresarial, consulte:</span><span class="sxs-lookup"><span data-stu-id="dcea6-141">For more information about Enterprise Mode Site lists, see:</span></span>

- [<span data-ttu-id="dcea6-142">Usar o Enterprise Mode Site List Manager</span><span class="sxs-lookup"><span data-stu-id="dcea6-142">Use the Enterprise Mode Site List Manager</span></span>](/internet-explorer/ie11-deploy-guide/use-the-enterprise-mode-site-list-manager)
- <span data-ttu-id="dcea6-143">[Adicionar vários sites à lista de sites do Modo Empresarial usando um arquivo e o Enterprise Mode Site List Manager (esquema v.2)](/internet-explorer/ie11-deploy-guide/add-multiple-sites-to-enterprise-mode-site-list-using-the-version-2-schema-and-enterprise-mode-tool).</span><span class="sxs-lookup"><span data-stu-id="dcea6-143">[Add multiple sites to the Enterprise Mode site list using a file and the Enterprise Mode Site List Manager (schema v.2)](/internet-explorer/ie11-deploy-guide/add-multiple-sites-to-enterprise-mode-site-list-using-the-version-2-schema-and-enterprise-mode-tool).</span></span>

### <a name="configure-using-the-use-the-enterprise-mode-ie-website-list-policy"></a><span data-ttu-id="dcea6-144">Configurar usando a política de lista de sites Usar o Modo Empresarial IE</span><span class="sxs-lookup"><span data-stu-id="dcea6-144">Configure using the Use the Enterprise Mode IE website list policy</span></span>

<span data-ttu-id="dcea6-145">O modo IE pode usar a política existente que configura a Lista de Sites Empresariais para o Internet Explorer, permitindo criar e manter uma única lista.</span><span class="sxs-lookup"><span data-stu-id="dcea6-145">IE mode can use the existing policy configuring the Enterprise Site List for Internet Explorer, allowing you to create and maintain a single list.</span></span>

1. <span data-ttu-id="dcea6-146">Criar ou reutilizar um XML de lista de sites</span><span class="sxs-lookup"><span data-stu-id="dcea6-146">Create or reuse a Site List XML</span></span>
    1. <span data-ttu-id="dcea6-147">Todos os sites que têm o elemento _\<open-in\>IE11\</open-in\>_ serão abertos no modo IE.</span><span class="sxs-lookup"><span data-stu-id="dcea6-147">All sites that have the element _\<open-in\>IE11\</open-in\>_ will now open in IE mode.</span></span>
2. <span data-ttu-id="dcea6-148">Abra o Editor de Políticas de Grupo.</span><span class="sxs-lookup"><span data-stu-id="dcea6-148">Open Group Policy Editor.</span></span>
3. <span data-ttu-id="dcea6-149">Clique em **Configuração do Computador** > **Modelos Administrativos** > **Windows Components** > **Internet Explorer**.</span><span class="sxs-lookup"><span data-stu-id="dcea6-149">Click **Computer Configuration** > **Administrative Templates** > **Windows Components** > **Internet Explorer**.</span></span>
4. <span data-ttu-id="dcea6-150">Clique duas vezes em **Usar a lista de sites do IE do Modo Empresarial**.</span><span class="sxs-lookup"><span data-stu-id="dcea6-150">Double-click **Use the Enterprise Mode IE website list**.</span></span>
5. <span data-ttu-id="dcea6-151">Selecione **Habilitado**.</span><span class="sxs-lookup"><span data-stu-id="dcea6-151">Select **Enabled**.</span></span>
6. <span data-ttu-id="dcea6-152">Em **Opções**, digite o local da lista de sites.</span><span class="sxs-lookup"><span data-stu-id="dcea6-152">Under **Options**, type the location of website list.</span></span> <span data-ttu-id="dcea6-153">Você pode usar um dos seguintes locais:</span><span class="sxs-lookup"><span data-stu-id="dcea6-153">You can use one of the following locations:</span></span>
    - <span data-ttu-id="dcea6-154">(Recomendado) Local HTTPS: **https**:**//iemode/sites.xml**</span><span class="sxs-lookup"><span data-stu-id="dcea6-154">(Recommended) HTTPS location: **https**:**//iemode/sites.xml**</span></span>
    - <span data-ttu-id="dcea6-155">Arquivo da rede local: **\\\network\shares\sites.xml**</span><span class="sxs-lookup"><span data-stu-id="dcea6-155">Local network file: **\\\network\shares\sites.xml**</span></span>
    - <span data-ttu-id="dcea6-156">Arquivo local: **file:///c:/Users/\<user\>/Documents/sites.xml**</span><span class="sxs-lookup"><span data-stu-id="dcea6-156">Local file: **file:///c:/Users/\<user\>/Documents/sites.xml**</span></span>
7. <span data-ttu-id="dcea6-157">Clique em **OK** ou **Aplicar** para salvar essas configurações.</span><span class="sxs-lookup"><span data-stu-id="dcea6-157">Click **OK** or **Apply** to save these settings.</span></span>

### <a name="configure-using-the-configure-the-enterprise-mode-site-list-policy"></a><span data-ttu-id="dcea6-158">Configurar usando a política Configurar a Lista de Sites do Modo Empresarial</span><span class="sxs-lookup"><span data-stu-id="dcea6-158">Configure using the Configure the Enterprise Mode Site List policy</span></span>

<span data-ttu-id="dcea6-159">Você também pode configurar o modo IE com uma política separada para o Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="dcea6-159">You can also configure IE mode with a separate policy for Microsoft Edge.</span></span> <span data-ttu-id="dcea6-160">Essa política adicional permite substituir a lista de sites do IE.</span><span class="sxs-lookup"><span data-stu-id="dcea6-160">This additional policy allows you to override the IE site list.</span></span> <span data-ttu-id="dcea6-161">Por exemplo, algumas organizações direcionam a lista de sites de produção para todos os usuários.</span><span class="sxs-lookup"><span data-stu-id="dcea6-161">For example, some organizations will target the production site list to all users.</span></span> <span data-ttu-id="dcea6-162">Você pode implantar a lista de sites piloto em um pequeno grupo de usuários usando essa política.</span><span class="sxs-lookup"><span data-stu-id="dcea6-162">You can then deploy the pilot site list to a small group of users using this policy.</span></span>

1. <span data-ttu-id="dcea6-163">Criar ou reutilizar um XML de lista de sites</span><span class="sxs-lookup"><span data-stu-id="dcea6-163">Create or reuse a Site List XML</span></span>
    1. <span data-ttu-id="dcea6-164">Todos os sites que têm o elemento _\<open-in\>IE11\</open-in\>_ serão abertos no modo IE.</span><span class="sxs-lookup"><span data-stu-id="dcea6-164">All sites that have the element _\<open-in\>IE11\</open-in\>_ will now open in IE mode.</span></span>
2. <span data-ttu-id="dcea6-165">Abra o Editor de Políticas de Grupo.</span><span class="sxs-lookup"><span data-stu-id="dcea6-165">Open Group Policy Editor.</span></span>
3. <span data-ttu-id="dcea6-166">Clique em **Configuração do Computador** > **Modelos Administrativos** > **Microsoft Edge**.</span><span class="sxs-lookup"><span data-stu-id="dcea6-166">Click **Computer Configuration** > **Administrative Templates** > **Microsoft Edge**.</span></span>
4. <span data-ttu-id="dcea6-167">Clique duas vezes em **Configurar a Lista de Sites do Modo Empresarial**.</span><span class="sxs-lookup"><span data-stu-id="dcea6-167">Double-click **Configure the Enterprise Mode Site List**.</span></span>
5. <span data-ttu-id="dcea6-168">Selecione **Habilitado**.</span><span class="sxs-lookup"><span data-stu-id="dcea6-168">Select **Enabled**.</span></span>
6. <span data-ttu-id="dcea6-169">Em **Opções**, digite o local da lista de sites.</span><span class="sxs-lookup"><span data-stu-id="dcea6-169">Under **Options**, type the location of website list.</span></span> <span data-ttu-id="dcea6-170">Você pode usar um dos seguintes locais:</span><span class="sxs-lookup"><span data-stu-id="dcea6-170">You can use one of the following locations:</span></span>
    - <span data-ttu-id="dcea6-171">(Recomendado) Local HTTPS: **https**:**//iemode/sites.xml**</span><span class="sxs-lookup"><span data-stu-id="dcea6-171">(Recommended) HTTPS location: **https**:**//iemode/sites.xml**</span></span> <!--Trying to keep this from being an active link in MD -->
    - <span data-ttu-id="dcea6-172">Arquivo da rede local: **\\\network\shares\sites.xml**</span><span class="sxs-lookup"><span data-stu-id="dcea6-172">Local network file: **\\\network\shares\sites.xml**</span></span>
    - <span data-ttu-id="dcea6-173">Arquivo local: **file:///c:/Users/\<user\>/Documents/sites.xml**</span><span class="sxs-lookup"><span data-stu-id="dcea6-173">Local file: **file:///c:/Users/\<user\>/Documents/sites.xml**</span></span>
7. <span data-ttu-id="dcea6-174">Clique em **OK** ou **Aplicar** para salvar essas configurações.</span><span class="sxs-lookup"><span data-stu-id="dcea6-174">Click **OK** or **Apply** to save these settings.</span></span>

### <a name="configure-all-intranet-sites"></a><span data-ttu-id="dcea6-175">Configurar todos os sites de intranet</span><span class="sxs-lookup"><span data-stu-id="dcea6-175">Configure all intranet sites</span></span>

<span data-ttu-id="dcea6-176">O modo IE pode ser configurado como para todos os sites na zona da Intranet Local.</span><span class="sxs-lookup"><span data-stu-id="dcea6-176">IE mode can be configured as for all sites in the Local Intranet zone.</span></span> <span data-ttu-id="dcea6-177">Você pode remover sites individuais do modo IE usando uma Lista de Sites do Modo Empresarial.</span><span class="sxs-lookup"><span data-stu-id="dcea6-177">You can remove individual sites from IE mode using an Enterprise Mode Site List.</span></span>

>[!NOTE]
>
> <span data-ttu-id="dcea6-178">A zona da Intranet Local contém sites adicionados explicitamente, mas também atribui sites a essa zona usando heurística.</span><span class="sxs-lookup"><span data-stu-id="dcea6-178">The Local Intranet zone contains explicitly added sites, but also assigns sites to this zone using heuristics.</span></span> <span data-ttu-id="dcea6-179">Isso pode incluir nomes de host sem ponto (por exemplo, **https**:**//folhadepagamento**) e sites que o script de configuração do proxy configura para contornar o proxy.</span><span class="sxs-lookup"><span data-stu-id="dcea6-179">This can include dotless host names (e.g. **https**:**//payroll**) and sites that the proxy configuration script configures to bypass the proxy.</span></span> <span data-ttu-id="dcea6-180">Se uma parte externa controlar o DNS ou o proxy, ela poderá forçar que os sites usem o modo IE.</span><span class="sxs-lookup"><span data-stu-id="dcea6-180">If an external party controls DNS or proxy, they could potentially force websites into IE mode.</span></span>

1. <span data-ttu-id="dcea6-181">Abra o Editor de política de grupo local.</span><span class="sxs-lookup"><span data-stu-id="dcea6-181">Open Local Group Policy Editor.</span></span>
2. <span data-ttu-id="dcea6-182">Clique em **Configuração do Computador** > **Modelos Administrativos** > **Microsoft Edge**.</span><span class="sxs-lookup"><span data-stu-id="dcea6-182">Click **Computer Configuration** > **Administrative Templates** > **Microsoft Edge**.</span></span>
3. <span data-ttu-id="dcea6-183">Clique duas vezes em **Enviar todos os sites da intranet para o Internet Explorer**.</span><span class="sxs-lookup"><span data-stu-id="dcea6-183">Double-click **Send all intranet sites to Internet Explorer**.</span></span>
4. <span data-ttu-id="dcea6-184">Selecione **Habilitado** e clique em **OK** ou em **Aplicar** para salvar as configurações de política.</span><span class="sxs-lookup"><span data-stu-id="dcea6-184">Select **Enabled**, and then click **OK** or **Apply** to save the policy settings.</span></span>

## <a name="redirect-sites-from-ie-to-microsoft-edge"></a><span data-ttu-id="dcea6-185">Redirecionar sites do IE para o Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="dcea6-185">Redirect sites from IE to Microsoft Edge</span></span>

<span data-ttu-id="dcea6-186">Você pode impedir que os usuários usem o Internet Explorer para sites que não precisam dele.</span><span class="sxs-lookup"><span data-stu-id="dcea6-186">You can prevent your users from using Internet Explorer for sites that don't need it.</span></span> <span data-ttu-id="dcea6-187">O Internet Explorer pode redirecionar sites para o Microsoft Edge automaticamente se eles não estiverem na sua lista de sites.</span><span class="sxs-lookup"><span data-stu-id="dcea6-187">Internet Explorer can automatically redirect sites to Microsoft Edge if they aren't on your site list.</span></span>

1. <span data-ttu-id="dcea6-188">Abra o Editor de Políticas de Grupo.</span><span class="sxs-lookup"><span data-stu-id="dcea6-188">Open Group Policy Editor.</span></span>
2. <span data-ttu-id="dcea6-189">Clique em **Configuração do Computador** > **Ferramentas Administrativas** > **Componentes do Windows** > **Internet Explorer**.</span><span class="sxs-lookup"><span data-stu-id="dcea6-189">Click **Computer Configuration** > **Administrative Tools** > **Windows Components** > **Internet Explorer**.</span></span>
3. <span data-ttu-id="dcea6-190">Clique duas vezes em **Enviar todos os sites não incluídos na Lista de Sites do Modo Empresarial para o Microsoft Edge.**</span><span class="sxs-lookup"><span data-stu-id="dcea6-190">Double-click **Send all sites not included in the Enterprise Mode Site List to Microsoft Edge.**</span></span>
4. <span data-ttu-id="dcea6-191">Selecione **Habilitado**</span><span class="sxs-lookup"><span data-stu-id="dcea6-191">Select **Enabled**</span></span>
5. <span data-ttu-id="dcea6-192">Clique em **OK** ou **Aplicar** para salvar essas configurações.</span><span class="sxs-lookup"><span data-stu-id="dcea6-192">Click **OK** or **Apply** to save these settings.</span></span>
6. <span data-ttu-id="dcea6-193">Clique duas vezes em **Configurar qual canal do Microsoft Edge usar para abrir sites redirecionados**.</span><span class="sxs-lookup"><span data-stu-id="dcea6-193">Double-click **Configure which channel of Microsoft Edge to use for opening redirected sites**.</span></span>
7. <span data-ttu-id="dcea6-194">Selecione **Habilitado**.</span><span class="sxs-lookup"><span data-stu-id="dcea6-194">Select **Enabled**.</span></span>
8. <span data-ttu-id="dcea6-195">Em **Opções**, selecione as três principais opções para o canal - o Internet Explorer será redirecionado para a opção mais bem classificada que o usuário instalou no dispositivo:</span><span class="sxs-lookup"><span data-stu-id="dcea6-195">Under **Options**, select your top three choices for the channel to use - Internet Explorer will redirect to the highest ranked choice that the user has installed on that device:</span></span>
   - <span data-ttu-id="dcea6-196">Microsoft Edge Stable</span><span class="sxs-lookup"><span data-stu-id="dcea6-196">Microsoft Edge Stable</span></span>
   - <span data-ttu-id="dcea6-197">Microsoft Edge Beta versão 77 ou posterior</span><span class="sxs-lookup"><span data-stu-id="dcea6-197">Microsoft Edge Beta version 77 or later</span></span>
   - <span data-ttu-id="dcea6-198">Microsoft Edge Dev versão 77 ou posterior</span><span class="sxs-lookup"><span data-stu-id="dcea6-198">Microsoft Edge Dev version 77 or later</span></span>
   - <span data-ttu-id="dcea6-199">Microsoft Edge Canary versão 77 ou posterior</span><span class="sxs-lookup"><span data-stu-id="dcea6-199">Microsoft Edge Canary version 77 or later</span></span>
   - <span data-ttu-id="dcea6-200">Microsoft Edge versão 45 ou anterior</span><span class="sxs-lookup"><span data-stu-id="dcea6-200">Microsoft Edge version 45 or earlier</span></span>
9. <span data-ttu-id="dcea6-201">Clique em **OK** ou **Aplicar** para salvar essas configurações.</span><span class="sxs-lookup"><span data-stu-id="dcea6-201">Click **OK** or **Apply** to save these settings.</span></span>

## <a name="see-also"></a><span data-ttu-id="dcea6-202">Consulte também</span><span class="sxs-lookup"><span data-stu-id="dcea6-202">See also</span></span>

- [<span data-ttu-id="dcea6-203">Página de aterrissagem do Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="dcea6-203">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="dcea6-204">Sobre o modo IE</span><span class="sxs-lookup"><span data-stu-id="dcea6-204">About IE mode</span></span>](./edge-ie-mode.md)
- [<span data-ttu-id="dcea6-205">Informações adicionais sobre o Modo Empresarial</span><span class="sxs-lookup"><span data-stu-id="dcea6-205">Additional Enterprise Mode information</span></span>](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)