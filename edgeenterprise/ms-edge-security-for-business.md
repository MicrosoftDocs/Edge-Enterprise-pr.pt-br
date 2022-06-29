---
title: Segurança do Microsoft Edge para a sua empresa
ms.author: collw
author: seanongit
manager: chuckf
ms.date: 06/22/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Segurança do Microsoft Edge para a sua empresa
ms.openlocfilehash: 062faede97e8e440b3828158500c40efc688ae7a
ms.sourcegitcommit: ec29195d797cf00c28aef6a80008a62e7fc01be4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/29/2022
ms.locfileid: "12629561"
---
# <a name="microsoft-edge-security-for-your-business"></a>Segurança do Microsoft Edge para a sua empresa

O Microsoft Edge foi criado a partir do projeto de fonte aberta Chromium, que é a base do Google Chrome, o que significa que ele compartilha o design e a mesma arquitetura de segurança bem planejada e bem testada na sua fundação. A história de segurança do Microsoft Edge não para por aqui. Na verdade, o **Microsoft Edge é mais seguro do que o Google Chrome para sua empresa no Windows 10**. Ele tem defesas sofisticadas e avançadas contra phishing e malware, e tem suporte nativo para o isolamento de hardware no Windows 10, não necessitando de nenhum software adicional para alcançar essa linha de base segura. Além disso, quando comparado com o suporte nativo para os serviços de segurança e conformidade do Microsoft 365, o Microsoft Edge traz recursos de segurança e recursos avançados adicionais que ajudam a proteger contra a perda de dados para obter ainda mais benefícios. Para obter mais informações, assista [Vídeo: segurança, compatibilidade e capacidade de gerenciamento do Microsoft Edge](microsoft-edge-video-security-compatibility-manageability.md).

Vamos entrar nos detalhes, começando com as **ameaças externas** e, em seguida, conferimos a **proteção de informações e riscos internos**.

## <a name="external-threat-protection"></a>Proteção contra ameaças externas

### <a name="highest-rated-protection-against-phishing-and-malware"></a>Proteção melhor avaliada contra phishing e malware

