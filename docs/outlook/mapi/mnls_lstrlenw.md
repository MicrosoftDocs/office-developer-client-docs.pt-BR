---
title: MNLS_lstrlenW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d342a956-1164-4c9c-b0bb-7a0b72dc97fc
description: 'Última modificação: 21 de fevereiro de 2012'
ms.openlocfilehash: 31f699d1193e55a88e57a0f491658e0d537ef75d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338462"
---
# <a name="mnls_lstrlenw"></a>MNLS_lstrlenW

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Determina o comprimento da cadeia de caracteres Unicode especificada, excluindo o caractere nulo de terminação.
  
> [!TIP]
> Considere usar [StringCchLength](https://msdn.microsoft.com/library/ms647539%28VS.85%29.aspx) em vez disso. 
  
```cpp
int MNLS_lstrlen(
  LPCWSTR lpsz);
```

## <a name="parameters"></a>Parâmetros

 _lpsz_
  
> [in] A cadeia de caracteres Unicode terminada por caractere nulo a ser verificada.
    
## <a name="return-value"></a>Valor de retorno

A função retorna um inteiro com o comprimento da cadeia de caracteres. É uma contagem de caracteres na cadeia de caracteres, excluindo o caractere nulo de terminação. Se  _lpsz_ for NULL, a função retornará zero. 
  
## <a name="remarks"></a>Comentários

Esta função quebra a **função lstrlen.** Para obter mais informações, consulte [lstrlen](https://msdn.microsoft.com/library/ms647492%28VS.85%29.aspx).
  
## <a name="see-also"></a>Confira também



[lstrlen](https://msdn.microsoft.com/library/ms647492%28VS.85%29.aspx)
  
[StringCchLength](https://msdn.microsoft.com/library/ms647539%28VS.85%29.aspx)

