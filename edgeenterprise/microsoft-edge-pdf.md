---
title: Leitor de PDF no Microsoft Edge
ms.author: adigan
author: dan-wesley
manager: balajek
ms.date: 06/28/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Saiba mais sobre o leitor de PDF no Microsoft Edge.
ms.openlocfilehash: 0b1cffceb63c1829c39bdd3fa658df2e5f776584
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/09/2021
ms.locfileid: "11643177"
---
# <a name="pdf-reader-in-microsoft-edge"></a>Leitor de PDF no Microsoft Edge

Arquivos PDF fazem grande parte do nosso dia a dia. Eles estão disponíveis sob a forma de contratos e acordos, boletins informativos, formulários, artigos de pesquisa, currículos, etc. Esses arquivos destacam a necessidade de um leitor de PDF confiável, seguro e eficiente que possa ser adotado pelas empresas.

O Microsoft Edge acompanha um leitor de PDF interno que permite que você abra os arquivos PDF locais, arquivos PDF on-line ou arquivos PDF inseridos nas páginas da Web. Você pode fazer anotações nesses arquivos com tinta e destaque. Esse leitor de PDF oferece aos usuários uma única aplicação para atender às necessidades da página Web e do documento PDF. O leitor de PDF do Microsoft Edge é uma aplicação segura e confiável que funciona em todas as plataformas de área de trabalho do Windows e do MacOS.

> [!NOTE]
> Este artigo se aplica ao Microsoft Edge versão 77 ou posteriores.

## <a name="prerequisites-support-and-constraints"></a>Pré-requisitos, suporte e restrições

A tabela a seguir mostra quais canais e versões do Microsoft Edge oferecem suporte a cada recurso do leitor de PDF.

