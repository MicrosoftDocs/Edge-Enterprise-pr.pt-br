---
title: Saiba como configurar as preferências iniciais no Microsoft Edge.
ms.author: collw
author: dan-wesley
manager: srugh
ms.date: 03/23/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Saiba como configurar as preferências iniciais no Microsoft Edge.
ms.openlocfilehash: 751097853e02589fe1b900f6af0d290feb5fbe67
ms.sourcegitcommit: dd8cdbd35726c795ddce917e549ddf17ee7f5290
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/11/2022
ms.locfileid: "12473401"
---
# <a name="configure-microsoft-edge-using-initial-preferences-settings-for-the-first-run"></a>Configurar Microsoft Edge usando as configurações de Preferências Iniciais para a primeira execução

Use as informações neste artigo para definir Microsoft Edge de Preferências Iniciais em seus Windows dispositivos.

> [!Note]
> Este artigo se aplica Microsoft Edge versão 93 ou posterior.

## <a name="configure-policy-settings-on-windows"></a>Definir configurações de política no Windows

A partir Microsoft Edge versão 93, a Microsoft dá suporte a um número limitado de Preferências Iniciais, anteriormente chamadas de "Preferências Mestras", para ajudar os administradores a configurar navegadores para a primeira execução. Para obter mais informações, consulte as configurações com suporte na tabela de configurações [de preferência a](#preference-settings) seguir.

Quando implantadas, as Preferências Iniciais atuam como as configurações padrão do navegador em dispositivos gerenciados. Essas preferências são as configurações preferenciais dos administradores a serem usadas como configurações padrão do navegador para a primeira execução.

> [!NOTE]
> As preferências iniciais podem ser alteradas pelos usuários e não estão disponíveis para alguns dispositivos porque não estão ingressados em um domínio do® Active Directory.

Alguns exemplos de configurações de preferências iniciais incluem a configuração inicial de uma página inicial padrão ou guias com URLs específicas.

As preferências são copiadas apenas uma vez *do arquivo initial_preferences* , as alterações feitas nesse arquivo após a configuração não serão respeitadas. Se uma configuração for gerenciada por [uma Microsoft Edge e](/deployedge/microsoft-edge-policies) configurada no arquivo *initial_preferences*, a política sempre terá precedência.

### <a name="preference-settings"></a>Configurações de preferência

A tabela a seguir mostra as configurações com suporte no momento Microsoft Edge.

| Categoria preferências | Configuração |
| - | - |
| Bookmark_bar | show_apps_shortcut<br>show_managed_bookmarks<br>show_on_all_tabs |
| Bookmarks | editing_enabled |
| Navegador/clear_data | browsing_history<br>browsing_history_basic"<br>Cache<br>cache_basic<br>cookies<br>download_history<br>form_data<br>Senhas |
| História | browsing_history<br>Cache<br>cookies<br>download_history<br>form_data<br>hosted_apps_data<br>Senhas<br>site_settings |
| Browser | first_run_tabs<br>dark_theme<br>show_toolbar_bookmarks_button<br>show_toolbar_collections_butto<br>show_toolbar_downloads_button<br>show_home_button<br>show_prompt_before_closing_tabs<br>show_toolbar_history_button |
| default_search_provider | [default_search_provider] habilitado |
| Tela inteira | Permitido |
| home page | Homepage_url |
| homepage_is_newtabpage | homepage_is_newtabpage |
| Sessão | restore_on_startup<br>startup_urls |
| Extensões | Extensões: configurações |

## <a name="1-download-an-example-initial_preferences-file"></a>1: Baixar um arquivo de initial_preferences exemplo

Para começar, baixe o arquivo "Política" na página [Microsoft Edge Enterprise destino](https://www.microsoft.com/edge/business/download). Extraia os arquivos no download e abra o *arquivo initial_preferences* na pasta *de* exemplos. A próxima captura de tela mostra as opções de arquivo de política que estão disponíveis para download

:::image type="content" source="media/initial-preferences-support-on-microsoft-edge-browser/edge-policy-files.png" alt-text="Microsoft Edge de política disponíveis para download.":::

## <a name="2-customize-and-validate-the-initial_preferences-file"></a>2: Personalizar e validar o initial_preferences arquivo

Personalize as configurações de preferências no arquivo ** initial_preferences baixado e valide as alterações para garantir que não haja erros no código JSON. Se você encontrar erros, verifique a sintaxe e a estrutura do arquivo *initial_preferences* , faça correções e verifique-o novamente. Algumas ferramentas de exemplo para validar JSON, Ferramentas [JSON](https://jsonformatter.org/) Online ou [edição JSON em Visual Studio Code](https://code.visualstudio.com/docs/languages/json).

## <a name="3-deploy-preferences-to-users-computer"></a>3: Implantar preferências no computador dos usuários

Implante o *initial_preferences* nos dispositivos dos usuários ao mesmo tempo em que o Microsoft Edge é implantado e coloque o arquivo no seguinte local no dispositivo.

### <a name="windows-amd64-and-arm64"></a>Windows (AMD64 e ARM64)

| Canal | Location |
| - | - |
| Estável | `"C:\Program Files (x86)\Microsoft\Edge\Application"` |
| Beta | `"C:\Program Files (x86)\Microsoft\Edge Beta\Application"` |
|Canary | `"%LOCALAPPDATA%\Microsoft\Edge SxS\Application"` |
| Dev | `"C:\Program Files (x86)\Microsoft\Edge Dev\Application"` |

> [!NOTE]
> O *initial_preferences* precisa ser implantado na mesma pasta que o arquivo *msedge.exe* nos computadores Windows usuários.  

### <a name="macos"></a>macOS

| Canal | Location |
| - | - |
| Estável | `"~/Library/Application Support/Microsoft Edge/Microsoft Edge Initial Preferences"` |
| Beta | `“~/Library/Application Support/Microsoft Edge Beta/Microsoft Edge Initial Preferences"` |
| Canary | `“~/Library/Application Support/Microsoft Edge Canary/Microsoft Edge Initial Preferences"` |
| Dev | `"~/Library/Application Support/Microsoft Edge Dev/Microsoft Edge Initial Preferences"` |

## <a name="important-notes-msi--pkg-deployment-and-initial_preferences-interaction"></a>Observações importantes: Implantação de MSI/Pkg *e initial_preferences* interação

As preferências iniciais só entrarão em vigor depois que *o arquivo initial_preferences* for implantado antes da primeira execução do navegador pelos usuários finais.  

## <a name="see-also"></a>Consulte também

- [O *arquivo initial_prefrences* modelo de exemplo](/edge/business/download)
