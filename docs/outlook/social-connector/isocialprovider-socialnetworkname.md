---
title: ISocialProviderSocialNetworkName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 96f32db2-d654-4e72-88d1-ef955e3ff42b
description: Retorna uma string que representa o nome de rede social.
ms.openlocfilehash: 78424db0940b2c23914355b2b20ba5bc531ad3ca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770848"
---
# <a name="isocialprovidersocialnetworkname"></a>ISocialProvider::SocialNetworkName

Retorna uma string que representa o nome de rede social. 
  
```cpp
[propget] HRESULT _stdcall SocialNetworkName([out, retval] BSTR* networkName);
```

## <a name="property-value"></a>Property value

Uma cadeia de caracteres que contém o nome de rede social.
  
## <a name="remarks"></a>Coment�rios

Provedores do Outlook Social Connector (OSC) devem localizar o nome de rede social.
  
## <a name="see-also"></a>Confira também

- [ISocialProvider: IUnknown](isocialprovideriunknown.md)

