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
- função tempactivecolumn12 [excel 2007],função TempActiveColumn [Excel 2007]
localization_priority: Normal
ms.assetid: 4b1f34c4-e7fa-4a0b-8fc5-c9d465ebb70c
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: d1399a407e3e269b78c7afbde8ff32c126b4b1bc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417872"
---
# <a name="tempactivecolumntempactivecolumn12"></a>TempActiveColumn/TempActiveColumn12

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Funções de biblioteca de estrutura que criam um /  **XLOPER XLOPER12** temporário contendo uma referência externa a uma coluna inteira na planilha ativa. 
  
```cs
LPXLOPER TempActiveColumn(BYTE col);
LPXLOPER12 TempActiveColumn12(COL col);
```

## <a name="parameters"></a>Parâmetros

 _col_ (**BYTE**)
  
A coluna a ser referenciada. Isso é baseado em zero para que a coluna A seja passada como 0. No Microsoft Office Excel 2003 e em versões anteriores, e a partir do Excel 2007 executando uma planilha no modo de compatibilidade, o valor máximo é 255 = 2^8 - 1 e é o valor máximo que pode ser tomada por um inteiro BYTE. A partir do Excel 2007 executando uma planilha, o valor máximo é 16.383 = 2^14 - 1. COL é definido como um inteiro assinado de 32 bits em XLCALL.H.
  
## <a name="return-value"></a>Valor de retorno

Retorna uma **referência externa xltypeRef** para a coluna passada. 
  
## <a name="example"></a>Exemplo

O exemplo a seguir **usa TempActiveColumn12** para selecionar a coluna B inteira. 
  
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

