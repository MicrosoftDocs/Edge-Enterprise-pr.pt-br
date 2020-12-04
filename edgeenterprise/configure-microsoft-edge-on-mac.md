---
title: Configurar o Microsoft Edge para macOS usando um. plist
ms.author: brianalt
author: kelleyvice-msft
manager: laurawi
ms.date: 11/30/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Definir as configurações de política do Microsoft Edge no macOS usando .plist
ms.openlocfilehash: abe110ab3589cc9276f28590273ece2d372be3b8
ms.sourcegitcommit: ed6a5afabf909df87bec48671c4c47bcdfaeb7bc
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/02/2020
ms.locfileid: "11194679"
---
# <span data-ttu-id="4f709-103">Definir as configurações de política do Microsoft Edge no macOS usando .plist</span><span class="sxs-lookup"><span data-stu-id="4f709-103">Configure Microsoft Edge policy settings for macOS using a .plist</span></span>

<span data-ttu-id="4f709-104">Este artigo descreve como configurar o Microsoft Edge no macOS usando um arquivo de lista de propriedades (.plist).</span><span class="sxs-lookup"><span data-stu-id="4f709-104">This article describes how to configure Microsoft Edge on macOS using a property list (.plist) file.</span></span> <span data-ttu-id="4f709-105">Você aprenderá a criar esse arquivo e a implementá-lo no Microsoft Intune.</span><span class="sxs-lookup"><span data-stu-id="4f709-105">You'll learn how to create this file and then deploy it to Microsoft Intune.</span></span>

