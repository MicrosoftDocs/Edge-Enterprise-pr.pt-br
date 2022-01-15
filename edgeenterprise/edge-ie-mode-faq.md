---
title: Solução de problemas e perguntas frequentes do modo IE
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 12/13/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Guia de solução de problemas e perguntas frequentes Microsoft Edge modo Internet Explorer
ms.openlocfilehash: 3c8a4d236a64d338e0ade15dccc37897b5d9a5bf
ms.sourcegitcommit: e7f3098d8b7d91cae20b5778a71a87daababc312
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/15/2022
ms.locfileid: "12297999"
---
# <a name="internet-explorer-ie-mode-troubleshooting-and-faq"></a>Solução de problemas e perguntas frequentes do modo do Internet Explorer (IE)

> [!NOTE]
> O aplicativo de área de trabalho do Internet Explorer 11 será retirado e ficará sem suporte em 15 de junho de 2022. Para ver a lista do que está no escopo, consulte Perguntas frequentes sobre a aposentadoria do aplicativo de área de trabalho do [Internet Explorer 11.](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/internet-explorer-11-desktop-app-retirement-faq/ba-p/2366549) Os mesmos aplicativos e sites do IE11 que você usa hoje podem abrir no Microsoft Edge com o modo Internet Explorer. Para saber mais, confira O futuro do [Internet Explorer no](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/) Windows 10 está Microsoft Edge postagem no blog.

Este artigo fornece dicas de solução de problemas e perguntas frequentes sobre o Microsoft Edge versão 77 ou posterior.

> [!NOTE]
> Este artigo se aplica ao Microsoft Edge versão 77 ou posterior.

## <a name="common-ie-mode-issues"></a>Problemas comuns do modo IE

Use esta seção como um guia para ajudá-lo a solucionar problemas e corrigir os dois problemas mais comuns ao mover para Microsoft Edge com o modo IE. Esses problemas são:

- Configurações incorretas do modo documento
- Configurações de site neutras incompletas

### <a name="incorrect-document-mode-configurations"></a>Configurações incorretas do modo documento

Esta seção descreve os sintomas e dá etapas para diagnosticar e corrigir esse problema.

#### <a name="symptoms"></a>Sintomas

Os usuários terão os seguintes sintomas:
  
- O reacionamento e o posicionamento dos elementos de página podem estar desligados ou podem estar ausentes 
- Algumas funcionalidades podem ser perdidas ou não funcionar como esperado. Por exemplo, os botões que funcionaram com o Internet Explorer não fazem nada ou retornam um erro.

#### <a name="how-to-troubleshoot-and-fix"></a>Como solucionar problemas e corrigir

A estratégia geral é duplicar as mesmas configurações que funcionaram com o Internet Explorer 11 para um site específico em nossa entrada de lista de sites do modo IE. Use a guia "Emulação" da barra de ferramentas do desenvolvedor F12 no IE 11, mostrada na próxima captura de tela para investigar o cenário que você deseja corrigir. Para abrir a barra de ferramentas Desenvolvedor, pressione a tecla F12 e selecione **Abrir DevTools**.

![Guia Emulação no exibição DevTools](./media/edge-ie-mode-faq/edge-ie-mode-emulation-tab.png)

A guia Emulação mostra duas informações para se concentrar: o modo de documento (1) e o texto abaixo da lista suspenso (2). Essas informações podem ajudar a explicar por que estamos no modo 11 (Padrão) para a página ou site que estamos olhando.

Há mensagens diferentes que podem ser exibidas para o modo Documento e, em nosso exemplo, elas são:
  
- Via meta tag compatível com X-UA
- Por meio do cabeçalho HTTP compatível com X-UA

As duas opções X-UA-Compatible indicam que a página da Web ou o servidor Web onde o site está hospedado, está mostrando o modo de documento que deve ser usado pelo navegador.  
Queremos honrar o modo de documento em quase todos os casos. Para fazer isso, precisamos selecionar um dos seguintes modos na entrada da lista de sites do modo IE para o site:

- Padrão
- IE8 Enterprise
- IE7 Enterprise

Essas opções respeitam a página da Web ou as diretivas do servidor Web. Lembre-se de que precisamos selecionar uma opção que inclua o modo de documento especificado. No exemplo de captura de tela, como o modo de documento especificado é 11, selecionamos "Padrão" porque o IE8 Enterprise e o IE7 Enterprise não suportam o modo de documento do IE 11.  

Se o modo Documento indicar que um dos modos de exibição de compatibilidade a seguir é necessário para o site, a configuração será simples.

- Por meio das configurações de modo de exibição de compatibilidade local
- Por meio da lista de exibição de compatibilidade
- Por meio das configurações de compatibilidade da intranet

