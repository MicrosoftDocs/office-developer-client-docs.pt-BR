---
title: xlfUnregister (Formulário 1)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfUnregister
keywords:
- função xlfunregister [Excel 2007]
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
# <a name="xlfunregister-form-1"></a><span data-ttu-id="687da-104">xlfUnregister (Formulário 1)</span><span class="sxs-lookup"><span data-stu-id="687da-104">xlfUnregister (Form 1)</span></span>

<span data-ttu-id="687da-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="687da-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="687da-106">Pode ser chamado de um comando DLL ou XLL que, por sua vez, foi chamado pelo Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="687da-106">Can be called from a DLL or XLL command that has itself been called by Microsoft Excel.</span></span> <span data-ttu-id="687da-107">Isso equivale a chamar **Unregister** de uma folha de macro XLM do Excel.</span><span class="sxs-lookup"><span data-stu-id="687da-107">This is equivalent to calling **UNREGISTER** from an Excel XLM macro sheet.</span></span> 
  
<span data-ttu-id="687da-108">**xlfUnregister** pode ser chamado de duas formas:</span><span class="sxs-lookup"><span data-stu-id="687da-108">**xlfUnregister** can be called in two forms:</span></span> 
  
- <span data-ttu-id="687da-109">Formulário 1: cancela o registro de um comando ou função individual.</span><span class="sxs-lookup"><span data-stu-id="687da-109">Form 1: Unregisters an individual command or function.</span></span>
    
- <span data-ttu-id="687da-110">Formulário 2: descarrega e desativa um XLL.</span><span class="sxs-lookup"><span data-stu-id="687da-110">Form 2: Unloads and deactivates an XLL.</span></span>
    
<span data-ttu-id="687da-111">Chamado no formato 1, essa função reduz a contagem de uso de uma função DLL ou de um comando que foi previamente registrado usando **xlfRegister** ou **Register**.</span><span class="sxs-lookup"><span data-stu-id="687da-111">Called in Form 1, this function reduces the use count of a DLL function or command that was previously registered using **xlfRegister** or **REGISTER**.</span></span> <span data-ttu-id="687da-112">Se a contagem de uso já for zero, essa função não terá efeito.</span><span class="sxs-lookup"><span data-stu-id="687da-112">If the usage count is already zero, this function has no effect.</span></span> <span data-ttu-id="687da-113">Quando a contagem de uso de todas as funções em uma DLL chega a zero, a DLL é descarregada da memória.</span><span class="sxs-lookup"><span data-stu-id="687da-113">When the use count of all the functions in a DLL reaches zero, the DLL is unloaded from memory.</span></span>
  
<span data-ttu-id="687da-114">**xlfRegister** (Form 1) também define um nome oculto que é o argumento de texto da função, _pxFunctionText_, e que é avaliado como a ID de registro de função ou comando.</span><span class="sxs-lookup"><span data-stu-id="687da-114">**xlfRegister** (Form 1) also defines a hidden name which is the function text argument,  _pxFunctionText_, and which evaluates to the function or command's registration ID.</span></span> <span data-ttu-id="687da-115">Ao cancelar o registro da função, esse nome deve ser excluído usando o **xlfSetName** para que o nome da função não seja mais listado pelo assistente de função.</span><span class="sxs-lookup"><span data-stu-id="687da-115">When unregistering the function, this name should be deleted using **xlfSetName** so that the function name is no longer listed by the Function Wizard.</span></span> <span data-ttu-id="687da-116">Confira mais informações em [Problemas conhecidos no desenvolvimento de XLL do Excel](known-issues-in-excel-xll-development.md).</span><span class="sxs-lookup"><span data-stu-id="687da-116">For more information, see [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
  
```cs
Excel4(xlfUnregister, LPXLOPER pxRes, 1, LPXLOPER pxRegisterId);
```

