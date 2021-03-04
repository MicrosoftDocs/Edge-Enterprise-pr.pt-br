---
title: Desabilitar o Internet Explorer 11
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 03/02/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Aprenda a desabilitar o Internet Explorer 11 e usar o modo Internet Explorer no Microsoft Edge.
ms.openlocfilehash: 08d1fe48bfc4614710f4a341a285048194a64794
ms.sourcegitcommit: 928714329d0b11575494f557498f69a8417a3289
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "11385321"
---
# <a name="disable-internet-explorer-11"></a><span data-ttu-id="a8f47-103">Desabilitar o Internet Explorer 11</span><span class="sxs-lookup"><span data-stu-id="a8f47-103">Disable Internet Explorer 11</span></span>

<span data-ttu-id="a8f47-104">Este artigo descreve como desabilitar o Internet Explorer 11 como um navegador autônomo em seu ambiente.</span><span class="sxs-lookup"><span data-stu-id="a8f47-104">This article describes how to disable Internet Explorer 11 as a standalone browser in your environment.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="a8f47-105">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="a8f47-105">Prerequisites</span></span>

<span data-ttu-id="a8f47-106">As seguintes atualizações do Windows e do software Microsoft Edge são necessárias:</span><span class="sxs-lookup"><span data-stu-id="a8f47-106">The following Windows updates and Microsoft Edge software are required:</span></span>

