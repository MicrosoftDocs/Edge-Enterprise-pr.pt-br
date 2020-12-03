---
title: Automatizar a implantação do Microsoft Edge para macOS com Jamf
ms.author: kvice
author: dan-wesley
manager: laurawi
ms.date: 11/30/2019
audience: ITPro
ms.topic: technical
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Como automatizar a implantação do Microsoft Edge para macOS com Jamf.
ms.openlocfilehash: 8639c0b7bf78bb8e22370dba29b592af73d8cb40
ms.sourcegitcommit: ed6a5afabf909df87bec48671c4c47bcdfaeb7bc
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/02/2020
ms.locfileid: "11194719"
---
# <span data-ttu-id="ac215-103">Implantar no macOS com Jamf</span><span class="sxs-lookup"><span data-stu-id="ac215-103">Deploy to macOS with Jamf</span></span>

<span data-ttu-id="ac215-104">Este artigo descreve como implantar o Microsoft Edge para macOS usando o Jamf.</span><span class="sxs-lookup"><span data-stu-id="ac215-104">This article describes how to deploy Microsoft Edge for macOS using Jamf.</span></span>

> [!NOTE]
> <span data-ttu-id="ac215-105">Este artigo aplica-se ao Microsoft Edge versão 77 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="ac215-105">This article applies to Microsoft Edge version 77 or later.</span></span>

## <span data-ttu-id="ac215-106">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="ac215-106">Prerequisites</span></span>

<span data-ttu-id="ac215-107">Antes de implantar Microsoft Edge, certifique-se de que você atenda aos seguintes pré-requisitos:</span><span class="sxs-lookup"><span data-stu-id="ac215-107">Before you deploy Microsoft Edge, make sure you meet the following prerequisites:</span></span>

- <span data-ttu-id="ac215-108">O arquivo de instalação do Microsoft Edge,  **MicrosoftEdgeDev-\<version\>.pkg** está em um local acessível em sua rede.</span><span class="sxs-lookup"><span data-stu-id="ac215-108">The Microsoft Edge installation file,  **MicrosoftEdgeDev-\<version\>.pkg** is in an accessible location on your network.</span></span> <span data-ttu-id="ac215-109">Você pode baixar os arquivos de instalação do Microsoft Edge Enterprise da [página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise).</span><span class="sxs-lookup"><span data-stu-id="ac215-109">You can download the Microsoft Edge Enterprise installation files from the [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise).</span></span>
- <span data-ttu-id="ac215-110">Você tem uma conta do Jamf Cloud com o nível de acesso e os privilégios necessários para criar e implantar arquivos de instalação em computadores.</span><span class="sxs-lookup"><span data-stu-id="ac215-110">You have a Jamf Cloud account with the level of access and privileges needed to create and deploy installation files to computers.</span></span>

## <span data-ttu-id="ac215-111">Para implantar o Microsoft Edge usando Jamf:</span><span class="sxs-lookup"><span data-stu-id="ac215-111">To deploy Microsoft Edge using Jamf:</span></span>

1. <span data-ttu-id="ac215-112">Entre no Jamf e vá para **Todas as Configurações**.</span><span class="sxs-lookup"><span data-stu-id="ac215-112">Sign on to Jamf and go to **All Settings**.</span></span>

    ![Abra Todas as Configurações](./media/mac-deploy/jamf-dash-main-open-settings.png)

2. <span data-ttu-id="ac215-114">Em **Todas as Configurações**, clique em **Gerenciamento do Computador**.</span><span class="sxs-lookup"><span data-stu-id="ac215-114">Under **All Settings**, click **Computer Management**.</span></span>

    ![Selecione Gerenciamento do Computador](./media/mac-deploy/jamf-all-settings-computer-mgmt.png)

3. <span data-ttu-id="ac215-116">Em **Gerenciamento do Computador**, clique em **Pacotes**.</span><span class="sxs-lookup"><span data-stu-id="ac215-116">Under **Computer Management**, click **Packages**.</span></span>

    ![Selecione Pacotes](./media/mac-deploy/jamf-all-settings-computer-mgmt-pkgs.png)

