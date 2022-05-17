---
title: Sincronização local para usuários do Active Directory (AD)
ms.author: collw
author: dan-wesley
manager: silvanam
ms.date: 05/17/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Sincronização local para usuários do Active Directory (AD)
ms.openlocfilehash: d829829d62073e357cec1c340ff9c1e99b0fb88f
ms.sourcegitcommit: d384115fb2197261ee8fa3b0bdbcb7455527616f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/17/2022
ms.locfileid: "12517546"
---
# <a name="on-premises-sync-for-active-directory-ad-users"></a>Sincronização local para usuários do Active Directory (AD)

Este artigo explica como os usuários do Active Directory (AD) podem transferir os favoritos e as configurações do Microsoft Edge entre computadores sem se conectar aos serviços de nuvem da Microsoft.

> [!NOTE]
> Este artigo se aplica ao Microsoft Edge versão 85 ou posterior.

## <a name="introduction"></a>Introdução

Sincronizar os dados do usuário no Microsoft Edge normalmente requer uma conta da Microsoft ou uma conta do Azure Active Directory (Azure AD) e uma conexão com os serviços de nuvem da Microsoft. Com a sincronização local, o Microsoft Edge salva os favoritos e as configurações de um usuário do Active Directory em um arquivo que pode ser movido entre diferentes computadores. A sincronização local não afeta a sincronização de nuvem para esses perfis que os permitem.

## <a name="how-it-works"></a>Como funciona

O Microsoft Edge permite que perfis sejam associados a contas do Active Directory (AD), que não podem ser usados com sincronização em nuvem. Quando a sincronização local está habilitada, os dados do perfil AD são salvos em um arquivo chamado profile.pb. Por padrão, esse arquivo está armazenado em *%APP_DATA%/Microsoft/Edge*. Após a gravação desse arquivo, ele poderá ser movido entre computadores diferentes, e os dados do usuário serão lidos e escritos em cada computador. Microsoft Edge somente leituras e gravações desse arquivo; é responsabilidade do administrador garantir que o arquivo seja movido conforme necessário.

## <a name="use-on-premises-sync"></a>Usar sincronização local

Para usar a sincronização local, você precisa habilitá-la, associar um perfil a uma conta do AD e, opcionalmente, alterar a localização dos dados do usuário.

### <a name="enable-on-premises-sync"></a>Habilitar sincronização local

Para habilitar a sincronização local no Microsoft Edge, configure a política [RoamingProfileSupportEnabled](./microsoft-edge-policies.md#roamingprofilesupportenabled).

### <a name="ensure-that-a-profile-is-associated-with-an-active-directory-account"></a>Garantir que o perfil esteja associado a uma conta do Active Directory

A sincronização local só funciona com o perfil associado a uma conta do Active Directory (AD). Se esse perfil não existir, a sincronização local não funcionará. Para garantir que os usuários entrem com uma conta do AD, configure a política [ConfigureOnPremisesAccountAutoSignIn](./microsoft-edge-policies.md#configureonpremisesaccountautosignin). Para a sincronização local, o Microsoft Edge depende apenas do AD para estabelecer uma identidade para os dados do usuário, e não há relação direta entre como o Microsoft Edge lê e escreve os dados locais e como o administrador configurou o roaming para um usuário do AD.

### <a name="change-the-location-of-the-user-data-optional"></a>Alterar a localização dos dados do usuário (opcional)

Por padrão, os dados do usuário são armazenados em um arquivamento chamado **profile.pb** em *%APPDATA%/Microsoft/Edge*. Para alterar o local desse arquivo, configure a política [RoamingProfileLocation](./microsoft-edge-policies.md#roamingprofilelocation).

## <a name="changes-in-the-user-experience-when-on-premises-sync-is-enabled"></a>Alterações na experiência do usuário quando a sincronização no local está habilitada

Quando a sincronização local estiver habilitada, os usuários não serão solicitados a habilitar a sincronização. Além disso, os usuários não podem desativar a sincronização nas configurações de sincronização e não podem ativar os tipos de sincronização que não têm suporte da sincronização local.

## <a name="on-premises-sync-usage-notes"></a>Anotações de uso de sincronização no local

### <a name="running-cloud-sync-and-on-premises-sync-on-the-same-computer"></a>Executando a sincronização de nuvem e a sincronização local no mesmo computador

A sincronização local não afeta a sincronização na nuvem. Se o Microsoft Edge tiver várias contas da Microsoft ou perfis do Azure Active Directory que sincronizam com a nuvem, estes perfis continuarão a sincronizar enquanto a sincronização local estiver habilitada.

### <a name="running-microsoft-edge-on-more-than-one-computer-at-a-time-isnt-recommended"></a>Não é recomendável executar o Microsoft Edge em mais de um computador por vez

Como a sincronização local funciona movendo um arquivo de dados do usuário entre computadores, a sincronização local não sincroniza as alterações entre as sessões simultâneas. Por esse motivo, a sincronização local funciona melhor quando usada em um computador por vez. Se houver sessões locais simultâneas em execução, os dados em qualquer um dos computadores poderão ser substituídos inesperadamente por dados de outro computador na próxima vez que você iniciar uma sessão do navegador.

> [!NOTE]
> O Microsoft Edge bloqueia o arquivo **perfil.pb** quando a sincronização local está habilitada. Se o redirecionamento de pasta for usado para compartilhar um único arquivo **profile.pb** entre computadores diferentes, somente uma instância do Microsoft Edge que usa o arquivo compartilhado poderá ser iniciada.

### <a name="using-other-sync-policies-with-on-premises-sync"></a>Usando outras políticas de sincronização com a sincronização local

A política [SyncTypesListDisabled](./microsoft-edge-policies.md#synctypeslistdisabled) pode ser usada para desabilitar seletivamente a sincronização de favoritos ou configurações, se necessário. A política [SyncDisabled](./microsoft-edge-policies.md#syncdisabled) não tem impacto na sincronização local.

## <a name="see-also"></a>Consulte também

- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Microsoft Edge e Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md)
- [Sincronização do Microsoft Edge Enterprise](microsoft-edge-enterprise-sync.md)