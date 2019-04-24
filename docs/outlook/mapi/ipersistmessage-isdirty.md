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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309608"
---
# <a name="ipersistmessageisdirty"></a>IPersistMessage::IsDirty

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Verifica se há alterações feitas desde o último salvamento no formulário.
  
```cpp
HRESULT IsDirty( void );
```

## <a name="parameters"></a>Parâmetros

Nenhuma
  
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O formulário tem alterações feitas desde que foi salvo pela última vez.
    
S_FALSE 
  
> O formulário não tem alterações feitas desde que foi salvo pela última vez.
    
## <a name="remarks"></a>Comentários

Os visualizadores de formulários chamam o método **IPersistMessage:: IsDirty** para determinar se a mensagem tem dados não salvos. 
  
## <a name="see-also"></a>Confira também



[IPersistMessage : IUnknown](ipersistmessageiunknown.md)

