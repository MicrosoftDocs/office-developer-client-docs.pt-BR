---
title: xlSheetId
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlSheetId
keywords:
- função xlsheetid [Excel 2007]
localization_priority: Normal
ms.assetid: cb32059c-b899-49cf-8028-ff828998ab75
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: a2ca1bb478c5c985ad7032e30ed0cfe3aef31406
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310301"
---
# <a name="xlsheetid"></a>xlSheetId

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Localiza a ID de uma folha nomeada para criar referências externas.
  
```cs
Excel12(xlSheetId, LPXLOPER12 pxRes, 1, LPXLOPER12 pxSheetName);
```

## <a name="parameters"></a>Parâmetros

_pxSheetName_ (**xltypeStr**)
  
(Opcional). O nome do livro e planilha que você deseja descobrir. Se for omitido, a função **xlSheetId** retornará a ID de planilha da planilha ativa (frontal). 
  
## <a name="return-value"></a>Valor de retorno

Retorna o ID de planilha em _pxRes\>-Val. mref. idSheet_. 
  
> [!NOTE]
> O ponteiro de matriz _pxRes-\>Val. mref. lpmref_ é definido como nulo após esta chamada, de modo que não haja necessidade de chamar **xlFree** para liberar a memória que esse tipo normalmente contém, embora seja totalmente seguro. 
  
## <a name="remarks"></a>Comentários

A pasta de trabalho que contém a folha especificada deve estar aberta para usar essa função. Não há como criar uma referência a uma pasta de trabalho não aberta de uma DLL. Para obter mais informações sobre como usar o **xlSheetId** para construir referências, confira [Gerenciamento de memória no Excel](memory-management-in-excel.md) para obter exemplos de construção **xltypeRef** . 
  
## <a name="example"></a>Exemplo

 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlSheetIdExample(void)
{       
   XLOPER12 xSheetName, xRes;
   xSheetName.xltype = xltypeStr;
   xSheetName.val.str = L"\022[BOOK1.XLSX]Sheet1";
   Excel12(xlSheetId, &xRes, 1, (LPXLOPER12)&xSheetName);
   Excel12f(xlcAlert, 0, 1, TempNum12(xRes.val.mref.idSheet));
   Excel12(xlFree, 0, 1, (LPXLOPER12)&xRes);
   return 1;
}
```

## <a name="see-also"></a>Confira também

- [xlSheetNm](xlsheetnm.md)
- [Funções da API de C que podem ser chamadas apenas de uma DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

