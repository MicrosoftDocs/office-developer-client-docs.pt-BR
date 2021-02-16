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
ms.openlocfilehash: 153bcbfd87ea9e85d834cba2fd9028e98fa25750
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420616"
---
# <a name="fbadrow"></a>FBadRow

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Valida uma linha em uma tabela.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapival.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Provedores de serviços  <br/> |
   
```cpp
ULONG FBadRow(
  LPSRow lprow
);
```

## <a name="parameters"></a>Parâmetros

 _lprow_
  
> [in] Ponteiro para uma [estrutura SRow](srow.md) que identifica a linha a ser validada. 
    
## <a name="return-value"></a>Valor de retorno

TRUE 
  
> A linha especificada é inválida.
    
FALSE 
  
> A linha especificada é válida.
    
## <a name="see-also"></a>Confira também



[FBadRowSet](fbadrowset.md)

