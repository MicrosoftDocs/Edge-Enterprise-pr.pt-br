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
# <a name="disable-internet-explorer-11"></a>Desabilitar o Internet Explorer 11

Este artigo descreve como desabilitar o Internet Explorer 11 como um navegador autônomo em seu ambiente.

## <a name="prerequisites"></a>Pré-requisitos

As seguintes atualizações do Windows e do software Microsoft Edge são necessárias:

- Atualizações do Windows

  - Windows 10, versão 2004, Windows Server versão 2004, Windows 10, versão 20H2: [KB4598291](https://support.microsoft.com/topic/february-2-2021-kb4598291-os-builds-19041-789-and-19042-789-preview-6a766199-a4f1-616e-1f5c-58bdc3ca5e3b) ou mais tarde
  - Windows 10 versão 1909, Windows Server versão 1909: [KB4598298](https://support.microsoft.com/topic/january-21-2021-kb4598298-os-build-18363-1350-preview-02dfd9ba-91a2-1b82-dede-42f288c02511) ou mais tarde
  - Windows 10 versão 1809, Windows Server versão 1809, e Windows Server 2019: [KB4598296](https://support.microsoft.com/topic/january-21-2021-kb4598296-os-build-17763-1728-preview-4c0931ff-45b7-ff59-5e00-c03b5afb363d) ou mais tarde
  - Windows 10, versão 1607, Windows Server 2016: [KB4601318](https://support.microsoft.com/topic/february-9-2021-kb4601318-os-build-14393-4225-c5e3de6c-e3e6-ffb5-6197-48b9ce16446e) ou mais tarde
   - Windows 10 versão inicial (Julho 2015): [KB4601331](https://support.microsoft.com/office/february-9-2021%e2%80%94kb4601331-os-build-10240-18842-6227d078-fef3-8d67-27e0-1882e6cb79ff?ui=en-US&rs=en-US&ad=US) ou mais tarde
  - Windows 8.1: [KB4601384](https://support.microsoft.com/topic/february-9-2021-kb4601384-monthly-rollup-16bdbb75-dd4b-2910-abc5-7891c9756b96) ou mais tarde
  - Windows Server 2012: [KB4601348](https://support.microsoft.com/topic/february-9-2021-kb4601348-monthly-rollup-2c338c0c-73d6-fb80-cc91-f1a86e80db0c) ou mais tarde
  
- Canal Estável do Microsoft Edge


## <a name="overview"></a>Visão geral

Para organizações que exigem o Internet Explorer 11 (IE11) para compatibilidade herdada, o modo Internet Explorer (modo IE) no Microsoft Edge oferece uma experiência de navegador único e contínua. Os usuários podem acessar aplicativos legados de dentro do Microsoft Edge sem ter que voltar para o IE11.

Depois de configurar o modo IE, você pode desativar o IE11 como um navegador autônomo **sem afetar a funcionalidade do modo IE** em sua organização usando a política de grupo.

> [!NOTE]
> Se você precisa do aplicativo IE11 autônomo para sites específicos e deseja redirecionar todo o tráfego do navegador para o Microsoft Edge, pode configurar o [Envie todos os sites não incluídos na lista de sites para o Microsoft Edge](https://docs.microsoft.com/deployedge/edge-ie-mode-policies#redirect-sites-from-ie-to-microsoft-edge) política para redirecionar sites do IE para o Microsoft Edge.

## <a name="user-experience-after-redirecting-traffic-to-microsoft-edge"></a>Experiência do usuário após redirecionar o tráfego para o Microsoft Edge

Quando você ativa o **Desabilitar o Internet Explorer 11 como um navegador autônomo** política, todas as atividades do IE11 são redirecionadas para o Microsoft Edge e os usuários têm a seguinte experiência:

- O ícone do IE11 no menu Iniciar será removido, mas o da barra de tarefas permanecerá.
- Quando os usuários tentam iniciar atalhos ou associações de arquivos que usam o IE11, eles são redirecionados para abrir o mesmo arquivo/URL no Microsoft Edge.
- Quando os usuários tentam iniciar o IE11 invocando diretamente o binário iexplore.exe, o Microsoft Edge é iniciado.

Como parte da configuração da política para esta experiência, você pode opcionalmente mostrar uma mensagem de redirecionamento para cada usuário que tentar iniciar o IE11. Esta mensagem pode ser definida para exibir "Sempre" ou "Uma vez por usuário". Por padrão, a mensagem de redirecionamento mostrada na próxima captura de tela nunca é mostrada.

:::image type="content" source="media/edge-ie-disable-ie11/disable-ie-redirect-msg.png" alt-text="Alerta ao tentar abrir o IE após um redirecionamento para o Microsoft Edge estar ativo.":::

Se a sua Lista de Sites do Modo Enterprise contém aplicativos configurados para abrir no aplicativo IE11 e você desabilitar o IE11 com esta política, eles serão abertos no modo IE no Microsoft Edge.
> [!NOTE]
> Há um problema conhecido com o fluxo do usuário quando um site é configurado para abrir no IE11 e a política de desabilitação do IE11 é definida. O problema está sendo investigado ativamente.

## <a name="disable-internet-explorer-11-as-a-standalone-browser"></a>Desabilitar o Internet Explorer 11 como um navegador independente

Para desabilitar o Internet Explorer 11 usando a política de grupo, siga estas etapas:

1. Baixar e instalar o mais recente [Modelo de política Microsoft Edge](https://www.microsoft.com/en-us/business/download).
2. Abra o Editor de Política de Grupo.
3. Vá para ***Configuração do computador/Modelos administrativos/Componentes do Windows/Internet Explorer***. 
4. Duplo click **Desabilitar o Internet Explorer 11 como um navegador independente**.
5. Selecionar **Habilitar**.
6. Sob **Opções**, escolha um dos seguintes valores:

   - **Nunca** se você não quiser notificar os usuários de que o IE11 está desativado.
   - **Sempre** se você deseja notificar os usuários sempre que eles forem redirecionados do IE11.
   - **Uma vez por usuário** se desejar notificar os usuários apenas na primeira vez que forem redirecionados.

7. Clicar **OK** ou **Aplicar** para salvar esta configuração de política.

## <a name="see-also"></a>Ver também

- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Sobre o modo IE](https://docs.microsoft.com/deployedge/edge-ie-mode)
- [Informações adicionais sobre o Modo Empresarial](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)