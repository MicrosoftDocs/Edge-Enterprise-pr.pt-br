---
title: Edge para a infraestrutura da área de trabalho de Virtualização
ms.author: anlake
author: AndreaLBarr
manager: collw
ms.date: 06/08/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Microsoft Edge para Infraestrutura da Área de Trabalho Virtualizada.
ms.openlocfilehash: eaad1b72934b336ce86d14dd8da92a6984d21914
ms.sourcegitcommit: 4192328ee585bc32a9be528766b8a5a98e046c8e
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/25/2021
ms.locfileid: "11618005"
---
# <a name="microsoft-edge-for-virtualized-desktop-infrastructure"></a>Microsoft Edge para Infraestrutura da Área de Trabalho Virtualizada

Este artigo descreve os requisitos e limitações para o uso da Microsoft Edge em um ambiente virtualizado.

## <a name="what-is-vdi"></a>O que é VDI?

Virtual Desktop Infrastructure (VDI) é uma tecnologia de virtualização que hospeda um sistema operacional da área de trabalho e aplicativos em um servidor centralizado em um centro de dados. Isto permite uma experiência da área de trabalho totalmente personalizada para os usuários com uma fonte centralizada totalmente segura e compatível.

O Microsoft Edge pode ser usado em um ambiente virtualizado da mesma maneira que pode ser usado no dispositivo local, durante a execução em um ambiente de servidor seguro e controlado. Dependendo da solução VDI escolhida, também pode ser possível fornecer a seus usuários acesso sem problemas aos Aplicativos e Sites da intranet.

A maioria dos recursos do Edge são suportados em ambientes VDI sem nenhuma configuração especial. No entanto, para garantir uma experiência perfeita, é recomendável seguir as diretrizes abaixo.

## <a name="platforms-certified-for-edge"></a>Plataformas certificadas para o Edge

- Área de Trabalho Virtual do Azure
- Citrix Virtual Apps e Desktops (anteriormente conhecidos como XenApp e XenDesktop)

Embora outras soluções VDI ainda não tenham sido verificadas pela equipe do Edge, é esperado que os fluxos de trabalho mais comuns no Edge sejam apoiados. As diretrizes fornecidas abaixo podem ou não ser aplicáveis à solução escolhida.

## <a name="edge-on-vdi-performance-considerations"></a>Edge nas considerações de desempenho da VDI

Ao projetar seu ambiente VDI, você deve considerar cuidadosamente os fluxos de trabalho e as necessidades de seus usuários para alcançar o melhor desempenho, bem como os limites da configuração de seu servidor.

O Edge recomenda os seguintes requisitos mínimos para implantar o Edge em ambientes VDI:

- vCPU – 2-4 Núcleos por Usuário
- RAM – 1 GB por Usuário

Observe que grandes aplicativos web e extensões complexas exigirão mais memória e terão que ser contabilizadas ao configurar seu ambiente.

## <a name="edge-on-non-persisted-vdi-environments"></a>Edge em ambientes VDI não persistentes

Muitas soluções VDI permitem o acesso a ambientes persistentes, onde é atribuído aos usuários um ambiente virtual que persiste entre sessões, e ambientes não persistentes, onde os usuários são atribuídos a uma das várias máquinas disponíveis, possivelmente uma máquina diferente a cada sessão, os dados do usuário podem ou não sincronizar entre as sessões.

Ao usar um ambiente não persistente, geralmente é criada uma "imagem dourada" que é usada para cada dispositivo que inclui os aplicativos e configurações necessários. Abaixo estão nossas recomendações para preparar o Edge para essa imagem.

### <a name="deploy-edge"></a>Implante o Edge

Se você estiver no Windows 10, versão 1803 ou superior, você deve ter o Microsoft Edge instalado em seu sistema. No entanto, se você estiver em uma versão mais antiga do Windows ou desejar implantar um canal diferente do Edge, as seguintes etapas são recomendadas.

