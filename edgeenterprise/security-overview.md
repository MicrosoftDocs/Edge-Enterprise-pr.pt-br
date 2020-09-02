---
title: Visão geral da segurança do Microsoft Edge
ms.author: srugh
author: srugh
manager: seanlyn
ms.date: 04/29/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Visão geral da implantação do Microsoft Edge
ms.openlocfilehash: f22f2dcbace00cd535d201950c2af488c708525b
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979156"
---
# Visão geral da segurança do Microsoft Edge
  
Os administradores de TI da empresa estão constantemente enfrentando uma infinidade de desafios de segurança existentes e emergentes. Ao mesmo tempo, protegem a rede corporativa e os dispositivos de ataques mal-intencionados, assim como impedem o acesso não autorizado e vazamentos de dados corporativos. O Microsoft Edge fornece vários recursos exclusivos internos e nativos que ajudam a resolver esses desafios.

> [!NOTE]
> Este artigo se aplica ao Microsoft Edge versão 77 ou posteriores.

## Acesso condicional

Um aspecto fundamental da segurança na nuvem é a identidade e o acesso ao gerenciamento de seus recursos na nuvem. Em um mundo que prioriza a mobilidade e a nuvem, os usuários podem acessar os recursos da sua organização usando vários dispositivos e aplicativos em qualquer lugar. Como resultado, o foco apenas em quem pode acessar um recurso não é suficiente. Também é necessário considerar como um recurso é acessado. O acesso condicional do Azure Active Directory (Azure AD) ajuda você a dominar o equilíbrio entre segurança e produtividade.

### Acesso a recursos protegidos com acesso condicional no Microsoft Edge

O Microsoft Edge oferece suporte ao acesso condicional do Azure AD nativamente. Não é necessário instalar uma extensão separada. Quando você estiver conectado a um perfil do Microsoft Edge com as credenciais empresariais de AD do Azure, o Microsoft Edge permite um acesso impecável aos recursos de nuvem empresarial protegidos usando o Acesso condicional.

Em um dispositivo compatível, a identidade que acessa o recurso deve corresponder à identidade do perfil.  Se isso não acontecer, você verá uma mensagem como a da próxima captura de tela. No exemplo de captura de tela, "testadmin@evostsoneboxtest.com" é a conta necessária para acessar o recurso.

![Mensagem de acesso condicional no navegador](./media/edge-security/microsoft-edge-security-conditional-access.png)

Para continuar, você precisa alternar para o perfil necessário (se tiver um) ou criar um perfil com a identidade correspondente.

Para entrar e trabalhar com seu perfil, clique na imagem da conta no canto superior direito do navegador. É possível usar o menu suspendo para:

- Selecionar outro perfil. Clicar no nome do perfil.
- Criar um perfil. Clique em **Adicionar um recurso**.
- Gerenciar seus perfis. Clique em **Gerenciar configurações de perfil**.

Esse suporte está disponível em todas as plataformas, incluindo todas as versões compatíveis do Windows e do macOS.

### Como implantar o Acesso condicional no Azure Active Directory

[Implantar Acesso condicional](https://docs.microsoft.com/azure/active-directory/conditional-access/plan-conditional-access) fornece um guia detalhado para ajudar a implantar o Acesso condicional no Azure Active Directory.

## Consulte também

- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Vídeo: segurança, compatibilidade e gerenciabilidade](/microsoft-edge-video-security-compatibility-manageability.md)
