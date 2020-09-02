---
title: Configurar políticas do modo IE
ms.author: cjacks
author: cjacks
manager: saudm
ms.date: 03/25/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Configurar políticas do modo IE
ms.openlocfilehash: 2d2ded3a3fb338bdf2d815d681b52249007945ac
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979020"
---
# Configurar políticas do modo IE

Este artigo explica como configurar as políticas do modo IE.

> [!NOTE]
> Este artigo se aplica aos Canais **Estável**, **Beta** e **Dev** do Microsoft Edge Beta, versão 77 ou posteriores.

A configuração do modo IE tem três etapas:

1. [Configurar a integração do Internet Explorer](#configure-internet-explorer-integration)
2. [Redirecionar sites do Microsoft Edge para o modo do IE](#redirect-sites-from-microsoft-edge-to-ie-mode)
3. (Opcional) [Redirecione sites do IE para Microsoft Edge](#redirect-sites-from-ie-to-microsoft-edge)

> [!NOTE]
> As políticas para habilitar o modo do IE podem ser configuradas por meio do Intune. Para obter mais informações, confira [Adicionar o Microsoft Edge ao Microsoft Intune](https://docs.microsoft.com/intune/apps/apps-windows-edge?toc=https://docs.microsoft.com/DeployEdge/toc.json&bc=https://docs.microsoft.com/DeployEdge/breadcrumb/toc.json) e [Configurar as políticas do Microsoft Edge com o Microsoft Intune](https://docs.microsoft.com/DeployEdge/configure-edge-with-intune).

## Configurar a integração do Internet Explorer

Você pode configurar o Internet Explorer para abrir diretamente no Microsoft Edge (modo IE). Você também pode configurar o Internet Explorer para abrir com uma janela independente do Internet Explorer 11. A maioria dos usuários prefere quando os sites são abertos diretamente dentro do Microsoft Edge no modo IE.

### Habilitar a integração do Internet Explorer usando a Política de Grupo

1. Baixar e usar o [Modelo de Política do Microsoft Edge](https://www.microsoft.com/en-us/edge/business/download) mais recente.
2. Abra o Editor de Políticas de Grupo.
3. Clique em **Configuração do Computador** > **Modelos Administrativos** > **Microsoft Edge**.
4. Clique duas vezes em **Configurar integração do Internet Explorer**.
5. Selecione **Habilitado**.
6. Em **Opções**, defina o valor da lista suspensa como 
   -  **Modo Internet Explorer** se você deseja que os sites sejam abertos no modo IE no Microsoft Edge
   -  ** Internet Explorer 11** se desejar que os sites sejam abertos em uma janela independente do Internet Explorer 11
   -  **Nenhum** se você quiser impedir que os usuários configurem o modo Internet Explorer via edge://sinalizadores ou pela linha de comando

   > [!NOTE]
   > Definir a política para **Desabilitada** significa que o modo de IE está desabilitado por política, mas pode ser definido por meio de edge://flags ou opções de linha de comando.
7. Clique em **OK** ou em **Aplicar** para salvar essa configuração de política.

## Redirecionar sites do Microsoft Edge para o modo do IE

Existem duas opções para identificar quais sites devem abrir no modo IE:

- (Recomendado) [Configurar sites na lista de sites da empresa](#configure-sites-on-the-enterprise-site-list)
- [Configurar todos os sites de Intranet](#configure-all-intranet-sites)

### Configurar sites na lista de sites da empresa

Você pode usar as seguintes políticas de grupo para configurar sites específicos para serem abertos no modo IE:

- [Usar a lista de sites do IE no Modo Empresarial](#configure-using-the-use-the-enterprise-mode-ie-website-list-policy) (Internet Explorer)
- [Configurar a lista de sites do Modo Empresarial](#configure-using-the-configure-the-enterprise-mode-site-list-policy) (Microsoft Edge, versão 78 ou posterior)<br/>Esta política permite criar uma lista de Sites do Modo Empresarial separada para o Microsoft Edge. A habilitação desta política substitui as configurações da política "Usar a lista de sites do Modo Empresarial IE", se "Configurar integração do Internet Explorer" estiver habilitado. Desabilitar ou não configurar essa política não afeta o comportamento padrão da política "Configurar integração do Internet Explorer".
    > [!NOTE]
    > Não é obrigatório configurar a política do Microsoft Edge. Muitas organizações usam isso como uma substituição, permitindo-as direcionar a Lista de Sites atual para todos os usuários com a política do IE e direcionar mais facilmente uma versão atualizada para usos piloto com a política do Microsoft Edge.

Para obter mais informações sobre as listas de sites do Modo Empresarial, consulte:

- [Usar o Enterprise Mode Site List Manager](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/use-the-enterprise-mode-site-list-manager)
- [Adicionar vários sites à lista de sites do Modo Empresarial usando um arquivo e o Enterprise Mode Site List Manager (esquema v.2)](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/add-multiple-sites-to-enterprise-mode-site-list-using-the-version-2-schema-and-enterprise-mode-tool).

### Configurar usando a política de lista de sites Usar o Modo Empresarial IE

O modo IE pode usar a política existente que configura a Lista de Sites Empresariais para o Internet Explorer, permitindo criar e manter uma única lista.

1. Criar ou reutilizar um XML de lista de sites
    1. Todos os sites que têm o elemento _\<open-in\>IE11\</open-in\>_ serão abertos no modo IE.
2. Abra o Editor de Políticas de Grupo.
3. Clique em **Configuração do Computador** > **Modelos Administrativos** > **Windows Components** > **Internet Explorer**.
4. Clique duas vezes em **Usar a lista de sites do IE do Modo Empresarial**.
5. Selecione **Habilitado**.
6. Em **Opções**, digite o local da lista de sites. Você pode usar um dos seguintes locais:
    - (Recomendado) Local HTTPS: **https**:**//iemode/sites.xml**
    - Arquivo da rede local: **\\\network\shares\sites.xml**
    - Arquivo local: **file:///c:/Users/\<user\>/Documents/sites.xml**
7. Clique em **OK** ou **Aplicar** para salvar essas configurações.

### Configurar usando a política Configurar a Lista de Sites do Modo Empresarial

Você também pode configurar o modo IE com uma política separada para o Microsoft Edge. Essa política adicional permite substituir a lista de sites do IE. Por exemplo, algumas organizações direcionam a lista de sites de produção para todos os usuários. Você pode implantar a lista de sites piloto em um pequeno grupo de usuários usando essa política.

1. Criar ou reutilizar um XML de lista de sites
    1. Todos os sites que têm o elemento _\<open-in\>IE11\</open-in\>_ serão abertos no modo IE.
2. Abra o Editor de Políticas de Grupo.
3. Clique em **Configuração do Computador** > **Modelos Administrativos** > **Microsoft Edge**.
4. Clique duas vezes em **Configurar a Lista de Sites do Modo Empresarial**.
5. Selecione **Habilitado**.
6. Em **Opções**, digite o local da lista de sites. Você pode usar um dos seguintes locais:
    - (Recomendado) Local HTTPS: **https**:**//iemode/sites.xml** <!--Trying to keep this from being an active link in MD -->
    - Arquivo da rede local: **\\\network\shares\sites.xml**
    - Arquivo local: **file:///c:/Users/\<user\>/Documents/sites.xml**
7. Clique em **OK** ou **Aplicar** para salvar essas configurações.

### Configurar todos os sites de intranet

O modo IE pode ser configurado como para todos os sites na zona da Intranet Local. Você pode remover sites individuais do modo IE usando uma Lista de Sites do Modo Empresarial.

>[!NOTE]
>
> A zona da Intranet Local contém sites adicionados explicitamente, mas também atribui sites a essa zona usando heurística. Isso pode incluir nomes de host sem ponto (por exemplo, **https**:**//folhadepagamento**) e sites que o script de configuração do proxy configura para contornar o proxy. Se uma parte externa controlar o DNS ou o proxy, ela poderá forçar que os sites usem o modo IE.

1. Abra o Editor de política de grupo local.
2. Clique em **Configuração do Computador** > **Modelos Administrativos** > **Microsoft Edge**.
3. Clique duas vezes em **Enviar todos os sites da intranet para o Internet Explorer**.
4. Selecione **Habilitado** e clique em **OK** ou em **Aplicar** para salvar as configurações de política.

## Redirecionar sites do IE para o Microsoft Edge

Você pode impedir que os usuários usem o Internet Explorer para sites que não precisam dele. O Internet Explorer pode redirecionar sites para o Microsoft Edge automaticamente se eles não estiverem na sua lista de sites.

1. Abra o Editor de Políticas de Grupo.
2. Clique em **Configuração do Computador** > **Ferramentas Administrativas** > **Componentes do Windows** > **Internet Explorer**.
3. Clique duas vezes em **Enviar todos os sites não incluídos na Lista de Sites do Modo Empresarial para o Microsoft Edge.**
4. Selecione **Habilitado**
5. Clique em **OK** ou **Aplicar** para salvar essas configurações.
6. Clique duas vezes em **Configurar qual canal do Microsoft Edge usar para abrir sites redirecionados**.
7. Selecione **Habilitado**.
8. Em **Opções**, selecione as três principais opções para o canal - o Internet Explorer será redirecionado para a opção mais bem classificada que o usuário instalou no dispositivo:
   - Microsoft Edge Stable
   - Microsoft Edge Beta versão 77 ou posterior
   - Microsoft Edge Dev versão 77 ou posterior
   - Microsoft Edge Canary versão 77 ou posterior
   - Microsoft Edge versão 45 ou anterior
9. Clique em **OK** ou **Aplicar** para salvar essas configurações.

## Consulte também

- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Sobre o modo IE](https://docs.microsoft.com/deployedge/edge-ie-mode)
- [Informações adicionais sobre o Modo Empresarial](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)