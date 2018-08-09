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
ms.openlocfilehash: 1767c86cb5390572b95530060f2295034ed35f43
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770464"
---
# <a name="smapiverbarray"></a>SMAPIVerbArray

  
  
**Aplica-se a**: Outlook 
  
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

