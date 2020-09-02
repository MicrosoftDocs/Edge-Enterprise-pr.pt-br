---
title: Definir as configurações de política do Microsoft Edge para Windows usando o Microsoft Intune.
ms.author: kvice
author: kelleyvice-msft
manager: laurawi
ms.date: 06/18/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Definir as configurações de política do Microsoft Edge para Windows usando o Microsoft Intune.
ms.openlocfilehash: 6200b52e9061f37f85fe0bfe7cf59a2172db97df
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979008"
---
# Definir as configurações de política do Microsoft Edge com o Microsoft Intune

Este artigo explica como definir as configurações de política do Microsoft Edge para Windows 10 usando o Microsoft Intune.

> [!NOTE]
> Este artigo aplica-se ao Microsoft Edge versão 77 ou posterior.

Você pode definir políticas e configurações do Microsoft Edge adicionando um perfil de configuração de dispositivo ao Microsoft Intune. Usar o Intune para gerenciar e aplicar políticas é o mesmo que usar a Política de grupo do Active Directory ou configurar as configurações locais do Objeto da política de grupo (GPO) nos dispositivos do usuário.

Para obter mais informações sobre o gerenciamento de políticas do Microsoft Edge com o Microsoft Intune, leia [Gerenciar o acesso via Web usando o Microsoft Edge com o Microsoft Intune](https://docs.microsoft.com/intune/manage-microsoft-edge), mas lembre-se de que o artigo vinculado é específico para o Microsoft Edge versão 45 e anterior e, portanto, pode conter informações e referências que não se apliquem ao Microsoft Edge Enterprise versão 77 e posterior.

> [!TIP]
> Para obter informações sobre como configurar o Microsoft Edge no macOS usando o Microsoft Intune, consulte [Configurar para macOS](configure-microsoft-edge-on-mac.md).

## Criar um perfil para gerenciar as configurações no Microsoft Edge para Windows 10

Usando os Modelos Administrativos no Microsoft Intune, você pode gerenciar as políticas de grupo do Microsoft Edge em seus dispositivos Windows 10 usando a nuvem. Esta seção ajudará você a criar um modelo para definir as configurações de aplicativo específicas do Microsoft Edge. Quando você cria o modelo, ele cria um perfil de configuração de dispositivo. Você então poderá atribuir ou implantar esse perfil em dispositivos Windows 10 em sua organização.

### Pré-requisitos

- Windows 10 com os seguintes requisitos mínimos do sistema:
  - Windows 10, versão 1909
  - Windows 10, versão 1903 com [KB4512941](https://support.microsoft.com/kb/4512941) instalado
  - Windows 10, versão 1809 com [KB4512534](https://support.microsoft.com/kb/4512534) instalado
  - Windows 10, versão 1803 com [KB4512509](https://support.microsoft.com/kb/4512509) instalado
  - Windows 10, versão 1709 com [KB4516071](https://support.microsoft.com/kb/4516071) instalado

### Usar Modelos administrativos para criar uma política para o Microsoft Edge

Esse procedimento alavanca os Modelos Administrativos (que você pode estar familiarizado com a Política de grupo) que são incorporados no Intune. Você pode usar esses modelos para criar uma política para o Microsoft Edge, selecionando configurações de uma lista pré-configurada.

1. Entrar no portal do [Microsoft Endpoint Manager](https://endpoint.microsoft.com/).
2. Selecione **Dispositivos** no painel de navegação à esquerda.
3. Em **Dispositivos** | **Visão geral**, selecione **Perfis de configuração** (em Título da política).
4. Na barra de comandos superior, selecione **Criar perfil**.
5. Na lista suspensa abaixo **Plataforma**, selecione **Windows 10 e versão posterior**.
6. Na lista suspensa abaixo **Perfil**, selecione **Modelos administrativos** e clique no botão **Criar**. A próxima captura de tela mostra as listas suspensas para selecionar a plataforma e o tipo de perfil.

    ![Selecionar a plataforma e o tipo de perfil](./media/configure-edge-with-intune/create-profile-platform.png)

7. Na guia **Básico**, insira um **Nome**, descritivo como política do Microsoft Edge. Opcionalmente, insira uma **Descrição** para a política.
A próxima captura de tela mostra o formulário da guia **Básico** e a barra de menus mostra as próximas etapas (como guias acinzentadas) para criar o perfil.

   ![Insira Nome e Descrição](./media/configure-edge-with-intune/create-profile-basics-tab.png)

8. Selecione **Avançar**.
9. Na guia **Configurações**, selecione a pasta Microsoft Edge em um dos seguintes locais:

   - abaixo da pasta Configuração do computador
   - abaixo da pasta Configuração do usuário.

   As configurações disponíveis do Microsoft Edge serão exibidas no painel direito. Por exemplo, *Configuração do computador/Microsoft Edge/Permitir restrições de download* exibidos na captura de tela a seguir.

   ![Guia Definições de configuração](./media/configure-edge-with-intune/create-profile-configuration-settings-tab.png)

   > [!NOTE]
   > Consulte [Microsoft Edge – Políticas](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies) e [Microsoft Edge – Políticas de atualização](https://docs.microsoft.com/DeployEdge/microsoft-edge-update-policies) para a lista mais completa e atualizada de todas as configurações disponíveis do Microsoft Edge.

10. Use o campo de pesquisa ("Pesquisar para filtrar itens...") para encontrar uma configuração específica que você quer configurar. Nesse exemplo, a cadeia de caracteres de pesquisa é "página inicial". A próxima captura de tela mostra os resultados da pesquisa.

    ![Resultados de pesquisas](./media/configure-edge-with-intune/create-profile-configuration-settings-tab-search.png)

11. Depois de encontrar a configuração que quer configurar, selecione-a para expor os valores que você pode definir. Na próxima captura de tela, selecionamos "Configurar a URL da página inicial" como um exemplo.

    ![Configurar a política de URL da página inicial](./media/configure-edge-with-intune/create-profile-configuration-settings-tab-edit-pol.png)

12. Habilitar a política e inserir um valor para a URL da página inicial, como mostrado na captura de tela anterior.

13. Clique em **OK**. A coluna "Status" deve ser exibida como "Habilitada", conforme mostrado no exemplo a seguir.

    ![O status de configuração está Habilitado](./media/configure-edge-with-intune/create-profile-configuration-settings-tab-set-enabled.png)

14. Clique no botão **Avançar**.

15. Na guia **Rótulos de escopo**, adicione um rótulo de escopo se você quiser, do contrário, clique no botão **Próximo**.

16. Na guia **Atribuições**, clique em **+ Selecionar grupos para incluir** para atribuir essa política ao grupo do Azure Active Directory (Azure AD) que contiver os dispositivos ou os usuários que você quer que recebam essa configuração de política. Consulte [Atribuir perfis de usuário e dispositivo no Microsoft Intune](https://docs.microsoft.com/intune/device-profile-assign) para obter mais informações sobre como atribuir o perfil ao seu usuário ou aos seus grupos de dispositivos do Azure AD.

    ![Selecionar grupos para incluir](./media/configure-edge-with-intune/create-profile-assignments-tab.png)

17. Clique no botão **Avançar**.

18. Na guia **Revisar + criar**, examine o resumo das suas alterações para verificar se está correto e clique no botão **Criar**.

19. A política recém-criada (Política do Microsoft Edge) é exibida na captura de tela a seguir.

    ![Selecionar grupos para incluir](./media/configure-edge-with-intune/create-profile-new-policy-finished.png)

Para obter mais informações sobre perfis do Windows 10, consulte [Usar modelos do Windows 10 para definir configurações de política de grupo no Microsoft Intune](https://docs.microsoft.com/intune/administrative-templates-windows).

## Consulte também

- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Gerenciar o acesso via Web usando o Microsoft Edge com o Microsoft Intune](https://docs.microsoft.com/intune/manage-microsoft-edge)
- [Usar os modelos di Windows 10 para definir as configurações de política de grupo no Microsoft Intune](https://docs.microsoft.com/intune/administrative-templates-windows)
- [Implantar o Microsoft Edge usando o Microsoft Intune](https://docs.microsoft.com/intune/apps/apps-windows-edge/?toc=https://docs.microsoft.com/DeployEdge/toc.json&bc=https://docs.microsoft.com/DeployEdge/breadcrumb/toc.json)
