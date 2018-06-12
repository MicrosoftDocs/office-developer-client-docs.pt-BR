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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 66542d2cc7600ecbcd8de9043b6b40559744c2ad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767587"
---
# <a name="iostxsyncend"></a>IOSTX::SyncEnd

  
  
**Aplica-se a**: Outlook 
  
Finaliza a sincronização no estado atual e sai desse estado.
  
```cpp
HRESULT SyncEnd();
```

## <a name="remarks"></a>Coment�rios

O cliente deve chamar **IOSTX::SyncEnd** para cada chamada ao [IOSTX::SyncBeg](iostx-syncbeg.md). A estrutura de dados correspondente contém informações para indicar se o cliente foi concluída com êxito o estado atual para que o Outlook pode limpar o seu estado interno.
  
## <a name="see-also"></a>Confira também



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::InitSync](iostx-initsync.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX::SyncHdrEnd](iostx-synchdrend.md)
  
[IOSTX: IUnknown](iostxiunknown.md)


[Constantes MAPI](mapi-constants.md)

