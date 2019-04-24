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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 800f79179f999ba193d4177abb7341095b8b896d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321214"
---
# <a name="imapiofflinemgrunadvise"></a>IMAPIOfflineMgr::Unadvise

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Cancela os retornos de chamada para um objeto offline.
  
```cpp
HRESULT COfflineObj::Unadvise( 
      ULONG ulFlags, 
      ULONG ulAdviseToken 
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> no Sinalizadores para o retorno de chamada de cancelamento. Só há suporte para o valor MAPIOFFLINE_UNADVISE_DEFAULT.
    
 _ulAdviseToken_
  
> no Um token de aviso que identifica o registro de retorno de chamada que deve ser cancelado. 
    
## <a name="return-value"></a>Valor de retorno

S_OK
  
> A chamada foi bem-sucedida. Essa chamada deve retornar S_OK.
    
## <a name="remarks"></a>Comentários

Remove o registro do retorno de chamada que foi associado ao *ulAdviseToken* retornado de uma chamada anterior para **[IMAPIOfflineMgr:: Advise](imapiofflinemgr-advise.md)**. Faz com que o objeto **IMAPIOfflineMgr** Libere sua referência no objeto **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)** associado ao *ulAdviseToken* . 
  
## <a name="see-also"></a>Confira também



[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)


[Constantes de MAPI](mapi-constants.md)

