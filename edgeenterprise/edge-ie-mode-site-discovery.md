---
title: Guia Passo a Passo do Enterprise Site Discovery
ms.author: collw
author: appcompatguy
manager: saudm
ms.date: 01/19/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Usar o Enterprise Site Discovery para se Preparar para o Modo IE
ms.openlocfilehash: a93569f455e5671a2d4adf8f5f70238d3f23143d
ms.sourcegitcommit: 556aca8dde42dd66364427f095e8e473b86651a0
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2022
ms.locfileid: "12445595"
---
# <a name="enterprise-site-discovery-step-by-step-guide"></a>Guia Passo a Passo do Enterprise Site Discovery

>[!Note]
> O aplicativo de área de trabalho Internet Explorer 11 será desativado e ficará sem suporte em 15 de junho de 2022 (para obter uma lista do que está no escopo, [consulte as Perguntas frequentes](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/internet-explorer-11-desktop-app-retirement-faq/ba-p/2366549)). Os mesmos aplicativos e sites do IE11 que você usa hoje podem abrir no Microsoft Edge com o modo Internet Explorer. [Saiba mais aqui](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/).

Este artigo fornece um guia passo a passo para usar o Enterprise Site Discovery com o Microsoft Endpoint Configuration Manager.

O Enterprise Site Discovery pode ajudá-lo a configurar sua Lista de Sites do Modo Empresarial. O Enterprise Site Discovery ajudará você a:

- Descubra quais sites estão usando modos de documento herdados. A menos que esses sites estejam detectando navegadores modernos e fornecendo HTML diferente, eles provavelmente precisam usar o modo IE.
- Descubra quais sites estão usando controles ActiveX. O Microsoft Edge não dá suporte a controles ActiveX. A menos que esses sites estejam detectando navegadores modernos e fornecendo HTML diferente, eles provavelmente precisam usar o modo IE.

> [!NOTE]
> Este artigo se aplica aos Canais **Estável**, **Beta** e **Dev** do Microsoft Edge Beta, versão 77 ou posteriores.

## <a name="prerequisites"></a>Pré-requisitos

Este guia pressupõe que você tenha experiência com o Gerenciador de Configurações do Microsoft Endpoint e tenha os seguintes serviços e funções instalados:

1. Microsoft Endpoint Configuration Manager
2. Microsoft SQL Server Reporting Services
3. (Opcional) Função de Ponto do Reporting Services do Gerenciador de Configurações configurada

## <a name="download-enterprise-site-discovery-tools"></a>Baixar Ferramentas do Enterprise Site Discovery

Baixe as seguintes ferramentas:

