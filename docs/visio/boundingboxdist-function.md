---
title: Função BOUNDINGBOXDIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8a2490f2-48c4-5df3-a3b3-40e8e0c80479
description: Retorna a medida da parte especificada da caixa delimitadora da forma.
ms.openlocfilehash: a62d5b82c310e7b99e16b70982b75a68172b7fd8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428274"
---
# <a name="boundingboxdist-function"></a><span data-ttu-id="a15ac-103">Função BOUNDINGBOXDIST</span><span class="sxs-lookup"><span data-stu-id="a15ac-103">BOUNDINGBOXDIST Function</span></span>

<span data-ttu-id="a15ac-104">Retorna a medida da parte especificada da caixa delimitadora da forma.</span><span class="sxs-lookup"><span data-stu-id="a15ac-104">Returns the measurement of the specified part of the shape's bounding box.</span></span> 
  
## <a name="version-information"></a><span data-ttu-id="a15ac-105">Informações da versão</span><span class="sxs-lookup"><span data-stu-id="a15ac-105">Version Information</span></span>

<span data-ttu-id="a15ac-106">Version Added: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="a15ac-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="a15ac-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a15ac-107">Syntax</span></span>

<span data-ttu-id="a15ac-108">BOUNDINGBOXDIST(\*\* *Index* \*\* )</span><span class="sxs-lookup"><span data-stu-id="a15ac-108">BOUNDINGBOXDIST(\*\* *Index* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="a15ac-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a15ac-109">Parameters</span></span>

|<span data-ttu-id="a15ac-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="a15ac-110">**Name**</span></span>|<span data-ttu-id="a15ac-111">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="a15ac-111">**Required/Optional**</span></span>|<span data-ttu-id="a15ac-112">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="a15ac-112">**Data Type**</span></span>|<span data-ttu-id="a15ac-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="a15ac-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="a15ac-114">_Index_</span><span class="sxs-lookup"><span data-stu-id="a15ac-114">_Index_</span></span> <br/> |<span data-ttu-id="a15ac-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="a15ac-115">Required</span></span>  <br/> |<span data-ttu-id="a15ac-116">**Número**</span><span class="sxs-lookup"><span data-stu-id="a15ac-116">**Number**</span></span> <br/> |<span data-ttu-id="a15ac-117">A parte da caixa delimitativa da forma a ser medida e retornada.</span><span class="sxs-lookup"><span data-stu-id="a15ac-117">The part of the shape's bounding box to measure and return.</span></span> <span data-ttu-id="a15ac-118">Consulte comentários para os valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="a15ac-118">See Remarks for possible values.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="a15ac-119">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="a15ac-119">Return value</span></span>

 <span data-ttu-id="a15ac-120">**Número**</span><span class="sxs-lookup"><span data-stu-id="a15ac-120">**Number**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a15ac-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="a15ac-121">Remarks</span></span>

 <span data-ttu-id="a15ac-122">*Index*  pode ser um dos seguintes valores.</span><span class="sxs-lookup"><span data-stu-id="a15ac-122">*Index*  can be one of the following values.</span></span> 
  
|<span data-ttu-id="a15ac-123">**Item**</span><span class="sxs-lookup"><span data-stu-id="a15ac-123">**Item**</span></span>|<span data-ttu-id="a15ac-124">**Valor**</span><span class="sxs-lookup"><span data-stu-id="a15ac-124">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a15ac-125">Largura</span><span class="sxs-lookup"><span data-stu-id="a15ac-125">Width</span></span>  <br/> |<span data-ttu-id="a15ac-126">0</span><span class="sxs-lookup"><span data-stu-id="a15ac-126">0</span></span>  <br/> |
|<span data-ttu-id="a15ac-127">Altura</span><span class="sxs-lookup"><span data-stu-id="a15ac-127">Height</span></span>  <br/> |<span data-ttu-id="a15ac-128">1 </span><span class="sxs-lookup"><span data-stu-id="a15ac-128">1</span></span>  <br/> |
|<span data-ttu-id="a15ac-129">Borda esquerda até o pino da forma</span><span class="sxs-lookup"><span data-stu-id="a15ac-129">Left edge to shape pin</span></span>  <br/> |<span data-ttu-id="a15ac-130">2 </span><span class="sxs-lookup"><span data-stu-id="a15ac-130">2</span></span>  <br/> |
|<span data-ttu-id="a15ac-131">Pino da forma até a borda direita</span><span class="sxs-lookup"><span data-stu-id="a15ac-131">Shape pin to right edge</span></span>  <br/> |<span data-ttu-id="a15ac-132">3 </span><span class="sxs-lookup"><span data-stu-id="a15ac-132">3</span></span>  <br/> |
|<span data-ttu-id="a15ac-133">Pino da forma até a borda superior</span><span class="sxs-lookup"><span data-stu-id="a15ac-133">Shape pin to top edge</span></span>  <br/> |<span data-ttu-id="a15ac-134">4 </span><span class="sxs-lookup"><span data-stu-id="a15ac-134">4</span></span>  <br/> |
|<span data-ttu-id="a15ac-135">Borda inferior até o pino da forma</span><span class="sxs-lookup"><span data-stu-id="a15ac-135">Bottom edge to shape pin</span></span>  <br/> |<span data-ttu-id="a15ac-136">5 </span><span class="sxs-lookup"><span data-stu-id="a15ac-136">5</span></span>  <br/> |
|<span data-ttu-id="a15ac-137">Centro da caixa delimitadora até PinX</span><span class="sxs-lookup"><span data-stu-id="a15ac-137">Center of bounding box to PinX</span></span>  <br/> |<span data-ttu-id="a15ac-138">6 </span><span class="sxs-lookup"><span data-stu-id="a15ac-138">6</span></span>  <br/> |
|<span data-ttu-id="a15ac-139">Centro da caixa delimitadora até PinY</span><span class="sxs-lookup"><span data-stu-id="a15ac-139">Center of bounding box to PinY</span></span>  <br/> |<span data-ttu-id="a15ac-140">7 </span><span class="sxs-lookup"><span data-stu-id="a15ac-140">7</span></span>  <br/> |
   

