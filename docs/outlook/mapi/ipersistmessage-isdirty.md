---
title: IPersistMessageIsDirty
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.IsDirty
api_type:
- COM
ms.assetid: 57f688db-3a1c-49ff-a15a-8508bda5de68
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 0d2ae556f4dd98b5f6e274a21c608d4ea364d4ec
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576201"
---
# <a name="ipersistmessageisdirty"></a>IPersistMessage::IsDirty

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Verifica o formulário para que as alterações feitas desde o último salvamento.
  
```cpp
HRESULT IsDirty( void );
```

## <a name="parameters"></a>Parâmetros

Nenhum
  
## <a name="return-value"></a>Valor retornado

S_OK 
  
> O formulário tem alterações feitas desde que foi salvo pela última vez.
    
S_FALSE 
  
> O formulário não terá as alterações feitas desde que foi salvo pela última vez.
    
## <a name="remarks"></a>Comentários

Visualizadores de formulário chame o método de **IPersistMessage::IsDirty** para determinar se a mensagem tem os dados. 
  
## <a name="see-also"></a>Confira também



[IPersistMessage : IUnknown](ipersistmessageiunknown.md)

