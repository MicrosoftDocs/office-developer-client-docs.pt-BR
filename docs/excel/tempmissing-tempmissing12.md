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
- função tempmissing [Excel 2007], função TempMissing12 [Excel 2007]
localization_priority: Normal
ms.assetid: d9cb6afc-1fbb-45d6-88e5-84eba3af3c60
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 37c127b2252f18643b34dfc72fd9929885a68d01
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310490"
---
# <a name="tempmissingtempmissing12"></a>TempMissing/TempMissing12

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Função da biblioteca de estrutura que cria um **XLOPER de XLOPER**/ **** temporário do tipo **xltypeMissing**.
  
```cs
LPXLOPER TempMissing(void);
LPXLOPER12 TempMissing12(void);
```

## <a name="parameters"></a>Parâmetros

Essa função não usa parâmetros.
  
## <a name="return-value"></a>Valor de retorno

Retorna um ponteiro para um **** ****/ **XLOPER12**XLOPER xltypeMissing.
  
## <a name="example"></a>Exemplo

Este exemplo usa **TempMissing12** para fornecer três argumentos ausentes para **xlcWorkspace** seguidos por um **Boolean** **falso** para suprimir a exibição das barras de rolagem da planilha. Os primeiros três argumentos correspondem a outras configurações do espaço de trabalho que não são afetadas. 
  
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

