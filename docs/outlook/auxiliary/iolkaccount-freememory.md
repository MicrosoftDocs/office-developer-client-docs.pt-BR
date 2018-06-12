---
title: IOlkAccountFreeMemory
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3b2ee5aa-7639-d86d-447e-50bda54aa3ec
description: Libera memória alocada pela interface IOlkAccount.
ms.openlocfilehash: ce3046db29cb2cac7d7ee72a3e4e9125346a4ac4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765900"
---
# <a name="iolkaccountfreememory"></a>IOlkAccount::FreeMemory

Libera memória alocada pela interface [IOlkAccount](iolkaccount.md) . 
  
## <a name="quick-info"></a>Informações rápidas

Consulte [IOlkAccount](iolkaccount.md).
  
```cpp
HRESULT IOlkAccount::FreeMemory (  
    BYTE *pv, 
); 

```

## <a name="parameters"></a>Par�metros

_VP_
  
> [in] Um ponteiro para a memória para ser liberada.
    
## <a name="return-values"></a>Valores de retorno

S_OK se a chamada foi bem-sucedida; Caso contrário, um código de erro.
  
## <a name="remarks"></a>Coment�rios

Use este método para liberar memória alocado pelo [IOlkAccount::GetProp](iolkaccount-getprop.md) (se o valor da propriedade conta especificada é um tipo binário ou cadeia de caracteres) e [IOlkAccount::GetAccountInfo](iolkaccount-getaccountinfo.md).
  
## <a name="see-also"></a>Confira também

- [IOlkAccount::GetAccountInfo](iolkaccount-getaccountinfo.md)  
- [IOlkAccount::GetProp](iolkaccount-getprop.md)

