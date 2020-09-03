---
title: Reversão do Microsoft Edge para empresas
ms.author: v-danwes
author: dan-wesley
manager: srugh
ms.date: 09/02/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Como reverter o Microsoft Edge para uma versão anterior
ms.openlocfilehash: 9f659b0bcdd82f54a814c8ad4157521061cdfa7c
ms.sourcegitcommit: 827a47d641c7ddc1d89be5d5fc0615373dec18b0
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993701"
---
# Como reverter o Microsoft Edge para uma versão anterior

Este artigo descreve como reverter para uma versão anterior do Microsoft Edge usando o recurso de reversão.

>[!NOTE]
>Este artigo se aplica ao Microsoft Edge versão 86 ou posterior.

## Introdução à reversão

A reversão permite que você substitua a versão do navegador Microsoft Edge por uma versão anterior. Esse recurso foi projetado para ser uma rede de segurança para empresas que implantam o Microsoft Edge. Ele oferece uma maneira de solucionar problemas com o Microsoft Edge. Os benefícios da reversão são a possibilidade de reverter para a versão anterior do navegador de forma fácil e rápida. A reversão reduz o impacto potencial causado por um problema com o Microsoft Edge nas operações de negócios.

## Antes de começar

É importante compreender como o recurso de reversão está instalado em um ambiente do Microsoft Edge. Você pode implantar a reversão ao usar dois métodos diferentes: manualmente com, um MSI ou ao usar a atualização do Microsoft Edge e a Política de grupo. Também incentivamos o uso de uma seleção das Políticas de grupo para se ter uma implantação mais suave.

### Recomendações

O recurso de reversão é destinado a ser uma correção temporária dos problemas que você possa encontrar em uma atualização do navegador Microsoft Edge. Recomendamos que os usuários instalem a versão mais recente do navegador Microsoft Edge para usar a proteção oferecida pelas atualizações de segurança mais recentes. Reverter para uma versão anterior corre o perigo de se expor aos problemas de segurança conhecidos.

Antes de reverter temporariamente a versão do seu navegador, também recomendamos que você habilite a Sincronização para todos os usuários da sua organização. Se você não ativar a Sincronização, há um risco de perda permanente dos dados de navegação. Para obter mais informações sobre a Sincronização, consulte [Sincronização do Microsoft Edge](microsoft-edge-enterprise-sync.md).

> [!CAUTION]
> Use apenas a reversão quando for necessário, pois sempre há o risco de perda de dados.

## Habilitar a reversão manualmente com um MSI

Usar as etapas a seguir para fazer a reversão manualmente usando um MSI.

