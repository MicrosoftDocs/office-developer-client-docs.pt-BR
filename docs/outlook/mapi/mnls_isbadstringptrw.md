---
title: MNLS_IsBadStringPtrW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 293a0700-b950-4fc2-a2e5-148d6c846384
description: 'Última modificação: 20 de fevereiro de 2012'
ms.openlocfilehash: 0e64df38afdb8ecce35eb0151d36dde3da35f0a4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356851"
---
# <a name="mnls_isbadstringptrw"></a>MNLS_IsBadStringPtrW

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Verifica se um ponteiro para uma cadeia de caracteres larga é válido.
  
```cpp
BOOL MNLS_IsBadStringPtrW(
  LPCWSTR lpsz,
  UINT ucchMax);
```

## <a name="parameters"></a>Parâmetros

 _lpsz_
  
> [in] Um ponteiro para a cadeia de caracteres larga.
    
 _ucchMax_
  
> [in] O comprimento máximo da cadeia de caracteres em caracteres, incluindo o terminador.
    
## <a name="return-value"></a>Valor de retorno

Retorna um Boolean que será true se a cadeia de caracteres for ruim.
  
## <a name="remarks"></a>Comentários

Esta função quebra [IsBadStringPtr](https://msdn.microsoft.com/library/aa366714%28VS.85%29.aspx). Para obter mais informações, consulte [IsBadStringPtr](https://msdn.microsoft.com/library/aa366714%28VS.85%29.aspx).
  

