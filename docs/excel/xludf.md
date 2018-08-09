---
title: xlUDF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlUDF
keywords:
- função xlUDF [excel 2007]
localization_priority: Normal
ms.assetid: b608b356-ca5c-47bb-9de8-9b7e2b3924dd
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 8f45f800ca50d2a46792e7cf5e00ac25bd099e8c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765492"
---
# <a name="xludf"></a><span data-ttu-id="45cba-104">xlUDF</span><span class="sxs-lookup"><span data-stu-id="45cba-104">xlUDF</span></span>

<span data-ttu-id="45cba-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="45cba-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="45cba-106">Chama uma função definida pelo usuário (UDF).</span><span class="sxs-lookup"><span data-stu-id="45cba-106">Calls a user-defined function (UDF).</span></span> <span data-ttu-id="45cba-107">Essa função permite que uma DLL chamar o Visual Basic para funções definidas pelo usuário do Applications (VBA), funções de idioma de macro XLM e funções registradas contidas em outros complementos.</span><span class="sxs-lookup"><span data-stu-id="45cba-107">This function allows a DLL to call Visual Basic for Applications (VBA) user-defined functions, XLM macro language functions, and registered functions contained in other add-ins.</span></span>
  
```cs
Excel12(xlUDF, LPXLOPER12 pxRes, int iCount, LPXLOPER12 pxFnRef,
LPXLOPER12 pxArg1, ...);
```

## <a name="parameters"></a><span data-ttu-id="45cba-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="45cba-108">Parameters</span></span>

<span data-ttu-id="45cba-109">_pxFnRef_ (**xltypeRef**, **xltypeSRef**, **xltypeStr** ou **xltypeNum**)</span><span class="sxs-lookup"><span data-stu-id="45cba-109">_pxFnRef_ (**xltypeRef**, **xltypeSRef**, **xltypeStr** or **xltypeNum**)</span></span>
  
<span data-ttu-id="45cba-110">A referência da função que você deseja chamar.</span><span class="sxs-lookup"><span data-stu-id="45cba-110">The reference of the function you want to call.</span></span> <span data-ttu-id="45cba-111">Isso pode ser uma referência de célula de planilha macro, o nome registrado da função como uma cadeia de caracteres ou a ID de registro da função.</span><span class="sxs-lookup"><span data-stu-id="45cba-111">This can be a macro sheet cell reference, the registered name of the function as a string, or the register ID of the function.</span></span> <span data-ttu-id="45cba-112">Para o suplemento funções XLL registradas usando **xlfRegister** ou **registrar** com o argumento _pxFunctionText_ fornecido, a ID pode ser obtida usando **xlfEvaluate** para pesquisar o nome.</span><span class="sxs-lookup"><span data-stu-id="45cba-112">For XLL add-in functions registered using **xlfRegister** or **REGISTER** with the argument  _pxFunctionText_ supplied, the ID can be obtained by using **xlfEvaluate** to look up the name.</span></span> 
  
<span data-ttu-id="45cba-113">_pxArg1,..._</span><span class="sxs-lookup"><span data-stu-id="45cba-113">_pxArg1, ..._</span></span>
  
<span data-ttu-id="45cba-114">Zero ou mais argumentos para a função definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="45cba-114">Zero or more arguments to the user-defined function.</span></span> <span data-ttu-id="45cba-115">Quando você chama essa função nas versões anteriores ao Excel 2007, o número máximo de argumentos adicionais que podem ser passados é 29, que é 30 incluindo _pxFnRef_.</span><span class="sxs-lookup"><span data-stu-id="45cba-115">When you are calling this function in versions earlier than Excel 2007, the maximum number of additional arguments that can be passed is 29, which is 30 including  _pxFnRef_.</span></span> <span data-ttu-id="45cba-116">Iniciando no Excel 2007, esse limite é promovido a 254, que é 255 incluindo _pxFnRef_.</span><span class="sxs-lookup"><span data-stu-id="45cba-116">Starting in Excel 2007, this limit is raised to 254, which is 255 including  _pxFnRef_.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="45cba-117">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="45cba-117">Return value</span></span>

<span data-ttu-id="45cba-118">Retorna o valor que a função definida pelo usuário retornada.</span><span class="sxs-lookup"><span data-stu-id="45cba-118">Returns whatever value the user-defined function returned.</span></span>
  
## <a name="example"></a><span data-ttu-id="45cba-119">Exemplo</span><span class="sxs-lookup"><span data-stu-id="45cba-119">Example</span></span>

<span data-ttu-id="45cba-120">O exemplo a seguir executa **TestMacro** na planilha Macro1 na BOOK1. XLS.</span><span class="sxs-lookup"><span data-stu-id="45cba-120">The following example runs **TestMacro** on sheet Macro1 in BOOK1.XLS.</span></span> <span data-ttu-id="45cba-121">Certifique-se de que a macro estiver em uma planilha chamada Macro1.</span><span class="sxs-lookup"><span data-stu-id="45cba-121">Make sure that the macro is on a sheet named Macro1.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="45cba-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="45cba-122">See also</span></span>

- [<span data-ttu-id="45cba-123">Funções da API de C que podem ser chamadas apenas de uma DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="45cba-123">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

