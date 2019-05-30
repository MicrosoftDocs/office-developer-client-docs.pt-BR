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
ms.openlocfilehash: 46c8aa418f495905630fed2833d84afc93945346
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537791"
---
# <a name="b-cell-geometry-section"></a><span data-ttu-id="c4d5d-104">Célula B (Seção Geometry)</span><span class="sxs-lookup"><span data-stu-id="c4d5d-104">B Cell (Geometry Section)</span></span>

<span data-ttu-id="c4d5d-105">Representa informações diferentes em linhas diferentes.</span><span class="sxs-lookup"><span data-stu-id="c4d5d-105">Represents different information in different rows.</span></span> <span data-ttu-id="c4d5d-106">Esta tabela descreve a célula B com base na linha na qual está localizada.</span><span class="sxs-lookup"><span data-stu-id="c4d5d-106">This table describes the B cell based on the row in which it's located.</span></span>
  
|<span data-ttu-id="c4d5d-107">Linha</span><span class="sxs-lookup"><span data-stu-id="c4d5d-107">Row</span></span>|<span data-ttu-id="c4d5d-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="c4d5d-108">Description</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c4d5d-109">EllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="c4d5d-109">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> | <span data-ttu-id="c4d5d-110">A coordenada *y* do ponto de controle de um arco.</span><span class="sxs-lookup"><span data-stu-id="c4d5d-110">The  *y*  -coordinate of an arc's control point.</span></span>  <br/> |
|[<span data-ttu-id="c4d5d-111">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="c4d5d-111">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> | <span data-ttu-id="c4d5d-112">A última espessura da B-spline racional não-uniforme (NURBS).</span><span class="sxs-lookup"><span data-stu-id="c4d5d-112">The last weight of the nonuniform rational B-spline (NURBS).</span></span>  <br/> |
|[<span data-ttu-id="c4d5d-113">SplineStart</span><span class="sxs-lookup"><span data-stu-id="c4d5d-113">SplineStart</span></span>](splinestart-row-geometry-section.md) <br/> | <span data-ttu-id="c4d5d-114">O primeiro nó de uma spline.</span><span class="sxs-lookup"><span data-stu-id="c4d5d-114">The first knot of a spline.</span></span>  <br/> |
|[<span data-ttu-id="c4d5d-115">InfiniteLine</span><span class="sxs-lookup"><span data-stu-id="c4d5d-115">InfiniteLine</span></span>](infiniteline-row-geometry-section.md) <br/> | <span data-ttu-id="c4d5d-116">Uma coordenada *y* de um ponto em uma linha infinita; emparelhado com a coordenada *x* representada pela [](a-cell-geometry-section.md) célula a.</span><span class="sxs-lookup"><span data-stu-id="c4d5d-116">A  *y*  -coordinate of a point on an infinite line; paired with  *x*  -coordinate represented by the [A](a-cell-geometry-section.md) cell.</span></span>  <br/> |
|[<span data-ttu-id="c4d5d-117">Elipse</span><span class="sxs-lookup"><span data-stu-id="c4d5d-117">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> | <span data-ttu-id="c4d5d-118">Uma coordenada *y* de um ponto em uma elipse; emparelhado com a coordenada *x* representada pela [](a-cell-geometry-section.md) célula a.</span><span class="sxs-lookup"><span data-stu-id="c4d5d-118">A  *y*  -coordinate of a point on an ellipse; paired with  *x*  -coordinate represented by the [A](a-cell-geometry-section.md) cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c4d5d-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="c4d5d-119">Remarks</span></span>

<span data-ttu-id="c4d5d-120">Para fazer referência à célula B pelo nome, a partir de outra fórmula ou programa, usando a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="c4d5d-120">To get a reference to the B cell by name from another formula, or from a program, using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c4d5d-121">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="c4d5d-121">Cell name:</span></span>  <br/> | <span data-ttu-id="c4d5d-122">Geometry *i* . B *j* onde *i* e *j* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="c4d5d-122">Geometry  *i*  .B  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
|| <span data-ttu-id="c4d5d-123">Geometry *i* . B1 (linhas InfiniteLine e Ellipse)</span><span class="sxs-lookup"><span data-stu-id="c4d5d-123">Geometry  *i*  .B1 (InfiniteLine and Ellipse rows)</span></span>  <br/> |
   
<span data-ttu-id="c4d5d-124">Para fazer referência à célula B pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="c4d5d-124">To get a reference to the B cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c4d5d-125">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="c4d5d-125">Section index:</span></span>  <br/> |<span data-ttu-id="c4d5d-126">**visSectionFirstComponent** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="c4d5d-126">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="c4d5d-127">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="c4d5d-127">Row index:</span></span>  <br/> |<span data-ttu-id="c4d5d-128">**visRowVertex** +  *j* onde *j* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="c4d5d-128">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
||<span data-ttu-id="c4d5d-129">\*\*visRowVertex \*\*(linhas Ellipse e InfiniteLine)</span><span class="sxs-lookup"><span data-stu-id="c4d5d-129">**visRowVertex** (InfiniteLine and Ellipse rows)</span></span>  <br/> |
| <span data-ttu-id="c4d5d-130">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="c4d5d-130">Cell index:</span></span>  <br/> |<span data-ttu-id="c4d5d-131">**visControlX** (EllipticalArcTo row)</span><span class="sxs-lookup"><span data-stu-id="c4d5d-131">**visControlX** (EllipticalArcTo row)</span></span>  <br/> |
||<span data-ttu-id="c4d5d-132">**visControlY** (linha EllipticalArcTo)</span><span class="sxs-lookup"><span data-stu-id="c4d5d-132">**visControlY** (EllipticalArcTo row)</span></span>  <br/> |
||<span data-ttu-id="c4d5d-133">\*\*visNURBSWeight \*\*(linha NURBSTo)</span><span class="sxs-lookup"><span data-stu-id="c4d5d-133">**visNURBSWeight** (NURBSTo row)</span></span>  <br/> |
||<span data-ttu-id="c4d5d-134">\*\*visSplineKnot2 \*\*(linha SplineStart)</span><span class="sxs-lookup"><span data-stu-id="c4d5d-134">**visSplineKnot2** (SplineStart row)</span></span>  <br/> |
||<span data-ttu-id="c4d5d-135">\*\*visInfiniteLineY2 \*\*(linha InfiniteLine)</span><span class="sxs-lookup"><span data-stu-id="c4d5d-135">**visInfiniteLineY2** (InfiniteLine row)</span></span>  <br/> |
||<span data-ttu-id="c4d5d-136">\*\*visEllipseMajorY \*\*(linha Ellipse)</span><span class="sxs-lookup"><span data-stu-id="c4d5d-136">**visEllipseMajorY** (Ellipse row)</span></span>  <br/> |
   

