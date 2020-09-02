---
title: Configurar o Microsoft Edge no macOS com Jamf
ms.author: brianalt
author: dan-wesley
manager: laurawi
ms.date: 02/20/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Definir as configurações de política do Microsoft Edge em dispositivos Mac com o Jamf
ms.openlocfilehash: 336bdfed2c53811615b0183dc5ca7db916cd7428
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10978978"
---
# <span data-ttu-id="f40e3-103">Definir as configurações de política do Microsoft Edge no macOS com o Jamf</span><span class="sxs-lookup"><span data-stu-id="f40e3-103">Configure Microsoft Edge policy settings on macOS with Jamf</span></span>

<span data-ttu-id="f40e3-104">Este artigo descreve como definir as configurações de política no macOS usando um arquivo de manifesto de política do Microsoft Edge no JAMF Pro 10,19.</span><span class="sxs-lookup"><span data-stu-id="f40e3-104">This article describes how to configure policy settings on macOS using a Microsoft Edge policy manifest file on Jamf Pro 10.19.</span></span>

<span data-ttu-id="f40e3-105">Você também pode definir as configurações de política do Microsoft Edge no macOS usando um arquivo de lista de propriedades (.plist).</span><span class="sxs-lookup"><span data-stu-id="f40e3-105">You can also configure Microsoft Edge policy settings on macOS by using a property list (.plist) file.</span></span> <span data-ttu-id="f40e3-106">Para saber mais, confira [Configurar para macOS usando um .plist](configure-microsoft-edge-on-mac.md)</span><span class="sxs-lookup"><span data-stu-id="f40e3-106">For more information, see [Configure for macOS using a .plist](configure-microsoft-edge-on-mac.md)</span></span>


## <span data-ttu-id="f40e3-107">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="f40e3-107">Prerequisites</span></span>

<span data-ttu-id="f40e3-108">É necessário o seguinte software:</span><span class="sxs-lookup"><span data-stu-id="f40e3-108">The following software is required:</span></span>

- <span data-ttu-id="f40e3-109">Canal Estável 81 do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="f40e3-109">Microsoft Edge Stable channel 81</span></span>
- <span data-ttu-id="f40e3-110">Arquivo de Modelos de Política, versão 81.0.416.3</span><span class="sxs-lookup"><span data-stu-id="f40e3-110">Policy Templates file, version 81.0.416.3</span></span>
- <span data-ttu-id="f40e3-111">Jamf Pro, Versão 10,19</span><span class="sxs-lookup"><span data-stu-id="f40e3-111">Jamf Pro, Version 10.19</span></span>

## <span data-ttu-id="f40e3-112">Sobre o aplicativo Jamf Pro e menu de Configurações Personalizadas</span><span class="sxs-lookup"><span data-stu-id="f40e3-112">About the Jamf Pro Application & Custom Settings menu</span></span>

<span data-ttu-id="f40e3-113">Antes do Jamf Pro 10.18, o gerenciamento do Office 365 envolvia a criação manual de um arquivo .plist.</span><span class="sxs-lookup"><span data-stu-id="f40e3-113">Before Jamf Pro 10.18, managing Office 365 involved manually building a .plist file.</span></span> <span data-ttu-id="f40e3-114">Esse era um fluxo de trabalho demorado que exigia uma forte experiência técnica.</span><span class="sxs-lookup"><span data-stu-id="f40e3-114">This was a time-consuming workflow that required a strong technical background.</span></span> <span data-ttu-id="f40e3-115">Jamf Pro 10,18 eliminou essas barreiras simplificando o processo de configuração.</span><span class="sxs-lookup"><span data-stu-id="f40e3-115">Jamf Pro 10.18 eliminated those barriers by streamlining the configuration process.</span></span> <span data-ttu-id="f40e3-116">No entanto, os Administradores de TI só poderiam usar essa nova interface de usuário para os aplicativos específicos e domínios de preferência especificados pelo Jamf.</span><span class="sxs-lookup"><span data-stu-id="f40e3-116">However, IT Admins could only use this new user interface for specific applications and preference domains specified by Jamf.</span></span>

