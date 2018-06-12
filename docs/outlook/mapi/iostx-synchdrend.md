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
description: 'Modificado pela última vez: 03 de julho de 2012'
ms.openlocfilehash: ee68052f330bf3239cd12139ffbd77f5a180f6cc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767582"
---
# <a name="iostxsynchdrend"></a>IOSTX::SyncHdrEnd

 
  
**Aplica-se a**: Outlook 
  
Finaliza a sincronização para um cabeçalho de mensagem.
  
```cpp
HRESULT SyncHdrEnd( 
    LPMAPIPROGRESS pprog 
);
```

## <a name="parameters"></a>Par�metros

 _pprog_
  
> [in] Interface de **[IMAPIProgress](imapiprogressiunknown.md)** para sincronização de movido ou copiadas de mensagens. Consulte mapidefs.h para a definição de tipo de **LPMAPIPROGRESS**. 
    
## <a name="remarks"></a>Coment�rios

Após a **[IOSTX::SyncBeg](iostx-syncbeg.md)**, armazenamento local entra de [baixar o estado do cabeçalho da mensagem](download-message-header-state.md). O cliente baixa um item de mensagem completo (como *pmsgFull* **[HDRSYNC](hdrsync.md)** ). Se isso for bem-sucedida, o cliente também define *ulFlags* no **HDRSYNC** como **HSF_OK**. Após **IOSTX::SyncHdrEnd**, o Outlook verifica o resultado em **HDRSYNC** e usa *pprog* e as informações no **HDRSYNC** para atualizar o cabeçalho de mensagem local. 
  
Armazenamento local retorna ao estado em que se encontrava antes do anterior **[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)**. 
  
## <a name="see-also"></a>Confira também



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::InitSync](iostx-initsync.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncEnd](iostx-syncend.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX: IUnknown](iostxiunknown.md)


[Constantes MAPI](mapi-constants.md)

