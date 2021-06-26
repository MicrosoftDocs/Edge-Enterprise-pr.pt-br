---
title: Configuração e suporte à identidade do Microsoft Edge
ms.author: avvaid
author: dan-wesley
manager: srugh
ms.date: 02/05/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Configuração e suporte à identidade do Microsoft Edge
ms.openlocfilehash: 34a5a4aa958873a012d0a2da4184cb508af27a8a
ms.sourcegitcommit: 4192328ee585bc32a9be528766b8a5a98e046c8e
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/25/2021
ms.locfileid: "11617911"
---
# <a name="microsoft-edge-identity-support-and-configuration"></a>Configuração e suporte à identidade do Microsoft Edge

Este artigo descreve como o Microsoft Edge usa a identidade para dar suporte a recursos como sincronização e logon único (SSO). O Microsoft Edge oferece suporte para entrada usando: Serviços de Domínio Active Directory (AD DS), Azure Active Directory (Azure AD) e contas da Microsoft (MSA). No momento o Microsoft Edge suporta apenas contas do Azure Active Directory (Azure AD) pertencentes à nuvem global ou à nuvem soberana do GCC. Estamos trabalhando para adicionar outras nuvens soberanas.

> [!NOTE]
> Este artigo se aplica ao Microsoft Edge versão 77 ou posterior.

## <a name="browser-sign-in-and-authenticated-features"></a>Entrada do navegador e recursos autenticados

Com o Microsoft Edge é possível entrar em um perfil de navegador com uma conta do Azure AD, uma conta MSA ou uma conta de domínio. O tipo de conta usada para entrar determina quais recursos autenticados estão disponíveis para o usuário no Microsoft Edge. A tabela a seguir resume o suporte a recursos para cada tipo de conta.

| Recurso   | Azure AD Premium | Azure AD Gratuito | AD DS local | MSA     |
|----|------------------|---------------|----------------|---------|
| Sincronização | Sim | Não | Não | Sim |
| SSO com Token de atualização principal | Sim | Sim | Não | Sim |
| SSO de conexão remota | Sim | Sim | Sim | N/D |
| Autenticação Integrada do Windows | Sim | Sim | Sim | N/A |
| Página Nova guia Corporativa | Requer O365 |   Requer O365 | Não | N/A |
| Pesquisa da Microsoft | Requer O365 | Requer O365 | Não | N/D |

## <a name="how-users-can-sign-into-microsoft-edge"></a>Como os usuários podem entrar no Microsoft Edge

### <a name="automatic-sign-in"></a>Entrada automática

O Microsoft Edge usa a conta padrão do SO para entrar automaticamente no navegador. Dependendo de como um dispositivo está configurado, os usuários podem entrar automaticamente no Microsoft Edge usando uma das seguintes abordagens.

