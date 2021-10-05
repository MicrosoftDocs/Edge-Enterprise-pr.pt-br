---
title: Guia detalhado para a política ExtensionSettings
ms.author: aspoddar
author: dan-wesley
manager: balajek
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Um guia de referência detalhado para configurar extensões do Microsoft Edge usando a política ExtensionSettings.
ms.openlocfilehash: 7dceff78172626d70863883e0762be2f4cb7e51c
ms.sourcegitcommit: e825c6a1b0e63004288e13f6bb672743b0ecfafb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/05/2021
ms.locfileid: "12069007"
---
# <a name="detailed-guide-to-the-extensionsettings-policy"></a>Guia detalhado para a política ExtensionSettings

Microsoft Edge oferece várias maneiras de gerenciar extensões. Uma maneira comum é definir várias políticas em um só lugar com uma cadeia de caracteres JSON no Editor de Política de Grupo do Windows ou no Registro do Windows usando a política [ExtensionSettings](/deployedge/microsoft-edge-policies#extensionsettings).

> [!NOTE]
> Este artigo se aplica ao Microsoft Edge versão 77 ou posterior.

## <a name="before-you-begin"></a>Antes de começar

Você decide se deseja definir todas as configurações de gerenciamento de extensão aqui ou definir esses controles por meio de outras políticas.
  
A política ExtensionSettings pode substituir outras políticas que você definiu em outro lugar na política de grupo, incluindo as seguintes políticas:

- [ExtensionAllowedTypes](/DeployEdge/microsoft-edge-policies#extensionallowedtypes)
- [ExtensionInstallBlocklist](/DeployEdge/microsoft-edge-policies#extensioninstallblocklist)
- [ExtensionInstallForcelist](/DeployEdge/microsoft-edge-policies#extensioninstallforcelist)
- [ExtensionInstallSources](/DeployEdge/microsoft-edge-policies#extensioninstallsources)
- [ExtensionInstallAllowlist](/DeployEdge/microsoft-edge-policies#extensioninstallsources)

## <a name="extensionsettings-policy-fields"></a>Campos de política de ExtensionSettings

Essa política pode controlar configurações como URL de atualização, de onde a extensão será baixada para instalação inicial, e permissões bloqueadas ou quais permissões não têm permissão para executar. Os campos de política disponíveis são descritos na tabela a seguir.

| &nbsp; | Descrição |
|--|--|
| **allowed_types** | Só pode ser usado para configurar a configuração padrão, *. Especifica quais tipos de usuários de aplicativo ou extensão têm permissão para instalar no Microsoft Edge. O valor é uma lista de cadeias de caracteres, cada uma delas deve ser uma das seguintes: "extension", "theme", "user_script" e "hosted_app".   |
| **blocked_install_message**| Se você impedir que os usuários instalem determinadas extensões, poderá especificar uma mensagem personalizada a ser exibida no navegador se os usuários tentarem instalá-las.<br>Acrescente texto à mensagem de erro genérica que é exibida no site de complementos do Microsoft Edge. Por exemplo, você pode dizer aos usuários como entrar em contato com o departamento de TI ou por que uma extensão específica não está disponível. A mensagem pode ter até 1.000 caracteres.   |
|**blocked_permissions**  | Impede que os usuários instalem e executem extensões que solicitam determinadas permissões de API que sua organização não permite. Por exemplo, você pode bloquear extensões que acessam cookies. Se uma extensão exigir uma permissão que você bloqueou, o usuário não poderá instalá-la. Se os usuários instalaram a extensão anteriormente, ela não será mais carregada. Se uma extensão contiver uma permissão bloqueada como um requisito opcional, ela será instalada como de costume. Em seguida, enquanto a extensão está em execução, as permissões bloqueadas são recusadas automaticamente.<br>Para obter uma lista de permissões disponíveis, consulte [declarar permissões](/microsoft-edge/extensions-chromium/enterprise/declare-permissions).   |
| **installation_mode**| Controla se e como as extensões especificadas são adicionadas ao Microsoft Edge. Você pode definir o modo de instalação para uma das seguintes opções:<br>- permitido: Usuários podem instalar a extensão. Se nenhum modo de instalação for definido, essa configuração será o padrão.<br>- bloqueado: Usuários não podem instalar a extensão.<br>- force_installed: Instala automaticamente a extensão sem interação do usuário. Usuários não podem removê-la. Você também precisa definir o local de download da extensão usando update_url. **Observação**: Você não pode usar essa configuração com * porque o Microsoft Edge não saberá qual extensão instalar automaticamente.<br>- normal_installed: Instala automaticamente a extensão sem interação do usuário. Usuários podem desabilitá-la. Você também precisa definir o local de download da extensão usando update_url. **Observação**: Você não pode usar essa configuração com * porque o Microsoft Edge não saberá qual extensão instalar automaticamente.<br>- removido: Usuários não podem instalar a extensão. Se os usuários instalaram a extensão anteriormente, o Microsoft Edge a remove. |  |
| **install_sources** | Pode ser usado somente para configurar a configuração padrão, *. Especifica quais URLs têm permissão para instalar extensões. O local do arquivo *.crx e a página em que o download é iniciado (o referenciador) devem ser permitidos por esses padrões. Para obter exemplos de padrão de URL, consulte [padrões de correspondência](/microsoft-edge/extensions-chromium/enterprise/match-patterns).  |
| **minimum_version_required** |Microsoft Edge desabilita extensões, incluindo extensões instaladas à força, com uma versão anterior à versão mínima especificada.<br>O formato da cadeia de caracteres de versão é o mesmo usado no manifesto da extensão.     |
| **update_url** | Aplica-se somente a force_installed e normal_installed. Especifica de onde Microsoft Edge deve baixar uma extensão. Se a extensão estiver hospedada no site de Complementos do Microsoft Edge, use este local: `https://edge.microsoft.com/extensionwebstorebase/v1/crx`.<br>Microsoft Edge usa a URL que você especifica para a instalação inicial da extensão. Para atualizações de extensão subsequentes, o Microsoft Edge usa a URL no manifesto da extensão.   |
| **runtime_allowed_hosts**| Permite que as extensões interajam com sites especificados, mesmo que também estejam definidas em runtime_blocked_hosts. Você pode especificar até 100 entradas. Entradas extras são descartadas.<br>O formato de padrão de host é semelhante a  [padrões de correspondência](/microsoft-edge/extensions-chromium/enterprise/match-patterns) ,contudo você não pode definir o caminho. Por exemplo:<br>- *://*.example.com<br>- *://exemplo.*— há suporte para curingas eTLD     |
| **runtime_blocked_hosts**| Impede que as extensões interajam ou modifiquem sites que você especificar. As modificações incluem bloqueio de injeção de JavaScript, acesso a cookie e modificações de solicitação da Web.<br>Você pode especificar até 100 entradas. Entradas extras são descartadas.<br>O formato de padrão do host é semelhante aos padrões de correspondência, contudo você não pode definir o caminho. Por exemplo:<br>- *://*.example.com<br>- *://exemplo.*— há suporte para curingas eTLD   |
| **override_update_url**| Disponível na Borda 93<br>Se estiver definido como , Edge usará a URL de atualização especificada na política ExtensionSettings ou na política `true` ExtensionInstallForcelist, para atualizações de extensão subsequentes.<br>Se isso não estiver definido ou estiver definido como , Edge usará a URL especificada no manifesto da `false` extensão para atualizações.|
| **toolbar_state**| Disponível na Borda 94<br>Essa configuração de política permite que você force a exibição de uma extensão instalada na barra de ferramentas. O estado padrão é `default_shown` para todas as extensões. Os estados a seguir são possíveis para essa configuração<br>-`force_shown`: Você pode optar por forçar a exibição de uma extensão instalada na barra de ferramentas. Os usuários não poderão ocultar o ícone de extensão específico da barra de ferramentas.<br>-`default_hidden`: Nesse estado, as extensões ficam ocultas da barra de ferramentas na instalação. Os usuários podem mostrar na barra de ferramentas, se necessário.<br>-`default_shown`: Esta é a configuração de surdez de todas as extensões instaladas no navegador.

Estas são as chaves permitidas no escopo global (*): 

- blocked_permissions
- installation_mode - somente `"blocked"` , ou são os valores `"allowed"` `"removed"` válidos neste escopo.
- runtime_blocked_hosts
- blocked_install_message
- allowed_types
- runtime_allowed_hosts
- install_sources

Estas são as chaves permitidas em um escopo de extensão individual: 

- blocked_permissions
- minimum_version_required
- blocked_install_message
- installation_mode - `"blocked"` , `"allowed"` , , e são os `"removed"` `"force_installed"` valores `"normal_installed"` possíveis.
- runtime_allowed_hosts
- update_url
- override_update_url
- runtime_blocked_hosts
- toolbar_state

Estas são as chaves permitidas em um escopo de URL de atualização: 

- blocked_permissions
- installation_mode - somente `"blocked"` , ou são os valores `"allowed"` `"removed"` válidos neste escopo.

## <a name="configure-using-a-json-string-in-windows-group-policy-editor"></a>Configurar usando uma cadeia de caracteres JSON no Editor de Política de Grupo do Windows

As etapas para usar a política de configurações de extensão usando GPO pressupõem que você já importou o ADM/ADMX para Políticas do Microsoft Edge.

1. Abra o editor de política de grupo e vá para **Microsoft Edge > Extensões > Configurar política de configuração de gerenciamento de extensão**.
2. Habilite a política e insira seus dados JavaScript Object Notation (JSON) compactos na caixa de texto como uma única linha sem quebras de linha.
3. Para validar a política e compactá-la em uma única linha, use uma ferramenta de compactação JSON.

### <a name="properly-format-json-for-the-extension-settings-policy"></a>Formatar corretamente o JSON para a política de configurações de extensão

Você precisa entender as duas partes dessa política: o escopo padrão e o escopo individual. O escopo padrão é genérico para extensões sem seu próprio escopo. O escopo individual é aplicado somente a essa extensão.  

O escopo padrão é identificado pelo asterisco (*). O exemplo a seguir define um escopo padrão e um escopo de extensão individual.

```json
{ 
   “*”: {}, 
   “nckgahadagoaajjgafhacjanaoiihapd”: {} 
} 
```

Uma extensão só obterá suas configurações de um escopo. Se houver um escopo de extensão individual para essa extensão, essas serão as configurações que se aplicam a essa extensão. Se nenhum escopo de extensão individual existir, a extensão usará o escopo padrão.  

O próximo exemplo de JSON impede que qualquer extensão seja executada em `.example.com` e bloqueia qualquer extensão que exija a permissão "USB".

```json
{ 
  "*": { 
    "runtime_blocked_hosts": ["*://*.example.com"], 
    "blocked_permissions": ["usb"] 
  } 
} 
```

**JSON compacto**

```json
{"*":{"runtime_blocked_hosts":["*://*.example.com"],"blocked_permissions":["usb"]}} 
```

### <a name="a-few-more-json-examples-for-extension-settings"></a>Mais alguns exemplos de JSON para configurações de extensão

#### <a name="using-installation_mode-property-to-allow-and-block-extensions"></a>Usando installation_mode para permitir e bloquear extensões

- O usuário pode instalar todas as extensões – essa é a configuração padrão 

  `{ "*": {"installation_mode": "allowed" }}`
- O usuário não pode instalar nenhuma extensão.  

  `{ "*": {"installation_mode": "blocked" }}`

- Especifique uma mensagem personalizada a ser exibida quando a instalação for bloqueada.

   `{"*": {"blocked_install_message": ["Call IT(408 - 555 - 1234) for an exception"]}}`

#### <a name="using-installation_mode-property-to-force-install-extensions"></a>Usando a propriedade installation_mode para forçar a instalação de extensões

Ao usar installation_mode como "force_installed", a extensão é instalada automaticamente sem interação do usuário. Um usuário não pode desabilitar ou remover a extensão. Se uma extensão for instalada "normal" ou "force", o campo **update_url** também deverá ser definido. Esse campo aponta para o local do qual a extensão pode ser instalada. Use os seguintes locais para o campo **update_url**:

- Se a extensão que você está baixando estiver hospedada no repositório de complementos do Microsoft Edge, use [https://edge.microsoft.com/extensionwebstorebase/v1/crx](https://edge.microsoft.com/extensionwebstorebase/v1/crx).
- Se a extensão que você está baixando estiver hospedada no Chrome Web Store, use [https://clients2.google.com/service/update2/crx](https://clients2.google.com/service/update2/crx).
- Se você estiver hospedando a extensão em seu próprio servidor, use a URL na qual Microsoft Edge pode baixar a extensão compactada (arquivo .crx). Exemplo de JSON:

   `{"nckgahadagoaajjgafhacjanaoiihapd": {"installation_mode": "force_installed","update_url": "https://edge.microsoft.com/extensionwebstorebase/v1/crx"}}`
  
No exemplo acima, em vez de "force_installed", se você usar "normal_installed", a extensão será instalada automaticamente sem interação do usuário, mas ele poderá desabilitar a extensão.  

   > [!TIP]
   > A formatação correta de uma cadeia de caracteres JSON pode ser complicada. Use um verificador JSON antes de implementar a política. Ou experimente a versão inicial da [ Ferramenta Gerador de Configurações de Extensão](https://microsoft.github.io/edge-extension-settings-generator/minimal)

## <a name="configure-using-the-windows-registry"></a>Configurar usando o Registro do Windows

A política ExtensionSettings deve ser gravada no Registro sob esta chave:

`HKLM\Software\Policies\Microsoft\Edge\`

> [!NOTE]
> É possível usar HKCU em vez de HKLM. O caminho equivalente pode ser configurado com Objeto de Política de Grupo (GPO).  

Para o Microsoft Edge, todas as configurações serão iniciadas sob esta chave:

`HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Edge\`

A próxima chave que você criará é a ID de Extensão para escopo individual ou um asterisco (*) para o Escopo Padrão. Por exemplo, você usaria o seguinte local para configurações que se aplicam ao Google Hangouts:

`HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Edge\ExtensionSettings\nckgahadagoaajjgafhacjanaoiihapd`

Para configurações que se aplicam ao Escopo Padrão, use este local:

`HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Edge\ExtensionSettings\*`

Configurações diferentes exigirão formatos diferentes, dependendo se são uma cadeia de caracteres ou uma matriz de cadeias de caracteres. Valores de matriz exigem [＂value＂]. Valores de cadeia de caracteres podem ser inseridos como estão. A lista a seguir mostra quais configurações são matrizes ou cadeias de caracteres:

- Installation_mode = Cadeia de caracteres
- update_url = Cadeia de caracteres
- blocked_permissions = Matriz de cadeias de caracteres
- allowed_permissions = Matriz de cadeias de caracteres
- minimum_version_required = Cadeia de caracteres
- runtime_blocked_hosts = Matriz de cadeias de caracteres
- runtime_allowed_hosts = Matriz de cadeias de caracteres
- blocked_install_message = Cadeia de caracteres


## <a name="see-also"></a>Veja também

- [Gerenciar extensões do Microsoft Edge na empresa](microsoft-edge-manage-extensions.md)
- [Usar políticas de grupo para gerenciar extensões do Microsoft Edge](microsoft-edge-manage-extensions-policies.md)
- [Perguntas frequentes sobre extensões do Microsoft Edge](microsoft-edge-manage-extensions-faq.md)
- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
