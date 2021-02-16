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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 0b6837b51b09ecd9a60630c613e1806cb10c1d87
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421736"
---
# <a name="imapiofflinesetcurrentstate"></a>IMAPIOffline::SetCurrentState

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Define o estado atual de um objeto offline como online ou offline.
  
```cpp
HRESULT SetCurrentState( 
    ULONG ulFlags, 
    ULONG ulMask, 
    ULONG ulState, 
    void* pReserved 
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> [in] Modifica o comportamento dessa chamada. Os valores com suporte são:
    
MAPIOFFLINE_FLAG_BLOCK
  
> Definir  _ulFlags_ como esse valor bloqueará a **chamada SetCurrentState** até que a alteração de estado seja concluída. Por padrão, a transição ocorre de forma assíncrona. Quando a transição estiver ocorrendo de forma assíncrona, todas as chamadas **SetCurrentState** retornarão E_PENDING **até** que a alteração seja concluída. 
    
MAPIOFFLINE_FLAG_DEFAULT
  
> Define o estado atual sem bloqueio.
    
 _ulMask_
  
> [in] A parte do estado a ser mudada. O único valor com suporte é MAPIOFFLINE_STATE_OFFLINE_MASK.
    
 _ulState_
  
> [in] O estado para o que mudar. Deve ser um destes dois valores:
    
MAPIOFFLINE_STATE_ONLINE
  
> 
    
MAPIOFFLINE_STATE_OFFLINE
  
> 
    
 _pReserved_
  
> Esse parâmetro é reservado para uso interno do Outlook e não tem suporte. 
    
## <a name="return-value"></a>Valor de retorno

S_OK
  
> O estado do objeto offline foi alterado com êxito.
    
E_PENDING
  
> Isso indica que o estado do objeto offline está mudando de forma assíncrona. Isso ocorre quando  _ulFlags_ é definido como MAPIOFFLINE_FLAG_BLOCK em uma chamada **SetCurrentState** anterior e qualquer chamada **setCurrentState** subsequente retornará esse valor até que a alteração de estado assíncrona seja concluída. 
    
## <a name="see-also"></a>Confira também



[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)
  
[IMAPIOffline::GetCurrentState](imapioffline-getcurrentstate.md)


[Constantes de MAPI](mapi-constants.md)

