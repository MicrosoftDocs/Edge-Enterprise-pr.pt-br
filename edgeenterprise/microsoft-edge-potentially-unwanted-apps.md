---
title: Usar o Microsoft Edge para se proteger contra aplicativos potencialmente indesejados
ms.author: kvice
author: dan-wesley
manager: srugh
ms.date: 03/04/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Usar o Microsoft Edge para se proteger contra aplicativos potencialmente indesejados
ms.openlocfilehash: 615442acc0e9ed58da37aa0ef8b3747e916a8024
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10978975"
---
# Proteger-se contra aplicativos potencialmente indesejados (PUAs)

Este artigo explica como você pode se proteger contra aplicativos potencialmente indesejados (PUAs) usando o Microsoft Edge ou o Windows Defender Antivirus.

> [!NOTE]
> Este artigo se aplica ao Microsoft Edge versão 80 ou posterior.

## Visão geral

Aplicativos potencialmente indesejados não são considerados vírus ou malware, mas eles podem executar ações em pontos de extremidade que afetem negativamente o desempenho ou o uso do ponto de extremidade. Por exemplo, o *software Evasion* tenta ativamente escapar a detecção por produtos de segurança. Esse tipo de software pode aumentar o risco de sua rede ser infectada com malware real. PUA também pode se referir aos aplicativos cuja reputação é considerada ruim.

