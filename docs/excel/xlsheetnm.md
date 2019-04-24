---
title: xlSheetNm
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlSheetNm
keywords:
- função xlsheetnm [Excel 2007]
localization_priority: Normal
ms.assetid: bcb16207-5499-4474-b006-51ccde1002d7
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 5d62be7ebef71547de3a903db4c1a030984b8640
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303868"
---
# <a name="xlsheetnm"></a>xlSheetNm

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Retorna o nome de uma planilha ou folha de macro de sua ID de folha interna contida em uma referência externa ou o nome da planilha atual se for passada uma referência interna.
  
```cs
Excel12(xlSheetNm, LPXLOPER12 pxRes, 1, LPXLOPER12 pxExtref);
```

## <a name="parameters"></a>Parâmetros

_pxExtref_ (**xltypeRef** ou **xltypeSRef**)
  
Uma referência à planilha cujo nome você deseja obter.
  
Se você estiver passando uma referência externa (**xltypeRef**), ela precisará conter apenas a ID da planilha. As estruturas de dados que descrevem as células na planilha são ignoradas e não precisam ser fornecidas. Se a ID estiver definida como zero, **xlSheetNm** retornará o nome da planilha atual. 
  
Se você estiver passando uma referência interna (**xltypeSef**), **xlSheetNm** retornará o nome da planilha atual. 
  
## <a name="property-valuereturn-value"></a>Valor de propriedade/Valor de retorno

Retorna o nome da planilha (**xltypeStr**) no formulário `[Book1]Sheet1`.
  
## <a name="example"></a>Exemplo

O exemplo a seguir exibe o nome da planilha a partir da qual a função foi chamada. A função funciona corretamente somente se for chamado a partir de uma planilha de macro durante a execução de uma macro de comando XLM. Isso ocorre porque ele chama **xlcAlert**, que somente os comandos podem fazer, e precisa ser chamado a partir de uma planilha em vez de uma caixa de diálogo, menu ou barra de comandos para que o **xlfCaller** retorne uma referência. 
  
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
- [Funções da API de C que podem ser chamadas apenas de uma DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

