---
title: Implantar o Microsoft Edge usando o System Center Configuration Manager
ms.author: kvice
author: kelleyvice-msft
manager: laurawi
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Saiba como implantar Microsoft Edge com o SCCM (System Center Configuration Manager).
ms.openlocfilehash: b0efa986c7f230f455d052f8e003616e081e324a
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/09/2021
ms.locfileid: "11641577"
---
# <a name="deploy-microsoft-edge-using-system-center-configuration-manager"></a>Implantar o Microsoft Edge usando o System Center Configuration Manager

Este artigo mostra como automatizar uma implantação do Microsoft Edge usando o SCCM (System Center Configuration Manager).

>[!NOTE]
>Este artigo aplica-se ao Microsoft Edge versão 77 ou posterior.

## <a name="before-you-begin"></a>Antes de começar

Revise as informações em [Introdução ao gerenciamento de aplicativos no Configuration Manager](/sccm/apps/understand/introduction-to-application-management). Este artigo de gerenciamento de aplicativos ajudará você a entender a terminologia usada neste artigo e é um guia para preparar seu site para instalar aplicativos.

Baixe os arquivos de instalação do Microsoft Edge (**MicrosoftEdgeDevEnterpriseX64.msi** e/ou **MicrosoftEdgeDevEnterpriseX86.msi**) da [página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise).

Armazene os arquivos de instalação do Microsoft Edge em um local de rede acessível.

## <a name="create-the-application"></a>Criar o aplicativo

Você criará o aplicativo usando um assistente do Configuration Manager.

### <a name="start-the-create-application-wizard-and-create-the-application"></a>Iniciar o assistente para Criar Aplicativo e criar o aplicativo  

1. No console do Configuration Manager, clique em **Biblioteca de Software** > **Gerenciamento de Aplicativos** > **Aplicativos**.  

2. Na guia **Início**, no grupo **Criar**, clique em **Criar Aplicativo**. Ou clique com o botão direito do mouse em **Aplicativos** na barra de navegação e clique em **Criar Aplicativo**.

    ![Criar aplicativo](./media/edge-ent-deployment-sccm/edge-ent-create-app-1.png)

3. Na página **Geral** do **Assistente para Criar Aplicativo**, escolha **Detectar automaticamente informações sobre este aplicativo em arquivos de instalação**. Isso preenche algumas das informações do assistente com informações extraídas do arquivo .msi de instalação. Forneça as seguintes informações:  

   - **Tipo**: escolha **Windows Installer (arquivo \*.msi)**.  

   - **Local**: digite o local (ou clique em **Navegar** para selecionar o local) do arquivo de instalação **MicrosoftEdgeDevEnterpriseX64.msi** ou **MicrosoftEdgeDevEnterpriseX86.msi**. Observe que o local deve ser especificado no formato *\\\Servidor\Compartilhamento\Arquivo* para que o Configuration Manager localize os arquivos de instalação.  

   A página **Especificar configurações para este aplicativo** será semelhante ao seguinte exemplo:  

    ![Especificar configurações para este aplicativo](./media/edge-ent-deployment-sccm/edge-ent-create-app-2.png)

4. Clique em **Avançar**. Em **Detalhes** na página **Informações Importadas**, você verá informações sobre o aplicativo e todos os arquivos associados que foram importados. Clique em **Avançar** para continuar com o assistente.  

    ![Exibir informações importadas](./media/edge-ent-deployment-sccm/edge-ent-create-app-3.png)

5. Na página **Informações Gerais**, você pode adicionar mais informações sobre o aplicativo. Por exemplo, Versão do software, Comentários do administrador e Editor. Você pode usar essas informações para ajudar a classificar e localizar o aplicativo no console do Configuration Manager.

   Você também pode usar o campo **Programa de instalação** para especificar a linha de comando completa que será usada para instalar o aplicativo em computadores. Você pode editar isso para adicionar suas próprias propriedades (por exemplo, **/q** para uma instalação autônoma).

   A captura de tela a seguir mostra um exemplo em que os campos **Especificar informações sobre este aplicativo** são usados.

   ![Especificar metadados do aplicativo](./media/edge-ent-deployment-sccm/edge-ent-create-app-5.png)

6. Clique em **Avançar**.
7. Na página **Resumo**, você pode confirmar as configurações do aplicativo em **Detalhes** e terminar de usar o assistente. Clique em **Avançar**.  

    ![Detalhes de configurações do aplicativo](./media/edge-ent-deployment-sccm/edge-ent-create-app-6.png)

8. Na página **Conclusão**, clique em **Fechar**.

    ![Caixa de diálogo Êxito](./media/edge-ent-deployment-sccm/edge-ent-create-app-7.png)

Você terminou a criação do aplicativo. Use as etapas abaixo para vê-la no Configuration Manager:

- selecione o espaço de trabalho **Biblioteca de Software**
- expanda **Gerenciamento de Aplicativos**
- clique em **Aplicativos**.

