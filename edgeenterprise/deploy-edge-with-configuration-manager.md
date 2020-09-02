---
title: Implantar o Microsoft Edge usando o System Center Configuration Manager
ms.author: kvice
author: kelleyvice-msft
manager: laurawi
ms.date: 09/30/2019
audience: ITPro
ms.topic: procedural
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Saiba como implantar Microsoft Edge com o SCCM (System Center Configuration Manager).
ms.openlocfilehash: be14f2db3b28b7585bfad1706b9f82209235df0a
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979037"
---
# <span data-ttu-id="99e2d-103">Implantar o Microsoft Edge usando o System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="99e2d-103">Deploy Microsoft Edge using System Center Configuration Manager</span></span>

<span data-ttu-id="99e2d-104">Este artigo mostra como automatizar uma implantação do Microsoft Edge usando o SCCM (System Center Configuration Manager).</span><span class="sxs-lookup"><span data-stu-id="99e2d-104">This article shows you how to automate a Microsoft Edge deployment by using System Center Configuration Manager (SCCM).</span></span>

>[!NOTE]
><span data-ttu-id="99e2d-105">Este artigo aplica-se ao Microsoft Edge versão 77 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="99e2d-105">This article applies to Microsoft Edge version 77 or later.</span></span>

## <span data-ttu-id="99e2d-106">Antes de começar</span><span class="sxs-lookup"><span data-stu-id="99e2d-106">Before you begin</span></span>

