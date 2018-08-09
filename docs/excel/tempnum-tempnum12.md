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
- função tempnum12 [excel 2007], função TempNum [Excel 2007]
localization_priority: Normal
ms.assetid: 5b74d618-db3a-4d84-bd17-4fee7ae3b51e
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 5ebe58dba32c2cf0382bf0811713eaa0a5471dda
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765441"
---
# <a name="tempnumtempnum12"></a>TempNum/TempNum12

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Função da biblioteca de Framework que cria um temporário **XLOPER**/ **XLOPER12** contendo um número de planilha do Microsoft Excel (um double IEEE de 8 bytes). 
  
```cs
LPXLOPER TempNum(double d);
LPXLOPER12 TempNum12(double d);
```

## <a name="parameters"></a>Parâmetros

 _d_ (**double**)
  
O valor desejado. Observe que os números de sub-recursos normais padrão IEEE não são suportados atualmente e são arredondados para zero. Há suporte para infinito negativo.
  
## <a name="return-value"></a>Valor retornado

Retorna numéricos **xltypeNum** contendo o valor passado ou zero se o valor passado na era sub-recursos normal. 
  
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



[Funções na biblioteca de estrutura](functions-in-the-framework-library.md)

