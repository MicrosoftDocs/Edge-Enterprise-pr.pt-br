---
title: Perguntas frequentes sobre o Microsoft Edge na empresa
ms.author: collw
author: dan-wesley
manager: seanlynd
ms.date: 08/30/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Perguntas frequentes sobre o Microsoft Edge na empresa
ms.openlocfilehash: 80a86dd2e058c34022cfbc832054dcf52a44526e
ms.sourcegitcommit: 3e3362b0c5c663df160e8e8f68a4c82564183b2d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/31/2022
ms.locfileid: "12740701"
---
# <a name="microsoft-edge-frequently-asked-questions"></a>Perguntas frequentes sobre o Microsoft Edge

Este artigo contém perguntas frequentes sobre o Microsoft Edge na empresa.

> [!NOTE]
> Este artigo se aplica ao Microsoft Edge versão 77 ou posterior.

## <a name="how-do-i-know-which-version-of-microsoft-edge-i-have"></a>Como sei que versão do Microsoft Edge tenho?

Selecione o ícone de reticências (**...**) no canto superior direito do Microsoft Edge e, em seguida, selecione **Configurações**. Escolha **Sobre o Microsoft Edge** para ver sua versão do Microsoft Edge.

## <a name="what-about-internet-explorer-11"></a>E o Internet Explorer 11?

>[!Note]
> O aplicativo da área de trabalho do Internet Explorer 11 foi [desativado e está sem suporte a partir de 15 de junho de 2022](https://aka.ms/IEJune15Blog) para determinadas versões do Windows 10.  
>
> - Você ainda pode acessar sites antigos e herdados que exigem o Internet Explorer com o modo Internet Explorer no Microsoft Edge. [Saiba como >](https://aka.ms/IEmodewebsite)
> - O aplicativo da área de trabalho do Internet Explorer 11 será redirecionado progressivamente para o navegador mais rápido e seguro Microsoft Edge e, por fim, será desabilitado por meio do Windows Update. [Desabilitar o IE hoje>](/deployedge/edge-ie-disable-ie11)  

## <a name="does-microsoft-edge-support-activex-controls-or-browser-helper-objects-like-silverlight-or-java"></a>O Microsoft Edge dá suporte a controles ActiveX ou objetos auxiliares do navegador, como Silverlight ou Java?

Não. O Microsoft Edge não dá suporte a controles ActiveX ou BHOs (Objetos de Ajuda do Navegador), como Silverlight ou Java. No entanto, se você estiver executando aplicativos Web que usam controles ActiveX, BHOs ou modos de documento herdados no Internet Explorer 11, poderá configurá-los para serem executados no modo IE no Microsoft Edge. Para obter mais informações, consulte [Configurar o modo IE no Microsoft Edge](./edge-ie-mode.md).

## <a name="will-favorites-be-ported-over-from-the-current-version-of-microsoft-edge-or-will-i-have-to-re-add-them"></a>Os favoritos serão portados da versão atual do Microsoft Edge ou eu vou ter que adicioná-los novamente?

O Microsoft Edge dá suporte à importação de instalados existentes do Microsoft Edge, Chrome, Internet Explorer e Firefox (no Win10). As configurações a seguir têm suporte para importação: Indicadores, Histórico, Senhas e Preenchimento Automático (pagamentos, endereços e formulários genéricos). Você pode optar por importar na primeira experiência de execução ou das configurações do navegador.

## <a name="whats-the-difference-between-the-stable-beta-dev-and-canary-channelsbuilds"></a>Qual é a diferença entre as versões/builds Estável, Beta, Dev e Canary?

O canal estável do Microsoft Edge é o canal mais estável que oferecemos com recursos voltados para a empresa prontos para você fazer o piloto e [avaliar em toda](https://aka.ms/EdgeEnterprise) a sua organização. O canal Beta permite que você valide a próxima versão Estável com um conjunto representativo de usuários. Os canais Estável e Beta são atualizados aproximadamente a cada quatro semanas. Os canais Dev e Canary continuam sendo atualizados semanalmente e diariamente, respectivamente. Os instaladores offline (MSIs e arquivos PKG) estão disponíveis apenas para canais Estáveis, Beta e Dev. Para obter mais informações, consulte [Visão geral dos canais do Microsoft Edge](./microsoft-edge-channels.md).

## <a name="what-kind-of-extension-support-do-i-have-with-microsoft-edge"></a>Que tipo de suporte de extensão tenho com o Microsoft Edge?

O Microsoft Edge dá suporte a extensões [do Microsoft Edge Insider Addons](https://go.microsoft.com/fwlink/?linkid=2081222) e da [Chrome Web Store](https://go.microsoft.com/fwlink/?linkid=2072338).

## <a name="do-you-support-mobile-device-management-mdm-and-microsoft-intune"></a>Há suporte para o gerenciamento de dispositivo móvel (MDM) e o Microsoft Intune?

Sim. Agora há suporte para configurar o Microsoft Edge no Windows 10 usando o Microsoft Intune e o MDM (gerenciamento de dispositivo móvel). Para obter mais informações, consulte [Configurar o Microsoft Edge usando o Microsoft Intune](./configure-edge-with-intune.md) e [Configurar o Microsoft Edge usando o gerenciamento de dispositivo móvel](./configure-edge-with-mdm.md).

## <a name="does-windows-server-update-services-wsus-support-the-initial-deployment-of-microsoft-edge"></a>O Windows Server Update Services (WSUS) dá suporte à implantação inicial do Microsoft Edge?

Sim. Há pacotes no Catálogo [do Microsoft Update que](https://www.catalog.update.microsoft.com/Search.aspx?q=the%20new%20microsoft%20edge%20for%20windows) podem ser usados para a implantação inicial do Microsoft Edge por meio do WSUS. Após a implantação inicial, as atualizações automáticas são configuradas por padrão. Para saber mais, consulte [Atualizar no WSUS para o novo Microsoft Edge para Windows 10, versão 1809, 1903, 1909 e 2004: 29 de outubro de 2020](https://support.microsoft.com/help/4584642/update-in-wsus-for-the-new-microsoft-edge).

 As atualizações manuais podem ser feitas por meio de uma ferramenta de gerenciamento de configuração, como [o ConfigMgr](/configmgr/apps/deploy-use/deploy-edge?bc=%2fDeployEdge%2fbreadcrumb%2ftoc.json&toc=%2fDeployEdge%2ftoc.json).

## <a name="are-initial-preferences-supported"></a>Há suporte para preferências iniciais?

Sim. Para obter mais informações, consulte [Configurar o Microsoft Edge usando as configurações de Preferências Iniciais para a primeira execução](./initial-preferences-support-on-microsoft-edge-browser.md)

## <a name="see-also"></a>Consulte também

- [Página de aterrissagem da documentação do Microsoft Edge](./index.yml)
- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
  
