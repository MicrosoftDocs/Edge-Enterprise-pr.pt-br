---
title: Configure Microsoft Edge para macOS usando uma lista de propriedades.
ms.author: brianalt
author: kelleyvice-msft
manager: laurawi
ms.date: 12/14/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Saiba como configurar as configurações Microsoft Edge de política no macOS usando uma lista de propriedades que você pode implantar no Microsoft Intune.
ms.openlocfilehash: 4cb3d635c8fc108a3b81ec17175ce0e3d8fa287a
ms.sourcegitcommit: e7f3098d8b7d91cae20b5778a71a87daababc312
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/15/2022
ms.locfileid: "12297690"
---
# <a name="configure-microsoft-edge-policy-settings-for-macos-using-a-property-list"></a>Configurar Microsoft Edge de política para macOS usando uma lista de propriedades

Este artigo descreve como configurar o Microsoft Edge no macOS usando um arquivo de lista de propriedades (\.plist). Você aprenderá a criar esse arquivo e a implementá-lo no Microsoft Intune.

Para obter mais informações, consulte [About Information Property List Files](https://developer.apple.com/library/archive/documentation/General/Reference/InfoPlistKeyReference/Articles/AboutInformationPropertyListFiles.html) (site da Apple) e [Ajustes personalizados de payload](https://support.apple.com/guide/mdm/custom-mdm9abbdbe7/1/web/1).

> [!NOTE]
> Este artigo aplica-se ao Microsoft Edge versão 77 ou posterior.

## <a name="configure-microsoft-edge-policies-on-macos"></a>Configurar políticas do Microsoft Edge no macOS

A primeira etapa é criar seu plist. Você pode criar o arquivo plist com qualquer editor de texto. Outra opção é usar [Terminal para criar o perfil de configuração](#create-a-configuration-profile-using-terminal). No entanto, é mais fácil criar e editar um arquivo plist com uma ferramenta que formatar o código XML para você. *O Xcode* é um ambiente de desenvolvimento integrado gratuito que está disponível nos seguintes locais:

- [Site para desenvolvedores da Apple](https://developer.apple.com/xcode/)
- [Mac App Store](https://apps.apple.com/app/xcode/id497799835?mt=12)

Para obter uma lista de políticas com suporte e seus nomes de teclas de preferência, consulte [Referência de políticas do navegador Microsoft Edge](./microsoft-edge-policies.md). No arquivo de modelos de política, que pode ser baixado [da](https://aka.ms/EdgeEnterprise)página inicial do Microsoft Edge Enterprise , há um exemplo de plist (*itadminexample.plist*) na pasta de **exemplos.** Esse arquivo contém todos os tipos de dados com suporte que você pode personalizar para definir suas configurações de política.

Depois de criar o conteúdo da sua lista de plist, nomee a lista usando o domínio de Microsoft Edge de preferência, que é "*com.microsoft.Edge*". Esse nome é sensível a casos e não deve incluir o canal que você está direcionando porque se aplica a todos os Microsoft Edge canais. O nome do arquivo plist deve ser **_com.microsoft.Edge.plist_**.

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

Depois de converter o arquivo verifique se seus dados de política estão corretos e contiver as configurações, você deseja que seu perfil de configuração.

> [!NOTE]
> Somente pares chave devem estar no conteúdo do arquivo plist ou xml. Antes de carregar o seu ficheiro no Intune, remova todos os \<plist> e \<dict> valores, assim como os cabeçalhos xml do seu ficheiro. O arquivo deve conter apenas pares de chave/valor.

## <a name="deploy-your-plist"></a>Implantar seu plist

Usando Microsoft Intune, crie um novo perfil de configuração de dispositivo voltado para a plataforma macOS e selecione o *tipo de perfil de arquivo De* preferência. Direcione **com.microsoft.Edge** como o nome de domínio de preferência e carregue seu plist. Para obter mais informações, [consulte Adicionar um arquivo de lista de propriedades a dispositivos macOS usando Microsoft Intune](/intune/configuration/preference-file-settings-macos).

Para Jamf, carregue o arquivo \.plist como *uma carga Configurações* personalizado.

## <a name="see-also"></a>Consulte também

- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Configurar para macOS com Jamf](configure-microsoft-edge-on-mac-jamf.md)
- [Configurar para o Windows](configure-microsoft-edge.md)
- [Configurar para o Windows com o Intune](configure-edge-with-intune.md)