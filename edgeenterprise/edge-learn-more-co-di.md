---
title: ClickOnce e DirectInvoke no Microsoft Edge
ms.author: collw
author: AndreaLBarr
manager: srugh
ms.date: 05/25/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Saiba mais sobre os recursos clickOnce e DirectInvoke no Microsoft Edge.
ms.openlocfilehash: ef0ec841541972ec563079fee0f1ae802951ea4b
ms.sourcegitcommit: 3e3362b0c5c663df160e8e8f68a4c82564183b2d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/31/2022
ms.locfileid: "12740771"
---
# <a name="understand-the-clickonce-and-directinvoke-features-in-microsoft-edge"></a>Noções básicas sobre os recursos ClickOnce e DirectInvoke no Microsoft Edge

ClickOnce e DirectInvoke são recursos disponíveis no IE e no Microsoft Edge que dão suporte ao uso de um manipulador de arquivos para baixar arquivos de um site. Embora eles atendam a diferentes finalidades, os dois recursos permitem que sites especifiquem que um arquivo solicitado para download seja passado para um manipulador de arquivos no dispositivo do usuário. As solicitações do ClickOnce são manipuladas pelo manipulador de arquivos nativo no Windows. As solicitações do DirectInvoke são manipuladas por um manipulador de arquivos registrado pelo site que hospeda o arquivo.

Depois de configurar o ClickOnce ou o DirectInvoke, os prompts do ClickOnce ou do DirectInvoke podem ser ignorados configurando outras políticas corporativas. Essas políticas podem dar suporte a ignorar os prompts clickOnce ou DirectInvoke para tipos de arquivo especificados para todos os domínios ou para tipos de arquivo especificados de domínios especificados.

Para obter mais informações sobre esses recursos, consulte:

