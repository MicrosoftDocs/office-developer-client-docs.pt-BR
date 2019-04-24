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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285757"
---
# <a name="isocialprovidergetcapabilities"></a>ISocialProvider::GetCapabilities

Obtém uma cadeia de caracteres que descreve os recursos do provedor.
  
```cpp
HRESULT _stdcall GetCapabilities([out, retval] BSTR* result);
```

## <a name="parameters"></a>Parâmetros

_result_
  
> bota Uma sequência de caracteres XML que representa os recursos de um provedor do Outlook Social Connector (OSC).
    
## <a name="remarks"></a>Comentários

A cadeia de caracteres XML do _resultado_ retornado deve estar em conformidade com a definição de esquema para o elemento **Capabilities** , conforme definido no esquema XML da EXTENSIBILIDADE do provedor do OSC. 
  
O provedor deve retornar uma cadeia de caracteres de _resultado_ para permitir que chamadas subsequentes do OSC para o provedor funcionem corretamente. 
  
## <a name="see-also"></a>Confira também

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

