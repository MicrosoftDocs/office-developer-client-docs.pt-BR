---
title: ExcelCursorProc
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- ExcelCursorProc
keywords:
- função excelcursorproc [excel 2007]
localization_priority: Normal
ms.assetid: 43759617-998d-4030-a17d-c4bbe35ffaf9
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: d3cc41487f0cae31e110249fe148f5370319a39a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432489"
---
# <a name="excelcursorproc"></a>ExcelCursorProc

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Quando uma caixa de diálogo modal é exibida sobre a janela do Microsoft Excel, o cursor é um cursor ocupado sobre a janela do Excel. Este **WndProc** intercepta WM_SETCURSOR digitar mensagens do Windows e altera o cursor de volta para uma seta normal. 
  
```cs
LRESULT CALLBACK ExcelCursorProc(HWND hwnd, UINT wMsg, WPARAM wParam, LPARAM lParam);
```

## <a name="parameters"></a>Parâmetros

 _hWndDlg_ (**HWND**)
  
Contém o alça HWND do Windows da caixa de diálogo.
  
 _message_ (**UINT**)
  
A mensagem à que responder.
  
 _wParam_ (**WPARAM**)
  
 _lParam_ (**LPARAM**)
  
Argumentos passados pelo Windows.
  
## <a name="property-valuereturn-value"></a>Valor de propriedade/Valor de retorno

LRESULT: 0 se a mensagem foi manipulada, caso contrário, o resultado retornado pelo **WndProc padrão.**
  
### <a name="example"></a>Exemplo

Consulte  `\SAMPLES\GENERIC\GENERIC.C` o código-fonte para esta função. 
  
## <a name="see-also"></a>Confira também



[Funções na DLL genérica](functions-in-the-generic-dll.md)

