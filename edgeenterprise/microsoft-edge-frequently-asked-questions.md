---
title: Perguntas frequentes (perguntas frequentes) sobre Microsoft Edge na empresa
ms.author: collw
author: dan-wesley
manager: seanlynd
ms.date: 01/11/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Perguntas frequentes (perguntas frequentes) sobre Microsoft Edge na empresa
ms.openlocfilehash: 86f1fdee4697d8087014e35daf41b600eeb62471
ms.sourcegitcommit: e7f3098d8b7d91cae20b5778a71a87daababc312
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/15/2022
ms.locfileid: "12298310"
---
# <a name="microsoft-edge-frequently-asked-questions"></a>Microsoft Edge perguntas frequentes

Este artigo contém perguntas frequentes (perguntas frequentes) sobre Microsoft Edge na empresa.

> [!NOTE]
> Este artigo se aplica ao Microsoft Edge versão 77 ou posterior.

## <a name="how-do-i-know-which-version-of-microsoft-edge-i-have"></a>Como sei que versão do Microsoft Edge tenho?

Selecione o ícone de releições (**...**) no canto superior direito do Microsoft Edge e selecione **Configurações**. Escolha **Sobre o Microsoft Edge** para ver sua versão do Microsoft Edge.

## <a name="what-about-internet-explorer-11"></a>E o Internet Explorer 11?

O aplicativo de área de trabalho do Internet Explorer 11 será retirado e ficará sem suporte em 15 de junho de 2022. Para ver o que está no escopo, consulte O futuro do Internet Explorer no Windows 10 [está em Microsoft Edge](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/). Os mesmos aplicativos e sites do IE11 que você usa hoje podem abrir no Microsoft Edge com o modo Internet Explorer. Para obter mais informações, consulte Perguntas frequentes sobre a aposentadoria de aplicativos da área de trabalho do [Internet Explorer 11.](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/internet-explorer-11-desktop-app-retirement-faq/ba-p/2366549)

## <a name="does-microsoft-edge-support-activex-controls-or-browser-helper-objects-like-silverlight-or-java"></a>O Microsoft Edge dá suporte ActiveX controles ou objetos auxiliares do navegador como o Silverlight ou Java?

Não. Microsoft Edge não dá suporte a controles ActiveX ou Objetos de Ajuda do Navegador (BHOs) como Silverlight ou Java. No entanto, se você estiver executando aplicativos Web que usam controles ActiveX, BHOs ou modos de documento herdados no Internet Explorer 11, você pode configurá-los para executar no modo IE no Microsoft Edge. Para obter mais informações, consulte [Configurar o modo IE no Microsoft Edge](./edge-ie-mode.md).

## <a name="will-favorites-be-ported-over-from-the-current-version-of-microsoft-edge-or-will-i-have-to-re-add-them"></a>Os favoritos serão portados da versão atual do Microsoft Edge ou eu vou ter que adicioná-los de novo?

Microsoft Edge é compatível com a importação de instalação existente de Microsoft Edge, Chrome, Internet Explorer e Firefox (no Win10). As configurações a seguir são suportadas para importação: Indicadores, Histórico, Senhas e Autofill (pagamentos, endereços e formulários genéricos). Você pode optar por importar na primeira experiência de execução ou das configurações do navegador.

## <a name="whats-the-difference-between-the-stable-beta-dev-and-canary-channelsbuilds"></a>Qual é a diferença entre as versões/builds Estável, Beta, Dev e Canary?

O canal estável do Microsoft Edge é o canal mais estável que oferecemos com recursos voltados para a empresa prontos para que você pilote e avalie [em](https://aka.ms/EdgeEnterprise) toda a sua organização. O canal Beta permite que você valide a próxima versão Estável com um conjunto representativo de usuários. Os canais Estável e Beta são atualizados aproximadamente a cada seis semanas. Os canais Dev e Canary continuam a ser atualizados semanalmente e diariamente, respectivamente. Os instaladores offline (arquivos MSIs e PKG) estão disponíveis apenas para canais Estáveis, Beta e Dev. Para obter mais informações, consulte [Visão geral dos canais do Microsoft Edge](./microsoft-edge-channels.md).

## <a name="what-kind-of-extension-support-do-i-have-with-microsoft-edge"></a>Que tipo de suporte de extensão tenho com Microsoft Edge?

Microsoft Edge suporta extensões de [Microsoft Edge Insider Addons](https://go.microsoft.com/fwlink/?linkid=2081222) e o [Chrome Web Store](https://go.microsoft.com/fwlink/?linkid=2072338).

## <a name="do-you-support-mobile-device-management-mdm-and-microsoft-intune"></a>Há suporte para o gerenciamento de dispositivo móvel (MDM) e o Microsoft Intune?

Sim. Agora há suporte para configurar o Microsoft Edge no Windows 10 usando o Microsoft Intune e o MDM (gerenciamento de dispositivo móvel). Para obter mais informações, consulte [Configurar o Microsoft Edge usando o Microsoft Intune](./configure-edge-with-intune.md) e [Configurar o Microsoft Edge usando o gerenciamento de dispositivo móvel](./configure-edge-with-mdm.md).

## <a name="does-windows-server-update-services-wsus-support-the-initial-deployment-of-microsoft-edge"></a>O Windows Server Update Services (WSUS) dá suporte à implantação inicial do Microsoft Edge?

Sim. Há pacotes no [Catálogo de Atualizações](https://www.catalog.update.microsoft.com/Search.aspx?q=the%20new%20microsoft%20edge%20for%20windows) da Microsoft que podem ser usados para a implantação inicial de Microsoft Edge via WSUS. Após a implantação inicial, as atualizações automáticas são configuradas por padrão. Para saber mais, consulte [Atualizar no WSUS para o novo Microsoft Edge para Windows 10, versão 1809, 1903, 1909 e 2004: 29 de outubro de 2020](https://support.microsoft.com/help/4584642/update-in-wsus-for-the-new-microsoft-edge).

 As atualizações manuais podem ser feitas por meio de uma ferramenta de gerenciamento de configuração, como [ConfigMgr](/configmgr/apps/deploy-use/deploy-edge?bc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2fbreadcrumb%2ftoc.json&toc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2ftoc.json).

## <a name="are-initial-preferences-supported"></a>As Preferências Iniciais são suportadas?

Sim. Para obter mais informações, [consulte Configure Microsoft Edge using Initial Preferences settings for the first run](./initial-preferences-support-on-microsoft-edge-browser.md)

## <a name="see-also"></a>Consulte também

- [Página de aterrissagem da documentação do Microsoft Edge](./index.yml)
- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
  