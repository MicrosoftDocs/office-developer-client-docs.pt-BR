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
- função tempactivecolumn12 [excel 2007], função TempActiveColumn [Excel 2007]
localization_priority: Normal
ms.assetid: 4b1f34c4-e7fa-4a0b-8fc5-c9d465ebb70c
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: ac3dbb0bb43527f790e6934d73bee30a33f8555f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765439"
---
# <a name="tempactivecolumntempactivecolumn12"></a>TempActiveColumn/TempActiveColumn12

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Funções da biblioteca Framework que criam um temporário **XLOPER**/ **XLOPER12** contendo uma referência externa para uma coluna inteira na planilha ativa. 
  
```cs
LPXLOPER TempActiveColumn(BYTE col);
LPXLOPER12 TempActiveColumn12(COL col);
```

## <a name="parameters"></a>Par�metros

 _col_ (**Bytes**)
  
A coluna a ser referenciado. Isso é baseado em zero que a coluna A é passada como 0. No Microsoft Office Excel 2003 e anteriores versões e iniciando em uma pasta de trabalho em execução no modo de compatibilidade do Excel 2007, o valor máximo é de 255 = 2 ^ 8 1 e é o valor máximo que pode ser realizado por um inteiro de bytes. Iniciando no Excel 2007 executando uma pasta de trabalho, o valor máximo é 16,383 = 2 ^ 14-1. COL é definido como um inteiro assinado de 32 bits em XLCALL. H.
  
## <a name="return-value"></a>Valor retornado

Retorna uma referência de **xltypeRef** externo à coluna passada. 
  
## <a name="example"></a>Example

O exemplo a seguir usa **TempActiveColumn12** para selecionar toda a coluna B. 
  
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

