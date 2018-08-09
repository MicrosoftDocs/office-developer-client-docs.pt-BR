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
ms.openlocfilehash: e061808c57f25f881cc17fa5251e46ed5d524acd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767691"
---
# <a name="ipstxgetlasterror"></a>IPSTX::GetLastError

  
  
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



[IPSTX::EmulateSpooler](ipstx-emulatespooler.md)
  
[IPSTX::GetSyncObject](ipstx-getsyncobject.md)

