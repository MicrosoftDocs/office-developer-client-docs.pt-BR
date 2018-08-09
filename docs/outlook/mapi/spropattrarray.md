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
ms.openlocfilehash: e9ad675e6df88265238a28f18e5cfcdacfdfbb5f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770477"
---
# <a name="spropattrarray"></a>SPropAttrArray

  
  
**Aplica-se a**: Outlook 
  
Contém uma lista de atributos para propriedades de um objeto. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |IMessage.h  <br/> |
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
  
> Uma matriz de atributos de propriedade. Os valores válidos para os atributos são:
    
    - PROPATTR_MANDATORY
    
    - PROPATTR_READABLE
    
    - PROPATTR_WRITEABLE
    
    - PROPATTR_NOT_PRESENT
    
## <a name="remarks"></a>Comentários

A estrutura **SPropAttrArray** é utilizada pelos objetos de dados de propriedade que implementam o [IPropData: IMAPIProp](ipropdataimapiprop.md) interface. Ele também é usado pela implementação do MAPI do [IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md) ou seja com base no armazenamento estruturado. 
  
## <a name="see-also"></a>Confira também



[IPropData: IMAPIProp](ipropdataimapiprop.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)
  
[CbNewSPropAttrArray](cbnewspropattrarray.md)
  
[CbSPropAttrArray](cbspropattrarray.md)


[Estruturas MAPI](mapi-structures.md)

