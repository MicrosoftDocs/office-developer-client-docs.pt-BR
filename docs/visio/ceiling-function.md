---
title: Função CEILING
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251405
localization_priority: Normal
ms.assetid: 1a8d6d48-7ae3-5483-28d2-5b1706088a53
description: Cerca um número de distância de 0 (zero) para a próxima instância de vários. Se vários não for especificado, o número arredoda para longe de 0 para o próximo inteiro.
ms.openlocfilehash: 449f17d1b68c116cccb2635723a3f6277d0ac2a9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404124"
---
# <a name="ceiling-function"></a><span data-ttu-id="d6675-104">Função CEILING</span><span class="sxs-lookup"><span data-stu-id="d6675-104">CEILING Function</span></span>

<span data-ttu-id="d6675-105">Volta um número de distância de 0 (zero) para a próxima instância de  _vários_.</span><span class="sxs-lookup"><span data-stu-id="d6675-105">Rounds a number away from 0 (zero) to the next instance of  _multiple_.</span></span> <span data-ttu-id="d6675-106">Se  _vários_ não for especificado, o número arredoda para longe de 0 para o próximo inteiro.</span><span class="sxs-lookup"><span data-stu-id="d6675-106">If  _multiple_ is not specified, the number rounds away from 0 to the next integer.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="d6675-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d6675-107">Syntax</span></span>

<span data-ttu-id="d6675-108">CEILING(\*\* *number* \*\*, \*\* *multiple* \*\* )</span><span class="sxs-lookup"><span data-stu-id="d6675-108">CEILING(\*\* *number* \*\*, \*\* *multiple* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="d6675-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d6675-109">Parameters</span></span>

|<span data-ttu-id="d6675-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="d6675-110">**Name**</span></span>|<span data-ttu-id="d6675-111">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="d6675-111">**Required/Optional**</span></span>|<span data-ttu-id="d6675-112">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="d6675-112">**Data Type**</span></span>|<span data-ttu-id="d6675-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="d6675-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="d6675-114">_number_</span><span class="sxs-lookup"><span data-stu-id="d6675-114">_number_</span></span> <br/> |<span data-ttu-id="d6675-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="d6675-115">Required</span></span>  <br/> |<span data-ttu-id="d6675-116">**Número**</span><span class="sxs-lookup"><span data-stu-id="d6675-116">**Number**</span></span> <br/> |<span data-ttu-id="d6675-117">O número a ser arredondado.</span><span class="sxs-lookup"><span data-stu-id="d6675-117">The number to round.</span></span>  <br/> |
| <span data-ttu-id="d6675-118">_multiple_</span><span class="sxs-lookup"><span data-stu-id="d6675-118">_multiple_</span></span> <br/> |<span data-ttu-id="d6675-119">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="d6675-119">Required</span></span>  <br/> |<span data-ttu-id="d6675-120">**Número**</span><span class="sxs-lookup"><span data-stu-id="d6675-120">**Number**</span></span> <br/> |<span data-ttu-id="d6675-121">O múltiplo para arredondar para.</span><span class="sxs-lookup"><span data-stu-id="d6675-121">The multiple to round to.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d6675-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="d6675-122">Remarks</span></span>

 <span data-ttu-id="d6675-123">_Número_ e  _múltiplo_ devem ter os mesmos sinais ou um #NUM!</span><span class="sxs-lookup"><span data-stu-id="d6675-123">_Number_ and  _multiple_ must have the same signs, or a #NUM!</span></span> <span data-ttu-id="d6675-124">será retornado.</span><span class="sxs-lookup"><span data-stu-id="d6675-124">error is returned.</span></span> <span data-ttu-id="d6675-125">Se um  _ou_  _vários_ não puderem ser convertidos em um valor, um #VALUE!</span><span class="sxs-lookup"><span data-stu-id="d6675-125">If either  _number_ or  _multiple_ cannot be converted to a value, a #VALUE!</span></span> <span data-ttu-id="d6675-126">será retornado.</span><span class="sxs-lookup"><span data-stu-id="d6675-126">error is returned.</span></span> <span data-ttu-id="d6675-127">Se um  _ou_  _vários_ for 0, o resultado será 0.</span><span class="sxs-lookup"><span data-stu-id="d6675-127">If either  _number_ or  _multiple_ is 0, the result is 0.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="d6675-128">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d6675-128">Example 1</span></span>

<span data-ttu-id="d6675-129">CEILING(3,7)</span><span class="sxs-lookup"><span data-stu-id="d6675-129">CEILING(3.7)</span></span>
  
<span data-ttu-id="d6675-130">Retornará 4</span><span class="sxs-lookup"><span data-stu-id="d6675-130">Returns 4</span></span>
  
## <a name="example-2"></a><span data-ttu-id="d6675-131">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="d6675-131">Example 2</span></span>

<span data-ttu-id="d6675-132">CEILING(-3,7)</span><span class="sxs-lookup"><span data-stu-id="d6675-132">CEILING(-3.7)</span></span>
  
<span data-ttu-id="d6675-133">Retornará -4</span><span class="sxs-lookup"><span data-stu-id="d6675-133">Returns -4</span></span>
  
## <a name="example-3"></a><span data-ttu-id="d6675-134">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="d6675-134">Example 3</span></span>

<span data-ttu-id="d6675-135">CEILING(3,7, 0,25)</span><span class="sxs-lookup"><span data-stu-id="d6675-135">CEILING(3.7, 0.25)</span></span>
  
<span data-ttu-id="d6675-136">Retornará 3,75</span><span class="sxs-lookup"><span data-stu-id="d6675-136">Returns 3.75</span></span>
  

