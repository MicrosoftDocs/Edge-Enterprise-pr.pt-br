---
title: Configurar o modo de quiosque do Microsoft Edge
ms.author: aguta
author: aguta
manager: srugh
ms.date: 02/05/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Configurar o modo de quiosque do Microsoft Edge
ms.openlocfilehash: 3f6e75b73d8c541bae4442263a5b415aeeb15eb1
ms.sourcegitcommit: c290b0b0fa6b7d7f94dcdfdda91302da733326ec
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/06/2021
ms.locfileid: "11314614"
---
# Configurar o modo de quiosque do Microsoft Edge

Este artigo descreve como configurar as opções do modo de quiosque do Microsoft Edge que você pode realizar no piloto. Há também um roteiro de recursos que estamos planejando.

> [!NOTE]
> Este artigo se aplica ao Microsoft Edge versão 87 ou posterior.

## Visão geral

O modo de quiosque do Microsoft Edge oferece duas experiências de bloqueio do navegador, para que as organizações possam criar, gerenciar e oferecer a melhor experiência para seus clientes. As seguintes experiências de bloqueio estão disponíveis:  

- Experiência de **Sinalização Digital/Interativa**: exibe um site específico no modo de tela inteira.
- Experiência de **Navegação Pública**: executa uma versão de várias guias no Microsoft Edge.

As duas experiências estão executando uma sessão InPrivate do Microsoft Edge, que protege os dados do usuário.

## Configurar o modo de quiosque do Microsoft Edge

