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
description: Arredonda um número de 0 (zero) para a próxima instância do múltiplo. Se multiple não for especificado, o número será arredondado para longe de 0 do próximo número inteiro.
ms.openlocfilehash: fa982b44ea4a73e7da614c49a52cd50efd612f20
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771447"
---
# <a name="ceiling-function"></a><span data-ttu-id="ea6c7-104">Função CEILING</span><span class="sxs-lookup"><span data-stu-id="ea6c7-104">CEILING Function</span></span>

<span data-ttu-id="ea6c7-105">Arredonda um número de 0 (zero) para a próxima instância do _vários_.</span><span class="sxs-lookup"><span data-stu-id="ea6c7-105">Rounds a number away from 0 (zero) to the next instance of  _multiple_.</span></span> <span data-ttu-id="ea6c7-106">Se _vários_ não for especificado, o número será arredondado para longe de 0 do próximo número inteiro.</span><span class="sxs-lookup"><span data-stu-id="ea6c7-106">If  _multiple_ is not specified, the number rounds away from 0 to the next integer.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="ea6c7-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ea6c7-107">Syntax</span></span>

<span data-ttu-id="ea6c7-108">CEILING (* * *número* * *, * * *vários* * *)</span><span class="sxs-lookup"><span data-stu-id="ea6c7-108">CEILING(** *number* **, ** *multiple* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="ea6c7-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ea6c7-109">Parameters</span></span>

|<span data-ttu-id="ea6c7-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="ea6c7-110">**Name**</span></span>|<span data-ttu-id="ea6c7-111">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="ea6c7-111">**Required/Optional**</span></span>|<span data-ttu-id="ea6c7-112">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="ea6c7-112">**Data Type**</span></span>|<span data-ttu-id="ea6c7-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="ea6c7-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="ea6c7-114">_number_</span><span class="sxs-lookup"><span data-stu-id="ea6c7-114">_number_</span></span> <br/> |<span data-ttu-id="ea6c7-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="ea6c7-115">Required</span></span>  <br/> |<span data-ttu-id="ea6c7-116">**Número**</span><span class="sxs-lookup"><span data-stu-id="ea6c7-116">**Number**</span></span> <br/> |<span data-ttu-id="ea6c7-117">O número a ser arredondado.</span><span class="sxs-lookup"><span data-stu-id="ea6c7-117">The number to round.</span></span>  <br/> |
| <span data-ttu-id="ea6c7-118">_vários_</span><span class="sxs-lookup"><span data-stu-id="ea6c7-118">_multiple_</span></span> <br/> |<span data-ttu-id="ea6c7-119">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="ea6c7-119">Required</span></span>  <br/> |<span data-ttu-id="ea6c7-120">**Número**</span><span class="sxs-lookup"><span data-stu-id="ea6c7-120">**Number**</span></span> <br/> |<span data-ttu-id="ea6c7-121">O múltiplo para arredondar para.</span><span class="sxs-lookup"><span data-stu-id="ea6c7-121">The multiple to round to.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ea6c7-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="ea6c7-122">Remarks</span></span>

 <span data-ttu-id="ea6c7-123">_Número_ e _vários_ devem ter o mesmo sinal ou um #NUM!</span><span class="sxs-lookup"><span data-stu-id="ea6c7-123">_Number_ and  _multiple_ must have the same signs, or a #NUM!</span></span> <span data-ttu-id="ea6c7-124">erro será retornado.</span><span class="sxs-lookup"><span data-stu-id="ea6c7-124">error is returned.</span></span> <span data-ttu-id="ea6c7-125">Se o _número_ ou o _múltiplo_ não puder ser convertida para um valor, um #VALUE!</span><span class="sxs-lookup"><span data-stu-id="ea6c7-125">If either  _number_ or  _multiple_ cannot be converted to a value, a #VALUE!</span></span> <span data-ttu-id="ea6c7-126">erro será retornado.</span><span class="sxs-lookup"><span data-stu-id="ea6c7-126">error is returned.</span></span> <span data-ttu-id="ea6c7-127">Se o _número_ ou o _múltiplo_ for 0, o resultado é 0.</span><span class="sxs-lookup"><span data-stu-id="ea6c7-127">If either  _number_ or  _multiple_ is 0, the result is 0.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="ea6c7-128">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ea6c7-128">Example 1</span></span>

<span data-ttu-id="ea6c7-129">CEILING(3.7)</span><span class="sxs-lookup"><span data-stu-id="ea6c7-129">CEILING(3.7)</span></span>
  
<span data-ttu-id="ea6c7-130">Retornará 4</span><span class="sxs-lookup"><span data-stu-id="ea6c7-130">Returns 4</span></span>
  
## <a name="example-2"></a><span data-ttu-id="ea6c7-131">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="ea6c7-131">Example 2</span></span>

<span data-ttu-id="ea6c7-132">CEILING(-3.7)</span><span class="sxs-lookup"><span data-stu-id="ea6c7-132">CEILING(-3.7)</span></span>
  
<span data-ttu-id="ea6c7-133">Retornará -4</span><span class="sxs-lookup"><span data-stu-id="ea6c7-133">Returns -4</span></span>
  
## <a name="example-3"></a><span data-ttu-id="ea6c7-134">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="ea6c7-134">Example 3</span></span>

<span data-ttu-id="ea6c7-135">CEILING (3,7, 0,25)</span><span class="sxs-lookup"><span data-stu-id="ea6c7-135">CEILING(3.7, 0.25)</span></span>
  
<span data-ttu-id="ea6c7-136">Retornará 3,75</span><span class="sxs-lookup"><span data-stu-id="ea6c7-136">Returns 3.75</span></span>
  

