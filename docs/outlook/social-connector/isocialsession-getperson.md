---
title: ISocialSessionGetPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2d0a2945-54d7-417f-b5c6-2647c70263cf
description: Obtém uma interface ISocialPerson com base em que o parâmetro userID.
ms.openlocfilehash: 5769f4c41bb97f45ab722f1b3a3febe24c8a7ab2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770854"
---
# <a name="isocialsessiongetperson"></a>ISocialSession::GetPerson

Obtém uma interface [ISocialPerson](isocialpersoniunknown.md) com base em que o parâmetro _userID_ . 
  
```cpp
HRESULT _stdcall GetPerson([in] BSTR userId, [out, retval] ISocialPerson** result);
```

## <a name="parameters"></a>Parâmetros

_userId_
  
> [in] Uma cadeia de caracteres que contém um endereço SMTP ou de ID de usuário de uma pessoa.
    
_resultado_
  
> [out] Uma interface **ISocialPerson** . 
    
## <a name="remarks"></a>Comentários

O parâmetro _userID_ deve ser um endereço SMTP ou de ID de usuário. 
  
## <a name="see-also"></a>Confira também

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

