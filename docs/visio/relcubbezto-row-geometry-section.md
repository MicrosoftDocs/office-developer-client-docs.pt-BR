---
title: Linha RelCubBezTo (Seção Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 77777dd4-5a2c-4048-9ea4-9bd876862963
description: Contém as coordenadas x e y do ponto de extremidade de uma curva de Bézier cúbica relativas à largura e altura da forma, às coordenadas x e y do ponto de controle do início da largura e altura da forma relativa da curva e as coordenadas x - e y -do ponto de controle do final da largura e altura da forma relativa da curva.
ms.openlocfilehash: cb886706c4c5cbb3488a95b57dcc84e0e45ee326
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430326"
---
# <a name="relcubbezto-row-geometry-section"></a><span data-ttu-id="b065f-103">Linha RelCubBezTo (Seção Geometry)</span><span class="sxs-lookup"><span data-stu-id="b065f-103">RelCubBezTo Row (Geometry Section)</span></span>

<span data-ttu-id="b065f-104">Contém as coordenadas  *x*  e  *y*  do ponto de extremidade de uma curva de Bézier cúbica relativas à largura e altura da forma, às coordenadas  *x*  e  *y*  do ponto de controle do início da largura e altura da forma relativa da curva e as coordenadas  *x*  - e  *y -do*  ponto de controle do final da largura e altura da forma relativa da curva.</span><span class="sxs-lookup"><span data-stu-id="b065f-104">Contains the  *x*  - and  *y*  -coordinates of the endpoint of a cubic Bézier curve relative to the shape's width and height, the  *x*  - and  *y*  -coordinates of the control point of the beginning of the curve relative shape's width and height, and the  *x*  - and  *y*  -coordinates of the control point of the ending of the curve relative shape's width and height.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="b065f-105">Uma **linha RelCubBezTo** só pode ser persistente nos formatos de arquivo .vsdx, .vsdm, .vstx, .vstm, .vssx e .vssm.</span><span class="sxs-lookup"><span data-stu-id="b065f-105">A **RelCubBezTo** row can only be persisted in the .vsdx, .vsdm, .vstx, .vstm, .vssx, and .vssm file formats.</span></span> <span data-ttu-id="b065f-106">Quando um arquivo é salvo nos formatos Visio 2003-2010, a linha **RelCubBezTo** é convertida em uma [linha NURBSTo.](nurbsto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="b065f-106">When a file is saved to the Visio 2003-2010 formats, the **RelCubBezTo** row is converted to a [NURBSTo](nurbsto-row-geometry-section.md) row.</span></span> 
  
<span data-ttu-id="b065f-107">Uma **linha RelCubBezTo** contém as células a seguir.</span><span class="sxs-lookup"><span data-stu-id="b065f-107">A **RelCubBezTo** row contains the following cells.</span></span> 
  
|<span data-ttu-id="b065f-108">**Célula**</span><span class="sxs-lookup"><span data-stu-id="b065f-108">**Cell**</span></span>|<span data-ttu-id="b065f-109">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="b065f-109">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b065f-110">X</span><span class="sxs-lookup"><span data-stu-id="b065f-110">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="b065f-111">A  *coordenada x*  do vértice final de uma curva de Bézier cúbica relativa à largura da forma.</span><span class="sxs-lookup"><span data-stu-id="b065f-111">The  *x*  -coordinate of the ending vertex of a cubic Bézier curve relative to the width of the shape.</span></span>  <br/> |
|[<span data-ttu-id="b065f-112">Y</span><span class="sxs-lookup"><span data-stu-id="b065f-112">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="b065f-113">A  *coordenada y*  do vértice final de uma curva de Bézier cúbica relativa à altura da forma.</span><span class="sxs-lookup"><span data-stu-id="b065f-113">The  *y*  -coordinate of the ending vertex of a cubic Bézier curve relative to the height of the shape.</span></span>  <br/> |
|[<span data-ttu-id="b065f-114">A</span><span class="sxs-lookup"><span data-stu-id="b065f-114">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="b065f-115">A  *coordenada x*  do ponto de controle inicial da curva em relação à largura da forma; um ponto no arco. O ponto de controle é melhor localizado entre os vértices inicial e final do arco.</span><span class="sxs-lookup"><span data-stu-id="b065f-115">The  *x*  -coordinate of the curve's beginning control point relative to the shape's width; a point on the arc. The control point is best located between the beginning and ending vertices of the arc.</span></span>  <br/> |
|[<span data-ttu-id="b065f-116">B</span><span class="sxs-lookup"><span data-stu-id="b065f-116">B</span></span>](b-cell-geometry-section.md) <br/> |<span data-ttu-id="b065f-117">A  *coordenada y*  do ponto de controle inicial de uma curva em relação à altura da forma.</span><span class="sxs-lookup"><span data-stu-id="b065f-117">The  *y*  -coordinate of a curve's beginning control point relative to the shape's height.</span></span>  <br/> |
|[<span data-ttu-id="b065f-118">C</span><span class="sxs-lookup"><span data-stu-id="b065f-118">C</span></span>](c-cell-geometry-section.md) <br/> |<span data-ttu-id="b065f-119">A  *coordenada x*  do ponto de controle final da curva em relação à largura da forma; um ponto no arco. O ponto de controle é melhor localizado entre o ponto de controle inicial e os vértices finais do arco.</span><span class="sxs-lookup"><span data-stu-id="b065f-119">The  *x*  -coordinate of the curve's ending control point relative to the shape's width; a point on the arc. The control point is best located between the beginning control point and ending vertices of the arc.</span></span>  <br/> |
|[<span data-ttu-id="b065f-120">D</span><span class="sxs-lookup"><span data-stu-id="b065f-120">D</span></span>](d-cell-geometry-section.md) <br/> |<span data-ttu-id="b065f-121">A  *coordenada y*  do ponto de controle final de uma curva em relação à altura da forma.</span><span class="sxs-lookup"><span data-stu-id="b065f-121">The  *y*  -coordinate of a curve's ending control point relative to the shape's height.</span></span>  <br/> |
   

