---
title: Associar extensões de arquivo com o modo Internet Explorer
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 11/16/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Associar extensões de arquivo com o modo Internet Explorer
ms.openlocfilehash: c80732239b911f7cd3d615e9ce1e480db2749f17
ms.sourcegitcommit: fc0ac6bb6655d1f6e2de7c838f275779cd7a5de6
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/17/2020
ms.locfileid: "11175174"
---
# <span data-ttu-id="09adc-103">Associar extensões de arquivo com o modo Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="09adc-103">Associate file extensions with Internet Explorer mode</span></span>

<span data-ttu-id="09adc-104">Este artigo explica como associar o Microsoft Edge com o modo do Internet Explorer com extensões de arquivo para aplicativos da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="09adc-104">This article explains how to associate Microsoft Edge with Internet Explorer mode with file extensions for desktop applications.</span></span>

> [!NOTE]
> <span data-ttu-id="09adc-105">Este artigo se aplica ao Microsoft Edge versão 86 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="09adc-105">This article applies to Microsoft Edge version 86 or later.</span></span>

## <span data-ttu-id="09adc-106">Diretrizes de associação de extensão de arquivo com o modo Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="09adc-106">Guidance for file extension association with Internet Explorer mode</span></span>

<span data-ttu-id="09adc-107">As instruções a seguir mostram uma entrada que associa o Microsoft Edge com o modo IE ao tipo de arquivo. mht.</span><span class="sxs-lookup"><span data-stu-id="09adc-107">The following instructions show an entry that associates Microsoft Edge with IE mode with the .mht file type.</span></span> <span data-ttu-id="09adc-108">Use as etapas a seguir como um guia para definir uma associação de arquivo.</span><span class="sxs-lookup"><span data-stu-id="09adc-108">Use the following steps as a guide for setting a file association.</span></span>

> [!NOTE]
> <span data-ttu-id="09adc-109">Você pode definir extensões de arquivo específicas para abrir no modo Internet Explorer por padrão usando a política para **Definir um arquivo de configuração de associações padrão**.</span><span class="sxs-lookup"><span data-stu-id="09adc-109">You can set specific file extensions to open in Internet Explorer mode by default using the policy to **Set a default associations configuration file**.</span></span> <span data-ttu-id="09adc-110">Para obter mais informações, consulte [Política de CSP – ApplicationDefaults](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration).</span><span class="sxs-lookup"><span data-stu-id="09adc-110">For more information, see [Policy CSP - ApplicationDefaults](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration).</span></span>

1. <span data-ttu-id="09adc-111">Defina um novo ProgID com o canal Microsoft Edge a ser usado para abrir com o modo Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="09adc-111">Define a new ProgID with the Microsoft Edge channel to use to open with Internet Explorer mode.</span></span> <span data-ttu-id="09adc-112">O ProgID inclui o nome e o ícone do aplicativo e o caminho completo para msedge.exe.</span><span class="sxs-lookup"><span data-stu-id="09adc-112">The ProgID includes the application name and Icon and the full path to msedge.exe.</span></span>

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

2. <span data-ttu-id="09adc-113">Configure as atualizações do shell para passar a linha de comando necessária para abrir com o modo IE.</span><span class="sxs-lookup"><span data-stu-id="09adc-113">Configure shell updates to pass the command line needed to open with IE mode.</span></span>

```markdown
[HKEY_CURRENT_USER\SOFTWARE\Classes\MSEdgeIEModeMHT\shell\open\command]
@="\"C:\\<edge_installation_dir>\\msedge.exe\" -ie-mode-file-url -- \"%1\""
```

3. <span data-ttu-id="09adc-114">Por fim, associe a extensão de arquivo .mht a um novo ProgID.</span><span class="sxs-lookup"><span data-stu-id="09adc-114">Finally, associate the .mht file extension with a new ProgID.</span></span> <span data-ttu-id="09adc-115">Adicione o ProgID como um nome de valor, com o tipo de valor de REG_SZ.</span><span class="sxs-lookup"><span data-stu-id="09adc-115">Add your ProgID as a value name, with the value type of REG_SZ.</span></span>

```markdown
[HKEY_CURRENT_USER\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\FileExts\.mht\OpenWithProgids]
"MSEdgeIEModeMHT"=hex(0):
```

<span data-ttu-id="09adc-116">Depois de definir as chaves descritas no exemplo anterior, os usuários verão uma opção adicional no menu **Abrir com** para abrir um arquivo .mht usando o Microsoft Edge \<channel\> com o modo IE.</span><span class="sxs-lookup"><span data-stu-id="09adc-116">After you set the keys described in the previous example, your users will see an additional option on the **Open with** menu to open an .mht file using Microsoft Edge \<channel\> with IE mode.</span></span>

## <span data-ttu-id="09adc-117">Exemplo de registro</span><span class="sxs-lookup"><span data-stu-id="09adc-117">Registry Example</span></span>

<span data-ttu-id="09adc-118">Você pode salvar o trecho de código a seguir como um arquivo .reg e importá-lo para o registro.</span><span class="sxs-lookup"><span data-stu-id="09adc-118">You can save the following code snippet as a .reg file and import it into the registry.</span></span>

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

## <span data-ttu-id="09adc-119">Consulte também</span><span class="sxs-lookup"><span data-stu-id="09adc-119">See also</span></span>

- [<span data-ttu-id="09adc-120">Sobre o modo IE</span><span class="sxs-lookup"><span data-stu-id="09adc-120">About IE mode</span></span>](https://docs.microsoft.com/deployedge/edge-ie-mode)
- [<span data-ttu-id="09adc-121">Informações de sites configuráveis</span><span class="sxs-lookup"><span data-stu-id="09adc-121">Configurable sites information</span></span>](https://docs.microsoft.com/deployedge/edge-learnmore-configurable-sites-ie-mode)
- [<span data-ttu-id="09adc-122">Informações adicionais sobre o Modo Empresarial</span><span class="sxs-lookup"><span data-stu-id="09adc-122">Additional Enterprise Mode information</span></span>](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
- [<span data-ttu-id="09adc-123">Configurando associações de tipo de arquivo</span><span class="sxs-lookup"><span data-stu-id="09adc-123">Setting file type associations</span></span>](https://docs.microsoft.com/windows/win32/shell/fa-file-types)
- [<span data-ttu-id="09adc-124">Página de aterrissagem do Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="09adc-124">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