- [ClickOnce](/visualstudio/deployment/clickonce-security-and-deployment?view=vs-2019)
- [DirectInvoke](https://technet.microsoft.com/learning/jj215788(v=vs.94).aspx)

> [!NOTE]
> Atualmente, o Chromium não oferece suporte nativo ao ClickOnce nem ao DirectInvoke.

## <a name="overview-prerequisites-and-process"></a>Visão geral: pré-requisitos e processo

Para que o ClickOnce e o DirectInvoke funcionem conforme planejado e o manipulador de arquivos seja solicitado com êxito, o manipulador de arquivos deve ser registrado no sistema operacional como compatível com ClickOnce ou DirectInvoke. Geralmente, esse registro acontece quando o sistema operacional original é instalado ou quando um novo programa instalado solicita a capacidade de usar o DirectInvoke para atualizações.

Quando um site recebe uma solicitação de download que requer o ClickOnce ou o DirectInvoke, ocorrem as seguintes ações:

- O site solicita que o navegador use um manipulador de arquivos especificado.
- O navegador verifica o Registro do sistema operacional para confirmar se o manipulador de arquivos está registrado para o tipo de arquivo solicitado.
- Se o manipulador de arquivos estiver registrado, o navegador chamará o manipulador de arquivos e passará a URL como um argumento para o manipulador de arquivos.
- O manipulador de arquivos processa a URL e baixa o arquivo.

  > [!NOTE]
  > A URL é usada para determinar a origem do arquivo, bem como todos os parâmetros a serem usados ao acessar o arquivo.  Por exemplo: pontos de extremidade, manifesto ou metadados.

## <a name="use-cases"></a>Casos de uso

Os seguintes casos de uso são representativos.

Você pode usar o ClickOnce para implantar e atualizar facilmente software em dispositivos com mínima interação do usuário. Os usuários podem instalar e executar um aplicativo do Windows clicando em um link em uma página da Web. Se configurado corretamente, o aplicativo ClickOnce pode instalar programas sem que os usuários definam configurações para o instalador. Por exemplo, locais dos arquivos, quais opções instalar etc.

Os casos de uso do DirectInvoke dependem da intenção do site que está solicitando o DirectInvoke. Por exemplo, o recurso de edição colaborativa de arquivos do Microsoft Word. Em vez de clicar em um link e baixar a cópia inteira de um documento em que você está trabalhando com seus colegas, o DirectInvoke permite baixar as partes do documento que foram alteradas. Isso reduz a quantidade de dados transferidos, podendo reduzir o tempo necessário para abrir o documento.  

## <a name="current-support-for-clickonce-and-directinvoke-in-microsoft-edge"></a>Suporte atual ao ClickOnce e ao DirectInvoke no Microsoft Edge

Suporte ao ClickOnce e ao DirectInvoke:

- O ClickOnce e o DirectInvoke têm suporte prontos para todos os usuários do Windows.

  > [!NOTE]
  > Os usuários que precisam desabilitar o suporte ao ClickOnce podem acessar *edge://flags/#edge-click-once* e selecionar **Desabilitador** na lista suspensa. Você precisará **Reiniciar** o navegador.

- O ClickOnce e o DirectInvoke não têm suporte em outras plataformas que não seja o Windows.

## <a name="clickonce-and-directinvoke-file-handling-security"></a>Segurança de manipulação de arquivos do ClickOnce e do DirectInvoke

O ClickOnce e o DirectInvoke são protegidos Microsoft 365 Defender verificação de reputação de URL do SmartScreen.

Se uma solicitação ClickOnce ou DirectInvoke for sinalizada pelo serviço de reputação de URL do Microsoft 365 Defender SmartScreen como não segura, os usuários com o ClickOnce ou DirectInvoke habilitado verão dois pop-ups.

O primeiro pop-up pergunta ao usuário se ele quer abrir o arquivo. Esse pop-up é exibido independentemente de o arquivo ter sido sinalizado como seguro ou não seguro. O usuário pode **relatar o arquivo como não seguro****, cancelar** a solicitação ou selecionar **Abrir** para continuar.

   ![Aviso para abrir um arquivo](./media/edge-learn-more-co-di/edge-clickonce-modal-1.png)

Se o usuário tentar abrir um arquivo que foi sinalizado como não seguro, um segundo pop-up será exibido.  Esse pop-up avisa o usuário de que o arquivo foi sinalizado como não seguro e pergunta se ele tem certeza de que quer baixar o arquivo.

O segundo pop-up só aparece se:

- o arquivo for um arquivo do ClickOnce ou do DirectInvoke
- o ClickOnce ou o DirectInvoke estiverem habilitados
- o arquivo estiver sinalizado como não seguro

 ![Aviso para abrir um arquivo não seguro](./media/edge-learn-more-co-di/edge-clickonce-modal-2.png)

> [!NOTE]
> Se o ClickOnce ou o DirectInvoke estiverem desabilitados, os arquivos solicitados serão tratados como downloads regulares e, se sinalizados como não seguros, serão marcados como não seguros. Isso é consistente com o tratamento de outros downloads não seguros.

## <a name="clickonce-and-directinvoke-policies"></a>Políticas do ClickOnce e do DirectInvoke

Há duas políticas de grupo que você pode usar para habilitar ou desabilitar o ClickOnce e o DirectInvoke para usuários corporativos. Essas duas políticas são [ClickOnceEnabled](./microsoft-edge-policies.md#clickonceenabled) e [DirectInvokeEnabled](./microsoft-edge-policies.md#directinvokeenabled). Essas duas políticas são rotuladas no Editor de Política de Grupo como "Permitir que os usuários abram arquivos usando o protocolo ClickOnce" e "Permitir que os usuários abram arquivos usando o protocolo DirectInvoke", respectivamente.

Para especificar tipos de arquivo para os quais os prompts clickOnce ou DirectInvoke devem ser ignorados, use a política rotulada no Editor do Política de Grupo como "Lista de tipos de arquivo que devem ser abertos automaticamente no download". Essa configuração de política permitirá que os tipos de arquivo especificados sejam abertos automaticamente após o download para todos os domínios.  

Você pode ignorar os prompts do ClickOnce ou do DirectInvoke para tipos de arquivo específicos para domínios específicos configurando mais duas políticas. Essas políticas são rotuladas no Editor do Política de Grupo como "Lista de tipos de arquivo que devem ser abertos automaticamente no download" e "URLs em que AutoOpen-FileTypes pode aplicar".

> [!NOTE]
> A política "URLs em que AutoOpen- FileTypes pode se aplicar" é uma política de suporte para "Lista de tipos de arquivo que devem ser abertos automaticamente no download" e não faz nada por conta própria.  

## <a name="clickonce-and-directinvoke-behavior"></a>Comportamento do ClickOnce e do DirectInvoke

Os exemplos a seguir mostram a manipulação de arquivos quando o ClickOnce e o DirectInvoke estão habilitados ou desabilitados.

### <a name="clickonce-enabled"></a>ClickOnce habilitado

1. Um usuário abre um link para uma página que solicita suporte ao ClickOnce e recebe o aviso exibido na próxima captura de tela.

   ![Solicitar a abertura de um arquivo não seguro com o ClickOnce habilitado](./media/edge-learn-more-co-di/edge-clickonce-enabled-1.png)

2. Depois que o usuário seleciona **Abrir**, o ClickOnce tenta iniciar o aplicativo.

   ![O ClickOnce tenta iniciar o aplicativo](./media/edge-learn-more-co-di/edge-clickonce-enabled-launch-app.png)

3. Depois que o usuário seleciona **Abrir**, o navegador mostra um pop-up que pergunta ao usuário se ele tem certeza de que deseja instalar o aplicativo.

   ![Aviso para abrir o arquivo](./media/edge-learn-more-co-di/edge-clickonce-enabled-2.png)

   > [!NOTE]
   > A interface, as mensagens e as opções mostradas pelo manipulador de arquivos do ClickOnce variam de acordo com o tipo e a configuração do arquivo acessado.

### <a name="clickonce-disabled"></a>ClickOnce desabilitado

1. Quando um usuário abrir um link para uma página que solicita suporte ao ClickOnce, ele verá uma mensagem na bandeja de download semelhante à da próxima captura de tela.

   ![Aviso de download de arquivo](./media/edge-learn-more-co-di/edge-clickonce-disabled-1.png)

### <a name="directinvoke-enabled"></a>DirectInvoke habilitado

1. Um usuário abre um link para uma página que solicita suporte ao DirectInvoke e recebe o aviso exibido na próxima captura de tela.

   ![Solicitar a abertura do arquivo da página solicitando suporte](./media/edge-learn-more-co-di/edge-directinvoke-open-link-1.png)

2. Quando o usuário **seleciona Abrir,** o manipulador de arquivos solicitado é aberto. Neste exemplo, o Microsoft Word é usado para abrir o documento exibido na captura de tela anterior.

   > [!NOTE]
   > A interface, as mensagens e as opções mostradas pelo manipulador de arquivos do DirectInvoke variam de acordo com o tipo e a configuração do arquivo acessado.

### <a name="directinvoke-disabled"></a>DirectInvoke desabilitado

1. Quando um usuário abre um link para uma página que solicita suporte ao DirectInvoke, o DirectInvoke se comporta igual quando o ClickOnce está desabilitado. Eles verão uma mensagem na bandeja de download semelhante à da próxima captura de tela.

   ![Solicitar a abertura do arquivo quando o DirectInvoke estiver desabilitado](./media/edge-learn-more-co-di/edge-directinvoke-open-link-2.png)

## <a name="see-also"></a>Ver também

- [Segurança e implantação do ClickOnce](/visualstudio/deployment/clickonce-security-and-deployment)
- [DirectInvoke no Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/dev-guides/jj215788(v=vs.85))
- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
