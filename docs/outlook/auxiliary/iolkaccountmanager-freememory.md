---
title: IOlkAccountManagerFreeMemory
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: acb67186-ab38-e918-5402-2526307a5bd0
description: Libera memória alocada pela interface IOlkAccountManager.
ms.openlocfilehash: 3e680e1e26d6c9b12c2dd4a7d48df4dbeae14154
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322054"
---
# <a name="iolkaccountmanagerfreememory"></a>IOlkAccountManager::FreeMemory

Libera memória alocada pela interface [IOlkAccountManager](iolkaccountmanager.md) . 
  
## <a name="quick-info"></a>Informações rápidas

Confira [IOlkAccountManager](iolkaccountmanager.md).
  
```cpp
HRESULT IOlkAccountManager::FreeMemory (  
    BYTE *pv, 
);
```

## <a name="parameters"></a>Parâmetros

_PV_
  
> no Um ponteiro para a memória a ser liberado.
    
## <a name="return-values"></a>Valores de retorno

S_OK se a chamada for bem-sucedida; caso contrário, um código de erro.
  
## <a name="remarks"></a>Comentários

Use este método para liberar a memória alocada por [IOlkAccountManager:: GetOrder](iolkaccountmanager-getorder.md).
  
## <a name="see-also"></a>Confira também

- [IOlkAccountManager::GetOrder](iolkaccountmanager-getorder.md)

