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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 91985d3dc8a7816c3da3215e505097c57c63e035
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407568"
---
# <a name="ipersistmessageisdirty"></a>IPersistMessage::IsDirty

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Verifica o formulário em busca de alterações feitas desde o último salvar.
  
```cpp
HRESULT IsDirty( void );
```

## <a name="parameters"></a>Parâmetros

Nenhum
  
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O formulário tem alterações que foram feitas desde que foi salvo pela última vez.
    
S_FALSE 
  
> O formulário não tem alterações feitas desde que foi salvo pela última vez.
    
## <a name="remarks"></a>Comentários

Os visualizadores de formulário chamam o método **IPersistMessage::IsDirty** para determinar se a mensagem tem dados não-sobresaldos. 
  
## <a name="see-also"></a>Confira também



[IPersistMessage : IUnknown](ipersistmessageiunknown.md)

