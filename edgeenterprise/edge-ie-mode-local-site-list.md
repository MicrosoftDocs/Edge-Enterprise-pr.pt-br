---
title: Lista de sites locais para o modo Internet Explorer (IE)
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 07/06/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Saiba como habilitar listas de sites locais e configurar o acesso fácil ao modo IE
ms.openlocfilehash: 66d894e82203a1f3ed7bae4cd14dc5ec44982516
ms.sourcegitcommit: ef95039fbc92a3310f420b1c26fc4bed5b2e43b1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/07/2022
ms.locfileid: "12635718"
---
# <a name="configure-local-site-list-for-internet-explorer-ie-mode"></a>Configurar a lista de sites locais para o modo Internet Explorer (IE)

>[!Note]
> O aplicativo da área de trabalho do Internet Explorer 11 foi [desativado e está sem suporte a partir de 15 de junho de 2022](https://aka.ms/IEJune15Blog) para determinadas versões do Windows 10.  
>
> - Você ainda pode acessar sites antigos e herdados que exigem o Internet Explorer com o modo Internet Explorer no Microsoft Edge. [Saiba como >](https://aka.ms/IEmodewebsite)
> - O aplicativo da área de trabalho do Internet Explorer 11 será redirecionado progressivamente para o navegador mais rápido e seguro Microsoft Edge e, por fim, será desabilitado por meio do Windows Update. [Desabilitar o IE hoje>](/deployedge/edge-ie-disable-ie11)  

Este artigo explica como configurar o acesso fácil ao modo Internet Explorer (modo IE) e permitir o uso de listas de sites locais em sua organização.

> [!NOTE]
> Este artigo se aplica ao Microsoft Edge versão 92 ou posterior.

## <a name="prerequisites"></a>Pré-requisitos

1. Atualizações do Windows

   - Windows 11

   - Windows 10, versão 1909 – [KB5003974](https://support.microsoft.com/topic/kb5003974-servicing-stack-update-for-windows-10-version-1909-june-15-2021-0e65680e-2d21-4a31-b97a-e24c022aeccf) e [KB5003698](https://support.microsoft.com/topic/june-15-2021-kb5003698-os-build-18363-1645-preview-1ecf117e-1f89-40f9-a0a5-ed5766737620) ou posterior

   - Windows 10, versão 2004; Windows 10, versão 20H2 e Windows 10, versão 21H – [KB5005260](https://support.microsoft.com/topic/kb5005260-servicing-stack-update-for-windows-10-version-2004-20h2-and-21h1-august-10-2021-ec4c5daa-2cec-4b06-be93-037f150fe3ba) e [KB5005101](https://support.microsoft.com/topic/september-1-2021-kb5005101-os-builds-19041-1202-19042-1202-and-19043-1202-preview-82a50f27-a56f-4212-96ce-1554e8058dc1) ou posterior

2. Microsoft Edge versão 92 (92.0.902.55 ou posterior)

> [!IMPORTANT]
> Não há suporte para esse recurso de lista de sites local Windows Server 2016 no momento.

## <a name="overview"></a>Visão geral

O modo IE é alimentado pela configuração da Lista de Sites do Modo Empresarial. Enquanto você estiver identificando e configurando sites na lista de sites para usar o modo IE, os usuários não precisam mais esperar ou voltar para o aplicativo IE11 autônomo.

A partir da versão 92 do Microsoft Edge, o acesso repetido a sites *do* modo IE não configurado é mais fácil. Os usuários podem recarregar sites no modo IE. Eles podem adicionar esses sites à lista de sites locais para renderizar automaticamente no modo IE por 30 dias, enquanto a lista de sites da organização é atualizada. Quando [o IE11 está](/deployedge/edge-ie-disable-ie11) desabilitado em seu ambiente, os usuários não dependem mais apenas da lista de sites da organização.

Você pode configurar essa experiência por meio de políticas de grupo para sua organização.

> [!NOTE]
> Um *site não configurado é* aquele que requer o modo IE, mas não está configurado para abrir no modo IE na Lista de Sites do Modo Empresarial.

## <a name="enable-the-local-site-list-experience"></a>Habilitar a experiência de lista de sites local

Para habilitar a experiência de lista de sites locais, os usuários podem acessar *a url edge://settings/defaultBrowser* e definir Permitir que sites sejam recarregados no modo **Internet Explorer** como **Permitir**.

:::image type="content" source="media/Edge-hybrid-IE-mode/internet-explorer-compatibilitiy.png" alt-text="Compatibilidade com o Internet Explorer":::

>[!Note]  
>
>1. Se você habilitou o teste de modo IE por meio da política *InternetExplorerIntegrationTestingAllowed* , verá essa configuração, mas ela ficará esmaecada, a menos que você habilite explicitamente a política *InternetExplorerIntegrationReloadInIEModeAllowed* .
>
>2. Se **Permitir que sites** sejam recarregados no modo Internet Explorer estiver definido como **Padrão, os** usuários poderão recarregar sites no modo IE se tiverem o uso existente do Internet Explorer 11.  

Quando essa configuração estiver habilitada, os usuários poderão recarregar um site no modo IE selecionando Configurações e muito mais (o ícone de reticências **...) > Recarregar no modo Internet Explorer**. Os usuários também podem selecionar a guia Recarregar no modo **Internet Explorer** quando clicam com o botão direito do mouse em uma guia ou escolhem Abrir link na nova guia modo **Internet Explorer** quando clicam com o botão direito do mouse em um link.

:::image type="content" source="media/Edge-hybrid-IE-mode/reload-in-internet-exploror-mode-screenshot.png" alt-text="Recarregar no modo Internet Explorer":::

O **ícone Recarregar no modo Internet Explorer** pode ser fixado na barra de ferramentas. O botão da barra de ferramentas permite que os usuários entrem e saiam facilmente do modo IE e possam ser gerenciados por *meio edge://settings/appearance URL* .

:::image type="content" source="media/Edge-hybrid-IE-mode/reload-in-internet-exploror-mode-icon-screenshot.png" alt-text="Recarregue no ícone do Modo Internet Explorer":::

>[!Note]
>Se o usuário estiver em um site que já esteja na Lista de Sites do Modo Empresarial da organização, as opções para recarregar no modo (ou sair) do Internet Explorer estarão visíveis, mas esmaecidos.

Quando a opção é selecionada, o site é recarregado no modo IE. O ícone do indicador do modo IE é visível à esquerda da barra de endereços. O submenu mostra uma opção que os usuários podem alternar para Abrir a página no modo de exibição Compatibilidade, que adiciona a página à lista de configurações do modo de exibição de Compatibilidade do Internet Explorer e atualiza a página.**** Além disso, há uma opção que os usuários podem alternar para **Abrir a página no modo Internet Explorer** da próxima vez. Isso adiciona a página específica na qual o usuário está na lista de sites local e será aberto automaticamente no modo IE nos próximos 30 dias.

:::image type="content" source="media/Edge-hybrid-IE-mode/site-has-been-reloaded-in-ie-mode-screenshot2.png" alt-text="Esta página está aberta no Modo Internet Explorer":::

Depois que um site for recarregado no modo IE, a navegação "na página" permanecerá no modo IE (por exemplo, um link, um script, um formulário na página ou um redirecionamento do lado do servidor de outra navegação "na página").  

Enquanto estiver no modo IE, os usuários verão uma faixa indicando que estão no modo IE, a opção de sair do modo IE e fixar o ícone do modo IE na barra de ferramentas (se ele ainda não estiver fixado).

:::image type="content" source="media/Edge-hybrid-IE-mode/ie-mode-banner-screenshot.png" alt-text="Faixa do modo IE":::

Os usuários podem optar por sair do modo IE usando o botão Sair na faixa, o ícone do modo IE fixado ou Configurações e muito mais (o ícone de reticências **...) >** Sair do modo Internet Explorer, caso contrário, o Microsoft Edge sairá automaticamente do modo IE quando ocorrer uma navegação que não seja "na página" (por exemplo, usando a barra de endereços, o botão Voltar,  ou um link favorito).

As entradas permanecem na lista de sites locais por um período padrão de 30 dias. Recomendamos que você configure sites herdados para sua organização na Lista de Sites do Modo Empresarial. A lista de sites locais garantirá que os usuários possam continuar seu fluxo de trabalho sem serem interrompidos enquanto a lista de sites da organização é atualizada. No dia 31, quando os usuários navegarem até o site, eles verão uma faixa explicando que o site não será mais carregado no modo IE. Os usuários podem adicioná-lo novamente à lista de sites locais, se assim escolherem.

:::image type="content" source="media/Edge-hybrid-IE-mode/page-will-no-longer-load-in-ie-mode-screenshot.png" alt-text="A página não será mais carregada no modo IE":::

## <a name="policies-to-configure-the-use-of-local-site-lists-for-ie-mode"></a>Políticas para configurar o uso de listas de sites locais para o modo IE

Duas políticas de grupo estão disponíveis para configurar a experiência de lista de sites locais no Microsoft Edge. Estas políticas são:

### <a name="policy-internetexplorerintegrationreloadiniemodeallowed"></a>Política: InternetExplorerIntegrationReloadInIEModeAllowed

Essa política corresponde à configuração do Microsoft Edge "Permitir que os sites sejam recarregados no modo Internet Explorer". Você pode acessar essa configuração indo para o URL *edge://settings/defaultbrowser*.

- Se você habilitar essa política, os usuários poderão recarregar um site no modo IE selecionando Configurações e muito mais (o ícone de reticências **... > Recarregar no modo Internet Explorer**. Os usuários também podem selecionar a guia Recarregar no modo **Internet Explorer** quando clicarem com o botão direito do mouse em uma guia ou escolher Abrir link na nova guia do modo **Internet Explorer** quando clicarem com o botão direito do mouse em um link.
Opcionalmente, os usuários podem dizer ao Microsoft Edge para usar o modo IE para o site no futuro. Essa opção será lembrada por um padrão de 30 dias e poderá ser gerenciada usando a política *InternetExplorerIntegrationLocalSiteListExpirationDays*.

- Se você desabilitar essa política, os usuários não poderão recarregar um site não configurado no modo IE.

- Se você não configurar essa política, mostraremos aos usuários opções para recarregar sites não configurados no modo IE, dependendo do uso recente do Internet Explorer 11.

Observe que essa política tem precedência sobre como você configurou a política [InternetExplorerIntegrationTestingAllowed](/deployedge/microsoft-edge-policies#internetexplorerintegrationtestingallowed) e essa política será desabilitada.

### <a name="policy-internetexplorerintegrationlocalsitelistexpirationdays"></a>Política: InternetExplorerIntegrationLocalSiteListExpirationDays

Essa política pode ser usada para ajustar o número de dias que um site permanece na lista de sites locais para os usuários.  

- Se você desabilitar ou não configurar essa política, um valor padrão de 30 dias será usado.

- Se você habilitar a política, deverá inserir um valor entre 0 e 90 dias para manter o site na lista de sites locais de um usuário.

Essa política não terá efeito se você desabilitou a *política InternetExplorerIntegrationReloadInIEModeAllowed* .

> [!NOTE]
> Atualmente, a lista de sites locais não é sincronizada entre dispositivos. Essa melhoria está atualmente em nossa lista de pendências e atualizaremos esse recurso quando ele estiver disponível.

## <a name="see-also"></a>Consulte também

- Desabilitar o Internet Explorer 11 – [Desabilitar o Internet Explorer 11](/deployedge/edge-ie-disable-ie11)
- Configurar políticas de modo IE – [Configurar políticas de modo IE](/deployedge/edge-ie-mode-policies)
