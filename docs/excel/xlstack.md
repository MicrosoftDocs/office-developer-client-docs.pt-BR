---
title: xlStack
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlStack
keywords:
- função xlstack [excel 2007]
localization_priority: Normal
ms.assetid: f9f030e8-1ec9-4cbf-92e1-360526260916
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 55ceed93407b1d99e05bc20fb6ce0b22459de7df
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429976"
---
# <a name="xlstack"></a><span data-ttu-id="fcecc-104">xlStack</span><span class="sxs-lookup"><span data-stu-id="fcecc-104">xlStack</span></span>

<span data-ttu-id="fcecc-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="fcecc-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="fcecc-106">Verifica a quantidade de espaço que resta na pilha.</span><span class="sxs-lookup"><span data-stu-id="fcecc-106">Checks the amount of space left on the stack.</span></span>
  
```cs
Excel12(xlStack, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a><span data-ttu-id="fcecc-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fcecc-107">Parameters</span></span>

<span data-ttu-id="fcecc-108">Essa função não usa argumentos.</span><span class="sxs-lookup"><span data-stu-id="fcecc-108">This function takes no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="fcecc-109">Valor de propriedade/Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="fcecc-109">Property value/Return value</span></span>

<span data-ttu-id="fcecc-110">Retorna o número de bytes (**xltypeInt**) restantes na pilha.</span><span class="sxs-lookup"><span data-stu-id="fcecc-110">Returns the number of bytes (**xltypeInt**) remaining on the stack.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fcecc-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="fcecc-111">Remarks</span></span>

<span data-ttu-id="fcecc-112">A quantidade de espaço em pilha disponível de versões recentes excedentes ao inteiro assinado de 16 bits do **XLOPER**.</span><span class="sxs-lookup"><span data-stu-id="fcecc-112">The amount of available stack space of recent versions overflows the 16-bit signed integer of the **XLOPER**.</span></span> <span data-ttu-id="fcecc-113">Isso significa que **xlStack** pode retornar um valor entre -32767 e 32768 quando chamado usando **XLOPER** s e **Excel4** ou **Excel4v**.</span><span class="sxs-lookup"><span data-stu-id="fcecc-113">This means that **xlStack** can return a value between -32767 and 32768 when called using **XLOPER** s and **Excel4** or **Excel4v**.</span></span> <span data-ttu-id="fcecc-114">Para obter o valor correto nesse caso, você deve lançar o valor retornado para um curto não assinado.</span><span class="sxs-lookup"><span data-stu-id="fcecc-114">To obtain the correct value in this case, you must cast the returned value to an unsigned short.</span></span>
  
<span data-ttu-id="fcecc-115">A partir do Excel 2007, você deve chamar essa função usando **XLOPER12** s e **Excel12** ou **Excel12v**, nesse caso, o valor retornado é a quantidade de espaço em pilha disponível ou 64 KB, o que for menor.</span><span class="sxs-lookup"><span data-stu-id="fcecc-115">Starting in Excel 2007, you should call this function using **XLOPER12** s and **Excel12** or **Excel12v**, in which case the returned value is amount of stack space available or 64 KB, whichever is the lesser.</span></span>
  
<span data-ttu-id="fcecc-116">O Excel tem uma quantidade limitada de espaço na pilha, e você deve ter cuidado para não sobrecarr o espaço.</span><span class="sxs-lookup"><span data-stu-id="fcecc-116">Excel has a limited amount of space on the stack, and you should take care not to overrun this space.</span></span> <span data-ttu-id="fcecc-117">Nunca coloque estruturas de dados muito grandes na pilha e faça o máximo possível de variáveis locais estáticas.</span><span class="sxs-lookup"><span data-stu-id="fcecc-117">Never put very large data structures on the stack, and make as many local variables as possible static.</span></span> <span data-ttu-id="fcecc-118">Evite chamar funções recursivamente, pois isso preencherá rapidamente a pilha.</span><span class="sxs-lookup"><span data-stu-id="fcecc-118">Avoid calling functions recursively, because that will quickly fill up the stack.</span></span>
  
<span data-ttu-id="fcecc-119">Se você suspeitar que está anulando a pilha, chame essa função com frequência para ver quanto espaço na pilha é deixado.</span><span class="sxs-lookup"><span data-stu-id="fcecc-119">If you suspect that you are overrunning the stack, call this function frequently to see how much stack space is left.</span></span>
  
## <a name="example"></a><span data-ttu-id="fcecc-120">Exemplo</span><span class="sxs-lookup"><span data-stu-id="fcecc-120">Example</span></span>

<span data-ttu-id="fcecc-121">O primeiro exemplo exibe uma mensagem de alerta contendo a quantidade de espaço em pilha à esquerda e está contida em  `\SAMPLES\EXAMPLE\EXAMPLE.C` .</span><span class="sxs-lookup"><span data-stu-id="fcecc-121">The first example displays an alert message containing the amount of stack space left and is contained in  `\SAMPLES\EXAMPLE\EXAMPLE.C`.</span></span> <span data-ttu-id="fcecc-122">O segundo exemplo faz a mesma coisa, trabalhando com **XLOPER** s e não está contido no código de exemplo do SDK.</span><span class="sxs-lookup"><span data-stu-id="fcecc-122">The second example does the same thing, working with **XLOPER** s and is not contained in the SDK example code.</span></span>
  
```cs
short WINAPI xlStackExample(void)
{
   XLOPER12 xRes;
   Excel12(xlStack, &xRes, 0);
   Excel12(xlcAlert, 0, 1, (LPXLOPER12)&xRes);
   return 1;
} 
short int WINAPI xlStackExample_XLOPER(void)
{
    XLOPER xRes;
    Excel4(xlStack, (LPXLOPER)&xRes, 0);
    xRes.xltype = xltypeNum; // Change the type to double
    // Cast to an unsigned short to get rid of the overflow problem
    xRes.val.num = (double)(unsigned short) xRes.val.w;
    Excel4(xlcAlert, 0, 1, (LPXLOPER)& xRes);
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="fcecc-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="fcecc-123">See also</span></span>

- [<span data-ttu-id="fcecc-124">Funções da API de C que podem ser chamadas apenas de uma DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="fcecc-124">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

