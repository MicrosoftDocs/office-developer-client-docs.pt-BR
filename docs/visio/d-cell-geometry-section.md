---
title: Célula D (Seção Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251753
localization_priority: Normal
ms.assetid: 5f1fdf59-db58-561c-e187-1af72a8b87f2
description: Representa informações diferentes em linhas diferentes. Esta tabela descreve a célula D com base na linha na qual está localizada.
ms.openlocfilehash: a76093f028986907b58175bc6b8c81a7056cfe07
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542496"
---
# <a name="d-cell-geometry-section"></a><span data-ttu-id="7a462-104">Célula D (Seção Geometry)</span><span class="sxs-lookup"><span data-stu-id="7a462-104">D Cell (Geometry Section)</span></span>

<span data-ttu-id="7a462-105">Representa informações diferentes em linhas diferentes.</span><span class="sxs-lookup"><span data-stu-id="7a462-105">Represents different information in different rows.</span></span> <span data-ttu-id="7a462-106">Esta tabela descreve a célula D com base na linha na qual está localizada.</span><span class="sxs-lookup"><span data-stu-id="7a462-106">This table describes the D cell based on the row in which it's located.</span></span>
  
|<span data-ttu-id="7a462-107">Linha</span><span class="sxs-lookup"><span data-stu-id="7a462-107">Row</span></span>|<span data-ttu-id="7a462-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="7a462-108">Description</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7a462-109">EllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="7a462-109">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> | <span data-ttu-id="7a462-p103">A razão entre os eixos principal e secundário de um arco. Apesar do significado comum dessas palavras, o eixo "principal" não precisa ser maior que o eixo "secundário". Logo, a razão não precisa ser maior que 1. Definir esta célula para um valor menor ou igual a 0, ou maior que 1000, pode ocasionar resultados imprevisíveis.</span><span class="sxs-lookup"><span data-stu-id="7a462-p103">The ratio of an arc's major axis to its minor axis. Despite the usual meaning of these words, the "major" axis does not have to be greater than the "minor" axis, so this ratio does not have to be greater than 1. Setting this cell to a value less than or equal to 0 or greater than 1000 can lead to unpredictable results.</span></span>  <br/> |
|[<span data-ttu-id="7a462-113">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="7a462-113">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> | <span data-ttu-id="7a462-114">A primeira espessura da B-spline racional não-uniforme (NURBS).</span><span class="sxs-lookup"><span data-stu-id="7a462-114">The first weight of the nonuniform rational B-spline (NURBS).</span></span>  <br/> |
|[<span data-ttu-id="7a462-115">SplineStart</span><span class="sxs-lookup"><span data-stu-id="7a462-115">SplineStart</span></span>](splinestart-row-geometry-section.md) <br/> | <span data-ttu-id="7a462-116">O grau de uma spline (um inteiro de 1 a 25).</span><span class="sxs-lookup"><span data-stu-id="7a462-116">The degree of a spline (an integer from 1 to 25).</span></span>  <br/> |
|[<span data-ttu-id="7a462-117">Elipse</span><span class="sxs-lookup"><span data-stu-id="7a462-117">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> | <span data-ttu-id="7a462-118">Uma *coordenada y* de um ponto em uma elipse; emparelhada com a coordenada *x* representada pela [célula C.](c-cell-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="7a462-118">A  *y*  -coordinate of a point on an ellipse; paired with the  *x*  -coordinate represented by the [C](c-cell-geometry-section.md) cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7a462-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="7a462-119">Remarks</span></span>

<span data-ttu-id="7a462-120">Para fazer referência à célula D pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="7a462-120">To get a reference to the D cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7a462-121">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="7a462-121">Cell name:</span></span>  <br/> | <span data-ttu-id="7a462-122">Geometry  *i*  . D  *j*            onde  *i*  e  *j*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="7a462-122">Geometry  *i*  .D  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
|| <span data-ttu-id="7a462-123">Geometry  *i*  . D1 (linha Ellipse) onde i =  *<*  1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="7a462-123">Geometry  *i*  .D1 (Ellipse row)            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="7a462-124">Para fazer referência à célula D pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos:</span><span class="sxs-lookup"><span data-stu-id="7a462-124">To get a reference to the D cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7a462-125">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="7a462-125">Section index:</span></span>  <br/> |<span data-ttu-id="7a462-126">**visSectionFirstComponent**  +   *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="7a462-126">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="7a462-127">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="7a462-127">Row index:</span></span>  <br/> |<span data-ttu-id="7a462-128">**visRowVertex**  +   *j* onde *j* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="7a462-128">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
||<span data-ttu-id="7a462-129">**visRowVertex**(linha Ellipse)</span><span class="sxs-lookup"><span data-stu-id="7a462-129">**visRowVertex** (Ellipse row)</span></span>  <br/> |
| <span data-ttu-id="7a462-130">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="7a462-130">Cell index</span></span>  <br/> |<span data-ttu-id="7a462-131">**visAspectRatio**(linha EllipticalArcTo)</span><span class="sxs-lookup"><span data-stu-id="7a462-131">**visAspectRatio** (EllipticalArcTo row)</span></span>  <br/> |
||<span data-ttu-id="7a462-132">**visNURBSWeightPrev**(linha NURBSTo)</span><span class="sxs-lookup"><span data-stu-id="7a462-132">**visNURBSWeightPrev** (NURBSTo row)</span></span>  <br/> |
||<span data-ttu-id="7a462-133">**visSplineDegree**(linha SplineStart)</span><span class="sxs-lookup"><span data-stu-id="7a462-133">**visSplineDegree** (SplineStart row)</span></span>  <br/> |
||<span data-ttu-id="7a462-134">**visEllipseMinorY**(linha Ellipse)</span><span class="sxs-lookup"><span data-stu-id="7a462-134">**visEllipseMinorY** (Ellipse row)</span></span>  <br/> |
   

