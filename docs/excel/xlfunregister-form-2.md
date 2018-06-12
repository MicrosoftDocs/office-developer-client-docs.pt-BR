---
title: xlfUnregister (formulário 2)
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
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: e0154e380b65b8c57e7e96a98ef131e26b49e203
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765488"
---
# <a name="xlfunregister-form-2"></a><span data-ttu-id="c07a9-104">xlfUnregister (formulário 2)</span><span class="sxs-lookup"><span data-stu-id="c07a9-104">xlfUnregister (Form 2)</span></span>

<span data-ttu-id="c07a9-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="c07a9-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="c07a9-106">Pode ser chamado a partir de um comando DLL ou XLL próprio foi chamado pelo Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="c07a9-106">Can be called from a DLL or XLL command that has itself been called by Microsoft Excel.</span></span> <span data-ttu-id="c07a9-107">Isso é equivalente a chamar **cancela o registro** de uma folha de macro do Excel XLM.</span><span class="sxs-lookup"><span data-stu-id="c07a9-107">This is equivalent to calling **UNREGISTER** from an Excel XLM macro sheet.</span></span> 
  
<span data-ttu-id="c07a9-108">**xlfUnregister** pode ser chamado de duas formas:</span><span class="sxs-lookup"><span data-stu-id="c07a9-108">**xlfUnregister** can be called in two forms:</span></span> 
  
- <span data-ttu-id="c07a9-109">Formulário 1: Cancela o registro de um comando individual ou uma função.</span><span class="sxs-lookup"><span data-stu-id="c07a9-109">Form 1: Unregisters an individual command or function.</span></span>
    
- <span data-ttu-id="c07a9-110">Formulário 2: Descarrega e desativa um XLL.</span><span class="sxs-lookup"><span data-stu-id="c07a9-110">Form 2: Unloads and deactivates an XLL.</span></span>
    
<span data-ttu-id="c07a9-111">Chamado no formulário 2, essa função força um DLL ou código do recurso a ser descarregado completamente.</span><span class="sxs-lookup"><span data-stu-id="c07a9-111">Called in Form 2, this function forces a DLL or code resource to be unloaded completely.</span></span> <span data-ttu-id="c07a9-112">Ele cancela o registro de todas as funções em uma DLL, mesmo se eles estão atualmente em uso por outra macro, não importa qual a contagem de uso.</span><span class="sxs-lookup"><span data-stu-id="c07a9-112">It unregisters all of the functions in a DLL, even if they are currently in use by another macro, no matter what the use count.</span></span> <span data-ttu-id="c07a9-113">Essa função chama **xlAutoClose**e, em seguida, cancela o registro de todas as funções na DLL.</span><span class="sxs-lookup"><span data-stu-id="c07a9-113">This function calls **xlAutoClose**, and then unregisters all the functions in the DLL.</span></span>
  
```cs
Excel12(xlfUnregister, LPXLOPER12 pxRes, 1, LPXLOPER12 pxModuleText);
```

## <a name="parameters"></a><span data-ttu-id="c07a9-114">Par�metros</span><span class="sxs-lookup"><span data-stu-id="c07a9-114">Parameters</span></span>

<span data-ttu-id="c07a9-115">_pxModuleText_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="c07a9-115">_pxModuleText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="c07a9-116">O nome da DLL.</span><span class="sxs-lookup"><span data-stu-id="c07a9-116">The name of the DLL.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="c07a9-117">Propriedade valor/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="c07a9-117">Property value/Return value</span></span>

<span data-ttu-id="c07a9-118">Se tiver êxito, retornará **TRUE** (**xltypeBool**).</span><span class="sxs-lookup"><span data-stu-id="c07a9-118">If successful, returns **TRUE** (**xltypeBool**).</span></span> <span data-ttu-id="c07a9-119">Se for bem sucedida, retornará **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="c07a9-119">If unsuccessful, returns **FALSE**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c07a9-120">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="c07a9-120">Remarks</span></span>

> [!NOTE] 
> <span data-ttu-id="c07a9-121">Não chame essa forma da função da sua implementação do [xlAutoClose](xlautoclose.md) em uma tentativa de cancelar o registro de todos os recursos da DLL com chamada de uma função simples.</span><span class="sxs-lookup"><span data-stu-id="c07a9-121">Do not call this form of the function from your implementation of the [xlAutoClose](xlautoclose.md) in an attempt to unregister all of the DLL's resources with one simple function call.</span></span> <span data-ttu-id="c07a9-122">Isso leva a chamada recursiva de **xlAutoClose** e um estouro de pilha.</span><span class="sxs-lookup"><span data-stu-id="c07a9-122">This leads to recursive calling of **xlAutoClose** and a stack overflow.</span></span> 
  
### <a name="remember-to-delete-names"></a><span data-ttu-id="c07a9-123">Lembre-se de excluir nomes</span><span class="sxs-lookup"><span data-stu-id="c07a9-123">Remember to delete names</span></span>

<span data-ttu-id="c07a9-124">Se você especificou o argumento _pxFunctionText_ de **xlfRegister**, ao registrar a DLL as funções e comandos, você deve explicitamente excluir os nomes chamando **xlfSetName** para cada um, omitindo o segundo argumento para que o função não aparece mais no Assistente de função.</span><span class="sxs-lookup"><span data-stu-id="c07a9-124">If you specified the  _pxFunctionText_ argument to **xlfRegister**, when registering the DLL's functions and commands, you must explicitly delete the names by calling **xlfSetName** for each one, omitting the second argument so that the function no longer appears in the Function Wizard.</span></span> <span data-ttu-id="c07a9-125">Para obter mais informações, consulte [Problemas conhecidos no desenvolvimento de XLL do Excel](known-issues-in-excel-xll-development.md).</span><span class="sxs-lookup"><span data-stu-id="c07a9-125">For more information, see [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c07a9-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="c07a9-126">See also</span></span>

- [<span data-ttu-id="c07a9-127">xlfRegister (Form 1)</span><span class="sxs-lookup"><span data-stu-id="c07a9-127">xlfRegister (Form 1)</span></span>](xlfregister-form-1.md)
- [<span data-ttu-id="c07a9-128">xlfRegisterId</span><span class="sxs-lookup"><span data-stu-id="c07a9-128">xlfRegisterId</span></span>](xlfregisterid.md)
- [<span data-ttu-id="c07a9-129">xlfUnregister (formulário 1)</span><span class="sxs-lookup"><span data-stu-id="c07a9-129">xlfUnregister (Form 1)</span></span>](xlfunregister-form-1.md)
- [<span data-ttu-id="c07a9-130">Funções de XLM API C essenciais e úteis</span><span class="sxs-lookup"><span data-stu-id="c07a9-130">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

