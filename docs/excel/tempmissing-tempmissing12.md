---
title: TempMissing/TempMissing12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempMissing
- TempMissing12
keywords:
- função tempmissing [excel 2007], função TempMissing12 [Excel 2007]
localization_priority: Normal
ms.assetid: d9cb6afc-1fbb-45d6-88e5-84eba3af3c60
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: a6db2e1f2917ecd9361043577f4bf203b3267a5c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765445"
---
# <a name="tempmissingtempmissing12"></a>TempMissing/TempMissing12

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Função da biblioteca de Framework que cria um temporário **XLOPER**/ **XLOPER12** do tipo **xltypeMissing**.
  
```cs
LPXLOPER TempMissing(void);
LPXLOPER12 TempMissing12(void);
```

## <a name="parameters"></a>Par�metros

Essa função não usa parâmetros.
  
## <a name="return-value"></a>Valor retornado

Retorna um ponteiro para uma **xltypeMissing** **XLOPER**/ **XLOPER12**.
  
## <a name="example"></a>Example

Este exemplo usa **TempMissing12** para fornecer três argumentos ausentes para **xlcWorkspace** seguido **booleano** **FALSE** para suprimir a exibição das barras de rolagem da planilha. Os três primeiros argumentos correspondem às outras configurações de espaço de trabalho que não são afetadas. 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempMissingExample(void)
{
   XLOPER12 xBool;
   xBool.xltype = xltypeBool;
   xBool.val.xbool = 0;
   Excel12f(xlcWorkspace, 0, 4, TempMissing12(), TempMissing12(),
      TempMissing12(), (LPXLOPER12)&xBool);
   return 1;
}
```

## <a name="see-also"></a>Confira também



[Funções na biblioteca do Framework](functions-in-the-framework-library.md)

