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
ms.openlocfilehash: b0260ffe5dc4806cb627fd71c78866bf96796455
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434715"
---
# <a name="fbadcolumnset"></a>FBadColumnSet

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Testa a validade de uma coluna de tabela definida para uso por um provedor de serviços em uma chamada subsequente para o método [IMAPITable::SetColumns.](imapitable-setcolumns.md) 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapival.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Provedores de serviços  <br/> |
   
```cpp
ULONG FBadColumnSet(
  LPSPropTagArray lpptaCols
);
```

## <a name="parameters"></a>Parâmetros

 _lpptaCols_
  
> [in] Ponteiro para uma [estrutura SPropTagArray](sproptagarray.md) que contém uma matriz de marcas de propriedade definindo as colunas da tabela a validar. 
    
## <a name="return-value"></a>Valor de retorno

TRUE 
  
> O conjunto de colunas especificado é inválido. 
    
FALSE 
  
> O conjunto de colunas especificado é válido.
    
## <a name="remarks"></a>Comentários

A **função FBadColumnSet** trata colunas do tipo PT_ERROR como inválidas e colunas do tipo PT_NULL como válidas. 
  