<span data-ttu-id="99e2d-107">Revise as informações em [Introdução ao gerenciamento de aplicativos no Configuration Manager](https://docs.microsoft.com/sccm/apps/understand/introduction-to-application-management).</span><span class="sxs-lookup"><span data-stu-id="99e2d-107">Review the information in [Introduction to application management in Configuration Manager](https://docs.microsoft.com/sccm/apps/understand/introduction-to-application-management).</span></span> <span data-ttu-id="99e2d-108">Este artigo de gerenciamento de aplicativos ajudará você a entender a terminologia usada neste artigo e é um guia para preparar seu site para instalar aplicativos.</span><span class="sxs-lookup"><span data-stu-id="99e2d-108">This application management article will help you understand the terminology used in this article and is a guide to preparing your site to install applications.</span></span>

<span data-ttu-id="99e2d-109">Baixe os arquivos de instalação do Microsoft Edge (**MicrosoftEdgeDevEnterpriseX64.msi** e/ou **MicrosoftEdgeDevEnterpriseX86.msi**) da [página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise).</span><span class="sxs-lookup"><span data-stu-id="99e2d-109">Download the Microsoft Edge Enterprise installation files (**MicrosoftEdgeDevEnterpriseX64.msi** and/or **MicrosoftEdgeDevEnterpriseX86.msi**) from the [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise).</span></span>

<span data-ttu-id="99e2d-110">Armazene os arquivos de instalação do Microsoft Edge em um local de rede acessível.</span><span class="sxs-lookup"><span data-stu-id="99e2d-110">Make sure you store the Microsoft Edge installation files in an accessible network location.</span></span>

## <span data-ttu-id="99e2d-111">Criar o aplicativo</span><span class="sxs-lookup"><span data-stu-id="99e2d-111">Create the application</span></span>

<span data-ttu-id="99e2d-112">Você criará o aplicativo usando um assistente do Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="99e2d-112">You'll create the application using a Configuration Manager wizard.</span></span>

### <span data-ttu-id="99e2d-113">Iniciar o assistente para Criar Aplicativo e criar o aplicativo</span><span class="sxs-lookup"><span data-stu-id="99e2d-113">Start the Create Application Wizard and create the application</span></span>  

1. <span data-ttu-id="99e2d-114">No console do Configuration Manager, clique em **Biblioteca de Software** > **Gerenciamento de Aplicativos** > **Aplicativos**.</span><span class="sxs-lookup"><span data-stu-id="99e2d-114">In the Configuration Manager console, click **Software Library** > **Application Management** > **Applications**.</span></span>  

2. <span data-ttu-id="99e2d-115">Na guia **Início**, no grupo **Criar**, clique em **Criar Aplicativo**.</span><span class="sxs-lookup"><span data-stu-id="99e2d-115">On the **Home** tab, in the **Create** group, click **Create Application**.</span></span> <span data-ttu-id="99e2d-116">Ou clique com o botão direito do mouse em **Aplicativos** na barra de navegação e clique em **Criar Aplicativo**.</span><span class="sxs-lookup"><span data-stu-id="99e2d-116">Or, right-click on **Applications** in the navigation bar and then click **Create Application**.</span></span>

    ![Criar aplicativo](./media/edge-ent-deployment-sccm/edge-ent-create-app-1.png)

3. <span data-ttu-id="99e2d-118">Na página **Geral** do **Assistente para Criar Aplicativo**, escolha **Detectar automaticamente informações sobre este aplicativo em arquivos de instalação**.</span><span class="sxs-lookup"><span data-stu-id="99e2d-118">On the **General** page of the **Create Application Wizard**, choose **Automatically detect information about this application from installation files**.</span></span> <span data-ttu-id="99e2d-119">Isso preenche algumas das informações do assistente com informações extraídas do arquivo .msi de instalação.</span><span class="sxs-lookup"><span data-stu-id="99e2d-119">This pre-populates some of the information in the wizard with information that's extracted from the installation .msi file.</span></span> <span data-ttu-id="99e2d-120">Forneça as seguintes informações:</span><span class="sxs-lookup"><span data-stu-id="99e2d-120">Provide the following information:</span></span>  

   - <span data-ttu-id="99e2d-121">**Tipo**: escolha **Windows Installer (arquivo \*.msi)**.</span><span class="sxs-lookup"><span data-stu-id="99e2d-121">**Type**: Choose **Windows Installer (\*.msi file)**.</span></span>  

   - <span data-ttu-id="99e2d-122">**Local**: digite o local (ou clique em **Navegar** para selecionar o local) do arquivo de instalação **MicrosoftEdgeDevEnterpriseX64.msi** ou **MicrosoftEdgeDevEnterpriseX86.msi**.</span><span class="sxs-lookup"><span data-stu-id="99e2d-122">**Location**: Type the location (or click **Browse** to select the location) of the installation file **MicrosoftEdgeDevEnterpriseX64.msi** or **MicrosoftEdgeDevEnterpriseX86.msi**.</span></span> <span data-ttu-id="99e2d-123">Observe que o local deve ser especificado no formato *\\\Servidor\Compartilhamento\Arquivo* para que o Configuration Manager localize os arquivos de instalação.</span><span class="sxs-lookup"><span data-stu-id="99e2d-123">Note that the location must be specified in the form *\\\Server\Share\File* for Configuration Manager to locate the installation files.</span></span>  

   <span data-ttu-id="99e2d-124">A página **Especificar configurações para este aplicativo** será semelhante ao seguinte exemplo:</span><span class="sxs-lookup"><span data-stu-id="99e2d-124">Your **Specify settings for this application** page will look like the following example:</span></span>  

    ![Especificar configurações para este aplicativo](./media/edge-ent-deployment-sccm/edge-ent-create-app-2.png)

4. <span data-ttu-id="99e2d-126">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="99e2d-126">Click **Next**.</span></span> <span data-ttu-id="99e2d-127">Em **Detalhes** na página **Informações Importadas**, você verá informações sobre o aplicativo e todos os arquivos associados que foram importados.</span><span class="sxs-lookup"><span data-stu-id="99e2d-127">Under **Details** on the **Imported Information** page, you'll see information about the application and any associated files that were imported.</span></span> <span data-ttu-id="99e2d-128">Clique em **Avançar** para continuar com o assistente.</span><span class="sxs-lookup"><span data-stu-id="99e2d-128">Click **Next** to continue with the wizard.</span></span>  

    ![Exibir informações importadas](./media/edge-ent-deployment-sccm/edge-ent-create-app-3.png)

5. <span data-ttu-id="99e2d-130">Na página **Informações Gerais**, você pode adicionar mais informações sobre o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="99e2d-130">On the **General Information** page, you can add more information about the application.</span></span> <span data-ttu-id="99e2d-131">Por exemplo, Versão do software, Comentários do administrador e Editor.</span><span class="sxs-lookup"><span data-stu-id="99e2d-131">For example, Software version, Administrator comments, and Publisher.</span></span> <span data-ttu-id="99e2d-132">Você pode usar essas informações para ajudar a classificar e localizar o aplicativo no console do Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="99e2d-132">You can use this information to to help you sort and find the application in the Configuration Manager console.</span></span>

   <span data-ttu-id="99e2d-133">Você também pode usar o campo **Programa de instalação** para especificar a linha de comando completa que será usada para instalar o aplicativo em computadores.</span><span class="sxs-lookup"><span data-stu-id="99e2d-133">You can also use the **Installation program** field to specify the full command line that will be used to install the application on PCs.</span></span> <span data-ttu-id="99e2d-134">Você pode editar isso para adicionar suas próprias propriedades (por exemplo, **/q** para uma instalação autônoma).</span><span class="sxs-lookup"><span data-stu-id="99e2d-134">You can edit this to add your own properties (for example, **/q** for an unattended installation).</span></span>

   <span data-ttu-id="99e2d-135">A captura de tela a seguir mostra um exemplo em que os campos **Especificar informações sobre este aplicativo** são usados.</span><span class="sxs-lookup"><span data-stu-id="99e2d-135">The following screenshot shows an example where the **Specify information about this application** fields are used.</span></span>

   ![Especificar metadados do aplicativo](./media/edge-ent-deployment-sccm/edge-ent-create-app-5.png)

6. <span data-ttu-id="99e2d-137">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="99e2d-137">Click **Next**.</span></span>
7. <span data-ttu-id="99e2d-138">Na página **Resumo**, você pode confirmar as configurações do aplicativo em **Detalhes** e terminar de usar o assistente.</span><span class="sxs-lookup"><span data-stu-id="99e2d-138">On the **Summary** page, you can confirm your application settings under **Details** and then finish using the wizard.</span></span> <span data-ttu-id="99e2d-139">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="99e2d-139">Click **Next**.</span></span>  

    ![Detalhes de configurações do aplicativo](./media/edge-ent-deployment-sccm/edge-ent-create-app-6.png)

8. <span data-ttu-id="99e2d-141">Na página **Conclusão**, clique em **Fechar**.</span><span class="sxs-lookup"><span data-stu-id="99e2d-141">On the **Completion** page, click **Close**.</span></span>

    ![Caixa de diálogo Êxito](./media/edge-ent-deployment-sccm/edge-ent-create-app-7.png)

<span data-ttu-id="99e2d-143">Você terminou a criação do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="99e2d-143">You've finished creating the application.</span></span> <span data-ttu-id="99e2d-144">Use as etapas abaixo para vê-la no Configuration Manager:</span><span class="sxs-lookup"><span data-stu-id="99e2d-144">Use the following steps to see it in Configuration Manager:</span></span>

- <span data-ttu-id="99e2d-145">selecione o espaço de trabalho **Biblioteca de Software**</span><span class="sxs-lookup"><span data-stu-id="99e2d-145">select the **Software Library** workspace</span></span>
- <span data-ttu-id="99e2d-146">expanda **Gerenciamento de Aplicativos**</span><span class="sxs-lookup"><span data-stu-id="99e2d-146">expand **Application Management**</span></span>
- <span data-ttu-id="99e2d-147">clique em **Aplicativos**.</span><span class="sxs-lookup"><span data-stu-id="99e2d-147">click **Applications**.</span></span>

<span data-ttu-id="99e2d-148">A captura de tela a seguir mostra o exemplo usado neste artigo.</span><span class="sxs-lookup"><span data-stu-id="99e2d-148">The following screenshot shows the example used for this article.</span></span>  

![Aplicativos](./media/edge-ent-deployment-sccm/edge-ent-create-app-8.png)

## <span data-ttu-id="99e2d-150">Alterar as propriedades e as configurações de implantação do aplicativo</span><span class="sxs-lookup"><span data-stu-id="99e2d-150">Change application properties and deployment settings</span></span>

<span data-ttu-id="99e2d-151">Depois de criar um aplicativo, você poderá refinar as configurações do aplicativo, se necessário.</span><span class="sxs-lookup"><span data-stu-id="99e2d-151">After you create an application, you can refine the application settings if you need to.</span></span> <span data-ttu-id="99e2d-152">Para ver as propriedades do aplicativo:</span><span class="sxs-lookup"><span data-stu-id="99e2d-152">To look at the application properties:</span></span>

- <span data-ttu-id="99e2d-153">selecione o aplicativo</span><span class="sxs-lookup"><span data-stu-id="99e2d-153">select the application</span></span>
- <span data-ttu-id="99e2d-154">em **Início**>**Propriedades**, clique em **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="99e2d-154">in **Home**>**Properties**, click **Properties**.</span></span>  

   ![Configurar as propriedades do aplicativo](./media/edge-ent-deployment-sccm/edge-ent-create-app-req-1.png)

 <span data-ttu-id="99e2d-156">Na página de diálogo **Propriedades do Aplicativo <nome do aplicativo\>**, você verá uma exibição com guias dos itens que pode configurar para alterar o comportamento do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="99e2d-156">In the **<application name\> Application Properties** dialog page, you'll see a tabbed view of the items that you can configure to change the behavior of the application.</span></span> <span data-ttu-id="99e2d-157">Para obter mais informações sobre as configurações que você pode definir, consulte [Criar aplicativos](https://docs.microsoft.com/sccm/apps/deploy-use/create-applications).</span><span class="sxs-lookup"><span data-stu-id="99e2d-157">For more information about the settings you can configure, see [Create applications](https://docs.microsoft.com/sccm/apps/deploy-use/create-applications).</span></span>

<span data-ttu-id="99e2d-158">Neste exemplo, você mudará algumas propriedades do tipo de implantação do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="99e2d-158">For this example, you'll change some properties of the application's deployment type.</span></span> <span data-ttu-id="99e2d-159">Para alterar as propriedades da implantação:</span><span class="sxs-lookup"><span data-stu-id="99e2d-159">To change the deployment properties:</span></span>

1. <span data-ttu-id="99e2d-160">Clique na guia **Tipos de Implantação**.</span><span class="sxs-lookup"><span data-stu-id="99e2d-160">Click the **Deployment Types** tab.</span></span>
2. <span data-ttu-id="99e2d-161">Em **Tipos de implantação:**, selecione o aplicativo **Nome**</span><span class="sxs-lookup"><span data-stu-id="99e2d-161">Under **Deployment types:**, select the application **Name**</span></span>
3. <span data-ttu-id="99e2d-162">Clique em **Editar**.</span><span class="sxs-lookup"><span data-stu-id="99e2d-162">Click **Edit**.</span></span>

   ![Editar o tipo de implantação](./media/edge-ent-deployment-sccm/edge-ent-create-app-req-2.png)

### <span data-ttu-id="99e2d-164">Adicionar um requisito ao tipo de implantação</span><span class="sxs-lookup"><span data-stu-id="99e2d-164">Add a requirement to the deployment type</span></span>

 <span data-ttu-id="99e2d-165">Os requisitos especificam as condições que devem ser atendidas antes que um aplicativo seja instalado em um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="99e2d-165">Requirements specify conditions that must be met before an application is installed on a device.</span></span> <span data-ttu-id="99e2d-166">Você pode escolher entre os requisitos internos ou pode criar os seus próprios.</span><span class="sxs-lookup"><span data-stu-id="99e2d-166">You can choose from built-in requirements or you can create your own.</span></span> <span data-ttu-id="99e2d-167">Por exemplo, você pode adicionar um requisito de que o aplicativo só será instalado em computadores que estejam executando o Windows 10 **x86** ou **x64**, dependendo da arquitetura do processador de destino do arquivo de instalação.</span><span class="sxs-lookup"><span data-stu-id="99e2d-167">For example, you can add a requirement that the application will only be installed on PCs that are running Windows 10 **x86** or **x64**, depending on the installation file's target processor architecture.</span></span> <span data-ttu-id="99e2d-168">Neste exemplo, você especificará o Windows 10 **x86**.</span><span class="sxs-lookup"><span data-stu-id="99e2d-168">In this example, you'll specify Windows 10 **x86**.</span></span>

1. <span data-ttu-id="99e2d-169">Na página de propriedades do tipo de implantação que você acabou de abrir, clique na guia **Requisitos**.</span><span class="sxs-lookup"><span data-stu-id="99e2d-169">From the deployment type properties page you just opened, click the **Requirements** tab.</span></span>

2. <span data-ttu-id="99e2d-170">Clique em **Adicionar** para abrir o diálogo **Criar Requisito**.</span><span class="sxs-lookup"><span data-stu-id="99e2d-170">Click **Add** to open the **Create Requirement** dialog.</span></span>

    ![Criar requisito](./media/edge-ent-deployment-sccm/edge-ent-create-app-req-3.png)

3. <span data-ttu-id="99e2d-172">Na caixa de diálogo **Criar Requisito**, especifique as seguintes informações:</span><span class="sxs-lookup"><span data-stu-id="99e2d-172">In the **Create Requirement** dialog box, specify the following information:</span></span>

    - <span data-ttu-id="99e2d-173">**Categoria**: **Dispositivo**</span><span class="sxs-lookup"><span data-stu-id="99e2d-173">**Category**: **Device**</span></span>  

    - <span data-ttu-id="99e2d-174">**Condição**: **Sistema operacional**</span><span class="sxs-lookup"><span data-stu-id="99e2d-174">**Condition**: **Operating system**</span></span>  

    - <span data-ttu-id="99e2d-175">**Tipo de regra**: **valor**</span><span class="sxs-lookup"><span data-stu-id="99e2d-175">**Rule type**: **Value**</span></span>  

    - <span data-ttu-id="99e2d-176">**Operador**: **um de**</span><span class="sxs-lookup"><span data-stu-id="99e2d-176">**Operator**: **One of**</span></span>  

    - <span data-ttu-id="99e2d-177">Na lista dos sistemas operacionais, selecione **Windows 10** > **Todos os Windows 10 (32 bits)**.</span><span class="sxs-lookup"><span data-stu-id="99e2d-177">From the operating systems list, select **Windows 10** > **All Windows 10 (32-bit)**.</span></span>  

    <span data-ttu-id="99e2d-178">Quando você terminar, o diálogo será semelhante ao seguinte exemplo de captura de tela:</span><span class="sxs-lookup"><span data-stu-id="99e2d-178">When you're finished, the dialog will look like the following screenshot example:</span></span>

    ![Adicionar requisito](./media/edge-ent-deployment-sccm/edge-ent-create-app-req-4.png)

4. <span data-ttu-id="99e2d-180">Clique em **OK** para fechar cada página de propriedades aberta e retorne à lista **Aplicativos** no console do Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="99e2d-180">Click **OK** to close each open property page and return to the **Applications** list in the Configuration Manager console.</span></span>  

## <span data-ttu-id="99e2d-181">Adicionar o conteúdo do aplicativo a um ponto de distribuição</span><span class="sxs-lookup"><span data-stu-id="99e2d-181">Add the application content to a distribution point</span></span>  

<span data-ttu-id="99e2d-182">Para implantar o aplicativo atualizado em computadores, certifique-se de que o conteúdo do aplicativo seja copiado para um ponto de distribuição.</span><span class="sxs-lookup"><span data-stu-id="99e2d-182">To deploy the updated application to PCs, make sure that the application content is copied to a distribution point.</span></span> <span data-ttu-id="99e2d-183">Os computadores acessam o ponto de distribuição para instalar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="99e2d-183">PCs access the distribution point to install the application.</span></span>  

>[!TIP]
><span data-ttu-id="99e2d-184">Para saber mais sobre pontos de distribuição e gerenciamento de conteúdo no Configuration Manager, consulte [Implantar e gerenciar conteúdo para o System Center Configuration Manager](https://docs.microsoft.com/sccm/core/servers/deploy/configure/deploy-and-manage-content).</span><span class="sxs-lookup"><span data-stu-id="99e2d-184">To find out more about distribution points and content management in Configuration Manager, see [Deploy and manage content for System Center Configuration Manager](https://docs.microsoft.com/sccm/core/servers/deploy/configure/deploy-and-manage-content).</span></span>  

1. <span data-ttu-id="99e2d-185">No console do Configuration Manager, clique em **Biblioteca de Software**.</span><span class="sxs-lookup"><span data-stu-id="99e2d-185">In the Configuration Manager console, click **Software Library**.</span></span>  

2. <span data-ttu-id="99e2d-186">No espaço de trabalho **Biblioteca de Software**, expanda **Aplicativos**.</span><span class="sxs-lookup"><span data-stu-id="99e2d-186">In the **Software Library** workspace, expand **Applications**.</span></span> <span data-ttu-id="99e2d-187">Selecione o aplicativo que você criou na lista de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="99e2d-187">Select the application you created in the list of applications.</span></span>

3. <span data-ttu-id="99e2d-188">Na guia **Início**, no grupo **Implantação**, clique em **Distribuir Conteúdo**.</span><span class="sxs-lookup"><span data-stu-id="99e2d-188">On the **Home** tab in the **Deployment** group, click **Distribute Content**.</span></span>  

4. <span data-ttu-id="99e2d-189">Na página **Geral** do **Assistente para Distribuir Conteúdo**, verifique se o nome do aplicativo está correto e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="99e2d-189">On the **General** page of the **Distribute Content Wizard**, check that the application name is correct, and then click **Next**.</span></span>  

5. <span data-ttu-id="99e2d-190">Na página **Conteúdo**, revise as informações que serão copiadas para o ponto de distribuição e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="99e2d-190">On the **Content** page, review the information that will be copied to the distribution point, and then click **Next**.</span></span>  

6. <span data-ttu-id="99e2d-191">Na página **Destino de Conteúdo**, clique em **Adicionar** para selecionar uma ou mais coleções, pontos de distribuição ou grupos de pontos de distribuição nos quais será instalado o conteúdo do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="99e2d-191">On the **Content Destination** page, click **Add** to select one or more collections, distribution points, or distribution point groups on which to install the application content.</span></span>

7. <span data-ttu-id="99e2d-192">Conclua o assistente.</span><span class="sxs-lookup"><span data-stu-id="99e2d-192">Complete the wizard.</span></span>

<span data-ttu-id="99e2d-193">Você pode verificar se o conteúdo do aplicativo foi copiado com êxito para o ponto de distribuição do espaço de trabalho **Monitoramento**, em **Status de Distribuição** > **Status do Conteúdo**.</span><span class="sxs-lookup"><span data-stu-id="99e2d-193">You can check that the application content was copied successfully to the distribution point from the **Monitoring** workspace, under **Distribution Status** > **Content Status**.</span></span>  

## <span data-ttu-id="99e2d-194">Implantar o aplicativo</span><span class="sxs-lookup"><span data-stu-id="99e2d-194">Deploy the application</span></span>  

<span data-ttu-id="99e2d-195">Em seguida, implante o aplicativo em uma coleção de dispositivos em sua hierarquia.</span><span class="sxs-lookup"><span data-stu-id="99e2d-195">Next, deploy the application to a device collection in your hierarchy.</span></span> <span data-ttu-id="99e2d-196">Neste exemplo, você implanta o aplicativo na coleção de dispositivos **Todos os Sistemas**.</span><span class="sxs-lookup"><span data-stu-id="99e2d-196">In this example, you deploy the application to the **All Systems** device collection.</span></span>  

>[!TIP]
><span data-ttu-id="99e2d-197">Lembre-se de que somente os computadores Windows 10 da arquitetura de processador especificada instalarão o aplicativo por causa dos requisitos que você selecionou antes.</span><span class="sxs-lookup"><span data-stu-id="99e2d-197">Remember that only Windows 10 computers of the specified processor architecture will install the application because of the requirements that you selected earlier.</span></span>  

1. <span data-ttu-id="99e2d-198">No console do Configuration Manager, clique em **Biblioteca de Software** > **Gerenciamento de Aplicativos** > **Aplicativos**.</span><span class="sxs-lookup"><span data-stu-id="99e2d-198">In the Configuration Manager console, click **Software Library** > **Application Management** > **Applications**.</span></span>

2. <span data-ttu-id="99e2d-199">Na lista de aplicativos, selecione o aplicativo que você criou anteriormente.</span><span class="sxs-lookup"><span data-stu-id="99e2d-199">From the list of applications, select the application that you created earlier.</span></span> <span data-ttu-id="99e2d-200">Em seguida, na guia **Início** do grupo **Implantação**, clique em **Implantar** ou clique com o botão direito do mouse no aplicativo e selecione **Implantar**.</span><span class="sxs-lookup"><span data-stu-id="99e2d-200">Then, on the **Home** tab in the **Deployment** group, click **Deploy**, or right-click the application and select **Deploy**.</span></span>

    ![Implantar o aplicativo](./media/edge-ent-deployment-sccm/edge-ent-deploy-app-1.png)

3. <span data-ttu-id="99e2d-202">Na página **Geral** do **Assistente para Implantar Software**, clique em **Procurar** para selecionar a coleção de dispositivos para a qual você deseja implantar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="99e2d-202">On the **General** page of the **Deploy Software Wizard**, click **Browse** to select the device collection to which you want to deploy the application.</span></span>

    ![Procurar o arquivo de instalação](./media/edge-ent-deployment-sccm/edge-ent-deploy-app-2.png)

4. <span data-ttu-id="99e2d-204">Na página **Conteúdo**, verifique se o ponto de distribuição do qual deseja instalar o aplicativo está selecionado.</span><span class="sxs-lookup"><span data-stu-id="99e2d-204">On the **Content** page, check that the distribution point from which you want PCs to install the application is selected.</span></span>

    ![Especificar ponto de distribuição](./media/edge-ent-deployment-sccm/edge-ent-deploy-app-6.png)

5. <span data-ttu-id="99e2d-206">Na página **Configurações de Implantação**, verifique se a ação de implantação está definida como **Instalar**, e a finalidade da implantação é definida como **Obrigatória**.</span><span class="sxs-lookup"><span data-stu-id="99e2d-206">On the **Deployment Settings** page, make sure that the deployment action is set to **Install**, and the deployment purpose is set to **Required**.</span></span>

    ![Definir configurações de implantação](./media/edge-ent-deployment-sccm/edge-ent-deploy-app-8.png)

    >[!TIP]
    ><span data-ttu-id="99e2d-208">Ao definir a finalidade da implantação como **Obrigatória**, você deve verificar se o aplicativo está instalado em computadores que atendam aos requisitos definidos.</span><span class="sxs-lookup"><span data-stu-id="99e2d-208">By setting the deployment purpose to **Required**, you make sure that the application is installed on PCs that meet the requirements that you set.</span></span> <span data-ttu-id="99e2d-209">Se você definir esse valor como **Disponível**, os usuários poderão instalar o aplicativo sob demanda do Centro de Software.</span><span class="sxs-lookup"><span data-stu-id="99e2d-209">If you set this value to **Available**, then users can install the application on demand from Software Center.</span></span>  

6. <span data-ttu-id="99e2d-210">Na página **Agendamento**, você pode configurar quando o aplicativo será instalado.</span><span class="sxs-lookup"><span data-stu-id="99e2d-210">On the **Scheduling** page, you can configure when the application will be installed.</span></span> <span data-ttu-id="99e2d-211">Neste exemplo, selecione **O mais rápido possível após o horário disponível**.</span><span class="sxs-lookup"><span data-stu-id="99e2d-211">For this example, select **As soon as possible after the available time**.</span></span>

    ![Agendar a implantação](./media/edge-ent-deployment-sccm/edge-ent-deploy-app-9.png)

7. <span data-ttu-id="99e2d-213">Na página **Experiência do Usuário**, selecione os valores desejados e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="99e2d-213">On the **User Experience** page, select your desired values and click **Next**.</span></span>

    ![Especificar experiência do usuário](./media/edge-ent-deployment-sccm/edge-ent-deploy-app-10.png)

8. <span data-ttu-id="99e2d-215">Especifique as opções de alerta desejadas e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="99e2d-215">Specify your desired alert options and click **Next**.</span></span>

    ![Especificar configurações de alerta](./media/edge-ent-deployment-sccm/edge-ent-deploy-app-11.png)

9. <span data-ttu-id="99e2d-217">Conclua o assistente.</span><span class="sxs-lookup"><span data-stu-id="99e2d-217">Complete the wizard.</span></span>

<span data-ttu-id="99e2d-218">Use as informações na seção **Monitorar o aplicativo** a seguir para ver o status da implantação do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="99e2d-218">Use the information in the following **Monitor the application** section to see the status of your application deployment.</span></span>  

## <span data-ttu-id="99e2d-219">Monitorar o aplicativo</span><span class="sxs-lookup"><span data-stu-id="99e2d-219">Monitor the application</span></span>

 <span data-ttu-id="99e2d-220">Nesta seção, você examinará rapidamente o status de implantação do aplicativo que acabou de implantar.</span><span class="sxs-lookup"><span data-stu-id="99e2d-220">In this section, you'll take a quick look at the deployment status of the application that you just deployed.</span></span>  

### <span data-ttu-id="99e2d-221">Para revisar o status da implantação</span><span class="sxs-lookup"><span data-stu-id="99e2d-221">To review the deployment status</span></span>  

1. <span data-ttu-id="99e2d-222">No console do Configuration Manager, clique em **Monitoramento** > **Implantações**.</span><span class="sxs-lookup"><span data-stu-id="99e2d-222">In the Configuration Manager console, click **Monitoring** > **Deployments**.</span></span>  

2. <span data-ttu-id="99e2d-223">Na lista de implantações, selecione o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="99e2d-223">From the list of deployments, select the application.</span></span>

    ![Monitorar a implantação](./media/edge-ent-deployment-sccm/edge-ent-monitor-deployment.png)

3. <span data-ttu-id="99e2d-225">Na guia **Início**, no grupo **Implantação**, clique em **Exibir Status**.</span><span class="sxs-lookup"><span data-stu-id="99e2d-225">On the **Home** tab in the **Deployment** group, click **View Status**.</span></span>  

4. <span data-ttu-id="99e2d-226">Selecione uma das seguintes guias para ver mais atualizações de status sobre a implantação do aplicativo:</span><span class="sxs-lookup"><span data-stu-id="99e2d-226">Select one of the following tabs to see more status updates about the application deployment:</span></span>  

    - <span data-ttu-id="99e2d-227">**Êxito**: o aplicativo foi instalado com êxito nos computadores indicados.</span><span class="sxs-lookup"><span data-stu-id="99e2d-227">**Success**: The application installed successfully on the indicated PCs.</span></span>  

    - <span data-ttu-id="99e2d-228">**Em Andamento**: a instalação do aplicativo ainda não terminou.</span><span class="sxs-lookup"><span data-stu-id="99e2d-228">**In Progress**: The application has not yet finished installing.</span></span>  

    - <span data-ttu-id="99e2d-229">**Erro**: ocorreu um erro ao instalar o aplicativo nos computadores indicados.</span><span class="sxs-lookup"><span data-stu-id="99e2d-229">**Error**: An error occurred installing the application on the indicated PCs.</span></span> <span data-ttu-id="99e2d-230">Mais informações sobre o erro também são exibidas.</span><span class="sxs-lookup"><span data-stu-id="99e2d-230">Further information about the error is also displayed.</span></span>  

    - <span data-ttu-id="99e2d-231">**Requisitos não atendidos**: nenhuma tentativa de instalação foi feita nos dispositivos indicados porque eles não atenderam aos requisitos que você configurou (neste exemplo, porque eles não são executados no Windows 10).</span><span class="sxs-lookup"><span data-stu-id="99e2d-231">**Requirements Not Met**: No installation attempt was made on the indicated devices because they did not meet the requirements you configured (in this example, because they do not run on Windows 10.)</span></span>

    - <span data-ttu-id="99e2d-232">**Desconhecido**: o Configuration Manager não pôde relatar o status da implantação.</span><span class="sxs-lookup"><span data-stu-id="99e2d-232">**Unknown**: Configuration Manager was unable to report the status of the deployment.</span></span> <span data-ttu-id="99e2d-233">Verifique novamente mais tarde.</span><span class="sxs-lookup"><span data-stu-id="99e2d-233">Check back again later.</span></span>  

    >[!TIP]
    ><span data-ttu-id="99e2d-234">Há várias maneiras de monitorar implantações de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="99e2d-234">There are several ways you can monitor application deployments.</span></span> <span data-ttu-id="99e2d-235">Para obter mais informações, consulte [Monitorar aplicativos do console do System Center Configuration Manager](https://docs.microsoft.com/sccm/apps/deploy-use/monitor-applications-from-the-console).</span><span class="sxs-lookup"><span data-stu-id="99e2d-235">For more information, see [Monitor applications from the System Center Configuration Manager console](https://docs.microsoft.com/sccm/apps/deploy-use/monitor-applications-from-the-console).</span></span>  

## <span data-ttu-id="99e2d-236">Experiência do usuário final</span><span class="sxs-lookup"><span data-stu-id="99e2d-236">End-user experience</span></span>  

<span data-ttu-id="99e2d-237">Os usuários com computadores gerenciados pelo Configuration Manager e que executam o Windows 10 da arquitetura de processador especificada verão uma mensagem informando que devem instalar o aplicativo Microsoft Edge Dev.</span><span class="sxs-lookup"><span data-stu-id="99e2d-237">Users who have PCs that are managed by Configuration Manager and are running Windows 10 of the specified processor architecture, will see a message telling them that they must install the Microsoft Edge Dev application.</span></span> <span data-ttu-id="99e2d-238">Ao aceitar essa opção de instalação, o aplicativo será instalado.</span><span class="sxs-lookup"><span data-stu-id="99e2d-238">When they accept this installation option, the application is installed.</span></span>  

## <span data-ttu-id="99e2d-239">Consulte também</span><span class="sxs-lookup"><span data-stu-id="99e2d-239">See also</span></span>

- [<span data-ttu-id="99e2d-240">Página de aterrissagem do Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="99e2d-240">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="99e2d-241">Criar e implantar um aplicativo com o System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="99e2d-241">Create and deploy an application with System Center Configuration Manager</span></span>](https://docs.microsoft.com/sccm/apps/get-started/create-and-deploy-an-application)
