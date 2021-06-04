---
title: Sintaxe da expressão regular 2
ms.author: comanea
author: dan-wesley
manager: seanlyn
ms.date: 06/09/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Sintaxe da expressão regular 2
ms.openlocfilehash: 9654a25d2c0474601fb719b145ebb1f59241a6d9
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979058"
---
# Sintaxe da Expressão Regular 2 (re2.h)

As expressões regulares são uma notação para descrever os conjuntos de cadeias de caracteres. Quando uma cadeia de caracteres está no conjunto descrito por uma expressão regular, costumamos dizer que a expressão regular corresponde à cadeia.

A expressão regular mais simples é um único caractere literal. Exceto pelos metacaracteres, como *\ * *? ()|*, os caracteres correspondem a si próprios. Para corresponder a um metacaractere, entre com uma barra invertida: \+ corresponde a um caractere literal de adição.

Duas expressões regulares podem ser alteradas ou concatenadas para formar uma nova expressão regular se: *e<sub>1</sub>* corresponde a _s_ e *e<sub>2</sub>* corresponde a _t_, nesse caso, *e<sub>1</sub>* | *e<sub>2</sub>* correspondem a _s_ ou _t_, e *e<sub>1</sub>* *e<sub>2</sub>*  correspondem a _st_.

Os metacaracteres _\*_, _+_ e _?_ são operadores de repetição: *e<sub>1</sub>* _\*_ corresponde a uma cadeia de caracteres zero ou mais (possivelmente diferentes), cada uma das quais correspondem a *e<sub>1</sub>*; *e<sub>1</sub>* _+_ corresponde a um ou mais; *e<sub>1</sub>* _?_ iguala zero ou um.

A precedência do operador, da associação mais fraca para a mais forte, é primeiro a alternância, depois a concatenação e, por fim, os operadores de repetição. Os parênteses explícitos podem ser usados para forçar diferentes significados, como nas expressões aritméticas. Alguns exemplos: _ab|cd_ é equivalente a _(ab)|(cd)_ ; _ab\*_ é equivalente a _a(b\*)_ .

A sintaxe descrita até o momento é a maior parte da sintaxe de expressão regular _egrep_ do Unix. Esse subconjunto é suficiente para descrever todas as linguagens regulares: uma linguagem regular é um conjunto de cadeias de caracteres que podem ser correspondidos em uma única passagem do texto usando apenas uma quantidade fixa de memória. As facilidades de expressão regular mais recentes (notadamente Perl e aquelas que o copiaram) adicionaram muitos novos operadores e sequências de escape, o que torna as expressões regulares mais concisas e, às vezes, mais irregulares, mas, geralmente, não mais robustas.

Esta página lista a sintaxe de expressão regular aceita por RE2.

Ela também lista algumas sintaxes aceitas pela PCRE, PERL e VIM.

##  <a name="syntax-tables"></a>Tabelas de sintaxe

