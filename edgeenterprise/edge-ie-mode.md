---
title: O que é o modo Internet Explorer?
ms.author: kvice
author: dan-wesley
manager: laurawi
ms.date: 06/28/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Saiba como o modo Internet Explorer no Microsoft Edge fornece acesso a sites que precisam do Internet Explorer 11 e acesso a sites modernos.
ms.openlocfilehash: 5903e8a50f0afa50daa5921f3c97f3dbcbf0c3c5
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/09/2021
ms.locfileid: "11641387"
---
# <a name="what-is-internet-explorer-ie-mode"></a>O que é o modo Internet Explorer (IE)?

>[!Note]
> O aplicativo de área de trabalho Internet Explorer 11 será desativado e ficará sem suporte em 15 de junho de 2022 (para obter uma lista do que está no escopo, [consulte as Perguntas frequentes](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/internet-explorer-11-desktop-app-retirement-faq/ba-p/2366549)). Os mesmos aplicativos e sites do IE11 que você usa hoje podem abrir no Microsoft Edge com o modo Internet Explorer. [Saiba mais aqui](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/).

Criamos o modo Internet Explorer (IE) no Microsoft Edge para organizações que ainda precisam do Internet Explorer 11 para compatibilidade com sites existentes, mas também precisam de um navegador moderno. Esse recurso torna mais fácil para as organizações usarem um navegador, para web/aplicativos legados ou para web/app moderno. Este artigo fornece uma introdução ao uso do Microsoft Edge com o modo IE.

> [!NOTE]
> Este artigo se aplica ao Microsoft Edge versão 77 ou posterior.

## <a name="what-is-ie-mode"></a>O que é o modo IE?

O modo IE no Microsoft Edge facilita o uso de todos os sites de que sua organização precisa em um único navegador. Ele usa o mecanismo integrado Chromium para sites modernos e o mecanismo Trident MSHTML do Internet Explorer 11 (IE11) para sites herdados.

Quando um site é carregado no modo IE, o indicador do logotipo do IE é exibido no lado esquerdo da barra de navegação. Você pode clicar no indicador do logotipo do IE para exibir informações adicionais, como mostrado:

  ![Indicador do logotipo do IE](./media/ie-mode/ie-logo-indicator1.png)

Somente os sites que você configurou especificamente (via política) usarão o modo IE; todos os outros sites serão renderizados como sites da Web modernos. Para um site usar o modo IE, você precisa:

- Listar o site no XML da Lista de Sites do Modo Corporativo definido em uma destas políticas:
  - Microsoft Edge 78 ou posterior, "Configurar a Lista de Sites do Modo Empresarial"
  - Internet Explorer, "Usar a lista de sites do IE do modo Empresarial"
  > [!NOTE]
  > Processamos apenas uma lista de sites no modo corporativo. A política de lista de sites do Microsoft Edge tem precedência sobre a política de lista de sites do Internet Explorer.
- Todos os sites da Intranet quando a diretiva de grupo **Enviar todos os sites da intranet para o Internet Explorer** está ativada (Microsoft Edge 77 ou posterior).

### <a name="ie-mode-supports-the-following-internet-explorer-functionality"></a>O modo IE oferece suporte à seguinte funcionalidade do Internet Explorer

- Todos os modos de documento e modos corporativos.
- Controle ActiveX (como por exemplo, Java e Silverlight)
- Objetos Auxiliares de Navegador 
- Configurações do Internet Explorer e Políticas de Grupo que afetam as configurações da zona de segurança e o Modo Protegido
- As ferramentas de desenvolvedor F12 para o IE, quando iniciadas com o [IEChooser](/office/dev/add-ins/testing/debug-add-ins-using-f12-developer-tools-on-windows-10)
- Extensões do Microsoft Edge (extensões que interagem com o conteúdo da página do IE diretamente não têm suporte.)

### <a name="ie-mode-doesnt-support-the-following-internet-explorer-functionality"></a>O modo IE não oferece suporte à seguinte funcionalidade do Internet Explorer

- Barras de ferramentas do Internet Explorer
- Configurações do Internet Explorer e Políticas de Grupo que afetam o menu de navegação (por exemplo, mecanismos de pesquisa e home pages).
- Ferramentas de desenvolvedor F12 do IE11 ou Microsoft Edge

## <a name="prerequisites"></a>Pré-requisitos

Os pré-requisitos a seguir se aplicam ao uso do Microsoft Edge com o modo IE.

> [!IMPORTANT]
> Para garantir o sucesso, instale as atualizações mais recentes para o Windows e o Microsoft Edge. Se isso não for feito, provavelmente o modo IE deixará de funcionar.

