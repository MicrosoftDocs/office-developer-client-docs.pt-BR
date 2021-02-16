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
ms.openlocfilehash: 44e3613338c8932bc80dd1150392033dfa3cd050
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426930"
---
# <a name="isequalmapiuid"></a>IsEqualMAPIUID

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Testa duas [estruturas MAPIUID](mapiuid.md) para determinar se elas contêm o mesmo identificador. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
|Estrutura relacionada:  <br/> |**MAPIUID** <br/> |
   
```cpp
IsEqualMAPIUID(lpuid1, lpuid2)
```

## <a name="parameters"></a>Parâmetros

 _lpuid1_
  
> Ponteiro para a primeira **estrutura MAPIUID** a ser testada. 
    
 _lpuid2_
  
> Ponteiro para a segunda **estrutura MAPIUID** a ser testada. 
    
## <a name="remarks"></a>Comentários

A macro **IsEqualMAPIUID** retornará TRUE se as duas estruturas **MAPIUID** contêm o mesmo identificador e FALSE se não contêm. 
  
A macro **IsEqualMAPIUID** requer que o arquivo de título Memory.h seja incluído. 
  
## <a name="see-also"></a>Confira também



[MAPIUID](mapiuid.md)


[Macros relacionadas a estruturas](macros-related-to-structures.md)

