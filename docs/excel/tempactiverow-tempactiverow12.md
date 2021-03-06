---
title: TempActiveRow/TempActiveRow12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempActiveRow
- TempActiveRow12
keywords:
- função tempactiverow [excel 2007],função TempActiveRow12 [Excel 2007]
localization_priority: Normal
ms.assetid: cbb9181c-59b0-4133-a085-94a94ac3f229
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 1f89c458a521b41e4f172f8a6c53526440bb472b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413105"
---
# <a name="tempactiverowtempactiverow12"></a>TempActiveRow/TempActiveRow12

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Funções de biblioteca de estrutura que criam um /  **XLOPER XLOPER12** temporário contendo uma referência externa a uma linha inteira na planilha ativa. 
  
```cs
LPXLOPER TempActiveRow(WORD row);
LPXLOPER12 TempActiveRow12(ROW row);
```

## <a name="parameters"></a>Parâmetros

 _row_
  
A linha a ser referenciada. Os argumentos de linha são baseados em zero para que a linha 1 seja passada como 0. No Microsoft Office Excel 2003 e em versões anteriores, e a partir do Excel 2007 executando uma planilha no modo de compatibilidade, o valor máximo é 65.535 = 2^16 - 1 e é o valor máximo que pode ser feito por um inteiro do WORD. A partir do Excel 2007 executando uma planilha, o valor máximo é 1.048.575 = 2^20 - 1. O RW é definido como um inteiro assinado de 32 bits em XLCALL.H.
  
## <a name="return-value"></a>Valor de retorno

Retorna uma **referência externa xltypeRef** para células de linha passadas. 
  
## <a name="example"></a>Exemplo

Este exemplo usa a **função TempActiveRow12** para selecionar a linha 113. 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempActiveRowExample(void)
{
   Excel12f(xlcSelect, 0, 1, TempActiveRow12(112));
   return 1;
}
```

## <a name="see-also"></a>Confira também



[Funções na biblioteca do Framework](functions-in-the-framework-library.md)

