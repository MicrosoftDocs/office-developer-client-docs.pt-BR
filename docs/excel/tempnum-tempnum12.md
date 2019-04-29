---
title: TempNum/TempNum12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempNum
- TempNum12
keywords:
- função tempnum12 [Excel 2007], função TempNum [Excel 2007]
localization_priority: Normal
ms.assetid: 5b74d618-db3a-4d84-bd17-4fee7ae3b51e
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: cabd44ab828a2cfe22253e9aaf12abf7b7709d69
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426629"
---
# <a name="tempnumtempnum12"></a><span data-ttu-id="31454-104">TempNum/TempNum12</span><span class="sxs-lookup"><span data-stu-id="31454-104">TempNum/TempNum12</span></span>

 <span data-ttu-id="31454-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="31454-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="31454-106">A função da biblioteca de estrutura que cria um **XLOPER de XLOPER**/ \*\*\*\* temporário contendo um número de planilha do Microsoft Excel (um duplo IEEE de 8 bytes).</span><span class="sxs-lookup"><span data-stu-id="31454-106">Framework library function that creates a temporary **XLOPER**/ **XLOPER12** containing a Microsoft Excel worksheet number (an IEEE 8-byte double).</span></span> 
  
```cs
LPXLOPER TempNum(double d);
LPXLOPER12 TempNum12(double d);
```

## <a name="parameters"></a><span data-ttu-id="31454-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="31454-107">Parameters</span></span>

 <span data-ttu-id="31454-108">_d_ (**duplo**)</span><span class="sxs-lookup"><span data-stu-id="31454-108">_d_ (**double**)</span></span>
  
<span data-ttu-id="31454-109">O valor desejado.</span><span class="sxs-lookup"><span data-stu-id="31454-109">The intended value.</span></span> <span data-ttu-id="31454-110">Observe que os números do IEEE sub-normal não têm suporte no momento e são arredondados para zero.</span><span class="sxs-lookup"><span data-stu-id="31454-110">Note that IEEE sub-normal numbers are not currently supported and are rounded to zero.</span></span> <span data-ttu-id="31454-111">O infinito negativo é suportado.</span><span class="sxs-lookup"><span data-stu-id="31454-111">Negative infinity is supported.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="31454-112">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="31454-112">Return value</span></span>

<span data-ttu-id="31454-113">Retorna um **xltypeNum** numérico que contém o valor passado ou zero se o valor passado em é sub-normal.</span><span class="sxs-lookup"><span data-stu-id="31454-113">Returns a numeric **xltypeNum** containing the value passed in or zero if the passed in value was sub-normal.</span></span> 
  
## <a name="example"></a><span data-ttu-id="31454-114">Exemplo</span><span class="sxs-lookup"><span data-stu-id="31454-114">Example</span></span>

<span data-ttu-id="31454-115">Este exemplo usa a função **TempNum12** para passar um argumento para **xlfGetWorkspace**.</span><span class="sxs-lookup"><span data-stu-id="31454-115">This example uses the **TempNum12** function to pass an argument to **xlfGetWorkspace**.</span></span>
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempNumExample(void)
{
   XLOPER12 xRes;
   Excel12f(xlfGetWorkspace, &xRes, 1, TempNum12(44));
   Excel12f(xlFree, 0, 1, (LPXLOPER12)&xRes);
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="31454-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="31454-116">See also</span></span>



[<span data-ttu-id="31454-117">Funções na biblioteca do Framework</span><span class="sxs-lookup"><span data-stu-id="31454-117">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

