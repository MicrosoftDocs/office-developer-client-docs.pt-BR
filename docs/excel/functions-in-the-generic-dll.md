---
title: Funções na DLL genérica
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- dll genérico [excel 2007], funções, funções [Excel 2007], DLL genérico
localization_priority: Normal
ms.assetid: 80ce2247-d69d-45b0-b5e2-4ff0d7078a2c
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: e78f276e58ca1c98786e28ed5167762cf0bfdf7f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765390"
---
# <a name="functions-in-the-generic-dll"></a><span data-ttu-id="7904b-104">Funções na DLL genérica</span><span class="sxs-lookup"><span data-stu-id="7904b-104">Functions in the Generic DLL</span></span>

 <span data-ttu-id="7904b-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="7904b-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="7904b-106">A pasta `\EXAMPLES\GENERIC\` contém os arquivos de projeto do Microsoft Visual Studio e arquivos de código fonte que são necessários para compilar o exemplo GENERIC.xll DLL.</span><span class="sxs-lookup"><span data-stu-id="7904b-106">The folder  `\EXAMPLES\GENERIC\` contains Microsoft Visual Studio project files and source code files that are needed to compile the example DLL GENERIC.xll.</span></span> <span data-ttu-id="7904b-107">Você pode usar este projeto como modelo para escrever seus próprios XLLs do Excel Microsoft.</span><span class="sxs-lookup"><span data-stu-id="7904b-107">You can use this project as a template for writing your own Microsoft Excel XLLs.</span></span> <span data-ttu-id="7904b-108">O código-fonte deste projeto demonstra muitos dos recursos da API C Excel.</span><span class="sxs-lookup"><span data-stu-id="7904b-108">The source code in this project demonstrates many of the features of the Excel C API.</span></span> 
  
<span data-ttu-id="7904b-109">Quando você carrega GENERIC.xll, ele cria um novo menu **genérico** com quatro comandos:</span><span class="sxs-lookup"><span data-stu-id="7904b-109">When you load GENERIC.xll, it creates a new **Generic** menu with four commands:</span></span> 
  
- <span data-ttu-id="7904b-110">**Diálogo** - exibe uma caixa de diálogo do Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="7904b-110">**Dialog** - Displays a Microsoft Excel dialog box.</span></span> 
    
- <span data-ttu-id="7904b-111">**Festa** - move a seleção em torno até você pressionar a tecla **ESC** .</span><span class="sxs-lookup"><span data-stu-id="7904b-111">**Dance** - Moves the selection around until you press the **ESC** key.</span></span> 
    
- <span data-ttu-id="7904b-112">**Diálogo nativo** - exibe uma caixa de diálogo do Windows.</span><span class="sxs-lookup"><span data-stu-id="7904b-112">**Native Dialog** - Displays a Windows dialog box.</span></span> 
    
- <span data-ttu-id="7904b-113">**Exit** - descarrega GENERIC.xll e remove o menu **genérico** .</span><span class="sxs-lookup"><span data-stu-id="7904b-113">**Exit** - Unloads GENERIC.xll and removes the **Generic** menu.</span></span> 
    
<span data-ttu-id="7904b-114">GENERIC.xll também fornece três funções de planilha, Func1, FuncSum e FuncFib, que pode ser usada sempre que GENERIC.xll é carregado.</span><span class="sxs-lookup"><span data-stu-id="7904b-114">GENERIC.xll also provides three worksheet functions, Func1, FuncSum, and FuncFib, which can be used whenever GENERIC.xll is loaded.</span></span> <span data-ttu-id="7904b-115">GENERIC.xll podem ser carregados usando o Gerenciador de suplemento ou ele será carregado se ele estava ativo no final da última sessão Excel normal.</span><span class="sxs-lookup"><span data-stu-id="7904b-115">GENERIC.xll can be loaded using the Add-in Manager, or it is loaded if it was active at the normal end of the last Excel session.</span></span>
  
<span data-ttu-id="7904b-116">Esse projeto usa a biblioteca de framework (FRMWRK32.lib).</span><span class="sxs-lookup"><span data-stu-id="7904b-116">This project uses the framework library (FRMWRK32.lib).</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="7904b-117">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="7904b-117">In this section</span></span>

[<span data-ttu-id="7904b-118">DIALOGMsgProc</span><span class="sxs-lookup"><span data-stu-id="7904b-118">DIALOGMsgProc</span></span>](dialogmsgproc.md)
  
[<span data-ttu-id="7904b-119">ExcelCursorProc</span><span class="sxs-lookup"><span data-stu-id="7904b-119">ExcelCursorProc</span></span>](excelcursorproc.md)
  
[<span data-ttu-id="7904b-120">HookExcelWindow</span><span class="sxs-lookup"><span data-stu-id="7904b-120">HookExcelWindow</span></span>](hookexcelwindow.md)
  
[<span data-ttu-id="7904b-121">UnhookExcelWindow</span><span class="sxs-lookup"><span data-stu-id="7904b-121">UnhookExcelWindow</span></span>](unhookexcelwindow.md)
  
[<span data-ttu-id="7904b-122">fShowDialog</span><span class="sxs-lookup"><span data-stu-id="7904b-122">fShowDialog</span></span>](fshowdialog.md)
  
[<span data-ttu-id="7904b-123">fDance</span><span class="sxs-lookup"><span data-stu-id="7904b-123">fDance</span></span>](fdance.md)
  
[<span data-ttu-id="7904b-124">fDialog/fDialog12</span><span class="sxs-lookup"><span data-stu-id="7904b-124">fDialog/fDialog12</span></span>](fdialog-fdialog12.md)
  
[<span data-ttu-id="7904b-125">fExit</span><span class="sxs-lookup"><span data-stu-id="7904b-125">fExit</span></span>](fexit.md)
  
[<span data-ttu-id="7904b-126">Func1</span><span class="sxs-lookup"><span data-stu-id="7904b-126">Func1</span></span>](func1.md)
  
[<span data-ttu-id="7904b-127">FuncSum</span><span class="sxs-lookup"><span data-stu-id="7904b-127">FuncSum</span></span>](funcsum.md)
  
[<span data-ttu-id="7904b-128">FuncFib</span><span class="sxs-lookup"><span data-stu-id="7904b-128">FuncFib</span></span>](funcfib.md)
  
## <a name="see-also"></a><span data-ttu-id="7904b-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="7904b-129">See also</span></span>



[<span data-ttu-id="7904b-130">Funções na biblioteca de estrutura</span><span class="sxs-lookup"><span data-stu-id="7904b-130">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

