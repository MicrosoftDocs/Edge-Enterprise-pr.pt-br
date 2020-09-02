---
title: ClickOnce e DirectInvoke no Microsoft Edge
ms.author: kele
author: dan-wesley
manager: srugh
ms.date: 04/30/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Saiba mais sobre o ClickOnce e o DirectInvoke no Microsoft Edge.
ms.openlocfilehash: 8290c34bd29ca72678e3fa68f74b689d0cf797e3
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979075"
---
# Noções básicas sobre os recursos ClickOnce e DirectInvoke no Microsoft Edge

ClickOnce e DirectInvoke são recursos disponíveis no IE e no Microsoft Edge (versão 45 e anterior) que oferecem suporte ao uso de um manipulador de arquivos para baixar arquivos de um site. Embora eles atendam a diferentes finalidades, os dois recursos permitem que sites especifiquem que um arquivo solicitado para download seja passado para um manipulador de arquivos no dispositivo do usuário. As solicitações do ClickOnce são manipuladas pelo manipulador de arquivos nativo no Windows. As solicitações do DirectInvoke são manipuladas por um manipulador de arquivos registrado pelo site que hospeda o arquivo.

Para obter mais informações sobre esses recursos, consulte:

- [ClickOnce](https://docs.microsoft.com/visualstudio/deployment/clickonce-security-and-deployment?view=vs-2019)
- [DirectInvoke]( https://technet.microsoft.com/learning/jj215788(v=vs.94).aspx)

> [!NOTE]
> Atualmente, o Chromium não oferece suporte nativo ao ClickOnce nem ao DirectInvoke.

## Visão geral: pré-requisitos e processo

Para que o ClickOnce e o DirectInvoke funcionem conforme planejado e o manipulador de arquivos seja solicitado com êxito, o manipulador de arquivos deve ser registrado no sistema operacional como compatível com ClickOnce ou DirectInvoke. Geralmente, esse registro acontece quando o sistema operacional original é instalado ou quando um novo programa instalado solicita a capacidade de usar o DirectInvoke para atualizações.

Quando um site recebe uma solicitação de download que requer o ClickOnce ou o DirectInvoke, ocorrem as seguintes ações:

- O site solicita que o navegador use um manipulador de arquivos especificado.
- O navegador verifica o Registro do sistema operacional para confirmar se o manipulador de arquivos está registrado para o tipo de arquivo solicitado.
- Se o manipulador de arquivos estiver registrado, o navegador chamará o manipulador de arquivos e passará a URL como um argumento para o manipulador de arquivos.
- O manipulador de arquivos processa a URL e baixa o arquivo.

  > [!NOTE]
  > A URL é usada para determinar a origem do arquivo, bem como todos os parâmetros a serem usados ao acessar o arquivo.  Por exemplo: pontos de extremidade, manifesto ou metadados.

## Casos de uso

Os seguintes casos de uso são representativos.

Você pode usar o ClickOnce para implantar e atualizar facilmente software em dispositivos com mínima interação do usuário. Os usuários podem instalar e executar um aplicativo do Windows clicando em um link em uma página da Web. Se configurado corretamente, o aplicativo ClickOnce pode instalar programas sem que os usuários definam configurações para o instalador. Por exemplo, locais dos arquivos, quais opções instalar etc.

Os casos de uso do DirectInvoke dependem da intenção do site que está solicitando o DirectInvoke. Por exemplo, o recurso de edição colaborativa de arquivos do Microsoft Word. Em vez de clicar em um link e baixar a cópia inteira de um documento em que você está trabalhando com seus colegas, o DirectInvoke permite baixar as partes do documento que foram alteradas. Isso reduz a quantidade de dados transferidos, podendo reduzir o tempo necessário para abrir o documento.  

## Suporte atual ao ClickOnce e ao DirectInvoke no Microsoft Edge

Suporte ao ClickOnce e ao DirectInvoke:

- Para os usuários do Windows, o DirectInvoke tem suporte imediato, mas o ClickOnce está desabilitado.

  > [!NOTE]
  > Os usuários que precisam do suporte ao ClickOnce podem acessar edge://flags/#edge-click-once e selecionar **Ativar** na lista suspensa. Você precisará **Reiniciar** o navegador.

- O ClickOnce e o DirectInvoke não têm suporte em outras plataformas que não seja o Windows.
- Como o ClickOnce é um recurso empresarial usado por um grupo específico de usuários avançados e não se destina ao uso geral, ele é desabilitado por padrão.

## Segurança de manipulação de arquivos do ClickOnce e do DirectInvoke

O ClickOnce e o DirectInvoke são protegidos pelo serviço de verificação de reputação de URL do Microsoft Defender SmartScreen.

Se uma solicitação do ClickOnce ou do DirectInvoke for sinalizada pelo serviço de reputação de URL do Microsoft Defender SmartScreen como não seguro, os usuários com o ClickOnce ou o DirectInvoke habilitado verão dois pop-ups.

O primeiro pop-up pergunta ao usuário se ele quer abrir o arquivo. Esse pop-up é exibido independentemente de o arquivo ter sido sinalizado como seguro ou não seguro. O usuário pode **Relatar o arquivo como não seguro**, **Cancelar** a solicitação ou clicar em **Abrir** para continuar.

   ![Aviso para abrir um arquivo](./media/edge-learn-more-co-di/edge-clickonce-modal-1.png)

Se o usuário tentar abrir um arquivo que foi sinalizado como não seguro, um segundo pop-up será exibido.  Esse pop-up avisa o usuário de que o arquivo foi sinalizado como não seguro e pergunta se ele tem certeza de que quer baixar o arquivo.

O segundo pop-up só aparece se:

- o arquivo for um arquivo do ClickOnce ou do DirectInvoke
- o ClickOnce ou o DirectInvoke estiverem habilitados
- o arquivo estiver sinalizado como não seguro

 ![Aviso para abrir um arquivo não seguro](./media/edge-learn-more-co-di/edge-clickonce-modal-2.png)

> [!NOTE]
> Se o ClickOnce ou o DirectInvoke estiverem desabilitados, os arquivos solicitados serão tratados como downloads regulares e, se sinalizados como não seguros, serão marcados como não seguros. Isso é consistente com o tratamento de outros downloads não seguros.

## Políticas do ClickOnce e do DirectInvoke

Há duas políticas de grupo que você pode usar para habilitar ou desabilitar o ClickOnce e o DirectInvoke para usuários corporativos. Essas duas políticas são [ClickOnceEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#clickonceenabled) e [DirectInvokeEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#directinvokeenabled). Essas duas políticas são rotuladas no Editor de Política de Grupo como "Permitir que os usuários abram arquivos usando o protocolo ClickOnce" e "Permitir que os usuários abram arquivos usando o protocolo DirectInvoke", respectivamente.

## Comportamento do ClickOnce e do DirectInvoke

Os exemplos a seguir mostram a manipulação de arquivos quando o ClickOnce e o DirectInvoke estão habilitados ou desabilitados.

### ClickOnce habilitado

1. Um usuário abre um link para uma página que solicita suporte ao ClickOnce e recebe o aviso exibido na próxima captura de tela.

   ![Aviso para abrir um arquivo não seguro](./media/edge-learn-more-co-di/edge-clickonce-enabled-1.png)

2. Depois que o usuário clica em **Abrir**, o ClickOnce tenta iniciar o aplicativo.

   ![O ClickOnce tenta iniciar o aplicativo](./media/edge-learn-more-co-di/edge-clickonce-enabled-launch-app.png)

3. Depois que o usuário clica em **Abrir**, o navegador mostra um pop-up que pergunta se o usuário tem certeza de que quer instalar o aplicativo.

   ![Aviso para abrir o arquivo](./media/edge-learn-more-co-di/edge-clickonce-enabled-2.png)

   > [!NOTE]
   > A interface, as mensagens e as opções mostradas pelo manipulador de arquivos do ClickOnce variam de acordo com o tipo e a configuração do arquivo acessado.

### ClickOnce desabilitado

1. Quando um usuário abre um link para uma página que solicita suporte ao ClickOnce, ele verá uma mensagem na bandeja de download semelhante à da próxima captura de tela.

   ![Aviso de download de arquivo](./media/edge-learn-more-co-di/edge-clickonce-disabled-1.png)

### DirectInvoke habilitado

1. Um usuário abre um link para uma página que solicita suporte ao DirectInvoke e recebe o aviso exibido na próxima captura de tela.

   ![Aviso para abrir um arquivo](./media/edge-learn-more-co-di/edge-directinvoke-open-link-1.png)

2. Quando o usuário clica em **Abrir**, o manipulador de arquivos solicitado é aberto. Neste exemplo, o Microsoft Word é usado para abrir o documento exibido na captura de tela anterior.

   > [!NOTE]
   > A interface, as mensagens e as opções mostradas pelo manipulador de arquivos do DirectInvoke variam de acordo com o tipo e a configuração do arquivo acessado.

### DirectInvoke desabilitado

1. Quando um usuário abre um link para uma página que solicita suporte ao DirectInvoke, o DirectInvoke se comporta igual quando o ClickOnce está desabilitado. Ele verá uma mensagem na bandeja de download semelhante à da próxima captura de tela.

   ![Aviso para abrir um arquivo](./media/edge-learn-more-co-di/edge-directinvoke-open-link-2.png)

## Ver também

- [Segurança e implantação do ClickOnce](https://go.microsoft.com/fwlink/?linkid=2099880)
- [DirectInvoke no Internet Explorer](https://go.microsoft.com/fwlink/?linkid=2099871)
- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
