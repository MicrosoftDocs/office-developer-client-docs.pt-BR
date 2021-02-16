---
title: Funções na DLL genérica
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- generic dll [excel 2007], functions,functions [Excel 2007], Generic DLL
localization_priority: Normal
ms.assetid: 80ce2247-d69d-45b0-b5e2-4ff0d7078a2c
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 3064e1a09ad8850e121da678f3702a6236574599
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420595"
---
# <a name="functions-in-the-generic-dll"></a>Funções na DLL genérica

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
A pasta contém arquivos de projeto do Microsoft Visual Studio e arquivos de código-fonte necessários para  `\EXAMPLES\GENERIC\` compilar o exemplo DLL GENERIC.xll. Você pode usar esse projeto como um modelo para escrever seus próprios XLLs do Microsoft Excel. O código-fonte deste projeto demonstra muitos dos recursos da API de C do Excel. 
  
Quando você carrega GENERIC.xll, ele cria um novo menu **Genérico** com quatro comandos: 
  
- **Caixa** de diálogo - Exibe uma caixa de diálogo do Microsoft Excel. 
    
- **Paulo** - Move a seleção até você pressionar a **tecla ESC.** 
    
- **Caixa de diálogo** Nativa - Exibe uma caixa de diálogo do Windows. 
    
- **Exit** - Descarrega GENERIC.xll e remove o menu **Genérico.** 
    
GENERIC.xll also provides three worksheet functions, Func1, FuncSum, and FuncFib, which can be used whenever GENERIC.xll is loaded. GENERIC.xll can be loaded using the Add-in Manager, or it is loaded if it was active at the normal end of the last Excel session.
  
Esse projeto usa a biblioteca de estrutura (FRMWRK32.lib).
  
## <a name="in-this-section"></a>Nesta seção

[DIALOGMsgProc](dialogmsgproc.md)
  
[ExcelCursorProc](excelcursorproc.md)
  
[HookExcelWindow](hookexcelwindow.md)
  
[UnhookExcelWindow](unhookexcelwindow.md)
  
[fShowDialog](fshowdialog.md)
  
[fDance](fdance.md)
  
[fDialog/fDialog12](fdialog-fdialog12.md)
  
[fExit](fexit.md)
  
[Func1](func1.md)
  
[FuncSum](funcsum.md)
  
[FuncFib](funcfib.md)
  
## <a name="see-also"></a>Confira também



[Funções na biblioteca do Framework](functions-in-the-framework-library.md)

