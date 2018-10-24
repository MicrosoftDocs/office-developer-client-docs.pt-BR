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
ms.openlocfilehash: 559f1c609000608d0eb920a0240ac8848e4bc2a7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570790"
---
# <a name="imsgserviceadminmsgservicetransportorder"></a>IMsgServiceAdmin::MsgServiceTransportOrder

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Define a ordem na qual transporte provedores são chamados para entregar uma mensagem.
  
```cpp
HRESULT MsgServiceTransportOrder(
  ULONG cUID,
  LPMAPIUID lpUIDList,
  ULONG ulFlags    
);
```

## <a name="parameters"></a>Parâmetros

 _cUID_
  
> [in] A contagem de identificadores exclusivos no parâmetro _lpUIDList_ . 
    
 _lpUIDList_
  
> [in] Um ponteiro para uma matriz de identificadores exclusivos que representam os provedores de transporte. A matriz contém um identificador para cada provedor de transporte configurada no perfil atual.
    
 _ulFlags_
  
> [in] Reservado; deve ser zero.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A ordem de transporte foi definida com êxito.
    
MAPI_E_BUSY 
  
> O valor no parâmetro _cUID_ difere do número de provedores de transporte realmente no perfil. 
    
E_NOT_FOUND 
  
> Uma ou mais das estruturas [MAPIUID](mapiuid.md) passadas no parâmetro _lpUIDList_ não fazem referência a um provedor de transporte no momento no perfil. 
    
## <a name="remarks"></a>Comentários

O método **IMsgServiceAdmin::MsgServiceTransportOrder** define a ordem de entrega de provedores de transporte em um perfil. O parâmetro _lpUIDList_ deve conter uma lista classificada dos identificadores de entrada do provedor de transporte obtidos da propriedade **PR_PROVIDER_UID** ([PidTagProviderUid](pidtagprovideruid-canonical-property.md)) da tabela retornada do [IMsgServiceAdmin:: GetProviderTable](imsgserviceadmin-getprovidertable.md) método. Um aplicativo cliente deve passar a lista completa em _lpUIDList_.
  
 Substituições **SetTransportOrder** transportam preferências de provedor, como o sinalizador STATUS_XP_PREFER_LAST definido na propriedade **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)). 
  
## <a name="see-also"></a>Confira também



[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)

