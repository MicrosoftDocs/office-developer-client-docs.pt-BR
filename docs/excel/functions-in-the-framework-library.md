---
title: Funções na biblioteca de estrutura
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
keywords:
- funções da biblioteca do Framework [excel 2007] funções [Excel 2007], biblioteca Framework
localization_priority: Normal
ms.assetid: 7d9a13fd-9a4c-423e-bb08-4a5be57c7905
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 1d3878e376f95be3b277f1bb1a59545eb0a631ac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765385"
---
# <a name="functions-in-the-framework-library"></a><span data-ttu-id="8b4dc-104">Funções na biblioteca de estrutura</span><span class="sxs-lookup"><span data-stu-id="8b4dc-104">Functions in the Framework Library</span></span>

<span data-ttu-id="8b4dc-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="8b4dc-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="8b4dc-106">Biblioteca do Framework foi criada para ajudar a tornar escrever XLLs mais fácil.</span><span class="sxs-lookup"><span data-stu-id="8b4dc-106">The Framework Library was created to help make writing XLLs easier.</span></span> <span data-ttu-id="8b4dc-107">Ele inclui funções simples de gerenciamento **XLOPER**/ **XLOPER12** memória, criando temporário **XLOPER**/ **XLOPER12**, modo eficiente chamar as funções de retorno de chamada do Microsoft Excel (**Excel4**, **Excel4v** * * Excel12 * *, * * Excel12v * *) e a impressão de depuração cadeias de caracteres em um terminal conectado.</span><span class="sxs-lookup"><span data-stu-id="8b4dc-107">It includes simple functions for managing **XLOPER**/ **XLOPER12** memory, creating temporary **XLOPER**/ **XLOPER12**, robustly calling the Microsoft Excel callback functions (**Excel4**, **Excel4v**, ** Excel12 **, ** Excel12v **) and printing debugging strings on an attached terminal.</span></span>
  
<span data-ttu-id="8b4dc-108">As funções incluídas nessa biblioteca ajudam a simplificar a um trecho de código que é semelhante ao seguinte.</span><span class="sxs-lookup"><span data-stu-id="8b4dc-108">The functions included in this library help simplify a piece of code that looks like the following.</span></span>
  
```cs
XLOPER12 xMissing, xBool;
xMissing.xltype = xltypeMissing;
xBool.xltype = xltypeBool;
xBool.val.xbool = 0;
Excel12(xlcDisplay, 0, 2, (LPXLOPER12) &xMissing, (LPXLOPER12) &xBool);
```

<span data-ttu-id="8b4dc-109">O código simplificado se parece com o exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="8b4dc-109">The simplified code looks like the following example.</span></span>
  
```cs
Excel12f(xlcDisplay, 0, 2, TempMissing12(), TempBool12(0));
```

<span data-ttu-id="8b4dc-110">As seguintes funções estão incluídas na biblioteca do Framework:</span><span class="sxs-lookup"><span data-stu-id="8b4dc-110">The following functions are included in the Framework library:</span></span>
  
||
|:-----|
|[<span data-ttu-id="8b4dc-111">debugPrintf</span><span class="sxs-lookup"><span data-stu-id="8b4dc-111">debugPrintf</span></span>](debugprintf.md) <br/> |
|<span data-ttu-id="8b4dc-112">**GetTempMemory**</span><span class="sxs-lookup"><span data-stu-id="8b4dc-112">**GetTempMemory**</span></span> <br/> |
|<span data-ttu-id="8b4dc-113">**FreeAllTempMemory**</span><span class="sxs-lookup"><span data-stu-id="8b4dc-113">**FreeAllTempMemory**</span></span> <br/> |
|[<span data-ttu-id="8b4dc-114">InitFramework</span><span class="sxs-lookup"><span data-stu-id="8b4dc-114">InitFramework</span></span>](initframework.md) <br/> |
|[<span data-ttu-id="8b4dc-115">QuitFramework</span><span class="sxs-lookup"><span data-stu-id="8b4dc-115">QuitFramework</span></span>](quitframework.md) <br/> |
   
