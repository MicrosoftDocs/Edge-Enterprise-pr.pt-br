---
title: Configurar o Microsoft Edge usando o Gerenciamento de Dispositivo Móvel
ms.author: kvice
author: dan-wesley
manager: laurawi
ms.date: 10/25/2019
audience: ITPro
ms.topic: technical
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Configurar o Microsoft Edge usando o Gerenciamento de Dispositivo Móvel.
ms.openlocfilehash: c9a725b5d0e820fb907150a8f83eeb17291b9f6a
ms.sourcegitcommit: f363ceb6c42054fabc95ce8d7bca3c52d80e6a9f
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/24/2021
ms.locfileid: "11447545"
---
# <a name="configure-microsoft-edge-using-mobile-device-management"></a>Configurar o Microsoft Edge usando o Gerenciamento de Dispositivo Móvel

Este artigo explica como configurar o Microsoft Edge no Windows 10 usando o [Gerenciamento de Dispositivo Móvel (MDM)](/windows/client-management/mdm/) por meio da [Ingestão de ADMX](/windows/client-management/mdm/win32-and-centennial-app-policy-configuration). Este artigo também descreve:

- Como [criar um OMA-URI (Open Mobile Alliance Uniform Resource Identifier) para políticas do Microsoft Edge](#create-an-oma-uri-for-microsoft-edge-policies).
- Como [configurar o Microsoft Edge no Intune usando a ingestão de ADMX e o OMA-URI personalizado](#configure-microsoft-edge-in-intune-using-admx-ingestion).

> [!NOTE]
> Este artigo aplica-se ao Microsoft Edge versão 77 ou posterior.

## <a name="prerequisites"></a>Pré-requisitos

Windows 10 com os seguintes requisitos mínimos do sistema:

- Windows 10, versão 1903 com [KB4512941](https://support.microsoft.com/help/4512941/) e [KB4517211](https://support.microsoft.com/help/4517211/) instalados
- Windows 10, versão 1809 com [KB4512534](https://support.microsoft.com/help/4512534/) e [KB4520062](https://support.microsoft.com/help/4520062/) instalados
- Windows 10, versão 1803 com [KB4512509](https://support.microsoft.com/help/4512509/) e [KB4519978](https://support.microsoft.com/help/4519978) instalados
- Windows 10, versão 1709 com [KB4516071](https://support.microsoft.com/help/4516071/) e [KB4520006](https://support.microsoft.com/help/4520006) instalados

## <a name="overview"></a>Visão geral

Você pode configurar o Microsoft Edge no Windows 10 usando o MDM com seu provedor de EMM (Gerenciamento de Mobilidade Empresarial) ou MDM preferencial que dê suporte à [Ingestão de ADMX](/windows/client-management/mdm/win32-and-centennial-app-policy-configuration).

Configurar o Microsoft Edge com MDM é um processo de duas partes:

1. A ingestão do arquivo ADMX do Microsoft Edge no seu provedor de EMM ou MDM. Consulte seu provedor para obter instruções sobre como ingerir um arquivo ADMX.

   > [!NOTE]
   > Para o Microsoft Intune, consulte [Configurar o Microsoft Edge no Intune usando a ingestão de ADMX](#configure-microsoft-edge-in-intune-using-admx-ingestion).

2. [Como criar um OMA-URI para uma política do Microsoft Edge](#create-an-oma-uri-for-microsoft-edge-policies).

## <a name="create-an-oma-uri-for-microsoft-edge-policies"></a>Criar um OMA-URI para políticas do Microsoft Edge

As seções a seguir descrevem como criar o caminho OMA-URI e pesquisar e definir o valor no formato XML para políticas de navegador obrigatórias e recomendadas.

Antes de começar, baixe o arquivo de modelos de política do Microsoft Edge (MicrosoftEdgePolicyTemplates.cab) da [página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise) e extraia o conteúdo.

Há três etapas para definir o OMA-URI:

1. [Criar o caminho OMA-URI](#create-the-oma-uri-path)
2. [Especificar o tipo de dados OMA-URI](#specify-the-data-type)
3. [Definir o valor do OMA-URI](#set-the-value-for-a-browser-policy)

### <a name="create-the-oma-uri-path"></a>Criar o caminho OMA-URI

Use a fórmula a seguir como um guia para criar os caminhos OMA-URI. <br/><br/>
*`./Device/Vendor/MSFT/Policy/Config/<ADMXIngestName>~Policy~<ADMXNamespace>~<ADMXCategory>/<PolicyName>`* <br/><br/>

| Parâmetro         | Descrição                                                                                   |
|-------------------|-----------------------------------------------------------------------------------------------|
| \<ADMXIngestName> | Use "Edge" ou o que você definiu ao ingerir o modelo administrativo. Por exemplo, se você tiver usado "./Device/Vendor/MSFT/Policy/ConfigOperations/ADMXInstall/MicrosoftEdge/Policy/EdgeAdmx", então use "MicrosoftEdge".<br/><br/> O `<ADMXIngestionName>` deve corresponder ao que foi usado quando o arquivo ADMX foi ingerido. |
| \<ADMXNamespace>  | "microsoft_edge" ou "microsoft_edge_recommended", dependendo de você estar definindo uma política obrigatória ou recomendada. |
| \<ADMXCategory>   | O "parentCategory" da política é definido no arquivo ADMX. Omita `<ADMXCategory>` se a política não estiver agrupada (nenhuma "parentCategory" definida). |
| \<PolicyName>     | O nome da política pode ser encontrado no artigo [Referência de política do navegador](./microsoft-edge-policies.md). |

#### <a name="uri-path-example"></a>Exemplo de caminho de URI:

Neste exemplo, suponha que o nó `<ADMXIngestName>` tenha sido nomeado como "Edge" e que você está definindo uma política obrigatória. O caminho do URI seria:<br/><br/>
*`./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~<ADMXCategory>/<PolicyName>`*

Se a política não estiver em um grupo (por exemplo, DiskCacheSize), remova "`~<ADMXCategory>`". Substitua `<PolicyName>` pelo nome da política, DiskCacheSize. O caminho do URI seria:<br/><br/>
*`./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge/DiskCacheSize`*

Se a política estiver em um grupo, siga estas etapas:

1. Abra **msedge.admx** com qualquer editor xml.
2. Procure o nome da política que você deseja definir. Por exemplo, "ExtensionInstallForceList".
3. Use o valor do atributo *ref* do elemento *parentCategory*. Por exemplo, "extensões" de \<parentCategory ref=" Extensions"/>.
4. Substitua `<ADMXCategory>` pelo valor do atributo *ref* para construir o caminho do URI. O caminho URI seria:<br/><br/>
*`/Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~Extensions/ExtensionInstallForcelist`*

### <a name="specify-the-data-type"></a>Especificar o tipo de dados

O tipo de dados OMA-URI sempre será "String".

### <a name="set-the-value-for-a-browser-policy"></a>Definir o valor de uma política do navegador

Esta seção descreve como definir o valor, em formato XML, para cada tipo de dados. Vá para [Referência de política do navegador](./microsoft-edge-policies.md) para procurar o tipo de dados da política.

> [!NOTE]
> Para tipos de dados não Boolianos, o valor sempre começa com `<enabled/>`.

#### <a name="boolean-data-type"></a>Tipo de dados Booliano

Para políticas que sejam tipos Boolianos, use `<enabled/>` ou `<disabled/>`.

#### <a name="integer-data-type"></a>Tipo de dados Integer

O valor sempre precisará ser iniciado com o elemento `<enabled/>` seguido por `<data id="[valueName]" value="[decimal value]"/>`.

Para encontrar o nome do valor e o valor decimal para uma nova página de guia, use estas etapas:

1. Abra **msedge.admx** com qualquer editor xml.
2. Procure o elemento `<policy>` em que o atributo de nome corresponda ao nome da política que você deseja definir. Para "RestoreOnStartup", procure `name="RestoreOnStartup"`.
3. No nó `<elements>`, encontre o valor que você deseja definir.
4. Use o valor no atributo "valueName" no nó `<elements>`. Para "RestoreOnStartup", o "valueName" é "RestoreOnStartup".
5. Use o valor no atributo "value" no nó `<decimal>`. Para "RestoreOnStartup" abrir a página da nova guia, o valor é "5".

Para abrir a nova página de guia na inicialização, use:<br>
`<enabled/> <data id="RestoreOnStartup" value="5"/>`

#### <a name="list-of-strings-data-type"></a>Lista de tipos de dados de cadeia de caracteres

O valor sempre precisará ser iniciado com o elemento `<enabled/>` seguido por `<data id="[listID]" value="[string 1];[string 2];[string 3]"/>`.

> [!NOTE]
> O nome do atributo "id=" não é o nome da política, mesmo se na maioria dos casos ele corresponder ao nome da política. É o valor do atributo de ID do nó \<list>, encontrado no arquivo ADMX.

Para localizar o listID e definir o valor para bloquear uma URL, siga estas etapas:

1. Abra **msedge.admx** com qualquer editor xml.
2. Procure o elemento `<policy>` em que o atributo de nome corresponda ao nome da política que você deseja definir. Para "URLBlocklist", procure `name="URLBlocklist"`.
3. Use o valor no atributo "id" do `<list> node for [listID]`.
4. O "valor" é uma lista de URLs separadas por um ponto-e-vírgula (;)

Por exemplo, para bloquear o acesso a `contoso.com` e `https://ssl.server.com`:<br>
`<enabled/> <data id=" URLBlocklistDesc" value="contoso.com;https://ssl.server.com"/>`

#### <a name="dictionary-or-string-data-type"></a>Tipo de dados Dictionary ou String

O valor sempre precisará ser iniciado com `<enabled/>` seguido por `<data id="[textID]" value="[string]"/>`.

Para localizar a textID e definir o valor que defina a localidade, siga estas etapas:

1. Abra **msedge.admx** com qualquer editor xml.
2. Procure o elemento `<policy>` em que o atributo de nome corresponda ao nome da política que você deseja definir. Para "ApplicationLocaleValue", procure `name="ApplicationLocaleValue"`.
3. Use o valor no atributo "id" do nó `<text>` para `[textID]`.
4. Defina o "valor" com o código de cultura.

Para definir a localidade como "es-US" com a política "ApplicationLocaleValue":<br>
`<enabled/> <data id="ApplicationLocaleValue" value="es-US"/>`

### <a name="create-the-oma-uri-for-a-recommended-policies"></a>Criar o OMA-URI para políticas recomendadas

Definir o caminho do URI para políticas recomendadas dependerá da política que você deseja configurar.

#### <a name="to-define-the-uri-path-for-a-recommended-policy"></a>Para definir o caminho do URI para uma política recomendada

Use a fórmula do caminho do URI (*`./Device/Vendor/MSFT/Policy/Config/<ADMXIngestName>~Policy~<ADMXNamespace>~<ADMXCategory>/<PolicyName>`*) e as etapas a seguir para definir o caminho do URI:

1. Abra **msedge.admx** com qualquer editor xml.
2. Se a política que você deseja configurar não estiver em um grupo, pule para a etapa 4 e remova `~<ADMXCategory>` do caminho.
3. Se a política que você deseja configurar estiver em um grupo:

   - Para pesquisar a `<ADMXCategory>`, procure a política que você deseja definir. Ao pesquisar, acrescente "_recommended" ao nome da política. Por exemplo, uma pesquisa para "RegisteredProtocolHandlers_recommended” tem o seguinte resultado:

        ```xml
         <policy class="Both" displayName="$(string.RegisteredProtocolHandlers)" explainText="$(string.RegisteredProtocolHandlers_Explain)" key="Software\Policies\Microsoft\Edge\Recommended" name="RegisteredProtocolHandlers_recommended" presentation="$(presentation.RegisteredProtocolHandlers)">
           <parentCategory ref="ContentSettings_recommended"/>
           <supportedOn ref="SUPPORTED_WIN7_V77"/>
           <elements>
             <text id="RegisteredProtocolHandlers" maxLength="1000000" valueName="RegisteredProtocolHandlers"/>
           </elements>
         </policy>
        ```

   - Copie o valor do atributo *ref* do elemento `<parentCategory>`. Para "ContentSettings", copie "ContentSettings_recommended" de `<parentCategory ref=" ContentSettings_recommended"/>`.
   - Substitua `<ADMXCategory>` pelo valor do atributo *ref* para construir o caminho do URI na fórmula de caminho do URI.

4. O `<PolicyName>` é o nome da política com "_recommended" anexado.

#### <a name="oma-uri-path-examples-for-recommended-policies"></a>Exemplos de caminho OMA-URI para políticas recomendadas

A tabela a seguir mostra exemplos de caminhos OMA-URI para políticas recomendadas.

|              Política               |             OMA-URI                      |
|-----------------------------------|------------------------------------------|
| [RegisteredProtocolHandlers](./microsoft-edge-policies.md#registeredprotocolhandlers)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~ContentSettings_recommended/RegisteredProtocolHandlers_recommended`                        |
| [PasswordManagerEnabled](./microsoft-edge-policies.md#passwordmanagerenabled)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~PasswordManager_recommended/PasswordManagerEnabled_recommended`                        |
| [PrintHeaderFooter](./microsoft-edge-policies.md#printheaderfooter)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~Printing_recommended/PrintHeaderFooter_recommended`                        |
| [SmartScreenEnabled](./microsoft-edge-policies.md#smartscreenenabled)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~SmartScreen_recommended/SmartScreenEnabled_recommended`                        |
| [HomePageLocation](./microsoft-edge-policies.md#homepagelocation)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~Startup_recommended/HomepageLocation_recommended`                        |
| [ShowHomeButton](./microsoft-edge-policies.md#showhomebutton)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~Startup_recommended/ShowHomeButton_recommended`                        |
| [FavoritesBarEnabled](./microsoft-edge-policies.md#favoritesbarenabled)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~/FavoritesBarEnabled_recommended`                        |

### <a name="oma-uri-examples"></a>Exemplos de OMA-URI

Os exemplos de OMA-URI com seu caminho do URI, tipo e um valor de exemplo.

#### <a name="boolean-data-type-examples"></a>Exemplos do tipo de dados Booliano

*[ShowHomeButton](./microsoft-edge-policies.md#ShowHomeButton):*

| Campo   | Valor                                                                                |
|---------|--------------------------------------------------------------------------------------|
| Nome    | Microsoft Edge: ShowHomeButton                                                       |
| OMA-URI | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~Startup/ShowHomeButton` |
| tipo    | String                                                                               |
| Valor   | `<enabled/>`                                                                          |

*[DefaultSearchProviderEnabled](./microsoft-edge-policies.md#DefaultSearchProviderEnabled):*

| Campo   | Valor                                                                                |
|---------|--------------------------------------------------------------------------------------|
| Nome    | Microsoft Edge: DefaultSearchProviderEnabled                                         |
| OMA-URI | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~DefaultSearchProvider/DefaultSearchProviderEnabled`    |
| tipo    | String                                                                               |
| Valor   | `<disable/>`                                                                          |

### <a name="integer-data-type-examples"></a>Exemplos de tipo de dados Integer

*[AutoImportAtFirstRun](./microsoft-edge-policies.md#AutoImportAtFirstRun):*

| Campo   | Valor                                                                                |
|---------|--------------------------------------------------------------------------------------|
| Nome    | Microsoft Edge: AutoImportAtFirstRun                                                 |
| OMA-URI | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge/AutoImportAtFirstRun`   |
| tipo    | String                                                                               |
| Valor   | `<enabled/><data id="AutoImportAtFirstRun" value="1"/>`                             |

*[DefaultImagesSetting](./microsoft-edge-policies.md#DefaultImagesSetting):*

| Campo   | Valor                                                                                |
|---------|--------------------------------------------------------------------------------------|
| Nome    | Microsoft Edge: DefaultImagesSetting                                                 |
| OMA-URI | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~ContentSettings/DefaultImagesSetting`    |
| tipo    | String                                                                               |
| Valor   | `<enabled/><data id="DefaultImagesSetting" value="2"/>`                             |

*[DiskCacheSize](./microsoft-edge-policies.md#DiskCacheSize):*

| Campo   | Valor                                                                                |
|---------|--------------------------------------------------------------------------------------|
| Nome    | Microsoft Edge: DiskCacheSize                                                        |
| OMA-URI | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge/DiskCacheSize`        |
| tipo    | String                                                                               |
| Valor   | `<enabled/><data id="DiskCacheSize" value="1000000"/>`                               |

#### <a name="list-of-strings-data-type-examples"></a>Lista de exemplos de tipos de dados de cadeia de caracteres
<!--
*[NotificationsAllowedForUrls](./microsoft-edge-policies.md#NotificationsAllowedForUrls):*

| Field   | Value                                                                                |
|---------|--------------------------------------------------------------------------------------|
| Name    | Microsoft Edge: NotificationsAllowedForUrls                                          |
| OMA-URI | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~ContentSettings/NotificationsAllowedForUrls`    |
| Type    | String                                                                               |
| Value   | `<enabled/><data id="NotificationsAllowedForUrlsDesc" value="https://www.contoso.com"/>`<br>For multiple list items: `<data id="NotificationsAllowedForUrlsDesc" value="https://www.contoso.com;[*.]contoso.edu"/>`                               |
-->
*[RestoreOnStartupURLS](./microsoft-edge-policies.md#RestoreOnStartupURLS):*

| Campo   | Valor                                                                                |
|---------|--------------------------------------------------------------------------------------|
| Nome    | Microsoft Edge: RestoreOnStartupURLS                                                 |
| OMA-URI | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~Startup/RestoreOnStartupURLs`    |
| Tipo    | String                                                                               |
| Valor   | `<enabled/><data id="RestoreOnStartupURLsDesc" value="1&#xF000;http://www.bing.com"/>`<br>Para vários itens de lista: `<enabled/><data id="RestoreOnStartupURLsDesc" value="1&#xF000;http://www.bing.com&#xF000;2&#xF000;http://www.microsoft.com"/>`  |

*[ExtensionInstallForcelist](./microsoft-edge-policies.md#ExtensionInstallForcelist):*

| Campo   | Valor                                                                                |
|---------|--------------------------------------------------------------------------------------|
| Nome    | Microsoft Edge: ExtensionInstallForcelist                                            |
| OMA-URI | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~Extensions/ExtensionInstallForcelist`    |
| Tipo    | String                                                                               |
| Valor   | `<enabled/><data id="ExtensionInstallForcelistDesc" value="1&#xF000;gbchcmhmhahfdphkhkmpfmihenigjmpp;https://extensionwebstorebase.edgesv.net/v1/crx"/>`                               |

#### <a name="dictionary-and-string-data-type-example"></a>Exemplo de tipo de dados Dictionary e String

*[ProxyMode](./microsoft-edge-policies.md#ProxyMode):*

| Campo   | Valor                                                                                |
|---------|--------------------------------------------------------------------------------------|
| Nome    | Microsoft Edge: ProxyMode                                                            |
| OMA-URI | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~ProxyMode/ProxyMode`  |
| Tipo    | String                                                                               |
| Valor   | `<enabled/><data id="ProxyMode" value="auto_detect"/>`                               |

## <a name="configure-microsoft-edge-in-intune-using-admx-ingestion"></a>Configurar o Microsoft Edge no Intune usando a ingestão de ADMX

A maneira recomendada de configurar o Microsoft Edge com o Microsoft Intune é usar o perfil Modelos Administrativos conforme descrito em [Definir as configurações de política do Microsoft Edge com o Microsoft Intune](./configure-edge-with-intune.md). Se deseja avaliar uma política que no momento não esteja disponível nos Modelos Administrativos do Microsoft Edge no Intune, você poderá configurar o Microsoft Edge usando [configurações personalizadas para dispositivos Windows 10 no Intune](/intune/configuration/custom-settings-windows-10).

Esta seção descreve como:

1. [Ingerir o arquivo ADMX do Microsoft Edge no Intune](#ingest-the-microsoft-edge-admx-file-into-intune)
2. [Definir uma política usando OMA-URI personalizado no Intune](#set-a-policy-using-custom-oma-uri-in-intune)

> [!IMPORTANT]
> Como prática recomendada, não use um perfil OMA-URI personalizado e um perfil de modelos de Administração para definir a mesma configuração do Microsoft Edge no Intune. Se você implantar a mesma política usando um perfil OMA-URI e um perfil de modelo Administrativo personalizados, mas com valores diferentes, os usuários obterão resultados imprevisíveis. É altamente recomendável remover seu perfil OMA-URI antes de usar um perfil de modelos de Administração.

### <a name="ingest-the-microsoft-edge-admx-file-into-intune"></a>Ingerir o arquivo ADMX do Microsoft Edge no Intune

Esta seção descreve como ingerir o modelo administrativo do Microsoft Edge (arquivo **msedge.admx**) no Intune.

> [!WARNING]
> Não modifique o arquivo ADMX antes de ingerir o arquivo.

Para ingerir o arquivo ADMX, siga estas etapas:

1. Baixe o arquivo de modelos de política do Microsoft Edge (MicrosoftEdgePolicyTemplates.cab) da [página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise) e extraia o conteúdo. O arquivo que você deseja ingerir é **msedge.admx**.
2. Entre no [portal do Microsoft Azure](https://portal.azure.com).
3. Selecione **Intune** em _Todos os Serviços_ ou procure Intune na caixa de pesquisa do portal.
4. Em _Microsoft Intune - Visão geral_, selecione **Configuração do dispositivo** | **Perfis**.
5. Na barra de comandos superior, selecione **+ Criar perfil**.

   ![Criar um perfil de dispositivo](./media/edge-cfg-with-mdm/configure-edge-mdm-intune-create-profile.png)

6. Forneça as seguintes informações de perfil:

   - **Nome**: insira um nome descritivo. Neste exemplo, "Configuração ingerida do ADMX do Microsoft Edge".
   - **Descrição**: insira uma descrição opcional para o perfil.
   - **Plataforma**: selecione "Windows 10 e posterior"
   - **Tipo de perfil**: selecione "Personalizado"

7. Em **Configurações Personalizadas de OMA-URI**, clique em **Adicionar** para adicionar uma ingestão de ADMX.

   ![Adicionar ingestão para OMA-URI](./media/edge-cfg-with-mdm/configure-edge-mdm-intune-create-profile-add-omauri.png)

8. Em **Adicionar Linha**, forneça as seguintes informações:

   - **Nome**: insira um nome descritivo. Neste exemplo, use "Ingestão de ADMX do Microsoft Edge".
   - **Descrição**: insira uma descrição opcional para a configuração.
   - **OMA-URI**: insira "*./Device/Vendor/MSFT/Policy/ConfigOperations/ADMXInstall/Edge/Policy/EdgeAdmx*"
   - **Tipo de dados**: selecione "String"
   - **Valor**: essa área de entrada aparece depois que você seleciona o **Tipo de dados**. Abra o arquivo msedge.admx do arquivo de modelos de política do Microsoft Edge que você extraiu na etapa 1. Copie **TODO o texto** do arquivo msedge.admx e cole-o na área de texto **Valor** mostrada na captura de tela a seguir.

        ![Adicionar uma ingestão de ADMX](./media/edge-cfg-with-mdm/configure-edge-intune-mdm-omauri-addrow-ingest.png)

   - Clique em **OK**.

9. Em **Configurações Personalizadas de OMA-URI**, clique em **OK**.
10. Em **Criar perfil**, clique em **Criar**. A próxima captura de tela mostra informações sobre o perfil recém-criado.

    ![Novas informações sobre o perfil do dispositivo ](./media/edge-cfg-with-mdm/configure-edge-mdm-intune-create-profile-done.png)

<!--
> [!NOTE]
> You can use the preceding steps to ingest the msedgeupate.admx policy template file.
-->
### <a name="set-a-policy-using-custom-oma-uri-in-intune"></a>Definir uma política usando OMA-URI personalizado no Intune

> [!NOTE]
> Antes de usar as etapas nesta seção, você deverá concluir as etapas descritas em [Ingerir o arquivo ADMX do Microsoft Edge no Intune](#ingest-the-microsoft-edge-admx-file-into-intune).

1. Entre no [portal do Microsoft Azure](https://portal.azure.com).
2. Selecione **Intune** em _Todos os Serviços_ ou procure Intune na caixa de pesquisa do portal.
3. Acesse **Intune**>**Configuração do dispositivo**>**Perfis**.
4. Selecione o perfil "Configuração ingerida do ADMX do Microsoft Edge" ou o nome usado para o perfil.
5. Para adicionar configurações de política do Microsoft Edge, você terá de abrir as **Configurações Personalizadas de OMA-URI**. Em **Gerenciar**, clique em **Propriedades** e clique em **Configurações**.

    ![Definir configurações de perfil](./media/edge-cfg-with-mdm/configure-edge-mdm-intune-add-policy-settings.png)

6. Em **Configurações Personalizadas de OMA-URI**, clique em **Adicionar**.

    ![Adicionar linha às configurações de OMA-URI](./media/edge-cfg-with-mdm/configure-edge-mdm-intune-add-policy-settings-add-row.png)

7. Em **Adicionar Linha**, forneça as seguintes informações:

   - **Nome**: insira um nome descritivo. Sugerimos o uso do nome de política que você deseja configurar. Neste exemplo, use "ShowHomeButton".
   - **Descrição** (opcional): insira uma descrição para a configuração.
   - **OMA-URI**: insira o OMA-URI para a política. Usando a política "ShowHomeButton" como um exemplo, utilize esta cadeia de caracteres: "*./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~Startup/ShowHomeButton*"
   - **Tipo de dados**: selecione o tipo de dados de configurações de política. Para a política "ShowHomeButton", use "String"
   - **Valor**: insira a configuração que você deseja configurar para a política. No exemplo de "ShowHomeButton", insira "\<enabled/>". A captura de tela a seguir mostra as definições para a configuração de uma política.

        ![Adicionar Linha, Configurações Personalizadas de OMA-URI](./media/edge-cfg-with-mdm/configure-edge-mdm-custom-omauri-setting.png)

   - Clique em **OK**.

8. Em **Configurações Personalizadas de OMA-URI**, clique em **OK**.
9. No perfil "**Configuração ingerida do ADMX do Microsoft Edge - Propriedades**" (ou o nome que você usou), clique em **Salvar**.

Depois que o perfil for criado e as propriedades definidas, você precisará [atribuir o perfil ao Microsoft Intune](/intune/configuration/device-profile-assign).

#### <a name="confirm-that-the-policy-was-set"></a>Confirmar se a política foi definida

Siga as etapas a seguir para confirmar se a política do Microsoft Edge está usando o perfil que você criou. (Dê ao Microsoft Intune tempo para propagar a política para um dispositivo atribuído no exemplo de perfil "Configuração ingerida do ADMX do Microsoft Edge").

1. Abra o Microsoft Edge e acesse *edge://policy*.
2. Na página **Políticas**, veja se a política definida no perfil está listada.
3. Se sua política não for mostrada, consulte [Diagnosticar falhas de MDM no Windows 10](/windows/client-management/mdm/diagnose-mdm-failures-in-windows-10) ou [Solucionar problemas de uma configuração de política](#troubleshoot-a-policy-setting).

#### <a name="troubleshoot-a-policy-setting"></a>Solucionar problemas de uma configuração de política

Se uma política do Microsoft Edge não estiver entrando em vigor, tente as seguintes etapas:

Abra a página *edge://policy* no dispositivo de destino (um dispositivo ao qual você atribuiu o perfil no Microsoft Intune) e procure pela política. Se a política não estiver na página *edge://policy*, tente o seguinte:

- Verifique se a política está no Registro e se está correta. No dispositivo de destino, abra o Editor do Registro do Windows 10 (**tecla Windows + r**, insira “*regedit*” e então pressione **Enter**). Verifique se a política está corretamente definida no caminho *\Software\Policies\ Microsoft\Edge*. Se você não encontrar a política no caminho esperado, a política não foi enviada por push corretamente para o dispositivo.
- Verifique se o caminho OMA-URI está correto e se o valor é uma cadeia de caracteres XML válida. Se qualquer um deles estiver incorreto, a política não será enviada por push para o dispositivo de destino.

Para obter mais dicas sobre a solução de problemas, consulte [Configurar o Microsoft Intune](/intune/fundamentals/setup-steps) e [Sincronizar dispositivos](/intune/remote-actions/device-sync).

## <a name="see-also"></a>Consulte também

- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Definir as configurações de política do Microsoft Edge com o Microsoft Intune](configure-edge-with-intune.md)
- [Gerenciamento de dispositivos móveis](/windows/client-management/mdm/)
- [Usar configurações personalizadas para dispositivos Windows 10 no Intune](/intune/configuration/custom-settings-windows-10)
- [Configuração de política de aplicativo Win32 e Ponte de Desktop](/windows/client-management/mdm/win32-and-centennial-app-policy-configuration)
- [Noções básicas sobre políticas baseadas em ADMX](/windows/client-management/mdm/understanding-admx-backed-policies)