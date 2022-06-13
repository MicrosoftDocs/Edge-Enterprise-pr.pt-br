---
title: Planejar sua implantação do Microsoft Edge
ms.author: collw
author: dan-wesley
manager: srugh
ms.date: 12/08/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Planejar sua implantação do Microsoft Edge
ms.openlocfilehash: e49008b9d7ce7af1d44581397c82fc5fb3e248f1
ms.sourcegitcommit: 2d3e2a7180e2df82b6345865c201ad64731cbda7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/12/2022
ms.locfileid: "12582016"
---
# <a name="plan-your-deployment-of-microsoft-edge"></a>Planejar sua implantação do Microsoft Edge

Este artigo descreve as práticas recomendadas para implantar o Microsoft Edge em um ambiente corporativo.

>[!NOTE]
>Este artigo se aplica ao Microsoft Edge versão 77 ou posterior.

## <a name="article-content"></a>Conteúdo do artigo

As seções a seguir fornecem orientações específicas para o planejamento da implantação do Microsoft Edge.

   - [Avaliar seu ambiente do navegador e as necessidades do navegador](#evaluate-your-existing-browser-environment-and-browser-needs)
  - [Certifique-se de que seus dispositivos Windows 10 estejam prontos](#make-sure-your-windows-10-devices-are-ready)
  - [Determinar a metodologia de sua implantação](#determine-your-deployment-methodology)
    - [Implantar para usuários finais por função](#deploy-to-end-users-by-role)
    - [Implantar para usuários por site](#deploy-to-end-users-by-site)
  - [Fazer descoberta de site](#do-site-discovery)
    - [Se você já implantou e configurou a versão herdada do Microsoft Edge](#if-youve-already-deployed-and-configured-the-legacy-version-of-microsoft-edge)
    - [Se você configurou o Internet Explorer como navegador padrão](#if-youve-configured-internet-explorer-as-your-default-browser)
    - [Analisar dados da descoberta de site](#analyze-site-discovery-data)
  - [Determinar sua estratégia de canal](#determine-your-channel-strategy)
    - [Vários dispositivos e canais](#multiple-devices-and-channels)
  - [Definir e configurar políticas](#define-and-configure-policies)
    - [Definir sua estratégia de atualização e políticas](#define-your-update-strategy-and-policies)
  - [Fazer o teste de compatibilidade do aplicativo](#do-app-compatibility-testing)
    - [Teste de aplicativo de linha interna de negócios](#internal-line-of-business-app-testing)
    - [Suporte a aplicativos de terceiros](#third-party-app-support)
  - [Implantar o Microsoft Edge em um grupo piloto](#deploy-microsoft-edge-to-a-pilot-group)
  - [Validar a implantação](#validate-your-deployment)
  - [Implantação ampla do Microsoft Edge](#broad-deployment-of-microsoft-edge)
  - [Consulte também](#see-also)

## <a name="evaluate-your-existing-browser-environment-and-browser-needs"></a>Avaliar seu ambiente do navegador e as necessidades do navegador

Reserve um tempo para entender o estado atual do navegador e a visão do projeto para garantir que todas as partes interessadas do projeto estejam alinhados e trabalhando para atingir o mesmo resultado.

Comece definindo o estado atual:

- Quais navegadores estão implantados no ambiente atualmente?
- Qual navegador está definido como navegador padrão?
- Você precisa usar o Internet Explorer para alguns aplicativos?
- Você usa uma lista de sites do modo empresarial para configurar o Internet Explorer atualmente?
- Quais plataformas de sistema operacional são compatíveis com seu ambiente? (Windows 10, macOS, Windows 7, Windows Server etc.)
- Quais ferramentas de gerenciamento você usa para o gerenciamento do navegador?
- Quem é responsável pelo gerenciamento e pela configuração do navegador?
- Qual é o seu processo para validar a compatibilidade do navegador?

Depois de entender o estado atual, você poderá determinar as metas desejadas para a implantação do navegador, levando em conta o seguinte:

- Deseja [definir o Microsoft Edge como navegador padrão](./edge-default-browser.md)?
- Como você [configurará o Microsoft Edge](./configure-microsoft-edge.md)?
- Quais recursos são cruciais para serem configurados como parte da implantação inicial?
- Qual é o processo para abordar problemas identificados de compatibilidade ou configuração?

Você também deve entender os **pré-requisitos** para recursos nos quais está interessado, como:

- [Windows Defender Application Guard](/windows/security/threat-protection/windows-defender-application-guard/reqs-wd-app-guard)
- [Modo Internet Explorer](./edge-ie-mode.md)
- [Autenticação e sincronização](./microsoft-edge-security-identity.md)

Com essas respostas em mente, você está pronto para planejar a implantação do Microsoft Edge.
<!--bookmark -->

## <a name="make-sure-your-windows-10-devices-are-ready"></a>Certifique-se de que seus dispositivos Windows 10 estejam prontos

O canal estável do Microsoft Edge exige a atualização cumulativa mais recente (LCU) de outubro de 2019 (ou posterior). Se você tentar implantar em um dispositivo com Windows 10 que tenha um LCU mais antigo, a instalação falhará. Para obter mais detalhes sobre as LCU mínimas que devem ser aplicadas antes da implantação do Microsoft Edge, confira [atualizações do Windows que oferecem suporte à próxima versão do Microsoft Edge](./microsoft-edge-sysupdate-windows-updates.md).

## <a name="determine-your-deployment-methodology"></a>Determinar a metodologia de sua implantação

Depois de saber o estado final desejado, você estará pronto para começar a planejar como chegar lá. As duas principais maneiras de implantar o Microsoft Edge são por função e por site.

### <a name="deploy-to-end-users-by-role"></a>Implantar para usuários finais por função

Se a compatibilidade do aplicativo for sua principal preocupação, e você não tiver um bom controle sobre quais aplicativos testar, considere implantar para usuários finais por função. Isso permite que cada onda de uma implantação em fases forneça comentários e insights sobre aplicativos que talvez precisem ter a configuração modificada para resolver problemas de compatibilidade.

### <a name="deploy-to-end-users-by-site"></a>Implantar para usuários por site

Se a largura de banda for sua principal preocupação, considere fazer o teste de compatibilidade de aplicativos antecipadamente. Depois de concluir o teste, implante-os para usuários finais por site, para que você possa aproveitar o cache de outras otimizações de entrega de software.

## <a name="do-site-discovery"></a>Fazer descoberta de site

Se você tiver uma dependência em aplicativos web herdados e planejar usar o modo Internet Explorer (que é o caso da maioria dos clientes), provavelmente precisará de uma descoberta de site adicional.

### <a name="if-youve-already-deployed-and-configured-the-legacy-version-of-microsoft-edge"></a>Se você já implantou e configurou a versão herdada do Microsoft Edge

Se você já configurou a lista de sites do modo empresarial para funcionar na versão herdada do Microsoft Edge, seu trabalho está quase pronto. Algo que você talvez precise adicionar são sites neutros.

Sites neutros geralmente são sites que oferecem logon único (SSO). Se você navegar até um site neutro no Microsoft Edge, poderá permanecer no Microsoft Edge para autenticar. Se você navegar até um site neutro no modo Internet Explorer, convém permanecer no modo do Internet Explorer para autenticar.

Identifique os sites com SSO (ou outros tipos neutros) usados e adicione-os à sua lista de sites do modo empresarial.

### <a name="if-youve-configured-internet-explorer-as-your-default-browser"></a>Se você configurou o Internet Explorer como navegador padrão

Se você estiver usando somente o Internet Explorer, talvez não saiba quais sites atualizaram para padrões modernos da Web e quais ainda exigem o Internet Explorer. Convém encontrar esses sites e adicioná-los à lista de sites do modo empresarial. Isso permite que você use o modo Internet Explorer somente nos sites que precisam dele.

> [!TIP]
> Use as ferramentas do [Enterprise Site Discovery](/internet-explorer/ie11-deploy-guide/collect-data-using-enterprise-site-discovery) para descobrir os sites que podem precisar do modo Internet Explorer. Você pode coletar dados em computadores que executam do Windows Internet Explorer 8 até o Internet Explorer 11 no Windows 10, no Windows 8.1 ou no Windows 7.

### <a name="analyze-site-discovery-data"></a>Analisar dados da descoberta de site

Depois de coletar os dados do site, recomendamos o seguinte processo de 4 etapas para analisar os dados:

1. Classifique os dados por domínio e, em seguida, por URL.
2. Defina os limites de um "aplicativo" para configurar para o modo Internet Explorer. Convém incluir todos os sites e controles da Web que definem o aplicativo. Porém, não convém incluir sites e controles adicionais definindo o aplicativo muito amplamente. Alguns sites podem ser tão simples quanto "http://contoso.com/app1", enquanto outros podem exigir que você defina vários sites e páginas.
3. Teste o aplicativo para verificar se ele não funciona nativamente. Muitos sites oferecerão conteúdo moderno quando detectarem um navegador moderno e só oferecerão conteúdo herdado quando detectarem o Internet Explorer.
4. Adicione o aplicativo à sua lista de sites do modo empresarial se ele não passar no teste.

   > [!NOTE]
   > Como prática recomendada, agrupe todos os sites que compõem um aplicativo. Se os todos sites precisam ser usados para realizar uma tarefa, e se eles tendem a serem atualizados juntos, é uma boa indicação de que eles devem ser agrupados. Dessa forma, ao atualizar um aplicativo, é mais fácil remover todo o site do modo Internet Explorer e começar a usar um navegador moderno para esse aplicativo.

## <a name="determine-your-channel-strategy"></a>Determinar sua estratégia de canal

O Microsoft Edge é lançado em [vários canais](./microsoft-edge-channels.md).

> [!NOTE]
> Você pode instalar mais de um canal em um dispositivo

O canal estável é o que convém implantar na maioria dos dispositivos. No entanto, você deve considerar uma estratégia de implantação que inclua vários dispositivos e vários canais.

### <a name="multiple-devices-and-channels"></a>Vários dispositivos e canais

Recomendamos ter um subconjunto representativo de dispositivos configurados para usar o canal Beta. Isso permite que você visualize futuras alterações no navegador. Você pode ver se essas alterações afetarão os usuários finais ou aplicativos.

Também convém disponibilizar o canal do Desenvolvedor (ou até mesmo o canal Canary) para algumas funções, como desenvolvedores da Web. Considere se você deseja atribuir a alguns dispositivos canais mais fluidos e em constante mudança ou simplesmente disponibilizar esses canais para que os usuários optem por instalar.

Como é possível instalar vários canais em um dispositivo, você pode mitigar o risco de teste para os usuários que optaram por instalar um canal de pré-lançamento. Por exemplo, se você tiver um usuário que está usando o canal Beta e houver um problema, eles poderão alternar para o canal Estável e continuar trabalhando. Isso libera-os até que o problema possa ser corrigido.

> [!NOTE]
> Se o usuário habilitou a sincronização, a configuração será sincronizada em todos os canais, facilitando ainda mais a transição entre canais.

## <a name="define-and-configure-policies"></a>Definir e configurar políticas

Depois de criar sua lista de sites do modo empresarial, recomendamos identificar e configurar as políticas que você pretende implantar com o Microsoft Edge. Isso garante que essas políticas sejam aplicadas ao realizar o teste.

Primeiro, considere a experiência de primeira execução que você deseja que os usuários tenham. Se você quiser importar automaticamente as configurações do navegador atual, configure a política para [AutoImportAtFirstRun.](./microsoft-edge-policies.md#autoimportatfirstrun)

Para políticas de segurança, recomendamos começar com a linha de base de segurança do Microsoft Edge. A Linha de Base de Segurança pode ser aplicada usando o Blog de Linhas de Base de Segurança da [Microsoft](https://techcommunity.microsoft.com/t5/microsoft-security-baselines/bg-p/Microsoft-Security-Baselines) ou usando [Microsoft Intune](/intune/protect/security-baseline-settings-edge).

Para outras políticas, é recomendável analisar as configurações de política para o [Microsoft Edge](./microsoft-edge-policies.md) e as [Atualizações do Microsoft Edge](./microsoft-edge-update-policies.md).

### <a name="define-your-update-strategy-and-policies"></a>Definir sua estratégia de atualização e políticas

Também convém determinar como deseja fazer atualizações depois de implantar o Microsoft Edge:

- **Permitir que o Microsoft Edge se atualize** (padrão). Se você optar por permitir atualizações automáticas do Microsoft Edge, o Microsoft Edge se atualizará automaticamente atualizado no ritmo determinado pelos canais implantados.
- **Atualizar o Microsoft Edge em seu próprio ritmo**. Se você preferir ter um controle explícito sobre quando as atualizações são implantadas, poderá desabilitar as atualizações automáticas e implantá-las você mesmo, (consulte a [Referência da política de atualização](./microsoft-edge-update-policies.md). Depois de desabilitar as atualizações automáticas, você pode implantar atualizações para cada canal usando uma das seguintes ferramentas:

- [Intune](/intune/apps/apps-windows-edge?bc=%2fDeployEdge%2fbreadcrumb%2ftoc.json&toc=%2fDeployEdge%2ftoc.json)
- [Gerenciador de Configurações](./deploy-edge-with-configuration-manager.md)
- a ferramenta de implantação de sua escolha.

Independentemente de sua estratégia de atualização, recomendamos o uso de uma estratégia de implantação anelada. Com as atualizações automáticas, isso significa ter uma amostra representativa de usuários executando o canal Beta, para identificar problemas com o que se tornará o canal Estável. Com as atualizações manuais, isso também pode incluir uma validação adicional de um grupo piloto após o lançamento de um novo build do canal Estável. Isso é seguido por uma implantação abrangente.

>[!NOTE]
>O suporte do Microsoft Edge só será aplicado à versão mais recente do Microsoft Edge em cada canal

## <a name="do-app-compatibility-testing"></a>Fazer o teste de compatibilidade do aplicativo

A compatibilidade do aplicativo com o Microsoft Edge é extremamente alta; tão alta que a Microsoft oferece as seguintes promessas de compatibilidade:

1. Se funcionar no Microsoft Edge *versão 45 e anterior*, ele funcionará no Microsoft Edge *versão 77 e posterior*.
2. Se funcionar no Internet Explorer, ele funcionará no Microsoft Edge no modo Internet Explorer.
3. Se funcionar no Google Chrome, ele funcionará no Microsoft Edge.

Se você tiver um aplicativo em que não cumprimos nossa promessa de compatibilidade, cumpriremos a promessa de corrigi-lo com[Aplicativo do Microsoft Assure](https://www.microsoft.com/fasttrack/microsoft-365/desktop-app-assure).

### <a name="internal-line-of-business-app-testing"></a>Teste de aplicativo de linha interna de negócios

Apesar de nossa promessa de compatibilidade, sabemos que muitas organizações devem validar alguns aplicativos por motivos de conformidade ou gerenciamento de risco. Embora esperemos que isso seja muito simples, é importante ser organizado e rigoroso no teste de aplicativos.

Há duas maneiras de fazer o teste de compatibilidade de aplicativos:

1. Testes de laboratório. Os aplicativos são validados em um ambiente totalmente controlado com configurações específicas.
2. Testes piloto. Os aplicativos são validados por um número limitado de usuários em seu ambiente de trabalho diário usando seus próprios dispositivos.

Escolha o método mais adequado para cada aplicativo, para gerenciar riscos sem muito investimento no teste de compatibilidade.

### <a name="third-party-app-support"></a>Suporte a aplicativos de terceiros

Além de seus próprios aplicativos de linha de negócios, muitas organizações usam aplicativos fornecidos por fontes externas. O artigo [Pronto para o Microsoft Edge](deploy-edge-ready-for-edge.md) contém uma lista de aplicações web que podem estar em uso dentro de sua organização. Esta lista fornece links para declarações de suporte do provedor para seus produtos quando usados com o Microsoft Edge.

## <a name="deploy-microsoft-edge-to-a-pilot-group"></a>Implantar o Microsoft Edge em um grupo piloto

Depois de definir as políticas e concluir o teste de compatibilidade inicial do aplicativo, você estará pronto para implantá-lo no grupo piloto. Implante no grupo piloto usando uma das seguintes ferramentas:

- [Microsoft Intune para Windows](/intune/apps/apps-windows-edge?bc=%2fDeployEdge%2fbreadcrumb%2ftoc.json&toc=%2fDeployEdge%2ftoc.json) ou [Microsoft Intune para macOS](/intune/apps/apps-edge-macos?bc=%2fDeployEdge%2fbreadcrumb%2ftoc.json&toc=%2fDeployEdge%2ftoc.json)
- [Gerenciador de Configurações](./deploy-edge-with-configuration-manager.md).
- Outra ferramenta de gerenciamento, baixe e implante o [Arquivo MSI para o Microsoft Edge](https://www.microsoftedgeinsider.com/enterprise).

## <a name="validate-your-deployment"></a>Validar a implantação

Depois de implantar o piloto, convém capturar todos os comentários obtidos com seus usuários.

- Capture comentários sobre a compatibilidade. Identifique os sites que pertencem à lista de sites do modo empresarial que não foram identificados durante a descoberta de site.
- Capture comentários sobre a configuração de política. Verifique se os usuários podem usar os principais recursos e fazer seu trabalho ao seguirem as diretrizes de segurança.
- Capture comentários sobre a facilidade de uso e novos recursos. Identifique as áreas em que um treinamento deve ser desenvolvido e entregue com base nas perguntas dos usuários.

## <a name="broad-deployment-of-microsoft-edge"></a>Implantação ampla do Microsoft Edge

Depois de concluir o piloto e atualizar o plano de implantação com as lições aprendidas no piloto, você estará pronto para fazer uma implantação completa do Microsoft Edge a todos os usuários.  Parabéns!

## <a name="see-also"></a>Ver também

- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Vídeo - Implantar o Microsoft Edge](microsoft-edge-video-deploy.md)
