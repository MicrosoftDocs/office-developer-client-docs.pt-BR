---
title: Linha EllipticalArcTo (Seção Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm3015
localization_priority: Normal
ms.assetid: 7ceb30a8-1d05-feff-35d8-08a198784a27
description: Contém x e y-coordenadas do ponto de extremidade de um arco elíptico, x e y-coordenadas dos pontos de controle do arco, ângulo de x-eixo ao eixo principal da elipse e a razão entre os eixos principal e secundária da elipse.
ms.openlocfilehash: 9a356429f14a20b72a8bd55689855e2954d4a807
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771794"
---
# <a name="ellipticalarcto-row-geometry-section"></a><span data-ttu-id="cc90e-103">Linha EllipticalArcTo (Seção Geometry)</span><span class="sxs-lookup"><span data-stu-id="cc90e-103">EllipticalArcTo Row (Geometry Section)</span></span>

<span data-ttu-id="cc90e-104">Contém *x* e *y* - coordenadas do ponto de extremidade do arco elíptico, *x* - e *y* -coordenadas dos pontos de controle do arco, ângulo do *x* -eixo ao eixo principal da elipse e proporção entre principal da elipse e secundária eixos r.</span><span class="sxs-lookup"><span data-stu-id="cc90e-104">Contains  *x*  - and  *y*  -coordinates of an elliptical arc's endpoint,  *x*  - and  *y*  -coordinates of the control points on the arc, angle from the  *x*  -axis to the ellipse's major axis, and ratio between the ellipse's major and minor axes.</span></span> 
  
<span data-ttu-id="cc90e-105">Uma linha EllipticalArcTo contém as células a seguir.</span><span class="sxs-lookup"><span data-stu-id="cc90e-105">An EllipticalArcTo row contains the following cells.</span></span>
  
|<span data-ttu-id="cc90e-106">**Célula**</span><span class="sxs-lookup"><span data-stu-id="cc90e-106">**Cell**</span></span>|<span data-ttu-id="cc90e-107">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="cc90e-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cc90e-108">X</span><span class="sxs-lookup"><span data-stu-id="cc90e-108">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="cc90e-109">*X* -coordenadas do vértice final em um arco.</span><span class="sxs-lookup"><span data-stu-id="cc90e-109">The  *x*  -coordinate of the ending vertex on an arc.</span></span>  <br/> |
|[<span data-ttu-id="cc90e-110">Y</span><span class="sxs-lookup"><span data-stu-id="cc90e-110">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="cc90e-111">*Y* -coordenadas do vértice final em um arco.</span><span class="sxs-lookup"><span data-stu-id="cc90e-111">The  *y*  -coordinate of the ending vertex on an arc.</span></span>  <br/> |
|[<span data-ttu-id="cc90e-112">A</span><span class="sxs-lookup"><span data-stu-id="cc90e-112">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="cc90e-113">*X* -coordenadas do ponto de controle do arco; um ponto do arco. O ponto de controle está localizado melhor sobre na metade entre exagerada vértices do arco. Caso contrário, o arco pode aumentar para um tamanho extremo para passar pelo ponto de controle, com resultados imprevisíveis.</span><span class="sxs-lookup"><span data-stu-id="cc90e-113">The  *x*  -coordinate of the arc's control point; a point on the arc. The control point is best located about halfway between the beginning and ending vertices of the arc. Otherwise, the arc may grow to an extreme size in order to pass through the control point, with unpredictable results.</span></span>  <br/> |
|[<span data-ttu-id="cc90e-114">B</span><span class="sxs-lookup"><span data-stu-id="cc90e-114">B</span></span>](b-cell-geometry-section.md) <br/> |<span data-ttu-id="cc90e-115">*Y* -coordenadas do ponto de controle do arco.</span><span class="sxs-lookup"><span data-stu-id="cc90e-115">The  *y*  -coordinate of an arc's control point.</span></span>  <br/> |
|[<span data-ttu-id="cc90e-116">C</span><span class="sxs-lookup"><span data-stu-id="cc90e-116">C</span></span>](c-cell-geometry-section.md) <br/> |<span data-ttu-id="cc90e-117">O ângulo do eixo de principal do arco em relação a *x* -o eixo de seu pai.</span><span class="sxs-lookup"><span data-stu-id="cc90e-117">The angle of an arc's major axis relative to the  *x*  -axis of its parent.</span></span>  <br/> |
|[<span data-ttu-id="cc90e-118">D</span><span class="sxs-lookup"><span data-stu-id="cc90e-118">D</span></span>](d-cell-geometry-section.md) <br/> |<span data-ttu-id="cc90e-p101">A razão entre os eixos principal e secundário de um arco. Apesar do significado comum dessas palavras, o eixo "principal" não precisa ser maior que o eixo "secundário". Logo, a razão não precisa ser maior que 1. Definir esta célula para um valor menor ou igual a 0, ou maior que 1000, pode ocasionar resultados imprevisíveis.</span><span class="sxs-lookup"><span data-stu-id="cc90e-p101">The ratio of an arc's major axis to its minor axis. Despite the usual meaning of these words, the "major" axis does not have to be greater than the "minor" axis, so this ratio does not have to be greater than 1. Setting this cell to a value less than or equal to 0 or greater than 1000 can lead to unpredictable results.</span></span>  <br/> |
   