|<span data-ttu-id="8b4dc-116">**Funções usadas com XLOPERs**</span><span class="sxs-lookup"><span data-stu-id="8b4dc-116">**Functions Used with XLOPERs**</span></span>|<span data-ttu-id="8b4dc-117">**Funções usadas com XLOPER12s**</span><span class="sxs-lookup"><span data-stu-id="8b4dc-117">**Functions Used with XLOPER12s**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8b4dc-118">Excel</span><span class="sxs-lookup"><span data-stu-id="8b4dc-118">Excel</span></span>](excel-excel12f.md) <br/> |[<span data-ttu-id="8b4dc-119">Excel12f</span><span class="sxs-lookup"><span data-stu-id="8b4dc-119">Excel12f</span></span>](excel-excel12f.md) <br/> |
|[<span data-ttu-id="8b4dc-120">TempNum</span><span class="sxs-lookup"><span data-stu-id="8b4dc-120">TempNum</span></span>](tempnum-tempnum12.md) <br/> |[<span data-ttu-id="8b4dc-121">TempNum12</span><span class="sxs-lookup"><span data-stu-id="8b4dc-121">TempNum12</span></span>](tempnum-tempnum12.md) <br/> |
|[<span data-ttu-id="8b4dc-122">TempStr</span><span class="sxs-lookup"><span data-stu-id="8b4dc-122">TempStr</span></span>](tempstr.md) <br/> |[<span data-ttu-id="8b4dc-123">TempStr12</span><span class="sxs-lookup"><span data-stu-id="8b4dc-123">TempStr12</span></span>](tempstrconst-tempstr12.md) <br/> |
|[<span data-ttu-id="8b4dc-124">TempStrConst</span><span class="sxs-lookup"><span data-stu-id="8b4dc-124">TempStrConst</span></span>](tempstrconst-tempstr12.md) <br/> |[<span data-ttu-id="8b4dc-125">TempStr12Const</span><span class="sxs-lookup"><span data-stu-id="8b4dc-125">TempStr12Const</span></span>](tempstrconst-tempstr12.md) <br/> |
|[<span data-ttu-id="8b4dc-126">TempBool</span><span class="sxs-lookup"><span data-stu-id="8b4dc-126">TempBool</span></span>](tempbool-tempbool12.md) <br/> |[<span data-ttu-id="8b4dc-127">TempBool12</span><span class="sxs-lookup"><span data-stu-id="8b4dc-127">TempBool12</span></span>](tempbool-tempbool12.md) <br/> |
|[<span data-ttu-id="8b4dc-128">TempInt</span><span class="sxs-lookup"><span data-stu-id="8b4dc-128">TempInt</span></span>](tempint-tempint12.md) <br/> |[<span data-ttu-id="8b4dc-129">TempInt12</span><span class="sxs-lookup"><span data-stu-id="8b4dc-129">TempInt12</span></span>](tempint-tempint12.md) <br/> |
|[<span data-ttu-id="8b4dc-130">TempErr</span><span class="sxs-lookup"><span data-stu-id="8b4dc-130">TempErr</span></span>](temperr-temperr12.md) <br/> |[<span data-ttu-id="8b4dc-131">TempErr12</span><span class="sxs-lookup"><span data-stu-id="8b4dc-131">TempErr12</span></span>](temperr-temperr12.md) <br/> |
|[<span data-ttu-id="8b4dc-132">TempActiveRef</span><span class="sxs-lookup"><span data-stu-id="8b4dc-132">TempActiveRef</span></span>](tempactiveref-tempactiveref12.md) <br/> |[<span data-ttu-id="8b4dc-133">TempActiveRef12</span><span class="sxs-lookup"><span data-stu-id="8b4dc-133">TempActiveRef12</span></span>](tempactiveref-tempactiveref12.md) <br/> |
|[<span data-ttu-id="8b4dc-134">TempActiveCell</span><span class="sxs-lookup"><span data-stu-id="8b4dc-134">TempActiveCell</span></span>](tempactivecell-tempactivecell12.md) <br/> |[<span data-ttu-id="8b4dc-135">TempActiveCell12</span><span class="sxs-lookup"><span data-stu-id="8b4dc-135">TempActiveCell12</span></span>](tempactivecell-tempactivecell12.md) <br/> |
|[<span data-ttu-id="8b4dc-136">TempActiveRow</span><span class="sxs-lookup"><span data-stu-id="8b4dc-136">TempActiveRow</span></span>](tempactiverow-tempactiverow12.md) <br/> |[<span data-ttu-id="8b4dc-137">TempActiveRow12</span><span class="sxs-lookup"><span data-stu-id="8b4dc-137">TempActiveRow12</span></span>](tempactiverow-tempactiverow12.md) <br/> |
|[<span data-ttu-id="8b4dc-138">TempActiveColumn</span><span class="sxs-lookup"><span data-stu-id="8b4dc-138">TempActiveColumn</span></span>](tempactivecolumn-tempactivecolumn12.md) <br/> |[<span data-ttu-id="8b4dc-139">TempActiveColumn12</span><span class="sxs-lookup"><span data-stu-id="8b4dc-139">TempActiveColumn12</span></span>](tempactivecolumn-tempactivecolumn12.md) <br/> |
|[<span data-ttu-id="8b4dc-140">TempMissing</span><span class="sxs-lookup"><span data-stu-id="8b4dc-140">TempMissing</span></span>](tempmissing-tempmissing12.md) <br/> |[<span data-ttu-id="8b4dc-141">TempMissing12</span><span class="sxs-lookup"><span data-stu-id="8b4dc-141">TempMissing12</span></span>](tempmissing-tempmissing12.md) <br/> |
   
