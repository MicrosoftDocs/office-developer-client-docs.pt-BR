---
title: xlfSetName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfSetName
keywords:
- função xlfSetName [excel 2007]
localization_priority: Normal
ms.assetid: ea7fd713-7c1b-4648-a609-3334f595c61a
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 48ce927f6bcb328a90779948a660cf9d0b460205
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765464"
---
# <a name="xlfsetname"></a><span data-ttu-id="63532-104">xlfSetName</span><span class="sxs-lookup"><span data-stu-id="63532-104">xlfSetName</span></span>

<span data-ttu-id="63532-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="63532-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="63532-106">Usado para criar e excluir nomes definidos associados a DLL.</span><span class="sxs-lookup"><span data-stu-id="63532-106">Used to create and delete defined names associated with the DLL.</span></span>
  
```cs
Excel12(xlfSetName, LPXLOPER12 pxRes, 2, LPXLOPER12 pxNameText, LPXLOPER12 pxNameDefinition);
```

## <a name="parameters"></a><span data-ttu-id="63532-107">Par�metros</span><span class="sxs-lookup"><span data-stu-id="63532-107">Parameters</span></span>

<span data-ttu-id="63532-108">_pxNameText_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="63532-108">_pxNameText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="63532-109">O nome do intervalo, que deve se adequar às limitações usuais no Microsoft Excel sobre nomes válidos.</span><span class="sxs-lookup"><span data-stu-id="63532-109">The name of the range, which should conform to the usual limitations in Microsoft Excel on valid names.</span></span>
  
<span data-ttu-id="63532-110">_pxNameDefinition_ (**xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeMulti**, **xltypeSRef**, **xltypeRef**ou **xltypeInt**)</span><span class="sxs-lookup"><span data-stu-id="63532-110">_pxNameDefinition_ (**xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeMulti**, **xltypeSRef**, **xltypeRef**, or **xltypeInt**)</span></span>
  
<span data-ttu-id="63532-111">(Opcional).</span><span class="sxs-lookup"><span data-stu-id="63532-111">(Optional).</span></span> <span data-ttu-id="63532-112">O valor, o conjunto de valores, célula ou intervalo de células que _pxNameText_ é definido como.</span><span class="sxs-lookup"><span data-stu-id="63532-112">The value, set of values, cell, or range of cells that  _pxNameText_ is defined as.</span></span> <span data-ttu-id="63532-113">Se for omitido, o nome é excluído.</span><span class="sxs-lookup"><span data-stu-id="63532-113">If omitted, the name is deleted.</span></span> 
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="63532-114">Propriedade valor/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="63532-114">Property value/Return value</span></span>

<span data-ttu-id="63532-115">_pxRes_ (**xltypeBool** ou **xltypeErr**)</span><span class="sxs-lookup"><span data-stu-id="63532-115">_pxRes_ (**xltypeBool** or **xltypeErr**)</span></span>
  
<span data-ttu-id="63532-116">TRUE se a operação foi bem-sucedida ou FALSE se o nome não pôde ser criado ou excluído.</span><span class="sxs-lookup"><span data-stu-id="63532-116">TRUE if the operation succeeded or FALSE if the name could not be created or deleted.</span></span> <span data-ttu-id="63532-117">Retorna #VALUE!</span><span class="sxs-lookup"><span data-stu-id="63532-117">Returns #VALUE!</span></span> <span data-ttu-id="63532-118">Se um ou mais dos argumentos eram inválida.</span><span class="sxs-lookup"><span data-stu-id="63532-118">if one or more of the arguments was invalid.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="63532-119">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="63532-119">Remarks</span></span>

<span data-ttu-id="63532-120">Quando um comando ou uma função é registrado usando **xlfRegister** com um argumento válido _pxFunctionText_ , o Excel criará um nome associado a DLL de recurso.</span><span class="sxs-lookup"><span data-stu-id="63532-120">When a function or command is registered using **xlfRegister** with a valid  _pxFunctionText_ argument, Excel creates a name associated with the DLL resource.</span></span> <span data-ttu-id="63532-121">Quando sua DLL está sendo descarregado, tais nomes devem ser excluídos usando a [função xlfSetName](xlfsetname.md).</span><span class="sxs-lookup"><span data-stu-id="63532-121">When your DLL is being unloaded, such names should be deleted using the [xlfSetName function](xlfsetname.md).</span></span> <span data-ttu-id="63532-122">No entanto, devido a um problema conhecido no Excel, essa operação de exclusão falhar.</span><span class="sxs-lookup"><span data-stu-id="63532-122">However, due to a known issue in Excel, this deletion operation fails.</span></span> <span data-ttu-id="63532-123">Para obter mais informações, consulte [Problemas conhecidos no desenvolvimento de XLL do Excel](known-issues-in-excel-xll-development.md).</span><span class="sxs-lookup"><span data-stu-id="63532-123">For more information, see [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
  
### <a name="example"></a><span data-ttu-id="63532-124">Example</span><span class="sxs-lookup"><span data-stu-id="63532-124">Example</span></span>

<span data-ttu-id="63532-125">Ver o código para a função **xlAutoClose** em `\SAMPLES\GENERIC\GENERIC.C`.</span><span class="sxs-lookup"><span data-stu-id="63532-125">See the code for the **xlAutoClose** function in  `\SAMPLES\GENERIC\GENERIC.C`.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="63532-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="63532-126">See also</span></span>

- [<span data-ttu-id="63532-127">Funções de XLM API C essenciais e úteis</span><span class="sxs-lookup"><span data-stu-id="63532-127">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

