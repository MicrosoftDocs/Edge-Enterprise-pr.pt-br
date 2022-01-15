---
title: Microsoft Edge infraestrutura de área de trabalho virtual (VDI)
ms.author: anlake
author: dan-wesley
manager: collw
ms.date: 11/12/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Microsoft Edge infraestrutura de área de trabalho virtual (VDI).
ms.openlocfilehash: fe1c1a7acf0b514812ff0aaf8f7a2b307304657d
ms.sourcegitcommit: e7f3098d8b7d91cae20b5778a71a87daababc312
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/15/2022
ms.locfileid: "12298129"
---
# <a name="microsoft-edge-for-virtual-desktop-infrastructure-vdi"></a>Microsoft Edge infraestrutura de área de trabalho virtual (VDI)

Este artigo descreve os requisitos e limitações para o uso Microsoft Edge em um ambiente virtual.

## <a name="what-is-vdi"></a>O que é VDI?

A infraestrutura de área de trabalho virtual (VDI) é uma tecnologia de virtualização de área de trabalho que hospeda um sistema operacional e aplicativos em um servidor centralizado em um data center. Essa tecnologia permite uma experiência de área de trabalho totalmente personalizada para usuários em uma fonte centralizada segura e compatível.

Microsoft Edge pode ser usado em um ambiente virtual da mesma maneira que é usado em um dispositivo local. Uma área de trabalho virtual aproveita um ambiente de servidor seguro e controlado. Dependendo da solução VDI escolhida, também pode ser possível dar aos usuários acesso contínuo a aplicativos e sites da intranet.

A maioria Microsoft Edge recursos são suportados em ambientes VDI sem qualquer configuração especial. No entanto, para garantir uma experiência ideal, recomendamos que você revise as seguintes diretrizes.

## <a name="platforms-certified-for-microsoft-edge"></a>Plataformas certificadas para Microsoft Edge

As seguintes plataformas são certificadas para Microsoft Edge:

- Área de Trabalho Virtual do Azure
- Citrix Virtual Apps e Desktops (anteriormente conhecidos como XenApp e XenDesktop)

Embora outras soluções VDI ainda não tenham sido certificadas pela equipe Microsoft Edge, é esperado que os fluxos de trabalho mais comuns no Microsoft Edge sejam suportados. As diretrizes a seguir podem ou não ser aplicáveis à solução escolhida.

## <a name="performance-considerations-for-microsoft-edge-on-vdi"></a>Considerações de desempenho para Microsoft Edge em VDI

Ao projetar seu ambiente VDI, considere cuidadosamente os fluxos de trabalho e as necessidades de seus usuários para obter o desempenho ideal e compreender os limites da configuração do seu servidor.

Os seguintes requisitos mínimos são recomendados para implantar Microsoft Edge em um ambiente VDI:

- vCPU – 2 a 4 núcleos por usuário
- RAM – 1 GB por Usuário

Aplicativos e extensões da Web grandes e complexos precisarão de mais memória e capacidade de processamento, o que deve ser considerado ao configurar seu ambiente virtual.

## <a name="microsoft-edge-on-non-persisted-vdi-environments"></a>Microsoft Edge em ambientes VDI não persistentes

Muitas soluções VDI permitem o acesso a ambientes persistentes, onde é atribuído aos usuários um ambiente virtual que persiste entre sessões, e ambientes não persistentes, onde os usuários são atribuídos a uma das várias máquinas disponíveis, possivelmente uma máquina diferente a cada sessão, os dados do usuário podem ou não sincronizar entre as sessões.

Ao usar um ambiente não persistente, geralmente se cria uma "imagem dourada" que tem os aplicativos e configurações necessários que serão implantados em cada dispositivo. Use as seguintes recomendações como um guia para preparar uma imagem dourada.

### <a name="deploy-microsoft-edge"></a>Implantar o Microsoft Edge

Se você estiver Windows 10, versão 1803 ou superior, já deve ter Microsoft Edge instalado em seu sistema. No entanto, se você estiver usando uma versão mais antiga do Windows ou quiser implantar um canal Microsoft Edge diferente, siga estas etapas:

