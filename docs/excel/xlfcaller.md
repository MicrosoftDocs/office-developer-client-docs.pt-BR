---
title: xlfCaller
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfCaller
keywords:
- função xlfCaller [excel 2007]
localization_priority: Normal
ms.assetid: de4b119c-ae2e-4207-9783-8d5692a4d052
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 92d2d1877d7b315d178ef1fa36b47bd5f9f8e661
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765461"
---
# <a name="xlfcaller"></a><span data-ttu-id="7c00b-104">xlfCaller</span><span class="sxs-lookup"><span data-stu-id="7c00b-104">xlfCaller</span></span>

 <span data-ttu-id="7c00b-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="7c00b-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="7c00b-106">Retorna informações sobre a célula, o intervalo de células, o comando em um menu, a ferramenta em uma barra de ferramentas ou objeto que chamou o comando DLL ou a função que está sendo executado.</span><span class="sxs-lookup"><span data-stu-id="7c00b-106">Returns information about the cell, range of cells, command on a menu, tool on a toolbar, or object that called the DLL command or function that is currently running.</span></span>
  
|<span data-ttu-id="7c00b-107">**Chamado a partir de código**</span><span class="sxs-lookup"><span data-stu-id="7c00b-107">**Code called from**</span></span>|<span data-ttu-id="7c00b-108">**Retorna**</span><span class="sxs-lookup"><span data-stu-id="7c00b-108">**Returns**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7c00b-109">DLL</span><span class="sxs-lookup"><span data-stu-id="7c00b-109">DLL</span></span>  <br/> |<span data-ttu-id="7c00b-110">A identificação do registro.</span><span class="sxs-lookup"><span data-stu-id="7c00b-110">The Register ID.</span></span>  <br/> |
|<span data-ttu-id="7c00b-111">Uma única célula</span><span class="sxs-lookup"><span data-stu-id="7c00b-111">A single cell</span></span>  <br/> |<span data-ttu-id="7c00b-112">Uma referência de célula única.</span><span class="sxs-lookup"><span data-stu-id="7c00b-112">A single-cell reference.</span></span>  <br/> |
|<span data-ttu-id="7c00b-113">Uma fórmula de matriz com várias células</span><span class="sxs-lookup"><span data-stu-id="7c00b-113">A multi-cell array formula</span></span>  <br/> |<span data-ttu-id="7c00b-114">Uma referência de várias célula.</span><span class="sxs-lookup"><span data-stu-id="7c00b-114">A multi-cell reference.</span></span>  <br/> |
|<span data-ttu-id="7c00b-115">Uma expressão de formatação condicional</span><span class="sxs-lookup"><span data-stu-id="7c00b-115">A conditional formatting expression</span></span>  <br/> |<span data-ttu-id="7c00b-116">Uma referência à célula à qual a condição de formatação é aplicada.</span><span class="sxs-lookup"><span data-stu-id="7c00b-116">A reference to the cell to which the formatting condition is applied.</span></span>  <br/> |
|<span data-ttu-id="7c00b-117">Um menu</span><span class="sxs-lookup"><span data-stu-id="7c00b-117">A menu</span></span>  <br/> | <span data-ttu-id="7c00b-118">Uma matriz de linha única de quatro elementos:</span><span class="sxs-lookup"><span data-stu-id="7c00b-118">A four-element single-row array:</span></span>  <br/>  <span data-ttu-id="7c00b-119">ID de barra.</span><span class="sxs-lookup"><span data-stu-id="7c00b-119">The bar ID.</span></span>  <br/>  <span data-ttu-id="7c00b-120">A posição do menu.</span><span class="sxs-lookup"><span data-stu-id="7c00b-120">The menu position.</span></span>  <br/>  <span data-ttu-id="7c00b-121">A posição de submenu.</span><span class="sxs-lookup"><span data-stu-id="7c00b-121">The submenu position.</span></span>  <br/>  <span data-ttu-id="7c00b-122">A posição do comando.</span><span class="sxs-lookup"><span data-stu-id="7c00b-122">The command position.</span></span>  <br/> |
|<span data-ttu-id="7c00b-123">Uma barra de ferramentas</span><span class="sxs-lookup"><span data-stu-id="7c00b-123">A toolbar</span></span>  <br/> | <span data-ttu-id="7c00b-124">Uma matriz de linha única de dois elementos:</span><span class="sxs-lookup"><span data-stu-id="7c00b-124">A two-element single-row array:</span></span>  <br/>  <span data-ttu-id="7c00b-125">O número de barra de ferramentas para barras de ferramentas internas ou o nome da barra de ferramentas para barras de ferramentas personalizadas.</span><span class="sxs-lookup"><span data-stu-id="7c00b-125">The toolbar number for built-in toolbars or the toolbar name for custom toolbars.</span></span>  <br/>  <span data-ttu-id="7c00b-126">A posição na barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="7c00b-126">The position on the toolbar.</span></span>  <br/> |
|<span data-ttu-id="7c00b-127">Um objeto graphic</span><span class="sxs-lookup"><span data-stu-id="7c00b-127">A graphic object</span></span>  <br/> |<span data-ttu-id="7c00b-128">O identificador de objeto (nome de objeto).</span><span class="sxs-lookup"><span data-stu-id="7c00b-128">The object identifier (object name).</span></span>  <br/> |
|<span data-ttu-id="7c00b-129">Um comando associado a um xlcOnEnter, em. Inserir, evento interceptação</span><span class="sxs-lookup"><span data-stu-id="7c00b-129">A command associated with an xlcOnEnter, ON.ENTER, event trap</span></span>  <br/> |<span data-ttu-id="7c00b-130">Uma referência para a célula ou células inseridas.</span><span class="sxs-lookup"><span data-stu-id="7c00b-130">A reference to the cell or cells being entered.</span></span>  <br/> |
|<span data-ttu-id="7c00b-131">Um comando associado a um xlcOnDoubleclick, em. DOUBLECLICK, evento desvio.</span><span class="sxs-lookup"><span data-stu-id="7c00b-131">A command associated with an xlcOnDoubleclick, ON.DOUBLECLICK, event trap.</span></span>  <br/> |<span data-ttu-id="7c00b-132">A célula que foi clicado duas vezes (não necessariamente a célula ativa).</span><span class="sxs-lookup"><span data-stu-id="7c00b-132">The cell that was double-clicked (not necessarily the active cell).</span></span>  <br/> |
|<span data-ttu-id="7c00b-133">Macro Auto_Open, AutoClose, Auto_Activate ou Auto_Deactivate</span><span class="sxs-lookup"><span data-stu-id="7c00b-133">Auto_Open, AutoClose, Auto_Activate or Auto_Deactivate macro</span></span>  <br/> |<span data-ttu-id="7c00b-134">O nome da folha de chamada.</span><span class="sxs-lookup"><span data-stu-id="7c00b-134">The name of the calling sheet.</span></span>  <br/> |
|<span data-ttu-id="7c00b-135">Outros métodos não listados</span><span class="sxs-lookup"><span data-stu-id="7c00b-135">Other methods not listed</span></span>  <br/> |<span data-ttu-id="7c00b-136">#REF!</span><span class="sxs-lookup"><span data-stu-id="7c00b-136">#REF!</span></span> <span data-ttu-id="7c00b-137">Erro</span><span class="sxs-lookup"><span data-stu-id="7c00b-137">Error.</span></span>  <br/> |
   