Integrado ao Microsoft Edge, o Microsoft Defender SmartScreen bloqueia mais tentativas de [phishing](https://aka.ms/EdgePhishingReport) e [malware](https://aka.ms/EdgeMalwareReport) do que a Navegação Segura do Google Chrome, de acordo com um estudo independente do CyberRatings.org. O Microsoft Defender SmartScreen fornece verificações de reputação em tempo real de sites e downloads à medida que os usuários trabalham online e faz parte do [Microsoft Intelligent Security Graph](https://www.microsoft.com/microsoft-365/windows/intelligent-security), que desenha sinais e insights gerados da grande rede de ativos globais, pesquisadores e parceiros da Microsoft. Executando verificações contra listas dinâmicas e baseadas na nuvem de downloads e sites perigosos, o Microsoft Edge ajuda a detectar e bloquear até mesmo as ameaças indesejadas que desaparecem rapidamente.  

O [Microsoft Edge SmartScreen](/windows/security/threat-protection/microsoft-defender-smartscreen/microsoft-defender-smartscreen-overview) bloqueou 92,3% das tentativas de phishing durante os navegadores da [Web do CyberRatings.org](https://aka.ms/EdgePhishingReport) versus o teste de phishing e 97,4% das tentativas de malware durante o teste de navegadores da [Web do CyberRatings.org vs. Teste de malware](https://aka.ms/EdgeMalwareReport) em comparação com as taxas de Navegação Segura do Chrome de 84,6% e 86,3%, respectivamente.

### <a name="the-only-browser-on-windows-10-that-natively-supports-hardware-isolation"></a>O único navegador no Windows 10 compatível nativamente com isolamento de hardware

O Microsoft Edge é o único navegador no Windows 10 compatível nativamente com os recursos de isolamento de hardware. Como parte do Windows 10 Pro ou Enterprise, o Microsoft Defender Application Guard (Application Guard) executa sites não confiáveis em um kernel isolado no dispositivo local e em redes internas. Os sites não confiáveis são executados em um "contêiner", portanto, quando um ataque surge, ele é colocado em área restrita do restante da rede corporativa. Para obter mais informações, consulte o tópico sobre [Suporte do Microsoft Edge para o Application Guard](./microsoft-edge-security-windows-defender-application-guard.md).

Para o Chrome, uma extensão está disponível para usar Windows 10 de hardware — a extensão MDAG. Em seguida, essa extensão inicia o Microsoft Edge para usar o isolamento no nível de kernel do Application Guard. Além disso, para obter isolamento de nível de kernel semelhante para uma solução somente Chrome, é necessário um software de isolamento de terceiros.

> [!NOTE]
> O Application Guard está disponível no Windows 10, versão 1809 e superior. O Application Guard não está disponível nas edições do Windows 10 Home.

## <a name="internal-risks-and-information-protection"></a>Proteção de informações e riscos internos

### <a name="native-support-for-microsoft-365-security-without-additional-software"></a>Suporte nativo para a segurança do Microsoft 365 sem software adicional

Além da proteção contra ameaças externas, os administradores de TI também devem proteger contra riscos internos. A proteção de dados corporativos confidenciais — robusta e em escala — é a principal prioridade para os administradores de TI, particularmente porque as forças de trabalho se descentralizaram. O Microsoft Edge é o único navegador com suporte nativo para o acesso condicional do Azure AD, a Proteção de Informações do Windows e a nova Proteção contra Perda de Dados de Ponto de Extremidade do Microsoft (DLP), sem necessidade de software adicional.

**O Microsoft Edge é o único navegador que oferece suporte nativo ao acesso condicional**. [O suporte para o acesso condicional no Microsoft Edge](ms-edge-security-conditional-access.md) permite que as organizações usem sinais de identidade como parte de suas decisões de controle de acesso. [O acesso condicional](/azure/active-directory/conditional-access/overview) é a ferramenta usada pelo Azure Active Directory para reunir sinais, para tomar decisões e impor políticas organizacionais. O acesso condicional está no centro do novo plano de controle de identidade controlada. Para obter suporte ao acesso condicional no Chrome, é necessário um plug-in adicional.

> [!NOTE]
> Azure AD acesso condicional requer um Microsoft 365 E3 (ou superior) ou uma Microsoft 365 Business Premium assinatura.

**Microsoft Edge é o único navegador que oferece nativamente suporte à Proteção de Informações do Windows (WIP)**, que fornece proteção aos dados corporativos para ajudar a evitar vazamentos acidentais por usuários em dispositivos Windows 10. [O suporte do Microsoft Edge para a WIP](./microsoft-edge-security-windows-information-protection.md)pode ser configurado para permitir que apenas aplicativos impostos pelo administrador de TI acessem dados corporativos. Ele também oferece controles de vazamento, como a proteção da área de transferência, a criptografia de arquivos no download e a prevenção de carregamentos de arquivos para compartilhamentos de rede não autorizados ou o local da nuvem, com uma experiência de usuário perfeita. A WIP funciona em uma configuração baseada em perímetro, em que os administradores de TI definem o limite corporativo, e todos os dados dentro desse limite são considerados corporativos. O Chrome não é habilitado para WIP com controles de vazamento.

> [!NOTE]
> A configuração de Proteção de Informações do Windows (WIP) exige o licenciamento do Microsoft Intune ou do Microsoft Endpoint Configuration Manager, ou uso de uma solução de gerenciamento de dispositivo móvel (MDM) de terceiros, que pode ter requisitos de licença adicionais.

A **prevenção contra perda de dados do Ponto de extremidade da Microsoft (Endpoint DLP) só tem suporte nativo no Microsoft Edge**. O Ponto de extremidade da DLP integra-se com a Central de Segurança da Microsoft e estende a proteção de informações ao Microsoft Edge para ajudar a alertar os usuários sobre atividades não compatíveis e evitar a perda de dados enquanto os usuários trabalham online. Ela descobre e rotula os dados confidenciais dentro da empresa que correspondem aos critérios definidos pelo administrador, como arquivos que contenham números de cartão de crédito ou identificações governamentais (por exemplo, números de seguridade social), informações financeiras, etc. As políticas de proteção de informações da Microsoft podem ser implantadas no Microsoft Endpoint DLP sem a reconfiguração adicional, incluindo identificadores de conteúdo confidenciais e políticas que os administradores de TI já personalizaram. Essa é uma implantação tranquila da proteção de informações para administradores de TI.

Para saber mais sobre os pré-requisitos de DLP do ponto de extremidade e como configurar a prevenção contra perda de dados, vá para Introdução à prevenção contra perda [de dados do ponto de extremidade](/microsoft-365/compliance/endpoint-dlp-getting-started?preserve-view=true&view=o365-worldwide).

> [!NOTE]
> A prevenção contra perda de dados do Microsoft Endpoint requer Microsoft 365 E5, um Microsoft 365 E5 Compliance ou uma Microsoft 365 Business Premium assinatura.

## <a name="see-also"></a>Consulte também

- [Página inicial do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Vídeo: segurança, compatibilidade e capacidade de gerenciamento do Microsoft Edge](microsoft-edge-video-security-compatibility-manageability.md)
