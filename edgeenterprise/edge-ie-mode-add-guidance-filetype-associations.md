---
title: Adicionar modo do Internet Explorer ao menu de contexto Abrir com
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 11/13/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Adicionar modo do Internet Explorer ao menu de contexto Abrir com
ms.openlocfilehash: 6453cd2587e3bec10404d2491914debb999fcf3f
ms.sourcegitcommit: e3c80274a9b8ef15761c968214b3cba593476132
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/13/2020
ms.locfileid: "11168477"
---
# <span data-ttu-id="2bf3e-103">Adicionar modo do Internet Explorer ao menu de contexto "Abrir com"</span><span class="sxs-lookup"><span data-stu-id="2bf3e-103">Add Internet Explorer mode to the "Open with" context menu</span></span>

<span data-ttu-id="2bf3e-104">Este artigo explica como associar o Microsoft Edge com o modo do Internet Explorer com extensões de arquivo para aplicativos da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="2bf3e-104">This article explains how to associate Microsoft Edge with Internet Explorer mode with file extensions for desktop applications.</span></span>

> [!NOTE]
> <span data-ttu-id="2bf3e-105">Este artigo se aplica ao Microsoft Edge versão 86 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="2bf3e-105">This article applies to Microsoft Edge version 86 or later.</span></span>

## <span data-ttu-id="2bf3e-106">Diretrizes de associação de extensão de arquivo com o modo Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="2bf3e-106">Guidance for file extension association with Internet Explorer mode</span></span>

<span data-ttu-id="2bf3e-107">As instruções a seguir mostram uma entrada que associa o Microsoft Edge com o modo IE ao tipo de arquivo. mht.</span><span class="sxs-lookup"><span data-stu-id="2bf3e-107">The following instructions show an entry that associates Microsoft Edge with IE mode with the .mht file type.</span></span> <span data-ttu-id="2bf3e-108">Use as etapas a seguir como um guia para definir uma associação de arquivo.</span><span class="sxs-lookup"><span data-stu-id="2bf3e-108">Use the following steps as a guide for setting a file association.</span></span>

> [!NOTE]
> <span data-ttu-id="2bf3e-109">Você pode definir extensões de arquivo específicas para abrir no modo Internet Explorer por padrão usando a política para **Definir um arquivo de configuração de associações padrão**.</span><span class="sxs-lookup"><span data-stu-id="2bf3e-109">You can set specific file extensions to open in Internet Explorer mode by default using the policy to **Set a default associations configuration file**.</span></span> <span data-ttu-id="2bf3e-110">Para obter mais informações, consulte [Política de CSP – ApplicationDefaults](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration).</span><span class="sxs-lookup"><span data-stu-id="2bf3e-110">For more information, see [Policy CSP - ApplicationDefaults](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration).</span></span>

1. <span data-ttu-id="2bf3e-111">Defina um novo ProgID com o canal Microsoft Edge a ser usado para abrir com o modo Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="2bf3e-111">Define a new ProgID with the Microsoft Edge channel to use to open with Internet Explorer mode.</span></span> <span data-ttu-id="2bf3e-112">O ProgID inclui o nome e o ícone do aplicativo e o caminho completo para msedge.exe.</span><span class="sxs-lookup"><span data-stu-id="2bf3e-112">The ProgID includes the application name and Icon and the full path to msedge.exe.</span></span>

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

2. <span data-ttu-id="2bf3e-113">Configure as atualizações do shell para passar a linha de comando necessária para abrir com o modo IE.</span><span class="sxs-lookup"><span data-stu-id="2bf3e-113">Configure shell updates to pass the command line needed to open with IE mode.</span></span>

```markdown
[HKEY_CURRENT_USER\SOFTWARE\Classes\MSEdgeIEModeMHT\shell\open\command]
@="\"C:\\<edge_installation_dir>\\msedge.exe\" -ie-mode-file-url -- \"%1\""
```

3. <span data-ttu-id="2bf3e-114">Por fim, associe a extensão de arquivo .mht a um novo ProgID.</span><span class="sxs-lookup"><span data-stu-id="2bf3e-114">Finally, associate the .mht file extension with a new ProgID.</span></span> <span data-ttu-id="2bf3e-115">Adicione o ProgID como um nome de valor, com o tipo de valor de REG_SZ.</span><span class="sxs-lookup"><span data-stu-id="2bf3e-115">Add your ProgID as a value name, with the value type of REG_SZ.</span></span>

```markdown
[HKEY_CURRENT_USER\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\FileExts\.mht\OpenWithProgids]
"MSEdgeIEModeMHT"=hex(0):
```

<span data-ttu-id="2bf3e-116">Depois de definir as chaves descritas no exemplo anterior, os usuários verão uma opção adicional no menu **Abrir com** para abrir um arquivo .mht usando o Microsoft Edge \<channel\> com o modo IE.</span><span class="sxs-lookup"><span data-stu-id="2bf3e-116">After you set the keys described in the previous example, your users will see an additional option on the **Open with** menu to open an .mht file using Microsoft Edge \<channel\> with IE mode.</span></span>

## <span data-ttu-id="2bf3e-117">Exemplo de registro</span><span class="sxs-lookup"><span data-stu-id="2bf3e-117">Registry Example</span></span>

<span data-ttu-id="2bf3e-118">Você pode salvar o trecho de código a seguir como um arquivo .reg e importá-lo para o registro.</span><span class="sxs-lookup"><span data-stu-id="2bf3e-118">You can save the following code snippet as a .reg file and import it into the registry.</span></span>

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

## <span data-ttu-id="2bf3e-119">Consulte também</span><span class="sxs-lookup"><span data-stu-id="2bf3e-119">See also</span></span>

- [<span data-ttu-id="2bf3e-120">Sobre o modo IE</span><span class="sxs-lookup"><span data-stu-id="2bf3e-120">About IE mode</span></span>](https://docs.microsoft.com/deployedge/edge-ie-mode)
- [<span data-ttu-id="2bf3e-121">Informações de sites configuráveis</span><span class="sxs-lookup"><span data-stu-id="2bf3e-121">Configurable sites information</span></span>](https://docs.microsoft.com/deployedge/edge-learnmore-configurable-sites-ie-mode)
- [<span data-ttu-id="2bf3e-122">Informações adicionais sobre o Modo Empresarial</span><span class="sxs-lookup"><span data-stu-id="2bf3e-122">Additional Enterprise Mode information</span></span>](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
- [<span data-ttu-id="2bf3e-123">Configurando associações de tipo de arquivo</span><span class="sxs-lookup"><span data-stu-id="2bf3e-123">Setting file type associations</span></span>](https://docs.microsoft.com/windows/win32/shell/fa-file-types)
- [<span data-ttu-id="2bf3e-124">Página de aterrissagem do Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="2bf3e-124">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
