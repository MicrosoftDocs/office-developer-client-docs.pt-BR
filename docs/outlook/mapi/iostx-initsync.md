---
title: IOSTXInitSync
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.InitSync
api_type:
- COM
ms.assetid: e22244a2-ac5f-910a-501f-4483ea0667c2
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 07305f712fd925b206ce18a32f8f5a24f199ccbf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767576"
---
# <a name="iostxinitsync"></a>IOSTX::InitSync

  
  
**Aplica-se a**: Outlook 
  
Informa o armazenamento de mensagens local que sincronização está prestes a iniciar.
  
```cpp
HRESULT InitSync( 
    ULONG ulFlags 
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> [in] Sinalizadores para determinar o comportamento apropriado durante a sincronização. O Outlook usa esses sinalizadores em cada estado da máquina de estado de replicação para determinar as informações que deverão ser fornecidas para o cliente. Por exemplo, se o cliente passa **SYNC_ONLY_ASSOCIATED**, Outlook retornará somente informações relacionadas a itens associados (ou ocultos). 
    
## <a name="see-also"></a>Confira também



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncEnd](iostx-syncend.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX::SyncHdrEnd](iostx-synchdrend.md)
  
[IOSTX : IUnknown](iostxiunknown.md)


[Constantes MAPI](mapi-constants.md)

