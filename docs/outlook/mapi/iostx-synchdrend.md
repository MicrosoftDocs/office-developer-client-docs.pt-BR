---
title: IOSTXSyncHdrEnd
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.SyncHdrEnd
api_type:
- COM
ms.assetid: a0beb6eb-7978-c64e-dba1-89f0caf2090e
description: 'Last modified: July 03, 2012'
ms.openlocfilehash: 864c2d2dfd17c285b0d8a401d59ce5b7d0463864
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432769"
---
# <a name="iostxsynchdrend"></a>IOSTX::SyncHdrEnd

 
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Encerra a sincronização para um header de mensagem.
  
```cpp
HRESULT SyncHdrEnd( 
    LPMAPIPROGRESS pprog 
);
```

## <a name="parameters"></a>Parâmetros

 _pp que_
  
> [in] **[Interface IMAPIProgress](imapiprogressiunknown.md)** para sincronização de mensagens movidas ou copiadas. Consulte mapidefs.h para a definição de tipo de **LPMAPIPROGRESS**. 
    
## <a name="remarks"></a>Comentários

Após **[IOSTX::SyncBeg](iostx-syncbeg.md)**, o armazenamento local entra no estado do [header da](download-message-header-state.md)mensagem de download. O cliente baixa um item de mensagem completo (como  *pmsgFull*  em **[HDRSYNC](hdrsync.md)** ). Se isso for bem-sucedido, o cliente também define  *ulFlags*  em **HDRSYNC** **como HSF_OK**. Depois **de IOSTX::SyncHdrEnd**, o Outlook verifica o resultado em **HDRSYNC** e usa  *pp as informações*  em **HDRSYNC** para atualizar o header de mensagem local. 
  
O armazenamento local retorna ao estado em que estava antes do **[IOSTX anterior::SyncHdrBeg](iostx-synchdrbeg.md)**. 
  
## <a name="see-also"></a>Confira também



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::InitSync](iostx-initsync.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncEnd](iostx-syncend.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX : IUnknown](iostxiunknown.md)


[Constantes de MAPI](mapi-constants.md)

