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
ms.openlocfilehash: 7009658c7a6844a5c6071f502c05114a4accd7b7
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541299"
---
# <a name="a-cell-geometry-section"></a><span data-ttu-id="08257-104">Célula A (Seção Geometry)</span><span class="sxs-lookup"><span data-stu-id="08257-104">A Cell (Geometry Section)</span></span>

<span data-ttu-id="08257-105">Representa informações diferentes em linhas diferentes.</span><span class="sxs-lookup"><span data-stu-id="08257-105">Represents different information in different rows.</span></span> <span data-ttu-id="08257-106">Esta tabela descreve a célula A com base na linha na qual está localizada.</span><span class="sxs-lookup"><span data-stu-id="08257-106">This table describes the A cell based on the row in which it's located.</span></span>
  
|<span data-ttu-id="08257-107">Linha</span><span class="sxs-lookup"><span data-stu-id="08257-107">Row</span></span>|<span data-ttu-id="08257-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="08257-108">Description</span></span>|
|:-----|:-----|
|[<span data-ttu-id="08257-109">ArcTo</span><span class="sxs-lookup"><span data-stu-id="08257-109">ArcTo</span></span>](arcto-row-geometry-section.md) <br/> | <span data-ttu-id="08257-110">A distância do ponto médio de um arco até o ponto médio de sua corda.</span><span class="sxs-lookup"><span data-stu-id="08257-110">The distance from the arc's midpoint to the midpoint of its chord.</span></span>  <br/> |
|[<span data-ttu-id="08257-111">EllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="08257-111">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> | <span data-ttu-id="08257-112">A coordenada *x* do ponto de controle do arco, um ponto no arco. O ponto de controle é melhor localizado sobre a metade entre os vértices inicial e final do arco. Caso contrário, o arco pode chegar a um tamanho extremo para passar pelo ponto de controle, com resultados imprevisíveis.</span><span class="sxs-lookup"><span data-stu-id="08257-112">The  *x*  -coordinate of the arc's control point, a point on the arc. The control point is best located about halfway between the beginning and ending vertices of the arc. Otherwise, the arc may grow to an extreme size in order to pass through the control point, with unpredictable results.</span></span>  <br/> |
|[<span data-ttu-id="08257-113">PolylineTo</span><span class="sxs-lookup"><span data-stu-id="08257-113">PolylineTo</span></span>](polylineto-row-geometry-section.md) <br/> | <span data-ttu-id="08257-114">A fórmula da polilinha.</span><span class="sxs-lookup"><span data-stu-id="08257-114">The polyline formula.</span></span>  <br/> |
|[<span data-ttu-id="08257-115">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="08257-115">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> | <span data-ttu-id="08257-116">O penúltimo nó da B-spline racional não-uniforme (NURBS).</span><span class="sxs-lookup"><span data-stu-id="08257-116">The second to the last knot of the nonuniform rational B-spline (NURBS).</span></span>  <br/> |
|[<span data-ttu-id="08257-117">SplineStart</span><span class="sxs-lookup"><span data-stu-id="08257-117">SplineStart</span></span>](splinestart-row-geometry-section.md) <br/> | <span data-ttu-id="08257-118">O segundo nó da spline.</span><span class="sxs-lookup"><span data-stu-id="08257-118">The second knot of the spline.</span></span>  <br/> |
|[<span data-ttu-id="08257-119">SplineKnot</span><span class="sxs-lookup"><span data-stu-id="08257-119">SplineKnot</span></span>](splineknot-row-geometry-section.md) <br/> | <span data-ttu-id="08257-120">Um dos nós da spline (exceto o último ou os dois primeiros).</span><span class="sxs-lookup"><span data-stu-id="08257-120">One of the spline's knots (other than the last one or the first two).</span></span>  <br/> |
|[<span data-ttu-id="08257-121">InfiniteLine</span><span class="sxs-lookup"><span data-stu-id="08257-121">InfiniteLine</span></span>](infiniteline-row-geometry-section.md) <br/> | <span data-ttu-id="08257-122">Uma coordenada *x* de um ponto na linha infinita; emparelhado com a coordenada *y* representada pela célula [B](b-cell-geometry-section.md) .</span><span class="sxs-lookup"><span data-stu-id="08257-122">An  *x*  -coordinate of a point on the infinite line; paired with  *y*  -coordinate represented by the [B](b-cell-geometry-section.md) cell.</span></span>  <br/> |
|[<span data-ttu-id="08257-123">Elipse</span><span class="sxs-lookup"><span data-stu-id="08257-123">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> | <span data-ttu-id="08257-124">Uma coordenada *x* de um ponto na elipse; emparelhado com a coordenada *y* representada pela célula [B](b-cell-geometry-section.md) .</span><span class="sxs-lookup"><span data-stu-id="08257-124">An  *x*  -coordinate of a point on the ellipse; paired with  *y*  -coordinate represented by the [B](b-cell-geometry-section.md) cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="08257-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="08257-125">Remarks</span></span>

<span data-ttu-id="08257-126">Para fazer referência à célula A pelo nome, a partir de outra fórmula ou programa, usando a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="08257-126">To get a reference to the A cell by name from another formula, or from a program, using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="08257-127">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="08257-127">Cell name:</span></span>  <br/> | <span data-ttu-id="08257-128">Geometry *i* . A *j* onde *i* e *j* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="08257-128">Geometry  *i*  .A  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
|| <span data-ttu-id="08257-129">Geometry *i* . A1 (linhas InfiniteLine e Ellipse) onde *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="08257-129">Geometry  *i*  .A1 (InfiniteLine and Ellipse rows)            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="08257-130">Para fazer referência à célula A pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="08257-130">To get a reference to the A cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="08257-131">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="08257-131">Section index:</span></span>  <br/> |<span data-ttu-id="08257-132">**visSectionFirstComponent** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="08257-132">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="08257-133">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="08257-133">Row index:</span></span>  <br/> |<span data-ttu-id="08257-134">**visRowVertex** +  *j* onde *j* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="08257-134">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
||<span data-ttu-id="08257-135">\*\*visRowVertex \*\*(linhas Ellipse e InfiniteLine)</span><span class="sxs-lookup"><span data-stu-id="08257-135">**visRowVertex** (InfiniteLine and Ellipse rows)</span></span>  <br/> |
| <span data-ttu-id="08257-136">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="08257-136">Cell index:</span></span>  <br/> |<span data-ttu-id="08257-137">\*\*visBow \*\*(linha ArcTo)</span><span class="sxs-lookup"><span data-stu-id="08257-137">**visBow** (ArcTo row)</span></span>  <br/> |
||<span data-ttu-id="08257-138">**visControlX** (EllipticalArcTo row)</span><span class="sxs-lookup"><span data-stu-id="08257-138">**visControlX** (EllipticalArcTo row)</span></span>  <br/> |
||<span data-ttu-id="08257-139">**visControlY** (linha EllipticalArcTo)</span><span class="sxs-lookup"><span data-stu-id="08257-139">**visControlY** (EllipticalArcTo row)</span></span>  <br/> |
||<span data-ttu-id="08257-140">**visPolylineData** (Linha Polyline)</span><span class="sxs-lookup"><span data-stu-id="08257-140">**visPolylineData** (Polyline row)</span></span>  <br/> |
||<span data-ttu-id="08257-141">**visNURBSKnot** (Linha NURBSto)</span><span class="sxs-lookup"><span data-stu-id="08257-141">**visNURBSKnot** (NURBSTo row)</span></span>  <br/> |
||<span data-ttu-id="08257-142">**visSplineKnot** (Linhas SplineStart e SplineKnot)</span><span class="sxs-lookup"><span data-stu-id="08257-142">**visSplineKnot** (SplineStart and SplineKnot rows)</span></span>  <br/> |
||<span data-ttu-id="08257-143">**visInfiniteLineX2** (Linha InfiniteLine)</span><span class="sxs-lookup"><span data-stu-id="08257-143">**visInfiniteLineX2** (InfiniteLine row)</span></span>  <br/> |
||<span data-ttu-id="08257-144">**visEllipseMajorX** (Linha Ellipse)</span><span class="sxs-lookup"><span data-stu-id="08257-144">**visEllipseMajorX** (Ellipse row)</span></span>  <br/> |
   

