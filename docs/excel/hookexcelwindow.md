---
title: HookExcelWindow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- HookExcelWindow
keywords:
- função hookexcelwindow [Excel 2007]
localization_priority: Normal
ms.assetid: 13f0ae5e-9951-4e89-a245-7cf68c6f6724
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 4103bf3a95388d20efeb74fcd736aeb5520d0845
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310826"
---
# <a name="hookexcelwindow"></a><span data-ttu-id="ee35f-104">HookExcelWindow</span><span class="sxs-lookup"><span data-stu-id="ee35f-104">HookExcelWindow</span></span>

 <span data-ttu-id="ee35f-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="ee35f-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="ee35f-106">Instala o **ExcelCursorProc** para que seja chamado antes do Microsoft Excel principal **WndProc**.</span><span class="sxs-lookup"><span data-stu-id="ee35f-106">Installs **ExcelCursorProc** so that it is called before the Microsoft Excel main **WndProc**.</span></span>
  
```cs
extern void FAR PASCAL HookExcelWindow(HANDLE hWndExcel);
```

## <a name="parameters"></a><span data-ttu-id="ee35f-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ee35f-107">Parameters</span></span>

 <span data-ttu-id="ee35f-108">_hWndExcel_ (**Identificador**)</span><span class="sxs-lookup"><span data-stu-id="ee35f-108">_hWndExcel_ (**HANDLE**)</span></span>
  
<span data-ttu-id="ee35f-109">A alça principal do Windows do Excel.</span><span class="sxs-lookup"><span data-stu-id="ee35f-109">The Excel main Windows handle.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="ee35f-110">Valor de propriedade/Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ee35f-110">Property value/Return value</span></span>

<span data-ttu-id="ee35f-111">A função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="ee35f-111">The function does not return a value.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ee35f-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="ee35f-112">Remarks</span></span>

<span data-ttu-id="ee35f-113">A função obtém o endereço do Excel **WndProc** por meio do uso de **GetWindowLong ()**.</span><span class="sxs-lookup"><span data-stu-id="ee35f-113">The function obtains the address of the Excel **WndProc** through the use of **GetWindowLong()**.</span></span> <span data-ttu-id="ee35f-114">Ele armazena esse valor em um global que pode ser usado para chamar o **WndProc** padrão e também para restaurá-lo.</span><span class="sxs-lookup"><span data-stu-id="ee35f-114">It stores this value in a global that can be used to call the default **WndProc** and also to restore it.</span></span> <span data-ttu-id="ee35f-115">Por fim, substitui esse endereço pelo endereço de **ExcelCursorProc** usando **SetWindowLong ()**.</span><span class="sxs-lookup"><span data-stu-id="ee35f-115">Finally, it replaces this address with the address of **ExcelCursorProc** using **SetWindowLong()**.</span></span>
  
### <a name="example"></a><span data-ttu-id="ee35f-116">Exemplo</span><span class="sxs-lookup"><span data-stu-id="ee35f-116">Example</span></span>

<span data-ttu-id="ee35f-117">Consulte `\SAMPLES\GENERIC\GENERIC.C` o código-fonte para essa função.</span><span class="sxs-lookup"><span data-stu-id="ee35f-117">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ee35f-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="ee35f-118">See also</span></span>



[<span data-ttu-id="ee35f-119">Funções na DLL genérica</span><span class="sxs-lookup"><span data-stu-id="ee35f-119">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

