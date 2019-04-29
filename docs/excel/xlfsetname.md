---
title: xlfSetName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfSetName
keywords:
- função xlfSetName [Excel 2007]
localization_priority: Normal
ms.assetid: ea7fd713-7c1b-4648-a609-3334f595c61a
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: e6327ccf2cd18e42c3ef9abe538e6f669e498352
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404257"
---
# <a name="xlfsetname"></a><span data-ttu-id="d2b08-104">xlfSetName</span><span class="sxs-lookup"><span data-stu-id="d2b08-104">xlfSetName</span></span>

<span data-ttu-id="d2b08-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="d2b08-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="d2b08-106">Usado para criar e excluir nomes definidos associados à DLL.</span><span class="sxs-lookup"><span data-stu-id="d2b08-106">Used to create and delete defined names associated with the DLL.</span></span>
  
```cs
Excel12(xlfSetName, LPXLOPER12 pxRes, 2, LPXLOPER12 pxNameText, LPXLOPER12 pxNameDefinition);
```

## <a name="parameters"></a><span data-ttu-id="d2b08-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d2b08-107">Parameters</span></span>

<span data-ttu-id="d2b08-108">_pxNameText_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="d2b08-108">_pxNameText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="d2b08-109">O nome do intervalo, que deve estar em conformidade com as limitações normais no Microsoft Excel em nomes válidos.</span><span class="sxs-lookup"><span data-stu-id="d2b08-109">The name of the range, which should conform to the usual limitations in Microsoft Excel on valid names.</span></span>
  
<span data-ttu-id="d2b08-110">_pxNameDefinition_ (**xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeMulti**, **xltypeSRef**, **xltypeRef**ou **xltypeInt**)</span><span class="sxs-lookup"><span data-stu-id="d2b08-110">_pxNameDefinition_ (**xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeMulti**, **xltypeSRef**, **xltypeRef**, or **xltypeInt**)</span></span>
  
<span data-ttu-id="d2b08-111">(Opcional).</span><span class="sxs-lookup"><span data-stu-id="d2b08-111">(Optional).</span></span> <span data-ttu-id="d2b08-112">O valor, o conjunto de valores, a célula ou o intervalo de células que o _pxNameText_ está definido como.</span><span class="sxs-lookup"><span data-stu-id="d2b08-112">The value, set of values, cell, or range of cells that  _pxNameText_ is defined as.</span></span> <span data-ttu-id="d2b08-113">Se for omitido, o nome será excluído.</span><span class="sxs-lookup"><span data-stu-id="d2b08-113">If omitted, the name is deleted.</span></span> 
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="d2b08-114">Valor de propriedade/Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="d2b08-114">Property value/Return value</span></span>

<span data-ttu-id="d2b08-115">_pxRes_ (**xltypeBool** ou **xltypeErr**)</span><span class="sxs-lookup"><span data-stu-id="d2b08-115">_pxRes_ (**xltypeBool** or **xltypeErr**)</span></span>
  
<span data-ttu-id="d2b08-116">TRUE se a operação foi bem-sucedida ou FALSE se o nome não pôde ser criado ou excluído.</span><span class="sxs-lookup"><span data-stu-id="d2b08-116">TRUE if the operation succeeded or FALSE if the name could not be created or deleted.</span></span> <span data-ttu-id="d2b08-117">Retorna #VALUE!</span><span class="sxs-lookup"><span data-stu-id="d2b08-117">Returns #VALUE!</span></span> <span data-ttu-id="d2b08-118">se um ou mais argumentos forem inválidos.</span><span class="sxs-lookup"><span data-stu-id="d2b08-118">if one or more of the arguments was invalid.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d2b08-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="d2b08-119">Remarks</span></span>

<span data-ttu-id="d2b08-120">Quando um comando ou função é registrado usando **xlfRegister** com um argumento _pxFunctionText_ válido, o Excel cria um nome associado ao recurso dll.</span><span class="sxs-lookup"><span data-stu-id="d2b08-120">When a function or command is registered using **xlfRegister** with a valid  _pxFunctionText_ argument, Excel creates a name associated with the DLL resource.</span></span> <span data-ttu-id="d2b08-121">Quando sua DLL estiver sendo descarregada, esses nomes devem ser excluídos usando a [função xlfSetName](xlfsetname.md).</span><span class="sxs-lookup"><span data-stu-id="d2b08-121">When your DLL is being unloaded, such names should be deleted using the [xlfSetName function](xlfsetname.md).</span></span> <span data-ttu-id="d2b08-122">No enTanto, devido a um problema conhecido no Excel, essa operação de exclusão falha.</span><span class="sxs-lookup"><span data-stu-id="d2b08-122">However, due to a known issue in Excel, this deletion operation fails.</span></span> <span data-ttu-id="d2b08-123">Confira mais informações em [Problemas conhecidos no desenvolvimento de XLL do Excel](known-issues-in-excel-xll-development.md).</span><span class="sxs-lookup"><span data-stu-id="d2b08-123">For more information, see [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
  
### <a name="example"></a><span data-ttu-id="d2b08-124">Exemplo</span><span class="sxs-lookup"><span data-stu-id="d2b08-124">Example</span></span>

<span data-ttu-id="d2b08-125">Consulte o código para a função **xlAutoClose** no `\SAMPLES\GENERIC\GENERIC.C`.</span><span class="sxs-lookup"><span data-stu-id="d2b08-125">See the code for the **xlAutoClose** function in  `\SAMPLES\GENERIC\GENERIC.C`.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d2b08-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="d2b08-126">See also</span></span>

- [<span data-ttu-id="d2b08-127">Funções XLM essenciais e úteis para a API C</span><span class="sxs-lookup"><span data-stu-id="d2b08-127">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

