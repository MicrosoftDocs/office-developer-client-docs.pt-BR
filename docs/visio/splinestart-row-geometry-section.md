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
description: Contém x e y-coordenadas do segundo ponto de controle de uma spline, seu segundo nó, seu primeiro nó, o último nó e o grau da spline.
ms.openlocfilehash: 0944da12e6090fde41dc5927b5705e103d29f76d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773051"
---
# <a name="splinestart-row-geometry-section"></a><span data-ttu-id="a940e-103">Linha SplineStart (Seção Geometry)</span><span class="sxs-lookup"><span data-stu-id="a940e-103">SplineStart Row (Geometry Section)</span></span>

<span data-ttu-id="a940e-104">Contém *x* e *y* -coordenadas do segundo ponto de controle de uma spline, seu segundo nó, seu primeiro nó, o último nó e o grau da spline.</span><span class="sxs-lookup"><span data-stu-id="a940e-104">Contains  *x*  - and  *y*  -coordinates for a spline's second control point, its second knot, its first knot, the last knot, and the degree of the spline.</span></span> 
  
<span data-ttu-id="a940e-105">Uma linha SplineStart contém as células a seguir.</span><span class="sxs-lookup"><span data-stu-id="a940e-105">A SplineStart row contains the following cells.</span></span>
  
|<span data-ttu-id="a940e-106">**Célula**</span><span class="sxs-lookup"><span data-stu-id="a940e-106">**Cell**</span></span>|<span data-ttu-id="a940e-107">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="a940e-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a940e-108">X</span><span class="sxs-lookup"><span data-stu-id="a940e-108">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="a940e-109">*X* -coordenadas do segundo ponto de controle de uma spline.</span><span class="sxs-lookup"><span data-stu-id="a940e-109">The  *x*  -coordinate of a spline's second control point.</span></span>  <br/> |
|[<span data-ttu-id="a940e-110">Y</span><span class="sxs-lookup"><span data-stu-id="a940e-110">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="a940e-111">*Y* -coordenadas do segundo ponto de controle de uma spline.</span><span class="sxs-lookup"><span data-stu-id="a940e-111">The  *y*  -coordinate of a spline's second control point.</span></span>  <br/> |
|[<span data-ttu-id="a940e-112">A</span><span class="sxs-lookup"><span data-stu-id="a940e-112">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="a940e-113">O segundo nó da spline.</span><span class="sxs-lookup"><span data-stu-id="a940e-113">The second knot of the spline.</span></span>  <br/> |
|[<span data-ttu-id="a940e-114">B</span><span class="sxs-lookup"><span data-stu-id="a940e-114">B</span></span>](b-cell-geometry-section.md) <br/> |<span data-ttu-id="a940e-115">O primeiro nó de uma spline.</span><span class="sxs-lookup"><span data-stu-id="a940e-115">The first knot of a spline.</span></span>  <br/> |
|[<span data-ttu-id="a940e-116">C</span><span class="sxs-lookup"><span data-stu-id="a940e-116">C</span></span>](c-cell-geometry-section.md) <br/> |<span data-ttu-id="a940e-117">O último nó de uma spline.</span><span class="sxs-lookup"><span data-stu-id="a940e-117">The last knot of a spline.</span></span>  <br/> |
|[<span data-ttu-id="a940e-118">D</span><span class="sxs-lookup"><span data-stu-id="a940e-118">D</span></span>](d-cell-geometry-section.md) <br/> |<span data-ttu-id="a940e-119">O grau de uma spline (um inteiro de 1 a 25).</span><span class="sxs-lookup"><span data-stu-id="a940e-119">The degree of a spline (an integer from 1 to 25).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a940e-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="a940e-120">Remarks</span></span>

<span data-ttu-id="a940e-p101">O Visio exibe a definição de uma spline em uma seção Geometry que contém uma linha SplineStart, seguida de uma ou mais linhas SplineKnot. A linha SplineStart tem que ser precedida de outro tipo de linha, assim como uma linha MoveTo, para indicar o primeiro ponto de controle da spline. A linha precedente pode ser uma linha LineTo, ArcTo, NURBSTo, PolylineTo ou EllipticalArcTo, no caso da spline acompanhar um segmento desse tipo.</span><span class="sxs-lookup"><span data-stu-id="a940e-p101">Visio displays the definition of a spline in a Geometry section that contains a SplineStart row followed by one or more SplineKnot rows. The SplineStart row must be preceded by another kind of row, such as a MoveTo row, to indicate the first control point of the spline. The preceding row can be a LineTo, ArcTo, NURBSTo, PolylineTo, or EllipticalArcTo row if the spline follows a segment of that type.</span></span>
  

