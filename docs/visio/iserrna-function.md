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
description: 'Retorna TRUE se o valor de referênciadecélula for o tipo de erro # n/d! (não disponível); Caso contrário, ele retornará FALSE. A função ISERRNA é usada em fórmulas que se referem a outra célula.'
ms.openlocfilehash: a471119265d77866e51ccc6bb556f2ce0095d31d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772110"
---
# <a name="iserrna-function"></a><span data-ttu-id="f615a-105">Função ISERRNA</span><span class="sxs-lookup"><span data-stu-id="f615a-105">ISERRNA Function</span></span>

<span data-ttu-id="f615a-106">Retorna TRUE se o valor de _referênciadecélula_ for o tipo de erro # n/d!</span><span class="sxs-lookup"><span data-stu-id="f615a-106">Returns TRUE if the value of  _cellreference_ is error type #N/A!</span></span> <span data-ttu-id="f615a-107">(não disponível); Caso contrário, ele retornará FALSE.</span><span class="sxs-lookup"><span data-stu-id="f615a-107">(not available); otherwise, it returns FALSE.</span></span> <span data-ttu-id="f615a-108">A função ISERRNA é usada em fórmulas que se referem a outra célula.</span><span class="sxs-lookup"><span data-stu-id="f615a-108">The ISERRNA function is used in formulas that refer to another cell.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="f615a-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f615a-109">Syntax</span></span>

<span data-ttu-id="f615a-110">ISERRNA (* * *referênciadecélula* * *)</span><span class="sxs-lookup"><span data-stu-id="f615a-110">ISERRNA(** *cellreference* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="f615a-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f615a-111">Parameters</span></span>

|<span data-ttu-id="f615a-112">**Name**</span><span class="sxs-lookup"><span data-stu-id="f615a-112">**Name**</span></span>|<span data-ttu-id="f615a-113">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="f615a-113">**Required/Optional**</span></span>|<span data-ttu-id="f615a-114">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="f615a-114">**Data Type**</span></span>|<span data-ttu-id="f615a-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="f615a-115">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="f615a-116">_referênciadecélula_</span><span class="sxs-lookup"><span data-stu-id="f615a-116">_cellreference_</span></span> <br/> |<span data-ttu-id="f615a-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="f615a-117">Required</span></span>  <br/> |<span data-ttu-id="f615a-118">**String**</span><span class="sxs-lookup"><span data-stu-id="f615a-118">**String**</span></span> <br/> |<span data-ttu-id="f615a-119">Referência a uma célula.</span><span class="sxs-lookup"><span data-stu-id="f615a-119">Reference to a cell.</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="f615a-120">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f615a-120">Example 1</span></span>

|<span data-ttu-id="f615a-121">**Célula**</span><span class="sxs-lookup"><span data-stu-id="f615a-121">**Cell**</span></span>|<span data-ttu-id="f615a-122">**Formula**</span><span class="sxs-lookup"><span data-stu-id="f615a-122">**Formula**</span></span>|<span data-ttu-id="f615a-123">**Valor retornado**</span><span class="sxs-lookup"><span data-stu-id="f615a-123">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f615a-124">Scratch. a1</span><span class="sxs-lookup"><span data-stu-id="f615a-124">Scratch.A1</span></span>  <br/> |<span data-ttu-id="f615a-125">="5 + 3"</span><span class="sxs-lookup"><span data-stu-id="f615a-125">="5 + 3"</span></span>  <br/> |<span data-ttu-id="f615a-126">"8"</span><span class="sxs-lookup"><span data-stu-id="f615a-126">"8"</span></span>  <br/> |
|<span data-ttu-id="f615a-127">Scratch.B1</span><span class="sxs-lookup"><span data-stu-id="f615a-127">Scratch.B1</span></span>  <br/> |<span data-ttu-id="f615a-128">=ISERRNA(Scratch.a1)</span><span class="sxs-lookup"><span data-stu-id="f615a-128">=ISERRNA(Scratch.A1)</span></span>  <br/> |<span data-ttu-id="f615a-129">FALSO</span><span class="sxs-lookup"><span data-stu-id="f615a-129">FALSE</span></span>  <br/> |
   
<span data-ttu-id="f615a-130">Retornará FALSO porque o valor retornado está disponível.</span><span class="sxs-lookup"><span data-stu-id="f615a-130">Returns FALSE because the value returned is available.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="f615a-131">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="f615a-131">Example 2</span></span>

|<span data-ttu-id="f615a-132">**Célula**</span><span class="sxs-lookup"><span data-stu-id="f615a-132">**Cell**</span></span>|<span data-ttu-id="f615a-133">**Formula**</span><span class="sxs-lookup"><span data-stu-id="f615a-133">**Formula**</span></span>|<span data-ttu-id="f615a-134">**Valor retornado**</span><span class="sxs-lookup"><span data-stu-id="f615a-134">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f615a-135">Scratch. a1</span><span class="sxs-lookup"><span data-stu-id="f615a-135">Scratch.A1</span></span>  <br/> |<span data-ttu-id="f615a-136">=NA( )</span><span class="sxs-lookup"><span data-stu-id="f615a-136">=NA( )</span></span>  <br/> |<span data-ttu-id="f615a-137">#N/A!</span><span class="sxs-lookup"><span data-stu-id="f615a-137">#N/A!</span></span>  <br/> |
|<span data-ttu-id="f615a-138">Scratch.B1</span><span class="sxs-lookup"><span data-stu-id="f615a-138">Scratch.B1</span></span>  <br/> |<span data-ttu-id="f615a-139">=ISERRNA(Scratch.a1)</span><span class="sxs-lookup"><span data-stu-id="f615a-139">=ISERRNA(Scratch.A1)</span></span>  <br/> |<span data-ttu-id="f615a-140">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="f615a-140">TRUE</span></span>  <br/> |
   
<span data-ttu-id="f615a-141">Retornará VERDADEIRO porque o valor retornado é um tipo de erro de #N/A!</span><span class="sxs-lookup"><span data-stu-id="f615a-141">Returns TRUE because the value returned is error type #N/A!</span></span>
  

