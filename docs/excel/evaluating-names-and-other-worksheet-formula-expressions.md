---
title: Avaliar nomes e outras expressões de fórmula de planilha
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- avaliação de expressão [excel 2007],planilhas [Excel 2007], avaliação de nome, avaliação de expressões [Excel 2007], avaliação de nomes de planilha [Excel 2007],expressões [Excel 2007], avaliação, nomes [Excel 2007], avaliação, avaliação de nome [Excel 2007],cadeias de caracteres [Excel 2007], conversão em valores,função xlfEvaluate [Excel 2007],planilhas [Excel 2007], avaliação de expressão
localization_priority: Normal
ms.assetid: 2b23c75e-2a95-4f26-8714-2a73f5e326a7
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 97328cbc57a9144a133524774e3be10a84a96bf4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406861"
---
# <a name="evaluating-names-and-other-worksheet-formula-expressions"></a><span data-ttu-id="4dc5f-104">Avaliar nomes e outras expressões de fórmula de planilha</span><span class="sxs-lookup"><span data-stu-id="4dc5f-104">Evaluating names and other worksheet formula expressions</span></span>

<span data-ttu-id="4dc5f-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="4dc5f-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="4dc5f-106">Um dos recursos mais importantes que o Excel expõe por meio da API de C é a capacidade de converter qualquer fórmula de cadeia de caracteres que possa ser inserida legalmente em uma planilha em um valor ou em uma matriz de valores.</span><span class="sxs-lookup"><span data-stu-id="4dc5f-106">One of the most important features that Excel exposes through the C API is the ability to convert any string formula that can legally be entered into a worksheet to a value, or array of values.</span></span> <span data-ttu-id="4dc5f-107">Isso é essencial para funções e comandos XLL que devem ler o conteúdo de nomes definidos, por exemplo.</span><span class="sxs-lookup"><span data-stu-id="4dc5f-107">This is essential for XLL functions and commands that must read the contents of defined names, for example.</span></span> <span data-ttu-id="4dc5f-108">Essa capacidade é exposta por meio [da função xlfEvaluate](xlfevaluate.md), conforme mostrado neste exemplo.</span><span class="sxs-lookup"><span data-stu-id="4dc5f-108">This ability is exposed through the [xlfEvaluate function](xlfevaluate.md), as shown in this example.</span></span>
  
```C
int WINAPI evaluate_name_example(void)
{
  wchar_t *expression = L"\016!MyDefinedName";
  XLOPER12 xNameText, xNameValue;
  xNameText.xltype = xltypeStr;
  xNameText.val.str = expression;
// Try to evaluate the name. Will fail with a #NAME? error
// if MyDefinedName is not defined in the active workbook.
  Excel12(xlfEvaluate, &xNameValue, 1, &xNameText);
// Attempt to convert the value to a string and display it in
// an alert dialog. This fails if xNameValue is an error value.
  Excel12(xlcAlert, 0, 1, &xNameValue);
// Must free xNameValue in case MyDefinedName evaluated to a string
  Excel12(xlFree, 0, 1, &xNameValue);
  return 1;
}
```

<span data-ttu-id="4dc5f-109">Observe que, ao avaliar um nome de planilha, por conta própria ou em uma fórmula, você deve prefixar o nome com '!', pelo menos.</span><span class="sxs-lookup"><span data-stu-id="4dc5f-109">Note that when you are evaluating a worksheet name, either on its own or in a formula, you must prefix the name with '!', at least.</span></span> <span data-ttu-id="4dc5f-110">Caso contrário, o Excel tentará encontrar o nome em um namespace oculto reservado para DLLs.</span><span class="sxs-lookup"><span data-stu-id="4dc5f-110">Otherwise, Excel tries to find the name in a hidden namespace reserved for DLLs.</span></span> <span data-ttu-id="4dc5f-111">Você pode criar e excluir nomes DLL ocultos usando a [função xlfSetName](xlfsetname.md).</span><span class="sxs-lookup"><span data-stu-id="4dc5f-111">You can create and delete hidden DLL names using the [xlfSetName function](xlfsetname.md).</span></span> <span data-ttu-id="4dc5f-112">Você pode obter a definição de qualquer nome definido, seja um nome DLL oculto ou um nome de planilha, usando a função **xlfGetDef.**</span><span class="sxs-lookup"><span data-stu-id="4dc5f-112">You can get the definition of any defined name, whether it is a hidden DLL name or a worksheet name, using the **xlfGetDef** function.</span></span> 
  
