---
title: FBadSortOrderSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FBadSortOrderSet
api_type:
- COM
ms.assetid: b7f80e0a-8ddd-4b24-ab63-2078a8152058
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 31840923e24cddd0dc3dfa9cc67b610d0dcd7e47
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428456"
---
# <a name="fbadsortorderset"></a>FBadSortOrderSet

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Valida uma ordem de classificação definida verificando sua alocação de memória. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapival.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Provedores de serviços  <br/> |
   
```cpp
ULONG FBadSortOrderSet(
  LPSSortOrderSet lpsos
);
```

## <a name="parameters"></a>Parâmetros

 _Lpsos_
  
> no Ponteiro para uma estrutura [SSortOrderSet](ssortorderset.md) identificando a ordem de classificação definida para ser validada. 
    
## <a name="return-value"></a>Valor de retorno

TRUE 
  
> O conjunto de ordem de classificação especificado é inválido. 
    
FALSE 
  
> O conjunto de ordem de classificação especificado é válido.
    
## <a name="remarks"></a>Comentários

A função **FBadSortOrderSet** pode ser usada para preparar uma chamada para um método Sort, como o método [IMAPITable:: SortTable](imapitable-sorttable.md) . 
  

