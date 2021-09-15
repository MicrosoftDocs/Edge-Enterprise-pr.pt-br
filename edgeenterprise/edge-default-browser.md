---
title: Definir o Microsoft Edge como o navegador padrão no Windows e macOS
ms.author: brianalt
author: dan-wesley
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Saiba como definir o Microsoft Edge como o navegador padrão.
ms.openlocfilehash: 191d7835a0c4aacfc2fde409c57622ff5a351926
ms.sourcegitcommit: 8968f3107291935ed9adc84bba348d5f187eadae
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/12/2021
ms.locfileid: "11978641"
---
# <a name="set-microsoft-edge-as-the-default-browser"></a>Definir Microsoft Edge como o navegador padrão

Este artigo explica como você pode definir o Microsoft Edge como o navegador padrão no Windows e macOS.

> [!NOTE]
> Este artigo aplica-se ao Microsoft Edge versão 77 ou posteriores no Windows 8 e no Windows 10. Para o Windows 7 e o macOS, consulte a política [Definir o Microsoft Edge como navegador padrão](./microsoft-edge-policies.md#defaultbrowsersettingenabled).

## <a name="introduction"></a>Introdução

Você pode usar a Política de Grupo **Definir um arquivo de configuração de associações padrão** ou a configuração do Gerenciamento de Dispositivo Móvel [DefaultAssociationsConfiguration](/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration) para definir o Microsoft Edge como o navegador padrão da sua organização.

Para definir o Microsoft Edge Estável como o navegador padrão para arquivos html, links http/https e arquivos PDF, use o seguinte exemplo de arquivo de associação de aplicativo:

```xml
<?xml version="1.0" encoding="UTF-8"?>
<DefaultAssociations> 
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgeHTM" Identifier=".html"/>
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgeHTM" Identifier=".htm"/>
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgeHTM" Identifier="http"/>
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgeHTM" Identifier="https"/>  
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgePDF" Identifier=".pdf"/>
</DefaultAssociations>
```

> [!NOTE]
> Para definir o Microsoft Edge Beta como o navegador padrão, defina **ApplicationName** como "Microsoft Edge Beta" e **ProgId** como "MSEdgeBHTML". Para definir o Microsoft Edge Dev como o navegador padrão, defina **ApplicationName** como "Microsoft Edge Dev" e **ProgId** como "MSEdgeDHTML".


> [!NOTE]
> As associações de arquivos padrão não serão aplicadas se o Microsoft Edge não estiver instalado no dispositivo de destino. Neste cenário, os usuários deverão selecionar seu aplicativo padrão ao abrirem um link ou um arquivo htm/html.

## <a name="set-microsoft-edge-as-the-default-browser-on-domain-joined-devices"></a>Definir o Microsoft Edge como o navegador padrão em dispositivos ingressados no domínio

Você pode definir Microsoft Edge como o navegador padrão em dispositivos ingressados no domínio definindo a política de grupo **Definir um arquivo de configuração de associações padrão**. Ativar essa política de grupo requer que você crie e armazene um arquivo de configuração de associações padrão. Esse arquivo é armazenado localmente ou em um compartilhamento de rede. Para obter mais informações sobre como criar esse arquivo, consulte [Exportar ou importar associações de aplicativo padrão](/windows-hardware/manufacture/desktop/export-or-import-default-application-associations).

### <a name="to-configure-the-group-policy-for-a-default-file-type-and-protocol-associations-configuration-file"></a>Para configurar a política de grupo para um tipo de arquivo padrão e um arquivo de configuração de associações de protocolo:

1. Abra o editor de Política de Grupo e vá para **Configuração do Computador\Modelos Administrativos\Componentes do Windows\Explorador de Arquivos**.
2. Selecione **Definir um arquivo de configuração de associações padrão**.
3. Clique em **configuração de política** e em **Habilitado**.
4. Em **Opções:**, digite o local do arquivo de configuração de associações padrão.
5. Clique em **OK** para salvar as configurações da política.

O exemplo na próxima captura de tela mostra um arquivo de associações chamado *appassoc.xml* em um compartilhamento de rede que possa ser acessado do dispositivo de destino.

   ![Habilitar associação de arquivo na política de grupo](./media/edge-learnmore-make-edge-default-browser/edge-learnmore-app-associations.png)

   > [!NOTE]
   > Se essa configuração for habilitada e o dispositivo do usuário for ingressado em domínio, o arquivo de configuração de associações será processado na próxima vez que o usuário entrar.

## <a name="set-microsoft-edge-as-the-default-browser-on-azure-active-directory-joined-devices"></a>Defina o Microsoft Edge como o navegador padrão em dispositivos ingressados no Azure Active Directory

Para definir o Microsoft Edge Beta como o navegador padrão em dispositivos ingressados no Azure Active Directory, siga as etapas da configuração do Gerenciamento de Dispositivo Móvel [DefaultAssociationsConfiguration](/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration) usando o seguinte arquivo de associação de aplicativo como um exemplo.

```xml
<?xml version="1.0" encoding="UTF-8"?>
<DefaultAssociations>
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgeHTM" Identifier=".html"/>
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgeHTM" Identifier=".htm"/>
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgeHTM" Identifier="http"/>
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgeHTM" Identifier="https"/>  
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgePDF" Identifier=".pdf"/>
</DefaultAssociations>
```

> [!NOTE]
> Para definir o Microsoft Edge Beta como o navegador padrão, defina **ApplicationName** como "Microsoft Edge Beta" e **ProgId** como "MSEdgeBHTML". Para definir o Microsoft Edge Dev como o navegador padrão, defina **ApplicationName** como "Microsoft Edge Dev" e **ProgId** como "MSEdgeDHTML".

## <a name="set-microsoft-edge-as-the-default-browser-on-macos"></a>Definir o Microsoft Edge como o navegador padrão no macOS

A tentativa de definir o navegador padrão do macOS de forma programática faz com que um aviso apareça para o usuário final. Esse aviso é um recurso de segurança do macOS que só pode ser automatizado com o uso de um AppleScript.

Devido a essa limitação, há dois métodos principais para configurar Microsoft Edge como o navegador padrão no macOS. A primeira opção é atualizar o dispositivo com uma imagem do macOS em que o Microsoft Edge já foi definido como o navegador padrão. A outra opção é usar a política [Definir o Microsoft Edge como navegador padrão](./microsoft-edge-policies.md#defaultbrowsersettingenabled) , que solicita que o usuário defina o Microsoft Edge como navegador padrão.

Ao usar um desses métodos, ainda é possível que um usuário altere o navegador padrão. Isso ocorre porque, por motivos de segurança, a preferência de navegador padrão não pode ser bloqueada de forma programática. Por esse motivo, recomendamos que você implante a política **Definir o Microsoft Edge como navegador padrão** , mesmo que você crie uma imagem com o Microsoft Edge como navegador padrão. Se a política for definida e o usuário remover o Microsoft Edge como navegador padrão, da próxima vez que ele abrir o Microsoft Edge, ele será solicitado a defini-lo como o padrão.

## <a name="see-also"></a>Consulte também

- [Planejar sua implantação do Microsoft Edge](./deploy-edge-plan-deployment.md)
- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Definir o Microsoft Edge como navegador padrão (Windows 7 e macOS)](./microsoft-edge-policies.md#defaultbrowsersettingenabled)
- [Windows 10 – como configurar associações de arquivos para profissionais de TI?](/archive/blogs/windowsinternals/windows-10-how-to-configure-file-associations-for-it-pros)
- [Exportar ou importar associações de aplicativo padrão](/windows-hardware/manufacture/desktop/export-or-import-default-application-associations)
  - [Visão geral do DISM](/windows-hardware/manufacture/desktop/what-is-dism)
  - [DISM - Gerenciamento e Manutenção de Imagens de Implantação](/windows-hardware/manufacture/desktop/dism---deployment-image-servicing-and-management-technical-reference-for-windows)