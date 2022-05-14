---
title: Notas da versão do Microsoft Edge para canal beta
ms.author: leahtu
author: dan-wesley
manager: srugh
ms.date: 05/13/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Notas da versão do Microsoft Edge para canal beta
ms.openlocfilehash: 1bc567a58bf055c1b76543b4d86a1e8f6de9343d
ms.sourcegitcommit: faf629ac0acec4081c77c6fee32526edfa08e677
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2022
ms.locfileid: "12513530"
---
# <a name="release-notes-for-microsoft-edge-beta-channel"></a>Notas de versão do canal do Microsoft Edge beta

Estas notas de versão fornecem informações sobre os novos recursos e atualizações não relacionadas à segurança que estão inclusos no canal Beta do Microsoft Edge. As versões arquivadas dessas notas de versão estão disponíveis nas notas [de versão arquivadas para Microsoft Edge Beta Channel](./microsoft-edge-relnote-archive-beta-channel.md).

> [!NOTE]
> A Plataforma da Web do Microsoft Edge evolui constantemente para melhorar a experiência, segurança e privacidade do usuário. Para saber mais, confira [Compatibilidade de sites: alterações que afetam o Microsoft Edge](/microsoft-edge/web-platform/site-impacting-changes).

## <a name="version-1020124512-may-13"></a>Versão 102.0.1245.12: 13 de maio

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-102012457-may-10"></a>Versão 102.0.1245.7: 10 de maio

### <a name="policy-updates"></a>Atualizações de política

#### <a name="new-policies"></a>Novas políticas

