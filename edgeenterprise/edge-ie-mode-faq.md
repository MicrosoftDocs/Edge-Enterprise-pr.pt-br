---
title: Solução de problemas e perguntas frequentes do modo internet explorer (IE)
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 04/25/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Guia de solução de problemas e perguntas frequentes Microsoft Edge modo Internet Explorer
ms.openlocfilehash: 44b51664592c1b8bdadc78f5d6521b9d53d5b342
ms.sourcegitcommit: 2d3e2a7180e2df82b6345865c201ad64731cbda7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/12/2022
ms.locfileid: "12582116"
---
# <a name="internet-explorer-ie-mode-troubleshooting-and-faq"></a>Solução de problemas e perguntas frequentes do modo internet explorer (IE)

> [!NOTE]
> O aplicativo da área de trabalho do Internet Explorer 11 será desativado e ficará sem suporte em 15 de junho de 2022. Para ver a lista do que está no escopo, confira as perguntas frequentes sobre desativação do aplicativo da área de trabalho do [Internet Explorer 11](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/internet-explorer-11-desktop-app-retirement-faq/ba-p/2366549). Os mesmos aplicativos e sites do IE11 que você usa hoje podem abrir no Microsoft Edge com o modo Internet Explorer. Para saber mais, confira [O futuro do Internet Explorer no Windows 10 está Microsoft Edge](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/) postagem no blog.

Este artigo fornece dicas de solução de problemas e perguntas frequentes Microsoft Edge versão 77 ou posterior.

> [!NOTE]
> Este artigo se aplica ao Microsoft Edge versão 77 ou posterior.

## <a name="what-if-i-need-help-with-setting-up-microsoft-edge-or-internet-explorer-mode"></a>E se eu precisar de ajuda para configurar o Microsoft Edge ou o modo Internet Explorer?

