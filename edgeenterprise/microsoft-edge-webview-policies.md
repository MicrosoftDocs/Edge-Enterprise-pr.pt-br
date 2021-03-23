---
title: Documentação de Política do Microsoft Edge WebView2
ms.author: stmoody
author: dan-wesley
manager: tahills
ms.date: 03/18/2021
audience: ITPro
ms.topic: reference
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
ms.custom: ''
description: Documentação do Windows e do Mac para todas as políticas compatíveis com o Microsoft Edge Browser
ms.openlocfilehash: 38aac0e4ffd932583ad48a2dd13cf8e93df79e29
ms.sourcegitcommit: 6a3787dead062e4a0860adbc570229974dcaee07
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "11442371"
---
# <a name="microsoft-edge-webview2---policies"></a>Políticas do Microsoft Edge WebView2

A versão mais recente do Microsoft Edge WebView2 inclui as políticas a seguir. Você pode usar essas políticas para configurar como o Microsoft Edge WebView2 será executado em sua organização.

Para saber mais sobre o conjunto adicional de políticas, usado para controlar como e quando o Microsoft Edge WebView2 é atualizado, confira [Referência de política de atualização do Microsoft Edge](microsoft-edge-update-policies.md).

> [!NOTE]
> Este artigo se aplica ao Microsoft Edge versão 87 ou posterior.

## <a name="available-policies"></a>Políticas disponíveis

Estas tabelas listam todas as políticas de grupo disponíveis nesta versão do Microsoft Edge WebView2. Use os links na tabela a seguir para obter mais detalhes sobre políticas específicas.

- [Configurações de substituição do carregador](#loader-override-settings)


### [*<a name="loader-override-settings"></a>Configurações de substituição do carregador*](#loader-override-settings-policies)

|Nome da política|Legenda|
|-|-|
|[BrowserExecutableFolder](#browserexecutablefolder)|Configurar o local da pasta executável do navegador|
|[ReleaseChannelPreference](#releasechannelpreference)|Definir a preferência de ordem de pesquisa do canal de lançamento|




  ## <a name="loader-override-settings-policies"></a>Políticas de configurações de substituição do carregador

  [Voltar ao início](#microsoft-edge-webview2---policies)

  ### <a name="browserexecutablefolder"></a>BrowserExecutableFolder

  #### <a name="configure-the-location-of-the-browser-executable-folder"></a>Configurar o local da pasta executável do navegador

  
  
  #### <a name="supported-versions"></a>Versões com suporte:

  - No Windows desde 87 ou posterior

  #### <a name="description"></a>Descrição

  Essa política configura aplicativos de WebView2 para usar o WebView2 Runtime no caminho especificado. A pasta deve conter os seguintes arquivos: msedgewebview2.exe, msedge.dll e assim por diante.

Para definir o valor do caminho da pasta, forneça um Nome do valor e um Par do valor. Defina o nome do valor para a ID do Modelo de Usuário do Aplicativo ou o nome do arquivo executável. Você pode usar o caractere curinga "*" como nome do valor a ser aplicado a todos os aplicativos.

  #### <a name="supported-features"></a>Recursos compatíveis:

  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### <a name="data-type"></a>Tipo de dados:

  - Lista de cadeias de caracteres

  #### <a name="windows-information-and-settings"></a>Informações e configurações do Windows

  ##### <a name="group-policy-admx-info"></a>Informações da Política de Grupo (ADMX)

  - Nome exclusivo da PG: BrowserExecutableFolder
  - Nome da PG: Configurar o local da pasta executável do navegador
  - Caminho da PG (obrigatório): Modelos administrativos/Microsoft Edge WebView2/Configurações de substituição do carregador
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da PG: MSEdgeWebView2.admx

  ##### <a name="windows-registry-settings"></a>Configurações de registro do Windows

  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge\WebView2\BrowserExecutableFolder
  - Caminho (recomendado): N/A
  - Nome de valor: lista de REG_SZ
  - Tipo de valor: lista de REG_SZ

  ##### <a name="example-value"></a>Valor de exemplo:

```
SOFTWARE\Policies\Microsoft\Edge\WebView2\BrowserExecutableFolder = "Name: *, Value: C:\\Program Files\\Microsoft Edge WebView2 Runtime Redistributable 85.0.541.0 x64"

```

  

  [Voltar ao início](#microsoft-edge-webview2---policies)

  ### <a name="releasechannelpreference"></a>ReleaseChannelPreference

  #### <a name="set-the-release-channel-search-order-preference"></a>Definir a preferência de ordem de pesquisa do canal de lançamento

  
  
  #### <a name="supported-versions"></a>Versões com suporte:

  - No Windows desde 87 ou posterior

  #### <a name="description"></a>Descrição

  O pedido padrão de pesquisa de canal é WebView2 Runtime, Beta, Dev e Canary.

Para inverter a ordem de pesquisa padrão, defina essa política como 1.

Para definir o valor da preferência de canal de lançamento, forneça um Nome do valor e um Par do valor. Defina o nome do valor para a ID do Modelo de Usuário do Aplicativo ou o nome do arquivo executável. Você pode usar o caractere curinga "*" como nome do valor a ser aplicado a todos os aplicativos.

  #### <a name="supported-features"></a>Recursos compatíveis:

  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### <a name="data-type"></a>Tipo de dados:

  - Lista de cadeias de caracteres

  #### <a name="windows-information-and-settings"></a>Informações e configurações do Windows

  ##### <a name="group-policy-admx-info"></a>Informações da Política de Grupo (ADMX)

  - Nome exclusivo da PG: ReleaseChannelPreference
  - Nome da PG: Definir a preferência de ordem de pesquisa do canal de lançamento
  - Caminho da PG (obrigatório): Modelos administrativos/Microsoft Edge WebView2/Configurações de substituição do carregador
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da PG: MSEdgeWebView2.admx

  ##### <a name="windows-registry-settings"></a>Configurações de registro do Windows

  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge\WebView2\ReleaseChannelPreference
  - Caminho (recomendado): N/A
  - Nome de valor: lista de REG_SZ
  - Tipo de valor: lista de REG_SZ

  ##### <a name="example-value"></a>Valor de exemplo:

```
SOFTWARE\Policies\Microsoft\Edge\WebView2\ReleaseChannelPreference = "Name: *, Value: 1"

```

  

  [Voltar ao início](#microsoft-edge-webview2---policies)


## <a name="see-also"></a>Ver também

- [Configurar o Microsoft Edge](configure-microsoft-edge.md)
- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Blog de linhas de base de segurança da Microsoft](https://techcommunity.microsoft.com/t5/microsoft-security-baselines/bg-p/Microsoft-Security-Baselines)