- [AllHttpAuthSchemesAllowedForOrigins](/DeployEdge/microsoft-edge-policies#allhttpauthschemesallowedfororigins) – Lista de origens que permitem toda a autenticação HTTP
- [OutlookHubMenuEnabled](/DeployEdge/microsoft-edge-policies#outlookhubmenuenabled) – Permitir que os usuários acessem o Outlook menu
- [NetworkServiceSandboxEnabled](/DeployEdge/microsoft-edge-policies#networkservicesandboxenabled) – Habilitar a área restrita do serviço de rede
- [UserAgentClientHintsGREASEUpdateEnabled](/DeployEdge/microsoft-edge-policies#useragentclienthintsgreaseupdateenabled) - Controlar o recurso User-Agent atualização de GREASE de dicas do cliente

## <a name="version-1010121039-may-5"></a>Versão 101.0.1210.39: 5 de maio

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-1010121031-april-27"></a>Versão 101.0.1210.31: 27 de abril

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-1010121026-april-22"></a>Versão 101.0.1210.26: 22 de abril

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-1010121019-april-18"></a>Versão 101.0.1210.19: 18 de abril

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-1010121014-april-12"></a>Versão 101.0.1210.14: 12 de abril

Vários bugs e problemas de desempenho corrigidos.

### <a name="feature-updates"></a>Atualizações de recursos

- **Melhorias no Gerenciador de Lista de Sites Corporativos.** Agora você pode configurar cookies compartilhados entre o Microsoft Edge e o Internet Explorer em sua lista de sites corporativos. Você pode acessar o [Gerenciador de Lista de Sites Corporativos](/deployedge/edge-ie-mode-site-list-manager) em *edge://compat/SiteListManager*.

## <a name="version-1010121010-april-8"></a>Versão 101.0.1210.10: 8 de abril

### <a name="feature-updates"></a>Atualizações de recursos

- **Capacidade de definir o perfil padrão.** A [política EdgeDefaultProfileEnabled](/DeployEdge/microsoft-edge-policies#edgedefaultprofileenabled) permitirá que você defina um perfil padrão a ser usado ao abrir o navegador em vez do último perfil usado. Essa política não será aplicável se o parâmetro `--profile-directory` tiver sido especificado.

- **Alternador de Certificado do Cliente.** Esse recurso oferecerá uma maneira para os usuários limparem o certificado lembrado e ressurgir o seletor de certificado ao visitar um site que exige autenticação de certificado http. A alternância pode ser feita sem sair manualmente Microsoft Edge.

- **Inicie o Aplicativos Web Progressivo (PWAs) na Barra de Favoritos.** Melhorias na PWA de inicialização começarão a aparecer começando com um ícone de Aplicativos que pode ser adicionado à barra de ferramentas.

- **Gerencie a configuração "Permitir extensões de outras lojas".** Use a [política ControlDefaultStateOfAllowExtensionFromOtherStoresSettingEnabled](/DeployEdge/microsoft-edge-policies#controldefaultstateofallowextensionfromotherstoressettingenabled) para controlar o estado padrão da configuração "Permitir extensões de outros repositórios".

### <a name="policy-updates"></a>Atualizações de política

#### <a name="new-policies"></a>Novas políticas

- [ConfigureKeyboardShortcuts](/DeployEdge/microsoft-edge-policies#configurekeyboardshortcuts) - Configure a lista de comandos para os quais desabilitar atalhos de teclado
- [ControlDefaultStateOfAllowExtensionFromOtherStoresSettingEnabled](/DeployEdge/microsoft-edge-policies#controldefaultstateofallowextensionfromotherstoressettingenabled) - Configurar o estado padrão da configuração Permitir extensões de outras lojas
- [EdgeAssetDeliveryServiceEnabled](/DeployEdge/microsoft-edge-policies#edgeassetdeliveryserviceenabled) - Permitir que recursos baixem ativos do Serviço de Entrega de Ativos
- [EdgeDefaultProfileEnabled](/DeployEdge/microsoft-edge-policies#edgedefaultprofileenabled) - Configuração de perfil padrão habilitada
- [InternetExplorerModeEnableSavePageAs](/DeployEdge/microsoft-edge-policies#internetexplorermodeenablesavepageas) - Permitir Salvar página como no modo Internet Explorer
- [KioskSwipeGesturesEnabled](/DeployEdge/microsoft-edge-policies#kioskswipegesturesenabled) - Deslizar gestos no modo de quiosque do Microsoft Edge habilitado
- [MicrosoftOfficeMenuEnabled](/DeployEdge/microsoft-edge-policies#microsoftofficemenuenabled) - Permitir que os usuários acessem o menu do Microsoft Office
- [SiteSafetyServicesEnabled](/DeployEdge/microsoft-edge-policies#sitesafetyservicesenabled) - Permitir que os usuários configurem os serviços de segurança do site

#### <a name="deprecated-policy"></a>Política preterida

- [ForceCertificatePromptsOnMultipleMatches](/DeployEdge/microsoft-edge-policies#forcecertificatepromptsonmultiplematches) - Configure se o Microsoft Edge deve selecionar automaticamente um certificado quando houver várias correspondências de certificado para um site configurado com "AutoSelectCertificateForUrls"

#### <a name="obsoleted-policy"></a>Política obsoleta

- [WebSQLInThirdPartyContextEnabled](/DeployEdge/microsoft-edge-policies#websqlinthirdpartycontextenabled) - Forçar o WebSQL em contextos de terceiros para ser habilitado novamente


## <a name="version-1000118527-march-31"></a>Versão 100.0.1185.27: 31 de março

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-1000118523-march-28"></a>Versão 100.0.1185.23: 28 de março

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-1000118517-march-23"></a>Versão 100.0.1185.17: 23 de março

Vários bugs e problemas de desempenho corrigidos.

## <a name="version-1000118512-march-18"></a>Versão 100.0.1185.12: 18 de março

Vários bugs e problemas de desempenho corrigidos.

### <a name="feature-updates"></a>Atualizações de recursos

- **Simplificando as Ativações do protocolo de aplicativo do Microsoft 365.** As Ativações do protocolo de aplicativo do Microsoft 365 nos serviços confiáveis de armazenamento em nuvem da Microsoft agora iniciarão determinados aplicativos diretamente do Microsoft 365, incluindo subdomínios do SharePoint e URLs do Microsoft OneDrive. Você pode usar as políticas [AutoLaunchProtocolsComponentEnabled](/deployedge/microsoft-edge-policies#autolaunchprotocolscomponentenabled) e [AutoLaunchProtocolsFromOrigins](/deployedge/microsoft-edge-policies#autolaunchprotocolsfromorigins) para habilitar os prompts de ativação do protocolo de aplicativo, se desejado, e para definir outros aplicativos e serviços em que os avisos são habilitados ou desabilitados.


<!--- from Version 100.0.1185.10: March 17 to Version 99.0.1150.16: February 14 --->
<!--- From Version 99.0.1150.11: February 9 to Version 98.0.1108.27: January 19 --->
<!-- archive from Version 98.0.1108.23: January 14 to Version 97.0.1072.28: December 8 -->
<!--- Version 97.0.1072.21: December 1 to Version 96.0.1054.13: November 5  --->
<!--- archive from Version 96.0.1054.8: November 1 to Version 95.0.1020.14: October 5  --->
<!-- archive from version 95.0.1020.9: September 28 to version 94.0.992.14: September 7 -->
<!-- archive from Version 94.0.992.9: September 2 to Version 92.0.902.40: July 6 -->
<!--Archive from Version 92.0.902.22: June 21 to Version 89.0.774.23: February 8  -->
<!-- Archive from Version 87.0.664.18: October 26 to to version 89.0.774.18: February 3 --->
<!-- Archive from Version 87.0.664.12: October 20 to version 86.0.622.15: September 14 -->
<!--- Archived to version 86.0.622.11: September 9 ---->
<!--- Archived to version 85.0.564.18: July 28 ---->

## <a name="see-also"></a>Consulte também

- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)

