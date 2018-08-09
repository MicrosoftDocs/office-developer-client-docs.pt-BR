---
title: FuncSum
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- FuncSum
keywords:
- função funcsum [excel 2007]
localization_priority: Normal
ms.assetid: 934192ef-8a89-4dbb-bd37-01e92ba24256
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 0b991cf5cdae90522abc9512193ee556e4c6e6e1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765378"
---
# <a name="funcsum"></a><span data-ttu-id="2b8b2-104">FuncSum</span><span class="sxs-lookup"><span data-stu-id="2b8b2-104">FuncSum</span></span>

 <span data-ttu-id="2b8b2-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="2b8b2-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="2b8b2-106">Função de planilha definida pelo usuário de exemplo que leva argumentos de 1 a 29 e computa sua soma.</span><span class="sxs-lookup"><span data-stu-id="2b8b2-106">Example user-defined worksheet function that takes 1 to 29 arguments and computes their sum.</span></span> <span data-ttu-id="2b8b2-107">Cada argumento pode ser um único número, um intervalo ou uma matriz.</span><span class="sxs-lookup"><span data-stu-id="2b8b2-107">Each argument can be a single number, a range, or an array.</span></span> <span data-ttu-id="2b8b2-108">Quando GENERIC.xll é carregado, ele registra esta função para que ele possa ser chamado da planilha.</span><span class="sxs-lookup"><span data-stu-id="2b8b2-108">When GENERIC.xll is loaded, it registers this function so that it can be called from the worksheet.</span></span> 
  
```cs
LPXLOPER12 WINAPI FuncSum(LPXLOPER12 px1, LPXLOPER12 px2, LPXLOPER12 px3,LPXLOPER12 px4, LPXLOPER12 px5, LPXLOPER12 px6, LPXLOPER12 px7,LPXLOPER12 px8, LPXLOPER12 px9, LPXLOPER12 px10, LPXLOPER12 px11,LPXLOPER12 px12, LPXLOPER12 px13, LPXLOPER12 px14, LPXLOPER12 px15,LPXLOPER12 px16, LPXLOPER12 px17, LPXLOPER12 px18, LPXLOPER12 px19,LPXLOPER12 px20, LPXLOPER12 px21, LPXLOPER12 px22, LPXLOPER12 px23,LPXLOPER12 px24, LPXLOPER12 px25, LPXLOPER12 px26, LPXLOPER12 px27,LPXLOPER12 px28, LPXLOPER12 px29);
```

## <a name="parameters"></a><span data-ttu-id="2b8b2-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2b8b2-109">Parameters</span></span>

 <span data-ttu-id="2b8b2-110">_px1-px29_ (**LPXLOPER12**)</span><span class="sxs-lookup"><span data-stu-id="2b8b2-110">_px1-px29_ (**LPXLOPER12**)</span></span>
  
<span data-ttu-id="2b8b2-111">Ponteiros para os argumentos **XLOPER12** .</span><span class="sxs-lookup"><span data-stu-id="2b8b2-111">Pointers to **XLOPER12** arguments.</span></span> <span data-ttu-id="2b8b2-112">A função aceita qualquer tipo de tipo de entrada, mas é codificada somente para operar em números, literais matrizes de números e intervalos que contenham somente números ou células em branco.</span><span class="sxs-lookup"><span data-stu-id="2b8b2-112">The function accepts any kind of input type but is coded only to operate on numbers, literal arrays of numbers, and ranges containing only numbers or blank cells.</span></span> <span data-ttu-id="2b8b2-113">Se menos de 29 argumentos é fornecido, os argumentos restantes são fornecidos como **xltypeMissing**.</span><span class="sxs-lookup"><span data-stu-id="2b8b2-113">If fewer than 29 arguments are supplied, the remaining arguments are supplied as **xltypeMissing**.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="2b8b2-114">Valor de propriedade/Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="2b8b2-114">Property value/Return value</span></span>

<span data-ttu-id="2b8b2-115">(**XltypeNum LPXLOPER12** ou **xltypeErr**)</span><span class="sxs-lookup"><span data-stu-id="2b8b2-115">(**LPXLOPER12 xltypeNum** or **xltypeErr**)</span></span>
  
<span data-ttu-id="2b8b2-116">A soma dos argumentos ou #VALUE!</span><span class="sxs-lookup"><span data-stu-id="2b8b2-116">The sum of the arguments or #VALUE!</span></span> <span data-ttu-id="2b8b2-117">Se houver não-numéricos na lista de argumentos fornecidos ou em uma célula em um intervalo ou de um elemento em uma matriz.</span><span class="sxs-lookup"><span data-stu-id="2b8b2-117">if there are non-numerics in the supplied argument list or in a cell in a range or element in an array.</span></span>
  
### <a name="example"></a><span data-ttu-id="2b8b2-118">Exemplo</span><span class="sxs-lookup"><span data-stu-id="2b8b2-118">Example</span></span>

<span data-ttu-id="2b8b2-119">Consulte `\SAMPLES\GENERIC\GENERIC.C` para o código-fonte para essa função.</span><span class="sxs-lookup"><span data-stu-id="2b8b2-119">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2b8b2-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="2b8b2-120">See also</span></span>



[<span data-ttu-id="2b8b2-121">Funções na DLL genérica</span><span class="sxs-lookup"><span data-stu-id="2b8b2-121">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

