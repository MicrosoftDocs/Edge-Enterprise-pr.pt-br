---
title: Solução de problemas e perguntas frequentes do modo IE
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 11/03/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Solução de problemas e perguntas frequentes para o modo Microsoft Edge Internet Explorer
ms.openlocfilehash: 651fc438e64c21e33787724fb3d5931f0f5b75fa
ms.sourcegitcommit: 4ec03873a85f065d9bfa6203cfe6c3e938f79bc5
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2021
ms.locfileid: "12155138"
---
# <a name="internet-explorer-ie-mode-troubleshooting-and-faq"></a>Solução de problemas e perguntas frequentes do modo do Internet Explorer (IE)

> [!NOTE]
> O aplicativo de área de trabalho do Internet Explorer 11 será retirado e ficará sem suporte em 15 de junho de 2022. Para ver a lista do que está no escopo, consulte Perguntas frequentes sobre a aposentadoria do aplicativo de área de trabalho do [Internet Explorer 11.](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/internet-explorer-11-desktop-app-retirement-faq/ba-p/2366549) Os mesmos aplicativos e sites do IE11 que você usa hoje podem abrir no Microsoft Edge com o modo Internet Explorer. Para saber mais, confira O futuro do [Internet Explorer no](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/) Windows 10 está Microsoft Edge postagem no blog.

Este artigo fornece dicas de solução de problemas e perguntas frequentes sobre o Microsoft Edge versão 77 ou posterior.

> [!NOTE]
> Este artigo se aplica ao Microsoft Edge versão 77 ou posterior.

## <a name="troubleshoot-ie-mode"></a>Solucionar problemas do modo IE

Use as informações desta seção para diagnosticar e corrigir problemas do modo IE.

### <a name="internet-explorer-mode--general-diagnostic-information"></a>Informações gerais de diagnóstico do modo Internet Explorer

Você pode obter informações de diagnóstico do modo Internet Explorer na guia Compatibilidade do Microsoft Edge. Para abrir esta guia, vá para *edge://compat/iediagnostic*. Esta página pode mostrar mensagens de diagnóstico. Esta página também fornece informações de configuração para as seguintes categorias:

- **Verificação de chave de registro.** (Exibido apenas se a verificação falhar.) Verifica se a integração com o Internet Explorer está configurada corretamente no registro. Caso não seja, o usuário poderá selecionar **Corrigir para** resolver o problema.
- **Modo Internet Explorer.** Mostra a versão da API usada, com base na configuração e no SO. Se houver algum problema, o usuário poderá ser solicitado a instalar uma atualização do Windows Update.
- **Configuração do modo Internet Explorer.** Mostra se o modo Internet Explorer está ativado e como está configurado.
- **Linha de comando.** Mostra a cadeia de caracteres de linha de comando e as opções usadas para iniciar Microsoft Edge.
- **Configurações de política de grupo.** Mostra se o modo IE está configurado usando políticas de grupo, e as políticas que estão aplicadas.

### <a name="error-message-to-open-this-page-in-internet-explorer-mode-reinstall-microsoft-edge-with-administrator-privileges"></a>Mensagem de erro: "Para abrir esta página no modo Internet Explorer, reinstale o Microsoft Edge com privilégios de administrador".

Você pode ver esse erro se não tiver todas as atualizações Windows necessárias. Consulte os pré-requisitos listados em [Sobre o modo IE](./edge-ie-mode.md) para obter as versões necessárias do Windows e Microsoft Edge.

Se você já instalou todas as atualizações necessárias Windows, você poderá ver esse erro se:

- Você estiver usando o canal Canary, que é instalado no nível do usuário por padrão.
- Você estiver usando o canal Estável, Beta ou Dev, mas quando solicitada a elevação durante a instalação, a elevação foi cancelada. Quando você cancelar o prompt de elevação, a instalação continuará no nível do usuário.
- O Internet Explorer 11 foi desabilitado nos Recursos do Windows.

As soluções possíveis são:

- Execute o instalador para qualquer canal no nível do sistema: `installer.exe --system-level`.
- Habilite o Internet Explorer 11 nos Recursos do Windows.

