---
title: IMAPIOfflineMgrUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOfflineMgr.Unadvise
api_type:
- COM
ms.assetid: 250b9137-facb-81a2-41b1-96a57366c04e
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 35dfc7af9852609dcfcc3fcb9d65ec2e4afa9632
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579519"
---
# <a name="imapiofflinemgrunadvise"></a>IMAPIOfflineMgr::Unadvise

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Cancela retornos de chamada para um objeto offline.
  
```cpp
HRESULT COfflineObj::Unadvise( 
      ULONG ulFlags, 
      ULONG ulAdviseToken 
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> [in] Sinalizadores de cancelamento de retorno de chamada. Somente o valor MAPIOFFLINE_UNADVISE_DEFAULT é suportado.
    
 _ulAdviseToken_
  
> [in] Um token de advise que identifica o registro de retorno de chamada que deve ser cancelado. 
    
## <a name="return-value"></a>Valor retornado

S_OK
  
> A chamada foi bem-sucedida. Essa chamada deve retornar S_OK.
    
## <a name="remarks"></a>Comentários

Remove o registro para o retorno de chamada que estava associado com *ulAdviseToken* retornados de uma chamada anterior ao **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**. Faz com que o objeto **IMAPIOfflineMgr** liberar a sua referência no objeto **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)** associado *ulAdviseToken* . 
  
## <a name="see-also"></a>Confira também



[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)


[Constantes MAPI](mapi-constants.md)

