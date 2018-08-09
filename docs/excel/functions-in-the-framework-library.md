---
title: Funções na biblioteca de estrutura
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
keywords:
- funções da biblioteca do Framework [excel 2007] funções [Excel 2007], biblioteca Framework
localization_priority: Normal
ms.assetid: 7d9a13fd-9a4c-423e-bb08-4a5be57c7905
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 1d3878e376f95be3b277f1bb1a59545eb0a631ac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765385"
---
# <a name="functions-in-the-framework-library"></a>Funções na biblioteca de estrutura

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Biblioteca do Framework foi criada para ajudar a tornar escrever XLLs mais fácil. Ele inclui funções simples de gerenciamento **XLOPER**/ **XLOPER12** memória, criando temporário **XLOPER**/ **XLOPER12**, modo eficiente chamar as funções de retorno de chamada do Microsoft Excel (**Excel4**, **Excel4v** * * Excel12 * *, * * Excel12v * *) e a impressão de depuração cadeias de caracteres em um terminal conectado.
  
As funções incluídas nessa biblioteca ajudam a simplificar a um trecho de código que é semelhante ao seguinte.
  
```cs
XLOPER12 xMissing, xBool;
xMissing.xltype = xltypeMissing;
xBool.xltype = xltypeBool;
xBool.val.xbool = 0;
Excel12(xlcDisplay, 0, 2, (LPXLOPER12) &xMissing, (LPXLOPER12) &xBool);
```

O código simplificado se parece com o exemplo a seguir.
  
```cs
Excel12f(xlcDisplay, 0, 2, TempMissing12(), TempBool12(0));
```

As seguintes funções estão incluídas na biblioteca do Framework:
  
||
|:-----|
|[debugPrintf](debugprintf.md) <br/> |
|**GetTempMemory** <br/> |
|**FreeAllTempMemory** <br/> |
|[InitFramework](initframework.md) <br/> |
|[QuitFramework](quitframework.md) <br/> |
   
|**Funções usadas com XLOPERs**|**Funções usadas com XLOPER12s**|
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
   
O uso dessas funções reduz a quantidade de tempo necessária para gravar uma DLL ou XLL. Iniciando o desenvolvimento do aplicativo de exemplo GENÉRICO também reduz o tempo de desenvolvimento. Use GENÉRICO. C como um modelo para ajudar a configurar a estrutura de um XLL e substitua o código existente com seus próprios.
  
Temporário **XLOPER**/ **XLOPER12** funções criar **XLOPER**/ **XLOPER12** valores usando a memória a partir de um local heap gerenciado por biblioteca do Framework. **XLOPER**/ **XLOPER12** valores permanecerão válidos até que você chamar a função **FreeAllTempMemory** ou qualquer uma das funções do **Excel** ou **Excel12f** . (As funções do **Excel** e **Excel12f** livre toda a memória temporária antes de retornar). 
  
Para usar as funções da biblioteca Framework, você deve incluir a FRAMEWRK. H do arquivo em seu código C e adicionar o FRAMEWRK. C ou FRMWRK32. Arquivos de biblioteca para seu projeto de código.
  
## <a name="see-also"></a>Confira também

- [Excel XLL SDK API Function Reference](excel-xll-sdk-api-function-reference.md)

