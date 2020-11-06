---
title: Perguntas frequentes sobre o Edge na empresa
ms.author: jwhit
author: jwhit-MSFT
manager: laurawi
ms.date: 11/04/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Perguntas frequentes sobre a implantação do Microsoft Edge na empresa
ms.openlocfilehash: e689967cbad950e2969535bad0dd63d5d7081798
ms.sourcegitcommit: 12827458f6217f443128e826c1d18d36d401d03b
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "11154316"
---
# Perguntas frequentes sobre o Microsoft Edge na empresa

> [!NOTE]
> Este artigo se aplica ao Microsoft Edge versão 77 ou posterior.

## Como sei que versão do Microsoft Edge tenho?

No canto superior direito do Microsoft Edge, clique no ícone de elipse (**...**) e em **Configurações**. Escolha **Sobre o Microsoft Edge** para ver sua versão do Microsoft Edge.

## O Internet Explorer 11 continuará a receber atualizações?

Temos o compromisso de manter o Internet Explorer um navegador compatível, confiável e seguro. O Internet Explorer ainda é um componente do Windows e segue o ciclo de vida de suporte do sistema operacional no qual ele está instalado. Para obter mais informações, consulte as [Perguntas frequentes sobre ciclo de vida - Internet Explorer](https://support.microsoft.com/help/17454/). Embora continuemos a dar suporte e atualizar ao Internet Explorer, os recursos e as atualizações de plataforma mais recentes estarão disponíveis somente no Microsoft Edge.

## Posso executar a versão atual do Microsoft Edge (Versão Herdada do Microsoft Edge) lado a lado ao experimentar a nova versão?

Pode sim. Depois de 15 de janeiro de 2020, a nova versão do Microsoft Edge (com base em Chromium) será distribuída para dispositivos da edição Home e Pro que executam o Windows 10 versão 1803 ou mais recente. Os dispositivos ingressados em domínio serão excluídos dessa atualização. Para obter mais informações, consulte [Visão geral das atualizações do Microsoft Edge](https://docs.microsoft.com/deployedge/microsoft-edge-blocker-toolkit#overview). Você pode ter uma instalação lado a lado da Versão Herdada do Microsoft Edge enquanto avalia a próxima versão do Microsoft Edge. Para obter mais informações, consulte [Como acessar a versão antiga do Microsoft Edge](https://docs.microsoft.com/deployedge/microsoft-edge-sysupdate-access-old-edge). Além disso, cada um dos novos canais de Microsoft Edge também tem suporte para instalações lado a lado. Para obter mais informações, consulte [Visão geral dos canais do Microsoft Edge](https://docs.microsoft.com/deployedge/microsoft-edge-channels).

## O Microsoft Edge (Chromium-based) oferece suporte aos controles ActiveX ou BHOs, como o Silverlight ou o Java?

Não. O Microsoft Edge não oferece suporte aos controles ActiveX e BHOs, como Silverlight ou Java. Contudo, se você estiver executando aplicativos da Web que utilizam controles ActiveX, o BHOs, ou modos de documentos legados no Internet Explorer 11, você pode configurá-los para executar no modo IE no novo Microsoft Edge. Para obter mais informações, consulte [Configurar o modo IE no Microsoft Edge](https://docs.microsoft.com/DeployEdge/edge-ie-mode).

## Os favoritos serão transferidos da versão atual do Microsoft Edge ou terei que adicioná-los novamente?

Atualmente, o Microsoft Edge dá suporte à importação de instalações existentes do Microsoft Edge, do Chrome, do Internet Explorer e do Firefox (no Win10). As seguintes configurações têm suporte para importação: marcadores, histórico, senhas e autopreenchimento (pagamentos, endereços e formulários genéricos). Você pode optar por importar na primeira experiência de execução ou das configurações do navegador.  

## Qual é a diferença entre as versões/builds Estável, Beta, Dev e Canary?

O canal Estável da próxima versão do Microsoft Edge é o canal mais estável que oferecemos, com recursos focados em empresas prontos para você [experimentar e avaliar](https://aka.ms/EdgeEnterprise). O canal Beta permite que você valide a próxima versão Estável com um conjunto representativo de usuários. Os canais estável e Beta serão atualizados aproximadamente a cada seis semanas. Os canais Dev e Canary continuarão sendo atualizados semanalmente e diariamente, respectivamente. Os instaladores offline (MSIs e PKG) só estão disponíveis para canais estáveis, beta e de desenvolvimento. Para obter mais informações, consulte [Visão geral dos canais do Microsoft Edge](https://docs.microsoft.com/deployedge/microsoft-edge-channels).

## Que tipo de suporte a extensão tenho com a nova versão do Microsoft Edge?

O Microsoft Edge dá suporte a extensões dos [Complementos do Microsoft Edge Insider](https://go.microsoft.com/fwlink/?linkid=2081222) e da [Chrome Web Store](https://go.microsoft.com/fwlink/?linkid=2072338).

## Há suporte para o gerenciamento de dispositivo móvel (MDM) e o Microsoft Intune?

Sim. Agora há suporte para configurar o Microsoft Edge no Windows 10 usando o Microsoft Intune e o MDM (gerenciamento de dispositivo móvel). Para obter mais informações, consulte [Configurar o Microsoft Edge usando o Microsoft Intune](configure-edge-with-intune.md) e [Configurar o Microsoft Edge usando o gerenciamento de dispositivo móvel](configure-edge-with-mdm.md).

## O WSUS suporta a implantação inicial do novo Microsoft Edge?

Sim. Há pacotes no [Catálogo do Microsoft Update](https://www.catalog.update.microsoft.com/Search.aspx?q=the%20new%20microsoft%20edge%20for%20windows) que podem ser usados para a implantação inicial do novo Microsoft Edge por meio do WSUS. Após a implantação inicial, as atualizações automáticas são configuradas por padrão. Para saber mais, consulte [Atualizar no WSUS para o novo Microsoft Edge para Windows 10, versão 1809, 1903, 1909 e 2004: 29 de outubro de 2020](https://support.microsoft.com/help/4584642/update-in-wsus-for-the-new-microsoft-edge).

As atualizações manuais podem ser feitas por meio de uma ferramenta de gerenciamento de configuração, como a [ConfigMgr.](https://docs.microsoft.com/configmgr/apps/deploy-use/deploy-edge?toc=https://docs.microsoft.com/DeployEdge/toc.json&bc=https://docs.microsoft.com/DeployEdge/breadcrumb/toc.json).

## Consulte também

- [Página de aterrissagem da documentação do Microsoft Edge](https://docs.microsoft.com/DeployEdge/)
- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
