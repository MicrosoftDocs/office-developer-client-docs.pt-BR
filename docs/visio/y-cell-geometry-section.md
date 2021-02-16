---
title: Célula Y (Seção Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251750
localization_priority: Normal
ms.assetid: a53b5787-f419-7a36-3c04-c63b3c173ac7
description: Representa uma coordenada y em uma forma em coordenadas locais. Esta tabela descreve a célula X com base na linha na qual está localizada.
ms.openlocfilehash: 7dea96b544c84f09abe1d72304da0bacaa09432f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540487"
---
# <a name="y-cell-geometry-section"></a><span data-ttu-id="de348-104">Célula Y (Seção Geometry)</span><span class="sxs-lookup"><span data-stu-id="de348-104">Y Cell (Geometry Section)</span></span>

<span data-ttu-id="de348-105">Representa uma coordenada  *y*  em uma forma em coordenadas locais.</span><span class="sxs-lookup"><span data-stu-id="de348-105">Represents a  *y*  -coordinate on a shape in local coordinates.</span></span> <span data-ttu-id="de348-106">Esta tabela descreve a célula X com base na linha na qual está localizada.</span><span class="sxs-lookup"><span data-stu-id="de348-106">This table describes the Y cell based on the row in which it's located.</span></span> 
  
|<span data-ttu-id="de348-107">Linha</span><span class="sxs-lookup"><span data-stu-id="de348-107">Row</span></span>|<span data-ttu-id="de348-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="de348-108">Description</span></span>|
|:-----|:-----|
|[<span data-ttu-id="de348-109">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="de348-109">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> | <span data-ttu-id="de348-110">Se a linha MoveTo for a primeira linha da seção, a célula Y representará a coordenada  *y*  do primeiro vértice de um caminho.</span><span class="sxs-lookup"><span data-stu-id="de348-110">If the MoveTo row is the first row in the section, the Y cell represents the  *y*  -coordinate of the first vertex of a path.</span></span> <span data-ttu-id="de348-111">Se a linha MoveTo aparecer entre duas linhas, a célula Y representará a coordenada  *y*  do primeiro vértice após a quebra no caminho.</span><span class="sxs-lookup"><span data-stu-id="de348-111">If the MoveTo row appears between two rows, the Y cell represents the  *y*  -coordinate of the first vertex after the break in the path.</span></span>  <br/> |
|[<span data-ttu-id="de348-112">LineTo</span><span class="sxs-lookup"><span data-stu-id="de348-112">LineTo</span></span>](lineto-row-geometry-section.md) <br/> | <span data-ttu-id="de348-113">A  *coordenada y*  do vértice final de um segmento de linha reta.</span><span class="sxs-lookup"><span data-stu-id="de348-113">The  *y*  -coordinate of the ending vertex of a straight line segment.</span></span>  <br/> |
|[<span data-ttu-id="de348-114">ArcTo</span><span class="sxs-lookup"><span data-stu-id="de348-114">ArcTo</span></span>](arcto-row-geometry-section.md) <br/> | <span data-ttu-id="de348-115">A  *coordenada y*  do vértice final de um arco.</span><span class="sxs-lookup"><span data-stu-id="de348-115">The  *y*  -coordinate of the ending vertex of an arc.</span></span>  <br/> |
|[<span data-ttu-id="de348-116">EllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="de348-116">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> | <span data-ttu-id="de348-117">A  *coordenada y*  do vértice final de um arco elíptico.</span><span class="sxs-lookup"><span data-stu-id="de348-117">The  *y*  -coordinate of the ending vertex of an elliptical arc.</span></span>  <br/> |
|[<span data-ttu-id="de348-118">PolylineTo</span><span class="sxs-lookup"><span data-stu-id="de348-118">PolylineTo</span></span>](polylineto-row-geometry-section.md) <br/> | <span data-ttu-id="de348-119">A  *coordenada y*  do vértice final de uma polilinha.</span><span class="sxs-lookup"><span data-stu-id="de348-119">The  *y*  -coordinate of the ending vertex of a polyline.</span></span>  <br/> |
|[<span data-ttu-id="de348-120">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="de348-120">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> | <span data-ttu-id="de348-121">A  *coordenada y*  do último ponto de controle de uma B-spline racional não uniforme (NURBS).</span><span class="sxs-lookup"><span data-stu-id="de348-121">The  *y*  -coordinate of the last control point of a nonuniform rational B-spline (NURBS).</span></span>  <br/> |
|[<span data-ttu-id="de348-122">SplineStart</span><span class="sxs-lookup"><span data-stu-id="de348-122">SplineStart</span></span>](splinestart-row-geometry-section.md) <br/> | <span data-ttu-id="de348-123">A  *coordenada y*  do segundo ponto de controle de uma spline.</span><span class="sxs-lookup"><span data-stu-id="de348-123">The  *y*  -coordinate of a spline's second control point.</span></span>  <br/> |
|[<span data-ttu-id="de348-124">SplineKnot</span><span class="sxs-lookup"><span data-stu-id="de348-124">SplineKnot</span></span>](splineknot-row-geometry-section.md) <br/> | <span data-ttu-id="de348-125">A  *coordenada y*  de um ponto de controle.</span><span class="sxs-lookup"><span data-stu-id="de348-125">The  *y*  -coordinate of a control point.</span></span>  <br/> |
|[<span data-ttu-id="de348-126">InfiniteLine</span><span class="sxs-lookup"><span data-stu-id="de348-126">InfiniteLine</span></span>](infiniteline-row-geometry-section.md) <br/> | <span data-ttu-id="de348-127">Uma  *coordenada y*  de um ponto na linha infinita.</span><span class="sxs-lookup"><span data-stu-id="de348-127">A  *y-*  coordinate of a point on the infinite line.</span></span>  <br/> |
|[<span data-ttu-id="de348-128">Elipse</span><span class="sxs-lookup"><span data-stu-id="de348-128">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> | <span data-ttu-id="de348-129">A  *coordenada y*  do centro da elipse.</span><span class="sxs-lookup"><span data-stu-id="de348-129">The  *y*  -coordinate of the center of the ellipse.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="de348-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="de348-130">Remarks</span></span>

<span data-ttu-id="de348-131">Para fazer referência à célula Y pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="de348-131">To get a reference to the Y cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="de348-132">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="de348-132">Cell name:</span></span>  <br/> | <span data-ttu-id="de348-133">Geometry  *i*  . Y  *j*            onde  *i*  e  *j*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="de348-133">Geometry  *i*  .Y  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
|| <span data-ttu-id="de348-134">Geometry  *i*  . Y1 (linhas InfiniteLine e Ellipse) onde  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="de348-134">Geometry  *i*  .Y1 (InfiniteLine and Ellipse rows)            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="de348-135">Para fazer referência à célula Y pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="de348-135">To get a reference to the Y cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="de348-136">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="de348-136">Section index:</span></span>  <br/> |<span data-ttu-id="de348-137">**visSectionFirstComponent**  +   *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="de348-137">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="de348-138">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="de348-138">Row index:</span></span>  <br/> |<span data-ttu-id="de348-139">**visRowVertex**  +   *j* onde *j* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="de348-139">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
||<span data-ttu-id="de348-140">**visRowVertex**(linhas Ellipse e InfiniteLine)</span><span class="sxs-lookup"><span data-stu-id="de348-140">**visRowVertex** (InfiniteLine and Ellipse rows)</span></span>  <br/> |
| <span data-ttu-id="de348-141">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="de348-141">Cell index:</span></span>  <br/> |<span data-ttu-id="de348-142">**visY**(linhas MoveTo, LineTo, ArcTo, EllipticalArcTo, NURBSTo, PolylineTo, SplineStart e SplineKnot)</span><span class="sxs-lookup"><span data-stu-id="de348-142">**visY** (MoveTo, LineTo, ArcTo, EllipticalArcTo, NURBSTo, Polyline, SplineStart, and SplineKnot rows)</span></span>  <br/> |
||<span data-ttu-id="de348-143">**visInfiniteLineY1**(linha InfiniteLine)</span><span class="sxs-lookup"><span data-stu-id="de348-143">**visInfiniteLineY1** (InfiniteLine row)</span></span>  <br/> |
||<span data-ttu-id="de348-144">**visEllipseCenterY**(linha Ellipse)</span><span class="sxs-lookup"><span data-stu-id="de348-144">**visEllipseCenterY** (Ellipse row)</span></span>  <br/> |
   