4. <span data-ttu-id="ac215-118">Na página **Pacotes**, clique em **+ Novo** para adicionar um novo pacote.</span><span class="sxs-lookup"><span data-stu-id="ac215-118">On the **Packages** page, click **+ New** to add a new package.</span></span>

    ![Selecione Novo para adicionar um novo pacote](./media/mac-deploy/jamf-all-settings-computer-mgmt-new-pkg.png)

5. <span data-ttu-id="ac215-120">Na página **Novo Pacote**, insira os detalhes sobre o pacote e clique em **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="ac215-120">On the **New Package** page, enter the details about the package and then click **Save**.</span></span> <span data-ttu-id="ac215-121">(Por exemplo, NOME DE EXIBIÇÃO, INFORMAÇÕES ou OBSERVAÇÕES.)</span><span class="sxs-lookup"><span data-stu-id="ac215-121">(For example, DISPLAY NAME, INFO, or NOTES.)</span></span>

    ![Selecione Salvar para salvar as informações do pacote](./media/mac-deploy/jamf-all-settings-computer-mgmt-save-pkg-info.png)

6. <span data-ttu-id="ac215-123">Selecione **Computadores** na barra de menus e, em seguida, selecione **Políticas** na barra de navegação.</span><span class="sxs-lookup"><span data-stu-id="ac215-123">Select **Computers** on the menu bar, and then select **Policies** in the navigation bar.</span></span>

7. <span data-ttu-id="ac215-124">Selecione **+ Novo** para exibir o painel **Nova Política**.</span><span class="sxs-lookup"><span data-stu-id="ac215-124">Select **+ New** to display the **New Policy** pane.</span></span>

    ![Selecione Novo para criar uma nova política](./media/mac-deploy/jamf-all-settings-computer-new-policy.png)

8. <span data-ttu-id="ac215-126">Na guia **Opções**, selecione **Geral**.</span><span class="sxs-lookup"><span data-stu-id="ac215-126">On the **Options** tab, select **General**.</span></span>

    - <span data-ttu-id="ac215-127">Em **NOME DE EXIBIÇÃO**, insira o nome de exibição da política.</span><span class="sxs-lookup"><span data-stu-id="ac215-127">Under **DISPLAY NAME**, enter the display name for the policy.</span></span>
    - <span data-ttu-id="ac215-128">Em **Gatilho**, selecione o evento que vai disparar a política.</span><span class="sxs-lookup"><span data-stu-id="ac215-128">Under **Trigger**, select the event that will trigger the policy.</span></span> <span data-ttu-id="ac215-129">(No exemplo a seguir, o evento é Inicialização.)</span><span class="sxs-lookup"><span data-stu-id="ac215-129">(In the following example, the event is Startup.)</span></span>

    ![Insira informações sobre a implantação](./media/mac-deploy/jamf-all-settings-computer-cfg-policy.png)

9. <span data-ttu-id="ac215-131">Na guia **Opções**, clique em **Pacotes**.</span><span class="sxs-lookup"><span data-stu-id="ac215-131">On the **Options** tab, click **Packages**.</span></span>

10. <span data-ttu-id="ac215-132">No pop-up **Configurar Pacotes**, clique em **Configurar**.</span><span class="sxs-lookup"><span data-stu-id="ac215-132">On the **Configure Packages** popup, click **Configure**.</span></span>

    ![Configure o pacote](./media/mac-deploy/jamf-all-settings-computer-policy-pkg-configure.png)

11. <span data-ttu-id="ac215-134">O pacote que você adicionou é mostrado no painel **Pacotes**.</span><span class="sxs-lookup"><span data-stu-id="ac215-134">The package that you added shows on the **Packages** pane.</span></span> <span data-ttu-id="ac215-135">Clique em **Adicionar**.</span><span class="sxs-lookup"><span data-stu-id="ac215-135">Click **Add**.</span></span> <span data-ttu-id="ac215-136">Neste exemplo, o pacote é "MicrosoftEdgeBeta" na captura de tela a seguir.</span><span class="sxs-lookup"><span data-stu-id="ac215-136">For this example, the package is "MicrosoftEdgeBeta" in the following screenshot.</span></span>

    ![Adicione o pacote](./media/mac-deploy/jamf-all-settings-computer-policy-pkg-add-beta.png)

