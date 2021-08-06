---
title: Suporte do Microsoft Edge para Proteção de Informações do Windows
ms.author: kvice
author: dan-wesley
manager: srugh
ms.date: 06/29/2029
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Suporte do Microsoft Edge para Proteção de Informações do Windows
ms.openlocfilehash: 0ccb75384a1bf38aaaf2216813bff336e59e278b33da7d8267183442f9a31a16
ms.sourcegitcommit: d44c0997ffe40d67421312ed96e7766da947eaa0
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/05/2021
ms.locfileid: "11726964"
---
# <a name="microsoft-edge-support-for-windows-information-protection-wip"></a>Suporte do Microsoft Edge para Proteção de Informações do Windows (WIP)

Este artigo descreve como o Microsoft Edge tem suporte para a Proteção de Informações do Windows (WIP).

> [!NOTE]
> Isso se aplica ao Microsoft Edge versão 81 ou mais recente.

## <a name="overview"></a>Visão geral

A Proteção de Informações do Windows (WIP) é um recurso do Windows 10 que ajuda a proteger os dados corporativos contra divulgações acidentais ou não autorizadas. Com o aumento do trabalho remoto, há um maior risco de compartilhar dados corporativos fora do local de trabalho. Esse risco aumenta quando atividades pessoais e atividades de trabalho ocorrem em dispositivos corporativos.

O Microsoft Edge é compatível com a WIP para ajudar a proteger o conteúdo em um ambiente da Web em que os usuários compartilham e distribuem conteúdo com frequência.

### <a name="system-requirements"></a>Requisitos de sistema

Os requisitos a seguir se aplicam aos dispositivos que usam WIP na empresa:

