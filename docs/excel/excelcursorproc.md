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
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 07be8da4a07b988d5e848048a088859b58ea3a14
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765364"
---
# <a name="excelcursorproc"></a>ExcelCursorProc

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Quando uma caixa de diálogo restrita for exibida sobre a janela do Microsoft Excel, o cursor é um cursor ocupado sobre a janela do Excel. Este desvios **WndProc** mensagem WM_SETCURSOR digite mensagens do Windows e alterações de volta o cursor em uma seta normal. 
  
```cs
LRESULT CALLBACK ExcelCursorProc(HWND hwnd, UINT wMsg, WPARAM wParam, LPARAM lParam);
```

## <a name="parameters"></a>Par�metros

 _hWndDlg_ (**HWND**)
  
Contém um manipulador de Windows HWND da caixa de diálogo.
  
 _mensagem_ (**UINT**)
  
A mensagem para responder aos.
  
 _wParam_ (**WPARAM**)
  
 _lParam_ (**LPARAM**)
  
Os argumentos passados pelo Windows.
  
## <a name="property-valuereturn-value"></a>Propriedade valor/valor de retorno

LRESULT: 0 se a mensagem foi tratada, caso contrário, o resultado retornado pelo **WndProc**padrão.
  
### <a name="example"></a>Example

Consulte `\SAMPLES\GENERIC\GENERIC.C` para o código-fonte para essa função. 
  
## <a name="see-also"></a>Confira também



[Funções na DLL genérico](functions-in-the-generic-dll.md)

