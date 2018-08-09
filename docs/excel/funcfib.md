---
title: FuncFib
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- FuncFib
keywords:
- função funcfib [excel 2007]
localization_priority: Normal
ms.assetid: 6a719f04-b2d1-4f87-a227-be561cbd3e49
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 8d1c97ea57e968aaedffca6b37ded3d875e87413
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765370"
---
# <a name="funcfib"></a><span data-ttu-id="a8a3b-104">FuncFib</span><span class="sxs-lookup"><span data-stu-id="a8a3b-104">FuncFib</span></span>

 <span data-ttu-id="a8a3b-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="a8a3b-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="a8a3b-106">Função de planilha definida pelo usuário de exemplo que computa o número de Fibonacci enésima.</span><span class="sxs-lookup"><span data-stu-id="a8a3b-106">Example user-defined worksheet function that computes the Nth Fibonacci number.</span></span> <span data-ttu-id="a8a3b-107">Quando GENERIC.xll é carregado, ele registra esta função para que ele possa ser chamado da planilha.</span><span class="sxs-lookup"><span data-stu-id="a8a3b-107">When GENERIC.xll is loaded, it registers this function so that it can be called from the worksheet.</span></span>
  
```cs
LPXLOPER12 WINAPI FuncFib (LPXLOPER12 pxN);
```

## <a name="parameters"></a><span data-ttu-id="a8a3b-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a8a3b-108">Parameters</span></span>

 <span data-ttu-id="a8a3b-109">_pxN_ (**LPXLOPER12**)</span><span class="sxs-lookup"><span data-stu-id="a8a3b-109">_pxN_ (**LPXLOPER12**)</span></span>
  
<span data-ttu-id="a8a3b-110">O valor de N para o qual o número de Fibonacci enésima é necessário.</span><span class="sxs-lookup"><span data-stu-id="a8a3b-110">The value of N for which the Nth Fibonacci number is required.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="a8a3b-111">Valor de propriedade/Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="a8a3b-111">Property value/Return value</span></span>

<span data-ttu-id="a8a3b-112">(**xltypeNum LPXLOPER12** se tiver êxito ou **xltypeErr** caso contrário)</span><span class="sxs-lookup"><span data-stu-id="a8a3b-112">(**xltypeNum LPXLOPER12** if successful or **xltypeErr** otherwise)</span></span> 
  
<span data-ttu-id="a8a3b-113">O número de Fibonacci enésima.</span><span class="sxs-lookup"><span data-stu-id="a8a3b-113">The Nth Fibonacci number.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a8a3b-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="a8a3b-114">Remarks</span></span>

<span data-ttu-id="a8a3b-115">A função usa uma variável estática definida dentro do bloco de função, como o valor de retorno **XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="a8a3b-115">The function uses a static variable defined within the function block as the return value **XLOPER12**.</span></span> <span data-ttu-id="a8a3b-116">Isso não é thread-safe e, portanto essa função e qualquer função de planilha que usa essa estratégia para retornar **XLOPER**s ou s **XLOPER12**, não devem ser registradas como thread-safe iniciada no Excel 2007.</span><span class="sxs-lookup"><span data-stu-id="a8a3b-116">This is not thread safe, and so this function, and any worksheet function that uses this strategy for returning **XLOPER**s or **XLOPER12**s, should not be registered as thread safe starting in Excel 2007.</span></span>
  
### <a name="example"></a><span data-ttu-id="a8a3b-117">Exemplo</span><span class="sxs-lookup"><span data-stu-id="a8a3b-117">Example</span></span>

<span data-ttu-id="a8a3b-118">Consulte `\SAMPLES\GENERIC\GENERIC.C` para o código-fonte para essa função.</span><span class="sxs-lookup"><span data-stu-id="a8a3b-118">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a8a3b-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="a8a3b-119">See also</span></span>



[<span data-ttu-id="a8a3b-120">Funções na DLL genérica</span><span class="sxs-lookup"><span data-stu-id="a8a3b-120">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

