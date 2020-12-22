---
title: Associar extensões de arquivo com o modo Internet Explorer
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 12/21/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Associar extensões de arquivo com o modo Internet Explorer
ms.openlocfilehash: 9f39a3319c3e45001090dd9f0cffb3e7ce2648fb
ms.sourcegitcommit: 306582403d4272831bcac390154c7cc7041a9b7e
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/21/2020
ms.locfileid: "11238188"
---
# <span data-ttu-id="6c211-103">Associar extensões de arquivo com o modo Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="6c211-103">Associate file extensions with Internet Explorer mode</span></span>

<span data-ttu-id="6c211-104">Este artigo explica como associar o Microsoft Edge com o modo do Internet Explorer com extensões de arquivo para aplicativos da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="6c211-104">This article explains how to associate Microsoft Edge with Internet Explorer mode with file extensions for desktop applications.</span></span>

> [!NOTE]
> <span data-ttu-id="6c211-105">Este artigo se aplica ao Microsoft Edge versão 86 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="6c211-105">This article applies to Microsoft Edge version 86 or later.</span></span>

## <span data-ttu-id="6c211-106">Diretrizes de associação de extensão de arquivo com o modo Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="6c211-106">Guidance for file extension association with Internet Explorer mode</span></span>

<span data-ttu-id="6c211-107">As instruções a seguir mostram uma entrada que associa o Microsoft Edge com o modo IE ao tipo de arquivo. mht.</span><span class="sxs-lookup"><span data-stu-id="6c211-107">The following instructions show an entry that associates Microsoft Edge with IE mode with the .mht file type.</span></span> <span data-ttu-id="6c211-108">Use as etapas a seguir como um guia para definir uma associação de arquivo.</span><span class="sxs-lookup"><span data-stu-id="6c211-108">Use the following steps as a guide for setting a file association.</span></span>

> [!NOTE]
> <span data-ttu-id="6c211-109">Você pode definir extensões de arquivo específicas para abrir no modo Internet Explorer por padrão usando a política para **Definir um arquivo de configuração de associações padrão**.</span><span class="sxs-lookup"><span data-stu-id="6c211-109">You can set specific file extensions to open in Internet Explorer mode by default using the policy to **Set a default associations configuration file**.</span></span> <span data-ttu-id="6c211-110">Para obter mais informações, consulte [Política de CSP – ApplicationDefaults](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration).</span><span class="sxs-lookup"><span data-stu-id="6c211-110">For more information, see [Policy CSP - ApplicationDefaults](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration).</span></span>

1. <span data-ttu-id="6c211-111">Defina um novo ProgID com o canal Microsoft Edge a ser usado para abrir com o modo Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="6c211-111">Define a new ProgID with the Microsoft Edge channel to use to open with Internet Explorer mode.</span></span> <span data-ttu-id="6c211-112">O ProgID inclui o nome e o ícone do aplicativo e o caminho completo para msedge.exe.</span><span class="sxs-lookup"><span data-stu-id="6c211-112">The ProgID includes the application name and Icon and the full path to msedge.exe.</span></span>

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

2. <span data-ttu-id="6c211-113">Configure as atualizações do shell para passar a linha de comando necessária para abrir com o modo IE.</span><span class="sxs-lookup"><span data-stu-id="6c211-113">Configure shell updates to pass the command line needed to open with IE mode.</span></span>

```markdown
[HKEY_CURRENT_USER\SOFTWARE\Classes\MSEdgeIEModeMHT\shell\open\command]
@="\"C:\\<edge_installation_dir>\\msedge.exe\" -ie-mode-file-url -- \"%1\""
```

3. <span data-ttu-id="6c211-114">Por fim, associe a extensão de arquivo .mht a um novo ProgID.</span><span class="sxs-lookup"><span data-stu-id="6c211-114">Finally, associate the .mht file extension with a new ProgID.</span></span> <span data-ttu-id="6c211-115">Adicione o ProgID como um nome de valor, com o tipo de valor de REG_SZ.</span><span class="sxs-lookup"><span data-stu-id="6c211-115">Add your ProgID as a value name, with the value type of REG_SZ.</span></span>

