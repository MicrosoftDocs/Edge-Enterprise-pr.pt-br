---
title: Microsoft Edge e acesso condicional
ms.author: srugh
author: srugh
manager: seanlyn
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Microsoft Edge e acesso condicional
ms.openlocfilehash: bee6aa73e078037adf28af05755bd0a74b30a65b5122eeca16fb7f6c2af1ae4a
ms.sourcegitcommit: d44c0997ffe40d67421312ed96e7766da947eaa0
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/05/2021
ms.locfileid: "11726704"
---
# <a name="microsoft-edge-and-conditional-access"></a>Microsoft Edge e acesso condicional
  
Esse artigo descreve como o Microsoft Edge é compatível com o acesso condicional e como acessar os recursos protegidos pelo acesso condicional.

> [!NOTE]
> Este artigo se aplica ao Microsoft Edge versão 77 ou posterior.

Um aspecto fundamental da segurança na nuvem é a identidade e o acesso ao gerenciamento de seus recursos na nuvem. Em um mundo que prioriza a mobilidade e a nuvem, os usuários podem acessar os recursos da sua organização usando vários dispositivos e aplicativos em qualquer lugar. Como resultado, o foco apenas em quem pode acessar um recurso não é suficiente. Também é necessário considerar como um recurso é acessado. O acesso condicional do Azure Active Directory (Azure AD) ajuda você a dominar o equilíbrio entre segurança e produtividade.

## <a name="accessing-conditional-access-protected-resources-in-microsoft-edge"></a>Acesso a recursos protegidos com acesso condicional no Microsoft Edge

O Microsoft Edge oferece suporte ao acesso condicional do Azure AD nativamente. Não é necessário instalar uma extensão separada. Quando você estiver conectado a um perfil do Microsoft Edge com as credenciais empresariais de AD do Azure, o Microsoft Edge permite um acesso impecável aos recursos de nuvem empresarial protegidos usando o Acesso condicional.

Em um dispositivo compatível, a identidade que acessa o recurso deve corresponder à identidade do perfil.  Se isso não acontecer, você verá uma mensagem como a da próxima captura de tela. No exemplo de captura de tela, "testadmin@evostsoneboxtest.com" é a conta necessária para acessar o recurso.

![Mensagem de acesso condicional no navegador](./media/edge-security/microsoft-edge-security-conditional-access.png)

Para continuar, você precisa alternar para o perfil necessário (se tiver um) ou criar um perfil com a identidade correspondente.

Para entrar e trabalhar com seu perfil, clique na imagem da conta no canto superior direito do navegador. É possível usar o menu suspendo para:

- Selecionar outro perfil. Clicar no nome do perfil.
- Criar um perfil. Clique em **Adicionar um recurso**.
- Gerenciar seus perfis. Clique em **Gerenciar configurações de perfil**.

Esse suporte está disponível em todas as plataformas, incluindo todas as versões compatíveis do Windows e do macOS.

### <a name="how-to-deploy-conditional-access-in-azure-active-directory"></a>Como implantar o Acesso condicional no Azure Active Directory

[Implantar Acesso condicional](/azure/active-directory/conditional-access/plan-conditional-access) fornece um guia detalhado para ajudar a implantar o Acesso condicional no Azure Active Directory.

## <a name="see-also"></a>Consulte também

- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Vídeo: segurança, compatibilidade e gerenciabilidade](/microsoft-edge-video-security-compatibility-manageability.md)