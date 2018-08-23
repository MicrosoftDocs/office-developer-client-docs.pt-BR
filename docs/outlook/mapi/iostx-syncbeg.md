---
title: IOSTXSyncBeg
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.SyncBeg
api_type:
- COM
ms.assetid: 4a935df3-98c4-2742-206e-4e16eda7b9bc
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 37d37d6402b165ea57626fe4791cfb1a4bcf76cc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565113"
---
# <a name="iostxsyncbeg"></a>IOSTX::SyncBeg

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Prepara o armazenamento local para sincronização em um estado particular e recupera as informações necessárias para replicar.
  
```cpp
HRESULT SyncBeg( 
    UINT uiSync, 
    LPVOID *ppv 
);
```

## <a name="parameters"></a>Parâmetros

 _uiSync_
  
>  [in] O estado que entrará no armazenamento local. A seguir está uma lista de identificadores de estado: 
    
LR_SYNC_IDLE
  
> 
    
LR_SYNC
  
> 
    
LR_SYNC_UPLOAD_HIERARCHY
  
> 
    
LR_SYNC_UPLOAD_FOLDER
  
> 
    
LR_SYNC_CONTENTS
  
> 
    
LR_SYNC_UPLOAD_TABLE
  
> 
    
LR_SYNC_UPLOAD_MESSAGE
  
> 
    
LR_SYNC_UPLOAD_MESSAGE_READ
  
> 
    
LR_SYNC_UPLOAD_MESSAGE_DEL
  
> 
    
LR_SYNC_DOWNLOAD_HIERARCHY
  
> 
    
LR_SYNC_DOWNLOAD_TABLE
  
> 
    
 _ppv_
  
>  [in] / [ponteiro para a estrutura de dados correspondente ao estado insiram out]. 
    
[DNHIER](dnhier.md)
  
> 
    
[DNTBL](dntbl.md)
  
> 
    
[DNTBL](dntbl.md)
  
> 
    
[SYNC](sync.md)
  
> 
    
[SYNCCONT](synccont.md)
  
> 
    
[UPDEL](updel.md)
  
> 
    
[UPDELE](updele.md)
  
> 
    
[UPFLD](upfld.md)
  
> 
    
[UPHIER](uphier.md)
  
> 
    
[UPMOV](upmov.md)
  
> 
    
[UPMSG](upmsg.md)
  
> 
    
[UPREAD](upread.md)
  
> 
    
[UPREADE](upreade.md)
  
> 
    
[UPTBL](uptbl.md)
  
> 
    
[UPTBLE](uptble.md)
  
> 
    
## <a name="remarks"></a>Comentários

O cliente chama **[IOSTX::SetSyncResult](iostx-setsyncresult.md)** para definir o resultado da sincronização e, em seguida, chama **[IOSTX::SyncEnd](iostx-syncend.md)** para encerrar a esse estado. O cliente deve chamar **[IOSTX::SyncEnd](iostx-syncend.md)** para cada chamada ao **IOSTX::SyncBeg** para determinar se o estado foi replicado com êxito. Depois que tiver sido determinado, o Outlook pode começar a limpar o seu estado interno. 
  
A maioria dessas estruturas contém [out] / [in] informações, permitindo que o Outlook passar informações para o cliente e o cliente para passar informações para o Outlook. Quando o cliente chama **IOSTX::SyncBeg**, Outlook aloca a estrutura de dados para um determinado estado e inicializa com informações para esse estado. Essas são as informações de [out]. Enquanto estiver em um estado, o cliente atualiza a estrutura de dados correspondente para esse estado. Este é o [in] informações. 
  
## <a name="see-also"></a>Confira também



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::InitSync](iostx-initsync.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncEnd](iostx-syncend.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX::SyncHdrEnd](iostx-synchdrend.md)
  
[IOSTX : IUnknown](iostxiunknown.md)


[Constantes MAPI](mapi-constants.md)

