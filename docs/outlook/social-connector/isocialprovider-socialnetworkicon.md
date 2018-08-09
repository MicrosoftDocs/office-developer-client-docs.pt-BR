---
title: ISocialProviderSocialNetworkIcon
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8b51675f-77b7-4df0-8496-b1e8958c6544
description: Retorna uma matriz de bytes que representa o ícone para a rede social.
ms.openlocfilehash: b86a2d1c14c444ba79db495a3795dc61b1fe3660
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770974"
---
# <a name="isocialprovidersocialnetworkicon"></a>ISocialProvider::SocialNetworkIcon

Retorna uma matriz de bytes que representa o ícone para a rede social. 
  
```cpp
[propget] HRESULT _stdcall SocialNetworkIcon([out, retval] SAFEARRAY(unsigned char)* networkIcon);
```

## <a name="property-value"></a>Property value

Um ponteiro para uma estrutura que especifica uma matriz de bytes que contém o ícone para a rede social.
  
## <a name="remarks"></a>Comentários

Os recursos de imagem com suporte são formatos. png,. JPEG e. bmp.
  
## <a name="see-also"></a>Confira também

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

