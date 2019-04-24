---
title: DIALOGMsgProc
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- DIALOGMsgProc
keywords:
- função dialogmsgproc [Excel 2007]
localization_priority: Normal
ms.assetid: 9a538e83-ba34-4806-bb8c-7cda3beb6b66
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 1de1b73f5672067f07518ef3367d77349395a1c3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310959"
---
# <a name="dialogmsgproc"></a><span data-ttu-id="69802-104">DIALOGMsgProc</span><span class="sxs-lookup"><span data-stu-id="69802-104">DIALOGMsgProc</span></span>

<span data-ttu-id="69802-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="69802-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="69802-106">Este procedimento é associado com a caixa de diálogo nativa do Windows que [fShowDialog](fshowdialog.md) é exibida.</span><span class="sxs-lookup"><span data-stu-id="69802-106">This procedure is associated with the native Windows dialog box that [fShowDialog](fshowdialog.md) displays.</span></span> <span data-ttu-id="69802-107">Ele fornece as rotinas de serviço chamadas pelo Windows para os eventos (mensagens) que ocorrem quando o usuário opera um dos botões, campos de entrada ou controles da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="69802-107">It provides the service routines called by Windows for the events (messages) that occur when the user operates one of the dialog box's buttons, entry fields, or controls.</span></span> 
  
```cs
BOOL CALLBACK DIALOGMsgProc(HWND hWndDlg, UINT message, WPARAM wParam, LPARAM lParam);
```

## <a name="parameters"></a><span data-ttu-id="69802-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="69802-108">Parameters</span></span>

 <span data-ttu-id="69802-109">_hWndDlg_ (**HWND**)</span><span class="sxs-lookup"><span data-stu-id="69802-109">_hWndDlg_ (**HWND**)</span></span>
  
<span data-ttu-id="69802-110">Contém o identificador de janelas do HWND da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="69802-110">Contains the HWND Windows handle of the dialog box.</span></span>
  
 <span data-ttu-id="69802-111">_mensagem_ (**Uint**)</span><span class="sxs-lookup"><span data-stu-id="69802-111">_message_ (**UINT**)</span></span>
  
<span data-ttu-id="69802-112">A mensagem a ser respondida.</span><span class="sxs-lookup"><span data-stu-id="69802-112">The message to respond to.</span></span>
  
 <span data-ttu-id="69802-113">_wParam_ (**WParam**)</span><span class="sxs-lookup"><span data-stu-id="69802-113">_wParam_ (**WPARAM**)</span></span>
  
 <span data-ttu-id="69802-114">_lParam_ (**LParam**)</span><span class="sxs-lookup"><span data-stu-id="69802-114">_lParam_ (**LPARAM**)</span></span>
  
<span data-ttu-id="69802-115">Argumentos passados pelo Windows.</span><span class="sxs-lookup"><span data-stu-id="69802-115">Arguments passed by Windows.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="69802-116">Valor de propriedade/Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="69802-116">Property value/Return value</span></span>

 <span data-ttu-id="69802-117">**True** se a mensagem for processada, **false** se não.</span><span class="sxs-lookup"><span data-stu-id="69802-117">**TRUE** if message processed, **FALSE** if not.</span></span> 
  
### <a name="example"></a><span data-ttu-id="69802-118">Exemplo</span><span class="sxs-lookup"><span data-stu-id="69802-118">Example</span></span>

<span data-ttu-id="69802-119">Consulte `\SAMPLES\GENERIC\GENERIC.C` o código-fonte para essa função.</span><span class="sxs-lookup"><span data-stu-id="69802-119">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="69802-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="69802-120">See also</span></span>



[<span data-ttu-id="69802-121">Funções na DLL genérica</span><span class="sxs-lookup"><span data-stu-id="69802-121">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