A captura de tela a seguir mostra o exemplo usado neste artigo.  

![Aplicativos](./media/edge-ent-deployment-sccm/edge-ent-create-app-8.png)

## <a name="change-application-properties-and-deployment-settings"></a>Alterar as propriedades e as configurações de implantação do aplicativo

Depois de criar um aplicativo, você poderá refinar as configurações do aplicativo, se necessário. Para ver as propriedades do aplicativo:

- selecione o aplicativo
- em **Início**>**Propriedades**, clique em **Propriedades**.  

   ![Configurar as propriedades do aplicativo](./media/edge-ent-deployment-sccm/edge-ent-create-app-req-1.png)

 Na página de diálogo **Propriedades do Aplicativo <nome do aplicativo\>**, você verá uma exibição com guias dos itens que pode configurar para alterar o comportamento do aplicativo. Para obter mais informações sobre as configurações que você pode definir, consulte [Criar aplicativos](/sccm/apps/deploy-use/create-applications).

Neste exemplo, você mudará algumas propriedades do tipo de implantação do aplicativo. Para alterar as propriedades da implantação:

1. Clique na guia **Tipos de Implantação**.
2. Em **Tipos de implantação:**, selecione o aplicativo **Nome**
3. Clique em **Editar**.

   ![Editar o tipo de implantação](./media/edge-ent-deployment-sccm/edge-ent-create-app-req-2.png)

### <a name="add-a-requirement-to-the-deployment-type"></a>Adicionar um requisito ao tipo de implantação

 Os requisitos especificam as condições que devem ser atendidas antes que um aplicativo seja instalado em um dispositivo. Você pode escolher entre os requisitos internos ou pode criar os seus próprios. Por exemplo, você pode adicionar um requisito de que o aplicativo só será instalado em computadores que estejam executando o Windows 10 **x86** ou **x64**, dependendo da arquitetura do processador de destino do arquivo de instalação. Neste exemplo, você especificará o Windows 10 **x86**.

1. Na página de propriedades do tipo de implantação que você acabou de abrir, clique na guia **Requisitos**.

2. Clique em **Adicionar** para abrir o diálogo **Criar Requisito**.

    ![Criar requisito](./media/edge-ent-deployment-sccm/edge-ent-create-app-req-3.png)

3. Na caixa de diálogo **Criar Requisito**, especifique as seguintes informações:

    - **Categoria**: **Dispositivo**  

    - **Condição**: **Sistema operacional**  

    - **Tipo de regra**: **valor**  

    - **Operador**: **um de**  

    - Na lista dos sistemas operacionais, selecione **Windows 10** > **Todos os Windows 10 (32 bits)**.  

    Quando você terminar, o diálogo será semelhante ao seguinte exemplo de captura de tela:

    ![Adicionar requisito](./media/edge-ent-deployment-sccm/edge-ent-create-app-req-4.png)

4. Clique em **OK** para fechar cada página de propriedades aberta e retorne à lista **Aplicativos** no console do Configuration Manager.  

## <a name="add-the-application-content-to-a-distribution-point"></a>Adicionar o conteúdo do aplicativo a um ponto de distribuição  

Para implantar o aplicativo atualizado em computadores, certifique-se de que o conteúdo do aplicativo seja copiado para um ponto de distribuição. Os computadores acessam o ponto de distribuição para instalar o aplicativo.  

>[!TIP]
>Para saber mais sobre pontos de distribuição e gerenciamento de conteúdo no Configuration Manager, consulte [Implantar e gerenciar conteúdo para o System Center Configuration Manager](/sccm/core/servers/deploy/configure/deploy-and-manage-content).  

1. No console do Configuration Manager, clique em **Biblioteca de Software**.  

2. No espaço de trabalho **Biblioteca de Software**, expanda **Aplicativos**. Selecione o aplicativo que você criou na lista de aplicativos.

3. Na guia **Início**, no grupo **Implantação**, clique em **Distribuir Conteúdo**.  

4. Na página **Geral** do **Assistente para Distribuir Conteúdo**, verifique se o nome do aplicativo está correto e clique em **Avançar**.  

5. Na página **Conteúdo**, revise as informações que serão copiadas para o ponto de distribuição e clique em **Avançar**.  

6. Na página **Destino de Conteúdo**, clique em **Adicionar** para selecionar uma ou mais coleções, pontos de distribuição ou grupos de pontos de distribuição nos quais será instalado o conteúdo do aplicativo.

7. Conclua o assistente.

Você pode verificar se o conteúdo do aplicativo foi copiado com êxito para o ponto de distribuição do espaço de trabalho **Monitoramento**, em **Status de Distribuição** > **Status do Conteúdo**.  

## <a name="deploy-the-application"></a>Implantar o aplicativo  

