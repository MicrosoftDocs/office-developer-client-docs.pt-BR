---
title: xlfCaller
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfCaller
keywords:
- Função xlfcaller [excel 2007]
localization_priority: Normal
ms.assetid: de4b119c-ae2e-4207-9783-8d5692a4d052
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: fb788375504cefab75fde9513147c1d54acdaa07
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405727"
---
# <a name="xlfcaller"></a><span data-ttu-id="32e54-104">xlfCaller</span><span class="sxs-lookup"><span data-stu-id="32e54-104">xlfCaller</span></span>

 <span data-ttu-id="32e54-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="32e54-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="32e54-106">Retorna informações sobre a célula, intervalo de células, comando em um menu, ferramenta em uma barra de ferramentas ou objeto que chamou o comando ou a função DLL em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="32e54-106">Returns information about the cell, range of cells, command on a menu, tool on a toolbar, or object that called the DLL command or function that is currently running.</span></span>
  
|<span data-ttu-id="32e54-107">**Código chamado de**</span><span class="sxs-lookup"><span data-stu-id="32e54-107">**Code called from**</span></span>|<span data-ttu-id="32e54-108">**Retorna**</span><span class="sxs-lookup"><span data-stu-id="32e54-108">**Returns**</span></span>|
|:-----|:-----|
|<span data-ttu-id="32e54-109">DLL</span><span class="sxs-lookup"><span data-stu-id="32e54-109">DLL</span></span>  <br/> |<span data-ttu-id="32e54-110">A ID do Registro.</span><span class="sxs-lookup"><span data-stu-id="32e54-110">The Register ID.</span></span>  <br/> |
|<span data-ttu-id="32e54-111">Uma única célula</span><span class="sxs-lookup"><span data-stu-id="32e54-111">A single cell</span></span>  <br/> |<span data-ttu-id="32e54-112">Uma referência de célula única.</span><span class="sxs-lookup"><span data-stu-id="32e54-112">A single-cell reference.</span></span>  <br/> |
|<span data-ttu-id="32e54-113">Uma fórmula de matriz de várias células</span><span class="sxs-lookup"><span data-stu-id="32e54-113">A multi-cell array formula</span></span>  <br/> |<span data-ttu-id="32e54-114">Uma referência de várias células.</span><span class="sxs-lookup"><span data-stu-id="32e54-114">A multi-cell reference.</span></span>  <br/> |
|<span data-ttu-id="32e54-115">Uma expressão de formatação condicional</span><span class="sxs-lookup"><span data-stu-id="32e54-115">A conditional formatting expression</span></span>  <br/> |<span data-ttu-id="32e54-116">Uma referência à célula à qual a condição de formatação é aplicada.</span><span class="sxs-lookup"><span data-stu-id="32e54-116">A reference to the cell to which the formatting condition is applied.</span></span>  <br/> |
|<span data-ttu-id="32e54-117">Um menu</span><span class="sxs-lookup"><span data-stu-id="32e54-117">A menu</span></span>  <br/> | <span data-ttu-id="32e54-118">Uma matriz de linha única de quatro elementos:</span><span class="sxs-lookup"><span data-stu-id="32e54-118">A four-element single-row array:</span></span>  <br/>  <span data-ttu-id="32e54-119">A ID da barra.</span><span class="sxs-lookup"><span data-stu-id="32e54-119">The bar ID.</span></span>  <br/>  <span data-ttu-id="32e54-120">A posição do menu.</span><span class="sxs-lookup"><span data-stu-id="32e54-120">The menu position.</span></span>  <br/>  <span data-ttu-id="32e54-121">A posição do submenu.</span><span class="sxs-lookup"><span data-stu-id="32e54-121">The submenu position.</span></span>  <br/>  <span data-ttu-id="32e54-122">A posição do comando.</span><span class="sxs-lookup"><span data-stu-id="32e54-122">The command position.</span></span>  <br/> |
|<span data-ttu-id="32e54-123">Uma barra de ferramentas</span><span class="sxs-lookup"><span data-stu-id="32e54-123">A toolbar</span></span>  <br/> | <span data-ttu-id="32e54-124">Uma matriz de linha única de dois elementos:</span><span class="sxs-lookup"><span data-stu-id="32e54-124">A two-element single-row array:</span></span>  <br/>  <span data-ttu-id="32e54-125">O número da barra de ferramentas para barras de ferramentas ou o nome da barra de ferramentas para barras de ferramentas personalizadas.</span><span class="sxs-lookup"><span data-stu-id="32e54-125">The toolbar number for built-in toolbars or the toolbar name for custom toolbars.</span></span>  <br/>  <span data-ttu-id="32e54-126">A posição na barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="32e54-126">The position on the toolbar.</span></span>  <br/> |
|<span data-ttu-id="32e54-127">Um objeto gráfico</span><span class="sxs-lookup"><span data-stu-id="32e54-127">A graphic object</span></span>  <br/> |<span data-ttu-id="32e54-128">O identificador de objeto (nome do objeto).</span><span class="sxs-lookup"><span data-stu-id="32e54-128">The object identifier (object name).</span></span>  <br/> |
|<span data-ttu-id="32e54-129">Um comando associado a um xlcOnEnter, ON. ENTER, intercepta eventos</span><span class="sxs-lookup"><span data-stu-id="32e54-129">A command associated with an xlcOnEnter, ON.ENTER, event trap</span></span>  <br/> |<span data-ttu-id="32e54-130">Uma referência à célula ou células que estão sendo inseridas.</span><span class="sxs-lookup"><span data-stu-id="32e54-130">A reference to the cell or cells being entered.</span></span>  <br/> |
|<span data-ttu-id="32e54-131">Um comando associado a um xlcOnDoubleclick, ON. DOUBLECLICK, interceptação de eventos.</span><span class="sxs-lookup"><span data-stu-id="32e54-131">A command associated with an xlcOnDoubleclick, ON.DOUBLECLICK, event trap.</span></span>  <br/> |<span data-ttu-id="32e54-132">A célula que foi clicada duas vezes (não necessariamente a célula ativa).</span><span class="sxs-lookup"><span data-stu-id="32e54-132">The cell that was double-clicked (not necessarily the active cell).</span></span>  <br/> |
|<span data-ttu-id="32e54-133">Auto_Open, AutoClose, Auto_Activate ou Auto_Deactivate macro</span><span class="sxs-lookup"><span data-stu-id="32e54-133">Auto_Open, AutoClose, Auto_Activate or Auto_Deactivate macro</span></span>  <br/> |<span data-ttu-id="32e54-134">O nome da planilha de chamada.</span><span class="sxs-lookup"><span data-stu-id="32e54-134">The name of the calling sheet.</span></span>  <br/> |
|<span data-ttu-id="32e54-135">Outros métodos não listados</span><span class="sxs-lookup"><span data-stu-id="32e54-135">Other methods not listed</span></span>  <br/> |<span data-ttu-id="32e54-136">#REF!</span><span class="sxs-lookup"><span data-stu-id="32e54-136">#REF!</span></span> <span data-ttu-id="32e54-137">Erro</span><span class="sxs-lookup"><span data-stu-id="32e54-137">Error.</span></span>  <br/> |
   
