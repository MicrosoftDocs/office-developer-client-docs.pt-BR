---
title: ISocialSession2 IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f516e86e-0158-472b-9711-fe7491b24404
description: O suporta a adição de amigos, a sincronização por demanda ou híbrida de amigos, a sincronização sob demanda de atividades ou o logon na rede social usando credenciais armazenadas em cache.
ms.openlocfilehash: 6dc581bb812408d7e01f94c375671783445616a1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345294"
---
# <a name="isocialsession2--iunknown"></a>ISocialSession2 : IUnknown

O suporta a adição de amigos, a sincronização por demanda ou híbrida de amigos, a sincronização sob demanda de atividades ou o logon na rede social usando credenciais armazenadas em cache.
  
## <a name="members"></a>Members

A tabela a seguir mostra os membros que estão disponíveis na interface **ISocialSession2** . 
  
|**Nome**|**Tipo de membro**|**Descrição**|
|:-----|:-----|:-----|
|[FollowPersonEx](isocialsession2-followpersonex.md) <br/> |Método		  <br/> |Adiciona a pessoa identificada pelos __ parâmetros EmailAddresses e _DisplayName_ como um amigo para o usuário conectado na rede social.  <br/> |
|[GetActivitiesEx](isocialsession2-getactivitiesex.md) <br/> |Método		  <br/> |Obtém uma cadeia de caracteres que representa uma coleção de atividades dos usuários especificados pelo parâmetro _hashedAddresses_ .  <br/> |
|[GetPeopleDetails](isocialsession2-getpeopledetails.md) <br/> |Método		  <br/> |Retorna uma cadeia de caracteres que contém uma coleção de detalhes de pessoa e imagem para os usuários especificados pelo parâmetro _personsAddresses_ .  <br/> |
|[LogonCached](isocialsession2-logoncached.md) <br/> |Método		  <br/> |Faz logon no site de rede social usando credenciais armazenadas em cache.  <br/> |
   
## <a name="remarks"></a>Comentários

Um provedor do Outlook Social Connector (OSC) pode optar por implementar essa interface se o provedor oferecer suporte à sincronização por demanda ou híbrida de amigos, à sincronização sob demanda de atividades ou ao fazer logon na rede social usando credenciais armazenadas em cache. Se o provedor do OSC implementar o **ISocialSession2** e suportar as seguintes pessoas na rede social, o OSC chamaria [ISocialSession2:: FollowPersonEx](isocialsession2-followpersonex.md) em vez de [ISocialSession:: FollowPerson](isocialsession-followperson.md)e o provedor deve implementar **ISocialSession2:: FollowPersonEx**também.
  
## <a name="see-also"></a>Confira também

- [Interfaces do provedor do Outlook Social Connector](outlook-social-connector-provider-interfaces.md)

