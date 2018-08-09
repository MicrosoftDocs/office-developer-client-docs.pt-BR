---
title: IXPProviderShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPProvider.Shutdown
api_type:
- COM
ms.assetid: e2d8a025-c2a3-4edb-b6e4-022e07e854dd
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: f5d253d0306e55699fbe5b9c9decf8c3242867fd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767756"
---
# <a name="ixpprovidershutdown"></a>IXPProvider::Shutdown

  
  
**Aplica-se a**: Outlook 
  
Fecha para baixo de um provedor de transporte de forma ordenada.
  
```cpp
HRESULT Shutdown (
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parâmetros

 _lpulFlags_
  
> [in] Reservado; deve ser zero.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada teve êxito em desligar o provedor de transporte.
    
## <a name="remarks"></a>Comentários

O MAPI spooler chama o método **IXPProvider::Shutdown** antes de liberar um objeto de provedor de transporte. Antes de chamar o **desligamento**, MAPI libera todos os objetos de logon para um provedor.
  
## <a name="see-also"></a>Confira também



[XPProviderInit](xpproviderinit.md)
  
[IXPProvider : IUnknown](ixpprovideriunknown.md)

