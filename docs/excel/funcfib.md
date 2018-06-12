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
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 8d1c97ea57e968aaedffca6b37ded3d875e87413
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765370"
---
# <a name="funcfib"></a>FuncFib

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Função de planilha definida pelo usuário de exemplo que computa o número de Fibonacci enésima. Quando GENERIC.xll é carregado, ele registra esta função para que ele possa ser chamado da planilha.
  
```cs
LPXLOPER12 WINAPI FuncFib (LPXLOPER12 pxN);
```

## <a name="parameters"></a>Par�metros

 _pxN_ (**LPXLOPER12**)
  
O valor de N para o qual o número de Fibonacci enésima é necessário.
  
## <a name="property-valuereturn-value"></a>Propriedade valor/valor de retorno

(**xltypeNum LPXLOPER12** se tiver êxito ou **xltypeErr** caso contrário) 
  
O número de Fibonacci enésima.
  
## <a name="remarks"></a>Coment�rios

A função usa uma variável estática definida dentro do bloco de função, como o valor de retorno **XLOPER12**. Isso não é thread-safe e, portanto essa função e qualquer função de planilha que usa essa estratégia para retornar **XLOPER**s ou s **XLOPER12**, não devem ser registradas como thread-safe iniciada no Excel 2007.
  
### <a name="example"></a>Example

Consulte `\SAMPLES\GENERIC\GENERIC.C` para o código-fonte para essa função. 
  
## <a name="see-also"></a>Confira também



[Funções na DLL genérico](functions-in-the-generic-dll.md)

