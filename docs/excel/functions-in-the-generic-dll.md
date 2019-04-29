---
title: Funções na DLL genérica
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- dll genérica [Excel 2007], funções, funções [Excel 2007], DLL genérica
localization_priority: Normal
ms.assetid: 80ce2247-d69d-45b0-b5e2-4ff0d7078a2c
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 3064e1a09ad8850e121da678f3702a6236574599
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420595"
---
# <a name="functions-in-the-generic-dll"></a><span data-ttu-id="89dcd-104">Funções na DLL genérica</span><span class="sxs-lookup"><span data-stu-id="89dcd-104">Functions in the Generic DLL</span></span>

 <span data-ttu-id="89dcd-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="89dcd-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="89dcd-106">A pasta `\EXAMPLES\GENERIC\` contém arquivos de projeto do Microsoft Visual Studio e arquivos de código-fonte que são necessários para compilar o exemplo de dll genérico. XLL.</span><span class="sxs-lookup"><span data-stu-id="89dcd-106">The folder  `\EXAMPLES\GENERIC\` contains Microsoft Visual Studio project files and source code files that are needed to compile the example DLL GENERIC.xll.</span></span> <span data-ttu-id="89dcd-107">Você pode usar esse projeto como modelo para escrever seus próprios XLLs do Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="89dcd-107">You can use this project as a template for writing your own Microsoft Excel XLLs.</span></span> <span data-ttu-id="89dcd-108">O código-fonte neste projeto demonstra muitos dos recursos da API do Excel C.</span><span class="sxs-lookup"><span data-stu-id="89dcd-108">The source code in this project demonstrates many of the features of the Excel C API.</span></span> 
  
<span data-ttu-id="89dcd-109">Quando você carrega GENERIC. XLL, ele cria um novo menu **genérico** com quatro comandos:</span><span class="sxs-lookup"><span data-stu-id="89dcd-109">When you load GENERIC.xll, it creates a new **Generic** menu with four commands:</span></span> 
  
- <span data-ttu-id="89dcd-110">**Dialog** : exibe uma caixa de diálogo do Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="89dcd-110">**Dialog** - Displays a Microsoft Excel dialog box.</span></span> 
    
- <span data-ttu-id="89dcd-111">**Dança** : move a seleção até você pressionar a tecla **ESC** .</span><span class="sxs-lookup"><span data-stu-id="89dcd-111">**Dance** - Moves the selection around until you press the **ESC** key.</span></span> 
    
- <span data-ttu-id="89dcd-112">**Diálogo nativo** – exibe uma caixa de diálogo do Windows.</span><span class="sxs-lookup"><span data-stu-id="89dcd-112">**Native Dialog** - Displays a Windows dialog box.</span></span> 
    
- <span data-ttu-id="89dcd-113">**Exit** -descarrega Generic. XLL e remove o menu **genérico** .</span><span class="sxs-lookup"><span data-stu-id="89dcd-113">**Exit** - Unloads GENERIC.xll and removes the **Generic** menu.</span></span> 
    
<span data-ttu-id="89dcd-114">GENERIC. XLL também fornece três funções de planilha, func1, FuncSum e FuncFib, que podem ser usadas sempre que GENERIC. XLL for carregado.</span><span class="sxs-lookup"><span data-stu-id="89dcd-114">GENERIC.xll also provides three worksheet functions, Func1, FuncSum, and FuncFib, which can be used whenever GENERIC.xll is loaded.</span></span> <span data-ttu-id="89dcd-115">GENERIC. XLL pode ser carregado usando o Gerenciador de suplementos ou é carregado se estava ativo no final normal da última sessão do Excel.</span><span class="sxs-lookup"><span data-stu-id="89dcd-115">GENERIC.xll can be loaded using the Add-in Manager, or it is loaded if it was active at the normal end of the last Excel session.</span></span>
  
<span data-ttu-id="89dcd-116">Este projeto usa a biblioteca do Framework (FRMWRK32. lib).</span><span class="sxs-lookup"><span data-stu-id="89dcd-116">This project uses the framework library (FRMWRK32.lib).</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="89dcd-117">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="89dcd-117">In this section</span></span>

[<span data-ttu-id="89dcd-118">DIALOGMsgProc</span><span class="sxs-lookup"><span data-stu-id="89dcd-118">DIALOGMsgProc</span></span>](dialogmsgproc.md)
  
[<span data-ttu-id="89dcd-119">ExcelCursorProc</span><span class="sxs-lookup"><span data-stu-id="89dcd-119">ExcelCursorProc</span></span>](excelcursorproc.md)
  
[<span data-ttu-id="89dcd-120">HookExcelWindow</span><span class="sxs-lookup"><span data-stu-id="89dcd-120">HookExcelWindow</span></span>](hookexcelwindow.md)
  
[<span data-ttu-id="89dcd-121">UnhookExcelWindow</span><span class="sxs-lookup"><span data-stu-id="89dcd-121">UnhookExcelWindow</span></span>](unhookexcelwindow.md)
  
[<span data-ttu-id="89dcd-122">fShowDialog</span><span class="sxs-lookup"><span data-stu-id="89dcd-122">fShowDialog</span></span>](fshowdialog.md)
  
[<span data-ttu-id="89dcd-123">fDance</span><span class="sxs-lookup"><span data-stu-id="89dcd-123">fDance</span></span>](fdance.md)
  
[<span data-ttu-id="89dcd-124">fDialog/fDialog12</span><span class="sxs-lookup"><span data-stu-id="89dcd-124">fDialog/fDialog12</span></span>](fdialog-fdialog12.md)
  
[<span data-ttu-id="89dcd-125">fExit</span><span class="sxs-lookup"><span data-stu-id="89dcd-125">fExit</span></span>](fexit.md)
  
[<span data-ttu-id="89dcd-126">Func1</span><span class="sxs-lookup"><span data-stu-id="89dcd-126">Func1</span></span>](func1.md)
  
[<span data-ttu-id="89dcd-127">FuncSum</span><span class="sxs-lookup"><span data-stu-id="89dcd-127">FuncSum</span></span>](funcsum.md)
  
[<span data-ttu-id="89dcd-128">FuncFib</span><span class="sxs-lookup"><span data-stu-id="89dcd-128">FuncFib</span></span>](funcfib.md)
  
## <a name="see-also"></a><span data-ttu-id="89dcd-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="89dcd-129">See also</span></span>



[<span data-ttu-id="89dcd-130">Funções na biblioteca do Framework</span><span class="sxs-lookup"><span data-stu-id="89dcd-130">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

