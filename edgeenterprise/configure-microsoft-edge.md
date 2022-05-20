---
title: Configurar o Microsoft Edge para Windows com configurações de política
ms.author: v-danwesley
author: dan-wesley
manager: collw
ms.date: 05/19/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Saiba como definir as configurações de política do Microsoft Edge em dispositivos Windows
ms.openlocfilehash: e50a1020972b76c5c10d1da9e02c0d50e0cb990f
ms.sourcegitcommit: b96e309e575b4bcb0d179645ed37dea544bfaeda
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/19/2022
ms.locfileid: "12520467"
---
# <a name="configure-microsoft-edge-policy-settings-on-windows-devices"></a>Definir configurações de política do Microsoft Edge em dispositivos Windows

Use este artigo como guia para definir as configurações de política do Microsoft Edge em dispositivos Windows. Se você ainda não configurou o Microsoft Edge, consulte o [guia de configuração do Microsoft Edge](https://go.microsoft.com/fwlink/?linkid=2187484).

> [!NOTE]
> Este artigo aplica-se ao Microsoft Edge versão 77 ou posterior.

## <a name="introduction-to-policy-settings-on-windows"></a>Introdução às configurações de políticas no Windows

Você pode usar *objetos de política de grupo ( GPO)* para definir as configurações de política para o Microsoft Edge e atualizações gerenciadas do Microsoft Edge em todas as versões do Windows. Você também pode configurar políticas por meio do registro para:

- Dispositivos Windows que ingressaram em um domínio do Microsoft Active Directory (AD)
- Instâncias do Windows 10 Pro ou Enterprise registradas para o gerenciamento de dispositivos no Microsoft Intune

Para configurar o Microsoft Edge com objetos de política de grupo, instale *modelos administrativos* que adicionam regras e configurações para o Microsoft Edge para a política de grupo do Repositório Central no seu domínio do Active Directory.  Alternativamente, adicione estas regras e configurações à pasta modelo de Definição de Políticas em computadores individuais e depois configure as políticas específicas que você deseja definir.

Você pode usar a política de grupo do Active Directory para definir as configurações de política do Microsoft Edge se preferir gerenciar a política no nível do domínio. Esta abordagem permite que você gerencie as configurações de políticas globalmente. Você pode direcionar configurações de políticas diferentes para UOs específicas ou usar filtros WMI para aplicar configurações apenas a usuários ou computadores retornados por uma consulta específica. Para configurar políticas em computadores individuais, você pode utilizar o Editor de Política de Grupo Local no computador de destino. Essa abordagem permite que você aplique configurações de política que afetam somente o dispositivo local.

O Microsoft Edge dá suporte a políticas *obrigatórias* e *recomendadas*. As políticas obrigatórias substituem as preferências do usuário e impedem que ele use a política. As políticas recomendadas fornecem uma configuração padrão que o usuário pode substituir. A maioria das políticas é obrigatória, mas existe um subconjunto que é obrigatório e recomendado. Se ambas as versões de uma política forem definidas, a configuração obrigatória terá precedência. Uma política recomendada só tem efeito quando o usuário não modificou a configuração.

>[!TIP]
> Você pode usar o Microsoft Intune para definir as configurações de política do Microsoft Edge. Para obter mais informações, consulte [Configurar o Microsoft Edge usando o Microsoft Intune](configure-edge-with-intune.md).

Há dois modelos administrativos para o Microsoft Edge, ambos podem ser aplicados com ferramentas comuns de gerenciamento de política de grupo, como o Editor de Política de Grupo Local para aplicativos em um computador individual ou o Console de Gerenciamento de Política de Grupo para redes de domínio do Microsoft Windows. Esses modelos são:

- *msedge.admx* para [definir as configurações do Microsoft Edge](./microsoft-edge-policies.md)
- *msedgeupdate.admx* para [gerenciar atualizações do Microsoft Edge](./microsoft-edge-update-policies.md)

As etapas a seguir descrevem como instalar, configurar e testar os modelos do Microsoft Edge.

## <a name="1-download-and-install-the-microsoft-edge-administrative-template"></a>1. Baixar e instalar o modelo administrativo do Microsoft Edge

Se você quiser definir as configurações de política do Microsoft Edge no Active Directory, baixe os arquivos em um local de rede que você possa acessar de um controlador de domínio ou de uma estação de trabalho com o RSAT (Ferramentas de Administração de Servidor Remoto) instalado. Para configurar em um computador individual, baixe os arquivos para esse computador.

Quando você adiciona os arquivos de modelo administrativo ao local adequado, as configurações de política do Microsoft Edge ficam imediatamente disponíveis no Editor de Política de Grupo.

Acesse a [página inicial do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise) para baixar o arquivo de modelos de política do Microsoft Edge e extrair o conteúdo.

### <a name="add-the-administrative-template-to-active-directory"></a>Adicionar o modelo administrativo ao Active Directory

1. Em um controlador de domínio ou estação de trabalho com RSAT, vá para a pasta **PolicyDefinition** (também conhecida como *Repositório Central*) em qualquer controlador de domínio do seu domínio. Para versões mais antigas do Windows Server, talvez seja necessário criar a pasta **PolicyDefinition**. Para obter mais informações, consulte [Como criar e gerenciar o Repositório Central para Modelos Administrativos de Política de Grupo no Windows](https://support.microsoft.com/help/3087759/how-to-create-and-manage-the-central-store-for-group-policy-administra).
2. Abra *MicrosoftEdgePolicyTemplates* e acesse **windows** > **admx**.
3. Copie o arquivo *msedge.admx* para a pasta PolicyDefinition. (Exemplo: %systemroot%\sysvol\domain\policies\PolicyDefinitions)
4. Na pasta *admx*, abra a pasta do idioma apropriado. Por exemplo, se você estiver nos EUA, abra a pasta **en-US**.
5. Copie o arquivo *msedge.adml* para a pasta do idioma correspondente na pasta PolicyDefinition. Crie a pasta caso ela ainda não exista. (Exemplo: %systemroot%\sysvol\domain\policies\PolicyDefinitions\EN-US)
6. Se o domínio tiver mais de um controlador de domínio, os novos arquivos ADMX serão replicados para eles no próximo intervalo de replicação de domínio.
7. Para confirmar se os arquivos foram carregados corretamente, abra o **Editor de Gerenciamento de Política de Grupo** nas Ferramentas Administrativas do Windows e expanda **Configuração do Computador** > **Políticas** > **Modelos Administrativos** > **Microsoft Edge**. Você deve ver um ou mais nós do Microsoft Edge, como mostrado abaixo.

    ![Políticas do Microsoft Edge](./media/configure-microsoft-edge/edge-gpo-policies.png)

### <a name="add-the-administrative-template-to-an-individual-computer"></a>Adicionar o modelo administrativo a um computador individual

1. No computador de destino, abra *MicrosoftEdgePolicyTemplates* e vá para **windows** > **admx**.
2. Copie o arquivo *msedge.admx* para sua pasta do modelo Definição de Política. (Exemplo: C:\Windows\PolicyDefinitions)
3. Na pasta *admx*, abra a pasta do idioma apropriado. Por exemplo, se você estiver nos EUA, abra a pasta **en-US**.
4. Copie o arquivo *msedge.adml* para a pasta do idioma correspondente na sua pasta Definição de Política. (Exemplo: C:\Windows\PolicyDefinitions\en-US)
5. Para confirmar se os arquivos foram carregados corretamente, abra o Editor de Políticas do Grupo Local diretamente (tecla Windows + R e digite gpedit.msc) ou abra o MMC e carregue o snap-in do Editor de Políticas do Grupo Local. Se ocorrer um erro, isso geralmente significa que os arquivos estão em um local incorreto.

## <a name="2-set-mandatory-or-recommended-policies"></a>2. Definir políticas obrigatórias ou recomendadas

Você pode definir políticas obrigatórias ou recomendadas para configurar o Microsoft Edge com o Editor de Política de Grupo para o Active Directory e computadores individuais. Você pode criar um escopo para as configurações de política para **Configuração do Computador** ou **Configuração do Usuário** selecionando o nó apropriado conforme descrito a seguir.

- Para configurar uma política obrigatória, abra o Editor de Política de Grupo e vá para (**Configuração do Computador** ou **Configuração do Usuário**) > **Políticas** > **Modelos Administrativos** > **Microsoft Edge**.
- Para configurar uma política recomendada, abra o Editor de Política de Grupo e vá para (**Configuração do Computador** ou **Configuração do Usuário**) > **Políticas** > **Modelos Administrativos** > **Microsoft Edge – Configurações Padrão (os usuários podem substituir)**.

  ![Abrir o Editor de Política de Grupo](./media/configure-microsoft-edge/edge-ad-policy.png)

## <a name="3-test-your-policies"></a>3. Testar as políticas

Em um dispositivo cliente de destino, abra o Microsoft Edge e acesse **edge://policy** para ver todas as políticas aplicadas. Se você tiver aplicado configurações de política no computador local, as políticas deverão aparecer imediatamente. Talvez seja necessário fechar e reabrir o Microsoft Edge se ele estiver aberto enquanto você estiver configurando as configurações da política.

![Exibir políticas configuradas no navegador](./media/configure-microsoft-edge/edge-gpEdit.png)

Para configurações de políticas de grupo do Active Directory, as configurações de políticas são enviadas para computadores de domínio em um intervalo regular definido pelo administrador do domínio. Os computadores de destino podem não receber atualizações de política imediatamente. Se desejar atualizar manualmente as configurações da política de grupo do Active Directory Domain Services em um computador de destino, execute o seguinte comando por meio de um prompt de comando ou de uma sessão do PowerShell no computador de destino:

``` powershell
gpupdate /force
```

Talvez seja necessário fechar e reabrir o Microsoft Edge antes que as novas políticas apareçam.

Você também pode usar REGEDIT.exe em um computador de destino para exibir as configurações do Registro que armazenam as configurações da política de grupo. Estas configurações de política estão localizadas neste caminho do Registro: **HKLM\SOFTWARE\Policies\Microsoft\Edge**.

## <a name="see-also"></a>Consulte também

- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Configurar para o Windows com o Intune](configure-edge-with-intune.md)
- [Configurar para macOS](configure-microsoft-edge-on-mac.md)
- [Procurar políticas empresariais do Microsoft Edge](microsoft-edge-policies.md)


