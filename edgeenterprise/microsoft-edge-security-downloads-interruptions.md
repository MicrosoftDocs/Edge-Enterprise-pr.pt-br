---
title: Interrompendo downloads de arquivos potencialmente perigosos
ms.author: kvice
author: AndreaLBarr
manager: srugh
ms.date: 05/20/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Interrompendo downloads de arquivos potencialmente perigosos
ms.openlocfilehash: 6239fd766c9e10d070188133a84ec0d7ce42a882
ms.sourcegitcommit: 4192328ee585bc32a9be528766b8a5a98e046c8e
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/25/2021
ms.locfileid: "11618026"
---
# <a name="interrupting-downloads-of-potentially-dangerous-files"></a>Interrompendo downloads de arquivos potencialmente perigosos

O componente Políticas de Tipo de Arquivo do Microsoft Edge permite que os arquivos sejam classificados pelo nível de "periculosidade", de forma que arquivos inofensivos (por exemplo, arquivos `.txt`) possam ser baixados livremente, enquanto arquivos potencialmente perigosos (por exemplo, arquivos `.dll`) estão sujeitos a um grau mais alto de verificação e uma experiência de usuário mais consciente de segurança.

## <a name="determining-the-danger-level-of-a-file-type"></a>Determinando o Nível de perigo de um Tipo de arquivo

Microsoft Edge herda suas políticas de tipo de arquivo do navegador Chromium upstream; você pode exibir o conteúdo atual da lista [aqui](https://source.chromium.org/chromium/chromium/src/+/main:components/safe_browsing/core/resources/download_file_types.asciipb). Dentro da lista, você verá que cada tipo tem um danger_level, que é um dos três valores: `DANGEROUS`, `NOT_DANGEROUS` ou `ALLOW_ON_USER_GESTURE`.

Os dois primeiros são simples: **NOT_DANGEROUS** significa que o arquivo é seguro para baixar, mesmo se o download foi acidental. **DANGEROUS** significa que o navegador sempre deve avisar o usuário de que o download pode prejudicar seu dispositivo.

A terceira configuração **ALLOW_ON_USER_GESTURE** é mais sutil. Esses arquivos são potencialmente perigosos, mas provavelmente são inofensivos se o usuário solicitou o download. O Microsoft Edge permitirá que esses downloads prossigam automaticamente se duas condições forem atendidas:

1. Há um [gesto do usuário](https://textslashplain.com/2020/05/18/browser-basics-user-gestures/) associado à solicitação de rede que iniciou o download (por exemplo, o usuário clicou em um link para o download).
2. Há uma visita anterior registrada à origem de referência (a página que vincula ao download) antes da meia-noite mais recente (ou seja, ontem ou anterior). Isso implica que o usuário tem um histórico de visita ao site.

O download também prosseguirá automaticamente se o usuário o iniciou explicitamente usando o comando de menu de contexto **Salvar link como**, inseriu a URL do download diretamente na barra de endereços do navegador ou se o Microsoft Defender SmartScreen indicou que o arquivo é seguro.

**Atualização:** A partir da versão 91, o Microsoft Edge interromperá downloads que não tenham o gesto necessário.

## <a name="user-experience-for-downloads-lacking-gestures"></a>Experiência do usuário para downloads sem gestos

Se um download para um tipo potencialmente perigoso for iniciado sem o gesto necessário, o Microsoft Edge afirmará que o download "foi bloqueado". Comandos nomeados `Keep` e `Delete` estão disponíveis a partir do ... menu no item de download para permitir que o usuário continue ou cancele o download.

:::image type="content" source="media/microsoft-edge-security-Download-interruptions/Dowload-was-blocked.png" alt-text="Download foi bloqueado":::

Na página `edge://downloads`, o usuário verá as mesmas opções:

:::image type="content" source="media/microsoft-edge-security-Download-interruptions/msg-keep-delete-option.png" alt-text="Opção Manter Exclusão do MSG":::

## <a name="enterprise-controls"></a>Controles Empresariais

Embora os usuários não possam encontrar interrupções de download para sites que usam todos os dias, eles podem encontrar para downloads legítimos em sites que usam raramente. Para ajudar a simplificar a experiência do usuário para empresas, uma Política de Grupo está disponível.

As empresas podem usar [ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](/deployedge/microsoft-edge-policies#exemptdomainfiletypepairsfromfiletypedownloadwarnings) para especificar os tipos de arquivo que podem ser baixados de sites específicos sem interrupção. Por exemplo, a política a seguir permite que arquivos XML sejam baixados de contoso.com e woodgrovebank.com sem interrupção e arquivos MSG sejam baixados de qualquer site.

`[{"file_extension":"xml","domains":["contoso.com", "woodgrovebank.com"]},
{"file_extension":"msg", "domains": ["*"]}]`

## <a name="file-types-requiring-a-gesture"></a>Tipos de arquivo que exigem um gesto

As [políticas de tipos de arquivo](https://source.chromium.org/chromium/chromium/src/+/main:components/safe_browsing/core/resources/download_file_types.asciipb) mais recentes são publicadas no código-fonte do Chromium. A partir de maio de 2021, os tipos de arquivo com um `danger_level` de `ALLOW_ON_USER_GESTURE` em pelo menos uma plataforma do sistema operacional  incluem:
`crx, pl, py, pyc, pyo, pyw, rb, efi, oxt, msi, msp, mst, ade, adp, mad, maf, mag, mam, maq, mar, mas, mat, mav, maw, mda, mdb, mde, mdt, mdw, mdz, accdb, accde, accdr, accda, ocx, ops, paf, pcd, pif, plg, prf, prg, pst, cpi, partial, xrm-ms, rels, svg, xml, xsl, xsd, ps1, ps1xml, ps2, ps2xml, psc1, psc2, js, jse, vb, vbe, vbs, vbscript, ws, wsc, wsf, wsh, msh, msh1, msh2, mshxml, msh1xml, msh2xml, ad, app, application, appref-ms, asp, asx, bas, bat, chi, chm, cmd, com, cpl, crt, cer, der, eml, exe, fon, fxp, hlp, htt, inf, ins, inx, isu, isp, job, lnk, mau, mht, mhtml, mmc, msc, msg, reg, rgs, scr, sct, search-ms, settingcontent-ms, shb, shs, slk, u3p, vdx, vsx, vtx, vsdx, vssx, vstx, vsdm, vssm, vstm, vsd, vsmacros, vss, vst, vsw, xnk, cdr, dart, dc42, diskcopy42, dmg, dmgpart, dvdr, dylib, img, imgpart, ndif, service, smi, sparsebundle, sparseimage, toast, udif, action, definition, wflow, caction, as, cpgz, command, mpkg, pax, workflow, xip, mobileconfig, configprofile, internetconnect, networkconnect, pkg, deb, pet, pup, rpm, slp, out, run, bash, csh, ksh, sh, shar, tcsh, desktop, dex,apk`

## <a name="danger-level-may-vary-by-operating-system"></a>O nível de perigo pode variar de acordo com o sistema operacional

Às vezes, as configurações de tipo de arquivo variam dependendo da plataforma do sistema operacional cliente. Por exemplo, um `.exe` não é perigoso em um Mac, enquanto um `.applescript` é inofensivo no Windows.
