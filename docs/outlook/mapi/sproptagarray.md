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
ms.openlocfilehash: 5237a5c2767920bdb604bfe86603cea4fca56b84
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572771"
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
  
> Contagem de marcas de propriedade na matriz indicado pelo membro **aulPropTag** . 
    
 **aulPropTag**
  
> Matriz de marcas de propriedade.
    
## <a name="remarks"></a>Comentários

Uma marca de propriedade é um inteiro não assinado de 32 bits que consiste em duas partes: 
  
- Um identificador nos superiores 16 bits.
    
- Um tipo nos ordem baixa 16 bits.
    
O identificador é um valor numérico em um determinado intervalo. MAPI define os intervalos para os identificadores descrever o que a propriedade é usada para e quem é responsável por manter a ele. MAPI define restrições para cada um das marcas de propriedade ao qual ele oferece suporte no arquivo de cabeçalho Mapitags.h.
  
O tipo indica o formato para o valor da propriedade. MAPI define as constantes para cada um dos tipos de propriedade que ele suporta no arquivo de cabeçalho Mapidefs.h. 
  
Para obter mais informações sobre marcas de propriedade e seus componentes, consulte um dos seguintes tópicos: 
  
[Marcas de propriedade MAPI](mapi-property-tags.md)
  
[Visão geral do identificador de propriedade MAPI](mapi-property-identifier-overview.md)
  
[Visão geral do tipo de propriedade MAPI](mapi-property-type-overview.md)
  
Para obter uma lista completa dos tipos de propriedade de valor único e de valores múltiplos, consulte o apêndice, [tipos e identificadores de propriedade](property-identifiers-and-types.md). 
  
## <a name="see-also"></a>Confira também



[Estruturas MAPI](mapi-structures.md)

