---
title: FBUser
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal649b5400-8dc5-cc5c-3455-f462e2d31689
ms.assetid: ''
description: Identifica um usuário que pode ou não ter livre/ocupado dados disponíveis.
ms.openlocfilehash: 2511a94678f9ef8f2cb6be868db4f718d92ecb6d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387899"
---
# <a name="fbuser"></a>FBUser

Identifica um usuário que pode ou não ter livre/ocupado dados disponíveis.
  
## <a name="quick-info"></a>Informações rápidas

```cpp
typedef struct tagFBUser 
{ 
   ULONG m_cbEid; 
   LPENTRYID m_lpEid; 
   ULONG m_ulReserved; 
   LPWSTR m_pwszReserved; 
} FBUser;

```

## <a name="members"></a>Members

_m_cbEid_
  
> O comprimento da identificação de entrada do usuário de email como representado pela interface [IMailUser](https://docs.microsoft.com/previous-versions/windows/desktop/wab/-wab-imailuser-deleteprops) . 
    
_m_lpEid_
  
> A identificação de entrada do usuário de email como representado pela interface **IMailUser** . 
    
_m_ulReserved_
  
> Este parâmetro é reservado para uso interno do Outlook e não é suportado.
    
_m_pwszReserved_
  
> Este parâmetro é reservado para uso interno do Outlook e não é suportado.
    
## <a name="see-also"></a>Confira também

- [Sobre a API do serviço de disponibilidade](about-the-free-busy-api.md)  
- [IFreeBusySupport](ifreebusysupport.md)