1. Baixe o Microsoft Edge MSI que corresponde ao seu sistema operacional VDI VM de:

    - [Baixe o Microsoft Edge for Business - Microsoft](https://www.microsoft.com/edge/business/download)

2. Execute o seguinte comando para instalar o MSI na VM (máquina virtual VDI):

    - `msiexec /i <path_to_msi> /qn /norestart /l*v <install_logfile_name>`

### <a name="disable-automatic-updates"></a>Desabilite atualizações automáticas

Para máquinas não persistentes, a melhor prática é desabilitar as atualizações automáticas e atualizar o Microsoft Edge atualizando a imagem dourada para garantir que não haja incompatibilidades de versão entre o pool de máquinas virtuais.

Para obter mais informações sobre como desabilitar atualizações automáticas, consulte as seguintes políticas:

- [Atualizar o padrão de substituição de política](/deployedge/microsoft-edge-update-policies#updatedefault)

- [Atualizar a substituição de política](/deployedge/microsoft-edge-update-policies#update)

### <a name="profile-management"></a>Gerenciamento de perfil

Em configurações não persistentes, é importante considerar que as VMs podem não manter o estado do usuário entre sessões ou os usuários podem ter uma VM que nunca usaram antes. Nesse cenário, a VM não tem nenhum dos dados do usuário.

Microsoft Edge dá suporte a vários métodos para sincronizar dados do usuário para que eles sejam disponibilizados independentemente de como eles estão acessando Microsoft Edge. Dois métodos são Azure Active Directory sincronização (Azure AD) e sincronização local para usuários do AD.

### <a name="azure-ad-sync"></a>Azure AD Sync

Se o plano do Azure AD for compatível com ele, Enterprise sincronização é o método mais rápido e mais fácil para garantir que os dados do usuário Microsoft Edge sincronizados com todos os dispositivos do usuário. Para obter mais informações, consulte [Configure Microsoft Edge enterprise sync](/deployedge/microsoft-edge-enterprise-sync)

### <a name="on-premise-sync-for-active-directory-users"></a>Sincronização Local para Usuários do Active Directory

Com a sincronização local, o Microsoft Edge salva os favoritos e as configurações de um usuário do Active Directory em um arquivo que pode ser facilmente movido entre diferentes computadores.  

Para obter mais informações sobre requisitos e configuração, consulte Sincronização local para usuários do [Active Directory (AD)](/deployedge/microsoft-edge-on-premises-sync)

### <a name="user-profile-redirection"></a>Redirecionamento do Perfil do Usuário  

Há várias soluções para migrar e redirecionar toda a pasta do usuário para garantir que o contexto do usuário seja mantido em um ambiente não persistente. Verifique com seu provedor VDI para determinar a solução recomendada para seu ambiente.

Algumas soluções populares incluem as seguintes opções:

- [Visão geral do FSLogix - FSLogix](/fslogix/overview)
- [Como Configurar o Gerenciamento de Perfil Citrix](https://support.citrix.com/article/CTX222893)

Em alguns casos, pastas desnecessárias devem ser excluídas da pasta do usuário com backup para reduzir os tempos de carregamento iniciais quando um usuário faz logon em um computador e seu perfil está sendo migrado. Em caso afirmativo, recomendamos que as pastas a seguir sejam excluídas de seu backup para reduzir o tamanho.

- %LocalAppData%\Microsoft\Edge\User Data\Default\Cache
- %LocalAppData%\Microsoft\Edge\User Data\Default\Code Cache
- %LocalAppData%\Microsoft\Edge\User Data\Default\JumpListIconsTopSites
- %LocalAppData%\Microsoft\Edge\User Data\Default\JumpListIconsRecentClosed

## <a name="known-issues"></a>Problemas conhecidos

### <a name="microsoft-edge-crashes-in-older-versions-of-xenapp-and-xendesktop"></a>Microsoft Edge falhas em versões mais antigas do XenApp e XenDesktop

Esse problema deve ser atenuado em versões mais recentes desses produtos. No entanto, se você estiver encontrando esse problema em seu ambiente, poderá resolver o problema desabilitando os Ganchos de API citrix para Microsoft Edge, consulte [How to Disable Citrix API Hooks on a Per-application Basis.](https://support.citrix.com/article/CTX107825)

### <a name="degraded-performance-when-rendering-pages-with-exceptionally-large-html-tables"></a>Desempenho degradado ao renderizar páginas com tabelas HTML excepcionalmente grandes

As seguintes políticas citrix são conhecidas por renderização lenta de páginas html com tabelas grandes (30.000+ linha).

- Exibição automática de teclado
- Caixa de combinação remota

Para obter mais informações, consulte Configurações de política de experiência [móvel (citrix.com)](https://docs.citrix.com/citrix-virtual-apps-desktops/policies/reference/ica-policy-settings/mobile-experience-policy-settings.html) para obter mais informações. A desabilitação dessas políticas deve mitigar a questão.

### <a name="windows-account-manager-authorization-scenarios-that-is-azure-sync-fail-in-microsoft-edge-when-run-as-a-citrix-seamless-application"></a>Windows cenários de autorização do Gerenciador de Conta (ou seja, sincronização do Azure) falham no Microsoft Edge quando executados como um aplicativo sem interrupção do Citrix

Esse é um problema conhecido no Microsoft Edge e em outros aplicativos que usam o WAM (ou seja, Office) devido aos componentes de Windows necessários que não estão sendo inicializados durante a execução no modo "contínuo". Experimente uma das seguintes opções para resolver esse problema:

- Use Microsoft Edge por meio de uma Área de Trabalho Remota para o Host Citrix em vez de um aplicativo remoto contínuo.
- Em vez disso, use aplicativos remotos da Área de Trabalho Virtual do Azure, que tem mitigações para esse problema.

## <a name="see-also"></a>Consulte também

- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Área de Trabalho Virtual do Azure](https://azure.microsoft.com/services/virtual-desktop/)