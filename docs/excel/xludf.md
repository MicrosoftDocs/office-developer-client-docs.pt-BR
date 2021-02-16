---
title: xlUDF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlUDF
keywords:
- função xludf [excel 2007]
localization_priority: Normal
ms.assetid: b608b356-ca5c-47bb-9de8-9b7e2b3924dd
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 569334847c7612b86f6ddc967f159e2ef425cbbb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430641"
---
# <a name="xludf"></a>xlUDF

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Chama uma função definida pelo usuário (UDF). Essa função permite que uma DLL chame funções definidas pelo usuário do Visual Basic for Applications (VBA), funções de linguagem de macro XLM e funções registradas contidas em outros complementos.
  
```cs
Excel12(xlUDF, LPXLOPER12 pxRes, int iCount, LPXLOPER12 pxFnRef,
LPXLOPER12 pxArg1, ...);
```

## <a name="parameters"></a>Parâmetros

_pxFnRef_ (**xltypeRef**, **xltypeSRef**, **xltypeStr** ou **xltypeNum**)
  
A referência da função que você deseja chamar. Pode ser uma referência de célula de planilha de macro, o nome registrado da função como uma cadeia de caracteres ou a ID de registro da função. Para funções de complemento XLL registradas usando **xlfRegister** ou **REGISTER** com o argumento  _pxFunctionText_ fornecido, a ID pode ser obtida usando **xlfEvaluate** para procurar o nome. 
  
_pxArg1, ..._
  
Zero ou mais argumentos para a função definida pelo usuário. Quando você está chamando essa função em versões anteriores ao Excel 2007, o número máximo de argumentos adicionais que podem ser passados é 29, que é 30 incluindo  _pxFnRef_. A partir do Excel 2007, esse limite é elevado a 254, que é 255 incluindo  _pxFnRef_.
  
## <a name="return-value"></a>Valor de retorno

Retorna qualquer valor que a função definida pelo usuário tenha retornado.
  
## <a name="example"></a>Exemplo

O exemplo a seguir **executa TestMacro** na planilha Macro1 BOOK1.XLS. Certifique-se de que a macro está em uma planilha chamada Macro1. 
  
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

