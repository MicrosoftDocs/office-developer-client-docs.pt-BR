---
title: ISocialSessionGetLogonUrl
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d61bab07-acb3-433b-8783-c3fe110a5582
description: Obtém uma cadeia de caracteres que representa uma URL que é usada para apresentar um formulário baseado em navegador ao usuário durante a autenticação da Web.
ms.openlocfilehash: 83867282922ea136b9673609cc2ba2f1a206f6ab
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427910"
---
# <a name="isocialsessiongetlogonurl"></a>ISocialSession::GetLogonUrl

Obtém uma cadeia de caracteres que representa uma URL que é usada para apresentar um formulário baseado em navegador ao usuário durante a autenticação da Web.
  
```cpp
HRESULT _stdcall GetLogonUrl([out, retval] BSTR* url);
```

## <a name="parameters"></a>Parâmetros

_url_
  
> bota Uma cadeia de caracteres que contém uma URL para o formulário usado na autenticação da Web.
    
## <a name="remarks"></a>Comentários

Depois que o formulário é apresentado ao usuário, o método [ISocialSession:: LogonWeb](isocialsession-logonweb.md) é chamado com uma cadeia de caracteres vazia __ para o parâmetro connectem. 
  
## <a name="see-also"></a>Confira também

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

