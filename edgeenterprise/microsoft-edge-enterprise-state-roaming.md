---
title: Microsoft Edge e Enterprise State Roaming
ms.author: kvice
author: dan-wesley
manager: laurawi
ms.date: 02/14/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Microsoft Edge e Enterprise State Roaming
ms.openlocfilehash: e56c59868f354c4e74f663a4d2bb5f585f9d8169
ms.sourcegitcommit: f363ceb6c42054fabc95ce8d7bca3c52d80e6a9f
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/24/2021
ms.locfileid: "11448105"
---
# <a name="microsoft-edge-and-enterprise-state-roaming"></a>Microsoft Edge e Enterprise State Roaming

Este artigo explica como a participação do Microsoft Edge na oferta do Enterprise State Roaming (ESR) está mudando para oferecer um suporte melhor à sincronização entre plataformas e dispositivos.

> [!NOTE]
> Este artigo se aplica ao Microsoft Edge versão 77 ou posterior.

## <a name="introduction"></a>Introdução

Com o Windows 10, os usuários do [Azure Active Directory (Azure AD)](/azure/active-directory/fundamentals/active-directory-whatis) têm a possibilidade de sincronizar de maneira segura as configurações de usuário e os dados das configurações do aplicativo com a nuvem. O [Enterprise State Roaming (ESR)](/azure/active-directory/devices/enterprise-state-roaming-overview) oferece aos usuários uma experiência unificada em todos os dispositivos Windows e reduz o tempo necessário para configurar um novo dispositivo.

Como parte da adoção da plataforma Chromium pelo Microsoft Edge, sua solução de sincronização agora está desconectada da estrutura de sincronização do Windows. Isso afeta a relação do Microsoft Edge com a oferta de ESR.

> [!IMPORTANT]
> O novo Microsoft Edge não participa da oferta de ESR.

## <a name="whats-changing-with-microsoft-edge"></a>O que mudará no Microsoft Edge?

