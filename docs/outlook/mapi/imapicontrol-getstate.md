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
ms.openlocfilehash: 3d45c4722b6a0200ea3937ba606da0af5c793df2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581850"
---
# <a name="imapicontrolgetstate"></a>IMAPIControl::GetState

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Recupera um valor que indica se o controle de botão está ativado ou desativado.
  
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
  
> [out] Um ponteiro para um valor que indica o estado do controle de botão. Pode ser retornado um dos seguintes valores:
    
MAPI_DISABLED 
  
> O controle de botão está desabilitado e não pode ser clicado. 
    
MAPI_ENABLED 
  
> O controle de botão é ativado e pode ser clicado.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O estado do controle botão foi recuperado com êxito.
    
## <a name="remarks"></a>Comentários

Provedores de serviços de implementam o método **IMAPIControl::GetState** para fornecer MAPI com o estado de um controle de botão. Se o botão estiver habilitado, ele pode responder a um clique do mouse ou pressionamento de tecla. Se ele estiver desabilitado, o botão aparece esmaecido e não responde a um clique do mouse ou pressionamento de tecla. 
  
Para obter mais informações sobre como implementar **GetState** e o outro [IMAPIControl: IUnknown](imapicontroliunknown.md) métodos, consulte a [Implementação do objeto de controle](control-object-implementation.md).
  
## <a name="see-also"></a>Confira também



[IMAPIControl::Activate](imapicontrol-activate.md)
  
[IMAPIControl : IUnknown](imapicontroliunknown.md)

