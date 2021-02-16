---
title: DIALOGMsgProc
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- DIALOGMsgProc
keywords:
- função dialogmsgproc [excel 2007]
localization_priority: Normal
ms.assetid: 9a538e83-ba34-4806-bb8c-7cda3beb6b66
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 1de1b73f5672067f07518ef3367d77349395a1c3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406511"
---
# <a name="dialogmsgproc"></a>DIALOGMsgProc

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Esse procedimento é associado à caixa de diálogo nativa do Windows exibida [por fShowDialog.](fshowdialog.md) Ele fornece as rotinas de serviço chamadas pelo Windows para os eventos (mensagens) que ocorrem quando o usuário opera um dos botões, campos de entrada ou controles da caixa de diálogo. 
  
```cs
BOOL CALLBACK DIALOGMsgProc(HWND hWndDlg, UINT message, WPARAM wParam, LPARAM lParam);
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

 **TRUE** se a mensagem for **processada, FALSE** se não. 
  
### <a name="example"></a>Exemplo

Consulte  `\SAMPLES\GENERIC\GENERIC.C` o código-fonte para esta função. 
  
## <a name="see-also"></a>Confira também



[Funções na DLL genérica](functions-in-the-generic-dll.md)

