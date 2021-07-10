---
title: Edge para a infraestrutura da área de trabalho de Virtualização
ms.author: anlake
author: AndreaLBarr
manager: collw
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Microsoft Edge para Infraestrutura da Área de Trabalho Virtualizada.
ms.openlocfilehash: 5dc234b0e6fbba4778f8236399a0ff438f704578
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/09/2021
ms.locfileid: "11641847"
---
# <a name="microsoft-edge-for-virtualized-desktop-infrastructure"></a><span data-ttu-id="4acc0-103">Microsoft Edge para Infraestrutura da Área de Trabalho Virtualizada</span><span class="sxs-lookup"><span data-stu-id="4acc0-103">Microsoft Edge for Virtualized Desktop Infrastructure</span></span>

<span data-ttu-id="4acc0-104">Este artigo descreve os requisitos e limitações para o uso da Microsoft Edge em um ambiente virtualizado.</span><span class="sxs-lookup"><span data-stu-id="4acc0-104">This article describes the requirements and limitations for using Microsoft Edge in a virtualized environment.</span></span>

## <a name="what-is-vdi"></a><span data-ttu-id="4acc0-105">O que é VDI?</span><span class="sxs-lookup"><span data-stu-id="4acc0-105">What is VDI?</span></span>

<span data-ttu-id="4acc0-106">Virtual Desktop Infrastructure (VDI) é uma tecnologia de virtualização que hospeda um sistema operacional da área de trabalho e aplicativos em um servidor centralizado em um centro de dados.</span><span class="sxs-lookup"><span data-stu-id="4acc0-106">Virtual Desktop Infrastructure (VDI) is virtualization technology that hosts a desktop operating system and applications on a centralized server in a data center.</span></span> <span data-ttu-id="4acc0-107">Isto permite uma experiência da área de trabalho totalmente personalizada para os usuários com uma fonte centralizada totalmente segura e compatível.</span><span class="sxs-lookup"><span data-stu-id="4acc0-107">This enables a fully personalized desktop experience for users with a fully secured and compliant centralized source.</span></span>

<span data-ttu-id="4acc0-108">O Microsoft Edge pode ser usado em um ambiente virtualizado da mesma maneira que pode ser usado no dispositivo local, durante a execução em um ambiente de servidor seguro e controlado.</span><span class="sxs-lookup"><span data-stu-id="4acc0-108">Microsoft Edge can be used in such a virtualized environment in much the same ways as it can be used on the local device, all the while running from secure and controlled server environment.</span></span> <span data-ttu-id="4acc0-109">Dependendo da solução VDI escolhida, também pode ser possível fornecer a seus usuários acesso sem problemas aos Aplicativos e Sites da intranet.</span><span class="sxs-lookup"><span data-stu-id="4acc0-109">Depending on your chosen VDI solution it may also be possible to give your users seamless access to intranet Applications and Sites.</span></span>

<span data-ttu-id="4acc0-110">A maioria dos recursos do Edge são suportados em ambientes VDI sem nenhuma configuração especial.</span><span class="sxs-lookup"><span data-stu-id="4acc0-110">Most features of Edge are supported on VDI environments without any special configuration.</span></span> <span data-ttu-id="4acc0-111">No entanto, para garantir uma experiência perfeita, é recomendável seguir as diretrizes abaixo.</span><span class="sxs-lookup"><span data-stu-id="4acc0-111">However, to ensure an optimal experience it’s recommended to follow the guidance below.</span></span>

## <a name="platforms-certified-for-edge"></a><span data-ttu-id="4acc0-112">Plataformas certificadas para o Edge</span><span class="sxs-lookup"><span data-stu-id="4acc0-112">Platforms certified for Edge</span></span>

- <span data-ttu-id="4acc0-113">Área de Trabalho Virtual do Azure</span><span class="sxs-lookup"><span data-stu-id="4acc0-113">Azure Virtual Desktop</span></span>
- <span data-ttu-id="4acc0-114">Citrix Virtual Apps e Desktops (anteriormente conhecidos como XenApp e XenDesktop)</span><span class="sxs-lookup"><span data-stu-id="4acc0-114">Citrix Virtual Apps and Desktops (formerly known as XenApp and XenDesktop)</span></span>

