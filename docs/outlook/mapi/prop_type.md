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
ms.openlocfilehash: 0c33633c4decd697cf241f8b7c27360f776a1ade
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412832"
---
# <a name="prop_type"></a>PROP_TYPE

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Retorna o tipo de propriedade de uma marca de propriedade especificada.
  
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

A **PROP_TYPE** macro pode ser usada para determinar o tipo de uma propriedade. Por exemplo, chamar PROP_TYPE (**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))) resulta no valor PT_BINARY sendo retornado.
  
Cada marca de propriedade contém o tipo de propriedade na palavra de ordem baixa (bits 0 a 15) e o identificador da propriedade na palavra de ordem alta (bits 16 a 31). A **PROP_TYPE** macro extrai o tipo de propriedade e o coloca nos bits 0 a 15 do inteiro a ser retornado. Os bits restantes do valor de retorno são definidos como zeros. 
  
## <a name="see-also"></a>Confira também



[SPropValue](spropvalue.md)


[Macros relacionadas a estruturas](macros-related-to-structures.md)

