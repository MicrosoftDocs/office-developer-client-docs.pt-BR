---
title: IMAPITableFreeBookmark
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.FreeBookmark
api_type:
- COM
ms.assetid: 797833f7-8295-41bc-8980-977e5f5e05e8
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 36d1518764985c4783d967e263ca5c05d63f935f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588479"
---
# <a name="imapitablefreebookmark"></a>IMAPITable::FreeBookmark

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Libera a memória associada a um indicador.
  
```cpp
HRESULT FreeBookmark(
BOOKMARK bkPosition
);
```

## <a name="parameters"></a>Parâmetros

 _bkPosition_
  
> [in] O indicador para ser liberada, criados chamando o método [IMAPITable::CreateBookmark](imapitable-createbookmark.md) . 
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> O indicador foi liberado com êxito.
    
MAPI_E_INVALID_BOOKMARK 
  
> O indicador especificado não existe.
    
## <a name="remarks"></a>Comentários

O método **IMAPITable::FreeBookmark** libera um indicador que não é mais necessária. O indicador não é mais válido após essa chamada. Sempre que uma tabela é liberada da memória, todos seus indicadores associadas também sejam liberados. 
  
## <a name="notes-to-implementers"></a>Notas para implementadores

Se o chamador passa uma dos três indicadores predefinidos no parâmetro _bkPosition_ , ignore a solicitação e retornar S_OK. 
  
## <a name="see-also"></a>Confira também



[IMAPITable::CreateBookmark](imapitable-createbookmark.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

