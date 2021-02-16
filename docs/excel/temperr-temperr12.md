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
- função queer [excel 2007],função TempErr12 [Excel 2007]
localization_priority: Normal
ms.assetid: cf8c26b2-ca2b-4dda-a02d-0ccbeac19106
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 68a0addc36ecf1b4491ab1e4f5b10f359bbc59c3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410606"
---
# <a name="temperrtemperr12"></a><span data-ttu-id="c02db-104">TempErr/TempErr12</span><span class="sxs-lookup"><span data-stu-id="c02db-104">TempErr/TempErr12</span></span>

 <span data-ttu-id="c02db-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="c02db-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="c02db-106">Função de biblioteca de estrutura que cria um  /  **XLOPER XLOPER12 temporário** contendo um erro de planilha do Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="c02db-106">Framework library function that creates a temporary **XLOPER**/ **XLOPER12** containing a Microsoft Excel worksheet error.</span></span> 
  
```cs
LPXLOPER TempErr(WORD err);
LPXLOPER12 TempErr12(BOOL err);
```

## <a name="parameters"></a><span data-ttu-id="c02db-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c02db-107">Parameters</span></span>

 <span data-ttu-id="c02db-108">_err_</span><span class="sxs-lookup"><span data-stu-id="c02db-108">_err_</span></span>
  
<span data-ttu-id="c02db-109">O código de erro desejado ou seu equivalente numérico literal, conforme mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="c02db-109">The desired error code, or its literal numeric equivalent, as shown in the following table.</span></span>
  
|<span data-ttu-id="c02db-110">**Erro**</span><span class="sxs-lookup"><span data-stu-id="c02db-110">**Error**</span></span>|<span data-ttu-id="c02db-111">**Código de erro definido em XLCALL. H**</span><span class="sxs-lookup"><span data-stu-id="c02db-111">**Error code defined in XLCALL.H**</span></span>|<span data-ttu-id="c02db-112">**Equivalente decimal**</span><span class="sxs-lookup"><span data-stu-id="c02db-112">**Decimal equivalent**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c02db-113">#NULL</span><span class="sxs-lookup"><span data-stu-id="c02db-113">#NULL</span></span>  <br/> |<span data-ttu-id="c02db-114">**xlerrNull**</span><span class="sxs-lookup"><span data-stu-id="c02db-114">**xlerrNull**</span></span> <br/> |<span data-ttu-id="c02db-115">0</span><span class="sxs-lookup"><span data-stu-id="c02db-115">0</span></span>  <br/> |
|<span data-ttu-id="c02db-116">#DIV/0!</span><span class="sxs-lookup"><span data-stu-id="c02db-116">#DIV/0!</span></span>  <br/> |<span data-ttu-id="c02db-117">**xlerrDiv0**</span><span class="sxs-lookup"><span data-stu-id="c02db-117">**xlerrDiv0**</span></span> <br/> |<span data-ttu-id="c02db-118">7 </span><span class="sxs-lookup"><span data-stu-id="c02db-118">7</span></span>  <br/> |
|<span data-ttu-id="c02db-119">#VALUE!</span><span class="sxs-lookup"><span data-stu-id="c02db-119">#VALUE!</span></span>  <br/> |<span data-ttu-id="c02db-120">**xlerrValue**</span><span class="sxs-lookup"><span data-stu-id="c02db-120">**xlerrValue**</span></span> <br/> |<span data-ttu-id="c02db-121">15 </span><span class="sxs-lookup"><span data-stu-id="c02db-121">15</span></span>  <br/> |
|<span data-ttu-id="c02db-122">#REF!</span><span class="sxs-lookup"><span data-stu-id="c02db-122">#REF!</span></span>  <br/> |<span data-ttu-id="c02db-123">**xlerrRef**</span><span class="sxs-lookup"><span data-stu-id="c02db-123">**xlerrRef**</span></span> <br/> |<span data-ttu-id="c02db-124">23</span><span class="sxs-lookup"><span data-stu-id="c02db-124">23</span></span>  <br/> |
|<span data-ttu-id="c02db-125">#NAME?</span><span class="sxs-lookup"><span data-stu-id="c02db-125">#NAME?</span></span>  <br/> |<span data-ttu-id="c02db-126">**xlerrName**</span><span class="sxs-lookup"><span data-stu-id="c02db-126">**xlerrName**</span></span> <br/> |<span data-ttu-id="c02db-127">29</span><span class="sxs-lookup"><span data-stu-id="c02db-127">29</span></span>  <br/> |
|<span data-ttu-id="c02db-128">#NUM!</span><span class="sxs-lookup"><span data-stu-id="c02db-128">#NUM!</span></span>  <br/> |<span data-ttu-id="c02db-129">**xlerrNum**</span><span class="sxs-lookup"><span data-stu-id="c02db-129">**xlerrNum**</span></span> <br/> |<span data-ttu-id="c02db-130">36</span><span class="sxs-lookup"><span data-stu-id="c02db-130">36</span></span>  <br/> |
|<span data-ttu-id="c02db-131">#N/A</span><span class="sxs-lookup"><span data-stu-id="c02db-131">#N/A</span></span>  <br/> |<span data-ttu-id="c02db-132">**xlerrNA**</span><span class="sxs-lookup"><span data-stu-id="c02db-132">**xlerrNA**</span></span> <br/> |<span data-ttu-id="c02db-133">42</span><span class="sxs-lookup"><span data-stu-id="c02db-133">42</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="c02db-134">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="c02db-134">Return value</span></span>

<span data-ttu-id="c02db-135">Retorna um **xltypeBool** que contém o código de erro passado.</span><span class="sxs-lookup"><span data-stu-id="c02db-135">Returns an **xltypeBool** containing the error code passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="c02db-136">Exemplo</span><span class="sxs-lookup"><span data-stu-id="c02db-136">Example</span></span>

<span data-ttu-id="c02db-137">Este exemplo usa a **função TempErr12** para retornar um #VALUE!</span><span class="sxs-lookup"><span data-stu-id="c02db-137">This example uses the **TempErr12** function to return a #VALUE!</span></span> <span data-ttu-id="c02db-138">para o Excel.</span><span class="sxs-lookup"><span data-stu-id="c02db-138">error to Excel.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="c02db-139">A função de biblioteca Do Framework **TempErr12** aloca memória de um buffer interno, que normalmente é liberado quando a função **Framework Excel12f** é chamada.</span><span class="sxs-lookup"><span data-stu-id="c02db-139">The Framework library function **TempErr12** allocates memory from an internal buffer, which is normally freed when the Framework function **Excel12f** is called.</span></span> <span data-ttu-id="c02db-140">Se esta função de exemplo for chamada repetidamente sem que **o Excel12f** seja chamado, ocorrerá um vazamento de memória.</span><span class="sxs-lookup"><span data-stu-id="c02db-140">If this example function is called repeatedly without **Excel12f** being called, a memory leak occurs.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
LPXLOPER WINAPI TempErrExample(void)
{
    return TempErr12(xlerrValue);
}
```

## <a name="see-also"></a><span data-ttu-id="c02db-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="c02db-141">See also</span></span>



[<span data-ttu-id="c02db-142">Funções na biblioteca do Framework</span><span class="sxs-lookup"><span data-stu-id="c02db-142">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

