---
title: Microsoft Edge e Microsoft Defender Application Guard
ms.author: srugh
author: dan-wesley
manager: seanlyn
ms.date: 06/19/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Suporte do Microsoft Edge para o Windows Defender Application Guard
ms.openlocfilehash: 7bd2efd35e0cd65c524a17a88f659e9b3838233f
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979158"
---
# Suporte do Microsoft Edge para o Windows Defender Application Guard

Este artigo descreve como o Microsoft Edge oferece suporte para o Windows Defender Application Guard (Application Guard).

> [!NOTE]
> Este artigo se aplica ao Microsoft Edge versão 77 ou posterior.

## Visão geral

Os arquitetos de segurança na empresa devem lidar com a tensão que existe entre a produtividade e a segurança. É muito fácil bloquear um navegador e permitir que apenas alguns sites confiáveis sejam carregados. Essa abordagem melhorará a postura geral de segurança, mas será menos produtiva. Se você a fizer menos restritiva para melhorar a produtividade, aumentará o perfil de risco. É um equilíbrio difícil de alcançar!

É ainda mais difícil acompanhar as novas ameaças emergentes neste cenário de ameaças em constante mudança. Os navegadores continuam sendo a principal superfície de ataque em dispositivos cliente atuais, pois seu trabalho fundamental é permitir que os usuários acessem, baixem e abram conteúdo não confiável de fontes não confiáveis. Os indivíduos mal intencionados estão constantemente trabalhando com novas formas de ataques de engenharia social para navegadores. As estratégias de prevenção ou de detecção/resposta de incidentes de segurança não podem garantir 100% da segurança.

