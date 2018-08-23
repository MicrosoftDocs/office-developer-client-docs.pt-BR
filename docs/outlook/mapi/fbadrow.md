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
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 23b4ed78f4b65a5af4c2f3e11fa770030fe4eeee
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590159"
---
# <a name="fbadrow"></a>FBadRow

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
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

## <a name="parameters"></a>Parâmetros

 _lprow_
  
> [in] Ponteiro para uma estrutura [SRow](srow.md) que identifica a linha a ser validado. 
    
## <a name="return-value"></a>Valor retornado

VERDADEIRO 
  
> A linha especificada é inválida.
    
FALSO 
  
> A linha especificada é válida.
    
## <a name="see-also"></a>Confira também



[FBadRowSet](fbadrowset.md)

