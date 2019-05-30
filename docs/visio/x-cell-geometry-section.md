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
ms.openlocfilehash: 2b3303533db446780ef797844ac5e1438cec242f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538211"
---
# <a name="x-cell-geometry-section"></a><span data-ttu-id="137e9-104">Célula X (Seção Geometry)</span><span class="sxs-lookup"><span data-stu-id="137e9-104">X Cell (Geometry Section)</span></span>

<span data-ttu-id="137e9-105">Representa uma coordenada *x* em uma forma em coordenadas locais.</span><span class="sxs-lookup"><span data-stu-id="137e9-105">Represents an  *x*  -coordinate on a shape in local coordinates.</span></span> <span data-ttu-id="137e9-106">Esta tabela descreve a célula X com base na linha na qual está localizada.</span><span class="sxs-lookup"><span data-stu-id="137e9-106">This table describes the X cell based on the row in which it's located.</span></span> 
  
|<span data-ttu-id="137e9-107">Linha</span><span class="sxs-lookup"><span data-stu-id="137e9-107">Row</span></span>|<span data-ttu-id="137e9-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="137e9-108">Description</span></span>|
|:-----|:-----|
|[<span data-ttu-id="137e9-109">MoveTo</span><span class="sxs-lookup"><span data-stu-id="137e9-109">MoveTo</span></span>](moveto-row-geometry-section.md) <br/> | <span data-ttu-id="137e9-110">Se a linha MoveTo for a primeira linha na seção, a célula X representará a coordenada *X* do primeiro vértice de um caminho.</span><span class="sxs-lookup"><span data-stu-id="137e9-110">If the MoveTo row is the first row in the section, the X cell represents the  *x*  -coordinate of the first vertex of a path.</span></span> <span data-ttu-id="137e9-111">Se a linha MoveTo aparecer entre duas linhas, a célula X representará a coordenada *X* do primeiro vértice depois da quebra no caminho.</span><span class="sxs-lookup"><span data-stu-id="137e9-111">If the MoveTo row appears between two rows, the X cell represents the  *x*  -coordinate of the first vertex after the break in the path.</span></span>  <br/> |
|[<span data-ttu-id="137e9-112">LineTo</span><span class="sxs-lookup"><span data-stu-id="137e9-112">LineTo</span></span>](lineto-row-geometry-section.md) <br/> | <span data-ttu-id="137e9-113">A coordenada *x* do vértice final de um segmento de linha reta.</span><span class="sxs-lookup"><span data-stu-id="137e9-113">The  *x*  -coordinate of the ending vertex of a straight line segment.</span></span>  <br/> |
|[<span data-ttu-id="137e9-114">ArcTo</span><span class="sxs-lookup"><span data-stu-id="137e9-114">ArcTo</span></span>](arcto-row-geometry-section.md) <br/> | <span data-ttu-id="137e9-115">A coordenada *x* do vértice final de um arco.</span><span class="sxs-lookup"><span data-stu-id="137e9-115">The  *x*  -coordinate of the ending vertex of an arc.</span></span>  <br/> |
|[<span data-ttu-id="137e9-116">EllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="137e9-116">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> | <span data-ttu-id="137e9-117">A coordenada *x* do vértice final de um arco elíptico.</span><span class="sxs-lookup"><span data-stu-id="137e9-117">The  *x*  -coordinate of the ending vertex of an elliptical arc.</span></span>  <br/> |
|[<span data-ttu-id="137e9-118">PolylineTo</span><span class="sxs-lookup"><span data-stu-id="137e9-118">PolylineTo</span></span>](polylineto-row-geometry-section.md) <br/> | <span data-ttu-id="137e9-119">A coordenada *x* do vértice final de uma polilinha.</span><span class="sxs-lookup"><span data-stu-id="137e9-119">The  *x*  -coordinate of the ending vertex of a polyline.</span></span>  <br/> |
|[<span data-ttu-id="137e9-120">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="137e9-120">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> | <span data-ttu-id="137e9-121">A coordenada *x* do último ponto de controle de uma B-spline racional não-uniforme (NURBS).</span><span class="sxs-lookup"><span data-stu-id="137e9-121">The  *x*  -coordinate of the last control point of a nonuniform rational B-spline (NURBS).</span></span>  <br/> |
|[<span data-ttu-id="137e9-122">SplineStart</span><span class="sxs-lookup"><span data-stu-id="137e9-122">SplineStart</span></span>](splinestart-row-geometry-section.md) <br/> | <span data-ttu-id="137e9-123">A coordenada *x* do segundo ponto de controle de uma spline.</span><span class="sxs-lookup"><span data-stu-id="137e9-123">The  *x*  -coordinate of a spline's second control point.</span></span>  <br/> |
|[<span data-ttu-id="137e9-124">SplineKnot</span><span class="sxs-lookup"><span data-stu-id="137e9-124">SplineKnot</span></span>](splineknot-row-geometry-section.md) <br/> | <span data-ttu-id="137e9-125">A coordenada *x* de um ponto de controle.</span><span class="sxs-lookup"><span data-stu-id="137e9-125">The  *x*  -coordinate of a control point.</span></span>  <br/> |
|[<span data-ttu-id="137e9-126">InfiniteLine</span><span class="sxs-lookup"><span data-stu-id="137e9-126">InfiniteLine</span></span>](infiniteline-row-geometry-section.md) <br/> | <span data-ttu-id="137e9-127">Uma coordenada *x* de um ponto na linha infinita.</span><span class="sxs-lookup"><span data-stu-id="137e9-127">An  *x*  -coordinate of a point on the infinite line.</span></span>  <br/> |
|[<span data-ttu-id="137e9-128">Elipse</span><span class="sxs-lookup"><span data-stu-id="137e9-128">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> | <span data-ttu-id="137e9-129">A coordenada *x* do centro da elipse.</span><span class="sxs-lookup"><span data-stu-id="137e9-129">The  *x*  -coordinate of the center of the ellipse.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="137e9-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="137e9-130">Remarks</span></span>

<span data-ttu-id="137e9-131">Para fazer referência à célula X pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="137e9-131">To get a reference to the X cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="137e9-132">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="137e9-132">Cell name:</span></span>  <br/> | <span data-ttu-id="137e9-133">Geometry *i* . X *j* onde *i* e *j* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="137e9-133">Geometry  *i*  .X  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
|| <span data-ttu-id="137e9-134">Geometry *i* . X1 (linhas InfiniteLine e Ellipse) onde *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="137e9-134">Geometry  *i*  .X1 (InfiniteLine and Ellipse rows)            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="137e9-135">Para fazer referência à célula X pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="137e9-135">To get a reference to the X cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="137e9-136">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="137e9-136">Section index:</span></span>  <br/> |<span data-ttu-id="137e9-137">**visSectionFirstComponent** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="137e9-137">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="137e9-138">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="137e9-138">Row index:</span></span>  <br/> |<span data-ttu-id="137e9-139">**visRowVertex** +  *j* onde *j* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="137e9-139">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
||<span data-ttu-id="137e9-140">\*\*visRowVertex \*\*(linhas Ellipse e InfiniteLine)</span><span class="sxs-lookup"><span data-stu-id="137e9-140">**visRowVertex** (InfiniteLine and Ellipse rows)</span></span>  <br/> |
| <span data-ttu-id="137e9-141">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="137e9-141">Cell index:</span></span>  <br/> |<span data-ttu-id="137e9-142">\*\*visX \*\*(linhas MoveTo, LineTo, ArcTo, EllipticalArcTo, NURBSTo, PolylineTo, SplineStart e SplineKnot)</span><span class="sxs-lookup"><span data-stu-id="137e9-142">**visX** (MoveTo, LineTo, ArcTo, EllipticalArcTo, NURBSTo, Polyline, SplineStart, and SplineKnot rows)</span></span>  <br/> |
||<span data-ttu-id="137e9-143">\*\*visInfiniteLineX1 \*\*(linha InfiniteLine)</span><span class="sxs-lookup"><span data-stu-id="137e9-143">**visInfiniteLineX1** (InfiniteLine row)</span></span>  <br/> |
||<span data-ttu-id="137e9-144">\*\*visEllipseCenterX \*\*(linha Ellipse)</span><span class="sxs-lookup"><span data-stu-id="137e9-144">**visEllipseCenterX** (Ellipse row)</span></span>  <br/> |
   

