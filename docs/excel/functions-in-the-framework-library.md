---
title: Funções na Biblioteca de Estrutura
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
keywords:
- funções de biblioteca de estrutura [excel 2007],funções [Excel 2007], biblioteca de estrutura
localization_priority: Normal
ms.assetid: 7d9a13fd-9a4c-423e-bb08-4a5be57c7905
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 4eeb9e5db09592e98e9afb763efaa6be18eb2f7e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417543"
---
# <a name="functions-in-the-framework-library"></a><span data-ttu-id="174b3-104">Funções na Biblioteca de Estrutura</span><span class="sxs-lookup"><span data-stu-id="174b3-104">Functions in the Framework Library</span></span>

<span data-ttu-id="174b3-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="174b3-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="174b3-106">A Biblioteca de Estruturas foi criada para ajudar a facilitar a escrita de XLLs.</span><span class="sxs-lookup"><span data-stu-id="174b3-106">The Framework Library was created to help make writing XLLs easier.</span></span> <span data-ttu-id="174b3-107">Ele inclui funções simples para gerenciar a memória **XLOPER** XLOPER12, criar xlOPER XLOPER12 temporário , chamando robustamente as funções de retorno de chamada do /   Microsoft Excel  /  (**Excel4**, **Excel4v**, \*\* Excel12 \*\*, \*\* Excel12v \*\*) e imprimir cadeias de caracteres de depuração em um terminal anexado.</span><span class="sxs-lookup"><span data-stu-id="174b3-107">It includes simple functions for managing **XLOPER**/ **XLOPER12** memory, creating temporary **XLOPER**/ **XLOPER12**, robustly calling the Microsoft Excel callback functions (**Excel4**, **Excel4v**, \*\* Excel12 \*\*, \*\* Excel12v \*\*) and printing debugging strings on an attached terminal.</span></span>
  
<span data-ttu-id="174b3-108">As funções incluídas nesta biblioteca ajudam a simplificar uma parte do código semelhante à seguinte.</span><span class="sxs-lookup"><span data-stu-id="174b3-108">The functions included in this library help simplify a piece of code that looks like the following.</span></span>
  
```cs
XLOPER12 xMissing, xBool;
xMissing.xltype = xltypeMissing;
xBool.xltype = xltypeBool;
xBool.val.xbool = 0;
Excel12(xlcDisplay, 0, 2, (LPXLOPER12) &xMissing, (LPXLOPER12) &xBool);
```

<span data-ttu-id="174b3-109">O código simplificado se parece com o exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="174b3-109">The simplified code looks like the following example.</span></span>
  
```cs
Excel12f(xlcDisplay, 0, 2, TempMissing12(), TempBool12(0));
```

<span data-ttu-id="174b3-110">As seguintes funções estão incluídas na biblioteca do Framework:</span><span class="sxs-lookup"><span data-stu-id="174b3-110">The following functions are included in the Framework library:</span></span>
  
||
|:-----|
|[<span data-ttu-id="174b3-111">debugPrintf</span><span class="sxs-lookup"><span data-stu-id="174b3-111">debugPrintf</span></span>](debugprintf.md) <br/> |
|<span data-ttu-id="174b3-112">**GetTempMemory**</span><span class="sxs-lookup"><span data-stu-id="174b3-112">**GetTempMemory**</span></span> <br/> |
|<span data-ttu-id="174b3-113">**FreeAllTempMemory**</span><span class="sxs-lookup"><span data-stu-id="174b3-113">**FreeAllTempMemory**</span></span> <br/> |
|[<span data-ttu-id="174b3-114">InitFramework</span><span class="sxs-lookup"><span data-stu-id="174b3-114">InitFramework</span></span>](initframework.md) <br/> |
|[<span data-ttu-id="174b3-115">QuitFramework</span><span class="sxs-lookup"><span data-stu-id="174b3-115">QuitFramework</span></span>](quitframework.md) <br/> |
   
