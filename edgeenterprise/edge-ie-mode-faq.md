---
title: Perguntas frequentes sobre o modo IE
ms.author: cjacks
author: cjacks
manager: saudm
ms.date: 05/27/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Perguntas frequentes e solução de problemas do Microsoft Edge com o modo IE
ms.openlocfilehash: fcceb9eab19d667f772c593fe4f362606c1623ff
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979027"
---
# Perguntas frequentes sobre o modo IE

Este artigo fornece dicas para solução de problemas e uma seção de perguntas frequentes para o Microsoft Edge (versão 77 ou posterior).

> [!NOTE]
> Este artigo se aplica aos Canais **Estável**, **Beta** e **Dev** do Microsoft Edge Beta, versão 77 ou posteriores.

## Solução de problemas do modo IE

Use as informações desta seção para diagnosticar e corrigir problemas do modo IE.

### Informações de diagnóstico do modo Internet Explorer

Você pode obter informações de diagnóstico do modo Internet Explorer na guia Compatibilidade do Microsoft Edge. Para abrir esta guia, vá para *edge://compat/iediagnostic*. Esta página pode mostrar mensagens de diagnóstico. Esta página também fornece informações de configuração para as seguintes categorias:

- **Verificação de chave de registro**. (Exibido apenas se a verificação falhar.) Verifica se a integração com o Internet Explorer está configurada corretamente no registro. Caso contrário, o usuário pode clicar em **Corrigir** para resolver o problema.
- **Modo Internet Explorer**. Mostra a versão da API usada, com base na configuração e no SO. Se houver algum problema, o usuário poderá ser solicitado a instalar uma atualização do **Windows Update**.
- **Configuração do modo Internet Explorer**. Mostra se o modo Internet Explorer está ativado e como está configurado.
- **Linha de comando**. Exibe a cadeia de caracteres de linha de comando e as chaves usadas para iniciar o Microsoft Edge.
- **Configurações de política de grupo**. Mostra se o modo IE está configurado usando políticas de grupo, e as políticas que estão aplicadas.

### Mensagem de erro: "Para abrir esta página no modo Internet Explorer, reinstale o Microsoft Edge com privilégios de administrador".

Você pode ver esse erro se não tiver todas as atualizações necessárias do Windows Update. Consulte os pré-requisitos listados em [Sobre o modo IE](https://docs.microsoft.com/deployedge/edge-ie-mode) para obter as versões necessárias do Windows e Microsoft Edge.

Se você já instalou todas as atualizações necessárias do Windows Update, poderá ver este erro se:

- Você estiver usando o canal Canary, que é instalado no nível do usuário por padrão.
- Você estiver usando o canal Estável, Beta ou Dev, mas quando solicitada a elevação durante a instalação, a elevação foi cancelada. Quando você cancelar o prompt de elevação, a instalação continuará no nível do usuário.
- O Internet Explorer 11 foi desabilitado nos Recursos do Windows.

Possíveis soluções:

- Execute o instalador para qualquer canal no nível do sistema: `installer.exe --system-level`.
- Habilite o Internet Explorer 11 nos Recursos do Windows.

Para verificar se o Microsoft Edge está instalado no nível do sistema, digite "edge://versão" na barra de endereços do Microsoft Edge. O caminho do executável mostrará um caminho que começa com *C:\Arquivos de Programas*, o que indica uma instalação do sistema. Se o caminho do executável começar com *C:\Users\*, desinstale e reinstale o Microsoft Edge com privilégios de administrador.

### Mensagem de erro: "para abrir esta página no modo IE, tente reiniciar o Microsoft Edge".

Esse erro pode ocorrer se houver um erro inesperado no Internet Explorer. Reiniciar o Microsoft Edge geralmente corrige esse erro.

### Mensagem de erro: "Desative a depuração remota para abrir este site no modo IE. Caso contrário, talvez ele não funcione como esperado".

Esse erro pode ocorrer se você estiver depurando remotamente e navegar a uma página da Web configurada para executar no modo IE. Você pode continuar, mas a página será renderizada usando o Microsoft Edge.

## Perguntas frequentes

### O modo IE substituirá o Internet Explorer 11?

Temos o compromisso de manter o Internet Explorer um navegador compatível, confiável e seguro. O Internet Explorer ainda é um componente do Windows e segue o ciclo de vida de suporte do sistema operacional no qual ele está instalado. Para saber os detalhes, consulte [Perguntas frequentes sobre o ciclo de vida – Internet Explorer](https://support.microsoft.com/help/17454/). Embora a Microsoft continue a dar suporte e atualizar o Internet Explorer, os recursos e as atualizações de plataforma mais recentes estarão disponíveis somente no Microsoft Edge.

### Posso usar "Abrir com o Explorer" ou "Exibir no Explorador de Arquivos" no SharePoint com o modo IE?

Sim, se funcionar no Internet Explorer 11 autônomo, funcionará no modo IE. No entanto, em vez de usar a opção Abrir com o Explorer, a abordagem recomendada para gerenciar arquivos e pastas fora do SharePoint é [sincronizar seus arquivos do SharePoint](https://support.office.com/en-us/article/sync-sharepoint-files-with-the-onedrive-sync-app-6de9ede8-5b6e-4503-80b2-6190f3354a88) ou [mover ou copiar arquivos no SharePoint](https://support.office.com/en-us/article/move-or-copy-files-in-sharepoint-00e2f483-4df3-46be-a861-1f5f0c1a87bc).

### O modo IE no Microsoft Edge é compatível com a opção *desfazer mesclagem* que era compatível com o Internet Explorer 11?

Não há nenhuma linha de comando explícita no Microsoft Edge para espelhar a opção *desfazer mesclagem*, mas há algumas alternativas que recomendamos para fornecer essa funcionalidade.

1. Usar Perfis no Microsoft Edge: cada perfil é mapeado para uma sessão diferente do IE para as páginas do modo IE, para que se comporte de forma idêntica com a opção *desfazer mesclagem*.
2. Use a linha de comando`--user-data-dir=<path>`, mas com um caminho diferente para cada sessão. Se necessário, você pode criar um utilitário para que o execute de forma que ambos inicializem o Microsoft Edge e altera o caminho da sessão.

Se nenhuma das opções acima funcionar para o seu cenário, fale por meio de um dos nossos canais de comentários: suporte da Microsoft, [Fórum TechCommunity](https://techcommunity.microsoft.com/t5/enterprise/bd-p/EdgeInsiderEnterprise)ou [UserVoice do Microsoft Edge](https://microsoftedge.uservoice.com/forums/928825-enterprise).

## Consulte também

- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Sobre o modo IE](https://docs.microsoft.com/deployedge/edge-ie-mode)
- [Informações adicionais sobre o Modo Empresarial](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)