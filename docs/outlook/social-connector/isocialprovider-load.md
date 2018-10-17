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
ms.openlocfilehash: 73d14f66785417e80448f622256d0b9cb059b83c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385827"
---
# <a name="isocialproviderload"></a>ISocialProvider::Load

Inicializa o provedor do Outlook Social Connector (OSC).
  
```cpp
HRESULT _stdcall Load([in] BSTR socialProviderInterfaceVersion, [in] BSTR languageTag);
```

## <a name="parameters"></a>Parâmetros

_socialProviderInterfaceVersion_
  
> [in] A versão das interfaces do provedor do OSC esperada pelo OSC.
    
_languageTag_
  
> [in] A marcação de idioma da Internet Engineering Task Force (IETF), definida por [[RFC4646]](https://www.ietf.org/rfc/rfc4646.txt) e [[RFC4647]](https://www.ietf.org/rfc/rfc4647.txt), que representa o idioma atual da interface de usuário do Outlook.
    
## <a name="remarks"></a>Comentários

O formato de versão para o parâmetro _socialProviderInterfaceVersion_ é _X_. _xxxx_, em que _X_ é a versão principal e _xxxx_ é a versão secundária do OSC. No Office 2013, confira se a versão principal é a 15. 
  
## <a name="see-also"></a>Confira também

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

