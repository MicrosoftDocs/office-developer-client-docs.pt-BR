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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: a1ad209ff127a34d7da5ca8dbe1f4a6656d32876
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409451"
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
  
> [in] O indicador a ser liberado, criado chamando o [método IMAPITable::CreateBookmark.](imapitable-createbookmark.md) 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O indicador foi liberado com êxito.
    
MAPI_E_INVALID_BOOKMARK 
  
> O indicador especificado não existe.
    
## <a name="remarks"></a>Comentários

O **método IMAPITable::FreeBookmark** libera um indicador que não é mais necessário. O indicador não é mais válido após essa chamada. Sempre que uma tabela é liberada da memória, todos os seus indicadores associados também são liberados. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Se o chamador passar um dos três indicadores predefinidos no parâmetro  _bkPosition,_ ignore a solicitação e retorne S_OK. 
  
## <a name="see-also"></a>Confira também



[IMAPITable::CreateBookmark](imapitable-createbookmark.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

