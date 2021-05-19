---
title: Atualizações do Windows para o Microsoft Edge
ms.author: jtkim
author: dan-wesley
manager: srugh
ms.date: 02/05/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Atualizações do Windows para o Microsoft Edge
ms.openlocfilehash: 953becc459fe729f84d54da419481b3c6e26cc47
ms.sourcegitcommit: 16a92a51560fdba6f6480e4533453348f026c7ef
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/05/2021
ms.locfileid: "11313901"
---
# Atualizações do Windows para oferecer suporte à próxima versão do Microsoft Edge

Este artigo descreve como o Windows será atualizado para oferecer suporte à próxima versão do Microsoft Edge.

> [!IMPORTANT]
> Consulte a postagem [do blog da equipe de produto do Microsoft Edge](https://aka.ms/EdgeLegacyEOS) sobre o fim de serviço da Versão Prévia do Microsoft Edge.

> [!NOTE]
> Este artigo aplica-se ao canal estável do Microsoft Edge.

## Microsoft Edge e o ciclo de lançamento do Windows

A próxima versão do Microsoft Edge apresenta recursos de atualização mais frequentes e flexíveis. Como as versões do navegador não são vinculadas às versões principais do Windows, as alterações serão feitas no sistema operacional para garantir que a próxima versão do Microsoft Edge se adapte perfeitamente ao Windows. Como resultado, as atualizações de recursos serão lançadas em um ciclo de 6 semanas (aproximadamente). As atualizações de segurança e compatibilidade serão enviadas conforme necessário.

## Atualizações e a experiência do usuário

As atualizações não mudam a experiência do usuário até que o canal estável da próxima versão do Microsoft Edge seja instalado. A instalação do Microsoft Edge Beta, Dev ou Canary não dispara alterações no Windows. Essas versões do navegador serão instaladas junto com os navegadores existentes.

Quando todas as atualizações forem aplicadas e o canal estável da próxima versão do Microsoft Edge for instalado no nível do sistema, as seguintes alterações entrarão em vigor no sistema:

- Todos os itens fixados, blocos e atalhos do menu Iniciar para a versão atual do Microsoft Edge serão migrados para a próxima versão do Microsoft Edge.
- Todos os itens fixados e atalhos da barra de tarefas da versão atual do Microsoft Edge serão migrados para a próxima versão do Microsoft Edge.
- A próxima versão do Microsoft Edge será fixada na barra de tarefas. Se a versão atual do Microsoft Edge já estiver fixada, ela será substituída.
- A próxima versão do Microsoft Edge adicionará um atalho à área de trabalho. Se a versão atual do Microsoft Edge já tiver um atalho, ela será substituída.
- A maioria dos protocolos que o Microsoft Edge processa por padrão será migrada para a próxima versão do Microsoft Edge.
- O Microsoft Edge atual ficará oculto em todas as superfícies da experiência do sistema operacional, incluindo configurações, todos os aplicativos e quaisquer caixas de diálogo de suporte de arquivo ou protocolo.
- Todas as tentativas de iniciar a versão atual do Microsoft Edge redirecionam para a próxima versão do Microsoft Edge.

  > [!NOTE]
  > As instalações em nível de usuário não acionam esses comportamentos.

Juntamente com as alterações anteriores, há alterações que ocorrem independentemente da instalação do canal estável da próxima versão do Microsoft Edge.

- O Microsoft Edge cancela o registro de livros e protocolos XML não compatíveis com a próxima versão do Microsoft Edge. Os usuários que tentarem abrir esses protocolos receberão uma caixa de diálogo solicitando que escolham um aplicativo padrão. Saiba mais sobre as alterações no suporte em [Baixar um aplicativo de ePub para continuar lendo](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fsupport.microsoft.com%2Fhelp%2F4517840&data=02%7C01%7Cv-danwes%40microsoft.com%7Cc9f8571b880549c30fcf08d72be5eaf9%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637026138803983526&sdata=qtb3DvVZQ6H%2FFXnBievkl%2B%2BngAQXwl340PcH8kRc3y4%3D&reserved=0).

## Linha do Tempo

As alterações necessárias para oferecer suporte à experiência descrita serão fornecidas com três atualizações para diferentes versões do Windows.

### Windows versões 1903 e 1909

- Primeiro conjunto de mudanças na atualização opcional de julho de 2019, fornecido com a atualização de segurança de agosto de 2019.
- Segundo conjunto de mudanças na atualização opcional de agosto de 2019, fornecido com a atualização de segurança de setembro de 2019.

  > [!NOTE]
  > Esta é a atualização em que o Microsoft Edge cancela o registro do protocolo XML.

- Terceiro conjunto de mudanças na atualização opcional de setembro de 2019, fornecido com a atualização de segurança de outubro de 2019.

  > [!NOTE]
  > Esta é a atualização em que o Microsoft Edge não oferece mais suporte para eBooks.

### Windows versões 1709, 1803 e 1809

- Primeiro conjunto de mudanças na atualização opcional de agosto de 2019, fornecido com a atualização de segurança de setembro de 2019.
- Segundo conjunto de mudanças na atualização opcional de setembro de 2019, fornecido com a atualização de segurança de outubro de 2019.

  > [!NOTE]
  > Esta é a atualização em que o Microsoft Edge cancela o registro do protocolo XML.

- Terceiro conjunto de mudanças na atualização opcional de outubro de 2019, fornecido com a atualização de segurança de novembro de 2019.

  > [!NOTE]
  > Esta é a atualização em que o Microsoft Edge não oferece mais suporte para eBooks.

A tabela a seguir fornece os detalhes de atualizações específicas em cada conjunto de alterações.

| Windows 10 | Mais informações | Download necessário |
|--|--|--|
| Versão 1709 | [KB4525241](https://support.microsoft.com/help/4525241/windows-10-update-kb4525241) | [Atualização Cumulativa para Windows 10 Versão 1709](https://www.catalog.update.microsoft.com/Search.aspx?q=4525241) |
| Versão 1803  | [KB4525237](https://support.microsoft.com/help/4525237/windows-10-update-kb4525237) | [Atualização Cumulativa para Windows 10 Versão 1803](https://www.catalog.update.microsoft.com/Search.aspx?q=KB4525237) |
| Versão 1809  | [KB4523205](https://support.microsoft.com/help/4523205/windows-10-update-kb4523205) | [Atualização Cumulativa para Windows 10 Versão 1809](https://www.catalog.update.microsoft.com/Search.aspx?q=4523205) |
| Versão 1903 e 1909 |[KB4517389](https://support.microsoft.com/help/4517389/windows-10-update-kb4517389)  | [Atualização Cumulativa para Windows 10 Versão 1903 e 1909](https://www.catalog.update.microsoft.com/Search.aspx?q=4517389) |

## Consulte também

- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Documentação do Microsoft Edge](https://docs.microsoft.com/DeployEdge/)
