---
title: Configurar o modo de quiosque do Microsoft Edge
ms.author: v-danwesley
author: dan-wesley
manager: srugh
ms.date: 05/02/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Aprenda sobre os recursos do modo de quiosque e como configurar as opções do modo de quiosque do Microsoft Edge.
ms.openlocfilehash: 17ec165ce86155a03e5adc757ddafcad3e3c9819
ms.sourcegitcommit: 592f6e40b13e28af588473b2a75c3ae697e5db2d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/05/2022
ms.locfileid: "12505494"
---
# <a name="configure-microsoft-edge-kiosk-mode"></a>Configurar o modo de quiosque do Microsoft Edge

Este artigo descreve como configurar as opções do modo de quiosque do Microsoft Edge que você pode realizar no piloto. Há também um roteiro de recursos que estamos planejando.

> [!NOTE]
> Este artigo se aplica ao Microsoft Edge versão 87 ou posterior.

> [!IMPORTANT]
> Chame os recursos do modo quiosque do Microsoft Edge no Windows 10 usando os argumentos de linha de comando fornecidos em [Use os recursos do modo quiosque](#use-kiosk-mode-features).

## <a name="overview"></a>Visão Geral

O modo de quiosque do Microsoft Edge oferece duas experiências de bloqueio do navegador, para que as organizações possam criar, gerenciar e oferecer a melhor experiência para seus clientes. As seguintes experiências de bloqueio estão disponíveis:  

- Experiência de **Sinalização Digital/Interativa**: exibe um site específico no modo de tela inteira.
- Experiência de **Navegação Pública**: executa uma versão de várias guias no Microsoft Edge.

As duas experiências estão executando uma sessão InPrivate do Microsoft Edge, que protege os dados do usuário.

## <a name="set-up-microsoft-edge-kiosk-mode"></a>Configurar o modo de quiosque do Microsoft Edge

Um conjunto inicial de recursos de modo de quiosque já está disponível para teste com o Canal Estável do Microsoft Edge, versão 87. Você pode baixar a versão mais recente do [Microsoft Edge (Canal Estável Oficial)](https://www.microsoft.com/edge).

### <a name="kiosk-mode-supported-features"></a>Recursos com suporte no modo quiosque

A tabela a seguir lista os recursos compatíveis com o modo quiosque no Microsoft Edge e na Versão Prévia do Microsoft Edge. Usar esta tabela como um guia para a transição para o Microsoft Edge, comparando como esses recursos são suportados em ambas as versões do Microsoft Edge.

|Recurso|Sinalização Interativa/Digital|Navegação pública|Disponível com a versão do Microsoft Edge (e superior)|Disponível com Versão Prévia do Microsoft Edge|
|-|-|-|-|-|
|Navegação InPrivate.|S|S|89|S|
|Redefinir em inatividade|S|S|89|S|
|[Barra de endereços somente leitura](./microsoft-edge-policies.md#kioskaddressbareditingenabled) (política) |N|S |89|N|
|[Excluir downloads na saída](./microsoft-edge-policies.md#kioskdeletedownloadsonexit) (política)  | S|S |89|N|
|F11 bloqueado (entrar/sair de tela inteira) | S | S |89|S|
|F12 bloqueado (iniciar Ferramentas do Desenvolvedor) | S | S |89|S|
| Suporte a várias guias | N| S|89|S|
|[Permitir suporte de URL](./microsoft-edge-policies.md#urlallowlist) (política)|S|S|89|N|
|[Bloquear suporte de URL](./microsoft-edge-policies.md#urlblocklist) (política)|S|S|89|N|
|[Mostrar botão Página Principal](./microsoft-edge-policies.md#showhomebutton) (política)|N|S|89|S|
|[Gerenciar favoritos](./microsoft-edge-policies.md#managedfavorites) (política)|N|S|89|S|
|[Habilitar impressora](./microsoft-edge-policies.md#printingenabled) (política)|S|S|89|S|
|[Configurar a URL da página de nova guia](./microsoft-edge-policies.md#newtabpagelocation) (política)|N|S|89|S|
|Botão encerrar sessão * | N| S|89|S|
|Todas as URLs internas do Microsoft Edge estão bloqueadas, exceto *edge://downloads* e *edge://print* |N|S|89|S|
| Ctrl+N bloqueado (abrir uma nova janela) | S | S |89|S|
| Ctrl+T bloqueado (abrir nova guia) |S | N |89|S|
|Configurações e mais (...) exibirá somente as opções necessárias  |S |S |89|S|
|Restringir o lançamento de outros aplicativos do navegador|S|S|90|S|
|Bloqueio de configurações de impressão da IU|S|S|90|S|
|[Definir a página da nova guia como a página inicial ](./microsoft-edge-policies.md#homepageisnewtabpage) (política)|N|S|90|S|

> [!NOTE]
> Os recursos seguidos por "*" são ativados apenas em um cenário de aplicativo único de acesso atribuído.

## <a name="use-kiosk-mode-features"></a>Usar os recursos do modo de quiosque

Microsoft Edge recursos do modo de quiosque podem ser invocados com as seguintes Windows 10 de linha de comando para sinalização digital/interativa e navegação pública.

### <a name="kiosk-mode-digitalinteractive-signage"></a>Sinalização digital / interativa em modo quiosque
 
```
msedge.exe --kiosk www.contoso.com --edge-kiosk-type=fullscreen
```

### <a name="kiosk-mode-public-browsing"></a>Modo quiosque Navegação pública

```
msedge.exe --kiosk www.contoso.com --edge-kiosk-type=public-browsing
```

### <a name="kiosk-mode-download-files-on-exit"></a>Baixar arquivos no modo de quiosque ao sair

Para configurar Microsoft Edge para remover arquivos baixados quando uma instância de Quiosque é fechada, as duas Políticas de Grupo a seguir devem ser configuradas:
- [Excluir downloads ao sair](./microsoft-edge-policies.md#kioskdeletedownloadsonexit) = Habilitado
- [Definir diretório de](./microsoft-edge-policies.md#downloaddirectory) download = ${local_app_data}\Microsoft\Edge\KioskDownloads 


### <a name="additional-command-line-options"></a>Opções de linha de comando adicionais

- **--no-first-run:** desabilitar a primeira experiência de executar do Microsoft Edge.

   ```
  msedge.exe --kiosk www.contoso.com --edge-kiosk-type=fullscreen --no-first-run
  ```

  ```
  msedge.exe --kiosk www.contoso.com --edge-kiosk-type=public-browsing --no-first-run
  ```

- **--kiosk-idle-timeout-minutes=**: altere o tempo (em minutos) da última atividade do usuário antes que Microsoft Edge modo de quiosque redefina a sessão do usuário fechando o navegador. Observação: esse sinalizador não será reiniciado Microsoft Edge depois que ele for fechado. Uma tecnologia separada, como Acesso Atribuído ou Inicialização de Shell, é necessária para reiniciar automaticamente o Edge após o tempo limite de ociosidade. Substitua "valor" no próximo exemplo pelo número de minutos.

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

## <a name="support-policies-for-kiosk-mode"></a>Políticas suportadas no modo de quiosque

Use qualquer uma das políticas do Microsoft Edge listadas na tabela a seguir para aprimorar a experiência de quiosque para o tipo de quiosque do Microsoft Edge que você configurar. Para saber mais sobre essas políticas, consulte [Microsoft Edge – Referência de política do browser](./microsoft-edge-policies.md).

> [!NOTE]
> A configuração da política não está limitada às políticas listadas na tabela a seguir. No entanto, políticas adicionais devem ser testadas para garantir que a funcionalidade do modo quiosque não seja afetada negativamente.

|Política de grupo|Sinalização Interativa/Digital|Navegação pública em um aplicativo|
|--|--|--|
|[Impressão](./microsoft-edge-policies.md#printing-policies) | S|S |
|[HomePageLocation](./microsoft-edge-policies.md#homepagelocation) |N | S|
|[ShowHomeButton](./microsoft-edge-policies.md#showhomebutton) |N | S|
|[NewTabPageLocation](./microsoft-edge-policies.md#newtabpagelocation) |N |S |
|[FavoritesBarEnabled](./microsoft-edge-policies.md#favoritesbarenabled) |N |S |
|[URLAllowlist](./microsoft-edge-policies.md#urlallowlist) |S |S |
|[URLBlocklist](./microsoft-edge-policies.md#urlblocklist) |S | S|
|[ManagedSearchEngines](./microsoft-edge-policies.md#managedsearchengines) |N | S|
|[UserFeedbackAllowed](./microsoft-edge-policies.md#userfeedbackallowed) |N | S|
|[VerticalTabsAllowed](./microsoft-edge-policies.md#verticaltabsallowed) | N|S |
|[Configurações do SmartScreen](./microsoft-edge-policies.md#smartscreen-settings-policies) |S |S |
|[EdgeCollectionsEnabled](./microsoft-edge-policies.md#edgecollectionsenabled)|S|S|

## <a name="microsoft-edge-with-assigned-access"></a>Microsoft Edge com acesso atribuído

### <a name="single-app-kiosk"></a>Quiosque de aplicativo único

O Microsoft Edge modo de quiosque versão 90 oferece uma extensa lista de recursos. Consulte a seção dos recursos com suporte do modo de quiosque.
Com as atualizações Windows a seguir, você pode configurar Microsoft Edge aplicativo único de acesso atribuído.

|Sistema operacional|Versão|Atualizações|
|--|--|--|
|Windows 10 | 2004 ou posterior|[KB4601382 ou posterior](https://support.microsoft.com/topic/february-24-2021-kb4601382-os-builds-19041-844-and-19042-844-preview-1a7ed2b4-017d-2644-a1e8-dd6bf14cba76) |
|Windows 10| 1909| [KB4601380 ou posterior](https://support.microsoft.com/topic/february-16-2021-kb4601380-os-build-18363-1411-preview-2e3c38e1-a947-1033-8006-a30f3806da18)|

Você pode gerenciar o Microsoft Edge modo de quiosque atribuído ao aplicativo único de acesso por meio [Windows Configurações](/deployedge/microsoft-edge-configure-kiosk-mode#configure-using-windows-settings) e Intune.

### <a name="multi-app-kiosk"></a>Quiosque de vários aplicativos

O Microsoft Edge pode ser executado com [acesso atribuído a vários aplicativos](/windows/configuration/lock-down-windows-10-to-specific-apps) no Windows 10, que é o equivalente ao tipo de modo de quiosque "Navegação Normal" da Versão Herdada do Microsoft Edge. Para configurar o Microsoft Edge com acesso atribuído a vários aplicativos, siga as instruções sobre como [Configurar um quiosque para vários aplicativos](/windows/configuration/lock-down-windows-10-to-specific-apps). (A AUMID para o Microsoft Edge canal estável **é Microsoft.MicrosoftEdge.Stable_8wekyb3d8bbwe! MSEDGE**).

Ao usar Microsoft Edge com acesso atribuído a vários aplicativos, você pode configurar o quiosque do Microsoft Edge para usar as políticas do navegador [Microsoft Edge](./microsoft-edge-policies.md) para configurar a experiência de navegação para atender aos seus requisitos exclusivos.

### <a name="configure-using-windows-settings"></a>Configurar usando as configurações do Windows

As Configurações do Windows é a maneira mais simples de configurar um ou mais dispositivos em modo de quiosque de aplicativo único. Use as etapas a seguir para configurar um computador em modo de quiosque de aplicativo único.

1. As atualizações mínimas do sistema para os sistemas operacionais listados na tabela a seguir.

|Sistema operacional|Versão|Atualizações|
|--|--|--|
|Windows 10 | 2004 ou posterior|[KB4601382 ou posterior](https://support.microsoft.com/topic/february-24-2021-kb4601382-os-builds-19041-844-and-19042-844-preview-1a7ed2b4-017d-2644-a1e8-dd6bf14cba76) |
|Windows 10| 1909| [KB4601380 ou posterior](https://support.microsoft.com/topic/february-16-2021-kb4601380-os-build-18363-1411-preview-2e3c38e1-a947-1033-8006-a30f3806da18)|

2. Para testar os recursos mais recentes, você pode baixar o canal estável mais recente do [Microsoft Edge](https://www.microsoft.com/edge/business/download), versão 89 ou superior.

3. No computador modo de quiosque, abra as configurações do Windows e digite "modo de quiosque" no campo de pesquisa. Selecione  **Configurar um modo de quiosque (acesso atribuído)**, mostrada na próxima captura de tela para abrir a caixa de diálogo para criar o modo de quiosque.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-1-assigned-access.png" alt-text="Configurar o modo de quiosque com acesso atribuído":::

4. Na página **Configurar um quiosque** , selecione  **Introdução**.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-2-get-started.png" alt-text="Página modo de quiosque – introdução":::

5. Digite um nome para criar uma nova conta de quiosque ou escolha uma conta existente na lista suspensa preenchida e  **selecioneNext**.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-3-create-account.png" alt-text="Modo de quiosque - criar conta":::

6. Na página **Escolher um aplicativo de quiosque** , selecione **Microsoft Edge** e, em seguida,  **selecioneNext**.

   > [!NOTE]
   > Isso se aplica apenas ao Microsoft Edge Dev, Beta e a canais estáveis.

     :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-5c-choose-a-kiosk-app.png" alt-text="Exibição do modo quiosque – sinal digital de tela inteira":::

7. Escolha uma das opções a seguir para exibir o Microsoft Edge na execução no modo de quiosque:

   - Sinalização digital/interativa - Exibe um site específico no modo de tela inteira executando o Microsoft Edge.
   - Navegador público - Executa uma versão limitada com várias guias do Microsoft Edge.

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-5a-digital-sign.png" alt-text="Como o quiosque será usado - sinal digital de tela inteira":::

8. Selecione **Próximo**.
9. Digite a URL a ser carregada quando o quiosque for iniciado.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-6-enter-url.png" alt-text="Modo de quiosque - Inserir URL":::

10. Aceite o valor padrão de 5 minutos para o tempo ocioso ou escolha um outro valor.

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-7-enter-idle-time.png" alt-text="Modo de quiosque - Inserir tempo ocioso":::

11. Selecione **Próximo**.
12. Feche a janela de  **Configurações**  para salvar e aplicar suas opções.

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode--8-done.png" alt-text="Modo de quiosque – concluir configuração":::

13. Saia do dispositivo de modo de quiosque e entre com a conta de modo de quiosque local para validar a configuração.

## <a name="functional-limitations"></a>Limitações funcionais

Com o lançamento desta versão prévia do modo quiosque, continuamos trabalhando para melhorar o produto e adicionar novos recursos.

No momento, não oferecemos suporte aos seguintes recursos e recomendamos que você desligue:

- [InPrivateModeAvailability](./microsoft-edge-policies.md#inprivatemodeavailability)
- [IsolateOrigins](./microsoft-edge-policies.md#isolateorigins)
- [ManagedFavorites](./microsoft-edge-policies.md#managedfavorites)
- [EdgeShoppingAssistantEnabled](./microsoft-edge-policies.md#edgeshoppingassistantenabled)
- [EdgeCollectionsEnabled](./microsoft-edge-policies.md#edgecollectionsenabled)
- [UserFeedbackAllowed](./microsoft-edge-policies.md#userfeedbackallowed)
- [DefaultPopupsSetting](./microsoft-edge-policies.md#defaultpopupssetting)
- [StartupBoostEnabled](./microsoft-edge-policies.md#startupboostenabled)
- [Extensões](./microsoft-edge-policies.md#extensions-policies)
- [BackgroundModeEnabled](./microsoft-edge-policies.md#backgroundmodeenabled)
- [UserFeedbackAllowed](./microsoft-edge-policies.md#userfeedbackallowed)

## <a name="see-also"></a>Veja também

- [Página de destino do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Planejar sua implantação do Microsoft Edge](deploy-edge-plan-deployment.md)
- [Configurar quiosques e sinalizações digitais em edições do Windows desktop](/windows/configuration/kiosk-methods)
- [Planejar a transição do modo de quiosque](microsoft-edge-kiosk-mode-transition-plan.md)
