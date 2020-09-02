---
title: Usar o Microsoft Edge para se proteger contra aplicativos potencialmente indesejados
ms.author: kvice
author: dan-wesley
manager: srugh
ms.date: 03/04/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Usar o Microsoft Edge para se proteger contra aplicativos potencialmente indesejados
ms.openlocfilehash: 615442acc0e9ed58da37aa0ef8b3747e916a8024
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10978975"
---
# <span data-ttu-id="0dca4-103">Proteger-se contra aplicativos potencialmente indesejados (PUAs)</span><span class="sxs-lookup"><span data-stu-id="0dca4-103">Protect against potentially unwanted applications (PUAs)</span></span>

<span data-ttu-id="0dca4-104">Este artigo explica como você pode se proteger contra aplicativos potencialmente indesejados (PUAs) usando o Microsoft Edge ou o Windows Defender Antivirus.</span><span class="sxs-lookup"><span data-stu-id="0dca4-104">This article explains how you can protect against potentially unwanted applications (PUAs) using Microsoft Edge or by using Windows Defender Antivirus.</span></span>

> [!NOTE]
> <span data-ttu-id="0dca4-105">Este artigo se aplica ao Microsoft Edge versão 80 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="0dca4-105">This article applies to Microsoft Edge version 80 or later.</span></span>

## <span data-ttu-id="0dca4-106">Visão geral</span><span class="sxs-lookup"><span data-stu-id="0dca4-106">Overview</span></span>

<span data-ttu-id="0dca4-107">Aplicativos potencialmente indesejados não são considerados vírus ou malware, mas eles podem executar ações em pontos de extremidade que afetem negativamente o desempenho ou o uso do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="0dca4-107">Potentially unwanted applications aren't considered to be viruses or malware, but these apps might perform actions on endpoints that adversely affect endpoint performance or use.</span></span> <span data-ttu-id="0dca4-108">Por exemplo, o *software Evasion* tenta ativamente escapar a detecção por produtos de segurança.</span><span class="sxs-lookup"><span data-stu-id="0dca4-108">For example, *Evasion software* actively tries to evade detection by security products.</span></span> <span data-ttu-id="0dca4-109">Esse tipo de software pode aumentar o risco de sua rede ser infectada com malware real.</span><span class="sxs-lookup"><span data-stu-id="0dca4-109">This kind of software can increase the risk of your network being infected with actual malware.</span></span> <span data-ttu-id="0dca4-110">PUA também pode se referir aos aplicativos cuja reputação é considerada ruim.</span><span class="sxs-lookup"><span data-stu-id="0dca4-110">PUA can also refer to applications that are considered to have poor reputation.</span></span>

