---
title: ISocialSessionGetNetworkIdentifier
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 534e404f-54c6-4d2b-a8d0-d2ee990a972f
description: Obtém uma cadeia de caracteres que representa um identificador de rede social exclusivo para uma determinada conexão de rede social.
ms.openlocfilehash: 3051abd6dcccec878e8c53332980731772d543eb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433273"
---
# <a name="isocialsessiongetnetworkidentifier"></a>ISocialSession::GetNetworkIdentifier

Obtém uma cadeia de caracteres que representa um identificador de rede social exclusivo para uma determinada conexão de rede social. 
  
```cpp
HRESULT _stdcall GetNetworkIdentifier([out, retval] BSTR* networkIdentifier);
```

## <a name="parameters"></a>Parâmetros

_networkIdentifier_
  
> bota Uma cadeia de caracteres que contém um identificador de rede social exclusivo.
    
## <a name="remarks"></a>Comentários

Um identificador de rede exclusivo é uma cadeia de caracteres que identifica a rede social do provedor do Outlook Social Connector (OSC). Este método também pode retornar E_NOTIMPL.
  
## <a name="see-also"></a>Confira também

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

