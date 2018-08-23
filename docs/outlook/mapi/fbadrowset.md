---
title: FBadRowSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FBadRowSet
api_type:
- COM
ms.assetid: 3890dd50-e6ca-4859-bada-f6752ab61d41
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: e86e9fbf4901b5944775886f38db1ba12c4b122d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590957"
---
# <a name="fbadrowset"></a>FBadRowSet

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Valida todas as linhas de tabela incluídas em um conjunto de linhas da tabela.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapival.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços  <br/> |
   
```cpp
BOOL FBadRowSet(
  LPSRowSet lpRowSet
);
```

## <a name="parameters"></a>Parâmetros

 _lpRowSet_
  
> [in] Ponteiro para uma estrutura [SRowSet](srowset.md) que identifica a linha definida para ser validado. Se o ponteiro for NULL, a estrutura é inválida. 
    
## <a name="return-value"></a>Valor retornado

VERDADEIRO 
  
> Uma linha do conjunto de linha especificada é inválida ou linha do próprio conjunto é inválida. 
    
FALSO 
  
> As linhas do conjunto de linha especificada e a linha definida em si são válidos.
    
## <a name="see-also"></a>Confira também



[FBadRow](fbadrow.md)

