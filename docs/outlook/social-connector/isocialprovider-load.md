---
title: ISocialProviderLoad
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6356f7bf-e3a1-4294-ad6e-df77bdd0356c
description: Inicializa o provedor do Outlook Social Connector (OSC).
ms.openlocfilehash: 172595db8d9467f22a80c8caf0e3444250826aaf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770846"
---
# <a name="isocialproviderload"></a>ISocialProvider::Load

Inicializa o provedor do Outlook Social Connector (OSC).
  
```cpp
HRESULT _stdcall Load([in] BSTR socialProviderInterfaceVersion, [in] BSTR languageTag);
```

## <a name="parameters"></a>Parâmetros

_socialProviderInterfaceVersion_
  
> [in] A versão das interfaces do provedor do OSC esperado pelo OSC.
    
_languageTag_
  
> [in] A Internet Engineering Task Force (IETF) marca de idioma, definida por [[RFC4646]](http://www.ietf.org/rfc/rfc4646.txt) e [[RFC4647]](http://www.ietf.org/rfc/rfc4647.txt), que representa o idioma de interface do usuário atual do Outlook.
    
## <a name="remarks"></a>Comentários

O formato de versão para o parâmetro _socialProviderInterfaceVersion_ é _X_. _xxxx_, onde _X_ é a versão principal e _xxxx_ é a versão secundária do OSC. Para o Office 2013, verifique a versão principal sendo 15. 
  
## <a name="see-also"></a>Confira também

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

