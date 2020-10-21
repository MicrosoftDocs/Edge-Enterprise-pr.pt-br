---
title: Acessar a versão antiga do Microsoft Edge
ms.author: jtkim
author: dan-wesley
manager: srugh
ms.date: 08/17/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Saiba como acessar a versão herdada do Microsoft Edge.
ms.openlocfilehash: e4733d020f3a681ded50e5a087fe086d39362201
ms.sourcegitcommit: f7f7eb69d2298b0f9779a9fd28e3c4e297ef2e05
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125513"
---
# Acessar a Versão Herdada do Microsoft Edge depois de instalar a nova versão do Microsoft Edge

Saiba como acessar a Versão Herdada do Microsoft Edge depois de instalar a nova versão do Microsoft Edge.

> [!NOTE]
> Este artigo aplica-se ao [canal Estável](microsoft-edge-channels.md) do Microsoft Edge.

Embora a maioria das organizações queira substituir o Microsoft Edge Legacy pela nova versão, há algumas situações em que os usuários precisarão acessar as duas versões. Por exemplo:

- Assistência técnica e equipe de suporte que interagem com os usuários que estão usando uma ou ambas as versões do Microsoft Edge.
- Desenvolvedores que oferecem suporte aos clientes que usam uma ou ambas as versões do Microsoft Edge.

