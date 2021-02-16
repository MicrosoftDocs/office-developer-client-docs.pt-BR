---
title: ISocialSessionGetPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2d0a2945-54d7-417f-b5c6-2647c70263cf
description: Obtém uma interface ISocialPerson com base no parâmetro userID.
ms.openlocfilehash: b54e39b3712fb57d89d03787f1e5fa0ff50ff84a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439818"
---
# <a name="isocialsessiongetperson"></a>ISocialSession::GetPerson

Obtém uma interface [ISocialPerson](isocialpersoniunknown.md) com base no _parâmetro userID._ 
  
```cpp
HRESULT _stdcall GetPerson([in] BSTR userId, [out, retval] ISocialPerson** result);
```

## <a name="parameters"></a>Parâmetros

_userId_
  
> [in] Uma cadeia de caracteres que contém uma ID de usuário ou endereço SMTP de uma pessoa.
    
_result_
  
> [out] Uma interface **ISocialPerson.** 
    
## <a name="remarks"></a>Comentários

O  _parâmetro userID_ deve ser uma ID de usuário ou endereço SMTP. 
  
## <a name="see-also"></a>Confira também

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

