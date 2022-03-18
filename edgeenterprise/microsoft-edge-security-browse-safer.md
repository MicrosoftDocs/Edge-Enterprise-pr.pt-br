---
title: Navegar com segurança com o Microsoft Edge
ms.author: pchiquini
author: dan-wesley
manager: robfranco
ms.date: 02/17/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Saiba como a segurança aprimorada oferece suporte à navegação mais segura com o Microsoft Edge.
ms.openlocfilehash: 43c48cb6210ce194a16759c5adb05a6f67b05249
ms.sourcegitcommit: 556aca8dde42dd66364427f095e8e473b86651a0
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2022
ms.locfileid: "12445889"
---
# <a name="browse-more-safely-with-microsoft-edge"></a>Navegar com segurança com o Microsoft Edge

Este artigo descreve como o Microsoft Edge fornece segurança aprimorada na Web.

> [!NOTE]
> Este artigo se aplica ao Microsoft Edge versão 98 ou posterior.

## <a name="overview"></a>Visão geral

O Microsoft Edge está adicionando proteções de segurança aprimoradas para fornecer uma camada adicional de proteção ao navegar na Web e visitar sites desconhecidos. A plataforma Web foi projetada para lhe dar uma experiência avançada de navegação usando tecnologias poderosas, como JavaScript. Por outro lado, esse poder pode ser convertido em mais exposição quando você visita um site mal-intencionado. Com a segurança aprimorada, o Microsoft Edge ajuda a reduzir o risco de um ataque aplicando automaticamente configurações de segurança mais conservadoras em sites desconhecidos e se adapta ao longo do tempo à medida que você continua a navegar.

## <a name="defense-in-depth"></a>Defesa detalhada

