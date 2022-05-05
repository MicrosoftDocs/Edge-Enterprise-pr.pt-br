---
title: Microsoft Edge desabilitar a modificação de 'document.domain'
ms.author: niarci
author: dan-wesley
manager: erikan
ms.date: 04/25/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Microsoft Edge desabilitar a modificação de 'document.domain'
ms.openlocfilehash: 197334da0f70aa2cfa081a240de383c79fbbf701
ms.sourcegitcommit: 592f6e40b13e28af588473b2a75c3ae697e5db2d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/05/2022
ms.locfileid: "12505697"
---
# <a name="microsoft-edge-will-disable-modifying-documentdomain"></a>Microsoft Edge desabilitar a modificação`document.domain`

> [!NOTE]
> Este artigo se aplica Microsoft Edge versão estável 106 ou posterior.

> [!WARNING]
> Se seu site depender de relaxar a política de mesma origem por meio `document.domain`de, sua ação será necessária. Continue a ler mais sobre por que isso está mudando ou acesse a [](#alternative-cross-origin-communication) comunicação alternativa entre origens para saber mais sobre mecanismos alternativos para obter comunicação entre origens.

## <a name="introduction"></a>Introdução

A propriedade "domain" da interface Document obtém ou define a parte de domínio da origem do documento atual, conforme usado pela política [de mesma origem](https://developer.mozilla.org/docs/Web/Security/Same-origin_policy).

A partir Microsoft Edge versão 106, `document.domain` as tentativas de modificar a propriedade usando JavaScript serão ignoradas. Você precisará usar abordagens alternativas, `postMessage()` como a API de Mensagens de Canal, para se comunicar entre origens.

Como alternativa, se seu site depende do relaxamento `document.domain` da política de mesma origem para funcionar corretamente, o site `Origin-Agent-Cluster: ?0` pode enviar um cabeçalho; esse cabeçalho deve ser enviado de todos os outros documentos que exigem o relaxamento.

> [!NOTE]
> `document.domain` não terá efeito se apenas um documento o definir.

## <a name="why-make-documentdomain-immutable"></a>Por que tornar `document.domain` imutável?

Alguns sites definidos `document.domain` para permitir a comunicação entre páginas "do mesmo site, mas entre origens". A `document.domain` configuração possibilita que documentos do mesmo site se comuniquem com mais facilidade. Como essa alteração relaxa a política de mesma origem, uma página pai pode acessar o documento de um iframe do mesmo site e percorrer a árvore DOM e [vice-versa](https://html.spec.whatwg.org/multipage/origin.html#relaxing-the-same-origin-restriction).

> [!IMPORTANT]
> Sites do mesmo site, mas entre origens, têm os mesmos [subdomínios eTLD+1](https://web.dev/same-site-same-origin/#:~:text=the%20whole%20site%20name%20is%20known%20as%20the%20etld%2B1) , mas diferentes.

Digamos que uma página em `https://parent.example.com` inserir uma página de iframe de `https://video.example.com`. Essas páginas têm o mesmo eTLD+1 (`example.com`) com subdomínios diferentes. Quando ambas as páginas são `document.domain` definidas como `'example.com'`, o navegador trata as duas páginas como se elas são da mesma origem.

Essa técnica é conveniente; mas apresenta um risco de segurança.  

## <a name="security-concerns-with-documentdomain"></a>Preocupações de segurança com `document.domain`

As preocupações de segurança `document.domain` relacionadas levaram a uma alteração na especificação que avisa os desenvolvedores sobre essa preocupação e informa a eles para evitar usá-la, se possível. A discussão atual com [outros fornecedores de navegador](https://github.com/w3ctag/design-reviews/issues/564) está se movendo na mesma direção.

Os exemplos a seguir mostram como um invasor pode abuso `document.domain`.

Considere um serviço de hospedagem compartilhado que fornece um subdomínio exclusivo para cada cliente. Se um desenvolvedor definir `document.domain` em sua página, a página de um invasor atendida de um subdomínio diferente poderá definir o mesmo valor e modificar o conteúdo da página da vítima.

Da mesma forma, considere um serviço de hospedagem compartilhado que atende a páginas usando uma porta diferente para cada cliente. Se um desenvolvedor definir `document.domain` em sua página, a página de um invasor atendida de uma porta diferente poderá definir o mesmo valor e modificar o conteúdo da página da vítima. Esse ataque é possível porque `document.domain` ignora o componente de número da porta da origem.

> [!NOTE]
>Para saber mais sobre as implicações de segurança da configuração `document.domain`, leia o artigo [Document.domain no MDN](https://developer.mozilla.org/docs/Web/API/Document/domain#setter).

## <a name="how-will-i-know-if-my-site-is-affected"></a>Como saberei se meu site foi afetado?

Se seu site for afetado por essa alteração, Microsoft Edge mostrará um aviso no painel Problemas do DevTools. A captura de tela a seguir mostra um exemplo desse aviso.

:::image type="content" source="media/edge-learnmore-origin-keyed-agent-cluster/document-domain-modification-warning.png" alt-text="Aviso quando document.domain é modificado.":::

Se você tiver um ponto de extremidade de relatório configurado, também será enviado relatórios de substituição. Saiba mais sobre [como usar a API de Relatórios](https://web.dev/reporting-api/) com serviços de coleta de relatórios existentes ou criando sua própria solução de relatório.

> [!TIP]
> Você pode executar seu site por meio da auditoria de [API preterida do LightHouse](https://web.dev/deprecations/) para localizar todas as APIs que estão agendadas para serem removidas Microsoft Edge.

## <a name="alternative-cross-origin-communication"></a>Comunicação alternativa entre origens

No momento, você tem duas opções para substituir `document.domain` por seu site. Na maioria dos casos de uso, [postMessage() entre origens](https://developer.mozilla.org/docs/Web/API/Window/postMessage) ou [a API de Mensagens de Canal](https://developer.mozilla.org/docs/Web/API/Channel_Messaging_API) pode substituir `document.domain`.

A lista a seguir mostra as etapas que um desenvolvedor precisa seguir `postMessage()` para usar em vez de `document.domain` para manipulação dom entre origens.

1. `https://parent.example.com` envia uma mensagem por `postMessage()` meio de um iframe que contém solicitando `https://video.example.com` que ele modifique seu próprio DOM.
2. `https://video.example.com` manipula seu DOM e usa para `postMessage` notificar o pai de seu sucesso.
3. `https://parent.example.com` reconhece o sucesso.

Para a etapa 1 em `https://parent.example.com`:

```

// Configure a handler to receive messages from the subframe.
iframe.addEventListener('message', (event) => { 

// Reject all messages except from https://video.example.com 
  if (event.origin !== 'https://video.example.com') return;
  
  // Filter success messages 
    if (event.data === 'succeeded') { 

    // DOM manipulation is succeeded 

  } 

}); 

// Send a message to the subframe at https://video.example.com

iframe.postMessage('Request DOM manipulation', 'https://video.example.com'); 

```

Para a etapa 2 em `https://video.example.com`:

```

// Configure a handler to receive messages from the parent frame.
window.addEventListener('message', (event) => {
 
  // Reject all messages except ones from https://parent.example.com 
  
  if (event.origin !== 'https://parent.example.com') return;
  
  // Perform requested DOM manipulation on https://video.example.com.
  
  if (event.data === "showTheButton") {
     document.getElementById('btnContinue').style.visibility = 'visible';
     // Send a success message back to the parent.

     event.source.postMessage('succeeded', event.origin); 
  }
}); 

```

### <a name="send-the-origin-agent-cluster-0-header-as-a-last-resort"></a>Enviar o `Origin-Agent-Cluster: ?0` cabeçalho como último recurso

Se você tiver motivos fortes para continuar a configuração `document.domain`, poderá enviar o `Origin-Agent-Cluster: ?0` cabeçalho de resposta no documento de destino.

```
Origin-Agent-Cluster: ?0 
```

O `Origin-Agent-Cluster` cabeçalho instrui o navegador se o documento deve ser manipulado pelo cluster do agente com chave de origem ou não. Para saber mais, leia `Origin-Agent-Cluster`[Solicitando isolamento de desempenho com o cabeçalho Origin-Agent-Cluster](https://web.dev/origin-agent-cluster/).

Quando você envia esse cabeçalho, seu documento pode continuar a ser definido `document.domain` mesmo depois que ele se torna imutável por padrão.

## <a name="browser-compatibility"></a>Compatibilidade do navegador

As organizações a seguir dão suporte à substituição `document.domain` no interesse da compatibilidade do navegador.

- A [especificação De](https://html.spec.whatwg.org/multipage/origin.html#:~:text=Because%20of%20these%20security%20pitfalls%2C%20this%20feature%20is%20in%20the%20process%20of%20being%20removed%20from%20the%20web%20platform) origem indica que o recurso deve ser removido.
- A [posição de padrões do Mozilla](https://github.com/mozilla/standards-positions/issues/601) considera desabilitar por `document.domain` padrão a criação de protótipos.
- [O WebKit](https://github.com/w3ctag/design-reviews/issues/564#issuecomment-768450217) indica que eles são moderadamente positivos sobre a substituição do `document.domain` setter.

## <a name="other-resources"></a>Outros recursos

- [Document.domain](https://developer.mozilla.org/docs/Web/API/Document/domain)
- [Isolamento e substituição de origem `document.domain`](https://github.com/mikewest/deprecating-document-domain/)
- [Preterindo setter `document.domain`](https://github.com/w3ctag/design-reviews/issues/564)

## <a name="content-license"></a>Licença de conteúdo

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e compartilhado pela Chromium.org e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional](http://creativecommons.org/licenses/by/4.0/). A página original pode ser encontrada [aqui](https://developer.chrome.com/blog/immutable-document-domain/).

<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br />Esse trabalho é licenciado sob uma <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons</a>.
