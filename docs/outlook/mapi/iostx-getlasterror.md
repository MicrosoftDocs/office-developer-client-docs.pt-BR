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
ms.openlocfilehash: 9c29011ae2e9b59a7a0a38148fa6c5b673fd9590
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422296"
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

 _And_
  
>  no Código de erro. 
    
 _ulFlags_
  
>  [in] Sinalizadores para modificar o comportamento. Deve ser 0. 
    
 _lppMAPIError_
  
>  bota Ponteiro para a estrutura **MAPIERROR** que contém as informações estendidas do erro. Consulte mapidefs. h para a definição de tipo de **LPMAPIERROR**. 
    
## <a name="see-also"></a>Confira também



[IOSTX::InitSync](iostx-initsync.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncEnd](iostx-syncend.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX::SyncHdrEnd](iostx-synchdrend.md)
  
[IOSTX : IUnknown](iostxiunknown.md)


[Constantes de MAPI](mapi-constants.md)

