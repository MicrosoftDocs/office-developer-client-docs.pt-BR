---
title: Linha RelLineTo (seção geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a900e174-d26a-4314-ae4f-d89e186350ce
description: Contém as coordenadas x e y do vértice final de um segmento de linha reta em relação à largura e à altura de uma forma.
ms.openlocfilehash: 2e85033b4a2e16c2df09b1a09655fcd4b97dd03d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437158"
---
# <a name="rellineto-row-geometry-section"></a><span data-ttu-id="6eb77-103">Linha RelLineTo (seção geometry)</span><span class="sxs-lookup"><span data-stu-id="6eb77-103">RelLineTo Row (Geometry Section)</span></span>

<span data-ttu-id="6eb77-104">Contém as coordenadas *x* e *y* do vértice final de um segmento de linha reta em relação à largura e à altura de uma forma.</span><span class="sxs-lookup"><span data-stu-id="6eb77-104">Contains  *x*  -and  *y*  -coordinates of the ending vertex of a straight line segment relative to a shape's width and height.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="6eb77-105">Uma linha **RelLineTo** só pode persistir nos formatos de arquivo. vsdx,. vsdm,. vstx,. VSTM,. vssx e. vssm.</span><span class="sxs-lookup"><span data-stu-id="6eb77-105">A **RelLineTo** row can only be persisted in the .vsdx, .vsdm, .vstx, .vstm, .vssx, and .vssm file formats.</span></span> <span data-ttu-id="6eb77-106">Quando um arquivo é salvo nos formatos do Visio 2003-2010, a linha **RelLineTo** é convertida em uma linha [LineTo](lineto-row-geometry-section.md) .</span><span class="sxs-lookup"><span data-stu-id="6eb77-106">When a file is saved to the Visio 2003-2010 formats, the **RelLineTo** row is converted to a [LineTo](lineto-row-geometry-section.md) row.</span></span> 
  
<span data-ttu-id="6eb77-107">Uma linha **RelLineTo** contém as células a seguir.</span><span class="sxs-lookup"><span data-stu-id="6eb77-107">A **RelLineTo** row contains the following cells.</span></span> 
  
|<span data-ttu-id="6eb77-108">**Célula**</span><span class="sxs-lookup"><span data-stu-id="6eb77-108">**Cell**</span></span>|<span data-ttu-id="6eb77-109">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="6eb77-109">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6eb77-110">X</span><span class="sxs-lookup"><span data-stu-id="6eb77-110">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="6eb77-111">A coordenada *x* do vértice final de um segmento de linha reta em relação à largura da forma.</span><span class="sxs-lookup"><span data-stu-id="6eb77-111">The  *x*  -coordinate of the ending vertex of a straight line segment relative to the shape's width.</span></span>  <br/> |
|[<span data-ttu-id="6eb77-112">Y</span><span class="sxs-lookup"><span data-stu-id="6eb77-112">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="6eb77-113">A coordenada *y* do vértice final de um segmento de linha reta em relação à altura da forma.</span><span class="sxs-lookup"><span data-stu-id="6eb77-113">The  *y*  -coordinate of the ending vertex of a straight line segment relative to the shape's height.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6eb77-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="6eb77-114">Remarks</span></span>

<span data-ttu-id="6eb77-115">Os valores na linha **RelLineTo** são equivalentes a valores em uma linha [LineTo](lineto-row-geometry-section.md) que são multiplicados pela largura e altura da forma.</span><span class="sxs-lookup"><span data-stu-id="6eb77-115">Values in the **RelLineTo** row are equivalent to values in a [LineTo](lineto-row-geometry-section.md) row that are multiplied by the width and height of the shape.</span></span> <span data-ttu-id="6eb77-116">Por exemplo: uma linha **RelLineTo** em que o valor da célula **X** é "0" e o valor da célula **Y** é "0,5" pode ser substituído pela linha **LineTo** onde o valor da célula **X** é a fórmula "largura*0" e a célula **Y** é o fórmula "altura*0,5".</span><span class="sxs-lookup"><span data-stu-id="6eb77-116">For example: a **RelLineTo** row where the value of the **X** cell is "0" and the value of the **Y** cell is "0.5" can be replaced with **LineTo** row where the value of the **X** cell is the formula "Width*0" and the **Y** cell is the formula "Height*0.5."</span></span> 
  