12. <span data-ttu-id="ac215-138">Na página **Nova Política**, use as listas suspensas para selecionar **PONTO DE DISTRIBUIÇÃO** e **AÇÃO** a ser tomada para a política.</span><span class="sxs-lookup"><span data-stu-id="ac215-138">On the **New Policy** page, uUse the drop-down lists to select the **DISTRIBUTION POINT** and **ACTION** to take for the policy.</span></span> <span data-ttu-id="ac215-139">Clique em **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="ac215-139">Click **Save**.</span></span> <span data-ttu-id="ac215-140">A captura de tela a seguir usa "Ponto de distribuição padrão de cada computador" e "Instalar" como exemplo.</span><span class="sxs-lookup"><span data-stu-id="ac215-140">The following screenshot uses "Each computer's default distribution point" and "Install" as an example.</span></span>

    ![Selecione ponto de distribuição e ação](./media/mac-deploy/jamf-all-settings-computer-mgmt-pkg-cfg-distro.png)

13. <span data-ttu-id="ac215-142">Na página **Nova Política**, selecione a guia **Escopo**. Você pode gerenciar o escopo da implantação com base em computadores ou usuários.</span><span class="sxs-lookup"><span data-stu-id="ac215-142">On the **New Policy** page, select the **Scope** tab. You can manage the scope of the deployment based on computers or users.</span></span> <span data-ttu-id="ac215-143">Neste exemplo, selecione **Todos os Computadores** na lista suspensa **COMPUTADORES DE DESTINO** e clique em **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="ac215-143">For this example, select **All Computers** from the **TARGET COMPUTERS** drop-down list and then click **Save**.</span></span>

    ![Selecione o escopo da implantação](./media/mac-deploy/jamf-all-settings-computer-mgmt-add-target.png)

14. <span data-ttu-id="ac215-145">Neste ponto, você pode revisar a política de implantação do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ac215-145">At this point you can review the Microsoft Edge deployment policy.</span></span> <span data-ttu-id="ac215-146">Se as opções de implantação atenderem aos seus requisitos, clique em **Concluído**.</span><span class="sxs-lookup"><span data-stu-id="ac215-146">If the deployment options meet your requirements, click **Done**.</span></span>

    ![Clique em concluído](./media/mac-deploy/jamf-all-settings-computer-mgmt-finish-add-deployment.png)

    > [!NOTE]
    > <span data-ttu-id="ac215-148">Você pode retornar a uma política de implantação a qualquer momento para alterar as configurações.</span><span class="sxs-lookup"><span data-stu-id="ac215-148">You can return to a deployment policy at any time to change settings.</span></span>

<span data-ttu-id="ac215-149">Parabéns!</span><span class="sxs-lookup"><span data-stu-id="ac215-149">Congratulations!</span></span> <span data-ttu-id="ac215-150">Você acabou de configurar o Jamf para implantar o Microsoft Edge para macOS.</span><span class="sxs-lookup"><span data-stu-id="ac215-150">You’ve just finished configuring Jamf to deploy Microsoft Edge for macOS.</span></span> <span data-ttu-id="ac215-151">Quando a condição de gatilho que você definiu for verdadeira, o pacote será implantado nos computadores especificados.</span><span class="sxs-lookup"><span data-stu-id="ac215-151">When the trigger condition you defined is true, the package will get deployed to the computers you specified.</span></span>

## <span data-ttu-id="ac215-152">Consulte também</span><span class="sxs-lookup"><span data-stu-id="ac215-152">See also</span></span>

- [<span data-ttu-id="ac215-153">Página de aterrissagem do Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="ac215-153">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="ac215-154">Jamf.com</span><span class="sxs-lookup"><span data-stu-id="ac215-154">Jamf.com</span></span>](https://www.jamf.com/)
- [<span data-ttu-id="ac215-155">Integrar o Jamf ao Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="ac215-155">Integrate Jamf with Microsoft Intune</span></span>](https://docs.microsoft.com/intune/conditional-access-integrate-jamf)
