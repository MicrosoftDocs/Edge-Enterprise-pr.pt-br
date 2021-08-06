---
title: Estratégia de configuração de site de empresa
ms.author: shisub
author: shisub
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Um guia passo a passo para configurar a lista de Sites do Modo Empresa para o modo Internet Explorer.
ms.openlocfilehash: ec0d1364f3db00bc78e29bab8abbfcf1748f68494791fd5288a435a8b1230018
ms.sourcegitcommit: d44c0997ffe40d67421312ed96e7766da947eaa0
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/05/2021
ms.locfileid: "11724414"
---
# <a name="enterprise-site-configuration-strategy"></a>Estratégia de configuração de site de empresa

>[!Note]
> O aplicativo de área de trabalho Internet Explorer 11 será desativado e ficará sem suporte em 15 de junho de 2022 (para obter uma lista do que está no escopo, [consulte as Perguntas frequentes](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/internet-explorer-11-desktop-app-retirement-faq/ba-p/2366549)). Os mesmos aplicativos e sites do IE11 que você usa hoje podem abrir no Microsoft Edge com o modo Internet Explorer. [Saiba mais aqui](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/).

Este artigo descreve as alterações na Lista de Sites do Modo Empresa para dar suporte ao modo Internet Explorer para o Microsoft Edge versão 77 e posterior.

Para obter mais informações sobre o esquema do arquivo XML da Lista de Sites do Modo Empresa, confira as [orientações do esquema do Modo Empresarial v.2](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance).

> [!NOTE]
> Este artigo se aplica ao Microsoft Edge versão 77 ou posterior.
<!--
## Updated schema elements

The following table describes the \<open-in app\> element added to the v.2 of the Enterprise Mode schema:

| **Element** | **Description** |
| --- | --- |
| \<open-in app="**true**"\> | A child element that controls what browser is used for sites. This element is required for sites that need to **open in IE11**.|

**Example:**

``` xml
<site url="contoso.com">

  <open-in app="true">IE11</open-in>

</site>
```

The following table shows the possible values of the \<open-in\> element:

| **Value** | **Description** |
| --- | --- |
| **\<open-in\>IE11\</open-in\>** | Opens the site in IE mode or a full IE11 window. To enable IE mode, see [Configure IE mode policies](./edge-ie-mode-policies.md)|
| **\<open-in app="**true**"\>IE11\</open-in\>** | Opens the site in a full IE11 window |
| **\<open-in\>MSEdge\</open-in\>** | Opens the site in Microsoft Edge |
| **\<open-in\>None or not specified\</open-in\>** | Opens the site in the default browser or in the browser where the user navigated to the site. |
|**\<open-in\>Configurable\</open-in\>** | Allows the site to participate in IE mode engine determination. To learn more, see [Learn about Configurable sites in IE mode](edge-learnmore-configurable-sites-ie-mode.md).  |

>[!NOTE]
> The attribute app=**"true"** is only recognized when associated to _'open-in' IE11_. Adding it to the other 'open-in' elements won't change browser behavior.   -->

## <a name="configuration-strategy"></a>Estratégia de configuração

As etapas a seguir fazem parte de uma estratégia de configuração de site para o modo IE:
1. Preparar sua lista de sites
2. Configurar sites neutros
3. (Opcional) Usar o compartilhamento de cookies, se necessário

<!--
Step 1.  – if you don’t have one use Site Discovery Step-by-Step
Step 2 – Neutral sites + sticky mode
        Use more examples and explain sticky mode better
Step 3 – If that doesn’t cover your needs, then use Cookie sharing -->

## <a name="prepare-your-site-list"></a>Preparar sua lista de sites

Se você já tiver uma lista de sites do Modo Empresa para o IE11 ou a Versão Prévia do Microsoft Edge, poderá reutilizar para configurar o modo IE.

No entanto, se você não tiver uma lista de sites, poderá usar a [ferramenta de descoberta de sites de empresa](/deployedge/edge-ie-mode-site-discovery) para preencher sua lista de sites.

## <a name="configure-neutral-sites"></a>Configurar sites neutros

Para que o modo IE funcione corretamente, os servidores de autenticação/logon único (SSO) precisam ser configurados explicitamente como sites neutros. Caso contrário, as páginas do modo IE tentarão redirecionar para o Microsoft Edge e a autenticação falhará.

Um site neutro usará o navegador onde a navegação começou - no modo Microsoft Edge ou IE. A configuração de sites neutros garante que todos os aplicativos que usam esses servidores de autenticação, modernos e herdados, continuem funcionando.

Para configurar sites neutros, configure o menu suspenso *Open In* como “Nenhum” na ferramenta Enterprise Mode Site List Manager ou atualizando diretamente o XML da lista de sites:

``` xml
<site url="login.contoso.com">
   
    <open-in>None</open-in>

</site>
```

Para identificar servidores de autenticação, inspecione o tráfego de rede de um aplicativo usando as Ferramentas de Desenvolvedor do IE11. Se precisar de mais tempo para identificar seus servidores de autenticação, você pode configurar uma política para manter todas as navegações in-page no modo IE para permitir que seus usuários continuem seus fluxos de trabalho sem interrupções. Para minimizar o uso do modo IE quando desnecessário, desabilite essa configuração depois de identificar e adicionar seus servidores de autenticação à lista de sites. Para obter mais informações, confira [Manter a navegação na página no modo IE](/deployedge/edge-learnmore-inpage-nav).

>[!NOTE]
   >O esquema v.1 do modo empresa não é compatível com a integração do modo IE. Se você estiver usando o esquema v.1 atualmente com o Internet Explorer 11, deverá atualizar para o esquema v.2. Para obter mais informações, confira [Diretrizes sobre o esquema v.2 do Modo Empresa](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance).

## <a name="optional-use-cookie-sharing-if-necessary"></a>(Opcional) Usar o compartilhamento de cookies, se necessário

Por padrão, os processos do Microsoft Edge e do Internet Explorer não compartilham cookies de sessão e essa falta de compartilhamento pode ser inconveniente em alguns casos ao usar o modo IE. Por exemplo, quando um usuário precisa se autenticar novamente no modo IE quando anteriormente estava acostumado a fazê-lo ou ao sair de uma sessão do Microsoft Edge, não saia da sessão do modo Internet Explorer para transações críticas. Nesses cenários, você pode configurar cookies específicos definidos pelo SSO para serem enviados do Microsoft Edge para o Internet Explorer para que a experiência de autenticação se torne mais contínua, eliminando a necessidade de reautenticação. Para obter mais informações, confira[Compartilhamento de cookies do Microsoft Edge para o Internet Explorer](/deployedge/edge-ie-mode-add-guidance-cookieshare).

## <a name="see-also"></a>Confira também

- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Sobre o modo IE](./edge-ie-mode.md)
- [Informações adicionais sobre o Modo Empresarial](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
