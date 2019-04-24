---
title: IOlkAccountFreeMemory
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3b2ee5aa-7639-d86d-447e-50bda54aa3ec
description: Libera memória alocada pela interface IOlkAccount.
ms.openlocfilehash: a7f763ba4fc260a517f8b7df4d3791f4a8fd23b0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321333"
---
# <a name="iolkaccountfreememory"></a>IOlkAccount::FreeMemory

Libera memória alocada pela interface [IOlkAccount](iolkaccount.md) . 
  
## <a name="quick-info"></a>Informações rápidas

Confira [IOlkAccount](iolkaccount.md).
  
```cpp
HRESULT IOlkAccount::FreeMemory (  
    BYTE *pv, 
); 

```

## <a name="parameters"></a>Parâmetros

_PV_
  
> no Um ponteiro para que a memória seja liberada.
    
## <a name="return-values"></a>Valores de retorno

S_OK se a chamada for bem-sucedida; caso contrário, um código de erro.
  
## <a name="remarks"></a>Comentários

Use este método para liberar memória alocada por [IOlkAccount:: GetProp](iolkaccount-getprop.md) (se o valor da propriedade de conta especificada for um tipo de cadeia de caracteres ou binário) e [IOlkAccount:: GetAccountInfo](iolkaccount-getaccountinfo.md).
  
## <a name="see-also"></a>Confira também

- [IOlkAccount::GetAccountInfo](iolkaccount-getaccountinfo.md)  
- [IOlkAccount::GetProp](iolkaccount-getprop.md)

