---
title: ISocialProviderGetCapabilities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f40d5405-12e3-475b-b731-d2223ab70c1d
description: Obtém uma cadeia de caracteres que descreve os recursos do provedor.
ms.openlocfilehash: cf3d1418ac0ecbfc3f67bb550a24ec71781f2637
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408100"
---
# <a name="isocialprovidergetcapabilities"></a>ISocialProvider::GetCapabilities

Obtém uma cadeia de caracteres que descreve os recursos do provedor.
  
```cpp
HRESULT _stdcall GetCapabilities([out, retval] BSTR* result);
```

## <a name="parameters"></a>Parâmetros

_result_
  
> [out] Uma cadeia de caracteres XML que representa os recursos de um provedor do Outlook Social Connector (OSC).
    
## <a name="remarks"></a>Comentários

A cadeia  _de caracteres_ XML de resultado retornado deve estar em conformidade com a definição de esquema para o elemento **capabilities,** conforme definido no esquema XML para extensibilidade do provedor OSC. 
  
O provedor deve retornar uma cadeia  _de_ caracteres de resultado para permitir que chamadas subsequentes do OSC para o provedor funcionem corretamente. 
  
## <a name="see-also"></a>Confira também

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

