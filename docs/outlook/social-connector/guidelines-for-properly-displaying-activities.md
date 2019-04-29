---
title: Diretrizes para exibir atividades corretamente
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 55268188-8432-4145-9527-f5888949fc24
description: Os provedores do Outlook Social Connector (OSC) podem definir os elementos getActivities e dynamicActivitiesLookupEx para que os itens de atividade do repositório OSC estejam na memória.
ms.openlocfilehash: b2fcaa125ac8bf7924726f4f09ff507769c3a3f7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422912"
---
# <a name="guidelines-for-properly-displaying-activities"></a>Diretrizes para exibir atividades corretamente

Os provedores do Outlook Social Connector (OSC) podem **** definir os elementos getactivities e **dynamicActivitiesLookupEx** para que os itens de atividade do repositório OSC estejam na memória. Este tópico descreve as APIs de extensibilidade do provedor OSC que o OSC chama para obter ou atualizar atividades e detalhes do proprietário da atividade, se o provedor OSC oferecer suporte à sincronização de feeds de atividade da rede social. O tópico também lista alguns elementos filhos do elemento **ofeed** que o provedor do OSC deve definir para que o OSC exiba atividades adequadamente no cartão de visita do Office ou no painel de pessoas do Outlook. 
  
- O OSC chama o método [ISocialSession2:: GetActivitiesEx](isocialsession2-getactivitiesex.md) para obter e armazenar atividades na pasta de feed de notícias para o usuário conectado. O provedor do OSC deve implementar **GetActivitiesEx** para retornar uma cadeia de caracteres XML de _atividades_ que esteja em conformidade com a definição de esquema XML do provedor OSC do elemento **ofeed** . 
    
- O provedor OSC deve definir o **** elemento OwnerId, que é um elemento filho do elemento **activityDetails** . **OwnerId** é uma cadeia de caracteres opaca que identifica o proprietário da atividade na rede social. 
    
- O provedor OSC deve definir os elementos **nameHint** e **EmailAddress** no nó **publisherVariable** do elemento **templateVariables** . 
    
   Observe que, por meio do esquema XML do provedor OSC, o elemento **nameHint** é um elemento opcional. O OSC o utiliza para corresponder ao nome de exibição do usuário selecionado no cartão de visita ou no painel de pessoas. Da mesma forma, o elemento **EmailAddress** é um elemento opcional no esquema XML. O OSC o usa para corresponder o endereço SMTP do usuário selecionado no cartão de visita ou no painel de pessoas. 
    
   Se apenas o **** elemento OwnerId for especificado, mas um ou ambos **nameHint** e **EmailAddress** não forem especificados, o OSC chamará o método [ISocialSession2:: GetPeopleDetails](isocialsession2-getpeopledetails.md) e, em seguida, o [ISocialPerson:: GetDetails](isocialperson-getdetails.md) método para obter mais informações sobre a pessoa identificada pelo **OwnerId**. Quando o OSC chama **ISocialPerson:: GetDetails**, o provedor deve retornar **Person** XML que especifica os elementos **FullName** e **EmailAddress** . 
    
## <a name="see-also"></a>Confira também

- [XML para atividades](xml-for-activities.md)  
- [XML para amigos](xml-for-friends.md)  
- [XML para recursos](xml-for-capabilities.md)

