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
description: Arredonda um número para fora de 0 (zero) para a próxima instância de múltiplo. Se múltiplo não for especificado, o número será arredondado para longe de 0 até o próximo inteiro.
ms.openlocfilehash: 449f17d1b68c116cccb2635723a3f6277d0ac2a9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337223"
---
# <a name="ceiling-function"></a><span data-ttu-id="19ba9-104">Função CEILING</span><span class="sxs-lookup"><span data-stu-id="19ba9-104">CEILING Function</span></span>

<span data-ttu-id="19ba9-105">Arredonda um número para fora de 0 (zero) para a próxima instância de _múltiplo_.</span><span class="sxs-lookup"><span data-stu-id="19ba9-105">Rounds a number away from 0 (zero) to the next instance of  _multiple_.</span></span> <span data-ttu-id="19ba9-106">Se _múltiplo_ não for especificado, o número será arredondado para longe de 0 até o próximo inteiro.</span><span class="sxs-lookup"><span data-stu-id="19ba9-106">If  _multiple_ is not specified, the number rounds away from 0 to the next integer.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="19ba9-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="19ba9-107">Syntax</span></span>

<span data-ttu-id="19ba9-108">TETO (\* \* *número* \* \*, \* \* *múltiplo* \* \*)</span><span class="sxs-lookup"><span data-stu-id="19ba9-108">CEILING(\*\* *number* \*\*, \*\* *multiple* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="19ba9-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="19ba9-109">Parameters</span></span>

|<span data-ttu-id="19ba9-110">**Nome**</span><span class="sxs-lookup"><span data-stu-id="19ba9-110">**Name**</span></span>|<span data-ttu-id="19ba9-111">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="19ba9-111">**Required/Optional**</span></span>|<span data-ttu-id="19ba9-112">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="19ba9-112">**Data Type**</span></span>|<span data-ttu-id="19ba9-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="19ba9-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="19ba9-114">_number_</span><span class="sxs-lookup"><span data-stu-id="19ba9-114">_number_</span></span> <br/> |<span data-ttu-id="19ba9-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="19ba9-115">Required</span></span>  <br/> |<span data-ttu-id="19ba9-116">**Número**</span><span class="sxs-lookup"><span data-stu-id="19ba9-116">**Number**</span></span> <br/> |<span data-ttu-id="19ba9-117">O número a ser arredondado.</span><span class="sxs-lookup"><span data-stu-id="19ba9-117">The number to round.</span></span>  <br/> |
| <span data-ttu-id="19ba9-118">_vários_</span><span class="sxs-lookup"><span data-stu-id="19ba9-118">_multiple_</span></span> <br/> |<span data-ttu-id="19ba9-119">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="19ba9-119">Required</span></span>  <br/> |<span data-ttu-id="19ba9-120">**Número**</span><span class="sxs-lookup"><span data-stu-id="19ba9-120">**Number**</span></span> <br/> |<span data-ttu-id="19ba9-121">O múltiplo a ser arredondado.</span><span class="sxs-lookup"><span data-stu-id="19ba9-121">The multiple to round to.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="19ba9-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="19ba9-122">Remarks</span></span>

 <span data-ttu-id="19ba9-123">_Número_ e _múltiplos_ devem ter os mesmos sinais ou um #NUM!</span><span class="sxs-lookup"><span data-stu-id="19ba9-123">_Number_ and  _multiple_ must have the same signs, or a #NUM!</span></span> <span data-ttu-id="19ba9-124">será retornado.</span><span class="sxs-lookup"><span data-stu-id="19ba9-124">error is returned.</span></span> <span data-ttu-id="19ba9-125">Se um ou _vários_ _números_ não puderem ser convertidos em um valor, um #VALUE!</span><span class="sxs-lookup"><span data-stu-id="19ba9-125">If either  _number_ or  _multiple_ cannot be converted to a value, a #VALUE!</span></span> <span data-ttu-id="19ba9-126">será retornado.</span><span class="sxs-lookup"><span data-stu-id="19ba9-126">error is returned.</span></span> <span data-ttu-id="19ba9-127">Se um dos _números_ ou _vários_ for 0, o resultado será 0.</span><span class="sxs-lookup"><span data-stu-id="19ba9-127">If either  _number_ or  _multiple_ is 0, the result is 0.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="19ba9-128">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="19ba9-128">Example 1</span></span>

<span data-ttu-id="19ba9-129">TETO (3.7)</span><span class="sxs-lookup"><span data-stu-id="19ba9-129">CEILING(3.7)</span></span>
  
<span data-ttu-id="19ba9-130">Retornará 4</span><span class="sxs-lookup"><span data-stu-id="19ba9-130">Returns 4</span></span>
  
## <a name="example-2"></a><span data-ttu-id="19ba9-131">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="19ba9-131">Example 2</span></span>

<span data-ttu-id="19ba9-132">TETO (-3,7)</span><span class="sxs-lookup"><span data-stu-id="19ba9-132">CEILING(-3.7)</span></span>
  
<span data-ttu-id="19ba9-133">Retornará -4</span><span class="sxs-lookup"><span data-stu-id="19ba9-133">Returns -4</span></span>
  
## <a name="example-3"></a><span data-ttu-id="19ba9-134">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="19ba9-134">Example 3</span></span>

<span data-ttu-id="19ba9-135">TETO (3.7, 0,25)</span><span class="sxs-lookup"><span data-stu-id="19ba9-135">CEILING(3.7, 0.25)</span></span>
  
<span data-ttu-id="19ba9-136">Retornará 3,75</span><span class="sxs-lookup"><span data-stu-id="19ba9-136">Returns 3.75</span></span>
  

