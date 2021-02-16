---
title: TempActiveRef/TempActiveRef12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempActiveRef
- TempActiveRef12
keywords:
- função tempactiveref [excel 2007],função TempActiveRef12 [Excel 2007]
localization_priority: Normal
ms.assetid: 7c69d15a-294b-4545-983b-720409001e0e
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 58feee8f43e0f90f710c9e4387684dcb6d173a7b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415541"
---
# <a name="tempactivereftempactiveref12"></a>TempActiveRef/TempActiveRef12

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Função de biblioteca de estrutura que cria um /  **XLOPER XLOPER12** temporário contendo uma referência externa ao bloco retangular de células na planilha ativa. 
  
```cs
LPXLOPER TempActiveRef(WORD rwFirst, WORD rwLast, BYTE colFirst, BYTE colLast);
LPXLOPER12 TempActiveRef12(ROW rwFirst, ROW rwLast, COL colFirst, COL colLast);
```

## <a name="parameters"></a>Parâmetros

 _rwFirst_
  
A linha inicial da referência.
  
 _rwLast_
  
A linha final da referência.
  
Os argumentos de linha são baseados em zero para que a linha 1 seja passada como 0. No Microsoft Office Excel 2003 e em versões anteriores, e a partir do Excel 2007 executando uma planilha no modo de compatibilidade, o valor máximo é 65.535 = 2^16 - 1 e é o valor máximo que pode ser feito por um inteiro do WORD. A partir do Excel 2007 executando uma planilha, o valor máximo é 1.048.575 = 2^20 - 1. O RW é definido como um inteiro assinado de 32 bits em XLCALL.H.
  
 _colFirst_
  
O número da coluna inicial da referência.
  
 _colLast_
  
O número da coluna final da referência.
  
Os argumentos de coluna são baseados em zero para que a coluna A seja passada como 0. No Excel 2003 e em versões anteriores, e a partir do Excel 2007 executando uma planilha no modo de compatibilidade, o valor máximo é 255 = 2^8 - 1 e é o valor máximo que pode ser feito por um inteiro BYTE. A partir do Excel 2007 executando uma planilha, o valor máximo é 16.383 = 2^14 - 1. COL é definido como um inteiro assinado de 32 bits em XLCALL.H.
  
## <a name="return-value"></a>Valor de retorno

Retorna uma **referência externa xltypeRef** para o bloco retangular de células passadas. 
  
## <a name="example"></a>Exemplo

Este exemplo usa a **função TempActiveRef12** para selecionar as células A105:C110. 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempActiveRefExample(void)
{
    Excel12f(xlcSelect, 0, 1, TempActiveRef12(104, 109, 0, 2));
    return 1;
}
```

## <a name="see-also"></a>Confira também



[Funções na biblioteca do Framework](functions-in-the-framework-library.md)

