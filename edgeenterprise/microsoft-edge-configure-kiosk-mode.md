---
title: Configurar o modo de quiosque do Microsoft Edge
ms.author: aguta
author: aguta
manager: srugh
ms.date: 09/22/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Configurar o modo de quiosque do Microsoft Edge
ms.openlocfilehash: d7c9df82079f8343d43ccfd312623e6e01358fa9
ms.sourcegitcommit: 858227653fc89532d1d274735f53280e27b2a8c0
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/22/2020
ms.locfileid: "11072638"
---
# Configurar o modo de quiosque do Microsoft Edge

Este artigo descreve como configurar as opções do modo de quiosque do Microsoft Edge que você pode realizar no piloto. Há também um roteiro de recursos que temos como alvo.

> [!NOTE]
> Este artigo se aplica ao Microsoft Edge versão 87 ou posterior.

Para obter informações sobre o modo de quiosque da Versão Herdada do Microsoft Edge (versão 45 e anteriores), consulte [Implantar o modo de quiosque do Microsoft Edge](https://aka.ms/edgekioskmode).

## Visão geral

O modo de quiosque do Microsoft Edge oferece duas experiências de bloqueio do navegador, para que as organizações possam criar, gerenciar e oferecer a melhor experiência para seus clientes. As seguintes experiências de bloqueio estão disponíveis:  

- A experiência de sinalização digital/interativa exibe um site específico no modo de tela inteira.
- A experiência de navegação pública executa uma versão de várias guias no Microsoft Edge.

As duas experiências estão executando uma sessão Microsoft Edge InPrivate, que protege os dados do usuário.

## Configurar o modo de quiosque do Microsoft Edge  

Um conjunto inicial de recursos de modo de quiosque já está disponível para teste com o Microsoft Edge Canary Channel, versão 87. Você pode baixar o Microsoft Edge Canary na página do [Microsoft Edge Insider Channels](https://www.microsoftedgeinsider.com/download).

### Recursos do modo de quiosque

Os seguintes recursos estão disponíveis:

- Navegação InPrivate. Protege os dados do usuário excluindo os dados e os downloads do navegador quando a sessão termina.
- Política para configurar Excluir downloads ao sair.
- Redefinir a sessão de usuário após um determinado período de inatividade.
- Conjunto inicial de funcionalidade de bloqueio. As funções a seguir estão disponíveis:

  - Menu de contexto do mouse
  - F12 Ferramentas de desenvolvedor
  - F11 Sair da tela inteira (enquanto estiver no modo de tela inteira)
  - Bloqueio do conjunto inicial de páginas *Edge://*

> [!NOTE]
> À medida que o modo de quiosque evolui, mais recursos estarão disponíveis.

### Usar recursos do modo de quiosque

Você pode invocar os recursos do modo de quiosque do Microsoft Edge com as seguintes opções de linha de comando do Windows 10:

- Sinalização interativa/digital do modo de quiosque: `msedge.exe --kiosk www.contoso.com --edge-kiosk-type=fullscreen`
- Navegação pública modo de quiosque: `msedge.exe --kiosk www.contoso.com --edge-kiosk-type=public-browsing`

#### Opções de linha de comando adicionais

- `--no-first-run` : Desabilite a primeira experiência de execução do Microsoft Edge.
- `--kiosk-idle-timeout-minutes` : Altere o tempo (em minutos) da última atividade de usuário antes que o modo de quiosque do Microsoft Edge redefina a sessão do usuário. Os seguintes valores são válidos:

  - Valores padrão
    - Tela cheia - desativado
    - Navegação pública - 5 minutos
  - Valores permitidos
    - 0 - desativa o cronômetro
    - 1-1440 minutos para redefinição no timer de ociosidade

## Configurar o modo de quiosque com acesso atribuído

O modo de quiosque do Microsoft Edge com acesso atribuído está disponível atualmente para teste com a versão mais recente do [Windows 10 Insider Preview](https://insider.windows.com/), versão 20215 ou superior e com o [Microsoft Edge Dev](https://www.microsoftedgeinsider.com/download), versão 87.0.644 ou superior.

**Como faço para obter a visualização do Windows Insiders?**

Para instalar uma versão do Windows 10 Insider Preview Build em um computador, siga as instruções em [Introdução ao Windows 10 Insider Preview Builds](https://docs.microsoft.com/windows-insider/get-started).

### Configurar usando as configurações do Windows

As Configurações do Windows é a maneira mais simples de configurar um ou mais dispositivos em modo de quiosque de aplicativo único. Use as etapas a seguir para configurar um computador em modo de quiosque de aplicativo único.

1. Instale a versão do Windows 10 Insider Preview mais recente, versão 20215 ou superior. Siga as instruções em [Introdução ao Windows 10 Insider Preview Builds](https://docs.microsoft.com/windows-insider/get-started).
2. Instalar a versão mais recente do [canal Microsoft Edge Dev](https://www.microsoftedgeinsider.com/download), 87.0.644 ou superior.

   > [!IMPORTANT]
   > Como é necessária uma instalação no nível do dispositivo, só há suporte para um canal que não seja Canary.

3. No computador modo de quiosque, abra as configurações do Windows e digite "modo de quiosque" no campo de pesquisa. Selecione  **Configurar um modo de quiosque (acesso atribuído)**, mostrada na próxima captura de tela para abrir a caixa de diálogo para criar o modo de quiosque.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-1-assigned-access.png" alt-text="Configurar o modo de quiosque com acesso atribuído":::

4. Na página **Configurar um modo de quiosque** , clique em  **Introdução**.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-2-get-started.png" alt-text="Página modo de quiosque – introdução":::

5. Digite um nome para criar uma nova conta modo de quiosque ou escolha uma conta existente na lista suspensa preenchida e clique em  **Avançar**.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-3-create-account.png" alt-text="Modo de quiosque - criar conta":::

6. Na página **Escolher um aplicativo de modo de quiosque** , selecione **Microsoft Edge** e clique em  **Avançar**.

   > [!NOTE]
   > Isso se aplica apenas ao Microsoft Edge Dev, Beta e a canais estáveis.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-4-pick-app.png" alt-text="Modo de quiosque - escolha um aplicativo":::

7. Escolha uma das opções a seguir para exibir o Microsoft Edge na execução no modo de quiosque:

   - Sinalização digital/interativa - Exibe um site específico no modo de tela inteira executando o Microsoft Edge.
   - Navegador público - Executa uma versão limitada com várias guias do Microsoft Edge.

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-5a-digital-sign.png" alt-text="Exibição do modo quiosque – sinal digital de tela inteira":::

8. Selecione **Próximo**.
9. Digite a URL a ser carregada quando o quiosque for iniciado.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-6-enter-url.png" alt-text="Modo de quiosque - Inserir URL":::

10. Aceite o valor padrão de 5 minutos para o tempo ocioso ou escolha um outro valor.

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-7-enter-idle-time.png" alt-text="Modo de quiosque - Inserir tempo ocioso":::

11. Clique **Próximo**.
12. Feche a janela de  **Configurações**  para salvar e aplicar suas opções.

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode--8-done.png" alt-text="Modo de quiosque – concluir configuração":::

13. Reinicie o dispositivo de modo de quiosque e entre com a conta de modo de quiosque local para validar a configuração.

## Limitações funcionais

Com o lançamento desta versão de visualização do modo de quiosque, continuamos a melhorar o produto e adicionar novos recursos.

Embora o modo de quiosque não ofereça suporte à funcionalidade a seguir, o trabalho está em andamento nos seguintes recursos:

- Coleções
- Extensões
- Modo Internet Explorer
- Windows Defender Application Guard (WDAG)

## Mapa

### Ainda este ano (2020)

Incluiremos os seguintes recursos:

- Botão encerrar sessão
- Barra de endereços da URL somente leitura  
  - Configurável com a Política de Grupo
  - Quando habilitados, os usuários serão impedidos de editar a URL da barra de endereços para experimentar a navegação para outra página.

- Mais funções de bloqueio:

  - Aceleradores adicionais serão bloqueados (por exemplo, CTRL+N)
  - O "..." menu configurações habilitará somente as opções necessárias (por exemplo, Imprimir, Ajuda, Comentários e Ler em voz alta)
  - Bloqueio *edge://* adicional de páginas (por exemplo, *edge://settings*)
  - Configurar opções de impressão, IU
  - Limitando o explorador de arquivos apenas à pasta de download.

### No início de 2021

Incluiremos os seguintes recursos e suporte:

- Disponibilidade geral do modo de quiosque do Microsoft Edge com acesso atribuído a um único aplicativo no Windows.
- Recursos adicionais para a paridade com a Versão Prévia do Microsoft Edge.
- Integração com o Intune para configurar os dispositivos usando o Profile UX do modo de quiosque.

## Consulte também

- [Configurar quiosques e sinalizações digitais em edições do Windows desktop](https://docs.microsoft.com/windows/configuration/kiosk-methods)
- [Implantar o modo de quiosque da Versão Herdada do Microsoft Edge](https://aka.ms/edgekioskmode) 
- [Planejar sua implantação do Microsoft Edge](deploy-edge-plan-deployment.md)
- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)