<span data-ttu-id="4acc0-115">Embora outras soluções VDI ainda não tenham sido verificadas pela equipe do Edge, é esperado que os fluxos de trabalho mais comuns no Edge sejam apoiados.</span><span class="sxs-lookup"><span data-stu-id="4acc0-115">While other VDI solutions have not yet been verified by the Edge team, it is expected that the most common workflows in Edge should be supported.</span></span> <span data-ttu-id="4acc0-116">As diretrizes fornecidas abaixo podem ou não ser aplicáveis à solução escolhida.</span><span class="sxs-lookup"><span data-stu-id="4acc0-116">Guidance provided below may or may not be applicable to your chosen solution.</span></span>

## <a name="edge-on-vdi-performance-considerations"></a><span data-ttu-id="4acc0-117">Edge nas considerações de desempenho da VDI</span><span class="sxs-lookup"><span data-stu-id="4acc0-117">Edge on VDI performance considerations</span></span>

<span data-ttu-id="4acc0-118">Ao projetar seu ambiente VDI, você deve considerar cuidadosamente os fluxos de trabalho e as necessidades de seus usuários para alcançar o melhor desempenho, bem como os limites da configuração de seu servidor.</span><span class="sxs-lookup"><span data-stu-id="4acc0-118">When designing your VDI environment you should carefully consider the workflows and needs of your users to achieve optimal performance, as well as the limits of your server configuration.</span></span>

<span data-ttu-id="4acc0-119">O Edge recomenda os seguintes requisitos mínimos para implantar o Edge em ambientes VDI:</span><span class="sxs-lookup"><span data-stu-id="4acc0-119">Edge recommends the following minimal requirements for deploying Edge to VDI environments:</span></span>

- <span data-ttu-id="4acc0-120">vCPU – 2-4 Núcleos por Usuário</span><span class="sxs-lookup"><span data-stu-id="4acc0-120">vCPU – 2-4 Cores per User</span></span>
- <span data-ttu-id="4acc0-121">RAM – 1 GB por Usuário</span><span class="sxs-lookup"><span data-stu-id="4acc0-121">RAM – 1 GB per User</span></span>

<span data-ttu-id="4acc0-122">Observe que grandes aplicativos web e extensões complexas exigirão mais memória e terão que ser contabilizadas ao configurar seu ambiente.</span><span class="sxs-lookup"><span data-stu-id="4acc0-122">Please note that large complex web applications and extensions will require more memory and will have to be accounted for when configuring your environment.</span></span>

## <a name="edge-on-non-persisted-vdi-environments"></a><span data-ttu-id="4acc0-123">Edge em ambientes VDI não persistentes</span><span class="sxs-lookup"><span data-stu-id="4acc0-123">Edge on non-persisted VDI environments</span></span>

<span data-ttu-id="4acc0-124">Muitas soluções VDI permitem o acesso a ambientes persistentes, onde é atribuído aos usuários um ambiente virtual que persiste entre sessões, e ambientes não persistentes, onde os usuários são atribuídos a uma das várias máquinas disponíveis, possivelmente uma máquina diferente a cada sessão, os dados do usuário podem ou não sincronizar entre as sessões.</span><span class="sxs-lookup"><span data-stu-id="4acc0-124">Many VDI solutions allow access to persisted environments, where users are assigned a virtual environment that persists between sessions, and non-persisted environments, where users are assigned to one of several available machines, possibly a different machine each session, user data may or may not sync between sessions.</span></span>

