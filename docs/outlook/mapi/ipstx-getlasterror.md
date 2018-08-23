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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: f45b070464fe1b3c177088ff6aa3295f961d45f6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592588"
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

 _hResult_
  
>  [in] Código de erro. 
    
 _ulFlags_
  
>  [in] Sinalizadores para modificar o comportamento. Isso deve ser de 0. 
    
 _lppMAPIError_
  
>  [out] Ponteiro para a estrutura **MAPIERROR** que contém as informações estendidas para o erro. Consulte mapidefs.h para a definição de tipo de **LPMAPIERROR**. 
    
## <a name="see-also"></a>Confira também



[IPSTX::EmulateSpooler](ipstx-emulatespooler.md)
  
[IPSTX::GetSyncObject](ipstx-getsyncobject.md)

