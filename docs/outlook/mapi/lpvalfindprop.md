---
title: LpValFindProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 67461a38-bb60-467b-901b-39c645e764f7
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: d7601eb50818fa6f39384a6b024215fc4917e83a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767773"
---
# <a name="lpvalfindprop"></a>LpValFindProp

  
  
**Aplica-se a**: Outlook 
  
Procura uma propriedade especificada em uma propriedade definida.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |mapiutil.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços e aplicativos cliente.  <br/> |
   
```cpp
LPSPropValue LpValFindProp(
  ULONG ulPropTag,
  ULONG cValues,
  LPSPropValue lpPropArray
);
```

## <a name="parameters"></a>Parâmetros

 _ulPropTag_
  
> [in] Marca para a propriedade pesquisar no conjunto de propriedades, indicado pelo parâmetro _lpPropArray_ . 
    
 _cValues_
  
> [in] Contagem de propriedades no conjunto de propriedades, indicado pelo parâmetro _lpPropArray_ . 
    
 _lpPropArray_
  
> [in] Matriz de estruturas de **SPropValue** que define as propriedades a serem pesquisados. 
    
## <a name="return-value"></a>Valor retornado

A função **LpValFindProp** retorna uma estrutura **SPropValue** que define a propriedade que corresponda a propriedade input marca ou NULL se não houver nenhuma correspondência. 
  
## <a name="remarks"></a>Comentários

A função **LpValFindProp** é idêntica ao **PpropFindProp**.
  
## <a name="see-also"></a>Confira também



[PpropFindProp](ppropfindprop.md)
  
[SPropValue](spropvalue.md)

