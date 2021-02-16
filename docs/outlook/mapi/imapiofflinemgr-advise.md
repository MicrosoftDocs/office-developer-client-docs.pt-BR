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
ms.openlocfilehash: 3ca7fdc39da8d3ee8ecf6f0f253284df10a392e5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426916"
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
  
> [in] Informações sobre o tipo de retorno de chamada, quando receber um retorno de chamada, uma interface de retorno de chamada para o chamador e outros detalhes. Ele também contém um token de cliente que o Outlook usa no envio de retornos de chamada de notificação subsequentes para o chamador do cliente.
    
 _ashAdviseToken_
  
> [out] Um token de consultoria retornado ao chamador do cliente para cancelar subsequentemente o retorno de chamada do objeto.
    
## <a name="return-value"></a>Valor de retorno

S_OK
  
> A chamada foi bem-sucedida.
    
E_INVALIDARG
  
> Um parâmetro inválido foi especificado.
    
E_NOINTERFACE
  
> A interface de retorno de chamada especificada em  *pAdviseInfo*  não é válida. 
    
## <a name="remarks"></a>Comentários

Ao abrir um objeto offline usando **[HrOpenOfflineObj](hropenofflineobj.md)**, um cliente obtém um objeto offline que oferece suporte a **IMAPIOfflineMgr**. O cliente pode verificar os tipos de retornos de chamada suportados pelo objeto usando **[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)**. O cliente pode determinar o tipo e outros detalhes sobre o retorno de chamada que deseja e, em seguida, chamar **IMAPIOfflineMgr::Advise** para registrar para receber esses retornos de chamada sobre o objeto. 
  
## <a name="see-also"></a>Confira também



[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)
  
[IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md)


[Constantes MAPI](mapi-constants.md)
  
[HrOpenOfflineObj](hropenofflineobj.md)

