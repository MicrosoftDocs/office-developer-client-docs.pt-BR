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
ms.openlocfilehash: e748427b39418a80cae88e98b4aa7eef6df24393
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767612"
---
# <a name="ipersistmessageisdirty"></a>IPersistMessage::IsDirty

  
  
**Aplica-se a**: Outlook 
  
Verifica o formulário para que as alterações feitas desde o último salvamento.
  
```cpp
HRESULT IsDirty( void );
```

## <a name="parameters"></a>Parâmetros

None
  
## <a name="return-value"></a>Valor retornado

S_OK 
  
> O formulário tem alterações feitas desde que foi salvo pela última vez.
    
S_FALSE 
  
> O formulário não terá as alterações feitas desde que foi salvo pela última vez.
    
## <a name="remarks"></a>Coment�rios

Visualizadores de formulário chame o método de **IPersistMessage::IsDirty** para determinar se a mensagem tem os dados. 
  
## <a name="see-also"></a>Confira também



[IPersistMessage: IUnknown](ipersistmessageiunknown.md)

