---
title: Função NURBS
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251579
localization_priority: Normal
ms.assetid: f34db20d-6501-2026-a5e8-29c4d4cb2405
description: Retorna uma B-spline racional não-uniforme (NURBS). Essa função é usada na célula E nas linhas geométricas NURBSTo.
ms.openlocfilehash: 005a66b9da2425beaf416ec2273c10446c183add
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/15/2018
ms.locfileid: "19772457"
---
# <a name="nurbs-function"></a><span data-ttu-id="51bc9-104">Função NURBS</span><span class="sxs-lookup"><span data-stu-id="51bc9-104">NURBS Function</span></span>

<span data-ttu-id="51bc9-105">Retorna uma B-spline racional não-uniforme (NURBS).</span><span class="sxs-lookup"><span data-stu-id="51bc9-105">Returns a nonuniform rational B-spline (NURBS).</span></span> <span data-ttu-id="51bc9-106">Essa função é usada na célula E nas linhas geométricas NURBSTo.</span><span class="sxs-lookup"><span data-stu-id="51bc9-106">This function is used in the E cell in the NURBSTo geometry rows.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="51bc9-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="51bc9-107">Syntax</span></span>

<span data-ttu-id="51bc9-108">NURBS (* * *knotLast* * *, * * *grau* * *, * * *tipoX* * *, * * *tipoY* * *, * * *x1* * *, * * *y1* * *, * * *knot1* * *, * * *weight1* * *,...)</span><span class="sxs-lookup"><span data-stu-id="51bc9-108">NURBS(** *knotLast* **, ** *degree* **, ** *xType* **, ** *yType* **, ** *x1* **, ** *y1* **, ** *knot1* **, ** *weight1* **, ...)</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="51bc9-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="51bc9-109">Parameters</span></span>

