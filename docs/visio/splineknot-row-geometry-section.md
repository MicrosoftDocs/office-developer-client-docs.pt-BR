---
title: Linha SplineKnot (Seção Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm3050
localization_priority: Normal
ms.assetid: 9fbae27d-4f1b-c5f7-aacb-16f359331e83
description: Contém as coordenadas x e y para o ponto de controle de uma spline e o nó de uma spline.
ms.openlocfilehash: 432b714772d96e0ab0861bbfb62075258404e607
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407414"
---
# <a name="splineknot-row-geometry-section"></a>Linha SplineKnot (Seção Geometry)

Contém as coordenadas *x* e *y* para o ponto de controle de uma spline e o nó de uma spline. 
  
Uma linha SplineKnot contém as células a seguir.
  
|**Célula**|**Descrição**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |A coordenada *x* de um ponto de controle.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |A coordenada *y* de um ponto de controle.  <br/> |
|[A](a-cell-geometry-section.md) <br/> |Um dos nós da spline (exceto o último ou os dois primeiros).  <br/> |
   
## <a name="remarks"></a>Comentários

O Visio exibe a definição de uma spline em uma seção Geometry que contém uma linha SplineStart, seguida de uma ou mais linhas SplineKnot. A linha SplineStart tem que ser precedida de outro tipo de linha, assim como uma linha MoveTo, para indicar o primeiro ponto de controle da spline. A linha precedente pode ser uma linha LineTo, ArcTo, NURBSTo, PolylineTo ou EllipticalArcTo, no caso da spline acompanhar um segmento desse tipo.
  

