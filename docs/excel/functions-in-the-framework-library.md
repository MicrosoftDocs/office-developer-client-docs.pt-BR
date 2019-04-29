---
title: Funções na biblioteca do Framework
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
keywords:
- funções da biblioteca do Framework [Excel 2007], funções [Excel 2007], biblioteca de estrutura
localization_priority: Normal
ms.assetid: 7d9a13fd-9a4c-423e-bb08-4a5be57c7905
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 4eeb9e5db09592e98e9afb763efaa6be18eb2f7e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417543"
---
# <a name="functions-in-the-framework-library"></a>Funções na biblioteca do Framework

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
A biblioteca do Framework foi criada para ajudar a facilitar a criação de XLLs. Ele inclui funções simples para gerenciar a memória de**XLOPER12** **XLOPER**/ , criando um **XLOPER de XLOPER**/ **** temporário, chamando de forma robusta as funções de retorno de chamada do Microsoft Excel (**Excel4**, **Excel4v** , * * Excel12 * *, * * Excel12v * *) e imprimindo cadeias de caracteres de depuração em um terminal anexado.
  
As funções incluídas nesta biblioteca ajudam a simplificar uma parte do código semelhante à seguinte.
  
```cs
XLOPER12 xMissing, xBool;
xMissing.xltype = xltypeMissing;
xBool.xltype = xltypeBool;
xBool.val.xbool = 0;
Excel12(xlcDisplay, 0, 2, (LPXLOPER12) &xMissing, (LPXLOPER12) &xBool);
```

O código simplificado é semelhante ao exemplo a seguir.
  
```cs
Excel12f(xlcDisplay, 0, 2, TempMissing12(), TempBool12(0));
```

As funções a seguir estão incluídas na biblioteca da estrutura:
  
||
|:-----|
|[debugPrintf](debugprintf.md) <br/> |
|**GetTempMemory** <br/> |
|**FreeAllTempMemory** <br/> |
|[InitFramework](initframework.md) <br/> |
|[QuitFramework](quitframework.md) <br/> |
   
|**Funções usadas com XLOPERs**|**Funções usadas com o XLOPER12s**|
|:-----|:-----|
|[Excel](excel-excel12f.md) <br/> |[Excel12f](excel-excel12f.md) <br/> |
|[TempNum](tempnum-tempnum12.md) <br/> |[TempNum12](tempnum-tempnum12.md) <br/> |
|[TempStr](tempstr.md) <br/> |[TempStr12](tempstrconst-tempstr12.md) <br/> |
|[TempStrConst](tempstrconst-tempstr12.md) <br/> |[TempStr12Const](tempstrconst-tempstr12.md) <br/> |
|[TempBool](tempbool-tempbool12.md) <br/> |[TempBool12](tempbool-tempbool12.md) <br/> |
|[TempInt](tempint-tempint12.md) <br/> |[TempInt12](tempint-tempint12.md) <br/> |
|[TempErr](temperr-temperr12.md) <br/> |[TempErr12](temperr-temperr12.md) <br/> |
|[TempActiveRef](tempactiveref-tempactiveref12.md) <br/> |[TempActiveRef12](tempactiveref-tempactiveref12.md) <br/> |
|[TempActiveCell](tempactivecell-tempactivecell12.md) <br/> |[TempActiveCell12](tempactivecell-tempactivecell12.md) <br/> |
|[TempActiveRow](tempactiverow-tempactiverow12.md) <br/> |[TempActiveRow12](tempactiverow-tempactiverow12.md) <br/> |
|[TempActiveColumn](tempactivecolumn-tempactivecolumn12.md) <br/> |[TempActiveColumn12](tempactivecolumn-tempactivecolumn12.md) <br/> |
|[TempMissing](tempmissing-tempmissing12.md) <br/> |[TempMissing12](tempmissing-tempmissing12.md) <br/> |
   
O uso dessas funções reduz a quantidade de tempo necessária para gravar uma DLL ou XLL. Iniciar o desenvolvimento do aplicativo de exemplo genérico também reduz o tempo de desenvolvimento. Use genérico. C como um modelo para ajudar a configurar a estrutura de um XLL e, em seguida, substituir o código existente pelo seu próprio.
  
As funções de **XLOPER**/ temporárias do**XLOPER12** criam valores **XLOPER**/ **XLOPER12** usando a memória de uma pilha local gerenciada pela biblioteca do Framework. Os valores de**XLOPER12** **XLOPER**/ permanecem válidos até que você chame a função **FreeAllTempMemory** ou uma das funções do **Excel** ou do **Excel12f** . (As funções **Excel** e **Excel12f** liberam todas as memórias temporárias antes de retornar.) 
  
Para usar as funções da biblioteca do Framework, você deve incluir o FRAMEWRK. H no seu código C e adicione o FRAMEWRK. C ou FRMWRK32. Arquivos LIB no projeto de código.
  
## <a name="see-also"></a>Confira também

- [Excel XLL SDK API Function Reference](excel-xll-sdk-api-function-reference.md)

