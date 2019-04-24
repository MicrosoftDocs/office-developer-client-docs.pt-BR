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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336775"
---
# <a name="isocialsessionunfollowperson"></a>ISocialSession::UnFollowPerson

Remove a pessoa identificada pelo parâmetro _userid_ como um amigo na rede social. 
  
```cpp
HRESULT _stdcall UnFollowPerson([in] BSTR userID);
```

## <a name="parameters"></a>Parâmetros

_ID_
  
> no Uma cadeia de caracteres que contém uma ID de usuário de rede social para uma pessoa.
    
## <a name="remarks"></a>Comentários

O parâmetro _userid_ deve ser uma ID de usuário válida para a pessoa na rede social. 
  
Se o provedor do Outlook Social Connector (OSC) tiver definido **doNotFollowPerson** como **true** no XML para **recursos**, o provedor deverá retornar o erro OSC_E_NOT_FOUND, caso o ID de usuário passado não corresponda a um usuário na rede. Se o provedor tiver definido **doNotFollowPerson** como **falso** em **recursos**, o provedor deverá retornar o erro OSC_E_FAIL. Confira informações sobre os códigos de erro em [Códigos de Erro do Provedor do Conector Social do Outlook](outlook-social-connector-provider-error-codes.md).
  
## <a name="see-also"></a>Confira também

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

