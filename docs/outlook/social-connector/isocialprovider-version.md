---
title: ISocialProviderVersion
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: dfc92878-ab8b-4721-aee8-997c56a8e45b
description: Retorna uma cadeia de caracteres que representa o número de versão do provedor para esta rede social.
ms.openlocfilehash: 0749b8fb83a11328233442b79e1f9de50076effe
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438271"
---
# <a name="isocialproviderversion"></a>ISocialProvider::Version

Retorna uma cadeia de caracteres que representa o número de versão do provedor para esta rede social. 
  
```cpp
[propget] HRESULT _stdcall Version([out, retval] BSTR* Version);
```

## <a name="property-value"></a>Valor de propriedade

Uma cadeia de caracteres que contém o número de versão do provedor.
  
## <a name="remarks"></a>Comentários

A cadeia de caracteres de versão deve usar o _MajorVersion_. Formato _MinorVersion_ (por exemplo, 1,4730). 
  
## <a name="see-also"></a>Confira também

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

