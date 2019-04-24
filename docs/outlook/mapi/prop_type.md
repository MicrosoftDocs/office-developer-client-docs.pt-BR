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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332757"
---
# <a name="proptype"></a>PROP_TYPE

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Retorna o tipo de propriedade de uma marca de propriedade especificada.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs. h  <br/> |
|Estrutura relacionada:  <br/> |[SPropValue](spropvalue.md) <br/> |
   
```cpp
PROP_TYPE (ulPropTag)
```

## <a name="parameters"></a>Parâmetros

 _ulPropTag_
  
> Marca de propriedade que contém o tipo de propriedade a ser retornado.
    
## <a name="remarks"></a>Comentários

A macro **PROP_TYPE** pode ser usada para determinar o tipo de uma propriedade. Por exemplo, chamar PROP_TYPE (**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))) resulta no valor PT_BINARY que está sendo retornado.
  
Cada marca de propriedade contém o tipo de propriedade na palavra de ordem inferior (bits 0 a 15) e o identificador de propriedade na palavra de ordem alta (bits 16 a 31). A macro **PROP_TYPE** extrai o tipo de propriedade e a coloca em bits 0 a 15 do inteiro a ser retornado. Os bits restantes do valor de retorno são definidos como zeros. 
  
## <a name="see-also"></a>Confira também



[SPropValue](spropvalue.md)


[Macros relacionadas a estruturas](macros-related-to-structures.md)

