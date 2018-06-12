---
title: IOlkAccountManagerFreeMemory
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: acb67186-ab38-e918-5402-2526307a5bd0
description: Libera memória alocada pela interface IOlkAccountManager.
ms.openlocfilehash: 85ba4d0d47eb5c879fa562e3147860533ef59f23
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765956"
---
# <a name="iolkaccountmanagerfreememory"></a>IOlkAccountManager::FreeMemory

Libera memória alocada pela interface [IOlkAccountManager](iolkaccountmanager.md) . 
  
## <a name="quick-info"></a>Informações rápidas

Consulte [IOlkAccountManager](iolkaccountmanager.md).
  
```cpp
HRESULT IOlkAccountManager::FreeMemory (  
    BYTE *pv, 
);
```

## <a name="parameters"></a>Par�metros

_VP_
  
> [in] Um ponteiro para a memória para liberar.
    
## <a name="return-values"></a>Valores de retorno

S_OK se a chamada foi bem-sucedida; Caso contrário, um código de erro.
  
## <a name="remarks"></a>Coment�rios

Use esse método para liberar memória alocada pelo [IOlkAccountManager::GetOrder](iolkaccountmanager-getorder.md).
  
## <a name="see-also"></a>Confira também

- [IOlkAccountManager::GetOrder](iolkaccountmanager-getorder.md)

