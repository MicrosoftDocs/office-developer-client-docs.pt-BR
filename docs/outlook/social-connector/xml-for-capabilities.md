---
title: XML para recursos
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: edad1223-a55f-4e4a-8e90-3471f2f559ac
description: 'O elemento capabilities no esquema XML do provedor (OSC) permite que um provedor OSC especifique sua funcionalidade. Essa funcionalidade inclui o seguinte:'
ms.openlocfilehash: ff6abbd4d99eb542a11e3d64a2015fc0585fca79
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435002"
---
# <a name="xml-for-capabilities"></a>XML para recursos

O **elemento** capabilities no esquema XML do provedor (OSC) permite que um provedor OSC especifique sua funcionalidade. Essa funcionalidade inclui o seguinte: 
  
- Se o provedor oferece suporte para obter, armazenando em cache ou procurando dinamicamente amigos e atividades da rede social.
    
- Como o OSC deve exibir determinadas interfaces de usuário de logon.
    
- Se o OSC deve usar a autenticação baseada em formulários ou configurar automaticamente a rede social e fazer logon no usuário na rede social.
    
O esquema XML para **recursos** é fundamental porque identifica para o OSC a funcionalidade suportada pelo provedor. Um provedor OSC deve implementar o [método ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) que retorna uma cadeia  _de caracteres de_ resultado. O OSC chama **ISocialProvider::GetCapabilities** para obter informações sobre os  recursos do provedor OSC na cadeia de caracteres de resultado, que está em conformidade com a definição de esquema XML para o elemento **capabilities.** Essas informações permitem que chamadas subsequentes do OSC para o provedor OSC funcionem corretamente. 
  
Para especificar recursos de um provedor OSC como um parâmetro de saída do método **ISocialProvider::GetCapabilities,** você deve estar em conformidade com o esquema XML de extensibilidade do provedor OSC. A figura a seguir mostra a **estrutura** XML de recursos. 
  
**Figura 1. \<capabilities \> Estrutura XML**

![capabilities XML structure](media/ol14oscref_Specifyingxmlforcapabilities_image1.gif)
  
Para descrições detalhadas dos elementos filho do elemento **capabilities,** consulte [Elementos XML de recursos.](capabilities-xml-elements.md) Para obter um exemplo do XML de **recursos**, consulte [Exemplo do XML de recursos](capabilities-xml-example.md). Para obter uma definição completa do esquema XML do provedor OSC, inclusive de quais elementos são obrigatórios ou opcionais, confira o [Esquema XML do Provedor do Outlook Social Connector](outlook-social-connector-provider-xml-schema.md).
  
## <a name="see-also"></a>Confira também

- [Exemplo do XML de recursos](capabilities-xml-example.md)  
- [Sincronizar amigos e atividades](synchronizing-friends-and-activities.md)  
- [XML para amigos](xml-for-friends.md)  
- [XML para atividades](xml-for-activities.md)
- [Como desenvolver um provedor com o esquema XML do OSC](developing-a-provider-with-the-osc-xml-schema.md)

