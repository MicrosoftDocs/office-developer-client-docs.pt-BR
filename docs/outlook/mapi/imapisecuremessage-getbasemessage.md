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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: a2da3f6851e45a70dcd4604396a85430c539a830
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428575"
---
# <a name="imapisecuremessagegetbasemessage"></a>IMAPISecureMessage::GetBaseMessage

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Recupera o [IMessage subjacente: IMAPIProp](imessageimapiprop.md) que este [IMAPISecureMessage: IUnknown](imapisecuremessageiunknown.md) está encapsulando. 
  
```cpp
HRESULT GetBaseMessage(
  LPMMESSAGE FAR * ppmsg
);
```

## <a name="parameters"></a>Parâmetros

 _ppmsg_
  
> bota Um objeto Message seguro.
    
## <a name="return-value"></a>Valor de retorno

S_OK
  
> A chamada teve êxito e retornou o valor ou valores esperados.
    
## <a name="see-also"></a>Confira também



[IMAPISecureMessage : IUnknown](imapisecuremessageiunknown.md)
  
[IMessage : IMAPIProp](imessageimapiprop.md)

