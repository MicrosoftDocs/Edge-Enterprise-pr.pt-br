---
title: Formato de filtro para políticas de URL do Microsoft Edge
ms.author: brianalt
author: dan-wesley
manager: srugh
ms.date: 05/01/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Saiba mais sobre o formato de filtro usado para as políticas URLBlocklist e URLAllowlist do Microsoft Edge.
ms.openlocfilehash: 5a0eff1ca7be17fccd1087716d426b13ea302847
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979065"
---
# Formato de filtro para políticas baseadas em lista de URL

Este artigo descreve o formato de filtro usado para as políticas baseadas em lista de URLs do Microsoft Edge (por exemplo, as políticas [URLBlocklist](microsoft-edge-policies.md#urlblocklist), [URLAllowList](microsoft-edge-policies.md#urlallowlist) e [CertificateTransparencyEnforcementDisabledForUrls](microsoft-edge-policies.md#certificatetransparencyenforcementdisabledforurls).

> [!NOTE]
> Este artigo aplica-se ao Microsoft Edge versão 77 ou posterior.

##  <a name="the-filter-format"></a>O formato de filtro

O formato de filtro é:

```
    [scheme://][.]host[:port][/path][@query]
```

Os campos no formato de filtro são:

| Campo | Descrição |
| --- | --- |
| **esquema** (*opcional*) | Ele pode ser http://, https://, ftp://, edge:// etc. |
| **host** (*necessário*) | Ele deve ser um nome de host ou endereço IP válido e você pode usar um caractere curinga ("\*"). Para desabilitar a correspondência de subdomínio, inclua um ponto opcional (".") antes do **host**. |
| **porta** (*opcional*) | Os valores válidos variam de 1 a 65535. |
| **caminho** (*opcional*) | Você pode usar qualquer cadeia de caracteres no caminho. |
| **consulta** (*opcional*) | A **consulta** é de tokens chave-valor ou somente chave-valor separados por um "E" comercial ("&"). Separe os tokens de chave-valor com um sinal de igual ("="). Para indicar uma correspondência de prefixo, você pode usar um asterisco ("\*") no final da **consulta**. |

##  <a name="comparing-the-filter-format-to-the-url-format"></a>Como comprar o formato de filtro ao formato de URL

O formato do filtro é parecido com o formato da URL, exceto pelo seguinte:

- Se você incluir "user:pass", ele será ignorado. Por exemplo, http://user:pass@ftp.contoso.com/pub/example.iso.
- Se você incluir um identificador de fragmento ("#"), ele e tudo que vier depois dele serão ignorados.
- Você pode usar um caractere curinga ("*") como o **host** e pode prefixá-lo com um ponto (".").
- Você pode usar uma barra ("/") ou um ponto (".") como sufixo para o **host**. Nesse caso, o sufixo é ignorado.

##  <a name="filter-selection-criteria"></a>Critérios de seleção de filtro

O filtro selecionado para uma URL é a correspondência mais específica encontrada após o processamento das seguintes regras de seleção de filtro:

1. Os filtros com a correspondência de **host** mais longa são selecionados primeiro.
2. Dos filtros selecionados, todos os filtros com um esquema ou porta sem correspondência são descartados.
3. Nos filtros restantes, o filtro com o **caminho** de correspondência mais longo é selecionado.
4. Nos filtros restantes, o filtro com o conjunto de tokens de consulta mais longo é selecionado. Nesta etapa, o filtro de lista de permissões terá precedência sobre o filtro de lista de bloqueios se os dois filtros tiverem o mesmo tamanho de **caminho** e número de tokens de **consulta**.
5. Se não houver um filtro válido restante, o subdomínio mais à esquerda será removido do **host** e o processo de seleção será reiniciado na etapa 1. O **host** de asterisco especial ("*") é o último pesquisado e corresponde a todos os hosts.
6. Se um filtro estiver disponível, ele bloqueará ou permitirá a solicitação de URL.

   >[!NOTE]
   >O comportamento padrão é permitir a solicitação de URL se nenhum filtro corresponder.

##  <a name="example-filter-selection-criteria"></a>Critérios de seleção de filtro de exemplo

Neste exemplo, ao procurar uma correspondência para "https://sub.contoso.com/docs" a seleção de filtro:

1. Procurará um filtro para "sub.contoso.com". Se encontrar um filtro, a pesquisa prosseguirá para a etapa 2. Se um filtro não for encontrado, ela tentará novamente com "contoso.com", "com" e, por fim, "".
2. Nos filtros selecionados, qualquer um que não tenha "http" no **esquema** será removido.
3. Dos filtros restantes, qualquer um que tenha um número de porta exato que não seja "80" será removido.
4. Dos filtros restantes, qualquer um que não tenha "/docs" como prefixo do **caminho** será removido.
5. Dos filtros restantes, o filtro com o maior prefixo de caminho será selecionado e aplicado. Se um filtro não for encontrado, o processo de seleção será reiniciado novamente na etapa 1. O processo é repetido com o próximo subdomínio.

###  <a name="additional-filter-information"></a>Informações adicionais de filtro

Se um filtro tiver um ponto (".") prefixando o **host**, então somente as correspondências de **host** exatas serão filtradas. Por exemplo:

- “contoso.com” (sem ponto) corresponderá a “contoso.com”, “www.contoso.com” e “sub.www.contoso.com”
- “.www.contoso.com” (com um prefixo de ponto) só corresponderá a “www.contoso.com”

Você pode usar um **esquema** padrão ou de cliente. Os esquemas padrão com suporte incluem:

- _about_, _blob_, _content_, _edge_, _cid_, _data_, _file_, _filesystem_, _ftp_, _gopher_, _http_, _https_, _javascript_, _mailto_, _ws_ e _wss_.

Qualquer outro **esquema** será tratado como um **esquema** personalizado, mas somente os padrões _schema:*_ e _schema://*_ são permitidos. Por exemplo:

- “custom:*” ou “custom://*” corresponderá a “custom:app”
- “custom:app” ou “custom://app” são inválidos

**schema** e **host** não diferenciam maiúsculas de minúsculas. Por exemplo:

- O filtro “http://contoso.com” corresponde a “HTTP://contoso.com”, “http://contoso.COM” e “http://contoso.com”

**path** e **query** diferenciam maiúsculas de minúsculas. Por exemplo:

- O filtro “http://contoso.com/path?query=A” não corresponde a “http://contoso.com/Path?query=A” ou “http://contoso.com/path?Query=A”. Ele corresponde a “http://contoso.COM/path?query=A”.

##  <a name="content-license"></a>Licença de conteúdo

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e compartilhado pela Chromium.org e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional](http://creativecommons.org/licenses/by/4.0/). A página original do [Chromium pode ser encontrada aqui](https://www.chromium.org/administrators/url-blacklist-filter-format).
  
<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br />Esse trabalho é licenciado sob uma <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons</a>.

##  <a name="see-also"></a>Consulte também

- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
