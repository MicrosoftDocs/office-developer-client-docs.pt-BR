---
title: SPropTagArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SPropTagArray
api_type:
- COM
ms.assetid: 4a9e1579-bebe-4a51-8ced-6dba9c3bcb63
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 9a5be98298ab1f9333ac1c223a6ef594e60dd86a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344433"
---
# <a name="sproptagarray"></a>SPropTagArray

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém uma matriz de marcas de propriedade. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs. h  <br/> |
|Macros relacionadas:  <br/> |[CbNewSPropTagArray](cbnewsproptagarray.md), [CbSPropTagArray](cbsproptagarray.md), [SizedSPropTagArray](sizedsproptagarray.md) <br/> |
   
```cpp
typedef struct _SPropTagArray
{
  ULONG cValues;
  ULONG aulPropTag[MAPI_DIM];
} SPropTagArray, FAR *LPSPropTagArray;

```

## <a name="members"></a>Members

 **cValues**
  
> Contagem de marcas de propriedade na matriz indicada pelo membro **aulPropTag** . 
    
 **aulPropTag**
  
> Matriz de marcas de propriedade.
    
## <a name="remarks"></a>Comentários

Uma marca de propriedade é um inteiro não assinado de 32 bits que consiste em duas partes: 
  
- Um identificador na ordem alta de 16 bits.
    
- Um tipo na ordem baixa de 16 bits.
    
O identificador é um valor numérico em um intervalo específico. MAPI define intervalos para identificadores para descrever o que a propriedade é usada e quem é responsável por mantê-la. MAPI define restrições para cada uma das marcas de propriedade que ele suporta no arquivo de cabeçalho Mapitags. h.
  
O tipo indica o formato do valor da propriedade. MAPI define constantes para cada um dos tipos de propriedade que ele suporta no arquivo de cabeçalho mapidefs. h. 
  
Para obter mais informações sobre marcas de propriedade e seus componentes, consulte um dos seguintes tópicos: 
  
[Marcas de propriedade MAPI](mapi-property-tags.md)
  
[Visão geral do identificador de propriedade MAPI](mapi-property-identifier-overview.md)
  
[Visão geral do tipo de propriedade MAPI](mapi-property-type-overview.md)
  
Para obter uma lista completa dos tipos de propriedade de valor único e múltiplos valores, confira o apêndice, os identificadores de [propriedade e os tipos](property-identifiers-and-types.md). 
  
## <a name="see-also"></a>Confira também



[Estruturas MAPI](mapi-structures.md)

