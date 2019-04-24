---
title: Obter informações de amigos
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d8a56746-4de4-4f24-af32-e85079c060b8
description: 'O Outlook Social Connector (OSC) chama o método ISocialProvider:: GetCapabilities para determinar as funcionalidades do provedor do OSC para uma rede social.'
ms.openlocfilehash: 697902631b010afab015e9cfb73fac81ac427d6e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286319"
---
# <a name="getting-friends-information"></a>Obter informações de amigos

O Outlook Social Connector (OSC) chama o método [ISocialProvider:: GetCapabilities](isocialprovider-getcapabilities.md) para determinar as funcionalidades do provedor do OSC para uma rede social. Se os **** elementos getfriends e **cacheFriends** no XML de **recursos** retornados indicarem que o provedor OSC dá suporte ao recebimento de amigos e ao cache de amigos como itens de contato do Outlook em uma pasta contatos correspondente, o OSC poderá fazer a sequência de chamadas a seguir. O OSC chama métodos nesta sequência para obter informações e imagens (conforme suportado pela interface [ISocialPerson](isocialpersoniunknown.md) ) para amigos na rede social. 
  
> [!NOTE]
> O OSC atualiza o cache em um intervalo padrão. Se ocorrer um erro durante a atualização do cache, o OSC tentará novamente em outro intervalo predefinido, que também pode ser controlado especificando o elemento **contactSyncRestartInterval** no XML de **recursos** . Para obter mais informações sobre como atualizar o cache de contatos, consulte [sincronizaNdo amigos e atividades](synchronizing-friends-and-activities.md). 
  
1. [ISocialSession:: LoggedOnUserID](isocialsession-loggedonuserid.md) – o OSC Obtém a ID de usuário do usuário do Office que está conectada à rede social. 
    
2. [ISocialSession:: GetPerson](isocialsession-getperson.md) — usando a ID de usuário do usuário do Office, o OSC Obtém um objeto **ISocialPerson** para esse usuário. 
    
3. [ISocialPerson:: GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) – o OSC Obtém a lista de amigos do usuário na rede social. 
    
4. [ISocialSession:: GetPerson](isocialsession-getperson.md) — para cada pessoa no XML retornado por **GETFRIENDSANDCOLLEAGUES**, o OSC Obtém uma interface **ISocialPerson** . 
    
5. [ISocialPerson:: GetPicture](isocialperson-getpicture.md) — para cada pessoa no XML retornada por **GETFRIENDSANDCOLLEAGUES**, o OSC Obtém um recurso Picture.
    
## <a name="see-also"></a>Confira também

- [XML para recursos](xml-for-capabilities.md)
- [Sequências de chamada típicas do OSC](osc-typical-calling-sequences.md)

