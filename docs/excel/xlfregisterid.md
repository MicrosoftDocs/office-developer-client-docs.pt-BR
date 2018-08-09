---
title: xlfRegisterId
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfRegisterId
keywords:
- função xlfregisterid [excel 2007]
localization_priority: Normal
ms.assetid: d34cf20c-a5cd-45fb-9dcb-d49eac2d99dd
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: cd401393b7465442cef9342b942a27456871c68b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765478"
---
# <a name="xlfregisterid"></a><span data-ttu-id="5ffbb-104">xlfRegisterId</span><span class="sxs-lookup"><span data-stu-id="5ffbb-104">xlfRegisterId</span></span>

<span data-ttu-id="5ffbb-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="5ffbb-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="5ffbb-106">Pode ser chamado a partir de uma DLL que o próprio foi chamada pelo Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="5ffbb-106">Can be called from a DLL that has itself been called by Microsoft Excel.</span></span> <span data-ttu-id="5ffbb-107">Se uma função já estiver registrada, ele retornará a identificação de registro existente para essa função sem registrando novamente a ele.</span><span class="sxs-lookup"><span data-stu-id="5ffbb-107">If a function is already registered, it returns the existing register ID for that function without reregistering it.</span></span> <span data-ttu-id="5ffbb-108">Se uma função ainda não estiver registrada, ele registra a ele e retorna o ID do registro resultante.</span><span class="sxs-lookup"><span data-stu-id="5ffbb-108">If a function is not yet registered, it registers it and returns the resulting register ID.</span></span>
  
```cs
Excel12(xlfRegisterId, LPXLOPER12 pxRes, 3,     LPXLOPER12 pxModuleText, LPXLOPER12 pxProcedure, LPXLOPER12 pxTypeText);
```

## <a name="parameters"></a><span data-ttu-id="5ffbb-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5ffbb-109">Parameters</span></span>

<span data-ttu-id="5ffbb-110">_pxModuleText_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="5ffbb-110">_pxModuleText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="5ffbb-111">O nome da DLL que contém a função.</span><span class="sxs-lookup"><span data-stu-id="5ffbb-111">The name of the DLL containing the function.</span></span>
  
<span data-ttu-id="5ffbb-112">_pxProcedure_ (**xltypeStr** ou **xltypeNum**)</span><span class="sxs-lookup"><span data-stu-id="5ffbb-112">_pxProcedure_ (**xltypeStr** or **xltypeNum**)</span></span>
  
<span data-ttu-id="5ffbb-113">Se uma cadeia de caracteres, o nome da função a ser chamada.</span><span class="sxs-lookup"><span data-stu-id="5ffbb-113">If a string, the name of the function to call.</span></span> <span data-ttu-id="5ffbb-114">Se um número, o número ordinal exportar o número da função a ser chamada.</span><span class="sxs-lookup"><span data-stu-id="5ffbb-114">If a number, the ordinal export number of the function to call.</span></span> <span data-ttu-id="5ffbb-115">Para manter a clareza e robustez, sempre use o formulário de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="5ffbb-115">For clarity and robustness, always use the string form.</span></span>
  
<span data-ttu-id="5ffbb-116">_pxTypeText_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="5ffbb-116">_pxTypeText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="5ffbb-117">Uma cadeia de caracteres opcional especificando os tipos de todos os argumentos para a função e o tipo do valor de retorno da função.</span><span class="sxs-lookup"><span data-stu-id="5ffbb-117">An optional string specifying the types of all the arguments to the function and the type of the return value of the function.</span></span> <span data-ttu-id="5ffbb-118">Para obter mais informações, consulte a seção "Comentários".</span><span class="sxs-lookup"><span data-stu-id="5ffbb-118">For more information, see the "Remarks" section.</span></span> <span data-ttu-id="5ffbb-119">Este argumento pode ser emitido para um autônomo DLL (XLL) definindo **xlAutoRegister**.</span><span class="sxs-lookup"><span data-stu-id="5ffbb-119">This argument can be omitted for a stand-alone DLL (XLL) defining **xlAutoRegister**.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="5ffbb-120">Valor de propriedade/Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="5ffbb-120">Property value/Return value</span></span>

<span data-ttu-id="5ffbb-121">Retorna a ID de registro da função (**xltypeNum**), que pode ser usada em chamadas subsequentes para **xlfUnregister**.</span><span class="sxs-lookup"><span data-stu-id="5ffbb-121">Returns the register ID of the function (**xltypeNum**), which can be used in subsequent calls to **xlfUnregister**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5ffbb-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="5ffbb-122">Remarks</span></span>

<span data-ttu-id="5ffbb-123">Essa função é útil quando você não quiser preocupar mantendo um identificador de registro, mas você precisa de um posteriormente para cancelar o registro.</span><span class="sxs-lookup"><span data-stu-id="5ffbb-123">This function is useful when you do not want to worry about maintaining a register ID, but you need one later for unregistering.</span></span> <span data-ttu-id="5ffbb-124">Também é útil para atribuição a botões, ferramentas e menus quando a função que você deseja atribuir estiver em uma DLL.</span><span class="sxs-lookup"><span data-stu-id="5ffbb-124">It is also useful for assigning to menus, tools, and buttons when the function you want to assign is in a DLL.</span></span>
  
<span data-ttu-id="5ffbb-125">Onde uma função DLL ou XLL foi registrada com um argumento válido _pxFunctionText_ tendo sido fornecido ao **xlfRegister**, sua identificação register também pode ser obtida ao passar o _pxFunctionText_ para a função **xlfEvaluate**.</span><span class="sxs-lookup"><span data-stu-id="5ffbb-125">Where a DLL or XLL function has been registered with a valid  _pxFunctionText_ argument having been supplied to **xlfRegister**, its register ID can also be obtained by passing the  _pxFunctionText_ to the function **xlfEvaluate**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5ffbb-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="5ffbb-126">See also</span></span>

- [<span data-ttu-id="5ffbb-127">REGISTRAR</span><span class="sxs-lookup"><span data-stu-id="5ffbb-127">REGISTER</span></span>](xlfregister-form-1.md)
- [<span data-ttu-id="5ffbb-128">CANCELAR O REGISTRO</span><span class="sxs-lookup"><span data-stu-id="5ffbb-128">UNREGISTER</span></span>](xlfunregister-form-1.md)
- [<span data-ttu-id="5ffbb-129">Funções XLM essenciais e úteis para a API de C</span><span class="sxs-lookup"><span data-stu-id="5ffbb-129">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

