---
title: xlfRegisterId
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfRegisterId
keywords:
- Função xlfregisterid [excel 2007]
localization_priority: Normal
ms.assetid: d34cf20c-a5cd-45fb-9dcb-d49eac2d99dd
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 05119226d0b6190a2c4b30846c03a59b5c3cd1d8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420056"
---
# <a name="xlfregisterid"></a><span data-ttu-id="cf760-104">xlfRegisterId</span><span class="sxs-lookup"><span data-stu-id="cf760-104">xlfRegisterId</span></span>

<span data-ttu-id="cf760-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="cf760-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="cf760-106">Pode ser chamado a partir de uma DLL que foi chamada pelo Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="cf760-106">Can be called from a DLL that has itself been called by Microsoft Excel.</span></span> <span data-ttu-id="cf760-107">Se uma função já estiver registrada, ela retornará a ID do registro existente para essa função sem reregistiá-la.</span><span class="sxs-lookup"><span data-stu-id="cf760-107">If a function is already registered, it returns the existing register ID for that function without reregistering it.</span></span> <span data-ttu-id="cf760-108">Se uma função ainda não estiver registrada, ela a registrará e retornará a ID do registro resultante.</span><span class="sxs-lookup"><span data-stu-id="cf760-108">If a function is not yet registered, it registers it and returns the resulting register ID.</span></span>
  
```cs
Excel12(xlfRegisterId, LPXLOPER12 pxRes, 3,     LPXLOPER12 pxModuleText, LPXLOPER12 pxProcedure, LPXLOPER12 pxTypeText);
```

## <a name="parameters"></a><span data-ttu-id="cf760-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cf760-109">Parameters</span></span>

<span data-ttu-id="cf760-110">_pxModuleText_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="cf760-110">_pxModuleText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="cf760-111">O nome da DLL que contém a função.</span><span class="sxs-lookup"><span data-stu-id="cf760-111">The name of the DLL containing the function.</span></span>
  
<span data-ttu-id="cf760-112">_pxProcedure_ (**xltypeStr** ou **xltypeNum**)</span><span class="sxs-lookup"><span data-stu-id="cf760-112">_pxProcedure_ (**xltypeStr** or **xltypeNum**)</span></span>
  
<span data-ttu-id="cf760-113">Se for uma cadeia de caracteres, o nome da função a ser chamada.</span><span class="sxs-lookup"><span data-stu-id="cf760-113">If a string, the name of the function to call.</span></span> <span data-ttu-id="cf760-114">Se número, o número de exportação ordinal da função a chamar.</span><span class="sxs-lookup"><span data-stu-id="cf760-114">If a number, the ordinal export number of the function to call.</span></span> <span data-ttu-id="cf760-115">Para maior clareza e robustez, sempre use o formulário de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="cf760-115">For clarity and robustness, always use the string form.</span></span>
  
<span data-ttu-id="cf760-116">_pxTypeText_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="cf760-116">_pxTypeText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="cf760-117">Uma cadeia de caracteres opcional especificando os tipos de todos os argumentos para a função e o tipo do valor de retorno da função.</span><span class="sxs-lookup"><span data-stu-id="cf760-117">An optional string specifying the types of all the arguments to the function and the type of the return value of the function.</span></span> <span data-ttu-id="cf760-118">Para obter mais informações, consulte a seção "Comentários".</span><span class="sxs-lookup"><span data-stu-id="cf760-118">For more information, see the "Remarks" section.</span></span> <span data-ttu-id="cf760-119">Esse argumento pode ser omitido para uma DLL (XLL) autônomo definindo **xlAutoRegister**.</span><span class="sxs-lookup"><span data-stu-id="cf760-119">This argument can be omitted for a stand-alone DLL (XLL) defining **xlAutoRegister**.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="cf760-120">Valor de propriedade/Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="cf760-120">Property value/Return value</span></span>

<span data-ttu-id="cf760-121">Retorna a ID do registro da função (**xltypeNum**), que pode ser usada em chamadas subsequentes **para xlfUnregister**.</span><span class="sxs-lookup"><span data-stu-id="cf760-121">Returns the register ID of the function (**xltypeNum**), which can be used in subsequent calls to **xlfUnregister**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="cf760-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="cf760-122">Remarks</span></span>

<span data-ttu-id="cf760-123">Essa função é útil quando você não quer se preocupar com a manutenção de uma ID de registro, mas precisa de uma mais tarde para o registro.</span><span class="sxs-lookup"><span data-stu-id="cf760-123">This function is useful when you do not want to worry about maintaining a register ID, but you need one later for unregistering.</span></span> <span data-ttu-id="cf760-124">Também é útil para atribuir a menus, ferramentas e botões quando a função que você deseja atribuir está em uma DLL.</span><span class="sxs-lookup"><span data-stu-id="cf760-124">It is also useful for assigning to menus, tools, and buttons when the function you want to assign is in a DLL.</span></span>
  
<span data-ttu-id="cf760-125">Onde uma função DLL ou XLL foi registrada com um argumento  _pxFunctionText_ válido tendo sido fornecido para **xlfRegister**, sua ID de registro também pode ser obtida passando  _o pxFunctionText_ para a função **xlfEvaluate**.</span><span class="sxs-lookup"><span data-stu-id="cf760-125">Where a DLL or XLL function has been registered with a valid  _pxFunctionText_ argument having been supplied to **xlfRegister**, its register ID can also be obtained by passing the  _pxFunctionText_ to the function **xlfEvaluate**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="cf760-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="cf760-126">See also</span></span>

- [<span data-ttu-id="cf760-127">REGISTER</span><span class="sxs-lookup"><span data-stu-id="cf760-127">REGISTER</span></span>](xlfregister-form-1.md)
- [<span data-ttu-id="cf760-128">UNREGISTER</span><span class="sxs-lookup"><span data-stu-id="cf760-128">UNREGISTER</span></span>](xlfunregister-form-1.md)
- [<span data-ttu-id="cf760-129">Funções XLM essenciais e úteis para a API C</span><span class="sxs-lookup"><span data-stu-id="cf760-129">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

