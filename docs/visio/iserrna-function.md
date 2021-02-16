---
title: Função ISERRNA
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251451
localization_priority: Normal
ms.assetid: 6ee7dc3d-efe9-c862-f71d-034b3d9c3ec6
description: 'Retorna TRUE se o valor de cellreference for tipo de erro #N/A! (não disponível); caso contrário, retornará FALSE. A função ISERRNA é usada em fórmulas que se referem a outra célula.'
ms.openlocfilehash: 8a398eca6da659a6b8f29e4ef8e31b18abf56fde
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432111"
---
# <a name="iserrna-function"></a><span data-ttu-id="8dd9f-105">Função ISERRNA</span><span class="sxs-lookup"><span data-stu-id="8dd9f-105">ISERRNA Function</span></span>

<span data-ttu-id="8dd9f-106">Retorna TRUE se o valor de  _cellreference for_ tipo de erro #N/A!</span><span class="sxs-lookup"><span data-stu-id="8dd9f-106">Returns TRUE if the value of  _cellreference_ is error type #N/A!</span></span> <span data-ttu-id="8dd9f-107">(não disponível); caso contrário, retornará FALSE.</span><span class="sxs-lookup"><span data-stu-id="8dd9f-107">(not available); otherwise, it returns FALSE.</span></span> <span data-ttu-id="8dd9f-108">A função ISERRNA é usada em fórmulas que se referem a outra célula.</span><span class="sxs-lookup"><span data-stu-id="8dd9f-108">The ISERRNA function is used in formulas that refer to another cell.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="8dd9f-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8dd9f-109">Syntax</span></span>

<span data-ttu-id="8dd9f-110">ISERRNA(\*\* *cellreference* \*\* )</span><span class="sxs-lookup"><span data-stu-id="8dd9f-110">ISERRNA(\*\* *cellreference* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="8dd9f-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8dd9f-111">Parameters</span></span>

|<span data-ttu-id="8dd9f-112">**Name**</span><span class="sxs-lookup"><span data-stu-id="8dd9f-112">**Name**</span></span>|<span data-ttu-id="8dd9f-113">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="8dd9f-113">**Required/Optional**</span></span>|<span data-ttu-id="8dd9f-114">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="8dd9f-114">**Data Type**</span></span>|<span data-ttu-id="8dd9f-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="8dd9f-115">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="8dd9f-116">_cellreference_</span><span class="sxs-lookup"><span data-stu-id="8dd9f-116">_cellreference_</span></span> <br/> |<span data-ttu-id="8dd9f-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="8dd9f-117">Required</span></span>  <br/> |<span data-ttu-id="8dd9f-118">**String**</span><span class="sxs-lookup"><span data-stu-id="8dd9f-118">**String**</span></span> <br/> |<span data-ttu-id="8dd9f-119">Referência a uma célula.</span><span class="sxs-lookup"><span data-stu-id="8dd9f-119">Reference to a cell.</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="8dd9f-120">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8dd9f-120">Example 1</span></span>

|<span data-ttu-id="8dd9f-121">**Cell**</span><span class="sxs-lookup"><span data-stu-id="8dd9f-121">**Cell**</span></span>|<span data-ttu-id="8dd9f-122">**Fórmula**</span><span class="sxs-lookup"><span data-stu-id="8dd9f-122">**Formula**</span></span>|<span data-ttu-id="8dd9f-123">**Valor retornado**</span><span class="sxs-lookup"><span data-stu-id="8dd9f-123">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8dd9f-124">Scratch.A1</span><span class="sxs-lookup"><span data-stu-id="8dd9f-124">Scratch.A1</span></span>  <br/> |<span data-ttu-id="8dd9f-125">="5 + 3"</span><span class="sxs-lookup"><span data-stu-id="8dd9f-125">="5 + 3"</span></span>  <br/> |<span data-ttu-id="8dd9f-126">"8"</span><span class="sxs-lookup"><span data-stu-id="8dd9f-126">"8"</span></span>  <br/> |
|<span data-ttu-id="8dd9f-127">Scratch.B1</span><span class="sxs-lookup"><span data-stu-id="8dd9f-127">Scratch.B1</span></span>  <br/> |<span data-ttu-id="8dd9f-128">=ISERRNA(Scratch.A1)</span><span class="sxs-lookup"><span data-stu-id="8dd9f-128">=ISERRNA(Scratch.A1)</span></span>  <br/> |<span data-ttu-id="8dd9f-129">FALSE</span><span class="sxs-lookup"><span data-stu-id="8dd9f-129">FALSE</span></span>  <br/> |
   
<span data-ttu-id="8dd9f-130">Retornará FALSO porque o valor retornado está disponível.</span><span class="sxs-lookup"><span data-stu-id="8dd9f-130">Returns FALSE because the value returned is available.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="8dd9f-131">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="8dd9f-131">Example 2</span></span>

|<span data-ttu-id="8dd9f-132">**Cell**</span><span class="sxs-lookup"><span data-stu-id="8dd9f-132">**Cell**</span></span>|<span data-ttu-id="8dd9f-133">**Fórmula**</span><span class="sxs-lookup"><span data-stu-id="8dd9f-133">**Formula**</span></span>|<span data-ttu-id="8dd9f-134">**Valor retornado**</span><span class="sxs-lookup"><span data-stu-id="8dd9f-134">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8dd9f-135">Scratch.A1</span><span class="sxs-lookup"><span data-stu-id="8dd9f-135">Scratch.A1</span></span>  <br/> |<span data-ttu-id="8dd9f-136">=NA( )</span><span class="sxs-lookup"><span data-stu-id="8dd9f-136">=NA( )</span></span>  <br/> |<span data-ttu-id="8dd9f-137">#N/A!</span><span class="sxs-lookup"><span data-stu-id="8dd9f-137">#N/A!</span></span>  <br/> |
|<span data-ttu-id="8dd9f-138">Scratch.B1</span><span class="sxs-lookup"><span data-stu-id="8dd9f-138">Scratch.B1</span></span>  <br/> |<span data-ttu-id="8dd9f-139">=ISERRNA(Scratch.A1)</span><span class="sxs-lookup"><span data-stu-id="8dd9f-139">=ISERRNA(Scratch.A1)</span></span>  <br/> |<span data-ttu-id="8dd9f-140">TRUE</span><span class="sxs-lookup"><span data-stu-id="8dd9f-140">TRUE</span></span>  <br/> |
   
<span data-ttu-id="8dd9f-141">Retornará VERDADEIRO porque o valor retornado é um tipo de erro de #N/A!</span><span class="sxs-lookup"><span data-stu-id="8dd9f-141">Returns TRUE because the value returned is error type #N/A!</span></span>
  