|<span data-ttu-id="174b3-116">**Funções usadas com XLOPERs**</span><span class="sxs-lookup"><span data-stu-id="174b3-116">**Functions Used with XLOPERs**</span></span>|<span data-ttu-id="174b3-117">**Funções usadas com XLOPER12s**</span><span class="sxs-lookup"><span data-stu-id="174b3-117">**Functions Used with XLOPER12s**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="174b3-118">Excel</span><span class="sxs-lookup"><span data-stu-id="174b3-118">Excel</span></span>](excel-excel12f.md) <br/> |[<span data-ttu-id="174b3-119">Excel12f</span><span class="sxs-lookup"><span data-stu-id="174b3-119">Excel12f</span></span>](excel-excel12f.md) <br/> |
|[<span data-ttu-id="174b3-120">TempNum</span><span class="sxs-lookup"><span data-stu-id="174b3-120">TempNum</span></span>](tempnum-tempnum12.md) <br/> |[<span data-ttu-id="174b3-121">TempNum12</span><span class="sxs-lookup"><span data-stu-id="174b3-121">TempNum12</span></span>](tempnum-tempnum12.md) <br/> |
|[<span data-ttu-id="174b3-122">TempStr</span><span class="sxs-lookup"><span data-stu-id="174b3-122">TempStr</span></span>](tempstr.md) <br/> |[<span data-ttu-id="174b3-123">TempStr12</span><span class="sxs-lookup"><span data-stu-id="174b3-123">TempStr12</span></span>](tempstrconst-tempstr12.md) <br/> |
|[<span data-ttu-id="174b3-124">TempStrConst</span><span class="sxs-lookup"><span data-stu-id="174b3-124">TempStrConst</span></span>](tempstrconst-tempstr12.md) <br/> |[<span data-ttu-id="174b3-125">TempStr12Const</span><span class="sxs-lookup"><span data-stu-id="174b3-125">TempStr12Const</span></span>](tempstrconst-tempstr12.md) <br/> |
|[<span data-ttu-id="174b3-126">TempBool</span><span class="sxs-lookup"><span data-stu-id="174b3-126">TempBool</span></span>](tempbool-tempbool12.md) <br/> |[<span data-ttu-id="174b3-127">TempBool12</span><span class="sxs-lookup"><span data-stu-id="174b3-127">TempBool12</span></span>](tempbool-tempbool12.md) <br/> |
|[<span data-ttu-id="174b3-128">TempInt</span><span class="sxs-lookup"><span data-stu-id="174b3-128">TempInt</span></span>](tempint-tempint12.md) <br/> |[<span data-ttu-id="174b3-129">TempInt12</span><span class="sxs-lookup"><span data-stu-id="174b3-129">TempInt12</span></span>](tempint-tempint12.md) <br/> |
|[<span data-ttu-id="174b3-130">TempErr</span><span class="sxs-lookup"><span data-stu-id="174b3-130">TempErr</span></span>](temperr-temperr12.md) <br/> |[<span data-ttu-id="174b3-131">TempErr12</span><span class="sxs-lookup"><span data-stu-id="174b3-131">TempErr12</span></span>](temperr-temperr12.md) <br/> |
|[<span data-ttu-id="174b3-132">TempActiveRef</span><span class="sxs-lookup"><span data-stu-id="174b3-132">TempActiveRef</span></span>](tempactiveref-tempactiveref12.md) <br/> |[<span data-ttu-id="174b3-133">TempActiveRef12</span><span class="sxs-lookup"><span data-stu-id="174b3-133">TempActiveRef12</span></span>](tempactiveref-tempactiveref12.md) <br/> |
|[<span data-ttu-id="174b3-134">TempActiveCell</span><span class="sxs-lookup"><span data-stu-id="174b3-134">TempActiveCell</span></span>](tempactivecell-tempactivecell12.md) <br/> |[<span data-ttu-id="174b3-135">TempActiveCell12</span><span class="sxs-lookup"><span data-stu-id="174b3-135">TempActiveCell12</span></span>](tempactivecell-tempactivecell12.md) <br/> |
|[<span data-ttu-id="174b3-136">TempActiveRow</span><span class="sxs-lookup"><span data-stu-id="174b3-136">TempActiveRow</span></span>](tempactiverow-tempactiverow12.md) <br/> |[<span data-ttu-id="174b3-137">TempActiveRow12</span><span class="sxs-lookup"><span data-stu-id="174b3-137">TempActiveRow12</span></span>](tempactiverow-tempactiverow12.md) <br/> |
|[<span data-ttu-id="174b3-138">TempActiveColumn</span><span class="sxs-lookup"><span data-stu-id="174b3-138">TempActiveColumn</span></span>](tempactivecolumn-tempactivecolumn12.md) <br/> |[<span data-ttu-id="174b3-139">TempActiveColumn12</span><span class="sxs-lookup"><span data-stu-id="174b3-139">TempActiveColumn12</span></span>](tempactivecolumn-tempactivecolumn12.md) <br/> |
|[<span data-ttu-id="174b3-140">TempMissing</span><span class="sxs-lookup"><span data-stu-id="174b3-140">TempMissing</span></span>](tempmissing-tempmissing12.md) <br/> |[<span data-ttu-id="174b3-141">TempMissing12</span><span class="sxs-lookup"><span data-stu-id="174b3-141">TempMissing12</span></span>](tempmissing-tempmissing12.md) <br/> |
   
