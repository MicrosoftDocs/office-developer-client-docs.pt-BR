---
title: IOSTXGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.GetLastError
api_type:
- COM
ms.assetid: b25c9288-b391-6303-3643-5a5b66b75c48
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 69853dbec46b08c4dc402012fb7f1074f30ebf52
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767568"
---
# <a name="iostxgetlasterror"></a>IOSTX::GetLastError

  
  
**Aplica-se a**: Outlook 
  
Obtém informações estendidas sobre o último erro.
  
```cpp
HRESULT GetLastError( 
    HRESULT hResult, 
    ULONG ulFlags, 
    LPMAPIERROR *lppMAPIError 
);
```

## <a name="parameters"></a>Parâmetros

 _hResult_
  
>  [in] Código de erro. 
    
 _ulFlags_
  
>  [in] Sinalizadores para modificar o comportamento. Isso deve ser de 0. 
    
 _lppMAPIError_
  
>  [out] Ponteiro para a estrutura **MAPIERROR** que contém as informações estendidas para o erro. Consulte mapidefs.h para a definição de tipo de **LPMAPIERROR**. 
    
## <a name="see-also"></a>Confira também



[IOSTX::InitSync](iostx-initsync.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncEnd](iostx-syncend.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX::SyncHdrEnd](iostx-synchdrend.md)
  
[IOSTX : IUnknown](iostxiunknown.md)


[Constantes MAPI](mapi-constants.md)

