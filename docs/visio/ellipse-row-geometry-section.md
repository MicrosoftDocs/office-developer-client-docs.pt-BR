---
title: Linha Ellipse (Seção Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm3010
localization_priority: Normal
ms.assetid: 183fb303-4acb-a486-7b97-f11f7ae3978f
description: Contém as coordenadas x e y do ponto central da elipse e dois pontos na elipse.
ms.openlocfilehash: 5121ba0c7bf97eaeaaf8a438dd40eccddada4362
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421827"
---
# <a name="ellipse-row-geometry-section"></a><span data-ttu-id="470c0-103">Linha Ellipse (Seção Geometry)</span><span class="sxs-lookup"><span data-stu-id="470c0-103">Ellipse Row (Geometry Section)</span></span>

<span data-ttu-id="470c0-104">Contém as coordenadas *x* e *y* do ponto central da elipse e dois pontos na elipse.</span><span class="sxs-lookup"><span data-stu-id="470c0-104">Contains the  *x*  - and  *y*  -coordinates of the ellipse's center point and two points on the ellipse.</span></span> 
  
<span data-ttu-id="470c0-105">Uma linha Ellipse contém as células a seguir.</span><span class="sxs-lookup"><span data-stu-id="470c0-105">An Ellipse row contains the following cells.</span></span>
  
|<span data-ttu-id="470c0-106">**Célula**</span><span class="sxs-lookup"><span data-stu-id="470c0-106">**Cell**</span></span>|<span data-ttu-id="470c0-107">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="470c0-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="470c0-108">X</span><span class="sxs-lookup"><span data-stu-id="470c0-108">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="470c0-109">A coordenada *x* do ponto central.</span><span class="sxs-lookup"><span data-stu-id="470c0-109">The  *x*  -coordinate of the center point.</span></span>  <br/> |
|[<span data-ttu-id="470c0-110">Y</span><span class="sxs-lookup"><span data-stu-id="470c0-110">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="470c0-111">A coordenada *y* do ponto central.</span><span class="sxs-lookup"><span data-stu-id="470c0-111">The  *y*  -coordinate of the center point.</span></span>  <br/> |
|[<span data-ttu-id="470c0-112">A</span><span class="sxs-lookup"><span data-stu-id="470c0-112">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="470c0-113">A coordenada x de um ponto na elipse; emparelhado com a coordenada *y* representada pela célula B.</span><span class="sxs-lookup"><span data-stu-id="470c0-113">The x-coordinate of one point on the ellipse; paired with  *y*  -coordinate represented by the B cell.</span></span>  <br/> |
|[<span data-ttu-id="470c0-114">A.b.c.</span><span class="sxs-lookup"><span data-stu-id="470c0-114">B</span></span>](b-cell-geometry-section.md) <br/> |<span data-ttu-id="470c0-115">A coordenada *y* de um ponto na elipse; emparelhado com a coordenada x representada pela célula a.</span><span class="sxs-lookup"><span data-stu-id="470c0-115">The  *y*  -coordinate of one point on the ellipse; paired with x-coordinate represented by the A cell.</span></span>  <br/> |
|[<span data-ttu-id="470c0-116">Unidade</span><span class="sxs-lookup"><span data-stu-id="470c0-116">C</span></span>](c-cell-geometry-section.md) <br/> |<span data-ttu-id="470c0-117">A coordenada *x* de outro ponto na elipse; emparelhado com a coordenada *y* representada pela célula D.</span><span class="sxs-lookup"><span data-stu-id="470c0-117">The  *x*  -coordinate of another point on the ellipse; paired with  *y*  -coordinate represented by the D cell.</span></span>  <br/> |
|[<span data-ttu-id="470c0-118">D</span><span class="sxs-lookup"><span data-stu-id="470c0-118">D</span></span>](d-cell-geometry-section.md) <br/> |<span data-ttu-id="470c0-119">A coordenada *y* de outro ponto na elipse; emparelhado com a coordenada *y* representada pela célula C.</span><span class="sxs-lookup"><span data-stu-id="470c0-119">The  *y*  -coordinate of another point on the ellipse; paired with  *y*  -coordinate represented by the C cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="470c0-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="470c0-120">Remarks</span></span>

<span data-ttu-id="470c0-121">Uma seção Geometry que contém uma linha Ellipse ou InfiniteLine não deveria conter qualquer outra linha.</span><span class="sxs-lookup"><span data-stu-id="470c0-121">A geometry section that contains an Ellipse or an InfiniteLine row should not contain any other rows.</span></span>
  

