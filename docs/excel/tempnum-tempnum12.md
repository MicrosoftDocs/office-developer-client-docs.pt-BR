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
- função tempnum12 [excel 2007], função TempNum [Excel 2007]
localization_priority: Normal
ms.assetid: 5b74d618-db3a-4d84-bd17-4fee7ae3b51e
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 5ebe58dba32c2cf0382bf0811713eaa0a5471dda
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765441"
---
# <a name="tempnumtempnum12"></a><span data-ttu-id="90a67-104">TempNum/TempNum12</span><span class="sxs-lookup"><span data-stu-id="90a67-104">TempNum/TempNum12</span></span>

 <span data-ttu-id="90a67-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="90a67-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="90a67-106">Função da biblioteca de Framework que cria um temporário **XLOPER**/ **XLOPER12** contendo um número de planilha do Microsoft Excel (um double IEEE de 8 bytes).</span><span class="sxs-lookup"><span data-stu-id="90a67-106">Framework library function that creates a temporary **XLOPER**/ **XLOPER12** containing a Microsoft Excel worksheet number (an IEEE 8-byte double).</span></span> 
  
```cs
LPXLOPER TempNum(double d);
LPXLOPER12 TempNum12(double d);
```

## <a name="parameters"></a><span data-ttu-id="90a67-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="90a67-107">Parameters</span></span>

 <span data-ttu-id="90a67-108">_d_ (**double**)</span><span class="sxs-lookup"><span data-stu-id="90a67-108">_d_ (**double**)</span></span>
  
<span data-ttu-id="90a67-109">O valor desejado.</span><span class="sxs-lookup"><span data-stu-id="90a67-109">The intended value.</span></span> <span data-ttu-id="90a67-110">Observe que os números de sub-recursos normais padrão IEEE não são suportados atualmente e são arredondados para zero.</span><span class="sxs-lookup"><span data-stu-id="90a67-110">Note that IEEE sub-normal numbers are not currently supported and are rounded to zero.</span></span> <span data-ttu-id="90a67-111">Há suporte para infinito negativo.</span><span class="sxs-lookup"><span data-stu-id="90a67-111">Negative infinity is supported.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="90a67-112">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="90a67-112">Return value</span></span>

<span data-ttu-id="90a67-113">Retorna numéricos **xltypeNum** contendo o valor passado ou zero se o valor passado na era sub-recursos normal.</span><span class="sxs-lookup"><span data-stu-id="90a67-113">Returns a numeric **xltypeNum** containing the value passed in or zero if the passed in value was sub-normal.</span></span> 
  
## <a name="example"></a><span data-ttu-id="90a67-114">Exemplo</span><span class="sxs-lookup"><span data-stu-id="90a67-114">Example</span></span>

<span data-ttu-id="90a67-115">Este exemplo usa a função **TempNum12** para passar um argumento para **xlfGetWorkspace**.</span><span class="sxs-lookup"><span data-stu-id="90a67-115">This example uses the **TempNum12** function to pass an argument to **xlfGetWorkspace**.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="90a67-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="90a67-116">See also</span></span>



[<span data-ttu-id="90a67-117">Funções na biblioteca de estrutura</span><span class="sxs-lookup"><span data-stu-id="90a67-117">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

