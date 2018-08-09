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
ms.openlocfilehash: 7b70bf4ed0ff45921df407605baa692c7621bca4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765451"
---
# <a name="unhookexcelwindow"></a>UnhookExcelWindow

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Remove o **ExcelCursorProc** instalado anteriormente pelo **HookExcelWindow**. Isso poderia ter sido feito para que **ExcelCursorProc** foi chamado antes do Microsoft Excel principal **WndProc**.
  
```cs
extern void FAR PASCAL UnhookExcelWindow(HANDLE hWndExcel);
```

## <a name="parameters"></a>Parâmetros

 _hWndExcel_ (**Lidar com**)
  
Lidar com as janelas principais do Excel.
  
## <a name="property-valuereturn-value"></a>Valor de propriedade/Valor de retorno

A função não retorna um valor.
  
## <a name="remarks"></a>Comentários

Essa função restaura o padrão de Excel **WndProc** usando **SetWindowLong()** para restaurar o endereço que foi salvo pelo **HookExcelWindow()**.
  
### <a name="example"></a>Exemplo

Consulte `\SAMPLES\GENERIC\GENERIC.C` para o código-fonte para essa função. 
  
## <a name="see-also"></a>Confira também



[Funções na DLL genérica](functions-in-the-generic-dll.md)

