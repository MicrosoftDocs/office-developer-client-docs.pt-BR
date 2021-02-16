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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404852"
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
  
> [in] Sinalizadores para cancelar retorno de chamada. Somente o valor MAPIOFFLINE_UNADVISE_DEFAULT é suportado.
    
 _ulAdviseToken_
  
> [in] Um token de consultoria que identifica o registro de retorno de chamada que deve ser cancelado. 
    
## <a name="return-value"></a>Valor de retorno

S_OK
  
> A chamada foi bem-sucedida. Essa chamada deve retornar S_OK.
    
## <a name="remarks"></a>Comentários

Remove o registro do retorno de chamada associado ao  *ulAdviseToken*  retornado de uma chamada anterior para **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**. Faz com que o objeto **IMAPIOfflineMgr** libere sua referência no objeto **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)** associado  *a ulAdviseToken*  . 
  
## <a name="see-also"></a>Confira também



[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)


[Constantes de MAPI](mapi-constants.md)

