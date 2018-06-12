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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 5d1654908c50c348a27e1281168756100b7a88a2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766535"
---
# <a name="fbadcolumnset"></a>FBadColumnSet

  
  
**Aplica-se a**: Outlook 
  
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

## <a name="parameters"></a>Par�metros

 _lpptaCols_
  
> [in] Ponteiro para uma estrutura [SPropTagArray](sproptagarray.md) que contém uma matriz de marcas de propriedade definindo as colunas da tabela para validar. 
    
## <a name="return-value"></a>Valor retornado

VERDADEIRO 
  
> O conjunto de coluna especificada é inválido. 
    
FALSO 
  
> O conjunto de coluna especificada é válido.
    
## <a name="remarks"></a>Coment�rios

A função **FBadColumnSet** trata as colunas do tipo PT_ERROR como inválida e colunas do tipo PT_NULL como válido. 
  

