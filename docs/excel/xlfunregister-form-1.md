---
title: xlfUnregister (Formulário 1)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfUnregister
keywords:
- função xlfunregister [excel 2007]
localization_priority: Normal
ms.assetid: 850bf65f-a151-44d6-b49f-d53ae2c83760
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 6077027a27c054c5a5e65a751373c41a87cb3836
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765473"
---
# <a name="xlfunregister-form-1"></a><span data-ttu-id="444a0-104">xlfUnregister (Formulário 1)</span><span class="sxs-lookup"><span data-stu-id="444a0-104">xlfUnregister (Form 1)</span></span>

<span data-ttu-id="444a0-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="444a0-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="444a0-106">Pode ser chamado a partir de um comando DLL ou XLL próprio foi chamado pelo Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="444a0-106">Can be called from a DLL or XLL command that has itself been called by Microsoft Excel.</span></span> <span data-ttu-id="444a0-107">Isso é equivalente a chamar **cancela o registro** de uma folha de macro do Excel XLM.</span><span class="sxs-lookup"><span data-stu-id="444a0-107">This is equivalent to calling **UNREGISTER** from an Excel XLM macro sheet.</span></span> 
  
<span data-ttu-id="444a0-108">**xlfUnregister** pode ser chamado de duas formas:</span><span class="sxs-lookup"><span data-stu-id="444a0-108">**xlfUnregister** can be called in two forms:</span></span> 
  
- <span data-ttu-id="444a0-109">Formulário 1: Cancela o registro de um comando individual ou uma função.</span><span class="sxs-lookup"><span data-stu-id="444a0-109">Form 1: Unregisters an individual command or function.</span></span>
    
- <span data-ttu-id="444a0-110">Formulário 2: Descarrega e desativa um XLL.</span><span class="sxs-lookup"><span data-stu-id="444a0-110">Form 2: Unloads and deactivates an XLL.</span></span>
    
<span data-ttu-id="444a0-111">Chamado no formulário 1, essa função reduz a contagem de uso de uma função DLL ou o comando que foi registrado anteriormente usando **xlfRegister** ou **registrar**.</span><span class="sxs-lookup"><span data-stu-id="444a0-111">Called in Form 1, this function reduces the use count of a DLL function or command that was previously registered using **xlfRegister** or **REGISTER**.</span></span> <span data-ttu-id="444a0-112">Se a contagem de uso já for zero, essa função não tem efeito.</span><span class="sxs-lookup"><span data-stu-id="444a0-112">If the usage count is already zero, this function has no effect.</span></span> <span data-ttu-id="444a0-113">Quando a contagem de uso de todas as funções em uma DLL chega a zero, a DLL seja descarregada da memória.</span><span class="sxs-lookup"><span data-stu-id="444a0-113">When the use count of all the functions in a DLL reaches zero, the DLL is unloaded from memory.</span></span>
  
<span data-ttu-id="444a0-114">**xlfRegister** (Forma 1) também define um nome oculto, que é o argumento de texto de função, _pxFunctionText_, e que avalia para a função ou a ID de registro. do comando</span><span class="sxs-lookup"><span data-stu-id="444a0-114">**xlfRegister** (Form 1) also defines a hidden name which is the function text argument,  _pxFunctionText_, and which evaluates to the function or command's registration ID.</span></span> <span data-ttu-id="444a0-115">Quando a função Cancelando o registro, esse nome deve ser excluído usando **xlfSetName** , de modo que o nome da função não está mais listado pelo Assistente de função.</span><span class="sxs-lookup"><span data-stu-id="444a0-115">When unregistering the function, this name should be deleted using **xlfSetName** so that the function name is no longer listed by the Function Wizard.</span></span> <span data-ttu-id="444a0-116">Para obter mais informações, consulte [Problemas conhecidos no desenvolvimento de XLL do Excel](known-issues-in-excel-xll-development.md).</span><span class="sxs-lookup"><span data-stu-id="444a0-116">For more information, see [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
  
```cs
Excel4(xlfUnregister, LPXLOPER pxRes, 1, LPXLOPER pxRegisterId);
```

## <a name="parameters"></a><span data-ttu-id="444a0-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="444a0-117">Parameters</span></span>

<span data-ttu-id="444a0-118">_pxRegisterId_ (**xltypeNum**)</span><span class="sxs-lookup"><span data-stu-id="444a0-118">_pxRegisterId_ (**xltypeNum**)</span></span>
  
<span data-ttu-id="444a0-119">A ID do registro da função a ser cancelado.</span><span class="sxs-lookup"><span data-stu-id="444a0-119">The registration ID of the function to be unregistered.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="444a0-120">Valor de propriedade/Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="444a0-120">Property value/Return value</span></span>

