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
ms.openlocfilehash: 0a93dd44960a01996672a55501a7626d0ff56986
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567885"
---
# <a name="iabprovidershutdown"></a>IABProvider::Shutdown

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Cancela uma conexão para uma sessão ativa.
  
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

Em sua implementação do método **desligamento** , execute as tarefas que você considerar necessário. MAPI chama seu método de **desligamento** somente depois de você ter lançado todos os seus objetos de logon. 
  
## <a name="see-also"></a>Confira também



[IABProvider : IUnknown](iabprovideriunknown.md)

