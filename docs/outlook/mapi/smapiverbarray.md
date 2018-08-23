---
title: SMAPIVerbArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SMAPIVerbArray
api_type:
- COM
ms.assetid: 8736f75c-3e95-42dd-9bc1-2f0bd23c4a02
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7a2911779e5f9edb8c0bba7c3476a74ce410477c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569460"
---
# <a name="smapiverbarray"></a>SMAPIVerbArray

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém uma matriz de estruturas de [SMAPIVerb](smapiverb.md) que descrevem os verbos MAPI. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |MAPIForm.h  <br/> |
|Macro relacionada:  <br/> |[CbMAPIVerbArray](cbmapiverbarray.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cMAPIVerb;
  SMAPIVerb aMAPIVerb[MAPI_DIM];
} SMAPIVerbArray, FAR * LPMAPIVERBARRAY;

```

## <a name="members"></a>Members

 **cForms**
  
> Contagem de verbos na matriz.
    
 **aFormInfo**
  
> Matriz de verbos MAPI.
    
## <a name="remarks"></a>Comentários

A estrutura **SMAPIVerbArray** é passada como um parâmetro no método [IMAPIFormInfo::CalcVerbSet](imapiforminfo-calcverbset.md) . 
  
## <a name="see-also"></a>Confira também



[SMAPIVerb](smapiverb.md)


[Estruturas MAPI](mapi-structures.md)

