---
title: Obter atividades
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8cb8f916-f061-4c4c-ad1b-40d44af3345a
description: O OSC chama o método ISocialProvider::GetCapabilities para determinar os recursos do provedor de OSC para uma rede social.
ms.openlocfilehash: 82bb5322118fa3ebd7610f56b8f34ae95b59a40f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770824"
---
# <a name="getting-activities"></a>Obter atividades

O OSC chama o método [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) para determinar os recursos do provedor de OSC para uma rede social. Se os elementos **getActivities** e **dynamicActivitiesLookupEx** em **recursos** retornado XML indicarem que o provedor do OSC suporta Introdução atividades sob demanda e armazenando atividades na memória, o OSC pode fazer o seguinte: sequência de chamada. O OSC também notas a função de hash especificada no elemento **hashFunction** nas **capacidades** XML. O OSC chama os métodos na sequência a seguir para obter informações e atividades (conforme suportado pela interface [ISocialPerson](isocialpersoniunknown.md) ) de amigos e amigos na rede social: 
  
1. [ISocialSession::GetLoggedOnUser](isocialsession-getloggedonuser.md) — ao final do processo de autenticação, o OSC chama **GetLoggedOnUser** para obter uma interface [ISocialProfile](isocialprofileisocialperson.md) para o usuário que está sendo autenticado. Para obter mais informações sobre autenticação, consulte [Autenticação básica](basic-authentication.md) e [autenticação baseada em formulários](forms-based-authentication.md).
    
2. [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) — para as pessoas exibidas no painel de pessoas do Outlook, o OSC obtém e hashes lida com seu SMTP, chama **ISocialSession2::GetActivitiesEx**e armazena (na memória) os dados de atividades são retornadas para Essas pessoas. O OSC obtém um parâmetro de saída, _atividades_, que é uma cadeia de caracteres que contém uma coleção de atividades de amigos do usuário conectado. Esta cadeia de caracteres está de acordo com a definição de esquema para o elemento de **feed de atividades** . 
    
3. [ISocialSession::GetPerson](isocialsession-getperson.md) — para cada elemento **activityDetails** no **feed de atividades** XML retornado pelo **GetActivitiesEx**, há um elemento **ownerID** que indica que a atividade de proprietário. O OSC usa esse valor **ownerID** para chamar **GetPerson** para obter uma interface **ISocialPerson** dessa pessoa. 
    
4. [ISocialPerson::GetDetails](isocialperson-getdetails.md) — com base no objeto **ISocialPerson** obtido na etapa 3, o OSC chama **GetDetails** para obter detalhes dessa pessoa, como o nome e sobrenome. O OSC pode fazer o mesmo para cada atividade especificada em um elemento **activityDetails** no **feed de atividades** XML retornado pelo **GetActivitiesEx** na etapa 2. 
    
> [!NOTE]
> O OSC atualiza o cache de atividades em um intervalo padrão. Para obter mais informações sobre como atualizar o cache de atividades, consulte [Sincronizando amigos e atividades](synchronizing-friends-and-activities.md). 
  
## <a name="see-also"></a>Confira também

- [XML para recursos](xml-for-capabilities.md)
- [Sequências de chamadas comuns do OSC](osc-typical-calling-sequences.md)

