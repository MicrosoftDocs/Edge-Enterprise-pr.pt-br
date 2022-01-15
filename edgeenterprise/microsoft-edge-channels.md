---
title: Visão geral de canal do Microsoft Edge
ms.author: srugh
author: RyanHechtMSFT
manager: seanlynd
ms.date: 12/10/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Visão geral de canal do Microsoft Edge
ms.openlocfilehash: d18f7f501497d82d0b370a7ab028329a5fcbd036
ms.sourcegitcommit: e7f3098d8b7d91cae20b5778a71a87daababc312
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/15/2022
ms.locfileid: "12297619"
---
# <a name="overview-of-the-microsoft-edge-channels"></a>Visão geral dos canais do Microsoft Edge

Um dos benefícios da próxima versão do Microsoft Edge é que a Microsoft pode fornecer novos recursos regularmente. No entanto, como o administrador que implanta Microsoft Edge para usuários em sua organização, talvez você queira mais controle sobre a frequência com que seus usuários obterão esses novos recursos. A Microsoft fornece quatro opções, chamadas canais, para controlar a frequência Microsoft Edge é atualizada com novos recursos. Eis uma visão geral das quatro opções.

Para obter mais informações sobre o suporte para cada canal, leia: Microsoft Edge [Ciclo de Vida](/deployedge/microsoft-edge-support-lifecycle)
  
> [!NOTE]
> Este artigo se aplica ao Microsoft Edge versão 77 ou posterior.

## <a name="channel-overview"></a>Visão geral de canal

