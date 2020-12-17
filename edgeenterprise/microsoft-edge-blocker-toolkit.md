---
title: Blocker Toolkit para desabilitar a entrega automática do Microsoft Edge
ms.author: kvice
author: dan-wesley
manager: srugh
ms.date: 12/16/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Blocker Toolkit para desabilitar a entrega automática do Microsoft Edge
ms.openlocfilehash: 9fb97d2dfec4822f8ce76dc3e37b85118c6572ad
ms.sourcegitcommit: 606282995b466a968bab40c16005a6653323c763
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/16/2020
ms.locfileid: "11229612"
---
# Blocker Toolkit para desabilitar a entrega automática do Microsoft Edge (baseado no Chromium)

Este artigo descreve o Blocker Toolkit para desabilitar a entrega automática e a instalação do Microsoft Edge.

As seguintes atualizações foram feitas neste artigo:

- **01/09/2020** com mais informações sobre dispositivos que podem exigir o uso do kit de ferramentas do Bloqueador
- **28/02/2020** para remover "MDM gerenciado" dos critérios de dispositivos a serem excluídos desta atualização automática
- **30/06/2020**para refletir que todos os dispositivos conectados do Windows Update estão no escopo para receber esta atualização (em vigor não antes de 30/07/2020)
- **10/12/2020** para explicar as situações pré-20H2 nas quais as configurações do Kit de ferramentas do Bloqueador serão ignoradas

> [!NOTE]
> Isso se aplica ao canal estável do Microsoft Edge.

## Visão geral

Para ajudar nossos clientes a se tornarem mais seguros e atualizados, a Microsoft distribuirá o Microsoft Edge (Chromium) para dispositivos conectados ao Windows Update executando Windows 10 versão 1803 e posterior. Esse processo será iniciado após 15 de janeiro de 2020, e mais informações estarão disponíveis nessa data.

O Blocker Toolkit destina-se a organizações que desejam bloquear a entrega automática do Microsoft Edge (baseado no Chromium) em dispositivos conectados ao Windows Update que executam o Windows 10 versão 1803 e posterior. Os dispositivos gerenciados pelo Windows Server Update Services (WSUS) ou Windows Update para Empresas (WUfB) serão excluídos deste Windows Update automático, mas podem receber o novo Microsoft Edge (baseado no Chromium) por meio de sua organização.

**É importante observar que:**

