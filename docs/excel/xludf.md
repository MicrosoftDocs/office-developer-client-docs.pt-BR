---
title: xlUDF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlUDF
keywords:
- função xlUDF [excel 2007]
localization_priority: Normal
ms.assetid: b608b356-ca5c-47bb-9de8-9b7e2b3924dd
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 8f45f800ca50d2a46792e7cf5e00ac25bd099e8c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765492"
---
# <a name="xludf"></a>xlUDF

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Chama uma função definida pelo usuário (UDF). Essa função permite que uma DLL chamar o Visual Basic para funções definidas pelo usuário do Applications (VBA), funções de idioma de macro XLM e funções registradas contidas em outros complementos.
  
```cs
Excel12(xlUDF, LPXLOPER12 pxRes, int iCount, LPXLOPER12 pxFnRef,
LPXLOPER12 pxArg1, ...);
```

## <a name="parameters"></a>Parâmetros

_pxFnRef_ (**xltypeRef**, **xltypeSRef**, **xltypeStr** ou **xltypeNum**)
  
A referência da função que você deseja chamar. Isso pode ser uma referência de célula de planilha macro, o nome registrado da função como uma cadeia de caracteres ou a ID de registro da função. Para o suplemento funções XLL registradas usando **xlfRegister** ou **registrar** com o argumento _pxFunctionText_ fornecido, a ID pode ser obtida usando **xlfEvaluate** para pesquisar o nome. 
  
_pxArg1,..._
  
Zero ou mais argumentos para a função definida pelo usuário. Quando você chama essa função nas versões anteriores ao Excel 2007, o número máximo de argumentos adicionais que podem ser passados é 29, que é 30 incluindo _pxFnRef_. Iniciando no Excel 2007, esse limite é promovido a 254, que é 255 incluindo _pxFnRef_.
  
## <a name="return-value"></a>Valor retornado

Retorna o valor que a função definida pelo usuário retornada.
  
## <a name="example"></a>Exemplo

O exemplo a seguir executa **TestMacro** na planilha Macro1 na BOOK1. XLS. Certifique-se de que a macro estiver em uma planilha chamada Macro1. 
  
`\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlUDFExample(void)
{       
   XLOPER12 xMacroName, xMacroRef, xRes;
   xMacroName.xltype = xltypeStr;
   xMacroName.val.str = L"\044[BOOK1.XLSX]Macro1!TestMacro";
   Excel12(xlfEvaluate, &xMacroRef, 1, (LPXLOPER12)&xMacroName);
   Excel12(xlUDF, &xRes, 1, (LPXLOPER12)&xMacroRef);
   return 1;
}
```

## <a name="see-also"></a>Confira também

- [Funções da API de C que podem ser chamadas apenas de uma DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

