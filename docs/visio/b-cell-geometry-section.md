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
# <a name="b-cell-geometry-section"></a><span data-ttu-id="ee9fa-104">Célula B (Seção Geometry)</span><span class="sxs-lookup"><span data-stu-id="ee9fa-104">B Cell (Geometry Section)</span></span>

<span data-ttu-id="ee9fa-p102">Representa informações diferentes em linhas diferentes. Esta tabela descreve a célula B com base na linha na qual está localizada.</span><span class="sxs-lookup"><span data-stu-id="ee9fa-p102">Represents different information in different rows. This table describes the B cell based on the row in which it's located.</span></span>
  
|<span data-ttu-id="ee9fa-107">**Row**</span><span class="sxs-lookup"><span data-stu-id="ee9fa-107">**Row**</span></span>|<span data-ttu-id="ee9fa-108">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="ee9fa-108">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ee9fa-109">EllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="ee9fa-109">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> | <span data-ttu-id="ee9fa-110">*Y* -coordenadas do ponto de controle do arco.</span><span class="sxs-lookup"><span data-stu-id="ee9fa-110">The  *y*  -coordinate of an arc's control point.</span></span>  <br/> |
|[<span data-ttu-id="ee9fa-111">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="ee9fa-111">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> | <span data-ttu-id="ee9fa-112">A última espessura da B-spline racional não-uniforme (NURBS).</span><span class="sxs-lookup"><span data-stu-id="ee9fa-112">The last weight of the nonuniform rational B-spline (NURBS).</span></span>  <br/> |
|[<span data-ttu-id="ee9fa-113">SplineStart</span><span class="sxs-lookup"><span data-stu-id="ee9fa-113">SplineStart</span></span>](splinestart-row-geometry-section.md) <br/> | <span data-ttu-id="ee9fa-114">O primeiro nó de uma spline.</span><span class="sxs-lookup"><span data-stu-id="ee9fa-114">The first knot of a spline.</span></span>  <br/> |
|[<span data-ttu-id="ee9fa-115">InfiniteLine</span><span class="sxs-lookup"><span data-stu-id="ee9fa-115">InfiniteLine</span></span>](infiniteline-row-geometry-section.md) <br/> | <span data-ttu-id="ee9fa-116">Um *y* -coordenadas de um ponto em uma linha infinita; juntamente com *x* -coordenada representada pela célula [A](a-cell-geometry-section.md) .</span><span class="sxs-lookup"><span data-stu-id="ee9fa-116">A  *y*  -coordinate of a point on an infinite line; paired with  *x*  -coordinate represented by the [A](a-cell-geometry-section.md) cell.</span></span>  <br/> |
|[<span data-ttu-id="ee9fa-117">Elipse</span><span class="sxs-lookup"><span data-stu-id="ee9fa-117">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> | <span data-ttu-id="ee9fa-118">Um *y* -coordenadas de um ponto em um elipse, juntamente com *x* -coordenada representada pela célula [A](a-cell-geometry-section.md) .</span><span class="sxs-lookup"><span data-stu-id="ee9fa-118">A  *y*  -coordinate of a point on an ellipse; paired with  *x*  -coordinate represented by the [A](a-cell-geometry-section.md) cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ee9fa-119">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="ee9fa-119">Remarks</span></span>

<span data-ttu-id="ee9fa-120">Para fazer referência à célula B pelo nome, a partir de outra fórmula ou de um programa, use a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="ee9fa-120">To get a reference to the B cell by name from another formula, or from a program, using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ee9fa-121">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="ee9fa-121">Cell name:</span></span>  <br/> | <span data-ttu-id="ee9fa-122">Geometria *i* . B *j* onde *i* e *j* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="ee9fa-122">Geometry  *i*  .B  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
|| <span data-ttu-id="ee9fa-123">Geometria *i* . B1 (linhas InfiniteLine e Ellipse)</span><span class="sxs-lookup"><span data-stu-id="ee9fa-123">Geometry  *i*  .B1 (InfiniteLine and Ellipse rows)</span></span>  <br/> |
   
<span data-ttu-id="ee9fa-124">Para obter uma referência à célula B pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="ee9fa-124">To get a reference to the B cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ee9fa-125">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="ee9fa-125">Section index:</span></span>  <br/> |<span data-ttu-id="ee9fa-126">**visSectionFirstComponent** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="ee9fa-126">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="ee9fa-127">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="ee9fa-127">Row index:</span></span>  <br/> |<span data-ttu-id="ee9fa-128">**visRowVertex** +  *j* onde *j* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="ee9fa-128">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
||<span data-ttu-id="ee9fa-129">**visRowVertex** (Linhas InfiniteLine e Ellipse)</span><span class="sxs-lookup"><span data-stu-id="ee9fa-129">**visRowVertex** (InfiniteLine and Ellipse rows)</span></span>  <br/> |
| <span data-ttu-id="ee9fa-130">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="ee9fa-130">Cell index:</span></span>  <br/> |<span data-ttu-id="ee9fa-131">**visControlX** (Linha EllipticalArcTo)</span><span class="sxs-lookup"><span data-stu-id="ee9fa-131">**visControlX** (EllipticalArcTo row)</span></span>  <br/> |
||<span data-ttu-id="ee9fa-132">**visControlY** (Linha EllipticalArcTo)</span><span class="sxs-lookup"><span data-stu-id="ee9fa-132">**visControlY** (EllipticalArcTo row)</span></span>  <br/> |
||<span data-ttu-id="ee9fa-133">**visNURBSWeight** (Linha NURBSTo)</span><span class="sxs-lookup"><span data-stu-id="ee9fa-133">**visNURBSWeight** (NURBSTo row)</span></span>  <br/> |
||<span data-ttu-id="ee9fa-134">**visSplineKnot2** (Linha SplineStart)</span><span class="sxs-lookup"><span data-stu-id="ee9fa-134">**visSplineKnot2** (SplineStart row)</span></span>  <br/> |
||<span data-ttu-id="ee9fa-135">**visInfiniteLineY2** (Linha InfiniteLine)</span><span class="sxs-lookup"><span data-stu-id="ee9fa-135">**visInfiniteLineY2** (InfiniteLine row)</span></span>  <br/> |
||<span data-ttu-id="ee9fa-136">**visEllipseMajorY** (Linha ellipse)</span><span class="sxs-lookup"><span data-stu-id="ee9fa-136">**visEllipseMajorY** (Ellipse row)</span></span>  <br/> |
   

