---
title: IsEqualMAPIUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.IsEqualMAPIUID
api_type:
- COM
ms.assetid: 85d71b73-0630-4c5d-b0e3-b48d27a300d0
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 635a4a872b83a2996b1a0198975a0ecd2cd906eb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767695"
---
# <a name="isequalmapiuid"></a>IsEqualMAPIUID

  
  
**Aplica-se a**: Outlook 
  
Testa duas estruturas [MAPIUID](mapiuid.md) para determinar se eles contêm o mesmo identificador. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
|Estrutura relacionada:  <br/> |**MAPIUID** <br/> |
   
```cpp
IsEqualMAPIUID(lpuid1, lpuid2)
```

## <a name="parameters"></a>Parâmetros

 _lpuid1_
  
> Ponteiro para a estrutura **MAPIUID** primeiro a ser testado. 
    
 _lpuid2_
  
> Ponteiro para a estrutura **MAPIUID** segundo a ser testado. 
    
## <a name="remarks"></a>Comentários

A macro **IsEqualMAPIUID** retorna TRUE se as duas estruturas **MAPIUID** contêm o mesmo identificador e FALSE se não tiverem. 
  
A macro **IsEqualMAPIUID** requer que o arquivo de cabeçalho Memory.h ser incluídos. 
  
## <a name="see-also"></a>Confira também



[MAPIUID](mapiuid.md)


[Macros relacionadas a estruturas](macros-related-to-structures.md)

