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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: a57a72b413ba412154a27a08244e86b117cbea7d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409689"
---
# <a name="ixpprovidershutdown"></a>IXPProvider::Shutdown

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Fecha um provedor de transporte de maneira ordenada.
  
```cpp
HRESULT Shutdown (
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parâmetros

 _lpulFlags_
  
> no Serve deve ser zero.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada teve êxito ao desligar o provedor de transporte.
    
## <a name="remarks"></a>Comentários

O spooler MAPI chama o método **IXPProvider:: Shutdown** antes de liberar um objeto de provedor de transporte. Antes de chamar **Shutdown**, MAPI libera todos os objetos de logon de um provedor.
  
## <a name="see-also"></a>Confira também



[XPProviderInit](xpproviderinit.md)
  
[IXPProvider : IUnknown](ixpprovideriunknown.md)

