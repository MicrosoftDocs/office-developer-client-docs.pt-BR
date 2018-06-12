---
title: FBadRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FBadRow
api_type:
- COM
ms.assetid: 205d00df-488d-4888-8782-a1f70f54d720
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: c3025c353c71958a19303c5e79cec319a3bf8015
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766552"
---
# <a name="fbadrow"></a>FBadRow

  
  
**Aplica-se a**: Outlook 
  
Valida uma linha em uma tabela.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapival.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços  <br/> |
   
```cpp
ULONG FBadRow(
  LPSRow lprow
);
```

## <a name="parameters"></a>Par�metros

 _lprow_
  
> [in] Ponteiro para uma estrutura [SRow](srow.md) que identifica a linha a ser validado. 
    
## <a name="return-value"></a>Valor retornado

VERDADEIRO 
  
> A linha especificada é inválida.
    
FALSO 
  
> A linha especificada é válida.
    
## <a name="see-also"></a>Confira também



[FBadRowSet](fbadrowset.md)

