---
title: SPropProblem
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SPropProblem
api_type:
- COM
ms.assetid: 55943197-fd11-442d-bb4b-0bff565b846e
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7c19cce33ec351a5627870782ebb4fe509a98be2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573282"
---
# <a name="spropproblem"></a>SPropProblem

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Descreve um erro que se relacionam com uma operação envolvendo uma propriedade.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SPropProblem
{
  ULONG ulIndex;
  ULONG ulPropTag;
  SCODE scode;
} SPropProblem, FAR *LPSPropProblem;

```

## <a name="members"></a>Members

 **ulIndex**
  
> Um índice em uma matriz das marcas de propriedade.
    
 **ulPropTag**
  
> Marca de propriedade para a propriedade que tem o erro.
    
 **SCODE**
  
> Valor de erro descrevendo o problema com a propriedade. Esse valor pode ser qualquer valor MAPI [SCODE](scode.md) . 
    
## <a name="remarks"></a>Comentários

Uma matriz de estruturas de **SPropProblem** é retornada dos seguintes métodos: 
  
- [IMAPISupport::DoCopyTo](imapisupport-docopyto.md)
    
- [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md)
    
- [IMAPIProp::DeleteProps](imapiprop-deleteprops.md)
    
- [IMAPIProp::SetProps](imapiprop-setprops.md)
    
- [IMAPIProp::CopyProps](imapiprop-copyprops.md)
    
- [IMAPIProp::CopyTo](imapiprop-copyto.md)
    
- [IPropData::HrAddObjProps](ipropdata-hraddobjprops.md)
    
Uma estrutura **SPropProblem** contém um valor de erro **SCODE** resultante de uma operação tentando modificar ou excluir uma propriedade MAPI. 
  
Para obter mais informações sobre como a estrutura de **SPropProblem** funciona com erros relacionados às propriedades, consulte [Propriedades de chamada de MAPI](mapi-named-properties.md). 
  
## <a name="see-also"></a>Confira também



[SCODE](scode.md)
  
[SPropProblemArray](spropproblemarray.md)


[Estruturas MAPI](mapi-structures.md)

