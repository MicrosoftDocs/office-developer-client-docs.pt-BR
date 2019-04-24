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
ms.openlocfilehash: fa1588d4a58824b57c132fc8e66a0abd6e9acd0a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357425"
---
# <a name="lpvalfindprop"></a>LpValFindProp

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Procura por uma propriedade especificada em um conjunto de propriedades.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |mapiutil. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente e provedores de serviços.  <br/> |
   
```cpp
LPSPropValue LpValFindProp(
  ULONG ulPropTag,
  ULONG cValues,
  LPSPropValue lpPropArray
);
```

## <a name="parameters"></a>Parâmetros

 _ulPropTag_
  
> no A marca da propriedade a ser pesquisada no conjunto de propriedades, indicado pelo parâmetro _lpPropArray_ . 
    
 _cValues_
  
> no Contagem de propriedades no conjunto de propriedades, indicada pelo parâmetro _lpPropArray_ . 
    
 _lpPropArray_
  
> no Matriz de estruturas **SPropValue** que define as propriedades a serem pesquisadas. 
    
## <a name="return-value"></a>Valor de retorno

A função **LpValFindProp** retorna uma estrutura **SPropValue** que define a propriedade que corresponde à marca de propriedade de entrada ou NULL se não houver correspondência. 
  
## <a name="remarks"></a>Comentários

A função **LpValFindProp** é idêntica a **PpropFindProp**.
  
## <a name="see-also"></a>Confira também



[PpropFindProp](ppropfindprop.md)
  
[SPropValue](spropvalue.md)

