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
description: 'Última modificação: 03 de julho de 2012'
ms.openlocfilehash: 864c2d2dfd17c285b0d8a401d59ce5b7d0463864
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332183"
---
# <a name="iostxsynchdrend"></a>IOSTX::SyncHdrEnd

 
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Termina a sincronização de um cabeçalho de mensagem.
  
```cpp
HRESULT SyncHdrEnd( 
    LPMAPIPROGRESS pprog 
);
```

## <a name="parameters"></a>Parâmetros

 _pprog_
  
> no **[Método imapiprogress](imapiprogressiunknown.md)** interface para sincronização de mensagens movidas ou copiadas. Consulte mapidefs. h para a definição de tipo de **LPMAPIPROGRESS**. 
    
## <a name="remarks"></a>Comentários

Após o **[IOSTX:: SyncBeg](iostx-syncbeg.md)**, o repositório local entra no [status do cabeçalho da mensagem de download](download-message-header-state.md). O cliente baixa um item de mensagem completo (como *pmsgFull* no **[HDRSYNC](hdrsync.md)** ). Se isso for bem-sucedido, o cliente também definirá *parâmetroulflags* no **HDRSYNC** como **HSF_OK**. Após o **IOSTX:: SyncHdrEnd**, o Outlook verifica o resultado em **HDRSYNC** e usa *Pprog* e as informações em **HDRSYNC** para atualizar o cabeçalho da mensagem local. 
  
O repositório local retorna ao estado em que estava antes da IOSTX anterior **[:: SyncHdrBeg](iostx-synchdrbeg.md)**. 
  
## <a name="see-also"></a>Confira também



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::InitSync](iostx-initsync.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncEnd](iostx-syncend.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX : IUnknown](iostxiunknown.md)


[Constantes de MAPI](mapi-constants.md)

