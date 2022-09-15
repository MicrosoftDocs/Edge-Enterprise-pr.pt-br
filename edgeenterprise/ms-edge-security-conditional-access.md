---
title: Microsoft Edge e acesso condicional
ms.author: srugh
author: srugh
manager: seanlyn
ms.date: 05/25/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Suporte do Microsoft Edge para Acesso Condicional
ms.openlocfilehash: 9b2356f9dee3677b7b7009a11017e901918580cf
ms.sourcegitcommit: 8a2193791e6606a4dced9808013d6b064d2f2319
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/15/2022
ms.locfileid: "12753906"
---
# <a name="microsoft-edge-and-conditional-access"></a>Microsoft Edge e acesso condicional
  
Esse artigo descreve como o Microsoft Edge é compatível com o acesso condicional e como acessar os recursos protegidos pelo acesso condicional.

> [!NOTE]
> Este artigo se aplica ao Microsoft Edge versão 77 ou posterior.

Um aspecto fundamental da segurança na nuvem é a identidade e o acesso ao gerenciamento de seus recursos na nuvem. Em um mundo móvel e de primeira nuvem, os usuários podem acessar os recursos da sua organização usando vários dispositivos e aplicativos de qualquer lugar. Como resultado disso, apenas se concentrar em quem pode acessar um recurso não é suficiente. Também é necessário considerar como um recurso é acessado. O acesso condicional do Azure Active Directory (Azure AD) ajuda você a dominar o equilíbrio entre segurança e produtividade.

## <a name="accessing-conditional-access-protected-resources-in-microsoft-edge"></a>Acesso a recursos protegidos com acesso condicional no Microsoft Edge

O Microsoft Edge oferece suporte ao acesso condicional do Azure AD nativamente. Não é necessário instalar uma extensão separada. Quando você estiver conectado a um perfil do Microsoft Edge com as credenciais empresariais de AD do Azure, o Microsoft Edge permite um acesso impecável aos recursos de nuvem empresarial protegidos usando o Acesso condicional.

Em um dispositivo compatível, a identidade que acessa o recurso deve corresponder à identidade do perfil.  Se isso não acontecer, você verá uma mensagem como a da próxima captura de tela. No exemplo de captura de tela, "testadmin@evostsoneboxtest.com" é a conta necessária para acessar o recurso.

![Mensagem de acesso condicional no navegador](./media/edge-security/microsoft-edge-security-conditional-access.png)

Para continuar, você precisa alternar para o perfil necessário (se tiver um) ou criar um perfil com a identidade correspondente.

Para entrar e trabalhar com seu perfil, selecione a imagem da conta no canto superior direito do navegador. É possível usar o menu suspendo para:

- Escolha outro perfil. Selecione o nome do perfil.
- Criar um perfil. Selecione **Adicionar um perfil**.
- Gerenciar seus perfis. Selecione **Gerenciar configurações de perfil**.

Esse suporte está disponível em todas as plataformas, incluindo todas as versões compatíveis do Windows e do macOS.

> [!NOTE]
> Não há suporte para o Acesso Condicional no modo InPrivate, pois não há nenhum conceito de um perfil conectado nesse modo.

### <a name="how-to-deploy-conditional-access-in-azure-active-directory"></a>Como implantar o Acesso condicional no Azure Active Directory

[Implantar o Acesso Condicional](/azure/active-directory/conditional-access/plan-conditional-access) fornece um guia detalhado para ajudar a planejar e implantar o Acesso Condicional no Azure Active Directory.

## <a name="see-also"></a>Consulte também

- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Vídeo: segurança, compatibilidade e gerenciabilidade](/deployedge/microsoft-edge-video-security-compatibility-manageability)
