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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: a5c754a209a3e1bce8888851b88e116f92920eb4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767580"
---
# <a name="iostxsynchdrbeg"></a>IOSTX::SyncHdrBeg

  
  
**Aplica-se a**: Outlook 
  
Inicia a sincronização de um cabeçalho de mensagem.
  
```cpp
HRESULT SyncHdrBeg( 
    ULONG cbeid, 
    LPENTRYID lpeid, 
    LPVOID *ppv 
);
```

## <a name="parameters"></a>Par�metros

 _cbeid_
  
> [in] O número de bytes na identificação de entrada da mensagem.
    
 _lpeid_
  
> [in] A identificação de entrada da mensagem.
    
 _ppv_
  
>  [in] / [out] ponteiro para a estrutura **[HDRSYNC](hdrsync.md)** para o cabeçalho da mensagem. 
    
## <a name="remarks"></a>Coment�rios

Após a **IOSTX::SyncHdrBeg**, o local armazenar transições a [baixar o estado do cabeçalho da mensagem](download-message-header-state.md). Inicializa o Outlook para o cliente a estrutura **HDRSYNC** com a representação atual do cabeçalho da mensagem no repositório e a pasta pai. O cliente, em seguida, deve baixar um item de mensagem completo (como *pmsgFull* **HDRSYNC** ). Se isso foi bem-sucedida, o cliente também definirá *ulFlags* em **HDRSYNC** **HSF_OK**. Após a **[IOSTX::SyncHdrEnd](iostx-synchdrend.md)**, o Outlook verifica o resultado em **HDRSYNC** e usa as informações em **HDRSYNC** para atualizar o cabeçalho de mensagem local. 
  
## <a name="see-also"></a>Confira também



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::InitSync](iostx-initsync.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncEnd](iostx-syncend.md)
  
[IOSTX::SyncHdrEnd](iostx-synchdrend.md)
  
[IOSTX: IUnknown](iostxiunknown.md)


[Constantes MAPI](mapi-constants.md)

