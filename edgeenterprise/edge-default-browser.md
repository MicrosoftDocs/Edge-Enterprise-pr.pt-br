---
title: Definir o Microsoft Edge como o navegador padrão no Windows e macOS
ms.author: brianalt
author: dan-wesley
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Saiba como definir o Microsoft Edge como o navegador padrão.
ms.openlocfilehash: 191d7835a0c4aacfc2fde409c57622ff5a351926
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/09/2021
ms.locfileid: "11641537"
---
# <a name="set-microsoft-edge-as-the-default-browser"></a><span data-ttu-id="d468e-103">Definir Microsoft Edge como o navegador padrão</span><span class="sxs-lookup"><span data-stu-id="d468e-103">Set Microsoft Edge as the default browser</span></span>

<span data-ttu-id="d468e-104">Este artigo explica como você pode definir o Microsoft Edge como o navegador padrão no Windows e macOS.</span><span class="sxs-lookup"><span data-stu-id="d468e-104">This article explains how you can set Microsoft Edge as the default browser on Windows and macOS.</span></span>

> [!NOTE]
> <span data-ttu-id="d468e-105">Este artigo aplica-se ao Microsoft Edge versão 77 ou posteriores no Windows 8 e no Windows 10.</span><span class="sxs-lookup"><span data-stu-id="d468e-105">This article applies to Microsoft Edge version 77 or later on Windows 8 and Windows 10.</span></span> <span data-ttu-id="d468e-106">Para o Windows 7 e o macOS, consulte a política [Definir o Microsoft Edge como navegador padrão](./microsoft-edge-policies.md#defaultbrowsersettingenabled).</span><span class="sxs-lookup"><span data-stu-id="d468e-106">For Windows 7 and macOS, see the [Set Microsoft Edge as default browser](./microsoft-edge-policies.md#defaultbrowsersettingenabled) policy.</span></span>

## <a name="introduction"></a><span data-ttu-id="d468e-107">Introdução</span><span class="sxs-lookup"><span data-stu-id="d468e-107">Introduction</span></span>

<span data-ttu-id="d468e-108">Você pode usar a Política de Grupo **Definir um arquivo de configuração de associações padrão** ou a configuração do Gerenciamento de Dispositivo Móvel [DefaultAssociationsConfiguration](/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration) para definir o Microsoft Edge como o navegador padrão da sua organização.</span><span class="sxs-lookup"><span data-stu-id="d468e-108">You can use the **Set a default associations configuration file** Group Policy or the [DefaultAssociationsConfiguration](/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration) Mobile Device Management setting to set Microsoft Edge as the default browser for your organization.</span></span>

<span data-ttu-id="d468e-109">Para definir o Microsoft Edge Estável como o navegador padrão para arquivos html, links http/https e arquivos PDF, use o seguinte exemplo de arquivo de associação de aplicativo:</span><span class="sxs-lookup"><span data-stu-id="d468e-109">To set Microsoft Edge Stable as the default browser for html files, http/https links, and PDF files use the following application association file example:</span></span>

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
> <span data-ttu-id="d468e-110">Para definir o Microsoft Edge Beta como o navegador padrão, defina **ApplicationName** como "Microsoft Edge Beta" e **ProgId** como "MSEdgeBHTML".</span><span class="sxs-lookup"><span data-stu-id="d468e-110">To set Microsoft Edge Beta as the default browser, set **ApplicationName** to "Microsoft Edge Beta" and **ProgId** to "MSEdgeBHTML".</span></span> <span data-ttu-id="d468e-111">Para definir o Microsoft Edge Dev como o navegador padrão, defina **ApplicationName** como "Microsoft Edge Dev" e **ProgId** como "MSEdgeDHTML".</span><span class="sxs-lookup"><span data-stu-id="d468e-111">To set Microsoft Edge Dev as the default browser, set **ApplicationName** to "Microsoft Edge Dev" and **ProgId** to "MSEdgeDHTML".</span></span>


> [!NOTE]
> <span data-ttu-id="d468e-112">As associações de arquivos padrão não serão aplicadas se o Microsoft Edge não estiver instalado no dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="d468e-112">The default file associations aren't applied if Microsoft Edge isn't installed on the target device.</span></span> <span data-ttu-id="d468e-113">Neste cenário, os usuários deverão selecionar seu aplicativo padrão ao abrirem um link ou um arquivo htm/html.</span><span class="sxs-lookup"><span data-stu-id="d468e-113">In this scenario, users are prompted to select their default application when they open a link or a htm/html file.</span></span>

## <a name="set-microsoft-edge-as-the-default-browser-on-domain-joined-devices"></a><span data-ttu-id="d468e-114">Definir o Microsoft Edge como o navegador padrão em dispositivos ingressados no domínio</span><span class="sxs-lookup"><span data-stu-id="d468e-114">Set Microsoft Edge as the default browser on domain-joined devices</span></span>

<span data-ttu-id="d468e-115">Você pode definir Microsoft Edge como o navegador padrão em dispositivos ingressados no domínio definindo a política de grupo **Definir um arquivo de configuração de associações padrão**.</span><span class="sxs-lookup"><span data-stu-id="d468e-115">You can set Microsoft Edge as the default browser on domain-joined devices by configuring the **Set a default associations configuration file** group policy.</span></span> <span data-ttu-id="d468e-116">Ativar essa política de grupo requer que você crie e armazene um arquivo de configuração de associações padrão.</span><span class="sxs-lookup"><span data-stu-id="d468e-116">Turning this group policy on requires you to create and store a default associations configuration file.</span></span> <span data-ttu-id="d468e-117">Esse arquivo é armazenado localmente ou em um compartilhamento de rede.</span><span class="sxs-lookup"><span data-stu-id="d468e-117">This file is stored locally or on a network share.</span></span> <span data-ttu-id="d468e-118">Para obter mais informações sobre como criar esse arquivo, consulte [Exportar ou importar associações de aplicativo padrão](/windows-hardware/manufacture/desktop/export-or-import-default-application-associations).</span><span class="sxs-lookup"><span data-stu-id="d468e-118">For more information about creating this file, see [Export or Import Default Application Associations](/windows-hardware/manufacture/desktop/export-or-import-default-application-associations).</span></span>

### <a name="to-configure-the-group-policy-for-a-default-file-type-and-protocol-associations-configuration-file"></a><span data-ttu-id="d468e-119">Para configurar a política de grupo para um tipo de arquivo padrão e um arquivo de configuração de associações de protocolo:</span><span class="sxs-lookup"><span data-stu-id="d468e-119">To configure the group policy for a default file type and protocol associations configuration file:</span></span>

1. <span data-ttu-id="d468e-120">Abra o editor de Política de Grupo e vá para **Configuração do Computador\Modelos Administrativos\Componentes do Windows\Explorador de Arquivos**.</span><span class="sxs-lookup"><span data-stu-id="d468e-120">Open the Group Policy editor and go to the **Computer Configuration\Administrative Templates\Windows Components\File Explorer**.</span></span>
2. <span data-ttu-id="d468e-121">Selecione **Definir um arquivo de configuração de associações padrão**.</span><span class="sxs-lookup"><span data-stu-id="d468e-121">Select **Set a default associations configuration file**.</span></span>
3. <span data-ttu-id="d468e-122">Clique em **configuração de política** e em **Habilitado**.</span><span class="sxs-lookup"><span data-stu-id="d468e-122">Click **policy setting**, and then click **Enabled**.</span></span>
4. <span data-ttu-id="d468e-123">Em **Opções:**, digite o local do arquivo de configuração de associações padrão.</span><span class="sxs-lookup"><span data-stu-id="d468e-123">Under **Options:**, type the location to your default associations configuration file.</span></span>
5. <span data-ttu-id="d468e-124">Clique em **OK** para salvar as configurações da política.</span><span class="sxs-lookup"><span data-stu-id="d468e-124">Click **OK** to save the policy settings.</span></span>

<span data-ttu-id="d468e-125">O exemplo na próxima captura de tela mostra um arquivo de associações chamado *appassoc.xml* em um compartilhamento de rede que possa ser acessado do dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="d468e-125">The example in the next screenshot shows an associations file named *appassoc.xml* on a network share that is accessible from the target device.</span></span>

   ![Habilitar associação de arquivo na política de grupo](./media/edge-learnmore-make-edge-default-browser/edge-learnmore-app-associations.png)

   > [!NOTE]
   > <span data-ttu-id="d468e-127">Se essa configuração for habilitada e o dispositivo do usuário for ingressado em domínio, o arquivo de configuração de associações será processado na próxima vez que o usuário entrar.</span><span class="sxs-lookup"><span data-stu-id="d468e-127">If this setting is enabled and the user's device is domain-joined, the associations configuration file is processed the next time the user signs on.</span></span>

## <a name="set-microsoft-edge-as-the-default-browser-on-azure-active-directory-joined-devices"></a><span data-ttu-id="d468e-128">Defina o Microsoft Edge como o navegador padrão em dispositivos ingressados no Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="d468e-128">Set Microsoft Edge as the default browser on Azure Active Directory joined devices</span></span>

<span data-ttu-id="d468e-129">Para definir o Microsoft Edge Beta como o navegador padrão em dispositivos ingressados no Azure Active Directory, siga as etapas da configuração do Gerenciamento de Dispositivo Móvel [DefaultAssociationsConfiguration](/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration) usando o seguinte arquivo de associação de aplicativo como um exemplo.</span><span class="sxs-lookup"><span data-stu-id="d468e-129">To set Microsoft Edge as the default browser on Azure Active Directory joined devices follow the steps in the [DefaultAssociationsConfiguration](/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration) Mobile Device Management setting using the following application association file as an example.</span></span>

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
> <span data-ttu-id="d468e-130">Para definir o Microsoft Edge Beta como o navegador padrão, defina **ApplicationName** como "Microsoft Edge Beta" e **ProgId** como "MSEdgeBHTML".</span><span class="sxs-lookup"><span data-stu-id="d468e-130">To set Microsoft Edge Beta as the default browser, set **ApplicationName** to "Microsoft Edge Beta" and **ProgId** to "MSEdgeBHTML".</span></span> <span data-ttu-id="d468e-131">Para definir o Microsoft Edge Dev como o navegador padrão, defina **ApplicationName** como "Microsoft Edge Dev" e **ProgId** como "MSEdgeDHTML".</span><span class="sxs-lookup"><span data-stu-id="d468e-131">To set Microsoft Edge Dev as the default browser, set **ApplicationName** to "Microsoft Edge Dev" and **ProgId** to "MSEdgeDHTML".</span></span>

## <a name="set-microsoft-edge-as-the-default-browser-on-macos"></a><span data-ttu-id="d468e-132">Definir o Microsoft Edge como o navegador padrão no macOS</span><span class="sxs-lookup"><span data-stu-id="d468e-132">Set Microsoft Edge as the default browser on macOS</span></span>

<span data-ttu-id="d468e-133">A tentativa de definir o navegador padrão do macOS de forma programática faz com que um aviso apareça para o usuário final.</span><span class="sxs-lookup"><span data-stu-id="d468e-133">Attempting to programmatically set the default browser on macOS causes a prompt to appear for the end user.</span></span> <span data-ttu-id="d468e-134">Esse aviso é um recurso de segurança do macOS que só pode ser automatizado com o uso de um AppleScript.</span><span class="sxs-lookup"><span data-stu-id="d468e-134">This prompt is a macOS security feature that can only be automated away by using an AppleScript.</span></span>

<span data-ttu-id="d468e-135">Devido a essa limitação, há dois métodos principais para configurar Microsoft Edge como o navegador padrão no macOS.</span><span class="sxs-lookup"><span data-stu-id="d468e-135">Because of this limitation, there are two main methods for setting Microsoft Edge as the default browser on a macOS.</span></span> <span data-ttu-id="d468e-136">A primeira opção é atualizar o dispositivo com uma imagem do macOS em que o Microsoft Edge já foi definido como o navegador padrão.</span><span class="sxs-lookup"><span data-stu-id="d468e-136">The first option is to flash the device with an image of macOS where Microsoft Edge has already been set as the default browser.</span></span> <span data-ttu-id="d468e-137">A outra opção é usar a política [Definir o Microsoft Edge como navegador padrão](./microsoft-edge-policies.md#defaultbrowsersettingenabled) , que solicita que o usuário defina o Microsoft Edge como navegador padrão.</span><span class="sxs-lookup"><span data-stu-id="d468e-137">The other option is to use the [Set Microsoft Edge as default browser](./microsoft-edge-policies.md#defaultbrowsersettingenabled) policy, which prompts the user to set Microsoft Edge as the default browser.</span></span>

<span data-ttu-id="d468e-138">Ao usar um desses métodos, ainda é possível que um usuário altere o navegador padrão.</span><span class="sxs-lookup"><span data-stu-id="d468e-138">When using either of these methods, it is still possible for a user to change the default browser.</span></span> <span data-ttu-id="d468e-139">Isso ocorre porque, por motivos de segurança, a preferência de navegador padrão não pode ser bloqueada de forma programática.</span><span class="sxs-lookup"><span data-stu-id="d468e-139">This is because for security reasons, the default browser preference can’t be blocked programmatically.</span></span> <span data-ttu-id="d468e-140">Por esse motivo, recomendamos que você implante a política **Definir o Microsoft Edge como navegador padrão** , mesmo que você crie uma imagem com o Microsoft Edge como navegador padrão.</span><span class="sxs-lookup"><span data-stu-id="d468e-140">For this reason, we recommend that you deploy the **Set Microsoft Edge as default browser** policy even if you create an image with Microsoft Edge as the default browser.</span></span> <span data-ttu-id="d468e-141">Se a política for definida e o usuário remover o Microsoft Edge como navegador padrão, da próxima vez que ele abrir o Microsoft Edge, ele será solicitado a defini-lo como o padrão.</span><span class="sxs-lookup"><span data-stu-id="d468e-141">If the policy is set and a user changes the default browser from Microsoft Edge the next time they open Microsoft Edge, they will be prompted to set it as the default.</span></span>

## <a name="see-also"></a><span data-ttu-id="d468e-142">Consulte também</span><span class="sxs-lookup"><span data-stu-id="d468e-142">See also</span></span>

- [<span data-ttu-id="d468e-143">Planejar sua implantação do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="d468e-143">Plan your deployment of Microsoft Edge</span></span>](./deploy-edge-plan-deployment.md)
- [<span data-ttu-id="d468e-144">Página de aterrissagem do Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="d468e-144">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="d468e-145">Definir o Microsoft Edge como navegador padrão (Windows 7 e macOS)</span><span class="sxs-lookup"><span data-stu-id="d468e-145">Set Microsoft Edge as default browser (Windows 7 and macOS)</span></span>](./microsoft-edge-policies.md#defaultbrowsersettingenabled)
- [<span data-ttu-id="d468e-146">Windows 10 – como configurar associações de arquivos para profissionais de TI?</span><span class="sxs-lookup"><span data-stu-id="d468e-146">Windows 10 – How to configure file associations for IT Pros?</span></span>](/archive/blogs/windowsinternals/windows-10-how-to-configure-file-associations-for-it-pros)
- [<span data-ttu-id="d468e-147">Exportar ou importar associações de aplicativo padrão</span><span class="sxs-lookup"><span data-stu-id="d468e-147">Export or Import Default Application Associations</span></span>](/windows-hardware/manufacture/desktop/export-or-import-default-application-associations)
  - [<span data-ttu-id="d468e-148">Visão geral do DISM</span><span class="sxs-lookup"><span data-stu-id="d468e-148">DISM Overview</span></span>](/windows-hardware/manufacture/desktop/what-is-dism)
  - [<span data-ttu-id="d468e-149">DISM - Gerenciamento e Manutenção de Imagens de Implantação</span><span class="sxs-lookup"><span data-stu-id="d468e-149">DISM - Deployment Image Servicing and Management</span></span>](/windows-hardware/manufacture/desktop/dism---deployment-image-servicing-and-management-technical-reference-for-windows)