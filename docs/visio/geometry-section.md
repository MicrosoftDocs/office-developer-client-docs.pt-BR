---
title: Seção Geometry
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm2055
localization_priority: Normal
ms.assetid: 75601a1e-6b1a-27ee-a2bd-69e569315982
description: Contém linhas que listam as coordenadas dos vértices de linhas e arcos que compõem a forma.
ms.openlocfilehash: 59f85c512b7038f6cfddcb657435730a2e724bd6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771954"
---
# <a name="geometry-section"></a><span data-ttu-id="f016c-103">Seção Geometry</span><span class="sxs-lookup"><span data-stu-id="f016c-103">Geometry Section</span></span>

<span data-ttu-id="f016c-104">Contém linhas que listam as coordenadas dos vértices de linhas e arcos que compõem a forma.</span><span class="sxs-lookup"><span data-stu-id="f016c-104">Contains rows that list the coordinates of the vertices for the lines and arcs that make up the shape.</span></span> 
  
<span data-ttu-id="f016c-105">A geometria de uma forma pode ser expressa em várias seções **Geometry** .</span><span class="sxs-lookup"><span data-stu-id="f016c-105">The geometry of a shape can be expressed in multiple **Geometry** sections.</span></span> <span data-ttu-id="f016c-106">Vários caminhos podem ser útil quando vários caminhos tem propriedades diferentes (por exemplo, caminhos de [recorte de imagem](clippingpath-cell-foreign-image-info-section.md) ).</span><span class="sxs-lookup"><span data-stu-id="f016c-106">Multiple paths can be useful when multiple paths have different properties (e.g. [image clipping](clippingpath-cell-foreign-image-info-section.md) paths).</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="f016c-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="f016c-107">Remarks</span></span>

<span data-ttu-id="f016c-108">A seção **Geometry** contém os seguintes tipos de linha.</span><span class="sxs-lookup"><span data-stu-id="f016c-108">The **Geometry** section contains the following row types.</span></span> <span data-ttu-id="f016c-109">Para obter detalhes, consulte os tópicos de linha.</span><span class="sxs-lookup"><span data-stu-id="f016c-109">For details, see the row topics.</span></span> 
  
