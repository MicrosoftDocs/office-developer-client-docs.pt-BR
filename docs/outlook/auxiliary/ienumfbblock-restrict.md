---
title: IEnumFBBlockRestrict
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 887cea55-8f1c-45ec-3100-d03e1213d7c9
description: Restringe a enumeração para um período de tempo especificado.
ms.openlocfilehash: 6b07fe52a84d6a808ab7400ff3e8982b1cce51ca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765817"
---
# <a name="ienumfbblockrestrict"></a>IEnumFBBlock::Restrict

Restringe a enumeração para um período de tempo especificado.
  
## <a name="quick-info"></a>Informações rápidas

Consulte [IEnumFBBlock](ienumfbblock.md).
  
```cpp
HRESULT Restrict(  
    FILETIME ftmStart, 
    FILETIME ftmEnd 
);

```

## <a name="parameters"></a>Par�metros

_ftmStart_
  
>  [in] A hora de início para restringir a enumeração. 
    
_ftmEnd_
  
> [in] A hora de término para restringir a enumeração.
    
## <a name="return-values"></a>Valores de retorno

S_OK se a chamada foi bem-sucedida; Caso contrário, um código de erro.
  
## <a name="remarks"></a>Coment�rios

Este método também redefine a enumeração.
  
## <a name="see-also"></a>Confira também

- [IEnumFBBlock::Clone](ienumfbblock-clone.md)  
- [IEnumFBBlock::Next](ienumfbblock-next.md)  
- [IEnumFBBlock::Reset](ienumfbblock-reset.md)  
- [IEnumFBBlock::Skip](ienumfbblock-skip.md)  
- [Use o tempo relativo para acessar dados do tipo disponível/ocupado](how-to-use-relative-time-to-access-free-busy-data.md)

