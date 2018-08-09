---
title: ISocialSession2 IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f516e86e-0158-472b-9711-fe7491b24404
description: Suporta a adição de amigos, a sincronização sob demanda ou híbrida de amigos, a sincronização sob demanda de atividades, ou de fazer logon na rede social usando credenciais armazenadas em cache.
ms.openlocfilehash: b14804d35e54ebe9fe2a529fb2664f0a661653bb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770868"
---
# <a name="isocialsession2--iunknown"></a>ISocialSession2 : IUnknown

Suporta a adição de amigos, a sincronização sob demanda ou híbrida de amigos, a sincronização sob demanda de atividades, ou de fazer logon na rede social usando credenciais armazenadas em cache.
  
## <a name="members"></a>Members

A tabela a seguir mostra os membros que estão disponíveis na interface **ISocialSession2** . 
  
|**Name**|**Tipo de membro**|**Descrição**|
|:-----|:-----|:-----|
|[FollowPersonEx](isocialsession2-followpersonex.md) <br/> |Método  <br/> |Adiciona a pessoa identificada pelos parâmetros _emailAddresses_ e _displayName_ como um amigo para o usuário de logon na rede social.  <br/> |
|[GetActivitiesEx](isocialsession2-getactivitiesex.md) <br/> |Método  <br/> |Obtém um string que representa uma coleção de atividades dos usuários especificados pelo parâmetro _hashedAddresses_ .  <br/> |
|[GetPeopleDetails](isocialsession2-getpeopledetails.md) <br/> |Método  <br/> |Retorna uma string que contém uma coleção de detalhes de imagem e a pessoa para os usuários especificados pelo parâmetro _personsAddresses_ .  <br/> |
|[LogonCached](isocialsession2-logoncached.md) <br/> |Método  <br/> |Logs para o site de rede social usando credenciais armazenadas em cache.  <br/> |
   
## <a name="remarks"></a>Comentários

Um provedor do Outlook Social Connector (OSC) pode optar por implementar essa interface, se o provedor oferece suporte a sincronização sob demanda ou híbrida de amigos, sincronização sob demanda de atividades, ou de fazer logon na rede social usando credenciais armazenadas em cache. Se o provedor do OSC implementa **ISocialSession2** e dá suporte às seguintes pessoas na rede social, o OSC chamaria [ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md) em vez de [ISocialSession::FollowPerson](isocialsession-followperson.md)e o provedor deve implementar **ISocialSession2::FollowPersonEx**, também.
  
## <a name="see-also"></a>Confira também

- [Interfaces do provedor do Outlook Social Connector](outlook-social-connector-provider-interfaces.md)

