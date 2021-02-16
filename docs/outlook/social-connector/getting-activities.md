---
title: Obter atividades
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8cb8f916-f061-4c4c-ad1b-40d44af3345a
description: O OSC chama o método ISocialProvider::GetCapabilities para determinar os recursos do provedor OSC para uma rede social.
ms.openlocfilehash: 9d504fb64368a6910feaa38f0ef19ed631b4d4e3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420574"
---
# <a name="getting-activities"></a>Obter atividades

O OSC chama o [método ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) para determinar os recursos do provedor OSC para uma rede social. Se os elementos **getActivities** e **dynamicActivitiesLookupEx** no **XML** de recursos retornados indicarem que o provedor OSC oferece suporte para obter atividades sob demanda e armazenar atividades na memória, o OSC poderá fazer a seguinte sequência de chamada. O OSC também observa a função hash especificada no elemento **hashFunction** no XML **de recursos.** O OSC chama métodos na seguinte sequência para obter atividades e informações (conforme suportado pela interface [ISocialPerson)](isocialpersoniunknown.md) para amigos e não amigos na rede social: 
  
1. [ISocialSession::GetLoggedOnUser](isocialsession-getloggedonuser.md) — No final do processo de autenticação, o OSC chama **GetLoggedOnUser** para obter uma interface [ISocialProfile](isocialprofileisocialperson.md) para o usuário que está sendo autenticado. Para obter mais informações sobre autenticação, [consulte Autenticação básica](basic-authentication.md) e [autenticação baseada em formulários.](forms-based-authentication.md)
    
2. [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) — Para as pessoas exibidas no Painel de Pessoas do Outlook, o OSC obtém e hashes seus endereços SMTP, chama **ISocialSession2::GetActivitiesEx** e armazena (na memória) os dados de atividades retornados para essas pessoas. O OSC obtém em um parâmetro de saída,  _atividades_, que é uma cadeia de caracteres que contém uma coleção de atividades para amigos do usuário conectado. Essa cadeia de caracteres está em conformidade com a definição de esquema para **o elemento activityFeed.** 
    
3. [ISocialSession::GetPerson](isocialsession-getperson.md) — Para cada elemento **activityDetails** no XML **activityFeed** retornado por **GetActivitiesEx**, há um elemento **ownerID** que indica a pessoa que possui essa atividade. O OSC usa esse **valor ownerID** para chamar **GetPerson** para obter uma interface **ISocialPerson** para essa pessoa. 
    
4. [ISocialPerson::GetDetails](isocialperson-getdetails.md) — Com base no objeto **ISocialPerson** obtido da etapa 3, o OSC chama **GetDetails** para obter detalhes dessa pessoa, como o nome e o sobrenome. O OSC pode fazer o mesmo para cada atividade especificada em um elemento **activityDetails** no XML **activityFeed** retornado por **GetActivitiesEx** na etapa 2. 
    
> [!NOTE]
> O OSC atualiza o cache de atividades em um intervalo padrão. Para obter mais informações sobre como atualizar o cache de atividades, consulte [Sincronizando amigos e atividades.](synchronizing-friends-and-activities.md) 
  
## <a name="see-also"></a>Confira também

- [XML para recursos](xml-for-capabilities.md)
- [Sequências de chamada típicas do OSC](osc-typical-calling-sequences.md)