<span data-ttu-id="8b4dc-142">O uso dessas funções reduz a quantidade de tempo necessária para gravar uma DLL ou XLL.</span><span class="sxs-lookup"><span data-stu-id="8b4dc-142">Use of these functions shortens the amount of time required to write a DLL or XLL.</span></span> <span data-ttu-id="8b4dc-143">Iniciando o desenvolvimento do aplicativo de exemplo GENÉRICO também reduz o tempo de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="8b4dc-143">Starting development from the sample application GENERIC also shortens development time.</span></span> <span data-ttu-id="8b4dc-144">Use GENÉRICO. C como um modelo para ajudar a configurar a estrutura de um XLL e substitua o código existente com seus próprios.</span><span class="sxs-lookup"><span data-stu-id="8b4dc-144">Use GENERIC.C as a template to help set up the framework of an XLL, and then replace the existing code with your own.</span></span>
  
<span data-ttu-id="8b4dc-145">Temporário **XLOPER**/ **XLOPER12** funções criar **XLOPER**/ **XLOPER12** valores usando a memória a partir de um local heap gerenciado por biblioteca do Framework.</span><span class="sxs-lookup"><span data-stu-id="8b4dc-145">The temporary **XLOPER**/ **XLOPER12** functions create **XLOPER**/ **XLOPER12** values by using memory from a local heap managed by the Framework library.</span></span> <span data-ttu-id="8b4dc-146">**XLOPER**/ **XLOPER12** valores permanecerão válidos até que você chamar a função **FreeAllTempMemory** ou qualquer uma das funções do **Excel** ou **Excel12f** .</span><span class="sxs-lookup"><span data-stu-id="8b4dc-146">The **XLOPER**/ **XLOPER12** values remain valid until you call the **FreeAllTempMemory** function or either of the **Excel** or **Excel12f** functions.</span></span> <span data-ttu-id="8b4dc-147">(As funções do **Excel** e **Excel12f** livre toda a memória temporária antes de retornar).</span><span class="sxs-lookup"><span data-stu-id="8b4dc-147">(The **Excel** and **Excel12f** functions free all temporary memory before returning.)</span></span> 
  
<span data-ttu-id="8b4dc-148">Para usar as funções da biblioteca Framework, você deve incluir a FRAMEWRK. H do arquivo em seu código C e adicionar o FRAMEWRK. C ou FRMWRK32. Arquivos de biblioteca para seu projeto de código.</span><span class="sxs-lookup"><span data-stu-id="8b4dc-148">To use the Framework library functions, you must include the FRAMEWRK.H file in your C code and add the FRAMEWRK.C or FRMWRK32.LIB files to your code project.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8b4dc-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="8b4dc-149">See also</span></span>

- [<span data-ttu-id="8b4dc-150">Excel XLL SDK API Function Reference</span><span class="sxs-lookup"><span data-stu-id="8b4dc-150">Excel XLL SDK API Function Reference</span></span>](excel-xll-sdk-api-function-reference.md)

