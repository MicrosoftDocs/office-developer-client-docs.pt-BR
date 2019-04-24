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
ms.openlocfilehash: 069cb41ceac70a2eaaa08440e43745605890f071
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318036"
---
# <a name="bookmark"></a>BOOKMARK

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Define dados de indicadores para memorizar uma posição em uma tabela. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs. h  <br/> |
|Métodos relacionados:  <br/> |[IMAPITable:: CreateBookmark](imapitable-createbookmark.md) [IMAPITable:: FreeBookmark](imapitable-freebookmark.md) <br/> |
   
```cpp
typedef ULONG_PTR BOOKMARK;
```

## <a name="remarks"></a>Comentários

MAPI define três indicadores, listados da seguinte maneira:
  
BOOKMARK_BEGINNING 
  
> Memoriza a posição inicial da tabela. 
    
BOOKMARK_CURRENT 
  
> Memoriza a posição atual da tabela.
    
BOOKMARK_END 
  
> Memoriza a posição final da tabela.
    
Os clientes podem criar outros indicadores para lembrar outras posições da tabela. Os indicadores são válidos somente quando a tabela está aberta. Os clientes devem liberar todos os indicadores criados antes de fechar a tabela associada. 
  
## <a name="see-also"></a>Confira também



[IMAPITable::CreateBookmark](imapitable-createbookmark.md)
  
[IMAPITable::ExpandRow](imapitable-findrow.md)
  
[IMAPITable::FreeBookmark](imapitable-freebookmark.md)
  
[IMAPITable::SeekRow](imapitable-seekrow.md)


[Tipos de dados MAPI](mapi-data-types.md)

