---
title: IMAPISecureMessageGetBaseMessage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISecureMessage.GetBaseMessage
api_type:
- COM
ms.assetid: 573f40c5-e0d2-4281-8c22-10a1ae1f0dee
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 70c8bd36142d18b541ad6a2e0ded3bebcfb6dbb4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767158"
---
# <a name="imapisecuremessagegetbasemessage"></a>IMAPISecureMessage::GetBaseMessage

  
  
**Aplica-se a**: Outlook 
  
Recupera subjacente [IMessage: IMAPIProp](imessageimapiprop.md) que esta [IMAPISecureMessage: IUnknown](imapisecuremessageiunknown.md) é encapsular. 
  
```cpp
HRESULT GetBaseMessage(
  LPMMESSAGE FAR * ppmsg
);
```

## <a name="parameters"></a>Par�metros

 _ppmsg_
  
> [out] Um objeto de mensagem segura.
    
## <a name="return-value"></a>Valor retornado

S_OK
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
## <a name="see-also"></a>Confira também



[IMAPISecureMessage: IUnknown](imapisecuremessageiunknown.md)
  
[IMessage: IMAPIProp](imessageimapiprop.md)

