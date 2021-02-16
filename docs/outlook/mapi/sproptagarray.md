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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430697"
---
# <a name="sproptagarray"></a>SPropTagArray

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém uma matriz de marcas de propriedade. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
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
  
> Contagem de marcas de propriedade na matriz indicada pelo membro **aulPropTag.** 
    
 **aulPropTag**
  
> Matriz de marcas de propriedade.
    
## <a name="remarks"></a>Comentários

Uma marca de propriedade é um inteiro não assinado de 32 bits que consiste em duas partes: 
  
- Um identificador nos 16 bits de alta ordem.
    
- Um tipo nos 16 bits de ordem baixa.
    
O identificador é um valor numérico em um intervalo específico. O MAPI define intervalos para que os identificadores descrevam para que a propriedade é usada e para quem é responsável por mantê-la. MAPI define restrições para cada uma das marcas de propriedade que ele suporta no arquivo de título Mapitags.h.
  
O tipo indica o formato do valor da propriedade. MAPI define constantes para cada um dos tipos de propriedade que ele suporta no arquivo de header Mapidefs.h. 
  
Para obter mais informações sobre marcas de propriedade e seus componentes, consulte um dos seguintes tópicos: 
  
[Marcas de propriedade MAPI](mapi-property-tags.md)
  
[Visão geral do identificador de propriedade MAPI](mapi-property-identifier-overview.md)
  
[Visão geral do tipo de propriedade MAPI](mapi-property-type-overview.md)
  
Para uma lista completa dos tipos de propriedade de valor único e de vários valores, consulte o apêndice, Identificadores e tipos [de propriedade.](property-identifiers-and-types.md) 
  
## <a name="see-also"></a>Confira também



[Estruturas MAPI](mapi-structures.md)

