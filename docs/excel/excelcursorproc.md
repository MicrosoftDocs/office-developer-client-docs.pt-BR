---
title: ExcelCursorProc
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- ExcelCursorProc
keywords:
- função excelcursorproc [excel 2007]
localization_priority: Normal
ms.assetid: 43759617-998d-4030-a17d-c4bbe35ffaf9
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 07be8da4a07b988d5e848048a088859b58ea3a14
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765364"
---
# <a name="excelcursorproc"></a><span data-ttu-id="cd97c-104">ExcelCursorProc</span><span class="sxs-lookup"><span data-stu-id="cd97c-104">ExcelCursorProc</span></span>

 <span data-ttu-id="cd97c-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="cd97c-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="cd97c-106">Quando uma caixa de diálogo restrita for exibida sobre a janela do Microsoft Excel, o cursor é um cursor ocupado sobre a janela do Excel.</span><span class="sxs-lookup"><span data-stu-id="cd97c-106">When a modal dialog box is displayed over the Microsoft Excel window, the cursor is a busy cursor over the Excel window.</span></span> <span data-ttu-id="cd97c-107">Este desvios **WndProc** mensagem WM_SETCURSOR digite mensagens do Windows e alterações de volta o cursor em uma seta normal.</span><span class="sxs-lookup"><span data-stu-id="cd97c-107">This **WndProc** traps WM_SETCURSOR type Windows messages and changes the cursor back to a normal arrow.</span></span> 
  
```cs
LRESULT CALLBACK ExcelCursorProc(HWND hwnd, UINT wMsg, WPARAM wParam, LPARAM lParam);
```

## <a name="parameters"></a><span data-ttu-id="cd97c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cd97c-108">Parameters</span></span>

 <span data-ttu-id="cd97c-109">_hWndDlg_ (**HWND**)</span><span class="sxs-lookup"><span data-stu-id="cd97c-109">_hWndDlg_ (**HWND**)</span></span>
  
<span data-ttu-id="cd97c-110">Contém um manipulador de Windows HWND da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="cd97c-110">Contains the HWND Windows handle of the dialog box.</span></span>
  
 <span data-ttu-id="cd97c-111">_mensagem_ (**UINT**)</span><span class="sxs-lookup"><span data-stu-id="cd97c-111">_message_ (**UINT**)</span></span>
  
<span data-ttu-id="cd97c-112">A mensagem para responder aos.</span><span class="sxs-lookup"><span data-stu-id="cd97c-112">The message to respond to.</span></span>
  
 <span data-ttu-id="cd97c-113">_wParam_ (**WPARAM**)</span><span class="sxs-lookup"><span data-stu-id="cd97c-113">_wParam_ (**WPARAM**)</span></span>
  
 <span data-ttu-id="cd97c-114">_lParam_ (**LPARAM**)</span><span class="sxs-lookup"><span data-stu-id="cd97c-114">_lParam_ (**LPARAM**)</span></span>
  
<span data-ttu-id="cd97c-115">Os argumentos passados pelo Windows.</span><span class="sxs-lookup"><span data-stu-id="cd97c-115">Arguments passed by Windows.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="cd97c-116">Valor de propriedade/Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="cd97c-116">Property value/Return value</span></span>

<span data-ttu-id="cd97c-117">LRESULT: 0 se a mensagem foi tratada, caso contrário, o resultado retornado pelo **WndProc**padrão.</span><span class="sxs-lookup"><span data-stu-id="cd97c-117">LRESULT: 0 if the message was handled, otherwise the result returned by the default **WndProc**.</span></span>
  
### <a name="example"></a><span data-ttu-id="cd97c-118">Exemplo</span><span class="sxs-lookup"><span data-stu-id="cd97c-118">Example</span></span>

<span data-ttu-id="cd97c-119">Consulte `\SAMPLES\GENERIC\GENERIC.C` para o código-fonte para essa função.</span><span class="sxs-lookup"><span data-stu-id="cd97c-119">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="cd97c-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="cd97c-120">See also</span></span>



[<span data-ttu-id="cd97c-121">Funções na DLL genérica</span><span class="sxs-lookup"><span data-stu-id="cd97c-121">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

