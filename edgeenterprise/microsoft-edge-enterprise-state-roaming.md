---
title: Microsoft Edge e Enterprise State Roaming
ms.author: kvice
author: dan-wesley
manager: laurawi
ms.date: 05/31/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Microsoft Edge e Enterprise State Roaming
ms.openlocfilehash: 154e0d0a70412e25058c27b6b1f7f5fbd2699fa5
ms.sourcegitcommit: b8ce42bb539f74a93f1e66497e3b6f6f076e0c2a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/01/2022
ms.locfileid: "12555344"
---
# <a name="microsoft-edge-and-enterprise-state-roaming"></a>Microsoft Edge e Enterprise State Roaming

Este artigo explica como a participação do Microsoft Edge na oferta do Enterprise State Roaming (ESR) está mudando para oferecer um suporte melhor à sincronização entre plataformas e dispositivos.

> [!NOTE]
> Este artigo se aplica ao Microsoft Edge versão 77 ou posterior, a menos que indicado de outra forma.

## <a name="introduction"></a>Introdução

Com o Windows 10, os usuários do [Azure Active Directory (Azure AD)](/azure/active-directory/fundamentals/active-directory-whatis) têm a possibilidade de sincronizar de maneira segura as configurações de usuário e os dados das configurações do aplicativo com a nuvem. O [Enterprise State Roaming (ESR)](/azure/active-directory/devices/enterprise-state-roaming-overview) oferece aos usuários uma experiência unificada em todos os dispositivos Windows e reduz o tempo necessário para configurar um novo dispositivo.

Como resultado da adoção Microsoft Edge plataforma Chromium, sua solução de sincronização agora está desconectada Windows estrutura de sincronização. Essa desconexão afeta a relação de Microsoft Edge com a oferta de ESR.

> [!IMPORTANT]
> Microsoft Edge não participa da oferta de ESR.

## <a name="whats-changing-with-microsoft-edge"></a>O que mudará no Microsoft Edge?

