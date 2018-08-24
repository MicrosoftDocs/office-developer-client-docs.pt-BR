---
title: MNLS_IsBadStringPtrW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 293a0700-b950-4fc2-a2e5-148d6c846384
description: 'Modificado pela última vez: 20 de fevereiro de 2012'
ms.openlocfilehash: 0052d0bd6b485340a92cca9f22ca65c9e2442df6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589564"
---
# <a name="mnlsisbadstringptrw"></a>MNLS_IsBadStringPtrW

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Verifica se um ponteiro para uma cadeia de caracteres longa é válido.
  
```cpp
BOOL MNLS_IsBadStringPtrW(
  LPCWSTR lpsz,
  UINT ucchMax);
```

## <a name="parameters"></a>Parâmetros

 _lpsz_
  
> [in] Um ponteiro para a cadeia de caracteres longa.
    
 _ucchMax_
  
> [in] O comprimento máximo da cadeia de caracteres em caracteres, incluindo o terminador.
    
## <a name="return-value"></a>Valor retornado

Retorna um Boolean que será true se a cadeia de caracteres é defeituoso.
  
## <a name="remarks"></a>Comentários

Essa função distribui [IsBadStringPtr](http://msdn.microsoft.com/en-us/library/aa366714%28VS.85%29.aspx). Para obter mais informações, consulte [IsBadStringPtr](http://msdn.microsoft.com/en-us/library/aa366714%28VS.85%29.aspx).
  