<span data-ttu-id="4dc5f-113">A especificação completa de um nome de planilha tem o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="4dc5f-113">The full specification for a worksheet name takes the following form:</span></span>
  
`='C:\example folder\[Book1.xls]Sheet1'!Name`
  
<span data-ttu-id="4dc5f-114">Observe que o Excel 2007 introduziu várias novas extensões de arquivo.</span><span class="sxs-lookup"><span data-stu-id="4dc5f-114">Note that Excel 2007 introduced a number of new file extensions.</span></span> <span data-ttu-id="4dc5f-115">Você pode omitir o caminho, o nome da pasta de trabalho e o nome da planilha onde não há ambiguidade entre as planilhas abertas nesta sessão do Excel.</span><span class="sxs-lookup"><span data-stu-id="4dc5f-115">You can omit the path, the workbook name, and the sheet name where there is no ambiguity among the open workbooks in this Excel session.</span></span> 
  
<span data-ttu-id="4dc5f-116">O próximo exemplo avalia a fórmula  `COUNT(A1:IV65536)` da planilha ativa e exibe o resultado.</span><span class="sxs-lookup"><span data-stu-id="4dc5f-116">The next example evaluates the formula  `COUNT(A1:IV65536)` for the active worksheet and displays the result.</span></span> <span data-ttu-id="4dc5f-117">Observe a necessidade de prefixar o endereço do intervalo com '!', que é consistente com a convenção de referência de intervalo em folhas de macro XLM.</span><span class="sxs-lookup"><span data-stu-id="4dc5f-117">Note the need to prefix the range address with '!', which is consistent with the range reference convention on XLM macro sheets.</span></span> <span data-ttu-id="4dc5f-118">O XLM da API de C segue esta convenção:</span><span class="sxs-lookup"><span data-stu-id="4dc5f-118">The C API XLM follows this convention:</span></span> 
  
- <span data-ttu-id="4dc5f-119">`=A1` Uma referência à célula A1 na folha de macro atual.</span><span class="sxs-lookup"><span data-stu-id="4dc5f-119">`=A1` A reference to cell A1 on the current macro sheet.</span></span> <span data-ttu-id="4dc5f-120">(Não definido para XLLs).</span><span class="sxs-lookup"><span data-stu-id="4dc5f-120">(Not defined for XLLs).</span></span> 
  
- <span data-ttu-id="4dc5f-121">`=!A1` Uma referência à célula A1 da planilha ativa (que pode ser uma planilha ou uma folha de macro)</span><span class="sxs-lookup"><span data-stu-id="4dc5f-121">`=!A1` A reference to cell A1 on the active sheet (which could be a worksheet or macro sheet)</span></span> 
  
- <span data-ttu-id="4dc5f-122">`=Sheet1!A1` Uma referência à célula A1 na planilha especificada, Sheet1 neste caso.</span><span class="sxs-lookup"><span data-stu-id="4dc5f-122">`=Sheet1!A1` A reference to cell A1 on the specified sheet, Sheet1 in this case.</span></span> 
  
- <span data-ttu-id="4dc5f-123">`=[Book1.xls]Sheet1!A1` Uma referência à célula A1 na planilha especificada na pasta de trabalho especificada.</span><span class="sxs-lookup"><span data-stu-id="4dc5f-123">`=[Book1.xls]Sheet1!A1` A reference to cell A1 on the specified sheet in the specified workbook.</span></span> 
  
