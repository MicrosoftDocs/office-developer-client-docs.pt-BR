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
description: Retorna o restante (módulo) que resulta quando um número é dividido por um divisor.
ms.openlocfilehash: f6b713b1b3a9d2afa85f49de9d451642a00d8dad
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429268"
---
# <a name="modulus-function"></a><span data-ttu-id="21f15-103">Função MODULUS</span><span class="sxs-lookup"><span data-stu-id="21f15-103">MODULUS Function</span></span>

<span data-ttu-id="21f15-104">Retorna o restante (módulo) que resulta quando um número é dividido por um divisor.</span><span class="sxs-lookup"><span data-stu-id="21f15-104">Returns the remainder (modulus) that results when a number is divided by a divisor.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="21f15-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="21f15-105">Syntax</span></span>

<span data-ttu-id="21f15-106">MODULUS(\*\* *number* \*\*, \*\* *divisor* \*\* )</span><span class="sxs-lookup"><span data-stu-id="21f15-106">MODULUS(\*\* *number* \*\*, \*\* *divisor* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="21f15-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="21f15-107">Parameters</span></span>

|<span data-ttu-id="21f15-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="21f15-108">**Name**</span></span>|<span data-ttu-id="21f15-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="21f15-109">**Required/Optional**</span></span>|<span data-ttu-id="21f15-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="21f15-110">**Data Type**</span></span>|<span data-ttu-id="21f15-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="21f15-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="21f15-112">_number_</span><span class="sxs-lookup"><span data-stu-id="21f15-112">_number_</span></span> <br/> |<span data-ttu-id="21f15-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="21f15-113">Required</span></span>  <br/> |<span data-ttu-id="21f15-114">**Número**</span><span class="sxs-lookup"><span data-stu-id="21f15-114">**Number**</span></span> <br/> |<span data-ttu-id="21f15-115">O dividendo.</span><span class="sxs-lookup"><span data-stu-id="21f15-115">The dividend.</span></span>  <br/> |
| <span data-ttu-id="21f15-116">_divisor_</span><span class="sxs-lookup"><span data-stu-id="21f15-116">_divisor_</span></span> <br/> |<span data-ttu-id="21f15-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="21f15-117">Required</span></span>  <br/> |<span data-ttu-id="21f15-118">**Número**</span><span class="sxs-lookup"><span data-stu-id="21f15-118">**Number**</span></span> <br/> |<span data-ttu-id="21f15-119">O divisor.</span><span class="sxs-lookup"><span data-stu-id="21f15-119">The divisor.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="21f15-120">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="21f15-120">Return value</span></span>

<span data-ttu-id="21f15-121">Número</span><span class="sxs-lookup"><span data-stu-id="21f15-121">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="21f15-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="21f15-122">Remarks</span></span>

<span data-ttu-id="21f15-p101">O resultado tem o mesmo sinal do divisor. Um erro de #DIV/0! será retornado se o divisor for 0.</span><span class="sxs-lookup"><span data-stu-id="21f15-p101">The result has the same sign as the divisor. A #DIV/0! error is returned if the divisor is 0.</span></span> 
  
<span data-ttu-id="21f15-126">Na maioria das situações, a função MODULUS deve ser usada em vez da função MOD.</span><span class="sxs-lookup"><span data-stu-id="21f15-126">In almost all situations, the MODULUS function should be used rather than the MOD function.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="21f15-127">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="21f15-127">Example 1</span></span>

<span data-ttu-id="21f15-128">MODULUS(5, 1,4)</span><span class="sxs-lookup"><span data-stu-id="21f15-128">MODULUS(5, 1.4)</span></span>
  
<span data-ttu-id="21f15-129">Retornará 0,8.</span><span class="sxs-lookup"><span data-stu-id="21f15-129">Returns 0.8.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="21f15-130">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="21f15-130">Example 2</span></span>

<span data-ttu-id="21f15-131">MODULUS(5, -1,4)</span><span class="sxs-lookup"><span data-stu-id="21f15-131">MODULUS(5, -1.4)</span></span>
  
<span data-ttu-id="21f15-132">Retornará -0,6.</span><span class="sxs-lookup"><span data-stu-id="21f15-132">Returns -0.6.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="21f15-133">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="21f15-133">Example 3</span></span>

<span data-ttu-id="21f15-134">MODULUS(-5, 1,4)</span><span class="sxs-lookup"><span data-stu-id="21f15-134">MODULUS(-5, 1.4)</span></span>
  
<span data-ttu-id="21f15-135">Retornará 0,6.</span><span class="sxs-lookup"><span data-stu-id="21f15-135">Returns 0.6.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="21f15-136">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="21f15-136">Example 4</span></span>

<span data-ttu-id="21f15-137">MODULUS(-5, -1,4)</span><span class="sxs-lookup"><span data-stu-id="21f15-137">MODULUS(-5, -1.4)</span></span>
  
<span data-ttu-id="21f15-138">Retornará -0,8.</span><span class="sxs-lookup"><span data-stu-id="21f15-138">Returns -0.8.</span></span>
  

