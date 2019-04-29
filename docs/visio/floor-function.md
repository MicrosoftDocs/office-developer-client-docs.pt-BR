---
title: Função FLOOR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251423
localization_priority: Normal
ms.assetid: 6788bc96-cc86-5f21-781f-67274e7f605a
description: Arredonda um número para 0 (zero), para o próximo inteiro ou para a próxima instância de múltiplo.
ms.openlocfilehash: 7a16a77a990180f34dd7a5706c24ec3232438467
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439895"
---
# <a name="floor-function"></a><span data-ttu-id="c6bc3-103">Função FLOOR</span><span class="sxs-lookup"><span data-stu-id="c6bc3-103">FLOOR Function</span></span>

<span data-ttu-id="c6bc3-104">Arredonda um número para 0 (zero), para o próximo inteiro ou para a próxima instância de _múltiplo_.</span><span class="sxs-lookup"><span data-stu-id="c6bc3-104">Rounds a number toward 0 (zero), to the next integer, or to the next instance of  _multiple_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="c6bc3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c6bc3-105">Syntax</span></span>

<span data-ttu-id="c6bc3-106">PISO (\* \* *número* \* \*, \* \* *múltiplo* \* \*)</span><span class="sxs-lookup"><span data-stu-id="c6bc3-106">FLOOR(\*\* *number* \*\*, \*\* *multiple* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="c6bc3-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c6bc3-107">Parameters</span></span>

|<span data-ttu-id="c6bc3-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="c6bc3-108">**Name**</span></span>|<span data-ttu-id="c6bc3-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="c6bc3-109">**Required/Optional**</span></span>|<span data-ttu-id="c6bc3-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="c6bc3-110">**Data Type**</span></span>|<span data-ttu-id="c6bc3-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="c6bc3-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="c6bc3-112">_number_</span><span class="sxs-lookup"><span data-stu-id="c6bc3-112">_number_</span></span> <br/> |<span data-ttu-id="c6bc3-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="c6bc3-113">Required</span></span>  <br/> |<span data-ttu-id="c6bc3-114">**Número**</span><span class="sxs-lookup"><span data-stu-id="c6bc3-114">**Number**</span></span> <br/> |<span data-ttu-id="c6bc3-115">O número a ser arredondado.</span><span class="sxs-lookup"><span data-stu-id="c6bc3-115">The number to round.</span></span>  <br/> |
| <span data-ttu-id="c6bc3-116">_vários_</span><span class="sxs-lookup"><span data-stu-id="c6bc3-116">_multiple_</span></span> <br/> |<span data-ttu-id="c6bc3-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="c6bc3-117">Required</span></span>  <br/> |<span data-ttu-id="c6bc3-118">**Número**</span><span class="sxs-lookup"><span data-stu-id="c6bc3-118">**Number**</span></span> <br/> |<span data-ttu-id="c6bc3-119">O múltiplo para o qual arredondar.</span><span class="sxs-lookup"><span data-stu-id="c6bc3-119">The multiple to which to round.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="c6bc3-120">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="c6bc3-120">Return value</span></span>

<span data-ttu-id="c6bc3-121">Número</span><span class="sxs-lookup"><span data-stu-id="c6bc3-121">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c6bc3-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="c6bc3-122">Remarks</span></span>

<span data-ttu-id="c6bc3-123">Se _múltiplo_ não for especificado, o número será arredondado para 0 até o próximo inteiro.</span><span class="sxs-lookup"><span data-stu-id="c6bc3-123">If  _multiple_ is not specified, the number rounds toward 0 to the next integer.</span></span> 
  
 <span data-ttu-id="c6bc3-124">_Número_ e _múltiplos_ devem ter os mesmos sinais ou um #NUM!</span><span class="sxs-lookup"><span data-stu-id="c6bc3-124">_Number_ and  _multiple_ must have the same signs, or a #NUM!</span></span> <span data-ttu-id="c6bc3-125">será retornado.</span><span class="sxs-lookup"><span data-stu-id="c6bc3-125">error is returned.</span></span> <span data-ttu-id="c6bc3-126">Se um ou _vários_ _números_ não puderem ser convertidos em um valor, um #VALUE!</span><span class="sxs-lookup"><span data-stu-id="c6bc3-126">If either  _number_ or  _multiple_ cannot be converted to a value, a #VALUE!</span></span> <span data-ttu-id="c6bc3-127">será retornado.</span><span class="sxs-lookup"><span data-stu-id="c6bc3-127">error is returned.</span></span> <span data-ttu-id="c6bc3-128">Se um dos _números_ ou _vários_ for 0, o resultado será 0.</span><span class="sxs-lookup"><span data-stu-id="c6bc3-128">If either  _number_ or  _multiple_ is 0, the result is 0.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="c6bc3-129">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c6bc3-129">Example 1</span></span>

<span data-ttu-id="c6bc3-130">PISO (3.7)</span><span class="sxs-lookup"><span data-stu-id="c6bc3-130">FLOOR(3.7)</span></span>
  
<span data-ttu-id="c6bc3-131">Retornará 3.</span><span class="sxs-lookup"><span data-stu-id="c6bc3-131">Returns 3.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="c6bc3-132">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="c6bc3-132">Example 2</span></span>

<span data-ttu-id="c6bc3-133">FLOOR (-3,7)</span><span class="sxs-lookup"><span data-stu-id="c6bc3-133">FLOOR(-3.7)</span></span>
  
<span data-ttu-id="c6bc3-134">Retornará -3.</span><span class="sxs-lookup"><span data-stu-id="c6bc3-134">Returns -3.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="c6bc3-135">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="c6bc3-135">Example 3</span></span>

<span data-ttu-id="c6bc3-136">PISO (3.7, 0,5)</span><span class="sxs-lookup"><span data-stu-id="c6bc3-136">FLOOR(3.7, 0.5)</span></span>
  
<span data-ttu-id="c6bc3-137">Retornará 3,5.</span><span class="sxs-lookup"><span data-stu-id="c6bc3-137">Returns 3.5.</span></span>
  

