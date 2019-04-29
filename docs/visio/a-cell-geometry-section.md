---
title: Célula A (Seção Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm51215
localization_priority: Normal
ms.assetid: 6853df0f-d22e-89ca-7d34-342b9c0bea23
description: Representa informações diferentes em linhas diferentes. Esta tabela descreve a célula A com base na linha na qual está localizada.
ms.openlocfilehash: 42f346b06cad827cfe56fc113a8387d1a31a6867
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432916"
---
# <a name="a-cell-geometry-section"></a><span data-ttu-id="b3470-104">Célula A (Seção Geometry)</span><span class="sxs-lookup"><span data-stu-id="b3470-104">A Cell (Geometry Section)</span></span>

<span data-ttu-id="b3470-105">Representa informações diferentes em linhas diferentes.</span><span class="sxs-lookup"><span data-stu-id="b3470-105">Represents different information in different rows.</span></span> <span data-ttu-id="b3470-106">Esta tabela descreve a célula A com base na linha na qual está localizada.</span><span class="sxs-lookup"><span data-stu-id="b3470-106">This table describes the A cell based on the row in which it's located.</span></span>
  
|<span data-ttu-id="b3470-107">**Row**</span><span class="sxs-lookup"><span data-stu-id="b3470-107">**Row**</span></span>|<span data-ttu-id="b3470-108">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="b3470-108">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b3470-109">ArcTo</span><span class="sxs-lookup"><span data-stu-id="b3470-109">ArcTo</span></span>](arcto-row-geometry-section.md) <br/> | <span data-ttu-id="b3470-110">A distância do ponto médio de um arco até o ponto médio de sua corda.</span><span class="sxs-lookup"><span data-stu-id="b3470-110">The distance from the arc's midpoint to the midpoint of its chord.</span></span>  <br/> |
|[<span data-ttu-id="b3470-111">EllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="b3470-111">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> | <span data-ttu-id="b3470-112">A coordenada *x* do ponto de controle do arco, um ponto no arco. O ponto de controle é melhor localizado sobre a metade entre os vértices inicial e final do arco. Caso contrário, o arco pode chegar a um tamanho extremo para passar pelo ponto de controle, com resultados imprevisíveis.</span><span class="sxs-lookup"><span data-stu-id="b3470-112">The  *x*  -coordinate of the arc's control point, a point on the arc. The control point is best located about halfway between the beginning and ending vertices of the arc. Otherwise, the arc may grow to an extreme size in order to pass through the control point, with unpredictable results.</span></span>  <br/> |
|[<span data-ttu-id="b3470-113">PolylineTo</span><span class="sxs-lookup"><span data-stu-id="b3470-113">PolylineTo</span></span>](polylineto-row-geometry-section.md) <br/> | <span data-ttu-id="b3470-114">A fórmula da polilinha.</span><span class="sxs-lookup"><span data-stu-id="b3470-114">The polyline formula.</span></span>  <br/> |
|[<span data-ttu-id="b3470-115">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="b3470-115">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> | <span data-ttu-id="b3470-116">O penúltimo nó da B-spline racional não-uniforme (NURBS).</span><span class="sxs-lookup"><span data-stu-id="b3470-116">The second to the last knot of the nonuniform rational B-spline (NURBS).</span></span>  <br/> |
|[<span data-ttu-id="b3470-117">SplineStart</span><span class="sxs-lookup"><span data-stu-id="b3470-117">SplineStart</span></span>](splinestart-row-geometry-section.md) <br/> | <span data-ttu-id="b3470-118">O segundo nó da spline.</span><span class="sxs-lookup"><span data-stu-id="b3470-118">The second knot of the spline.</span></span>  <br/> |
|[<span data-ttu-id="b3470-119">SplineKnot</span><span class="sxs-lookup"><span data-stu-id="b3470-119">SplineKnot</span></span>](splineknot-row-geometry-section.md) <br/> | <span data-ttu-id="b3470-120">Um dos nós da spline (exceto o último ou os dois primeiros).</span><span class="sxs-lookup"><span data-stu-id="b3470-120">One of the spline's knots (other than the last one or the first two).</span></span>  <br/> |
|[<span data-ttu-id="b3470-121">InfiniteLine</span><span class="sxs-lookup"><span data-stu-id="b3470-121">InfiniteLine</span></span>](infiniteline-row-geometry-section.md) <br/> | <span data-ttu-id="b3470-122">Uma coordenada *x* de um ponto na linha infinita; emparelhado com a coordenada *y* representada pela célula [B](b-cell-geometry-section.md) .</span><span class="sxs-lookup"><span data-stu-id="b3470-122">An  *x*  -coordinate of a point on the infinite line; paired with  *y*  -coordinate represented by the [B](b-cell-geometry-section.md) cell.</span></span>  <br/> |
|[<span data-ttu-id="b3470-123">Elipse</span><span class="sxs-lookup"><span data-stu-id="b3470-123">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> | <span data-ttu-id="b3470-124">Uma coordenada *x* de um ponto na elipse; emparelhado com a coordenada *y* representada pela célula [B](b-cell-geometry-section.md) .</span><span class="sxs-lookup"><span data-stu-id="b3470-124">An  *x*  -coordinate of a point on the ellipse; paired with  *y*  -coordinate represented by the [B](b-cell-geometry-section.md) cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b3470-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="b3470-125">Remarks</span></span>

<span data-ttu-id="b3470-126">Para fazer referência à célula A pelo nome, a partir de outra fórmula ou programa, usando a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="b3470-126">To get a reference to the A cell by name from another formula, or from a program, using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b3470-127">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="b3470-127">Cell name:</span></span>  <br/> | <span data-ttu-id="b3470-128">Geometry *i* . A *j* onde *i* e *j* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="b3470-128">Geometry  *i*  .A  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
|| <span data-ttu-id="b3470-129">Geometry *i* . A1 (linhas InfiniteLine e Ellipse) onde *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="b3470-129">Geometry  *i*  .A1 (InfiniteLine and Ellipse rows)            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="b3470-130">Para fazer referência à célula A pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="b3470-130">To get a reference to the A cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b3470-131">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="b3470-131">Section index:</span></span>  <br/> |<span data-ttu-id="b3470-132">**visSectionFirstComponent** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="b3470-132">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="b3470-133">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="b3470-133">Row index:</span></span>  <br/> |<span data-ttu-id="b3470-134">**visRowVertex** +  *j* onde *j* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="b3470-134">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
||<span data-ttu-id="b3470-135">\*\*visRowVertex \*\*(linhas Ellipse e InfiniteLine)</span><span class="sxs-lookup"><span data-stu-id="b3470-135">**visRowVertex** (InfiniteLine and Ellipse rows)</span></span>  <br/> |
| <span data-ttu-id="b3470-136">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="b3470-136">Cell index:</span></span>  <br/> |<span data-ttu-id="b3470-137">\*\*visBow \*\*(linha ArcTo)</span><span class="sxs-lookup"><span data-stu-id="b3470-137">**visBow** (ArcTo row)</span></span>  <br/> |
||<span data-ttu-id="b3470-138">**visControlX** (EllipticalArcTo row)</span><span class="sxs-lookup"><span data-stu-id="b3470-138">**visControlX** (EllipticalArcTo row)</span></span>  <br/> |
||<span data-ttu-id="b3470-139">**visControlY** (linha EllipticalArcTo)</span><span class="sxs-lookup"><span data-stu-id="b3470-139">**visControlY** (EllipticalArcTo row)</span></span>  <br/> |
||<span data-ttu-id="b3470-140">**visPolylineData** (Linha Polyline)</span><span class="sxs-lookup"><span data-stu-id="b3470-140">**visPolylineData** (Polyline row)</span></span>  <br/> |
||<span data-ttu-id="b3470-141">**visNURBSKnot** (Linha NURBSto)</span><span class="sxs-lookup"><span data-stu-id="b3470-141">**visNURBSKnot** (NURBSTo row)</span></span>  <br/> |
||<span data-ttu-id="b3470-142">**visSplineKnot** (Linhas SplineStart e SplineKnot)</span><span class="sxs-lookup"><span data-stu-id="b3470-142">**visSplineKnot** (SplineStart and SplineKnot rows)</span></span>  <br/> |
||<span data-ttu-id="b3470-143">**visInfiniteLineX2** (Linha InfiniteLine)</span><span class="sxs-lookup"><span data-stu-id="b3470-143">**visInfiniteLineX2** (InfiniteLine row)</span></span>  <br/> |
||<span data-ttu-id="b3470-144">**visEllipseMajorX** (Linha Ellipse)</span><span class="sxs-lookup"><span data-stu-id="b3470-144">**visEllipseMajorX** (Ellipse row)</span></span>  <br/> |
   

