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
ms.openlocfilehash: 2e4ae22ace37455c9ccb9d8ff2a7f07a48132234
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768149"
---
# <a name="mnlslstrcpyw"></a>MNLS_lstrcpyW

 
  
**Aplica-se a**: Outlook 
  
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

