---
title: Proteção desegurança moderna para aplicativos herdados vulneráveis
ms.author: gennlu
author: dan-wesley
manager: kawong
ms.date: 10/26/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Saiba como Microsoft Edge com o modo IE fornece proteção de segurança moderna para aplicativos herdados vulneráveis.
ms.openlocfilehash: 9a0a4b896d9077a04f980340e3b12f3ad18e0b1a
ms.sourcegitcommit: 42f01cad0bf15224222b2aeadb48f03d46c35723
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2021
ms.locfileid: "12154502"
---
# <a name="modern-security-protection-for-vulnerable-legacy-apps"></a>Proteção desegurança moderna para aplicativos herdados vulneráveis

À medida que a Internet evoluiu nos últimos 20 anos, os usuários também desenvolveram necessidades e expectativas em relação aos navegadores que usam. Hoje, a Internet é fundamental para muitas empresas e ter um navegador moderno projetado para atender, com segurança, às necessidades de negócios é fundamental. O Microsoft Edge é um navegador moderno criado para acessar com segurança a Web moderna. Este artigo mostra como o modo Internet Explorer (IE) no Microsoft Edge é mais seguro do que o Internet Explorer.

## <a name="introduction"></a>Introdução

A telemetria interna da Microsoft mostra que o navegador é o aplicativo da área de trabalho nº 1. A centralidade do navegador como uma ferramenta de produtividade diária significa que o navegador apresenta uma grande área de superfície exposta a ataques da Internet. À medida que a Internet e seus aplicativos se tornaram mais complexos, surgiram também ameaças à segurança. Ao longo dos anos, o cenário de ameaças evoluiu e atrainu atores de ameaças sofisticados, incluindo, mas não se limitando a, estados-nações e grupos criminosos organizados que buscam lucro por meio de phishing, ransomware e assim por diante.

Embora tenha evoluído e progredido com iterações até o IE11, o IE ainda se baseia em uma tecnologia que tem 25 anos. É um navegador herdado que está desatualizado e não consegue atender aos desafios de segurança da Web moderna.

Para manter as redes de uma organização seguras contra as ameaças sofisticadas de hoje, os administradores de TI tentam manter os usuários usando um navegador moderno. Isso garante que eles sejam protegidos por recursos de segurança modernos, na maioria do tempo, ou o tempo todo, enquanto navegam.
A prática comum hoje é usar um navegador moderno e o navegador IE é uma solução alternativa conveniente, mas ineficaz. Os usuários que usam o navegador IE para uma atividade podem acabar facilmente usando o IE para todas as atividades, o que nega as proteções que um navegador moderno fornece.

O Microsoft Edge está posicionado exclusivamente para fornecer segurança atualizada, permitindo que os usuários aproveitem ao máximo a tecnologia de segurança moderna.

## <a name="reduce-threat-surface-area"></a>Reduzir a área da superfície de ameaça

Entendemos que modernizar todos os seus sites herdados ao mesmo tempo pode não ser viável. Com Microsoft Edge e o modo IE, você pode usar um navegador moderno seguro para acessar seus sites herdados antes de modernizá-los. O Microsoft Edge com o modo IE usa um sistema de mecanismo duplo exclusivo, que permite abrir sites com o mecanismo IE ou com o novo mecanismo moderno. O mecanismo do navegador é determinado pelo site que você visita. Como o mecanismo do IE mais antigo é menos seguro, você deseja limitar o uso do mecanismo herdado apenas a sites abertos em que confia. Sites confiáveis são sites que você possui, controla ou sabe que não têm vulnerabilidades de segurança. Como prática recomendada, você só deve acessar sites não confiáveis com o mecanismo de navegador moderno porque ele é mais seguro.

O modo IE foi projetado para gerenciar o acesso a sites não confiáveis. O modo IE usa uma "allowlist" em que você identifica os sites confiáveis que podem usar o mecanismo herdado. Qualquer site que não está na lista é aberto automaticamente usando o mecanismo moderno para a experiência de navegação mais segura. O conteúdo não confiável de fontes não confiáveis é sempre gerenciado pelo mecanismo moderno. Com o modo IE, você controla quais sites são renderizados usando o mecanismo herdado e, quando você navega para qualquer outro site, o Microsoft Edge alterna automaticamente para o mecanismo moderno. Como resultado, uma organização não precisa depender do comportamento e das práticas do usuário para autorregistrar e decidir qual navegador usar. Da perspectiva dos usuários, é uma experiência fluida. Eles não precisam pensar sobre qual é o navegador "certo" a ser usado porque o Microsoft Edge abre perfeitamente o site que está tentando acessar, seja ele um site herdado ou um site moderno.

O modo IE é mais seguro do que o IE porque não há suporte para barras de ferramentas, o que reduz a área da superfície para um ataque. As barras de ferramentas são vetores comprovados para ataques de malware e phishing. Além disso, o aplicativo da área de trabalho do IE será desabilitado após a desativação, o que eliminará o tempo que os usuários usam um navegador desatualizado. Os usuários poderão acessar sites e aplicativos herdados confiáveis identificados em uma lista de permissões para o modo IE no Microsoft Edge.

O usuário estará em um ambiente moderno sem precisar ajustar seu comportamento, mas também sem perder o acesso a sites e aplicativos herdados críticos. O Microsoft Edge é o único navegador que permite aos usuários usar um único navegador para acessar sites herdados e modernos.  

