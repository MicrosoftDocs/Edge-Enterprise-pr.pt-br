---
title: Definir as configurações de política do Microsoft Edge para Windows usando o Microsoft Intune.
ms.author: kvice
author: kelleyvice-msft
manager: laurawi
ms.date: 06/18/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Definir as configurações de política do Microsoft Edge para Windows usando o Microsoft Intune.
ms.openlocfilehash: 6200b52e9061f37f85fe0bfe7cf59a2172db97df
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979008"
---
# <span data-ttu-id="a20f7-103">Definir as configurações de política do Microsoft Edge com o Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="a20f7-103">Configure Microsoft Edge policy settings with Microsoft Intune</span></span>

<span data-ttu-id="a20f7-104">Este artigo explica como definir as configurações de política do Microsoft Edge para Windows 10 usando o Microsoft Intune.</span><span class="sxs-lookup"><span data-stu-id="a20f7-104">This article explains how to configure Microsoft Edge policy settings for Windows 10 using Microsoft Intune.</span></span>

> [!NOTE]
> <span data-ttu-id="a20f7-105">Este artigo aplica-se ao Microsoft Edge versão 77 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="a20f7-105">This article applies to Microsoft Edge version 77 or later.</span></span>

<span data-ttu-id="a20f7-106">Você pode definir políticas e configurações do Microsoft Edge adicionando um perfil de configuração de dispositivo ao Microsoft Intune.</span><span class="sxs-lookup"><span data-stu-id="a20f7-106">You can configure Microsoft Edge policies and settings by adding a device configuration profile to Microsoft Intune.</span></span> <span data-ttu-id="a20f7-107">Usar o Intune para gerenciar e aplicar políticas é o mesmo que usar a Política de grupo do Active Directory ou configurar as configurações locais do Objeto da política de grupo (GPO) nos dispositivos do usuário.</span><span class="sxs-lookup"><span data-stu-id="a20f7-107">Using Intune to manage and enforce policies is equivalent to using Active Directory Group Policy or configuring local Group Policy Object (GPO) settings on user devices.</span></span>

