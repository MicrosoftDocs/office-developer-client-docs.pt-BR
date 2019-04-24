---
title: IOlkEnumSkip
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e83e409c-f201-df9d-5e30-879adf15318d
description: Ignora um número especificado de contas no enumerador.
ms.openlocfilehash: d4063b0ff4852e6932cf50789eea3caa81d4d586
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321984"
---
# <a name="iolkenumskip"></a>IOlkEnum::Skip

Ignora um número especificado de contas no enumerador.
  
## <a name="quick-info"></a>Informações rápidas

Consulte [IOlkEnum](iolkenum.md).
  
```cpp
HRESULT IOlkEnum::Skip(  
    DWORD cSkip 
);
```

## <a name="parameters"></a>Parâmetros

_cSkip_
  
> no O número de contas a serem ignoradas.
    
## <a name="return-values"></a>Valores de retorno

S_OK se a chamada foi bem-sucedida. Caso contrário, um código de erro.
  
## <a name="see-also"></a>Confira também

- [IOlkEnum::GetCount](iolkenum-getcount.md) 
- [IOlkEnum::GetNext](iolkenum-getnext.md)  
- [IOlkEnum::Reset](iolkenum-reset.md)

