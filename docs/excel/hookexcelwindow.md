---
title: HookExcelWindow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- HookExcelWindow
keywords:
- função hookexcelwindow [excel 2007]
localization_priority: Normal
ms.assetid: 13f0ae5e-9951-4e89-a245-7cf68c6f6724
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 8965cc6b1e3d24001c42744f2ee7d447aa4c79b5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765383"
---
# <a name="hookexcelwindow"></a><span data-ttu-id="900db-104">HookExcelWindow</span><span class="sxs-lookup"><span data-stu-id="900db-104">HookExcelWindow</span></span>

 <span data-ttu-id="900db-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="900db-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="900db-106">Instala **ExcelCursorProc** para que ele seja chamado antes que o Microsoft Excel principal **WndProc**.</span><span class="sxs-lookup"><span data-stu-id="900db-106">Installs **ExcelCursorProc** so that it is called before the Microsoft Excel main **WndProc**.</span></span>
  
```cs
extern void FAR PASCAL HookExcelWindow(HANDLE hWndExcel);
```

## <a name="parameters"></a><span data-ttu-id="900db-107">Par�metros</span><span class="sxs-lookup"><span data-stu-id="900db-107">Parameters</span></span>

 <span data-ttu-id="900db-108">_hWndExcel_ (**Lidar com**)</span><span class="sxs-lookup"><span data-stu-id="900db-108">_hWndExcel_ (**HANDLE**)</span></span>
  
<span data-ttu-id="900db-109">Lidar com as janelas principais do Excel.</span><span class="sxs-lookup"><span data-stu-id="900db-109">The Excel main Windows handle.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="900db-110">Propriedade valor/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="900db-110">Property value/Return value</span></span>

<span data-ttu-id="900db-111">A função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="900db-111">The function does not return a value.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="900db-112">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="900db-112">Remarks</span></span>

<span data-ttu-id="900db-113">A função obtém o endereço do Excel **WndProc** devido ao uso de **GetWindowLong()**.</span><span class="sxs-lookup"><span data-stu-id="900db-113">The function obtains the address of the Excel **WndProc** through the use of **GetWindowLong()**.</span></span> <span data-ttu-id="900db-114">Ele armazena esse valor em globais que podem ser usados para chamar o padrão **WndProc** e também para restaurá-lo.</span><span class="sxs-lookup"><span data-stu-id="900db-114">It stores this value in a global that can be used to call the default **WndProc** and also to restore it.</span></span> <span data-ttu-id="900db-115">Finalmente, ele substitui esse endereço com o endereço do **ExcelCursorProc** usando **SetWindowLong()**.</span><span class="sxs-lookup"><span data-stu-id="900db-115">Finally, it replaces this address with the address of **ExcelCursorProc** using **SetWindowLong()**.</span></span>
  
### <a name="example"></a><span data-ttu-id="900db-116">Example</span><span class="sxs-lookup"><span data-stu-id="900db-116">Example</span></span>

<span data-ttu-id="900db-117">Consulte `\SAMPLES\GENERIC\GENERIC.C` para o código-fonte para essa função.</span><span class="sxs-lookup"><span data-stu-id="900db-117">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="900db-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="900db-118">See also</span></span>



[<span data-ttu-id="900db-119">Funções na DLL genérico</span><span class="sxs-lookup"><span data-stu-id="900db-119">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