| Tipos de expressões de caractere único | Exemplos |
| --- | --- |
| qualquer caractere, possivelmente incluindo nova linha (s=true) | . |
| classe de caractere | [xyz] |
| classe de caractere negada | [^xyz] |
| classe de caractere Perl ([link](#user-content-perl)) | \d |
| classe de caractere Perl negada | \D |
| classe de caractere ASCII ([link](#user-content-ascii)) | [[:alpha:]] |
| classe de caractere ASCII negada | [[:^alpha:]] |
| Classe de caractere unicode (nome de uma letra) | \pN |
| classe de caractere Unicode | \p{Greek} |
| classe de caractere Unicode negada (nome de uma letra) | \PN |
| classe de caractere Unicode negada | \P{Greek} |

| | Compostos |
| --- | --- |
| xy | x seguido por y |
| x\|y | x ou y (prefira x) |

| | Repetições |
| --- | --- |
| x\* | zero ou mais x, prefira mais |
| x+ | um ou mais x, prefira mais |
| x? | zero ou um x, prefira um |
| x{n,m} | n ou n + 1 ou ... ou m x, prefira mais |
| x{n,} | n ou mais x, prefira mais |
| x{n} | exatamente n x |
| x\*? | zero ou mais x, prefira menos |
| x+? | um ou mais x, prefira menos |
| x?? | zero ou um x, prefira zero |
| x{n,m}? | n ou n + 1 ou ... ou m x, prefira menos |
| x{n,}? | n ou mais x, prefira menos |
| x{n}? | exatamente n x |
| x{} | (≡ x\*) (SEM SUPORTE) VIM |
| x{-} | (≡ x\*?) (SEM SUPORTE) VIM |
| x{-n} | (≡ x{n}?) (SEM SUPORTE) VIM |
| x= | (≡ x?) (SEM SUPORTE) VIM |

Restrições de implementação: os formulários de contagem x{n, m}, x{n,} e x{n} rejeitam formulários que criam uma contagem mínima ou máxima de repetição acima de 1000. As repetições ilimitadas não estão sujeitas a essa restrição.

| | Repetições possessivas |
| --- | --- |
| x\*+ | zero ou mais x, possessivas (SEM SUPORTE) |
| x++ | um ou mais x, possessivas (SEM SUPORTE) |
| x?+ | zero ou mais x, possessivas (SEM SUPORTE) |
| x{n,m}+ | n ou ... ou m x, possessivas (SEM SUPORTE) |
| x{n,}+ | n ou mais x, possessivas (SEM SUPORTE) |
| x{n}+ | exatamente n x, possessivas (SEM SUPORTE) |

| | Agrupamento |
| --- | --- |
| (re) | grupo de captura numerada (subcorrespondência) |
| (?P&lt;name&gt;re) | grupo de captura numerada chamado &amp; (subcorrespondência) |
| (?&lt;name&gt;re) | grupo de captura numerada chamado &amp; (subcorrespondência) (SEM SUPORTE) |
| (?&#39;name&#39;re) | grupo de captura numerada chamado &amp; (subcorrespondência) (SEM SUPORTE) |
| (?:re) | grupo de não captura |
| (?flags) | definir sinalizadores no grupo atual; não captura |
| (?flags:re) | Defina sinalizadores durante a re; não captura |
| (?#text) | comentário (sem suporte) |
| (?\|x\|y\|z) | redefinição de numeração de ramificação (SEM SUPORTE) |
| (?&gt;re) | possessivos correspondentes à re (SEM SUPORTE) |
| re@&gt; | possessivos correspondentes à re (SEM SUPORTE) |
| %(re) | grupo de não captura (SEM SUPORTE) VIM |

| | Sinalizadores |
| --- | --- |
| i | não diferencia maiúsculas de minúsculas (padrão falso) |
| m | modo de várias linhas: ^ e $ correspondem ao início/término da linha, além do inicio/término do texto (falso padrão) |
| s | let . Corresponde a \n (padrão falso) |
| U | ungreedy: mude o significado de x\* e x\*?, x+ e x+?, etc (falso padrão) |

A sintaxe do sinalizador é xyz (definir) or -xyz (desmarcar) or xy-z (definir xy, desmarcar z)

|  | Cadeias de caracteres vazia |
| --- | --- |
| ^ | no início do texto ou linha (m=true) |
| $ | no final do texto (como \z não \Z) ou linha (m=true) |
| \A | no início do texto |
| \b | em um limite de palavra ASCII (\w em um lado e \W, \A ou \z no outro) |
| \B | não presente em um limite de palavra ASCII |
| \g | ao início do subtexto sendo pesquisado (SEM SUPORTE) PCRE |
| \G | ao final da última correspondência (SEM SUPORTE) PERL |
| \Z | ao final do texto ou antes de nova linha ao final do texto (SEM SUPORTE) |
| \z | ao final do texto |
| (?=re) | antes do texto correspondente à re (SEM SUPORTE) |
| (?!re) | antes do texto não correspondente à re (SEM SUPORTE) |
| (?&lt;=re) | depois do texto correspondente à re (SEM SUPORTE) |
| (?&lt;!re) | depois do texto não correspondente à re (SEM SUPORTE) |
| re&amp; | antes do texto correspondente à re (SEM SUPORTE) VIM |
| re@= | antes do texto correspondente à re (SEM SUPORTE) VIM |
| re@! | antes do texto não correspondente à re (SEM SUPORTE) VIM |
| re@&lt;= | depois do texto correspondente à re (SEM SUPORTE) VIM |
| re@&lt;! | depois do texto não correspondente à re (SEM SUPORTE) VIM |
| \zs | define o início da correspondência (= \K) (SEM SUPORTE) VIM |
| \ze | define o final da correspondência (SEM SUPORTE) VIM |
| \%^ | início do arquivo (SEM SUPORTE) VIM |
| \%$ | final do arquivo (SEM SUPORTE) VIM |
| \%V | na tela (SEM SUPORTE) VIM |
| \%# | posição do cursor (SEM SUPORTE) VIM |
| \%&#39;m | marcar posição do m (SEM SUPORTE) VIM |
| \%23l | na linha 23 (SEM SUPORTE) VIM |
| \%23c | na coluna 23 (SEM SUPORTE) VIM |
| \%23v | na coluna virtual 23 (SEM SUPORTE) VIM |

|  | Sequencias de escape |
| --- | --- |
| \a | sino (≡ \007) |
| \f | feed de formulário (≡ \014) |
| \t | guia horizontal (≡ \011) |
| \n | nova linha (≡ \012) |
| \r | retorno de carro (≡ \015) |
| \v | Caractere de tabulação vertical (≡ \013) |
| \* | literal \*, para qualquer caractere de pontuação \* |
| \123 | código de caractere octal (até três dígitos) |
| \x7F | código de caractere hex (exatamente dois dígitos) |
| \x{10FFFF} | contagem de caracteres hex |
| \C | combinar um byte único mesmo no modo UTF-8 |
| \Q...\E | texto literal... mesmo se... possui pontuação |
| \1 | referência anterior (SEM SUPORTE) |
| \b | backspace (SEM SUPORTE) (usar \010) |
| \cK | caratere de controle ^K (SEM SUPORTE) (usar \001 etc) |
| \e | escape (SEM SUPORTE) (usar \033) |
| \g1 | referência anterior (SEM SUPORTE) |
| \g{1} | referência anterior (SEM SUPORTE) |
| \g{+1} | referência anterior (SEM SUPORTE) |
| \g{-1} | referência anterior (SEM SUPORTE) |
| \g{name} | referência nomeada (SEM SUPORTE) |
| \g&lt;name&gt; | chamada de sub-rotina (SEM SUPORTE) |
| \g&#39;name&#39; | chamada de sub-rotina (SEM SUPORTE) |
| \k&lt;nome&gt; | referência nomeada (SEM SUPORTE) |
| \k&#39;name&#39; | referência nomeada (SEM SUPORTE) |
| \lX | X em minúsculo (SEM SUPORTE) |
| \ux | X em maiúsculo (SEM SUPORTE) |
| \L...\E | texto em minúscula ... (SEM SUPORTE) |
| \K | reiniciar o início de $0 (SEM SUPORTE) |
| \N{name} | caracteres Unicode nomeado (SEM SUPORTE) |
| \R | quebra de linha (SEM SUPORTE) |
| \U...\E | texto em maiúscula ... (SEM SUPORTE) |
| \X | sequência Unicode estendida (SEM SUPORTE) |
| \%d123 | caractere decimal 123 (SEM SUPORTE) VIM |
| \%xFF | caractere hexadecimal FF (SEM SUPORTE) VIM |
| \%o123 | caractere octal 123 (SEM SUPORTE) VIM |
| \%u1234 | caractere Unicode 0x1234 (SEM SUPORTE) VIM |
| \%U12345678 | caractere Unicode 0x12345678 (SEM SUPORTE) VIM |

|  | Elementos de classe de caractere |
| --- | --- |
| x | caractere único |
| A-Z | intervalo de caracteres (inclusivo) |
| \d | classe de caractere Perl |
| [:foo:] | classe de caractere ASCII foo |
| \p{Foo} | classe de caractere Unicode Foo |
| \pF | Classe de caractere Unicode F (nome de uma letra) |

|  | Classes de caractere nomeada como elementos de classe de caractere |
| --- | --- |
| [\d] | dígitos (≡ \d) |
| [^\d] | não são dígitos (≡ \D) |
| [\D] | não são dígitos (≡ \D) |
| [^\D] | não são não dígitos (≡ \d) |
| [[:name:]] | classe ASCII nomeada dentro da classe de caractere (≡ [:name:]) |
| [^[:name:]] | classe ASCII nomeada dentro da classe de caractere negada (≡ [:^name:]) |
| [\p{Name}] | propriedade Unicode nomeada dentro da classe de caractere (≡ \p{Name}) |
| [^\p{Name}] | propriedade Unicode nomeada dentro da classe de caractere negada (≡ \P{Name}) |

| <a name="user-content-perl"></a> | Classes de caracteres Perl (todas somente ASCII) |
| --- | --- |
| \d | dígitos (≡ [0-9]) |
| \D | não são dígitos (≡ [^0-9]) |
| \s | espaço em branco (≡ [\t\n\f\r]) |
| \S | não é espaço em branco (≡ [^\t\n\f\r]) |
| \w | caracteres de palavra (≡ [0-9A-Za-z\_]) |
| \W | não são caracteres de palavra (≡ [^0-9A-Za-z\_]) |
| \h | espaço horizontal (SEM SUPORTE) |
| \H | não é espaço horizontal (SEM SUPORTE) |
| \v | espaço vertical (SEM SUPORTE) |
| \V | não é espaço vertical (SEM SUPORTE) |

|<a name="user-content-ascii"></a>  | classe de caractere ASCII |
| --- | --- |
| [[:alnum:]] | alfanumérico (≡ [0-9A-Za-z]) |
| [[:alpha:]] | alfabético (≡ [A-Za-z]) |
| [[:ascii:]] | ASCII (≡ [\x00-\x7F]) |
| [[:blank:]] | em branco (≡ [\t]) |
| [[:cntrl:]] | controle (≡ [\x00-\x1F\x7F]) |
| [[:digit:]] | dígitos (≡ [0-9]) |
| [[:graph:]] | gráfico (≡ `[!-~]` ≡ `[A-Za-z0-9!&quot;#$%&amp;&#39;()\*+,\-./:;&lt;=&gt;?@[\\\]^_`\` `{\|}~]`) |
| [[:lower:]] | letras em minúscula (≡ [a-z]) |
| [[:print:]] | imprimível (≡ [-~] ≡ [[:graph:]]) |
| [[:punct:]] | pontuação (≡ [!-/:-@[-`{-~]) |
| [[:space:]] | espaço em branco (≡ [\t\n\v\f\r]) |
| [[:upper:]] | letras em maiúscula (≡ [A-Z]) |
| [[:word:]] | caracteres de palavra (≡ [0-9A-Za-z\_]) |
| [[:xdigit:]] | dígito hex (≡ [0-9A-Fa-f]) |

| | nomes de classe de caractere Unicode -- categoria geral |
| --- | --- |
| C | outros |
| Cc | control |
| Cf | format |
| Cn | pontos de código não atribuídos (SEM SUPORTE) |
| Co | uso privado |
| Cs | substituto |
| L | letra |
| LC | letra em maiúscula (SEM SUPORTE) |
| L&amp; | letra em maiúscula (SEM SUPORTE) |
| Ll | letras em minúscula |
| Lm | letra modificadora |
| Lo | outra letra |
| Lt | primeira letra do título em maiúscula |
| Lu | letra em maiúscula |
| M | marcado |
| Mc | marca de espaçamento |
| Me | marca de circunscrição |
| Mn | marca sem espaçamento |
| N | number |
| Nd | número decimal |
| Nl | número da letra |
| Não | outro número |
| P | pontuação |
| Pc | pontuação do conector |
| Pd | traço |
| Pe | pontuação de fechamento |
| Pf | pontuação final |
| Pi | pontuação inicial |
| Po | outra pontuação |
| Ps | pontuação aberta |
| S | symbol |
| Sc | símbolo de moeda |
| Sk | símbolo modificador |
| Sm | símbolo matemático |
| So | outro símbolo |
| Z | separador |
| Zl | separador de linha |
| Zp | separador de parágrafo |
| Zs | separador de espaço |

| nomes de classe de caractere Unicode -- scripts |
| --- |
| Adlam |
| Ahom |
| Anatolian\_Hieroglyphs |
| Árabe |
| armênio |
| Avestan |
| Balinês |
| Bamum |
| Bassa\_Vah |
| Batak |
| Bengali |
| Bhaiksuki |
| Bopomofo |
| Brahmi |
| Braille |
| Buginese |
| Buhid |
| Canadense\_Aborígine |
| Carian |
| Cáucaso\_Albanês |
| Cakm |
| Cham |
| Cheroqui |
| Chorasmian |
| Comum |
| Coptas |
| Cuneiforme |
| Cipriota |
| Cirílica |
| Deseret |
| Devanágari |
| Dives\_Akuru |
| Dogra |
| Duployan |
| Hieróglifos\_Egípcios |
| Elbasan |
| Elimaico |
| Etíope |
| georgiano |
| Glagolítico |
| Gótica |
| Grantha |
| Grego |
| Guzerate |
| Gunjala\_Gondi |
| Gurmukhi |
| Hangul |
| Hangul |
| Hanifi\_Rohingya |
| Hanunoo |
| Hatran |
| Hebraico |
| Hiragana |
| Aramaico\_Imperial |
| Herdado |
| Pahlavi\_Inscricional |
| Parthian\_Inscricional |
| Javanês |
| Kthi |
| kannada |
| Katakana |
| Kayah\_Li |
| Kharoshthi |
| Khitan\_Small\_Script |
| Khmer |
| Khojki |
| Khudawadi |
| Lao |
| Latino |
| Lepcha |
| Limbu |
| Linear\_A |
| Linear\_B |
| Lisu |
| Lício |
| Lídio |
| Mahajani |
| Makasar |
| malaiala |
| Mandaico |
| Maniqueano |
| Marchen |
| Masaram\_Gondi |
| Medefaidrin |
| Meitei\_Mayek |
| Mende\_Kikakui |
| Meroíticos\_Cursivos |
| Hieróglifos\_Meroíticos |
| Miao |
| Modi |
| Mongol |
| Mro |
| Multani |
| Myanmar |
| Nabateu |
| Nandinagari |
| Tai\_Lue\_Novo |
| Newa |
| Nko |
| Nushu |
| Nyiakeng\_Puachue\_Hmong |
| Ogham |
| Ol\_Chiki |
| Húngaro\_Antigo |
| Itálico\_Antigo |
| Árabe\_Meridional\_Antigo |
| Permic\_Antigo |
| Persa\_Antigo |
| Sogdian\_Antigo |
| Árabe\_Meridional\_Antigo |
| Túrquico\_Antigo |
| Oriya |
| Osage |
| Osmanli |
| Pahawh\_Hmong |
| Palmirena |
| Pau\_Cin\_Hau |
| Phags\_Pa |
| Fenício |
| Psalter\_Pahlavi |
| Rejang |
| Rúnica |
| Samaritano |
| Saurashtra |
| Sharada |
| Shaviano |
| Siddham |
| SignWriting |
| cingalês |
| Sogdiano |
| Sora\_Sompeng |
| Soyombo |
| Sundanês |
| Syloti\_Nagri |
| Siríaco |
| Filipino |
| Tagbanwa |
| Tai\_Le |
| Tai\_Tham |
| Tai\_Viet |
| Takri |
| Tâmil |
| Tangut |
| Télugo |
| Thaana |
| Tailandês |
| Tibetano |
| Tifinagh |
| Tirhuta |
| Ugarítico |
| Vai |
| Wancho |
| Warang\_Citi |
| Yezidi |
| Yi |
| Zanabazar\_Square |

|  | classes de caractere VIM |
| --- | --- |
| \i | caractere identificador (SEM SUPORTE) VIM |
| \I | \i, exceto dígitos (SEM SUPORTE) VIM |
| \k | caractere de palavra-chave (SEM SUPORTE) VIM |
| \K | \k, exceto dígitos (SEM SUPORTE) VIM |
| \f | caractere de nome de arquivo (SEM SUPORTE) VIM |
| \F | \f, exceto dígitos (SEM SUPORTE) VIM |
| \p | caractere imprimível (SEM SUPORTE) VIM |
| \P | \p, exceto dígitos (SEM SUPORTE) VIM |
| \s | caractere de espaço em branco (≡ [\t]) (SEM SUPORTE) VIM |
| \S | caractere de espaço não em branco (≡ [^ \t]) (SEM SUPORTE) VIM |
| \d | dígitos (≡ [0-9]) VIM |
| \D | Não é \d VIM |
| \x | dígitos hexadecimais (≡ [0-9A-Fa-f]) (SEM SUPORTE) VIM |
| \X | não é \x (SEM SUPORTE) VIM |
| \o | dígitos octais (≡ [0-7]) (SEM SUPORTE) VIM |
| \O | não é \o (SEM SUPORTE) VIM |
| \w | caractere de palavra VIM |
| \W | Não é \w VIM |
| \h | cabeçalho do caractere de palavra (SEM SUPORTE) VIM |
| \H | não é \h (SEM SUPORTE) VIM |
| \a | Alfabético (SEM SUPORTE) VIM |
| \A | não é \a (SEM SUPORTE) VIM |
| \l | em minúsculas (SEM SUPORTE) VIM |
| \L | não minúsculas (SEM SUPORTE) VIM |
| \u | em maiúsculas (SEM SUPORTE) VIM |
| \U | não maiúsculas (SEM SUPORTE) VIM |
| \_x | \x mais nova linha, para qualquer x (SEM SUPORTE) VIM |
| \c | ignorar maiúsculas e minúsculas (SEM SUPORTE) VIM |
| \C | diferenciar maiúsculas e minúsculas (SEM SUPORTE) VIM |
| \m | magic (SEM SUPORTE) VIM |
| \M | nomagic (SEM SUPORTE) VIM |
| \v | verymagic (SEM SUPORTE) VIM |
| \V | verynomagic (SEM SUPORTE) VIM |
| \Z | ignorar diferenças na combinação de caracteres Unicode (SEM SUPORTE) VIM |

|  | Magic |
| --- | --- |
| (?{code}) | código Perl arbitrário (SEM SUPORTE) PERL |
| (??{code}) | código Perl arbitrário adiado (SEM SUPORTE) PERL |
| (?n) | chamada recursiva para o grupo de captura regexp n (SEM SUPORTE) |
| (?+n) | chamada recursiva para o grupo de captura regexp n (SEM SUPORTE) |
| (?-n) | chamada recursiva para o grupo de captura regexp -n (SEM SUPORTE) |
| (?C) | PCRE callout (SEM SUPORTE) PCRE |
| (?R) | chamada recursiva para regexp inteiro (≡ (?0)) (SEM SUPORTE) |
| (?&amp;name) | chamada recursiva para o grupo nomeado (SEM SUPORTE) |
| (?P=name) | referência nomeada (SEM SUPORTE) |
| (?P&gt;name) | chamada recursiva para o grupo nomeado (SEM SUPORTE) |
| (?(cond)true|false) | ramificação condicional (SEM SUPORTE) |
| (?(cond)true) | ramificação condicional (SEM SUPORTE) |
| (\*ACCEPT) | tornar regexps mais semelhantes ao prólogo (SEM SUPORTE) |
| (\*COMMIT) | (SEM SUPORTE) |
| (\*F) | (SEM SUPORTE) |
| (\*FAIL) | (SEM SUPORTE) |
| (\*MARK) | (SEM SUPORTE) |
| (\*PRUNE) | (SEM SUPORTE) |
| (\*SKIP) | (SEM SUPORTE) |
| (\*THEN) | (SEM SUPORTE) |
| (\*ANY) | definir convenção de nova linha (SEM SUPORTE) |
| (\*ANYCRLF) | (SEM SUPORTE) |
| (\*CR) | (SEM SUPORTE) |
| (\*CRLF) | (SEM SUPORTE) |
| (\*LF) | (SEM SUPORTE) |
| (\*BSR\_ANYCRLF) | definir convenção \R (SEM SUPORTE) |
| (\*BSR\_UNICODE) | (SEM SUPORTE) PCRE |

##  <a name="content-license"></a>Licença de conteúdo

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e compartilhado pela Chromium.org e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional](http://creativecommons.org/licenses/by/4.0/). A página original pode ser encontrada [aqui](https://github.com/google/re2/wiki/Syntax).
  
<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br />Esse trabalho é licenciado sob uma <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons</a>.

##  <a name="see-also"></a>Consulte também

- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)