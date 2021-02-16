---
title: IMAPIControlGetState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIControl.GetState
api_type:
- COM
ms.assetid: fb321b48-3e5f-4b99-9af0-a57b66f26a2e
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: f477c617533d66fc129c7192c9f86bb8a46afbb1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419006"
---
# <a name="imapicontrolgetstate"></a>IMAPIControl::GetState

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Recupera um valor que indica se o controle de botão está habilitado ou desabilitado.
  
```cpp
HRESULT GetState(
  ULONG ulFlags,
  ULONG FAR * lpulState
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> [in] Reservado; deve ser zero.
    
 _lpulState_
  
> [out] Um ponteiro para um valor que indica o estado do controle de botão. Um dos seguintes valores pode ser retornado:
    
MAPI_DISABLED 
  
> O controle de botão está desabilitado e não pode ser clicado. 
    
MAPI_ENABLED 
  
> O controle de botão está habilitado e pode ser clicado.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O estado do controle de botão foi recuperado com êxito.
    
## <a name="remarks"></a>Comentários

Os provedores de serviços implementam **o método IMAPIControl::GetState** para fornecer MAPI com o estado de um controle de botão. Se o botão estiver habilitado, ele poderá responder a um clique do mouse ou pressionar tecla. Se estiver desabilitado, o botão aparecerá esmaecida e não responderá a um clique do mouse ou pressionada por tecla. 
  
For more information about how to implement **GetState** and the other [IMAPIControl : IUnknown](imapicontroliunknown.md) methods, see [Control Object Implementation](control-object-implementation.md).
  
## <a name="see-also"></a>Confira também



[IMAPIControl::Activate](imapicontrol-activate.md)
  
[IMAPIControl : IUnknown](imapicontroliunknown.md)

