---
title: Criar variáveis de diretório de dados do usuário do Microsoft Edge
ms.author: brianalt
author: AndreaLBarr
manager: srugh
ms.date: 07/08/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Saiba como criar variáveis de diretório de dados do usuário do Microsoft Edge
ms.openlocfilehash: e314f23334390fa45efa58daefac0730d8b849732fde75aeacffe4a486c50762
ms.sourcegitcommit: d44c0997ffe40d67421312ed96e7766da947eaa0
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/05/2021
ms.locfileid: "11724264"
---
# <a name="create-microsoft-edge-user-data-directory-variables"></a>Criar variáveis de diretório de dados do usuário do Microsoft Edge

Este artigo explica como você pode usar as variáveis de diretório de dados em vez de usar caminhos embutido em código ao modificar o Microsoft Edge.

>[!NOTE]
>Este artigo se aplica ao Microsoft Edge versão 77 ou posterior.
## <a name="path-variables"></a>Variáveis de caminho

Políticas para modificar caminhos de diretório de dados (por exemplo, configurando as variáveis de suporte [UserDataDir](microsoft-edge-policies.md#userdatadir) ou [DownloadDirectory](microsoft-edge-policies.md#downloaddirectory). Ao configurar essas políticas, você pode usar variáveis em vez de caminhos embutidos no código. Por exemplo, para armazenar os dados de perfil em dados de aplicativo local do usuário no Windows, em vez do local padrão. Definir a política [UserDataDir](microsoft-edge-policies.md#userdatadir) como **${local_app_data}\Edge\Profile**. Na maioria das instalações de Windows 10, esse caminho resolve como *C:\Users\\&lt;Usuário atual&gt;\AppData\Local\Microsoft\Edge\Profile*.

>[!NOTE]
>Para exibir o **Caminho do perfil** atual, abra a página **Sobre a versão** (digite “edge://version”). O **Caminho do perfil** segue este formato: *C:\Users\\&lt;Usuário atual&gt;\AppData\Local\Microsoft\Edge\User Data\Default*.

### <a name="guidance-for-using-path-variables"></a>Diretrizes para usar variáveis de caminho

Examine as diretrizes a seguir antes de usar variáveis de caminho.

- Todas as políticas que envolvem caminhos em que Microsoft Edge armazena dados diferentes dependem da plataforma. Algumas dessas políticas estão disponíveis somente em plataformas específicas, mas outras podem ser usadas em todas as plataformas.
- Para evitar erros causados por aplicativos a partir de locais diferentes em ocasiões diferentes, verifique se os caminhos são absolutos.
- Cada variável só pode ocorrer uma vez em um caminho. Para a maioria deles, essa é a única maneira significativa de usar variáveis, pois elas são resolvidas como caminhos absolutos.
- Quase todas as políticas criarão o caminho se não existirem (se possível nas circunstâncias existentes).
- O uso de locais de rede para algumas políticas pode levar a resultados inesperados devido às diferenças em como diferentes versões/canais do Microsoft Edge tratam a estrutura de pastas.

### <a name="supported-path-variables"></a>Variáveis de caminho compatíveis

O Microsoft Edge dá suporte às variáveis de caminho a seguir.

#### <a name="all-platforms"></a>Todas as plataformas

| Variável | Descrição |
| --- | --- |
| **${user_name}** | O usuário que está usando o Microsoft Edge. O Microsoft Edge respeita as SUIDs (Definir ID de Usuário do proprietário na execução). Exemplo: *audreysmall* |
| **${machine_name}** | O nome do computador, possivelmente incluindo o nome do domínio. Exemplo: *audreysmall* ou *audrey.ex.contoso.com* |

#### <a name="windows-only"></a>Windows somente.

| Variável | Descrição |
| --- | --- |
| **${documents}** | A pasta Documentos do usuário atual. Exemplo: *C:\Users\Administrador\Documentos* |
|**${local_app_data}** | A pasta Dados de Aplicativos do usuário atual. Exemplo: *C:\Users\Administrador\AppData\Local* |
|**${roaming_app_data}** | A pasta Dados de Aplicativos em Roaming do usuário atual. Exemplo: *C:\Users\Administrador\AppData\Roaming* |
| **${profile}** | A pasta base do usuário atual. Exemplo: *C:\Users\Administrador* |
| **${global_app_data}** | A pasta de Dados de Aplicativos de todo o sistema. Exemplo: *C:\AppData* |
| **${program_files}** | A pasta Arquivos de Programa do processo atual. Essa pasta depende se é um processo de 32 bits ou de 64 bits. Resolução de exemplo: *C:\Arquivos de programas (x86)* |
| **${windows}** | A pasta Windows. Exemplo: *C:\Windows* |
| **${client_name}** | O nome do computador cliente conectado a uma sessão RDP ou Citrix. Essa variável estará vazia se for usada em uma sessão local. Se ela for usada em um caminho, coloque um prefixo para garantir que não fique em branco. Exemplo: *C:\edge_profiles\session_${client_name}* resolve como *C:\edge_profiles\session_&lt;ForlocalSessions&gt;* e *C:\edge_profiles\session_&lt;SomePCname&gt;* para sessões remotas. |
| **${session_name}** | O nome da sessão ativa. Use esse nome para diferenciar várias sessões remotas conectadas simultaneamente que estejam usando um único perfil de usuário. Exemplo: *WinSta0 para sessões de área de trabalho local* |

#### <a name="macos-only"></a>Somente MacOS

| Variável | Descrição |
| --- | --- |
| **${users}** | A pasta onde os perfis dos usuários são armazenados. Exemplo: */Users* |
| **${documents}** | A pasta Documentos do usuário atual. Exemplo: */Users/audreysmall/Documentos* |

## <a name="content-license"></a>Licença de conteúdo

>[!NOTE]
>Partes dessa página são modificações baseadas no trabalho criado e compartilhado por Chromium.org e usadas de acordo com os termos descritos na [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons](http://creativecommons.org/licenses/by/4.0/). A página original pode ser encontrada [aqui](https://www.chromium.org/administrators/policy-list-3/user-data-directory-variables).
  
<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br/>Esse trabalho é licenciado sob uma <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons</a>.
## <a name="see-also"></a>Consulte também

- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
