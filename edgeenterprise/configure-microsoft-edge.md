---
title: Configurar o Microsoft Edge para Windows
ms.author: brianalt
author: kelleyvice-msft
manager: laurawi
ms.date: 06/28/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Definir configurações de política do Microsoft Edge em dispositivos Windows
ms.openlocfilehash: a962a42c8dc40589c9275625007827ec2f76450002115a0c6d8c9e2d733df2e8
ms.sourcegitcommit: d44c0997ffe40d67421312ed96e7766da947eaa0
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/05/2021
ms.locfileid: "11725234"
---
# <a name="configure-microsoft-edge-policy-settings-on-windows"></a>Definir configurações de política do Microsoft Edge no Windows

Use as informações a seguir para definir as configurações de política do Microsoft Edge em seus dispositivos Windows.

> [!NOTE]
> Este artigo aplica-se ao Microsoft Edge versão 77 ou posterior.

## <a name="configure-policy-settings-on-windows"></a>Definir configurações de política no Windows

Você pode usar _objetos de política de grupo ( GPO)_ para definir as configurações de política para o Microsoft Edge e atualizações gerenciadas do Microsoft Edge em todas as versões do Windows. Você também pode provisionar a política por meio do Registro para dispositivos Windows que fazem parte de um domínio do Microsoft Active Directory ou instâncias do Windows 10 Pro ou do Enterprise inscritas no gerenciamento de dispositivos no Microsoft Intune. Para configurar o Microsoft Edge com objetos de política de grupo, você instala os _modelos administrativos_ que adicionam regras e configurações para o Microsoft Edge ao Repositório Central de políticas de grupo no domínio do Active Directory ou à pasta do modelo Definição de Política em computadores individuais e, em seguida, configura as políticas específicas que deseja definir.

Você pode usar a política de grupo do Active Directory para definir as configurações de política do Microsoft Edge se preferir gerenciar a política no nível do domínio. Isso permite que você gerencie as configurações de política globalmente, definindo configurações de política diferentes para UOs específicas ou usando filtros WMI para aplicar configurações somente a usuários ou computadores retornados por uma consulta específica. Para configurar a política em computadores individuais, você poderá aplicar configurações de política que afetam somente o dispositivo local usando o Editor de Política de Grupo Local no computador de destino.

O Microsoft Edge oferece suporte a políticas _obrigatórias_ e _recomendadas_. As políticas obrigatórias substituem as preferências do usuário e impedem que o usuário as alterem, enquanto a política recomendada fornece uma configuração padrão que pode ser substituída pelo usuário. A maioria das políticas só é obrigatória; um subconjunto é obrigatório e recomendado. Se ambas as versões de uma política forem definidas, a configuração obrigatória terá precedência. Uma política recomendada só entra em vigor quando o usuário não modifica a configuração.

>[!TIP]
> Você pode usar o Microsoft Intune para definir as configurações de política do Microsoft Edge. Para obter mais informações, consulte [Configurar o Microsoft Edge usando o Microsoft Intune](configure-edge-with-intune.md).

Há dois modelos administrativos para o Microsoft Edge, que podem ser aplicados no nível do computador ou do domínio do Active Directory:

- *msedge.admx* para [definir as configurações do Microsoft Edge](microsoft-edge-policies.md)
- *msedgeupdate. admx* para [gerenciar atualizações do Microsoft Edge](microsoft-edge-update-policies.md).

Para começar, baixe e instale o modelo administrativo do Microsoft Edge.

### <a name="1-download-and-install-the-microsoft-edge-administrative-template"></a>1. Baixar e instalar o modelo administrativo do Microsoft Edge

Se você quiser definir as configurações de política do Microsoft Edge no Active Directory, baixe os arquivos em um local de rede que você possa acessar de um controlador de domínio ou de uma estação de trabalho com o RSAT (Ferramentas de Administração de Servidor Remoto) instalado. Para configurar em um computador individual, bastará baixar os arquivos para esse computador.

Quando você adiciona os arquivos de modelo administrativo ao local adequado, as configurações de política do Microsoft Edge ficam imediatamente disponíveis no Editor de Política de Grupo.

Acesse a [página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise) para baixar o arquivo de modelos de política do Microsoft Edge(*MicrosoftEdgePolicyTemplates.cab*) e extrair o conteúdo.

#### <a name="add-the-administrative-template-to-active-directory"></a>Adicionar o modelo administrativo ao Active Directory

