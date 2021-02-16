---
title: IMsgServiceAdminRenameMsgService
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.RenameMsgService
api_type:
- COM
ms.assetid: eba0e7f2-03c1-4713-aa36-3d0b398cd197
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 2f0f1fb94ea36512bbc40df8a4877e89d2613a25
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422100"
---
# <a name="imsgserviceadminrenamemsgservice"></a>IMsgServiceAdmin::RenameMsgService

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Depreciado. Atribui um novo nome a um serviço de mensagens. 
  
```cpp
HRESULT RenameMsgService(
  LPMAPIUID lpUID,
  ULONG ulFlags,
  LPSTR lpszDisplayName
);
```

## <a name="parameters"></a>Parâmetros

 _lpUID_
  
> [in] Um ponteiro para a [estrutura MAPIUID](mapiuid.md) que contém o identificador exclusivo para o serviço de mensagens a ser renomeada. 
    
 _ulFlags_
  
> [in] Reservado; deve ser zero.
    
 _lpszDisplayName_
  
> [in] Um ponteiro para o novo nome para o serviço de mensagens.
    
## <a name="return-value"></a>Valor de retorno

MAPI_E_NO_SUPPORT 
  
> O MAPI não dá suporte à renomeação desse serviço de mensagens. **RenameMsgService** sempre retorna esse valor. 
    
## <a name="remarks"></a>Comentários

Para atribuir um novo nome a um serviço de mensagens, os clientes devem usar a **propriedade PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md)) do serviço de mensagens. Os nomes dos provedores de serviços em um serviço de mensagens são armazenados **em suas PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) propriedades. 
  
## <a name="see-also"></a>Confira também



[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)

