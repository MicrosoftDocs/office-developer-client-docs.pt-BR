---
title: Funções na DLL genérico
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- dll genérico [excel 2007], funções, funções [Excel 2007], DLL genérico
localization_priority: Normal
ms.assetid: 80ce2247-d69d-45b0-b5e2-4ff0d7078a2c
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: e78f276e58ca1c98786e28ed5167762cf0bfdf7f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765390"
---
# <a name="functions-in-the-generic-dll"></a>Funções na DLL genérico

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
A pasta `\EXAMPLES\GENERIC\` contém os arquivos de projeto do Microsoft Visual Studio e arquivos de código fonte que são necessários para compilar o exemplo GENERIC.xll DLL. Você pode usar este projeto como modelo para escrever seus próprios XLLs do Excel Microsoft. O código-fonte deste projeto demonstra muitos dos recursos da API C Excel. 
  
Quando você carrega GENERIC.xll, ele cria um novo menu **genérico** com quatro comandos: 
  
- **Diálogo** - exibe uma caixa de diálogo do Microsoft Excel. 
    
- **Festa** - move a seleção em torno até você pressionar a tecla **ESC** . 
    
- **Diálogo nativo** - exibe uma caixa de diálogo do Windows. 
    
- **Exit** - descarrega GENERIC.xll e remove o menu **genérico** . 
    
GENERIC.xll também fornece três funções de planilha, Func1, FuncSum e FuncFib, que pode ser usada sempre que GENERIC.xll é carregado. GENERIC.xll podem ser carregados usando o Gerenciador de suplemento ou ele será carregado se ele estava ativo no final da última sessão Excel normal.
  
Esse projeto usa a biblioteca de framework (FRMWRK32.lib).
  
## <a name="in-this-section"></a>Nesta se��o

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

