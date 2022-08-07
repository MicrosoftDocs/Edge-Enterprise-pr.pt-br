---
title: Navegar com segurança com o Microsoft Edge
ms.author: pchiquini
author: dan-wesley
manager: robfranco
ms.date: 08/04/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Saiba como a segurança aprimorada oferece suporte à navegação mais segura com o Microsoft Edge.
ms.openlocfilehash: ff6bf5f9844ad282b18495149f171c05fb1727b4
ms.sourcegitcommit: c4b3a38fdb78cf663f82d35148716d88f3e7551d
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2022
ms.locfileid: "12691806"
---
# <a name="browse-more-safely-with-microsoft-edge"></a>Navegar com segurança com o Microsoft Edge

Este artigo descreve como o Microsoft Edge fornece segurança aprimorada na Web.

> [!NOTE]
> Este artigo se aplica ao Microsoft Edge versão 104 ou posterior.

## <a name="overview"></a>Visão geral

O Microsoft Edge está adicionando proteções de segurança aprimoradas para fornecer uma camada extra de proteção ao navegar na Web e visitar sites desconhecidos. A plataforma Web foi projetada para lhe dar uma experiência avançada de navegação usando tecnologias poderosas, como JavaScript. Por outro lado, esse poder pode ser convertido em mais exposição quando você visita um site mal-intencionado. Com o modo de segurança aprimorada, o Microsoft Edge ajuda a reduzir o risco de um ataque aplicando automaticamente configurações de segurança mais conservadoras em sites desconhecidos e se adapta ao longo do tempo à medida que você continua navegando.

## <a name="defense-in-depth"></a>Defesa detalhada

