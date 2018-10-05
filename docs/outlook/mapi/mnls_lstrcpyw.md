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
ms.openlocfilehash: 1a1cf0a607dd4b57353eda74f9b14965e110c071
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382705"
---
# <a name="mnlslstrcpyw"></a>MNLS_lstrcpyW

 
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Copia uma cadeia de caracteres para um buffer.
  
> [!CAUTION]
> Não a use. Considere o uso [StringCchCopy](https://msdn.microsoft.com/library/ms647527%28VS.85%29.aspx) . 
  
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
    
## <a name="return-value"></a>Valor de retorno

Se a função tiver êxito, o valor de retorno é um ponteiro para o buffer.
  
Se a função falhar, o valor de retorno é nulo e lpString1 pode não ser terminada em nulo.
  
## <a name="remarks"></a>Comentários

Essa função é disposto a função **lstrcpy** . Para obter mais informações, consulte [lstrcpy](https://msdn.microsoft.com/library/ms647490%28VS.85%29.aspx).
  
## <a name="see-also"></a>Confira também



[lstrcpy](https://msdn.microsoft.com/library/ms647490%28VS.85%29.aspx)

