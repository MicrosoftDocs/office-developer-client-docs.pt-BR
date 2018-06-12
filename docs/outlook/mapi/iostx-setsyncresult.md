---
title: IOSTXSetSyncResult
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.SetSyncResult
api_type:
- COM
ms.assetid: 7f083ee0-bf36-0059-1589-66e454fe0098
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 74a4e299da6c0637c3da70c329569266d43dbd9a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767578"
---
# <a name="iostxsetsyncresult"></a>IOSTX::SetSyncResult

  
  
**Aplica-se a**: Outlook 
  
Define o resultado da sincronização.
  
```cpp
HRESULT SetSyncResult( 
    HRESULT hrSync 
);
```

## <a name="parameters"></a>Par�metros

 _hrSync_
  
>  [in] O resultado da sincronização. 
    
## <a name="remarks"></a>Coment�rios

Chame **IOSTX::SetSyncResult** antes de chamar **IOSTX::SyncEnd** para informar o armazenamento local do resultado da sincronização. 
  
## <a name="see-also"></a>Confira também



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::InitSync](iostx-initsync.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncEnd](iostx-syncend.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX::SyncHdrEnd](iostx-synchdrend.md)


[Constantes MAPI](mapi-constants.md)

