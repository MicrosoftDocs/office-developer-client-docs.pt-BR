---
title: xlfUnregister (Formulário 1)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfUnregister
keywords:
- Função xlfunregister [excel 2007]
localization_priority: Normal
ms.assetid: 850bf65f-a151-44d6-b49f-d53ae2c83760
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 3f5ebc08f89651331186990d8574e3150d4f484a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410081"
---
# <a name="xlfunregister-form-1"></a><span data-ttu-id="2449b-104">xlfUnregister (Formulário 1)</span><span class="sxs-lookup"><span data-stu-id="2449b-104">xlfUnregister (Form 1)</span></span>

<span data-ttu-id="2449b-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="2449b-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="2449b-106">Pode ser chamado de um comando DLL ou XLL que, por sua vez, foi chamado pelo Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="2449b-106">Can be called from a DLL or XLL command that has itself been called by Microsoft Excel.</span></span> <span data-ttu-id="2449b-107">Isso equivale a chamar **UNREGISTER de** uma folha de macro XLM do Excel.</span><span class="sxs-lookup"><span data-stu-id="2449b-107">This is equivalent to calling **UNREGISTER** from an Excel XLM macro sheet.</span></span> 
  
<span data-ttu-id="2449b-108">**xlfUnregister** pode ser chamado de duas formas:</span><span class="sxs-lookup"><span data-stu-id="2449b-108">**xlfUnregister** can be called in two forms:</span></span> 
  
- <span data-ttu-id="2449b-109">Formulário 1: Desastra o registro de um comando ou função individual.</span><span class="sxs-lookup"><span data-stu-id="2449b-109">Form 1: Unregisters an individual command or function.</span></span>
    
- <span data-ttu-id="2449b-110">Formulário 2: Descarrega e desativa um XLL.</span><span class="sxs-lookup"><span data-stu-id="2449b-110">Form 2: Unloads and deactivates an XLL.</span></span>
    
<span data-ttu-id="2449b-111">Chamada no Formulário 1, esta função reduz a contagem de uso de uma função ou comando DLL que foi registrado anteriormente usando **xlfRegister** ou **REGISTER**.</span><span class="sxs-lookup"><span data-stu-id="2449b-111">Called in Form 1, this function reduces the use count of a DLL function or command that was previously registered using **xlfRegister** or **REGISTER**.</span></span> <span data-ttu-id="2449b-112">Se a contagem de uso já for zero, essa função não terá efeito.</span><span class="sxs-lookup"><span data-stu-id="2449b-112">If the usage count is already zero, this function has no effect.</span></span> <span data-ttu-id="2449b-113">Quando a contagem de uso de todas as funções em uma DLL atinge zero, a DLL é descarregada da memória.</span><span class="sxs-lookup"><span data-stu-id="2449b-113">When the use count of all the functions in a DLL reaches zero, the DLL is unloaded from memory.</span></span>
  
<span data-ttu-id="2449b-114">**xlfRegister** (Formulário 1) também define um nome oculto que é o argumento de texto da função,  _pxFunctionText_ e que avalia a ID de registro da função ou comando.</span><span class="sxs-lookup"><span data-stu-id="2449b-114">**xlfRegister** (Form 1) also defines a hidden name which is the function text argument,  _pxFunctionText_, and which evaluates to the function or command's registration ID.</span></span> <span data-ttu-id="2449b-115">Quando a função for registrada, esse nome deverá ser excluído usando **xlfSetName** para que o nome da função não seja mais listado pelo Assistente de Função.</span><span class="sxs-lookup"><span data-stu-id="2449b-115">When unregistering the function, this name should be deleted using **xlfSetName** so that the function name is no longer listed by the Function Wizard.</span></span> <span data-ttu-id="2449b-116">Confira mais informações em [Problemas conhecidos no desenvolvimento de XLL do Excel](known-issues-in-excel-xll-development.md).</span><span class="sxs-lookup"><span data-stu-id="2449b-116">For more information, see [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
  
```cs
Excel4(xlfUnregister, LPXLOPER pxRes, 1, LPXLOPER pxRegisterId);
```

