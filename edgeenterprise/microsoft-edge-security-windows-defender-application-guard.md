---
title: Microsoft Edge e Microsoft Defender Application Guard
ms.author: srugh
author: AndreaLBarr
manager: seanlyn
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Suporte do Microsoft Edge para o Windows Defender Application Guard
ms.openlocfilehash: 4d9f5b0590199a9938b19e60fdd38e7c0098ac76
ms.sourcegitcommit: 51a858ee4b1f837df85dbcca335f4abebae7771b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2021
ms.locfileid: "11925987"
---
# <a name="microsoft-edge-support-for-microsoft-defender-application-guard"></a>Suporte do Microsoft Edge para o Windows Defender Application Guard

Este artigo descreve como o Microsoft Edge oferece suporte para o Windows Defender Application Guard (Application Guard).

> [!NOTE]
> Este artigo se aplica ao Microsoft Edge versão 77 ou posterior.

## <a name="overview"></a>Visão geral

Os arquitetos de segurança na empresa devem lidar com a tensão que existe entre a produtividade e a segurança. É muito fácil bloquear um navegador e permitir que apenas alguns sites confiáveis sejam carregados. Essa abordagem melhorará a postura geral de segurança, mas será menos produtiva. Se você a fizer menos restritiva para melhorar a produtividade, aumentará o perfil de risco. É um equilíbrio difícil de alcançar!

É ainda mais difícil acompanhar as novas ameaças emergentes neste cenário de ameaças em constante mudança. Os navegadores continuam sendo a principal superfície de ataque em dispositivos cliente atuais, pois seu trabalho fundamental é permitir que os usuários acessem, baixem e abram conteúdo não confiável de fontes não confiáveis. Os indivíduos mal intencionados estão constantemente trabalhando com novas formas de ataques de engenharia social para navegadores. As estratégias de prevenção ou de detecção/resposta de incidentes de segurança não podem garantir 100% da segurança.

