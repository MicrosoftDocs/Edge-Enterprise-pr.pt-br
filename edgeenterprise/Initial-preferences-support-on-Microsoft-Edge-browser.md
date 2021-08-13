---
title: Suporte a preferências iniciais Microsoft Edge navegador
ms.author: collw
author: AndreaLBarr
manager: srugh
ms.date: 07/27/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: As preferências iniciais dão suporte Microsoft Edge navegador.
ms.openlocfilehash: 39af88d21107ad548166c749c3ba765754270b48
ms.sourcegitcommit: 715cb8c8101a6daed48563f33d2bc40ee7109e0e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/13/2021
ms.locfileid: "11882257"
---
# <a name="configure-microsoft-edge-using-initial-preferences-settings-for-the-first-run"></a>Configurar Microsoft Edge usando as configurações de Preferências Iniciais para a primeira execução

Use as informações a seguir para configurar Microsoft Edge configurações de Preferências Iniciais em seus Windows dispositivos.

> [!Note]
> Este artigo se aplica Microsoft Edge versão 93 ou posterior.

## <a name="configure-policy-settings-on-windows"></a>Definir configurações de política no Windows

A partir Microsoft Edge versão 93, a Microsoft oferece suporte a um número limitado de Preferências Iniciais, anteriormente chamadas de "Preferências Mestras", para ajudar os administradores a configurar navegadores para a primeira executar; consulte a lista das configurações suportadas abaixo.  

Quando implantado, as Preferências Iniciais atuam como as configurações padrão do navegador em dispositivos gerenciados; estas são as configurações que são preferidas pelos administradores a serem usadas como padrão, mas podem ser alteradas por usuários ou não estão disponíveis para alguns dispositivos, pois eles não estão ingressados em um domínio do Active Directory®.

Alguns exemplos de configurações de Preferências Iniciais incluem a configuração inicial de uma página inicial padrão ou guias com URLs específicas.

As preferências são copiadas initial_preferences arquivo somente uma vez e qualquer alteração feita nesse arquivo após a configuração não será respeitada. Se uma configuração for gerenciada por [uma Microsoft Edge e](/deployedge/microsoft-edge-policies) configurada no arquivo initial_preferences, a política sempre tem precedência.

A seguir está a lista de configurações de preferências que atualmente são suportadas por Microsoft Edge:

| Categoria Preferências | Configuração |
| - | - |
| Bookmark_bar | show_apps_shortcut<br>show_managed_bookmarks<br>show_on_all_tabs |
| Bookmarks | editing_enabled |
| Navegador /clear_data | browsing_history<br>browsing_history_basic"<br>cache<br>cache_basic<br>cookies<br>download_history<br>form_data<br>passwords |
| Histórico | browsing_history<br>cache<br>cookies<br>download_history<br>form_data<br>hosted_apps_data<br>passwords<br>site_settings |
| Browser | first_run_tabs<br>dark_theme<br>show_toolbar_bookmarks_button<br>show_toolbar_collections_butto<br>show_toolbar_downloads_button<br>show_home_button<br>show_prompt_before_closing_tabs<br>show_toolbar_history_button |
| default_search_provider | [default_search_provider] habilitado |
| Tela inteira | Permitido |
| home page | Homepage_url |
| homepage_is_newtabpage | homepage_is_newtabpage |
| Sessão | restore_on_startup<br>startup_urls |
| Extensões | Extensões : configurações |

## <a name="1-download-an-example-initial_preferences-file"></a>1: Baixar um exemplo initial_preferences arquivo

Para começar, baixe o exemplo *initial_preferences* formulário de arquivo neste local na página inicial Microsoft Edge Enterprise [e](https://www.microsoft.com/edge/business/download) **siga** as etapas abaixo.

## <a name="2-customize-and-validate-the-initial_preferences-file"></a>2: Personalizar e validar o initial_preferences arquivo

Personalize as configurações de ** preferências no arquivo initial_preferences baixado e valide as alterações para garantir que não haja erros no código JSON. Se você encontrar erros, verifique a sintaxe e a estrutura do arquivo *initial_preferences,* faça correções e valide-o novamente. Poucas ferramentas de exemplo para validar JSON, Ferramentas [JSON](https://jsonformatter.org/) Online ou [edição JSON em Visual Studio Code](https://code.visualstudio.com/docs/languages/json).

## <a name="3-deploy-preferences-to-users-computer"></a>3: Implantar preferências no computador dos usuários

Implante o *arquivo initial_preferences* nos dispositivos dos usuários ao mesmo tempo em que Microsoft Edge Browser é implantado e coloque o arquivo no local a seguir no dispositivo.

### <a name="windows-amd64-and-arm64"></a>Windows (AMD64 e ARM64)

| Canal | Location |
| - | - |
| Estável | `"C:\Program Files (x86)\Microsoft\Edge\Application"` |
| Beta | `"C:\Program Files (x86)\Microsoft\Edge Beta\Application"` |
|Canary | `"%LOCALAPPDATA%\Microsoft\Edge SxS\Application"` |
| Dev | `"C:\Program Files (x86)\Microsoft\Edge Dev\Application"` |

**Observação**: o *arquivo initial_preferences* precisa ser implantado na mesma pasta que o arquivo msedge.exe nos computadores Windows usuários.  

### <a name="macos"></a>macOS

| Canal | Location |
| - | - |
| Estável | `"~/Library/Application Support/Microsoft Edge/Microsoft Edge Initial Preferences"` |
| Beta | `“~/Library/Application Support/Microsoft Edge Beta/Microsoft Edge Initial Preferences"` |
| Canary | `“~/Library/Application Support/Microsoft Edge Canary/Microsoft Edge Initial Preferences"` |
| Dev | `"~/Library/Application Support/Microsoft Edge Dev/Microsoft Edge Initial Preferences"` |

## <a name="important-notes-msi--pkg-deployment-and-initial_preferences-interaction"></a>Observações importantes: Implantação de MSI/Pkg *e initial_preferences* interação

As preferências iniciais só entrarão em vigor quando o arquivo initial_preferences for implantado antes que o navegador seja executado pela primeira vez pelos usuários finais.  

## <a name="see-also"></a>Consulte também

- [O *initial_prefrences* de modelo de exemplo](https://www.microsoft.com/edge/business/download)
