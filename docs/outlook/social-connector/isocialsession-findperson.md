---
title: ISocialSessionFindPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a86cb847-5d49-44b8-b2bc-0e35e70395b4
description: Obtém uma cadeia de caracteres que representa uma ou mais pessoas que corresponderem ao parâmetro userID.
ms.openlocfilehash: 1aa6478126e509c8d707d6a8d11b2c8428177bbd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434792"
---
# <a name="isocialsessionfindperson"></a>ISocialSession::FindPerson

Obtém uma cadeia de caracteres que representa uma ou mais pessoas que corresponderem ao _parâmetro userID._ 
  
```cpp
HRESULT _stdcall FindPerson([in] BSTR userId, [out, retval] BSTR* result);
```

## <a name="parameters"></a>Parâmetros

_userId_
  
> [in] Uma ID de usuário de rede social, endereço SMTP ou nome de exibição de uma pessoa.
    
_result_
  
> [out] Uma cadeia de caracteres XML que representa uma ou mais pessoas que corresponderem às informações de identificação especificadas pelo _parâmetro userId._ 
    
## <a name="remarks"></a>Comentários

Se uma ou mais pessoas corresponderem **à solicitação FindPerson,** esse método retornará as informações dessas pessoas no  _parâmetro de_ resultado. A  _cadeia_ de caracteres XML de resultado deve estar em conformidade com a definição de esquema para **amigos,** conforme definido no esquema para extensibilidade do provedor do Outlook Social Connector (OSC). 
  
## <a name="see-also"></a>Confira também

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

