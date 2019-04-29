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
- função tempint12 [Excel 2007], função TempInt [Excel 2007]
localization_priority: Normal
ms.assetid: 86d690b8-caca-450d-93f7-69ca4cd1a6e0
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 16a2222dbc51ad9480dbd5941ca2ed13f65b55e2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438747"
---
# <a name="tempinttempint12"></a>TempInt/TempInt12

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Função da biblioteca de estrutura que cria um**XLOPER12** **XLOPER**/ temporário que contém um inteiro. 
  
```cs
LPXLOPER TempInt(short int i);
LPXLOPER12 TempInt12(int i);
```

## <a name="parameters"></a>Parâmetros

 _i_
  
O valor inteiro pretendido. Observe que o inteiro **XLOPER** é um inteiro de 16 bits com sinal (int curta), enquanto o inteiro **XLOPER12** é um inteiro de 32 bits assinado ([Long] int). 
  
## <a name="return-value"></a>Valor de retorno

Retorna um inteiro **xltypeInt** que contém o valor passado. 
  
## <a name="example"></a>Exemplo

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

