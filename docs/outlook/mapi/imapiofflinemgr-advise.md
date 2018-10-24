---
title: IMAPIOfflineMgrAdvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOfflineMgr.Advise
api_type:
- COM
ms.assetid: 784b6218-548d-817a-caaa-cf9be6bc3d2f
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: e0c8c4c6251581506c7bdd78c009bb12e8291c81
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586932"
---
# <a name="imapiofflinemgradvise"></a>IMAPIOfflineMgr::Advise

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Registra um cliente para receber retornos de chamada em um objeto offline.
  
```cpp
HRESULT COfflineObj::Advise( 
      ULONG ulFlags, 
      MAPIOFFLINE_ADVISEINFO* pAdviseInfo, 
      ULONG* pulAdviseToken 
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
>  [in] Sinalizadores que modificam o comportamento. Somente o valor MAPIOFFLINE_ADVISE_DEFAULT é suportado. 
    
 _pAdviseInfo_
  
> [in] Informações sobre o tipo de retorno de chamada, quando receber um retorno de chamada, uma interface de retorno de chamada para o chamador e outros detalhes. Ele também contém um token de cliente que o Outlook usa no envio retornos de chamada de notificação subsequentes para o chamador do cliente.
    
 _pulAdviseToken_
  
> [out] Um token de advise retornado para o chamador do cliente para subsequentemente cancelamento de retorno de chamada para o objeto.
    
## <a name="return-value"></a>Valor de retorno

S_OK
  
> A chamada foi bem-sucedida.
    
E_INVALIDARG
  
> Um parâmetro inválido foi especificado.
    
E_NOINTERFACE
  
> A interface de retorno de chamada especificada em *pAdviseInfo* não é válida. 
    
## <a name="remarks"></a>Comentários

Ao abrir um objeto offline usando **[HrOpenOfflineObj](hropenofflineobj.md)**, um cliente obtém um objeto offline que suporta **IMAPIOfflineMgr**. O cliente pode verificar os tipos de retornos de chamada suportados pelo objeto usando **[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)**. O cliente pode determinar o tipo e outros detalhes sobre o retorno de chamada, ele quiser e depois ligue **IMAPIOfflineMgr::Advise** para registrar-se para receber esses retornos de chamada sobre o objeto. 
  
## <a name="see-also"></a>Confira também



[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)
  
[IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md)


[Constantes de MAPI](mapi-constants.md)
  
[HrOpenOfflineObj](hropenofflineobj.md)

