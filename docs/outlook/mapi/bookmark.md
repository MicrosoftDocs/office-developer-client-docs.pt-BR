---
title: Indicador
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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 8f5f3bc454e18b1dbab434fc1b7cc094b0d6a360
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766398"
---
# <a name="bookmark"></a>Indicador

  
  
**Aplica-se a**: Outlook 
  
Define os dados de indicadores para memorizar uma posição em uma tabela. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
|Métodos relacionados:  <br/> |[IMAPITable::CreateBookmark](imapitable-createbookmark.md) [IMAPITable::FreeBookmark](imapitable-freebookmark.md) <br/> |
   
```cpp
typedef ULONG_PTR BOOKMARK;
```

## <a name="remarks"></a>Coment�rios

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
  
[IMAPITable:: FindRow](imapitable-findrow.md)
  
[IMAPITable::FreeBookmark](imapitable-freebookmark.md)
  
[IMAPITable::SeekRow](imapitable-seekrow.md)


[Tipos de dados MAPI](mapi-data-types.md)

