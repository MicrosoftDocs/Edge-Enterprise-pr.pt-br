---
title: 'Segurança do gerenciador de senhas do Microsoft Edge '
ms.author: v-danwesley
author: dan-wesley
manager: collw
ms.date: 08/25/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Segurança do gerenciador de senhas do Microsoft Edge
ms.openlocfilehash: 90ac5760f4e53ffe9b91380adecd5cf40e84ba0c
ms.sourcegitcommit: f8a5f3bbc786f3666a2974a4f7be0e6145efb8da
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2022
ms.locfileid: "12735923"
---
# <a name="microsoft-edge-password-manager-security"></a>Segurança do gerenciador de senhas do Microsoft Edge

As perguntas frequentes neste artigo descrevem como o gerenciador de senhas interno do Microsoft Edge fornece segurança para as senhas de usuário.

> [!Note]
>Este artigo se aplica ao Microsoft Edge versão 77 ou posterior.

## <a name="how-are-passwords-stored-in-microsoft-edge-and-how-safe-is-this-approach"></a>Como as senhas são armazenadas em Microsoft Edge e qual é a segurança dessa abordagem?

O Microsoft Edge armazena senhas criptografadas no disco. Eles são criptografados usando AES e a chave de criptografia é salva em uma área de armazenamento do sistema operacional (SO). Essa técnica é chamada de criptografia local de dados. Embora nem todos os dados do navegador sejam criptografados, dados confidenciais como senhas, números de cartão de crédito e cookies são criptografados quando são salvos.

O gerenciador de senhas do Microsoft Edge criptografa senhas para que elas só possam ser acessadas quando um usuário estiver conectado ao sistema operacional. Mesmo que um invasor tenha direitos de administrador ou acesso offline e possa acessar os dados armazenados localmente, o sistema foi projetado para impedir que o invasor obtenha as senhas de texto de um usuário que não está conectado.

É possível descriptografar as senhas de outro usuário se esse usuário tiver feito logon e o invasor tiver a senha do usuário ou tiver comprometido o controlador de domínio.

### <a name="about-the-encryption-method"></a>Sobre o método de criptografia

A chave de criptografia do perfil é protegida usando o OSCrypt do Chromium e usa os seguintes locais de armazenamento do sistema operacional específicos da plataforma:

- No Windows, a área de armazenamento é DPAPI

- No Mac, a área de armazenamento é Keychain

- No Linux, a área de armazenamento é Gnome Keyring ou KWallet

Todas essas áreas de armazenamento criptografam a chave AES usando uma chave acessível para alguns ou todos os processos em execução como o usuário. Esse vetor de ataque geralmente é exibido em blogs como uma possível "exploração" ou "vulnerabilidade". Essa é uma compreensão incorreta do modelo de ameaça do navegador e da postura de segurança.

No entanto, ataques fisicamente locais e malware estão fora do modelo de ameaça e, sob essas condições, os dados criptografados seriam vulneráveis. Se o computador estiver infectado com malware, um invasor poderá obter acesso descriptografado às áreas de armazenamento do navegador. O código do invasor, em execução como sua conta de usuário, pode fazer tudo o que você pode fazer.

## <a name="why-encrypt-data-locally-why-not-store-the-encryption-key-elsewhere-or-make-it-harder-to-obtain"></a>Por que criptografar dados localmente? Por que não armazenar a chave de criptografia em outro lugar ou dificultar a obtenção?

Navegadores da Internet (incluindo o Microsoft Edge) não estão equipados com defesas contra ameaças quando todo o dispositivo está comprometido devido a um malware em execução como usuário no computador. No entanto, programas como o Microsoft Defender SmartScreen e proteções no nível do sistema operacional como o Windows Defender são projetados para garantir que o dispositivo não seja comprometido.

Apesar da incapacidade de proteger contra malware de confiança total, a Criptografia de Dados Local é útil em determinados cenários. Por exemplo, se um invasor encontrar uma maneira de roubar arquivos do disco sem a capacidade de executar código ou roubar um laptop que não está protegido com Criptografia de Disco Completo, a Criptografia de Dados Local dificultará que o invasor obtenha dados armazenados.

## <a name="do-you-recommend-storing-passwords-in-microsoft-edge"></a>Você recomenda o armazenamento de senhas no Microsoft Edge?

