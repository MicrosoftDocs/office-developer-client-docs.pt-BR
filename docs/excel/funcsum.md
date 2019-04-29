---
title: FuncSum
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- FuncSum
keywords:
- função funcsum [Excel 2007]
localization_priority: Normal
ms.assetid: 934192ef-8a89-4dbb-bd37-01e92ba24256
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 14db5812165812161cf7031f75338a981251dfd2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406938"
---
# <a name="funcsum"></a>FuncSum

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Exemplo de função de planilha definida pelo usuário que leva de 1 a 29 argumentos e computa sua soma. Cada argumento pode ser um número único, um intervalo ou uma matriz. Quando GENERIC. XLL é carregado, ele registra essa função para que ela possa ser chamada da planilha. 
  
```cs
LPXLOPER12 WINAPI FuncSum(LPXLOPER12 px1, LPXLOPER12 px2, LPXLOPER12 px3,LPXLOPER12 px4, LPXLOPER12 px5, LPXLOPER12 px6, LPXLOPER12 px7,LPXLOPER12 px8, LPXLOPER12 px9, LPXLOPER12 px10, LPXLOPER12 px11,LPXLOPER12 px12, LPXLOPER12 px13, LPXLOPER12 px14, LPXLOPER12 px15,LPXLOPER12 px16, LPXLOPER12 px17, LPXLOPER12 px18, LPXLOPER12 px19,LPXLOPER12 px20, LPXLOPER12 px21, LPXLOPER12 px22, LPXLOPER12 px23,LPXLOPER12 px24, LPXLOPER12 px25, LPXLOPER12 px26, LPXLOPER12 px27,LPXLOPER12 px28, LPXLOPER12 px29);
```

## <a name="parameters"></a>Parâmetros

 _PX1-px29_ (**LPXLOPER12**)
  
Ponteiros para argumentos **XLOPER12** . A função aceita qualquer tipo de tipo de entrada, mas é codificada apenas para operar em números, matrizes literais de números e intervalos que contenham apenas números ou células em branco. Se forem fornecidos menos de 29 argumentos, os argumentos restantes serão fornecidos como **xltypeMissing**.
  
## <a name="property-valuereturn-value"></a>Valor de propriedade/Valor de retorno

(**LPXLOPER12 xltypeNum** ou **xltypeErr**)
  
A soma dos argumentos ou #VALUE! Se houver não numéricos na lista de argumentos fornecidos ou em uma célula em um intervalo ou elemento em uma matriz.
  
### <a name="example"></a>Exemplo

Consulte `\SAMPLES\GENERIC\GENERIC.C` o código-fonte para essa função. 
  
## <a name="see-also"></a>Confira também



[Funções na DLL genérica](functions-in-the-generic-dll.md)

