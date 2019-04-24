---
title: Relacionar o OSC ao Outlook e a redes sociais
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f33705cc-8add-42be-9d9f-f4e9245d83f5
description: O Outlook Social Connector (OSC) pode ser exibido no cartão de contato do Office e nas atividades do Outlook, no status ou nas atualizações de foto de um colega de funcionários, amigo ou pessoa à qual você está associado.
ms.openlocfilehash: 0ee9451e64f12e8ba371c1ba91a1379cff257313
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329251"
---
# <a name="relating-the-osc-with-outlook-and-social-networks"></a>Relacionar o OSC ao Outlook e a redes sociais

O Outlook Social Connector (OSC) pode ser exibido no cartão de contato do Office e nas atividades do Outlook, no status ou nas atualizações de foto de um colega de funcionários, amigo ou pessoa à qual você está associado. Por padrão, o OSC exibe os emails, anexos e solicitações de reunião do Outlook recebidos de uma pessoa selecionada. Se a pessoa selecionada e o usuário do Office colaborarem em um site do SharePoint, o OSC também exibirá atualizações de documentos e outras atividades de site desse site do SharePoint. Dependendo dos contextos de associação nos quais o usuário do Office está interessado, o usuário do Office pode instalar os provedores do OSC para aplicativos de linha de negócios, sites corporativos internos ou vários sites de rede social e profissionais, como o LinkedIn, Facebook e Windows Live.
  
Para dar suporte ao compartilhamento de funcionalidade nos aplicativos cliente do Office, o mecanismo principal do OSC é implementado como parte de um componente compartilhado do Office e o painel de pessoas é implementado como um suplemento do Outlook. Para usar o OSC, um usuário do Office deve ter instalado o Outlook nesse computador cliente e configurar o Outlook com um perfil, para que o OSC possa armazenar em cache contatos em uma pasta de contatos. 
  
Um provedor OSC é uma DLL COM (Component Object Model) que permite ao OSC acessar os dados da rede social de uma maneira que seja independente das APIs de cada rede social. Uma DLL de provedor OSC deve ser instalada localmente em um computador cliente. O provedor OSC de uma rede social conecta o OSC, que faz parte do Outlook, com a rede social na Internet.
  
Um provedor de OSC deve implementar um conjunto de interfaces, definido como parte da extensibilidade do provedor OSC, para se comunicar com o OSC. A extensibilidade do provedor OSC está disponível como uma plataforma aberta.
  
A arquitetura do provedor do OSC permite que vários provedores funcionem com o mecanismo principal do OSC e informações sociais agregadas, como amigos e atividades. A Figura 1 ilustra a arquitetura do provedor OSC.
  
**Figura 1. Arquitetura do provedor do Outlook Social Connector**

![Social networks, OSC providers, OSC, and Office](media/off15OSCRef_Architecture.gif)
  
## <a name="terminology"></a>Terminologia

Nesta referência do provedor do Outlook Social Connector, uma rede social é usada para se referir aos seguintes tipos de sites: 
  
- Sites colaborativos, como o SharePoint.
    
- Sites de redes sociais, como o Facebook e o Windows Live.
    
- Sites de rede profissionais como o LinkedIn.
    
- Outros aplicativos de linha de negócios ou sites internos corporativos usados para redes.
    
O termo Friend é usado geralmente para incluir amigos, familiares, colegas, conexões e qualquer pessoa à qual um usuário do Office esteja associado em um contexto colaborativo, como o SharePoint, ou adicionado à conta de rede social do usuário. Não amigos são pessoas referidas em atualizações de atividade de amigos, mas não são amigos que foram adicionados à conta de rede social do usuário do Office. Contatos são pessoas em uma pasta de contatos do Outlook. 
  
## <a name="see-also"></a>Confira também

- [Introdução ao desenvolvimento de um provedor de serviços do Outlook Social Connector](getting-started-with-developing-an-outlook-social-connector-provider.md)