Os usuários que podem contar com o gerenciador de senhas interno do Microsoft Edge podem usar (e usam) senhas mais fortes e exclusivas porque não precisam lembrar de todas elas e digitá-las com a mesma frequência. E como o gerenciador de senhas só preencherá automaticamente as senhas nos sites aos quais elas pertencem, os usuários têm menos probabilidade de se enquadrarem em um ataque de phishing.

> [!Note]
>Relatórios do setor mostram que 80% dos incidentes online estão relacionados a phishing e mais de 37% dos usuários não treinados falham nos testes de phishing.

O gerenciador de senhas do Microsoft Edge é conveniente e facilmente distribuído, o que contribui para melhorar a segurança. Quando combinado com a sincronização, você pode obter todas as suas senhas em todos os seus dispositivos e é fácil usar uma senha diferente para cada site. Você pode usar senhas longas e complexas e para todos os sites sem precisar lembrar delas e ignorar a não precisará digitar uma cadeia de caracteres complexa todas as vezes. A conveniência do gerenciador de senhas significa que há menos risco de ataque de phishing.

No entanto, usar um gerenciador de senhas com chave na sessão de logon do sistema operacional do usuário também significa que um invasor nessa sessão pode recuperar imediatamente todas as senhas salvas do usuário. Sem um gerenciador de senhas para roubar, um adversário precisaria rastrear as teclas digitadas ou monitorar as senhas enviadas.

Para decidir usar um gerenciador de senhas é necessário avaliar os muitos benefícios que descrevemos em relação à possibilidade de todo o dispositivo ser comprometido. Para a maioria dos modelos de ameaça, usar o gerenciador de senhas do Microsoft Edge é a opção recomendada.

