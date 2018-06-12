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
- função tempactivecell12 [excel 2007], função TempActiveCell [Excel 2007]
localization_priority: Normal
ms.assetid: ac5a200d-32d5-4313-9a6d-d730032aaf10
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 8ad409a76195d67fa61e7991ce6527c40e0a3265
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765433"
---
# <a name="tempactivecelltempactivecell12"></a>TempActiveCell/TempActiveCell12

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Funções da biblioteca Framework que criam um temporário **XLOPER**/ **XLOPER12** contendo uma referência externa a uma célula na planilha ativa. 
  
```cs
LPXLOPER TempActiveCell(WORD row, BYTE col);
LPXLOPER12 TempActiveCell12(RW row, COL co);
```

## <a name="parameters"></a>Par�metros

 _linha_
  
A linha a ser referenciado. Argumentos de linha são baseada em zero, portanto, essa linha 1 é passada como 0. No Microsoft Office Excel 2003 e anteriores versões e iniciando em uma pasta de trabalho em execução no modo de compatibilidade do Excel 2007, o valor máximo é 65.535 = 2 ^ 16-1 e é o valor máximo que pode ser realizado por um inteiro do WORD. Iniciando no Excel 2007 executando uma pasta de trabalho, o valor máximo é 1.048.575 = 2 ^ 20-1. RW é definido como um inteiro assinado de 32 bits em XLCALL. H.
  
 _col_
  
A coluna a ser referenciado. Isso é baseado em zero que a coluna A é passada como 0. No Excel 2003 e anteriores versões e iniciando em uma pasta de trabalho em execução no modo de compatibilidade do Excel 2007, o valor máximo é de 255 = 2 ^ 8 1 e é o valor máximo que pode ser realizado por um inteiro de bytes. Iniciando no Excel 2007 executando uma pasta de trabalho, o valor máximo é 16,383 = 2 ^ 14-1. COL é definido como um inteiro assinado de 32 bits em XLCALL. H.
  
## <a name="return-value"></a>Valor retornado

Retorna uma referência de **xltypeRef** externo para a célula passada. 
  
## <a name="example"></a>Example

O exemplo a seguir usa **TempActiveCell12** para exibir o conteúdo de B94 na planilha ativa. 
  
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

