---
title: Configurar e solucionar problemas de sincronização do Microsoft Edge
ms.author: scottbo
author: dan-wesley
manager: silvanam
ms.date: 01/22/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Configurar e solucionar problemas de sincronização do Microsoft Edge
ms.openlocfilehash: 36912d2fd1c33a227ce1d4b7c912f6ef1dfdcc00
ms.sourcegitcommit: 8a88fd38bdb5e132e89bf17dd2b5fb72f5d1b4b9
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/22/2021
ms.locfileid: "11297447"
---
# Configurar e solucionar problemas de sincronização do Microsoft Edge

Este artigo explica como configurar e usar o Microsoft Edge para sincronizar seus favoritos, senhas e outros dados do navegador com todos os seus dispositivos conectados. Este artigo também fornece as etapas para a solução dos problemas mais comuns encontrados sobre a sincronização. Ele também inclui as ferramentas recomendadas para coletar os logs necessários para a solução de problemas.

> [!NOTE]
> Aplica-se ao Microsoft Edge versão 77 ou posterior, a menos que indicado de outra forma.

## Visão geral

A sincronização do Microsoft Edge permite que os usuários acessem seus dados de navegação em todos os dispositivos conectados. Os dados com suporte na sincronização incluem:

- Favoritos
- Senhas
- Endereços e etc. (preenchimento de formulário)
- Coleções
- Configurações
- Extensão
- Abrir guias (disponível no Microsoft Edge versão 88)
- Histórico (disponível no Microsoft Edge versão 88)

A funcionalidade de sincronização é habilitada através do consentimento do usuário, e os usuários podem ativar ou desativar a sincronização de cada um dos tipos de dados listados acima.

> [!NOTE]
> Outros dados de configuração e conectividade do dispositivo (como nome, marca e modelo do dispositivo) são carregados para dar suporte à funcionalidade de sincronização.

## Pré-requisitos

A sincronização do Microsoft Edge das contas do Azure Active Directory (Azure AD) está disponível para qualquer uma das seguintes assinaturas:

- Azure AD Premium (P1 ou P2)
- M365 Business Premium
- Office 365 E1 e superior
- Proteção de informações do Azure (AIP) (P1 ou P2)
- Todas as assinaturas EDU (Aplicativos da Microsoft para Estudantes ou Docentes, Exchange Online para Estudantes ou Docentes, O365 A1 ou superior, M365 A1 ou superior, Proteção de Informações do Azure P1 ou P2 para Estudantes ou Docentes)

## Políticas de grupo de sincronização

Você pode usar as seguintes políticas de grupo para configurar e gerenciar a sincronização do Microsoft Edge:

