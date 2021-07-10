---
title: Usar políticas de grupo para gerenciar extensões do Microsoft Edge
ms.author: aspoddar
author: AndreaLBarr
manager: balajek
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Usar políticas de grupo para gerenciar extensões do Microsoft Edge na empresa
ms.openlocfilehash: dad239a448ec1f0ebef60c7072bfaad5c3baed57
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/09/2021
ms.locfileid: "11641367"
---
# <a name="use-group-policies-to-manage-microsoft-edge-extensions"></a>Usar políticas de grupo para gerenciar extensões do Microsoft Edge

Este artigo descreve as opções e as etapas para gerenciar extensões usando políticas de grupo. As opções de extensão pressupõem que você já tem o Microsoft Edge gerenciado para os usuários. Se você ainda não configurou Microsoft Edge para ser gerenciado para seus usuários, siga o link abaixo para fazer isso agora.

- [Gerenciar extensões do Microsoft Edge na empresa](/deployedge/microsoft-edge-manage-extensions)

> [!NOTE]
> Este artigo se aplica ao Microsoft Edge versão 77 ou posterior.

## <a name="block-extensions-based-on-their-permissions"></a>Bloquear extensões com base em suas permissões

Você pode controlar quais extensões os usuários podem instalar com base nas permissões usando a política [ExtensionSettings](/deployedge/microsoft-edge-policies#extensionsettings). Se uma extensão instalada precisar de uma permissão bloqueada, ela simplesmente não será executada. A extensão não é removida, apenas desabilitada.

> [!NOTE]
> A configuração de permissões bloqueadas só pode ser definida dentro da política de configurações de extensão.  

Use as etapas a seguir como um guia para bloquear uma extensão.

1. Abra o editor de gerenciamento de política de grupo, vá para **Modelos Administrativos > Microsoft Edge > Extensões**  e selecione **Definir configurações de gerenciamento de extensão**.
2. Habilite a política e insira as permissões que você deseja que sejam permitidas ou bloqueadas usando uma cadeia de caracteres JSON que é compactada. A próxima captura de tela mostra como bloquear uma extensão que usa a permissão "usb".

    :::image type="content" source="media/microsoft-edge-manage-extensions-policies/manage-extensions-gp-block-1.png" alt-text="Configurar a política de grupo para bloquear uma extensão.":::

O exemplo a seguir mostra o JSON para bloquear qualquer extensão que precise do uso da permissão "usb" e sua cadeia de caracteres compactada.

### <a name="json-example"></a>Exemplo de JSON:

   ```json
   { 
        "*": { 
             "blocked_permissions": ["usb"] 
        } 
   } 
   ```

   ```json
   {"*":{"blocked_permissions":["usb"]}} 
   ```

   > [!NOTE]
   > Para bloquear todas as extensões que usam a permissão, use um asterisco para a ID de extensão, conforme mostrado no exemplo anterior. Se você especificar uma ID de extensão, a política se aplicará somente a essa extensão. Você pode bloquear mais de uma, mas elas precisam ser entradas separadas.

## <a name="prevent-extensions-from-altering-web-pages"></a>Impedir que extensões alterem páginas da Web

Essa configuração impede que as extensões leiam e alterem dados de sites e domínios confidenciais. O bloqueio de ações indesejadas é feito bloqueando ações como injeção de script em seus sites, leitura dos cookies ou modificações de solicitação da Web. Essa configuração não impede que os usuários instalem ou removam extensões, ela só impede que as extensões alterem os sites especificados. 
  
> [!NOTE]
> A configuração de hosts permitido ou /bloqueados de Runtime só pode ser definida dentro da política de configurações de extensão.  

Você pode definir as seguintes configurações na política ExtensionSettings para evitar (ou permitir) alterações de sites ou domínios:

- **Runtime_blocked_hosts**. Essa configuração impede que as extensões façam alterações ou leia dados dos sites que você especificar.
- **Runtime_allowed_hosts**. Essa configuração permite que as extensões façam alterações ou leiam dados dos sites que você especificar. O seguinte formato é usado para especificar seus sites na cadeia de caracteres JSON na política:

  ```json
  [http|https|ftp|*]://[subdomain|*].[hostname|*].[eTLD|*] [http|https|ftp|*],
  ```

  > [!NOTE]
  > `[hostname|*], and [eTLD|*]` as seções são necessárias, mas a seção `[subdomain|*]` é opcional.

A tabela a seguir mostra exemplos de padrões de host válidos e padrões correspondentes.

|Padrões de host válidos|Correspondências|Não corresponde|
|--|--|--|
|  `*://*.example.*` | `http://example.com`<br>`https://test.example.co.uk`   | `https://example.microsoft.com`<br>`http://example.microsoft.co.uk`  |
| `http://example.*` | `http://example.com`<br>`http://example.ly` | `https://example.com`<br>`http://test.example.com`   |
| `http://example.com`   | `http://example.com` | `https://example.com`<br>`http://test.example.co.uk` |
| `*://*`   | Todas as URLs  |   |

Use as etapas a seguir como um guia para bloquear ou permitir que extensões acessem um site ou domínio.

1. Abra o editor de gerenciamento de política de grupo, vá para **Modelos Administrativos > Microsoft Edge > Extensões**e selecione **Definir configurações de gerenciamento de extensão**.  
2. Habilite a política e insira as permissões que você deseja permitir ou bloquear, compactando as permissões para uma única cadeia de caracteres JSON.

Os exemplos a seguir mostram como bloquear extensões em um nome de host e como bloquear extensões no mesmo domínio.

### <a name="json-example-to-block-hostname"></a>Exemplo de JSON para bloquear o nome do host

Este exemplo mostra o JSON e a cadeia de caracteres JSON compactada para impedir que qualquer extensão acesse o nome de host `www.microsoft.com`.

```json
{ 
    "*":{ 
            "runtime_blocked_hosts":["www.microsoft.com"] 
    } 
} 
```

```json
{"*":{"runtime_blocked_hosts":["www.microsoft.com"]}} 
```

> [!NOTE]
> Para impedir que todas as extensões acessem uma página da Web, use um asterisco para a ID de extensão, conforme mostrado no exemplo anterior.  Se você especificar uma ID de extensão em vez de um asterisco, a política só se aplicará a essa extensão. Você pode bloquear mais de uma extensão, mas elas precisam ser entradas separadas.

### <a name="json-example-to-block-extensions-on-same-domain"></a>Exemplo de JSON para bloquear extensões no mesmo domínio

Este exemplo mostra o JSON e a cadeia de caracteres JSON compactada para bloquear a execução de extensões específicas no mesmo domínio, "importantwebsite".

```json
{ 
    "aapbdbdomjkkjkaonfhkkikfgjllcleb": { 
        "runtime_blocked_hosts": ["*://*.importantwebsite"] 
    }, 
    "bfbmjmiodbnnpllbbbfblcplfjjepjdn": { 
        "runtime_blocked_hosts": ["*://*.importantwebsite"] 
    } 
} 
```

```json
{"aapbdbdomjkkjkaonfhkkikfgjllcleb": {"runtime_blocked_hosts": ["*://,*.importantwebsite"]},"bfbmjmiodbnnpllbbbfblcplfjjepjdn": {"runtime_blocked_hosts": ["*://*.importantwebsite"]}} 
```

## <a name="allow-or-block-extensions-in-group-policy"></a>Permitir ou bloquear extensões na política de grupo

Você pode usar as políticas [ExtensionInstallBlocklist](/DeployEdge/microsoft-edge-policies#extensioninstallblocklist) e [ExtensionInstallAllowlist](/DeployEdge/microsoft-edge-policies#extensioninstallallowlist) para controlar quais extensões são bloqueadas ou permitidas. Use as etapas a seguir como um guia para permitir todas as extensões, exceto aquelas que você deseja bloquear.

1. Abra o editor de gerenciamento de política de grupo, vá para **Modelos Administrativos > Microsoft Edge > Extensões >** e selecione **Controlar quais extensões não podem ser instaladas**.
2. Selecione **Habilitado**.
3. Clique em **Mostrar**.
4. Insira a ID do aplicativo das extensões que você deseja bloquear. Ao adicionar várias IDs de aplicativo, use uma linha separada para cada ID.
5. Para bloquear todas as extensões, digite * _ na política para impedir que qualquer *\** extensão seja instalada. Você pode usar isso em conjunto com a política "Permitir que extensões específicas sejam instaladas" para permitir que apenas determinadas extensões sejam instaladas. A próxima captura de tela mostra uma extensão que será bloqueada com base na ID do aplicativo fornecida.

   :::image type="content" source="media/microsoft-edge-manage-extensions-policies/manage-extensions-gp-block-2.png" alt-text="Use a ID do aplicativo para bloquear uma extensão.":::

   > [!TIP]
   > Se você não encontrar a ID do aplicativo de uma extensão, examine a extensão Site de complementos do Microsoft Edge. Localize a extensão específica e você verá a ID do aplicativo no final da URL na omnibox.

> [!NOTE]
> Você pode adicionar uma extensão à lista de bloqueios que já está instalada no computador de um usuário. Isso desabilitará a extensão e impedirá que o usuário a habilite novamente. Ele não será desinstalado, apenas desabilitado.

## <a name="force-install-an-extension"></a>Forçar a instalação de uma extensão

Use a política [ExtensionInstallForcelist](/DeployEdge/microsoft-edge-policies#extensioninstallforcelist) para controlar quais extensões são bloqueadas ou permitidas. Use as etapas a seguir como um guia para forçar a instalação de uma extensão.

1. No Editor de Política de Grupo, vá para _*Modelos Administrativos> Microsoft Edge > Extensões >** e selecione Controlar quais extensões são **instaladas silenciosamente**.
2. Selecione **Habilitado**.  
3. Clique em **Mostrar**.
4. Insira a ID do aplicativo ou as IDs da extensão ou das extensões que você deseja forçar a instalação.  

A extensão será instalada silenciosamente sem a necessidade de interação do usuário. O usuário também não poderá desinstalar ou desabilitar a extensão. Essa configuração substituirá qualquer política de lista de bloqueio habilitada.

> [!NOTE]
> Para extensões hospedadas na Loja Da Web do Chrome, use uma cadeia de caracteres como: `pckdojakecnhhplcgfflhndiffaohfah;https://clients2.google.com/service/update2/crx`.

## <a name="block-extensions-from-a-specific-store-or-update-url"></a>Bloquear extensões de um repositório ou URL de atualização específico

Para bloquear extensões de um repositório ou URL específico, você só precisa bloquear o *update_url* para esse repositório usando a política [ExtensionSettings](/deployedge/microsoft-edge-policies#extensionsettings).

Use as etapas a seguir como um guia para bloquear extensões de um repositório ou URL específico.

1. Abra o editor de gerenciamento de política de grupo, vá para **Modelos Administrativos > Microsoft Edge > Extensões >** e selecione **Definir configurações de gerenciamento de extensão**.  
2. Habilite a política e insira as permissões que você deseja permitir ou bloquear, compactando-a em uma única cadeia de caracteres JSON.

O exemplo a seguir mostra o JSON e a cadeia de caracteres JSON compactada a serem bloqueados do Chrome Web Store usando sua URL de atualização (`https://clients2.google.com/service/update2/crx`).

### <a name="json-example-for-blocking-on-update-url"></a>Exemplo de JSON para bloqueio na URL de atualização

```json
{ 
"update_url:https://clients2.google.com/service/update2/crx":{ 
                                                             " installation_mode":"blocked" 
                                                             } 
} 
```

```json
{"update_url:https://clients2.google.com/service/update2/crx":{"installation_mode":"blocked"}} 
```

> [!NOTE]
> Observe que você ainda pode usar **ExtensionInstallForcelist** e **ExtensionInstallAllowlist** para permitir ou forçar a instalação de extensões específicas, mesmo se o armazenamento estiver bloqueado usando o JSON no exemplo anterior.

## <a name="see-also"></a>Veja também

- [Gerenciar extensões do Microsoft Edge na empresa](microsoft-edge-manage-extensions.md)
- [Criar um repositório para hospedar extensões do Microsoft Edge](microsoft-edge-manage-extensions-webstore.md)
- [Guia de referência para a política ExtensionSettings](microsoft-edge-manage-extensions-ref-guide.md)
- [Perguntas frequentes sobre extensões do Microsoft Edge](microsoft-edge-manage-extensions-faq.md)
- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
