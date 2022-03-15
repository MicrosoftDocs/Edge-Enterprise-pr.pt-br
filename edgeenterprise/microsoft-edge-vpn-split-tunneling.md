---
title: Microsoft Edge vpn de túnel dividido para WebRTC
ms.author: juso
author: dan-wesley
manager: harneets
ms.date: 01/24/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Habilitar Microsoft Edge vpn de túnel dividido para WebRTC (Web Real-Time Comunicação)
ms.openlocfilehash: 73bd6494ebb95db23d2701cc9dab4023af28eb70
ms.sourcegitcommit: 556aca8dde42dd66364427f095e8e473b86651a0
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2022
ms.locfileid: "12445890"
---
# <a name="split-tunnel-vpn-support-for-webrtc-web-real-time-communication"></a>Suporte de VPN de túnel dividido para WebRTC (Web Real-Time Comunicação)
  
Este artigo descreve o suporte Microsoft Edge VPN de túnel dividido para WebRTC. Esse suporte permite que os clientes corporativos recebam o benefício do túnel dividido de VPN para tráfego ponto a ponto em Microsoft Edge. O túnel dividido de VPN melhora a qualidade de streaming de mídia ponto a ponto para os usuários e reduz a carga do servidor VPN.

> [!NOTE]
> Este artigo se aplica Microsoft Edge versão 96 ou posterior.

## <a name="what-is-vpn-split-tunneling-and-why-should-i-use-it"></a>O que é o túnel dividido de VPN e por que devo usá-lo?

O túnel dividido de VPN é um recurso que permite que os usuários usem duas redes diferentes para tráfego em vez de ter todo o tráfego roteado por meio de uma VPN. Windows suporte a esse recurso para aplicativos nativos, e o túnel dividido de VPN também é oferecido para aplicativos Microsoft 365 por túnel dividido de VPN em Windows. Para obter mais informações, consulte [Overview: VPN split tunneling with Office 365 - Microsoft 365 Enterprise](/microsoft-365/enterprise/microsoft-365-vpn-split-tunnel?view=o365-worldwide&preserve-view=true). Microsoft Edge também honrou a configuração de túnel dividido vpn, mas o suporte para o tráfego ponto a ponto estava ausente.

Ouvimos falar das necessidades dos clientes para rotear o tráfego de usuários ponto a ponto por meio de sua rede corporativa ou infraestrutura de nuvem pela VPN.Eles estavam frustrados com a qualidade das chamadas de conferência de vídeo de seus usuários em navegadores em comparação com aplicativos nativos.Conforme demonstrado pela experiência nativa, o túnel dividido de VPN para tráfego ponto a ponto pode melhorar a qualidade das chamadas de vídeo do usuário roteando-a por meio de conexões normais da Internet em vez de VPN. Ele também pode reduzir a carga geral do servidor VPN roteamento de tráfego designado de uma VPN. Microsoft Edge agora traz essa melhoria de tráfego ponto a ponto para clientes corporativos.

## <a name="how-to-configure-vpn-split-tunneling-on-microsoft-edge"></a>Como configurar o túnel dividido de VPN no Microsoft Edge

Para habilitar o túnel dividido de VPN e configurar as redes para seus usuários, recomendamos que você comece com as diretrizes em Implementar o túnel dividido de VPN para Office 365 [- Microsoft 365 Enterprise](/microsoft-365/enterprise/microsoft-365-vpn-implement-split-tunnel?view=o365-worldwide&preserve-view=true). Com a tabela de roteamento adequada configurada com base nas informações descritas no artigo anterior, você só precisa tomar a etapa adicional de habiltar a [política WebRtcRespectOsRoutingTableEnabled](/deployedge/microsoft-edge-policies#webrtcrespectosroutingtableenabled) . Essa política habilita o suporte Windows regras de tabela de roteamento do sistema operacional ao fazer conexões ponto a ponto via WebRTC. Agora você está pronto para fornecer uma experiência de streaming de mídia ponto a ponto aprimorada Microsoft Edge!

## <a name="see-also"></a>Consulte também

- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
