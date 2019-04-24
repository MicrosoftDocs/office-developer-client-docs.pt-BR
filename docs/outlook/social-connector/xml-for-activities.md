---
title: XML para atividades
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: acc4a555-a3bf-4a79-86dc-aba6477733b8
description: Este tópico contém um cenário de exemplo que mostra as chamadas da API de extensibilidade do provedor do Outlook Social Connector (OSC) que um provedor do OSC implementa e o OSC faz para obter informações sobre atividades. As informações são expressas em cadeias de caracteres XML que estão em conformidade com o esquema XML do provedor OSC.
ms.openlocfilehash: a4f1c6ce1f33b59811f6a6fecb737cd1f737946b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329117"
---
# <a name="xml-for-activities"></a>XML para atividades

Este tópico contém um cenário de exemplo que mostra as chamadas da API de extensibilidade do provedor do Outlook Social Connector (OSC) que um provedor do OSC implementa e o OSC faz para obter informações sobre atividades. As informações são expressas em cadeias de caracteres XML que estão em conformidade com o esquema XML do provedor OSC.
  
O esquema XML do provedor OSC permite que um provedor do OSC defina atividades. As informações de atividade podem incluir a rede social onde os itens de feeds de atividades originaram, detalhes de cada item de feed de atividade (como proprietário, tipo e data de publicação da atividade) e o modelo para exibir a atividade. Para dar suporte à exibição de atividades no painel de pessoas ou no cartão de visita, o provedor OSC de uma rede social deve implementar e retornar o XML de atividades correto. Para obter um exemplo de XML de feed de atividades, consulte [exemplo de XML de feed de atividades](activity-feed-xml-example.md). Para obter mais informações sobre a sincronização das atividades dos amigos, consulte [sincronizaNdo amigos e atividades](synchronizing-friends-and-activities.md). Para obter uma definição completa do esquema XML do provedor OSC, incluindo quais elementos são obrigatórios ou opcionais, consulte [esquema XML do provedor do Outlook Social Connector](outlook-social-connector-provider-xml-schema.md). 
  
No cenário a seguir, o OSC sincroniza dinamicamente as atividades de uma pessoa selecionada no painel de pessoas e obtém detalhes sobre essa pessoa:
  
1. Um provedor OSC que oferece suporte à sincronização sob demanda de atividades indica que o OSC está usando os **** elementos getactivities e **dynamicActivitiesLookupEx** . O provedor OSC também define o elemento **hashFunction** . Todos os três elementos são elementos filhos dos **recursos**. 
    
2. O provedor OSC implementa os métodos **ISocialProvider:: GetCapabilities** e [ISocialSession2:: GetActivitiesEx](isocialsession2-getactivitiesex.md) . 
    
3. O OSC chama **ISocialProvider:: GetCapabilities** para verificar o valor de **getactivities** e **dynamicActivitiesLookupEx** para verificar se o provedor do OSC oferece suporte à sincronização sob demanda de atividades. O OSC também observa o valor do elemento **hashFunction** suportado pelo provedor OSC. 
    
4. O OSC atualiza o painel de pessoas ou o cartão de contato para permitir que o usuário veja as atividades mais recentes da pessoa selecionada. O OSC criptografa o endereço SMTP da pessoa usando a função de hash especificada no elemento **hashFunction** , formando uma cadeia de caracteres XML que está de acordo com a definição de esquema XML do elemento **hashedAddresses** . 
    
5. O OSC chama **ISocialSession2:: GetActivitiesEx**, fornecendo esta cadeia de caracteres XML do endereço hash como o parâmetro _hashedAddresses_ , para obter uma coleção atual de atividades para essa pessoa no parâmetro _Activities_ . A cadeia de caracteres de parâmetro de _atividades_ está em conformidade com a definição de esquema XML do elemento **ofeed** . 
    
6. Com base na definição de esquema XML para o **ofeed**, o OSC analisa ainda mais a cadeia de caracteres de _atividades_ para descobrir o tipo, a data de publicação e outras informações sobre cada atividade e como exibir a atividade. 
    
7. Para obter detalhes sobre a pessoa selecionada, o OSC chama [ISocialSession2:: GetPeopleDetails](isocialsession2-getpeopledetails.md), fornecendo a mesma cadeia de caracteres XML de endereços de hash como o argumento para o parâmetro _personsAddresses_ . Os detalhes sobre a pessoa são retornados no parâmetro _Persons_ . Esses detalhes podem incluir **FirstName**, **LastName**e **EmailAddress**. O __ parâmetro performations se refere à definição de esquema XML para o elemento **Person** . 
    
Você pode encontrar mais informações sobre como especificar XML para atividades nos seguintes tópicos desta seção:
  
- [Visão geral do XML para um item do feed de atividades](overview-of-xml-for-an-activity-feed-item.md)
    
- [Elemento activityDetails](activitydetails-element.md)
    
- [Elemento activityTemplateContainer](activitytemplatecontainer-element.md)
    
- [Variáveis do modelo](template-variables.md)
    
- [Diretrizes para exibir atividades de modo adequado](guidelines-for-properly-displaying-activities.md)
    
## <a name="see-also"></a>Confira também

- [Exemplo de XML de feed de atividades](activity-feed-xml-example.md)  
- [Sincronizar amigos e atividades](synchronizing-friends-and-activities.md) 
- [XML para recursos](xml-for-capabilities.md)  
- [XML para amigos](xml-for-friends.md)
- [Desenvolvimento de um provedor com o esquema XML do OSC](developing-a-provider-with-the-osc-xml-schema.md)