Para obter uma descrição dos critérios usados para a classificação de software como PUA, confira [Aplicativos potencialmente indesejados](https://docs.microsoft.com/windows/security/threat-protection/intelligence/criteria#potentially-unwanted-application-pua).

## Proteger-se contra PUA com o Microsoft Edge

O Microsoft Edge (versão 80.0.361.50 ou posterior) bloqueia downloads PUA e URLs de recursos associadas.

Para configurar a proteção, habilite o recurso **bloquear aplicativos potencialmente indesejados** no Microsoft Edge.

> [!NOTE]
> A [postagem no blog da equipe do Microsoft Edge](https://blogs.windows.com/msedgedev/2020/02/27/protecting-users-potentially-unwanted-apps/) descreve esse novo recurso e explica como tratar um aplicativo rotulado incorretamente ou relatar um aplicativo como indesejado.

### Para habilitar proteção contra PUA:

1. Abra as **Configurações** no navegador.
2. Selecione **Privacidade e serviços**.
3. Na seção **Serviços**, verifique se o **Microsoft Defender SmartScreen** está ativado. Caso contrário, ative o Microsoft Defender SmartScreen. O exemplo na captura de tela a seguir mostra que o navegador é gerenciado pela organização e que o Microsoft Defender SmartScreen está ativado.

   ![Ativar o Microsoft Edge PUA nas Configurações](./media/microsoft-edge-potentially-unwanted-apps/security-pua-setup.png)

4. Na seção **Serviços**, use o botão de alternância mostrado na captura de tela anterior para ativar **Bloquear aplicativos potencialmente indesejados**.

   > [!TIP]
   > Você pode explorar com segurança o recurso de bloqueio de URL da proteção contra PUA, testando-o em uma das nossas páginas de demonstração do [Windows Defender SmartScreen](https://demo.smartscreen.msft.net/).

Quando o Microsoft Edge detectar um PUA, você verá uma mensagem como a exibida na próxima captura de tela.

   ![Mensagem de aviso do Microsoft Edge PUA](./media/microsoft-edge-potentially-unwanted-apps/security-pua-msg.png)

### Para bloquear contra URLs associadas a PUA

Depois de ativar a proteção contra PUA no Microsoft Edge, o Windows Defender SmartScreen protegerá você contra URLs associadas a PUA.

Há várias maneiras de os administradores configurarem como o Microsoft Edge e o Windows Defender SmartScreen funcionam em conjunto para proteger os usuários contra URLs associadas a PUA. Para obter mais informações, consulte:

- [Definir configurações de política do Microsoft Edge no Windows](https://docs.microsoft.com/DeployEdge/configure-microsoft-edge)
- [Configurações do SmartScreen](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#smartscreen-settings)
- [Política SmartScreenPuaEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#smartscreenpuaenabled)
- [Configurar o Windows Defender SmartScreen](https://docs.microsoft.com/microsoft-edge/deploy/available-policies?source=docs#configure-windows-defender-smartscreen)

Os administradores também podem personalizar a lista de bloqueios da Proteção Avançada contra Ameaças do Microsoft Defender (Microsoft Defender ATP). Eles podem usar o portal do Microsoft Defender ATP para [criar e gerenciar indicadores de IPs e URLs](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/manage-indicators#create-indicators-for-ips-and-urlsdomains-preview).

## Proteger-se contra PUA com o Windows Defender Antivirus

O artigo [Detectar e bloquear aplicativos potencialmente indesejados](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-antivirus/detect-block-potentially-unwanted-apps-windows-defender-antivirus#windows-defender-antivirus) também descreve como você pode configurar o Windows Defender Antivirus para habilitar a proteção contra PUA. Você pode configurar a proteção usando qualquer uma das seguintes opções:

- [Microsoft Intune](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-antivirus/detect-block-potentially-unwanted-apps-windows-defender-antivirus#use-intune-to-configure-pua-protection)
- [Microsoft Endpoint Configuration Manager](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-antivirus/detect-block-potentially-unwanted-apps-windows-defender-antivirus#use-configuration-manager-to-configure-pua-protection)
- [Política de Grupo](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-antivirus/detect-block-potentially-unwanted-apps-windows-defender-antivirus#use-group-policy-to-configure-pua-protection)
- [Cmdlets do PowerShell](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-antivirus/detect-block-potentially-unwanted-apps-windows-defender-antivirus#use-powershell-cmdlets-to-configure-pua-protection)

Quando o Windows Defender detecta um arquivo PUA em um ponto de extremidade, ele coloca o arquivo em quarentena e notifica o usuário ([ a menos que as notificações estejam desabilitadas](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-antivirus/configure-notifications-windows-defender-antivirus)) no mesmo formato da detecção de ameaças normal (precedido de "PUA:"). As ameaças detectadas também aparecem na [lista de quarentena no aplicativo de Segurança do Windows](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-antivirus/windows-defender-security-center-antivirus#detection-history).

### Notificações e eventos PUA

Há várias maneiras de um administrador ver eventos PUA:

- No Visualizador de Eventos do Windows, mas não no Microsoft Endpoint Configuration Manager ou no Intune.
- Em um email, se as notificações de email para detecção de PUA estiverem ativadas.
- Nos logs de eventos do[ Windows Defender Antivirus](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-antivirus/troubleshoot-windows-defender-antivirus), em que um evento PUA é registrado sob o ID de evento 1116 com a mensagem: "A plataforma antimalware detectou malware ou outro software potencialmente indesejado."

> [!NOTE]
> Os usuários verão "*.exe foi bloqueado como um aplicativo potencialmente indesejado pelo Microsoft defender SmartScreen".

### Incluir um aplicativo na lista de permissões

Assim como o Microsoft Edge, o Windows Defender Antivirus oferece uma maneira de permitir arquivos bloqueados por engano ou que sejam necessários para concluir uma tarefa. Se isso acontecer, você pode incluir um arquivo na lista de permissões. Para obter mais informações, confira [como configurar a Endpoint Protection no Configuration Manager](https://docs.microsoft.com/previous-versions/system-center/system-center-2012-R2/hh508770(v=technet.10)#to-exclude-specific-files-or-folders) para saber como excluir arquivos ou pastas específicas.

## Consulte também

- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Proteção contra ameaças](https://docs.microsoft.com/windows/security/threat-protection/index)
- [Configurar a proteção comportamental, heurística e em tempo real](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-antivirus/configure-protection-features-windows-defender-antivirus)
- [Proteção de próxima geração](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-antivirus/windows-defender-antivirus-in-windows-10)
- [Linha de base de segurança para o Microsoft Edge baseado em Chromium, versão 79](https://techcommunity.microsoft.com/t5/microsoft-security-baselines/security-baseline-final-for-chromium-based-microsoft-edge/ba-p/1111863)
