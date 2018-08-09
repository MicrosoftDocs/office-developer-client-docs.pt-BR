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
description: Arredonda um número de 0 (zero), para o próximo número inteiro ou para a próxima instância do múltiplo.
ms.openlocfilehash: f66b993e3ab48fd1abc685b7db5889d5bf24fbfc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771889"
---
# <a name="floor-function"></a><span data-ttu-id="e3ca8-103">Função FLOOR</span><span class="sxs-lookup"><span data-stu-id="e3ca8-103">FLOOR Function</span></span>

<span data-ttu-id="e3ca8-104">Arredonda um número de 0 (zero), para o próximo número inteiro ou para a próxima instância do _vários_.</span><span class="sxs-lookup"><span data-stu-id="e3ca8-104">Rounds a number toward 0 (zero), to the next integer, or to the next instance of  _multiple_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="e3ca8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e3ca8-105">Syntax</span></span>

<span data-ttu-id="e3ca8-106">FLOOR (* * *número* * *, * * *vários* * *)</span><span class="sxs-lookup"><span data-stu-id="e3ca8-106">FLOOR(** *number* **, ** *multiple* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="e3ca8-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e3ca8-107">Parameters</span></span>

|<span data-ttu-id="e3ca8-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="e3ca8-108">**Name**</span></span>|<span data-ttu-id="e3ca8-109">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="e3ca8-109">**Required/Optional**</span></span>|<span data-ttu-id="e3ca8-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="e3ca8-110">**Data Type**</span></span>|<span data-ttu-id="e3ca8-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="e3ca8-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="e3ca8-112">_number_</span><span class="sxs-lookup"><span data-stu-id="e3ca8-112">_number_</span></span> <br/> |<span data-ttu-id="e3ca8-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="e3ca8-113">Required</span></span>  <br/> |<span data-ttu-id="e3ca8-114">**Número**</span><span class="sxs-lookup"><span data-stu-id="e3ca8-114">**Number**</span></span> <br/> |<span data-ttu-id="e3ca8-115">O número a ser arredondado.</span><span class="sxs-lookup"><span data-stu-id="e3ca8-115">The number to round.</span></span>  <br/> |
| <span data-ttu-id="e3ca8-116">_vários_</span><span class="sxs-lookup"><span data-stu-id="e3ca8-116">_multiple_</span></span> <br/> |<span data-ttu-id="e3ca8-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="e3ca8-117">Required</span></span>  <br/> |<span data-ttu-id="e3ca8-118">**Número**</span><span class="sxs-lookup"><span data-stu-id="e3ca8-118">**Number**</span></span> <br/> |<span data-ttu-id="e3ca8-119">O múltiplo para o qual arredondar.</span><span class="sxs-lookup"><span data-stu-id="e3ca8-119">The multiple to which to round.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="e3ca8-120">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="e3ca8-120">Return value</span></span>

<span data-ttu-id="e3ca8-121">Number</span><span class="sxs-lookup"><span data-stu-id="e3ca8-121">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e3ca8-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="e3ca8-122">Remarks</span></span>

<span data-ttu-id="e3ca8-123">Se _vários_ não for especificado, o número será arredondado para 0 do próximo número inteiro.</span><span class="sxs-lookup"><span data-stu-id="e3ca8-123">If  _multiple_ is not specified, the number rounds toward 0 to the next integer.</span></span> 
  
 <span data-ttu-id="e3ca8-124">_Número_ e _vários_ devem ter o mesmo sinal ou um #NUM!</span><span class="sxs-lookup"><span data-stu-id="e3ca8-124">_Number_ and  _multiple_ must have the same signs, or a #NUM!</span></span> <span data-ttu-id="e3ca8-125">erro será retornado.</span><span class="sxs-lookup"><span data-stu-id="e3ca8-125">error is returned.</span></span> <span data-ttu-id="e3ca8-126">Se o _número_ ou o _múltiplo_ não puder ser convertida para um valor, um #VALUE!</span><span class="sxs-lookup"><span data-stu-id="e3ca8-126">If either  _number_ or  _multiple_ cannot be converted to a value, a #VALUE!</span></span> <span data-ttu-id="e3ca8-127">erro será retornado.</span><span class="sxs-lookup"><span data-stu-id="e3ca8-127">error is returned.</span></span> <span data-ttu-id="e3ca8-128">Se o _número_ ou o _múltiplo_ for 0, o resultado é 0.</span><span class="sxs-lookup"><span data-stu-id="e3ca8-128">If either  _number_ or  _multiple_ is 0, the result is 0.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="e3ca8-129">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e3ca8-129">Example 1</span></span>

<span data-ttu-id="e3ca8-130">FLOOR(3.7)</span><span class="sxs-lookup"><span data-stu-id="e3ca8-130">FLOOR(3.7)</span></span>
  
<span data-ttu-id="e3ca8-131">Retornará 3.</span><span class="sxs-lookup"><span data-stu-id="e3ca8-131">Returns 3.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="e3ca8-132">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="e3ca8-132">Example 2</span></span>

<span data-ttu-id="e3ca8-133">FLOOR(-3.7)</span><span class="sxs-lookup"><span data-stu-id="e3ca8-133">FLOOR(-3.7)</span></span>
  
<span data-ttu-id="e3ca8-134">Retornará -3.</span><span class="sxs-lookup"><span data-stu-id="e3ca8-134">Returns -3.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="e3ca8-135">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="e3ca8-135">Example 3</span></span>

<span data-ttu-id="e3ca8-136">FLOOR (3,7, 0,5)</span><span class="sxs-lookup"><span data-stu-id="e3ca8-136">FLOOR(3.7, 0.5)</span></span>
  
<span data-ttu-id="e3ca8-137">Retornará 3,5.</span><span class="sxs-lookup"><span data-stu-id="e3ca8-137">Returns 3.5.</span></span>
  

