---
title: Função BOUNDINGBOXDIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8a2490f2-48c4-5df3-a3b3-40e8e0c80479
description: Retorna a medida da parte especificada da caixa delimitadora da forma.
ms.openlocfilehash: 94cad37c4a0d2c6c7e7c69d997af09a9d7f1d651
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771425"
---
# <a name="boundingboxdist-function"></a><span data-ttu-id="0732a-103">Função BOUNDINGBOXDIST</span><span class="sxs-lookup"><span data-stu-id="0732a-103">BOUNDINGBOXDIST Function</span></span>

<span data-ttu-id="0732a-104">Retorna a medida da parte especificada da caixa delimitadora da forma.</span><span class="sxs-lookup"><span data-stu-id="0732a-104">Returns the measurement of the specified part of the shape's bounding box.</span></span> 
  
## <a name="version-information"></a><span data-ttu-id="0732a-105">Informações da versão</span><span class="sxs-lookup"><span data-stu-id="0732a-105">Version Information</span></span>

<span data-ttu-id="0732a-106">Version Added: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="0732a-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="0732a-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0732a-107">Syntax</span></span>

<span data-ttu-id="0732a-108">BOUNDINGBOXDIST (* * *índice* * *)</span><span class="sxs-lookup"><span data-stu-id="0732a-108">BOUNDINGBOXDIST(** *Index* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="0732a-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0732a-109">Parameters</span></span>

|<span data-ttu-id="0732a-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="0732a-110">**Name**</span></span>|<span data-ttu-id="0732a-111">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="0732a-111">**Required/Optional**</span></span>|<span data-ttu-id="0732a-112">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="0732a-112">**Data Type**</span></span>|<span data-ttu-id="0732a-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="0732a-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="0732a-114">_Index_</span><span class="sxs-lookup"><span data-stu-id="0732a-114">_Index_</span></span> <br/> |<span data-ttu-id="0732a-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="0732a-115">Required</span></span>  <br/> |<span data-ttu-id="0732a-116">**Número**</span><span class="sxs-lookup"><span data-stu-id="0732a-116">**Number**</span></span> <br/> |<span data-ttu-id="0732a-117">A parte da forma delimitadora da caixa para medir e retornar.</span><span class="sxs-lookup"><span data-stu-id="0732a-117">The part of the shape's bounding box to measure and return.</span></span> <span data-ttu-id="0732a-118">Consulte Comentários para obter os valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="0732a-118">See Remarks for possible values.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="0732a-119">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="0732a-119">Return value</span></span>

 <span data-ttu-id="0732a-120">**Número**</span><span class="sxs-lookup"><span data-stu-id="0732a-120">**Number**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0732a-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="0732a-121">Remarks</span></span>

 <span data-ttu-id="0732a-122">*Index* pode ser um dos seguintes valores.</span><span class="sxs-lookup"><span data-stu-id="0732a-122">*Index*  can be one of the following values.</span></span> 
  
|<span data-ttu-id="0732a-123">**1.1**</span><span class="sxs-lookup"><span data-stu-id="0732a-123">**Item**</span></span>|<span data-ttu-id="0732a-124">**Valor**</span><span class="sxs-lookup"><span data-stu-id="0732a-124">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0732a-125">Largura</span><span class="sxs-lookup"><span data-stu-id="0732a-125">Width</span></span>  <br/> |<span data-ttu-id="0732a-126">0</span><span class="sxs-lookup"><span data-stu-id="0732a-126">0</span></span>  <br/> |
|<span data-ttu-id="0732a-127">Altura</span><span class="sxs-lookup"><span data-stu-id="0732a-127">Height</span></span>  <br/> |<span data-ttu-id="0732a-128">1</span><span class="sxs-lookup"><span data-stu-id="0732a-128">1</span></span>  <br/> |
|<span data-ttu-id="0732a-129">Borda esquerda até o pino da forma</span><span class="sxs-lookup"><span data-stu-id="0732a-129">Left edge to shape pin</span></span>  <br/> |<span data-ttu-id="0732a-130">2</span><span class="sxs-lookup"><span data-stu-id="0732a-130">2</span></span>  <br/> |
|<span data-ttu-id="0732a-131">Pino da forma até a borda direita</span><span class="sxs-lookup"><span data-stu-id="0732a-131">Shape pin to right edge</span></span>  <br/> |<span data-ttu-id="0732a-132">3</span><span class="sxs-lookup"><span data-stu-id="0732a-132">3</span></span>  <br/> |
|<span data-ttu-id="0732a-133">Pino da forma até a borda superior</span><span class="sxs-lookup"><span data-stu-id="0732a-133">Shape pin to top edge</span></span>  <br/> |<span data-ttu-id="0732a-134">4</span><span class="sxs-lookup"><span data-stu-id="0732a-134">4</span></span>  <br/> |
|<span data-ttu-id="0732a-135">Borda inferior até o pino da forma</span><span class="sxs-lookup"><span data-stu-id="0732a-135">Bottom edge to shape pin</span></span>  <br/> |<span data-ttu-id="0732a-136">5</span><span class="sxs-lookup"><span data-stu-id="0732a-136">5</span></span>  <br/> |
|<span data-ttu-id="0732a-137">Centro da caixa delimitadora até PinX</span><span class="sxs-lookup"><span data-stu-id="0732a-137">Center of bounding box to PinX</span></span>  <br/> |<span data-ttu-id="0732a-138">6</span><span class="sxs-lookup"><span data-stu-id="0732a-138">6</span></span>  <br/> |
|<span data-ttu-id="0732a-139">Centro da caixa delimitadora até PinY</span><span class="sxs-lookup"><span data-stu-id="0732a-139">Center of bounding box to PinY</span></span>  <br/> |<span data-ttu-id="0732a-140">7</span><span class="sxs-lookup"><span data-stu-id="0732a-140">7</span></span>  <br/> |
   

