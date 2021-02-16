---
title: Obter informações de amigos
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d8a56746-4de4-4f24-af32-e85079c060b8
description: O Outlook Social Connector (OSC) chama o método ISocialProvider::GetCapabilities para determinar os recursos do provedor OSC para uma rede social.
ms.openlocfilehash: 697902631b010afab015e9cfb73fac81ac427d6e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428792"
---
# <a name="getting-friends-information"></a>Obter informações de amigos

O Outlook Social Connector (OSC) chama o método [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) para determinar os recursos do provedor OSC para uma rede social. Se os elementos **getFriends** e **cacheFriends** no **XML** de recursos retornados indicarem que o provedor OSC dá suporte a obter amigos e armazenar em cache amigos como itens de contato do Outlook em uma pasta de contatos correspondente, o OSC poderá fazer a seguinte sequência de chamada. O OSC chama métodos nesta sequência para obter informações e imagens (conforme suportado pela interface [ISocialPerson)](isocialpersoniunknown.md) para amigos na rede social. 
  
> [!NOTE]
> O OSC atualiza o cache em um intervalo padrão. Se ocorrer um erro durante a atualização do cache, o OSC se recuperará em outro intervalo predefinido, que também pode ser controlado especificando o elemento **contactSyncRestartInterval** no **XML** de recursos. Para obter mais informações sobre como atualizar o cache de contatos, consulte [Sincronizando amigos e atividades.](synchronizing-friends-and-activities.md) 
  
1. [ISocialSession::LoggedOnUserID](isocialsession-loggedonuserid.md) — O OSC obtém a ID de usuário do Office que está conectado à rede social. 
    
2. [ISocialSession::GetPerson](isocialsession-getperson.md) — Usando a ID de usuário do usuário do Office, o OSC obtém um objeto **ISocialPerson** para esse usuário. 
    
3. [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) — O OSC obtém a lista de amigos do usuário na rede social. 
    
4. [ISocialSession::GetPerson](isocialsession-getperson.md) — Para cada pessoa no XML retornado por **GetFriendsAndColleagues**, o OSC obtém uma interface **ISocialPerson.** 
    
5. [ISocialPerson::GetPicture](isocialperson-getpicture.md) — Para cada pessoa no XML retornado por **GetFriendsAndColleagues**, o OSC obtém um recurso de imagem.
    
## <a name="see-also"></a>Confira também

- [XML para recursos](xml-for-capabilities.md)
- [Sequências de chamada típicas do OSC](osc-typical-calling-sequences.md)

