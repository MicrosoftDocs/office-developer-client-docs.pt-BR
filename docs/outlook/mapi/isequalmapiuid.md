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
ms.openlocfilehash: 0c72164cac8a37d0372ac93f4ed6d3face966ddb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566660"
---
# <a name="isequalmapiuid"></a>IsEqualMAPIUID

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
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

