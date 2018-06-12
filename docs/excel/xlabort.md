---
title: xlAbort
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAbort
keywords:
- função xlAbort [excel 2007]
localization_priority: Normal
ms.assetid: 0fe71454-6b00-464b-8abf-afb209d57754
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: e90cbe496404b4cc602dee1ad21c91c8f5f91bfd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765457"
---
# <a name="xlabort"></a>xlAbort

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Gere o processador para outras tarefas no sistema e verifica se o usuário pressiona **ESC** para cancelar uma macro. Se o usuário pressiona **ESC** durante um recálculo de pasta de trabalho, ele também pode ser detectado de dentro de uma função de planilha chamando essa função. 
  
```cs
Excel12(xlAbort, LPXLOPER12 pxRes, 1, LPXLOPER12 pxRetain);
```

## <a name="parameters"></a>Par�metros

 _pxRetain_ (**xltypeBool**)
  
(Opcional). Se **Falso**, essa função verifica a condição de quebra e limpa qualquer quebra pendente. Isso permite que o usuário continue apesar a condição de quebra. Se esse argumento for omitido ou for **TRUE**, a função verifica uma anulação de usuário sem limpá-lo.
  
## <a name="property-valuereturn-value"></a>Propriedade valor/valor de retorno

Retorna **TRUE** (**xltypeBool**) se o usuário pressionou a **tecla ESC**.
  
## <a name="remarks"></a>Coment�rios

### 

#### <a name="frequent-calls-may-be-needed"></a>Chamadas frequentes podem ser necessários

Funções e comandos que pode demorar muito tempo devem chamar essa função com frequência para gerar o processador para outras tarefas no sistema.
  
#### <a name="avoid-sensitive-language"></a>Evite idioma confidencial

Evite usar o termo "Anulação" em sua interface do usuário. Considere o uso de "Cancelar", "Paralisado e" "Quebrar" ou "Parar" em vez disso.
  
## <a name="example"></a>Example

O código a seguir move a célula ativa repetidamente em uma planilha até que um minuto decorrido ou até que o usuário pressionar **ESC**. Ele chama a função **xlAbort** ocasionalmente. Isso produz o processador, facilitando multitarefa cooperativa. 
  
 `\SAMPLES\GENERIC\GENERIC.C`
  
```cs
int WINAPI fDance(void)
{
   DWORD dtickStart;
   XLOPER12 xAbort, xConfirm;
   int boolSheet;
   int col=0;
   XCHAR rgch[32];
//
// Check what kind of sheet is active. If it is a worksheet or macro
// sheet, this function will move the selection in a loop to show
// activity. In any case, it will update the status bar with a countdown.
//
// Call xlSheetId; if that fails the current sheet is not a macro sheet or
// worksheet. Next, get the time at which to start. Then start a while
// loop that will run for one minute. During the while loop, check if the
// user has pressed ESC. If true, confirm the abort. If the abort is
// confirmed, clear the message bar and return; if the abort is not
// confirmed, clear the abort state and continue. After checking for an
// abort, move the active cell if on a worksheet or macro. Then
// update the status bar with the time remaining.
//
// This block uses TempActiveCell12(), which creates a temporary XLOPER12.
// The XLOPER12 contains a reference to a single cell on the active sheet.
// This function is part of the framework library.
//
   boolSheet = (Excel12f(xlSheetId, 0, 0) == xlretSuccess);
   dtickStart = GetTickCount();
   while (GetTickCount() < dtickStart + 60000L)
   {
      Excel12f(xlAbort, &xAbort, 0);
      if (xAbort.val.xbool)
      {
         Excel12f(xlcAlert, &xConfirm, 2,
           TempStr12(L"Are you sure you want to cancel this operation?"),
              TempNum12(1));
         if (xConfirm.val.xbool)
         {
            Excel12f(xlcMessage, 0, 1, TempBool12(0));
            return 1;
         }
         else
         {
            Excel12f(xlAbort, 0, 1, TempBool12(0));
         }
      }
      if (boolSheet)
      {
         Excel12f(xlcSelect, 0, 1,
            TempActiveCell12(0,(BYTE)col));
         col = (col + 1) & 3;
      }
      wsprintfW(rgch,L"0:%lu",
         (60000 + dtickStart - GetTickCount()) / 1000L);
      Excel12f(xlcMessage, 0, 2, TempBool12(1), TempStr12(rgch));
   }
   Excel12f(xlcMessage, 0, 1, TempBool12(0));
   return 1;
}
```

## <a name="see-also"></a>Confira também



[Funções da API C que podem ser chamadas apenas por um DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