Com Microsoft Edge, a solução de sincronização não está vinculada ao ecossistema de Windows sincronização. Essa solução de sincronização nos permite oferecer Microsoft Edge em todas as plataformas, como Windows 7, Windows 8.1, iOS, Android e macOS. Também podemos oferecer sincronização para contas não primárias no Windows. Além disso, podemos fornecer o Microsoft Edge em uma cadência de lançamento mais frequente e flexível que a do Windows. (Para obter mais informações, consulte [Atualizações do Windows para oferecer suporte à próxima versão do Microsoft Edge](microsoft-edge-sysupdate-windows-updates.md). Todos esses fatores realçam a necessidade de reavaliar Microsoft Edge participação na oferta de ESR.

O ESR é enquadrado como uma oferta de produto Windows com promessas sobre como os dados de dispositivos Windows são tratados, mas Microsoft Edge sincronização estenderá essa funcionalidade além de Windows dispositivos. Como os dados se movem entre esses dispositivos, fica difícil definir a oferta de Microsoft Edge de sincronização no contexto do ESR. Para simplificar a maneira como a sincronização funciona e é gerenciada, e para acomodar as alterações destacadas, foi tomada a decisão de tirar o Microsoft Edge da oferta de ESR.

## <a name="does-this-mean-that-enterprises-will-lose-the-abilities-they-had-as-part-of-esr"></a>Isso significa que as empresas perderão as habilidades que tinham como parte da ESR?

Não. O Microsoft Edge continuará dando suporte à maioria das capacidades fornecidas na oferta de ESR.

### <a name="unified-experience-across-devices-and-new-device-configuration-time"></a>Experiência unificada entre dispositivos e novo tempo de configuração de dispositivo

Quando um usuário se conecta ao seu dispositivo Windows com uma conta do Azure Active Directory (AAD), o Microsoft Edge herda implicitamente essa identidade na primeira inicialização do novo navegador.

Depois que um usuário consentir explicitamente em ativar a sincronização no Microsoft Edge, o navegador sincronizará todos os dados do navegador, como favoritos, senhas e histórico. A sincronização garante uma experiência unificada entre dispositivos e reduz o tempo necessário para personalizar o navegador.

### <a name="separation-of-corporate-and-consumer-data"></a>Separação de dados corporativos e do consumidor

As organizações estão no controle de seus dados e não há nenhuma combinação de dados corporativos em uma conta de nuvem de consumidor ou dados de consumidor em uma conta de nuvem corporativa.

### <a name="enhanced-security"></a>Segurança reforçada

Os dados são criptografados automaticamente antes de saírem do dispositivo Windows 10 do usuário usando a Proteção de Informações do Azure, e os dados permanecem criptografados em repouso na nuvem. Todo o conteúdo continua criptografado em repouso na nuvem, exceto os namespaces, como nomes de configurações.

### <a name="monitoring"></a>Monitoramento

Forneceremos controle e visibilidade sobre quem sincroniza as configurações em sua organização e em quais dispositivos por meio da integração com o portal do Azure AD. Essa funcionalidade será habilitada em uma versão futura.

### <a name="management"></a>Gerenciamento

Os administradores poderão controlar quais membros em sua organização podem habilitar a sincronização. Consulte [Usar a Proteção de Informações do Azure para configurar Microsoft Edge sincronizar](microsoft-edge-enterprise-sync.md#use-azure-information-protection-to-configure-microsoft-edge-sync) e [sincronizar políticas de grupo](microsoft-edge-enterprise-sync.md#sync-group-policies). Além disso, os usuários podem ativar/desativar a sincronização para cada um de seus dispositivos e alternar cada atributo de dados individualmente para sincronização.

### <a name="key-management"></a>Gerenciamento de chaves

O recurso de sincronização usa a AIP (Proteção de Informações do Azure) para proteger os dados sincronizados apenas para o usuário e os administradores corporativos. A AIP dá suporte a chaves gerenciadas da Microsoft (padrão) e traga sua própria chave para o gerenciamento de chaves de nuvem. A estratégia de gerenciamento de chaves na nuvem usada por sua organização é transparente para o Microsoft Edge e não tem impacto sobre o recurso de sincronização.

> [!IMPORTANT]
> O método [Mantenha sua própria chave (HYOK)](/azure/information-protection/configure-adrms-restrictions) e o Active Directory Rights Management Services não têm suporte.

## <a name="summary-of-sync-attributes"></a>Resumo dos atributos de sincronização

Os seguintes atributos de dados serão sincronizados na nova versão do Microsoft Edge na primeira inicialização:

- Favoritos
- Senhas
- Endereços e etc. (preenchimento de formulário)
- Coleções
- Configurações
- Extensões
- Abrir guias (disponível no Microsoft Edge versão 88 ou posterior)
- Histórico (disponível na versão Microsoft Edge 88 ou posterior)

A lista anterior de atributos é diferente dos atributos que podem ser sincronizados no Microsoft Edge Legacy. (Para obter detalhes sobre as configurações do Microsoft Edge Legacy, consulte [Configurações de roaming do Windows 10](/azure/active-directory/devices/enterprise-state-roaming-windows-settings-reference).) Os usuários podem habilitar/desabilitar esses atributos seletivamente usando as configurações do Microsoft Edge. Devido à diferença de atributos entre as duas versões (por exemplo, histórico), os usuários podem ser solicitados a autorizar a sincronização novamente.

> [!NOTE]
> Ao contrário Versão Prévia do Microsoft Edge, o Microsoft Edge não usa o gerenciador de credenciais do Windows para senhas e, como resultado, não sincroniza senhas com o Internet Explorer ou outros aplicativos que usam o Windows Credential Manager.

## <a name="terms-of-service"></a>Termos de serviço

Os termos de serviço para Microsoft Edge sincronização se enquadram na licença de software da Microsoft que pode ser visualizada Microsoft Edge em *edge://terms*.

## <a name="see-also"></a>Ver também

- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Sincronização do Microsoft Edge](microsoft-edge-enterprise-sync.md)