## <a name="parameters"></a><span data-ttu-id="687da-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="687da-117">Parameters</span></span>

<span data-ttu-id="687da-118">_pxRegisterId_ (**xltypeNum**)</span><span class="sxs-lookup"><span data-stu-id="687da-118">_pxRegisterId_ (**xltypeNum**)</span></span>
  
<span data-ttu-id="687da-119">A ID de registro da função a ser cancelada.</span><span class="sxs-lookup"><span data-stu-id="687da-119">The registration ID of the function to be unregistered.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="687da-120">Valor de propriedade/Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="687da-120">Property value/Return value</span></span>

<span data-ttu-id="687da-121">Se bem-sucedido, retorna **true** (**xltypeBool**), caso contrário, retorna false.</span><span class="sxs-lookup"><span data-stu-id="687da-121">If successful, returns **TRUE** (**xltypeBool**), otherwise it returns FALSE.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="687da-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="687da-122">Remarks</span></span>

<span data-ttu-id="687da-123">A ID de registro da função é retornada por **xlfRegister** quando a função é registrada pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="687da-123">The registration ID of the function is returned by **xlfRegister** when the function is first registered.</span></span> <span data-ttu-id="687da-124">Ela também pode ser obtida chamando-se a [função xlfRegisterId](xlfregisterid.md) ou a [função xlfEvaluate](xlfevaluate.md).</span><span class="sxs-lookup"><span data-stu-id="687da-124">It can also be obtained by calling the [xlfRegisterId function](xlfregisterid.md) or the [xlfEvaluate function](xlfevaluate.md).</span></span> <span data-ttu-id="687da-125">Observe que xlfRegisterId tenta registrar a função se ela ainda não tiver sido registrada.</span><span class="sxs-lookup"><span data-stu-id="687da-125">Note that xlfRegisterId tries to register the function if it has not already been registered.</span></span> <span data-ttu-id="687da-126">Por esse motivo, se você estiver apenas tentando obter a ID para que possa cancelar o registro da função, é melhor obtê-la passando o nome registrado para **xlfEvaluate**.</span><span class="sxs-lookup"><span data-stu-id="687da-126">For this reason, if you are only trying to get the ID so that you can unregister the function, it is better to obtain it by passing the registered name to **xlfEvaluate**.</span></span> <span data-ttu-id="687da-127">Se a função não tiver sido registrada, o **xlfEvaluate** falhará com um #NAME? erros.</span><span class="sxs-lookup"><span data-stu-id="687da-127">If the function has not been registered, **xlfEvaluate** fails with a #NAME? error.</span></span> 
  
## <a name="example"></a><span data-ttu-id="687da-128">Exemplo</span><span class="sxs-lookup"><span data-stu-id="687da-128">Example</span></span>

<span data-ttu-id="687da-129">Consulte o código para a função **fExit** no `\SAMPLES\GENERIC\GENERIC.C`.</span><span class="sxs-lookup"><span data-stu-id="687da-129">See the code for the **fExit** function in  `\SAMPLES\GENERIC\GENERIC.C`.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="687da-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="687da-130">See also</span></span>

- [<span data-ttu-id="687da-131">xlfRegister (Formulário 1)</span><span class="sxs-lookup"><span data-stu-id="687da-131">xlfRegister (Form 1)</span></span>](xlfregister-form-1.md)
- [<span data-ttu-id="687da-132">xlfRegisterId</span><span class="sxs-lookup"><span data-stu-id="687da-132">xlfRegisterId</span></span>](xlfregisterid.md)
- [<span data-ttu-id="687da-133">xlfUnregister (Formulário 2)</span><span class="sxs-lookup"><span data-stu-id="687da-133">xlfUnregister (Form 2)</span></span>](xlfunregister-form-2.md)
- [<span data-ttu-id="687da-134">Funções XLM essenciais e úteis para a API C</span><span class="sxs-lookup"><span data-stu-id="687da-134">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

