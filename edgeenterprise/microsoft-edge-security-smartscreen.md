---
title: Suporte do Microsoft Edge para o Microsoft Defender SmartScreen
ms.author: kvice
author: dan-wesley
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Suporte do Microsoft Edge para o Microsoft Defender SmartScreen
ms.openlocfilehash: c09664e6c7785607e40ac53e26c2f377a66f6cef7a6da2b1d53cf15baad29616
ms.sourcegitcommit: d44c0997ffe40d67421312ed96e7766da947eaa0
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/05/2021
ms.locfileid: "11727125"
---
# <a name="microsoft-edge-support-for-microsoft-defender-smartscreen"></a>Suporte do Microsoft Edge para o Microsoft Defender SmartScreen

Este artigo descreve as vantagens de usar o Microsoft Defender SmartScreen, explica como ele funciona e descreve como configurar esse recurso do Microsoft Edge.

> [!NOTE]
> Este artigo se aplica ao Microsoft Edge versão 77 ou posterior.

O Microsoft Defender SmartScreen é um serviço que o Microsoft Edge usa para manter você seguro enquanto navega pela Web. O Microsoft Defender SmartScreen fornece um sistema de aviso prévio contra sites que podem se envolver em ataques de phishing ou tentar distribuir software mal-intencionado por meio de um ataque focado. Para obter mais informações, assista a [Vídeo: Navegação segura no Microsoft Edge](microsoft-edge-video-security-smartscreen.md).

> [!NOTE]
> Antes do Windows 10, versão 1703, esse recurso era chamado de filtro do SmartScreen, quando usado no navegador, e Microsoft SmartScreen, quando usado fora do navegador.

## <a name="the-benefits-of-microsoft-defender-smartscreen"></a>Benefícios do Microsoft Defender SmartScreen

