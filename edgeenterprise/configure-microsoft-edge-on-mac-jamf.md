---
title: Configurar o Microsoft Edge no macOS com Jamf
ms.author: brianalt
author: dan-wesley
manager: laurawi
ms.date: 11/30/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Definir as configurações de política do Microsoft Edge em dispositivos Mac com o Jamf
ms.openlocfilehash: 1859d9fb1fd3ea8ff6908c41f75df21a8b338769
ms.sourcegitcommit: ed6a5afabf909df87bec48671c4c47bcdfaeb7bc
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/02/2020
ms.locfileid: "11194709"
---
# <span data-ttu-id="7cb42-103">Definir as configurações de política do Microsoft Edge no macOS com o Jamf</span><span class="sxs-lookup"><span data-stu-id="7cb42-103">Configure Microsoft Edge policy settings on macOS with Jamf</span></span>

<span data-ttu-id="7cb42-104">Este artigo descreve como definir as configurações de política no macOS usando um arquivo de manifesto de política do Microsoft Edge no JAMF Pro 10,19.</span><span class="sxs-lookup"><span data-stu-id="7cb42-104">This article describes how to configure policy settings on macOS using a Microsoft Edge policy manifest file on Jamf Pro 10.19.</span></span>

<span data-ttu-id="7cb42-105">Você também pode definir as configurações de política do Microsoft Edge no macOS usando um arquivo de lista de propriedades (.plist).</span><span class="sxs-lookup"><span data-stu-id="7cb42-105">You can also configure Microsoft Edge policy settings on macOS by using a property list (.plist) file.</span></span> <span data-ttu-id="7cb42-106">Para saber mais, confira [Configurar para macOS usando um .plist](configure-microsoft-edge-on-mac.md)</span><span class="sxs-lookup"><span data-stu-id="7cb42-106">For more information, see [Configure for macOS using a .plist](configure-microsoft-edge-on-mac.md)</span></span>


## <span data-ttu-id="7cb42-107">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="7cb42-107">Prerequisites</span></span>

<span data-ttu-id="7cb42-108">É necessário o seguinte software:</span><span class="sxs-lookup"><span data-stu-id="7cb42-108">The following software is required:</span></span>

- <span data-ttu-id="7cb42-109">Canal Estável 81 do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="7cb42-109">Microsoft Edge Stable channel 81</span></span>
- <span data-ttu-id="7cb42-110">Arquivo de Modelos de Política, versão 81.0.416.3</span><span class="sxs-lookup"><span data-stu-id="7cb42-110">Policy Templates file, version 81.0.416.3</span></span>
- <span data-ttu-id="7cb42-111">Jamf Pro, Versão 10,19</span><span class="sxs-lookup"><span data-stu-id="7cb42-111">Jamf Pro, Version 10.19</span></span>

## <span data-ttu-id="7cb42-112">Sobre o aplicativo Jamf Pro e menu de Configurações Personalizadas</span><span class="sxs-lookup"><span data-stu-id="7cb42-112">About the Jamf Pro Application & Custom Settings menu</span></span>

<span data-ttu-id="7cb42-113">Antes do Jamf Pro 10.18, o gerenciamento do Office 365 envolvia a criação manual de um arquivo .plist.</span><span class="sxs-lookup"><span data-stu-id="7cb42-113">Before Jamf Pro 10.18, managing Office 365 involved manually building a .plist file.</span></span> <span data-ttu-id="7cb42-114">Esse era um fluxo de trabalho demorado que exigia uma forte experiência técnica.</span><span class="sxs-lookup"><span data-stu-id="7cb42-114">This was a time-consuming workflow that required a strong technical background.</span></span> <span data-ttu-id="7cb42-115">Jamf Pro 10,18 eliminou essas barreiras simplificando o processo de configuração.</span><span class="sxs-lookup"><span data-stu-id="7cb42-115">Jamf Pro 10.18 eliminated those barriers by streamlining the configuration process.</span></span> <span data-ttu-id="7cb42-116">No entanto, os Administradores de TI só poderiam usar essa nova interface de usuário para os aplicativos específicos e domínios de preferência especificados pelo Jamf.</span><span class="sxs-lookup"><span data-stu-id="7cb42-116">However, IT Admins could only use this new user interface for specific applications and preference domains specified by Jamf.</span></span>