Para verificar se o Microsoft Edge está instalado no nível do sistema, digite "edge://versão" na barra de endereços do Microsoft Edge. O caminho do executável mostrará um caminho que começa com *C:\Arquivos de Programas*, o que indica uma instalação do sistema. Se o caminho executável começar com *C:\Users*, desinstalar e reinstalar Microsoft Edge com privilégios de administrador.

### <a name="error-message-to-open-this-page-in-ie-mode-try-restarting-microsoft-edge"></a>Mensagem de erro "Para abrir essa página no modo IE, tente reiniciar Microsoft Edge".

Você pode ver esse erro se houver um erro inesperado no Internet Explorer. Reiniciar o Microsoft Edge geralmente corrige esse erro.

### <a name="error-message-turn-off-remote-debugging-to-open-this-site-in-ie-mode-otherwise-it-might-not-work-as-expected"></a>Mensagem de erro: "Desative a depuração remota para abrir este site no modo IE. Caso contrário, talvez ele não funcione como esperado".

Você pode ver esse erro se estiver depurando remotamente e navegar até uma página da Web configurada para ser executado no modo IE. Você pode continuar, mas a página será renderizada usando o Microsoft Edge.

### <a name="error-message-could-not-retrieve-emie-site-list"></a>Mensagem de erro: "Não foi possível recuperar a lista de sites emIE".

Você pode ver esse erro na *página* edge://compat/enterprise indicando que o download da lista de sites falhou. A partir da versão 87 do Microsoft Edge, quando os cookies são bloqueados para solicitações de terceiros usando a política [BlockThirdPartyCookies](/deployedge/microsoft-edge-policies#blockthirdpartycookies), a autenticação HTTP também não é permitida. Você pode permitir cookies para o domínio específico que hospeda sua Lista de Sites do Modo Empresarial usando a política [CookiesAllowedForURLs](/deployedge/microsoft-edge-policies#cookiesallowedforurls) para garantir que os downloads da lista de sites sejam bem-sucedidos.

## <a name="frequently-asked-questions"></a>Perguntas Frequentes

### <a name="will-ie-mode-replace-internet-explorer-11"></a>O modo IE substituirá o Internet Explorer 11?

Sim, o aplicativo de área de trabalho do Internet Explorer 11 será retirado e ficará sem suporte em 15 de junho de 2022. Para ver o que está no escopo, consulte [Perguntas frequentes sobre](/lifecycle/faq/internet-explorer-microsoft-edge)ciclo de vida - Internet Explorer . Os mesmos aplicativos e sites do IE11 que você usa hoje podem abrir no Microsoft Edge com o modo Internet Explorer. Para saber mais, leia [O futuro do Internet Explorer no](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/)Windows 10 está Microsoft Edge .

### <a name="how-can-i-debug-my-legacy-application-while-using-ie-mode-on-microsoft-edge"></a>Como posso depurar meu aplicativo herdável usando o modo IE no Microsoft Edge?

Você pode usar o IEChooser para iniciar o Internet Explorer DevTools para depurar o conteúdo de suas guias de modo IE. Para usar o IEChooser, siga estas etapas:

1. Abra IEChooser.
   - Abra a caixa de diálogo Executar. Por exemplo, pressione `Windows logo key`  +  `R` o .
   - Insira `%systemroot%\system32\f12\IEChooser.exe` e selecione **Ok**.
2. No IEChooser, selecione a entrada para a guia Modo IE.

### <a name="can-i-test-a-site-in-microsoft-edge-while-it-is-configured-to-open-ie-mode-in-the-enterprise-mode-site-list"></a>Posso testar um site em Microsoft Edge enquanto ele está configurado para abrir o modo IE na lista de sites Enterprise modo?

Sim, enquanto você está modernizando seus sites herdados, você pode testar aplicativos configurados no modo IE Microsoft Edge. Para fazer isso, você pode executar Microsoft Edge com o sinalizador `--ie-mode-test` de linha de comando. Certifique-se de que não haja Microsoft Edge instâncias em execução. Em seguida, você pode **selecionar Configurações e mais** (o ícone de releitos ...) **> ferramentas mais > abrir sites no modo de borda.**

### <a name="can-i-use-view-in-file-explorer-in-sharepoint-online-on-microsoft-edge"></a>Posso usar "Exibir no Explorador de Arquivos" no SharePoint Online no Microsoft Edge?