- **O dispositivo é híbrido/AAD-J:** Disponível no Win10, Windows de nível inferior e versões de servidor correspondentes.
O usuário é conectado automaticamente à sua conta do Azure AD.
- **O dispositivo está associado a um domínio:** Disponível no Win10, Windows de nível inferior e versões de servidor correspondentes.
Por padrão, o usuário não será conectado automaticamente. Se você deseja conectar usuários automaticamente com contas de domínio, use a política [ConfigureOnPremisesAccountAutoSignIn](./microsoft-edge-policies.md#configureonpremisesaccountautosignin). Se você deseja conectar usuários automaticamente com suas contas do Azure AD, considere junção híbrida em seus dispositivos.
- **A conta padrão do SO é MSA:** Win10 RS3 (Versão 1709/Build 10.0.16299) e superior. Esse cenário é improvável em dispositivos corporativos. Mas, se a conta padrão do SO for MSA, o Microsoft Edge entrará automaticamente com a conta MSA.

### <a name="manual-sign-in"></a>Entrada manual

Caso o usuário não entre automaticamente, ele poderá entrar manualmente no Microsoft Edge, durante a primeira experiência de execução, configurações do navegador ou abrindo o submenu de identidade.

### <a name="managing-browser-sign-in"></a>Gerenciando a entrada do navegador

Se você deseja gerenciar a entrada do navegador, pode usar as seguintes políticas:

- Verifique se os usuários sempre têm um perfil de trabalho no Microsoft Edge. [Confira NonRemovableProfileEnabled](./microsoft-edge-policies.md#nonremovableprofileenabled)
- Restrinja a entrada a um conjunto confiável de contas. [Confira RestrictSigninToPattern](./microsoft-edge-policies.md#restrictsignintopattern)
- Desative ou force a entrada do navegador. [Confira BrowserSignin](./microsoft-edge-policies.md#browsersignin)

## <a name="browser-to-web-single-sign-on-sso"></a>Navegador para Logon Único da Web (SSO)

Em algumas plataformas, você pode configurar o Microsoft Edge para entrar automaticamente em sites para seus usuários. Essa opção evita que eles reinsiram suas credenciais para acessar seus sites de trabalho e aumentem sua produtividade.

### <a name="sso-with-primary-refresh-token-prt"></a>SSO com Token de atualização principal (PRT)

O Microsoft Edge tem suporte nativo para SSO baseado em PRT e você não precisa de uma extensão. No Windows 10 RS3 e superior, se um usuário estiver conectado ao perfil do navegador, ele receberá o SSO com o mecanismo de PRT em sites que oferecem suporte para SSO baseado em PRT.

Um Token de Atualização Principal (PRT) é uma chave do Azure AD usada para autenticação em dispositivos Windows 10, iOS e Android. Ele permite logon único (SSO) entre os aplicativos usados nesses dispositivos. Para obter mais informações, consulte [O que é um primário Token de atualização?](/azure/active-directory/devices/concept-primary-refresh-token).

### <a name="seamless-sso"></a>SSO de conexão remota

Assim como o SSO de PRT, o Microsoft Edge tem suporte nativo ao SSO Contínuo sem precisar de uma extensão. No Windows 10 RS3 e superior, se um usuário estiver conectado ao perfil do navegador, ele receberá o SSO com o mecanismo de PRT em sites que oferecem suporte para SSO baseado em PRT.

O Logon Único Contínuo conecta os usuários automaticamente quando eles estão em dispositivos corporativos conectados a uma rede corporativa. Quando habilitados, os usuários não precisam digitar suas senhas para entrar no Azure AD. Normalmente, eles nem precisam digitar seus nomes de usuário. Para obter mais informações, consulte [Logon Único Contínuo do Azure Active Directory](/azure/active-directory/hybrid/how-to-connect-sso).

### <a name="windows-integrated-authentication-wia"></a>Autenticação Integrada do Windows (WIA)

O Microsoft Edge também oferece suporte à autenticação integrada do Windows para solicitações de autenticação na rede interna de uma organização para qualquer aplicativo que use um navegador para sua autenticação. Isso tem suporte em todas as versões do Windows 10 e Windows de nível inferior. Por padrão, o Microsoft Edge usa a zona da intranet como uma lista de permissões para o WIA. Como alternativa, você pode personalizar a lista de servidores habilitados para autenticação integrada usando a política [AuthServerAllowlist](./microsoft-edge-policies.md#authserverallowlist). No macOS, esta política é necessária para ativar a Autenticação integrada.

Para oferecer suporte ao SSO baseado em WIA no Microsoft Edge (versão 77 e posterior), você também pode ter que fazer algumas configurações do lado do servidor. Você provavelmente precisará configurar a propriedade dos Serviços de Federação do Active Directory (AD FS) **WiaSupportedUserAgents** para adicionar suporte à nova cadeia de caracteres do agente do usuário do Microsoft Edge. Para obter instruções sobre como fazer isso, confira as configurações [Exibir WIASupportedUserAgent](/windows-server/identity/ad-fs/operations/configure-ad-fs-browser-wia#view-wiasupporteduseragent-settings) e [Alterar WIASupportedUserAgent](/windows-server/identity/ad-fs/operations/configure-ad-fs-browser-wia#change-wiasupporteduseragent-settings). Um exemplo da cadeia de caracteres do agente de usuário do Microsoft Edge no Windows 10 é mostrado abaixo e você pode aprender mais sobre a [cadeia de caracteres do agente de usuário do Microsoft Edge aqui](/microsoft-edge/web-platform/user-agent-string). 

O seguinte exemplo de uma cadeia de caracteres de agente do usuário é para a compilação mais recente do Canal de desenvolvimento no momento em que este artigo foi publicado:<br> `"Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/80.0.3951.0 Safari/537.36 Edg/80.0.334.2"`

Para serviços que exigem a delegação de credenciais Negotiate, o Microsoft Edge oferece suporte à Delegação Restrita usando a política [AuthNegotiateDelegateAllowlist](./microsoft-edge-policies.md#authnegotiatedelegateallowlist).

## <a name="additional-authentication-concepts"></a>Conceitos de autenticação adicionais

### <a name="proactive-authentication"></a>Autenticação Proativa

A autenticação proativa é uma otimização do navegador para o SSO do site que a frontal carrega a autenticação para determinados sites de terceiros. Isso melhora o desempenho da barra de endereço se o usuário estiver usando o Bing como mecanismo de pesquisa. Isso fornece aos usuários resultados de pesquisa personalizados e do Microsoft Search for Business (MSB). Também habilita permitir a autenticação de serviços importantes, como a Página Nova Guia do Office. Você pode controlá-lo usando a política [ProactiveAuthEnabled]( /deployedge/microsoft-edge-policies#proactiveauthenabled).

### <a name="windows-hello-credui-for-ntlm-authentication"></a>Windows Hello CredUI para autenticação NTLM

Quando um site tenta conectar usuários usando os mecanismos NTLM ou Negotiate e o SSO não está disponível, oferecemos aos usuários uma experiência na qual eles podem compartilhar suas credenciais de SO com o site para satisfazer o desafio de autenticação usando o Windows Hello Cred UI. Esse fluxo de entrada será exibido apenas para usuários do Windows 10 que não obtiverem logon único durante um desafio NTLM ou Negotiate.

### <a name="sign-in-automatically-using-saved-passwords"></a>Entrar automaticamente usando senhas salvas

Se um usuário salvar senhas no Microsoft Edge, ele poderá habilitar um recurso que os conecta automaticamente aos sites em que as credenciais foram salvas. Os usuários podem alternar esse recurso acessando *edge://settings/passwords*. Se você deseja configurar esse recurso, pode usar as políticas do [gerenciador de senhas](./microsoft-edge-policies.md#password-manager-and-protection).

## <a name="see-also"></a>Consulte também

- [Página inicial do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Vídeo: Microsoft Edge e Identidade](microsoft-edge-video-identity.md)
- [Gerenciamento de identidades e acessos](https://www.microsoft.com/security/technology/identity-access-management)
- [Plataforma de identidade](https://developer.microsoft.com/identity)
- [Quatro etapas para uma base de identidade segura com Azure Active Directory](/azure/active-directory/hybrid/four-steps)