---
title: Configurar o Microsoft Edge no macOS com Jamf
ms.author: brianalt
author: dan-wesley
manager: laurawi
ms.date: 02/20/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Definir as configurações de política do Microsoft Edge em dispositivos Mac com o Jamf
ms.openlocfilehash: 336bdfed2c53811615b0183dc5ca7db916cd7428
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10978978"
---
# Definir as configurações de política do Microsoft Edge no macOS com o Jamf

Este artigo descreve como definir as configurações de política no macOS usando um arquivo de manifesto de política do Microsoft Edge no JAMF Pro 10,19.

Você também pode definir as configurações de política do Microsoft Edge no macOS usando um arquivo de lista de propriedades (.plist). Para saber mais, confira [Configurar para macOS usando um .plist](configure-microsoft-edge-on-mac.md)


## Pré-requisitos

É necessário o seguinte software:

- Canal Estável 81 do Microsoft Edge
- Arquivo de Modelos de Política, versão 81.0.416.3
- Jamf Pro, Versão 10,19

## Sobre o aplicativo Jamf Pro e menu de Configurações Personalizadas

Antes do Jamf Pro 10.18, o gerenciamento do Office 365 envolvia a criação manual de um arquivo .plist. Esse era um fluxo de trabalho demorado que exigia uma forte experiência técnica. Jamf Pro 10,18 eliminou essas barreiras simplificando o processo de configuração. No entanto, os Administradores de TI só poderiam usar essa nova interface de usuário para os aplicativos específicos e domínios de preferência especificados pelo Jamf.

No Jamf Pro 10.19, um usuário pode fazer upload de um manifesto JSON como um "esquema personalizado" para direcionar qualquer domínio de preferência e a interface gráfica do usuário será gerada a partir desse manifesto. O esquema personalizado que é criado acompanha a especificação de esquema JSON.

