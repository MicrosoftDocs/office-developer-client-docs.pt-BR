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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: ae4497295328155780fc5208d1699169698e02d8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317168"
---
# <a name="iostxsyncbeg"></a>IOSTX::SyncBeg

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Prepara o repositório local para sincronização em um determinado Estado e recupera as informações necessárias para a replicação.
  
```cpp
HRESULT SyncBeg( 
    UINT uiSync, 
    LPVOID *ppv 
);
```

## <a name="parameters"></a>Parâmetros

 _uiSync_
  
>  no O estado que o repositório local inserirá. Veja a seguir uma lista de identificadores de Estado: 
    
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
    
 _PPV_
  
>  [in]/[out] ponteiro para a estrutura de dados que corresponde ao estado a ser inserido. 
    
[DNHIER](dnhier.md)
  
> 
    
[DNTBL](dntbl.md)
  
> 
    
[DNTBL](dntbl.md)
  
> 
    
[SINCRONIZAÇÃO](sync.md)
  
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

O cliente chama **[IOSTX:: SetSyncResult](iostx-setsyncresult.md)** para definir o resultado da sincronização e, em seguida, chama **[IOSTX:: SyncEnd](iostx-syncend.md)** para terminar esse estado. O cliente deve chamar **[IOSTX:: SyncEnd](iostx-syncend.md)** para cada chamada para **IOSTX:: SyncBeg** a fim de determinar se o estado foi replicado com êxito. Depois de determinado, o Outlook pode começar a limpar seu estado interno. 
  
A maioria dessas estruturas contém informações de [out]/[in], permitindo que o Outlook passe informações para o cliente e o cliente passe informações para o Outlook. Quando o cliente chama **IOSTX:: SyncBeg**, o Outlook aloca a estrutura de dados para um determinado Estado e a inicializa com informações para esse estado. Estas são as informações de [out]. Enquanto estiver em um estado, o cliente atualiza a estrutura de dados correspondente para esse estado. Estas são as informações do [in]. 
  
## <a name="see-also"></a>Confira também



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::InitSync](iostx-initsync.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncEnd](iostx-syncend.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX::SyncHdrEnd](iostx-synchdrend.md)
  
[IOSTX : IUnknown](iostxiunknown.md)


[Constantes de MAPI](mapi-constants.md)

