---
title: xlSheetNm
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlSheetNm
keywords:
- função xlsheetnm [excel 2007]
localization_priority: Normal
ms.assetid: bcb16207-5499-4474-b006-51ccde1002d7
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 815565d886b1aea203f6b3b9774325d6b534abd2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765491"
---
# <a name="xlsheetnm"></a>xlSheetNm

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Retorna o nome de uma planilha ou folha de macro da sua ID de planilha interna contida em uma referência externa ou o nome da planilha atual se passar uma referência interna.
  
```cs
Excel12(xlSheetNm, LPXLOPER12 pxRes, 1, LPXLOPER12 pxExtref);
```

## <a name="parameters"></a>Par�metros

_pxExtref_ (**xltypeRef** ou **xltypeSRef**)
  
Uma referência à planilha cujo nome desejado.
  
Se você estiver passando uma referência externa (**xltypeRef**), ele precisa conter apenas a ID da folha. As estruturas de dados que descrevem as células na planilha são ignoradas e não precisam ser fornecido. Se a ID estiver definida como zero, **xlSheetNm** retorna o nome da planilha atual. 
  
Se você estiver passando uma referência interna (**xltypeSef**), **xlSheetNm** retorna o nome da planilha atual. 
  
## <a name="property-valuereturn-value"></a>Propriedade valor/valor de retorno

Retorna o nome da planilha (**xltypeStr**) no formato `[Book1]Sheet1`.
  
## <a name="example"></a>Example

O exemplo a seguir exibe o nome da planilha do qual a função foi chamada. A função funciona corretamente somente se chamado a partir de uma folha de macro durante a execução de um comando de macro XLM. Isso acontece porque ele chama **xlcAlert**, que podem ser feito apenas comandos e, em seguida, ele precisa ser chamado a partir de uma planilha em vez de uma caixa de diálogo, menu ou barra de comandos na ordem para **xlfCaller** retornar uma referência. 
  
`\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlSheetNmExample(void)
{
   XLOPER12 xRes, xSheetName;
   Excel12(xlfCaller, &xRes, 0);
   Excel12(xlSheetNm, &xSheetName, 1, (LPXLOPER12)&xRes);
   Excel12(xlcAlert, 0, 1, (LPXLOPER12)&xSheetName);
   Excel12(xlFree, 0, 1, (LPXLOPER12)&xSheetName);
   return 1;
}
```

## <a name="see-also"></a>Confira também

- [xlSheetId](xlsheetid.md)
- [Funções da API C que podem ser chamadas apenas por um DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