Como todas as configurações de Modo de Exibição de Compatibilidade resultam no comportamento "IE7 Enterprise", escolha essa configuração na seção "Modo dePat" da entrada da lista de sites do modo IE.

Para obter mais informações sobre a lógica que o modo Internet Explorer ou IE usa para pousar em um modo de doc sobre outro, consulte o artigo Modos de documento preterido e o artigo do [Internet Explorer 11.](/internet-explorer/ie11-deploy-guide/deprecated-document-modes)

A regra geral é usar o modo mais atual baseado em lógica que permite que um determinado site funcione conforme esperado. Começamos com o modo Padrão, movemos para o modo Enterprise IE8 e, em seguida, para o modo Enterprise IE7. Essa seleção oferece às páginas filho a flexibilidade de usar diferentes modos de documento conforme necessário por meio da lógica interna para suas necessidades específicas. Como resultado, todas as páginas do site não são bloqueadas em um modo de documento específico.  

A tabela a seguir lista os modos de documento disponíveis para essas configurações.

| Modo baseado em lógica | Padrão | IE8 Enterprise | IE7 Enterprise |
|--|--|--|--|
| Modos de documento disponíveis | Modo doc do IE11<br> Modo Doc do IE10<br>Modo Doc do IE9<br> Modo doc do IE8<br>Modo doc do IE7<br>Modo IE5 Quirks | Modo doc do IE8<br>Modo doc do IE7<br>Modo IE5 Quirks   | Modo doc do IE7<br>Modo IE5 Quirks  |

> [!NOTE]
> Em alguns casos, um site ou página específico requer um modo de documento específico para funcionar conforme projetado. Recomendamos que as opções explícitas do modo Documento só sejam usadas quando as opções baseadas em lógica não são eficazes.

### <a name="incomplete-neutral-site-configurations"></a>Configurações de site neutras incompletas

Esta seção descreve os sintomas e dá etapas para diagnosticar e corrigir esse problema.

#### <a name="symptoms"></a>Sintomas
  
Uma página depende do SSO para autenticação, mas os usuários são solicitados várias vezes para credenciais, experimentam um comportamento de redirecionamento de loop, erros de autenticação com falha ou alguma combinação desses sintomas.
  
#### <a name="how-to-troubleshoot-and-fix"></a>Como solucionar problemas e corrigir
  
Antes de começar a analisar um fluxo de trabalho com falha na Microsoft Edge, consulte a barra de endereços para o logotipo do modo "e" do IE, mostrado na próxima captura de tela.

![Logotipo do IE Microsoft Edge barra de menus.](./media/edge-ie-mode-faq/edge--ie-mode-logo.png)