- [Pacote de Instalação e Configuração do Enterprise Site Discovery](https://go.microsoft.com/fwlink/p/?LinkId=517719)
- [Construtor de Relatórios da Microsoft](https://www.microsoft.com/download/details.aspx?id=53613)

## <a name="enable-enterprise-site-discovery"></a>Habilitar o Enterprise Site Discovery

Para que você possa se conectar à Instrumentação de Gerenciamento do Windows (WMI) para recuperar dados de descoberta do site, primeiro implante o provedor de classe WMI no dispositivo.

Em **Pacote de Instalação e Configuração do Enterprise Site Discovery**, extraia o conteúdo para uma pasta em seu compartilhamento de arquivo definitivo da biblioteca de software. Exemplo: **\\\\DSL\\EnterpriseSiteDiscovery**.

Em seguida, crie um pacote no Gerenciador de Configurações do Microsoft Endpoint, conforme descrito na [documentação](/configmgr/apps/deploy-use/packages-and-programs), selecionando as seguintes opções:

- Na página **Pacote**, selecione **Nome** e especifique o nome **Habilitar Descoberta do Site**
- Na página **Pacote**, selecione **Este pacote contém arquivos de origem**
- Na página **Pacote**, especifique a pasta de origem para a qual você extraiu os arquivos (por exemplo, **\\\\DSL\\EnterpriseSiteDiscovery**)
- Na página **Tipo de programa**, escolha **Programa Padrão**
- Na página **Programa Padrão**, digite a linha de comando para configurar o Descoberta do Site no dispositivo da seguinte maneira:
  ```dos
  powershell.exe -ExecutionPolicy Bypass .\IETelemetrySetUp-Win8.ps1
  ```
  > [!NOTE]
  > O script suporta o uso de opções de linha de comando para `-ZoneAllowList` e `-SiteAllowList`. Para este passo a passo, configuraremos essas opções por meio da política de grupo (abaixo).
- Na página **Programa Padrão**, selecione a opção para executar **Oculto**.
- Na página **Programa Padrão**, em **Programa pode executar**, selecione a opção **Se um usuário está ou não conectado**.

Após criar o pacote, clique duas vezes no nome do pacote **Ativar Descoberta do Site** para visualizar suas propriedades. Na propriedade **Após a execução**, selecione **Gerenciador de configuração reinicia o computador**. A coleta de dados WMI começará após a reinicialização dos dispositivos.

> [!NOTE]
> Você pode configurar o tempo que um usuário precisa para reiniciar o dispositivo, conforme descrito na [documentação de configurações do cliente](/configmgr/core/clients/deploy/about-client-settings#computer-restart).

## <a name="configure-enterprise-site-discovery-via-group-policy"></a>Configurar o Enterprise Site Discovery por meio da Política de Grupo

Com o Enterprise Site Discovery habilitado, você pode configurar quais dados coletará. Considere as leis locais e os requisitos regulatórios, conforme descrito [aqui](/internet-explorer/ie11-deploy-guide/collect-data-using-enterprise-site-discovery#what-data-is-collected).

1. Abrir o Editor de Política de Grupo
2. Clique em **Configuração do Computador** > **Modelos Administrativos** > **Componentes do Windows** > **Internet Explorer** 
3. Clique duas vezes em **Ativar saída WMI da Descoberta do Site**
4. Selecione **Habilitado**
5. Clique em **OK** ou em **Aplicar** para salvar essa configuração de política

Você pode limitar as zonas nas quais você coleta dados do site:

1. Clique duas vezes em **Limitar saída da Descoberta do Site por Zona**
2. Selecione **Habilitado**
3. Insira uma bitmask indicando em quais zonas habilitar a descoberta do site:
    1. Zona de Sites Restritos
    2. Zona da Internet
    3. Zona de Sites Confiáveis
    4. Zona da Intranet Local
    5. Zona do Computador Local
    
    Exemplo 1: **00010** coletará dados apenas para a zona da Intranet Local

    Exemplo 2: **10111** coletará dados para todas as zonas, exceto a zona da Internet
4. Clique em **OK** ou em **Aplicar** para salvar essa configuração de política

Você pode limitar os domínios para os quais você coleta dados do site:

1. Clique duas vezes em **Limitar saída da Descoberta do Site por domínio**
2. Selecione **Habilitado**
3. Digite os domínios para os quais você deseja coletar dados, um domínio por linha
4. Clique em **OK** ou em **Aplicar** para salvar essa configuração de política

## <a name="collect-site-discovery-data-using-configuration-manager"></a>Colete dados da Descoberta do Site usando o Gerenciador de Configurações

Agora que seus dispositivos estão gerando dados, é hora de coletar esses dados no Gerenciador de Configurações.

1. No console do Gerenciador de Configurações, escolha **Administração** > **Configurações do Cliente** > **Configurações Padrão do Cliente**
2. Na guia **Página Inicial**, no grupo **Propriedades**, escolher **Propriedades**
3. Na caixa de diálogo **Configurações Padrão do Cliente**, escolha **Inventário de Hardware**
4. Na lista **Configurações do Dispositivo**, escolha **Definir Slasses**
5. Na caixa de diálogo **Classes de Inventário de Hardware**, escolha **Adicionar**
6. Na caixa de diálogo **Adicionar Classe de Inventário de Hardware**, clique em **Conectar**
7. Na caixa de diálogo **Conectar-se à Instrumentação de Gerenciamento do Windows (WMI)**, digite o nome de um computador onde o Enterprise Site Discovery está configurado. Se você estiver se conectando a outro computador, precisará de credenciais com permissão para acessar o WMI.
8. Na caixa de texto **Namespace WMI**, digite **root\cimv2\IETelemetry**
9. Escolha **Conectar**
10. Na caixa **de diálogo Adicionar** Classe de Inventário de Hardware, **** na lista De classes inventário, selecione as classes WMI **IESystemINfo**, **IEUrlInfo** e **IECountInfo**.
11. Clique em **OK** para fechar a caixa de diálogo **Classificadores de classe** e as outras caixas de diálogo abertas.

Depois que o cliente atualizar as configurações do ponto de gerenciamento, os dados serão relatados quando o próximo inventário de hardware for executado (por padrão a cada sete dias).

## <a name="import-site-discovery-reports"></a>Importar relatórios de Descoberta do Site

O pacote Enterprise Site Discovery inclui dois exemplos de relatórios. Um relatório mostra sites usando controles ActiveX e outro mostra sites usando modos de documento herdados.

### <a name="configure-the-site-discovery-sample-report"></a>Configure o relatório de exemplo de Descoberta do Site

Use o procedimento a seguir para criar um relatório de exemplo que use três fontes de dados: os sites que um usuário visita, informações sobre o sistema e os modos de documento usados ​​pelos sites. Este relatório ajuda a identificar sites que podem depender dos modos de documentos herdados.

1. Copie o relatório **SCCM_Report-Site_Discovery.rdl** no servidor do Gerenciador de Configurações.
2. Instale o [Construtor de Relatórios da Microsoft](/sql/reporting-services/install-windows/install-report-builder?view=sql-server-ver15).
3. Clique duas vezes em **SCCM_Report-Site_Discovery.rdl** para abrir o relatório no Construtor de Relatórios.
4. Na primeira vez que você tentar abrir o relatório, ele tentará entrar em contato com o servidor onde ele foi criado. Quando solicitado a **Conectar-se ao Servidor de Relatório**, clique em **Não**.
5. Depois que o relatório for aberto, expanda **Fontes de Dados** e clique duas vezes em **DataSource1**.
6. Na janela **Propriedades da Fonte de Dados**, selecione **Usar uma conexão incorporada no meu relatório** e clique no botão **Build...**.
7. Na janela **Propriedades da Conexão**, selecione **Nome do Servidor** e digite o nome do servidor do Gerenciador de Configurações. Em seguida, em **Selecionar ou inserir um nome de banco de dados**, selecione o nome do banco de dados do Gerenciador de Configurações na lista suspensa.
8. Clique em **OK** para fechar a janela **Propriedades da Conexão**.
9. Clique em **Testar Conexão** para testar a conexão. Se a conexão for bem-sucedida, clique em **OK** para fechar a janela **Propriedades da Fonte de Dados**.
10. Repita as etapas 5 a 9 para a **Fonte de Dados 2**.
11. Expanda **Conjuntos de Dados** e clique duas vezes em **DataSet1**.
12. Na janela **Propriedades do Conjunto de Dados**, clique na caixa de texto **Consulta:** e substitua **USE CM_A1B** pelo nome do banco de dados selecionado na Etapa 7.
13. Repita as etapas 11 a 12 para **DataSet2**, **DataSet3** e **DataSet4**.
14. Na guia **Página Inicial** da faixa de opções, clique no botão **Executar** para testar o relatório.
15. Salve o relatório.
16. Feche o Construtor de Relatórios da Microsoft.
17. Renomeie o arquivo para **Descoberta do Site.rdl**

### <a name="configure-the-activex-sample-report"></a>Configure o relatório de exemplo ActiveX

Use o procedimento a seguir para criar um relatório de exemplo que usa uma fonte de dados: os sites que estão usando controles ActiveX. Como o Internet Explorer é o único navegador que suporta controles ActiveX, esses sites podem exigir o modo IE.

1. Copie o relatório **Exemplo de relatório SCCM - ActiveX.rdl** para o servidor do Gerenciador de Configurações.
2. Instale o [Construtor de Relatórios da Microsoft](/sql/reporting-services/install-windows/install-report-builder?view=sql-server-ver15).
3. Clique duas vezes em **Exemplo de relatório SCCM - ActiveX.rdl** para abrir o relatório no Construtor de Relatórios.
4. Na primeira vez que você tentar abrir o relatório, ele tentará entrar em contato com o servidor onde ele foi criado. Quando solicitado a **Conectar-se ao Servidor de Relatório**, clique em **Não**.
5. Depois de abrir o relatório, expanda **Fontes de Dados** e clique duas vezes em **AutoGen__5C6358F2_4BB6_4a1b_A16E_8D96795D8602_**.
6. Na janela **Propriedades da Fonte de Dados**, selecione **Usar uma conexão incorporada no meu relatório** e clique no botão **Build...**.
7. Na janela **Propriedades da Conexão**, selecione **Nome do Servidor** e digite o nome do servidor do Gerenciador de Configurações. Em seguida, em **Selecionar ou inserir um nome de banco de dados**, selecione o nome do banco de dados do Gerenciador de Configurações na lista suspensa.
8. Clique em **OK** para fechar a janela **Propriedades da Conexão**.
9. Clique em **Testar Conexão** para testar a conexão. Se a conexão for bem-sucedida, clique em **OK** para fechar a janela **Propriedades da Fonte de Dados**.
10. Expanda **Conjuntos de Dados** e clique duas vezes em **DataSet1**.
11. Na janela **Propriedades do Conjunto de Dados**, clique na caixa de texto **Consulta:** e substitua **USE CM_A1B** pelo nome do banco de dados selecionado na Etapa 7.
12. Na guia **Página Inicial** da faixa de opções, clique no botão **Executar** para testar o relatório.
13. Salve o relatório.
14. Feche o Construtor de Relatórios da Microsoft.
15. Renomeie o arquivo para **ActiveX**

### <a name="upload-configured-reports-to-microsoft-sql-server-reporting-services"></a>Carregue relatórios configurados no Microsoft SQL Server Reporting Services

Depois de configurar os relatórios para o seu ambiente, carregue-os no servidor de relatórios.

1. Inicie o aplicativo **Gerenciador de Configurações do Reporting Services**.
2. Na janela **Conexão do Servidor de Relatório**, clique em **Conectar** e, em seguida, clique no URL listado em **Identificação de Site do Portal da Web**
3. Na janela do navegador que é aberta, você deve estar na **Página SQL Server Reporting Services** - clique na pasta **ConfigMgr_SCCMSiteCode** para o seu Código de Site do SCCM.
4. Na faixa de opções, passe o mouse sobre **+Novo** e clique no item de menu **Pasta**.
5. Digite um nome da pasta, como **Enterprise Site Discovery**, e clique no botão **Criar**.
6. Clique na pasta **Enterprise Site Discovery**.
7. Na faixa de opções, clique no botão **Carregar**.
8. Selecione o relatório de **Descoberta do Site** e clique em **OK**.
9. Repita as etapas 7 e 8 para o relatório **ActiveX**.

### <a name="view-reports-in-configuration-manager"></a>Visualize os relatórios no Gerenciador de Configurações

Agora que você personalizou e enviou os relatórios, é possível visualizá-los no Gerenciador de Configurações.

1. No console do Gerenciador de Configurações, escolha **Monitoramento** > **Reportar** > **Relatórios** > **Enterprise Site Discovery**
2. Clique duas vezes em um relatório para visualizá-lo.

## <a name="disable-enterprise-site-discovery"></a>Desabilitar o Enterprise Site Discovery

Quando terminar de coletar dados, você deve desabilitar o Enterprise Site Discovery. Crie um segundo pacote para desabilitar o Enterprise Site Discovery no Gerenciador de Configurações do Microsoft Endpoint, conforme descrito na [documentação](/configmgr/apps/deploy-use/packages-and-programs), selecionando as seguintes opções:

- Na página **Pacote**, selecione **Nome** e especifique o nome **Desabilitar Descoberta do Site**
- Na página **Pacote**, selecione **Este pacote contém arquivos de origem**
- Na página **Pacote**, especifique a pasta de origem para a qual você extraiu os arquivos (por exemplo, **\\\\DSL\\EnterpriseSiteDiscovery**)
- Na página **Tipo de programa**, escolha **Programa Padrão**
- Na página **Programa Padrão**, digite a linha de comando que desabilitará a Descoberta do Site no dispositivo da seguinte maneira:
  ```dos
  powershell.exe -ExecutionPolicy Bypass .\IETelemetrySetUp-Win8.ps1 -IEFeatureOff
  ```
- Na página **Programa Padrão**, selecione a opção para executar **Oculto**
- Na página **Programa Padrão**, em **Programa pode executar**, selecione a opção **Se um usuário está ou não conectado**.

## <a name="see-also"></a>Consulte também

- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Sobre o modo IE](./edge-ie-mode.md)
- [Informações adicionais sobre o Modo Empresarial](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
- [Informações adicionais sobre o Enterprise Site Discovery](/internet-explorer/ie11-deploy-guide/collect-data-using-enterprise-site-discovery)