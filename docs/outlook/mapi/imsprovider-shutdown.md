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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317259"
---
# <a name="imsprovidershutdown"></a>IMSProvider::Shutdown

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Fecha um provedor de repositório de mensagens de maneira ordenada.
  
```cpp
HRESULT Shutdown(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parâmetros

 _lpulFlags_
  
> no Serve deve ser um ponteiro para zero.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada teve êxito e retornou o valor ou valores esperados.
    
## <a name="remarks"></a>Comentários

MAPI chama o método **IMSProvider:: Shutdown** imediatamente antes de liberar o objeto do provedor de repositório de mensagens. MAPI libera todos os objetos de logon para um provedor **** antes de chamar o desligamento para esse provedor. 
  
## <a name="see-also"></a>Confira também



[IMSProvider : IUnknown](imsprovideriunknown.md)

