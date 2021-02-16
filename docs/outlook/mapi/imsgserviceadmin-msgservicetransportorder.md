---
title: IMsgServiceAdminMsgServiceTransportOrder
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.MsgServiceTransportOrder
api_type:
- COM
ms.assetid: c57ada0e-b9a1-496b-8548-75686d8cba4e
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 3d532e0eb46daa412711344421936a58da309b7b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420091"
---
# <a name="imsgserviceadminmsgservicetransportorder"></a>IMsgServiceAdmin::MsgServiceTransportOrder

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Define a ordem na qual os provedores de transporte são chamados para entregar uma mensagem.
  
```cpp
HRESULT MsgServiceTransportOrder(
  ULONG cUID,
  LPMAPIUID lpUIDList,
  ULONG ulFlags    
);
```

## <a name="parameters"></a>Parâmetros

 _cUID_
  
> [in] A contagem de identificadores exclusivos no _parâmetro lpUIDList._ 
    
 _lpUIDList_
  
> [in] Um ponteiro para uma matriz de identificadores exclusivos que representam provedores de transporte. A matriz contém um identificador para cada provedor de transporte configurado no perfil atual.
    
 _ulFlags_
  
> [in] Reservado; deve ser zero.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O pedido de transporte foi definido com êxito.
    
MAPI_E_BUSY 
  
> O valor no parâmetro  _cUID_ difere do número de provedores de transporte no perfil. 
    
MAPI_E_NOT_FOUND 
  
> Uma ou mais das estruturas [MAPIUID](mapiuid.md) passadas no parâmetro  _lpUIDList_ não se referem a um provedor de transporte atualmente no perfil. 
    
## <a name="remarks"></a>Comentários

O **método IMsgServiceAdmin::MsgServiceTransportOrder** define a ordem de entrega dos provedores de transporte em um perfil. O _parâmetro lpUIDList_ deve conter uma lista ordenada de identificadores de entrada de provedor de transporte obtidos da propriedade **PR_PROVIDER_UID** ([PidTagProviderUid](pidtagprovideruid-canonical-property.md)) da tabela retornada do método [IMsgServiceAdmin::GetProviderTable.](imsgserviceadmin-getprovidertable.md) Um aplicativo cliente deve passar a lista completa em  _lpUIDList_.
  
 **SetTransportOrder** substitui as preferências do provedor de transporte, como o sinalizador STATUS_XP_PREFER_LAST definido na propriedade **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)). 
  
## <a name="see-also"></a>Confira também



[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)

