---
title: Função MODULUS
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251465
localization_priority: Normal
ms.assetid: cb6326a5-1bf8-b6a3-5c0d-d38c071353a5
description: Retorna o resto que resulta quando um número é dividido por um divisor.
ms.openlocfilehash: 4e2ef7acf9dc04e788cb2b8a0ff737f12a79c61a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772399"
---
# <a name="modulus-function"></a><span data-ttu-id="e01ea-103">Função MODULUS</span><span class="sxs-lookup"><span data-stu-id="e01ea-103">MODULUS Function</span></span>

<span data-ttu-id="e01ea-104">Retorna o resto que resulta quando um número é dividido por um divisor.</span><span class="sxs-lookup"><span data-stu-id="e01ea-104">Returns the remainder (modulus) that results when a number is divided by a divisor.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="e01ea-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e01ea-105">Syntax</span></span>

<span data-ttu-id="e01ea-106">MODULUS (* * *número* * *, * * *divisor* * *)</span><span class="sxs-lookup"><span data-stu-id="e01ea-106">MODULUS(** *number* **, ** *divisor* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="e01ea-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e01ea-107">Parameters</span></span>

|<span data-ttu-id="e01ea-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="e01ea-108">**Name**</span></span>|<span data-ttu-id="e01ea-109">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="e01ea-109">**Required/Optional**</span></span>|<span data-ttu-id="e01ea-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="e01ea-110">**Data Type**</span></span>|<span data-ttu-id="e01ea-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="e01ea-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="e01ea-112">_number_</span><span class="sxs-lookup"><span data-stu-id="e01ea-112">_number_</span></span> <br/> |<span data-ttu-id="e01ea-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="e01ea-113">Required</span></span>  <br/> |<span data-ttu-id="e01ea-114">**Número**</span><span class="sxs-lookup"><span data-stu-id="e01ea-114">**Number**</span></span> <br/> |<span data-ttu-id="e01ea-115">O dividendo.</span><span class="sxs-lookup"><span data-stu-id="e01ea-115">The dividend.</span></span>  <br/> |
| <span data-ttu-id="e01ea-116">_divisor_</span><span class="sxs-lookup"><span data-stu-id="e01ea-116">_divisor_</span></span> <br/> |<span data-ttu-id="e01ea-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="e01ea-117">Required</span></span>  <br/> |<span data-ttu-id="e01ea-118">**Número**</span><span class="sxs-lookup"><span data-stu-id="e01ea-118">**Number**</span></span> <br/> |<span data-ttu-id="e01ea-119">O divisor.</span><span class="sxs-lookup"><span data-stu-id="e01ea-119">The divisor.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="e01ea-120">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="e01ea-120">Return value</span></span>

<span data-ttu-id="e01ea-121">Number</span><span class="sxs-lookup"><span data-stu-id="e01ea-121">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e01ea-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="e01ea-122">Remarks</span></span>

<span data-ttu-id="e01ea-p101">O resultado tem o mesmo sinal do divisor. Um erro de #DIV/0! será retornado se o divisor for 0.</span><span class="sxs-lookup"><span data-stu-id="e01ea-p101">The result has the same sign as the divisor. A #DIV/0! error is returned if the divisor is 0.</span></span> 
  
<span data-ttu-id="e01ea-126">Na maioria das situações, a função MODULUS deve ser usada em vez da função MOD.</span><span class="sxs-lookup"><span data-stu-id="e01ea-126">In almost all situations, the MODULUS function should be used rather than the MOD function.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="e01ea-127">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e01ea-127">Example 1</span></span>

<span data-ttu-id="e01ea-128">MODULUS(5, 1,4)</span><span class="sxs-lookup"><span data-stu-id="e01ea-128">MODULUS(5, 1.4)</span></span>
  
<span data-ttu-id="e01ea-129">Retornará 0,8.</span><span class="sxs-lookup"><span data-stu-id="e01ea-129">Returns 0.8.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="e01ea-130">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="e01ea-130">Example 2</span></span>

<span data-ttu-id="e01ea-131">MODULUS(5, -1,4)</span><span class="sxs-lookup"><span data-stu-id="e01ea-131">MODULUS(5, -1.4)</span></span>
  
<span data-ttu-id="e01ea-132">Retornará -0,6.</span><span class="sxs-lookup"><span data-stu-id="e01ea-132">Returns -0.6.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="e01ea-133">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="e01ea-133">Example 3</span></span>

<span data-ttu-id="e01ea-134">MODULUS(-5, 1,4)</span><span class="sxs-lookup"><span data-stu-id="e01ea-134">MODULUS(-5, 1.4)</span></span>
  
<span data-ttu-id="e01ea-135">Retornará 0,6.</span><span class="sxs-lookup"><span data-stu-id="e01ea-135">Returns 0.6.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="e01ea-136">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="e01ea-136">Example 4</span></span>

<span data-ttu-id="e01ea-137">MODULUS(-5, -1,4)</span><span class="sxs-lookup"><span data-stu-id="e01ea-137">MODULUS(-5, -1.4)</span></span>
  
<span data-ttu-id="e01ea-138">Retornará -0,8.</span><span class="sxs-lookup"><span data-stu-id="e01ea-138">Returns -0.8.</span></span>
  

