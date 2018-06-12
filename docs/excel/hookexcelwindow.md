---
title: HookExcelWindow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- HookExcelWindow
keywords:
- função hookexcelwindow [excel 2007]
localization_priority: Normal
ms.assetid: 13f0ae5e-9951-4e89-a245-7cf68c6f6724
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 8965cc6b1e3d24001c42744f2ee7d447aa4c79b5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765383"
---
# <a name="hookexcelwindow"></a>HookExcelWindow

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Instala **ExcelCursorProc** para que ele seja chamado antes que o Microsoft Excel principal **WndProc**.
  
```cs
extern void FAR PASCAL HookExcelWindow(HANDLE hWndExcel);
```

## <a name="parameters"></a>Par�metros

 _hWndExcel_ (**Lidar com**)
  
Lidar com as janelas principais do Excel.
  
## <a name="property-valuereturn-value"></a>Propriedade valor/valor de retorno

A função não retorna um valor.
  
## <a name="remarks"></a>Coment�rios

A função obtém o endereço do Excel **WndProc** devido ao uso de **GetWindowLong()**. Ele armazena esse valor em globais que podem ser usados para chamar o padrão **WndProc** e também para restaurá-lo. Finalmente, ele substitui esse endereço com o endereço do **ExcelCursorProc** usando **SetWindowLong()**.
  
### <a name="example"></a>Example

Consulte `\SAMPLES\GENERIC\GENERIC.C` para o código-fonte para essa função. 
  
## <a name="see-also"></a>Confira também



[Funções na DLL genérico](functions-in-the-generic-dll.md)

