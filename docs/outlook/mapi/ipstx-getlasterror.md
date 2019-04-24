---
title: IPSTXGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTX.GetLastError
api_type:
- COM
ms.assetid: 68dc0ecc-881e-de69-faaa-90acb9857031
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 1d0fb16ba63548a44dba3920670c0e65f8c700a1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315096"
---
# <a name="ipstxgetlasterror"></a>IPSTX::GetLastError

  
  
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



[IPSTX::EmulateSpooler](ipstx-emulatespooler.md)
  
[IPSTX::GetSyncObject](ipstx-getsyncobject.md)