1. Desabilitar as atualizações do Microsoft Edge.

   > [!NOTE]
   > Recomendamos que você instale os Modelos administrativos mais recentes. Para obter mais informações, consulte [Download e instalação do modelo administrativo do Microsoft Edge](https://docs.microsoft.com/DeployEdge/configure-microsoft-edge#1-download-and-install-the-microsoft-edge-administrative-template).

   - Abra o Editor de política de grupo local e acesse *Configuração do computador>Atualização do Microsoft Edge>Aplicativos>Microsoft Edge>*.
   - Selecione **Atualizar a substituição da política** e depois selecione **Ativado**.
   - Em **Opções**, clique em **Atualização desabilitada** na Lista suspensa de políticas.

2. Obtenha o MSI.

   - Baixe o MSI da versão que você quer reverter [aqui](https://www.microsoft.com/edge/business/download).
   - Salve o MSI na sua área de trabalho.

3. Execute o comando de reversão.

   - Abra o aviso de comando do Windows com **Executar como administrador**.
   - Digite o seguinte comando, onde: *C:\Users\username\Desktop\test* é o caminho para o MSI baixado e FileName é o nome do arquivo. msi:<br>
 `C:\Users\username\Desktop\test>msiexec /I FileName.msi /qn ALLOWDOWNGRADE=1`<br>
     > [!NOTE]
     > Para obter mais informações sobre o msiexec, consulte [msiexec](https://docs.microsoft.com/windows-server/administration/windows-commands/msiexec).
   - Feche o Microsoft Edge e abra-o novamente para verificar se a reversão funcionou. Em **Configurações e mais** (ALT + F), acesse **Configurações** e selecione **Sobre o Microsoft Edge**.

## Habilitar a reversão com a atualização do Microsoft Edge e a Política de grupo

Use as seguintes etapas para ativar a reversão com a atualização do Microsoft Edge e a Política de grupo.

1. Abra o Editor de política de grupo local e acesse *Configuração do computador>Atualização do Microsoft Edge>Aplicativos>Microsoft Edge>*.
2. Selecione **Reversão para a versão de destino** e selecione **Habilitado**.
3. Selecione **Substituição da versão de destino** e clique na versão do navegador que você quer reverter.
4. Selecione **Atualizar a substituição da política** e depois selecione **Ativado**. Em **Opções**, escolha uma das opções a seguir na Lista suspensa de políticas (exceto para **Atualização desabilitada**):

   - Sempre permitir as atualizações
   - Apenas atualizações silenciosas automáticas

     > [!NOTE]
     > Para forçar uma atualização de política de grupo, digite `dsregcmd /status`no prompt de comando do administrador do Windows (executar como administrador).

5. Clique em **OK** para salvar as configurações da política. A reversão ocorrerá na próxima vez que a atualização do Microsoft Edge verificar se há atualizações. Se você quiser que a atualização ocorra mais cedo, você pode alterar o intervalo de pesquisa do Microsoft Edge Update ou ativar a reversão usando um MSI.

### Erros comuns da reversão

Os seguintes erros impedirão a reversão:

- A entrada é uma versão de destino sem suporte
- A entrada é uma versão de destino inexistente
- A entrada está formatada incorretamente

### Políticas de grupo recomendadas

As configurações e políticas de grupo a seguir são altamente recomendáveis para usar a reversão.

#### Políticas de grupo de sincronização

- ForceSync. Defina ForceSync como habilitado. Esta política forçará a Sincronização em todos os usuários do Azure Active Directory (Azure AD). Essa política só é eficaz para as versões 86 e posteriores do Microsoft Edge.
- O *Configurar a lista dos tipos que são excluídos da política de sincronização* permite que os administradores controlem quais dados podem ser sincronizados pelos usuários.

#### Navegador para reiniciar as Políticas de grupo

Recomendamos forçar a reinicialização dos usuários depois da reversão.

- Habilitar *Ativar Notificar um usuário de que é recomendado ou necessário reiniciar um navegador quando houver atualizações pendentes*. Em opções, selecione **Necessário**.
- Habilitar *Definir o período de tempo das notificações de atualização* e defina o tempo desejado em milissegundos.

## Instantâneo

Um instantâneo é uma versão carimbada da pasta dados do usuário. Durante uma atualização de versão, um instantâneo da versão anterior é feito e armazenado na pasta do instantâneo. Após a reversão, um instantâneo com a versão correspondida será copiado para a nova pasta de dados do usuário e excluído da pasta do instantâneo. Se uma versão correspondente ao recurso de downgrade não estiver disponível, a reversão dependerá da sincronização para preencher os dados do usuário na nova versão do Microsoft Edge.

A política de grupo [UserDataSnapshotRetentionLimit] permite definir um limite para o número de instantâneos que podem ser mantidos a qualquer momento. Por padrão, três instantâneos são mantidos. Você pode configurar essa política para manter até cinco instantâneos.

## Perguntas frequentes

### Reversão manual do MSI

#### Quais erros genéricos do MSI podem ocorrer?

1. Se a política de grupo Instalar atualização estiver desabilitada, a reversão não ocorrerá.

   - Para usar a reversão, certifique-se de que a opção Instalar está configurada como **Habilitada**. Quando essa política está desabilitada, ela impede que os canais do Microsoft Edge sejam instalados. Para obter mais informações, consulte [Instalar](https://docs.microsoft.com/deployedge/microsoft-edge-update-policies#install).

2. Se as Atualizações de esclarecimento não estiverem presentes, as instalações do Microsoft Edge serão bloqueadas, a menos que *Permitir que a experiência do navegador Microsoft Edge lado a lado* estiver habilitado.

   - Para as versões Windows 1903 e 1909: se a sua última atualização foi antes de outubro de 2019, talvez você tenha essa edição.
   - Para as versões Windows 1709, 1803 e 1809: se sua última atualização foi antes de novembro de 2019, você pode ter essa edição.<br>
Para obter mais informações, consulte [Atualizações do Windows para oferecer suporte à próxima versão do Microsoft Edge](https://docs.microsoft.com/deployedge/microsoft-edge-sysupdate-windows-updates).

#### A seguinte mensagem de erro foi exibida depois de usar o Aviso de comando e a reversão não ocorreu. Qual é o problema?

![Mensagem de status da reversão](./media/edge-learnmore-rollback/edge-rollback-cmd-flag-error.png)

*ALLOWDOWNGRADE = 1* não foi executado.

### Reversão da atualização do Microsoft Edge e da Política de grupo

#### Configurei *Reversão para a versão de destino*, habilitei *Substituir a política de atualização*, inseri a versão do navegador desejado para *Substituição da versão de destino*, mas a versão do navegador não era a que eu esperava. Qual é o problema?

Alguns erros comuns que impedem a reversão são:

- Se a Reversão para a versão de destino não for definida, a reversão não será executada.
- Há um dos seguintes problemas com a configuração de substituição da versão de destino:

  - A substituição da versão de destino está definida como uma versão de destino sem suporte.
  - A substituição da versão de destino está definida para uma versão de destino inexistente.
  - A entrada Substituição da versão de destino está formatada incorretamente.

- Se a substituição da política de atualizações estiver definida como " Atualizações desabilitadas", o Microsoft Edge Update não aceitará atualizações e a reversão não será executada.

### Configurei todas as políticas de grupo corretamente, mas a reversão não foi executada. O que aconteceu?

A atualização do Microsoft Edge ainda não executa nenhuma verificação de atualizações. Por padrão, a atualização automática verifica se há atualizações a cada 10 horas. Você pode corrigir esse problema alterando o intervalo de pesquisa do Microsoft Edge Update com a política de substituição de grupo do período de verificação da atualização automática. Para obter mais informações, consulte a política [AutoUpdateCheckPeriodMinutes](https://docs.microsoft.com/deployedge/microsoft-edge-update-policies#autoupdatecheckperiodminutes).

### Como um Administrador de TI, segui todas as etapas para reverter corretamente. Apenas uma parte do meu grupo de usuários foi revertida. Por que os outros usuários ainda não foram revertidos?

A configuração da política de grupo ainda não foi sincronizada com todos os clientes. Quando o administrador define uma política de grupo, os clientes não recebem essas configurações instantaneamente. Você pode [forçar uma atualização remota da política de grupo](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-server-2012-r2-and-2012/jj134201(v=ws.11)).


## Consulte também

- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
