---
title: Planejar a transição do modo de quiosque
ms.author: aguta
author: aguta
manager: srugh
ms.date: 02/05/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Planejar a transição do modo de quiosque
ms.openlocfilehash: 3a438c6dd71d9e1f0e644d24e3b1d1d60b099e8e
ms.sourcegitcommit: b1d49b229c47dc1d99e1b677d75aad38b3334ed6
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/05/2021
ms.locfileid: "11314231"
---
# Planejar a transição do modo de quiosque

Este artigo fornece orientação sobre como fazer a transição de seu quiosque da Versão Prévia do Microsoft Edge para o Microsoft Edge.  

> [!NOTE]
> Este artigo se aplica aos canais Microsoft Edge Stable, Beta e Dev, versão 87 ou posterior.

> [!IMPORTANT]
> Quando o suporte para Versão Prévia do Microsoft Edge encerrar em 9 de março de 2021, ele será removido e substituído pelo Microsoft Edge no Chromium como parte do Windows Update em abril. Para obter detalhes, vá para [esta postagem do blog](https://aka.ms/EdgeLegacyEOS). Para continuar a usar seus cenários de quiosque baseados em navegador, você precisa instalar o Microsoft Edge no Chromium e configurar o modo quiosque antes do lançamento do Windows Update de abril para o seu dispositivo.

## Etapas de configuração do quiosque

Use as etapas a seguir como guia para configurar um quiosque no Microsoft Edge.

**Etapa 1: avalie suas necessidades em relação à funcionalidade do modo quiosque lançada (e futura).** A tabela a seguir lista os recursos compatíveis com o modo quiosque no Microsoft Edge no Chromium e na Versão Prévia do Microsoft Edge. Use esta tabela como um guia para a transição para o Microsoft Edge, comparando como esses recursos são suportados em ambas as versões do Microsoft Edge.

|Característica|Sinalização Interativa/Digital|Navegação pública|Disponível com a versão Microsoft Edge (e superior)|Disponível com a Versão Prévia do Microsoft Edge|
|-|-|-|-|-|
|Navegação InPrivate|S|S|89|Y|
|Redefinir em inatividade|S|S|89|Y|
|[Barra de endereços somente leitura](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#kioskaddressbareditingenabled) (política) |N|S |89|N|
|[Excluir downloads na saída](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#kioskdeletedownloadsonexit) (política)  | S|S |89|N|
|F11 bloqueado (entrar/sair de tela inteira) | S | S | 89 |Y|
|F12 bloqueado (iniciar Ferramentas do Desenvolvedor) | S | S | 89 |Y|
| Suporte a várias guias | N| S| 89|Y|
|[Permitir suporte a URL](https://docs.microsoft.com/deployedge/microsoft-edge-policies#urlallowlist) (política)|Y|S|89|N|
|[Bloquear suporte a URL](https://docs.microsoft.com/deployedge/microsoft-edge-policies#urlblocklist) (política)|Y|S|89|N|
|[Mostrar botão Página Principal](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#showhomebutton) (política)|N|S|89|Y|
|[Gerenciar favoritos](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#managedfavorites) (política)|N|S|89|Y|
|[Habilitar impressora](https://docs.microsoft.com/deployedge/microsoft-edge-policies#printingenabled) (política)|Y|S|89|Y|
|[Configurar a URL da página de nova guia](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#newtabpagelocation) (política)|N|S||Y|
|Botão encerrar sessão | N| S| 89|Y|
|Todas as URLs internas do Microsoft Edge estão bloqueadas, exceto *edge://downloads* e *edge://print* |N|S|89|Y|
| Ctrl+N bloqueado (abrir uma nova janela) | S | S | 89 |Y|
| Ctrl+T bloqueado (abrir nova guia) |Y | S | 89 |Y|
|Configurações e mais (...) exibirá somente as opções necessárias  |Y |S |89 |Y|
|Restringir o lançamento de outros aplicativos do navegador|Y|Y|90/91|Y|
|Bloqueio das configurações de impressão da interface do usuário|Y|Y|90/91|Y|
|[Definir a página da nova guia como a home page](https://docs.microsoft.com/deployedge/microsoft-edge-policies#homepageisnewtabpage) (política)|-|-|A ser definido|Y|

> [!NOTE]
> Para obter informações sobre a programação de lançamento do Microsoft Edge, confira [Agenda de lançamento do Microsoft Edge](microsoft-edge-release-schedule.md).

**Etapa 2: teste o novo quiosque no Microsoft Edge.** Recomendamos que você teste a configuração do modo quiosque no Microsoft Edge. Uma maneira rápida e fácil de testar o modo quiosque é configurar um único aplicativo de acesso atribuído usando as Configurações do Windows, conforme descrito a seguir.

1. Instale o Windows 10 Insider Preview mais recente, versão 20215 ou superior. Siga as instruções em [Introdução às Compilações de Visualização do Windows 10 Insider](https://docs.microsoft.com/windows-insider/get-started).
2. Instale a versão mais recente do [ canal Microsoft Edge Stable ](https://www.microsoft.com/edge), versão 87 ou superior.  Para testar os recursos mais recentes, você pode baixar o [ canal Microsoft Edge Beta ](https://www.microsoftedgeinsider.com/download) mais recente, versão 89 ou superior.

   > [!IMPORTANT]
   > Como uma instalação no nível do dispositivo é necessária, o canal Canary não é compatível.

3. No computador do quiosque, abra as Configurações do Windows e digite "quiosque" no campo de pesquisa. Selecione  **Configurar um modo de quiosque (acesso atribuído)**, mostrada na próxima captura de tela para abrir a caixa de diálogo para criar o modo de quiosque.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-1-assigned-access.png" alt-text="Configurar o modo de quiosque com acesso atribuído":::

4. Na página **Configurar um modo de quiosque** , clique em  **Introdução**.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-2-get-started.png" alt-text="Página modo de quiosque – introdução":::

5. Digite um nome para criar uma nova conta modo de quiosque ou escolha uma conta existente na lista suspensa preenchida e clique em  **Avançar**.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-3-create-account.png" alt-text="Modo de quiosque - criar conta":::

6. Na página ** Escolha um aplicativo de quiosque **  , selecione ** Microsoft Edge ** e clique em  ** Avançar **.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-4-pick-app.png" alt-text="Modo quiosque - escolha um aplicativo":::

7. Selecione uma das seguintes opções de exibição do Microsoft Edge durante a execução no modo quiosque:

   - Sinalização digital/interativa - exibe um site específico em modo de tela inteira, executando o Microsoft Edge.
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

13. Saia do dispositivo de quiosque e faça login com a conta do quiosque local para validar a configuração.

**Etapa 3: desenvolva um plano de transição.** Com base em seus testes e necessidades organizacionais, recomendamos desenvolver um plano de transição e mudar para o Microsoft Edge no Chromium antes que o suporte para a Versão Prévia do Microsoft Edge encerre em 9 de março de 2021.

## Cenários adicionais que exigem a recriação de um modo quiosque existente

Se você atualizar para o Windows 10, versão 20H2, o Microsoft Edge no Chromium será instalado e a Versão Prévia do Microsoft Edge ficará oculta. Neste caso, você precisará configurar o modo quiosque novamente no Microsoft Edge no Chromium.

## Como obter ajuda

O modo quiosque pode ser uma parte importante de seus negócios diários, por isso queremos ajudar a tornar essa transição o mais suave possível e ajudá-lo a evitar interrupções. Se sua empresa precisa de ajuda na transição para o Microsoft Edge no Chromium:

- [ Suporte ](https://support.serviceshub.microsoft.com/supportforbusiness/create?sapId=a77ee9b7-b6b6-aa08-d7b9-887ebe228207) está disponível na Microsoft. 
- O [ suporte FastTrack ](https://www.microsoft.com/fasttrack/microsoft-365/microsoft-edge?rtc=1) também está disponível sem custo adicional para clientes com 150 ou mais estações pagas do Windows 10 Enterprise.
- [ App Assure ](https://www.microsoft.com/en-us/fasttrack/microsoft-365/app-assure) está disponível se você tiver problemas de compatibilidade de site ou aplicativo.

## Ver também

- [Página inicial do Microsoft Edge Empresa](https://aka.ms/EdgeEnterprise)
- [Novo Microsoft Edge para substituir a Versão Prévia do Microsoft Edge pelo lançamento do Windows 10 Update Tuesday de abril](https://techcommunity.microsoft.com/t5/microsoft-365-blog/new-microsoft-edge-to-replace-microsoft-edge-legacy-with-april-s/ba-p/2114224)