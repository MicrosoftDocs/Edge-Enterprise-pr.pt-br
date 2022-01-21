---
title: Saiba como Microsoft Edge manipula downloads de conteúdo misto
ms.author: collw
author: dan-wesley
manager: srugh
ms.date: 11/24/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Saiba mais sobre downloads de conteúdo misto e como o Microsoft Edge lida com eles.
ms.openlocfilehash: c199a8b763e456daac34bd1ba07e64ced50358f5
ms.sourcegitcommit: e7f3098d8b7d91cae20b5778a71a87daababc312
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/15/2022
ms.locfileid: "12298279"
---
# <a name="learn-how-microsoft-edge-handles-mixed-content-downloads"></a>Saiba como Microsoft Edge manipula downloads de conteúdo misto

Este artigo define downloads de conteúdo misto e explica como o Microsoft Edge lida com eles.

>[!NOTE]
>Este artigo se aplica ao Microsoft Edge versão 85 ou posterior.

## <a name="what-are-mixed-content-downloads"></a>O que são downloads de conteúdo misto?

Um download de conteúdo misto ocorre quando você inicia um download de uma página HTML carregada em uma conexão HTTPS segura, mas existe uma das seguintes condições:

- Um ou mais redirecionamentos do local de download foram carregados em uma conexão HTTP insegura.
- O local final do download foi carregado em uma conexão HTTP insegura.

Qualquer um dos cenários anteriores é um download de conteúdo misto porque a solicitação foi feita usando HTTPS seguro e as conexões HTTP e HTTPS são usadas para alcançar o destino final. Os navegadores modernos exibem avisos sobre esse tipo de conteúdo para indicar que esse download pode ser transferido de forma insegura, mesmo que a página original tenha sido acessada com segurança.

## <a name="download-warnings-and-user-options"></a>Baixar avisos e opções de usuário

O aviso de download garante que os usuários saibam que o arquivo que estão baixando pode ser lido por invasores mal-intencionados em sua rede. Esse aviso permite que um usuário tome uma decisão informada sobre se deseja baixar o arquivo.

No Microsoft Edge, os downloads de conteúdo misto serão bloqueados, mas os usuários poderão ignorar e baixar o arquivo se desejarem. O Microsoft Edge planeja começar a bloquear downloads de arquivos de conteúdo misto executáveis, começando com o Microsoft Edge versão 85, e bloqueará diferentes tipos de arquivos em versões futuras.

> [!NOTE]
> A implantação desse recurso está sujeita a alterações com base na programação de lançamentos e nos comentários dos usuários.

<!-- The schedule of the block for different filetypes is to be determined and may be impacted by usage data and user feedback. -->

Na prateleira de downloads, a mensagem de aviso de bloqueio se parece com o exemplo na próxima captura de tela.

 ![Aviso de conteúdo misto na bandeja de downloads](./media/edge-learnmore-mixed-content-downloads/edge-mixed-content-download-tray-warning.png)

Na página de download, o aviso de bloqueio é semelhante ao seguinte exemplo de captura de tela:

 ![Aviso de substituição de conteúdo misto](./media/edge-learnmore-mixed-content-downloads/edge-mixed-content-download-page-warning.png)

Se um usuário decidir manter o download, ele será solicitado a confirmar sua ação. A próxima captura de tela mostra um exemplo desse prompt de confirmação.

 ![Escolha o modo Internet Explorer](./media/edge-learnmore-mixed-content-downloads/edge-mixed-content-download-override.png)

## <a name="supporting-policies"></a>Políticas de apoio

As empresas que desejem excluir o bloqueio de conteúdo misto de sites específicos podem usar a política [InsecureContentAllowedForUrls](./microsoft-edge-policies.md#insecurecontentallowedforurls) para fazer isso.

## <a name="content-license"></a>Licença de conteúdo

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e compartilhado pela Chromium.org e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional](http://creativecommons.org/licenses/by/4.0/). A página original pode ser encontrada [aqui](https://developers.google.com/web/fundamentals/security/prevent-mixed-content/what-is-mixed-content).
  
<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br />Esse trabalho é licenciado sob uma <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons</a>.

## <a name="see-also"></a>Consulte também

- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