A partir Microsoft Edge versão 95, você pode habilitar o recurso Exibir no **Explorador** de Arquivos para SharePoint bibliotecas de documentos modernas online. Para que essa experiência seja visível e funcione para seus usuários, você precisará habilitar Microsoft Edge política "Configurar o recurso Exibir no Explorador de Arquivos para páginas SharePoint [em Microsoft Edge"](/deployedge/microsoft-edge-policies#configureviewinfileexplorer) e atualizar sua configuração de locatário do SharePoint Online. Saiba mais: Exibir SharePoint arquivos com o Explorador de [Arquivos no Microsoft Edge - SharePoint no Microsoft 365 | Microsoft Docs](/SharePoint/sharepoint-view-in-edge).

No entanto, em vez de usar a opção Exibir no Explorador de Arquivos, [a](https://support.microsoft.com/office/sync-sharepoint-and-teams-files-with-your-computer-6de9ede8-5b6e-4503-80b2-6190f3354a88?ui=en-us&rs=en-us&ad=us) abordagem recomendada para gerenciar arquivos e pastas fora do SharePoint é sincronizar arquivos SharePoint e Teams com seu computador ou Mover ou copiar arquivos em SharePoint [.](https://support.microsoft.com/office/move-or-copy-files-in-sharepoint-00e2f483-4df3-46be-a861-1f5f0c1a87bc?ui=en-us&rs=en-us&ad=us)

### <a name="does-ie-mode-on-microsoft-edge-support-the-no-merge-option-that-was-supported-in-internet-explorer-11"></a>O modo IE no Microsoft Edge dá suporte à opção "não mesclar" suportada no Internet Explorer 11?

As alternativas recomendadas para a funcionalidade sem mesclagem no Microsoft Edge são uma das seguintes ações:

1. Use Perfis no Microsoft Edge - Cada perfil mapeia para uma sessão de IE diferente para páginas de modo IE, para que ele se comporte de forma idêntica à opção sem mesclagem.
2. Use a linha de comando`--user-data-dir=<path>`, mas com um caminho diferente para cada sessão. Se necessário, você pode criar um utilitário para que o execute de forma que ambos inicializem o Microsoft Edge e altera o caminho da sessão.

Se nenhuma das opções anteriores funcionar para seu cenário, a partir da Microsoft Edge versão 93, o modo IE no Microsoft Edge dará suporte à não mesclagem. Para um usuário final, quando uma nova janela do navegador é lançada de um aplicativo de modo IE, ela estará em uma sessão separada, como o comportamento sem mesclagem no IE11.

Para cada janela Microsoft Edge, a primeira vez que uma guia modo IE é visitada dentro dessa janela, se for um site designado "sem mesclagem", essa janela será bloqueada em uma sessão de IE diferente "sem mesclagem".  Essa janela permanece bloqueada de todas as outras janelas Microsoft Edge até que a última guia modo IE seja fechada na janela bloqueada. Isso segue o comportamento anterior em que os usuários podiam iniciar o IE sem mesclagem e iniciar Microsoft Edge sem mesclar usando outros mecanismos. Todos os sites abertos em uma nova janela (por meio de window.open) respeitarão a natureza de mesclagem do processo pai.

> [!NOTE]
> Não há suporte para alternamento de sessão. As navegação na mesma guia modo IE usarão a mesma sessão.

Você pode validar o comportamento sem mesclagem na Microsoft Edge versão 93 ou posterior seguindo estas etapas:

1. Verifique se o modo IE está habilitado na Microsoft Edge versão 93 ou posterior.
2. Você pode configurar sites que precisam impedir o compartilhamento de sessão na lista de sites do modo Enterprise definindo o valor do atributo merge-type como "no-merge". Esse atributo não é aplicável somente quando o elemento open-in é definido como Microsoft Edge. Por padrão, todos os sites têm um valor de mesclagem do tipo merge. (**Observação:** **a** ferramenta de gerenciador ** de lista de sites integrada disponível no edge://compat/sitelistmanager inclui uma caixa de seleção Sem mesclagem quando você adiciona ou edita um site.)

   ```
   <site url="contoso.com">
   <open-in merge-type="no-merge">IE11</open-in>
   </site>
   ```

3. Navegue até qualquer site configurado como sem mesclagem. O site deve estar em sua própria sessão de IE não mesclada. Quando você abre outra Microsoft Edge ou janela e navega para o mesmo site, ela deve estar em sua própria sessão do IE. Observe que há vários processos iexplore.exe no Gerenciador de Tarefas.

Se você tiver algum comentário, entre em contato com um de nossos canais de comentários: suporte da Microsoft ou fórum [TechCommunity.](https://techcommunity.microsoft.com/t5/enterprise/bd-p/EdgeInsiderEnterprise)

### <a name="can-i-save-links-as-webpages-in-internet-explorer-mode"></a>Posso salvar links como páginas da Web no modo Internet Explorer?

Sim, você pode habilitar a opção Salvar destino como no menu de contexto do modo Internet Explorer no Microsoft Edge. Para fazer isso, configure a política de grupo "*Allow Save Target As in Internet Explorer mode*" localizada em Configuração do Computador > Modelos *Administrativos > Windows Componentes > Internet Explorer*. O mecanismo de salvamento funciona da mesma forma que no Internet Explorer, e se o destino for salvo como um arquivo html, a reabertura do arquivo renderizará a página no Microsoft Edge.

A capacidade de salvar links como páginas da Web exige as seguintes atualizações mínimas do sistema operacional:

- Windows 10, versão 2004, Windows Server, versão 2004, Windows 10, versão 20H2: [KB4580364](https://support.microsoft.com/help/4580364/windows-10-update-kb4580364)
- Windows 10, versão 1903, Windows 10, versão 1909, Windows Server, versão 1903: [KB4580386](https://support.microsoft.com/help/4580386/windows-10-update-kb4580386)
- Windows 10, versão 1809, Windows Server, versão 1809, Windows Server 2019: [KB4580390](https://support.microsoft.com/help/4580390/windows-10-update-kb4580390)
- Windows 10, versão 1803: [KB4586785](https://support.microsoft.com/help/4586785/windows-10-update-kb4586785)
- Windows 10, versão 1607: [KB4586830](https://support.microsoft.com/help/4586830/windows-10-update-kb4586830)
- Windows 10, versão 1507: [KB4586787](https://support.microsoft.com/help/4586787/windows-10-update-kb4586787)

### <a name="can-i-test-a-site-in-microsoft-edge-while-it-is-configured-to-open-ie-mode-in-the-enterprise-mode-site-list"></a>Posso testar um site em Microsoft Edge enquanto ele está configurado para abrir o modo IE na lista de sites Enterprise modo?

Sim, enquanto você está modernizando seus sites herdamentos, você pode testar sites de modo IE em Microsoft Edge. Para fazer isso, você pode executar Microsoft Edge com o sinalizador `--ie-mode-test` de linha de comando. Certifique-se de que não haja Microsoft Edge instâncias em execução. Em **seguida, selecione Configurações e mais** (o ícone de releitos) ... **> ferramentas mais > abrir sites no modo de borda.**

### <a name="my-application-requires-transferring-post-data-between-ie-mode-and-microsoft-edge-is-this-supported"></a>Meu aplicativo requer a transferência de dados POST entre o modo IE e Microsoft Edge. Há suporte para isso?

A partir canal Microsoft Edge Beta versão 96, as navegação que alternam entre o modo Internet Explorer e o Microsoft Edge incluirão dados de formulário e cabeçalhos HTTP adicionais. No entanto, se os dados do formulário incluirem anexos de arquivo, eles não serão transferidos entre os mecanismos. Você pode escolher quais tipos de dados devem ser incluídos em tais navegaçãos usando a política de grupo [InternetExplorerIntegrationComplexNavDataTypes.](/deployedge/microsoft-edge-policies#internetexplorerintegrationcomplexnavdatatypes)

Além de Microsoft Edge versão 96, você precisa ter as seguintes atualizações Windows instaladas para esta experiência:

- Windows 10 versão 2004; Windows Servidor versão 2004; Windows 10 versão; Windows Servidor versão 20H2 e Windows 10 versão 21H1 - KB5006738 ou posterior

  > [!NOTE]
  > As atualizações Windows 10 versão 19H2, Windows Server 2022 e Windows 11 estão chegando em breve.

## <a name="see-also"></a>Consulte também
  
- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Sobre o modo IE](./edge-ie-mode.md)
- [Informações adicionais sobre o Modo Empresarial](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
