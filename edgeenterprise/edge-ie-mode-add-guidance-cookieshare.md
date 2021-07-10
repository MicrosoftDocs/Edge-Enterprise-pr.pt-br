---
title: Compartilhamento de cookies do Microsoft Edge para o Internet Explorer
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: 'Como compartilhar os cookies do Microsoft Edge para o Internet Explorer '
ms.openlocfilehash: 8f1a38106e49f71aa9d27f32cfecbd0df44eaf9f
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/09/2021
ms.locfileid: "11641837"
---
# <a name="cookie-sharing-from-microsoft-edge-to-internet-explorer"></a>Compartilhamento de cookies do Microsoft Edge para o Internet Explorer

>[!Note]
> O aplicativo de área de trabalho Internet Explorer 11 será desativado e ficará sem suporte em 15 de junho de 2022 (para obter uma lista do que está no escopo, [consulte as Perguntas frequentes](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/internet-explorer-11-desktop-app-retirement-faq/ba-p/2366549)). Os mesmos aplicativos e sites do IE11 que você usa hoje podem abrir no Microsoft Edge com o modo Internet Explorer. [Saiba mais aqui](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/).

Este artigo explica como configurar o compartilhamento de cookie de sessão de um processo do Microsoft Edge para o processo do Internet Explorer, ao usar o modo Internet Explorer.

> [!NOTE]
> Este artigo se aplica ao Microsoft Edge versão 87 ou posterior.

## <a name="prerequisites"></a>Pré-requisitos

- Atualizações do Windows

  - Windows 10, versão 2004, Windows Server, versão 2004-KB4571744 ou superior
  - Windows 10, versão 1909, Windows Server, versão 1909 – KB4566116 ou superior
  - Windows 10, versão 1903, Windows Server, versão 1903 – KB4566116 ou superior
  - Windows 10, versão 1809, Windows Server, versão 1809 e Windows Server 2019 - KB4571748 ou superior
  - Windows 10 versão 1803 - KB4577032 ou superior

- Microsoft Edge versão 87 ou posterior
- [ Modo IE ](./edge-ie-mode.md)   configurado com Lista de Sites do modo Empresarial

## <a name="overview"></a>Visão geral

Uma configuração comum em grandes organizações é ter um aplicativo que funciona em um link de navegador moderno para outro aplicativo, que pode ser configurado para abrir no modo Internet Explorer com logon Único (SSO) habilitado como parte do fluxo de trabalho.

Por padrão, os processos do Microsoft Edge e do Internet Explorer não compartilham os cookies de sessão e isso pode ser inconveniente em alguns casos. Por exemplo, quando um usuário precisa se reautenticar no modo do Internet Explorer ou ao sair de uma sessão do Microsoft Edge, ele não sai da sessão do modo Internet Explorer. Nesses cenários, você pode configurar os cookies específicos e definidos pelo SSO para serem enviados do Microsoft Edge para o Internet Explorer para que a experiência de autenticação torne-se mais contínua, eliminando a necessidade de reautenticação.

> [!NOTE]
> Os cookies de sessão só podem ser compartilhados do Microsoft Edge para o Internet Explorer. Não é possível compartilhar os cookies de sessão ao contrário (do Internet Explorer para o Microsoft Edge).

## <a name="how-cookie-sharing-works"></a>Como funciona o compartilhamento de cookies

O XML da lista de sites do Modo Empresarial foi estendido para permitir que os elementos adicionais especifiquem os cookies que precisam ser compartilhados de uma sessão do Microsoft Edge com o Internet Explorer.  

Na primeira vez que uma guia do modo do Internet Explorer é criada em uma sessão do Microsoft Edge, todos os cookies correspondentes são compartilhados com a sessão do Internet Explorer. Subsequentemente, sempre que um cookie que corresponde a uma regra é adicionado, excluído ou modificado, ele é enviado como uma atualização para a sessão do Internet Explorer. O conjunto de cookies compartilhados também é reavaliado quando a lista de sites é atualizada.

### <a name="updated-schema-elements"></a>Elementos do esquema atualizados

A tabela a seguir descreve o elemento \<shared-cookie\> adicionado para oferecer suporte ao recurso de compartilhamento de cookies.

| Elemento| Descrição |
|-|-|
| \<shared-cookie **domain**=".contoso.com" **name**="cookie1"\>\</shared-cookie\><br><br>OU<br><br>\<shared-cookie **host**="subdomain.contoso.com" **name**="cookie2"\>\</shared-cookie\>   |** (Obrigatório) ** Um elemento \<shared-cookie\> requer, no mínimo, um atributo de * domínio * (para os cookies de domínio) ou um * host * (para os cookies somente de host) e um atributo *nome*.<br>Devem corresponder exatamente ao domínio e ao nome do cookie, respectivamente. **Observe** que os subdomínios não correspondem.<br><br>O atributo *domínio* é usado para cookies de domínio (e um ponto inicial é permitido, mas opcional).<br>O atributo * host * é usado para cookies somente de host (e um entrelinhamento é um erro). Especificar que nenhum ou ambos resultará em erro.<br>* Um cookie é um cookie de domínio se um domínio foi especificado na cadeia de caracteres do cookie (via cabeçalho de resposta HTTP Set-Cookie ou document.cookie JS API). Um cookie de domínio se aplica ao domínio especificado e a todos os subdomínios. Se um domínio não foi especificado na cadeia de caracteres do cookie, o cookie é um cookie somente de host e só se aplica ao host específico para o qual ele foi definido. Observe que algumas classes de URLs, como nomes de host de palavra única (por exemplo, http://intranetsite) e endereços IP (por exemplo, http://10.0.0.1) podem definir apenas os cookies de host.    |
| \<shared-cookie **host**="subdomain.contoso.com" **name**="cookie2" **path**="/a/b/c"\>\</shared-cookie\>  | ** (Opcional) ** Um atributo * caminho * pode ser especificado. Se nenhum atributo de caminho for especificado (ou se o atributo de caminho estiver vazio), quaisquer cookies que correspondam a domínio/host e nome corresponderão à política, independentemente do caminho (regra de caractere curinga).<br><br>Se um caminho for especificado, ele deve ser uma correspondência exata.<br>Se um cookie corresponder a uma regra com um caminho, isso terá precedência sobre uma regra sem caminho. |

#### <a name="sharing-example"></a>Exemplo de compartilhamento

```xml
<site-list version="1">
<shared-cookie domain=".contoso.com" name="cookie1"></shared-cookie> 
<shared-cookie host="subdomain.contoso.com" name="cookie2" path="/a/b/c">
</shared-cookie>
</site-list>
```

## <a name="see-also"></a>Consulte também

- [Sobre o modo IE](./edge-ie-mode.md)
- [Informações de sites configuráveis](./edge-learnmore-configurable-sites-ie-mode.md)
- [Informações adicionais sobre o Modo Empresarial](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)