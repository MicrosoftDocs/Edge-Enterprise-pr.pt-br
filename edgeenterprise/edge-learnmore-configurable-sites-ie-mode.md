---
title: Microsoft Edge e sites configuráveis no modo IE
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Microsoft Edge e sites configuráveis no modo IE
ms.openlocfilehash: 0248ecd394acee5773751c0685969e3d40940431
ms.sourcegitcommit: 8968f3107291935ed9adc84bba348d5f187eadae
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/12/2021
ms.locfileid: "11978629"
---
# <a name="learn-about-configurable-sites-in-ie-mode"></a>Saiba mais sobre sites configuráveis no modo IE

Este artigo explica o recurso de sites configuráveis na lista de sites do modo empresarial ao usar o modo IE no Microsoft Edge.

## <a name="prerequisites"></a>Pré-requisitos

- Atualizações do Windows

  - Windows 10 versão 1909; Windows Server versão 1909 – KB4550945 ou posterior
  - Windows 10 versão 1903; Windows Server versão 1903 – KB4550945 ou posterior
  - Windows 10 versão 1809; Windows Server versão 1809; e Windows Server 2019 – KB4550969 ou posterior
  - Windows 10 versão 1803 – KB4550944 ou superior
  - Windows 10 versão 1607; Windows Server 2016 – KB4556826 ou superior
  - Versão inicial do Windows 10, julho de 2015 – KB4550947 ou superior
  - Windows 8.1 – KB4556798 ou superior

- Microsoft Edge versão 83 ou posterior
- [Modo IE](./edge-ie-mode.md) configurado com a lista de sites do modo empresarial

## <a name="overview"></a>Visão geral

Configurar sites que precisam do modo IE na lista de sites do modo empresarial funcionará bem na maioria dos ambientes com aplicativos herdados. No entanto, em alguns casos essa abordagem não é a melhor para configurar um subconjunto de sites para abrir no modo do IE sem processar um domínio inteiro no modo do IE. Por exemplo, quando seu ambiente do contém aplicativos modernos e herdados sendo executados em um único servidor, e você gostaria de ter a flexibilidade para renderizar apenas os aplicativos herdados no modo IE e os aplicativos restantes para renderizar no modo Microsoft Edge.

A solução é usar o recurso sites configuráveis da lista de sites do modo empresarial. Quando o recurso está habilitado, o Microsoft Edge permite que os sites com a marca "configurada" participem da determinação do mecanismo do IE.

## <a name="how-configurable-sites-works"></a>Como funcionam os sites configuráveis

### <a name="automatic-switching-from-the-microsoft-edge-engine-to-the-ie-mode-engine"></a>Mudança automática do mecanismo no Microsoft Edge para o mecanismo no modo IE

Para usar o recurso sites configuráveis, você precisará de um ou mais sites na lista de sites do modo empresarial para ter a opção `<open-in>Configurable</open-in>`.

Exemplo:

```
<site-list version="1">
  <site url="app.com">
    <open-in>Configurable</open-in>
  </site>
</site-list>
```

Quando o recurso sites configuráveis estiver habilitado, ocorrerá o seguinte comportamento:

1. Ao fazer uma solicitação para um site configurável, o Microsoft Edge enviará o cabeçalho da solicitação HTTP "`X-InternetExplorerModeConfigurable: 1`".
2. Um site configurável pode enviar uma resposta de redirecionamento (por exemplo, HTTP 302) com o cabeçalho de resposta HTTP "`X-InternetExplorerMode: 1`" para solicitar que o Microsoft Edge carregue o site no modo IE.
3. O destino do redirecionamento (ou seja, o valor do cabeçalho de resposta do Local) também deve ser um siteConfigurável ou **Neutro**, caso contrário, o cabeçalho de resposta do modo IE será ignorado. Espera-se que o destino do redirecionamento geralmente seja igual à URL original. No entanto, não precisa ser.

   > [!NOTE]
   > A resposta de redirecionamento está sujeita ao cache de acordo com o comportamento de cache HTTP normal do Microsoft Edge para redirecionamentos.

### <a name="switching-back-from-ie-mode-engine-to-microsoft-edge-engine"></a>Mudança de um mecanismo do modo IE para o mecanismo do modo Microsoft Edge

Habilitar os sites configuráveis no Microsoft Edge habilita automaticamente os seguintes comportamentos nas guias do modo IE:

1. Ao fazer uma solicitação para um site configurável, as guias do modo IE enviarão o cabeçalho da solicitação HTTP "`X-InternetExplorerModeConfigurable: 1`", da mesma forma que as guias do Microsoft Edge.
2. Um site configurável poderá enviar uma resposta de redirecionamento (por exemplo, HTTP 302) com o cabeçalho de resposta HTTP "`X-InternetExplorerMode: 0`" para solicitar que o a navegação retorne ao modo Microsoft Edge.
3. O destino do redirecionamento (ou seja, o valor do cabeçalho de resposta do **Local**) também deve ser um site**Configurável** ou **Neutro**, caso contrário, o cabeçalho de resposta do modo IE será ignorado. Espera-se que o destino do redirecionamento geralmente seja igual à URL original. No entanto, não precisa ser.

   > [!NOTE]
   > A resposta de redirecionamento está sujeita ao cache de acordo com o comportamento de cache HTTP normal do Microsoft Edge para redirecionamentos.

> [!TIP]
> Os dois mecanismos de navegador enviam o mesmo cabeçalho de solicitação "`X-InternetExplorerModeConfigurable: 1`" aos sites configuráveis. Você deve usar o cabeçalho da solicitação do agente do usuário para diferenciar as solicitações no modo Microsoft Edge versus no modo IE para evitar o redirecionamento quando o site estiver carregando no mecanismo correto.

## <a name="see-also"></a>Consulte também

- [Sobre o modo IE](./edge-ie-mode.md)
- [Informações adicionais sobre o Modo Empresarial](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)