---
title: Linha SplineStart (Seção Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm3055
localization_priority: Normal
ms.assetid: 8e327e00-0844-efa4-900b-6954d3b009bb
description: Contém as coordenadas x e y para o segundo ponto de controle de uma spline, seu segundo nó, seu primeiro nó, o último nó e o grau da spline.
ms.openlocfilehash: 2ec06619770af4e5dbcc1a763595b6e01a39052b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417473"
---
# <a name="splinestart-row-geometry-section"></a><span data-ttu-id="fd9ad-103">Linha SplineStart (Seção Geometry)</span><span class="sxs-lookup"><span data-stu-id="fd9ad-103">SplineStart Row (Geometry Section)</span></span>

<span data-ttu-id="fd9ad-104">Contém as coordenadas *x* e *y* para o segundo ponto de controle de uma spline, seu segundo nó, seu primeiro nó, o último nó e o grau da spline.</span><span class="sxs-lookup"><span data-stu-id="fd9ad-104">Contains  *x*  - and  *y*  -coordinates for a spline's second control point, its second knot, its first knot, the last knot, and the degree of the spline.</span></span> 
  
<span data-ttu-id="fd9ad-105">Uma linha SplineStart contém as células a seguir.</span><span class="sxs-lookup"><span data-stu-id="fd9ad-105">A SplineStart row contains the following cells.</span></span>
  
|<span data-ttu-id="fd9ad-106">**Célula**</span><span class="sxs-lookup"><span data-stu-id="fd9ad-106">**Cell**</span></span>|<span data-ttu-id="fd9ad-107">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="fd9ad-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fd9ad-108">X</span><span class="sxs-lookup"><span data-stu-id="fd9ad-108">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="fd9ad-109">A coordenada *x* do segundo ponto de controle de uma spline.</span><span class="sxs-lookup"><span data-stu-id="fd9ad-109">The  *x*  -coordinate of a spline's second control point.</span></span>  <br/> |
|[<span data-ttu-id="fd9ad-110">Y</span><span class="sxs-lookup"><span data-stu-id="fd9ad-110">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="fd9ad-111">A coordenada *y* do segundo ponto de controle de uma spline.</span><span class="sxs-lookup"><span data-stu-id="fd9ad-111">The  *y*  -coordinate of a spline's second control point.</span></span>  <br/> |
|[<span data-ttu-id="fd9ad-112">A</span><span class="sxs-lookup"><span data-stu-id="fd9ad-112">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="fd9ad-113">O segundo nó da spline.</span><span class="sxs-lookup"><span data-stu-id="fd9ad-113">The second knot of the spline.</span></span>  <br/> |
|[<span data-ttu-id="fd9ad-114">A.b.c.</span><span class="sxs-lookup"><span data-stu-id="fd9ad-114">B</span></span>](b-cell-geometry-section.md) <br/> |<span data-ttu-id="fd9ad-115">O primeiro nó de uma spline.</span><span class="sxs-lookup"><span data-stu-id="fd9ad-115">The first knot of a spline.</span></span>  <br/> |
|[<span data-ttu-id="fd9ad-116">Unidade</span><span class="sxs-lookup"><span data-stu-id="fd9ad-116">C</span></span>](c-cell-geometry-section.md) <br/> |<span data-ttu-id="fd9ad-117">O último nó de uma spline.</span><span class="sxs-lookup"><span data-stu-id="fd9ad-117">The last knot of a spline.</span></span>  <br/> |
|[<span data-ttu-id="fd9ad-118">D</span><span class="sxs-lookup"><span data-stu-id="fd9ad-118">D</span></span>](d-cell-geometry-section.md) <br/> |<span data-ttu-id="fd9ad-119">O grau de uma spline (um inteiro de 1 a 25).</span><span class="sxs-lookup"><span data-stu-id="fd9ad-119">The degree of a spline (an integer from 1 to 25).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fd9ad-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="fd9ad-120">Remarks</span></span>

<span data-ttu-id="fd9ad-p101">O Visio exibe a definição de uma spline em uma seção Geometry que contém uma linha SplineStart, seguida de uma ou mais linhas SplineKnot. A linha SplineStart tem que ser precedida de outro tipo de linha, assim como uma linha MoveTo, para indicar o primeiro ponto de controle da spline. A linha precedente pode ser uma linha LineTo, ArcTo, NURBSTo, PolylineTo ou EllipticalArcTo, no caso da spline acompanhar um segmento desse tipo.</span><span class="sxs-lookup"><span data-stu-id="fd9ad-p101">Visio displays the definition of a spline in a Geometry section that contains a SplineStart row followed by one or more SplineKnot rows. The SplineStart row must be preceded by another kind of row, such as a MoveTo row, to indicate the first control point of the spline. The preceding row can be a LineTo, ArcTo, NURBSTo, PolylineTo, or EllipticalArcTo row if the spline follows a segment of that type.</span></span>
  