```cs
Excel12(xlfCaller, (LPXLOPER12) pxRes,0);
```

## <a name="property-valuereturn-value"></a><span data-ttu-id="32e54-138">Valor de propriedade/Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="32e54-138">Property value/Return value</span></span>

<span data-ttu-id="32e54-139">O valor de retorno é um dos seguintes tipos de dados /  **XLOPER XLOPER12:** **xltypeRef**, **xltypeSRef**, **xltypeNum**, **xltypeStr**, **xltypeErr** ou **xltypeMulti**.</span><span class="sxs-lookup"><span data-stu-id="32e54-139">The return value is one of the following **XLOPER**/ **XLOPER12** data types: **xltypeRef**, **xltypeSRef**, **xltypeNum**, **xltypeStr**, **xltypeErr**, or **xltypeMulti**.</span></span> <span data-ttu-id="32e54-140">Como três desses tipos apontam para a memória alocada, o valor de retorno **de xlfCaller** sempre deve ser liberado em uma chamada para a função [xlFree](xlfree.md) quando não for mais necessário.</span><span class="sxs-lookup"><span data-stu-id="32e54-140">Since three of these types point to allocated memory, the return value of **xlfCaller** should always be freed in a call to the [xlFree function](xlfree.md) when it is no longer needed.</span></span> 
  
<span data-ttu-id="32e54-141">Para obter mais informações sobre **XLOPERs** /  **XLOPER12s,** consulte [Gerenciamento de Memória no Excel.](memory-management-in-excel.md)</span><span class="sxs-lookup"><span data-stu-id="32e54-141">For more information about **XLOPERs**/ **XLOPER12s** see [Memory Management in Excel](memory-management-in-excel.md).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="32e54-142">Comentários</span><span class="sxs-lookup"><span data-stu-id="32e54-142">Remarks</span></span>

<span data-ttu-id="32e54-143">Esta função é a única função que não é de planilha que pode ser chamada a partir de uma função de planilha DLL/XLL.</span><span class="sxs-lookup"><span data-stu-id="32e54-143">This function is the only non-worksheet function that can be called from a DLL/XLL worksheet function.</span></span> <span data-ttu-id="32e54-144">Outras funções de informações XLM só podem ser chamadas de comandos ou funções equivalentes de planilha de macro.</span><span class="sxs-lookup"><span data-stu-id="32e54-144">Other XLM information functions can only be called from commands or macro-sheet equivalent functions.</span></span>
  
## <a name="example"></a><span data-ttu-id="32e54-145">Exemplo</span><span class="sxs-lookup"><span data-stu-id="32e54-145">Example</span></span>

 <span data-ttu-id="32e54-146">`\SAMPLES\EXAMPLE\EXAMPLE.C`.</span><span class="sxs-lookup"><span data-stu-id="32e54-146">`\SAMPLES\EXAMPLE\EXAMPLE.C`.</span></span> <span data-ttu-id="32e54-147">Esta função chama uma macro de comando (xlcSelect) e funcionará corretamente somente quando chamado de uma folha de macro.</span><span class="sxs-lookup"><span data-stu-id="32e54-147">This function calls a command macro (xlcSelect) and will work correctly only when called from a macro sheet.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="32e54-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="32e54-148">See also</span></span>



[<span data-ttu-id="32e54-149">Funções XLM essenciais e úteis para a API C</span><span class="sxs-lookup"><span data-stu-id="32e54-149">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

