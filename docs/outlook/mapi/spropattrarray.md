---
title: SPropAttrArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SPropAttrArray
api_type:
- COM
ms.assetid: 30dd19d9-0840-49e9-aec6-ec8d19b1f91d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 55cba4f7cfb3fa8035117348b10ab1d6d3082710
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358111"
---
# <a name="spropattrarray"></a>SPropAttrArray

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém uma lista de atributos para propriedades de um objeto. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |IMessage. h  <br/> |
|Macros relacionadas:  <br/> |[CbNewSPropAttrArray](cbnewspropattrarray.md), [CbSPropAttrArray](cbspropattrarray.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cValues;
  ULONG aPropAttr[MAPI_DIM];
} SPropAttrArray, FAR *LPSPropAttrArray;

```

## <a name="members"></a>Members

 **cValues**
  
> Contagem de atributos de propriedade no membro **aPropAttr** . 
    
 **aPropAttr**
  
> Uma matriz de atributos de propriedade. Os valores válidos para atributos são os seguintes:
    
    - PROPATTR_MANDATORY
    
    - PROPATTR_READABLE
    
    - PROPATTR_WRITEABLE
    
    - PROPATTR_NOT_PRESENT
    
## <a name="remarks"></a>Comentários

A estrutura **SPropAttrArray** é usada por objetos de dados de propriedade que implementam a interface [IPropData: IMAPIProp](ipropdataimapiprop.md) . Ele também é usado pela implementação de MAPI do [IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md) que se baseia no armazenamento estruturado. 
  
## <a name="see-also"></a>Confira também



[IPropData: IMAPIProp](ipropdataimapiprop.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)
  
[CbNewSPropAttrArray](cbnewspropattrarray.md)
  
[CbSPropAttrArray](cbspropattrarray.md)


[Estruturas MAPI](mapi-structures.md)

