---
title: Definir o Microsoft Edge como o navegador padrão no Windows e macOS
ms.author: brianalt
author: dan-wesley
manager: srugh
ms.date: 1/15/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Saiba como definir o Microsoft Edge como o navegador padrão.
ms.openlocfilehash: c8cc45e0fe42dcbbd828dd81ae568f141cda2985
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979022"
---
# <span data-ttu-id="d8024-103">Definir Microsoft Edge como o navegador padrão</span><span class="sxs-lookup"><span data-stu-id="d8024-103">Set Microsoft Edge as the default browser</span></span>

<span data-ttu-id="d8024-104">Este artigo explica como você pode definir o Microsoft Edge como o navegador padrão no Windows e macOS.</span><span class="sxs-lookup"><span data-stu-id="d8024-104">This article explains how you can set Microsoft Edge as the default browser on Windows and macOS.</span></span>

> [!NOTE]
> <span data-ttu-id="d8024-105">Este artigo aplica-se ao Microsoft Edge versão 77 ou posteriores no Windows 8 e no Windows 10.</span><span class="sxs-lookup"><span data-stu-id="d8024-105">This article applies to Microsoft Edge version 77 or later on Windows 8 and Windows 10.</span></span> <span data-ttu-id="d8024-106">Para o Windows 7 e o macOS, consulte a política [Definir o Microsoft Edge como navegador padrão](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultbrowsersettingenabled).</span><span class="sxs-lookup"><span data-stu-id="d8024-106">For Windows 7 and macOS, see the [Set Microsoft Edge as default browser](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultbrowsersettingenabled) policy.</span></span>

## <span data-ttu-id="d8024-107">Introdução</span><span class="sxs-lookup"><span data-stu-id="d8024-107">Introduction</span></span>

<span data-ttu-id="d8024-108">Você pode usar a Política de Grupo **Definir um arquivo de configuração de associações padrão** ou a configuração do Gerenciamento de Dispositivo Móvel [DefaultAssociationsConfiguration](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration) para definir o Microsoft Edge como o navegador padrão da sua organização.</span><span class="sxs-lookup"><span data-stu-id="d8024-108">You can use the **Set a default associations configuration file** Group Policy or the [DefaultAssociationsConfiguration](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration) Mobile Device Management setting to set Microsoft Edge as the default browser for your organization.</span></span>

<span data-ttu-id="d8024-109">Para definir o Microsoft Edge Estável como o navegador padrão para arquivos html, links http/https e arquivos PDF, use o seguinte exemplo de arquivo de associação de aplicativo:</span><span class="sxs-lookup"><span data-stu-id="d8024-109">To set Microsoft Edge Stable as the default browser for html files, http/https links, and PDF files use the following application association file example:</span></span>

```xml
<?xml version="1.0" encoding="UTF-8"?>
<DefaultAssociations> 
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgeHTM" Identifier=".html"/>
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgeHTM" Identifier=".htm"/>
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgeHTM" Identifier="http"/>
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgeHTM" Identifier="https"/>  
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgePDF" Identifier=".pdf"/>
</DefaultAssociations>
```

> [!NOTE]
> <span data-ttu-id="d8024-110">Para definir o Microsoft Edge Beta como o navegador padrão, defina **ApplicationName** como "Microsoft Edge Beta" e **ProgId** como "MSEdgeBHTML".</span><span class="sxs-lookup"><span data-stu-id="d8024-110">To set Microsoft Edge Beta as the default browser, set **ApplicationName** to "Microsoft Edge Beta" and **ProgId** to "MSEdgeBHTML".</span></span> <span data-ttu-id="d8024-111">Para definir o Microsoft Edge Dev como o navegador padrão, defina **ApplicationName** como "Microsoft Edge Dev" e **ProgId** como "MSEdgeDHTML".</span><span class="sxs-lookup"><span data-stu-id="d8024-111">To set Microsoft Edge Dev as the default browser, set **ApplicationName** to "Microsoft Edge Dev" and **ProgId** to "MSEdgeDHTML".</span></span>