Para saber mais, confira [Perfis de Configuração do Computador](https://jamf.it/computer-configuration-profiles) no Guia do Administrador do Jamf Pro.

## Obter o manifesto da política para uma versão específica do Microsoft Edge

Para obter o manifesto de política:

- Vá para a [página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise).
- Na lista suspensa de canal/versão, selecione **qualquer canal com a versão 81 ou posterior.***.
- Na lista suspensa Build, selecione qualquer Build **81 ou posterior.***.
- Clique em OBTER ARQUIVOS DE POLÍTICA para baixar nosso pacote de modelos de política.

  > [!NOTE]
  > Atualmente, o pacote de modelos de política é assinado como um arquivo Cab. Você precisará usar uma ferramenta de terceiros, como The Unarchiver, para abrir o arquivo no macOS.

Depois de descompactar o arquivo CAB, descompacte o arquivo ZIP e navegue até o diretório de nível superior "mac". O manifesto, chamado de "policy_manifest.json", está neste diretório.

Esse manifesto será publicado em todos os pacotes de política, começando com o build 81.0.416.3. Se você deseja testar políticas no canal Dev, você pode pegar o manifesto associado a cada lançamento do Dev e testá-lo no Jamf Pro.  

## Usar o manifesto de política no Jamf Pro

Use as etapas a seguir para carregar o manifesto de política para o Jamf Pro e, em seguida, crie um perfil de política para o macOS.

1. Entre no Jamf.
2. Selecione a guia **Computador**.
3. Em **Gerenciamento de Conteúdo**, selecione **Perfis de Configuração**.
4. Na página **Perfis de Configuração**, clique em **+ Novo**.

   ![Adicionar um novo perfil no Jamf](media/configure-microsoft-edge-on-mac-jamf/configure-macos-jamf-configuration-profiles.png)

5. Em **Novo Perfil de Configuração do macOS**>**Opções**, selecione **Aplicativo e Configurações Personalizadas**.
6. Na janela pop-up **Aplicativo e Configurações Personalizadas**, clique em **Configurar**.

   ![Definir Aplicativos e Configurações Personalizadas](media/configure-microsoft-edge-on-mac-jamf/configure-macos-jamf-app-and-custom.png)

7. Na seção **Aplicativo e Configurações Personalizadas**, defina os valores mostrados na captura de tela a seguir.

   ![Origem do perfil e esquema personalizado](media/configure-microsoft-edge-on-mac-jamf/configure-macos-jamf-app-and-custom-schema.png)

   - Para **Método de Criação**, escolha **Definir configurações**.
   - Para **Fonte**, escolha **Esquema Personalizado**.
   - Para **Domínio de Preferência**, forneça o nome do seu domínio. Este exemplo usa *com.microsoft.Edge* como o domínio.
   - Para **Esquema Personalizado**, cole o conteúdo do arquivo de manifesto "policy_manifest.json".
   - Clique em **Salvar**.

8. Depois de salvar o perfil, Jamf exibe a seção **Geral** mostrada na próxima captura de tela.

   ![Seção Configurar Geral](media/configure-microsoft-edge-on-mac-jamf/configure-macos-jamf-app-and-custom-general-setting.png)

   - Forneça um **Nome** de exibição para o perfil e uma **Descrição**.
   - Mantenha a configuração padrão para **Categoria**, que é **Nenhuma**.
   - Para o **Método de Distribuição**, as opções são **Instalar Automaticamente** ou **Disponibilizar no Autoatendiment**o.
   - Para **Nível**, as opções são **Nível do Usuário** ou **Nível do Computador**.
   - Clique em **Salvar**.

9. Depois de salvar a seção Geral, Jamf mostra o perfil de configuração "Microsoft Edge Beta Channel" configurado para o nosso exemplo. Na próxima captura de tela, observe que você pode continuar trabalhando no perfil clicando em **Editar** ou, se tiver terminado, clique em **Concluído**.

   ![Novo perfil de configuração com opções](media/configure-microsoft-edge-on-mac-jamf/configure-macos-jamf-configuration-profiles-beta-channel.png)

   > [!NOTE]
   > Você pode editar esse perfil depois que ele for salvo e em outra sessão do Jamf. Por exemplo, você pode decidir alterar o Método de Distribuição para Disponibilizar no Autoatendimento.

   Para fazer uma edição de acompanhamento no Canal Estável do Microsoft Edge, ou excluí-lo, selecione o nome do perfil, mostrado na captura de tela Perfis de Configuração a seguir.

   ![Lista de Perfis de Configuração](media/configure-microsoft-edge-on-mac-jamf/configure-macos-jamf-configuration-profiles-beta-channel-done.png)

Depois de criar o novo perfil de configuração, você ainda terá que configurar o **Escopo** para o perfil.

### Para configurar o escopo

1. Para **Destinos**, forneça as seguintes configurações mínimas:

   - COMPUTADORES DE DESTINO. As opções são Computadores Específicos ou Todos os Computadores.
   - USUÁRIOS DE DESTINO. As opções são Usuários Específicos ou Todos os Usuários.
   - Clique em **Salvar**.
2. Para **Limitações**, mantenha a configuração padrão: Nenhuma. Clique em **Cancelar**.
3. Para **Exclusões**, mantenha a configuração padrão: Nenhuma. Clique em **Cancelar**.

## Perguntas frequentes

### O Microsoft Edge pode ser configurado para usar as preferências mestres?

Sim, você pode configurar o Microsoft Edge para usar um arquivo de preferências mestre.

Um arquivo de preferências mestre permite definir as configurações padrão para um perfil de usuário do navegador quando o Microsoft Edge for implantado. Você também pode usar um arquivo de preferências mestre para aplicar configurações em computadores que não são gerenciados por um sistema de gerenciamento de dispositivo. Essas configurações são aplicadas ao perfil do usuário na primeira vez que o usuário executa o navegador. Depois que o usuário executar o navegador, as alterações feitas no arquivo de preferências mestre não serão aplicadas. Um usuário pode alterar as configurações das preferências do mestre no navegador. Se quiser fazer uma configuração obrigatória ou alterar uma configuração após a primeira execução do navegador, você deverá usar uma política.

Um arquivo de preferências mestre permite que você personalize muitas configurações e preferências diferentes para o navegador, incluindo aquelas compartilhadas com outros navegadores baseados em Chromium e específicas do Microsoft Edge.  As preferências relacionadas à política podem ser configuradas usando o arquivo de preferências mestre. Nos casos em que uma política é definida e há um conjunto de preferências do mestre correspondente, a configuração de política terá precedência.

> [!IMPORTANT]
> Todas as preferências disponíveis podem não ser consistentes com a terminologia e as convenções de nomenclatura do Microsoft Edge.  Não há garantia de que essas preferências continuarão funcionando como esperado em versões futuras. As preferências podem ser alteradas ou ignoradas em versões posteriores.

Um arquivo de preferências mestre é um arquivo de texto formatado usando a marcação JSON. Esse arquivo precisa ser adicionado ao mesmo diretório do que o executável msedge.exe. Para implantações corporativas em todo o sistema no macOS,isso geralmente é: “*~/Library/Application Support/Microsoft/Microsoft Edge Master Preferences*" ou "*/Library/Microsoft/Microsoft Edge Master Preferences*”.

## Consulte também

- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Configurar para macOS com Intune](configure-microsoft-edge-on-mac.md)
- [Configurar para o Windows](configure-microsoft-edge.md)
- [Configurar para o Windows com o Intune](configure-edge-with-intune.md)
