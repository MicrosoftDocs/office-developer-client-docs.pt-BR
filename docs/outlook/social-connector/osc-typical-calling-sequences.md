---
title: Sequências de chamadas típicas de OSC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f61960f7-e018-4d2e-8e32-426ed46d9064
description: Esta seção descreve as sequências de chamada típicas do Outlook Social Connector (OSC) de membros nas interfaces de extensibilidade do provedor OSC, que um provedor osC implementa.
ms.openlocfilehash: f7829b710d6840ccd1fa0f990d6e03b2eb879431
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413609"
---
# <a name="osc-typical-calling-sequences"></a>Sequências de chamadas típicas de OSC

Esta seção descreve as sequências de chamada típicas do Outlook Social Connector (OSC) de membros nas interfaces de extensibilidade do provedor OSC, implementadas por um provedor do OSC. As sequências de chamada típicas ilustram como e quando o OSC usa essas interfaces e métodos para permitir que você determine melhor como implementar um determinado membro em uma interface de extensibilidade do provedor. A sequência de chamada real pode variar dependendo dos recursos retornados pelo [método ISocialProvider::GetCapabilities.](isocialprovider-getcapabilities.md) Exemplos de recursos incluem o seguinte: 
  
- Suporte do provedor para obter, armazenamento em cache ou procurar dinamicamente amigos e atividades da rede social.
    
- A interface do usuário que o OSC deve exibir para logon do usuário.
    
- O tipo de autenticação (por exemplo, autenticação baseada em formulários) que o OSC deve usar.
    
## <a name="in-this-section"></a>Nesta seção

- [Autenticação](basic-authentication.md)Básica: descreve a sequência de chamada típica do OSC para dar suporte a um usuário do Office que está fazendo logon em uma rede social, se o provedor OSC suportar a autenticação básica.
    
- [Autenticação baseada](forms-based-authentication.md)em formulários: descreve a sequência de chamada típica do OSC para dar suporte a um usuário do Office que está fazendo logon em uma rede social, se o provedor OSC suportar autenticação baseada em formulários.
    
- [Getting Activities](getting-activities.md): Descreve a sequência de chamada típica do OSC para sincronizar as atividades dos amigos do usuário do Office de uma rede social, se o provedor OSC de rede social suportar a sincronização de atividades.
    
- [Obter informações](getting-friends-information.md)de amigos: descreve a sequência de chamada típica do OSC para sincronizar a lista de amigos do usuário do Office de uma rede social, se o provedor OSC de rede social suportar a sincronização em cache de contatos.
    
## <a name="reference"></a>Referências

- [Referência do provedor do Outlook Social Connector](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a>Seções relacionadas

- [Introdução ao desenvolvimento de um provedor de serviços do Outlook Social Connector](getting-started-with-developing-an-outlook-social-connector-provider.md)
  
- [Modelos de exemplo do OSC](osc-sample-templates.md)
  
- [Desenvolver um provedor com o esquema XML do OSC](developing-a-provider-with-the-osc-xml-schema.md)
  
- [Depurar um provedor](debugging-a-provider.md)
  
- [Implantar um provedor](deploying-a-provider.md)
  
- [Práticas recomendadas para o desenvolvimento de um provedor](best-practices-for-developing-a-provider.md)
  
## <a name="see-also"></a>Confira também

- [XML para recursos](xml-for-capabilities.md)