```markdown
[HKEY_CURRENT_USER\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\FileExts\.mht\OpenWithProgids]
"MSEdgeIEModeMHT"=hex(0):
```

<span data-ttu-id="6c211-116">Depois de definir as chaves descritas no exemplo anterior, os usuários verão uma opção adicional no menu **Abrir com** para abrir um arquivo .mht usando o Microsoft Edge \<channel\> com o modo IE.</span><span class="sxs-lookup"><span data-stu-id="6c211-116">After you set the keys described in the previous example, your users will see an additional option on the **Open with** menu to open an .mht file using Microsoft Edge \<channel\> with IE mode.</span></span>

## <span data-ttu-id="6c211-117">Exemplo de registro</span><span class="sxs-lookup"><span data-stu-id="6c211-117">Registry Example</span></span>

<span data-ttu-id="6c211-118">Você pode salvar o trecho de código a seguir como um arquivo .reg e importá-lo para o registro.</span><span class="sxs-lookup"><span data-stu-id="6c211-118">You can save the following code snippet as a .reg file and import it into the registry.</span></span>

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
## <span data-ttu-id="6c211-119">Configurando tipos de arquivo para abrir no modo Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="6c211-119">Configuring file types to open in Internet Explorer mode</span></span>

<span data-ttu-id="6c211-120">Ao iniciar o Microsoft Edge 88, você pode configurar links de tipos de arquivo específicos para abrir no modo do Internet Explorer usando a política [ Mostrar menu de contexto para abrir links no modo do Internet Explorer](https://docs.microsoft.com/deployedge/microsoft-edge-policies#show-context-menu-to-open-a-link-in-internet-explorer-mode).</span><span class="sxs-lookup"><span data-stu-id="6c211-120">Starting Edge 88, you can configure specific file type links to open in Internet Explorer mode using the policy [Show context menu to open links in Internet Explorer mode](https://docs.microsoft.com/deployedge/microsoft-edge-policies#show-context-menu-to-open-a-link-in-internet-explorer-mode).</span></span> 

<span data-ttu-id="6c211-121">Você pode definir os tipos de arquivo aos quais essa opção deve ser aplicada, especificando as extensões de arquivo nesta política [Abrir arquivos locais na lista de permissões de extensão de arquivo no modo Internet Explorer](https://docs.microsoft.com/deployedge/microsoft-edge-policies#internetexplorerintegrationlocalfileextensionallowlist).</span><span class="sxs-lookup"><span data-stu-id="6c211-121">You can define file types this option should apply to, by specifying file extensions in this policy [Open local files in Internet Explorer mode file extension allow list](https://docs.microsoft.com/deployedge/microsoft-edge-policies#internetexplorerintegrationlocalfileextensionallowlist).</span></span> 

## <span data-ttu-id="6c211-122">Consulte também</span><span class="sxs-lookup"><span data-stu-id="6c211-122">See also</span></span>

- [<span data-ttu-id="6c211-123">Sobre o modo IE</span><span class="sxs-lookup"><span data-stu-id="6c211-123">About IE mode</span></span>](https://docs.microsoft.com/deployedge/edge-ie-mode)
- [<span data-ttu-id="6c211-124">Informações de sites configuráveis</span><span class="sxs-lookup"><span data-stu-id="6c211-124">Configurable sites information</span></span>](https://docs.microsoft.com/deployedge/edge-learnmore-configurable-sites-ie-mode)
- [<span data-ttu-id="6c211-125">Informações adicionais sobre o Modo Empresarial</span><span class="sxs-lookup"><span data-stu-id="6c211-125">Additional Enterprise Mode information</span></span>](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
- [<span data-ttu-id="6c211-126">Configurando associações de tipo de arquivo</span><span class="sxs-lookup"><span data-stu-id="6c211-126">Setting file type associations</span></span>](https://docs.microsoft.com/windows/win32/shell/fa-file-types)
- [<span data-ttu-id="6c211-127">Página de aterrissagem do Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="6c211-127">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
