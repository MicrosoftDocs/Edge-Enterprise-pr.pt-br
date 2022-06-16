---
title: O que é o modo Internet Explorer?
ms.author: kvice
author: dan-wesley
manager: laurawi
ms.date: 06/15/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Saiba como o modo Internet Explorer no Microsoft Edge fornece acesso a sites que precisam do Internet Explorer 11 e acesso a sites modernos.
ms.openlocfilehash: c501ae566115a084f3c6df8e1676d6762468e034
ms.sourcegitcommit: 01011d970e85683f74f889651f5f402da642f34a
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/15/2022
ms.locfileid: "12595189"
---
# <a name="what-is-internet-explorer-ie-mode"></a>O que é o modo Internet Explorer (IE)?

>[!Note]
> O aplicativo da área de trabalho do Internet Explorer 11 foi [desativado e está sem suporte a partir de 15 de junho de 2022](https://aka.ms/IEJune15Blog) para determinadas versões do Windows 10.  
>
> - Você ainda pode acessar sites antigos e herdados que exigem o Internet Explorer com o modo Internet Explorer no Microsoft Edge. [Saiba como >](https://aka.ms/IEmodewebsite)
> - O aplicativo da área de trabalho do Internet Explorer 11 será redirecionado progressivamente para o navegador mais rápido e seguro Microsoft Edge e, por fim, será desabilitado por meio do Windows Update. [Desabilitar o IE hoje>](/deployedge/edge-ie-disable-ie11)  


Criamos o modo Internet Explorer (IE) no Microsoft Edge para organizações que ainda precisam do Internet Explorer 11 para compatibilidade com sites existentes, mas também precisam de um navegador moderno. Esse recurso torna mais fácil para as organizações usarem um navegador, para web/aplicativos legados ou para web/app moderno. Este artigo fornece uma introdução ao uso do Microsoft Edge com o modo IE.

Para obter um guia de configuração avançada, consulte [Configurar o modo IE para Microsoft Edge](https://go.microsoft.com/fwlink/?linkid=2188232).

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
- Configure a política de grupo **Enviar todos os sites da intranet para o Internet Explorer** e configure-a como **Habilitada** (Microsoft Edge 77 ou posterior.)

### <a name="ie-mode-supports-the-following-internet-explorer-functionality"></a>O modo IE oferece suporte à seguinte funcionalidade do Internet Explorer

- Todos os modos do documento e modos corporativos.
- Controles do ActiveX (como Java ou Silverlight). **Observação**: o Silverlight não [terá mais suporte](https://support.microsoft.com/windows/silverlight-end-of-support-0a3be3c7-bead-e203-2dfd-74f0a64f1788) a partid do dia 12 de outubro de 2021. 
- Objetos auxiliares do navegador 
- Configurações do Internet Explorer e políticas de grupo que afetam as configurações da zona de segurança e o Modo Protegido
- Ferramentas de desenvolvedor F12 para IE, quando lançadas com [IEChooser](/deployedge/edge-ie-mode-faq#how-can-i-debug-my-legacy-application-while-using-ie-mode-on-microsoft-edge-)
- Extensões do Microsoft Edge (Extensões que interagem com o conteúdo da página do IE diretamente não recebem suporte.)

### <a name="ie-mode-doesnt-support-the-following-internet-explorer-functionality"></a>O modo IE não oferece suporte à seguinte funcionalidade do Internet Explorer

- Barras de ferramentas do Internet Explorer
- Configurações do Internet Explorer e políticas de grupo que controlam o menu de navegação.
- Ferramentas de desenvolvedor do IE11 ou Microsoft Edge F12

## <a name="prerequisites"></a>Pré-requisitos

Os pré-requisitos a seguir se aplicam ao uso do Microsoft Edge com o modo IE.

> [!IMPORTANT]
> Para garantir o sucesso, instale as atualizações mais recentes para o Windows e o Microsoft Edge. Se isso não for feito, provavelmente o modo IE deixará de funcionar.

1. As atualizações mínimas do sistema para os sistemas operacionais listados na tabela a seguir.

 | Sistema operacional | Versão       | Atualizações |
 |------------------|---------------|---------|
 | Windows 11       |               |         |
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
