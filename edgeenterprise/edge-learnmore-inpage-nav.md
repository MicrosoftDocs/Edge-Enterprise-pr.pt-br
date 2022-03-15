---
title: Manter a navegação na página no modo do Internet Explorer
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 02/15/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Manter a navegação na página no modo do Internet Explorer
ms.openlocfilehash: 2b340f403d66f78372cc4b3a045d0c0ebb6b849b
ms.sourcegitcommit: 556aca8dde42dd66364427f095e8e473b86651a0
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2022
ms.locfileid: "12445855"
---
# <a name="keep-in-page-navigation-in-internet-explorer-mode"></a>Manter a navegação na página no modo do Internet Explorer

Você pode usar essa política como uma solução temporária para forçar toda a navegação na página de sites do modo do Internet Explorer (modo IE) para permanecer no modo do IE.

Uma navegação na página é iniciada a partir de um link, um script ou um formulário na página atual. Também pode ser um redirecionamento do servidor de uma tentativa anterior de navegação na página. Por outro lado, um usuário pode iniciar uma navegação que não é “na página” e independente da página atual de várias maneiras, usando os controles do navegador. Por exemplo, usando a barra de endereço, o botão voltar ou um link favorito.

>[!NOTE]
>Este artigo se aplica ao Microsoft Edge versão 81 ou posterior.

## <a name="prerequisites"></a>Pré-requisitos

As seguintes atualizações do Windows são necessárias para esta política:

- Windows 11
- Windows 10 versão 1909 e 1903, Windows Server versão 1909 e 1903 ([KB4532695](https://support.microsoft.com/help/4532695))
- Windows 10 versão 1809, Windows Server versão 1809, Windows Server 2019 ([KB4534321](https://support.microsoft.com/help/4534321))
- Windows 10 versão 1803 ([KB4534308](https://support.microsoft.com/help/4534308))
- Windows 10 versão 1709 ([KB4534318](https://support.microsoft.com/help/4534318))

## <a name="about-this-policy"></a>Sobre essa política

Essa política oferece tempo para identificar e configurar todos os servidores de autenticação usados ​​pelos seus sites no modo IE. No entanto, essa política pode resultar em uma experiência de navegação inconsistente, na qual alguns sites são renderizados no modo IE e outras vezes renderizados no modo Microsoft Edge. Essa experiência depende se a navegação do site começou em uma página de modo do IE. Qualquer site que não esteja explicitamente configurado para abrir em um mecanismo de renderização específico estará sujeito a essa inconsistência.

Se você habilitar essa política, recomendamos que a desabilite depois de identificar todos os servidores de autenticação e adicioná-los à lista de sites como neutros. Isso garante que seus sites modernos nunca sejam renderizados inadvertidamente no modo do IE.

## <a name="keep-in-page-navigation-in-ie-mode"></a>Manter navegações na página no modo do IE

Para manter as navegações automáticas ou toda a navegação na página no modo Internet Explorer, siga estas etapas:

1. Abra o Editor de política de grupo local.
2. Clique em **Configuração do Computador** > **Modelos Administrativos** > **Microsoft Edge**.
3. Em **Configuração**, clique duas vezes em **Especificar como as navegações "na página" para sites não configurados se comportam quando iniciadas nas páginas do modo Internet Explorer**.

   ![Configuração de política na página](media/edge-learnmore-inpage-nav/learnmore-in-page-nav-settings.png)

4. Selecione **Habilitado** 

   ![Habilitar política na página](media/edge-learnmore-inpage-nav/learnmore-in-page-nav-enable.png)

5. Escolha uma das opções a seguir na lista suspensa:

   - **Padrão** - Apenas sites configurados para abrir no modo Internet Explorer serão abertos nesse modo. Qualquer site não configurado para abrir no modo Internet Explorer será redirecionado de volta ao Microsoft Edge.
   - **Manter apenas navegações automáticas no modo Internet Explorer** - Use essa opção se desejar a experiência padrão, exceto que todas as navegações automáticas (como redirecionamentos 302) para sites não configurados serão mantidas no modo Internet Explorer.
   - **Mantenha toda a navegação** na página no modo Internet Explorer (Menos Recomendado **_)_** – Todas as navegação de páginas carregadas no modo IE para sites não configurados são mantidas no modo Internet Explorer.

6. Clique em **OK** ou **Aplicar** para salvar as configurações de política.

## <a name="see-also"></a>Consulte também

- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
