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
ms.openlocfilehash: 54e28f22f2dc8fdbe19821d8188087b78c327518
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770844"
---
# <a name="isocialprovidergetcapabilities"></a>ISocialProvider::GetCapabilities

Obtém uma cadeia de caracteres que descreve os recursos do provedor.
  
```cpp
HRESULT _stdcall GetCapabilities([out, retval] BSTR* result);
```

## <a name="parameters"></a>Parâmetros

_resultado_
  
> [out] Uma sequência de caracteres XML que representa as capacidades de um provedor do Outlook Social Connector (OSC).
    
## <a name="remarks"></a>Comentários

A cadeia de caracteres retornada _resultado_ XML deve estar em conformidade com a definição de esquema para o elemento de **recursos** , conforme definido no esquema XML para fornecer extensibilidade de provedor do OSC. 
  
O provedor deve retornar uma cadeia de caracteres de _resultado_ para habilitar chamadas subsequentes provenientes do OSC para o provedor para que funcionem corretamente. 
  
## <a name="see-also"></a>Confira também

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

