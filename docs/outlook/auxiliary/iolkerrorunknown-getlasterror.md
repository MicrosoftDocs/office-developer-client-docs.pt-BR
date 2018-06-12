---
title: IOlkErrorUnknownGetLastError
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3f332de3-470d-9bc2-0c65-684bb58bcd7a
description: Obtém uma cadeia de caracteres da mensagem de erro especificado.
ms.openlocfilehash: 7b00392cdf65d1d4990f2231769e5126c9ae26dc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765989"
---
# <a name="iolkerrorunknowngetlasterror"></a>IOlkErrorUnknown::GetLastError

Obtém uma cadeia de caracteres da mensagem de erro especificado. 
  
## <a name="quick-info"></a>Informações rápidas

Consulte [IOlkErrorUnknown](iolkerrorunknown.md).
  
```cpp
HRESULT IOlkErrorUnknown::GetLastError(  
    HRESULT hr, 
    LPWSTR *ppwszError 
); 

```

## <a name="parameters"></a>Par�metros

_RH_
  
> [in] O código de erro a ser procurada.
    
_ppwszError_
  
> [out] A mensagem de erro que corresponde ao *RH* . 
    
## <a name="return-values"></a>Valores de retorno

|**HRESULT**|**Descrição**|
|:-----|:-----|
|S_OK  <br/> |A chamada foi bem-sucedida.  <br/> |
|E_INVALIDARG  <br/> |Um ou mais argumentos são inválidos.  <br/> |
   
## <a name="see-also"></a>Confira também

- [Constantes (API de gerenciamento de conta)](constants-account-management-api.md)

