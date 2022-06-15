---
title: Guia Passo a Passo do Enterprise Site Discovery
ms.author: collw
author: dan-wesley
manager: collw
ms.date: 06/15/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Guia para usar o Enterprise Site Discovery para se preparar para o modo IE.
ms.openlocfilehash: e7db4ddeb3bbaaafdac53814249088e2736d9e7d
ms.sourcegitcommit: 01011d970e85683f74f889651f5f402da642f34a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/15/2022
ms.locfileid: "12595219"
---
# <a name="enterprise-site-discovery-step-by-step-guide"></a>Guia passo a passo da Descoberta de Sites de Empresas

>[!Note]
> O aplicativo da área de trabalho do Internet Explorer 11 foi desativado e está sem suporte a partir de 15 de junho de [2022](https://aka.ms/IEJune15Blog) para determinadas versões do Windows 10.  
>
> - Você ainda pode acessar sites antigos e herdados que exigem o Internet Explorer com o modo Internet Explorer Microsoft Edge. [Saiba como >](https://aka.ms/IEmodewebsite)
> - O aplicativo da área de trabalho do Internet Explorer 11 será redirecionado progressivamente para o navegador mais rápido e seguro Microsoft Edge e, por fim, será desabilitado por meio Windows Update. [Desabilitar o IE hoje>](/deployedge/edge-ie-disable-ie11)  

Este artigo fornece um guia passo a passo para usar o Enterprise Site Discovery com o Microsoft Endpoint Configuration Manager.

> [!TIP]
> A menos que seu ambiente exija o uso das etapas neste guia, recomendamos que você use o assistente de implantação do [Microsoft Edge](https://aka.ms/edgeadvisor) e o script que ele gera para configurar Enterprise Descoberta de Sites.

O Enterprise Site Discovery pode ajudá-lo a configurar sua Lista de Sites do Modo Empresarial. O Enterprise Site Discovery ajudará você a:

- Descubra quais sites estão usando modos de documento herdados. A menos que esses sites estejam detectando navegadores modernos e fornecendo HTML diferente, eles provavelmente precisam usar o modo IE.
- Descubra quais sites estão usando controles ActiveX. O Microsoft Edge não dá suporte a controles ActiveX. A menos que esses sites estejam detectando navegadores modernos e fornecendo HTML diferente, eles provavelmente precisam usar o modo IE.

> [!NOTE]
> Este artigo se aplica aos Canais **Estável**, **Beta** e **Dev** do Microsoft Edge Beta, versão 77 ou posteriores.

## <a name="prerequisites"></a>Pré-requisitos

Este guia pressupõe que você tenha experiência com o Gerenciador de Configurações do Microsoft Endpoint e tenha os seguintes serviços e funções instalados:

- Microsoft Endpoint Configuration Manager
- Microsoft SQL Server Reporting Services
- (Opcional) Configuration Manager Reporting Services função de ponto está configurada

## <a name="download-enterprise-site-discovery-tools"></a>Baixar Ferramentas do Enterprise Site Discovery

Baixe as seguintes ferramentas:

- [Pacote de Instalação e Configuração do Enterprise Site Discovery](https://go.microsoft.com/fwlink/p/?LinkId=517719)
- [Construtor de Relatórios da Microsoft](https://www.microsoft.com/download/details.aspx?id=53613)

## <a name="enable-enterprise-site-discovery"></a>Habilitar o Enterprise Site Discovery

Antes de se conectar ao WMI (instrumentação de gerenciamento) do Windows para recuperar dados de descoberta de site, você precisa implantar o provedor de classe WMI no dispositivo que está coletando esses dados.

Em **Pacote de Instalação e Configuração do Enterprise Site Discovery**, extraia o conteúdo para uma pasta em seu compartilhamento de arquivo definitivo da biblioteca de software. Exemplo: **\\\\DSL\\EnterpriseSiteDiscovery**.

Em seguida, crie um pacote Microsoft Endpoint Configuration Manager, conforme descrito em [Pacotes e programas Configuration Manager](/configmgr/apps/deploy-use/packages-and-programs).

Defina o novo pacote com as seguintes configurações:

- Na página **Pacote** :
  - selecione **Nome e** especifique o nome **Habilitar Descoberta de Site**
  - select **Este pacote contém arquivos de origem**
  - especifique a pasta de origem para a qual você extraiu os arquivos (por exemplo, **\\\\DSL\\EnterpriseSiteDiscovery**)
- Na página **Tipo de programa**, escolha **Programa Padrão**
- Na página **Programa Padrão** , insira o seguinte comando para configurar a Descoberta de Site no dispositivo:

  ```dos
  
    powershell.exe -ExecutionPolicy Bypass .\IETelemetrySetUp-Win8.ps1

  ```

  > [!NOTE]
  > O script suporta o uso de opções de linha de comando para `-ZoneAllowList` e `-SiteAllowList`. Para este passo a passo, configuraremos essas opções por meio da política [de grupo](#configure-enterprise-site-discovery-via-group-policy).

- Na página **Programa** Padrão:
  - selecione a opção para executar **Oculto**
  - em **Programa pode ser executado**, selecione a **opção Se um usuário está conectado ou não**

Após criar o pacote, clique duas vezes no nome do pacote **Ativar Descoberta do Site** para visualizar suas propriedades. Para a **propriedade Após a execução** , selecione **Configuration Manager reinicia o computador**. A coleta de dados WMI será iniciada após a reinicialização dos dispositivos.

> [!NOTE]
> Você pode configurar o tempo que um usuário precisa para reiniciar o dispositivo, conforme descrito na [documentação de configurações do cliente](/configmgr/core/clients/deploy/about-client-settings#computer-restart).

Para confirmar que a coleta de dados está funcionando, visite alguns sites e execute o comando do PowerShell a seguir para verificar se os dados estão sendo preenchidos no namespace do WMI.

```powershell

Get-WmiObject -Namespace “root/cimv2/IETelemetry” -Class IEURLInfo | Select-Object URL, NumberOfVisits, CrashCount, DocMode | Sort-Object

```

## <a name="configure-enterprise-site-discovery-via-group-policy"></a>Configurar o Enterprise Site Discovery por meio da Política de Grupo

Com o Enterprise Site Discovery habilitado, você pode configurar quais dados coletará. Considere as leis locais e os requisitos regulatórios, conforme descrito [em Quais dados são coletados?](/internet-explorer/ie11-deploy-guide/collect-data-using-enterprise-site-discovery#what-data-is-collected).

1. Abra o Editor de Política de Grupo.
2. Selecione **Modelos Administrativos** >  de  > **Configuração do** **Computador Windows Componentes do** > **Internet Explorer**.
3. Clique duas vezes **em Ativar saída WMI de Descoberta de Site**.
4. Selecione **Habilitado**.
5. Selecione **OK** ou **Aplicar** para salvar esta configuração de política.

Você pode escolher as zonas em que deseja coletar dados do site:

1. Clique duas vezes em **Limitar a saída da Descoberta de Site por Zona**.
2. Selecione **Habilitado**.
3. Defina **a Máscara de**  Zona para indicar para quais das zonas a seguir habilitar a descoberta de site.

    - Zona de Sites Restritos
    - Zona da Internet
    - Zona de Sites Confiáveis
    - Zona da Intranet Local
    - Zona do Computador Local
   > [!NOTE]
   > Para configurar zonas incluídas na descoberta de site, um número binário é formado com base nas zonas selecionadas. A representação decimal desse número é usada para representar esse número na política.

    Exemplos: a Máscara de Zona 2: **00010** coletará dados para a zona da Intranet Local somente a Máscara de Zona 6: **00110** coletará dados somente para zonas de site confiáveis e intranet

4. Selecione **OK** ou **Aplicar** para salvar esta configuração de política.

Você também pode limitar os domínios para os quais coletar dados do site:

1. Clique duas vezes em **Limitar saída da Descoberta de Site por domínio**.
2. Selecione **Habilitado**.
3. Insira os domínios para os quais você deseja coletar dados, um domínio por linha.
4. Selecione **OK** ou **Aplicar** para salvar esta configuração de política.

## <a name="collect-site-discovery-data-using-configuration-manager"></a>Colete dados da Descoberta do Site usando o Gerenciador de Configurações

Agora que seus dispositivos estão gerando dados, é hora de coletar esses dados no Gerenciador de Configurações.

1. No console Configuration Manager, escolha **Cliente** >  de**Administração Configurações** >  **Cliente Padrão Configurações**.
2. No grupo **Propriedades** da guia **Página Inicial,** escolha **Propriedades**.
3. Na caixa **de diálogo Configurações** Cliente Padrão, escolha **Inventário de Hardware**.
4. Na lista **de Configurações** dispositivo, escolha **Definir Classes**.
5. Na caixa **de diálogo Classes de Inventário de Hardware** , escolha **Adicionar**.
6. Na caixa **de diálogo Adicionar Classe de Inventário de** Hardware, **selecione Conexão**.
7. Na caixa de diálogo **Conectar-se à Instrumentação de Gerenciamento do Windows (WMI)**, digite o nome de um computador onde o Enterprise Site Discovery está configurado. Se você estiver se conectando a outro computador, precisará de credenciais com permissão para acessar o WMI.
8. Na caixa **de texto namespace WMI** , insira **root\cimv2\IETelemetry**.
9. Escolha **Conexão**.
10. Na caixa **de diálogo** Adicionar Classe de Inventário de Hardware, **** na lista classes Inventory, selecione as classes WMI **IESystemINfo**, **IEUrlInfo** e **IECountInfo**.
11. Selecione **OK** para fechar a **caixa de diálogo Qualificadores de** classe e os outros diálogos abertos.

Depois que o cliente atualizar as configurações do ponto de gerenciamento, os dados serão relatados quando o próximo inventário de hardware for executado (por padrão a cada sete dias).

## <a name="import-site-discovery-reports"></a>Importar relatórios de Descoberta do Site

O pacote Enterprise Site Discovery inclui dois exemplos de relatórios. Um relatório mostra sites usando ActiveX e o relatório mostra sites usando modos de documento herdados.

### <a name="configure-the-site-discovery-sample-report"></a>Configure o relatório de exemplo de Descoberta do Site

Use as etapas como um guia para criar um relatório de exemplo que usa três fontes de dados. Essas fontes de dados são: os sites que um usuário visita, informações sobre seu sistema e os modos de documento usados pelos sites. Este relatório ajuda a identificar sites que podem depender dos modos de documentos herdados.

1. Copie o relatório **SCCM_Report-Site_Discovery.rdl** no servidor do Gerenciador de Configurações.
2. Instale o [Construtor de Relatórios da Microsoft](/sql/reporting-services/install-windows/install-report-builder).
3. Clique duas vezes em **SCCM_Report-Site_Discovery.rdl** para abrir o relatório no Construtor de Relatórios.
4. Na primeira vez que você tentar abrir o relatório, ele tentará entrar em contato com o servidor onde ele foi criado. Quando for solicitado a Conexão **para o Servidor de Relatório**, selecione **Não**.
5. Depois que o relatório for aberto, expanda **Fontes de Dados** e clique duas vezes em **DataSource1**.
6. Na janela **Propriedades da Fonte de** Dados, **selecione Usar uma conexão inserida no meu relatório** e, em seguida, **selecione Compilar...**.

> [!NOTE]
> Certifique-se de selecionar Microsoft SQL Server como a Fonte de Dados. Report Builder padrão é Microsoft SQL Server Analysis Services como a fonte de dados.

7. Na janela **Propriedades da Conexão**, selecione **Nome do Servidor** e digite o nome do servidor do Gerenciador de Configurações. Em seguida, em **Selecionar ou inserir um nome de banco de dados**, selecione o nome do banco de dados do Gerenciador de Configurações na lista suspensa.
8. Selecione **OK** para fechar a **janela Propriedades da** Conexão.
9. Selecione **Testar Conexão** para testar a conexão. Se a conexão for bem-sucedida, selecione **OK** para fechar a janela **Propriedades da Fonte de** Dados.
10. Repita as etapas 5 a 9 para a **Fonte de Dados 2**.
11. Expanda **Conjuntos de Dados** e clique duas vezes em **DataSet1**.
12. Na janela **Propriedades do Conjunto de** Dados, clique na **caixa de texto Consulta:** Copie a consulta para Bloco de notas e, em seguida, localize e substitua **** CM_A1B pelo nome do banco de dados selecionado na Etapa 7. Cole a consulta atualizada na **caixa de texto Consulta:**
13. Repita as etapas 11 a 12 para **DataSet2**, **DataSet3** e **DataSet4**.
14. Na guia **Página Inicial** da faixa de opções, selecione o **botão** Executar para testar o relatório.
15. Salve o relatório e feche o Microsoft Report Builder.
17. Renomear o arquivo de relatório para **Site Discovery.rdl**

### <a name="configure-the-activex-sample-report"></a>Configure o relatório de exemplo ActiveX

Use o procedimento a seguir para criar um relatório de exemplo que usa uma fonte de dados: os sites que estão usando controles ActiveX. Como o Internet Explorer é o único navegador que dá suporte ActiveX controles, esses sites podem exigir o modo IE no Microsoft Edge.

1. Copie o relatório **Exemplo de relatório SCCM - ActiveX.rdl** para o servidor do Gerenciador de Configurações.
2. Instale o [Construtor de Relatórios da Microsoft](/sql/reporting-services/install-windows/install-report-builder).
3. Clique duas vezes em **Exemplo de relatório SCCM - ActiveX.rdl** para abrir o relatório no Construtor de Relatórios.
4. Na primeira vez que você tentar abrir o relatório, ele tentará entrar em contato com o servidor onde ele foi criado. Quando for solicitado a Conexão **para o Servidor de Relatório**, selecione **Não**.
5. Depois de abrir o relatório, expanda **Fontes de Dados** e clique duas vezes em **AutoGen__5C6358F2_4BB6_4a1b_A16E_8D96795D8602_**.
6. Na janela **Propriedades da Fonte de** Dados, **selecione Usar uma conexão inserida no meu relatório** e, em seguida, **selecione Compilar...**.
7. Na janela **Propriedades da Conexão**, selecione **Nome do Servidor** e digite o nome do servidor do Gerenciador de Configurações. Em seguida, em **Selecionar ou inserir um nome de banco de dados**, selecione o nome do banco de dados do Gerenciador de Configurações na lista suspensa.
8. Selecione **OK** para fechar a **janela Propriedades da** Conexão.
9. Selecione **Testar Conexão** para testar a conexão. Se a conexão for bem-sucedida, selecione **OK** para fechar a janela **Propriedades da Fonte de** Dados.
10. Expanda **Conjuntos de Dados** e clique duas vezes em **DataSet1**.
11. Na janela **Propriedades do Conjunto de** Dados, clique na **caixa de texto Consulta:** Copie a consulta para Bloco de notas e, em seguida, localize e substitua **** CM_A1B pelo nome do banco de dados selecionado na Etapa 7. Cole a consulta atualizada na **caixa de texto Consulta:**
12. Na guia **Página Inicial** da faixa de opções, selecione o **botão** Executar para testar o relatório.
13. Salve o relatório.
14. Feche o Construtor de Relatórios da Microsoft.
15. Renomeie o arquivo para **ActiveX**

### <a name="upload-configured-reports-to-microsoft-sql-server-reporting-services"></a>Carregue relatórios configurados no Microsoft SQL Server Reporting Services

Depois de configurar os relatórios para o seu ambiente, carregue-os no servidor de relatórios.

1. Inicie o aplicativo **Gerenciador de Configurações do Reporting Services**.
2. Na janela **Conexão do Servidor de** Relatório, **selecione Conexão** e, em seguida, selecione a URL listada em **Identificação do Site do Portal da Web**
3. Na janela do navegador que é aberta, você deve estar na página **SQL Server Reporting Services** - selecione a pasta ConfigMgr_SCCMSiteCode para **** o Código do Site do SCCM.
4. Na faixa de opções, passe o mouse **sobre +Novo** e selecione o item **de** menu Pasta.
5. Insira um nome de pasta, como **Enterprise Descoberta de Site**, e selecione o **botão** Criar.
6. Selecione a pasta **Enterprise Descoberta de Site**.
7. Na faixa de opções, selecione o **Upload** botão.
8. Selecione o **relatório descoberta de** site e selecione **OK**.
9. Repita as etapas 7 e 8 para o relatório **ActiveX**.

### <a name="view-reports-in-configuration-manager"></a>Visualize os relatórios no Gerenciador de Configurações

Agora que você personalizou e enviou os relatórios, é possível visualizá-los no Gerenciador de Configurações.

1. No console do Gerenciador de Configurações, escolha **Monitoramento** > **Reportar** > **Relatórios** > **Enterprise Site Discovery**
2. Clique duas vezes em um relatório para visualizá-lo.

## <a name="disable-enterprise-site-discovery"></a>Desabilitar o Enterprise Site Discovery

Quando terminar de coletar dados, desabilite a Enterprise Site Discovery. Crie um segundo pacote para desabilitar Enterprise Descoberta de Sites no Microsoft Endpoint Configuration Manager, conforme descrito nos pacotes e programas [no Configuration Manager](/configmgr/apps/deploy-use/packages-and-programs). Configure as seguintes opções:

- Na página **Pacote** :
  - selecione **Nome e** especifique o nome **Desabilitar Descoberta de Site**.
  - select **Este pacote contém arquivos de origem**.
  - especifique a pasta de origem para a qual você extraiu os arquivos (por exemplo, **\\\\DSL\\EnterpriseSiteDiscovery**).
- Na página **Tipo de** Programa, escolha **Programa Padrão**.
- Na página **Programa Padrão** , insira a seguinte linha de comando para desabilitar a Descoberta de Site no dispositivo:

  ```dos
  powershell.exe -ExecutionPolicy Bypass .\IETelemetrySetUp-Win8.ps1 -IEFeatureOff

  ```

- Na página **Programa** Padrão:
  - selecione a opção **Executar** Oculto.
  - em **Programa pode ser executado**, selecione a **opção Se um usuário está conectado ou não**.

## <a name="see-also"></a>Consulte também

- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Sobre o modo IE](./edge-ie-mode.md)
- [Informações adicionais sobre o Modo Empresarial](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
- [Informações adicionais sobre o Enterprise Site Discovery](/internet-explorer/ie11-deploy-guide/collect-data-using-enterprise-site-discovery)
