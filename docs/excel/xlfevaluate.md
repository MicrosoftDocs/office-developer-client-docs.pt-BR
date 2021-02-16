---
title: xlfEvaluate
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfEvaluate
keywords:
- Função xlfevaluate [excel 2007]
localization_priority: Normal
ms.assetid: deea3ee6-2a32-47ef-bfa4-914891538633
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 527f7e932a41103c374e327a1bd0dd4c7d8e92a0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439181"
---
# <a name="xlfevaluate"></a><span data-ttu-id="2a0ee-104">xlfEvaluate</span><span class="sxs-lookup"><span data-stu-id="2a0ee-104">xlfEvaluate</span></span>

 <span data-ttu-id="2a0ee-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="2a0ee-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="2a0ee-106">Usa o analisador do Microsoft Excel e o avaliador de funções para avaliar qualquer expressão que possa ser inserida em uma célula de planilha.</span><span class="sxs-lookup"><span data-stu-id="2a0ee-106">Uses the Microsoft Excel parser and function evaluator to evaluate any expression that could be entered in a worksheet cell.</span></span>
  
```cs
Excel12(xlfEvaluate, LPXLOPER12 pxRes, 1, LPXLOPER12 pxFormulaText);
```

## <a name="parameters"></a><span data-ttu-id="2a0ee-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2a0ee-107">Parameters</span></span>

 <span data-ttu-id="2a0ee-108">_pxFormulaText (xltypeStr)_</span><span class="sxs-lookup"><span data-stu-id="2a0ee-108">_pxFormulaText (xltypeStr)_</span></span>
  
<span data-ttu-id="2a0ee-109">A cadeia de caracteres a ser avaliada.</span><span class="sxs-lookup"><span data-stu-id="2a0ee-109">The string to be evaluated.</span></span> <span data-ttu-id="2a0ee-110">Um sinal de igual à frente (=) é opcional.</span><span class="sxs-lookup"><span data-stu-id="2a0ee-110">A leading equal sign (=) is optional.</span></span> <span data-ttu-id="2a0ee-111">A cadeia de caracteres pode ser qualquer texto que possa ser inserido legalmente em uma célula de planilha de macro ou planilha de macro.</span><span class="sxs-lookup"><span data-stu-id="2a0ee-111">The string can be any text that can legally be entered into a worksheet or macro sheet cell.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="2a0ee-112">Valor de propriedade/Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="2a0ee-112">Property value/Return value</span></span>

<span data-ttu-id="2a0ee-113">Retorna o resultado da avaliação da cadeia de caracteres que pode ser qualquer um dos tipos **xltypeNum**, **xltypeStr**, **xltypeBool**, **xltypeErr**, **xltypeNil**, **xltypeMulti**.</span><span class="sxs-lookup"><span data-stu-id="2a0ee-113">Returns the result of evaluating the string which can be any of the types **xltypeNum**, **xltypeStr**, **xltypeBool**, **xltypeErr**, **xltypeNil**, **xltypeMulti**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2a0ee-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="2a0ee-114">Remarks</span></span>

<span data-ttu-id="2a0ee-115">A cadeia de caracteres pode conter apenas funções, não equivalentes de comando.</span><span class="sxs-lookup"><span data-stu-id="2a0ee-115">The string can contain only functions, not command equivalents.</span></span> <span data-ttu-id="2a0ee-116">Equivale a pressionar **F9 a partir** da barra de fórmulas.</span><span class="sxs-lookup"><span data-stu-id="2a0ee-116">It is equivalent to pressing **F9** from the formula bar.</span></span> <span data-ttu-id="2a0ee-117">Se **xlfEvaluate** for chamado de uma função de planilha XLL registrada como thread-safe, a expressão deverá conter apenas funções thread-safe.</span><span class="sxs-lookup"><span data-stu-id="2a0ee-117">If **xlfEvaluate** is called from an XLL worksheet function that has been registered as thread safe, the expression must only contain thread-safe functions.</span></span> 
  
