---
title: PROP_TYPE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PROP_TYPE
api_type:
- COM
ms.assetid: 746d63fa-bfb7-479f-94dc-ba40011c1ec9
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 91a9d15544ebc71d27c8a9a6f930f3c32ecaa4fe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770176"
---
# <a name="proptype"></a>PROP_TYPE

  
  
**Aplica-se a**: Outlook 
  
Retorna o tipo de propriedade de uma marca de propriedade especificado.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
|Estrutura relacionada:  <br/> |[SPropValue](spropvalue.md) <br/> |
   
```cpp
PROP_TYPE (ulPropTag)
```

## <a name="parameters"></a>Parâmetros

 _ulPropTag_
  
> Marca de propriedade que contém o tipo de propriedade a ser retornado.
    
## <a name="remarks"></a>Comentários

A macro **PROP_TYPE** pode ser usada para determinar o tipo de uma propriedade. Por exemplo, chamando PROP_TYPE (**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))) resultados no valor PT_BINARY sendo retornados.
  
A marca de cada propriedade contém o tipo de propriedade da palavra de ordem baixa (0 a 15 bits) e o identificador de propriedade da palavra de ordem alta (16 a 31 bits). A macro **PROP_TYPE** extrai o tipo de propriedade e a coloca em bits 0 a 15 do inteiro a ser retornado. Os bits restantes do valor de retorno são definidos com zeros. 
  
## <a name="see-also"></a>Confira também



[SPropValue](spropvalue.md)


[Macros relacionadas a estruturas](macros-related-to-structures.md)