1. Em um controlador de domínio ou uma estação de trabalho com o RSAT, navegue até a pasta **PolicyDefinition** (também conhecida como o _Repositório Central_) em qualquer controlador de domínio para seu domínio. Para versões mais antigas do Windows Server, talvez seja necessário criar a pasta PolicyDefinition. Para obter mais informações, consulte [Como criar e gerenciar o Repositório Central para Modelos Administrativos de Política de Grupo no Windows](https://support.microsoft.com/help/3087759/how-to-create-and-manage-the-central-store-for-group-policy-administra).
2. Abra *MicrosoftEdgePolicyTemplates* e acesse **windows** > **admx**.
3. Copie o arquivo *msedge.admx* para a pasta PolicyDefinition. (Exemplo: %systemroot%\sysvol\domain\policies\PolicyDefinitions)
4. Na pasta *admx*, abra a pasta do idioma apropriado. Por exemplo, se você estiver nos EUA, abra a pasta **en-US**.
5. Copie o arquivo *msedge.adml* para a pasta do idioma correspondente na pasta PolicyDefinition. Crie a pasta se ela ainda não existir. (Exemplo: %systemroot%\sysvol\domain\policies\PolicyDefinitions\EN-US)
6. Se o domínio tiver mais de um controlador de domínio, os novos arquivos ADMX serão replicados para eles no próximo intervalo de replicação de domínio.
7. Para confirmar se os arquivos foram carregados corretamente, abra o **Editor de Gerenciamento de Política de Grupo** nas Ferramentas Administrativas do Windows e expanda **Configuração do Computador** > **Políticas** > **Modelos Administrativos** > **Microsoft Edge**. Você deve ver um ou mais nós do Microsoft Edge, como mostrado abaixo.

    ![Políticas do Microsoft Edge](./media/configure-microsoft-edge/edge-gpo-policies.png)

#### <a name="add-the-administrative-template-to-an-individual-computer"></a>Adicionar o modelo administrativo a um computador individual

1. No computador de destino, abra *MicrosoftEdgePolicyTemplates* e vá para **windows** > **admx**.
2. Copie o arquivo *msedge.admx* para sua pasta do modelo Definição de Política. (Exemplo: C:\Windows\PolicyDefinitions)
3. Na pasta *admx*, abra a pasta do idioma apropriado. Por exemplo, se você estiver nos EUA, abra a pasta **en-US**.
4. Copie o arquivo *msedge.adml* para a pasta do idioma correspondente na sua pasta Definição de Política. (Exemplo: C:\Windows\PolicyDefinitions\en-US)
5. Para confirmar se os arquivos foram carregados corretamente, abra o Editor de Política de Grupo Local diretamente (tecla Windows + R e digite gpedit.msc) ou abra o MMC e carregue o snap-in Editor de Política de Grupo Local. Se ocorrer um erro, isso geralmente significa que os arquivos estão em um local incorreto.

### <a name="2-set-mandatory-or-recommended-policies"></a>2. Definir políticas obrigatórias ou recomendadas

Você pode definir políticas obrigatórias ou recomendadas para configurar o Microsoft Edge com o Editor de Política de Grupo para o Active Directory e computadores individuais. Você pode criar um escopo para as configurações de política para **Configuração do Computador** ou **Configuração do Usuário** selecionando o nó apropriado conforme descrito a seguir.

- Para configurar uma política obrigatória, abra o Editor de Política de Grupo e vá para (**Configuração do Computador** ou **Configuração do Usuário**) > **Políticas** > **Modelos Administrativos** > **Microsoft Edge**.
- Para configurar uma política recomendada, abra o Editor de Política de Grupo e vá para (**Configuração do Computador** ou **Configuração do Usuário**) > **Políticas** > **Modelos Administrativos** > **Microsoft Edge – Configurações Padrão (os usuários podem substituir)**.

  ![Abrir o Editor de Política de Grupo](./media/configure-microsoft-edge/edge-ad-policy.png)

### <a name="3-test-your-policies"></a>3. Testar as políticas

Em um dispositivo cliente de destino, abra o Microsoft Edge e navegue até **edge://policy** para ver todas as políticas aplicadas. Se você tiver aplicado configurações de política no computador local, as políticas deverão aparecer imediatamente. Talvez seja necessário fechar e reabrir o Microsoft Edge se ele estava aberto enquanto você estava definindo as configurações de política.

![Exibir políticas configuradas no navegador](./media/configure-microsoft-edge/edge-gpEdit.png)

Para as configurações de política de grupo do Active Directory, as configurações de política são propagadas para os computadores do domínio a um intervalo regular definido pelo administrador do domínio, e talvez os computadores de destino não recebam as atualizações de política imediatamente. Para atualizar manualmente as configurações de política de grupo do Active Directory em um computador de destino, execute o seguinte comando em um prompt de comando ou em uma sessão do PowerShell no computador de destino:

``` powershell
gpupdate /force
```

Talvez seja necessário fechar e reabrir o Microsoft Edge antes que as novas políticas apareçam.

Você também pode usar REGEDIT.exe em um computador de destino para exibir as configurações do Registro que armazenam as configurações da política de grupo. Essas configurações estão localizadas no caminho do Registro **HKLM\SOFTWARE\Policies\Microsoft\Edge**.

## <a name="see-also"></a>Confira também

- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Configurar para o Windows com o Intune](configure-edge-with-intune.md)
- [Configurar para macOS](configure-microsoft-edge-on-mac.md)
- [Procurar políticas empresariais do Microsoft Edge](microsoft-edge-policies.md)