<span data-ttu-id="0dca4-111">Para obter uma descrição dos critérios usados para a classificação de software como PUA, confira [Aplicativos potencialmente indesejados](https://docs.microsoft.com/windows/security/threat-protection/intelligence/criteria#potentially-unwanted-application-pua).</span><span class="sxs-lookup"><span data-stu-id="0dca4-111">For a description of the criteria used to classify software as a PUA, see [Potentially unwanted application](https://docs.microsoft.com/windows/security/threat-protection/intelligence/criteria#potentially-unwanted-application-pua).</span></span>

## <span data-ttu-id="0dca4-112">Proteger-se contra PUA com o Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="0dca4-112">Protect against PUA with Microsoft Edge</span></span>

<span data-ttu-id="0dca4-113">O Microsoft Edge (versão 80.0.361.50 ou posterior) bloqueia downloads PUA e URLs de recursos associadas.</span><span class="sxs-lookup"><span data-stu-id="0dca4-113">Microsoft Edge (version 80.0.361.50 or later) blocks PUA downloads and associated resource URLs.</span></span>

<span data-ttu-id="0dca4-114">Para configurar a proteção, habilite o recurso **bloquear aplicativos potencialmente indesejados** no Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="0dca4-114">You can set up protection by enabling the **Block potentially unwanted apps** feature in Microsoft Edge.</span></span>

> [!NOTE]
> <span data-ttu-id="0dca4-115">A [postagem no blog da equipe do Microsoft Edge](https://blogs.windows.com/msedgedev/2020/02/27/protecting-users-potentially-unwanted-apps/) descreve esse novo recurso e explica como tratar um aplicativo rotulado incorretamente ou relatar um aplicativo como indesejado.</span><span class="sxs-lookup"><span data-stu-id="0dca4-115">The [Microsoft Edge Team blog post](https://blogs.windows.com/msedgedev/2020/02/27/protecting-users-potentially-unwanted-apps/) describes this new feature and explains how to handle a mislabeled app or report an app as unwanted.</span></span>

### <span data-ttu-id="0dca4-116">Para habilitar proteção contra PUA:</span><span class="sxs-lookup"><span data-stu-id="0dca4-116">To enable PUA protection:</span></span>

1. <span data-ttu-id="0dca4-117">Abra as **Configurações** no navegador.</span><span class="sxs-lookup"><span data-stu-id="0dca4-117">Open **Settings** in the browser.</span></span>
2. <span data-ttu-id="0dca4-118">Selecione **Privacidade e serviços**.</span><span class="sxs-lookup"><span data-stu-id="0dca4-118">Select **Privacy and services**.</span></span>
3. <span data-ttu-id="0dca4-119">Na seção **Serviços**, verifique se o **Microsoft Defender SmartScreen** está ativado.</span><span class="sxs-lookup"><span data-stu-id="0dca4-119">In the **Services** section, check to see that **Microsoft Defender SmartScreen** is turned on.</span></span> <span data-ttu-id="0dca4-120">Caso contrário, ative o Microsoft Defender SmartScreen.</span><span class="sxs-lookup"><span data-stu-id="0dca4-120">If not, then turn on Microsoft Defender SmartScreen.</span></span> <span data-ttu-id="0dca4-121">O exemplo na captura de tela a seguir mostra que o navegador é gerenciado pela organização e que o Microsoft Defender SmartScreen está ativado.</span><span class="sxs-lookup"><span data-stu-id="0dca4-121">The example in the following screenshot shows the browser is managed by the organization and that Microsoft Defender SmartScreen is turned on.</span></span>

   ![Ativar o Microsoft Edge PUA nas Configurações](./media/microsoft-edge-potentially-unwanted-apps/security-pua-setup.png)

4. <span data-ttu-id="0dca4-123">Na seção **Serviços**, use o botão de alternância mostrado na captura de tela anterior para ativar **Bloquear aplicativos potencialmente indesejados**.</span><span class="sxs-lookup"><span data-stu-id="0dca4-123">In the **Services** section, use the toggle shown in the preceding screenshot to turn on **Block potentially unwanted apps**.</span></span>

   > [!TIP]
   > <span data-ttu-id="0dca4-124">Você pode explorar com segurança o recurso de bloqueio de URL da proteção contra PUA, testando-o em uma das nossas páginas de demonstração do [Windows Defender SmartScreen](https://demo.smartscreen.msft.net/).</span><span class="sxs-lookup"><span data-stu-id="0dca4-124">You can safely explore the URL-blocking feature of PUA protection by testing it out on one of our Windows Defender SmartScreen [demo pages](https://demo.smartscreen.msft.net/).</span></span>

<span data-ttu-id="0dca4-125">Quando o Microsoft Edge detectar um PUA, você verá uma mensagem como a exibida na próxima captura de tela.</span><span class="sxs-lookup"><span data-stu-id="0dca4-125">When Microsoft Edge detects a PUA, you will see a message like the one in the next screenshot.</span></span>

   ![Mensagem de aviso do Microsoft Edge PUA](./media/microsoft-edge-potentially-unwanted-apps/security-pua-msg.png)

### <span data-ttu-id="0dca4-127">Para bloquear contra URLs associadas a PUA</span><span class="sxs-lookup"><span data-stu-id="0dca4-127">To block against PUA-associated URLs</span></span>

<span data-ttu-id="0dca4-128">Depois de ativar a proteção contra PUA no Microsoft Edge, o Windows Defender SmartScreen protegerá você contra URLs associadas a PUA.</span><span class="sxs-lookup"><span data-stu-id="0dca4-128">After you turn on PUA protection in Microsoft Edge, Windows Defender SmartScreen will protect you from PUA-associated URLs.</span></span>

<span data-ttu-id="0dca4-129">Há várias maneiras de os administradores configurarem como o Microsoft Edge e o Windows Defender SmartScreen funcionam em conjunto para proteger os usuários contra URLs associadas a PUA.</span><span class="sxs-lookup"><span data-stu-id="0dca4-129">There are several ways admins can configure how Microsoft Edge and Windows Defender SmartScreen work together to protect users from PUA-associated URLs.</span></span> <span data-ttu-id="0dca4-130">Para obter mais informações, consulte:</span><span class="sxs-lookup"><span data-stu-id="0dca4-130">For more information, see:</span></span>

- [<span data-ttu-id="0dca4-131">Definir configurações de política do Microsoft Edge no Windows</span><span class="sxs-lookup"><span data-stu-id="0dca4-131">Configure Microsoft Edge policy settings on Windows</span></span>](https://docs.microsoft.com/DeployEdge/configure-microsoft-edge)
- [<span data-ttu-id="0dca4-132">Configurações do SmartScreen</span><span class="sxs-lookup"><span data-stu-id="0dca4-132">SmartScreen settings</span></span>](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#smartscreen-settings)
- [<span data-ttu-id="0dca4-133">Política SmartScreenPuaEnabled</span><span class="sxs-lookup"><span data-stu-id="0dca4-133">SmartScreenPuaEnabled policy</span></span>](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#smartscreenpuaenabled)
- [<span data-ttu-id="0dca4-134">Configurar o Windows Defender SmartScreen</span><span class="sxs-lookup"><span data-stu-id="0dca4-134">Configure Windows Defender SmartScreen</span></span>](https://docs.microsoft.com/microsoft-edge/deploy/available-policies?source=docs#configure-windows-defender-smartscreen)

<span data-ttu-id="0dca4-135">Os administradores também podem personalizar a lista de bloqueios da Proteção Avançada contra Ameaças do Microsoft Defender (Microsoft Defender ATP).</span><span class="sxs-lookup"><span data-stu-id="0dca4-135">Admins can also customize the Microsoft Defender Advanced Threat Protection (Microsoft Defender ATP) block list.</span></span> <span data-ttu-id="0dca4-136">Eles podem usar o portal do Microsoft Defender ATP para [criar e gerenciar indicadores de IPs e URLs](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/manage-indicators#create-indicators-for-ips-and-urlsdomains-preview).</span><span class="sxs-lookup"><span data-stu-id="0dca4-136">They can use the Microsoft Defender ATP portal to [create and manage indicators for IPs and URLs](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/manage-indicators#create-indicators-for-ips-and-urlsdomains-preview).</span></span>

## <span data-ttu-id="0dca4-137">Proteger-se contra PUA com o Windows Defender Antivirus</span><span class="sxs-lookup"><span data-stu-id="0dca4-137">Protect against PUA with Windows Defender Antivirus</span></span>

<span data-ttu-id="0dca4-138">O artigo [Detectar e bloquear aplicativos potencialmente indesejados](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-antivirus/detect-block-potentially-unwanted-apps-windows-defender-antivirus#windows-defender-antivirus) também descreve como você pode configurar o Windows Defender Antivirus para habilitar a proteção contra PUA.</span><span class="sxs-lookup"><span data-stu-id="0dca4-138">The [Detect and block potentially unwanted applications](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-antivirus/detect-block-potentially-unwanted-apps-windows-defender-antivirus#windows-defender-antivirus) article also describes how you can configure Windows Defender Antivirus to enable PUA protection.</span></span> <span data-ttu-id="0dca4-139">Você pode configurar a proteção usando qualquer uma das seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="0dca4-139">You can configure protection using any of the following options:</span></span>

- [<span data-ttu-id="0dca4-140">Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="0dca4-140">Microsoft Intune</span></span>](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-antivirus/detect-block-potentially-unwanted-apps-windows-defender-antivirus#use-intune-to-configure-pua-protection)
- [<span data-ttu-id="0dca4-141">Microsoft Endpoint Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="0dca4-141">Microsoft Endpoint Configuration Manager</span></span>](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-antivirus/detect-block-potentially-unwanted-apps-windows-defender-antivirus#use-configuration-manager-to-configure-pua-protection)
- [<span data-ttu-id="0dca4-142">Política de Grupo</span><span class="sxs-lookup"><span data-stu-id="0dca4-142">Group Policy</span></span>](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-antivirus/detect-block-potentially-unwanted-apps-windows-defender-antivirus#use-group-policy-to-configure-pua-protection)
- [<span data-ttu-id="0dca4-143">Cmdlets do PowerShell</span><span class="sxs-lookup"><span data-stu-id="0dca4-143">PowerShell cmdlets</span></span>](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-antivirus/detect-block-potentially-unwanted-apps-windows-defender-antivirus#use-powershell-cmdlets-to-configure-pua-protection)

<span data-ttu-id="0dca4-144">Quando o Windows Defender detecta um arquivo PUA em um ponto de extremidade, ele coloca o arquivo em quarentena e notifica o usuário ([ a menos que as notificações estejam desabilitadas](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-antivirus/configure-notifications-windows-defender-antivirus)) no mesmo formato da detecção de ameaças normal (precedido de "PUA:"). As ameaças detectadas também aparecem na [lista de quarentena no aplicativo de Segurança do Windows](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-antivirus/windows-defender-security-center-antivirus#detection-history).</span><span class="sxs-lookup"><span data-stu-id="0dca4-144">When Windows Defender detects a PUA file on an endpoint it quarantines the file and notifies the user ([unless notifications are disabled](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-antivirus/configure-notifications-windows-defender-antivirus)) in the same format as a normal threat detection (prefaced with "PUA:".) Detected threats also appear in the [quarantine list in the Windows Security app](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-antivirus/windows-defender-security-center-antivirus#detection-history).</span></span>

### <span data-ttu-id="0dca4-145">Notificações e eventos PUA</span><span class="sxs-lookup"><span data-stu-id="0dca4-145">PUA notifications and events</span></span>

<span data-ttu-id="0dca4-146">Há várias maneiras de um administrador ver eventos PUA:</span><span class="sxs-lookup"><span data-stu-id="0dca4-146">There are several ways an admin can see PUA events:</span></span>

- <span data-ttu-id="0dca4-147">No Visualizador de Eventos do Windows, mas não no Microsoft Endpoint Configuration Manager ou no Intune.</span><span class="sxs-lookup"><span data-stu-id="0dca4-147">In the Windows Event Viewer, but not in Microsoft Endpoint Configuration Manager or Intune.</span></span>
- <span data-ttu-id="0dca4-148">Em um email, se as notificações de email para detecção de PUA estiverem ativadas.</span><span class="sxs-lookup"><span data-stu-id="0dca4-148">In an email if email notifications for PUA detections is turned on.</span></span>
- <span data-ttu-id="0dca4-149">Nos logs de eventos do[ Windows Defender Antivirus](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-antivirus/troubleshoot-windows-defender-antivirus), em que um evento PUA é registrado sob o ID de evento 1116 com a mensagem: "A plataforma antimalware detectou malware ou outro software potencialmente indesejado."</span><span class="sxs-lookup"><span data-stu-id="0dca4-149">In [Windows Defender Antivirus](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-antivirus/troubleshoot-windows-defender-antivirus) event logs, where a PUA event is recorded under event ID 1116 with the message: "The antimalware platform detected malware or other potentially unwanted software."</span></span>

> [!NOTE]
> <span data-ttu-id="0dca4-150">Os usuários verão "\*.exe foi bloqueado como um aplicativo potencialmente indesejado pelo Microsoft defender SmartScreen".</span><span class="sxs-lookup"><span data-stu-id="0dca4-150">Users will see "\*.exe has been blocked as a potentially unwanted app by Microsoft Defender SmartScreen".</span></span>

### <span data-ttu-id="0dca4-151">Incluir um aplicativo na lista de permissões</span><span class="sxs-lookup"><span data-stu-id="0dca4-151">Allow-list an app</span></span>

<span data-ttu-id="0dca4-152">Assim como o Microsoft Edge, o Windows Defender Antivirus oferece uma maneira de permitir arquivos bloqueados por engano ou que sejam necessários para concluir uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="0dca4-152">Like Microsoft Edge, Windows Defender Antivirus provides a way to allow files that are blocked by mistake or needed to complete a task.</span></span> <span data-ttu-id="0dca4-153">Se isso acontecer, você pode incluir um arquivo na lista de permissões.</span><span class="sxs-lookup"><span data-stu-id="0dca4-153">If this happens you can allow-list a file.</span></span> <span data-ttu-id="0dca4-154">Para obter mais informações, confira [como configurar a Endpoint Protection no Configuration Manager](https://docs.microsoft.com/previous-versions/system-center/system-center-2012-R2/hh508770(v=technet.10)#to-exclude-specific-files-or-folders) para saber como excluir arquivos ou pastas específicas.</span><span class="sxs-lookup"><span data-stu-id="0dca4-154">For more information, see [How to Configure Endpoint Protection in Configuration Manager](https://docs.microsoft.com/previous-versions/system-center/system-center-2012-R2/hh508770(v=technet.10)#to-exclude-specific-files-or-folders) to learn how to exclude specific files or folders.</span></span>

## <span data-ttu-id="0dca4-155">Consulte também</span><span class="sxs-lookup"><span data-stu-id="0dca4-155">See also</span></span>

- [<span data-ttu-id="0dca4-156">Página de aterrissagem do Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="0dca4-156">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="0dca4-157">Proteção contra ameaças</span><span class="sxs-lookup"><span data-stu-id="0dca4-157">Threat protection</span></span>](https://docs.microsoft.com/windows/security/threat-protection/index)
- [<span data-ttu-id="0dca4-158">Configurar a proteção comportamental, heurística e em tempo real</span><span class="sxs-lookup"><span data-stu-id="0dca4-158">Configure behavioral, heuristic, and real-time protection</span></span>](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-antivirus/configure-protection-features-windows-defender-antivirus)
- [<span data-ttu-id="0dca4-159">Proteção de próxima geração</span><span class="sxs-lookup"><span data-stu-id="0dca4-159">Next-generation protection</span></span>](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-antivirus/windows-defender-antivirus-in-windows-10)
- [<span data-ttu-id="0dca4-160">Linha de base de segurança para o Microsoft Edge baseado em Chromium, versão 79</span><span class="sxs-lookup"><span data-stu-id="0dca4-160">Security baseline for Chromium-based Microsoft Edge, version 79</span></span>](https://techcommunity.microsoft.com/t5/microsoft-security-baselines/security-baseline-final-for-chromium-based-microsoft-edge/ba-p/1111863)
