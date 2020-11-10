---
title: Segurança do Microsoft Edge para a sua empresa
ms.author: seanlynd
author: seanongit
manager: chuckf
ms.date: 11/09/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Segurança do Microsoft Edge para a sua empresa
ms.openlocfilehash: 465dbc2a7e90d205630f559d8a7b7d582f0467ae
ms.sourcegitcommit: 10e18ce8a9585bb54c2716939fce93e1c6e708fd
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/09/2020
ms.locfileid: "11160950"
---
# Segurança do Microsoft Edge para a sua empresa

O Microsoft Edge foi criado a partir do projeto de fonte aberta Chromium, que é a base do Google Chrome, o que significa que ele compartilha o design e a mesma arquitetura de segurança bem planejada e bem testada na sua fundação. A história de segurança do Microsoft Edge não para por aqui. Na verdade, o **Microsoft Edge é mais seguro do que o Google Chrome para sua empresa no Windows 10**. Ele tem defesas sofisticadas e avançadas contra phishing e malware, e tem suporte nativo para o isolamento de hardware no Windows 10, não necessitando de nenhum software adicional para alcançar essa linha de base segura. Além disso, quando comparado com o suporte nativo para os serviços de segurança e conformidade do Microsoft 365, o Microsoft Edge traz recursos de segurança e recursos avançados adicionais que ajudam a proteger contra a perda de dados para obter ainda mais benefícios.

Vamos entrar nos detalhes, começando com as ameaças externas e, em seguida, conferimos a **proteção de informações e riscos internos**.

## Proteção contra ameaças externas

### Proteção melhor avaliada contra phishing e malware

