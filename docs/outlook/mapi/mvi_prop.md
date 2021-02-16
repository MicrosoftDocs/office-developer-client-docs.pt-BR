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
ms.openlocfilehash: 087d38face72e1e067350b1959b37313ebbd7c44
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410676"
---
# <a name="mvi_prop"></a>MVI_PROP

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Define o MVI_FLAG para uma propriedade especificada. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
|Estrutura relacionada:  <br/> |[SPropValue](spropvalue.md) <br/> |
   
```cpp
MVI_PROP (tag)
```

## <a name="parameters"></a>Parâmetros

 _tag_
  
> A marca de propriedade a ser modificada.
    
## <a name="remarks"></a>Comentários

O MVI_FLAG combina a configuração de MV_FLAG, identificando uma propriedade como de vários valores e MV_INSTANCE, solicitando que uma propriedade de vários valores seja exibida em uma tabela em várias linhas. O tipo de propriedade da propriedade afetada é modificado, mas o identificador permanece inalterado. 
  
Por exemplo, quando a MVI_PROP macro é aplicada a uma propriedade do tipo PT_FLOAT, seu tipo é alterado para PT_MV_FLOAT. Quando incluídas em uma tabela, várias linhas são usadas para representar a propriedade que tem uma linha para cada valor. As propriedades das outras colunas são repetidas. 
  
Para obter mais informações sobre esses sinalizadores, consulte Visão geral do tipo de propriedade [MAPI](mapi-property-type-overview.md) e [como trabalhar com colunas de múltiplos valores.](working-with-multivalued-columns.md)
  
## <a name="see-also"></a>Confira também



[SPropValue](spropvalue.md)


[Macros relacionadas a estruturas](macros-related-to-structures.md)

