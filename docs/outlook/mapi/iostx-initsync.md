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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: b9086383b45d40d5839284ac785d72438be60e00
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317189"
---
# <a name="iostxinitsync"></a>IOSTX::InitSync

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Informa o repositório de mensagens local que a sincronização está prestes a começar.
  
```cpp
HRESULT InitSync( 
    ULONG ulFlags 
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> no Sinalizadores para determinar o comportamento apropriado durante a sincronização. O Outlook usa esses sinalizadores em cada Estado da máquina de estado de replicação para determinar as informações que ele deve fornecer para o cliente. Por exemplo, se o cliente passar **SYNC_ONLY_ASSOCIATED**, o Outlook retornará apenas informações relacionadas aos itens associados (ou ocultos). 
    
## <a name="see-also"></a>Confira também



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncEnd](iostx-syncend.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX::SyncHdrEnd](iostx-synchdrend.md)
  
[IOSTX : IUnknown](iostxiunknown.md)


[Constantes de MAPI](mapi-constants.md)

