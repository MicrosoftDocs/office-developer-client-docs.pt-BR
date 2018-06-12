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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: e6963fc373f771289e3dbff3a0b41857352b4b9a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766559"
---
# <a name="fbadrowset"></a>FBadRowSet

  
  
**Aplica-se a**: Outlook 
  
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

## <a name="parameters"></a>Par�metros

 _lpRowSet_
  
> [in] Ponteiro para uma estrutura [SRowSet](srowset.md) que identifica a linha definida para ser validado. Se o ponteiro for NULL, a estrutura é inválida. 
    
## <a name="return-value"></a>Valor retornado

VERDADEIRO 
  
> Uma linha do conjunto de linha especificada é inválida ou linha do próprio conjunto é inválida. 
    
FALSO 
  
> As linhas do conjunto de linha especificada e a linha definida em si são válidos.
    
## <a name="see-also"></a>Confira também



[FBadRow](fbadrow.md)