Uma estratégia de segurança principal é a [Assume Breach Methodology](/office365/Enterprise/office-365-monitoring-and-testing#assume-breach-methodology), que significa que existe uma aceitação de que um ataque vai acontecer pelo menos uma vez, independente dos esforços para impedi-lo. Essa mentalidade exige a criação de defesas para conter o dano, o que garante que a rede corporativa e outros recursos permaneçam protegidos neste cenário.  A implantação do Application Guard para o Microsoft Edge se encaixa nesta estratégia.

## <a name="about-application-guard"></a>Sobre o Application Guard

Projetado para o Windows 10 e o Microsoft Edge, o Application Guard usa uma abordagem de isolamento de hardware. Essa abordagem permite a inicialização da navegação de um site não confiável dentro de um contêiner. O isolamento de hardware ajuda as empresas a proteger seus dados e redes corporativas no caso de os usuários visitarem um site comprometido ou mal-intencionado.

O administrador corporativo define quais são os sites, recursos de nuvem e redes internas confiáveis. Tudo que não está na lista de sites confiáveis é considerado não confiável. Esses sites são isolados da rede corporativa e dos dados do dispositivo do usuário.

Para saber mais:

- Assista o nosso vídeo [Isolamento do navegador Microsoft Edge usando o Application Guard](microsoft-edge-video-security-application-guard.md)
- Leia [O que é o Application Guard e como ele funciona?](/windows/security/threat-protection/microsoft-defender-application-guard/md-app-guard-overview#what-is-application-guard-and-how-does-it-work)

A próxima captura de tela mostra um exemplo de mensagem do Application Guard que mostra que o usuário está navegando em um espaço seguro.

![Mensagem de navegação segura do Application Guard](media/microsoft-edge-security-windows-defender-application-guard/wd-application-guard-1.png)

## <a name="whats-new"></a>Novidades

O suporte do Application Guard no novo navegador Microsoft Edge tem paridade funcional com a Versão Prévia do Microsoft Edge e inclui vários aperfeiçoamentos.

### <a name="enable-application-guard-in-passive-mode-and-browse-edge-normally"></a>Habilitar o Application Guard no modo passivo e procurar Borda normalmente

A partir Microsoft Edge 94, os usuários agora têm a opção de configurar o modo passivo, o que significa que o Application Guard ignora a configuração da lista de sites e os usuários podem navegar no Edge normalmente. Este suporte pode ser controlado pela política. Você pode atualizar a política de borda [ApplicationGuardPassiveModeEnabled](/deployedge/microsoft-edge-policies#applicationguardpassivemodeenabled) para habilitar ou desabilitar o modo passivo.

> [!Note]
> Essa política AFETA SOMENTE o Edge, portanto, as navegação de outros navegadores podem ser redirecionadas para o Contêiner do Application Guard se você tiver as extensões correspondentes habilitadas.

### <a name="favorites-synchronizing-from-the-host-to-the-container"></a>Favoritos sincronizando do host para o contêiner

Alguns de nossos clientes estão solicitando a sincronização de favoritos entre o navegador host e o contêiner no Application Guard. A partir do Microsoft Edge 91, os usuários agora têm a opção de configurar o Application Guard para sincronizar seus favoritos do host para o contêiner. Isso garante que novos favoritos também apareçam no contêiner.

Este suporte pode ser controlado pela política. Você pode atualizar a política do Microsoft Edge [ApplicationGuardFavoritesSyncEnabled](/deployedge/microsoft-edge-policies#applicationguardfavoritessyncenabled) para habilitar ou desabilitar a sincronização de favoritos.

> [!Note]
> Por motivos de segurança, a sincronização de favoritos só é possível do host para o contêiner e não o contrário. Para garantir uma lista unificada de favoritos no host e no contêiner, desabilitamos o gerenciamento de favoritos dentro do contêiner.

### <a name="identify-network-traffic-originating-from-the-container"></a>Identificar o tráfego de rede proveniente do contêiner

Vários clientes estão usando o WDAG em uma configuração específica em que eles querem identificar o tráfego de rede proveniente do contêiner. Alguns dos cenários para isso são:

- Para restringir o acesso a apenas alguns sites não confiáveis
- Para permitir o acesso à Internet somente do contêiner

A partir do Microsoft Edge versão 91, há suporte integrado para marcar o tráfego de rede originado de contêineres do Application Guard, permitindo que as empresas usem proxy para filtrar o tráfego e aplicar políticas específicas. Você pode usar o cabeçalho para identificar qual tráfego está por meio do contêiner ou do host usando [ApplicationGuardTrafficIdentificationEnabled](/deployedge/microsoft-edge-policies#applicationguardtrafficidentificationenabled).

### <a name="extension-support-inside-the-container"></a>Suporte à extensão dentro do contêiner

O suporte à extensão dentro do contêiner tem sido uma das principais solicitações dos clientes. Os cenários variaram de querer executar bloqueadores de anúncios dentro do contêiner para melhorar o desempenho do navegador a ter a habilidade de executar extensões personalizadas dentro do contêiner.

As instalações de extensão no contêiner agora têm suporte, começando pela versão 81 do Microsoft Edge. Este suporte pode ser controlado pela política. O  que é usado na política de [ExtensionInstallForcelist](./microsoft-edge-policies.md#extensioninstallforcelist) deve ser adicionado como um recurso neutro nas políticas de isolamento de rede usadas pelo Application Guard.

Alguns exemplos de suporte a contêiner incluem os seguintes cenários:

- Forçar instalações de uma extensão no host
- Remover uma extensão do host
- Extensões bloqueadas no host

> [!NOTE]
> Também é possível instalar manualmente as extensões individuais dentro do contêiner do armazenamento da extensão. As extensões instaladas manualmente só persistirão no contêiner quando a política [Permitir a persistência](/windows/security/threat-protection/microsoft-defender-application-guard/configure-md-app-guard#application-specific-settings) estiver ativada.

### <a name="identifying-application-guard-traffic-via-dual-proxy"></a>Identificação do tráfego do Application Guard por Proxy Duplo

Alguns clientes corporativos estão implantando o Application Guard usando um caso de uso específico, em que é necessário identificar o tráfego da Web vindo de um contêiner do Microsoft Defender Application Guard no nível do proxy. A partir da versão 84 do Canal Estável, o Microsoft Edge será compatível com o proxy duplo para atender a essa necessidade. Você pode configurar essa funcionalidade usando a política [ApplicationGuardContainerProxy](./microsoft-edge-policies.md#applicationguardcontainerproxy).

O desenho a seguir mostra a arquitetura de proxy duplo do Microsoft Edge.

![Arquitetura de proxy duplo para o Application Guard](media/microsoft-edge-security-windows-defender-application-guard/wd-application-guard-dual-proxy.png)

### <a name="diagnostic-page-for-troubleshooting"></a>Página de diagnóstico para solução de problemas

Outro ponto de preocupação do usuário é solucionar problemas de configuração do Application Guard em um dispositivo quando um problema for relatado. O Microsoft Edge tem uma página de diagnóstico (`edge://application-guard-internals`) para solucionar problemas do usuário. Um destes diagnósticos é a capacidade de verificar a confiança da URL com base na configuração do dispositivo do usuário.

A próxima captura de tela mostra uma página de diagnóstico de várias guias para ajudá-lo a diagnosticar problemas relatados pelos usuários no dispositivo.

![Página de diagnóstico do Application Guard](media/microsoft-edge-security-windows-defender-application-guard/wd-application-guard-2.png)

### <a name="microsoft-edge-updates-in-the-container"></a>Atualizações do Microsoft Edge no contêiner

As atualizações herdadas do Microsoft Edge no contêiner fazem parte do ciclo de atualização do sistema operacional Windows. Como a nova versão do Microsoft Edge se atualiza independente do sistema operacional Windows, não há mais dependências nas atualizações do contêiner. O canal e a versão do host Microsoft Edge são replicados dentro do contêiner.

## <a name="prerequisites"></a>Pré-requisitos

Os seguintes requisitos se aplicam aos dispositivos usando o Application Guard com o Microsoft Edge:

- Windows 10 1809 (RS5) e superior.
- Somente SKUs de clientes Windows

  > [!NOTE]
  > O Application Guard tem suporte apenas em SKUs do Windows 10 Pro e Windows 10 Enterprise.

- Uma das soluções de gerenciamento descritas nos [Requisitos do software](/windows/security/threat-protection/microsoft-defender-application-guard/reqs-md-app-guard#software-requirements)

## <a name="how-to-install-application-guard"></a>Como instalar o Application Guard

Os artigos a seguir fornecem as informações necessárias para instalar, configurar e testar o Application Guard com o Microsoft Edge.

- [Requisitos de sistema](/windows/security/threat-protection/microsoft-defender-application-guard/reqs-md-app-guard)
- [Instalar o Microsoft Defender Application Guard](/windows/security/threat-protection/microsoft-defender-application-guard/install-md-app-guard)
- [Configurar as políticas de grupo do Windows Defender](/windows/security/threat-protection/microsoft-defender-application-guard/configure-md-app-guard)
- [Testar o Application Guard](/windows/security/threat-protection/microsoft-defender-application-guard/test-scenarios-md-app-guard)

## <a name="frequently-asked-questions"></a>Perguntas Frequentes

### <a name="does-application-guard-work-in-ie-mode"></a>O Application Guard funciona no modo IE?

O modo IE dá suporte à funcionalidade do Application Guard, mas não antecipamos muito uso desse recurso no modo IE. O modo IE é recomendado para ser implantado para uma lista de sites internos confiáveis, e o Application Guard é apenas para sites não confiáveis. Certifique-se de que todos os sites do modo IE ou os endereços IP também sejam adicionados à política de isolamento de rede a ser considerada um recurso confiável pelo Application Guard.

### <a name="do-i-need-to-install-the-application-guard-chrome-extension"></a>Preciso instalar a extensão do Chrome do Application Guard?

Não, o recurso Application Guard tem suporte nativo no Microsoft Edge. Na verdade, não há suporte para a extensão de Chrome do Application Guard no Microsoft Edge.

### <a name="can-employees-download-documents-from-the-application-guard-edge-session-onto-host-devices"></a>Os funcionários podem baixar documentos da sessão Application Guard Edge nos dispositivos host?

Na Windows 10 Enterprise, versão 1803, os usuários podem baixar documentos do contêiner isolado do Application Guard para o computador host. Esse recurso é gerenciado pela política.

Na Windows 10 Enterprise, versão 1709 ou Windows 10 Professional, versão 1803, não é possível baixar arquivos do contêiner isolado do Application Guard para o computador host. No entanto, os funcionários podem usar as opções Imprimir em PDF ou Imprimir como XPS e salvar esses arquivos no dispositivo host.

### <a name="can-employees-copy-and-paste-between-the-host-device-and-the-application-guard-edge-session"></a>Os funcionários podem copiar e colar entre o dispositivo host e a sessão Application Guard Edge?

Dependendo das configurações da sua organização, os funcionários podem copiar e colar imagens (.bmp) e texto de e para o contêiner isolado.

### <a name="why-dont-employees-see-their-favorites-in-the-application-guard-edge-session"></a>Por que os funcionários não veem seus favoritos na sessão de Borda do Application Guard?

Dependendo das configurações da sua organização, pode ser que a Sincronização de Favoritos está desligada. Para gerenciar a política, consulte: Microsoft Edge e Microsoft Defender Application Guard | Microsoft Docs.

### <a name="why-arent-employees-able-to-see-their-extensions-in-the-application-guard-edge-session"></a>Por que os funcionários não conseguem ver suas extensões na sessão de Borda do Application Guard?

Certifique-se de habilitar a política de extensões na configuração do Application Guard.

### <a name="my-extension-doesnt-seem-to-work-in-edge-application-guard"></a>Minha extensão não parece funcionar no Edge Application Guard?

Se a política de extensões estiver habilitada para o MDAG na configuração, verifique se sua extensão requer componentes de Tratamento de Mensagens Nativas, essas extensões não são suportadas no contêiner do Application Guard.

### <a name="im-trying-to-watch-playback-video-with-hdr-why-is-the-hdr-option-missing"></a>Estou tentando ver vídeo de reprodução com HDR, por que a opção HDR está ausente?

Para que a reprodução de vídeo HDR funcione no contêiner, a Aceleração de Hardware vGPU precisa ser habilitada no Application Guard.

### <a name="are-there-any-other-platform-related-faqs"></a>Há outras perguntas frequentes relacionadas a plataformas?

Sim. [Perguntas frequentes - Microsoft Defender Application Guard](/windows/security/threat-protection/microsoft-defender-application-guard/faq-md-app-guard) 

## <a name="see-also"></a>Consulte também

- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Proteção Avançada contra Ameaças do Microsoft Defender](/windows/security/threat-protection/microsoft-defender-atp/microsoft-defender-advanced-threat-protection)
- [Vídeo: Isolamento de navegador Microsoft Edge usando o Application Guard](https://www.youtube.com/watch?v=zQjaRqNXMqw&t=3s)
