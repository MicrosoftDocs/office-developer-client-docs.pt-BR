---
title: Linha RelQuadBezTo (Seção Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ae57707-5a50-43f0-8c78-516790b5034e
description: Contém os x e y - coordenadas do ponto de extremidade de uma curva de Bézier quadrática em relação à largura da forma e a altura e a x - e y-coordenadas do ponto de controle de largura e a altura da forma relativa curva.
ms.openlocfilehash: 99796e85a857fd320598cb48993fc29bdfa4964d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772723"
---
# <a name="relquadbezto-row-geometry-section"></a><span data-ttu-id="3260a-103">Linha RelQuadBezTo (Seção Geometry)</span><span class="sxs-lookup"><span data-stu-id="3260a-103">RelQuadBezTo Row (Geometry Section)</span></span>

<span data-ttu-id="3260a-104">Contém os *x* e *y* - coordenadas do ponto de extremidade de uma curva de Bézier quadrática em relação à largura da forma e a altura e o *x* - e *y* -coordenadas do ponto de controle de largura e a altura da forma relativa curva.</span><span class="sxs-lookup"><span data-stu-id="3260a-104">Contains the  *x*  - and  *y*  -coordinates of the endpoint of a quadratic Bézier curve relative to the shape's width and height and the  *x*  - and  *y*  -coordinates of the control point of the curve relative shape's width and height.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="3260a-105">Uma linha **RelQuadBezTo** só pode ser mantida nos formatos de arquivo. vsdx,. vsdm,. vstx,. vstm,. vssx e. vssm.</span><span class="sxs-lookup"><span data-stu-id="3260a-105">A **RelQuadBezTo** row can only be persisted in the .vsdx, .vsdm, .vstx, .vstm, .vssx, and .vssm file formats.</span></span> <span data-ttu-id="3260a-106">Quando um arquivo é salva para os formatos de 2010 do Visio 2003, a linha **RelQuadBezTo** é convertida em uma linha [NURBSTo](nurbsto-row-geometry-section.md) .</span><span class="sxs-lookup"><span data-stu-id="3260a-106">When a file is saved to the Visio 2003-2010 formats, the **RelQuadBezTo** row is converted to a [NURBSTo](nurbsto-row-geometry-section.md) row.</span></span> 
  
<span data-ttu-id="3260a-107">Uma linha de **RelQuadBezTo** contém as células a seguir.</span><span class="sxs-lookup"><span data-stu-id="3260a-107">A **RelQuadBezTo** row contains the following cells.</span></span> 
  
|<span data-ttu-id="3260a-108">**Célula**</span><span class="sxs-lookup"><span data-stu-id="3260a-108">**Cell**</span></span>|<span data-ttu-id="3260a-109">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="3260a-109">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3260a-110">X</span><span class="sxs-lookup"><span data-stu-id="3260a-110">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="3260a-111">*X* -coordenadas do vértice final de uma curva de Bézier quadrática relativa à largura da forma.</span><span class="sxs-lookup"><span data-stu-id="3260a-111">The  *x*  -coordinate of the ending vertex of a quadratic Bézier curve relative to the width of the shape.</span></span>  <br/> |
|[<span data-ttu-id="3260a-112">Y</span><span class="sxs-lookup"><span data-stu-id="3260a-112">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="3260a-113">*Y* -coordenadas do vértice final de uma curva de Bézier quadrática relativa à altura da forma.</span><span class="sxs-lookup"><span data-stu-id="3260a-113">The  *y*  -coordinate of the ending vertex of a quadratic Bézier curve relative to the height of the shape.</span></span>  <br/> |
|[<span data-ttu-id="3260a-114">A</span><span class="sxs-lookup"><span data-stu-id="3260a-114">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="3260a-115">*X* -coordenadas do ponto de controle da curva em relação à largura da forma; um ponto do arco. O ponto de controle está localizado melhor sobre na metade entre exagerada vértices do arco.</span><span class="sxs-lookup"><span data-stu-id="3260a-115">The  *x*  -coordinate of the curve's control point relative to the shape's width; a point on the arc. The control point is best located about halfway between the beginning and ending vertices of the arc.</span></span>  <br/> |
|[<span data-ttu-id="3260a-116">B</span><span class="sxs-lookup"><span data-stu-id="3260a-116">B</span></span>](b-cell-geometry-section.md) <br/> |<span data-ttu-id="3260a-117">*Y* -coordenadas do ponto de controle da curva em relação à altura da forma.</span><span class="sxs-lookup"><span data-stu-id="3260a-117">The  *y*  -coordinate of a curve's control point relative to the shape's height.</span></span>  <br/> |
   

