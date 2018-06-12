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
# <a name="boundingboxdist-function"></a><span data-ttu-id="8a0d0-103">Função BOUNDINGBOXDIST</span><span class="sxs-lookup"><span data-stu-id="8a0d0-103">BOUNDINGBOXDIST Function</span></span>

<span data-ttu-id="8a0d0-104">Retorna a medida da parte especificada da caixa delimitadora da forma.</span><span class="sxs-lookup"><span data-stu-id="8a0d0-104">Returns the measurement of the specified part of the shape's bounding box.</span></span> 
  
## <a name="version-information"></a><span data-ttu-id="8a0d0-105">Informações da versão</span><span class="sxs-lookup"><span data-stu-id="8a0d0-105">Version Information</span></span>

<span data-ttu-id="8a0d0-106">Versão adicionada: Visio 2010</span><span class="sxs-lookup"><span data-stu-id="8a0d0-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="8a0d0-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8a0d0-107">Syntax</span></span>

<span data-ttu-id="8a0d0-108">BOUNDINGBOXDIST (* * *índice* * *)</span><span class="sxs-lookup"><span data-stu-id="8a0d0-108">BOUNDINGBOXDIST(** *Index* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="8a0d0-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8a0d0-109">Parameters</span></span>

|<span data-ttu-id="8a0d0-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="8a0d0-110">**Name**</span></span>|<span data-ttu-id="8a0d0-111">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="8a0d0-111">**Required/Optional**</span></span>|<span data-ttu-id="8a0d0-112">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="8a0d0-112">**Data Type**</span></span>|<span data-ttu-id="8a0d0-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="8a0d0-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="8a0d0-114">_Index_</span><span class="sxs-lookup"><span data-stu-id="8a0d0-114">_Index_</span></span> <br/> |<span data-ttu-id="8a0d0-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="8a0d0-115">Required</span></span>  <br/> |<span data-ttu-id="8a0d0-116">**Número**</span><span class="sxs-lookup"><span data-stu-id="8a0d0-116">**Number**</span></span> <br/> |<span data-ttu-id="8a0d0-117">A parte da forma delimitadora da caixa para medir e retornar.</span><span class="sxs-lookup"><span data-stu-id="8a0d0-117">The part of the shape's bounding box to measure and return.</span></span> <span data-ttu-id="8a0d0-118">Consulte Comentários para obter os valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="8a0d0-118">See Remarks for possible values.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="8a0d0-119">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="8a0d0-119">Return value</span></span>

 <span data-ttu-id="8a0d0-120">**Número**</span><span class="sxs-lookup"><span data-stu-id="8a0d0-120">**Number**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8a0d0-121">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="8a0d0-121">Remarks</span></span>

 <span data-ttu-id="8a0d0-122">*Index* pode ser um dos seguintes valores.</span><span class="sxs-lookup"><span data-stu-id="8a0d0-122">*Index*  can be one of the following values.</span></span> 
  
|<span data-ttu-id="8a0d0-123">**1.1**</span><span class="sxs-lookup"><span data-stu-id="8a0d0-123">**Item**</span></span>|<span data-ttu-id="8a0d0-124">**Valor**</span><span class="sxs-lookup"><span data-stu-id="8a0d0-124">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8a0d0-125">Largura</span><span class="sxs-lookup"><span data-stu-id="8a0d0-125">Width</span></span>  <br/> |<span data-ttu-id="8a0d0-126">0</span><span class="sxs-lookup"><span data-stu-id="8a0d0-126">0</span></span>  <br/> |
|<span data-ttu-id="8a0d0-127">Altura</span><span class="sxs-lookup"><span data-stu-id="8a0d0-127">Height</span></span>  <br/> |<span data-ttu-id="8a0d0-128">1</span><span class="sxs-lookup"><span data-stu-id="8a0d0-128">1</span></span>  <br/> |
|<span data-ttu-id="8a0d0-129">Borda esquerda até o pino da forma</span><span class="sxs-lookup"><span data-stu-id="8a0d0-129">Left edge to shape pin</span></span>  <br/> |<span data-ttu-id="8a0d0-130">2</span><span class="sxs-lookup"><span data-stu-id="8a0d0-130">2</span></span>  <br/> |
|<span data-ttu-id="8a0d0-131">Pino da forma até a borda direita</span><span class="sxs-lookup"><span data-stu-id="8a0d0-131">Shape pin to right edge</span></span>  <br/> |<span data-ttu-id="8a0d0-132">3</span><span class="sxs-lookup"><span data-stu-id="8a0d0-132">3</span></span>  <br/> |
|<span data-ttu-id="8a0d0-133">Pino da forma até a borda superior</span><span class="sxs-lookup"><span data-stu-id="8a0d0-133">Shape pin to top edge</span></span>  <br/> |<span data-ttu-id="8a0d0-134">4</span><span class="sxs-lookup"><span data-stu-id="8a0d0-134">4</span></span>  <br/> |
|<span data-ttu-id="8a0d0-135">Borda inferior até o pino da forma</span><span class="sxs-lookup"><span data-stu-id="8a0d0-135">Bottom edge to shape pin</span></span>  <br/> |<span data-ttu-id="8a0d0-136">5</span><span class="sxs-lookup"><span data-stu-id="8a0d0-136">5</span></span>  <br/> |
|<span data-ttu-id="8a0d0-137">Centro da caixa delimitadora até PinX</span><span class="sxs-lookup"><span data-stu-id="8a0d0-137">Center of bounding box to PinX</span></span>  <br/> |<span data-ttu-id="8a0d0-138">6</span><span class="sxs-lookup"><span data-stu-id="8a0d0-138">6</span></span>  <br/> |
|<span data-ttu-id="8a0d0-139">Centro da caixa delimitadora até PinY</span><span class="sxs-lookup"><span data-stu-id="8a0d0-139">Center of bounding box to PinY</span></span>  <br/> |<span data-ttu-id="8a0d0-140">7</span><span class="sxs-lookup"><span data-stu-id="8a0d0-140">7</span></span>  <br/> |
   

