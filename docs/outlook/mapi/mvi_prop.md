---
title: MVI_PROP
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MVI_PROP
api_type:
- COM
ms.assetid: d7f07524-6935-4a60-aaf3-3f753ea8d86a
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: f8f58ee18095dec8a222ae8b5a19cbefbaafa663
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768179"
---
# <a name="mviprop"></a>MVI_PROP

  
  
**Aplica-se a**: Outlook 
  
Define o MVI_FLAG para uma propriedade especificada. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
|Estrutura relacionada:  <br/> |[SPropValue](spropvalue.md) <br/> |
   
```cpp
MVI_PROP (tag)
```

## <a name="parameters"></a>Parâmetros

 _marca_
  
> A marca de propriedade a ser modificada.
    
## <a name="remarks"></a>Comentários

O MVI_FLAG combina a configuração da MV_FLAG, que identifica uma propriedade como valores múltiplos e MV_INSTANCE, solicitando que uma propriedade de valores múltiplos exibida em uma tabela em várias linhas. O tipo de propriedade da propriedade afetado é modificado, mas o identificador permanecerá inalterado. 
  
Por exemplo, quando a macro MVI_PROP é aplicada a uma propriedade do tipo PT_FLOAT, seu tipo é alterado para PT_MV_FLOAT. Quando incluído em uma tabela, várias linhas são usadas para representar a propriedade que tem uma linha para cada valor. As propriedades das outras colunas são repetidas. 
  
Para obter mais informações sobre esses sinalizadores, consulte [Visão geral do tipo de propriedade de MAPI](mapi-property-type-overview.md) e [trabalhar com vários valores de colunas](working-with-multivalued-columns.md).
  
## <a name="see-also"></a>Confira também



[SPropValue](spropvalue.md)


[Macros relacionadas a estruturas](macros-related-to-structures.md)

