---
title: Identificar e interromper downloads de arquivos potencialmente perigosos
ms.author: kvice
author: AndreaLBarr
manager: srugh
ms.date: 01/10/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Entender como o Microsoft Edge identifica e interrompe downloads de arquivos potencialmente perigosos
ms.openlocfilehash: d5bd4e21045ae1615f66d208ece7d6cf1acb41e7
ms.sourcegitcommit: 8a2193791e6606a4dced9808013d6b064d2f2319
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/15/2022
ms.locfileid: "12753916"
---
# <a name="identify-and-interrupt-downloads-of-potentially-dangerous-files"></a>Identificar e interromper downloads de arquivos potencialmente perigosos

O componente Políticas de Tipo de Arquivo do Microsoft Edge classifica os arquivos pelo nível de "perigo" para gerenciar downloads de arquivos. Um arquivo inofensivo (por exemplo, `.txt` um arquivo) pode ser baixado livremente, `.dll` enquanto um arquivo potencialmente perigoso como um está sujeito a um grau mais alto de habilitação. Esse exame fornece uma experiência de usuário mais consciente de segurança.

## <a name="how-microsoft-edge-determines-the-danger-level-of-a-file-type"></a>Como o Microsoft Edge determina o nível de perigo de um tipo de arquivo

O Microsoft Edge herda suas políticas de tipo de arquivo do navegador Chromium upstream. Você pode exibir esses tipos de arquivo e sua classificação [no arquivo download_file_types.asciipb](https://source.chromium.org/chromium/chromium/src/+/main:components/safe_browsing/core/resources/download_file_types.asciipb;drc=af17ad3f07c1d8a24381eb7669bec0c2ffb86521) . Nesse arquivo, você verá que cada tipo tem um **danger_level, que** é um dos três valores: `DANGEROUS`, `NOT_DANGEROUS`ou `ALLOW_ON_USER_GESTURE`.

As duas classificações a seguir são simples:

- **NOT_DANGEROUS** significa que o arquivo é seguro para download, mesmo que a solicitação de download seja acidental.
- **DANGEROUS** significa que o navegador sempre deve avisar o usuário de que o download pode prejudicar seu dispositivo.

A terceira configuração, **ALLOW_ON_USER_GESTURE** é mais sutil. Esses arquivos são potencialmente perigosos, mas provavelmente inofensivos se o usuário solicitar o download. O Microsoft Edge permitirá que esses downloads continuem automaticamente se **duas** condições **forem atendidas** :

- Há um gesto do [usuário associado](https://textslashplain.com/2020/05/18/browser-basics-user-gestures/) à solicitação de rede que iniciou o download. Por exemplo, o usuário clicou em um link para o download.
- Há uma visita anterior registrada à origem de referência (a página vinculada ao download) antes da meia-noite mais recente (ou seja, ontem ou anterior). Essa visita gravada implica que o usuário tem um histórico de visita ao site.

O download também continuará automaticamente se o usuário o iniciar explicitamente usando o **link** Salvar como comando de menu de contexto, inserir a URL do download diretamente na barra de endereços do navegador ou se o Microsoft Defender SmartScreen indicar que o arquivo é seguro.

> [!NOTE]
> A partir da versão 91, o Microsoft Edge interromperá os downloads que não têm o gesto necessário.

## <a name="user-experience-for-downloads-that-lack-a-gesture"></a>Experiência do usuário para downloads que não têm um gesto

Se um download para um tipo potencialmente perigoso começar sem o gesto necessário, o Microsoft Edge declara que o download "foi bloqueado". Comandos nomeados `Keep` `Delete` e estão disponíveis no **...** (reticências) no item de download para permitir que o usuário continue ou cancele o download.

:::image type="content" source="media/microsoft-edge-security-Download-interruptions/Dowload-was-blocked.png" alt-text="O download está bloqueado, o usuário pode manter ou excluir o download.":::

Na página `edge://downloads` , o usuário verá as mesmas opções. A próxima captura de tela mostra e exemplo dessas opções.

:::image type="content" source="media/microsoft-edge-security-Download-interruptions/msg-keep-delete-option.png" alt-text="O download está bloqueado, mas o usuário pode manter ou excluir o download.":::

## <a name="enterprise-controls-for-downloads"></a>Controles empresariais para downloads

Embora os usuários não possam encontrar interrupções de download para sites que usam todos os dias, eles podem encontrar para downloads legítimos em sites que usam raramente. Para ajudar a simplificar a experiência do usuário para empresas, uma Política de Grupo está disponível.

As empresas podem usar [ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](/deployedge/microsoft-edge-policies#exemptdomainfiletypepairsfromfiletypedownloadwarnings) para especificar os tipos de arquivo que podem ser baixados de sites específicos sem interrupção. Por exemplo, a política a seguir permite que os arquivos XML baixem de contoso.com e woodgrovebank.com sem interrupção e os arquivos MSG baixam de qualquer site.

`[{"file_extension":"xml","domains":["contoso.com", "woodgrovebank.com"]},
{"file_extension":"msg", "domains": ["*"]}]`

## <a name="file-types-requiring-a-gesture"></a>Tipos de arquivo que exigem um gesto

As [políticas de tipos de arquivo](https://source.chromium.org/chromium/chromium/src/+/main:components/safe_browsing/core/resources/download_file_types.asciipb;drc=af17ad3f07c1d8a24381eb7669bec0c2ffb86521) mais recentes são publicadas no código-fonte do Chromium. A partir de maio de 2021, os tipos de arquivo com um `danger_level` de `ALLOW_ON_USER_GESTURE` em pelo menos uma plataforma do sistema operacional  incluem:
`crx, pl, py, pyc, pyo, pyw, rb, efi, oxt, msi, msp, mst, ade, adp, mad, maf, mag, mam, maq, mar, mas, mat, mav, maw, mda, mdb, mde, mdt, mdw, mdz, accdb, accde, accdr, accda, ocx, ops, paf, pcd, pif, plg, prf, prg, pst, cpi, partial, xrm-ms, rels, svg, xml, xsl, xsd, ps1, ps1xml, ps2, ps2xml, psc1, psc2, js, jse, vb, vbe, vbs, vbscript, ws, wsc, wsf, wsh, msh, msh1, msh2, mshxml, msh1xml, msh2xml, ad, app, application, appref-ms, asp, asx, bas, bat, chi, chm, cmd, com, cpl, crt, cer, der, eml, exe, fon, fxp, hlp, htt, inf, ins, inx, isu, isp, job, lnk, mau, mht, mhtml, mmc, msc, msg, reg, rgs, scr, sct, search-ms, settingcontent-ms, shb, shs, slk, u3p, vdx, vsx, vtx, vsdx, vssx, vstx, vsdm, vssm, vstm, vsd, vsmacros, vss, vst, vsw, xnk, cdr, dart, dc42, diskcopy42, dmg, dmgpart, dvdr, dylib, img, imgpart, ndif, service, smi, sparsebundle, sparseimage, toast, udif, action, definition, wflow, caction, as, cpgz, command, mpkg, pax, workflow, xip, mobileconfig, configprofile, internetconnect, networkconnect, pkg, deb, pet, pup, rpm, slp, out, run, bash, csh, ksh, sh, shar, tcsh, desktop, dex,apk`

## <a name="the-file-type-danger-level-may-vary-by-operating-system"></a>O nível de perigo do tipo de arquivo pode variar de acordo com o sistema operacional

Às vezes, as configurações de tipo de arquivo variam dependendo da plataforma do sistema operacional cliente. Por exemplo, um `.exe` arquivo não é perigoso em um Mac, enquanto um `.applescript` arquivo é inofensivo no Windows.
