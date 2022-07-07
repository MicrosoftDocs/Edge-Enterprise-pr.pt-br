---
title: Suporte de plataforma para recursos do Microsoft Edge
ms.author: collw
author: dan-wesley
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Resumo do suporte de plataforma para recursos do Microsoft Edge
ms.openlocfilehash: a8d8efc6ec1108f23cb8bf2c0961c62a87628832
ms.sourcegitcommit: 2465bada4ab3063adc6f94ebb1895949a5b6219e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/06/2022
ms.locfileid: "12635653"
---
# <a name="platform-support-for-microsoft-edge-features"></a>Suporte de plataforma para recursos do Microsoft Edge

Este artigo resume o suporte de plataforma para recursos do Microsoft Edge.

> [!NOTE]
> Este artigo se aplica ao Microsoft Edge versão 77 ou posterior.

## <a name="feature-matrix-for-platforms"></a>Matriz de recursos para plataformas

As tabelas a seguir resumem o suporte a recursos para as plataformas Windows e macOS.

> [!NOTE]
> Android e iOS atualmente não estão representados nas tabelas de suporte, no entanto, continuamos trabalhando nessas informações e faremos as atualizações necessárias.

| Recursos de segurança |Win 10|Win 8.1|Win 7|macOS|Linux|URL|
|-------------------|------|-------|-----|-----|-----|---|
|Acesso Condicional do Azure Active Directory (Azure AD)|Sim|Sim|Sim|Sim|Não|[Acesso Condicional do Microsoft Azure Active Directory](/deployedge/ms-edge-security-conditional-access#accessing-conditional-access-protected-resources-in-microsoft-edge)|
|Microsoft Defender Application Guard|Sim (1890+)|Não|Não|Não|Não|[Microsoft Defender Application Guard](/deployedge/microsoft-edge-security-windows-defender-application-guard) |
|Microsoft Defender SmartScreen|Sim|Sim|Sim|Sim|Sim|[Microsoft Defender SmartScreen](/deployedge/microsoft-edge-security-smartscreen) |
|Microsoft Ponto de extremidade da DLP|Sim|Não|Não|Não|Não|[Microsoft Ponto de extremidade da DLP](/deployedge/microsoft-edge-security-dlp#microsoft-endpoint-data-loss-prevention-endpoint-dlp)|
|Monitor de Senhas|Sim|Sim|Sim|Sim|Sim|[Monitor de Senhas](https://blogs.windows.com/msedgedev/2021/01/21/edge-88-privacy/)|
|Gerador de Senhas|Sim|Sim|Sim|Sim|Sim|[Gerador de Senhas](https://blogs.windows.com/msedgedev/2021/01/21/edge-88-privacy/)|
|Proteção de Informações do Windows (WIP)|Sim (1607+)|Não|Não|Não|Não|[WIP](/deployedge/microsoft-edge-security-windows-information-protection#system-requirements)|

|Recursos de identidade| Win 10 | Win 8.1 | Win 7 | macOS | Linux | URL |
|-----------------|--------|---------|-------|-------|-------|-----|
|Login Automático (híbrido / AAD-J)|Sim|Sim|Sim|Não|Não|[híbrido/AAD-J](/deployedge/microsoft-edge-security-identity#automatic-sign-in)|
|Login Automático (ingressou no domínio)|Sim|Sim|Sim|Não|Não|[domínio ingressou](/deployedge/microsoft-edge-security-identity#automatic-sign-in)|
|Login Automático (A conta padrão do sistema operacional é MSA)|Sim (1709+)|Não|Não|Não|Não|[MSA](/deployedge/microsoft-edge-security-identity#automatic-sign-in)|
|Navegador para Logon Único na Web (SSO)|Sim|Sim|Sim|Sim|Sim|[SSO de Navegador da Web](https://www.microsoft.com/microsoft-365/roadmap?featureid=66332)|
|Troca guiada/"Troca Automática de Perfil"|Sim|Sim|Sim|Sim|Sim|[Usando vários perfis no trabalho e na residência](https://blogs.windows.com/msedgedev/2020/04/30/automatic-profile-switching/) |
|Perfis Múltiplos|Sim|Sim|Sim|Sim|Sim|[Usando vários perfis no trabalho e na residência](https://blogs.windows.com/msedgedev/2020/04/30/automatic-profile-switching/) |
|Sincronização local para Active Directory (AD)|Sim|Sim|Sim|Não|Não|[Sincronização local para usuários do Active Directory (AD)](/deployedge/microsoft-edge-on-premises-sync) |
|SSO de conexão remota|Sim (1709+)|Sim|Sim|Sim|Sim|[SSO de conexão remota](/deployedge/microsoft-edge-security-identity#seamless-sso)|
|SSO com Token de atualização principal (PRT)|Sim (1709+)|Sim|Sim|Não|Não|[SSO com PRT](/deployedge/microsoft-edge-security-identity#sso-with-primary-refresh-token-prt)|
|Autenticação Integrada do Windows (WIA)|Sim|Sim|Sim|Sim * (Política Obrigatória)|Sim|[WIA](/deployedge/microsoft-edge-security-identity#windows-integrated-authentication-wia)|

|Recursos adicionais|Win 10|Win 8.1|Win 7|macOS|Linux|URL|
|-------------------|------|-------|-----|-----|-----|---|
|Coleções|Sim|Sim|Sim|Sim|Sim|[Coleções](https://blogs.windows.com/msedgedev/2019/12/09/improvements-collections-sync-microsoft-edge/) |
|Página de Nova Guia de Empresa|Sim|Sim|Sim|Sim|Sim|[Página de Nova Guia](https://blogs.windows.com/msedgedev/2020/10/29/enterprise-new-tab-page-my-feed/) |
|Modo IE|Sim|Sim|Sim|Não|Não|[Modo IE](/deployedge/edge-ie-mode#prerequisites)|
|Modo quiosque|Sim|Não|Não|Não|Não|[Modo quiosque](/deployedge/microsoft-edge-configure-kiosk-mode)|
|Pesquisa da Microsoft no Bing|Sim|Sim|Sim|Sim|Sim|[Pesquisa Inteligente no Bing](https://www.microsoft.com/edge/business/intelligent-search-with-bing) |
|Leitor de PDF|Sim|Sim|Sim|Sim|Sim|[Leitor de PDF](/deployedge/microsoft-edge-pdf) |
|Compras|Sim|Sim|Sim|Sim|Sim|[Compras](https://techcommunity.microsoft.com/t5/articles/introducing-shopping-with-microsoft-edge/m-p/1870080) |
|Guias de Insuidade|Sim|Sim|Sim|Sim|Sim|[Visão geral do recurso](/deployedge/microsoft-edge-relnote-stable-channel)<br>[Última Postagem do Blog](https://blogs.windows.com/msedgedev/2021/03/04/edge-89-performance/)<br>[Políticas de Grupo](/deployedge/microsoft-edge-policies#sleeping-tabs-settings)|
|Sincronização|Sim|Sim|Sim|Sim|Sim|[Sincronização de Empresa](/deployedge/microsoft-edge-enterprise-sync) |
|Reversão de Versão|Sim|Sim|Sim|Não|Não|[Reversão de versão](/deployedge/edge-learnmore-rollback) |
|Guias Verticais|Sim|Sim|Sim|Sim|Sim| |

## <a name="see-also"></a>Confira também

- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)