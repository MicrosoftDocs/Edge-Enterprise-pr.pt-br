---
title: Compatibilidade com versões anteriores para a página Nova guia da empresa
ms.author: ruchir
author: dan-wesley
manager: vwehren
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Compatibilidade com versões anteriores para a página Nova guia da empresa
ms.openlocfilehash: e2534f9df82aa81843d7cd292ada99a4c7574a3c
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/09/2021
ms.locfileid: "11642077"
---
# <a name="backwards-compatibility-for-the-enterprise-new-tab-page"></a>Compatibilidade com versões anteriores para a página Nova guia da empresa

Este artigo descreve a mudança para a página da Nova guia e como os usuários podem ser compatíveis com versões anteriores do Microsoft Edge, versão 87 e anterior.

> [!NOTE]
> Este artigo se aplica ao Microsoft Edge versão 87 ou posterior.

## <a name="information-feeds-from-single-endpoint"></a>Feeds de informações do ponto de extremidade único

A nova versão da página Nova guia da Empresa combina conteúdo compatível do Microsoft 365 com feeds de informações relevantes e em conformidade com o setor que são servidos pelo ponto de extremidade MSN.com.

> [!NOTE]
> O conteúdo do Office 365 foi originalmente servido usando o domínio [Office.com](https://www.office.com).

Se o acesso ao domínio MSN.com for restrito à sua organização, é altamente recomendável conceder aos usuários acesso a esse [URL](https://ntp.msn.com).

Se precisar de mais tempo para habilitar o acesso ao domínio do MSN, recomendamos usar o [NewTabPageSetFeedType](./microsoft-edge-policies.md#newtabpagesetfeedtype), que permite que você escolha a experiência do Microsoft News ou o feed do Office 365 para a página Nova guia.

### <a name="keep-using-officecom"></a>Continuar usando o Office.com

 Você pode configurar a política **NewTabPageSetFeedType** para continuar usando o domínio substituído do Office.com.

> [!IMPORTANT]
> A política **NewTabPageSetFeedType** e o domínio Office.com que atendem ao conteúdo do Office 365 deixarão de funcionar quando a versão 90 do Microsoft Edge for lançada.

As configurações de política a seguir forçarão a Nova guia empresarial a converter o conteúdo de documentos do Office a partir do domínio Office.com.

- Defina a política como **Obrigatória**.
- Defina o valor do mapeamento de política para **Office (1) = experiência de feed do Office 365**.

Se não for possível migrar para o Office.com, envie-nos seus comentários. Outra opção é definir o [NewTabPageLocation](./microsoft-edge-policies.md#newtabpagelocation) para que ele aponte para uma URL de ponto de extremidade permitida pela sua organização.

> [!NOTE]
> A política **NewTabPageLocation** tem precedência se a política **NewTabPageSetFeedType** também estiver configurada.

## <a name="enterprise-users-will-now-get-microsoft-news-content-via-my-feed"></a>Os usuários corporativos receberão o conteúdo de notícias da Microsoft por meio do Meu Feed

A página de Nova guia da empresa oferecerá informações relevantes do setor no **Meus feed** e o conteúdo do Office 365 em um único modo de exibição para os usuários que se conectam a uma conta do Azure Active Directory (Azure AD). Para os usuários que entrarem com o Azure Active Directory (Azure AD) que selecionarem a opção Microsoft Notícias no submenu configurações, seu novo modo de exibição de página de guia será substituído com conteúdo**Meu feed**. Ao abrir uma nova página da guia no navegador, ele terá a seguinte aparência como o exemplo da captura de tela a seguir.

![Nova guia mostrando o conteúdo do Meu feed.](media/microsoft-edge-ntp-backward-compatibility/microsoft-edge-ntp-myfeed-view.png)

> [!NOTE]
> Os usuários que não entrarem com o Azure AD ainda poderão ver o feed de notícias do MSN quando abrirem uma Nova guia.

## <a name="page-layout"></a>Layout de página

Com as alterações na página Nova guia, o layout da página não tem mais que controlar dois tipos de conteúdo específicos (Office 365 e Microsoft Notícias), portanto, a opção de conteúdo não está disponível. A próxima captura de tela mostra o submenu do layout da página.

![Modo de exibição do layout para a página Nova guia.](media/microsoft-edge-ntp-backward-compatibility/microsoft-edge-ntp-page-layout.png)

Caso pretenda manter o acesso ao conteúdo do Microsoft Notícias que não esteja associado à sua organização, você deve usar um perfil diferente do navegador. Vá para  *edge://settings/profiles* e saia do seu perfil do Azure AD. Essa ação exibirá o modo de exibição padrão para a página de Nova guia da empresa. 

## <a name="see-also"></a>Consulte também

- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Modo Empresarial do Internet Explorer 11](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)