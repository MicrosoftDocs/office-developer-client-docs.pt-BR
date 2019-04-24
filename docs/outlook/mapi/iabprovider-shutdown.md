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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348899"
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
  
> No Serve deve ser um ponteiro para zero.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A conexão foi cancelada com êxito.
    
## <a name="notes-to-implementers"></a>Observações para implementadores

Na sua implementação do método **Shutdown** , execute qualquer tarefa que você considere necessário. O MAPI chama seu método **Shutdown** somente depois que você lançou todos os objetos de logon. 
  
## <a name="see-also"></a>Confira também



[IABProvider : IUnknown](iabprovideriunknown.md)