Com o novo Microsoft Edge, a solução de sincronização não está vinculada ao ecossistema de sincronização do Windows. Isso nos permite oferecer o Microsoft Edge em todas as plataformas, como Windows 7, Windows 8.1, iOS, Android e macOS. Isso também nos permite oferecer sincronização para contas não primárias no Windows. Além disso, podemos fornecer o Microsoft Edge em uma cadência de lançamento mais frequente e flexível que a do Windows. (Para obter mais informações, consulte [Atualizações do Windows para oferecer suporte à próxima versão do Microsoft Edge](microsoft-edge-sysupdate-windows-updates.md). Todos esses fatores destacaram a necessidade de reavaliar a participação do Microsoft Edge na oferta de ESR.

O ESR é enquadrado como uma oferta de produto do Windows com promessas sobre como os dados de dispositivos Windows são manipulados, mas a sincronização do Microsoft Edge vai além dos dispositivos Windows. E, à medida que os dados transitam por esses dispositivos, é difícil definir a oferta de sincronização do Microsoft Edge no contexto do ESR. Para simplificar a maneira como a sincronização funciona e é gerenciada, e para acomodar as alterações destacadas, foi tomada a decisão de tirar o Microsoft Edge da oferta de ESR.

## <a name="does-this-mean-enterprises-will-lose-the-abilities-they-had-as-part-of-esr"></a>Isso significa que as empresas perderão as capacidades que tinham como parte do ESR?

Não. O Microsoft Edge continuará dando suporte à maioria das capacidades fornecidas na oferta de ESR.

### <a name="unified-experience-across-devices-and-new-device-configuration-time"></a>Experiência unificada entre dispositivos e novo tempo de configuração de dispositivo

Quando um usuário se conecta ao seu dispositivo Windows com uma conta do Azure Active Directory (AAD), o Microsoft Edge herda implicitamente essa identidade na primeira inicialização do novo navegador.

Depois que o usuário autorizar explicitamente a ativação da sincronização no novo Microsoft Edge, o navegador sincronizará todos os dados do navegador, como favoritos, senhas e histórico. Isso garante uma experiência unificada em todos os dispositivos e reduz o tempo necessário para personalizar o navegador.

### <a name="separation-of-corporate-and-consumer-data"></a>Separação de dados corporativos e do consumidor

As organizações estão no controle dos dados, e não há mistura de dados corporativos em uma conta de nuvem do consumidor ou de dados do consumidor em uma conta de nuvem corporativa.

### <a name="enhanced-security"></a>Segurança reforçada

Os dados são criptografados automaticamente antes de saírem do dispositivo Windows 10 do usuário usando a Proteção de Informações do Azure, e os dados permanecem criptografados em repouso na nuvem. Todo o conteúdo continua criptografado em repouso na nuvem, exceto os namespaces, como nomes de configurações.

### <a name="monitoring"></a>Monitoramento

Forneceremos controle e visibilidade sobre quem sincroniza as configurações em sua organização e em quais dispositivos por meio da integração com o portal do Azure AD. Essa funcionalidade será habilitada em uma versão futura.

### <a name="management"></a>Gerenciamento

Os administradores poderão controlar quais membros em sua organização podem habilitar a sincronização. Consulte [Configurar a sincronização do Microsoft Edge](microsoft-edge-enterprise-sync.md#configure-microsoft-edge-sync) e [Sincronizar políticas de grupo](microsoft-edge-enterprise-sync.md#sync-group-policies). Além disso, os usuários podem ativar/desativar a sincronização para cada um dos seus dispositivos, bem como alternar cada atributo de dados individualmente para sincronização.

### <a name="key-management"></a>Gerenciamento de chaves

O recurso de sincronização usa a Proteção de Informações do Azure (AIP) para proteger os dados sincronizados somente para o usuário e os administradores corporativos. O AIP oferece suporte a dispositivos gerenciados pela Microsoft (padrão) e com a própria chave para gerenciamento de chaves na nuvem. A estratégia de gerenciamento de chaves na nuvem usada por sua organização é transparente para o Microsoft Edge e não tem impacto sobre o recurso de sincronização.

> [!IMPORTANT]
> O método [Mantenha sua própria chave (HYOK)](/azure/information-protection/configure-adrms-restrictions) e o Active Directory Rights Management Services não têm suporte.

## <a name="summary-of-sync-attributes"></a>Resumo dos atributos de sincronização

Os seguintes atributos de dados serão sincronizados na nova versão do Microsoft Edge na primeira inicialização:

- Favoritos
- Senhas
- Preenchimento de formulários
- Histórico
- Guias abertas (sessões)
- Configurações (preferências)
- Extensões

A lista anterior de atributos é diferente dos atributos que podem ser sincronizados no Microsoft Edge Legacy. (Para obter detalhes sobre as configurações do Microsoft Edge Legacy, consulte [Configurações de roaming do Windows 10](/azure/active-directory/devices/enterprise-state-roaming-windows-settings-reference).) Os usuários podem habilitar/desabilitar esses atributos seletivamente usando as configurações do Microsoft Edge. Devido à diferença de atributos entre as duas versões (por exemplo, histórico), os usuários podem ser solicitados a autorizar a sincronização novamente.

> [!NOTE]
> Diferentemente do Microsoft Edge Legacy, o novo Microsoft Edge não usa o Gerenciador de credenciais do Windows para senhas e, portanto, não sincroniza senhas com o Internet Explorer ou outros apps que usam o Gerenciador de credenciais do Windows.

## <a name="terms-of-service"></a>Termos de serviço

Os termos de serviço de sincronização do Microsoft Edge estão sujeitos à licença de software da Microsoft visível no Microsoft Edge, em *edge://terms*.

## <a name="see-also"></a>Consulte também

- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Sincronização do Microsoft Edge](microsoft-edge-enterprise-sync.md)