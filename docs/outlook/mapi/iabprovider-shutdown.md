---
title: IABProviderShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABProvider.Shutdown
api_type:
- COM
ms.assetid: 1fbe6dc1-254b-4557-92c8-9fa42a8efd64
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 8b2190f77c7575d3d4f5e25fa0863bec844158bc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409780"
---
# <a name="iabprovidershutdown"></a>IABProvider::Shutdown

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Cancela uma conexão com uma sessão ativa.
  
```cpp
HRESULT Shutdown(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parâmetros

 _lpulFlags_
  
> [In] Reservado; deve ser um ponteiro para zero.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A conexão foi cancelada com êxito.
    
## <a name="notes-to-implementers"></a>Observações para implementadores

Na implementação do método **Shutdown,** execute as tarefas que considerar necessárias. MAPI calls your **Shutdown** method only after you have released all your logon objects. 
  
## <a name="see-also"></a>Confira também



[IABProvider : IUnknown](iabprovideriunknown.md)