Se, durante o processo de autenticação SSO, virmos o "e", mas ele desaparecer após um redirecionamento, isso aponta para um site neutro ausente. Depois Microsoft Edge cair no modo IE, precisamos ficar lá para manter informações de sessão e cookie. Se a URL aparecer na barra de endereços tempo suficiente para identificá-la, adicione-a à lista de sites do modo IE como um site neutro usando as etapas descritas em [Configure neutral sites](/deployedge/edge-ie-mode-sitelist#configure-neutral-sites).

Muitas vezes, o ciclo de redirecionamento acontece tão rapidamente que é difícil identificar os sites neutros ausentes. Para ajudar nessa análise, usamos uma ferramenta interna no mecanismo Chromium: **net-export**.

> [!TIP]
> Os rastreamentos de rede são inerentemente barulhentos. Para minimizar o ruído, feche todas as outras instâncias e guias do navegador que não são necessárias para o fluxo de trabalho específico que você está investigando.

As etapas a seguir descrevem como solucionar problemas de uma configuração de site neutra.
  
1. Abra uma nova guia no Microsoft Edge e vá para *edge://net-export*.
2. Selecione **Iniciar o log em disco**e escolha um local onde você deseja salvar o log .json resultante. Esse log pode ser excluído com segurança após concluir a solução de problemas.
3. Abra outra guia (mantenha a guia net-export aberta) e repita o fluxo de trabalho com falha.
4. Depois de concluir, volte para a guia net-export e selecione **Parar Registro em Log**.
5. Selecione o hiperlink "visualizador de netlog".
6. Na página resultante, selecione **Escolher Arquivo**e, em seguida, escolha o arquivo .json que você criou na etapa 2.
7. Depois que o arquivo de log for carregado, selecione **Eventos** no menu do lado esquerdo.
8. Role pelo log de rede e identifique a URL inicial. (Você também pode usar a função de pesquisa para encontrar seu ponto de partida.)
9. Desde o ponto inicial, role para baixo e procure URLs no fluxo de trabalho que não tenham uma entrada na lista de sites do modo IE. Preste atenção especial às URLs com indicadores para SSO, AUTH, LOGIN e assim por diante.
10. Depois de identificar uma URL de candidato, adicione-a à lista de sites do modo IE como um site neutro selecionando **Nenhum** no menu suspenso Abrir. Teste o fluxo de trabalho novamente.

Em alguns casos, várias entradas de site neutras são necessárias, dependendo da arquitetura de site específica. Se o fluxo de trabalho ainda falhar após adicionar um novo site neutro, repita o processo para capturar um novo log de exportação de rede e executar outra passagem.

Em algumas instâncias raras, pode ser necessário configurar cookies compartilhados específicos para garantir que as informações necessárias chegue aos sites do modo IE. Se você estiver ciente de um cookie específico necessário, você poderá configurar o compartilhamento de cookies usando as etapas descritas em [compartilhamento](/deployedge/edge-ie-mode-add-guidance-cookieshare)de cookies do Microsoft Edge para o Internet Explorer .

## <a name="what-if-these-steps-dont-fix-the-issue"></a>E se essas etapas não corrigirem o problema?

Este artigo foi projetado para ajudar a solucionar problemas mais comuns de configuração do modo IE, mas pode não abranger todos os cenários possíveis. Se você encontrar um problema com o que não pode corrigir e precisar de ajuda, entre em contato com o App Assure at e ajudaremos você [https://aka.ms/AppAssure](https://aka.ms/AppAssure) com seu problema.

## <a name="get-general-diagnostic-and-configuration-information"></a>Obter informações gerais de diagnóstico e configuração

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

Você pode ver esse erro na *página* edge://compat/enterprise indicando que o download da lista de sites falhou. A partir Microsoft Edge versão 87, quando cookies são bloqueados para solicitações de terceiros usando a [política BlockThirdPartyCookies,](/deployedge/microsoft-edge-policies#blockthirdpartycookies) a autenticação HTTP também não é permitida. Você pode permitir cookies para o domínio específico que hospeda sua Lista de Sites do Modo Empresarial usando a política [CookiesAllowedForURLs](/deployedge/microsoft-edge-policies#cookiesallowedforurls) para garantir que os downloads da lista de sites sejam bem-sucedidos.

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

Sim, enquanto você está modernizando seus sites herdados, você pode testar aplicativos configurados no modo IE Microsoft Edge. Para testar esses aplicativos, você pode configurar a [política InternetExplorerModeTabInEdgeModeAllowed.](/deployedge/microsoft-edge-policies#internetexplorermodetabinedgemodeallowed) Se você habilitar essa política, os usuários poderão abrir sites de modo IE no Microsoft Edge selecionando Configurações e mais **(o** ícone de replicação ...) > **Mais**Ferramentas Abrir sites no modo borda  >  ****.

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

### <a name="my-application-requires-transferring-post-data-between-ie-mode-and-microsoft-edge-is-this-supported"></a>Meu aplicativo requer a transferência de dados POST entre o modo IE e Microsoft Edge. Há suporte para isso?

A partir canal Microsoft Edge Beta versão 96, as navegação que alternam entre o modo Internet Explorer e o Microsoft Edge incluirão dados de formulário e cabeçalhos HTTP adicionais. No entanto, se os dados do formulário incluirem anexos de arquivo, eles não serão transferidos entre os mecanismos. Você pode escolher quais tipos de dados devem ser incluídos em tais navegaçãos usando a política de grupo [InternetExplorerIntegrationComplexNavDataTypes.](/deployedge/microsoft-edge-policies#internetexplorerintegrationcomplexnavdatatypes)

Além de Microsoft Edge versão 96, você precisa ter as seguintes atualizações Windows instaladas para esta experiência:

- Windows 11 [KB5007262](https://support.microsoft.com/topic/november-22-2021-kb5007262-os-build-22000-348-preview-7f3e18d7-4189-4882-b0e9-afc920253aee) ou posterior
- Windows Server 2022 [KB5007254](
https://support.microsoft.com/topic/november-22-2021-kb5007254-os-build-20348-380-preview-9a960291-d62e-486a-adcc-6babe5ae6fc1) ou posterior
- Windows 10 versão 2004; Windows Server versão 2004; Windows 10 versão; Windows Server versão 20H2 e Windows 10 versão 21H1 - [KB5006738](https://support.microsoft.com/topic/october-26-2021-kb5006738-os-builds-19041-1320-19042-1320-and-19043-1320-preview-ccbce6bf-ae00-4e66-9789-ce8e7ea35541) ou posterior
- Windows 10 versão 1909 [KB5007189](
https://support.microsoft.com/topic/november-9-2021-kb5007189-os-build-18362-1916-91b4647c-9979-4d84-8e64-efc8674e8c1f) ou posterior

## <a name="see-also"></a>Consulte também
  
- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Sobre o modo IE](./edge-ie-mode.md)
- [Informações adicionais sobre o Modo Empresarial](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
