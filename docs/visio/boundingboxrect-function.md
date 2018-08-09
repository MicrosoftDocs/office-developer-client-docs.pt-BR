---
title: Função BOUNDINGBOXRECT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1f66d2b2-ec9e-cd58-7642-96850fe4589e
description: Retorna a coordenada da borda especificada da caixa delimitadora da forma.
ms.openlocfilehash: 2c850cb213ec0093ead53cd860f92e38da46f27e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771420"
---
# <a name="boundingboxrect-function"></a><span data-ttu-id="5b353-103">Função BOUNDINGBOXRECT</span><span class="sxs-lookup"><span data-stu-id="5b353-103">BOUNDINGBOXRECT Function</span></span>

<span data-ttu-id="5b353-104">Retorna a coordenada da borda especificada da caixa delimitadora da forma.</span><span class="sxs-lookup"><span data-stu-id="5b353-104">Returns the coordinate of the specified edge of the shape's bounding box.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="5b353-105">Informações da versão</span><span class="sxs-lookup"><span data-stu-id="5b353-105">Version Information</span></span>

<span data-ttu-id="5b353-106">Version Added: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="5b353-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="5b353-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5b353-107">Syntax</span></span>

<span data-ttu-id="5b353-108">BOUNDINGBOXRECT (* * *índice* * *)</span><span class="sxs-lookup"><span data-stu-id="5b353-108">BOUNDINGBOXRECT(** *Index* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="5b353-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5b353-109">Parameters</span></span>

|<span data-ttu-id="5b353-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="5b353-110">**Name**</span></span>|<span data-ttu-id="5b353-111">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="5b353-111">**Required/Optional**</span></span>|<span data-ttu-id="5b353-112">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="5b353-112">**Data Type**</span></span>|<span data-ttu-id="5b353-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="5b353-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="5b353-114">_Index_</span><span class="sxs-lookup"><span data-stu-id="5b353-114">_Index_</span></span> <br/> |<span data-ttu-id="5b353-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="5b353-115">Required</span></span>  <br/> |<span data-ttu-id="5b353-116">**Integer**</span><span class="sxs-lookup"><span data-stu-id="5b353-116">**Integer**</span></span> <br/> |<span data-ttu-id="5b353-p101">A borda da caixa delimitadora da forma para a qual será obtida a coordenada. Consulte Comentários para obter os valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="5b353-p101">The edge of the shape's bounding box for which to get the coordinate. See Remarks for possible values.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="5b353-119">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="5b353-119">Return value</span></span>

 <span data-ttu-id="5b353-120">**Número**</span><span class="sxs-lookup"><span data-stu-id="5b353-120">**Number**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5b353-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="5b353-121">Remarks</span></span>

 <span data-ttu-id="5b353-122">*Index* pode ser um dos seguintes valores.</span><span class="sxs-lookup"><span data-stu-id="5b353-122">*Index*  can be one of the following values.</span></span> 
  
|<span data-ttu-id="5b353-123">**1.1**</span><span class="sxs-lookup"><span data-stu-id="5b353-123">**Item**</span></span>|<span data-ttu-id="5b353-124">**Valor**</span><span class="sxs-lookup"><span data-stu-id="5b353-124">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5b353-125">Borda esquerda</span><span class="sxs-lookup"><span data-stu-id="5b353-125">Left edge</span></span>  <br/> |<span data-ttu-id="5b353-126">0</span><span class="sxs-lookup"><span data-stu-id="5b353-126">0</span></span>  <br/> |
|<span data-ttu-id="5b353-127">Borda direita</span><span class="sxs-lookup"><span data-stu-id="5b353-127">Right edge</span></span>  <br/> |<span data-ttu-id="5b353-128">1</span><span class="sxs-lookup"><span data-stu-id="5b353-128">1</span></span>  <br/> |
|<span data-ttu-id="5b353-129">Borda superior</span><span class="sxs-lookup"><span data-stu-id="5b353-129">Top edge</span></span>  <br/> |<span data-ttu-id="5b353-130">2</span><span class="sxs-lookup"><span data-stu-id="5b353-130">2</span></span>  <br/> |
|<span data-ttu-id="5b353-131">Borda inferior</span><span class="sxs-lookup"><span data-stu-id="5b353-131">Bottom edge</span></span>  <br/> |<span data-ttu-id="5b353-132">3</span><span class="sxs-lookup"><span data-stu-id="5b353-132">3</span></span>  <br/> |
   
<span data-ttu-id="5b353-133">Se a forma tiver um pai, o valor de retorno é no sistema de coordenadas desse pai.</span><span class="sxs-lookup"><span data-stu-id="5b353-133">If the shape has a parent, the return value is in the coordinate system of that parent.</span></span>
  

