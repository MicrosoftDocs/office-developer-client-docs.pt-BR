---
title: Excel4v/Excel12v
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Excel12v
- Excel4v
keywords:
- função excel12v [excel 2007],função Excel4v [Excel 2007]
localization_priority: Normal
ms.assetid: e3e96b98-c5a7-4625-95b6-a1e2d09c6d3d
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 11ab86a95dde2ad52840822b28ce4d74dd05d148
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414988"
---
# <a name="excel4vexcel12v"></a><span data-ttu-id="a45b8-104">Excel4v/Excel12v</span><span class="sxs-lookup"><span data-stu-id="a45b8-104">Excel4v/Excel12v</span></span>

 <span data-ttu-id="a45b8-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="a45b8-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="a45b8-106">Chama uma função de planilha interna do Microsoft Excel, função ou comando de planilha de macro ou comando especial somente XLL, de dentro de uma DLL, XLL ou recurso de código.</span><span class="sxs-lookup"><span data-stu-id="a45b8-106">Calls an internal Microsoft Excel worksheet function, macro sheet function or command, or XLL-only special function or command, from within a DLL, XLL, or code resource.</span></span>
  
<span data-ttu-id="a45b8-107">Todas as versões recentes do Excel são **suportadas pelo Excel4v.**</span><span class="sxs-lookup"><span data-stu-id="a45b8-107">All recent versions of Excel support **Excel4v**.</span></span> <span data-ttu-id="a45b8-108">A partir do Excel 2007, **o Excel12v** é suportado.</span><span class="sxs-lookup"><span data-stu-id="a45b8-108">Starting in Excel 2007, **Excel12v** is supported.</span></span> 
  
<span data-ttu-id="a45b8-109">Essas funções podem ser chamadas somente quando o Excel tiver passado o controle para a DLL ou XLL.</span><span class="sxs-lookup"><span data-stu-id="a45b8-109">These functions can be called only when Excel has passed control to the DLL or XLL.</span></span> <span data-ttu-id="a45b8-110">Eles também podem ser chamados quando o Excel tiver passado pelo controle indiretamente por meio de uma chamada para o VBA (Visual Basic for Applications).</span><span class="sxs-lookup"><span data-stu-id="a45b8-110">They can also be called when Excel has passed control indirectly via a call to Visual Basic for Applications (VBA).</span></span> <span data-ttu-id="a45b8-111">Eles não podem ser chamados em nenhum outro momento.</span><span class="sxs-lookup"><span data-stu-id="a45b8-111">They cannot be called at any other time.</span></span> <span data-ttu-id="a45b8-112">Por exemplo, eles não podem ser chamados durante chamadas para a função DllMain ou outras vezes quando o sistema operacional tiver chamado a DLL ou de um thread criado pela DLL.</span><span class="sxs-lookup"><span data-stu-id="a45b8-112">For example, they cannot be called during calls to the DllMain function or other times when the operating system has called the DLL, or from a thread created by the DLL.</span></span> 
  
<span data-ttu-id="a45b8-113">As funções Excel4 e [Excel12](excel4-excel12.md) aceitam seus argumentos como uma lista de comprimento variável na pilha, enquanto as funções **Excel4v** e **Excel12v** aceitam seus argumentos como uma matriz.</span><span class="sxs-lookup"><span data-stu-id="a45b8-113">The [Excel4 and Excel12](excel4-excel12.md) functions accept their arguments as a variable length list on the stack, whereas the **Excel4v** and **Excel12v** functions accept their arguments as an array.</span></span> <span data-ttu-id="a45b8-114">Em todos os outros aspectos, **o Excel4** se comporta da mesma forma que o **Excel4v** e o **Excel12** se comporta da mesma forma que o **Excel12v.**</span><span class="sxs-lookup"><span data-stu-id="a45b8-114">In all other respects, **Excel4** behaves the same as **Excel4v**, and **Excel12** behaves the same as **Excel12v**.</span></span>
  
```cs
int _cdecl Excel4v(int iFunction, LPXLOPER pxRes, int iCount, LPXLOPER rgx[]);
int _cdecl Excel12v(int iFunction, LPXLOPER12 pxRes, int iCount, LPXLOPER12 rgx[]);
```

## <a name="parameters"></a><span data-ttu-id="a45b8-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a45b8-115">Parameters</span></span>

 <span data-ttu-id="a45b8-116">_iFunction_ (**int**)</span><span class="sxs-lookup"><span data-stu-id="a45b8-116">_iFunction_ (**int**)</span></span>
  
<span data-ttu-id="a45b8-117">Um número que indica o comando, a função ou a função especial que você deseja chamar.</span><span class="sxs-lookup"><span data-stu-id="a45b8-117">A number that indicates the command, function, or special function you want to call.</span></span> <span data-ttu-id="a45b8-118">Para uma lista de valores  _válidos de iFunction,_ consulte a seção Comentários a seguir.</span><span class="sxs-lookup"><span data-stu-id="a45b8-118">For a list of valid  _iFunction_ values, see the following Remarks section.</span></span> 
  
 <span data-ttu-id="a45b8-119">_pxRes_ (**LPXLOPER** ou **LPXLOPER12**)</span><span class="sxs-lookup"><span data-stu-id="a45b8-119">_pxRes_ (**LPXLOPER** or **LPXLOPER12**)</span></span>
  
