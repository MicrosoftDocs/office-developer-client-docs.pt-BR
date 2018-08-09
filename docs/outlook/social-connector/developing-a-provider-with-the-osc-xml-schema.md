---
title: Desenvolver um provedor com o esquema XML OSC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0872b1b9-c21f-4bba-8cf1-4b010d8d7fb6
description: O esquema XML de provedor do Outlook Social Connector (OSC) define o formato de uma quantidade significativa de informações que são passadas de uma rede social por meio do provedor do OSC da rede para o OSC.
ms.openlocfilehash: 93df682751146b501a316be62641b8cfd47a74a8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770838"
---
# <a name="developing-a-provider-with-the-osc-xml-schema"></a>Desenvolver um provedor com o esquema XML OSC

O esquema XML de provedor do Outlook Social Connector (OSC) define o formato de uma quantidade significativa de informações que são passadas de uma rede social por meio do provedor do OSC da rede para o OSC. O esquema XML permite que um provedor OSC especificar recursos do provedor, amigos e itens de feed na rede social, usando os três elementos principais, **recursos**, **feed de atividades**e **amigos**e seus filhos de atividade elementos. O provedor do OSC implementa interfaces e seus métodos na extensibilidade do provedor do OSC, retornando cadeias de caracteres XML como parâmetros de saída que estão em conformidade com o esquema XML de provedor do OSC. O OSC chama esses métodos para obter informações que ele pode entender como definido pelo esquema XML.
  
> [!NOTE]
> Estensibilidade do provedor do OSC oferece suporte a provedores de depuração, definindo o `DebugProviders` valor o `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector` a chave do registro como 1. Quando você ativa a depuração de provedor, o OSC valida o provedor XML contra a versão do esquema OSC XML especificado no atributo **xmlns** XML. Para OSC 1.1 e versões do OSC desde o Outlook Social Connector 2013, especifique o atributo **xmlns** da seguinte maneira:`xmlns="http://schemas.microsoft.com/office/outlook/2010/06/socialprovider.xsd"`
  
## <a name="in-this-section"></a>Nesta seção

- [Sincronizando amigos e atividades](synchronizing-friends-and-activities.md): descreve as várias maneiras em que os provedores OSC podem sincronizar amigos, não-amigos e atividades em uma rede social. 
    
- [Exemplos de XML de provedor do OSC](osc-provider-xml-examples.md): exemplos de XML inclui que mostram como especificar recursos de um provedor OSC, amigos e atividade feed itens em uma rede social usando o esquema OSC XML.
    
- [XML de recursos](xml-for-capabilities.md): explica-método [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) que o OSC usa para obter informações sobre recursos, expressado em **recursos de** XML, do provedor do OSC. Esta seção também descreve os elementos XML no esquema XML de provedor do OSC que permitem que um provedor OSC especificar sua funcionalidade, incluindo como ele autentica usuários e sincroniza amigos e atividades. 
    
- [XML para amigos](xml-for-friends.md): dá exemplos das APIs que o OSC usa para obter informações dos amigos, expressadas em **amigos** XML, do provedor do OSC. Esta seção também descreve os elementos no **amigos** XML. 
    
- [XML para atividades](xml-for-activities.md): dá exemplos das APIs que o OSC usa para obter informações de atividades, expressadas no **feed de atividades** XML, do provedor do OSC. Esta seção também descreve os elementos XML no esquema XML de provedor do OSC que permitem que um provedor OSC especificar um feed de atividade. Um feed de atividade inclui da rede onde a atividade feed itens se originou, detalhes de cada item de feed de atividade (como proprietário, digite e data da atividade de publicação) e o modelo para exibir a atividade. 
    
## <a name="reference"></a>Referência

- [Referência do provedor do Outlook Social Connector](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a>Se��es relacionadas

- [Introdução ao desenvolvimento de um Outlook Social Connector Provider](getting-started-with-developing-an-outlook-social-connector-provider.md)
  
- [Modelos de amostra do OSC](osc-sample-templates.md)
  
- [Sequências de chamadas comuns do OSC](osc-typical-calling-sequences.md)
  
- [Depurando um provedor](debugging-a-provider.md)
  
- [Implantando um provedor](deploying-a-provider.md)
  
- [Práticas recomendadas para o desenvolvimento de um provedor](best-practices-for-developing-a-provider.md)
  
## <a name="see-also"></a>Confira também

- [Depurando um provedor](debugging-a-provider.md)

