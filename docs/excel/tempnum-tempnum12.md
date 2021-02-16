---
title: TempNum/TempNum12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempNum
- TempNum12
keywords:
- Função tempnum12 [excel 2007],função TempNum [Excel 2007]
localization_priority: Normal
ms.assetid: 5b74d618-db3a-4d84-bd17-4fee7ae3b51e
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: cabd44ab828a2cfe22253e9aaf12abf7b7709d69
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426629"
---
# <a name="tempnumtempnum12"></a>TempNum/TempNum12

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Função de biblioteca de estrutura que cria um **XLOPER** XLOPER12 temporário contendo um número de planilha do /   Microsoft Excel (um duplo IEEE de 8 byte). 
  
```cs
LPXLOPER TempNum(double d);
LPXLOPER12 TempNum12(double d);
```

## <a name="parameters"></a>Parâmetros

 _d_ (**duplo**)
  
O valor pretendido. Observe que os números sub-normais do IEEE não têm suporte no momento e são arredondados para zero. Há suporte para infinito negativo.
  
## <a name="return-value"></a>Valor de retorno

Retorna um **xltypeNum** numérico contendo o valor passado ou zero se o valor passado era sub-normal. 
  
## <a name="example"></a>Exemplo

Este exemplo usa a **função TempNum12** para passar um argumento para **xlfGetWorkspace**.
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempNumExample(void)
{
   XLOPER12 xRes;
   Excel12f(xlfGetWorkspace, &xRes, 1, TempNum12(44));
   Excel12f(xlFree, 0, 1, (LPXLOPER12)&xRes);
   return 1;
}
```

## <a name="see-also"></a>Confira também



[Funções na biblioteca do Framework](functions-in-the-framework-library.md)