<span data-ttu-id="a45b8-120">Um ponteiro para um **XLOPER** (no caso de **Excel4v**) ou um **XLOPER12** (no caso de **Excel12v**) que conterá o resultado da função avaliada.</span><span class="sxs-lookup"><span data-stu-id="a45b8-120">A pointer to an **XLOPER** (in the case of **Excel4v**) or an **XLOPER12** (in the case of **Excel12v**) that will hold the result of the evaluated function.</span></span>
  
 <span data-ttu-id="a45b8-121">_iCount_ (**int**)</span><span class="sxs-lookup"><span data-stu-id="a45b8-121">_iCount_ (**int**)</span></span>
  
<span data-ttu-id="a45b8-122">O número de argumentos subsequentes que serão passados para a função.</span><span class="sxs-lookup"><span data-stu-id="a45b8-122">The number of subsequent arguments that will be passed to the function.</span></span> <span data-ttu-id="a45b8-123">Em versões do Excel até 2003, pode ser qualquer número de 0 a 30.</span><span class="sxs-lookup"><span data-stu-id="a45b8-123">In versions of Excel up to 2003 this can be any number from 0 through 30.</span></span> <span data-ttu-id="a45b8-124">A partir do Excel 2007, pode ser qualquer número de 0 a 255.</span><span class="sxs-lookup"><span data-stu-id="a45b8-124">Starting in Excel 2007, this can be any number from 0 through 255.</span></span>
  
 <span data-ttu-id="a45b8-125">_rgx_ (**LPXLOPER []** ou **LPXLOPER12 []**)</span><span class="sxs-lookup"><span data-stu-id="a45b8-125">_rgx_ (**LPXLOPER []** or **LPXLOPER12 []**)</span></span>
  
<span data-ttu-id="a45b8-126">Uma matriz que contém os argumentos para a função.</span><span class="sxs-lookup"><span data-stu-id="a45b8-126">An array that contains the arguments to the function.</span></span> <span data-ttu-id="a45b8-127">Todos os argumentos na matriz devem ser ponteiros para valores **XLOPER** ou **XLOPER12.**</span><span class="sxs-lookup"><span data-stu-id="a45b8-127">All arguments in the array must be pointers to **XLOPER** or **XLOPER12** values.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="a45b8-128">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="a45b8-128">Return value</span></span>

<span data-ttu-id="a45b8-129">Essas funções retornam os mesmos valores que **Excel4** e **Excel12**.</span><span class="sxs-lookup"><span data-stu-id="a45b8-129">These functions return the same values as **Excel4** and **Excel12**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a45b8-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="a45b8-130">Remarks</span></span>

<span data-ttu-id="a45b8-131">Essas funções são úteis onde o número de argumentos passados para o operador é variável.</span><span class="sxs-lookup"><span data-stu-id="a45b8-131">These functions are useful where the number of arguments passed to the operator is variable.</span></span> <span data-ttu-id="a45b8-132">Por exemplo, **Excel4v** e **Excel12v** são úteis quando você registra funções usando [xlfRegister](xlfregister-form-1.md) onde o número do total de argumentos depende do número de argumentos tomadas pela função que está sendo registrada.</span><span class="sxs-lookup"><span data-stu-id="a45b8-132">For example, **Excel4v** and **Excel12v** are useful when you register functions by using [xlfRegister](xlfregister-form-1.md) where the number of total arguments depends on the number of arguments taken by the function being registered.</span></span> <span data-ttu-id="a45b8-133">**Excel4v** e **Excel12v** também são úteis quando você escreve uma função wrapper para **Excel4** ou **Excel12**.</span><span class="sxs-lookup"><span data-stu-id="a45b8-133">**Excel4v** and **Excel12v** are also useful when you write a wrapper function for **Excel4** or **Excel12**.</span></span> <span data-ttu-id="a45b8-134">Nesses casos, você precisa converter uma lista de argumentos variável, como normalmente seria fornecido para **Excel4** ou **Excel12**, para um argumento de matriz única de tamanho variável para chamar de volta no Excel usando **Excel4v** ou **Excel12v**.</span><span class="sxs-lookup"><span data-stu-id="a45b8-134">In these cases, you need to convert a variable argument list, as would normally be supplied to **Excel4** or **Excel12**, to a single array argument of variable size to call back into Excel by using **Excel4v** or **Excel12v**.</span></span>
  
### <a name="example"></a><span data-ttu-id="a45b8-135">Exemplo</span><span class="sxs-lookup"><span data-stu-id="a45b8-135">Example</span></span>

<span data-ttu-id="a45b8-136">Para exemplos de código, consulte o código para as funções **Excel** e **Excel12f** no Excel 2010 XLL SDK, no seguinte local onde você instalou o SDK:</span><span class="sxs-lookup"><span data-stu-id="a45b8-136">For code examples, see the code for the **Excel** and **Excel12f** functions in the Excel 2010 XLL SDK, at the following location where you installed the SDK:</span></span> 
  
<span data-ttu-id="a45b8-137">Samples\Framewrk\Framewrk.c</span><span class="sxs-lookup"><span data-stu-id="a45b8-137">Samples\Framewrk\Framewrk.c</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a45b8-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="a45b8-138">See also</span></span>



[<span data-ttu-id="a45b8-139">Excel4/Excel12</span><span class="sxs-lookup"><span data-stu-id="a45b8-139">Excel4/Excel12</span></span>](excel4-excel12.md)

