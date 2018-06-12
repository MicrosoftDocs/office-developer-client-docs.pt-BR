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
description: Representa um x-coordenadas em uma forma em coordenadas locais. Esta tabela descreve a célula X com base na linha na qual está localizada.
ms.openlocfilehash: e5bc99d4f73d49741c4378009dfc2a883bb655ed
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773298"
---
# <a name="x-cell-geometry-section"></a><span data-ttu-id="962ca-104">Célula X (Seção Geometry)</span><span class="sxs-lookup"><span data-stu-id="962ca-104">X Cell (Geometry Section)</span></span>

<span data-ttu-id="962ca-105">Representa um *x* -coordenadas em uma forma em coordenadas locais.</span><span class="sxs-lookup"><span data-stu-id="962ca-105">Represents an  *x*  -coordinate on a shape in local coordinates.</span></span> <span data-ttu-id="962ca-106">Esta tabela descreve a célula X com base na linha na qual está localizada.</span><span class="sxs-lookup"><span data-stu-id="962ca-106">This table describes the X cell based on the row in which it's located.</span></span> 
  
|<span data-ttu-id="962ca-107">**Row**</span><span class="sxs-lookup"><span data-stu-id="962ca-107">**Row**</span></span>|<span data-ttu-id="962ca-108">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="962ca-108">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="962ca-109">MoveTo</span><span class="sxs-lookup"><span data-stu-id="962ca-109">MoveTo</span></span>](moveto-row-geometry-section.md) <br/> | <span data-ttu-id="962ca-110">Se a linha MoveTo for a primeira linha na seção, a célula X representará a *x* -coordenadas do primeiro vértice de um caminho.</span><span class="sxs-lookup"><span data-stu-id="962ca-110">If the MoveTo row is the first row in the section, the X cell represents the  *x*  -coordinate of the first vertex of a path.</span></span> <span data-ttu-id="962ca-111">Se a linha MoveTo aparecer entre duas linhas, a célula X representará a *x* -coordenadas do primeiro vértice depois da quebra no caminho.</span><span class="sxs-lookup"><span data-stu-id="962ca-111">If the MoveTo row appears between two rows, the X cell represents the  *x*  -coordinate of the first vertex after the break in the path.</span></span>  <br/> |
|[<span data-ttu-id="962ca-112">LineTo</span><span class="sxs-lookup"><span data-stu-id="962ca-112">LineTo</span></span>](lineto-row-geometry-section.md) <br/> | <span data-ttu-id="962ca-113">*X* -coordenadas do vértice final de um segmento de linha reta.</span><span class="sxs-lookup"><span data-stu-id="962ca-113">The  *x*  -coordinate of the ending vertex of a straight line segment.</span></span>  <br/> |
|[<span data-ttu-id="962ca-114">ArcTo</span><span class="sxs-lookup"><span data-stu-id="962ca-114">ArcTo</span></span>](arcto-row-geometry-section.md) <br/> | <span data-ttu-id="962ca-115">*X* -coordenadas do vértice final de um arco.</span><span class="sxs-lookup"><span data-stu-id="962ca-115">The  *x*  -coordinate of the ending vertex of an arc.</span></span>  <br/> |
|[<span data-ttu-id="962ca-116">EllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="962ca-116">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> | <span data-ttu-id="962ca-117">*X* -coordenadas do vértice final de um arco elíptico.</span><span class="sxs-lookup"><span data-stu-id="962ca-117">The  *x*  -coordinate of the ending vertex of an elliptical arc.</span></span>  <br/> |
|[<span data-ttu-id="962ca-118">PolylineTo</span><span class="sxs-lookup"><span data-stu-id="962ca-118">PolylineTo</span></span>](polylineto-row-geometry-section.md) <br/> | <span data-ttu-id="962ca-119">*X* -coordenadas do vértice final de uma polilinha.</span><span class="sxs-lookup"><span data-stu-id="962ca-119">The  *x*  -coordinate of the ending vertex of a polyline.</span></span>  <br/> |
|[<span data-ttu-id="962ca-120">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="962ca-120">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> | <span data-ttu-id="962ca-121">*X* -coordenadas do último ponto de controle de uma B-spline racional não-uniforme (NURBS).</span><span class="sxs-lookup"><span data-stu-id="962ca-121">The  *x*  -coordinate of the last control point of a nonuniform rational B-spline (NURBS).</span></span>  <br/> |
|[<span data-ttu-id="962ca-122">SplineStart</span><span class="sxs-lookup"><span data-stu-id="962ca-122">SplineStart</span></span>](splinestart-row-geometry-section.md) <br/> | <span data-ttu-id="962ca-123">*X* -coordenadas do segundo ponto de controle de uma spline.</span><span class="sxs-lookup"><span data-stu-id="962ca-123">The  *x*  -coordinate of a spline's second control point.</span></span>  <br/> |
|[<span data-ttu-id="962ca-124">SplineKnot</span><span class="sxs-lookup"><span data-stu-id="962ca-124">SplineKnot</span></span>](splineknot-row-geometry-section.md) <br/> | <span data-ttu-id="962ca-125">*X* -coordenadas de um ponto de controle.</span><span class="sxs-lookup"><span data-stu-id="962ca-125">The  *x*  -coordinate of a control point.</span></span>  <br/> |
|[<span data-ttu-id="962ca-126">InfiniteLine</span><span class="sxs-lookup"><span data-stu-id="962ca-126">InfiniteLine</span></span>](infiniteline-row-geometry-section.md) <br/> | <span data-ttu-id="962ca-127">Um *x* -coordenadas de um ponto em uma linha infinita.</span><span class="sxs-lookup"><span data-stu-id="962ca-127">An  *x*  -coordinate of a point on the infinite line.</span></span>  <br/> |
|[<span data-ttu-id="962ca-128">Elipse</span><span class="sxs-lookup"><span data-stu-id="962ca-128">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> | <span data-ttu-id="962ca-129">*X* -coordenadas do centro da elipse.</span><span class="sxs-lookup"><span data-stu-id="962ca-129">The  *x*  -coordinate of the center of the ellipse.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="962ca-130">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="962ca-130">Remarks</span></span>

<span data-ttu-id="962ca-131">Para obter uma referência à célula X pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="962ca-131">To get a reference to the X cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="962ca-132">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="962ca-132">Cell name:</span></span>  <br/> | <span data-ttu-id="962ca-133">Geometria *i* . X *j* onde *i* e *j* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="962ca-133">Geometry  *i*  .X  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
|| <span data-ttu-id="962ca-134">Geometria *i* . X1 (linhas InfiniteLine e Ellipse) onde *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="962ca-134">Geometry  *i*  .X1 (InfiniteLine and Ellipse rows)            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="962ca-135">Para obter uma referência à célula X pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="962ca-135">To get a reference to the X cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="962ca-136">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="962ca-136">Section index:</span></span>  <br/> |<span data-ttu-id="962ca-137">**visSectionFirstComponent** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="962ca-137">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="962ca-138">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="962ca-138">Row index:</span></span>  <br/> |<span data-ttu-id="962ca-139">**visRowVertex** +  *j* onde *j* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="962ca-139">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
||<span data-ttu-id="962ca-140">**visRowVertex** (Linhas InfiniteLine e Ellipse)</span><span class="sxs-lookup"><span data-stu-id="962ca-140">**visRowVertex** (InfiniteLine and Ellipse rows)</span></span>  <br/> |
| <span data-ttu-id="962ca-141">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="962ca-141">Cell index:</span></span>  <br/> |<span data-ttu-id="962ca-142">**visX** (Linhas MoveTo, LineTo, ArcTo, EllipticalArcTo, NURBSTo, PolylineTo, SplineStart e SplineKnot)</span><span class="sxs-lookup"><span data-stu-id="962ca-142">**visX** (MoveTo, LineTo, ArcTo, EllipticalArcTo, NURBSTo, Polyline, SplineStart, and SplineKnot rows)</span></span>  <br/> |
||<span data-ttu-id="962ca-143">**visInfiniteLineX1** (Linha InfiniteLine)</span><span class="sxs-lookup"><span data-stu-id="962ca-143">**visInfiniteLineX1** (InfiniteLine row)</span></span>  <br/> |
||<span data-ttu-id="962ca-144">**visEllipseCenterX** (Linha ellipse)</span><span class="sxs-lookup"><span data-stu-id="962ca-144">**visEllipseCenterX** (Ellipse row)</span></span>  <br/> |
   

