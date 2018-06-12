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
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 3a69d192babbcf0419850e203f51d8cfd81cdef6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765265"
---
# <a name="dialogmsgproc"></a>DIALOGMsgProc

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Esse procedimento é associado com a caixa de diálogo nativa do Windows que [fShowDialog](fshowdialog.md) exibe. Ele fornece as rotinas de serviço chamadas pelo Windows para a eventos (mensagens) que ocorrem quando o usuário opera em um dos botões, campos de entrada ou controles da caixa de diálogo. 
  
```cs
BOOL CALLBACK DIALOGMsgProc(HWND hWndDlg, UINT message, WPARAM wParam, LPARAM lParam);
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

 **TRUE** se a mensagem processada, **FALSE** se não. 
  
### <a name="example"></a>Example

Consulte `\SAMPLES\GENERIC\GENERIC.C` para o código-fonte para essa função. 
  
## <a name="see-also"></a>Confira também



[Funções na DLL genérico](functions-in-the-generic-dll.md)