## <a name="parameters"></a><span data-ttu-id="2449b-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2449b-117">Parameters</span></span>

<span data-ttu-id="2449b-118">_pxRegisterId_ (**xltypeNum**)</span><span class="sxs-lookup"><span data-stu-id="2449b-118">_pxRegisterId_ (**xltypeNum**)</span></span>
  
<span data-ttu-id="2449b-119">A ID de registro da função a ser não registrou.</span><span class="sxs-lookup"><span data-stu-id="2449b-119">The registration ID of the function to be unregistered.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="2449b-120">Valor de propriedade/Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="2449b-120">Property value/Return value</span></span>

<span data-ttu-id="2449b-121">Se tiver êxito, **retornará TRUE** (**xltypeBool**), caso contrário, retornará FALSE.</span><span class="sxs-lookup"><span data-stu-id="2449b-121">If successful, returns **TRUE** (**xltypeBool**), otherwise it returns FALSE.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2449b-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="2449b-122">Remarks</span></span>

<span data-ttu-id="2449b-123">A ID de registro da função é retornada por **xlfRegister** quando a função é registrada pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="2449b-123">The registration ID of the function is returned by **xlfRegister** when the function is first registered.</span></span> <span data-ttu-id="2449b-124">Ele também pode ser obtido chamando a função [xlfRegisterId](xlfregisterid.md) ou [a função xlfEvaluate](xlfevaluate.md).</span><span class="sxs-lookup"><span data-stu-id="2449b-124">It can also be obtained by calling the [xlfRegisterId function](xlfregisterid.md) or the [xlfEvaluate function](xlfevaluate.md).</span></span> <span data-ttu-id="2449b-125">Observe que xlfRegisterId tentará registrar a função se ainda não tiver sido registrada.</span><span class="sxs-lookup"><span data-stu-id="2449b-125">Note that xlfRegisterId tries to register the function if it has not already been registered.</span></span> <span data-ttu-id="2449b-126">Por esse motivo, se você estiver apenas tentando obter a ID para que possa registrar a função, é melhor obtendo-la passando o nome registrado para **xlfEvaluate**.</span><span class="sxs-lookup"><span data-stu-id="2449b-126">For this reason, if you are only trying to get the ID so that you can unregister the function, it is better to obtain it by passing the registered name to **xlfEvaluate**.</span></span> <span data-ttu-id="2449b-127">Se a função não tiver sido registrada, **xlfEvaluate** falhará com um #NAME? erro.</span><span class="sxs-lookup"><span data-stu-id="2449b-127">If the function has not been registered, **xlfEvaluate** fails with a #NAME? error.</span></span> 
  
## <a name="example"></a><span data-ttu-id="2449b-128">Exemplo</span><span class="sxs-lookup"><span data-stu-id="2449b-128">Example</span></span>

<span data-ttu-id="2449b-129">Consulte o código para **a função fExit** em  `\SAMPLES\GENERIC\GENERIC.C` .</span><span class="sxs-lookup"><span data-stu-id="2449b-129">See the code for the **fExit** function in  `\SAMPLES\GENERIC\GENERIC.C`.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="2449b-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="2449b-130">See also</span></span>

- [<span data-ttu-id="2449b-131">xlfRegister (Formulário 1)</span><span class="sxs-lookup"><span data-stu-id="2449b-131">xlfRegister (Form 1)</span></span>](xlfregister-form-1.md)
- [<span data-ttu-id="2449b-132">xlfRegisterId</span><span class="sxs-lookup"><span data-stu-id="2449b-132">xlfRegisterId</span></span>](xlfregisterid.md)
- [<span data-ttu-id="2449b-133">xlfUnregister (Formulário 2)</span><span class="sxs-lookup"><span data-stu-id="2449b-133">xlfUnregister (Form 2)</span></span>](xlfunregister-form-2.md)
- [<span data-ttu-id="2449b-134">Funções XLM essenciais e úteis para a API C</span><span class="sxs-lookup"><span data-stu-id="2449b-134">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

