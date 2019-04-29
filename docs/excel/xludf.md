---
title: xlUDF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlUDF
keywords:
- função xlUDF [Excel 2007]
localization_priority: Normal
ms.assetid: b608b356-ca5c-47bb-9de8-9b7e2b3924dd
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 569334847c7612b86f6ddc967f159e2ef425cbbb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430641"
---
# <a name="xludf"></a><span data-ttu-id="f9b2f-104">xlUDF</span><span class="sxs-lookup"><span data-stu-id="f9b2f-104">xlUDF</span></span>

<span data-ttu-id="f9b2f-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f9b2f-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="f9b2f-106">Chama uma função definida pelo usuário (UDF).</span><span class="sxs-lookup"><span data-stu-id="f9b2f-106">Calls a user-defined function (UDF).</span></span> <span data-ttu-id="f9b2f-107">Essa função permite que uma DLL chame funções definidas pelo usuário do Visual Basic for Applications (VBA), funções de linguagem de macro XLM e funções registradas contidas em outros suplementos.</span><span class="sxs-lookup"><span data-stu-id="f9b2f-107">This function allows a DLL to call Visual Basic for Applications (VBA) user-defined functions, XLM macro language functions, and registered functions contained in other add-ins.</span></span>
  
```cs
Excel12(xlUDF, LPXLOPER12 pxRes, int iCount, LPXLOPER12 pxFnRef,
LPXLOPER12 pxArg1, ...);
```

## <a name="parameters"></a><span data-ttu-id="f9b2f-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f9b2f-108">Parameters</span></span>

<span data-ttu-id="f9b2f-109">_pxFnRef_ (**xltypeRef**, **xltypeSRef**, **xltypeStr** ou **xltypeNum**)</span><span class="sxs-lookup"><span data-stu-id="f9b2f-109">_pxFnRef_ (**xltypeRef**, **xltypeSRef**, **xltypeStr** or **xltypeNum**)</span></span>
  
<span data-ttu-id="f9b2f-110">A referência da função que você deseja chamar.</span><span class="sxs-lookup"><span data-stu-id="f9b2f-110">The reference of the function you want to call.</span></span> <span data-ttu-id="f9b2f-111">Pode ser uma referência de célula de planilha de macro, o nome registrado da função como uma cadeia de caracteres ou a ID de registro da função.</span><span class="sxs-lookup"><span data-stu-id="f9b2f-111">This can be a macro sheet cell reference, the registered name of the function as a string, or the register ID of the function.</span></span> <span data-ttu-id="f9b2f-112">Para funções de suplemento XLL registradas usando **xlfRegister** ou **Register** com o argumento _pxFunctionText_ fornecido, a ID pode ser obtida usando o **xlfEvaluate** para pesquisar o nome.</span><span class="sxs-lookup"><span data-stu-id="f9b2f-112">For XLL add-in functions registered using **xlfRegister** or **REGISTER** with the argument  _pxFunctionText_ supplied, the ID can be obtained by using **xlfEvaluate** to look up the name.</span></span> 
  
<span data-ttu-id="f9b2f-113">_pxArg1,..._</span><span class="sxs-lookup"><span data-stu-id="f9b2f-113">_pxArg1, ..._</span></span>
  
<span data-ttu-id="f9b2f-114">Zero ou mais argumentos para a função definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="f9b2f-114">Zero or more arguments to the user-defined function.</span></span> <span data-ttu-id="f9b2f-115">Quando você chama essa função em versões anteriores ao Excel 2007, o número máximo de argumentos adicionais que podem ser passados é 29, que é 30 incluindo _pxFnRef_.</span><span class="sxs-lookup"><span data-stu-id="f9b2f-115">When you are calling this function in versions earlier than Excel 2007, the maximum number of additional arguments that can be passed is 29, which is 30 including  _pxFnRef_.</span></span> <span data-ttu-id="f9b2f-116">A partir do Excel 2007, esse limite é aumentado para 254, que é 255, incluindo _pxFnRef_.</span><span class="sxs-lookup"><span data-stu-id="f9b2f-116">Starting in Excel 2007, this limit is raised to 254, which is 255 including  _pxFnRef_.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="f9b2f-117">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="f9b2f-117">Return value</span></span>

<span data-ttu-id="f9b2f-118">Retorna qualquer valor retornado pela função definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="f9b2f-118">Returns whatever value the user-defined function returned.</span></span>
  
## <a name="example"></a><span data-ttu-id="f9b2f-119">Exemplo</span><span class="sxs-lookup"><span data-stu-id="f9b2f-119">Example</span></span>

<span data-ttu-id="f9b2f-120">O exemplo a seguir executa o **TestMacro** na planilha MACRO1 no BOOK1. XLS.</span><span class="sxs-lookup"><span data-stu-id="f9b2f-120">The following example runs **TestMacro** on sheet Macro1 in BOOK1.XLS.</span></span> <span data-ttu-id="f9b2f-121">Certifique-se de que a macro está em uma planilha chamada Macro1.</span><span class="sxs-lookup"><span data-stu-id="f9b2f-121">Make sure that the macro is on a sheet named Macro1.</span></span> 
  
`\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlUDFExample(void)
{       
   XLOPER12 xMacroName, xMacroRef, xRes;
   xMacroName.xltype = xltypeStr;
   xMacroName.val.str = L"\044[BOOK1.XLSX]Macro1!TestMacro";
   Excel12(xlfEvaluate, &xMacroRef, 1, (LPXLOPER12)&xMacroName);
   Excel12(xlUDF, &xRes, 1, (LPXLOPER12)&xMacroRef);
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="f9b2f-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="f9b2f-122">See also</span></span>

- [<span data-ttu-id="f9b2f-123">Funções da API de C que podem ser chamadas apenas de uma DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="f9b2f-123">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

