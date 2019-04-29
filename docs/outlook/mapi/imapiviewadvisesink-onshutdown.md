---
title: IMAPIViewAdviseSinkOnShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewAdviseSink.OnShutdown
api_type:
- COM
ms.assetid: c9c3aecf-5e4b-407a-8ea1-6211b4c6e0a5
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: b43c1b96130052a05ac390f10f545a66fe72b7fe
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428519"
---
# <a name="imapiviewadvisesinkonshutdown"></a>IMAPIViewAdviseSink::OnShutdown

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Notifica o Visualizador de formulários de que um formulário está sendo fechado.
  
```cpp
HRESULT OnShutdown( void );
```

## <a name="parameters"></a>Parâmetros

Nenhum
  
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A notificação foi bem-sucedida.
    
## <a name="remarks"></a>Comentários

Para obter mais informações sobre notificações de formulário, consulte [envio e recebimento de notificações de formulários](sending-and-receiving-form-notifications.md).
  
## <a name="see-also"></a>Confira também



[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)