O Microsoft Defender SmartScreen oferece vários benefícios, resumidos na lista a seguir. Esses benefícios estão descritos em detalhes na [documentação do Microsoft Defender SmartScreen](/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-overview#benefits-of-windows-defender-smartscreen). Os benefícios são:

- Suporte antiphishing e antimalware
- URL baseada em reputação e proteção de aplicativo
- Integração do sistema operacional
- Heurística e dados de diagnóstico aprimorados
- Gerenciamento por meio da Política de Grupo e do Microsoft Intune
- Bloqueio de URLs associadas a aplicativos potencialmente indesejados

## <a name="understand-how-microsoft-defender-smartscreen-works"></a>Entenda como o Microsoft Defender SmartScreen funciona

Várias entradas contribuem para os avisos do Microsoft Defender SmartScreen. Os dados são recebidos de várias fontes, incluindo comentários dos usuários, provedores de dados e modelos de inteligência. Esses dados são usados para ajudar a identificar conteúdo potencialmente mal-intencionado. O Microsoft Defender SmartScreen também verifica aplicativos baixados ou instaladores de aplicativos para ver se eles são mal-intencionados. Em ambos os cenários, o Microsoft Defender SmartScreen avisa os usuários adequadamente sobre conteúdo suspeito.

### <a name="site-analysis"></a>Análise do site

O Microsoft Defender SmartScreen determina se um site é potencialmente mal-intencionado por meio de:

- Análise de páginas da Web visitadas para verificar se há indícios de comportamento suspeito.
- Análise de sites visitados em relação a um registro dinâmico de sites de phishing informados.

Se o Microsoft Defender SmartScreen determinar que uma página é maliciosa, ela mostrará uma página de aviso para notificar ao usuário que o site foi relatado como não seguro. A próxima captura de tela mostra um exemplo de uma página de aviso do Microsoft Defender SmartScreen quando um usuário tenta abrir um site mal-intencionado.

![Página de bloqueio do Microsoft Defender SmartScreen para um link para site externo](media/microsoft-edge-security-smartscreen/microsoft-edge-smartscreen-warning.png)

Os usuários recebem a opção de relatar um site como seguro ou não seguro na mensagem de aviso. Para mais informações, confira [como denunciar um site](/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-set-individual-device#how-users-can-report-websites-as-safe-or-unsafe).

### <a name="file-analysis"></a>Análise de arquivo

O Microsoft Defender SmartScreen determina se um aplicativo baixado ou um instalador de aplicativo é potencialmente mal-intencionado com base em vários critérios, como o tráfego de downloads, o histórico de downloads, o histórico de resultados do antivírus e a reputação da URL.

- Arquivos com uma reputação segura conhecida serão baixados sem qualquer notificação.  
- Arquivos com reputação mal-intencionada conhecida mostram um aviso para informar ao usuário que o arquivo não é seguro e foi relatado como mal-intencionado. Microsoft Defender SmartScreen bloquea notificação para arquivo com reputação maliciosa

  ![Microsoft Defender SmartScreen bloquea notificação para arquivo com reputação maliciosa](media/microsoft-edge-security-smartscreen/ms-edge-smartscreen-known-malicious.png)

- Os arquivos desconhecidos mostram um aviso para que o usuário saiba que o download não possui uma pegada conhecida e se recomenda cautela. A próxima captura de tela é um exemplo de aviso de um arquivo desconhecido.

  ![Microsoft Defender SmartScreen bloquear notificação para arquivo com reputação desconhecida](media/microsoft-edge-security-smartscreen/ms-edge-smartscreen-unknown-malicious.png)

Nem todos os programas desconhecidos são mal-intencionados, e o aviso de desconhecido tem o objetivo de fornecer contexto e orientação aos usuários que precisam, principalmente se o aviso for inesperado.

  ![Manter arquivo com reputação mal-intencionada](media/microsoft-edge-security-smartscreen/ms-edge-smartscreen-unknown-malicious-keep.png)

No entanto, os usuários ainda podem baixar e executar o aplicativo clicando em **... | Manter | Mostrar mais | Manter mesmo assim**.

> [!TIP]
> **INFO para Clientes Corporativos.** Por padrão, o Microsoft Defender SmartScreen permite que os usuários ignorem os avisos. Como essa interação do usuário é potencialmente arriscada, recomendamos que você revise essas [configurações de política de grupo recomendadas](/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-available-settings#recommended-group-policy-and-mdm-settings-for-your-organization).

Você pode ver como o Microsoft Defender SmartScreen responde a diferentes cenários usando nosso [site de demonstração](https://demo.smartscreen.msft.net/).

## <a name="microsoft-defender-smartscreen-and-user-privacy"></a>Privacidade do usuário e o Microsoft Defender SmartScreen

O Microsoft Defender SmartScreen protege os usuários enquanto eles navegam na Internet usando um sistema de verificação de reputação. O Microsoft Edge passa informações relevantes sobre a URL ou arquivo para o serviço Microsoft Defender SmartScreen para iniciar a verificação de reputação. A verificação compara o site ou arquivo com listas dinâmicas de sites e arquivos conhecidos por serem perigosos. Todas as solicitações para o serviço Microsoft Defender SmartScreen são feitas com criptografia TLS. O serviço retorna os resultados da verificação de reputação, o que pode levar o Microsoft Edge a exibir um aviso para o site ou arquivo. Esses resultados são armazenados localmente no dispositivo.

O serviço Microsoft Defender SmartScreen armazena dados sobre verificações de reputação. À medida que novos sites são identificados, o serviço os adiciona a um banco de dados dinâmico de URLs e arquivos mal-intencionados conhecidos. Esses dados são armazenados em servidores Microsoft seguros e são usados apenas para serviços de segurança da Microsoft. Esses dados nunca serão usados para identificar ou direcionar usuários de forma alguma. A limpeza do cache de navegação limpa todos os dados de URL armazenados localmente no Microsoft Defender SmartScreen. A limpeza do histórico de downloads removerá todos os dados do SmartScreen armazenados localmente relacionados a downloads de arquivos.

Para obter mais informações sobre o Microsoft Defender SmartScreen e a privacidade no Microsoft Edge, leia o [White paper de privacidade do Microsoft Edge](/microsoft-edge/privacy-whitepaper#smartscreen).

## <a name="microsoft-defender-smartscreen-setup-for-admins"></a>Configuração do Microsoft Defender SmartScreen para administradores

Os administradores podem configurar o Microsoft Defender SmartScreen usando a Diretiva de Grupo, o Microsoft Intune ou as configurações de gerenciamento de dispositivos móveis (MDM). Com base em como você configura o Microsoft Defender SmartScreen, é possível mostrar aos usuários uma página de aviso e deixá-los continuar no site ou bloquear o site completamente.

### <a name="microsoft-defender-smartscreen-set-up-using-group-policy"></a>Microsoft Defender SmartScreen configurado usando a Política de Grupo

Para obter uma lista completa das políticas do SmartScreen, confira [Configurações do Microsoft Defender SmartScreen](./microsoft-edge-policies.md#smartscreen-settings)

### <a name="microsoft-defender-smartscreen-set-up-using-mdm"></a>Configuração do Microsoft Defender SmartScreen usando MDM

Para obter mais informações, consulte:

- [Configurações do Windows Intune para o Microsoft Defender SmartScreen](/mem/intune/protect/endpoint-protection-windows-10#windows-defender-smartscreen-settings)
- [Configurações de política MDM](/mem/intune/protect/endpoint-protection-windows-10#windows-defender-smartscreen-settings)

## <a name="microsoft-defender-smartscreen-setup-for-users"></a>Configuração do Microsoft Defender SmartScreen para usuários

O Microsoft Defender SmartScreen está ativado por padrão no Microsoft Edge. Para desativar o Microsoft Defender SmartScreen, vá para *edge://settings/privacy > Serviços > Microsoft Defender SmartScreen*. Essa configuração é a mesma para todos os perfis associados à instalação do Microsoft Edge em um dispositivo. Essa configuração não é sincronizada entre dispositivos. A configuração se aplica à navegação InPrivate e ao modo Convidado. Se um dispositivo for gerenciado com políticas de grupo definidas por uma organização, essa configuração será refletida em *edge://settings/privacy*.

> [!NOTE]
> Os usuários podem configurar o Microsoft Defender SmartScreen para um dispositivo individual, a menos que a Diretiva de Grupo ou o MDM estejam configurados para evitá-lo. Para obter mais informações, confira [configurar e usar o Microsoft Defender SmartScreen em dispositivos individuais](/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-set-individual-device).

## <a name="frequently-asked-questions"></a>Perguntas frequentes

### <a name="how-does-the-reputation-check-system-work"></a>Como funciona o sistema de verificação de reputação?

Enquanto você navega na Web, o Microsoft Defender SmartScreen categoriza sites e downloads como tráfego principal, perigoso ou desconhecido. O tráfego principal são sites populares que o Microsoft Defender SmartScreen determinou serem confiáveis. Se você vai para um site marcado como perigoso, o Microsoft Defender SmartScreen imediatamente o impede de acessar o site. Quando você acessa um site desconhecido, o Microsoft DefenderSmartScreen verifica sua reputação para determinar se você pode acessar o site.

## <a name="see-also"></a>Consulte também

- [Página inicial do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Vídeo: navegação segura no Microsoft Edge](microsoft-edge-video-security-smartscreen.md)
- [Visão geral do Microsoft Defender SmartScreen](/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-overview)
- [Proteção contra ameaças](/windows/security/threat-protection/index)
- [Proteção contra aplicativos potencialmente indesejados](./microsoft-edge-potentially-unwanted-apps.md)