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
description: Contém as coordenadas x e y do ponto de extremidade, x e y de um arco elíptico - e as coordenadas y dos pontos de controle no arco, o ângulo do eixo x para o eixo principal da elipse e a proporção entre os eixos principal e secundário da elipse.
ms.openlocfilehash: c6db7560a05652ca3bfcadb2fd4857ac39370562
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421400"
---
# <a name="ellipticalarcto-row-geometry-section"></a><span data-ttu-id="b36b4-103">Linha EllipticalArcTo (Seção Geometry)</span><span class="sxs-lookup"><span data-stu-id="b36b4-103">EllipticalArcTo Row (Geometry Section)</span></span>

<span data-ttu-id="b36b4-104">Contém as coordenadas  *x*  e  *y*  do ponto de extremidade,  *x*  e y de um arco elíptico - e as coordenadas  *y*  dos pontos de controle no arco, o ângulo do eixo  *x*  para o eixo principal da elipse e a proporção entre os eixos principal e secundário da elipse.</span><span class="sxs-lookup"><span data-stu-id="b36b4-104">Contains  *x*  - and  *y*  -coordinates of an elliptical arc's endpoint,  *x*  - and  *y*  -coordinates of the control points on the arc, angle from the  *x*  -axis to the ellipse's major axis, and ratio between the ellipse's major and minor axes.</span></span> 
  
<span data-ttu-id="b36b4-105">Uma linha EllipticalArcTo contém as células a seguir.</span><span class="sxs-lookup"><span data-stu-id="b36b4-105">An EllipticalArcTo row contains the following cells.</span></span>
  
|<span data-ttu-id="b36b4-106">**Célula**</span><span class="sxs-lookup"><span data-stu-id="b36b4-106">**Cell**</span></span>|<span data-ttu-id="b36b4-107">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="b36b4-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b36b4-108">X</span><span class="sxs-lookup"><span data-stu-id="b36b4-108">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="b36b4-109">A  *coordenada x*  do vértice final em um arco.</span><span class="sxs-lookup"><span data-stu-id="b36b4-109">The  *x*  -coordinate of the ending vertex on an arc.</span></span>  <br/> |
|[<span data-ttu-id="b36b4-110">Y</span><span class="sxs-lookup"><span data-stu-id="b36b4-110">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="b36b4-111">A  *coordenada y*  do vértice final em um arco.</span><span class="sxs-lookup"><span data-stu-id="b36b4-111">The  *y*  -coordinate of the ending vertex on an arc.</span></span>  <br/> |
|[<span data-ttu-id="b36b4-112">A</span><span class="sxs-lookup"><span data-stu-id="b36b4-112">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="b36b4-113">A  *coordenada x*  do ponto de controle do arco; um ponto no arco. O ponto de controle é melhor localizado aproximadamente no meio dos vértices inicial e final do arco. Caso contrário, o arco pode aumentar até um tamanho extremo para passar pelo ponto de controle, com resultados imprevisíveis.</span><span class="sxs-lookup"><span data-stu-id="b36b4-113">The  *x*  -coordinate of the arc's control point; a point on the arc. The control point is best located about halfway between the beginning and ending vertices of the arc. Otherwise, the arc may grow to an extreme size in order to pass through the control point, with unpredictable results.</span></span>  <br/> |
|[<span data-ttu-id="b36b4-114">B</span><span class="sxs-lookup"><span data-stu-id="b36b4-114">B</span></span>](b-cell-geometry-section.md) <br/> |<span data-ttu-id="b36b4-115">A  *coordenada y*  do ponto de controle de um arco.</span><span class="sxs-lookup"><span data-stu-id="b36b4-115">The  *y*  -coordinate of an arc's control point.</span></span>  <br/> |
|[<span data-ttu-id="b36b4-116">C</span><span class="sxs-lookup"><span data-stu-id="b36b4-116">C</span></span>](c-cell-geometry-section.md) <br/> |<span data-ttu-id="b36b4-117">O ângulo do eixo principal de um arco em relação ao  *eixo x*  de seu pai.</span><span class="sxs-lookup"><span data-stu-id="b36b4-117">The angle of an arc's major axis relative to the  *x*  -axis of its parent.</span></span>  <br/> |
|[<span data-ttu-id="b36b4-118">D</span><span class="sxs-lookup"><span data-stu-id="b36b4-118">D</span></span>](d-cell-geometry-section.md) <br/> |<span data-ttu-id="b36b4-p101">A razão entre os eixos principal e secundário de um arco. Apesar do significado comum dessas palavras, o eixo "principal" não precisa ser maior que o eixo "secundário". Logo, a razão não precisa ser maior que 1. Definir esta célula para um valor menor ou igual a 0, ou maior que 1000, pode ocasionar resultados imprevisíveis.</span><span class="sxs-lookup"><span data-stu-id="b36b4-p101">The ratio of an arc's major axis to its minor axis. Despite the usual meaning of these words, the "major" axis does not have to be greater than the "minor" axis, so this ratio does not have to be greater than 1. Setting this cell to a value less than or equal to 0 or greater than 1000 can lead to unpredictable results.</span></span>  <br/> |
   

