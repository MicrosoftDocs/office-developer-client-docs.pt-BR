---
title: UnhookExcelWindow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- UnhookExcelWindow
keywords:
- função unhookexcelwindow
localization_priority: Normal
ms.assetid: 6508cb69-0c7c-4d8c-a466-dd79eb13e316
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: aef2734aeb4d9cf5df33e3d012cef309e8a1eb6e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409444"
---
# <a name="unhookexcelwindow"></a>UnhookExcelWindow

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Remove o **ExcelCursorProc** que foi instalado anteriormente pelo **HookExcelWindow**. Isso seria feito para que o **ExcelCursorProc** fosse chamado antes do Microsoft Excel principal **WndProc**.
  
```cs
extern void FAR PASCAL UnhookExcelWindow(HANDLE hWndExcel);
```

## <a name="parameters"></a>Parâmetros

 _hWndExcel_ (**Identificador**)
  
A alça principal do Windows do Excel.
  
## <a name="property-valuereturn-value"></a>Valor de propriedade/Valor de retorno

A função não retorna um valor.
  
## <a name="remarks"></a>Comentários

Essa função restaura o padrão **WndProc** do Excel usando **SetWindowLong ()** para restaurar o endereço que foi salvo pelo **HookExcelWindow ()**.
  
### <a name="example"></a>Exemplo

Consulte `\SAMPLES\GENERIC\GENERIC.C` o código-fonte para essa função. 
  
## <a name="see-also"></a>Confira também



[Funções na DLL genérica](functions-in-the-generic-dll.md)