|Canal|Finalidade principal|Com que frequência atualizado com novos recursos|Com suporte?|
|:---:|---|:---:|:---:|
|[Estável](#stable-channel)|Implantação Ampla|~4 semanas|Sim|
|[Estável Estendido](#extended-stable-channel)|Uma opção de versão corporativa para Estável alinhada a um ciclo de lançamento mais longo |~8 semanas|Sim|
|[Beta](#beta-channel)|Validação do representante na organização|~4 semanas|Sim|
|[Dev](#dev-channel)|Planejamento e desenvolvimento|Semanalmente|Não|
|[Canary](#canary-channel)|Conteúdo do bleeding edge|Diário|Não|

O canal de atualização que você decide implantar depende de vários fatores. Por exemplo, o número de aplicativos de linha de negócios em uso afetará seus requisitos de teste sempre que houver Microsoft Edge atualização. Para ajudá-lo a tomar essa decisão, examine as seguintes informações sobre os quatro canais de atualização disponíveis para o Microsoft Edge.

### <a name="stable-channel"></a>Canal Estável

O Canal Estável destina-se à implantação ampla em sua organização, e é o canal em que a maioria dos usuários deve estar. É o mais estável dos canais e é o resultado da estabilização do conjunto de recursos disponível na versão anterior do Canal Beta. Novos recursos são dados a cada 4 semanas. As atualizações de qualidade e segurança são enviadas conforme o necessário. Um lançamento do Canal Estável é mantido até que o próximo lançamento do canal esteja disponível.

### <a name="beta-channel"></a>Canal Beta

O Canal Beta destina-se à implantação de produção para um conjunto de exemplos representativos de usuários. É uma versão com suporte, e cada versão de Beta é a ser a ser adida até que a próxima versão seja disponibilizada. Este canal oferece uma ótima oportunidade para validar que as coisas funcionam conforme esperado em seu ambiente. Se você encontrar um problema, ele poderá ser remediado antes que o lançamento seja publicado no Canal Estável. Novos recursos são dados a cada 4 semanas. As atualizações de qualidade e segurança são enviadas conforme o necessário.

### <a name="dev-channel"></a>Canal Dev

O Canal Dev destina-se a ajudá-lo a planejar e desenvolver com os recursos mais recentes do Microsoft Edge, mas com maior qualidade do que o canal Canary. Este canal é a oportunidade de ver o que está por vir e preparar-se para a próxima versão Beta.

### <a name="canary-channel"></a>Canal Canary

O Canal Canary é lançado diariamente e é o bleeding edge de todos os canais. Se você quiser acesso aos investimentos mais novos, eles aparecerão aqui primeiro. Devido à natureza dessa cadência, surgirão problemas ao longo do tempo. Você pode querer outro canal instalado lado a lado se estiver usando as versões canárias.

### <a name="extended-stable-channel"></a>Canal Estável Estendido

Ao contrário de nossos canais de visualização (Canary, Dev e Beta), o Canal Estável Estendido não está disponível como um aplicativo de navegador separado. Este canal é uma opção de lançamento empresarial para o Microsoft Edge aplicativo Estável que está alinhado a um ciclo de lançamento maior de 8 semanas. Isso se opõe ao ciclo de lançamento principal de quatro semanas para o canal Estável. Embora seja recomendável atualizar Estável em seu ciclo de 4 semanas de lançamento, o Estável Estendido existe para atender mais efetivamente as organizações que podem exigir uma linha do tempo mais longa para testar e validar novas versões do navegador.

A opção de versão "Estável Estendida" de 8 semanas para Microsoft Edge Estável fornece __ atualizações cumulativas de recursos que se alinham com versões com números mesmo começando com Microsoft Edge 94. As atualizações de recursos de versões com números ímpares serão empacotadas e entregues como parte da versão subsequente numerada. Por exemplo, se uma organização selecionar o ciclo de lançamento "Estável Estendido" de 8 semanas com o Microsoft Edge 94, eles receberão atualizações de recursos subsequentes com Microsoft Edge 96, Microsoft Edge 98 e assim por diante. Embora as atualizações de recursos sejam empacotadas e entregues com novas versões com base no ciclo de lançamento selecionado, correções e patches de segurança importantes serão entregues conforme necessário, independentemente da opção de versão selecionada para ajudar a manter a segurança do navegador. Os clientes podem optar pela opção de versão Estável Estendida a qualquer momento e entrarão em vigor com a próxima versão estável estendida.

![Exemplo de comparação Microsoft Edge opções de ciclo de versão estável e estendida.](./media/microsoft-edge-channels/extended-stable-explainer.png)

#### <a name="opting-in-to-the-extended-stable-release-cadence"></a>Opting in to the Extended Stable Release Ence

##### <a name="opting-in-to-extended-stable-on-windows-with-automatic-updates-recommended"></a>Opting to Extended Stable on Windows with Automatic Updates (recommended)

Se você atualizar automaticamente Microsoft Edge, poderá usar objetos de política de grupo para optar pela Cadência de Versão Estável Estendida. [Siga este guia](/DeployEdge/configure-microsoft-edge#1-download-and-install-the-microsoft-edge-administrative-template) para obter mais informações sobre como baixar e instalar os modelos administrativos mais recentes Microsoft Edge Política de Grupo.

1. Abra o Editor de política de grupo local e acesse _Configuração do computador>Atualização do Microsoft Edge>Aplicativos>Microsoft Edge>_.
2. Selecione **Substituir canal de destino** e selecione **Habilitado**.
3. Em **Opções,** escolha **"Estável Estendido"** na lista suspenso Política.

Quando a próxima atualização para o canal Estável Estendido for lançada com um número de versão maior do que o que seu dispositivo instalou no momento, o Microsoft Edge atualizará automaticamente para o canal Estável Estendido. A cadeia de `edge://settings/help` caracteres de versão em indicará que você está executando um canal diferente.

> [!NOTE]
> A aceitação de Estável Estendido entrará em vigor quando houver uma nova atualização no canal Estável Estendido com um número de versão maior (principal ou menor) do que o que está instalado no momento em seu dispositivo. Se você estiver executando a versão mais recente do Microsoft Edge Estável e aceitar em Estável Estendido, ele entrará em vigor com o próximo patch ou atualização do Microsoft Edge.
>
> Por padrão, Microsoft Edge não se rebaixará. Se você estiver executando uma versão com número ímpar do Microsoft Edge Estável, a aceitação para Estável Estendido significa que você receberá atualizações NO até o próximo lançamento com número Microsoft Edge.
>
> Se você quiser garantir que todos os seus dispositivos comecem com uma versão específica do Extended Stable, você pode implantar essa versão específica do Edge Stable como um MSI com reversões habilitadas. Por exemplo, se você quiser começar com o Extended Stable 94, mas alguns dispositivos já foram atualizados para o Estável 95, você pode implantar um MSI da Borda 94 com a reação habilitada. Para obter mais informações sobre como implantar MSIs de Borda com a reação habilitada, consulte nosso guia [de rebaixamento.](/DeployEdge/edge-learnmore-rollback)

##### <a name="opting-in-to-extended-stable-on-windows-via-intune"></a>Opting in to Extended Stable on Windows via Intune

Microsoft Edge Modelos Administrativos podem ser gerenciados da mesma forma que os Objetos de Política de Grupo locais do Microsoft Endpoint Manager de administração. Siga nosso [guia sobre como configurar Microsoft Edge com o Intune](/mem/intune/configuration/administrative-templates-configure-edge). 

A**configuração**" Substituição de Canal de Destino " pode ser encontrada nas subpastas "_Microsoft Edge Update >Applications>Microsoft Edge_". Ele deve ser definido como "**Estável Estendido**" 

Quando a próxima atualização para o canal Estável Estendido for lançada com um número de versão maior do que o que seu dispositivo instalou no momento, o Microsoft Edge atualizará automaticamente para o canal Estável Estendido. A cadeia de `edge://settings/help` caracteres de versão em indicará que você está executando um canal diferente.

##### <a name="opting-in-to-extended-stable-on-windows-via-configuration-manager"></a>Opting in to Extended Stable on Windows via Configuration Manager

Consulte nosso guia sobre a atualização do Microsoft Edge com o [Configuration Manager](/mem/configmgr/apps/deploy-use/deploy-edge#update-microsoft-edge) para obter mais informações sobre como sincronizar e aprovar Microsoft Edge atualizações no Configuration Manager.

As atualizações estáveis estendidas são distribuídas na biblioteca de software na categoria de produto "Microsoft Edge", semelhante às atualizações existentes para os canais Estável, Beta e Desenvolvimento. No entanto, ao contrário de Beta e Dev, que se aplicam aos seus próprios aplicativos de navegador, as atualizações Estáveis Estendidas se aplicam Microsoft Edge aplicativo Estável. Portanto, para seu cliente Windows Update para determinar se deve aplicar atualizações estáveis ou estendidas, ele verifica o status da política de grupo "Substituição de Canal de Destino". Se a política não estiver configurada ou estiver definida como "Estável", as atualizações estáveis serão aplicadas. Se estiver definido como "Estável Estendido", as atualizações Estáveis Estendidas serão aplicadas. Siga as instruções acima para optar por Estável Estendido com Atualizações Automáticas para obter instruções sobre como definir corretamente a Política de Grupo. 

## <a name="flighting-pre-release-channels-in-your-organization"></a>Pré-lançamento de canais de pré-lançamento em sua organização

A política de grupo "Substituição de Canal de Destino" também pode ser usada para liberar perfeitamente os canais de pré-lançamento do Microsoft Edge em sua organização sem que os usuários precisem usar um segundo aplicativo de navegador da Web. Por exemplo, você pode definir a política "Substituição de Canal de Destino" como "Beta" para um conjunto de exemplos representativos de usuários em sua organização. Quando esses usuários abrirem Microsoft Edge, eles estarão executando o lançamento do canal Beta em vez de Estável (provavelmente sem nem perceber!). Essa configuração de política pode dar uma visão antecipada de como a próxima versão do Microsoft Edge funcionará em sua empresa e ajudar a validar que tudo funciona conforme esperado. Você obterá sinais antecipados de seus usuários que encontrarem qualquer problema e podem garantir que eles sejam remediados antes da versão ser publicada no Canal Estável. Como parte da solução de problemas de um problema do usuário, a cadeia de caracteres de versão em informará se o canal do usuário é diferente do `edge://settings/help` canal estável padrão.

> [!NOTE]
> Como o build nos canais "Beta" e "Dev" do Microsoft Edge tem números de versão maiores do que o de "Estável", se você receber uma atualização para o canal "Beta" ou "Dev" e desejar reverter para Estável, o recurso de reversão do [Microsoft Edge](/DeployEdge/edge-learnmore-rollback) será necessário. Simplesmente definir "Substituição de Canal de Destino" de volta como Estável significa que você receberá nenhuma atualização até que a versão estável mais recente tenha um número de versão maior do que a versão do Microsoft Edge que você está executando no seu dispositivo.

## <a name="see-also"></a>Consulte também

- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Downloads de canal](https://aka.ms/EdgeEnterprise)