<span data-ttu-id="a20f7-108">Para obter mais informações sobre o gerenciamento de políticas do Microsoft Edge com o Microsoft Intune, leia [Gerenciar o acesso via Web usando o Microsoft Edge com o Microsoft Intune](https://docs.microsoft.com/intune/manage-microsoft-edge), mas lembre-se de que o artigo vinculado é específico para o Microsoft Edge versão 45 e anterior e, portanto, pode conter informações e referências que não se apliquem ao Microsoft Edge Enterprise versão 77 e posterior.</span><span class="sxs-lookup"><span data-stu-id="a20f7-108">For more information about managing Microsoft Edge policies with Microsoft Intune, you can read [Manage web access by using Microsoft Edge with Microsoft Intune](https://docs.microsoft.com/intune/manage-microsoft-edge), but keep in mind that the linked article is specific to Microsoft Edge version 45 and earlier and therefore may contain information and references that don't apply to Microsoft Edge Enterprise version 77 and later.</span></span>

> [!TIP]
> <span data-ttu-id="a20f7-109">Para obter informações sobre como configurar o Microsoft Edge no macOS usando o Microsoft Intune, consulte [Configurar para macOS](configure-microsoft-edge-on-mac.md).</span><span class="sxs-lookup"><span data-stu-id="a20f7-109">For information on how to configure Microsoft Edge on macOS using Microsoft Intune, see [Configure for macOS](configure-microsoft-edge-on-mac.md).</span></span>

## <span data-ttu-id="a20f7-110">Criar um perfil para gerenciar as configurações no Microsoft Edge para Windows 10</span><span class="sxs-lookup"><span data-stu-id="a20f7-110">Create a profile to manage settings in Microsoft Edge for Windows 10</span></span>

<span data-ttu-id="a20f7-111">Usando os Modelos Administrativos no Microsoft Intune, você pode gerenciar as políticas de grupo do Microsoft Edge em seus dispositivos Windows 10 usando a nuvem.</span><span class="sxs-lookup"><span data-stu-id="a20f7-111">Using Administrative Templates in Microsoft Intune, you can manage Microsoft Edge group policies on your Windows 10 devices using the cloud.</span></span> <span data-ttu-id="a20f7-112">Esta seção ajudará você a criar um modelo para definir as configurações de aplicativo específicas do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="a20f7-112">This section will help you create a template to configure Microsoft Edge-specific application settings.</span></span> <span data-ttu-id="a20f7-113">Quando você cria o modelo, ele cria um perfil de configuração de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a20f7-113">When you create the template, it creates a device configuration profile.</span></span> <span data-ttu-id="a20f7-114">Você então poderá atribuir ou implantar esse perfil em dispositivos Windows 10 em sua organização.</span><span class="sxs-lookup"><span data-stu-id="a20f7-114">You can then assign or deploy this profile to Windows 10 devices in your organization.</span></span>

### <span data-ttu-id="a20f7-115">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="a20f7-115">Prerequisites</span></span>

- <span data-ttu-id="a20f7-116">Windows 10 com os seguintes requisitos mínimos do sistema:</span><span class="sxs-lookup"><span data-stu-id="a20f7-116">Windows 10 with the following minimum system requirements:</span></span>
  - <span data-ttu-id="a20f7-117">Windows 10, versão 1909</span><span class="sxs-lookup"><span data-stu-id="a20f7-117">Windows 10, version 1909</span></span>
  - <span data-ttu-id="a20f7-118">Windows 10, versão 1903 com [KB4512941](https://support.microsoft.com/kb/4512941) instalado</span><span class="sxs-lookup"><span data-stu-id="a20f7-118">Windows 10, version 1903 with [KB4512941](https://support.microsoft.com/kb/4512941) installed</span></span>
  - <span data-ttu-id="a20f7-119">Windows 10, versão 1809 com [KB4512534](https://support.microsoft.com/kb/4512534) instalado</span><span class="sxs-lookup"><span data-stu-id="a20f7-119">Windows 10, version 1809 with [KB4512534](https://support.microsoft.com/kb/4512534) installed</span></span>
  - <span data-ttu-id="a20f7-120">Windows 10, versão 1803 com [KB4512509](https://support.microsoft.com/kb/4512509) instalado</span><span class="sxs-lookup"><span data-stu-id="a20f7-120">Windows 10, version 1803 with [KB4512509](https://support.microsoft.com/kb/4512509) installed</span></span>
  - <span data-ttu-id="a20f7-121">Windows 10, versão 1709 com [KB4516071](https://support.microsoft.com/kb/4516071) instalado</span><span class="sxs-lookup"><span data-stu-id="a20f7-121">Windows 10, version 1709 with [KB4516071](https://support.microsoft.com/kb/4516071) installed</span></span>

### <span data-ttu-id="a20f7-122">Usar Modelos administrativos para criar uma política para o Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="a20f7-122">Use Administrative Templates to create a policy for Microsoft Edge</span></span>

<span data-ttu-id="a20f7-123">Esse procedimento alavanca os Modelos Administrativos (que você pode estar familiarizado com a Política de grupo) que são incorporados no Intune.</span><span class="sxs-lookup"><span data-stu-id="a20f7-123">This procedure leverages Administrative templates (which you might be familiar with from Group Policy) that are built into Intune.</span></span> <span data-ttu-id="a20f7-124">Você pode usar esses modelos para criar uma política para o Microsoft Edge, selecionando configurações de uma lista pré-configurada.</span><span class="sxs-lookup"><span data-stu-id="a20f7-124">You can use these templates to create a policy for Microsoft Edge by selecting settings from a pre-configured list.</span></span>

1. <span data-ttu-id="a20f7-125">Entrar no portal do [Microsoft Endpoint Manager](https://endpoint.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="a20f7-125">Sign in to the [Microsoft Endpoint Manager](https://endpoint.microsoft.com/) portal.</span></span>
2. <span data-ttu-id="a20f7-126">Selecione **Dispositivos** no painel de navegação à esquerda.</span><span class="sxs-lookup"><span data-stu-id="a20f7-126">Select **Devices** in the left-hand navigation pane.</span></span>
3. <span data-ttu-id="a20f7-127">Em **Dispositivos** | **Visão geral**, selecione **Perfis de configuração** (em Título da política).</span><span class="sxs-lookup"><span data-stu-id="a20f7-127">From **Devices** | **Overview**, select **Configuration Profiles** (under Policy heading).</span></span>
4. <span data-ttu-id="a20f7-128">Na barra de comandos superior, selecione **Criar perfil**.</span><span class="sxs-lookup"><span data-stu-id="a20f7-128">On the top command bar, select **Create profile**.</span></span>
5. <span data-ttu-id="a20f7-129">Na lista suspensa abaixo **Plataforma**, selecione **Windows 10 e versão posterior**.</span><span class="sxs-lookup"><span data-stu-id="a20f7-129">In the drop-down list below **Platform**, select **Windows 10 and later**.</span></span>
6. <span data-ttu-id="a20f7-130">Na lista suspensa abaixo **Perfil**, selecione **Modelos administrativos** e clique no botão **Criar**.</span><span class="sxs-lookup"><span data-stu-id="a20f7-130">In the drop-down list below **Profile**, select **Administrative Templates** and then click the **Create** button.</span></span> <span data-ttu-id="a20f7-131">A próxima captura de tela mostra as listas suspensas para selecionar a plataforma e o tipo de perfil.</span><span class="sxs-lookup"><span data-stu-id="a20f7-131">The next screenshot shows the drop-down lists to select the platform and type of profile.</span></span>

    ![Selecionar a plataforma e o tipo de perfil](./media/configure-edge-with-intune/create-profile-platform.png)

7. <span data-ttu-id="a20f7-133">Na guia **Básico**, insira um **Nome**, descritivo como política do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="a20f7-133">On the **Basics** tab, enter a descriptive **Name**, such as Microsoft Edge Policy.</span></span> <span data-ttu-id="a20f7-134">Opcionalmente, insira uma **Descrição** para a política.</span><span class="sxs-lookup"><span data-stu-id="a20f7-134">Optionally, enter a  **Description** for the policy.</span></span>
<span data-ttu-id="a20f7-135">A próxima captura de tela mostra o formulário da guia **Básico** e a barra de menus mostra as próximas etapas (como guias acinzentadas) para criar o perfil.</span><span class="sxs-lookup"><span data-stu-id="a20f7-135">The next screenshot shows the form for the **Basics** tab and the menu bar shows the next steps (as grayed out tabs) to create the profile.</span></span>

   ![Insira Nome e Descrição](./media/configure-edge-with-intune/create-profile-basics-tab.png)

8. <span data-ttu-id="a20f7-137">Selecione **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="a20f7-137">Select **Next**.</span></span>
9. <span data-ttu-id="a20f7-138">Na guia **Configurações**, selecione a pasta Microsoft Edge em um dos seguintes locais:</span><span class="sxs-lookup"><span data-stu-id="a20f7-138">On the **Configuration settings** tab, select the Microsoft Edge folder in one of the following locations:</span></span>

   - <span data-ttu-id="a20f7-139">abaixo da pasta Configuração do computador</span><span class="sxs-lookup"><span data-stu-id="a20f7-139">below the Computer Configuration folder</span></span>
   - <span data-ttu-id="a20f7-140">abaixo da pasta Configuração do usuário.</span><span class="sxs-lookup"><span data-stu-id="a20f7-140">below the User Configuration folder.</span></span>

   <span data-ttu-id="a20f7-141">As configurações disponíveis do Microsoft Edge serão exibidas no painel direito.</span><span class="sxs-lookup"><span data-stu-id="a20f7-141">The available settings for Microsoft Edge will be shown on the right pane.</span></span> <span data-ttu-id="a20f7-142">Por exemplo, *Configuração do computador/Microsoft Edge/Permitir restrições de download* exibidos na captura de tela a seguir.</span><span class="sxs-lookup"><span data-stu-id="a20f7-142">For example, *Computer Configuration/Microsoft Edge/Allow download restrictions* shown in the following screenshot.</span></span>

   ![Guia Definições de configuração](./media/configure-edge-with-intune/create-profile-configuration-settings-tab.png)

   > [!NOTE]
   > <span data-ttu-id="a20f7-144">Consulte [Microsoft Edge – Políticas](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies) e [Microsoft Edge – Políticas de atualização](https://docs.microsoft.com/DeployEdge/microsoft-edge-update-policies) para a lista mais completa e atualizada de todas as configurações disponíveis do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="a20f7-144">See [Microsoft Edge – Policies](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies) and [Microsoft Edge – Update policies](https://docs.microsoft.com/DeployEdge/microsoft-edge-update-policies) for the most complete and up to date list of all the available settings for Microsoft Edge.</span></span>

10. <span data-ttu-id="a20f7-145">Use o campo de pesquisa ("Pesquisar para filtrar itens...") para encontrar uma configuração específica que você quer configurar.</span><span class="sxs-lookup"><span data-stu-id="a20f7-145">Use the search field ("Search to filter items ...") to find a specific setting you want to configure.</span></span> <span data-ttu-id="a20f7-146">Nesse exemplo, a cadeia de caracteres de pesquisa é "página inicial".</span><span class="sxs-lookup"><span data-stu-id="a20f7-146">In this example, the search string is "home page".</span></span> <span data-ttu-id="a20f7-147">A próxima captura de tela mostra os resultados da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="a20f7-147">The next screenshot shows the search results.</span></span>

    ![Resultados de pesquisas](./media/configure-edge-with-intune/create-profile-configuration-settings-tab-search.png)

11. <span data-ttu-id="a20f7-149">Depois de encontrar a configuração que quer configurar, selecione-a para expor os valores que você pode definir.</span><span class="sxs-lookup"><span data-stu-id="a20f7-149">After you find the setting you intend to configure, select it to expose the values you can set.</span></span> <span data-ttu-id="a20f7-150">Na próxima captura de tela, selecionamos "Configurar a URL da página inicial" como um exemplo.</span><span class="sxs-lookup"><span data-stu-id="a20f7-150">In the next screenshot, we selected "Configure the home page URL" as an example.</span></span>

    ![Configurar a política de URL da página inicial](./media/configure-edge-with-intune/create-profile-configuration-settings-tab-edit-pol.png)

12. <span data-ttu-id="a20f7-152">Habilitar a política e inserir um valor para a URL da página inicial, como mostrado na captura de tela anterior.</span><span class="sxs-lookup"><span data-stu-id="a20f7-152">Enable the policy and enter a value for the Home page URL, as shown in the previous screenshot.</span></span>

13. <span data-ttu-id="a20f7-153">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="a20f7-153">Click **OK**.</span></span> <span data-ttu-id="a20f7-154">A coluna "Status" deve ser exibida como "Habilitada", conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="a20f7-154">The settings "State" column should appear as "Enabled", as shown in the following screenshot example.</span></span>

    ![O status de configuração está Habilitado](./media/configure-edge-with-intune/create-profile-configuration-settings-tab-set-enabled.png)

14. <span data-ttu-id="a20f7-156">Clique no botão **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="a20f7-156">Click the **Next** button.</span></span>

15. <span data-ttu-id="a20f7-157">Na guia **Rótulos de escopo**, adicione um rótulo de escopo se você quiser, do contrário, clique no botão **Próximo**.</span><span class="sxs-lookup"><span data-stu-id="a20f7-157">On the **Scope tags** tab, add a Scope tag if wanted, otherwise click the **Next** button.</span></span>

16. <span data-ttu-id="a20f7-158">Na guia **Atribuições**, clique em **+ Selecionar grupos para incluir** para atribuir essa política ao grupo do Azure Active Directory (Azure AD) que contiver os dispositivos ou os usuários que você quer que recebam essa configuração de política.</span><span class="sxs-lookup"><span data-stu-id="a20f7-158">On the **Assignments** tab, click **+ Select groups to include** to assign this policy to the Azure Active Directory (Azure AD) group that contains the devices or the users that you want to receive this policy setting.</span></span> <span data-ttu-id="a20f7-159">Consulte [Atribuir perfis de usuário e dispositivo no Microsoft Intune](https://docs.microsoft.com/intune/device-profile-assign) para obter mais informações sobre como atribuir o perfil ao seu usuário ou aos seus grupos de dispositivos do Azure AD.</span><span class="sxs-lookup"><span data-stu-id="a20f7-159">See [Assign user and device profiles in Microsoft Intune](https://docs.microsoft.com/intune/device-profile-assign) for information about how to assign the profile to your Azure AD user or device groups.</span></span>

    ![Selecionar grupos para incluir](./media/configure-edge-with-intune/create-profile-assignments-tab.png)

17. <span data-ttu-id="a20f7-161">Clique no botão **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="a20f7-161">Click the **Next** button.</span></span>

18. <span data-ttu-id="a20f7-162">Na guia **Revisar + criar**, examine o resumo das suas alterações para verificar se está correto e clique no botão **Criar**.</span><span class="sxs-lookup"><span data-stu-id="a20f7-162">On the **Review + create** tab, review the summary of your changes to ensure it's correct and then click the **Create** button.</span></span>

19. <span data-ttu-id="a20f7-163">A política recém-criada (Política do Microsoft Edge) é exibida na captura de tela a seguir.</span><span class="sxs-lookup"><span data-stu-id="a20f7-163">The newly created policy (Microsoft Edge Policy) is shown in the following screenshot.</span></span>

    ![Selecionar grupos para incluir](./media/configure-edge-with-intune/create-profile-new-policy-finished.png)

<span data-ttu-id="a20f7-165">Para obter mais informações sobre perfis do Windows 10, consulte [Usar modelos do Windows 10 para definir configurações de política de grupo no Microsoft Intune](https://docs.microsoft.com/intune/administrative-templates-windows).</span><span class="sxs-lookup"><span data-stu-id="a20f7-165">For more information about Windows 10 profiles, see [Use Windows 10 templates to configure group policy settings in Microsoft Intune](https://docs.microsoft.com/intune/administrative-templates-windows).</span></span>

## <span data-ttu-id="a20f7-166">Consulte também</span><span class="sxs-lookup"><span data-stu-id="a20f7-166">See also</span></span>

- [<span data-ttu-id="a20f7-167">Página de aterrissagem do Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="a20f7-167">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="a20f7-168">Gerenciar o acesso via Web usando o Microsoft Edge com o Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="a20f7-168">Manage web access by using Microsoft Edge with Microsoft Intune</span></span>](https://docs.microsoft.com/intune/manage-microsoft-edge)
- [<span data-ttu-id="a20f7-169">Usar os modelos di Windows 10 para definir as configurações de política de grupo no Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="a20f7-169">Use Windows 10 templates to configure group policy settings in Microsoft Intune</span></span>](https://docs.microsoft.com/intune/administrative-templates-windows)
- [<span data-ttu-id="a20f7-170">Implantar o Microsoft Edge usando o Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="a20f7-170">Deploy Microsoft Edge using Microsoft Intune</span></span>](https://docs.microsoft.com/intune/apps/apps-windows-edge/?toc=https://docs.microsoft.com/DeployEdge/toc.json&bc=https://docs.microsoft.com/DeployEdge/breadcrumb/toc.json)
