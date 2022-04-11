---
title: Compartilhamento de cookies entre Microsoft Edge e Internet Explorer
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 03/08/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Saiba como compartilhar cookies entre o Microsoft Edge Internet Explorer
ms.openlocfilehash: 403404c96b91cde62e714324864b87ff2e57f8db
ms.sourcegitcommit: dd8cdbd35726c795ddce917e549ddf17ee7f5290
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/11/2022
ms.locfileid: "12473412"
---
# <a name="cookie-sharing-between-microsoft-edge-and-internet-explorer"></a>Compartilhamento de cookies entre Microsoft Edge e Internet Explorer

>[!Note]
> O aplicativo da área de trabalho do Internet Explorer (IE) 11 será desativado e ficará sem suporte em 15 de junho de 2022. Para ver o que está no escopo e fora do escopo quando o IE 11 é desativado, confira as perguntas frequentes sobre desativação de aplicativos da área de trabalho do [Internet Explorer 11](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/internet-explorer-11-desktop-app-retirement-faq/ba-p/2366549). Os mesmos aplicativos e sites do IE 11 que você usa hoje podem ser abertos Microsoft Edge com o modo Internet Explorer. Para saber mais, confira [O futuro do Internet Explorer no Windows 10 está em Microsoft Edge](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/).

Este artigo explica como configurar o compartilhamento de cookie de sessão entre um processo Microsoft Edge e um processo do Internet Explorer, ao usar o modo Internet Explorer.

> [!NOTE]
> Este artigo se aplica ao Microsoft Edge versão 87 ou posterior.

## <a name="prerequisites"></a>Pré-requisitos

Para compartilhar cookies de sessão do Microsoft Edge para o Internet Explorer:

- Atualizações do Windows

  - Windows 11
  - Windows 10, versão 2004, Windows Server, versão 2004-KB4571744 ou superior
  - Windows 10, versão 1909, Windows Server, versão 1909 – KB4566116 ou superior
  - Windows 10, versão 1903, Windows Server, versão 1903 – KB4566116 ou superior
  - Windows 10, versão 1809, Windows Server, versão 1809 e Windows Server 2019 - KB4571748 ou superior
  - Windows 10 versão 1803 - KB4577032 ou superior
  - Windows 10 Enterprise LTSC 2016 e Windows Server 2016 - KB4580346 ou superior
  - Windows 10 Enterprise 2015 LTSB - KB4580327 ou superior
  - Windows 8.1 e Windows Server 2012 R2 – KB4586768 ou superior
  - Windows 10 Enterprise LTSC 2016 e Windows Server 2016 - KB4580346 ou superior
  - Windows 10 Enterprise 2015 LTSB - KB4580327 ou superior
  - Windows 8.1 e Windows Server 2012 R2 – KB4586768 ou superior
- Microsoft Edge versão 87 ou posterior
- [ Modo IE ](./edge-ie-mode.md)   configurado com Lista de Sites do modo Empresarial

Para compartilhar cookies de sessão entre Microsoft Edge Internet Explorer:

- Atualizações do Windows
  
  - Windows 11 - KB5010414 ou superior
  - Windows Server 2022 – KB5010421 ou superior
  - Windows 10 versão 20H2 – KB5010415 ou superior
  - Windows 10 versão 21H1 – KB5010415 ou superior
  - Windows 10 versão 21H2 - KB5010415 ou superior
- Microsoft Edge versão 99 ou posterior
- [ Modo IE ](./edge-ie-mode.md)   configurado com Lista de Sites do modo Empresarial

## <a name="overview"></a>Visão geral

Uma configuração comum em grandes organizações é ter um aplicativo que funciona em um link de navegador moderno para outro aplicativo, que pode ser configurado para abrir no modo Internet Explorer com logon Único (SSO) habilitado como parte do fluxo de trabalho.

Por padrão, os Microsoft Edge e o Internet Explorer não compartilham cookies de sessão, e essa falta de compartilhamento pode ser inconveniente em alguns casos. Por exemplo, quando um usuário precisa autenticar novamente no modo Internet Explorer ou ao sair de uma sessão do Microsoft Edge não sai da sessão do modo Internet Explorer. Nesses cenários, você pode configurar cookies específicos definidos pelo SSO para serem enviados do Microsoft Edge para o Internet Explorer para que a experiência de autenticação se torne mais contínua, eliminando a necessidade de reautenticação.

> [!NOTE]
> Antes Microsoft Edge versão 99, os cookies de sessão só podem ser compartilhados Microsoft Edge internet Explorer. A partir Microsoft Edge versão 99, o compartilhamento de cookies de sessão ao contrário (do Internet Explorer para o Microsoft Edge) é possível.

## <a name="how-cookie-sharing-works"></a>Como funciona o compartilhamento de cookies