- <span data-ttu-id="a8f47-107">Atualizações do Windows</span><span class="sxs-lookup"><span data-stu-id="a8f47-107">Windows updates</span></span>

  - <span data-ttu-id="a8f47-108">Windows 10, versão 2004, Windows Server versão 2004, Windows 10, versão 20H2: [KB4598291](https://support.microsoft.com/topic/february-2-2021-kb4598291-os-builds-19041-789-and-19042-789-preview-6a766199-a4f1-616e-1f5c-58bdc3ca5e3b) ou mais tarde</span><span class="sxs-lookup"><span data-stu-id="a8f47-108">Windows 10, version 2004, Windows Server version 2004, Windows 10, version 20H2: [KB4598291](https://support.microsoft.com/topic/february-2-2021-kb4598291-os-builds-19041-789-and-19042-789-preview-6a766199-a4f1-616e-1f5c-58bdc3ca5e3b) or later</span></span>
  - <span data-ttu-id="a8f47-109">Windows 10 versão 1909, Windows Server versão 1909: [KB4598298](https://support.microsoft.com/topic/january-21-2021-kb4598298-os-build-18363-1350-preview-02dfd9ba-91a2-1b82-dede-42f288c02511) ou mais tarde</span><span class="sxs-lookup"><span data-stu-id="a8f47-109">Windows 10 version 1909, Windows Server version 1909: [KB4598298](https://support.microsoft.com/topic/january-21-2021-kb4598298-os-build-18363-1350-preview-02dfd9ba-91a2-1b82-dede-42f288c02511) or later</span></span>
  - <span data-ttu-id="a8f47-110">Windows 10 versão 1809, Windows Server versão 1809, e Windows Server 2019: [KB4598296](https://support.microsoft.com/topic/january-21-2021-kb4598296-os-build-17763-1728-preview-4c0931ff-45b7-ff59-5e00-c03b5afb363d) ou mais tarde</span><span class="sxs-lookup"><span data-stu-id="a8f47-110">Windows 10 version 1809, Windows Server version 1809, and Windows Server 2019: [KB4598296](https://support.microsoft.com/topic/january-21-2021-kb4598296-os-build-17763-1728-preview-4c0931ff-45b7-ff59-5e00-c03b5afb363d) or later</span></span>
  - <span data-ttu-id="a8f47-111">Windows 10, versão 1607, Windows Server 2016: [KB4601318](https://support.microsoft.com/topic/february-9-2021-kb4601318-os-build-14393-4225-c5e3de6c-e3e6-ffb5-6197-48b9ce16446e) ou mais tarde</span><span class="sxs-lookup"><span data-stu-id="a8f47-111">Windows 10, version 1607, Windows Server 2016: [KB4601318](https://support.microsoft.com/topic/february-9-2021-kb4601318-os-build-14393-4225-c5e3de6c-e3e6-ffb5-6197-48b9ce16446e) or later</span></span>
   - <span data-ttu-id="a8f47-112">Windows 10 versão inicial (Julho 2015): [KB4601331](https://support.microsoft.com/office/february-9-2021%e2%80%94kb4601331-os-build-10240-18842-6227d078-fef3-8d67-27e0-1882e6cb79ff?ui=en-US&rs=en-US&ad=US) ou mais tarde</span><span class="sxs-lookup"><span data-stu-id="a8f47-112">Windows 10 initial version (July 2015): [KB4601331](https://support.microsoft.com/office/february-9-2021%e2%80%94kb4601331-os-build-10240-18842-6227d078-fef3-8d67-27e0-1882e6cb79ff?ui=en-US&rs=en-US&ad=US) or later</span></span>
  - <span data-ttu-id="a8f47-113">Windows 8.1: [KB4601384](https://support.microsoft.com/topic/february-9-2021-kb4601384-monthly-rollup-16bdbb75-dd4b-2910-abc5-7891c9756b96) ou mais tarde</span><span class="sxs-lookup"><span data-stu-id="a8f47-113">Windows 8.1: [KB4601384](https://support.microsoft.com/topic/february-9-2021-kb4601384-monthly-rollup-16bdbb75-dd4b-2910-abc5-7891c9756b96) or later</span></span>
  - <span data-ttu-id="a8f47-114">Windows Server 2012: [KB4601348](https://support.microsoft.com/topic/february-9-2021-kb4601348-monthly-rollup-2c338c0c-73d6-fb80-cc91-f1a86e80db0c) ou mais tarde</span><span class="sxs-lookup"><span data-stu-id="a8f47-114">Windows Server 2012: [KB4601348](https://support.microsoft.com/topic/february-9-2021-kb4601348-monthly-rollup-2c338c0c-73d6-fb80-cc91-f1a86e80db0c) or later</span></span>
  
- <span data-ttu-id="a8f47-115">Canal Estável do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="a8f47-115">Microsoft Edge Stable Channel</span></span>


## <a name="overview"></a><span data-ttu-id="a8f47-116">Visão geral</span><span class="sxs-lookup"><span data-stu-id="a8f47-116">Overview</span></span>

<span data-ttu-id="a8f47-117">Para organizações que exigem o Internet Explorer 11 (IE11) para compatibilidade herdada, o modo Internet Explorer (modo IE) no Microsoft Edge oferece uma experiência de navegador único e contínua.</span><span class="sxs-lookup"><span data-stu-id="a8f47-117">For organizations that require Internet Explorer 11 (IE11) for legacy compatibility, Internet Explorer mode (IE mode) on Microsoft Edge provides a seamless, single browser experience.</span></span> <span data-ttu-id="a8f47-118">Os usuários podem acessar aplicativos legados de dentro do Microsoft Edge sem ter que voltar para o IE11.</span><span class="sxs-lookup"><span data-stu-id="a8f47-118">Users can access legacy applications from within Microsoft Edge without having to switch back to IE11.</span></span>

<span data-ttu-id="a8f47-119">Depois de configurar o modo IE, você pode desativar o IE11 como um navegador autônomo **sem afetar a funcionalidade do modo IE** em sua organização usando a política de grupo.</span><span class="sxs-lookup"><span data-stu-id="a8f47-119">After you configure IE mode, you can disable IE11 as a standalone browser **without affecting IE mode functionality** across your organization using group policy.</span></span>

> [!NOTE]
> <span data-ttu-id="a8f47-120">Se você precisa do aplicativo IE11 autônomo para sites específicos e deseja redirecionar todo o tráfego do navegador para o Microsoft Edge, pode configurar o [Envie todos os sites não incluídos na lista de sites para o Microsoft Edge](https://docs.microsoft.com/deployedge/edge-ie-mode-policies#redirect-sites-from-ie-to-microsoft-edge) política para redirecionar sites do IE para o Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="a8f47-120">If you need the standalone IE11 app for specific sites, and want to redirect all other browser traffic to Microsoft Edge, you can configure the [Send all sites not included in the site list to Microsoft Edge](https://docs.microsoft.com/deployedge/edge-ie-mode-policies#redirect-sites-from-ie-to-microsoft-edge) policy to redirect sites from IE to Microsoft Edge.</span></span>

## <a name="user-experience-after-redirecting-traffic-to-microsoft-edge"></a><span data-ttu-id="a8f47-121">Experiência do usuário após redirecionar o tráfego para o Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="a8f47-121">User experience after redirecting traffic to Microsoft Edge</span></span>

<span data-ttu-id="a8f47-122">Quando você ativa o **Desabilitar o Internet Explorer 11 como um navegador autônomo** política, todas as atividades do IE11 são redirecionadas para o Microsoft Edge e os usuários têm a seguinte experiência:</span><span class="sxs-lookup"><span data-stu-id="a8f47-122">When you enable the **Disable Internet Explorer 11 as a standalone browser** policy, all IE11 activity is redirected to Microsoft Edge and users have the following experience:</span></span>

- <span data-ttu-id="a8f47-123">O ícone do IE11 no menu Iniciar será removido, mas o da barra de tarefas permanecerá.</span><span class="sxs-lookup"><span data-stu-id="a8f47-123">The IE11 icon on the Start Menu will be removed, but the one on the taskbar will remain.</span></span>
- <span data-ttu-id="a8f47-124">Quando os usuários tentam iniciar atalhos ou associações de arquivos que usam o IE11, eles são redirecionados para abrir o mesmo arquivo/URL no Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="a8f47-124">When users try to launch shortcuts or file associations that use IE11, they will be redirected to open the same file/URL in Microsoft Edge.</span></span>
- <span data-ttu-id="a8f47-125">Quando os usuários tentam iniciar o IE11 invocando diretamente o binário iexplore.exe, o Microsoft Edge é iniciado.</span><span class="sxs-lookup"><span data-stu-id="a8f47-125">When users try to launch IE11 by directly invoking the iexplore.exe binary, Microsoft Edge will launch instead.</span></span>

<span data-ttu-id="a8f47-126">Como parte da configuração da política para esta experiência, você pode opcionalmente mostrar uma mensagem de redirecionamento para cada usuário que tentar iniciar o IE11.</span><span class="sxs-lookup"><span data-stu-id="a8f47-126">As part of setting the policy for this experience, you can optionally show a redirect message for each user who tries to launch IE11.</span></span> <span data-ttu-id="a8f47-127">Esta mensagem pode ser definida para exibir "Sempre" ou "Uma vez por usuário".</span><span class="sxs-lookup"><span data-stu-id="a8f47-127">This message can be set to display "Always" or "Once per user".</span></span> <span data-ttu-id="a8f47-128">Por padrão, a mensagem de redirecionamento mostrada na próxima captura de tela nunca é mostrada.</span><span class="sxs-lookup"><span data-stu-id="a8f47-128">By default, the redirect message shown in the next screenshot is never shown.</span></span>

:::image type="content" source="media/edge-ie-disable-ie11/disable-ie-redirect-msg.png" alt-text="Alerta ao tentar abrir o IE após um redirecionamento para o Microsoft Edge estar ativo.":::

<span data-ttu-id="a8f47-130">Se a sua Lista de Sites do Modo Enterprise contém aplicativos configurados para abrir no aplicativo IE11 e você desabilitar o IE11 com esta política, eles serão abertos no modo IE no Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="a8f47-130">If your Enterprise Mode Site List contains applications that are configured to open in the IE11 app and you disable IE11 with this policy, they will open in IE mode on Microsoft Edge.</span></span>
> [!NOTE]
> <span data-ttu-id="a8f47-131">Há um problema conhecido com o fluxo do usuário quando um site é configurado para abrir no IE11 e a política de desabilitação do IE11 é definida.</span><span class="sxs-lookup"><span data-stu-id="a8f47-131">There is a known issue with the user flow when a site is configured to open in IE11 and the disable IE11 policy is set.</span></span> <span data-ttu-id="a8f47-132">O problema está sendo investigado ativamente.</span><span class="sxs-lookup"><span data-stu-id="a8f47-132">The issue being actively investigated.</span></span>

## <a name="disable-internet-explorer-11-as-a-standalone-browser"></a><span data-ttu-id="a8f47-133">Desabilitar o Internet Explorer 11 como um navegador independente</span><span class="sxs-lookup"><span data-stu-id="a8f47-133">Disable Internet Explorer 11 as a standalone browser</span></span>

<span data-ttu-id="a8f47-134">Para desabilitar o Internet Explorer 11 usando a política de grupo, siga estas etapas:</span><span class="sxs-lookup"><span data-stu-id="a8f47-134">To disable Internet Explorer 11 using group policy, follow these steps:</span></span>

1. <span data-ttu-id="a8f47-135">Baixar e instalar o mais recente [Modelo de política Microsoft Edge](https://www.microsoft.com/en-us/business/download).</span><span class="sxs-lookup"><span data-stu-id="a8f47-135">Download and install the latest [Microsoft Edge Policy Template](https://www.microsoft.com/en-us/business/download).</span></span>
2. <span data-ttu-id="a8f47-136">Abra o Editor de Política de Grupo.</span><span class="sxs-lookup"><span data-stu-id="a8f47-136">Open the Group Policy Editor.</span></span>
3. <span data-ttu-id="a8f47-137">Vá para ***Configuração do computador/Modelos administrativos/Componentes do Windows/Internet Explorer***.</span><span class="sxs-lookup"><span data-stu-id="a8f47-137">Go to ***Computer Configuration/Administrative Templates/Windows Components/Internet Explorer***.</span></span> 
4. <span data-ttu-id="a8f47-138">Duplo click **Desabilitar o Internet Explorer 11 como um navegador independente**.</span><span class="sxs-lookup"><span data-stu-id="a8f47-138">Double-click **Disable Internet Explorer 11 as a standalone browser**.</span></span>
5. <span data-ttu-id="a8f47-139">Selecionar **Habilitar**.</span><span class="sxs-lookup"><span data-stu-id="a8f47-139">Select **Enabled**.</span></span>
6. <span data-ttu-id="a8f47-140">Sob **Opções**, escolha um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="a8f47-140">Under **Options**, pick one of the following values:</span></span>

   - <span data-ttu-id="a8f47-141">**Nunca** se você não quiser notificar os usuários de que o IE11 está desativado.</span><span class="sxs-lookup"><span data-stu-id="a8f47-141">**Never** if you don’t want to notify users that IE11 is disabled.</span></span>
   - <span data-ttu-id="a8f47-142">**Sempre** se você deseja notificar os usuários sempre que eles forem redirecionados do IE11.</span><span class="sxs-lookup"><span data-stu-id="a8f47-142">**Always** if you want to notify users every time they're redirected from IE11.</span></span>
   - <span data-ttu-id="a8f47-143">**Uma vez por usuário** se desejar notificar os usuários apenas na primeira vez que forem redirecionados.</span><span class="sxs-lookup"><span data-stu-id="a8f47-143">**Once per user** if you want to notify users only the first time they are redirected.</span></span>

7. <span data-ttu-id="a8f47-144">Clicar **OK** ou **Aplicar** para salvar esta configuração de política.</span><span class="sxs-lookup"><span data-stu-id="a8f47-144">Click **OK** or **Apply** to save this policy setting.</span></span>

## <a name="see-also"></a><span data-ttu-id="a8f47-145">Ver também</span><span class="sxs-lookup"><span data-stu-id="a8f47-145">See also</span></span>

- [<span data-ttu-id="a8f47-146">Página de aterrissagem do Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="a8f47-146">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="a8f47-147">Sobre o modo IE</span><span class="sxs-lookup"><span data-stu-id="a8f47-147">About IE mode</span></span>](https://docs.microsoft.com/deployedge/edge-ie-mode)
- [<span data-ttu-id="a8f47-148">Informações adicionais sobre o Modo Empresarial</span><span class="sxs-lookup"><span data-stu-id="a8f47-148">Additional Enterprise Mode information</span></span>](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
