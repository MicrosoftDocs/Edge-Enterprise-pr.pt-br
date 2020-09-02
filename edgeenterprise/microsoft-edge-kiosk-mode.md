---
title: Modo de quiosque do Microsoft Edge
ms.author: brianalt
author: brianalt
manager: seanlynd
ms.date: 01/16/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Modo de quiosque do Microsoft Edge
ms.openlocfilehash: 7a690820752b5361349bf394055a737bd8175215
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979140"
---
# Modo de quiosque do Microsoft Edge

Este artigo fornece uma visão geral das opções do modo de quiosque do Microsoft Edge (versão 77 ou posteriores). Ele também aborda o que é necessário para continuar usando o modo de quiosque da Versão Herdada do Microsoft Edge (versão 45 e anteriores).

Para obter informações sobre o modo de quiosque da Versão Herdada do Microsoft Edge (versão 45 e anteriores), consulte [Implantar o modo de quiosque do Microsoft Edge](https://aka.ms/edgekioskmode).

## Microsoft Edge com acesso atribuído

O Microsoft Edge pode ser executado com [acesso atribuído a vários aplicativos](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps) no Windows 10, que é o equivalente ao tipo de modo de quiosque "Navegação Normal" da Versão Herdada do Microsoft Edge. Para configurar o Microsoft Edge com acesso atribuído a vários aplicativos, siga as instruções sobre como [Configurar um quiosque para vários aplicativos](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps). O AUMID para o canal Estável do Microsoft Edge é **MSEdge**.

Ao usar o Microsoft Edge com acesso atribuído a vários aplicativos, você poderá usar as [políticas de navegador do Microsoft Edge](microsoft-edge-policies.md) para configurar a experiência de navegação para atender aos seus requisitos exclusivos.

Hoje, o Microsoft Edge não oferece suporte para os mesmos tipos de modo de quiosque da Versão Herdada do Microsoft Edge para acesso atribuído de aplicativo único e o tipo de modo de quiosque "Navegação pública" no acesso atribuído a vários aplicativos. Se você precisar de um navegador para o dispositivo de quiosque de acesso atribuído de aplicativo único, recomendamos o uso do [modo de quiosque da Versão Herdada do Microsoft Edge](https://aka.ms/edgekioskmode) ou o [aplicativo Kiosk Browser da Microsoft](https://www.microsoft.com/p/kiosk-browser/9ngb5s5xg2kp?activetab=pivot:overviewtab). 

## Parâmetro de linha de comando "--kiosk" do Microsoft Edge

Você pode iniciar o Microsoft Edge no modo de quiosque usando o parâmetro de linha de comando "`--kiosk`". Isso abre o navegador em tela inteira com o atalho de teclado de tela inteira desabilitado (F11). Para fazer isso, crie um atalho com o destino definido como:<br>
*`"<local path>\msedge.exe" --kiosk http://bing.com`*

> [!NOTE]
> O parâmetro "`--kiosk`" não impedirá que o usuário acesse os atalhos de teclado do Windows e não impedirá a execução de outros aplicativos. Para realizar esse tipo de controle, considere o uso do [AppLocker para criar um quiosque do Windows 10](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-applocker) e um [Filtro de teclado](https://docs.microsoft.com/windows-hardware/customize/enterprise/keyboardfilter).

Para sair do modo de quiosque e fechar o navegador, use alt+F4.

## Suporte para o modo de quiosque da Versão Herdada do Microsoft Edge

Quando a nova versão do canal Estável do Microsoft Edge estiver instalada, a Versão Herdada do Microsoft Edge ficará oculta e todas as tentativas de iniciar a Versão Herdada do Microsoft Edge serão redirecionadas para a nova versão. Para obter informações sobre:

- Requisitos de atualizações do Windows, consulte [Atualizações do Windows para oferecer suporte à próxima versão do Microsoft Edge](microsoft-edge-sysupdate-windows-updates.md) 
- Acesso à Versão Herdada do Microsoft Edge depois de instalar o Microsoft Edge, consulte [Acessar a Versão Herdada do Microsoft Edge depois de instalar a nova versão do Microsoft Edge](microsoft-edge-sysupdate-access-old-edge.md)
 
Para continuar usando o modo de quiosque da Versão Herdada do Microsoft Edge em seus dispositivos de quiosque, execute uma das seguintes ações: 

- Se você pretende instalar o canal Estável do Microsoft Edge, deseja permitir que ele seja instalado ou se ele já estiver instalado em seu dispositivo de quiosque, implante a política [Permitir experiência de navegador lado a lado do Microsoft Edge](https://docs.microsoft.com/deployedge/microsoft-edge-update-policies#allowsxs) do Microsoft Edge.
- Para impedir que o canal Estável do Microsoft Edge seja instalado nos seus dispositivos de quiosque, implante a política [Permitir instalação padrão](https://docs.microsoft.com/deployedge/microsoft-edge-update-policies#allow-installation-default) do Microsoft Edge no canal Estável ou considere o uso do [Blocker toolkit para desabilitar a entrega automática do Microsoft Edge](microsoft-edge-blocker-toolkit.md). 

## Consulte também

- [Configurar quiosques e sinalizações digitais em edições do Windows desktop](https://docs.microsoft.com/windows/configuration/kiosk-methods)
- [Implantar o modo de quiosque da Versão Herdada do Microsoft Edge](https://aka.ms/edgekioskmode) 
- [Planejar sua implantação do Microsoft Edge](deploy-edge-plan-deployment.md)
- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
