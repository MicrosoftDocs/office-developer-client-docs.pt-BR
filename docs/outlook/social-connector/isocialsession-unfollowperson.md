---
title: ISocialSessionUnFollowPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 66c83041-ee83-41d5-b9dc-a4dc4c670f82
description: Remove a pessoa identificada pelo parâmetro userID como um amigo na rede social.
ms.openlocfilehash: 8b9a1e4f903e4bc805481b8679481103ea1ec82c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770865"
---
# <a name="isocialsessionunfollowperson"></a>ISocialSession::UnFollowPerson

Remove a pessoa identificada pelo parâmetro _userID_ como um amigo na rede social. 
  
```cpp
HRESULT _stdcall UnFollowPerson([in] BSTR userID);
```

## <a name="parameters"></a>Parâmetros

_userID_
  
> [in] Uma cadeia de caracteres que contém uma ID de usuário de rede social de uma pessoa.
    
## <a name="remarks"></a>Comentários

O parâmetro _userID_ deve ser uma ID de usuário válido para a pessoa na rede social. 
  
Se o provedor do Outlook Social Connector (OSC) definiu **doNotFollowPerson** como **true** no XML de **recursos**, o provedor deve retornar o erro OSC_E_NOT_FOUND no caso em que o usuário que ID informado não corresponde a um usuário na rede. Se o provedor definiu **doNotFollowPerson** como **false** em **recursos**, o provedor deve retornar o erro OSC_E_FAIL. Confira informações sobre os códigos de erro em [Códigos de Erro do Provedor do Conector Social do Outlook](outlook-social-connector-provider-error-codes.md).
  
## <a name="see-also"></a>Confira também

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