```cs
Excel12(xlfCaller, (LPXLOPER12) pxRes,0);
```

## <a name="property-valuereturn-value"></a><span data-ttu-id="7c00b-138">Valor de propriedade/Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="7c00b-138">Property value/Return value</span></span>

<span data-ttu-id="7c00b-139">O valor de retorno é um dos seguintes **XLOPER**/ **XLOPER12** tipos de dados: **xltypeRef**, **xltypeSRef**, **xltypeNum**, **xltypeStr**, **xltypeErr**ou **xltypeMulti**.</span><span class="sxs-lookup"><span data-stu-id="7c00b-139">The return value is one of the following **XLOPER**/ **XLOPER12** data types: **xltypeRef**, **xltypeSRef**, **xltypeNum**, **xltypeStr**, **xltypeErr**, or **xltypeMulti**.</span></span> <span data-ttu-id="7c00b-140">Desde que três desses tipos de apontar para a memória alocada, o valor de retorno de **xlfCaller** deve sempre ser liberado em uma chamada para a [função xlFree](xlfree.md) quando ele não é mais necessária.</span><span class="sxs-lookup"><span data-stu-id="7c00b-140">Since three of these types point to allocated memory, the return value of **xlfCaller** should always be freed in a call to the [xlFree function](xlfree.md) when it is no longer needed.</span></span> 
  
<span data-ttu-id="7c00b-141">Para obter mais informações sobre **XLOPERs**/ **XLOPER12s** consulte [Gerenciamento de memória no Excel](memory-management-in-excel.md).</span><span class="sxs-lookup"><span data-stu-id="7c00b-141">For more information about **XLOPERs**/ **XLOPER12s** see [Memory Management in Excel](memory-management-in-excel.md).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7c00b-142">Comentários</span><span class="sxs-lookup"><span data-stu-id="7c00b-142">Remarks</span></span>

<span data-ttu-id="7c00b-143">Essa função é a função apenas não-planilha que pode ser chamada a partir de uma função de planilha DLL/XLL.</span><span class="sxs-lookup"><span data-stu-id="7c00b-143">This function is the only non-worksheet function that can be called from a DLL/XLL worksheet function.</span></span> <span data-ttu-id="7c00b-144">Outras funções de informações XLM só podem ser chamadas de comandos ou equivalente de folha de macro funções.</span><span class="sxs-lookup"><span data-stu-id="7c00b-144">Other XLM information functions can only be called from commands or macro-sheet equivalent functions.</span></span>
  
## <a name="example"></a><span data-ttu-id="7c00b-145">Exemplo</span><span class="sxs-lookup"><span data-stu-id="7c00b-145">Example</span></span>

 <span data-ttu-id="7c00b-146">`\SAMPLES\EXAMPLE\EXAMPLE.C`.</span><span class="sxs-lookup"><span data-stu-id="7c00b-146"></span></span> <span data-ttu-id="7c00b-147">Esta função chama uma macro de comando (xlcSelect) e funcionará corretamente somente quando chamadas de uma folha de macro.</span><span class="sxs-lookup"><span data-stu-id="7c00b-147">This function calls a command macro (xlcSelect) and will work correctly only when called from a macro sheet.</span></span>
  
```cs
short WINAPI CallerExample(void)
{
   XLOPER12 xRes;
   Excel12(xlfCaller, &xRes, 0);
   Excel12(xlcSelect, 0, 1, (LPXLOPER12)&xRes);
   Excel12(xlFree, 0, 1, (LPXLOPER12)&xRes);
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="7c00b-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="7c00b-148">See also</span></span>



[<span data-ttu-id="7c00b-149">Funções XLM essenciais e úteis para a API de C</span><span class="sxs-lookup"><span data-stu-id="7c00b-149">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

