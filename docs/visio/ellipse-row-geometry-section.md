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
description: Contém os x e y-coordenadas do ponto central da elipse e dois pontos na elipse.
ms.openlocfilehash: 0a2acb0efa20f67d04581f827edbfc4fb4a2d6b0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771792"
---
# <a name="ellipse-row-geometry-section"></a><span data-ttu-id="724f0-103">Linha Ellipse (Seção Geometry)</span><span class="sxs-lookup"><span data-stu-id="724f0-103">Ellipse Row (Geometry Section)</span></span>

<span data-ttu-id="724f0-104">Contém os *x* e *y* -coordenadas do ponto central da elipse e dois pontos na elipse.</span><span class="sxs-lookup"><span data-stu-id="724f0-104">Contains the  *x*  - and  *y*  -coordinates of the ellipse's center point and two points on the ellipse.</span></span> 
  
<span data-ttu-id="724f0-105">Uma linha Ellipse contém as células a seguir.</span><span class="sxs-lookup"><span data-stu-id="724f0-105">An Ellipse row contains the following cells.</span></span>
  
|<span data-ttu-id="724f0-106">**Célula**</span><span class="sxs-lookup"><span data-stu-id="724f0-106">**Cell**</span></span>|<span data-ttu-id="724f0-107">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="724f0-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="724f0-108">X</span><span class="sxs-lookup"><span data-stu-id="724f0-108">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="724f0-109">*X* -coordenadas do ponto central.</span><span class="sxs-lookup"><span data-stu-id="724f0-109">The  *x*  -coordinate of the center point.</span></span>  <br/> |
|[<span data-ttu-id="724f0-110">Y</span><span class="sxs-lookup"><span data-stu-id="724f0-110">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="724f0-111">*Y* -coordenadas do ponto central.</span><span class="sxs-lookup"><span data-stu-id="724f0-111">The  *y*  -coordinate of the center point.</span></span>  <br/> |
|[<span data-ttu-id="724f0-112">A</span><span class="sxs-lookup"><span data-stu-id="724f0-112">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="724f0-113">A coordenada x de um ponto na elipse, juntamente com *y* -coordenada representada pela célula B.</span><span class="sxs-lookup"><span data-stu-id="724f0-113">The x-coordinate of one point on the ellipse; paired with  *y*  -coordinate represented by the B cell.</span></span>  <br/> |
|[<span data-ttu-id="724f0-114">B</span><span class="sxs-lookup"><span data-stu-id="724f0-114">B</span></span>](b-cell-geometry-section.md) <br/> |<span data-ttu-id="724f0-115">*Y* -coordenadas de um ponto na elipse, juntamente com a coordenada x representada pela célula.</span><span class="sxs-lookup"><span data-stu-id="724f0-115">The  *y*  -coordinate of one point on the ellipse; paired with x-coordinate represented by the A cell.</span></span>  <br/> |
|[<span data-ttu-id="724f0-116">C</span><span class="sxs-lookup"><span data-stu-id="724f0-116">C</span></span>](c-cell-geometry-section.md) <br/> |<span data-ttu-id="724f0-117">*X* -coordenadas de um outro ponto na elipse; juntamente com *y* -coordenada representada pela célula D.</span><span class="sxs-lookup"><span data-stu-id="724f0-117">The  *x*  -coordinate of another point on the ellipse; paired with  *y*  -coordinate represented by the D cell.</span></span>  <br/> |
|[<span data-ttu-id="724f0-118">D</span><span class="sxs-lookup"><span data-stu-id="724f0-118">D</span></span>](d-cell-geometry-section.md) <br/> |<span data-ttu-id="724f0-119">*Y* -coordenadas de um outro ponto na elipse; juntamente com *y* -coordenada representada pela célula C.</span><span class="sxs-lookup"><span data-stu-id="724f0-119">The  *y*  -coordinate of another point on the ellipse; paired with  *y*  -coordinate represented by the C cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="724f0-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="724f0-120">Remarks</span></span>

<span data-ttu-id="724f0-121">Uma seção Geometry que contém uma linha Ellipse ou InfiniteLine não deveria conter qualquer outra linha.</span><span class="sxs-lookup"><span data-stu-id="724f0-121">A geometry section that contains an Ellipse or an InfiniteLine row should not contain any other rows.</span></span>
  

