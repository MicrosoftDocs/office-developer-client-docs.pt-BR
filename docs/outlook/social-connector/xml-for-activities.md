---
title: XML para atividades
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: acc4a555-a3bf-4a79-86dc-aba6477733b8
description: Este tópico contém um cenário de exemplo que mostra o provedor do Outlook Social Connector (OSC) chamadas de API de extensibilidade que implementa um provedor OSC e faz com que o OSC para obter informações de atividades. Informações é expresso em cadeias de caracteres XML que estão em conformidade com o esquema XML de provedor do OSC.
ms.openlocfilehash: 44f74d9e72eec3ff6da7f9967315fc9d75191584
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770967"
---
# <a name="xml-for-activities"></a>XML para atividades

Este tópico contém um cenário de exemplo que mostra o provedor do Outlook Social Connector (OSC) chamadas de API de extensibilidade que implementa um provedor OSC e faz com que o OSC para obter informações de atividades. Informações é expresso em cadeias de caracteres XML que estão em conformidade com o esquema XML de provedor do OSC.
  
O esquema XML de provedor do OSC permite que um provedor OSC definir atividades. Informações de atividade podem incluir a rede social onde a atividade feed itens se originou, detalhes de cada item de feed de atividade (como proprietário, digite e data da atividade de publicação) e o modelo para exibir a atividade. Para oferecer suporte a atividades de mostrando no painel pessoas ou cartão de visita, provedor do OSC da rede social deve implementar e retornar as atividades corretas XML. Para obter um exemplo de atividade feed XML, consulte [Exemplo de XML de Feed de atividade](activity-feed-xml-example.md). Para obter mais informações sobre a sincronização de atividades dos amigos, consulte [Sincronizando amigos e atividades](synchronizing-friends-and-activities.md). Para uma definição completa do esquema de XML de provedor OSC, incluindo quais elementos são obrigatórias ou opcionais, consulte [Esquema de XML para Outlook Social Connector Provider](outlook-social-connector-provider-xml-schema.md). 
  
No cenário a seguir, o OSC dinamicamente sincroniza atividades de uma pessoa selecionada no painel de pessoas e obtém detalhes sobre essa pessoa:
  
1. Um provedor OSC que ofereça suporte a sincronização sob demanda das atividades indica que o OSC usando os elementos **getActivities** e **dynamicActivitiesLookupEx** . O provedor do OSC também define o elemento **hashFunction** . Todos os três elementos são elementos filho de **recursos**. 
    
2. O provedor do OSC implementa os métodos **ISocialProvider::GetCapabilities** e [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) . 
    
3. As chamadas OSC **ISocialProvider::GetCapabilities** para verificar o valor de **getActivities** e **dynamicActivitiesLookupEx** para verificar se o provedor OSC suporta a sincronização sob demanda de atividades. O OSC também notas o valor do elemento **hashFunction** suportado pelo provedor do OSC. 
    
4. O OSC atualiza o painel de pessoas ou o cartão de visita para permitir que o usuário veja as atividades mais recentes da pessoa selecionada. O OSC criptografa o endereço da pessoa SMTP usando a função de hash especificada no elemento **hashFunction** , formando uma cadeia de caracteres XML que está em conformidade com a definição de esquema XML para o elemento **hashedAddresses** . 
    
5. O OSC chama **ISocialSession2::GetActivitiesEx**, fornecendo essa cadeia de caracteres XML do endereço de hash como o parâmetro _hashedAddresses_ , para obter uma coleção atual das atividades dessa pessoa no parâmetro _atividades_ . A cadeia de caracteres do parâmetro de _atividades_ é compatível com a definição de esquema XML do elemento de **feed de atividades** . 
    
6. Com base na definição de esquema XML para o **feed de atividades**, ainda mais o OSC analisa a cadeia de caracteres de _atividades_ para descobrir o tipo, publicar data e outras informações sobre cada atividade e como exibir a atividade. 
    
7. Para obter detalhes sobre a pessoa selecionada, o OSC chama [ISocialSession2::GetPeopleDetails](isocialsession2-getpeopledetails.md), fornecendo a mesma cadeia XML de hash endereços como o argumento para o parâmetro _personsAddresses_ . Os detalhes sobre a pessoa são retornados no parâmetro _personsCollection_ . Esses detalhes podem incluir **firstName**, **lastName**e **emailAddress**. O parâmetro _personsCollection_ está de acordo com a definição de esquema XML para o elemento de **pessoa** . 
    
Você pode encontrar mais informações sobre a especificação XML para atividades nos seguintes tópicos desta seção:
  
- [Visão geral de XML para uma atividade Feed Item](overview-of-xml-for-an-activity-feed-item.md)
    
- [activityDetails elemento](activitydetails-element.md)
    
- [activityTemplateContainer elemento](activitytemplatecontainer-element.md)
    
- [Variáveis do modelo](template-variables.md)
    
- [Diretrizes para exibir adequadamente atividades](guidelines-for-properly-displaying-activities.md)
    
## <a name="see-also"></a>Confira também

- [Exemplo de XML de Feed de atividade](activity-feed-xml-example.md)  
- [Sincronização de amigos e atividades](synchronizing-friends-and-activities.md) 
- [XML para recursos](xml-for-capabilities.md)  
- [XML para amigos](xml-for-friends.md)
- [Desenvolvendo um provedor com o esquema OSC XML](developing-a-provider-with-the-osc-xml-schema.md)

