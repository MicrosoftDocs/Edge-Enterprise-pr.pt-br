---
title: Automatizar a implantação do Microsoft Edge para macOS com Jamf
ms.author: kvice
author: dan-wesley
manager: laurawi
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Como automatizar a implantação do Microsoft Edge para macOS com Jamf.
ms.openlocfilehash: 9c8fc0af734d4784ac122602b685bc561aabf340
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/09/2021
ms.locfileid: "11642057"
---
# <a name="deploy-to-macos-with-jamf"></a>Implantar no macOS com Jamf

Este artigo descreve como implantar o Microsoft Edge para macOS usando o Jamf.

> [!NOTE]
> Este artigo aplica-se ao Microsoft Edge versão 77 ou posterior.

## <a name="prerequisites"></a>Pré-requisitos

Antes de implantar Microsoft Edge, certifique-se de que você atenda aos seguintes pré-requisitos:

- O arquivo de instalação do Microsoft Edge,  **MicrosoftEdgeDev-\<version\>.pkg** está em um local acessível em sua rede. Você pode baixar os arquivos de instalação do Microsoft Edge Enterprise da [página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise).
- Você tem uma conta do Jamf Cloud com o nível de acesso e os privilégios necessários para criar e implantar arquivos de instalação em computadores.

## <a name="to-deploy-microsoft-edge-using-jamf"></a>Para implantar o Microsoft Edge usando Jamf:

1. Entre no Jamf e vá para **Todas as Configurações**.

    ![Abra Todas as Configurações](./media/mac-deploy/jamf-dash-main-open-settings.png)

2. Em **Todas as Configurações**, clique em **Gerenciamento do Computador**.

    ![Selecione Gerenciamento do Computador](./media/mac-deploy/jamf-all-settings-computer-mgmt.png)

3. Em **Gerenciamento do Computador**, clique em **Pacotes**.

    ![Selecione Pacotes](./media/mac-deploy/jamf-all-settings-computer-mgmt-pkgs.png)

4. Na página **Pacotes**, clique em **+ Novo** para adicionar um novo pacote.

    ![Selecione Novo para adicionar um novo pacote](./media/mac-deploy/jamf-all-settings-computer-mgmt-new-pkg.png)

5. Na página **Novo Pacote**, insira os detalhes sobre o pacote e clique em **Salvar**. (Por exemplo, NOME DE EXIBIÇÃO, INFORMAÇÕES ou OBSERVAÇÕES.)

    ![Selecione Salvar para salvar as informações do pacote](./media/mac-deploy/jamf-all-settings-computer-mgmt-save-pkg-info.png)

6. Selecione **Computadores** na barra de menus e, em seguida, selecione **Políticas** na barra de navegação.

7. Selecione **+ Novo** para exibir o painel **Nova Política**.

    ![Selecione Novo para criar uma nova política](./media/mac-deploy/jamf-all-settings-computer-new-policy.png)

8. Na guia **Opções**, selecione **Geral**.

    - Em **NOME DE EXIBIÇÃO**, insira o nome de exibição da política.
    - Em **Gatilho**, selecione o evento que vai disparar a política. (No exemplo a seguir, o evento é Inicialização.)

    ![Insira informações sobre a implantação](./media/mac-deploy/jamf-all-settings-computer-cfg-policy.png)

9. Na guia **Opções**, clique em **Pacotes**.

10. No pop-up **Configurar Pacotes**, clique em **Configurar**.

    ![Configure o pacote](./media/mac-deploy/jamf-all-settings-computer-policy-pkg-configure.png)

11. O pacote que você adicionou é mostrado no painel **Pacotes**. Clique em **Adicionar**. Neste exemplo, o pacote é "MicrosoftEdgeBeta" na captura de tela a seguir.

    ![Adicione o pacote](./media/mac-deploy/jamf-all-settings-computer-policy-pkg-add-beta.png)

12. Na página **Nova Política**, use as listas suspensas para selecionar **PONTO DE DISTRIBUIÇÃO** e **AÇÃO** a ser tomada para a política. Clique em **Salvar**. A captura de tela a seguir usa "Ponto de distribuição padrão de cada computador" e "Instalar" como exemplo.

    ![Selecione ponto de distribuição e ação](./media/mac-deploy/jamf-all-settings-computer-mgmt-pkg-cfg-distro.png)

13. Na página **Nova Política**, selecione a guia **Escopo**. Você pode gerenciar o escopo da implantação com base em computadores ou usuários. Neste exemplo, selecione **Todos os Computadores** na lista suspensa **COMPUTADORES DE DESTINO** e clique em **Salvar**.

    ![Selecione o escopo da implantação](./media/mac-deploy/jamf-all-settings-computer-mgmt-add-target.png)

14. Neste ponto, você pode revisar a política de implantação do Microsoft Edge. Se as opções de implantação atenderem aos seus requisitos, clique em **Concluído**.

    ![Clique em concluído](./media/mac-deploy/jamf-all-settings-computer-mgmt-finish-add-deployment.png)

    > [!NOTE]
    > Você pode retornar a uma política de implantação a qualquer momento para alterar as configurações.

Parabéns! Você acabou de configurar o Jamf para implantar o Microsoft Edge para macOS. Quando a condição de gatilho que você definiu for verdadeira, o pacote será implantado nos computadores especificados.

## <a name="see-also"></a>Consulte também

- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Jamf.com](https://www.jamf.com/)
- [Integrar o Jamf ao Microsoft Intune](/intune/conditional-access-integrate-jamf)