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
description: Entenda como Microsoft Edge identifica e interrompe downloads de arquivos potencialmente perigosos
ms.openlocfilehash: 436c85248ef4012d75a9786c36e8f48d53f720d1
ms.sourcegitcommit: e7f3098d8b7d91cae20b5778a71a87daababc312
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/15/2022
ms.locfileid: "12298189"
---
# <a name="identify-and-interrupt-downloads-of-potentially-dangerous-files"></a>Identificar e interromper downloads de arquivos potencialmente perigosos

Microsoft Edge de Políticas de Tipo de Arquivo da Microsoft Edge classifica os arquivos pelo nível de "periculosidade" para gerenciar downloads de arquivos. Um arquivo inofensivo (por exemplo, um arquivo) pode ser baixado livremente, enquanto um arquivo potencialmente perigoso como um é sujeito a um grau mais alto `.txt` `.dll` de verificação. Esse exame de análise fornece uma experiência de usuário mais consciente de segurança.

## <a name="how-microsoft-edge-determines-the-danger-level-of-a-file-type"></a>Como Microsoft Edge determina o nível de perigo de um tipo de arquivo

Microsoft Edge herda suas políticas de tipo de arquivo do navegador Chromium upstream. Você pode exibir esses tipos de arquivo e sua classificação [no arquivo download_file_types.asciipb.](https://source.chromium.org/chromium/chromium/src/+/main:components/safe_browsing/core/resources/download_file_types.asciipb;drc=af17ad3f07c1d8a24381eb7669bec0c2ffb86521) Neste arquivo, você verá que cada tipo tem um danger_level **,** que é um dos três valores: , `DANGEROUS` ou `NOT_DANGEROUS` `ALLOW_ON_USER_GESTURE` .

As duas classificações a seguir são simples:

- **NOT_DANGEROUS** significa que o arquivo é seguro para baixar, mesmo que a solicitação de download foi acidental.
- **DANGEROUS** significa que o navegador sempre deve avisar o usuário de que o download pode prejudicar seu dispositivo.

A terceira configuração, **ALLOW_ON_USER_GESTURE** é mais sutil. Esses arquivos são potencialmente perigosos, mas provavelmente são inofensivos se o usuário solicitar o download. Microsoft Edge permitirá que esses downloads continuem automaticamente se uma das seguintes condições for atendida:

- Há um gesto [do usuário associado](https://textslashplain.com/2020/05/18/browser-basics-user-gestures/) à solicitação de rede que iniciou o download. Por exemplo, o usuário clicou em um link para o download.
- Há uma visita anterior gravada à origem de referência (a página que vincula ao download) antes da meia-noite mais recente (ou seja, ontem ou anterior). Essa visita gravada implica que o usuário tem um histórico de visita ao site.

O download também continuará automaticamente se o usuário o iniciar explicitamente usando o **link** Salvar como comando de menu de contexto, inserirá a URL do download diretamente na barra de endereços do navegador ou se Microsoft Defender SmartScreen indicar que o arquivo está seguro.

> [!NOTE]
> A partir da versão 91, Microsoft Edge interromperá downloads que não têm o gesto necessário.

## <a name="user-experience-for-downloads-that-lack-a-gesture"></a>Experiência do usuário para downloads que não têm um gesto

Se um download para um tipo potencialmente perigoso for iniciado sem o gesto necessário, Microsoft Edge afirma que o download "foi bloqueado". Comandos `Keep` `Delete` nomeados e estão disponíveis no **...** (reellipse) opção no item de download para permitir que o usuário continue ou cancele o download.

:::image type="content" source="media/microsoft-edge-security-Download-interruptions/Dowload-was-blocked.png" alt-text="O download está bloqueado, o usuário pode manter ou excluir o download.":::

Na `edge://downloads` página, o usuário verá as mesmas opções. A próxima captura de tela mostra e exemplo dessas opções.

:::image type="content" source="media/microsoft-edge-security-Download-interruptions/msg-keep-delete-option.png" alt-text="O download está bloqueado, mas o usuário pode manter ou excluir o download.":::

## <a name="enterprise-controls-for-downloads"></a>Enterprise controles para downloads

Embora os usuários não possam encontrar interrupções de download para sites que usam todos os dias, eles podem encontrar para downloads legítimos em sites que usam raramente. Para ajudar a simplificar a experiência do usuário para empresas, uma Política de Grupo está disponível.

As empresas podem usar [ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](/deployedge/microsoft-edge-policies#exemptdomainfiletypepairsfromfiletypedownloadwarnings) para especificar os tipos de arquivo que podem ser baixados de sites específicos sem interrupção. Por exemplo, a política a seguir permite baixar arquivos XML de contoso.com e woodgrovebank.com sem interrupção, e arquivos MSG baixam de qualquer site.

`[{"file_extension":"xml","domains":["contoso.com", "woodgrovebank.com"]},
{"file_extension":"msg", "domains": ["*"]}]`

## <a name="file-types-requiring-a-gesture"></a>Tipos de arquivo que exigem um gesto

As [políticas de tipos de arquivo](https://source.chromium.org/chromium/chromium/src/+/main:components/safe_browsing/core/resources/download_file_types.asciipb;drc=af17ad3f07c1d8a24381eb7669bec0c2ffb86521) mais recentes são publicadas no código-fonte do Chromium. A partir de maio de 2021, os tipos de arquivo com um `danger_level` de `ALLOW_ON_USER_GESTURE` em pelo menos uma plataforma do sistema operacional  incluem:
`crx, pl, py, pyc, pyo, pyw, rb, efi, oxt, msi, msp, mst, ade, adp, mad, maf, mag, mam, maq, mar, mas, mat, mav, maw, mda, mdb, mde, mdt, mdw, mdz, accdb, accde, accdr, accda, ocx, ops, paf, pcd, pif, plg, prf, prg, pst, cpi, partial, xrm-ms, rels, svg, xml, xsl, xsd, ps1, ps1xml, ps2, ps2xml, psc1, psc2, js, jse, vb, vbe, vbs, vbscript, ws, wsc, wsf, wsh, msh, msh1, msh2, mshxml, msh1xml, msh2xml, ad, app, application, appref-ms, asp, asx, bas, bat, chi, chm, cmd, com, cpl, crt, cer, der, eml, exe, fon, fxp, hlp, htt, inf, ins, inx, isu, isp, job, lnk, mau, mht, mhtml, mmc, msc, msg, reg, rgs, scr, sct, search-ms, settingcontent-ms, shb, shs, slk, u3p, vdx, vsx, vtx, vsdx, vssx, vstx, vsdm, vssm, vstm, vsd, vsmacros, vss, vst, vsw, xnk, cdr, dart, dc42, diskcopy42, dmg, dmgpart, dvdr, dylib, img, imgpart, ndif, service, smi, sparsebundle, sparseimage, toast, udif, action, definition, wflow, caction, as, cpgz, command, mpkg, pax, workflow, xip, mobileconfig, configprofile, internetconnect, networkconnect, pkg, deb, pet, pup, rpm, slp, out, run, bash, csh, ksh, sh, shar, tcsh, desktop, dex,apk`

## <a name="the-file-type-danger-level-may-vary-by-operating-system"></a>O nível de perigo do tipo de arquivo pode variar de acordo com o sistema operacional

Às vezes, as configurações de tipo de arquivo variam dependendo da plataforma do sistema operacional cliente. Por exemplo, um arquivo não é perigoso em um Mac, enquanto um `.exe` `.applescript` arquivo é inofensivo Windows.
