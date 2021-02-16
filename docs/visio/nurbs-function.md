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
description: Retorna uma B-spline racional não uniforme (NURBS). Esta função é usada na célula E nas linhas de geometria NURBSTo.
ms.openlocfilehash: af92374a829c0df8e71ac81e630abc4fa64988dc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438453"
---
# <a name="nurbs-function"></a><span data-ttu-id="3aec4-104">Função NURBS</span><span class="sxs-lookup"><span data-stu-id="3aec4-104">NURBS Function</span></span>

<span data-ttu-id="3aec4-105">Retorna uma B-spline racional não uniforme (NURBS).</span><span class="sxs-lookup"><span data-stu-id="3aec4-105">Returns a nonuniform rational B-spline (NURBS).</span></span> <span data-ttu-id="3aec4-106">Esta função é usada na célula E nas linhas de geometria NURBSTo.</span><span class="sxs-lookup"><span data-stu-id="3aec4-106">This function is used in the E cell in the NURBSTo geometry rows.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="3aec4-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3aec4-107">Syntax</span></span>

<span data-ttu-id="3aec4-108">NURBS(\*\* *knotLast* \*\*, \*\* *degree* \*\*, \*\* *xType* \*\*, \*\* *yType* \*\*, \*\* *x1* \*\*, \*\* *y1* \*\*, \*\* *knot1* \*\*, \*\* *weight1* \*\*, ...)</span><span class="sxs-lookup"><span data-stu-id="3aec4-108">NURBS(\*\* *knotLast* \*\*, \*\* *degree* \*\*, \*\* *xType* \*\*, \*\* *yType* \*\*, \*\* *x1* \*\*, \*\* *y1* \*\*, \*\* *knot1* \*\*, \*\* *weight1* \*\*, ...)</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="3aec4-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3aec4-109">Parameters</span></span>

