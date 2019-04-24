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
ms.openlocfilehash: 364914df1c5897241dfeb89cce2cc3c62018ce24
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332148"
---
# <a name="iostxsyncend"></a>IOSTX::SyncEnd

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Termina a sincronização no estado atual e sai desse Estado.
  
```cpp
HRESULT SyncEnd();
```

## <a name="remarks"></a>Comentários

O cliente deve chamar **IOSTX:: SyncEnd** para cada chamada para [IOSTX:: SyncBeg](iostx-syncbeg.md). A estrutura de dados correspondente contém informações para indicar se o cliente concluiu com êxito o estado atual para que o Outlook possa limpar seu estado interno.
  
## <a name="see-also"></a>Confira também



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::InitSync](iostx-initsync.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX::SyncHdrEnd](iostx-synchdrend.md)
  
[IOSTX : IUnknown](iostxiunknown.md)


[Constantes de MAPI](mapi-constants.md)

