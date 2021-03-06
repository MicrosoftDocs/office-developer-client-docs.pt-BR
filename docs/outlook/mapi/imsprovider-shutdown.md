---
title: IMSProviderShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSProvider.Shutdown
api_type:
- COM
ms.assetid: 9ca1861d-9bc9-485a-9807-a598b869e5a2
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 77688f8a09c1d990201a247a3c4e3a11ba0963b3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438621"
---
# <a name="imsprovidershutdown"></a>IMSProvider::Shutdown

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Fecha um provedor de armazenamento de mensagens de forma pedido.
  
```cpp
HRESULT Shutdown(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parâmetros

 _lpulFlags_
  
> [in] Reservado; deve ser um ponteiro para zero.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor ou os valores esperados.
    
## <a name="remarks"></a>Comentários

MAPI calls the **IMSProvider::Shutdown** method just before releasing the message store provider object. O MAPI libera todos os objetos de logon para um provedor antes de chamar **o Desligamento** desse provedor. 
  
## <a name="see-also"></a>Confira também



[IMSProvider : IUnknown](imsprovideriunknown.md)