<span data-ttu-id="2a0ee-118">O uso principal da função **xlfEvaluate** é permitir que as DLLs descubram o valor atribuído a um nome definido que está em uma planilha ou em um nome oculto definido dentro da DLL.</span><span class="sxs-lookup"><span data-stu-id="2a0ee-118">The primary use of the **xlfEvaluate** function is to allow DLLs to find out the value assigned to a defined name that is either on a sheet or a hidden name defined within the DLL.</span></span> <span data-ttu-id="2a0ee-119">Observe que dentro de uma DLL/XLL, um nome de planilha deve ser prefixado com pelo menos um ponto de exclamação (!) para garantir que ele seja interpretado como externo à DLL.</span><span class="sxs-lookup"><span data-stu-id="2a0ee-119">Note that within a DLL/XLL, a worksheet name must be prefixed with at least an exclamation mark (!) to ensure that it is interpreted as external to the DLL.</span></span> <span data-ttu-id="2a0ee-120">Para obter mais informações, [consulte Avaliando nomes e outras expressões de fórmula de planilha.](evaluating-names-and-other-worksheet-formula-expressions.md)</span><span class="sxs-lookup"><span data-stu-id="2a0ee-120">For more information, see [Evaluating Names and Other Worksheet Formula Expressions](evaluating-names-and-other-worksheet-formula-expressions.md).</span></span>
  
 <span data-ttu-id="2a0ee-121">**xlfEvaluate** não pode ser usado para avaliar referências a uma planilha externa que não está aberta.</span><span class="sxs-lookup"><span data-stu-id="2a0ee-121">**xlfEvaluate** cannot be used to evaluate references to an external sheet that is not open.</span></span> 
  
## <a name="example"></a><span data-ttu-id="2a0ee-122">Exemplo</span><span class="sxs-lookup"><span data-stu-id="2a0ee-122">Example</span></span>

<span data-ttu-id="2a0ee-123">Este exemplo usa **xlfEvaluate** para fazer a coerção do texto "! B38" para o conteúdo da célula B38.</span><span class="sxs-lookup"><span data-stu-id="2a0ee-123">This example uses **xlfEvaluate** to coerce the text "!B38" to the contents of cell B38.</span></span> 
  
 <span data-ttu-id="2a0ee-124">`\SAMPLES\EXAMPLE\EXAMPLE.C`.</span><span class="sxs-lookup"><span data-stu-id="2a0ee-124">`\SAMPLES\EXAMPLE\EXAMPLE.C`.</span></span> <span data-ttu-id="2a0ee-125">Esta função chama uma macro de comando (**xlcAlert**) e funcionará corretamente somente quando chamado de uma folha de macro ou como um comando de macro.</span><span class="sxs-lookup"><span data-stu-id="2a0ee-125">This function calls a command macro (**xlcAlert**) and will work correctly only when called from a macro sheet or as a macro command.</span></span>
  
```cs
short WINAPI EvaluateExample(void)
{
    XLOPER12 xFormulaText, xRes, xRes2, xInt;
    xFormulaText.xltype = xltypeStr;
    xFormulaText.val.str = L"\004!B38";
    Excel12(xlfEvaluate, &xRes, 1, (LPXLOPER12)&xFormulaText);
    xInt.xltype = xltypeInt;
    xInt.val.w = 2;
    Excel12(xlcAlert, &xRes2, 2, (LPXLOPER12)&xRes, (LPXLOPER12)&xInt);
    Excel12(xlFree, 0, 1, (LPXLOPER12)&xRes);
    Excel12(xlFree, 0, 1, (LPXLOPER12)&xRes2);
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="2a0ee-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="2a0ee-126">See also</span></span>

- [<span data-ttu-id="2a0ee-127">Funções XLM essenciais e úteis para a API C</span><span class="sxs-lookup"><span data-stu-id="2a0ee-127">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

