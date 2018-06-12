---
title: xlStack
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlStack
keywords:
- função xlStack [excel 2007]
localization_priority: Normal
ms.assetid: f9f030e8-1ec9-4cbf-92e1-360526260916
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: fcd073f7d2b97e84743d01c498435f186277e345
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765482"
---
# <a name="xlstack"></a><span data-ttu-id="48515-104">xlStack</span><span class="sxs-lookup"><span data-stu-id="48515-104">xlStack</span></span>

<span data-ttu-id="48515-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="48515-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="48515-106">Verifica a quantidade de espaço deixado na pilha.</span><span class="sxs-lookup"><span data-stu-id="48515-106">Checks the amount of space left on the stack.</span></span>
  
```cs
Excel12(xlStack, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a><span data-ttu-id="48515-107">Par�metros</span><span class="sxs-lookup"><span data-stu-id="48515-107">Parameters</span></span>

<span data-ttu-id="48515-108">Essa função não assume nenhum argumento.</span><span class="sxs-lookup"><span data-stu-id="48515-108">This function takes no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="48515-109">Propriedade valor/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="48515-109">Property value/Return value</span></span>

<span data-ttu-id="48515-110">Retorna o número de bytes (**xltypeInt**) restante na pilha.</span><span class="sxs-lookup"><span data-stu-id="48515-110">Returns the number of bytes (**xltypeInt**) remaining on the stack.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="48515-111">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="48515-111">Remarks</span></span>

<span data-ttu-id="48515-112">A quantidade de espaço de pilha disponível das versões recentes estouros de inteiro assinado de 16 bits de **XLOPER**.</span><span class="sxs-lookup"><span data-stu-id="48515-112">The amount of available stack space of recent versions overflows the 16-bit signed integer of the **XLOPER**.</span></span> <span data-ttu-id="48515-113">Isso significa que **xlStack** pode retornar um valor entre-32767 e 32768 quando chamado usando **XLOPER**s e **Excel4** ou **Excel4v**.</span><span class="sxs-lookup"><span data-stu-id="48515-113">This means that **xlStack** can return a value between -32767 and 32768 when called using **XLOPER**s and **Excel4** or **Excel4v**.</span></span> <span data-ttu-id="48515-114">Para obter o valor correto, nesse caso, você deve converter o valor retornado para um unsigned short.</span><span class="sxs-lookup"><span data-stu-id="48515-114">To obtain the correct value in this case, you must cast the returned value to an unsigned short.</span></span>
  
<span data-ttu-id="48515-115">Iniciando no Excel 2007, você deve chamar essa função usando **XLOPER12**s e **Excel12** ou **Excel12v**, caso em que o valor retornado será a quantidade de espaço em pilha disponível ou de 64 KB, o que for o menor.</span><span class="sxs-lookup"><span data-stu-id="48515-115">Starting in Excel 2007, you should call this function using **XLOPER12**s and **Excel12** or **Excel12v**, in which case the returned value is amount of stack space available or 64 KB, whichever is the lesser.</span></span>
  
<span data-ttu-id="48515-116">O Excel tem uma quantidade de espaço limitada na pilha e você deve ter cuidado para não saturação esse espaço.</span><span class="sxs-lookup"><span data-stu-id="48515-116">Excel has a limited amount of space on the stack, and you should take care not to overrun this space.</span></span> <span data-ttu-id="48515-117">Nunca colocado estruturas de dados muito grande na pilha e faça como muitas variáveis locais quanto possível estático.</span><span class="sxs-lookup"><span data-stu-id="48515-117">Never put very large data structures on the stack, and make as many local variables as possible static.</span></span> <span data-ttu-id="48515-118">Evite chamando funções recursivamente, porque o que será preenchido rapidamente a pilha de itens.</span><span class="sxs-lookup"><span data-stu-id="48515-118">Avoid calling functions recursively, because that will quickly fill up the stack.</span></span>
  
<span data-ttu-id="48515-119">Se você achar que você está saturar a pilha, chame essa função com frequência para ver quanto espaço em pilha é da esquerda.</span><span class="sxs-lookup"><span data-stu-id="48515-119">If you suspect that you are overrunning the stack, call this function frequently to see how much stack space is left.</span></span>
  
## <a name="example"></a><span data-ttu-id="48515-120">Example</span><span class="sxs-lookup"><span data-stu-id="48515-120">Example</span></span>

<span data-ttu-id="48515-121">O primeiro exemplo exibe uma mensagem de alerta contendo a quantidade de espaço de pilha deixado e está contido no `\SAMPLES\EXAMPLE\EXAMPLE.C`.</span><span class="sxs-lookup"><span data-stu-id="48515-121">The first example displays an alert message containing the amount of stack space left and is contained in  `\SAMPLES\EXAMPLE\EXAMPLE.C`.</span></span> <span data-ttu-id="48515-122">O segundo exemplo faz a mesma coisa, trabalhando com **XLOPER**s e não está contido no código de exemplo do SDK.</span><span class="sxs-lookup"><span data-stu-id="48515-122">The second example does the same thing, working with **XLOPER**s and is not contained in the SDK example code.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="48515-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="48515-123">See also</span></span>

- [<span data-ttu-id="48515-124">Funções da API C que podem ser chamadas apenas por um DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="48515-124">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

