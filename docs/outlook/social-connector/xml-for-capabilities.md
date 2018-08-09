---
title: XML para recursos
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: edad1223-a55f-4e4a-8e90-3471f2f559ac
description: 'O elemento de recursos no esquema XML provedor (OSC) permite que um provedor OSC especificar sua funcionalidade. Essa funcionalidade inclui o seguinte:'
ms.openlocfilehash: 8192c4d559ae656cfc3b12cd8f50f7d4acd5ed5f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770953"
---
# <a name="xml-for-capabilities"></a>XML para recursos

O elemento de **recursos** no esquema XML provedor (OSC) permite que um provedor OSC especificar sua funcionalidade. Essa funcionalidade inclui o seguinte: 
  
- Se o provedor oferece suporte à obtenção, cache ou procurando dinamicamente amigos e atividades da rede social.
    
- Como o OSC deve exibir certas interfaces de usuário de logon.
    
- Se o OSC deve usar a autenticação baseada em formulários ou configurar automaticamente os logs e redes sociais do usuário na rede social.
    
O esquema XML de **recursos** é fundamental, pois ele identifica para o OSC a funcionalidade suportada pelo provedor. Um provedor OSC deve implementar o método [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) que retorna uma cadeia de caracteres de _resultado_ . O OSC chama **ISocialProvider::GetCapabilities** para obter informações sobre os recursos do provedor do OSC na sequência de _resultado_ , o que está em conformidade com a definição de esquema XML para o elemento de **recursos** . Essas informações permitem que chamadas subsequentes provenientes do OSC para o provedor do OSC para que funcionem corretamente. 
  
Para especificar os recursos de um provedor OSC como um parâmetro de saída do método **ISocialProvider::GetCapabilities** , você deve estar em conformidade com o esquema XML de extensibilidade de provedor OSC. A figura a seguir mostra a estrutura do XML de **recursos** . 
  
**Figura 1. \<recursos\> estrutura XML**

![capabilities XML structure](media/ol14oscref_Specifyingxmlforcapabilities_image1.gif)
  
Para obter descrições detalhadas dos elementos filho do elemento de **recursos** , consulte [Elementos XML de recursos](capabilities-xml-elements.md). Para obter um exemplo dos **recursos** de XML, consulte [Exemplo de XML de recursos](capabilities-xml-example.md). Para uma definição completa do esquema de XML de provedor OSC, incluindo quais elementos são obrigatórias ou opcionais, consulte [Esquema de XML para Outlook Social Connector Provider](outlook-social-connector-provider-xml-schema.md).
  
## <a name="see-also"></a>Confira também

- [Exemplo de XML de recursos](capabilities-xml-example.md)  
- [Sincronização de amigos e atividades](synchronizing-friends-and-activities.md)  
- [XML para amigos](xml-for-friends.md)  
- [XML para atividades](xml-for-activities.md)
- [Desenvolvendo um provedor com o esquema OSC XML](developing-a-provider-with-the-osc-xml-schema.md)

