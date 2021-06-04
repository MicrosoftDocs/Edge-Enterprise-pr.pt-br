---
title: Documentação da política do Microsoft Edge Update
ms.author: stmoody
author: brianalt-msft
manager: tahills
ms.date: 10/07/2020
audience: ITPro
ms.topic: reference
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
ms.custom: ''
description: Documentação para todas as políticas compatíveis com o Microsoft Edge Update
ms.openlocfilehash: feb7859f062ae39e2bbfe08d8e478386defb85cf
ms.sourcegitcommit: 4e6188ade942ca6fd599a4ce1c8e0d90d3d03399
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2020
ms.locfileid: "11105565"
---
# Microsoft Edge - Políticas de atualização
A versão mais recente do Microsoft Edge inclui as seguintes políticas que você pode usar para controlar como e quando o Microsoft Edge é atualizado.

Para obter informações sobre outras políticas disponíveis no Microsoft Edge, confira [Referência de política do navegador Microsoft Edge](microsoft-edge-policies.md)
> [!NOTE]
> Este artigo se aplica ao Microsoft Edge versão 77 ou posterior.
##  <a name="available-policies"></a>Políticas disponíveis
Estas tabelas listam todas as políticas de grupo relacionadas a atualizações disponíveis nesta versão do Microsoft Edge. Use os links na tabela a seguir para obter mais detalhes sobre políticas específicas.

