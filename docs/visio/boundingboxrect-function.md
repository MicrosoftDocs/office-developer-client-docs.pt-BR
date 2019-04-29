---
title: Função BOUNDINGBOXRECT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1f66d2b2-ec9e-cd58-7642-96850fe4589e
description: Retorna a coordenada da borda especificada da caixa delimitadora da forma.
ms.openlocfilehash: 0018118eb0991fe9dc1da0eb000566b69d8a4b4d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418068"
---
# <a name="boundingboxrect-function"></a><span data-ttu-id="dc71a-103">Função BOUNDINGBOXRECT</span><span class="sxs-lookup"><span data-stu-id="dc71a-103">BOUNDINGBOXRECT Function</span></span>

<span data-ttu-id="dc71a-104">Retorna a coordenada da borda especificada da caixa delimitadora da forma.</span><span class="sxs-lookup"><span data-stu-id="dc71a-104">Returns the coordinate of the specified edge of the shape's bounding box.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="dc71a-105">Informações da versão</span><span class="sxs-lookup"><span data-stu-id="dc71a-105">Version Information</span></span>

<span data-ttu-id="dc71a-106">Version Added: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="dc71a-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="dc71a-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dc71a-107">Syntax</span></span>

<span data-ttu-id="dc71a-108">BOUNDINGBOXRECT (\* \* *índice* \* \*)</span><span class="sxs-lookup"><span data-stu-id="dc71a-108">BOUNDINGBOXRECT(\*\* *Index* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="dc71a-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dc71a-109">Parameters</span></span>

|<span data-ttu-id="dc71a-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="dc71a-110">**Name**</span></span>|<span data-ttu-id="dc71a-111">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="dc71a-111">**Required/Optional**</span></span>|<span data-ttu-id="dc71a-112">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="dc71a-112">**Data Type**</span></span>|<span data-ttu-id="dc71a-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="dc71a-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="dc71a-114">_Index_</span><span class="sxs-lookup"><span data-stu-id="dc71a-114">_Index_</span></span> <br/> |<span data-ttu-id="dc71a-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="dc71a-115">Required</span></span>  <br/> |<span data-ttu-id="dc71a-116">**Integer**</span><span class="sxs-lookup"><span data-stu-id="dc71a-116">**Integer**</span></span> <br/> |<span data-ttu-id="dc71a-117">A borda da caixa delimitadora da forma para a qual será obtida a coordenada.</span><span class="sxs-lookup"><span data-stu-id="dc71a-117">The edge of the shape's bounding box for which to get the coordinate.</span></span> <span data-ttu-id="dc71a-118">Consulte Comentários para obter os valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="dc71a-118">See Remarks for possible values.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="dc71a-119">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="dc71a-119">Return value</span></span>

 <span data-ttu-id="dc71a-120">**Número**</span><span class="sxs-lookup"><span data-stu-id="dc71a-120">**Number**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="dc71a-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="dc71a-121">Remarks</span></span>

 <span data-ttu-id="dc71a-122">*Index* pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="dc71a-122">*Index*  can be one of the following values.</span></span> 
  
|<span data-ttu-id="dc71a-123">**Item**</span><span class="sxs-lookup"><span data-stu-id="dc71a-123">**Item**</span></span>|<span data-ttu-id="dc71a-124">**Valor**</span><span class="sxs-lookup"><span data-stu-id="dc71a-124">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="dc71a-125">Borda esquerda</span><span class="sxs-lookup"><span data-stu-id="dc71a-125">Left edge</span></span>  <br/> |<span data-ttu-id="dc71a-126">,0</span><span class="sxs-lookup"><span data-stu-id="dc71a-126">0</span></span>  <br/> |
|<span data-ttu-id="dc71a-127">Borda direita</span><span class="sxs-lookup"><span data-stu-id="dc71a-127">Right edge</span></span>  <br/> |<span data-ttu-id="dc71a-128">1</span><span class="sxs-lookup"><span data-stu-id="dc71a-128">1</span></span>  <br/> |
|<span data-ttu-id="dc71a-129">Borda superior</span><span class="sxs-lookup"><span data-stu-id="dc71a-129">Top edge</span></span>  <br/> |<span data-ttu-id="dc71a-130">duas</span><span class="sxs-lookup"><span data-stu-id="dc71a-130">2</span></span>  <br/> |
|<span data-ttu-id="dc71a-131">Borda inferior</span><span class="sxs-lookup"><span data-stu-id="dc71a-131">Bottom edge</span></span>  <br/> |<span data-ttu-id="dc71a-132">3D</span><span class="sxs-lookup"><span data-stu-id="dc71a-132">3</span></span>  <br/> |
   
<span data-ttu-id="dc71a-133">Se a forma tiver um pai, o valor de retorno estará no sistema de coordenadas desse pai.</span><span class="sxs-lookup"><span data-stu-id="dc71a-133">If the shape has a parent, the return value is in the coordinate system of that parent.</span></span>
  

