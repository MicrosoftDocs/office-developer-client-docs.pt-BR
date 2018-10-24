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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 78ae0f78e154c17f774817238b2083d98a8fb809
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584678"
---
# <a name="iostxgetlasterror"></a>IOSTX::GetLastError

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
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


[Constantes de MAPI](mapi-constants.md)