<span data-ttu-id="4f709-106">Para obter mais informações, consulte [About Information Property List Files](https://developer.apple.com/library/archive/documentation/General/Reference/InfoPlistKeyReference/Articles/AboutInformationPropertyListFiles.html) (site da Apple) e [Ajustes personalizados de payload](https://support.apple.com/guide/mdm/custom-mdm9abbdbe7/1/web/1).</span><span class="sxs-lookup"><span data-stu-id="4f709-106">For more information, see [About Information Property List Files](https://developer.apple.com/library/archive/documentation/General/Reference/InfoPlistKeyReference/Articles/AboutInformationPropertyListFiles.html) (Apple's website) and [Custom payload settings](https://support.apple.com/guide/mdm/custom-mdm9abbdbe7/1/web/1).</span></span>

> [!NOTE]
> <span data-ttu-id="4f709-107">Este artigo aplica-se ao Microsoft Edge versão 77 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="4f709-107">This article applies to Microsoft Edge version 77 or later.</span></span>

## <span data-ttu-id="4f709-108">Configurar políticas do Microsoft Edge no macOS</span><span class="sxs-lookup"><span data-stu-id="4f709-108">Configure Microsoft Edge policies on macOS</span></span>

<span data-ttu-id="4f709-109">A primeira etapa é criar seu plist.</span><span class="sxs-lookup"><span data-stu-id="4f709-109">The first step is to create your plist.</span></span> <span data-ttu-id="4f709-110">Você pode criar o arquivo plist com qualquer editor de texto ou pode usar o [Terminal para criar o perfil de configuração](#create-a-configuration-profile-using-terminal).</span><span class="sxs-lookup"><span data-stu-id="4f709-110">You can create the plist file with any text editor or you can use [Terminal to create the configuration profile](#create-a-configuration-profile-using-terminal).</span></span> <span data-ttu-id="4f709-111">No entanto, é mais fácil criar e editar um arquivo plist usando uma ferramenta que formate o código XML para você.</span><span class="sxs-lookup"><span data-stu-id="4f709-111">However, it's easier to create and edit a plist file using a tool that formats the XML code for you.</span></span> <span data-ttu-id="4f709-112">O *Xcode* é um ambiente de desenvolvimento integrado gratuito que você pode obter de um dos seguintes locais:</span><span class="sxs-lookup"><span data-stu-id="4f709-112">*Xcode* is a free integrated development environment that you can get from one of the following locations:</span></span>

- [<span data-ttu-id="4f709-113">Site para desenvolvedores da Apple</span><span class="sxs-lookup"><span data-stu-id="4f709-113">Apple developer website</span></span>](https://developer.apple.com/xcode/)
- [<span data-ttu-id="4f709-114">Mac App Store</span><span class="sxs-lookup"><span data-stu-id="4f709-114">Mac App Store</span></span>](https://apps.apple.com/app/xcode/id497799835?mt=12)

<span data-ttu-id="4f709-115">Para obter uma lista de políticas com suporte e seus nomes de teclas de preferência, consulte [Referência de políticas do navegador Microsoft Edge](microsoft-edge-policies.md).</span><span class="sxs-lookup"><span data-stu-id="4f709-115">For a list of supported policies and their preference key names, see [Microsoft Edge browser policies reference](microsoft-edge-policies.md).</span></span> <span data-ttu-id="4f709-116">No arquivo de modelos de política, que pode ser baixado da [página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise), há um plist de exemplo (*itadminexample.plist*) na pasta **examples**.</span><span class="sxs-lookup"><span data-stu-id="4f709-116">In the policy templates file, which can be downloaded from the [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise), there's an example plist (*itadminexample.plist*) in the **examples** folder.</span></span> <span data-ttu-id="4f709-117">O arquivo de exemplo contém todos os tipos de dados com suporte que você pode personalizar para definir suas configurações de política.</span><span class="sxs-lookup"><span data-stu-id="4f709-117">The example file contains all supported data types that you can customize to define your policy settings.</span></span> 

<span data-ttu-id="4f709-118">A próxima etapa depois que você criar o conteúdo de seu plist é nomeá-lo usando o domínio de preferência do Microsoft Edge, *com.microsoft.Edge*.</span><span class="sxs-lookup"><span data-stu-id="4f709-118">The next step after you create the contents of your plist, is to name it using the Microsoft Edge preference domain, *com.microsoft.Edge*.</span></span> <span data-ttu-id="4f709-119">O nome diferencia maiúsculas de minúsculas e não deve incluir o canal de destino, pois ele se aplica a todos os canais do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="4f709-119">The name is case sensitive and should not include the channel you are targeting because it applies to all Microsoft Edge channels.</span></span> <span data-ttu-id="4f709-120">O nome do arquivo plist deve ser **_com.microsoft.Edge.plist_**.</span><span class="sxs-lookup"><span data-stu-id="4f709-120">The plist file name must be **_com.microsoft.Edge.plist_**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4f709-121">A partir do build 78.0.249.2, todos os canais do Microsoft Edge no macOS serão lidos no domínio de preferência **com.microsoft.Edge**.</span><span class="sxs-lookup"><span data-stu-id="4f709-121">Starting with build 78.0.249.2, all Microsoft Edge channels on macOS read from the **com.microsoft.Edge** preference domain.</span></span> <span data-ttu-id="4f709-122">Todas as versões anteriores são lidas em um domínio específico de canal, como **com.microsoft.Edge.Dev** para o canal de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="4f709-122">All prior releases read from a channel specific domain, such as **com.microsoft.Edge.Dev** for Dev channel.</span></span>

<span data-ttu-id="4f709-123">A última etapa é implantar o plist nos dispositivos Mac dos seus usuários utilizando seu provedor MDM preferencial, como o Microsoft Intune.</span><span class="sxs-lookup"><span data-stu-id="4f709-123">The last step is to deploy your plist to your users' Mac devices using your preferred MDM provider, such as Microsoft Intune.</span></span> <span data-ttu-id="4f709-124">Para obter instruções, consulte [Implantar seu plist](#deploy-your-plist).</span><span class="sxs-lookup"><span data-stu-id="4f709-124">For instructions see [Deploy your plist](#deploy-your-plist).</span></span>

### <span data-ttu-id="4f709-125">Criar um perfil de configuração usando o Terminal</span><span class="sxs-lookup"><span data-stu-id="4f709-125">Create a configuration profile using Terminal</span></span>

1. <span data-ttu-id="4f709-126">No Terminal, use o seguinte comando para criar um plist para o Microsoft Edge em sua área de trabalho com suas configurações preferidas:</span><span class="sxs-lookup"><span data-stu-id="4f709-126">In Terminal, use the following command to create a plist for Microsoft Edge on your desktop with your preferred settings:</span></span>

   ```cmd
   /usr/bin/defaults write ~/Desktop/com.microsoft.Edge.plist RestoreOnStartup -int 1
   ```

2. <span data-ttu-id="4f709-127">Converta o plist de binários em formato de texto simples:</span><span class="sxs-lookup"><span data-stu-id="4f709-127">Convert the plist from binary to plain text format:</span></span>

   ```cmd
   /usr/bin/plutil -convert xml1 ~/Desktop/com.microsoft.Edge.plist
   ```

<span data-ttu-id="4f709-128">Depois de converter o arquivo, verifique se os dados da política estão corretos e se contêm as configurações desejadas para o perfil de configuração.</span><span class="sxs-lookup"><span data-stu-id="4f709-128">After converting the file verify that your policy data is correct and contains the settings you want for your configuration profile.</span></span>

> [!NOTE]
> <span data-ttu-id="4f709-129">Somente pares chave devem estar no conteúdo do arquivo plist ou xml.</span><span class="sxs-lookup"><span data-stu-id="4f709-129">Only key value pairs should be in the contents of the plist or xml file.</span></span> <span data-ttu-id="4f709-130">Antes de carregar o seu ficheiro no Intune, remova todos os \<plist> e \<dict> valores, assim como os cabeçalhos xml do seu ficheiro.</span><span class="sxs-lookup"><span data-stu-id="4f709-130">Prior to uploading your file into Intune remove all the \<plist> and \<dict> values, and xml headers from your file.</span></span> <span data-ttu-id="4f709-131">O arquivo deve conter apenas pares de chave/valor.</span><span class="sxs-lookup"><span data-stu-id="4f709-131">The file should only contain key value pairs.</span></span>

## <span data-ttu-id="4f709-132">Implantar seu plist</span><span class="sxs-lookup"><span data-stu-id="4f709-132">Deploy your plist</span></span>

<span data-ttu-id="4f709-133">Para o Microsoft Intune crie um novo perfil de configuração de dispositivo voltado para a plataforma do macOS e selecione o tipo de perfil *Arquivo de preferência*.</span><span class="sxs-lookup"><span data-stu-id="4f709-133">For Microsoft Intune create a new device configuration profile targeting the macOS platform and select the *Preference file* profile type.</span></span> <span data-ttu-id="4f709-134">Direcione **com.microsoft.Edge** como o nome de domínio de preferência e carregue seu plist.</span><span class="sxs-lookup"><span data-stu-id="4f709-134">Target **com.microsoft.Edge** as the preference domain name and upload your plist.</span></span> <span data-ttu-id="4f709-135">Para obter mais informações, consulte [Adicionar um arquivo de lista de propriedades a dispositivos macOS usando o Microsoft Intune](https://docs.microsoft.com/intune/configuration/preference-file-settings-macos).</span><span class="sxs-lookup"><span data-stu-id="4f709-135">For more information see [Add a property list file to macOS devices using Microsoft Intune](https://docs.microsoft.com/intune/configuration/preference-file-settings-macos).</span></span>

<span data-ttu-id="4f709-136">Para o Jamf, carregue o arquivo .plist como uma carga *Configurações personalizadas*.</span><span class="sxs-lookup"><span data-stu-id="4f709-136">For Jamf upload the .plist file as a *Custom Settings* payload.</span></span>

## <span data-ttu-id="4f709-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="4f709-137">See also</span></span>

- [<span data-ttu-id="4f709-138">Página de aterrissagem do Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="4f709-138">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="4f709-139">Configurar para macOS com Jamf</span><span class="sxs-lookup"><span data-stu-id="4f709-139">Configure for macOS with Jamf</span></span>](configure-microsoft-edge-on-mac-jamf.md)
- [<span data-ttu-id="4f709-140">Configurar para o Windows</span><span class="sxs-lookup"><span data-stu-id="4f709-140">Configure for Windows</span></span>](configure-microsoft-edge.md)
- [<span data-ttu-id="4f709-141">Configurar para o Windows com o Intune</span><span class="sxs-lookup"><span data-stu-id="4f709-141">Configure for Windows with Intune</span></span>](configure-edge-with-intune.md)
