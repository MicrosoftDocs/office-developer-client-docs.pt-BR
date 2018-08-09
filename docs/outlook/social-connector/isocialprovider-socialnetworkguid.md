---
title: ISocialProviderSocialNetworkGuid
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3c07f71d-b906-4a7f-b20a-4a7f558dbf11
description: Retorna um GUID que representa um identificador exclusivo para a rede social.
ms.openlocfilehash: 5ff10d51fab03c3bca3eead52848088f2cd80bba
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770863"
---
# <a name="isocialprovidersocialnetworkguid"></a>ISocialProvider::SocialNetworkGuid

Retorna um GUID que representa um identificador exclusivo para a rede social.
  
```cpp
[propget] HRESULT _stdcall SocialNetworkGuid([out, retval] GUID* guid);
```

## <a name="property-value"></a>Property value

Um ponteiro para um valor GUID que representa um identificador exclusivo para a rede social.
  
## <a name="remarks"></a>Comentários

O GUID deve ser imutável e não deve alterar, mesmo se altera a versão do provedor.
  
## <a name="see-also"></a>Confira também

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

