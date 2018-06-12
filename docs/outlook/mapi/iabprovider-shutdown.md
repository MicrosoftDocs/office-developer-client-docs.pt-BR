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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 2f1872c6f95f8ab12014de9890b0d03789bc5f0d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766859"
---
# <a name="iabprovidershutdown"></a>IABProvider::Shutdown

  
  
**Aplica-se a**: Outlook 
  
Cancela uma conexão para uma sessão ativa.
  
```cpp
HRESULT Shutdown(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Par�metros

 _lpulFlags_
  
> [In] Reservado; deve ser um ponteiro para zero.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A conexão foi cancelada com êxito.
    
## <a name="notes-to-implementers"></a>Notas para implementadores

Em sua implementação do método **desligamento** , execute as tarefas que você considerar necessário. MAPI chama seu método de **desligamento** somente depois de você ter lançado todos os seus objetos de logon. 
  
## <a name="see-also"></a>Confira também



[IABProvider: IUnknown](iabprovideriunknown.md)