Oferecemos várias opções de suporte. Se você tiver Suporte Unificado da Microsoft, entre em contato com esse serviço de suporte para obter ajuda com a transição. Também  [há FastTrack,](https://www.microsoft.com/en-us/fasttrack/microsoft-365/microsoft-edge?rtc=1) disponível sem custo adicional para clientes com 150 ou mais estações pagas de Windows 10.

Também recomendamos nosso guia Microsoft Edge + modo Internet Explorer [Introdução e](https://query.prod.cms.rt.microsoft.com/cms/api/am/binary/RWEHMs) nossa [série de blogs do modo IE](https://techcommunity.microsoft.com/t5/windows-10/internet-explorer-to-microsoft-edge-with-ie-mode-blog-series/m-p/2617124).

## <a name="are-there-any-tools-that-i-can-use-to-guide-me-through-ie-mode-troubleshooting"></a>Há alguma ferramenta que eu possa usar para me orientar na solução de problemas do modo IE?

Sim, o [Microsoft Virtual Agent fornece](https://go.microsoft.com/fwlink/?linkid=2194137) um passo a passo guiado baseado em cenário para solucionar problemas do modo IE.

## <a name="common-ie-mode-issues"></a>Problemas comuns do modo IE

Use esta seção como um guia para ajudá-lo a solucionar e corrigir os dois problemas mais comuns ao passar para o Microsoft Edge com o modo IE. Esses problemas são:

- Configurações incorretas do modo documento
- Configurações de site neutras incompletas

### <a name="incorrect-document-mode-configurations"></a>Configurações incorretas do modo documento

Esta seção descreve os sintomas e fornece etapas para diagnosticar e corrigir esse problema.

#### <a name="symptoms"></a>Sintomas

Os usuários terão os seguintes sintomas:
  
- O dimensionamento e o posicionamento de elementos de página podem estar desativados ou podem estar ausentes 
- Algumas funcionalidades podem ser perdidas ou não funcionar conforme o esperado. Por exemplo, os botões que funcionaram com o Internet Explorer não fazem nada ou retornam um erro.

#### <a name="how-to-troubleshoot-and-fix"></a>Como solucionar problemas e corrigir

A estratégia geral é duplicar as mesmas configurações que funcionaram com o Internet Explorer 11 para um site específico em nossa lista de sites do modo IE. Use a guia "Emulação" da Barra de Ferramentas do Desenvolvedor F12 no IE 11, mostrada na próxima captura de tela para investigar o cenário que você deseja corrigir. Para abrir a barra de ferramentas desenvolvedor, pressione a tecla F12 e selecione **Abrir DevTools**.

![Guia Emulação no modo de exibição DevTools](./media/edge-ie-mode-faq/edge-ie-mode-emulation-tab.png)

A guia Emulação mostra duas informações nas quais se concentrar: o modo documento (1) e o texto abaixo da lista suspensa (2). Essas informações podem ajudar a explicar por que estamos no modo 11 (Padrão) para a página ou site que estamos vendo.

Há mensagens diferentes que podem ser exibidas para o modo Documento e, em nosso exemplo, elas são:
  
- Por meio de meta tag compatível com X-UA
- Por meio do cabeçalho HTTP compatível com X-UA

As duas opções compatíveis com X-UA indicam que a página da Web ou o servidor Web onde o site está hospedado está mostrando o modo de documento que deve ser usado pelo navegador.  

Queremos honrar o modo de documento em quase todos os casos. Para fazer isso, precisamos selecionar um dos seguintes modos na entrada de lista de sites do modo IE para o site:

- Padrão
- IE8 Enterprise
- IE7 Enterprise

Essas opções respeitam a página da Web ou as diretivas do servidor Web. Lembre-se de que precisamos selecionar uma opção que inclua o modo de documento especificado. No exemplo de captura de tela, como o modo de documento especificado é 11, selecionamos "Padrão" porque o IE8 Enterprise e o IE7 Enterprise não dão suporte ao modo de documento do IE 11.  

Se o modo documento indicar que uma das exibições de compatibilidade a seguir é necessária para o site, a definição de configuração é simples.

- Por meio das configurações de exibição de compatibilidade local
- Por meio da lista de exibição de compatibilidade
- Por meio das configurações de compatibilidade da intranet

Como todas as configurações de Exibição de Compatibilidade resultam no comportamento "IE7 Enterprise", escolha essa configuração na seção "Modo de Compatibilidade" da entrada da lista de sites do modo IE.

Para obter mais informações sobre a lógica que o Internet Explorer ou o modo IE usa para pousar em um modo de documento sobre outro, consulte o artigo Modos de documento preteridos e [o artigo do Internet Explorer 11](/internet-explorer/ie11-deploy-guide/deprecated-document-modes) .

A regra geral é usar o modo mais atual baseado em lógica que permite que um determinado site funcione conforme o esperado. Começaríamos com o modo Padrão, passaríamos para o modo de Enterprise IE8 e, em seguida, para o modo de Enterprise IE7, se necessário. Essa seleção oferece às páginas filho a flexibilidade de usar diferentes modos de documento conforme necessário por meio da lógica interna para suas necessidades específicas. Como resultado, todas as páginas do site não são bloqueadas em um modo de documento específico.  

A tabela a seguir lista os modos de documento disponíveis para essas configurações.

| Modo baseado em lógica | Padrão | IE8 Enterprise | IE7 Enterprise |
|--|--|--|--|
| Modos de documento disponíveis | Modo de documento do IE11<br> Modo de documento do IE10<br>Modo de documento do IE9<br> Modo de documento do IE8<br>Modo de documento do IE7<br>Modo de Peculiaridades do IE5 | Modo de documento do IE8<br>Modo de documento do IE7<br>Modo de Peculiaridades do IE5   | Modo de documento do IE7<br>Modo de Peculiaridades do IE5  |

> [!NOTE]
> Em alguns casos, um determinado site ou página requer um modo de documento específico para funcionar conforme projetado. Recomendamos que as opções explícitas do modo documento só devem ser usadas quando as opções baseadas em lógica não são eficazes.

### <a name="incomplete-neutral-site-configurations"></a>Configurações de site neutras incompletas

Esta seção descreve os sintomas e fornece etapas para diagnosticar e corrigir esse problema.

#### <a name="symptoms"></a>Sintomas
  
Uma página depende do SSO para autenticação, mas os usuários são solicitados várias vezes a fornecer credenciais, experimentar um comportamento de redirecionamento de loop, erros de autenticação com falha ou alguma combinação desses sintomas.
  
#### <a name="how-to-troubleshoot-and-fix"></a>Como solucionar problemas e corrigir
  
Antes de começar a analisar um fluxo de trabalho com falha no Microsoft Edge, examine a barra de endereços para o logotipo "e" do modo IE, mostrado na próxima captura de tela.

![Logotipo do IE na Microsoft Edge de menus.](./media/edge-ie-mode-faq/edge--ie-mode-logo.png)

Se, durante o processo de autenticação de SSO, virmos o "e", mas ele desaparecer após um redirecionamento, esse comportamento apontará para um site neutro ausente. Depois Microsoft Edge quedas no modo IE, precisamos permanecer lá para manter as informações de sessão e cookie. Se a URL aparecer na barra de endereços tempo suficiente para identificá-la, adicione-a à lista de sites do modo IE como um site neutro usando as etapas descritas em Configurar [sites neutros](/deployedge/edge-ie-mode-sitelist#configure-neutral-sites).

Geralmente, o ciclo de redirecionamento ocorre tão rapidamente que é difícil identificar os sites neutros ausentes. Para ajudar com essa análise, usamos uma ferramenta interna no Chromium: **net-export**.

> [!TIP]
> Os rastreamentos de rede são inerentemente barulhentos. Para minimizar o ruído, feche todas as outras instâncias e guias do navegador que não são necessárias para o fluxo de trabalho específico que você está investigando.

As etapas a seguir descrevem como solucionar problemas de uma configuração de site neutra.
  
1. Abra uma nova guia no Microsoft Edge e vá para *edge://net-export*.
2. Selecione **Iniciar Registro em Log no Disco** e, em seguida, escolha um local em que você deseja salvar o log .json resultante. Esse log pode ser excluído com segurança depois que você concluir a solução de problemas.
3. Abra outra guia (mantenha a guia net-export aberta) e repita o fluxo de trabalho com falha.
4. Depois de concluir, retorne à guia net-export e selecione **Parar Registro em Log**.
5. Selecione o hiperlink "visualizador de netlog".
6. Na página resultante, selecione **Escolher Arquivo** e, em seguida, escolha o arquivo .json criado na etapa 2.
7. Depois que o arquivo de log for carregado, selecione **Eventos** no menu do lado esquerdo.
8. Role pelo log de rede e identifique a URL inicial. (Você também pode usar a função de pesquisa para localizar seu ponto de partida.)
9. Do ponto de partida, role para baixo e procure URLs no fluxo de trabalho que não têm uma entrada na lista de sites do modo IE. Preste atenção especial às URLs com indicadores de SSO, AUTH, LOGIN e assim por diante.
10. Depois de identificar uma URL candidata, adicione-a à lista de sites do modo IE como um site neutro selecionando **Nenhum** na lista suspensa Abrir. Teste o fluxo de trabalho novamente.

Em alguns casos, várias entradas de site neutras são necessárias, dependendo da arquitetura de site específica em vigor. Se o fluxo de trabalho ainda falhar depois de adicionar um novo site neutro, repita o processo para capturar um novo log de exportação de rede e executar outra passagem.

Em alguns casos raros, pode ser necessário configurar cookies compartilhados específicos para garantir que as informações necessárias chegue aos sites do modo IE. Se você estiver ciente de um cookie específico necessário, poderá configurar o compartilhamento de cookies usando as etapas descritas no compartilhamento de [cookies do Microsoft Edge para o Internet Explorer](/deployedge/edge-ie-mode-add-guidance-cookieshare).

### <a name="what-if-these-steps-dont-fix-the-issue"></a>E se essas etapas não corrigirem o problema?

Este artigo foi projetado para ajudar a solucionar os problemas mais comuns de configuração do modo IE, mas pode não abranger todos os cenários possíveis. Se você encontrar um problema com o qual não é possível corrigir e precisa de ajuda, [https://aka.ms/AppAssure](https://aka.ms/AppAssure) entre em contato com a Garantia de Aplicativo e ajudaremos você com o problema.

## <a name="get-general-diagnostic-and-configuration-information"></a>Obter informações gerais de diagnóstico e configuração

Você pode obter informações de diagnóstico do modo Internet Explorer na guia Compatibilidade do Microsoft Edge. Para abrir esta guia, vá para *edge://compat/iediagnostic*. A página "Informações de diagnóstico do modo Internet Explorer" pode mostrar mensagens de diagnóstico e você pode exportar dados de diagnóstico para um arquivo xml. Essa página de informações de diagnóstico também fornece informações de configuração para as seguintes categorias:

- **Verificação de chave de registro.** (Exibido apenas se a verificação falhar.) Verifica se a integração com o Internet Explorer está configurada corretamente no registro. Caso contrário, o usuário poderá selecionar **Corrigir para** resolver o problema.
- **Modo Internet Explorer.** Mostra a versão da API usada, com base na configuração e no SO. Se houver algum problema, o usuário poderá ser solicitado a instalar uma atualização do Windows Update.
- **Configuração do modo Internet Explorer.** Mostra se o modo Internet Explorer está ativado e como está configurado.
- **Linha de comando.** Mostra a cadeia de caracteres de linha de comando e as opções usadas para iniciar Microsoft Edge.
- **Configurações de política de grupo.** Mostra se o modo IE está configurado usando políticas de grupo, e as políticas que estão aplicadas.

### <a name="error-message-to-open-this-page-in-internet-explorer-mode-reinstall-microsoft-edge-with-administrator-privileges"></a>Mensagem de erro: "Para abrir esta página no modo Internet Explorer, reinstale o Microsoft Edge com privilégios de administrador".

Você poderá ver esse erro se não tiver todas as atualizações Windows necessárias. Consulte os pré-requisitos listados em [Sobre o modo IE](./edge-ie-mode.md) para obter as versões necessárias do Windows e Microsoft Edge.

Se você já tiver instalado todas as atualizações Windows necessárias, poderá ver esse erro se:

- Você estiver usando o canal Canary, que é instalado no nível do usuário por padrão.
- Você estiver usando o canal Estável, Beta ou Dev, mas quando solicitada a elevação durante a instalação, a elevação foi cancelada. Quando você cancelar o prompt de elevação, a instalação continuará no nível do usuário.
- O Internet Explorer 11 foi desabilitado nos Recursos do Windows.

As soluções possíveis são:

- Execute o instalador para qualquer canal no nível do sistema: `installer.exe --system-level`.
- Habilite o Internet Explorer 11 nos Recursos do Windows.

Para verificar se o Microsoft Edge está instalado no nível do sistema, digite "edge://versão" na barra de endereços do Microsoft Edge. O caminho do executável mostrará um caminho que começa com *C:\Arquivos de Programas*, o que indica uma instalação do sistema. Se o caminho executável começar com *C:\Users*, desinstale e reinstale Microsoft Edge com privilégios de administrador.

### <a name="error-message-to-open-this-page-in-ie-mode-try-restarting-microsoft-edge"></a>Mensagem de erro "Para abrir esta página no modo IE, tente reiniciar Microsoft Edge".

Você poderá ver esse erro se houver um erro inesperado no Internet Explorer. Reiniciar o Microsoft Edge geralmente corrige esse erro.

### <a name="error-message-turn-off-remote-debugging-to-open-this-site-in-ie-mode-otherwise-it-might-not-work-as-expected"></a>Mensagem de erro: "Desative a depuração remota para abrir este site no modo IE. Caso contrário, talvez ele não funcione como esperado".

Você poderá ver esse erro se estiver depurando remotamente e navegar até uma página da Web configurada para execução no modo IE. Você pode continuar, mas a página será renderizada usando o Microsoft Edge.

### <a name="error-message-could-not-retrieve-emie-site-list"></a>Mensagem de erro: "Não foi possível recuperar a lista de sites da EMIE".

Você pode ver esse erro na página *edge://compat/enterprise* indicando que o download da lista de sites falhou. A partir Microsoft Edge versão 87, quando os cookies são bloqueados para solicitações de terceiros usando a política [BlockThirdPartyCookies](/deployedge/microsoft-edge-policies#blockthirdpartycookies), a autenticação HTTP também não é permitida. Você pode permitir cookies para o domínio específico que hospeda sua Lista de Sites do Modo Empresarial usando a política [CookiesAllowedForURLs](/deployedge/microsoft-edge-policies#cookiesallowedforurls) para garantir que os downloads da lista de sites sejam bem-sucedidos.

### <a name="error-message-the-connection-for-this-site-is-not-secure"></a>Mensagem de erro: "A conexão para este site não é segura"

Esse erro poderá ocorrer se você estiver tentando abrir um site herdado no modo IE e o site estiver configurado para ser executado no TLS 1.0 ou no TLS 1.1. Esses protocolos são desabilitados por padrão no Microsoft Edge. Para obter mais informações, consulte Plano de alteração [: TLS 1.0 e TLS 1.1 em breve serão desabilitados por padrão](https://blogs.windows.com/msedgedev/2020/03/31/tls-1-0-tls-1-1-schedule-update-edge-ie11/)

### <a name="error-message-this-form-cannot-be-opened-in-a-web-browser-to-open-this-form-use-microsoft-infopath"></a>Mensagem de erro: "Este formulário não pode ser aberto em um navegador da Web. Para abrir este formulário, use o Microsoft InfoPath"

Determinados aplicativos podem exigir que você carregue a página da Web no modo IE. Você pode usar o recurso de modo IE no Microsoft Edge.

Talvez você também precise definir o atributo na `compat-mode` lista de sites Enterprise modo **padrão**. Para obter mais informações, [consulte Enterprise modo e a lista de sites Enterprise modo de exibição](/internet-explorer/ie11-deploy-guide/what-is-enterprise-mode#enterprise-mode-and-the-enterprise-mode-site-list-1).

> [!TIP]
> Os usuários podem exibir facilmente essa lista de sites e o modo de compatibilidade digitando **about:compat** em Microsoft Edge.

## <a name="frequently-asked-questions"></a>Perguntas frequentes

### <a name="will-ie-mode-replace-internet-explorer-11"></a>O modo IE substituirá o Internet Explorer 11?

Sim, o aplicativo da área de trabalho do Internet Explorer 11 será desativado e ficará sem suporte em 15 de junho de 2022. Para ver o que está no escopo, consulte perguntas frequentes [sobre ciclo de vida – Internet Explorer](/lifecycle/faq/internet-explorer-microsoft-edge). Os mesmos aplicativos e sites do IE11 que você usa hoje podem abrir no Microsoft Edge com o modo Internet Explorer. Para saber mais, leia [O futuro do Internet Explorer Windows 10 está em Microsoft Edge](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/).

### <a name="can-i-use-view-in-file-explorer-in-sharepoint-online-on-microsoft-edge"></a>Posso usar "Exibir no Explorador de Arquivos" no SharePoint Online no Microsoft Edge?

A partir Microsoft Edge versão 95, você pode habilitar a exibição **** Explorador de Arquivos funcionalidade para bibliotecas de documentos modernas do SharePoint Online. Para que essa experiência fique visível e funcione para seus usuários, você precisará habilitar o recurso Microsoft Edge "Configurar a exibição no recurso Explorador de Arquivos para páginas do [SharePoint no Microsoft Edge"](/deployedge/microsoft-edge-policies#configureviewinfileexplorer) e atualizar sua configuração de locatário do SharePoint Online. Saiba mais: [Exibir SharePoint arquivos com Explorador de Arquivos no Microsoft Edge – SharePoint no Microsoft 365 | Microsoft Docs](/SharePoint/sharepoint-view-in-edge).

No entanto, em vez de usar a opção Exibir no Explorador de Arquivos, a abordagem recomendada para gerenciar arquivos e pastas fora do SharePoint é sincronizar arquivos SharePoint e [Teams](https://support.microsoft.com/office/sync-sharepoint-and-teams-files-with-your-computer-6de9ede8-5b6e-4503-80b2-6190f3354a88?ui=en-us&rs=en-us&ad=us) com seu computador ou mover ou copiar arquivos no [SharePoint](https://support.microsoft.com/office/move-or-copy-files-in-sharepoint-00e2f483-4df3-46be-a861-1f5f0c1a87bc?ui=en-us&rs=en-us&ad=us).

### <a name="does-ie-mode-on-microsoft-edge-support-the-no-merge-option-that-was-supported-in-internet-explorer-11"></a>O modo IE no Microsoft Edge dá suporte à opção "sem mesclagem" compatível com o Internet Explorer 11?

As alternativas recomendadas para a funcionalidade sem mesclagem no Microsoft Edge são uma das seguintes ações:

1. Usar Perfis no Microsoft Edge – cada perfil é mapeado para uma sessão do IE diferente para páginas do modo IE, portanto, ele se comporta de forma idêntica à opção sem mesclagem.
2. Use a linha de comando`--user-data-dir=<path>`, mas com um caminho diferente para cada sessão. Se necessário, você pode criar um utilitário para o usuário executar que inicia Microsoft Edge e altera o caminho para a sessão.

Se nenhuma das opções anteriores funcionar para seu cenário, a partir da Microsoft Edge versão 93, o modo IE no Microsoft Edge será compatível com a não mesclagem. Para um usuário final, quando uma nova janela do navegador é iniciada de um aplicativo de modo IE, ela estará em uma sessão separada, como o comportamento de não mesclagem no IE11.

Para cada Microsoft Edge, na primeira vez que uma guia do modo IE é visitada dentro dessa janela, se for um site designado "sem mesclagem", essa janela será bloqueada em uma sessão diferente do IE "sem mesclagem".  Essa janela permanece bloqueada de todas as Microsoft Edge janelas até que a última guia modo IE seja fechada na janela bloqueada. Isso segue o comportamento anterior em que os usuários podiam iniciar o IE sem mesclagem e iniciar Microsoft Edge sem mesclagem usando outros mecanismos. Todos os sites abertos em uma nova janela (por meio de window.open) respeitarão a natureza de mesclagem do processo pai.

> [!NOTE]
> Não há suporte para alternância de sessão. As navegação na mesma guia modo IE usarão a mesma sessão.

Você pode validar o comportamento de não mesclagem Microsoft Edge versão 93 ou posterior seguindo estas etapas:

1. Verifique se o modo IE está habilitado Microsoft Edge versão 93 ou posterior.
2. Você pode configurar sites que precisam impedir o compartilhamento de sessão na lista de sites do modo Enterprise configurando o valor do atributo de tipo de mesclagem como "no-merge". Esse atributo não é aplicável somente quando o elemento open-in é definido como Microsoft Edge. Por padrão, todos os sites têm um valor do tipo mesclagem de mesclagem. (**Observação:** a ferramenta gerenciador de lista de sites integrada disponível no *edge://compat/sitelistmanager* inclui uma caixa de seleção **** Não mesclar quando você adiciona ou edita um site.)

   ```
   <site url="contoso.com">
   <open-in merge-type="no-merge">IE11</open-in>
   </site>
   ```

3. Navegue até qualquer site configurado como sem mesclagem. O site deve estar em sua própria sessão de IE não mesclada. Quando você abre outra Microsoft Edge ou janela e navega para o mesmo site, ela deve estar em sua própria sessão do IE. Observe que há vários processos iexplore.exe no Gerenciador de Tarefas.

Se você tiver algum comentário, entre em contato por meio de um dos nossos canais de comentários: Suporte da Microsoft ou fórum [techCommunity](https://techcommunity.microsoft.com/t5/enterprise/bd-p/EdgeInsiderEnterprise) .

### <a name="can-i-save-links-as-webpages-in-internet-explorer-mode"></a>Posso salvar links como páginas da Web no modo Internet Explorer?

Sim, você pode habilitar a opção Salvar destino como no menu de contexto do modo Internet Explorer no Microsoft Edge. Para fazer isso, configure a política de grupo "Permitir Salvar Destino como no modo *Internet Explorer*" localizada na Configuração do Computador > Modelos *Administrativos > Windows Componentes > Internet Explorer*. O mecanismo de salvamento funciona da mesma forma que no Internet Explorer e, se o destino for salvo como um arquivo html, reabrir o arquivo renderizará a página no Microsoft Edge.

A capacidade de salvar links como páginas da Web requer as seguintes atualizações mínimas do sistema operacional:

- Windows 10, versão 2004, Windows Server, versão 2004, Windows 10, versão 20H2: [KB4580364](https://support.microsoft.com/help/4580364/windows-10-update-kb4580364)
- Windows 10, versão 1903, Windows 10, versão 1909, Windows Server, versão 1903: [KB4580386](https://support.microsoft.com/help/4580386/windows-10-update-kb4580386)
- Windows 10, versão 1809, Windows Server, versão 1809, Windows Server 2019: [KB4580390](https://support.microsoft.com/help/4580390/windows-10-update-kb4580390)
- Windows 10, versão 1803: [KB4586785](https://support.microsoft.com/help/4586785/windows-10-update-kb4586785)
- Windows 10, versão 1607: [KB4586830](https://support.microsoft.com/help/4586830/windows-10-update-kb4586830)
- Windows 10, versão 1507: [KB4586787](https://support.microsoft.com/help/4586787/windows-10-update-kb4586787)

### <a name="can-i-test-a-site-in-microsoft-edge-while-it-is-configured-to-open-ie-mode-in-the-enterprise-mode-site-list"></a>Posso testar um site no Microsoft Edge enquanto ele está configurado para abrir o modo IE na Lista de Sites Enterprise Modo de Exibição?

Sim, enquanto estiver modernizando seus sites herdados, você pode testar aplicativos configurados no modo IE Microsoft Edge. Para testar esses aplicativos, você pode configurar a [política InternetExplorerModeTabInEdgeModeAllowed](/deployedge/microsoft-edge-policies#internetexplorermodetabinedgemodeallowed) . Se você habilitar essa política, os usuários poderão abrir sites do modo IE no Microsoft Edge selecionando **Configurações** e muito mais (o ícone de reticências...) **** >  > mais**ferramentas abrir sites** no modo de borda.

### <a name="how-can-i-debug-my-legacy-application-while-using-ie-mode-on-microsoft-edge"></a>Como posso depurar meu aplicativo herdado ao usar o modo IE no Microsoft Edge?

Você pode usar o IEChooser para iniciar o Internet Explorer DevTools para depurar o conteúdo das guias do modo IE. Para usar o IEChooser, siga estas etapas:

1. Abra IEChooser.
   - Abra a caixa de diálogo Executar. Por exemplo, pressione o `Windows logo key` + `R`botão .
   - Insira `%systemroot%\system32\f12\IEChooser.exe`e selecione **Ok**.
2. No IEChooser, selecione a entrada para a guia modo IE.

### <a name="my-application-requires-transferring-post-data-between-ie-mode-and-microsoft-edge-is-this-supported"></a>Meu aplicativo requer a transferência de dados POST entre o modo IE e Microsoft Edge. Há suporte para isso?

A partir canal Microsoft Edge Beta versão 96, as navegação que alternam entre o modo Internet Explorer e Microsoft Edge incluirão dados de formulário por padrão. No entanto, se os dados de formulário incluirem anexos de arquivo, eles não serão transferidos entre mecanismos. Você pode escolher quais tipos de dados devem ser incluídos em tais navegaçãos usando a política de grupo [InternetExplorerIntegrationComplexNavDataTypes](/deployedge/microsoft-edge-policies#internetexplorerintegrationcomplexnavdatatypes) .

Além da Microsoft Edge versão 96, você precisa ter as seguintes atualizações Windows instaladas para essa experiência:

- Windows 11 [KB5007262](https://support.microsoft.com/topic/november-22-2021-kb5007262-os-build-22000-348-preview-7f3e18d7-4189-4882-b0e9-afc920253aee) ou posterior
- Windows Server 2022 [KB5007254](
https://support.microsoft.com/topic/november-22-2021-kb5007254-os-build-20348-380-preview-9a960291-d62e-486a-adcc-6babe5ae6fc1) ou posterior
- Windows 10 versão 2004; Windows Server versão 2004; Windows 10 versão; Windows Server versão 20H2 e Windows 10 versão 21H1 – [KB5006738](https://support.microsoft.com/topic/october-26-2021-kb5006738-os-builds-19041-1320-19042-1320-and-19043-1320-preview-ccbce6bf-ae00-4e66-9789-ce8e7ea35541) ou posterior
- Windows 10 versão 1909 [KB5007189](
https://support.microsoft.com/topic/november-9-2021-kb5007189-os-build-18362-1916-91b4647c-9979-4d84-8e64-efc8674e8c1f) ou posterior

### <a name="where-can-i-find-the-reload-in-internet-explorer-mode-option"></a>Onde posso encontrar a opção "Recarregar no modo Internet Explorer"?

Esse recurso está disponível no Microsoft Edge versão 92 ou posterior. Para habilitar essa opção, configure "Permitir que os sites sejam recarregados nas configurações do modo Internet Explorer" Microsoft Edge como "Permitir".  Para obter mais informações, consulte [Habilitar a experiência de lista de sites locais](/deployedge/edge-ie-mode-local-site-list#enable-the-local-site-list-experience).

### <a name="where-is-the-file--new-session-option-in-microsoft-edge"></a>Onde está a opção "> nova sessão" no Microsoft Edge?

Uma solução de navegador moderna está disponível usando vários perfis no Microsoft Edge. Esse recurso permite que você crie uma nova sessão com outra conta. Os recursos a seguir fornecem informações sobre os benefícios de vários perfis e como usá-los.

- [Vídeo: Microsoft Edge e Identidade](/deployedge/microsoft-edge-video-identity)
- [Usar vários perfis no trabalho e em casa agora é mais fácil com Microsoft Edge](https://blogs.windows.com/msedgedev/2020/04/30/automatic-profile-switching/)

### <a name="why-am-i-getting-multiple-authentication-prompts-when-running-a-page-in-ie-mode-on-microsoft-edge"></a>Por que estou recebendo vários prompts de autenticação ao executar uma página no modo IE Microsoft Edge?

O certificado do cliente pode ser solicitado duas vezes no modo IE. Na primeira vez, a caixa de diálogo de seleção de certificado será exibida no modo IE e, na segunda vez, a caixa de diálogo será exibida Microsoft Edge. O processo de quadro e o processo de janela precisam solicitar autenticação.

Depois que o cache favicon for criado, você não será solicitado a fornecer um certificado de cliente novamente, a menos que exclua o cache. Como alternativa, você pode definir uma regra na configuração do servidor, como o IIS, para não exigir um certificado de cliente para o favicon.

### <a name="why-are-there-rendering-issues-like-text-wrapping-and-content-truncation-when-child-windows-are-running-in-ie-mode-in-microsoft-edge"></a>Por que há problemas de renderização, como encapsulamento de texto e truncamento de conteúdo quando as janelas filho estão em execução no modo IE no Microsoft Edge?

A área de conteúdo de uma janela filho que é renderizada no modo IE no Microsoft Edge é ligeiramente diferente do que é no Internet Explorer 11. Se uma página da Web tiver sido projetada com alinhamentos ou posicionamentos baseados em pixel, você poderá experimentar renderização incorreta, disposição de texto e assim por diante.

Duas configurações de política foram adicionadas ao Microsoft Edge versão 95 que permitem especificar ajustes personalizados à altura e à largura das janelas pop-up geradas de sites `window.open` do modo IE por meio do método. Você pode usar as seguintes políticas para ajustar o tamanho da janela:

- [InternetExplorerIntegrationWindowOpenHeightAdjustment](/deployedge/microsoft-edge-policies#internetexplorerintegrationwindowopenheightadjustment) – essa configuração permite que você especifique um ajuste personalizado para a altura das janelas pop-up geradas no site do modo Internet Explorer.
- [InternetExplorerIntegrationWindowOpenWidthAdjustment](/deployedge/microsoft-edge-policies#internetexplorerintegrationwindowopenwidthadjustment) – essa configuração permite especificar um ajuste personalizado para a largura das janelas pop-up geradas do site do modo Internet Explorer.

### <a name="why-arent-pop-ups-or-redirected-websites-loading-in-ie-mode-or-in-internet-explorer-11"></a>Por que pop-ups ou sites redirecionados não são carregados no modo IE ou no Internet Explorer 11?

Depois de configurar o modo IE, determinados sites, especialmente os sites que criam uma nova janela ou um site que é redirecionado, podem não ser renderizados no modo IE ou abertos no Internet Explorer 11.

Para esse tipo de site redirecionado, você pode usar a configuração na `allow-redirect="true"` lista de sites. Para obter mais informações, consulte [Elementos de esquema atualizados](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance#updated-schema-elements).

### <a name="why-arent-websites-loading-in-ie-mode-when-i-launch-microsoft-edge-for-the-first-time"></a>Por que os sites não são carregados no modo IE quando eu Microsoft Edge pela primeira vez?

Microsoft Edge precisa baixar a lista de sites do modo IE antes de aplicar as configurações do modo IE. Esse processo pode não ser concluída quando o navegador é iniciado. Uma política está disponível que pode forçar o carregamento da lista de sites antes que um site seja carregado. Para obter mais informações, confira a política [DelayNavigationsForInitialSiteListDownload](/deployedge/microsoft-edge-policies#delaynavigationsforinitialsitelistdownload).

### <a name="why-cant-i-open-files-or-pages-that-are-found-by-using-file-urls-in-microsoft-edge"></a>Por que não consigo abrir arquivos ou páginas que são encontrados usando file:// URLs no Microsoft Edge?

Devido a uma restrição Chromium segurança, o modo IE precisa ser usado. Você pode usar Microsoft Edge do modo IE para carregar páginas da Web hospedadas no protocolo **file://** dentro de uma zona da intranet. Você pode usar a política de [grupo IntranetFileLinksEnabled](/deployedge/microsoft-edge-policies#intranetfilelinksenabled) para habilitar essa funcionalidade.

## <a name="see-also"></a>Consulte também
  
- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Sobre o modo IE](./edge-ie-mode.md)
- [Informações adicionais sobre o Modo Empresarial](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
