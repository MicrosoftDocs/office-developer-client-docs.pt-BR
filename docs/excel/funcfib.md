---
title: FuncFib
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- FuncFib
keywords:
- função funcfib [Excel 2007]
localization_priority: Normal
ms.assetid: 6a719f04-b2d1-4f87-a227-be561cbd3e49
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: fb8f0c12c27fb2c95007eb5006c1d8b90970f3ad
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310833"
---
# <a name="funcfib"></a><span data-ttu-id="a6b1a-104">FuncFib</span><span class="sxs-lookup"><span data-stu-id="a6b1a-104">FuncFib</span></span>

 <span data-ttu-id="a6b1a-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="a6b1a-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="a6b1a-106">Exemplo de função de planilha definida pelo usuário que computa o número enésimo Fibonacci.</span><span class="sxs-lookup"><span data-stu-id="a6b1a-106">Example user-defined worksheet function that computes the Nth Fibonacci number.</span></span> <span data-ttu-id="a6b1a-107">Quando GENERIC. XLL é carregado, ele registra essa função para que ela possa ser chamada da planilha.</span><span class="sxs-lookup"><span data-stu-id="a6b1a-107">When GENERIC.xll is loaded, it registers this function so that it can be called from the worksheet.</span></span>
  
```cs
LPXLOPER12 WINAPI FuncFib (LPXLOPER12 pxN);
```

## <a name="parameters"></a><span data-ttu-id="a6b1a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a6b1a-108">Parameters</span></span>

 <span data-ttu-id="a6b1a-109">_pxN_ (**LPXLOPER12**)</span><span class="sxs-lookup"><span data-stu-id="a6b1a-109">_pxN_ (**LPXLOPER12**)</span></span>
  
<span data-ttu-id="a6b1a-110">O valor de N para o qual o enésimo número Fibonacci é necessário.</span><span class="sxs-lookup"><span data-stu-id="a6b1a-110">The value of N for which the Nth Fibonacci number is required.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="a6b1a-111">Valor de propriedade/Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="a6b1a-111">Property value/Return value</span></span>

<span data-ttu-id="a6b1a-112">(**XLTYPENUM LPXLOPER12** se for bem-sucedido ou **xltypeErr** caso contrário)</span><span class="sxs-lookup"><span data-stu-id="a6b1a-112">(**xltypeNum LPXLOPER12** if successful or **xltypeErr** otherwise)</span></span> 
  
<span data-ttu-id="a6b1a-113">O número enésimo Fibonacci.</span><span class="sxs-lookup"><span data-stu-id="a6b1a-113">The Nth Fibonacci number.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a6b1a-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="a6b1a-114">Remarks</span></span>

<span data-ttu-id="a6b1a-115">A função usa uma variável estática definida dentro do bloco de funções como o valor de retorno **XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="a6b1a-115">The function uses a static variable defined within the function block as the return value **XLOPER12**.</span></span> <span data-ttu-id="a6b1a-116">Isso não é thread-safe e, portanto, essa função e qualquer função de planilha que use essa estratégia para retornar **XLOPER**s ou **XLOPER12**s, não deve ser registrada como thread-safe a partir do Excel 2007.</span><span class="sxs-lookup"><span data-stu-id="a6b1a-116">This is not thread safe, and so this function, and any worksheet function that uses this strategy for returning **XLOPER**s or **XLOPER12**s, should not be registered as thread safe starting in Excel 2007.</span></span>
  
### <a name="example"></a><span data-ttu-id="a6b1a-117">Exemplo</span><span class="sxs-lookup"><span data-stu-id="a6b1a-117">Example</span></span>

<span data-ttu-id="a6b1a-118">Consulte `\SAMPLES\GENERIC\GENERIC.C` o código-fonte para essa função.</span><span class="sxs-lookup"><span data-stu-id="a6b1a-118">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a6b1a-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="a6b1a-119">See also</span></span>



[<span data-ttu-id="a6b1a-120">Funções na DLL genérica</span><span class="sxs-lookup"><span data-stu-id="a6b1a-120">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

