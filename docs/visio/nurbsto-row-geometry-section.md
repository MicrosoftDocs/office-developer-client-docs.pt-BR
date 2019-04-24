---
title: Linha NURBSTo (Seção Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251758
localization_priority: Normal
ms.assetid: 7e47acfe-5ec0-3689-eb89-0168f596a739
description: Contém as coordenadas x e y, a posição do segundo para o último nó, a posição da última espessura, a posição do primeiro nó, a posição da primeira espessura e a fórmula de uma B-spline racional não-uniforme (NURBS).
ms.openlocfilehash: a5fc83f9581277580d076c2a850bfe937602aef0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361016"
---
# <a name="nurbsto-row-geometry-section"></a><span data-ttu-id="4a964-103">Linha NURBSTo (Seção Geometry)</span><span class="sxs-lookup"><span data-stu-id="4a964-103">NURBSTo Row (Geometry Section)</span></span>

<span data-ttu-id="4a964-104">Contém as coordenadas *x* e *y* , a posição do segundo para o último nó, a posição da última espessura, a posição do primeiro nó, a posição da primeira espessura e A fórmula de uma B-spline racional não-uniforme (NURBS).</span><span class="sxs-lookup"><span data-stu-id="4a964-104">Contains the  *x*  - and  *y*  -coordinates, position of the second to last knot, position of the last weight, position of the first knot, position of the first weight, and the formula for a nonuniform rational B-spline (NURBS).</span></span> 
  
<span data-ttu-id="4a964-105">Uma linha NURBSTo contém as células a seguir.</span><span class="sxs-lookup"><span data-stu-id="4a964-105">A NURBSTo row contains the following cells.</span></span>
  
|<span data-ttu-id="4a964-106">**Cell**</span><span class="sxs-lookup"><span data-stu-id="4a964-106">**Cell**</span></span>|<span data-ttu-id="4a964-107">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="4a964-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4a964-108">X</span><span class="sxs-lookup"><span data-stu-id="4a964-108">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="4a964-109">A coordenada *x* do último ponto de controle de uma NURBS.</span><span class="sxs-lookup"><span data-stu-id="4a964-109">The  *x*  -coordinate of the last control point of a NURBS.</span></span>  <br/> |
|[<span data-ttu-id="4a964-110">Y</span><span class="sxs-lookup"><span data-stu-id="4a964-110">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="4a964-111">A coordenada *y* do último ponto de controle de uma NURBS.</span><span class="sxs-lookup"><span data-stu-id="4a964-111">The  *y*  -coordinate of the last control point of a NURBS.</span></span>  <br/> |
|[<span data-ttu-id="4a964-112">A</span><span class="sxs-lookup"><span data-stu-id="4a964-112">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="4a964-113">O penúltimo nó de uma NURBS.</span><span class="sxs-lookup"><span data-stu-id="4a964-113">The second to the last knot of the NURBS.</span></span>  <br/> |
|[<span data-ttu-id="4a964-114">A.b.c.</span><span class="sxs-lookup"><span data-stu-id="4a964-114">B</span></span>](b-cell-geometry-section.md) <br/> |<span data-ttu-id="4a964-115">A última espessura de uma NURBS.</span><span class="sxs-lookup"><span data-stu-id="4a964-115">The last weight of the NURBS.</span></span>  <br/> |
|[<span data-ttu-id="4a964-116">Unidade</span><span class="sxs-lookup"><span data-stu-id="4a964-116">C</span></span>](c-cell-geometry-section.md) <br/> |<span data-ttu-id="4a964-117">O primeiro nó de uma NURBS.</span><span class="sxs-lookup"><span data-stu-id="4a964-117">The first knot of the NURBS.</span></span>  <br/> |
|[<span data-ttu-id="4a964-118">D</span><span class="sxs-lookup"><span data-stu-id="4a964-118">D</span></span>](d-cell-geometry-section.md) <br/> |<span data-ttu-id="4a964-119">A primeira espessura de uma NURBS.</span><span class="sxs-lookup"><span data-stu-id="4a964-119">The first weight of the NURBS.</span></span>  <br/> |
|[<span data-ttu-id="4a964-120">E</span><span class="sxs-lookup"><span data-stu-id="4a964-120">E</span></span>](e-cell-geometry-section.md) <br/> |<span data-ttu-id="4a964-121">Uma fórmula NURBS.</span><span class="sxs-lookup"><span data-stu-id="4a964-121">A NURBS formula.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4a964-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="4a964-122">Remarks</span></span>

<span data-ttu-id="4a964-p101">Uma NURBS é um meio comum de representar matematicamente uma curva. Crie uma NURBS com a ferramenta **Forma Livre**.</span><span class="sxs-lookup"><span data-stu-id="4a964-p101">NURBS is a common way to represent a curve mathematically. You can create a NURBS with the **Freeform** tool.</span></span> 
  

