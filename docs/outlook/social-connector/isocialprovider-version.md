---
title: ISocialProviderVersion
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: dfc92878-ab8b-4721-aee8-997c56a8e45b
description: Retorna uma string que representa o número de versão do provedor para esta rede social.
ms.openlocfilehash: 5c82df2dc4c052b1a06bcecb16defbb4dee38b18
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770849"
---
# <a name="isocialproviderversion"></a>ISocialProvider::Version

Retorna uma string que representa o número de versão do provedor para esta rede social. 
  
```cpp
[propget] HRESULT _stdcall Version([out, retval] BSTR* Version);
```

## <a name="property-value"></a>Property value

Uma string que contém o número de versão do provedor.
  
## <a name="remarks"></a>Comentários

A cadeia de caracteres de versão deve usar o _MajorVersion_. Formato _MinorVersion_ (por exemplo, 1.4730). 
  
## <a name="see-also"></a>Confira também

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