A próxima seção explica por quê é importante minimizar o tempo que os usuários gastam usando o mecanismo de navegador herdado.

## <a name="minimize-legacy-browser-use"></a>Minimizar o uso do navegador herdado

As seções a seguir destacam os motivos pelos quais é importante minimizar o uso do mecanismo de navegador herdado.

### <a name="architectural-deficiency"></a>Deficiência arquitetônica

A deficiência arquitetônica no IE se deve ao fato de que sua arquitetura original não contabiliza a complexidade da Web moderna ou do cenário moderno de ameaças. O IE evoluiu de uma arquitetura de processo único que resultou em área restrita inadequada e uma superfície de ataque relativamente ampla. Navegadores modernos como Microsoft Edge são projetados em torno de um modelo de ameaça com base no cenário de ameaças atual. Esses navegadores incluem avanços de segurança, como isolamento de site e recursos de segurança baseados em hardware. Por exemplo, a CET (Tecnologia de Imposição de Fluxo de Controle) da Intel, que lida com muitas ameaças de segurança modernas. Essas mitigações de segurança NÃO estão disponíveis no IE, tornando-o um alvo fácil até mesmo para ataques simples.

### <a name="ease-of-exploitation"></a>Facilidade de exploração

O IE é mais fácil de explorar do que Microsoft Edge devido à sua arquitetura e à falta de suporte para recursos de segurança modernos. É mais fácil encontrar uma única vulnerabilidade no IE que possa levar a uma RCE (Execução Remota de Código) do que encontrar um ponto fraco semelhante no Microsoft Edge, em que várias vulnerabilidades devem ser encadeadas para obter um resultado semelhante. Além disso, os Objetos Auxiliares do ActiveX e do Navegador se tornaram vulnerabilidades e o suporte do IE para eles torna o navegador ainda mais fácil de explorar.  

### <a name="speed-of-security-patching"></a>Velocidade da aplicação de patch de segurança

Os navegadores são um dos aplicativos mais usados na área de trabalho, usados rotineiramente para fazer downloads e manipular conteúdo não confiável de fontes não confiáveis. Para se manter à frente das ameaças à segurança, os navegadores modernos podem implantar atualizações de segurança rapidamente. Como o IE está vinculado ao sistema operacional Windows, as velocidades das atualizações de segurança são limitadas e fazem com que o IE permaneça vulnerável por mais tempo. Ao contrário do IE, Microsoft Edge tem um atualizador interno com uma cadência de atualização muito mais rápida, reduzindo o tempo de resposta para dias em vez de semanas ou meses.

### <a name="security-researcher-ecosystem"></a>Ecossistema de pesquisadores de segurança

Melhorar a segurança do navegador do mundo real depende muito de um amplo ecossistema de pesquisadores de segurança externos incentivados por programas de recompensa para encontrar novas vulnerabilidades e explorações. O Internet Explorer não dá suporte a um programa de recompensas, o que limita o escopo de suas melhorias de segurança. Em comparação, o Microsoft Edge tem um programa de recompensas completo e uma equipe de pesquisa de vulnerabilidade interna para aprimorar a segurança do navegador de última geração. Como o Microsoft Edge é baseado no Chromium Open Source, ele também se beneficia do ecossistema de segurança do navegador do Chromium.

### <a name="phishing-protection-using-smartscreen"></a>Proteção contra phishing usando o SmartScreen

A SmartScreen, tecnologia de proteção contra phishing da Microsoft, bloqueia mais tentativas de phishing <sup>1</sup>e malware <sup>2</sup>do que a Navegação Segura do Google Chrome,  de acordo com um estudo independente da [CyberRatings.org](https://www.cyberratings.org/).

> [!NOTE]
> <sup>1</sup> Navegadores da Web versus Phishing: Relatório de Teste Comparativo (julho de 2021), CyberRatings.org<br>
> <sup>2</sup>Navegadores da Web vs. Malware: Relatório de Teste Comparativo (julho de 2021), CyberRatings.org

O Microsoft Edge oferece suporte nativo completo para SmartScreen, mas o IE só tem suporte parcial devido à sua arquitetura desatualizada.

Além de fornecer avanços de segurança que mapeiam práticas de segurança modernas, o Microsoft Edge é mais seguro do que o Chrome para empresas no Windows 10. O Microsoft Edge também foi projetado para aproveitar os recursos de segurança, a funcionalidade e as ferramentas disponíveis no pacote Microsoft 365 e Windows 10. Esse ecossistema de produtos reduz a complexidade de segurança e privacidade para a equipe de TI. Por exemplo, os investimentos e as decisões tomadas para a identidade no Microsoft 365 podem ser facilmente aplicados ao Microsoft Edge.

O modo IE no Microsoft Edge é uma solução exclusiva que garante que os usuários possam acessar sites herdados de IE críticos e, ao mesmo tempo, permanecer protegidos contra ameaças modernas.

## <a name="see-also"></a>Consulte também

- [Sobre o modo IE](./edge-ie-mode.md)
- [Informações adicionais sobre o Modo Empresarial](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
- [Segurança para os seus negócios](./ms-edge-security-for-business.md)
- [Página de aterrissagem do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)