1. Baixe o pacote Edge MSI que combina com seu sistema operacional VDI VM de:

    - [Baixe o Microsoft Edge for Business - Microsoft](https://www.microsoft.com/edge/business/download)

2. Instale o MSI para o VDI VM executando o seguinte comando:

    - `msiexec /i <path_to_msi> /qn /norestart /l*v <install_logfile_name>`

### <a name="disable-automatic-updates"></a>Desabilite atualizações automáticas

Para máquinas não persistentes, é melhor desabilitar atualizações automáticas e, em vez disso, atualizar o Edge atualizando a "imagem dourada" para garantir que não haja incompatibilidades de versão entre o pool de máquinas.

Consulte as seguintes políticas para desabilitar atualizações automáticas:

- [Atualizar o padrão de substituição de política](/deployedge/microsoft-edge-update-policies#updatedefault)

- [Atualizar a substituição de política](/deployedge/microsoft-edge-update-policies#update)

### <a name="profile-management"></a>Gerenciamento de perfil

Em configurações não persistentes, é importante considerar que as VMs podem não manter o estado do usuário entre sessões ou os usuários podem ser atribuídos a uma VM que nunca usaram antes e, como tal, não tenha nenhum de seus dados de usuário.

O Edge suporta vários métodos para sincronizar os dados do usuário, de modo que esteja disponível independentemente de como eles estão acessando o Edge.

### <a name="azure-ad-sync"></a>Azure AD Sync

Se seu plano Microsoft Azure Active Directory o suporta, o Enterprise sync é o método mais rápido e fácil para garantir que os dados do usuário Edge sejam sincronizados com todos os dispositivos do usuário.  

Consulte o seguinte para obter mais informações sobre os requisitos e configuração.  

- [Configurar sincronização do Microsoft Edge enterprise | Microsoft Docs](/deployedge/microsoft-edge-enterprise-sync)

### <a name="on-premise-sync-for-active-directory-users"></a>Sincronização Local para Usuários do Active Directory

Com a sincronização local, o Microsoft Edge salva os favoritos e as configurações de um usuário do Active Directory em um arquivo que pode ser facilmente movido entre diferentes computadores.  

Consulte o seguinte para obter mais informações sobre os requisitos e configuração.  

- [Sincronização local para usuários do Active Directory (AD) | Microsoft Docs](/deployedge/microsoft-edge-on-premises-sync)

### <a name="user-profile-redirection"></a>Redirecionamento do Perfil do Usuário  

Há várias soluções para migrar e redirecionar toda a pasta do usuário para garantir que o contexto do usuário seja mantido nesses ambientes não persistentes. Verifique com seu provedor VDI para determinar a solução recomendada.

Algumas soluções populares incluem:

- [Visão geral do FSLogix - FSLogix | Microsoft Docs](/fslogix/overview)
- [Como Configurar o Gerenciamento de Perfil Citrix](https://support.citrix.com/article/CTX222893)

Também é recomendável que, ao usar esse método, pastas desnecessárias sejam excluídas da pasta do usuário com backup para reduzir os tempos de carregamento iniciais quando os usuários fazem logon em um computador e o perfil está sendo migrado. Em caso afirmativo, recomendamos que as pastas a seguir sejam excluídas de seu backup para reduzir o tamanho.

- %LocalAppData%\Microsoft\Edge\User Data\Default\Cache
- %LocalAppData%\Microsoft\Edge\User Data\Default\Code Cache
- %LocalAppData%\Microsoft\Edge\User Data\Default\JumpListIconsTopSites
- %LocalAppData%\Microsoft\Edge\User Data\Default\JumpListIconsRecentClosed

## <a name="known-issues"></a>Problemas conhecidos

### <a name="microsoft-edge-crashes-in-older-versions-of-xenapp-and-xendesktop"></a>Microsoft Edge falhas em versões mais antigas do XenApp e XenDesktop

Este problema deve ser mitigado em versões mais recentes, no entanto, se você estiver encontrando esse problema em seu ambiente, você pode resolver o problema desabilitando os Ganchos API Citrix para Edge, consulte [Como Desabilitar os Ganchos da API Citrix por Aplicativo.](https://support.citrix.com/article/CTX107825)

### <a name="degraded-performance-when-rendering-pages-with-exceptionally-large-html-tables"></a>Desempenho degradado ao renderizar páginas com tabelas HTML excepcionalmente grandes

As seguintes políticas da Citrix são conhecidas pela lenta renderização de páginas html com tabelas muito grandes (mais de 30.000 linhas).

- Exibição automática de teclado
- Caixa de combinação remota

Consulte [Configurações da política de experiência móvel (citrix.com)](https://docs.citrix.com/citrix-virtual-apps-desktops/policies/reference/ica-policy-settings/mobile-experience-policy-settings.html) para obter mais informações. A desabilitação dessas políticas deve mitigar a questão.

### <a name="windows-account-manager-authorization-scenarios-ie--azure-sync-fail-in-edge-when-run-as-a-citrix-seamless-application"></a>Windows Cenários de autorização do Gerenciador de Contas (ou seja,  Sincronização do Azure) falha no Edge quando executado como um aplicativo sem interrupção do Citrix

Esse é um problema conhecido no Edge e em outros aplicativos que usam WAM (ou seja, Office) devido Windows componentes necessários para esses cenários não serem inicializados ao executar no modo "contínuo". Para resolver esse problema:

- Use Edge por meio de uma Área de Trabalho Remota para o Host Citrix em vez de como um aplicativo remoto contínuo.
- Em vez disso, use aplicativos remotos da Área de Trabalho Virtual do Azure, que têm mitigação para esse problema.
