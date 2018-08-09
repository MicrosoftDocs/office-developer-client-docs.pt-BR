---
title: Linha RelCubBezTo (Seção Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 77777dd4-5a2c-4048-9ea4-9bd876862963
description: Contém x - e y - coordenadas do ponto de extremidade de uma curva de Bézier cúbica em relação à largura da forma e a altura, x - e y - coordenadas do ponto de controle do início da largura da forma relativa curva e altura e o x - e y-coordenadas do contro l ponto do final da largura e a altura da forma relativa curva.
ms.openlocfilehash: 918701c19e36753dcbf1a210dda2234d1e540d6d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772675"
---
# <a name="relcubbezto-row-geometry-section"></a><span data-ttu-id="b735e-103">Linha RelCubBezTo (Seção Geometry)</span><span class="sxs-lookup"><span data-stu-id="b735e-103">RelCubBezTo Row (Geometry Section)</span></span>

<span data-ttu-id="b735e-104">Contém os *x* e *y* - coordenadas do ponto de extremidade de uma curva de Bézier cúbica em relação à largura da forma e a altura, *x* - e *y* -coordenadas do ponto de controle do início da largura e a altura da forma relativa curva e o *x* e *y* -coordenadas do ponto de controle do final da largura e a altura da forma relativa curva.</span><span class="sxs-lookup"><span data-stu-id="b735e-104">Contains the  *x*  - and  *y*  -coordinates of the endpoint of a cubic Bézier curve relative to the shape's width and height, the  *x*  - and  *y*  -coordinates of the control point of the beginning of the curve relative shape's width and height, and the  *x*  - and  *y*  -coordinates of the control point of the ending of the curve relative shape's width and height.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="b735e-105">Uma linha **RelCubBezTo** só pode ser mantida nos formatos de arquivo. vsdx,. vsdm,. vstx,. vstm,. vssx e. vssm.</span><span class="sxs-lookup"><span data-stu-id="b735e-105">A **RelCubBezTo** row can only be persisted in the .vsdx, .vsdm, .vstx, .vstm, .vssx, and .vssm file formats.</span></span> <span data-ttu-id="b735e-106">Quando um arquivo é salva para os formatos de 2010 do Visio 2003, a linha **RelCubBezTo** é convertida em uma linha [NURBSTo](nurbsto-row-geometry-section.md) .</span><span class="sxs-lookup"><span data-stu-id="b735e-106">When a file is saved to the Visio 2003-2010 formats, the **RelCubBezTo** row is converted to a [NURBSTo](nurbsto-row-geometry-section.md) row.</span></span> 
  
<span data-ttu-id="b735e-107">Uma linha de **RelCubBezTo** contém as células a seguir.</span><span class="sxs-lookup"><span data-stu-id="b735e-107">A **RelCubBezTo** row contains the following cells.</span></span> 
  
|<span data-ttu-id="b735e-108">**Célula**</span><span class="sxs-lookup"><span data-stu-id="b735e-108">**Cell**</span></span>|<span data-ttu-id="b735e-109">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="b735e-109">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b735e-110">X</span><span class="sxs-lookup"><span data-stu-id="b735e-110">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="b735e-111">*X* -coordenadas do vértice final de uma curva de Bézier cúbica relativa à largura da forma.</span><span class="sxs-lookup"><span data-stu-id="b735e-111">The  *x*  -coordinate of the ending vertex of a cubic Bézier curve relative to the width of the shape.</span></span>  <br/> |
|[<span data-ttu-id="b735e-112">Y</span><span class="sxs-lookup"><span data-stu-id="b735e-112">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="b735e-113">*Y* -coordenadas do vértice final de uma curva de Bézier cúbica relativa à altura da forma.</span><span class="sxs-lookup"><span data-stu-id="b735e-113">The  *y*  -coordinate of the ending vertex of a cubic Bézier curve relative to the height of the shape.</span></span>  <br/> |
|[<span data-ttu-id="b735e-114">A</span><span class="sxs-lookup"><span data-stu-id="b735e-114">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="b735e-115">*X* -coordenadas da curva inicial do ponto de controle em relação à largura da forma; um ponto do arco. O ponto de controle é melhor localizado entre o início e fim vértices do arco.</span><span class="sxs-lookup"><span data-stu-id="b735e-115">The  *x*  -coordinate of the curve's beginning control point relative to the shape's width; a point on the arc. The control point is best located between the beginning and ending vertices of the arc.</span></span>  <br/> |
|[<span data-ttu-id="b735e-116">B</span><span class="sxs-lookup"><span data-stu-id="b735e-116">B</span></span>](b-cell-geometry-section.md) <br/> |<span data-ttu-id="b735e-117">*Y* -coordenadas de uma curva inicial do ponto de controle em relação à altura da forma.</span><span class="sxs-lookup"><span data-stu-id="b735e-117">The  *y*  -coordinate of a curve's beginning control point relative to the shape's height.</span></span>  <br/> |
|[<span data-ttu-id="b735e-118">C</span><span class="sxs-lookup"><span data-stu-id="b735e-118">C</span></span>](c-cell-geometry-section.md) <br/> |<span data-ttu-id="b735e-119">*X* -coordenadas da curva final do ponto de controle em relação à largura da forma; um ponto do arco. O ponto de controle é melhor localizado entre os vértices início de ponto de e terminando de controle do arco.</span><span class="sxs-lookup"><span data-stu-id="b735e-119">The  *x*  -coordinate of the curve's ending control point relative to the shape's width; a point on the arc. The control point is best located between the beginning control point and ending vertices of the arc.</span></span>  <br/> |
|[<span data-ttu-id="b735e-120">D</span><span class="sxs-lookup"><span data-stu-id="b735e-120">D</span></span>](d-cell-geometry-section.md) <br/> |<span data-ttu-id="b735e-121">*Y* -coordenadas de uma curva final do ponto de controle em relação à altura da forma.</span><span class="sxs-lookup"><span data-stu-id="b735e-121">The  *y*  -coordinate of a curve's ending control point relative to the shape's height.</span></span>  <br/> |
   

