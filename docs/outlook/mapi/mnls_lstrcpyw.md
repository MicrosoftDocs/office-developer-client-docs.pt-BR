---
title: MNLS_lstrcpyW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a0f92c2d-b5ba-4558-b8a2-484b2db32bec
description: 'Última modificação: 18 de junho de 2012'
ms.openlocfilehash: 1a1cf0a607dd4b57353eda74f9b14965e110c071
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341724"
---
# <a name="mnls_lstrcpyw"></a>MNLS_lstrcpyW

 
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Copia uma cadeia de caracteres para um buffer.
  
> [!CAUTION]
> Não usar. Considere usar [StringCchCopy](https://msdn.microsoft.com/library/ms647527%28VS.85%29.aspx) em vez disso. 
  
```cpp
LPWSTR MNLS_lstrcpyW(
 LPWSTR lpString1,
LPCWSTR lpString2);
```

## <a name="parameters"></a>Parâmetros

lpString1
  
> [out] Um buffer para receber o conteúdo da cadeia de caracteres apontado pelo parâmetro lpString2.
    
lpString2
  
> [in] A cadeia de caracteres terminada por caractere nulo a ser copiada.
    
## <a name="return-value"></a>Valor de retorno

Se a função for bem-sucedida, o valor de retorno será um ponteiro para o buffer.
  
Se a função falhar, o valor de retorno será NULL e lpString1 poderá não ser encerrado por nulo.
  
## <a name="remarks"></a>Comentários

Esta função quebra a **função lstrcpy.** Para obter mais informações, [consulte lstrcpy](https://msdn.microsoft.com/library/ms647490%28VS.85%29.aspx).
  
## <a name="see-also"></a>Confira também



[lstrcpy](https://msdn.microsoft.com/library/ms647490%28VS.85%29.aspx)

