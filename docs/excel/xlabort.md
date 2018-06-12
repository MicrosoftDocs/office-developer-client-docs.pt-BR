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
# <a name="xlabort"></a><span data-ttu-id="40177-104">xlAbort</span><span class="sxs-lookup"><span data-stu-id="40177-104">xlAbort</span></span>

 <span data-ttu-id="40177-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="40177-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="40177-106">Gere o processador para outras tarefas no sistema e verifica se o usuário pressiona **ESC** para cancelar uma macro.</span><span class="sxs-lookup"><span data-stu-id="40177-106">Yields the processor to other tasks in the system and checks whether the user has pressed **ESC** to cancel a macro.</span></span> <span data-ttu-id="40177-107">Se o usuário pressiona **ESC** durante um recálculo de pasta de trabalho, ele também pode ser detectado de dentro de uma função de planilha chamando essa função.</span><span class="sxs-lookup"><span data-stu-id="40177-107">If the user has pressed **ESC** during a workbook recalculation, it can also be detected from within a worksheet function by calling this function.</span></span> 
  
```cs
Excel12(xlAbort, LPXLOPER12 pxRes, 1, LPXLOPER12 pxRetain);
```

## <a name="parameters"></a><span data-ttu-id="40177-108">Par�metros</span><span class="sxs-lookup"><span data-stu-id="40177-108">Parameters</span></span>

 <span data-ttu-id="40177-109">_pxRetain_ (**xltypeBool**)</span><span class="sxs-lookup"><span data-stu-id="40177-109">_pxRetain_ (**xltypeBool**)</span></span>
  
<span data-ttu-id="40177-110">(Opcional).</span><span class="sxs-lookup"><span data-stu-id="40177-110">(Optional).</span></span> <span data-ttu-id="40177-111">Se **Falso**, essa função verifica a condição de quebra e limpa qualquer quebra pendente.</span><span class="sxs-lookup"><span data-stu-id="40177-111">If **FALSE**, this function checks for the break condition and clears any pending break.</span></span> <span data-ttu-id="40177-112">Isso permite que o usuário continue apesar a condição de quebra.</span><span class="sxs-lookup"><span data-stu-id="40177-112">This enables the user to continue despite the break condition.</span></span> <span data-ttu-id="40177-113">Se esse argumento for omitido ou for **TRUE**, a função verifica uma anulação de usuário sem limpá-lo.</span><span class="sxs-lookup"><span data-stu-id="40177-113">If this argument is omitted or is **TRUE**, the function checks for a user abort without clearing it.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="40177-114">Propriedade valor/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="40177-114">Property value/Return value</span></span>

<span data-ttu-id="40177-115">Retorna **TRUE** (**xltypeBool**) se o usuário pressionou a **tecla ESC**.</span><span class="sxs-lookup"><span data-stu-id="40177-115">Returns **TRUE** (**xltypeBool**) if the user has pressed **ESC**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="40177-116">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="40177-116">Remarks</span></span>

### 

#### <a name="frequent-calls-may-be-needed"></a><span data-ttu-id="40177-117">Chamadas frequentes podem ser necessários</span><span class="sxs-lookup"><span data-stu-id="40177-117">Frequent Calls May Be Needed</span></span>

<span data-ttu-id="40177-118">Funções e comandos que pode demorar muito tempo devem chamar essa função com frequência para gerar o processador para outras tarefas no sistema.</span><span class="sxs-lookup"><span data-stu-id="40177-118">Functions and commands that could take a long time should call this function frequently to yield the processor to other tasks in the system.</span></span>
  
#### <a name="avoid-sensitive-language"></a><span data-ttu-id="40177-119">Evite idioma confidencial</span><span class="sxs-lookup"><span data-stu-id="40177-119">Avoid Sensitive Language</span></span>

<span data-ttu-id="40177-120">Evite usar o termo "Anulação" em sua interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="40177-120">Avoid using the term "Abort" in your user interface.</span></span> <span data-ttu-id="40177-121">Considere o uso de "Cancelar", "Paralisado e" "Quebrar" ou "Parar" em vez disso.</span><span class="sxs-lookup"><span data-stu-id="40177-121">Consider using "Cancel," "Halt," "Break," or "Stop" instead.</span></span>
  
## <a name="example"></a><span data-ttu-id="40177-122">Example</span><span class="sxs-lookup"><span data-stu-id="40177-122">Example</span></span>

<span data-ttu-id="40177-123">O código a seguir move a célula ativa repetidamente em uma planilha até que um minuto decorrido ou até que o usuário pressionar **ESC**.</span><span class="sxs-lookup"><span data-stu-id="40177-123">The following code repeatedly moves the active cell on a sheet until one minute has elapsed or until the user presses **ESC**.</span></span> <span data-ttu-id="40177-124">Ele chama a função **xlAbort** ocasionalmente.</span><span class="sxs-lookup"><span data-stu-id="40177-124">It calls the function **xlAbort** occasionally.</span></span> <span data-ttu-id="40177-125">Isso produz o processador, facilitando multitarefa cooperativa.</span><span class="sxs-lookup"><span data-stu-id="40177-125">This yields the processor, easing cooperative multitasking.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="40177-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="40177-126">See also</span></span>



[<span data-ttu-id="40177-127">Funções da API C que podem ser chamadas apenas por um DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="40177-127">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

