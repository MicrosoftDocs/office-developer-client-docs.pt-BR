---
title: FBUser
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal649b5400-8dc5-cc5c-3455-f462e2d31689
ms.assetid: ''
description: Identifica um usuário que pode ou não ter dados de disponibilidade disponíveis.
ms.openlocfilehash: 2511a94678f9ef8f2cb6be868db4f718d92ecb6d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317658"
---
# <a name="fbuser"></a>FBUser

Identifica um usuário que pode ou não ter dados de disponibilidade disponíveis.
  
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

## <a name="members"></a>Membros

_m_cbEid_
  
> O comprimento da ID de entrada do usuário de email conforme representado pela interface [IMailUser](https://docs.microsoft.com/previous-versions/windows/desktop/wab/-wab-imailuser-deleteprops) . 
    
_m_lpEid_
  
> A identificação de entrada do usuário de email conforme representado pela interface **IMailUser** . 
    
_m_ulReserved_
  
> Este parâmetro é reservado para uso interno do Outlook e não tem suporte.
    
_m_pwszReserved_
  
> Este parâmetro é reservado para uso interno do Outlook e não tem suporte.
    
## <a name="see-also"></a>Confira também

- [Sobre a API do serviço de disponibilidade](about-the-free-busy-api.md)  
- [IFreeBusySupport](ifreebusysupport.md)