> [!IMPORTANT]
> Executar a Versão Prévia do Microsoft Edge lado a lado com a nova versão do Microsoft Edge não é recomendável para uso em produção. Essa configuração deve ser usada apenas em casos específicos em que é necessário testar as versões do navegador.
>
> O aplicativo de área de trabalho da Versão Prévia do Microsoft Edge chegará ao fim do suporte em 9 de março de 2021 em favor do novo Microsoft Edge. Isso significa que a Versão Prévia do Microsoft Edge não receberá atualizações de segurança após essa data. Essa alteração é aplicável a todas as experiências executadas no aplicativo da área de trabalho da Versão Prévia do Microsoft Edge. [Saiba mais](https://techcommunity.microsoft.com/t5/microsoft-365-blog/microsoft-365-apps-say-farewell-to-internet-explorer-11-and/ba-p/1591666).

## Antes de começar
> [!NOTE]
> A partir do Windows 10 versão 20H2 a Versão Prévia do Microsoft Edge não está mais incluída. A experiência lado a lado não é compatível com esta versão do Windows 10.

Os procedimentos neste artigo se aplicam aos sistemas que foram atualizados com as últimas atualizações de segurança. Quando a nova versão do Microsoft Edge estiver instalada, a versão antiga (Versão Herdada do Microsoft Edge) será ocultada. Por padrão, todas as tentativas de iniciar a versão antiga irão redirecionar o usuário para a versão recém-instalada do Microsoft Edge. Este artigo descreve como você pode continuar usando o Microsoft Edge herdado após instalar o Microsoft Edge.

## QuickStart: experiência lado a lado com o Microsoft Edge Beta e a Versão Prévia do Microsoft Edge

Antes de usar as instruções detalhadas deste artigo, considere as duas etapas a seguir para permitir que os usuários executem a Versão Prévia do Microsoft Edge e o Microsoft Edge ([canal Beta](microsoft-edge-channels.md)) lado a lado.

1. Impeça a instalação automática do Canal Estável de Microsoft Edge pelo [Windows Update.](https://support.microsoft.com/help/12373/windows-update-faq).

   > [!TIP]
   > Use o [Blocker Toolkit](microsoft-edge-blocker-toolkit.md) para desabilitar a entrega automática do Microsoft Edge.

2. Instale o [canal Beta](https://www.microsoft.com/edge/business/download) da nova versão do Microsoft Edge.

   > [!NOTE]
   > Leia [Informações adicionais](#additional-information) para saber mais sobre as configurações de chave do registro.

Essa solução lado a lado é menos complexa e requer menos gerenciamento do que a solução detalhada descrita neste artigo. No entanto, isso significa que você estará executando o canal Beta em vez do canal Estável.

## Experiência lado a lado com o canal estável do Microsoft Edge e a Versão Prévia do Microsoft Edge

Instalar o canal Estável da próxima versão do Microsoft Edge no nível do sistema fará com que a versão atual (Versão Herdada do Microsoft Edge) seja ocultada. Para permitir que os usuários vejam as duas versões do Microsoft Edge lado a lado no Windows, você poderá habilitar essa experiência ao definir a política de grupo **Permitir experiência de navegador Lado a Lado do Microsoft Edge** como **Habilitada**.

Essa política de grupo é documentada [aqui](https://docs.microsoft.com/deployedge/microsoft-edge-update-policies#allowsxs)

### Para configurar a política de experiência do navegador lado a lado:

1. Instalar as definições de política do [Microsoft Edge for Business](https://www.microsoft.com/edge/business/download).

   - Escolha o CANAL/BUILD e a plataforma que você deseja usar e, em seguida, clique em OBTER ARQUIVOS DE POLÍTICA.
   - Extraia o arquivo compactados.
   - Copie msedge.admx e msedgeupdate.admx para o diretório `C:\Windows\PolicyDefinitions`.
   - Copie msedge.adml e msedgeupdate.adml (do diretório de idioma/local apropriado) para o diretório `C:\Windows\PolicyDefinitions\[APPROPRIATE LANGUAGE/LOCALE]`.

2. Abra o Editor de Política de Grupo (gpedit.msc).
3. Em **Configuração do Computador**, vá para *Modelos Administrativos>Microsoft Edge Update>Aplicativos*.

    > [!NOTE]
    > Se você não vir * Microsoft Edge Update*, verifique se a etapa 1 foi concluída corretamente.

4. Em **Aplicativos**, clique duas vezes em "Permitir a experiência de navegador Lado a Lado do Microsoft Edge". Veja nossas [práticas recomendadas](#best-practice-guidance) antes de passar para a próxima etapa.

    > [!NOTE]
    > Por padrão, essa política de grupo é definida como "Não configurada", o que resultará na Versão Herdada do Microsoft Edge sendo ocultada quando a nova versão do Microsoft Edge for instalada.

5. Selecione **Habilitado** e, em seguida, clique em **OK**.  

Definir essa política definirá a seguinte chave do Registro como '00000001':

- Chave: `Computer\HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate`
- Nome do valor: `Allowsxs`
- Tipo de valor: `'REG_DWORD'`

#### Diretrizes de prática recomendada

Para a melhor experiência, **Permitir experiência de navegador Lado a Lado do Microsoft Edge** deve ser habilitado antes que a nova versão do Microsoft Edge seja implantada nos dispositivos dos usuários.

Se a política de grupo for habilitada depois que o Microsoft Edge tiver sido implantado, haverá os seguintes efeitos colaterais e as ações necessárias:

1. **Permitir experiência de navegador Lado a Lado do Microsoft Edge** não entrará em vigor até o instalador da nova versão do Microsoft Edge ser executado novamente.

   > [!NOTE]
   > O instalador pode ser executado direta ou automaticamente quando a nova versão do Microsoft Edge for atualizada.

2. A Versão Herdada do Microsoft Edge precisará ser fixada novamente em Iniciar ou na Barra de Tarefas porque o marcador será migrado quando a nova versão do Microsoft Edge for implantada.
3. Os sites fixados em Iniciar ou na Barra de Tarefas para a Versão Herdada do Microsoft Edge serão migrados para a nova versão do Microsoft Edge.

## Informações adicionais

Depois que os sistemas forem totalmente atualizados e o canal Estável da próxima versão do Microsoft Edge for instalado, a seguinte chave do Registro e o valor serão definidos:

- Chave: `Computer\HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\EdgeUpdate\ClientState\{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}`
- Valor da chave: `BrowserReplacement`

  > [!IMPORTANT]
  > Essa chave é substituída sempre que o canal Estável do Microsoft Edge é atualizado. Como uma prática recomendada, recomendamos que você NÃO exclua essa chave para permitir que os usuários acessem as duas versões do Microsoft Edge.

## Consulte também

- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Atualizações do Windows para dar suporte ao Microsoft Edge](microsoft-edge-sysupdate-windows-updates.md)
