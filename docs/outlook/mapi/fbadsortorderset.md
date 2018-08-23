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
ms.openlocfilehash: 3b3f88495cafbd6ea764ca8901ac67c23749aebe
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578574"
---
# <a name="fbadsortorderset"></a>FBadSortOrderSet

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Valida uma ordem de classificação definida verificando sua alocação de memória. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapival.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços  <br/> |
   
```cpp
ULONG FBadSortOrderSet(
  LPSSortOrderSet lpsos
);
```

## <a name="parameters"></a>Parâmetros

 _lpsos_
  
> [in] Ponteiro para uma estrutura [SSortOrderSet](ssortorderset.md) que identifica a ordem de classificação, defina a ser validado. 
    
## <a name="return-value"></a>Valor retornado

VERDADEIRO 
  
> O conjunto de ordem de classificação especificado é inválido. 
    
FALSO 
  
> O conjunto de ordem de classificação especificada é válido.
    
## <a name="remarks"></a>Comentários

A função de **FBadSortOrderSet** pode ser usada para se preparar para uma chamada para um método de classificação, como o método [IMAPITable:: SortTable](imapitable-sorttable.md) . 
  

