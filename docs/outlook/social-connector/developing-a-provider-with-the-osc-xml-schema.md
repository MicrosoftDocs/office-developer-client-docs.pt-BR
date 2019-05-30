---
title: Desenvolver um provedor com o esquema XML OSC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0872b1b9-c21f-4bba-8cf1-4b010d8d7fb6
description: O esquema de provedor XML do Outlook Social Connector (OSC)define o formato de uma quantidade significativa de informações que passam de uma rede social através de um provedor do OSC da rede para o OSC.
ms.openlocfilehash: 2346e23beb2de1664ec90263a8f5db5d46c54e6f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539252"
---
# <a name="developing-a-provider-with-the-osc-xml-schema"></a>Desenvolver um provedor com o esquema XML OSC

O esquema de provedor XML do Outlook Social Connector (OSC)define o formato de uma quantidade significativa de informações que passam de uma rede social através de um provedor do OSC da rede para o OSC. O esquema XML permite que um provedor de OSC especifique as funcionalidades do provedor, amigos e itens do feed de atividades na rede social, usando os três principais elementos**funcionalidades**, **amigos**e **feed de o atividades**e seus elementos filhos. O provedor OSC implementa interfaces e seus métodos na extensibilidade OSC do provedor, retornando cadeias de caracteres XML como parâmetros de saída que estão em conformidade com o esquema OSC do provedor XML. O OSC chama esses métodos para obter informações que podem entender como definidas pela esquema XML.
  
> [!NOTE]
> A extensibilidade do provedor OSC dá suporte a provedores de depuração, configurando o`DebugProviders` valor da`HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector` chave de registro como 1. Quando você ativa o provedor de depuração de bugs, a OSC valida o provedor de XML em relação a versão do esquema XML OSC que você especifica no atributo XML **xmlns**. Para OSC 1.1 e versões do OSC desde o Outlook Social Connector 2013, especificar o atributo **xmlns**da seguinte maneira: `xmlns="http://schemas.microsoft.com/office/outlook/2010/06/socialprovider.xsd"`
  
## <a name="in-this-section"></a>Nesta seção

- [Sincronização de amigos e atividades](synchronizing-friends-and-activities.md): descreve as várias formas que provedores OSC podem sincronizar amigos, não-amigos e atividades em uma rede social. 
    
- [Exemplos de XML provedor OSC](osc-provider-xml-examples.md): inclui exemplos de que mostram como especificar os recursos de um provedor de OSC, amigos e itens do feed de atividades em uma rede social, usando o esquema XML do OSC.
    
- [XML para recursos](xml-for-capabilities.md): explica o método – [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) que o OSC usa para obter informações sobre os recursos, expresso nos **recursos** XML do provedor OSC. Esta seção descreve também os elementos XML no esquema XML do provedor OSC que permite que um provedor OSC especifique sua funcionalidade, incluindo a maneira que autentica usuários e sincroniza atividades e os amigos. 
    
- [XML para amigos](xml-for-friends.md): fornece exemplos de APIs que usam o OSC para obter informações de amigos, expressas no XML**amigos**do provedor OSC. Esta seção também descreve os elementos no XML**amigos**. 
    
- [XML de atividades](xml-for-activities.md): fornece exemplos de APIs que usam o OSC para obter informações sobre atividades, expressas no XML**feed de atividades** do provedor OSC. Esta seção descreve também os elementos XML no esquema XML do provedor OSC que permitem que um provedor OSC especifique um feed de atividades. Um feed de atividades inclui a rede na qual o item do feed de atividades teve origem, detalhes de cada item do feed de atividades (como proprietário, tipo e publicar a data da atividade) e o modelo para exibir a atividade. 
    
## <a name="reference"></a>Referências

- [Referência do provedor do Outlook Social Connector](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a>Seções relacionadas

- [Introdução ao desenvolvimento de um provedor de serviços do Outlook Social Connector](getting-started-with-developing-an-outlook-social-connector-provider.md)
  
- [Modelos de exemplo do OSC](osc-sample-templates.md)
  
- [Sequências de chamadas típicas de OSC](osc-typical-calling-sequences.md)
  
- [Depurar um provedor](debugging-a-provider.md)
  
- [Implantar um provedor](deploying-a-provider.md)
  
- [Práticas recomendadas para o desenvolvimento de um provedor](best-practices-for-developing-a-provider.md)
  
## <a name="see-also"></a>Confira também

- [Depurar um provedor](debugging-a-provider.md)

