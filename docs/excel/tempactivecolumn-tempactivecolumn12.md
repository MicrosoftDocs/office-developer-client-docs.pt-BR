---
title: TempActiveColumn/TempActiveColumn12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempActiveColumn
- TempActiveColumn12
keywords:
- função tempactivecolumn12 [Excel 2007], função TempActiveColumn [Excel 2007]
localization_priority: Normal
ms.assetid: 4b1f34c4-e7fa-4a0b-8fc5-c9d465ebb70c
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: d1399a407e3e269b78c7afbde8ff32c126b4b1bc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310466"
---
# <a name="tempactivecolumntempactivecolumn12"></a>TempActiveColumn/TempActiveColumn12

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Funções de biblioteca da estrutura que criam um **XLOPER de XLOPER**/ **** temporário contendo uma referência externa para uma coluna inteira na planilha ativa. 
  
```cs
LPXLOPER TempActiveColumn(BYTE col);
LPXLOPER12 TempActiveColumn12(COL col);
```

## <a name="parameters"></a>Parâmetros

 _Col_ (**Byte**)
  
A coluna a ser referenciada. Isso é baseado em zero, para que A coluna A seja passada como 0. No Microsoft Office Excel 2003 e versões anteriores, e a partir do Excel 2007 executando uma pasta de trabalho no modo de compatibilidade, o valor máximo é 255 = 2 ^ 8-1 e é o valor máximo que pode ser feito por um inteiro de BYTE. A partir do Excel 2007 executando uma pasta de trabalho, o valor máximo é 16.383 = 2 ^ 14-1. COL é definido como um inteiro assinado de 32 bits em XLCALL. 0.
  
## <a name="return-value"></a>Valor de retorno

Retorna uma referência externa **xltypeRef** à coluna passada. 
  
## <a name="example"></a>Exemplo

O exemplo a seguir usa **TempActiveColumn12** para selecionar a coluna inteira B. 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempActiveColumnExample(void)
{
    Excel12f(xlcSelect, 0, 1, TempActiveColumn12(1));
    return 1;
}
```

## <a name="see-also"></a>Confira também



[Funções na biblioteca do Framework](functions-in-the-framework-library.md)

