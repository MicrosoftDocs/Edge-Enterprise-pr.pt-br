---
title: Compatibilidade com versões anteriores para a página Nova guia da empresa
ms.author: ruchir
author: dan-wesley
manager: vwehren
ms.date: 10/28/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Compatibilidade com versões anteriores para a página Nova guia da empresa
ms.openlocfilehash: c10671a6ec8e1ff4dcb0db3f3c085f82ae973122
ms.sourcegitcommit: af6ab070d0c09bca4a9cf505b107ed7e04839763
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/29/2020
ms.locfileid: "11144465"
---
# Compatibilidade com versões anteriores para a página Nova guia da empresa

Este artigo descreve a mudança para a página da Nova guia e como os usuários podem ser compatíveis com versões anteriores do Microsoft Edge, versão 87 e anterior.

> [!NOTE]
> Este artigo se aplica ao Microsoft Edge versão 87 ou posterior.

## Feeds de informações do ponto de extremidade único

A nova versão da página Nova guia da Empresa combina conteúdo compatível do Microsoft 365 com feeds de informações relevantes e em conformidade com o setor que são servidos pelo ponto de extremidade MSN.com.

> [!NOTE]
> O conteúdo do Office 365 foi originalmente servido usando o domínio [Office.com](https://www.office.com).

Se o acesso ao domínio MSN.com for restrito à sua organização, é altamente recomendável conceder aos usuários acesso a esse [URL](https://ntp.msn.com).

Se precisar de mais tempo para habilitar o acesso ao domínio do MSN, recomendamos usar o [NewTabPageSetFeedType](https://docs.microsoft.com/deployedge/microsoft-edge-policies#newtabpagesetfeedtype), que permite que você escolha a experiência do Microsoft News ou o feed do Office 365 para a página Nova guia.

### Continuar usando o Office.com

 Você pode configurar a política **NewTabPageSetFeedType** para continuar usando o domínio substituído do Office.com.

> [!IMPORTANT]
> A política **NewTabPageSetFeedType** e o domínio Office.com que atendem ao conteúdo do Office 365 deixarão de funcionar quando a versão 90 do Microsoft Edge for lançada.

As configurações de política a seguir forçarão a Nova guia empresarial a converter o conteúdo de documentos do Office a partir do domínio Office.com.

- Defina a política como **Obrigatória**.
- Defina o valor do mapeamento de política para **Office (1) = experiência de feed do Office 365**.

Se não for possível migrar para o Office.com, envie-nos seus comentários. Outra opção é definir o [NewTabPageLocation](https://docs.microsoft.com/deployedge/microsoft-edge-policies#newtabpagelocation) para que ele aponte para uma URL de ponto de extremidade permitida pela sua organização.

> [!NOTE]
> A política **NewTabPageLocation** tem precedência se a política **NewTabPageSetFeedType** também estiver configurada.

## Os usuários corporativos receberão o conteúdo de notícias da Microsoft por meio do Meu Feed

A página de Nova guia da empresa oferecerá informações relevantes do setor no **Meus feed** e o conteúdo do Office 365 em um único modo de exibição para os usuários que se conectam a uma conta do Azure Active Directory (Azure AD). Para os usuários que entrarem com o Azure Active Directory (Azure AD) que selecionarem a opção Microsoft Notícias no submenu configurações, seu novo modo de exibição de página de guia será substituído com conteúdo**Meu feed**. Ao abrir uma nova página da guia no navegador, ele terá a seguinte aparência como o exemplo da captura de tela a seguir.

![Nova guia mostrando o conteúdo do Meu feed.](media/microsoft-edge-ntp-backward-compatibility/microsoft-edge-ntp-myfeed-view.png)

> [!NOTE]
> Os usuários que não entrarem com o Azure AD ainda poderão ver o feed de notícias do MSN quando abrirem uma Nova guia.

## Layout de página

Com as alterações na página Nova guia, o layout da página não tem mais que controlar dois tipos de conteúdo específicos (Office 365 e Microsoft Notícias), portanto, a opção de conteúdo não está disponível. A próxima captura de tela mostra o submenu do layout da página.

![Modo de exibição do layout para a página Nova guia.](media/microsoft-edge-ntp-backward-compatibility/microsoft-edge-ntp-page-layout.png)

Caso pretenda manter o acesso ao conteúdo do Microsoft Notícias que não esteja associado à sua organização, você deve usar um perfil diferente do navegador. Vá para  *edge://settings/profiles* e saia do seu perfil do Azure AD. Essa ação exibirá o modo de exibição padrão para a página de Nova guia da empresa. 

## Consulte também

- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Modo Empresarial do Internet Explorer 11](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)