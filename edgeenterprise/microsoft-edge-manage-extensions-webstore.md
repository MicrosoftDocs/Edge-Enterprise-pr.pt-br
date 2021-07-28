---
title: Extensões de auto-hospedagem do Microsoft Edge
ms.author: aspoddar
author: AndreaLBarr
manager: balajek
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Saiba como empacotar e hospedar extensões do Microsoft Edge na empresa.
ms.openlocfilehash: 8b0e9ed346848f7ee9330c51f6a1c9274df89371
ms.sourcegitcommit: 9088e839e82d80c72460586e9af0610c6ca71b83
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/23/2021
ms.locfileid: "11676108"
---
# <a name="self-host-microsoft-edge-extensions"></a>Extensões de auto-hospedagem do Microsoft Edge

Este artigo fornece orientações básicas para empacotar uma extensão para hospedar em sua própria loja na web. Ele também inclui instruções sobre como implantar extensões em dispositivos e usuários em sua organização.

## <a name="prerequisites"></a>Pré-requisitos

Para auto-hospedar suas próprias extensões, você precisará fornecer seus próprios serviços de hospedagem da Web para as extensões e seus arquivos de manifesto.

 As etapas a seguir pressupõem que você já criou sua extensão, tem alguma experiência com arquivos XML, um conhecimento prático sobre a configuração da política de grupo e saiba como usar o registro do Windows.

## <a name="publish-an-extension"></a>Publicar uma extensão

Antes de publicar uma extensão, ela precisa ser empacotada em um arquivo CRX (extensão do Chrome). Use as etapas a seguir como um guia para empacotar uma extensão como um arquivo CRX.

1. Na barra de endereços do Microsoft Edge, vá para *edge://extensions* e ative o **Modo desenvolvedor** se ele ainda não estiver habilitado.
2. Em **Extensões instaladas,** clique em **Extensão de Pacote** para criar o arquivo CRX.
3. Use a **Extensão de pacote** para encontrar o diretório que tem a origem da extensão. Selecione o diretório e clique em **Extensão de pacote**.  Isso criará seu arquivo CRX, juntamente com um arquivo PEM. Salve o arquivo PEM porque ele é necessário para fazer atualizações de versão para a extensão. A próxima captura de tela mostra a caixa de diálogo da **Extensão do pacote** para localizar o diretório raiz da extensão.

   :::image type="content" source="media/microsoft-edge-manage-extensions-webstore/manage-extensions-pack-dialog.png" alt-text="Caixa de diálogo da extensão de pacote para localizar o código-fonte de uma extensão.":::

   > [!IMPORTANT]
   > Armazene o arquivo PEM em um local seguro porque ele é a chave para a extensão e é necessário para atualizações futuras.

4. Arraste o arquivo CRX para a janela de extensões e certifique-se de que ele seja carregado.
5. Teste a extensão e anote o campo ID (esta é a ID CRX) e o número da versão. Você precisará das informações mais tarde. A próxima captura de tela mostra uma extensão de teste com sua ID CRX.

   :::image type="content" source="media/microsoft-edge-manage-extensions-webstore/manage-extensions-test-extension.png" alt-text="Exemplo de extensão mostrando a ID CRX":::

6. Upload o arquivo CRX para o host e observe a URL do local de onde ele será baixado. Essas informações são necessárias para o arquivo de manifesto XML.
7. Para criar um arquivo XML de manifesto com a ID do aplicativo/extensão, baixe a URL e a versão, defina os seguintes campos:  

   - **appid** - A ID da extensão da etapa 5
   - **codebase** - O local de download do arquivo CRX da etapa 6
   - **versão** - A versão do aplicativo/extensão, que deve corresponder à versão especificada no manifesto da extensão.

   O próximo trecho de código mostra um exemplo de um arquivo de manifesto XML.

   ```xml
   <?xml version='1.0' encoding='UTF-8'?> 
   <gupdate xmlns='http://www.google.com/update2/response' protocol='2.0'> 
     <app appid='ekilpdeokbpjmminmhfcgkncmmohmfeb'> 
     <updatecheck codebase='https://app.somecompany.com/extensionfolder/helloworld.crx' version='1.0' /> 
     </app> 
   </gupdate> 
   ```

   Para obter mais informações, consulte [Extensões de atualização automática no Microsoft Edge - Desenvolvimento do Microsoft Edge](/microsoft-edge/extensions-chromium/enterprise/auto-update).

