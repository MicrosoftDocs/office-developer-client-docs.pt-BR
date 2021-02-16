---
title: Diretrizes para exibir atividades corretamente
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 55268188-8432-4145-9527-f5888949fc24
description: Os provedores do Outlook Social Connector (OSC) podem definir os elementos getActivities e dynamicActivitiesLookupEx para que os itens de atividade do armazenamento OSC na memória.
ms.openlocfilehash: b2fcaa125ac8bf7924726f4f09ff507769c3a3f7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422912"
---
# <a name="guidelines-for-properly-displaying-activities"></a>Diretrizes para exibir atividades corretamente

Os provedores do Outlook Social Connector (OSC) podem definir os elementos **getActivities** e **dynamicActivitiesLookupEx** para que os itens de atividade do armazenamento OSC na memória. Este tópico descreve as APIs de extensibilidade do provedor OSC que o OSC chama para obter ou atualizar atividades e detalhes do proprietário da atividade, se o provedor OSC suportar a sincronização de feeds de atividade da rede social. O tópico também lista alguns elementos filho do elemento **activityFeed** que o provedor OSC deve definir para o OSC exibir as atividades corretamente no Cartão de Visita do Office ou no Painel de Pessoas do Outlook. 
  
- O OSC chama o método [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) para obter e armazenar atividades na pasta News Feed para o usuário conectado. O provedor OSC deve implementar **GetActivitiesEx** para retornar uma cadeia de caracteres _XML_ de atividades que está em conformidade com a definição de esquema XML do provedor OSC do **elemento activityFeed.** 
    
- O provedor OSC deve definir **o elemento ownerID,** que é um elemento filho do **elemento activityDetails.** **ownerID** é uma cadeia de caracteres opaca que identifica o proprietário da atividade na rede social. 
    
- O provedor OSC deve definir os **elementos nameHint** e **emailAddress** no nó **publisherVariable** do **elemento templateVariables.** 
    
   Observe que, de acordo com o esquema XML do provedor OSC, o **elemento nameHint** é um elemento opcional. O OSC o usa para corresponder ao nome de exibição do usuário selecionado no Cartão de Visita ou no Painel de Pessoas. Da mesma forma, **o elemento emailAddress** é um elemento opcional no esquema XML. O OSC o usa para corresponder ao endereço SMTP do usuário selecionado no Cartão de Visita ou no Painel de Pessoas. 
    
   Se apenas o elemento **ownerID** for especificado, mas um ou ambos de **nameHint** e **emailAddress** não são especificados, o OSC chama o método [ISocialSession2::GetPeopleDetails](isocialsession2-getpeopledetails.md) e, em seguida, o método [ISocialPerson::GetDetails](isocialperson-getdetails.md) para obter mais informações sobre a pessoa identificada pelo **ownerID**. Quando o OSC chama **ISocialPerson::GetDetails**, o provedor deve retornar **o** XML da pessoa que especifica os **elementos fullName** e **emailAddress.** 
    
## <a name="see-also"></a>Confira também

- [XML para atividades](xml-for-activities.md)  
- [XML para amigos](xml-for-friends.md)  
- [XML para recursos](xml-for-capabilities.md)