> [!Note]
>Se uma empresa estiver preocupada com o roubo de uma senha específica ou um site comprometido devido a uma senha roubada, precauções adicionais devem ser tomadas. Algumas soluções eficazes que ajudam a atenuar esse tipo de incidente são o SSO (logon único) por meio do Active Directory, Azure Active Directory ou de terceiros. Outras soluções incluem 2FA (como [MS Authenticator](/azure/active-directory/user-help/user-help-auth-app-download-install)) ou [WebAuthN](https://webauthn.guide/).

## <a name="should-a-password-manager-be-enabled-by-an-organization"></a>Um gerenciador de senhas deve ser habilitado por uma organização?

A resposta simples e fácil é: sim, use o gerenciador de senhas do navegador.

A resposta mais completa diz que seria necessário ter um conhecimento aprofundado do seu modelo de ameaça, pois as opções de segurança variam dependendo de modelos de ameaça diferentes. Algumas perguntas relevantes a serem consideradas ao pensar se você deve habilitar o gerenciador de senhas para sua organização são:

- Com que tipo de invasores você está preocupado?

- Em que tipo de sites os usuários fazem logon?

- Os usuários selecionam senhas fortes e exclusivas?

- As contas dos usuários estão protegidas com 2FA?

- Quais tipos de ataques são mais prováveis?

- Como proteger seus dispositivos corporativos contra malware?

- Qual é a tolerância pessoal dos usuários para inconveniência?

- Considere o impacto da sincronização de dados.

É importante considerar a segurança dos dados do usuário conforme eles são sincronizados com vários dispositivos de usuário e a quantidade de controle que a organização tem na sincronização automática de dados.

Sincronização de dados e Microsoft Edge:

- A sincronização de dados pode ser habilitada ou desabilitada conforme desejado em toda a organização.

- Segurança de dados em trânsito e em repouso na nuvem: todos os dados sincronizados são criptografados em trânsito por HTTPS quando transferidos entre o navegador e os servidores da Microsoft. Os dados sincronizados também são armazenados em um estado criptografado nos servidores da Microsoft. Os tipos de dados confidenciais, como endereços e senhas, são criptografados no dispositivo antes de serem sincronizados. Se você estiver usando uma conta corporativa ou de estudante, todos os tipos de dados serão criptografados antes de serem sincronizados usando Proteção de Informações do Microsoft Purview.

## <a name="why-do-microsoft-security-baselines-recommend-disabling-the-password-manager"></a>Por que as linhas de base de segurança da Microsoft recomendam desabilitar o gerenciador de senhas?

No momento, a equipe de segurança da Microsoft classificou o impacto de um worm que compromete uma rede de computadores empresariais (resultando na perda de todas as credenciais nos gerenciadores de senhas de todos os dispositivos) como mais grave do que o risco (mais provável, mas com menor impacto) de ataques de phishing direcionados que comprometem uma única credencial inserida pelo usuário.

Essa avaliação está em discussão e está sujeita a alterações com a adição de novos recursos de melhoria de segurança no Microsoft Edge.

## <a name="can-malicious-extensions-gain-access-to-passwords"></a>Extensões mal-intencionadas podem obter acesso a senhas?

Uma extensão com permissão para interagir com uma página é inerentemente capaz de acessar qualquer coisa dessa página, incluindo uma senha preenchida automaticamente. Da mesma forma, uma extensão mal-intencionada pode modificar o conteúdo de campos de formulário e solicitações/respostas de rede para usar indevidamente a autoridade do contexto de logon do usuário atual.

No entanto, o Microsoft Edge fornece um amplo conjunto de políticas que permitem um controle refinado sobre extensões instaladas. O uso das políticas na tabela a seguir é necessário para proteger dados corporativos.

| Política | Legenda |
|-|-|
|[BlockExternalExtensions](/deployedge/microsoft-edge-policies#blockexternalextensions)|Bloqueia a instalação de extensões externas|
|[ExtensionAllowedTypes](/deployedge/microsoft-edge-policies#extensionallowedtypes)|Configurar tipos de extensão permitidas|
|[ExtensionInstallAllowlist](/deployedge/microsoft-edge-policies#extensioninstallallowlist)|Permitir que extensões específicas sejam instaladas|
|[ExtensionInstallBlocklist](/deployedge/microsoft-edge-policies#extensioninstallblocklist)|Controlar quais extensões não podem ser instaladas|
|[ExtensionInstallForcelist](/deployedge/microsoft-edge-policies#extensioninstallforcelist)|Controlar quais extensões são instaladas silenciosamente|
|[ExtensionInstallSources](/deployedge/microsoft-edge-policies#extensioninstallsources)|Configurar fontes de instalação de extensão e script de usuário|
| [ExtensionSettings](/deployedge/microsoft-edge-policies#extensionsettings) |Definir configurações de gerenciamento de extensão. |

## <a name="how-does-the-microsoft-edge-password-manager-compare-with-a-third-party-product"></a>Como o gerenciador de senhas do Microsoft Edge é comparado com um produto de terceiros?

A tabela a seguir mostra como o gerenciador de senhas do Microsoft Edge se compara a gerenciadores de senhas de terceiros.

| Gerenciador de senhas de terceiros | Gerenciador de senhas do Microsoft Edge|
|-|-|
| *Sincronização do servidor*. Alguns produtos armazenam senhas na nuvem para sincronizar todos os seus dispositivos. Esse recurso é útil, mas há um risco se o serviço de nuvem for comprometido e seus dados forem expostos. **Comentários:** O risco é reduzido ao ter senhas criptografadas na nuvem e armazenar a chave de criptografia em seus dispositivos para que os invasores não possam acessar a chave e suas senhas.| Há um risco de exposição à nuvem porque as senhas são sincronizadas entre dispositivos Windows que Microsoft Edge instalados. **Comentários:** esse risco é mitigado pelas etapas de segurança de dados abordadas neste artigo.|
| *Confiança*. É necessário confiar que o terceiro não está fazendo nada mal-intencionado, como enviar suas senhas para outra pessoa. **Comentários:** Esse risco pode ser atenuado examinando o código-fonte (no caso de produtos de software livre) ou acreditando que o fornecedor se preocupa com sua reputação e receita. | **Comentários: **A Microsoft é um fornecedor conhecido e confiável com décadas de histórico no fornecimento de segurança e produtividade de nível empresarial, com recursos projetados para proteger suas senhas em todo o mundo. |
| *Segurança da cadeia do fornecedor*. É difícil verificar se o fornecedor tem processos seguros de cadeia de fornecimento/build/lançamento para o código-fonte. |**Comentários:** A Microsoft tem processos internos robustos para garantir o risco mínimo ao código-fonte. |
| *Cliente ou conta comprometida*. Se um dispositivo cliente ou uma conta de usuário for comprometida, um invasor poderá obter as senhas. **Comentários:** esse risco é atenuado para alguns gerenciadores de senhas que exigem que o usuário insira uma Senha Mestra que não seja armazenada localmente para descriptografar as senhas. A Senha Mestra é apenas uma mitigação parcial porque um invasor pode ler pressionamentos de teclas e obter a senha mestra conforme ela é digitada ou lê senhas da memória do processo ao preencher um campo de formulário. | **Comentários:** a Microsoft oferece proteções no nível do sistema operacional como Windows Defender, projetadas para garantir que o dispositivo não esteja comprometido para começar. No entanto, se um dispositivo cliente for comprometido, um invasor poderá descriptografar as senhas. |

> [!Note]
> Os produtos de terceiros podem fornecer proteção contra modelos de ameaças adicionais, mas isso se deve à complexidade ou à facilidade de uso. O gerenciador de senhas do Microsoft Edge foi projetado para fornecer gerenciamento de senha conveniente e fácil de usar que pode ser totalmente controlado por administradores de TI usando a Política de Grupo e não requer confiança de terceiros.

## <a name="why-doesnt-microsoft-offer-a-master-password-to-protect-the-data"></a>Por que a Microsoft não oferece uma Senha Mestra para proteger os dados?

Quando as senhas do navegador são criptografadas em disco, a chave de criptografia fica disponível para qualquer processo em seu dispositivo, o que inclui qualquer malware que esteja em execução local. Mesmo que as senhas sejam criptografadas em um "cofre" por uma chave mestra, elas serão descriptografadas quando carregadas no espaço de memória do navegador e poderão ser coletadas depois que você desbloquear o cofre.

Um recurso de Senha Mestra (que autentica o usuário antes de preencher automaticamente seus dados) fornece uma compensação na conveniência para uma mitigação mais ampla de ameaças. Especificamente, ele ajuda a reduzir a janela de exposição de dados contra malware latente ou invasores fisicamente locais. No entanto, uma Senha Mestra não é uma panacéia, e invesores locais e malwares dedicados têm várias estratégias para contornar a proteção de uma Senha Mestra.

> [!Note]
> O Microsoft Edge agora oferece a capacidade de habilitar a autenticação antes da funcionalidade de preenchimento automático; isso fornece aos usuários uma camada adicional de privacidade e impede que suas senhas armazenadas sejam usadas por qualquer pessoa, menos eles. Para obter mais detalhes, consulte [Privacidade adicional para suas senhas salvas](https://support.microsoft.com/topic/additional-privacy-for-your-saved-passwords-31dbd670-e314-4901-a546-6f302548502e).  

## <a name="can-using-a-password-manager-impact-my-privacy"></a>O uso de um gerenciador de senhas pode afetar minha privacidade?

Não se forem executadas etapas para proteger o acesso às senhas salvas.

Há uma exploração conhecida que alguns anunciantes usam, que usa senhas armazenadas para identificar e rastrear usuários exclusivamente. Para obter mais informações, consulte  [Os segmentadores de anúncios estão obtendo dados do gerenciador de senhas do seu navegador](https://www.theverge.com/2017/12/30/16829804/browser-password-manager-adthink-princeton-research). Os navegadores executaram etapas para atenuar esse  [problema de privacidade](https://bugs.chromium.org/p/chromium/issues/detail?id=798492). A classe PasswordValueGatekeeper pode ser usada para limitar o acesso aos dados do campo de senha, mesmo quando o navegador estivá configurado para autopreenchimento durante o carregamento.

Essa ameaça de coleta de informações do usuário pode ser facilmente atenuada habilitando o recurso de edge://flags/#fill-on-account-select opcional. Esse recurso só permite que senhas sejam adicionadas a um campo de formulário depois que o usuário escolhe explicitamente uma credencial, o que garante que os usuários fiquem cientes de quem está recebendo suas senhas.

## <a name="see-also"></a>Veja também

[Página de aterrissagem do Microsoft Edge Enterprise](https://www.microsoft.com/edge/business/download)

[Como Microsoft Edge é mais seguro do que o Chrome para empresas Windows 10](/DeployEdge/ms-edge-security-for-business)
