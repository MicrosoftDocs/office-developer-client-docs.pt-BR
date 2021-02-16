---
title: Relacionar o OSC ao Outlook e a redes sociais
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f33705cc-8add-42be-9d9f-f4e9245d83f5
description: O Outlook Social Connector (OSC) pode ser exibido nas atividades, status ou atualizações do Painel de Pessoas do Office e do Painel de Pessoas do Outlook para um colega de trabalho, amigo ou qualquer pessoa com quem você está associado.
ms.openlocfilehash: 0ee9451e64f12e8ba371c1ba91a1379cff257313
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428008"
---
# <a name="relating-the-osc-with-outlook-and-social-networks"></a>Relacionar o OSC ao Outlook e a redes sociais

O Outlook Social Connector (OSC) pode ser exibido nas atividades, status ou atualizações do Painel de Pessoas do Office e do Painel de Pessoas do Outlook para um colega de trabalho, amigo ou qualquer pessoa com quem você está associado. Por padrão, o OSC exibe os emails, anexos e solicitações de reunião do Outlook recebidos de uma pessoa selecionada. Se a pessoa selecionada e o usuário do Office colaborarem em um site do SharePoint, o OSC também exibirá atualizações de documentos e outras atividades de site desse site do SharePoint. Dependendo dos contextos de associação em que o usuário do Office está interessado, o usuário do Office pode instalar provedores OSC para aplicativos de linha de negócios, sites corporativos internos ou uma variedade de sites de redes sociais e profissionais, como LinkedIn, Facebook e Windows Live.
  
Para dar suporte ao compartilhamento de funcionalidades entre aplicativos cliente do Office, o mecanismo principal do OSC é implementado como parte de um componente compartilhado do Office e o Painel de Pessoas é implementado como um complemento do Outlook. Para usar o OSC, um usuário do Office deve ter instalado o Outlook no computador cliente e configurado o Outlook com um perfil, para que o OSC possa armazenar em cache contatos em uma pasta Contatos. 
  
Um provedor de OSC é um Component Object Model (COM) DLL que permite o OSC acessar dados de redes sociais de forma independente das APIs de cada rede social. Uma DLL do provedor OSC deve ser instalada localmente em um computador cliente. O provedor osC de uma rede social conecta o OSC, que faz parte do Outlook, com a rede social na Internet.
  
Um provedor OSC deve implementar um conjunto de interfaces, definido como parte da extensibilidade do provedor OSC, para se comunicar com o OSC. A extensibilidade do provedor OSC está disponível como uma plataforma aberta.
  
A arquitetura de provedor do OSC permite que vários provedores trabalhem com o mecanismo principal do OSC e agregam informações sociais, como amigos e atividades. A Figura 1 ilustra a arquitetura do provedor OSC.
  
**Figura 1. Arquitetura do provedor do Outlook Social Connector**

![Social networks, OSC providers, OSC, and Office](media/off15OSCRef_Architecture.gif)
  
## <a name="terminology"></a>Terminologia

Nesta Referência do Provedor do Outlook Social Connector, uma rede social é usada para se referir aos seguintes tipos de sites: 
  
- Sites colaborativos, como o SharePoint.
    
- Sites de redes sociais, como Facebook e Windows Live.
    
- Sites de rede profissionais, como o LinkedIn.
    
- Outros aplicativos de linha de negócios ou sites internos corporativos usados para rede.
    
O termo amigo geralmente é usado para incluir amigos, familiares, colegas, conexões e qualquer outra pessoa à qual um usuário do Office está associado em um contexto colaborativo, como o SharePoint, ou adicionou à conta de rede social do usuário. Não amigos são pessoas referenciadas nas atualizações de atividades dos amigos, mas não são amigos que foram adicionados à conta de rede social do usuário do Office. Contatos são pessoas em uma pasta de contatos do Outlook. 
  
## <a name="see-also"></a>Confira também

- [Introdução ao desenvolvimento de um provedor de serviços do Outlook Social Connector](getting-started-with-developing-an-outlook-social-connector-provider.md)

