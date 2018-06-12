---
title: IMAPIOfflineSetCurrentState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOffline.SetCurrentState
api_type:
- COM
ms.assetid: c0aa0df2-79f9-2558-7eb6-accae9bef4b2
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 15e2d5c2aca595c3a06d215cd069c23da3e48125
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767112"
---
# <a name="imapiofflinesetcurrentstate"></a>IMAPIOffline::SetCurrentState

  
  
**Aplica-se a**: Outlook 
  
Define o estado atual de um objeto offline para online ou offline.
  
```cpp
HRESULT SetCurrentState( 
    ULONG ulFlags, 
    ULONG ulMask, 
    ULONG ulState, 
    void* pReserved 
);
```

## <a name="parameters"></a>Par�metros

 _ulFlags_
  
> [in] Modifica o comportamento desta chamada. Os valores suportados são:
    
MAPIOFFLINE_FLAG_BLOCK
  
> A definição de _ulFlags_ como esse valor bloqueará a chamada **SetCurrentState** até que a alteração de estado seja concluída. Por padrão a transição é feita de forma assíncrona. Quando a transição está ocorrendo de forma assíncrona, todas as chamadas **SetCurrentState** retornará **E_PENDING** até que a alteração seja concluída. 
    
MAPIOFFLINE_FLAG_DEFAULT
  
> Define o estado atual sem bloqueio.
    
 _ulMask_
  
> [in] A parte do estado para alterar. O único valor com suporte é MAPIOFFLINE_STATE_OFFLINE_MASK.
    
 _ulState_
  
> [in] Para alterar para o estado. Ele deve ser um destes dois valores:
    
MAPIOFFLINE_STATE_ONLINE
  
> 
    
MAPIOFFLINE_STATE_OFFLINE
  
> 
    
 _Preservadas_
  
> Este parâmetro é reservado para uso interno do Outlook e não é suportado. 
    
## <a name="return-value"></a>Valor retornado

S_OK
  
> O estado do objeto offline foi alterado com êxito.
    
E_PENDING
  
> Isso indica que o estado do objeto offline está mudando de forma assíncrona. Esse problema ocorre quando _ulFlags_ estiver definido como MAPIOFFLINE_FLAG_BLOCK em uma chamada de **SetCurrentState** anterior e qualquer chamada **SetCurrentState** subsequente irá retornar esse valor até que a alteração de estado assíncrona seja concluída. 
    
## <a name="see-also"></a>Confira também



[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)
  
[IMAPIOffline::GetCurrentState](imapioffline-getcurrentstate.md)


[Constantes MAPI](mapi-constants.md)

