---
title: xlAbort
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAbort
keywords:
- função xlAbort [Excel 2007]
localization_priority: Normal
ms.assetid: 0fe71454-6b00-464b-8abf-afb209d57754
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 08ab69252520e76a5631c5e32a3970d2d95b1ff4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436654"
---
# <a name="xlabort"></a><span data-ttu-id="24eee-104">xlAbort</span><span class="sxs-lookup"><span data-stu-id="24eee-104">xlAbort</span></span>

 <span data-ttu-id="24eee-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="24eee-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="24eee-106">Gera o processador para outras tarefas no sistema e verifica se o usuário pressionou **ESC** para cancelar uma macro.</span><span class="sxs-lookup"><span data-stu-id="24eee-106">Yields the processor to other tasks in the system and checks whether the user has pressed **ESC** to cancel a macro.</span></span> <span data-ttu-id="24eee-107">Se o usuário pressionou **ESC** durante um recálculo de pasta de trabalho, ele também pode ser detectado de dentro de uma função de planilha chamando essa função.</span><span class="sxs-lookup"><span data-stu-id="24eee-107">If the user has pressed **ESC** during a workbook recalculation, it can also be detected from within a worksheet function by calling this function.</span></span> 
  
```cs
Excel12(xlAbort, LPXLOPER12 pxRes, 1, LPXLOPER12 pxRetain);
```

## <a name="parameters"></a><span data-ttu-id="24eee-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="24eee-108">Parameters</span></span>

 <span data-ttu-id="24eee-109">_pxRetain_ (**xltypeBool**)</span><span class="sxs-lookup"><span data-stu-id="24eee-109">_pxRetain_ (**xltypeBool**)</span></span>
  
<span data-ttu-id="24eee-110">(Opcional).</span><span class="sxs-lookup"><span data-stu-id="24eee-110">(Optional).</span></span> <span data-ttu-id="24eee-111">Se **false**, esta função verifica a condição de interrupção e limpa qualquer quebra pendente.</span><span class="sxs-lookup"><span data-stu-id="24eee-111">If **FALSE**, this function checks for the break condition and clears any pending break.</span></span> <span data-ttu-id="24eee-112">Isso permite que o usuário continue apesar da condição de interrupção.</span><span class="sxs-lookup"><span data-stu-id="24eee-112">This enables the user to continue despite the break condition.</span></span> <span data-ttu-id="24eee-113">Se esse argumento for omitido ou for **true**, a função verificará a anulação do usuário sem limpá-lo.</span><span class="sxs-lookup"><span data-stu-id="24eee-113">If this argument is omitted or is **TRUE**, the function checks for a user abort without clearing it.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="24eee-114">Valor de propriedade/Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="24eee-114">Property value/Return value</span></span>

<span data-ttu-id="24eee-115">Retorna **true** (**xltypeBool**) se o usuário pressionou **ESC**.</span><span class="sxs-lookup"><span data-stu-id="24eee-115">Returns **TRUE** (**xltypeBool**) if the user has pressed **ESC**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="24eee-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="24eee-116">Remarks</span></span>

### 

#### <a name="frequent-calls-may-be-needed"></a><span data-ttu-id="24eee-117">Chamadas frequentes podem ser necessárias</span><span class="sxs-lookup"><span data-stu-id="24eee-117">Frequent Calls May Be Needed</span></span>

<span data-ttu-id="24eee-118">Funções e comandos que podem levar muito tempo devem chamar essa função freqüentemente para gerar o processador para outras tarefas no sistema.</span><span class="sxs-lookup"><span data-stu-id="24eee-118">Functions and commands that could take a long time should call this function frequently to yield the processor to other tasks in the system.</span></span>
  
#### <a name="avoid-sensitive-language"></a><span data-ttu-id="24eee-119">Evitar idioma confidencial</span><span class="sxs-lookup"><span data-stu-id="24eee-119">Avoid Sensitive Language</span></span>

<span data-ttu-id="24eee-120">Evite usar o termo "Abort" em sua interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="24eee-120">Avoid using the term "Abort" in your user interface.</span></span> <span data-ttu-id="24eee-121">Considere usar "Cancelar", "parar", "" quebrar "ou" parar ".</span><span class="sxs-lookup"><span data-stu-id="24eee-121">Consider using "Cancel," "Halt," "Break," or "Stop" instead.</span></span>
  
## <a name="example"></a><span data-ttu-id="24eee-122">Exemplo</span><span class="sxs-lookup"><span data-stu-id="24eee-122">Example</span></span>

<span data-ttu-id="24eee-123">O código a seguir move repetidamente a célula ativa em uma planilha até que um minuto tenha decorrido ou até que o usuário pressione **ESC**.</span><span class="sxs-lookup"><span data-stu-id="24eee-123">The following code repeatedly moves the active cell on a sheet until one minute has elapsed or until the user presses **ESC**.</span></span> <span data-ttu-id="24eee-124">Ele chama a função **xlAbort** ocasionalmente.</span><span class="sxs-lookup"><span data-stu-id="24eee-124">It calls the function **xlAbort** occasionally.</span></span> <span data-ttu-id="24eee-125">Isso gera o processador, facilitando a multitarefas cooperativa.</span><span class="sxs-lookup"><span data-stu-id="24eee-125">This yields the processor, easing cooperative multitasking.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="24eee-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="24eee-126">See also</span></span>



[<span data-ttu-id="24eee-127">Funções da API de C que podem ser chamadas apenas de uma DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="24eee-127">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

