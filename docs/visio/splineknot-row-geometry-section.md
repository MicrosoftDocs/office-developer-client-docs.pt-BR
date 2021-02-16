---
title: Linha SplineKnot (Seção Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm3050
localization_priority: Normal
ms.assetid: 9fbae27d-4f1b-c5f7-aacb-16f359331e83
description: Contém coordenadas x e y para o ponto de controle de uma spline e o nó de uma spline.
ms.openlocfilehash: 432b714772d96e0ab0861bbfb62075258404e607
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407414"
---
# <a name="splineknot-row-geometry-section"></a><span data-ttu-id="a4849-103">Linha SplineKnot (Seção Geometry)</span><span class="sxs-lookup"><span data-stu-id="a4849-103">SplineKnot Row (Geometry Section)</span></span>

<span data-ttu-id="a4849-104">Contém  *coordenadas x*  e  *y*  para o ponto de controle de uma spline e o nó de uma spline.</span><span class="sxs-lookup"><span data-stu-id="a4849-104">Contains  *x*  - and  *y*  -coordinates for a spline's control point and a spline's knot.</span></span> 
  
<span data-ttu-id="a4849-105">Uma linha SplineKnot contém as células a seguir.</span><span class="sxs-lookup"><span data-stu-id="a4849-105">A SplineKnot row contains the following cells.</span></span>
  
|<span data-ttu-id="a4849-106">**Célula**</span><span class="sxs-lookup"><span data-stu-id="a4849-106">**Cell**</span></span>|<span data-ttu-id="a4849-107">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="a4849-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a4849-108">X</span><span class="sxs-lookup"><span data-stu-id="a4849-108">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="a4849-109">A  *coordenada x*  de um ponto de controle.</span><span class="sxs-lookup"><span data-stu-id="a4849-109">The  *x*  -coordinate of a control point.</span></span>  <br/> |
|[<span data-ttu-id="a4849-110">Y</span><span class="sxs-lookup"><span data-stu-id="a4849-110">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="a4849-111">A  *coordenada y*  de um ponto de controle.</span><span class="sxs-lookup"><span data-stu-id="a4849-111">The  *y*  -coordinate of a control point.</span></span>  <br/> |
|[<span data-ttu-id="a4849-112">A</span><span class="sxs-lookup"><span data-stu-id="a4849-112">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="a4849-113">Um dos nós da spline (exceto o último ou os dois primeiros).</span><span class="sxs-lookup"><span data-stu-id="a4849-113">One of the spline's knots (other than the last one or the first two).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a4849-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="a4849-114">Remarks</span></span>

<span data-ttu-id="a4849-p101">O Visio exibe a definição de uma spline em uma seção Geometry que contém uma linha SplineStart, seguida de uma ou mais linhas SplineKnot. A linha SplineStart tem que ser precedida de outro tipo de linha, assim como uma linha MoveTo, para indicar o primeiro ponto de controle da spline. A linha precedente pode ser uma linha LineTo, ArcTo, NURBSTo, PolylineTo ou EllipticalArcTo, no caso da spline acompanhar um segmento desse tipo.</span><span class="sxs-lookup"><span data-stu-id="a4849-p101">Visio displays the definition of a spline in a Geometry section that contains a SplineStart row followed by one or more SplineKnot rows. The SplineStart row must be preceded by another kind of row, such as a MoveTo row, to indicate the first control point of the spline. The preceding row can be a LineTo, ArcTo, NURBSTo, PolylineTo, or EllipticalArcTo row if the spline follows a segment of that type.</span></span>
  