- [SyncDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#syncdisabled): desabilita completamente a sincronização.
- [SavingBrowserHistoryDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#savingbrowserhistorydisabled): desabilita o salvamento do histórico de navegação e a sincronização. Também desabilita a sincronização das guias abertas.
- [AllowDeletingBrowserHistory](https://docs.microsoft.com/deployedge/microsoft-edge-policies#allowdeletingbrowserhistory): quando essa política é definida como Desabilitada, a sincronização do histórico também será desabilitada.
- [SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled): configura a lista dos tipos excluídos da sincronização.
- [RoamingProfileSupportEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#roamingprofilesupportenabled): permite que os perfis Active Directory (AD) usem o armazenamento local. Para obter mais informações, confira [Sincronização local para usuários do Active Directory (AD)](https://docs.microsoft.com/DeployEdge/microsoft-edge-on-premises-sync).
- [ForceSync]( https://docs.microsoft.com/deployedge/microsoft-edge-policies#forcesync): ativar a sincronização por padrão e não exigir consentimento do usuário para sincronizar.  

## Configurar a sincronização do Microsoft Edge

As opções de configuração para a sincronização do Microsoft Edge estão disponíveis por meio do serviço de Proteção de Informações do Azure (AIP). Quando o (AIP) estiver habilitado para um locatário, todos os usuários poderão sincronizar os dados do Microsoft Edge, independentemente do licenciamento. Instruções sobre como habilitar o AIP estão disponíveis [aqui](https://docs.microsoft.com/azure/information-protection/activate-office365).

Para restringir a sincronização a certos conjuntos de usuários, você pode habilitar a [Política de controle de integração do AIP](https://docs.microsoft.com/powershell/module/aipservice/set-aipserviceonboardingcontrolpolicy?view=azureipps&preserve-view=true)  para esses usuários. Se a sincronização ainda não estiver disponível depois de garantir que todos os usuários necessários estejam integrados, certifique-se de que o IPCv3Service está habilitado usando o cmdlet [Get-AIPServiceIPCv3](https://docs.microsoft.com/powershell/module/aipservice/get-aipserviceipcv3?view=azureipps&preserve-view=true)  PowerShell.

> [!CAUTION]
> Ativar a Proteção de Informações do Azure também permitirá que outros aplicativos, como o Microsoft Word ou o Microsoft Outlook, protejam o conteúdo com o AIP. Além disso, qualquer política de controle de integração usada para restringir a sincronização do Microsoft Edge também restringirá outros aplicativos de proteger conteúdo usando o AIP.

## Microsoft Edge e ESR (Enterprise State Roaming)

O Microsoft Edge é um aplicativo de plataforma cruzada com um escopo expandido para sincronizar dados do usuário em todos os seus dispositivos e não faz parte do Azure AD Enterprise State Roaming. No entanto, o Microsoft Edge cumprirá as promessas de proteção de dados do ESR, como a capacidade de trazer sua própria chave. Para obter mais informações, confira [Microsoft Edge e Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).

## Solucionar problemas de sincronização

Esta seção fornece as etapas para a solução dos problemas mais encontrados referente a sincronização. Ele também inclui as ferramentas recomendadas para coletar os logs necessários para a solução de problemas.

### Problemas de identidade versus problemas de sincronização

Um caso de uso popular para manter a identidade do usuário no navegador é dar suporte à sincronização. Por esta razão, os problemas com identidade são frequentemente confundidos com problemas de sincronização. Entenda a diferença entre problemas de identidade e de sincronização antes de começar a solucionar os problemas de sincronização.

Antes de tratar um problema como sendo de sincronização, verifique se o usuário está conectado ao navegador com uma conta válida.

A próxima captura de tela mostra um exemplo de um erro de identidade. O erro é "**Last Token Error, EDGE_AUTH_ERROR: 3, 54, 3ea**", que é encontrado no *edge://sync-internals* em **Credenciais**:

:::image type="content" source="media/microsoft-edge-enterprise-sync-configure-and-troubleshoot/sync-identity-issue.png" alt-text="Last Token Error EDGE_AUTH_ERROR: 3,54, 3ea":::

### Problemas comuns de sincronização

#### Problema: Não é possível acessar a assinatura do M365 ou a da Proteção de Informações do Azure

Você tem uma assinatura anterior do M365 ou da AIP (Proteção de Informações do Azure) que expirou e foi substituída por uma nova assinatura? Nesse caso, a ID do locatário foi alterada e os dados de serviço precisam ser reajustados. Confira as instruções para redefinir os dados no problema **Erro de criptógrafo encontrado**.

#### Problema: "A sincronização não está disponível para esta conta".

Se este erro for encontrado para uma conta do Azure Active Directory, ou se DISABLED_BY_ADMIN aparecer em *edge://sync-internals*, siga as etapas no próximo procedimento sequencialmente até que o problema seja corrigido.

> [!NOTE]
> Como a origem deste erro geralmente requer uma alteração de configuração em um locatário do Azure Active Directory, estas etapas de solução de problemas só podem ser executadas por um administrador do locatário e não por usuários finais.

1. Verifique se o locatário corporativo tem uma assinatura do M365 com suporte. A lista atual dos tipos de assinatura disponíveis está [fornecida aqui](https://docs.microsoft.com/azure/information-protection/activate-office365). Se o locatário não tiver uma assinatura com suporte, é possível comprar a Proteção de Informações do Azure separadamente, ou atualizar para uma das assinaturas com suporte.
2. Se uma assinatura com suporte estiver disponível, verifique se o locatário tem a AIP (Proteção de Informações do Microsoft Azure) disponível. As instruções para verificar o status da AIP e, se necessário, ativar a AIP estão [aqui](https://docs.microsoft.com/azure/information-protection/activate-office365).
3. Se a etapa 2 mostrar que a AIP está ativa, mas a sincronização ainda não funciona, ative o ESR (Enterprise State Roaming). As instruções para habilitar o ESR estão [aqui](https://docs.microsoft.com/azure/active-directory/devices/enterprise-state-roaming-enable). Observe que o ESR não precisa permanecer ativado. Você pode desativar o ESR se esta etapa corrigir o problema.
4. Confirme se a Proteção de Informações do Azure não tem escopo por meio de uma política de integração. Você pode usar o miniaplicativo [Get-AadrmOnboardingControlPolicy](https://docs.microsoft.com/powershell/module/aadrm/get-aadrmonboardingcontrolpolicy?view=azureipps) do PowerShell para ver se o escopo está habilitado. Os dois exemplos a seguir mostram uma configuração com escopo e outra sem escopo para um grupo de segurança específico.

   ```powershell
    PS C:\Work\scripts\PowerShell> Get-AadrmOnboardingControlPolicy
 
    UseRmsUserLicense SecurityGroupObjectId                Scope
    ----------------- ---------------------                -----
                False 
   ```

   ```powershell

    PS C:\Work\scripts\PowerShell> Get-AadrmOnboardingControlPolicy
 
    UseRmsUserLicense SecurityGroupObjectId                Scope
    ----------------- ---------------------                -----
                False f1488a05-8196-40a6-9483-524948b90282   All
   ```


   Se o escopo estiver habilitado, o usuário afetado deverá ser adicionado ao grupo de segurança para o escopo, ou o escopo deverá ser removido. No exemplo abaixo, a integração definiu a AIP para o grupo de segurança indicado e o escopo deve ser removido com o miniplicativo [Set-AadrmOnboardingControlPolicy](https://docs.microsoft.com/powershell/module/aadrm/set-aadrmonboardingcontrolpolicy?view=azureipps) do PowerShell.

5. Confirme se o IPCv3Service está ativado no locatário. O miniaplicativo [Get-AadrmConfiguration](https://docs.microsoft.com/powershell/module/aadrm/get-aadrmconfiguration?view=azureipps) do PowerShell mostra o status do serviço.

   :::image type="content" source="media/microsoft-edge-enterprise-sync-configure-and-troubleshoot/sync-scoped-cfg-example.png" alt-text="Verifique se IPCv3Service está habilitado.":::

6. Se o problema não for corrigido, contate o [suporte do Microsoft Edge](https://www.microsoftedgeinsider.com/support).

#### Problema: Travado em "Configurando a sincronização..." ou "Não foi possível se conectar ao servidor de sincronização. Tentando novamente..."

1. Tente sair e entrar novamente.
2. Vá para *edge://sync-internals*. Se na seção "**Informações do tipo**" o seguinte erro estiver presente, pule para o problema a seguir, **Erro de criptógrafo encontrado**.

   `"Error:GenerateCryptoErrorsForTypes@../../components/sync/driver/data_type_manager_impl.cc:42, cryptographer error was encountered"`

3. Tente executar ping no ponto de extremidade do servidor. O ponto de extremidade do servidor para um cliente está disponível em *edge://sync-internals*. A próxima captura de tela mostra informações do ponto de extremidade em **Informações do Ambiente**.

   :::image type="content" source="media/microsoft-edge-enterprise-sync-configure-and-troubleshoot/sync-endpoint-info.png" alt-text="Informações sobre o ponto de extremidade":::

4. Se o ponto de extremidade do servidor estiver vazio, ou se o servidor não puder ser pingado e um firewall estiver presente no ambiente, confirme se os pontos de extremidade de serviço necessários estão disponíveis para o computador cliente.

   - Pontos de extremidade do serviço de sincronização do Microsoft Edge:
     - [https://edge-enterprise.activity.windows.com](https://edge-enterprise.activity.windows.com)
     - [https://edge.activity.windows.com](https://edge.activity.windows.com)
    - Pontos de extremidade da Proteção de Informações do Azure:
      - [https://api.aadrm.com](https://api.aadrm.com) (para a maioria dos locatários)
      - [https://api.aadrm.de](https://api.aadrm.de) (para locatários na Alemanha)
      - [https://api.aadrm.cn](https://api.aadrm.cn) (para locatários na China)
   - [Pontos de Extremidade do Serviço de Notificação do Windows](https://docs.microsoft.com/windows/uwp/design/shell/tiles-and-notifications/firewall-allowlist-config).

5. Se o problema ainda não estiver corrigido, entre em contato com o [suporte do Microsoft Edge.](https://www.microsoftedgeinsider.com/support)

### Problema: erro de criptógrafo encontrado

Este erro está visível em **Informações do tipo** em *edge://sync-internals*, e isso poderá significar que os dados do lado de serviço do usuário precisam ser redefinidos. O exemplo a seguir mostra uma mensagem de erro de criptografia:
<br>"Error:GenerateCryptoErrorsForTypes@.. /.. /components/sync/driver/data_type_manager_impl.cc:42, erro criptografador encontrado".

1. Reinicie o Microsoft Edge e navegue até *edge://sync-internals* e verifique a seção “**Status da Chave de Conta do AAD**”
   - "Êxito" em "Último Resultado do MIP": o erro de criptógrafo significa que os dados do servidor podem ser criptografados com uma chave perdida. É necessário a redefinição dos dados para retomar a sincronia.
   - "Sem permissões" em "Último Resultado do MIP": possivelmente isso foi causado por uma alteração no Azure AD ou por alterações na assinatura do locatário. É necessário a redefinição dos dados para retomar a sincronia.
   - Outros erros podem significar problemas de configuração do servidor.
2. Se a redefinição de dados for necessária, confira [Redefinir dados do Microsoft Edge na nuvem](edge-learnmore-reset-data-in-cloud.md).

#### Problema: "A sincronização foi desativada pelo administrador".

Certifique-se de que a [política SyncDisabled ](https://docs.microsoft.com/deployedge/microsoft-edge-policies#syncdisabled) não está definida.

## Perguntas frequentes

### SEGURANÇA e CONFORMIDADE COM O SERVIDOR/DADOS

#### Os dados sincronizados estão encriptados?

Os dados são criptografados no transporte usando TLS 1.2 ou posterior. Todos os tipos de dados também são criptografados como descansar no serviço da Microsoft usando o AES128. Todos os tipos de dados, exceto os usados na guia aberta e na sincronização do histórico, são adicionalmente criptografados antes de deixar o dispositivo do usuário com chaves gerenciadas através da política da [Proteção de Informações do Microsoft Azure](https://docs.microsoft.com/deployedge/microsoft-edge-policies#restrictsignintopattern).

#### Por que a guia aberta e os dados do histórico não têm mais criptografia do lado do cliente?

Para reduzir o uso de recursos nos dispositivos do usuário final, os dados do histórico são gerados no lado do servidor com base nos dados de roaming da guia aberta. Este processo não seria possível com a criptografia ao lado do cliente desses dados. Para desabilitar a guia aberta e a sincronização do histórico, aplique as políticas [SavingBrowserHistoryDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#savingbrowserhistorydisabled) ou [SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled) .

#### Os administradores de locatários podem ter suas próprias chaves?

Sim, pela [Proteção de informações do Azure](https://azure.microsoft.com/services/information-protection/).

#### Onde os dados sincronizados são armazenados no Microsoft Edge?

Os dados sincronizados para contas do Azure AD são armazenados em servidores seguros de acordo com a ID do locatário. Por exemplo, os dados de um locatário registrado nos Estados Unidos são armazenados em servidores localizados geograficamente nessa região e aproveitam a mesma solução de armazenamento usada pelos aplicativos do Office.

#### Os dados deixam a nuvem da Microsoft, além de sincronizar com o Microsoft Edge?

Não.

#### Em que termos de serviço a sincronização empresarial se encaixa?

Os termos de serviço da sincronização do Microsoft Edge se enquadram na licença de software da Microsoft exibida no Microsoft Edge em *Edge://terms*. A sua assinatura e os termos de serviço do Azure AD estão, em última análise, em [Termos de serviço on-line](https://www.microsoft.com/licensing/product-licensing/products)da Microsoft.

#### O Microsoft Edge dá suporte á conformidade do Government Community Cloud (GCC) High?

Não atualmente. Para os clientes na nuvem GCC High, o Microsoft Edge sync está desabilitado.

### APLICAÇÃO DE SINCRONIZAÇÃO

#### Por que a sincronização do Microsoft Edge não é compatível com todas as assinaturas do M365?

A sincronização empresarial depende da [Proteção de Informações do Azure,](https://azure.microsoft.com/services/information-protection/)que não está disponível em todas as assinaturas do M365.

#### A sincronização do Microsoft Edge é baseada no Enterprise State Roaming?

Não. O ESR pode ser usado para habilitar a sincronização, mas a sincronização do Microsoft Edge não faz parte do ESR. Para obter mais informações, consulte [Sincronização do Microsoft Edge](https://review.docs.microsoft.com/DeployEdge/microsoft-edge-enterprise-sync) e [Microsoft Edge e Enterprise State Roaming](https://review.docs.microsoft.com/DeployEdge/microsoft-edge-enterprise-state-roaming).

#### O Microsoft Edge oferecerá suporte para sincronização entre o Microsoft Edge e o IE?

Não há planos para dar suporte a essa sincronização. Se você ainda precisar do IE no seu ambiente para oferecer suporte aos aplicativos herdados, considere o nosso [novo modo do IE](https://docs.microsoft.com/deployedge/edge-ie-mode).

#### O Microsoft Edge será sincronizado com o Microsoft Edge herdado?

Não. Acreditamos que a conexão destes dois ecossistemas comprometerá a confiabilidade da sincronia no Microsoft Edge. Garantiremos que os dados existentes serão migrados para o Microsoft Edge. Os usuários também poderão importar dados do navegador de sua escolha, o que também significa que o Microsoft Edge não terá uma maneira de sincronizar com o IE.

### GERENCIANDO A SINCRONIZAÇÃO

#### É possível impedir que os meus usuários sincronizem com um locatário pessoal?

Não diretamente, mas você pode determinar quais perfis podem entrar no Microsoft Edge usando a política [RestrictSigninToPattern](https://docs.microsoft.com/deployedge/microsoft-edge-policies#restrictsignintopattern).

## Ver também

- [Sincronização do Microsoft Edge Enterprise](microsoft-edge-enterprise-sync.md)
- [Microsoft Edge e Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md)
- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
