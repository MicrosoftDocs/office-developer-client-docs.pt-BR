---
title: IOSTXSyncEnd
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.SyncEnd
api_type:
- COM
ms.assetid: da9de705-bdab-6cb8-35ea-61f03cdc4ff5
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: fd5b2ed23eba30cbe861a20c4fd100cb8ea1aeb0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568837"
---
# <a name="iostxsyncend"></a>IOSTX::SyncEnd

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Finaliza a sincronização no estado atual e sai desse estado.
  
```cpp
HRESULT SyncEnd();
```

## <a name="remarks"></a>Comentários

O cliente deve chamar **IOSTX::SyncEnd** para cada chamada ao [IOSTX::SyncBeg](iostx-syncbeg.md). A estrutura de dados correspondente contém informações para indicar se o cliente foi concluída com êxito o estado atual para que o Outlook pode limpar o seu estado interno.
  
## <a name="see-also"></a>Confira também



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::InitSync](iostx-initsync.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX::SyncHdrEnd](iostx-synchdrend.md)
  
[IOSTX : IUnknown](iostxiunknown.md)


[Constantes de MAPI](mapi-constants.md)

