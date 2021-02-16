---
title: Célula C (Seção Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm140
localization_priority: Normal
ms.assetid: d51a1dd8-678a-a34d-658d-bd7a027dd379
description: Representa informações diferentes em linhas diferentes. Esta tabela descreve a célula C com base na linha na qual está localizada.
ms.openlocfilehash: 0284fea02c7eb890b56b6c865a69eb36662d8ae6
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541887"
---
# <a name="c-cell-geometry-section"></a><span data-ttu-id="68f8f-104">Célula C (Seção Geometry)</span><span class="sxs-lookup"><span data-stu-id="68f8f-104">C Cell (Geometry Section)</span></span>

<span data-ttu-id="68f8f-105">Representa informações diferentes em linhas diferentes.</span><span class="sxs-lookup"><span data-stu-id="68f8f-105">Represents different information in different rows.</span></span> <span data-ttu-id="68f8f-106">Esta tabela descreve a célula C com base na linha na qual está localizada.</span><span class="sxs-lookup"><span data-stu-id="68f8f-106">This table describes the C cell based on the row in which it's located.</span></span>
  
|<span data-ttu-id="68f8f-107">Linha</span><span class="sxs-lookup"><span data-stu-id="68f8f-107">Row</span></span>|<span data-ttu-id="68f8f-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="68f8f-108">Description</span></span>|
|:-----|:-----|
|[<span data-ttu-id="68f8f-109">EllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="68f8f-109">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> | <span data-ttu-id="68f8f-110">O ângulo do eixo principal de um arco em relação ao  *eixo x*  de seu pai.</span><span class="sxs-lookup"><span data-stu-id="68f8f-110">The angle of an arc's major axis relative to the  *x*  -axis of its parent.</span></span>  <br/> |
|[<span data-ttu-id="68f8f-111">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="68f8f-111">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> | <span data-ttu-id="68f8f-112">O primeiro nó da B-spline racional não uniforme (NURBS).</span><span class="sxs-lookup"><span data-stu-id="68f8f-112">The first knot of the nonuniform rational B-spline (NURBS).</span></span>  <br/> |
|[<span data-ttu-id="68f8f-113">SplineStart</span><span class="sxs-lookup"><span data-stu-id="68f8f-113">SplineStart</span></span>](splinestart-row-geometry-section.md) <br/> | <span data-ttu-id="68f8f-114">O último nó de uma spline.</span><span class="sxs-lookup"><span data-stu-id="68f8f-114">The last knot of a spline.</span></span>  <br/> |
|[<span data-ttu-id="68f8f-115">Elipse</span><span class="sxs-lookup"><span data-stu-id="68f8f-115">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> | <span data-ttu-id="68f8f-116">Uma *coordenada x* de um ponto em uma elipse; emparelhado com a coordenada *y* representada pela [célula D.](d-cell-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="68f8f-116">An  *x*  -coordinate of a point on an ellipse; paired with the  *y*  -coordinate represented by the [D](d-cell-geometry-section.md) cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="68f8f-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="68f8f-117">Remarks</span></span>

<span data-ttu-id="68f8f-118">Para fazer referência à célula C pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU,** utilize:</span><span class="sxs-lookup"><span data-stu-id="68f8f-118">To get a reference to the C cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="68f8f-119">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="68f8f-119">Cell name:</span></span>  <br/> | <span data-ttu-id="68f8f-120">Geometry  *i*  . C  *j*            onde  *i*  e  *j*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="68f8f-120">Geometry  *i*  .C  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
|| <span data-ttu-id="68f8f-121">Geometry  *i*  . C1 (Linha Ellipse)</span><span class="sxs-lookup"><span data-stu-id="68f8f-121">Geometry  *i*  .C1 (Ellipse row)</span></span>  <br/> |
   
<span data-ttu-id="68f8f-122">Para fazer referência à célula C pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="68f8f-122">To get a reference to the C cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="68f8f-123">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="68f8f-123">Section index:</span></span>  <br/> |<span data-ttu-id="68f8f-124">**visSectionFirstComponent**  +   *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="68f8f-124">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="68f8f-125">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="68f8f-125">Row index:</span></span>  <br/> |<span data-ttu-id="68f8f-126">**visRowVertex**  +   *j* onde *j* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="68f8f-126">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
||<span data-ttu-id="68f8f-127">**visRowVertex**(linha Ellipse)</span><span class="sxs-lookup"><span data-stu-id="68f8f-127">**visRowVertex** (Ellipse row)</span></span>  <br/> |
| <span data-ttu-id="68f8f-128">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="68f8f-128">Cell index:</span></span>  <br/> |<span data-ttu-id="68f8f-129">**visEccentricityAngle** (linha EllipticalArcTo)</span><span class="sxs-lookup"><span data-stu-id="68f8f-129">**visEccentricityAngle** (EllipticalArcTo row)</span></span>  <br/> |
||<span data-ttu-id="68f8f-130">**visNURBSKnotPrev** (linha NURBSTo)</span><span class="sxs-lookup"><span data-stu-id="68f8f-130">**visNURBSKnotPrev** (NURBSTo row)</span></span>  <br/> |
||<span data-ttu-id="68f8f-131">**visSplineKnot3** (linha SplineStart)</span><span class="sxs-lookup"><span data-stu-id="68f8f-131">**visSplineKnot3** (SplineStart row)</span></span>  <br/> |
||<span data-ttu-id="68f8f-132">**visEllipseMinorX** (linha Ellipse)</span><span class="sxs-lookup"><span data-stu-id="68f8f-132">**visEllipseMinorX** (Ellipse row)</span></span>  <br/> |
   

