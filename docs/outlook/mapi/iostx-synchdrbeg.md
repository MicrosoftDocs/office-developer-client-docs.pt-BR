---
title: IOSTXSyncHdrBeg
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.SyncHdrBeg
api_type:
- COM
ms.assetid: 7f8ca7cf-ac0b-9b77-c1dd-9f1d0871d603
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 49ef9862d5156a1bed242652df32baab9a0123fc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405090"
---
# <a name="iostxsynchdrbeg"></a>IOSTX::SyncHdrBeg

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Inicia a sincronização para um header de mensagem.
  
```cpp
HRESULT SyncHdrBeg( 
    ULONG cbeid, 
    LPENTRYID lpeid, 
    LPVOID *ppv 
);
```

## <a name="parameters"></a>Parâmetros

 _cbeid_
  
> [in] O número de bytes na ID de entrada da mensagem.
    
 _lpeid_
  
> [in] A ID de entrada da mensagem.
    
 _ppv_
  
>  [in]/[out] Ponteiro para a **[estrutura HDRSYNC](hdrsync.md)** para o header da mensagem. 
    
## <a name="remarks"></a>Comentários

Upon **IOSTX::SyncHdrBeg**, the local store transitions to the [download message header state](download-message-header-state.md). Outlook initializes for the client the **HDRSYNC** structure with the current representation of the message header in the store and the parent folder. O cliente deve baixar um item de mensagem completo (como  *pmsgFull*  em **HDRSYNC** ). Se isso foi bem-sucedido, o cliente também define  *ulFlags* **em HDRSYNC** **como HSF_OK**. Após **[IOSTX::SyncHdrEnd](iostx-synchdrend.md)**, o Outlook verifica o resultado em **HDRSYNC** e usa as informações em **HDRSYNC** para atualizar o header de mensagem local. 
  
## <a name="see-also"></a>Confira também



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::InitSync](iostx-initsync.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncEnd](iostx-syncend.md)
  
[IOSTX::SyncHdrEnd](iostx-synchdrend.md)
  
[IOSTX : IUnknown](iostxiunknown.md)


[Constantes de MAPI](mapi-constants.md)

