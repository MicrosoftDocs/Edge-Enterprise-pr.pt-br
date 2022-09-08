---
title: Documentação de Política do Microsoft Edge WebView2
ms.author: stmoody
author: dan-wesley
manager: venkatk
ms.date: 09/07/2022
audience: ITPro
ms.topic: reference
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
ms.custom: generated
description: Documentação do Windows e do Mac para todas as políticas compatíveis com o Microsoft Edge Browser
ms.openlocfilehash: 9b081a027d0cdc83735f3fd4e2684bcecd895f32
ms.sourcegitcommit: 80d9f61a23a7dc0def80089850a53ea02e571ed6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/08/2022
ms.locfileid: "12746107"
---
# <a name="microsoft-edge-webview2---policies"></a>Políticas do Microsoft Edge WebView2

A versão mais recente do Microsoft Edge WebView2 inclui as políticas a seguir. Você pode usar essas políticas para configurar como o Microsoft Edge WebView2 será executado em sua organização.

Para saber mais sobre o conjunto adicional de políticas, usado para controlar como e quando o Microsoft Edge WebView2 é atualizado, confira [Referência de política de atualização do Microsoft Edge](microsoft-edge-update-policies.md).


> [!NOTE]
> Este artigo se aplica ao Microsoft Edge versão 87 ou posterior.

## <a name="available-policies"></a>Políticas disponíveis

Estas tabelas listam todas as políticas de grupo disponíveis nesta versão do Microsoft Edge WebView2. Use os links na tabela a seguir para obter mais detalhes sobre políticas específicas.

- [Configurações de substituição do carregador](#loader-override-settings)
- [Adicional](#additional)


### [*<a name="loader-override-settings"></a>Configurações de substituição do carregador*](#loader-override-settings-policies)

|Nome da política|Legenda|
|-|-|
|[BrowserExecutableFolder](#browserexecutablefolder)|Configurar o local da pasta executável do navegador|
|[ReleaseChannelPreference](#releasechannelpreference)|Definir a preferência de ordem de pesquisa do canal de lançamento|
### [*<a name="additional"></a>Adicional*](#additional-policies)

|Nome da política|Legenda|
|-|-|
|[ExperimentationAndConfigurationServiceControl](#experimentationandconfigurationservicecontrol)|Controlar a comunicação com o serviço de experimentação e configuração|




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

  ## <a name="additional-policies"></a>Políticas adicionais

  [Voltar ao início](#microsoft-edge-webview2---policies)

  ### <a name="experimentationandconfigurationservicecontrol"></a>ExperimentationAndConfigurationServiceControl

  #### <a name="control-communication-with-the-experimentation-and-configuration-service"></a>Controlar a comunicação com o serviço de experimentação e configuração

  
  
  #### <a name="supported-versions"></a>Versões com suporte:

  - No Windows desde 97 ou posterior

  #### <a name="description"></a>Descrição

  O Serviço de Experimentação e Configuração é usado para implantar cargas de Experimentação e Configuração no cliente.

O conteúdo de experimentação consiste em uma lista dos recursos em desenvolvimento inicial que a Microsoft está disponibilizando para testes e comentários.

A carga de configuração consiste em uma lista de configurações recomendadas que a Microsoft deseja implantar para otimizar a experiência do usuário.

A carga de configuração também pode conter uma lista de ações a serem executadas em determinados domínios por motivos de compatibilidade. Por exemplo, o navegador pode substituir a cadeia de caracteres do Agente do Usuário em um site se esse site for interrompido. Cada uma dessas ações deve ser temporária enquanto a Microsoft tenta resolver o problema com o proprietário do site.

Se você definir essa política como o modo 'FullMode', o conteúdo total será baixado do Serviço de Experimentação e Configuração. Isso inclui os conteúdos de experimentação e configuração.

Se você definir essa política como 'ConfigurationsOnlyMode', somente a carga de configuração será baixada.

Se você definir essa política como 'RestrictedMode', a comunicação com o Serviço de Experimentação e Configuração será interrompida completamente. A Microsoft não recomenda essa configuração.

Se você não configurar essa política em um dispositivo gerenciado, o comportamento nos canais Beta e Estável será o mesmo que o 'ConfigurationsOnlyMode'. Nos canais Canary e Dev, o comportamento é o mesmo que 'FullMode'.

Se você não configurar essa política em um dispositivo não gerenciado, o comportamento será o mesmo que o 'FullMode'.

Mapeamento das opções de política:

* FullMode (2) = Recuperar configurações e experiências

* ConfigurationsOnlyMode (1) = Recuperar apenas configurações

* RestrictedMode (0) = Desabilitar a comunicação com o Serviço de Experimentação e Configuração

Use as informações anteriores ao configurar essa política.

  #### <a name="supported-features"></a>Recursos compatíveis:

  - Pode ser obrigatório: Sim
  - Pode ser recomendável: não
  - Atualização dinâmica das políticas: Sim

  #### <a name="data-type"></a>Tipo de dados:

  - Inteiro

  #### <a name="windows-information-and-settings"></a>Informações e configurações do Windows

  ##### <a name="group-policy-admx-info"></a>Informações da Política de Grupo (ADMX)

  - Nome Exclusivo da Política de Grupo: ExperimentationAndConfigurationServiceControl
  - Nome da Política de Grupo: Controlar a comunicação com o serviço de experimentação e configuração
  - Caminho da Política de Grupo (obrigatório): Modelos Administrativos/Microsoft Edge WebView2/
  - Caminho da Política de Grupo (recomendado): N/A
  - Nome do arquivo ADMX da PG: MSEdgeWebView2.admx

  ##### <a name="windows-registry-settings"></a>Configurações de registro do Windows

  - Caminho (obrigatório): SOFTWARE\Policies\Microsoft\Edge\WebView2
  - Caminho (recomendado): N/A
  - Nome do valor: ExperimentationAndConfigurationServiceControl
  - Tipo de valor: REG_DWORD

  ##### <a name="example-value"></a>Valor de exemplo:

```
0x00000002
```

  

  [Voltar ao início](#microsoft-edge-webview2---policies)


## <a name="see-also"></a>Consulte também

- [Configurar o Microsoft Edge](configure-microsoft-edge.md)
- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Blog de linhas de base de segurança da Microsoft](https://techcommunity.microsoft.com/t5/microsoft-security-baselines/bg-p/Microsoft-Security-Baselines)