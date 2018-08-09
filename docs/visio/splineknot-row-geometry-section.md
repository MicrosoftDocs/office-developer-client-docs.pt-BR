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
description: Contém x e y-coordenadas do ponto de controle de uma spline e o nó de uma spline.
ms.openlocfilehash: 297889208e064870dd37ed45a17fef7cb4b333b7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773049"
---
# <a name="splineknot-row-geometry-section"></a><span data-ttu-id="097d4-103">Linha SplineKnot (Seção Geometry)</span><span class="sxs-lookup"><span data-stu-id="097d4-103">SplineKnot Row (Geometry Section)</span></span>

<span data-ttu-id="097d4-104">Contém *x* e *y* -coordenadas do ponto de controle de uma spline e o nó de uma spline.</span><span class="sxs-lookup"><span data-stu-id="097d4-104">Contains  *x*  - and  *y*  -coordinates for a spline's control point and a spline's knot.</span></span> 
  
<span data-ttu-id="097d4-105">Uma linha SplineKnot contém as células a seguir.</span><span class="sxs-lookup"><span data-stu-id="097d4-105">A SplineKnot row contains the following cells.</span></span>
  
|<span data-ttu-id="097d4-106">**Célula**</span><span class="sxs-lookup"><span data-stu-id="097d4-106">**Cell**</span></span>|<span data-ttu-id="097d4-107">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="097d4-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="097d4-108">X</span><span class="sxs-lookup"><span data-stu-id="097d4-108">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="097d4-109">*X* -coordenadas de um ponto de controle.</span><span class="sxs-lookup"><span data-stu-id="097d4-109">The  *x*  -coordinate of a control point.</span></span>  <br/> |
|[<span data-ttu-id="097d4-110">Y</span><span class="sxs-lookup"><span data-stu-id="097d4-110">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="097d4-111">*Y* -coordenadas de um ponto de controle.</span><span class="sxs-lookup"><span data-stu-id="097d4-111">The  *y*  -coordinate of a control point.</span></span>  <br/> |
|[<span data-ttu-id="097d4-112">A</span><span class="sxs-lookup"><span data-stu-id="097d4-112">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="097d4-113">Um dos nós da spline (exceto o último ou os dois primeiros).</span><span class="sxs-lookup"><span data-stu-id="097d4-113">One of the spline's knots (other than the last one or the first two).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="097d4-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="097d4-114">Remarks</span></span>

<span data-ttu-id="097d4-p101">O Visio exibe a definição de uma spline em uma seção Geometry que contém uma linha SplineStart, seguida de uma ou mais linhas SplineKnot. A linha SplineStart tem que ser precedida de outro tipo de linha, assim como uma linha MoveTo, para indicar o primeiro ponto de controle da spline. A linha precedente pode ser uma linha LineTo, ArcTo, NURBSTo, PolylineTo ou EllipticalArcTo, no caso da spline acompanhar um segmento desse tipo.</span><span class="sxs-lookup"><span data-stu-id="097d4-p101">Visio displays the definition of a spline in a Geometry section that contains a SplineStart row followed by one or more SplineKnot rows. The SplineStart row must be preceded by another kind of row, such as a MoveTo row, to indicate the first control point of the spline. The preceding row can be a LineTo, ArcTo, NURBSTo, PolylineTo, or EllipticalArcTo row if the spline follows a segment of that type.</span></span>
  