8. Upload o arquivo XML concluído para um local de onde ele possa ser baixado, anotando a URL. Essa URL será necessária ao instalar a extensão usando uma política de grupo. Consulte [Distribuir uma extensão hospedada privadamente.](#distribute-a-privately-hosted-extension)

   > [!IMPORTANT]
   > O local de hospedagem da extensão não precisa de autenticação. Ele precisa estar acessível por dispositivos de usuário onde quer que possam ser usados.

## <a name="publish-updates-to-an-extension"></a>Publicar atualizações em uma extensão

Depois de alterar e testar a extensão atualizada, você pode publicá-la. Use as etapas a seguir como um guia para publicar uma atualização.

1. Altere o número de versão no seu arquivo de extensão manifest.JSON para um número mais alto usando a seguinte sintaxe: `"version":"versionString"`. Se a "versão":"1.0", você poderá atualizar para "versão":"1.1" ou qualquer número maior que "1.0".
2. Atualize a "versão" de `<updatecheck>` no arquivo XML para corresponder ao número que você colocou no arquivo de manifesto na etapa anterior. Por exemplo:<br>`<updatecheck codebase='https://app.somecompany.com/extensionfolder/helloworld.crx' version='1.1' />`
3. Crie um arquivo CRX que inclua as novas alterações. Vá para *edge://extensions* e habilite o **Modo desenvolvedor**.
4. Clique em **Pacote de extensão** e vá para o diretório para a fonte de extensão.

   > [!IMPORTANT]
   > Use o mesmo arquivo PEM que foi gerado e salvo na primeira vez que o arquivo CRX foi criado. Se você não usar o mesmo arquivo PEM, a ID do aplicativo da extensão será mudada e a atualização será tratada como uma nova extensão.

5. Arraste e solte o arquivo CRX na janela de extensões e verifique se ele é carregado. A extensão será desabilitada após essa operação. Para habilita-lo, adicione a ID CRX da extensão à política ExtensionInstallAllowList. 
6. Teste a extensão atualizada.
7. Substitua o arquivo CRX antigo e o arquivo XML pelos novos arquivos para a extensão atualizada.

As alterações da extensão serão escolhidas durante o próximo ciclo de sincronização de política. Para obter mais informações sobre a atualização de extensões, consulte: [Atualizar URL](/microsoft-edge/extensions-chromium/enterprise/auto-update#update-url) e [Atualizar manifesto](/microsoft-edge/extensions-chromium/enterprise/auto-update#updated-manifest).

## <a name="distribute-a-privately-hosted-extension"></a>Distribuir uma extensão hospedada privadamente

Você pode compartilhar o link do local onde o arquivo CRX está hospedado e, assim que os usuários inserirem a URL em seu navegador, a extensão será baixada e instalada. Os usuários podem habilitar a extensão da página edge://extensions. Para permitir que os usuários instalem extensões auto-hospedadas, você precisa adicionar as IDs CRX de extensão à política [ExtensionInstallAllowList](/deployedge/microsoft-edge-policies#extensioninstallallowlist) e adicionar a URL do local onde o arquivo CRX está hospedado à política [ExtensionInstallSources.](/deployedge/microsoft-edge-policies#extensioninstallsources)

Como alternativa, você pode usar a política de grupo [ExtensionInstallForceList](/deployedge/microsoft-edge-manage-extensions-policies#force-install-an-extension) para forçar a instalação de uma extensão nos dispositivos de seus usuários.

Você pode aplicar essas políticas aos usuários e dispositivos selecionados ou ambos. Lembre-se de que as atualizações de política não são instantâneas e levará tempo para que as configurações de política entrem em vigor.

## <a name="see-also"></a>Veja também

- [Gerenciar extensões do Microsoft Edge na empresa](microsoft-edge-manage-extensions.md)
- [Usar políticas de grupo para gerenciar extensões do Microsoft Edge](microsoft-edge-manage-extensions-policies.md)
- [Guia detalhado da política ExtensionSettings](microsoft-edge-manage-extensions-ref-guide.md)
- [Perguntas frequentes sobre extensões do Microsoft Edge](microsoft-edge-manage-extensions-faq.md)
- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
