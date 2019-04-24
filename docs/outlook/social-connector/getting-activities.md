---
title: Obter atividades
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8cb8f916-f061-4c4c-ad1b-40d44af3345a
description: 'O OSC chama o método ISocialProvider:: GetCapabilities para determinar os recursos do provedor do OSC para uma rede social.'
ms.openlocfilehash: 9d504fb64368a6910feaa38f0ef19ed631b4d4e3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327178"
---
# <a name="getting-activities"></a>Obter atividades

O OSC chama o método [ISocialProvider:: GetCapabilities](isocialprovider-getcapabilities.md) para determinar os recursos do provedor do OSC para uma rede social. Se os **** elementos getactivities e **dynamicActivitiesLookupEx** no XML de **recursos** retornados indicarem que o provedor OSC dá suporte à realização de atividades sob demanda e ao armazenamento de atividades na memória, o OSC poderá fazer o seguinte sequência de chamadas. O OSC também registra a função de hash especificada no elemento **hashFunction** no XML **Capabilities** . O OSC chama métodos na seguinte sequência para obter atividades e informações (conforme suportado pela interface [ISocialPerson](isocialpersoniunknown.md) ) para amigos e não amigos na rede social: 
  
1. [ISocialSession:: GetLoggedOnUser](isocialsession-getloggedonuser.md) – no final do processo de autenticação, o OSC chama **GetLoggedOnUser** para obter uma interface [métodoisocialprofile](isocialprofileisocialperson.md) para o usuário que está sendo autenticado. Para obter mais informações sobre autenticação, consulte [autenticação básica](basic-authentication.md) e [autenticação baseada em formulários](forms-based-authentication.md).
    
2. [ISocialSession2:: GetActivitiesEx](isocialsession2-getactivitiesex.md) — para as pessoas exibidas no painel de pessoas do Outlook, o OSC Obtém e codifica seus endereços SMTP, chama **ISocialSession2:: GetActivitiesEx**e armazena (na memória) os dados de atividades retornados para essas pessoas. O OSC Obtém um parâmetro de saída, _Activities_, que é uma cadeia de caracteres que contém uma coleção de atividades para amigos do usuário conectado. Essa cadeia de caracteres está em conformidade com a definição de esquema para o elemento **ofeed** . 
    
3. [ISocialSession:: GetPerson](isocialsession-getperson.md) — para cada elemento **ActivityDetails** no XML **ofeed** retornado por **GetActivitiesEx**, há um elemento **OwnerId** que indica a pessoa que possui essa atividade. O OSC usa esse **** valor OwnerId para chamar **GetPerson** para obter uma interface **ISocialPerson** para essa pessoa. 
    
4. [ISocialPerson:: GetDetails](isocialperson-getdetails.md) — com base no objeto **ISocialPerson** obtido da etapa 3, o OSC chama **GetDetails** para obter detalhes dessa pessoa, como nome e sobrenome. O OSC pode fazer o mesmo para cada atividade especificada em um elemento **activityDetails** no XML **Ofeed** retornado por **GetActivitiesEx** na etapa 2. 
    
> [!NOTE]
> O OSC atualiza o cache de atividades em um intervalo padrão. Para obter mais informações sobre como atualizar o cache de atividades, consulte [sincronizaNdo amigos e atividades](synchronizing-friends-and-activities.md). 
  
## <a name="see-also"></a>Confira também

- [XML para recursos](xml-for-capabilities.md)
- [Sequências de chamada típicas do OSC](osc-typical-calling-sequences.md)

