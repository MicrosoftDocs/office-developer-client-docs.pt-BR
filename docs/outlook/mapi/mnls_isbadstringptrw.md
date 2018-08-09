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
ms.openlocfilehash: dd7d310c8e801ba1246a0ce948aced9fa6a1a8af
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768143"
---
# <a name="mnlsisbadstringptrw"></a>MNLS_IsBadStringPtrW

  
  
**Aplica-se a**: Outlook 
  
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
  