O XML da lista de sites do modo Enterprise é estendido para permitir que mais elementos especifiquem cookies de sessão que precisam ser compartilhados entre o Microsoft Edge e o Internet Explorer.

Na primeira vez que uma guia do modo do Internet Explorer é criada em uma sessão do Microsoft Edge, todos os cookies correspondentes são compartilhados com a sessão do Internet Explorer. Depois disso, sempre que um cookie que corresponde a uma regra é adicionado, excluído ou modificado, ele é enviado como uma atualização para a sessão do Internet Explorer. O conjunto de cookies compartilhados também é reavaliado quando a lista de sites é atualizada.

### <a name="updated-schema-elements"></a>Elementos do esquema atualizados

A tabela a seguir descreve o elemento \<shared-cookie\> adicionado para oferecer suporte ao recurso de compartilhamento de cookies.

| Elemento| Descrição |
|-|-|
| \<shared-cookie **domain**=".contoso.com" **name**="cookie1"\>\</shared-cookie\><br><br>OU<br><br>\<shared-cookie **host**="subdomain.contoso.com" **name**="cookie2"\>\</shared-cookie\>   |** (Obrigatório) ** Um elemento \<shared-cookie\> requer, no mínimo, um atributo de * domínio * (para os cookies de domínio) ou um * host * (para os cookies somente de host) e um atributo *nome*.<br>Esses atributos devem ser correspondências exatas com o domínio e o nome do cookie, respectivamente. **Observe** que os subdomínios não correspondem.<br><br>O atributo *domínio* é usado para cookies de domínio (e um ponto inicial é permitido, mas opcional).<br>O atributo * host * é usado para cookies somente de host (e um entrelinhamento é um erro). Especificar que nenhum ou ambos resultará em erro.<br>* Um cookie é um cookie de domínio se um domínio foi especificado na cadeia de caracteres do cookie (via cabeçalho de resposta HTTP Set-Cookie ou document.cookie JS API). Um cookie de domínio se aplica ao domínio especificado e a todos os subdomínios. Se um domínio não tiver sido especificado na cadeia de caracteres de cookie, o cookie será um cookie somente de host e se aplicará apenas ao host específico para o qual ele foi definido. Algumas classes de URLs, como nomes de host de palavra única (por exemplo, http://intranetsite) e endereços IP (por exemplo, http://10.0.0.1) só podem definir cookies somente de host.    |
| \<shared-cookie **host**="subdomain.contoso.com" **name**="cookie2" **path**="/a/b/c"\>\</shared-cookie\>  | ** (Opcional) ** Um atributo * caminho * pode ser especificado. Se nenhum atributo de caminho for especificado (ou se o atributo de caminho estiver vazio), quaisquer cookies que correspondam a domínio/host e nome corresponderão à política, independentemente do caminho (regra de caractere curinga).<br><br>Se um caminho for especificado, ele deve ser uma correspondência exata.<br>Se um cookie corresponder a uma regra com um caminho, isso terá precedência sobre uma regra sem caminho. |
| \<shared-cookie **domain**=".contoso.com" **name**="cookie1" **source-engine**="MSEdge"\>\</shared-cookie\><br><br>OU<br><br>\<shared-cookie **domain**=".contoso.com" **name**="cookie1" **source-engine**="IE11"\>\</shared-cookie\><br><br>OU<br><br>\<shared-cookie **domain**=".contoso.com" **name**="cookie1" **source-engine**="Both"\>\</shared-cookie\> | **(Opcional)** O atributo de mecanismo de origem especifica como os cookies de sessão são compartilhados entre Microsoft Edge Internet Explorer. Onde:<br><br>- **MSEdge**. Compartilhe cookies de sessão do Microsoft Edge para o Internet Explorer.<br>- **IE11**.  Compartilhe cookies de sessão do Internet Explorer para Microsoft Edge.<br>- **Os dois.** Compartilhe cookies de sessão de e para Microsoft Edge Internet Explorer.<br>- **Padrão ou não especificado**. Os cookies de sessão serão compartilhados Microsoft Edge Internet Explorer. |

#### <a name="sharing-example"></a>Exemplo de compartilhamento

```xml
<site-list version="1"> 
<shared-cookie domain=".contoso.com" name="cookie1"></shared-cookie>  
<shared-cookie host="subdomain.contoso.com" name="cookie2" path="/a/b/c"> 
</shared-cookie> 
<shared-cookie host="subdomain.contoso.com" name="cookie3" source-engine="MSEdge"></shared-cookie> 
</site-list> 
```

## <a name="see-also"></a>Consulte também

- [Sobre o modo IE](./edge-ie-mode.md)
- [Informações de sites configuráveis](./edge-learnmore-configurable-sites-ie-mode.md)
- [Informações adicionais sobre o Modo Empresarial](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
