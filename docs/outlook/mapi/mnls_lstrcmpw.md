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
ms.openlocfilehash: 03b0eb794b07bc56ec6dce4a567d89294b2c908a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386345"
---
# <a name="mnlslstrcmpw"></a>MNLS_lstrcmpW

 
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
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
    
## <a name="return-value"></a>Valor de retorno

Retorna os valores descritos para uma chamada para **MNLS_CompareStringW** , exceto CSTR_EQUAL um equivalente. 
  
## <a name="remarks"></a>Comentários

 _MNLS_lstrcmpW_ executa uma comparação chamando [MNLS_CompareStringW](mnls_comparestringw.md) com uma localidade em GetUserDefaultLCID, 0 para sinalizadores e -1 para cch1 e cch2. 
  
## <a name="see-also"></a>Confira também



[GetUserDefaultLCID](https://msdn.microsoft.com/library/dd318135%28VS.85%29.aspx)

