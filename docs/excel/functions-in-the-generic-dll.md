---
title: Funções na DLL genérica
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- dll genérica [Excel 2007], funções, funções [Excel 2007], DLL genérica
localization_priority: Normal
ms.assetid: 80ce2247-d69d-45b0-b5e2-4ff0d7078a2c
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 3064e1a09ad8850e121da678f3702a6236574599
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304085"
---
# <a name="functions-in-the-generic-dll"></a>Funções na DLL genérica

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
A pasta `\EXAMPLES\GENERIC\` contém arquivos de projeto do Microsoft Visual Studio e arquivos de código-fonte que são necessários para compilar o exemplo de dll genérico. XLL. Você pode usar esse projeto como modelo para escrever seus próprios XLLs do Microsoft Excel. O código-fonte neste projeto demonstra muitos dos recursos da API do Excel C. 
  
Quando você carrega GENERIC. XLL, ele cria um novo menu **genérico** com quatro comandos: 
  
- **Dialog** : exibe uma caixa de diálogo do Microsoft Excel. 
    
- **Dança** : move a seleção até você pressionar a tecla **ESC** . 
    
- **Diálogo nativo** – exibe uma caixa de diálogo do Windows. 
    
- **Exit** -descarrega Generic. XLL e remove o menu **genérico** . 
    
GENERIC. XLL também fornece três funções de planilha, func1, FuncSum e FuncFib, que podem ser usadas sempre que GENERIC. XLL for carregado. GENERIC. XLL pode ser carregado usando o Gerenciador de suplementos ou é carregado se estava ativo no final normal da última sessão do Excel.
  
Este projeto usa a biblioteca do Framework (FRMWRK32. lib).
  
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

