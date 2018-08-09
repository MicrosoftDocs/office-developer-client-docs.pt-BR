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
ms.openlocfilehash: ff748827950c79c3c94e9f70ce8b0bb335884290
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767474"
---
# <a name="imsgserviceadminrenamemsgservice"></a>IMsgServiceAdmin::RenameMsgService

  
  
**Aplica-se a**: Outlook 
  
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

