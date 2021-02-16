---
title: xlSheetId
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlSheetId
keywords:
- função xlsheetid [excel 2007]
localization_priority: Normal
ms.assetid: cb32059c-b899-49cf-8028-ff828998ab75
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: a2ca1bb478c5c985ad7032e30ed0cfe3aef31406
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428428"
---
# <a name="xlsheetid"></a>xlSheetId

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Localiza a ID da planilha de uma planilha nomeada para construir referências externas.
  
```cs
Excel12(xlSheetId, LPXLOPER12 pxRes, 1, LPXLOPER12 pxSheetName);
```

## <a name="parameters"></a>Parâmetros

_pxSheetName_ (**xltypeStr**)
  
(Opcional). O nome do livro e da planilha que você deseja descobrir. Se for omitida, **a função xlSheetId** retornará a ID da planilha ativa (frontal). 
  
## <a name="return-value"></a>Valor de retorno

Retorna a ID da planilha  _em pxRes- \> val.mref.idSheet_. 
  
> [!NOTE]
> O ponteiro da matriz  _pxRes- \> val.mref.lpmref_ é definido como NULL após essa chamada para que não seja necessário chamar **xlFree** para liberar a memória que esse tipo normalmente contém, embora seja completamente seguro fazer isso. 
  
## <a name="remarks"></a>Comentários

A pasta de trabalho que contém a planilha especificada deve estar aberta para usar essa função. Não há como construir uma referência a uma agenda não aberta a partir de uma DLL. Para obter mais informações sobre como usar **xlSheetId** para construir referências, consulte Gerenciamento de Memória no [Excel](memory-management-in-excel.md) para obter exemplos de construção **xltypeRef.** 
  
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

