---
title: ISocialSessionFindPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a86cb847-5d49-44b8-b2bc-0e35e70395b4
description: Obtém um string que representa uma ou mais pessoas que coincidem com o parâmetro userID.
ms.openlocfilehash: 0b7525f853f7d97a991e2996a4e715cc53756d4a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770852"
---
# <a name="isocialsessionfindperson"></a>ISocialSession::FindPerson

Obtém um string que representa uma ou mais pessoas que coincidem com o parâmetro _userID_ . 
  
```cpp
HRESULT _stdcall FindPerson([in] BSTR userId, [out, retval] BSTR* result);
```

## <a name="parameters"></a>Parâmetros

_userId_
  
> [in] Uma ID de usuário de rede social, endereço SMTP ou nome de exibição de uma pessoa.
    
_resultado_
  
> [out] Uma sequência de caracteres XML que representa uma ou mais pessoas que coincidem com as informações de identificação especificadas pelo parâmetro _userId_ . 
    
## <a name="remarks"></a>Comentários

Se a solicitação de **FindPerson** corresponderem a uma ou mais pessoas, esse método retorna as informações de pessoas no parâmetro _resultado_ . A cadeia de caracteres XML de _resultado_ deve estar em conformidade com a definição de esquema para **amigos**, conforme definido no esquema para fornecer extensibilidade de provedor do Outlook Social Connector (OSC). 
  
## <a name="see-also"></a>Confira também

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

