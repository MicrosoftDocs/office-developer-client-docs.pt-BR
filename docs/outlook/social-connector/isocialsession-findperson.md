---
title: ISocialSessionFindPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a86cb847-5d49-44b8-b2bc-0e35e70395b4
description: Obtém uma cadeia de caracteres que representa uma ou mais pessoas que correspondem ao parâmetro userID.
ms.openlocfilehash: 1aa6478126e509c8d707d6a8d11b2c8428177bbd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285368"
---
# <a name="isocialsessionfindperson"></a>ISocialSession::FindPerson

Obtém uma cadeia de caracteres que representa uma ou mais pessoas que correspondem ao parâmetro _userid_ . 
  
```cpp
HRESULT _stdcall FindPerson([in] BSTR userId, [out, retval] BSTR* result);
```

## <a name="parameters"></a>Parâmetros

_ID_
  
> no Uma ID de usuário de rede social, um endereço SMTP ou um nome de exibição de uma pessoa.
    
_result_
  
> bota Uma sequência de caracteres XML que representa uma ou mais pessoas que correspondem às informações de identificação especificadas pelo parâmetro _userid_ . 
    
## <a name="remarks"></a>Comentários

Se uma ou mais pessoas corresponderem à solicitação **FindPerson** , este método retornará as informações dessas pessoas no parâmetro _Result_ . A cadeia de caracteres XML do _resultado_ deve estar em conformidade com a definição de esquema para **amigos**, conforme definido no esquema para a extensibilidade do provedor do Outlook Social Connector (OSC). 
  
## <a name="see-also"></a>Confira também

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

