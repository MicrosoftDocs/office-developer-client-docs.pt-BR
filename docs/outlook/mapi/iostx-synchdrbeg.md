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
ms.openlocfilehash: 2d05592d1fdcdcd53c8b7879f9cdcd432df1a3f7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579463"
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
  
> [in] O número de bytes na identificação de entrada da mensagem.
    
 _lpeid_
  
> [in] A identificação de entrada da mensagem.
    
 _ppv_
  
>  [in] / [out] ponteiro para a estrutura **[HDRSYNC](hdrsync.md)** para o cabeçalho da mensagem. 
    
## <a name="remarks"></a>Comentários

Após a **IOSTX::SyncHdrBeg**, o local armazenar transições a [baixar o estado do cabeçalho da mensagem](download-message-header-state.md). Inicializa o Outlook para o cliente a estrutura **HDRSYNC** com a representação atual do cabeçalho da mensagem no repositório e a pasta pai. O cliente, em seguida, deve baixar um item de mensagem completo (como *pmsgFull* **HDRSYNC** ). Se isso foi bem-sucedida, o cliente também definirá *ulFlags* em **HDRSYNC** **HSF_OK**. Após a **[IOSTX::SyncHdrEnd](iostx-synchdrend.md)**, o Outlook verifica o resultado em **HDRSYNC** e usa as informações em **HDRSYNC** para atualizar o cabeçalho de mensagem local. 
  
## <a name="see-also"></a>Confira também



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::InitSync](iostx-initsync.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncEnd](iostx-syncend.md)
  
[IOSTX::SyncHdrEnd](iostx-synchdrend.md)
  
[IOSTX : IUnknown](iostxiunknown.md)


[Constantes de MAPI](mapi-constants.md)

