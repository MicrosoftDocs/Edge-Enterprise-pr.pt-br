---
title: Implantar o Microsoft Edge com atualizações do Windows 10
ms.author: ryhecht
author: RyanHechtMSFT
manager: tinad
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Implantar o Microsoft Edge com atualizações do Windows 10
ms.openlocfilehash: 1f3a99259cb28c46e4f6f30de05fade6ac158336
ms.sourcegitcommit: 556aca8dde42dd66364427f095e8e473b86651a0
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2022
ms.locfileid: "12445825"
---
# <a name="deploy-microsoft-edge-with-windows-10-updates"></a>Implantar o Microsoft Edge com atualizações do Windows 10

O artigo fornece informações para usuários que estão implantando o Microsoft Edge usando as atualizações do Windows 10.

## <a name="for-windows-10-release-20h2"></a>Para Windows 10 versão 20H2

Windows 10 20H2 e posteriores incluem Microsoft Edge pré-instalado como o navegador padrão. No entanto, a versão 84 do Edge que foi enviada com o Windows 10 20H2 e a versão 92 do Edge que foi enviada com Windows 10 21H2, agora está desatualizada. Embora Microsoft Edge se atualize automaticamente para uma versão mais recente depois que um usuário tiver feito logor, já que o tempo da atualização depende de vários fatores, isso pode ser um pouco imprestável. Para organizações que desejam maior controle e desejam garantir que o Edge (canal estável) seja atualizado para a versão mais recente antes do logon do usuário, o comando a seguir do PowerShell pode ser usado para forçar uma atualização de Borda durante Windows OOBE.

`Start-Process -FilePath "C:\Program Files (x86)\Microsoft\EdgeUpdate\MicrosoftEdgeUpdate.exe" -argumentlist "/silent /install appguid={56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}&appname=Microsoft%20Edge&needsadmin=True"`

Se você Windows autopilot, é possível envolvê-lo como um arquivo .intunewin usando a ferramenta de preparação de conteúdo [do Microsoft Win32](/mem/intune/apps/apps-win32-prepare). Em seguida, ele pode ser definido como um aplicativo necessário para a Página de Status de Registro (ESP), se desejado.

> [!NOTE]
> Se você atualmente aproveitar políticas como substituição de [](/deployedge/microsoft-edge-update-policies#target-channel-override) Canal de Destino ou [](/deployedge/microsoft-edge-update-policies#targetversionprefix) Substituição de Versão de Destino para permanecer em uma versão mais antiga do Edge, esteja ciente de que o script acima não levará nenhuma política em consideração e simplesmente atualizará para a versão mais recente. Por padrão, o Edge não se rebaixa, incluindo depois que essas políticas são recebidas posteriormente.

## <a name="for-windows-10-releases-rs4-through-20h1"></a>Para Windows 10, versões RS4 a 20H1

O Windows Server Update Services (WSUS) tem atualizações para cada versão do Windows 10 de RS4 a 20H1 que removerão o aplicativo de desktop Versão Prévia do Microsoft Edge e o substituirão pelo Microsoft Edge. Para obter mais informações, consulte [este artigo de suporte](https://support.microsoft.com/topic/update-in-wsus-for-the-new-microsoft-edge-for-windows-10-version-1809-1903-1909-and-2004-october-29-2020-b4980418-4ec4-dee7-3b17-1c6499bd127c) para descobrir qual atualização do WSUS é a certa para a sua versão do Windows.

## <a name="for-windows-10-releases-prior-to-rs4-and-windows-7-81-and-earlier"></a>Para versões do Windows 10 anteriores ao RS4 (e Windows 7, 8.1 e anteriores)

As atualizações do Windows para instalar o Microsoft Edge não estão disponíveis para essas versões. Considere outras opções para implantar o Microsoft Edge nesses dispositivos, como [Configuration Manager](/configmgr/apps/deploy-use/deploy-edge?bc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2fbreadcrumb%2ftoc.json&toc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2ftoc.json) ou [Intune ](/intune/apps/apps-windows-edge/?bc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2fbreadcrumb%2ftoc.json&toc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2ftoc.json).

## <a name="see-also"></a>Veja também

- [Página de destino do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Planejar sua implantação do Microsoft Edge](deploy-edge-plan-deployment.md)
