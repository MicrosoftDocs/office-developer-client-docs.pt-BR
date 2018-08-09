---
title: IOlkAccountHelperHandsOffSession
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9f71fdef-5df5-0892-b64c-293a2f22f5c3
description: Libera o objeto de sessão MAPI que foi retornado por IOlkAccountHelper::GetMapiSession.
ms.openlocfilehash: 71931be73e75e858224d3da2c92071341ac45e72
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765950"
---
# <a name="iolkaccounthelperhandsoffsession"></a>IOlkAccountHelper::HandsOffSession

Libera o objeto de sessão MAPI que foi retornado por - [IOlkAccountHelper::GetMapiSession](iolkaccounthelper-getmapisession.md).
  
## <a name="quick-info"></a>Informações rápidas

Consulte [IOlkAccountHelper](iolkaccounthelper.md).
  
```cpp
HRESULT IOlkAccountHelper::HandsOffSession( );
```

## <a name="return-values"></a>Valores de retorno

|**HRESULT**|**Descrição**|
|:-----|:-----|
|S_OK  <br/> |Se a implementação dos **IOlkAccountHelper** criar sua própria sessão MAPI que é retornado em **IOlkAccountHelper::GetMapiSession**, você deve liberar aqui, a sessão e retornar S_OK.  <br/> |
|E_NOTIMPL  <br/> |Se a implementação dos **IOlkAccountHelper** não criou seu próprio sessão MAPI, você deverá retornar somente E_NOTIMPL. Nesse caso, isso é o único valor de retorno com suporte.  <br/> |
   
## <a name="see-also"></a>Confira também

- [Constantes (API de gerenciamento de conta)](constants-account-management-api.md)  
- [IOlkAccountHelper::GetMapiSession](iolkaccounthelper-getmapisession.md)