1. As atualizações mínimas do sistema para os sistemas operacionais listados na tabela a seguir.

 | Sistema operacional | Versão       | Atualizações |
 |------------------|---------------|---------|
 | Windows 10       | 1909 ou posterior |         |
 | Windows 10       | 1903          | [KB4501375](https://support.microsoft.com/help/4501375/windows-10-update-kb4501375) ou posterior |
 | Windows Server   | 1903          | [KB4501375](https://support.microsoft.com/help/4501375/windows-10-update-kb4501375) ou posterior |
 | Windows 10       | 1809          | [KB4501371](https://support.microsoft.com/help/4501371/windows-10-update-kb4501371) ou posterior |
 | Windows Server   | 1809          | [KB4501371](https://support.microsoft.com/help/4501371/windows-10-update-kb4501371) ou posterior |
 | Windows Server   | 2019          | [KB4501371](https://support.microsoft.com/help/4501371/windows-10-update-kb4501371) ou posterior |
 | Windows 10       | 1803          | [KB4512509](https://support.microsoft.com/help/4512509/windows-10-update-kb4512509) ou posterior |
 | Windows 10       | 1709          | [KB4512494](https://support.microsoft.com/help/4512494/windows-10-update-kb4512494) ou posterior |
 | Windows 10       | 1607          | [KB4516061](https://support.microsoft.com/help/4516061/windows-10-update-kb4516061) ou posterior |
 | Windows Server   | 2016          | [KB4516061](https://support.microsoft.com/help/4516061/windows-10-update-kb4516061) ou posterior |
 | Windows 10       | versão inicial, julho de 2015 | [KB4520011](https://support.microsoft.com/help/4520011/windows-10-update-kb4520011) ou posterior |
 | Windows 8       | 8.1              | [KB4507463](https://support.microsoft.com/help/4507463/july-16-2019-kb4507463-os-build-preview-of-monthly-rollup) ou posterior; [KB4511872](https://support.microsoft.com/help/4511872/cumulative-security-update-for-internet-explorer) ou posterior |
 | Windows Server   | 2012 R2       | [KB4507463](https://support.microsoft.com/help/4507463/july-16-2019-kb4507463-os-build-preview-of-monthly-rollup) ou posterior; [KB4511872](https://support.microsoft.com/help/4511872/cumulative-security-update-for-internet-explorer) ou posterior |
 | Windows 8  | Incorporado            | Instale [KB4492872](https://support.microsoft.com/help/4492872/update-for-internet-explorer-april-16-2019) para atualizar para o Internet Explorer 11; depois instale [KB4507447](https://support.microsoft.com/help/4507447/windows-server-2012-update-kb4507447) ou posterior ou [KB4511872](https://support.microsoft.com/help/4511872/cumulative-security-update-for-internet-explorer) ou posterior |
 | Windows Server   | 2012           | Instale [KB4492872](https://support.microsoft.com/help/4492872/update-for-internet-explorer-april-16-2019) para atualizar para o Internet Explorer 11; depois instale [KB4507447](https://support.microsoft.com/help/4507447/windows-server-2012-update-kb4507447) ou posterior ou [KB4511872](https://support.microsoft.com/help/4511872/cumulative-security-update-for-internet-explorer) ou posterior |
 | Windows 7        |  SP1**        | [KB4507437](https://support.microsoft.com/help/4507437/windows-7-update-kb4507437) ou posterior; ou [KB4511872](https://support.microsoft.com/help/4511872/cumulative-security-update-for-internet-explorer) ou posterior |
 | Windows Server   |  2008 R2**    | [KB4507437](https://support.microsoft.com/help/4507437/windows-7-update-kb4507437) ou posterior; ou [KB4511872](https://support.microsoft.com/help/4511872/cumulative-security-update-for-internet-explorer) ou posterior |
  > [!IMPORTANT]
  > ** O Windows 7 e o Windows Server 2008 R2 terão suporte do Microsoft Edge mesmo depois que os sistemas operacionais não tiverem mais suporte. Para que o modo IE tenha suporte nesses sistemas operacionais, os dispositivos precisarão ter as [Atualizações de segurança estendidas para o Windows 7](https://support.microsoft.com/help/4527878/faq-about-extended-security-updates-for-windows-7). É recomendável atualizar para um sistema operacional compatível assim que possível para permanecer seguro. O suporte para o Microsoft Edge com as Atualizações de Segurança Estendidas deve ser considerado uma ponte temporária para chegar a um estado de sistema operacional compatível.

2. O modelo administrativo do Microsoft Edge. Para obter mais informações, consulte [Configurar o Microsoft Edge](./configure-microsoft-edge.md).
3. Internet Explorer 11 habilitado nos Recursos do Windows.

## <a name="see-also"></a>Consulte também

- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Informações adicionais sobre o Modo Empresarial](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)