---
title: Linha RelQuadBezTo (seção geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ae57707-5a50-43f0-8c78-516790b5034e
description: Contém as coordenadas x e y do ponto de extremidade de uma curva de Bézier quadrática em relação à largura e altura da forma e às coordenadas x e y do ponto de controle da largura e altura da forma relativa da curva.
ms.openlocfilehash: f517fa006c6630a26e9162adfbb1be2139487e63
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423353"
---
# <a name="relquadbezto-row-geometry-section"></a><span data-ttu-id="ea138-103">Linha RelQuadBezTo (seção geometry)</span><span class="sxs-lookup"><span data-stu-id="ea138-103">RelQuadBezTo Row (Geometry Section)</span></span>

<span data-ttu-id="ea138-104">Contém as coordenadas *x* e *y* do ponto de extremidade de uma curva de Bézier quadrática em relação à largura e altura da forma e às coordenadas *x* e *y* do ponto de controle da largura e altura da forma relativa da curva.</span><span class="sxs-lookup"><span data-stu-id="ea138-104">Contains the  *x*  - and  *y*  -coordinates of the endpoint of a quadratic Bézier curve relative to the shape's width and height and the  *x*  - and  *y*  -coordinates of the control point of the curve relative shape's width and height.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="ea138-105">Uma linha **RelQuadBezTo** só pode persistir nos formatos de arquivo. vsdx,. vsdm,. vstx,. VSTM,. vssx e. vssm.</span><span class="sxs-lookup"><span data-stu-id="ea138-105">A **RelQuadBezTo** row can only be persisted in the .vsdx, .vsdm, .vstx, .vstm, .vssx, and .vssm file formats.</span></span> <span data-ttu-id="ea138-106">Quando um arquivo é salvo nos formatos do Visio 2003-2010, a linha **RelQuadBezTo** é convertida em uma linha [nurbsto](nurbsto-row-geometry-section.md) .</span><span class="sxs-lookup"><span data-stu-id="ea138-106">When a file is saved to the Visio 2003-2010 formats, the **RelQuadBezTo** row is converted to a [NURBSTo](nurbsto-row-geometry-section.md) row.</span></span> 
  
<span data-ttu-id="ea138-107">Uma linha **RelQuadBezTo** contém as células a seguir.</span><span class="sxs-lookup"><span data-stu-id="ea138-107">A **RelQuadBezTo** row contains the following cells.</span></span> 
  
|<span data-ttu-id="ea138-108">**Célula**</span><span class="sxs-lookup"><span data-stu-id="ea138-108">**Cell**</span></span>|<span data-ttu-id="ea138-109">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="ea138-109">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ea138-110">X</span><span class="sxs-lookup"><span data-stu-id="ea138-110">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="ea138-111">A coordenada *x* do vértice final de uma curva de Bézier quadrática em relação à largura da forma.</span><span class="sxs-lookup"><span data-stu-id="ea138-111">The  *x*  -coordinate of the ending vertex of a quadratic Bézier curve relative to the width of the shape.</span></span>  <br/> |
|[<span data-ttu-id="ea138-112">Y</span><span class="sxs-lookup"><span data-stu-id="ea138-112">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="ea138-113">A coordenada *y* do vértice final de uma curva de Bézier quadrática em relação à altura da forma.</span><span class="sxs-lookup"><span data-stu-id="ea138-113">The  *y*  -coordinate of the ending vertex of a quadratic Bézier curve relative to the height of the shape.</span></span>  <br/> |
|[<span data-ttu-id="ea138-114">A</span><span class="sxs-lookup"><span data-stu-id="ea138-114">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="ea138-115">A coordenada *x* do ponto de controle da curva em relação à largura da forma; um ponto no arco. O ponto de controle é melhor localizado sobre a metade entre os vértices inicial e final do arco.</span><span class="sxs-lookup"><span data-stu-id="ea138-115">The  *x*  -coordinate of the curve's control point relative to the shape's width; a point on the arc. The control point is best located about halfway between the beginning and ending vertices of the arc.</span></span>  <br/> |
|[<span data-ttu-id="ea138-116">A.b.c.</span><span class="sxs-lookup"><span data-stu-id="ea138-116">B</span></span>](b-cell-geometry-section.md) <br/> |<span data-ttu-id="ea138-117">A coordenada *y* do ponto de controle de uma curva em relação à altura da forma.</span><span class="sxs-lookup"><span data-stu-id="ea138-117">The  *y*  -coordinate of a curve's control point relative to the shape's height.</span></span>  <br/> |
   

