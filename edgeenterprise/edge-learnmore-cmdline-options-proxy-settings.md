---
title: Configurações de proxy do Microsoft Edge
ms.author: brianalt
author: dan-wesley
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: 'Usar opções de linha de comando para definir as configurações de proxy '
ms.openlocfilehash: 5a7a422813b751d2ed120bc5a287564600dba8e1
ms.sourcegitcommit: 592f6e40b13e28af588473b2a75c3ae697e5db2d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/05/2022
ms.locfileid: "12505484"
---
# <a name="how-to-use-microsoft-edge-command-line-options-to-configure-proxy-settings"></a>Como usar as opções de linha de comando do Microsoft Edge para definir as configurações de proxy

Este artigo descreve como você pode usar as opções de linha de comando para substituir as configurações de rede do sistema padrão.

>[!NOTE]
>Este artigo aplica-se ao Microsoft Edge versão 77 ou posterior.

## <a name="system-network-settings"></a>Configurações de rede do sistema

Por padrão, a pilha de rede do Microsoft Edge usa as configurações de rede do sistema. Essas configurações incluem as *configurações de proxy* e os *repositórios de certificados e chaves privadas*.

Há cenários em que os usuários solicitam uma alternativa ao uso das configurações padrão de proxy do sistema. Para dar suporte a esses cenários, o Microsoft Edge é compatível com opções de linha de comando que você pode usar para definir configurações de proxy personalizadas.

Essas opções de linha de comando correspondem às seguintes políticas no grupo **Servidor de proxy**:

- [ProxyBypassList](./microsoft-edge-policies.md#proxybypasslist)
- [ProxyMode](./microsoft-edge-policies.md#proxymode)
- [ProxyPacUrl](./microsoft-edge-policies.md#proxypacurl)
- [ProxyServer](./microsoft-edge-policies.md#proxyserver)
- [ProxySettings](./microsoft-edge-policies.md#proxysettings)

## <a name="command-line-options-for-proxy-settings"></a>Opções de linha de comando para configurações de proxy

O Microsoft Edge dá suporte às seguintes opções de linha de comando relacionadas ao proxy.

 **`--no-proxy-server`**
 
Informa ao Microsoft Edge para não usar um Proxy, mesmo que o sistema esteja de alguma forma configurado para usar um. Ela substitui todas as outras configurações de proxy fornecidas.

**`--proxy-auto-detect`**

Informa ao Microsoft Edge para tentar detectar automaticamente sua configuração de proxy. Esse argumento será ignorado se `--proxy-server` estiver configurado.

**`--proxy-server=<scheme>=<uri>[:<port>][;...] | <uri>[:<port>] | "direct://"`**

Informa ao Microsoft Edge para usar uma configuração de proxy personalizada. Você pode especificar uma configuração de proxy personalizada de três maneiras.

1. Forneça um mapeamento separado por ponto-e-vírgula de esquemas de lista para pares de url/porta. Por exemplo, `--proxy-server="http=proxy1:8080;ftp=ftpproxy"` diz ao Microsoft Edge para usar o proxy HTTP "proxy1:8080" para URLs de http e o proxy HTTP "ftpproxy:80" para URLs de ftp.
2. Fornecendo um único uri com porta opcional a ser usada para todas as URLs. Por exemplo, `--proxy-server="proxy2:8080"` usará o proxy em "proxy2:8080" para todo o tráfego.
3. Usando o valor especial "direct://". Por exemplo, `--proxy-server="direct://"` fará com que nenhuma conexão use um proxy. 

>[!NOTE]
>Você pode configurar o Microsoft Edge para tentar usar um proxy e fazer fallback para entrar diretamente se o proxy não estiver disponível. Por exemplo, `--proxy-server="http://proxy2:8080,direct://`.

**`--proxy-bypass-list=(<trailing_domain>|<ip-address>)[:<port>][;...]`**

Informa ao Microsoft Edge para ignorar qualquer proxy especificado para a lista de hosts separados por ponto-e-vírgula especificada. Esse sinalizador deve ser usado com `--proxy-server`.

>[!NOTE]
>A correspondência de domínio à direita não requer separadores ".", "\*microsoft.com" corresponderá a "imicrosoft.com". Por exemplo, `--proxy-server="proxy2:8080" --proxy-bypass-list="*.microsoft.com;*example.com;127.0.0.1:8080"` usará o servidor proxy "proxy2" na porta 8080 para todos os hosts, exceto as solicitações para \*.microsoft.com, example.com e 127.0.0.1 na porta 8080. No exemplo anterior, as solicitações de imicrosoft.com ainda serão mediadas por proxy. No entanto, as solicitações de iexample.com ignoram o proxy porque \* example.com foi especificado em vez de \*. example.com.

**`--proxy-pac-url=<pac-file-url>`**

Informa ao Microsoft Edge para usar o arquivo PAC na URL especificada. Por exemplo, `--proxy-pac-url="https://wpad/proxy.pac"` informa o Microsoft Edge para resolver informações de proxy de solicitações de URL usando o arquivo **proxy.pac**.

## <a name="content-license"></a>Licença de conteúdo

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e compartilhado pela Chromium.org e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional](http://creativecommons.org/licenses/by/4.0/). A página original pode ser encontrada [aqui](https://www.chromium.org/developers/design-documents/network-settings#TOC-Command-line-options-for-proxy-sett).
  
<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br />Esse trabalho é licenciado sob uma <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons</a>.

## <a name="see-also"></a>Consulte também

- Para ver as configurações avançadas e as opções adicionais, consulte a [documentação do proxy](https://chromium.googlesource.com/chromium/src/+/HEAD/net/docs/proxy.md) no projeto Chromium Open Source.
- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)