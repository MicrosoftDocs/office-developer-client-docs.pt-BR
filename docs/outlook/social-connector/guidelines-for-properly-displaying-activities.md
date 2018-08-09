---
title: Diretrizes para exibir atividades corretamente
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 55268188-8432-4145-9527-f5888949fc24
description: Provedores do Outlook Social Connector (OSC) podem definir os elementos getActivities e dynamicActivitiesLookupEx para que o OSC armazenar itens de atividade na memória.
ms.openlocfilehash: f8cb5850c8920f09f784343db18372bb75ca17a4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770823"
---
# <a name="guidelines-for-properly-displaying-activities"></a>Diretrizes para exibir atividades corretamente

Provedores do Outlook Social Connector (OSC) podem definir o **getActivities** e elementos de **dynamicActivitiesLookupEx** ter o OSC armazenam itens de atividade na memória. Este tópico descreve a extensibilidade do provedor OSC feeds de APIs que o OSC chama para obter ou atualizar as atividades e detalhes de proprietário de atividade, se o provedor do OSC oferece suporte à sincronização de atividades da rede social. O tópico também lista alguns elementos filho do elemento de **feed de atividades** que o provedor do OSC deve ser definida para que o OSC exibir atividades adequadamente no cartão de visita do Office ou no painel de pessoas do Outlook. 
  
- O OSC chama o método [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) para obter e armazenar atividades na pasta News Feed para o usuário conectado. O provedor do OSC deve implementar **GetActivitiesEx** para retornar uma cadeia de caracteres XML de _atividades_ que seja compatível com o provedor do OSC definição de esquema XML do elemento de **feed de atividades** . 
    
- O provedor do OSC deve definir o elemento **ownerID** , que é um elemento filho do elemento **activityDetails** . **ownerID** é uma sequência de caracteres opaca que identifica o proprietário da atividade na rede social. 
    
- O provedor do OSC deve definir os elementos **nameHint** e **emailAddress** no nó do elemento **templateVariables** **publisherVariable** . 
    
   Observe que, por que o esquema XML de provedor OSC, o elemento **nameHint** é um elemento opcional. O OSC utiliza para corresponder ao nome de exibição do usuário selecionado no painel pessoas ou cartão de visita. Da mesma forma, o elemento **emailAddress** é um elemento opcional do esquema XML. O OSC utiliza para corresponder ao endereço SMTP do usuário selecionado no painel pessoas ou cartão de visita. 
    
   Se apenas o elemento **ownerID** for especificado, mas um ou ambos **nameHint** e **emailAddress** não forem especificados, o OSC chama o método [ISocialSession2::GetPeopleDetails](isocialsession2-getpeopledetails.md) e, em seguida, o [ISocialPerson::GetDetails](isocialperson-getdetails.md) método para obter mais informações sobre a pessoa identificada pelo **ownerID**. Quando o OSC chama **ISocialPerson::GetDetails**, o provedor deve retornar **pessoa** XML que especifica os elementos **fullName** e **emailAddress** . 
    
## <a name="see-also"></a>Confira também

- [XML para atividades](xml-for-activities.md)  
- [XML para amigos](xml-for-friends.md)  
- [XML para recursos](xml-for-capabilities.md)

