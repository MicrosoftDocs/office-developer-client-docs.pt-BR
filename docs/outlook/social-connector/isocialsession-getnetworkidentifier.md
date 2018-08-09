---
title: ISocialSessionGetNetworkIdentifier
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 534e404f-54c6-4d2b-a8d0-d2ee990a972f
description: Obtém um string que representa um identificador exclusivo de redes sociais para uma conexão de rede social fornecido.
ms.openlocfilehash: eb618ba8e8bb37278c1fdb09d984fba141a9d686
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770978"
---
# <a name="isocialsessiongetnetworkidentifier"></a>ISocialSession::GetNetworkIdentifier

Obtém um string que representa um identificador exclusivo de redes sociais para uma conexão de rede social fornecido. 
  
```cpp
HRESULT _stdcall GetNetworkIdentifier([out, retval] BSTR* networkIdentifier);
```

## <a name="parameters"></a>Parâmetros

_networkIdentifier_
  
> [out] Uma cadeia de caracteres que contém um identificador exclusivo de redes sociais.
    
## <a name="remarks"></a>Comentários

Um identificador exclusivo de rede é uma cadeia de caracteres que identifica a rede social de provedor do Outlook Social Connector (OSC). Este método também pode retornar E_NOTIMPL.
  
## <a name="see-also"></a>Confira também

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

