---
title: TempErr/TempErr12
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempErr
- TempErr12
keywords:
- função temperr [Excel 2007], função TempErr12 [Excel 2007]
localization_priority: Normal
ms.assetid: cf8c26b2-ca2b-4dda-a02d-0ccbeac19106
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 68a0addc36ecf1b4491ab1e4f5b10f359bbc59c3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310343"
---
# <a name="temperrtemperr12"></a><span data-ttu-id="5627c-104">TempErr/TempErr12</span><span class="sxs-lookup"><span data-stu-id="5627c-104">TempErr/TempErr12</span></span>

 <span data-ttu-id="5627c-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="5627c-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="5627c-106">A função da biblioteca de estrutura que cria um **XLOPER de XLOPER**/ \*\*\*\* temporário contendo um erro de planilha do Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="5627c-106">Framework library function that creates a temporary **XLOPER**/ **XLOPER12** containing a Microsoft Excel worksheet error.</span></span> 
  
```cs
LPXLOPER TempErr(WORD err);
LPXLOPER12 TempErr12(BOOL err);
```

## <a name="parameters"></a><span data-ttu-id="5627c-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5627c-107">Parameters</span></span>

 <span data-ttu-id="5627c-108">_err_</span><span class="sxs-lookup"><span data-stu-id="5627c-108">_err_</span></span>
  
<span data-ttu-id="5627c-109">O código de erro desejado ou seu equivalente numérico literal, conforme mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="5627c-109">The desired error code, or its literal numeric equivalent, as shown in the following table.</span></span>
  
|<span data-ttu-id="5627c-110">**Error**</span><span class="sxs-lookup"><span data-stu-id="5627c-110">**Error**</span></span>|<span data-ttu-id="5627c-111">**Código de erro definido no XLCALL. 0**</span><span class="sxs-lookup"><span data-stu-id="5627c-111">**Error code defined in XLCALL.H**</span></span>|<span data-ttu-id="5627c-112">**Equivalente Decimal**</span><span class="sxs-lookup"><span data-stu-id="5627c-112">**Decimal equivalent**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5627c-113">#NULL</span><span class="sxs-lookup"><span data-stu-id="5627c-113">#NULL</span></span>  <br/> |<span data-ttu-id="5627c-114">**xlerrNull**</span><span class="sxs-lookup"><span data-stu-id="5627c-114">**xlerrNull**</span></span> <br/> |<span data-ttu-id="5627c-115">,0</span><span class="sxs-lookup"><span data-stu-id="5627c-115">0</span></span>  <br/> |
|<span data-ttu-id="5627c-116">#DIV/0!</span><span class="sxs-lookup"><span data-stu-id="5627c-116">#DIV/0!</span></span>  <br/> |<span data-ttu-id="5627c-117">**xlerrDiv0**</span><span class="sxs-lookup"><span data-stu-id="5627c-117">**xlerrDiv0**</span></span> <br/> |<span data-ttu-id="5627c-118">178</span><span class="sxs-lookup"><span data-stu-id="5627c-118">7</span></span>  <br/> |
|<span data-ttu-id="5627c-119">#VALUE!</span><span class="sxs-lookup"><span data-stu-id="5627c-119">#VALUE!</span></span>  <br/> |<span data-ttu-id="5627c-120">**xlerrValue**</span><span class="sxs-lookup"><span data-stu-id="5627c-120">**xlerrValue**</span></span> <br/> |<span data-ttu-id="5627c-121">15</span><span class="sxs-lookup"><span data-stu-id="5627c-121">15</span></span>  <br/> |
|<span data-ttu-id="5627c-122">#REF!</span><span class="sxs-lookup"><span data-stu-id="5627c-122">#REF!</span></span>  <br/> |<span data-ttu-id="5627c-123">**xlerrRef**</span><span class="sxs-lookup"><span data-stu-id="5627c-123">**xlerrRef**</span></span> <br/> |<span data-ttu-id="5627c-124">23</span><span class="sxs-lookup"><span data-stu-id="5627c-124">23</span></span>  <br/> |
|<span data-ttu-id="5627c-125">#NAME?</span><span class="sxs-lookup"><span data-stu-id="5627c-125">#NAME?</span></span>  <br/> |<span data-ttu-id="5627c-126">**xlerrName**</span><span class="sxs-lookup"><span data-stu-id="5627c-126">**xlerrName**</span></span> <br/> |<span data-ttu-id="5627c-127">anos</span><span class="sxs-lookup"><span data-stu-id="5627c-127">29</span></span>  <br/> |
|<span data-ttu-id="5627c-128">#NUM!</span><span class="sxs-lookup"><span data-stu-id="5627c-128">#NUM!</span></span>  <br/> |<span data-ttu-id="5627c-129">**xlerrNum**</span><span class="sxs-lookup"><span data-stu-id="5627c-129">**xlerrNum**</span></span> <br/> |<span data-ttu-id="5627c-130">36</span><span class="sxs-lookup"><span data-stu-id="5627c-130">36</span></span>  <br/> |
|<span data-ttu-id="5627c-131">#N/A</span><span class="sxs-lookup"><span data-stu-id="5627c-131">#N/A</span></span>  <br/> |<span data-ttu-id="5627c-132">**xlerrNA**</span><span class="sxs-lookup"><span data-stu-id="5627c-132">**xlerrNA**</span></span> <br/> |<span data-ttu-id="5627c-133">42</span><span class="sxs-lookup"><span data-stu-id="5627c-133">42</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="5627c-134">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="5627c-134">Return value</span></span>

<span data-ttu-id="5627c-135">Retorna um **xltypeBool** contendo o código de erro passado.</span><span class="sxs-lookup"><span data-stu-id="5627c-135">Returns an **xltypeBool** containing the error code passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="5627c-136">Exemplo</span><span class="sxs-lookup"><span data-stu-id="5627c-136">Example</span></span>

<span data-ttu-id="5627c-137">Este exemplo usa a função **TempErr12** para retornar um #VALUE!</span><span class="sxs-lookup"><span data-stu-id="5627c-137">This example uses the **TempErr12** function to return a #VALUE!</span></span> <span data-ttu-id="5627c-138">erro no Excel.</span><span class="sxs-lookup"><span data-stu-id="5627c-138">error to Excel.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="5627c-139">A função de biblioteca da estrutura **TempErr12** aloca memória de um buffer interno, que normalmente é liberado quando a função de estrutura **Excel12f** é chamada.</span><span class="sxs-lookup"><span data-stu-id="5627c-139">The Framework library function **TempErr12** allocates memory from an internal buffer, which is normally freed when the Framework function **Excel12f** is called.</span></span> <span data-ttu-id="5627c-140">Se esta função de exemplo for chamada repetidamente sem o **Excel12f** ser chamado, ocorrerá um vazamento de memória.</span><span class="sxs-lookup"><span data-stu-id="5627c-140">If this example function is called repeatedly without **Excel12f** being called, a memory leak occurs.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
LPXLOPER WINAPI TempErrExample(void)
{
    return TempErr12(xlerrValue);
}
```

## <a name="see-also"></a><span data-ttu-id="5627c-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="5627c-141">See also</span></span>



[<span data-ttu-id="5627c-142">Funções na biblioteca do Framework</span><span class="sxs-lookup"><span data-stu-id="5627c-142">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

