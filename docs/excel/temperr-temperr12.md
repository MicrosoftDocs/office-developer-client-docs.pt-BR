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
- função temperr [excel 2007], função TempErr12 [Excel 2007]
localization_priority: Normal
ms.assetid: cf8c26b2-ca2b-4dda-a02d-0ccbeac19106
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 22c0ff1b8259fc0e5ee70edb06bb3db53781ff8c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765435"
---
# <a name="temperrtemperr12"></a><span data-ttu-id="3aa3b-104">TempErr/TempErr12</span><span class="sxs-lookup"><span data-stu-id="3aa3b-104">TempErr/TempErr12</span></span>

 <span data-ttu-id="3aa3b-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="3aa3b-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="3aa3b-106">Função da biblioteca de Framework que cria um temporário **XLOPER**/ **XLOPER12** contendo um erro de planilha do Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="3aa3b-106">Framework library function that creates a temporary **XLOPER**/ **XLOPER12** containing a Microsoft Excel worksheet error.</span></span> 
  
```cs
LPXLOPER TempErr(WORD err);
LPXLOPER12 TempErr12(BOOL err);
```

## <a name="parameters"></a><span data-ttu-id="3aa3b-107">Par�metros</span><span class="sxs-lookup"><span data-stu-id="3aa3b-107">Parameters</span></span>

 <span data-ttu-id="3aa3b-108">_Err_</span><span class="sxs-lookup"><span data-stu-id="3aa3b-108">_err_</span></span>
  
<span data-ttu-id="3aa3b-109">O código de erro desejado ou seu equivalente numérico literal, conforme mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="3aa3b-109">The desired error code, or its literal numeric equivalent, as shown in the following table.</span></span>
  
|<span data-ttu-id="3aa3b-110">**Erro**</span><span class="sxs-lookup"><span data-stu-id="3aa3b-110">**Error**</span></span>|<span data-ttu-id="3aa3b-111">**Código de erro definido no XLCALL. H**</span><span class="sxs-lookup"><span data-stu-id="3aa3b-111">**Error code defined in XLCALL.H**</span></span>|<span data-ttu-id="3aa3b-112">**Equivalente decimal**</span><span class="sxs-lookup"><span data-stu-id="3aa3b-112">**Decimal equivalent**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3aa3b-113">#NULL</span><span class="sxs-lookup"><span data-stu-id="3aa3b-113">#NULL</span></span>  <br/> |<span data-ttu-id="3aa3b-114">**xlerrNull**</span><span class="sxs-lookup"><span data-stu-id="3aa3b-114">**xlerrNull**</span></span> <br/> |<span data-ttu-id="3aa3b-115">0</span><span class="sxs-lookup"><span data-stu-id="3aa3b-115">0</span></span>  <br/> |
|<span data-ttu-id="3aa3b-116">#DIV/0!</span><span class="sxs-lookup"><span data-stu-id="3aa3b-116">#DIV/0!</span></span>  <br/> |<span data-ttu-id="3aa3b-117">**xlerrDiv0**</span><span class="sxs-lookup"><span data-stu-id="3aa3b-117">**xlerrDiv0**</span></span> <br/> |<span data-ttu-id="3aa3b-118">7</span><span class="sxs-lookup"><span data-stu-id="3aa3b-118">7</span></span>  <br/> |
|<span data-ttu-id="3aa3b-119">#VALUE!</span><span class="sxs-lookup"><span data-stu-id="3aa3b-119">#VALUE!</span></span>  <br/> |<span data-ttu-id="3aa3b-120">**xlerrValue**</span><span class="sxs-lookup"><span data-stu-id="3aa3b-120">**xlerrValue**</span></span> <br/> |<span data-ttu-id="3aa3b-121">15</span><span class="sxs-lookup"><span data-stu-id="3aa3b-121">15</span></span>  <br/> |
|<span data-ttu-id="3aa3b-122">#REF!</span><span class="sxs-lookup"><span data-stu-id="3aa3b-122">#REF!</span></span>  <br/> |<span data-ttu-id="3aa3b-123">**xlerrRef**</span><span class="sxs-lookup"><span data-stu-id="3aa3b-123">**xlerrRef**</span></span> <br/> |<span data-ttu-id="3aa3b-124">23</span><span class="sxs-lookup"><span data-stu-id="3aa3b-124">23</span></span>  <br/> |
|<span data-ttu-id="3aa3b-125">#NAME?</span><span class="sxs-lookup"><span data-stu-id="3aa3b-125">#NAME?</span></span>  <br/> |<span data-ttu-id="3aa3b-126">**xlerrName**</span><span class="sxs-lookup"><span data-stu-id="3aa3b-126">**xlerrName**</span></span> <br/> |<span data-ttu-id="3aa3b-127">29</span><span class="sxs-lookup"><span data-stu-id="3aa3b-127">29</span></span>  <br/> |
|<span data-ttu-id="3aa3b-128">#NUM!</span><span class="sxs-lookup"><span data-stu-id="3aa3b-128">#NUM!</span></span>  <br/> |<span data-ttu-id="3aa3b-129">**xlerrNum**</span><span class="sxs-lookup"><span data-stu-id="3aa3b-129">**xlerrNum**</span></span> <br/> |<span data-ttu-id="3aa3b-130">36</span><span class="sxs-lookup"><span data-stu-id="3aa3b-130">36</span></span>  <br/> |
|<span data-ttu-id="3aa3b-131">#N/A</span><span class="sxs-lookup"><span data-stu-id="3aa3b-131">#N/A</span></span>  <br/> |<span data-ttu-id="3aa3b-132">**xlerrNA**</span><span class="sxs-lookup"><span data-stu-id="3aa3b-132">**xlerrNA**</span></span> <br/> |<span data-ttu-id="3aa3b-133">42</span><span class="sxs-lookup"><span data-stu-id="3aa3b-133">42</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="3aa3b-134">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="3aa3b-134">Return value</span></span>

