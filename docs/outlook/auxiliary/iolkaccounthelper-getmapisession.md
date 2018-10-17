---
title: IOlkAccountHelperGetMapiSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a431787c-6e9a-9be1-165f-98c778d12e3e
description: Abre uma sessão MAPI e mantém uma referência à sessão para o gerente de conta.
ms.openlocfilehash: 5886ac1ae1bb8f3b43e09f49e48434d9a73656ce
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392596"
---
# <a name="iolkaccounthelpergetmapisession"></a>IOlkAccountHelper::GetMapiSession

Abre uma sessão MAPI e mantém uma referência à sessão para o gerente de conta.
  
## <a name="quick-info"></a>Informações rápidas

Confira [IOlkAccountHelper](iolkaccounthelper.md).
  
```cpp
HRESULT IOlkAccountHelper::GetMapiSession(  
    LPUNKNOWN *ppmsess 
);
```

## <a name="parameters"></a>Parâmetros

_ppmsess_
  
> [out] A sessão MAPI atual.
    
## <a name="return-values"></a>Valor de retorno

S_OK se a chamada foi bem-sucedida. Caso contrário, um código de erro.
  
## <a name="remarks"></a>Comentários

Devido a problemas de referência circular, o gerente de conta em si não pode manter a referência para a sessão MAPI.
  
## <a name="see-also"></a>Confira também

- [IOlkAccountHelper::HandsOffSession](iolkaccounthelper-handsoffsession.md)
- [IMAPISession : IUnknown](https://msdn.microsoft.com/library/5650fa2a-6e62-451c-964e-363f7bee2344%28Office.15%29.aspx)

