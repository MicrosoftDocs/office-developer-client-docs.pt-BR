---
title: Linha SplineStart (Seção Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm3055
localization_priority: Normal
ms.assetid: 8e327e00-0844-efa4-900b-6954d3b009bb
description: Contém x e y-coordenadas do segundo ponto de controle de uma spline, seu segundo nó, seu primeiro nó, o último nó e o grau da spline.
ms.openlocfilehash: 0944da12e6090fde41dc5927b5705e103d29f76d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773051"
---
# <a name="splinestart-row-geometry-section"></a>Linha SplineStart (Seção Geometry)

Contém *x* e *y* -coordenadas do segundo ponto de controle de uma spline, seu segundo nó, seu primeiro nó, o último nó e o grau da spline. 
  
Uma linha SplineStart contém as células a seguir.
  
|**Célula**|**Descrição**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |*X* -coordenadas do segundo ponto de controle de uma spline.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |*Y* -coordenadas do segundo ponto de controle de uma spline.  <br/> |
|[A](a-cell-geometry-section.md) <br/> |O segundo nó da spline.  <br/> |
|[B](b-cell-geometry-section.md) <br/> |O primeiro nó de uma spline.  <br/> |
|[C](c-cell-geometry-section.md) <br/> |O último nó de uma spline.  <br/> |
|[D](d-cell-geometry-section.md) <br/> |O grau de uma spline (um inteiro de 1 a 25).  <br/> |
   
## <a name="remarks"></a>Comentários

O Visio exibe a definição de uma spline em uma seção Geometry que contém uma linha SplineStart, seguida de uma ou mais linhas SplineKnot. A linha SplineStart tem que ser precedida de outro tipo de linha, assim como uma linha MoveTo, para indicar o primeiro ponto de controle da spline. A linha precedente pode ser uma linha LineTo, ArcTo, NURBSTo, PolylineTo ou EllipticalArcTo, no caso da spline acompanhar um segmento desse tipo.
  

