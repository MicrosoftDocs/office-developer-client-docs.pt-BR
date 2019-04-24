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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348962"
---
# <a name="boundingboxdist-function"></a><span data-ttu-id="9443f-103">Função BOUNDINGBOXDIST</span><span class="sxs-lookup"><span data-stu-id="9443f-103">BOUNDINGBOXDIST Function</span></span>

<span data-ttu-id="9443f-104">Retorna a medida da parte especificada da caixa delimitadora da forma.</span><span class="sxs-lookup"><span data-stu-id="9443f-104">Returns the measurement of the specified part of the shape's bounding box.</span></span> 
  
## <a name="version-information"></a><span data-ttu-id="9443f-105">Informações da versão</span><span class="sxs-lookup"><span data-stu-id="9443f-105">Version Information</span></span>

<span data-ttu-id="9443f-106">Version Added: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="9443f-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="9443f-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9443f-107">Syntax</span></span>

<span data-ttu-id="9443f-108">BOUNDINGBOXDIST (\* \* *índice* \* \*)</span><span class="sxs-lookup"><span data-stu-id="9443f-108">BOUNDINGBOXDIST(\*\* *Index* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="9443f-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9443f-109">Parameters</span></span>

|<span data-ttu-id="9443f-110">**Nome**</span><span class="sxs-lookup"><span data-stu-id="9443f-110">**Name**</span></span>|<span data-ttu-id="9443f-111">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="9443f-111">**Required/Optional**</span></span>|<span data-ttu-id="9443f-112">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="9443f-112">**Data Type**</span></span>|<span data-ttu-id="9443f-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="9443f-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="9443f-114">_Index_</span><span class="sxs-lookup"><span data-stu-id="9443f-114">_Index_</span></span> <br/> |<span data-ttu-id="9443f-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="9443f-115">Required</span></span>  <br/> |<span data-ttu-id="9443f-116">**Número**</span><span class="sxs-lookup"><span data-stu-id="9443f-116">**Number**</span></span> <br/> |<span data-ttu-id="9443f-117">A parte da caixa delimitadora da forma para medir e retornar.</span><span class="sxs-lookup"><span data-stu-id="9443f-117">The part of the shape's bounding box to measure and return.</span></span> <span data-ttu-id="9443f-118">Consulte comentários para os valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="9443f-118">See Remarks for possible values.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="9443f-119">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="9443f-119">Return value</span></span>

 <span data-ttu-id="9443f-120">**Número**</span><span class="sxs-lookup"><span data-stu-id="9443f-120">**Number**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9443f-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="9443f-121">Remarks</span></span>

 <span data-ttu-id="9443f-122">*Index* pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="9443f-122">*Index*  can be one of the following values.</span></span> 
  
|<span data-ttu-id="9443f-123">**Item**</span><span class="sxs-lookup"><span data-stu-id="9443f-123">**Item**</span></span>|<span data-ttu-id="9443f-124">**Valor**</span><span class="sxs-lookup"><span data-stu-id="9443f-124">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9443f-125">Largura</span><span class="sxs-lookup"><span data-stu-id="9443f-125">Width</span></span>  <br/> |<span data-ttu-id="9443f-126">,0</span><span class="sxs-lookup"><span data-stu-id="9443f-126">0</span></span>  <br/> |
|<span data-ttu-id="9443f-127">Altura</span><span class="sxs-lookup"><span data-stu-id="9443f-127">Height</span></span>  <br/> |<span data-ttu-id="9443f-128">1</span><span class="sxs-lookup"><span data-stu-id="9443f-128">1</span></span>  <br/> |
|<span data-ttu-id="9443f-129">Borda esquerda até o pino da forma</span><span class="sxs-lookup"><span data-stu-id="9443f-129">Left edge to shape pin</span></span>  <br/> |<span data-ttu-id="9443f-130">duas</span><span class="sxs-lookup"><span data-stu-id="9443f-130">2</span></span>  <br/> |
|<span data-ttu-id="9443f-131">Pino da forma até a borda direita</span><span class="sxs-lookup"><span data-stu-id="9443f-131">Shape pin to right edge</span></span>  <br/> |<span data-ttu-id="9443f-132">3D</span><span class="sxs-lookup"><span data-stu-id="9443f-132">3</span></span>  <br/> |
|<span data-ttu-id="9443f-133">Pino da forma até a borda superior</span><span class="sxs-lookup"><span data-stu-id="9443f-133">Shape pin to top edge</span></span>  <br/> |<span data-ttu-id="9443f-134">quatro</span><span class="sxs-lookup"><span data-stu-id="9443f-134">4</span></span>  <br/> |
|<span data-ttu-id="9443f-135">Borda inferior até o pino da forma</span><span class="sxs-lookup"><span data-stu-id="9443f-135">Bottom edge to shape pin</span></span>  <br/> |<span data-ttu-id="9443f-136">0,5</span><span class="sxs-lookup"><span data-stu-id="9443f-136">5</span></span>  <br/> |
|<span data-ttu-id="9443f-137">Centro da caixa delimitadora até PinX</span><span class="sxs-lookup"><span data-stu-id="9443f-137">Center of bounding box to PinX</span></span>  <br/> |<span data-ttu-id="9443f-138">6</span><span class="sxs-lookup"><span data-stu-id="9443f-138">6</span></span>  <br/> |
|<span data-ttu-id="9443f-139">Centro da caixa delimitadora até PinY</span><span class="sxs-lookup"><span data-stu-id="9443f-139">Center of bounding box to PinY</span></span>  <br/> |<span data-ttu-id="9443f-140">178</span><span class="sxs-lookup"><span data-stu-id="9443f-140">7</span></span>  <br/> |
   