<span data-ttu-id="4acc0-125">Ao usar um ambiente não persistente, geralmente é criada uma "imagem dourada" que é usada para cada dispositivo que inclui os aplicativos e configurações necessários.</span><span class="sxs-lookup"><span data-stu-id="4acc0-125">When using a non-persisted environment, one usually creates a “golden image” which is used for each device that includes the needed apps and configurations.</span></span> <span data-ttu-id="4acc0-126">Abaixo estão nossas recomendações para preparar o Edge para essa imagem.</span><span class="sxs-lookup"><span data-stu-id="4acc0-126">Below are our recommendations for preparing Edge for such an image.</span></span>

### <a name="deploy-edge"></a><span data-ttu-id="4acc0-127">Implante o Edge</span><span class="sxs-lookup"><span data-stu-id="4acc0-127">Deploy Edge</span></span>

<span data-ttu-id="4acc0-128">Se você estiver no Windows 10, versão 1803 ou superior, você deve ter o Microsoft Edge instalado em seu sistema.</span><span class="sxs-lookup"><span data-stu-id="4acc0-128">If you are on Windows 10, version 1803 and above, you should have Microsoft Edge installed on your system.</span></span> <span data-ttu-id="4acc0-129">No entanto, se você estiver em uma versão mais antiga do Windows ou desejar implantar um canal diferente do Edge, as seguintes etapas são recomendadas.</span><span class="sxs-lookup"><span data-stu-id="4acc0-129">However, if you are on an older version of Windows or wish to deploy a different channel of Edge, the following steps are recommended.</span></span>