|<span data-ttu-id="f016c-110">**Row**</span><span class="sxs-lookup"><span data-stu-id="f016c-110">**Row**</span></span>|<span data-ttu-id="f016c-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="f016c-111">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f016c-112">MoveTo</span><span class="sxs-lookup"><span data-stu-id="f016c-112">MoveTo</span></span>](moveto-row-geometry-section.md) <br/> |<span data-ttu-id="f016c-113">Move para uma coordenada.</span><span class="sxs-lookup"><span data-stu-id="f016c-113">Move to a coordinate.</span></span>  <br/> |
|[<span data-ttu-id="f016c-114">LineTo</span><span class="sxs-lookup"><span data-stu-id="f016c-114">LineTo</span></span>](lineto-row-geometry-section.md) <br/> |<span data-ttu-id="f016c-115">Desenha uma linha para uma coordenada.</span><span class="sxs-lookup"><span data-stu-id="f016c-115">Draw a line to a coordinate.</span></span>  <br/> |
|[<span data-ttu-id="f016c-116">ArcTo</span><span class="sxs-lookup"><span data-stu-id="f016c-116">ArcTo</span></span>](arcto-row-geometry-section.md) <br/> |<span data-ttu-id="f016c-117">Desenha um arco circular para uma coordenada.</span><span class="sxs-lookup"><span data-stu-id="f016c-117">Draw a circular arc to a coordinate.</span></span>  <br/> |
|[<span data-ttu-id="f016c-118">EllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="f016c-118">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> |<span data-ttu-id="f016c-119">Desenha um arco elíptico para uma coordenada.</span><span class="sxs-lookup"><span data-stu-id="f016c-119">Draw an elliptical arc to a coordinate.</span></span>  <br/> |
|[<span data-ttu-id="f016c-120">PolylineTo</span><span class="sxs-lookup"><span data-stu-id="f016c-120">PolylineTo</span></span>](polylineto-row-geometry-section.md) <br/> |<span data-ttu-id="f016c-121">Desenha uma polilinha, ou linhas consecutivas, para uma coordenada.</span><span class="sxs-lookup"><span data-stu-id="f016c-121">Draw a polyline, or consecutive lines, to a coordinate.</span></span>  <br/> |
|[<span data-ttu-id="f016c-122">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="f016c-122">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> |<span data-ttu-id="f016c-123">Desenha uma não-uniforme rational B-spline uniforme (NURBS) para uma coordenada.</span><span class="sxs-lookup"><span data-stu-id="f016c-123">Draw a non-uniform rational B-spline (NURBS) to a coordinate.</span></span>  <br/> |
|[<span data-ttu-id="f016c-124">SplineStart</span><span class="sxs-lookup"><span data-stu-id="f016c-124">SplineStart</span></span>](splinestart-row-geometry-section.md) <br/> |<span data-ttu-id="f016c-125">Inicia uma spline.</span><span class="sxs-lookup"><span data-stu-id="f016c-125">Start a spline.</span></span>  <br/> |
|[<span data-ttu-id="f016c-126">SplineKnot</span><span class="sxs-lookup"><span data-stu-id="f016c-126">SplineKnot</span></span>](splineknot-row-geometry-section.md) <br/> |<span data-ttu-id="f016c-127">Desenha um segmento de spline em uma coordenada do nó.</span><span class="sxs-lookup"><span data-stu-id="f016c-127">Draw a spline segment to a knot coordinate.</span></span>  <br/> |
|[<span data-ttu-id="f016c-128">InfiniteLine</span><span class="sxs-lookup"><span data-stu-id="f016c-128">InfiniteLine</span></span>](infiniteline-row-geometry-section.md) <br/> |<span data-ttu-id="f016c-129">Desenha uma linha infinita de uma coordenada para outra.</span><span class="sxs-lookup"><span data-stu-id="f016c-129">Draw an infinite line from one coordinate to another.</span></span>  <br/> |
|[<span data-ttu-id="f016c-130">Elipse</span><span class="sxs-lookup"><span data-stu-id="f016c-130">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> |<span data-ttu-id="f016c-131">Desenha uma elipse a partir de uma coordenada central e um eixo principal/secundário.</span><span class="sxs-lookup"><span data-stu-id="f016c-131">Draw an ellipse from a center coordinate and a major/minor axis.</span></span>  <br/> |
|[<span data-ttu-id="f016c-132">RelCubBezTo</span><span class="sxs-lookup"><span data-stu-id="f016c-132">RelCubBezTo</span></span>](relcubbezto-row-geometry-section.md) <br/> |<span data-ttu-id="f016c-133">Desenhe uma curva de Bézier cúbica em relação a largura e altura da forma.</span><span class="sxs-lookup"><span data-stu-id="f016c-133">Draw a cubic Bezier curve relative to the width and height of the shape.</span></span>  <br/> |
|[<span data-ttu-id="f016c-134">RelEllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="f016c-134">RelEllipticalArcTo</span></span>](relellipticalarcto-row-geometry-section.md) <br/> |<span data-ttu-id="f016c-135">Desenha um arco elíptico para uma coordenada em relação a altura e largura da forma.</span><span class="sxs-lookup"><span data-stu-id="f016c-135">Draw an elliptical arc to a coordinate relative to the height and width of the shape.</span></span>  <br/> |
|[<span data-ttu-id="f016c-136">RelLineTo</span><span class="sxs-lookup"><span data-stu-id="f016c-136">RelLineTo</span></span>](rellineto-row-geometry-section.md) <br/> |<span data-ttu-id="f016c-137">Desenha uma linha para coordenadas relativo a altura e largura de uma forma.</span><span class="sxs-lookup"><span data-stu-id="f016c-137">Draw a line to a coordinate relative the height and width of a shape.</span></span>  <br/> |
|[<span data-ttu-id="f016c-138">RelMoveTo</span><span class="sxs-lookup"><span data-stu-id="f016c-138">RelMoveTo</span></span>](relmoveto-row-geometry-section.md) <br/> |<span data-ttu-id="f016c-139">Move para uma coordenada em relação a largura e altura da forma.</span><span class="sxs-lookup"><span data-stu-id="f016c-139">Move to a coordinate relative to the width and height of the shape.</span></span>  <br/> |
|[<span data-ttu-id="f016c-140">RelQuadBezTo</span><span class="sxs-lookup"><span data-stu-id="f016c-140">RelQuadBezTo</span></span>](relquadbezto-row-geometry-section.md) <br/> |<span data-ttu-id="f016c-141">Desenha uma curva de Bézier quadrática em relação a largura e altura da forma.</span><span class="sxs-lookup"><span data-stu-id="f016c-141">Draws a quadratic Bezier curve relative to the width and height of the shape.</span></span>  <br/> |
   
<span data-ttu-id="f016c-142">Para alterar um tipo de linha nesta seção, clique com o botão direito do mouse na linha e clique em **Alterar Tipo de Linha** no menu de atalho.</span><span class="sxs-lookup"><span data-stu-id="f016c-142">To change a row type in this section, right-click the row, and then click **Change Row Type** on the shortcut menu.</span></span> 
  

