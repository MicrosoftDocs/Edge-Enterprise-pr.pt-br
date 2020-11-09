---
title: Compartilhamento de cookies do Microsoft Edge para o Internet Explorer
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 11/05/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 'Como compartilhar os cookies do Microsoft Edge para o Internet Explorer '
ms.openlocfilehash: 5740a4ce31a240573b9106e7a20a5c44688aca0a
ms.sourcegitcommit: 2024629929044e2dcf146674058c1d6312c32e9a
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2020
ms.locfileid: "11157533"
---
# Compartilhamento de cookies do Microsoft Edge para o Internet Explorer

Este artigo explica como configurar o compartilhamento de cookie de sessão de um processo do Microsoft Edge para o processo do Internet Explorer, ao usar o modo Internet Explorer.

> [!NOTE]
> Este artigo se aplica ao Microsoft Edge versão 87 ou posterior.

## Pré-requisitos

- Atualizações do Windows

  - Windows 10 versão 2004, versão do servidor Windows 2004 - KB4571744 ou superior
  - Windows 10 versão 1909, versão do servidor Windows 1909 - KB4566116 ou superior
  - Windows 10 versão 1903, versão do servidor Windows 1903 - KB4566116 ou superior
  - Windows 10 versão 1809, versão do Servidor Windows 1809 e Servidor Windows 2019 - KB4571748 ou superior
  - Windows 10 versão 1803 - KB4577032 ou superior

- Microsoft Edge versão 87 ou posterior
- [ Modo IE ](https://aka.ms/iemodeonedge)   configurado com Lista de Sites do modo Empresarial

## Visão geral

Uma configuração comum em grandes organizações é ter um aplicativo que funciona em um link de navegador moderno para outro aplicativo, que pode ser configurado para abrir no modo Internet Explorer com logon Único (SSO) habilitado como parte do fluxo de trabalho.

Por padrão, os processos do Microsoft Edge e do Internet Explorer não compartilham os cookies de sessão e isso pode ser inconveniente em alguns casos. Por exemplo, quando um usuário precisa se reautenticar no modo do Internet Explorer ou ao sair de uma sessão do Microsoft Edge, ele não sai da sessão do modo Internet Explorer. Nesses cenários, você pode configurar os cookies específicos e definidos pelo SSO para serem enviados do Microsoft Edge para o Internet Explorer para que a experiência de autenticação torne-se mais contínua, eliminando a necessidade de reautenticação.

> [!NOTE]
> Os cookies de sessão só podem ser compartilhados do Microsoft Edge para o Internet Explorer. Não é possível compartilhar os cookies de sessão ao contrário (do Internet Explorer para o Microsoft Edge).

## Como funciona o compartilhamento de cookies

O XML da lista de sites do Modo Empresarial foi estendido para permitir que os elementos adicionais especifiquem os cookies que precisam ser compartilhados de uma sessão do Microsoft Edge com o Internet Explorer.  

Na primeira vez que uma guia do modo do Internet Explorer é criada em uma sessão do Microsoft Edge, todos os cookies correspondentes são compartilhados com a sessão do Internet Explorer. Subsequentemente, sempre que um cookie que corresponde a uma regra é adicionado, excluído ou modificado, ele é enviado como uma atualização para a sessão do Internet Explorer. O conjunto de cookies compartilhados também é reavaliado quando a lista de sites é atualizada.

### Elementos do esquema atualizados

A tabela a seguir descreve o elemento \<shared-cookie\> adicionado para oferecer suporte ao recurso de compartilhamento de cookies.

| Elemento| Descrição |
|-|-|
| \<shared-cookie **domain**=".contoso.com" **name**="cookie1"\>\</shared-cookie\><br><br>OU<br><br>\<shared-cookie **host**="subdomain.contoso.com" **name**="cookie2"\>\</shared-cookie\>   |** (Obrigatório) ** Um elemento \<shared-cookie\> requer, no mínimo, um atributo de * domínio * (para os cookies de domínio) ou um * host * (para os cookies somente de host) e um atributo *nome*.<br>Devem corresponder exatamente ao domínio e ao nome do cookie, respectivamente. **Observe** que os subdomínios não correspondem.<br><br>O atributo *domínio* é usado para cookies de domínio (e um ponto inicial é permitido, mas opcional).<br>O atributo * host * é usado para cookies somente de host (e um entrelinhamento é um erro). Especificar que nenhum ou ambos resultará em erro.<br>* Um cookie é um cookie de domínio se um domínio foi especificado na cadeia de caracteres do cookie (via cabeçalho de resposta HTTP Set-Cookie ou document.cookie JS API). Um cookie de domínio se aplica ao domínio especificado e a todos os subdomínios. Se um domínio não foi especificado na cadeia de caracteres do cookie, o cookie é um cookie somente de host e só se aplica ao host específico para o qual ele foi definido. Observe que algumas classes de URLs, como nomes de host de palavra única (por exemplo, http://intranetsite) e endereços IP (por exemplo, http://10.0.0.1) podem definir apenas os cookies de host.    |
| \<shared-cookie **host**="subdomain.contoso.com" **name**="cookie2" **path**="/a/b/c"\>\</shared-cookie\>  | ** (Opcional) ** Um atributo * caminho * pode ser especificado. Se nenhum atributo de caminho for especificado (ou se o atributo de caminho estiver vazio), quaisquer cookies que correspondam a domínio/host e nome corresponderão à política, independentemente do caminho (regra de caractere curinga).<br><br>Se um caminho for especificado, ele deve ser uma correspondência exata.<br>Se um cookie corresponder a uma regra com um caminho, isso terá precedência sobre uma regra sem caminho. |

#### Exemplo de compartilhamento

```xml
<site-list version="1">
<shared-cookie domain=".contoso.com" name="cookie1"></shared-cookie> 
<shared-cookie host="subdomain.contoso.com" name="cookie2" path="/a/b/c">
</shared-cookie>
</site-list>
```

## Consulte também

- [Sobre o modo IE](https://docs.microsoft.com/deployedge/edge-ie-mode)
- [Informações de sites configuráveis](https://docs.microsoft.com/deployedge/edge-learnmore-configurable-sites-ie-mode)
- [Informações adicionais sobre o Modo Empresarial](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)