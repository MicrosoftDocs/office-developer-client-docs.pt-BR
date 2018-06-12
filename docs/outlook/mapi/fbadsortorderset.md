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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 0e200ea20c55cfd5729ce4c1f590de2d61ca73bc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766533"
---
# <a name="fbadsortorderset"></a>FBadSortOrderSet

  
  
**Aplica-se a**: Outlook 
  
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

## <a name="parameters"></a>Par�metros

 _lpsos_
  
> [in] Ponteiro para uma estrutura [SSortOrderSet](ssortorderset.md) que identifica a ordem de classificação, defina a ser validado. 
    
## <a name="return-value"></a>Valor retornado

VERDADEIRO 
  
> O conjunto de ordem de classificação especificado é inválido. 
    
FALSO 
  
> O conjunto de ordem de classificação especificada é válido.
    
## <a name="remarks"></a>Coment�rios

A função de **FBadSortOrderSet** pode ser usada para se preparar para uma chamada para um método de classificação, como o método [IMAPITable:: SortTable](imapitable-sorttable.md) . 
  

