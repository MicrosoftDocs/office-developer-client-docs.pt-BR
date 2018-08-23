---
title: FBadColumnSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FBadColumnSet
api_type:
- HeaderDef
ms.assetid: 15be5a8c-4299-4434-b521-c901215b9dda
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 4e5f19258fb7716e741928f02a0a87f3939c74e0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575095"
---
# <a name="fbadcolumnset"></a>FBadColumnSet

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os testes a validade de uma coluna de tabela definida para usam por um provedor de serviço em uma chamada subsequente ao método [IMAPITable::SetColumns](imapitable-setcolumns.md) . 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapival.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços  <br/> |
   
```cpp
ULONG FBadColumnSet(
  LPSPropTagArray lpptaCols
);
```

## <a name="parameters"></a>Parâmetros

 _lpptaCols_
  
> [in] Ponteiro para uma estrutura [SPropTagArray](sproptagarray.md) que contém uma matriz de marcas de propriedade definindo as colunas da tabela para validar. 
    
## <a name="return-value"></a>Valor retornado

VERDADEIRO 
  
> O conjunto de coluna especificada é inválido. 
    
FALSO 
  
> O conjunto de coluna especificada é válido.
    
## <a name="remarks"></a>Comentários

A função **FBadColumnSet** trata as colunas do tipo PT_ERROR como inválida e colunas do tipo PT_NULL como válido. 
  

