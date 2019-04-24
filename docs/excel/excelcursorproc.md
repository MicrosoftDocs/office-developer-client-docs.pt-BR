---
title: ExcelCursorProc
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- ExcelCursorProc
keywords:
- função excelcursorproc [Excel 2007]
localization_priority: Normal
ms.assetid: 43759617-998d-4030-a17d-c4bbe35ffaf9
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: d3cc41487f0cae31e110249fe148f5370319a39a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304092"
---
# <a name="excelcursorproc"></a><span data-ttu-id="06b49-104">ExcelCursorProc</span><span class="sxs-lookup"><span data-stu-id="06b49-104">ExcelCursorProc</span></span>

 <span data-ttu-id="06b49-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="06b49-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="06b49-106">Quando uma caixa de diálogo modal é exibida sobre a janela do Microsoft Excel, o cursor é um cursor ocupado sobre a janela do Excel.</span><span class="sxs-lookup"><span data-stu-id="06b49-106">When a modal dialog box is displayed over the Microsoft Excel window, the cursor is a busy cursor over the Excel window.</span></span> <span data-ttu-id="06b49-107">Essa WM_SETCURSOR de interceptação **WndProc** digita mensagens do Windows e altera o cursor de volta para uma seta normal.</span><span class="sxs-lookup"><span data-stu-id="06b49-107">This **WndProc** traps WM_SETCURSOR type Windows messages and changes the cursor back to a normal arrow.</span></span> 
  
```cs
LRESULT CALLBACK ExcelCursorProc(HWND hwnd, UINT wMsg, WPARAM wParam, LPARAM lParam);
```

## <a name="parameters"></a><span data-ttu-id="06b49-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="06b49-108">Parameters</span></span>

 <span data-ttu-id="06b49-109">_hWndDlg_ (**HWND**)</span><span class="sxs-lookup"><span data-stu-id="06b49-109">_hWndDlg_ (**HWND**)</span></span>
  
<span data-ttu-id="06b49-110">Contém o identificador de janelas do HWND da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="06b49-110">Contains the HWND Windows handle of the dialog box.</span></span>
  
 <span data-ttu-id="06b49-111">_mensagem_ (**Uint**)</span><span class="sxs-lookup"><span data-stu-id="06b49-111">_message_ (**UINT**)</span></span>
  
<span data-ttu-id="06b49-112">A mensagem a ser respondida.</span><span class="sxs-lookup"><span data-stu-id="06b49-112">The message to respond to.</span></span>
  
 <span data-ttu-id="06b49-113">_wParam_ (**WParam**)</span><span class="sxs-lookup"><span data-stu-id="06b49-113">_wParam_ (**WPARAM**)</span></span>
  
 <span data-ttu-id="06b49-114">_lParam_ (**LParam**)</span><span class="sxs-lookup"><span data-stu-id="06b49-114">_lParam_ (**LPARAM**)</span></span>
  
<span data-ttu-id="06b49-115">Argumentos passados pelo Windows.</span><span class="sxs-lookup"><span data-stu-id="06b49-115">Arguments passed by Windows.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="06b49-116">Valor de propriedade/Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="06b49-116">Property value/Return value</span></span>

<span data-ttu-id="06b49-117">LRESULT: 0 se a mensagem foi tratada, caso contrário, o resultado retornado pelo **WndProc**padrão.</span><span class="sxs-lookup"><span data-stu-id="06b49-117">LRESULT: 0 if the message was handled, otherwise the result returned by the default **WndProc**.</span></span>
  
### <a name="example"></a><span data-ttu-id="06b49-118">Exemplo</span><span class="sxs-lookup"><span data-stu-id="06b49-118">Example</span></span>

<span data-ttu-id="06b49-119">Consulte `\SAMPLES\GENERIC\GENERIC.C` o código-fonte para essa função.</span><span class="sxs-lookup"><span data-stu-id="06b49-119">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="06b49-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="06b49-120">See also</span></span>



[<span data-ttu-id="06b49-121">Funções na DLL genérica</span><span class="sxs-lookup"><span data-stu-id="06b49-121">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

