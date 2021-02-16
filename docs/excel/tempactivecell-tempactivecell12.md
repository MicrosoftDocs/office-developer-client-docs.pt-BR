---
title: TempActiveCell/TempActiveCell12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempActiveCell
- TempActiveCell12
keywords:
- função tempactivecell12 [excel 2007],função TempActiveCell [Excel 2007]
localization_priority: Normal
ms.assetid: ac5a200d-32d5-4313-9a6d-d730032aaf10
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: f9bdb4cd9919d0e52654a3996ede99c4d1b35cc6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413189"
---
# <a name="tempactivecelltempactivecell12"></a>TempActiveCell/TempActiveCell12

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Funções de biblioteca de estrutura que criam um /  **XLOPER XLOPER12** temporário contendo uma referência externa a uma célula na planilha ativa. 
  
```cs
LPXLOPER TempActiveCell(WORD row, BYTE col);
LPXLOPER12 TempActiveCell12(RW row, COL co);
```

## <a name="parameters"></a>Parâmetros

 _row_
  
A linha a ser referenciada. Os argumentos de linha são baseados em zero para que a linha 1 seja passada como 0. No Microsoft Office Excel 2003 e em versões anteriores, e a partir do Excel 2007 executando uma planilha no modo de compatibilidade, o valor máximo é 65.535 = 2^16 - 1 e é o valor máximo que pode ser feito por um inteiro do WORD. A partir do Excel 2007 executando uma planilha, o valor máximo é 1.048.575 = 2^20 - 1. O RW é definido como um inteiro assinado de 32 bits em XLCALL.H.
  
 _col_
  
A coluna a ser referenciada. Isso é baseado em zero para que a coluna A seja passada como 0. No Excel 2003 e em versões anteriores, e a partir do Excel 2007 executando uma planilha no modo de compatibilidade, o valor máximo é 255 = 2^8 - 1 e é o valor máximo que pode ser feito por um inteiro BYTE. A partir do Excel 2007 executando uma planilha, o valor máximo é 16.383 = 2^14 - 1. COL é definido como um inteiro assinado de 32 bits em XLCALL.H.
  
## <a name="return-value"></a>Valor de retorno

Retorna uma **referência externa xltypeRef** para a célula passada. 
  
## <a name="example"></a>Exemplo

O exemplo a seguir **usa TempActiveCell12** para exibir o conteúdo de B94 na planilha ativa. 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempActiveCellExample(void)
{
   Excel12f(xlcAlert, 0, 1, TempActiveCell12(93,1));
   return 1;
}
```

## <a name="see-also"></a>Confira também



[Funções na biblioteca do Framework](functions-in-the-framework-library.md)