- Windows 10, versão 1607 ou posterior
- Somente SKUs de clientes Windows
- Uma das soluções de gerenciamento descritas nos [pré-requisitos da WIP](/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip#prerequisites)

### <a name="windows-information-protection-benefits"></a>Benefícios da Proteção de Informações do Windows

A WIP fornece os seguintes benefícios:

- Separação óbvia entre dados pessoais e corporativos, sem a necessidade de os funcionários alternarem ambientes ou aplicativos.
- Proteção adicional de dados para aplicativos de linha de negócios existentes, sem a necessidade de atualizá-los.
- A capacidade de apagar remotamente os dados corporativos de dispositivos de gerenciamento de dispositivo móvel (MDM) do Intune, além de deixar os dados pessoais inalterados. 
- Relatórios de auditoria para controlar problemas e para ações corretivas, como treinamento de conformidade para usuários.
- Integração com o seu sistema de gerenciamento existente para configurar, implantar e gerenciar WIP. Alguns exemplos são o Microsoft Intune, o Microsoft Endpoint Configuration Manager ou o seu sistema de Gerenciamento de Dispositivo Móvel (MDM) atual.

## <a name="wip-policy-and-protection-modes"></a>Modos de política e proteção da WIP

Usando políticas, você pode configurar os quatro modos de proteção descritos na tabela a seguir. Para obter mais informações, confira [modos de proteção da WIP](/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip#wip-protection-modes).

| Modo | Descrição |
|------|-------------|
| Bloqueio | A WIP procura práticas inadequadas de compartilhamento de dados e impede que o funcionário execute a ação. Essa pesquisa pode incluir o compartilhamento de dados corporativos com aplicativos protegidos que não sejam da empresa, além de compartilhar dados corporativos entre aplicativos ou a tentativa de compartilhamento fora da rede da sua organização. |
| Permitir substituições | A WIP procura compartilhamento de dados inapropriados, avisando os funcionários se eles fizerem algo considerado potencialmente inseguro. No entanto, esse modo de gerenciamento permite que o funcionário substitua a política e compartilhe os dados, registrando a ação no log de auditoria. |
| Silencioso | A WIP é executada silenciosamente, registrando em log o compartilhamento inadequado de dados, sem impedir nenhuma ação que tenha sido solicitada para interação do funcionário no modo Permitir substituições. Ações não permitidas, como aplicativos tentando acessar de maneira inadequada um recurso de rede ou dados protegidos pela WIP, continuam sendo interrompidas. |
| Desativada | A WIP permanece desativada e não ajuda a proteger nem auditar os dados. Depois de desativar a WIP, é feita uma tentativa de descriptografar todos os arquivos marcados pela WIP nas unidades conectadas localmente. As suas informações de descriptografia e política anteriores não serão reaplicadas automaticamente se você reativar a proteção WIP novamente.
 |

## <a name="wip-features-supported-in-microsoft-edge"></a>Recursos da WIP com suporte no Microsoft Edge

A partir da versão 81 do Microsoft Edge, há suporte para os seguintes recursos:

- Os sites de trabalho serão indicados por um ícone de maleta na barra de endereços.  
- Os arquivos baixados de um local de trabalho são automaticamente criptografados.
- Imposição de Silencioso/Bloqueio/Substituição para carregamentos de arquivos de trabalho para locais que não são de trabalho.  
- Imposição de Silencioso/Bloqueio/Substituição para ações de Arrastar e Soltar arquivos.
- Imposição de Silencioso/Bloqueio/Substituição para ações da Área de Transferência.
- A navegação em locais de trabalho de perfis que não são de trabalho redireciona automaticamente para o Perfil de Trabalho (associado à identidade do Azure AD).
- O modo IE é compatível com a funcionalidade completa da WIP.

## <a name="working-with-wip-in-microsoft-edge"></a>Trabalhando com a WIP no Microsoft Edge

Depois que o suporte à WIP estiver habilitado para o Microsoft Edge, os usuários verão quando informações relacionadas ao trabalho forem acessadas. A próxima captura de tela mostra o ícone de maleta na barra de endereços, indicando que as informações relacionadas ao trabalho são acessadas por meio do navegador.

 ![Indicador da barra de endereços para sites marcados como "trabalho"](./media/microsoft-edge-security-windows-information-protection/microsoft-edge-wip-notify.png)

O Microsoft Edge oferece aos usuários a capacidade de compartilhar conteúdo protegido em um site não aprovado. A próxima captura de tela mostra o aviso do Microsoft Edge que permite que um usuário use conteúdo protegido em um site não aprovado.

 ![Aviso de substituição de conteúdo protegido](./media/microsoft-edge-security-windows-information-protection/microsoft-edge-wip-override.png)

## <a name="configure-policies-to-support-wip"></a>Configurar políticas para oferecer suporte à WIP

O uso da WIP com o Microsoft Edge requer a presença de um perfil de trabalho.

### <a name="ensure-the-presence-of-a-work-profile"></a>Garanta a presença de um perfil de trabalho

Em máquinas unidas híbridas, o Microsoft Edge é automaticamente conectado com a conta do Azure Active Directory (Azure AD). Para garantir que os usuários não removam esse perfil, que é necessário para a WIP, configure a seguinte política:

- [NonRemovableProfileEnabled](./microsoft-edge-policies.md#nonremovableprofileenabled)

> [!NOTE]
> Se o seu ambiente não tiver união híbrida, você pode fazer a união híbrida usando estas instruções: [Planejar a implementação de união híbrida do Azure Active Directory](/azure/active-directory/devices/hybrid-azuread-join-plan).

Se a junção híbrida não for uma opção, você poderá usar as contas locais do Active Directory para permitir que o Microsoft Edge crie automaticamente um perfil de trabalho especial com as contas de domínio dos usuários. Observe que as contas locais podem não receber todos os recursos do Azure AD, como a sincronização de nuvem, o Office NTP, e assim por diante.)

#### <a name="active-directory-ad-accounts"></a>Contas do Active Directory (AD)

Para contas do AD, você deve configurar a política a seguir para que o Microsoft Edge crie um perfil de trabalho especial automaticamente.

- [ConfigureOnPremisesAccountAutoSignIn](./microsoft-edge-policies.md#configureonpremisesaccountautosignin)

### <a name="windows-policies-for-wip"></a>Políticas do Windows para a WIP

Você pode configurar a WIP usando políticas do Windows. Para saber mais, confira [Criar e implantar políticas da WIP usando o Microsoft Intune](/windows/security/information-protection/windows-information-protection/overview-create-wip-policy)

## <a name="frequently-asked-questions"></a>Perguntas frequentes

### <a name="how-do-i-resolve-error-code--2147024540"></a>Como resolver o Código de erro -2147024540?

Esse código de erro corresponde ao seguinte erro de Proteção de Informações do Windows: *ERROR_EDP_POLICY_DENIES_OPERATION: a operação solicitada foi bloqueada pela política de Proteção de Informações do Windows. Para obter mais informações, entre em contato com o administrador do sistema.*.

O Microsoft Edge mostra esse erro quando a organização habilitou a Proteção de Informações do Windows (WIP), permitindo que apenas os usuários com aplicativos aprovados acessem recursos corporativos. Nesse caso, como o Microsoft Edge não está na lista de aplicativos aprovados, o administrador precisará atualizar as políticas de WIP para conceder acesso ao Microsoft Edge.

A captura de tela a seguir mostra como o Microsoft Intune é usado para adicionar o Microsoft Edge como um aplicativo permitido para WIP.

 ![Caixa de diálogo do Intune para adicionar o Microsoft Edge como um aplicativo para WIP](./media/microsoft-edge-security-windows-information-protection/microsoft-edge-wip-exemption.png)

Se você não estiver usando o Microsoft Intune, baixe e aplique a atualização de política no arquivo de [Política AppLocker para WIP Enterprise](https://download.microsoft.com/download/8/9/9/8995d820-065c-4ab1-aa2a-9d6dc0cd7ffa/MsEdge%20-%20WIP%20Enterprise%20AppLocker%20Policy%20Files.zip).

## <a name="see-also"></a>Consulte também

- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise) 
- [Proteja dados corporativos usando a Proteção de Informações do Windows](/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip)