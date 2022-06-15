---
title: Configurar políticas do modo IE
ms.author: collw
author: AndreaLBarr
manager: srugh
ms.date: 06/15/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Configurar políticas do modo IE
ms.openlocfilehash: 6e0d3501d9510c8e8530908bdbef6f3162b1806a
ms.sourcegitcommit: 01011d970e85683f74f889651f5f402da642f34a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/15/2022
ms.locfileid: "12595229"
---
# <a name="configure-ie-mode-policies"></a>Configurar políticas do modo IE

>[!Note]
> O aplicativo da área de trabalho do Internet Explorer 11 foi desativado e está sem suporte a partir de 15 de junho de [2022](https://aka.ms/IEJune15Blog) para determinadas versões do Windows 10.  
>
> - Você ainda pode acessar sites antigos e herdados que exigem o Internet Explorer com o modo Internet Explorer Microsoft Edge. [Saiba como >](https://aka.ms/IEmodewebsite)
> - O aplicativo da área de trabalho do Internet Explorer 11 será redirecionado progressivamente para o navegador mais rápido e seguro Microsoft Edge e, por fim, será desabilitado por meio Windows Update. [Desabilitar o IE hoje>](/deployedge/edge-ie-disable-ie11)  

Este artigo explica como configurar as políticas do modo IE.

> [!NOTE]
> Este artigo se aplica aos Canais **Estável**, **Beta** e **Dev** do Microsoft Edge Beta, versão 77 ou posteriores.

A configuração do modo IE tem três etapas:

1. [Configurar a integração do Internet Explorer](#configure-internet-explorer-integration)
2. [Redirecionar sites do Microsoft Edge para o modo do IE](#redirect-sites-from-microsoft-edge-to-ie-mode)
3. (Opcional) [Redirecione sites do IE para Microsoft Edge](#redirect-sites-from-ie-to-microsoft-edge)

    1. Se você estiver pronto para desabilitar o aplicativo IE11, siga as etapas em [Desabilitar o Internet Explorer 11](/deployedge/edge-ie-disable-ie11)
    2. Caso contrário, siga o restante das etapas em [Redirecionar sites do IE para o Microsoft Edge](/deployedge/edge-ie-mode-policies#redirect-sites-from-ie-to-microsoft-edge)

> [!NOTE]
> As políticas para habilitar o modo do IE podem ser configuradas por meio do Intune. Para obter mais informações, confira [Adicionar o Microsoft Edge ao Microsoft Intune](/intune/apps/apps-windows-edge?bc=%2fDeployEdge%2fbreadcrumb%2ftoc.json&toc=%2fDeployEdge%2ftoc.json) e [Configurar as políticas do Microsoft Edge com o Microsoft Intune](./configure-edge-with-intune.md).

## <a name="configure-internet-explorer-integration"></a>Configurar a integração do Internet Explorer

Você pode configurar o Internet Explorer para abrir diretamente no Microsoft Edge (modo IE). Você também pode configurar o Internet Explorer para abrir com uma janela independente do Internet Explorer 11. A maioria dos usuários prefere quando os sites são abertos diretamente dentro do Microsoft Edge no modo IE.

### <a name="enable-internet-explorer-integration-using-group-policy"></a>Habilitar a integração do Internet Explorer usando a Política de Grupo

1. Baixar e usar o [Modelo de Política do Microsoft Edge](https://www.microsoft.com/en-us/edge/business/download) mais recente.
2. Abra o Editor de Políticas de Grupo.
3. Clique em **Configuração do Usuário/Configuração do Computador** > **Modelos Administrativos** > **Microsoft Edge**.
4. Clique duas vezes em **Configurar integração do Internet Explorer**.
5. Selecione **Habilitado**.
6. Em **Opções**, defina o valor da lista suspensa como
   -  **Modo Internet Explorer** se você deseja que os sites sejam abertos no modo IE no Microsoft Edge
   -  **Internet Explorer 11** se você quiser que os sites sejam abertos em uma janela autônoma do Internet Explorer 11 (essa opção não terá suporte após 15 de junho de 2022 quando o aplicativo de área de trabalho do Internet Explorer 11 for desativado e ficar sem suporte.  Após 15 de junho de 2022, quando o IE11 não estiver mais disponível, essa opção se comportará da mesma forma que a opção de modo **Internet Explorer** .)  
   -  **Nenhum** se você quiser impedir que os usuários configurem o modo Internet Explorer via edge://sinalizadores ou pela linha de comando

   > [!NOTE]
   > Definir a política para **Desabilitada** significa que o modo de IE está desabilitado por política, mas pode ser definido por meio de edge://flags ou opções de linha de comando.
7. Clique em **OK** ou em **Aplicar** para salvar essa configuração de política.

## <a name="redirect-sites-from-microsoft-edge-to-ie-mode"></a>Redirecionar sites do Microsoft Edge para o modo do IE

Existem duas opções para identificar quais sites devem abrir no modo IE:

- (Recomendado) [Configurar sites na lista de sites da empresa](#configure-sites-on-the-enterprise-site-list)
- [Configurar todos os sites de Intranet](#configure-all-intranet-sites)

### <a name="configure-sites-on-the-enterprise-site-list"></a>Configurar sites na lista de sites da empresa

Você pode usar as seguintes políticas de grupo para configurar sites específicos para serem abertos no modo IE:

- [Usar a lista de sites do IE no Modo Empresarial](#configure-using-the-use-the-enterprise-mode-ie-website-list-policy) (Internet Explorer)
- [Configurar a lista de sites do Modo Empresarial](#configure-using-the-configure-the-enterprise-mode-site-list-policy) (Microsoft Edge, versão 78 ou posterior)<br/>Esta política permite criar uma lista de Sites do Modo Empresarial separada para o Microsoft Edge. A habilitação desta política substitui as configurações da política "Usar a lista de sites do Modo Empresarial IE", se "Configurar integração do Internet Explorer" estiver habilitado. Desabilitar ou não configurar essa política não afeta o comportamento padrão da política "Configurar integração do Internet Explorer".
    > [!NOTE]
    > Não é obrigatório configurar a política do Microsoft Edge. Muitas organizações usam isso como uma substituição, permitindo-as direcionar a Lista de Sites atual para todos os usuários com a política do IE e direcionar mais facilmente uma versão atualizada para usos piloto com a política do Microsoft Edge.

Para obter mais informações sobre Enterprise de sites do modo de exibição, consulte [Usar o Enterprise Site List Manager](/deployedge/edge-ie-mode-site-list-manager).


### <a name="configure-using-the-use-the-enterprise-mode-ie-website-list-policy"></a>Configurar usando a política de lista de sites Usar o Modo Empresarial IE

O modo IE pode usar a política existente que configura a Lista de Sites Empresariais para o Internet Explorer, permitindo criar e manter uma única lista.

1. Criar ou reutilizar um XML de lista de sites
    1. Todos os sites que têm o elemento _\<open-in\>IE11\</open-in\>_ serão abertos no modo IE.
2. Abra o Editor de Políticas de Grupo.
3. Clique em **Configuração do Usuário/Configuração do Computador** > **Modelos Administrativos** > **Componentes do Windows** > **Internet Explorer**.
4. Clique duas vezes em **Usar a lista de sites do IE do Modo Empresarial**.
5. Selecione **Habilitado**.
6. Em **Opções**, digite o local da lista de sites. Você pode usar um dos seguintes locais:
    - (Recomendado) Local HTTPS: **https**:**//iemode/sites.xml**
    - Arquivo da rede local: **\\\network\shares\sites.xml**
    - Arquivo local: **file:///c:/Users/\<user\>/Documents/sites.xml**
7. Clique em **OK** ou **Aplicar** para salvar essas configurações.

### <a name="configure-using-the-configure-the-enterprise-mode-site-list-policy"></a>Configurar usando a política Configurar a Lista de Sites do Modo Empresarial

Você também pode configurar o modo IE com uma política separada para o Microsoft Edge. Essa política adicional permite substituir a lista de sites do IE. Por exemplo, algumas organizações direcionam a lista de sites de produção para todos os usuários. Você pode implantar a lista de sites piloto em um pequeno grupo de usuários usando essa política.

1. Criar ou reutilizar um XML de lista de sites
    1. Todos os sites que têm o elemento _\<open-in\>IE11\</open-in\>_ serão abertos no modo IE.
2. Abra o Editor de Políticas de Grupo.
3. Clique em **Configuração do Usuário/Configuração do Computador** > **Modelos Administrativos** > **Microsoft Edge**.
4. Clique duas vezes em **Configurar a Lista de Sites do Modo Empresarial**.
5. Selecione **Habilitado**.
6. Em **Opções**, digite o local da lista de sites. Você pode usar um dos seguintes locais:
    - (Recomendado) Local HTTPS: **https**:**//iemode/sites.xml** <!--Trying to keep this from being an active link in MD -->
    - Arquivo da rede local: **\\\network\shares\sites.xml**
    - Arquivo local: **file:///c:/Users/\<user\>/Documents/sites.xml**
7. Clique em **OK** ou **Aplicar** para salvar essas configurações.

### <a name="configure-all-intranet-sites"></a>Configurar todos os sites de intranet

O modo IE pode ser configurado como para todos os sites na zona da Intranet Local. Você pode remover sites individuais do modo IE usando uma Lista de Sites do Modo Empresarial.

>[!NOTE]
>
> A zona da Intranet Local contém sites adicionados explicitamente, mas também atribui sites a essa zona usando heurística. Isso pode incluir nomes de host sem ponto (por exemplo, **https**:**//folhadepagamento**) e sites que o script de configuração do proxy configura para contornar o proxy. Se uma parte externa controlar o DNS ou o proxy, ela poderá forçar que os sites usem o modo IE.

1. Abra o Editor de política de grupo local.
2. Clique em **Configuração do Usuário/Configuração do Computador** > **Modelos Administrativos** > **Microsoft Edge**.
3. Clique duas vezes em **Enviar todos os sites da intranet para o Internet Explorer**.
4. Selecione **Habilitado** e clique em **OK** ou em **Aplicar** para salvar as configurações de política.

## <a name="redirect-sites-from-ie-to-microsoft-edge"></a>Redirecionar sites do IE para o Microsoft Edge

Você pode impedir que os usuários usem o Internet Explorer para sites que não precisam dele. O Internet Explorer pode redirecionar sites para o Microsoft Edge automaticamente se eles não estiverem na sua lista de sites.

1. Abra o Editor de Políticas de Grupo.
2. Clique em **Configuração do Usuário/Configuração do Computador** > **Ferramentas Administrativas** > **Componentes do Windows** > **Internet Explorer**.
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

    > [!TIP]
    > Para localizar sites que você precisa adicionar à sua lista de sites do modo IE, consulte Configurar o modo [IE para Microsoft Edge](https://go.microsoft.com/fwlink/?linkid=2188235) guia. Se você já tiver uma lista de sites, as ferramentas neste guia ajudarão você a aplicá-la aos usuários certos.

## <a name="see-also"></a>Consulte também

- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Sobre o modo IE](./edge-ie-mode.md)
- [Informações adicionais sobre o Modo Empresarial](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