A segurança aprimorada no Microsoft Edge reduz as vulnerabilidades relacionadas à memória desabilitando a compilação JIT (just-in-time) do JavaScript e habilitando proteções adicionais do sistema operacional para o navegador. Essas proteções incluem [Proteção de Pilha Imposta por Hardware](https://techcommunity.microsoft.com/t5/windows-kernel-internals-blog/developer-guidance-for-hardware-enforced-stack-protection/ba-p/2163340) e [Proteção de Código Arbitrário (ACG)](/microsoft-365/security/defender-endpoint/exploit-protection-reference?view=o365-worldwide#arbitrary-code-guard).

Quando combinadas, essas alterações ajudam a fornecer "defesa detalhada" porque elas dificultam mais do que nunca para um site mal-intencionado aproveitar uma vulnerabilidade sem patch para gravar na memória executável e atacar um usuário final. Você pode saber mais sobre os resultados da experimentação na [postagem do blog](https://microsoftedge.github.io/edgevr/posts/Super-Duper-Secure-Mode) da equipe da Segurança do Microsoft Edge e [Introdução à segurança aprimorada para Microsoft Edge](https://microsoftedge.github.io/edgevr/posts/Introducing-Enhanced-Security-for-Microsoft-Edge/).

Você também pode estar interessado em saber mais sobre as [proteções de segurança de primeira linha no Microsoft Edge](/deployedge/ms-edge-security-for-business). Notavelmente, talvez você queira saber mais sobre como o [SmartScreen do Microsoft Edge](/deployedge/microsoft-edge-security-smartscreen) protege os usuários contra tentativas de phishing e downloads de malware.

> [!NOTE]
> Atualmente, não há suporte para os sites que usam WebAssembly (WASM) neste modo. Se você precisar de acesso a um site que precisa de WASM, considere adicioná-lo à sua lista de exceções, conforme descrito abaixo.

## <a name="whats-new-in-microsoft-edge-security-settings"></a>Novidades nas configurações de segurança do Microsoft Edge

Com **Aprimorar sua segurança na Web**, o Microsoft Edge oferece uma camada extra de proteção ao navegar na Web.

Use as etapas a seguir para configurar a segurança adicionada.

1. No Microsoft Edge, vá para **Configurações e mais** > **Configurações** > **Privacidade, pesquisa e serviços**.
2. Em **Segurança**, verifique se **Aprimorar sua segurança na Web** está habilitado.
3. Selecione a opção que é melhor para sua navegação.

As seguintes configurações de alternância estão disponíveis:

- Desativar (Padrão): o recurso está desativado
- Ativar – Balanceado (Recomendado): o Microsoft Edge aplicará proteções de segurança adicionais quando os usuários visitarem sites desconhecidos, mas irá ignorar essas proteções para sites visitados com frequência. Essa combinação fornece um nível prático de proteção contra invasores, preservando a experiência do usuário para as tarefas usuais de um usuário na Web.
- Ativado – Estrito: o Microsoft Edge aplicará proteções de segurança adicionais para todos os sites que um usuário visita. Os usuários podem relatar alguma dificuldade para realizar suas tarefas usuais.

A captura de tela a seguir mostra a página de configuração "Aprimorar sua segurança na Web", com a segurança aprimorada habilitada e definida para fornecer segurança balanceada.

:::image type="content" source="media/microsoft-edge-security-browse-safer/browse-safer-enhance-security-dialog.png" alt-text="Caixa de diálogo para configurar a segurança balanceada na Web.":::

### <a name="how-balanced-mode-works"></a>Como funciona o modo "Balanceado"

O modo balanceado é um modo adaptável que se baseia no comportamento do usuário em um determinado dispositivo, e a compreensão da Microsoft sobre o risco na Web para dar aos sites que os usuários provavelmente usarão e confiarão acesso total à plataforma Web, limitando o que sites novos e desconhecidos podem fazer.

### <a name="how-strict-mode-works"></a>Como funciona o modo "Estrito"

Como o nome sugere, o Modo Estrito aplica essas proteções de segurança a todos os sites por padrão. No entanto, você ainda pode adicionar sites manualmente à lista de sites de exceção e a configuração de administrador corporativo ainda será aplicada, se presente. O modo estrito não é apropriado para a maioria dos usuários finais porque pode exigir algum nível de configuração para o usuário concluir suas tarefas normais.

### <a name="exception-site-list"></a>Lista de sites de exceção

No modo Balanceado e Estrito, você também pode criar exceções para determinados sites conhecidos em que você confia. Use as etapas a seguir para adicionar um site à sua lista de exceções.

1. No Microsoft Edge, selecione **Configurações e mais** >  **Configurações** >  **Privacidade, pesquisa e serviços**.
2. Verifique se **Aprimorar sua segurança na Web** está ligado.
3. Em **Aprimorar sua segurança na Web**, selecione **Exceções**.
4. Selecione **Adicionar um site**, digite a URL completa e selecione **Adicionar**.

> [!NOTE]
> Você pode usar as etapas (1 a 3) para exibir sites em **Exceções de segurança aprimoradas**. Você pode **Editar** um site, **Remover** um site ou **Remover todas as** exceções.

A próxima captura de tela mostra a página de configurações para exceções de segurança.

:::image type="content" source="media/microsoft-edge-security-browse-safer/browse-safer-enhanced-exceptions.png" alt-text="Página Configurações para definir exceções de segurança":::

### <a name="enterprise-controls"></a>Controles corporativos

Os administradores corporativos podem configurar esse recurso de segurança usando configurações de Política de Grupo, incluindo a criação de listas de "Permissões" e "Negações" para aprimorar explicitamente a segurança de seus usuários ao visitar determinados sites ou desabilitar o modo para outras pessoas. Para ver uma lista completa de políticas, consulte a [documentação de política do navegador do Microsoft Edge](/deployedge/microsoft-edge-policies).

## <a name="user-experience-with-enhanced-security"></a>Experiência do usuário com segurança aprimorada

Depois que um usuário aprimora a segurança, ele verá uma faixa com as palavras "Segurança adicionada" em sua barra de navegação de URL quando o Microsoft Edge estiver aplicando a segurança aprimorada para um site específico.

:::image type="content" source="media/microsoft-edge-security-browse-safer/browse-safer-added-security-banner.png" alt-text="Faixa mostrando que a segurança adicionada está ativada.":::

Ao selecionar a faixa, você verá o seguinte submenu. Você pode alternar "Aprimorar a segurança deste site" para habilitar ou desabilitar a segurança aprimorada para um determinado site. Se você alterar o botão de alternância de "Aprimorar a segurança deste site", o Microsoft Edge adicionará esse site à lista de sites de exceção. A próxima captura de tela mostra o recurso desativado para o site.  

:::image type="content" source="media/microsoft-edge-security-browse-safer/browse-safer-enhanced-security-off.png" alt-text="Caixa de diálogo com a segurança aprimorada desligada.":::

> [!NOTE]
> "Aprimorar a segurança para este site" só aparece quando a segurança aprimorada está habilitada na página de configurações.

## <a name="send-us-feedback"></a>Enviar feedback

Queremos obter seus comentários sobre nossa próxima iteração para melhorar "Aprimorar a segurança na Web". Se algo não funcionar da maneira esperada ou se você tiver comentários para compartilhar sobre essas alterações, queremos saber sua opinião. Você pode entrar em contato com Suporte da Microsoft para relatar problemas ou comentários. Você também pode deixar comentários em nosso [Fórum TechCommunity](https://techcommunity.microsoft.com/t5/enterprise/bd-p/EdgeInsiderEnterprise).

## <a name="see-also"></a>Consulte também

- [Vídeo: navegação segura no Microsoft Edge](microsoft-edge-video-security-smartscreen.md)
- [Modo de Segurança do Super Duper](https://microsoftedge.github.io/edgevr/posts/Super-Duper-Secure-Mode/)
- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
