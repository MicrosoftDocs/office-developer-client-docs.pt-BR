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
- função tempnum12 [Excel 2007], função TempNum [Excel 2007]
localization_priority: Normal
ms.assetid: 5b74d618-db3a-4d84-bd17-4fee7ae3b51e
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: cabd44ab828a2cfe22253e9aaf12abf7b7709d69
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310357"
---
# <a name="tempnumtempnum12"></a>TempNum/TempNum12

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
A função da biblioteca de estrutura que cria um **XLOPER de XLOPER**/ **** temporário contendo um número de planilha do Microsoft Excel (um duplo IEEE de 8 bytes). 
  
```cs
LPXLOPER TempNum(double d);
LPXLOPER12 TempNum12(double d);
```

## <a name="parameters"></a>Parâmetros

 _d_ (**duplo**)
  
O valor desejado. Observe que os números do IEEE sub-normal não têm suporte no momento e são arredondados para zero. O infinito negativo é suportado.
  
## <a name="return-value"></a>Valor de retorno

Retorna um **xltypeNum** numérico que contém o valor passado ou zero se o valor passado em é sub-normal. 
  
## <a name="example"></a>Exemplo

Este exemplo usa a função **TempNum12** para passar um argumento para **xlfGetWorkspace**.
  
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

