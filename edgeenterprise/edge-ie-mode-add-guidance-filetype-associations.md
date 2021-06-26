---
title: Associar extensões de arquivo com o modo Internet Explorer
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 05/19/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Associar extensões de arquivo com o modo Internet Explorer
ms.openlocfilehash: c027b11e426cd665cb9e6cc25b4c9f66a0c6762a
ms.sourcegitcommit: 4192328ee585bc32a9be528766b8a5a98e046c8e
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/25/2021
ms.locfileid: "11617451"
---
# <a name="associate-file-extensions-with-internet-explorer-mode"></a><span data-ttu-id="c0725-103">Associar extensões de arquivo ao modo Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="c0725-103">Associate file extensions with Internet Explorer mode</span></span>

>[!Note]
> <span data-ttu-id="c0725-104">O aplicativo de área de trabalho Internet Explorer 11 será desativado e ficará sem suporte em 15 de junho de 2022 (para obter uma lista do que está no escopo, [consulte as Perguntas frequentes](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/internet-explorer-11-desktop-app-retirement-faq/ba-p/2366549)).</span><span class="sxs-lookup"><span data-stu-id="c0725-104">The Internet Explorer 11 desktop application will be retired and go out of support on June 15, 2022 (for a list of what’s in scope, [see the FAQ](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/internet-explorer-11-desktop-app-retirement-faq/ba-p/2366549)).</span></span> <span data-ttu-id="c0725-105">Os mesmos aplicativos e sites do IE11 que você usa hoje podem abrir no Microsoft Edge com o modo Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="c0725-105">The same IE11 apps and sites you use today can open in Microsoft Edge with Internet Explorer mode.</span></span> <span data-ttu-id="c0725-106">[Saiba mais aqui](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/).</span><span class="sxs-lookup"><span data-stu-id="c0725-106">[Learn more here](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/).</span></span>

<span data-ttu-id="c0725-107">Este artigo explica como associar o Microsoft Edge com o modo do Internet Explorer com extensões de arquivo para aplicativos da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="c0725-107">This article explains how to associate Microsoft Edge with Internet Explorer mode with file extensions for desktop applications.</span></span>

> [!NOTE]
> <span data-ttu-id="c0725-108">Este artigo se aplica ao Microsoft Edge versão 86 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="c0725-108">This article applies to Microsoft Edge version 86 or later.</span></span>

## <a name="guidance-for-file-extension-association-with-internet-explorer-mode"></a><span data-ttu-id="c0725-109">Diretrizes de associação de extensão de arquivo com o modo Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="c0725-109">Guidance for file extension association with Internet Explorer mode</span></span>

<span data-ttu-id="c0725-110">As instruções a seguir mostram uma entrada que associa o Microsoft Edge com o modo IE ao tipo de arquivo. mht.</span><span class="sxs-lookup"><span data-stu-id="c0725-110">The following instructions show an entry that associates Microsoft Edge with IE mode with the .mht file type.</span></span> <span data-ttu-id="c0725-111">Use as etapas a seguir como um guia para definir uma associação de arquivo.</span><span class="sxs-lookup"><span data-stu-id="c0725-111">Use the following steps as a guide for setting a file association.</span></span>

> [!NOTE]
> <span data-ttu-id="c0725-112">Você pode definir extensões de arquivo específicas para abrir no modo Internet Explorer por padrão usando a política para **Definir um arquivo de configuração de associações padrão**.</span><span class="sxs-lookup"><span data-stu-id="c0725-112">You can set specific file extensions to open in Internet Explorer mode by default using the policy to **Set a default associations configuration file**.</span></span> <span data-ttu-id="c0725-113">Para obter mais informações, consulte [Política de CSP – ApplicationDefaults](/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration).</span><span class="sxs-lookup"><span data-stu-id="c0725-113">For more information, see [Policy CSP - ApplicationDefaults](/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration).</span></span>

1. <span data-ttu-id="c0725-114">Defina um novo ProgID com o canal Microsoft Edge a ser usado para abrir com o modo Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="c0725-114">Define a new ProgID with the Microsoft Edge channel to use to open with Internet Explorer mode.</span></span> <span data-ttu-id="c0725-115">O ProgID inclui o nome e o ícone do aplicativo e o caminho completo para msedge.exe.</span><span class="sxs-lookup"><span data-stu-id="c0725-115">The ProgID includes the application name and Icon and the full path to msedge.exe.</span></span>

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

2. <span data-ttu-id="c0725-116">Configure as atualizações do shell para passar a linha de comando necessária para abrir com o modo IE.</span><span class="sxs-lookup"><span data-stu-id="c0725-116">Configure shell updates to pass the command line needed to open with IE mode.</span></span>

