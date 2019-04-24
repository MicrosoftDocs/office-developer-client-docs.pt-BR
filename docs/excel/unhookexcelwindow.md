---
title: UnhookExcelWindow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- UnhookExcelWindow
keywords:
- função unhookexcelwindow
localization_priority: Normal
ms.assetid: 6508cb69-0c7c-4d8c-a466-dd79eb13e316
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: aef2734aeb4d9cf5df33e3d012cef309e8a1eb6e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310308"
---
# <a name="unhookexcelwindow"></a><span data-ttu-id="09da8-104">UnhookExcelWindow</span><span class="sxs-lookup"><span data-stu-id="09da8-104">UnhookExcelWindow</span></span>

 <span data-ttu-id="09da8-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="09da8-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="09da8-106">Remove o **ExcelCursorProc** que foi instalado anteriormente pelo **HookExcelWindow**.</span><span class="sxs-lookup"><span data-stu-id="09da8-106">Removes the **ExcelCursorProc** that was previously installed by **HookExcelWindow**.</span></span> <span data-ttu-id="09da8-107">Isso seria feito para que o **ExcelCursorProc** fosse chamado antes do Microsoft Excel principal **WndProc**.</span><span class="sxs-lookup"><span data-stu-id="09da8-107">This would have been done so that **ExcelCursorProc** was called before the Microsoft Excel main **WndProc**.</span></span>
  
```cs
extern void FAR PASCAL UnhookExcelWindow(HANDLE hWndExcel);
```

## <a name="parameters"></a><span data-ttu-id="09da8-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="09da8-108">Parameters</span></span>

 <span data-ttu-id="09da8-109">_hWndExcel_ (**Identificador**)</span><span class="sxs-lookup"><span data-stu-id="09da8-109">_hWndExcel_ (**HANDLE**)</span></span>
  
<span data-ttu-id="09da8-110">A alça principal do Windows do Excel.</span><span class="sxs-lookup"><span data-stu-id="09da8-110">The Excel main Windows handle.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="09da8-111">Valor de propriedade/Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="09da8-111">Property value/Return value</span></span>

<span data-ttu-id="09da8-112">A função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="09da8-112">The function does not return a value.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="09da8-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="09da8-113">Remarks</span></span>

<span data-ttu-id="09da8-114">Essa função restaura o padrão **WndProc** do Excel usando **SetWindowLong ()** para restaurar o endereço que foi salvo pelo **HookExcelWindow ()**.</span><span class="sxs-lookup"><span data-stu-id="09da8-114">This function restores the Excel default **WndProc** using **SetWindowLong()** to restore the address that was saved by **HookExcelWindow()**.</span></span>
  
### <a name="example"></a><span data-ttu-id="09da8-115">Exemplo</span><span class="sxs-lookup"><span data-stu-id="09da8-115">Example</span></span>

<span data-ttu-id="09da8-116">Consulte `\SAMPLES\GENERIC\GENERIC.C` o código-fonte para essa função.</span><span class="sxs-lookup"><span data-stu-id="09da8-116">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="09da8-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="09da8-117">See also</span></span>



[<span data-ttu-id="09da8-118">Funções na DLL genérica</span><span class="sxs-lookup"><span data-stu-id="09da8-118">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

