---
title: FBadEntryList
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FBadEntryList
api_type:
- HeaderDef
ms.assetid: 270c47c3-ae68-4995-b304-27f861b350d6
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 21ed5a23b96dabdd594547109ecb1e6c048a4844
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427770"
---
# <a name="fbadentrylist"></a>FBadEntryList

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Valida uma lista de identificadores de entrada MAPI. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapival.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Provedores de serviços  <br/> |
   
```cpp
BOOL FBadEntryList(
  LPENTRYLIST lpEntryList
);
```

## <a name="parameters"></a>Parâmetros

 _lpEntryList_
  
> [in] Ponteiro para uma [estrutura ENTRYLIST](entrylist.md) que contém uma matriz de identificadores de entrada a serem validados. 
    
## <a name="return-value"></a>Valor de retorno

TRUE 
  
> Um ou mais dos identificadores de entrada listados são inválidos. 
    
FALSE 
  
> Todos os identificadores de entrada listados são válidos.
    
## <a name="remarks"></a>Comentários

A **função FBadEntryList** determina se a lista de identificadores de entrada foi gerada corretamente. Um exemplo de um identificador inválido é aquele para o qual a memória foi alocada incorretamente ou um identificador de um tamanho incorreto. 
  