1. <span data-ttu-id="4acc0-130">Baixe o pacote Edge MSI que combina com seu sistema operacional VDI VM de:</span><span class="sxs-lookup"><span data-stu-id="4acc0-130">Download the Edge MSI package matching your VDI VM operating system from:</span></span>

    - [<span data-ttu-id="4acc0-131">Baixe o Microsoft Edge for Business - Microsoft</span><span class="sxs-lookup"><span data-stu-id="4acc0-131">Download Microsoft Edge for Business - Microsoft</span></span>](https://www.microsoft.com/edge/business/download)

2. <span data-ttu-id="4acc0-132">Instale o MSI para o VDI VM executando o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="4acc0-132">Install the MSI to the VDI VM by running the following command:</span></span>

    - `msiexec /i <path_to_msi> /qn /norestart /l*v <install_logfile_name>`

### <a name="disable-automatic-updates"></a><span data-ttu-id="4acc0-133">Desabilite atualizações automáticas</span><span class="sxs-lookup"><span data-stu-id="4acc0-133">Disable automatic updates</span></span>

<span data-ttu-id="4acc0-134">Para máquinas não persistentes, é melhor desabilitar atualizações automáticas e, em vez disso, atualizar o Edge atualizando a "imagem dourada" para garantir que não haja incompatibilidades de versão entre o pool de máquinas.</span><span class="sxs-lookup"><span data-stu-id="4acc0-134">For non-persisted machines it is best practice to disable automatic updates and instead update Edge by updating the “golden image” to ensure that there are no version mismatches among the pool of machines.</span></span>

<span data-ttu-id="4acc0-135">Consulte as seguintes políticas para desabilitar atualizações automáticas:</span><span class="sxs-lookup"><span data-stu-id="4acc0-135">See the following policies for disabling automatic updates:</span></span>

- [<span data-ttu-id="4acc0-136">Atualizar o padrão de substituição de política</span><span class="sxs-lookup"><span data-stu-id="4acc0-136">Update policy override default</span></span>](/deployedge/microsoft-edge-update-policies#updatedefault)

- [<span data-ttu-id="4acc0-137">Atualizar a substituição de política</span><span class="sxs-lookup"><span data-stu-id="4acc0-137">Update policy override</span></span>](/deployedge/microsoft-edge-update-policies#update)

### <a name="profile-management"></a><span data-ttu-id="4acc0-138">Gerenciamento de perfil</span><span class="sxs-lookup"><span data-stu-id="4acc0-138">Profile management</span></span>

<span data-ttu-id="4acc0-139">Em configurações não persistentes, é importante considerar que as VMs podem não manter o estado do usuário entre sessões ou os usuários podem ser atribuídos a uma VM que nunca usaram antes e, como tal, não tenha nenhum de seus dados de usuário.</span><span class="sxs-lookup"><span data-stu-id="4acc0-139">On non-persisted setups it is important to consider that VMs may not maintain user state between sessions or users may be assigned a VM they have never used before and as such has none of their user data.</span></span>

<span data-ttu-id="4acc0-140">O Edge suporta vários métodos para sincronizar os dados do usuário, de modo que esteja disponível independentemente de como eles estão acessando o Edge.</span><span class="sxs-lookup"><span data-stu-id="4acc0-140">Edge supports several methods for syncing user data such that it is available regardless of how they are accessing Edge.</span></span>

### <a name="azure-ad-sync"></a><span data-ttu-id="4acc0-141">Azure AD Sync</span><span class="sxs-lookup"><span data-stu-id="4acc0-141">Azure AD Sync</span></span>

<span data-ttu-id="4acc0-142">Se seu plano Microsoft Azure Active Directory o suporta, o Enterprise sync é o método mais rápido e fácil para garantir que os dados do usuário Edge sejam sincronizados com todos os dispositivos do usuário.</span><span class="sxs-lookup"><span data-stu-id="4acc0-142">If your Azure AD plan supports it, Enterprise sync is the fastest and easiest method to ensure that Edge user data is synced to all user devices.</span></span>  

<span data-ttu-id="4acc0-143">Consulte o seguinte para obter mais informações sobre os requisitos e configuração.</span><span class="sxs-lookup"><span data-stu-id="4acc0-143">See the following for more information on requirements and configuration.</span></span>  

- [<span data-ttu-id="4acc0-144">Configurar sincronização do Microsoft Edge enterprise | Microsoft Docs</span><span class="sxs-lookup"><span data-stu-id="4acc0-144">Configure Microsoft Edge enterprise sync | Microsoft Docs</span></span>](/deployedge/microsoft-edge-enterprise-sync)

### <a name="on-premise-sync-for-active-directory-users"></a><span data-ttu-id="4acc0-145">Sincronização Local para Usuários do Active Directory</span><span class="sxs-lookup"><span data-stu-id="4acc0-145">On-premise Sync for Active Directory Users</span></span>

<span data-ttu-id="4acc0-146">Com a sincronização local, o Microsoft Edge salva os favoritos e as configurações de um usuário do Active Directory em um arquivo que pode ser facilmente movido entre diferentes computadores.</span><span class="sxs-lookup"><span data-stu-id="4acc0-146">With on-premises sync, Microsoft Edge saves an Active Directory user's favorites and settings to a file that can easily be moved between different computers.</span></span>  

<span data-ttu-id="4acc0-147">Consulte o seguinte para obter mais informações sobre os requisitos e configuração.</span><span class="sxs-lookup"><span data-stu-id="4acc0-147">See the following for more information on requirements and configuration.</span></span>  

- [<span data-ttu-id="4acc0-148">Sincronização local para usuários do Active Directory (AD) | Microsoft Docs</span><span class="sxs-lookup"><span data-stu-id="4acc0-148">On-premises sync for Active Directory (AD) users | Microsoft Docs</span></span>](/deployedge/microsoft-edge-on-premises-sync)

### <a name="user-profile-redirection"></a><span data-ttu-id="4acc0-149">Redirecionamento do Perfil do Usuário</span><span class="sxs-lookup"><span data-stu-id="4acc0-149">User Profile Redirection</span></span>  

<span data-ttu-id="4acc0-150">Há várias soluções para migrar e redirecionar toda a pasta do usuário para garantir que o contexto do usuário seja mantido nesses ambientes não persistentes.</span><span class="sxs-lookup"><span data-stu-id="4acc0-150">There are several solutions for migrating and redirecting the entire user folder to ensure that user context is maintained in such non-persisted environments.</span></span> <span data-ttu-id="4acc0-151">Verifique com seu provedor VDI para determinar a solução recomendada.</span><span class="sxs-lookup"><span data-stu-id="4acc0-151">Check with your VDI provider to determine the recommended solution.</span></span>

<span data-ttu-id="4acc0-152">Algumas soluções populares incluem:</span><span class="sxs-lookup"><span data-stu-id="4acc0-152">Some popular solutions include:</span></span>

- [<span data-ttu-id="4acc0-153">Visão geral do FSLogix - FSLogix | Microsoft Docs</span><span class="sxs-lookup"><span data-stu-id="4acc0-153">FSLogix Overview - FSLogix | Microsoft Docs</span></span>](/fslogix/overview)
- [<span data-ttu-id="4acc0-154">Como Configurar o Gerenciamento de Perfil Citrix</span><span class="sxs-lookup"><span data-stu-id="4acc0-154">How to Configure Citrix Profile Management</span></span>](https://support.citrix.com/article/CTX222893)

<span data-ttu-id="4acc0-155">Também é recomendável que, ao usar esse método, pastas desnecessárias sejam excluídas da pasta do usuário com backup para reduzir os tempos de carregamento iniciais quando os usuários fazem logon em um computador e o perfil está sendo migrado.</span><span class="sxs-lookup"><span data-stu-id="4acc0-155">It is also may be recommended that when using this method unnecessary folders be excluded from the backed-up user folder to reduce initial loading times when users are logging on to a machine and the profile is being migrated.</span></span> <span data-ttu-id="4acc0-156">Em caso afirmativo, recomendamos que as pastas a seguir sejam excluídas de seu backup para reduzir o tamanho.</span><span class="sxs-lookup"><span data-stu-id="4acc0-156">If so, we recommend the following folders be excluded from your backup to reduce size.</span></span>

- <span data-ttu-id="4acc0-157">%LocalAppData%\Microsoft\Edge\User Data\Default\Cache</span><span class="sxs-lookup"><span data-stu-id="4acc0-157">%LocalAppData%\Microsoft\Edge\User Data\Default\Cache</span></span>
- <span data-ttu-id="4acc0-158">%LocalAppData%\Microsoft\Edge\User Data\Default\Code Cache</span><span class="sxs-lookup"><span data-stu-id="4acc0-158">%LocalAppData%\Microsoft\Edge\User Data\Default\Code Cache</span></span>
- <span data-ttu-id="4acc0-159">%LocalAppData%\Microsoft\Edge\User Data\Default\JumpListIconsTopSites</span><span class="sxs-lookup"><span data-stu-id="4acc0-159">%LocalAppData%\Microsoft\Edge\User Data\Default\JumpListIconsTopSites</span></span>
- <span data-ttu-id="4acc0-160">%LocalAppData%\Microsoft\Edge\User Data\Default\JumpListIconsRecentClosed</span><span class="sxs-lookup"><span data-stu-id="4acc0-160">%LocalAppData%\Microsoft\Edge\User Data\Default\JumpListIconsRecentClosed</span></span>

## <a name="known-issues"></a><span data-ttu-id="4acc0-161">Problemas conhecidos</span><span class="sxs-lookup"><span data-stu-id="4acc0-161">Known issues</span></span>

### <a name="microsoft-edge-crashes-in-older-versions-of-xenapp-and-xendesktop"></a><span data-ttu-id="4acc0-162">Microsoft Edge falhas em versões mais antigas do XenApp e XenDesktop</span><span class="sxs-lookup"><span data-stu-id="4acc0-162">Microsoft Edge crashes in older versions of XenApp and XenDesktop</span></span>

<span data-ttu-id="4acc0-163">Este problema deve ser mitigado em versões mais recentes, no entanto, se você estiver encontrando esse problema em seu ambiente, você pode resolver o problema desabilitando os Ganchos API Citrix para Edge, consulte [Como Desabilitar os Ganchos da API Citrix por Aplicativo.](https://support.citrix.com/article/CTX107825)</span><span class="sxs-lookup"><span data-stu-id="4acc0-163">This issue should be mitigated in newer versions however if you are encountering this issue in your environment, you can work around the issue by disabling Citrix API Hooks for Edge, see [How to Disable Citrix API Hooks on a Per-application Basis.](https://support.citrix.com/article/CTX107825)</span></span>

### <a name="degraded-performance-when-rendering-pages-with-exceptionally-large-html-tables"></a><span data-ttu-id="4acc0-164">Desempenho degradado ao renderizar páginas com tabelas HTML excepcionalmente grandes</span><span class="sxs-lookup"><span data-stu-id="4acc0-164">Degraded performance when rendering pages with exceptionally large HTML tables</span></span>

<span data-ttu-id="4acc0-165">As seguintes políticas da Citrix são conhecidas pela lenta renderização de páginas html com tabelas muito grandes (mais de 30.000 linhas).</span><span class="sxs-lookup"><span data-stu-id="4acc0-165">The following Citrix policies are known to slow rendering of html pages with very large (30,000+ row) tables.</span></span>

- <span data-ttu-id="4acc0-166">Exibição automática de teclado</span><span class="sxs-lookup"><span data-stu-id="4acc0-166">Automatic keyboard display</span></span>
- <span data-ttu-id="4acc0-167">Caixa de combinação remota</span><span class="sxs-lookup"><span data-stu-id="4acc0-167">Remote the combo box</span></span>

<span data-ttu-id="4acc0-168">Consulte [Configurações da política de experiência móvel (citrix.com)](https://docs.citrix.com/citrix-virtual-apps-desktops/policies/reference/ica-policy-settings/mobile-experience-policy-settings.html) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="4acc0-168">See [Mobile experience policy settings (citrix.com)](https://docs.citrix.com/citrix-virtual-apps-desktops/policies/reference/ica-policy-settings/mobile-experience-policy-settings.html) for more information.</span></span> <span data-ttu-id="4acc0-169">A desabilitação dessas políticas deve mitigar a questão.</span><span class="sxs-lookup"><span data-stu-id="4acc0-169">Disabling these policies should mitigate the issue.</span></span>

### <a name="windows-account-manager-authorization-scenarios-ie--azure-sync-fail-in-edge-when-run-as-a-citrix-seamless-application"></a><span data-ttu-id="4acc0-170">Windows Cenários de autorização do Gerenciador de Contas (ou seja,  Sincronização do Azure) falha no Edge quando executado como um aplicativo sem interrupção do Citrix</span><span class="sxs-lookup"><span data-stu-id="4acc0-170">Windows Account Manager authorization scenarios (i.e.  Azure sync) fail in Edge when run as a Citrix seamless application</span></span>

<span data-ttu-id="4acc0-171">Esse é um problema conhecido no Edge e em outros aplicativos que usam WAM (ou seja, Office) devido Windows componentes necessários para esses cenários não serem inicializados ao executar no modo "contínuo".</span><span class="sxs-lookup"><span data-stu-id="4acc0-171">This is a known issue in Edge and other applications that use WAM (i.e. Office) due to Windows components necessary for such scenarios not being initialized when running in the “seamless” mode.</span></span> <span data-ttu-id="4acc0-172">Para resolver esse problema:</span><span class="sxs-lookup"><span data-stu-id="4acc0-172">To work around this issue:</span></span>

- <span data-ttu-id="4acc0-173">Use Edge por meio de uma Área de Trabalho Remota para o Host Citrix em vez de como um aplicativo remoto contínuo.</span><span class="sxs-lookup"><span data-stu-id="4acc0-173">Use Edge via a Remote Desktop to the Citrix Host instead of as a seamless remote application.</span></span>
- <span data-ttu-id="4acc0-174">Em vez disso, use aplicativos remotos da Área de Trabalho Virtual do Azure, que têm mitigação para esse problema.</span><span class="sxs-lookup"><span data-stu-id="4acc0-174">Use Azure Virtual Desktop remote apps instead, which has mitigation's for this issue.</span></span>
