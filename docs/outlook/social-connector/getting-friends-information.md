---
title: Obter informações de amigos
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d8a56746-4de4-4f24-af32-e85079c060b8
description: Outlook Social Connector (OSC) chama o método ISocialProvider::GetCapabilities para determinar os recursos do provedor de OSC para uma rede social.
ms.openlocfilehash: 68443992351f4c83e8e560a753941e97bf91de67
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770821"
---
# <a name="getting-friends-information"></a>Obter informações de amigos

Outlook Social Connector (OSC) chama o método [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) para determinar os recursos do provedor de OSC para uma rede social. Se os elementos **getFriends** e **cacheFriends** em **recursos** retornado XML indicarem que o provedor do OSC oferece suporte a introdução de amigos e itens em uma pasta de contatos correspondente de contato de amigos cache como o Outlook, o OSC pode fazer a seguinte sequência de chamada. O OSC chama os métodos nesta sequência para obter informações e imagens (conforme suportado pela interface [ISocialPerson](isocialpersoniunknown.md) ) de amigos na rede social. 
  
> [!NOTE]
> O OSC atualiza o cache em um intervalo padrão. Se ocorrer um erro durante o cache atualize, as tentativas OSC em outro intervalo predefinido, o que também podem ser controlados especificando-se o elemento **contactSyncRestartInterval** nas **capacidades** XML. Para obter mais informações sobre como atualizar o cache de contatos, consulte [Sincronizando amigos e atividades](synchronizing-friends-and-activities.md). 
  
1. [ISocialSession::LoggedOnUserID](isocialsession-loggedonuserid.md) — o OSC obtém a identificação de usuário do usuário Office que é conectado à rede social. 
    
2. [ISocialSession::GetPerson](isocialsession-getperson.md) — usando a ID de usuário do usuário do Office, o OSC obtém um objeto de **ISocialPerson** para esse usuário. 
    
3. [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) — o OSC obtém a lista de amigos do usuário na rede social. 
    
4. [ISocialSession::GetPerson](isocialsession-getperson.md) — para cada pessoa no XML retornados por **GetFriendsAndColleagues**, o OSC obtém uma interface **ISocialPerson** . 
    
5. [ISocialPerson::GetPicture](isocialperson-getpicture.md) — para cada pessoa no XML retornados por **GetFriendsAndColleagues**, o OSC obtém um recurso de imagem.
    
## <a name="see-also"></a>Confira também

- [XML para recursos](xml-for-capabilities.md)
- [Sequências de chamadas comuns do OSC](osc-typical-calling-sequences.md)

