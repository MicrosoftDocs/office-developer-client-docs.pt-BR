---
title: xlfEvaluate
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfEvaluate
keywords:
- função xlfevaluate [Excel 2007]
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
# <a name="xlfevaluate"></a><span data-ttu-id="7edbc-104">xlfEvaluate</span><span class="sxs-lookup"><span data-stu-id="7edbc-104">xlfEvaluate</span></span>

 <span data-ttu-id="7edbc-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="7edbc-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="7edbc-106">Usa o Microsoft Excel Parser e o avaliador de função para avaliar qualquer expressão que possa ser inserida em uma célula de planilha.</span><span class="sxs-lookup"><span data-stu-id="7edbc-106">Uses the Microsoft Excel parser and function evaluator to evaluate any expression that could be entered in a worksheet cell.</span></span>
  
```cs
Excel12(xlfEvaluate, LPXLOPER12 pxRes, 1, LPXLOPER12 pxFormulaText);
```

## <a name="parameters"></a><span data-ttu-id="7edbc-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7edbc-107">Parameters</span></span>

 <span data-ttu-id="7edbc-108">_pxFormulaText (xltypeStr)_</span><span class="sxs-lookup"><span data-stu-id="7edbc-108">_pxFormulaText (xltypeStr)_</span></span>
  
<span data-ttu-id="7edbc-109">A cadeia de caracteres a ser avaliada.</span><span class="sxs-lookup"><span data-stu-id="7edbc-109">The string to be evaluated.</span></span> <span data-ttu-id="7edbc-110">Um sinal de igual (=) à esquerda é opcional.</span><span class="sxs-lookup"><span data-stu-id="7edbc-110">A leading equal sign (=) is optional.</span></span> <span data-ttu-id="7edbc-111">A cadeia de caracteres pode ser qualquer texto que possa ser inserido legalmente em uma planilha ou célula de planilha de macro.</span><span class="sxs-lookup"><span data-stu-id="7edbc-111">The string can be any text that can legally be entered into a worksheet or macro sheet cell.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="7edbc-112">Valor de propriedade/Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="7edbc-112">Property value/Return value</span></span>

<span data-ttu-id="7edbc-113">Retorna o resultado da avaliação da cadeia de caracteres que pode ser qualquer um dos tipos **xltypeNum**, **xltypeStr**, **xltypeBool**, **xltypeErr**, **xltypeNil**, **xltypeMulti**.</span><span class="sxs-lookup"><span data-stu-id="7edbc-113">Returns the result of evaluating the string which can be any of the types **xltypeNum**, **xltypeStr**, **xltypeBool**, **xltypeErr**, **xltypeNil**, **xltypeMulti**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7edbc-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="7edbc-114">Remarks</span></span>

<span data-ttu-id="7edbc-115">A cadeia de caracteres pode conter apenas funções, não equivalentes de comando.</span><span class="sxs-lookup"><span data-stu-id="7edbc-115">The string can contain only functions, not command equivalents.</span></span> <span data-ttu-id="7edbc-116">É equivalente a pressionar **F9** da barra de fórmulas.</span><span class="sxs-lookup"><span data-stu-id="7edbc-116">It is equivalent to pressing **F9** from the formula bar.</span></span> <span data-ttu-id="7edbc-117">Se **xlfEvaluate** for chamado a partir de uma função de planilha XLL registrada como thread-safe, a expressão deve conter apenas funções thread-safe.</span><span class="sxs-lookup"><span data-stu-id="7edbc-117">If **xlfEvaluate** is called from an XLL worksheet function that has been registered as thread safe, the expression must only contain thread-safe functions.</span></span> 
  
<span data-ttu-id="7edbc-118">O uso principal da função **xlfEvaluate** é permitir que as DLLs descubram o valor atribuído a um nome definido em uma planilha ou um nome oculto definido dentro da dll.</span><span class="sxs-lookup"><span data-stu-id="7edbc-118">The primary use of the **xlfEvaluate** function is to allow DLLs to find out the value assigned to a defined name that is either on a sheet or a hidden name defined within the DLL.</span></span> <span data-ttu-id="7edbc-119">Observe que, em uma DLL/XLL, um nome de planilha deve ser prefixado com pelo menos um ponto de exclamação (!) para garantir que ele seja interpretado como externo à DLL.</span><span class="sxs-lookup"><span data-stu-id="7edbc-119">Note that within a DLL/XLL, a worksheet name must be prefixed with at least an exclamation mark (!) to ensure that it is interpreted as external to the DLL.</span></span> <span data-ttu-id="7edbc-120">Para obter mais informações, consulte [avaliar nomes e outras expressões de fórmula de planilha](evaluating-names-and-other-worksheet-formula-expressions.md).</span><span class="sxs-lookup"><span data-stu-id="7edbc-120">For more information, see [Evaluating Names and Other Worksheet Formula Expressions](evaluating-names-and-other-worksheet-formula-expressions.md).</span></span>
  
 <span data-ttu-id="7edbc-121">**xlfEvaluate** não pode ser usado para avaliar referências a uma planilha externa que não está aberta.</span><span class="sxs-lookup"><span data-stu-id="7edbc-121">**xlfEvaluate** cannot be used to evaluate references to an external sheet that is not open.</span></span> 
  
## <a name="example"></a><span data-ttu-id="7edbc-122">Exemplo</span><span class="sxs-lookup"><span data-stu-id="7edbc-122">Example</span></span>

<span data-ttu-id="7edbc-123">Este exemplo usa **xlfEvaluate** para forçar o texto "! B38 "com o conteúdo da célula B38.</span><span class="sxs-lookup"><span data-stu-id="7edbc-123">This example uses **xlfEvaluate** to coerce the text "!B38" to the contents of cell B38.</span></span> 
  
 <span data-ttu-id="7edbc-124">`\SAMPLES\EXAMPLE\EXAMPLE.C`.</span><span class="sxs-lookup"><span data-stu-id="7edbc-124"></span></span> <span data-ttu-id="7edbc-125">Essa função chama uma macro de comando (**xlcAlert**) e funcionará corretamente somente quando for chamado a partir de uma folha de macro ou como um comando de macro.</span><span class="sxs-lookup"><span data-stu-id="7edbc-125">This function calls a command macro (**xlcAlert**) and will work correctly only when called from a macro sheet or as a macro command.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="7edbc-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="7edbc-126">See also</span></span>

- [<span data-ttu-id="7edbc-127">Funções XLM essenciais e úteis para a API C</span><span class="sxs-lookup"><span data-stu-id="7edbc-127">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

