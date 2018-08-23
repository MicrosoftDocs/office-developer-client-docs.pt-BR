---
title: BOOKMARK
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.BOOKMARK
api_type:
- COM
ms.assetid: 678bdc52-3404-48b2-9154-64ce2a941555
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: be41a9916b6b231d5715cf18fe2b0d804434f2ea
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594478"
---
# <a name="bookmark"></a>BOOKMARK

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Define os dados de indicadores para memorizar uma posição em uma tabela. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
|Métodos relacionados:  <br/> |[IMAPITable::CreateBookmark](imapitable-createbookmark.md) [IMAPITable::FreeBookmark](imapitable-freebookmark.md) <br/> |
   
```cpp
typedef ULONG_PTR BOOKMARK;
```

## <a name="remarks"></a>Comentários

MAPI define três indicadores, listadas a seguir:
  
BOOKMARK_BEGINNING 
  
> Lembra-se a posição inicial da tabela. 
    
BOOKMARK_CURRENT 
  
> Lembra-se a posição atual da tabela.
    
BOOKMARK_END 
  
> Lembra-se a posição final da tabela.
    
Os clientes podem criar outros indicadores lembrando outras posições de tabela. Indicadores são válidas somente quando a tabela é aberta. Clientes devem liberar todos os indicadores que eles criaram antes de fechar a tabela associada. 
  
## <a name="see-also"></a>Confira também



[IMAPITable::CreateBookmark](imapitable-createbookmark.md)
  
[IMAPITable::ExpandRow](imapitable-findrow.md)
  
[IMAPITable::FreeBookmark](imapitable-freebookmark.md)
  
[IMAPITable::SeekRow](imapitable-seekrow.md)


[Tipos de dados MAPI](mapi-data-types.md)

