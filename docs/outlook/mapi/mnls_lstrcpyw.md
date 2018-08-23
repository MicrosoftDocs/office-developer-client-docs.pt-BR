---
title: MNLS_lstrcpyW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a0f92c2d-b5ba-4558-b8a2-484b2db32bec
description: 'Modificado pela última vez: 18 de junho de 2012'
ms.openlocfilehash: 4d3210c098d0a7c83721798c8c32ffd9f1e5ebb4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575459"
---
# <a name="mnlslstrcpyw"></a>MNLS_lstrcpyW

 
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Copia uma cadeia de caracteres para um buffer.
  
> [!CAUTION]
> Não a use. Considere o uso [StringCchCopy](http://msdn.microsoft.com/en-us/library/ms647527%28VS.85%29.aspx) . 
  
```cpp
LPWSTR MNLS_lstrcpyW(
 LPWSTR lpString1,
LPCWSTR lpString2);
```

## <a name="parameters"></a>Parâmetros

lpString1
  
> [out] Um buffer para receber o conteúdo da cadeia de caracteres apontado pelo parâmetro lpString2.
    
lpString2
  
> [in] A sequência terminada em nulo a ser copiado.
    
## <a name="return-value"></a>Valor retornado

Se a função tiver êxito, o valor de retorno é um ponteiro para o buffer.
  
Se a função falhar, o valor de retorno é nulo e lpString1 pode não ser terminada em nulo.
  
## <a name="remarks"></a>Comentários

Essa função é disposto a função **lstrcpy** . Para obter mais informações, consulte [lstrcpy](http://msdn.microsoft.com/en-us/library/ms647490%28VS.85%29.aspx).
  
## <a name="see-also"></a>Confira também



[lstrcpy](http://msdn.microsoft.com/en-us/library/ms647490%28VS.85%29.aspx)

