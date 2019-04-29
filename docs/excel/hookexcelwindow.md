---
title: HookExcelWindow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- HookExcelWindow
keywords:
- função hookexcelwindow [Excel 2007]
localization_priority: Normal
ms.assetid: 13f0ae5e-9951-4e89-a245-7cf68c6f6724
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 4103bf3a95388d20efeb74fcd736aeb5520d0845
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413504"
---
# <a name="hookexcelwindow"></a>HookExcelWindow

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Instala o **ExcelCursorProc** para que seja chamado antes do Microsoft Excel principal **WndProc**.
  
```cs
extern void FAR PASCAL HookExcelWindow(HANDLE hWndExcel);
```

## <a name="parameters"></a>Parâmetros

 _hWndExcel_ (**Identificador**)
  
A alça principal do Windows do Excel.
  
## <a name="property-valuereturn-value"></a>Valor de propriedade/Valor de retorno

A função não retorna um valor.
  
## <a name="remarks"></a>Comentários

A função obtém o endereço do Excel **WndProc** por meio do uso de **GetWindowLong ()**. Ele armazena esse valor em um global que pode ser usado para chamar o **WndProc** padrão e também para restaurá-lo. Por fim, substitui esse endereço pelo endereço de **ExcelCursorProc** usando **SetWindowLong ()**.
  
### <a name="example"></a>Exemplo

Consulte `\SAMPLES\GENERIC\GENERIC.C` o código-fonte para essa função. 
  
## <a name="see-also"></a>Confira também



[Funções na DLL genérica](functions-in-the-generic-dll.md)

