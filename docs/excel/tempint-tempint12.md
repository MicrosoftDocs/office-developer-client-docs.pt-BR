---
title: TempInt/TempInt12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempInt
- TempInt12
keywords:
- função tempint12 [excel 2007], função TempInt [Excel 2007]
localization_priority: Normal
ms.assetid: 86d690b8-caca-450d-93f7-69ca4cd1a6e0
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: eb1dd9be0c0b20e533d9cd8202f8878c43b997be
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765444"
---
# <a name="tempinttempint12"></a>TempInt/TempInt12

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Função da biblioteca de Framework que cria um temporário **XLOPER**/ **XLOPER12** que contém um número inteiro. 
  
```cs
LPXLOPER TempInt(short int i);
LPXLOPER12 TempInt12(int i);
```

## <a name="parameters"></a>Par�metros

 _Eu_
  
O valor de inteiro pretendido. Observe que o inteiro **XLOPER** é um inteiro assinado de 16 bits (short int), enquanto o inteiro **XLOPER12** é um inteiro assinado de 32 bits (int [long]). 
  
## <a name="return-value"></a>Valor retornado

Retorna um inteiro **xltypeInt** contendo o valor passado. 
  
## <a name="example"></a>Example

Este exemplo usa a função **TempInt12** para passar um argumento para **xlfGetWorkspace**.
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempIntExample(void)
{
    XLOPER12 xRes;
    Excel12f(xlfGetWorkspace, (LPXLOPER12)&xRes, 1, TempInt12(44));
    Excel12f(xlFree, 0, 1, (LPXLOPER12)&xRes);
    return 1;
}
```

## <a name="see-also"></a>Confira também



[Funções na biblioteca do Framework](functions-in-the-framework-library.md)

