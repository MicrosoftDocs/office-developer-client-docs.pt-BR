---
title: Sequências de chamadas típicas de OSC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f61960f7-e018-4d2e-8e32-426ed46d9064
description: Esta seção descreve as sequências de chamada típica Outlook Social Connector (OSC) de membros em interfaces de extensibilidade do provedor de OSC, que implementa um provedor OSC.
ms.openlocfilehash: 4a79e27fadb78933f41f26818cfab8b7f4a5aae7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770943"
---
# <a name="osc-typical-calling-sequences"></a>Sequências de chamadas típicas de OSC

Esta seção descreve as sequências de chamada típica Outlook Social Connector (OSC) de membros em interfaces de extensibilidade do provedor de OSC, que implementa um provedor OSC. As sequências de chamada típicas ilustram como e quando o OSC usa tais interfaces e métodos, para permitir a melhor determinam como implementar um determinado membro em uma interface de extensibilidade do provedor. A sequência de chamada real pode variar dependendo dos recursos retornados pelo método [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) . Exemplos de recursos incluem o seguinte: 
  
- Provedor de suporte para obtenção, cache ou procurando dinamicamente amigos e atividades da rede social.
    
- Interface do usuário que o OSC deve ser exibida para logon do usuário.
    
- O tipo de autenticação (por exemplo, autenticação baseada em formulários) que o OSC deve usar.
    
## <a name="in-this-section"></a>Nesta seção

- [A autenticação básica](basic-authentication.md): descreve a sequência de chamada típica do OSC para dar suporte a um usuário do Office que está conectado a uma rede social, se o provedor do OSC suportar a autenticação básica.
    
- [Autenticação baseada em formulários](forms-based-authentication.md): descreve a sequência de chamada típica do OSC para dar suporte a um usuário do Office que está conectado a uma rede social, se o provedor do OSC oferece suporte a autenticação baseada em formulários.
    
- [Obtendo atividades](getting-activities.md): descreve a sequência de chamada típica do OSC sincronize as atividades de amigos do usuário do Office a partir de uma rede social, se o provedor do OSC de redes sociais oferece suporte à sincronização de atividades.
    
- [Obtendo informações de amigos](getting-friends-information.md): descreve a sequência de chamada típica do OSC sincronize a lista de amigos do usuário do Office a partir de uma rede social, se o provedor OSC de redes sociais oferece suporte a cache de sincronização de contatos.
    
## <a name="reference"></a>Referência

- [Referência do provedor do Outlook Social Connector](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a>Se��es relacionadas

- [Introdução ao desenvolvimento de um Outlook Social Connector Provider](getting-started-with-developing-an-outlook-social-connector-provider.md)
  
- [Modelos de amostra do OSC](osc-sample-templates.md)
  
- [Desenvolvendo um provedor com o esquema OSC XML](developing-a-provider-with-the-osc-xml-schema.md)
  
- [Depurando um provedor](debugging-a-provider.md)
  
- [Implantando um provedor](deploying-a-provider.md)
  
- [Práticas recomendadas para o desenvolvimento de um provedor](best-practices-for-developing-a-provider.md)
  
## <a name="see-also"></a>Confira também

- [XML para recursos](xml-for-capabilities.md)

