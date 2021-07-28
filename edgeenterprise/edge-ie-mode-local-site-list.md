---
title: Lista de sites locais para modo IE
ms.author: shisub
author: AndreaLBarr
manager: srugh
ms.date: 07/20/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Saiba como habilitar listas de sites locais e acesso fácil ao modo IE
ms.openlocfilehash: 0c79622a1f96cad83a2436f5e79e69914f4a2c40
ms.sourcegitcommit: 9088e839e82d80c72460586e9af0610c6ca71b83
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/23/2021
ms.locfileid: "11676130"
---
## <a name="local-site-list-for-ie-mode"></a>Lista de sites locais para modo IE

>[!Note]
> O aplicativo de área de trabalho Internet Explorer 11 será desativado e ficará sem suporte em 15 de junho de 2022 (para obter uma lista do que está no escopo, [consulte as Perguntas frequentes](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/internet-explorer-11-desktop-app-retirement-faq/ba-p/2366549)). Os mesmos aplicativos e sites do IE11 que você usa hoje podem abrir no Microsoft Edge com o modo Internet Explorer. [Saiba mais aqui](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/).

Este artigo explica como configurar o acesso fácil ao modo Internet Explorer (modo IE) e permitir o uso de listas de sites locais em sua organização.

> [!NOTE]
> Este artigo se aplica Microsoft Edge versão 92 ou posterior.

### <a name="prerequisites"></a>Pré-requisitos

1. Atualizações do Windows