<span data-ttu-id="3aa3b-135">Retorna um **xltypeBool** que contém o código de erro passados.</span><span class="sxs-lookup"><span data-stu-id="3aa3b-135">Returns an **xltypeBool** containing the error code passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="3aa3b-136">Example</span><span class="sxs-lookup"><span data-stu-id="3aa3b-136">Example</span></span>

<span data-ttu-id="3aa3b-137">Este exemplo usa a função **TempErr12** para retornar um #VALUE!</span><span class="sxs-lookup"><span data-stu-id="3aa3b-137">This example uses the **TempErr12** function to return a #VALUE!</span></span> <span data-ttu-id="3aa3b-138">erro para o Excel.</span><span class="sxs-lookup"><span data-stu-id="3aa3b-138">error to Excel.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="3aa3b-139">A função de biblioteca Framework **TempErr12** aloca memória de um buffer interno, que normalmente é liberado quando a função Framework **Excel12f** é chamada.</span><span class="sxs-lookup"><span data-stu-id="3aa3b-139">The Framework library function **TempErr12** allocates memory from an internal buffer, which is normally freed when the Framework function **Excel12f** is called.</span></span> <span data-ttu-id="3aa3b-140">Se a função neste exemplo é chamada repetidamente sem **Excel12f** está sendo chamado, ocorre um vazamento de memória.</span><span class="sxs-lookup"><span data-stu-id="3aa3b-140">If this example function is called repeatedly without **Excel12f** being called, a memory leak occurs.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
LPXLOPER WINAPI TempErrExample(void)
{
    return TempErr12(xlerrValue);
}
```

## <a name="see-also"></a><span data-ttu-id="3aa3b-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="3aa3b-141">See also</span></span>



[<span data-ttu-id="3aa3b-142">Funções na biblioteca do Framework</span><span class="sxs-lookup"><span data-stu-id="3aa3b-142">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

