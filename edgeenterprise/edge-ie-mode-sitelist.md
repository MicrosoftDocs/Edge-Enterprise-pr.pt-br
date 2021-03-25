---
title: Configurar sites na lista de sites do modo empresarial
ms.author: cjacks
author: cjacks
manager: saudm
ms.date: 05/28/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Configurar Lista de Sites Empresariais
ms.openlocfilehash: 9b1943e4d50dcc770b4a634b99ecbd001d1ffbcc
ms.sourcegitcommit: f363ceb6c42054fabc95ce8d7bca3c52d80e6a9f
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/24/2021
ms.locfileid: "11447645"
---
# <a name="configure-sites-on-the-enterprise-mode-site-list"></a>Configurar sites na lista de sites do modo empresarial

Este artigo descreve alterações na Lista de Sites do Modo Empresarial que oferecem suporte à configuração do modo IE para Microsoft Edge versão 77 e posterior.

Para obter mais informações sobre o esquema do arquivo XML da Lista de Sites do Modo Empresarial, consulte as [orientações do esquema do Modo Empresarial v.2](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance).

> [!NOTE]
> Este artigo se aplica aos Canais **Estável**, **Beta** e **Dev** do Microsoft Edge Beta, versão 77 ou posteriores.

## <a name="updated-schema-elements"></a>Elementos do esquema atualizados

A tabela a seguir descreve o elemento \<open-in app\> adicionado ao esquema v.2 do esquema Modo Empresarial:

| **Elemento** | **Descrição** |
| --- | --- |
| \<open-in app="**true**"\> | Um elemento filho que controla qual navegador é usado para sites. Esse elemento é obrigatório para sites que precisam ser **abertos no IE11**.|

**Exemplo:**

``` xml
<site url="contoso.com">

  <open-in app="true">IE11</open-in>

</site>
```

A tabela a seguir mostra os valores possíveis do elemento\<open-in\>:

| **Valor** | **Descrição** |
| --- | --- |
| **\<open-in\>IE11\</open-in\>** | Abre o site no modo IE ou em uma janela completa do IE11. Para ativar o modo IE, confira [Configurar políticas do modo IE](./edge-ie-mode-policies.md)|
| **\<open-in app="**true**"\>IE11\</open-in\>** | Abre o site em uma janela completa do IE11 |
| **\<open-in\>MSEdge\</open-in\>** | Abre o site no Microsoft Edge |
| **\<open-in\>Nenhum ou não especificado.\</open-in\>** | Abre o site no navegador padrão ou no navegador em que o usuário navegou até o site. |
|**\<open-in\>Configurável\</open-in\>** | Permite ao site participar da determinação do mecanismo do IE. Para saber mais, confira [Saber mais sobre sites Configuráveis no modo IE](edge-learnmore-configurable-sites-ie-mode.md).  |

>[!NOTE]
> O atributo app =**"true"** é reconhecido somente quando associado a _'open-in' IE11_. Adicioná-lo aos outros elementos 'open-in' não mudará o comportamento do navegador.   

## <a name="configure-neutral-sites"></a>Configurar sites neutros

Para que o modo IE funcione corretamente, os servidores de autenticação/Logon Único precisarão ser explicitamente configurados como sites neutros. Caso contrário, as páginas do modo IE tentarão redirecionar para o Microsoft Edge e a autenticação falhará.

Um site neutro usará o navegador onde a navegação começou - no modo Microsoft Edge ou IE. A configuração de sites neutros garante que todos os aplicativos que usam esses servidores de autenticação, modernos e herdados, continuem funcionando.

Para configurar sites neutros, configure o menu suspenso *Open In* como “Nenhum” na ferramenta Enterprise Mode Site List Manager ou atualizando diretamente o XML da lista de sites:

``` xml
<site url="login.contoso.com">
   
    <open-in>None</open-in>

</site>
```

Para identificar servidores de autenticação, inspecione o tráfego de rede de um aplicativo usando as Ferramentas de Desenvolvedor do IE11. Se você precisar de mais tempo para identificar seus servidores de autenticação, poderá configurar uma política para manter toda a navegação na página no modo IE. Para minimizar o uso do modo IE, desative essa configuração depois de identificar e adicionar seus servidores de autenticação à lista de sites. Para obter mais informações, confira [Configurar a navegação na página para permanecer no modo IE](./microsoft-edge-policies.md#internetexplorerintegrationsiteredirect).

>[!NOTE]
   >O esquema v.1 do Modo Empresarial não tem suporte na integração do modo IE. Se você estiver usando o esquema v.1 atualmente com o Internet Explorer 11, deverá atualizar para o esquema v.2. Para obter mais informações, consulte [Diretrizes sobre o esquema v.2 do Modo Empresarial](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance).

## <a name="see-also"></a>Consulte também

- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Sobre o modo IE](./edge-ie-mode.md)
- [Informações adicionais sobre o Modo Empresarial](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)