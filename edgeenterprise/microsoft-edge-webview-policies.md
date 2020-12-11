---
title: Documentação de Política do Microsoft Edge WebView2
ms.author: stmoody
author: dan-wesley
manager: tahills
ms.date: 12/10/2020
audience: ITPro
ms.topic: reference
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
ms.custom: ''
description: Documentação do Windows e do Mac para todas as políticas compatíveis com o Microsoft Edge Browser
ms.openlocfilehash: 698b291d8831efe1efd7fcbb436fe3921e09f255
ms.sourcegitcommit: 2887b30d46a9fe59d2ab9f95e638197ae058eaf7
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "11205719"
---
# Políticas do Microsoft Edge WebView2

A versão mais recente do Microsoft Edge WebView2 inclui as políticas a seguir. Você pode usar essas políticas para configurar como o Microsoft Edge WebView2 será executado em sua organização.

Para saber mais sobre o conjunto adicional de políticas, usado para controlar como e quando o Microsoft Edge WebView2 é atualizado, confira [Referência de política de atualização do Microsoft Edge](microsoft-edge-update-policies.md).


> [!NOTE]
> Este artigo se aplica ao Microsoft Edge versão 87 ou posterior.

## Políticas disponíveis

Estas tabelas listam todas as políticas de grupo disponíveis nesta versão do Microsoft Edge WebView2. Use os links na tabela a seguir para obter mais detalhes sobre políticas específicas.

|||
|-|-|
|[Configurações de substituição do carregador](#loader-override-settings)|

### [*Configurações de substituição do carregador*](#loader-override-settings-policies)

|Nome da política|Legenda|
|-|-|
|[BrowserExecutableFolder](#browserexecutablefolder)|Configurar o local da pasta executável do navegador|
|[ReleaseChannelPreference](#releasechannelpreference)|Definir a preferência de ordem de pesquisa do canal de lançamento|




  ## Políticas de configurações de substituição do carregador

  [Voltar ao início](#microsoft-edge-webview2---policies)

  ### BrowserExecutableFolder

  #### Configurar o local da pasta executável do navegador

  
  
  #### Versões com suporte:

  - No Windows desde 87 ou posterior

  #### Descrição

  Essa política configura aplicativos de WebView2 para usar o WebView2 Runtime no caminho especificado. A pasta deve conter os seguintes arquivos: msedgewebview2.exe, msedge.dll e assim por diante.

Para definir o valor do caminho da pasta, forneça um Nome do valor e um Par do valor. Defina o nome do valor para a ID do Modelo de Usuário do Aplicativo ou o nome do arquivo executável. Você pode usar o caractere curinga "*" como nome do valor a ser aplicado a todos os aplicativos.

  #### Recursos compatíveis:

  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:

  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows

  ##### Informações da Política de Grupo (ADMX)

  - Nome exclusivo da PG: BrowserExecutableFolder
  - Nome da PG: Configurar o local da pasta executável do navegador
  - Caminho da PG (obrigatório): Modelos administrativos/Microsoft Edge WebView2/Configurações de substituição do carregador
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da PG: MSEdgeWebView2.admx

  ##### Configurações de registro do Windows

  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge\WebView2\BrowserExecutableFolder
  - Caminho (recomendado): N/A
  - Nome de valor: lista de REG_SZ
  - Tipo de valor: lista de REG_SZ

  ##### Valor de exemplo:

```
SOFTWARE\Policies\Microsoft\Edge\WebView2\BrowserExecutableFolder = "Name: *, Value: C:\\Program Files\\Microsoft Edge WebView2 Runtime Redistributable 85.0.541.0 x64"

```

  

  [Voltar ao início](#microsoft-edge-webview2---policies)

  ### ReleaseChannelPreference

  #### Definir a preferência de ordem de pesquisa do canal de lançamento

  
  
  #### Versões com suporte:

  - No Windows desde 87 ou posterior

  #### Descrição

  O pedido padrão de pesquisa de canal é WebView2 Runtime, Beta, Dev e Canary.

Para inverter a ordem de pesquisa padrão, defina essa política como 1.

Para definir o valor da preferência de canal de lançamento, forneça um Nome do valor e um Par do valor. Defina o nome do valor para a ID do Modelo de Usuário do Aplicativo ou o nome do arquivo executável. Você pode usar o caractere curinga "*" como nome do valor a ser aplicado a todos os aplicativos.

  #### Recursos compatíveis:

  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### Tipo de dados:

  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows

  ##### Informações da Política de Grupo (ADMX)

  - Nome exclusivo da PG: ReleaseChannelPreference
  - Nome da PG: Definir a preferência de ordem de pesquisa do canal de lançamento
  - Caminho da PG (obrigatório): Modelos administrativos/Microsoft Edge WebView2/Configurações de substituição do carregador
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da PG: MSEdgeWebView2.admx

  ##### Configurações de registro do Windows

  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge\WebView2\ReleaseChannelPreference
  - Caminho (recomendado): N/A
  - Nome de valor: lista de REG_SZ
  - Tipo de valor: lista de REG_SZ

  ##### Valor de exemplo:

```
SOFTWARE\Policies\Microsoft\Edge\WebView2\ReleaseChannelPreference = "Name: *, Value: 1"

```

  

  [Voltar ao início](#microsoft-edge-webview2---policies)


## Consulte também

- [Configurar o Microsoft Edge](configure-microsoft-edge.md)
- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Blog de linhas de base de segurança da Microsoft](https://techcommunity.microsoft.com/t5/microsoft-security-baselines/bg-p/Microsoft-Security-Baselines)