Uma estratégia de segurança principal é a [Assume Breach Methodology](https://docs.microsoft.com/office365/Enterprise/office-365-monitoring-and-testing#assume-breach-methodology), que significa que existe uma aceitação de que um ataque vai acontecer pelo menos uma vez, independente dos esforços para impedi-lo. Essa mentalidade exige a criação de defesas para conter o dano, o que garante que a rede corporativa e outros recursos permaneçam protegidos neste cenário.  A implantação do Application Guard para o Microsoft Edge se encaixa nesta estratégia.

## Sobre o Application Guard

Projetado para o Windows 10 e o Microsoft Edge, o Application Guard usa uma abordagem de isolamento de hardware. Essa abordagem permite a inicialização da navegação de um site não confiável dentro de um contêiner. O isolamento de hardware ajuda as empresas a proteger seus dados e redes corporativas no caso de os usuários visitarem um site comprometido ou mal-intencionado.

O administrador corporativo define quais são os sites, recursos de nuvem e redes internas confiáveis. Tudo que não está na lista de sites confiáveis é considerado não confiável. Esses sites são isolados da rede corporativa e dos dados do dispositivo do usuário.

Para mais informação, confira [O que é o Application Guard e como ele funciona?](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-application-guard/md-app-guard-overview#what-is-application-guard-and-how-does-it-work).

A próxima captura de tela mostra um exemplo de mensagem do Application Guard que mostra que o usuário está navegando em um espaço seguro.

![Mensagem de navegação segura do Application Guard](media/microsoft-edge-security-windows-defender-application-guard/wd-application-guard-1.png)

## Novidades

O suporte do Application Guard no novo navegador Microsoft Edge tem paridade funcional com o Microsoft Edge herdado e inclui vários aperfeiçoamentos.

### Suporte à extensão dentro do contêiner

O suporte à extensão dentro do contêiner tem sido uma das principais solicitações dos clientes. Os cenários variaram de querer executar bloqueadores de anúncios dentro do contêiner para melhorar o desempenho do navegador a ter a habilidade de executar extensões personalizadas dentro do contêiner.

As instalações de extensão no contêiner agora têm suporte, começando pela versão 81 do Microsoft Edge. Este suporte pode ser controlado pela política. O  que é usado na política de [ExtensionInstallForcelist](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#extensioninstallforcelist) deve ser adicionado como um recurso neutro nas políticas de isolamento de rede usadas pelo Application Guard.

Alguns exemplos de suporte a contêiner incluem os seguintes cenários:

- Forçar instalações de uma extensão no host
- Remover uma extensão do host
- Extensões bloqueadas no host

> [!NOTE]
> Também é possível instalar manualmente as extensões individuais dentro do contêiner do armazenamento da extensão. As extensões instaladas manualmente só persistirão no contêiner quando a política [Permitir a persistência](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-application-guard/configure-md-app-guard#application-specific-settings) estiver ativada.

### Identificação do tráfego do Application Guard por Proxy Duplo

Alguns clientes corporativos estão implantando o Application Guard usando um caso de uso específico, em que é necessário identificar o tráfego da Web vindo de um contêiner do Microsoft Defender Application Guard no nível do proxy. A partir da versão 84 do Canal Estável, o Microsoft Edge será compatível com o proxy duplo para atender a essa necessidade. Você pode configurar essa funcionalidade usando a política [ApplicationGuardContainerProxy](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#applicationguardcontainerproxy).

O desenho a seguir mostra a arquitetura de proxy duplo do Microsoft Edge.

![Arquitetura de proxy duplo para o Application Guard](media/microsoft-edge-security-windows-defender-application-guard/wd-application-guard-dual-proxy.png)

### Página de diagnóstico para solução de problemas

Outro ponto de preocupação do usuário é solucionar problemas de configuração do Application Guard em um dispositivo quando um problema for relatado. O Microsoft Edge tem uma página de diagnóstico (`edge://application-guard-internals`) para solucionar problemas do usuário. Um destes diagnósticos é a capacidade de verificar a confiança da URL com base na configuração do dispositivo do usuário.

A próxima captura de tela mostra uma página de diagnóstico de várias guias para ajudá-lo a diagnosticar problemas relatados pelos usuários no dispositivo.

![Página de diagnóstico do Application Guard](media/microsoft-edge-security-windows-defender-application-guard/wd-application-guard-2.png)

### Atualizações do Microsoft Edge no contêiner

As atualizações herdadas do Microsoft Edge no contêiner fazem parte do ciclo de atualização do sistema operacional Windows. Como a nova versão do Microsoft Edge se atualiza independente do sistema operacional Windows, não há mais dependências nas atualizações do contêiner. O canal e a versão do host Microsoft Edge são replicados dentro do contêiner.

## Pré-requisitos

Os seguintes requisitos se aplicam aos dispositivos usando o Application Guard com o Microsoft Edge:

- Windows 10 1809 (RS5) e superior.
- Somente SKUs de clientes Windows

  > [!NOTE]
  > O Application Guard tem suporte apenas em SKUs do Windows 10 Pro e Windows 10 Enterprise.

- Uma das soluções de gerenciamento descritas nos [Requisitos do software](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-application-guard/reqs-md-app-guard#software-requirements)

## Como instalar o Application Guard

Os artigos a seguir fornecem as informações necessárias para instalar, configurar e testar o Application Guard com o Microsoft Edge.

- [Requisitos de sistema](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-application-guard/reqs-md-app-guard)
- [Instalar o Microsoft Defender Application Guard](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-application-guard/install-md-app-guard)
- [Configurar as políticas de grupo do Windows Defender](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-application-guard/configure-md-app-guard)
- [Testar o Application Guard](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-application-guard/test-scenarios-md-app-guard)

## Perguntas frequentes

### O Application Guard funciona no modo IE?

O modo IE é compatível com a funcionalidade do Application Guard, mas não prevemos muito o uso desse recurso no modo do IE. O modo IE deve ser implantado para uma lista de sites internos confiáveis e o Application Guard destina-se apenas a sites não confiáveis. Certifique-se de que todos os sites do modo IE ou os endereços IP também sejam adicionados à política de isolamento de rede a ser considerada um recurso confiável pelo Application Guard.

### Preciso instalar a extensão do Chrome do Application Guard?

Não, o recurso Application Guard tem suporte nativo no Microsoft Edge. Na verdade, não há suporte para a extensão de Chrome do Application Guard no Microsoft Edge.

### Há outras perguntas frequentes relacionadas a plataformas?

Sim. [Perguntas frequentes - Microsoft Defender Application Guard](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-application-guard/faq-md-app-guard) 

## Consulte também

- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Visão geral da segurança](security-overview.md)
- [Proteção Avançada contra Ameaças do Microsoft Defender](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/microsoft-defender-advanced-threat-protection)