Em seguida, implante o aplicativo em uma coleção de dispositivos em sua hierarquia. Neste exemplo, você implanta o aplicativo na coleção de dispositivos **Todos os Sistemas**.  

>[!TIP]
>Lembre-se de que somente os computadores Windows 10 da arquitetura de processador especificada instalarão o aplicativo por causa dos requisitos que você selecionou antes.  

1. No console do Configuration Manager, clique em **Biblioteca de Software** > **Gerenciamento de Aplicativos** > **Aplicativos**.

2. Na lista de aplicativos, selecione o aplicativo que você criou anteriormente. Em seguida, na guia **Início** do grupo **Implantação**, clique em **Implantar** ou clique com o botão direito do mouse no aplicativo e selecione **Implantar**.

    ![Implantar o aplicativo](./media/edge-ent-deployment-sccm/edge-ent-deploy-app-1.png)

3. Na página **Geral** do **Assistente para Implantar Software**, clique em **Procurar** para selecionar a coleção de dispositivos para a qual você deseja implantar o aplicativo.

    ![Procurar o arquivo de instalação](./media/edge-ent-deployment-sccm/edge-ent-deploy-app-2.png)

4. Na página **Conteúdo**, verifique se o ponto de distribuição do qual deseja instalar o aplicativo está selecionado.

    ![Especificar ponto de distribuição](./media/edge-ent-deployment-sccm/edge-ent-deploy-app-6.png)

5. Na página **Configurações de Implantação**, verifique se a ação de implantação está definida como **Instalar**, e a finalidade da implantação é definida como **Obrigatória**.

    ![Definir configurações de implantação](./media/edge-ent-deployment-sccm/edge-ent-deploy-app-8.png)

    >[!TIP]
    >Ao definir a finalidade da implantação como **Obrigatória**, você deve verificar se o aplicativo está instalado em computadores que atendam aos requisitos definidos. Se você definir esse valor como **Disponível**, os usuários poderão instalar o aplicativo sob demanda do Centro de Software.  

6. Na página **Agendamento**, você pode configurar quando o aplicativo será instalado. Neste exemplo, selecione **O mais rápido possível após o horário disponível**.

    ![Agendar a implantação](./media/edge-ent-deployment-sccm/edge-ent-deploy-app-9.png)

7. Na página **Experiência do Usuário**, selecione os valores desejados e clique em **Avançar**.

    ![Especificar experiência do usuário](./media/edge-ent-deployment-sccm/edge-ent-deploy-app-10.png)

8. Especifique as opções de alerta desejadas e clique em **Avançar**.

    ![Especificar configurações de alerta](./media/edge-ent-deployment-sccm/edge-ent-deploy-app-11.png)

9. Conclua o assistente.

Use as informações na seção **Monitorar o aplicativo** a seguir para ver o status da implantação do seu aplicativo.  

## <a name="monitor-the-application"></a>Monitorar o aplicativo

 Nesta seção, você examinará rapidamente o status de implantação do aplicativo que acabou de implantar.  

### <a name="to-review-the-deployment-status"></a>Para revisar o status da implantação  

1. No console do Configuration Manager, clique em **Monitoramento** > **Implantações**.  

2. Na lista de implantações, selecione o aplicativo.

    ![Monitorar a implantação](./media/edge-ent-deployment-sccm/edge-ent-monitor-deployment.png)

3. Na guia **Início**, no grupo **Implantação**, clique em **Exibir Status**.  

4. Selecione uma das seguintes guias para ver mais atualizações de status sobre a implantação do aplicativo:  

    - **Êxito**: o aplicativo foi instalado com êxito nos computadores indicados.  

    - **Em Andamento**: a instalação do aplicativo ainda não terminou.  

    - **Erro**: ocorreu um erro ao instalar o aplicativo nos computadores indicados. Mais informações sobre o erro também são exibidas.  

    - **Requisitos não atendidos**: nenhuma tentativa de instalação foi feita nos dispositivos indicados porque eles não atenderam aos requisitos que você configurou (neste exemplo, porque eles não são executados no Windows 10).

    - **Desconhecido**: o Configuration Manager não pôde relatar o status da implantação. Verifique novamente mais tarde.  

    >[!TIP]
    >Há várias maneiras de monitorar implantações de aplicativos. Para obter mais informações, consulte [Monitorar aplicativos do console do System Center Configuration Manager](/sccm/apps/deploy-use/monitor-applications-from-the-console).  

## <a name="end-user-experience"></a>Experiência do usuário final  

Os usuários com computadores gerenciados pelo Configuration Manager e que executam o Windows 10 da arquitetura de processador especificada verão uma mensagem informando que devem instalar o aplicativo Microsoft Edge Dev. Ao aceitar essa opção de instalação, o aplicativo será instalado.  

## <a name="see-also"></a>Consulte também

- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Criar e implantar um aplicativo com o System Center Configuration Manager](/sccm/apps/get-started/create-and-deploy-an-application)