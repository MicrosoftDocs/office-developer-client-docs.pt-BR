---
title: MNLS_lstrlenW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d342a956-1164-4c9c-b0bb-7a0b72dc97fc
description: 'Modificado pela última vez: 21 de fevereiro de 2012'
ms.openlocfilehash: 1135a8e07bf94a200d06db8b692ee39dfdb78272
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588885"
---
# <a name="mnlslstrlenw"></a>MNLS_lstrlenW

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Determina o comprimento da cadeia Unicode especificado, excluindo o caractere de terminação null.
  
> [!TIP]
> Considere o uso [StringCchLength](http://msdn.microsoft.com/en-us/library/ms647539%28VS.85%29.aspx) . 
  
```cpp
int MNLS_lstrlen(
  LPCWSTR lpsz);
```

## <a name="parameters"></a>Parâmetros

 _lpsz_
  
> [in] A sequência de Unicode terminada em nulo a ser verificado.
    
## <a name="return-value"></a>Valor retornado

A função retorna um inteiro com o comprimento da cadeia de caracteres. É uma contagem de caracteres na cadeia de caracteres, excluindo o caractere de terminação null. Se _lpsz_ for NULL, a função retornará zero. 
  
## <a name="remarks"></a>Comentários

Essa função é disposto a função **lstrlen** . Para obter mais informações, consulte [lstrlen](http://msdn.microsoft.com/en-us/library/ms647492%28VS.85%29.aspx).
  
## <a name="see-also"></a>Confira também



[lstrlen](http://msdn.microsoft.com/en-us/library/ms647492%28VS.85%29.aspx)
  
[StringCchLength](http://msdn.microsoft.com/en-us/library/ms647539%28VS.85%29.aspx)

