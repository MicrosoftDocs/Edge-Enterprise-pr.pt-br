---
title: Associar extensões de arquivo com o modo Internet Explorer
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Associar extensões de arquivo com o modo Internet Explorer
ms.openlocfilehash: 43d856a293c22d3fe115387a37c2677112a96049d5b2a2ad4c6f28cb1a56cb03
ms.sourcegitcommit: d44c0997ffe40d67421312ed96e7766da947eaa0
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/05/2021
ms.locfileid: "11724574"
---
# <a name="associate-file-extensions-with-internet-explorer-mode"></a>Associar extensões de arquivo ao modo Internet Explorer

>[!Note]
> O aplicativo de área de trabalho Internet Explorer 11 será desativado e ficará sem suporte em 15 de junho de 2022 (para obter uma lista do que está no escopo, [consulte as Perguntas frequentes](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/internet-explorer-11-desktop-app-retirement-faq/ba-p/2366549)). Os mesmos aplicativos e sites do IE11 que você usa hoje podem abrir no Microsoft Edge com o modo Internet Explorer. [Saiba mais aqui](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/).

Este artigo explica como associar o Microsoft Edge com o modo do Internet Explorer com extensões de arquivo para aplicativos da área de trabalho.

> [!NOTE]
> Este artigo se aplica ao Microsoft Edge versão 86 ou posterior.

## <a name="guidance-for-file-extension-association-with-internet-explorer-mode"></a>Diretrizes de associação de extensão de arquivo com o modo Internet Explorer

As instruções a seguir mostram uma entrada que associa o Microsoft Edge com o modo IE ao tipo de arquivo. mht. Use as etapas a seguir como um guia para definir uma associação de arquivo.

> [!NOTE]
> Você pode definir extensões de arquivo específicas para abrir no modo Internet Explorer por padrão usando a política para **Definir um arquivo de configuração de associações padrão**. Para obter mais informações, consulte [Política de CSP – ApplicationDefaults](/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration).

1. Defina um novo ProgID com o canal Microsoft Edge a ser usado para abrir com o modo Internet Explorer. O ProgID inclui o nome e o ícone do aplicativo e o caminho completo para msedge.exe.

```markdown
[HKEY_CURRENT_USER\SOFTWARE\Classes\MSEdgeIEModeMHT\Application]
"ApplicationCompany"="Microsoft Corporation"
"ApplicationName"="Microsoft Edge with IE Mode"
"ApplicationIcon"="C:\\<edge_installation_dir>\\msedge.exe,4"
"AppUserModelId"=""
```

```markdown
[HKEY_CURRENT_USER\SOFTWARE\Classes\MSEdgeIEModeMHT\DefaultIcon]
@="C:\\<edge_installation_dir>\\msedge.exe,4"
```

2. Configure as atualizações do shell para passar a linha de comando necessária para abrir com o modo IE.

```markdown
[HKEY_CURRENT_USER\SOFTWARE\Classes\MSEdgeIEModeMHT\shell\open\command]
@="\"C:\\<edge_installation_dir>\\msedge.exe\" -ie-mode-file-url -- \"%1\""
```

3. Por fim, associe a extensão de arquivo .mht a um novo ProgID. Adicione o ProgID como um nome de valor, com o tipo de valor de REG_SZ.

```markdown
[HKEY_CURRENT_USER\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\FileExts\.mht\OpenWithProgids]
"MSEdgeIEModeMHT"=hex(0):
```

Depois de definir as chaves descritas no exemplo anterior, os usuários verão uma opção adicional no menu **Abrir com** para abrir um arquivo .mht usando o Microsoft Edge \<channel\> com o modo IE.

## <a name="registry-example"></a>Exemplo de registro

Você pode salvar o trecho de código a seguir como um arquivo .reg e importá-lo para o registro.

```markdown
Windows Registry Editor Version 5.00

[HKEY_CURRENT_USER\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\FileExts\.mht\OpenWithProgids]
"MSEdgeIEModeMHT"=hex(0):

[HKEY_CURRENT_USER\SOFTWARE\Classes\MSEdgeIEModeMHT]

[HKEY_CURRENT_USER\SOFTWARE\Classes\MSEdgeIEModeMHT\Application]
"ApplicationCompany"="Microsoft Corporation"
"ApplicationName"="Microsoft Edge with IE Mode"
"ApplicationIcon"="C:\\<edge_installation_dir>\\msedge.exe,4"
"AppUserModelId"=""

[HKEY_CURRENT_USER\SOFTWARE\Classes\MSEdgeIEModeMHT\DefaultIcon]
@="C:\\<edge_installation_dir>\\msedge.exe,4"

[HKEY_CURRENT_USER\SOFTWARE\Classes\MSEdgeIEModeMHT\shell]

[HKEY_CURRENT_USER\SOFTWARE\Classes\MSEdgeIEModeMHT\shell\open]

[HKEY_CURRENT_USER\SOFTWARE\Classes\MSEdgeIEModeMHT\shell\open\command]
@="\"C:\\<edge_installation_dir>\\msedge.exe\" -ie-mode-file-url -- \"%1\""

```

## <a name="configuring-file-types-to-open-in-internet-explorer-mode"></a>Configurando tipos de arquivo para abrir no modo Internet Explorer

Ao iniciar o Microsoft Edge 88, você pode configurar links de tipos de arquivo específicos para abrir no modo do Internet Explorer usando a política [ Mostrar menu de contexto para abrir links no modo do Internet Explorer](./microsoft-edge-policies.md#internetexplorerintegrationreloadiniemodeallowed).

Você pode definir os tipos de arquivo aos quais essa opção deve ser aplicada, especificando as extensões de arquivo nesta política [Abrir arquivos locais na lista de permissões de extensão de arquivo no modo Internet Explorer](./microsoft-edge-policies.md#internetexplorerintegrationlocalfileextensionallowlist). 

## <a name="see-also"></a>Consulte também

- [Sobre o modo IE](./edge-ie-mode.md)
- [Informações de sites configuráveis](./edge-learnmore-configurable-sites-ie-mode.md)
- [Informações adicionais sobre o Modo Empresarial](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
- [Configurando associações de tipo de arquivo](/windows/win32/shell/fa-file-types)
- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)