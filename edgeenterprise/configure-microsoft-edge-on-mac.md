---
title: Configurar o Microsoft Edge para macOS usando um. plist
ms.author: brianalt
author: kelleyvice-msft
manager: laurawi
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Definir as configurações de política do Microsoft Edge no macOS usando .plist
ms.openlocfilehash: df8a51869665416ae7babe24fb7419ccaf723af6b8ca0381065d97b3728a4d87
ms.sourcegitcommit: d44c0997ffe40d67421312ed96e7766da947eaa0
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/05/2021
ms.locfileid: "11725274"
---
# <a name="configure-microsoft-edge-policy-settings-for-macos-using-a-plist"></a>Definir as configurações de política do Microsoft Edge no macOS usando .plist

Este artigo descreve como configurar o Microsoft Edge no macOS usando um arquivo de lista de propriedades (.plist). Você aprenderá a criar esse arquivo e a implementá-lo no Microsoft Intune.

Para obter mais informações, consulte [About Information Property List Files](https://developer.apple.com/library/archive/documentation/General/Reference/InfoPlistKeyReference/Articles/AboutInformationPropertyListFiles.html) (site da Apple) e [Ajustes personalizados de payload](https://support.apple.com/guide/mdm/custom-mdm9abbdbe7/1/web/1).

> [!NOTE]
> Este artigo aplica-se ao Microsoft Edge versão 77 ou posterior.

## <a name="configure-microsoft-edge-policies-on-macos"></a>Configurar políticas do Microsoft Edge no macOS

A primeira etapa é criar seu plist. Você pode criar o arquivo plist com qualquer editor de texto ou pode usar o [Terminal para criar o perfil de configuração](#create-a-configuration-profile-using-terminal). No entanto, é mais fácil criar e editar um arquivo plist usando uma ferramenta que formate o código XML para você. O *Xcode* é um ambiente de desenvolvimento integrado gratuito que você pode obter de um dos seguintes locais:

- [Site para desenvolvedores da Apple](https://developer.apple.com/xcode/)
- [Mac App Store](https://apps.apple.com/app/xcode/id497799835?mt=12)

Para obter uma lista de políticas com suporte e seus nomes de teclas de preferência, consulte [Referência de políticas do navegador Microsoft Edge](microsoft-edge-policies.md). No arquivo de modelos de política, que pode ser baixado da [página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise), há um plist de exemplo (*itadminexample.plist*) na pasta **examples**. O arquivo de exemplo contém todos os tipos de dados com suporte que você pode personalizar para definir suas configurações de política. 

A próxima etapa depois que você criar o conteúdo de seu plist é nomeá-lo usando o domínio de preferência do Microsoft Edge, *com.microsoft.Edge*. O nome diferencia maiúsculas de minúsculas e não deve incluir o canal de destino, pois ele se aplica a todos os canais do Microsoft Edge. O nome do arquivo plist deve ser **_com.microsoft.Edge.plist_**.

> [!IMPORTANT]
> A partir do build 78.0.249.2, todos os canais do Microsoft Edge no macOS serão lidos no domínio de preferência **com.microsoft.Edge**. Todas as versões anteriores são lidas em um domínio específico de canal, como **com.microsoft.Edge.Dev** para o canal de desenvolvimento.

A última etapa é implantar o plist nos dispositivos Mac dos seus usuários utilizando seu provedor MDM preferencial, como o Microsoft Intune. Para obter instruções, consulte [Implantar seu plist](#deploy-your-plist).

### <a name="create-a-configuration-profile-using-terminal"></a>Criar um perfil de configuração usando o Terminal

1. No Terminal, use o seguinte comando para criar um plist para o Microsoft Edge em sua área de trabalho com suas configurações preferidas:

   ```cmd
   /usr/bin/defaults write ~/Desktop/com.microsoft.Edge.plist RestoreOnStartup -int 1
   ```

2. Converta o plist de binários em formato de texto simples:

   ```cmd
   /usr/bin/plutil -convert xml1 ~/Desktop/com.microsoft.Edge.plist
   ```

Depois de converter o arquivo, verifique se os dados da política estão corretos e se contêm as configurações desejadas para o perfil de configuração.

> [!NOTE]
> Somente pares chave devem estar no conteúdo do arquivo plist ou xml. Antes de carregar o seu ficheiro no Intune, remova todos os \<plist> e \<dict> valores, assim como os cabeçalhos xml do seu ficheiro. O arquivo deve conter apenas pares de chave/valor.

## <a name="deploy-your-plist"></a>Implantar seu plist

Para o Microsoft Intune crie um novo perfil de configuração de dispositivo voltado para a plataforma do macOS e selecione o tipo de perfil *Arquivo de preferência*. Direcione **com.microsoft.Edge** como o nome de domínio de preferência e carregue seu plist. Para obter mais informações, consulte [Adicionar um arquivo de lista de propriedades a dispositivos macOS usando o Microsoft Intune](/intune/configuration/preference-file-settings-macos).

Para o Jamf, carregue o arquivo .plist como uma carga *Configurações personalizadas*.

## <a name="see-also"></a>Confira também

- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Configurar para macOS com Jamf](configure-microsoft-edge-on-mac-jamf.md)
- [Configurar para o Windows](configure-microsoft-edge.md)
- [Configurar para o Windows com o Intune](configure-edge-with-intune.md)