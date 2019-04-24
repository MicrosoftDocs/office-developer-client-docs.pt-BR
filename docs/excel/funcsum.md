---
title: FuncSum
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- FuncSum
keywords:
- função funcsum [Excel 2007]
localization_priority: Normal
ms.assetid: 934192ef-8a89-4dbb-bd37-01e92ba24256
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 14db5812165812161cf7031f75338a981251dfd2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304057"
---
# <a name="funcsum"></a><span data-ttu-id="de75b-104">FuncSum</span><span class="sxs-lookup"><span data-stu-id="de75b-104">FuncSum</span></span>

 <span data-ttu-id="de75b-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="de75b-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="de75b-106">Exemplo de função de planilha definida pelo usuário que leva de 1 a 29 argumentos e computa sua soma.</span><span class="sxs-lookup"><span data-stu-id="de75b-106">Example user-defined worksheet function that takes 1 to 29 arguments and computes their sum.</span></span> <span data-ttu-id="de75b-107">Cada argumento pode ser um número único, um intervalo ou uma matriz.</span><span class="sxs-lookup"><span data-stu-id="de75b-107">Each argument can be a single number, a range, or an array.</span></span> <span data-ttu-id="de75b-108">Quando GENERIC. XLL é carregado, ele registra essa função para que ela possa ser chamada da planilha.</span><span class="sxs-lookup"><span data-stu-id="de75b-108">When GENERIC.xll is loaded, it registers this function so that it can be called from the worksheet.</span></span> 
  
```cs
LPXLOPER12 WINAPI FuncSum(LPXLOPER12 px1, LPXLOPER12 px2, LPXLOPER12 px3,LPXLOPER12 px4, LPXLOPER12 px5, LPXLOPER12 px6, LPXLOPER12 px7,LPXLOPER12 px8, LPXLOPER12 px9, LPXLOPER12 px10, LPXLOPER12 px11,LPXLOPER12 px12, LPXLOPER12 px13, LPXLOPER12 px14, LPXLOPER12 px15,LPXLOPER12 px16, LPXLOPER12 px17, LPXLOPER12 px18, LPXLOPER12 px19,LPXLOPER12 px20, LPXLOPER12 px21, LPXLOPER12 px22, LPXLOPER12 px23,LPXLOPER12 px24, LPXLOPER12 px25, LPXLOPER12 px26, LPXLOPER12 px27,LPXLOPER12 px28, LPXLOPER12 px29);
```

## <a name="parameters"></a><span data-ttu-id="de75b-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="de75b-109">Parameters</span></span>

 <span data-ttu-id="de75b-110">_PX1-px29_ (**LPXLOPER12**)</span><span class="sxs-lookup"><span data-stu-id="de75b-110">_px1-px29_ (**LPXLOPER12**)</span></span>
  
<span data-ttu-id="de75b-111">Ponteiros para argumentos **XLOPER12** .</span><span class="sxs-lookup"><span data-stu-id="de75b-111">Pointers to **XLOPER12** arguments.</span></span> <span data-ttu-id="de75b-112">A função aceita qualquer tipo de tipo de entrada, mas é codificada apenas para operar em números, matrizes literais de números e intervalos que contenham apenas números ou células em branco.</span><span class="sxs-lookup"><span data-stu-id="de75b-112">The function accepts any kind of input type but is coded only to operate on numbers, literal arrays of numbers, and ranges containing only numbers or blank cells.</span></span> <span data-ttu-id="de75b-113">Se forem fornecidos menos de 29 argumentos, os argumentos restantes serão fornecidos como **xltypeMissing**.</span><span class="sxs-lookup"><span data-stu-id="de75b-113">If fewer than 29 arguments are supplied, the remaining arguments are supplied as **xltypeMissing**.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="de75b-114">Valor de propriedade/Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="de75b-114">Property value/Return value</span></span>

<span data-ttu-id="de75b-115">(**LPXLOPER12 xltypeNum** ou **xltypeErr**)</span><span class="sxs-lookup"><span data-stu-id="de75b-115">(**LPXLOPER12 xltypeNum** or **xltypeErr**)</span></span>
  
<span data-ttu-id="de75b-116">A soma dos argumentos ou #VALUE!</span><span class="sxs-lookup"><span data-stu-id="de75b-116">The sum of the arguments or #VALUE!</span></span> <span data-ttu-id="de75b-117">Se houver não numéricos na lista de argumentos fornecidos ou em uma célula em um intervalo ou elemento em uma matriz.</span><span class="sxs-lookup"><span data-stu-id="de75b-117">if there are non-numerics in the supplied argument list or in a cell in a range or element in an array.</span></span>
  
### <a name="example"></a><span data-ttu-id="de75b-118">Exemplo</span><span class="sxs-lookup"><span data-stu-id="de75b-118">Example</span></span>

<span data-ttu-id="de75b-119">Consulte `\SAMPLES\GENERIC\GENERIC.C` o código-fonte para essa função.</span><span class="sxs-lookup"><span data-stu-id="de75b-119">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="de75b-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="de75b-120">See also</span></span>



[<span data-ttu-id="de75b-121">Funções na DLL genérica</span><span class="sxs-lookup"><span data-stu-id="de75b-121">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