|<span data-ttu-id="51bc9-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="51bc9-110">**Name**</span></span>|<span data-ttu-id="51bc9-111">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="51bc9-111">**Required/Optional**</span></span>|<span data-ttu-id="51bc9-112">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="51bc9-112">**Data Type**</span></span>|<span data-ttu-id="51bc9-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="51bc9-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="51bc9-114">_knotLast_</span><span class="sxs-lookup"><span data-stu-id="51bc9-114">_knotLast_</span></span> <br/> |<span data-ttu-id="51bc9-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="51bc9-115">Required</span></span>  <br/> |<span data-ttu-id="51bc9-116">**cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="51bc9-116">**string**</span></span> <br/> | <span data-ttu-id="51bc9-117">O último nó.</span><span class="sxs-lookup"><span data-stu-id="51bc9-117">The last knot.</span></span>  <br/> |
| <span data-ttu-id="51bc9-118">_grau_</span><span class="sxs-lookup"><span data-stu-id="51bc9-118">_degree_</span></span> <br/> |<span data-ttu-id="51bc9-119">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="51bc9-119">Required</span></span>  <br/> |<span data-ttu-id="51bc9-120">**Numérico**</span><span class="sxs-lookup"><span data-stu-id="51bc9-120">**Numeric**</span></span> <br/> |<span data-ttu-id="51bc9-121">O grau da spline.</span><span class="sxs-lookup"><span data-stu-id="51bc9-121">The spline's degree.</span></span>  <br/> |
| <span data-ttu-id="51bc9-122">_tipoX_</span><span class="sxs-lookup"><span data-stu-id="51bc9-122">_xType_</span></span> <br/> |<span data-ttu-id="51bc9-123">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="51bc9-123">Required</span></span>  <br/> |<span data-ttu-id="51bc9-124">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="51bc9-124">**Numeric**</span></span> <br/> |<span data-ttu-id="51bc9-125">Especifica como interpretar os dados de entrada de _x_ .</span><span class="sxs-lookup"><span data-stu-id="51bc9-125">Specifies how to interpret the  _x_ input data.</span></span> <span data-ttu-id="51bc9-126">Se _tipoX_ for 0, todos os dados de entrada _x_ será interpretada como uma porcentagem da largura.</span><span class="sxs-lookup"><span data-stu-id="51bc9-126">If  _xType_ is 0, all  _x_ input data is interpreted as a percentage of Width.</span></span> <span data-ttu-id="51bc9-127">Se _tipoX_ for 1, todos os dados de entrada _x_ será interpretada como coordenadas locais.</span><span class="sxs-lookup"><span data-stu-id="51bc9-127">If  _xType_ is 1, all  _x_ input data is interpreted as local coordinates.</span></span>  <br/> |
| <span data-ttu-id="51bc9-128">_tipoY_</span><span class="sxs-lookup"><span data-stu-id="51bc9-128">_yType_</span></span> <br/> |<span data-ttu-id="51bc9-129">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="51bc9-129">Required</span></span>  <br/> |<span data-ttu-id="51bc9-130">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="51bc9-130">**Numeric**</span></span> <br/> |<span data-ttu-id="51bc9-131">Especifica como interpretar os dados de entrada _y_ .</span><span class="sxs-lookup"><span data-stu-id="51bc9-131">Specifies how to interpret the  _y_ input data.</span></span> <span data-ttu-id="51bc9-132">Se _tipoY_ for 0, todos os dados de entrada _y_ será interpretada como uma porcentagem da altura.</span><span class="sxs-lookup"><span data-stu-id="51bc9-132">If  _yType_ is 0, all  _y_ input data is interpreted as a percentage of Height.</span></span> <span data-ttu-id="51bc9-133">Se _tipoY_ for 1, todos os dados de entrada _y_ será interpretada como coordenadas locais.</span><span class="sxs-lookup"><span data-stu-id="51bc9-133">If  _yType_ is 1, all  _y_ input data is interpreted as local coordinates.</span></span>  <br/> |
| <span data-ttu-id="51bc9-134">_x1_</span><span class="sxs-lookup"><span data-stu-id="51bc9-134">_x1_</span></span> <br/> |<span data-ttu-id="51bc9-135">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="51bc9-135">Required</span></span>  <br/> |<span data-ttu-id="51bc9-136">**String**</span><span class="sxs-lookup"><span data-stu-id="51bc9-136">**String**</span></span> <br/> |<span data-ttu-id="51bc9-137">Uma coordenada x.</span><span class="sxs-lookup"><span data-stu-id="51bc9-137">An x-coordinate.</span></span>  <br/> |
| <span data-ttu-id="51bc9-138">_Y1_</span><span class="sxs-lookup"><span data-stu-id="51bc9-138">_y1_</span></span> <br/> |<span data-ttu-id="51bc9-139">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="51bc9-139">Required</span></span>  <br/> |<span data-ttu-id="51bc9-140">**String**</span><span class="sxs-lookup"><span data-stu-id="51bc9-140">**String**</span></span> <br/> |<span data-ttu-id="51bc9-141">Uma coordenada y.</span><span class="sxs-lookup"><span data-stu-id="51bc9-141">A y-coordinate.</span></span>  <br/> |
| <span data-ttu-id="51bc9-142">_knot1_</span><span class="sxs-lookup"><span data-stu-id="51bc9-142">_knot1_</span></span> <br/> |<span data-ttu-id="51bc9-143">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="51bc9-143">Required</span></span>  <br/> |<span data-ttu-id="51bc9-144">**String**</span><span class="sxs-lookup"><span data-stu-id="51bc9-144">**String**</span></span> <br/> |<span data-ttu-id="51bc9-145">Um nó na B-spline.</span><span class="sxs-lookup"><span data-stu-id="51bc9-145">A knot on the B-spline.</span></span>  <br/> |
| <span data-ttu-id="51bc9-146">_weight1_</span><span class="sxs-lookup"><span data-stu-id="51bc9-146">_weight1_</span></span> <br/> |<span data-ttu-id="51bc9-147">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="51bc9-147">Required</span></span>  <br/> |<span data-ttu-id="51bc9-148">**String**</span><span class="sxs-lookup"><span data-stu-id="51bc9-148">**String**</span></span> <br/> |<span data-ttu-id="51bc9-149">Uma espessura na B-spline.</span><span class="sxs-lookup"><span data-stu-id="51bc9-149">A weight on the B-spline.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="51bc9-150">Comentários</span><span class="sxs-lookup"><span data-stu-id="51bc9-150">Remarks</span></span>

<span data-ttu-id="51bc9-151">Para cada argumento *x* , deve haver um argumento *y* ; Caso contrário, um erro será retornado.</span><span class="sxs-lookup"><span data-stu-id="51bc9-151">For every  *x*  argument, there must be a  *y*  argument; otherwise, an error is returned.</span></span> 
  
<span data-ttu-id="51bc9-152">Você deve especificar pelo menos um *x*, *y*, *nó* e *espessura* argumento; Caso contrário, o Visio retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="51bc9-152">You must specify at least one  *x*, *y*, *knot*  , and  *weight*  argument; otherwise, Visio returns an error.</span></span> 
  

