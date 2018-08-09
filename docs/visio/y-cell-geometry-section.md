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
description: Representa um y-coordenadas em uma forma em coordenadas locais. Esta tabela descreve a célula Y com base na linha na qual está localizada.
ms.openlocfilehash: 461fd0ec41d34132f469c811292550d2f7e094f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773333"
---
# <a name="y-cell-geometry-section"></a><span data-ttu-id="8985c-104">Célula Y (Seção Geometry)</span><span class="sxs-lookup"><span data-stu-id="8985c-104">Y Cell (Geometry Section)</span></span>

<span data-ttu-id="8985c-105">Representa um *y* -coordenadas em uma forma em coordenadas locais.</span><span class="sxs-lookup"><span data-stu-id="8985c-105">Represents a  *y*  -coordinate on a shape in local coordinates.</span></span> <span data-ttu-id="8985c-106">Esta tabela descreve a célula Y com base na linha na qual está localizada.</span><span class="sxs-lookup"><span data-stu-id="8985c-106">This table describes the Y cell based on the row in which it's located.</span></span> 
  
|<span data-ttu-id="8985c-107">**Row**</span><span class="sxs-lookup"><span data-stu-id="8985c-107">**Row**</span></span>|<span data-ttu-id="8985c-108">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="8985c-108">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8985c-109">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="8985c-109">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> | <span data-ttu-id="8985c-110">Se a linha MoveTo for a primeira linha na seção, a célula Y representará a *y* -coordenadas do primeiro vértice de um caminho.</span><span class="sxs-lookup"><span data-stu-id="8985c-110">If the MoveTo row is the first row in the section, the Y cell represents the  *y*  -coordinate of the first vertex of a path.</span></span> <span data-ttu-id="8985c-111">Se a linha MoveTo aparecer entre duas linhas, a célula Y representará a *y* -coordenadas do primeiro vértice depois da quebra no caminho.</span><span class="sxs-lookup"><span data-stu-id="8985c-111">If the MoveTo row appears between two rows, the Y cell represents the  *y*  -coordinate of the first vertex after the break in the path.</span></span>  <br/> |
|[<span data-ttu-id="8985c-112">LineTo</span><span class="sxs-lookup"><span data-stu-id="8985c-112">LineTo</span></span>](lineto-row-geometry-section.md) <br/> | <span data-ttu-id="8985c-113">*Y* -coordenadas do vértice final de um segmento de linha reta.</span><span class="sxs-lookup"><span data-stu-id="8985c-113">The  *y*  -coordinate of the ending vertex of a straight line segment.</span></span>  <br/> |
|[<span data-ttu-id="8985c-114">ArcTo</span><span class="sxs-lookup"><span data-stu-id="8985c-114">ArcTo</span></span>](arcto-row-geometry-section.md) <br/> | <span data-ttu-id="8985c-115">*Y* -coordenadas do vértice final de um arco.</span><span class="sxs-lookup"><span data-stu-id="8985c-115">The  *y*  -coordinate of the ending vertex of an arc.</span></span>  <br/> |
|[<span data-ttu-id="8985c-116">EllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="8985c-116">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> | <span data-ttu-id="8985c-117">*Y* -coordenadas do vértice final de um arco elíptico.</span><span class="sxs-lookup"><span data-stu-id="8985c-117">The  *y*  -coordinate of the ending vertex of an elliptical arc.</span></span>  <br/> |
|[<span data-ttu-id="8985c-118">PolylineTo</span><span class="sxs-lookup"><span data-stu-id="8985c-118">PolylineTo</span></span>](polylineto-row-geometry-section.md) <br/> | <span data-ttu-id="8985c-119">*Y* -coordenadas do vértice final de uma polilinha.</span><span class="sxs-lookup"><span data-stu-id="8985c-119">The  *y*  -coordinate of the ending vertex of a polyline.</span></span>  <br/> |
|[<span data-ttu-id="8985c-120">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="8985c-120">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> | <span data-ttu-id="8985c-121">*Y* -coordenadas do último ponto de controle de uma B-spline racional não-uniforme (NURBS).</span><span class="sxs-lookup"><span data-stu-id="8985c-121">The  *y*  -coordinate of the last control point of a nonuniform rational B-spline (NURBS).</span></span>  <br/> |
|[<span data-ttu-id="8985c-122">SplineStart</span><span class="sxs-lookup"><span data-stu-id="8985c-122">SplineStart</span></span>](splinestart-row-geometry-section.md) <br/> | <span data-ttu-id="8985c-123">*Y* -coordenadas do segundo ponto de controle de uma spline.</span><span class="sxs-lookup"><span data-stu-id="8985c-123">The  *y*  -coordinate of a spline's second control point.</span></span>  <br/> |
|[<span data-ttu-id="8985c-124">SplineKnot</span><span class="sxs-lookup"><span data-stu-id="8985c-124">SplineKnot</span></span>](splineknot-row-geometry-section.md) <br/> | <span data-ttu-id="8985c-125">*Y* -coordenadas de um ponto de controle.</span><span class="sxs-lookup"><span data-stu-id="8985c-125">The  *y*  -coordinate of a control point.</span></span>  <br/> |
|[<span data-ttu-id="8985c-126">InfiniteLine</span><span class="sxs-lookup"><span data-stu-id="8985c-126">InfiniteLine</span></span>](infiniteline-row-geometry-section.md) <br/> | <span data-ttu-id="8985c-127">*Y -* coordenadas de um ponto em uma linha infinita.</span><span class="sxs-lookup"><span data-stu-id="8985c-127">A  *y-*  coordinate of a point on the infinite line.</span></span>  <br/> |
|[<span data-ttu-id="8985c-128">Elipse</span><span class="sxs-lookup"><span data-stu-id="8985c-128">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> | <span data-ttu-id="8985c-129">*Y* -coordenadas do centro da elipse.</span><span class="sxs-lookup"><span data-stu-id="8985c-129">The  *y*  -coordinate of the center of the ellipse.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8985c-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="8985c-130">Remarks</span></span>

<span data-ttu-id="8985c-131">Para fazer referência à célula Y pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="8985c-131">To get a reference to the Y cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8985c-132">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="8985c-132">Cell name:</span></span>  <br/> | <span data-ttu-id="8985c-133">Geometria *i* . Y *j* onde *i* e *j* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="8985c-133">Geometry  *i*  .Y  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
|| <span data-ttu-id="8985c-134">Geometria *i* . Y1 (linhas InfiniteLine e Ellipse) onde *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="8985c-134">Geometry  *i*  .Y1 (InfiniteLine and Ellipse rows)            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="8985c-135">Para fazer referência à célula Y pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="8985c-135">To get a reference to the Y cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8985c-136">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="8985c-136">Section index:</span></span>  <br/> |<span data-ttu-id="8985c-137">**visSectionFirstComponent** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="8985c-137">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="8985c-138">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="8985c-138">Row index:</span></span>  <br/> |<span data-ttu-id="8985c-139">**visRowVertex** +  *j* onde *j* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="8985c-139">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
||<span data-ttu-id="8985c-140">**visRowVertex **(linhas Ellipse e InfiniteLine)</span><span class="sxs-lookup"><span data-stu-id="8985c-140">**visRowVertex** (InfiniteLine and Ellipse rows)</span></span>  <br/> |
| <span data-ttu-id="8985c-141">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="8985c-141">Cell index:</span></span>  <br/> |<span data-ttu-id="8985c-142">**visY **(linhas MoveTo, LineTo, ArcTo, EllipticalArcTo, NURBSTo, PolylineTo, SplineStart e SplineKnot)</span><span class="sxs-lookup"><span data-stu-id="8985c-142">**visY** (MoveTo, LineTo, ArcTo, EllipticalArcTo, NURBSTo, Polyline, SplineStart, and SplineKnot rows)</span></span>  <br/> |
||<span data-ttu-id="8985c-143">**visInfiniteLineY1 **(linha InfiniteLine)</span><span class="sxs-lookup"><span data-stu-id="8985c-143">**visInfiniteLineY1** (InfiniteLine row)</span></span>  <br/> |
||<span data-ttu-id="8985c-144">**visEllipseCenterY **(linha Ellipse)</span><span class="sxs-lookup"><span data-stu-id="8985c-144">**visEllipseCenterY** (Ellipse row)</span></span>  <br/> |
   

