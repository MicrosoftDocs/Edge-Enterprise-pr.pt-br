---
title: Planejar a transição do modo de quiosque
ms.author: v-danwesley
author: dan-wesley
manager: srugh
ms.date: 05/26/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Planejar a transição do modo de quiosque
ms.openlocfilehash: c8f2605ef15d8fec8fac32cb94099b4b394e81aa
ms.sourcegitcommit: 3771634abdfd7d376778ad6ae10a385d5658b7d3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/27/2022
ms.locfileid: "12551796"
---
# <a name="plan-your-kiosk-mode-transition"></a>Planejar a transição do modo de quiosque

Este artigo fornece orientação sobre como fazer a transição de seu quiosque da Versão Prévia do Microsoft Edge para o Microsoft Edge.  

> [!NOTE]
> Este artigo se aplica aos canais Microsoft Edge Stable, Beta e Dev, versão 87 ou posterior.

> [!IMPORTANT]
> Quando o suporte para Versão Prévia do Microsoft Edge encerrar em 9 de março de 2021, ele será removido e substituído pelo Microsoft Edge no Chromium como parte do Windows Update em abril. Para obter detalhes, vá para [esta postagem do blog](https://aka.ms/EdgeLegacyEOS). Para continuar a usar seus cenários de quiosque baseados em navegador, você precisa instalar o Microsoft Edge no Chromium e configurar o modo quiosque antes do lançamento do Windows Update de abril para o seu dispositivo.

## <a name="kiosk-setup-steps"></a>Etapas de configuração do quiosque

Use as etapas a seguir como guia para configurar um quiosque no Microsoft Edge.

**Etapa 1: avalie suas necessidades em relação à funcionalidade do modo quiosque lançada (e futura).** A tabela a seguir lista os recursos compatíveis com o modo quiosque no Microsoft Edge no Chromium e na Versão Prévia do Microsoft Edge. Use esta tabela como um guia para a transição para o Microsoft Edge, comparando como esses recursos são suportados em ambas as versões do Microsoft Edge.

|Característica|Sinalização Interativa/Digital|Navegação pública|Disponível com a versão do Microsoft Edge (e superior)|Disponível com Versão Prévia do Microsoft Edge|
|-|-|-|-|-|
|Navegação InPrivate.|S|S|89|S|
|Redefinir em inatividade|S|S|89|S|
|[Barra de endereços somente leitura](./microsoft-edge-policies.md#kioskaddressbareditingenabled) (política) |N|S |89|N|
|[Excluir downloads na saída](./microsoft-edge-policies.md#kioskdeletedownloadsonexit) (política)  | S|S |89|N|
|F11 bloqueado (entrar/sair de tela inteira) | S | S | 89 |S|
|F12 bloqueado (iniciar Ferramentas do Desenvolvedor) | S | S | 89 |S|
| Suporte a várias guias | N| S| 89|S|
|[Permitir suporte de URL](./microsoft-edge-policies.md#urlallowlist) (política)|S|S|89|N|
|[Bloquear suporte de URL](./microsoft-edge-policies.md#urlblocklist) (política)|S|S|89|N|
|[Mostrar botão Página Principal](./microsoft-edge-policies.md#showhomebutton) (política)|N|S|89|S|
|[Gerenciar favoritos](./microsoft-edge-policies.md#managedfavorites) (política)|N|S|89|S|
|[Habilitar impressora](./microsoft-edge-policies.md#printingenabled) (política)|S|S|89|S|
|[Configurar a URL da página de nova guia](./microsoft-edge-policies.md#newtabpagelocation) (política)|N|S|89|S|
|Botão encerrar sessão | N| S| 89|S|
|Todas as URLs internas do Microsoft Edge estão bloqueadas, exceto *edge://downloads* e *edge://print* |N|S|89|S|
| Ctrl+N bloqueado (abrir uma nova janela) | S | S | 89 |S|
| Ctrl+T bloqueado (abrir nova guia) |S | S | 89 |S|
|Configurações e mais (...) exibirá somente as opções necessárias  |S |S |89 |S|
|Restringir o lançamento de outros aplicativos do navegador|S|S|90|S|
|Bloqueio de configurações de impressão da IU|S|S|90|S|
|[Definir a página da nova guia como a página inicial ](./microsoft-edge-policies.md#homepageisnewtabpage) (política)|N|S|90|S|

> [!NOTE]
> Para obter informações sobre a programação de lançamento do Microsoft Edge, confira [Agenda de lançamento do Microsoft Edge](microsoft-edge-release-schedule.md).

**Etapa 2: teste o novo quiosque no Microsoft Edge.** Recomendamos que você teste a configuração do modo quiosque no Microsoft Edge. Uma maneira rápida e fácil de testar o modo quiosque é configurar um único aplicativo de acesso atribuído usando as Configurações do Windows, conforme descrito a seguir.

1. As atualizações mínimas do sistema para os sistemas operacionais listados na tabela a seguir.

|Sistema operacional|Versão|Atualizações|
|--|--|--|
|Windows 10 | 2004 ou posterior|[KB4601382 ou posterior](https://support.microsoft.com/topic/february-24-2021-kb4601382-os-builds-19041-844-and-19042-844-preview-1a7ed2b4-017d-2644-a1e8-dd6bf14cba76) |
|Windows 10| 1909| [KB4601380 ou posterior](https://support.microsoft.com/topic/february-16-2021-kb4601380-os-build-18363-1411-preview-2e3c38e1-a947-1033-8006-a30f3806da18)|

2. Para testar os recursos mais recentes, você pode baixar o [canal Microsoft Edge Beta ](https://www.microsoftedgeinsider.com/download)mais recente, versão 89 ou superior.

   > [!IMPORTANT]
   > Como uma instalação no nível do dispositivo é necessária, o canal Canary não é compatível.

3. No computador do quiosque, abra as Configurações do Windows e digite "quiosque" no campo de pesquisa. Selecione  **Configurar um modo de quiosque (acesso atribuído)**, mostrada na próxima captura de tela para abrir a caixa de diálogo para criar o modo de quiosque.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-1-assigned-access.png" alt-text="Configurar o modo de quiosque com acesso atribuído":::

4. Na página **Configurar um modo de quiosque** , clique em  **Introdução**.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-2-get-started.png" alt-text="Página modo de quiosque – introdução":::

5. Digite um nome para criar uma nova conta modo de quiosque ou escolha uma conta existente na lista suspensa preenchida e clique em  **Avançar**.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-3-create-account.png" alt-text="Modo de quiosque - criar conta":::

6. Na página ** Escolha um aplicativo de quiosque **  , selecione **Microsoft Edge** e clique em  **Avançar**.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-5c-choose-a-kiosk-app.png" alt-text="Escolher um Quiosque: sinal digital de tela inteira":::

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

## <a name="additional-scenarios-that-require-you-to-recreate-an-existing-kiosk-mode"></a>Cenários adicionais que exigem a recriação de um modo quiosque existente

Se você atualizar para o Windows 10, versão 20H2, o Microsoft Edge no Chromium será instalado e a Versão Prévia do Microsoft Edge ficará oculta. Neste caso, você precisará configurar o modo quiosque novamente no Microsoft Edge no Chromium.

## <a name="how-to-get-help"></a>Como obter ajuda

O modo quiosque pode ser uma parte importante de seus negócios diários, por isso queremos ajudar a tornar essa transição o mais suave possível e ajudá-lo a evitar interrupções. Se sua empresa precisa de ajuda na transição para o Microsoft Edge no Chromium:

- [ Suporte ](https://support.serviceshub.microsoft.com/supportforbusiness/create?sapId=a77ee9b7-b6b6-aa08-d7b9-887ebe228207) está disponível na Microsoft. 
- O [ suporte FastTrack ](https://www.microsoft.com/fasttrack/microsoft-365/microsoft-edge?rtc=1) também está disponível sem custo adicional para clientes com 150 ou mais estações pagas do Windows 10 Enterprise.
- [ App Assure ](https://www.microsoft.com/en-us/fasttrack/microsoft-365/app-assure) está disponível se você tiver problemas de compatibilidade de site ou aplicativo.

## <a name="see-also"></a>Ver também

- [Página inicial do Microsoft Edge Empresa](https://aka.ms/EdgeEnterprise)
- [Novo Microsoft Edge para substituir a Versão Prévia do Microsoft Edge pelo lançamento do Windows 10 Update Tuesday de abril](https://techcommunity.microsoft.com/t5/microsoft-365-blog/new-microsoft-edge-to-replace-microsoft-edge-legacy-with-april-s/ba-p/2114224)