---
title: ISocialSession2 IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f516e86e-0158-472b-9711-fe7491b24404
description: Oferece suporte à adição de amigos, sob demanda ou sincronização híbrida de amigos, sincronização sob demanda de atividades ou logor na rede social usando credenciais armazenadas em cache.
ms.openlocfilehash: 6dc581bb812408d7e01f94c375671783445616a1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408828"
---
# <a name="isocialsession2--iunknown"></a>ISocialSession2 : IUnknown

Oferece suporte à adição de amigos, sob demanda ou sincronização híbrida de amigos, sincronização sob demanda de atividades ou logor na rede social usando credenciais armazenadas em cache.
  
## <a name="members"></a>Members

A tabela a seguir mostra os membros que estão disponíveis na interface **ISocialSession2.** 
  
|**Nome**|**Tipo de membro**|**Descrição**|
|:-----|:-----|:-----|
|[FollowPersonEx](isocialsession2-followpersonex.md) <br/> |Method  <br/> |Adiciona a pessoa identificada pelos parâmetros  _emailAddresses_ e  _displayName_ como um amigo do usuário conectado na rede social.  <br/> |
|[GetActivitiesEx](isocialsession2-getactivitiesex.md) <br/> |Method  <br/> |Obtém uma cadeia de caracteres que representa uma coleção de atividades dos usuários especificados pelo _parâmetro hashedAddresses._  <br/> |
|[GetPeopleDetails](isocialsession2-getpeopledetails.md) <br/> |Method  <br/> |Retorna uma cadeia de caracteres que contém uma coleção de detalhes de pessoa e imagem para os usuários especificados pelo _parâmetro personsAddresses._  <br/> |
|[LogonCached](isocialsession2-logoncached.md) <br/> |Method  <br/> |Faz o login no site da rede social usando credenciais armazenadas em cache.  <br/> |
   
## <a name="remarks"></a>Comentários

Um provedor do Outlook Social Connector (OSC) pode optar por implementar essa interface se o provedor suportar a sincronização sob demanda ou híbrida de amigos, sincronização sob demanda de atividades ou logon na rede social usando credenciais armazenadas em cache. Se o provedor OSC implementar **ISocialSession2** e suportar as seguintes pessoas na rede social, o OSC chamará [ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md) em vez de [ISocialSession::FollowPerson](isocialsession-followperson.md), e o provedor deverá implementar **ISocialSession2::FollowPersonEx**, também.
  
## <a name="see-also"></a>Confira também

- [Interfaces do provedor do Outlook Social Connector](outlook-social-connector-provider-interfaces.md)

