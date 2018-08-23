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
ms.openlocfilehash: a8f4e62a8eb1b5e61cb0223c66b921e15ab9423b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577678"
---
# <a name="spropattrarray"></a>SPropAttrArray

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
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