```markdown
[HKEY_CURRENT_USER\SOFTWARE\Classes\MSEdgeIEModeMHT\shell\open\command]
@="\"C:\\<edge_installation_dir>\\msedge.exe\" -ie-mode-file-url -- \"%1\""
```

3. <span data-ttu-id="c0725-117">Por fim, associe a extensão de arquivo .mht a um novo ProgID.</span><span class="sxs-lookup"><span data-stu-id="c0725-117">Finally, associate the .mht file extension with a new ProgID.</span></span> <span data-ttu-id="c0725-118">Adicione o ProgID como um nome de valor, com o tipo de valor de REG_SZ.</span><span class="sxs-lookup"><span data-stu-id="c0725-118">Add your ProgID as a value name, with the value type of REG_SZ.</span></span>

```markdown
[HKEY_CURRENT_USER\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\FileExts\.mht\OpenWithProgids]
"MSEdgeIEModeMHT"=hex(0):
```

<span data-ttu-id="c0725-119">Depois de definir as chaves descritas no exemplo anterior, os usuários verão uma opção adicional no menu **Abrir com** para abrir um arquivo .mht usando o Microsoft Edge \<channel\> com o modo IE.</span><span class="sxs-lookup"><span data-stu-id="c0725-119">After you set the keys described in the previous example, your users will see an additional option on the **Open with** menu to open an .mht file using Microsoft Edge \<channel\> with IE mode.</span></span>

## <a name="registry-example"></a><span data-ttu-id="c0725-120">Exemplo de registro</span><span class="sxs-lookup"><span data-stu-id="c0725-120">Registry Example</span></span>

<span data-ttu-id="c0725-121">Você pode salvar o trecho de código a seguir como um arquivo .reg e importá-lo para o registro.</span><span class="sxs-lookup"><span data-stu-id="c0725-121">You can save the following code snippet as a .reg file and import it into the registry.</span></span>

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

## <a name="configuring-file-types-to-open-in-internet-explorer-mode"></a><span data-ttu-id="c0725-122">Configurando tipos de arquivo para abrir no modo Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="c0725-122">Configuring file types to open in Internet Explorer mode</span></span>

<span data-ttu-id="c0725-123">Ao iniciar o Microsoft Edge 88, você pode configurar links de tipos de arquivo específicos para abrir no modo do Internet Explorer usando a política [ Mostrar menu de contexto para abrir links no modo do Internet Explorer](./microsoft-edge-policies.md#internetexplorerintegrationreloadiniemodeallowed).</span><span class="sxs-lookup"><span data-stu-id="c0725-123">Starting Edge 88, you can configure specific file type links to open in Internet Explorer mode using the policy [Show context menu to open links in Internet Explorer mode](./microsoft-edge-policies.md#internetexplorerintegrationreloadiniemodeallowed).</span></span>

<span data-ttu-id="c0725-124">Você pode definir os tipos de arquivo aos quais essa opção deve ser aplicada, especificando as extensões de arquivo nesta política [Abrir arquivos locais na lista de permissões de extensão de arquivo no modo Internet Explorer](./microsoft-edge-policies.md#internetexplorerintegrationlocalfileextensionallowlist).</span><span class="sxs-lookup"><span data-stu-id="c0725-124">You can define file types this option should apply to, by specifying file extensions in this policy [Open local files in Internet Explorer mode file extension allow list](./microsoft-edge-policies.md#internetexplorerintegrationlocalfileextensionallowlist).</span></span> 

## <a name="see-also"></a><span data-ttu-id="c0725-125">Consulte também</span><span class="sxs-lookup"><span data-stu-id="c0725-125">See also</span></span>

- [<span data-ttu-id="c0725-126">Sobre o modo IE</span><span class="sxs-lookup"><span data-stu-id="c0725-126">About IE mode</span></span>](./edge-ie-mode.md)
- [<span data-ttu-id="c0725-127">Informações de sites configuráveis</span><span class="sxs-lookup"><span data-stu-id="c0725-127">Configurable sites information</span></span>](./edge-learnmore-configurable-sites-ie-mode.md)
- [<span data-ttu-id="c0725-128">Informações adicionais sobre o Modo Empresarial</span><span class="sxs-lookup"><span data-stu-id="c0725-128">Additional Enterprise Mode information</span></span>](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
- [<span data-ttu-id="c0725-129">Configurando associações de tipo de arquivo</span><span class="sxs-lookup"><span data-stu-id="c0725-129">Setting file type associations</span></span>](/windows/win32/shell/fa-file-types)
- [<span data-ttu-id="c0725-130">Página de aterrissagem do Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="c0725-130">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)