|<span data-ttu-id="3aec4-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="3aec4-110">**Name**</span></span>|<span data-ttu-id="3aec4-111">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="3aec4-111">**Required/Optional**</span></span>|<span data-ttu-id="3aec4-112">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="3aec4-112">**Data Type**</span></span>|<span data-ttu-id="3aec4-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="3aec4-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="3aec4-114">_knotLast_</span><span class="sxs-lookup"><span data-stu-id="3aec4-114">_knotLast_</span></span> <br/> |<span data-ttu-id="3aec4-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="3aec4-115">Required</span></span>  <br/> |<span data-ttu-id="3aec4-116">**cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3aec4-116">**string**</span></span> <br/> | <span data-ttu-id="3aec4-117">O último nó.</span><span class="sxs-lookup"><span data-stu-id="3aec4-117">The last knot.</span></span>  <br/> |
| <span data-ttu-id="3aec4-118">_degree_</span><span class="sxs-lookup"><span data-stu-id="3aec4-118">_degree_</span></span> <br/> |<span data-ttu-id="3aec4-119">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="3aec4-119">Required</span></span>  <br/> |<span data-ttu-id="3aec4-120">**Numérica**</span><span class="sxs-lookup"><span data-stu-id="3aec4-120">**Numeric**</span></span> <br/> |<span data-ttu-id="3aec4-121">O grau da spline.</span><span class="sxs-lookup"><span data-stu-id="3aec4-121">The spline's degree.</span></span>  <br/> |
| <span data-ttu-id="3aec4-122">_xType_</span><span class="sxs-lookup"><span data-stu-id="3aec4-122">_xType_</span></span> <br/> |<span data-ttu-id="3aec4-123">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="3aec4-123">Required</span></span>  <br/> |<span data-ttu-id="3aec4-124">**Numérica**</span><span class="sxs-lookup"><span data-stu-id="3aec4-124">**Numeric**</span></span> <br/> |<span data-ttu-id="3aec4-125">Especifica como interpretar os dados _de entrada x._</span><span class="sxs-lookup"><span data-stu-id="3aec4-125">Specifies how to interpret the  _x_ input data.</span></span> <span data-ttu-id="3aec4-126">Se  _xType_ for 0, todos  _os dados de entrada x_ serão interpretados como uma porcentagem de Width.</span><span class="sxs-lookup"><span data-stu-id="3aec4-126">If  _xType_ is 0, all  _x_ input data is interpreted as a percentage of Width.</span></span> <span data-ttu-id="3aec4-127">Se  _xType_ for 1, todos  _os dados de entrada x_ serão interpretados como coordenadas locais.</span><span class="sxs-lookup"><span data-stu-id="3aec4-127">If  _xType_ is 1, all  _x_ input data is interpreted as local coordinates.</span></span>  <br/> |
| <span data-ttu-id="3aec4-128">_yType_</span><span class="sxs-lookup"><span data-stu-id="3aec4-128">_yType_</span></span> <br/> |<span data-ttu-id="3aec4-129">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="3aec4-129">Required</span></span>  <br/> |<span data-ttu-id="3aec4-130">**Numérica**</span><span class="sxs-lookup"><span data-stu-id="3aec4-130">**Numeric**</span></span> <br/> |<span data-ttu-id="3aec4-131">Especifica como interpretar os dados _de entrada y._</span><span class="sxs-lookup"><span data-stu-id="3aec4-131">Specifies how to interpret the  _y_ input data.</span></span> <span data-ttu-id="3aec4-132">Se  _yType_ for 0, todos os  _dados de_ entrada y serão interpretados como uma porcentagem de Altura.</span><span class="sxs-lookup"><span data-stu-id="3aec4-132">If  _yType_ is 0, all  _y_ input data is interpreted as a percentage of Height.</span></span> <span data-ttu-id="3aec4-133">Se  _yType_ for 1, todos os  _dados de_ entrada y serão interpretados como coordenadas locais.</span><span class="sxs-lookup"><span data-stu-id="3aec4-133">If  _yType_ is 1, all  _y_ input data is interpreted as local coordinates.</span></span>  <br/> |
| <span data-ttu-id="3aec4-134">_x1_</span><span class="sxs-lookup"><span data-stu-id="3aec4-134">_x1_</span></span> <br/> |<span data-ttu-id="3aec4-135">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="3aec4-135">Required</span></span>  <br/> |<span data-ttu-id="3aec4-136">**String**</span><span class="sxs-lookup"><span data-stu-id="3aec4-136">**String**</span></span> <br/> |<span data-ttu-id="3aec4-137">Uma coordenada x.</span><span class="sxs-lookup"><span data-stu-id="3aec4-137">An x-coordinate.</span></span>  <br/> |
| <span data-ttu-id="3aec4-138">_y1_</span><span class="sxs-lookup"><span data-stu-id="3aec4-138">_y1_</span></span> <br/> |<span data-ttu-id="3aec4-139">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="3aec4-139">Required</span></span>  <br/> |<span data-ttu-id="3aec4-140">**String**</span><span class="sxs-lookup"><span data-stu-id="3aec4-140">**String**</span></span> <br/> |<span data-ttu-id="3aec4-141">Uma coordenada y.</span><span class="sxs-lookup"><span data-stu-id="3aec4-141">A y-coordinate.</span></span>  <br/> |
| <span data-ttu-id="3aec4-142">_knot1_</span><span class="sxs-lookup"><span data-stu-id="3aec4-142">_knot1_</span></span> <br/> |<span data-ttu-id="3aec4-143">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="3aec4-143">Required</span></span>  <br/> |<span data-ttu-id="3aec4-144">**String**</span><span class="sxs-lookup"><span data-stu-id="3aec4-144">**String**</span></span> <br/> |<span data-ttu-id="3aec4-145">Um nó na B-spline.</span><span class="sxs-lookup"><span data-stu-id="3aec4-145">A knot on the B-spline.</span></span>  <br/> |
| <span data-ttu-id="3aec4-146">_weight1_</span><span class="sxs-lookup"><span data-stu-id="3aec4-146">_weight1_</span></span> <br/> |<span data-ttu-id="3aec4-147">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="3aec4-147">Required</span></span>  <br/> |<span data-ttu-id="3aec4-148">**String**</span><span class="sxs-lookup"><span data-stu-id="3aec4-148">**String**</span></span> <br/> |<span data-ttu-id="3aec4-149">Uma espessura na B-spline.</span><span class="sxs-lookup"><span data-stu-id="3aec4-149">A weight on the B-spline.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3aec4-150">Comentários</span><span class="sxs-lookup"><span data-stu-id="3aec4-150">Remarks</span></span>

<span data-ttu-id="3aec4-151">Para cada  *argumento x,*  deve haver um  *argumento y;*  caso contrário, um erro será retornado.</span><span class="sxs-lookup"><span data-stu-id="3aec4-151">For every  *x*  argument, there must be a  *y*  argument; otherwise, an error is returned.</span></span> 
  
<span data-ttu-id="3aec4-152">Você deve especificar pelo menos um  *argumento x*, *y*, *nó*  *e*  peso; caso contrário, o Visio retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="3aec4-152">You must specify at least one  *x*, *y*, *knot*  , and  *weight*  argument; otherwise, Visio returns an error.</span></span> 
  

