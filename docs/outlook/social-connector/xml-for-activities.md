---
title: XML para atividades
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: acc4a555-a3bf-4a79-86dc-aba6477733b8
description: Este tópico contém um cenário de exemplo que mostra as chamadas de API de extensibilidade do provedor outlook Social Connector (OSC) que um provedor osC implementa e o OSC faz para obter informações de atividades. As informações são expressas em cadeias de caracteres XML que estão em conformidade com o esquema XML do provedor OSC.
ms.openlocfilehash: a4f1c6ce1f33b59811f6a6fecb737cd1f737946b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409626"
---
# <a name="xml-for-activities"></a>XML para atividades

Este tópico contém um cenário de exemplo que mostra as chamadas de API de extensibilidade do provedor outlook Social Connector (OSC) que um provedor osC implementa e o OSC faz para obter informações de atividades. As informações são expressas em cadeias de caracteres XML que estão em conformidade com o esquema XML do provedor OSC.
  
O esquema XML do provedor OSC permite que um provedor OSC defina atividades. As informações de atividade podem incluir a rede social na qual os itens do feed de atividades se originaram, detalhes de cada item do feed de atividades (como proprietário, tipo e data de publicação da atividade) e o modelo para exibir a atividade. Para dar suporte à exibição de atividades no Painel de Pessoas ou no Cartão de Visita, o provedor OSC de uma rede social deve implementar e retornar o XML de atividades corretas. Para um exemplo de XML do feed de atividades, consulte [Exemplo XML do feed de atividades.](activity-feed-xml-example.md) Para obter mais informações sobre como sincronizar atividades de amigos, consulte [Sincronizando amigos e atividades.](synchronizing-friends-and-activities.md) Para obter uma definição completa do esquema XML do provedor OSC, inclusive de quais elementos são obrigatórios ou opcionais, confira o [Esquema XML do Provedor do Outlook Social Connector](outlook-social-connector-provider-xml-schema.md). 
  
No cenário a seguir, o OSC sincroniza dinamicamente as atividades de uma pessoa selecionada no Painel de Pessoas e obtém detalhes sobre essa pessoa:
  
1. Um provedor OSC que oferece suporte à sincronização sob demanda de atividades indica que para o OSC usando os elementos **getActivities** e **dynamicActivitiesLookupEx.** O provedor OSC também define o elemento **hashFunction**. Todos os três elementos são elementos filhos de **capabilities**. 
    
2. O provedor OSC implementa os métodos **ISocialProvider::GetCapabilities** e [ISocialSession2::GetActivitiesEx.](isocialsession2-getactivitiesex.md) 
    
3. O OSC chama **ISocialProvider::GetCapabilities** para verificar o valor de **getActivities** e **dynamicActivitiesLookupEx** para verificar se o provedor OSC oferece suporte à sincronização sob demanda de atividades. O OSC também observa o valor do **elemento hashFunction** suportado pelo provedor OSC. 
    
4. O OSC atualiza o Painel de Pessoas ou o Cartão de Visita para permitir que o usuário veja as atividades mais recentes da pessoa selecionada. O OSC criptografa o endereço SMTP da pessoa usando a função hash especificada no elemento **hashFunction,** formando uma cadeia de caracteres XML em conformidade com a definição de esquema XML para o elemento **hashedAddresses.** 
    
5. O OSC chama **ISocialSession2::GetActivitiesEx**, fornecendo essa cadeia de caracteres XML do endereço com hashed Como o  parâmetro _hashedAddresses,_ para obter uma coleção atual de atividades para essa pessoa no parâmetro de atividades. A _cadeia de_ caracteres de parâmetro de atividades está em conformidade com a definição de esquema XML do elemento **activityFeed.** 
    
6. Com base na definição de esquema XML para **activityFeed**, o OSC analisará ainda mais a cadeia de caracteres de atividades para descobrir o tipo, a data de publicação e outras informações sobre cada atividade e como exibir a atividade.  
    
7. Para obter detalhes sobre a pessoa selecionada, o OSC chama [ISocialSession2::GetPeopleDetails](isocialsession2-getpeopledetails.md), fornecendo a mesma cadeia de caracteres XML de endereços com hashed como o argumento para o parâmetro _personsAddresses._ Os detalhes sobre a pessoa são retornados no parâmetro _personsCollection._ Esses detalhes podem incluir **firstName**, **lastName** e **emailAddress**. O _parâmetro personsCollection_ está em conformidade com a definição de esquema XML para o **elemento person.** 
    
Você pode encontrar mais informações sobre como especificar XML para atividades nos seguintes tópicos desta seção:
  
- [Visão geral do XML para um item do feed de atividades](overview-of-xml-for-an-activity-feed-item.md)
    
- [Elemento activityDetails](activitydetails-element.md)
    
- [Elemento activityTemplateContainer](activitytemplatecontainer-element.md)
    
- [Variáveis do modelo](template-variables.md)
    
- [Diretrizes para a exibição adequada das atividades](guidelines-for-properly-displaying-activities.md)
    
## <a name="see-also"></a>Confira também

- [Exemplo de XML de feed de atividades](activity-feed-xml-example.md)  
- [Sincronizar amigos e atividades](synchronizing-friends-and-activities.md) 
- [XML para recursos](xml-for-capabilities.md)  
- [XML para amigos](xml-for-friends.md)
- [Como desenvolver um provedor com o esquema XML do OSC](developing-a-provider-with-the-osc-xml-schema.md)

