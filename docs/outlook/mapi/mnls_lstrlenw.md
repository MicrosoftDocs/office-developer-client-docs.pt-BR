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
ms.openlocfilehash: 70c15970ce69e4bc075da6bf55320cb23116b7a4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768166"
---
# <a name="mnlslstrlenw"></a>MNLS_lstrlenW

  
  
**Aplica-se a**: Outlook 
  
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