Um conjunto inicial de recursos de modo de quiosque já está disponível para teste com o Canal Estável do Microsoft Edge, versão 87. Você pode baixar a versão mais recente do [Microsoft Edge (Canal Estável Oficial)](https://www.microsoft.com/edge).

### Recursos com suporte no modo quiosque

A tabela a seguir lista os recursos compatíveis com o modo quiosque no Microsoft Edge e na Versão Prévia do Microsoft Edge. Usar esta tabela como um guia para a transição para o Microsoft Edge, comparando como esses recursos são suportados em ambas as versões do Microsoft Edge.

|Recurso|Sinalização Interativa/Digital|Navegação pública|Disponível com a versão do Microsoft Edge (e superior)|Disponível com Versão Prévia do Microsoft Edge|
|-|-|-|-|-|
|Navegação InPrivate.|S|S|89|S|
|Redefinir em inatividade|S|S|89|S|
|[Barra de endereços somente leitura](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#kioskaddressbareditingenabled) (política) |N|S |89|N|
|[Excluir downloads na saída](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#kioskdeletedownloadsonexit) (política)  | S|S |89|N|
|F11 bloqueado (entrar/sair de tela inteira) | S | S | 89 |S|
|F12 bloqueado (iniciar Ferramentas do Desenvolvedor) | S | S | 89 |S|
| Suporte a várias guias | N| S| 89|S|
|[Permitir suporte de URL](https://docs.microsoft.com/deployedge/microsoft-edge-policies#urlallowlist) (política)|S|S|89|N|
|[Bloquear suporte de URL](https://docs.microsoft.com/deployedge/microsoft-edge-policies#urlblocklist) (política)|S|S|89|N|
|[Mostrar botão Página Principal](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#showhomebutton) (política)|N|S|89|S|
|[Gerenciar favoritos](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#managedfavorites) (política)|N|S|89|S|
|[Habilitar impressora](https://docs.microsoft.com/deployedge/microsoft-edge-policies#printingenabled) (política)|S|S|89|S|
|[Configurar a URL da página de nova guia](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#newtabpagelocation) (política)|N|S||S|
|Botão encerrar sessão | N| S| 89|S|
|Todas as URLs internas do Microsoft Edge estão bloqueadas, exceto *edge://downloads* e *edge://print* |N|S|89|S|
| Ctrl+N bloqueado (abrir uma nova janela) | S | S | 89 |S|
| Ctrl+T bloqueado (abrir nova guia) |S | S | 89 |S|
|Configurações e mais (...) exibirá somente as opções necessárias  |S |S |89 |S|
|Restringir o lançamento de outros aplicativos do navegador|S|S|90/91|S|
|Bloqueio de configurações de impressão da IU|S|S|90/91|S|
|[Defina a página da nova guia como a página inicial ](https://docs.microsoft.com/deployedge/microsoft-edge-policies#homepageisnewtabpage) (política)|-|-|A ser definido|S|

> [!NOTE]
> À medida que o modo de quiosque evolui, mais recursos estarão disponíveis.

## Usar recursos do modo de quiosque

Os recursos do modo quiosque do Microsoft Edge podem ser chamados com as seguintes opções de linha de comando do Windows 10 para sinalização digital / interativa e navegação pública.

### Sinalização digital / interativa em modo quiosque
 
```
msedge.exe --kiosk www.contoso.com --edge-kiosk-type=fullscreen
```

### Modo quiosque Navegação pública

```
msedge.exe --kiosk www.contoso.com --edge-kiosk-type=public-browsing
```

### Opções de linha de comando adicionais

- **--no-first-run:** desabilitar a primeira experiência de executar do Microsoft Edge.

   ```
  msedge.exe --kiosk www.contoso.com --edge-kiosk-type=fullscreen --no-first-run
  ```

  ```
  msedge.exe --kiosk www.contoso.com --edge-kiosk-type=public-browsing --no-first-run
  ```

- **--kiosk-idle-timeout-minutes =**: Altere o tempo (em minutos) da última atividade do usuário antes que o modo quiosque do Microsoft Edge redefina a sessão do usuário. Substitua "valor" no próximo exemplo pelo número de minutos.

   ```
   --kiosk-idle-timeout-minutes=value
   ``` 
   Os seguintes "valores" são suportados:

     - Valores padrão (em minutos)
       - Tela inteira - 0 (desligado)
       - Navegação pública - 5 minutos
    - Valores permitidos
      - 0 - desativa o cronômetro
      - 1-1440 minutos para redefinição no timer de ociosidade


    ```
    msedge.exe --kiosk www.contoso.com --edge-kiosk-type=fullscreen --kiosk-idle-timeout-minutes=1
   ```

   ```
   msedge.exe --kiosk www.contoso.com --edge-kiosk-type=public-browsing --kiosk-idle-timeout-minutes=1
   ```

## Políticas suportadas no modo de quiosque

Use qualquer uma das políticas do Microsoft Edge listadas na tabela a seguir para aprimorar a experiência de quiosque para o tipo de quiosque do Microsoft Edge que você configurar. Para saber mais sobre essas políticas, consulte [Microsoft Edge – Referência de política do browser](https://docs.microsoft.com/deployedge/microsoft-edge-policies).

> [!NOTE]
> A configuração da política não está limitada às políticas listadas na tabela a seguir. No entanto, políticas adicionais devem ser testadas para garantir que a funcionalidade do modo quiosque não seja afetada negativamente.

|Política de grupo|Sinalização Interativa/Digital|Navegação pública em um aplicativo|
|--|--|--|
|[Impressão](https://docs.microsoft.com/deployedge/microsoft-edge-policies#printing-policies) | S|S |
|[HomePageLocation](https://docs.microsoft.com/deployedge/microsoft-edge-policies#homepagelocation) |N | S|
|[ShowHomeButton](https://docs.microsoft.com/deployedge/microsoft-edge-policies#showhomebutton) |N | S|
|[NewTabPageLocation](https://docs.microsoft.com/deployedge/microsoft-edge-policies#newtabpagelocation) |N |S |
|[FavoritesBarEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#favoritesbarenabled) |N |S |
|[URLAllowlist](https://docs.microsoft.com/deployedge/microsoft-edge-policies#urlallowlist) |S |S |
|[URLBlocklist](https://docs.microsoft.com/deployedge/microsoft-edge-policies#urlblocklist) |S | S|
|[ManagedSearchEngines](https://docs.microsoft.com/deployedge/microsoft-edge-policies#managedsearchengines) |N | S|
|[UserFeedbackAllowed](https://docs.microsoft.com/deployedge/microsoft-edge-policies#userfeedbackallowed) |N | S|
|[VerticalTabsAllowed](https://docs.microsoft.com/deployedge/microsoft-edge-policies#verticaltabsallowed) | N|S |
|[Configurações do SmartScreen](https://docs.microsoft.com/deployedge/microsoft-edge-policies#smartscreen-settings-policies) |S |S |
|[EdgeCollectionsEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#edgecollectionsenabled)|S|S|

## Microsoft Edge com acesso atribuído

### Quiosque de aplicativo único

No momento, o Microsoft Edge tem suporte para um subconjunto de tipos de modo quiosque da Versão Prévia do Microsoft Edge para acesso atribuído a um aplicativo único com as seguintes experiências de bloqueio: com a Navegação Digital/Interativa e Pública.  

O modo quiosque do Microsoft Edge com aplicativo único de acesso atribuído está disponível atualmente para teste com o  [Windows 10 Insider Preview Build ](https://insider.windows.com/), versão 20215 ou superior, e com o [Microsoft Edge Beta Channel](https://www.microsoftedgeinsider.com/download), versão 89 ou superior.

**Como faço para obter a visualização do Windows Insiders?**

Para instalar uma versão do Windows 10 Insider Preview Build em um computador, siga as instruções em  [Introdução às Compilações do Windows 10 Insider Preview](https://docs.microsoft.com/windows-insider/get-started).

### Quiosque de vários aplicativos

O Microsoft Edge pode ser executado com [acesso atribuído a vários aplicativos](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps) no Windows 10, que é o equivalente ao tipo de modo de quiosque "Navegação Normal" da Versão Herdada do Microsoft Edge. Para configurar o Microsoft Edge com acesso atribuído a vários aplicativos, siga as instruções sobre como [Configurar um quiosque para vários aplicativos](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps). (O AUMID para o canal Estável do Microsoft Edge é **MSEdge**).

Ao usar o Microsoft Edge com acesso atribuído a vários aplicativos, você poderá usar as [políticas de navegador do Microsoft Edge](https://review.docs.microsoft.com/DeployEdge/microsoft-edge-policies) para configurar a experiência de navegação para atender aos seus requisitos exclusivos.

### Configurar usando as configurações do Windows

As Configurações do Windows é a maneira mais simples de configurar um ou mais dispositivos em modo de quiosque de aplicativo único. Use as etapas a seguir para configurar um computador em modo de quiosque de aplicativo único.

1. Instale a versão do Windows 10 Insider Preview mais recente, versão 20215 ou superior. Siga as instruções em [Introdução às Compilações de Visualização do Windows 10 Insider](https://docs.microsoft.com/windows-insider/get-started).
2. Para testar os recursos mais recentes, você pode baixar o [canal Microsoft Edge Beta ](https://www.microsoftedgeinsider.com/download)mais recente, versão 89 ou superior.
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

13. Saia do dispositivo de modo de quiosque e entre com a conta de modo de quiosque local para validar a configuração.

## Limitações funcionais

Com o lançamento desta versão de visualização do modo de quiosque, continuamos a melhorar o produto e adicionar novos recursos.

Recomendamos que você desligue:

- [InPrivateModeAvailability](https://docs.microsoft.com/deployedge/microsoft-edge-policies#inprivatemodeavailability)
- [IsolateOrigins](https://docs.microsoft.com/deployedge/microsoft-edge-policies#isolateorigins)
- [ManagedFavorites](https://docs.microsoft.com/deployedge/microsoft-edge-policies#managedfavorites)
- [EdgeShoppingAssistantEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#edgeshoppingassistantenabled)
- [EdgeCollectionsEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#edgecollectionsenabled)
- [UserFeedbackAllowed](https://docs.microsoft.com/deployedge/microsoft-edge-policies#userfeedbackallowed)
- [DefaultPopupsSetting](https://docs.microsoft.com/deployedge/microsoft-edge-policies#defaultpopupssetting)
- [StartupBoostEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#startupboostenabled)
- [InternetExplorerIntegrationLevel](https://docs.microsoft.com/deployedge/microsoft-edge-policies#internetexplorerintegrationlevel)
- [Extensões](https://docs.microsoft.com/deployedge/microsoft-edge-policies#extensions-policies)
- [BackgroundModeEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#backgroundmodeenabled)

## Roteiro

### No início de 2021

Incluiremos os seguintes recursos e suporte:

- Disponibilidade geral do modo de quiosque do Microsoft Edge com acesso atribuído a um único aplicativo no Windows 10 1909 ou superior.
- Recursos adicionais para a paridade com a Versão Prévia do Microsoft Edge.
- Integração com o Intune para configurar os dispositivos usando o Profile UX do modo de quiosque.
- Restrinja o lançamento de outros aplicativos do navegador.
- Bloqueio das configurações de impressão da interface do usuário.

## Veja também

- [Página de destino do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Planejar sua implantação do Microsoft Edge](deploy-edge-plan-deployment.md)
- [Configurar quiosques e sinalizações digitais em edições do Windows desktop](https://docs.microsoft.com/windows/configuration/kiosk-methods)
- [Planejar a transição do modo de quiosque](microsoft-edge-kiosk-mode-transition-plan.md)
