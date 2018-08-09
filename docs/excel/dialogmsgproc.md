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
ms.openlocfilehash: 3a69d192babbcf0419850e203f51d8cfd81cdef6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765265"
---
# <a name="dialogmsgproc"></a><span data-ttu-id="9ab66-104">DIALOGMsgProc</span><span class="sxs-lookup"><span data-stu-id="9ab66-104">DIALOGMsgProc</span></span>

<span data-ttu-id="9ab66-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="9ab66-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="9ab66-106">Esse procedimento é associado com a caixa de diálogo nativa do Windows que [fShowDialog](fshowdialog.md) exibe.</span><span class="sxs-lookup"><span data-stu-id="9ab66-106">This procedure is associated with the native Windows dialog box that [fShowDialog](fshowdialog.md) displays.</span></span> <span data-ttu-id="9ab66-107">Ele fornece as rotinas de serviço chamadas pelo Windows para a eventos (mensagens) que ocorrem quando o usuário opera em um dos botões, campos de entrada ou controles da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="9ab66-107">It provides the service routines called by Windows for the events (messages) that occur when the user operates one of the dialog box's buttons, entry fields, or controls.</span></span> 
  
```cs
BOOL CALLBACK DIALOGMsgProc(HWND hWndDlg, UINT message, WPARAM wParam, LPARAM lParam);
```

## <a name="parameters"></a><span data-ttu-id="9ab66-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9ab66-108">Parameters</span></span>

 <span data-ttu-id="9ab66-109">_hWndDlg_ (**HWND**)</span><span class="sxs-lookup"><span data-stu-id="9ab66-109">_hWndDlg_ (**HWND**)</span></span>
  
<span data-ttu-id="9ab66-110">Contém um manipulador de Windows HWND da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="9ab66-110">Contains the HWND Windows handle of the dialog box.</span></span>
  
 <span data-ttu-id="9ab66-111">_mensagem_ (**UINT**)</span><span class="sxs-lookup"><span data-stu-id="9ab66-111">_message_ (**UINT**)</span></span>
  
<span data-ttu-id="9ab66-112">A mensagem para responder aos.</span><span class="sxs-lookup"><span data-stu-id="9ab66-112">The message to respond to.</span></span>
  
 <span data-ttu-id="9ab66-113">_wParam_ (**WPARAM**)</span><span class="sxs-lookup"><span data-stu-id="9ab66-113">_wParam_ (**WPARAM**)</span></span>
  
 <span data-ttu-id="9ab66-114">_lParam_ (**LPARAM**)</span><span class="sxs-lookup"><span data-stu-id="9ab66-114">_lParam_ (**LPARAM**)</span></span>
  
<span data-ttu-id="9ab66-115">Os argumentos passados pelo Windows.</span><span class="sxs-lookup"><span data-stu-id="9ab66-115">Arguments passed by Windows.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="9ab66-116">Valor de propriedade/Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="9ab66-116">Property value/Return value</span></span>

 <span data-ttu-id="9ab66-117">**TRUE** se a mensagem processada, **FALSE** se não.</span><span class="sxs-lookup"><span data-stu-id="9ab66-117">**TRUE** if message processed, **FALSE** if not.</span></span> 
  
### <a name="example"></a><span data-ttu-id="9ab66-118">Exemplo</span><span class="sxs-lookup"><span data-stu-id="9ab66-118">Example</span></span>

<span data-ttu-id="9ab66-119">Consulte `\SAMPLES\GENERIC\GENERIC.C` para o código-fonte para essa função.</span><span class="sxs-lookup"><span data-stu-id="9ab66-119">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9ab66-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="9ab66-120">See also</span></span>



[<span data-ttu-id="9ab66-121">Funções na DLL genérica</span><span class="sxs-lookup"><span data-stu-id="9ab66-121">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

