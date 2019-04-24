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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317154"
---
# <a name="iostxsynchdrbeg"></a>IOSTX::SyncHdrBeg

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Inicia a sincronização de um cabeçalho de mensagem.
  
```cpp
HRESULT SyncHdrBeg( 
    ULONG cbeid, 
    LPENTRYID lpeid, 
    LPVOID *ppv 
);
```

## <a name="parameters"></a>Parâmetros

 _cbeid_
  
> no O número de bytes na ID de entrada da mensagem.
    
 _lpeid_
  
> no A identificação de entrada da mensagem.
    
 _PPV_
  
>  [in]/[out] ponteiro para a estrutura **[HDRSYNC](hdrsync.md)** do cabeçalho da mensagem. 
    
## <a name="remarks"></a>Comentários

Após o **IOSTX:: SyncHdrBeg**, o repositório local transita para o [estado de cabeçalho da mensagem de download](download-message-header-state.md). O Outlook é inicializado para o cliente a estrutura **HDRSYNC** com a representação atual do cabeçalho da mensagem no repositório e na pasta pai. O cliente deve baixar um item de mensagem completo (como *pmsgFull* no **HDRSYNC** ). Se isso tiver sido bem-sucedido, o cliente também define *parâmetroulflags* no **HDRSYNC** como **HSF_OK**. Após o **[IOSTX:: SyncHdrEnd](iostx-synchdrend.md)**, o Outlook verifica o resultado em **HDRSYNC** e usa as informações em **HDRSYNC** para atualizar o cabeçalho da mensagem local. 
  
## <a name="see-also"></a>Confira também



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::InitSync](iostx-initsync.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncEnd](iostx-syncend.md)
  
[IOSTX::SyncHdrEnd](iostx-synchdrend.md)
  
[IOSTX : IUnknown](iostxiunknown.md)


[Constantes de MAPI](mapi-constants.md)

