---
title: xlfUnregister (Formulário 2)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfUnregister (Form 2)
keywords:
- xlfunregister [excel 2007]
localization_priority: Normal
ms.assetid: 39c6eba7-ba41-4e7b-9a28-2b662378ff5a
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 8bf1151e1ba4c165e784b88dce80096a2eaa62de
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419902"
---
# <a name="xlfunregister-form-2"></a><span data-ttu-id="64165-104">xlfUnregister (Formulário 2)</span><span class="sxs-lookup"><span data-stu-id="64165-104">xlfUnregister (Form 2)</span></span>

<span data-ttu-id="64165-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="64165-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="64165-106">Pode ser chamado de um comando DLL ou XLL que, por sua vez, foi chamado pelo Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="64165-106">Can be called from a DLL or XLL command that has itself been called by Microsoft Excel.</span></span> <span data-ttu-id="64165-107">Isso equivale a chamar **UNREGISTER de** uma folha de macro XLM do Excel.</span><span class="sxs-lookup"><span data-stu-id="64165-107">This is equivalent to calling **UNREGISTER** from an Excel XLM macro sheet.</span></span> 
  
<span data-ttu-id="64165-108">**xlfUnregister** pode ser chamado de duas formas:</span><span class="sxs-lookup"><span data-stu-id="64165-108">**xlfUnregister** can be called in two forms:</span></span> 
  
- <span data-ttu-id="64165-109">Formulário 1: Desastra o registro de um comando ou função individual.</span><span class="sxs-lookup"><span data-stu-id="64165-109">Form 1: Unregisters an individual command or function.</span></span>
    
- <span data-ttu-id="64165-110">Formulário 2: Descarrega e desativa um XLL.</span><span class="sxs-lookup"><span data-stu-id="64165-110">Form 2: Unloads and deactivates an XLL.</span></span>
    
<span data-ttu-id="64165-111">Chamada no Formulário 2, essa função força um DLL ou recurso de código a ser descarregado completamente.</span><span class="sxs-lookup"><span data-stu-id="64165-111">Called in Form 2, this function forces a DLL or code resource to be unloaded completely.</span></span> <span data-ttu-id="64165-112">Ele desastra o registro de todas as funções em uma DLL, mesmo se elas estão sendo usadas por outra macro, independentemente da contagem de uso.</span><span class="sxs-lookup"><span data-stu-id="64165-112">It unregisters all of the functions in a DLL, even if they are currently in use by another macro, no matter what the use count.</span></span> <span data-ttu-id="64165-113">Essa função chama **xlAutoClose** e, em seguida, desautorna todas as funções na DLL.</span><span class="sxs-lookup"><span data-stu-id="64165-113">This function calls **xlAutoClose**, and then unregisters all the functions in the DLL.</span></span>
  
```cs
Excel12(xlfUnregister, LPXLOPER12 pxRes, 1, LPXLOPER12 pxModuleText);
```

## <a name="parameters"></a><span data-ttu-id="64165-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="64165-114">Parameters</span></span>

<span data-ttu-id="64165-115">_pxModuleText_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="64165-115">_pxModuleText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="64165-116">O nome da DLL.</span><span class="sxs-lookup"><span data-stu-id="64165-116">The name of the DLL.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="64165-117">Valor de propriedade/Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="64165-117">Property value/Return value</span></span>

<span data-ttu-id="64165-118">Se bem-sucedido, **retorna VERDADEIRO** (**xltypeBool**).</span><span class="sxs-lookup"><span data-stu-id="64165-118">If successful, returns **TRUE** (**xltypeBool**).</span></span> <span data-ttu-id="64165-119">Se não tiver êxito, **retornará FALSE**.</span><span class="sxs-lookup"><span data-stu-id="64165-119">If unsuccessful, returns **FALSE**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="64165-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="64165-120">Remarks</span></span>

> [!NOTE] 
> <span data-ttu-id="64165-121">Não chame essa forma da função de sua implementação do [xlAutoClose](xlautoclose.md) em uma tentativa de ressumentar todos os recursos da DLL com uma chamada de função simples.</span><span class="sxs-lookup"><span data-stu-id="64165-121">Do not call this form of the function from your implementation of the [xlAutoClose](xlautoclose.md) in an attempt to unregister all of the DLL's resources with one simple function call.</span></span> <span data-ttu-id="64165-122">Isso leva à chamada recursiva **de xlAutoClose** e a um estouro de pilha.</span><span class="sxs-lookup"><span data-stu-id="64165-122">This leads to recursive calling of **xlAutoClose** and a stack overflow.</span></span> 
  
### <a name="remember-to-delete-names"></a><span data-ttu-id="64165-123">Lembre-se de excluir nomes</span><span class="sxs-lookup"><span data-stu-id="64165-123">Remember to delete names</span></span>

<span data-ttu-id="64165-124">Se você especificou o argumento  _pxFunctionText_ para **xlfRegister**, ao registrar as funções e comandos da DLL, exclua explicitamente os nomes chamando **xlfSetName** para cada um deles, omitindo o segundo argumento para que a função não apareça mais no Assistente de Função.</span><span class="sxs-lookup"><span data-stu-id="64165-124">If you specified the  _pxFunctionText_ argument to **xlfRegister**, when registering the DLL's functions and commands, you must explicitly delete the names by calling **xlfSetName** for each one, omitting the second argument so that the function no longer appears in the Function Wizard.</span></span> <span data-ttu-id="64165-125">Confira mais informações em [Problemas conhecidos no desenvolvimento de XLL do Excel](known-issues-in-excel-xll-development.md).</span><span class="sxs-lookup"><span data-stu-id="64165-125">For more information, see [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="64165-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="64165-126">See also</span></span>

- [<span data-ttu-id="64165-127">xlfRegister (Formulário 1)</span><span class="sxs-lookup"><span data-stu-id="64165-127">xlfRegister (Form 1)</span></span>](xlfregister-form-1.md)
- [<span data-ttu-id="64165-128">xlfRegisterId</span><span class="sxs-lookup"><span data-stu-id="64165-128">xlfRegisterId</span></span>](xlfregisterid.md)
- [<span data-ttu-id="64165-129">xlfUnregister (Formulário 1)</span><span class="sxs-lookup"><span data-stu-id="64165-129">xlfUnregister (Form 1)</span></span>](xlfunregister-form-1.md)
- [<span data-ttu-id="64165-130">Funções XLM essenciais e úteis para a API C</span><span class="sxs-lookup"><span data-stu-id="64165-130">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

