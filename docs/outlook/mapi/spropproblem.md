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
ms.openlocfilehash: b3a0872c94459fc7c24d13e35adf335ef8012182
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407771"
---
# <a name="spropproblem"></a>SPropProblem

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Descreve um erro relacionado a uma operação envolvendo uma propriedade.
  
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
  
> Um índice em uma matriz de marcas de propriedade.
    
 **ulPropTag**
  
> Marca de propriedade da propriedade que tem o erro.
    
 **scode**
  
> Valor de erro que descreve o problema com a propriedade. Esse valor pode ser qualquer valor [de SCODE MAPI.](scode.md) 
    
## <a name="remarks"></a>Comentários

Uma matriz de **estruturas SPropProblem** é retornada dos seguintes métodos: 
  
- [IMAPISupport::DoCopyTo](imapisupport-docopyto.md)
    
- [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md)
    
- [IMAPIProp::DeleteProps](imapiprop-deleteprops.md)
    
- [IMAPIProp::SetProps](imapiprop-setprops.md)
    
- [IMAPIProp::CopyProps](imapiprop-copyprops.md)
    
- [IMAPIProp::CopyTo](imapiprop-copyto.md)
    
- [IPropData::HrAddObjProps](ipropdata-hraddobjprops.md)
    
Uma **estrutura SPropProblem** contém um valor de erro **SCODE** que resulta de uma operação tentando modificar ou excluir uma propriedade MAPI. 
  
Para obter mais informações sobre como **a estrutura SPropProblem** funciona com erros relacionados a propriedades, consulte [MAPI Named Properties](mapi-named-properties.md). 
  
## <a name="see-also"></a>Confira também



[SCODE](scode.md)
  
[SPropProblemArray](spropproblemarray.md)


[Estruturas MAPI](mapi-structures.md)

