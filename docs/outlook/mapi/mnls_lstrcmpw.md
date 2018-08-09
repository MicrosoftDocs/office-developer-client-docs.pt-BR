---
title: MNLS_lstrcmpW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d26c59d7-c839-426f-8693-727fc6bef67e
description: 'Modificado pela última vez: 18 de junho de 2012'
ms.openlocfilehash: 8ffd3c8337edcd96af6c3c4e425d274b21fee9f6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768136"
---
# <a name="mnlslstrcmpw"></a>MNLS_lstrcmpW

 
  
**Aplica-se a**: Outlook 
  
Compara duas cadeias de caracteres Unicode.
  
```cpp
int MNLS_lstrcmpW(
  LPCWSTR lpString1,
  LPCWSTR lpString2);
```

## <a name="parameters"></a>Parâmetros

 _lpString1_
  
> [in] Ponteiro para a primeira cadeia de caracteres Unicode para comparar.
    
 _lpString2_
  
> [in] Ponteiro para a segunda cadeia de caracteres Unicode para comparar.
    
## <a name="return-value"></a>Valor retornado

Retorna os valores descritos para uma chamada para **MNLS_CompareStringW** , exceto CSTR_EQUAL um equivalente. 
  
## <a name="remarks"></a>Comentários

 _MNLS_lstrcmpW_ executa uma comparação chamando [MNLS_CompareStringW](mnls_comparestringw.md) com uma localidade em GetUserDefaultLCID, 0 para sinalizadores e -1 para cch1 e cch2. 
  
## <a name="see-also"></a>Confira também



[GetUserDefaultLCID](http://msdn.microsoft.com/en-us/library/dd318135%28VS.85%29.aspx)
