---
title: ISocialSessionGetLogonUrl
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d61bab07-acb3-433b-8783-c3fe110a5582
description: Obtém um string que representa uma URL que é usada para apresentar um formulário baseado em navegador para o usuário durante a autenticação da web.
ms.openlocfilehash: 343919f194b238fc519bb8f6d808b44a8ab6e7b9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770851"
---
# <a name="isocialsessiongetlogonurl"></a>ISocialSession::GetLogonUrl

Obtém um string que representa uma URL que é usada para apresentar um formulário baseado em navegador para o usuário durante a autenticação da web.
  
```cpp
HRESULT _stdcall GetLogonUrl([out, retval] BSTR* url);
```

## <a name="parameters"></a>Parâmetros

_URL_
  
> [out] Uma cadeia de caracteres que contém uma URL para o formulário usado na autenticação da web.
    
## <a name="remarks"></a>Comentários

Depois que o formulário é apresentado ao usuário, o método [ISocialSession::LogonWeb](isocialsession-logonweb.md) é chamado com uma sequência vazia para o parâmetro _connectIn_ . 
  
## <a name="see-also"></a>Confira também

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

