---
title: Linha RelCubBezTo (seção geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 77777dd4-5a2c-4048-9ea4-9bd876862963
description: Contém as coordenadas x e y do ponto de extremidade de uma curva Bézier cúbica em relação à largura e à altura da forma, as coordenadas x e y do ponto de controle do início da largura e altura da forma relativa da curva e as coordenadas x e y do contro ponto l do final da largura e altura da forma relativa da curva.
ms.openlocfilehash: cb886706c4c5cbb3488a95b57dcc84e0e45ee326
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320031"
---
# <a name="relcubbezto-row-geometry-section"></a><span data-ttu-id="1846b-103">Linha RelCubBezTo (seção geometry)</span><span class="sxs-lookup"><span data-stu-id="1846b-103">RelCubBezTo Row (Geometry Section)</span></span>

<span data-ttu-id="1846b-104">Contém as coordenadas *x* e *y* do ponto de extremidade de uma curva Bézier cúbica em relação à largura e altura da forma, as coordenadas *x* e *y* do ponto de controle do início da largura e altura da forma relativa da curva. e as coordenadas *x* e *y* do ponto de controle do fim da largura e altura da forma relativa da curva.</span><span class="sxs-lookup"><span data-stu-id="1846b-104">Contains the  *x*  - and  *y*  -coordinates of the endpoint of a cubic Bézier curve relative to the shape's width and height, the  *x*  - and  *y*  -coordinates of the control point of the beginning of the curve relative shape's width and height, and the  *x*  - and  *y*  -coordinates of the control point of the ending of the curve relative shape's width and height.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="1846b-105">Uma linha **RelCubBezTo** só pode persistir nos formatos de arquivo. vsdx,. vsdm,. vstx,. VSTM,. vssx e. vssm.</span><span class="sxs-lookup"><span data-stu-id="1846b-105">A **RelCubBezTo** row can only be persisted in the .vsdx, .vsdm, .vstx, .vstm, .vssx, and .vssm file formats.</span></span> <span data-ttu-id="1846b-106">Quando um arquivo é salvo nos formatos do Visio 2003-2010, a linha **RelCubBezTo** é convertida em uma linha [nurbsto](nurbsto-row-geometry-section.md) .</span><span class="sxs-lookup"><span data-stu-id="1846b-106">When a file is saved to the Visio 2003-2010 formats, the **RelCubBezTo** row is converted to a [NURBSTo](nurbsto-row-geometry-section.md) row.</span></span> 
  
<span data-ttu-id="1846b-107">Uma linha **RelCubBezTo** contém as células a seguir.</span><span class="sxs-lookup"><span data-stu-id="1846b-107">A **RelCubBezTo** row contains the following cells.</span></span> 
  
|<span data-ttu-id="1846b-108">**Cell**</span><span class="sxs-lookup"><span data-stu-id="1846b-108">**Cell**</span></span>|<span data-ttu-id="1846b-109">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="1846b-109">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1846b-110">X</span><span class="sxs-lookup"><span data-stu-id="1846b-110">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="1846b-111">A coordenada *x* do vértice final de uma curva Bézier cúbica em relação à largura da forma.</span><span class="sxs-lookup"><span data-stu-id="1846b-111">The  *x*  -coordinate of the ending vertex of a cubic Bézier curve relative to the width of the shape.</span></span>  <br/> |
|[<span data-ttu-id="1846b-112">Y</span><span class="sxs-lookup"><span data-stu-id="1846b-112">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="1846b-113">A coordenada *y* do vértice final de uma curva Bézier cúbica em relação à altura da forma.</span><span class="sxs-lookup"><span data-stu-id="1846b-113">The  *y*  -coordinate of the ending vertex of a cubic Bézier curve relative to the height of the shape.</span></span>  <br/> |
|[<span data-ttu-id="1846b-114">A</span><span class="sxs-lookup"><span data-stu-id="1846b-114">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="1846b-115">A coordenada *x* do ponto de controle inicial da curva em relação à largura da forma; um ponto no arco. O ponto de controle é melhor localizado entre os vértices inicial e final do arco.</span><span class="sxs-lookup"><span data-stu-id="1846b-115">The  *x*  -coordinate of the curve's beginning control point relative to the shape's width; a point on the arc. The control point is best located between the beginning and ending vertices of the arc.</span></span>  <br/> |
|[<span data-ttu-id="1846b-116">A.b.c.</span><span class="sxs-lookup"><span data-stu-id="1846b-116">B</span></span>](b-cell-geometry-section.md) <br/> |<span data-ttu-id="1846b-117">A coordenada *y* do ponto de controle inicial de uma curva em relação à altura da forma.</span><span class="sxs-lookup"><span data-stu-id="1846b-117">The  *y*  -coordinate of a curve's beginning control point relative to the shape's height.</span></span>  <br/> |
|[<span data-ttu-id="1846b-118">Unidade</span><span class="sxs-lookup"><span data-stu-id="1846b-118">C</span></span>](c-cell-geometry-section.md) <br/> |<span data-ttu-id="1846b-119">A coordenada *x* do ponto de controle final da curva em relação à largura da forma; um ponto no arco. O ponto de controle é melhor localizado entre o ponto de controle inicial e os vértices finais do arco.</span><span class="sxs-lookup"><span data-stu-id="1846b-119">The  *x*  -coordinate of the curve's ending control point relative to the shape's width; a point on the arc. The control point is best located between the beginning control point and ending vertices of the arc.</span></span>  <br/> |
|[<span data-ttu-id="1846b-120">D</span><span class="sxs-lookup"><span data-stu-id="1846b-120">D</span></span>](d-cell-geometry-section.md) <br/> |<span data-ttu-id="1846b-121">A coordenada *y* do ponto de controle final de uma curva em relação à altura da forma.</span><span class="sxs-lookup"><span data-stu-id="1846b-121">The  *y*  -coordinate of a curve's ending control point relative to the shape's height.</span></span>  <br/> |
   