<span data-ttu-id="f40e3-117">No Jamf Pro 10.19, um usuário pode fazer upload de um manifesto JSON como um "esquema personalizado" para direcionar qualquer domínio de preferência e a interface gráfica do usuário será gerada a partir desse manifesto.</span><span class="sxs-lookup"><span data-stu-id="f40e3-117">In Jamf Pro 10.19, a user can upload a JSON manifest as a "custom schema" to target any preference domain, and the graphical user interface will be generated from this manifest.</span></span> <span data-ttu-id="f40e3-118">O esquema personalizado que é criado acompanha a especificação de esquema JSON.</span><span class="sxs-lookup"><span data-stu-id="f40e3-118">The custom schema that's created follows the JSON Schema specification.</span></span>

<span data-ttu-id="f40e3-119">Para saber mais, confira [Perfis de Configuração do Computador](https://jamf.it/computer-configuration-profiles) no Guia do Administrador do Jamf Pro.</span><span class="sxs-lookup"><span data-stu-id="f40e3-119">For more information, see [Computer Configuration Profiles](https://jamf.it/computer-configuration-profiles) in the Jamf Pro Administrator's Guide.</span></span>

## <span data-ttu-id="f40e3-120">Obter o manifesto da política para uma versão específica do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="f40e3-120">Get the policy manifest for a specific version of Microsoft Edge</span></span>

<span data-ttu-id="f40e3-121">Para obter o manifesto de política:</span><span class="sxs-lookup"><span data-stu-id="f40e3-121">To get the policy manifest:</span></span>

- <span data-ttu-id="f40e3-122">Vá para a [página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise).</span><span class="sxs-lookup"><span data-stu-id="f40e3-122">Go to the [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise).</span></span>
- <span data-ttu-id="f40e3-123">Na lista suspensa de canal/versão, selecione \*\*qualquer canal com a versão 81 ou posterior.\*\*\*.</span><span class="sxs-lookup"><span data-stu-id="f40e3-123">On the Channel/Version dropdown list, select \*\*any channel with version 81 or later.\*\*\*.</span></span>
- <span data-ttu-id="f40e3-124">Na lista suspensa Build, selecione qualquer Build \*\*81 ou posterior.\*\*\*.</span><span class="sxs-lookup"><span data-stu-id="f40e3-124">On the Build dropdown list, select any \*\*81 build or later.\*\*\*.</span></span>
- <span data-ttu-id="f40e3-125">Clique em OBTER ARQUIVOS DE POLÍTICA para baixar nosso pacote de modelos de política.</span><span class="sxs-lookup"><span data-stu-id="f40e3-125">Click GET POLICY FILES to download our policy templates bundle.</span></span>

  > [!NOTE]
  > <span data-ttu-id="f40e3-126">Atualmente, o pacote de modelos de política é assinado como um arquivo Cab.</span><span class="sxs-lookup"><span data-stu-id="f40e3-126">Currently, the policy templates bundle is signed as a CAB file.</span></span> <span data-ttu-id="f40e3-127">Você precisará usar uma ferramenta de terceiros, como The Unarchiver, para abrir o arquivo no macOS.</span><span class="sxs-lookup"><span data-stu-id="f40e3-127">You'll need to use a 3rd party tool, such as The Unarchiver to open the file on macOS.</span></span>

<span data-ttu-id="f40e3-128">Depois de descompactar o arquivo CAB, descompacte o arquivo ZIP e navegue até o diretório de nível superior "mac".</span><span class="sxs-lookup"><span data-stu-id="f40e3-128">After you unpack the CAB file, unpack the ZIP file and navigate to the "mac" top level directory.</span></span> <span data-ttu-id="f40e3-129">O manifesto, chamado de "policy_manifest.json", está neste diretório.</span><span class="sxs-lookup"><span data-stu-id="f40e3-129">The manifest, which is named "policy_manifest.json", is in this directory.</span></span>

<span data-ttu-id="f40e3-130">Esse manifesto será publicado em todos os pacotes de política, começando com o build 81.0.416.3.</span><span class="sxs-lookup"><span data-stu-id="f40e3-130">This manifest will be published in every policy bundle starting with build 81.0.416.3.</span></span> <span data-ttu-id="f40e3-131">Se você deseja testar políticas no canal Dev, você pode pegar o manifesto associado a cada lançamento do Dev e testá-lo no Jamf Pro.</span><span class="sxs-lookup"><span data-stu-id="f40e3-131">If you want to test policies in the Dev channel, you can take the manifest associated with each Dev release and test it in Jamf Pro.</span></span>  

## <span data-ttu-id="f40e3-132">Usar o manifesto de política no Jamf Pro</span><span class="sxs-lookup"><span data-stu-id="f40e3-132">Use the policy manifest in Jamf Pro</span></span>

<span data-ttu-id="f40e3-133">Use as etapas a seguir para carregar o manifesto de política para o Jamf Pro e, em seguida, crie um perfil de política para o macOS.</span><span class="sxs-lookup"><span data-stu-id="f40e3-133">Use the following steps to upload the policy manifest to Jamf Pro and then create a policy profile for macOS.</span></span>

1. <span data-ttu-id="f40e3-134">Entre no Jamf.</span><span class="sxs-lookup"><span data-stu-id="f40e3-134">Sign in to Jamf.</span></span>
2. <span data-ttu-id="f40e3-135">Selecione a guia **Computador**.</span><span class="sxs-lookup"><span data-stu-id="f40e3-135">Select the **Computer** tab.</span></span>
3. <span data-ttu-id="f40e3-136">Em **Gerenciamento de Conteúdo**, selecione **Perfis de Configuração**.</span><span class="sxs-lookup"><span data-stu-id="f40e3-136">Under **Content Management**, select **Configuration Profiles**.</span></span>
4. <span data-ttu-id="f40e3-137">Na página **Perfis de Configuração**, clique em **+ Novo**.</span><span class="sxs-lookup"><span data-stu-id="f40e3-137">On the **Configuration Profiles** page, click **+ New**.</span></span>

   ![Adicionar um novo perfil no Jamf](media/configure-microsoft-edge-on-mac-jamf/configure-macos-jamf-configuration-profiles.png)

5. <span data-ttu-id="f40e3-139">Em **Novo Perfil de Configuração do macOS**>**Opções**, selecione **Aplicativo e Configurações Personalizadas**.</span><span class="sxs-lookup"><span data-stu-id="f40e3-139">On **New macOS Configuration Profile**>**Options**, select **Application & Custom Settings**.</span></span>
6. <span data-ttu-id="f40e3-140">Na janela pop-up **Aplicativo e Configurações Personalizadas**, clique em **Configurar**.</span><span class="sxs-lookup"><span data-stu-id="f40e3-140">On the **Application & Custom Settings** popup window, click **Configure**.</span></span>

   ![Definir Aplicativos e Configurações Personalizadas](media/configure-microsoft-edge-on-mac-jamf/configure-macos-jamf-app-and-custom.png)

7. <span data-ttu-id="f40e3-142">Na seção **Aplicativo e Configurações Personalizadas**, defina os valores mostrados na captura de tela a seguir.</span><span class="sxs-lookup"><span data-stu-id="f40e3-142">In the **Application & Custom Settings** section, set the values shown in the following screen shot.</span></span>

   ![Origem do perfil e esquema personalizado](media/configure-microsoft-edge-on-mac-jamf/configure-macos-jamf-app-and-custom-schema.png)

   - <span data-ttu-id="f40e3-144">Para **Método de Criação**, escolha **Definir configurações**.</span><span class="sxs-lookup"><span data-stu-id="f40e3-144">For **Creation Method**, pick **Configure settings**.</span></span>
   - <span data-ttu-id="f40e3-145">Para **Fonte**, escolha **Esquema Personalizado**.</span><span class="sxs-lookup"><span data-stu-id="f40e3-145">For **Source**, pick **Custom Schema**.</span></span>
   - <span data-ttu-id="f40e3-146">Para **Domínio de Preferência**, forneça o nome do seu domínio.</span><span class="sxs-lookup"><span data-stu-id="f40e3-146">For **Preference Domain**, provide the name of your domain.</span></span> <span data-ttu-id="f40e3-147">Este exemplo usa *com.microsoft.Edge* como o domínio.</span><span class="sxs-lookup"><span data-stu-id="f40e3-147">This example uses *com.microsoft.Edge* as the domain.</span></span>
   - <span data-ttu-id="f40e3-148">Para **Esquema Personalizado**, cole o conteúdo do arquivo de manifesto "policy_manifest.json".</span><span class="sxs-lookup"><span data-stu-id="f40e3-148">For **Custom Schema**, paste the contents of the "policy_manifest.json" manifest file.</span></span>
   - <span data-ttu-id="f40e3-149">Clique em **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="f40e3-149">Click **Save**.</span></span>

8. <span data-ttu-id="f40e3-150">Depois de salvar o perfil, Jamf exibe a seção **Geral** mostrada na próxima captura de tela.</span><span class="sxs-lookup"><span data-stu-id="f40e3-150">After you save the profile, Jamf displays the **General** section shown in the next screen shot.</span></span>

   ![Seção Configurar Geral](media/configure-microsoft-edge-on-mac-jamf/configure-macos-jamf-app-and-custom-general-setting.png)

   - <span data-ttu-id="f40e3-152">Forneça um **Nome** de exibição para o perfil e uma **Descrição**.</span><span class="sxs-lookup"><span data-stu-id="f40e3-152">Provide a display **Name** for the profile and a **Description**.</span></span>
   - <span data-ttu-id="f40e3-153">Mantenha a configuração padrão para **Categoria**, que é **Nenhuma**.</span><span class="sxs-lookup"><span data-stu-id="f40e3-153">Keep the default setting for **Category**, which is **None**.</span></span>
   - <span data-ttu-id="f40e3-154">Para o **Método de Distribuição**, as opções são **Instalar Automaticamente** ou **Disponibilizar no Autoatendiment**o.</span><span class="sxs-lookup"><span data-stu-id="f40e3-154">For **Distribution Method**, the options are **Install Automatically** or **Make Available in Self Service**.</span></span>
   - <span data-ttu-id="f40e3-155">Para **Nível**, as opções são **Nível do Usuário** ou **Nível do Computador**.</span><span class="sxs-lookup"><span data-stu-id="f40e3-155">For **Level**, the options are **User Level** or **Computer Level**.</span></span>
   - <span data-ttu-id="f40e3-156">Clique em **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="f40e3-156">Click **Save**.</span></span>

9. <span data-ttu-id="f40e3-157">Depois de salvar a seção Geral, Jamf mostra o perfil de configuração "Microsoft Edge Beta Channel" configurado para o nosso exemplo.</span><span class="sxs-lookup"><span data-stu-id="f40e3-157">After you save the General section, Jamf shows the "Microsoft Edge Beta Channel" configuration profile set up for our example.</span></span> <span data-ttu-id="f40e3-158">Na próxima captura de tela, observe que você pode continuar trabalhando no perfil clicando em **Editar** ou, se tiver terminado, clique em **Concluído**.</span><span class="sxs-lookup"><span data-stu-id="f40e3-158">In the next screen shot, note that you can keep working the profile by clicking **Edit** or if you're finished, click **Done**.</span></span>

   ![Novo perfil de configuração com opções](media/configure-microsoft-edge-on-mac-jamf/configure-macos-jamf-configuration-profiles-beta-channel.png)

   > [!NOTE]
   > <span data-ttu-id="f40e3-160">Você pode editar esse perfil depois que ele for salvo e em outra sessão do Jamf.</span><span class="sxs-lookup"><span data-stu-id="f40e3-160">You can edit this profile after it's been saved and in another Jamf session.</span></span> <span data-ttu-id="f40e3-161">Por exemplo, você pode decidir alterar o Método de Distribuição para Disponibilizar no Autoatendimento.</span><span class="sxs-lookup"><span data-stu-id="f40e3-161">For example, you might decide to change the Distribution Method to Make Available in Self Service.</span></span>

   <span data-ttu-id="f40e3-162">Para fazer uma edição de acompanhamento no Canal Estável do Microsoft Edge, ou excluí-lo, selecione o nome do perfil, mostrado na captura de tela Perfis de Configuração a seguir.</span><span class="sxs-lookup"><span data-stu-id="f40e3-162">To do a follow up edit on the Microsoft Edge Stable Channel, or delete it, select the profile name, shown in the following Configuration Profiles screen shot.</span></span>

   ![Lista de Perfis de Configuração](media/configure-microsoft-edge-on-mac-jamf/configure-macos-jamf-configuration-profiles-beta-channel-done.png)

<span data-ttu-id="f40e3-164">Depois de criar o novo perfil de configuração, você ainda terá que configurar o **Escopo** para o perfil.</span><span class="sxs-lookup"><span data-stu-id="f40e3-164">After you create the new configuration profile you still have to configure the **Scope** for the profile.</span></span>

### <span data-ttu-id="f40e3-165">Para configurar o escopo</span><span class="sxs-lookup"><span data-stu-id="f40e3-165">To configure the scope</span></span>

1. <span data-ttu-id="f40e3-166">Para **Destinos**, forneça as seguintes configurações mínimas:</span><span class="sxs-lookup"><span data-stu-id="f40e3-166">For **Targets**, provide the following minimum settings:</span></span>

   - <span data-ttu-id="f40e3-167">COMPUTADORES DE DESTINO.</span><span class="sxs-lookup"><span data-stu-id="f40e3-167">TARGET COMPUTERS.</span></span> <span data-ttu-id="f40e3-168">As opções são Computadores Específicos ou Todos os Computadores.</span><span class="sxs-lookup"><span data-stu-id="f40e3-168">The options are Specific Computers or All Computers.</span></span>
   - <span data-ttu-id="f40e3-169">USUÁRIOS DE DESTINO.</span><span class="sxs-lookup"><span data-stu-id="f40e3-169">TARGET USERS.</span></span> <span data-ttu-id="f40e3-170">As opções são Usuários Específicos ou Todos os Usuários.</span><span class="sxs-lookup"><span data-stu-id="f40e3-170">The options are Specific Users or All Users.</span></span>
   - <span data-ttu-id="f40e3-171">Clique em **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="f40e3-171">Click **Save**.</span></span>
2. <span data-ttu-id="f40e3-172">Para **Limitações**, mantenha a configuração padrão: Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="f40e3-172">For **Limitations**, keep the default setting: None.</span></span> <span data-ttu-id="f40e3-173">Clique em **Cancelar**.</span><span class="sxs-lookup"><span data-stu-id="f40e3-173">Click **Cancel**.</span></span>
3. <span data-ttu-id="f40e3-174">Para **Exclusões**, mantenha a configuração padrão: Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="f40e3-174">For **Exclusions**, keep the default setting: None.</span></span> <span data-ttu-id="f40e3-175">Clique em **Cancelar**.</span><span class="sxs-lookup"><span data-stu-id="f40e3-175">Click **Cancel**.</span></span>

## <span data-ttu-id="f40e3-176">Perguntas frequentes</span><span class="sxs-lookup"><span data-stu-id="f40e3-176">Frequently Asked Questions</span></span>

### <span data-ttu-id="f40e3-177">O Microsoft Edge pode ser configurado para usar as preferências mestres?</span><span class="sxs-lookup"><span data-stu-id="f40e3-177">Can Microsoft Edge be configured to use master preferences?</span></span>

<span data-ttu-id="f40e3-178">Sim, você pode configurar o Microsoft Edge para usar um arquivo de preferências mestre.</span><span class="sxs-lookup"><span data-stu-id="f40e3-178">Yes, you can configure Microsoft Edge to use a master preferences file.</span></span>

<span data-ttu-id="f40e3-179">Um arquivo de preferências mestre permite definir as configurações padrão para um perfil de usuário do navegador quando o Microsoft Edge for implantado.</span><span class="sxs-lookup"><span data-stu-id="f40e3-179">A master preferences file lets you configure default settings for a browser user profile when Microsoft Edge is deployed.</span></span> <span data-ttu-id="f40e3-180">Você também pode usar um arquivo de preferências mestre para aplicar configurações em computadores que não são gerenciados por um sistema de gerenciamento de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f40e3-180">You can also use a master preferences file to apply settings on computers that aren't managed by a device management system.</span></span> <span data-ttu-id="f40e3-181">Essas configurações são aplicadas ao perfil do usuário na primeira vez que o usuário executa o navegador.</span><span class="sxs-lookup"><span data-stu-id="f40e3-181">These settings are applied to the user’s profile the first time the user runs the browser.</span></span> <span data-ttu-id="f40e3-182">Depois que o usuário executar o navegador, as alterações feitas no arquivo de preferências mestre não serão aplicadas.</span><span class="sxs-lookup"><span data-stu-id="f40e3-182">After the user runs the browser, changes to the master preferences file aren’t applied.</span></span> <span data-ttu-id="f40e3-183">Um usuário pode alterar as configurações das preferências do mestre no navegador.</span><span class="sxs-lookup"><span data-stu-id="f40e3-183">A user can change settings from the master preferences in the browser.</span></span> <span data-ttu-id="f40e3-184">Se quiser fazer uma configuração obrigatória ou alterar uma configuração após a primeira execução do navegador, você deverá usar uma política.</span><span class="sxs-lookup"><span data-stu-id="f40e3-184">If you want to make a setting mandatory or change a setting after the first run of the browser, you must use a policy.</span></span>

<span data-ttu-id="f40e3-185">Um arquivo de preferências mestre permite que você personalize muitas configurações e preferências diferentes para o navegador, incluindo aquelas compartilhadas com outros navegadores baseados em Chromium e específicas do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="f40e3-185">A master preferences file lets you to customize many different settings and preferences for the browser, including those shared with other Chromium based browsers and specific to Microsoft Edge.</span></span>  <span data-ttu-id="f40e3-186">As preferências relacionadas à política podem ser configuradas usando o arquivo de preferências mestre.</span><span class="sxs-lookup"><span data-stu-id="f40e3-186">Policy related preferences can be configured using the master preferences file.</span></span> <span data-ttu-id="f40e3-187">Nos casos em que uma política é definida e há um conjunto de preferências do mestre correspondente, a configuração de política terá precedência.</span><span class="sxs-lookup"><span data-stu-id="f40e3-187">In cases where a policy is set and there’s a corresponding master preference set, the policy setting takes precedence.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f40e3-188">Todas as preferências disponíveis podem não ser consistentes com a terminologia e as convenções de nomenclatura do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="f40e3-188">All the available preferences might not be consistent with Microsoft Edge terminology and naming conventions.</span></span>  <span data-ttu-id="f40e3-189">Não há garantia de que essas preferências continuarão funcionando como esperado em versões futuras.</span><span class="sxs-lookup"><span data-stu-id="f40e3-189">There’s no guarantee that these preferences will continue to work as expected in future releases.</span></span> <span data-ttu-id="f40e3-190">As preferências podem ser alteradas ou ignoradas em versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="f40e3-190">Preferences might be changed or ignored in later versions.</span></span>

<span data-ttu-id="f40e3-191">Um arquivo de preferências mestre é um arquivo de texto formatado usando a marcação JSON.</span><span class="sxs-lookup"><span data-stu-id="f40e3-191">A master preferences file is a text file that’s formatted using JSON markup.</span></span> <span data-ttu-id="f40e3-192">Esse arquivo precisa ser adicionado ao mesmo diretório do que o executável msedge.exe.</span><span class="sxs-lookup"><span data-stu-id="f40e3-192">This file needs to be added to the same directory as the msedge.exe executable.</span></span> <span data-ttu-id="f40e3-193">Para implantações corporativas em todo o sistema no macOS,isso geralmente é: “*~/Library/Application Support/Microsoft/Microsoft Edge Master Preferences*" ou "*/Library/Microsoft/Microsoft Edge Master Preferences*”.</span><span class="sxs-lookup"><span data-stu-id="f40e3-193">For system wide enterprise deployments on macOS this is typically: “*~/Library/Application Support/Microsoft/Microsoft Edge Master Preferences*" or "*/Library/Microsoft/Microsoft Edge Master Preferences*”.</span></span>

## <span data-ttu-id="f40e3-194">Consulte também</span><span class="sxs-lookup"><span data-stu-id="f40e3-194">See also</span></span>

- [<span data-ttu-id="f40e3-195">Página de aterrissagem do Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="f40e3-195">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="f40e3-196">Configurar para macOS com Intune</span><span class="sxs-lookup"><span data-stu-id="f40e3-196">Configure for macOS with Intune</span></span>](configure-microsoft-edge-on-mac.md)
- [<span data-ttu-id="f40e3-197">Configurar para o Windows</span><span class="sxs-lookup"><span data-stu-id="f40e3-197">Configure for Windows</span></span>](configure-microsoft-edge.md)
- [<span data-ttu-id="f40e3-198">Configurar para o Windows com o Intune</span><span class="sxs-lookup"><span data-stu-id="f40e3-198">Configure for Windows with Intune</span></span>](configure-edge-with-intune.md)