|||
|-|-|
|[Aplicativos](#applications)|[Preferências](#preferences)|
|[Servidor proxy](#proxy-server)|[Microsoft Edge WebView](#microsoft-edge-webview)|

### [Aplicativos](#applications-policies)
|Nome da política|Legenda|
|-|-|
|[InstallDefault](#installdefault)|Permitir a instalação padrão|
|[UpdateDefault](#updatedefault)|Atualizar o padrão de substituição de política|
|[Install](#install)|Permitir a instalação (por canal)|
|[Update](#update)|Atualizar a substituição de política (por canal)|
|[Allowsxs](#allowsxs)|Permitir a experiência de navegador Lado a Lado do Microsoft Edge|
|[CreateDesktopShortcutDefault](#createdesktopshortcutdefault)|Impedir a criação de Atalho da Área de Trabalho com a instalação padrão|
|[CreateDesktopShortcut](#createdesktopshortcut)|Impedir a criação de Atalho da Área de Trabalho com a instalação (por canal)|
|[RollbackToTargetVersion](#rollbacktotargetversion)|Reverter para a Versão de Destino (por canal)|
|[TargetVersionPrefix](#targetversionprefix)|Substituir versão de destino (por canal)|

### [Preferências](#preferences-policies)
|Nome da política|Legenda|
|-|-|
|[AutoUpdateCheckPeriodMinutes](#autoupdatecheckperiodminutes)|Atualizar automaticamente a substituição do período de verificação|
|[UpdatesSuppressed](#updatessuppressed)|O período em cada dia para suprimir a verificação de atualização automática|

### [Servidor proxy](#proxy-server-policies)
|Nome da política|Legenda|
|-|-|
|[ProxyMode](#proxymode)|Escolher como especificar as configurações do servidor proxy|
|[ProxyPacUrl](#proxypacurl)|A URL para um arquivo .pac de proxy|
|[ProxyServer](#proxyserver)|Endereço ou URL do servidor proxy|

### [Microsoft Edge WebView](#microsoft-edge-webview-policies)
|Nome da política|Legenda|
|-|-|
|[Instalar](#install-webview)|Permitir instalação|
|[Atualização](#update-webview)|Atualizar a substituição de política|

##  <a name="applications-policies"></a>Políticas de aplicativos

[Voltar ao início](#microsoft-edge---update-policies)
###  <a name="installdefault"></a>InstallDefault
#### Permitir a instalação padrão
>Microsoft Edge Update 1.2.145.5 e posterior

#### Descrição
Você pode especificar o comportamento padrão de todos os canais para permitir ou bloquear o Microsoft Edge em dispositivos associados ao domínio.

Você pode substituir esta política para canais individuais habilitando a política '[Permitir instalação](#install)' para canais específicos.

Se você desabilitar esta política, a instalação do Microsoft Edge será bloqueada. Isso só afeta a instalação do software Microsoft Edge quando a '[Permitir instalação](#install)' está definida como Não configurada.

Esta política não impede a execução do Microsoft Edge Update, nem impede que os usuários instalem o software do Microsoft Edge por outros métodos.

Esta política está disponível apenas em instâncias do Windows que fazem parte de um domínio Microsoft® Active Directory®.
#### Informações e configurações do Windows
##### Informações da Política de Grupo (ADMX)
- Nome exclusivo da Política de Grupo: InstallDefault
- Nome da Política de Grupo: Permitir a instalação padrão
- Caminho da Política Padrão: Modelos Administrativos/Microsoft Edge Update/Aplicativos
- Nome do arquivo GP ADMX: msedgeupdate.admx
##### Configurações de registro do Windows
- Caminho: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Nome do valor: InstallDefault
- Tipo de valor: REG_DWORD
##### Valor de exemplo:
```
0x00000001
```
[Voltar ao início](#microsoft-edge---update-policies)


###  <a name="updatedefault"></a>UpdateDefault
#### Atualizar o padrão de substituição de política
>Microsoft Edge Update 1.2.145.5 e posterior

#### Descrição
Permite especificar o comportamento padrão para todos os canais referentes à maneira como o Microsoft Edge Update trata as atualizações disponíveis para o Microsoft Edge. Pode ser substituído para canais individuais ao especificar a política '[Atualizar a substituição de política](#update)' para esses canais específicos.

  Se você habilitar essa política, o Microsoft Edge Update tratará as atualizações do Microsoft Edge de acordo com as seguintes opções:
   - Sempre permitir atualizações: as atualizações sempre serão aplicadas quando forem encontradas por uma verificação de atualização periódica ou por uma verificação de atualização manual.
   - Somente atualizações silenciosas automáticas: as atualizações serão aplicadas somente quando forem encontradas pela verificação de atualização periódica.
   - Somente atualizações manuais: as atualizações serão aplicadas somente quando o usuário executar uma verificação de atualização manual.
   - Atualizações desabilitadas: as atualizações nunca serão aplicadas.

  Se você selecionar atualizações manuais, verifique periodicamente se há atualizações usando o mecanismo de atualizações manuais do aplicativo, se disponível. Se você desabilitar as atualizações, verifique periodicamente se há atualizações e as distribua aos usuários.

  Se você não habilitar e configurar essa política, o Microsoft Edge Update trata as atualizações disponíveis conforme especificado pela política '[Atualizar a substituição de política"](#update)'.

  Esta política está disponível apenas em instâncias do Windows que fazem parte de um domínio Microsoft® Active Directory®.
#### Informações e configurações do Windows
##### Informações da Política de Grupo (ADMX)
- Nome exclusivo da Política de Grupo: UpdateDefault
- Nome da Política de Grupo: Atualizar o padrão de substituição de política
- Caminho da Política Padrão: Modelos Administrativos/Microsoft Edge Update/Aplicativos
- Nome do arquivo GP ADMX: msedgeupdate.admx
##### Configurações de registro do Windows
- Caminho: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Nome do valor: UpdateDefault
- Tipo de valor: REG_DWORD
##### Valor de exemplo:
```
0x00000003
```
[Voltar ao início](#microsoft-edge---update-policies)


###  <a name="install"></a>Install
#### Permitir instalação
>Microsoft Edge Update 1.2.145.5 e posterior

#### Descrição
Especifica se um canal do Microsoft Edge pode ser instalado em dispositivos ingressados ​​no domínio.

  Se você habilitar esta política para um canal, o Microsoft Edge não terá sua instalação bloqueada.

  Se você desabilitar esta política para um canal, o Microsoft Edge será bloqueado para instalação.

  Se você não configurar esta política para um canal, a configuração da política '[Permitir instalação padrão](#installdefault)' determina se os usuários podem instalar esse canal do Microsoft Edge.

  Esta política está disponível apenas em instâncias do Windows que fazem parte de um domínio Microsoft® Active Directory®.
#### Informações e configurações do Windows
##### Informações da Política de Grupo (ADMX)
- Nome exclusivo da Política de Grupo: Install
- Nome da Política de Grupo: Permitir instalação
- Caminho da Política de Grupo: 
  - Modelos Administrativos/Microsoft Edge Update/Aplicativos/Microsoft Edge
  - Modelos Administrativos/Microsoft Edge Update/Aplicativos/Microsoft Edge Beta
  - Modelos Administrativos/Microsoft Edge Update/Aplicativos/Microsoft Edge Canary
  - Modelos Administrativos/Microsoft Edge Update/Aplicativos/Microsoft Edge Dev
- Nome do arquivo GP ADMX: msedgeupdate.admx
##### Configurações de registro do Windows
- Caminho: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Nome do valor: 
  - (Estável): Install{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}
  - (Beta): Install{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}
  - (Canary): Install{65C35B14-6C1D-4122-AC46-7148CC9D6497}
  - (Dev): Install{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}
- Tipo de valor: REG_DWORD
##### Valor de exemplo:
```
0x00000001
```
[Voltar ao início](#microsoft-edge---update-policies)


###  <a name="update"></a>Update
#### Atualizar a substituição de política
>Microsoft Edge Update 1.2.145.5 e posterior

#### Descrição
Especifica como o Microsoft Edge Update trata as atualizações disponíveis do Microsoft Edge.

Se você habilitar essa política, o Microsoft Edge Update tratará as atualizações do Microsoft Edge de acordo com as seguintes opções:
  - Sempre permitir atualizações: as atualizações sempre serão aplicadas quando forem encontradas por uma verificação de atualização periódica ou por uma verificação de atualização manual.
  - Somente atualizações silenciosas automáticas: as atualizações serão aplicadas somente quando forem encontradas pela verificação de atualização periódica.
  - Somente atualizações manuais: as atualizações serão aplicadas somente quando o usuário executar uma verificação de atualização manual. (Nem todos os aplicativos fornecem uma interface para essa opção.)
  - Atualizações desabilitadas: as atualizações nunca serão aplicadas.

Se você selecionar atualizações manuais, verifique periodicamente se há atualizações usando o mecanismo de atualizações manuais do aplicativo, se disponível. Se você desabilitar as atualizações, verifique periodicamente se há atualizações e as distribua aos usuários.

Se você não habilitar e configurar essa política, o Microsoft Edge Update tratará as atualizações disponíveis conforme especificado pela política '[Atualizar a substituição de política padrão](#updatedefault)'.

Consulte [https://go.microsoft.com/fwlink/?linkid=2136406](https://go.microsoft.com/fwlink/?linkid=2136406) para mais informações.

Esta política está disponível apenas em instâncias do Windows que fazem parte de um domínio Microsoft® Active Directory®.
#### Informações e configurações do Windows
##### Informações da Política de Grupo (ADMX)
- Nome exclusivo da Política de Grupo: Update
- Nome da Política de Grupo: Atualizar a substituição de política
- Caminho da Política de Grupo: 
  - Modelos Administrativos/Microsoft Edge Update/Aplicativos/Microsoft Edge
  - Modelos Administrativos/Microsoft Edge Update/Aplicativos/Microsoft Edge Beta
  - Modelos Administrativos/Microsoft Edge Update/Aplicativos/Microsoft Edge Canary
  - Modelos Administrativos/Microsoft Edge Update/Aplicativos/Microsoft Edge Dev
- Nome do arquivo GP ADMX: msedgeupdate.admx
##### Configurações de registro do Windows
- Caminho: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Nome do valor: 
  - (Estável): Update{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}
  - (Beta): Update{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}
  - (Canary): Update{65C35B14-6C1D-4122-AC46-7148CC9D6497}
  - (Dev): Update{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}
- Tipo de valor: REG_DWORD
##### Valor de exemplo:
```
0x00000001
```
[Voltar ao início](#microsoft-edge---update-policies)


###  <a name="allowsxs"></a>Allowsxs
#### Permitir a experiência de navegador Lado a Lado do Microsoft Edge
>Microsoft Edge Update 1.2.145.5 e posterior

#### Description
Essa política permite que um usuário execute o Microsoft Edge (Edge HTML) e o Microsoft Edge (baseado no Chromium) lado a lado.

Se essa política for definida como "Não configurada", o Microsoft Edge (baseado no Chromium) substituirá o Microsoft Edge (HTML do Edge) depois que o canal Estável do Microsoft Edge (baseado no Chromium) e as atualizações de segurança de novembro de 2019 forem instalados.  Esse comportamento é igual à configuração "Desabilitada".

A configuração "Desabilitada" bloqueia uma experiência lado a lado, e o Microsoft Edge (baseado no Chromium) substituirá o Microsoft Edge (HTML do Edge) depois que o canal Estável do Microsoft Edge (baseado no Chromium) e as atualizações de segurança de novembro de 2019 forem instalados.  Esse comportamento é igual à configuração "Não configurada".

Quando essa política for "Habilitada", o Microsoft Edge (baseado no Chromium) e o Microsoft Edge (Edge HTML) poderão ser executados lado a lado depois que o Microsoft Edge (baseado no Chromium) for instalado.

Para que essa política de grupo entre em vigor, ela deve ser configurada antes da instalação automática do Microsoft Edge (baseado no Chromium) pelo Windows Update. Observação: um usuário pode bloquear a atualização automática do Microsoft Edge (baseado no Chromium) usando o kit de ferramentas do bloqueador do Microsoft Edge (baseado no Chromium).
#### Informações e configurações do Windows
##### Informações da Política de Grupo (ADMX)
- Nome exclusivo da Política de Grupo: Allowsxs
- Nome da Política de Grupo: Permitir a experiência de navegador Lado a Lado do Microsoft Edge
- Caminho da Política Padrão: Modelos Administrativos/Microsoft Edge Update/Aplicativos
- Nome do arquivo GP ADMX: msedgeupdate.admx
##### Configurações de registro do Windows
- Caminho: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Nome do valor: Allowsxs
- Tipo de valor: REG_DWORD
##### Valor de exemplo:
```
0x00000001
```
[Voltar ao início](#microsoft-edge---update-policies)


###  <a name="createdesktopshortcutdefault"></a>CreateDesktopShortcutDefault
#### Impedir a criação de Atalho da Área de Trabalho com a instalação padrão
>Microsoft Edge Update 1.3.128.0 e posterior

#### Descrição
Permite especificar o comportamento padrão de todos os canais para criar um atalho da área de trabalho quando o Microsoft Edge for instalado.

  Se você habilitar esta política, um atalho da área de trabalho será criado quando o Microsoft Edge for instalado.
Se você desabilitar esta política, nenhum atalho da área de trabalho será criado quando o Microsoft Edge for instalado.
Se você não configurar esta política, um atalho da área de trabalho para o Microsoft Edge será criado durante a instalação.
Se o Microsoft Edge já estiver instalado, esta política não terá efeito.
#### Informações e configurações do Windows
##### Informações da Política de Grupo (ADMX)
- Nome exclusivo da Política de Grupo: CreateDesktopShortcutDefault
- Nome da Política de Grupo: Impedir a criação de Atalho da Área de Trabalho com a instalação padrão
- Caminho da Política Padrão: Modelos Administrativos/Microsoft Edge Update/Aplicativos
- Nome do arquivo GP ADMX: msedgeupdate.admx
##### Configurações de registro do Windows
- Caminho: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Nome do Valor: CreateDesktopShortcutDefault
- Tipo de valor: REG_DWORD
##### Valor de exemplo:
```
0x00000001
```
[Voltar ao início](#microsoft-edge---update-policies)


###  <a name="createdesktopshortcut"></a>CreateDesktopShortcut
#### Impedir a criação de Atalho da Área de Trabalho com a instalação
>Microsoft Edge Update 1.3.128.0 e posterior

#### Descrição
Se você habilitar esta política, um atalho da área de trabalho será criado quando o Microsoft Edge for instalado.
Se você desabilitar esta política, nenhum atalho da área de trabalho será criado quando o Microsoft Edge for instalado.
Se você não configurar esta política, um atalho da área de trabalho para o Microsoft Edge será criado durante a instalação.
Se o Microsoft Edge já estiver instalado, esta política não terá efeito.

  Se você não configurar esta política para um canal, a configuração de política padrão '[Evitar a criação de um Atalho no Desktop ao instalar](#createdesktopshortcutdefault)' determinará a criação de um atalho quando o Microsoft Edge for instalado.
#### Informações e configurações do Windows
##### Informações da Política de Grupo (ADMX)
- Nome exclusivo da Política de Grupo: CreateDesktopShortcut
- Nome da GP: Impedir a criação de Atalho da Área de Trabalho com a instalação
- Caminho da Política de Grupo: 
  - Modelos Administrativos/Microsoft Edge Update/Aplicativos/Microsoft Edge
  - Modelos Administrativos/Microsoft Edge Update/Aplicativos/Microsoft Edge Beta
  - Modelos Administrativos/Microsoft Edge Update/Aplicativos/Microsoft Edge Canary
  - Modelos Administrativos/Microsoft Edge Update/Aplicativos/Microsoft Edge Dev
- Nome do arquivo GP ADMX: msedgeupdate.admx
##### Configurações de registro do Windows
- Caminho: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Nome do valor: 
  - (Estável): CreateDesktopShortcut{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}
  - (Beta): CreateDesktopShortcut{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}
  - (Canary): CreateDesktopShortcut{65C35B14-6C1D-4122-AC46-7148CC9D6497}
  - (Dev): CreateDesktopShortcut{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}
- Tipo de valor: REG_DWORD
##### Valor de exemplo:
```
0x00000001
```
[Voltar ao início](#microsoft-edge---update-policies)


###  <a name="rollbacktotargetversion"></a>RollbackToTargetVersion
#### Reverter para a Versão de Destino
>Microsoft Edge Update 1.3.133.3 e posterior

#### Descrição
Especifica que o Microsoft Edge Update deve reverter as instalações do Microsoft Edge para a versão indicada em '[Substituição da versão de destino](#targetversionprefix)'.

Esta política não tem efeito a menos que '[Substituição da versão de destino](#targetversionprefix)' seja definida e '[Substituição da política de atualização](#update)' seja definida como um dos estados ATIVADO (Sempre permitir atualizações, Somente atualizações automáticas silenciosas, Somente atualizações manuais).

Se você desabilitar esta política ou não configurá-la, as instalações que possuem uma versão superior à especificada pela '[Substituição da versão de destino](#targetversionprefix)' serão deixadas como estão.

Se você habilitar esta política, as instalações que possuem uma versão atual superior à especificada pela '[Substituição da versão de destino](#targetversionprefix)' serão desatualizadas para a versão de destino.

Recomendamos que os usuários instalem a versão mais recente do navegador Microsoft Edge para garantir a proteção pelas atualizações de segurança mais recentes. Reverter para uma versão anterior corre o perigo de se expor aos problemas de segurança conhecidos. Esta política deve ser usada como uma correção temporária para resolver problemas em uma atualização do navegador Microsoft Edge.

Antes de reverter temporariamente a versão do seu navegador, recomendamos que você ative a Sincronização ([https://go.microsoft.com/fwlink/?linkid=2133032](https://go.microsoft.com/fwlink/?linkid=2133032)) para todos os usuários em sua organização. Se você não ativar a Sincronização, existe o risco de perda permanente de dados de navegação. Use esta política por sua conta e risco.

Nota: Todas as versões disponíveis para reversão podem ser vistas aqui [https://aka.ms/EdgeEnterprise](https://aka.ms/EdgeEnterprise).

Esta política se aplica ao Microsoft Edge versão 86 ou posterior.

Consulte [https://go.microsoft.com/fwlink/?linkid=2133918](https://go.microsoft.com/fwlink/?linkid=2133918) para mais informações.

Esta política está disponível apenas em instâncias do Windows que fazem parte de um domínio Microsoft® Active Directory®.
#### Informações e configurações do Windows
##### Informações da Política de Grupo (ADMX)
- Nome exclusivo da GP: RollbackToTargetVersion
- Nome da GP: Reverter para a Versão de Destino
- Caminho da Política de Grupo: 
  - Modelos Administrativos/Microsoft Edge Update/Aplicativos/Microsoft Edge
  - Modelos Administrativos/Microsoft Edge Update/Aplicativos/Microsoft Edge Beta
  - Modelos Administrativos/Microsoft Edge Update/Aplicativos/Microsoft Edge Canary
  - Modelos Administrativos/Microsoft Edge Update/Aplicativos/Microsoft Edge Dev
- Nome do arquivo GP ADMX: msedgeupdate.admx
##### Configurações de registro do Windows
- Caminho: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Nome do valor: 
  - (Estável): RollbackToTargetVersion{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}
  - (Beta): RollbackToTargetVersion{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}
  - (Canário): RollbackToTargetVersion{65C35B14-6C1D-4122-AC46-7148CC9D6497}
  - (Dev): RollbackToTargetVersion{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}
- Tipo de valor: REG_DWORD
##### Valor de exemplo:
```
0x00000001
```
[Voltar ao início](#microsoft-edge---update-policies)


###  <a name="targetversionprefix"></a>TargetVersionPrefix
#### Substituir versão de destino
>Microsoft Edge Update 1.3.119.43 e posterior

#### Descrição
Quando esta política estiver habilitada e a atualização automática estiver habilitada, o Microsoft Edge será atualizado para a versão especificada por esse valor de política.

O valor da política deve ser uma versão do Microsoft Edge específica, por exemplo, 83.0.499.12.

Se um dispositivo tiver uma versão mais recente do Microsoft Edge do que o valor especificado, a versão mais recente do Microsoft Edge será mantida e ele não será revertido para a versão especificada.

Se a versão especificada não existir ou estiver formatada inadequadamente, o Microsoft Edge permanecerá na versão atual e não será atualizado para versões futuras automaticamente.

Consulte [https://go.microsoft.com/fwlink/?linkid=2136707](https://go.microsoft.com/fwlink/?linkid=2136707) para mais informações.

Esta política está disponível apenas em instâncias do Windows que fazem parte de um domínio Microsoft® Active Directory®.
#### Informações e configurações do Windows
##### Informações da Política de Grupo (ADMX)
- Nome exclusivo da Política de Grupo: TargetVersionPrefix
- Nome da Política de Grupo: Substituir versão de destino
- Caminho da Política de Grupo: 
  - Modelos Administrativos/Microsoft Edge Update/Aplicativos/Microsoft Edge
  - Modelos Administrativos/Microsoft Edge Update/Aplicativos/Microsoft Edge Beta
  - Modelos Administrativos/Microsoft Edge Update/Aplicativos/Microsoft Edge Canary
  - Modelos Administrativos/Microsoft Edge Update/Aplicativos/Microsoft Edge Dev
- Nome do arquivo GP ADMX: msedgeupdate.admx
##### Configurações de registro do Windows
- Caminho: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Nome do valor: 
  - (Estável): TargetVersionPrefix {56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}
  - (Beta): TargetVersionPrefix {2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}
  - (Canary): TargetVersionPrefix {65C35B14-6C1D-4122-AC46-7148CC9D6497}
  - (Dev): TargetVersionPrefix {0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}
- Tipo do valor: REG_SZ
##### Valor de exemplo:
```
83.0.499.12
```
[Voltar ao início](#microsoft-edge---update-policies)


##  <a name="preferences-policies"></a>Políticas de preferências

[Voltar ao início](#microsoft-edge---update-policies)
###  <a name="autoupdatecheckperiodminutes"></a>AutoUpdateCheckPeriodMinutes
#### Atualizar automaticamente a substituição do período de verificação
>Microsoft Edge Update 1.2.145.5 e posterior

#### Descrição
Se habilitada, essa política permite definir um valor para o número mínimo de minutos entre as verificações de atualização automática. Caso contrário, por padrão, a verificação de atualização automática verifica se há as atualizações a cada 10 horas.

  Se você quiser desabilitar todas as verificações de atualização automática, defina o valor como 0 (não recomendado).
#### Informações e configurações do Windows
##### Informações da Política de Grupo (ADMX)
- Nome exclusivo da Política de Grupo: AutoUpdateCheckPeriodMinutes
- Nome da Política de Grupo: Atualizar automaticamente a substituição do período de verificação
- Caminho da Política de Grupo: Modelos Administrativos/Microsoft Edge Update/Preferências
- Nome do arquivo GP ADMX: msedgeupdate.admx
##### Configurações de registro do Windows
- Caminho: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Nome do valor: AutoUpdateCheckPeriodMinutes
- Tipo de valor: REG_DWORD
##### Valor de exemplo:
```
0x00000578
```
[Voltar ao início](#microsoft-edge---update-policies)


###  <a name="updatessuppressed"></a>UpdatesSuppressed
#### Período em cada dia para suprimir a verificação de atualização automática
>Microsoft Edge Update 1.3.33.5 e posterior

#### Descrição
Se você habilitar essa política, as verificações de atualização serão suprimidas por dia a partir de Hora:Minuto por um período de duração (em minutos). A duração não é afetada pelo horário de verão. Por exemplo, se o horário de início for 22:00 e a duração for de 480 minutos, as atualizações serão suprimidas por exatamente oito horas, independentemente do horário de verão começar ou terminar durante esse período.

  Se você desabilitar ou não configurar essa política, as verificações de atualização não serão suprimidas durante nenhum período específico.
#### Informações e configurações do Windows
##### Informações da Política de Grupo (ADMX)
- Nome exclusivo da Política de Grupo: UpdatesSuppressed
- Nome da Política de Grupo: Período em cada dia para suprimir a verificação de atualização automática
  - Opções { Hour, Minute, Duration }
- Caminho da Política de Grupo: Modelos Administrativos/Microsoft Edge Update/Preferências
- Nome do arquivo GP ADMX: msedgeupdate.admx
##### Configurações de registro do Windows
- Caminho: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Nome do valor: 
  - UpdatesSuppressedDurationMin
  - UpdatesSuppressedStartHour
  - UpdatesSuppressedStartMin
- Tipo de valor: REG_DWORD
##### Valor de exemplo:
```
duration   : 0x0000003c
start hour : 0x00000001
start min  : 0x00000002
```
[Voltar ao início](#microsoft-edge---update-policies)


##  <a name="proxy-server-policies"></a>Políticas do servidor proxy

[Voltar ao início](#microsoft-edge---update-policies)
###  <a name="proxymode"></a>ProxyMode
#### Escolher como especificar as configurações do servidor proxy
>Microsoft Edge Update 1.3.21.81 e posterior

#### Descrição
Permite especificar as configurações do servidor proxy que serão usadas pelo Microsoft Edge Update.

  Se você habilitar essa configuração da política, poderá escolher entre as seguintes opções do servidor proxy:
   - Se você optar por nunca usar um servidor proxy e sempre se conectar diretamente, todas as outras opções serão ignoradas.
   - Se você optar por usar as configurações de proxy do sistema ou detectar automaticamente o servidor proxy, todas as outras opções serão ignoradas.
   - Se escolher o modo fixo do servidor proxy, você poderá especificar mais opções em '[Endereço ou URL do servidor proxy](#proxyserver)'.
   - Se você optar por usar um script de proxy .pac, deve especificar a URL do script em '[De URL para um arquivo .pac de proxy](#proxypacurl)'.

  Se você habilitar essa política, os usuários de sua organização não poderão alterar as configurações de proxy no Microsoft Edge Update.

  Se você desabilitar ou não configurar essa política, nenhuma configuração do servidor proxy será definida, mas os usuários de sua organização poderão escolher suas próprias configurações de proxy para o Microsoft Edge Update.
#### Informações e configurações do Windows
##### Informações da Política de Grupo (ADMX)
- Nome exclusivo da Política de Grupo: ProxyMode
- Nome da Política de Grupo: Escolher como especificar as configurações do servidor proxy
- Caminho da Política de Grupo: Modelos Administrativos/Microsoft Edge Update/Servidor Proxy
- Nome do arquivo GP ADMX: msedgeupdate.admx
##### Configurações de registro do Windows
- Caminho: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Nome do valor: ProxyMode
- Tipo do valor: REG_SZ
##### Valor de exemplo:
```
fixed_servers
```
[Voltar ao início](#microsoft-edge---update-policies)


###  <a name="proxypacurl"></a>ProxyPacUrl
#### A URL para um arquivo .pac de proxy
>Microsoft Edge Update 1.3.21.81 e posterior

#### Descrição
Permite especificar uma URL para um arquivo (PAC) de configuração automática de proxy.

  Se habilitar essa política, você poderá especificar uma URL de um arquivo PAC para automatizar a maneira como o Microsoft Edge Update seleciona para a busca de um site específico.

  Essa política será aplicada somente se você especificou as configurações de proxy manuais na política '[Escolher como especificar configurações do servidor proxy](#proxymode)'.

  Não configure essa política se você selecionou uma configuração de proxy que não seja manual na política '[Escolher como especificar as configurações do servidor proxy](#proxymode)'.
#### Informações e configurações do Windows
##### Informações da Política de Grupo (ADMX)
- Nome exclusivo da Política de Grupo: ProxyPacUrl
- Nome da Política de Grupo: A URL para um arquivo .pac de proxy
- Caminho da Política de Grupo: Modelos Administrativos/Microsoft Edge Update/Servidor Proxy
- Nome do arquivo GP ADMX: msedgeupdate.admx
##### Configurações de registro do Windows
- Caminho: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Nome do valor: ProxyPacUrl
- Tipo do valor: REG_SZ
##### Valor de exemplo:
```
https://www.microsoft.com
```
[Voltar ao início](#microsoft-edge---update-policies)


###  <a name="proxyserver"></a>ProxyServer
#### Endereço ou URL do servidor proxy
>Microsoft Edge Update 1.3.21.81 e posterior

#### Description
Permite especificar a URL do servidor proxy para o Microsoft Edge Update usar.

  Se você habilitar essa política, poderá configurar a URL do servidor proxy usada pelo Microsoft Edge Update em sua organização.

  Essa política será aplicada somente se você selecionou as configurações de proxy manuais na política '[Escolher como especificar as configurações do servidor proxy](#proxymode)'.

  Não configure essa política se você selecionou uma configuração de proxy que não seja manual na política '[Escolher como especificar as configurações do servidor proxy](#proxymode)'.
#### Informações e configurações do Windows
##### Informações da Política de Grupo (ADMX)
- Nome exclusivo da Política de Grupo: ProxyServer
- Nome da Política de Grupo: O endereço ou a URL do servidor proxy
- Caminho da Política de Grupo: Modelos Administrativos/Microsoft Edge Update/Servidor Proxy
- Nome do arquivo GP ADMX: msedgeupdate.admx
##### Configurações de registro do Windows
- Caminho: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Nome do valor: ProxyServer
- Tipo do valor: REG_SZ
##### Valor de exemplo:
```
https://www.microsoft.com
```
[Voltar ao início](#microsoft-edge---update-policies)


##  <a name="microsoft-edge-webview-policies"></a>Políticas do Microsoft Edge WebView

[Voltar ao início](#microsoft-edge---update-policies)
###  <a name="install-(webview)"></a>Instalar (WebView)
#### Permitir instalação
>Microsoft Edge Update 1.3.127.1 e posterior

#### Descrição
Permite especificar se o Microsoft Edge WebView pode ser instalado usando o Microsoft Edge Update.

  - Se você habilitar esta política, os usuários poderão instalar o Microsoft Edge WebView por meio do Microsoft Edge Update.
  - Se você desabilitar esta política, os usuários não poderão instalar o Microsoft Edge WebView por meio do Microsoft Edge Update.
  - Se você não configurar esta política, a configuração da política '[Permitir instalação padrão](#installdefault)' determina se os usuários podem instalar o Microsoft Edge WebView por meio do Microsoft Edge Update.
#### Informações e configurações do Windows
##### Informações da Política de Grupo (ADMX)
- Nome exclusivo da Política de Grupo: Install
- Nome da Política de Grupo: Permitir instalação
- Caminho da Política de Grupo: Modelos Administrativos/Microsoft Edge Update/Microsoft Edge WebView
- Nome do arquivo GP ADMX: msedgeupdate.admx
##### Configurações de registro do Windows
- Caminho: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Nome do valor: 
  - Install{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}
- Tipo de valor: REG_DWORD
##### Valor de exemplo:
```
0x00000001
```
[Voltar ao início](#microsoft-edge---update-policies)


###  <a name="update-(webview)"></a>Atualização (WebView)
#### Atualizar a substituição de política
>Microsoft Edge Update 1.3.127.1 e posterior

#### Descrição
Permite especificar se as atualizações automáticas estão habilitadas ou não para o Microsoft Edge WebView. O Microsoft Edge WebView é um componente usado pelos aplicativos para exibir conteúdo da Web.
As atualizações automáticas estão habilitadas por padrão. Desabilitar as atualizações automáticas do Microsoft Edge WebView pode causar problemas de compatibilidade com aplicativos que dependem desse componente.

  Se você habilitar esta política, o Microsoft Edge Update tratará as atualizações do Microsoft Edge WebView de acordo com as seguintes opções:
  - Sempre permitir atualizações: as atualizações serão baixadas e aplicadas automaticamente
  - Atualizações desabilitadas: as atualizações nunca serão baixadas ou aplicadas

  Se você não habilitar esta política, as atualizações serão baixadas e aplicadas automaticamente.
#### Informações e configurações do Windows
##### Informações da Política de Grupo (ADMX)
- Nome exclusivo da Política de Grupo: Update
- Nome da Política de Grupo: Atualizar a substituição de política
- Caminho da Política de Grupo: Modelos Administrativos/Microsoft Edge Update/Microsoft Edge WebView
- Nome do arquivo GP ADMX: msedgeupdate.admx
##### Configurações de registro do Windows
- Caminho: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Nome do valor: 
  - Update{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}
- Tipo de valor: REG_DWORD
##### Valor de exemplo:
```
0x00000001
```
[Voltar ao início](#microsoft-edge---update-policies)


##  <a name="see-also"></a>Consulte também
  - [Configurar o Microsoft Edge](configure-microsoft-edge.md)
  - [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)