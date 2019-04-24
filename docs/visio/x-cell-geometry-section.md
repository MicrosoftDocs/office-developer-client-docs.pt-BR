---
title: Célula X (Seção Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1135
localization_priority: Normal
ms.assetid: 2416b323-e084-18e1-c9be-a797078dfab9
description: Representa uma coordenada x em uma forma em coordenadas locais. Esta tabela descreve a célula X com base na linha na qual está localizada.
ms.openlocfilehash: 6554000a86a6bf27d343a5647161bbe416725e64
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285109"
---
# <a name="x-cell-geometry-section"></a><span data-ttu-id="e96be-104">Célula X (Seção Geometry)</span><span class="sxs-lookup"><span data-stu-id="e96be-104">X Cell (Geometry Section)</span></span>

<span data-ttu-id="e96be-105">Representa uma coordenada *x* em uma forma em coordenadas locais.</span><span class="sxs-lookup"><span data-stu-id="e96be-105">Represents an  *x*  -coordinate on a shape in local coordinates.</span></span> <span data-ttu-id="e96be-106">Esta tabela descreve a célula X com base na linha na qual está localizada.</span><span class="sxs-lookup"><span data-stu-id="e96be-106">This table describes the X cell based on the row in which it's located.</span></span> 
  
|<span data-ttu-id="e96be-107">**Linha**</span><span class="sxs-lookup"><span data-stu-id="e96be-107">**Row**</span></span>|<span data-ttu-id="e96be-108">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="e96be-108">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e96be-109">MoveTo</span><span class="sxs-lookup"><span data-stu-id="e96be-109">MoveTo</span></span>](moveto-row-geometry-section.md) <br/> | <span data-ttu-id="e96be-110">Se a linha MoveTo for a primeira linha na seção, a célula X representará a coordenada *X* do primeiro vértice de um caminho.</span><span class="sxs-lookup"><span data-stu-id="e96be-110">If the MoveTo row is the first row in the section, the X cell represents the  *x*  -coordinate of the first vertex of a path.</span></span> <span data-ttu-id="e96be-111">Se a linha MoveTo aparecer entre duas linhas, a célula X representará a coordenada *X* do primeiro vértice depois da quebra no caminho.</span><span class="sxs-lookup"><span data-stu-id="e96be-111">If the MoveTo row appears between two rows, the X cell represents the  *x*  -coordinate of the first vertex after the break in the path.</span></span>  <br/> |
|[<span data-ttu-id="e96be-112">LineTo</span><span class="sxs-lookup"><span data-stu-id="e96be-112">LineTo</span></span>](lineto-row-geometry-section.md) <br/> | <span data-ttu-id="e96be-113">A coordenada *x* do vértice final de um segmento de linha reta.</span><span class="sxs-lookup"><span data-stu-id="e96be-113">The  *x*  -coordinate of the ending vertex of a straight line segment.</span></span>  <br/> |
|[<span data-ttu-id="e96be-114">ArcTo</span><span class="sxs-lookup"><span data-stu-id="e96be-114">ArcTo</span></span>](arcto-row-geometry-section.md) <br/> | <span data-ttu-id="e96be-115">A coordenada *x* do vértice final de um arco.</span><span class="sxs-lookup"><span data-stu-id="e96be-115">The  *x*  -coordinate of the ending vertex of an arc.</span></span>  <br/> |
|[<span data-ttu-id="e96be-116">EllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="e96be-116">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> | <span data-ttu-id="e96be-117">A coordenada *x* do vértice final de um arco elíptico.</span><span class="sxs-lookup"><span data-stu-id="e96be-117">The  *x*  -coordinate of the ending vertex of an elliptical arc.</span></span>  <br/> |
|[<span data-ttu-id="e96be-118">PolylineTo</span><span class="sxs-lookup"><span data-stu-id="e96be-118">PolylineTo</span></span>](polylineto-row-geometry-section.md) <br/> | <span data-ttu-id="e96be-119">A coordenada *x* do vértice final de uma polilinha.</span><span class="sxs-lookup"><span data-stu-id="e96be-119">The  *x*  -coordinate of the ending vertex of a polyline.</span></span>  <br/> |
|[<span data-ttu-id="e96be-120">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="e96be-120">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> | <span data-ttu-id="e96be-121">A coordenada *x* do último ponto de controle de uma B-spline racional não-uniforme (NURBS).</span><span class="sxs-lookup"><span data-stu-id="e96be-121">The  *x*  -coordinate of the last control point of a nonuniform rational B-spline (NURBS).</span></span>  <br/> |
|[<span data-ttu-id="e96be-122">SplineStart</span><span class="sxs-lookup"><span data-stu-id="e96be-122">SplineStart</span></span>](splinestart-row-geometry-section.md) <br/> | <span data-ttu-id="e96be-123">A coordenada *x* do segundo ponto de controle de uma spline.</span><span class="sxs-lookup"><span data-stu-id="e96be-123">The  *x*  -coordinate of a spline's second control point.</span></span>  <br/> |
|[<span data-ttu-id="e96be-124">SplineKnot</span><span class="sxs-lookup"><span data-stu-id="e96be-124">SplineKnot</span></span>](splineknot-row-geometry-section.md) <br/> | <span data-ttu-id="e96be-125">A coordenada *x* de um ponto de controle.</span><span class="sxs-lookup"><span data-stu-id="e96be-125">The  *x*  -coordinate of a control point.</span></span>  <br/> |
|[<span data-ttu-id="e96be-126">InfiniteLine</span><span class="sxs-lookup"><span data-stu-id="e96be-126">InfiniteLine</span></span>](infiniteline-row-geometry-section.md) <br/> | <span data-ttu-id="e96be-127">Uma coordenada *x* de um ponto na linha infinita.</span><span class="sxs-lookup"><span data-stu-id="e96be-127">An  *x*  -coordinate of a point on the infinite line.</span></span>  <br/> |
|[<span data-ttu-id="e96be-128">Elipse</span><span class="sxs-lookup"><span data-stu-id="e96be-128">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> | <span data-ttu-id="e96be-129">A coordenada *x* do centro da elipse.</span><span class="sxs-lookup"><span data-stu-id="e96be-129">The  *x*  -coordinate of the center of the ellipse.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e96be-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="e96be-130">Remarks</span></span>

<span data-ttu-id="e96be-131">Para fazer referência à célula X pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="e96be-131">To get a reference to the X cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e96be-132">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="e96be-132">Cell name:</span></span>  <br/> | <span data-ttu-id="e96be-133">Geometry *i* . X *j* onde *i* e *j* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="e96be-133">Geometry  *i*  .X  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
|| <span data-ttu-id="e96be-134">Geometry *i* . X1 (linhas InfiniteLine e Ellipse) onde *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="e96be-134">Geometry  *i*  .X1 (InfiniteLine and Ellipse rows)            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="e96be-135">Para fazer referência à célula X pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="e96be-135">To get a reference to the X cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e96be-136">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="e96be-136">Section index:</span></span>  <br/> |<span data-ttu-id="e96be-137">**visSectionFirstComponent** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="e96be-137">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="e96be-138">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="e96be-138">Row index:</span></span>  <br/> |<span data-ttu-id="e96be-139">**visRowVertex** +  *j* onde *j* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="e96be-139">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
||<span data-ttu-id="e96be-140">\*\*visRowVertex \*\*(linhas Ellipse e InfiniteLine)</span><span class="sxs-lookup"><span data-stu-id="e96be-140">**visRowVertex** (InfiniteLine and Ellipse rows)</span></span>  <br/> |
| <span data-ttu-id="e96be-141">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="e96be-141">Cell index:</span></span>  <br/> |<span data-ttu-id="e96be-142">\*\*visX \*\*(linhas MoveTo, LineTo, ArcTo, EllipticalArcTo, NURBSTo, PolylineTo, SplineStart e SplineKnot)</span><span class="sxs-lookup"><span data-stu-id="e96be-142">**visX** (MoveTo, LineTo, ArcTo, EllipticalArcTo, NURBSTo, Polyline, SplineStart, and SplineKnot rows)</span></span>  <br/> |
||<span data-ttu-id="e96be-143">\*\*visInfiniteLineX1 \*\*(linha InfiniteLine)</span><span class="sxs-lookup"><span data-stu-id="e96be-143">**visInfiniteLineX1** (InfiniteLine row)</span></span>  <br/> |
||<span data-ttu-id="e96be-144">\*\*visEllipseCenterX \*\*(linha Ellipse)</span><span class="sxs-lookup"><span data-stu-id="e96be-144">**visEllipseCenterX** (Ellipse row)</span></span>  <br/> |
   

