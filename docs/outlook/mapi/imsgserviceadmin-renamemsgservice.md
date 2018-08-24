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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: a6eba20fb346f53052808abf8fcae8993d423d34
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589557"
---
# <a name="imsgserviceadminrenamemsgservice"></a>IMsgServiceAdmin::RenameMsgService

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Obsoleto. Atribui um novo nome para um serviço de mensagem. 
  
```cpp
HRESULT RenameMsgService(
  LPMAPIUID lpUID,
  ULONG ulFlags,
  LPSTR lpszDisplayName
);
```

## <a name="parameters"></a>Parâmetros

 _lpUID_
  
> [in] Um ponteiro para a estrutura [MAPIUID](mapiuid.md) que contém o identificador exclusivo para o serviço de mensagem renomear. 
    
 _ulFlags_
  
> [in] Reservado; deve ser zero.
    
 _lpszDisplayName_
  
> [in] Um ponteiro para o novo nome para o serviço de mensagem.
    
## <a name="return-value"></a>Valor retornado

MAPI_E_NO_SUPPORT 
  
> MAPI não oferece suporte para renomear este serviço de mensagem. **RenameMsgService** sempre retorna este valor. 
    
## <a name="remarks"></a>Comentários

Para atribuir um novo nome para um serviço de mensagem, os clientes devem usar a propriedade **PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md)) do serviço de mensagem. Os nomes dos provedores de serviços em um serviço de mensagem são armazenados em suas propriedades **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)). 
  
## <a name="see-also"></a>Confira também



[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)

