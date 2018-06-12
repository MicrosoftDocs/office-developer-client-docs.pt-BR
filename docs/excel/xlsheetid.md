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
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: e4e184d4e456ffe26292fe31b1b41463834216f9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765481"
---
# <a name="xlsheetid"></a>xlSheetId

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Localiza a ID de folha de uma planilha nomeada para construir as referências externas.
  
```cs
Excel12(xlSheetId, LPXLOPER12 pxRes, 1, LPXLOPER12 pxSheetName);
```

## <a name="parameters"></a>Par�metros

_pxSheetName_ (**xltypeStr**)
  
(Opcional). O nome do catálogo e folha que você deseja saber sobre. Se for omitido, a função **xlSheetId** retorna a ID de folha da planilha ativa (frente). 
  
## <a name="return-value"></a>Valor retornado

Retorna a ID de folha no _pxRes -\>val.mref.idSheet_. 
  
> [!NOTE]
> O _pxRes -\>val.mref.lpmref_ ponteiro de matriz é definido como NULL após essa chamada para que não é necessário chamar **xlFree** para liberar a memória que normalmente contém esse tipo, embora seja completamente seguro de fazê-lo. 
  
## <a name="remarks"></a>Coment�rios

A pasta de trabalho contendo a planilha especificada deve ser aberta para usar esta função. Não é possível construir uma referência a uma pasta de trabalho não aberta de uma DLL. Para obter mais informações sobre como usar o **xlSheetId** para construir referências, consulte [Gerenciamento de memória no Excel](memory-management-in-excel.md) para obter exemplos de construção de **xltypeRef** . 
  
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
- [Funções da API C que podem ser chamadas apenas por um DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

