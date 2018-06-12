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
- função tempactiverow [excel 2007], função TempActiveRow12 [Excel 2007]
localization_priority: Normal
ms.assetid: cbb9181c-59b0-4133-a085-94a94ac3f229
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: a406d6e5a8ffa91e103276cb39230058b4840614
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765434"
---
# <a name="tempactiverowtempactiverow12"></a>TempActiveRow/TempActiveRow12

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Funções da biblioteca Framework que criam um temporário **XLOPER**/ **XLOPER12** contendo uma referência externa para uma linha inteira na planilha ativa. 
  
```cs
LPXLOPER TempActiveRow(WORD row);
LPXLOPER12 TempActiveRow12(ROW row);
```

## <a name="parameters"></a>Par�metros

 _linha_
  
A linha a ser referenciado. Argumentos de linha são baseada em zero, portanto, essa linha 1 é passada como 0. No Microsoft Office Excel 2003 e anteriores versões e iniciando em uma pasta de trabalho em execução no modo de compatibilidade do Excel 2007, o valor máximo é 65.535 = 2 ^ 16-1 e é o valor máximo que pode ser realizado por um inteiro do WORD. Iniciando no Excel 2007 executando uma pasta de trabalho, o valor máximo é 1.048.575 = 2 ^ 20-1. RW é definido como um inteiro assinado de 32 bits em XLCALL. H.
  
## <a name="return-value"></a>Valor retornado

Retorna uma referência de **xltypeRef** externo às células da linha passados. 
  
## <a name="example"></a>Example

Este exemplo usa a função **TempActiveRow12** para selecionar linha 113. 
  
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

