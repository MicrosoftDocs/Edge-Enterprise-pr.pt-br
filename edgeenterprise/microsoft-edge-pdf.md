---
title: Leitor de PDF no Microsoft Edge
ms.author: adigan
author: dan-wesley
manager: balajek
ms.date: 08/05/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Saiba mais sobre o leitor de PDF no Microsoft Edge.
ms.openlocfilehash: c189bc08d4af0c9d5c4d9c573e0b5b7ef32a7fb3
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979143"
---
# Leitor de PDF no Microsoft Edge

Os arquivos em PDF representam uma parte significativa do nosso cotidiano. Eles estão disponíveis sob a forma de contratos e acordos, boletins informativos, formulários, artigos de pesquisa, currículos, etc. Esses arquivos destacam a necessidade de um leitor de PDF confiável, seguro e eficiente que possa ser adotado pelas empresas.

O Microsoft Edge acompanha um leitor de PDF interno que permite que você abra os arquivos PDF locais, arquivos PDF on-line ou arquivos PDF inseridos nas páginas da Web. Você pode fazer anotações nesses arquivos com tinta e destaque. Esse leitor de PDF oferece aos usuários uma única aplicação para atender às necessidades da página Web e do documento PDF. O leitor de PDF do Microsoft Edge é uma aplicação segura e confiável que funciona em todas as plataformas de área de trabalho do Windows e do MacOS.

> [!NOTE]
> Este artigo se aplica ao Microsoft Edge versão 77 ou posteriores.

## Pré-requisitos, suporte e restrições

A tabela a seguir mostra quais canais e versões do Microsoft Edge oferecem suporte a cada recurso do leitor de PDF.