<span data-ttu-id="4dc5f-124">Em um XLL, uma referência sem um ponto de exclamação à frente (**!**) não pode ser convertida em um valor.</span><span class="sxs-lookup"><span data-stu-id="4dc5f-124">In an XLL, a reference without a leading exclamation point (**!**) cannot be converted to a value.</span></span> <span data-ttu-id="4dc5f-125">Isso não tem significado porque não há uma folha de macro atual.</span><span class="sxs-lookup"><span data-stu-id="4dc5f-125">It has no meaning because there is no current macro sheet.</span></span> <span data-ttu-id="4dc5f-126">Observe que um sinal de igual à parte ( ) é **=** opcional e é omitido no próximo exemplo.</span><span class="sxs-lookup"><span data-stu-id="4dc5f-126">Note that a leading equals sign (**=**) is optional and is omitted in the next example.</span></span>
  
```C
int WINAPI evaluate_expression_example(void)
{
    wchar_t *expression = L"\022COUNT(!A1:IV65536)";
    XLOPER12 xExprText, xExprValue;
    xExprText.xltype = xltypeStr;
    xExprText.val.str = expression;
// Try to evaluate the formula.
    Excel12(xlfEvaluate, &xExprValue, 1, &xExprText);
// Attempt to convert the value to a string and display it in
// an alert dialog. Will fail if xExprValue is an error.
    Excel12(xlcAlert, 0, 1, &xExprValue);
// Not strictly necessary, as COUNT never returns a string
// but does no harm.
    Excel12(xlFree, 0, 1, &xExprValue);
    return 1;
}
```

<span data-ttu-id="4dc5f-127">Você também pode usar a função **xlfEvaluate** para recuperar a ID de registro de uma função XLL de seu nome registrado, que pode ser usado para chamar essa função usando a função [xlUDF](xludf.md).</span><span class="sxs-lookup"><span data-stu-id="4dc5f-127">You can also use the **xlfEvaluate** function to retrieve the registration ID of an XLL function from its registered name, which can then be used to call that function using the [xlUDF function](xludf.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="4dc5f-128">O nome registrado pode ser passado diretamente para a **função xlUDF.**</span><span class="sxs-lookup"><span data-stu-id="4dc5f-128">The registered name can be passed directly to the **xlUDF** function.</span></span> <span data-ttu-id="4dc5f-129">Isso significa que você pode evitar ter que avaliar o nome para obter a ID antes de chamar **xlUDF**.</span><span class="sxs-lookup"><span data-stu-id="4dc5f-129">This means that you can avoid having to evaluate the name to get the ID before calling **xlUDF**.</span></span> <span data-ttu-id="4dc5f-130">No entanto, se a função for chamada várias vezes, chamá-la usando a ID de registro será mais rápida.</span><span class="sxs-lookup"><span data-stu-id="4dc5f-130">However, if the function is to be called many times, calling it by using the registration ID is faster.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4dc5f-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="4dc5f-131">See also</span></span>

- [<span data-ttu-id="4dc5f-132">Avaliação de expressões e planilhas do Excel</span><span class="sxs-lookup"><span data-stu-id="4dc5f-132">Excel Worksheet and Expression Evaluation</span></span>](excel-worksheet-and-expression-evaluation.md)
- [<span data-ttu-id="4dc5f-133">Permitir intervenções de usuário em operações demoradas</span><span class="sxs-lookup"><span data-stu-id="4dc5f-133">Permitting User Breaks in Lengthy Operations</span></span>](permitting-user-breaks-in-lengthy-operations.md)
- [<span data-ttu-id="4dc5f-134">Introdução ao Excel XLL SDK</span><span class="sxs-lookup"><span data-stu-id="4dc5f-134">Getting Started with the Excel XLL SDK</span></span>](getting-started-with-the-excel-xll-sdk.md)