<span data-ttu-id="7cb42-117">No Jamf Pro 10.19, um usuário pode fazer upload de um manifesto JSON como um "esquema personalizado" para direcionar qualquer domínio de preferência e a interface gráfica do usuário será gerada a partir desse manifesto.</span><span class="sxs-lookup"><span data-stu-id="7cb42-117">In Jamf Pro 10.19, a user can upload a JSON manifest as a "custom schema" to target any preference domain, and the graphical user interface will be generated from this manifest.</span></span> <span data-ttu-id="7cb42-118">O esquema personalizado que é criado acompanha a especificação de esquema JSON.</span><span class="sxs-lookup"><span data-stu-id="7cb42-118">The custom schema that's created follows the JSON Schema specification.</span></span>

<span data-ttu-id="7cb42-119">Para saber mais, confira [Perfis de Configuração do Computador](https://jamf.it/computer-configuration-profiles) no Guia do Administrador do Jamf Pro.</span><span class="sxs-lookup"><span data-stu-id="7cb42-119">For more information, see [Computer Configuration Profiles](https://jamf.it/computer-configuration-profiles) in the Jamf Pro Administrator's Guide.</span></span>

## <span data-ttu-id="7cb42-120">Obter o manifesto da política para uma versão específica do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="7cb42-120">Get the policy manifest for a specific version of Microsoft Edge</span></span>

<span data-ttu-id="7cb42-121">Para obter o manifesto de política:</span><span class="sxs-lookup"><span data-stu-id="7cb42-121">To get the policy manifest:</span></span>

- <span data-ttu-id="7cb42-122">Vá para a [página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise).</span><span class="sxs-lookup"><span data-stu-id="7cb42-122">Go to the [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise).</span></span>
- <span data-ttu-id="7cb42-123">Na lista suspensa Canal/Versão, selecione **qualquer canal com a versão 81 ou posterior.** _.</span><span class="sxs-lookup"><span data-stu-id="7cb42-123">On the Channel/Version dropdown list, select **any channel with version 81 or later.**_.</span></span>
- <span data-ttu-id="7cb42-124">Na lista suspensa de Build, selecione qualquer _ *compilação do 81 ou posterior.* \* _.</span><span class="sxs-lookup"><span data-stu-id="7cb42-124">On the Build dropdown list, select any _*81 build or later.*\*_.</span></span>
- <span data-ttu-id="7cb42-125">Clique em OBTER ARQUIVOS DE POLÍTICA para baixar nosso pacote de modelos de política.</span><span class="sxs-lookup"><span data-stu-id="7cb42-125">Click GET POLICY FILES to download our policy templates bundle.</span></span>

  > [!NOTE]
  > <span data-ttu-id="7cb42-126">Atualmente, o pacote de modelos de política é assinado como um arquivo Cab.</span><span class="sxs-lookup"><span data-stu-id="7cb42-126">Currently, the policy templates bundle is signed as a CAB file.</span></span> <span data-ttu-id="7cb42-127">Você precisará usar uma ferramenta de terceiros, como The Unarchiver, para abrir o arquivo no macOS.</span><span class="sxs-lookup"><span data-stu-id="7cb42-127">You'll need to use a 3rd party tool, such as The Unarchiver to open the file on macOS.</span></span>

<span data-ttu-id="7cb42-128">Depois de descompactar o arquivo CAB, descompacte o arquivo ZIP e navegue até o diretório de nível superior "mac".</span><span class="sxs-lookup"><span data-stu-id="7cb42-128">After you unpack the CAB file, unpack the ZIP file and navigate to the "mac" top level directory.</span></span> <span data-ttu-id="7cb42-129">O manifesto, chamado de "policy_manifest.json", está neste diretório.</span><span class="sxs-lookup"><span data-stu-id="7cb42-129">The manifest, which is named "policy_manifest.json", is in this directory.</span></span>

<span data-ttu-id="7cb42-130">Esse manifesto será publicado em todos os pacotes de política, começando com o build 81.0.416.3.</span><span class="sxs-lookup"><span data-stu-id="7cb42-130">This manifest will be published in every policy bundle starting with build 81.0.416.3.</span></span> <span data-ttu-id="7cb42-131">Se você deseja testar políticas no canal Dev, você pode pegar o manifesto associado a cada lançamento do Dev e testá-lo no Jamf Pro.</span><span class="sxs-lookup"><span data-stu-id="7cb42-131">If you want to test policies in the Dev channel, you can take the manifest associated with each Dev release and test it in Jamf Pro.</span></span>  

## <span data-ttu-id="7cb42-132">Usar o manifesto de política no Jamf Pro</span><span class="sxs-lookup"><span data-stu-id="7cb42-132">Use the policy manifest in Jamf Pro</span></span>

<span data-ttu-id="7cb42-133">Use as etapas a seguir para carregar o manifesto de política para o Jamf Pro e, em seguida, crie um perfil de política para o macOS.</span><span class="sxs-lookup"><span data-stu-id="7cb42-133">Use the following steps to upload the policy manifest to Jamf Pro and then create a policy profile for macOS.</span></span>

1. <span data-ttu-id="7cb42-134">Entre no Jamf.</span><span class="sxs-lookup"><span data-stu-id="7cb42-134">Sign in to Jamf.</span></span>
2. <span data-ttu-id="7cb42-135">Selecione a guia _\*computador\*\*.</span><span class="sxs-lookup"><span data-stu-id="7cb42-135">Select the _*Computer*\* tab.</span></span>
3. <span data-ttu-id="7cb42-136">Em **Gerenciamento de Conteúdo**, selecione **Perfis de Configuração**.</span><span class="sxs-lookup"><span data-stu-id="7cb42-136">Under **Content Management**, select **Configuration Profiles**.</span></span>
4. <span data-ttu-id="7cb42-137">Na página **Perfis de Configuração**, clique em **+ Novo**.</span><span class="sxs-lookup"><span data-stu-id="7cb42-137">On the **Configuration Profiles** page, click **+ New**.</span></span>

   ![Adicionar um novo perfil no Jamf](media/configure-microsoft-edge-on-mac-jamf/configure-macos-jamf-configuration-profiles.png)

5. <span data-ttu-id="7cb42-139">Em **Novo Perfil de Configuração do macOS**>**Opções**, selecione **Aplicativo e Configurações Personalizadas**.</span><span class="sxs-lookup"><span data-stu-id="7cb42-139">On **New macOS Configuration Profile**>**Options**, select **Application & Custom Settings**.</span></span>
6. <span data-ttu-id="7cb42-140">Na janela pop-up **Aplicativo e Configurações Personalizadas**, clique em **Configurar**.</span><span class="sxs-lookup"><span data-stu-id="7cb42-140">On the **Application & Custom Settings** popup window, click **Configure**.</span></span>

   ![Definir Aplicativos e Configurações Personalizadas](media/configure-microsoft-edge-on-mac-jamf/configure-macos-jamf-app-and-custom.png)

7. <span data-ttu-id="7cb42-142">Na seção **Aplicativo e Configurações Personalizadas**, defina os valores mostrados na captura de tela a seguir.</span><span class="sxs-lookup"><span data-stu-id="7cb42-142">In the **Application & Custom Settings** section, set the values shown in the following screen shot.</span></span>

   ![Origem do perfil e esquema personalizado](media/configure-microsoft-edge-on-mac-jamf/configure-macos-jamf-app-and-custom-schema.png)

   - <span data-ttu-id="7cb42-144">Para **Método de Criação**, escolha **Definir configurações**.</span><span class="sxs-lookup"><span data-stu-id="7cb42-144">For **Creation Method**, pick **Configure settings**.</span></span>
   - <span data-ttu-id="7cb42-145">Para **Fonte**, escolha **Esquema Personalizado**.</span><span class="sxs-lookup"><span data-stu-id="7cb42-145">For **Source**, pick **Custom Schema**.</span></span>
   - <span data-ttu-id="7cb42-146">Para **Domínio de Preferência**, forneça o nome do seu domínio.</span><span class="sxs-lookup"><span data-stu-id="7cb42-146">For **Preference Domain**, provide the name of your domain.</span></span> <span data-ttu-id="7cb42-147">Este exemplo usa *com.microsoft.Edge* como o domínio.</span><span class="sxs-lookup"><span data-stu-id="7cb42-147">This example uses *com.microsoft.Edge* as the domain.</span></span>
   - <span data-ttu-id="7cb42-148">Para **Esquema Personalizado**, cole o conteúdo do arquivo de manifesto "policy_manifest.json".</span><span class="sxs-lookup"><span data-stu-id="7cb42-148">For **Custom Schema**, paste the contents of the "policy_manifest.json" manifest file.</span></span>
   - <span data-ttu-id="7cb42-149">Clique em **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="7cb42-149">Click **Save**.</span></span>

8. <span data-ttu-id="7cb42-150">Depois de salvar o perfil, Jamf exibe a seção **Geral** mostrada na próxima captura de tela.</span><span class="sxs-lookup"><span data-stu-id="7cb42-150">After you save the profile, Jamf displays the **General** section shown in the next screen shot.</span></span>

   ![Seção Configurar Geral](media/configure-microsoft-edge-on-mac-jamf/configure-macos-jamf-app-and-custom-general-setting.png)

   - <span data-ttu-id="7cb42-152">Forneça um **Nome** de exibição para o perfil e uma **Descrição**.</span><span class="sxs-lookup"><span data-stu-id="7cb42-152">Provide a display **Name** for the profile and a **Description**.</span></span>
   - <span data-ttu-id="7cb42-153">Mantenha a configuração padrão para **Categoria**, que é **Nenhuma**.</span><span class="sxs-lookup"><span data-stu-id="7cb42-153">Keep the default setting for **Category**, which is **None**.</span></span>
   - <span data-ttu-id="7cb42-154">Para o **Método de Distribuição**, as opções são **Instalar Automaticamente** ou **Disponibilizar no Autoatendiment**o.</span><span class="sxs-lookup"><span data-stu-id="7cb42-154">For **Distribution Method**, the options are **Install Automatically** or **Make Available in Self Service**.</span></span>
   - <span data-ttu-id="7cb42-155">Para **Nível**, as opções são **Nível do Usuário** ou **Nível do Computador**.</span><span class="sxs-lookup"><span data-stu-id="7cb42-155">For **Level**, the options are **User Level** or **Computer Level**.</span></span>
   - <span data-ttu-id="7cb42-156">Clique em **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="7cb42-156">Click **Save**.</span></span>

9. <span data-ttu-id="7cb42-157">Depois de salvar a seção Geral, Jamf mostra o perfil de configuração "Microsoft Edge Beta Channel" configurado para o nosso exemplo.</span><span class="sxs-lookup"><span data-stu-id="7cb42-157">After you save the General section, Jamf shows the "Microsoft Edge Beta Channel" configuration profile set up for our example.</span></span> <span data-ttu-id="7cb42-158">Na próxima captura de tela, observe que você pode continuar trabalhando no perfil clicando em **Editar** ou, se tiver terminado, clique em **Concluído**.</span><span class="sxs-lookup"><span data-stu-id="7cb42-158">In the next screen shot, note that you can keep working the profile by clicking **Edit** or if you're finished, click **Done**.</span></span>

   ![Novo perfil de configuração com opções](media/configure-microsoft-edge-on-mac-jamf/configure-macos-jamf-configuration-profiles-beta-channel.png)

   > [!NOTE]
   > <span data-ttu-id="7cb42-160">Você pode editar esse perfil depois que ele for salvo e em outra sessão do Jamf.</span><span class="sxs-lookup"><span data-stu-id="7cb42-160">You can edit this profile after it's been saved and in another Jamf session.</span></span> <span data-ttu-id="7cb42-161">Por exemplo, você pode decidir alterar o Método de Distribuição para Disponibilizar no Autoatendimento.</span><span class="sxs-lookup"><span data-stu-id="7cb42-161">For example, you might decide to change the Distribution Method to Make Available in Self Service.</span></span>

   <span data-ttu-id="7cb42-162">Para fazer uma edição de acompanhamento no Canal Estável do Microsoft Edge, ou excluí-lo, selecione o nome do perfil, mostrado na captura de tela Perfis de Configuração a seguir.</span><span class="sxs-lookup"><span data-stu-id="7cb42-162">To do a follow up edit on the Microsoft Edge Stable Channel, or delete it, select the profile name, shown in the following Configuration Profiles screen shot.</span></span>

   ![Lista de Perfis de Configuração](media/configure-microsoft-edge-on-mac-jamf/configure-macos-jamf-configuration-profiles-beta-channel-done.png)

<span data-ttu-id="7cb42-164">Depois de criar o novo perfil de configuração, você ainda terá que configurar o **Escopo** para o perfil.</span><span class="sxs-lookup"><span data-stu-id="7cb42-164">After you create the new configuration profile you still have to configure the **Scope** for the profile.</span></span>

### <span data-ttu-id="7cb42-165">Para configurar o escopo</span><span class="sxs-lookup"><span data-stu-id="7cb42-165">To configure the scope</span></span>

1. <span data-ttu-id="7cb42-166">Para **Destinos**, forneça as seguintes configurações mínimas:</span><span class="sxs-lookup"><span data-stu-id="7cb42-166">For **Targets**, provide the following minimum settings:</span></span>

   - <span data-ttu-id="7cb42-167">COMPUTADORES DE DESTINO.</span><span class="sxs-lookup"><span data-stu-id="7cb42-167">TARGET COMPUTERS.</span></span> <span data-ttu-id="7cb42-168">As opções são Computadores Específicos ou Todos os Computadores.</span><span class="sxs-lookup"><span data-stu-id="7cb42-168">The options are Specific Computers or All Computers.</span></span>
   - <span data-ttu-id="7cb42-169">USUÁRIOS DE DESTINO.</span><span class="sxs-lookup"><span data-stu-id="7cb42-169">TARGET USERS.</span></span> <span data-ttu-id="7cb42-170">As opções são Usuários Específicos ou Todos os Usuários.</span><span class="sxs-lookup"><span data-stu-id="7cb42-170">The options are Specific Users or All Users.</span></span>
   - <span data-ttu-id="7cb42-171">Clique em **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="7cb42-171">Click **Save**.</span></span>
2. <span data-ttu-id="7cb42-172">Para **Limitações**, mantenha a configuração padrão: Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="7cb42-172">For **Limitations**, keep the default setting: None.</span></span> <span data-ttu-id="7cb42-173">Clique em **Cancelar**.</span><span class="sxs-lookup"><span data-stu-id="7cb42-173">Click **Cancel**.</span></span>
3. <span data-ttu-id="7cb42-174">Para **Exclusões**, mantenha a configuração padrão: Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="7cb42-174">For **Exclusions**, keep the default setting: None.</span></span> <span data-ttu-id="7cb42-175">Clique em **Cancelar**.</span><span class="sxs-lookup"><span data-stu-id="7cb42-175">Click **Cancel**.</span></span>

## <span data-ttu-id="7cb42-176">Confira também</span><span class="sxs-lookup"><span data-stu-id="7cb42-176">See also</span></span>

- [<span data-ttu-id="7cb42-177">Página de aterrissagem do Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="7cb42-177">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="7cb42-178">Configurar para macOS com Intune</span><span class="sxs-lookup"><span data-stu-id="7cb42-178">Configure for macOS with Intune</span></span>](configure-microsoft-edge-on-mac.md)
- [<span data-ttu-id="7cb42-179">Configurar para o Windows</span><span class="sxs-lookup"><span data-stu-id="7cb42-179">Configure for Windows</span></span>](configure-microsoft-edge.md)
- [<span data-ttu-id="7cb42-180">Configurar para o Windows com o Intune</span><span class="sxs-lookup"><span data-stu-id="7cb42-180">Configure for Windows with Intune</span></span>](configure-edge-with-intune.md)
