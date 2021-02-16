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
ms.openlocfilehash: c276a9e5af18f7e4a3afbaa66d366d55de460a58
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418432"
---
# <a name="isocialsessionunfollowperson"></a>ISocialSession::UnFollowPerson

Remove a pessoa identificada pelo  _parâmetro userID_ como um amigo na rede social. 
  
```cpp
HRESULT _stdcall UnFollowPerson([in] BSTR userID);
```

## <a name="parameters"></a>Parâmetros

_userID_
  
> [in] Uma cadeia de caracteres que contém uma ID de usuário de rede social para uma pessoa.
    
## <a name="remarks"></a>Comentários

O  _parâmetro userID_ deve ser uma ID de usuário válida para a pessoa na rede social. 
  
Se o provedor do Outlook Social Connector (OSC) tiver definido **doNotFollowPerson** como **true** no XML para **recursos,** o provedor deverá retornar o erro OSC_E_NOT_FOUND caso a ID de usuário passada não corresponder a um usuário na rede. Se o provedor tiver definido **doNotFollowPerson** como **falso** nos **recursos,** o provedor deverá retornar o OSC_E_FAIL erro. Confira informações sobre os códigos de erro em [Códigos de Erro do Provedor do Conector Social do Outlook](outlook-social-connector-provider-error-codes.md).
  
## <a name="see-also"></a>Confira também

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

