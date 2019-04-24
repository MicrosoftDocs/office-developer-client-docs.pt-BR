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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321424"
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
  
>  no Sinalizadores que modificam o comportamento. Só há suporte para o valor MAPIOFFLINE_ADVISE_DEFAULT. 
    
 _pAdviseInfo_
  
> no Informações sobre o tipo de retorno de chamada, quando receber um retorno de chamada, uma interface de retorno de chamada para o chamador e outros detalhes. Ele também contém um token de cliente usado pelo Outlook no envio de retornos de chamada de notificação subsequentes para o chamador do cliente.
    
 _pulAdviseToken_
  
> bota Um token de aviso retornado ao chamador do cliente para cancelar subsequentemente o retorno de chamada para o objeto.
    
## <a name="return-value"></a>Valor de retorno

S_OK
  
> A chamada foi bem-sucedida.
    
E_INVALIDARG
  
> Um parâmetro inválido foi especificado.
    
E_NOINTERFACE
  
> A interface de retorno de chamada especificada em *pAdviseInfo* não é válida. 
    
## <a name="remarks"></a>Comentários

Ao abrir um objeto offline usando o **[HrOpenOfflineObj](hropenofflineobj.md)**, um cliente obtém um objeto offline que oferece suporte a **IMAPIOfflineMgr**. O cliente pode verificar os tipos de retornos de chamada suportados pelo objeto usando **[IMAPIOffline:: GetCapabilities](imapioffline-getcapabilities.md)**. O cliente pode determinar o tipo e outros detalhes sobre o retorno de chamada desejado e, em seguida, chamar **IMAPIOfflineMgr:: Advise** para registrar para receber tais retornos de chamada sobre o objeto. 
  
## <a name="see-also"></a>Confira também



[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)
  
[IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md)


[Constantes MAPI](mapi-constants.md)
  
[HrOpenOfflineObj](hropenofflineobj.md)

