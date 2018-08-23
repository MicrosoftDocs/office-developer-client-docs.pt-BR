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
ms.openlocfilehash: 113628ef5487bc66a07d1367c938ed178a8e32ec
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582907"
---
# <a name="fbadentrylist"></a>FBadEntryList

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Valida uma lista dos identificadores de entrada MAPI. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapival.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços  <br/> |
   
```cpp
BOOL FBadEntryList(
  LPENTRYLIST lpEntryList
);
```

## <a name="parameters"></a>Parâmetros

 _lpEntryList_
  
> [in] Ponteiro para uma estrutura [ENTRYLIST](entrylist.md) que contém uma matriz de identificadores de entrada a ser validado. 
    
## <a name="return-value"></a>Valor retornado

VERDADEIRO 
  
> Um ou mais dos identificadores de entrada listada são inválidos. 
    
FALSO 
  
> Todos os identificadores de entrada listada são válidos.
    
## <a name="remarks"></a>Comentários

A função **FBadEntryList** determina se a lista de identificadores de entrada foi gerada corretamente. Um exemplo de um identificador inválido é aquele para o qual memória foi alocada incorretamente ou um identificador de um tamanho incorreto. 
  

