---
title: Atualizações do Windows para dar suporte ao Microsoft Edge
ms.author: jtkim
author: dan-wesley
manager: srugh
ms.date: 11/17/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Atualizações do Windows para dar suporte ao Microsoft Edge.
ms.openlocfilehash: 52687fccfa8a0f98b742ce72b262682fdafb6d52
ms.sourcegitcommit: 2d3e2a7180e2df82b6345865c201ad64731cbda7
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/12/2022
ms.locfileid: "12582046"
---
# <a name="windows-updates-to-support-the-next-version-of-microsoft-edge"></a>Atualizações do Windows para oferecer suporte à próxima versão do Microsoft Edge

Este artigo descreve como o Windows será atualizado para oferecer suporte à próxima versão do Microsoft Edge

> [!IMPORTANT]
> Consulte a postagem [do blog da equipe de produto do Microsoft Edge](https://aka.ms/EdgeLegacyEOS) sobre o fim de serviço da Versão Prévia do Microsoft Edge.

> [!NOTE]
> Este artigo aplica-se ao canal estável do Microsoft Edge.

## <a name="microsoft-edge-and-the-windows-release-cycle"></a>Microsoft Edge e o ciclo de lançamento do Windows

A próxima versão do Microsoft Edge apresenta recursos de atualização mais frequentes e flexíveis. Como as versões do navegador não são vinculadas às versões principais do Windows, as alterações serão feitas no sistema operacional para garantir que a próxima versão do Microsoft Edge se adapte perfeitamente ao Windows. Como resultado, as atualizações de recursos serão lançadas em um ciclo de 4 semanas (aproximadamente). As atualizações de segurança e compatibilidade serão enviadas conforme necessário.

## <a name="updates-and-the-user-experience"></a>Atualizações e a experiência do usuário

As atualizações não mudam a experiência do usuário até que o canal estável da próxima versão do Microsoft Edge seja instalado. A instalação do Microsoft Edge Beta, Dev ou Canary não dispara alterações no Windows. Essas versões do navegador serão instaladas junto com os navegadores existentes.

Quando todas as atualizações forem aplicadas e o canal estável da próxima versão do Microsoft Edge for instalado no nível do sistema, as seguintes alterações entrarão em vigor no sistema:

- Todos os itens fixados, blocos e atalhos do menu Iniciar para a versão atual do Microsoft Edge serão migrados para a próxima versão do Microsoft Edge.
- Todos os itens fixados e atalhos da barra de tarefas da versão atual do Microsoft Edge serão migrados para a próxima versão do Microsoft Edge.
- A próxima versão do Microsoft Edge será fixada na barra de tarefas. Se a versão atual do Microsoft Edge já estiver fixada, ela será substituída.
- A próxima versão do Microsoft Edge adicionará um atalho à área de trabalho. Se a versão atual do Microsoft Edge já tiver um atalho, ela será substituída.
- A maioria dos protocolos que o Microsoft Edge processa por padrão será migrada para a próxima versão do Microsoft Edge.
- O Microsoft Edge atual ficará oculto em todas as superfícies da experiência do sistema operacional, incluindo configurações, todos os aplicativos e quaisquer caixas de diálogo de suporte de arquivo ou protocolo.
- Todas as tentativas de iniciar a versão atual do Microsoft Edge redirecionam para a próxima versão do Microsoft Edge.

  > [!NOTE]
  > As instalação no nível do usuário não dispararão os comportamentos anteriores.

Juntamente com as alterações anteriores, há alterações que ocorrem independentemente da instalação do canal estável da próxima versão do Microsoft Edge.

- O Microsoft Edge cancela o registro de livros e protocolos XML não compatíveis com a próxima versão do Microsoft Edge. Os usuários que tentarem abrir esses protocolos receberão uma caixa de diálogo solicitando que escolham um aplicativo padrão. Visite o Microsoft Store para ver nossas recomendações para leitores de livros eletrônicos.
  
## <a name="older-versions-of-windows"></a>Versões mais antigas do Windows

Para implantar o Microsoft Edge em um dispositivo que executa uma versão Windows mais antiga do Windows 10 RS4, use o [Configuration Manager](/mem/configmgr/apps/deploy-use/deploy-edge?bc=%2FDeployEdge%2Fbreadcrumb%2Ftoc.json&toc=%2FDeployEdge%2Ftoc.json), [Microsoft Intune](/mem/intune/apps/apps-windows-edge?bc=%2FDeployEdge%2Fbreadcrumb%2Ftoc.json&toc=%2FDeployEdge%2Ftoc.json) ou atualize para uma versão suportada do Windows 10. O artigo a seguir lista as versões com suporte do Windows 10 e Windows 11.

- [Versões com suporte do cliente Windows](/windows/release-health/supported-versions-windows-client)

> [!NOTE]
> Para Windows 10 RS4-20H1, implante um Windows LCU a partir de maio de 2021 ou mais novo para obter o Microsoft Edge. Para obter mais informações, consulte [ o histórico de atualização do Windows 10](https://support.microsoft.com/topic/windows-10-update-history-1b6aac92-bf01-42b5-b158-f80c6d93eb11)

> [!IMPORTANT]
> Se você precisar de atualizações não listadas aqui, execute o Windows Update ou entre em contato com o administrador.

## <a name="see-also"></a>Consulte também

- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Documentação do Microsoft Edge](./index.yml)
