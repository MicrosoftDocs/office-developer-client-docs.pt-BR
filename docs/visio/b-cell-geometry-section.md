---
title: Célula B (Seção Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251751
localization_priority: Normal
ms.assetid: b0fb6a47-47d8-ab9c-854d-0b0bbfdfcc27
description: Representa informações diferentes em linhas diferentes. Esta tabela descreve a célula B com base na linha na qual está localizada.
ms.openlocfilehash: 7d6f51d037be4852c6a101ad6e576a3a13488cb7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771290"
---
# <a name="b-cell-geometry-section"></a><span data-ttu-id="bf07e-104">Célula B (Seção Geometry)</span><span class="sxs-lookup"><span data-stu-id="bf07e-104">B Cell (Geometry Section)</span></span>

<span data-ttu-id="bf07e-p102">Representa informações diferentes em linhas diferentes. Esta tabela descreve a célula B com base na linha na qual está localizada.</span><span class="sxs-lookup"><span data-stu-id="bf07e-p102">Represents different information in different rows. This table describes the B cell based on the row in which it's located.</span></span>
  
|<span data-ttu-id="bf07e-107">**Row**</span><span class="sxs-lookup"><span data-stu-id="bf07e-107">**Row**</span></span>|<span data-ttu-id="bf07e-108">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="bf07e-108">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bf07e-109">EllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="bf07e-109">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> | <span data-ttu-id="bf07e-110">*Y* -coordenadas do ponto de controle do arco.</span><span class="sxs-lookup"><span data-stu-id="bf07e-110">The  *y*  -coordinate of an arc's control point.</span></span>  <br/> |
|[<span data-ttu-id="bf07e-111">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="bf07e-111">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> | <span data-ttu-id="bf07e-112">A última espessura da B-spline racional não-uniforme (NURBS).</span><span class="sxs-lookup"><span data-stu-id="bf07e-112">The last weight of the nonuniform rational B-spline (NURBS).</span></span>  <br/> |
|[<span data-ttu-id="bf07e-113">SplineStart</span><span class="sxs-lookup"><span data-stu-id="bf07e-113">SplineStart</span></span>](splinestart-row-geometry-section.md) <br/> | <span data-ttu-id="bf07e-114">O primeiro nó de uma spline.</span><span class="sxs-lookup"><span data-stu-id="bf07e-114">The first knot of a spline.</span></span>  <br/> |
|[<span data-ttu-id="bf07e-115">InfiniteLine</span><span class="sxs-lookup"><span data-stu-id="bf07e-115">InfiniteLine</span></span>](infiniteline-row-geometry-section.md) <br/> | <span data-ttu-id="bf07e-116">Um *y* -coordenadas de um ponto em uma linha infinita; juntamente com *x* -coordenada representada pela célula [A](a-cell-geometry-section.md) .</span><span class="sxs-lookup"><span data-stu-id="bf07e-116">A  *y*  -coordinate of a point on an infinite line; paired with  *x*  -coordinate represented by the [A](a-cell-geometry-section.md) cell.</span></span>  <br/> |
|[<span data-ttu-id="bf07e-117">Elipse</span><span class="sxs-lookup"><span data-stu-id="bf07e-117">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> | <span data-ttu-id="bf07e-118">Um *y* -coordenadas de um ponto em um elipse, juntamente com *x* -coordenada representada pela célula [A](a-cell-geometry-section.md) .</span><span class="sxs-lookup"><span data-stu-id="bf07e-118">A  *y*  -coordinate of a point on an ellipse; paired with  *x*  -coordinate represented by the [A](a-cell-geometry-section.md) cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bf07e-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="bf07e-119">Remarks</span></span>

<span data-ttu-id="bf07e-120">Para fazer referência à célula B pelo nome, a partir de outra fórmula ou programa, usando a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="bf07e-120">To get a reference to the B cell by name from another formula, or from a program, using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bf07e-121">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="bf07e-121">Cell name:</span></span>  <br/> | <span data-ttu-id="bf07e-122">Geometria *i* . B *j* onde *i* e *j* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="bf07e-122">Geometry  *i*  .B  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
|| <span data-ttu-id="bf07e-123">Geometria *i* . B1 (linhas InfiniteLine e Ellipse)</span><span class="sxs-lookup"><span data-stu-id="bf07e-123">Geometry  *i*  .B1 (InfiniteLine and Ellipse rows)</span></span>  <br/> |
   
<span data-ttu-id="bf07e-124">Para fazer referência à célula B pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="bf07e-124">To get a reference to the B cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bf07e-125">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="bf07e-125">Section index:</span></span>  <br/> |<span data-ttu-id="bf07e-126">**visSectionFirstComponent** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="bf07e-126">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="bf07e-127">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="bf07e-127">Row index:</span></span>  <br/> |<span data-ttu-id="bf07e-128">**visRowVertex** +  *j* onde *j* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="bf07e-128">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
||<span data-ttu-id="bf07e-129">**visRowVertex **(linhas Ellipse e InfiniteLine)</span><span class="sxs-lookup"><span data-stu-id="bf07e-129">**visRowVertex** (InfiniteLine and Ellipse rows)</span></span>  <br/> |
| <span data-ttu-id="bf07e-130">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="bf07e-130">Cell index:</span></span>  <br/> |<span data-ttu-id="bf07e-131">**visControlX** (EllipticalArcTo row)</span><span class="sxs-lookup"><span data-stu-id="bf07e-131">**visControlX** (EllipticalArcTo row)</span></span>  <br/> |
||<span data-ttu-id="bf07e-132">**visControlY** (linha EllipticalArcTo)</span><span class="sxs-lookup"><span data-stu-id="bf07e-132">**visControlY** (EllipticalArcTo row)</span></span>  <br/> |
||<span data-ttu-id="bf07e-133">**visNURBSWeight **(linha NURBSTo)</span><span class="sxs-lookup"><span data-stu-id="bf07e-133">**visNURBSWeight** (NURBSTo row)</span></span>  <br/> |
||<span data-ttu-id="bf07e-134">**visSplineKnot2 **(linha SplineStart)</span><span class="sxs-lookup"><span data-stu-id="bf07e-134">**visSplineKnot2** (SplineStart row)</span></span>  <br/> |
||<span data-ttu-id="bf07e-135">**visInfiniteLineY2 **(linha InfiniteLine)</span><span class="sxs-lookup"><span data-stu-id="bf07e-135">**visInfiniteLineY2** (InfiniteLine row)</span></span>  <br/> |
||<span data-ttu-id="bf07e-136">**visEllipseMajorY **(linha Ellipse)</span><span class="sxs-lookup"><span data-stu-id="bf07e-136">**visEllipseMajorY** (Ellipse row)</span></span>  <br/> |
   