| Recurso | Versão de canal estável |
|---------|------------------------|
| Exibir e imprimir arquivos PDF locais, on-line e incorporados | 79.0.309.71                |
| Preenchimento do formulário básico<br>(Os formulários JavaScript não possuem suporte) | 79.0.309.71           |
| Escrita à tinta  | 80.0.361.48            |
| Personalização de tinta | 83.0.478.54  |
| Highlight  | 81.0.416.53.         |
| Ler em voz alta | Sendo promovido agora nos canais [Microsoft Edge Insider](https://www.microsoftedgeinsider.com/) |
| Visualizar arquivos MIP protegidos | Suporte ao Windows na versão 80.0.361.48<br>Suporte ao Mac na versão 81.0.416.53 |
|  Visualizar arquivos IRM protegidos  | 83.0.478.37            |

### Restrições

Observe as seguintes restrições para o leitor de PDF atual:

-  A Arquitetura de formulários XML (XFA)é um formato herdado de formulários que não possui suporte no Microsoft Edge.
-  A documentação relacionada com cenários de Acessibilidade que atualmente não possuem suporte pode ser encontrada no blog [Relatório de conformidade de acessibilidade da Microsoft](https://cloudblogs.microsoft.com/industry-blog/government/2018/09/11/accessibility-conformance-reports/).

## Recursos

### Escrita à tinta

A escrita à tinta nos arquivos em PDF é útil para criar anotações rápidas para facilitar a consulta, o sinal ou o preenchimento de formulários em PDF. Esse recurso já está disponível no Microsoft Edge. Além de arquivos em PDF de escrita à tinta, conforme necessário, você pode usar a cor e a largura do traçado para dar atenção às diferentes partes do arquivo em PDF. A próxima captura de tela mostra como um usuário pode adicionar escrita à tinta em uma página em PDF.

<!-- SCREENSHOT -->
![Página Adicionar escrita à tinta em PDF](media/microsoft-edge-pdf/pdf-reader-inking.png)

### Highlight

O leitor de PDF no Microsoft Edge é fornecido com o suporte para adicionar e editar destaques. Para criar um destaque, o usuário só precisa selecionar o texto, clicar com o botão direito nele, selecionar destaques no menu e escolher a cor desejada. A próxima captura de tela mostra as opções de destaque disponíveis.

![Usar a opção destacar no leitor de PDF](media/microsoft-edge-pdf/pdf-reader-highlight.png)

### Ler em voz alta

O recurso Ler em Voz alta do PDF permite que os usuários ouçam ao conteúdo em PDF enquanto realizam outras tarefas que podem ser importantes para eles. Ele também ajuda os alunos de auditoria a se concentrarem no conteúdo, o que facilita o aprendizado. A próxima captura de tela mostra um exemplo lido em voz alta. O destaque mostra o texto que está sendo lido no momento.

![Usar a opção destacar no leitor de PDF](media/microsoft-edge-pdf/pdf-reader-read-aloud-example.png)

### PDFs protegidos

A [Proteção de informações da Microsoft (MIP)](https://docs.microsoft.com/microsoft-365/compliance/protect-information?view=o365-worldwide) permite que os usuários colaborem com outras pessoas de maneira segura enquanto aderem às políticas de conformidade da sua organização. Depois que um arquivo é protegido, as ações que os usuários podem realizar são determinadas pelas permissões que lhes são atribuídas.

Esses arquivos podem ser abertos diretamente no navegador sem precisar baixar qualquer outro software ou instalar um suplemento. Isso integra a segurança fornecida pelo MIP diretamente no navegador, proporcionando um fluxo de trabalho contínuo.

<!-- SCREENSHOT -->
![Documento em PDF protegido.](media/microsoft-edge-pdf/pdf-reader-protected-pdf2.png)

Além dos arquivos protegidos pelo MIP, os arquivos em [PDF em Gerenciamento de direitos de informação (IRM)](https://docs.microsoft.com/microsoft-365/compliance/set-up-irm-in-sp-admin-center?view=o365-worldwide) protegidos por bibliotecas do SharePoint também podem ser abertos originalmente no navegador.

Com o Microsoft Edge, os usuários podem visualizar os arquivos MIP protegidos localmente, ou na nuvem. Se for salvo localmente, o arquivo pode ser aberto diretamente no navegador. Se o arquivo for aberto de um serviço de nuvem como o SharePoint, talvez o usuário precise usar a opção "Abrir no navegador".

Se o perfil com o qual o usuário se conectou no Microsoft Edge tiver pelo menos permissões de visualização do arquivo, o arquivo será aberto no Microsoft Edge.

<!-- SCREENSHOT -->
![Aviso para salvar a página de PDF do SharePoint é protegido pelo MIP](media/microsoft-edge-pdf/pdf-reader-sharepoint-irm.png)

## Acessibilidade

O leitor de PDF é fornecido com suporte à acessibilidade do teclado, modo de alto contraste e suporte ao leitor de tela através de dispositivos Windows e MacOS.

### Acessibilidade do teclado

Os usuários podem usar a navegação para diferentes partes do documento com as quais um usuário pode interagir, como campos de formulário e destaques, usando o teclado.

<!-- SCREENSHOT -->

### Modo de alto contraste

O leitor de PDF usará as configurações definidas no nível do sistema operacional para renderizar o conteúdo em PDF no modo de alto contraste.

<!-- SCREENSHOT -->
<!--![High contrast mode for pdf file](media/microsoft-edge-pdf/pdf-reader-high-contrast.png)-->

### Suporte do leitor de tela

Os usuários podem navegar e ler arquivos em PDF usando os leitores de tela em computadores com Windows e Mac. <!--The next screenshot shows the toolbar that users can use for audio settings when they're using the Read Aloud option in PDF reader. -->

<!-- SCREENSHOT -->
<!--
![Screen reader toolbar](media/microsoft-edge-pdf/pdf-reader-read-aloud.png) -->

## Segurança e confiabilidade

A segurança está entre os princípios mais importantes de qualquer organização. A segurança do leitor de PDF é uma parte integrante do projeto de segurança do Microsoft Edge. Dois dos recursos de segurança mais importantes de uma perspectiva do leitor de PDF são o isolamento do processo e o Microsoft Defender Application Guard (Application Guard).

- Isolamento do processo. Os PDFs abertos de diferentes sites são totalmente isolados. O navegador não precisa se comunicar com nenhum website, nem com arquivos em PDF abertos de outra fonte. A navegação em PDF é segura contra qualquer ataque que pretenda utilizar PDFs comprometidos como superfície de ataque.

- Application Guard. Com o Application Guard, os administradores podem configurar uma lista de sites que sua organização confia. Se os usuários abrirem quaisquer outros sites, eles serão abertos em uma janela separada do Application Guard que funciona no seu próprio contêiner. O contêiner ajuda a proteger a rede corporativa e quaisquer dados no computador do usuário de serem comprometidos.<br><br>
Essa proteção também se aplica a qualquer arquivo PDF on-line que seja visualizado. Além disso, quaisquer arquivos PDF que forem baixados de uma janela do Application Guard são armazenados e, quando necessário, reabertos no contêiner. Isso ajuda a manter seu ambiente seguro não apenas quando o arquivo é baixado, mas durante todo o seu ciclo de vida. Para obter mais informações, consulte [Application Guard](https://docs.microsoft.com/DeployEdge/microsoft-edge-security-windows-defender-application-guard).

### Confiabilidade

Uma vez que o Microsoft Edge é baseado no Chromium, os usuários podem esperar pelo mesmo nível de confiabilidade que estão acostumados a ver no Google Chrome.

## Implantar e atualizar o leitor de PDF

O leitor de PDF é instalado e atualizado com o restante do navegador Microsoft Edge. Para saber mais sobre como implantar o Microsoft Edge, assista ao vídeo [Implantar o Microsoft Edge para centenas ou milhares de dispositivos](microsoft-edge-video-deploy.md). Você também pode encontrar mais informações sobre a implantação na página inicial da [documentação do Microsoft Edge](https://docs.microsoft.com/DeployEdge/).

> [!TIP]
> Você pode tornar o Microsoft Edge o leitor de PDF padrão da sua organização. Para fazer isso, [siga estas etapas](https://docs.microsoft.com/deployedge/edge-default-browser).

## Roteiro e comentários

O roteiro do leitor de PDF no Microsoft Edge está disponível [aqui](https://techcommunity.microsoft.com/t5/articles/roadmap-for-pdf-reader-in-microsoft-edge/m-p/1467667).

Analisamos ativamente seus comentários sobre os recursos que você considera importantes. Sinta-se à vontade para nos enviar comentários pelo [Microsoft Edge UserVoice](https://microsoftedge.uservoice.com/) e no fórum [Microsoft Edge Insider](https://techcommunity.microsoft.com/t5/microsoft-edge-insider/ct-p/MicrosoftEdgeInsider).

## Consulte também

- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)