- Windows 10, versão 1909 - [KB5003698](https://support.microsoft.com/topic/june-15-2021-kb5003698-os-build-18363-1645-preview-1ecf117e-1f89-40f9-a0a5-ed5766737620) ou posterior  

- Windows 10, versão 2004; Windows 10, versão 20H2 e Windows 10, versão 21H1 – [KB5003690](https://support.microsoft.com/topic/june-21-2021-kb5003690-os-builds-19041-1081-19042-1081-and-19043-1081-preview-11a7581f-2a01-47d5-ba12-431709ee2248) ou posterior

2. Microsoft Edge versão 92 (92.0.925.0 ou posterior)

## <a name="overview"></a>Visão Geral

O modo IE é alimentado pela configuração da lista de sites Enterprise Modo. Enquanto você está identificando e configurando sites na lista de sites para usar o modo IE, os usuários não precisam mais esperar ou voltar para o aplicativo IE11 autônomo.

A partir Microsoft Edge versão 92, o acesso repetido a sites de modo *IE* não configurado é mais fácil. Os usuários podem recarregar sites no modo IE. Eles podem adicionar esses sites à lista de sites locais para renderizar automaticamente no modo IE por um período de 30 dias, enquanto a lista de sites da organização é atualizada. Quando [o IE11 é](/deployedge/edge-ie-disable-ie11) desabilitado em seu ambiente, seus usuários não são mais dependentes somente da lista de sites da organização.

Você pode configurar essa experiência por meio de políticas de grupo para sua organização.

Observação: *um* site não configurado é aquele que requer o modo IE, mas não está configurado para abrir no modo IE na lista de sites do modo Enterprise Modo.

## <a name="local-site-list-experience"></a>Experiência de lista de sites locais

Para habilitar a experiência de lista de sites locais, os usuários podem ir para a *URL* edge://settings/defaultBrowser e definir Permitir que sites sejam recarregados no modo **Internet Explorer** como **Permitir**.

:::image type="content" source="media/Edge-hybrid-IE-mode/internet-explorer-compatibilitiy.png" alt-text="Compatibilidade com o Internet Explorer":::

>[! Observação:]  

>1. Se você habilitar o teste do modo IE por meio da política *InternetExplorerIntegrationTestingAllowed,* você verá essa configuração, mas ela será esnobada, a menos que você habilita explicitamente a política *InternetExplorerIntegrationReloadInIEModeAllowed.*  
>2. Se **Permitir que sites** sejam recarregados no modo Internet Explorer esteja definido como **Padrão,** os usuários poderão recarregar sites no modo IE se eles têm uso existente do Internet Explorer 11.  

Quando essa configuração estiver habilitada, os usuários poderão recarregar um site no modo IE selecionando Configurações e mais (o ícone de releições **...)**> Recarregar no modo Internet Explorer . Os usuários também podem selecionar a guia Recarregar no modo **Internet Explorer** quando clicam com o botão direito do mouse em uma guia ou escolhem Abrir link na nova guia modo **Internet Explorer** quando clicam com o botão direito do mouse em um link.

:::image type="content" source="media/Edge-hybrid-IE-mode/reload-in-internet-exploror-mode-screenshot.png" alt-text="Recarregar no modo Internet Explorer":::

O **ícone Recarregar no modo Internet Explorer** pode ser fixado na barra de ferramentas. O botão da barra de ferramentas permite que os usuários entrem e saiam facilmente do modo IE e podem ser gerenciados por meio da URL *edge://settings/appearance.*

:::image type="content" source="media/Edge-hybrid-IE-mode/reload-in-internet-exploror-mode-icon-screenshot.png" alt-text="Recarregar no ícone do modo internet Explorer":::

>[!Note]
>Se o usuário estiver em um site que já esteja na lista de sites de modo Enterprise da organização, as opções para Recarregar no modo Internet Explorer (ou Sair) estarão visíveis, mas acinzentadas.

Quando a opção é selecionada, o site é recarregado no modo IE. O ícone do indicador do modo IE fica visível à esquerda da barra de endereços e o flyout mostra uma opção que os usuários podem alternar para Abrir a página no modo Internet Explorer da próxima vez. Isso adiciona a página específica em que o usuário está na lista de sites local e será aberta automaticamente no modo IE pelos próximos 30 dias.

:::image type="content" source="media/Edge-hybrid-IE-mode/site-has-been-reloaded-in-ie-mode-screenshot.png" alt-text="Esta página está aberta no modo Internet Explorer":::

Depois que um site for recarregado no modo IE, as navegaçãos "na página" permanecerão no modo IE (por exemplo, um link, um script ou um formulário na página ou um redirecionamento do lado do servidor de outra navegação "na página").  

Enquanto estiver no modo IE, os usuários verão um banner indicando que estão no modo IE, a opção para Deixar o modo IE e fixar o ícone do modo IE na barra de ferramentas (se ainda não estiver fixado).

:::image type="content" source="media/Edge-hybrid-IE-mode/ie-mode-banner-screenshot.png" alt-text="Faixa de modo IE":::

Os usuários podem optar por sair do modo IE usando o botão Deixar na faixa, o ícone de modo IE fixado ou Configurações e mais (o ícone de releições **...)**> modo Sair do Internet Explorer , caso contrário, o Microsoft Edge sairá automaticamente do modo IE quando ocorrer uma navegação que não seja "na página" (por exemplo, usando a barra de endereços, o botão voltar ou um link favorito).

As entradas permanecem na lista de sites locais por um período padrão de 30 dias. Recomendamos que você configure sites herdado para sua organização na lista Enterprise site do modo de usuário. A lista de sites locais garantirá que os usuários possam continuar seu fluxo de trabalho sem serem interrompidos enquanto a lista de sites da organização é atualizada. No dia 31, quando os usuários navegarem até o site, eles verão um banner explicando que o site não será mais carregado no modo IE. Os usuários podem adicioná-lo de volta à lista de sites local, se assim escolherem.

:::image type="content" source="media/Edge-hybrid-IE-mode/page-will-no-longer-load-in-ie-mode-screenshot.png" alt-text="A página não será mais carregada no modo IE":::

## <a name="policies-to-configure-the-use-of-local-site-lists-for-ie-mode"></a>Políticas para configurar o uso de listas de sites locais para o modo IE

Duas políticas de grupo estão disponíveis para configurar a experiência de lista de sites local Microsoft Edge. Estas políticas são:

### *<a name="policy-internetexplorerintegrationreloadiniemodeallowed"></a>Política: InternetExplorerIntegrationReloadInIEModeAllowed*

Essa política corresponde à configuração Microsoft Edge "Permitir que os sites sejam recarregados no modo Internet Explorer". Você pode acessar essa configuração indo para o URL *edge://settings/defaultbrowser*.

- Se você habilitar essa política, os usuários poderão recarregar um site no modo IE selecionando Configurações e muito mais **(o**ícone de releições ... > Recarregar no modo Internet Explorer . Os usuários também podem selecionar a guia Recarregar no modo **Internet Explorer** quando clicam com o botão direito do mouse em uma guia ou escolhem Abrir link na nova guia modo **Internet Explorer** quando clicam com o botão direito do mouse em um link.
Os usuários podem, opcionalmente, Microsoft Edge usar o modo IE para o site no futuro. Essa opção será lembrada por um padrão de 30 dias e poderá ser gerenciada usando a política *InternetExplorerIntegrationLocalSiteListExpirationDays*.

- Se você desabilitar essa política, os usuários não terão permissão para recarregar um site não configurado no modo IE.

- Se você não configurar essa política, mostraremos aos usuários opções para recarregar sites não configurados no modo IE, dependendo do uso recente do Internet Explorer 11.

Observe que essa política tem precedência sobre como você configurou a [política InternetExplorerIntegrationTestingAllowed](/deployedge/microsoft-edge-policies#internetexplorerintegrationtestingallowed) e essa política será desabilitada.

### *<a name="policy-internetexplorerintegrationlocalsitelistexpirationdays"></a>Política: InternetExplorerIntegrationLocalSiteListExpirationDays*

Essa política pode ser usada para ajustar o número de dias em que um site permanece na lista de sites local para usuários.  

- Se você desabilitar ou não configurar essa política, será usado um valor padrão de 30 dias.

- Se você habilitar a política, deverá inserir um valor entre 0 e 90 dias para manter o site na lista de sites local de um usuário.

Essa política não terá efeito se você desabilitou a *política InternetExplorerIntegrationReloadInIEModeAllowed.*

**Observação:**

No momento, a lista de sites locais não é sincronizada entre dispositivos. Essa melhoria está atualmente em nosso backlog e atualizaremos quando isso se tornar disponível.

## <a name="see-also"></a>Consulte também

Desabilitar o Internet Explorer 11 - [Desabilitar o Internet Explorer 11 | Microsoft Docs](/deployedge/edge-ie-disable-ie11)

Configurar políticas de modo IE - Configurar políticas de [modo IE | Microsoft Docs](/deployedge/edge-ie-mode-policies)