| Recurso | Versão de canal estável |
|---------|------------------------|
| Exibir e imprimir arquivos PDF locais, on-line e incorporados | 79.0.309.71                |
| Preenchimento do formulário básico<br>(Os formulários JavaScript não possuem suporte) | 79.0.309.71           |
|Sumário| 86.0.622.38 |
| Visão da página |Sendo promovido agora nos canais [Microsoft Edge Insider](https://www.microsoftedgeinsider.com/) |
| Modo navegação com cursor |87.0.664.41 |
| Escrita à tinta  | 80.0.361.48            |
| Personalização de tinta | 83.0.478.54  |
| Highlight  | 81.0.416.53         |
| Notas de texto | Sendo promovido agora nos canais [Microsoft Edge Insider](https://www.microsoftedgeinsider.com/) |
| Ler em voz alta | 84.0.522.63  |
| Exibir arquivos protegidos da Proteção de Informações da Microsoft (MIP) | Suporte ao Windows na versão 80.0.361.48<br>Suporte ao Mac na versão 81.0.416.53 |
|  Visualizar arquivos protegidos por IRM (Gerenciamento de Direitos de Informação)  | 83.0.478.37            |
| Visualizar e validar Assinaturas Digitais | Disponível nos canais Canary e Dev. Sendo trabalhado ativamente. |

### <a name="constraints"></a>Restrições

Observe as seguintes restrições para o leitor de PDF atual:

-  A Arquitetura de formulários XML (XFA)é um formato herdado de formulários que não possui suporte no Microsoft Edge.
-  A documentação relacionada com cenários de Acessibilidade que atualmente não possuem suporte pode ser encontrada no blog [Relatório de conformidade de acessibilidade da Microsoft](https://cloudblogs.microsoft.com/industry-blog/government/2018/09/11/accessibility-conformance-reports/).

## <a name="features"></a>Recursos

O leitor de PDF, integrado ao Microsoft Edge, vem com os recursos básicos de leitura e navegação, como Zoom, Girar, Ajustar à página/largura, ir para a página e pesquisar, entre outros. Eles podem ser acessados por meio de uma barra de ferramentas fixável na parte superior do conteúdo PDF. Esta seção fornece uma visão geral de algumas funções importantes. A próxima captura de tela mostra a barra de ferramentas do leitor de PDF.

![Barra de ferramentas Leitor de PDF](media/microsoft-edge-pdf/pdf-reader-toolbar.png)

### <a name="table-of-contents"></a>Sumário

O sumário permite que os usuários naveguem facilmente por documentos PDF que tenham um índice. Quando um usuário clica no ícone de índice, é aberto um painel de navegação que mostra uma lista das seções e subseções do documento PDF. Em seguida, o usuário pode clicar em qualquer um dos rótulos no painel para navegar até essa seção do documento. O painel permanece aberto pelo tempo necessário e pode ser fechado quando o usuário quiser voltar a ler o documento. A próxima captura de tela mostra o painel de navegação para um documento aberto.

![Navegação do leitor de PDF com o índice](media/microsoft-edge-pdf/pdf-reader-toc.png)

### <a name="page-view"></a>Visão da página

O Microsoft Edge oferece suporte a diferentes exibições para documentos PDF em nossos canais Dev e Canary. Os usuários podem alterar o layout de um documento de uma única exibição de página para duas páginas que são exibidas lado a lado. Para alterar a forma como o documento PDF está sendo exibido, os usuários podem clicar no botão Exibir Página na barra de ferramentas pdf e, em seguida, escolher qualquer exibição que quiserem usar. A exibição de duas páginas é mostrada na próxima captura de tela.

![Leitor de PDF usando o visualização de duas páginas do documento.](media/microsoft-edge-pdf/pdf-reader-page-view.png)

### <a name="caret-mode-browsing"></a>Modo navegação com cursor

A navegação com cursor está disponível para arquivos PDF abertos no Microsoft Edge, o que significa que os usuários podem interagir com arquivos PDF usando o teclado. Se um usuário pressionar a tecla F7 em qualquer lugar do navegador, ele será perguntado se a navegação com cursor deve ser ativada. Se estiver habilitada, a navegação com cursor estará disponível para qualquer conteúdo aberto no navegador, seja arquivos PDF ou páginas da Web. Quando um usuário pressiona F7 novamente, a navegação com cursor é desligada. Quando a navegação com o cursor estiver ativa e o foco estiver no conteúdo, os usuários verão um cursor piscando no arquivo PDF. O cursor também pode ser usado para navegar pelo arquivo ou para selecionar texto pressionando Shift ao mover o cursor. Essa capacidade permite que os usuários facilmente criem elementos como destaques ou interajam com elementos como links, campos de formulário com o teclado. A próxima captura de tela mostra o menu pop-up para ativar a navegação com cursor.

![Menu de leitura de PDF para navegação com cursor.](media/microsoft-edge-pdf/pdf-reader-caret-mode.png)

### <a name="inking"></a>Escrita à tinta

A escrita à tinta nos arquivos em PDF é útil para criar anotações rápidas para facilitar a consulta, o sinal ou o preenchimento de formulários em PDF. Esse recurso já está disponível no Microsoft Edge. Além de arquivos em PDF de escrita à tinta, conforme necessário, você pode usar a cor e a largura do traçado para dar atenção às diferentes partes do arquivo em PDF. A próxima captura de tela mostra como um usuário pode adicionar escrita à tinta em uma página em PDF.

![Página Adicionar escrita à tinta em PDF](media/microsoft-edge-pdf/pdf-reader-inking.png)

### <a name="highlight"></a>Highlight

O leitor de PDF no Microsoft Edge é fornecido com o suporte para adicionar e editar destaques. Para criar um destaque, o usuário só precisa selecionar o texto, clicar com o botão direito nele, selecionar destaques no menu e escolher a cor desejada. Os destaques também podem ser criados usando uma caneta ou teclado. A próxima captura de tela mostra as opções de destaque disponíveis.

![Usar a opção destacar no leitor de PDF](media/microsoft-edge-pdf/pdf-reader-highlight.png)

### <a name="text-notes"></a>Notas de texto

Durante a leitura de um arquivo PDF, as anotações de texto podem ser adicionadas ao texto no arquivo para fazer anotações mais tarde para facilitar a referência.

Os usuários podem adicionar uma nota selecionando a parte do texto para a qual desejam adicionar uma nota e invocando o menu de contexto com o botão direito do mouse. Selecionando a opção **Adicionar Comentário** no menu abrirá uma caixa de texto onde os usuários podem adicionar seus comentários. Eles podem digitar o comentário e depois clicar na marca de verificação para salvar o comentário.

Depois que uma nota é adicionada, o texto selecionado será realçado e um ícone de comentário aparecerá para indicar o comentário. Os usuários podem passar o mouse sobre esse ícone para visualizar o comentário ou clicar nele para abrir e editar a nota.

A próxima captura de tela mostra uma observação sendo adicionada ao texto realçado.

![O leitor de PDF adiciona nota de texto ao documento.](media/microsoft-edge-pdf/pdf-reader-text-note.png)

### <a name="read-aloud"></a>Ler em voz alta

Ler em voz alta para PDF aumenta a conveniência de ouvir o conteúdo pdf enquanto realiza outras tarefas que podem ser importantes para os usuários. Ele também ajuda os alunos de auditoria a se concentrarem no conteúdo, o que facilita o aprendizado. A próxima captura de tela mostra um exemplo de Leitura em voz alta. O destaque mostra o texto que está sendo lido no momento.

![Usar a opção de realçada para Ler em voz alta no leitor de PDF](media/microsoft-edge-pdf/pdf-reader-read-aloud-example.png)

### <a name="protected-pdfs"></a>PDFs protegidos

A [Proteção de informações da Microsoft (MIP)](/microsoft-365/compliance/protect-information?preserve-view=true&view=o365-worldwide) permite que os usuários colaborem com outras pessoas de maneira segura enquanto aderem às políticas de conformidade da sua organização. Depois que um arquivo é protegido, as ações que os usuários podem realizar são determinadas pelas permissões que lhes são atribuídas.

> [!IMPORTANT]
> Uma licença é necessária para o MIP. Para saber mais, confira este [Guia de licenciamento do Microsoft 365.](/office365/servicedescriptions/microsoft-365-service-descriptions/microsoft-365-tenantlevel-services-licensing-guidance/microsoft-365-security-compliance-licensing-guidance#information-protection)

Esses arquivos podem ser abertos diretamente no navegador sem precisar baixar qualquer outro software ou instalar um suplemento. Esse recurso integra a segurança fornecida pelo MIP diretamente no navegador, fornecendo um fluxo de trabalho contínuo.

![Documento em PDF protegido.](media/microsoft-edge-pdf/pdf-reader-protected-pdf2.png)

Além dos arquivos protegidos pelo MIP, os arquivos em [PDF em Gerenciamento de direitos de informação (IRM)](/microsoft-365/compliance/set-up-irm-in-sp-admin-center?preserve-view=true&view=o365-worldwide) protegidos por bibliotecas do SharePoint também podem ser abertos originalmente no navegador.

Com o Microsoft Edge, os usuários podem visualizar os arquivos MIP protegidos localmente, ou na nuvem. Se for salvo localmente, o arquivo pode ser aberto diretamente no navegador. Se o arquivo for aberto de um serviço de nuvem como o SharePoint, talvez o usuário precise usar a opção "Abrir no navegador".

Se o perfil com o qual o usuário se conectou no Microsoft Edge tiver pelo menos permissões de visualização do arquivo, o arquivo será aberto no Microsoft Edge.

![Aviso para salvar a página de PDF do SharePoint é protegido pelo MIP](media/microsoft-edge-pdf/pdf-reader-sharepoint-irm.png)

### <a name="view-and-validate-certificate-based-digital-signatures"></a>Exibir e validar assinaturas digitais baseadas em certificado

Nesse mundo digital, torna-se importante estabelecer a autenticidade e a propriedade do conteúdo no documento. As assinaturas digitais baseadas em certificado são comumente usadas em documentos PDF para garantir que o conteúdo no documento seja o mesmo que o autor pretendia que fosse e não tenha sido alterado. Com o Microsoft Edge, você pode exibir e validar assinaturas digitais de certificado em PDFs.

Estamos trabalhando ativamente para melhorar o suporte para lidar com mais cenários e estamos ansiosos para obter comentários sobre o mesmo.

## <a name="accessibility"></a>Acessibilidade

O leitor de PDF é fornecido com suporte à acessibilidade do teclado, modo de alto contraste e suporte ao leitor de tela através de dispositivos Windows e MacOS.

### <a name="keyboard-accessibility"></a>Acessibilidade do teclado

Os usuários podem usar a navegação para diferentes partes do documento com as quais um usuário pode interagir, como campos de formulário e destaques, usando o teclado. Os usuários também podem usar o modo Caret para navegar e interagir com os arquivos PDF usando o teclado.

### <a name="high-contrast-mode"></a>Modo de alto contraste

O leitor de PDF usará as configurações definidas no nível do sistema operacional para renderizar o conteúdo em PDF no modo de alto contraste.

### <a name="screen-reader-support"></a>Suporte do leitor de tela

Os usuários podem navegar e ler arquivos em PDF usando os leitores de tela em computadores com Windows e Mac.

## <a name="security-and-reliability"></a>Segurança e confiabilidade

A segurança está entre os princípios mais importantes de qualquer organização. A segurança do leitor de PDF é uma parte integrante do projeto de segurança do Microsoft Edge. Dois dos recursos de segurança mais importantes de uma perspectiva do leitor de PDF são o isolamento do processo e o Microsoft Defender Application Guard (Application Guard).

- Isolamento do processo. Os PDFs abertos de diferentes sites são totalmente isolados. O navegador não precisa se comunicar com nenhum website, nem com arquivos em PDF abertos de outra fonte. A navegação em PDF é segura contra qualquer ataque que pretenda utilizar PDFs comprometidos como superfície de ataque.

- Application Guard. Com o Application Guard, os administradores podem configurar uma lista de sites que sua organização confia. Se os usuários abrirem quaisquer outros sites, eles serão abertos em uma janela separada do Application Guard que funciona no seu próprio contêiner. O contêiner ajuda a proteger a rede corporativa e quaisquer dados no computador do usuário de serem comprometidos.<br><br>
Essa proteção também se aplica a qualquer arquivo PDF on-line que seja visualizado. Além disso, quaisquer arquivos PDF que forem baixados de uma janela do Application Guard são armazenados e, quando necessário, reabertos no contêiner. Isso ajuda a manter seu ambiente seguro não apenas quando o arquivo é baixado, mas durante todo o seu ciclo de vida. Para obter mais informações, consulte [Application Guard](./microsoft-edge-security-windows-defender-application-guard.md).

### <a name="reliability"></a>Confiabilidade

Como o Microsoft Edge é baseado no Chromium, os usuários podem esperar o mesmo nível de confiabilidade que estão acostumados a ver em outros navegadores baseados no Chromium.

## <a name="deploy-and-update-pdf-reader"></a>Implantar e atualizar o leitor de PDF

O leitor de PDF é instalado e atualizado com o restante do navegador Microsoft Edge. Para saber mais sobre como implantar o Microsoft Edge, assista ao vídeo [Implantar o Microsoft Edge para centenas ou milhares de dispositivos](microsoft-edge-video-deploy.md). Você também pode encontrar mais informações sobre a implantação na página inicial da [documentação do Microsoft Edge](./index.yml).

> [!TIP]
> Você pode tornar o Microsoft Edge o leitor de PDF padrão da sua organização. Para fazer isso, [siga estas etapas](./edge-default-browser.md).

## <a name="roadmap-and-feedback"></a>Roteiro e comentários

O mapa para leitor de PDF no Microsoft Edge está disponível [aqui.](https://techcommunity.microsoft.com/t5/articles/roadmap-for-pdf-reader-in-microsoft-edge/m-p/1467667)

Estamos analisando ativamente seus comentários sobre os recursos que considera importantes. .Sinta-se à vontade para nos enviar feedback por meio do [Microsoft Edge Insider](https://techcommunity.microsoft.com/t5/microsoft-edge-insider/ct-p/MicrosoftEdgeInsider) fórum.

## <a name="see-also"></a>Ver também

- [Página inicial do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Roteiro do Microsoft 365](https://www.microsoft.com/microsoft-365/roadmap)
- [Vídeo: leitor de PDF de nível empresarial do Microsoft Edge](microsoft-edge-video-pdf-reader.md)