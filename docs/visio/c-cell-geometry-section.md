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
ms.openlocfilehash: 5599c09ad3656653c486d7feff9aed2ee89e4614
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413364"
---
# <a name="c-cell-geometry-section"></a><span data-ttu-id="12108-104">Célula C (Seção Geometry)</span><span class="sxs-lookup"><span data-stu-id="12108-104">C Cell (Geometry Section)</span></span>

<span data-ttu-id="12108-105">Representa informações diferentes em linhas diferentes.</span><span class="sxs-lookup"><span data-stu-id="12108-105">Represents different information in different rows.</span></span> <span data-ttu-id="12108-106">Esta tabela descreve a célula C com base na linha na qual está localizada.</span><span class="sxs-lookup"><span data-stu-id="12108-106">This table describes the C cell based on the row in which it's located.</span></span>
  
|<span data-ttu-id="12108-107">**Row**</span><span class="sxs-lookup"><span data-stu-id="12108-107">**Row**</span></span>|<span data-ttu-id="12108-108">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="12108-108">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="12108-109">EllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="12108-109">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> | <span data-ttu-id="12108-110">O ângulo do eixo principal do arco em relação ao eixo *x* de seu pai.</span><span class="sxs-lookup"><span data-stu-id="12108-110">The angle of an arc's major axis relative to the  *x*  -axis of its parent.</span></span>  <br/> |
|[<span data-ttu-id="12108-111">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="12108-111">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> | <span data-ttu-id="12108-112">O primeiro nó da B-spline racional não-uniforme (NURBS).</span><span class="sxs-lookup"><span data-stu-id="12108-112">The first knot of the nonuniform rational B-spline (NURBS).</span></span>  <br/> |
|[<span data-ttu-id="12108-113">SplineStart</span><span class="sxs-lookup"><span data-stu-id="12108-113">SplineStart</span></span>](splinestart-row-geometry-section.md) <br/> | <span data-ttu-id="12108-114">O último nó de uma spline.</span><span class="sxs-lookup"><span data-stu-id="12108-114">The last knot of a spline.</span></span>  <br/> |
|[<span data-ttu-id="12108-115">Elipse</span><span class="sxs-lookup"><span data-stu-id="12108-115">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> | <span data-ttu-id="12108-116">Uma coordenada *x* de um ponto em uma elipse; emparelhado com a coordenada *y* representada pela célula [D](d-cell-geometry-section.md) .</span><span class="sxs-lookup"><span data-stu-id="12108-116">An  *x*  -coordinate of a point on an ellipse; paired with the  *y*  -coordinate represented by the [D](d-cell-geometry-section.md) cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="12108-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="12108-117">Remarks</span></span>

<span data-ttu-id="12108-118">Para fazer referência à célula C pelo nome a partir de outra fórmula ou de um programa que usa a \*\*\*\* propriedade Cells, utilize:</span><span class="sxs-lookup"><span data-stu-id="12108-118">To get a reference to the C cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="12108-119">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="12108-119">Cell name:</span></span>  <br/> | <span data-ttu-id="12108-120">Geometry *i* . C *j* onde *i* e *j* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="12108-120">Geometry  *i*  .C  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
|| <span data-ttu-id="12108-121">Geometry *i* . C1 (linha Ellipse)</span><span class="sxs-lookup"><span data-stu-id="12108-121">Geometry  *i*  .C1 (Ellipse row)</span></span>  <br/> |
   
<span data-ttu-id="12108-122">Para obter uma referência para a célula C pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="12108-122">To get a reference to the C cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="12108-123">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="12108-123">Section index:</span></span>  <br/> |<span data-ttu-id="12108-124">**visSectionFirstComponent** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="12108-124">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="12108-125">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="12108-125">Row index:</span></span>  <br/> |<span data-ttu-id="12108-126">**visRowVertex** +  *j* onde *j* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="12108-126">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
||<span data-ttu-id="12108-127">\*\*visRowVertex \*\*(linha Ellipse)</span><span class="sxs-lookup"><span data-stu-id="12108-127">**visRowVertex** (Ellipse row)</span></span>  <br/> |
| <span data-ttu-id="12108-128">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="12108-128">Cell index:</span></span>  <br/> |<span data-ttu-id="12108-129">**visEccentricityAngle** (Linha EllipticalArcTo)</span><span class="sxs-lookup"><span data-stu-id="12108-129">**visEccentricityAngle** (EllipticalArcTo row)</span></span>  <br/> |
||<span data-ttu-id="12108-130">**visNURBSKnotPrev** (Linha NURBSto)</span><span class="sxs-lookup"><span data-stu-id="12108-130">**visNURBSKnotPrev** (NURBSTo row)</span></span>  <br/> |
||<span data-ttu-id="12108-131">**visSplineKnot3** (Linha SplineStart)</span><span class="sxs-lookup"><span data-stu-id="12108-131">**visSplineKnot3** (SplineStart row)</span></span>  <br/> |
||<span data-ttu-id="12108-132">**visEllipseMinorX** (Linha Ellipse)</span><span class="sxs-lookup"><span data-stu-id="12108-132">**visEllipseMinorX** (Ellipse row)</span></span>  <br/> |
   