<span data-ttu-id="444a0-121">Se tiver êxito, retornará **TRUE** (**xltypeBool**), caso contrário, ele retornará FALSE.</span><span class="sxs-lookup"><span data-stu-id="444a0-121">If successful, returns **TRUE** (**xltypeBool**), otherwise it returns FALSE.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="444a0-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="444a0-122">Remarks</span></span>

<span data-ttu-id="444a0-123">O registro retornado por **xlfRegister** ID da função quando a função for primeira registrado.</span><span class="sxs-lookup"><span data-stu-id="444a0-123">The registration ID of the function is returned by **xlfRegister** when the function is first registered.</span></span> <span data-ttu-id="444a0-124">Ele também pode ser obtido chamando-se a [função xlfRegisterId](xlfregisterid.md) ou a [função xlfEvaluate](xlfevaluate.md).</span><span class="sxs-lookup"><span data-stu-id="444a0-124">It can also be obtained by calling the [xlfRegisterId function](xlfregisterid.md) or the [xlfEvaluate function](xlfevaluate.md).</span></span> <span data-ttu-id="444a0-125">Observe que xlfRegisterId tenta registrar a função se ele já não foi registrado.</span><span class="sxs-lookup"><span data-stu-id="444a0-125">Note that xlfRegisterId tries to register the function if it has not already been registered.</span></span> <span data-ttu-id="444a0-126">Por esse motivo, se você estiver tentando apenas obter a identificação de modo que você pode cancelar o registro de função, é melhor obtê-lo, passando o nome registrado para **xlfEvaluate**.</span><span class="sxs-lookup"><span data-stu-id="444a0-126">For this reason, if you are only trying to get the ID so that you can unregister the function, it is better to obtain it by passing the registered name to **xlfEvaluate**.</span></span> <span data-ttu-id="444a0-127">Se a função não foi registrada, **xlfEvaluate** falhar com um #NAME? erro.</span><span class="sxs-lookup"><span data-stu-id="444a0-127">If the function has not been registered, **xlfEvaluate** fails with a #NAME? error.</span></span> 
  
## <a name="example"></a><span data-ttu-id="444a0-128">Exemplo</span><span class="sxs-lookup"><span data-stu-id="444a0-128">Example</span></span>

<span data-ttu-id="444a0-129">Ver o código para a função **fExit** em `\SAMPLES\GENERIC\GENERIC.C`.</span><span class="sxs-lookup"><span data-stu-id="444a0-129">See the code for the **fExit** function in  `\SAMPLES\GENERIC\GENERIC.C`.</span></span>
  
```cs
int WINAPI fExit(void)
{
   XLOPER12  xDLL,    // The name of this DLL //
   xFunc,             // The name of the function //
   xRegId;            // The registration ID //
   int i;
//
// This code gets the DLL name. It then uses this along with information
// from g_rgFuncs[] to obtain a REGISTER.ID() for each function. The
// register ID is then used to unregister each function. Then the code
// frees the DLL name and calls xlAutoClose.
//
   // Make xFunc a string //
   xFunc.xltype = xltypeStr;
   Excel12f(xlGetName, &xDLL, 0);
   for (i = 0; i < g_rgWorksheetFuncsRows; i++)
   {
      xFunc.val.str = (LPWSTR) (g_rgWorksheetFuncs[i][0]);
      Excel12f(xlfRegisterId,&xRegId,2,(LPXLOPER12)&xDLL,(LPXLOPER12)&xFunc);
      Excel12f(xlfUnregister, 0, 1, (LPXLOPER12) &xRegId);
   }
   for (i = 0; i < g_rgCommandFuncsRows; i++)
   {
      xFunc.val.str = (LPWSTR) (g_rgCommandFuncs[i][0]);
      Excel12f(xlfRegisterId,&xRegId,2,(LPXLOPER12)&xDLL,(LPXLOPER12)&xFunc);
      Excel12f(xlfUnregister, 0, 1, (LPXLOPER12) &xRegId);
   }
   Excel12f(xlFree, 0, 1,  (LPXLOPER12) &xDLL);
   return xlAutoClose();
}
```

## <a name="see-also"></a><span data-ttu-id="444a0-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="444a0-130">See also</span></span>

- [<span data-ttu-id="444a0-131">xlfRegister (Form 1)</span><span class="sxs-lookup"><span data-stu-id="444a0-131">xlfRegister (Form 1)</span></span>](xlfregister-form-1.md)
- [<span data-ttu-id="444a0-132">xlfRegisterId</span><span class="sxs-lookup"><span data-stu-id="444a0-132">xlfRegisterId</span></span>](xlfregisterid.md)
- [<span data-ttu-id="444a0-133">xlfUnregister (Formulário 2)</span><span class="sxs-lookup"><span data-stu-id="444a0-133">xlfUnregister (Form 2)</span></span>](xlfunregister-form-2.md)
- [<span data-ttu-id="444a0-134">Funções XLM essenciais e úteis para a API de C</span><span class="sxs-lookup"><span data-stu-id="444a0-134">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

