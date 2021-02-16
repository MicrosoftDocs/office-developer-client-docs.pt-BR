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
ms.openlocfilehash: 49e6c8254cbd527635685c3f974da57ee3ac82a5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411789"
---
# <a name="fbadrowset"></a>FBadRowSet

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Valida todas as linhas de tabela incluídas em um conjunto de linhas de tabela.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapival.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Provedores de serviços  <br/> |
   
```cpp
BOOL FBadRowSet(
  LPSRowSet lpRowSet
);
```

## <a name="parameters"></a>Parâmetros

 _lpRowSet_
  
> [in] Ponteiro para uma [estrutura SRowSet](srowset.md) identificando o conjunto de linhas a ser validado. Se o ponteiro for NULL, a estrutura será inválida. 
    
## <a name="return-value"></a>Valor de retorno

TRUE 
  
> Uma linha do conjunto de linhas especificado é inválida ou o próprio conjunto de linhas é inválido. 
    
FALSE 
  
> As linhas do conjunto de linhas especificado e o próprio conjunto de linhas são válidas.
    
## <a name="see-also"></a>Confira também



[FBadRow](fbadrow.md)

