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
ms.openlocfilehash: ed67197e46ee159ba2175b0e86623fe1704992d2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771632"
---
# <a name="d-cell-geometry-section"></a><span data-ttu-id="b70ea-104">Célula D (Seção Geometry)</span><span class="sxs-lookup"><span data-stu-id="b70ea-104">D Cell (Geometry Section)</span></span>

<span data-ttu-id="b70ea-p102">Representa informações diferentes em linhas diferentes. Esta tabela descreve a célula D com base na linha na qual está localizada.</span><span class="sxs-lookup"><span data-stu-id="b70ea-p102">Represents different information in different rows. This table describes the D cell based on the row in which it's located.</span></span>
  
|<span data-ttu-id="b70ea-107">**Row**</span><span class="sxs-lookup"><span data-stu-id="b70ea-107">**Row**</span></span>|<span data-ttu-id="b70ea-108">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="b70ea-108">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b70ea-109">EllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="b70ea-109">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> | <span data-ttu-id="b70ea-p103">A razão entre os eixos principal e secundário de um arco. Apesar do significado comum dessas palavras, o eixo "principal" não precisa ser maior que o eixo "secundário". Logo, a razão não precisa ser maior que 1. Definir esta célula para um valor menor ou igual a 0, ou maior que 1000, pode ocasionar resultados imprevisíveis.</span><span class="sxs-lookup"><span data-stu-id="b70ea-p103">The ratio of an arc's major axis to its minor axis. Despite the usual meaning of these words, the "major" axis does not have to be greater than the "minor" axis, so this ratio does not have to be greater than 1. Setting this cell to a value less than or equal to 0 or greater than 1000 can lead to unpredictable results.</span></span>  <br/> |
|[<span data-ttu-id="b70ea-113">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="b70ea-113">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> | <span data-ttu-id="b70ea-114">A primeira espessura da B-spline racional não-uniforme (NURBS).</span><span class="sxs-lookup"><span data-stu-id="b70ea-114">The first weight of the nonuniform rational B-spline (NURBS).</span></span>  <br/> |
|[<span data-ttu-id="b70ea-115">SplineStart</span><span class="sxs-lookup"><span data-stu-id="b70ea-115">SplineStart</span></span>](splinestart-row-geometry-section.md) <br/> | <span data-ttu-id="b70ea-116">O grau de uma spline (um inteiro de 1 a 25).</span><span class="sxs-lookup"><span data-stu-id="b70ea-116">The degree of a spline (an integer from 1 to 25).</span></span>  <br/> |
|[<span data-ttu-id="b70ea-117">Elipse</span><span class="sxs-lookup"><span data-stu-id="b70ea-117">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> | <span data-ttu-id="b70ea-118">Um *y* -coordenadas de um ponto em um elipse, juntamente com o *x* -coordenada representada pela célula [C](c-cell-geometry-section.md) .</span><span class="sxs-lookup"><span data-stu-id="b70ea-118">A  *y*  -coordinate of a point on an ellipse; paired with the  *x*  -coordinate represented by the [C](c-cell-geometry-section.md) cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b70ea-119">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="b70ea-119">Remarks</span></span>

<span data-ttu-id="b70ea-120">Para obter uma referência à célula D pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="b70ea-120">To get a reference to the D cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b70ea-121">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="b70ea-121">Cell name:</span></span>  <br/> | <span data-ttu-id="b70ea-122">Geometria *i* . D *j* onde *i* e *j* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="b70ea-122">Geometry  *i*  .D  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
|| <span data-ttu-id="b70ea-123">Geometria *i* . D1 (linha Ellipse) onde *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="b70ea-123">Geometry  *i*  .D1 (Ellipse row)            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="b70ea-124">Para obter uma referência à célula D pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="b70ea-124">To get a reference to the D cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b70ea-125">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="b70ea-125">Section index:</span></span>  <br/> |<span data-ttu-id="b70ea-126">**visSectionFirstComponent** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="b70ea-126">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="b70ea-127">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="b70ea-127">Row index:</span></span>  <br/> |<span data-ttu-id="b70ea-128">**visRowVertex** +  *j* onde *j* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="b70ea-128">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
||<span data-ttu-id="b70ea-129">**visRowVertex** (Linha ellipse)</span><span class="sxs-lookup"><span data-stu-id="b70ea-129">**visRowVertex** (Ellipse row)</span></span>  <br/> |
| <span data-ttu-id="b70ea-130">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="b70ea-130">Cell index</span></span>  <br/> |<span data-ttu-id="b70ea-131">**visAspectRatio** (Linha EllipticalArcTo)</span><span class="sxs-lookup"><span data-stu-id="b70ea-131">**visAspectRatio** (EllipticalArcTo row)</span></span>  <br/> |
||<span data-ttu-id="b70ea-132">**visNURBSWeightPrev** (Linha NURBSTo)</span><span class="sxs-lookup"><span data-stu-id="b70ea-132">**visNURBSWeightPrev** (NURBSTo row)</span></span>  <br/> |
||<span data-ttu-id="b70ea-133">**visSplineDegree** (Linha SplineStart)</span><span class="sxs-lookup"><span data-stu-id="b70ea-133">**visSplineDegree** (SplineStart row)</span></span>  <br/> |
||<span data-ttu-id="b70ea-134">**visEllipseMinorY** (Linha ellipse)</span><span class="sxs-lookup"><span data-stu-id="b70ea-134">**visEllipseMinorY** (Ellipse row)</span></span>  <br/> |
   