- O Blocker Toolkit não impede que os usuários instalem manualmente o Microsoft Edge (baseado no Chromium) do download pela Internet ou de mídias externas.
- As organizações com atualizações gerenciadas por meio do Windows Update para Empresas (WUfB) não receberão automaticamente essa atualização e não precisarão implantar o Blocker Toolkit.
- As organizações com ambientes gerenciados com uma solução de gerenciamento de atualizações, como o Windows Server Update Services (WSUS) ou o System Center Configuration Manager (SCCM, não precisam implantar o Blocker Toolkit. Eles podem usar esses produtos para gerenciar totalmente a implantação de atualizações lançadas por meio do Windows Update e do Microsoft Update, incluindo a [Atualização no WSUS para o novo Microsoft Edge](https://support.microsoft.com/help/4584642/update-in-wsus-for-the-new-microsoft-edge), em seu ambiente.
- Esta atualização é uma atualização autônoma (não faz parte da atualização cumulativa mensal) para proporcionar flexibilidade aos clientes corporativos e controle máximo sobre a implantação dessa atualização.
- O novo Microsoft Edge (baseado em Chromium) está incluído como parte da atualização de recursos do Windows 10, versão 20H2 no segundo semestre de 2020. O kit de ferramentas Bloqueador não afeta o comportamento ou a implantação da versão 20H2. Confira mais informações sobre o Windows 10, versão 20H2 [aqui](https://blogs.windows.com/windowsexperience/2020/06/16/whats-next-for-windows-10-updates/).

Você pode baixar o arquivo executável do Blocker Toolkit em [https://msedgeblockertoolkit.blob.core.windows.net/blockertoolkit/MicrosoftEdgeChromiumBlockerToolkit.exe](https://msedgeblockertoolkit.blob.core.windows.net/blockertoolkit/MicrosoftEdgeChromiumBlockerToolkit.exe).

### Componentes do kit de ferramentas

Este kit de ferramentas contém os seguintes componentes:

- Script do bloqueador de executáveis (.CMD)
- Modelo Administrativo da Política de Grupo (.ADMX e .ADML)

### Sistemas operacionais com suporte

Windows 10 versão 1803 e mais recente.

## Script do bloqueador

O script cria uma chave do Registro e define o valor associado para bloquear ou desbloquear (dependendo da opção de linha de comando usada) a entrega automática do Microsoft Edge (baseado no Chromium) no computador local ou em um computador de destino remoto.

**Chave do Registro:** `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\EdgeUpdate`<br>
**Nome do valor da chave:** `DoNotUpdateToEdgeWithChromium`

| Valor                | Resultado                         |
|----------------------|--------------------------------|
| *A chave não está definida* | A distribuição *não* está bloqueada. |
| 0                    | A distribuição *não* está bloqueada. |
| 1                    | A distribuição está bloqueada.       |

O script tem a seguinte sintaxe de linha de comando:<br>
`EdgeChromium_Blocker.cmd [<machine name>] [/B] [/U] [/H]`

### Nome do computador

O parâmetro `<machine name>` é opcional. Se não for especificado, a ação será executada no computador local. Caso contrário, o computador remoto é acessado por meio das funcionalidades de registro remoto do comando `REG`. Se o registro remoto não puder ser acessado devido a permissões de segurança ou o computador local não for encontrado, uma mensagem de erro será retornada do comando `REG`.

### Opções

As opções usadas pelo script são mutuamente exclusivas e somente a primeira opção válida de um determinado comando é acionada. O script pode ser executado várias vezes no mesmo computador.

| Opção       | Descrição                              |
|--------------|------------------------------------------|
| `/B`         | Bloqueia a distribuição                      |
| `/U`         | Desbloqueia a distribuição                    |
| `/H` ou `/?` | Exibe a seguinte ajuda resumida:<br>`This tool can be used to remotely block or unblock the delivery of Microsoft Edge (Chromium-based) through Automatic Updates.`<br> `Usage:`<br>`EdgeChromium_Blocker.cmd [<machine name>] [/B][/U][/H]`<br>`B = Block Microsoft Edge (Chromium-based) deployment`<br>`U = Allow Microsoft Edge (Chromium-based) deployment`<br>`H = Help`<br>`Examples:`<br>`EdgeChromium_Blocker.cmd mymachine /B (blocks delivery on machine "mymachine")`<br>`EdgeChromium_Blocker.cmd /U (unblocks delivery on the local machine)`<br> |

## Modelo Administrativo da Política de Grupo (arquivos .ADMX e .ADML)

O Modelo Administrativo da Política de Grupo (arquivos .ADMX e .ADML) permite que os administradores importem as novas configurações de Política de Grupo para bloquear ou desbloquear a entrega automática do Microsoft Edge (baseado no Chromium) em seu ambiente de Política de Grupo e usar a Política de Grupo para executar a ação centralmente entre os sistemas em seu ambiente.

Os usuários que executam o Windows 10 RS3 Enterprise/EDU e RS4 e versões mais recentes verão a política no seguinte caminho:

```
/Computer Configuration  
  /Administrative Templates
    /Classic Administrative Templates
      /Windows Components
        /Windows Update  
          /Microsoft Edge (Chromium-based) Blockers  
```

Essa configuração está disponível somente como uma configuração de computador. Não há configuração do usuário.

> [!IMPORTANT]
> Essa configuração do Registro não é armazenada em uma chave de políticas e é considerada uma *preferência*. Portanto, se o Objeto de Política de Grupo que implementa a configuração for removido ou a política for definida como **Não Configurada**, a configuração permanecerá. Para desbloquear a distribuição do Microsoft Edge (baseado no Chromium) usando a Política de Grupo, defina a política como **Desabilitada**.

## Consulte também

- [Página de aterrissagem do Microsoft Edge Enterprise](https://www.microsoftedgeinsider.com/enterprise)
- [Atualizações do Windows para dar suporte ao Microsoft Edge](https://docs.microsoft.com/deployedge/microsoft-edge-sysupdate-windows-updates)
- [Como acessar a versão antiga do Microsoft Edge](https://docs.microsoft.com/deployedge/microsoft-edge-sysupdate-access-old-edge)