<span data-ttu-id="174b3-142">O uso dessas funções reduz o tempo necessário para gravar uma DLL ou XLL.</span><span class="sxs-lookup"><span data-stu-id="174b3-142">Use of these functions shortens the amount of time required to write a DLL or XLL.</span></span> <span data-ttu-id="174b3-143">Iniciar o desenvolvimento a partir do exemplo de aplicativo GENERIC também reduz o tempo de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="174b3-143">Starting development from the sample application GENERIC also shortens development time.</span></span> <span data-ttu-id="174b3-144">Use GENERIC. C como um modelo para ajudar a configurar a estrutura de um XLL e, em seguida, substituir o código existente por seu próprio.</span><span class="sxs-lookup"><span data-stu-id="174b3-144">Use GENERIC.C as a template to help set up the framework of an XLL, and then replace the existing code with your own.</span></span>
  
<span data-ttu-id="174b3-145">As funções **XLOPER** /  **XLOPER12** temporárias criam valores  /  **XLOPER XLOPER12** usando memória de uma pilha local gerenciada pela biblioteca framework.</span><span class="sxs-lookup"><span data-stu-id="174b3-145">The temporary **XLOPER**/ **XLOPER12** functions create **XLOPER**/ **XLOPER12** values by using memory from a local heap managed by the Framework library.</span></span> <span data-ttu-id="174b3-146">Os **valores XLOPER** XLOPER12 permanecem válidos até que você chame a função /   **FreeAllTempMemory** ou uma das funções **Excel** ou **Excel12f.**</span><span class="sxs-lookup"><span data-stu-id="174b3-146">The **XLOPER**/ **XLOPER12** values remain valid until you call the **FreeAllTempMemory** function or either of the **Excel** or **Excel12f** functions.</span></span> <span data-ttu-id="174b3-147">(As **funções Excel** e **Excel12f** liberam toda a memória temporária antes de retornar.)</span><span class="sxs-lookup"><span data-stu-id="174b3-147">(The **Excel** and **Excel12f** functions free all temporary memory before returning.)</span></span> 
  
<span data-ttu-id="174b3-148">Para usar as funções de biblioteca do Framework, você deve incluir o FRAMEWRK. Arquivo H no código C e adicione FRAMEWRK. C ou FRMWRK32. Arquivos LIB para seu projeto de código.</span><span class="sxs-lookup"><span data-stu-id="174b3-148">To use the Framework library functions, you must include the FRAMEWRK.H file in your C code and add the FRAMEWRK.C or FRMWRK32.LIB files to your code project.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="174b3-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="174b3-149">See also</span></span>

- [<span data-ttu-id="174b3-150">Excel XLL SDK API Function Reference</span><span class="sxs-lookup"><span data-stu-id="174b3-150">Excel XLL SDK API Function Reference</span></span>](excel-xll-sdk-api-function-reference.md)

