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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 334ec8dd0c683cf9b765f387281c624b20520098
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767544"
---
# <a name="imsprovidershutdown"></a>IMSProvider::Shutdown

  
  
**Aplica-se a**: Outlook 
  
Fecha um provedor de armazenamento de mensagem de forma ordenada.
  
```cpp
HRESULT Shutdown(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parâmetros

 _lpulFlags_
  
> [in] Reservado; deve ser um ponteiro para zero.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
## <a name="remarks"></a>Comentários

MAPI chama o método **IMSProvider::Shutdown** antes de liberar o objeto de provedor de repositório de mensagem. MAPI libera todos os objetos de logon para um provedor antes de chamar o **desligamento** desse provedor. 
  
## <a name="see-also"></a>Confira também



[IMSProvider : IUnknown](imsprovideriunknown.md)