> [!NOTE]
> <span data-ttu-id="d8024-112">As associações de arquivos padrão não serão aplicadas se o Microsoft Edge não estiver instalado no dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="d8024-112">The default file associations aren't applied if Microsoft Edge isn't installed on the target device.</span></span> <span data-ttu-id="d8024-113">Neste cenário, os usuários deverão selecionar seu aplicativo padrão ao abrirem um link ou um arquivo htm/html.</span><span class="sxs-lookup"><span data-stu-id="d8024-113">In this scenario, users are prompted to select their default application when they open a link or a htm/html file.</span></span>

## <span data-ttu-id="d8024-114">Definir o Microsoft Edge como o navegador padrão em dispositivos ingressados no domínio</span><span class="sxs-lookup"><span data-stu-id="d8024-114">Set Microsoft Edge as the default browser on domain-joined devices</span></span>

<span data-ttu-id="d8024-115">Você pode definir Microsoft Edge como o navegador padrão em dispositivos ingressados no domínio definindo a política de grupo **Definir um arquivo de configuração de associações padrão**.</span><span class="sxs-lookup"><span data-stu-id="d8024-115">You can set Microsoft Edge as the default browser on domain-joined devices by configuring the **Set a default associations configuration file** group policy.</span></span> <span data-ttu-id="d8024-116">Ativar essa política de grupo requer que você crie e armazene um arquivo de configuração de associações padrão.</span><span class="sxs-lookup"><span data-stu-id="d8024-116">Turning this group policy on requires you to create and store a default associations configuration file.</span></span> <span data-ttu-id="d8024-117">Esse arquivo é armazenado localmente ou em um compartilhamento de rede.</span><span class="sxs-lookup"><span data-stu-id="d8024-117">This file is stored locally or on a network share.</span></span> <span data-ttu-id="d8024-118">Para obter mais informações sobre como criar esse arquivo, consulte [Exportar ou importar associações de aplicativo padrão](https://docs.microsoft.com/windows-hardware/manufacture/desktop/export-or-import-default-application-associations).</span><span class="sxs-lookup"><span data-stu-id="d8024-118">For more information about creating this file, see [Export or Import Default Application Associations](https://docs.microsoft.com/windows-hardware/manufacture/desktop/export-or-import-default-application-associations).</span></span>

### <span data-ttu-id="d8024-119">Para configurar a política de grupo para um tipo de arquivo padrão e um arquivo de configuração de associações de protocolo:</span><span class="sxs-lookup"><span data-stu-id="d8024-119">To configure the group policy for a default file type and protocol associations configuration file:</span></span>

1. <span data-ttu-id="d8024-120">Abra o editor de Política de Grupo e vá para **Configuração do Computador\Modelos Administrativos\Componentes do Windows\Explorador de Arquivos**.</span><span class="sxs-lookup"><span data-stu-id="d8024-120">Open the Group Policy editor and go to the **Computer Configuration\Administrative Templates\Windows Components\File Explorer**.</span></span>
2. <span data-ttu-id="d8024-121">Selecione **Definir um arquivo de configuração de associações padrão**.</span><span class="sxs-lookup"><span data-stu-id="d8024-121">Select **Set a default associations configuration file**.</span></span>
3. <span data-ttu-id="d8024-122">Clique em **configuração de política** e em **Habilitado**.</span><span class="sxs-lookup"><span data-stu-id="d8024-122">Click **policy setting**, and then click **Enabled**.</span></span>
4. <span data-ttu-id="d8024-123">Em **Opções:**, digite o local do arquivo de configuração de associações padrão.</span><span class="sxs-lookup"><span data-stu-id="d8024-123">Under **Options:**, type the location to your default associations configuration file.</span></span>
5. <span data-ttu-id="d8024-124">Clique em **OK** para salvar as configurações da política.</span><span class="sxs-lookup"><span data-stu-id="d8024-124">Click **OK** to save the policy settings.</span></span>

<span data-ttu-id="d8024-125">O exemplo na próxima captura de tela mostra um arquivo de associações chamado *appassoc.xml* em um compartilhamento de rede que possa ser acessado do dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="d8024-125">The example in the next screenshot shows an associations file named *appassoc.xml* on a network share that is accessible from the target device.</span></span>

   ![Habilitar associação de arquivo na política de grupo](./media/edge-learnmore-make-edge-default-browser/edge-learnmore-app-associations.png)

   > [!NOTE]
   > <span data-ttu-id="d8024-127">Se essa configuração for habilitada e o dispositivo do usuário for ingressado em domínio, o arquivo de configuração de associações será processado na próxima vez que o usuário entrar.</span><span class="sxs-lookup"><span data-stu-id="d8024-127">If this setting is enabled and the user's device is domain-joined, the associations configuration file is processed the next time the user signs on.</span></span>

## <span data-ttu-id="d8024-128">Defina o Microsoft Edge como o navegador padrão em dispositivos ingressados no Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="d8024-128">Set Microsoft Edge as the default browser on Azure Active Directory joined devices</span></span>

<span data-ttu-id="d8024-129">Para definir o Microsoft Edge Beta como o navegador padrão em dispositivos ingressados no Azure Active Directory, siga as etapas da configuração do Gerenciamento de Dispositivo Móvel [DefaultAssociationsConfiguration](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration) usando o seguinte arquivo de associação de aplicativo como um exemplo.</span><span class="sxs-lookup"><span data-stu-id="d8024-129">To set Microsoft Edge as the default browser on Azure Active Directory joined devices follow the steps in the [DefaultAssociationsConfiguration](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration) Mobile Device Management setting using the following application association file as an example.</span></span>

```xml
<?xml version="1.0" encoding="UTF-8"?>
<DefaultAssociations>
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgeHTM" Identifier=".html"/>
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgeHTM" Identifier=".htm"/>
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgeHTM" Identifier="http"/>
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgeHTM" Identifier="https"/>  
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgePDF" Identifier=".pdf"/>
</DefaultAssociations>
```

> [!NOTE]
> <span data-ttu-id="d8024-130">Para definir o Microsoft Edge Beta como o navegador padrão, defina **ApplicationName** como "Microsoft Edge Beta" e **ProgId** como "MSEdgeBHTML".</span><span class="sxs-lookup"><span data-stu-id="d8024-130">To set Microsoft Edge Beta as the default browser, set **ApplicationName** to "Microsoft Edge Beta" and **ProgId** to "MSEdgeBHTML".</span></span> <span data-ttu-id="d8024-131">Para definir o Microsoft Edge Dev como o navegador padrão, defina **ApplicationName** como "Microsoft Edge Dev" e **ProgId** como "MSEdgeDHTML".</span><span class="sxs-lookup"><span data-stu-id="d8024-131">To set Microsoft Edge Dev as the default browser, set **ApplicationName** to "Microsoft Edge Dev" and **ProgId** to "MSEdgeDHTML".</span></span>

## <span data-ttu-id="d8024-132">Definir o Microsoft Edge como o navegador padrão no macOS</span><span class="sxs-lookup"><span data-stu-id="d8024-132">Set Microsoft Edge as the default browser on macOS</span></span>

<span data-ttu-id="d8024-133">A tentativa de definir o navegador padrão do macOS de forma programática faz com que um aviso apareça para o usuário final.</span><span class="sxs-lookup"><span data-stu-id="d8024-133">Attempting to programmatically set the default browser on macOS causes a prompt to appear for the end user.</span></span> <span data-ttu-id="d8024-134">Esse aviso é um recurso de segurança do macOS que só pode ser automatizado com o uso de um AppleScript.</span><span class="sxs-lookup"><span data-stu-id="d8024-134">This prompt is a macOS security feature that can only be automated away by using an AppleScript.</span></span>

<span data-ttu-id="d8024-135">Devido a essa limitação, há dois métodos principais para configurar Microsoft Edge como o navegador padrão no macOS.</span><span class="sxs-lookup"><span data-stu-id="d8024-135">Because of this limitation, there are two main methods for setting Microsoft Edge as the default browser on a macOS.</span></span> <span data-ttu-id="d8024-136">A primeira opção é atualizar o dispositivo com uma imagem do macOS em que o Microsoft Edge já foi definido como o navegador padrão.</span><span class="sxs-lookup"><span data-stu-id="d8024-136">The first option is to flash the device with an image of macOS where Microsoft Edge has already been set as the default browser.</span></span> <span data-ttu-id="d8024-137">A outra opção é usar a política [Definir o Microsoft Edge como navegador padrão](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultbrowsersettingenabled) , que solicita que o usuário defina o Microsoft Edge como navegador padrão.</span><span class="sxs-lookup"><span data-stu-id="d8024-137">The other option is to use the [Set Microsoft Edge as default browser](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultbrowsersettingenabled) policy, which prompts the user to set Microsoft Edge as the default browser.</span></span>

<span data-ttu-id="d8024-138">Ao usar um desses métodos, ainda é possível que um usuário altere o navegador padrão.</span><span class="sxs-lookup"><span data-stu-id="d8024-138">When using either of these methods, it is still possible for a user to change the default browser.</span></span> <span data-ttu-id="d8024-139">Isso ocorre porque, por motivos de segurança, a preferência de navegador padrão não pode ser bloqueada de forma programática.</span><span class="sxs-lookup"><span data-stu-id="d8024-139">This is because for security reasons, the default browser preference can’t be blocked programmatically.</span></span> <span data-ttu-id="d8024-140">Por esse motivo, recomendamos que você implante a política **Definir o Microsoft Edge como navegador padrão** , mesmo que você crie uma imagem com o Microsoft Edge como navegador padrão.</span><span class="sxs-lookup"><span data-stu-id="d8024-140">For this reason, we recommend that you deploy the **Set Microsoft Edge as default browser** policy even if you create an image with Microsoft Edge as the default browser.</span></span> <span data-ttu-id="d8024-141">Se a política for definida e o usuário remover o Microsoft Edge como navegador padrão, da próxima vez que ele abrir o Microsoft Edge, ele será solicitado a defini-lo como o padrão.</span><span class="sxs-lookup"><span data-stu-id="d8024-141">If the policy is set and a user changes the default browser from Microsoft Edge the next time they open Microsoft Edge, they will be prompted to set it as the default.</span></span>

## <span data-ttu-id="d8024-142">Consulte também</span><span class="sxs-lookup"><span data-stu-id="d8024-142">See also</span></span>

- [<span data-ttu-id="d8024-143">Planejar sua implantação do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="d8024-143">Plan your deployment of Microsoft Edge</span></span>](https://docs.microsoft.com/DeployEdge/deploy-edge-plan-deployment)
- [<span data-ttu-id="d8024-144">Página de aterrissagem do Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="d8024-144">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="d8024-145">Definir o Microsoft Edge como navegador padrão (Windows 7 e macOS)</span><span class="sxs-lookup"><span data-stu-id="d8024-145">Set Microsoft Edge as default browser (Windows 7 and macOS)</span></span>](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultbrowsersettingenabled)
- [<span data-ttu-id="d8024-146">Windows 10 – como configurar associações de arquivos para profissionais de TI?</span><span class="sxs-lookup"><span data-stu-id="d8024-146">Windows 10 – How to configure file associations for IT Pros?</span></span>](https://docs.microsoft.com/archive/blogs/windowsinternals/windows-10-how-to-configure-file-associations-for-it-pros)
- [<span data-ttu-id="d8024-147">Exportar ou importar associações de aplicativo padrão</span><span class="sxs-lookup"><span data-stu-id="d8024-147">Export or Import Default Application Associations</span></span>](https://docs.microsoft.com/windows-hardware/manufacture/desktop/export-or-import-default-application-associations)
  - [<span data-ttu-id="d8024-148">Visão geral do DISM</span><span class="sxs-lookup"><span data-stu-id="d8024-148">DISM Overview</span></span>](https://docs.microsoft.com/windows-hardware/manufacture/desktop/what-is-dism)
  - [<span data-ttu-id="d8024-149">DISM - Gerenciamento e Manutenção de Imagens de Implantação</span><span class="sxs-lookup"><span data-stu-id="d8024-149">DISM - Deployment Image Servicing and Management</span></span>](https://docs.microsoft.com/windows-hardware/manufacture/desktop/dism---deployment-image-servicing-and-management-technical-reference-for-windows)