Desenvolvido no Microsoft Edge, o SmartScreen bloqueia as tentativas de phishing e malware mais do que a Navegação Segura do Google Chrome, de acordo com um [estudo independente dos laboratórios do NSS](https://www.nsslabs.com/tested-technologies/web-browser-security-wbs/). O SmartScreen fornece verificações de reputação de sites e downloads em tempo real à medida que os usuários trabalham online, e faz parte do [Gráfico de Segurança Inteligente da Microsoft](https://www.microsoft.com/microsoft-365/windows/intelligent-security), que desenha sinais e percepções geradas na grande rede de ativos, pesquisadores e parceiros global do Microsoft. Executando verificações contra listas dinâmicas e baseadas na nuvem de downloads e sites perigosos, o Microsoft Edge ajuda a detectar e bloquear até mesmo as ameaças indesejadas que desaparecem rapidamente.  

O [Microsoft Edge com SmartScreen](https://docs.microsoft.com//DeployEdge/microsoft-edge-security-smartscreen) bloqueou 95,5% das tentativas de phishing e 98,5% de tentativas de malware [durante os testes de laboratório do NSS](https://www.nsslabs.com/tested-technologies/web-browser-security-wbs/) em comparação com as taxas da Navegação Segura do Chrome de 86,9% e 86,0%, respectivamente.

### O único navegador no Windows 10 compatível nativamente com isolamento de hardware

O Microsoft Edge é o único navegador no Windows 10 compatível nativamente com os recursos de isolamento de hardware. Como parte do Windows 10 Pro ou Enterprise, o Microsoft Defender Application Guard (Application Guard) executa sites não confiáveis em um kernel isolado no dispositivo local e em redes internas. Os sites não confiáveis são executados em um "contêiner", portanto, quando surge um ataque, ele fica na área restrita do restante da rede corporativa. Para obter mais informações, consulte o tópico sobre [Suporte do Microsoft Edge para o Application Guard](https://docs.microsoft.com/DeployEdge/microsoft-edge-security-windows-defender-application-guard).

Para o Chrome, uma extensão está disponível para aproveitar o isolamento de hardware do Windows 10, a extensão MDAG. Essa extensão então inicializa o Microsoft Edge para aproveitar o isolamento de nível kernel do Application Guard. Além disso, para obter isolamento de nível de kernel semelhante para uma solução única do Chrome, é necessário um software de isolamento de terceiros.

> [!NOTE]
> O Application Guard está disponível no Windows 10, versão 1809 e superior. O Application Guard não está disponível nas edições do Windows 10 Home.

## Proteção de informações e riscos internos

### Suporte nativo para a segurança do Microsoft 365 sem software adicional

Além da proteção contra ameaças externas, os administradores de TI também devem proteger contra riscos internos. A proteção de dados corporativos confidenciais — robusta e em escala — é a principal prioridade para os administradores de TI, particularmente porque as forças de trabalho se descentralizaram. O Microsoft Edge é o único navegador com suporte nativo para o acesso condicional do Azure AD, a Proteção de Informações do Windows e a nova Proteção contra Perda de Dados de Ponto de Extremidade do Microsoft (DLP), sem necessidade de software adicional.

**O Microsoft Edge é o único navegador que oferece suporte nativo ao acesso condicional**. [O suporte para o acesso condicional no Microsoft Edge](ms-edge-security-conditional-access.md) permite que as organizações usem sinais de identidade como parte de suas decisões de controle de acesso. [O acesso condicional](https://docs.microsoft.com/azure/active-directory/conditional-access/overview) é a ferramenta usada pelo Azure Active Directory para reunir sinais, para tomar decisões e impor políticas organizacionais. O acesso condicional está no centro do novo plano de controle de identidade controlada. Para obter suporte ao acesso condicional no Chrome, é necessário um plug-in adicional.

> [!NOTE]
> É necessária uma assinatura do Microsoft 365 E3 ou superior para o acesso condicional do Azure AD.

**Microsoft Edge é o único navegador que oferece nativamente suporte à Proteção de Informações do Windows (WIP)**, que fornece proteção aos dados corporativos para ajudar a evitar vazamentos acidentais por usuários em dispositivos Windows 10. [O suporte do Microsoft Edge para a WIP](https://docs.microsoft.com/DeployEdge/microsoft-edge-security-windows-information-protection)pode ser configurado para permitir que apenas aplicativos impostos pelo administrador de TI acessem dados corporativos. Ele também oferece controles de vazamento, como a proteção da área de transferência, a criptografia de arquivos no download e a prevenção de carregamentos de arquivos para compartilhamentos de rede não autorizados ou o local da nuvem, com uma experiência de usuário perfeita. A WIP funciona em uma configuração baseada em perímetro, em que os administradores de TI definem o limite corporativo, e todos os dados dentro desse limite são considerados corporativos. O Chrome não é esclarecido no WIP com controles de vazamento.

> [!NOTE]
> A configuração de Proteção de Informações do Windows (WIP) exige o licenciamento do Microsoft Intune ou do Microsoft Endpoint Configuration Manager, ou uso de uma solução de gerenciamento de dispositivo móvel (MDM) de terceiros, que pode ter requisitos de licença adicionais.

**O Microsoft Endpoint DLP somente será suportado nativamente no Microsoft Edge. (O Microsoft Endpoint DLP está atualmente em fase de visualização pública e espera-se que esteja disponível em geral ainda em 2020).**. A Proteção contra Perda de Dados de Ponto de Extremidade do Microsoft (DLP) integra o centro de segurança do Microsoft e amplia a proteção de informações para o Microsoft Edge para ajudar os usuários de atividade não compatível e evitar a perda de dados quando os usuários trabalham online. Ela descobre e rotula os dados confidenciais dentro da empresa que correspondem aos critérios definidos pelo administrador, como arquivos que contenham números de cartão de crédito ou identificações governamentais (por exemplo, números de seguridade social), informações financeiras, etc. As políticas de proteção de informações da Microsoft podem ser implantadas no Microsoft Endpoint DLP sem a reconfiguração adicional, incluindo identificadores de conteúdo confidenciais e políticas que os administradores de TI já personalizaram. Essa é uma implantação tranquila da proteção de informações para administradores de TI.

> [!NOTE]
> A assinatura do Microsoft 365 E5 Compliance ou Microsoft 365 E5 Compliance é necessária para a Proteção contra Perda de Dados de Ponto de Extremidade do Microsoft.

## Consulte também

- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