O modo de segurança aprimorada no Microsoft Edge atenua as vulnerabilidades relacionadas à memória, desabilitando a compilação JavaScript just-in-time (JIT) e habilitando proteções adicionais do sistema operacional para o navegador. Essas proteções incluem [Proteção de Pilha Imposta por Hardware](https://techcommunity.microsoft.com/t5/windows-kernel-internals-blog/developer-guidance-for-hardware-enforced-stack-protection/ba-p/2163340) e [Proteção de Código Arbitrário (ACG)](/microsoft-365/security/defender-endpoint/exploit-protection-reference?view=o365-worldwide#arbitrary-code-guard).

Quando combinadas, essas alterações ajudam a fornecer 'defesa em profundidade' porque tornam mais difícil do que nunca para um site malicioso usar uma vulnerabilidade sem patch para gravar em memória executável e atacar um usuário final. Você pode saber mais sobre os resultados da experimentação na [postagem do blog](https://microsoftedge.github.io/edgevr/posts/Super-Duper-Secure-Mode) da equipe da Segurança do Microsoft Edge e [Introdução à segurança aprimorada para Microsoft Edge](https://microsoftedge.github.io/edgevr/posts/Introducing-Enhanced-Security-for-Microsoft-Edge/).

Você também pode estar interessado em saber mais sobre as [proteções de segurança de primeira linha no Microsoft Edge](/deployedge/ms-edge-security-for-business). Notavelmente, talvez você queira saber mais sobre como o [SmartScreen do Microsoft Edge](/deployedge/microsoft-edge-security-smartscreen) protege os usuários contra tentativas de phishing e downloads de malware.

> [!NOTE]
> Atualmente, não há suporte para os sites que usam WebAssembly (WASM) neste modo. Se você precisar de acesso a um site que precisa de WASM, considere adicioná-lo à sua lista de sites de exceção, conforme descrito em [Lista de sites de exceção](#exception-site-list).

## <a name="whats-new-in-microsoft-edge-security-settings"></a>Novidades nas configurações de segurança do Microsoft Edge

Com **Aprimorar sua segurança na Web**, o Microsoft Edge oferece uma camada extra de proteção ao navegar na Web.

Use as etapas a seguir para configurar a segurança adicionada.

1. No Microsoft Edge, vá para **Configurações e mais** > **Configurações** > **Privacidade, pesquisa e serviços**.
2. Em **Segurança**, verifique se **Aprimorar sua segurança na Web** está habilitado.
3. Selecione a opção que é melhor para sua navegação.

As seguintes configurações de alternância estão disponíveis:

- Desativar (Padrão): o recurso está desativado
- Ativado – Básico (recomendado): o Microsoft Edge aplicará proteções de segurança adicionais aos sites menos visitados. Essa configuração preserva a experiência do usuário para os sites mais populares na Web.  
- Ativado – Equilibrado: o Microsoft Edge aplicará proteções de segurança adicionais quando os usuários visitarem sites desconhecidos, mas ignorará essas proteções para sites visitados com frequência. Essa combinação fornece um nível prático de proteção contra invasores, preservando a experiência do usuário para as tarefas usuais de um usuário na Web.
- Ativado – Estrito: o Microsoft Edge aplicará proteções de segurança adicionais para todos os sites que um usuário visita. Os usuários podem relatar alguma dificuldade para realizar suas tarefas usuais.

A captura de tela a seguir mostra a página de configurações "Aprimorar sua segurança na Web", com o modo de segurança aprimorada habilitado e definido para fornecer segurança Básica.

:::image type="content" source="media/microsoft-edge-security-browse-safer/browse-safer-enhance-security-dialog2.png" alt-text="Caixa de diálogo para configurar a segurança balanceada na Web.":::

### <a name="how-basic-mode-works"></a>Como funciona o modo "Básico"

O modo básico é um modo estático que aplica essas atenuações de segurança apenas aos sites menos visitados. Esse modo não leva em consideração o comportamento do usuário e só habilita o recurso nos sites menos visitados.

### <a name="how-balanced-mode-works"></a>Como funciona o modo "Balanceado"

O modo balanceado é um modo adaptável que se baseia no comportamento do usuário em um determinado dispositivo, e a compreensão da Microsoft sobre o risco na Web para dar aos sites que os usuários provavelmente usarão e confiarão acesso total à plataforma Web, limitando o que sites novos e desconhecidos podem fazer.

### <a name="how-strict-mode-works"></a>Como funciona o modo "Estrito"

Como o nome sugere, o Modo Estrito aplica essas proteções de segurança a todos os sites por padrão. No entanto, você ainda pode adicionar sites manualmente à lista de sites de exceção e a configuração de administrador corporativo ainda será aplicada, se presente. O modo estrito não é apropriado para a maioria dos usuários finais porque pode exigir algum nível de configuração para o usuário concluir suas tarefas normais.

### <a name="exception-site-list"></a>Lista de sites de exceção

No modo Básico, Equilibrado e Estrito, você também pode criar exceções para determinados sites familiares nos quais você confia. Use as etapas a seguir para adicionar um site à sua lista de exceções.

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

> [!NOTE]
> Definir a política [EnhanceSecurityMode](/deployedge/microsoft-edge-policies#enhancesecuritymode) como 'StrictMode' ou definir a política [DefaultJavaScriptJitSetting](/deployedge/microsoft-edge-policies#defaultjavascriptjitsetting) como BlockJavaScriptJit terá o mesmo efeito que alterar a configuração **Aprimorar sua segurança na Web** em *edge://settings/privacy* como 'Estrito'.

## <a name="user-experience-with-enhanced-security-mode"></a>Experiência do usuário com o modo de segurança aprimorada

Depois que um usuário ativar o modo de segurança aprimorada, ele verá uma faixa com as palavras “Segurança adicionada” na sua barra de navegação de URL quando o Microsoft Edge estiver aplicando o modo de segurança aprimorada para um site específico.

:::image type="content" source="media/microsoft-edge-security-browse-safer/browse-safer-added-security-banner.png" alt-text="Faixa mostrando que a segurança adicionada está ativada.":::

Quando você selecionar a faixa, verá o próximo submenu. Você pode selecionar "Aprimorar a segurança deste site" para redirecioná-lo para um segundo submenu que mostra as configurações de segurança para o site atual e dá ao usuário a opção de ativar ou desativar a segurança.

> [!NOTE]
> "Aprimorar a segurança deste site" só aparece quando o modo de segurança aprimorada está habilitado nas Configurações do Microsoft Edge.

:::image type="content" source="media/microsoft-edge-security-browse-safer/browse-safer-enhance-security-for-site-option.png" alt-text="Mostra a opção de aprimorar a segurança do site atual.":::

No submenu mostrado na próxima captura de tela, você pode habilitar ou desabilitar manualmente o modo de segurança aprimorada para um site específico. Se você alterar a alternância "Usar a segurança aprimorada para este site", o Microsoft Edge adicionará proativamente esse site à lista de sites de exceção.

> [!NOTE]
> Você sempre pode remover este site atualizando a lista de sites de exceção em **Configurações** > **Privacidade, pesquisa e serviços** > **Exceções da segurança aprimorada**.

:::image type="content" source="media/microsoft-edge-security-browse-safer/browse-safer-enhance-security-for-site-toggle.png" alt-text="Mostra as configurações de segurança do site com alternância para ativar ou desativar a segurança.":::

## <a name="send-us-feedback"></a>Enviar feedback

Queremos receber seus comentários sobre nossa próxima iteração para melhorar o "modo de segurança aprimorada". Se algo não funcionar da maneira esperada ou se você tiver comentários para compartilhar sobre essas alterações, queremos saber sua opinião. Você pode entrar em contato com Suporte da Microsoft para relatar problemas ou comentários. Você também pode deixar comentários em nosso [Fórum TechCommunity](https://techcommunity.microsoft.com/t5/enterprise/bd-p/EdgeInsiderEnterprise).

## <a name="see-also"></a>Consulte também

- [Vídeo: navegação segura no Microsoft Edge](microsoft-edge-video-security-smartscreen.md)
- [Modo de Segurança do Super Duper](https://microsoftedge.github.io/edgevr/posts/Super-Duper-Secure-Mode/)
- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
