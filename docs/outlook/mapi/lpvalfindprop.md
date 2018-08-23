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
ms.openlocfilehash: c4a201411e2232a3e5fdcd97dcbc9460f657b12a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578091"
---
# <a name="lpvalfindprop"></a>LpValFindProp

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
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

