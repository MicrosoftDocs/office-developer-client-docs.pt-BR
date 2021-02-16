---
title: FuncFib
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- FuncFib
keywords:
- função funcfib [excel 2007]
localization_priority: Normal
ms.assetid: 6a719f04-b2d1-4f87-a227-be561cbd3e49
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: fb8f0c12c27fb2c95007eb5006c1d8b90970f3ad
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423668"
---
# <a name="funcfib"></a>FuncFib

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Exemplo de função de planilha definida pelo usuário que calcula o número Nº 1º Demôniacci. Quando GENERIC.xll é carregado, ele registra essa função para que possa ser chamada a partir da planilha.
  
```cs
LPXLOPER12 WINAPI FuncFib (LPXLOPER12 pxN);
```

## <a name="parameters"></a>Parâmetros

 _pxN_ (**LPXLOPER12**)
  
O valor N para o qual é necessário o número Nº Dem.
  
## <a name="property-valuereturn-value"></a>Valor de propriedade/Valor de retorno

(**xltypeNum LPXLOPER12 se** tiver êxito ou **xltypeErr** caso contrário) 
  
O núm Nº 1º Dememanacci.
  
## <a name="remarks"></a>Comentários

A função usa uma variável estática definida dentro do bloco de função como o valor de retorno **XLOPER12**. Isso não é thread-safe e, portanto, essa função e qualquer função de planilha que use essa estratégia para retornar **XLOPER** s ou **XLOPER12** s, não deve ser registrada como thread-safe a partir do Excel 2007.
  
### <a name="example"></a>Exemplo

Consulte  `\SAMPLES\GENERIC\GENERIC.C` o código-fonte para esta função. 
  
## <a name="see-also"></a>Confira também



[Funções na DLL genérica](functions-in-the-generic-dll.md)

