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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: a6ae89bf9b2b16439cc06f0e106859dda10ea22c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/15/2018
ms.locfileid: "19766943"
---
# <a name="imapicontrolgetstate"></a>IMAPIControl::GetState

  
  
**Aplica-se a**: Outlook 
  
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
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> O estado do controle botão foi recuperado com êxito.
    
## <a name="remarks"></a>Comentários

Provedores de serviços de implementam o método **IMAPIControl::GetState** para fornecer MAPI com o estado de um controle de botão. Se o botão estiver habilitado, ele pode responder a um clique do mouse ou pressionamento de tecla. Se ele estiver desabilitado, o botão aparece esmaecido e não responde a um clique do mouse ou pressionamento de tecla. 
  
Para obter mais informações sobre como implementar **GetState** e o outro [IMAPIControl: IUnknown](imapicontroliunknown.md) métodos, consulte a [Implementação do objeto de controle](control-object-implementation.md).
  
## <a name="see-also"></a>Confira também



[IMAPIControl::Activate](imapicontrol-activate.md)
  
[IMAPIControl : IUnknown](imapicontroliunknown.md)

